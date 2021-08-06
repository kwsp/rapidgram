<script>
  import Post from './Post.svelte'

  const posts = [
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
    'placeholder...',
  ]
</script>

<div class="container">
  {#each posts as post}
    <div class="post-container" style="height=100">
      <Post caption={post} />
    </div>
  {/each}
</div>

<style>
  .container {
    max-width: 600px;
  }
</style>
