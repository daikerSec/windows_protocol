# 前言

熟悉内网渗透的应该都对IPC，黄金票据，白银票据，NTLM Relay，Pth,Ptt,Ptk 这些词汇再熟悉不够了，对其利用工具也了如指掌，但是有些人对里面使用的原理还不太了解，知其然不知其所以然，本系列文章将针对内网渗透的常见协议\(如kerbeos,ntlm,smb,ldap等\)进行协议分析，相关漏洞分析以及漏洞工具分析利用。

- gitbook 地址 [https://daiker.gitbook.io/windows-protocol/](https://daiker.gitbook.io/windows-protocol/)
- 目标更新进度
    * [Kerberos 篇](kerberos/README.md)
      * [AS\_REQ & AS\_REP](kerberos/1.md)
      * [TGS\_REQ & TGS\_REP](kerberos/2.md)
      * [PAC](kerberos/3.md)
    * [NTLM 篇](ntlm-pian/README.md)
      * [NTLM 基础 介绍](ntlm-pian/4.md)
      * [发起NTLM  请求](ntlm-pian/5.md)
      * [Net- NTLM 利用](ntlm-pian/6.md)
      * [漏洞概述](ntlm-pian/7.md)
    * [LDAP 篇](ldap-pian/README.md)
      * [Active Directory简介](ldap-pian/8.md)
      * [组和OU介绍](ldap-pian/9.md)


