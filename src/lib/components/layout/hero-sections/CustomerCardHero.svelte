<!--

@component CustomerCardHero

This hero displays a row of customers. If used, we don't need a testimonial section on the same page.

It should ALWAYS have between 3 and 5 customers!
-->

<script lang="ts">
	// Components
	import AnimateText from "$lib/components/animation/AnimateText.svelte";
	import Button from "$lib/components/ui/Button.svelte";

	// Constants
	import { cta } from "$lib/navigation";
	import { onMount } from "svelte";
	import StakeholderCard from "../sub/StakeholderCard.svelte";
	import { animate, stagger } from "motion";

	let cards: HTMLElement[] = $state([]);

	// Types
	type Props = {
		centered?: boolean;
		title: string;
		subtitle: string;
		customers: Array<{
			name: string;
			position?: string;
			imageSrc: string;
		}>;
		callsToAction?: Array<{
			href: string;
			label: string;
		}>; // A maximum of two calls to action, with the first one being primary and the second one being secondary
	};

	let {
		title,
		subtitle,
		customers = [],
		callsToAction = [cta],
		centered = false,
		...rest
	}: Props = $props();

	onMount(() => {
		animate(
			cards,
			{
				// y: ["50%", 0],
				scale: [0.9, 1],
				filter: ["blur(4px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.5,
				ease: "easeOut",
				delay: stagger(0.1, {
					startDelay: 0.5,
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<div class="bg-background" {...rest}>
	<header
		class={[
			"section-px container mx-auto grid items-end gap-16 gap-y-9 text-balance",
			centered ? "place-items-center py-16 text-center" : "mb-12 pt-24 xl:grid-cols-[1fr_auto]"
		]}
		data-enter-container
	>
		<div class="grid max-w-prose gap-6">
			<h1 class="text-display w-full text-balance" data-enter>
				<span class="block"><AnimateText text={title} /></span>
			</h1>

			<p
				data-enter
				class={[
					"text-muted-foreground text-headline block  max-w-[45ch] text-pretty transition duration-500 ease-out",
					centered && "mx-auto"
					// isTitleComplete ? "opacity-100" : "translate-y-2 opacity-0 blur-sm"
				]}
			>
				{subtitle}
			</p>
		</div>

		<!-- CTA buttons removed per request for more whitespace -->
	</header>

	<div
		class="mt-4 grid flex-nowrap gap-(--card-gap) overflow-x-auto px-(--card-gap) whitespace-nowrap [--card-gap:calc(var(--radius)/2)] [--gap:--spacing(5)] max-lg:auto-cols-max max-lg:grid-flow-col md:whitespace-normal lg:grid-cols-[var(--cols)] lg:flex-wrap"
		style:--cols="repeat({customers.length},1fr)"
	>
		{#each customers as customer, index}
			<div class="h-full overflow-clip">
				<StakeholderCard bind:cards {...customer} {index} />
			</div>
		{/each}
	</div>
</div>

<!-- Prompt Input Bar: ChatGPT-style below customer cards -->
<div class="flex items-center gap-2 px-4 py-4 max-w-xl mx-auto w-full mt-6 bg-white dark:bg-gray-900 border border-gray-200/50 dark:border-gray-800/50 rounded-full shadow-sm">
  <input
    type="text"
    placeholder="what does your company do"
    class="flex-grow border-none bg-transparent outline-none px-3 py-2 text-base text-foreground placeholder:text-gray-400 rounded-full"
    aria-label="Describe your startup prompt"
    style="order:0;"
  />
  <Button variant="secondary" size="md" iconOnly={true} class="rounded-full !bg-gray-100 !border-none !text-gray-800 hover:!bg-gray-200 p-2 w-14 h-14 flex items-center justify-center">
    <svg width="28" height="28" fill="none" stroke="currentColor" stroke-width="2.25" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
      <path d="M6 12h12M15 9l3 3-3 3" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
  </Button>
</div>
