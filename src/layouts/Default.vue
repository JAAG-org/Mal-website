<template>
  <div class="block">
    <header class="header">
        <strong>
          <g-link to="/">{{ $static.metadata.siteName }}</g-link>
        </strong>
        <nav class="nav">
          <g-link class="nav__link" to="/">Home</g-link>
          <g-link class="nav__link" to="/about/">About</g-link>
          <g-link class="nav__link" to="/event/">Events</g-link>
        </nav>
      </header>
    <div class="layout">
      <div class="content"> 
        <slot/>
      </div>
    </div>
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
  font-family: 'Helvetica Neue', Arial, sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  background-color: rgb(228, 228, 228);
}

.content {
  margin-top: 80px;
}

h1 {
  font-family: 'Helvetica Neue', Roboto, Arial, sans-serif;
}

a {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  text-decoration: none;
  color: black;
}

p {
  font-family: 'Helvetica Neue', Arial, sans-serif;
}

a:hover {
  text-decoration: underline;
  font-style: italic;
}

.layout {
  margin: 0 auto;
  padding-left: 40px;
  padding-right: 40px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
  width: 100%;
  position: fixed;
  top: 0px;
  z-index: 999;
  padding-left: 20px;
  padding-right: 20px;
}
.nav {
  position: absolute;
  right: 80px;
}
.nav__link {
  margin-left: 20px;
}

.noselect {
  -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
     -khtml-user-select: none; /* Konqueror HTML */
       -moz-user-select: none; /* Old versions of Firefox */
        -ms-user-select: none; /* Internet Explorer/Edge */
            user-select: none; /* Non-prefixed version, currently
                                  supported by Chrome, Edge, Opera and Firefox */
}
</style>
