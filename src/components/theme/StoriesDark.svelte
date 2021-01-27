<style lang="scss">
  @import '../scss/variables.scss';

  :global(.stories-dark) {
    border-radius: 4px;
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: $second;
    transition: 0.5s;

    :global(.stories-container) {
      :global(.head) {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0.5em 0 0 0;
        
        :global(h2) {
          font-size: 12px;
          color: $white;
          font-weight: 600;
        }
        :global(span) {
          font-size: 12px;
          font-weight: normal;
          color: $gray;
          cursor: pointer;
        }
      }

      :global(.items) {
        margin: 0.5em 0 0.5em 0;

        :global(.item) {
          display: flex;
          align-items: center;
          margin: 0 0 0.5em 0;

          :global(img) {
            width: 32px;
            height: 32px;
            border-radius: 50%;
          }

          :global(h2) {
            font-size: 14px;
            color: $white;
            margin: 0 0 0 0.5em;
            :global(span) {
              display: block;
              font-size: 9px;
              text-transform: uppercase;
              color: gray;
            }
          }

          :global(.item-box) {
            width: 32px;
            height: 32px;
            border: double 2px transparent;
            border-radius: 100%;
            background-image: linear-gradient(#fff, #fff),
              radial-gradient(circle at top left, #f09433, #bc1888);
            background-origin: border-box;
            background-clip: content-box, border-box;
          }
        }
      }
    }
  }
</style>
