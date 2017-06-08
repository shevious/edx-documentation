.. _Awarding Partial Credit for a Problem:

***************************************
문제에 부분점수 주기
***************************************

다음과 같은 문제 유형에서 학습자에게 부분점수를 부여할 수 있다.

* :ref:`Awarding Partial Credit in a Checkbox Problem`
* :ref:`Awarding Partial Credit in a Multiple Choice Problem`
* :ref:`Awarding Partial Credit in a Numerical Input Problem`
* :ref:`Award Half Credit`

문제에 부분점수를 줌으로서 학습자가 아는 만큼 정확하게 점수를 줄 수 있고 이를 통해 의욕을 높일 수 있다.

자세한 사항은 각 문제 유형 별 내용을 참고하면 된다.

.. only:: Partners

  .. note::
    부분점수 기능은 kmooc.kr과 테스트서버에서 잠정적인 기능이다. 학습자에게 제공하기 전에 확실히 테스트할 필요가 있다. 자세한 사항은 파트너 매니저에게 (K-MOOC 관리자에게) 문의하면 된다.

==========================================
학습자가 부분점수를 얻는 방법
==========================================

학습자는 학습 관리 시스템에 정답을 입력할 때 부분 점수를 얻는다.

다음 예에서 강좌 운영팀은 오답 보기 하나에 대해서 0점이 아닌 25%를 부여하도록 부분점수를 설정했다. 이 오답을 선택한 학습자는 전체 점수의 25%를 획득하였다.

.. image:: ../../../shared/images/partial_credit_multiple_choice.png
 :alt: A multiple choice problem with partial credit for an incorrect
     answer.
 :width: 500


====================================================
부분 점수와 학습자 성취 보고
====================================================

학습자가 문제에 대해 부분 점수를 획득하면 학습 관리 시스템은 성적에 학습자가 얻은 점수만을 입력한다. 그러나 학습 관리 시스템은 다음과 같은 방법으로 학습자가 어떤 식으로든 점수를 얻은 문제를 보고한다.

* 학습자가 부분 점수를 얻었을 때 생성되는 이벤트는 학습자가 정확한 답을 했음을 알려준다. 구체적으로 correctness 필드는 correct 값을 갖는다.

  자세한 사항은  :ref:`problem` 를 참고하면 된다.

* 학습자 정답 분포 보고에서 정답에 대한 값은 1이다.

* K-MOOC Insights의 학습자 성취 보고는 그 답을 정답으로 인식한다.

강좌 운영팀은 학습자 제출 기록에서 부분 점수를 얻었던 것을 확인할 수 있다. 제출 기록은 학습자가 총 점수에서 얻은 점수를 표시해주며 ``correctness`` 필드는 ``partially-correct`` 값을 갖는다. 자세한 사항은 :ref:`Student_Answer_Submission` 을 참고하면 된다.
