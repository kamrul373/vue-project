<template>
	<div class="homesidebar">
		<div class="widgets">
			<h3 class="sidebar-title">Direct Messages</h3>
			<PeoplesWidget></PeoplesWidget>
			<h3 class="sidebar-title">#Channels</h3>
			<ChannelsComponent></ChannelsComponent>
			<h3 class="sidebar-title">
				#Projects
			</h3>
			<ProjectsWidget></ProjectsWidget>
		</div>
	</div>
</template>

<script>
import PeoplesWidget from './Peoples.vue'
import ChannelsComponent from '../components/Channels.vue'
import ProjectsWidget from '../components/ProjectsWidget.vue'
export default {
	name: 'HomeSidebar',
	components: {
		PeoplesWidget,
		ChannelsComponent,
		ProjectsWidget
	}
}
</script>
<style>
.homesidebar {
	padding: 15px 25px;
	width: 25%
}

.widgets {
	padding: 0 15px;
}

.sidebar-title {
	padding: 10px 2px;
	color: hsl(0deg, 0%, 21%);
	font-weight: bold
}

@media all and (max-width: 768px) {
	.homesidebar {

		width: 105%
	}
}
</style>
