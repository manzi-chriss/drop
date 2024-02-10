<template>
    <div class="top-bar">
        <div class="logo"><p>LOGO</p></div>
 <div class="all">
    <div class="home"><router-link to="/">Home</router-link></div>
    <div class="home"><router-link to="/Hello">About us</router-link></div>
    <div class="home"><router-link to="/">Contact</router-link></div>
</div>
    </div>
</template>

<script>
export default {
    name: 'TopBar'
};
</script>

<style scoped>

.top-bar {
    background-color:none;
    padding: 0px ;
    display: flex;
    margin-left:-auto ;
    margin-top:  -200px; 
    border-radius: 10px;
    width: 90vw;
    height: 50px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.9); 
   
}
.home{
    margin: 3px;
    color: beige;
    padding-left:100px ;    
}
.home:hover{
    margin: 6px;
    color: beige;
    padding-left:100px ;
    margin-bottom: 20px;    
}
.logo{
    margin: 10px;
}
.all{
    margin-left:50%;
    display: flex;
}
</style>
