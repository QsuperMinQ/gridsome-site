<template>

    <!-- layout -->
    <div class="layout-style">

      <!-- 顶部导航 -->
      <div class="top-header">
        <!-- logo -->
        <img class="uni-logo" src="/images/universityLogo.png"/>

        <!-- 导航栏 -->
        <a-menu v-model="current" mode="horizontal">
          <a-menu-item key="home">Home </a-menu-item>
          <a-menu-item key="committee"><g-link class="nav__link" to="/journal/">Committee</g-link> </a-menu-item>
          <a-menu-item key="topic">Corence Topic </a-menu-item>
          <a-menu-item key="template">Abstract Template </a-menu-item>
          <a-sub-menu>
            <span slot="title" class="submenu-title-wrapper">History</span >
            <a-menu-item key="setting:1">
              2020
            </a-menu-item>
            <a-menu-item key="setting:2">
              2019
            </a-menu-item>
            <a-menu-item key="setting:3">
              2018
            </a-menu-item>
          </a-sub-menu>
          <a-menu-item key="contact">
            <a href="https://antdv.com" target="_blank" rel="noopener noreferrer"
              >contact</a
            >
          </a-menu-item>
        </a-menu>

      </div>

      <!-- slot -->
      <div>
        <!-- banner -->
        <a-carousel autoplay>
          <div>
            <h2 class="carousel-text">
              4th International Conference on <br>
            Advanced Materials and Engineering Applications<br>
            Sept 26-28, 2021 Handan, China 
            </h2>
            <img src="/images/banner.png" class="carousel-img"/>
          </div>
          <div>
            <img src="/images/banner.png" class="carousel-img"/>
          </div>
        </a-carousel>

        <!-- 会议介绍 -->
        <div class="introduction">

          <a-row>
            <a-col :span="13">
              
              <h3 class="title-h3">INTRODUCTION OF THE CONFERENCE</h3>
              <p class="intro-content">
                This conference will be hosted by Hebei University of Engineering (HUE), China, sponsored by Loughborough University, UK, and joinly organized by school of Mechanical and Equipment Engineering of Hebei University of Engineering, Key Laboratory of intelligent industrial equipment technology of Hebei Province and modern equipment manufacturing collaborative innovation center of Southern Hebei New Area. The main objectives are to provide a single informal platform for scholars and engineers to exchange and assimilate new research ideas and information in the field of advanced materials and their applications in engineering equipment, and to promote collaboration opportunities between individuals and research institutions. At the same time, we hope that this conference will provide more opportunities for young scholars and encourage them to make a difference in academic research. The conference will invite well-known experts at home and abroad to make online or offline reports. Both oral and poster presentations are welcome. The language of the conference is English. See the conference website for details http://icamea.hebeu.edu.cn.
              </p>
              
            </a-col>
            <a-col :span="11">
              <div class="right">
                <h3 class="title-h3">IMPORTANT DATES</h3>
                <div class="impotant-date">

                  <div class="date-item">
                    <p class="date-title">Submit the abstract of the paper</p>
                    <div>
                      <a-icon type="calendar" :style="{color: 'blue'}"/> &nbsp;July 15, 2021 
                    </div>
                    <p class="date-content">Before <span :style="{fontWeight: 700}">July 15, 2021</span>, submit the abstract of the paper.</p>
                  </div>

                  <div class="date-item">
                    <p class="date-title">The employment notice will be issued</p>
                    <div>
                    <a-icon type="calendar" :style="{color: 'blue'}"/> &nbsp;July 31, 2021
                    </div>
                    <p class="date-content">On <span :style="{fontWeight: 700}">July 31, 2021</span>, the employment notice will be issued.</p>
                  </div>

                  <div class="date-item">
                    <p class="date-title">Submit the full text of the paper</p>
                    <div>
                    <a-icon type="calendar" :style="{color: 'blue'}"/> &nbsp;August 31, 2021 
                    </div>
                    <p class="date-content">Before <span :style="{fontWeight: 700}">August 31, 2021</span>, submit the full text of the paper</p>
                  </div>

                </div>
              </div>
            </a-col>
          </a-row>

          <!-- 专家介绍 -->
          <div>
            <h3 class="title-h3">INTRODUCTION OF EXPERTS</h3>

            <div v-for="info in expertsList" :key="info.id" class="expert-introduction">
              <img class="expert-head" :src="info.pic"/>
              <div>{{info.introdution}}</div>
            </div>
          </div>

          <!-- 主办、协办、承办单位 -->

          <div>
            <h3 class="title-h3">HOST, CO-HOST, ORGANIZER</h3>
            <div v-for="info in hostList" :key="info.key" class="host">
              <p class="host-title">{{info.key}}:</p>
              <div>
                <p v-for="item in info.content" :key="item">{{item}}</p>
              </div>
            </div>
          </div>

          <!-- 地图 -->
          <h3 class="title-h3">MAP</h3>
          <div class="map"></div>
        </div>


      </div>


    </div>
</template>
<script>
export default {

  data: () => {
    return {
      current: ['home'],
      expertsList: [
        {
          id: 1,
          pic: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fpic1.zhimg.com%2F50%2Fv2-ad8b04b5093adf62ef70ec3f1e0c2abf_hd.jpg&refer=http%3A%2F%2Fpic1.zhimg.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1627461963&t=1ba73c12342c417f643e6e9ef9a4d32f',
          introdution: 'xxx, 博士学位，材料领域专家,曾获得国家级荣誉奖项，有100多项专利...'
        },
        {
          id: 2,
          pic: 'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.zcool.cn%2Fcommunity%2F010cb65e205811a80120a895cf85b3.jpg%401280w_1l_2o_100sh.jpg&refer=http%3A%2F%2Fimg.zcool.cn&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1627461964&t=005712e0590d68f6ecd46bc61634c327',
          introdution: 'xxx, 博士学位，材料领域专家'
        }
      ],
      hostList: [
        {
          key: 'HOST',
          content: ['Hebei University of Engineering']
        },
        {
          key: 'CO-HOST',
          content: ['Loughborough University']
        },
        {
          key: 'ORGANIZER',
          content: [
            'School of Mechanical and Equipment Engineering of Hebei University of Engineering',
            'Key Laboratory of intelligent industrial equipment technology of Hebei Province',
            'Modern equipment manufacturing collaborative innovation center of Southern Hebei New Area'
          ]
        },
      ]
    }
  }
}
</script>
<style scoped> 

  .layout-style {
    /* background-image: url('/images/gear.jpeg'); */
    background-repeat: no-repeat;
    background-size: 50%;
    background-position: left top;
  }

  .top-header {
    display: flex;
    padding: 20px 0;
    width: 1000px;
    margin: 0 auto;
  }

  .uni-logo {
    width: 200px;
    height: 45px;
    margin-right: 50px;
  } 

  .carousel-img {
    width: 100%;
  }

  .carousel-text {
    color: #ffffff;
    font-weight: 600;
    font-size: 20px;
    position: absolute;
    text-align: center;
    width: 100%;
    left: 0;
    top: 35px;
    font-size: 30px;
  }

  .introduction {
    width: 1000px;
    margin: 0 auto;
    padding: 50px;
  }

  .title-h3 {
    font-size: 24px;
    color: #333333;
    font-weight: 700;
  }

  .intro-content {
    color: #656565;
    font-weight: 700;
  }

  .right {
    margin-left: 30px;
    box-shadow: 0 8px 30px rgb(0 0 0 / 12%);
    padding: 15px;
  }

  .date-item {
    margin-bottom: 25px;
  }

  .date-title {
    font-size: 19px;
    color: #414042;
    margin-bottom: 10px;
  }

  .date-content {
    margin-top: 10px;
  }

  .expert-introduction {
    display: flex;
    align-items: center;
    margin: 20px 0 20px 0;
  }

  .expert-head {
    width: 50px;
    margin-right: 20px;
  }

  .host {
    display: flex;
  }

  .host-title {
    font-weight: 600;
    margin-right: 5px;
    width: 90px;
  }

  .map {
    width: 100%;
    height: 400px;
    background-image: url('http://jixie.hebeu.edu.cn/_mediafile/jixie/2019/01/17/jdrygtn627.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }

  
</style>
