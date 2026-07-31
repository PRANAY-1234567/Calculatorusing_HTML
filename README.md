# 🧮 Flask Calculator with Firebase Realtime Database

A simple yet powerful **Calculator Web Application** built using **Flask**, **HTML**, and **Firebase Realtime Database**. The application performs basic arithmetic operations and stores every successful calculation in Firebase for future reference.

This project is ideal for beginners learning Flask web development, form handling, and Firebase integration.

---

# 🚀 Features

* ➕ Addition
* ➖ Subtraction
* ✖️ Multiplication
* ➗ Division
* 📥 User-friendly web interface
* 🔥 Firebase Realtime Database integration
* 💾 Stores calculation history
* ⚠️ Handles division by zero
* 🌐 Flask-based web application

---

# 🛠️ Technologies Used

## Backend

* Python
* Flask

## Frontend

* HTML5
* CSS3 *(Optional for styling)*

## Database

* Firebase Realtime Database

## Firebase SDK

* Firebase Admin SDK

---

# 📂 Project Structure

```text
Flask-Calculator/
│
├── app.py
├── templates/
│   └── index.html
│
├── static/
│   ├── style.css
│
├── firebase-adminsdk.json
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/flask-calculator-firebase.git

cd flask-calculator-firebase
```

---

## 2️⃣ Create a Virtual Environment (Optional)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install flask firebase-admin
```

or

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Configure Firebase

1. Create a project in **Firebase Console**.
2. Enable **Realtime Database**.
3. Generate a **Firebase Admin SDK** private key.
4. Download the JSON credentials file.
5. Update the credential path inside `app.py`.

Example:

```python
cred = credentials.Certificate("path/to/firebase-adminsdk.json")
```

Also update the database URL:

```python
firebase_admin.initialize_app(cred, {
    "databaseURL": "https://your-project-id-default-rtdb.firebaseio.com/"
})
```

---

# ▶️ Running the Application

Start the Flask development server:

```bash
python app.py
```

Open your browser and visit:

```text
http://127.0.0.1:5000
```

---

# 💻 Supported Operations

| Operation      | Symbol |
| -------------- | ------ |
| Addition       | +      |
| Subtraction    | -      |
| Multiplication | ×      |
| Division       | ÷      |

---

# 🔥 Firebase Data Structure

Each successful calculation is stored under the **calculations** node.

Example:

```json
{
  "calculations": {
    "-NzAbc123": {
      "operation": "10 + 20 = 30",
      "result": 30
    },
    "-NzAbc456": {
      "operation": "15 * 5 = 75",
      "result": 75
    }
  }
}
```

---

# 📋 Sample Output

### Input

```text
First Number : 25

Second Number : 5

Operation : Division
```

### Output

```text
Result : 5.0
```

Stored in Firebase:

```text
25 / 5 = 5.0
```

---

# 🧠 How It Works

1. User enters two numbers.
2. User selects an arithmetic operation.
3. Flask receives the form data using a POST request.
4. The selected calculation is performed.
5. The result is displayed on the webpage.
6. Successful calculations are pushed to Firebase Realtime Database.
7. Division by zero returns an error without storing data.

---

# 🎯 Learning Outcomes

This project helps you learn:

* Flask Routing
* HTML Form Handling
* POST Requests
* Jinja2 Templates
* Firebase Realtime Database
* Firebase Admin SDK
* CRUD Operations
* Python Conditional Statements
* Web Application Development

---

# 🔮 Future Improvements

* 🕒 Display calculation history
* 🗑️ Delete previous calculations
* 📊 Scientific calculator functions
* 🌙 Dark mode
* 📱 Responsive mobile interface
* 🧾 User authentication with Firebase Authentication
* 📈 Calculation analytics dashboard
* 💾 Export history as PDF or CSV

---

# 👨‍💻 Author

**Pranay Jadhao**

Electronics & Telecommunication Engineer

Aspiring Software Engineer | Python | Flask | Firebase | SQL | Data Analytics

**GitHub:** https://github.com/your-username

**LinkedIn:** https://linkedin.com/in/your-profile

---

# 📄 License

This project is licensed under the **MIT License**.

Feel free to use, modify, and contribute for educational and learning purposes.

---

⭐ If you found this project useful, consider giving it a **Star** on GitHub!

![image](https://github.com/user-attachments/assets/c9288e3b-801a-4c33-b167-df3767a21480)
