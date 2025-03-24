# 📊 TikTok Video Claim Classification - Data Inspection & Preparation

## 🚀 Project Overview
This project is part of TikTok’s machine learning initiative to build a model that classifies video text as **claims** or **opinions**. 

The dataset contains TikTok video metadata, user engagement metrics, and preliminary labels. The goal of this phase is to inspect, clean, and prepare the dataset for exploratory data analysis (EDA) and model development.

---

## 🎯 Objectives
✅ Import the dataset and review structure  
✅ Inspect data types and check for missing values  
✅ Identify relevant and irrelevant variables  
✅ Analyze key numeric columns (min, max values)  
✅ Perform initial feature engineering  
✅ Prepare a clean dataset for the next phase (EDA and modeling)

---

## 📁 Dataset Description
**Sample Columns (example structure):**
- `video_id` — Unique video identifier
- `user_id` — Unique user identifier
- `video_text` — Transcript or text from the video
- `likes` — Number of likes
- `shares` — Number of shares
- `comments` — Number of comments
- `upload_date` — Date of upload
- `claim_label` — Target variable: "claim" or "opinion"
- `user_bio` — User profile bio
- `video_url` — URL to the video

---

## 🛠 Data Processing Steps
1. **Data Import & Initial Review**
   - Loaded the dataset into a Pandas DataFrame
   - Displayed the first few rows for quick inspection
   
2. **Data Types & Missing Values**
   - Ran `.info()` and `.isnull().sum()` to check data types and null counts

3. **Column Relevance**
   - **Kept:** `video_text`, `likes`, `shares`, `comments`, `claim_label`
   - **Dropped (planned):** `upload_date`, `user_bio`, `video_url`
   
4. **Variable Exploration**
   - Reviewed `likes`, `shares`, and `comments` min/max values
   - Identified potential skew and outliers for future handling

5. **Feature Engineering**
   - Created `engagement = likes + shares + comments`
   - Created `text_length = word count of video_text`

---

## 📈 Sample Insights
| Feature     | Min | Max  |
|------------ |---- |----- |
| Likes       | 0   | 1.2M |
| Shares      | 0   | 350K |
| Comments    | 0   | 250K |
| Text Length | 3   | 300  |

---

## 📂 Next Steps
- Full Exploratory Data Analysis (EDA)
- Text pre-processing for model readiness
- Model selection and training (NLP focus)

---

## 👥 Contributors
- Rosie Mae Bradshaw — Data Science Manager
- Orion Rainier — Data Scientist
- **Your Name** — Data Analyst (Notebook & Data Preparation)

---

## 💡 Quote from the Team
*"Big data isn’t about bits, it’s about talent." — Douglas Merrill*
