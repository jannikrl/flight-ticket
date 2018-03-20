<template>
  <div class="flight-route">
  	<div class="airline">
  		<p>Scandinavian Airlines System</p>
  		<img src="../../../assets/sas-logo.svg">
  	</div>

  	<div class="departure">
  		<span>CPH <strong>14:15</strong></span>
  	</div>

  	<div class="duration">
  		30t 40m
  	</div>

  	<div class="arrival">
  		<span><strong>06:55</strong> SYD</span>
  	</div>
  </div>
</template>

<!-- The "scoped" attribute limits CSS to this component only -->
<style lang="scss" scoped>
	@import 'src/assets/scss/_variables';

	$flight-ticket-border-color: #e3e6e7;

	.flight-route {
	  display:flex;
	  margin-top: 25px;
	  border-bottom: 1px solid $flight-ticket-border-color;

	  > div {
	  	border-right: 1px dotted $flight-ticket-border-color;
	  	margin: $box-padding 0;
	  	padding: 0 $box-padding;
	  	font-size: 14px;

	  	&:last-child {
	  		border-right: 0px;
	  	}
	  }

	  .airline {
	  	flex: 0 0 45px;
	  	position: relative;

  		p {
  			position: absolute;
			top: -30px;
			left: $box-padding;
			min-width: 500px;
			font-size: 10px;
			opacity: 0.5;
  		}

	  	img {
	  		width: 32px;
	  		margin-right: 15px;
	  	}
	  }

	  .departure,
	  .duration,
	  .arrival {
		display: flex;
	  	align-items: center;

	  	white-space: nowrap;
	  }

	  .departure,
	  .arrival {
	  	font-size: 16px;
	  	font-weight: 600;

	  	strong {
	  		font-weight: 700;
	  		margin: 0 5px;
	  	}
	  }

	  .departure {
	  	justify-content: flex-end;

	  	flex: 1 1 40%;
	  }

	  .duration {
	  	justify-content: center;

	  	flex: 1 1 20%;
	  }

	  .arrival {
	  	justify-content: flex-start;

	  	flex: 1 1 40%;
	  }
	}
</style>