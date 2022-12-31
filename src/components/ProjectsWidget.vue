<template>
  <div>
    <div>
      <ul
        v-for="project in projects"
        :key="project.id"
      >
        <li class="flex">
          <div>
            <span>{{ project.project }}</span>
          </div>
          <div>
            <span class="green">+{{ project.current }} </span>
            <span>{{ project.total }}</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
	name: 'ProjectsWidget',
	data () {
		return {
			projects: [
				{
					id: 1,
					project: 'Descovery',
					current: 12,
					total: 564
				},
				{
					id: 2,
					project: 'Bank',
					current: 16,
					total: 564
				},
				{
					id: 3,
					project: 'Electric',
					current: 14,
					total: 564
				},
				{
					id: 4,
					project: 'Fashion',
					current: 15,
					total: 564
				}]
		}
	}

}
</script>
<style scoped>
.green {
	margin-right: 10px;
}
</style>
