<script lang="ts">
  let isOpen: boolean = false;

  const toggleMenu = (): void => {
    isOpen = !isOpen;
  }
</script>

<style lang="scss">
  .menu {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.9);
    transform: scale(0);
    transition: transform 1s ease;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #eee;
    z-index: 1;

    &.open {
      transform: scale(1);
    }

    ul {
      list-style: none;
      text-align: center;
      padding: 0;
      margin: 0;

      li {
        margin: 0;
        padding: 10px;
        a {
          color: #eee;
          text-decoration: none;
          font-size: 2rem;
          font-family: baskerville, serif;
          font-weight: bold;
          text-transform: uppercase;
          letter-spacing: 0.2rem;
          transition: color 0.3s ease;

          &:hover {
            color: #aaa;
          }
        }
      }
    }

  }

  .hamburger {
    position: absolute;
    top: 30px;
    right: 30px;
    cursor: pointer;
    filter: drop-shadow(0 0 2px rgba(0, 0, 0, 0.5));
    z-index: 2;

    .line {
      transition: all 0.3s ease;
    }

    &.open {
      .top {
        fill: white;
        transform: rotate(45deg) translate(10px, -15px);
      }

      .middle {
        opacity: 0;
      }

      .bottom {
        fill: white;
        transform: rotate(-45deg) translate(-30px, 15px);
      }
    }
  }
</style>

<div class="hamburger" class:open={isOpen} on:click={toggleMenu}>
  <svg viewBox="0 0 100 80" width="40" height="40">
    <rect class="line top" width="90" height="3" fill="#333" rx="5" ry="5"></rect>
    <rect class="line middle" y="20" width="90" height="3" fill="#333" rx="5" ry="5"></rect>
    <rect class="line bottom" y="40" width="90" height="3" fill="#333" rx="5" ry="5"></rect>
  </svg>
</div>

<div class="menu" class:open={isOpen} on:click={toggleMenu}>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
  </ul>
</div>
