<script>
  import Profile from '../web/Profile.svelte';
  import Stories from '../web/Stories.svelte';
  import Footer from './Footer.svelte';
</script>

<style lang="scss">
  .sidebar {
    margin: 4.5em 0 0 0;

    .sidebar-container {
      position: fixed;
    }
  }
</style>

<div class="sidebar">
  <div class="sidebar-container">
    <Profile />
    <Stories />
    <Footer />
  </div>
</div>
