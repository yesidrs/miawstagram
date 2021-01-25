<script>
  import Header from './components/Header.svelte';
  import Main from './components/Main.svelte';
  import TimeLine from './components/TimeLine.svelte';
  import Sidebar from './components/Sidebar.svelte';
  import { onMount } from 'svelte';

  let data = {};
  const API = 'https://kittygram-api.now.sh/';

  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
  });
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400&family=Pacifico&display=swap');

  :global(body) {
    background-color: #fafafa;
    color: rgba(38, 38, 38, 0.7);
    font-family: 'Lato', sans-serif;

    :global(h1, h2, h3) {
      margin: 0;
    }
  }
</style>

<Header />
<Main>
  <TimeLine posts={data.posts}/>
  <Sidebar />
</Main>
