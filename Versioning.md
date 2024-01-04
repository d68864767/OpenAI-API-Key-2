# Versioning

The OpenAI API Key supports multiple versions to ensure backward compatibility and to introduce new features and improvements. This guide provides information on the different versions of the OpenAI API Key and how to use them.

## Table of Contents

1. [API Version 1.0](#api-version-1.0)
2. [API Version 2.0](#api-version-2.0)
3. [Future Versions](#future-versions)

## API Version 1.0

API Version 1.0 is the initial version of the OpenAI API Key. It provides basic functionalities such as text generation, language translation, sentiment analysis, and more. To use this version, include `v1` in the API endpoint URL like this:

```python
'https://api.openai.com/v1/endpoint'
```

Replace `endpoint` with the specific endpoint you want to use.

## API Version 2.0

API Version 2.0 introduces new features and improvements over the previous version. It includes additional functionalities such as chatbots, image generation, and more. To use this version, include `v2` in the API endpoint URL like this:

```python
'https://api.openai.com/v2/endpoint'
```

Replace `endpoint` with the specific endpoint you want to use.

## Future Versions

OpenAI is continuously working on improving the API and adding new features. Future versions of the API will be announced in the [Updates and Changelog](UpdatesAndChangelog.md) section. To use a future version, include the version number in the API endpoint URL as shown in the examples above.

Please note that when a new version is released, the previous versions will still be supported for a certain period of time to ensure backward compatibility. However, it is recommended to always use the latest version to take advantage of the new features and improvements.

For more information on how to use the OpenAI API Key, please refer to the [API Documentation](APIDocumentation.md) guide.
