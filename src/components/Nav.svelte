<script>
  import { fade } from "svelte/transition";
  import Button from "./Button.svelte";
  export let segment;
</script>

<style>
	nav {
	  border-bottom: 1px solid rgba(255, 62, 0, 0.1);
	  font-weight: 300;
	  padding: 0 1em;
	}

	ul {
	  margin: 0;
	  padding: 0;
	}

	/* clearfix */
	ul::after {
	  content: "";
	  display: block;
	  clear: both;
	}

	li {
	  display: block;
	  float: left;
	}

	.selected {
	  position: relative;
	  display: inline-block;
	}

	.selected::after {
	  position: absolute;
	  content: "";
	  width: calc(100% - 1em);
	  height: 2px;
	  background-color: rgb(255, 62, 0);
	  display: block;
	  bottom: -1px;
	}

	a {
	  text-decoration: none;
	  padding: 1em 0.5em;
	  display: block;
	}
</style>

<nav class="m-auto w-auto p-4">
	<ul class="flex">
		<li><a id="home" class='{segment === undefined ? "selected" : ""} p-2' href='.'>
			<Button>Home</Button></a></li>
		<li><a rel=prefetch id="projects" class='{segment === "projects" ? "selected" : ""} p-2' href='projects'>
			<Button>Projects</Button></a></li>
		<li><a rel=prefetch id="about" class='{segment === "about" ? "selected" : ""} p-2' href='about'>
			<Button>About</Button></a></li>
	</ul>

</nav>