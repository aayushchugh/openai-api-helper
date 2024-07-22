# openai-helper

`openai-helper` is a user-friendly library designed to simplify interactions with the OpenAI API.<br /> With minimal setup, you can start making requests to OpenAI's chat completions endpoint quickly and easily. This package provides a straightforward way to integrate OpenAI's powerful language models into your applications with just a few lines of code.

## Key Features
Easy Setup: Initialize with your OpenAI API key and get started in minutes.<br />
Simplified API Calls: Use a single method to make requests and handle responses effortlessly.

## Installation
Install openai-helper using npm:
```bash
npm install openai-helper
```
## Usage
Basic Example
Here’s how to use openai-helper to interact with the OpenAI API:
```javascript
const OpenAIHelper = require('openai-helper');

async function main() {
    const apiKey = 'YOUR_OPENAI_API_KEY';
    const model = 'GPT_MODEL';
    const prompt = 'YOUR_PROMPT';

    const openai = new OpenAIHelper(apiKey);

    try {
        const response = await openai.call(model, prompt, 0.8,1);
        console.log('Response from OpenAI:', message);
    } catch (error) {
        console.error('Error:', error);
    }
}

main();
```

## Call Method
The call method sends a request to the OpenAI API and returns the response.

model: Specify the GPT model (e.g., 'gpt-4o-mini').<br />
prompt: Provide the text prompt for the model.<br />
temperature (optional): Adjust the randomness of the response (default is 0.7).<br />
responseType (optional): Format your response json. (0 for complete json response, 1 for message string reponse. default is 1)<br />

## Testing
You can find a sample usage file in the repository for testing purposes:</br>
`test.js`: Contains example code demonstrating how to use the openai-helper library.</br>

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please fork the repository and submit pull requests or open issues to suggest improvements. Ensure that your code follows the project's coding standards and includes appropriate tests.
