# MDS7203 — Calendario de clases

Este calendario es válido para el semestre de otoño, 2026.

## Unidad 1: Introducción (2 semanas)

|  Sem  |   #   | Contenidos                                                                                        | Eval  |
| :---: | :---: | ------------------------------------------------------------------------------------------------- | :---: |
|   1   |  C1   | Introducción al curso: motivación, objetivos, estructura. Paradigmas generativos modernos.        |       |
|   1   |  C2   | Repaso: probabilidades, redes neuronales, optimización.                                           |       |
|   2   |  C3   | Redes bayesianas I: motivación, formulación, ejemplos, conexión con modelos generativos modernos. |       |
|   2   |  C4   | Redes bayesianas II: modelos condicionales, variable latente, estimación de parámetros.           |       |
|   2   |  A1   | Repaso de PyTorch.                                                                                |       |

## Unidad 2: Modelos Autorregresivos y LLMs (3 semanas)

|  Sem  |   #   | Contenidos                                                                                                                  |      Eval      |
| :---: | :---: | --------------------------------------------------------------------------------------------------------------------------- | :------------: |
|   3   |  C5   | Formulación ARM, arquitecturas recurrentes, teacher forcing, estrategias de generación.                                     |                |
|   3   |  C6   | Arquitectura GPT.                                                                                                           |      CL1       |
|   3   |  A2   | Introducción a librería Transformers.                                                                                       |                |
|   4   |  C7   | Variantes Transformer: tokenizadores, positional encoders, normalizaciones, mecanismos de atención, MoE.                    |                |
|   4   |  C8   | Otros Transformers (BERT, CLIP, ViT, Chameleon, AlphaFold), LLMs (chat templates, entrenamiento conversacional, LM Studio). |                |
|   4   |  A3   | Revisión detallada de BERT, ViT y CLIP usando Transformers.                                                                 |                |
|   5   |  C9   | Propiedades empíricas (leyes de escala, habilidades emergentes, prompting), agentes (RAG, function calling).                |                |
|   5   |  C10  | Inferencia eficiente (KV-caching, cuantización), fine-tuning (SFT, heurísticas, LoRA, RLHF/DPO).                            | CL2<br>Pub. T1 |
|   5   |  A4   | Nociones de GPU y redes (SSH), uso de GPU en la nube y fine-tuning eficiente de un LLM.                                     |                |

## Unidad 3: Redes Generativas Adversarias (2 semanas)

|  Sem  |   #   | Contenidos                                                                                           | Eval  |
| :---: | :---: | ---------------------------------------------------------------------------------------------------- | :---: |
|   6   |  C11  | Formulación, generación condicional, implementación.                                                 |       |
|   6   |  C12  | Arquitecturas (conv. transpuestas, DCGAN, SAGAN, U-Net, ProGAN, StyleGAN, BigGAN, MuseGAN).          |       |
|   6   |  A5   | Implementación y entrenamiento U-Net.                                                                |       |
|   7   |  C13  | Transferencia de estilo (pix2pix, CycleGAN), OT (problema de Kantorovich, distancia de Wasserstein). |       |
|   7   |  C14  | Métricas (FID e IS), WGAN, limitaciones de GANs, contexto histórico.                                 |  CL3  |
|   7   |  A6   | Implementación SAGAN, cálculo FID/IS.                                                                |       |

## Unidad 4: Autoencoders Variacionales (2 semanas)

|  Sem  |   #   | Contenidos                                                                                                                                  | Eval  |
| :---: | :---: | ------------------------------------------------------------------------------------------------------------------------------------------- | :---: |
|   8   |  C15  | Autoencoders clásicos, introducción a los VAEs.                                                                                             |       |
|   8   |  C16  | Formulación VAE (inferencia variacional, derivación ELBO, reconstrucción y regularización KL), implementación (caso gaussiano y bernoulli). |       |
|   8   |  A7   | Comparación GAN vs VAE usando FIS/IS.                                                                                                       |       |
|   9   |  C17  | Interpolación en espacio latente, modificación de atributos, disentanglement.                                                               |       |
|   9   |  C18  | Truco de la reparametrización, variantes VAE (VRAE, continuous Bernoulli, beta-VAE, covarianza no diagonal, VQ-VAE).                        |  CL4  |
|   9   |  A8   | Revisión de un VAE con Diffusers.                                                                                                           |       |

## Unidad 5: Flujos Normalizantes (1 semana)

|  Sem  |   #   | Contenidos                                                       |  Eval   |
| :---: | :---: | ---------------------------------------------------------------- | :-----: |
|  10   |  C19  | Teorema de cambio de variable, formulación flujos normalizantes. |         |
|  10   |  C20  | Ejemplos (NICE, RealNVP), sampling y estimación de densidad.     | Pub. T2 |
|  10   |  A9   | NODE.                                                            |         |

## Unidad 6: Modelos Basados en Score (1 semana)

|  Sem  |   #   | Contenidos                                                   | Eval  |
| :---: | :---: | ------------------------------------------------------------ | :---: |
|  11   |  C21  | EBMs: función de energía, langevin sampling, score matching. |       |
|  11   |  C22  | DSM y DSM con múltiples niveles de ruido.                    |  CL5  |
|  11   |  A10  | Implementación DSM multinivel.                               |       |

## Unidad 7: Modelos de Difusión (2 semanas)

|  Sem  |   #   | Contenidos                                                                  | Eval  |
| :---: | :---: | --------------------------------------------------------------------------- | :---: |
|  12   |  C23  | Formulación DDPM, propiedades, ELBO.                                        |       |
|  12   |  C24  | Implementación, reparametrizaciones equivalentes.                           |       |
|  12   |  A11  | Revisión DDPM con Diffusers.                                                |       |
|  13   |  C25  | Generación condicional, guidance, arquitecturas (U-Net para difusión, DiT). |       |
|  13   |  C26  | DMs famosos, adaptadores, propiedades DMs y relación con OT.                |  CL6  |
|  13   |  A12  | Fine-tuning con DreamBooth + LoRA.                                          |       |

## Unidad 8: Modelos a Tiempo Continuo (2 semanas)

|  Sem  |   #   | Contenidos                                                                                                             |      Eval      |
| :---: | :---: | ---------------------------------------------------------------------------------------------------------------------- | :------------: |
|  14   |  C27  | Repaso EDOs, ecuación de continuidad, intro. flow matching (formulación, entrenamiento, rectified flows, relación OT). |                |
|  14   |  C28  | FM, relación con OT y rectified flows, modelos SOTA (SD3, FLUX.1 Kontext).                                             |                |
|  14   |  A13  | Generación de videos.                                                                                                  |                |
|  15   |  C29  | Cálculo estocástico (movimiento browniano, SDEs, Euler-Maruyama, Fokker-Planck), teorema de Anderson.                  |                |
|  15   |  C30  | Difusión a tiempo continuo: formulación, probability flow ODE, formulación moderna, relación FM-DM.                    | CL7<br>Pub. T3 |
|  15   |  A14  | Modelo SOTA.                                                                                                           |                |
