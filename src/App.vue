<template>
  <div id="app">
    <div class="test">
      <span class="icon"></span>
      <span class="text">介绍</span>
    </div>
    <div class="test">
      <span class="success-icon"></span>
      <span class="text success-text">安装部署成功</span>
    </div>
    <div class="test">
      <span class="fail-icon"></span>
      <span class="text fail-text">安装部署失败</span>
    </div>
    <div class="input-box">
      <div class="require"></div>
      <div class="text">操作用户名</div>
    </div>
  </div>
</template>

<style lang="less">
*{
  margin: 0;
  padding: 0;
  list-style: none;
}
.test{
  margin-left: 80px;
  margin-top: 20px;
  color: #3e748f;
  font-size: 14px;
  .text{
    margin-left:5px;
  }
  .icon{
    display: inline-block;
    height: 18px;
    width: 18px;
    background-color: skyblue;
    border-radius: 50%;
    position: relative;
    top: 4px;
  }
  .icon::after{
    content: '';
    height: 2px;
    width: 2px;
    border-radius: 50%;
    background-color: white;
    position: absolute;
    top: 4px;
    left: 8px;
  }
  .icon::before{
    content: '';
    height: 7px;
    width: 2px;
    background-color: white;
    border-radius: 4px;
    position: absolute;
    bottom: 3px;
    left: 8px;
  }
  /* 部署成功*/
  .success-text{
    color: #499c54;
  }
  .success-icon{
    display: inline-block;
    height: 14px;
    width: 14px;
    background-color: #499c54;
    border-radius: 50%;
    position: relative;
    top: 3px;
  }
  .success-icon::after{
    content: '';
    height: 4px;
    width: 1px;
    background-color: white;
    position: absolute;
    top: 7px;
    left: 4px;
    transform: rotate(130deg);
    border-radius: 4px;
  }
  .success-icon::before{
    content: '';
    height: 8px;
    width: 1px;
    background-color: white;
    position: absolute;
    top: 3px;
    right: 5px;
    transform: rotate(35deg);
    border-radius: 4px;
  }
  /* 部署失败 */
  .fail-text{
    color: #d24444;
  }
  .fail-icon{
    display: inline-block;
    height: 14px;
    width: 14px;
    background-color: #d24444;
    border-radius: 50%;
    position: relative;
    top: 3px;
  }
  .fail-icon::after{
    content: '';
    height: 7px;
    width: 2px;
    background-color: white;
    border-radius: 4px;
    position: absolute;
    top: 2px;
    left: 6px;
  }
  .fail-icon::before{
    content: '';
    height: 2px;
    width: 2px;
    border-radius: 50%;
    background-color: white;
    position: absolute;
    bottom: 2px;
    left: 6px;
  }
}
/* 输入框必填样式*/
.input-box{
  font-size: 14px;
  margin-left: 80px;
  color:#d24444;
  margin-top: 20px;
  position: relative;
  div{
    display: inline-block;
  }
}
.require{
  position: absolute;
  top:3px;
  left: 0;
}
.text{
  padding-left: 10px;
}
.require::after{
  content: '*';
  font-size: 14px;
  color: #d24444;
  left: 0;
}

</style>
