<template>
    <div class="centerDiv">
        <div class="contentDiv">
            <div class="content">
                <div class="contentInnerDiv">
                    <p class="welcomeMessage">Welcome to my portfolio website!</p>
                    <p class="myWords">I'm a <span class="highlightWords">Developer and Designer</span> with a knack for
                        crafting
                        engaging
                        online experiences.</p>
                </div>
            </div>
            <div class="logo">
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
            <div class="message">
                <p style="margin: 0;">Whether you're seeking a freelancer for your next project or simply looking for
                    inspiration, I hope my work
                    resonates with you. Feel free to reach out—I'm always excited to collaborate and create something
                    extraordinary together.</p>
            </div>
            <div class="button">
                <div class="centerButton">
                    <div class="collobrateDiv">
                        <button class="collobrate">Let's Collaborate!</button>
                    </div>
                    <div class="viewProjectDiv">
                        <button class="viewProjects">View Projects?</button>
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
            github: require('../assets/Images/github.png'),
            linkedin: require('../assets/Images/linkedin.png'),
            netlify: require('../assets/Images/netlify.png'),
            instagram: require('../assets/Images/instagram.png'),
        }
    },
    components: {
    },
}
</script>

<style scoped>
.contentDiv {
    padding-block: min(3vw, 2rem);
    padding-inline: min(10vw, 20rem);
    display: grid;
    grid-template-columns: repeat(2, 1fr);
}

.content {
    min-width: 75vw;
    padding-top: 5vw;
    color: rgb(0, 0, 0);
    font-size: calc(1vw + 1rem);
}

.content .welcomeMessage {
    color: rgb(100, 100, 100);
}

.content .myWords {
    margin: 0px;
    font-size: calc(1vw + 5rem);
    font-weight: 800;
}

.content .myWords .highlightWords {
    color: red;
}

.logo img:hover {
    position: relative;
    z-index: 10;
    filter: drop-shadow(0mm 5mm 1mm rgb(31, 30, 30));
    animation: shiver 0.5s linear forwards;
}

.contentInnerDiv .profile {
    width: 64px;
}

@keyframes shiver {
    0% {
        transform: rotate(0deg) scale(1.1);
    }

    20% {
        transform: rotate(25deg) scale(1.1);
    }

    40% {
        transform: rotate(-25deg) scale(1.2);
    }

    60% {
        transform: rotate(15deg) scale(1.2);
    }

    60% {
        transform: rotate(-15deg) scale(1.3);
    }

    80% {
        transform: rotate(5deg)scale(1.3);
    }

    100% {
        transform: rotate(0deg) scale(1.4);
    }
}

.message {
    text-align: justify;
    padding-block: 3vw;
}

.centerButton {
    display: flex;
    align-items: center;
    gap: 3vw;
}

.centerButton button {
    font-size: calc(1vw + 1rem);
    padding: 5px 20px;
    background: red;
    border: none;
    color: white;
    width: min(60vw, 25rem);
    border-radius: 8px;
}

.centerButton .collobrateDiv {
    overflow: hidden;
    border-radius: 8px;
}

.centerButton .viewProjectDiv {
    overflow: hidden;
    border-radius: 8px;
}

.centerButton .collobrate:hover {
    background: black;
    color: white;
    transform: scale(1.1);
}


.centerButton .viewProjects {
    background: white;
    color: black;
    border: 1px solid black;
    box-sizing: border-box;
    overflow: hidden;
}

.centerButton .viewProjects:hover {
    background: red;
    color: white;
    transform: scale(1.1);
}





/* Above the 1400px */

@media (width >=1441px) {
    .logo img {
        transform: scale(2);
    }

}

@media (width >=1400px) {
    .centerButton button {
        font-size: calc(1vw + 1rem);
        padding: 1vw 5vw;
        width: auto;
    }

}



/* Above the 768px  */
@media (width >=769px) {
    .message {
        grid-column: span 2;
        font-size: calc(1vw + .5rem);
    }

    .logo {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 20px 0px;
        gap: 3vw;
        min-width: 5vw;
    }

    .logo .img {
        display: flex;
        justify-content: end;
    }


    .contentInnerDiv {
        width: 80%;
    }

    .centerButton {
        margin-top: calc(1vw + 1rem);
    }
}

/* Below the 768px  */
@media (width <=768px) {
    .contentDiv {
        padding-top: calc(10vw + 1rem);
        padding-inline: min(10vw, 20rem);
        grid-template-columns: auto;
    }

    .content {
        padding-top: calc(10vw + 1rem);
        padding-bottom: calc(5vw + .5rem);
        font-size: calc(1vw + 1rem);
        color: rgb(0, 0, 0);
    }

    .content .myWords {
        margin: 0px;
        font-size: calc(1vw + 3rem);
        font-weight: 800;
    }

    .message {
        grid-column: span 0;
        font-size: calc(1vw + .5rem);
        padding-block: calc(3vw + .5rem);
    }


    .logo {
        padding-block: calc(1vw + .5rem);
        display: flex;
        gap: 5vw;
        justify-content: center;
    }

    .centerButton {
        padding-block: calc(1vw + 1rem);
        display: flex;
        justify-content: space-around;
    }

}

@media (width <=650px) {
    .centerButton {
        padding-block: calc(1vw + 1rem);
        display: flex;
        flex-direction: column;
        width: min(80vw, 20rem);
        justify-content: center;
        gap: 2vw;
        margin-left: 50%;
        transform: translate(-50%);
    }
}

/* Below 425px */
@media (width <=425px) {
    .content {
        font-size: calc(1vw + 1rem);
    }

    .content .myWords {
        margin: 0px;
        font-size: calc(1vw + 2rem);
        font-weight: 800;
    }
}

@media (width <=390px) {
    .content {
        font-size: calc(2vw + 1.5rem);
    }
}

@media (width <=320px) {
    .content {
        font-size: calc(1vw + 1.5rem);
    }

    .content {
        padding-top: 0;
        padding-bottom: 0;
    }

    .content .myWords {
        margin: 0px;
        font-size: calc(1vw + 1.5rem);
        font-weight: 800;
    }

    .message {
        font-size: calc(1vw + .8rem);
        padding-block: 0;
    }

    .logo {
        padding-top: 15px;
        display: flex;
        gap: 5vw;
        justify-content: center;
    }

}</style>