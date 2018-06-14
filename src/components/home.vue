<template>
  <div class="home" ref="content">

     <b-navbar toggleable="md" type="dark" fixed="top" class="home_nav">
        
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="#" class="logo"></b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto" v-b-scrollspy:nav-scroller>
            <b-navbar-nav class="nav_link">
              <b-nav-item href="#home" @click="scrollIntoView" class="no">首页</b-nav-item>
              <b-nav-item href="#about" @click="scrollIntoView" >关于我们</b-nav-item>
              <b-nav-item href="#develop" @click="scrollIntoView" >集团发展</b-nav-item>
              <b-nav-item href="#bussiness" @click="scrollIntoView" >商业版图</b-nav-item>
              <b-nav-item href="#investment" @click="scrollIntoView" >投资理念</b-nav-item>
              <b-nav-item href="#join" @click="scrollIntoView" >加入我们</b-nav-item>
            </b-navbar-nav>
          </b-navbar-nav>

        </b-collapse>

    </b-navbar>

    <div id="nav-scroller"  class="scroll_body" >
      <div class="first_scrren">
      
        <div class="first_screen_text" id="home">
          <p>全球顶级</p>
          <h3>资产管理 和 区块链投资服务企业</h3>        
        </div>

        <div class="about" id="about">
          <p class="about_tit">关于我们</p>
          <p class="about_en">ABOUT US</p>
          <p class="about_intr">科银资本是一家具备澳洲劝他金融服务执照<br>专业于区块链基础建设、数字货币投资与咨询的公司</p>
          <p class="about_intr_small">科银资本是一家具备<br>澳洲劝他金融服务执照专业于<br>区块链基础建设、数字货币投资与咨询的公司</p>
          
          <ul class="about_power_list">
            <li v-on:mouseenter="isShowOne = true" v-on:mouseleave="isShowOne = false">
              <div class="about_team">

                <transition name="team" mode="out-in"
                  enter-active-class="animated pulse"
                  >
                    <div v-if="!isShowOne" key="defult">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">LOCATION</p>                 
                    </div>
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">XXXXXXX</p>                 
                    </div>
                </transition>
              </div>
            </li>

            <li v-on:mouseenter="isShowPower = true" v-on:mouseleave="isShowPower = false">
              <div class="about_power">
                <transition name="power" mode="out-in"
                  enter-active-class="animated pulse"
                  >
                    <div v-if="!isShowPower" key="defult">
                      <p class="about_list_tit">实力</p>
                      <p class="about_list_dis">POWER</p>                 
                    </div>
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">XXXXXXX</p>                 
                    </div>
                </transition>
              </div>
            </li>

            <li v-on:mouseenter="isShowLayout = true" v-on:mouseleave="isShowLayout = false">
              <div class="about_layout">
                <transition name="fade" mode="out-in"
                    enter-active-class="animated pulse"
                  >
                    <div v-if="!isShowLayout" key="defult">
                      <p class="about_list_tit">布局</p>
                      <p class="about_list_dis">GRRAGEMENT</p>                 
                    </div>  
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">XXXXXXX</p>                 
                  </div>
                </transition>

                <transition name="powerA"
                  enter-class="animated bounce"
                  enter-active-class="animated pulse"
                  
                  >
                  
                </transition>
              </div>
            </li>
          </ul>

          <ul class="about_power_s_list">
            <li class="about_list_s_team">
              <p class="about_list_s_tit">团队</p>
              <p class="about_list_s_txt">立足世界的区块链先驱实践企业</p>
            </li>
            <li class="about_list_s_power">
              <p class="about_list_s_tit">实力</p>
              <p class="about_list_s_txt">澳大利亚唯一一家具有<br>区块链数字货币风投牌照的投资公司</p>
            </li>
            <li class="about_list_s_layout">
              <p class="about_list_s_tit">布局</p>
              <p class="about_list_s_txt">澳大利亚唯一一家具有<br>区块链数字货币风投牌照的投资公司</p>
            </li>
          </ul>
        </div>
      </div>
      <div class="develop" id="develop">
        <p class="about_tit develop_tit">集团发展</p>
        <p class="about_en">DEVELOPMENT</p>

        <div class="develop_s_img"><img src="../assest/develop.jpg" /></div>

        <div class="develop_s_list">
          <ul class="develp_wrapper">
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>            
            <li class="develop_s_right">
              <p class="develop_year develop_s_year">2015</p>
              <p>1月：科银资本在澳大利亚成立</p>
              <p>2月：科银资本投资入股澳大利亚Blockchain Global</p>
            </li>
          </ul>

          <ul class="develp_wrapper">
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>            
            <li class="develop_s_right">
              <p class="develop_year develop_s_year">2016</p>
              <p>3月：与算力吧PoW8挖矿云平台达成深度合作</p>
              <p>3月：成立武汉链芯区块链技术有限公司，专注芯片生产与研发</p>
            </li>
          </ul>

          <ul class="develp_wrapper">
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>            
            <li class="develop_s_right">
              <p class="develop_year develop_s_year">2017</p>
              <p>5月：入股澳大利亚DigitalX区块链咨询服务公司</p>
              <p>6月：成立上海阔悦科技公司，专注于区块链技术及应用解决方案</p>
            </li>
          </ul>

          <b-collapse id="sDevelop" v-model="sDevelopIsShow">
            <ul class="develp_wrapper">
              <li class="develop_mid">
                <span class="develop_circle"></span>
              </li>            
              <li class="develop_s_right">
                <p class="develop_year develop_s_year">2018</p>
                <p>1月：入股澳洲数字货币交易所Claudex</p>
                <p>2月：科银资本旗下Fintech Review数字传媒公司成立 ，致力于打造区块链媒体行业标杆</p>
              </li>
            </ul>
          </b-collapse>

          <div class="develop_s_more m-1" 
              @click="sDevelopIsShow = !sDevelopIsShow"
              aria-controls="sDevelop"
              :aria-expanded="sDevelopIsShow ? 'true' : 'false'">
              <div v-if="!sDevelopIsShow">
                <p >展开全部</p> 
                <!-- <p v-else>向上收起</p>  -->
                <p class="develop_s_more_icon"></p>
              </div>

              <div v-if="sDevelopIsShow">
                <p class="develop_s_more_icon rotaAll"></p>
                <p >向上收起</p> 
              </div>
          </div>

        </div>

        <div class="develop_list">
          <ul class="develp_wrapper">
            <li class="develop_year">2015</li>
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>
            <li class="develop_dis padBtm40">
              <p>2015.01：科银资本在澳大利亚成立</p>
              <p>2015.03： 科银资本投资入股澳大利亚Blockchain Global</p>
            </li>
          </ul>
          <ul class="develp_wrapper">
            <li class="develop_year">2016</li>
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>
            <li class="develop_dis padBtm40">
              <p>2016.03：与算力吧PoW8挖矿云平台达成深度合作</p>
              <p>2016.03： 成立武汉链芯区块链技术有限公司，专注芯片生产与研发</p>
            </li>
          </ul>
          <ul class="develp_wrapper">
            <li class="develop_year">2017</li>
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>
            <li class="develop_dis padBtm40">
              <p>2017.05：入股澳大利亚DigitalX区块链咨询服务公司</p>
              <p>2017.06：成立上海阔悦科技公司，专注于区块链技术及应用解决方案</p>

              <b-collapse id="develop" v-model="developIsShow">
                <p>XXXXXX</p>
              </b-collapse>

              <div class="develop_s_more m-1" 
                 @click="developIsShow = !developIsShow"
                 aria-controls="develop"
                 :aria-expanded="developIsShow ? 'true' : 'false'">
                 <span v-if="!developIsShow" class="develop_more">展开全部</span>
                 
                 <span v-else class="develop_more">收起</span>
              </div>
             
            </li>
          </ul>
          <ul class="develp_wrapper">
            <li class="develop_year">2018</li>
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>
            <li class="develop_dis">
              <p>2018.01：入股澳洲数字货币交易所Claudex</p>
              <p>2018.02：科银资本旗下Fintech Review数字传媒公司成立 ，致力于打造区块链媒体行业标杆</p>
              
              <b-collapse id="develop2" v-model="developIsShow2">
                <p>XXXXXX</p>
              </b-collapse>

              <div class="develop_s_more m-1" 
                 @click="developIsShow2 = !developIsShow2"
                 aria-controls="develop2"
                 :aria-expanded="developIsShow2 ? 'true' : 'false'">
                 <span v-if="!developIsShow2" class="develop_more">展开全部</span>
                 
                 <span v-else class="develop_more">收起</span>
              </div>
            </li>
          </ul>
        </div>

        <div class="develop_img"><img src="../assest/develop.jpg" /></div>
      </div>

      <div class="map_bg" id="bussiness">
        <div class="business">
          <div class="business_s_top">
            <p class="about_tit develop_tit">商业版图</p>
            <p class="about_en">BUSSINESS MAP</p>
            <p class="business_dis">遍布全球 6个国家 15个城市 12个t区块链细分行业<br>包括芯片、整机、矿场、矿池、交易所、钱包、借贷、媒体、评级    IM流量入口、合规公募平台、底层链</p>
            <p class="business_s_dis">遍布全球 6个国家 15个城市 <br> 12个t区块链细分行业<br>包括芯片、整机、矿场、矿池、交易所<br>钱包、借贷、媒体、评级    IM流量入口<br>合规公募平台、底层链</p>            
          </div>

          <div class="business_s_box">
            <ul class="business_s_logo">
              <li class="business_band_zb"></li>
              <li class="business_band_biyin"></li>
              <li class="business_band_leek"></li>
              <li class="business_band_suanliba"></li>
              <li class="business_band_xianggang"></li>
              <li class="business_band_shanghai"></li>
              <li class="business_band_biwang"></li>
              <li class="business_band_hyper"></li>
              <li class="business_band_hcash"></li>
            </ul>
            
            <b-collapse id="sbuniess" v-model="sbuniessIsShow">
              <ul class="business_s_logo business_s_logo2">
                <li class="business_band_suanli"></li>
                <li class="business_band_qtum"></li>
                <li class="business_band_qiedalu"></li>
                <li class="business_band_name"></li>
                <li class="business_band_jnb"></li>
                <li class="business_band_hps"></li>
                <li class="business_band_hbi"></li>
                <li class="business_band_dprating"></li>
                <li class="business_band_coin"></li>
                <li class="business_band_clouddex"></li>
                <li class="business_band_bitbank"></li>
                <li class="business_band_batpool"></li>
              </ul>
            </b-collapse>
            

            <div class="develop_s_more m-1" 
              @click="sbuniessIsShow = !sbuniessIsShow"
              aria-controls="sbuniess"
              :aria-expanded="sbuniessIsShow ? 'true' : 'false'">
              <div v-if="!sbuniessIsShow">
                <p >查看更多</p> 
                <p class="develop_s_more_icon"></p>
              </div>

              <div v-if="sbuniessIsShow">
                <p class="develop_s_more_icon rotaAll"></p>
                <p >向上收起</p> 
              </div>
            </div>
            
          </div>

         
          <ul class="business_logo">
            <li class="business_band_zb"></li>
            <li class="business_band_biyin"></li>
            <li class="business_band_leek"></li>
            <li class="business_band_suanliba"></li>
            <li class="business_band_xianggang"></li>
            <li class="business_band_shanghai"></li>
            <li class="business_band_biwang"></li>
            <li class="business_band_hyper"></li>
            <li class="business_band_hcash"></li>
            <li class="business_band_suanli"></li>
          </ul>

          <b-collapse id="moreLogo" v-model="isMoreLogo">
            <ul class="business_logo">
              <li class="business_band_qtum"></li>
              <li class="business_band_qiedalu"></li>
              <li class="business_band_name"></li>
              <li class="business_band_jnb"></li>
              <li class="business_band_hps"></li>
              <li class="business_band_hbi"></li>
              <li class="business_band_dprating"></li>
              <li class="business_band_coin"></li>
              <li class="business_band_clouddex"></li>
              <li class="business_band_bitbank"></li>
              <li class="business_band_batpool"></li>
            </ul>
          </b-collapse>

          <div class="business_more" 
              @click="isMoreLogo = !isMoreLogo"
              aria-controls="moreLogo"
              :aria-expanded="isMoreLogo ? 'true' : 'false'">
              <div v-if="!isMoreLogo">
                <p >查看更多</p> 
                <span class="more_logo_icon"></span>
              </div>

              <div v-if="isMoreLogo">
                <span class="more_logo_icon rotaAll"></span>
                <p >向上收起</p> 
              </div>
            </div>
        </div>

        <div class="investment" id="investment">
          <p class="about_tit develop_tit">投资理念和哲学</p>
          <p class="about_en">INVESTMENT PHILOSOPHY</p>

          <ul class="investment_list">
            <li>
              <p class="investment_bg investment_pre"></p>
              <p class="investment_text">前瞻市场</p>
            </li>
            <li>
              <p class="investment_bg investment_enter"></p>
              <p class="investment_text">早期进入</p>
            </li>
            <li>
              <p class="investment_bg investment_layout"></p>
              <p class="investment_text">全生态布局</p>
            </li>
          </ul>
        </div>        
      </div>


      <div class="join" id="join">
        <p class="about_tit">加入我们</p>
        <p class="about_en join_en">JOIN IN US</p>

        <p class="join_invent">招聘/商务：offical@collinstar.com.cn</p>
        <p class="join_bold">信仰&nbsp&nbsp坚持&nbsp&nbsp专注&nbsp&nbsp专业</p>
      </div>
   </div>
      <footer class="footer">
        <div class="clear">
          <span class="left">Terms and Conditions Privacy Policy</span>
          <span class="right">© 2014-2015 by Collinstar Capital Pty Ltd. All Rights Reserved. Designed by Legend Web Design.</span>          
        </div>
      </footer>
  </div>


  
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      isShowOne: false,
      isShowPower: false,
      isShowLayout: false,
      developIsShow: false,
      developIsShow2: false,
      isMoreLogo: false,
      sDevelopIsShow: false,
      sbuniessIsShow: false,
      
    }
  },
  mounted () {
  },
  transitions: {
    bounce: {
      enterClass: 'bounceInLeft',
      leaveClass: 'bounceOutRight'
    }
  },

  methods: {
    mouseover: (index) => {
      this.isShowOne = !this.isShowOne;
    },
    showMore: (type) => {
      this[type] = !this[type];
    },
    scrollIntoView (evt) {
      evt.preventDefault()
      const href = evt.target.getAttribute('href')
      const el = href ? document.querySelector(href) : null
      if (el) {
        console.log(window.navigator.userAgent);
        let u = window.navigator.userAgent;
        if (!!u.match(/AppleWebKit.*Mobile.*/)||!!u.match(/AppleWebKit/)) {
          document.body.scrollTop = el.offsetTop + 40;
          document.documentElement.scrollTop = el.offsetTop + 40;
        } else {
          document.body.scrollTop = el.offsetTop - 50;
          document.documentElement.scrollTop = el.offsetTop - 50;
        }
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  @import '../styles/home.scss';
  @import '../styles/media.scss';
  
  

</style>
