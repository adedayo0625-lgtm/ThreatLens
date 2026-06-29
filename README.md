# ThreatLens 🔍

Passive visitor intelligence dashboard. Every request to the public page logs the visitor's **IP address**, **device type**, and **browser** — visible in a sleek admin panel.

## Features

- Captures IP, device name, browser, path, and timestamp for every visitor
- Clean dark-theme admin dashboard with live stats
- Auto-refreshes every 15 seconds
- One-click log clearing
- Login-protected admin panel

## Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/threatlens.git
cd threatlens

# 2. Create & activate a virtual environment
python3 -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run
python app.py
```

Open `http://localhost:5000` in your browser.  
Admin panel: `http://localhost:5000/admin`  
Default credentials: `admin` / `admin123`

## Environment Variables

| Variable         | Default    | Description              |
|------------------|------------|--------------------------|
| `SECRET_KEY`     | (insecure) | Flask session secret     |
| `ADMIN_USERNAME` | `admin`    | Admin login username     |
| `ADMIN_PASSWORD` | `admin123` | Admin login password     |

**Always set these in production.**

```bash
export SECRET_KEY="your-random-secret"
export ADMIN_USERNAME="yourname"
export ADMIN_PASSWORD="strongpassword"
python app.py
```

## Project Structure

```
threatlens/
├── app.py               # Flask application
├── requirements.txt
├── static/
│   ├── css/style.css
│   └── js/main.js
└── templates/
    ├── base.html
    ├── index.html       # Public landing page
    ├── login.html       # Admin login
    └── admin.html       # Admin dashboard
```

## ⚠️ Note

Visitor data is stored **in memory** and resets when the server restarts. For persistent storage, swap the `visitors` list for a database (SQLite, PostgreSQL, etc.).
# ThreatLens
