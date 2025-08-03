---
title: Discord
description: 身份验证模组
published: true
date: 2025-08-03T19:48:23+08:00
tags: 
---

Discord 是一个流行的网络游戏通信工具。
https://discordapp.com/

# 设置

## A) 在 Discord 上创建应用程序

1. 浏览 [Discord 开发者平台](https://discordapp.com/developers/applications/)。您需要一个现有帐户才能继续。
1. 点击 **新应用程序（New Application）**，输入一个 **名称（name）**（例如 Wiki），点击 **创建（Create）**。
1. 复制 **客户 ID（Client ID）** 和 **客户密钥（Client Secret）** 的值。稍后我们需要。

## B) 在 Wiki.js 中启用 Discord 策略

1. 在您 Wiki 的 **管理区（Administration Area）** 中，点击左侧导航栏的 **身份验证（Authentication）**。
1. 点击 **Discord**。
1. 输入先前复制的 **客户 ID（Client ID）** 和 **客户密钥（Client Secret）** 值。
1. 启用 **自助注册（Self-registration）** 选 项 *(除非 您计划手动授权用户)*。
1. 选择新用户首次登录时应被分 配的组（group）。
1. 确保在所有 **策略（strategies）** 列表中，**Discord** 旁边的复选框被选中。文本应显示该策略已 **启用（active）**。
1. 点击页面右上角的 **应用（Apply）** 以保存并应用配置。

## C) 在 Discord 上输入 OAuth2 设置

回到 Discord 开发者平台，您需要设置重定向 URI。在应用程序页面，点击左侧边栏的 **OAuth2**，并添加回调重定向 URI。此值可在 Wiki.js 的 **配 置参考（Configuration Reference）** 下方找到，位于 **Discord 策略（Discord strategy）** 的设置中。

点击页面底部的 **保存修改（Save Changes）** 按钮。

虽然可选，但建议设置 **应用标志（Application Logo）** 以方便您的终端用户识别。

![](https://static.requarks.io/logo/discord.svg){.align-abstopright}
