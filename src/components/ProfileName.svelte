<script>
  export let segment;
</script>

<div id="fullname" class='fullname-default {segment === undefined ? "" : "fullname-translate"}'>
  <h2>Test 2</h2>
</div>

<style>
  .fullname-default {
    position: absolute;
    top: 20rem;
    left: 3rem;
    width: 12rem;
    height: 12rem;
    text-align: center;

    font-size: 1.5rem;
    color: rgb(121, 117, 117);
    z-index: 999;
    transform-origin: "50% 50%";
    transition: 0.2s ease-in-out;
    transform: will-change;
  }

  .fullname-translate {
    transform: translate(-2rem, -8rem);
    color: white;
    font-size: 1rem;
    font-weight: bold;
  }
</style>