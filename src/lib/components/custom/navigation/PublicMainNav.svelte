<script lang="ts">
  import { page } from "$app/stores";
  //import { siteConfig } from '$lib/config';
  import { cn } from "$lib/utils";
  import { Spline } from "lucide-svelte";
</script>

<div class="mr-4 hidden md:flex">
  <a
    href="/"
    class="mb-1 mr-6 flex items-center space-x-2 no-underline underline-offset-0"
  >
    <Spline class="h-5 w-5" />
    <span class="hidden text-[15px] font-semibold sm:inline-block lg:text-base">
      <!-- {siteConfig.site_name} --> SiteName
    </span>
  </a>
  <nav class="flex items-center space-x-6 text-sm font-medium">
    <a
      href="/rentals"
      class={cn(
        "transition-colors hover:text-foreground/80 no-underline underline-offset-0",
        $page.url.pathname === "/rentals"
          ? "text-foreground"
          : "text-foreground/60"
      )}
    >
      Rentals
    </a>
    <a
      href="/blog"
      class={cn(
        "transition-colors hover:text-foreground/80 no-underline underline-offset-0",
        $page.url.pathname.startsWith("/blog")
          ? "text-foreground"
          : "text-foreground/60"
      )}
    >
      Blog
    </a>
    <a
      href="/list_with_us"
      class={cn(
        "transition-colors hover:text-foreground/80 no-underline underline-offset-0",
        $page.url.pathname.startsWith("/list_with_us")
          ? "text-foreground"
          : "text-foreground/60"
      )}
    >
      List with Us
    </a>
  </nav>
</div>

<style>
</style>
