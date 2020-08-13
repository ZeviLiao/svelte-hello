
<script>
  import { Router, Link, Route } from "svelte-routing";
	import Header from './Header.svelte';
	import Index from './pages/Index.svelte';
	import About from './pages/About.svelte';

  export let url = "";
</script>

<Router url="{url}">
  <nav>
    <Link to="/">Home</Link>
    <Link to="about">About</Link>
  </nav>
  <div>
    <Route path="about" component="{About}" />
    <Route path="/"><Index/></Route>
  </div>
</Router>