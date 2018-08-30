<template>
  <li class="item" @click="handleDelete">{{content}}</li>
</template>

<script>
export default {
 	props:['content','index'],
 	methods:{
 		handleDelete(){
 				this.$emit('delete',this.index)
 		}
 	}
}
</script>
<!--通过 scoped修饰符 增加css的作用域为当前组件-->
<style scoped>
	.item{
		color:#0f0
	}
</style>
