<template>
  <div class = "whole">
    <div class = "display">
      <span class = "currentNumber">{{currentNumber}}</span>
    </div>
    <div>
        1
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
    height: 80px;
    font-size: 60px;
}

.currentNumber{
    position: relative;
    left: 210px;
}
</style>