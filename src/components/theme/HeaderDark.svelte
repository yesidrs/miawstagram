<style lang="scss">
  @import '../scss/variables.scss';

  :global(.header-dark) {
    position: fixed;
    width: 100%;

    :global(.header-container) {
      background-color: $second;
      grid-template-columns: minmax(auto, 936px);
      display: grid;
      justify-content: center;
      box-shadow: 0px 8px 15px -9px rgba(0, 0, 0, 0.2);
      transition: 0.5s;

      :global(.content) {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.5em;

        :global(.logo) {
          :global(h1) {
            padding: 0;
            margin: 0;
            font-size: 28px;
            color: $logo;
            font-family: 'Pacifico', cursive;
            cursor: pointer;
            position: relative;
            display: inline-block;
            text-decoration: underline;
          }
        }

        :global(.nav) {
          :global(ul) {
            list-style: none;
            margin: 0;
            display: flex;
            align-items: center;

            :global(li) {
              display: inline-block;
              margin: 0 0 0 1em;
              color: $white;
            }

            :global(i) {
              font-size: 16px;
              cursor: pointer;
            }
          }
        }
      }
    }
  }
</style>
