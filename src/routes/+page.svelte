<script>
  let names = ['Aiden','Arion','Edard','Patrock','Harryx','Davon','Waelon','Rohn','Brayln','Maddax']
  const randomItem = (arr) => arr[(Math.random() * arr.length) | 0];
</script>

<div class="greeting-container">
  <div class="greeting">Good morning,</div>
  <div class="name">{randomItem(names)}</div>
</div>

<div class="search-container">
  <input type="text" placeholder="Search #tags @locations and /names ..." />
</div>

<div class="feed">
  <div class="controls">
    <div class="label">Mode</div>
    <div class="buttons">
      <div class="button">National</div>
      <div class="button selected">International</div>
    </div>
  </div>
  <div class="posts-list">
    <div class="post">
      <div class="content">
        <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
      </div>
      <div class="footer">
        <div class="author">
          <div class="avatar"></div>
          <div class="info">
            <time>June 21, 2022</time>
            <div class="handle">
              <div class="location">
                <img src="flags/norway.svg" alt="Norway" />
              </div>
              <div class="username">User Username</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .posts-list {
    margin: 2rem;
    display: grid;
    grid-auto-columns: minmax(100px, auto);
  }
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
    gap: .5rem;
  }
  .post .avatar {
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    background-color: var(--dark);
  }
  .post .handle {
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
  .greeting-container {
    position: relative;
    margin: 0 auto;
    max-width: 60rem;
    width: 100%;
    font-size: 1.25rem;
  }
  .greeting, .name {
    margin: 0 2rem;
  }
  .name {
    color: var(--lightest);
    font-weight: 500;
  }
  .search-container {
    position: relative;
    display: grid;
    z-index: 20;
  }
  input {
    margin: 2rem;
    padding: 1rem;
    border-radius: 1rem;
    font-size: 1rem;
    background-color: var(--dark);
    color: var(--lightest);
    border: 0;
    outline: .5rem solid var(--darkest);
  }
  input:focus {
    outline: .5rem solid var(--darker);
  }
  .controls {
    margin: 0 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: .5rem;
  }
  .label {
    font-size: 1.25rem;
    color: var(--lightest);
  }
  .buttons {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: wrap;
    gap: .5rem;
  }
  .button {
    display: inline-block;
    padding: .2rem .6em;
    border-radius: 999px;
    border: 2px solid var(--darker);
    cursor: pointer;
  }
  .button.selected {
    background: var(--darker);
  }
</style>