# 🦜 LangChain: Summarize Text From YouTube or Website

This Streamlit application enables users to input a YouTube or website URL and receive a concise summary of the content. It leverages LangChain's `load_summarize_chain` with the "stuff" chain type and Groq's LLMs to generate summaries.

---

## 🚀 Features

- **YouTube Summarization**: Extracts and summarizes transcripts from YouTube videos.
- **Website Summarization**: Fetches and summarizes textual content from web pages.
- **Custom Prompting**: Utilizes a tailored prompt template to guide the summarization process.
- **User-Friendly Interface**: Built with Streamlit for an intuitive user experience.

---

## 🛠️ Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/ssarthak0/LangChain-Summarize-Text-From-YouTube-or-Website
   cd LangChain-Summarize-Text-From-YouTube-or-Website
   ```

2. **Create and Activate a Virtual Environment**

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set Environment Variables**

   Create a `.env` file in the root directory and add your Groq API key:

   ```env
   GROQ_API_KEY=your_groq_api_key
   ```

---

## 🧪 Usage

1. **Run the Application**

   ```bash
   streamlit run app.py
   ```

2. **Interact with the App**

   - Enter your **Groq API Key** in the sidebar.
   - Input a **YouTube or website URL**.
   - Click on **"Summarize the Content from YT or Website"**.
   - View the generated summary displayed below the input fields.

---

## 📄 Prompt Template

The application uses the following prompt to guide the summarization:

```plaintext
Provide a summary of the following content in 300 words:
Content:{text}
```

---

## 📚 Dependencies

- `streamlit`
- `langchain`
- `langchain_groq`
- `langchain_community`
- `python-dotenv`
- `validators`
- `os`

Ensure all dependencies are installed as per the `requirements.txt` file.

---

## 📝 Notes

- The application distinguishes between YouTube and other URLs by checking for "youtube.com" in the input.
- For YouTube URLs, it uses `YoutubeLoader` to fetch transcripts.
- For other URLs, it employs `UnstructuredURLLoader` to extract textual content.
- The summarization is performed using LangChain's `load_summarize_chain` with the "stuff" chain type.

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙏 Acknowledgements

- [LangChain](https://www.langchain.com/)
- [Streamlit](https://streamlit.io/)
- [Groq](https://www.groq.com/)
