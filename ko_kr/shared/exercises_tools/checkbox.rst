.. _Checkbox:

##################
체크박스 문제
##################

.. note:: K-MOOC은 이 문제 유형에 대해 전체 지원을 제공한다.

.. contents::
  :local:
  :depth: 2

**********
개요
**********

체크박스 문제에서, 학습자는 선택지에서 하나 이상을 선택해야 한다. 또한 각 체크박스 문제에는 1개 이상의 정답이 있어야 한다.


.. image:: ../../../shared/images/CheckboxExample.png
 :alt: A checkbox problem with four options, two of which are correct.

.. note::
   문제는 모호하지 않아야 하고 함정문제는 피해야 한다. 체크박스 문제가 모호하면, 특히 답안 입력 횟수가 제한된 경우 학습자에게 혼동을 초래할 수 있다.


**************************************************
체크박스 문제 성과 분석
**************************************************

강좌의 체크박스 문제에 대해 K-MOOC Insights를 사용하여 축적된 학습자 성과 데이터를 분석할 수 있다. 자세한 사항은 K-MOOC :ref:`Using edX Insights` 를 참고하면 된다.


**************************************
체크박스 문제 만들기
**************************************

간편 편집기 또는 고급 편집기에서 체크박스 문제를 만들 수 있다. 우선 간편 편집기에서 문제를 만든 후 고급 편집기로 넘어가 XML의 다양한 설정을 사용할 수도 있다. 그러나 고급 편집기 사용 후 간편 편집기로 되돌아 올 수는 없다. 따라서 고급 편집기 사용 전에 완전히 문제 형식을 만드는 것이 좋다.


.. _Use the Simple Editor to Create a Checkbox Problem:

======================================================
간편 편집기를 사용해 체크박스 문제 만들기
======================================================

:ref:`Simple Editor` 를 사용해 체크박스 문제를 만들기 위해 아래의 단계를 따라야 한다.

#. 문제를 만들고 싶은 학습활동에서 **신규 구성요소 추가** 아래의 **문제** 를 클릭한다.

#. 두 가지 체크박스 문제 템플릿 중에 한가지를 고른다.

  * **일반 문제 유형** 에서 **체크박스** 또는 **힌트가 있는 체크박스** 를 클릭한다. 

  * 힌트가 있는 체크박스 관련, 자세한 사항은  `Use Feedback in a Checkbox Problem`_ 를 참고하면 된다.

    Studio는 학습활동에 체크박스 문제를 추가한다.

#. **편집** 을 클릭하면 간편 편집기가 열린다.
#. 예시 문제 텍스트를 지우고 새 텍스트를 입력한다.
#. 사용할 문제의 텍스트를 결정한 다음, 괄호 두 세트 (``>>question<<``) 로 해당 텍스트를 둘러싼다. 이 텍스트는 스크린 리더, 보고서 및 Insights에서 사용된다.
#. 기본 텍스트를 원하는 텍스트로 대체한다.
#. 모든 선택지를 선택한 다음, **체크박스** 버튼을 클릭한다. 이렇게 할 때, 각 선택지 옆에 괄호가 표시된다.
#. 정답 또는 답안에 대한 괄호 사이에 **x** 를 추가한다.
#. 설명을 추가하기 위해서 설명할 텍스트를 선택하고 도구 모음에서 **설명** 을 클릭한다.  ``[explanation]`` 가 설명 텍스트 앞뒤에 추가된다.
#. **설정** 을 클릭하고 문제에 대한 **메뉴명** 을 추가한다.
#. 문제에 대한 추가 설정을 선택한다. 자세한 사항은  :ref:`Problem Settings` 을 참고하면 된다.
#. **저장** 을 클릭한다.

위의 예제 문제에 대하여, 문제 구성 요소에 텍스트는 다음과 같다.

::

    Learning about the benefits of preventative healthcare can be particularly
    difficult. >>Check all of the reasons below why this may be the case.<<

    [x] A large amount of time passes between undertaking a preventative measure and seeing the result.
    [ ] Non-immunized people will always fall sick.
    [x] If others are immunized, fewer people will fall sick regardless of a particular individual's choice to get immunized or not.
    [x] Trust in healthcare professionals and government officials is fragile.

.. please do not line wrap this text.

    [explanation]
    People who are not immunized against a disease may still not fall sick from the disease. If someone is trying to learn whether or not preventative measures against the disease have any impact, he or she may see these people and conclude, since they have remained healthy despite not being immunized, that immunizations have no effect. Consequently, he or she would tend to believe that immunization (or other preventative measures) have fewer benefits than they actually do.
    [explanation]

========================================================================
고급 편집기를 사용해 체크박스 문제 편집하기
========================================================================

:ref:`Advanced Editor` 를 사용해 체크박스 문제를 편집하기 위해

#. :ref:`Use the Simple Editor to Create a Checkbox Problem` 를 이용해 문제를 만든다.
#. **고급 편집기** 를 선택하고 XML을 편집해 원하는 태그를 추가한다. 예를 들면 아래와 같다.

.. code-block:: xml

  <problem>
  <p>Learning about the benefits of preventative healthcare can be particularly difficult. Check all of the reasons below why this may be the case.</p>

  <choiceresponse>
    <checkboxgroup label="Check all of the reasons below why this may be the case">
      <choice correct="true"><text>A large amount of time passes between undertaking a preventative measure and seeing the result.</text></choice>
      <choice correct="false"><text>Non-immunized people will always fall sick.</text></choice>
      <choice correct="true"><text>If others are immunized, fewer people will fall sick regardless of a particular individual's choice to get immunized or not.</text></choice>
      <choice correct="true"><text>Trust in healthcare professionals and government officials is fragile.</text></choice>
    </checkboxgroup>
  </choiceresponse>

  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>People who are not immunized against a disease may still not fall sick from the disease. If someone is trying to learn whether or not preventative measures against the disease have any impact, he or she may see these people and conclude, since they have remained healthy despite not being immunized, that immunizations have no effect. Consequently, he or she would tend to believe that immunization (or other preventative measures) have fewer benefits than they actually do.</p>
   </div>
  </solution>
  </problem>

.. _Use Feedback in a Checkbox Problem:

********************************************
체크박스 문제에서 피드백 사용하기
********************************************

간편 편집기와 고급 편집기를 이용해 체크박스 문제에 피드백을 추가할 수 있다. 피드백에 관한 자세한 사항은 문제에 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

체크박스 문제에서 학습자가 고를 수 있는 보기에 대해 어떤 보기를 선택하는지에 따라 서로 다른 피드백을 추가할 수 있다. 이는 즉, 총 4가지 종류의 피드백이 존재할 수 있다는 뜻이다.

* 학습자가 정답을 고른다. 이 때 피드백은 정답인 이유를 설명한다.

* 학습자가 정답을 고르지 않는다. 이 때 피드백은 학습자가 이 보기를 고르지 않았다는 것을 알려주고 정답인 이유를 설명한다.

* 학습자가 오답을 고른다. 이 때 피드백은 학습자가 오답을 골랐다는 것을 알려주고 오답인 이유를 설명한다.

* 학습자가 오답을 고르지 않는다. 이 때 피드백은 학습자가 오답을 고르지 않은 것에 대한 추가 설명을 해준다.

=============================
복합 피드백
=============================

체크박스 문제를 설정하여 복합 피드백을 줄 수 있다. 복합 피드백은 특정 보기 조합에 대한 피드백이다. 예를 들어 만약 문제에 보기가 3가지 있다면 학습자가 특정 보기 조합을 골랐을 때 피드백이 나오도록 설정할 수 있다.


* A
* B
* C
* A, B
* B, C
* A, C
* A, B, C

보기가 3가지 이상인 문제는 각 조합에 대해 피드백을 따로 추가하는 것이 힘들 수 있다. 이 때 좀 더 선택될 가능성이 높거나 흔히 학습자가 틀릴 수 있는 조합에 대해 복합 피드백을 설정할 수 있다. 만약 학습자가 선택할 조합에 대해 피드백을 설정하지 않으면 개별 보기에만 피드백이 나오게 된다.

=======================================
간편 편집기에서 피드백 설정하기
=======================================

:ref:`Simple Editor` 에서 **개별 보기 및 복합 피드백** 을 설정할 수 있다. 새로운 체크박스 문제를 만들 때 힌트와 피드백이 있는 체크박스 템플릿을 선택한다. 이 템플릿은 피드백의 한 예시이다. 

개별 보기 피드백 설정하기
******************************************

간편 편집기에서 다음과 같이 개별 보기 피드백을 설정할 수 있다.

::

  [x] answer  {{ selected: Feedback when learner selects this option. },
  {unselected: Feedback when the learner does not select this option.}}

.. note:: ``selected`` 에 대해  ``S`` 를, unselected 에 대해  ``U`` 를 사용할 수 있다. 


예를 들어 다음 문제는 각 보기에 대한 피드백을 포함하고 있다.

::

  >>Which of the following is an example of a fruit? Check all that apply.<<

  [x] apple  {{ selected: You are correct that an apple is a fruit because it
  is the fertilized ovary that comes from an apple tree and contains seeds. },
  { unselected: Remember that an apple is also a fruit.}}

  [x] pumpkin {{ selected: You are correct that a pumpkin is a fruit because it
  is the fertilized ovary of a squash plant and contains seeds.}, { unselected:
  Remember that a pumpkin is also a fruit.}}

  [ ] potato   {{ U: You are correct that a potato is a vegetable because it is
  an edible part of a plant in tuber form.}, { S: A potato is a vegetable, not
  a fruit, because it does not come from the flower on a plant or tree and does
  not contain seeds.}}

  [x] tomato  {{ S: You are correct that a tomato is a fruit because it is the
  fertilized ovary of a tomato plant and contains seeds. }, { U: Many people
  mistakenly think a tomato is a vegetable. However, because a tomato is the
  fertilized ovary of a tomato plant and contains seeds it is classified as a
  fruit.}}


복합 피드백 설정하기
****************************

간편 편집기에서 다음과 같이 복합 피드백을 설정할 수 있다.

::

  {{ ((Answer Combination)) Feedback when learner selects this combination of
  options.}}

예를 들어 다음 복합 피드백은 학습자가 **A, B, 및 D 혹은 A, B, C, 및 D** 조합 을 선택했을 때 나타나게 된다.


::

  {{ ((A B D)) An apple, pumpkin, and tomato are all fruits as they are all the
  fertilized ovaries of a plant and contain seeds. }}

  {{ ((A B C D)) You are correct that an apple, pumpkin, and tomato are all
  fruits as they are all the fertilized ovaries of a plant and contain seeds.
  However, a potato is not a fruit as it is an edible part of a plant in tuber
  form and is classified as a vegetable.  }}

=========================================
고급 편집기에서 피드백 설정하기
=========================================

:ref:`Advanced Editor` 에서 개별 보기 및 복합 피드백을 설정할 수 있다.

개별 보기 피드백 설정하기
*************************************

고급 편집기에서 다음과 같이 개별 보기 피드백을 설정할 수 있다.

.. code-block:: xml

    <choice correct="true">Choice label
      <choicehint selected="true">
        Feedback for when learner selects this answer.
      </choicehint>
      <choicehint selected="false">
        Feedback for when learner does not select this answer.
      </choicehint>
    </choice>

예를 들어 다음 문제는 각 보기에 대한 피드백이다.

.. code-block:: xml

  <choiceresponse>
    <checkboxgroup label="Which of the following is an example
    of a fruit? Check all that apply.">
      <choice correct="true">apple
        <choicehint selected="true">You are correct that an apple is a fruit
          because it is the fertilized ovary that comes from an apple tree and
          contains seeds.
        </choicehint>
        <choicehint selected="false">Remember that an apple is also a
          fruit.
        </choicehint>
      </choice>
      <choice correct="true">pumpkin
        <choicehint selected="true">You are correct that a pumpkin is a fruit
          because it is the fertilized ovary of a squash plant and contains
          seeds.
        </choicehint>
        <choicehint selected="false">Remember that a pumpkin is also a
          fruit.
        </choicehint>
      </choice>
      <choice correct="false">potato
        <choicehint selected="true">A potato is a vegetable, not a fruit,
          because it does not come from the flower on a plant or tree and does
          not contain seeds.
        </choicehint>
        <choicehint selected="false">You are correct that a potato is
          classified as a vegetable because it is an edible part of a plant in
          tuber form.
        </choicehint>
      </choice>
      <choice correct="true">tomato
        <choicehint selected="true">You are correct that a tomato is
          classified as a fruit because it is the fertilized ovary of a tomato
          plant and contains seeds.
        </choicehint>
        <choicehint selected="false">Many people mistakenly think a tomato is
          a vegetable. However, because a tomato is the fertilized ovary of a
          tomato plant and contains seeds it is classified as a fruit.
        </choicehint>
      </choice>
    </checkboxgroup>
  </choiceresponse>

복합 피드백 설정하기
***************************

고급 편집기에서 ``<checkboxgroup>`` 요소 내의  ``<compoundhint>`` 요소에서 복합 피드백을 설정한다.

.. code-block:: xml

  <compoundhint value="Answer Combination">
    Feedback when learner selects this combination of answers.
  </compoundhint>}}

예를 들어 다음 복합 피드백은 학습자가 **A, B, 및 D** 혹은 **A, B, C, 및 D** 조합을 선택했을 때 나타나게 된다.

.. code-block:: xml

  <compoundhint value="A B D">An apple, pumpkin, and tomato are all fruits as
    they all are fertilized ovaries of a plant and contain seeds.
  </compoundhint>
  <compoundhint value="A B C D">You are correct that an apple, pumpkin, and
    tomato are all fruits as they all are fertilized ovaries of a plant and
    contain seeds. However, a potato is not a fruit as it is an edible part of
    a plant in tuber form and is classified as a vegetable.
  </compoundhint>

.. _Use Hints in a Checkbox Problem:

********************************************
체크박스 문제에서 힌트 사용하기
********************************************

간편 편집기 및 고급 편집기를 사용해 체크박스 문제에 힌트를 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst

.. _Awarding Partial Credit in a Checkbox Problem:

*********************************************
체크박스 문제에서 부분점수 주기
*********************************************

체크박스 문제에서 학습자에게 부분점수를 부여할 수 있다. 반드시 `advanced editor <Use the Advanced Editor to Edit a Checkbox Problem>`_ 를 사용하여야 한다.

부분 점수에 대한 설명은 :ref:`Awarding Partial Credit for a Problem` 를 참고하면 된다.

.. only:: Partners

 .. note::
    테스트서버와 kmooc.kr에서 부분점수를 사용하는 것은 아직 개발 중에 있다. 학습자에게 제공하기 전에 충분한 테스트를 거칠 필요가 있으며 자세한 사항은 파트너 매니저에게 (K-MOOC 관리자에게) 문의하면 된다.

다음 예제에서 학습자는 정답 3개 중 2개를 골랐으며 오답을 고르지 않았다. 학습자는 따라서 5개 정답 중 4개를 맞춘 것이라고 볼 수 있다. 강좌 운영팀은 고른 정답과 고르지 않은 오답에 대해 부분점수를 설정하였기 때문에 학습자는 이 문제에서 80%의 점수를 얻었다.

.. image:: ../../../shared/images/checkbox_partial_credit.png
 :alt: A checkbox choice problem with partial credit for two out of
     three answers.
 :width: 600


체크박스 문제에서 부분점수를 부여하는 방법은 두 가지 있다.

.. contents::
  :local:
  :depth: 1

.. _Every Decision Counts:

======================================
모든 선택에 부분점수 부여하기
======================================

체크박스 문제에서 학습자의 모든 선택에 대해 부분점수를 부여할 수 있다. 이 방식은 “모든 선택에 대한 부분점수”(EDC)이라고 부른다.

EDC에서 학습자는 정답을 고르지 않거나 오답을 골라 틀리는 보기에 대해 1/n만큼 점수를 잃는다. 이 때 “n”은 보기의 숫자를 의미한다.

예를 들어 만약 보기가 4개가 있고 각 보기가 25%의 점수를 갖는다고 하면 학습자가 하나의 보기를 틀렸을 경우 75%의 점수를 받는다.

다음 표는 EDC 문제에서 여러 정답 조합에 대해 학습자의 점수가 어떻게 달라질 수 있는지 보여준다.

.. list-table::
     :widths: 20 20 20 20
     :header-rows: 1

     * - 학습자 선택
       - 정답
       - 오답
       - 점수
     * - A, B, C
       - A, B, D
       - C
       - 75%
     * - A
       - A, C, D
       - B
       - 75%
     * - A, C
       - A, D
       - B, C
       - 50%
     * - C, D
       -
       - A, B, C, D
       - 0%

EDC 체크박스 문제 설정하기
**********************************

EDC 체크박스 문제를 설정하려면 문제 XML 내의 ``<choiceresponse>`` 요소에 ``partial_credit="EDC"`` 속성을 추가해야 한다. 

예를 들어 다음 XML은 부분 점수가 포함된 체크박스 문제를 보여준다.

.. code-block:: xml

  <choiceresponse partial_credit="EDC">
    <checkboxgroup label="Which of the following is a fruit? Check all that apply.">
      <choice correct="true">apple</choice>
      <choice correct="true">pumpkin</choice>
      <choice correct="false">potato</choice>
      <choice correct="true">tomato</choice>
    </checkboxgroup>
  </choiceresponse>

=======================
절반 형식 사용하기
=======================

학습자가 정답을 고르지 않거나 오답을 골라 틀리게 되는 모든 보기에 대해 남은 점수의 절반을 잃게 되는 방식을 사용할 수 있다. 이를 **절반** 형식이라고 부른다.


.. note:: 절반 부분점수의 경우 오답 보기에 비해 정답 보기가 2배 이상 많아야 한다. 또한 총 정답 보기의 숫자와 관계 없이 오답 세 개 이상에 대해 부분점수가 주어지지 않는다. 즉 보기가 5개 이상인 경우에 한해서만 2개의 오답에 대해 25%의 점수를 줄 수 있는 것이다. 3개 이상의 오답은 총 보기 개수와 관계 없이 0%의 점수를 얻는다.

절반 부분점수의 계산법은 다음과 같다.

* 오답이 없을 경우 점수의 100%를 획득한다.

* 오답이 하나 있고 보기 숫자가 3개 이상일 경우 점수의 50%를 획득한다. 오답이 하나 있고 보기가 2개라면 점수를 얻지 못한다.

* 오답이 2개 있고 보기가 5개 이상일 경우 점수의 25%를 획득한다. 오답이 2개 있고 보기가 3개 혹은 4개 있을 경우 점수를 얻지 못한다.

* 오답이 3개일 경우 보기의 수에 관계 없이 점수를 얻지 못한다.

다음은 총 보기의 수에 따른 절반 부분점수의 점수표다.

.. list-table::
     :widths: 30 30 30
     :header-rows: 1

     * - Number of Incorrect Answers
       - Number of Answer Options
       - Credit Given (%)
     * - 0
       - 2
       - 100
     * - 1
       - 2
       - 0
     * - 2
       - 2
       - 0

.. list-table::
     :widths: 30 30 30
     :header-rows: 1

     * - Number of Incorrect Answers
       - Number of Answer Options
       - Credit Given (%)
     * - 0
       - 3
       - 100
     * - 1
       - 3
       - 0
     * - 2
       - 3
       - 0
     * - 3
       - 3
       - 0

.. list-table::
     :widths: 30 30 30
     :header-rows: 1

     * - Number of Incorrect Answers
       - Number of Answer Options
       - Credit Given (%)
     * - 0
       - 4
       - 100
     * - 1
       - 4
       - 50
     * - 2
       - 4
       - 0
     * - 3
       - 4
       - 0
     * - 4
       - 4
       - 0

.. list-table::
     :widths: 30 30 30
     :header-rows: 1

     * - Number of Incorrect Answers
       - Number of Answer Options
       - Credit Given (%)
     * - 0
       - 5
       - 100
     * - 1
       - 5
       - 50
     * - 2
       - 5
       - 25
     * - 3
       - 5
       - 0
     * - 4
       - 5
       - 0
     * - 5
       - 5
       - 0

.. list-table::
     :widths: 30 30 30
     :header-rows: 1

     * - Number of Incorrect Answers
       - Number of Answer Options
       - Credit Given (%)
     * - 0
       - 7
       - 100
     * - 1
       - 7
       - 50
     * - 2
       - 7
       - 25
     * - 3
       - 7
       - 0
     * - 4
       - 7
       - 0
     * - 5
       - 7
       - 0


절반 부분점수 체크박스 문제 설정하기
************************************

절반 부분점수 체크박스 문제를 설정하기 위해 문제 XML에서 ``<choiceresponse>`` 요소에 ``partial_credit="halves"`` 속성을 추가해야 한다. 

예를 들어 다음 XML은 부분 점수가 포함된 체크박스 문제를 보여준다.

.. code-block:: xml

  <choiceresponse partial_credit="halves">
    <checkboxgroup label="Which of the following is a fruit? Check all that apply.">
      <choice correct="true">apple</choice>
      <choice correct="true">pumpkin</choice>
      <choice correct="false">potato</choice>
      <choice correct="true">tomato</choice>
    </checkboxgroup>
  </choiceresponse>


.. _Checkbox Problem XML:

****************************
체크박스 문제 XML (권장하지 않음)
****************************

============
템플릿
============

.. code-block:: xml

  <problem>
  <legend>Question text</legend>
  <choiceresponse>
    <checkboxgroup label="label text">
      <choice correct="false">
        Answer option A (incorrect)
        <choicehint selected="true">
          Feedback for when learner selects this answer.
        </choicehint>
        <choicehint selected="false">
          Feedback for when learner does not select this answer.
        </choicehint>
      </choice>
      <choice correct="true">
        Answer option B (correct)
        <choicehint selected="true">
          Feedback for when learner selects this answer.
        </choicehint>
        <choicehint selected="false">
          Feedback for when learner does not select this answer.
        </choicehint>
      </choice>
      <choice correct="false">
        Answer option C (correct)
        <choicehint selected="true">
          Feedback for when learner selects this answer.
        </choicehint>
        <choicehint selected="false">
          Feedback for when learner does not select this answer.
        </choicehint>
      </choice>
      <compoundhint value="A B">
        Feedback when answers A and B are selected.
      </compoundhint>
     <compoundhint value="A C">
        Feedback when answers A and C are selected.
      </compoundhint>
    </checkboxgroup>
  </choiceresponse>

  <demandhint>
    <hint>Hint 1</hint>
    <hint>Hint 2</hint>
    <hint>Hint 3</hint>
  </demandhint>

  <solution>
    <div class="detailed-solution">
      <p>Solution or Explanation Heading</p>
      <p>Solution or explanation text</p>
     </div>
  </solution>
  </problem>

======
태그
======

* ``<choiceresponse>`` (필수사항): 학습자들이 선택할 수 있는 옵션을 포함하는 문제를 설정한다.

* ``<checkboxgroup>`` (필수사항): 문제가 체크박스 문제임을 설정한다.

* ``<compoundhint>`` (선택사항): 특정 답안에 대한 피드백을 지정한다.

* ``<choice>`` (필수사항): 답안 옵션을 지정한다

* ``<demandhint>`` (선택사항): 학습자에게 힌트를 제공한다.

**Tag:** ``<choiceresponse>``

학습자들이 선택할 수 있는 옵션을 포함하는 문제를 설정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - 부분 점수 (선택사항)
       - 부여되는 부분 점수를 지정한다. ``EDC`` 혹은  ``halves``

  Children

  ``<checkboxgroup>``

**Tag:** ``<checkboxgroup>``

문제가 체크박스 문제임을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - 라벨 (필수사항)
       - 응답 입력 필드의 이름을 지정한다.

  Children

  ``<choice>``
  ``<compoundhint>``

**Tag:** ``<choice>``

답안 옵션을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - true (최소 하나 필수)
       - 정답을 나타낸다. 체크박스 문제에 대하여, 하나 이상의 ``<choice>`` 태그는 정답을 포함할 수 있다.
     * - false (최소 하나 필수)
       - 오답을 나타낸다.

  Children

  ``<choicehint>``

**Tag:** ``<choicehint>``

답안 보기에 대한 힌트를 나타낸다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - selected (필수사항)
       -답안 보기에 대해 힌트가 주어졌는지 여부를 나타낸다. ``true`` 혹은 ``false`` 

  Children

  (none)

**Tag:** ``<compoundhint>``

특정 답안 조합에 대한 피드백을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - 값 (최소 하나 필수)
       - 피드백이 나오기 위해 어떤 답안의 조합이 필요한지 나타낸다.

  Children

  (none)

**Tag:** ``<demandhint>``

학습자가 보게 될 힌트를 나타낸다.

  Children

  ``<hint>``

**Tag:** ``<hint>``

학습자가 보게 될 힌트를 나타낸다.

  Children

  (none)

