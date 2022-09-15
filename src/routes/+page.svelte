<script>
  import { randomItem, names } from '$lib/utils'
  import PostOne from '$lib/PostOne.svelte'
  let userLoggedIn
  const login = () => userLoggedIn = !userLoggedIn
</script>

<div class="greeting-container">
  {#if (!userLoggedIn)}
  <div class="greeting">Welcome to Citizens.</div>
  <div class="name"><div class="login-button" on:click="{login}">Become one today</div></div>
  {:else}
  <div class="greeting">Good morning,</div>
  <div class="name">{randomItem(names)} {randomItem(names)}</div>
  {/if}
</div>

<div class="feed">
  <div class="controls">
    <div class="label">Mode</div>
    <div class="buttons">
      <div class="button">National</div>
      <div class="button selected">International</div>
    </div>
  </div>
  {#if (!userLoggedIn)}
  <div class="guest-view">
    Please <div class="login-button" on:click="{login}">log in</div> for smart feed
  </div>
  {/if}
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
    padding: 2rem;
    max-width: 60rem;
    width: 100%;
    font-size: 1.25rem;
    background: var(--dark);
    border-bottom-left-radius: 1.5rem;
    border-bottom-right-radius: 1.5rem;
  }
  .name {
    color: var(--lightest);
    font-weight: 500;
  }
  .controls {
    margin: 2rem;
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
  .login-button {
    cursor: pointer;
  }
  .guest-view .login-button {
    display: inline;
    padding: .25rem .5rem;
    border-radius: .5rem;
    border: 1px dashed var(--dark);
    cursor: pointer;
    transition: all .2s linear;
  }
  .guest-view .login-button:hover {
    color: var(--lighter);
  }
</style>