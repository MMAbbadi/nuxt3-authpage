<template>
    <div class="body">
        <div v-if="logged" class="modal_login">
            <div class="container_modal">
                <div @click="logIn" class="close_btn">
                    <div class="container_btn">
                        <div class="inner_btn">
                            <p class="mark">X</p>
                        </div>
                    </div>
                </div>
                <h1 class="modal_text">
                    You've Logged In!
                </h1>
                <div class="modal_subtext">
                    Congrats!
                </div>
                <div class="check">
                    <div class="check_mark">&#10003</div>
                </div>
            </div>
        </div>
        <div class="main_display">
            <div class="bg">
    
                <div class="img_container"></div>
            </div>
        </div>
        <div class="form_display">
            <div class="title_plus_">
                <img src="" alt="" class="lg">
            <h3 class="form_text">Welcome!<br/><span>Enter Your Credentials</span></h3>
            </div>
            <div class="form_container">
                <input v-model="userInput" type="text" placeholder="Username" class="user_input">
                <input v-model="passwordInput" type="password" placeholder="Password" class="password_input">
                <button @click="logIn" type="submit" class="submit_infos">
                    Log In
                </button>
            </div>
            
        </div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                logged: false,             
            }
        },
        methods:{
            logIn(){
                this.logged = !this.logged
            }
        }
    }
</script>

<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family:Arial, Helvetica, sans-serif;
    }
    html{
        background: black;
    }
    .body{
        height:969px;
        display: flex;
        background: red;
    }
    /* MAIN DISPLAY */
    .main_display{
        width: 70%;
        height: 100%;
        background:rgb(46, 2, 63);
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .bg{
        height: 100%;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    
    /* FORM */
    .form_display{
        height: 100%;
        width: 30%;
        gap: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background: rgb(255, 255, 255);
    }
    .form_title{
        position: relative;
        top: 15%;
        bottom: 30%;
        left: auto;
        right: auto;
    }
    .form_container{
        height: 200px;
        display: flex;
        gap: 10px;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .user_input, .password_input{
        height: 30px;
        width: 250px;
        padding: 0 10px;
        border-radius: 10px;
        outline: none;
        border: 1px solid rgb(65, 65, 65);
    }
    .user_input:focus, .password_input:focus{
        outline: none;
    }
    .submit_infos{ 
        width: 120px;
        height: 35px;
        border: 1px solid rgb(65, 65, 65);
        border-radius: 15px;
        outline: none;
        color: white;
        background: rgb(48, 100, 248);
        cursor: pointer;
    }
    /* LOGGED MODAL */
    .modal_login{
        height: 100%;
        width: 100%;
        background: rgba(0, 0, 0, 0.2);
        position: absolute;
        top: auto;
        bottom: auto;
        left: auto;
        right: auto;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .container_modal{
        width: 400px;
        height: 400px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 15px;
        background-color: white;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.8);
    }
    .close_btn{
        width: 40px;
        height: 40px;
        background: white;
        border-radius: 40px;
        border: solid 1px black;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        top: -38%;
        right: -50%;
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.8);
        cursor: pointer;
    }
    /* MODAL CONTENT */
    .modal_text{
        position: relative;
        top: -15%;
    }
    .modal_subtext{
        position: relative;
        top: -5%;
    }
    .check{
        width: 50px;
        height: 50px;
        border-radius: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        background: rgb(124, 225, 124);
    }
    .check_mark{
        font-weight: 800;
        font-size: 25px;
    }
</style>