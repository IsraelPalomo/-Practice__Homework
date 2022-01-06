<template>
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
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.form {
	background: #323232;
	border-radius: 25px;
	width: 80%;
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
</style>
