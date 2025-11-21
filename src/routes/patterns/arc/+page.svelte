<svelte:head>
	<title>Arc — Canonical Patterns — CREATE SOMETHING.ltd</title>
	<meta
		name="description"
		content="Arc: Efficient connection between points. A canonical pattern for building sync integrations."
	/>
</svelte:head>

<!-- Header -->
<section class="pt-24 pb-16 px-6 border-b border-white/10">
	<div class="max-w-4xl mx-auto">
		<p class="text-sm tracking-widest uppercase opacity-60 mb-4">
			<a href="/patterns" class="hover:opacity-100">Canonical Patterns</a> / Arc
		</p>
		<h1 class="mb-6">Arc</h1>
		<p class="text-2xl opacity-70 leading-relaxed mb-8">
			Efficient connection between points
		</p>
		<div class="text-sm opacity-50">
			<p>Geometric principle • Applied to sync integrations • Lineage: Euclid, Rams, Mies</p>
		</div>
	</div>
</section>

<!-- The Principle -->
<section class="py-16 px-6">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">The Principle</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				<strong>Arc represents the minimal path between two points.</strong> Like an architectural arch,
				it carries load (data) across a span (systems) with minimal material (code).
			</p>

			<p>
				An arc is efficient not because it's the shortest distance—that would be a straight
				line—but because it's the <em>most elegant</em> connection when constraints exist. It acknowledges
				the forces at play and responds with grace, not brute force.
			</p>

			<p>
				In software, Arc is our pattern for building sync integrations. Not "sync everything
				everywhere," but <strong>efficient connection where it matters</strong>.
			</p>
		</div>
	</div>
</section>

<!-- Design Lineage -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">Design Lineage</h2>

		<div class="space-y-8">
			<!-- Euclid -->
			<div class="border-l-2 border-white/20 pl-6">
				<p class="text-xs font-mono opacity-40 mb-2">GEOMETRY</p>
				<h3 class="text-xl font-semibold mb-3">Euclid</h3>
				<p class="opacity-70 leading-relaxed">
					The arc as geometric form: the path traced by a point moving at constant distance from a
					center. Pure mathematics as foundation for understanding efficiency.
				</p>
			</div>

			<!-- Rams -->
			<div class="border-l-2 border-white/20 pl-6">
				<p class="text-xs font-mono opacity-40 mb-2">INDUSTRIAL DESIGN</p>
				<h3 class="text-xl font-semibold mb-3">Dieter Rams</h3>
				<p class="opacity-70 leading-relaxed">
					<em>"Weniger, aber besser"</em> — Less, but better. Arc embodies this by doing one thing
					(connection) exceptionally well, refusing feature creep in favor of clarity.
				</p>
			</div>

			<!-- Mies -->
			<div class="border-l-2 border-white/20 pl-6">
				<p class="text-xs font-mono opacity-40 mb-2">ARCHITECTURE</p>
				<h3 class="text-xl font-semibold mb-3">Ludwig Mies van der Rohe</h3>
				<p class="opacity-70 leading-relaxed">
					<em>"Less is more."</em> The arch in architecture demonstrates that minimal material, properly
					arranged, achieves maximum strength. Arc applies this to code.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- How Arc Works -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">How Arc Works</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p><strong>Arc is not a library or framework.</strong> It's a pattern for thinking about sync.</p>

			<div class="my-8 p-8 border border-white/10 bg-white/5">
				<p class="text-sm font-mono opacity-60 mb-4">The Arc Pattern:</p>
				<pre class="text-sm opacity-70 font-mono leading-loose overflow-x-auto">
System A  ──────arc──────>  System B

1. OAuth (authenticate both endpoints)
2. Sync (efficient transfer)
3. Transform (minimal translation)
				</pre>
			</div>

			<p><strong>Constraints that define Arc:</strong></p>

			<ul class="space-y-4 text-base opacity-70 pl-6">
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">—</span>
					<span
						><strong>Single direction:</strong> A→B, not bidirectional chaos. Clear flow, clear purpose.</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">—</span>
					<span
						><strong>Minimal transformation:</strong> Preserve source structure. Don't over-engineer the
						translation layer.</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">—</span>
					<span
						><strong>OAuth-based:</strong> No API keys, no manual config. Users authorize their own
						connections.</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">—</span>
					<span
						><strong>Serverless first:</strong> Cloudflare Workers, edge computing. Infrastructure
						matches the arc metaphor—distributed, efficient.</span
					>
				</li>
			</ul>
		</div>
	</div>
</section>

<!-- Implementations -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-5xl mx-auto">
		<h2 class="mb-12">Implementations</h2>

		<div class="space-y-8">
			<!-- Arc for Gmail -->
			<div class="border border-white/10 p-6 md:p-8">
				<div class="mb-6">
					<span class="text-xs font-mono opacity-40">ARC IMPLEMENTATION #1</span>
					<h3 class="text-2xl font-semibold mt-2">Arc for Gmail</h3>
					<p class="text-sm opacity-50 mt-1">Delivered to Half Dozen</p>
				</div>

				<p class="text-lg opacity-70 mb-6 leading-relaxed">
					Multi-user Gmail→Notion sync. OAuth-based, AI-powered summaries, automatic contact
					management.
				</p>

				<div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-sm md:text-base">
					<div>
						<p class="opacity-40 mb-2 uppercase tracking-wider text-xs">Stack</p>
						<ul class="opacity-60 space-y-1">
							<li>• Cloudflare Workers</li>
							<li>• Workers AI (email summaries)</li>
							<li>• Gmail API (OAuth 2.0)</li>
							<li>• Notion API 2025-09-03</li>
						</ul>
					</div>
					<div>
						<p class="opacity-40 mb-2 uppercase tracking-wider text-xs">Arc Principles Applied</p>
						<ul class="opacity-60 space-y-1">
							<li>• Single direction: Gmail→Notion</li>
							<li>• Minimal transformation: HTML→Notion blocks</li>
							<li>• OAuth-based: Multi-user auth</li>
							<li>• Serverless: Edge computing</li>
						</ul>
					</div>
				</div>

				<div class="mt-8 pt-6 border-t border-white/10">
					<p class="text-xs opacity-40 mb-3 uppercase tracking-wider">Key Challenge</p>
					<p class="text-sm opacity-60 leading-relaxed">
						Email HTML→Notion conversion requires character sanitization (mojibake), rich text
						array splitting, and link preservation. Arc principle: minimal transformation that
						preserves meaning.
					</p>
				</div>

				<div class="mt-6">
					<p class="text-xs opacity-40 mb-3 uppercase tracking-wider">Validated Through</p>
					<p class="text-sm opacity-60">
						Production deployment at Half Dozen. 5-minute sync cycles, multi-user OAuth, bespoke
						contact categorization (internal vs. external).
					</p>
				</div>
			</div>

			<!-- Arc for Fireflies -->
			<div class="border border-white/10 p-6 md:p-8 opacity-50">
				<div class="mb-6">
					<span class="text-xs font-mono opacity-40">ARC IMPLEMENTATION #2</span>
					<h3 class="text-2xl font-semibold mt-2">Arc for Fireflies</h3>
					<p class="text-sm opacity-50 mt-1">In Development</p>
				</div>

				<p class="text-lg opacity-70 mb-6 leading-relaxed">
					Fireflies.ai transcripts→Notion. Same Arc pattern, different endpoints.
				</p>

				<div class="text-sm opacity-60">
					<p>Pattern reusability validates Arc as canonical approach.</p>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Why Arc is Canonical -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">Why Arc is Canonical</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				Arc isn't just a naming convention—it's a <strong>validated pattern</strong> that emerged
				from the hermeneutic circle:
			</p>

			<div class="my-8 p-8 border border-white/10">
				<pre class="text-sm opacity-60 font-mono leading-relaxed overflow-x-auto">
<span class="opacity-100">.ltd</span> (Canon)
    ↓ Established "less, but better" + geometric principles
<span class="opacity-100">.space</span> (Practice)
    ↓ Built Arc for Gmail as experiment
<span class="opacity-100">.agency</span> (Services)
    ↓ Delivered to Half Dozen, validated in production
<span class="opacity-100">Feedback Loop</span>
    ↓ Arc proven reusable (Fireflies next)
    ↓ Pattern elevated to canonical status
<span class="opacity-100">.ltd</span> (Canon evolves)
				</pre>
			</div>

			<p><strong>Arc meets the canonical criteria:</strong></p>

			<ul class="space-y-4 text-base opacity-70 pl-6">
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">✓</span>
					<span
						><strong>Connects to lineage:</strong> Euclid (geometry), Rams (less, but better), Mies
						(minimal material, maximum strength)</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">✓</span>
					<span
						><strong>Proved through practice:</strong> Arc for Gmail experiment documented, tested,
						validated</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">✓</span>
					<span
						><strong>Delivered to clients:</strong> Half Dozen production deployment, bespoke
						configuration</span
					>
				</li>
				<li class="flex items-start gap-3">
					<span class="opacity-40 mt-1">✓</span>
					<span
						><strong>Embodies "less, but better":</strong> Single purpose (connection), minimal
						complexity, clear constraints</span
					>
				</li>
			</ul>

			<p class="pt-6 text-base opacity-60 italic">
				Arc wasn't designed—it was <em>discovered</em> through building, delivering, and reflecting
				on what worked.
			</p>
		</div>
	</div>
</section>

<!-- Interpretation, Not Adoption -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">Interpretation, Not Adoption</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				Arc demonstrates a crucial philosophical point: <strong
					>we cannot simply "adopt" the masters' principles</strong
				>—we can only interpret them.
			</p>

			<p>
				When we read Rams saying "less, but better," we don't understand it the same way a 1970s
				product designer would. We approach with our own <em>horizon of understanding</em>: API
				design, OAuth flows, serverless computing, database schemas.
			</p>

			<p><strong>This interpretation IS our internal opinion.</strong></p>

			<p>
				The Arc constraints—single direction, OAuth-based, minimal transformation, serverless
				first—didn't come from Rams or Mies directly. They emerged from <strong
					>our situated interpretation</strong
				> of their principles applied to sync integrations in 2025.
			</p>

			<div class="my-8 p-8 border border-white/10 bg-white/5">
				<p class="text-sm opacity-60 mb-4">
					Given Mies' principle that "less is more" (minimal material, maximum strength),
				</p>
				<p class="text-sm opacity-60 mb-4">
					And given our context of sync integrations between API-driven services,
				</p>
				<p class="text-sm opacity-100">
					<strong
						>We constrain ourselves to single-direction flows with minimal transformation
						layers.</strong
					>
				</p>
			</div>

			<p>This is being internally opinionated <em>through</em> the lineage, not instead of it.</p>

			<p>
				The hermeneutic circle reveals that understanding deepens through practice. We didn't find
				"Arc" in Rams' writings—we discovered it by applying "less, but better" to real problems.
				Arc is now part of our canon, enriching how we understand the masters.
			</p>

			<p class="pt-6 text-base opacity-60 italic">
				CREATE SOMETHING's value comes from situated interpretation: taking timeless principles
				and making them actionable in the specific context of modern software development.
			</p>
		</div>
	</div>
</section>

<!-- Future -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto">
		<h2 class="mb-8">The Arc Ecosystem</h2>

		<div class="space-y-6 text-lg opacity-80 leading-relaxed">
			<p>
				Arc is not a single product—it's a <strong>pattern applied to any sync problem</strong>:
			</p>

			<div class="my-8 space-y-3 text-base opacity-60">
				<p>→ Arc for Gmail (Gmail → Notion)</p>
				<p>→ Arc for Fireflies (Fireflies.ai → Notion)</p>
				<p>→ Arc for Slack (Slack → Notion)</p>
				<p>→ Arc for Discord (Discord → Notion)</p>
				<p class="opacity-40 italic">...any A→B where Arc principles apply</p>
			</div>

			<p>
				Each implementation validates the pattern. Each client engagement feeds back to refine the
				canon. The ecosystem grows through discipline, not ambition.
			</p>

			<p class="pt-6 text-base opacity-60 italic">
				Arc demonstrates that <strong>constraint breeds excellence</strong>. By limiting ourselves
				to one thing—efficient connection—we do it better than anyone.
			</p>
		</div>
	</div>
</section>

<!-- Back -->
<section class="py-16 px-6 border-t border-white/10">
	<div class="max-w-3xl mx-auto text-center">
		<a href="/patterns" class="text-sm font-medium opacity-60 hover:opacity-100">
			← Back to Patterns
		</a>
	</div>
</section>
