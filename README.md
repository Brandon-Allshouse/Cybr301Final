# CYBR 301 Final Project

A secure paper submission portal built with Flask and MySQL. This web application allows users to register, log in, and submit academic papers in PDF or DOCX format with support for co-authors. Designed with user authentication, CSRF protection, and file upload handling.

## 🔧 Technologies Used

- Python 3
- Flask
- Flask-WTF (CSRF Protection)
- Flask-Bcrypt (Password Hashing)
- Flask-SQLAlchemy (ORM)
- MySQL (Database)
- HTML (Frontend)
- WTForms
- Bootstrap (for styling)
- Werkzeug (for secure file uploads)

---

## 📂 Features

- User registration and login with encrypted passwords
- CSRF-protected forms
- Secure file uploads (`.pdf`, `.docx`)
- Submission dashboard showing submission count
- Co-author and abstract support per paper
- Limit of 2 paper submissions per user

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Brandon-Allshouse/Cybr301Final.git
cd Cybr301Final
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up MySQL Database

Make sure you have a MySQL server running. Create a database and user:

```sql
CREATE DATABASE users_db;
CREATE USER 'abc'@'localhost' IDENTIFIED BY 'abc123';
GRANT ALL PRIVILEGES ON users_db.* TO 'abc'@'localhost';
FLUSH PRIVILEGES;
```

Update the connection string in `main.py` if needed:

```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql+pymysql://abc:abc123@localhost/users_db'
```

### 5. Run the App

```bash
python main.py
```

Visit `http://127.0.0.1:5000` in your browser.

---

## 📁 File Structure

```
Cybr301Final/
│
├── templates/             # HTML templates (index, login, register, dashboard)
├── uploads/               # Uploaded paper files (created automatically)
├── requirements.txt       # Python dependencies
├── main.py                # Main Flask application
├── README.md              # Project documentation (you’re here!)
```

---

## 🔐 Security Notes

- Passwords are hashed with bcrypt.
- CSRF protection is enforced on all forms.
- Uploaded files are validated and saved with safe filenames.

---

## 📄 License

This project was built for educational purposes as part of the CYBR 301 course.

---

## 🙋‍♂️ Author

Brandon Allshouse  
[GitHub Profile](https://github.com/Brandon-Allshouse)
