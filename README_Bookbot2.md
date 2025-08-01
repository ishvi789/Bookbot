
# 📚 Bookbot2.0

A smart book recommendation chatbot powered by IBM Watson Assistant and Node.js (or your tech stack).

---

## 🧠 Overview

**Bookbot2.0** lets users interactively explore and get recommendations for books based on genre, author, or themes. It’s built with IBM Watson Assistant for understanding queries, paired with a backend in JavaScript or Python to fetch relevant data.

- Effortless book suggestions with natural conversation flow  
- Backend logic to look up books or integrate external APIs (e.g., Google Books, Goodreads)  
- Clean, easy-to-read user interface

---

## 🚀 Features

- Conversation-driven: ask anything about books  
- Supports filters like genre, author, mood, or language  
- Integrable with web, mobile, and chat platforms  
- Easily extensible to include more sources or advanced logic

---

## 🛠️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) or Python installed  
- An IBM Watson Assistant skill created and published  
- Your **integrationID**, **region**, and **serviceInstanceID** ready (from IBM Cloud Web Chat settings)

### Installation & Setup

1. Clone the repo  
   ```bash
   git clone https://github.com/ishvi789/Bookbot2.0.git
   cd Bookbot2.0
   ```

2. Install dependencies  
   ```bash
   npm install       # or pip install -r requirements.txt
   ```

3. Add configuration file (e.g., `.env`) for sensitive keys  
   ```
   WATSON_ASSISTANT_APIKEY=<your_api_key>
   WATSON_ASSISTANT_URL=<your_assistant_url>
   ```

4. Start the backend server  
   ```bash
   npm start         # or python app.py
   ```

5. Copy the Watson Web Chat embed code (from Watson Assistant → Integrations → Web Chat → Embed tab).  
   Paste it into `index.html` just above `</body>`.

---

## 🔧 Example Embed Code Snippet

```html
<script>
  window.watsonAssistantChatOptions = {
    integrationID: "YOUR_INTEGRATION_ID",
    region: "YOUR_REGION",
    serviceInstanceID: "YOUR_SERVICE_INSTANCE_ID",
    onLoad: function(instance) { instance.render(); }
  };
  setTimeout(function(){
    const t = document.createElement('script');
    t.src = "https://web-chat.global.assistant.watson.appdomain.cloud/versions/latest/WatsonAssistantChatEntry.js";
    document.head.appendChild(t);
  });
</script>
```

---

## 📂 Project Structure

```
Bookbot2.0/
├── public/
│   └── index.html               ← Embed snippet goes here
├── src/
│   ├── server.js                ← Backend logic & APIs
│   └── bookdata.js              ← Sample book data or API integration
├── .env.example                 
├── package.json or requirements.txt
└── README.md
```

---

## 🧩 How It Works

1. User interacts with chatbot widget on the website  
2. Dialog skill handles intents and entities  
3. Backend finds matching books and returns recommendations  
4. Chatbot delivers suggestions conversationally

---

## 🧪 Sample Interaction

- **User**: “Recommend me a fantasy book”  
- **Bot**: “You might enjoy *The Hobbit* or *The Name of the Wind*—would you like more?”  
- **User**: “Yes”  
- **Bot**: “Have you read *Harry Potter* series? It’s a great next pick!”

---

## 🧵 Contributing

Contributions are welcome! Feel free to:

- Improve book datasets or API integrations  
- Add support for user preferences history  
- Enhance the dialog or UI flow  

To start:
```bash
git fork https://github.com/ishvi789/Bookbot2.0.git
git checkout -b feature-new-books
# Make changes → Push → Create Pull Request
```

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` file for details.

---

## ✅ Resources

- [Watson Assistant Docs](https://cloud.ibm.com/docs/assistant) — setup, integration, and customization  
- [Google Books API Documentation](https://developers.google.com/books)  
- [Goodreads Developer API](https://www.goodreads.com/api) (if available)
