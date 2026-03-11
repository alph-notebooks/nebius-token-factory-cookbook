# Structured Output

Get the models to respond in a structured output.

## Runtime

10 mins

## 1 - Ask for JSON in the prompt

1 - Go to playground and select a model

2 - Supply this prompt:

```text
Extract the following fields from the support message:

- issue_type (billing | bug | feature_request | other)
- urgency (low | medium | high)
- customer_sentiment (-1 to 1)
- recommended_action

Output strictly as valid JSON.

<customer email goes here>
```

Here is [customer email](data/customer-email1.txt) we can use.


## 2 - Supply a JSON schema

Here is a sample prompt:

```text
Extract structured fields from the following customer complaint email. Output MUST be valid JSON and nothing else (no commentary, no markdown). Conform to this schema exactly:

{
  "type": "object",
  "required": ["ticket_title","priority","customer_info"],
  "properties": {
    "ticket_title": {"type":"string"},
    "priority": {"type":"string","enum":["P1","P2","P3","P4"]},
    "customer_info": {
        "type":"object",
        "properties":{
            "name":{"type":"string"},
            "email":{"type":"string"},
            "customer_id":{"type":"string"}
        }
    }
  }
}


Now extract from this email text below. Produce valid JSON that matches the schema.

<customer email goes here>
```

Here is [customer email](data/customer-email1.txt) we can use.

## 3 - Using API

We can specify exact JSON output format expected using an API as well.

Example: [guided_json.ipynb](../../guided_json.ipynb)