<template lang="html">
  <aside class="sidebar" v-show="show" v-bind:class="{slide: slide}">
    <div class="sidebarHeader">
      <div class="sidebarLogo">
      <a href=""><img src="@/assets/logo big.png" alt="logo"></a> 
       <h1>Mooogle </h1>
    </div>
    </div>
    <div class="menyWrap">
        <ul class="meny">
          <li><a href=""><img class="icon" src="@/assets/icon11.png" alt="logo"> <h3 class="category">Фильмы</h3></a>
            <ul>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
            </ul><br/><br/>
          </li>
            
          <li><a href=""><img class="icon" src="@/assets/icon2.png" alt="logo"><h3 class="category">Сериалы</h3></a>
            <ul>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
              <li class="subcategory"><a href=""><h4>Подкатегория</h4></a></li>
            </ul><br/><br/><br/>
          </li>     
          <li><a href=""><img class="icon" src="@/assets/icon3.png" alt="logo"><h3 class="category">Избранное</h3></a></li>
        </ul>  
    </div></aside>
  
</template>

<script>

export default {
  name: 'Sidebar',
  data() {
    return {
      //show: false,
      slide: true
    }
  }
}
</script>

<style lang="css">
  .sidebar {
    background-color: #fff;
    width: 300px;
    position: fixed;
    top: 0;
    left: 0;
    bottom: 0;
    z-index: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    box-shadow:  12px 0px 22px rgba(0,0,0,0.23);
  }

  .sidebarHeader{
    background-color: #77c1bb;
    width: 300px;
    height: 144px;
    margin-top: -343px;
    position: absolute
  }

  .meny{
     margin-top: -132px;
  }

  .sidebarLogo{
    margin-top: 24px;
    margin-left: 38px;
    
  }

  .sidebarLogo h1{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: 20px;
  }
  
  .slide-transition {
    transition: all 1.s cubic-bezier(.65, .05, .36, 1);
  }

  .slide-enter, .slide-leave {
    left: -100%;
  }

  .icon{
    margin-left: -47px;
    margin-right: 30px;
  }
  .subcategory{
    margin-left: 28px;
    margin-bottom: 7px;
  }
 
 .category{
   margin-bottom: 15px;
   margin-top: -18px;
 }
  .subcategory a h4{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: 10px;
    color: #372c48;
  }

  .meny>li a h3{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: 13px;
    color: #372c48;
  }

  .subcategory a:hover h4{
     color: #77c1bb;
  }

  .meny>li a:hover h3{
    color: #77c1bb;
  }
  
</style>
