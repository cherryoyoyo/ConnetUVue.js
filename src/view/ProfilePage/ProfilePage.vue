<template lang="">
    <div class="container">
        <div class="main-content">
            <div class="banner-box">
<<<<<<< HEAD
                <img src="../../assets/img/profile/background.svg" alt="">
                <div class="setting">
                    <router-link to="/index">
                        <span class="material-icons">settings</span>
                    </router-link>
=======
                <img src="../../assets/img/profile/background.svg" alt="" class="backimg">
                <div class="setting">
                    <button class="edit-button" @click="toggleEditList" v-show="showButton">編輯個人檔案</button>
                    <div v-if="showEditList" class="edit-list" v-click-outside="hideFanList">
                        <div class="edit-list-container">
                            <h2 class="edit-list-title">編輯個人檔案</h2>
                            <form @submit="submitForm">
                                <ul class="edit-list-items">
                                    <li class="edit-list-item">
                                        <label for="avatar">修改大頭貼：</label>
                                        <input type="file" id="avatar" accept="image/*" ref="avatarInput">
                                    </li>
                                    <li class="edit-list-item">
                                        <label for="username">修改會員名稱：</label>
                                        <input type="text" id="userName" v-model="userName">
                                    </li>
                                    <li class="edit-list-item">
                                        <label for="profile">修改個人簡介：</label>
                                        <input type="text" id="profile" v-model="profile">
                                    </li>
                                </ul>
                                <button type="submit">提交</button>
                            </form>
                        </div>
                    </div>
>>>>>>> dev
                </div>
            </div>
            <div class="profile-box flex-between">
                <div class="data-left">
<<<<<<< HEAD
                    <div class="photo-box">
                        <img src="" alt="個人照">
                    </div>
                    <div class="content-box">
                        <div class="username">
                            真正有影
                        </div>
                        <div class="slogan-box flex-center">
                            <span class="slogan">
                                你好，世界
                            </span>
                            <button class="edit">
                                <span class="material-icons">edit</span>
                            </button>
                        </div>
                        <div class="button-box flex-center">
                            <button class="profile-button">建立新文章</button>
                            <button class="profile-button">發佈動態</button>
                        </div>
                    </div>
                </div>
                <div class="data-right flex-end">
                    <button class="profile-button">追蹤</button>
                    <button class="profile-button">粉絲</button>
                    <button class="profile-button">訂閱</button>
                </div>
            </div>
            <ul class="nav flex-between">
                <li class="nav-item active">文章</li>
                <li class="nav-item">動態</li>
                <li class="nav-item">收藏</li>
            </ul>
            <div class="article-box flex-start">
                <div class="img-box">
                    <img src="../../assets/img/profile/article_img.svg" alt="文章縮圖">
                </div>
                <div class="article-content">
                    <div class="title">關於創新鏈的區塊鏈開發者最佳實踐!!</div>
                    <div class="tags flex-start">
                        <div class="tag">finance</div>
                        <div class="tag">bitcoin</div>
                        <div class="tag">crypto</div>
                    </div>
                    <div class="info-box flex-between">
                        <div class="author-info flex-start">
                            <div class="memoji-box flex-center">
                                <img src="../../assets/img/profile/memoji.svg" alt="">
                            </div>
                            <div class="author">
                                <div class="name">Pavel Gvay</div>
                                <div class="publish-time">3 weeks ago</div>
                            </div>
                        </div>
                        <div class="data-info flex-between">
                            <div class="count">651,324 Views</div>
                            <div class="count">36,6545 Likes</div>
                            <div class="count">56 comments</div>
                        </div>
                    </div>
                </div>
=======
                    <div class="photo-box" :style="{ backgroundImage: 'url(' + avatar + ')' }"></div>
                    <div class="content-box">
                        <div class="username">
                            <h1>{{ userName }}</h1>         
                        </div>
                        <div class="slogan-box flex-center">
                            <span class="slogan">{{ profile }}</span>
                        </div>
                        <div class="button-box flex-center">
                            <button class="profile-button">建立新文章</button> 
                            <button class="profile-button">發佈動態</button> 
                        </div>
                    </div>
                </div>
                <div class="countbar">
                    <button class="fans-button" @click="toggleFollowList">追蹤<br>{{followedByCount}}</button>
                    <div v-if="showFollowList" class="fan-list" v-click-outside="hideFollowList">
                        <div class="fan-list-container">
                            <h2 class="fan-list-title">所有追蹤</h2>
                            <ul class="fan-list-items">
                                <li class="fan-list-item" v-for="follow in follow" :key="follow.userId" @click="redirectToFanPage(follow.userId)">
                                    <img class="fan-avatar" :src="follow.avatar" alt="粉絲頭像">
                                    <span class="fan-name">{{ follow.userName }}</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <button class="fans-button" @click="toggleFanList">粉絲<br>{{followingCount}}</button>
                    <div v-if="showFanList" class="fan-list" v-click-outside="hideFanList">
                        <div class="fan-list-container">
                            <h2 class="fan-list-title">所有粉絲</h2>
                            <ul class="fan-list-items">
                                <li class="fan-list-item" v-for="fan in fans" :key="fan.userId" @click="redirectToFanPage(fan.userId)">
                                    <img class="fan-avatar" :src="fan.avatar" alt="粉絲頭像">
                                    <span class="fan-name">{{ fan.userName }}</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <button class="fans-button" @click="toggleSubList">訂閱<br>123</button>
                    <div v-if="showSubList" class="fan-list" v-click-outside="hideSubList">
                        <div class="fan-list-container">
                            <h2 class="fan-list-title">所有訂閱</h2>
                            <ul class="fan-list-items">
                                <li class="fan-list-item" v-for="fan in fans" :key="fan.id">
                                    <img class="fan-avatar" :src="fan.avatar" alt="粉絲頭像">
                                    <span class="fan-name">{{ fan.userName }}</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="follow">
                    <button class="follow-button" @click="toggleEditList">編輯個人檔案</button>
                    <button class="follow-button">分享個人檔案</button>
                </div>
            </div>
            <ul class="nav flex-between">
                <button class="nav-item" :class="{ active: activeTab === '文章' }" @click="activeTab = '文章'">文章</button>
                <button class="nav-item" :class="{ active: activeTab === '動態' }" @click="activeTab = '動態'">動態</button>
                <button class="nav-item" :class="{ active: activeTab === '收藏' }" @click="activeTab = '收藏'">收藏</button>
            </ul>
            <div v-if="activeTab === '文章'" class="tab-content">
                <ArticleitemVue />
            </div>
            <div v-if="activeTab === '動態'" class="tab-content">
                <Tweet />
            </div>
            <div v-if="activeTab === '收藏'" class="tab-content">
                <!-- 顯示收藏內容 -->
>>>>>>> dev
            </div>
        </div>
    </div>
</template>
<script>
<<<<<<< HEAD
export default {

}
</script>
<style lang="css" scoped>
=======

import axios from 'axios';
import Tweet from './components/MyProfilePage.vue';
import VueClickOutside from 'v-click-outside';
import ArticleitemVue from './components/Articleitem.vue';

export default {

    directives: {
    ClickOutside: VueClickOutside.directive
  },

    data() {
        return {
            userId: '',
            userName: '',
            avatar: '',
            profile: '',
            title: '',
            activeTab: '文章',
            followedByCount: '',
            followingCount: '',

            fans: [],
            follow: [],
            showFanList: false ,
            showFollowers: false,
            showFans: false,
            showSubscribers: false,
            showEditList: false,
            showSubList: false,
            showFollowList: false,
        };
    },

    components: {
        Tweet,
        ArticleitemVue,
    },

    methods: {

        redirectToFanPage(userId) {
            this.$router.push(`/Anotherprofile/${userId}`);
        },

        
  fetchFansData() {
      axios.get(`/users/following`)
        .then(response => {
            this.fans = response.data.data;
        })
            .catch(error => {
        });
    },

    fetchFollowData() {
      axios.get(`/users/followedBy`)
        .then(response => {
            this.follow = response.data.data;
        })
            .catch(error => {
            console.log(error);
        });
    },


    hideFanList() {
      this.showFanList = false;
      this.showEditList = false;
    },
    hideSubList() {
      this.showSubList = false;
    },
    hideFollowList() {
      this.showFollowList = false;
    },
    toggleEditList() {
      this.showEditList = !this.showEditList;
    },
    toggleSubList() {
      this.showSubList = !this.showSubList;
    },
    toggleFollowList() {
      this.showFollowList = !this.showFollowList;
      if (this.showFollowList && this.follow.length === 0) {
        this.fetchFollowData();
        }
    },
    toggleFanList() {
        this.showFanList = !this.showFanList;
        if (this.showFanList && this.fans.length === 0) {
        this.fetchFansData();
        }
},

    
    submitForm(event) {

        setTimeout(() => {
        location.reload();
      }, 1000);
      
  event.preventDefault();

  const formData = new FormData();

  formData.append('userId', this.userId);
  formData.append('userName', this.userName);
  formData.append('profile', this.profile);
  formData.append('files', this.$refs.avatarInput.files[0] == null?new File([], 'empty-file.txt'):this.$refs.avatarInput.files[0]);

  axios.put('/users', formData, {
    headers: {
      'Content-Type': 'multipart/form-data'
    }
  })
    .then(response => {
    })
    .catch(error => {
      console.log(error);
    });
}



  },
  
    
    created() {
        this.getUserData();
        this.getUserThreads();
    },
  

    created() {

        // 在組件創建時使用 Axios，並傳遞使用者 ID
        axios.post('/users/getUserId/0')
            .then(response => {
                this.userId = response.data.userId;
                this.userName = response.data.userName;
                this.avatar = response.data.avatar;
                this.profile = response.data.profile;
                this.followingCount = response.data.followingCount;
                this.followedByCount = response.data.followedByCount;
            })
            .catch(error => {
                console.log(error);
                // 處理錯誤 
            });

        // 查詢使用者文章的API
        axios.get('/threads/userThread/0')
            .then(response => {
                // console.log(response.data);
                if (response.data.data && response.data.data.length > 0) {
                    this.title = response.data.data[0].title;

                    this.activeTab = '文章';
                } else {
                    this.title = '找不到文章';
                }
            })
            .catch(error => {
                this.title = '找不到文章';
            });
    }
}
</script>
<style lang="css" scoped>

.tab-content {
    width: 1025px;  /* 更改這個數值到你想要的寬度 */
    height: 100%; /* 更改這個數值到你想要的高度 */
}

.backimg {
    width: 1025px;
}

.countbar {
    position: relative;
    margin-top: -220px;
    left: 300px;
    display: flex;

}

/* 粉丝列表容器样式 */
.fan-list {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #fff;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  z-index: 9999;
}

.fan-list-container {
    width: 600px;
    margin: 0 auto; /* 添加此行，使用margin: 0 auto; 将内容水平置中 */
    padding: 20px;
    display: flex; /* 添加此行，使用flex布局 */
    flex-direction: column; /* 添加此行，使内容垂直方向上居中 */
    align-items: center; /* 添加此行，使内容水平方向上居中 */
    max-height: 800px; /* 设置最大高度，根据需要进行调整 */
    overflow-y: scroll; /* 添加垂直滚动条 */
}

.fan-list-title {
  font-size: 40px;
  font-weight: bold;
  margin-bottom: 10px;
}

.fan-list-item {
  display: flex;
  align-items: center;
  margin-bottom: 100px;
  
}

.fan-avatar {
  width: 80px;
  height: 80px;
  border-radius: 100%;
  margin-right: 100px;
}

.fan-name {
  font-size: 30px;
  font-weight: bold;
}

/* 編輯個人檔案 */

.edit-list {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #fff;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
  border-radius: 4px;
  z-index: 9999;
}

.edit-list-container {
  width: 600px;
  margin: 0 auto; 
    padding: 20px;
    display: flex; 
    flex-direction: column; 
    align-items: center; 
    background-color: whitesmoke;
    border: 10px solid grey;
    border-radius: 10px;
}

.edit-list-title {
  font-size: 18px;
  font-weight: bold;
  margin-bottom: 10px;
}

.edit-list-item {
  display: flex;
  align-items: center;
  margin-bottom: 100px;
  border: 2px solid grey;
  border-radius: 10px;
}

.edit-avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}

.edit-name {
  font-size: 14px;
  font-weight: bold;
}


/* 編輯個人檔案 */


>>>>>>> dev
.container {
    display: flex;
    justify-content: center;
    align-items: start;
    padding-bottom: 40px;
}

.flex-between {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.flex-center {
    display: flex;
    justify-content: center;
    align-items: center;
}

<<<<<<< HEAD
=======
.flex-top {
    display: flex;
    justify-content: center;
    align-items: flex-start;
}

>>>>>>> dev
.flex-start {
    display: flex;
    justify-content: start;
    align-items: center;
}

.flex-end {
    display: flex;
    justify-content: end;
    align-items: center;
}

.main-content {
    width: fit-content;
}

<<<<<<< HEAD
=======
.edit-box {
    position: relative;
}

>>>>>>> dev
/* banner */
.banner-box {
    width: 882px;
    position: relative;
}

.photo-box {
    position: absolute;
    top: -251.52px;
    left: 48.72px;
    width: 291.5px;
    height: 291.5px;
    border-radius: 50%;
    background-color: #EFD7C7;
<<<<<<< HEAD
=======
    background-size: cover;
>>>>>>> dev
}

.setting {
    position: absolute;
    top: 13px;
    right: 13px;
}

.setting .material-icons {
    color: var(--black);
}

/* 個人資料 */
.profile-box {
    position: relative;
    margin-bottom: 40px;
}

.data-left {
    padding-top: 50px;
    width: 291.5px;
    flex: 1;
}

.content-box {
    width: calc(291.5px + 48.72px * 2);
<<<<<<< HEAD
}

.username {
=======
    height: 200px;
}

.username {
    height: 70px;
>>>>>>> dev
    font-family: 'Inter';
    font-size: 45px;
    font-weight: 700;
    line-height: 68px;
    letter-spacing: -0.022em;
    text-align: center;
    color: var(--black);
}

.slogan-box {
    margin: 0 auto 16px;
<<<<<<< HEAD
=======
    height: 50px;
>>>>>>> dev
}

.slogan {
    font-family: 'Inter';
    font-size: 27px;
    font-weight: 500;
    line-height: 41px;
    letter-spacing: -0.019em;
    text-align: center;
}

.slogan-box .edit {
    margin-left: 20px;
    border: none;
    background-color: transparent;
    cursor: pointer;
}

.data-right {
<<<<<<< HEAD
    flex: 1;
    margin-bottom: auto;
=======
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-direction: column;
}


.count-box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 15px;
}

.edit-button {
    padding: 8px 16px;
    border: 4px solid lightgrey;
    border-radius: 18.19px;
    background-color: gray;
    color: #FFF;
}

.follow{
    top: 135px;
    left:-130px;
    position: relative;
    display: flex;
    justify-content: space-between;
}

.follow-button {
    margin-left: 30PX;
    padding: 8px 30px;
    border: 4px solid lightgrey;
    border-radius: 18.19px;
    background-color: gray;
    color: #FFF;
}

.fans-button {
    padding: 8px 24px;
    border: 4px solid gray;
    border-radius: 18.19px;
    background-color: white;
    color: black;
    margin-right: 30px;
>>>>>>> dev
}

.profile-button {
    padding: 8px 16px;
    border: 4px solid lightgrey;
    border-radius: 18.19px;
    background-color: var(--black);
    color: #FFF;
<<<<<<< HEAD
    margin-right: 45.5px;
=======
    margin-right: 10px;
}

.button-box {

    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 40px;
>>>>>>> dev
}

.button-box .profile-button {
    width: 130px;
}

.button-box .profile-button:not(:last-child) {
    margin-right: 17.5px;
}

/* nav */
.nav {
    list-style-type: none;
    padding: 0 40px;
    margin: 0;
    margin-bottom: 37px;
}

.nav-item {
    font-family: 'Inter';
    font-size: 44px;
    font-weight: 500;
    line-height: 66px;
    letter-spacing: -0.011em;
    text-align: center;
}

.active {
    color: var(--active);
}

<<<<<<< HEAD
=======

>>>>>>> dev
/* article-box */
.article-box {
    border-radius: 17.29px;
    background-color: #FFF;
    box-shadow: 0px 4.0237250328063965px 4.0237250328063965px 0px #00000040;
    padding: 21px;
}

.article-box .img-box {
    margin-right: 21.61px;
}

.article-content {
    margin-bottom: auto;
    width: 100%;
}

.article-content .title {
    font-family: 'Source Sans Pro';
    font-size: 18px;
    font-weight: 600;
    line-height: 26px;
    letter-spacing: 0em;
    text-align: left;
    margin-bottom: 10px;
}

.tags .tag {
    padding: 5px 10px;
    border-radius: 21.6px;
    text-align: center;
    background-color: #F0F1FE;
    font-family: 'Source Sans Pro';
    font-size: 10px;
    font-weight: 600;
    line-height: 16px;
    letter-spacing: 0em;
    margin-right: 20px;
    margin-bottom: 32px;
}

.memoji-box {
    height: 45px;
    width: 45px;
    border-radius: 50%;
    background-color: #F0F1FE;
    margin-right: 10px;
}

.author .name {
    font-family: 'Source Sans Pro';
    font-size: 14px;
    font-weight: 600;
    line-height: 22px;
    letter-spacing: 0px;
    text-align: left;
    color: var(--black);
    position: relative;
}

.name::after {
    position: absolute;
    right: -20%;
    bottom: 20%;
    content: "";
    transform: translate(-50%, -50%);
    width: 6px;
    height: 6px;
    background-color: var(--secondary);
    border-radius: 50%;
}

.author .publish-time {
    font-family: 'Source Sans Pro';
    font-size: 10px;
    font-weight: 400;
    line-height: 16px;
    letter-spacing: 0em;
    text-align: left;
    color: var(--secondary);
}

.data-info {
    width: 345px;
    font-family: 'Source Sans Pro';
    font-size: 14px;
    font-weight: 400;
    line-height: 22px;
    letter-spacing: 0px;
    text-align: left;
    color: var(--secondary);
}
<<<<<<< HEAD
</style>
=======
</style>
>>>>>>> dev
