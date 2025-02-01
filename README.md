# accelotl

<div align="left"><img width="400px" src="https://github.com/user-attachments/assets/f1c9f3eb-d402-441a-9e0f-a3315068b0f1"></div>


## What is Accelotl?

**Accelotl** is a lightweight library designed to simplify and manage asynchronous workflows with multiple LLMs (Large Language Models). Inspired by the adaptability and flexibility of the axolotl, it offers robust and extensible asynchronous processing capabilities.

### Key Features

- **Asynchronous Workflow Management**: Easily build and manage complex task flows.
- **Highly Extensible Design**: Modular structure allows seamless integration with other tools and libraries.
- **Multi-LLM Support**: Smoothly interact with multiple language models.
- **Error Handling and Retry Mechanisms**: Robust support for retries, timeouts, and error recovery.
- **Customizable**: Intuitive APIs enable flexible flow configurations.

---

## Installation

To install Accelotl, use the following command:

```bash
npm install accelotl
# or
yarn add accelotl
```

---

## Getting Started

Here is an example of using Accelotl to interact with LLMs (such as OpenAI) through an elegant interface:

```typescript
import { Accelotl } from 'accelotl';

// Create an instance
const accelotl = new Accelotl({
  openai: {
    apiKey: 'your-openai-api-key',
  },
  otherPlatform: {
    apiKey: 'your-other-platform-api-key',
  },
});

// Specify a model and send a prompt to generate text
const result = await accelotl
  .use('openai', { model: 'text-davinci-003' })
  .generate({
    prompt: 'What is Accelotl?',
  });

console.log('Generated text:', result);
```

### Highlights

- **Easy Setup**: Configure API keys for multiple platforms in one place.
- **Simple Model Selection**: Flexibly choose models with the `use` method.
- **Promise-based Response**: Streamline asynchronous flow implementation.
- **Unified Interface**: Consistent operations across different LLMs.

---

## Why Choose Accelotl?

Accelotl bridges the gap between simplicity and scalability in asynchronous programming. By abstracting LLM selection and setup, it simplifies complex asynchronous workflows, reducing the burden on developers.

---

## Use Cases

- **API Orchestration**: Manage API calls with retries and error handling.
- **Data Pipelines**: Process and transform data across multiple stages.
- **Language Model Integration**: Build asynchronous flows for applications using multiple LLMs.

---

## License

Accelotl is licensed under the **Apache License 2.0**. See the [LICENSE](./LICENSE) file for details.

---

## Acknowledgments

Inspired by the flexibility of axolotls and the power of asynchronous programming. Special thanks to the LangChain.js community for their contributions.

