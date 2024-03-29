<script>
	import { HeartHandshake } from 'lucide-svelte';
</script>

<footer
	class="absolute -bottom-28 z-50 w-full bg-background/95 py-2 shadow-sm backdrop-blur supports-[backdrop-filter]:bg-background/60 md:-bottom-24 md:px-8 md:py-0"
>
	<div class="container flex flex-col items-center justify-center md:h-24 md:flex-row md:gap-4">
		<div class="flex flex-col items-end gap-0 md:flex-row md:gap-2 md:px-0">
			<a href="/rms" class='no-underline underline-offset-0 mb-1'>
				<HeartHandshake class="inline-block h-4 w-4" />
			</a>
			<p class="text-center text-sm leading-loose text-muted-foreground md:text-left">
				Built & designed by{' '}
				<a
					href="https://southtexas.software"
					target="_blank"
					rel="noreferrer"
					class="font-medium underline underline-offset-4"
				>
					southtexas.software
				</a>
				in collaboration with{' '}
				<a
					href="https://drivehomerv.com"
					target="_blank"
					rel="noreferrer"
					class="font-medium underline underline-offset-4"
				>
					Drive Home RV
				</a>
				.
			</p>
		</div>
	</div>
</footer>
