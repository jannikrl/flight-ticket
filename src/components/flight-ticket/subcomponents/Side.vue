<template>
	<div class="side">
		<header>
			<span>Premium Economy</span>
			<rating :valueAtBottom="true" :value="rating"></rating>
		</header>

		<footer>
			<span>27.229 <small>DKK</small></span>
			<btn color="button-primary" :block="true">Vælg</btn>
		</footer>
	</div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	.side {
		display: flex;
		flex-direction: column;
		justify-content: space-between;

		height: 100%;
		padding: $box-padding;

		header {
			span {
				display: block;
				font-size: 10px;
				opacity: 0.5;
				float: left;
			}
		}

		footer {
			text-align: right;

			span {
				display: block;
				font-size: 20px;
				font-weight: 700;
				margin-bottom: 3px;

				small {
					font-weight: normal;
					font-size: 14px;
				}
			}
		}

		.rating {
			float: right;
		}
	}
</style>

<script>
import Rating from '../../Rating'
import Btn from '../../Button'

export default {
	props: {
		rating: {
			type: Number
		}
	},

	components: {
		Rating,
		Btn,
	}
}
</script>