task 1 a
from flask import Flask, render_template, request, redirect, session, url_for
from flask import Flask, render_template

app = Flask(_name_)

@app.route('/login')
def login():
    return render_template("login.html")

from werkzeug.security import generate_password_hash, check_password_hash
import sqlite3

app = Flask(_name_)
app.secret_key = 'your_secret_key_here'  # Change this for production

# Database Setup
def init_db():
    with sqlite3.connect("users.db") as conn:
        c = conn.cursor()
        c.execute('''CREATE TABLE IF NOT EXISTS users (
task1 b
<!DOCTYPE html>
<html>
<head>
    <title>Login</title>
</head>
<body>
    <h2>Login</h2>
    {% if error %}
        <p style="color:red;">{{ error }}</p>
    {% endif %}
    <form method="POST">
        Username: <input type="text" name="username" required><br><br>
        Password: <input type="password" name="password" required><br><br>
        <input type="submit" value="Login">
    </form>
    <br>
    <a href="/register">New user? Register here</a>
</body>
</html>
