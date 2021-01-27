<style lang="scss">
  .share {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
    width: 300px;
    height: 80px;
    position: absolute;
    top: 300px;
    left: 30%;
    z-index: 9;
    padding: 1em;

    .head {
      display: flex;
      justify-content: space-between;
      align-items: center;
      h2 {
        font-size: 16px;
      }
      i {
        cursor: pointer;
      }
    }

    .content {
      a {
        display: flex;
        align-items: center;
        text-decoration: none;
        color: black;
        font-size: 14px;
        margin: 2em 0 0 0;
      }
      i {
        color: #3b5998;
        margin: 0 0.5em 0 0;
        font-size: 20px;
      }
    }
  }
</style>

<div class="share">
  <div class="head">
    <h2>Compartir</h2>
    <i class="fas fa-times-circle" on:click/>
  </div>
  <div class="content">
    <a href="https://www.facebook.com/sharer.php?&u=https://miawstagram.co" target="_blank">
      <i class="fab fa-facebook-square" />
      Compartir en Facebook
    </a>
  </div>
</div>
