<template>
	<div class="favorite">
		<mt-search  v-model="value"  cancel-text="取消"  placeholder="搜索">
		</mt-search>
		<div class="_search">
			
		</div>
		<mt-navbar v-model="selected">
		  <mt-tab-item id="1">选项一</mt-tab-item>
		  <mt-tab-item id="2">选项二</mt-tab-item>
		  <mt-tab-item id="3">选项三</mt-tab-item>
		</mt-navbar>
		
		<!-- tab-container -->
		<mt-tab-container v-model="selected">
		  <mt-tab-container-item id="1">
		    <mt-cell v-for="n in 10" :title="'内容 ' + n" />
		  </mt-tab-container-item>
		  <mt-tab-container-item id="2">
		    <mt-cell v-for="n in 4" :title="'测试 ' + n" />
		  </mt-tab-container-item>
		  <mt-tab-container-item id="3">
		    <mt-cell v-for="n in 6" :title="'选项 ' + n" />
		  </mt-tab-container-item>
		</mt-tab-container>
	</div>
</template>

<script>
	export default {
		name : "favorite",
		data(){
			return {
				value : "",
				selected : "1"
			}
		},
		mounted(){
			this.$emit("to-parent","收藏")
		}
	}
</script>

<style>
</style>