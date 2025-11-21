<svelte:head>
	<title>Standards — CREATE SOMETHING.ltd</title>
	<meta
		name="description"
		content="Explicit internal rules emerging from our interpretation of the masters' principles in the context of modern software development."
	/>
</svelte:head>

<!-- Header -->
<section class="pt-24 pb-16 px-6 border-b border-white/10">
	<div class="max-w-4xl mx-auto text-center">
		<p class="text-sm tracking-widest uppercase opacity-60 mb-4">Internal Rules</p>
		<h1 class="mb-6">Standards</h1>
		<p class="text-xl opacity-70 leading-relaxed">
			Explicit constraints emerging from our situated interpretation of "less, but better" in
			modern software development.
		</p>
	</div>
</section>

<!-- Philosophy -->
<section class="py-16 px-6">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">Interpretation, Not Adoption</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				These standards represent <strong>our internal opinions</strong>, grounded in the lineage
				of Rams, Mies, the Eameses, and others.
			</p>

			<p>
				We cannot simply "adopt" their principles—we can only interpret them through our horizon
				of understanding: API design, serverless computing, OAuth flows, reactive frameworks,
				database schemas.
			</p>

			<p>
				Each standard follows the format: <em>Given</em> a master's principle, <em>and given</em> our
				specific context, <em>we constrain ourselves to</em> an explicit rule.
			</p>

			<p class="text-base opacity-60 italic pt-6">
				This is being internally opinionated <strong>through</strong> the lineage, not instead of it.
			</p>
		</div>
	</div>
</section>

<!-- Design System Standards -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">Design System Standards</h2>

		<div class="space-y-8">
			<!-- Typography -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Fluid Typography</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "Good design is unobtrusive"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Web typography across viewport sizes</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Use clamp() for fluid scaling</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Typography scales smoothly without jarring breakpoint jumps. h1: 56px→112px, h2:
							32px→56px. Enable optical sizing for variable fonts.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code>h1 &#123; font-size: clamp(3.5rem, 9vw, 7rem); &#125;</code>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Type should adapt to context without demanding attention. Fluid scaling
						serves readability across devices without arbitrary breakpoints.
					</p>
				</div>
			</div>

			<!-- Color Palette -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Pure Black & White</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Mies: "Less is more"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Digital interface color systems</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Only #000000 and #FFFFFF</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							No grays, no brand colors, no accent palettes. Hierarchy through opacity (white/10,
							white/40, white/60), not through hue.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>background: #000000;<br />color: #FFFFFF;<br />border: rgba(255, 255, 255, 0.1);</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Every color introduces a decision point. Pure black and white eliminate
						arbitrary choices. Content and structure create hierarchy, not decoration.
					</p>
				</div>
			</div>

			<!-- Spacing -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Golden Ratio Spacing</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Divine proportion in classical architecture</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Web layout spacing systems</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Scale by φ (1.618)</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Spacing scale: 0.5rem, 1rem, 1.618rem, 2.618rem, 4.236rem, 6.854rem. Each step
							multiplies by the golden ratio.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>--space-sm: 1rem;<br />--space-md: 1.618rem;<br />--space-lg: 2.618rem;<br />--space-xl:
								4.236rem;</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Harmonious proportions emerge from mathematical constraints, not arbitrary
						8px grids. The golden ratio appears in nature and classical architecture for good
						reason.
					</p>
				</div>
			</div>

			<!-- Typography Stack -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Typography Stack</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Consistent typographic voice</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Variable fonts, system fallbacks</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Stack Sans Notch + JetBrains Mono</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Primary: Stack Sans Notch (variable 200-700) with optical-sizing: auto. Monospace:
							JetBrains Mono for code. System fallback: -apple-system, BlinkMacSystemFont, 'Segoe
							UI', system-ui.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>font-family: 'Stack Sans Notch', -apple-system,<br />&nbsp;&nbsp;BlinkMacSystemFont,
								'Segoe UI', system-ui;</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Stack Sans Notch provides optical precision for "less, but better"
						aesthetic. Variable fonts allow fine-tuned weight control. System fallbacks ensure
						universal accessibility.
					</p>
				</div>
			</div>

			<!-- Border Radius -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Border Radius Scale</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "Good design is unobtrusive"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Interface element corners</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Subtle corners: 8px, 12px, 16px, 24px</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Small: 8px (buttons, inputs). Medium: 12px (cards). Large: 16px (featured cards).
							XLarge: 24px (modals). Full: 9999px (pills, badges). Use sparingly—not every element
							needs rounded corners.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>--radius-sm: 8px;<br />--radius-md: 12px;<br />--radius-lg: 16px;<br />--radius-xl:
								24px;</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Corners should feel inevitable, not decorative. Larger radius for larger
						elements maintains optical consistency. Full radius reserved for intentional
						pill/badge patterns.
					</p>
				</div>
			</div>

			<!-- Animations -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Animation Standards</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "As little design as possible"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>UI feedback and transitions</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Animation serves understanding</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Easing: cubic-bezier(0.4, 0.0, 0.2, 1). Duration: 150ms (micro), 200ms (standard),
							300ms (deliberate), 500ms max. Hover: opacity 0.7 or translateY(-2px). Respect
							prefers-reduced-motion.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>transition: opacity 150ms cubic-bezier(0.4, 0.0, 0.2, 1);<br />transform:
								translateY(-2px);</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Animation only when it aids understanding. Speed maintains focus, never
						distracts. Every animation must justify its existence—decoration is not
						justification.
					</p>
				</div>
			</div>

			<!-- Accessibility -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Accessibility Requirements</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Universal access is fundamental</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>WCAG 2.1 AA compliance</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>44px touch targets, semantic HTML</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Touch targets: 44px × 44px minimum. Color contrast: Pure black/white provides 21:1
							ratio. Focus states: 2px outline with 2px offset. Semantic HTML: &lt;nav&gt;,
							&lt;main&gt;, &lt;article&gt;. All images require alt text.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>&lt;button class="w-11 h-11"&gt; &lt;!-- 44px --&gt;<br />:focus-visible &#123;
								outline: 2px solid white/60; &#125;</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Universal access is not optional—it's fundamental. Pure black and white
						provides maximum contrast. Opacity-based hierarchy maintains accessibility while
						creating visual hierarchy.
					</p>
				</div>
			</div>

			<!-- Z-Index -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Z-Index Scale</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "Good design is systematic"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Layering interface elements</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Predictable layering: 0, 10, 20, 30, 40, 50</strong>
							</p>
						</div>
					</div>

					<div class="pt-2">
						<p class="opacity-60 leading-relaxed mb-4">
							Base: 0 (document flow). Dropdown: 10. Sticky: 20. Fixed nav: 30 (z-50 in
							Tailwind). Modal: 40. Toast: 50. Never use arbitrary z-index values—chaos indicates
							poor information architecture.
						</p>
						<div class="bg-white/5 p-4 font-mono text-xs overflow-x-auto">
							<code
								>--z-base: 0;<br />--z-dropdown: 10;<br />--z-fixed: 30; /* Fixed navigation
								*/</code
							>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Z-index chaos indicates poor information architecture. Systematic layering
						makes stacking contexts predictable. Fixed navigation at z-50 ensures it stays above
						content.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Technology Stack Standards -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">Technology Stack Standards</h2>

		<div class="space-y-8">
			<!-- Serverless -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Serverless First</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Mies: "Minimal material, maximum strength"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Infrastructure that scales without waste</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Cloudflare Workers over servers</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						No idle resources. No provisioning. Code runs at the edge, close to users. Pay for
						execution, not capacity. Workers over Lambda. KV over traditional databases for
						ephemeral data.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Traditional servers waste resources during idle time. Serverless embodies
						"less, but better"—minimal infrastructure, maximum efficiency.
					</p>
				</div>
			</div>

			<!-- Framework -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Svelte Over React</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "As little design as possible"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Modern reactive frameworks</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>SvelteKit (compiles away)</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Svelte compiles to vanilla JavaScript. No runtime framework shipped to users. Svelte 5
						runes ($state, $derived) over Svelte 4 magic. Explicit reactivity over implicit
						tracking.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: React ships a runtime. Svelte disappears. Users get functionality without
						framework weight. Runes make reactivity explicit and understandable.
					</p>
				</div>
			</div>

			<!-- Database -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Notion as Canonical Target</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Notion: "Database for humans"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Arc pattern sync integrations</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Work with Notion's structure</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						For Arc implementations: Notion as destination database. Use Notion API 2025-09-03.
						Embrace Notion's block structure. Don't fight relational database paradigms—work with
						Notion's multi-source approach.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Notion democratizes data management. Syncing TO Notion empowers users to
						manage their data in a tool they understand, not force them into SQL schemas.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Code Quality Standards -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">Code Quality Standards</h2>

		<div class="space-y-8">
			<!-- Abstraction -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">No Premature Abstraction</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "Avoid being arbitrary"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Software architecture, DRY principle</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Abstraction only at third use</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Three similar lines > premature abstraction. Don't create helpers, utilities, or
						wrappers for one-time operations. Don't design for hypothetical future requirements.
						Wait for the pattern to prove itself.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Abstractions introduce indirection and complexity. They're only justified
						when the cost of duplication exceeds the cost of abstraction. Three uses is the
						threshold.
					</p>
				</div>
			</div>

			<!-- Naming -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Clarity Over Brevity</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Rams: "Good design is understandable"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Code readability, maintenance</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Descriptive names always</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						<code class="font-mono text-xs">getCurrentWorkingDirectory()</code> over
						<code class="font-mono text-xs">getCwd()</code>. Full words over abbreviations. Function
						names describe what they do, not clever puns. Variables describe what they contain.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Code is read 10x more than written. Editors have autocomplete. Brevity
						serves the writer; clarity serves the reader. Optimize for reading.
					</p>
				</div>
			</div>

			<!-- Dependencies -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Challenge Every Dependency</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Dieter Rams: "Less, but better"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>npm ecosystem bloat</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Justify every npm install</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Every dependency must justify its existence. Web APIs over npm packages when possible.
						Native fetch over axios. Native date handling over moment.js. Challenge the
						installation, not the absence.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Each dependency is a liability—maintenance burden, security surface, bundle
						size. The best dependency is the one you don't need.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- API Design Standards -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">API Design Standards (Arc Pattern)</h2>

		<div class="space-y-8">
			<!-- OAuth -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">OAuth Over API Keys</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>User autonomy, data ownership</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Multi-tenant sync architectures</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>OAuth 2.0 for authorization</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						No shared API keys. No manual configuration. Users authorize their own connections.
						Each user's OAuth token isolated. Respect token scopes—request minimum necessary
						permissions.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: API keys create shared secrets and trust boundaries. OAuth puts users in
						control of their data. Multi-tenant by design.
					</p>
				</div>
			</div>

			<!-- Single Direction -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Single Direction Sync</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Clear flow, clear purpose</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Sync complexity explosion</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>A→B only, never bidirectional</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Gmail→Notion, not Gmail↔Notion. If you need B→A, that's a different Arc. Conflict
						resolution is complexity. Single direction eliminates entire classes of problems.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Bidirectional sync doubles complexity. Conflicts, race conditions, infinite
						loops. Single direction keeps the arc clean and predictable.
					</p>
				</div>
			</div>

			<!-- Minimal Transformation -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Minimal Transformation</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Preserve source structure</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Data integrity, debugging</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Translate, don't interpret</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Preserve meaning with minimal manipulation. HTML→Notion blocks, not "smart" content
						extraction. Keep email structure intact. Don't guess at user intent. Transform only
						what's necessary for the destination format.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: Each transformation introduces assumptions and potential data loss. Minimal
						transformation = minimal surprise. Users should recognize their data.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Pattern Validation -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">Pattern Validation Standards</h2>

		<div class="space-y-8">
			<!-- Canonical Criteria -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Four Criteria for Canonical Status</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>Hermeneutic circle of understanding</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Distinguishing patterns from techniques</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Must pass all four gates</strong>
							</p>
						</div>
					</div>

					<div class="pt-2 space-y-3">
						<div class="flex items-start gap-3">
							<span class="opacity-40 mt-1">1.</span>
							<p class="opacity-60">
								<strong>Cite lineage:</strong> Connect to established principles from the masters
							</p>
						</div>
						<div class="flex items-start gap-3">
							<span class="opacity-40 mt-1">2.</span>
							<p class="opacity-60">
								<strong>Prove through .space:</strong> Validate via experiments and practice
							</p>
						</div>
						<div class="flex items-start gap-3">
							<span class="opacity-40 mt-1">3.</span>
							<p class="opacity-60">
								<strong>Deliver via .agency:</strong> Survive contact with production and clients
							</p>
						</div>
						<div class="flex items-start gap-3">
							<span class="opacity-40 mt-1">4.</span>
							<p class="opacity-60">
								<strong>Embody "less, but better":</strong> Demonstrate constraint as excellence
							</p>
						</div>
					</div>

					<p class="text-xs opacity-50 italic pt-4">
						Rationale: Not every technique becomes a pattern. Canonical status is earned through
						validation across all three domains of the ecosystem.
					</p>
				</div>
			</div>

			<!-- Evolution Pace -->
			<div class="border border-white/10 p-6 md:p-8">
				<h3 class="text-xl font-semibold mb-6">Slow Evolution</h3>

				<div class="space-y-4 text-sm md:text-base opacity-80">
					<div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-4 border-b border-white/10">
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Given</p>
							<p>"Slow is smooth, smooth is fast"</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Context</p>
							<p>Avoiding trend-chasing</p>
						</div>
						<div>
							<p class="text-xs uppercase tracking-wider opacity-40 mb-2">Rule</p>
							<p class="opacity-100">
								<strong>Discovery, not design</strong>
							</p>
						</div>
					</div>

					<p class="opacity-60 leading-relaxed pt-2">
						Patterns emerge slowly through validation, not through brainstorming sessions. Canon
						grows through discipline, not ambition. Don't force patterns into existence. Wait for
						them to prove themselves across multiple implementations.
					</p>

					<p class="text-xs opacity-50 italic pt-2">
						Rationale: The canon must be stable. Rapid change dilutes meaning. Patterns that
						emerge slowly through practice have deeper roots than patterns invented in meetings.
					</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- How Standards Evolve -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">How Standards Evolve</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				These standards aren't fixed—they evolve through the <strong>hermeneutic circle</strong>:
			</p>

			<div class="my-8 p-8 border border-white/10">
				<pre class="text-sm opacity-60 font-mono leading-relaxed overflow-x-auto">
<span class="opacity-100">.ltd</span> (Standards provide horizon of understanding)
    ↓
<span class="opacity-100">.space</span> (Practice tests interpretation)
    ↓
<span class="opacity-100">.agency</span> (Production validates or challenges)
    ↓
<span class="opacity-100">Feedback</span> (Understanding deepens)
    ↓
<span class="opacity-100">.ltd</span> (Standards refine or new ones emerge)
				</pre>
			</div>

			<p>
				When a standard doesn't hold in production, it doesn't belong here. When practice reveals a
				new constraint worth codifying, it earns a place.
			</p>

			<p>
				<strong>The Arc pattern is proof:</strong> it didn't exist when we started. It emerged through
				applying "less, but better" to sync integrations, survived client delivery, and now informs
				how we understand the masters.
			</p>

			<p class="pt-6 text-base opacity-60 italic">
				Standards are living interpretations, not dead rules. They should be challenged, tested,
				and refined—but slowly, carefully, and always with reference to the lineage.
			</p>
		</div>
	</div>
</section>

<!-- Footer Navigation -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<div class="flex flex-col sm:flex-row justify-between gap-6 text-sm">
			<a href="/patterns" class="font-medium opacity-60 hover:opacity-100">
				← View Canonical Patterns
			</a>
			<a href="/ethos" class="font-medium opacity-60 hover:opacity-100">
				Read Our Ethos →
			</a>
		</div>
	</div>
</section>
