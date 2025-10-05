# Web Scraping Project using BeautifulSoup

## 📌 Description
This is a beginner-friendly web scraping project made using Python and the BeautifulSoup library.  
It extracts specific data from a website and displays or saves it for further use.

## 🧰 Tools and Libraries Used
- Python 3  
- BeautifulSoup (bs4)

## ⚙️ How It Works
1. Sends a request to a web page.  
2. Parses the HTML content using BeautifulSoup.  
3. Extracts required information such as titles, links, or text.  
4. Displays the data in the console (or saves it to a file if needed).

## 💡 Example
```python
from bs4 import BeautifulSoup
import requests

url = "https://example.com"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")

for item in soup.find_all("h2"):
    print(item.text)
