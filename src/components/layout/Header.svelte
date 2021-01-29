<script>
  import HeaderDark from '../theme/HeaderDark.svelte';
  import ThemeButton from '../utils/ThemeButton.svelte';
  import { likeCount } from '../store/store.js';
</script>

<style lang="scss">
  .header {
    background-color: white;
    position: fixed;
    width: 100%;

    .header-container {
      grid-template-columns: minmax(auto, 936px);
      display: grid;
      justify-content: center;
      background-color: white;
      box-shadow: 0px 8px 15px -9px rgba(0, 0, 0, 0.2);
      transition: 0.5s;

      .content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.5em;

        .logo {
          h1 {
            padding: 0;
            margin: 0;
            font-size: 28px;
            color: #be1d84;
            font-family: 'Pacifico', cursive;
            cursor: pointer;
            position: relative;
            background: #fff;
            mix-blend-mode: multiply;
            display: inline-block;

            &:before {
              content: '';
              display: block;
              width: 100%;
              height: 100%;
              background: radial-gradient(circle at top left, #f09433, #bc1888);
              mix-blend-mode: screen;
              position: absolute;
              top: 0;
              left: 0;
            }
          }
        }

        .nav {
          ul {
            list-style: none;
            margin: 0;
            display: flex;
            align-items: center;

            li {
              display: inline-block;
              margin: 0 0 0 1em;
            }

            i {
              font-size: 16px;
              color: rgba(38, 38, 38, 0.7);
              cursor: pointer;
            }
          }
        }
      }
    }
  }
</style>

<HeaderDark />

<div class="header" id="header">
  <div class="header-container">
    <div class="content">
      <div class="logo">
        <h1>Miawstagram</h1>
      </div>
      <div class="nav">
        <ul>
          <li><ThemeButton /></li>
          <li>{$likeCount === 0 ? '' : $likeCount}</li>
          <li><i class="fas fa-heart" /></li>
          <li><i class="fas fa-user-alt" /></li>
        </ul>
      </div>
    </div>
  </div>
</div>
