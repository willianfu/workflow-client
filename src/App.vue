<template>
	<div id="app">
		<transition name="router-fade" mode="out-in">
			<router-view v-if="!$route.meta.keepAlive"/>
		</transition>
	</div>
</template>

<script>
  //import layout from './components/layout'
  export default {
    components: {},
    data() {
      return {}
    },
    mounted() {
      let beforeUrl = sessionStorage.getItem('router-path')
      if(beforeUrl === undefined || beforeUrl === ''){
        this.$router.push("/workPanel")
      }else {
        this.$router.push(beforeUrl)
      }

    },
    methods: {}
  }
</script>
<style lang="less">
	@import "@/assets/global";
	:focus {
		outline: -webkit-focus-ring-color auto 0px;
	}
	body {
		margin: 0;
		min-width: 500px;
		background-color: #f5f6f6;
	}
	body,html {margin:0; height:100%;}
	ul {
		padding: 0;
		margin: 0;
		
		li {
			list-style-type: none;
		}
	}

</style>
