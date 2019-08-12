<script>
  export let segment;
</script>

<img src="favicon.png" alt="Ben" class='bubble-default {segment === undefined ? "" : "bubble-translate"}'/>

<style>
  .bubble-default {
    position: absolute;
    top: 8rem;
    left: 3rem;
    width: 12rem;
    height: 12rem;
    border-radius: 50%;
    border: 2px solid lightgrey;
    z-index: 999;
    transform-origin: "50% 50%";
    transition: 0.2s ease-in-out;
    transform: will-change;
  }

  .bubble-translate {
    transform: translate(-2rem, -6rem) scale(0.5);
    border-radius: 20%;
  }
</style>