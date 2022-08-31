<template>
  <p v-if="isMorning" class='saludo-paragraph'>Buen día</p>
  <p v-if="isAfternoon" class='saludo-paragraph'>Buenas tardes</p>
  <p v-if="isEvening" class='saludo-paragraph' v-text="saludoNoche"></p>
  <p v-show="isMorning" class='saludo-paragraph'>Buen día</p>

  <div v-html="html"></div>

  <ul>
    <li v-for="(fruta,index) in frutas" v-bind:key="index">{{fruta}}</li>
  </ul>
  <input type="text" v-bind:placeholder="placeHolder">
</template>

<script>


const date = new Date().getHours();
console.log(date);


export default {
    name:'Saludo',
    data: ()=>{
        return {
            isMorning: date < 12 && date >= 6,
            isAfternoon: date>=12 && date < 18,
            isEvening: date >= 18 || (date >= 0 && date < 6),
            saludoNoche: 'Buenas noches',
            html:'<p class="saludo-paragraph"> Este es un párrafo ingresado por v-html </p>',
            frutas:['🍌','🍍','🍓','🍑','🍐','🍏','🍈','🍎'],
            placeHolder:'Mi vieja mula ya no es lo que era'
        }
    }
}
</script>

<style>
    .saludo-paragraph{
        text-align: center;
        margin: 0px auto;
        padding: 10px 15px;
        border: 1px solid whitesmoke;
    }
</style>