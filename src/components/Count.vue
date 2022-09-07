<template>  
    <h1 class="count-title">Contador App</h1>

    <div class="count-qty"> {{count}} </div>
    <div class="count-controlls">
        <button v-on:click="minus" v-bind:disabled="count===1">-</button>
        <button  v-on:click="increase" v-bind:disabled="count===stock">+</button>
    </div>
</template>

<script>
export default {
    name:'Count',
    data(){
        return{
            count:1,
            stock:12
        }
    },
    methods:{
        increase(){
            this.count += 1;
        },
        minus(){
            this.count -= 1;
        }
    }

}
</script>

<style>
    .count-title {
        padding: 20px 10px;
        text-align: center;
        font-size:2.4rem;
        text-transform: uppercase;
        letter-spacing: 2px;
    }

    .count-qty{
        margin: 20px auto;
        text-align: center;
        font-size: 5.8rem;
        font-weight: bold;
    }

    .count-controlls{
        display: flex;
        justify-content: center;
        gap:8px;
    }

    .count-controlls button{
        background-color: #8b5cf6;
        border: none;
        padding: 9px 12px;
        width: 40px;
        font-size: 1.2rem;
        color: #FFFFFF;
        transition: all 0.250s ease-in-out;
    }

    .count-controlls button:active{
        background-color: #b494ff;
        transform: scale(0.95);
    }
    .count-controlls button:disabled{
        background-color: #9b92b0;
        opacity: 80%;
    }

</style>