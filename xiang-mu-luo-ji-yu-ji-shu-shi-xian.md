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

* 智能合约：Solidity、Hardhat
* 后端：Next.js、Prisma、NextAuth
* 加密算法：待探讨
* 数据库：PostgreSQL
* 前端：Next.js、TailwindCSS、Ethers.js、Wagmi
* 部署平台：Vercel、Polygon
* 去中心化存储：IPFS、Infura

## 协作方式

基于 Github 协作，采用 Git Flow 分支模型。

## 账户

除了钱包登陆外，还需要提供至少一种以上传统登陆方式。这样可以降低用户使用门槛。

目前确认支持的登陆方式有：

* GitHub 登陆

## 支付

项目合约部署网络为 Polygon，交易代币为 MATIC。

目的是为了以最小的 gas 成本使用 ResourceFi。

同时需要考虑普通用户的支付问题。

应当支持银行卡、支付宝或微信交易，实时计算汇率。

交易模式类似币安的 c2c，只是把交易主体从代币换成了资源。

这部分内容的细节仍待商榷。

