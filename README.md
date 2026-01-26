<div align="center">

# MDS7203 — Modelos Generativos Profundos

[![U-Cursos](https://img.shields.io/badge/U--Cursos-Otoño%202026-blue?style=for-the-badge)](https://www.u-cursos.cl/ingenieria/2026/1/MDS7203/1/)
[![MDS](https://img.shields.io/badge/MDS-UChile-red?style=for-the-badge)](https://mds.uchile.cl/)

</div>

Este repositorio contiene todo el material del curso **MDS7203 Modelos Generativos Profundos**, parte del [Magíster en Ciencia de Datos](https://mds.uchile.cl/) de la Facultad de Ciencias Físicas y Matemáticas de la Universidad de Chile.

El curso cubre los fundamentos teóricos y prácticos de los modelos generativos modernos, comenzando con el estudio de los LLMs y sus usos agénticos, y concluyendo con el estudio de los modelos de difusión y flow matching. Los detalles de los contenidos se pueden revisar en el [programa del curso](Docs/Programa%20del%20curso.md) o en el [calendario de clases](Docs/Calendario%20de%20clases.md) del semestre actual (otoño, 2026).

### Requisitos Previos

Se espera que los estudiantes tengan conocimientos básicos en:

- **Probabilidades y estadística** (distribuciones, probabilidad condicional, esperanza).
- **Redes neuronales** (entrenamiento, arquitecturas fully connected y convolucional).
- **Programación en Python** (principalmente PyTorch).

La segunda clase del curso estará dedicada a repasar los conceptos necesarios para el desarrollo del curso.

## Evaluación

El curso tiene dos métodos de evaluación, los cuales deben ser aprobados por separado:

| Componente               | Ponderación | Descripción                                                 |
| ------------------------ | ----------- | ----------------------------------------------------------- |
| **Tareas**               | 50%         | 3 tareas (semanas 5, 10 y 15)                               |
| **Controles de Lectura** | 50%         | 7 controles de lectura (semanas impares, desde la semana 3) |

Los controles de lectura son realizados en clases, y solo se consideran los mejores 6 controles de lectura para el cálculo de la nota final. Las tareas se realizan de forma asíncrona en un plazo máximo de 2 semanas.

**Nota:** algunas tareas requieren acceso a GPU. En estos casos, es suficiente Google Colab (T4).

### Semestres Anteriores

<details>
<summary>Otoño 2025 (6 tareas).</summary>

| Tarea   | Enunciado                                                                  | Solución                                                                                   |
| ------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Tarea 1 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%201.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%201%20%28solución%29.ipynb) |
| Tarea 2 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%202.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%202%20%28solución%29.ipynb) |
| Tarea 3 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%203.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%203%20%28solución%29.ipynb) |
| Tarea 4 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%204.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%204%20%28solución%29.ipynb) |
| Tarea 5 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%205.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%205%20%28solución%29.ipynb) |
| Tarea 6 | [Enunciado](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%206.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20otoño/Tareas/Tarea%206%20%28solución%29.ipynb) |

</details>

<details>
<summary>Primavera 2025 (3 tareas).</summary>

| Tarea   | Enunciado                                                                         | Solución                                                                                          |
| ------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Tarea 1 | [Enunciado](Semestres%20anteriores/2025%2C%20primavera/Tareas/T1/Tarea%201.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20primavera/Tareas/T1/Tarea%201%20%28solución%29.ipynb) |
| Tarea 2 | [Enunciado](Semestres%20anteriores/2025%2C%20primavera/Tareas/T2/Tarea%202.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20primavera/Tareas/T2/Tarea%202%20%28solución%29.ipynb) |
| Tarea 3 | [Enunciado](Semestres%20anteriores/2025%2C%20primavera/Tareas/T3/Tarea%203.ipynb) | [Solución](Semestres%20anteriores/2025%2C%20primavera/Tareas/T3/Tarea%203%20%28solución%29.ipynb) |

</details>

## Bibliografía

### Notas del Curso

En Notion se encuentran disponibles las [notas complementarias](https://fernandofetis.notion.site/genai) de las clases.

### Bibliografía General

Los siguientes libros cubren los fundamentos teóricos y prácticos de los modelos generativos estudiados durante el curso:

| Libro                                                                                                                 | Autor         | Descripción                                                     |
| --------------------------------------------------------------------------------------------------------------------- | ------------- | --------------------------------------------------------------- |
| [Probabilistic Machine Learning: Advanced Topics](https://probml.github.io/pml-book/book2.html)                       | Kevin Murphy  | Parte IV. Fundamentos teóricos de los paradigmas generativos.   |
| [Generative Deep Learning, 2nd Edition](https://www.oreilly.com/library/view/generative-deep-learning/9781098134174/) | David Foster  | Enfoque práctico con implementaciones en PyTorch.               |
| [Deep Generative Modeling, 2nd Edition](https://link.springer.com/book/10.1007/978-3-031-64087-2)                     | Jakub Tomczak | Complemento al libro de Murphy con implementaciones en PyTorch. |

### Bibliografía por Unidad

Los siguientes libros sirven como complemento a los contenidos estudiados en clase:

| Libro                                                                                                                                       | Autor                        | Unidad / Tema                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- | ----------------------------------------------------------- |
| [Probabilistic Graphical Models: Principles and Techniques](https://mitpress.mit.edu/9780262013192/probabilistic-graphical-models/)         | Daphne Koller & Nir Friedman | Redes bayesianas (Unidad 1)                                 |
| [AI Agents in Action](https://www.manning.com/books/ai-agents-in-action)                                                                    | Valentino Gagliardi          | Agentes basados en LLMs (Unidad 2)                          |
| [Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch)                      | Sebastian Raschka            | Repaso de GPT implementado en clases (Unidad 2)             |
| [GANs in Action](https://www.manning.com/books/gans-in-action)                                                                              | Jakub Langr                  | GANs con implementaciones en Keras (Unidad 3)               |
| [Hands-On Generative AI with Transformers and Diffusion Models](https://www.oreilly.com/library/view/hands-on-generative-ai/9781098149239/) | Omar Sanseviero et al.       | LLMs y modelos de difusión con HuggingFace (Unidades 2 y 7) |
| [AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/)                                                        | Chip Huyen                   | Buenas prácticas y desarrollo de proyectos de IA (General)  |

### Papers del Curso

Los libros suelen ir un poco más atrasados respecto al estado del arte actual. Aquí se incluyen las referencias a los trabajos que se revisarán a lo largo del curso:

<details>
<summary>Lista de papers revisados</summary>

*Esta sección se irá actualizando con los papers revisados durante el semestre.*

</details>

---

<div align="center">

**Magíster en Ciencia de Datos · Facultad de Ciencias Físicas y Matemáticas
<br>
Universidad de Chile**

</div>
