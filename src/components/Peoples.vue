<template>
    <div>
        <div v-for='people in peoples'>
            <div class="flex">
                <div class="user">
                    <img :src="people.avatar" class="avatar" />
                    <h3 style="font-weight:600;">{{ people.name }}</h3>
                </div>
                <span :class="[people.status === 'Online' ? 'green' : '']">{{ people.status
                    }}</span>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Peoples',
    data() {
        return {
            peoples: []
        }
    },
    created() {
        {
            this.peoples = [
                {
                    "id": 1,
                    "avatar": "https://i.ibb.co/5sj3Bmh/author-7.webp",
                    "name": "Alice",
                    "status": "Online"
                },
                {
                    "id": 2,
                    "avatar": "https://i.ibb.co/sPcgJG1/author-1.jpg",
                    "name": "Jesy",
                    "status": "Ofline"
                },
                {
                    "id": 3,
                    "avatar": "https://i.ibb.co/47fHpFc/businessman-icon-image-male-avatar-profile-vector-glasses-beard-hairstyle-179728610.jpg",
                    "name": "Jack",
                    "status": "Ofline"
                },
                {
                    "id": 4,
                    "avatar": "https://i.ibb.co/b3BhGkN/author-5.jpg",
                    "name": "Bob",
                    "status": "Online"
                }
            ]
        }
    }
}
</script>
<style>
.homesidebar {
    padding: 15px 25px;
    width: 20%
}

.flex {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px
}

.user {
    display: flex;
    align-items: center;
}

.avatar {
    height: 50px;
    width: 50px;
    display: inline-block;
    margin-right: 10px;
}

.green {
    color: green
}
</style>
