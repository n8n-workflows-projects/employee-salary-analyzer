# 👨‍💼 Employee Salary Analyzer using n8n

This is a beginner-friendly n8n workflow that analyzes employee salary data stored in Google Sheets.

The workflow automatically checks each employee's salary and separates them into **Senior Employees** and **Junior Employees**. It then generates a salary summary and sends the report to HR through Gmail.

This project helped me practice conditional logic, data processing, Google Sheets integration, and email automation in n8n.

---

# 📌 What this workflow does

- Reads employee data from Google Sheets.
- Checks whether the employee's salary is greater than **₹50,000**.
- Saves senior employees into a separate Google Sheet.
- Saves junior employees into another Google Sheet.
- Calculates:
  - Total senior employees
  - Total salary
  - Average salary
  - Highest salary
- Sends the summary report to HR using Gmail.

---

# 🛠 Workflow

```text
Schedule Trigger
        │
        ▼
Update Google Sheet
        │
        ▼
Read Employee Data
        │
        ▼
IF (Salary > ₹50,000)
      /          \
     /            \
Senior          Junior
     │              │
     ▼              ▼
Save to         Save to
Senior Sheet    Junior Sheet
     │
     ▼
Summarize
     │
     ▼
Send Email to HR
```

---

# 🧩 Nodes Used

- Schedule Trigger
- Google Sheets
- IF
- Summarize
- Gmail

---

# 📊 Salary Rule

- Salary **greater than ₹50,000** → Senior Employee
- Salary **₹50,000 or below** → Junior Employee

---

# 📈 Summary Generated

The workflow creates a simple report containing:

- Total Senior Employees
- Total Salary
- Average Salary
- Highest Salary

---

# 📧 Email Report

After the workflow finishes, an email is automatically sent to HR with the salary summary.

Example:

```text
Employee Salary Report

Total Senior Employees : 31

Total Salary : ₹22,38,000

Average Salary : ₹72,193

Highest Salary : ₹98,000
```

---

# 🎯 What I Learned

While building this workflow, I learned how to:

- Read data from Google Sheets
- Use the IF node for decision making
- Separate data into different sheets
- Generate reports using the Summarize node
- Send automated emails using Gmail
- Build a complete automation workflow in n8n

---

# 💻 Technologies Used

- n8n
- Google Sheets
- Gmail

---

# 📂 Files

```
📁 Employee Salary Analyzer
 ├── workflow.json
 ├── README.md
 ├── images
 │    ├── workflow.png
 │    └── output.png
 └── sample-data
```

---

# 🚀 Future Improvements

Some ideas I would like to add later:

- Department-wise salary report
- Monthly salary analytics
- PDF report generation
- Slack notification for HR
- Dashboard with salary charts

---

# 📸 Workflow Preview

> Add your workflow screenshot here.

Example:

## Workflow design
![image alt]()

## workflow resource
![image alt]()

## workflow output
![image alt](https://github.com/n8n-workflows-projects/employee-salary-analyzer/blob/1d8a1e38787bb3b8829012c680a738f9b82763c9/Screenshot%202026-07-11%20113138.png)

![image alt]()


---

# 🙌 About This Project

I created this project as part of my n8n learning journey to understand how workflow automation can simplify HR tasks. It is a beginner-level project and helped me gain hands-on experience with Google Sheets, conditional logic, reporting, and email automation.
