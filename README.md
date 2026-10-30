• Introduction
The Student Result Management System is a web-based application developed using
HTML, CSS, and JavaScript. It is designed to simplify the process of managing and
calculating student results. In traditional methods, result calculation is done manually,
which can be time-consuming and prone to errors.
This system allows users to enter student details and marks, and it automatically
calculates the total marks, average, grade, and result (pass/fail). The results are
displayed instantly in a tabular format, making it easy to understand and manage.
The main aim of this project is to demonstrate the use of basic web technologies to
create an interactive and user-friendly application. It helps in improving efficiency,
accuracy, and speed in handling student result data.
• Title:
Student Result Management System
• Abstract
The Student Result Management System is a web-based application developed using
HTML, CSS, and JavaScript. It is designed to manage student academic results
efficiently. The system allows users to input student details and marks, automatically
calculates total and average marks, and assigns grades. This reduces manual effort and
minimizes calculation errors.
• Objectives
• To develop a simple and efficient result management system
• To automate the calculation of total and average marks
• To generate grades based on student performance
• To reduce human errors in result processing
• To provide a user-friendly interface
• Features
• Input student name and marks
• Automatic total and average calculation
• Grade generation based on marks
• Display results in tabular format
• Simple and interactive interface
• Technologies Used
• HTML – for structuring the webpage
• CSS – for designing and styling
• JavaScript – for logic, calculations, and interactivity
• System Design
The system is designed as a simple web application. The user enters student details
through input fields. JavaScript processes the data, calculates total, average, and grade,
and displays the result dynamically in a table on the same webpage.
• Database
This project does not use a database. All data is stored temporarily during execution
using JavaScript variables. Once the page is refreshed, the data is lost.
• PROJECT CODE
<!DOCTYPE html>
<html>
<head>
 <title>Student Result Management System</title>
 <style>
 body {
 font-family: Arial;
 background: #f4f4f4;
 text-align: center;
 }
 .container {
 width: 500px;
 margin: 30px auto;
 background: white;
 padding: 20px;
 border-radius: 10px;
 box-shadow: 0 0 10px gray;
 }
 input {
 width: 90%;
 padding: 8px;
 margin: 5px;
 }
 button {
 padding: 10px;
 margin: 10px;
 cursor: pointer;
 }
 table {
 width: 100%;
 margin-top: 20px;
 border-collapse: collapse;
 }
 th, td {
 border: 1px solid black;
 padding: 8px;
 }
 th {
 background: #ddd;
 }
 </style>
</head>
<body>
<div class="container">
 <h2>Student Result Management System</h2>
 <input type="text" id="name" placeholder="Student Name"><br>
 <input type="number" id="m1" placeholder="Marks 1"><br>
 <input type="number" id="m2" placeholder="Marks 2"><br>
 <input type="number" id="m3" placeholder="Marks 3"><br>
 <button onclick="addResult()">Add Result</button>
 <table id="resultTable">
 <tr>
 <th>Name</th>
 <th>Total</th>
 <th>Average</th>
 <th>Grade</th>
 <th>Result</th>
 <th>Action</th>
 </tr>
 </table>
</div>
<script>
function addResult() {
 let name = document.getElementById("name").value;
 let m1 = Number(document.getElementById("m1").value);
 let m2 = Number(document.getElementById("m2").value);
 let m3 = Number(document.getElementById("m3").value);
 if(name === "" || m1 === 0 || m2 === 0 || m3 === 0) {
 alert("Please enter all details");
 return;
 }
 let total = m1 + m2 + m3;
 let avg = total / 3;
 let grade = "";
 let result = "";
 if(avg >= 80) grade = "A";
 else if(avg >= 60) grade = "B";
 else if(avg >= 40) grade = "C";
 else grade = "F";
 result = avg >= 40 ? "Pass" : "Fail";
 let table = document.getElementById("resultTable");
 let row = table.insertRow();
 row.insertCell(0).innerHTML = name;
 row.insertCell(1).innerHTML = total;
 row.insertCell(2).innerHTML = avg.toFixed(2);
 row.insertCell(3).innerHTML = grade;
 row.insertCell(4).innerHTML = result;
 row.insertCell(5).innerHTML = "<button onclick='deleteRow(this)'>Delete</button>";
 document.getElementById("name").value = "";
 document.getElementById("m1").value = "";
 document.getElementById("m2").value = "";
 document.getElementById("m3").value = "";
}
function deleteRow(btn) {
 btn.parentElement.parentElement.remove();
}
</script>
</body>
</html>
• Output Screens
Step 1: Opening the Web Page
• When you open the HTML file, the page loads.
• You see:
o Title: Student Result Management System
o Input fields (Name, Marks 1, Marks 2, Marks 3)
o “Add Result” button
o Empty table (only headings visible)
Step 2: Entering Data
• You enter:
o Name → Rohit
o Marks → (example: 76, 87, 78)
Step 3: Clicking “Add Result”
• When you click the button:
o JavaScript function addResult() is called
• System checks:
o If name or marks are empty → shows alert
• Since all fields are filled → program continues
• Total = m1 + m2 + m3
→ 76+ 87 + 78 = 241
• Average = Total / 3
→ 241 / 3 = 80.33
• Based on average:
o ≥ 80 → Grade A
o ≥ 60 → B
o ≥ 40 → C
o < 40 → F
Here average = 80.33 → Grade A
• If average ≥ 40 → Pass
• Otherwise → Fail
80.33 → Pass
• After adding result:
o All input fields become empty
o Ready for next entry
Delete Button
• When you click Delete:
o That row is removed from the table
• Advantages
• Easy to use and understand
• Saves time in result calculation
• Reduces manual errors
• No need for complex software
• Lightweight and fast
• Limitations
• No permanent data storage
• Limited functionality
• Not suitable for large-scale use
• No user authentication system
• Future Scope
• Integration with database (MySQL, Firebase)
• Add login and authentication system
• Generate downloadable/printable reports
• Improve user interface with advanced design
• Add more subjects and student records
• Conclusion
The Student Result Management System is a simple and effective solution for managing
student results. It demonstrates the use of basic web technologies and helps in
understanding how data can be processed and displayed dynamically. It can be further
enhanced into a full-scale application with additional features.
