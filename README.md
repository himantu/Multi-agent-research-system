# Multi-Agent Research System

A multi-agent research assistant built with Python, LangChain, and Streamlit. The system uses specialized agents to:

- search the web for recent information,
- scrape relevant pages for deeper context,
- generate a structured research report, and
- review the report with a critic agent.

## Features

- Web search powered by Tavily
- URL scraping with BeautifulSoup and requests
- AI-generated research reports
- Built-in critique/feedback on the generated report
- Interactive UI with Streamlit

## Project Structure

```text
Multi-agent-research-system/
├── agents.py          # Agent and chain definitions
├── app.py             # Streamlit web interface
├── pipeline.py        # CLI research pipeline
├── tools.py           # Web search and scraping tools
├── requirements.txt   # Python dependencies
└── .env               # Environment variables (create locally)
```

## Tech Stack

- Python
- LangChain
- OpenAI GPT-4o-mini
- Streamlit
- Tavily Search API
- BeautifulSoup

## Installation

1. Clone the repository
2. Navigate to the project folder
3. Create a virtual environment (recommended)
4. Install dependencies:

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root with the following values:

```env
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

## Run the Streamlit App

```bash
streamlit run app.py
```

This starts the web interface where you can enter a research topic and view the generated report.

## Run the CLI Pipeline

```bash
python pipeline.py
```

You will be prompted to enter a research topic, and the pipeline will run the search, scrape, writing, and critique steps.

## Notes

- The current implementation uses the `gpt-4o-mini` model.
- The scraping tool limits extracted content to a portion of the page for efficiency.
- Make sure your API keys are valid and have available quota.

## License

This project is provided as-is for educational and experimental use.
