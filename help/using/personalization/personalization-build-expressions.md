---
title: Acerca del Editor de expresiones
description: Learn how to work with the Expression Editor.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---

# Acerca del Editor de expresiones {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Acerca del Editor de expresiones"
>abstract="The Expression Editor allows you to select, arrange, customize and validate all the data to create a customized personalization for your content."

[!DNL Journey Optimizer] It is available in every context where you need to define personalization like emails, push and offers.

In the expression editor interface, you will select, arrange, customize and validate all the data to create a customized personalization for your content.

![](assets/perso_ee1.png)

The left part of the screen displays a domain selector that lets you select the source for personalization.

![](assets/perso_ee3.png)

Available sources are:

* **[!UICONTROL Profile attributes]**[](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es)
* **[!UICONTROL Segment memberships]** [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)
* **[!UICONTROL Offer decisions]** Select the placement then insert the offers in your content. [](../messages/deliver-personalized-offers.md)
* **[!UICONTROL Contextual attributes]****** Obtenga más información en [esta sección](personalization-use-case.md).
* **[!UICONTROL Helper functions]** Obtenga más información en [esta sección](functions/functions.md).

Click the + button too add an attribute into the editor.

>[!NOTE]
>
>[](personalization-favorites.md)

![](assets/attribute-details.png)

In the following example, the expression editor lets you select the profiles that have their birthday today then complete the customization by inserting a specific offer corresponding to this day.

![](assets/perso_ee2.png)

Once your personalization expression is ready, you need to have it validated by the Expression Editor. Obtenga más información en [esta sección](personalization-validation.md).
