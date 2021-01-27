<script>
  import Profile from '../web/Profile.svelte';
  import Stories from '../web/Stories.svelte';
  import Footer from './Footer.svelte';
</script>

<style lang="scss">
  .sidebar {
    position: relative;
    padding: 4.5em 0 0 0;

    .container {
      position: fixed;
    }
  }
</style>

<div class="sidebar">
  <div class="container">
    <Profile />
    <Stories />
    <Footer />
  </div>
</div>
