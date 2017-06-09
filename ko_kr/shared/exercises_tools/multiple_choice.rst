.. _Multiple Choice:

########################
선다형 문제
########################

.. note:: K-MOOC은 이 문제 유형에 대해 전체 지원을 제공한다.

.. contents::
  :local:
  :depth: 1

**********
개관
**********

선다형 문제(multiple choice problem)에서는 학습자가 선택지 가운데 하나를 선택한다. 학습자가 드롭다운(dropdown) 화살표를 클릭하기 전까지 선택지가 표시되지 않는 :ref:`Dropdown` 문제와 달리, 선다형 문제에서는 해당 질문지 아래에서 선택지를 가시적으로 직접 확인할 수 있다 .

.. image:: ../../../shared/images/MultipleChoiceExample.png
 :alt: A multiple choice problem.
 :width: 600

또한, 선다형 문제에는 각 학습자에게 일련의 선택지를 무작위로 제시하는 등, 몇 가지 고급 선택 조건이 있다.  :ref:`Multiple Choice Advanced Options` 에서 이들 선택 조건에 관한 보다 자세한 정보를 확인할 수 있다.

**************************************************
선다형 문제 성과 분석하기
**************************************************

강좌의 선다형 문제에 Insights를 사용해 학습자 성과 데이터 및 답안을 분석할 수 있다. 자세한 사항은  :ref:`Using edX Insights` 를 참고하면 된다.

********************************************************
선다형 문제에 대한 교육학적 고려사항
********************************************************

K-MOOC은 채점 문제에 대해 선다형 문제가 아닌 참평가를 사용할 것을 권장한다. 온라인 강좌에서 참평가를 사용할 때 더욱 좋은 결과를 보이기 때문이다. 또한, 참평가는 시도의 수에 제한이 없고 완전학습이 가능하며 도전적으로 학습할 수 있어서 더욱 좋은 결과가 나온다.

선다형 문제는 다음과 같은 장점을 갖는다.

* 채점되지 않는 선다형 문제는 학습자가 지식 전달 측면에서 그 개념을 생각해 볼 수 있도록 돕는다.

* 많은 분야에서 참평가의 사용이 어렵거나 불가능하다. 이러한 강좌에서 선다형 문제가 유일한 대안이 될 수도 있다.

다행히도 선다형 문제는 평가 분석에서 가장 연구가 활발하다. 문제를 만드는 방법에 대한 가이드라인은 다음과 같다.

* 답안 보기 조합을 논리적으로 짠다. 일관적인 어조로 작성하고 길이를 비슷하게 한다.

* 어간에 최대한 많은 단어를 배치하고 간결하게 작성한다.

* 함정 보기는 정답과 비교해 압도적으로 짧거나 길거나 구조가 달라선 안 된다. 모든 보기는 구조, 길이 및 어조가 비슷해야 한다.

* 부정형 (특히 이중 부정)의 사용을 피한다.

* 단순 암기를 테스트하는 것이 아닌 이해와 비판적 사고를 시험한다.

* 만약 풀이 횟수에 제한이 있다면 함정 문제를 내지 말고 보기를 최대한 간단하고 명료하게 한다.

* 모든 함정 보기는 타당하게 작성한다.

* “모든 보기가 정답이다”나 “정답이 없다” 는 주의하여 사용해야 한다. 만약 학습자가 보기를 2개만 알아도 정답을 유추해낼 수 있기 때문이다.

****************************************
선다형 문제 만들기
****************************************

간편 편집기 또는 고급 편집기에서 선다형 문제를 만들 수 있다. 우선 간편 편집기에서 문제를 만든 후 고급 편집기로 넘어가 XML의 다양한 설정을 사용할 수도 있다. 그러나 고급 편집기 사용 후 간편 편집기로 되돌아 올 수는 없다. 따라서 고급 편집기 사용 전에 문제 형식을 완벽히 만드는 것이 좋다.

.. _Use the Simple Editor to Create a Multiple Choice Problem:

================================================================
간편 편집기로 선다형 문제 만들기
================================================================

 :ref:`Simple Editor` 로 선다형 문제를 만들기 위해

#. **신규 구성요소 추가** 에서 문제 를 클릭한다.
#. 두가지 선다형 문제 템플릿에서 하나를 고른다.

  * **공통 문제 유형** 탭에서 **선다형 문항** 을 클릭한다.

  * 피드백과 힌트가 있는 공통 문제 유형 탭에서 피드백과 힌트가 있는 선다형 문항 을 클릭한다. 자세한 사항은  `선다형 문제에서 피드백 사용하기`_ 를 참고하면 된다.

    Studio는 학습활동에 문제를 추가한다.

#. **편집** 을 선택하면 간편 편집기가 열린다.
#. 예제 문제 텍스트를 바꾼다.
#. 표시로 사용할 문제의 텍스트를 결정한 후 해당 텍스트를 꺾쇠괄호 (``>>question<<``) 로 묶는다. 이 텍스트는 화면 판독기, 보고 및 Insights에서 활용된다.
#. 새로운 줄에 답안 보기 별로 텍스트를 바꾼다.
#. 선택지를 모두 선택한 후 **선다형 문제** 단추를 클릭한다. 이제 구성 요소 편집기가 각 정답 옆에 한 쌍의 괄호를 추가한다.
#. 정답 옆의 괄호 사이에 “x”를 입력한다.
#. 설명을 추가하기 위하여 설명 텍스트를 선택하고 도구 모음에서 **설명** ``[explanation]`` 을 클릭한다 
#. 설정을 선택하고 문제에 대한 **표시 이름** 을 추가한다.
#. 기타 설정을 지정한다. 자세한 사항은 :ref:`Problem Settings` 을 참고하면 된다
#. **저장** 을 클릭한다.

상기 예제에 대한 문제 구성요소 내부의 텍스트는 다음과 같다.

::

    >>Lateral inhibition, as was first discovered in the horsehoe crab:<<

    ( ) is a property of touch sensation, referring to the ability of crabs
    to detect nearby predators.
    ( ) is a property of hearing, referring to the ability of crabs to detect
    low frequency noises.
    (x) is a property of vision, referring to the ability of crabs' eyes to
    enhance contrasts.
    ( ) has to do with the ability of crabs to use sonar to detect fellow
    horseshoe crabs nearby.
    ( ) has to do with a weighting system in the crab's skeleton that allows
    it to balance in turbulent water.

    [Explanation]
    Horseshoe crabs were essential to the discovery of lateral
    inhibition, a property of vision present in horseshoe crabs as well as in
    humans that enables enhancement of contrast at edges of objects as was
    demonstrated in class. In 1967, Haldan Hartline received the Nobel prize
    for his research on vision and in particular his research investigating
    lateral inhibition using horseshoe crabs.
    [Explanation]

========================================================================
고급 편집기로 선다형 문제 만들기
========================================================================

:ref:`Advanced Editor` 로 선다형 문제를 만들기 위해

#. :ref:`Use the Simple Editor to Create a Multiple Choice Problem` 에서 문제를 만든다.
#. 고급 편집기를 선택하고 XML을 수정해 다음 예제와 같이 태그와 속성을 추가한다.

.. code-block:: xml

  <problem>
  <p>Lateral inhibition, as was first discovered in the horseshoe crab...</p>
  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" label="Lateral inhibition, as was first discovered
      in the horseshoe crab">
      <choice correct="false">is a property of touch sensation, referring to the ability
      of crabs to detect nearby predators.</choice>
      <choice correct="false">is a property of hearing, referring to the ability of crabs
      to detect low frequency noises.</choice>
      <choice correct="false">is a property of vision, referring to the ability of crabs'
      eyes to enhance contrasts.</choice>
      <choice correct="true">has to do with the ability of crabs to use sonar to detect
      fellow horseshoe crabs nearby.</choice>
      <choice correct="false">has to do with a weighting system in the crab's skeleton
      that allows it to balance in turbulent water.</choice>
    </choicegroup>
  </multiplechoiceresponse>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>Horseshoe crabs were essential to the discovery of lateral inhibition,
       a property of vision present in horseshoe crabs as well as humans that
       enables enhancement of contrast at edges of objects as was demonstrated in class.
       In 1967, Haldan Hartline received the Nobel prize for his research on vision
       and in particular his research investigating lateral inhibition using
       horseshoe crabs.</p>
    </div>
  </solution>
  </problem>

.. _Use Feedback in a Multiple Choice Problem:

********************************************
선다형 문제에서 피드백 사용하기
********************************************

간편 편집기나 고급 편집기를 사용해 선다형 문제에 피드백을 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

선다형 문제에서 학습자가 선택할 수 있는 각 보기에 대해 피드백을 추가할 수 있다. 피드백을 추가할 때 권장사항은 다음과 같다.

* 오답을 선택했을 때 흔한 오개념 및 실수에 대한 피드백을 추가한다.

* 정답을 유추할 수 있는 내용을 포함한 피드백을 추가한다.

* 정답을 선택했을 때 정답인 이유를 설명하는 피드백을 추가한다. 학습자는 문제를 찍어서 맞출 수도 있기 때문에 정답인 이유를 설명하는 피드백을 추가하는 것이 좋다.

=======================================
간편 편집기로 피드백 설정하기
=======================================

:ref:`Simple Editor` 에서 다음과 같이 피드백을 설정할 수 있다. 새로운 선다형 문제를 만들 때 힌트와 피드백이 있는 선다형 문제 템플릿을 고른다. 이 템플릿엔 예제가 포함되어 있다.

::

  ( ) Answer {{Feedback for learners who select this answer.}}

다음 예제는 각 보기에 대해 피드백이 있다.

::

  >>Which of the following is an example of a vegetable?<<
  ( ) apple {{An apple is the fertilized ovary that comes from an apple tree
  and contains seeds classifying it as a fruit.}}
  ( ) pumpkin {{A pumpkin is the fertilized ovary of a squash plant and
  contains seeds classifying it as a fruit.}}
  (x) potato {{A potato is an edible part of a plant in tuber form and is
  classified as a vegetable}}
  ( ) tomato {{Many people mistakenly think a tomato is a vegetable. However,
  because a tomato is the fertilized ovary of a tomato plant and contains
  seeds it is classified as a fruit.}}

=========================================
고급 편집기에서 피드백 설정하기
=========================================

:ref:`Advanced Editor` 에서 다음과 같이 피드백을 설정할 수 있다.

.. code-block:: xml

    <choice correct="false">
      Choice Label
      <choicehint>
        Feedback for when learner selects this answer.
      </choicehint>
    </choice>

다음 예제는 각 보기에 대해 피드백이 있다.

.. code-block:: xml

  <multiplechoiceresponse>
    <choicegroup label="Which of the following is an example of a vegetable?"
      type="MultipleChoice">
      <choice correct="false">apple
        <choicehint>An apple is the fertilized
          ovary that comes from an apple tree and contains seeds classifying
          it as a fruit.
        </choicehint>
      </choice>
      <choice correct="false">pumpkin
        <choicehint>A pumpkin is the fertilized
          ovary of a squash plant and contains seeds classifying it as a fruit.
        </choicehint>
      </choice>
      <choice correct="true">potato
        <choicehint>A potato is an edible part of a plant in tuber form and is
          classified as a vegetable.
        </choicehint>
      </choice>
      <choice correct="false">tomato
        <choicehint>Many people mistakenly think a tomato is a vegetable.
         However, because a tomato is the fertilized ovary of a tomato plant
         and contains seeds it is classified as a fruit.
        </choicehint>
      </choice>
    </choicegroup>
  </multiplechoiceresponse>

=========================
사용자 지정 피드백 라벨 설정하기
=========================

학습자는 기본적으로 **정답** 과 **오답** 피드백 라벨을 보게 된다. 만약 피드백 라벨 설정을 안하면 다음 예제와 같은 화면을 보게 된다.

.. image:: ../../../shared/images/multiple_choice_feedback.png
 :alt: Multiple choice feedback with the standard label.
 :width: 600

이런 기본 피드백 라벨을 수정할 수 있다. 예를 들어 특정 오답에 대해 다음과 같이 사용자 지정 피드백 라벨을 사용할 수 있다.

.. image:: ../../../shared/images/multiple_choice_feedback_custom_label.png
 :alt: Multiple choice feedback with a custom label.
 :width: 600

.. note::
  **정답** 과 **오답** 기본 라벨은 학습자의 언어로 보이게 된다. 그러나 사용자 지정 라벨을 사용하면 모두 설정 언어로 보이게 되며 번역되지 않는다.

간편 편집기에서 사용자 지정 피드백 라벨 설정하기
***********************************************

:ref:`Simple Editor` 에서 다음과 같이 사용자 지정 피드백 라벨을 설정한다.

::

  ( ) Answer {{Label:: Feedback for learners who select this answer.}}

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

::

  ( ) tomato {{Not Quite:: Many people mistakenly think a tomato is a
  vegetable. However, because a tomato is the fertilized ovary of a tomato
  plant and contains seeds, it is a fruit.}}

고급 편집기에서 사용자 지정 피드백 라벨 사용하기
*************************************************

:ref:`Advanced Editor` 에서 다음과 같이 사용자 지정 피드백 라벨을 설정한다.

.. code-block:: xml

    <choice correct="true or fale">Answer
      <choicehint label="Custom Label">
        Feedback for learners who select this answer.
      </choicehint>
    </choice>

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

.. code-block:: xml

  <choice correct="false">
    tomato
    <choicehint label="Not Quite">
      Many people mistakenly think a tomato is a vegetable. However, because
      a tomato is the fertilized ovary of a tomato plant and contains seeds,
      it is a fruit.
    </choicehint>
  </choice>

.. _Use Hints in a Multiple Choice Problem:

********************************************
선다형 문제에서 힌트 사용하기
********************************************

간편 편집기와 고급 편집기를 사용해 선다형 문제에 힌트를 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.


.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst

.. _Awarding Partial Credit in a Multiple Choice Problem:

****************************************************
선다형 문제에서 부분점수 사용하기
****************************************************

선다형 문제에서 특정 오답을 골랐을 때 학습자에게 부분점수를 부여할 수 있다. 반드시 `advanced editor <Use the Advanced Editor to Edit a Multiple Choice Problem>`_ 를 사용해야 한다.  

.. only:: Partners

 .. note::
    테스트서버와 kmooc.kr에서 부분점수를 사용하는 기능은 아직 개발 중이다. 사용 전에 확실히 테스트를 거쳐야 한다. 자세한 사항은 K-MOOC 운영팀에게 문의하면 된다.

다음 예제에서 학습자는 오답을 선택했으며 부분점수를 받았다.

.. image:: ../../../shared/images/partial_credit_multiple_choice.png
 :alt: A multiple choice problem with partial credit for an incorrect answer.
 :width: 600

오답에 대해 몇%의 점수를 얻게 되는지 설정할 수 있다. 만약 %를 설정하지 않으면 기본적으로 50%를 부여한다.

자세한 사항은 :ref:`Awarding Partial Credit for a Problem` 를 참고하면 된다.

=================================================================
선다형 문제에서 부분점수 설정하기
=================================================================

선다형 문제에서 부분점수를 설정하려면 문제 XML에 다음과 같은 속성을 추가해야 한다.

* ``<multiplechoiceresponse>`` 요소에  ``partial_credit="points"`` 속성을 추가한다.

* 부분점수를 부여할 각 보기마다  ``<choice>`` 요소에  ``correct="partial"`` 속성을 추가한다.

* 선택사항으로 각 보기마다 점수의 몇 %를 부여할지 선택할 수 있다.  ``<choice>`` 요소의 ``point_values`` 속성에서 십진법 숫자를 입력한다. 예를 들어 25%를 부여하기 위해 ``point_value="0.25"`` 를 추가할 수 있다. 부여되는 점수는 정답에 얼마나 근접했는지에 따라 다를 것이다. 만약  ``point_value`` 속성을 추가하지 않으면 기본적으로 50%의 점수를 부여한다.

다음 예제의 XML은 선다형 문제 템플릿에서 부분 점수 설정을 끝낸 것이다.

.. code-block:: xml

  <multiplechoiceresponse partial_credit="points">
    <choicegroup label="Which of the following countries has the largest
        population?" type="MultipleChoice">
      <choice correct="partial" point_value="0.25">Brazil</choice>
      <choice correct="false">Germany</choice>
      <choice correct="true">Indonesia</choice>
      <choice correct="false">Russia</choice>
    </choicegroup>
  </multiplechoiceresponse>


.. _Multiple Choice Problem XML:

******************************
선다형 문제 XML
******************************

================
템플릿
================

.. code-block:: xml

  <problem>
  <p>Question text</p>
  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" label="label text">
      <choice correct="false" name="a">
        Incorrect choice
        <choicehint>
          Hint for incorrect choice.
        </choicehint>
      </choice>
      <choice correct="true" name="b">
        Correct choice
        <choicehint>
          Hint for correct choice.
        </choicehint>
      </choice>
    </choicegroup>
  </multiplechoiceresponse>
  <demandhint>
    <hint>Hint 1</hint>
    <hint>Hint 2</hint>
  </demandhint>

  <solution>
    <div class="detailed-solution">
    <p>Explanation or solution header</p>
    <p>Explanation or solution text</p>
    </div>
  </solution>
  </problem>

================
태그
================

* ``<multiplechoiceresponse>`` (필수): 해당 문제가 선다형 문제임을 나타낸다.

* ``<choicegroup>`` (필수): 선택지 목록의 시작을 나타낸다.

* ``<choice>`` (필수): 선택지를 나열한다.

* ``<demandhint>`` (선택): 힌트를 나타낸다.

**Tag:** ``<multiplechoiceresponse>``

해당 문제가 선다형 문제임을 나타낸다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 부분점수 (선택)
       - 부분점수를 나타낸다. 사용될 경우 “점수(points)”로 설정되어야 한다.

  (none)

  Children

  * ``<choicegroup>``
  * 모든 표준 HTML 태그 (텍스트 포맷에 사용) .

**Tag:** ``<choicegroup>``

선택지 목록의 시작을 나타낸다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 라벨  (필수)
       - 답변 필드의 명칭을 지정한다.
     * - 유형 (필수)
       - 반드시 “선다형”으로 설정해야 한다.

  Children

  * ``<choice>``

**Tag:** ``<choice>``

Lists an answer option.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 정답 (최소 1개 필수)
       - 정답 혹은 오답임을 나타낸다.

         * “true”로 지정할 경우 해당 선택지는 정답이 된다.
         * “false”로 지정할 경우 해당 선택지는 오답이 된다.
         * “부분(parital)”으로 지정할 경우 해당 선택지는 부분점수를 주게 된다.

         하나 이상의 정답이나 부분 정답을 지정할 수 있지만 학습자는 정답으로 하나의 보기만 선택할 수 있다.

     * - 점수 값
       - ``correct="partial"`` 는 십진법으로 학습자가 얻게 될 부분점수를 나타낸다. 만약 ``point_value`` 가 설정되지 않으면 50%를 부분점수로 부여받게 된다.
     * - 명칭
       - 최종 사용자가 선택지를 지칭하는 데 사용하는 고유한 명칭이다.

  Children

  ``<choicehint>``

**Tag:** ``<choicehint>``

정답에 대한 힌트를 나타낸다.

**Tag:** ``<demandhint>``

학습자가 보게 될 힌트를 나타낸다.

  Children

  ``<hint>``

**Tag:** ``<hint>``

학습자가 보게 될 힌트를 나타낸다.

  Children

  (none)

.. _Multiple Choice Advanced Options:

*********************************************
선다형 문제 고급 선택 조건
*********************************************

선다형 문제에는 다양한 고급 선택 조건이 있다. 문제 안에 있는 선택지의 순서를 변경할 수 있고 학습자가 특정 오답을 선택할 경우 나타나는 설명을 삽입하거나 학습자별로 선택지 집합을 무작위로 제시할 수도 있다. 보다 자세한 정보가 필요할 경우 다음을 참조한다.

* :ref:`Shuffle Answers in a Multiple Choice Problem`
* :ref:`Targeted Feedback in a Multiple Choice Problem`
* :ref:`Answer Pools in a Multiple Choice Problem`

.. _Shuffle Answers in a Multiple Choice Problem:

=============================================
선다형 문제의 선택지 순서 변경하기
=============================================

선택 조건의 하나로, 선다형 문제의 구성을 변경하여 선택지 순서를 바꿀 수 있다.

가령, 어떤 학습자가 보는 문제 화면은 다음과 같을 수 있다.

::

 What Apple device competed with the portable CD player?

 ( ) The iPad
 ( ) Napster
 ( ) The iPod
 ( ) The vegetable peeler

동일한 문제에 대하여 다른 학습자 또는 위의 학습자가 보는 문제 화면을 다음과 같이 구성할 수 있다.

::

 What Apple device competed with the portable CD player?

 ( ) The iPad
 ( ) The iPod
 ( ) The vegetable peeler
 ( ) Napster

또한, 선택지 중 일부의 순서를 바꾸되 나머지는 그대로 둘 수도 있다. 이를테면 원래의 선택지 순서를 그대로 유지한 채 선택지 가장 아래에 “위의 모든 답(All of the Above)”이라는 항목을 둘 수 있다.

선택지 순서 변경과 관련한 문제 구성은 간편 편집기 또는 고급 편집기 로 가능하다. 또한 무작위 변수를 사용 안함이 아닌 다른 값으로 설정해야 한다. 자세한 사항은 :ref:`Randomization` 를 참고하면 된다. 


간편 편집기로 선택지 순서 변경하기
*********************************************

:ref:`Simple Editor` 에서 선택지 순서를 변경할 수 있다.

예를 들어, 선택지 순서 변경에 앞서 다음 텍스트로 정의되는 선다형 문제가 있다고 가정한다. 이때,  ``(x)`` 는 정답을 의미한다.

::

 >>What Apple device competed with the portable CD player?<<
     ( ) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler

이 문제의 선택지 순서를 바꾸려면 첫 번째 선택지의 괄호 사이에 느낌표 ``!`` 를 입력한다.

::

 >>What Apple device competed with the portable CD player?<<
     (!) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler

선택지 중 하나의 위치를 고정하려면 해당 선택지의 괄호 사이에 앳d ``@`` 을 삽입한다.

::

 >>What Apple device competed with the portable CD player?<<
     (!) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler
     (@) All of the above

필요에 따라 복수의 기호를 삽입할 수 있다. 이를테면 정답의 위치를 고정하고자 하는 경우 다음과 같이 할 수 있다.

::

  (x@) The iPod

간편 편집기에서 설정이 끝나면 **편집** 을 선택하고 **설정** 으로 들어가 **무작위** 설정을 **절대 안함** 이 아닌 다른 것임을 확인한다.

고급 편집기로 선택지 순서 변경하기
*********************************************

:ref:`Advanced Editor` 의 XML을 통해 선택지 순서를 변경할 수 있다.

예를 들어, 선택지 순서 변경에 앞서 다음 XML로 선다형 문제를 정의할 수 있다.

.. code-block:: xml

 <problem>
  <p>What Apple device competed with the portable CD player?</p>
  <multiplechoiceresponse>
   <choicegroup type="MultipleChoice">
     <choice correct="false">The iPad</choice>
     <choice correct="false">Napster</choice>
     <choice correct="true">The iPod</choice>
     <choice correct="false">The vegetable peeler</choice>
   </choicegroup>
  </multiplechoiceresponse>
 </problem>


이 문제의 선택지 순서를 변경하려면 ``<choicegroup>``  에  ``shuffle="true"`` 를 추가한다.

.. code-block:: xml

 <problem>
  <p>What Apple device competed with the portable CD player?</p>
  <multiplechoiceresponse>
   <choicegroup type="MultipleChoice" shuffle="true">
     <choice correct="false">The iPad</choice>
     <choice correct="false">Napster</choice>
     <choice correct="true">The iPod</choice>
     <choice correct="false">The vegetable peeler</choice>
   </choicegroup>
  </multiplechoiceresponse>
 </problem>


선택지 가운데 하나의 위치를 고정하려면 해당 선택지에 해당하는 ``choice`` 에   ``fixed="true"`` 를 추가한다.

.. code-block:: xml

 <problem rerandomize="always">
  <p>What Apple device competed with the portable CD player?</p>
  <multiplechoiceresponse>
   <choicegroup type="MultipleChoice" shuffle="true">
     <choice correct="false">The iPad</choice>
     <choice correct="false">Napster</choice>
     <choice correct="true">The iPod</choice>
     <choice correct="false">The vegetable peeler</choice>
     <choice correct="false" fixed="true">All of the above</choice>
   </choicegroup>
  </multiplechoiceresponse>
 </problem>

예제와 같이 무작위 값을  ``problem`` 요소로 하거나 **편집** 아래 **설정** 을 들어가 **무작위 설정** 을 **절대 안함** 이 아님을 확인한다.

.. _Targeted Feedback in a Multiple Choice Problem:

===============================================
선별적 피드백을 제공하는 선다형 문제
===============================================

오답에 대한 설명을 학습자에게 자동 제시하여 학습자가 정답을 찾는 데 안내가 되도록 선다형 문제를 구성할 수 있다. 따라서, 학습자가 정답을 찾을 때까지 답을 반복적으로 선택할 수 있는 선다형 문제에서는 선별적 피드백이 가장 유용한다.


고급 편집기로 선별적 피드백 구성하기
********************************************************

:ref:`Advanced Editor` 의 XML을 통해 선별적 피드백을 제공하는 문제를 구성한다.

다음 XML 가이드라인을 따른다.

* ``<multiplechoiceresponse>`` 에  ``targeted-feedback`` 속성을 추가한다. 값은 주지 않는다.
* ``<solution>`` 앞에 ``<targetedfeedbackset>`` 을 추가한다.
* ``<targetedfeedbackset>`` 내부에  ``<targetedfeedback>`` 을 1개 이상 추가한다.
* 아래의 설명과 같이 각 ``<targetedfeedback>`` 내부에 오답에 대한 설명을 HTML 마크업으로 입력한다.
* 각 오답에 대한 동일한 ``explanation-id`` 속성값을 이용하여 ``<targetedfeedback>`` 을 해당 오답에 연결한다.
* 정답에는  ``<solution>`` 을 이용한다. 이 때, 정답의  ``<choice>`` 와 동일한  ``explanation-id`` 속성값을 사용한다.

이를테면 선다형 문제에 대한 XML은 다음과 같다.

.. code-block:: xml

   <problem>
   <p>What Apple device competed with the portable CD player?</p>
   <multiplechoiceresponse targeted-feedback="">
    <choicegroup type="MultipleChoice">
      <choice correct="false" explanation-id="feedback1">The iPad</choice>
      <choice correct="false" explanation-id="feedback2">Napster</choice>
      <choice correct="true" explanation-id="correct">The iPod</choice>
      <choice correct="false" explanation-id="feedback3">The vegetable peeler</choice>
    </choicegroup>
   </multiplechoiceresponse>
   ...

이 뒤에 선별적 피드백을 정의하는 XML이 온다.

.. code-block:: xml

   ...
   <targetedfeedbackset>
     <targetedfeedback explanation-id="feedback1">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>The iPad came out later and did not directly compete with portable
            CD players.</p>
       </div>
     </targetedfeedback>
     <targetedfeedback explanation-id="feedback2">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>Napster was not an Apple product.</p>
       </div>
     </targetedfeedback>
     <targetedfeedback explanation-id="feedback3">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>Vegetable peelers do not play music.</p>
       </div>
     </targetedfeedback>
    </targetedfeedbackset>

    <solution explanation-id="correct">
     <div class="detailed-solution">
      <p>The iPod directly competed with portable CD players.</p>
     </div>
    </solution>
    </problem>

.. _Answer Pools in a Multiple Choice Problem:

=============================================
선택지 풀을 제공하는 선다형 문제
=============================================

선택지를 무작위로 조합한 하위 집합을 각 학습자에게 제시하는 선다형 문제를 구성할 수 있다. 가령, 해당 선다형 문제에 잠재적 정답 10가지를 부여한 후 5개의 선택지로 구성한 집합 1개를 각 학습자에게 제시할 수 있다.

전체 선택지(선택지 풀) 중에는 반드시 최소 1가지의 정답이 있어야 하며 그 개수는 2개 이상일 수도 있다. 1명의 학습자에게 제시되는 각 선택지 집합에는 1개의 정답이 포함된다. 이를테면, 10개로 구성된 선택지 집합에 2개의 정답이 있도록 문제를 구성할 수 있다. 각 학습자에게 제공되는 선택지 각각에 이 2가지 정답 가운데 하나가 포함된다.

고급 편집기로 선택지 풀 구성하기
**************************************************

:ref:`Advanced Editor` 의 XML을 통해 선택지 풀(answer pool)을 제공하는 문제를 구성한다.

다음 XML 지침을 따른다.

* ``<choicegroup>`` 에서  ``answer-pool`` 속성을 부여한다. 이 때, 숫자로 된 값은 해당 선택지 집합에 포함된 선택지의 개수를 나타낸다. 이를테면  ``<choicegroup answer-pool="4">`` 과 같이 구성할 수 있다.

* 각 정답의  ``<choice>`` 에 ``explanation-id`` 속성과 풀이에 해당하는 값을 부여한다. 이를테면,  ``<choice correct="true" explanation-id="iPod">The iPod</choice>`` 와 같이 구성할 수 있다.

* 각  ``<solution>`` 에  ``explanation-id`` 속성과 정답으로 되돌리는 값을 부여한다. 이를테면,  ``<solution  explanation-id="iPod">`` 와 같이 구성할 수 있다.

.. note:: 전체 선택지 가운데 정답이 단 1가지인 경우 ``choice`` 나  ``<solution>`` 에  ``explanation-id`` 속성을 부여할 필요가 없다. 그러나 이 경우에도  ``<solution>`` 을  끝내기 위해서  ``<solutionset>`` 속성을 부여해야 한다.

이를테면 다음 선다형 문제에서는 각 학습자에게 4가지 선택지로 구성된 선택지 집합이 제시되며 각 집합에 속한 선택지 가운데 1개가 전체 2가지 정답 가운데 하나가 된다. 정답에 표시되는 설명에는 동일한 설명 ID(explanation ID)가 부여된다.

.. code-block:: xml

 <problem>
  <p>What Apple devices let you carry your digital music library in your pocket?</p>
   <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" answer-pool="4">
      <choice correct="false">The iPad</choice>
      <choice correct="false">Napster</choice>
      <choice correct="true" explanation-id="iPod">The iPod</choice>
      <choice correct="false">The vegetable peeler</choice>
      <choice correct="false">The iMac</choice>
      <choice correct="true" explanation-id="iPhone">The iPhone</choice>
    </choicegroup>
   </multiplechoiceresponse>

    <solutionset>
        <solution explanation-id="iPod">
        <div class="detailed-solution">
            <p>Explanation</p>
            <p>Yes, the iPod is Apple's portable digital music player.</p>
        </div>
        </solution>
        <solution explanation-id="iPhone">
        <div class="detailed-solution">
            <p>Explanation</p>
            <p>In addition to being a cell phone, the iPhone can store and play your
               digital music.</p>
        </div>
        </solution>
    </solutionset>
 </problem>


