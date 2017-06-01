.. _Survey Tool:

###################
설문 도구
###################

.. note:: K-MOOC은 이 도구에 대해 전체 지원을 제공한다.

이 장에서 강좌에 설문을 추가하는 법을 알아보도록 하자.

.. contents::
   :local:
   :depth: 2

*********
개관
*********

여러 질문에 학습자가 어떠한 답변을 했는지 알아보기 위해 강좌에 설문을 추가할 수 있다.

설문에서 다양한 질문과 그에 대한 선택지를 설정할 수 있으며 각 질문에 대해 설문지 모음이 있게 된다. 질문이 하나라면  :ref:`Poll Tool` 를 참고하면 된다.

다음 예제는 각각 3개의 선택지를 갖는 문제 3개다.

.. image:: ../../../shared/images/survey.png
    :alt: A survey asking multiple questions about the learner's view of the
     course.
    :width: 600

답안 제출 결과를 비공개 하지 않았다면, 학습자는 설문에 답안을 제출한 후 그 시점의 결과를 조회할 수 있다.

.. image:: ../../../shared/images/survey_results.png
    :alt: The results of a survey asking multiple questions about the
     learner's view of the course.
    :width: 600

.. _Enable the Survey Tool:

*********************************************
설문 도구 설정하기
*********************************************

강좌에 설문을 추가하기 전에 Studio나 OLX에서 설문 도구를 설정해야 한다.

Studio에서 콘텐츠 보관함 도구를 설정하기 위해  ``"survey"`` 키를 고급 설정 페이지의 고급 모듈 목록에 추가한다. 반드시 키 값을 “ “ 사이에 입력한다. 자세한 사항은  :ref:`Enable Additional Exercises and Tools` 를 참고하면 된다.

또는 OLX를 사용해 설문 도구를 설정할 수 있다.

======================================
OLX에서 설문 도구 설정하기
======================================

설문 도구를 설정하기 위해 강좌 구조 XML 파일을 편집해야 한다.

``course`` 디렉토리에서 강좌 XML 파일을 연다.  ``course`` 요소의 ``advanced-modules`` 속성에 ``survey`` 스트링을 추가한다.

예를 들어 다음 XML 코드는 설문 도구를 설정한다.

.. code-block:: xml

  <course advanced_modules="[&quot;survey&quot;,
      &quot;poll&quot;]" display_name="Sample Course"
      start="2015-01-01T00:00:00Z">
      ...
  </course>

***************************
Studio에서 설문 추가하기
***************************

구성요소를 추가하기 전에 반드시 설문 도구를 고급 설정에서 추가해야 한다.

#. 강좌 개요 페이지에서 설문을 추가할 학습활동을 연다.

#. **새 구성요소 추가하기** 아래 고급으로 들어가 **설문** 을 클릭한다.

   학습활동에 새 구성요소가 추가되며 3개의 답변 필드와 3개의 질문이 있는 기본 설문이 나오게 된다.

   .. image:: ../../../shared/images/survey_studio.png
    :alt: The survey component in Studio.
    :width: 600

#. 새 구성요소에서 **편집** 을 선택한다.

#. **메뉴 이름** 필드에 구성요소 이름을 입력한다.

#. **피드백** 필드에 답변 제출 이후 학습자가 볼 텍스트를 입력한다.

#. **개별 결과** 필드에서 **True** 를 선택하면 학습자에게 설문 조사 결과를 숨길 수 있다. 만약 기본값인 **False** 로 놔두면 학습자는 답안 제출 후 결과를 조회할 수 있다.

#. **최대 제출** 필드에서 학습자가 답변을 제출할 수 있는 횟수를 정할 수 있다. 0을 입력하면 제출 제한이 없게 된다.

   .. note::
    학습자에게 답변 제출 기회를 여러 번 준다면 개별 결과를 True(비공개)로 설정하는 것이 좋다. 그렇지 않으면 학습자가 다른 학습자의 답변을 보고 바꿀 수도 있다.

#. 설문의 선택지를 설정한다. 각 선택지는 선택할 수 있는 버튼과 함께 하나의 열로 학습자에게 공개된다.

   #. 각 선택지 필드에 학습자가 볼 열 이름을 입력한다.

   #. 선택지를 추가하려면 편집기 하단의 선택지 추가를 선택한다. 목록 하단에 새로운 선택지가 추가된다.

   #. 목록 가장 위의 선택지는 학습자에게 설문지의 맨 좌측 열에 표시되고 목록 아래 선택지는 맨 우측 열에 표시된다. 선택지 순서를 바꾸기 위해 각 선택지 옆의 위, 아래 버튼을 클릭한다.

   #. 선택지를 삭제하려면, 삭제를 클릭한다.

#. 설문 질문을 설정한다. 각 질문은 학습자에게 맨 좌측 열에 표시된다.

   #. 텍스트나 이미지를 입력해야 하며 이미지를 사용한다면 이미지 :ref:`Studio URL <File URLs>` 을 사용하면 된다.

   #. 설문 템플릿엔 3개 질문이 포함된다. 질문을 추가하기 위해 편집기 하단의 질문 추가하기를 선택한다. 새 질문이 목록 하단에 추가된다.

   #. 이미지를 사용한다면 시각 장애가 있는 학습자를 위해 이미지 대체 텍스트 필드에 이미지에 대한 설명을 입력해야 한다.

   #. 질문은 설정한 순서대로 표시된다. 질문 순서를 바꾸기 위해선 질문 옆의 위, 아래 버튼을 클릭하면 된다.

   #. 질문을 삭제하려면 **삭제** 를 클릭한다.

#. **저장** 을 클릭한다.

***************************
OLX에 설문 추가하기
***************************

OLX에 설문 XBlock을 추가하기 위해  ``survey`` 요소를 생성한다.  ``survey`` 요소를  ``vertical`` 요소에 포함시킬 수 있고 ``survey`` 를 단독 요소로 할 수도 있다.

다음 예제는 4개의 답안이 있는 설문 조사를 보여준다.

.. code-block:: xml

  <survey
    url_name="unique identifier for the survey"
    xblock-family="xblock.v1"
    questions="[
                 [&quot;unique code for question 1&quot;,
                   {
                     &quot;img&quot;: &quot;Static URL to image&quot;,
                     &quot;img_alt&quot;: &quot;Alternative text for image&quot;,
                     &quot;label&quot;: &quot;Text of question 1&quot;
                   }
                 ],
                 [&quot;unique code for question 2&quot;,
                   {
                     &quot;img&quot;: &quot;Static URL to image&quot;,
                     &quot;img_alt&quot;: &quot;Alternative text for image&quot;,
                     &quot;label&quot;: &quot;Text of question 2&quot;
                    }
                  ]
                ]"
    feedback="Feedback displayed to learner after submission"
    private_results="false"
    block_name="Display name for survey"
    max_submissions="1"
    answers="[
              [
                &quot;Unique identifier for answer 1&quot;,
                &quot;Answer text&quot;
              ],
              [
                &quot;Unique identifier for answer 2&quot;,
                &quot;Answer text&quot;
              ]
            ]"
  />

==========================
survey 요소 속성
==========================

다음은 ``survey`` 요소의 속성이다.

.. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - ``url_name``
       - 설문 이름.
     * - ``xblock-family``
       - XBlock 버전. 반드시  ``xblock.v1`` 이어야 한다.
     * - ``questions``
       - 질문 목록. 각 질문은 이름과 다음 이름에 대한 값 설명이 포함되어 있다.

         * ``img``, 질문 이미지 URL.
         * ``img_alt``, 이미지 대체 설명.
         * ``label``, 질문 텍스트.

         각 질문은  ``img`` 이나  ``label`` 중 하나 이상이 포함되어야 한다.
     * - ``answers``
       - 답변 목록. 각 답변은 이름과 다음 이름에 대한 값 설명이 포함되어 있다.

         * ``img``, 답변 이미지 URL.
         * ``img_alt``, 이미지 대체 설명.
         * ``label``, 답변 텍스트.

         각 답변은 ``img`` 이나  ``label`` 중 하나 이상이 포함되어야 한다.
     * - ``feedback``
       - 답변을 제출했을 때 학습자에게 보여지는 텍스트.
     * - ``private_results``
       - 학습자에게 설문 조사 결과 공개 여부. (``true``) 는 공개, (``false``) 는 미공개.
     * - ``block_name``
       - 설문 조사 메뉴 이름.
     * - ``max_submissions``
       - 학습자 답변 제출 가능 횟수. 0을 입력하면 학습자는 답변을 무제한 제출할 수 있다. 1이 아닌 값을 입력한다면 학습자가 다른 학습자 답변을 본 후 다른 답변을 입력하는 것을 방지하기 위해 ``private_results`` 를  ``true`` 로 설정한다.

***************************
공개된 설문 편집하기
***************************

설문을 생성하고 충분히 테스트하기 전까지는 공개하지 않는 것이 좋다. 공개된 이후 설문을 바꾸는 것은 최대한 피하는 것이 좋다.

만약 학습자가 이미 답변을 제출했다면 다음과 같은 사항을 고려해야 한다.

* 답변 값을 바꾸게 되면 기존 제출된 답변은 변경된 값에 대한 답변으로 인식된다. 이는 부정확한 결과로 이어질 수 있다.

* 선택지 하나를 삭제하면 그 선택지를 고른 기존 답변들은 삭제되며 학습자는 새 답변을 제출할 수 있다.

***************************
설문 결과 조회하기
***************************

강좌 운영자가 설문을 조회할 때 강좌 내 설문의 결과를 볼 수 있다.

설문의 **결과 조회** 를 선택한다

.. image:: ../../../shared/images/survey_view_results.png
    :alt: A survey with the View Results button for course staff.
    :width: 600

The results of the survey are then displayed.

.. image:: ../../../shared/images/survey_results.png
    :alt: The results of a survey asking multiple questions about the
     learner's view of the course.
    :width: 600
