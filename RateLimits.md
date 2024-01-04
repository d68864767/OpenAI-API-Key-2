# Rate Limits

The OpenAI API has rate limits to ensure fair usage and protect the system from abuse. This guide provides information on the rate limits for the OpenAI API Key.

## Overview

Rate limits are applied on a per-minute basis. If you exceed these limits, you will receive a `429 Too Many Requests` response from the API. The rate limits depend on the type of user:

- Free trial users: 20 requests per minute (RPM) and 40000 tokens per minute (TPM)
- Pay-as-you-go users (first 48 hours): 60 RPM and 60000 TPM
- Pay-as-you-go users (after 48 hours): 3500 RPM and 90000 TPM

## Headers

The API response includes the following headers that provide information about the rate limits:

- `X-RateLimit-Limit`: The maximum number of requests you can make per minute.
- `X-RateLimit-Remaining`: The number of requests remaining in the current rate limit window.
- `X-RateLimit-Reset`: The time at which the current rate limit window resets in UTC epoch seconds.

## Handling Rate Limits

If you exceed the rate limits, you should implement a backoff and retry strategy:

1. Backoff: Wait for some time before making the next request. The backoff time should increase exponentially with each consecutive rate limit error.
2. Retry: Retry the request after the backoff time.

Here is an example of how to handle rate limits in Python:

```python
import time
import openai

openai.api_key = 'your-api-key'

backoff_time = 1  # Start with a short backoff time
max_backoff_time = 120  # Don't wait for more than 2 minutes

while True:
    try:
        response = openai.Completion.create(engine="text-davinci-002", prompt="Hello, world!")
        print(response.choices[0].text.strip())
        backoff_time = 1  # Reset backoff time
    except openai.Error as e:
        if e.status_code == 429:
            print(f"Rate limit exceeded. Waiting for {backoff_time} seconds.")
            time.sleep(backoff_time)
            backoff_time = min(2 * backoff_time, max_backoff_time)  # Increase backoff time
        else:
            raise e
```

## Further Reading

For more information on rate limits, refer to the [OpenAI API documentation](https://beta.openai.com/docs/developer-quickstart/rate-limits/).
