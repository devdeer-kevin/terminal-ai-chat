# Terminal AI Chat 🤖

A CLI tool for chatting with Claude (Anthropic AI) directly from your terminal. Built with Deno and TypeScript.

## Features

- Direct communication with Claude via terminal
- Support for markdown formatting in responses
- Persistent chat history
- Configurable system prompts
- TypeScript for better code quality and developer experience

## Prerequisites

- [Deno](https://deno.land/) (Version >= 1.37)
- An API key from [Anthropic](https://www.anthropic.com/)

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/terminal-ai-chat.git
cd terminal-ai-chat
```

2. Create a `.env` file in the root directory:

```bash
ANTHROPIC_API_KEY=your-api-key-here
```

## Usage

Start the application:

```bash
deno run --allow-net --allow-env --allow-read --allow-write main.ts
```

### Chat Commands

- `/exit` or `/quit` - Exit the application
- `/clear` - Clear chat history
- `/help` - Show available commands
- `/save` - Save current conversation

## Project Structure

```
terminal-ai-chat/
├── src/
│   ├── client/
│   │   └── main.ts
│   ├── types/
│   │   └── index.ts
│   ├── utils/
│   │   ├── config.ts
│   └── main.ts
├── config/
│   └── default.ts
├── deno.json
├── .env
└── README.md
```

## Development

1. Install dependencies:

```bash
deno cache --reload deps.ts
```

2. Run tests:

```bash
deno test
```

3. Run linting:

```bash
deno lint
```

## Configuration

The application can be configured through `config/default.ts`:

```typescript
export default {
  model: "claude-3-sonnet-20240229",
  maxTokens: 4096,
  temperature: 0.7,
  historySize: 10,
  logLevel: "info",
};
```

## License

MIT

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Support

If you have any questions or issues, feel free to open an issue.
