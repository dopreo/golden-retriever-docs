# Golden Retriever

<img src="resources/icon.png" width="128" height="128" alt="Golden Retriever">

A Visual Studio Code extension that brings API collection management right into your editor. Think Postman, but with Git sync and workspace integration.

<!-- add here gif -->
<img src="resources/demo.gif" width="600" alt="Golden Retriever Demo">

## Features

🔄 **Git-Synced Collections**

- Store API collections directly in your repository under the `/collections` folder
- Version control your API collections alongside your code
- Share collections with your team through Git

🚀 **Request Management**

- Create, edit, and organize API requests
- Support for all HTTP methods (GET, POST, PUT, PATCH, DELETE)
- Folder organization for better request management
- Environment variable support through `.env` files

✨ **Rich Request Features**

- Query parameter builder
- Header management with bulk edit support
- Request body editor
- Test script support
- cURL command generation

🧪 **Testing & Validation**

- Write and run tests for your API requests
- Run individual collections or all collections at once
- View detailed test results and response data

## Installation

1. Open Visual Studio Code
2. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
3. Search for "Golden Retriever"
4. Click Install

## Getting Started

1. Create a `collections` folder in your workspace root

   ```bash
   mkdir collections
   ```

2. Create your first collection:

   - Click the Golden Retriever icon in the activity bar
   - Click the "Add Collection" button (+ icon)
   - Enter a name for your collection

3. Add requests:

   - Right-click on your collection
   - Select "Add Request"
   - Configure your request details

4. Run requests:
   - Click on any request to open it
   - Click "Send" to execute
   - View responses in the integrated response viewer

## Environment Variables

Golden Retriever supports environment variables through `.env` files:

1. Create a `.env` file in your workspace root
2. Add your variables:
   ```
   API_KEY=your-api-key
   BASE_URL=https://api.example.com
   ```
3. Use variables in requests with `{{VARIABLE_NAME}}` syntax:
   ```
   {{BASE_URL}}/users?key={{API_KEY}}
   ```

## Collection Structure

Collections are stored as JSON files in your `collections` folder:

```
📁 your-project
 ┣ 📁 collections
 ┃ ┣ 📄 users-api.json
 ┃ ┗ 📄 products-api.json
 ┗ 📄 .env
```

## FAQ

**Q: Where are my collections stored?**  
A: Collections are stored as JSON files in the `collections` folder of your workspace. This allows them to be version controlled with your project.

**Q: Can I import Postman collections?**  
A: Yes! Golden Retriever uses Postman/Newman compatible collection format. Just copy your Postman collection JSON into a file in your `collections` folder.

**Q: How do I share collections with my team?**  
A: Since collections are stored in your project repository, just commit and push the `collections` folder. Your team can pull the changes and immediately use them.

**Q: Are my environment variables secure?**  
A: Environment variables are stored in your local `.env` file, which should be added to `.gitignore` to keep sensitive data secure. The extension supports masking sensitive data in the UI.

**Q: Can I run multiple requests at once?**  
A: Yes! You can run an entire collection or all collections at once using the play button in the collections view.

**Q: Does it support request chaining or variables from responses?**  
A: Currently, this feature is not supported. However, you can use environment variables and test scripts to achieve similar functionality.

**Q: How do I change the collections folder location?**  
A: You can configure the collections path in VSCode settings:

1. Open Settings (Ctrl+,)
2. Search for "Golden Retriever"
3. Update the "Collections Path" setting

## Contributing

Found a bug or have a feature request? Please open an issue on our GitHub repository.

## License

This extension is released under the MIT License.

---

<a href="https://www.flaticon.com/free-icons/golden-retriever" title="golden retriever icons">Golden retriever icons created by Maxim Kulikov - Flaticon</a>
