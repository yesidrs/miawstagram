<script>
  import { blur } from 'svelte/transition';
  import Comments from './Comments.svelte';
  import Modal from '../utils/Modal.svelte';
  import Share from '../utils/Share.svelte';
  import CardDark from '../theme/CardDark.svelte';
  import { likeCount } from '../store/store.js';

  export let post;

  let isModal = false;
  let like = false;
  let bookmark = false;

  const handleClick = () => {
    isModal = !isModal;
  };

  const handleLike = () => {
    like = !like;

    if (like) {
      likeCount.update(n => n + 1);
    } else {
      likeCount.update(n => n - 1);
    }
  };
</script>

<style lang="scss">
  .card {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
    transition: 0.5s;

    .card-container {
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

    .active-like {
      color: #bc1888;
      animation: bounce linear 0.8s;
      animation-iteration-count: 1;
      transform-origin: 20% 20%;
    }
    .active-bookmark {
      color: #f09433;
    }
  }
</style>

<CardDark />

<div class="card" id="card">
  {#if isModal}
    <div transition:blur>
      <Modal>
        <Share on:click={handleClick} />
      </Modal>
    </div>
  {/if}
  <div class="card-container">
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
      <figure on:dblclick={handleLike}>
        <img src={post.photo} alt={post.username} />
      </figure>
    </div>
    <div class="icons">
      <div class="icons-first">
        <i class="fa fa-heart" class:active-like={like} on:click={handleLike} />
        <i class="fa fa-paper-plane" on:click={handleClick} />
      </div>
      <div class="icons-second">
        <i
          class="fa fa-bookmark"
          class:active-bookmark={bookmark}
          on:click={() => (bookmark = !bookmark)}
        />
      </div>
    </div>
    <div class="description">
      <h3>{post.username}</h3>
      <span>{post.postComment}</span>
    </div>
    <Comments comments={post.comments} />
  </div>
</div>
