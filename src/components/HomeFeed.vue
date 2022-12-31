<template>
	<div class="feed">
		<h2 class="body-title">Feeds</h2>
		<div v-for="post in posts" :key="post.id">
			<div class="post-header">
				<img :src="post.avatar" :alt="post.name" class="avatar">
				<strong>{{ post.name }}</strong>
				<span>{{ post.time }}</span>
			</div>
			<div class="post-body">
				<p>{{ post?.text }}</p>
				<div v-if="post?.img">
					<img :src="post?.img" :alt="post?.name" class="post-img" />
				</div>
			</div>
		</div>
	</div>
</template>
 
<script>
export default {
	name: 'HomeFeed',
	data() {
		return {
			posts: [
				{
					"id": 1,
					"avatar": "https://i.ibb.co/5sj3Bmh/author-7.webp",
					"name": "Alice",
					"status": "Online",
					'text': "Beautiful things can happen when you distance yourself from the negative.",
					"img": "",
					"time": "7.00 PM"
				},
				{
					"id": 2,
					"avatar": "https://i.ibb.co/sPcgJG1/author-1.jpg",
					"name": "Jesy",
					"status": "Ofline",
					"text": "",
					'img': "https://previews.123rf.com/images/steffens/steffens0908/steffens090800257/5367902-nature-of-some-beautiful-flowers.jpg",
					"time": "7.30 PM"
				},
				{
					"id": 3,
					"avatar": "https://i.ibb.co/47fHpFc/businessman-icon-image-male-avatar-profile-vector-glasses-beard-hairstyle-179728610.jpg",
					"name": "Jack",
					"status": "Ofline",
					"text": "Technology will not replace great teachers but technology in the hands of great teachers can be transformational.",
					'img': "https://static.vecteezy.com/system/resources/previews/002/202/047/original/blue-high-tech-futuristic-cyberspace-technology-background-free-vector.jpg",
					"time": "5.30 PM"
				},
				{
					"id": 4,
					"avatar": "https://i.ibb.co/b3BhGkN/author-5.jpg",
					"name": "Bob",
					"status": "Online",
					"text": "Life is a mirror and will reflect back to the thinker what he thinks into it.",
					'img': "https://www.news-medical.net/images/news/ImageForNews_722328_16605707865419041.jpg",
					"time": "4.30 PM"
				}
			]
		}
	}
}
</script>

<style>
.feed {
	width: 70%;
	margin: 0 auto
}

.feed h2.body-title {
	font-size: 18px;
	padding: 10px 0;
	font-weight: 700;
}

.post-header {
	display: flex;
	column-gap: 10px;
	align-items: center;
}

.post-body {
	padding: 10px 20px 20px 70px;
}

.post-img {
	width: 60%;
	padding: 10px 0
}

@media all and (max-width: 768px) {
	.feed {
		width: 90%;
		margin: 0 auto
	}

	.post-img {
		width: 100%;

	}
}
</style>
