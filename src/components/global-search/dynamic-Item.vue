<template>
    <div class="group-dynamic">
        <!-- 顶部用户信息 -->
        <div class="user-info">
            <img src="https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3744872283,1870099043&fm=27&gp=0.jpg">
            <p class="username">Victoria</p>
            <p class="time">2018-2-5</p>
        </div>
        <!-- 内容区域 -->
        <div class="dynamic-content-box mb20">
            <!-- 文本 -->
            <p class="dynamic-content">
                model 3 今天给预约了的老车主参观，趁着有时间就过去看啦，感觉还不错。 大雄，作业交完了😁😁不要嫌我文笔差哈……
            </p>
            <!-- 图片 -->
            <div class="img-list">
                <ul>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                </ul>
                <p class="total">8</p>
            </div>
        </div>
        <!-- <OnePxLine /> -->
    </div>
</template>
<script>
export default {};
</script>
<style lang='less' scoped>
.group-dynamic {
  // 用户信息
  .user-info {
    display: flex;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-items: center;
    font-size: 10px;
    color: #858585;
    margin-bottom: 16px;
    img {
      display: inline-block;
      width: 20px;
      height: 20px;
      border-radius: 100%;
      margin-right: 9px;
    }
    .username {
      font-size: 14px;
      color: #333333;
    }
    .time {
      flex: 1;
      text-align: right;
    }
  }
  // 内容区域
  .dynamic-content-box {
    width: 100%;
    padding: 10px;
    background: #fafafa;
    // 文本
    .dynamic-content {
      font-size: 13px;
      color: #333333;
    }
    // 图片列表
    .img-list {
      position: relative;
      top: 0;
      ul {
        display: flex;
        flex-wrap: nowrap;
        justify-content: flex-start;
        margin-top: 10px;
        li {
          width: 77px;
          height: 77px;
          background-image: url("http://i4.article.fd.zol-img.com.cn/g5/M00/04/03/ChMkJlpgPuGISF3iAAFxP3ckvFkAAkLfgGYMngAAXFX214.jpg");
          background-size: cover;
          background-position: center;
          margin-right: 5px;
        }
        li:last-child {
          margin-right: 0 !important;
        }
      }
      .total {
        position: absolute;
        right: 5px;
        bottom: 0;
        font-size: 12px;
        color: #fff;
      }
    }
  }
}
.mb20 {
  margin-bottom: 20px;
}
</style>