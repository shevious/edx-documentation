.. _Numerical Input:

########################
수치 입력 문제
########################

.. note:: K-MOOC은 이 문제 유형에 대해 전체 지원을 제공한다.

.. contents::
  :local:
  :depth: 1

**********
개관
**********

이 유형의 문제에서는 학습자가 질문에 대한 답변으로 숫자 또는 비교적 단순한 특정 수식을 입력한다. 학습자가 입력한 문자열은 기호식으로 변환되어 답변 필드 아래에 표시된다.

.. image:: ../../../shared/images/NumericalInputExample.png
 :alt: A problem with two questions, one answered correctly and one
     incorrectly.

수식 입력 문제에 대한 답변은 정수, 분수, 그리고 원주율(pi)이나 중력 가속도(g) 등의 상수를 포함할 수 있다. 제곱근(sqrt)이나 10을 밑으로 하는 로그 등의 간단한 함수, 그리고 사인(sin), 아크사인(arcsin)과 같은 삼각함수 및 역삼각함수를 나타내는 문자열도 가능하다. 학습자가 이들 함수를 나타내는 문자열을 입력하면 해당 문자열이 수학 기호로 변환된다. 수식 입력 문제에서 학습자의 문자열을 수식으로 변환하는 장면을 아래의 예에 제시한다.

.. image:: ../../../shared/images/Math5.png
 :alt: A learner typed n*x^(n-1) to enter the symbolic expression n times x to
     the n minus 1 power.

학습자가 입력할 수 있는 문자에 관한 보다 구체적인 정보를 :ref:`openlearners:Math Formatting` 에서 확인할 수 있다.

학습자가 작성한 정답이 정확할 필요 없게 오차범위를 설정할 수도 있다. Python 스크립트를 사용하거나 정확한 정답을 설정할 수 있다.

.. note::
  모든 학습활동 페이지에서 계산기를 활용할 수 있다. 자세한 사항은  :ref:`Calculator` 를 참고하면 된다.

**************************************************
수치 입력 문제 성과 분석하기
**************************************************

강좌의 수식 입력 문제에 Insights를 사용해 학습자 성과 데이터 및 답안을 분석할 수 있다. 자세한 사항은  :ref:`insights:Using edX Insights`  를 참고하면 된다.

***********************************
수치 입력 문제 생성하기
***********************************

간편 편집기나 고급 편집기로 수식 입력 문제를 생성할 수 있다.

* 지문에 이탤릭체, 볼드체, 특수 문자가 없는 경우라면 간편 편집기로 생성 가능하다.
* 문제 지문에 특수 포맷이나 특수 문자, 또는 Python 스크립트가 포함되는 경우 고급 편집기를 사용한다.

이를 테면, 아래의 예제를 생성하려면 고급 편집기를 사용해야 한다.

.. image:: ../../../shared/images/NumericalInput_Complex.png
 :alt: A problem that requires a square root as the answer.

이 예제에서 문제는 Python 스크립트를 사용하였다.

문제 지문에 Python 스크립트를 입력하는 방법에 대한 보다 구체적인 정보는 :ref:`Write Your Own Grader` 을 참조한다.

.. _Use the Simple Editor to Create a Numerical Input Problem:

========================================================================
간편 편집기를 이용해 수식 입력 문제 생성하기
========================================================================

:ref:`simple editor<Simple Editor>`  로 수식 입력 문제를 생성하기 위해.

#. **신규 구성요소 추가** 에서 **문제** 를 클릭한다.
#. 두가지 문제 템플릿 중 하나를 선택한다.

   * **일반문제유형** 탭의 **수치 입력** 을 클릭한다.

   * 일반문제유형탭에서 힌트가 있는 수치 입력을 클릭한다. 자세한 사항은  `Use Feedback in a Numerical Input Problems`_  를 참고하면 된다.

     Studio는 학습활동에 문제를 추가한다.

#. **편집** 을 선택하면 간편 편집기가 열린다.
#. 구성요소 편집기의 예제 문자열을 원하는 문자열로 바꾼다.
#. 질문으로 사용할 문제 텍스트를 결정한 후 해당 텍스트를 두 쌍의 (``>>question<<``) 로 묶는다. 이 텍스트가 화면 판독기, 보고, Insights에서 질문을 나타낸다 .
#. 정답 텍스트를 선택한 후 수식 입력 단추를 클릭하면 = 표시가 답 옆에 나타난다.
#. (선택 사항) 오차 범위 또는 허용 한계를 지정한다. 백분율, 숫자 또는 범위를 지정할 수 있다.

   * 정답 양측(±)으로 허용 한계를 지정하려면 해당 정답 뒤에 +-숫자%를 입력한다. 가령 2%의 허용 오차를 두고자 하는 경우 +-2%를 입력한다.

   * 정답 양측(±)으로 숫자를 지정하려면 해당 정답 뒤에 +-숫자를 입력한다. 가령 허용 한계 5를 두고자 하는 경우 +-5를 입력한다.

   * 범위를 지정하려면 시작 값과 끝 값은 ,로 나뉘며 대괄호([]) 또는 괄호(())를 이용한다. 대괄호는 해당 대괄호에 인접한 숫자를 포함한다는 의미이며 괄호는 해당 괄호에 인접한 숫자를 포함하지 않는다는 뜻이다. 이를테면, 범위를 [5, 8)로 지정할 경우 5, 6, 7은 정답이나 8은 정답이 아니다. 범위를 (5, 8]로 지정할 경우 6, 7, 8은 정답이나 5는 정답이 아니다.

#. 구성요소 편집기에서 설명용 텍스트를 선택한 후 설명 단추를 눌러 해당 텍스트에 설명 태그를 추가한다. ``[explanation]`` 가 설명용 텍스트 전후에 나타난다.
#. **설정** 을 선택하고 **표시 이름** 을 정한다.
#. 기타 설정을 지정한다. 자세한 사항은  :ref:`Problem Settings` 을 참고하면 된다.
#. **저장** 을 클릭한다.

상기 첫 번째 예제 가운데 문제 구성요소의 텍스트는 다음과 같다.

::

   >>What base is the decimal numeral system in?<<

   = 10

   [explanation]
   The decimal numeral system is base ten.
   [explanation]

.. _Use the Advanced Editor to Create a Numerical Input Problem:

========================================================================
Use the Advanced Editor to Create a Numerical Input Problem
========================================================================

고급 편집기로 수식 입력 문제를 만들기 위해.

#. :ref:`simple editor<Use the Simple Editor to Create a Numerical Input Problem>` 에서 문제를 만들었던 절차들을 따른다.
#. **고급 편집기** 를 선택하고, 입력되지 않은 고급 문제를 선택하여 XML을 수정해 다음 예제와 같이 태그와 속성을 추가한다.

**문제 코드**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>

  <legend>What base is the decimal numeral system in?</legend>
      <numericalresponse answer="10">
          <formulaequationinput label="What base is the decimal numeral system in?"/>
      </numericalresponse>

    <legend>What is the value of the standard gravity constant <i>g</i>, measured in m/s<sup>2</sup>? Give your answer to at least two decimal places.</legend>
    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput label="Give your answer to at least two decimal places"/>
    </numericalresponse>

  <!-- The following lines use Python script spacing. Make sure it is not indented when you add it to the problem component. -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

  <legend>What is the distance in the plane between the points (pi, 0) and (0, e)? You can type math.</legend>
      <numericalresponse answer="$computed_response">
          <responseparam type="tolerance" default="0.0001" />
          <formulaequationinput label="What is the distance in the plane between the points (pi, 0) and (0, e)?"/>
      </numericalresponse>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>The decimal numerical system is base ten.</p>
      <p>The standard gravity constant is defined to be precisely 9.80665 m/s<sup>2</sup>.
      This is 9.80 to two decimal places. Entering 9.8 also works.</p>
      <p>By the distance formula, the distance between two points in the plane is
         the square root of the sum of the squares of the differences of each coordinate.
        Even though an exact numerical value is checked in this case, the
        easiest way to enter this answer is to type
        <code>sqrt(pi^2+e^2)</code> into the editor.
        Other answers like <code>sqrt((pi-0)^2+(0-e)^2)</code> also work.
      </p>
    </div>
  </solution>
  </problem>

.. _Use Feedback in a Numerical Input Problems:

********************************************
Using Feedback in a Numerical Input Problems
********************************************

You can add feedback in a numerical input problem using the simple editor
or the advanced editor. For an overview of feedback in problems, see
:ref:`Adding Feedback and Hints to a Problem`.

In numerical input problems, you can provide feedback for correct answers.

.. note::
  You cannot provide feedback for incorrect answers in numerical input
  problems.

Use feedback for the correct answer to reinforce the process for arriving at
the numerical value.

=======================================
Configure Feedback in the Simple Editor
=======================================

In the :ref:`simple editor<Simple Editor>`, you configure answer feedback with
the following syntax. When you create a new numerical input problem, select the
template  **Numerical Input with Hints and Feedback**. This template has
example feedback syntax that you can replace.

::

  = Numerical Answer {{Feedback for the correct answer.}}

For example, the following problem has feedback for each possible answer.

::

  >>What is the arithmetic mean for the following set of numbers?
    (1, 5, 6, 3, 5)<<

  = 4 {{The mean for this set of numbers is 20 / 5 which equals 4.}}

=========================================
Configure Feedback in the Advanced Editor
=========================================

In the :ref:`advanced editor<Advanced Editor>`, you configure answer feedback
with the following syntax.

.. code-block:: xml

    <numericalresponse answer="Correct Answer">
      <formulaequationinput label="Question" />
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>

For example, the following problem has feedback for the correct answer.

.. code-block:: xml

  <numericalresponse answer="4">
    <formulaequationinput label="What is the arithmetic mean for the following
      set of numbers? (1, 5, 6, 3, 5)" />
    <correcthint>
      The mean for this set of numbers is 20 / 5 which equals 4.
    </correcthint>
  </numericalresponse>

=========================
Customize Feedback Labels
=========================

By default, the feedback label for correct answers is **Correct** . If you do
not define a feedback label, learners see this term when they submit a correct
answer, as in the following example.

.. image:: ../../../shared/images/numerical_input_feedback.png
 :alt: Numerical input feedback with the standard label.
 :width: 600

You can configure the problem to override the default labels. For example, you
can configure a custom label for the answer.

.. image:: ../../../shared/images/numerical_input_feedback_custom_label.png
 :alt: Numerical input feedback with a custom label.
 :width: 600

.. note::
  The default label **Correct** is displayed in the learner's requested
  language. If you provide a custom label, it is displayed to all users as you
  configure it and is not translated into different languages.

Customize Feedback Labels in the Simple Editor
***********************************************

In the :ref:`simple editor<Simple Editor>`, you configure a custom feedback
label with the following syntax.

::

  = 4 {{Label::Feedback}}

For example, the following feedback is configured to use a custom label.

::

  = 4 {{Good Job::The mean for this set of numbers is 20 / 5 which equals 4.}}

Customize Feedback Labels in the Advanced Editor
*************************************************

In the :ref:`advanced editor<Advanced Editor>`, you configure custom feedback
labels with the following syntax.

.. code-block:: xml

    <correcthint label="Custom Label">
      Feedback
    </correcthint>

For example, the following feedback is configured to use a custom label.

.. code-block:: xml

  <correcthint label="Good Job">
    The mean for this set of numbers is 20 / 5 which equals 4.
  </correcthint>

.. _Use Hints in a Numerical Input Problem:

********************************************
Using Hints in a Numerical Input Problem
********************************************

You can use hints in a numerical input problem, using the simple editor
or the advanced editor. For an overview of hints in problems, see
:ref:`Adding Feedback and Hints to a Problem`.

.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst

.. _Awarding Partial Credit in a Numerical Input Problem:

*****************************************************
Awarding Partial Credit in a Numerical Input Problem
*****************************************************

You can configure a numerical input problem to award partial credit to learners
who submit an answer that is close or related to the correct answer. You must
use the :ref:`advanced editor<Use the Advanced Editor to Create a Numerical
Input Problem>` to configure partial credit.

.. only:: Partners

 .. note::
    Support for partial credit problems in courses on edx.org and edX
    Edge is provisional. Ensure that you test such problems thoroughly before
    releasing them to learners. For more information, contact your edX partner
    manager.

In the following example, the learner entered an answer that was close to the
correct answer and received partial credit.

.. image:: ../../../shared/images/partial_credit_numerical_input.png
 :alt: A numerical input problem with partial credit for a close answer.
 :width: 600

For an overview of partial credit in problems, see
:ref:`Awarding Partial Credit for a Problem`.

There are two ways to award partial credit in a numerical input problem.

.. contents::
  :local:
  :depth: 1

.. Note:: You can use these ways of awarding partial credit in combination.

==========================
Identifying Close Answers
==========================

You can configure a numerical input problem so that answers that are close to
the correct answer receive partial credit.

You configure the tolerance for incorrect answers. Learners receive partial
credit for close answers based on the tolerance. By default, the tolerance is
multiplied by 2 and the following rules are applied.

* An answer within the tolerance receives 100% of the points for the problem.

* An answer within or equal to 2x of the tolerance receives 50%.

* An answer more than 2x the outside of the tolerance receives 0%.

You can optionally specify a different multiplier for the tolerance. For
example, you could set the multiplier to 3. In this case, the following rules
apply.

* An answer within the tolerance receives 100% of the points for the problem.

* An answer within or equal to 3x of the tolerance receives 50%.

* An answer more than 3x outside of the tolerance receives 0%.

Configure Close Answers for a Numerical Input Problem
******************************************************

To configure a numerical input problem to award partial credit for close
answers, you add the following attributes to the problem XML.

* Add the ``"partial_credit="close"`` attribute to the ``<numericalresponse>``
  element. If you are using close answers in combination with a list, set the
  attribute to ``partial_credit="close,list"``.

* Optionally, add the ``partial_range`` attribute to the ``<responseparam>``
  element and set its value to the tolerance multiplier. If you do not set the
  ``partial_range`` attribute, 2 is used as the tolerance multiplier.

For example, the following XML shows the numerical problem template
updated to provide partial credit for close answers.

.. code-block:: xml

  <numericalresponse answer="9.3*10^7" partial_credit="close">
    <formulaequationinput label="How many miles away from Earth is the sun?
      Use scientific notation to answer." />
    <responseparam type="tolerance" default="1%" partial_range="3"/>
  </numericalresponse>

=============================================
Awarding Partial Credit for Answers in a List
=============================================

For some numerical input problems, mistakes do not help a learner arrive at
the correct answer. For example, a small mistake can lead to negative instead of
positive results, or to an answer that is off by a square root or numerical
factor.

For these types of problems, you can configure a list of wrong answers that
receive partial credit. Learners who submit answers that are on the list
receive 50% of the problem's points.


Configure a List for a Numerical Input Problem
************************************************

To configure a numerical input problem to award partial credit for answers in a
list, you add the following attributes to the problem XML.

* Add the ``partial_credit="list"`` attribute to the ``<numericalresponse>``
  element. If you are a list in combination with close answers, set the
  attribute to ``partial_credit="close,list"``.

* Add the ``partial_answers`` attribute to the ``<responseparam>`` element. Set
  its value to one or more answers that should earn 50% of the problem's
  points. Separate multiple values by a comma (,).

For example, the following XML shows the numerical problem template
updated to provide partial credit for a different answer.

.. code-block:: xml

  <numericalresponse answer="93*10^7" partial_credit="list">
    <formulaequationinput label="How many miles away from Earth is the sun?
      Use scientific notation to answer." />
    <responseparam partial_answers="150*10^6"/>
  </numericalresponse>

******************************************
Add Text after the Numeric Response Field
******************************************

You might want to include a word, phrase, or sentence after the answer field
in a numerical input problem to help guide your students or resolve ambiguity.

.. image:: ../../../shared/images/NI_trailing_text.png
 :width: 500
 :alt: Three numerical input problems with text after the response field:
     "km", a percent sign, and a symbol for meters per second squared.

To do this, you must use the :ref:`advanced editor<Advanced Editor>`.

After you open the problem in the advanced editor, locate the
``formulaequationinput`` element. This element creates the response field for
the problem. The ``formulaequationinput`` element is a child of the
``numericalresponse`` element.

To add text after the answer field, add the ``trailing_text`` attribute
together with the text that you want to use inside the
``formulaequationinput`` element. Several examples follow.

.. note:: You can use MathJax inside the ``trailing_text`` attribute, as the
 third example shows. You cannot use HTML inside this attribute.

::

  <numericalresponse answer="12.87">
    <formulaequationinput label="How far is 8 miles in kilometers?"
    trailing_text="km" />
  </numericalresponse>

  <numericalresponse answer="91">
    <formulaequationinput label="According to the Pew Research Center's Internet
    and American Life Project, what percentage of the world's population has a
    cellular phone as of May 2013?" trailing_text="%" />
  </numericalresponse>

  <numericalresponse answer="9.81">
    <formulaequationinput label="What is the strength of Earth's gravity, to
    two decimal places?" trailing_text="\(m/s^{2}\)" />
  </numericalresponse>

.. _Numerical Input Problem XML:

****************************
Numerical Input Problem XML
****************************

=========
Templates
=========

The following templates represent problems with and without a decimal or
percentage tolerance.

Problem with No Tolerance
***************************

.. code-block:: xml

  <problem>

    <legend>TEXT OF PROBLEM</legend>
    <numericalresponse answer="ANSWER (NUMBER)">
      <formulaequationinput label="TEXT OF PROBLEM"/>
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>
    <solution>
      <div class="detailed-solution">
        <p>TEXT OF SOLUTION</p>
      </div>
    </solution>
  </problem>

Problem with a Decimal Tolerance
************************************

.. code-block:: xml

  <problem>

    <legend>TEXT OF PROBLEM</legend>
    <numericalresponse answer="ANSWER (NUMBER)">
      <responseparam type="tolerance" default="NUMBER (DECIMAL, e.g., .02)" />
      <formulaequationinput label="TEXT OF PROBLEM"/>
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>

    <solution>
      <div class="detailed-solution">
        <p>TEXT OF SOLUTION</p>
      </div>
    </solution>
  </problem>

Problem with a Percentage Tolerance
************************************

.. code-block:: xml

  <problem>

    <legend>TEXT OF PROBLEM</legend>
    <numericalresponse answer="ANSWER (NUMBER)">
      <responseparam type="tolerance" default="NUMBER (PERCENTAGE, e.g., 3%)" />
      <formulaequationinput label="TEXT OF PROBLEM"/>
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>

    <solution>
      <div class="detailed-solution">
        <p>TEXT OF SOLUTION</p>
      </div>
    </solution>
    </problem>

Answer Created Using a Script
************************************

.. code-block:: xml

  <problem>

  <!-- The following lines use Python script spacing. Make sure it is not indented when you add it to the problem component. -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

    <legend>TEXT OF PROBLEM</legend>
    <numericalresponse answer="$computed_response">
      <responseparam type="tolerance" default="0.0001" />
      <formulaequationinput label="TEXT OF PROBLEM"/>
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>

    <solution>
      <div class="detailed-solution">
        <p>TEXT OF SOLUTION</p>
      </div>
    </solution>
  </problem>

====
Tags
====

* ``<numericalresponse>`` (required): Specifies that the problem is a
  numerical input problem.

* ``<formulaequationinput />`` (required): Provides a response field where the
  learner enters a response.

* ``<correcthint>`` (optional): Specifies feedback for the correct answer.

* ``<responseparam>`` (optional): Specifies a tolerance, or margin of error,
  for an answer. Also specifies a partial credit tolerance multiplier.

* ``<script>`` (optional)

.. note:: Some older problems use the ``<textline math="1" />`` tag instead
 of the ``<formulaequationinput />`` tag. However, the ``<textline math="1"
 />`` tag has been deprecated. All new problems should use the
 ``<formulaequationinput />`` tag.

**Tag:** ``<numericalresponse>``

Specifies that the problem is a numerical input problem. The
``<numericalresponse>`` tag is similar to the ``<formularesponse>`` tag, but
the ``<numericalresponse>`` tag does not allow unspecified variables.

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - answer (required)
       - The correct answer to the problem, given as a mathematical
         expression.
     * - partial_credit (optional)
       - Specifies the type of partial credit given. ``close``, ``list``, or a
         combination of both in any order separated by a comma (,).

  .. note:: If you include a variable name preceded with a dollar sign
   ($) in the problem, you can include a script in the problem that computes
   the expression in terms of that variable.

  The grader evaluates the answer that you provide and the learner's response
  in the same way. The grader also automatically simplifies any numeric
  expressions that you or a learner provides. Answers can include simple
  expressions such as "0.3" and "42", or more complex expressions such as
  "1/3" and "sin(pi/5)".

  Children

  * ``<responseparam>``
  * ``<formulaequationinput>``
  * ``<correcthint>``

**Tag:** ``<formulaequationinput>``

Creates a response field in the LMS where learners enter a response.

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - label (required)
       - Specifies the name of the response field.
     * - size (optional)
       - Defines the width, in characters, of the response field in the LMS.

  Children

  (none)

**Tag:** ``<responseparam>``

Specifies a tolerance, or margin of error, for an answer.

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - type (optional)
       - "tolerance": Defines a tolerance for a number.
     * - default (optional)
       - A number or a percentage specifying a numerical or percent tolerance.
     * - partial_range (optional)
       - For partial credit problems of type close, a multiplier for the
         tolerance. Default is 2.
     * - partial_answers (optional)
       - For partial credit problems of type list, a comma-separated list of
         values that are to receive 50% credit.

  Children

  (none)

**Tag:** ``<correcthint>``

Specifies a hint for the correct answer.

**Tag:** ``<script>``

Specifies a script that the grader uses to evaluate a learner's response. A
problem behaves as if all of the code in all of the script tags were in a
single script tag. Specifically, any variables that are used in multiple
``<script>`` tags share a namespace and can be overridden.

As with all Python, indentation matters, even though the code is embedded in
XML.

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - type (required)
       - Must be set to "loncapa/python".

  Children

  (none)

**Tag:** ``<demandhint>``

Specifies hints available to the learner.

  Children

  ``<hint>``

**Tag:** ``<hint>``

Specifies a hint available to the learner.

  Children

  (none)


