
# Patient Visits Analytics Dashboard 🏥

## 🔗 Problem Statement

In the healthcare sector, patient satisfaction and operational efficiency are critical metrics for evaluating service quality and patient retention. This dashboard provides insights into patient visits, wait times, satisfaction scores, and referral behaviors. It helps healthcare providers:

* Monitor patient satisfaction across age, race, and department.
* Understand peak patient visit periods (by time, day, and month).
* Analyze operational delays via average wait times.
* Track internal (staff) vs external patient schedules.

The insights from this dashboard guide hospital management in identifying service gaps, improving patient experience, and optimizing departmental workload distributions.

---

## 📂 Dataset Overview

The dataset used in this project contains key information about patient visits. Below are the core columns and their descriptions:

| Column Name               | Description                                                   |
| ------------------------- | ------------------------------------------------------------- |
| `Date`                    | Timestamp of the patient visit                                |
| `Patient ID`              | Unique identifier for each patient                            |
| `Gender`                  | Gender of the patient (M/F/Null)                              |
| `Age`                     | Age of the patient in years                                   |
| `Satisfaction Score`      | Numeric rating provided by the patient (1-10 scale)           |
| `First Name`, `Last Name` | Patient's names (merged into `Full Name` in Power Query)      |
| `Race`                    | Racial category of the patient                                |
| `Patient Admin Flag`      | Boolean indicating if the patient is a hospital staff         |
| `Wait Time`               | Time (in minutes) the patient waited before being attended to |
| `Department Referral`     | Department to which the patient was referred                  |

---

## ✏️ Data Cleaning and Transformation (Power Query)

* Merged `First Name` and `Last Name` into a single `Full Name` column.
* Extracted `Moment` (AM/PM) from the `Date` column to analyze time-of-day patterns.
* Handled missing/null values in key columns like `Satisfaction Score` and `Department Referral`.
* Adjusted column headers for clarity and consistency.
* Corrected data types for numerical and categorical columns.
* Created additional calculated columns:

  * `Week Type`: Classified each date as "Weekend" or "Weekday".
  * `Age Group`: Segmented patients into logical age bands:

    * Infancy (≤2)
    * Early Childhood (≤6)
    * Middle Childhood (≤12)
    * Teenager (≤18)
    * Adult (≥19)

---

## ⚖️ DAX Measures and KPIs

Custom measures were created to provide actionable insights. Some key measures include:

* **Total Patients**: Count of unique patient visits.
* **% Administrative Schedule**: Share of hospital staff among total patients.
* **% Non-Administrative Schedule**: Opposite of the above.
* **% Referred vs Non-Referred Patients**
* **Average Satisfaction Score**
* **% Patients Without Ratings**
* **Average Wait Time**
* **Gender Breakdown**: Share of Male, Female, and "Undisclosed" patients

---

## 🌎 Time Intelligence

A custom Date Table was created containing:

* `Date`
* `Year`
* `Month`
* `Weekday` (e.g., Mon, Tue)
* `Week Type` (Weekend or Weekday)

Relationships were established between the Date Table and main dataset to enable:

* Monthly/Yearly trends
* Weekday vs Weekend analysis
* Time-of-day filtering (AM/PM)

---

## 🎟️ Visualizations & Analysis

Each visual was designed for clarity, user interaction, and storytelling. Major visual insights include:

### 📅 General Overview (Card Visuals)

* Total Patients
* % Admin / Non-Admin Schedules
* % Referred / Non-Referred Patients
* Avg. Satisfaction Score
* Avg. Wait Time
* Gender Distribution

### 📊 Trend and Distribution Analysis

* **Patients by Month**: Area chart showing monthly visit trends
* **Patients by Department Referral**: Clustered bar chart
* **Patients by Age Group**: Clustered bar chart for age-based patterns
* **Patients by Week Type**: Comparison of weekday vs weekend visits
* **Patients by Year**: Line chart indicating annual visit volumes

### 🔄 Multi-Dimensional Heatmaps

* **Avg. Wait Time by Age Group and Race**
* **Avg. Satisfaction by Age Group and Race**
* A **slicer** enables toggling between the above metrics.
* Dynamic **note caption** updates with slicer selection to guide viewers.

### ⏰ Moment-Based Filtering

A global **slicer** filters reports based on time of visit (AM/PM), offering another layer of analytical depth.

---

## 🎨 Dashboard Design and Layout

To enhance usability and professionalism:

* A custom background layout was designed in PowerPoint with complementary color schemes, icons, and layout structure.
* The design was imported into Power BI to serve as a non-intrusive background for the visualizations.

---

## 📂 Project Files

* **Dataset**: \[To be uploaded]
* **Power BI Dashboard (.pbix)**: \[To be uploaded]
* **Live Interactive Dashboard Link**: \[(https://app.powerbi.com/links/Oy3j4lei79?ctid=9c6fd5d9-c228-4b22-be9c-89e96580edb1&pbi_source=linkShare)]

---

## 🚀 Final Thoughts

This dashboard offers a full-cycle analytical experience from raw data ingestion and cleaning to interactive storytelling through dynamic visuals. It serves as a foundational tool for healthcare providers looking to understand and enhance patient experience while maintaining operational efficiency.

> "Data is not just information, it's insight in waiting."

---

**Created with passion and precision ❤️ using Power BI**
