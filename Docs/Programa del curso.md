# Programa de Curso: MDS7203 - Modelos Generativos Profundos

## Resultados de Aprendizaje

Al finalizar el curso, el estudiante será capaz de:

1. **Comprender** los fundamentos teóricos y algorítmicos de los modelos generativos profundos y su diferencia con modelos discriminativos.
2. **Identificar** modelos generativos clásicos y del estado del arte, incluyendo LLMs y modelos de difusión.
3. **Analizar** las hipótesis, ventajas y limitaciones de distintas familias de modelos generativos según el contexto de aplicación.
4. **Implementar** modelos generativos profundos usando frameworks modernos (PyTorch, librerías Transformers y Diffusers).
5. **Evaluar** la pertinencia de un modelo generativo específico según el dominio y requerimientos del problema.
6. **Aplicar** técnicas de fine-tuning y optimización en problemas prácticos.

## Metodología Docente

- **Clases expositivas participativas:** teoría de cada técnica generativa junto con sus hipótesis, ventajas y limitaciones (3 horas/semana).
- **Trabajo dirigido:** implementación de modelos en sesiones auxiliares (1.5 horas/semana).
- **Trabajo personal:** revisión de material y desarrollo práctico (5.5 horas/semana).

## Evaluación General

- **Tareas (50%):** 3 tareas (semanas 5, 10 y 15).
- **Controles de lectura (50%):** 7 controles de lectura en clases (semanas impares desde la semana 3). Se elimina el peor control.
- Se requiere aprobar ambos ítems por separado.

## Unidades Temáticas

### Unidad 1: Introducción

**Duración:** 2 semanas

#### Contenidos

- Introducción al curso: motivación, objetivos y estructura.
- Repaso de conceptos previos: probabilidades, redes neuronales, optimización.
- Definición de modelo generativo y diferencia con modelo discriminativo.
- Redes bayesianas: motivación, formulación, ejemplos clásicos, conexión con modelos generativos modernos, modelos generativos condicionales, modelos de variable latente, estimación de parámetros.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Distinguir** modelos generativos de modelos discriminativos.
- **Interpretar** la notación de modelos gráficos probabilísticos.
- **Comprender** los fundamentos para generar realizaciones desde distribuciones de probabilidad.
- **Utilizar** PyTorch para implementar y entrenar modelos neuronales.

### Unidad 2: Modelos Autorregresivos y LLMs

**Duración:** 3 semanas

#### Contenidos

- Formulación de modelos autorregresivos (ARM) mediante factorización de probabilidades condicionales.
- Language modeling: tokenización (BPE, WordPiece, SentencePiece), arquitecturas recurrentes (RNN, LSTM, GRU), teacher forcing, estrategias de generación (greedy, beam search, sampling, top-k, top-p).
- Arquitectura GPT: mecanismo de self-attention, formulación matemática, implementación desde cero, entrenamiento y generación.
- Variantes de la arquitectura Transformer: tipos de tokenizadores, positional encoders (sinusoidal, RoPE, ALiBi), normalizaciones (LayerNorm, RMSNorm, pre-norm vs post-norm), mecanismos de atención (multi-head, grouped-query, flash attention), Mixture of Experts (MoE).
- Otros modelos tipo Transformer: BERT, CLIP, Vision Transformer, Chameleon, AlphaFold.
- Large Language Models (LLMs): chat templates, entrenamiento para interacción conversacional, uso práctico con herramientas como LM Studio.
- Propiedades empíricas de los LLMs: leyes de escala, habilidades emergentes (in-context learning, chain-of-thought), técnicas de prompting.
- Agentes basados en LLMs: Retrieval-Augmented Generation (RAG), uso de herramientas externas (function calling, tool use), implementación de agentes.
- Técnicas de inferencia eficiente: KV-caching, cuantización.
- Fine-tuning de LLMs: Supervised Fine-Tuning (SFT), heurísticas de entrenamiento, entrenamiento distribuido, Low-Rank Adaptation (LoRA, QLoRA), alignment (RLHF, DPO).
- Herramientas: librería Transformers de Hugging Face, uso de GPUs en la nube.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Explicar** el principio matemático de los modelos autorregresivos y su aplicación a language modeling.
- **Describir** la arquitectura Transformer y sus variantes modernas.
- **Implementar** modelos de lenguaje usando la librería Transformers.
- **Analizar** las propiedades empíricas de los LLMs y sus implicancias.
- **Diseñar** sistemas basados en agentes con RAG y uso de herramientas.
- **Aplicar** técnicas de fine-tuning eficiente (LoRA, RLHF/DPO) para adaptar LLMs.

### Unidad 3: Redes Generativas Adversarias

**Duración:** 2 semanas

#### Contenidos

- Formulación de GANs: redes generadora y discriminadora, función de costo minimax, implementación y entrenamiento.
- Generación condicional: conditional GANs (cGANs), generación condicionada por etiquetas o embeddings.
- Arquitecturas para GANs: convoluciones transpuestas, DCGAN, SAGAN, U-Net, ProGAN, StyleGAN, BigGAN, MuseGAN.
- Transferencia de estilo: pix2pix, CycleGAN.
- Nociones de transporte óptimo: problema de Kantorovich, distancia de Wasserstein.
- Métricas de evaluación: Fréchet Inception Distance (FID), Inception Score (IS).
- Wasserstein GAN (WGAN): formulación, gradient penalty, ventajas sobre GAN clásica.
- Limitaciones de GANs: mode collapse, inestabilidad de entrenamiento, dificultad de evaluación.
- Contexto histórico y evolución del campo.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Identificar** los componentes y la dinámica de entrenamiento de una GAN.
- **Comprender** la formulación minimax y su interpretación teórica.
- **Implementar** arquitecturas como DCGAN, SAGAN y U-Net.
- **Aplicar** técnicas de transferencia de estilo con pix2pix y CycleGAN.
- **Evaluar** modelos generativos usando métricas FID e IS.
- **Analizar** variantes basadas en transporte óptimo (WGAN) y sus ventajas.

### Unidad 4: Autoencoders Variacionales

**Duración:** 2 semanas

#### Contenidos

- Autoencoders clásicos: arquitectura encoder-decoder, relación con compresión y reducción de dimensionalidad.
- Introducción a los VAEs: motivación probabilística, diferencias con autoencoders determinísticos.
- Formulación del VAE: inferencia variacional, derivación de la cota inferior de la evidencia (ELBO), término de reconstrucción y regularización KL.
- Implementación de un VAE: caso gaussiano (para datos continuos) y caso Bernoulli (para imágenes).
- Truco de la reparametrización: motivación, formulación, importancia para backpropagation a través de variables estocásticas.
- Interpolación en el espacio latente y modificación de atributos: aritmética de vectores latentes, disentanglement.
- Variantes de VAEs: VRAE, continuous Bernoulli, beta-VAE, matrices de covarianza no diagonales, VQ-VAE.
- Herramientas: revisión de VAE usando la librería Diffusers de Hugging Face.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Comprender** el rol del espacio latente en autoencoders y su interpretación probabilística.
- **Derivar** el objetivo ELBO y sus componentes.
- **Explicar** el truco de la reparametrización y su necesidad para el entrenamiento.
- **Implementar** un VAE con diferentes distribuciones de salida.
- **Comparar** variantes de VAEs y contrastarlos con GANs.

### Unidad 5: Flujos Normalizantes

**Duración:** 1 semana

#### Contenidos

- Teorema de cambio de variable para densidades de probabilidad.
- Formulación de flujos normalizantes: composición de transformaciones invertibles, distribución base y distribución objetivo.
- Requisitos de las transformaciones: invertibilidad, computabilidad del jacobiano.
- Sampling y estimación de densidad en modelos de flujo.
- Ejemplos de flujos normalizantes: NICE, RealNVP.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Comprender** el principio de transformaciones invertibles para modelamiento generativo.
- **Aplicar** el teorema de cambio de variable para estimación de verosimilitud exacta.
- **Implementar** flujos normalizantes como NICE y RealNVP.

### Unidad 6: Modelos Basados en Score

**Duración:** 1 semana

#### Contenidos

- Modelos basados en energía (EBMs): función de energía y distribución de Boltzmann, intratabilidad de la constante de normalización, Langevin sampling.
- Score matching: motivación, función de score, divergencia de Fisher, forma tratable.
- Denoising score matching (DSM): motivación, DSM con múltiples niveles de ruido.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Comprender** el modelamiento de distribuciones mediante funciones de energía y score.
- **Explicar** la conexión entre la función de score y la función de energía.
- **Analizar** el rol del ruido en múltiples escalas para la aproximación de la función score.
- **Implementar** modelos generativos basados en score con múltiples niveles de ruido.

### Unidad 7: Modelos de Difusión

**Duración:** 2 semanas

#### Contenidos

- Denoising Diffusion Probabilistic Models (DDPM): proceso forward, proceso reverso, derivación de la ELBO, implementación, reparametrizaciones equivalentes.
- Conexión con modelos de score: equivalencia entre DDPM y DSM con varios niveles de ruido.
- Generación condicional: forma clásica, classifier guidance y classifier-free guidance.
- Arquitecturas neuronales para modelos de difusión: U-Net y Diffusion Transformers (DiT).
- Algunos modelos de difusión: Stable Diffusion, DDIM, GLIDE, DALL-E 2, Imagen, Midjourney.
- Adaptadores: Textual Inversion, DreamBooth, ControlNet, IP-Adapter.
- Propiedades de los modelos de difusión: importancia del nivel de ruido en el proceso forward, relación con transporte óptimo.
- Herramientas: revisión de DMs usando la librería Diffusers de Hugging Face.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Describir** el proceso de entrenamiento y sampling en modelos de difusión.
- **Derivar** la ELBO y comprender las distintas reparametrizaciones equivalentes de los modelos de difusión.
- **Identificar** la relación entre DDPM y modelos basados en score.
- **Implementar** un modelo de difusión desde cero.
- **Aplicar** técnicas de guidance para controlar la generación.
- **Adaptar** modelos preentrenados usando DreamBooth, ControlNet y otros adaptadores.

### Unidad 8: Modelos a Tiempo Continuo

**Duración:** 2 semanas

#### Contenidos

- Repaso de ecuaciones diferenciales ordinarias (EDO): existencia y unicidad de soluciones, métodos numéricos (Euler, Runge-Kutta).
- Ecuación de continuidad: campos de velocidad, transporte de densidades de probabilidad.
- Flow matching: motivación, formulación como regresión de campos de velocidad, entrenamiento sin simulación, relación con rectified flows, relación con transporte óptimo.
- Modelos de flow matching del estado del arte: Stable Diffusion 3, FLUX.1 Kontext.
- Conceptos de cálculo estocástico: movimiento browniano, ecuaciones diferenciales estocásticas (SDE), algoritmo de Euler-Maruyama, ecuación de Fokker-Planck y relación con ecuación de continuidad.
- Teorema de Anderson: reversión temporal de SDEs, score como componente del drift reverso.
- Difusión a tiempo continuo: Teorema de Anderson, extensión de un modelo de difusión a tiempo continuo, probability flow ODE, formulación moderna, relación con flow matching.

#### Resultados de Aprendizaje

Al finalizar la unidad, el estudiante será capaz de:

- **Comprender** la formulación de modelos generativos mediante ecuaciones diferenciales (ODEs y SDEs).
- **Explicar** la relación teórica entre flow matching, modelos de difusión y modelos basados en score.
- **Derivar** resultados como el Teorema de Anderson y la probability flow ODE a partir de la ecuación de Fokker-Planck.
- **Analizar** modelos del estado del arte como Stable-Diffusion 3 y FLUX.1 Kontext.
- **Aplicar** estos conceptos a la generación de contenido multimedia (imágenes, música y videos).
