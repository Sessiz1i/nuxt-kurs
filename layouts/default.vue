<template>
  <div>
    <div id="nav">
        <div class="nav-content">
          <nuxt-link to="/">Home</nuxt-link>
          <nuxt-link to="/videos">Videos</nuxt-link>
        </div>
    </div>
    <div class="content">
      <nuxt/>
    </div>
  </div>
</template>

<style>
.content{
  max-width: 50rem;
  margin: auto;
}
.nav-content{
  display: flex;
  max-width: 50rem;
  margin: auto;
}
#nav {
  overflow: hidden;
  width: 100%;
  height: auto;
  background-color: #333;
}

#nav a {
  color: white;
  letter-spacing: 1px;
  padding: .5rem 1rem;
  font-size: 1.5rem;
  font-weight: 700;
  text-transform: uppercase;
  text-decoration: none;
  transition: all .3s;
}
#nav a:hover{
  background-color: #41b883;
  color: #333333;
}
#nav a.nuxt-link-exact-active{
  background-color: #41b883;
  color: white;
}
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
  Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
