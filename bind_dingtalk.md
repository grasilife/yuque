# 绑定钉钉登录

本文所描述的钉钉操作，只能由 __钉钉企业管理员 __进行。
完成此绑定后，在钉钉本企业通讯录中的所有员工可以直接用钉钉扫码登录语雀，无需注册。

整个过程需要两步操作。

## 第一步 : 创建企业内部 App

打开语雀企业后台管理，进入企业设置，在左边导航栏找到「钉钉登录」功能，注意下图的红框中logo地址和回调域名后面需要在钉钉开放平台中填写

![image.png | center | 832x454](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/8ad28a29-7a92-4254-9b6a-7cd3218c079b.png "")

再到 [钉钉开放平台 - 自助工具](https://open-dev.dingtalk.com/#/loginAndShareApp) 页面，点击「创建扫码登录应用授权」按钮，进行应用创建。

![image.png | center | 832x268](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/73c695f7-6f79-49d9-9c12-d0abbb27e1f6.png "")

将语雀提供「授权 LOGO 地址」和「回调域名」复制到下面的页面信息中, 并输入名称和描述，这里的名称和描述也可以复制语雀「绑定钉钉登陆」页面里面给你生成的名称和描述。

![image.png | center | 752x371](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/3c1b22a1-3284-4a11-be23-2e341569bac6.png "")

点击「确定」后，会在应用列表中出现一条新的记录。

![image.png | center | 832x233](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/78504601-9cc0-41d7-b832-a98bf118fc22.png "")

复制的 appId 和 appSecret 到语雀「绑定钉钉登陆」页面相对应的输入区。
![image.png | left | 471x367](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/b2220028-01a9-444d-95e3-0b65efc8d5e3.png "")
## 第二步 : 生成新的企业内部 CorpSecret

到 [钉钉开放平台 - 开发账号管理](https://open-dev.dingtalk.com/#/corpAuthInfo) 页面，生成 Corpid 和 CorpSecret

如下图，Corpid 直接复制红框内的 Corpid 即可，CorpSecret 则需要先点击下图蓝框中按钮

![image.png | center | 832x532](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/add5239a-fcf2-45ed-bd65-301ed9706e32.png "")

在「生成CorpSecret」弹出中输入相对应的名称，比如“企业知识库”，在关联部门中选择点击“通讯录”，选择整个企业。
在「__服务器公网出口 IP 白名单」__填写以下 IP 地址：

```plain
101.132.237.39
```

<span data-type="color" style="color:#FFA940;">注意：一定要填写这个IP，如果没有填写可能绑定以后无法访问。</span>

点击确认后，即可生成 CorpSecret 信息，可在新生成的列表中复制这个信息。

![Screen Shot 2018-01-13 at 3.40.08 PM.png | left | 614x453](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/8072a47b-fa49-42e8-b48d-067d4900293f.png "")

然后打开 语雀 后台管理，进入企业设置，在左边导航栏找到「钉钉登录」
将 CorpId 和新生成的 CorpSecret，填写到语雀「绑定钉钉登陆」的相应页面信息里。
![image.png | left | 590x426](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/29a1398a-8a8b-44a9-af68-41f7028dcfaa.png "")
## 扫码测试
绑定后，在此未登录下访问企业空间域名，会跳转到钉钉扫码登录，马上掏出手机测试下吧。下图是云工作室的案例：


![Screen Shot 2018-01-25 at 11.53.46 AM.png | center | 394x469](https://lark-assets-prod.oss-cn-hangzhou.aliyuncs.com/2018/png/3e82e1c9-d71d-498d-bba1-7c551b074f94.png "")


