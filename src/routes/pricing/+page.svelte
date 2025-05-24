<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials=[
    {
      name: "Amara Odette",
      position: "Founder & CEO",
      company: "Matya",
      quote: "Uncommon helped us increase signups by 35% after launch. As a solo founder, I don’t have time to handhold an agency — this felt like working with a senior team ready on day one.",
      image: "/generated/image-a-confident-black-female-founder-posing-.webp"
    },
    {
      name: "Rafael Cordero",
      position: "CTO",
      company: "AltaFin",
      quote: "We created our investor deck, hiring page, and first ad campaign in under a week. Engineers were able to keep building while Uncommon handled the positioning. It saved us well over 60 hours.",
      image: "/generated/image-a-poised-latino-male-cto-posing-for-a-pr.webp"
    },
    {
      name: "Hana Liu",
      position: "Head of Operations",
      company: "Verde",
      quote: "We used to spend weeks just wrangling designers and approvals. With Uncommon, we shipped a site in 4 days that ended up converting 28% better — no back-and-forth necessary.",
      image: "/generated/image-an-assured-east-asian-female-operations-.webp"
    }
  ]
/>

<CallToAction
  title="Build your company faster"
  subtitle="Get everything you need to launch, raise and grow in one tool"
  description="Uncommon helps you reach product-market fit with conversion-optimized websites, polished decks and smart ads. Used by startups backed by Sequoia. Try it free, no credit card required."
  imageSrc="/generated/image-a-cheerful-startup-founder-in-a-modern-o.webp"
  callsToAction={[
    {
      href: '/get-started',
      label: 'Start for free',
      variant: 'primary'
    },
    {
      href: '/contact',
      label: 'Talk to sales',
      variant: 'secondary'
    }
  ]}
/>
