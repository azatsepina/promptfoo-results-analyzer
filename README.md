# Promptfoo Results Analyzer

A Python-based analysis tool for evaluating and visualizing [Promptfoo](https://promptfoo.dev) evaluation results. This tool helps you analyze LLM prompt testing results, identify patterns, and generate comprehensive reports.

![Promptfoo Analysis Dashboard](Promptfoo_results_images/dashboard_screenshot.png)

## Prerequisites

### Python Installation

1. Download Python 3.8 or later from [python.org](https://python.org)
2. During installation on Windows:
   - ✅ Check "Add Python to PATH"
   - ✅ Check "Install pip"
3. Verify installation by opening a terminal/command prompt:
   ```bash
   python --version
   pip --version
   ```

### Promptfoo Installation

1. Install Node.js from [nodejs.org](https://nodejs.org)
2. Install Promptfoo globally:
   ```bash
   npm install -g promptfoo
   ```
3. Verify installation:
   ```bash
   promptfoo --version
   ```

## Project Setup

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd promptfoo-results-analyzer
   ```

2. Create and activate a virtual environment:
   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # macOS/Linux
   python -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run Streamlit Dashboard:
    ```bash
    streamlit run streamlit_analyzer.py
    ```
    This will open the interactive dashboard in your default browser where you can:
    - Upload and analyze Promptfoo results files
    - View key metrics like success rates and costs
    - Compare model performances
    - Visualize cost vs. success rate relationships

## Using Promptfoo

### Running Evaluations

1. Create a promptfoo configuration file (`promptfooconfig.yaml`):
   ```yaml
   prompts: prompts.txt
   providers: 
     - openai:gpt-3.5-turbo
     - openai:gpt-4
   tests: tests.yaml
   ```

2. Run the evaluation:
   ```bash
   promptfoo eval
   ```

3. View results in the browser:
   ```bash
   promptfoo view
   ```

4. Export results to JSON:
   ```bash
   promptfoo eval --output results.json
   ```

## Using the Analyzer

### Command Line Analysis

Run the analyzer on your results file:
```bash
python analyze_promptfoo.py
```

The script will generate a detailed report including:
- Executive Summary
- Key Findings & Recommendations
- Model Performance Comparison
- Error Analysis
- Cost Analysis

### Interactive Dashboard

The Streamlit dashboard provides an intuitive interface for:
- Uploading and analyzing results files
- Viewing key performance metrics
- Interactive visualizations of model performance
- Cost analysis and comparisons
- Success rate breakdowns by model

## Output Examples

The analyzer generates a comprehensive report with sections like:

```
=== Promptfoo Analysis Report ===
Generated on: 2024-03-21 10:30:45

📊 EXECUTIVE SUMMARY
-----------------
Overall Success Rate: 85.5%
Total Tests Run: 100
Total Cost: $1.2345

[And more detailed sections...]
```

Created by Jaime Mantilla, MSIT + AI
Last Updated: 08/2025
