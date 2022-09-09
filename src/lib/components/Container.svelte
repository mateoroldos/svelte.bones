<script type="ts">
	export let width: 'small' | 'medium' | 'large' | 'full' = 'medium';
</script>

<div class={width}>
	<slot />
</div>

<style>
	div {
		margin-inline: auto;
	}
	.small {
		width: min(var(--bones-container-width-porcentage, 90%), var(--container-s, 50rem));
	}
	.medium {
		width: min(var(--bones-container-width-porcentage, 90%), var(--container-m, 75rem));
	}
	.large {
		width: min(var(--bones-container-width-porcentage, 90%), var(--container-l, 85rem));
	}
	.full {
		width: 90%;
	}
</style>
