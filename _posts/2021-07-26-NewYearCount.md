---
title: New Years Counter
categories: [dev]
comments: true
---


### 2학년 1학기 '웹클라이언트컴퓨팅'수업 (이지영prof)

# 새해가 얼마 남았는지 카운트다운하는 프로그램

### ▽Code review▽

▼HTML
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>PROJECT NewYear</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    
    <h1> New Year is coming! :) </h1>

    <div class = "countdown-container">
        <div class="time">
            <h1 id="days">00</h1>
            <small>days</small>
        </div>
        <div class="time">
            <h1 id="hours">00</h1>
            <small>hours</small>
        </div>
        <div class="time">
            <h1 id="minutes">00</h1>
            <small>minutes</small>
        </div>
        <div class="time">
            <h1 id="seconds">00</h1>
            <small>seconds</small>
        </div>
    </div>

    <script src="./script.js"></script>
    
</body>
</html>
```

▼JAVA SCRIPT
```js
const body = document.body;
const endTime = new Date('December 31 2021 23:59:59');
const daysEl = document.getElementById('days');
const hoursEl = document.getElementById('hours');
const minutesEl = document.getElementById('minutes');
const secondsEl = document.getElementById('seconds'); 

setInterval(updateCountdown, 1000)
setInterval(createSnowFlake, 100); 

function updateCountdown() {
    const startTime = new Date();
    const diff = endTime - startTime;
    const days = Math.floor(diff / 1000 / 60 / 60 / 24);
    const hours = Math.floor(diff / 1000 / 60 / 60) % 24;
    const minutes = Math.floor(diff / 1000 / 60) % 60;
    const seconds = Math.floor(diff / 1000) % 60;
    daysEl.innerHTML = days;
    hoursEl.innerHTML = hours < 10 ? '0'+hours : hours;
    minutesEl.innerHTML = minutes < 10 ? '0'+minutes : minutes;
    secondsEl.innerHTML = seconds < 10 ? '0'+seconds : seconds;
}

function createSnowFlake() {
    const snow_flake = document.createElement('i');
    snow_flake.classList.add('fas');
    snow_flake.classList.add('fa-snowflake');
    snow_flake.style.left = Math.random() * window.innerWidth + 'px';
    snow_flake.style.animationDuration = Math.random() * 3 + 2 + 's';
    snow_flake.style.opacity = Math.random();
    snow_flake.style.fontSize = Math.random() * 10 + 10 + 'px';

    document.body.appendChild(snow_flake);

    setTimeout(() => {
        snow_flake.remove();
    }, 5000); 
}
```

▼CSS
```css
@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.10.2/css/all.min.css');

* {
    box-sizing: border-box;
}

body {
    background-color: #323975;
    color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-family: 'Muli', sans-serif;
    height:100vh;
    overflow: hidden;
    margin: 0;
    text-align: center;
}

.fa-snowflake {
    color: #fff;
    position: absolute;
    top: -20px;
    animation: fall linear forwards; 
}

@keyframes fall {
    to {
        transform: translateY(105vh); 
    }
}

.countdown-container {
    display: flex;
}

.time {
    display: flex;
    font-size: 1.2em;
    flex-direction: column;
    margin: 0 15px;
}

.time h1 {
    margin-bottom: 0;
}

.time small{
    color: #ccc; 
}
```

