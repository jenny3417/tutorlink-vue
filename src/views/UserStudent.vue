<template>
  <navbar></navbar>
  <div class="wrap">
    <div class="myLearn">
      <img class="head" src="../assets/icon/user.png" />
      <h1 class="myLearn">我的學習</h1>
      <router-link to="/member/teacher"><n-button type="info">切換老師</n-button></router-link>
    </div>
    <br />
    <div class="quickLink">
      <div>
        <router-link class="routerLink" to="/member/student/studentlesson"><img src="../assets/icon/lesson.png" alt=""
            style="width: 30px" />
          <div>我的課程</div>
        </router-link>
      </div>
      <div>
        <router-link class="routerLink" to="/member/student/favoriate" @click=""><img src="../assets/icon/favorite.png"
            alt="" style="width: 30px" />
          <div>我的收藏</div>
        </router-link>
      </div>
      <div><router-link class="routerLink" to="/member/student/exercise"><img src="../assets/icon/blackboard.png" alt=""
            style="width: 30px" />
          <div>我的作業</div>
        </router-link>
      </div>
      <div>
        <div class="routerLink"><img src="../assets/icon/schedule.png" alt="" style="width: 30px" />
          <CalendarButton></CalendarButton>
        </div>
      </div>
      <div><router-link class="routerLink" to="/member/student/videocourse"><img src="../assets/icon/youtube.png" alt=""
            style="width: 30px" />
          <div>我的影音</div>
        </router-link>
      </div>
      <div>
        <router-link class="routerLink" to="/member/student/beteacher"><img src="../assets/icon/teacher.png" alt=""
            style="width: 30px" />
          <div>成為老師</div>
        </router-link>
      </div>


    </div>
  </div>
  <router-view></router-view>
</template>

<script setup lang="js">
import Navbar from "@/components/public/Navbar.vue"
import CalendarButton from "../components/calendar/CalendarButton.vue";
</script>

<style scope>
.myLearn h1 {
  padding-left: 20px;
}

.wrap {
  display: block;
  position: relative;
  width: 100%;
  padding: 100px;
  margin: 0% auto;
  background-color: rgb(45, 43, 43);
  padding-left: 25%;
  padding-right: 25%;
}

.head {
  max-width: 100px;
  max-height: 100px;
  border-radius: 50%;
  border: solid;
  border-width: 3px;
  border-color: #fff;
  background-color: white;
}

.myLearn {
  display: inline;
  color: white;
  border-color: white;
  vertical-align: middle;
  font-weight: bold;
}

.quickLink {
  position: absolute;
  bottom: 2px;
  left: 25%;
  right: 25%;
  font-size: 25px;
  display: flex;
}

.routerLink {
  display: flex;
  margin: 10px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-bottom: 5px solid rgb(45, 43, 43);
}

.routerLink:hover {
  margin: 10px;
  /* color: rgb(165, 174, 189); */
  font-weight: bold;
  /* transition: all; */
  /* transition-duration: 0.5s; */
  border-bottom: 5px solid rgb(75, 180, 148);
}

.routerLink:focus {
  border-bottom: 5px solid rgb(230, 235, 234);
}

body::-webkit-scrollbar {
  display: none;
}
</style>
