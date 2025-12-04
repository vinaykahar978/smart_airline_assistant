# Smart Airline Assistant

🚀 **Live Demo:** (https://huggingface.co/spaces/vinaykahar978/smart_airline_assistant)

FlightAI is an interactive AI-powered airline support assistant built using **Gradio** and **OpenAI models**.
It helps users get instant travel information, including:

* ✈️ Flight ticket prices (via SQLite database lookup)
* 🖼️ AI-generated destination images (DALL·E 3)
* 🔊 Natural AI voice responses (GPT-4o Mini TTS)
* 💬 A smooth chat interface powered by GPT-4.1 Mini

Perfect for learning:
✔ AI tools
✔ Function calling
✔ TTS
✔ Image generation
✔ Database integration
✔ Gradio apps on Hugging Face Spaces

---

## 🌟 Features

### 🔍 **1. Ticket Price Lookup**

FlightAI fetches ticket prices from an internal **SQLite database (`prices.db`)**.

### 🎨 **2. AI Destination Art**

If a user mentions a travel city, the system generates a **beautiful pop-art style image** of that destination using **DALL·E 3**.

### 🔊 **3. Text-to-Speech Responses**

Every assistant reply is turned into natural speech via **GPT-4o Mini TTS**.

### 🤖 **4. Intelligent Chat**

Powered by **GPT-4.1 Mini** with function calling enabled and a custom system prompt for short, courteous airline-style responses.

### 🧱 **5. Simple Gradio UI**

A clean interface consisting of:

* Chatbot
* Generated image display
* Autoplay audio
* User textbox input

---

## 🗂️ Project Structure

```
app.py            # Main application
prices.db         # SQLite database (ticket prices)
requirements.txt  # Python dependencies
README.md         # Project documentation
```

---

## 🔧 Installation (Local Setup)

If you want to run this project locally:

```bash
git clone <your-repo-url>
cd <project-folder>

pip install -r requirements.txt
```

Create a `.env` file:

```
OPENAI_API_KEY=your_openai_key_here
```

Run:

```bash
python app.py
```

---

## 🧪 How It Works

### 💬 1. Chat

User sends a message → GPT-4.1 Mini analyzes and may call a function.

### 🛠 2. Function Calling

If user asks about a city →
`get_ticket_price()` fetches price from **prices.db**.

### 🎨 3. Image Generation

If a city is detected →
DALL·E 3 generates a **pop-art travel image**.

### 🔊 4. Text-to-Speech

Assistant’s reply → converted into **AI voice**.

### 🖥️ 5. Display

Chat + image + audio returned to the Gradio interface.

---

## 🔑 Secrets & API Keys (For Hugging Face Spaces)

Go to:

**Settings → Variables and Secrets → Repository Secrets**

Add:

```
OPENAI_API_KEY = your_key_here
```

---

## 🗃️ Database Notes

The app uses a local `prices.db` file.
If it’s not present, the app auto-creates an empty database, but **no prices will be available**.
You should upload a populated `prices.db`.


---

## 📦 Requirements

```
gradio
openai
python-dotenv
Pillow
```

SQLite is built into Python — no installation required.

---

## 🚀 Deployment on Hugging Face Spaces

1. Create a Space → Select **Gradio**
2. Upload:

   * `app.py`
   * `requirements.txt`
   * `prices.db`
   * `README.md`
3. Add the `OPENAI_API_KEY` secret
4. The Space will build automatically

---
