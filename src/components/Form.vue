<template>
	<div>
		<div class="container-form">
			<div class="img-form">
				<div>
					<img src="../assets/cuaderno.png" alt="" />
				</div>
			</div>
			<div class="form">
				<form @submit.prevent="addTasks()">
					<div class="form__name">
						<p>Name Task</p>
						<label for="name"></label>
						<input type="text" id="name" v-model="name" />
					</div>

					<div class="form__colour">
						<p>Colour Task</p>
						<label for="colour"></label>
						<input type="color" id="colour" v-model="colour" />
					</div>

					<button class="form__btn" type="submit">Add Task</button>
				</form>
			</div>
		</div>

		<div v-for="item in tasks" :key="item.id" class="tasks">
			<div class="task" :style="{ background: item.colour }">
				<h1>✏</h1>

				<h3>{{ item.name }}</h3>

				<div class="task.action">
					<img src="../assets/checkbox.png" alt="" />
					<img src="../assets/remove.png" alt="" />
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			name: "",

			colour: "",

			tasks: [],
		};
	},
	methods: {
		addTasks() {
			this.tasks.push({
				name: this.name,

				colour: this.colour,
			});
		},
	},
};
</script>

<style lang="scss" scoped>
.container-form {
	margin: 10rem 0 5rem 0;
	display: grid;
	grid-template-columns: 25rem 15rem;
	box-shadow: 0px 0px 8.4px rgba(0, 0, 0, 0.061),
		0px 0px 28.1px rgba(0, 0, 0, 0.089), 0px 0px 126px rgba(0, 0, 0, 0.15);
	.img-form {
		background-color: #b762c1;
		display: flex;
		justify-content: center;
		align-items: center;

		img {
			min-width: 10rem;
			min-height: 10rem;
			max-width: 13rem;
			max-height: 13rem;
		}
	}
	.form {
		background: #7900ff;
		font-family: monospace;
		color: #fff;
		letter-spacing: 2px;
		font-weight: 700;
		width: 90%;
		max-width: 30rem;
		padding: 1rem;
		display: grid;
		grid-template-columns: 1fr;
		justify-items: center;

		.form__name {
			input {
				border: 2px solid #fff;
				background-color: #b862c100;
				border-radius: 15px;
				height: 1.5rem;
				outline: none;
				padding: 0.3rem 1rem;
			}
		}
		.form__colour {
			margin-top: 2rem;

			input {
				width: 100%;
				cursor: pointer;
			}
		}

		.form__btn {
			display: block;
			margin: 2.5rem auto;
			padding: 1rem;
			background-image: #fff;
			border-radius: 15px;
			border: none;
			cursor: pointer;
			&:hover {
				transform: scale(1.1);
				background-color: rgb(163, 159, 159);
				transition: 0.3s ease-in-out;
			}
		}
	}
}
.tasks {
	.task {
		padding: 0.5rem 2rem;
		display: flex;
		gap: 3rem;
		justify-content: space-between;
		align-items: center;
		border: 2px #111 solid;
		margin-bottom: 1rem;
		img {
			width: 2.5rem;
			height: 2.5rem;
		}
	}
}
</style>
