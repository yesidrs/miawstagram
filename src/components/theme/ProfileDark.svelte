<style lang="scss">
  @import '../scss/variables.scss';

  :global(.profile-dark) {
    :global(.content) {
      display: flex;
      align-items: center;

      :global(.avatar) {
        :global(img) {
          width: 42px;
          height: 42px;
          border-radius: 50%;
          border: 1px solid $second !important;
        }
      }
      :global(.info) {
        margin: 0 0 0 0.5em;
        :global(h2) {
          font-size: 14px;
          color: $white;
          margin: 0;
          padding: 0;
        }
        :global(span) {
          font-size: 12px;
          font-weight: normal;
          color: $white;
        }
      }
    }
  }
</style>
