<!--
  Profile README for Gokulnaath-N. Banner source: assets/profile-banner.svg
  LeetCode figures (Achievements) were read from the live profile in Nov 2026; refresh them occasionally.
-->

<div align="center">


<img width="947" height="298" alt="image" src="https://github.com/user-attachments/assets/7558f0b7-d7de-432b-8666-4fe8182350de" />


**AI/ML Developer | Data Science | Deep Learning | Applied Artificial Intelligence**

*Turning Data into Intelligence. Building AI Systems with Purpose.*

[![GitHub](https://img.shields.io/badge/GitHub-161B22?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Gokulnaath-N) [![LinkedIn](https://img.shields.io/badge/LinkedIn-161B22?style=for-the-badge)](https://linkedin.com/in/gokulnaath-n) [![Email](https://img.shields.io/badge/Email-161B22?style=for-the-badge)](mailto:gokulnaath.n2024cce@sece.ac.in)

[About](#about) &nbsp;|&nbsp; [Projects](#featured-projects) &nbsp;|&nbsp; [Experience](#professional-experience) &nbsp;|&nbsp; [Skills](#technical-arsenal) &nbsp;|&nbsp; [Achievements](#achievements-and-leadership) &nbsp;|&nbsp; [Contact](#lets-connect)

</div>

---

## About

I am a Computer and Communication Engineering undergraduate at Sri Eshwar College of Engineering, Coimbatore (class of 2028), focused on Data Science, Machine Learning, and Applied AI. I enjoy building end-to-end intelligent systems, from data preprocessing, exploratory analysis and feature engineering to model training, evaluation, API development and cloud deployment.

My work spans computer vision, NLP, deep learning, EEG signal processing, predictive analytics and multi-agent AI systems. I am interested in turning complex data into practical, intelligent solutions.

**Current focus**

- Machine Learning and Statistical Learning
- Deep Learning and Neural Networks
- Computer Vision and NLP
- Data Analytics and Feature Engineering
- LLMs and Agentic AI
- ML Deployment and Cloud Infrastructure

---

## Featured Projects

Four systems that take raw signals or data all the way to a trained model and a working interface. Each is a working prototype with public code.

### 1. NeuroBright

**A neuroadaptive learning platform that reads EEG to adapt how a learner studies.**

```mermaid
flowchart LR
    A["EEG sensor"] --> B["Time-frequency features"] --> C["EEGNet classifier"] --> D["Adaptive content"]
    classDef n fill:#161B22,stroke:#22D3EE,color:#F0F6FC
    class A,B,C,D n
```

**Problem.** Digital learning content is static. It cannot tell when a learner is focused, overloaded or drifting off, and that gap is widest for neurodivergent learners, who need pacing and format to change with their state.

**Approach.** A single-channel EEG sensor feeds a pipeline that digitizes and filters the signal and converts it to the time-frequency domain. An EEGNet CNN classifies three cognitive states: focus, overload and drowsiness. A GenAI content engine then switches the lesson between text, video, audio and an AI tutor.

**Highlights**

- Complete brain-computer interface pipeline: acquisition, signal processing, model training, live inference and a React front end.
- Sliding-window inference with 2-second windows advancing every 500 ms, streamed to the interface over WebSocket.
- Demonstrated live to the Mayor of Coimbatore, who directed a 6-channel wearable build-out and a school pilot. The wearable version is in development.

![Python](https://img.shields.io/badge/Python-161B22?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-161B22?style=flat-square&logo=pytorch&logoColor=white) ![EEGNet](https://img.shields.io/badge/EEGNet-161B22?style=flat-square) ![MNE-Python](https://img.shields.io/badge/MNE--Python-161B22?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-161B22?style=flat-square&logo=fastapi&logoColor=white) ![React](https://img.shields.io/badge/React-161B22?style=flat-square&logo=react&logoColor=white)

[Repository](https://github.com/Gokulnaath-N/NeuroBright-Neuroadpative_Learning_Plarform)

---

### 2. WildGuard AI

**Real-time behavior monitoring for zoo and wildlife animals.**

```mermaid
flowchart LR
    A["Video stream"] --> B["YOLOv8 detection"] --> C["ByteTrack tracking"] --> D["VideoMAE actions"] --> E["Behavior flag"]
    classDef n fill:#161B22,stroke:#22D3EE,color:#F0F6FC
    class A,B,C,D,E n
```

**Problem.** Animal welfare monitoring depends on manual observation and delayed CCTV review. With caretaker shortages, abnormal or aggressive behavior can go unnoticed.

**Approach.** Three stages run in sequence on live video. YOLOv8 detects each animal, ByteTrack keeps a persistent identity for it across frames, and VideoMAE classifies its behavior as normal, abnormal or aggressive. The multi-species pipeline is deployed on AWS.

**Highlights**

- Designed after stakeholder research on caretaker shortages at Vandalur Zoo.
- Presented to the Coimbatore Forest Department through the Mayor's office.

![Python](https://img.shields.io/badge/Python-161B22?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-161B22?style=flat-square&logo=pytorch&logoColor=white) ![YOLOv8](https://img.shields.io/badge/YOLOv8-161B22?style=flat-square) ![ByteTrack](https://img.shields.io/badge/ByteTrack-161B22?style=flat-square) ![VideoMAE](https://img.shields.io/badge/VideoMAE-161B22?style=flat-square) ![AWS](https://img.shields.io/badge/AWS-161B22?style=flat-square)

[Repository](https://github.com/Gokulnaath-N/WildGuard)

---

### 3. PayMigo and GeoTruth

**Parametric income protection for gig workers, with an open-source fraud-verification engine.**

```mermaid
flowchart LR
    A["Weather, AQI, geodata"] --> B["XGBoost + LSTM"] --> C["Claim trigger"] --> D["GeoTruth 7 layers"] --> E["Truth Score 0-100"]
    classDef n fill:#161B22,stroke:#22D3EE,color:#F0F6FC
    class A,B,C,D,E n
```

**Problem.** Gig workers lose income when weather or air quality shuts down a shift. Automating payouts only works if the system can tell a genuine disruption from a spoofed location claim.

**Approach.** PayMigo models disruption risk from real-time weather, AQI and geospatial signals. XGBoost and LSTM forecasting trigger income-loss claims automatically, served through FastAPI with PostGIS and Redis. GeoTruth then verifies each claim: a seven-layer geospatial engine with a 38-dimensional feature pipeline looks for location spoofing and sensor inconsistencies and returns an explainable 0 to 100 Truth Score.

**Highlights**

- GeoTruth is published as an open-source package on PyPI (`pip install geotruth`).
- Top 25 Finalist, Guidewire DevTrails 2026 (18,000+ participants across 30 universities in India).

![Python](https://img.shields.io/badge/Python-161B22?style=flat-square&logo=python&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-161B22?style=flat-square) ![LSTM](https://img.shields.io/badge/LSTM-161B22?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-161B22?style=flat-square&logo=fastapi&logoColor=white) ![PostGIS](https://img.shields.io/badge/PostGIS-161B22?style=flat-square) ![Redis](https://img.shields.io/badge/Redis-161B22?style=flat-square&logo=redis&logoColor=white)

[PayMigo](https://github.com/Gokulnaath-N/PayMigo) &nbsp;|&nbsp; [GeoTruth](https://github.com/Gokulnaath-N/GeoTruth) &nbsp;|&nbsp; [GeoTruth on PyPI](https://pypi.org/project/geotruth/)

---

### 4. JobTrust India

**A multi-agent platform that investigates recruitment fraud and scores employment trust.**

```mermaid
flowchart LR
    A["Job case intake"] --> B["18-agent LangGraph"] --> C["Forensics + risk scoring"] --> D["Explainable trust score"]
    classDef n fill:#161B22,stroke:#22D3EE,color:#F0F6FC
    class A,B,C,D n
```

**Problem.** Fake job offers rely on cloned branding, forged documents and convincing language, and no single check catches all of them.

**Approach.** An 18-agent LangGraph pipeline combines LLMs, NLP, OCR and computer vision to examine a job case from several angles and produce an explainable job-trust score. Transformer-based semantic matching with skill-gap detection compares candidates and roles, XGBoost scores anomalies, and RAG with vector search grounds the analysis. Results are served through FastAPI and PostgreSQL, with safeguards against prompt injection.

**Highlights**

- 18 specialized agents orchestrated as a single stateful LangGraph workflow.
- Dedicated OCR and visual-forensics agents inspect logos and documents.

![Python](https://img.shields.io/badge/Python-161B22?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-161B22?style=flat-square&logo=pytorch&logoColor=white) ![Transformers](https://img.shields.io/badge/Transformers-161B22?style=flat-square&logo=huggingface&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-161B22?style=flat-square) ![LangGraph](https://img.shields.io/badge/LangGraph-161B22?style=flat-square) ![FastAPI](https://img.shields.io/badge/FastAPI-161B22?style=flat-square&logo=fastapi&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-161B22?style=flat-square&logo=postgresql&logoColor=white)

[Repository](https://github.com/Gokulnaath-N/Job-Trust-AI)

---

## Professional Experience

**National Institute of Electronics and Information Technology (NIELIT), Calicut**
<br>Research Intern, AI & Machine Learning (December 2025)

- Developed **PlateVision AI**, a real-time, three-stage license-plate recognition pipeline: YOLOv8 detection, OCR, and vehicle-type classification, with a MySQL layer that logs timestamped detections for downstream analytics.
- Built NLP and computer vision pipelines in PyTorch, including a RAG-based chatbot and object-detection systems.

**Infosys Springboard**
<br>Data Analytics Student Intern (January to February 2026)

- Worked on a healthcare analytics project on pharmaceutical supply across government and private hospitals, consolidating 600,000+ records from multiple public datasets.
- Performed data cleaning, EDA and feature engineering with Pandas and NumPy, using row-preserving merge strategies instead of deletion to protect data integrity.
- Built interactive Streamlit dashboards as part of a cross-functional team. [Dashboard code](https://github.com/Gokulnaath-N/HealthCare_analytics_Dashboard)

---

## Technical Arsenal

| Area | Tools and concepts |
| :-- | :-- |
| **Languages** | ![Python](https://img.shields.io/badge/Python-161B22?style=flat-square&logo=python&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-161B22?style=flat-square) ![C++](https://img.shields.io/badge/C%2B%2B-161B22?style=flat-square&logo=cplusplus&logoColor=white) |
| **Data science and analytics** | ![Pandas](https://img.shields.io/badge/Pandas-161B22?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-161B22?style=flat-square&logo=numpy&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-161B22?style=flat-square&logo=scikitlearn&logoColor=white) ![EDA](https://img.shields.io/badge/EDA-161B22?style=flat-square) ![Statistics](https://img.shields.io/badge/Statistics-161B22?style=flat-square) ![Probability](https://img.shields.io/badge/Probability-161B22?style=flat-square) ![Feature Engineering](https://img.shields.io/badge/Feature%20Engineering-161B22?style=flat-square) ![Data Preprocessing](https://img.shields.io/badge/Data%20Preprocessing-161B22?style=flat-square) |
| **Machine learning** | ![Regression](https://img.shields.io/badge/Regression-161B22?style=flat-square) ![Classification](https://img.shields.io/badge/Classification-161B22?style=flat-square) ![Clustering](https://img.shields.io/badge/Clustering-161B22?style=flat-square) ![XGBoost](https://img.shields.io/badge/XGBoost-161B22?style=flat-square) ![Model Evaluation](https://img.shields.io/badge/Model%20Evaluation-161B22?style=flat-square) ![Predictive Analytics](https://img.shields.io/badge/Predictive%20Analytics-161B22?style=flat-square) |
| **Deep learning and vision** | ![PyTorch](https://img.shields.io/badge/PyTorch-161B22?style=flat-square&logo=pytorch&logoColor=white) ![EEGNet](https://img.shields.io/badge/EEGNet-161B22?style=flat-square) ![YOLOv8](https://img.shields.io/badge/YOLOv8-161B22?style=flat-square) ![OpenCV](https://img.shields.io/badge/OpenCV-161B22?style=flat-square&logo=opencv&logoColor=white) ![VideoMAE](https://img.shields.io/badge/VideoMAE-161B22?style=flat-square) |
| **Generative AI and NLP** | ![Transformers](https://img.shields.io/badge/Transformers-161B22?style=flat-square&logo=huggingface&logoColor=white) ![LLMs](https://img.shields.io/badge/LLMs-161B22?style=flat-square) ![RAG](https://img.shields.io/badge/RAG-161B22?style=flat-square) ![LangChain](https://img.shields.io/badge/LangChain-161B22?style=flat-square&logo=langchain&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-161B22?style=flat-square) ![OCR](https://img.shields.io/badge/OCR-161B22?style=flat-square) ![NLP](https://img.shields.io/badge/NLP-161B22?style=flat-square) |
| **Backend and deployment** | ![FastAPI](https://img.shields.io/badge/FastAPI-161B22?style=flat-square&logo=fastapi&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-161B22?style=flat-square&logo=docker&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-161B22?style=flat-square) ![Git](https://img.shields.io/badge/Git-161B22?style=flat-square&logo=git&logoColor=white) |
| **Databases** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-161B22?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-161B22?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-161B22?style=flat-square&logo=redis&logoColor=white) ![PostGIS](https://img.shields.io/badge/PostGIS-161B22?style=flat-square) |

---

## Achievements and Leadership

- **Mentorship:** AI Technical Mentor at the Centre for Innovation, Sri Eshwar College of Engineering, mentoring 150+ students in applied AI/ML and project development.
- **Guidewire DevTrails 2026:** Top 25 Finalist among 18,000+ participants across 30 universities in India.
- **TCS CodeVita Season 13:** Qualifier, Global Rank 16,261 of 146,000+ participants.
- **LeetCode:** 341 problems solved and a contest rating of 1,691 (top 14.88% globally). [Profile](https://leetcode.com/u/Gokulnaath_N/)
- **Open source:** Contributor, GirlScript Summer of Code 2026, AI Agents track.
- **Campus competitions (SECE):** 1st Place, Project Expo | 2nd Place, Prompt Battle | 3rd Place, Freshathon 2025.
- **Nallas Corporate Hackathon 2025:** Finalist.

---

## Certifications

- Oracle Cloud Infrastructure 2025 Certified Foundations Associate
- IBM Data Science
- Mathematics for Machine Learning (DeepLearning.AI)
- Google Crash Course on Python

---

## GitHub Activity

<p align="center">
  <a href="https://github.com/Gokulnaath-N"><img src="https://github-readme-stats.vercel.app/api?username=Gokulnaath-N&show_icons=true&hide_border=true&bg_color=0D1117&title_color=22D3EE&text_color=C9D1D9&icon_color=8B5CF6&ring_color=22D3EE" alt="GitHub stats for Gokulnaath-N"></a>
  <a href="https://github.com/Gokulnaath-N?tab=repositories"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Gokulnaath-N&layout=compact&hide_border=true&bg_color=0D1117&title_color=22D3EE&text_color=C9D1D9&langs_count=6&hide=jupyter%20notebook,html,css" alt="Most used languages on GitHub"></a>
</p>

<p align="center">
  <a href="https://github.com/Gokulnaath-N"><img src="https://streak-stats.demolab.com/?user=Gokulnaath-N&hide_border=true&background=0D1117&ring=22D3EE&fire=8B5CF6&currStreakNum=22D3EE&sideNums=22D3EE&currStreakLabel=C9D1D9&sideLabels=C9D1D9&dates=8B949E" alt="GitHub contribution streak"></a>
</p>

---

## Let's Connect

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-161B22?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Gokulnaath-N) [![LinkedIn](https://img.shields.io/badge/LinkedIn-161B22?style=for-the-badge)](https://linkedin.com/in/gokulnaath-n) [![Email](https://img.shields.io/badge/Email-161B22?style=for-the-badge)](mailto:gokulnaath.n2024cce@sece.ac.in)

I welcome AI/ML collaborations, research discussions and open-source contributions. If you are working on something in this space, get in touch.

</div>
