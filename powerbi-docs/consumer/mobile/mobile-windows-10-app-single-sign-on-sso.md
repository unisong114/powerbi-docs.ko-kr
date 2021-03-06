---
title: Power BI 모바일 Windows 앱의 Single Sign-On
description: Power BI 모바일 Windows 앱의 SSO(Single Sign-On)에 대해 읽어 보세요. SSO는 단일 사용자 계정으로 한 번만 로그인하여 비즈니스를 수행하는 데 필요한 모든 응용 프로그램 및 리소스에 액세스하는 것을 의미합니다.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 09/17/2018
ms.author: maggies
ms.openlocfilehash: f13b6e0a6583bcb66da0fb0a27188c83c4bf6806
ms.sourcegitcommit: 698b788720282b67d3e22ae5de572b54056f1b6c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45975038"
---
# <a name="single-sign-on-in-the-power-bi-mobile-windows-app"></a>Power BI 모바일 Windows 앱의 Single Sign-On

Power BI 모바일 Windows 앱의 SSO(Single Sign-On)에 대해 읽어 보세요. SSO는 단일 사용자 계정으로 한 번만 로그인하여 비즈니스를 수행하는 데 필요한 모든 응용 프로그램 및 리소스에 액세스하는 것을 의미합니다. 로그인하면 다시 인증하지 않고도 모든 응용 프로그램에 액세스할 수 있습니다. 

Power BI Windows 앱은 Azure Active Directory에 통합되어 있으므로 기본 조직 계정을 사용하여 도메인에 가입된 장치에 로그인할 뿐 아니라 Power BI 서비스에도 로그인할 수 있습니다. Windows 휴대폰에서 Power BI를 보는 경우 Power BI에 사용하는 계정은 장치 설정에서 회사 또는 학교 계정으로 구성되어야 합니다.  

SSO는 Microsoft Azure Active Directory에서 관리하는 Windows 장치에만 사용할 수 있습니다. 

## <a name="sign-in-with-sso"></a>SSO로 로그인

로그인 프로세스를 간소화하기 위해 앱을 처음 설치하면 앱은 SSO를 사용하여 Power BI 서비스에 자동으로 인증을 시도합니다. 이 프로세스가 실패할 경우에만 앱은 사용자에게 Power BI의 자격 증명을 제공하도록 요청합니다.  

이미 Windows용 Power BI 모바일 앱을 사용하고 있는 경우 새 버전의 앱으로 업그레이드하면 SSO를 사용할 수도 있습니다. 앱에서 로그아웃하고 앱을 닫았다가 다시 엽니다. 앱이 다시 열리면 앱은 현재 Windows 자격 증명을 사용하여 Power BI 서비스에 자동으로 인증을 시도합니다. 

Power BI에 로그인하는 데 현재 Windows 활성 세션 자격 증명을 사용하지 않으려면 **설정**으로 이동하고, 로그아웃한 후, 다른 자격 증명으로 로그인하면 됩니다. 
 
## <a name="next-steps"></a>다음 단계

- [Windows 10용 Power BI 모바일 앱 시작](mobile-windows-10-phone-app-get-started.md)
- 궁금한 점이 더 있나요? [Power BI 커뮤니티에 질문합니다.](http://community.powerbi.com/)

