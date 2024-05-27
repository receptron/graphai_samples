# GraphAI Samples

## Overview

[GraphAI](https://github.com/receptron/graphai) is an asynchronous data flow execution engine, which allows developers to build *agentic applications* by describing *agent workflows* as declarative data flow graphs in YAML or JSON. 

This repository contains several sample GraphAI YAML files under the samples folder.

To run those samples, you need to install [GraphAI cli](https://github.com/receptron/graphai_cli) node package.

```
npm i -g  @receptron/graphai_cli
```

Then, you need to acquire approrpiate service keys, put them in .env file like below, and place it at the current folder.

```
OPENAI_API_KEY=sk-...
GROQ_API_KEY=gsk_...
ANTHROPIC_API_KEY=sk-...
GOOGLE_GENAI_API_KEY=AI...
```

After that you can run those GraphAI YAML files like below.

```
graphai openai/chat.ts # if you place .env file under the samples folder
graphai chat.ts # if you place .env file under the samples/openai folder.
```

## Samples

### chat.yaml

This is a simple chat application, which allows the user to talk to an AI chatbot. To terminate, type "/bye".

### interview.yaml

This application generates an interview of somebody you specify, such as "Steve Jobs" or "Satoshi Nakamoto".

### weather.yaml

This application acts as meteorologist. It will acquire the weather information from weather.gov and provide the weather information about the specified location.

### reception.yaml

This application acquires the name, date of birth and gender from the user, and report it. 

### metachat.yaml

This application dynamically generates an AI agentapp, which acquires the name, address and phone number from the user, using the reception.yaml as an example.

### wikipedia_rag.yaml

This appilcation performs an in-memory RAG using a Wikipedia article as the data source. 

**NOTE**: Because this application uses OpenAI's embeddings API, OPENAI_API_KEY is required even if you pick a non-OpenAI LLM. 