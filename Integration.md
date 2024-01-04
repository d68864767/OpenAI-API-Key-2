# Integration

The OpenAI API Key can be integrated with various programming languages. This guide provides instructions on how to integrate the OpenAI API Key with the following languages:

- [Python](#python)
- [JavaScript](#javascript)
- [Ruby](#ruby)
- [PHP](#php)
- [Java](#java)
- [C#](#csharp)
- [Node.js](#nodejs)
- [Go](#go)
- [Swift](#swift)

## Python

To integrate the OpenAI API Key with Python, you will need to install the OpenAI Python SDK. You can do this using pip:

```bash
pip install openai
```

Then, you can use the OpenAI API Key in your Python code like this:

```python
import openai

openai.api_key = 'your-api-key'
```

## JavaScript

To integrate the OpenAI API Key with JavaScript, you will need to install the OpenAI JavaScript SDK. You can do this using npm:

```bash
npm install openai
```

Then, you can use the OpenAI API Key in your JavaScript code like this:

```javascript
const openai = require('openai');

openai.setApiKey('your-api-key');
```

## Ruby

To integrate the OpenAI API Key with Ruby, you will need to install the OpenAI Ruby Gem. You can do this using gem:

```bash
gem install openai
```

Then, you can use the OpenAI API Key in your Ruby code like this:

```ruby
require 'openai'

OpenAI.api_key = 'your-api-key'
```

## PHP

To integrate the OpenAI API Key with PHP, you will need to install the OpenAI PHP Library. You can do this using composer:

```bash
composer require openai/openai
```

Then, you can use the OpenAI API Key in your PHP code like this:

```php
require 'vendor/autoload.php';

$openai = new OpenAI\OpenAI('your-api-key');
```

## Java

To integrate the OpenAI API Key with Java, you will need to install the OpenAI Java SDK. You can do this using Maven:

```xml
<dependency>
  <groupId>com.openai</groupId>
  <artifactId>openai</artifactId>
  <version>1.0.0</version>
</dependency>
```

Then, you can use the OpenAI API Key in your Java code like this:

```java
import com.openai.OpenAI;

OpenAI openai = new OpenAI("your-api-key");
```

## C#

To integrate the OpenAI API Key with C#, you will need to install the OpenAI C# Library. You can do this using NuGet:

```bash
Install-Package OpenAI -Version 1.0.0
```

Then, you can use the OpenAI API Key in your C# code like this:

```csharp
using OpenAI;

OpenAI openai = new OpenAI("your-api-key");
```

## Node.js

To integrate the OpenAI API Key with Node.js, you will need to install the OpenAI Node.js Package. You can do this using npm:

```bash
npm install openai
```

Then, you can use the OpenAI API Key in your Node.js code like this:

```javascript
const openai = require('openai');

openai.setApiKey('your-api-key');
```

## Go

To integrate the OpenAI API Key with Go, you will need to install the OpenAI Go Library. You can do this using go get:

```bash
go get github.com/openai/openai-go
```

Then, you can use the OpenAI API Key in your Go code like this:

```go
import "github.com/openai/openai-go"

openai.ApiKey = "your-api-key"
```

## Swift

To integrate the OpenAI API Key with Swift, you will need to install the OpenAI Swift Package. You can do this using Swift Package Manager:

```swift
dependencies: [
    .package(url: "https://github.com/openai/openai-swift", from: "1.0.0")
]
```

Then, you can use the OpenAI API Key in your Swift code like this:

```swift
import OpenAI

let openai = OpenAI(apiKey: "your-api-key")
```
