<script lang="ts">
	import FeatureBlock from './FeatureBlock.svelte';
</script>

<div>
<!-- Block 1: Production-Ready Models -->
<FeatureBlock 
	title="Production-ready models for any use case" 
	description="From efficient 7B models to powerful Large variants, deploy the right model for your needs."
	buttons={[
		{ text: "EXPLORE MODELS", icon: true },
		{ text: "VIEW DOCS" }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 font-mono text-xs">
		<div class="space-y-4">
			<div class="flex items-center justify-between p-3 border border-primary-200 bg-primary-50/30 rounded">
				<div class="flex items-center gap-3">
					<div class="w-2 h-2 bg-primary-600 rounded-full"></div>
					<span class="font-semibold">Mistral 7B</span>
				</div>
				<span class="text-[10px] text-muted">7.3B params</span>
			</div>
			<div class="flex items-center justify-between p-3 border border-primary-300 bg-primary-50/50 rounded">
				<div class="flex items-center gap-3">
					<div class="w-2 h-2 bg-primary-700 rounded-full"></div>
					<span class="font-semibold">Mixtral 8x7B</span>
				</div>
				<span class="text-[10px] text-muted">46.7B params</span>
			</div>
			<div class="flex items-center justify-between p-3 border border-primary-400 bg-primary-50/70 rounded">
				<div class="flex items-center gap-3">
					<div class="w-2 h-2 bg-primary-800 rounded-full"></div>
					<span class="font-semibold">Mistral Large 2</span>
				</div>
				<span class="text-[10px] text-muted">123B params</span>
			</div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 2: Mixture of Experts Architecture -->
<FeatureBlock 
	title="Mixture of Experts: Efficiency meets performance" 
	description="Sparse MoE architecture activates only relevant experts per token, reducing compute costs while maintaining accuracy"
	buttons={[
		{ text: "LEARN MORE", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full max-w-md bg-white border border-border rounded shadow-sm p-6 flex flex-col gap-4">
		<div class="text-[10px] font-mono text-muted mb-2">Token routing visualization</div>
		<div class="grid grid-cols-4 gap-2">
			{#each Array(8) as _, i}
				<div class="aspect-square rounded border-2 {i < 2 ? 'border-primary-600 bg-primary-100' : 'border-gray-200 bg-gray-50'} flex items-center justify-center text-[10px] font-mono">
					E{i + 1}
				</div>
			{/each}
		</div>
		<div class="flex items-center gap-2 text-[10px] text-muted font-mono mt-2">
			<div class="w-3 h-3 bg-primary-600 rounded"></div>
			<span>Active experts: 2/8</span>
		</div>
		<div class="mt-2 pt-3 border-t border-border text-[10px] text-muted">
			Only 12.9B parameters active per token, achieving 46.7B model performance
		</div>
	</div>
</FeatureBlock>

<!-- Block 3: La Plateforme API -->
<FeatureBlock 
	title="La Plateforme: Direct API access" 
	description="Access all Mistral models through our unified API platform with transparent pricing and no cloud intermediaries"
	buttons={[
		{ text: "GET API KEY", icon: true }
	]}
>
	<div class="w-full h-full bg-gray-950 border border-border rounded shadow-sm overflow-hidden font-mono text-[10px] text-green-400 p-4">
		<div class="mb-3 text-gray-500">$ curl https://api.mistral.ai/v1/chat/completions \</div>
		<div class="pl-4 space-y-1">
			<div class="text-gray-500">-H "Authorization: Bearer $MISTRAL_API_KEY" \</div>
			<div class="text-gray-500">-H "Content-Type: application/json" \</div>
			<div class="text-gray-500">-d '&#123;</div>
			<div class="pl-4 text-blue-400">"model": "mistral-large-latest",</div>
			<div class="pl-4 text-blue-400">"messages": [&#123;"role": "user", "content": "Hello"&#125;]</div>
			<div class="text-gray-500">&#125;'</div>
		</div>
		<div class="mt-4 pt-3 border-t border-gray-800">
			<div class="text-gray-500">&#123;"id": "chat-abc123", "object": "chat.completion"&#125;</div>
		</div>
		<div class="absolute bottom-2 right-2">
			<span class="w-2 h-2 bg-green-500 rounded-full inline-block animate-pulse"></span>
		</div>
	</div>
</FeatureBlock>

<!-- Block 4: Enterprise Deployment -->
<FeatureBlock 
	title="Enterprise deployment options" 
	description="Deploy on Azure, on-premise, or through European cloud providers with full data sovereignty and GDPR compliance"
	buttons={[
		{ text: "CONTACT SALES", icon: true }
	]}
	alignRight={true}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 flex flex-col gap-4">
		<div class="flex items-center gap-3 p-3 border border-border rounded hover:border-primary-300 transition-colors cursor-pointer">
			<div class="w-8 h-8 bg-blue-100 rounded flex items-center justify-center">
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<rect x="3" y="3" width="7" height="7"/>
					<rect x="14" y="3" width="7" height="7"/>
					<rect x="14" y="14" width="7" height="7"/>
					<rect x="3" y="14" width="7" height="7"/>
				</svg>
			</div>
			<div class="flex-1">
				<div class="font-semibold text-xs">Microsoft Azure</div>
				<div class="text-[10px] text-muted">Global cloud deployment</div>
			</div>
		</div>
		<div class="flex items-center gap-3 p-3 border border-border rounded hover:border-primary-300 transition-colors cursor-pointer">
			<div class="w-8 h-8 bg-purple-100 rounded flex items-center justify-center">
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<path d="M12 2L2 7L12 12L22 7L12 2Z"/>
					<path d="M2 17L12 22L22 17"/>
					<path d="M2 12L12 17L22 12"/>
				</svg>
			</div>
			<div class="flex-1">
				<div class="font-semibold text-xs">On-Premise</div>
				<div class="text-[10px] text-muted">Full control & security</div>
			</div>
		</div>
		<div class="flex items-center gap-3 p-3 border border-border rounded hover:border-primary-300 transition-colors cursor-pointer">
			<div class="w-8 h-8 bg-indigo-100 rounded flex items-center justify-center">
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<circle cx="12" cy="12" r="3"/>
					<path d="M12 1v6m0 6v6M1 12h6m6 0h6"/>
				</svg>
			</div>
			<div class="flex-1">
				<div class="font-semibold text-xs">OVHcloud</div>
				<div class="text-[10px] text-muted">European data residency</div>
			</div>
		</div>
	</div>
</FeatureBlock>

<!-- Block 5: Open Source Commitment -->
<FeatureBlock 
	title="Open source at our core" 
	description="Apache 2.0 licensed models alongside commercial offerings. Build with transparency and community support."
	buttons={[
		{ text: "VIEW ON GITHUB", icon: true }
	]}
>
	<div class="w-full h-full bg-white border border-border rounded shadow-sm p-6 flex flex-col gap-4">
		<div class="flex items-center justify-between pb-3 border-b border-border">
			<div class="text-[10px] font-mono text-muted">mistralai/mistral-src</div>
			<div class="flex items-center gap-2">
				<svg width="12" height="12" viewBox="0 0 16 16" fill="currentColor" class="text-muted">
					<path d="M8 .25a.75.75 0 01.673.418l1.882 3.815 4.21.612a.75.75 0 01.416 1.279l-3.046 2.97.719 4.192a.75.75 0 01-1.088.791L8 12.347l-3.766 1.98a.75.75 0 01-1.088-.79l.72-4.194L.818 6.374a.75.75 0 01.416-1.28l4.21-.611L7.327.668A.75.75 0 018 .25z"/>
				</svg>
				<span class="text-[10px] font-mono">10.2k</span>
			</div>
		</div>
		
		<div class="space-y-2">
			<div class="flex items-center gap-2 p-2 rounded hover:bg-gray-50">
				<div class="w-6 h-6 bg-primary-100 rounded flex items-center justify-center text-[10px] font-mono">📄</div>
				<div class="flex-1 text-[10px]">
					<div class="font-mono">mistral-7b-v0.1</div>
					<div class="text-muted">Apache 2.0 License</div>
				</div>
			</div>
			<div class="flex items-center gap-2 p-2 rounded hover:bg-gray-50">
				<div class="w-6 h-6 bg-primary-100 rounded flex items-center justify-center text-[10px] font-mono">📄</div>
				<div class="flex-1 text-[10px]">
					<div class="font-mono">mixtral-8x7b-v0.1</div>
					<div class="text-muted">Apache 2.0 License</div>
				</div>
			</div>
			<div class="flex items-center gap-2 p-2 rounded hover:bg-gray-50">
				<div class="w-6 h-6 bg-primary-100 rounded flex items-center justify-center text-[10px] font-mono">📄</div>
				<div class="flex-1 text-[10px]">
					<div class="font-mono">mistral-inference</div>
					<div class="text-muted">Apache 2.0 License</div>
				</div>
			</div>
		</div>

		<div class="mt-auto pt-3 border-t border-border text-[10px] text-muted">
			<span class="w-2 h-2 bg-green-500 rounded-full inline-block mr-2"></span>
			10M+ downloads
		</div>
	</div>
</FeatureBlock>
</div>
