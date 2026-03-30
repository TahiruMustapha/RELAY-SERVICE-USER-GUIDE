---
title: Custom Model Provider Guide
description: "How to configure custom model providers in OpenClaw."
---

# Custom Model Provider Guide

This tutorial walks you through configuring custom model providers in OpenClaw to connect various third-party AI model services.

## Prerequisites

Before you begin, make sure you have:
* OpenClaw installed and running.
* An API key from at least one model provider (e.g., PinCC, Alibaba Cloud Bailian, DeepSeek, etc.).

---

## Core Concepts

OpenClaw supports connecting any API endpoint compatible with OpenAI / Anthropic / Google protocols via `models.providers`.

### Supported API Protocols

| Protocol | Use Case |
| :--- | :--- |
| `anthropic-messages` | Anthropic Claude series and compatible APIs |
| `openai-completions` | OpenAI and most OpenAI-compatible providers |
| `openai-responses` | OpenAI Responses API |
| `google-generative-ai` | Google Gemini series |

---

## Configuration File Location

The OpenClaw configuration file is located at:
`~/.openclaw/openclaw.json`

---

## Basic Configuration Structure

```json
{
  "models": {
    "mode": "merge",
    "providers": {
      "provider-name": {
        "baseUrl": "API base URL",
        "apiKey": "your-api-key",
        "api": "protocol-type",
        "models": [
          {
            "id": "model-id",
            "name": "Model Display Name",
            "contextWindow": 200000,
            "maxTokens": 8192
          }
        ]
      }
    }
  }
}
```

---

## Configuration Examples

### Example: PinCC (Multi-model Aggregation Platform)

PinCC supports Claude, OpenAI, and Gemini models with a single API key.

**1. Configure Claude Models**
```json
{
  "models": {
    "mode": "merge",
    "providers": {
      "pincc-claude": {
        "baseUrl": "your-pincc-relay-url",
        "apiKey": "your-pincc-token",
        "api": "anthropic-messages",
        "authHeader": true,
        "models": [
          {
            "id": "claude-sonnet-4-6",
            "name": "Claude Sonnet 4.6",
            "api": "anthropic-messages",
            "contextWindow": 200000,
            "maxTokens": 8192
          }
        ]
      }
    }
  }
}
```

**2. Configure Google Gemini Models**
```json
{
  "pincc-gemini": {
    "baseUrl": "your-pincc-relay-url/v1beta",
    "apiKey": "your-pincc-token",
    "api": "google-generative-ai",
    "authHeader": true,
    "models": [
      {
        "id": "gemini-3.1-pro-preview",
        "name": "Gemini 3.1 Pro Preview",
        "api": "google-generative-ai",
        "contextWindow": 1000000,
        "maxTokens": 65536
      }
    ]
  }
}
```
