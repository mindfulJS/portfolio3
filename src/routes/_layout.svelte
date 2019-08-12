<script>
	import BackgroundWave from "../components/BackgroundWave.svelte";
	import Nav from "../components/Nav.svelte";
	import ProfileBubble from "../components/ProfileBubble.svelte";
	import ProfileName from "../components/ProfileName.svelte";
	export let segment;
	let width;
</script>

<div class='relative w-full opacity-0 fade-in header-img-default {segment === undefined ? "header-img-index" : segment === "projects" ? "header-img-projects" : "header-img-other"}' style="height: 20rem; animation-delay: 0.4s">
	<div id="wave" class="absolute w-full bottom-0 left-0">
		<BackgroundWave />
	</div>

	<div id="profile" class="opacity-0 fade-in" style="animation-delay: 0.6s">
		<ProfileBubble {segment} />
		<ProfileName {segment} />
	</div>

	<div id="navbar" class="absolute w-full top-0 left-0 opacity-0 fade-in" style="animation-delay: 0.8s">
		<div id="nav-buttons" class="float-right">
			<Nav {segment}/>
		</div>
	</div>
</div>

<main id="content" class="w-full h-full mt-12 opacity-0 fade-in" style="animation-delay: 1s">
	<slot></slot>
</main>


<style>
  .header-img-default {
    background-size: cover;
    transition: 0.2s ease-in-out;
  }

  .header-img-index {
    background-image: url("../../header3.jpg");
  }

  .header-img-projects {
    background-image: url("../../header2.jpg");
  }

  .header-img-other {
    background-image: url("../../header1.jpg");
  }

  .fade-in {
    animation: fadeIn 0.2s forwards;
  }

  @keyframes fadeIn {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
</style>