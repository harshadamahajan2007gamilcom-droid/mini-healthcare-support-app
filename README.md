<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mini Healthcare Support App</title>

<style>
body{
font-family:Arial,sans-serif;
margin:0;
background:#f4f7fc;
}

header{
background:#0077cc;
color:white;
text-align:center;
padding:20px;
}

.container{
width:90%;
max-width:800px;
margin:auto;
padding:20px;
}

.card{
background:white;
padding:20px;
margin:20px 0;
border-radius:10px;
box-shadow:0 2px 8px rgba(0,0,0,0.1);
}

input,textarea{
width:100%;
padding:10px;
margin:8px 0;
border:1px solid #ccc;
border-radius:5px;
}

button{
background:#0077cc;
color:white;
border:none;
padding:10px 15px;
border-radius:5px;
cursor:pointer;
}

button:hover{
background:#005fa3;
}

#answer{
margin-top:10px;
font-weight:bold;
color:green;
}
</style>
</head>

<body>

<header>
<h1>Mini Healthcare Support Web App</h1>
<p>Patient Support & Volunteer Registration</p>
</header>

<div class="container">

<div class="card">
<h2>Patient Support Form</h2>

<input type="text" placeholder="Full Name">
<input type="email" placeholder="Email">
<input type="tel" placeholder="Phone Number">
<textarea placeholder="Describe your issue"></textarea>

<button>Submit Request</button>
</div>

<div class="card">
<h2>Volunteer Registration</h2>

<input type="text" placeholder="Volunteer Name">
<input type="email" placeholder="Email">
<input type="text" placeholder="Skills">
<input type="text" placeholder="Availability">

<button>Register</button>
</div>

<div class="card">
<h2>AI FAQ Assistant</h2>

<input type="text" id="question" placeholder="Ask a question">
<button onclick="chatbot()">Ask</button>

<p id="answer"></p>
</div>

</div>

<script>
function chatbot(){

let q=document.getElementById("question").value.toLowerCase();
let ans="Please contact support team.";

if(q.includes("appointment")){
ans="Appointments can be booked online or by calling support.";
}
else if(q.includes("timing")){
ans="Hospital timings are 9 AM to 6 PM.";
}
else if(q.includes("emergency")){
ans="Emergency Helpline Number: 108";
}
else if(q.includes("volunteer")){
ans="Fill the volunteer registration form above.";
}

document.getElementById("answer").innerText=ans;
}
</script>

</body>
</html>
