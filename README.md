# Entropy Ghost
### Privacy Amplification for Location Data

Entropy Ghost is a privacy defense system for mobility data that increases
uncertainty around sensitive locations (such as a user’s home) while preserving
overall data utility.

The system demonstrates how calibrated noise can meaningfully degrade
location inference attacks without destroying usefulness.

---

## 🚀 Live Demo (START HERE)

👉 **Public Demo (Vercel)**  
https://entropy-ghost-demo.vercel.app/

The live demo shows how Entropy Ghost processes location traces and increases
ambiguity around inferred sensitive locations.

> Judges: the demo is fully interactive and requires no setup.

---

## 📊 Experimental Results

In addition to the live demo, we ran batch experiments across **30 users**
to quantify privacy improvements using attacker-centric metrics.

👉 **Results Notebook (metrics + analysis)**  
https://github.com/aashiagarwal2006/Entropy_Ghost_demo/blob/main/batch_kml_30_users_fixed_r90.ipynb

This notebook contains aggregated statistics only (no raw location data).

---

## ❓ Problem

Even coarse-grained location traces can be exploited to infer highly sensitive
information, such as a person’s home location, with high confidence.

Repeated visit patterns and spatial clustering allow attackers to narrow down
a single “most likely” home.

---

## 💡 Approach

Entropy Ghost increases *location entropy* so that attackers must consider
many plausible locations instead of one.

At a high level, the system:
1. Identifies home-like clusters from trajectory data
2. Applies calibrated noise to trajectories
3. Evaluates privacy using:
   - Number of plausible home locations
   - Search area (km²)
   - r90 radius (meters)

---

## 📈 Key Results (30 Users)

| Metric | No Noise | With Noise | Increase |
|------|--------|-----------|----------|
| Avg search area | 0.23 km² | 1.32 km² | **5.8×** |
| Possible home locations | 1.6 | 5.1 | **3.2×** |
| Home r90 radius | 185 m | 292 m | **1.6×** |

These results show a substantial increase in attacker uncertainty.

---

## 📁 Repository Contents

- `batch_kml_30_users_fixed_r90.ipynb`  
  Aggregated experiment results and privacy metrics.

This repository is intentionally limited to **results and documentation only**.

---

## 🧠 Takeaway

Entropy Ghost demonstrates that modest, well-calibrated noise can significantly
reduce the effectiveness of location inference attacks, making it a practical
privacy defense for real-world mobility data.
