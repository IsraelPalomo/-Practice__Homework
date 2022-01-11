<template>
	<div class="container-form">
		<div class="img-form"></div>
		<div class="form">
			<form>
				<div class="form__name">
					<p>Name Task</p>
					<label for="name"></label>
					<input type="text" id="name" />
				</div>
				<div class="form__importance">
					<p>Importance</p>
					<label for="importance"></label>
					<div class="container">
						<div>
							<p>Baja</p>
							<input type="radio" id="importance" value="Baja" />
						</div>
						<div>
							<p>Alta</p>
							<input type="radio" id="importance" value="Alta" />
						</div>
					</div>
				</div>
				<div class="form__colour">
					<p>Colour Task</p>
					<label for="colour"></label>
					<input type="color" id="colour" />
				</div>
				<div class="form__reminder">
					<p>Reminder</p>
					<label for="reminder"></label>
					<input type="time" id="reminder" placeholder="Time of reminder" />
				</div>
				<button class="form__btn" type="submit">Add Task</button>
			</form>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container-form {
	display: grid;
	grid-template-columns: 25rem 15rem;
	.img-form {
		background-color: #b762c1;
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
		.form__importance {
			.container {
				display: flex;
				gap: 1rem;
			}
		}
		.form__btn {
			display: block;
			margin: 2.5rem auto 0 auto;
		}
	}
}
</style>
