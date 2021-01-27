<script>
  let style = { darkMode: false };

  const toggle = () => {
    style.darkMode = !style.darkmode;

    let main = document.querySelector('.main');

    main.classList.toggle('dark-mode');
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
      background-color: #dc49a7;

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
