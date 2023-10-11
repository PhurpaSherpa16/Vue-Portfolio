<template>
    <div class="skillMainDiv">
        <div class="heading">
            <h1>Service, I provide!</h1>
            <hr>
        </div>
        <div class="what-I-offer">
            <div class="serviceDiv">
                <div class="service" id="service-one">
                    <div class="serviceHeading">
                        <h3>Website Design and Development</h3>
                        <lord-icon :src="`https://cdn.lordicon.com/${this.arrow}.json`" trigger="hover"
                            colors="primary:#000000" style="width:32px;height:32px" @click="toggle('serviceContentOne')">
                        </lord-icon>
                    </div>
                    <div class="serviceContent" id="serviceContentOne">
                        Passionate web designer & developer creating stunning, user-friendly websites to elevate brands and
                        enhance online experiences.
                    </div>
                </div>
                <div class="service" id="service-two">
                    <div class="serviceHeading">
                        <h3>Mobile Application</h3>
                        <lord-icon :src="`https://cdn.lordicon.com/${this.arrow}.json`" trigger="hover"
                            colors="primary:#000000" style="width:32px;height:32px" @click="toggle('serviceContentTwo')">
                        </lord-icon>
                    </div>
                    <div class="serviceContent" id="serviceContentTwo">
                        Experienced in mobile app development, creating user-friendly, innovative, and scalable solutions for various platforms.
                    </div>
                </div>
                <div class="service" id="service-three">
                    <div class="serviceHeading">
                        <h3>Desktop Application</h3>
                        <lord-icon :src="`https://cdn.lordicon.com/${this.arrow}.json`" trigger="hover"
                            colors="primary:#000000" style="width:32px;height:32px" @click="toggle('serviceContentThree')">
                        </lord-icon>
                    </div>
                    <div class="serviceContent" id="serviceContentThree">
                        Crafting efficient, user-friendly desktop apps that elevate user experiences and solve real-world problems with precision.
                    </div>
                </div>
            </div>
            <div class="skill">
                <div class="skillsDiv">
                    <div class="skill">
                        <img :src="html" alt="HTML" title="HTML" id="skill">
                    </div>
                    <div class="skill">
                        <img :src="css" alt="CSS" title="CSS" id="skill">
                    </div>
                    <div class="skill">
                        <img :src="js" alt="JS" title="JS" id="skill">
                    </div>
                    <div class="skill">
                        <img :src="python" alt="Python" title="Python" id="skill">
                    </div>
                    <div class="skill">
                        <img :src="android" alt="Android" title="Android" id="skill">
                    </div>
                    <div class="skill">
                        <img :src="figma" alt="Figma" title="Figma" id="skill">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            html: require('../assets/Images/html.png'),
            css: require('../assets/Images/css.png'),
            python: require('../assets/Images/python.png'),
            js: require('../assets/Images/js.png'),
            android: require('../assets/Images/android.png'),
            figma: require('../assets/Images/figma.png'),
            web: require('../assets/Images/web.jpg'),
            arrow: "rxufjlal",

        }
    },
    methods: {
        toggle(serviceContentOne) {
            var serviceContent = document.getElementById(`${serviceContentOne}`)
            let up = "xsdtfyne"
            let down = "rxufjlal"
            if (serviceContent.style.height !== "6rem") {
                serviceContent.style.height = "6rem";
                serviceContent.style.transition = "1s";
                this.arrow = up
            }
            else {
                serviceContent.style.height = "0vw";
                serviceContent.style.transition = "1s";
                this.arrow = down
            }
        }

    }
}
</script>

<style scoped>
.skillMainDiv {
    padding-block: min(5vw, 3rem);
    padding-inline: min(10vw, 20rem);
}

.what-I-offer {
    margin-block: 5vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 3vw;
}

.service {
    border-bottom: 1px solid rgba(167, 167, 167, 0.486);
}

.service .serviceHeading {
    display: flex;
    gap: 1vw;
    align-items: center;
}

.service .serviceContent {
    overflow: hidden;
    text-align: justify;
    padding-bottom: 2vw;
    height: 0vw;
}

.heading h1 {
    font-size: calc(3vw + 1.5rem);
    text-align: center;
    padding: 0;
    margin-bottom: 0;
    filter: drop-shadow(3px 20px 4px rgba(0, 0, 0, 0.11));
}

.heading hr {
    width: 25vw;
    height: 4px;
    background: rgb(114, 114, 114);
    border-radius: 8px;
    border: none;
    filter: drop-shadow(3px 10px 8px rgba(0, 0, 0, 0.411));
}

.skillsDiv {
    padding-block: min(5vw, 3rem);
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    place-content: center;
    place-items: center;
    gap: 7vw;
}

#skill {
    height: 64px;
    width: 64px;
}

#skill:hover {
    transform: scale(1.1);
    filter: drop-shadow(3px 20px 4px rgba(0, 0, 0, 0.747));
}

@media (width <=768px) {
    .what-I-offer {
        flex-direction: column;
    }
}

@media (width <=425px) {
    .skillsDiv {
        grid-template-columns: repeat(3, 1fr);
    }

    #skill {
        height: 32px;
        width: 32px;
    }
}
</style>