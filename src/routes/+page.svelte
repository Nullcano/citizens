<script>
  import PostOne from "$lib/PostOne.svelte";
  let names = ['Aiden','Arion','Edard','Patrock','Harryx','Davon','Waelon','Rohn','Brayln','Maddax']
  const randomItem = (arr) => arr[(Math.random() * arr.length) | 0];
</script>

<div class="greeting-container">
  <div class="greeting">Good morning,</div>
  <div class="name">{randomItem(names)}</div>
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
    <PostOne />
    <PostOne />
    <PostOne />
    <PostOne />
    <PostOne />
  </div>
</div>

<style>
  .posts-list {
    margin: 1rem;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1rem;
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