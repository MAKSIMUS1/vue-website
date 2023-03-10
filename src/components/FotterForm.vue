<template>
    <div class="wrapper">
        <div class="wrapper-flex">
            <form @submit.prevent id="form-container" action="#">
				<input v-bind:value="name" 
                @input="inputTitle"
                class="input" 
                type="text" 
                placeholder="Name">
				<input v-bind:value="email" 
                @input="inputEmail"
                class="input" 
                type="email" 
                placeholder="Email">
				<input 
                v-bind:value="budget" 
                @input="inputBudget"
                class="input" 
                type="text" 
                placeholder="Budget">
                <textarea 
                v-bind:value="description"
                @input="inputDescription"
                class="input" 
                type="text" 
                placeholder="Describe youre project..."></textarea>
                <div class="box-sendButton">
                    <input 
                    @click="send_Button"
                    class="send_Button" 
                    type="submit" 
                    name="submit_btn" 
                    value="Send message">
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            name: '',
            email: '',
            budget: '',
            description: ''
        }
    },
    methods:{
        inputTitle(e){
            this.name = e.target.value;
        },
        inputEmail(e){
            this.email = e.target.value;
        },
        inputBudget(e){
            this.budget = e.target.value;
        },
        inputDescription(e){
            this.description = e.target.value;
        },
        send_Button(e){
            //e.preventDefault();
            console.log(this.name, this.email, this.budget, this.description);
            this.name = '';
            this.email = '';
            this.budget = '';
            this.description = '';
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
    height: 639px;
    border: 1px solid black;
    background-color: #000000;
}
.wrapper-flex{
    height: 501px;
    border: 1px solid white ;
    margin-top: 68.95px;
    margin-left: 17.36%;
    margin-right: 17.36%;
}

textarea[name="details"] { 
  resize: none; 
  height: 127px;
}   
.input {
width: 100%;
height: 57px;
 font-size: 16px;
 border: none !important;
 padding: 12px 30px;
 box-sizing: border-box;
 color: #FFFFFF;
 outline: none;
 background-color: rgba(255, 255, 255, 0.18);
}
.input:nth-child(even){
    background-color: rgba(255, 255, 255, 0.2);
}

#form-container{
    height: 398px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.box-sendButton{
    flex:1;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.send_Button{
    width: 37.2%;
    height: 53px;
    border: 2px solid #7EC4BD;
    background-color: #000000;
    color: #8BCAC3;
}
</style>