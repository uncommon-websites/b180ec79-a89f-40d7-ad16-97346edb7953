<script lang="ts">
	export let title: string;
	export let description: string;
	export let buttons: { text: string; icon?: boolean; primary?: boolean }[] = [];
	export let alignRight = false;
</script>

<section class="py-16 border-b border-border">
	<div class="container-custom">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
			
			<!-- Text Content -->
			<div class="{alignRight ? 'lg:order-2 lg:pl-12' : 'lg:pr-12'}">
				<h2 class="text-2xl font-medium mb-4">{title}</h2>
				<p class="text-muted font-light mb-8 max-w-md">{description}</p>
				
				<div class="flex flex-wrap gap-3">
					{#each buttons as btn}
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							{btn.text}
							{#if btn.icon}
								<span class="text-muted border border-muted/30 rounded px-1 text-[9px] min-w-[16px] text-center">M</span>
							{/if}
						</button>
					{/each}
				</div>
			</div>

			<!-- Visual Content -->
			<div class="{alignRight ? 'lg:order-1' : ''} bg-primary-50/50 border border-border rounded-sm min-h-[300px] p-6 flex items-center justify-center overflow-hidden relative">
				<slot />
			</div>

		</div>
	</div>
</section>
