<template>
   <div class="card">
      <p class="title">
        Title
      </p>
      <p class="description" @click="finished = !finished">

        <textarea @click.stop="" v-show="finished == false " v-model="textareaValue" placeholder="choose note type in the right column, then start typing you text here"></textarea>
        <component :is="currentTab" :msg='textareaValue'></component>
        <span class="date">today</span>

      </p>
      <div class="actions">
        <span 
          v-for="tab in tabs" 
          :key="tab"
          @click="currentTab = tab"
          :class="{ active: tab === currentTab }"
          >
          {{tab}}
        </span>
        <span @click="finished = true" class="ready">✓</span>
      </div>
    </div>
</template>

<script>
import dD from '@/components/defaultDescription.vue'
import olD from '@/components/olD.vue'
import ulD from '@/components/ulD.vue'
export default {
  name: 'card',
  components: {
    dD, ulD, olD
  },
  props: {
    
  },
  data() {
    return {
      currentTab: "",
      tabs: ["dD", "ulD", "olD"],
      textareaValue: '',
      finished: false,
      isActive: true
    }
  },
  computed: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
