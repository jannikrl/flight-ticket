<template>
	<div class="footer-actions">
		<rating :value="rating"></rating>

		<span>Premium Economy</span>

		<a>15.797 <small>DKK</small> <i class="fa fa-angle-right"></i></a>
	</div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	.footer-actions {
		padding: $box-padding;
		display: flex;
		align-items: center;

		.rating {
			float: left;
		}

		span {
			opacity: 0.5;
			margin-left: 8px;
		}

		a {
			flex: 1;
			text-align: right;
			font-size: 19px;
			cursor: pointer;
			font-weight: bold;

			small {
				font-size: 13px;
				font-weight: normal;
			}

			i {
			    font-size: 26px;
			    height: 28px;
			    vertical-align: middle;
			    margin-left: 8px;
			}

			&:hover {
				text-decoration: none;
			}
		}
	}
</style>

<script>
import Rating from 'src/components/Rating'

export default {
	props: {
		rating: {
			type: Number
		}
	},

	components: {
		Rating,
	}
}
</script>