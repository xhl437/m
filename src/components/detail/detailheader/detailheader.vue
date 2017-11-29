<template>
  <div class="detailheader">
    <nav>
       <span class="left"><a href="##"><img src="http://m.ujipin.com/media/images/logo_t.png" alt=""></a></span>
       <div class="right">
           <a href="###" @click="isShow=!isShow"> <span class="icon icon-search"></span></a>
           <a href="/mine">
              <span class="icon icon-friends"></span>
           </a>
           <a href="javascript;;"> <span class="icon icon-gift"></span></a>

       </div>
    </nav>
    <div v-if="isShow">
                <div class="search-input">
                  <label class="icon icon-search" for="search"></label>
                  <input type="search" id='search' placeholder='输入关键字...'/>
                </div>
                <ul>
                    <li>111</li>
                    <li>222</li>
                    <li>333</li>
                    <li>444</li>
                    <li>555</li>
                </ul>
      </div>
</div>
      
    </div>
  </div>
</template>

<script>

export default {
  name: 'detailheader',
  data () {
    return {
        isShow:false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.detailheader{
    display: block;
    width: 100%;
    height:56px;
    background: #31313C;
    padding-left: 16px;
    position: fixed;
    left: 0;
    box-sizing: border-box;
    z-index: 10;
}
nav{
  
  height: 100%;
  display: flex;
  justify-content: space-between;
}

.left{
    float: left;
    width: 20%;
    height: 20px;
    color: #fff;
    display:block;
    margin-top: 20px;
}
a,img{display: block}
img{width: 100%;height: 100%}
.right{

  width: 40%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.right span{
  display:inline-block;
    width: 46px;
    height: 56px;
    text-align: center;
    margin-right: 10px;
}
.icon{
  font-size:24px;
  color: #fff;
}
#search{
  height: 40px;
}
ul{
  width: 100%;
  background: #fff;
}
ul li{
  padding: 8px 0px;
  font-size: 18px;
}



</style>