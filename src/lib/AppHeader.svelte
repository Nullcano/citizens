<header class="flex items-center">
  <div class="logo">
    CTZ
  </div>
  <div class="search-container">
    <input type="text" placeholder="#tag, @location, /name ..." />
  </div>
  <div class="menu-icon">
    <i></i>
    <i></i>
  </div>
</header>

<style>
  header {
    position: sticky;
    top: 0;
    padding: 1rem 2rem;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: var(--darker);
    z-index: 100;
  }
  .logo {
    position: relative;
    height: 3.5rem;
    font-size: 3rem;
    color: var(--lightest);
    font-family: 'Libre Barcode 39';
    overflow: hidden;
  }
  .search-container {
    position: relative;
    width: 70%;
    display: grid;
    z-index: 90;
  }
  input {
    width: 100%;
    padding: .5rem 1.5rem;
    border-radius: 1rem;
    font-size: 1rem;
    background-color: var(--dark);
    color: var(--lightest);
    border: 0;
    outline: .25rem solid var(--darker);
  }
  input:focus {
    outline: .25rem solid var(--darkest);
  }
  .menu-icon {
    width: 2rem;
    height: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: .5rem;
  }
  i {
    width: 2rem;
    height: .25rem;
    border-radius: .5rem;
    background: var(--lightest);
  }
  i:last-child {
    width: 1rem;
  }
  @media screen and (max-width: 60em) {
    .search-container {
      position: fixed;
      width: 100%;
      top: 5rem;
      left: 0;
      background: hsla(240, 7%, 11%, .9);
      backdrop-filter: blur(2px);
    }
    .search-container input {
      width: calc(100% - 4rem);
      margin: 2rem;
    }
  }
</style>