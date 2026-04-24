# 🧬 ImageJ Analysis Protocol – ER.ALT2 (OpenCell Dataset)

---

## 🎯 Objective
To perform quantitative analysis of a fluorescence microscopy image (ER.ALT2) using ImageJ, including preprocessing, segmentation, and automated particle counting to estimate cellular structures.

---

## 🖥️ Image Information
- Dataset: **OpenCell (ER.ALT2)**
- Image type: Grayscale fluorescence microscopy image  
- Analysis software: ImageJ  

---

## 🔬 Methodology

### 🔹 1. Image Import and Preparation
- Opened image using:
  - `File → Open.`
- Confirmed grayscale format:
  - `Image → Type → 8-bit`

Purpose:
- Ensure compatibility with thresholding and binary operations  

---

### 🔹 2. Intensity Adjustment (Brightness & Contrast)

- Adjusted using:
  - `Image → Adjust → Brightness/Contrast`

Parameters:
- Minimum intensity: **71**
- Maximum intensity: **324**

Purpose:
- Improve contrast between foreground (cells) and background  
- Enhance segmentation accuracy  

---

### 🔹 3. Scale Consideration

- Scale calibration was **not applied**  
- All measurements retained in **pixel units**

Implication:
- Results represent relative size/count rather than absolute physical dimensions  

---

### 🔹 4. Thresholding (Segmentation Preparation)

- Applied threshold using:
  - `Image → Adjust → Threshold`

Parameters:
- Lower threshold: **50**
- Upper threshold: **255**

Outcome:
- Foreground structures highlighted  
- Background effectively suppressed  

---

### 🔹 5. Binary Conversion and Segmentation

- Converted to binary mask:
  - `Process → Binary → Convert to Mask`

- Applied segmentation:
  - `Process → Binary → Watershed`

Purpose:
- Separate touching or overlapping particles  
- Improve counting precision  

---

### 🔹 6. Automated Particle Analysis

- Performed using:
  - `Analyze → Analyze Particles`

Parameters:
- Size: **0 – Infinity pixels**
- Circularity: **0.00 – 1.00**

Options enabled:
- Display Results  
- Summarize  
- Exclude on edges (if applied)

---

## 📊 Results

- **Total particle count:** **2098**

Output includes:
- Particle count  
- Area measurements  
- Shape descriptors (if enabled)  

---

## 📁 Data Export

- Results exported as:
  - `.csv` file for further statistical analysis  

- Processed image saved for documentation  

---

## ⚠️ Limitations and Considerations

- No size filtering → includes noise and small artifacts  
- Pixel-based measurement → no real-world scaling  
- Threshold selection influences segmentation accuracy  
- Watershed may over-segment in dense regions  

---

## 💡 Conclusion

The ImageJ-based workflow successfully enabled automated segmentation and quantification of structures in the ER.ALT2 dataset. A total of **2098 particles** were detected, demonstrating effective preprocessing and segmentation.

---

## Prepared by
Vedanti Raut  
Institute of Bioinformatics and Biotechnology (IBB),
Savitribai Phule Pune University (SPPU)

---
