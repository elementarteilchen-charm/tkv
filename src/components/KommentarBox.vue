<script setup>
	import Kommentar from './Kommentar.vue'
</script>

<template>
	<div class="comment-box border px-2 py-2">
		
		<Kommentar user="Unbekannter User" date="14.6.2022">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. 
		</Kommentar>
		<Kommentar user="Peter mit einem langen Namen" date="14.6.2022">
			Pariatur accusamus amet laborum nemo rerum! 
		</Kommentar>
		<Kommentar user="Alex User" date="14.6.2022">
			Voluptates.		
		</Kommentar>
		<Kommentar user="Balazs User" date="14.6.2022">
			Maxime, et modi harum perspiciatis temporibus reprehenderit, sequi ratione deserunt, autem laborum illum ut nostrum corrupti molestiae similique doloremque adipisci, dicta fugiat.	
		</Kommentar>
		<Kommentar user="Günther User" date="14.6.2022">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. 
		</Kommentar>
				<Kommentar user="Alex User" date="14.6.2022">
			Voluptates.		
		</Kommentar>
		<Kommentar user="Balazs User" date="14.6.2022">
			Maxime, et modi harum perspiciatis temporibus reprehenderit, sequi ratione deserunt, autem laborum illum ut nostrum corrupti molestiae similique doloremque adipisci, dicta fugiat.	
		</Kommentar>
		<Kommentar user="Günther User" date="14.6.2022">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. 
		</Kommentar>
		
	</div>
</template>

<style>
    div.comment-box {
        display:  grid;
        grid-row-gap: 0.5rem;
        height:  12rem;
        overflow:  hidden;
        overflow-y:  auto;
    }
</style>