<script type="ts">
	export let direction: 'column' | 'row' = 'column';
	export let breakpoint: 'small' | 'medium' | undefined = undefined;
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
	class:break-small={breakpoint === 'small'}
	class:break-medium={breakpoint === 'medium'}
	class:row={direction === 'row'}
	class:column={direction === 'column'}
>
	<slot />
</div>

<style type="scss">
	// Bascics
	div {
		display: flex;
	}
	.column {
		flex-direction: column;
	}
	.row {
		flex-direction: row;
	}

	// Sizes
	.small {
		gap: var(--bones-gap-s, 2rem);
	}
	.medium {
		gap: var(--bones-gap-m, 4rem);
	}
	.large {
		gap: var(--bones-gap-l, 6rem);
	}

	// Breakpoints
	// TODO: make this dynamic
	$breakpoints: (
		small: 40em,
		medium: 65em
	);
	.break-small.row {
		$size: map-get($breakpoints, 'small');

		@media only screen and (min-width: $size) {
			flex-direction: column;
		}
	}
	.break-medium.row {
		$size: map-get($breakpoints, 'medium');

		@media only screen and (min-width: $size) {
			flex-direction: column;
		}
	}
	.break-small.column {
		$size: map-get($breakpoints, 'small');

		@media only screen and (min-width: $size) {
			flex-direction: row;
		}
	}
	.break-medium.column {
		$size: map-get($breakpoints, 'medium');

		@media only screen and (min-width: $size) {
			flex-direction: row;
		}
	}
</style>
