<template>
  <div id="app">
    <div v-for="item in audios" :key="item.url">
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
          url: 'http://devtest.qiniudn.com/secret base~.mp3',
          controlList: 'onlyOnePlaying'
        },
        {
          url: 'http://devtest.qiniudn.com/回レ！雪月花.mp3',
          controlList: 'noDownload noMuted onlyOnePlaying'
        },{
          url: 'http://devtest.qiniudn.com/あっちゅ～ま青春!.mp3',
          controlList: 'noDownload noVolume noMuted onlyOnePlaying'
        },{
          url: 'http://devtest.qiniudn.com/Preparation.mp3',
          controlList: 'noDownload noSpeed onlyOnePlaying'
        }
      ]
    }
  }
}
</script>

<style>

</style>
