<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Typewriter Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #000;
            font-family: monospace;
            color: #39FF14;
        }
        svg {
            width: 100%;
            max-width: 800px;
            height: auto;
        }
        text {
            font-size: 36px;
            fill: #39FF14;
        }
        .cursor {
            animation: blink 1s infinite;
        }
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }
        @media (max-width: 768px) {
            text {
                font-size: 24px;
            }
        }
    </style>
</head>
<body>
    <svg viewBox="0 0 800 100">
        <text id="typewriter-text" x="50%" y="50%" text-anchor="middle" dominant-baseline="middle"></text>
    </svg>

    <script>
        const texts = [
            "Sérgio Servilha de Oliveira Filho",
            "Data Scientist 🔬",
            "ML Researcher 🔍",
            "Deep Learning Expert 🧠",
            "Applied Research Scientist 🚀"
        ];
        const textElement = document.getElementById('typewriter-text');
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingSpeed = 100;
        const deletingSpeed = 50;
        const pauseTime = 2000;

        function typeWriter() {
            const currentText = texts[textIndex];
            if (!isDeleting) {
                textElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
                if (charIndex === currentText.length) {
                    isDeleting = true;
                    setTimeout(typeWriter, pauseTime);
                    return;
                }
            } else {
                textElement.textContent = currentText.substring(0, charIndex);
                charIndex--;
                if (charIndex < 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                    setTimeout(typeWriter, 500);
                    return;
                }
            }
            setTimeout(typeWriter, isDeleting ? deletingSpeed : typingSpeed);
        }

        // Add blinking cursor
        function addCursor() {
            const cursor = document.createElementNS('http://www.w3.org/2000/svg', 'text');
            cursor.setAttribute('x', '50%');
            cursor.setAttribute('y', '50%');
            cursor.setAttribute('text-anchor', 'middle');
            cursor.setAttribute('dominant-baseline', 'middle');
            cursor.setAttribute('class', 'cursor');
            cursor.textContent = '|';
            textElement.parentNode.appendChild(cursor);
        }

        addCursor();
        typeWriter();
    </script>
</body>
</html>
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
