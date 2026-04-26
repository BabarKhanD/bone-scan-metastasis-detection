# 🦴 Bone Scan Metastasis Detection

> AI pipeline for bone metastasis detection from nuclear medicine bone scans. Uses dual-view CNN with Focal Loss achieving 100% recall, Grad-CAM explainability, automatic hotspot detection, and Vision Transformer comparison.

**Authors:** Babar Khan Durrani · Haleema Rehman  
**Institution:** Bahria University, BSEAS

---

## 📊 Results

| Model | Recall | Caught | mAP |
|---|---|---|---|
| Baseline CNN | 53% | 8/15 | 0.149 |
| Augmented CNN | 73% | 11/15 | 0.221 |
| **Focal Loss CNN** ⭐ | **100%** | **15/15** | **0.279** |
| Vision Transformer | 27% | 4/15 | 0.184 |

> 🏆 Focal Loss CNN at threshold 0.25 catches every cancer case — zero missed.

## 🚀 How to Run

```bash
# 1. Upload these files to Colab:
#    - kneeLANT.zip, kneeLPOST.zip
#    - kneeLANT.txt, kneeLPOST.txt (labels)
#    - best_cnn_baseline.keras
#    - best_cnn_aug.keras
#    - best_cnn_focal.keras
#    - best_vit.keras


### Interactive Image Checker
```
Enter image number (e.g. 1234) | type 'quit' to exit: 1234
Choose view: 1 = ANT | 2 = POST | 3 = BOTH: 1
```

---

## 📂 Structure

```
bone-scan-metastasis-detection/
├── bone_scan_no_training.py    ← Main code (load models + full analysis)
├── requirements.txt
├── results/                    ← All output images
└── report/
    └── bone_scan_report.tex    ← LaTeX report
```

---

## 📦 Requirements

```
tensorflow>=2.19.0
opencv-python
numpy pandas matplotlib seaborn scikit-learn Pillow
```

```bash
pip install -r requirements.txt
```

---

## ⚖️ Responsible AI

- Threshold 0.25 → zero missed cancer cases
- Grad-CAM heatmap on every prediction
- Decision support tool — not a replacement for radiologists

---

*Not intended for clinical use without regulatory approval.*
