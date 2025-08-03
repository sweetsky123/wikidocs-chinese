---
title: Azure Active Directory
description: 联合身份验证模块
published: true
date: 2022-08-31T17:01:57.649Z
tags: auth, module
editor: markdown
dateCreated: 2019-07-20T15:31:49.465Z
---

[Azure Active Directory (Azure AD)](https://azure.microsoft.com/en-ca/services/active-directory/) 是 Microsoft 的基于云的身份和权限管理服务，帮助您的员工登录并访问资源。

# 设置

## A) 复制重定向 URI

1. 在您 Wiki 的 **管理区（Administration Area）** 中，点击左侧导航栏的 **身份验证（Authentication）**。
1. 添加新的 **Microsoft Azure 活动目录（Azure Active Directory）** 联合身份验证策略。
1. 复制 **重定向 URI（Redirect URI）** 值，该值位于配置参考部分下方。保持此页面打开。稍后我们会回来查看。

## B) 创建 Azure AD 应用

1. 从 Azure 门户，进入 **Microsoft Azure 活动目录（Azure Active Directory）** 资源。
1. 点击左侧导航栏的 **应用注册（App registrations）**，然后点击顶部的 **新注册（New registration）**。
1. 输入 **名称（Name）**（例如 Wiki.js）并输入您之前复制的 **重定向 URI（Redirect URI）**。
1. 点击 **注册（Register）**。
1. 复制 **应用（客户）ID（Application (client) ID）**，您稍后需要它。
1. 点击顶部的 **端点（Endpoints）**，复制 **OpenID Connect 元数据文档（OpenID Connect metadata document）** 的 endpoint 值（例如 `https://login.microsoftonline.com/YOUR_TENANT_ID/v2.0/.well-known/openid-configuration`），稍后也需要它。
1. *(可选)* 点击左侧导航栏的 **品牌（Branding）**，输入必要信息以方便您的用户识别。
1. 点击左侧导航栏的 **身份验证（Authentication）**，输入 **登出 URL（Logout URL）**（`https://YOUR-WIKI.DOMAIN.COM`），并确保 **隐式权限（Implicit grant）** 下的 **ID トークン（ID tokens）** 复选框被选中，然后点击顶部的 **保存（Save）**。
1. 点击左侧导航栏的 **API 权限（API permissions）**，确保 **Microsoft Graph > User.Read** 权限已列在其中。
1. *(可选)* 在 **API 权限（API permissions）** 部分，您可以点击 **授予管理权限（Grant admin consent）**，代表目录中所有用户进行操作。这将避免用户首次登录时显示权限确认页面，这在内部分组织环境中通常更可取。

## C) 在 Wiki.js 中启用 Azure AD 策略

1. 返回步骤 A 中的 Wiki.js 管理页面。
1. 输入之前复制的 **身份元数据端点（Identity Metadata Endpoint）** 和 **客户 ID（Client ID）** 值。
1. 启用 **自助注册（Self-registation）** 选项 *(除非您计划手动授权用户)*。
1. 选择新用户首次登录时应被分配的 **组（group）**。
1. 确保在所有 **策略（strategies）** 列表中，**Microsoft Azure 活动目录（Azure Active Directory）** 旁边的复选框被选中。文本应显示该策是 **启用（active）**。
1. 点击页面右上角的 **应用（Apply）** 以保存并应用配置。

<img src="https://static.requarks.io/logo/azure.svg" class="align-abstopright" style="width:150px;" />
  
