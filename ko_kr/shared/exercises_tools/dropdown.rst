.. _Dropdown:

#####################
드롭다운 문제
#####################

.. note:: K-MOOC은 이 문제 유형에 대해 전체 지원을 제공한다.

.. contents::
  :local:
  :depth: 1

**********
개관
**********

드롭다운(Dropdown) 문제는 학습자가 드롭다운 목록으로 표시된 답안 옵션 모음에서 답안을 선택할 수 있도록 한다. 답안이 항상 질문 바로 아래 표시되는 다중 선택형 문제와는 달리, 드롭다운 문제는 학습자가 드롭다운 화살표 클릭 때까지 답안 선택안을 보여주지 않는다.

.. image:: ../../../shared/images/DropdownExample.png
 :alt: A problem component with 3 dropdown problems, 2 marked correct and 1
     incorrect.
 :width: 600

**************************************************
드롭다운 문제 성과 분석하기
**************************************************

강좌의 드롭다운 문제에 대해 K-MOOC Insights를 사용하여 학습자 성과 데이터 및 제출된 답안을 분석할 수 있다. 자세한 사항은  :ref:`Using edX Insights` 를 참고하면 된다.


********************************
드롭다운 문제 만들기
********************************

간편 편집기 또는 고급 편집기에서 드롭다운 문제를 만들 수 있다. 우선 간편 편집기에서 문제를 만든 후 고급 편집기로 넘어가 XML의 다양한 설정을 사용할 수도 있지만 고급 편집기 사용 후 간편 편집기로 되돌아 올 수는 없다. 따라서 고급 편집기 사용 전에 문제 형식을 완전히 만드는 것이 좋다.


.. _Use the Simple Editor to Create a Dropdown Problem:

========================================================================
간편 편집기
========================================================================

드롭다운 문제를 만들기 위해 다음 단계를 따르도록 한다.

#. 신규 구성요소 추가 에서 **문제** 를 클릭한다.

#. 두 드롭다운 문제 템플릿 중 하나를 선택한다.

  * **일반적인 문제 유형** 에서 **드롭다운** 을 선택한다.

  *힌트와 피드백이 있는 일반적인 문제 유형에서 힌트와 피드백이 있는 드롭다운을 선택한다. 자세한 사항은 `Use Feedback in a Dropdown Problem`_ 를 참고하면 된다.

    Studio는 문제를 학습활동에 추가한다.

#. **편집** 을 클릭하면 간편 편집기가 열린다.
#. 예제 텍스트를 문제에 대한 텍스트로 대체한다.
#. 라벨로 사용할 문제의 텍스트를 결정한 다음, 꺾쇠 괄호 두 세트(``>>question<<``)로 해당 텍스트를 둘러싼다. 이 텍스트가 화면 판독기, 보고, Insights 등에서 사용된다.
#. 쉼표로 구분하여 같은 줄에 각각의 가능한 답안을 입력한다.
#. 모든 답안 옵션을 선택한 다음, 드롭다운 버튼을 클릭한다. 이 작업을 수행하는 경우 대괄호 ([[])의 이중 세트가 나타나고 답안 옵션을 둘러싼다.
#. 대괄호 내에서, 괄호로 정답을 둘러싼다.
#. 설명을 첨부하려면 텍스트를 선택하고 도구 모음에서 설명을 클릭한다.  ``[explanation]`` 가 설명 텍스트 주변에 나타난다.
#. **설정** 을 선택하고 문제의 메뉴명을 작성한다.
#. 기타 고급 설정을 정한다. 자세한 사항은 :ref:`Problem Settings` 을 참고하면 된다.
#. **저장** 을 클릭한다.


위의 예제 문제에 대하여, 문제 구성요소에서 텍스트는 다음과 같다.

::

    >>What type of data are the following?<<

    Age:
    [[Nominal, Discrete, (Continuous)]]
    Age, rounded to the nearest year:
    [[Nominal, (Discrete), Continuous]]
    Life stage - infant, child, and adult:
    [[(Nominal), Discrete, Continuous]]

========================================================================
고급 편집기
========================================================================

고급 편집기로 드롭다운 문제를 편집하기 위해

#. :ref:`Use the Simple Editor to Create a Dropdown Problem` 에 나와 있는 대로 문제를 만든다.
 
#. **고급 편집기** 를 선택하고 XML을 편집하여 태그와 속성을 추가한다. 예를 들어


**문제 코드**:

.. code-block:: xml

  <problem>
  <p>
    <em>This exercise first appeared in HarvardX's PH207x Health in Numbers:
    Quantitative Methods in Clinical &amp; Public Health Research course, fall
    2012.</em>
  </p>
  <p>What type of data are the following?</p>
  <p>Age:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')"
      correct="Continuous" label="Age"/>
  </optionresponse>
  <p>Age, rounded to the nearest year:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')"
      correct="Discrete" label="Age, rounded to the nearest year"/>
  </optionresponse>
  <p>Life stage - infant, child, and adult:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')"
      correct="Nominal" label="Life stage"/>
  </optionresponse>
  </problem>

.. _Use Feedback in a Dropdown Problem:

********************************************
드롭다운 문제에서 피드백 사용하기
********************************************

간편 편집기나 고급 편집기를 사용해 드롭다운 문제에 피드백을 추가할 수 있다. 문제 피드백의 개관을 보기 위해선 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

드롭다운 문제에서 학습자가 고를 수 있는 선택지 마다 피드백을 추가할 수 있다. 다음은 피드백과 관련된 지침이다.

* 흔히 틀리는 오답에 피드백을 추가한다.

* 어느정도 정답을 유추할 수 있게 하는 피드백을 추가한다.

* 정답인 이유를 설명하는 피드백을 추가한다. 학습자는 찍어서 문제를 맞출 수도 있기 때문에 그 이유를 설명하는 것은 중요하다.


=======================================
간편 편집기에서 피드백 설정하기
=======================================

:ref:`simple editor<Simple Editor>` 에서 다음과 같이 답안 피드백을 설정할 수 있다. 새 드롭다운 문제를 만들 때 힌트와 피드백이 있는 드롭다운 템플릿을 선택한다. 그 후 원하는 내용으로 예제를 바꾸면 된다.


::

  Wrong Answer {{Feedback for learners who select this answer.}}
  (Correct Answer) {{Feedback for learners who select this answer.}}

예를 들어 다음 문제는 각 보기에 대해 피드백이 있다.

::

  >>A/an ________ is an example of a vegetable.<<

  [[
    apple {{An apple is the fertilized ovary that comes from an apple tree and
      contains seeds classifying it as a fruit.}}
    pumpkin {{A pumpkin is the fertilized ovary of a squash plant and contains
      seeds classifying it as a fruit.}}
    (potato) {{A potato is an edible part of a plant in tuber form and is
      classified as a vegetable}}
    tomato {{Many people mistakenly think a tomato is a vegetable. However,
      because a tomato is the fertilized ovary of a tomato plant and contains
      seeds it is classified as a fruit.}}
  ]]

=========================================
고급 편집기에서 피드백 설정하기
=========================================

:ref:`Advanced Editor` 에서 다음과 같이 피드백을 설정할 수 있다.

.. code-block:: xml

    <option correct="False">
      Option Label
      <optionhint>
        Feedback for when learner selects this answer.
      </optionhint>
    </option>

예를 들어 다음 문제는 각 보기에 대해 피드백이 있다.

.. code-block:: xml

  <optionresponse>
    <optioninput label="A/an ________ is an example of a vegetable.">
      <option correct="False">
        apple
        <optionhint>
          An apple is the fertilized ovary that comes from an apple tree and
          contains seeds classifying it as a fruit.
        </optionhint>
      </option>
      <option correct="False">
        pumpkin
        <optionhint>
          A pumpkin is the fertilized ovary of a squash plant and contains
          seeds classifying it as a fruit.
        </optionhint>
      </option>
      <option correct="True">
        potato
        <optionhint>
          A potato is an edible part of a plant in tuber form and is
          classified as a vegetable.
        </optionhint>
      </option>
      <option correct="False">
        tomato
        <optionhint>
          Many people mistakenly think a tomato is a vegetable. However,
          because a tomato is the fertilized ovary of a tomato plant and
          contains seeds it is classified as a fruit.
        </optionhint>
      </option>
    </optioninput>
  </optionresponse>

=========================
사용자 정의 피드백 라벨
=========================

기본적으로 학습자가 보는 피드백 라벨은 **정답** 과 **오답** 이다. 만약 피드백 라벨을 수정하지 않으면 학습자는 다음 예시와 같은 문구를 보게 된다.


.. image:: ../../../shared/images/dropdown_feedback.png
 :alt: Image of multiple choice feedback with the standard label.
 :width: 600

기본 라벨을 바꿀 수 있다. 다음은 사용자 정의 라벨을 사용한 예시다.

.. image:: ../../../shared/images/dropdown_feedback_custom_label.png
 :alt: Image of multiple choice feedback with a custom label.
 :width: 600

.. note::
  기본 라벨 **정답** 과 **오답** 은 학습자의 언어에 따라 다르게 나타난다. 만약 사용자 정의 라벨을 사용한다면 설정한 언어로 나오게 되며 번역되지 않는다.


간편 편집기에서 사용자 정의 피드백 라벨 사용하기
***********************************************

:ref:`Simple Editor` 에서 다음과 같이 사용자 정의 피드백 라벨을 설정할 수 있다.

::

  ( ) Answer {{Label:: Feedback for learners who select this answer.}}

예를 들어 다음 피드백은 사용자 정의 라벨을 사용하고 있다.

::

  ( ) tomato {{Not Quite:: Many people mistakenly think a tomato is a
  vegetable. However, because a tomato is the fertilized ovary of a tomato
  plant and contains seeds, it is a fruit.}}

고급 편집기에서 사용자 정의 피드백 라벨 설정하기
*************************************************

:ref:`Advanced Editor` 에서 다음과 같이 사용자 정의 피드백 라벨을 설정할 수 있다.

.. code-block:: xml

   <option correct="False">
     Answer
     <optionhint label="Custom Label">
       Feedback for learners who select this answer.
     </optionhint>
   </option>

예를 들어 다음 피드백은 사용자 정의 라벨을 사용하고 있다.

.. code-block:: xml

  <option correct="False">
    tomato
    <optionhint label="Not Quite">
      Many people mistakenly think a tomato is a vegetable. However, because a
      tomato is the fertilized ovary of a tomato plant and contains seeds it
      is classified as a fruit.
    </optionhint>
  </option>

.. _Use Hints in a Dropdown Problem:

********************************************
드롭다운 문제에서 힌트 사용하기
********************************************

간편 편집기나 고급 편집기를 통해 드롭다운 문제에서 힌트를 사용할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst


.. _Dropdown Problem XML:

************************
드롭다운 문제 XML
************************

========
템플릿
========

.. code-block:: xml

  <problem>
  <legend>Question text</legend>
  <optionresponse>
    <option correct="False">
      Option Label
      <optionhint>
        Feedback for when learner selects this answer.
      </optionhint>
    </option>
    <option correct="True">
      Option Label
      <optionhint>
        Feedback for when learner selects this answer.
      </optionhint>
    </option>
  </optionresponse>
  <demandhint>
    <hint>Hint 1</hint>
    <hint>Hint 2</hint>
    <hint>Hint 3</hint>
  </demandhint>
  <solution>
    <div class="detailed-solution">
      <p>Explanation or Solution Header</p>
      <p>Explanation or solution text</p>
    </div>
  </solution>
  </problem>

========
태그
========

* ``<optionresponse>`` (필수 사항): 문제가 드롭다운 문제임을 나타낸다.
  problem.

* ``<option>`` (필수 사항): 답안 옵션을 나열한다.

* ``<demandhint>`` (선택 사항): 힌트를 나타낸다.


**Tag:** ``<optionresponse>``

문제가 드롭다운 문제임을 나타낸다.

  속성

  (없음)

  Children

  ``<option>``

**Tag:** ``<option>``

답안 옵션을 나열한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - correct (필수)
       - 정답인지 여부를 나타낸다. 가능한 값은 “true” 및 “false”이다. 단 하나의 올바른 속성을 “true”로 설정할 수 있다.

  Children

  ``<optionhint>``

**Tag:** ``<optionhint>``

답안의 힌트를 나타낸다.

**Tag:** ``<demandhint>``

학습자가 볼 수 있는 힌트를 나타낸다.

  Children

  ``<hint>``

**Tag:** ``<hint>``

학습자가 볼 수 있는 힌트를 나타낸다.

  Children

  (none)
