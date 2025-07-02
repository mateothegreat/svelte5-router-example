<script lang="ts">
  import {
    route,
    Router,
    type RouteConfig,
  } from "@mateothegreat/svelte5-router";
  import Home from "./routes/home.svelte";
  import Kitchen from "./routes/kitchen.svelte";
  const routes: RouteConfig[] = [
    {
      path: "/",
      component: Home,
    },
    {
      path: "/kitchen",
      component: Kitchen,
    },
  ];
</script>

<a use:route href="/">Home</a> |
<a use:route href="/kitchen">Kitchen</a>

<Router {routes} />
