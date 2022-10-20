<template>
<div class="main">
  <h2>Logged in as: {{user.firstName}} {{user.lastName}} <button @click="logout" class="pure-button pure-button-primary">Logout</button></h2>
  <h1>My Fleet</h1>

<div class='fleet'>
      <div class='footer-item2 fleet-one'>
        <p>View Our Fleet.</p>
      </div>
    </div>
    <div class='footer'>
      <div class='footer-item footer-one'>
        <img src='../assets/image1.jpg'/>
      </div>
      <div class='footer-item footer-three'>
        <img src='../assets/3.jpg'/>
      </div>
      <div class='footer-item footer-four'>
        <img src='../assets/4.jpg'/>
      </div>
      <div class='footer-item footer-five'>
        <img src='../assets/5.jpg'/>
      </div>
      <div class='footer-item footer-six'>
        <img src='../assets/6.jpg'/>
      </div>
    </div>
    <div class='footer2'>
      <div class='text-info footer-one'>
        <p>Meet Road Warrior <br> Sleeps:6 <br> 4 Wheel Drive <br> Call Now To Book</p>
      </div>
      <div class='text-info footer-three'>
         <p>Meet Snow Bird <br> Sleeps:4 <br> 2 Wheel Drive <br> Call Now To Book</p>
      </div>
      <div class='text-info footer-four'>
         <p>Meet KT22 <br> Sleeps:8-10 <br> 4 Wheel Drive <br> Call Now To Book</p>
      </div>
      <div class='text-info footer-five'>
        <p>Meet Caddis Killer <br> Sleeps:4 <br> 2 Wheel Drive <br> Call Now To Book</p>
      </div>
      <div class='text-info footer-six'>
         <p>Meet Alta <br> Sleeps:10 <br> 4 Wheel Drive <br> Call Now To Book</p>
      </div>
    </div>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'MyFleet',
  computed: {
    user() {
      return this.$root.$data.user;
    }
  },
  methods: {
    async logout() {
      try {
        await axios.delete("/api/users");
        this.$root.$data.user = null;
      } catch (error) {
        this.$root.$data.user = null;
      }
    },
  }
}
</script>

<style scoped>

.footer2 {
  display: flex;
  justify-content: space-between;
}
.footer {
  display: flex;
  justify-content: space-between;
}
.fleet {
  background-color: #DB9964;
  font-size: 20px;
  font-family: Arial, Helvetica, sans-serif;
}
.footer-item2 {
  border: 5px solid #DB9964;
  height: 50px;
}
.footer-item {
  border: 1px solid #767676;
  background-color:  #ffff;
  height: 150px;
 
}
.text-info {
  border: 1px solid #767676;
  background-color: #ffff;
  height: 100px;
}

img {  
max-width: 100%;  
}  


.footer-one,
.footer-two,
.footer-three,
.footer-four,
.footer-five,
.footer-six {
  background-color: #fff;
  /*flex: initial;*/
  width: 300px;
}

</style>