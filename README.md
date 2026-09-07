# Curriculum Vitae - Rizky Yanuar Kristianto

[![Build and Deploy CV](https://github.com/rizkyyanuark/curriculum-vitae/actions/workflows/build.yml/badge.svg)](https://github.com/rizkyyanuark/curriculum-vitae/actions/workflows/build.yml)
[![Live CV](https://img.shields.io/badge/Live%20CV-GitHub%20Pages-2ea44f?style=flat-square&logo=github)](https://rizkyyanuark.github.io/curriculum-vitae/)
[![PDF Download](https://img.shields.io/badge/Download-PDF-red?style=flat-square&logo=adobeacrobatreader)](https://rizkyyanuark.github.io/curriculum-vitae/cv.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-rizkyyanuark-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/rizkyyanuark)
[![Portfolio](https://img.shields.io/badge/Portfolio-rizkyyanuark.vercel.app-black?style=flat-square&logo=vercel)](https://rizkyyanuark.vercel.app/)

A clean, modern, and ATS-friendly Curriculum Vitae written in **LaTeX**, fully integrated with **GitHub Actions CI/CD** to automatically compile the `cv.tex` source file and publish the latest version to **GitHub Pages** on every push.

---

## 🌐 Live Access

You can view or download the live, constantly updated version of this CV at:

* **Interactive Browser Link:** [https://rizkyyanuark.github.io/curriculum-vitae/](https://rizkyyanuark.github.io/curriculum-vitae/) *(instantly redirects to the latest PDF)*
* **Direct PDF Download:** [https://rizkyyanuark.github.io/curriculum-vitae/cv.pdf](https://rizkyyanuark.github.io/curriculum-vitae/cv.pdf)

---

## 📄 Curriculum Vitae Overview

The resume is tailored for **AI Data Engineer**, **Data Engineer**, and **Machine Learning Engineer** roles with a structured 2-page layout:

* **Header & Contact:** Direct phone (+6289676257683), verified email, LinkedIn, and GitHub links.
* **Summary:** Impact-driven profile highlighting scalable data pipelines, AI/ML workflows, and cloud deployments.
* **Education:** Bachelor of Data Science, State University of Surabaya (UNESA) - GPA 3.59/4.00 (145 Credits).
* **Work Experiences:**
  - **State University of Surabaya** - Research Assistant (Generative deep learning architectures, IEEE manuscript, 99.5% compute uptime on AWS EC2 GPU).
  - **Dinas Kominfo Jawa Timur** - AI Engineer Intern (Majadigi RAG Chatbot, NLP hoax detection, GitLab CI/CD, Linux VPS).
  - **PT PLN Icon Plus** - Data Engineer Intern (Airflow & PySpark ETL for 240,000+ daily operational records, data modeling, LLM AI Agent).
  - **Bangkit Academy (Google, GoTo, Traveloka)** - Machine Learning Engineer & Capstone Team Lead (Best Presenting Group out of 30+ teams, NV-Bite).
* **Organizational Experience:** Himpunan Mahasiswa Sains Data (Staff of Advocacy & Welfare, InSCAW Career Workshop).
* **Key Projects:**
  - **Hybrid Graph-RAG Knowledge Base (Yunesa):** Neo4j + Milvus multi-hop reasoning over 10,000+ papers, Scopus Q1 review.
  - **Sentiment Analysis Pipeline (KIP-K Tweets):** Automated Python pipeline, BiLSTM (88% accuracy), Looker Studio dashboard.
* **Technical Skills & Certifications:** Python, SQL, Apache Airflow, PySpark, PostgreSQL, BigQuery, Neo4j, Milvus, TensorFlow, AWS, GCP, Docker, MLOps.

---

## ⚙️ How the CI/CD Pipeline Works

1. **Trigger:** Any push to the `main` branch triggers the GitHub Actions workflow defined in [`.github/workflows/build.yml`](.github/workflows/build.yml).
2. **Build:** A dedicated Ubuntu runner spins up a TeXLive Docker container (`dante-ev/latex-action@latest`), compiles `cv.tex`, and validates the resulting `cv.pdf`.
3. **Deploy:** The workflow automatically commits and deploys `cv.pdf`, `index.html` (for auto-redirection), and `.nojekyll` to the orphan `build` branch using `peaceiris/actions-gh-pages@v4`.
4. **Publish:** GitHub Pages serves the `build` branch at `https://rizkyyanuark.github.io/curriculum-vitae/`.

---

## 🛠️ Quickstart & Local Editing

### Editing Online or Locally:
1. Clone this repository:
   ```bash
   git clone https://github.com/rizkyyanuark/curriculum-vitae.git
   cd curriculum-vitae
   ```
2. Modify `cv.tex` using your preferred text editor (VS Code, Antigravity, or Overleaf).
3. Commit and push changes:
   ```bash
   git add cv.tex
   git commit -m "update: add new certification or experience"
   git push origin main
   ```
4. Within 1-2 minutes, GitHub Actions will compile and update the live PDF automatically.

---

## 📬 Contact & Connect

* **Email:** [rizkyyanuarkristianto@gmail.com](mailto:rizkyyanuarkristianto@gmail.com)
* **LinkedIn:** [linkedin.com/in/rizkyyanuark](https://www.linkedin.com/in/rizkyyanuark)
* **GitHub:** [github.com/rizkyyanuark](https://github.com/rizkyyanuark)
* **Portfolio:** [rizkyyanuark.vercel.app](https://rizkyyanuark.vercel.app/)
