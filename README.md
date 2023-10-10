# Text-To-Speech-Converter-Web-Application
A Beautiful Web Application Which Convert Your Text into Speech .  
### HTML
```Html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text To Speach Converter</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">
        <h2>Text To Speech</h2>
        <div class="area">
            <label for="">Enter Text</label>
            <textarea role="10" cols="10" name="" id="in-text" placeholder="Enter Your Text.."></textarea>
        </div>
        <div class="voice-select">
            <h3>Select Voice </h3>
            <select>
                <option value="">Microsoft Zira</option>
                <option value="">Microsoft Marks</option>
                <option value="">Microsoft Hazel</option>
                <option value="">Microsoft Susan</option>
                <option value="">Microsoft David</option>
                <option value="">Microsoft George</option>
            </select>
        </div>
        <button type="button" id="btn">Convert</button>
    </div>


    <script src="script.js"></script>
</body>

</html>
```
### CSS
```CSS
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'poppins', sans-serif;
}

body {

    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #575151;
}

.container {
    background: transparent;
    width: 400px;
    height: 390px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    box-shadow: inset 0 0 60px whitesmoke,
        inset 20px 0 80px #f0f,
        inset -20px 0 80px #0ff,
        inset 20px 0 300px #f0f,
        inset -20px 0 300px #0ff,
        0 0 50px #fff,
        -10px 0 80px #f0f,
        10px 0 80px #0ff;
    border-radius: 50px;
}

.container h2 {
    text-align: center;
    color: #fff;
    margin-bottom: 12px;
}

.container .area {
    display: flex;
    flex-direction: column;
    padding: 0 8px;
}

.container .area label {
    font-weight: 500;
    font-size: 18px;
}

.container .area textarea {
    height: 150px;
    border: none;
    resize: none;
    padding: 4px;
    margin: 9px 0;
    outline: none;
    background: rgba(0, 0, 0, 0.2);
    color: #fff;
    font-size: 16px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.5);
}

::placeholder {
    color: #fff;
}

.container .voice-select {
    display: flex;
    flex-direction: column;
    padding: 0 14px;
}

.container .voice-select h3 {
    font-weight: 500;
}

.container .voice-select select {
    width: 220px;
    padding: 4px 0;
    margin-bottom: 10px;
    box-shadow: 0 0 4px #00b3b9;
    border: none;
    outline: none;
}

#btn {
    width: 75%;
    margin: 2px auto;
    padding: 7px 0;
    outline: none;
    border: none;
    background: transparent;
    background: transparent;
    background: linear-gradient(45deg, rgba(255, 0, 255, 0.363), rgba(0, 255, 255, 0.363));
    font-size: 16px;
    color: #fff;
    border-radius: 4px;
    cursor: pointer;
    transition: 0.3s ease;

}

#btn:hover {
    box-shadow: inset 0 0 60px whitesmoke,
        inset 20px 0 80px #f0f,
        inset -20px 0 80px #0ff,
        inset 20px 0 300px #f0f,
        inset -20px 0 300px #0ff,
        0 0 50px #fff,
        -10px 0 80px #f0f,
        10px 0 80px #0ff;
    color: #00093a;
    transform: scale(1.01);
}
```
```Javascript
const textarea = document.querySelector("textarea");
const btn = document.querySelector("#btn");
let synt = speechSynthesis;
function textToSpeach(text) {
    let utternance = new SpeechSynthesisUtterance(text);
    synt.speak(utternance);
}

btn.addEventListener("click", (e) => {
    if (textarea.value !== "") {
        textToSpeach(textarea.value);
    }
    else {
        textToSpeach("Please Enter Some Text First"); u7u
    }
})
//working only one default voice
```





