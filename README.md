# occ-mtl
KNOWLEDGE-GUIDED MULTI-TASK LEARNING FOR ORAL CANCER CLASSIFICATION


# OCC-MTL: Knowledge-Guided Multi-Task Learning for Oral Cancer Classification

> **ICIP 2026** | Jérôme de Chauveron, Chenyu Zha, Youssef Assis, et al.
> *Sorbonne Université · Université Paris Cité · Dental Monitoring · Hôpital Pitié-Salpêtrière*

---

## TL;DR

Standard black-box models fail at oral cancer diagnosis — data is scarce and predictions are clinically incoherent. **OCC-MTL** fixes this by jointly learning lesion classification and visual concept detection, guided by a novel clinical knowledge loss that penalizes medically implausible predictions.

---

## Key Ideas

- **Multi-task learning** — jointly predicts malignancy *and* clinical visual concepts (e.g., everted edges, induration, blurry borders)
- **Knowledge-guided loss** — an expert consistency matrix encodes which concept–diagnosis combinations are clinically valid, acting as a semantic regularizer
- **Concept curriculum** — the clinical constraint is gradually introduced during training, letting the model learn basic patterns first
- **Interpretable by design** — concept predictions provide built-in explainability without sacrificing performance

---

## Results at a Glance

| Dataset | Model | BACC |
|---------|-------|------|
| OMPAA (oral, proprietary) | OCC-MTL 5-concept | **82.5%** |
| OralCon (oral, public) | OCC-MTL 4-concept | **80.1%** |
| SkinCon (skin, public) | OCC-MTL 5-concept | **78.1%** |

Clinical incoherence dropped from **12.3% → 1.3%** with the knowledge-guided loss.

---

## Datasets

| Dataset | Images | Malignant | Histopath. validation |
|---------|--------|-----------|----------------------|
| OMPAA *(proprietary)* | 2,967 | 10.6% | ✅ |
| OralCon | 2,517 | 3.7% | ✅ |
| SkinCon | 3,886 | 15.9% | — |

---

## Citation

```bibtex
@inproceedings{dechauveron2026occmtl,
  title     = {Knowledge-guided multi-task learning for oral cancer classification},
  author    = {de Chauveron, Jérôme and Zha, Chenyu and Assis, Youssef and others},
  booktitle = {IEEE International Conference on Image Processing (ICIP)},
  year      = {2026}
}
```

---

*Code coming soon on GitHub. Concept annotations for OralCon will be released publicly.*
