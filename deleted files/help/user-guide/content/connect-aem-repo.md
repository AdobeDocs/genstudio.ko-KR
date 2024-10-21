---
title: " [!DNL AEM Assets Content Hub] 저장소에 연결"
description: Adobe GenStudio for Performance Marketing을 AEM(Adobe Experience Manager) [!DNL Content Hub] 저장소에 연결하고 기존의 승인된 콘텐츠를 활용하는 방법을 알아봅니다.
level: Experienced
feature: Assets, Content
source-git-commit: 6ba029f46a37c159ec48676a158a6a9b8fb5465d
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# [!DNL AEM Assets Content Hub] 저장소에 연결

Adobe Experience Manager(AEM)에 자산이 있는 경우 다음 단계에 따라 GenStudio for Performance Marketing에서 액세스할 수 있도록 할 수 있습니다.

>[!BEGINSHADEBOX]

**필수 구성 요소**:

다음 단계에서는 Admin Console 및 AEM Assetsas a Cloud Service 에 대한 관리 액세스 권한이 필요합니다.

>[!ENDSHADEBOX]

## 1단계: [!DNL AEM Assets Content Hub] 사용

**Content Hub 배포** 셀프서비스 프로세스에 따라 Cloud Manager에서 기존 AEM Assets에 대해 [!DNL Content Hub]을(를) 사용하도록 설정하십시오. _AEM as a Cloud Service_ 설명서에서 [배포 [!DNL Content Hub]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub)를 참조하십시오.

[!DNL AEM Assets Content Hub]을(를) 사용하도록 설정한 후에는 Admin Console 시 [!DNL AEM Assets as a Cloud Service] 내에 `contenthub` 접미사를 사용하는 새 인스턴스가 있습니다.

## 2단계: GenStudio 사용자 온보드

[!DNL Admin Console]에서 [!DNL AEM Assets Content Hub] 제품 프로필에 GenStudio 사용자 또는 사용자 그룹을 추가합니다. [!DNL AEM Assets Content Hub] 사용자는 자산을 볼 수 있지만 자산을 추가하거나 기존 자산을 수정할 수 없습니다.

- [온보드 [!DNL Content Hub] 관리자](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub#onboard-content-hub-administrator)
- [온보드 [!DNL Content Hub] 사용자](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/deploy-content-hub#onboard-content-hub-users)

## 3단계: 에셋 승인

[!DNL AEM Assets Content Hub]에서 사용할 자산을 승인하면 GenStudio for Performance Marketing에서 사용할 수 있습니다. _AEM as a Cloud Service_ 설명서의 [Experience Manager에서 자산 승인](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/approve-assets)을 참조하십시오.

## 4단계: 자산 가시성 구성

_[!DNL AEM Assets Content Hub]_구성 옵션에서 필터, 자산 세부 사항, 검색 및 브랜딩에 대한 각 구성 옵션 집합을 검토하십시오._ Content Hub _설명서에서 [AEM as a Cloud Service 사용자 인터페이스 구성](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/configure-content-hub-ui-options)을 참조하십시오.

## 5단계: 연결 확인

GenStudio for Performance Marketing 콘텐츠에서 오른쪽에 있는 갤러리 위에 _[!UICONTROL 위치]_ 목록을 사용할 수 있습니다. 액세스 권한이 없거나 조직이 [!DNL AEM Assets Content Hub] 리포지토리를 배포하고 연결하지 않은 경우 목록을 사용할 수 없습니다.
