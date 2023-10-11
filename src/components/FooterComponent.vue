<template>
    <div class="FooterMainDiv">
        <div class="FooterDiv">
            <div class="upper">
                <div class="content">
                    <div class="title">
                        <h1>Thank Your Visiting My Portfolio.</h1>
                    </div>
                </div>
            </div>
            <div class="lower">
                <div class="qr">
                            <img :src="qr" alt="QR" title="QR" id="qr">
                </div>
                <div class="content">
                    <div class="socialIcon">
                        <div class="social">
                            <div class="img">
                                <img :src="github" alt="github" title="Github">
                            </div>
                            <div class="img">
                                <img :src="linkedin" alt="Linkedin" title="Linkedin">
                            </div>
                            <div class="img">
                                <img :src="netlify" alt="Netlify" title="Netlify">
                            </div>
                            <div class="img">
                                <img :src="instagram" alt="Instagram" title="Instagram">
                            </div>
                        </div>
                    </div>
                    <p>Copyright © 2023 Portfolio inc. All rights reserved.</p>
                    <p>The content on this portfolio is for demonstration and informational purposes only.<br/> All works showcased
                        are the property of their respective owners, and no endorsement or partnership is implied.</p>
                    <p>Design and Develop my self.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                github: require('../assets/Images/githubLight.png'),
                linkedin: require('../assets/Images/linkedinLight.png'),
                netlify: require('../assets/Images/netlifyLight.png'),
                instagram: require('../assets/Images/instagramLight.png'),
                qr: require('../assets/Images/qr.png'),
            }
        }
    }

</script>

<style scoped>
#qr{
    height: 128px;
    width: 128px;
}
.FooterDiv {
    padding-block: min(5vw, 3rem);
}

.icon {
    transform: rotateX(180deg);
}

.upper{
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.socialIcon{
    display: flex;
    justify-content: space-between;
}

.lower{
    display: flex;
    align-items: center;
    gap: 26px;
    color: #6b6a6a;
    font-size: calc(0.5vw + 0.5rem);
}

p{
    margin: 2px;
    gap: 0;
}
.social{
    display: flex;
    justify-content: space-between;
    gap: 3vw;
    margin-bottom: 1vw;
}
</style>