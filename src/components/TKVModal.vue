<script setup>
	import TKVButton from './TKVButton.vue'

	defineProps({
		show: Boolean
	})
</script>

<template>
	<div v-if="show" class="tkvmodal-mask">
		<div class="tkvmodal-container">
			<header>
				Karten hinzufügen
			</header>
			<main>
				<div >
					Erfassen Sie hier neue Karten für Ihren Transportpartner
				</div>
				<div>
					Form elements
				</div>
				<div>
					Karten hinzufügen box
				</div>
			</main>
			<footer>
				<TKVButton>Speichern</TKVButton>
			</footer>
		</div>
	</div>
</template>

<style>
	.tkvmodal-mask {
		position: fixed;
		inset:  0;
		background-color: rgba(0,0,0,0.6);
		display:  grid;
		place-items:  center;
	}

	.tkvmodal-container {
		background-color: white;
		max-width: 640px;
		width:  80vw;
	}
	.tkvmodal-container > header {
		height: 3rem;
		padding:  1rem;
		background-color: blue;
		color: white;
	}

	.tkvmodal-container > main {
		height: auto;
		background-color: white;
		padding: 1rem;
	}
	
	.tkvmodal-container > footer {
		height: 3rem;
		background-color: lightgray;
		padding: 1rem;
	}
</style>