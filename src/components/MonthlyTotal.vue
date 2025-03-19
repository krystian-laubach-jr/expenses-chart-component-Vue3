<template>
  
	<div id="total">

	<div>
		<p class="lightBrown">Total this month</p>
		<h1>$478.33</h1>
	</div>

	<div style="text-align: right;">
		<p style="font-weight: 700;">+2.4%</p>
		<p class="lightBrown">from last month</p>
	</div>

	</div>

</template>

<style>

	#total {
		height: 25%;
		border-top: 3px solid hsl(27, 66%, 92%);

		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	#total p,h1 {
		margin: 0;
	}

	.lightBrown {
    color: hsl(28, 10%, 53%);
	}

</style>