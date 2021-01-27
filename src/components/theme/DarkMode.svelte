<style lang="scss">
  $primary: #2c2c2c;
  $second: #333333;
  $white: #fafafa;
  $gray: #c7c7c7;
  $logo: #FA95A1;

  :global(.header-dark) {
    background-color: $second !important;
    transition: 0.5s;

    :global(h1) {
      color: $logo !important;
      background: none !important;
      mix-blend-mode: inherit !important;
      text-decoration: underline !important;
      &:before {
        display: none !important;
      }
    }

    :global(ul li i) {
      color: $white !important;
    }
  }

  :global(.profile-dark) {
    :global(.avatar img) {
      border: 1px solid $second !important;
    }
    :global(h2) {
      color: $white !important;
    }
    :global(span) {
      color: $white !important;
    }
  }

  :global(.stories-dark) {
    background-color: $second !important;
    border: none !important;
    transition: 0.5s;

    :global(h2) {
      color: $white !important;
    }
    :global(span) {
      color: $gray !important;
    }
  }

  :global(.main-dark) {
    background-color: $primary !important;
    transition: 0.5s;
  }

  :global(.card-dark) {
    background-color: $second !important;
    border: none !important;
    transition: 0.5s;

    :global(h3) {
      color: $white !important;
    }
    :global(h2) {
      color: $white !important;
    }
    :global(span) {
      color: $white !important;
    }

    :global(i) {
      color: $white !important;
    }

    :global(.user img) {
      border: 1px solid $white !important;
    }

    :global(.comments) {
      :global(.add) {
        :global(input) {
          background-color: $second !important;
          transition: 0.5s;
        }
        :global(button) {
          background-color: $primary !important;
          color: $white !important;
          transition: 0.5s;
        }
      }
    }
  }
</style>
