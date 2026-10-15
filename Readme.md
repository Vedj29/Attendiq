# AttendIQ — Student Attendance Risk Management Dashboard

AttendIQ is a front-end demonstration dashboard that explores student attendance patterns and illustrates how machine-learning models can classify attendance-related risk. It includes an attendance overview, a student directory, and an interactive risk predictor.

> **Important:** This project uses fictional, synthetic student records. Predictions and evaluation scores are for academic demonstration only and must not be used to make real decisions about students.

## Features

- **Attendance Dashboard:** Summary metrics, attendance charts, risk distribution, and students needing attention.
- **Student Directory:** Search by student name or ID, filter by academic year and risk level, sort by attendance, and export records to CSV.
- **Risk Predictor:** Enter student indicators to view the predicted risk category, risk score, and an interpretable Decision Tree rule path.
- **Machine Learning:** Demonstrates Decision Tree and Random Forest classification implemented in JavaScript.
- **Year-wise Analysis:** Explore Second Year (SE), Third Year (TE), and Fourth Year (BE) AI & Data Science records.
- **Interactive Controls:** Simulate class attendance, reset demo data, and view high-risk alerts.
- **Responsive Design:** Sidebar navigation and layouts designed for desktop and smaller screens.

## Dataset

The dashboard contains **180 fictional student records**:

- 60 Second Year (SE) students
- 60 Third Year (TE) students
- 60 Fourth Year (BE) students

### Dataset attributes

| Attribute | Description |
|---|---|
| Student_ID | Synthetic student identifier |
| Student_Name | Fictional student name |
| Department | Academic department |
| Year | Academic year |
| Classes_Conducted | Total classes conducted |
| Classes_Attended | Total classes attended |
| Attendance_Percentage | Student attendance percentage |
| Previous_Term_Attendance_Percentage | Previous-term attendance |
| Consecutive_Absences | Number of consecutive absences |
| Assignment_Completion_Percentage | Assignment completion percentage |
| Internal_Marks_Percentage | Internal assessment marks |
| Risk_Status | Synthetic label used for model training |

Attendance percentage is calculated as:

`(Classes_Attended / Classes_Conducted) × 100`

The risk labels are synthetic demonstration labels, not verified outcomes for real students.

## Machine Learning Approach

AttendIQ demonstrates two classification algorithms:

### 1. Random Forest
An ensemble learning algorithm that combines predictions from multiple decision trees. Its output is used as the primary risk prediction in the dashboard.

### 2. Decision Tree
A tree-based classifier that provides a simpler, interpretable rule path for understanding a prediction.

Both models use five indicators:

1. Attendance percentage
2. Consecutive absences
3. Assignment completion percentage
4. Previous-term attendance percentage
5. Internal marks percentage

The code includes a stratified hold-out evaluation split and calculates accuracy for both models. Since the dataset and labels are synthetic, these results do not establish real-world predictive effectiveness.

## Technology Stack

- HTML5
- CSS3
- JavaScript
- [Chart.js 4.4.1](https://www.chartjs.org/) for data visualization

Chart.js is loaded through a CDN, so an internet connection is required for the charts unless the library is hosted locally.

## How to Run the Project

AttendIQ is a standalone HTML application. It does not require Python, Node.js, a database, or package installation.

1. Download or clone the repository.
2. Keep `attendiq_rf_dt_dashboard.html` in your project folder.
3. Open the HTML file in a modern browser such as Google Chrome, Microsoft Edge, or Firefox.
4. Use the sidebar to navigate between Dashboard, Students, and Risk Predictor.

### Hosting on GitHub Pages

1. Upload the HTML file to your GitHub repository.
2. Rename it to `index.html` if you want it to open as the repository's default page.
3. Enable GitHub Pages in the repository settings.
4. Open the published website link.

## How to Use

1. Open **Dashboard** to view attendance summaries, charts, and high-risk records.
2. Use the year filter to focus on SE, TE, or BE students.
3. Open **Students** to search, filter, sort, and export student records.
4. Open **Risk Predictor**, adjust the student indicators, and select **Predict risk**.
5. Use the class-recording and simulation controls to explore attendance changes.
6. Reset the demo data to restore the initial fictional records.

## Limitations and Responsible Use

- All student names and records are fictional.
- Risk labels are synthetic and do not represent actual academic outcomes.
- Accuracy on synthetic labels does not establish real-world predictive performance.
- The application does not connect to a college attendance system or live student database.
- Predictions should not replace faculty judgment, student discussions, or institutional policies.
- Do not enter personally identifiable or confidential student information into a public demonstration.

## Future Improvements

- Integrate an authorized attendance database with appropriate privacy and access controls.
- Evaluate models using representative, appropriately authorized real-world data.
- Add class-wise precision, recall, F1-score, and stronger validation.
- Add automated tests for filtering, prediction, and attendance updates.
- Introduce role-based access and audit logs before considering deployment.

## Project Status

**Academic prototype / demonstration project.** Not intended for production use.

## License

No license is currently specified. Add a license file if you want to define how others may use, modify, or distribute the project.
