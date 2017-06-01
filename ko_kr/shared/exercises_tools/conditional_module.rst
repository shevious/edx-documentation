.. _Conditional Module:

####################
조건 모듈
####################

.. note:: K-MOOC은 이 문제 유형에 대해 부분적 지원을 제공함

조건 모듈은 학습자가 어느 특정 조건을 만족하는 답변을 했을 때에만 문구가 보이도록 하는 기능이다. 예를 들어 어느 설문 조사 질문에 “예”라고 답한 학습자에겐 보이지만 “아니오”라고 답한 학습자는 볼 수 없는 것이다.

********************
양식 설명
********************

조건 모듈 입력의 주요 태그는

.. code-block:: xml

    <conditional> ... </conditional>

``conditional`` 은 모든 xmodule 태그 ( ``html``, ``video`` , ``poll`` 등) 또는 ``show`` 태그를 포함할 수 있다.

====================
``conditional`` 태그
====================

``conditional`` 태그는 상태 모듈의 단일 객체를 위한 주 컨테이너(container)이다. 이 태그는 다음의 속성을 지정할 수 있다


.. code-block:: xml

    sources - 필수모듈의 id 위치로, ';'로 분리
    [message | ""] - 하나 혹은 그 이상 통과하지 못한 경우 메시지. 필수 모듈에 링크를 만들 수 있는{link} 변수를 이용할 수 있다.

    [submitted] - map to `is_submitted` 모듈 방법에 맵핑
    (RESET 버튼을 누르면 이 함수에서 False로 되돌아가게 한다)

    [correct] - map to `is_correct` 모듈 방법에 맵핑
    [attempted] - map to `is_attempted` 모듈 방법에 맵핑
    [poll_answer] - map to `poll_answer` 모듈 속성에 맵핑
    [voted] - map to `voted` 모듈 속성에 맵핑

============
``show`` 태그
============

Xmodule의 몇 가지 세트에 대한 Symlink이다. 이 태그에 대하여 다음과 같은 속성을 지정할 수 있다.

.. code-block:: xml

    sources - 모듈 id의 위치로 ';' 로 분리된다

*********
예시
*********

========================================
예시 : 설문 조사에 의존하는 조건
========================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <h3>You see this because your vote value for "First question" was "man"</h3>
        </html>
    </conditional>

========================================================
예시 : 설문 조사에 의존하는 조건 (<show> 태그 사용하기)
========================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <show sources="i4x://MITx/0.000x/problem/test_1; i4x://MITx/0.000x/Video/Avi_resources; i4x://MITx/0.000x/problem/test_1"/>
        </html>
    </conditional>

================================================
예시 : 문제에 의존하는 조건
================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="True">
        <html display_name="HTML for attempted problem">You see this because "lec27_Q1" was attempted.</html>
    </conditional>
    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="False">
        <html display_name="HTML for not attempted problem">You see this because "lec27_Q1" was not attempted.</html>
    </conditional>
