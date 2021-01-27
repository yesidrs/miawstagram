<script>
  export let comments = [];

  const addComment = (e) => {
    const msg = e.target.text.value;
    const min = 3;

    if (msg.length > min) {
      const message = {
        id: Date.now(),
        text: msg,
        username: 'Entwickler'
      }

      comments = [...comments, message];
      e.target.text.value = '';
    }
  }
</script>

<style lang="scss">
  .comments {
    .content {
      padding: 0 1em 0.5em 1em;
      .users {
        margin: 0 0 0.5em 0;
        display: flex;

        h3 {
          font-size: 14px;
          color: black;
          font-weight: bold;
          margin: 0;
          padding: 0;
        }
        span {
          font-size: 14px;
          margin: 0 0 0 0.5em;
          font-weight: normal;
          color: rgba(38, 38, 38, 0.7);
        }
      }
    }

    .add {
      padding: 1em 1em 1em 1em;
      border-top: 1px solid rgba(219, 219, 219, 0.8);
      form {
        display: flex;
        justify-content: space-between;
        align-items: center;

        input {
          border: solid 1px #e9e9e9;
          border-radius: 5px;
          color: #696969;
          border: 1px solid transparent;
          font-size: 12px;
          outline: none;
          width: 100%;
          display: flex;
        }
        button {
          border: none;
          color: #3897f0;
          font-size: 12px;
          outline: none;
          cursor: pointer;
        }
      }
    }
  }
</style>

<div class="comments">
  <div class="content">
    {#each comments as comment}
      <div class="users">
        <h3>{comment.username}</h3>
        <span>{comment.text}</span>
      </div>
    {/each}
    <div class="add">
      <form on:submit|preventDefault={addComment} >
        <input type="text" name="text" placeholder="Agregar Comentario..." />
        <button type="submit">Post</button>
      </form>
    </div>
  </div>
</div>
