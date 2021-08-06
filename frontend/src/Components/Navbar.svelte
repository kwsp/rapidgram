<script>
  import Icon from 'svelte-awesome'
  import { home, user, heart, compass, comments } from 'svelte-awesome/icons'
</script>

<nav>
  <div class="container1">
    <div class="container2">
      <div class="navLogo">Rapidgram Logo</div>
      <div class="navSearchBar">
        <input type="text" placeholder="Search" value="" />
      </div>
      <div class="navIcons">
        <Icon style="margin-left: 22px;" data={home} scale="1.7" />
        <Icon style="margin-left: 22px;" data={comments} scale="1.7" />
        <Icon style="margin-left: 22px;" data={compass} scale="1.7" />
        <Icon style="margin-left: 22px;" data={heart} scale="1.7" />
        <Icon style="margin-left: 22px;" data={user} scale="1.7" />
      </div>
    </div>
  </div>
</nav>

<style>
  nav {
    top: 0;
    height: 54px;
    display: flex;
    align-items: center;
  }

  .container1 {
    width: 100%;
    height: 54px;
    border-bottom: 1px solid rgba(219, 219, 219, 1);
    align-items: center;
    justify-content: center;
    flex-direction: row;
    position: fixed;
    z-index: 10;
  }

  .container2 {
    background-color: white;
    display: flex;
    width: 100%;
    height: 54px;
    max-width: 975px;
    padding: 0 20px;

    align-items: center;
    justify-content: center;
    flex-direction: row;
    z-index: 10;
  }

  .navLogo {
    flex: 1 9999 0%;
    min-width: 40px;
  }

  .navSearchBar {
    height: 28px;
    min-width: 125px;
    width: 215px;
    display: flex;
    flex-direction: column;
    flex: 0 1 auto;
  }

  .navSearchBar > input {
    font-size: 16px;
    border: 1px solid rgba(219, 219, 219, 1);
    background: rgba(250, 250, 250, 1);
    outline: 0;
    padding: 3px 10px 3px 26px;
  }

  .navIcons {
    display: flex;
    flex: 1 0 0%;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: flex-end;
  }

  .navIcon {
    margin-left: 22px;
  }
</style>
