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
                        <li id="project">PROJECTS</li>
                        <li id="skills">SKILLS</li>
                        <li id="contact">CONTACT</li>
                        <li id="about">ABOUT</li>
                    </ul>
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
            if (hiddenMenuDiv.style.left !== "0px") {
                hiddenMenuDiv.style.left = "0px"
                portfolio.style.color = 'white'
                search.style.left = "0px"
                project.style.left = "0px"
                skills.style.left = "0px"
                contact.style.left = "0px"
                about.style.left = "0px"

                hiddenMenuDiv.style.transition = "0.3s"
                search.style.transition = "0.3s 0.1s"
                project.style.transition = "0.3s 0.2s"
                skills.style.transition = "0.3s 0.3s"
                contact.style.transition = "0.3s 0.4s"
                about.style.transition = "0.3s 0.5s"
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

                hiddenMenuDiv.style.transition = "0.3s 0.5s"
                search.style.transition = "0.3s 0.4s"
                project.style.transition = "0.3s 0.3s"
                skills.style.transition = "0.3s 0.2s"
                contact.style.transition = "0.3s 0.1s"
                about.style.transition = "0.3s"
                portfolio.style.transition = "0.3s 0.6s"
            }

            if (middle.style.display !== "none") {
                var positionInfo = top.getBoundingClientRect();
                var width = positionInfo.width
                middle.style.display = "none";
                top.style.backgroundColor = "#e34643";
                bottom.style.backgroundColor = "#e34643";
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

.menu ul li {
    position: relative;
    left: -10000px;
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
    gap: 3vw;
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
