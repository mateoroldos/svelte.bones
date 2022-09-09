<script type="ts">
	export let minWidth: 'small' | 'medium' | 'large' = 'medium';
	export let gap: 'small' | 'medium' | 'large' = 'medium';
</script>

<div class={`min-width-${minWidth} gap-${gap}`}>
	<slot />
</div>

<style type="scss">
	div {
		display: grid;
		width: 100%;
	}
	.min-width-small {
		grid-template-columns: repeat(
			auto-fill,
			minmax(min(var(--bones-column-min-width-s, 20rem), 100%), 1fr)
		);
	}
	.min-width-medium {
		grid-template-columns: repeat(
			auto-fill,
			minmax(min(var(--bones-column-min-width-m, 25rem), 100%), 1fr)
		);
	}
	.min-width-large {
		grid-template-columns: repeat(
			auto-fill,
			minmax(min(var(--bones-column-min-width-l, 30rem), 100%), 1fr)
		);
	}
	.gap-small {
		grid-gap: var(--bones-gap-s, 2rem);
	}
	.gap-medium {
		grid-gap: var(--bones-gap-m, 4rem);
	}
	.gap-large {
		grid-gap: var(--bones-gap-l, 6rem);
	}
</style>
