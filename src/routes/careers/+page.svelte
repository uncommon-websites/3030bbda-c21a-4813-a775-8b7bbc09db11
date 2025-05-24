<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Flexible Work",
			description: "Remote-first with flexible hours that respect work-life balance.",
			icon: IconBriefcase
		},
		{
			title: "Growth Opportunities",
			description: "Continuous learning with mentorship and education stipends.",
			icon: IconUsers
		},
		{
			title: "Comprehensive Benefits",
			description: "Health coverage, retirement plans, and generous paid time off.",
			icon: IconHeart
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Sofia Alvarez",
    position: "Operations Coordinator",
    company: "Operations Team",
    quote: "As a Latina in tech, it means so much to feel not just heard but truly seen. There’s real mutual respect here—the kind where every idea gets aired, and everyone's got your back when it counts.",
    image: "/generated/image-a-latina-woman-operations-coordinator-sm.webp"
  },
  {
    name: "Michael Chen",
    position: "Senior Developer",
    company: "Engineering Team",
    quote: "Uncommon is the place to push your skills and actually see progress every month. The challenges keep things exciting and there’s always space to learn, experiment, and grow as an engineer.",
    image: "/generated/image-an-east-asian-man-software-developer-smi.webp"
  },
  {
    name: "Priya Sharma",
    position: "Product Designer",
    company: "Design Team",
    quote: "I love that ideas win here, not titles. It’s a culture where collaboration across disciplines sparks creativity and where I get the trust and freedom to build things that really matter.",
    image: "/generated/image-a-south-asian-woman-product-designer-exu.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Submit your application",
    description: "Tell us how you want to contribute and share links to your best work. No long cover letter needed."
  },
  {
    step: 2,
    title: "Intro call",
    description: "Short chat to get to know each other and answer your questions."
  },
  {
    step: 3,
    title: "Work sample or paid challenge",
    description: "Collaborate on a practical assignment to experience how we solve problems together."
  },
  {
    step: 4,
    title: "Final interview with the founder",
    description: "Focused discussion on your strengths and how you work best."
  },
  {
    step: 5,
    title: "Offer and onboarding",
    description: "Simple, fast process. If we match, you’ll start building with us right away."
  }
];

	const values = [
	{
		icon: IconHeart,
		title: "Founder empathy",
		description: "We obsess over making Uncommon intuitive and frustration-free for real builders."
	},
	{
		icon: IconUsers,
		title: "Bias for action",
		description: "Move fast, experiment, and ship. Clear priorities, real results."
	},
	{
		icon: IconGlobe,
		title: "Low ego, high standards",
		description: "Build with compassion and give direct, honest feedback. We keep things simple and drama-free."
	}
];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build tools founders rely on"
	subtitle="Join the team shaping how startups launch, grow, and win"
	imageSrc="/generated/image-a-modern-tech-startup-office-with-a-dive.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
