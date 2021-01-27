<script>

import MainDark from "../theme/MainDark.svelte";

</script>
<style lang="scss">
  .main {
    display: grid;
    grid-template-columns: minmax(auto, 936px);
    justify-content: center;
    background-color: #fafafa;
    transition: .5s;

    .main-container {
      display: grid;
      grid-template-columns: 3fr 1fr;
      grid-gap: 2em;
      padding: 2em 0;
    }
  }
</style>

<MainDark />

<div class="main" id="main">
  <div class="main-container">
    <slot />
  </div>
</div>
