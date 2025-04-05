# calculator_project
MAKING A CALCULATOR USING HTML AND CSS
#2ND YEAR PROJECT.
IMAGE:
![calcu](https://github.com/user-attachments/assets/841ec7d7-ef64-4328-aee6-6b80ba4f4ea6)

![calcu2](https://github.com/user-attachments/assets/7d7d194d-0d37-4efa-93cf-5e05940017c0)

 HTML CODE:
 ______________________________________________________________________
 <div class="container">
    <div class="calculator">
        <link rel="stylesheet" href="calcu.css">
        <form>
            <div class="display">
                <input type="text" name="display" disabled>
            </div>
            <div>
                <input type="button" value="AC" onclick="display.value =''" class="ac">
                <input type="button" class="del" value="Del" onclick="display.value =display.value.toString().slice (0,-1)">
                <input type="button" class="symbols" value="." onclick="display.value +='.'">
                <input type="button" class="symbols" value="/" onclick="display.value +='/'">
            </div>
            <div>
                <input type="button" class="NumpadBtns" value="7" onclick="display.value +='7'">
                <input type="button" class="NumpadBtns" value="8" onclick="display.value +='8'">
                <input type="button" class="NumpadBtns" value="9" onclick="display.value +='9'">
                <input type="button" class="symbols" value="*" onclick="display.value +='*'">
            </div>
            <div>
                <input type="button" class="NumpadBtns" value="4" onclick="display.value +='4'">
                <input type="button" class="NumpadBtns" value="5" onclick="display.value +='5'">
                <input type="button" class="NumpadBtns" value="6" onclick="display.value +='6'">
                <input type="button" class="symbols" value="-" onclick="display.value +='-'">
            </div>
            <div>
                <input type="button" class="NumpadBtns" value="1" onclick="display.value +='1'">
                <input type="button" class="NumpadBtns" value="2" onclick="display.value +='2'">
                <input type="button" class="NumpadBtns" value="3" onclick="display.value +='3'">
                <input type="button" class="symbols" value="+" onclick="display.value +='+'">
            </div>
            <div>
                <input type="button" class="special" value="00" onclick="display.value +='00'">
                <input type="button" class="special" value="0" onclick="display.value += '0'">
                <input type="button" value="=" onclick="display.value = eval(display.value)" class="equal">
            </div>
        </form>
    </div>
</div>


CSS CODE:
_____________________________________________________________________________
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400;500;600;700;800;900;1000&display=swap');
*{
    margin: 0px;
    padding:0px;
    font-family: Arial, Helvetica, sans-serif;
    box-sizing: border-box;
    user-select: none;
}
body{
    height:100vh;
    Background: #240046;
    display:grid;
}
.container{
    width: 100%;
    
    height: 100%;

    display: flex;
}
.calculator{
    background: #023e7d;
    padding: 10px;
    box-shadow: 0px 0px 10px 3px rgba(0, 0, 0, 0.219);
    margin:auto;

    border-radius: 10px;
}

.calculator form input {
    border: 0;
    outline: 0;
    width: 60px;
    height:60px;
    border-radius: 10px;
    font-family: Nunito;
    font-weight: 700;
    font-size:1.7em;
    color: white;
    cursor: pointer;
    margin: 10px;

}
.calculator form input.NumpadBtns{
    background: #012a4a;
}
form .display{
    display: flex;
    justify-content: flex-end;
    margin: 20px 0;
}
form .display input{
    text-align: right;
    flex: 2;
    font-size: 45px;
    box-shadow: none;
    padding:20px;
    box-sizing: border-box;
    background: #218380; 
    box-shadow: 0 0 10px 3px #00000033;
    height:80px;
    color: white;
}

form input.equal{
width: 145px;
background: #005f08
}
form input.ac,form input.del{
    background: #5f0000
}

.symbols{
    background-color: #edae49;
}
.special{
    background: #248277;
}

.calculator form input:hover {
    box-shadow: 0px 0px 5px 3px #00000025;
}

