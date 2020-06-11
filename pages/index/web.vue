<template>
    <view>
		<iheader :showIcon="true" :showSearch="true"></iheader>
        <web-view :webview-styles="webviewStyles" :src="url"></web-view>
    </view>
</template>

<script>
	import iheader from '../../components/header.vue'
	import util from '../../utils/util.js'
    export default {
		components: {
			iheader
		},
        data() {
            return {
                webviewStyles: {
                    progress: {
                        color: '#00aaff'
                    }
                },
				url: ''
            }
        },
		onLoad: function (option){
			this.url = option.url
			
			// #ifdef APP-PLUS
			var currentWebview = this.$scope.$getAppWebview()
			//此对象相当于html5plus里的plus.webview.currentWebview()。在uni-app里vue页面直接使用plus.webview.currentWebview()无效，非v3编译模式使用this.$mp.page.$getAppWebview()
			setTimeout(function() {
				var sysInfo = util.getSysInfo()
				var statusBarHeight = sysInfo.statusBarHeight
				var titleBarHeight = sysInfo.titleBarHeight
				var windowHeight = sysInfo.windowHeight
				var top = statusBarHeight + titleBarHeight
				var height = windowHeight - top
				
				var wv = currentWebview.children()[0]
				wv.setStyle({top:top,height:height})
			}, 1000); //如果是页面初始化调用时，需要延时一下
			// #endif
		}
    }
</script>

<style>

</style>