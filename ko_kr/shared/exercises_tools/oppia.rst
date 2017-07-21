.. include:: ../../../links/links.rst

.. _Oppia Exploration Tool:

##########################
Oppia 탐구 도구
##########################

.. note:: K-MOOC은 이 도구에 대해 전체 지원을 제공한다.

`Oppia`_ 는 탐구라 불리는 짧은 상호작용 (혹은 쌍방향) 가이드라인을 만들 수 있는 외부 도구이다. 이번 장에서 Oppia 탐구를 강좌에 추가하는 법에 대해 알아보자.

.. contents::
  :local:
  :depth: 2

외부 사이트의 콘텐츠를 강좌에 추가할 때 장애가 있는 학습자가 사용할 수 있는지 확인해야 한다. 자세한 사항은  :ref:`Accessibility Best Practices for Course Content Development` 를 참고하면 된다.

*********
개관
*********

Studio에서 Oppia 탐구 도구를 활용해 탐구라고 부르는 상호작용 가이드를 강좌에 추가한다. Oppia 탐구는 경험학습이 가능하도록 튜터와의 소통을 촉발시킨다.

.. note:: Oppia 탐구는 채점할 수 없다. 현재 Oppia 탐구 구성요소는 채점되는 소주제에 사용해선 안 된다.

다음 예제는 K-MOOC 학습 관리 시스템에서 학습자들이 보게 될 Oppia 탐구 화면이다.

.. image:: ../../../shared/images/oppia.png
  :alt: An Oppia exploration in the course.
  :width: 800

Oppia 탐구를 만드는 방법은  `Oppia User Documentation`_  를 참고하면 된다.

.. _Enable the Oppia Exploration Tool:

*********************************************
Oppia 탐구 도구 설정하기
*********************************************

Oppia 탐구를 먼저 Studio에서 설정한 후 강좌에 추가할 수 있다.

Studio에서 오피스 믹스 도구를 설정하기 위해  ``"oppia"`` 키를 고급 설정 페이지의 고급 모듈 목록에 추가한다. 반드시 키 값을 “ “ 사이에 입력한다. 자세한 사항은  :ref:`Enable Additional Exercises and Tools` 를 참고하면 된다.

***********************************
Studio에 Oppia 탐구 추가하기
***********************************

강좌에 Oppia 탐구를 포함한 구성요소를 추가하기 전에 먼저 Oppia 탐구 도구를 설정해야 한다. 추가할 Oppia 탐구를 선택해 탐색을 호스트하는 사이트의 URL과 ID를 먼저 찾아야 한다.

#. **강좌 개요** 페이지에서 채점이 되지 않는 소주제에서 탐구를 추가할 학습활동을 연다.

#. **신규 구성요소 추가** 의 **고급** 에서 Oppia 탐구를 선택한다. 새 구성요소가 학습활동에 추가된다.

#. 추가된 새 구성요소에서 **편집** 을 선택한다.

   .. image:: ../../../shared/images/oppia_studio.png
     :alt: The Edit component dialog box for an Oppia exploration in Studio.
     :width: 600

#. **구성요소 메뉴 이름** 필드에 구성요소 이름을 입력한다. 학습 관리 시스템에는 이 이름이 탐구의 제목으로 표시된다.

#. Oppia 탐구 ID 필드에 추가할 탐색 번호를 입력한다. 예를 들어  ``qG6kclSxlWZn`` 나  ``gC4_ggkWar-L`` 처럼 입력하면 된다.

#. Oppia 서버 URL 필드에 추가할 탐구의 호스트 사이트를 입력한다. 예를 들어  ``www.oppia.org`` 처럼 입력하면 된다.

#. **저장** 을 클릭한다.

   Studio는 학습활동 페이지에 탐구를 표시하지 않는다. 추가한 탐구를 확인하기 위해 **미리보기** 를 클릭하거나 학습활동을 공개하고 **실시간 보기** 를 클릭한다.

