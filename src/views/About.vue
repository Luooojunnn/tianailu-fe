<template>
  <div class="about">
    <div style="display: flex;align-items: center;flex-direction: column;padding: 10px;background: #ff6923;">
      <div><img style="width: 80px;" src="../img/logo.png" /></div>
      <div style="color: white;font-size: 22px">陈奕迅</div>
      <div
        style="background: #434343;color: #dcdcdc;padding:4px 8px;margin-top: 10px;border-radius: 14px;border: 2px solid #dcdcdc"
      >
        分享我的名片
      </div>
    </div>
    <div style="background: white;border-radius: 10px;margin: 8px;display: flex;justify-content: center;">
      <div
        style="border: 1px solid #9a9a9a;display: flex;justify-content: space-around;line-height: 40px;width: 80%;border-radius: 20px;"
      >
        <div style="border-bottom: 2px solid black">基础资料</div>
        <div>择偶条件</div>
      </div>
    </div>
    <template v-if="card == 'mine'">
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>通讯信息（必填）</div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">微信</div>
          <div class="item"><el-input placeholder="请填写你的微信（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">手机</div>
          <div class="item"><el-input placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
      </div>
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>基本信息</div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">姓名</div>
          <div class="item"><el-input placeholder="请填写你的姓名"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">性别</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">生日</div>
          <div class="item"><el-date-picker type="date" placeholder="请选择生日"></el-date-picker></div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">身高</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">体重</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">学历</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">毕业院校</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">车房情况</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">公司性质</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">工作</div>
          <div class="item"><el-input placeholder="请填写你的姓名"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">年收入</div>
          <div class="item"><el-input placeholder="请填写你的姓名"></el-input></div>
        </div>
      </div>
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>家庭情况</div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">家乡</div>
          <div class="item"><el-input placeholder="请填写你的微信（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">家庭情况</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
      </div>
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>婚姻情况</div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">婚姻情况</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option label="男" value="男"></el-option>
              <el-option label="女" value="女"></el-option>
            </el-select>
          </div>
        </div>
      </div>
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>介绍自己</div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">个人情况</div>
          <div class="item"><el-input placeholder="请填写你的微信（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="color: #505050">兴趣爱好</div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="width: 100%"><el-input type="textarea" placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="color: #505050">描述自己的性格</div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="width: 100%"><el-input type="textarea" placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="color: #505050">你的未来规划</div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="width: 100%"><el-input type="textarea" placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="color: #505050">你的爱情观和价值观</div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="width: 100%"><el-input type="textarea" placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
      </div>
      <div style="background: #9a9a9a;padding: 10px 40px;color: #505050;font-weight: bold;">
        <div>用户相册（最多上传5张）</div>
      </div>
      <div style="padding: 10px 40px;">
        <div>
          <el-upload
            class="upload-demo"
            action="https://jsonplaceholder.typicode.com/posts/"
            :on-preview="handlePreview"
            :on-remove="handleRemove"
            :before-remove="beforeRemove"
            multiple
            :limit="5"
            :on-exceed="handleExceed"
            :file-list="fileList"
          >
            <el-button size="small" type="primary">点击上传</el-button>
            <div slot="tip" class="el-upload__tip">只能上传jpg文件</div>
          </el-upload>
        </div>
      </div>
    </template>
    <template v-if="card == 'demand'">
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="color: #505050">期望的他</div>
        </div>
        <div style="display: flex;justify-content: space-between;align-items: center;margin-top: 10px;">
          <div style="width: 100%"><el-input type="textarea" placeholder="请填写你的手机号（必填）"></el-input></div>
        </div>
      </div>
      <div style="padding: 10px 40px;">
        <div style="display: flex;justify-content: space-between;border-bottom: 1px solid #e1e1e1;align-items: center;">
          <div style="color: #505050">身高</div>
          <div class="item">
            <el-select v-model="value" placeholder="请选择">
              <el-option :label="i + 119 + 'cm'" :value="i + 119" v-for="(i, key) in 100" :key="key"></el-option>
            </el-select>
          </div>
        </div>
      </div>
    </template>
  </div>
</template>
<style scoped>
body {
  margin: 0;
  font-family: "Microsoft YaHei", 微软雅黑, "Microsoft JhengHei";
}
.el-input__inner {
  border: none;
}
.el-input__prefix {
  display: none;
}
.item {
  width: 210px;
}
.el-input--prefix .el-input__inner {
  padding-left: 15px;
}
</style>
<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Home",
  components: {
    // HelloWorld
  },
  data() {
    return {
    message: "vue",
    card: "demand",
  }
  }
};
</script>
<style scoped></style>
