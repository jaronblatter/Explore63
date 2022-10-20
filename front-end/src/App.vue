<template>
<div id="app">
  <div class="header">
    <div class="brand">
      <div class="brand">
        <h1>Explore63</h1>
        <h2> RV Reservation system</h2>
      </div>
      <div class="about"> 
        <h2>
          
              <router-link class="pure-button-about" to="/about">About</router-link>
            
              <router-link class="pure-button-about" to="/">Home</router-link>

        </h2>
      </div>
    </div>
  </div>
 
  <router-view/>
 
</div>
</template>

<style>
/* green yellow red orange */
/* 96ceb4 ffeead d9534f ffad60 */
body {
  margin: 0px;
  background: #F7F5F7;
}

nav a.router-link-exact-active {
  color: #42b983;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.brand {
  display: flex;
  background: #96ceb4;
  padding: 15px 15px;
}

.spacer {
  padding: 10px;
}

.brand h1 {
  display: inline-block;
  background: #DB9964;
  padding: 10px;
  border-radius: 30px;
  font-size: 14px;
}

.about h2 {
  display: inline-block;
  background: #DB9964;
  padding: 10px;
  border-radius: 30px;
  font-size: 14px;
}

.h1 {
  padding: 10px;
}

.about {
  margin-left: auto;

}

.main {
  padding: 20px 100px;
}

.pure-button {
  font-size: 10px;
}

.pure-button-about {
  font-size: 16px;
  color: #333;
  display: inline-block;
  background: #DB9964;
  text-align: right;clear:left;
  padding: 10px;
  border-radius: 30px;
  font-size: 14px;
}

h1 {
  font-size: 16px;
}

h2 {
  font-size: 12px;
  padding: 10px;
}

.space-right {
  margin-right: 10px;
}

a {
  color: #ffad60;
}

.pure-button-primary {
  background-color: #ffad60;
  color: #333;
  border-radius: 30px;
}
</style>
