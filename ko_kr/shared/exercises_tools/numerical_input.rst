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

학습자가 입력할 수 있는 문자에 관한 보다 구체적인 정보를 :ref:`Math Formatting` 에서 확인할 수 있다.

학습자가 작성한 정답이 정확할 필요 없게 오차범위를 설정할 수도 있다. Python 스크립트를 사용하거나 정확한 정답을 설정할 수 있다.

.. note::
  모든 학습활동 페이지에서 계산기를 활용할 수 있다. 자세한 사항은  :ref:`Calculator` 를 참고하면 된다.

**************************************************
수치 입력 문제 성과 분석하기
**************************************************

강좌의 수식 입력 문제에 Insights를 사용해 학습자 성과 데이터 및 답안을 분석할 수 있다. 자세한 사항은  :ref:`Using edX Insights`  를 참고하면 된다.

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

:ref:`Simple Editor`  로 수식 입력 문제를 생성하기 위해.

#. **신규 구성요소 추가** 에서 **문제** 를 클릭한다.
#. 두가지 문제 템플릿 중 하나를 선택한다.

   * **일반문제유형** 탭의 **수치 입력** 을 클릭한다.

   * 일반문제유형탭에서 힌트가 있는 수치 입력을 클릭한다. 자세한 사항은  `수식 입력 문제에서 피드백 사용하기`_  를 참고하면 된다.

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
고급 편집기로 수식 입력 문제 만들기
========================================================================

고급 편집기로 수식 입력 문제를 만들기 위해.

#. :ref:`Use the Simple Editor to Create a Numerical Input Problem` 에서 문제를 만들었던 절차들을 따른다.
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
수식 입력 문제에서 피드백 사용하기
********************************************

간편 편집기나 고급 편집기를 사용해 수식 입력 문제에 피드백을 추가할 수 있다. 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

수식 입력 문제에서 정답에 대해 피드백을 추가할 수 있다.

.. note::
  수식 입력 문제는 오답에 대해 피드백을 추가할 수 없다.

정답에 피드백을 추가해 정답 유추 과정을 설명한다.

=======================================
간편 편집기에서 피드백 설정하기
=======================================

:ref:`Simple Editor` 에서 다음과 같이 피드백을 설정할 수 있다. 새 수식 입력 문제를 만들 때 힌트와 **피드백이 있는 수식 입력 문제** 템플릿을 선택한다. 이 템플릿엔 예제가 포함되어 있다.

::

  = Numerical Answer {{Feedback for the correct answer.}}

다음 예제는 각 정답에 대한 피드백을 포함하고 있다.

::

  >>What is the arithmetic mean for the following set of numbers?
    (1, 5, 6, 3, 5)<<

  = 4 {{The mean for this set of numbers is 20 / 5 which equals 4.}}

=========================================
고급 편집기에서 피드백 설정하기
=========================================

:ref:`Advanced Editor` 에서 다음과 같이 피드백을 설정할 수 있다.

.. code-block:: xml

    <numericalresponse answer="Correct Answer">
      <formulaequationinput label="Question" />
      <correcthint>
        Feedback for the correct answer.
      </correcthint>
    </numericalresponse>

다음 예제는 정답에 대한 피드백을 포함하고 있다.

.. code-block:: xml

  <numericalresponse answer="4">
    <formulaequationinput label="What is the arithmetic mean for the following
      set of numbers? (1, 5, 6, 3, 5)" />
    <correcthint>
      The mean for this set of numbers is 20 / 5 which equals 4.
    </correcthint>
  </numericalresponse>

=========================
사용자 지정 피드백 라벨
=========================

기본적으로 정답에 대한 피드백 라벨은 **정답** 이다. 사용자 지정 피드백을 설정하지 않으면 다음 예제와 같이 학습자는 이 라벨을 보게 된다.

.. image:: ../../../shared/images/numerical_input_feedback.png
 :alt: Numerical input feedback with the standard label.
 :width: 600

사용자 지정 라벨을 사용하여 다음 예제와 같이 보여줄 수 있다.

.. image:: ../../../shared/images/numerical_input_feedback_custom_label.png
 :alt: Numerical input feedback with a custom label.
 :width: 600

.. note::
  **정답** 과 **오답** 기본 라벨은 학습자의 언어로 보이게 된다. 그러나 사용자 지정 라벨을 사용하면 모두 설정 언어로 보이게 되며 번역되지 않는다.

편집기에서 사용자 피드백 라벨 설정하기
***********************************************

:ref:`Simple Editor` 에서 사용자 지정 피드백 라벨을 설정할 수 있다.

::

  = 4 {{Label::Feedback}}

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

::

  = 4 {{Good Job::The mean for this set of numbers is 20 / 5 which equals 4.}}

고급 편집기에서 사용자 지정 피드백 라벨 설정하기
*************************************************

:ref:`Advanced Editor` 에서 다음과 같이 사용자 지정 피드백 라벨을 설정할 수 있다.

.. code-block:: xml

    <correcthint label="Custom Label">
      Feedback
    </correcthint>

다음 예제는 사용자 지정 피드백 라벨을 사용하고 있다.

.. code-block:: xml

  <correcthint label="Good Job">
    The mean for this set of numbers is 20 / 5 which equals 4.
  </correcthint>

.. _Use Hints in a Numerical Input Problem:

********************************************
수식 입력 문제에서 힌트 사용하기
********************************************

간편 편집기나 고급 편집기를 사용해 수식 입력 문제에서 힌트를 사용할 수 있다. 문제의 힌트에 대한 자세한 사항은 :ref:`Adding Feedback and Hints to a Problem` 를 참고하면 된다.

.. include:: ../../../shared/exercises_tools/Subsection_configure_hints.rst

.. _Awarding Partial Credit in a Numerical Input Problem:

*****************************************************
수식 입력 문제에서 부분 점수 부여하기
*****************************************************

수식 입력 문제에서 정답에 근접한 답변에 대해 부분 점수를 부여할 수 있다. 이때 반드시  :ref:`Use the Advanced Editor to Create a Numerical Input Problem` 를 사용해야 한다


.. only:: Partners

 .. note::
    테스트서버와 kmooc.kr에서 부분점수를 사용하는 기능은 아직 개발 중이다. 사용 전 확실히 테스트를 거쳐야 한다. 자세한 사항은 K-MOOC 파트너 매니저(관리자)에게 문의하면 된다.

다음 예제에서 학습자는 정답에 근접한 답변을 제출했으며 부분점수를 받았다.

.. image:: ../../../shared/images/partial_credit_numerical_input.png
 :alt: A numerical input problem with partial credit for a close answer.
 :width: 600

부분점수에 대한 전체적인 개관은 :ref:`Awarding Partial Credit for a Problem` 를 참고하면 된다. 

수식 입력 문제에 부분점수를 부여하는 방법은 두 가지 있다.

.. contents::
  :local:
  :depth: 1

.. Note:: 이 두 가지 방법을 동시에 사용할 수 있다.

==========================
정답에 근접한 답변
==========================

정답과 근접한 답변이 부분점수를 얻을 수 있도록 수식 입력 문제를 설정할 수 있다.

오답에 대한 한계를 설정한다. 학습자는 이 오차범위를 바탕으로 부분점수를 얻게 된다. 기본적으로 이 허용 한계의 두 배 수까지 답으로 인정하며 다음과 같은 규칙에 따라 부분점수를 부여한다.

* 허용 한계 내 답변은 점수의 100%를 획득한다.

* 허용 한계의 2배 내 답변은 점수의 50%를 획득한다.

* 허용 한계 2배 외 답변은 점수를 획득하지 못한다.

허용 한계를 3배 수로 설정할 수도 있다.

* 허용 한계 내 답변은 점수의 100%를 획득한다.

* 허용 한계의 3 배 내 답변은 점수의 50%를 획득한다.

* 허용 한계 3 배 외 답변은 점수를 획득하지 못한다.

수식 입력 문제에서 정답에 근접한 답변 설정하기
******************************************************

수식 입력 문제에서 정답에 근접한 답변에 대해 부분점수를 부여하도록 설정할 수 있다. 이 때 문제 XML에 다음 속성을 추가하면 된다.

* ``<numericalresponse>`` 요소에 ``"partial_credit="close"`` 속성을 추가한다. 만약 정답에 근접한 답변을 여러 가지 사용한다면  ``partial_credit="close,list"``  를 설정으로 한다.

* (선택사항)  ``<responseparam>`` 요소에  ``partial_range`` 속성을 추가하고 허용 한계를 설정한다. 따로 허용 한계 ``partial_range`` 를 정하지 않으면 2를 사용하게 된다.


다음 수식 입력 문제 템플릿에서 정답에 근접한 답변에 대해 부분점수를 사용하고 있다.

.. code-block:: xml

  <numericalresponse answer="9.3*10^7" partial_credit="close">
    <formulaequationinput label="How many miles away from Earth is the sun?
      Use scientific notation to answer." />
    <responseparam type="tolerance" default="1%" partial_range="3"/>
  </numericalresponse>

=============================================
답변 목록에 대해 부분점수 부여하기
=============================================

일부 수식 입력 문제에서 실수로 학습자의 답을 정답이 아니게 유도할 수 있다. 예를 들어 작은 실수가 부정적인 결과로 이어질 수도 있고 혹은 제곱근이나 다른 수치로 인한 결과일 수도 있다.

이런 문제들에 대해 부분 점수를 얻을 수 있는 답변 목록을 설정할 수 있다. 이 목록의 답변을 제출한 학습자는 점수의 50%를 얻을 수 있다.


수식 입력 문제에 목록 설정하기
************************************************

수식 입력 문제에서 답변 목록에 대해 부분점수를 부여하려면 다음 속성을 문제 XML에 추가해야 한다.

* ``<numericalresponse>`` 요소에  ``partial_credit="list"`` 속성을 추가한다. 만약 정답에 근접한 답변과 동시에 사용 중이라면 속성을  ``partial_credit="close,list"`` 로 한다.

* ``<responseparam>`` 요소에  ``partial_answers`` 속성을 추가한다. 하나 이상의 답변이 점수의 50%를 획득할 수 있도록 설정하고 여러 값이 있을 경우 ,로 구분한다.

다음 수식 입력 문제 템플릿에서 답변 목록에 대해 부분점수를 사용하고 있다.

.. code-block:: xml

  <numericalresponse answer="93*10^7" partial_credit="list">
    <formulaequationinput label="How many miles away from Earth is the sun?
      Use scientific notation to answer." />
    <responseparam partial_answers="150*10^6"/>
  </numericalresponse>

******************************************
수식 응답 필드에 텍스트 추가하기
******************************************

수식 입력 문제 답변 필드에 단어, 구문이나 문장을 추가해 문제의 헷갈리는 부분에 대해 설명할 수 있다.

.. image:: ../../../shared/images/NI_trailing_text.png
 :width: 500
 :alt: Three numerical input problems with text after the response field:
     "km", a percent sign, and a symbol for meters per second squared.

이 기능은 반드시  :ref:`Advanced Editor` 를 사용해야 한다.

고급 편집기에서 문제를 열고 ``formulaequationinput`` 요소를 찾는다. 이 요소는 문제에 응답 필드를 만든다.  ``formulaequationinput`` 요소는 ``numericalresponse`` 요소의 하위요소이다.

답변 필드에 텍스트를 추가하기 위해  ``trailing_text`` 속성을 ``formulaequationinput`` 요소 내에 사용할 텍스트와 함께 추가한다.

.. note:: ``trailing_text`` 속성 내에서 MathJax를 3번째 예제와 같이 사용할 수 있다. 이 속성에서 HTML은 사용할 수 없다.

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
수식 입력 문제 XML
****************************

=========
템플릿
=========

십진법 숫자 체계 또는 백분율로 나타낸 허용 한계 부여 여부에 따른 수식 입력 문제의 템플릿이다.

허용 한계를 주지 않은 문제
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

십진법 숫자로 허용 한계를 준 문제
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

백분율 허용 한계를 준 문제
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

스크립트로 생성한 정답
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
태그
====

* ``<numericalresponse>`` (필수): 해당 문제를 수식 입력 문제로 지정한다.

* ``<formulaequationinput />`` (필수): 학습자 답변을 입력할 답변 필드를 제공한다.

* ``<correcthint>`` (선택사항): 정답에 대한 피드백을 나타낸다.

* ``<responseparam>`` (선택): 정답에 대한 허용 한계 또는 오차 범위를 지정한다. 또 부분점수 허용 한계를 지정한다.

* ``<script>`` (선택)

.. note:: 기존 문제 일부는 ``<formulaequationinput />`` 태그 대신  ``<textline math="1" />`` 태그를 사용하고 있다. 그러나  ``<textline math="1" />`` 태그에 대한 비판이 있기 때문에 새로 생성하는 문제에서는 ``<formulaequationinput />`` 태그를 사용한다.

**태그:** ``<numericalresponse>``

해당 문제를 수식 입력 문제로 지정한다. ``<numericalresponse>`` 태그는  ``<formularesponse>`` 와 유사하지만 지정되지 않은 변수를 허용하지 않는다는 점에서 다르다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 답  (필수)
       - 문제의 정답. 수식으로 제시된다.
     * - 부분점수 (선택)
       - 부분점수의 종류를 지정한다. 각 종류는 ,로 구분된다.

  .. note:: 문제 지문에서 변수명 앞에 달러 기호($)를 붙이면 해당 수식을 해당 변수에 대해 계산하는 스크립트를 삽입할 수 있다.

  채점자는 제공하는 답과 학습자 답변을 동일한 방식으로 평가한다. 또한 채점자는 강좌 운영팀이 제공하는 또는 학습자가 제공하는 어떠한 수식에 대해 이를 자동적으로 단순화한다. 정답은 0.3이나 42처럼 단순할 수도, 1/3이나 sin(pi/5)처럼 다소 복잡할 수도 있다.

  Children

  * ``<responseparam>``
  * ``<formulaequationinput>``
  * ``<correcthint>``

**Tag:** ``<formulaequationinput>``

학습자가 답변을 입력하는 LMS에 답변 필드를 생성한다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 라벨  (필수)
       - 답변 필드의 이름을 지정한다.
     * - 크기  (선택)
       - LMS 내 답변 필드의 폭(width)을 문자(개수)로 정의한다.

  Children

  (none)

**Tag:** ``<responseparam>``

정답에 대한 허용 한계 또는 오차 범위를 지정한다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 유형 (선택)
       - “허용(tolerance)”: 숫자에 대한 허용 한계를 정의한다.
     * - 기본값  (선택)
       - 십진법 체계의 수 또는 백분율 허용 한계를 지정하는 숫자 또는 백분율.
     * - 부분 범위 (선택)
       - 허용 한계를 지정한다. 기본은 2로 되어있다.
     * - 부분 답 (선택)
       - 점수의 50%를 획득하는 목록을 지정한다.

  Children

  (none)

**Tag:** ``<correcthint>``

정답에 대한 힌트를 지정한다.

**Tag:** ``<script>``

채점자가 학습자 답변을 평가하기 위해 사용하는 스크립트를 지정한다. 스크립트 내 모든 코드가 하나의 스크립트 태그에 있는 것처럼 문제는 인식한다. 구체적으로 다수의 ``<script>`` 태그에 사용되는 모든 변수는 명칭 공간을 공유하며 수정이 가능하다.

다른 Python과 마찬가지로 들여쓰기가 중요하다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - 유형  (필수)
       - “loncapa/python”으로 설정되어야 한다.

  Children

  (none)

**Tag:** ``<demandhint>``

학습자가 보게 될 힌트를 지정한다.

  Children

  ``<hint>``

**Tag:** ``<hint>``

학습자가 보게 될 힌트를 지정한다.

  Children

  (none)


