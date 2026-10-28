# FSD
Lab Stuff
1.
a) Create a Web Page using HTML which contains a Heading, Image and 2 hyperlinks. Each hyperlink opens a new page in the same web browser. New page contains “Go Back” link that takes you to the main page.  
Index.html
<html>
<head>
 <title>Main Page</title>
</head>
<center>
<body>
 <h1>Welcome to the Website</h1>
 <img src="C:\Projects\fsd labb\1.a\butterfly.jfif" alt="Image" width="400" height="300">
<br>
 <a href="page1.html" target="_blank">Open page1</a>
<br>
 <a href="page2.html" target="_blank">Open page2</a>
</body>
</html>

Page1.html
<html>
<head>
 <title>Page1</title>
</head>
<center>
<body>
 <h2>This is page1</h2>
 <a href="index.html">Go back to Mainpage</a>
</body>
</html>

Page2.html
<html>
<head>
 <title>Page2</title>
</head>
<center>
<body>
 <h3>This is page2</h3>
 <a href="index.html">Go back to Mainpage</a>
</body>
</html>

OUTPUT:






b) Write a HTML program to create a Registration form, which contains User Name, Password, Date of Birth, Gender, Mail-id, Contact number, Address and submit button.
Reg.html
<html>
<head>
 <title>Registration Form</title>
 <link rel="stylesheet" href="style.css">
</head>
<center>
<body>
 <h2>Register here</h2>
 <form>
  <label for="username">Username</label>
  <input type="text">
  <br>
  <label for="password">Password</label>
  <input type="password">
  <br>
  <label for="dob">Date of Birth</label>
  <input type="date">
  <br>
  <label for="gender">Gender</label>
  <input type="radio" value="male">
  <label for="male">male</label>
  <input type="radio" value="female">
  <label for="female">female</label>
  <br>
  <label for="email">Email Id</label>
  <input type="email">
  <br>
  <label for="contact">Contact Number</label>
  <input type=tel">
  <br>
  <label for="address">Address</label>
  <textarea rows=4></textarea>
  <br>
  <button type="submit">Register</button>
 </form>
</body>
</html>

Style.css
body {
    background-color: lavender;
}
h2 {
    color: purple;
}

OUTPUT:

2.
a) Create a web page to demonstrate Position Property in CSS.

Pos.html
<html>
<head>
<link rel="stylesheet" href="stylepos.css">
</head>
<body>
<div class="fixed">
<h2>Position property</h2></div>
<div class="static">
This ele is positioned static.</div>
<div class="relative">
this is relatively positioned
</div>
<div class="parent">
 this is parent element
<div class="absolute">
this is absolute element
</div>
</div>
</body>	
</html>

Stylepos.css
div.static{
position:static;
border:3px solid yellow;
width:300px;height:50px;
padding:15px;
}
div.relative{
position:relative;
left:20px;
border:3px solid red;
width:250px;
padding:15px;
}
div.fixed{
position:fixed;
top:0;
right:0;
border:3px solid blue;
}
div.parent{
position:relative;
right:30px;
border:3px solid green;
padding:15px;
height:120px;
}
div.absolute{
position:absolute;
top:15px;
right:15px;
border:3px solid orange;
padding:10px;
background-color:lightpink;
}

OUTPUT:
b) Create a Newspaper Style Design to print minimum 2 articles using HTML and CSS.

Newsart.html
<!DOCTYPE html>
<html>
<head>
    <title>The Daily Chronicle</title>
    <link rel="stylesheet" href="style1.css">
</head>

<body>
<div class="newspaper">
    <header>
        <h1>THE DAILY CHRONICLE</h1>
        <p>Weather: Sunny | Late Edition</p>
    </header>
    <hr>
    <main>
        <section>
            <h2>MARS ROVER DISCOVERS WATER</h2>
            <p class="subhead">Scientists discover water beneath Mars.</p>
            <p class="byline">By Jane Doe</p>
            <img src="marsland.webp" alt="Mars">
            <p>Scientists discovered a large underground water reservoir on Mars. This discovery may help us understand the possibility of life on the red planet.</p>
        </section>
        <section>
            <h2>GLOBAL TECH SUMMIT DISCUSSES AI</h2>
            <p class="subhead">World leaders discuss AI safety.</p>
            <p class="byline">By John Smith</p>
            <img src="technology.jpg" alt="Technology">
            <p>Leaders from many countries discussed artificial intelligence safety rules. Experts believe AI regulations can reduce risks while supporting innovation.</p>
        </section>
    </main>
</div>
</body>
</html>



Style.css

body {
    background-color: beige;
    font-family: Georgia, serif;
    margin: 20px;
}
.newspaper {
    background-color: white;
    max-width: 1000px;
    margin: auto;
    padding: 20px;
}
header {
    text-align: center;
}
h1 {
    font-size: 40px;
}
main {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}
h2 {
    font-family: Arial, sans-serif;
}
.subhead {
    font-style: italic;
}
.byline {
    font-weight: bold;
}
img {
    width: 100%;
    filter: grayscale(100%);
}

p {
    line-height: 1.5;
    text-align: justify;
}OUTPUT:


3.
a) Write a JavaScript program to change the background color after clicking “change color” button.
Bkgrdcol.html
<html>
<head>
<title> Week3</title>
<style>
.relative{position:relative;
top:300px;
width:300px;}
</style>
</head>
<center><body style="background-color:beige;">
<h1> First JavaScript </h1>
<div class="relative"><button type="button" onclick="cFunction()">Change background color to orange</button></div>
<script>
function cFunction(){
    document.body.style.backgroundColor="orange";
}
</script>
</body>
</html>

OUTPUT:


b) Write a JavaScript program to validate registration page using regular expression.
Form.html	

<html>
<head>
    <title>Form Validation</title>
</head>
<body>
    <h2>Registration Form</h2>
    <form id="reg-form">
        <input type="text" id="name" placeholder="Enter name" required>
        <br><br>
        <input type="email" id="email" placeholder="Enter email" required>
        <br><br>
        <input type="password" id="password" placeholder="Enter password" required>
        <br><br>
        <button type="submit">Submit</button>
    </form>
    <script>
        document.getElementById("reg-form").addEventListener("submit", function(e) {
            e.preventDefault();
            let name = document.getElementById("name").value;
            let email = document.getElementById("email").value;
            let password = document.getElementById("password").value;
            let nameRegex = /^[a-zA-Z0-9]{3,10}$/;
            let emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;
            let passwordRegex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[!@#$%^&*])[a-zA-Z\d!@#$%^&*]{8,}$/;
            if (!nameRegex.test(name)) {
                alert("Invalid name!");
            }
            else if (!emailRegex.test(email)) {
                alert("Invalid email!");
            }
            else if (!passwordRegex.test(password)) {
                alert("Password must have 8 characters, uppercase, lowercase, number and symbol!");
            }
            else {
                alert("Registration successful!");
            }
        });
    </script>
</body>
</html>
OUTPUT:




4.
a) Write a code to hide and show an element in a periodic interval without any action from the user using JQuery.
Hideandshow.html
<!DOCTYPE html>
<html>
<head> <title>Hide and Show</title>
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<style>
.box{
    width:300px;
    height:300px;
    border:10px solid yellow;
    background-color:green;
}
</style>
</head>
<body>
<div class="box" id="element"></div>
<script>
$(document).ready(function(){
    var isVisible =true;
    setInterval(function(){
        if(isVisible){
            $('#element').hide();
            isVisible=false;
        }else{
        $('#element').show();
        isVisible=true;
        }       
    },2000);
});
</script>
</body>
</html>





OUTPUT:



b) Write a program to create and Build a star rating system using JQuery.
Star.html
<!DOCTYPE html>
<html>
<head>
 <title> Star Rating System </title>
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<style>
.star{
  font-size:30px;
  cursor: pointer;
}
div{
    width:300px;
    border:5px solid gold;
    padding:30px;
    background-color:lightgreen;
    margin:20px;
}
.select{
 color:gold;
}
</style>
</head>
<center>
<body>
<div>
<script>
$(document).ready(function(){
  $(".star").click(function(){
     let cvalue=$(this).data("value");
     $(".display").text("Your rating is "+cvalue);
     $(".star").each(function(){
     if($(this).data("value")<=cvalue){
         $(this).addClass("select");
     }
     else{
        $(this).removeClass("select");
     }
  });
  });
});
</script>
<center>
  <h1> Rating </h1>
  <span class="star" data-value="1">&#9733;</span>
  <span class="star" data-value="2">&#9733;</span>
  <span class="star" data-value="3">&#9733;</span>
  <span class="star" data-value="4">&#9733;</span>
  <span class="star" data-value="5">&#9733;</span>  
  <br><br>
  <p class="display"></p>
<center>
</div>
</body>
</html>

OUTPUT:






5.
a) Write a program to demonstrate ReactJS Class and Instance.
App.js
import React from "react";
class Ex extends React.Component {
  render() {
    return <h1>{this.props.name}</h1>;
  }
}
function App() {
  return (
    <div>
      <center>
        <Ex name="This is FSD Lab Week 5 1st Question" />
      </center>
    </div>
  );
}
export default App;

OUTPUT:



















b) Write a program to create a basic calculator to perform arithmetic operations using ReactJS.
Calci.js
import React, { useState } from "react";

function Calculate() {
    const [a, setA] = useState("");
    const [op, setOp] = useState("");
    const [b, setB] = useState("");
    const [result, setResult] = useState("");

    function calculate() {
        if (op === "+")
            setResult(Number(a) + Number(b));
        else if (op === "-")
            setResult(Number(a) - Number(b));
        else if (op === "*")
            setResult(Number(a) * Number(b));
        else if (op === "/")
            setResult(Number(a) / Number(b));
        else
            setResult("Invalid operator");
    }

    return (
        <div>
            <h1>Basic Calculator</h1>

            <input
                placeholder="First number"
                value={a}
                onChange={(e) => setA(e.target.value)}
            />

            <input
                placeholder="Operator (+, -, *, /)"
                value={op}
                onChange={(e) => setOp(e.target.value)}
            />

            <input
                placeholder="Second number"
                value={b}
                onChange={(e) => setB(e.target.value)}
            />

            <button onClick={calculate}>Calculate</button>

            <h2>Result: {result}</h2>
        </div>
    );
}

export default Calculate;
OUTPUT:

























6.
a) Demonstrate simple event handling examples using ReactJS.
import React,{useState} from 'react';
import './App.css';
function App() {
  const[num,setNum]=useState(0);
  function Event(event){ setNum(event.target.value); }
  function Display(){ alert("The entered number is "+num); }
  return (
    <>
    <h1> Event Handling </h1>
    <label>Enter a number: </label>
    <input type="number" onChange={Event}/>
    <br/><br/>
    <button onClick={Display}> submit </button>
    </>
  );
}
export default App;

OUTPUT:

efore Event:

After Event:


b) Write a program to create a simple voting application system using ReactJS.
import React,{useState} from 'react';
import './App.css';
function App(){
  const [p1,setP1]=useState(0);
  const [p2,setP2]=useState(0);
  return(
      <div>
        <h1> VOTING SYSTEM </h1>
         <label>BRS:</label>
         <button onClick={()=>{setP1(p1+1)}}>VOTE</button>
         <br/><br/>
         <label>BJP:</label>
         <button onClick={()=>{setP2(p2+1)}}>VOTE</button>
         <h2>Total Number of votes for BRS : {p1}</h2>
         <h2>Total Number of votes for BJP : {p2}</h2>
      </div>
  );
}
export default App;

OUTPUT:
Before Event:

After Event:

7.
a) Create a webpage to display “Hello World” using SERVLET.
index.html
import java.io.*;
import jakarta.servlet.*;
import jakarta.servlet.http.*;
import jakarta.servlet.annotation.WebServlet;

@WebServlet("/hello")
public class HelloServlet extends HttpServlet {
    public void doGet(HttpServletRequest req,
                      HttpServletResponse res)
                      throws IOException {

        res.setContentType("text/html");

        PrintWriter out = res.getWriter();

        out.println("<html>");
        out.println("<body>");
        out.println("<h1>Hello World</h1>");
        out.println("</body>");
        out.println("</html>");
    }
}
OUTPUT:

b) Implement a web application using SERVLET, which takes a name as input and on submitting it, shows a hello page. It shows start time at the right top comer of the page and provides a logout button. On clicking logout button, it should show a logout page with Thank You message with the duration of usage (hint: Use session to store name and time).
WelcomeServlet.java:
import java.util.*;
import java.io.*;
import jakarta.servlet.*;
import jakarta.servlet.http.*;
import jakarta.servlet.annotation.WebServlet;

@WebServlet("/welcome")
public class WelcomeServlet extends HttpServlet {
    public void doGet(HttpServletRequest req, HttpServletResponse res) throws IOException{
        res.setContentType("text/html");
        PrintWriter out=res.getWriter();
        out.println("<html><body>");
        out.println("<h2>Enter your Name</h2>");
        out.println("<form action='welcome' method='post'>");
        out.println("Name: <input type='text' name='name' required>");
        out.println("<input type='submit' value='submit'>");
        out.println("</form>");
        out.println("</body></html>");
    }
    public void doPost(HttpServletRequest req,HttpServletResponse res) throws IOException{
       
        String name=req.getParameter("name");
        HttpSession session=req.getSession();
        session.setAttribute("name", name);
        session.setAttribute("startTime", System.currentTimeMillis());
         res.setContentType("text/html");
        PrintWriter out=res.getWriter();
        out.println("<html><body>");
        out.println("<p style='text-align:right'>Start Time:"+new Date((Long)session.getAttribute("startTime"))+"</p>");
        out.println("<h1>Hello "+name+"</h1>");
        out.println("<form action='logout' method='post'>");
        out.println("<input type='submit' value='Logout'>");
        out.println("</form>");
        out.println("</body></html>");
    }
}
LogoutServlet.java:
import java.util.*;
import java.io.*;
import jakarta.servlet.*;
import jakarta.servlet.http.*;
import jakarta.servlet.annotation.WebServlet;
@WebServlet("/logout")
public class LogoutServlet extends HttpServlet {
    public void doPost(HttpServletRequest req,HttpServletResponse res) throws IOException{
        res.setContentType("text/html");
        PrintWriter out=res.getWriter();
        HttpSession session=req.getSession(false);
        out.println("<html><body>");
        if(session!=null && session.getAttribute("name")!=null){
            String name=(String) session.getAttribute("name");
            long start=(Long) session.getAttribute("startTime");
            long end=System.currentTimeMillis();
            long duration=(end-start)/1000;
            out.println("<h1>Thank you "+name+"</h1>");
            out.println("<p>Duration of usage: "+duration+"seconds</p>");
            session.invalidate();
        }else{
            out.println("Session already logged out");
        }
        out.println("</body></html>");
    }
}
OUTPUT:

8.
a) Write a JSP program to find a factorial of the given number.

index.jsp
<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
    <title>Factorial Program</title>
</head>
<body>
    <h2>Factorial of a Number</h2>

    <form action="factorial.jsp" method="post">
        Enter a Number:
        <input type="number" name="number"
               min="0" required>
        <input type="submit" value="Find Factorial">
    </form>
</body>
</html>

Factorial.jsp
<%@page import="java.math.BigInteger"%>
<%@page contentType="text/html" pageEncoding="UTF-8"%>

<html>
<body>
<%
    String value = request.getParameter("number");

    try {
        int n = Integer.parseInt(value);

        if (n < 0) {
%>
            <h3>Please enter a non-negative number.</h3>
<%
        } else {
            BigInteger factorial = BigInteger.ONE;

            for (int i = 1; i <= n; i++) {
                factorial = factorial.multiply(
                    BigInteger.valueOf(i));
            }
%>
            <h2>Factorial Result</h2>
            <h3><%= n %>! = <%= factorial %></h3>
<%
        }
    } catch (Exception e) {
%>
        <h3>Invalid Input</h3>
<%
    }
%>

<a href="index.jsp">Calculate Another Factorial</a>
</body>
</html>

OUTPUT:





b) Create a user validation web application using JSP, where the user submits the login name and password to the server. The name and password are checked against the data already available in database and if the data matches, a successful login page is returned. Otherwise show a failure message to the user.

Index.jsp
<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
    <head>
        <title>User Login</title>
    </head>
    <body>
        <div class="login-box">
            <h2>User Login</h2>
            <form action="validate.jsp" method="post">
                Username:
                <input type="text" name="username" required>
                <br>
                Password:
                <input type="password" name="password" required>
                <br><br>
                <input type="submit" value="Login" class="loginButton">
            </form>
        </div>
    </body>
</html>

Validate.jsp
<%@page import="java.sql.*"%>
<%@page contentType="text/html" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
    <head>
        <title>Login Validation</title>
        <style>
            body {
                font-family: Arial;
                text-align: center;
                margin-top: 120px;
            }
            .success {
                color: green;
            }
            .error {
                color: red;
            }
        </style>
    </head>
    <body>
        <%
            String username = request.getParameter("username");
            String password = request.getParameter("password");
            Connection con = null;
            PreparedStatement ps = null;
            ResultSet rs = null;
            try {
                // Load MySQL JDBC driver
                Class.forName("com.mysql.jdbc.Driver");
                // Establish database connection
                con = DriverManager.getConnection(
                        "jdbc:mysql://localhost:3306/webappdb", "root", "");
                // SQL query
                String sql = "SELECT * FROM users "
                           + "WHERE username=? "
                           + "AND password=?";
                // Create PreparedStatement
                ps = con.prepareStatement(sql);
                // Set username and password
                ps.setString(1, username);
                ps.setString(2, password);
                // Execute query
                rs = ps.executeQuery();
                if (rs.next()) {
                    // Store user in session
                    session.setAttribute("username", username);
        %>
                    <h2 class="success">Login Successful</h2>
                    <h3>Welcome <%= username %></h3>
                    <br>
                    <a href="logout.jsp">Logout</a>
        <%
                } else {
        %>
                    <h2 class="error">Login Failed</h2>
                    <h3>Invalid Username or Password</h3>
                    <br>
                    <a href="login.jsp">Try Again</a>
        <%
                }
            } catch (Exception e) {
        %>
                <h3 class="error">Database Error</h3>
                <p><%= e.getMessage() %></p>
        <%
            } finally {
                try {
                    if (rs != null)
                        rs.close();
                    if (ps != null)
                        ps.close();
                    if (con != null)
                        con.close();
                } catch (Exception e) {
                    // Ignore closing error
                }
            }
        %>
    </body>
</html>

Logout.jsp
<%@page contentType="text/html" pageEncoding="UTF-8"%>
<%
    String username = (String) session.getAttribute("username");
    session.invalidate();
%>
<!DOCTYPE html>
<html>
    <head>
        <title>Logout</title>
    </head>
    <body>
        <div style="text-align:center; margin-top:120px; font-family:Arial;">
            <h2>Thank You <%= username != null ? username : "User" %></h2>
            <h3>You have successfully logged out.</h3>
            <a href="login.jsp">Login Again</a>
        </div>
    </body>
</html>
OUTPUT:





9.
a) Demonstrate a simple example of Spring web MVC framework.
WelcomeController.java
package com.example.springmvc;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
@Controller
public class WelcomeController {
    @GetMapping("/")
    public String home() {
        return "index";
    }
    @GetMapping("/welcome")
    public String welcome(
            @RequestParam("name") String name,
            Model model) {
        model.addAttribute("studentName", name);
        return "welcome";
    }
}

index.html
<!DOCTYPE html>
<html>
    <head>
        <title>Spring MVC Example</title>
    </head>
    <body>
        <h2>Welcome to Spring MVC</h2>

        <form action="/welcome" method="get">
            Enter Student Name:
            <input type="text" name="name" required>
            <button type="submit">Submit</button>
        </form>
    </body>
</html>

welcome.html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
    <head>
        <title>Welcome Page</title>
    </head>
    <body>
        <h2>Spring MVC Application</h2>
        <h3 th:text="'Welcome, ' + ${studentName}">
            Welcome
        </h3>
        <a href="/">Back to Home</a>
    </body>
</html>

OUTPUT:
