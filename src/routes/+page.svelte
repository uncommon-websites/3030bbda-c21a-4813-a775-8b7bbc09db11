<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={true}
  title="Designed to sell, hire, raise."
  subtitle="The company building tool for founders."
  customers={[
    {
      name: 'Brand',
      imageSrc: '/generated/image-a-street-scene-in-an-urban-environment-w.webp'
    },
    {
      name: 'Website',
      imageSrc: '/generated/image-a-badge-lanyard-lying-on-a-simple-surfac.webp'
    },
    {
      name: 'Logo',
      imageSrc: '/generated/image-a-flat-lay-of-a-startup-hoodie-on-a-whit.webp'
    },
    {
      name: 'Deck',
      imageSrc: '/generated/image-monitor-screen-with-modern-pitch-deck-sl.webp'
    },
    {
      name: 'Merch',
      imageSrc: '/generated/image-startup-hoodie-mockup-flat-lay-on-white-.webp'
    }
  ]}
    {
      name: 'Maya Patel',
      position: 'Founder, Early Stage AI Startup',
      imageSrc: '/generated/image-a-confident-female-founder-in-a-modern-o.webp'
    },
    {
      name: 'Alex Kim',
      position: 'Product Manager, SaaS Platform',
      imageSrc: '/generated/image-a-male-product-manager-in-a-creative-wor.webp'
    },
    {
      name: 'Sophie Lemaire',
      position: 'Engineering Lead, Fintech',
      imageSrc: '/generated/image-a-smiling-female-engineering-lead-at-her.webp'
    },
    {
      name: 'Daniel Wu',
      position: 'Designer, Marketplace Startup',
      imageSrc: '/generated/image-a-male-designer-in-a-bright-coworking-sp.webp'
    },
    {
      name: 'Priya Shah',
      position: 'Marketer, Consumer App',
      imageSrc: '/generated/image-a-female-marketer-in-an-open-workspace-p.webp'
    }
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		"https://logo.clearbit.com/figma.com",
		"https://logo.clearbit.com/pitch.com",
		"https://logo.clearbit.com/linear.app",
		"https://logo.clearbit.com/zapier.com"
	]}
/>

<Summary
	title="What we do"
	text="Uncommon is your AI designer for company building. Instantly create websites, decks, ads, and more—so you can sell, hire, and raise, all in one tool. Move from idea to traction faster."
/>

<Testimonials
	testimonials={[
		{
			name: "Kira Amano",
			position: "Founder & CEO",
			company: "Everfine",
			quote:
				"We created our whole deck in a single afternoon. It saved us over 10 hours and helped land meetings with 5 investors in one week.",
			image: "/generated/image-a-confident-female-founder-sits-in-a-vib.webp"
		},
		{
			name: "Dorian Chae",
			position: "CFO",
			company: "Deltaix",
			quote:
				"Uncommon helped reduce our design expenses by 40%. No more wasting cycles updating decks and websites — it's auto-synced and always ready.",
			image: "/generated/image-in-a-modern-meeting-room-with-large-wind.webp"
		},
		{
			name: "Ari Mooren",
			position: "Marketing Lead",
			company: "Setlight",
			quote:
				"I launched three campaign pages in under a day. Normally would have taken design and dev a week. Game-changer for go-to-market speed.",
			image: "/generated/image-a-nonbinary-marketing-lead-is-immersed-i.webp"
		}
	]}
/>
/>

<Features
  title="Everything you need to build your company"
  subtitle="Six ways Uncommon helps you win"
  features={[
    {
      title: "Websites that convert",
      description: "Launch beautiful, conversion-focused sites with founder-level speed—no agencies, no templates."
    },
    {
      title: "Pitch decks that raise",
      description: "Get compelling, investor-ready decks crafted by a tool that knows what works."
    },
    {
      title: "Job pages for top hires",
      description: "Attract the talent you want with career pages designed to sell your mission."
    },
    {
      title: "Ad creatives on demand",
      description: "Generate launching-ready ads and social visuals that look polished and feel on-brand."
    },
    {
      title: "All-in-one platform",
      description: "Uncommon unifies your website, deck, hiring, and marketing—so you ship faster and fix less."
    },
    {
      title: "Gets smarter as you grow",
      description: "The more you build, the better your next project gets—like hiring a team that learns your business."
    }
  ]}
/>

<UseCases
  title="Use Cases"
  subtitle="Real-world ways founders use Uncommon"
  useCases={[
    {
      title: "Raise your next round",
      description: "AI builds investor decks, landing pages, and messaging to help you fundraise faster.",
      image: "/generated/image-a-group-of-startup-founders-engaged-in-a.webp",
      link: {
        href: "/use-cases/fundraising",
        label: "Learn more"
      }
    },
    {
      title: "Hire standout talent",
      description: "Instantly create branded job pages and content that attract the right candidates.",
      image: "/generated/image-a-diverse-team-of-professionals-collabor.webp",
      link: {
        href: "/use-cases/hiring",
        label: "Learn more"
      }
    },
    {
      title: "Launch your next product",
      description: "Get ad-ready landing pages and marketing so your next launch makes noise, not crickets.",
      image: "/generated/image-a-small-group-of-energetic-individuals-g.webp",
      link: {
        href: "/use-cases/launching",
        label: "Learn more"
      }
    }
  ]}
/>

<AboutTeaser />
<CallToAction
  title="Startups move fast. Your design team should too."
  subtitle="Uncommon builds your website, pitch deck, and ads — all from one prompt."
  description="AI-powered design that helps you sell, hire, and raise. Used by Sequoia-backed teams like Squint and nsave."
  imageSrc="/generated/image-a-joyful-startup-founder-casually-dresse.webp"
  callsToAction={[
    { href: '/get-started', label: 'Try it free', variant: 'primary' },
    { href: '/contact', label: 'Talk to sales', variant: 'secondary' }
  ]}
/>
