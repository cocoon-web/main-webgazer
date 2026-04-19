# Protocolo MAIN + WebGazer v3.1
**Desarrollo:** Constanza Ruiz-Danegger, PhD, Fundación El Pez Volador/ Cerena.
**Propósito:** Evaluación narrativa sincronizada con seguimiento ocular de bajo costo.

## 1. Requisitos de Uso
* **Navegador:** Chrome o Edge (recomendado).
* **Hardware:** Cámara web frontal y micrófono integrados.
* **Entorno:** Iluminación uniforme sobre el rostro del participante; evitar fuentes de luz intensas detrás (ventanas).
* **Archivos Locales:** El sistema funciona **offline** siempre que los archivos `.js` y las imágenes estén en la misma ruta.

## 2. Instrucciones de Operación
1.  **Inicio:** Abrir `index.html`. Ingresar el ID del participante (ej. `SAL_001`).
2.  **Calibración:** El participante debe mirar y hacer clic 5 veces en cada uno de los 9 puntos rojos. Esto entrena el modelo de IA para su fisonomía y posición.
3.  **Narrativa:** Al finalizar la calibración, aparecerán las láminas de MAIN. El participante debe relatar la historia mientras navega con las flechas o el teclado.
4.  **Cierre:** Presionar **"FINALIZAR Y GUARDAR"**. El sistema descargará automáticamente dos archivos.

## 3. Especificaciones Técnicas (Data Output)

### A. Dataset de Eyetracking (`ID_DATOS_COMPLETOS.csv`)
Archivo CSV con frecuencia de muestreo de ~20Hz.
* `tiempo_ms`: Tiempo relativo desde el inicio de WebGazer.
* `x_px` / `y_px`: Coordenadas de mirada en la pantalla.
* `lamina_id`: Identificador de la imagen de MAIN que se estaba visualizando (1 al 6). *Crucial para análisis de AOIs.*

### B. Registro de Audio (`ID_NARRATIVA.webm`)
* **Formato:** WebM (Codec Opus).
* **Sincronía:** El inicio del audio coincide con el inicio de la visualización de la primera lámina.

### C. Herramienta de Revisión (Heatmap)
El botón "REVISAR HEATMAP" permite visualizar sobre el DOM actual la densidad de fijaciones por lámina. Esto es para control de calidad inmediato en territorio; no reemplaza el análisis estadístico posterior de los datos crudos.

---

## 4. Nota de Contexto
Este desarrollo busca democratizar el acceso a herramientas de eyetracking en territorios de difícil acceso, integrando rigor científico con dispositivos de uso cotidiano. 
