<template>
    <div class="wrapper">
        <div class="box-flex-column">
            <p class="lets-go">{{ letsGo }}
            </p>
            <hr class="hrclass">
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            letsGo: 'LET’s Get in touch'
        }
    }
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.wrapper{
    width: 100%;
    height: 517px;
    border: 1px solid black;
    background-image: url('../assets/backgroundLETSGET.png');
    background-repeat: round;
}
.box-flex-column{
    height: 379px;
    margin-top: 68.95px;
    margin-left: 17.36%;
    margin-right: 17.36%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid white ;
}
.lets-go{

}
.hrclass{
    width: 80px;
    height: 2px;
    background: rgba(0, 0, 0, 0.09);
    border: none;
}
</style>