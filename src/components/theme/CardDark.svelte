<style lang="scss">
  @import '../scss/variables.scss';

  :global(.card-dark) {
    border-radius: 4px;
    background-color: $second;
    margin: 0 0 2em 0;
    transition: 0.5s;

    :global(.card-container) {
      :global(.header) {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1em;

        :global(.user) {
          display: flex;
          align-items: center;
          justify-content: flex-end;

          :global(img) {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            border: 1px solid $white;
          }

          :global(.info) {
            display: flex;
            flex-direction: column;

            :global(h2) {
              margin: 0;
              padding: 0;
              font-size: 14px;
              font-weight: 600;
              margin: 0 0 0 1em;
              color: $white;
            }

            :global(span) {
              display: block;
              font-size: 12px;
              font-weight: normal;
              color: $white;
              margin-left: 14px;
              margin-top: 5px;
            }
          }
        }

        :global(.settings) {
          :global(i) {
            cursor: pointer;
            color: $white;
          }
        }
      }

      :global(.photo) {
        padding: 0;
        margin: 0;
        :global(figure) {
          margin: 0;
          padding: 0;
          cursor: pointer;

          :global(img) {
            width: 100%;
            height: auto;
          }
        }
      }

      :global(.icons) {
        padding: 1em;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: $white;

        :global(i) {
          margin: 0 1em 0 0;
          cursor: pointer;
          font-size: 20px;

          &:last-child {
            margin: 0;
          }
        }
      }

      :global(.description) {
        padding: 0 1em 1em 1em;
        color: $white;

        :global(h3) {
          font-size: 14px;
          font-weight: bold;
        }
        :global(span) {
          font-size: 14px;
        }
      }
    }

    :global(.active-like) {
      color: #bc1888;
      animation: bounce linear 0.8s;
      animation-iteration-count: 1;
      transform-origin: 20% 20%;
    }
    :global(.active-bookmark) {
      color: #f09433;
    }
  }
</style>
