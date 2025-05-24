<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
  {
    title: "Builder obsession",
    description: "Created for founders who care about speed and substance. We cut the busywork so you can focus on real progress."
  },
  {
    title: "Design that works",
    description: "Looking sharp isn’t optional. Every asset is crafted to help you stand out, not blend in."
  },
  {
    title: "Clarity, not clutter",
    description: "No fluff, no filler. Every feature exists to help you sell, hire or raise."
  },
  {
    title: "Move at founder speed",
    description: "Uncommon is fast because opportunity doesn’t wait. Ship in days, not weeks."
  },
  {
    title: "Proof, not promises",
    description: "Every file, deck or site is judged by outcomes—investors, hires, customers. We back up the hype."
  },
  {
    title: "Team of builders, for builders",
    description: "Founded by a builder, for builders. We know what great looks like—and help you show it." 
  }
];
</script>

<SecondaryHero
	title="AI design, built for founding teams"
	subtitle="Websites, decks, and ads to sell, hire, and raise—done right, from day one"
	imageSrc="/generated/image-a-modern-startup-team-collaborating-in-a.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"I started Uncommon because I was tired of wasting time on things that didn’t move the needle. As a founder myself, I kept running into the same problem: starting from scratch on a deck, a site, a campaign — juggling freelancers or trying to write copy late at night just to get the story straight. I wanted something fast, smart, and good. So I built it.",
		"Uncommon is an AI-powered company building tool that helps founders speak clearly, show up professionally, and move fast. Just tell it what you’re working on, and get a website, pitch deck, ads — everything — built to help you sell, hire, or raise. No templates. No guessing. Just a story that works.",
		"It’s already trusted by teams like Squint and nsave — who both raised from Sequoia — to look sharp, sound right, and stay focused on building. I'm Thilo Konzok, and I built Uncommon for founders who'd rather spend time making progress than formatting slides. If that’s you, we’d love to help."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<section style="margin: 4rem 0;">
	<h2 class="text-3xl font-semibold mb-2">Meet the founder</h2>
	<p class="mb-6">Uncommon is built and led by Thilo Konzok — founder, designer and product thinker.</p>
	<img src="/generated/image-a-portrait-headshot-of-a-confident-europ.webp" alt="Photo of Thilo Konzok" style="max-width:280px; border-radius:16px; margin-bottom:16px;" />
	<p class="mb-4">Before creating Uncommon, Thilo was the co-founder and CEO of Yohana Europe (acquired), and previously led product teams in B2B software. With a background rooted in design and strategy, he’s spent years helping early-stage founders go from idea to traction.</p>
	<p class="mb-4">He started Uncommon to give startup teams the momentum and polish usually reserved for companies with big budgets and bigger headcounts. The tool cuts out the design and messaging guesswork so founders can show up looking ready — to customers, candidates, and investors — from day one.</p>
	<p class="mb-4">Today, Thilo is the sole builder behind Uncommon. Every decision, product improvement and conversation with early users goes directly through him. If you're using Uncommon, you're working with the founder.</p>
	<p class="mb-2">Used by funded teams like Squint and nsave to build standout brands — and raise from Sequoia.</p>
</section>

<!-- Investors section intentionally removed as there are no formal institutional investors for Uncommon. -->

<!-- CTA Section -->
<CallToAction
  title="Start looking like a company that wins"
  subtitle="Your first website, deck, ads, and more — done in days"
  description="Uncommon is the only AI designer built to help founders sell, hire, and raise — fast. Used by Squint and nsave, both backed by Sequoia. Try it free."
  callsToAction={[{ href: '/signup', label: 'Start building free', variant: 'primary' }, { href: '/contact', label: 'Book a demo', variant: 'secondary' }]}
  imageSrc="/generated/image-customer-founder-smiling-indoors-3-4.webp"
/>
