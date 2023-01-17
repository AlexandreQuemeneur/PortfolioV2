<template>
    <section class="send">

        <div class="fusee">
            <img src="@/assets/rocket.png" alt="" id="rocket">
        </div>

        <div class="contact">
            <form ref="form" @submit.prevent="sendEmail">

                <label>Name</label>
                <input type="text" name="user_name">

                <label>Email</label>
                <input type="email" name="user_email">

                <label>Message</label>
                <textarea name="message" class="message"></textarea>

                <input type="submit" value="Send" class="button">

                <p v-if="this.succes.sendIt">Thanks for your email</p>
                <p v-if="this.error.sendIt">Sorry something went wrong</p>
            </form>
        </div>
    </section> 
    <footer>
        
        <div><p class="boop">&#169;2023 Alexandre quemeneur, All Rights Reserved </p></div>
        <div class="social">
           <a target="_blank" href="https://github.com/AlexandreQuemeneur"><img src="@/assets/github.png" alt="github-logo"></a> 
           <a target="_blank" href="https://www.linkedin.com/in/alexandre-quemeneur/"><img src="@/assets/linkedin.png" alt="linkedin-logo"></a> 
           <a target="_blank" href="https://twitter.com/Octave_DeLaBath"><img src="@/assets/twitter.png" alt="twitter-logo"></a>
        </div>

       
    </footer>
</template>

<script>
import {gsap} from "gsap";
import { ScrollTrigger } from 'gsap/ScrollTrigger';
import emailjs from '@emailjs/browser';
gsap.registerPlugin(ScrollTrigger);
export default {
    name: "ContactComponent",
    data(){
        
        return{
            succes : {
                sendIt: false
            },
            error : {
                sendIt: false
            }
        }
    },
    mounted(){
        gsap.to("#rocket",{
            y: -7,
            yoyo: true,
            repeat: 1000,
            duration: 1,
        })
    },

    methods:{
        sendEmail() {
            emailjs.sendForm('service_f7y2g02', 'template_4grqns6', this.$refs.form, 'camcHrgzAXAZON1lp')
            .then((result) => {
                console.log('SUCCESS!', result.text);
                this.succes.sendIt = true;
                gsap.to("#rocket", {
                y: -1000,
                x: -500, 
                rotate: -45,
                opacity: 0, 
                ease: "slow(0.7, 0.7, false)",
                duration: 2.7,
            })
            }, (error) => {
                this.error.sendIt = true;
                console.log('FAILED...', error.text);
            });
        }
    },
}
</script>

<style lang="scss" scoped>

.send{
    width: 100%;
    height: 100vh;
    background-color: rgb(30, 30, 28);
    display: flex;
    justify-content: center;
    align-items: center;
}
.contact{
    width: 50%;
    form{
        display: flex;
        flex-direction: column;  
    }
}
.fusee{
    display: flex;
    justify-content: center;
    width:50%    
}

//Mobile devices
@media screen and (max-width: 415px){

    .contact{
        z-index: 9999;
        form{
            input{
                margin: 5px 0;
                padding: 5px;
                width: 65%;
                border: none;
                outline: none;
                color: black;
                border-top: 3px solid #F6E670;
            }
            textarea{
                width: 85%;
                height: 100px;
                margin: 2px 0;
                border: none;
                outline: none;
                color: black;
                padding: 5px;                
                border-top: 3px solid #F6E670;
            }
            .button:hover{
                border-top: 3px solid #9d8c0c;
                cursor: pointer;
            }
        }
    }
    #rocket{
        rotate: -15deg;
        width: 250px;  
    }
}


//tablet devices
@media screen and (min-width:416px) and (max-width: 1180px){
    .contact{
        form{
            button{
                width: 65%;
                height: 40px;
                margin-top: 5px;
                border: none;
                outline: none;
                color: black;
                border-top: 3px solid #F6E670;
            }
            input{
                width: 80%;
                height: 45px;
                margin: 7px 0;
                padding: 5px;
                border: none;
                outline: none;
                color: black;
                border-top: 3px solid #F6E670;
            }
            textarea{
                width: 85%;
                height: 250px;
                margin: 5px 0;
                padding: 5px;
                border: none;
                outline: none;
                color: black;
                border-top: 3px solid #F6E670;
            }
            .button:hover{
                border-top: 3px solid #9d8c0c;
                cursor: pointer;
            }
        }
    }
     #rocket{
        rotate: -8deg;
        width: 350px;  
    }   
}


//desktop devices
@media screen and (min-width:1181px){
    .contact{
        width: 50%;
        form{
            input{
                width: 70%;
                height: 50px;
                margin: 5px 0;
                padding: 5px;
                border: none;
                outline: none;
                color: black;
                border-top: 3px solid #F6E670;
            }
            button{
                width: 55%;
                height: 55px;
                color: black;
                margin: 10px 0 0 0;
                border: none;
                outline: none;
                border-top: 3px solid #F6E670;
            }
            textarea{
                width: 80%;
                height: 220px;
                padding: 5px;
                border: none;
                outline: none;
                color: black;
                margin: 10px 0;
                border-top: 3px solid #F6E670;
            }
            .button:hover{
                border-top: 3px solid #9d8c0c;
                cursor: pointer;
            }

        }
    }
    #rocket{
        rotate: -14deg;
        width: 450px;  
    }    
}


footer{
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 5px;
    background-color: rgb(30, 30, 28);
    max-height: 500px;
}
.social{
    width:50%;
    display: flex;
    justify-content: flex-end;
    align-items: center;

    img{
        width: 30px;
        height: 30px;
        margin: 0 10px 2px 10px;
    }
}
</style>