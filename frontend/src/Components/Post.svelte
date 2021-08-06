<script>
  import UserHandle from './UserHandle.svelte'

  export let caption

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
      <UserHandle handle={userData.handle} />
    </div>
  </header>

  <!-- Post media-->
  <div>
    <img src={imgData.src} alt={imgData.alt} />
  </div>

  <!-- Caption and comments -->
  <div>
    Captions and comments
    <div>
      <span class="handle">
        {userData.handle}
      </span>
      <span>
        {caption}
      </span>
    </div>
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
</style>
