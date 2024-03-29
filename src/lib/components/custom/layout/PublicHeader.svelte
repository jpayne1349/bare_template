<script lang="ts">
	import { LogIn } from 'lucide-svelte';
import ModeToggle from '../darkmode/ModeToggle.svelte';
	import PublicMainNav from '$lib/components/custom/navigation/PublicMainNav.svelte';
	import PublicMobileNav from '$lib/components/custom/navigation/PublicMobileNav.svelte';
</script>

<header
	class="sticky top-0 z-50 w-full border-b bg-background/95
shadow-sm backdrop-blur supports-[backdrop-filter]:bg-background/60"
>
	<div class="container flex flex-row-reverse md:flex-row h-14 items-center">
		<PublicMainNav />
		<PublicMobileNav />
		<div class="flex  items-center justify-between space-x-2 sm:space-x-4 md:flex-1 md:justify-end">
			<ModeToggle />
		</div>
	</div>
</header>

<style>
</style>
