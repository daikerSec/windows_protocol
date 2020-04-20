# 前言

熟悉内网渗透的应该都对IPC，黄金票据，白银票据，NTLM Relay，Pth,Ptt,Ptk，PTC 这些词汇再熟悉不够了，对其利用工具也了如指掌，但是有些人对里面使用的原理还不太了解，知其然不知其所以然，本系列文章就针对内网渗透的常见协议(如kerberos,ntlm,smb,ldap,netbios等)进行分析，介绍相关漏洞分析以及漏洞工具分析利用。

在这个系列文章里面主要有

1. kerberos 篇分为AS_REQ/AS_REP，TGS_REQ/TGS_TGS_REP,PAC三部分，介绍kerberos的点点滴滴，以及在协议设计与实现上可能出现的各种安全隐患，如用户名枚举，密码喷撒，黄金票据，白银票据，Kerberoasing等。
2. 在NTLM 篇，介绍NTLM,Net-ntlm 相关的一些知识点，介绍了PTH，PTH的缓解补丁kb2871997，以及整个NTLM协议里面最严重的一个问题--NTLM_Relay,怎么发起NTLM请求，拿到NTLM请求之后怎么做。从破解Net-ntlmv1，到Relay 会SMB，再到现在的配合资源约束委派的整个NTLM_relay 攻击的进化史。
3. 在LDAP篇，介绍了AD的一些内容，组，OU，计算机，用户，ACL，组策略，域信任等等。

由于水平有限。在编写整个系列文章的时候，难免有一些问题，多谢
- @hl0rey
- @xianyu
- @Imanfeng
- @rootclay
- @伍默 

等师傅提出的宝贵意见。在整个过程中收获最大的莫过于在师傅们提出指正之后，翻阅文档，调试工具，最后解决问题，得出结论，纠正一些之前片面的观点这个过程。这个系列的文章还会写下去，在LDAP篇结束之后，马上开启新的NetBios篇，如果师傅们在看文章的过程中，如有错误，希望指正出来。


- gitbook 地址 [https://daiker.gitbook.io/windows-protocol/](https://daiker.gitbook.io/windows-protocol/)
- 目标更新进度
    * Kerberos 篇
      * [AS\_REQ & AS\_REP](https://daiker.gitbook.io/windows-protocol/kerberos/1)
      * [TGS\_REQ & TGS\_REP](https://daiker.gitbook.io/windows-protocol/kerberos/2)
      * [PAC](https://daiker.gitbook.io/windows-protocol/kerberos/3)
    * NTLM 篇
      * [NTLM 基础 介绍](https://daiker.gitbook.io/windows-protocol/ntlm-pian/4)
      * [发起NTLM  请求](https://daiker.gitbook.io/windows-protocol/ntlm-pian/5)
      * [Net- NTLM 利用](https://daiker.gitbook.io/windows-protocol/ntlm-pian/6)
      * [漏洞概述](https://daiker.gitbook.io/windows-protocol/ntlm-pian/7)
    * LDAP 篇
      * [Active Directory简介](https://daiker.gitbook.io/windows-protocol/ldap-pian/8)
      * [组和OU介绍](https://daiker.gitbook.io/windows-protocol/ldap-pian/9)
      * [域用户和计算机用户介绍](https://daiker.gitbook.io/windows-protocol/ldap-pian/10)
      * [域权限上](https://daiker.gitbook.io/windows-protocol/ldap-pian/11)
      * [域权限下](https://daiker.gitbook.io/windows-protocol/ldap-pian/12)
      * [组策略](https://daiker.gitbook.io/windows-protocol/ldap-pian/13)
- 工具
    - * [kerberos 测试工具2.0](https://github.com/daikerSec/windows_protocol/raw/master/tools/kerberosGui.exe)

