# API Endpoints

The OpenAI API Key provides access to a variety of endpoints. This guide provides detailed information on how to use the following endpoints:

- [/generate](#generate)
- [/translate](#translate)
- [/analyze](#analyze)
- [/chat](#chat)
- [/image-generate](#image-generate)

## /generate

The `/generate` endpoint is used for text generation. Here is an example using Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.TextGeneration.create(
  engine="text-davinci-002",
  prompt="Translate the following English text to French: '{}'",
  max_tokens=60
)
```

## /translate

The `/translate` endpoint is used for language translation. Here is an example using Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.Translation.create(
  engine="text-davinci-002",
  prompt="Translate the following English text to French: '{}'",
  max_tokens=60
)
```

## /analyze

The `/analyze` endpoint is used for sentiment analysis. Here is an example using Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.Analysis.create(
  engine="text-davinci-002",
  prompt="Analyze the sentiment of the following text: '{}'",
  max_tokens=60
)
```

## /chat

The `/chat` endpoint is used for creating chatbots. Here is an example using Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.Chat.create(
  model="text-davinci-002",
  messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Who won the world series in 2020?"},
    ]
)
```

## /image-generate

The `/image-generate` endpoint is used for image generation. Here is an example using Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.ImageGeneration.create(
  engine="image-davinci-002",
  prompt="Generate an image of a 'blue bird'",
  max_tokens=60
)
```
