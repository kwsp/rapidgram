<script>
  export let handle
</script>

<span class="handle">
  <a href={`/u/${handle}`}>
    {handle}
  </a>
</span>

<style>
  a {
    text-decoration: none;
    color: inherit;
  }

  a:hover {
    text-decoration: underline;
  }

  .handle {
    font-weight: 600;
  }
</style>
