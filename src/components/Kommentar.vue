<script setup>
	defineProps(['user', 'date'])
</script>

<template>
	<div class="comment  border-bottom pb-2 ">
	    <div class="text-left ">
	        <slot></slot>
	    </div>

	    <div class="comment-username">
	        <div class="text-left text-truncate">
	            {{user}}
	        </div>
	        <div>
	            {{date}}
	        </div>
	    </div>
	    
	    <div>
	        <div class="text-center bg-primary text-white">
	            E
	        </div>
	    </div>
	    <div>
	        <div class="text-center bg-danger text-white">
	            D
	        </div>
	    </div>
	</div>
</template>

<style>

    div.comment {
        display: grid;
        grid-template-columns: 1fr 16rem  1.25rem 1.25rem;
        column-gap: 0.5rem;
        font-size: small;
    }

    div.comment-username {
        display: grid; 
        grid-template-columns: auto 5rem;
        column-gap: 0.25rem;
    }
</style>