<template>
  <div id="app">
    <div v-for="(item, index) in audios" :key="index">
      <VueAudio :theUrl="item.url" :theControlList="item.controlList"/>
    </div>
  </div>
</template>

<script>
import VueAudio from './components/VueAudio'

export default {
  name: 'app',
  components: {
    VueAudio
  },
  data () {
    return {
      audios: [
        {
          url: './static/horse.ogg',
          controlList: 'onlyOnePlaying'
        },
        {
          url: './static/horse.ogg',
          controlList: 'noDownload noMuted onlyOnePlaying'
        }, {
          url: './static/horse.ogg',
          controlList: 'noDownload noVolume noMuted onlyOnePlaying'
        }, {
          url: './static/horse.ogg',
          controlList: 'noDownload noSpeed onlyOnePlaying'
        }
      ]
    }
  }
}
</script>

<style>

</style>
