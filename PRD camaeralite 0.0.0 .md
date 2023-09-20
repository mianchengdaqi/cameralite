
> # 07.26 栾尚君 创建文档
> 
> # 07.27 补充流程图 和 原型说明
> 
> # 07.28 补充B类原型 和 上传图片质量打分-文案显示细节 重置规则细节 lora生成细节

# 概述

## 流程图

This content is only supported in a Feishu Docs

## 预计实现内容

1 页面 `8A`+`7B`+`1C`+`3D`;

2 服务 `数字分身排队机制` , `图像生成排队机制` ,`用户注册登录`，`钻石充值消费`，`微信订阅通知`；

3 数据 `用户·数字分身资产表`,`用户·照片资产表`, `用户·钻石资产表`, `用户·钻石消费表`;

4 算法 `盲盒生成指令` , `更像我指令` ，`更换模板指令`, `更换动作指令` ，`自定义图片动作指令`;

5 未定义 `可用性识别`， `上传图片的质量识别` ；

## 原型页面

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=ODAxMTQ1MDQwNWRmNzllYmM3NGEyZDUyOTJkMmQ1ZGZfdGw2aVpSYWRYNDBiajlDNjNDNjd1dXFwTGNhcW80T3hfVG9rZW46SHFDT2JRUnI2b04zRzZ4RmpnS2NQeHk5bkRlXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

# STEP1 制作数字分身

## A1 首页

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDdjMjhjODU5NjZhNDgzM2ExNzJlMThkZjA4ZjI1OWVfS2IxU0VjbWlIVzI3T3ZsUVNIMmhYcDhIY3JuYlNUTFhfVG9rZW46VlJVcWJadTVQb1VrSnF4SEk5OWNHOGV6bmdoXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

**说明：**

1. 上·轮播区：展示轮播图照片，duration 5s/张，9张循环；照片以效果图为主，真实照片固定展示在左下方；
    
2. 中·示例区：展示三个step的示例gif，共三个step：`STEP1 制作数字分身；STEP2 生成写真 ；STEP3 精修下载 ；`
    
3. 下·操作区：
    
    1. 主Button：`继续制作数字分身`，点击进入`A2 上传头像页面`；
        
    2. 副Button： `了解妙鸭`,点击进入`B1了解详情`页;
        

  

**文案：**

上·轮播区：

```Plain
封面照经本人授权使用
真实照片
```

中·示例区：

```Plain
STEP1 制作数字分身
STEP2 生成写真
STEP3 精修下载
```

下·操作区:

```Plain
继续制作数字分身
了解妙鸭
```

  

## A2 上传头像页面

上传

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=MTU1YmM2ZjhkODU5ZDMyMjAyYWY2NmZjYmI1MmExMDZfektvbWNTNGFXZjlCNDVUbVlsM3JvV09wWDdTZ24wV0VfVG9rZW46Q2YyVmJQZlZCb1poSm94U3FJNmNzcjc0bmhkXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=N2Q2NjgxMzc1NTlmZWY2NjZjYTI5NzdlMWZlOWNmYjhfUDBXTU9ua2dzM0k3aVRrdjdWNjdkNmhXN1N3ZU56N1hfVG9rZW46VjhjS2JMcGJ0bzJZbDl4NEMzNmNiMmlrbnZjXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=MWUzOGI0NmNjNDc2N2I2YmM2MTk5NjdiMTk2YTY2MjJfMm9zZkF5OWdBQUhGeDVFM1Nrc2RBVFRNd2lneXU0bGNfVG9rZW46UGhkb2JjZjRzb2pNNnN4VjNlUWNzQUtvbm9kXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

通过

失败

  

**说明**：

页面

1. 上· 操作区：标题文案'上传正面照片'，点击`空白区`或`添加一张正面照片`，进入照片选择器；
    
2. 下· 示例区：展示1个正确示例，3个错误示例：√`五官清晰；`，× `不是正面`, × `有遮挡`, × `过于模糊`,
    

### -可用性识别

1. 上传后的图片会进行`可用性识别`，
    
    1. 识别结果为`成功且可能有IP问题`时，将`识别结果` 和 `识别信息`展示在图片下方，可进行`下一步`或`重新上传`；
        
    2. 识别结果为`成功`时，直接进入`A3 上传二十半身照`页面；
        
    3. 识别结果为`失败`时，只能进行`重新上传`。
        

**文案：**

上 · 操作区

```Plain
1 上传正面照片 - 1张五官2清晰的正面照片 | 2 补充至少20张照片 - 上传半身照效果最佳
请确定您对上传的照片拥有合法使用权利或已取得合法授权
添加1张正面照片
```

下· 示例区

```Plain
照片示例 √五官清晰，× 不是正面, × 有遮挡, × 过于模糊,
```

识别

```Plain
toast：上传成功 识别成功 识别失败
图片识别中，请耐心等待
识别成功：xxxxx
正面照片识别失败：未能识别到人脸，请尝试换一张你的面部五官清晰的半身照片哦
这张照片可能为明星哦：请确定您对上传的照片拥有合法使用权利或已取得他人合法授权，否则您将依法承担责任哦
button：我确定,进行下一步 | 重新上传正面照片
```

## A3 上传二十半身照

上传

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=MzdlZDc1NjBjNjkyNTEyMWQwYjkzMjFiNmNjN2Q1ZDRfMHhHM0t4eHREaWFkUklOYlhuTWZzWUpBem5kSDA5eUxfVG9rZW46UENLdWJ4RnFvbzNZMDF4bk4xV2NEQWRyblVnXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=Nzk2NjkxYTYxNjU4MWZhYWY4MzlhYzhlNjYxMjAyMzVfM1p5Zm9rUmZzd3l2WmJ4QURtMnVYTWpja0pVdktReHlfVG9rZW46S1NMWWJMYUhzb3Z6Umt4cFFjeGNMS2lhbkIyXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=YmI1MGFlZDY5NzMyMmZmMGYxNTgwYTA2MTdhYzFiNTFfZWxNMmtQbWJYWkk4dVZqUDJDT2xGMFVqZWxaN0k0WWRfVG9rZW46WTlhbWIwZGFqb0N4VEF4TjN5QWNvdFE3bnllXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

识别

  

通过

  

  

**说明：**

页面

1. 上· 上传区：点击`补充上传至少20张照片`,进入`B2 图片选择器`， 选择后进行上传并进行 `上传图片的质量识别`
    
2. 中· 示例区：分两层，第一层展示3个正确示例 ，第二层展示4个错误示例；
    
3. 中· 结果区：分三层，第一层展示`上传是否可用`信息，第二层展示`已合格的图片`，第三层展示`识别失败`图片；
    
4. 下· 操作区：
    
    1. `补充上传`/`继续补充上传`：调起 `B2 图片选择器`继续上传用于识别的图片；
        
        1. 补充上传暂无上限
            
    2. `马上生成`：调起`微信扣费`,扣款成功后，进行LoRa训练排队，进入`A4 排队页面`;
        

  

### -上传图片质量识别

1. `上传图片的质量识别` ：根据在A2上传的正面照片不在后续上传的半身照中，则不通过；
    
2. 对图片识别并标注通过及不通过，
    
    1. 当通过的图片数量不足时，不可进入生成，可以`补充上传`;
        
    2. 当通过的图片数量充足时，`显示质量打分`，可点击`马上生成`，仍可以`继续上传补充`；
        
3. 在中· 结果区 中的第一层 `上传是否可用` 信息的文案`恭喜质量超过XX%用户`中,
    
    1. 在识别通过的图片达`20`张时,显示超过`80%`用户；
        
    2. 在识别通过的图片达`30`张时,显示超过`90%`用户；（90%以前，+`1.0%` per `1`张）
        
    3. 在识别通过的图片达`35`张时,显示超过`92%`用户；（90%以后，+`0.5%` per `1`张，进度只取整数部分）
        
    4. 在识别通过的图片达`40`张时,显示超过`95%`用户；
        
    5. 在识别通过的图片达`45`张时,显示超过`97%`用户；
        
    6. 在识别通过的图片达`50`张时,显示超过`100%`用户；（直到100%）
        

  

### - 数字分身LoRa训练机制

1. 根据上传的图片进行LoRa训练，在`14`轮epoch训练中，取`6`、`8`、`10`、`12` 共`4`个阶段的模型作为可使用的`数字分身LoRa`（单个LoRa大小`30M左右`，4个120M，个人用户在重置时可能存在最多`8`个LoRa）;
    
2. 根据`4`个阶段的模型，生成`4`张黄色背景的人像图片，作为数字LoRa的封面，在`B7 我的数字分身`中展示；
    
3. 选择第`10`epoch的模型作为默认数字分身，
    
    1. 作为`B7 我的数字分身`的`默认展示封面`；
        
    2. 据此生成 `3`套12张主题照片，在`A5 生成结果列表页`作为`默认展示照片`；
        
4. 可能存在`4`阶段的`数字分身LoRa`均不达标,`审核`在此时`拒绝通过`,用户`数字分身制作失败`;
    

  

## A4 排队页面

排队

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=MDY2NWU3MzgzMmJiOGUwZTBmNjliZWMyNzNjOGM1MDJfalhOa2l5SGVQR2tFWG1mNXhoMjB5bHJLYkVEQXFmb05fVG9rZW46SnhXZWJVcGdab3dhWDh4Y0gxcmNybUhpbmwxXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=NGFlZTlkYmI4MWRmMTU2MGNlM2RlZmQ5MWMzZjRlMmRfSFU3YWlUQ1VFM2Q4UFBNbTN4Q09qMHpnMHJXUjhVRXFfVG9rZW46RU1DaWJlWGRmbzZNdGJ4ajRLNmM4Zllibkt4XzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

制作

  

**说明：**

页面

1. 上· 进度区：展示LoRa训练进度信息；
    
2. 中· 动效区：展示之前的20张图片的浮动照片墙动效；
    
3. 下· 操作区：开启进度通知的Button 及开启说明；
    

  

### - 数字分身排队机制

1. `数字分身排队机制` ：
    
2. 排队信息：登记未完成人数`X`，LoRa数字人生成时间`10`分钟，服务器并行处理`B`个数字人生成人物，需要`T`时间，`T=10X / B` ,T换算为`n1`时 `n2`分 `n3`秒;
    
3. 正在制作：`10`分钟倒计时
    

  

**文案：**

上· 进度区

```Plain
你前面有{X}个人正在制作数字分身 - 预计需要{n1}小时{n2}分 
正在为你制作数字分身 - 预计需要{n2}分{n3}秒
```

下· 操作区

```Plain
您可开启通知，退出小程序等待，制作完成会第一时间通知您
Button：开启进度通知
```

# STEP2 生成写真

## A5 生成结果列表

初见

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=YmYxNDAwMzkyMjk2ODY2MTQxNjA2NDliYjdlMmJjOWRfdnAzRnBVcVJqRFBDbHBHb3M1bnpzZGlqSjRld2RjaDJfVG9rZW46RnlLRmJiWG05b0tsYjd4MDhIbGNzUHFibnZlXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=NDZkZWYyYTk5MGQ1ZGZlYTE4NTFjYWJmMDkxMzgxOGFfeWhCbmFqUFVRU1ZpR2M5NlladnMzU0IwV3JqTmJxYnVfVG9rZW46QThBNGI1N3A2bzhmS094SzN0T2N6ZHlDbjFnXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=M2M0ZDM2YjY2NmYzN2IyNWI3OTQ1NTRmZjQ0NzRhMTBfNUpkZDB5SElvcGk0bkV5ekJJT3NIZFN4anpvMnYwQTZfVG9rZW46UTVzZ2J5dTYyb0JYUUF4Yjl1N2Nka3lnbkNoXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

再见

  

删除

  

**说明:**

页面

1. 上· 基本信息 ：
    
    1. 展示头像，
        
    2. 在头像右侧展示 按行展示
        
    3. 标题`我的数字分身`,`生成时间`,`重置`
        
        1. 我的数字分身跳转`B7`,
            
        2. 点重置，暂时`保留所有用户分身和照片资产`数据，重新进入`A1` 开始生成分身的流程,当进入`A5`并`新的数字分身LoRa`生成，用户可以选择`覆盖旧LoRa` 或 `放弃新LoRa`;
            
            - 在用户做出选择后，`删除对应的用户分身和照片资产`；
                
    4. `钻石余额`,`去充值>`
        
2. 中· 作品展示：tab切换 + 照片墙
    
    1. tab切换： `我的收藏` 和 `生成历史`；
        
    2. 照片墙：我的收藏-瀑布流，生成历史-按每行4张展示；
        
        1. 点击照片墙中的`查看` 或 `图片`时，进入`A8 写真作品页面`;
            
        2. 点击照片墙中的`删除`,二次确认后,删除整行作品;
            
    3. 在初次进入页面时，tab切换区只显示`已为你生成3组主题写真`,照片墙展示`生成历史`的照片墙；
        
3. 下· 操作区：
    
    1. Button`制作更多写真`,点击进入`A6 写真模板主题列表`
        
    
      
    

  

**图片资产**

1. 默认生成4套主题图片，每套4张照片，
    
    1. 在第一次进入页面时，奢感光 清欢 都市正装 主题照 3套；
        
    2. 在点击头像时，进入`B7我的数字分身`可以看见 数字分身 主题照 1套；
        
2. 当做过 收藏 或 生成 操作，再进入生成结果页时，会有`我的收藏` 和 `生成历史`两个tab；
    
    1. 在内容为空时展示空内容的底图；
        

  

### - D1 钻石充值页面

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=OGNhZThiOTI1YWFjNmIyODFmZmI0YjZmNGNkNmRmZTlfRU1jWGg3ZzlYOGpxN0szN29na2g5SHFJN1BUNG05RXpfVG9rZW46Q2lSMWJlQzY1b1ZPOTl4VkRoQ2N1c2U5bklmXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

|   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|
|钻石|60|200|360|880|2400|5000|
|价格|6|18|30|68|168|328|
|折扣|-|9折|8.3折|7.7折|7折|6.6折|

**文案**

```Plain
钻石可用于高清化、下载原图、不能制作数字分身
Button： ￥{价格} 立即充值
充值即同意 《妙鸭钻石充值协议》
```

  

## A6 写真模板主题列表

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=NDU1MDQxMGNkNGQ2MTAzMTZhNmY1MzI0YmM0ZDQ0NGJfdDVwa1UyVE0yeVNjb1hJbXRHNktvZXVEMTQ1Z3ZHd0VfVG9rZW46TWZaTmJrcUJUb2RJNzF4dWxQb2N6VDdDbm5lXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

**说明：**

就是个图文列表，展示所有`主题`，没啥好说的，点击图片，会进入`A7 写真模板风姿选择`页面

|   |   |   |   |
|---|---|---|---|
|#|名称|描述|备注|
|1|千年 \| 大时代|王家卫花样年华|限免|
|2|千年 \| 新青年|民国校服|限免|
|3|千年 \| 瑞宫春|甄嬛传|限免|
|4|千年 \| 桂殿秋|红楼传 林黛玉|限免|
|5|千年 \| 太平乐|知否知否+清平乐|限免|
|6|晚秋|明星脸低饱和背景肖像|男|
|7|羽翼|光感、景深、羽衣飘发（漂浮感）||
|8|职场|职装照，黑白西装||
|9|情绪|海马体||
|10|江南|古装 海马体||
|11|焦点|侧光 纯底肖像|男|
|12|清欢|素底 肖像 张嘴||
|13|情书|张曼玉-喜剧之王 水手服 露齿||
|14|都市正装|海马体 证件照||
|15|氧气|瑜伽 居家||
|16|奢感光|光影 头顶打光||
|17|森林|大光圈虚化背景||
|18|旺角|红衣礼服 性感||
|19|春日|粉衣战神||
|20|青苹果|王菲||
|21|韩潮|都敏俊||
|22|白衣|男偶像||
|23|冷杉|不知道||
|24|南法假日|仙女 魔法发带||
|25|油画|油画色调 choker||
|26|桃夭|三生三世十里桃花+网红脸||
|27|林间|移轴？||
|28|初见|异域风格衣服，黑底||
|29|森林之子|翅膀 头顶光 绿衣 虚化||
|30|纯白梦境|头花 腮红 白衣 白底||
|31|暗夜萤火|哥特萝莉 腮红 choker||
|32|黄金蝴蝶|黄金 蝴蝶||
|33|浪漫配方|粉色 头饰||
|34|牛仔|飒 牛仔上衣 纯色底 正面光 迎风||
|35|极简正装|律师 中介 银行柜员 风格正装||
|36|回到童年（女）|白底 鞭子 蝴蝶结||
|37|回到童年（男）|白底 蓝底 童装照|男|
|38|正装（男）|高对比正装|男|
|39|摩托日记|林志颖+郭富城 机车||
|40|默片|邓超 中长发 黑白特写||

  

## A7 写真模板风姿选择

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=NDBiM2UwODYzNDVkMDE4NDljMzQwMzZhZjdlY2M3ZmJfQVdScUN0R3hjcG9acG5jME5RNW1rWkdGOUxuSGFnQzhfVG9rZW46R25IQmJmMUJHbzZ4dU54VkZ2QWNjM3FVbmVZXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

**说明：**

页面：

（比较简单，略）

功能：

1. 一个`主题`对应多套`风姿`,每套`风姿`，对应一套SD中的参数
    
    1. prompt中的非LoRa部分的信息
        
    2. ControlNet的信息
        
    3. 采样参数的信息
        
2. 点击`立即生成`，执行图像`生成指令`，进入`C1 生成写真页面`：
    
    1. 生成4批次图片（注意并非一批4张）；
        
3. 当选择`盲盒` 风姿时，会再多套风姿信息中做随机选择，用于后续的图片生成中；
    
4. 当选择`自定义` 风姿时，会调起`B5 自定义图片选择` ，识别上传图片中的姿态（openpose）信息，并用于后续的图片生成中；
    

  

### - 盲盒生成指令

1. 使用盲盒生成时，不使用指定`风姿`信息进行图像生成；
    
2. 同时，controlnet应该控制在该`主题`下的有`一套openpose姿态列表`中；
    
3. 在具备特定功能，且风格单一的`主题`中（如职装照），不提供`盲盒`选项
    

  

### - 自定义图片动作指令

1. 对上传图片进行`openpose`解析；
    
2. 在执行生成时，替代原`风姿`中controlnet的输入信息，执行图像生成；
    

  

  

## C1 生成写真页面

生成中

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=OWRjNTBlYzRkMjRlOTdmMjBiMjgxNGNmMjljNjBiZDJfY21ubDdpTE83WnBUcWlTSjRBUE9wbjlKUjdmaGZvTFJfVG9rZW46VlhieGJnS0Y2b1htWmp4VUwzb2M0RkdEbkhiXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=YmRjYzIxNTFhODk3YTQ0YTRiMWFlN2I5NWIxM2UzYjZfQXdnZGRLdlg1cTFuQzhLTlJjb3NSeXJGdXF4TDExREtfVG9rZW46WHU3ZWJhdXdIb0VzaXR4YzRqdGN6YzRibnpoXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

生成结束

  

  

**说明：**

页面

1. 上· 配置区：
    
    1. 展示`风姿`图片，在图片右侧展示所属`主题`名称
        
    2. Button：`更换动作` 和 `更换模板` ,在生成过程中为禁用状态；
        
2. 中· 生成区
    
    1. 随生成批次，生成一张，展示一张；否则展示妙鸭相机动态底图；
        
3. 下· 操作区
    
    1. `生成好了通知我`,在 生成中 展示，点击调起`B4 开启制作结果通知`
        
    2. `再次生成`,在 生成结束 显示，点击回到`C1 -生成中`状态；
        

  

### - 图像生成指令

根据用户`选定的数字分身LoRa`信息，

1. `更换动作`:进入A7 模板风姿列表，根据后续`主题不变，重新配置prompt+controlnet等信息`
    
2. `更换模板`:进入A6 模板主题列表，根据后续`重新配置prompt+controlnet等信息`
    
3. `再次生成`/`立即生成`:执行图像`生成指令`
    
    1. 再次生成会删除已生成的4张图片
        
    2. 页面返回不打断（stop） 生成执行进程；
        
4. `我想更像我一点`：调整`数字分身LoRa权重`，权重`1.0 →1.1`，依次类推`1.1 →1.2`,到`1.5封顶，不再增加权重`；
    

  

### - 图像生成排队机制

# 图像生成定义：携带用户的`数字分身LoRa`信息的图像4批次生成任务；

1. 每个任务要完成4批次图像生成后，执行下一用户的图像生成任务；
    
2. 排队信息：登记未完成任务数`X`，LoRa数字人生成时间`1.5`分钟，服务器并行处理`B`个数字人生成人物，需要`T`时间，`T=1.5X / B` ,T换算为`n1`时 `n2`分 `n3`秒;
    
3. 正在制作：`1.5`分钟倒计时
    

# STEP3 精修下载

## A8 写真作品页面

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=M2UzZjQ3NGQzYTFiNzQ2NTZkNTNiMTFiY2ExMzJkMjJfM3laSDhSaWdyemJ6d2JGV2FlVzNvR2JFaHFZQktZSVVfVG9rZW46QUVkSmJWOUY4bzF3UWN4dU5FdWNndnQwbk1lXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

**说明：**

页面

（如图所示）

功能

1. `我想更像我一点`，进入`C1 生成写真页面`,调高数字分身LoRa权重，重新执行生成操作；
    
2. 点击`生成高清版`，`点击下载` ，-2钻，弹层 `D2`,`D3`；
    
3. 点击`分享`+5钻, 调起`B6 作品分享页`;
    

  

钻石消费机制

|   |   |   |   |
|---|---|---|---|
||钻石|执行限制|页面|
|创建账号|+10|每账号1次|-|
|分享|+5|每天 `？` 次|B6|
|生成高清版|-2|余额≥`2`时，每天`不限`次|D2|
|下载|-2|余额≥`2`时，每天`不限`次|D3|
|钻石充值|+N （N为套餐值）|每天`不限`次|D1|

### - D2 高清照片消费

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=N2IwNTcxMTkzZTNhZmU1MzJmNDAyOTI4MDM0OThhNTVfWmNKS3FmQ2tnY3pReVZjaWlvRHRwdVQ3Ym1vR2RvaDJfVG9rZW46UTRMU2JPY1lLb2dkU3R4eTR2Y2NGellsbm5mXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

### - D3 下载照片消费

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=M2VhYmU4Y2U5NTY2MWFmZjBjYTBhZDI1YWE1Y2FiOGZfNGtvUVBIaGE0cjNFV3hYZ2ttWE52bFNndWNDdHBxdExfVG9rZW46SWR6bmI4VUI1b01UeWx4R0lBZWNQZ2ZLbjlnXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

  

# 其他

## B1 了解详情页

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=YTMzMjAwNmUzNmFkYjI3ZjM5ZTkzZDUyMTdmZWViZTJfWklxQm1IT2I3Z1YybGFYbXlHUW9WRjhZbXJFUXVsM0VfVG9rZW46RTdZMGJPSUlmb0JaRm54N2pETmM2UWRUbk5JXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

  

## B2 图片选择器

1. 微信照片选择
    
2. 在`上传头像页面` 中，先选择`拍摄` /`从相册选择`，选择相册后，进入照片选择；
    
3. 在`上传二十半身照`中，直接进入照片选择，最多`20`张;
    

  

## B3 微信扣费

（微信扣费界面）

## B4 开启制作结果通知

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=OTQyNGJhOGNiYWQ1MGM3YWExMmRkNzczZDQzMmZhYmNfdnlZQTBDczcxSTlVamtGTU5sSGdZZFl2TWdPc3d4djhfVG9rZW46T2cwMmI2aDZXb3JKY2N4YjA5V2NacVpiblliXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

|   |   |   |
|---|---|---|
|场景|**1 模型制作**|**2 制作结果**|
|标题|```Plain<br>AI制作结果通知<br>```|```Plain<br>模型制作完成通知<br>```|
|内容-举例|```YAML<br>AI作图主题 清欢<br>AI作图结果 大片已生成<br>完成时间 2023年7月26日 18:29:30<br>```|```YAML<br>制作结果 恭喜！您的形象已经生成<br>温馨提醒 点击查看，立即生成您的专属大片<br>```|

## B5 自定义图片选择

# 似乎可以与B2 合并

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=OWY1M2Q0NTJjNWIwNmU1OGMzMDlmMTdjNThkZjY1ZTVfZVZ3eFpYRmlhN2RlY0lnZjdvODEzczkwYTdzQzhoNTdfVG9rZW46RVZRTmI3NFpxb2dqZUN4ZVVzN2NQTnpxbjRjXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

**说明：**

1. 微信照片选择
    
2. 在`写真模板风姿选择`中`上传自定义图片`时，先选择`拍摄` /`从相册选择`，选择相册后，进入照片选择；
    

## B6 作品分享页

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=MTRhYzJjZGE1N2E4OGFkOTUzYTdjNTgxY2M0OGZlM2VfTEVudXlzVzBSbHZEYXFlcG45RlN6WDM1dThBdVkyWlJfVG9rZW46UHU2WWJ1WlpFb0lRbDh4SndDdGNIc2k3bk9jXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

说明:

1. 根据当前页面的图片生成分享图（图片+小程序码+妙鸭Logo+分享文案），可以进行`转发` 、`收藏` 、`保存` 操作;
    
2. 完成操作,`钻石+5`;
    

  

**文案**

```Plain
这是我数字分身，你也来试试吧
发送给朋友
收藏
保存到相册
```

## B7 我的数字分身

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=Yjg3ZDRlMDcxZDMwY2I2YjMxZDQ0N2Y4NjBjM2Q0Y2VfcndSeDkzanZEald3cTVoYjV0bmF1NVRhbG5POU8zNHhfVG9rZW46T3d2N2J0SklXbzI1ckV4RmVGdmNndTRxblBiXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)

  

  

  

**说明**

1. 默认展示与头像相同图片，可左右滑切换图片；
    
2. 当展示图片与默认图片不同时，可点击`换成这张`；
    
3. 可以`分享`, 调起`B6 作品分享页`
    
4. 可以`下载`,调起`D3 下载照片消费`
    

## 附录

  

![](https://buzakeji.feishu.cn/space/api/box/stream/download/asynccode/?code=ODRiMTA1M2VkMjg5YTMyMDYyODE0OGZiYjU4ZjQ5NWFfVWtTZ1JVN3NNcWtld3c3SjR5WlN3RlV4bHczRkRFZTVfVG9rZW46QmpEZWJQTnR1bzUxMzF4RVBKWWNuY1dqblBNXzE2OTUxOTY0NjY6MTY5NTIwMDA2Nl9WNA)
