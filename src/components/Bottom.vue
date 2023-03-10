<template>
    <div class="wrapper">
        <div class="firstFrame">

            <div class="iconTwoDots">
                <iconcommas/>
            </div>
            <div class="manAndWoman">
                <div class="people" v-for="human in peoples">
                    <div>{{ human.title }}</div>
                    <img :src=human.image alt="">
                    <div>{{ human.name }}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import iconcommas from './icons/IconCommas.vue'
export default {
    data(){
        return{
            peoples:[
                {title: '“I love these guys! They did a great job. I would recommend them to anyone.”', image: 'http://localhost:5173/julius.png', name:'Julius Von Uberstien'},
                {title: '“Elexis Corp. has grown immensely with the help of Minimal.”',                 image: 'http://localhost:5173/rachel.png', name:'Rachel Stamos'}
            ]
        }
    },
    components: {
        iconcommas
    }
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.firstFrame {
    width: 100%;
    height: 511px;
    background: #F5F5F5;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
}
.iconTwoDots{
    margin-top: 69px;
    align-self: center;
}
.manAndWoman{
    display: flex;
    flex-direction: row;
    justify-content: center;
    height: 274px;
}
.people{
    width: 40%;
    display: flex;
    flex-direction: column;
    text-align: center;
}
.people img{
    height: 64px;
}

</style>