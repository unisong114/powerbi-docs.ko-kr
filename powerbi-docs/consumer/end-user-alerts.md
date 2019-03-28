---
title: '자습서: Power BI 서비스에서 데이터 경고 설정'
description: 이 자습서에서는 대시보드의 데이터가 Microsoft Power BI 서비스에서 설정한 한도를 넘어 변경되면 알리도록 경고를 설정하는 방법을 알아봅니다.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: JbL2-HJ8clE
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-consumer
ms.topic: tutorial
ms.date: 12/06/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: 3732939dbf3d8a3569d0c945d9a4d0935d573c86
ms.sourcegitcommit: a054782370dec56d49bb205ee10b7e2018f22693
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56662161"
---
# <a name="tutorial-set-data-alerts-in-power-bi-service"></a>자습서: Power BI 서비스에서 데이터 경고 설정
대시보드의 데이터가 설정해 놓은 한도를 넘어 변경되면 알리도록 경고를 설정합니다. 

Power BI Pro 라이선스가 있는 경우 또는 [프리미엄 용량](../service-premium.md)의 사용자와 대시보드를 공유하는 경우 타일에서 경고를 설정할 수 있습니다. 경고는 보고서 시각적 개체에서 고정된 타일과 계기, KPI 및 카드에서만 설정할 수 있습니다. 경고는 보고서로부터 대시보드로 고정된 스트리밍 데이터 세트에서 만들어진 시각적 개체에 설정할 수 있으나, **타일 추가** > **사용자 지정 스트리밍 데이터**를 사용하여 대시보드에 직접 만든 스트리밍 타일에는 설정할 수 없습니다. 

대시보드를 공유하더라도 자신이 설정한 경고만 볼 수 있습니다. 데이터 경고는 플랫폼 전반에서 완전히 동기화되며 [Power BI 모바일 앱](mobile/mobile-set-data-alerts-in-the-mobile-apps.md) 및 Power BI 서비스에서 데이터 경고를 설정하고 봅니다. 

![타일](../media/service-set-data-alerts/powerbi-alert-types-new.png)

> [!WARNING]
> 데이터 기반 경고 알림은 데이터에 관한 정보를 제공합니다. 모바일 디바이스에서 Power BI 데이터를 보는 데 그 모바일 디바이스를 잃어버린 경우 Power BI 서비스를 사용하여 모든 데이터 기반 경고 규칙을 해제하는 것이 좋습니다.
> 

이 자습서에서는 다음 내용을 다룹니다.
> [!div class="checklist"]
> * 경고를 설정할 수 있는 사용자
> * 경고를 지원하는 시각적 개체
> * 내 경고를 볼 수 있는 사용자
> * Power BI Desktop 및 Mobile에서 작동하는 경고
> * 경고를 만드는 방법
> * 내 경고를 수신하는 위치

아직 Power BI에 등록하지 않은 경우 시작하기 전에 [평가판에 등록합니다](https://app.powerbi.com/signupredirect?pbi_source=web).

## <a name="set-data-alerts-in-power-bi-service"></a>Power BI 서비스에서 데이터 경고 설정
Amanda가 대시보드의 타일에 일부 경고를 추가하는 과정을 시청합니다. 그런 다음, 비디오 아래에 있는 단계별 지침을 따라서 직접 시도해 볼 수 있습니다.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JbL2-HJ8clE" frameborder="0" allowfullscreen></iframe>

이 예제는 [소매점 분석 샘플](http://go.microsoft.com/fwlink/?LinkId=529778) 대시보드의 카드 타일을 사용합니다.

1. 대시보드 계기, KPI 또는 카드 타일에서 추가 옵션(...)을 선택합니다.
   
   ![전체 매장 타일](media/end-user-alerts/powerbi-card.png)
2. 종 모양 아이콘 ![경고 아이콘](media/end-user-alerts/power-bi-bell-icon.png) 또는 **경고 관리**를 선택하여 **총 매장**에 대한 하나 이상의 경고를 추가합니다.
   
1. **경고 관리** 창에서 **+ 경고 규칙 추가**를 선택합니다.  슬라이더가 **켜기**로 설정되어 있는지 확인하고, 경고 제목을 입력합니다. 제목은 경고를 쉽게 인식하는 데 도움이 됩니다.
   
   ![경고 관리 창](media/end-user-alerts/powerbi-alert-title.png)
4. 아래로 스크롤하여 경고 세부 정보를 입력합니다.  이 예제에서는 총 매장의 수가 100을 넘으면 하루에 한 번 알려주는 경고를 만듭니다. 경고는 알림 센터에 표시됩니다. Power BI에서 전자 메일도 전송됩니다.
   
   ![경고 관리 창, 임계값 설정](media/end-user-alerts/power-bi-set-alert-details.png)
5. **저장 후 닫기**를 선택합니다.

## <a name="receiving-alerts"></a>경고 수신
추적되는 데이터가 설정해 놓은 임계값 중 하나에 도달하면, 몇 가지 현상이 발생합니다. 먼저, Power BI에서 마지막 경고가 전송된 후 1시간을 초과하여 경과했는지 또는 24시간을 초과하여 경과했는지(선택한 옵션에 따라) 확인됩니다. 데이터가 임계값을 넘어서는 동안은, 경고를 수신하게 됩니다.

다음으로, Power BI에서 알림 센터에 경고를 보내고 필요에 따라 전자 메일로 보냅니다. 각 경고에는 데이터에 대한 직접 링크가 포함됩니다. 관련 타일을 보려면 링크를 선택하세요.  

1. 전자 메일을 보내도록 경고를 설정해 놓으면, 다음과 같은 내용을 받은 편지함에서 찾을 수 있습니다.
   
   ![경고 이메일](media/end-user-alerts/powerbi-alerts-email.png)
2. Power BI에서 **알림 센터**에 메시지가 추가되고 해당되는 타일에 새로운 경고 아이콘이 추가됩니다.
   
   ![Power BI 서비스의 알림 아이콘](media/end-user-alerts/powerbi-alert-notifications.png)
3. 알림 센터를 열어서 경고 세부 정보를 봅니다.
   
    ![경고 참고](media/end-user-alerts/powerbi-alert-notification.png)
   
   > [!NOTE]
   > 경고는 새로 고쳐지는 데이터에만 적용됩니다. 데이터가 새로 고쳐지면, Power BI에서 해당 데이터에 대해 경고가 설정되어 있는지 확인됩니다. 데이터가 경고 임계값에 도달하면, 경고가 트리거됩니다.
   > 
   > 

## <a name="managing-alerts"></a>경고 관리
경고는 여러 가지 방법으로 관리할 수 있습니다. 대시보드 타일 자체에서, Power BI 설정 메뉴에서, 그리고 [ iPhone용 Power BI 모바일 앱](mobile/mobile-set-data-alerts-in-the-mobile-apps.md) 또는 [Windows 10용 Power BI 모바일 앱](mobile/mobile-set-data-alerts-in-the-mobile-apps.md)에서 관리할 수 있습니다.

### <a name="from-the-tile-itself"></a>타일 자체에서
1. 타일에 대한 경고를 변경하거나 제거하려면, 종 모양 아이콘 ![경고 아이콘](media/end-user-alerts/power-bi-bell-icon.png)을 선택하여 **경고 관리** 창을 다시 엽니다. 해당 타일에 설정해 놓은 모든 경고가 표시됩니다.
   
    ![경고 관리 창](media/end-user-alerts/powerbi-see-alerts.png).
2. 경고를 수정하려면, 경고 이름 왼쪽에 있는 화살표를 선택합니다.
   
    ![경고 이름 옆에 있는 화살표](media/end-user-alerts/powerbi-see-alerts-arrow.png).
3. 경고를 삭제하려면, 경고 이름 오른쪽에 있는 쓰레기통을 선택합니다.
   
      ![선택된 휴지통 아이콘](media/end-user-alerts/powerbi-see-alerts-delete.png)

### <a name="from-the-power-bi-settings-menu"></a>Power BI 설정 메뉴에서
1. Power BI 메뉴 모음에서 기어 아이콘을 선택합니다.
   
    ![기어 아이콘](media/end-user-alerts/powerbi-gear-icon.png).
2. **설정**에서 **경고**를 선택합니다.
   
    ![설정 창의 경고 탭](media/end-user-alerts/powerbi-alert-settings.png)
3. 여기에서 경고를 켜거나 끌 수 있으며, **경고 관리** 창을 열어서 내용을 변경하거나, 경고를 삭제할 수 있습니다.

## <a name="tips-and-troubleshooting"></a>팁 및 문제 해결
* 현재 Bing 타일 또는 카드 타일에 대해서는 날짜/시간 측정값에 대한 경고가 지원되지 않습니다.
* 경고는 숫자 데이터 형식에만 적용됩니다.
* 경고는 새로 고쳐지는 데이터에만 적용됩니다. 정적 데이터에 대해서는 적용되지 않습니다.
* 경고는 KPI/카드/계기 보고서 시각적 개체를 빌드한 다음, 해당 시각적 개체를 대시보드에 고정하는 경우 스트리밍 데이터 세트에서만 작동합니다.

## <a name="clean-up-resources"></a>리소스 정리
경고 삭제 지침은 위에 설명되어 있습니다. 간단히 말해서 Power BI 메뉴 모음에서 기어 아이콘을 선택합니다. **설정**에서 **경고**를 선택하고 경고를 삭제합니다.

> [!div class="nextstepaction"]
> [모바일 디바이스에서 데이터 경고 설정](mobile/mobile-set-data-alerts-in-the-mobile-apps.md)


