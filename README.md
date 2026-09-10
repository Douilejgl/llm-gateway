# llm-gateway

FastAPI gateway in front of an LLM with response caching

Side project, maintained when I have time.

## Installation

```bash
pip install -r requirements.txt
uvicorn main:app --reload
```

## Features

- Latency measured and returned per request
- POST /v1/chat with prompt/model/max_tokens
- Provider SDK plugs into one function
- SHA-256 keyed in-memory response cache

## Usage

```bash
curl localhost:8000/v1/chat \
  -H 'content-type: application/json' \
  -d '{"prompt": "hello", "model": "gpt-4o-mini"}'
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .gitignore
├── CHANGELOG.md
├── LICENSE
├── SECURITY.md
├── main.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## License

MIT. Do whatever you want.
