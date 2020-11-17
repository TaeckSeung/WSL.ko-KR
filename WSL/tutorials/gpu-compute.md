---
title: Linux 용 Windows 하위 시스템의 GPU 가속 Machine Learning 교육
description: NVIDIA, DirectML, Tensorflow 및 PyTorch에 대 한 WSL 2 지원에 대해 자세히 알아보세요.
keywords: wsl, windows, windows 하위 시스템, gpu 계산, gpu 가속, NVIDIA, azure, DirectML, Tensorflow, PyTorch, NVIDIA DA 미리 보기, GPU 드라이버, NVIDIA Container Toolkit, Docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: bc20f2d3f1da646ba01dcdc00de8eca6c3825ec8
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413314"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템의 GPU 가속 기계 학습 교육

#1 가장 많이 요청 된 WSL 기능을 제공 하는 GPU 계산에 대 한 지원은 이제 Windows 참가자 프로그램을 통해 미리 보기로 제공 됩니다. [블로그 게시물 읽기](https://blogs.windows.com/windowsdeveloper/?p=55781).

## <a name="what-is-gpu-compute"></a>GPU 계산 이란?

계산 집약적인 작업에 GPU 가속을 활용 하는 것을 일반적으로 "GPU 계산" 이라고 합니다. GPU 컴퓨팅은 GPU (그래픽 처리 장치)를 활용 하 여 수치 연산이 많은 워크 로드를 가속화 하 고 병렬 처리를 사용 하 여 CPU만 활용 하는 것 보다 많은 경우에 필요한 계산을 더 빠르게 완료 합니다. 이러한 병렬 처리는 CPU에서 실행 될 때 이러한 수학 집약적 작업에 대해 상당한 처리 속도를 향상 시킬 수 있습니다. 기계 학습 모델을 학습 하는 것은 GPU 계산에서이 계산 비용이 많이 드는 작업을 완료 하는 데 시간을 크게 단축할 수 있는 좋은 예입니다.

## <a name="install-and-set-up"></a>설치 및 설정

WSL 2 지원에 대 한 자세한 내용과 DirectML 문서 내의 [GPU 가속 교육 가이드](/windows/win32/direct3d12/gpu-accelerated-training) 에서 기계 학습 모델 학습을 시작 하는 방법을 알아보세요. 이 가이드에서는 다음 내용을 다룹니다.

* DirectML을 사용 하 여 TensorFlow를 설정 하는 초보자 또는 학생을 위한 지침
* 전문가 들이 기존에 사용할 수 있는 워크플로를 실행 하기 시작 하기 위한 지침