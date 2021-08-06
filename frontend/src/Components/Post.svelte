<script>
  import Handle from './Handle.svelte'

  export let caption
  export let postedWhen = '2 HOURS AGO'
  export let likedBy = [
    'teamusa',
    'thenzteam',
    'teamgb',
    'nu_sports',
    'allblacks',
  ]

  let userData = {
    handle: 'thenzteam',
    img: 'https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.olympic.org.nz%2Fassets%2FUploads%2FNZOC-Logo-Black-Background2.jpg&f=1&nofb=1',
  }

  let imgData = {
    src: 'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fresources.stuff.co.nz%2Fcontent%2Fdam%2Fimages%2F1%2Fo%2Fo%2F8%2Fh%2Fk%2Fimage.related.StuffLandscapeSixteenByNine.1420x800.1oo7om.png%2F1519932944035.jpg&f=1&nofb=1',
    alt: 'Some alt message',
  }
</script>

<article>
  <header>
    <!-- Profile picture -->
    <div class="profile-pic">
      <img src={userData.img} alt={'Profile picture of ' + userData.handle} />
    </div>
    <div class="header-rest">
      <Handle handle={userData.handle} />
    </div>
  </header>

  <!-- Post media-->
  <div>
    <img src={imgData.src} alt={imgData.alt} />
  </div>

  <!-- Caption and comments -->
  <div>
    <!-- Interaction buttons-->
    <section class="sec-interact">Icons</section>

    {#if likedBy.length > 0}
      <!-- Liked by -->
      <section class="sec-liked-by">
        <span>Liked by </span>
        <Handle handle={likedBy[0]} />
        <span> and </span>
        <span class="bold">
          {likedBy.length - 1} other{likedBy.length === 2 ? '' : 's'}
        </span>
      </section>
    {/if}

    <!-- Handle and caption-->
    <div class="sec-caption">
      <Handle handle={userData.handle} />
      <span>
        {caption}
      </span>
    </div>

    <div class="sec-posted-when">
      <!-- TODO: format time properly-->
      <time>
        {postedWhen}
      </time>
    </div>

    <!-- Add new comment-->
    <section class="sec-new-comment">New comment</section>
  </div>
</article>

<style>
  article {
    border-radius: 3px;
    border: 1px solid rgba(219, 219, 219, 1);

    margin-bottom: 24px;
  }

  header {
    height: 60px;
    padding: 16px;
    align-items: center;
    flex-direction: row;
  }

  header > .profile-pic {
    display: block;
    width: 32px;
    height: 32px;
  }

  .profile-pic > img {
    height: 100%;
    width: 100%;
    border-radius: 50%;
  }

  header > .header-rest {
    margin-left: 14px;
  }

  .sec-interact {
    padding: 0 16px;
    margin-top: 4px;
  }
  .sec-liked-by {
    display: block;
    padding: 0 16px;
    margin-bottom: 8px;
  }
  .sec-caption {
    display: block;
    padding: 0 16px;
  }
  .sec-posted-when {
    padding: 0 16px;
    font-size: 10px;
    color: rgba(142, 142, 142, 1);
    margin-top: 4px;
    margin-bottom: 4px;
  }
  .sec-new-comment {
    padding: 0 16px;
    margin-top: 4px;
  }

  .bold {
    font-weight: 600;
  }
</style>
