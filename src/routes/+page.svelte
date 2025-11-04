<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CenteredTextOnlyHero from "$lib/components/layout/hero-sections/CenteredTextOnlyHero.svelte";
</script>

<CenteredTextOnlyHero
	title="Commerce infrastructure for platforms and marketplaces"
	subtitle="Unify multi-merchant checkout across any ecommerce platform. Get cross-platform commerce orchestration in days, not months."
	imageSrc="/generated/image-a-modern-moody-architectural-office-inte.webp"
/>
<LogoScroller 
	label="Trusted by industry leaders" 
	logoUrls={[
		'https://cdn.brandfetch.io/throne.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/editorialist.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/thingtesting.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/aguabendita.com/w/400/h/400/logo'
	]} 
/>

<Summary
	title="The platform problem"
	text="Building multi-merchant marketplaces means integrating with dozens of ecommerce platforms—Shopify, WooCommerce, BigCommerce, and more. Each has different APIs, data formats, and authentication flows.

Violet solves this with a single unified API that connects to 16+ platforms and 5M+ merchants. What would take a large team months to build, you can ship with two developers in weeks."
/>

<Testimonials
	testimonials={[
		{
			name: "Priya Mehta",
			position: "VP of Engineering",
			company: "StyleMarket",
			quote:
				"We launched our multi-merchant marketplace in three weeks instead of six months. Violet's unified API eliminated the complexity of building individual platform integrations, letting our team of two backend developers ship what would have required a team of eight.",
			image: "/generated/image-editorial-documentary-style-photograph-o.webp"
		},
		{
			name: "Marcus Johnson",
			position: "Co-Founder & CTO",
			company: "CreatorHub",
			quote:
				"Our transaction processing costs dropped 92% within the first month. What used to take our operations team 48 hours to reconcile now happens instantly through Violet's normalized checkout flow. The ROI was immediate and measurable.",
			image: "/generated/image-editorial-documentary-style-image-of-a-c.webp"
		},
		{
			name: "Sofia Rodriguez",
			position: "Head of Product",
			company: "GiftCircle",
			quote:
				"Connecting to Shopify, WooCommerce, and BigCommerce took us four days total with Violet. Our previous attempt to build this ourselves consumed six months and never reached production. The unified data models meant zero merchant-specific edge cases.",
			image: "/generated/image-editorial-documentary-photograph-of-a-pr.webp"
		}
	]}
/>

<Features
	title="Built for speed, designed for scale"
	subtitle="Everything you need to orchestrate multi-merchant commerce without the complexity"
	features={[
		{
			title: "Ship integrations in days, not months",
			description:
				"Connect to 16+ ecommerce platforms with a single unified API. What takes a large team months to build, you can launch with two developers in weeks."
		},
		{
			title: "Access 5M+ merchants instantly",
			description:
				"One API unlocks Shopify, WooCommerce, BigCommerce, and 13+ more platforms. Scale your marketplace without building individual platform integrations."
		},
		{
			title: "Real-time data normalization",
			description:
				"Transform checkout from 36 hours to 300 milliseconds with unified data models. Every platform's data automatically normalized into a consistent schema."
		},
		{
			title: "Automated commission handling",
			description:
				"Calculate, transfer, and process refunds automatically across all merchants. Eliminate manual reconciliation and reduce transaction costs by 95%."
		},
		{
			title: "Crystal-clear merchant attribution",
			description:
				"Track which creator, channel, or campaign drove each purchase. Turn your marketplace into a transparent sales channel merchants actually want to join."
		},
		{
			title: "Platform-agnostic architecture",
			description:
				"Support custom integrations for enterprise merchants while maintaining the same unified API. Your marketplace works with any ecommerce system."
		}
	]}
/>
<AboutTeaser />
<CallToAction 
	title="Ship your marketplace this month"
	subtitle="Not next quarter"
	description="Stop wrestling with platform integrations. Join marketplace builders who deployed multi-merchant checkout in weeks with just two developers. Book a demo and see why teams choose Violet over building in-house."
	imageSrc="/generated/image-editorial-documentary-photograph-of-a-de.webp"
	callsToAction={[
		{
			href: "/",
			label: "Book a demo",
			variant: "primary"
		},
		{
			href: "/",
			label: "View documentation",
			variant: "secondary"
		}
	]}
/>
