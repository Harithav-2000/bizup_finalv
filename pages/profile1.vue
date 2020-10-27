<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div v-for="user_alias in User">
                      <div v-show="user_alias._id===id">
                       <div class="card">
                       <div class="profile-img">
                        <a href="#">
                        <img src="https://bootdey.com/img/Content/avatar/avatar7.png" alt="" title=""/>
                        </a>
                       </div>
                        <div>
                        <h3>ENTERPRISE NAME</h3>
                         <h4>{{user_alias.ename}} </h4>
                         </div>
                        </div>
                        <div class="card0">
                         <h4><b>ABOUT US</b></h4>
                         <h5>{{user_alias.about}} </h5>
                        </div>
                        <div class="card1">
                         <h4><b>CONTACT DETAILS</b></h4>
                         <h5><b>EMAIL_ID:</b>{{user_alias.email}}</h5>
                         <h5><b>PHONE_NO:</b>{{user_alias.phone}}</h5>
                         <h5><b>LOCATION:</b>{{user_alias.location}}</h5>
                         <h5><b>ADDRESS:</b>{{user_alias.address}}</h5>
                        </div>
                        <div class="card2">
                          <h5><b>PREFERANCES:</b>{{user_alias.preferance}}</h5>
                          <h5><b>CATEGORY:</b>{{user_alias.category}}</h5>
                        </div>
                      </div>
          </div>
        </div>
      </div>
    </div>
  <div>
   <label><span>&nbsp;</span><input type="submit" v-on:click.prevent="generateprofile()" value="Submit" />
      </label>
      </div>

  </section>
</template>

<script>
import Headers from "../components/Header.vue";
import axios from 'axios';
import {Router} from "vue-router";

export default {
  components: {
    Headers,
  },
   name: 'use5',
    data(){
        return{
            User: [],
            id:this.$route.query.id
            
        }
    },
methods:{
  generateprofile:function(id)
  {
    axios.get('http://localhost:3000/api/users?id=' +id).then((response)=>{
    console.log(response.data);
    this.User = response.data;
    })
    .catch((error)=>{
        console.log(error);
    })
  }
  }
};
</script>


<style>

.profile-img a {
  bottom: 15px;
  box-shadow: none;
  display: block;
  top: 0px;
  padding: 1px;
  position: absolute;
  height: 160px;
  width: 160px;
  background: rgba(0, 0, 0, 0.3) none repeat scroll 0 0;
  z-index: 9;
}
.profile-img img {
  background-color: #fff;
  border-radius: 2px;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.07);
  height: 158px;
  padding: 5px;
  width: 158px;
}


.card{
  position:centre;
  top: -10px;
  bottom:-150px;
  box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);
  margin:auto;
  width:900px;
  height:250px;
  text-align:centre;
  text-position:bottom;
  left:0;
  right:0;
  color:white;
  background-color:#93D;
}
.card0{
  position:centre;
  top:-100px;
  bottom:-200px;
  box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);
  margin:auto;
  width:900px;
  text-align:centre;
  background-color:wheat;
}
.card1{
  position:centre;
  top:-5px;
  bottom:-150px;
  box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);
  margin:auto;
  text-align:centre;
  background-color:wheat;
}
.card2{
  position:centre;
  top:100px;
  bottom:-200px;
  box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);
  margin:auto;
  width:900px;
  text-align:centre;
  background-color:wheat;
}
</style>
