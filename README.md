# 🌍 European Weather API with Flask

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-Web%20API-black?style=for-the-badge&logo=flask)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-purple?style=for-the-badge&logo=pandas)
![REST API](https://img.shields.io/badge/REST-API-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

A Flask-based Weather API that gathers historical temperature data from weather stations across Europe and returns temperature information through REST API endpoints.

This project uses:

- **Flask** for the backend API
- **Pandas** for data processing
- Local weather station datasets stored in TXT files

---

# 🚀 Features

✅ REST API with Flask  
✅ Historical weather data retrieval  
✅ Temperature lookup by station and date  
✅ Retrieve all data for a station  
✅ Retrieve yearly station data  
✅ JSON API responses  
✅ Data processing with Pandas  

---

# 📂 Project Structure

```bash
project-folder/
│
├── app.py
├── templates/
│   └── home.html
│
├── data_small/
│   ├── stations.txt
│   ├── TG_STAID000001.txt
│   ├── TG_STAID000002.txt
│   └── ...
│
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/weather-api.git
cd weather-api
```

---

## 2️⃣ Create Virtual Environment (Optional)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install flask pandas
```

---

# ▶️ Run the Application

```bash
python app.py
```

The API will start at:

```bash
http://127.0.0.1:5000/
```

---

# 🌐 API Overview

The Weather API gathers station and date information from Europe and returns a response with the temperature.

---

# 🔌 API Endpoints

---

## 🔹 Temperature for One Station on One Date

### URL Format

```http
http://127.0.0.1:5000/api/v1/station/date
```

### Example

```http
http://127.0.0.1:5000/api/v1/10/1988-10-25
```

### Sample Response

```json
{
  "station": "10",
  "date": "1988-10-25",
  "temperature": 11.2
}
```

---

## 🔹 All Data for One Station

### Example

```http
http://127.0.0.1:5000/api/v1/10
```

Returns all available weather records for the selected station.

---

## 🔹 One Station for One Specific Year

### Example

```http
http://127.0.0.1:5000/api/v1/yearly/10/1985
```

Returns all weather records for the specified year.

---

# 🧠 How It Works

The application:

1. Reads weather station datasets
2. Loads station files dynamically
3. Processes data using Pandas
4. Converts records into JSON responses
5. Serves API endpoints with Flask

Example from the project:

```python
temperature = df.loc[df["    DATE"] == date]['   TG'].squeeze() / 10
```

Temperature values are divided by 10 to convert them into Celsius.

---

# 📊 Data Flow

```text
Weather TXT Files
        ↓
      Pandas
        ↓
    Flask API
        ↓
   JSON Response
```

---

# 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Flask | REST API framework |
| Pandas | Data manipulation |
| HTML | Template rendering |

---

# 📌 Available Routes

| Route | Description |
|---|---|
| `/` | Home page |
| `/api/v1/10/1988-10-25` | Temperature for a specific date |
| `/api/v1/10` | All data for a station |
| `/api/v1/yearly/10/1985` | Yearly weather data |

---

# 🔥 Future Improvements

- Add Swagger/OpenAPI documentation
- Deploy to Render or Heroku
- Add charts and weather visualizations
- Add error handling for invalid stations
- Add frontend dashboard
- Add search functionality

---

# 🐛 Known Limitations

- No authentication
- Local dataset required
- No pagination for large responses
- Limited error handling

---

# 👩‍💻 Author

Developed by :contentReference[oaicite:0]{index=0}

---

# ⭐ Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 💡 Learning Outcomes

This project demonstrates:

- Flask routing
- REST API development
- Dynamic URL parameters
- Data manipulation with Pandas
- JSON response handling
- Backend web development fundamentals

---

# 🌟 Support

If you like this project, give it a ⭐ on GitHub!

   

