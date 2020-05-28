<template>
    <view>
		<iheader :showIcon="true" :showSearch="true"></iheader>
        <web-view :webview-styles="webviewStyles" :src="url"></web-view>
    </view>
</template>

<script>
	import iheader from '../../components/header.vue'
    export default {
		components: {
			iheader
		},
        data() {
            return {
                webviewStyles: {
                    progress: {
                        color: '#FF3333'
                    }
                },
				url: ''
            }
        },
		onLoad: function (option){
			this.url = option.url
		},
		
    }
</script>

<style>

</style>