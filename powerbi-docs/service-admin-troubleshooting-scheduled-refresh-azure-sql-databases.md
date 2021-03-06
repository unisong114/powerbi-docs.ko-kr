---
title: Azure SQL Database에 대해 예약된 새로 고침의 문제 해결
description: 'Power BI에서 Azure SQL Database에 대해 예약된 새로 고침의 문제 해결 '
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 12/06/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 9439ac6bd0b4df568b964f548372fb94d2fd0b26
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34238529"
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a>Power BI에서 Azure SQL Database에 대해 예약된 새로 고침의 문제 해결 
예약 새로 고침 설정에 대한 자세한 단계는 [Power BI에서 데이터 새로 고침](refresh-data.md)을 반드시 참조하세요.

Azure SQL Database에 예약 새로 고침을 설정할 때 자격 증명 편집 중에 오류 코드 400의 오류가 발생할 경우 다음에 따라 적합한 방화벽 규칙을 구성합니다.

1. Azure 관리 포털에 로그인
2. 새로 고침을 구성할 Azure SQL 서버로 이동
3. 허용된 서비스 섹션에서 ‘Windows Azure 서비스’ 켜기

![](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

궁금한 점이 더 있나요? [Power BI 커뮤니티를 이용하세요.](http://community.powerbi.com/)

