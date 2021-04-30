---
title: Personalize content in Journey Optimizer
description: Get Started with personalization
---
# Get started {#add-personalization}

![](../assets/do-not-localize/badge.png)

Personalization, in the context of Journey Optimizer, is the action of targeting a message to a specific subscriber by leveraging the data and information you have about him. It can be his first name, his interests, where he lives, and more.

Journey Optimizer uses an **inline** simple personalization syntax based on Handlebars which allows you to create expressions with contents enclosed by double curly braces **{{}}**. You can add multiple expressions in the same content or field without restrictions. Refer to [Personalization syntax](personalization-syntax.md).

The personalization is based on the profile data that are managed by the **XDM Individual Profile** schema defined in Adobe Experience Platform. For more on this, refer to  [Adobe Experience Platform Data Model (XDM) documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

>[!CAUTION]
>The **XDM Individual Profile** schema is the only one that you can use to personalize content in Journey Optimizer.

**Examples:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

During **message processing** (email and push), the expression is replaced with the data contained in the Experience Cloud platform databases.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
