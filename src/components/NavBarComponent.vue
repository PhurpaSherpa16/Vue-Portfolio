<template>
    <div class="navDiv">
        <div class="logo">
            <span id="portfolio">PORTFOLIO</span>
        </div>
        <div class="burgerMenu" @click="onToggle">
            <span class="bar" id="top"></span>
            <span class="bar" id="middle"></span>
            <span class="bar" id="bottom"></span>
        </div>
        <div id="hiddenMenuDiv" class="hiddenMenuDiv">
            <div class="items">
                <div class="searchBarDiv" id="searchBarDiv">
                    <lord-icon id="searchIcon" src="https://cdn.lordicon.com/xfftupfv.json" trigger="hover"
                        colors="primary:#001f3f" style="width:32px;height:32px"></lord-icon>
                    <input type="text" id="searchBar" placeholder="Search...">
                </div>
                <div class="menu">
                    <ul>
                        <div id="project" style="display: flex; gap: 20px;">
                            <lord-icon
                                src="https://cdn.lordicon.com/fpmskzsv.json"
                                trigger="loop"
                                delay = "1000"
                                colors="primary:#ffffff,secondary:#ffffff"
                                style="width:32px;height:32px">
                            </lord-icon>
                            <li><a href="/">PROJECTS</a></li>
                        </div>
                        <div id="skills" style="display: flex; gap: 20px;">
                            <lord-icon
                                src="https://cdn.lordicon.com/wluyqhxh.json"
                                trigger="loop"
                                delay = "1100"
                                colors="primary:#ffffff,secondary:#ffffff"
                                style="width:32px;height:32px">
                            </lord-icon>
                            <li><a href="/">Skills</a></li>
                        </div>
                        <div id="about" style="display: flex; gap: 20px;">
                            <lord-icon
                            src="https://cdn.lordicon.com/bhfjfgqz.json"
                            trigger="loop"
                            delay = "1200"
                            colors="primary:#ffffff,secondary:#ffffff"
                            style="width:32px;height:32px">
                            </lord-icon>
                            <li><a href="/">About</a></li>
                        </div>
                        <div id="contact" style="display: flex; gap: 20px;">
                            <lord-icon
                                src="https://cdn.lordicon.com/ssvybplt.json"
                                trigger="loop"
                                delay = "1300"
                                colors="primary:#ffffff,secondary:#ffffff"
                                style="width:32px;height:32px">
                            </lord-icon>
                            <li><a href="/">Contact</a></li>
                        </div>
                    </ul>
                </div>
                <div id="menuWords">
                    <span style="font-size: calc(.5vw + .5rem);">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Voluptas sequi ipsam veniam nemo, nihil minima, asperiores
                        vel adipisci <br/>
                        Lorem ipsum dolor sit ©2023 amet consectetur adipisicing elit.
                        Voluptas sequi
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    methods: {
        onToggle() {
            const hiddenMenuDiv = document.getElementById('hiddenMenuDiv')
            const portfolio = document.getElementById('portfolio')
            var search = document.getElementById("searchBarDiv")
            var project = document.getElementById("project")
            var skills = document.getElementById("skills")
            var contact = document.getElementById("contact")
            var about = document.getElementById("about")
            var top = document.getElementById("top")
            var middle = document.getElementById("middle")
            var bottom = document.getElementById("bottom")
            var menuWords = document.getElementById("menuWords")
            if (hiddenMenuDiv.style.left !== "0px") {
                hiddenMenuDiv.style.left = "0px"
                portfolio.style.color = 'white'
                search.style.left = "0px"
                project.style.left = "0px"
                skills.style.left = "0px"
                contact.style.left = "0px"
                about.style.left = "0px"
                menuWords.style.left = "0px"

                hiddenMenuDiv.style.transition = "0.3s"
                search.style.transition = "0.3s 0.1s"
                project.style.transition = "0.3s 0.2s"
                skills.style.transition = "0.3s 0.3s"
                contact.style.transition = "0.3s 0.4s"
                about.style.transition = "0.3s 0.5s"
                menuWords.style.transition = "0.4s 0.6s"
                portfolio.style.transition = "0.3s"
            }
            else {
                hiddenMenuDiv.style.left = "-10000px"
                portfolio.style.position = "relative"
                portfolio.style.color = 'black'
                search.style.left = "-10000px";
                project.style.left = "-10000px";
                skills.style.left = "-10000px";
                contact.style.left = "-10000px";
                about.style.left = "-10000px";
                menuWords.style.left = "-10000px";

                hiddenMenuDiv.style.transition = "0.3s 0.6s"
                search.style.transition = "0.3s 0.5s"
                project.style.transition = "0.3s 0.4s"
                skills.style.transition = "0.3s 0.3s"
                contact.style.transition = "0.3s 0.2s"
                about.style.transition = "0.3s 0.1s"
                menuWords.style.transition = "0.3s"
                portfolio.style.transition = "0.3s 0.7s"
            }

            if (middle.style.display !== "none") {
                var positionInfo = top.getBoundingClientRect();
                var width = positionInfo.width
                middle.style.display = "none";
                top.style.backgroundColor = "#ff0000";
                bottom.style.backgroundColor = "#ff0000";
                if (width == '22') {
                    top.style.transform = "translateY(3px) rotate(45deg)";
                    bottom.style.transform = "translateY(-3px) rotate(-45deg)";
                }
                else {
                    top.style.transform = "translateY(4px) rotate(45deg)";
                    bottom.style.transform = "translateY(-4px) rotate(-45deg)";
                }
            } else {
                middle.style.display = "block";
                top.style.transform = "translateY(0px) rotate(0deg)";
                bottom.style.transform = "translateY(0px) rotate(0deg)";
                top.style.backgroundColor = "black";
                bottom.style.backgroundColor = "black";
            }
        }
    }
}
</script>

<style scoped>
.navDiv {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    padding-inline: min(10vw, 20rem);
    padding-block: min(3vw, 2rem);
}

.logo {
    z-index: 100;
}

.logo span {
    font-size: calc(1.2vw + 1rem);
    letter-spacing: calc(.8vw + .1rem);
    cursor: pointer;
}

.burgerMenu {
    display: grid;
    gap: 5px;
    z-index: 100;
    cursor: pointer;
}

.burgerMenu span {
    width: 32px;
    height: 3px;
    border-radius: 100px;
    background-color: rgb(0, 0, 0);
    transition: 0.3s;
}

#middle {
    width: 24px;
}

.menu ul {
    cursor: pointer;
    list-style: none;
    display: flex;
    flex-direction: column;
    font-size: calc(1vw + .5rem);
    padding: 0;
    gap: 3vw;
}

.menu ul div {
    position: relative;
    left: -10000px;
}

.menu ul:hover div{
    opacity: 0.1;
    transition: 0s;
}

.menu ul div:hover{
    opacity: 1;
    transition: 0s;
}

.menu ul li a{
    color: white;
    text-decoration: none;
}

.hiddenMenuDiv {
    position: absolute;
    z-index: 99;
    top: 0;
    color: azure;
    background: rgb(14, 14, 14);
    min-height: 100vh;
    min-width: 100%;
    display: grid;
    left: -10000px;
}

.searchBarDiv {
    position: relative;
    left: -10000px;
}

.items {
    display: grid;
    place-content: center;
    place-items: center;
    gap: 2vw;
    padding-block: 10vw;
}

.hiddenMenuDiv input {
    background-color: rgb(255, 255, 255);
    padding: 10px 50px 10px 10px;
    border: none;
    border-radius: 8px;
    width: 40vw;
}

#searchIcon {
    position: absolute;
    right: 10px;
    top: 8%;
    cursor: pointer;
}

#menuWords{
    text-align: center;
    position: relative;
    left: -10000px;
}

@media (width <= 769px){
    .menu ul {
        font-size: calc(1vw + 1.2rem);
        gap: 4vw;
    }
}


@media (width <=425px) {
    .logo span {
        font-size: calc(1vw + 1.5rem);
        letter-spacing: calc(1vw + .5rem);
        cursor: pointer;
    }

    .burgerMenu {
        gap: 3px;
    }

    .burgerMenu span{
        width: 22px;
        left: 0px;
    }

    #middle {
        width: 14px;
    }

    .hiddenMenuDiv input {
        font-size: calc(1vw + 1rem);
    }
}

@media (width >=1441px) {
    .logo span {
        font-size: calc(1vw + 1.5rem);
        letter-spacing: calc(1vw + .5rem);
        cursor: pointer;
    }

    .burgerMenu {
        gap: 6px;
    }

    .burgerMenu span{
        width: 42px;
        left: 0px;
        height: 5px;
    }

    #middle {
        width: 34px;
    }

    .hiddenMenuDiv input {
        font-size: calc(1vw + 1.5rem);
    }
}
</style>
