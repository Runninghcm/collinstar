<template>
  <div class="home" ref="content">

     <b-navbar toggleable="md" type="dark" fixed="top" class="home_nav">
        
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="#home" @click="scrollIntoView" class="logo"></b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto" v-b-scrollspy:nav-scroller>
            <b-navbar-nav class="nav_link">
              <b-nav-item href="#home" @click="scrollIntoView" class="no">首页</b-nav-item>
              <b-nav-item href="#about" @click="scrollIntoView" >关于我们</b-nav-item>
              <b-nav-item href="#develop" @click="scrollIntoView" >集团发展</b-nav-item>
              <b-nav-item href="#bussiness" @click="scrollIntoView" >投资布局</b-nav-item>
              <b-nav-item href="#investment" @click="scrollIntoView" >投资理念</b-nav-item>
              <b-nav-item href="#join" @click="scrollIntoView" >加入我们</b-nav-item>
            </b-navbar-nav>
          </b-navbar-nav>

        </b-collapse>

    </b-navbar>

    <div class="scroll_body" >
      <div class="first_scrren">
      
        <div class="first_screen_text " id="home">
          <div class="homeTit animated zoomIn">
            <p>科银资本</p>
            <h3>遍布全球6个国家、15个城市、布局12个区块链细分行业</h3>       
          </div>

        </div>

        <div class="about" id="about">
          <div class="model_tit">
            <p class="about_tit">关于我们</p>
            <p class="about_en">About us</p>
          </div>
          
          <p class="side_text about_intr">科银资本是一家具备澳洲全套金融服务执照<br>专业于区块链基础建设、数字货币投资与咨询的资产管理公司</p>
          <p class="side_text about_intr_small">科银资本是一家具备澳洲全套金融服务执照<br>专业于区块链基础建设、数字货币投资与咨询的资产管理公司</p>
          
          <ul class="about_power_list">
            <li v-on:mouseenter="isShowOne = true" v-on:mouseleave="isShowOne = false">
              <div class="about_team">

                <transition name="team" mode="out-in"
                  enter-active-class="animated pulse"
                  >
                    <div v-if="!isShowOne" key="defult">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">Team</p>                 
                    </div>
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">团队</p>
                      <p class="about_list_dis">以跨行业、高学历、多文化背景的团队为支撑的世界级区块链先驱企业</p>                 
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
                      <p class="about_list_dis">Power</p>                 
                    </div>
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">实力</p>
                      <p class="about_list_dis">澳大利亚唯一一家具有区块链数字货币风投牌照的投资公司</p>                 
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
                      <p class="about_list_dis">Business</p>                 
                    </div>  
                    <div v-else class="power_active" key="active">
                      <p class="about_list_tit">布局</p>
                      <p class="about_list_dis">遍布全球6个国家、15个城市、12个细分行业的区块链全产业布局</p>                 
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
              <p class="about_list_s_txt">以跨行业、高学历、多文化<br>背景的团队为支撑的世界级区块链先驱企业</p>
            </li>
            <li class="about_list_s_power">
              <p class="about_list_s_tit">实力</p>
              <p class="about_list_s_txt">澳大利亚唯一一家具有<br>区块链数字货币风投牌照的投资公司</p>
            </li>
            <li class="about_list_s_layout">
              <p class="about_list_s_tit">布局</p>
              <p class="about_list_s_txt">遍布全球6个国家、15个城市<br>12个细分行业的区块链全产业布局</p>
            </li>
          </ul>
        </div>
      </div>
      <div class="develop" id="develop">
        <div class="model_tit">
          <p class="about_tit develop_tit">集团发展</p>
          <p class="about_en">Development</p>
        </div>

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
              
                <b-collapse id="sdevelop3" v-model="phoneDevelopIsShow2">
                  <div>
                    <p>2017.07：成立Leekico众筹平台，开展区块链众筹与孵化业务</p>
                    <p>2017.08：与Legend Digital神话科技数字传媒公司达成战略合作</p>
                    <p>2017.09：入股币安(Binance)数字货币交易所 </p>
                    <p>2017.10：收购澳大利亚Hatchstone legal法务咨询公司 </p>
                    <p>2017.10：与Chain of Home、Olympus Labs等众多行业领先者达成战略合作关系 </p>
                    <p>2017.10：投资新疆芯谷云创区块链产业园 </p>
                    <p>2017.11：收购币网（BW集团），开展挖矿业务</p>
                    <p>2017.11：科银资本蒙纳士大学联合实验室成立</p>
                    <p>2017.11： 科银资本旗下HyperPay 项目启动，旨于开通数字货币在各领域的支付通道</p>
                    <p>2017.12：科银资本旗下Blockchain Ventures基金启动，启动加密货币与数字资产基金投资业务</p>          
                  </div>
                </b-collapse>
                <div class="develop_s_more m-1" 
                    @click="phoneDevelopIsShow2 = !phoneDevelopIsShow2"
                    aria-controls="sdevelop3"
                    :aria-expanded="phoneDevelopIsShow2 ? 'true' : 'false'">
                    <p v-if="!phoneDevelopIsShow2">查看更多</p>
                    <p v-else>向上收起</p>
                </div>  
              </li>
          </ul>

          <ul class="develp_wrapper">
            <li class="develop_mid">
              <span class="develop_circle"></span>
            </li>            
            <li class="develop_s_right">
              <p class="develop_year develop_s_year">2018</p>
              <p>1月：入股澳洲数字货币交易所Claudex</p>
              <p>2月：科银资本旗下Fintech Review数字传媒公司成立 ，致力于打造区块链媒体行业标杆</p>

              <b-collapse id="sDevelop1" v-model="phoneDevelopIsShow">
                <div>
                  <p>2018.03：联合成立EOS超级节点WhatEOS </p>
                  <p>2018.04：科银资本香港理工大学联合实验室开幕</p>
                  <p>2018.05：科银资本入驻火币超级节点 </p>
                  <p>2018.06：收购CoinW数字货币交易所 </p>
                  <p>2018.07：成立科银资本韩国办事处，完善科银资本韩国布局</p>                  
                </div>
              </b-collapse>

              <div class="develop_s_more m-1" 
                @click="phoneDevelopIsShow = !phoneDevelopIsShow"
                aria-controls="sDevelop1"
                :aria-expanded="phoneDevelopIsShow ? 'true' : 'false'">
                <p v-if="!phoneDevelopIsShow">查看更多</p> 
                <p v-else>向上收起</p> 
              </div>
            </li>
          </ul>

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
                <p>2017.07：成立Leekico众筹平台，开展区块链众筹与孵化业务</p>
                <p>2017.08：与Legend Digital神话科技数字传媒公司达成战略合作</p>
                <p>2017.09：入股币安(Binance)数字货币交易所 </p>
                <p>2017.10：收购澳大利亚Hatchstone legal法务咨询公司 </p>
                <p>2017.10：与Chain of Home、Olympus Labs等众多行业领先者达成战略合作关系 </p>
                <p>2017.10：投资新疆芯谷云创区块链产业园 </p>
                <p>2017.11：收购币网（BW集团），开展挖矿业务</p>
                <p>2017.11：科银资本蒙纳士大学联合实验室成立</p>
                <p>2017.11：科银资本旗下HyperPay 项目启动，旨于开通数字货币在各领域的支付通道</p>
                <p>2017.12：科银资本旗下Blockchain Ventures基金启动，启动加密货币与数字资产基金投资业务</p>
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
                <p>2018.03：联合成立EOS超级节点WhatEOS </p>
                <p>2018.04：科银资本香港理工大学联合实验室开幕 </p>
                <p>2018.05：科银资本入驻火币超级节点 </p>
                <p>2018.06：收购CoinW数字货币交易所 </p>
                <p>2018.07：成立科银资本韩国办事处，完善科银资本韩国布局</p>
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

        <!-- <div class="develop_img"><img src="../assest/develop.jpg" /></div> -->
      </div>

      <div class="map_bg" id="bussiness">
        <div class="business">
          <div class="business_s_top">

            <div class="model_tit">
              <p class="about_tit develop_tit">投资布局</p>
              <p class="about_en">Business map</p>
            </div>

            <p class="side_text business_dis">遍布全球6个国家，15个城市，12个区块链细分行业。<br>包括芯片整机、矿池、算力平台、钱包、交易所、ICO平台、基金、媒体、市值管理、区块链实验室等</p>
            <p class="side_text business_s_dis">遍布全球6个国家，15个城市，<br>12个区块链细分行业。包括芯片整机<br>矿池、算力平台、钱包、交易所ICO平台<br>基金、媒体、市值管理、区块链实验室等</p>            
          </div>

          <div class="business_s_box">
            <ul class="business_s_logo">
              <li class="business_band_1"></li>
              <li class="business_band_2"></li>
              <li class="business_band_3"></li>
              <li class="business_band_4"></li>
              <li class="business_band_5"></li>
              <li class="business_band_6"></li>
              <li class="business_band_7"></li>
              <li class="business_band_8"></li>
              <li class="business_band_9"></li>
            </ul>
            
            <b-collapse id="sbuniess" v-model="sbuniessIsShow">
              <ul class="business_s_logo business_s_logo2">
                <li class="business_band_10"></li>
                <li class="business_band_11"></li>
                <li class="business_band_12"></li>
                <li class="business_band_13"></li>
                <li class="business_band_14"></li>
                <li class="business_band_15"></li>
                <li class="business_band_16"></li>
                <li class="business_band_17"></li>
                <li class="business_band_18"></li>
                <li class="business_band_19"></li>
                <li class="business_band_20"></li>
                <li class="business_band_21"></li>
                <li class="business_band_22"></li>
                <li class="business_band_23"></li>
                <li class="business_band_24"></li>
                <li class="business_band_25"></li>
                <li class="business_band_26"></li>
                <li class="business_band_27"></li>
                <li class="business_band_28"></li>
                <li class="business_band_29"></li>
                <li class="business_band_30"></li>
                <li class="business_band_31"></li>
                <li class="business_band_32"></li>
                <li class="business_band_33"></li>
                <li class="business_band_34"></li>
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
            <li class="business_band_1"></li>
            <li class="business_band_2"></li>
            <li class="business_band_3"></li>
            <li class="business_band_4"></li>
            <li class="business_band_5"></li>
            <li class="business_band_6"></li>
            <li class="business_band_7"></li>
            <li class="business_band_8"></li>
            <li class="business_band_9"></li>
            <li class="business_band_10"></li>
            <li class="business_band_11"></li>
            <li class="business_band_12"></li>
            <li class="business_band_13"></li>
            <li class="business_band_14"></li>
            <li class="business_band_15"></li>
            <li class="business_band_16"></li>
            <li class="business_band_17"></li>
            <li class="business_band_18"></li>
            <li class="business_band_19"></li>
            <li class="business_band_20"></li>
            <li class="business_band_21"></li>
            <li class="business_band_22"></li>
            <li class="business_band_23"></li>
            <li class="business_band_24"></li>
            <li class="business_band_25"></li>
            <li class="business_band_26"></li>
            <li class="business_band_27"></li>
            <li class="business_band_28"></li>
            <li class="business_band_29"></li>
            <li class="business_band_30"></li>
            <li class="business_band_31"></li>
            <li class="business_band_32"></li>
            <li class="business_band_33"></li>
            <li class="business_band_34"></li>
          </ul>
        </div> 

        
        <div class="investment" id="investment">
          <div class="model_tit">
            <p class="about_tit develop_tit">投资理念和哲学</p>
            <p class="about_en">Investment philosophy</p>
          </div>

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
        <div class="model_tit">
          <p class="about_tit">加入我们</p>
          <p class="about_en join_en">Join us</p>
        </div>
        <p class="join_bold">信仰&nbsp&nbsp坚持&nbsp&nbsp专注&nbsp&nbsp专业</p>
        <p class="join_invent">招聘：hr@collinstar.com.cn
          <!-- <br>商务：fiona@collinstar.com.cn -->
        </p>
        
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
      sbuniessIsShow: false,
      phoneDevelopIsShow: false,
      phoneDevelopIsShow2: false,
    }
  },
  mounted () {
    const el = document.querySelector('#home');
    const homeTit = el.querySelector('.homeTit');
    const me = this;
    setTimeout(function() {
      me.removeClass(homeTit, ' animated zoomIn');
    }, 1000);
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
    addClass: (obj, cls) => {
      if (obj) {
        var obj_class = obj.className,//获取 class 内容.
        blank = (obj_class != '') ? ' ' : '',//判断获取到的 class 是否为空, 如果不为空在前面加个'空格'.
        added = obj_class + blank + cls;//组合原来的 class 和需要添加的 class.
        obj.className = added;//替换原来的 class.
      }
    },
    removeClass: (obj, cls) => {
      if (obj) {
        var obj_class = obj.className,//获取 class 内容.
        isMatch = obj_class.search(cls);
        console.log(isMatch);
        if (isMatch != -1) {
          // const re = /${cls}/;
          var classN = obj_class.replace(cls, '');
        }
        obj.className = classN;//替换原来的 class.
      }
    },
    scrollIntoView (evt) {
      evt.preventDefault()
      const href = evt.target.getAttribute('href')
      const el = href ? document.querySelector(href) : null
      const tit = el ? el.querySelector('.model_tit') : null 
      const side_text = el ? el.querySelector('.side_text') : null 
      if (el) {
        let u = window.navigator.userAgent;
        if (!!u.match(/AppleWebKit.*Mobile.*/)||!!u.match(/AppleWebKit/)) {

          document.body.scrollTop = el.offsetTop;
          document.documentElement.scrollTop = el.offsetTop;
          if (el.id === 'home') {
            const homeTit = el.querySelector('.homeTit');
            this.addClass(homeTit, 'animated zoomIn');
          } else {
            this.addClass(tit, 'animated fadeInUp');
            this.addClass(side_text, 'animated fadeInUp');
          }
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
<style lang="scss" scoped>
  @import '../styles/home.scss';
  @import '../styles/media.scss';
  
  

</style>
