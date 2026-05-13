# Protocolo MAIN + WebGazer v3.1
**Desarrollo:** Dra. Constanza Ruiz-Danegger (Fundación El Pez Volador / Cerena)
**Propósito:** Seguimiento ocular (eye-tracking) de bajo costo y registro de narrativa sincronizada.

---

## 📂 Estructura de la Carpeta `MAIN_v3.1/`

Para garantizar el funcionamiento **offline** y la integridad del protocolo, la carpeta debe contener:

* **`index.html`**: Archivo principal de la aplicación (Lógica de interfaz y sincronización).
* **`webgazer.js`**: Motor de machine learning para el seguimiento ocular (debe estar en la raíz).
* **`README.md`**: Este manual técnico.
* **`main_img/`**: Carpeta con los estímulos visuales (láminas de la historia MAIN).
* **`libs/`**: *(Opcional)* Archivos locales de Swiper.js para uso 100% sin internet.

---

## 1. Requisitos de Uso
* **Navegador:** Chrome o Edge (altamente recomendado).
* **Hardware:** Cámara web frontal y micrófono integrado.
* **Entorno:** Iluminación uniforme sobre el rostro del participante. Evitar fuentes de luz intensas detrás del sujeto (ej. ventanas).
* **Conectividad:** Funciona **offline** una vez descargada la carpeta.

---

## 2. Instrucciones de Operación
1. **Configuración:** Abrir `index.html`. Ingresar el ID del participante (ej. `SAL_001`).
2. **Calibración:** El participante debe mirar y hacer clic en cada uno de los 9 puntos rojos (5 clics por punto). Esto entrena el modelo de IA para su posición específica.
3. **Tarea Narrativa:** Una vez calibrado, aparecerán las láminas de MAIN. El participante narra la historia mientras navega usando las flechas o los botones en pantalla.
4. **Finalización:** Hacer clic en **"FINALIZAR Y GUARDAR"**. El navegador descargará automáticamente dos archivos.

---

## 3. Especificaciones Técnicas (Salida de Datos)

### A. Dataset de Eyetracking (`ID_DATOS_COMPLETOS.csv`)
Archivo CSV con una frecuencia de muestreo de aproximadamente ~20Hz.
* `tiempo_ms`: Tiempo relativo desde el inicio de WebGazer.
* `x_px` / `y_px`: Coordenadas de la mirada en la pantalla.
* `lamina_id`: Identificador de la lámina de MAIN que se estaba viendo (1 a 6). *Crucial para el análisis automatizado de Áreas de Interés (AOI).*

### B. Registro de Audio (`ID_NARRATIVA.webm`)
* **Formato:** WebM (Codec Opus).
* **Sincronización:** El inicio del audio está perfectamente alineado con la visualización de la primera lámina.

### C. Herramienta de Revisión (Heatmap)
El botón **"REVISAR HEATMAP"** permite a los investigadores superponer la densidad de fijaciones por lámina sobre la interfaz. Diseñado para un **control de calidad inmediato en territorio**.

---

## 4. Nota de Contexto
Este desarrollo busca democratizar el acceso a herramientas de investigación de alta gama en territorios remotos, fusionando el rigor científico con hardware de uso cotidiano.
