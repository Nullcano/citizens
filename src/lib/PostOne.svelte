<script>
  import { randomInteger, randomItem, names } from '$lib/utils';
</script>

<div class="post">
    <div class="content">
      <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
    </div>
    <div class="footer">
      <div class="author">
        <div class="avatar" style="background-image:url('avatars/{randomInteger(1, 10)}.png')"></div>
        <div class="info">
          <time>12:34 PM &middot; Jun 21 &middot; 2022</time>
          <div class="handle">
            <div class="location">
              <img src="flags/norway.svg" alt="Norway" />
            </div>
            <div class="username">{randomItem(names)} {randomItem(names)}</div>
          </div>
        </div>
      </div>
    </div>
</div>

<style>
  .post {
    background: var(--darker);
    border-radius: 2rem;
  }
  .post .content {
    margin: 2rem;
    font-size: 1.5rem;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 4;
    overflow: hidden;
    text-overflow: ellipsis;
    color: var(--lighter);
  }
  .post .footer {
    margin: 1rem;
    display: flex;
    justify-content: space-between;
  }
  .post .author {
    display: grid;
    grid-template-columns: 4rem 1fr;
    align-items: center;
    gap: 1rem;
  }
  .post .author .info {
    display: flex;
    flex-direction: column;
  }
  .post .avatar {
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    background-color: var(--dark);
    background-size: cover;
    background-position: center;
  }
  .post time {
    font-size: .8rem;
    text-transform: uppercase;
  }
  .post .handle {
    margin-left: -2.5rem;
    display: flex;
    align-items: center;
    gap: .5rem;
    font-weight: 500;
    color: var(--lightest);
  }
  .post .location {
    width: 2rem;
    opacity: .5;
  }
</style>