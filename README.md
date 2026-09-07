# 🎥 YouTube Channels EDA & NLP Analysis

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)](youtube-project-with-notes.ipynb)
[![YouTube API](https://img.shields.io/badge/YouTube%20API-v3-FF0000?style=flat&logo=youtube&logoColor=white)](https://developers.google.com/youtube/v3)

A Data Analysis and Natural Language Processing (NLP) project extracting real-time metrics and analyzing engagement drivers across prominent educational & critical thinking YouTube channels using the **YouTube Data API v3**.

---

## 📌 Channels Included in Scope
* **Johnny Harris** (Geo-politics, Visual Journalism)
* **Wisecrack** (Pop Culture, Philosophy & Media Analysis)
* **Some More News** (Political Satire & Current Events)
* **Adam Conover** (Educational Comedy & Debunking)

> ℹ️ **Data Snapshot Note:** All channel metrics, video engagement stats, and video title metadata were extracted using the YouTube Data API v3 in **July 2023**.

---

## 🎯 Project Aims & Objectives
1. **API Data Pipeline:** Build custom modular Python functions to query Google's YouTube Data API v3 (`channels`, `playlistItems`, `videos` endpoints) and parse nested JSON responses into clean Pandas DataFrames.
2. **Hypothesis Testing & "Myth-Busting":** Evaluate common YouTube growth assumptions:
   * Do likes and comments correlate directly with higher view counts?
   * Does video duration impact interaction rates or total views?
   * How does title character length affect performance?
3. **Text Mining & Topic Modeling (NLP):** Clean and tokenize video title metadata using **NLTK** (stop-word removal, text normalization) to build frequency distributions and **WordClouds** highlighting viral content themes.

---

## 🛠️ Tech Stack & Tools
* **Data Extraction:** `googleapiclient.discovery` (YouTube Data API v3)
* **Data Manipulation:** `pandas`, `numpy`, `isodate`, `python-dateutil`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Natural Language Processing:** `nltk` (tokenization, stop-words), `wordcloud`

---

## 💡 Key Pipeline Implementation
The extraction workflow is split into three core functions:
* `get_channel_stats()`: Fetches global subscriber counts, total views, video count, and upload playlist IDs.
* `get_video_ids()`: Implements pagination handling (`nextPageToken`) to retrieve every video ID within a target channel playlist.
* `get_video_details()`: Batches API requests in chunks of 50 to extract metadata (`title`, `tags`, `publishedAt`, `duration`) and engagement statistics (`viewCount`, `likeCount`, `commentCount`).

---

## 👤 Author 

Leandro Soares: [LinkedIn Profile](https://www.linkedin.com/in/leandro-soares-91912097/)

---

## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/leandrod1/youtube-analysis.git](https://github.com/leandrod1/youtube-analysis.git)
   cd youtube-analysis
