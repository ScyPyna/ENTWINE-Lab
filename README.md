# 🔬 ENTWINE Lab Repository

This repository serves as the main workspace for the **ENTWINE project**.
It contains both project documentation and the software/hardware sub-projects
developed within the lab.

The repository is structured to keep documentation, workflows, and code
organized and version-controlled in a single place.

---

## 📚 Documentation

All general documentation is collected in the project Wiki:

👉 **[ENTWINE Project Wiki](Wiki/README.md)**

The Wiki provides an overview of laboratory practices, technical guidelines,
and organizational information relevant to the project.

---

## 💻 Sub-projects

This repository hosts multiple sub-projects related to the ENTWINE initiative.
Each sub-project is contained in its own directory and includes a dedicated
`README.md` describing its scope, structure, and usage.

### 🦠 moving-chlamydomonas

**[moving-chlamydomonas](https://github.com/ScyPyna/moving-chlamydomonas_pub)** — trajectory tracking and analysis pipeline for *Chlamydomonas* microalgae recorded on microscopy videos.

Provides two Streamlit web interfaces:
- **`tracking_app`** — interactive parameter tuning and batch tracking from `.avi` videos
- **`clam-app`** — statistical analysis and plotting of the resulting trajectories

```bash
git clone https://github.com/ScyPyna/moving-chlamydomonas_pub.git
cd moving-chlamydomonas_pub
pip install -e .
```

---

## 📌 Getting Started

- If you are new to the project, start by reading the **Wiki**.
- For project-specific work, navigate to the relevant sub-project directory.
- Refer to the documentation whenever procedures or workflows are updated.

---

📎 **Note**:  
This repository is actively maintained. Please ensure that both code and
documentation remain consistent when introducing changes.