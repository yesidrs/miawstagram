<script>
  import Comments from './Comments.svelte';

  export let post;
</script>

<style lang="scss">
  .card {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;

    .container {
      .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1em;

        .user {
          display: flex;
          align-items: center;
          justify-content: flex-end;
          img {
            width: 32px;
            height: 32px;
            border-radius: 50%;
          }

          .info {
            display: flex;
            flex-direction: column;

            h2 {
              margin: 0;
              padding: 0;
              font-size: 14px;
              font-weight: 600;
              margin: 0 0 0 1em;
              color: black;
            }

            span {
              display: block;
              font-size: 12px;
              font-weight: normal;
              color: rgba(38, 38, 38, 0.7);
              margin-left: 14px;
              margin-top: 5px;
            }
          }
        }

        .settings {
          i {
            cursor: pointer;
          }
        }
      }

      .photo {
        padding: 0;
        margin: 0;
        figure {
          margin: 0;
          padding: 0;
          cursor: pointer;

          img {
            width: 100%;
            height: auto;
          }
        }
      }

      .icons {
        padding: 1em;
        display: flex;
        justify-content: space-between;
        align-items: center;

        i {
          margin: 0 1em 0 0;
          cursor: pointer;
          font-size: 20px;

          &:last-child {
            margin: 0;
          }
        }
      }

      .description {
        padding: 0 1em 1em 1em;

        h3 {
          font-size: 14px;
          font-weight: bold;
          color: black;
        }
        span {
          font-size: 14px;
        }
      }
    }
  }

  // .active-like {
  //   color: #bc1888;
  //   animation: bounce linear 0.8s;
  //   animation-iteration-count: 1;
  //   transform-origin: 20% 20%;
  // }
  // .active-bookmark {
  //   color: #f09433;
  // }

  @keyframes bounce {
    0% {
      transform: translate(0px, 0px);
    }
    15% {
      transform: translate(0px, -25px);
    }
    30% {
      transform: translate(0px, 0px);
    }
    45% {
      transform: translate(0px, -15px);
    }
    60% {
      transform: translate(0px, 0px);
    }
    75% {
      transform: translate(0px, -5px);
    }
    100% {
      transform: translate(0px, 0px);
    }
  }
</style>

<div class="card">
  <div class="container">
    <div class="header">
      <div class="user">
        <img src={post.avatar} alt="" />
        <div class="info">
          <h2>{post.username}</h2>
          <span>{post.location}</span>
        </div>
      </div>
      <div class="settings"><i class="fa fa-ellipsis-h" /></div>
    </div>
    <div class="photo">
      <figure><img src={post.photo} alt="" /></figure>
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
      <h3>{post.username}</h3>
      <span>{post.postComment}</span>
    </div>
    <Comments comments={post.comments}/>
  </div>
</div>
