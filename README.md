<div align="center">
  <h1>MAIN-WebGazer v3.2</h1>
  <h3><b>Constanza Ruiz-Danegger, PhD</b></h3>
  <p>Executive Director, <b>Fundación El Pez Volador</b></p>
  <p>Centro de Referencia <b>Cerena</b> | Autism and Neurodiversity Centre</p>
  <a href="https://elpezvolador.org">🌐 elpezvolador.org</a>
</div>

---

## Overview
**MAIN-WebGazer** es un toolkit híbrido de código abierto que integra el **Multilingual Assessment Instrument for Narratives (MAIN)** con seguimiento ocular (eye-tracking) basado en webcams mediante `WebGazer.js`. 

Este proyecto, lanzado como contribución por el 20.º aniversario del **Proyecto El Pez Volador (2006-2026)**, operacionaliza la recursión implícito-explícita de la cognición social desde una lente neuro-afirmativa e intercultural.

## Características Principales
* **Biometría Accesible:** Eye-tracking de alta fidelidad utilizando webcams estándar, eliminando la necesidad de hardware costoso.
* **Disyunción Gaze-IST:** Un nuevo marcador biométrico que cuantifica la brecha entre los Términos de Estado Interno (IST) verbales y la atención visual a Áreas de Interés (AOI) sociales.
* **Visualización en Tiempo Real:** Generador de **Heatmaps** integrado para revisión inmediata post-sesión.
* **Captura Multimodal:** Grabación de audio sincronizada para el análisis de la narrativa y el cálculo del costo cognitivo del camuflaje lingüístico.
* **Diseño Neuro-afirmativo:** Protocolo de calibración de 9 puntos optimizado para perfiles sensoriales y tiempos de procesamiento neurodivergentes.
* **Adaptación Argentina:** Implementación completa de la versión de MAIN para Argentina, incluyendo el uso de *voseo* y léxico situado.

## Guía de Inicio Rápido
1.  **Clonar** el repositorio.
2.  **Descargar** `webgazer.js` y colocarlo en la raíz del proyecto.
3.  **Ejecutar un servidor local**: `python -m http.server 8000`.
4.  **Abrir** `index.html` en un navegador con cámara habilitada.
5.  **Seguir** el protocolo de calibración (5 clics por cada uno de los 9 puntos).

## Estructura de Datos
Al finalizar cada sesión, el toolkit exporta automáticamente:
* `SUBJ_ID_gaze.csv`: Datos de timestamp, coordenadas (x, y) y slide activo.
* `SUBJ_ID_audio.webm`: Registro de audio de la narración para análisis lingüístico.

## Citación
---

*Este proyecto cuenta con la autorización y registro en MAIN Worldwide Network (ZAS, Berlín).*

---
<p align="center">🌿 <i>Por favor, considera el medio ambiente antes de imprimir.</i></p>
