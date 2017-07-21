.. _Poll Tool:

###################
설문 조사 도구
###################

.. note:: K-MOOC은 이 도구에 대해 전체 지원을 제공한다.

다음 장은 강좌에 설문 조사를 추가하는 방법에 대해 설명한다.

.. contents::
   :local:
   :depth: 2

*********
개관
*********

강좌에 설문 조사를 추가해 다양한 질문에 대해 학습자의 의견을 모을 수 있다.

설문 조사에서 하나의 질문과 복수의 선택지를 만들 수 있다. 질문을 여러 가지 묻고 싶다면  :ref:`Survey Tool` 를 사용하면 된다.

다음 예제 설문 조사는 질문에 대해 선택지가 4가지 있다.

.. image:: ../../../shared/images/poll_tool.png
    :alt: A poll asking if the learner's favorite color is red, green, blue, or
     other.
    :width: 400

학습자가 설문 조사 질문 답변을 입력하면 결과가 공개되지 않도록 설정되지 않는 이상 당시의 설문 조사 결과를 조회할 수 있다.

.. image:: ../../../shared/images/poll_with_results.png
    :alt: A poll showing results after the learner has submitted a response.
    :width: 400

*******************************************
설문 조사 도구 설정하기
*******************************************

강좌에 설문 조사를 추가하기 전에 Studio나 OLX에서 설문 조사 도구를 설정해야 한다.

Studio에서 오피스 믹스 도구를 설정하기 위해  ``"poll"`` 키를 고급 설정 페이지의 고급 모듈 목록에 추가한다. 반드시 키 값을 “ “ 사이에 입력한다. 자세한 사항은  :ref:`Enable Additional Exercises and Tools` 를 참고하면 된다.


또는 OLX를 사용해 설문 조사 도구를 설정할 수도 있다.

======================================
OLX에서 설문 조사 도구 설정하기
======================================

강좌에서 설문 조사를 설정하기 위해 강좌 구조를 다루는 XML 파일을 편집해야 한다.

``course`` 디렉토리의 강좌 XML 파일을 연다. ``course`` 요소의  ``advanced-modules`` 속성에 스트링을 추가한다.

예를 들어 다음 XML 코드가 강좌 설문 조사를 설정한다.

.. code-block:: xml

  <course advanced_modules="[&quot;survey&quot;,
      &quot;poll&quot;]" display_name="Sample Course"
      start="2015-01-01T00:00:00Z">
      ...
  </course>

***************************
K-MOOC Studio에 설문 조사 추가하기
***************************

구성요소를 추가하기 전에 반드시 설문 조사를 설정해야 한다.

#. **강좌 개요** 페이지에서 설문 조사를 추가할 학습활동을 연다.

#. **신규 구성요소 추가** 아래의 **고급** 을 클릭하고 **설문 조사** 를 선택한다.

   새 구성요소가 학습활동에 추가되며 3개 선택지 필드를 포함한 기본 설문 조사가 추가된다.

   .. image:: ../../../shared/images/poll_studio.png
    :alt: The poll component in Studio.
    :width: 600

#. 새 구성요소에서 **편집** 을 선택한다.

#. 메뉴 이름 필드에 구성요소 이름을 입력한다.

#. 질문/프롬프트 필드에 설문 조사 위에 위치할 텍스트를 입력한다. 이 필드에 마크다운을 사용할 수 있다.

#. **피드백 필드** 에 응답을 제출한 후 학습자가 보게 될 텍스트를 입력한다. 이 필드에 마크다운을 사용할 수 있다.

#. **개별 결과** 필드에서 **True** 를 선택하면 학습자에게 설문 조사 결과를 숨길 수 있다. 만약 기본값인 **False** 로 놔두면 학습자는 답안 제출 후 결과를 조회할 수 있다.

#. **최대 제출 필드** 에서 학습자가 답변을 제출할 수 있는 횟수를 정할 수 있다. 0을 입력하면 제출 제한이 사라지게 된다.


   .. note::
    학습자에게 답변 제출 기회를 여러 번 준다면 **개별 결과** 를 **True** 로 설정하는 것이 좋다. 그렇지 않으면 학습자가 다른 학습자의 답변을 보고 바꿀 수도 있다.

#. 설문 조사 답안을 설정한다.

   #. 각 **선택지** 필드에 규학습자가 볼 답안 텍스트를 입력한다.

   #. 텍스트나 이미지를 입력해야 하며 이미지를 사용한다면 이미지 :ref:`File URLs` 을 사용하면 된다.

   #. 이미지를 사용한다면 시각 장애가 있는 학습자를 위해 **이미지 설명 이미지 대체 텍스트** 필드에 첨부해야 한다.

   #. 답안 추가를 위해 편집기 하단의 **답안 추가** 를 선택한다. 새로운 답안은 목록 하단에 추가된다.

   #. 답안 순서 변경을 위해 각 답안 옆의 버튼을 사용한다.

   #. 답안 제거를 위해 **삭제** 를 클릭한다.

#. **저장** 을 선택한다.

***************************
OLX에 설문 조사 추가하기
***************************

OLX에 설문 조사 XBlock을 추가하기 위해  ``poll`` 요소를 생성한다.  ``poll`` 요소를  ``vertical`` 요소에 포함시킬 수 있고 ``poll`` 를 단독 요소로 할 수도 있다.

다음 예제는 4개의 답안이 있는 설문 조사를 보여준다.

.. code-block:: xml

  <poll url_name="f4ae7de0006f426aa4eed4b0b8112da5" xblock-family="xblock.v1"
    feedback="Feedback"
    display_name="Poll"
    private_results="false"
    question="What is your favorite color?"
    max_submissions="1"
    answers="[
               [&quot;R&quot;,
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,
                   &quot;img_alt&quot;: &quot;Alt 1&quot;,
                   &quot;label&quot;: &quot;Red&quot;
                 }
               ],
               [&quot;B&quot;,
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,
                   &quot;img_alt&quot;: &quot;Alt 2&quot;,
                   &quot;label&quot;: &quot;Blue&quot;
                 }
               ],
               [&quot;G&quot;,
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,
                   &quot;img_alt&quot;: &quot;Alt3&quot;,
                   &quot;label&quot;: &quot;Green&quot;
                 }
               ],
               [&quot;O&quot;,
                 {
                   &quot;img&quot;: &quot;/static/image.png&quot;,
                   &quot;img_alt&quot;: &quot;Alt 4&quot;,
                   &quot;label&quot;: &quot;Other&quot;
                 }
               ]
             ]
  "/>

==========================
설문 조사 요소 속성
==========================

다음은 ``poll`` 요소에 대한 속성 표다.

.. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - ``url_name``
       - 설문 조사 이름.
     * - ``xblock-family``
       - XBlock 버전. 반드시 ``xblock.v1`` 이어야 한다.
     * - ``private_results``
       - 학습자에게 설문 조사 결과 공개 여부. (``true``) 는 공개 (``false``) 는 미공개. 
     * - ``display_name``
       - 설문 조사 메뉴 이름.
     * - ``question``
       - 설문조사 프롬프트.
     * - ``feedback``
       - 답변을 제출했을 때 학습자에게 보여지는 텍스트.
     * - ``max_submissions``
       - 학습자 답변 제출 가능 횟수. 0을 입력하면 학습자는 답변을 무제한 제출할 수 있다. 1이 아닌 값을 입력한다면 학습자가 다른 학습자 답변을 본 후 다른 답변을 입력하는 것을 방지하기 위해  ``private_results`` 를  ``true`` 로 설정한다.
     * - ``answers``
       - 답변 목록. 각 답변은 이름과 다음 이름에 대한 값 설명이 포함되어 있다.

         * ``img``, 답변 이미지 URL.
         * ``img_alt``, 이미지 대체 설명.
         * ``label``, 답변 텍스트.

         각 답변은  ``img`` 이나  ``label`` 중 하나 이상이 포함되어야 한다.

***************************
공개된 설문 조사 편집하기
***************************

설문 조사를 생성하고 충분히 테스트하기 전까지 공개하지 않는다. 공개된 이후 설문 조사를 바꾸는 것은 최대한 피하는 것이 좋다.

만약 학습자가 이미 답변을 제출했다면 다음과 같은 사항을 고려해야 한다.

* 답변 값을 바꾸게 되면 기존 제출된 답변은 변경된 값에 대한 답변으로 인식된다. 이는 부정확한 결과로 이어질 수 있다.

* 선택지 하나를 삭제하면 그 선택지를 고른 기존 답변들은 삭제되며 학습자는 새 답변을 제출할 수 있다.

***************************
설문 조사 결과 보기
***************************

강좌 운영자로서 설문 조사를 조회하면 강좌 내 설문 조사 결과를 볼 수 있다.

**결과 보기** 를 선택한다.

.. image:: ../../../shared/images/poll_view_results.png
    :alt: A poll with the View Results button for course staff.
    :width: 400

설문 조사 결과가 표시된다.

.. image:: ../../../shared/images/poll_with_results.png
    :alt: A poll showing results after the learner has submitted a response.
    :width: 400
