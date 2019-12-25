# 前言

熟悉内网渗透的应该都对IPC，黄金票据，白银票据，NTLM Relay，Pth,Ptt,Ptk 这些词汇再熟悉不够了，对其利用工具也了如指掌，但是有些人对里面使用的原理还不太了解，知其然不知其所以然，本系列文章将针对内网渗透的常见协议\(如kerbeos,ntlm,smb,ldap等\)进行协议分析，相关漏洞分析以及漏洞工具分析利用。

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


