---
title: 자산 세부 사항
description: 성능 마케터용 Adobe GenStudio은 검색 및 성능 추적을 위해 승인된 컨텐츠를 풍부한 메타데이터와 함께 저장합니다.
feature: Attributes, Assets
exl-id: 2be5cfee-f315-4ad6-8cf0-a8d3929b9ba3
source-git-commit: 95eb7c2eaeeceedf3abe5ab16e1e7c2de7bf8117
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# 자산 세부 사항

성능 마케터용 Adobe GenStudio은 검색 기능 및 성능 추적을 위해 승인된 컨텐츠를 풍부한 메타데이터와 함께 저장합니다.

각 자산(경험 및 템플릿 포함)에는 콘텐츠 성능을 식별, 추적, 사용 및 학습하는 데 도움이 되는 _세부 정보_(메타데이터)가 연결되었습니다.

**자산 세부 정보를 보려면**:

1. _[!DNL Content]_에서 에셋, 경험 또는 템플릿을 선택합니다. 에셋을 클릭하면 에셋의 중요 보기가 열립니다.

1. 자산 보기에서 오른쪽의 _[!UICONTROL 세부 정보]_ 섹션을 검토합니다.

   >[!TIP]
   >
   >_[!UICONTROL 세부 정보]_ 섹션이 표시되지 않으면 **[!UICONTROL 정보]**(i) 아이콘을 클릭합니다.

에셋 세부 사항에는 생성 또는 업로드 프로세스 중에 적용된 메타데이터가 포함됩니다. 에셋 메타데이터 유형에는 [시스템 메타데이터](#system-metadata) 및 [사용자 정의 메타데이터](#user-defined-metadata)가 포함됩니다.

>[!NOTE]
>
>AEM 저장소의 Assets에 다른 메타데이터가 표시됩니다. AEM Assets Content Hub 에셋 세부 정보를 구성하는 방법에 대해 알아보려면 [에셋 가시성 구성](connect-aem-repo.md#step-4-configure-asset-visibility)을 참조하십시오.

## 시스템 메타데이터

일부 에셋 메타데이터는 에셋이 업로드될 때 자동으로 수집됩니다. 기본 시스템 메타데이터는 편집할 수 없습니다.

에셋에 대해 저장되고 캡처되는 기본 메타데이터에는 파일 이름, 차원, 소스 등이 포함됩니다.

### 생성된 태그

승인된 에셋을 [!DNL Content]에 저장하면 GenStudio for Performance Marketters는 Adobe의 AI 및 머신 러닝 기능을 사용하여 에셋을 학습하고 에셋 기능을 기반으로 태그를 적용합니다. 예를 들어, 고양이 그림으로 인해 `pet photography` 또는 `cat`과(와) 같은 스마트 태그와 그림에서 지배적인 색상을 식별하는 색상 태그가 발생할 수 있습니다. 태그를 편집할 수 없습니다.

### 생성된 컨텐츠 메타데이터

새 에셋 또는 경험을 생성하는 데 사용된 정보는 사용된 프롬프트와 같은 메타데이터가 됩니다. 컨텐츠가 승인된 후에는 프롬프트를 편집할 수 없지만, 새로운 항목을 생성하기 위한 시작 위치로 사용할 수 있습니다.

## 사용자 정의 메타데이터

사용자 정의 메타데이터는 에셋의 콘텐츠에 마케팅 컨텍스트를 추가하여 마케터가 에셋을 사용하고 참여하는 방법을 이해할 수 있도록 합니다.

[에셋을 업로드](/help/user-guide/content/manage-assets.md#add-assets)할 때 성능 마케터용 GenStudio에 메타데이터로 존재하는 선택적 에셋 세부 정보 집합을 정의할 수 있습니다. 더 많은 세부 정보를 포함하면 검색 및 필터링에서 에셋 식별을 향상시킬 수 있습니다.

### 메타데이터 세부 정보

다음 표에서는 자산을 생성할 때 정의할 수 있는 메타데이터(자산 세부 사항)에 대해 자세히 설명합니다.

| 필드 | 설명 |
| ------------- | ----------- |
| 캠페인(프로젝트 이름) | 에셋으로 캡처 및 저장된 기본 메타데이터 |
| [!DNL Brands] | [[!DNL Brands]](/help/user-guide/guidelines/brands.md)이(가) 성능 마케터용 GenStudio에 추가되고 사용을 위해 게시됨 |
| [!DNL Products] | [[!DNL Products]](/help/user-guide/guidelines/products.md)이(가) 성능 마케터용 GenStudio에 추가되었습니다. |
| [!DNL Personas] | [[!DNL Personas]](/help/user-guide/guidelines/personas.md)이(가) 성능 마케터용 GenStudio에 추가되었습니다. |
| 채널 | 이메일 및 메타 광고와 같이 에셋을 사용하는 성능 마케터용 GenStudio의 콘텐츠 유형 |
| 일정 | 에셋이 사용된 기간(예: 분기, 시즌, 연도 등) 예: `Winter 2023` |
| 지역 | 자산이 사용되는 지역. 예: `North America`, `APAC`, `Italy` |
| 언어 | 에셋이 사용되는 언어입니다. 예: `Spanish` |
| 키워드 | 자산 특성 및 용도를 추가로 식별하기 위해 사용되는 키워드 |

<!-- ## History

Expand the _[!UICONTROL History]_ section to view a timeline of approvals and activity.

list other activity, show screenshot?
-->
