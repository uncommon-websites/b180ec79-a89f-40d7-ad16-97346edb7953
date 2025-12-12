<section class="py-20 border-b border-border">
	<div class="container-custom">
		<div class="flex flex-col md:flex-row justify-between items-start mb-16 gap-8">
			<div>
				<h2 class="text-3xl font-medium mb-2">Superior efficiency at competitive performance</h2>
				<p class="text-xl text-muted font-light">Mixture of Experts architecture advantage</p>
			</div>
			<div class="max-w-xs text-[10px] text-muted leading-relaxed border-l border-border pl-4">
				<strong class="text-foreground block mb-1">About this comparison</strong>
				Performance measured on MMLU benchmark (Massive Multitask Language Understanding) evaluating models across 57 subjects. Cost represents inference cost per million tokens. Mistral's sparse MoE architecture activates only relevant experts per token, achieving comparable accuracy to dense models at significantly lower computational cost. Learn more in our <a href="#" class="underline">technical blog</a>.
			</div>
		</div>

		<div class="relative w-full h-[500px] border border-border bg-primary-50/30 p-8 font-mono text-xs">
			<!-- Chart Grid -->
			<div class="absolute inset-0 p-8 grid grid-rows-6 grid-cols-1">
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
				<div class="border-b border-dashed border-gray-200 w-full h-full"></div>
			</div>
			
			<!-- Y Axis Label -->
			<div class="absolute left-2 top-1/2 -translate-y-1/2 -rotate-90 text-muted origin-center whitespace-nowrap">
				ACCURACY (%)
			</div>

			<!-- X Axis Label -->
			<div class="absolute bottom-2 left-1/2 -translate-x-1/2 text-muted">
				COST (CPM)
			</div>

			<!-- Top Left Legend -->
			<div class="absolute top-4 left-4 flex gap-4 text-[10px] text-muted">
				<span class="bg-gray-200 px-1 rounded text-foreground">MMLU Benchmark</span>
				<span>Inference Cost</span>
			</div>

			<!-- Data Points -->
			
			<!-- Mixtral 8x7B (The Winner) -->
			<div class="absolute top-[20%] left-[25%] flex flex-col items-center group cursor-pointer z-10">
				<div class="flex items-center gap-2 mb-1">
					<span class="text-accent font-bold">MIXTRAL 8x7B</span>
				</div>
				<div class="w-3 h-3 bg-accent rounded-full shadow-[0_0_0_4px_rgba(124,58,237,0.2)]"></div>
				<div class="mt-1 text-[10px] text-accent">70.6% / $2.0</div>
			</div>

			<!-- Mistral Large -->
			<div class="absolute top-[15%] right-[20%] flex flex-col items-center group cursor-pointer z-10">
				<div class="flex items-center gap-2 mb-1">
					<span class="text-primary-600 font-bold text-[10px]">MISTRAL LARGE 2</span>
				</div>
				<div class="w-3 h-3 bg-primary-600 rounded-full shadow-[0_0_0_4px_rgba(124,58,237,0.15)]"></div>
				<div class="mt-1 text-[10px] text-primary-600">84.0% / $3.0</div>
			</div>

			<!-- GPT-4 -->
			<div class="absolute top-[18%] right-[35%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">GPT-4</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">86.4% / $30.0</div>
			</div>

			<!-- Claude 3 Opus -->
			<div class="absolute top-[22%] left-[55%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">CLAUDE 3 OPUS</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">86.8% / $15.0</div>
			</div>

			<!-- Mistral 7B -->
			<div class="absolute top-[45%] left-[15%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">MISTRAL 7B</span>
				</div>
				<div class="w-2 h-2 bg-primary-400 rounded-full"></div>
				<div class="mt-1 text-[10px] text-primary-600">62.5% / $0.25</div>
			</div>

			<!-- LLaMA 2 70B -->
			<div class="absolute top-[50%] left-[40%] flex flex-col items-center group cursor-pointer">
				<div class="flex items-center gap-2 mb-1 opacity-100">
					<span class="font-bold text-[10px]">LLAMA 2 70B</span>
				</div>
				<div class="w-2 h-2 bg-black rounded-full"></div>
				<div class="mt-1 text-[10px] text-muted">68.9% / $0.90</div>
			</div>

			<!-- Bottom Right Legend -->
			<div class="absolute bottom-4 right-4 flex items-center gap-4 text-[10px]">
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-accent rounded-full"></div>
					<span class="text-accent font-bold">MISTRAL MODELS</span>
				</div>
				<div class="flex items-center gap-1">
					<div class="w-2 h-2 bg-black rounded-full"></div>
					<span class="text-muted">COMPETITORS</span>
				</div>
			</div>
		</div>
	</div>
</section>
