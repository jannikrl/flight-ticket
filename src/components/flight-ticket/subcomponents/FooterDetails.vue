<template>
	<div class="footer-details">
		<badge>Se detaljer</badge>

		<a href="#" class="booking-service">
			<span class="name">KoreanAir</span>
			<span class="price">27.229 DKK</span>
		</a>
	</div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	.footer-details {
		padding: $box-padding;

		.booking-service {
			color: #21a33d;
		    font-size: 10px;
		    font-weight: 700;
		    line-height: 12px;
		    text-align: right;
		    float: right;

			span {
				display: block;
			}
		}
	}
</style>

<script>
import Badge from '../../Badge'

export default {
	components: {
		Badge
	}
}
</script>