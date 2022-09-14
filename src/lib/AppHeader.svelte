<header class="flex items-center">
  <div class="logo">
    CTZ
  </div>
  <div class="search-container">
    <input type="text" placeholder="Search #tags @locations and /names ..." />
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
  }
  header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 11rem;
    border-bottom-left-radius: 2rem;
    border-bottom-right-radius: 2rem;
    background: var(--darker);
    z-index: -2;
  }
  header::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 14rem;
    background: linear-gradient(to bottom, var(--darker), transparent);
    z-index: -1;
  }
  
  .logo {
    position: relative;
    height: 3.5rem;
    font-size: 3rem;
    color: var(--lightest);
    font-family: 'Libre Barcode 39', cursive;
    overflow: hidden;
  }
  .search-container {
    position: relative;
    width: 70%;
    display: grid;
    z-index: 20;
  }
  input {
    width: 100%;
    padding: 1rem;
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
      width: 60%;
    }
  }
</style>