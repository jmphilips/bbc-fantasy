<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <div class="nav__toggle"><p class="nav__toggle__text">BOTTLE</p></div>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/constitution">Constitution</g-link>
        <g-link class="nav__link" to="/scoring">Scoring System</g-link>
        <g-link class="nav__link" to="/history">Book of Records</g-link>
        <g-link class="nav__link" to="/about/">About Us</g-link>
      </nav>
    </header>
    <div class="content">
      <slot/>
    </div>
    <footer>
      <div class="footer">
        <h2>----- Powered by Soju -----</h2>
      </div>
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
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

</style>
