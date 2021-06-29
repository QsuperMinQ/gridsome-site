<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link class="nav__link" to="/">
        <!-- {{ $static.metadata.siteName }} -->
        <g-image class="logo" alt="Example image" src="https://gridsome-forestry.netlify.app/assets/img/logo.332701b7.svg" />
        </g-link>
        
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/journal/">Journal</g-link>
        <g-link class="nav__link" to="/contact/">Say Hi!</g-link>
        <g-link class="nav__link" to="/test/">test</g-link>
      </nav>
    </header>
    <slot/>
    <footer>
      <div class="footer">Copyright © 2021</div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  color: #000;
  font-size: 16px;
  box-sizing: border-box;
}

.layout {
  margin: 0 auto;
  padding: 1rem 6rem 0;
  max-width: 1200px;
  box-sizing: border-box;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-right: 20px;
  text-decoration: none;
  color: #000;
}

.logo {
  height: 1.15rem;
}

.footer {
  padding: 6rem 0;
  font-size: .8rem;
}
</style>
