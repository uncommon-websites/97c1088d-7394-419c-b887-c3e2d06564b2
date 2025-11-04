<script lang="ts">
	// Props
	type Props = {
		title: string;
		subtitle: string;
	};
	let { title, subtitle }: Props = $props();
</script>

<section class="relative section-py overflow-hidden bg-background">
	<!-- Geometric Background Illustration -->
	<div class="absolute inset-0 overflow-hidden opacity-40">
		<!-- Grid Pattern -->
		<svg class="absolute inset-0 w-full h-full" xmlns="http://www.w3.org/2000/svg">
			<defs>
				<pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
					<path d="M 40 0 L 0 0 0 40" fill="none" stroke="currentColor" stroke-width="0.5" class="text-primary/20"/>
				</pattern>
				<linearGradient id="purpleGradient" x1="0%" y1="0%" x2="100%" y2="100%">
					<stop offset="0%" style="stop-color:var(--color-primary-600);stop-opacity:0.6" />
					<stop offset="100%" style="stop-color:var(--color-secondary-600);stop-opacity:0.6" />
				</linearGradient>
			</defs>
			<rect width="100%" height="100%" fill="url(#grid)" />
		</svg>

		<!-- Animated Connection Nodes -->
		<div class="absolute top-1/4 left-1/4 w-3 h-3 rounded-full bg-primary-600 animate-pulse"></div>
		<div class="absolute top-1/3 right-1/3 w-2 h-2 rounded-full bg-primary-500 animate-pulse" style="animation-delay: 0.5s"></div>
		<div class="absolute bottom-1/3 left-1/3 w-2.5 h-2.5 rounded-full bg-secondary-600 animate-pulse" style="animation-delay: 1s"></div>
		<div class="absolute top-2/3 right-1/4 w-2 h-2 rounded-full bg-primary-400 animate-pulse" style="animation-delay: 1.5s"></div>
		<div class="absolute bottom-1/4 right-1/3 w-3 h-3 rounded-full bg-secondary-500 animate-pulse" style="animation-delay: 2s"></div>

		<!-- Connection Lines -->
		<svg class="absolute inset-0 w-full h-full connection-lines" xmlns="http://www.w3.org/2000/svg">
			<line x1="25%" y1="25%" x2="66%" y2="33%" stroke="url(#purpleGradient)" stroke-width="1" opacity="0.3" class="animate-draw-line"/>
			<line x1="66%" y1="33%" x2="33%" y2="66%" stroke="url(#purpleGradient)" stroke-width="1" opacity="0.3" class="animate-draw-line" style="animation-delay: 0.5s"/>
			<line x1="33%" y1="66%" x2="75%" y2="66%" stroke="url(#purpleGradient)" stroke-width="1" opacity="0.3" class="animate-draw-line" style="animation-delay: 1s"/>
			<line x1="75%" y1="66%" x2="66%" y2="75%" stroke="url(#purpleGradient)" stroke-width="1" opacity="0.3" class="animate-draw-line" style="animation-delay: 1.5s"/>
		</svg>

		<!-- Floating Geometric Shapes -->
		<div class="absolute top-1/4 right-1/4 w-32 h-32 border border-primary-600/20 rounded-lg rotate-12 animate-float"></div>
		<div class="absolute bottom-1/4 left-1/4 w-24 h-24 border border-secondary-600/20 rounded-lg -rotate-12 animate-float" style="animation-delay: 1s; animation-duration: 8s"></div>
		<div class="absolute top-1/2 left-1/2 w-40 h-40 border border-primary-500/10 rounded-lg rotate-45 animate-float" style="animation-delay: 2s; animation-duration: 10s"></div>
	</div>

	<!-- Content -->
	<div class="relative container mx-auto section-px">
		<div class="max-w-4xl mx-auto text-center">
			<h1 class="text-display font-semibold text-foreground mb-6">
				{title}
			</h1>
			<p class="text-title3 text-muted-foreground max-w-3xl mx-auto">
				{subtitle}
			</p>
			<div class="flex flex-col sm:flex-row gap-4 justify-center mt-12">
				<a
					href="/"
					class="inline-flex items-center justify-center px-8 py-4 text-base font-medium text-primary-foreground bg-primary hover:bg-primary-700 transition-colors duration-200 rounded-lg"
				>
					Book a demo
				</a>
				<a
					href="/"
					class="inline-flex items-center justify-center px-8 py-4 text-base font-medium text-foreground bg-card hover:bg-card-hover border border-border transition-colors duration-200 rounded-lg"
				>
					View documentation
				</a>
			</div>
		</div>
	</div>
</section>

<style>
	@keyframes float {
		0%, 100% {
			transform: translateY(0) rotate(12deg);
		}
		50% {
			transform: translateY(-20px) rotate(12deg);
		}
	}

	@keyframes draw-line {
		0% {
			stroke-dasharray: 1000;
			stroke-dashoffset: 1000;
		}
		100% {
			stroke-dasharray: 1000;
			stroke-dashoffset: 0;
		}
	}

	.animate-float {
		animation: float 6s ease-in-out infinite;
	}

	.animate-draw-line {
		animation: draw-line 3s ease-in-out infinite;
	}
</style>