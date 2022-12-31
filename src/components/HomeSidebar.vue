<template>
	<div class="homesidebar">
		<h3 class="card-header-title">Direct Messages</h3>
		<Peoples></Peoples>
		<ChannelsComponent></ChannelsComponent>
		<ProjectsWidget></ProjectsWidget>
	</div>
</template>

<script>
import Peoples from './Peoples.vue'
import ChannelsComponent from '../components/Channels.vue'
import ProjectsWidget from '../components/ProjectsWidget.vue'
export default {
	name: 'HomeSidebar',
	components: {
		Peoples,
		ChannelsComponent,
		ProjectsWidget
	}
}
</script>
<style>
.homesidebar {
	padding: 15px 25px;
	width: 20%
}
</style>
