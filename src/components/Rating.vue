<template>
	<div class="rating" :class="{'valueAtBottom' : valueAtBottom}">
		<span>{{value}}</span>
		
		<i class="fa fa-smile-o" v-if="value > 7"></i>
		<i class="fa fa-meh-o" v-else-if="value > 3"></i>
		<i class="fa fa-frown-o" v-else></i>
	</div>
</template>

<style lang="scss" scoped>
	.rating {
		color: rgb(0,149,177);
		display: flex;
		align-items: center;

		span {
			font-size: 16px;
			font-weight: bold;
			margin: 0 5px;
		}

		i {
			font-size: 28px;
		}
	}

	.rating.valueAtBottom {
		flex-direction: column-reverse;

		span {
			font-size: 16px;
		}
	}
</style>

<script>
export default {
	props: {
		value: {
			type: Number,
			default: 5.5,
		},
		valueAtBottom: {
			type: Boolean,
			default: false,
		}
	}
}
</script>