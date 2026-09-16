### YouTube User Behavior & Engagement Analytics

## 🎯 Project Overview

An exploratory analytics project using **1 million YouTube user-video interactions** to understand **viewing behavior, watch completion, and user engagement patterns**.

The analysis explores how factors such as **video length, viewing behavior, and engagement actions** relate to user interaction and watch completion, with a focus on identifying meaningful patterns in the data.

---

## 📌 Key Findings

* **Watch completion decreases substantially as video length increases.**
* Average completion fell from **93.49%** for shorter videos to **56.36%** for very long videos.
* **Like rates remained around 30%** across all video-length groups.
* **Comment rates remained around 10%** across all groups.
* Video length showed a much stronger observed relationship with **watch completion** than with likes or comments.

---

## 📊 Dashboard

The Tableau dashboard summarizes:

* Watch completion by video length
* Like vs. comment rates by video length
* Overall engagement rates

![YouTube User Behavior & Engagement Dashboard](dashboard/YouTube%20User%20Behavior%20%26%20Engagement%20Dashboard.png)

**Tableau Public:** [View Interactive Dashboard](https://public.tableau.com/views/youtube_dashboard_17895558860970/YouTubeUserBehaviorEngagementDashboard?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)

---

## 🔍 Analysis Performed

### Video Length & Watch Completion

Videos were divided into four balanced length groups using quartiles:

| Video Length | Avg. Watch Completion |
| ------------ | --------------------: |
| Shorter      |                93.49% |
| Moderate     |                81.08% |
| Long         |                68.84% |
| Very Long    |                56.36% |

### Engagement

Overall engagement rates were also examined across the dataset:

* Like rate: **30.07%**
* Comment rate: **9.95%**
* Click rate: **30.08%**
* Subscription rate: **5.00%**

---

## 🧹 Data Preparation

The raw dataset contained inconsistent categorical values and invalid numerical records.

Key preparation steps included:

* Standardized category and engagement values
* Handled invalid `liked` values
* Corrected negative and excessive `watch_time`
* Handled zero-duration videos
* Recalculated `watch_percent`
* Converted timestamps to datetime
* Checked for duplicate records and final data quality

The cleaned dataset contains **1,000,000 interactions and 16 analysis-ready columns**.

---

## 🛠️ Tools Used

* **Python** — data preparation and exploratory analysis
* **Pandas** — data manipulation
* **Matplotlib** — analysis visualization
* **Tableau Public** — interactive dashboard
* **Git/GitHub** — project version control

---

## 📂 Project Structure

```text
youtube-user-behavior-analytics/
│
├── data/
│   ├── youtube recommendation dataset.csv
│   └── youtube_cleaned.csv
│
├── notebooks/
│   └── youtube.ipynb
│
├── dashboard/
│   ├── YouTube User Behavior & Engagement Dashboard (1).pdf
│   ├── YouTube User Behavior & Engagement Dashboard.png
│   └── youtube_dashboard.twbx
│
└── README.md
```

---

## 💡 Business Takeaway

The analysis shows a clear observed relationship between **video length and watch completion**: longer videos had substantially lower average completion rates in this dataset, while like and comment rates remained relatively stable.

For a video platform, this type of analysis can help identify where **content length may be associated with viewer drop-off**, while separating completion behavior from other forms of engagement.

**Note:** The dataset is synthetic and the analysis describes observed patterns, not causal effects or real YouTube user behavior.
