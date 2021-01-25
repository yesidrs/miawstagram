<div class="comments">
  <div class="content">
    <div class="users">
      <h3>El Firulais</h3>
      <span>Hola Elmo</span>
    </div>
    <div class="add">
      <form>
        <input type="text" id="text" placeholder="Agregar Comentario..." />
        <button type="submit">Post</button>
      </form>
    </div>
  </div>
</div>

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
