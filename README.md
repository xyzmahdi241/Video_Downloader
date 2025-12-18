# 🎥 Video Downloader

<div align="center">

![Video Downloader Banner](https://img.shields.io/badge/Video-Downloader-6366f1?style=for-the-badge&logo=download&logoColor=white)

**Download videos from YouTube, Facebook, and Instagram with ease!**

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-000000?style=flat-square&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](CONTRIBUTING.md)

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-usage) • [API Documentation](#-api-documentation) • [Contributing](#-contributing)

</div>

---

## 📋 Table of Contents

- [Features](#-features)
- [Demo](#-demo)
- [Screenshots](#-screenshots)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## ✨ Features

### 🚀 Core Features

- **Multi-Platform Support**: Download videos from YouTube, Facebook, and Instagram
- **High-Quality Downloads**: Get videos in the best available quality
- **Fast Processing**: Optimized download engine for maximum speed
- **User-Friendly Interface**: Beautiful, modern, and responsive UI
- **No Registration Required**: Start downloading immediately
- **Unlimited Downloads**: Download as many videos as you want

### 🎨 UI/UX Features

- ✅ Animated gradient backgrounds
- ✅ Smooth transitions and interactions
- ✅ Real-time progress tracking
- ✅ Platform auto-detection
- ✅ Copy-paste support
- ✅ Keyboard shortcuts
- ✅ Mobile-responsive design
- ✅ Dark-themed footer

### 🔒 Security & Privacy

- 🛡️ Secure file handling
- 🔐 No data storage
- ⏰ Automatic file cleanup (1-hour retention)
- 🚫 No tracking or analytics

---

## 🎬 Demo

### Live Demo
[Coming Soon] <!-- Add your deployment URL here -->

### Quick Start
```bash
# Clone the repository
git clone https://github.com/yourusername/video-downloader.git

# Navigate to the project
cd video-downloader

# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py
```

Visit `http://localhost:5000` in your browser!

---

## 📸 Screenshots

<div align="center">

### Home Page
![Home Page](<img width="1302" height="994" alt="Screenshot 2025-12-18 215545" src="https://github.com/user-attachments/assets/f38fbec7-e30e-441c-828b-3c0258bd6f9c" />
)

### Download Process
![Download Process](<img width="1428" height="875" alt="image" src="https://github.com/user-attachments/assets/b914bb16-67c4-477c-808d-b710c6508dea" />
)

### Mobile View
<img src="screenshots/mobile.png" width="300" alt="Mobile View">

</div>

---

## 🛠️ Tech Stack

### Backend
- **Python 3.8+** - Core programming language
- **Flask 2.0+** - Web framework
- **BeautifulSoup4** - HTML parsing
- **Requests** - HTTP library
- **fake-useragent** - User agent rotation

### Frontend
- **HTML5** - Markup language
- **CSS3** - Styling with custom properties
- **JavaScript (ES6+)** - Interactive functionality
- **Font Awesome 6.4.0** - Icons
- **Google Fonts (Poppins)** - Typography

### Features
- Context managers for resource handling
- Async download processing
- Thread-based file cleanup
- Custom exception handling
- RESTful API design

---

## 📦 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/video-downloader.git
   cd video-downloader
   ```

2. **Create Virtual Environment** (Recommended)
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create Required Directories**
   ```bash
   mkdir downloads
   mkdir moduls
   ```

5. **Run the Application**
   ```bash
   python app.py
   ```

6. **Access the Application**
   Open your browser and navigate to:
   ```
   http://localhost:5000
   ```

---

## 🎯 Usage

### Web Interface

1. **Open the Application**
   - Navigate to `http://localhost:5000` in your web browser

2. **Enter Video URL**
   - Paste a YouTube, Facebook, or Instagram video URL into the input field
   - The platform will be automatically detected

3. **Download Video**
   - Click the "Download" button
   - Wait for the video to be processed
   - Click "Download File" to save the video to your device

### Supported URL Formats

#### YouTube
```
https://www.youtube.com/watch?v=VIDEO_ID
https://youtu.be/VIDEO_ID
https://www.youtube.com/shorts/VIDEO_ID
https://www.youtube.com/embed/VIDEO_ID
```

#### Facebook
```
https://www.facebook.com/username/videos/VIDEO_ID
https://fb.watch/VIDEO_ID
```

#### Instagram
```
https://www.instagram.com/p/POST_ID/
https://www.instagram.com/reel/REEL_ID/
```

### Keyboard Shortcuts

- **Ctrl/Cmd + V**: Focus on URL input
- **Enter**: Submit download (when input is focused)
- **Escape**: Clear input and hide messages

---

## 📚 API Documentation

Detailed API documentation is available in [API.md](API.md)

### Quick Reference

#### Get Video Information
```http
POST /api/get-info
Content-Type: application/json

{
  "url": "https://www.youtube.com/watch?v=VIDEO_ID"
}
```

#### Download Video
```http
POST /api/download
Content-Type: application/json

{
  "url": "https://www.youtube.com/watch?v=VIDEO_ID"
}
```

#### Download File
```http
GET /api/download-file/{filename}
```

For complete API documentation, see [API.md](API.md)

---

## 📁 Project Structure

```
video-downloader/
│
├── app.py                      # Main Flask application
├── requirements.txt            # Python dependencies
├── README.md                   # This file
├── API.md                      # API documentation
│
├── moduls/                     # Custom modules
│   ├── __init__.py
│   ├── utlitis.py             # Downloader class and utilities
│   ├── expection.py           # Custom exceptions
│   └── parsing.py             # URL parsing and headers
│
├── templates/                  # HTML templates
│   └── index.html             # Main page template
│
├── static/                     # Static files
│   ├── css/
│   │   └── style.css          # Main stylesheet
│   └── js/
│       └── main.js            # JavaScript functionality
│
├── downloads/                  # Temporary download storage
│   └── .gitkeep
│
└── screenshots/                # Screenshots for documentation
    ├── home.png
    ├── download.png
    └── mobile.png
```

---

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Flask Configuration
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your-secret-key-here

# Server Configuration
HOST=0.0.0.0
PORT=5000

# Upload Configuration
UPLOAD_FOLDER=downloads
MAX_CONTENT_LENGTH=524288000  # 500MB in bytes

# Cleanup Configuration
CLEANUP_INTERVAL=3600  # 1 hour in seconds
FILE_RETENTION=3600    # 1 hour in seconds
```

### Application Settings

Edit `app.py` to customize:

```python
app.config['UPLOAD_FOLDER'] = 'downloads'
app.config['MAX_CONTENT_LENGTH'] = 500 * 1024 * 1024  # 500MB max
```

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the Repository**
   ```bash
   git fork https://github.com/yourusername/video-downloader.git
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Commit Your Changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```

4. **Push to the Branch**
   ```bash
   git push origin feature/AmazingFeature
   ```

5. **Open a Pull Request**

### Contribution Guidelines

- Follow PEP 8 style guide for Python code
- Use meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

---

## 🐛 Known Issues

- YouTube downloads may occasionally fail due to API changes
- Facebook videos with age restrictions may not be downloadable
- Instagram private account videos cannot be downloaded

For a complete list of issues and feature requests, visit our [Issues Page](https://github.com/yourusername/video-downloader/issues)

---

## 🗺️ Roadmap

### Version 1.1 (Coming Soon)
- [ ] Download quality selection
- [ ] Batch download support
- [ ] Download history
- [ ] User preferences

### Version 1.2
- [ ] TikTok support
- [ ] Twitter/X video support
- [ ] Audio-only download option
- [ ] Subtitle download

### Version 2.0
- [ ] User authentication
- [ ] Cloud storage integration
- [ ] Video format conversion
- [ ] Scheduled downloads

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ⚠️ Disclaimer

This tool is for educational purposes only. Please respect copyright laws and the terms of service of the platforms you're downloading from. Only download content you have permission to download.

---

## 🙏 Acknowledgments

- [Flask](https://flask.palletsprojects.com/) - The web framework used
- [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/) - HTML parsing
- [Font Awesome](https://fontawesome.com/) - Icons
- [Google Fonts](https://fonts.google.com/) - Poppins font family
- All contributors who have helped with code, bug reports, and suggestions

---

## 📞 Contact

**Your Name** - [@yourusername](https://twitter.com/yourusername)

**Project Link**: [https://github.com/yourusername/video-downloader](https://github.com/yourusername/video-downloader)

**Email**: your.email@example.com

---

## 💖 Support

If you found this project helpful, please consider:

- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting new features
- 🔀 Contributing to the code

---

<div align="center">

**Made with ❤️ by [Your Name](https://github.com/yourusername)**

[![GitHub followers](https://img.shields.io/github/followers/yourusername?style=social)](https://github.com/yourusername)
[![Twitter Follow](https://img.shields.io/twitter/follow/yourusername?style=social)](https://twitter.com/yourusername)

</div>
