# Authentication

Authentication to the OpenAI API is performed via API keys. This guide provides instructions on how to authenticate with the OpenAI API using API tokens and OAuth.

## API Tokens

API tokens are the primary method of authenticating with the OpenAI API. When you sign up for an account with OpenAI, you will be provided with an API key. This key should be included in all API requests to the server in a header that looks like the following:

```python
'Authorization: Bearer YOUR_API_KEY'
```

Replace `YOUR_API_KEY` with your actual API key.

Here is an example of how to use the API key in Python:

```python
import openai

openai.api_key = 'your-api-key'
```

## OAuth

OAuth is a protocol that lets external apps request authorization to private details in an OpenAI account without getting your password. This is preferred over Basic Authentication because tokens can be limited to specific types of data, and can be revoked by users at any time.

To authenticate via OAuth, you will need to create an OAuth app in your OpenAI account settings. Once you have created the app, you can use the client ID and client secret to authenticate like this:

```python
import openai

openai.client_id = 'your-client-id'
openai.client_secret = 'your-client-secret'
```

Please note that OAuth is not supported in all OpenAI SDKs. Check the documentation of the specific SDK for more details.

## Security

Never expose your API keys in any public website's client-side code. API keys are intended to be used in server-side code and stored securely on your server. If you need to use the API from a client-side application, consider using OAuth instead.

For more information on security best practices, please refer to the [Security Best Practices](SecurityBestPractices.md) guide.
