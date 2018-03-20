<template>
	<button class="button" :class="[{'button-block': block}, color]">
		<slot></slot>
	</button>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	.button {
		// Structure
		color: $default-button-color;
		background-color: $default-button-background-color;
		border: 1px solid $default-button-border-color;
		border-radius: $button-radius;
		font-size: 16px;
		text-align: center;
		padding: 8px 10px;
		transition: all 0.4s;

		&:hover {
			cursor: pointer;
		}

		// Size
		&.button-block {
			width: 100%;
		}

		// Color		
		&.button-primary {
			color: $primary-button-color;
			background-color: $primary-button-background-color;
			border: 1px solid $primary-button-border-color;

			&:hover {
				background-color: $primary-button-background-hover-color;
			}
		}
	}
</style>

<script>
export default {
	props: {
		color: {
			type: String,
			default: 'button-primary',
		},
		block: {
			type: Boolean,
			default: false,
		}
	}
}
</script>