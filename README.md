# 🚀 TikTok Shop Strategy: Creator Incubation & Content Conversion

### 🔗 [[Live Interactive Dashboard (Tableau)](YOUR_TABLEAU_PUBLIC_LINK_HERE)](https://public.tableau.com/views/TikTokE-commerceHiddenGemDiscoveryDashboard/2_1?:language=zh-CN&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

This project analyzes TikTok e-commerce performance data to optimize creator onboarding and content strategies. By defining **Collect Rate** as the primary proxy for purchase intent, it identifies "Hidden Gem" creators and leverages **NLP** and **Statistical Testing** to uncover actionable conversion drivers.

---

## 👨‍💻 What I Did

* **📌 Role:** Data Analyst | Growth Strategist
* **Metric Engineering & Volume-Weighted Analysis:** Shifted focus from vanity metrics to **Collect Rate (Collects/Views)** to accurately quantify high-intent user behavior and purchase interest. Applied **Volume-Weighted Average** across duration cohorts to eliminate Simpson's Paradox and outlier distortion, revealing the true underlying conversion performance.
* **Creator Efficiency Matrix:** Developed a 2-D segmentation model (Views vs. Efficiency) to identify **67 "Hidden Gem" creators** (approx. 20% of the dataset) who deliver high conversion despite lower view counts.
* **Content NLP & Stopword Tuning:** Cleaned and processed video captions using **Python** to strip marketing noise (`#fyp`, `#musthave`) and expose real product drivers like **Gadgets, Lamps, and Phone Accessories**.
* **Hypothesis Testing:** Executed **Welch’s T-Tests** to validate the causal impact of viral hashtags, providing a statistical baseline for marketing strategy.

---

## 🧠 Project Goal

To uncover how **video duration, caption keywords, and hashtag strategies** predict user conversion (Collect Rate) and to provide a data-backed **Creator Incubation List** for TikTok Shop expansion.

---

## 🛠️ Tools & Tech Stack

| Function | Tools Used |
| :--- | :--- |
| **Data Handling** | Python (pandas, numpy) |
| **Statistical Analysis** | scipy.stats (Welch's T-Test) |
| **NLP & Text Mining** | WordCloud, Iterative Stopword Tuning |
| **Visualization** | matplotlib, seaborn (Log-scale & Subplots), Tableau |

---

## 📥 Key Features Analyzed

| Category | Features |
| :--- | :--- |
| **Post Metadata** | `text` (captions), `duration`, `hashtags` |
| **Engagement** | `views`, `likes`, `collects` |
| **Derived Metrics** | `collect_rate` (Primary KPI), `has_MadeMeBuyIt` (Binary) |

---

## 🧪 Analysis & Engineered Insights

* **Collect Rate:** Defined as `collects / views`. This serves as the North Star metric for "Shopability."
* **Hidden Gem Logic:** `Views < Median` AND `Collect Rate > Global Average`. (Target: 67 Creators identified).
* **Duration Segmentation:** Analyzed performance across 5 time-bins to find the "Retention Sweet Spot."

---

## 📊 Core Findings

| Analysis | Key Metric / Outcome | Business Insight |
| :--- | :--- | :--- |
| **Duration Analysis** | **30-45s** peaked at **0.74%** weighted CR. | Conversion efficiency drops significantly after 45s. The 30-45s window is the statistical "Sweet Spot" for maximizing both traffic volume and purchase intent. |
| **Outlier Detection** | Identified **Sample Size Bias** in `60s+` cohort. | Discovered that while some ultra-long videos had a high CR, the extremely low video count (only 23 videos) indicated viral anomalies rather than a replicable strategy. |
| **NLP Word Cloud** | Top Terms: **Gadget, Lamp, Phone** | Merchandising focus should stay on Home Tech and Mobile Accessories. |
