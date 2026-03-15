# Getting Ready for the workshop


## Prerequisites

- [Nebius Token Factory](https://tokenfactory.nebius.com/) account
- [tavily](https://app.tavily.com) account
- Python dev env + [uv](https://github.com/astral-sh/uv) python package manager

## Step-1: Get API keys

- **Nebius API key** - Get yours at [Nebius Token Factory](https://tokenfactory.nebius.com/)
- **Tavily API key** - Get yours at [app.tavily.com](https://app.tavily.com) 

## Step-2: Get promocodes if applicable

Details will be given out at the workshop.

## Step 3 - Get the code

```bash
git   clone    https://github.com/nebius/token-factory-cookbook/
cd    token-factory-cookbook/workshops/token-factory-workshop
```

# Step 4 - Setup API Keys

### 4.1 - If running on Google Colab

Add `NEBIUS_API_KEY` and `TAVILY_API_KEY` to **Secrets**

<kbd>
<img src="https://github.com/nebius/token-factory-cookbook/raw/main/images/google-colab-1.png">
</kbd>


### 4.2 - If running locally


Create an `.env` file in project root dir (`token-factory-cookbook`) with both keys.

Use the provided `env_sample.txt` file as starter

```bash
cp   env_sample.txt   .env
```

Add your key in `.env` file as follows:


```text
NEBIUS_API_KEY=your_nebius_api_key_here
TAVILY_API_KEY=tvly-your_tavily_api_key_here
```


## Step 5 - Setup python env

```bash
cd  workshops/token-factory-workshop

uv  sync 
uv  venv
source .venv/bin/activate

# install a custom kernel to be used within vscode ..etc
python -m ipykernel install --user --name="tf-workshop" --display-name "tf-workshop"

jupyter kernelspec list  # verify kernel is successfully created

```

#