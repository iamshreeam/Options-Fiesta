# Options Fiesta 📈

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)

> **Options Fiesta** is an experimental cloud platform built for backtesting options strategies and valuing Black-Scholes Greeks. Developed as a mentored project under the **Finance and Analytics Club, IIT Kanpur** (May'25 - July'25).

## 🎯 Objective
To build an experimental cloud platform for backtesting options strategies and valuing Black-Scholes Greeks, serving as a comprehensive sandbox for evaluating derivatives risk, visualizing vol surfaces, and option payoffs.

## ✨ Key Features

- **Options Pricing & Greeks**: Real-time analytical pricing using the Black-Scholes model. Calculates core Greeks (Delta, Gamma, Vega, Theta, Rho).
- **Implied Volatility Surfaces**: Interactive 3D visualization of implied volatility surfaces across strikes and expiries using root-finding algorithms (Newton-Raphson).
- **Strategy Backtesting Engine**: A robust backtesting engine incorporating risk limits, position sizing (ATR, fixed fraction, Kelly), and execution models accounting for transaction costs and slippage.
- **Algorithmic Trading Signals**: Generates automated trading signals using primary technical indicators including SMA, EMA, Bollinger Bands, RSI, MACD, ATR, and VWAP.
- **Modern Web Interface**: A high-performance Django REST API backend coupled with an interactive React web UI for seamless data visualization.

## 🛠️ Tech Stack

- **Backend**: Django, Django REST Framework
- **Frontend**: React.js, Plotly/Chart.js
- **Database**: PostgreSQL (Metadata & Historical CSVs)
- **Task Queue**: Celery & Redis (for heavy backtesting computations)
- **Quantitative/Math**: NumPy, SciPy, Pandas

## 📊 Supported Option Strategies
The platform allows users to construct, visualize, and backtest various payoffs:
- Long Call / Long Put
- Covered Call & Protective Put
- Collars
- Straddles & Strangles
- Butterfly Spreads
- Ratio Spreads

## 🚀 Getting Started

> [!NOTE]
> Ensure you have Python 3.10+ and Node.js 18+ installed on your system before proceeding. Redis is also required for Celery task queuing.

### Backend Setup
```bash
# Clone the repository
git clone https://github.com/iamshreeam/Options-Fiesta.git
cd Options-Fiesta/backend

# Create virtual environment and install dependencies
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Run migrations and start server
python manage.py migrate
python manage.py runserver
