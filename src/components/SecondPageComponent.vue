<template>
    <div class="SecondPageMainDiv">
        <div class="SecondPageInnerDiv">
            
            <div class="words">
                <h2>Explore my diverse projects and discover how I blend 
                creativity with <span>Cutting-edge Technology</span> to bring ideas to life.</h2>
            </div>
            <div class="icon">
                <lord-icon class="i"
                src="https://cdn.lordicon.com/svbmmyue.json"
                trigger="loop"
                delay="1000"
                colors="primary:#ffffff,secondary:#ffffff">
            </lord-icon>
            </div>
        </div>
    </div>
</template>

<script>

export default{
    data(){
        return{
            program: require('../assets/Images/program.png')
        }
    }
}

</script>

<style scoped>
.SecondPageInnerDiv{
    margin-block: min(30vw, 5rem);
    color: white;
    background: rgb(0, 0, 0);
    padding-block: min(5vw, 2.5rem);
    padding-inline: min(10vw, 20rem);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.icon .i{
    height: calc(128px + 64px);
    width: calc(128px + 64px);
}

.SecondPageInnerDiv .words span{
    color: rgb(255, 0, 0);
}

@media (width <= 768px) {
    
.SecondPageInnerDiv{
    flex-direction: column;
    font-size: calc(1vw + .8rem);
    text-align: center;
}

.icon .i{
    height: 128px;
    width: 128px;
}

}

</style>