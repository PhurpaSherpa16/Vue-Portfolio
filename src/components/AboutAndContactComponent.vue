<template>
    <div class="mainDiv">
        <div class="itemsDiv">
            <div class="aboutDiv">
                <div class="heading">
                    <h1>You have a project, <br><span>Let's Collobrate & Grow Together.</span></h1>
                </div>
                <div class="myProfile">
                    <div class="card">
                        <div class="cardImage">
                            <div class="glass">
                            </div>
                        </div>
                        <div class="cardInfo">
                            <span class="profile">PROFILE</span><br>
                            <span class="details" id="title">Phurpa Sherpa</span><br>
                            <span class="details" id="degisnation">Web Desinger & Developer</span><br>
                            <span class="details" id="social">
                                <div>
                                    <img :src="youtube" alt="Youtube">
                                    15k+
                                </div>
                                <div>
                                    <img :src="instagram" alt="instagram">
                                    102k+
                                </div>
                                <div>
                                    <img :src="facebook" alt="facebook">
                                    50k
                                </div>
                                
                            </span>
                            <span class="details" id="buttons">
                                <div>
                                    <button id="buttonOne">
                                        Download CV
                                    </button>
                                </div>
                                <div>
                                    <button id="buttonTwo">
                                        Call Me
                                    </button>
                                </div>
                            </span>
                        </div>
                        
                    </div>
                </div>
            </div>
            <div class="footerDiv">
                <FooterComponent/>
            </div>
        </div>
    </div>
</template>

<script>

import FooterComponent from './FooterComponent.vue';

export default{
    data(){
        return{
            profile : require('../assets/Images/background.jpg'),
            youtube : require('../assets/Images/youtube.png'),
            instagram : require('../assets/Images/instagram.png'),
            facebook : require('../assets/Images/facebook.png'),
        }
    },
    components:{
        FooterComponent
    }
}

</script>

<style scoped>

#title{
    font-size: 22px;
    letter-spacing: 4px;
    font-weight: 800;
}
#degisnation{
    font-size: 14px;
    letter-spacing: 0px;
    font-weight: 800;
    color: #949393;
}
#social{
    padding-block: 1vw;
    display: flex;
    align-items: center;
    gap: 1vw;
    justify-content: center;
}

#social div{
    display: flex;
    align-items: center;
    gap: 0.5vw;
    justify-content: center;
}

#buttons{
    display: flex;
    justify-content: space-between;
}

#buttons button{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1vw;
    padding: 8px 25px;
    border-radius: 8px;
    cursor: pointer;
}
#buttonOne{
    color: white;
    background-color: red;
    border: 0px;
}

#buttonTwo{
    border: 1px solid black;
    color: black;
}
.itemsDiv {
    padding-block: min(5vw, 3rem);
    padding-inline: min(10vw, 20rem);
    color: #ffffff;
    background: rgb(0, 0, 0);
}

h1{
    font-size: calc(3vw + 1.5rem);
}

h1 span{
    color: red;
}

.aboutDiv{
    display: flex;
    gap: 5vw;
    align-items: center;
}

.card{
    border-radius: 8px;
    overflow: hidden;
    position: relative;
}

.cardImage{
    background: url('../assets/Images/one.jpg');
    overflow: hidden;
    border-radius: 8px;
    width: 320px;
    height: 220px;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    margin-bottom: 8px;
    position: relative;
}

.cardImage::before{
    content: "";
    position: absolute;
    height: 25px;
    width: 25px;
    background: transparent;
    border-radius: 8px;
    bottom: 62px;
    left: 0;
    box-shadow: -8px 8px 0 black;
    z-index: 2;
}
.cardImage::after{
    content: "";
    position: absolute;
    height: 25px;
    width: 25px;
    background: transparent;
    border-radius: 8px;
    bottom: 0px;
    left: 178px;
    box-shadow: -8px 8px 0 black;
    z-index: 2;
}

.glass{
    height: 110px;
    width: 320px;
    position: relative;
    bottom: -100px;
    background: rgba(110, 110, 110, 0.856);
}

.glass::before{
    content: "";
    height: 150px;
    width: 320px;
    position: absolute;
    background: url('../assets/Images/one.jpg') no-repeat center center/cover;
    filter: blur(8px);
}

.glass::after{
    content: "";
    height: 120px;
    width: 120px;
    color: black;
    text-align: center;
    top: -70px;
    left: 50%;
    transform: translate(-50%);
    background: url('../assets/Images/profile1.png') no-repeat center center/cover;
    position: absolute;
    z-index: 1;
    border-radius:100px;
}

.cardInfo{
    background: rgb(255, 255, 255);
    padding: 0 20px 20px 20px;
    border-radius: 8px;
    border-top-left-radius: 0px;
    position: relative;
    z-index: 2;
    color: black;
    text-align: center;
}

.cardInfo .profile{
    background: rgb(255, 255, 255);
    font-weight: 800;
    width: 130px;
    height: 22px;
    position: absolute;
    top: -70px;
    left: 0;
    border-top: 8px solid rgb(0, 0, 0);
    border-right: 8px solid rgb(0, 0, 0);
    border-top-right-radius: 16px;
    padding: 20px;
    letter-spacing: 8px;
    color: rgb(80, 79, 79);

}
.cardInfo .profile::before{
    content: "";
    position: absolute;
    height: 25px;
    width: 25px;
    background: transparent;
    border-radius: 8px;
    top: 0;
    left: 0;
    box-shadow: -8px -8px 0 black;
}
.cardInfo .profile::after{
    content: "";
    position: absolute;
    height: 25px;
    width: 25px;
    background: transparent;
    border-radius: 8px;
    bottom: 0px;
    right: -25px;
    box-shadow: -8px 8px 0 rgb(255, 255, 255);
}


@media (width <= 768px) {
    .aboutDiv{
        flex-direction: column;
    }
    #buttons{
        margin-top: 5px;
    }
}



</style>