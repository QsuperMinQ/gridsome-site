<template>
  <Layout>

    <div class="container">
      <div class="hero">
        <h1 class="hero-title">Simplicity. Aesthetics. Value.</h1>
        <div class="hero-content">
          Hi there, I'm an independent Digital Designer & Art Director focused on digital design for brands that like to have fun.
        </div>
      </div>

      <div class="contents">
       
        <div class="item" v-for="info in list" :key="info.id">
          <g-image class="image" alt="Example image" v-bind:src="info.url" />
          <h3 class="item-title">{{info.title}}</h3>
          <p class="item-color">{{info.color}}!</p>
        </div>
      </div>

      <div class="bottom-items">
        <div class="bottom-content">
          <div class="bottom-item">Gridsome with Forestry CMS</div>
          <div class="bottom-item">VueJS for your next project</div>
          <div class="bottom-item">macOS development environment</div>
          <div class="bottom-item">About Typography</div>
        </div>
      </div>
      
    </div>
    

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  },
  data: () => {
    return {
      list: [
        {id: 1, title: 'Apple', color: 'Green', url: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Ffiles.jb51.net%2Ffile_images%2Fphotoshop%2F201707%2F2017073115021827.jpg&refer=http%3A%2F%2Ffiles.jb51.net&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1627036719&t=6512b166af933599d6f1093087ff982b'},
        {id: 2, title: 'Lemon', color: 'Yellow', url: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fwww.dabaoku.com%2Fsucai%2Fzhiwulei%2Fshucai%2F0024.jpg&refer=http%3A%2F%2Fwww.dabaoku.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1627035901&t=9da6699f78902b0c50cbff9dabf12370'},
        {id: 3, title: 'Weather', color: 'Green', url: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201508%2F22%2F20150822112132_Q3NUM.thumb.400_0.jpeg&refer=http%3A%2F%2Fb-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1627036152&t=f9958da1db7abf1b7977217fa81e4cbc'},
        {id: 4, title: 'Love', color: 'Black', url: 'https://img1.baidu.com/it/u=2679562381,868418241&fm=26&fmt=auto&gp=0.jpg'},
      ]
    }
  }
}


</script>

<style>

.hero {
  width: 480px;
  max-width: 100%;
  margin: 0 auto;
  padding: 4rem 0 8rem;
}

.hero-title {
  font-size: 3rem;
  font-weight: 700;
  text-align: center;
  letter-spacing: -.01em;
  margin: 0 0 2rem;
}

.hero-content {
  font-size: 1.15rem;
  color: #787878;
  text-align: center;
}

.contents {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 4rem;
  box-sizing: border-box;
}

.item {
  text-align: center;
}

@media (min-width: 920px) {
  .item:nth-child(3n+1){
    grid-column: auto/span 2;
  }
}

@media (max-width: 920px) {
  .item{
    grid-column: auto/span 2;
  }
}



.item-title {
  font-size: 1rem;
  margin: 2rem 0 1rem;  
}

.item-color {
  margin-right: .8rem;  
}

.image {
  width: 100%;
  height: 560px;
  object-fit: cover;
}

.bottom-items {
  border-top: 1px solid #999999;
  border-bottom: 1px solid #999999;
  width: 100%;
}

.bottom-content {
  display: flex;
  flex-wrap: wrap;
}

.bottom-item {
  border-right: 1px solid #999999;
  padding: 2rem;
  box-sizing: border-box;
}


.bottom-item:nth-child(4) {
  border-right: 0px solid #999999;
}

@media (min-width: 920px){
  .bottom-item {
    flex: 0 0 25%;
  }
}

@media ( max-width: 920px ) {
  .bottom-item {
    flex: 0 0 50%;
  }


  .bottom-item:nth-child(1) {
    border-bottom: 1px solid #999999;
  }

  .bottom-item:nth-child(2) {
    border-bottom: 1px solid #999999;
    border-right: 0px solid #999999;
  }
}

</style>
