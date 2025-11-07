# 🏥 FastAPI Patient Management API

A **FastAPI-based RESTful API** for managing patient records — including creating, viewing, updating, sorting, and deleting patients.
This project demonstrates **Pydantic models**, **path/query parameters**, **computed fields**, and **JSON-based persistence**.

---

## 🚀 Features

* Create new patient records with automatic BMI & verdict calculation
* View all patients or a specific one by ID
* Update existing patient information
* Delete patients by ID
* Sort patients by height, weight, or BMI
* Uses JSON file storage (no database setup required)

---

## 🧠 Tech Stack

* **FastAPI** — Web framework
* **Pydantic** — Data validation & schema generation
* **Uvicorn** — ASGI server
* **Python 3.10+**

---

## ⚙️ Setup & Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Malikabriq/fastapi-patient-api.git
cd fastapi-patient-api
```

### 2️⃣ Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate       # On Windows
source venv/bin/activate    # On macOS/Linux
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run the FastAPI app

```bash
uvicorn main:app --reload
```

### 5️⃣ Open in your browser

```
http://127.0.0.1:8000/docs
```

---

## 📋 Example Endpoints

| Method   | Endpoint                      | Description           |
| -------- | ----------------------------- | --------------------- |
| `GET`    | `/`                           | Root endpoint         |
| `GET`    | `/view`                       | View all patients     |
| `GET`    | `/patient/{id}`               | View a single patient |
| `POST`   | `/create`                     | Add a new patient     |
| `PUT`    | `/edit/{id}`                  | Update patient info   |
| `DELETE` | `/delete/{id}`                | Delete a patient      |
| `GET`    | `/sort?sort_by=bmi&order=asc` | Sort patients by BMI  |

---

## 🧩 Example Patient JSON

```json
{
  "id": "P001",
  "name": "John Doe",
  "city": "New York",
  "age": 32,
  "gender": "male",
  "height": 1.75,
  "weight": 70
}
```

---

## 🧾 License

This project is open-source under the **MIT License**.
Feel free to use and modify it for learning or personal projects.

---

💡 *Made with FastAPI by [Malik Abriq](https://github.com/Malikabriq)*
