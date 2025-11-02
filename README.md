<!DOCTYPE html>
<html>
    <head>
    <title> Calculator.html </title>
    </head>

    <body>
        <style>

    /*Fundal*/
    body{
background-color: black ;
font-family: Arial;
color: white;
font-size: 30px;

    }

        /*Fundal BUTOANE gray*/
.backColor{

background-color:rgb(51, 51, 51);;
border-radius: 50px;
color: white;
size: 100px;
border: gray;   
height: 60px;
width: 60px;
margin-right: 3px;
font-size: 25px;
margin-bottom: 1px;
cursor: pointer;

}

        /*Fundal BUTOANE Orange*/


.orange-button{
background-color: orange;
border-radius: 50px;
color: white;
size: 100px;
border: orange;   
height: 60px;
width: 60px;
margin-right: 3px;
font-size: 25px;
margin-bottom: 1px;
cursor: pointer;

}

        /*Fundal BUTOANE Clear*/

.clear-button{

background-color:rgb(51, 51, 51);;
border-radius: 50px;
color: white;
size: 100px;
border: gray;   
height: 60px;
width: 60px;
margin-right: 5px;
font-size: 18px;
margin-bottom: 1px;
cursor: pointer;


}

        </style>



<p class="js-display"></p>

        <p>
<button onclick="

updateCalculation('1');

    " class="backColor"> 1 </button>

<button onclick="

updateCalculation('2');


" class="backColor"> 2 </button>

<button onclick="
 updateCalculation('3');

" class="backColor"> 3 </button>

<button onclick="

updateCalculation('+');

"class="orange-button"> + </button>
        </p>

        <p>
<button onclick="
    
    updateCalculation('4');

    " class="backColor"> 4 </button>
<button onclick="

updateCalculation('5');

"class="backColor"> 5 </button>
<button onclick="

updateCalculation('6');


"class="backColor"> 6 </button>
<button onclick="

updateCalculation('-');

" class="orange-button"> - </button> 
        </p>

         <p>
<button onclick="

    updateCalculation('7');

    
    " class="backColor"> 7 </button>
<button onclick="


updateCalculation('8');

" class="backColor"> 8 </button>
<button onclick="


updateCalculation('9');

" class="backColor"> 9 </button>
<button onclick="

updateCalculation('*');

" class="orange-button"> * </button>
        </p>

        <p>
<button onclick="

    updateCalculation('0');

    
    "class="backColor"> 0 </button>
<button onclick="

updateCalculation('.');

" class="backColor"> . </button>

<button onclick="

updateCalculation('/');


" class="backColor"> / </button>

<button onclick="
calculation=eval(calculation);

displayCalculation();

localStorage.setItem('calculation', calculation);

" class="orange-button"> = </button>

        </p>

        <p>
<button onclick="
calculation = '' ;

displayCalculation();
    
    localStorage.setItem('calculation', calculation);
    " class="clear-button">Clear</button>
        </p>

    </body>

<script>
let calculation = localStorage.getItem ('calculation') || '';


function updateCalculation(value){
    calculation+=value;
    
    displayCalculation();

    localStorage.setItem('calculation' , calculation);


}

    function displayCalculation(){
document.querySelector('.js-display')
.innerHTML = calculation;
    }


</script>


</html>
