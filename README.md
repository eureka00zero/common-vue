# @mfelibs/common-vue-cmnt

玲珑评论组件


#### demo（demo仍然走unpkg服务）
<a href="http://unpkg.smfe.sina.cn/@mfelibs/common-vue-cmnt/dist/demo/index.html" target="blank">http://unpkg.smfe.sina.cn/@mfelibs/common-vue-cmnt/dist/demo/index.html</a>

## cmd 调用方式：

### 安装

```bash
yarn add  @mfelibs/common-vue-cmnt --save
```

通过 `import` 导入
```javascript
import cmntList from "@mfelibs/common-vue-cmnt"
```

### 使用  
可参考[jsdoc](http://unpkg.smfe.sina.cn/@mfelibs/common-vue-cmnt/docs/index.html)

### CHANGELOG
[传送门](https://gitlab.weibo.cn/SINA_MFE_COMPONENTS/common-vue-cmnt/blob/master/CHANGELOG.md)  

#### 测试数据接口（如果还能访问的话）  
[世界杯圈子](http://comment5.sina.cn/cmnt/info?thread=1&channel=qcmnt&newsid=q_forum-1_5AE19C8B-3D879885-7A300FC9-8DA-92C&mid=5AE1E0F1-ADE180B-7A300FC9-7CD-87B&_=1525491356108&callback=jsonp3)  
cmntlist节点 一级评论
threaddict节点 二级评论


## 维护组件方式：  
为规范化组件版本，请确保安装了`commitizen`，若未安装，使用以下命令安装：  
```  
npm install -g commitizen
```  

当组件修改过后，使用以下指令更新：  
``` 
npm run jsdoc // 更新jsdoc文档（如果有更新）
git add .  
git cz // 按提示选择feature 或者fix 或者doc 等等  
// *** （如果是需要发版的提交，依据需求，执行以下之一，更新CHANGELOG，如果不需要发版，略过npm version） ***
npm version patch -m 'commit message' //发小补丁
npm version minor -m 'commit message' //发中版本
npm version major -m 'commit message' //发大版本  
// *** ***
git push
```  