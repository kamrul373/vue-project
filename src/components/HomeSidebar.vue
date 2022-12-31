<template>
    <div class="homesidebar">
        <h3 class="card-header-title">Direct Messages</h3>
        <Peoples></Peoples>
    </div>
</template>

<script>
import Peoples from "./Peoples.vue"
export default {
    name: 'HomeSidebar',
    components: {
        Peoples
    }
}
</script>
<style>
.homesidebar {
    padding: 15px 25px;
    width: 20%
}
</style>
