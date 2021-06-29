<template>
  <Layout>
    <div class="journal-container">
      <div class="journal-header">
        a wise person once said...
      </div>
      <div class="journal-positon">
        <div v-for="info in list" :key="info.id" class="journal-bg">
          <div class="journal-item">
            <h2 class="journal-title">{{info.title}}</h2>
            <p class="journal-content">{{info.content}}</p>
          </div>
        </div>
      </div>

    </div>

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Journal page'
  },
  data: () => {
    return {
      list: [
        { id: 1, title: 'Gridsome with Forestry CMS', content: 'Get up and running with Forestry CMS, a git-backed headless CMS with a slick editing interface.'},
        { id: 2, title: 'VueJS for your next project', content: 'Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces.'},
        { id: 3, title: 'macOS development environment', content: 'Get up and running with a fresh macOS Catalina install'},
        { id: 4, title: 'About Typography', content: 'Font face, vertical rythm, readability, this long fake text should flow.'},
      ]
    }
  }
}
</script>
<style>
  * {
    box-sizing: border-box;
  }

  .journal-container {
    min-height: calc(100vh - 13rem - 120px);
  }

  .journal-header {
    box-sizing: border-box;
    padding: 4rem 6rem;
    margin: 0;
    color: #eeeeee;
    font-size: 3rem;
    font-weight: 700;
  }

  .journal-positon {
    position: relative;
  }

  .journal-bg {
    transition: all .5s ease; 
    width: 100vw;
  }

  @media (max-width: 1200px) {
    .journal-bg {
      margin-left: -6rem;
      padding: 5rem 12rem;
    }
  }

  @media (min-width: 1200px) {
    .journal-bg {
      margin-left: calc((1200px - 12rem - 100vw)/2);
      padding: 5rem calc(100vw - 1200px);
    }
  }

  .journal-bg:hover{
    background-color: #f3f3f3;
  }

  .journal-bg:hover>.journal-item {
    transform: translateX(3rem);
  }

  .journal-item {
    box-sizing: border-box;
    transition: transform .5s ease;    
  }

  .journal-title{
    color: #000000;
    font-size: 2rem;
    margin: 0;
  }

  .journal-content {
    font-size: 1.15rem;
    line-height: 1.15;
  }
</style>
