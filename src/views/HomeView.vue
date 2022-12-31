<template>
	<div class="home">
		<HomeSidebar></HomeSidebar>
		<HomeFeed></HomeFeed>
	</div>
</template>

<script>
import { defineComponent } from 'vue'
import HomeSidebar from '../components/HomeSidebar.vue'
import HomeFeed from '@/components/HomeFeed.vue';

export default defineComponent({
	name: 'HomeView',
	components: {
		HomeSidebar,
		HomeFeed
	}
})
</script>
<style>
.home {
	display: flex;
	column-gap: 20px;
}
</style>
