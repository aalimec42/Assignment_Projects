...html
     <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OTP🔢</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h3>OTP VERIFICATON</h3>
        <div class="inp">
            <input type="text" maxlength="1">
            <input type="text" maxlength="1">
            <input type="text" maxlength="1">
            <input type="text" maxlength="1">
        </div>
        <p>Don't get the code? <a href="">Resend</a></p>
        <button>Verify</button>
    </div>
    
    <script src="script.js"></script>
</body>
</html>

...css
     .container{
    width: 220px;
    height: 250px;
    color: rgb(162, 162, 183);
    background-color: rgb(51, 58, 135);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px;
    border-radius: 15px;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 100;
    
    
}

input{
   width: 25px;
   height: 25px;
   margin: 8px 3px;
   font-size: 18px;
   outline: none;
   border: 1px solid #ecf0f1;
   border-radius: 5px;
   text-align: center;
   color: bisque;
   background-color: transparent;

}

p,a{
    color: blanchedalmond;
    font-size: 12px;
}

button{
    width: 80px;
    font-weight: 600;
    border-radius: 20px;
    border: 2px solid rgb(246, 181, 82);
    color: blanchedalmond;
    background-color: transparent;
    padding: 5px;
    cursor: pointer;
    transition: 0.4 ease-in;
    margin-top: 10px;
    &:hover{
        background-color: blanchedalmond;
        color:rgb(51, 58, 135);
    }
}

...js
    let input=[...document.querySelectorAll('input')];
    console.log(input)
    input.forEach(element =>{
        element.addEventListener('keyup',()=>{
            if(input.indexOf(element)+1 != input.length){
                input[input.indexOf(element)+1].focus()
            }
        })
    });

