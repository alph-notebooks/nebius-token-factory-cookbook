# Token Factory Workshop

## `https://bit.ly/4cCCNzV`

<img src="qrcode-workshop.png" width="300px">

## 1 -  Getting Started

[getting started guide](getting-started.md)

## 2 -  Exploring Token Factory

[explore Token Factory UI](explore-token-factory.md)

## 3 -  Structured Output

## 4 - Tool Calling

## 5 - Agent: Research Agent with Tavily

## 6 - Fine Tuning Models

## 7 - Distilling Models

## 8 - Integration with Coding Agents

## 9 - Some FUN

---


## Dev Notes

Project setup:

```bash
uv init --python=3.12
uv add openai  python-dotenv  pydantic tavily-python 
uv add --dev ipykernel

# create a requirements.txt file
uv export --frozen --no-hashes --no-emit-project --no-default-groups --output-file=requirements.txt
```