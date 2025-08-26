# MWAD-EX_03-To-Do-List-using-JavaScript
## Date:26-08-2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
### Index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h2>My To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Add a new task">
    <button onclick="addTask()">Add</button>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```
### Style.css
```
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #89f7fe, #66a6ff);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
}
.container {
  background: #fff;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  width: 360px;
}
h2 {
  text-align: center;
  margin-bottom: 20px;
  color: #333;
}
input {
  width: 70%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 8px;
}
button {
  padding: 10px;
  border: none;
  background: #4CAF50;
  color: white;
  cursor: pointer;
  border-radius: 8px;
  margin-left: 5px;
}
button:hover {
  background: #45a049;
}
ul {
  list-style: none;
  padding: 0;
  margin-top: 20px;
}
li {
  background: #f1f1f1;
  margin-bottom: 8px;
  padding: 10px;
  border-radius: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
li.done {
  text-decoration: line-through;
  color: gray;
}
.delete {
  background: red;
  color: white;
  padding: 5px 8px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 12px;
}
.delete:hover {
  background: darkred;
}
```
### Script.js
```
function addTask() {
  let input = document.getElementById("taskInput");
  let task = input.value.trim();
  if (task === "") return;
  
  let li = document.createElement("li");
  li.textContent = task;
  
  li.addEventListener("click", function () {
    li.classList.toggle("done");
  });

  let delBtn = document.createElement("span");
  delBtn.textContent = "X";
  delBtn.className = "delete";
  delBtn.onclick = function () {
    li.remove();
  };
  
  li.appendChild(delBtn);
  document.getElementById("taskList").appendChild(li);
  input.value = "";
}
```
## OUTPUT
<img width="1899" height="866" alt="image" src="https://github.com/user-attachments/assets/af40e99c-56ae-4c86-b488-f6e33c144668" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
