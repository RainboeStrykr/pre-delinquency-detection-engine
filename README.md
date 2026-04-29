# Pre-delinquency Detection Engine

A financial risk assessment system built for Barclays Hack-o-Hire 2026 that identifies customers at risk of delinquency before they default on payments. The system analyzes transaction patterns, account balances, and spending behaviors to predict potential financial distress.

**[Watch the demo](https://drive.google.com/file/d/1bOgeBC_13y27HGxIsx-Kxun4L-oJ0VEV/view?usp=drive_link)**

## Features

- **Real-time Risk Monitoring**: Tracks customer financial health through daily account analysis
- **Predictive Analytics**: Identifies early warning signs of potential delinquency
- **Customer Archetypes**: Classifies customers into risk categories:
  - STABLE_PRIME (Low risk, good savings)
  - LIQUIDITY_SHOCK (Sudden salary delay/loss)
  - OVERSPENDING (Gradual increase in discretionary spend)
  - SAVINGS_DEPLETION (Steady balance decline)
  - INCOME_INSTABILITY (Volatile income)
- **Interactive Dashboard**: Visualizes risk metrics and trends using Chart.js
- **Synthetic Data Generation**: Python script to generate realistic financial datasets

## Tech Stack

- **Frontend**: Next.js 16, React 19
- **Visualization**: Chart.js, react-chartjs-2
- **Data Generation**: Python (pandas, numpy, faker)
- **Styling**: CSS Modules

## Project Structure

```
├── app/                 # Next.js app directory
├── components/          # React components
├── data/                # JSON data files for the UI
├── lib/                 # Utility libraries
├── utils/               # Helper functions
├── generate_dataset.py  # Synthetic data generation script
├── customers.csv        # Customer profiles
├── daily_accounts.csv   # Daily account snapshots
└── transactions.csv     # Transaction records
```

## Getting Started

### Prerequisites

- Node.js 18+ 
- Python 3.8+ (for data generation)
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Generate synthetic data (optional - data files are included):
```bash
python generate_dataset.py
```

This will generate:
- `customers.csv` - 1,000 customer profiles with risk archetypes
- `daily_accounts.csv` - 180 days of daily account data
- `transactions.csv` - Transaction records with categories
- `data/customers_real.json` - UI-ready customer data
- `data/transactions_real.json` - UI-ready transaction data

### Running the Application

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the dashboard.

### Build for Production

```bash
npm run build
npm start
```

## Data Model

### Customer Attributes
- Customer ID
- Monthly salary
- EMI amount and due date
- Credit limit
- Baseline spending patterns
- Savings balance
- Risk score (0-100)
- Risk level (LOW/MEDIUM/HIGH)

### Risk Indicators
- Rolling 30-day balance trends
- EMI payment history
- Salary consistency
- Spending pattern drift
- ATM withdrawal frequency
- Macro shock susceptibility

## Hackathon Context

Built for Barclays Hack-o-Hire 2026, this project demonstrates:
- Financial data analysis
- Risk prediction algorithms
- Dashboard visualization
- Synthetic data simulation for testing

## Authors

- Abhiraj Bhowmick
- Ishaan Upponi
- Trisha Kumar
- Harini Sai
- Anniya Jenet Antony