.. _Text Input:

########################
텍스트 입력 문제
########################

.. note:: K-MOOC은 이 문제 유형에 대해 모두 지원한다.

.. contents::
  :local:
  :depth: 1

**********
개관
**********

텍스트 입력 문제에서는 학습자가 응답 필드에 텍스트를 입력한다. 응답은 숫자, 문자, 그리고 구두점과 같은 특수 문자를 포함할 수 있다. 학습자가 입력한 텍스트는 철자법과 구두점 사용을 포함하여, 교수자가 지정한 답과 반드시 정확히 일치해야 한다. 따라서 학습자가 오타를 낼 가능성을 고려하여 텍스트 입력 문제에 대한 응답 기회를 2회 이상으로 지정할 것을 권고한다.

.. image:: ../../../shared/images/TextInputExample.png
 :alt: An example text input problem.

**************************************************
선다형 문제 수행 분석하기
**************************************************

강좌의 텍스트 입력 문제에 대해 K-MOOC Insights 등을 활용해 학습자 수행 자료 및 답안을 분석할 수 있다. :ref:`insights:Using edX Insights` 를 참고하면 된다.

******************************
Creating a Text Input Problem
******************************

간편 편집기 또는 고급 편집기에서 선다형 문제를 만들 수 있다. 우선 간편 편집기에서 문제를 만든 후 고급 편집기로 넘어가 XML의 다양한 설정을 사용할 수도 있다. 그러나 고급 편집기 사용 후 간편 편집기로 되돌아 올 수는 없다. 따라서 고급 편집기 사용 전에 문제 형식을 완전
하게 만들어 놓는 것이 좋다.

.. _Use the Simple Editor to Create a Text Input Problem:

========================================================================
간편 편집기를 사용해 텍스트 입력 문제 생성하기
========================================================================

:ref:`simple editor<Simple Editor>` 로 텍스트 입력 문제를 만들기 위해.

#. **신규 구성요소 추가** 에서 문제 를 클릭한다.
#. 두 가지 텍스트 입력 문제 템플릿(텍스트 입력/힌트가 있는 텍스트 입력) 중 하나를 선택한다.

  * **공통 문제 유형** 탭의 텍스트 입력을 클릭한다.

  * 힌트와 피드백을 포함한 공통 문제 유형 탭에서 힌트와 피드백을 포함한 텍스트 입력을 클릭한다. 자세한 사항은  `Use Feedback in a Text Input Problem`_ 를 참고한다.

    Studio는 학습활동에 문제를 추가한다.

#. 편집을 선택하면 간편 편집기가 열린다.
#. 기존 텍스트를 수정하여 실제 학습자에게 제공하는 문제로 바꾼다.
#. 웹 접근성 지원을 위해 사용할 문제의 지문을 결정한다. 이어, 해당 텍스트를 두 쌍의 꺾쇠괄호 (``>>question<<``) 로 묶는다. 이 텍스트는 화면 판독기, 보고 및 Insights에 사용된다.
#. 정답 텍스트를 선택한 후 텍스트 입력 단추를 클릭한다. 이 단계까지 진행하면 답 옆에 = 기호가 표시된다.

   하나 이상의 정답을 설정할 수 있다. 자세한 사항은  :ref:`Multiple Responses in Text Input Problems` 를 참고하면 된다.

#. **설명** 을 추가하기 위해 설명 텍스트를 선택하고 도구 모음에서 설명을 클릭한다. 설명 텍스트 전후에 ``[explanation]`` 가 나타난다.
#. **설정** 을 선택하고 문제 표시명을 입력한다.
#. **문제 추가** 설정을 완료한다. 자세한 사항은 :ref:`Problem Settings` 을 참고하면 된다.
#. **저장** 을 선택한다.

상기 예의 경우 문제 구성요소 내부의 텍스트는 다음과 같다.

::

    >>What was the first post-secondary school in China to allow both male and
    female students?<<

    = Nanjing Higher Normal Institute
    or= National Central University
    or= Nanjing University

    [explanation]
    Nanjing Higher Normal Institute first admitted female students in 1920.
    [explanation]

========================================================================
고급 편집기로 텍스트 입력 문제 편집하기
========================================================================

고급 편집기로 텍스트 입력 문제를 편집하기 위해.

#. :ref:`simple editor<Use the Simple Editor to Create a Text Input Problem>` 에서 문제를 만든다.
#. **고급 편집기** 를 선택하고 XML을 편집해 필요한 태그와 속성을 다음 예와 같이 추가한다.

**문제코드**:

.. code-block:: xml

  <problem>
    <p>What was the first post-secondary school in China to allow both male and female students?</p>

    <stringresponse answer="Nanjing Higher Normal Institute" type="ci" >
      <additional_answer>National Central University</additional_answer>
      <additional_answer>Nanjing University</additional_answer>
      <textline label="What was the first post-secondary school in China to
        allow both male and female students?" size="20"/>
    </stringresponse>
    <solution>
      <div class="detailed-solution">
        <p>Explanation</p>
        <p>Nanjing Higher Normal Institute first admitted female students in
        1920.</p>
      </div>
    </solution>
  </problem>

.. _Use Feedback in a Text Input Problem:

********************************************
텍스트 입력 문제에서 피드백 사용하기
********************************************

간편 편집기나 고급 편집기를 사용해 텍스트 입력 문제에 피드백을 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

텍스트 입력 문제에서 학습자가 선택할 수 있는 각 보기에 대해 피드백을 추가할 수 있다.

정답을 선택했을 때 정답인 이유를 설명하는 피드백을 추가한다.

오답을 선택했을 때 흔히 있을 수 있는 오류에 대한 피드백을 추가한다. 텍스트 입력 문제 피드백은 학습자가 정답을 유추할 수 있도록 작성되어야 한다.

=======================================
간편 편집기에서 피드백 설정하기
=======================================

:ref:`simple editor<Simple Editor>`  에서 다음과 같이 피드백을 설정할 수 있다. 새 텍스트 입력 문제를 생성할 때 힌트와 피드백을 포함한 텍스트 입력 템플릿인 힌트가 있는 텍스트 입력 을 선택한다. 이 템플릿의 예제 피드백을 지우고 새 값을 입력하면 된다.

::

  = Correct Answer {{Feedback for learners who select this answer.}}
  not= Incorrect Answer {{Feedback for learners who select this answer.}}

예를 들어 다음 문제는 정답에 대한 피드백과 두 오답에 대한 피드백을 포함하고 있다.

::

  >>What is the largest state in the U.S. in terms of land area?<<

  =Alaska {{Alaska is the largest state in the U.S. in terms of not only land
  area, but also total area and water area. Alaska is 576,400 square miles,
  more than double the land area of the second largest state, Texas.}}

  not=Texas {{While many people think Texas is the largest state in terms of
  land area, it is actually the second largest and contains 261,797 square
  miles.}}

  not=California {{California is the third largest state and contains 155,959
  square miles.}}


=========================================
고급 편집기에서 피드백 설정하기
=========================================

:ref:`advanced editor<Advanced Editor>` 에서 다음과 같이 피드백을 설정할 수 있다.

.. code-block:: xml

    <stringresponse answer="Correct Answer" type="ci" >
      <correcthint>Hint for correct answer.</correcthint>
      <stringequalhint answer="Incorrect Anser">
        Hint for incorrect answer.
      </stringequalhint>
    </stringresponse>

예를 들어 다음 문제는 정답에 대한 피드백과 두 오답에 대한 피드백을 포함하고 있다.

.. code-block:: xml

  <problem>

    <p>What was the first post-secondary school in China to allow both male and female students?</p>
    <stringresponse answer="Alaska" type="ci" >
      <correcthint>
        Alaska is the largest state in the U.S. in terms of not only land
        area, but also total area and water area. Alaska is 576,400 square
        miles, more than double the land area of the second largest state,
        Texas.
      </correcthint>
      <stringequalhint answer="Texas">
        While many people think Texas is the largest state in terms of land
        area, it is actually the second largest of the 50 U.S. states
        containing 261,797 square miles.
      </stringequalhint>
      <stringequalhint answer="California">
        California is the third largest state in the U.S. in terms of land
        area containing 155,959 square miles.</stringequalhint>
      <textline label="What is the largest state in the U.S. in terms of land
        area?" size="20"/>
    </stringresponse>
  </problem>

=========================
사용자 지정 피드백 라벨 설정하기
=========================

학습자는 기본적으로 정답과 오답 피드백 라벨을 보게 된다. 만약 피드백 라벨 설정을 안하면 다음 예제와 같은 화면을 보게 된다.

.. image:: ../../../shared/images/text_input_feedback.png
 :alt: Image of text input feedback with the standard label.
 :width: 600

이런 기본 피드백 라벨을 수정할 수 있다. 예를 들어 특정 오답에 대해 다음과 같이 사용자 지정 피드백 라벨을 사용할 수 있다.

.. image:: ../../../shared/images/text_input_feedback_custom_label.png
 :alt: Image of text input feedback with a custom label.
 :width: 600

.. note::
  정답과 오답 기본 라벨은 학습자의 언어로 보이게 된다. 그러나 사용자 지정 라벨을 사용하면 모두 설정된 언어로 보이게 되며 번역되지 않는다.

간편 편집기에서 사용자 지정 피드백 라벨 설정하기
***********************************************

:ref:`simple editor<Simple Editor>` 에서 다음과 같이 사용자 지정 피드백 라벨을 설정한다.

::

  not=Answer {{Label:: Feedback}}

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

::

  not=Texas {{Close but wrong:: While many people think Texas is the largest
  state in terms of land area, it is actually the second largest of the 50 U.S.
  states, containing 261,797 square miles.}}

고급 편집기에서 사용자 지정 피드백 라벨 사용하기
*************************************************

:ref:`advanced editor<Advanced Editor>` 에서 다음과 같이 사용자 지정 피드백 라벨을 설정한다.

.. code-block:: xml

    <stringequalhint answer="Incorrect Anser" label="Custom Label">
      Feedback
    </stringequalhint>

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

.. code-block:: xml

    <stringequalhint answer="Texas" label="Close but wrong">
      While many people think Texas is the largest state in terms of land
      area, it is actually the second largest of the 50 U.S. states containing
      261,797 square miles.
    </stringequalhint>

.. _Use Hints in a Text Input Problem:

********************************************
텍스트 입력 문제에서 힌트 사용하기
********************************************

간편 편집기와 고급 편집기를 사용해 선다형 문제에 힌트를 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst

.. _Multiple Responses in Text Input Problems:

******************************************
텍스트 입력 문제에서 복수정답 설정하기
******************************************

텍스트 입력 문제에서 1개 이상의 정답을 지정할 수 있다. 이를테면 “Dr. Martin Luther King, Junior”을 정확히 입력하는 대신 “Martin Luther King”이나 “Doctor Martin Luther King” 등의 기타 변형도 수용하는 것이다. 이 역시 기본 편집기나 고급 편집기로 생성할 수 있다.

==============
간편 편집기
==============

기본 편집기로 추가 정답을 지정할 경우 각 추가 정답 앞에 “or=” 를 삽입한다. (큰따옴표는 입력하지 않다.)

::

    >>What African-American led the United States civil rights movement during
    the 1960s?<<
    = Dr. Martin Luther King, Jr.
    or= Dr. Martin Luther King, Junior
    or= Martin Luther King, Jr.
    or= Martin Luther King

=====================
고급 편집기
=====================

고급 편집기로 추가 정답을 지정할 경우 ``<additional_answer>`` 의 여는 태그와 닫는 태그 안쪽에서 각 추가 정답에  ``<stringresponse>`` .

.. code-block:: xml

  <problem>

  <p>What African-American led the United States civil rights movement during the 1960s?</p>

  <stringresponse answer="Dr. Martin Luther King, Jr." type="ci" >
    <additional_answer>Dr. Martin Luther King, Junior</additional_answer>
    <additional_answer>Martin Luther King, Jr.</additional_answer>
    <additional_answer>Martin Luther King</additional_answer>
    <textline label="What African-American led the United States civil rights
      movement during the 1960s?" size="20"/>
  </stringresponse>
  </problem>

******************************************
텍스트 입력 필드 뒤에 텍스트 추가하기
******************************************

텍스트 입력 문제에서 응답 필드 뒤에 단어, 구문이나 문장을 추가해 학습자가 문제를 잘 이해할 수 있도록 도울 수 있다.

.. image:: ../../../shared/images/MC_trailing_text.png
 :width: 500
 :alt: Multiple choice problem with the word "Institute" after the answer
  field.

반드시 :ref:`advanced editor<Advanced Editor>` 를 사용해야 한다.

문제에서  ``textline`` 요소를 찾는다. 이 요소가 문제 응답 필드를 생성하며  ``stringresponse`` 의 하위구성요소이다. 예를 들어.

::

  <stringresponse answer="Ashmun" type="ci" >
    <textline label="What Pennsylvania school was founded in 1854 to provide
     educational opportunities for African-Americans?" size="20" />
  </stringresponse>

정답 필드 옆에 텍스트를 추가하기 위해  ``trailing_text`` 속성을  ``textline`` 요소 안에 사용할 텍스트와 함께 추가한다

::

  <stringresponse answer="Ashmun" type="ci" >
    <textline label="What Pennsylvania school was founded in 1854 to provide educational
     opportunities for African-Americans?" size="20" trailing_text="Institute" />
  </stringresponse>


******************************************
텍스트 입력 문제의 대소문자 구분
******************************************

텍스트 입력 문제는 응답에서 대소문자를 구분하지 않는 것이 초기 설정이다. 이를 변경하여 대소문자 구분을 필수로 하는 정답을 요구할 수 있다.

텍스트 입력 응답에서 대소문자를 구분하려면 반드시 :ref:`Advanced Editor` 를 사용해야 한다 .

고급 편집기에서 대소문자를 구분하지 않는 경우 ``stringresponse`` 요소의 type 속성을 ci 로 한다. 이를테면 다음과 같다.

::

    <stringresponse answer="Michigan" type="ci">
      <textline size="20"/>
    </stringresponse>

대소문자를 구분하려면  ``type`` 속성을 ``cs`` 로 변경한다.

::

    <stringresponse answer="Michigan" type="cs">
      <textline size="20"/>
    </stringresponse>

*************************************************
텍스트 입력 문제의 응답 필드 길이
*************************************************

텍스트 입력 문제의 응답 필드 길이 초기 설정값은 20글자이다.

학습 활동을 미리보기하여 해당 응답 입력 필드 길이가 정답을 기입하기에 충분한지 확인하고 기입 가능성이 있는 오답을 고려하여 여분의 길이를 더 주는 것이 좋다.

응답 필드 길이 초기값이 충분하지 않은 경우  :ref:`advanced editor<Advanced Editor>` 로 이를 변경할 수 있다.

고급 편집기의 경우, 정답에 대한 XML 블록에서 ``textline`` 요소의 ``size`` 속성값은 ``20`` 이다.

::

    <stringresponse answer="Democratic Republic of the Congo" type="ci">
      <textline size="20"/>
    </stringresponse>

응답 필드의 길이를 수정하기 위해, ``size`` 속성값을 수정한다

::

    <stringresponse answer="Democratic Republic of the Congo" type="ci">
      <textline size="40"/>
    </stringresponse>

********************************************************
텍스트 입력 문제의 정규표현식
********************************************************

텍스트 입력 문제에서 학습자가 응답한 특정 정규 표현식을 답으로 인정하게 할 수도 있다. 이를 위해 고급 편집기에서 해당 문제의 XML을 변경해야만 한다.

학습자가 입력한 정규 표현식은 교수자가 지정한 정답의 일부를 반드시 포함해야 한다. 가령 교수자가 
 ``<answer="example answer" type="regexp">`` 을 지정한 경우  ``example answered``, ``two example answers``, ``==exampleanswer==`` 등은 정답이지만  ``examples`` 나  ``example anser`` 은 정답이 아니다.

``regexp`` 을  ``type`` 속성값에 추가할 수 있다. 이를테면 ``type="ci regexp"`` , ``type="regexp"`` , ``type="regexp cs"`` 등이 가능하다. 이 경우 어떤 답 혹은 힌트라도 정규 표현식으로 간주한다.

.. _Text Input Problem XML:

***********************
텍스트 입력 문제 XML
***********************

==============
템플릿
==============

.. code-block:: xml

  <problem>
      <p>Problem text</p>
      <stringresponse answer="Correct answer 1" type="ci regexp">
          <additional_answer>Correct answer 2</additional_answer>
          <additional_answer>Correct answer 3</additional_answer>
          <textline size="20" label="label text"/>
          <correcthint>Provides feedback when learners submit the correct response.</correcthint>
          <stringequalhint answer="Incorrect answer 1">Provides feedback when learners submit the specified incorrect response.</stringequalhint>
          <stringequalhint answer="Incorrect answer 2">Provides feedback when learners submit the specified incorrect response.</stringequalhint>
          <textline label="Which U.S. state has the largest land area?" size="20"/>
      </stringresponse>

      <demandhint>
        <hint>The first text string to display when learners request a hint.</hint>
        <hint>The second text string to display when learners request a hint.</hint>
      </demandhint>
  </problem>

=======
Tags
=======

* ``<stringresponse>``: 텍스트 입력 문제임을 나타낸다. 이는 다음과 같은 하위 태그를 갖는다.

  - ``<textline>``: 학습자가 응답을 입력하는 LMS에 응답 필드를 생성한다.

  - ``<additional_answer>`` (선택): 문제에 대한 추가 정답을 지정한다. 하나의 문제가 가질 수 있는 추가 정답의 수는 제한이 없다.

  - ``<correcthint>`` (선택): 정답에 대한 피드백을 나타낸다.

  - ``<stringequalhint>`` (선택): 피드백을 제공할 오답의 텍스트를 지정한다.

* ``<demandhint>`` (선택): 학습자가 정답에 도달하기 위해 요청할 수 있는 하나 이상의 힌트를 나타낸다. ``<demandhint>`` 태그는  ``<hint>`` 를 차일드 태그로 갖는다.


**Tag:** ``<stringresponse>``

텍스트 입력 문제임을 나타낸다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - answer (필수)
       - 정답을 지정한다. 답을 정규 표현식으로 지정하기 위해 type 속성에 “regexp” 를 추가한다. type 속성에 “regexp” 를 추가하지 않을 경우 학습자의 응답은 이 속성값과 반드시 정확히 일치해야 한다.
     * - type (선택)
       - 문제가 대소문자를 구분하는지, 그리고 정규 표현식을 허하는지 허용 여부를 지정할 수 있다.

         * <stringresponse> 태그가 type="ci" 를 포함하는 경우 해당 문제는 대소문자를 구분하지 않다.
         * <stringresponse> 태그가 type="cs" 를 포함하는 경우 해당 문제는 대소문자를 구분한다
         * <stringresponse> 태그가 type="regexp" 를 포함하는 경우 해당 문제는 정규 표현식을 설정한다.

         <stringresponse> 태그의 type 속성은 이들 값을 조합할 수도 있다. 가령, <stringresponse type="regexp cs"> 는 해당 문제가 정규 표현식을 허용하며 동시에 대소문자를 구분하는 것으로 규정한다.


  Children

  * ``<textline />`` (필수사항)
  * ``<additional_answer>`` (선택사항)
  * ``<correcthint>`` (선택사항)
  * ``<stringequalhint>`` (선택사항)

**Tag:** ``<textline />``

학습자가 응답을 입력하는 LMS에 응답 필드를 생성한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - label (필수)
       - 문제의 텍스트를 포함한다.
     * - size (선택)
       - LMS의 응답란에 size 를 입력한다.
     * - hidden (선택)
       - true 로 설정된 경우 학습자는 응답 필드를 볼 수 없다.
     * - correct_answer (선택)
       - 문제의 정답 목록이다.
     * - trailing_text
       - 응답 필드 옆에 추가할 텍스트를 추가한다.

  Children

  (none)

**Tag:** ``<additional_answer>``

문제에 대한 추가 정답을 지정한다. 하나의 문제가 가질 수 있는 추가 정답의 수는 제한이 없다.

  Attributes

  (none)

  Children

  (none)

**Tag:** ``<correcthint>``

교수자가 흔히 발생하는 어떤 오답에 힌트를 제공했음을 나타낸다.

  Attributes

  (none)

  Children

  (none)

**Tag:** ``<stringequalhint>``

오답에 대한 피드백을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - answer (필수)
       - 오답의 텍스트이다.

  Children

  (none)

**Tag:** ``<demandhint>``

학습자가 정답에 도달하기 위해 요청할 수 있는 하나 이상의 힌트를 나타낸다.

  Attributes

  (none)

  Children

**Tag:** ``<hint>``

힌트의 텍스트를 포함한다. 학습 관리 시스템은 각 힌트를 ``<demandhint>`` 태그 내에 ``<hint>`` 태그가 추가된 순서로 학습자에게 보여준다.

**************************
기존 힌트 방식

**************************

다음 예제는 텍스트 입력 문제 힌트를 설정할 때 기존에 사용하던  ``<hintgroup>`` 요소 내의 XML 형식을 보여준다. 이 XML 형식을 사용하는 문제는 K-MOOC 플랫폼에서 계속 사용할 수 있다. 그러나 K-MOOC은 위에 기술된 새로운 힌트 설정 방식을 사용하기를 권장한다.

.. code-block:: xml

  <problem>
      <p>Problem text</p>
      <stringresponse answer="Correct answer 1" type="ci regexp">
          <additional_answer>Correct answer 2</additional_answer>
          <additional_answer>Correct answer 3</additional_answer>
          <textline size="20" label="label text"/>
          <hintgroup>
              <stringhint answer="Incorrect answer A" type="ci" name="hintA" />
                <hintpart on="hintA">
                    <startouttext />Text of hint for incorrect answer A<endouttext />
                </hintpart >
              <stringhint answer="Incorrect answer B" type="ci" name="hintB" />
                <hintpart on="hintB">
                    <startouttext />Text of hint for incorrect answer B<endouttext />
                </hintpart >
              <stringhint answer="Incorrect answer C" type="ci" name="hintC" />
                <hintpart on="hintC">
                    <startouttext />Text of hint for incorrect answer C<endouttext />
                </hintpart >
          </hintgroup>
      </stringresponse>
      <solution>
      <div class="detailed-solution">
      <p>Explanation or Solution Header</p>
      <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

