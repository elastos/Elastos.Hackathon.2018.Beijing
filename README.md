# 亦来云2018年度Hackathon

## 背景
为了推进技术落地、开拓产品思维、发现优秀团队，亦来云主办此次黑客马拉松编程比赛。

## 时间&地点
2018年5月12~13日在北京五道口智造大街45号PNP一楼。

## 形式
分三个阶段：
1. 报名，向组委会报名参赛，提供选手名单、参赛主题。
2. 开发，根据题目要求进行开发。
3. 展示&评选，5月12日在现场调试、展示、评委打分，最终评选出获胜队伍。

## 题目
基于亦来云Carrier库实现App。
不限App的功能和用途，只要在其中使用了Carrier的功能即可。

## 奖金
1. 一等奖1名，奖金200ELA
2. 二等奖2名，奖金100ELA
3. 鼓励奖5名，奖金20ELA

## 规则
1. 5月12日之前为报名和开发阶段，可以自由选题。
2. 5月12日进行调试和展示，以及最后的debug和调整。
3. 5月13日评委针对各队实现的App进行打分，按得分顺次获得奖金。

## Carrier简介
### 功能介绍
  - 解决互联网上app节点没有公网ip无法直接互联的问题。通常解决这个问题需要部署一台中心服务器来做数据中转。亦来云Carrier基于P2P通信技术实现了无中心的直连通信方案。
  - 提供跨网络访问能力，例如，任意两个app节点可以在不同的子网内，例如，一个在家里wifi环境，一个在公司wifi环境。App之间通过一个“地址”字符串，互相“加好友”确认授权，即可直接通信。
### Carrier编程基本概念
  - Whisper
    代表一个Carrier节点对象。通过它来控制节点的初始化、开启和停止。
  - Friend
    好友，代表一个节点对另一个节点的授权许可。例如，一个节点向另一个节点发送数据，必须先建立好友关系，否则无法通信。
    针对好友可以进行：添加、删除、发送消息等操作。
    基于好友的消息通信，是一个长度受限、不可靠的通信机制，类似UDP数据包。
  - Session
    会话，两个节点之间要想建立长连接、高时效、高可靠性的数据传输通道，可以选择用Session方式。针对Session要进行初始化、请求和确认请求等等操作。
  - Stream
    流，在Session建立成功以后，节点之间通过读写Stream传送数据。
  - Channel
    这是针对同一个session实现的多路复用，是对一个Session使用上进行的封装。
### Android
  - 代码库&编译方法
    <https://github.com/elastos/Elastos.NET.Carrier.Android.SDK>
  - 用法
    <https://github.com/elastos/Elastos.NET.Carrier.Android.SDK#basic-tests>
  - 接口文档
    <https://github.com/elastos/Elastos.NET.Carrier.Android.SDK#build-docs>
### JS
  - <https://github.com/elastos/Elastos.NET.Carrier.Nodejs.SDK>
### C++
  - <https://github.com/elastos/Elastos.NET.Carrier.Native.SDK/>
