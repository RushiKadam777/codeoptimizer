# **Code Optimization Suggester** 🚀

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![OpenAI](https://img.shields.io/badge/OpenAI-API-yellow.svg)
![DeepSeek](https://img.shields.io/badge/DeepSeek-API-orange.svg)

An AI-powered web application that analyzes and suggests optimizations for your code snippets. Supports multiple programming languages and both OpenAI/DeepSeek APIs.

## **Features** ✨

- **Multi-language support** (Python, JavaScript, Java, C++, etc.)
- **Smart optimization suggestions** (performance, readability, best practices)
- **API flexibility** (Works with both OpenAI and DeepSeek)
- **Rate limiting** (Prevents API quota exhaustion)
- **Response caching** (Reduces redundant API calls)
- **Error handling** (User-friendly error messages)

## **Demo** 🎥

[![Demo Video](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://youtu.be/YOUR_VIDEO_ID)

## **Installation** ⚙️

### **Prerequisites**
- Python 3.8+
- OpenAI or DeepSeek API key

### **Setup**
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/code-optimizer.git
   cd code-optimizer
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure environment variables:
   ```bash
   cp .env.example .env
   ```
   Edit `.env` with your API details:
   ```ini
   FLASK_SECRET_KEY=your_secret_key
   API_PROVIDER=openai  # or "deepseek"
   API_KEY=your_api_key_here
   API_BASE=https://api.deepseek.com/v1  # Only for DeepSeek
   ```

## **Usage** 🖥️

1. Start the Flask development server:
   ```bash
   python app.py
   ```

2. Open your browser to:
   ```
   http://localhost:5000
   ```

3. Paste your code, select language, and click "Optimize"

## **Configuration** ⚙️

### **API Options**
| Variable | Description |
|----------|-------------|
| `API_PROVIDER` | `openai` or `deepseek` |
| `API_KEY` | Your API key |
| `API_BASE` | Required for DeepSeek |

### **Rate Limiting**
Adjust in `app.py`:
```python
REQUEST_INTERVAL = 1.0  # Seconds between API calls
CACHE_TIMEOUT = 300     # Cache duration in seconds
```

## **Project Structure** 📂
```
code-optimizer/
├── app.py              # Main application
├── requirements.txt    # Dependencies
├── .env.example        # Environment template
├── static/
│   └── style.css       # Stylesheet
└── templates/
    └── index.html      # Frontend interface
```

## **Examples** 💻

Try these optimization examples:

**Python:**
```python
# Before
def sum_list(numbers):
    total = 0
    for num in numbers:
        total += num
    return total

# After (Suggested Optimization)
def sum_list(numbers):
    return sum(numbers)
```

**JavaScript:**
```javascript
// Before
function findMax(arr) {
    let max = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) max = arr[i];
    }
    return max;
}

// After (Suggested Optimization)
function findMax(arr) {
    return Math.max(...arr);
}
```

## **Contributing** 🤝
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## **License** 📄
Distributed under the MIT License. See `LICENSE` for more information.

## **Acknowledgements** 🙏
- OpenAI API
- DeepSeek API
- Flask Community

---

**Happy Coding!** 💻✨
