---
title: 액세스 가능한 템플릿 만들기
description: 더 많은 대상자에게 도달하고 최적의 경험을 제공할 수 있는 성능 마케터를 위한 Adobe GenStudio 템플릿을 작성합니다.
feature: Templates, Content
source-git-commit: c891f876fe5a7c75487fcba6552a213533f0b609
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# 액세스 가능한 템플릿 만들기

Adobe은 모든 대상자에게 최적의 경험을 제공하기 위해 최선을 다하고 있습니다. 자세한 내용은 [Adobe의 접근성 이니셔티브](https://www.adobe.com/trust/accessibility/initiatives.html)를 참조하십시오.

GenStudio for Performance Marketers에서 다양한 경험에 대한 콘텐츠를 만들 수 있는 에셋과 템플릿을 업로드할 수 있습니다. 접근성 표준을 준수하면 콘텐츠가 의도한 최대 대상자에게 도달할 수 있습니다.

최적의 접근성 표준을 사용하여 템플릿을 준비하려면 다음 권장 사항을 사용하십시오.

## 대체 텍스트

이미지와 같이 텍스트가 아닌 콘텐츠에 대해 텍스트 대체 요소를 제공합니다.

```html
<img alt="Collage of ideas, books, man holding giant pencil, computer" src="card-create-assets.png">
```

![아이디어, 책, 큰 연필 들고 있는 남자, 컴퓨터 콜라주](../../assets/card-create-assets.png){width="400"}

## 링크 목적(링크만)

링크의 목적 및 위치를 설명하는 명확한 링크 텍스트를 만듭니다.

예를 들어 &quot;여기를 클릭&quot; 또는 &quot;자세히 읽기&quot;와 같은 링크 텍스트를 사용하는 경우 링크의 목적을 명확하게 설명하지 않습니다.

```html
<a href="product-site.html">Click here</a>
```

링크의 위치를 명확하게 설명하는 텍스트를 사용하는 것이 좋습니다. 링크 소스의 제목과 목적을 사용하는 것이 더 좋습니다.

```html
<a href="product-site.html">Explore Product Site</a>
```

## 언어

많은 제품 및 서비스가 언어를 창의적 또는 독특한 방식으로 사용합니다. 전문 용어, 긴 문장, 복잡한 어구를 피하십시오. 타겟 대상자와 호환되고 간결하고 읽기 쉬운 언어를 사용하십시오.

- 가능한 경우 명확한 설명, 인라인 정의 또는 관련 가능한 예를 사용합니다. 고유한 국어를 번역하는 것은 어려울 수 있습니다.

- 축약어 또는 약어의 첫 번째 인스턴스에 대한 정의의 철자 또는 링크 약어를 번역하는 것은 어려울 수 있습니다.

- 가능하면 시각적 요소를 사용하여 텍스트나 복잡한 아이디어를 보완합니다.
