# MAIN + WebGazer v3.1
**Development:** Constanza Ruiz-Danegger, PhD, Fundación El Pez Volador / Cerena.  
**Purpose:** Synchronized narrative assessment with low-cost eye-tracking integration.

---

## 1. Requirements for Use
* **Browser:** Chrome or Edge (recommended).
* **Hardware:** Integrated front-facing webcam and microphone.
* **Environment:** Even lighting on the participant's face; avoid intense backlighting (e.g., windows behind the subject).
* **Local Files:** The system operates **offline**, provided that the `.js` files and images are located within the same directory.

---

## 2. Operating Instructions
1.  **Setup:** Open `index.html`. Enter the Participant ID (e.g., `SUBJ_001`).
2.  **Calibration:** The participant must look at and click each of the 9 red dots 5 times. This trains the AI model for their specific physiognomy and screen position.
3.  **Narrative Task:** Once calibration is complete, the MAIN story pictures will appear. The participant narrates the story while navigating through the slides using arrows or the keyboard.
4.  **Completion:** Click **"FINISH & SAVE DATA"**. The system will automatically trigger the download of two files.

---

## 3. Technical Specifications (Data Output)

### A. Eye-tracking Dataset (`ID_EYE_TRACKING_DATA.csv`)
CSV file with a sampling frequency of approximately ~20Hz.
* `timestamp_ms`: Relative time since the start of WebGazer.
* `x_px` / `y_px`: Gaze coordinates on the screen.
* `picture_id`: Identifier of the MAIN picture being viewed (1 to 6). *Crucial for Area of Interest (AOI) analysis.*

### B. Audio Recording (`ID_NARRATIVE_AUDIO.webm`)
* **Format:** WebM (Opus Codec).
* **Synchronization:** Audio onset is synchronized with the initial display of the first picture.

### C. Review Tool (Heatmap)
The "REVIEW HEATMAP" button allows for an immediate overlay of fixation density per slide on the current DOM. This is intended for **on-site quality control** and does not replace subsequent statistical analysis of the raw data.

---

## 4. Contextual Note
This development aims to democratize access to eye-tracking tools in remote or underserved territories, integrating scientific rigor with everyday consumer devices.
