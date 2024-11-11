---
title: "Ollama"
weight: 
description: >
  Run your models locally
categories: [ArtificialIntelligence]
tags: [LocalModel]
---

Prerequirement 
- GPU -- good news/bad news - it works/it works badly
https://ollama.com/blog/amd-preview

docker run -d -p 3001:8080 -e OLLAMA_BASE_URL=http://<REMOTE_SERVER_IP>:11434/  --name open-webui --restart always ghcr.io/open-webui/open-webui:main

ollama -- lLM runner 


# Installation of ollama
  manual installation - custom configuration 
  https://ollama.com/blog/ollama-is-now-available-as-an-official-docker-image

expain installation shell script 

LLM,SLM, large Image model
# Companies which creates models 

# Possible options to use AI models
ollama https://github.com/ollama/ollama
azure's openai offering 
openai 

# Tool kit 
ROCm and CUDA

# Terminologies with respect to AI

What is a token --?
what is a model --? create a modelfile
what is a dataset? 
what is training?
what is fine-tuning model--? 
what is instruct model ?
what is prompt --? vary based on model
tool calling ?
NLP?
Transformers? 


what is a library/framework --?
  langchain/langgraph 


# RAG / Vector database


# local models
- privacy - no third-party-service
- cost - CAPEX high/ OPEX low

# repositories
Huggingface like pypi,registry,



# ollama inside vs code editor 
https://ollama.com/blog/continue-code-assistant


# ollama client as python package 
https://ollama.com/blog/python-javascript-libraries

