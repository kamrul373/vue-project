<template>
    <div class="homesidebar">
        <h3 class="card-header-title">Direct Messages</h3>
        <Peoples></Peoples>
        <Channels></Channels>
    </div>
</template>

<script>
import Peoples from './Peoples.vue'
import Channels from '../components/Channels.vue'
export default {
    name: 'HomeSidebar',
    components: {
        Peoples,
        Channels
    }
}
</script>
<style>
.homesidebar {
    padding: 15px 25px;
    width: 20%
}
</style>
