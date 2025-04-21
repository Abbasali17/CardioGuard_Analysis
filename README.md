# CardioGuard Post-Launch Analysis: Patient Journey & HCP Segmentation

## Project Overview

This project simulates a real-world pharmaceutical analytics scenario focused on analyzing the post-launch performance of a fictional cardiovascular drug, "CardioGuard". Using synthetic patient-level prescription data, the analysis delves into patient treatment pathways (Lines of Therapy, Persistency, Compliance) and identifies distinct Healthcare Provider (HCP) prescribing segments to inform strategic decision-making for the drug's second year on the market.

This repository contains the Python code (in Jupyter Notebooks), synthetic data, generated figures, and a summary report for the analysis.

## Business Scenario

PharmaCo launched CardioGuard 12 months ago. Initial uptake patterns are crucial for refining marketing, sales, and patient support strategies. This analysis utilizes prescription data spanning approximately 2.5 years (including pre-launch competitor data and 12 months post-CardioGuard launch) to provide data-driven insights.

## Objectives

*   Identify and profile the cohort of patients initiating CardioGuard.
*   Determine CardioGuard's typical placement within the patient's Line of Therapy (LoT).
*   Measure patient persistency (duration) on CardioGuard therapy using survival analysis.
*   Assess patient compliance (adherence) via Medication Possession Ratio (MPR).
*   Segment Healthcare Providers (HCPs) based on their post-launch prescribing behaviors.
*   Identify key HCP segments for targeted sales and marketing engagement.

## Skills Demonstrated

This project directly addresses requirements often found in pharmaceutical/healthcare analytics roles, specifically showcasing experience in:

*   **HCP & Patient Level Data Analytics:** The entire project revolves around analyzing granular prescription data linked to unique patients and prescribers.
*   **HCP Segmentation & Targeting:** Calculated HCP-specific metrics (volume, share, adoption speed), applied K-Means clustering to identify distinct behavioral segments, profiled segments, and derived actionable targeting recommendations (Notebook: `04_HCP_Segmentation_Targeting.ipynb`, Report Section 5.2).
*   **Patient Cohorts:** Identified and analyzed the "CardioGuard Initiators" cohort (Notebook: `03_Patient_Journey_Analysis.ipynb`, Report Section 5.1.1).
*   **Lines of Therapy (LoT):** Implemented logic to determine if CardioGuard was used as 1st Line or 2nd Line+ based on prior prescription history (Notebook: `03_Patient_Journey_Analysis.ipynb`, Report Section 5.1.2).
*   **Persistency Analysis:** Calculated time-on-therapy using Kaplan-Meier survival analysis, accounting for censoring (Notebook: `03_Patient_Journey_Analysis.ipynb`, Report Section 5.1.3).
*   **Compliance Analysis:** Calculated Medication Possession Ratio (MPR) over a defined period (Notebook: `03_Patient_Journey_Analysis.ipynb`, Report Section 5.1.4).
*   **Data Processing & Feature Engineering:** Demonstrated proficiency in data cleaning, merging (Pandas), and creating relevant analytical features (e.g., `prescription_end_date`, `is_new_to_drug`, `days_since_launch`).
*   **Data Visualization:** Utilized Matplotlib and Seaborn to create informative charts (demographics, LoT distribution, K-M curve, MPR histogram, Elbow plot, segment scatter plot).
*   **Reporting & Interpretation:** Summarized complex analytical findings into actionable business insights and recommendations (Report: `CardioGuard_Analysis_Report.md`).

## Technology Stack

*   **Language:** Python (3.x)
*   **Libraries:**
    *   `pandas`: Data manipulation and analysis.
    *   `numpy`: Numerical operations.
    *   `matplotlib` & `seaborn`: Data visualization.
    *   `scikit-learn`: K-Means clustering, data scaling (`StandardScaler`).
    *   `lifelines`: Kaplan-Meier survival analysis (Persistency).
    *   `Faker`: Synthetic data generation.
    *   `os`: Operating system interactions (directory creation).
*   **Environment:** Jupyter Notebooks / Google Colab

## Data Description

The project utilizes three synthetic CSV files located in the `data/` directory:

*   `patients.csv`: Contains unique patient identifiers and basic demographic information (age group, gender, partial zip).
*   `hcps.csv`: Contains unique HCP identifiers and their specialty/partial zip.
*   `prescriptions.csv`: The core transactional data, linking patients, HCPs, drugs, prescription dates, and days supply.



## Setup and Usage

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/YourUsername/CardioGuard-Analysis-Portfolio.git
    cd CardioGuard-Analysis-Portfolio
    ```
2.  **Create a Virtual Environment (Recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Notebooks:** Open and run the Jupyter Notebook
   *  HCP&Patient_analysis.ipynb

    

## Key Findings & Visualizations

The analysis yielded several key insights, detailed in the `reports/CardioGuard_Analysis_Report.md` file. Highlights include:

1.  **Dominant 2L+ Usage:** CardioGuard is primarily used after other therapies (95.5%).
2.  **Early Persistency Challenge:** Median time on therapy is ~4.3 months (131 days), indicating a need for early support.
3.  **Suboptimal Compliance:** Average MPR is low (~60%), suggesting significant adherence gaps.
4.  **Actionable HCP Segments:** Four distinct HCP segments were identified, with "High Vol / Low Adopt" (Segment B) representing the largest growth opportunity.

Key visualizations illustrating these findings (e.g., LoT distribution, Kaplan-Meier curve, MPR histogram, HCP segment scatter plot) can be found in the `figures/` directory.

## Actionable Recommendations

Based on the analysis, key recommendations for PharmaCo include:

1.  **Refine Messaging:** Focus communication on CardioGuard's benefits in the 2L+ setting.
2.  **Targeted HCP Engagement:** Prioritize resources on the "High Vol / Low Adopt" segment for growth and implement retention strategies for "High Vol / High Adopt" champions.
3.  **Enhance Patient Support:** Develop programs to address early persistency drops and improve overall compliance (MPR).



## Limitations

*   The analysis uses synthetic data.
*   The Line of Therapy calculation is simplified.
*   MPR measures possession, not actual consumption.
*   The analysis represents a snapshot in time.

## Contact

Abbas Ali - p.abbasali5@gmail.com

Project Link: (https://github.com/Abbasali17/CardioGuard-Analysis)

## License

Distributed under the MIT License. See `LICENSE` file for more information (Optional - create a LICENSE file if desired).
