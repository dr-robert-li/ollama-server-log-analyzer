# Ollama Server Log Analyzer

The Access Log Analyzer is a Python script that analyzes server access log files for potential errors, problems, or unusual activity. It utilizes the Ollama Python package and the LLaMA 3 OSS LLM to process the log files and generate insights.

## Features

- Analyzes multiple log files in a specified folder
- Supports both regular log files and gzip compressed log files
- Allows filtering log files based on specific strings
- Processes log files in batches of 500 lines
- Generates a detailed analysis report highlighting potential issues and suspicious activities
- Provides a summary of the analysis findings

## Requirements

- Python 3.x
- Ollama Python package
- LLaMA 3 OSS LLM

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/access-log-analyzer.git
```

2. Install the required dependencies:

```bash
pip install ollama
```

3. Set up the LLaMA 3 OSS LLM:

```bash
ollama run llama3
```

Note: Ensure that you have at least 32GB of memory and port 11434 open on your server.

## Usage

1. Open the `access_log_analyzer.ipynb` notebook in Jupyter Notebook or JupyterLab.

2. Run the notebook cells in sequential order.

3. When prompted, enter the following information:
- Folder path containing the log files
- Filter strings separated by commas (optional)
- Folder path to save the output text file

4. The script will analyze the log files and generate an output text file (`log_analysis_output.txt`) in the specified output folder.

5. The script will also generate a summary of the analysis findings and save it as `log_analysis_summary.txt` in the output folder.

## Customization

If you are running the Ollama API on a different server, you may need to modify the `Client` initialization in the notebook. Update the `host` parameter with the appropriate server URL and port:

```python
from ollama import Client
client = Client(host='http://your-server-url:port')
```


#### License
This project is licensed under the MIT License.

#### Acknowledgements
* Ollama Python Package
* Meta LLaMA 3 OSS LLM