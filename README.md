# Vue3.0 常规图形验证码

#### 介绍
Vue3.0 常规图形验证码 
仅有简单英文+数字的 最常规的4位验证

  超简单仅限前端验证用   
通过网上原生的js修改过来的  
 小项目临时用还是够的 
看后面有空的话会更新题库模式的

#### 说明
2021.3.12 自己要用个简易的验证码组件  

网上找到的都是vue2.0的  

索性自己百度加工了下搞了个vue3.0的凑合用下


顺便发出来 给需要的人参考使用

#### Vue3.0使用此组件


1、复制 仓库内的 PicCode 文件夹 到你vue3.0项目的 src/components/ 文件夹下

2、 参考下面示例代码

```
<template>
  {{ Code }}
  <PicCode :width="200" :height="60" v-model:Code="Code" />
</template>

<script lang='ts'>
import { defineComponent, reactive, ref } from "vue";
import PicCode from "@/components/PicCode/PicCode.vue";

export default defineComponent({
  components: { PicCode },
  setup() {
    const Code = ref(1);
    return {
      Code,
    };
  },
});
</script>

<style>
</style>
```
Code为生成的验证码文本内容   用作对比验证码是否输入正确
其他的没啥了吧，使用挺简单的  
小项目凑合用吧!


#### 效果示例：
![效果示例](https://images.gitee.com/uploads/images/2021/0312/002903_6bcdada1_2040311.png "效果示例")