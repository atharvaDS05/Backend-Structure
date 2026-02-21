📈 Stock Trends Analysis Dashboard – Backend

This repository contains the backend services for the Stock Trends Analysis Dashboard — a web application that allows users to analyze and visualize stock market trends by simply selecting a stock ticker. The backend handles data retrieval from Yahoo Finance, computes technical indicators, applies labeling strategies, performs backtesting, and exposes APIs for ML evaluation and frontend integration.

🚀 Features

📥 Fetch historical stock data via Yahoo Finance

📊 Compute technical indicators (SMA, RSI, MACD, etc.)

🏷️ Apply labeling rules for trend detection

🔁 Backtest trading strategies using labeled data

🤖 Train and evaluate ML models

🔌 RESTful API endpoints for frontend consumption

✅ Modular structure for clean scalability and maintenance

🗂️ Project Structure
stock-trends-dashboard-backend/
├── app/
│   ├── main.py               # Entry point of the FastAPI app
│   ├── api/                  # API route definitions
│   ├── core/                 # Configuration management
│   ├── services/             # Business logic: data, indicators, labeling, ML
│   ├── schemas/              # Request and response models
│   └── utils/                # Utility functions (e.g., caching)
├── tests/                    # Unit and integration tests
├── .env.example              # Environment variable sample file
├── requirements.txt          # Python dependencies
└── README.md                 # Project overview
🧪 API Endpoints

Base URL: /api/v1

Endpoint	Method	Description
/health	GET	Health check
/tickers/{symbol}/indicators	GET	Returns computed technical indicators
/tickers/{symbol}/labels	GET	Returns labeled time series
/tickers/{symbol}/backtest	GET	Executes a backtest and returns results
/tickers/{symbol}/ml/results	GET	(Optional) Returns ML evaluation results

See app/api/routes.py for detailed implementation.

⚙️ Setup Instructions
Prerequisites

Python 3.9+

pip

Optional: virtualenv or venv for isolation

1. Clone the Repository
git clone https://github.com/yourusername/stock-trends-dashboard-backend.git
cd stock-trends-dashboard-backend
2. Create a Virtual Environment
python3 -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
3. Install Dependencies
pip install -r requirements.txt
4. Create .env File
cp .env.example .env

No secrets are required right now, but this file supports environment config for future extensibility.

▶️ Run the Server
uvicorn app.main:app --reload

The backend will be available at: http://localhost:8000

Visit http://localhost:8000/docs
 to explore Swagger UI and test endpoints interactively.

✅ Testing

To run unit tests:

pytest

Basic test coverage includes:

API health check

Service-level unit tests for indicator logic and backtesting

📌 Tech Stack

Framework: FastAPI (Python)

Data: Yahoo Finance (via yfinance)

Visualization: Frontend consumes backend APIs (handled separately)

Testing: Pytest

ML (optional): scikit-learn for baseline models

👥 Contributors

Atharva Sharma – Backend Design, ML Integration

Kuanysh Amandos  – Frontend & UI

Ulzhalgas Seidaliyeva– Documentation & QA

Haoqian Zhang – Dashboard/UI Developer and Data/Backend Developer

Mackenzie Kong-Sivert – QA and Documentation Support

📎 Related Repositories

Frontend Repository
 (to be connected)

