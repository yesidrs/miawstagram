<script>
  import { onMount } from 'svelte';
  import Header from './components/layout/Header.svelte';
  import Main from './components/layout/Main.svelte';
  import Sidebar from './components/layout/Sidebar.svelte';
  import TimeLine from './components/layout/TimeLine.svelte';

  let data = {};
  const API = 'https://kittygram-api.now.sh/';

  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
  });
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400&family=Pacifico&display=swap');
</style>

<Header />
<Main>
  <TimeLine posts={data.posts} />
  <Sidebar />
</Main>
