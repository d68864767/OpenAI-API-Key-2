# Data Input and Output

The OpenAI API Key allows for various types of data input and output. This guide provides detailed information on how to handle data input and output when using the OpenAI API Key.

## Table of Contents

1. [Data Input](#data-input)
2. [Data Output](#data-output)

## Data Input

Data input refers to the data you send to the OpenAI API. This could be a text string for text generation, a language code for translation, or an image for image generation. The data input is usually included in the body of the API request.

Here is an example of data input using the `/generate` endpoint in Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.TextGeneration.create(
  engine="text-davinci-002",
  prompt="Translate the following English text to French: '{}'",
  max_tokens=60
)
```

In this example, the data input is the `prompt` and `max_tokens` parameters.

## Data Output

Data output refers to the data you receive from the OpenAI API. This could be a generated text string, a translated text, or a generated image. The data output is included in the response from the API.

Here is an example of data output using the `/generate` endpoint in Python:

```python
import openai

openai.api_key = 'your-api-key'

response = openai.TextGeneration.create(
  engine="text-davinci-002",
  prompt="Translate the following English text to French: '{}'",
  max_tokens=60
)

print(response['choices'][0]['text'])
```

In this example, the data output is the generated text, which is accessed from the `response` object.

Remember to handle your data input and output correctly to ensure the proper functioning of your application. For more specific information on data input and output for different endpoints, refer to the [API Endpoints](APIEndpoints.md) guide.
