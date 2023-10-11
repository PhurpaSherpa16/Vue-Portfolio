<template>
  <div class="homeDiv">
    <div class="homeContentDiv">
      <div class="navDiv">
        <NavBarComponent />
      </div>
      <div>
        <IdexPageComponent />
      </div>
      <div>
        <SecondPageComponent/>
      </div>
      <div>
        <ProjectComponent/>
      </div>
      <div>
        <SkillComponent/>
      </div>
      <div>
        <AboutAndContactComponentVue/>
      </div>
    </div>
  </div>
</template>

<script>
import NavBarComponent from "@/components/NavBarComponent.vue"
import IdexPageComponent from "@/components/IdexPageComponent.vue"
import SecondPageComponent from "@/components/SecondPageComponent.vue"
import ProjectComponent from "@/components/ProjectComponents.vue"
import SkillComponent from "@/components/SkillComponent.vue"
import AboutAndContactComponentVue from "@/components/AboutAndContactComponent.vue"

export default {
  data() {
    return {
    }
  },
  components: {
    NavBarComponent,
    IdexPageComponent,
    SecondPageComponent,
    ProjectComponent,
    SkillComponent,
    AboutAndContactComponentVue

  },
}
</script>

<style scoped>
.homeDiv {
  overflow: hidden;
}

.navDiv {
  position: fixed;
  min-width: 80lvw;
  z-index: 100;
  background: white;
  filter: drop-shadow(1px 1px 10px #b6b6b61f);
}

@media (width >= 1600px) {
    .navDiv {
    min-width: 85vw;
  }
}

</style>
