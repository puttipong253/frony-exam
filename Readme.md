--- CSS ---

1.font-family: 'Roboto', sans-serif;

2. #red-box {
        background-color: red;
        border: 1px solid green;
        width: 200px;
        height: 200px;
        margin: auto;
   }
3. @media screen and (min-width: 512px){
   #response-box, body {
   width: 100%;
   height: 100%;
   background-color: green;
   }
   }
   @media screen and (min-width: 720px){
   #response-box, body {
   width: 100%;
   height: 100%;
   background-color: purple;
   }
   }
   @media screen and (min-width: 1024px){
   #response-box, body {
   width: 100%;
   height: 100%;
   background-color: skyblue;
   }
   }
4. #bg-box {
        width: 300px;
        height: 300px;
        background-image: url("bg.jpg");
   }
5. #blue-circle {
        width: 300px;
        height: 300px;
        background-color: skyblue;
        border-radius: 100%;
        position: absolute;
        animation-name: circle;
        animation-duration: 4s;
        animation-iteration-count: infinite;
   }

   @keyframes circle {
   0% {
   left: 0;
   transform: translateX(0);
   }
   50% {
   left: 100%;
   transform: translateX(-100%);
   }
   100% {
   left: 0;
   transform: translateX(0);
   }
   }
6. #gradient-btn {
        width: 200px;
        height: 60px;
        border-radius: 10px;
        border: none;
        background-image: linear-gradient(90deg, #f6b144, #e69220)
   }
7. #fade-btn {
        width: 200px;
        height: 60px;
        border-radius: 10px;
        border: none;
        background-color: red;
        transition: all .8s ease-in;
   }
   #fade-btn:hover {
        background-color: white;
   }
8. #red-box {
        width: 200px;
        height: 100px;
        border-radius: 10px;
        border: none;
        background-color: red;
        transition: all .8s ease-in;
   }
   #red-box:hover {
        width: 400px;
        height: 200px;
   }
9. #flex-container {
        display: flex;
        background-color: lightskyblue;
        width: 900px;
        height: 750px;
   }
   #green-box {
        align-self: start;
        width: 300px;
        height: 250px;
        background-color: green;
   }
   #red-box {
        align-self: center;
        width: 300px;
        height: 250px;
        background-color: red;
   }
   #blue-box {
        align-self: end;
        width: 300px;
        height: 250px;
        background-color: blue;
   }
10. div ที่อยู่ภายใต้ parent จะถูก style ของ parent ครอบทั้งหมด เพราะฉะนั้นขนาด font ของ child จะเท่ากับของ parent 

--- JAVASCRIPT ---

1. document.getElementById("mylist")
2. function onClick() {
        document.getElementById("box").style.border = "2px solid green";
        document.getElementById("box").style.backgroundColor = "red";
        document.getElementById("box").style.opacity = "0.7";
        document.getElementById("box").style.width = "100px";
        document.getElementById("box").style.height = "100px";
   }
3. <input id="inputName" type="text" value=""/>
   <p id="name"></p>
   <button onclick="onClick()">click</button>
   
   function onClick() {
     var a = document.getElementById("inputName").value;
     document.getElementById("name").innerHTML = a;
   }
4. <input id="inputAge1" type="checkbox" value="20"/>
   <input id="inputAge2" type="radio" value="10"/>
   <p id="age1"></p>
   <p id="age2"></p>
   <button onclick="onClick()">click</button>
   
   function onClick() {
     var a = document.getElementById("inputAge1").value;
     document.getElementById("age1").innerHTML = a;

     var b = document.getElementById("inputAge2").value;
     document.getElementById("age2").innerHTML = b;
   }
5. <select id="number" >
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
    <option value="4">4</option>
   </select>
   <button onclick="onClick()">Try it</button>
   <p id="name"></p>

   function onClick() {
     var a = document.getElementById("number").value;
     document.getElementById("name").innerHTML = a;
   }
6. class Cal {
   constructor(price, amount, discount) {
   this.price = price;
   this.amount = amount;
   this.discount = discount
   }
   setPrice(value){
   this.price = value
   }
   setAmount(value){
   this.amount = value
   }
   setDiscount(value){
   this.discount = value
   }
   summary(){
   return (this.amount * this.price) - this.discount
   }
   }
   const calculate = new Cal();

   calculate.setPrice(5)
   calculate.setAmount(2)
   calculate.setDiscount(3)
   calculate.summary()
7. <div id="love-message"></div>

   var myVar = setTimeout(function(){
   document.getElementById("love-message").innerHTML = 'I LOVE YOU'
   }, 8000);

   
   