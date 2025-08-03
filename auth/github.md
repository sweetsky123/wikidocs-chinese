---
title: GitHub
description: 联合身份验证模块
published: true
date: 2025-08-03T20:10:41+08:00
tags: auth, module
---

GitHub 是一个基于使用 Git的网页的版本控制托管服务。

# 设置

## A) 创建 OAuth GitHub 应用

1. 前往 [New OAuth Application](https://github.com/settings/applications/new) 页面
 	- 您也可以通过进入组织设置页面并点击 `OAuth Apps`，然后 `New OAuth App` 使用组织而非个人账户。
1. 输入一个 **应用名称（Application Name）**（例如 Wiki.js）。
1. 输入指向您 wiki 的 **主页 URL（Homepage URL）**。
1. 输入 **授权回调 URL（Authorization callback URL）**。  
	此值可在 Wiki.js 的 **配置引用（Configuration Reference）** 中找到，显示在 **GitHub 策略（GitHub strategy）** 设置下方。
1. 点击 **注册应用（Register application）**。
1. 将显示 **客户 ID（Client ID）** 和 **客户密钥（Client Secret）**。复制这两个密键。稍后我们需要它们。
1. *(可选)*{.caption} 上传此应用的头像。

## B) 在 Wiki.js 中启用 GitHub 策略

1. 在您的 wiki 的 **管理区（Administration Area）** 中，点击左侧菜单的 **身份验证（Authentication）**。
1. 点击 **Github**。
1. 输入先前复制的 **客户 ID（Client ID）** 和 **客户密钥（Client Secret）** 值。
	> **仅限 GitHub Enterprise：**
		> - 启用 **使用 GitHub Enterprise（Use GitHub Enterprise）** 开关。
  	> - 输入您的 **GitHub Enterprise 域名（GitHub Enterprise Domain）** *(不带 http/s 前缀或斜杠，例如 github.yourdomain.com)*
    > - 输入您的 **GitHub Enterprise 用户端点（GitHub Enterprise User Endpoint）** *(例如 https://api.github.yourdomain.com)*
	{.is-info}
1. 启用 **自助注册（Self-registration）** 选项 *(除非您计划手动授权用户)*。
1. 选择新用户首次登录时应被分配的 **组（group）**。
1. 确保在所有 **策略（strategies）** 列表中，**GitHub** 旁边的复选框被选中。文本应显示该策略已 **启用（active）**。
1. 点击页面右上角的 **应用（Apply）** 以保存并应用配置。

![](https://static.requarks.io/logo/github.svg =x50){.align-abstopright}
