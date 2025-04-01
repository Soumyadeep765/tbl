# Welcome to TBL Documentation

![TBL Logo](https://raw.githubusercontent.com/Soumyadeep765/tbl/main/assets/logo.png)

Tele Bot Lang (TBL) is a custom scripting language designed specifically for Telegram bot development with:

- 🚀 **Zero-setup** environment
- 💡 **JavaScript-like** syntax
- 🤖 **Built-in** Telegram API methods
- 📦 **Preloaded** utilities (HTTP, Storage, etc.)

```info
**Pro Tip**: TBL automatically handles updates and provides useful variables like `user`, `chat`, and `message` in every command.
```

## Quick Example

Here's a simple TBL command:

```tbl
Command: /greet
Aliases: hello, hi
Answer: Hello {user.first_name}! I'll greet you properly...
Code: {
  // Get current hour for proper greeting
  let hour = new Date().getHours();
  let greeting = hour < 12 ? "Good morning" : 
                hour < 18 ? "Good afternoon" : "Good evening";
  
  // Send personalized message
  Api.sendMessage({
    text: `${greeting} ${user.first_name}! 😊`,
    reply_markup: {
      inline_keyboard: [[{
        text: "Visit our website",
        url: "https://teleservices.io"
      }]]
    }
  });
}
```

```warning
Remember to handle errors in your TBL code. Use the `on_error` parameter in API calls to gracefully handle failures.
```

## Key Features

### 1. Built-in Components
TBL comes with these ready-to-use components:

- **Api**: Direct Telegram API access
- **Bot**: Simplified bot methods
- **HTTP**: Web request capabilities
- **Libs**: Utility libraries

### 2. Custom Markdown
This documentation supports special TBL-flavored markdown:

- ` ```tbl ` code blocks with copy functionality
- ` ```info ` and ` ```warning ` note blocks
- Automatic syntax highlighting

### 3. Easy Integration
All your documentation lives in GitHub:

1. Edit Markdown files
2. Push changes
3. Documentation updates automatically

---

Ready to get started? [Check out the Getting Started guide](#getting-started)
