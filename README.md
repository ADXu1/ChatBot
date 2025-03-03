# ChatBot
# LLM API Hub

![LLM API Hub Banner](https://images.unsplash.com/photo-1677442135136-760c813a6a2e?q=80&w=1920&auto=format&fit=crop)

## 🚀 Overview

LLM API Hub is a modern web application that allows users to seamlessly integrate and interact with various Large Language Model APIs, with a primary focus on Google's Gemini models. This dashboard provides an intuitive interface for managing API configurations and engaging in conversations with AI models.

## ✨ Features

- **Multiple API Integration Methods**:
  - Google Gemini SDK integration
  - Direct Gemini API integration
  - Custom API support for other LLM providers

- **API Management**:
  - Create, edit, and delete API configurations
  - Test API connections before saving
  - Set active API for conversations

- **Chat Interface**:
  - Clean, intuitive messaging UI
  - Real-time conversation with AI models
  - Support for multiple message exchanges

- **Supported Gemini Models**:
  - Gemini 1.5 Flash & Pro
  - Gemini 2.0 Flash & Pro
  - Legacy models (via SDK)

## 🖥️ Screenshots

![Dashboard Screenshot](https://images.unsplash.com/photo-1667372393119-3d4c48d07fc9?q=80&w=1920&auto=format&fit=crop)

## 🛠️ Technologies

- **Frontend**: React, TypeScript, Tailwind CSS
- **Routing**: React Router
- **API Integration**: Google Generative AI SDK, Fetch API
- **State Management**: React Hooks, Local Storage
- **UI Components**: Custom components with Lucide React icons
- **Build Tool**: Vite

## 📋 Prerequisites

- Node.js (v16 or higher)
- Google Gemini API key (get one at [Google AI Studio](https://makersuite.google.com/app/apikey))

## 🚀 Getting Started

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/llm-api-hub.git
cd llm-api-hub
```

2. **Install dependencies**

```bash
npm install
```

3. **Start the development server**

```bash
npm run dev
```

4. **Build for production**

```bash
npm run build
```

## 🔧 Configuration

1. Navigate to the Settings page
2. Click "Add New API"
3. Choose your provider:
   - Google Gemini (SDK)
   - Google Gemini (Direct API)
   - Custom API
4. Enter your API key and other required information
5. Test the connection
6. Save your configuration

## 🌐 API Integration Examples

### Google Gemini SDK

```javascript
import { GoogleGenerativeAI } from '@google/generative-ai';

const genAI = new GoogleGenerativeAI(apiKey);
const model = genAI.getGenerativeModel({ model: 'gemini-pro' });
const result = await model.generateContent(prompt);
const response = await result.response;
const text = response.text();
```

### Direct Gemini API

```javascript
const endpoint = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;
const response = await fetch(endpoint, {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    contents: [{ parts: [{ text: prompt }] }]
  })
});
const data = await response.json();
const text = data.candidates?.[0]?.content?.parts?.[0]?.text;
```

## 🔒 Security

- API keys are stored locally in the browser's localStorage
- No data is sent to any server except the LLM provider's API
- Consider implementing server-side proxies for production use

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [Google Generative AI](https://ai.google.dev/)
- [React](https://reactjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Lucide Icons](https://lucide.dev/)
- [Vite](https://vitejs.dev/)

---

Made with ❤️ by Ethan
