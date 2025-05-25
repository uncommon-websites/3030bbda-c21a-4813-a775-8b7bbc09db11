<script lang="ts">
	// Components
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
    },
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
