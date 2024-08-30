---
title: 유효한 프롬프트 작성
description: 성능 마케터를 위한 Adobe GenStudio에 대한 효과적인 프롬프트를 작성하는 방법을 알아봅니다.
feature: Prompt, Generative AI, Brands Service, Personas Service, Products Service, Guidelines
source-git-commit: 306b64b44e69dbcec3984d1a0b54230fe0dbe48c
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---


# 유효한 프롬프트 작성

성과 마케터를 위한 Adobe GenStudio에서 효과적으로 작업하려면 생성 AI와 통신하는 것이 중요합니다.

GenStudio for Performance Marketters는 에셋을 수정할 수 있는 기회가 있을 때마다 생성 AI 프롬프트를 제공합니다. 효과적인 프롬프트의 구성 요소에는 구성된 지침을 통해 제공되지 않는 설명 언어, 예 및 정보가 포함되어야 합니다.

가장 좋은 방법은 [지침](/help/user-guide/guidelines/overview.md)을(를) 사용하여 성능 마케터용 GenStudio에 브랜드 정보를 제공하는 것입니다. 그러면 생성 AI를 완전히 활용하여 브랜드에 맞게 조정된 콘텐츠 경험을 만들 수 있습니다.

## 기술 언어

자연어를 사용하여 자신의 아이디어를 표현하여 경험을 만들 수 있다. 프롬프트는 AI가 개인화된 채널 콘텐츠와 비전을 보완하는 이미지를 생성하도록 안내합니다. 세부 정보를 많이 제공할수록 사용자의 요구 사항에 맞는 이미지나 경험을 제작할 가능성이 높아집니다. 명확하고 설명적인 언어를 사용하여 가능한 한 많은 세부 정보를 제공합니다.

- **이미지**&#x200B;의 경우 분위기, 기분, 색상, 구성 및 스타일을 설명하는 단어를 사용하십시오.
- **복사**&#x200B;의 경우 대상, 목적, 새 기능 설명, 예 및 작업을 설명하는 단어를 사용하십시오.

다음은 의도, 타겟 대상자 및 스타일에 대한 정보를 설명하는 샘플 프롬프트입니다.

```bash
Write an email to motivate infrequent users of Photoshop to follow an in-app tutorial that teaches them to combine elements of two photos into a beautiful work of art. Highlight the generative AI capabilities of Photoshop and use references to natural imagery.
```

+++샘플 결과 참조

![생성된 전자 메일 3개](/help/assets/sample-email.png)

+++

## 프롬프트 기준

성능 마케터용 GenStudio [[!DNL Create]](/help/user-guide/create/overview.md)에서는 프롬프트 영역의 **[!UICONTROL 프롬프트 기준]**([_매개 변수_](/help/user-guide/create/overview.md#parameters) 및 프롬프트)을 사용하여 선택을 통해 세부 정보를 추가하여 AI 해석을 개선할 수 있습니다.

[이메일](/help/tutorials/create-email-experience.md)의 경우, 프롬프트 기준에는 _매개 변수_&#x200B;의 [지침](/help/user-guide/guidelines/overview.md) 추가, 이메일 변형에 사용할 에셋 업로드 및 설명 프롬프트가 포함될 수 있습니다. [메타데이터](/help/tutorials/create-meta-ad.md)의 경우 프롬프트 기준에는 _매개 변수_&#x200B;의 브랜드 지침, 기존 에셋의 선택 또는 업로드, 이미지 또는 에셋(예: 종횡비) 관련 설정 및 프롬프트가 포함될 수 있습니다. 실제 성능은 [구성 지침](/help/user-guide/guidelines/add-guidelines.md)에서 시작됩니다.

>[!NOTE]
>
>프롬프트 영역의 _매개 변수_&#x200B;에 지침이 추가된 경우 프롬프트에 해당 지침에 대한 참조를 포함할 필요가 없습니다. 성능 마케터용 GenStudio은 콘텐츠 생성에서 해당 [!DNL Brands], [!DNL Products] 및 [!DNL Personas]을(를) 활용합니다.

### 지침

GenStudio for Performance Marketers 지침은 생성 AI가 에셋 구성을 개인화할 수 있도록 지원합니다. 프롬프트 기준이 표시되면 구성된 지침에서 [[!DNL Brand]](/help/user-guide/guidelines/brands.md), [[!DNL Persona]](/help/user-guide/guidelines/personas.md) 및 [[!DNL Product]](/help/user-guide/guidelines/products.md)을(를) 선택할 수 있습니다.

>[!TIP]
>
>성능 마케터용 GenStudio에서 [!DNL Brand] 지침을 사용하는 방법과 시기를 제어할 수 있습니다. 브랜드 지침을 구성하고 관리하는 방법은 [지침](/help/user-guide/guidelines/overview.md)을 참조하세요.

## 다시 시도

프롬프트는 반복적인 프로세스입니다. 결과가 예상과 맞지 않으면 프롬프트를 검토하고 일부 내용을 변경하거나 세부 정보를 추가하십시오. 또는 캠페인 개요의 섹션에 붙여넣을 수 있습니다. 성능 마케터용 GenStudio에 특정 단어, 요소 또는 테마를 피하도록 요청할 수도 있습니다.

## 모범 사례

효과적인 프롬프트를 만들기 위한 몇 가지 간단한 모범 사례입니다.

- 수행할 작업과 수행하지 않을 작업에 대한 세부 정보를 제공합니다.
- 외부 참조를 사용하여 컨텍스트를 제공합니다.
- GenStudio을 활용하여 성과 마케터 지침을 확인하십시오.
- 정기적으로 지침을 검토하고 조정합니다.
- 반복 및 세분화.
- 실험을 통해 배우십시오.
