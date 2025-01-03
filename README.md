# Twitter Trends Scraper (TrendScraper)🐦
# DEMO : https://drive.google.com/file/d/1Qb265-OA_g_9u6jxxpuZwndm8OjNFRHG/view?usp=sharing
A web application that automatically scrapes trending topics from Twitter using Selenium automation. Built with Python Flask and MongoDB.

## 🌟 Key Features

- Automated Twitter login and trend scraping
- Real-time trend fetching with one click
- MongoDB integration for data persistence
- Clean UI with Tailwind CSS
- Error handling and logging
- IP tracking for each scrape request

## 🛠️ Tech Stack

- **Backend:** Python, Flask
- **Frontend:** HTML, JavaScript, Tailwind CSS
- **Database:** MongoDB
- **Automation:** Selenium WebDriver
- **Other:** Chrome WebDriver, python-dotenv

## 📋 Prerequisites

- Python 3.8+
- Google Chrome browser
- MongoDB account
- Twitter account

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd stir
   ```

2. **Set up Python environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Configure environment variables**
   Create `.env` file in root directory:
   ```
   MONGODB_URI=your_mongodb_connection_string
   TWITTER_USERNAME=your_twitter_username
   TWITTER_PASSWORD=your_twitter_password
   PROXYMESH_HOST=proxy_host  # Optional
   PROXYMESH_PORT=proxy_port  # Optional
   ```

4. **Run the application**
   ```bash
   python src/app.py
   ```

5. **Access the application**
   Open `http://localhost:5000` in your browser

## 📁 Project Structure

```
stir/
├── src/
│   ├── app.py          # Flask server and routes
│   ├── scraper.py      # Twitter scraping logic
│   └── config.py       # Configuration management
├── templates/
│   └── index.html      # Frontend interface
├── requirements.txt    # Python dependencies
├── .env               # Environment variables
└── README.md          # Documentation
```

## 🔧 Configuration

| Variable | Description | Required |
|----------|-------------|----------|
| MONGODB_URI | MongoDB connection string | Yes |
| TWITTER_USERNAME | Twitter login username | Yes |
| TWITTER_PASSWORD | Twitter login password | Yes |
| PROXYMESH_HOST | Proxy server host | No |
| PROXYMESH_PORT | Proxy server port | No |

## 🔒 Security Considerations

- Never commit `.env` file to version control
- Use environment variables for sensitive data
- Implement rate limiting for production
- Keep dependencies updated
- Use secure MongoDB connection string

## 🐛 Troubleshooting

1. **Selenium Issues**
   - Ensure Chrome browser is installed
   - Update Chrome WebDriver if needed
   - Check Chrome version compatibility

2. **MongoDB Connection**
   - Verify MongoDB URI is correct
   - Check network connectivity
   - Ensure IP whitelist is configured

3. **Twitter Login Fails**
   - Verify credentials are correct
   - Check for Twitter rate limiting
   - Consider using proxy if blocked
