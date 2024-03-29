<script lang="ts">
  import Button from "$lib/components/ui/button/button.svelte";
  import * as Sheet from "$lib/components/ui/sheet";
  //import { siteConfig } from '$lib/config';
  import { PanelTopOpen, Spline } from "lucide-svelte";
  import MobileSheetLink from "./MobileSheetLink.svelte";

  let open = false;
</script>

<Sheet.Root bind:open>
  <Sheet.Trigger asChild let:builder>
    <Button
      builders={[builder]}
      variant="ghost"
      class="mr-0 px-0 text-base hover:bg-transparent focus-visible:bg-transparent focus-visible:ring-0 focus-visible:ring-offset-0 md:hidden"
    >
      <PanelTopOpen class="h-5 w-5 rotate-90" />
      <span class="sr-only">Toggle Menu</span>
    </Button>
    <Sheet.Content side="right" class="pl-6">
      <MobileSheetLink href="/" class="flex items-center" bind:open>
        <Spline class="ml-2 h-4 w-4" />
        <span class="ml-2 font-semibold text-primary">SiteName</span>
      </MobileSheetLink>

      <div class="my-4 h-[calc(100vh-8rem)] overflow-auto pb-10 pl-8">
        <div class="flex flex-col space-y-3">
          <MobileSheetLink
            href="/rentals"
            bind:open
            class="text-muted-foreground"
          >
            Rentals
          </MobileSheetLink>
          <MobileSheetLink href="/blog" bind:open class="text-muted-foreground">
            Blog
          </MobileSheetLink>
          <MobileSheetLink
            href="/list_with_us"
            bind:open
            class="text-muted-foreground"
          >
            List with Us
          </MobileSheetLink>
        </div>
      </div>
    </Sheet.Content>
  </Sheet.Trigger>
</Sheet.Root>

<a
  href="/"
  class="mx-auto flex items-center space-x-1 md:hidden no-underline underline-offset-0"
>
  <Spline class="-ml-7 h-5 w-5" />
  <span class="text-[15px] font-semibold sm:inline-block lg:text-base">
    SiteName
  </span>
</a>

<style>
</style>
