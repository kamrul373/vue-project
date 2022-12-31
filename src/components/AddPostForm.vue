<template>
	<div class="addpost">
		<div>
			<h3 class="sidebar-title">Add New Post</h3>
			<form @submit="handleAddPost">
				<div class=" field-body">
					<div class="field">
						<div class="control has-icons-right">
							<textarea rows="4" class="textarea" name="text" required></textarea>
						</div>
					</div>
				</div>
				<div class="field-body">
					<div class="field">
						<div class="control has-icons-right">
							<input type="file" name="img" @change="handleImage" />
						</div>
					</div>
				</div>
				<input type="submit" value="Publish" class="addpostbtn">
			</form>
		</div>
	</div>
</template>

<script>
export default {
	name: 'AddPostForm',
	data() {
		return {
			img: ''
		}
	},
	methods: {
		handleAddPost(e) {
			e.preventDefault()
			const text = e.target.text.value
			const time = new Date()
			const currentTime = time.toLocaleString('en-US', { hour: 'numeric', minute: 'numeric', hour12: true })
			const postData = {
				"id": Math.floor(Math.random() * 100000),
				"avatar": "https://i.ibb.co/5sj3Bmh/author-7.webp",
				"name": "Alice",
				'text': text,
				"img": this.img,
				"time": currentTime
			}
			this.$emit('postdata', postData)
			e.target.reset()
		},
		handleImage(e) {
			const image = e.target.files[0]
			return this.img = URL.createObjectURL(image)
		}
	}
}
</script>
<style scoped>
.addpost {
	margin-top: 25px;
}

form {
	display: flex;
	flex-direction: column;
	gap: 10px;
}

textarea {
	width: 100%;
	margin-top: 10px
}

.addpostbtn {
	background-color: #0F77EA;
	color: #FFFFFF;
	padding: 10px;
	border: none;
	width: 100px
}
</style>
