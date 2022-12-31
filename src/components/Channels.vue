<template>
	<div>
		<div>
			<ul v-for="channel in channels" :key="channel.id">
				<li class="flex">
					<div>
						<span>{{ channel.channel }}</span>
					</div>
					<div>
						<span class="green">+{{ channel.current }} </span>
						<span>{{ channel.total }}</span>
					</div>
				</li>
			</ul>
		</div>
	</div>
	</div>
</template>
<script>
export default {
	name: 'ChannelsComponent',
	data() {
		return {
			channels: [
				{
					id: 1,
					channel: 'Payment',
					current: 12,
					total: 564
				},
				{
					id: 2,
					channel: 'Desgin',
					current: 16,
					total: 564
				},
				{
					id: 3,
					channel: 'Sales',
					current: 14,
					total: 564
				},
				{
					id: 4,
					channel: 'Marketing',
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