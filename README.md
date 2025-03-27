# 🔍 AML Detection System using LangGraph

A sophisticated Anti-Money Laundering (AML) detection system built using the LangGraph framework. This tool leverages graph-based analysis to identify suspicious financial patterns and potential money laundering activities.

## 🏗️ System Architecture

![AML Detection System Architecture](https://github.com/subrata-samanta/Langgraph_AML_Detection/blob/main/graph.png)

The system implements a state-based graph workflow with these key components:

- 📊 **State Management**: [`AMLState`](aml.py) class handling transaction data and analysis results
- 🎯 **Risk Assessment Nodes**:
  - 📄 Document Analysis
  - 🌍 Geographic Risk Assessment
  - 👤 Behavioral Analysis
  - 💰 Crypto Risk Analysis
  - ⚠️ Sanctions Screening
  - 👔 PEP Screening
- 🔄 **Decision Routing**: Smart paths based on risk levels and transaction types

## ✨ Features

### 🔑 Core Functionality
- 📈 Graph-based transaction analysis workflow
- ⚡ Real-time risk scoring and assessment
- 🎯 Multi-factor AML detection:
  - 🌎 Geographic risk assessment
  - 🔍 Behavioral pattern analysis
  - 📝 Document verification
  - 🪙 Cryptocurrency monitoring
  - 👥 PEP screening
  - 🚫 Sanctions checking

### 🚀 Advanced Capabilities
- 📑 Automated SAR generation
- 🔍 Enhanced due diligence workflows
- 🎯 Risk-based routing
- 📄 Document analysis using LLM
- ⚙️ Configurable risk thresholds

## 🛠️ Setup

1. Install dependencies:
```sh
pip install langgraph langchain-groq
```

2. Set environment variables:
```sh
export GROQ_API_KEY=your_api_key_here
```

3. Prepare data:
- Add `sample_cases.json` to root directory
- Match provided test case format

## 💻 Usage

```python

from aml_langgraph import run_analysis

# Sample transaction
transaction = {
    "amount": 9500,
    "origin_country": "US",
    "destination_country": "CA",
    "parties": ["retail_chain_inc"],
    "timestamp": "2025-03-27T19:20:16.639571"
}

# Sample customer data
customer = {
    "name": "James Smith",
    "account_age_days": 120,
    "transaction_history": []
}

# Run analysis
run_analysis(transaction, customer)
```

## ⚙️ Configuration

Customize risk parameters:
- 🌍 High-risk countries
- 💰 Tax haven jurisdictions
- ⚠️ Sanctioned entities
- 🕸️ Darknet identifiers
- 📊 Risk scoring weights

Edit in the [configuration section](aml.py).

## 📊 Output

Generated analysis includes:
- 📈 Risk scores (0-100)
- 🔄 Decision path visualization
- ⚠️ Triggered alerts
- 🤖 LLM analysis results
- 📝 SAR status
- 👥 Review requirements

## 🤝 Contributing

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Submit Pull Request

## 📄 License

MIT License
