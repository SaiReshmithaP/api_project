# LLM-Based Assignment Answering API

This project provides an API that automatically answers graded assignment questions for the IIT Madras Online Degree in Data Science course **'Tools in Data Science'**. The API is deployed on Vercel and can accept text-based questions and file uploads to generate answers.

## 🚀 Tech Stack
- **Backend**: Python (FastAPI or Flask)
- **Deployment**: Vercel (using Serverless Functions) or AWS Lambda
- **LLM Integration**: OpenAI GPT API or a fine-tuned local model
- **Storage**: Temporary in-memory storage or cloud storage (for handling file uploads)
- **Repository**: GitHub with an MIT License

## 📌 API Implementation
### **Endpoint:**
```
POST https://your-app.vercel.app/api/
```

### **Request Format:**
The API accepts a **POST request** with the following:
- `question` (string) – The assignment question.
- `file` (optional) – A file attachment (e.g., ZIP containing a CSV file).

Example Request using `curl`:
```bash
curl -X POST "https://your-app.vercel.app/api/" \
  -H "Content-Type: multipart/form-data" \
  -F "question=Download and unzip file abcd.zip which has a single extract.csv file inside. What is the value in the 'answer' column of the CSV file?" \
  -F "file=@abcd.zip"
```

### **Processing Logic:**
1. If the request contains only text:
   - The API sends the question to an LLM (e.g., OpenAI GPT) to generate an answer.
2. If the request contains a file:
   - The API extracts relevant information from the file (e.g., reads a CSV inside a ZIP) and returns the required data.

### **Response Format:**
```json
{
  "answer": "1234567890"
}
```

## 📦 Deployment
The API is deployed using **Vercel**. To deploy:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Deploy to Vercel:
   ```bash
   vercel deploy
   ```

## 📜 License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## 📌 Contributing
Contributions are welcome! Feel free to fork this repository and submit pull requests.

---
**Maintainer:** [Sai Reshmitha](https://github.com/SaiReshmithaP)
