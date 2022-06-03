<template>
  <div class="services">
    <BC />
    <MCE />
    <Lab />
    <MIA />
    
  </div>
</template>

<script>
import BC from "~/components/Services/I-S.vue"
import MCE from "~/components/Services/M-C-E.vue"
import Lab from "~/components/Services/ict-lab.vue"
import MIA from "~/components/Services/m-i-a.vue"


export default {
  components: {
    BC,
    MCE,
    Lab,
    MIA,
  }
}
</script>

<style lang="scss" scoped>

</style>