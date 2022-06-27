<script type="ts">
	export let gap: 'small' | 'medium' | 'large' = 'medium';
	export let align: 'flex-start' | 'flex-end' | 'center' | 'baseline' | 'stretch' = 'center';
	export let justify:
		| 'flex-start'
		| 'flex-end'
		| 'center'
		| 'space-between'
		| 'space-around'
		| 'space-evenly' = 'center';
</script>

<div class={gap} style={`align-items: ${align}; justify-content: ${justify}`}>
	<slot />
</div>

<style type="scss">
	div {
		display: flex;
		flex-direction: row;
	}
	.small {
		gap: var(--gap-small, 2rem);
	}
	.medium {
		gap: var(--gap-medium, 4rem);
	}
	.large {
		gap: var(--gap-large, 6rem);
	}
</style>
