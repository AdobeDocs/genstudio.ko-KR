---
title: 템플릿 사용자 정의
description: GenStudio용 사용자 지정 템플릿을 만드는 방법을 알아봅니다.
level: Intermediate
feature: Templates, Content
source-git-commit: d7d11077d35a4c1924e4be456c00b1fae24e0a1b
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---


# 템플릿 사용자 정의

_Handlebars_ 템플릿 언어를 사용하여 GenStudio에 대한 HTML 템플릿을 조정할 수 있습니다. Handlebars 구문에서는 컨텐츠 자리 표시자로 이중 중괄호가 있는 일반 텍스트를 사용합니다. 템플릿을 준비하는 방법은 _Handlebars 언어 안내서_&#x200B;의 [`What is Handlebars?`](https://handlebarsjs.com/guide/#what-is-handlebars)을(를) 참조하십시오.

<!-- This is for email. In the future, maybe use tabs to provide guidance for other template types.
-->If you do not have an HTML template ready to use in GenStudio, you can start by defining the structure of your email using HTML tags: `DOCTYPE`, `html`, `head`, and `body`. You can include CSS styles to customize the appearance of your email.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Title</title>
    <style>
    </style>
</head>
<body>
</body>
</html>
```

[템플릿 예제](#template-examples)를 참조하십시오.

>[!TIP]
>
>다음 몇 섹션에서는 이메일 필드에 콘텐츠 자리 표시자를 추가하고, 예제 템플릿을 참조하고, 미리 보기에서 불필요한 요소를 숨기고, 정적 콘텐츠로 연결되는 링크를 관리합니다. 템플릿이 준비되면 [GenStudio에 업로드](use-templates.md#upload-a-template)하고 사용자 지정 템플릿을 기반으로 개인화된 이메일을 생성할 수 있습니다.

## 콘텐츠 자리 표시자

템플릿의 헤드 또는 본문 내에서 Handlebars 구문을 사용하여 GenStudio에서 템플릿을 실제 콘텐츠로 채워야 하는 위치에 콘텐츠 자리 표시자를 삽입할 수 있습니다. GenStudio은 필드 이름을 기반으로 콘텐츠 자리 표시자를 자동으로 인식하고 해석합니다.

예를 들어 `{{ headline }}`을(를) 사용하여 전자 메일의 제목을 배치할 위치를 나타낼 수 있습니다.

```handlebars
<div>{{ headline }}</div>
```

### 필드 이름

사용자 지정 템플릿에서 허용되는 최대 필드 수는 20개입니다.

#### 인식된 필드 이름

다음 표에는 템플릿으로의 채우기에 대해 GenStudio에서 인식하는 필드 이름이 나열되어 있습니다.

| 필드 | 역할 | 채널 템플릿 |
| -------------- | ---------------------- | -------------------- |
| `pre_header` | 사전 머리글 | 이메일(권장) |
| `headline` | 제목 | 이메일(권장)<br>메타 광고 |
| `body` | 본문 복사 | 이메일(권장)<br>메타 광고 |
| `cta` | 클릭 유도 문안 | 이메일(권장)<br>메타 광고 |
| `on_image_text` | 이미지 텍스트에서 | 메타 광고(권장) |
| `image` | 이미지 | 이메일(권장)<br>메타 광고(권장) |
| `brand_logo` | 선택한 브랜드의 로고 | 메타 광고 |

GenStudio은 템플릿의 특정 필드를 자동으로 채우므로 템플릿 디자인에 포함할 필요가 없습니다.

* `subject` 필드(전자 메일 템플릿)
* `headline`, `body` 및 `CTA` 필드(메타 광고 템플릿)

>[!WARNING]
>
>instagram 광고의 경우 생성된 헤드라인은 최종 경험에 표시되지 않습니다.

#### 브랜드 로고 필드 이름

템플릿에 브랜드 로고를 추가하려면 다음 코드를 사용하여 기본 로고를 렌더링합니다.

```{{#if brand_logo}}{{brand_logo}}{{else}} encoded inline logo {{/if}}```

#### 수동 필드 이름

다른 모든 필드 이름은 수동으로 채워진 필드로 처리됩니다. 섹션을 편집할 수 있게 하려면 편집할 섹션 주위에 이중 대괄호를 추가합니다.

> 예: ``{{customVariable}}``(customVariable는 수동으로 편집 가능한 섹션임)

## 섹션 또는 그룹

_섹션_&#x200B;은(는) 이 섹션의 필드에 높은 수준의 일관성이 필요하다는 것을 GenStudio에 알립니다. 이러한 관계를 구축하면 AI가 해당 섹션의 크리에이티브 요소와 일치하는 콘텐츠를 생성할 수 있습니다.

필드 이름에 선택한 접두사를 사용하여 필드가 섹션 또는 그룹의 일부임을 나타냅니다.

예를 들어 강조 표시된 영역에 나타나는 컨텐츠를 강조표시할 수 있습니다.

* `spotlight_headline`
* `spotlight_body`

각 섹션에는 각 필드 유형 중 하나만 있을 수 있습니다. 위의 예에서 `spotlight` 접두사는 하나의 `spotlight_headline` 필드만 가질 수 있습니다.

템플릿에는 최대 3개의 섹션이 포함될 수 있습니다.

* `headline`
* `body`
* `spotlight_headline`
* `spotlight_body`
* `news_headline`
* `news_body`

GenStudio은 `spotlight_headline`이(가) `news_body`보다 `spotlight_body`과(와) 더 밀접하게 관련되어 있음을 이해합니다.

## 템플릿 예

+++예: 한 개의 섹션이 있는 이메일 템플릿

다음은 하나의 섹션을 포함하는 이메일에 대한 HTML 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 간단한 인라인 CSS가 포함되어 있습니다. 본문에는 전자 메일 생성 프로세스 중에 GenStudio에서 콘텐츠를 삽입하는 데 사용할 `pre-header`, `headline` 및 `image` [자리 표시자](#content-placeholders)가 포함되어 있습니다.

```handlebars {line-numbers="true" highlight="13"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
    </div>
</body>
</html>
```

+++

+++예: 여러 섹션이 있는 이메일 템플릿

다음은 위의 예제와 동일한 HTML 템플릿이지만 두 개의 섹션이 더 있습니다. 헤드에는 그룹을 스타일링할 인라인 CSS가 포함되어 있습니다. 본문에서는 접두사를 사용하여 [콘텐츠 자리 표시자](#content-placeholders)가 있는 두 개의 그룹을 사용합니다.

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <title>Adobe</title>
    <style>
        .container {
            width: 100%;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
        .pod {
            background-color: #f8f8f8;
            margin: 10px;
            padding: 20px;
            border-radius: 5px;
        }
        .pod h2 {
            color: #333;
        }
        .pod p {
            color: #666;
        }
    </style>
</head>
<body>{{ pre_header }}
    <div class="container">
        <h1>{{ headline }}</h1>
        <p><img alt="{{ headline }}"
                src="{{ image }}"
                width="600" height="600"
                border="0"/></p>
        <p>{{ body }}</p>
        <div class="pod">
            <h2>{{ pod1_headline }}</h2>
            <p>This is Pod 1 content.</p>
        </div>
        <div class="pod">
            <h2>{{ pod2_headline }}</h2>
            <p>This is Pod 2 content.</p>
        </div>
    </div>
</body>
</html>
```

+++

+++예: 메타 광고 템플릿

다음은 메타 광고 템플릿의 기본 예입니다. 헤드에는 스타일링을 위한 인라인 CSS가 포함되어 있습니다. 본문에서는 접두사를 사용하여 [콘텐츠 자리 표시자](#content-placeholders)를 사용합니다.

```handlebars {line-numbers="true" highlight="33"}
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adobe</title>
    <style>
        .ad-container {
            width: 300px;
            border: 1px solid #ddd;
            padding: 16px;
            font-family: Arial, sans-serif;
        }
        .ad-image {
            width: 100%;
            height: auto;
        }
        .ad-headline {
            font-size: 18px;
            font-weight: bold;
            margin: 12px 0;
        }
        .ad-body {
            font-size: 14px;
            margin: 12px 0;
        }
        .ad-cta {
            display: inline-block;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
<div class="ad-container">
    <img src="{{ image }}" alt="Ad Image" class="ad-image">
    <div class="ad-headline">"{{ headline }}"</div>
    <div class="ad-body">"{{ body }}"</div>
    <a href="(https://example.com)" class="ad-cta">"{{ CTA }}"</a>
</div>

</body>
</html>
```

+++

## 템플릿 미리 보기

기본 제공 도우미(특정 작업을 수행하는 Handlebars 템플릿 언어의 특수 표현식)를 사용하여 특수 콘텐츠의 가시성을 제어합니다. 예를 들어 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가할 수 있습니다.

템플릿을 렌더링할 때는 `_genStudio.browser` 값이 설정되고, 템플릿을 내보낼 때는 `genStudio.export` 값이 설정됩니다. 조건부 래퍼를 사용하여 이메일 상단에 특정 콘텐츠를 포함하도록 결정할 수 있습니다. 예를 들어 템플릿을 내보내기에 사용하는 경우 다음과 같습니다.

```handlebars
{{#if _genStudio.export}}
<%@ include view='emailParent' %>
{{/if}}
```

또 다른 예는 GenStudio에서 템플릿을 미리 볼 때 추적 코드를 사용하지 못하도록 하는 것일 수 있다. 이 예에서는 미리 보기 링크를 깔끔하게 유지하면서 내보낸 템플릿의 링크에 추적 매개 변수를 추가하는 방법을 보여 줍니다.

```handlebars
<a class="button" {{#if _genStudio.browser }}
   href="{{ link }}"{{/if}}{{#if _genStudio.export }}
   href="{{ link }}?trackingid=<%=getTrackingId()%>&mv=email"{{/if}}
   target="_blank">{{ cta }}</a>
```

## 정적 콘텐츠

이메일 및 메타 템플릿은 종종 GenStudio 외부에서 호스팅되는 이미지 및 CSS 파일에 연결됩니다. GenStudio은 이러한 템플릿 또는 템플릿에서 파생된 경험에 대한 썸네일을 생성할 때 올바른 CORS(원본 간 리소스 공유) 헤더가 없으면 이러한 외부 리소스를 무시할 수 있습니다.

썸네일 생성 프로세스 중에 이러한 리소스를 사용할 수 있도록 하려면 다음 두 가지 옵션을 고려하십시오.

1. **CORS 헤더 사용**: 호스트 서버는 프로덕션 환경에 대해 `Access-Control-Allow-Origin` 헤더가 `https://experience.adobe.com` 값으로 설정된 응답을 보내야 합니다. 이 방법을 사용하면 GenStudio에서 리소스에 액세스하고 리소스를 포함할 수 있습니다.
1. **데이터 URL 사용**: 데이터 URL을 사용하여 외부 리소스를 템플릿에 직접 포함합니다. 이 메서드는 CORS 제한을 무시하고 썸네일 생성 중에 리소스를 사용할 수 있도록 합니다.
