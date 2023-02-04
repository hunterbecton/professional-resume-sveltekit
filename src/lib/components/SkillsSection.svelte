<script>
	import SectionHeader from './SectionHeader.svelte';

	export let skills;
</script>

<section class="skills">
	<div class="skills__container">
		<SectionHeader title="Skills" />
		<div class="skills__list">
			{#each skills as skill}
				<p class="skills__item p-base">{skill}</p>
			{/each}
		</div>
	</div>
</section>

<style>
	.skills {
		padding: 1.5rem 2rem 4rem 2rem;
	}

	.skills__container {
		max-width: 67rem;
		margin: 0 auto;
	}

	.skills__list {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		gap: 1rem 2rem;
		margin-top: 0.5rem;
	}

	.skills__item {
		color: var(--neutral-eight);
		font-weight: 400;
	}

	@media (max-width: 640px) {
		.skills__list {
			grid-template-columns: repeat(2, 1fr);
		}
	}
</style>
