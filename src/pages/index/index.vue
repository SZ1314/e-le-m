<template>
  <div>
    <index-header></index-header>
    <index-search></index-search>
    <index-swiper :list="swiperInfo"></index-swiper>
    <index-icons :list="iconsInfo"></index-icons>
    <index-sights></index-sights>
    <index-footer></index-footer>
  </div>
</template>
<script>
import IndexHeader from './header'
import IndexSearch from './search'
import IndexSwiper from './swiper'
import IndexIcons from './icons'
import IndexSights from './sights'
import IndexFooter from './footer'
import axios from 'axios'
export default {
  name: 'index',
  components: {
    IndexHeader,
    IndexSearch,
    IndexSwiper,
    IndexIcons,
    IndexSights,
    IndexFooter
  },
  data () {
    return {
      swiperInfo: [],
      iconsInfo: []
    }
  },
  methods: {
    getIndexDate () {
      axios.get('/api/index.json')
        .then(this.handleGetDateSucc.bind(this))
        .catch(this.handleGetDateErr.bind(this))
    },
    handleGetDateSucc (res) {
      const data = res.data.data
      this.swiperInfo = data.swiperList
      this.iconsInfo = data.iconList
      console.log(res)
      console.log(this.iconsInfo)
    },
    handleGetDateErr () {
      console.log('error')
    }
  },
  created () {
    this.getIndexDate()
  }
}
</script>
