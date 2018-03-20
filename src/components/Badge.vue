<template>
	<div class="badge" :class="[color]">
		<i class="fa fa-info-circle"></i>
		<span>
			<slot></slot>
		</span>
	</div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	.badge {
		// Structure
		border: 1px solid $default-badge-border-color;
		background-color: $default-badge-background-color;
		display: inline-block;
		padding: 2px 8px 3px;
		border-radius: 99px;

		i {
			opacity: 0.5;
			font-size: 12px;
		}

		span {
			opacity: 0.5;
			font-size: 10px;
			font-weight: bold;
		}

		&:hover {
			cursor: pointer;
		}

		// Color
		&.badge-primary {
			border: 1px solid $primary-badge-border-color;
			background-color: $primary-badge-background-color;

			&:hover {
				background-color: $primary-badge-background-hover-color;
			}	
		}
	}
</style>

<script>
export default {
	props: {
		color: {
			type: String,
			default: 'badge-primary'
		}
	}
}
</script>