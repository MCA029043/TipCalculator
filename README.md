
# Tip-Calculator

This is a simple HTML and JavaScript code that allows the user to Calculate Tip .

## Step 1: Create the HTML file

The HTML file is responsible for creating the user interface and loading the JavaScript file.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tip Calculator</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
       
      <div class="area">
        <h1>Charles' Tip calculator!</h1>
        <h2 style="margin-left: 20px;">How much was your bill?</h2>
        <div style="margin-left: 20px;">Rs. <input type="text" id="billAmount" /></div>
        <h2 class="h2">How was your service?</h2>
        <div style="margin-left: 20px;">
        <select id="ddlViewBy">
            <option value="0" disabled="" selected="" >Choose an Option</option>
            <option value=".3">30% Outstanding</option>
            <option value=".2">20% Good</option>
            <option value=".15">15% It was Okay</option>
            <option value=".10">10% Bad</option>
            <option value=".05">5% Terrible</option>
          </select>
          </div>
        <h2 class="h2">How many people are sharing the bill?</h2>
        <div style="margin-left: 20px;"> <input type="text" id="totalPeople" />People</div>
        <button id="calculate">Calculate</button>
      </div>
   
    </div>
    <script src="script.js"></script>
  </body>
</html>

```

## Step 2: Create the JavaScript file

The JavaScript file is responsible for getting the keyword from the user and then displaying it on the screen.

```javascript
let container = document.querySelector(".area");
let calculate = document.querySelector("#calculate");
let div = document.createElement("p");
calculate.addEventListener("click",()=>{
    div.innerText =""
    let amount=document.querySelector('#billAmount').value;
    let totalPeople = document.getElementById("totalPeople").value;
    var service = document.getElementById("ddlViewBy").value;
    div.innerText = ` Tip Amount is ${amount*service/totalPeople}`
    container.appendChild(div);

   
})
```

## Step 3: Run the code

To run the code, open the HTML file in a web browser.

## Conclusion

This is a simple example of how User can calculate Tip according to service. This code can be used as a starting point for more complex projects.
