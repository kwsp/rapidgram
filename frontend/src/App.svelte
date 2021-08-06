<script>
  import Navbar from './Components/Navbar.svelte'
  import PostList from './Components/PostList.svelte'
</script>

<!-- Top bar -->
<Navbar />
<main>
  <div class="main-container">
    <!-- Posts -->
    <PostList />
  </div>
</main>

<style>
  main {
    display: flex;
  }

  .main-container {
    padding-top: 30px;
    max-width: 935px;
    width: 100%;
    margin: 0 auto;
  }
</style>
