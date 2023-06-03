<div class="content">
  <main><slot /></main>
  <footer>
    <small>Fachvortrag – Moritz Kronberger – 15.06.2023</small>
    <small>Web-Technologien – Fabian Ziegler</small>
  </footer>
</div>

<style>
  .content {
    height: 100vh;
    width: 100vw;
    position: relative;
    padding: var(--spacing-10);
    padding-bottom: var(--spacing-05);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  main {
    height: 100%;
  }

  footer {
    opacity: 0.5;
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
</style>
