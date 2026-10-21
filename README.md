# Hospital-Performance-Data-Analysis
Hospital Performance Data Analysis:  A Python-Based Data Analysis Project

ABSTRACT

Healthcare institutions generate vast amounts of data related to patient admissions, treatments,
billing, insurance coverage, and hospital operations. Analysing this data helps healthcare
organizations improve patient care, optimize resource utilization, and enhance operational
efficiency. This project focuses on the analysis of a Hospital Performance Dataset containing
approximately 2,100 patient records and 25 attributes.
The project involved data loading, data cleaning, preprocessing, missing value treatment, duplicate
removal, outlier detection, data validation, exploratory data analysis (EDA), correlation analysis,
and data visualization using Python. Various statistical and visual analytical techniques were
applied to understand patterns in patient demographics, treatment costs, insurance coverage,
patient billing, waiting times, and satisfaction scores. The analysis revealed that treatment cost has
a strong influence on patient billing, while patient satisfaction is only weakly related to treatment
expenses and length of hospital stay. Insurance coverage plays a significant role in reducing patient
financial burden. Interactive dashboards and visualizations were developed using Plotly to
facilitate effective healthcare decision-making.
Keywords: Healthcare Analytics, Hospital Performance, Python, Data Analysis, Patient
Satisfaction, Treatment Cost, Visualization.

1. INTRODUCTION

The Hospital Performance Data Analysis project aims to examine healthcare data to understand
patterns related to patient care, hospital operations, treatment expenses, and service quality.
Hospitals generate large volumes of information through patient admissions, diagnoses,
treatments, billing transactions, insurance claims, and satisfaction surveys. Analysing this
information helps healthcare organizations evaluate their performance and make data-driven
decisions.
The dataset used in this project contains approximately 2,100 patient records with details such as
age, gender, hospital name, department, diagnosis, admission type, treatment costs, insurance
coverage, patient bills, waiting time, length of stay, and satisfaction scores. These variables provide
a comprehensive view of both the clinical and operational aspects of hospital management.
Before analysis, the dataset underwent several preprocessing steps to improve data quality.
Missing values were identified and treated using appropriate statistical methods, categorical
variables were standardized, and date and numerical fields were converted into suitable formats.
Outliers in variables such as treatment cost, insurance coverage, patient billing, and satisfaction
scores were detected using the Interquartile Range (IQR) method and treated to minimize their
impact on analysis results.
After preprocessing, Exploratory Data Analysis (EDA) was carried out to investigate patient
demographics, departmental workloads, admission patterns, treatment expenses, insurance
utilization, and patient satisfaction levels. Statistical summaries, correlation analysis, and
visualizations created using Python libraries such as Pandas, Matplotlib, Seaborn, and Plotly were
used to identify trends, distributions, and relationships among key hospital performance indicators.

The study also explores how factors such as treatment cost, insurance coverage, waiting time, and
length of hospital stay influence overall patient experience. Interactive dashboards were developed
to present the findings in a clear and user-friendly manner, enabling easier interpretation of hospital
performance metrics.
The primary goal of this project is to transform raw hospital data into meaningful insights that can
support healthcare administrators in improving operational efficiency, financial planning, resource
allocation, and patient satisfaction. Through analytical techniques and visualization tools, the
project demonstrates the value of data analytics in enhancing the quality and effectiveness of
healthcare services

2. PROBLEM STATEMENT
   
The main problem addressed in this project is that hospitals generate a large amount of patient,
treatment, billing, and operational data, but it is often difficult to extract meaningful insights from
raw data due to missing values, duplicates, inconsistencies, and outliers. Without proper analysis,
hospitals may find it challenging to understand factors affecting treatment costs, patient
satisfaction, insurance utilization, and overall performance. Therefore, this project aims to analyse
hospital data using data analytics techniques to generate actionable insights that can support better
decision-making and improve healthcare services.

4. PROJECT OBJECTIVES

• The specific objectives of the project are:
• To perform data cleaning and preprocessing on the hospital dataset.
• To identify and handle missing values, duplicate records, and inconsistent data.
• To detect and treat outliers using appropriate statistical techniques.
• To analyse patient demographics such as age and gender distribution.
• To study hospital departments, admission types, and diagnosis patterns.
• To evaluate treatment costs, insurance coverage, and patient billing trends.
• To analyse waiting times, length of stay, and patient satisfaction scores.
• To identify relationships among key hospital performance indicators through correlation
analysis.
• To create meaningful visualizations using Matplotlib, Seaborn, and Plotly.
• To develop interactive dashboards for better understanding of hospital performance metrics.
• To generate actionable insights and recommendations that can help improve hospital
operations, resource utilization, financial planning, and patient satisfaction.

4. DATASET DESCRIPTION

The dataset used in this project is a Hospital Performance Dataset consisting of approximately
2,100 patient records and 25 attributes. The dataset contains information related to patient
demographics, hospital departments, medical treatments, financial transactions, insurance
coverage, waiting times, and patient satisfaction. The data was analysed to study healthcare service
efficiency, treatment expenditures, patient experience, and hospital operational performance.
During the preprocessing stage, missing values were identified and handled using appropriate
statistical techniques. Duplicate records were removed, column names were standardized, data
types were corrected, and outliers were treated using the Interquartile Range (IQR) method. After
data cleaning and validation, approximately 2,063 records were retained for analysis



## Dataset Description

| Field | Meaning / Use in Analysis |
|--------|---------------------------|
| patient_id | Unique identifier assigned to each patient record. |
| age | Patient age used for demographic and distribution analysis. |
| gender | Gender category used for patient population analysis. |
| city | Patient location used for city-wise analysis. |
| hospital_name | Name of the hospital associated with the patient. |
| department | Medical department responsible for treatment. |
| doctor_name | Attending doctor associated with the patient's case. |
| admission_type | Type of admission such as Emergency or Regular. |
| diagnosis | Medical condition diagnosed for the patient. |
| treatment_type | Category of treatment provided. |
| admission_date | Date of patient admission. |
| discharge_date | Date of discharge from the hospital. |
| length_of_stay | Total hospitalization duration in days. |
| treatment_cost | Overall treatment expenditure incurred. |
| insurance_covered | Amount covered through insurance. |
| patient_bill | Final amount payable by the patient. |
| medicine_cost | Cost of medicines prescribed during treatment. |
| test_cost | Cost incurred for diagnostic and laboratory tests. |
| doctor_fee | Consultation and professional medical fee. |
| wait_time_minutes | Patient waiting time before receiving medical attention. |
| satisfaction_score | Patient satisfaction rating used for service evaluation. |
| payment_method | Method used to settle hospital payments. |
| bed_type | Type of hospital bed allocated to the patient. |
| readmission_flag | Indicates whether the patient was readmitted after discharge. |


5.TOOLS AND TECHNOLOGIES USED

Various tools and technologies were used throughout this project to perform data cleaning,
preprocessing, exploratory data analysis, statistical evaluation, and data visualization. These tools
helped in transforming raw hospital data into meaningful insights and visual representations.

## Tools and Technologies Used

| Library/Tool | Purpose in the Project |
|--------------|------------------------|
| Pandas | Used for data loading, cleaning, preprocessing, and manipulation of the hospital dataset. |
| NumPy | Used for numerical computations and statistical operations. |
| Matplotlib | Used to create charts such as histograms, bar plots, and scatter plots. |
| Seaborn | Used for advanced statistical visualizations such as box plots and correlation heatmaps. |
| Plotly | Used to create interactive charts and dashboards for hospital performance analysis. |
| Google Colab | Used as the platform for coding, executing Python programs, and visualizing results. |



6. DATA CLEANING AND PREPROCESSING
   
The Hospital Performance Dataset was cleaned and pre-processed to ensure consistency, improve
data quality, and prepare the data for analysis. The preprocessing stage addressed missing values,
column naming issues, data-type inconsistencies, categorical variations, and invalid records. The
following steps were carried out.
6.1 Column Names and Renamed Fields
Column names were standardized by removing leading and trailing spaces, converting all names
to lowercase, and replacing spaces with underscores. Special characters and formatting
inconsistencies were also removed.

## Column Renaming

| Original Column Name | Renamed Column |
|---------------------|----------------|
| charges_amt | treatment_cost |
| insurance_amt | insurance_covered |
| patient_satisfaction | satisfaction_score |
| admissiondate | admission_date |
| dischargedate | discharge_date |
| lengthofstay | length_of_stay |
| patientid | patient_id |
| patientname | patient_name |
| doctorfee | doctor_fee |

6.2 Missing Values

Missing values were identified and treated according to the nature of each variable. Numerical
columns were filled using median values, while categorical columns were filled using the most
frequently occurring category (mode).

## Missing Value Treatment

| Column(s) | Missing-Value Treatment |
|-----------|--------------------------|
| age, treatment_cost, insurance_covered, patient_bill, medicine_cost, test_cost, doctor_fee, wait_time_minutes, satisfaction_score | Filled with the median value of the respective column. |
| city, department, gender, treatment_type, payment_method, doctor_name, hospital_name, admission_type, diagnosis, bed_type | Filled with the most frequent category (mode). |

Before preprocessing, missing values were identified in both numerical and categorical variables.
Numerical variables such as age, treatment cost, insurance covered, patient bill, medicine cost, test
cost, doctor fee, wait time minutes, and satisfaction score were imputed using their median values
to reduce the impact of extreme observations. Categorical variables including city, department,
gender, treatment type, payment method, doctor name, hospital name, admission type, diagnosis,
and bed type were imputed using the most frequently occurring category (mode). After applying
these treatments, the dataset was rechecked to ensure that no critical missing values remained.

6.2 Duplicates

The dataset was examined for duplicate observations using the duplicated () function.
The duplicate-record check did not identify any duplicate rows. Since all patient records were
unique, no observations were removed during this step. The absence of duplicate records helped
maintain the integrity of the analysis and ensured that patient information was not counted more
than once.

6.3 Data types

Several variables were initially stored as object (text) data types and required conversion into
appropriate formats before analysis.
Admission and discharge date fields were converted to datetime format using the pd.to_datetime()
function. Validation checks confirmed that there were zero invalid admission dates and zero invalid
discharge dates after conversion.
Financial variables were converted to numeric format after removing currency symbols and
formatting characters.
The errors='coerce' parameter was used during conversion so that invalid entries were converted to missing values and subsequently handled through imputation.

## Data Type Conversion

During preprocessing, date and numerical fields were converted into appropriate formats to enable accurate analysis.

| Column(s) | Conversion Applied |
|-----------|-------------------|
| admission_date, discharge_date | Converted to datetime format using `pd.to_datetime()`. |
| treatment_cost, insurance_covered, patient_bill, medicine_cost, test_cost, doctor_fee | Converted to numeric format using `pd.to_numeric()` after removing currency symbols and commas. |
| age, wait_time_minutes, satisfaction_score | Converted to numeric format using `pd.to_numeric()`. Missing values generated during conversion were handled through imputation. |

6.4 Standardizing categorical values
Categorical variables were standardized to eliminate inconsistencies caused by capitalization
differences, extra spaces, and spelling variations. All categorical values were converted to
lowercase and stripped of unnecessary whitespace to ensure uniform formatting

The following columns were standardized: gender, department, payment_method, doctor_name,
city, hospital_name, admission_type, diagnosis, treatment_type, readmission_flag, bed_type
In addition, department names were standardized to correct spelling variations and abbreviated
forms.

## Data Standardization

To ensure consistency across categorical values, similar department names were standardized during data preprocessing.

| Original Value | Standardized Value |
|---------------|-------------------|
| cardio | cardiology |
| cardiologyg | cardiology |
| ortho | orthopaedics |
| orthopedics | orthopaedics |
| neuro | neurology |
| neurologgy | neurology |

7. OUTLIER ANALYSIS

An outlier is a value that lies unusually far from the main distribution. The analysis applies the
Interquartile Range (IQR) method and checks the age, treatment_cost, insurance_covered,
wait_time_minutes, and satisfaction_score columns. The summary statistics reveal a small
number of extreme observations, particularly in the insurance coverage variable.
IQR Method
Q1 is the 25th percentile and Q3 is the 75th percentile. The interquartile range is calculated as:
IQR = Q3 − Q1
The conventional lower and upper fences are:
Q1 − 1.5 × IQR and Q3 + 1.5 × IQR

## Outlier Analysis Using IQR Method

The Interquartile Range (IQR) method was used to identify potential outliers in selected numerical variables. Outliers were flagged for analysis but retained where appropriate to preserve important healthcare-related variations.

| Column | Q1 | Q3 | IQR | Upper IQR Fence | Values Flagged in Analysis |
|---------|--------|--------|---------|----------------|---------------------------|
| age | 34 | 67 | 33 | 116.5 | One outlier detected |
| treatment_cost | 83,995.5 | 211,559 | 127,563.5 | 402,904.25 | No outliers detected |
| insurance_covered | 24,200 | 94,850 | 70,650 | 200,825 | Twenty-eight outliers detected |
| wait_time_minutes | 34 | 90 | 56 | 174 | No outliers detected |
| satisfaction_score | 3 | 8 | 5 | 15.5 | No outliers detected |

The analysis identifies one outlier in the age column and twenty-eight outliers in the
insurance_covered column. No outliers are detected in treatment_cost, wait_time_minutes, or
satisfaction_score based on the IQR criteria.
Following capping, the dataset retains 2,063 records and all observations remain available for
Exploratory Data Analysis (EDA). This approach improves robustness while preserving
potentially meaningful healthcare records involving unusually high insurance coverage amounts.

8.EXPLORATORY DATA ANALYSIS

Exploratory Data Analysis (EDA) was performed to understand the distribution, central tendency,
variability, and relationships among variables in the Hospital Performance Dataset. Both
numerical and categorical variables were analysed to identify patterns related to patient
demographics, treatment costs, hospital operations, and patient satisfaction.
8.1 Numerical Data Analysis
The numerical columns were analysed using the mean, median, minimum, maximum, and standard
deviation to understand their central values, range, and variation.

Numerical Summary Statistics

## Descriptive Statistics

The table below summarizes the key statistical measures for selected numerical variables in the hospital dataset.

| Variable | Mean | Median | Minimum | Maximum | Standard Deviation |
|----------|------|--------|---------|---------|-------------------|
| age | 50.21 | 50.00 | 0 | 120 | 18.91 |
| length_of_stay | 6.25 | 6.00 | 1 | 12 | 3.46 |
| treatment_cost | 149,222.57 | 146,100.00 | 10,000 | 300,000 | 80,747.51 |
| medicine_cost | 11,155.88 | 11,025.00 | 2,000 | 20,000 | 5,223.97 |
| test_cost | 15,380.09 | 15,125.00 | 1,000 | 30,000 | 8,551.51 |
| insurance_covered | 64,997.29 | 53,200.00 | 4,100 | 241,000 | 49,420.64 |
| patient_bill | 84,225.29 | 70,129.00 | 1,652 | 285,500 | 59,671.23 |
| satisfaction_score | 5.41 | 5.00 | 1 | 10 | 2.86 |

Interpretation

The average patient age was 50 years, indicating that most patients were middle-aged or older
adults. The average hospital stay was approximately 6 days. Financial variables showed
considerable variation, with an average treatment cost of ₹149,223 and an average patient bill of
₹84,225. Insurance coverage ranged from ₹4,100 to ₹241,000. The average satisfaction score was
5.41 out of 10, reflecting moderate patient satisfaction levels.

8.1.1 Distribution Analysis

The descriptive statistics were used to analyze the central tendency and variability of the numerical variables. The average patient age was approximately 50 years, and the average length of stay was about 6 days. The average treatment cost was ₹149,223, while the average patient bill was ₹84,225.
Insurance coverage varied considerably across patients, ranging from ₹4,100 to ₹241,000. The average satisfaction score was 5.41 out of 10, indicating moderate patient satisfaction levels. Cost-related variables showed higher variability than demographic variables, suggesting differences in treatment complexity and healthcare expenses across patients.

8.1.2 Group-by Average Analysis

The analysis compares average patient bills by department, average satisfaction scores by department, and average length of stay by hospital.

## Summary of Group-Based Analysis

The following analyses were performed to compare patient billing, satisfaction, and hospitalization duration across departments and hospitals.

| Analysis | Analysis Result | Interpretation |
|-----------|----------------|---------------|
| Average patient bill by department | Highest: Dermatology ₹90,433; Lowest: Pediatrics ₹80,329 | Treatment costs vary across departments, reflecting differences in healthcare services and resource utilization. |
| Average satisfaction score by department | Highest: Pediatrics 5.74; Lowest: Cardiology 5.21 | Patient satisfaction levels differ slightly among departments, indicating variations in patient experience. |
| Average length of stay by hospital | Highest: Apollo Hospital 6.59 days; Lowest: Manipal Hospital 5.91 days | Hospitalization duration varies across hospitals due to differences in patient conditions and treatment requirements. |


8.2 Categorical Analysis

The value_counts() function was used to analyse the distribution of records across different
categorical variables. The categorical columns analysed were department, hospital_name, city,
payment_method, and admission_type. This analysis helps identify the most frequently occurring
categories and understand patient distribution patterns within the dataset.

8.2.1 Most Common Categories

## Categorical Feature Analysis

The frequency distribution of key categorical variables was analyzed to identify dominant patterns in hospital operations and patient admissions.

| Analysis | Analysis Result | Interpretation |
|-----------|----------------|---------------|
| Department | Highest: ENT (341 records); Lowest: Gynaecology (208 records) | ENT recorded the highest patient volume, indicating greater demand for ENT-related services. |
| Hospital Name | Highest: Fortis Hospital (368 records); Lowest: KIMS Hospital (302 records) | Patient admissions were distributed across hospitals, with Fortis Hospital having the largest share of records. |
| City | Highest: Pune (356 records); Lowest: Hyderabad (238 records) | Pune contributed the highest number of patient records, indicating greater healthcare activity in the dataset. |
| Payment Method | Highest: UPI (575 records); Lowest: Debit Card (393 records) | Digital payment methods were widely used, with UPI being the most preferred mode of payment. |
| Admission Type | Highest: Regular (1,039 records); Emergency (1,024 records) | Both admission categories were nearly equally distributed, with regular admissions occurring slightly more frequently. |

8.2.2 Percentage Analysis

The percentage distribution of categorical variables was analysed using
value_counts(normalize=True) to understand the proportion of records across departments,
hospitals, cities, payment methods, and admission types.

Percentage Distribution Analysis

## Percentage Distribution Analysis

The percentage contribution of key categorical variables was calculated to identify the most dominant categories within the dataset.

| Analysis | Highest Percentage | Interpretation |
|----------|-------------------|---------------|
| Department | ENT (16.53%) | ENT accounted for the largest share of patient records among all departments. |
| Hospital Name | Fortis Hospital (17.84%) | Fortis Hospital represented the highest proportion of patient records. |
| City | Pune (17.26%) | Pune contributed the largest share of records among all cities. |
| Payment Method | UPI (27.87%) | UPI was the most preferred payment method among patients. |
| Admission Type | Regular (50.36%) | Regular admissions were slightly more frequent than emergency admissions. |

Interpretation

The analysis revealed that ENT (16.53%), Fortis Hospital (17.84%), and Pune (17.26%) had the
highest shares in their respective categories. UPI (27.87%) was the most commonly used payment
method, while Regular admissions (50.36%) slightly exceeded Emergency admissions (49.64%).

8.1.6 Correlation Analysis

Correlation analysis was performed to examine the relationships among hospital performance
indicators, treatment costs, billing amounts, insurance coverage, and patient satisfaction.

## Correlation Analysis

Correlation analysis was performed to understand the relationships between key financial, operational, and patient satisfaction variables.

| Variables | Correlation Coefficient | Interpretation |
|------------|------------------------|---------------|
| Treatment Cost vs Patient Bill | 0.79 | Strong positive correlation |
| Treatment Cost vs Insurance Covered | 0.68 | Moderate positive correlation |
| Insurance Covered vs Patient Bill | 0.09 | Very weak positive correlation |
| Length of Stay vs Satisfaction Score | -0.09 | Weak negative correlation |
| Treatment Cost vs Satisfaction Score | -0.06 | Very weak negative correlation |

Interpretation

Correlation analysis revealed that treatment_cost and patient_bill had the strongest positive
relationship (0.79), followed by treatment_cost and insurance_covered (0.68). Relationships
involving satisfaction_score were weak, indicating that patient satisfaction is not strongly affected
by treatment cost, insurance coverage, or length of stay.

9. Visualisation & Interpretation
    
The analysis uses various visualizations created using Matplotlib, Seaborn, and Plotly to explore
patterns within the Hospital Performance Dataset. Visual representations help simplify complex
healthcare data by highlighting trends, comparisons, distributions, and relationships that may not
be easily identified from raw data alone. The following charts and dashboards summarize key
findings related to patient demographics, treatment costs, hospital performance, billing patterns,
length of stay, and patient satisfaction.

9.1 Bar Chart – Average Patient Bill by Department

Analysis type: Univariate Comparative Analysis

The chart shows noticeable variation in average patient bills among departments. Paediatrics
recorded the highest average patient bill at approximately ₹110,000, followed by Orthopaedics and
Dermatology, with average bills close to ₹90,000. In contrast, Neurology recorded the lowest
average patient bill, at approximately ₹54,000.

    
9.2 Histogram – Age Distribution of Patients

Analysis type: Univariate Analysis

The histogram illustrates the distribution of patient ages within the dataset. Most patients fall
between 20 and 80 years of age, with a higher concentration of records in the middle-aged and
older age groups. Very few observations are present at the extreme age ranges. The distribution
aligns with the average age of approximately 50 years, indicating that hospital services in the
dataset are primarily utilized by adult and elderly patients.

9.3 Box Plot – Patient Bill Distribution by Department

Analysis type: Univariate Comparative Analysis

The box plot illustrates the distribution of patient bills across different hospital departments. It
highlights variations in billing patterns, median values, spread, and potential outliers. The chart
shows that billing amounts vary considerably among departments, with Dermatology,
Orthopaedics, and Paediatrics exhibiting higher billing ranges and several outlier observations.
The presence of outliers indicates that some patients incurred substantially higher costs, likely due
to specialized treatments or complex medical procedures. Overall, the visualization demonstrates
that patient billing is not uniform across departments and varies according to the nature of
healthcare services provided.

9.4 Scatter Plot – Length of Stay vs Satisfaction Score

Analysis type: Bivariate Analysis

The scatter plot illustrates the relationship between length of stay and patient satisfaction score.
The points are widely distributed across the chart with no clear upward or downward trend,
indicating a very weak relationship between the two variables. Patients with both short and long
hospital stays reported varying satisfaction levels. This observation is consistent with the
correlation analysis, which showed a weak negative correlation (-0.09) between length of stay and
satisfaction score. Therefore, patient satisfaction appears to be influenced more by service quality
and treatment experience than by the duration of hospitalization.

9.5 Correlation Heatmap – Hospital Performance Metrics

Analysis type: Multivariate Analysis

The correlation heatmap illustrates the relationships among numerical variables in the Hospital
Performance Dataset. The strongest positive correlation was observed between treatment_cost
and patient_bill (0.78), indicating that higher treatment costs generally result in higher patient
bills. A moderate positive relationship was also found between treatment_cost and
insurance_covered (0.66). Most other variables showed weak correlations, particularly those
involving satisfaction_score, suggesting that patient satisfaction is not strongly influenced by
financial factors alone. Overall, the heatmap helps identify key associations among hospital
performance indicators and highlights the primary factors affecting patient billing.

9.6 Interactive Dashboard – Average Patient Bill by Department

Analysis type: Interactive Comparative Analysis

An interactive dashboard was developed using Plotly to compare the average patient bill across
hospital departments. The visualization shows that Dermatology and Orthopaedics recorded the
highest average patient bills, while ENT and Pediatrics reported comparatively lower billing
amounts. The interactive format allows easier comparison of departmental costs and helps identify
areas with higher treatment expenses. This dashboard supports hospital administrators in
evaluating departmental financial performance and making informed decisions regarding cost
management and resource allocation.

9.7 Interactive Scatter Plot – Patient Bill vs Satisfaction Score

Analysis type: Interactive Bivariate Analysis

An interactive scatter plot was created using Plotly to examine the relationship between patient
bills and satisfaction scores across different hospital departments. Each point represents a patient
record, while bubble size indicates the length of stay. The points are widely dispersed throughout
the chart, showing no clear positive or negative trend between billing amounts and satisfaction
levels. Patients with both low and high medical expenses reported varying satisfaction scores,
suggesting that treatment cost alone does not determine patient satisfaction. This finding supports
the correlation analysis, which showed a very weak relationship between patient_bill and
satisfaction_score. The visualization highlights that factors such as service quality, treatment
outcomes, and hospital experience may have a greater influence on patient satisfaction than billing
amounts.


10. KEY FINDINGS AND INSIGHTS

• The ENT department recorded the highest patient volume.
• Fortis Hospital handled the largest number of patient admissions.
• Pune contributed the highest number of patient records.
• The most frequently used payment method was UPI
• Regular admission was the most common admission type
• Average patient age was approximately 50 years.
• Average hospital stay was approximately 6 days.
• Average treatment cost was approximately ₹149,223
• Average patient bill was approximately ₹84,225.
• Waiting time had a slight negative impact on patient satisfaction.

11. RECOMMENDATIONS

• Reduce patient waiting times to improve satisfaction.
• Strengthen doctor-patient communication.
• Improve hospital service quality and responsiveness.
• Monitor high-cost departments regularly.
• Optimize resource utilization and treatment costs.
• Expand insurance support programs.
• Implement periodic patient feedback mechanisms.
• Utilize data-driven decision-making for hospital management.

12. CONCLUSION
    
This project successfully analysed hospital performance data using Python-based analytical
techniques. The study involved data preprocessing, missing value treatment, outlier detection,
exploratory analysis, visualization, and dashboard development.
The findings indicate that treatment costs significantly affect patient billing, while patient
satisfaction is influenced more by overall service quality than by healthcare expenses. Insurance
plays a crucial role in reducing the financial burden on patients, and emergency admissions
represent a substantial portion of hospital activities.
The project demonstrates the importance of healthcare analytics in improving operational
efficiency, financial planning, and patient care quality. The generated insights can assist hospital
administrators in making informed decisions and enhancing overall hospital performance.
.
14. LIMITATIONS AND FUTURE SCOPE

Limitations

• The dataset is limited to available hospital records.
• Some missing values required statistical imputation.
• Analysis was restricted to historical data.
• External healthcare factors were not included.

Future Scope

• Patient readmission prediction using machine learning.
• Length of stay forecasting.
• Treatment cost prediction models.
• Patient satisfaction prediction.
• Real-time hospital monitoring dashboards.
• Advanced healthcare analytics using artificial intelligence.

16. REFERENCES
    
1. Pandas Documentation: https://pandas.pydata.org/
2. NumPy Documentation: https://numpy.org/
3. Matplotlib Documentation: https://matplotlib.org/
4. Seaborn Documentation: https://seaborn.pydata.org/
5. Plotly Documentation: https://plotly.com/python/
6. Python Documentation: https://docs.python.org/
7. Google Colab Documentation: https://colab.research.google.com/
