<template>
	<div class="container-form">
		<div class="img-form"></div>
		<div class="form">
			<form>
				<div class="form__name">
					<p>Name Task</p>
					<label for="name"></label>
					<input type="text" id="name" placeholder="Write you name task" />
				</div>
				<div class="form__importance">
					<p>Importance</p>
					<label for="importance"></label>
					<progress id="importance" value="0" max="100"></progress>
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
		background-image: url("../assets/imgForm.jpg");
		background-size: cover;
		background-repeat: no-repeat;
		background-position: top center;
		border-radius: 25px 0 0 25px;
	}
	.form {
		background: #323232;
		border-radius: 0 25px 25px 0;
		width: 90%;
		max-width: 30rem;
		padding: 1rem;
		display: grid;
		grid-template-columns: 1fr;
		justify-items: center;
		.form__btn {
			display: block;
			margin: 2.5rem auto 0 auto;
		}
	}
}
</style>
