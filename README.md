# 🔬 Biolight Lab Repository

This repository serves as the main workspace for the **ENTWINE project**.
It contains both project documentation and the software/hardware sub-projects
developed within the lab.

The repository is structured to keep documentation, workflows, and code
organized and version-controlled in a single place.

---

## 📚 Documentation

All general documentation is collected in the project Wiki:

👉 **[Biolight Wiki](Wiki/README.md)**

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

- ask for your SOLDI credentials, needed for the canteen and for accessing all the IT services: Gianni takes care of this (email Loretta Servidio)
- go to the administration office to create and activate your badge to access the lab and offices
- create your unical email following these [instructions](https://github.com/ScyPyna/ENTWINE-Lab/blob/main/Wiki/02_IT/Email_Request/README.md)
- create your [tailscale](https://github.com/ScyPyna/ENTWINE-Lab/blob/main/Wiki/02_IT/OpenVPN/README.md) account—needed for the next steps
- join Mattermost to communicate with the rest of the team
- request your Microsoft Office licence on [uniticket](https://ticket.unical.it/dashboard/) (request code L1)
- ask Gianni for access to our Claude team licence (you need a @unical email)
- set up your [SSH](https://github.com/ScyPyna/ENTWINE-Lab/blob/main/Wiki/02_IT/SSH_Keys/README.md) keys to access the Workstation, where you can analyse the data
- ask Giusy for your NAS account, where your data are stored
- request [OpenVPN](https://github.com/ScyPyna/ENTWINE-Lab/blob/main/Wiki/02_IT/OpenVPN/README.md) access to reach the IT services from away
- now you can read [here](https://github.com/ScyPyna/moving-chlamydomonas_pub) how to use the app to analyse the data
- if you are coming from abroad, check also the [administrative process](https://github.com/ScyPyna/ENTWINE-Lab/blob/main/Wiki/03_Administrative/README.md) section
- have fun exploring the other pages, and help us keep the wiki updated!


---

📎 **Note**:  
This repository is actively maintained. Please ensure that both code and
documentation remain consistent when introducing changes.
