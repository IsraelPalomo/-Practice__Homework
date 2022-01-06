<template>
	<div class="home">
		<Form />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Form from "@/components/Form.vue";

@Component({
	components: { Form },
})
export default class Home extends Vue {}
</script>
<style lang="scss" scoped>
.home {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 100%;
	height: 100vh;
	box-sizing: border-box;
}
</style>
