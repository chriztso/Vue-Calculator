<template>
  <div class = "whole">
    <div class = "display">
      <span class = "currentNumber">{{currentNumber}}</span>
    </div>
    <div class = "firstRow">
        <div id = "AC">
          <span class = "symbol">AC</span>
        </div> 
         <div id = "plusMinus">
          <span class = "symbol">+/-</span>
        </div> 
         <div id = "percentage">
          <span class = "symbol">%</span>
        </div>  
        <div id = "divide">
          <span class = "symbol">÷</span>
        </div>    
    </div>       
    <div class = "secondRow">
        <div id = "seven">
          <span class = "symbol">7</span>
        </div> 
         <div id = "eight">
          <span class = "symbol">8</span>
        </div> 
         <div id = "nine">
          <span class = "symbol">9</span>
        </div>  
        <div id = "multiply">
          <span class = "symbol">x</span>
        </div>    
    </div> 
     <div class = "thirdRow">
        <div id = "four">
          <span class = "symbol">4</span>
        </div> 
         <div id = "five">
          <span class = "symbol">5</span>
        </div> 
         <div id = "six">
          <span class = "symbol">6</span>
        </div>  
        <div id = "subtract">
          <span class = "symbol">-</span>
        </div>    
    </div>            

  </div>
</template>

<script>
export default{
    data() {
        return {
            currentNumber: '0'
        }
    }
}
</script>


<style>
.whole{
    border: 1px solid black; 
    border-radius: 4px;
    margin: 0 auto;
    width: 250px;
    height: 350px;
}

.display{
    background-color:rgb(92,91,92);
    color: white;
    height: 88px;
    font-size: 60px;
}

.currentNumber{
    position: relative;
    left: 210px;
}

.firstRow, .secondRow, .thirdRow{
    display: flex;
    flex-direction: row;
    height: 52px;
}


.symbol{
    color: white;
    position: relative; 
    top: 30%;
}

#AC, #plusMinus, #percentage, #seven, #eight, #nine, 
#four, #five, #six
{
    background-color: rgb(71, 70, 71);
    width: 25%;
    text-align: center;
}

#divide, #multiply, #subtract{
    background-color: rgb(246, 158, 31);
    width: 25%;
    text-align: center;
}

</style>