<template>
  
  <div class="day">
    <p>Mon</p>
    <div class="pillar" style="height: 20%" ></div>
    <div class="amount"><p>$69</p></div>
  </div>
  
</template>

<style>
  .day {
    height: 100%;
    width: 10%;

    color: hsl(28, 10%, 53%);
    text-align: center;

    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    gap: 5%
}

.day > * {
    transition-duration: 0.2s;
}

.day p {
    margin: 0;
}

.day:hover .amount {
    opacity: 1;
}

.day:hover .pillar {
    opacity: 80%;
}

.amount {
    width: 150%;
    height: 20%;

    opacity: 0;

    background-color: hsl(25, 47%, 15%);
    border-radius: 5px;

    color: white;

    display: flex;
    align-items: center;
    justify-content: space-around;
}

.pillar {
    background-color: hsl(10, 79%, 65%);
    border-radius: 5px;

    width: 100%;
    height: 60%;
}

.largest {
    background-color: hsl(186, 34%, 60%);
}

#total {
    height: 25%;
    border-top: 3px solid hsl(27, 66%, 92%);

    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>