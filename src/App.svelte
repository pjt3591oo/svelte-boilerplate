<script>
	import { Router, Link, Route } from "svelte-routing";
	import NavLink from "./components/NavLink.svelte";
	import Home from './routes/Home.svelte'
	import About from './routes/About.svelte'
	export let name;
	export let url = "";
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<Router url="{url}">
  <nav>
    <NavLink to="/">Home</NavLink>
    <NavLink to="about">About</NavLink>
  </nav>

	<div>
		<Route path="/" component="{Home}"/>
		<Route path="/about" component="{About}"/>
	</div>

</Router>
