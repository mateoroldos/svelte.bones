<script type="ts">
	export let paddingTop: 'none' | 'small' | 'medium' | 'large' = 'medium';
	export let paddingBottom: 'none' | 'small' | 'medium' | 'large' = 'medium';
</script>

<section class={`padding-top-${paddingTop} padding-bottom-${paddingBottom}`}>
	<slot />
</section>

<style>
	.padding-top-small {
		padding-block-start: var(--section-padding-s, 2rem);
	}
	.padding-top-medium {
		padding-block-start: var(--section-padding-m, 4rem);
	}
	.padding-top-large {
		padding-block-start: var(--section-padding-m, 6rem);
	}
	.padding-top-none {
		padding-block-start: 0;
	}
	.padding-bottom-small {
		padding-block-end: var(--section-padding-s, 2rem);
	}
	.padding-bottom-medium {
		padding-block-end: var(--section-padding-m, 4rem);
	}
	.padding-bottom-large {
		padding-block-end: var(--section-padding-m, 6rem);
	}
	.padding-bottom-none {
		padding-block-end: 0;
	}
</style>
