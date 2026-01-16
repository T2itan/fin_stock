CS50 Finance
A web-based tool that allows users to manage a virtual portfolio of stocks. Users can check real-time stock quotes, buy and sell shares using virtual currency, and track their transaction history.

## Features
User Authentication: Secure registration and login system.

Real-time Quotes: Fetches current stock prices using the IEX Cloud API.

Virtual Trading: Users start with $10,000.00 of virtual cash to build their portfolio.

Portfolio Management: A dynamic homepage that displays current holdings, share counts, current prices, and total net worth.

Transaction History: A detailed log of every buy and sell action, including timestamps and prices.

## Tech Stack
Backend: Python with the Flask web framework.

Database: SQL (via SQLite) to store user data, portfolios, and histories.

Frontend: HTML5, CSS3, and Bootstrap for responsive design.

API: IEX Cloud for financial data.

## Project Structure
Plaintext
finance/
├── app.py           # Main application logic and routes
├── helpers.py       # Helper functions (login requirements, lookup, usd formatting)
├── static/          # CSS and favicon files
├── templates/       # Jinja2 HTML templates (layout, login, index, etc.)
└── finance.db       # SQLite database
## Getting Started
1. Prerequisites

Ensure you have Python 3 and pip installed. You will also need an API key from IEX Cloud.

2. Installation

Clone the repository and install the dependencies:

Bash
pip install -r requirements.txt
3. Set Environment Variables

Export your API key and the Flask app name:

Bash
export API_KEY=your_public_api_key
export FLASK_APP=app.py
4. Run the Application

Bash
flask run
The app will be available at http://127.0.0.1:5000/.

## Database Schema
The application utilizes a relational database to track users and their activity.

Users Table: Stores usernames and hashed passwords (using generate_password_hash).

Transactions Table: Tracks user_id, symbol, shares, price, and timestamp.

## Acknowledgments
CS50 Staff: For the distribution code and the helpers.py utilities.

IEX Cloud: For providing the financial data API.
