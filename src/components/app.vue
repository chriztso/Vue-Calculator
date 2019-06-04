<template>
  <div class = "whole">
    <div class = "display">
      <span class = "currentNumber">{{currentNumber}}</span>
    </div>
    <div class = "firstRow">
        <div id = "AC" v-on:click = 'clearNumbers'>
          <span class = "symbol">AC</span>
        </div> 
         <div id = "plusMinus">
          <span class = "symbol" v-on:click = 'changeSign'>+/-</span>
        </div> 
         <div id = "percentage">
          <span class = "symbol" v-on:click = 'makePercentage'>%</span>
        </div>  
        <div id = "divide">
          <span class = "symbol">÷</span>
        </div>    
    </div>       
    <div class = "secondRow">
        <div id = "seven">
          <span class = "symbol" v-on:click = 'getText' data-value='7'>7</span>
        </div> 
         <div id = "eight">
          <span class = "symbol" v-on:click = 'getText' data-value='8'>8</span>
        </div> 
         <div id = "nine">
          <span class = "symbol" v-on:click = 'getText' data-value='9'>9</span>
        </div>  
        <div id = "multiply">
          <span class = "symbol">x</span>
        </div>    
    </div> 
    <div class = "thirdRow">
        <div id = "four">
          <span class = "symbol" v-on:click = 'getText' data-value='4'>4</span>
        </div> 
         <div id = "five">
          <span class = "symbol" v-on:click = 'getText' data-value='5'>5</span>
        </div> 
         <div id = "six">
          <span class = "symbol" v-on:click = 'getText' data-value='6'>6 </span>
        </div>  
        <div id = "subtract">
          <span class = "symbol">-</span>
        </div>    
    </div>  
    <div class = "fourthRow">
        <div id = "three">
          <span class = "symbol" v-on:click = 'getText' data-value='3'>3</span>
        </div> 
         <div id = "two">
          <span class = "symbol" v-on:click = 'getText' data-value='2'>2</span>
        </div> 
         <div id = "one">
          <span class = "symbol" v-on:click = 'getText' data-value='1'>1</span>
        </div>  
        <div id = "add">
          <span class = "symbol" v-on:click = 'addNumber'>+</span>
        </div>    
    </div>  
    <div class = "lastRow">
        <div id = "zero">
          <span class = "symbol" v-on:click = 'getText' data-value='0'>0</span>
        </div> 
         <div id = "period">
          <span class = "symbol" v-on:click = 'getText' data-value='.'>.</span>
        </div> 
         <div id = "equal">
          <span class = "symbol">=</span>
        </div>  
    </div>            

  </div>
</template>

<script>
export default{
    data() {
        return {
            currentNumber: '', 
            result : ''
        }
    },
    methods: {
      getText(event){
        if(this.result[this.result.length-1] === '+'){
          this.currentNumber = '';
        }
        this.currentNumber += event.target.getAttribute('data-value');
        this.result += event.target.getAttribute('data-value');
      },
      clearNumbers(){
        this.currentNumber = '';
        this.result = '';
      },
      changeSign(){
        this.currentNumber *= -1;
      },
      makePercentage(){
        this.currentNumber /= 100;
      },
      addNumber(){
        if(this.result[this.result.length-1] !== '+'){
          this.result = eval(this.result);
          this.currentNumber = this.result;
        }
        this.result += '+';
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
    text-align: right;
}

.firstRow, .secondRow, .thirdRow, .fourthRow, .lastRow{
    display: flex;
    flex-direction: row;
    height: 52px;
}

.symbol{
    color: white;
    position: relative; 
    top: 30%;
}

#AC, #plusMinus, #percentage{
    background-color: rgb(71, 70, 71);
    width: 25%;
    text-align: center;
}

#seven, #eight, #nine, 
#four, #five, #six, #three, #two, #one, 
#period
{
    background-color: rgb(119, 117, 115);
    width: 25%;
    text-align: center;
}

#zero{
    background-color: rgb(119, 117, 115);
    width: 50%;
    text-align: center;
}

#divide, #multiply, #subtract, #add, #equal{
    background-color: rgb(246, 158, 31);
    width: 25%;
    text-align: center;
}

</style>