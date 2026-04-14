<div style="text-align: center; font-family: 'Fira Code', monospace; font-size: 36px; color: #39FF14; line-height: 1.2; min-height: 50px; display: flex; align-items: center; justify-content: center; flex-direction: column;">
  <div id="typing-text"></div>
  <style>
    @media (max-width: 768px) {
      div[style*="text-align: center"] {
        font-size: 24px;
      }
    }
  </style>
  <script>
    const texts = [
      "Sérgio Servilha de Oliveira Filho",
      "Data Scientist 🔬",
      "ML Researcher 🔍",
      "Deep Learning Expert 🧠",
      "Applied Research Scientist 🚀"
    ];
    let currentTextIndex = 0;
    let currentCharIndex = 0;
    let isErasing = false;
    const typingSpeed = 75; // ms per character
    const erasingSpeed = 75; // ms per character
    const pauseTime = 2000; // ms
    const element = document.getElementById('typing-text');

    function typeWriter() {
      const currentText = texts[currentTextIndex];
      if (!isErasing) {
        element.textContent = currentText.substring(0, currentCharIndex + 1);
        currentCharIndex++;
        if (currentCharIndex === currentText.length) {
          isErasing = true;
          setTimeout(typeWriter, pauseTime);
          return;
        }
      } else {
        element.textContent = currentText.substring(0, currentCharIndex);
        currentCharIndex--;
        if (currentCharIndex < 0) {
          isErasing = false;
          currentTextIndex = (currentTextIndex + 1) % texts.length;
        }
      }
      setTimeout(typeWriter, isErasing ? erasingSpeed : typingSpeed);
    }

    typeWriter();
  </script>
</div>
# 🚀 Tech Stack

## 💻 Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)

## 🎨 Frameworks & Libraries
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)

## 🎯 Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

## 🕷️ Scraping & Automation Arsenal
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Scrapy](https://img.shields.io/badge/Scrapy-1C5E2E?style=for-the-badge&logo=scrapy&logoColor=white)
![Beautiful Soup](https://img.shields.io/badge/Beautiful%20Soup-FFD43B?style=for-the-badge&logo=python&logoColor=black)
![Requests](https://img.shields.io/badge/Requests-2C3E50?style=for-the-badge&logo=python&logoColor=white)

### Specialties:
- 📊 Data extraction & ETL pipelines
- ⏰ Scheduled scraping jobs
- ⚡ High-speed concurrent scraping

## 🤖 AI & Machine Learning
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit%20learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)

### Focus Areas:
- 📈 Classification & prediction models
