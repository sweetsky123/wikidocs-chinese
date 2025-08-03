---
title: Auth0
description: Auth0 身份验证模块
published: true
date: 2025-08-03T19:40:41+08:00
tags: 
---

Auth0 是一个流行的云服务，用于管理您在各个应用程序中的身份验证。
[auth0.com](https://auth0.com)

# 设置

## A) 创建 Auth0 应用程序

1. 如果尚未注册，请在 [Auth0](https://auth0.com/) 创建一个账户。
1. 从仪表板中点击左侧导航栏的 **应用程序（Applications）**。
1. 点击 **创建应用程序（Create Application）**，输入一个 **名称（name）**（例如 Wiki）并选择 **常规 Web 网站（Regular Web Applications）** 作为类型。
1. 点击 **创建（Create）**。
1. 应用程序创建完成后，切换到 **设置（Setting）**选项卡。
1. 复制 **域名（Domain）**、**客户 ID（Client ID）** 和 **密文（Client Secret）** 的值。稍后我们需要它们。

## B) 在 Wiki.js 中启用 Auth0 策略

1. 在您 Wiki 的 **管理区（Administration Area）** 中，点击左侧导航栏的 **身份验证（Authentication）**。
1. 点击 **Auth0**。
1. 输入先前复制的 **域名（Domain）**、**客户 ID（Client ID）** 和 **密文（Client Secret）** 值。
1. 启用 **自助注册（Self-registration）** 选项*（如果计划手动授权用户则无需启用）*。
1. 选择新用户登录时应被分配的 **组（group）**。
1. 确保在所有 **策略** 列表中， **Auth0** 旁边的复选框被选中。文本应显示该策略已 **启用（active）**。
1. 点击页面右上角的 **应用（Apply）** 以保存并应用配置。

## C) 在 Auth0 中输入允许的端点

回到 Auth0 仪表板网站上的应用页面，你需要填写：
- 允许的回调 URL
- 允许的 Web 起源
- 允许的登出 URL

这些值可以在 Wiki.js 的 **配置参考（Configuration Reference）** 中找到，显示在 **Auth0 策略（Auth0 strategy）** 的设置下方。填写完成后，点击页面底部的 **保存更改（Save Changes）** 按钮。虽然可选，但建议设置 **应用logo（Application Logo）** 以方便您的终端用户识别。

![](https://static.requarks.io/logo/auth0.svg =x50){.align-abstopright}
  
