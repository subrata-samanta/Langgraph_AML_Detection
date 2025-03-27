# Langgraph_AML_Detection
A Python-based Anti-Money Laundering (AML) detection system built using LangGraph framework. This tool leverages graph-based analysis to identify suspicious financial patterns and potential money laundering activities. Features graph-based transaction analysis and pattern detection for enhanced AML compliance.


# AML Detection System using LangGraph

A sophisticated Anti-Money Laundering (AML) detection system built using the LangGraph framework. This system employs graph-based analysis and LLM-powered detection to identify suspicious financial patterns and potential money laundering activities.

## Features

### Core Functionality
- Graph-based transaction analysis workflow
- Real-time risk scoring and assessment
- Multi-factor AML detection including:
  - Geographic risk assessment
  - Behavioral pattern analysis
  - Document verification
  - Cryptocurrency transaction monitoring
  - PEP (Politically Exposed Person) screening
  - Sanctions list checking

### Advanced Capabilities
- Automated SAR (Suspicious Activity Report) generation
- Enhanced due diligence workflows
- Risk-based routing and decisioning
- Document analysis using LLM
- Configurable risk thresholds

## System Architecture

![AML Detection System Architecture](https://github.com/subrata-samanta/Langgraph_AML_Detection/blob/main/graph.png)

The system uses a state-based graph workflow with the following key components:

- **State Management**: [`AMLState`](aml.py) class handling transaction data and analysis results
- **Risk Assessment Nodes**:
  - Document Analysis
  - Geographic Risk Assessment
  - Behavioral Analysis
  - Crypto Risk Analysis
  - Sanctions Screening
  - PEP Screening
- **Decision Routing**: Conditional paths based on risk levels and transaction types

## Setup

1. Install required dependencies:
```sh
pip install langgraph langchain-groq
```

2. Configure environment variables:
```sh
export GROQ_API_KEY=your_api_key_here
```

3. Prepare sample data:
- Ensure `sample_cases.json` is present in the root directory
- Format should match the provided test cases

## Usage

```python
from aml import run_analysis

# Example transaction
transaction = {
    "amount": 9500,
    "origin_country": "US",
    "destination_country": "CA",
    "parties": ["retail_chain_inc"],
    "timestamp": "2025-03-27T19:20:16.639571"
}

# Example customer data
customer = {
    "name": "James Smith",
    "account_age_days": 120,
    "transaction_history": []
}

# Run analysis
run_analysis(transaction, customer)
```

## Configuration

The system includes configurable risk parameters:

- High-risk countries
- Tax haven jurisdictions
- Sanctioned entities list
- Darknet market identifiers
- Risk scoring weights

These can be modified in the [configuration section](aml.py) of the code.

## Output

The system generates detailed analysis reports including:
- Risk scores (0-100)
- Decision path visualization
- Triggered alerts
- LLM analysis findings
- SAR generation status
- Human review requirements

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is open-source and available under the MIT License.
