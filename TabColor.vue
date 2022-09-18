<template>
    <button :style="this.StyleBtn" @click="click" class="btn">клик!</button>
</template>
<script>
export default {
    name: "TabColor",
    data () {
        return {
            StyleBtn: {
                background: 'rgb(255,255,255)',
                color: 'rgb(0,0,0)',
                BorderRadius: '0px',
                BorderColor: 'rgb(0,0,0)' 
            }
        }
    },
    methods: {
        random(max=255) {
           return Math.floor(Math.random()*max)
        },
        click () {
            let red = this.random();
            let green = this.random();
            let blue = this.random();
            this.StyleBtn.background = `rgb(${red}, ${green}, ${blue})`;
            this.StyleBtn.color = `rgb(${255-red}, ${255-green},${255-blue})`;
            this.StyleBtn.BorderRadius = this.random(100) + 'px';
            this.StyleBtn.BorderColor = `rgb(${this.random()}, ${this.random()}, ${this.random()})`
            console.log(this.StyleBtn)            

        }
    }
    
    }
</script>

<style>
   .btn{
    font-size: 40px;
    transition: 0.5s;
   }
</style>