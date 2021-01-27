<style lang="scss">
  @import '../scss/variables.scss';

  :global(.comments-dark) {
    :global(.content) {
      padding: 0 1em 0.5em 1em;
      :global(.users) {
        margin: 0 0 0.5em 0;
        display: flex;

        :global(h3) {
          font-size: 14px;
          color: $white;
          font-weight: bold;
          margin: 0;
          padding: 0;
        }
        :global(span) {
          font-size: 14px;
          margin: 0 0 0 0.5em;
          font-weight: normal;
          color: $white;
        }
      }
    }

    :global(.add) {
      padding: 1em 1em 1em 1em;
      border-top: 1px solid rgba(219, 219, 219, 0.8);
      :global(form) {
        display: flex;
        justify-content: space-between;
        align-items: center;

        :global(input) {
          color: #696969;
          border: 1px solid transparent;
          font-size: 12px;
          outline: none;
          width: 100%;
          display: flex;
          transition: 0.5s;
          background-color: $second;
        }
        :global(button) {
          background-color: $primary;
          border: none;
          color: $white;
          font-size: 12px;
          outline: none;
          cursor: pointer;
          transition: 0.5s;
        }
      }
    }
  }
</style>