<script>
	import ExperienceSection from '../lib/components/ExperienceSection.svelte';
	import Contact from '../lib/components/Contact.svelte';
	import SkillsSection from '../lib/components/SkillsSection.svelte';
	import { resume } from '../lib/content/resume';

	let { name, description, contacts, experiences, skills } = resume;
</script>

<svelte:head>
	<title>Susan Minerva | Web Developer in Atlanta, GA</title>
	<meta name="title" content="Susan Minerva | Web Developer in Atlanta, GA" />
	<meta
		name="description"
		content="Susan Minerva, an expert web developer in Atlanta, creates user-friendly, visually appealing websites."
	/>
	<meta name="keywords" content="web development, developer, programmer" />
	<meta name="robots" content="index, nofollow" />
</svelte:head>

<main class="wrapper">
	<Contact {name} {description} {contacts} />
	<ExperienceSection {experiences} />
	<SkillsSection {skills} />
</main>

<style>
	.wrapper {
		background-color: var(--white);
	}
</style>
