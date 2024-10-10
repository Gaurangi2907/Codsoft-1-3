<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator Project</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>I am a Calculator</h1>
        <div class="calculator">
            <div class="input"></div>
            <div class="result"></div>
            <ul class="btn_container">
                <li class="operator">(</li>
                <li class="num">7</li>
                <li class="num">4</li>
                <li class="num">1</li>
                <li class="clear">C</li>
                <li class="operator">)</li>
                <li class="num">8</li>
                <li class="num">5</li>
                <li class="num">2</li>
                <li class="num">0</li>
                <li class="del">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-delete"><path d="M21 4H8l-7 8 7 8h13a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2z"/><line x1="18" y1="9" x2="12" y2="15"/><line x1="12" y1="9" x2="18" y2="15"/></svg>
                </li>
                <li class="num">9</li>
                <li class="num">6</li>
                <li class="num">3</li>
                <li class="num">.</li>
                <li class="operator">/</li>
                <li class="operator">*</li>
                <li class="operator">-</li>
                <li class="operator">+</li>
                <li class="equal">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24" color="#ffffff" fill="none">
                        <path d="M4 8H20" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" />
                        <path d="M4 16H20" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" />
                    </svg>
                </li>
            </ul>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
.container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 48px;
    gap: 24px;
}

h1{
    font-weight: bold;
}

.calculator{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 10px;
    overflow: scroll;
    height: 800px;
    width: 600px;
    border-radius: 24px;
    background-color: #171717;
    color:aliceblue;
}

ul{
    display: grid;
    list-style: none;
    grid-template-rows: repeat(5,minmax(0,1fr));
    grid-auto-flow: column;
    row-gap:20px;
    column-gap: 48px;
    padding-top: 12px;
    padding-bottom: 12px;
}

li{
    height: 96px;
    width: 96px;
    border-radius: 9999px;
    display: flex;
    cursor: pointer;
    font-size: 30px;
    align-items: center;
    justify-content: center;
}

.num,.clear{
    background-color: #52525b;
}

.operator,.del{
    background-color: #27272a;
}

.equal{
    background-color: rgb(255,159,10);
}

.input,.result{
    display: flex;
    align-items: flex-end;
    justify-content: flex-end;
    height: 50%;
    padding: 8px;
    font-size: 30px;
    border-radius: 24px;
    width: 100%;
}

.input{
    color: #737373;
    overflow: scroll;
}
let equation = document.querySelector(".input")
let result = document.querySelector(".result")
let button = document.querySelector(".btn_container")

button.addEventListener("click", e=>{
    if(e.target.classList.contains('num')){

       equation.innerHTML = equation.innerHTML + e.target.innerHTML
    }
    else if(e.target.classList.contains('operator')){
        equation.innerHTML = equation.innerHTML + e.target.innerHTML
    }
    else if(e.target.classList.contains('del')){
        equation.innerHTML = equation.innerHTML.slice(0,-1)
    }
    else if(e.target.classList.contains('equal')){
        result.innerHTML = ""
        result.innerHTML = result.innerHTML + eval(equation.innerHTML)
    }
    else if(e.target.classList.contains('clear')){
        result.innerHTML = ""
        equation.innerHTML = ""
    }
})
