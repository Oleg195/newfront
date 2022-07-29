<template>
  <div class="fon">
    <div class="menu">
      <div class="logo"></div>
      <div class="inform"><marquee behavior="scroll" direction="left" >Добро пожаловать на сайт </marquee></div>
    <div class="menuu"><RouterLink class="dom" to="/">Home</RouterLink> <p style="color:#2c5592">|</p>
    <RouterLink to="/products" class="ducts">Products</RouterLink> <p style="color:#2c5592">|</p> 
    <RouterLink to="/login" class="log">Login</RouterLink> <p style="color:#2c5592">|</p> 
    <RouterLink to="/cart" class="caart">Cart</RouterLink> <p style="color:#2c5592">|</p>
    <RouterLink to="/fav" class="faav">Fav</RouterLink>
    </div></div>
    <RouterView />
  </div>
</template>

<script>
import { createClient, provideClient } from '@urql/vue';
export default {
  setup() {
    const client = createClient({
      url: "http://38.242.229.113:8055/graphql",
      fetchOptions: () => {
      
      const token = localStorage.getItem('token')
      return {
        headers: { authorization: token ? `Bearer ${token}` : '' }
      };
    },
    });
    
    provideClient(client);
  }
}
</script>

<style scoped>

.logo{
  background-image: url("https://cdn.worldvectorlogo.com/logos/apple-4.svg");
     max-width: 100%;
     background-size: cover;

border: 6px solid #0f250c;
     display: flex; 
     justify-content: flex-start; 
     align-items: center; 
     padding-left: 1%; 
     color: rgb(211, 12, 12);
     height: 65px; 
    }
    .fon{background-image: url("https://img.freepik.com/free-photo/blue-sky-with-clouds_1127-282.jpg");
    
    -moz-background-size: 100%; /* Firefox 3.6+ */
    -webkit-background-size: 100%; /* Safari 3.1+ и Chrome 4.0+ */
    -o-background-size: 100%; /* Opera 9.6+ */
    background-size: 100%; /* Современные браузеры */
width: 100%;
background-attachment:fixed;

}
.inform{ width: 50%;
background-color: #e8e8e6;
background-image:url(https://demo.themeum.com/html/triangle/1.1/images/home/slider-bg.png;),url();background-position-y:bottom;background-repeat:no-repeat;
animation: gorod 5s infinite linear;}    
@keyframes gorod{0%{background-position-x:0%}100%{background-position-x:96% ;}
}


.dom:hover {
  color:rgb(149, 152, 168);
}
.ducts:hover {
  color:rgb(149, 152, 168);
}
.log:hover {
  color:rgb(149, 152, 168);
}
.caart:hover {
  color:rgb(149, 152, 168);
}
.faav:hover {
  color:rgb(149, 152, 168);
}
.loading { 
  font-size: 170%;
  text-align: center;
  padding: 5%;
    padding-bottom: 5%;
  padding-bottom: 15%;
  color: #7b7b7b66;
} 
 .error { 
  font-size: 170%;
  text-align: center;
  padding: 5%;
    padding-bottom: 5%;
  padding-bottom: 15%;
  color: #7b7b7b66;
} 
.menu{ 
  max-width: 100%;
    background-color: #237196;;
    height: 75px;
    display: flex;
    align-items: center;
    justify-content: space-around;
        border-bottom: 1px solid;
     box-shadow: rgb(44 85 146) 0px 19px 38px -29px inset; 

}
.menu h1{ 
      font-weight: initial;
      font-size: unset;
}
.menuu{ 

  display: flex;
  justify-content: flex-end;
  align-items: center;
 max-width: 100%;
}

a{
text-decoration: none;
color: #000000;
padding: 0px 10px 0px 10px;
font-size: unset;
text-transform: uppercase;
font-weight: bold;
}
/* .footer {
  background-color: #000000;
  color: aliceblue;
  text-align: center;
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 80px;
} */
@media only screen and (max-width: 320px) {
   .menuu {
    font-size: 12px
  }
  
}
@media only screen and (max-width: 375px) {

 
  
}
@media only screen and (max-width: 425px){

    .inform{display:none}
  .logo{display:none}
  }

@media only screen and (max-width: 768px){
.logo{width: 12%;}
  .inform{margin-left:5px;}
 
  }
  

@media only screen and (max-width: 1024px){
  .inform{margin-left:15px;}

.logo{width: 7%;}
};
@media only screen and (max-width: 1440px){
  .logo{width: 4%;}

}
@media only screen and (max-width: 2560px){

   .inform{width: 50%;}
.logo{width: 12%;}

} 
</style>