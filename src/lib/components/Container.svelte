<script type="ts">
	export let width: 'small' | 'medium' | 'large' | 'full' = 'medium';
</script>

<div class={width}>
	<slot />
</div>

<style>
	.full {
		width: 90%;
	}
	.large {
		width: min(var(--max-width-percent, 90%), var(--container-large, 85rem));
	}
	.medium {
		width: min(var(--max-width-percent, 90%), var(--container-large, 75rem));
	}
	.small {
		width: min(var(--max-width-percent, 90%), var(--container-large, 50rem));
	}
	div {
		background-color: rgb(145, 145, 218);
	}
</style>
