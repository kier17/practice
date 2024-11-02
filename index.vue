<script setup>  
import { ref } from 'vue'  

// 导航菜单状态  
const isMenuOpen = ref(false)  
  

// 文章数据  
const articles = [  
  { title: '拨通语音和视频通话，时时刻刻与彼此相伴', description: '无论是与同学进行群组通话，还是与妈妈简短通话，语音和视频通话都能让你们感觉彼此近在眼前。', image: 'src/assets/imgs/newImgs/article3-1.png' },  
  { title: '自由自在地交谈', description: '端到端加密让您的个人消息和通话更有安全保障。只有您与您的交谈对象可以查看或收听，任何中间方都无法查看或收听，WhatsApp 也不例外。', image: 'src/assets/imgs/newImgs/article3-2.png' },  
  { title: '利用群组保持联系', description: '无论是计划与好友一起出游，还是不想错过家人对话，群组对话都可轻松应对。', image: 'src/assets/imgs/newImgs/article3-3.png' },  
  { title: '表达真情实感', description: '不用文字，也能肆意展现自我。使用贴图和 GIF 来表达自己的感情，或发布动态来分享每日点滴。录制语音消息，简单问声好或讲述一段篇幅较长的故事。', image: 'src/assets/imgs/newImgs/article3-4.png' },  
  { title: '实现业务转型', description: 'WhatsApp Business 可助您触达全球客户，规模化打造引人入胜的体验。您可以借助 WhatsApp 展示商品和服务，提高销量以及与顾客建立关系。', image: 'src/assets/imgs/newImgs/article3-5.png' },  
]  
// 页脚链接  
const footerLinks = {  
  whatsapp: [  
    { text: '功能', url: '#' },  
    { text: '博客', url: '#' },  
    { text: '安全', url: '#' },  
    { text: 'For Business', url: '#' }  
  ],  
  company: [  
    { text: '关于我们', url: '#' },  
    { text: '招聘信息', url: '#' },  
    { text: '品牌中心', url: '#' },  
    { text: '隐私', url: '#' }  
  ],  
  download: [  
    { text: 'Android', url: '#' },  
    { text: 'iPhone', url: '#' },  
    { text: 'Mac/PC', url: '#' },  
    { text: 'whatsApp网页版', url: '#' }  
  ]  ,
  help: [  
    { text: '联系我们', url: '#' },  
    { text: '帮助中心', url: '#' },  
    { text: '下载', url: '#' },  
    { text: '安全声明', url: '#' }  
  ]  
}  

// 语言选择  
const languages = [  
  { code: 'zh', name: '简体中文' },  
  { code: 'en', name: 'English' },  
  { code: 'es', name: 'Español' }  
]  
const selectedLanguage = ref('zh')  
</script>  

<template>  
  <div class="app">  
    <!-- 导航栏 -->  
    <nav class="navbar">  
      <div class="navbar-container">  
        <button class="menu-button" @click="isMenuOpen = !isMenuOpen">  
          <span class="menu-icon"></span>  
        </button>  

        <div class="logo">  
          <img src="src/assets/imgs/newImgs/what-logo.svg" alt="WhatsApp Logo">  
        </div>  

        <div class="nav-links" :class="{ 'active': isMenuOpen }">  
          <a href="#" class="nav-link">功能</a>  
          <a href="#" class="nav-link">隐私</a>  
          <a href="#" class="nav-link">帮助中心</a>  
          <a href="#" class="nav-link">博客</a>  
          <a href="#" class="nav-link">商家专区</a>  
          <a href="#" class="nav-link">whatsApp网页版</a>  
          <a href="#" class="nav-link">下载</a>  

        </div>  

        <button class="download-button">  
          <span>下载</span>  
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none" class="_wauiIcon__download-alternative _agnt _9u4c"><path fill-rule="evenodd" clip-rule="evenodd" d="M13.75 13.75C13.75 14.1642 13.4142 14.5 13 14.5L3 14.5C2.58579 14.5 2.25 14.1642 2.25 13.75C2.25 13.3358 2.58579 13 3 13L13 13C13.4142 13 13.75 13.3358 13.75 13.75Z" fill="currentColor"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M8.7487 2C8.7487 1.58579 8.41291 1.25 7.9987 1.25C7.58448 1.25 7.2487 1.58579 7.2487 2L7.2487 9.53955L3.19233 5.51449C2.89831 5.22274 2.42344 5.22458 2.13168 5.5186C1.83993 5.81263 1.84177 6.2875 2.13579 6.57925L7.46912 11.8714C7.76154 12.1616 8.23325 12.1616 8.52567 11.8714L13.859 6.57926C14.153 6.2875 14.1549 5.81263 13.8631 5.5186C13.5714 5.22458 13.0965 5.22274 12.8025 5.51449L8.7487 9.53697L8.7487 2Z" fill="currentColor"></path></svg>
        </button>      
      </div>  

      <!-- 移动端菜单 -->  
      <div v-if="isMenuOpen" class="mobile-menu">  
        <a href="#" class="mobile-link">功能</a>  
        <a href="#" class="mobile-link">隐私</a>  
        <a href="#" class="mobile-link">帮助中心</a>  
        <a href="#" class="mobile-link">博客</a>  
        <a href="#" class="mobile-link">商家专区</a>  
        <a href="#" class="nmobile-link">whatsApp网页版</a>  
        <a href="#" class="mobile-link">下载</a>  
      </div>  
    </nav>  

    <main class="main-content">  
    <!-- 功能展示部分 -->  
      <section class="features">  
        <div class="features-container">  
          <div class="feature-box">  
            <!-- 左边内容 -->  
            <div class="feature-content">  
              <article>  
                <h1>私密地收发消息</h1>  
                <p>简单、可靠的免费*私密消息和通话体验，在世界各地均可享受。</p>  
                <button class="download-button">下载</button>  
              </article>  
            </div>  
            <!-- 右边图片 -->  
            <div class="feature-image">  
              <!-- 五张图片 -->  
              <img src="src/assets/imgs/newImgs/what-article1-1.png" alt="Feature Image 1">  
              <img src="src/assets/imgs/newImgs/what-article1-2.png" alt="Feature Image 2">  
              <img src="src/assets/imgs/newImgs/what-article1-3.png" alt="Feature Image 3">  
              <img src="src/assets/imgs/newImgs/what-article1-4.png" alt="Feature Image 4">  
              <img src="src/assets/imgs/newImgs/what-article1-5.png" alt="Feature Image 5">  
            </div>  
          </div> 
        </div>  
        <p class="bottle-p">* 可能会产生流量费用。请联系您的运营商了解详情。</p> 
        <img class="chat-pic" src="src/assets/imgs/newImgs/what-article2-1.png" alt="">
        <div>       
           <h2 class="pic-h">借助私密消息和通话，您可以放心地表达自己，畅所欲言，跨越距离的阻碍，与最重要的人保持紧密联系。</h2>
        </div>
        <img class="chat-pic" src="src/assets/imgs/newImgs/what-article2-2.png" alt="">
      </section>  
      <section class="pic-articles">
        <div  
      v-for="(item, index) in articles"  
      :key="index"  
      :class="['pic-article', { reverse: index % 2 !== 0 }]"  
    >  
      <div class="letter">  
        <h2>{{ item.title }}</h2>  
        <p>{{ item.description }}</p>  
        <a href="#">了解更多 ></a>  
      </div>  
      <div class="pic">  
        <img :src="item.image" alt="Feature Image" />  
      </div>  
    </div>  
      </section>
    </main>  

    <!-- 页脚 -->  
    <footer class="footer">  
      <div class="footer-container">  
        <div class="footer-grid">  
          <!-- Logo和描述 -->  
          <div class="footer-section ">  
            <div class="logo-des">  
              <img src="src/assets/imgs/newImgs/footer-logo.svg" alt="WhatsApp" class="footer-logo">  
              <button class="download-button">  
                  <span>下载</span>  
                  <svg width="16" height="16" viewBox="0 0 16 16" fill="none" class="_wauiIcon__download-alternative _agnt _9u4c"><path fill-rule="evenodd" clip-rule="evenodd" d="M13.75 13.75C13.75 14.1642 13.4142 14.5 13 14.5L3 14.5C2.58579 14.5 2.25 14.1642 2.25 13.75C2.25 13.3358 2.58579 13 3 13L13 13C13.4142 13 13.75 13.3358 13.75 13.75Z" fill="currentColor"></path><path fill-rule="evenodd" clip-rule="evenodd" d="M8.7487 2C8.7487 1.58579 8.41291 1.25 7.9987 1.25C7.58448 1.25 7.2487 1.58579 7.2487 2L7.2487 9.53955L3.19233 5.51449C2.89831 5.22274 2.42344 5.22458 2.13168 5.5186C1.83993 5.81263 1.84177 6.2875 2.13579 6.57925L7.46912 11.8714C7.76154 12.1616 8.23325 12.1616 8.52567 11.8714L13.859 6.57926C14.153 6.2875 14.1549 5.81263 13.8631 5.5186C13.5714 5.22458 13.0965 5.22274 12.8025 5.51449L8.7487 9.53697L8.7487 2Z" fill="currentColor"></path></svg>
              </button>             
            </div>
          </div>  

          <!-- WhatsApp链接 -->  
          <div class="footer-section">  
            <h3>功用介绍</h3>  
            <ul>  
              <li v-for="link in footerLinks.whatsapp" :key="link.text">  
                <a :href="link.url">{{ link.text }}</a>  
              </li>  
            </ul>  
          </div>  

          <!-- 公司链接 -->  
          <div class="footer-section">  
            <h3>我们是谁</h3>  
            <ul>  
              <li v-for="link in footerLinks.company" :key="link.text">  
                <a :href="link.url">{{ link.text }}</a>  
              </li>  
            </ul>  
          </div>  

          <!-- 下载链接 -->  
          <div class="footer-section">  
            <h3>使用WhatsApp</h3>  
            <ul>  
              <li v-for="link in footerLinks.download" :key="link.text">  
                <a :href="link.url">{{ link.text }}</a>  
              </li>  
            </ul>  
          </div>  
             <!-- 下载链接 -->  
             <div class="footer-section">  
            <h3>需要帮助？</h3>  
            <ul>  
              <li v-for="link in footerLinks.help" :key="link.text">  
                <a :href="link.url">{{ link.text }}</a>  
              </li>  
            </ul>  
          </div>  
        </div>  

       <div class="footer-bottom">  
          <div class="footer-copyright">  
            <p>2024 ©</p>  
            <p>WhatsApp LLC.</p>  
          </div>
          <div class="footer-links">  
            <a href="#">条款和隐私政策</a>  
            <a href="#">网站地图</a>  
          </div>  
          <div class="social-icons">  
            <a href="#">
              <svg viewBox="0 0 1200 1227" fill="none" xmlns="http://www.w3.org/2000/svg" class="_aghm _adid _arcp _afbl"><path d="M714.163 519.284L1160.89 0H1055.03L667.137 450.887L357.328 0H0L468.492 681.821L0 1226.37H105.866L515.491 750.218L842.672 1226.37H1200L714.137 519.284H714.163ZM569.165 687.828L521.697 619.934L144.011 79.6944H306.615L611.412 515.685L658.88 583.579L1055.08 1150.3H892.476L569.165 687.854V687.828Z" fill="currentColor"></path></svg></a>  
            <a href="#">
              <svg width="23" height="16" viewBox="0 0 23 16" fill="none" xmlns="http://www.w3.org/2000/svg" class="_wauiIcon__youtube _adid _arcp _afbl"><path d="M22.0088 5.95168C22.0583 4.52034 21.7452 3.0997 21.0988 1.82168C20.6602 1.29728 20.0515 0.943393 19.3788 0.821683C16.5963 0.569209 13.8023 0.465727 11.0088 0.511683C8.22546 0.463642 5.44152 0.563783 2.66882 0.811683C2.12064 0.9114 1.61333 1.16853 1.20882 1.55168C0.308816 2.38168 0.208816 3.80168 0.108816 5.00168C-0.036272 7.15925 -0.036272 9.32412 0.108816 11.4817C0.137746 12.1571 0.23831 12.8275 0.408816 13.4817C0.529391 13.9867 0.773339 14.454 1.11882 14.8417C1.52608 15.2451 2.0452 15.5169 2.60882 15.6217C4.76473 15.8878 6.93703 15.9981 9.10882 15.9517C12.6088 16.0017 15.6788 15.9517 19.3088 15.6717C19.8863 15.5733 20.42 15.3012 20.8388 14.8917C21.1188 14.6116 21.3279 14.2688 21.4488 13.8917C21.8064 12.7943 21.9821 11.6458 21.9688 10.4917C22.0088 9.93168 22.0088 6.55168 22.0088 5.95168ZM8.74882 11.0917V4.90168L14.6688 8.01168C13.0088 8.93168 10.8188 9.97168 8.74882 11.0917Z" fill="currentColor"></path></svg>
            </a>
              <a href="#">
                <svg width="20" height="21" viewBox="0 0 20 21" fill="none" xmlns="http://www.w3.org/2000/svg" class="_wauiIcon__instagram _adid _arcp _afbl"><path d="M15.34 3.96C15.1027 3.96 14.8707 4.03038 14.6733 4.16224C14.476 4.29409 14.3222 4.48151 14.2313 4.70078C14.1405 4.92005 14.1168 5.16133 14.1631 5.39411C14.2094 5.62689 14.3236 5.84071 14.4915 6.00853C14.6593 6.17635 14.8731 6.29064 15.1059 6.33694C15.3387 6.38324 15.5799 6.35948 15.7992 6.26866C16.0185 6.17783 16.2059 6.02402 16.3378 5.82668C16.4696 5.62935 16.54 5.39734 16.54 5.16C16.54 4.84174 16.4136 4.53652 16.1885 4.31147C15.9635 4.08643 15.6583 3.96 15.34 3.96ZM19.94 6.38C19.9206 5.5503 19.7652 4.7294 19.48 3.95C19.2257 3.28313 18.83 2.67928 18.32 2.18C17.8248 1.66743 17.2196 1.27418 16.55 1.03C15.7727 0.736161 14.9508 0.57721 14.12 0.56C13.06 0.5 12.72 0.5 10 0.5C7.28 0.5 6.94 0.5 5.88 0.56C5.04915 0.57721 4.22734 0.736161 3.45 1.03C2.78168 1.27665 2.17693 1.66956 1.68 2.18C1.16743 2.67518 0.774176 3.28044 0.53 3.95C0.236161 4.72734 0.07721 5.54915 0.0599999 6.38C-5.58794e-08 7.44 0 7.78 0 10.5C0 13.22 -5.58794e-08 13.56 0.0599999 14.62C0.07721 15.4508 0.236161 16.2727 0.53 17.05C0.774176 17.7196 1.16743 18.3248 1.68 18.82C2.17693 19.3304 2.78168 19.7234 3.45 19.97C4.22734 20.2638 5.04915 20.4228 5.88 20.44C6.94 20.5 7.28 20.5 10 20.5C12.72 20.5 13.06 20.5 14.12 20.44C14.9508 20.4228 15.7727 20.2638 16.55 19.97C17.2196 19.7258 17.8248 19.3326 18.32 18.82C18.8322 18.3226 19.2283 17.7182 19.48 17.05C19.7652 16.2706 19.9206 15.4497 19.94 14.62C19.94 13.56 20 13.22 20 10.5C20 7.78 20 7.44 19.94 6.38ZM18.14 14.5C18.1327 15.1348 18.0178 15.7637 17.8 16.36C17.6403 16.7952 17.3839 17.1884 17.05 17.51C16.7256 17.8405 16.3332 18.0964 15.9 18.26C15.3037 18.4778 14.6748 18.5927 14.04 18.6C13.04 18.65 12.67 18.66 10.04 18.66C7.41 18.66 7.04 18.66 6.04 18.6C5.38089 18.6123 4.72459 18.5109 4.1 18.3C3.68578 18.1281 3.31136 17.8728 3 17.55C2.66809 17.2287 2.41484 16.8352 2.26 16.4C2.01586 15.7952 1.88044 15.1519 1.86 14.5C1.86 13.5 1.8 13.13 1.8 10.5C1.8 7.87 1.8 7.5 1.86 6.5C1.86448 5.85106 1.98295 5.20795 2.21 4.6C2.38605 4.17791 2.65627 3.80166 3 3.5C3.30381 3.15617 3.67929 2.8831 4.1 2.7C4.70955 2.48004 5.352 2.36508 6 2.36C7 2.36 7.37 2.3 10 2.3C12.63 2.3 13 2.3 14 2.36C14.6348 2.36728 15.2637 2.48225 15.86 2.7C16.3144 2.86865 16.7223 3.14285 17.05 3.5C17.3777 3.80718 17.6338 4.18273 17.8 4.6C18.0223 5.20893 18.1373 5.85178 18.14 6.5C18.19 7.5 18.2 7.87 18.2 10.5C18.2 13.13 18.19 13.5 18.14 14.5ZM10 5.37C8.98581 5.37198 7.99496 5.67453 7.15265 6.23942C6.31035 6.80431 5.65438 7.6062 5.26763 8.54375C4.88089 9.48131 4.78072 10.5125 4.97979 11.5069C5.17886 12.5014 5.66824 13.4145 6.38608 14.131C7.10392 14.8474 8.01801 15.335 9.01286 15.5321C10.0077 15.7293 11.0387 15.6271 11.9755 15.2385C12.9123 14.85 13.7129 14.1924 14.2761 13.349C14.8394 12.5056 15.14 11.5142 15.14 10.5C15.1413 9.8251 15.0092 9.15661 14.7512 8.53296C14.4933 7.90931 14.1146 7.34281 13.6369 6.86605C13.1592 6.38929 12.5919 6.01168 11.9678 5.75493C11.3436 5.49818 10.6749 5.36736 10 5.37ZM10 13.83C9.34139 13.83 8.69757 13.6347 8.14995 13.2688C7.60234 12.9029 7.17552 12.3828 6.92348 11.7743C6.67144 11.1659 6.6055 10.4963 6.73398 9.85035C6.86247 9.20439 7.17963 8.61104 7.64533 8.14533C8.11104 7.67963 8.70439 7.36247 9.35035 7.23398C9.99631 7.1055 10.6659 7.17144 11.2743 7.42348C11.8828 7.67552 12.4029 8.10234 12.7688 8.64995C13.1347 9.19757 13.33 9.84139 13.33 10.5C13.33 10.9373 13.2439 11.3703 13.0765 11.7743C12.9092 12.1784 12.6639 12.5454 12.3547 12.8547C12.0454 13.1639 11.6784 13.4092 11.2743 13.5765C10.8703 13.7439 10.4373 13.83 10 13.83Z" fill="currentColor"></path></svg>
              </a>
          <a href="#">
            <svg width="11" height="21" viewBox="0 0 11 21" fill="none" xmlns="http://www.w3.org/2000/svg" class="_wauiIcon__facebook-alt _adid _arcp _afbl"><path d="M8.51 3.82003H10.39V0.64003C9.47975 0.545377 8.56516 0.498646 7.65 0.50003C4.93 0.50003 3.07 2.16003 3.07 5.20003V7.82003H0V11.38H3.07V20.5H6.75V11.38H9.81L10.27 7.82003H6.75V5.55003C6.75 4.50003 7.03 3.82003 8.51 3.82003Z" fill="currentColor"></path></svg>
          </a>
         </div>
          <div class="language-selector">  
            <select v-model="selectedLanguage">  
              <option v-for="lang in languages" :key="lang.code" :value="lang.code">  
                {{ lang.name }}  
              </option>  
            </select>  
          </div>  
        </div>
      </div>  
    </footer>  
  </div>  
</template>  

<style scoped>  
/* 变量定义 */  
:root {  
  --primary-color: #25D366;  
  --secondary-color: #128C7E;  
  --text-color: #1C1E21;  
  --bg-color: #fcf5eb;  
  --footer-bg: rgb(17, 27, 33);  
  --max-width: 1200px;  
  --nav-height: 64px;  
}  

/* 基础样式 */  
.app {  
  min-height: 100vh;  
  background-color: rgb(252, 245, 235);  
}  

/* 导航栏样式 */  
.navbar {  
  position: fixed;  
  top: 0;  
  left: 0;  
  right: 0;  
  height: 80px;  
  background: rgba(252, 245, 235) ;  
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);  
  z-index: 1000;  
  display: flex;  
  justify-content: center; /* 水平居中 */  
  align-items: center; /* 垂直居中 */  
}  

.navbar-container {  
  height: 50px;  
  display: flex;  
  align-items: center;  
  justify-content: space-between;  
  width: 100%; /* 确保使用全宽 */  
  max-width: 2000px; /* 根据需要设置最大宽度 */  
}  

.logo img {  
  height: 24px;  
  width: 100px;
  margin-left: 20px;
}  

.nav-links {  
  display: none;  
}  

.nav-link {  
  color: #666;  
  font-size: 17px;
  white-space: nowrap;

  text-decoration: none;  
  transition: color 0.3s ease;  
}  

.nav-link:hover {  
  color: var(--primary-color);  
}  


.download-button {  
  background-color: #25d366; /* 绿色背景 */  
  border: 1px solid #1c1e21; /* 黑色边框 */  
  border-radius: 25px; /* 圆角 */  
  width: 120px; /* 按钮宽度 */  
  height: 51px; /* 按钮高度 */  
  display: flex;  
  align-items: center;  
  justify-content: center;  
  cursor: pointer;  
  transition: background-color 0.3s ease, color 0.3s ease;  
  color: #151516; /* 文字颜色 */  
  font-size: 17px; /* 字体大小 */  
  font-family: Helvetica Neue, Helvetica Neue, Helvetica, Arial, sans-serif;
  font-weight: 500;
  margin-right: 20px;
}  

.download-button:hover {  
  background-color: #1c1e21; /* 悬停时黑色背景 */  
  color: #ffffff; /* 悬停时白色文字 */  
}  

.download-button .icon {  
  margin-left: 8px; /* 图标与文本间的间距 */  
  fill: currentColor; /* 使用当前文本颜色 */  
} 

/* 修改汉堡菜单图标样式 */  
.menu-button {  
  display: block;  
  background: none;  
  border: none;  
  padding: 0.5rem;  
  cursor: pointer;  
  width: 40px;  
  height: 40px;  
  display: flex;  
  align-items: center;  
  justify-content: center;  
}  

.menu-icon {  
  display: block;  
  width: 22px;  
  height: 1px;  
  background: black;  
  position: relative;  
  /* transition: background-color 0.3s ease;   */
}  

.menu-icon::before,  
.menu-icon::after {  
  content: '';  
  position: absolute;  
  width: 22px;  
  height: 1px;  
  background: black;  
  left: 0;  
}  

.menu-icon::before {  
  top: -4px;  
}  

.menu-icon::after {  
  bottom: -4px;  
}  

/* 当菜单打开时的动画效果 */  
.menu-button[aria-expanded="true"] .menu-icon {  
  background: transparent;  
}  

.menu-button[aria-expanded="true"] .menu-icon::before {  
  transform: rotate(45deg) translate(5px, 5px);  
}  

.menu-button[aria-expanded="true"] .menu-icon::after {  
  transform: rotate(-45deg) translate(5px, -5px);  
}  
.download-icon{
  background-color: rgb(37, 211, 102) ;
}
.mobile-menu {  
  display: block;  
  position: absolute;  
  top: var(--nav-height);  
  left: 0;  
  right: 0;  
  background: rgba(255, 255, 255, 0.901);  
  border-top: 1px solid #eee;  
  padding: 1rem;  
}  

.mobile-link {  
  display: block;  
  color: #666;  
  text-decoration: none;  
  padding: 0.75rem 1rem;  
  transition: color 0.3s ease;  
}  

.mobile-link:hover {  
  color: var(--primary-color);  
}  

/* 主要内容样式 */  
.main-content {  
  

}  
.features{
}

.features-container {  
  padding: 32px;  
  background-image: url('src/assets/imgs/newImgs/what-article1.png');  
  width: 100%; /* Changed to percentage for responsiveness */  
  max-width: 2000px; 
  aspect-ratio: calc(1158 / 752); /* Maintain aspect ratio */  
  height: 752px;
  margin: 0 auto;
  background-size: cover; /* 或者使用 contain */  
  background-position: center;  
  background-repeat: no-repeat;  
  border-radius: 20px; /* 设置圆角 */  
  overflow: hidden; /* 确保内容不溢出圆角 */  
  display: flex;  
  justify-content: space-between;  
  align-items: center;  
}  

.feature-box {  
  display: flex;  
  padding: 24px;  
  border-radius: 8px;  
  width: 100%;
  margin: 0 100px;
}  

.feature-content {  
  flex: 1;  
  padding-right: 24px; 
  width: 360px; 
  line-height: 1;
}  

.feature-content h1 {  
  font-size: 81px;  
  margin-bottom: 16px;  
}  

.feature-content p {  
  font-size: 19px;  
  margin-bottom: 24px;  
}  


.feature-image {  
  display: flex;  
  flex-direction: column;  
  gap: 10px;  
}  

.feature-image img {  
  width: 436px;  
  border-radius: 10px;  
  object-fit: cover;  
}  
.bottle-p{
  color: rgb(94, 94, 94);
  font-size: 13px;
  font-weight: 400;
  text-align: right;
  margin-right: 20px;
  height: 42px;
  line-height: 42px;

}
.chat-pic{
    height: auto;
    max-width: 100%;
    width: auto;
    padding: 32px;
}
.pic-h{
  color: black;
  font-size: 49px;
  text-align: center;
  width: 900px;
  height: 147px;
  margin: 56px auto;
  line-height: 1; /* 设置行高为1，取消行间距 */  

}
.pic-articles{
  display: flex;  
  flex-direction: column;  
}  

.pic-article {  
  display: flex;  
  margin-bottom: 30px;  
}  

.letter {  
  flex: 1;  
  padding: 20px;  
}  
.letter h2{
  color: black;
  font-size: 61px;
  text-align: center;
  width: 450px;
  margin: 56px auto;
  line-height: 1; /* 设置行高为1，取消行间距 */  
  font-family: Helvetica Neue, Helvetica Neue, Helvetica, Arial, sans-serif;
  font-weight: 400;
}
.letter a{
  color: black;
  font-size: 17px;
  margin: 40px 70.6px;

}
.letter p{
  color: black;
  font-size: 19px;
  line-height: 25px;
  font-weight: 400;
  text-align: right;
  margin: 0 70.6px;
}
.pic {  
  flex: 1;  
}  

.pic img {  
  width: 100%;  
  height: auto;  
}  

.reverse {  
  flex-direction: row-reverse;  
}  

/* 页脚样式 */  
.footer {  
  color: white;  
  padding: 4rem 0 2rem;  
  background-color: rgb(17, 27, 33);
  height: 200px ;
}  

.footer-container {  
  max-width: 2000px;  
  background-color: rgb(17, 27, 33);
  
}  

.footer-grid {  
  display: flex;  
  justify-content: space-between; /* Distribute items across the available space */  
  align-items: center; /* Vertically align items */  
  width: 100%; /* Ensure grid stretches across the parent width */  
  max-width: 1000px; /* Provide a maximum width for centering */  
  margin: 0 auto; /* Center the footer-grid within its parent */  
  box-sizing: border-box; 
  padding-bottom: 10px;
  border-bottom: rgb(45, 63, 58) solid 1px;/* Include padding in the total width calculation */  
}  

.footer-section {  
  flex: 1; /* Allow sections to take equal space */  
  text-align: center; /* Center content within each section horizontally */  
}  
.logo-des {  
  display: flex; /* Use flexbox for layout */  
  flex-direction: column; /* Arrange items in a column */  
  justify-content: center; /* Center elements vertically */  
  align-items: center; /* Center elements horizontally */  
  height: 200px; /* Optional: Set a height for the div */  
}  
.footer-section h3 {  
  font-size: 13px;  
  font-weight: 600;  
  margin-bottom: 1.5rem;  
  color: rgb(138, 144, 150);  

}  

.footer-section ul {  
  list-style: none;  
  padding: 0;  
}  

.footer-section ul li {  
  margin-bottom: 0.75rem;  
}  

.footer-section a {  
  color: white;  
  font-size: 19px;
  text-decoration: none;  
  transition: color 0.3s ease;  
}  

.footer-section a:hover {  
  color: white;  
}  

.footer-logo {  
  max-width: 120px; /* Adjust as needed for logo size */  
  margin-bottom: 110px;  
}  
.footer-section button {  
  margin-left: 15px;
}


.footer-bottom {  
  display: flex;  
  justify-content: space-between;  
  align-items: center;  
  background-color: rgb(17, 27, 33);  /* Adjust to match the dark theme */  
  padding: 32px;    
  color: rgb(138, 144, 150);  
  max-width: 1000px; /* Provide a maximum width for centering */  
  height: 56px;
  margin: 0 auto;
  font-size: 13px;

}  

.footer-bottom p {  
  margin: 0;  
}  

.footer-links a {  
  margin-right: 20px;  
  text-decoration: none;  
}  

.footer-links a:hover {  
  text-decoration: underline;  
}  

.social-icons {  
  display: flex; /* Use flexbox to arrange items horizontally */  
  gap: 15px; /* Add space between icons */  
}  

.social-icons a {  
  display: inline-block; /* Ensure each icon is treated as a block */  
}  

.social-icons svg {  
  width: 24px;  
  height: 24px;  
  fill: currentColor;  
}  

.language-selector select {  
  background-color: transparent;  
  border: 1px solid #fff;  
  padding: 5px;  
  border-radius: 5px;  
}

/* 响应式设计 */  
@media (min-width: 1200px) {  
  .menu-button {  
    display: none;  
  }  

  .nav-links {  
    display: flex;  
    gap: 2rem;  
  }  

  .mobile-menu {  
    display: none;  
  }  

  .feature-block {  
    flex-direction: row;  
    text-align: left;  
    gap: 4rem;  
  }  

  .feature-block.reverse {  
    flex-direction: row-reverse;  
  }  

  .footer-grid {  
    grid-template-columns: repeat(4, 1fr);  
  }  

  .footer-bottom {  
    flex-direction: row;  
    justify-content: space-between;  
  }  
}  

/* 动画效果 */  
@keyframes fadeIn {  
  from {  
    opacity: 0;  
    transform: translateY(20px);  
  }  
  to {  
    opacity: 1;  
    transform: translateY(0);  
  }  
}  

.feature-block {  
  animation: fadeIn 0.6s ease-out;  
}  
</style>  