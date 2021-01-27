<script>
  let darkMode = false;

  const toggle = () => {
    darkMode = !darkMode;

    let header = document.getElementById('header');
    let main = document.getElementById('main');
    let profile = document.getElementById('profile');
    let stories = document.getElementById('stories');
    let cards = document.querySelectorAll('#card');
    let comments = document.querySelectorAll('#comments');

    header.classList.toggle('header');
    header.classList.toggle('header-dark');

    main.classList.toggle('main');
    main.classList.toggle('main-dark');

    stories.classList.toggle('stories');
    stories.classList.toggle('stories-dark');

    profile.classList.toggle('profile');
    profile.classList.toggle('profile-dark');

    cards.forEach((card) => {
      card.classList.toggle('card');
      card.classList.toggle('card-dark');
    });

    comments.forEach((comment) => {
      comment.classList.toggle('comments');
      comment.classList.toggle('comments-dark');
    });
  };
</script>

<style lang="scss">
  .toggle {
    position: relative;
    width: 50px;
    height: 24px;
    appearance: none;
    background-color: #c6c6c6;
    outline: none;
    border-radius: 20px;
    box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);

    &:checked {
      background-color: #fa95a1;

      &:before {
        left: 30px;
      }
    }

    &:before {
      content: '';
      position: absolute;
      width: 24px;
      height: 24px;
      border-radius: 20px;
      top: 0;
      left: 0;
      background-color: #fafafa;
      transform: scale(1.1);
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
      transition: 0.5s;
    }
  }
</style>

<input type="checkbox" class="toggle" on:click={toggle} />
