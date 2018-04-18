<template>
  <div>
    <index-header></index-header>
    <index-footer></index-footer>
  </div>
</template>
<script>
import IndexHeader from './header'
import IndexFooter from './footer'
export default {
  name: 'index',
  components: {
    IndexHeader,
    IndexFooter
  }
}
</script>
