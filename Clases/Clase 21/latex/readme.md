# Revisión Clase 21 — Modelos de difusión (parte III)

Revisión del beamer `slides.tex` y de las arquitecturas neuronales
(`images/attn_unet.pdf`, `images/cross_attn_unet.pdf`).
**No se modificó nada**: esto es solo un listado para que tú decidas qué cambiar.

---

## 1. Revisión del beamer

### Errores a corregir

1. **Coma espuria en una fórmula (línea 119).**
   En el frame *Classifier-free guidance*:
   ```latex
   \nabla_{x_t}\log q(y|x_t) = \nabla_{x_t}\log q(x_t|y) - \nabla_{x_t},\log q(x_t).
   ```
   Hay una coma sobrante antes de `\log` (`\nabla_{x_t},\log`). Debe ser
   `\nabla_{x_t}\log q(x_t)`. No rompe la compilación, pero se renderiza una coma
   visible en la ecuación.

2. **Dimensión de `y` inconsistente (líneas 57 vs 64).**
   - Línea 57: «$y\in\R^C$ es un vector».
   - Línea 64: «el embedding de la condición $y\in\R^D$».

   El mismo objeto `y` aparece con dos dimensiones distintas ($\R^C$ y $\R^D$).
   Además, $D$ ya está reservado para la **dimensión de los datos** en todo el
   curso ($\operatorname{I}_D$, $\mu_\theta:\R^D\times\{0,\ldots,T\}\to\R^D$ en la
   Clase 20), por lo que escribir $y\in\R^D$ colisiona con esa notación.
   Sugerencia: usar $\R^C$ en ambos lugares (o el símbolo que prefieras, pero
   distinto de $D$).

### Observaciones menores (estilo, opcional)

3. **Minúscula tras punto (líneas 119–120).** La ecuación termina en punto y la
   oración siguiente empieza con «por lo que…» en minúscula. Conviene reescribir
   (p. ej. quitar el punto de la ecuación, o capitalizar «Por lo que»).

4. **«p.g.» (líneas 60 y 159).** En español lo estándar es «p. ej.» (por ejemplo);
   «p.g.» no es una abreviatura correcta. **No es un error introducido en esta
   clase**: se usa de forma consistente en todo el curso (clases 02, 04, 06, 15,
   17…), así que probablemente es intencional. Lo dejo solo como nota por si
   quieres unificarlo a futuro.

### Cosas que verifiqué y están correctas ✓

- Reparametrización score-prediction (líneas 80–81): las expresiones de $\mu_q$ en
  función de $\epsilon$ y del score coinciden exactamente con las de la Clase 20
  (líneas 142 y 188).
- Relación $\epsilon = -\sqrt{1-\bar\alpha_t}\,\nabla_{x_t}\log q(x_t)$ (línea 85):
  correcta (se deduce igualando las dos expresiones de $x_0$ de la Clase 20).
- Classifier guidance (líneas 92–111): regla de Bayes
  $\nabla\log q(x_t|y)=\nabla\log q(y|x_t)+\nabla\log q(x_t)$ correcta; la
  interpretación como bajada de temperatura $\tilde q\propto q(y|x_t)^s q(x_t)$ es
  consistente con el escalamiento $s$.
- Classifier-free guidance (líneas 114–139): la sustitución y el resultado
  $\tilde q = s\,\nabla\log q(x_t|y)+(1-s)\,\nabla\log q(x_t)$ son correctos, así
  como la versión en $\epsilon$:
  $\tilde\epsilon = s\,\epsilon(x_t,t,y)+(1-s)\,\epsilon(x_t,t,\varnothing)$.
- Notación general ($\sim\mathcal N$, $\sigma_q^2(t)\operatorname{I}_D$,
  $\mu_\theta(x_t,t,y)$, $\bar\alpha_t$, $\varnothing$) consistente con clases
  previas.

### Nota sobre las imágenes de GLIDE (frame líneas 142–149)

Los **archivos parecen tener el contenido intercambiado respecto a su nombre**:

- `glide_guidance.pdf` muestra imágenes **borrosas/incoherentes** → corresponden a
  generación **sin** guidance.
- `glide_unguided.pdf` muestra imágenes **nítidas y bien alineadas con el prompt**
  → corresponden a generación **con** guidance.

En la diapositiva se colocan `glide_guidance` (izquierda) y `glide_unguided`
(derecha), con caption «simple (izquierda) y con guidance (derecha)». Como **ambos
archivos están cruzados**, el resultado renderizado queda visualmente correcto
(izquierda = borroso = simple; derecha = nítido = con guidance). Es decir, **la
diapositiva se ve bien**, pero los nombres de archivo son engañosos. Sugerencia:
renombrar los PDFs (intercambiarlos) para evitar confusión a futuro; si los
renombras, recuerda invertir también el orden en el `\includegraphics`.

---

## 2. Revisión de las arquitecturas

### `attn_unet.pdf` (inyección tipo FiLM) — Correcta ✓

- **Orden de bloques correcto:** cada nivel del encoder es `ResNet → Atención`;
  el cuello de botella es `ResNet → Atención → ResNet`; el decoder es
  `ResNet → Atención`. Es el orden estándar de una U-Net con atención.
- **Inyección de `t, y` (FiLM) en los bloques ResNet:** correcta. La modulación
  FiLM actúa sobre las features convolucionales, que viven en los bloques ResNet.
  Coincide con el texto de la diapositiva (línea 154: «en cada bloque
  convolucional»).
- **Skip connections** (líneas punteadas) del encoder al decoder a la misma
  resolución: correctas.
- *Comentario opcional (no es error):* en implementaciones reales la atención suele
  aplicarse solo en algunas resoluciones (las más bajas), no en todos los niveles.
  Como diagrama pedagógico está perfectamente bien mostrarla en todos.

### `cross_attn_unet.pdf` (atención cruzada) — Casi correcta, con una observación

- **Estructura idéntica** a la anterior. ✓
- **Inyección de la secuencia `y` (flechas verdes) en los bloques de Atención vía
  atención cruzada:** correcta. La cross-attention efectivamente vive en los
  bloques de atención. ✓
- **`t, y` (flechas moradas) sigue entrando por FiLM en los ResNet:** correcto que
  el tiempo `t` se inyecte siempre por ahí. ✓

- **⚠️ Observación principal — etiqueta del recuadro morado.**
  El recuadro morado dice «$t, y$» y el verde dice «$y$». Pero según la diapositiva
  (línea 159), en este caso `y` es una **secuencia de embeddings**
  $\{e_1,\ldots,e_L\}$. Una secuencia **no** puede inyectarse vía FiLM, porque FiLM
  requiere un **vector** (un único embedding) para producir los parámetros de
  escala/desplazamiento. Tal como está, la figura sugiere que el mismo `y` entra
  a la vez como vector (FiLM, morado) y como secuencia (cross-attention, verde),
  lo cual es inconsistente con el texto.

  **Sugerencias (elige una):**
  1. Cambiar el recuadro morado a solo «$t$» (lo más limpio: el tiempo por FiLM,
     la secuencia de texto por cross-attention).
  2. Si quieres mantener `y` en el camino FiLM, aclarar que ahí se usa un
     **embedding global / pooled** de `y` (un vector), distinto de la secuencia
     $\{e_1,\ldots,e_L\}$ que va por cross-attention. Esto sí ocurre en algunas
     arquitecturas (p. ej. el pooled text embedding de Stable Diffusion), pero
     conviene explicitarlo para no confundir.

- En resumen: **la información se inyecta en el lugar correcto** (FiLM en ResNet,
  cross-attention en los bloques de atención) y **el orden de los bloques es
  correcto**. El único punto a ajustar es la etiqueta «$t, y$» del recuadro morado
  para que sea coherente con que `y` es una secuencia.
