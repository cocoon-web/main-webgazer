# MAIN Protocol + WebGazer v3.1
**Development:** Constanza Ruiz-Danegger, PhD (Fundación El Pez Volador / Cerena)
**Purpose:** Low-cost eye-tracking and synchronized narrative recording.

---

## 📂 Directory Structure `MAIN_v3.1/`

To ensure **offline** functionality and protocol integrity, the folder must contain:

* **`index.html`**: Main application file (Interface & Synchronization logic).
* **`webgazer.js`**: Machine learning engine for eye-tracking (must be in the root).
* **`README.md`**: This technical manual.
* **`main_img/`**: Folder containing visual stimuli (MAIN pictures).
* **`libs/`**: *(Optional)* Local Swiper.js assets for 100% offline use.

---

## 1. Requirements for Use
* **Browser:** Chrome or Edge (highly recommended).
* **Hardware:** Front-facing webcam and integrated microphone.
* **Environment:** Even lighting on the participant's face. Avoid strong light sources behind the subject (e.g., windows).
* **Connectivity:** Works **offline** once the folder is downloaded.

---

## 2. Operating Instructions
1. **Setup:** Open `index.html`. Enter Participant ID (e.g., `SUBJ_001`).
2. **Calibration:** The participant must look at and click each of the 9 red dots 5 times. This trains the AI model for their specific position.
3. **Narrative Task:** Once calibrated, the MAIN pictures will appear. The participant narrates the story while navigating using arrows or the on-screen buttons.
4. **Completion:** Click **"FINISH & SAVE DATA"**. The browser will trigger the download of two files.

---

## 3. Technical Specifications (Data Output)

### A. Eye-tracking Dataset (`ID_EYE_TRACKING_DATA.csv`)
CSV file with a sampling frequency of approximately ~20Hz.
* `timestamp_ms`: Relative time since WebGazer started.
* `x_px` / `y_px`: Gaze coordinates on the screen.
* `picture_id`: Identifier of the MAIN picture being viewed (1 to 6). *Crucial for automated Area of Interest (AOI) analysis.*

### B. Audio Recording (`ID_NARRATIVE_AUDIO.webm`)
* **Format:** WebM (Opus Codec).
* **Synchronization:** Audio onset is perfectly aligned with the display of the first picture.

### C. Review Tool (Heatmap)
The **"REVIEW HEATMAP"** button allows researchers to overlay fixation density per slide on the current interface. This is designed for **immediate on-site quality control**.

---

## 4. Contextual Note
This development aims to democratize access to high-end research tools in remote territories, merging scientific rigor with everyday consumer hardware.
