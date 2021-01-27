<script>

import ProfileDark from "../theme/ProfileDark.svelte";

</script>
<style lang="scss">
  .profile {
    .content {
      display: flex;
      align-items: center;

      .avatar {
        img {
          width: 42px;
          height: 42px;
          border-radius: 50%;
        }
      }
      .info {
        margin: 0 0 0 0.5em;
        h2 {
          font-size: 14px;
          color: black;
          margin: 0;
          padding: 0;
        }
        span {
          font-size: 12px;
          font-weight: normal;
        }
      }
    }
  }
</style>

<ProfileDark />

<div class="profile" id="profile">
  <div class="content">
    <div class="avatar">
      <img src="/img/profile.jpg" alt="profile" />
    </div>
    <div class="info">
      <h2>Entwickler</h2>
      <span>Yesid Rodelo</span>
    </div>
  </div>
</div>
