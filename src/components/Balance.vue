<!-- eslint-disable vue/multi-word-component-names -->
<template>

	<div id="balance">
		<div>
			<p>My balance</p>
			<h2>$921.48</h2>
		</div>

		<img src="src/assets/logo.svg">
	</div>

</template>

<style>
	#balance {
    width: 90%;
    height: 20%;

    padding-right: 5%;
    padding-left: 5%;

    background-color: hsl(10, 79%, 65%);
    color: white;

    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

	}
</style>