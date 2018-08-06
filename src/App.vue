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
          url: './static/falling-star.mp3',
          controlList: 'onlyOnePlaying'
        },
        {
          url: './static/falling-star.mp3',
          controlList: 'noDownload noMuted onlyOnePlaying'
        }, {
          url: './static/falling-star.mp3',
          controlList: 'noDownload noVolume noMuted onlyOnePlaying'
        }, {
          url: './static/falling-star.mp3',
          controlList: 'noDownload noSpeed onlyOnePlaying'
        }
      ]
    }
  }
}
</script>

<style>

</style>
