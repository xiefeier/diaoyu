<template>
  <div class="content_box">
    <div class="content_out">
      <h3>异常行为登录警告</h3>
      <span id="time" v-once>{{ '今天 ' + hour + ':' + sec }}</span>
      <br>
      <div class="who">清华大学用户:</div>
      <p class="content">
        网盾系统监测发现,你的账号存在境外可疑地区多次登录的异常情况，可能已经泄露个人重要信息!
      </p>
      <p class="content">请遵照以下操作指南尽快更新账号密码，以免给个人和学校造成损失!</p>
      <a href="" class="link">专用链接</a>
      <br>
      <div class="info">
        <span>IT技术部门</span>
        <span>2021年12月1日</span>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'App',
  components: {

  },
  setup() {
    const time = new Date()
    let hour = time.getHours()
    let sec = time.getMinutes() 
    sec=sec>9?sec:"0"+sec
    return {
      hour,
      sec
    }
  },
}
</script>

<style type="text/css" lang="less">
.content_box {
  display: flex;
  justify-content: center;
  align-items: center;
}

.content_out {
  height: 450px;
  width: 364px;
  border: 3px solid black;
  .link{
    margin-left: 20px;
  }
  h3 {
    margin-left: 20px;
    margin-top: 40px;
    margin-bottom: 5px;
  }

  #time {
    margin-left: 20px;
    color: gray;
    font-size: 0.9rem;
  }
  .who{
    margin: 20px 20px 0 !important
  }
  p {
    margin: 0;
    margin-left: 20px;
    margin-right: 20px;
    line-height: 1.5rem;
    text-indent: 2rem;
  }

}

.info {
  margin-top: 20px;
  margin-left: 20px;
  width: 120px;
  font-weight: bold;
  span {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}</style>