# 项目逻辑与技术实现

{% hint style="warning" %}
WIP
{% endhint %}

## 整体逻辑

首先由资源发布者进行资源发布。

这时数据存储在后端，状态为待审核。项目方可见，用户不可见。

项目方审核通过后，会将资源通过私钥进行加密，私钥和密文分别发布到 IPFS。

不同类型的资源需要通过不同的加密算法进行加密，来保证资源紧凑地体积。



## 技术选型

* 智能合约：Solidity
* 后端：Next.js、prisma、nextauth
* 加密算法：待探讨
* 数据库：PostgreSQL
* 前端：Next.js、TailwindCSS、ethers.js、wagmi
* 部署平台：vercel
* 去中心化存储：IPFS、pinata

## 协作方式

基于 Github 协作，采用 git flow 分支模型。

## 账户

除了钱包登陆外，还需要提供至少一种以上 Web2 的登陆方式。

比如 GitHub 登陆，这样可以降低用户使用门槛。

## 支付

需要考虑普通用户的支付问题。

比如通过传统支付方式进行支付，银行卡、支付宝或微信。然后转换成加密数字货币。

这部分内容仍待商榷。

{% hint style="warning" %}
WIP
{% endhint %}

