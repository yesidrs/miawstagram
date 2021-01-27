<style lang="scss">
  @import '../scss/variables.scss';
  :global(.main-dark) {
    display: grid;
    grid-template-columns: minmax(auto, 936px);
    justify-content: center;
    background-color: #2c2c2c;
    transition: 0.5s;

    :global(.main-container) {
      display: grid;
      grid-template-columns: 3fr 1fr;
      grid-gap: 2em;
      padding: 2em 0;
    }
  }
</style>
