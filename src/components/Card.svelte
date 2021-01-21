<script>
  import Comments from './Comments.svelte';
</script>

<div class="card">
  <div class="container">
    <div class="header">
      <div class="user-info">
        <img src="/img/elmo.jpg" alt="" />
        <h2>Elmo.pug</h2>
        <span>Medellín, Colombia</span>
      </div>
      <div class="settings"><i class="fa fa-ellipsis-h" /></div>
    </div>
    <div class="photo">
      <figure><img src="/img/elmo.jpg" alt="" /></figure>
    </div>
    <div class="icons">
      <div class="icons-first">
        <i class="fa fa-heart" />
        <i class="fa fa-paper-plane" />
      </div>
      <div class="icons-second">
        <i class="fa fa-bookmark" />
      </div>
    </div>
    <div class="description">
      <h3>Elmo.pug</h3>
      <span>Hola!</span>
    </div>
    <Comments />
  </div>
</div>
