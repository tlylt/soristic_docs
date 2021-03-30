<header>
    <link
      href="/tabulator_modern.css"
      rel="stylesheet"
    />
    <script
      type="text/javascript"
      src="/tabulator.min.js"
    ></script>
  <navbar type="dark">
    <a slot="brand" href="{{baseUrl}}/index.html" title="Home" class="navbar-brand">Soristic Docs</a>
    <li slot="right">
      <form class="navbar-form">
        <searchbar :data="searchData" placeholder="Search" :on-hit="searchCallback" menu-align-right></searchbar>
      </form>
    </li>
  </navbar>
</header>
