<script>
	import Experience from './Experience.svelte';
	import SectionHeader from './SectionHeader.svelte';

	export let experiences;
</script>

<section class="experience">
	<div class="experience__container">
		<SectionHeader title="Experience" />
		{#each experiences as experience}
			<Experience {experience} class="experience__item" />
		{/each}
	</div>
</section>

<style>
	.experience {
		padding: 3rem 2rem;
	}

	.experience__container {
		max-width: 67rem;
		margin: 0 auto;
	}

	.experience__container > :global(.experience__item:not(:first-of-type)) {
		margin-top: 3rem;
	}

	@media (max-width: 640px) {
		.experience {
			padding-left: 1rem;
			padding-right: 1rem;
		}
	}
</style>
