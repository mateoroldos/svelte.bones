<script type="ts">
	export let gap: 'small' | 'medium' | 'large' | 'none' | number = 'medium';
	export let align: 'flex-start' | 'flex-end' | 'center' | 'baseline' | 'stretch' = 'center';
	export let justify:
		| 'flex-start'
		| 'flex-end'
		| 'center'
		| 'space-between'
		| 'space-around'
		| 'space-evenly' = 'center';
</script>

<div
	class={typeof gap === 'string' ? gap : ''}
	style={`align-items: ${align}; justify-content: ${justify}; ${
		typeof gap === 'number' ? `gap: ${gap}rem` : ''
	}`}
>
	<slot />
</div>

<style type="scss">
	div {
		display: flex;
		flex-direction: row;
	}
	.small {
		gap: var(--bones-gap-s, 2rem);
	}
	.medium {
		gap: var(--bones-gap-m, 4rem);
	}
	.large {
		gap: var(--bones-gap-l, 6rem);
	}
</style>
