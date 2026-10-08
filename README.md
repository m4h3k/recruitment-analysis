# **📊 RECRUITMENT FUNNEL ANALYSIS**

An exploratory data analysis project focused on understanding the recruitment funnel, hiring performance, department-wise trends, sourcing channels, and time-to-hire using Python.
The project analyzes recruitment data to identify where candidates drop out of the hiring process and which departments and recruitment sources contribute most effectively to successful hires.

# **🔗 Project Notebook**
```
👉 Recruitment Analysis.ipynb
```
# **📌 Project Overview**

Recruitment teams receive candidates through multiple channels and move them through different stages before a successful hire.

This project analyzes that process as a recruitment funnel:
```
Applied
   ↓
Screening
   ↓
Interview
   ↓
Offer
   ↓
Hired
```

The analysis focuses on understanding:

- Candidate progression through the recruitment funnel
- Drop-off at each hiring stage
- Hiring performance by department
- Effectiveness of recruitment sources
- Average and median time required to hire candidates

# **🎯 Objectives**

The main objectives of this project are:

- Understand the structure and quality of the recruitment dataset.
- Clean missing and duplicate records.
- Analyze candidate progression through recruitment stages.
- Calculate stage-wise candidate drop-off.
- Identify departments with the highest number of hires.
- Compare recruitment source performance.
- Analyze overall time-to-hire.
- Compare hiring time across departments.

# **📂 Dataset**

The dataset contains 5,215 candidate records and 7 columns:

| Column | Description |
|---|---|
| `candidate_id` | Unique identifier for each candidate |
| `department` | Department for which the candidate applied |
| `source` | Recruitment channel/source |
| `application_date` | Date on which the candidate applied |
| `stage_reached` | Final recruitment stage reached by the candidate |
| `offer_status` | Status of the candidate's offer |
| `time_to_hire_days` | Number of days required to hire the candidate |

The dataset initially contained:
- 5,215 rows
- 7 columns
- 15 duplicate rows
- 40 missing values in source
- 4,638 missing values in time_to_hire_days, which is expected for candidates who were not hired.

# **🧹 Data Cleaning**

The following preprocessing steps were performed:

- Duplicate Removal :
The dataset contained 15 duplicate records.These records were removed, leaving 5,200 unique candidate records for analysis.
- Missing Recruitment Sources :
There were 40 missing values in the source column. Instead of removing these candidates, the missing values were replaced with: "Unknown"
This preserved the candidate records while clearly identifying candidates whose recruitment source was unavailable.


# **📈 Key Insights**

## 1\. Recruitment Funnel

After data cleaning, the recruitment funnel contained **5,200 unique candidates** at the application stage.

| Recruitment Stage | Candidates |
| --- | --- |
| Applied | 5,200 |
| Screening | 3,581 |
| Interview | 1,931 |
| Offer | 793 |
| Hired | 576 |

The funnel shows a significant reduction in candidates as they progress through the recruitment process.

### Stage-wise Drop-off

| Stage Transition | Drop-off |
| --- | --- |
| Applied → Screening | 31.13% |
| Screening → Interview | 46.08% |
| Interview → Offer | 58.93% |
| Offer → Hired | 27.36% |

The **largest drop-off occurs between the Interview and Offer stages**, where approximately **58.93% of candidates are lost**.

This suggests that the interview-to-offer stage is the most restrictive point in the recruitment funnel.

---

## 2\. Overall Hiring Conversion

Out of **5,200 candidates**, **576 candidates were hired**.

This represents an overall hiring conversion rate of approximately:

**11.08%**

```
5,200 Applicants
       ↓
   576 Hires
       ↓
  11.08% Conversion
```

This provides a high-level view of how effectively the recruitment pipeline converts applicants into successful hires.

---

## 3\. Department-wise Hiring

The analysis compares hiring performance across different departments.

| Department | Hires |
| --- | --- |
| Engineering | 133 |
| Sales | 130 |
| Marketing | 104 |

**Engineering** recorded the highest number of hires, closely followed by **Sales**.

This indicates that Engineering and Sales represent two of the strongest departments in terms of absolute hiring volume within the analyzed dataset.

---

## 4\. Recruitment Source Analysis

Candidates came from several recruitment channels:

| Recruitment Source | Candidates |
| --- | --- |
| LinkedIn | 1,569 |
| Job Portal | 1,286 |
| Referral | 1,080 |
| Campus Drive | 727 |
| Walk-in | 498 |
| Unknown | 40 |

**LinkedIn** generated the highest number of applicants, followed by **Job Portal** and **Referral**.

However, applicant volume alone does not necessarily indicate recruitment effectiveness. Therefore, the analysis also examines the conversion rate of candidates from different recruitment sources.

### Source Conversion

The analysis compares recruitment sources based on their ability to convert applicants into successful hires.

Some observed conversion rates include:

| Recruitment Source | Conversion Rate |
| --- | --- |
| Walk-in | 10.04% |
| LinkedIn | 9.62% |
| Unknown | 7.50% |

The analysis also evaluates other recruitment channels to distinguish between sources that generate high applicant volume and sources that generate better hiring outcomes.

---

## 5\. Time-to-Hire Analysis

For successfully hired candidates:

- **Average time-to-hire:** 32.1 days
- **Median time-to-hire:** 30.2 days

This indicates that a typical successful candidate takes approximately **one month** to move through the recruitment process.

The project also analyzes time-to-hire across departments to identify areas where the recruitment process may be comparatively faster or slower.

---

# **💡 Business Insights**

Based on the analysis, several practical observations can be made.

### 🔹 Focus on the Interview → Offer Stage

The **58.93% drop-off between Interview and Offer** is the largest funnel loss.

Recruitment teams could investigate:

- Interview evaluation criteria
- Candidate-job fit
- Interview consistency
- Hiring manager decision-making
- Candidate expectations versus job requirements

Improving this stage could potentially have a significant impact on overall hiring conversion.

### 🔹 Don't Optimize Only for Applicant Volume

LinkedIn generates the largest number of applicants, but applicant volume alone does not indicate recruitment effectiveness.

Recruitment teams should consider both:

- Number of applicants generated
- Percentage of applicants converted into hires

This provides a more complete picture of sourcing-channel performance.

### 🔹 Referrals and Campus Drives Show Strong Potential

The analysis indicates that **Referral and Campus Drive** candidates show stronger conversion performance than several other channels.

This suggests that these channels may be worth further consideration when developing recruitment sourcing strategies.

### 🔹 Hiring Takes Approximately One Month

With an average time-to-hire of **32.1 days** and a median of **30.2 days**, successful candidates typically spend around one month moving through the hiring process.

Recruitment teams could investigate department-level differences in hiring time to identify potential process bottlenecks.

---

# **📊 Analysis Workflow**

The project follows a standard data analytics workflow:

```
Raw Recruitment Data
        ↓
Data Inspection
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Recruitment Funnel Analysis
        ↓
Department Analysis
        ↓
Source Performance Analysis
        ↓
Time-to-Hire Analysis
        ↓
Business Insights
```

# **🛠️ Technologies Used**

- **Python**
- **Jupyter Notebook**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization

---

# **📊 Visualizations**

The notebook uses data visualizations to analyze:

- Recruitment funnel
- Candidate drop-off
- Department-wise hiring
- Hiring conversion rates
- Time-to-hire distribution
- Department-wise hiring time
- Recruitment-source performance

These visualizations make it easier to identify recruitment bottlenecks and compare hiring performance across different dimensions.

---

# **📁 Project Structure**

```
recruitment-analysis/
│
├── Recruitment Analysis.ipynb
├── hiring_data.csv
└── README.md
```

---

# **🚀 How to Run the Project**

## 1\. Clone the Repository

```
git clone https://github.com/m4h3k/recruitment-analysis.git
cd recruitment-analysis
```

## 2\. Install Dependencies

```
pip install pandas numpy matplotlib seaborn jupyter
```

## 3\. Launch Jupyter Notebook

```
jupyter notebook
```

Open the following notebook:

```
Recruitment Analysis.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

---

# **🔮 Future Improvements**

This project can be extended by:

- Developing a machine learning model to predict hiring outcomes.
- Predicting candidate drop-off probability.
- Adding additional candidate attributes such as experience and skills.
- Developing an interactive **Streamlit** recruitment analytics application.

---

# **📌 Conclusion**

This project demonstrates how **Exploratory Data Analysis can be used to evaluate and improve recruitment processes**.

The analysis highlights important recruitment KPIs:

| KPI | Value |
| --- | --- |
| Unique Candidates Analyzed | 5,200 |
| Successful Hires | 576 |
| Overall Hiring Conversion | 11.08% |
| Highest Funnel Drop-off | Interview → Offer |
| Interview → Offer Drop-off | 58.93% |
| Average Time-to-Hire | 32.1 days |
| Median Time-to-Hire | 30.2 days |

Overall, this project demonstrates practical skills in:

- Data cleaning
- Exploratory data analysis
- Recruitment funnel analysis
- Data visualization
- KPI analysis

---
