
.. _Set up Discussions in Cohorted Courses:

######################################################
학습집단별 게시판 설정하기
######################################################

이 장은 학습집단별 게시판을 설정하는 방법을 다룬다.

.. contents::
  :local:
  :depth: 1

*********
개관
*********

학습 집단 기능이 활성화된 강좌에서, 학습 집단에 따라 토의 주제를 나누거나 모든 학습자가 같은 토의 주제를 다룰 수 있도록 설정할 수 있다.

집단 별로 나뉘어 있는 게시판 주제는 모든 학습자에게 공개되나 글, 반응 및 답변은 집단 내 학습자에게만 공개된다. 모든 학습자가 참여하는 게시판의 글, 반응 및 답변은 집단과 관계없이 모든 학습자에게 공개된다.

최초로 학습 집단을 활성화했을 때, 일반 주제를 위한 활동과 주제별 토의 주제의 활동은 차이가 있다

시스템은 기본적으로, 일반 주제는 학습자 모두에게 통합적으로 제시하고, 주제별 토의 주제는 학습 집단별로 나누어 제시한다. 토의 유형을 나누거나 통합하도록 설정할 수 있다

.. warning:: 학습자가 게시판에 글을 올리기 시작한 이후 실시간 강좌 게시판 집단 설정을 바꾼다면 학습자에게 크게 영향을 주게 된다. 학습자는 전에 보지 못하던 글을 보거나 볼 수 있던 글을 못보게 될 수 있다. 이러한 점을 명심하고 집단 설정을 변경해야 한다. 자세한 사항은 :ref:`Altering Cohort Configuration` 를 참고하면 된다.

게시판 학습집단 설정에 관해 다음을 참고하면 된다.

* :ref:`Coursewide Discussion Topics and Cohorts`
* :ref:`Specify Whether CourseWide Discussion Topics are Cohorted`
* :ref:`Content Specific Discussion Topics and Cohorts`
* :ref:`Specify that All ContentSpecific Discussion Topics are Cohorted`
* :ref:`Specify Some ContentSpecific Discussion Topics as Cohorted`

강좌에서 토의에 관한 개괄적 정보는  :ref:`Discussions`  에서 볼 수 있다.강좌에 학습집단 사용에 관한 정보는 :ref:`Cohorts Overview` 와  :ref:`Moderating Discussions for Cohorts` 에서 볼 수 있다.

.. note:: 게시판을 학습집단으로 구분짓는 것은 게시판 글을 집단 별로 나누는 것이며 게시판 주제는 강좌 내 모든 학습자에게 공개된다. 콘텐츠별 게시판 주제를 생성해 특정 집단에만 공개하고 싶다면 게시판 구성요소의 공개 설정을 바꿔야 한다. 자세한 사항은  :ref:`Cohorted Courseware Overview`  를 참고하면 된다.

.. _Coursewide Discussion Topics and Cohorts:

***********************************************
일반 토의 주제와 학습 집단
***********************************************

최초로  :ref:`Create CourseWide Discussion Topics` 했을 때, 토의 주제는 모든 학습자에게 통합적으로 제시되고, 강좌의 모든 학습자는 속한 학습 집단에 상관 없이 이 주제에 대하여 게시글을 쓰고, 읽고, 응답하고, 코멘트를 남길 수 있다. 


일반 토의 주제를 추가한 후, 토의 주제가 학습 집단에 따라 분류되도록 환경 설정을 할 수 있다. 게시판 주제가 학습 집단에 따라 분류되었는지 확인하기 위해  :ref:`Specify Whether CourseWide Discussion Topics are Cohorted`  를 참고한다.


====================================================================
예시: 학습 집단별 일반 주제 게시판 설정
====================================================================

일반 주제 게시판은 기본 설정으로 모든 학습자에게 공개되어 있다. 그러나 학습 집단별로 일반 주제 게시판을 나눠 학습자가 집단별로 글을 보고 반응할 수 있도록 할 수 있다.

다음 예제는 시스템에서 제공하는 주제에 3개의 일반 주제를 더해 총 4개의 게시판 주제를 갖는다.

* 주제
* 강좌 Q&A
* 공지사항
* 브레인스토밍

주제와 강좌 Q&A 항목의 글은 모든 학습자에게 공개하는 것이 좋다.

그러나, 주제와 공지사항을 학습 집단별로 진행할 수 있도록 해당 주제에 학습 집단을 설정할 수 있다. 학습 집단별 일반 주제 게시판 분류 유무를 확인하기 위해  :ref:`Specify Whether CourseWide Discussion Topics are Cohorted` 를 참고한다.

또한, 학습자가 해당 주제에 게시물을 추가하기 전에, 확인할 수 있는 사람이 누구인지 알 수 있도록 설정할 수 있다. 이러한 기능을 사용하기 위해서는  :ref:`Apply Naming Conventions to Discussion Topics`  를 참고하면 된다.

.. _Specify Whether CourseWide Discussion Topics are Cohorted:

********************************************************************
학습 집단별 일반 주제 게시판 분류 설정하기
********************************************************************

일반 주제 게시판은 기본 설정으로 모든 학습자에게 공개되어 있다. 그러나 학습 집단별로 일반 주제 게시판을 나눠 학습자가 집단별로 글을 보고 반응할 수 있도록 할 수 있다.

일반 주제 게시판 설정을 바꾸기 위해.

#. 학습 관리 시스템에서 교수자를 선택하고 학습집단을 클릭한다.

#. 게시판 주제 학습 집단별 분류 유무 설정을 선택한다.

#. 일반 주제 게시판에서 학습 집단별로 나눌 게시판 주제 옆의 체크박스를 클릭해 나눌 주제를 선택한다. 다시 체크박스를 누르면 모든 학습자에게 공개된다.

#. 저장을 선택한다.

   일반 주제 게시판 주제 목록에 반영된다.

   .. image:: ../../../../shared/images/CohortDiscussionsCourseWide.png
     :alt: Two course-wide discussion topics in list, one cohorted and one
       unified.
     :width: 400

자세한 사항은 :ref:`Moderating Discussions for Cohorts` 를 참고하면 된다.

.. _Content Specific Discussion Topics and Cohorts:

**********************************************
주제별 토의와 학습집단
**********************************************

강좌에서 학습 집단 기능을 활성화하고, 스튜디오의 토의 구성 요소를 학습 활동에 추가하여  :ref:`Create ContentSpecific Discussion Topics`  할 때, 주제별 토의는 학습집단 기본 값으로 나뉘어진다. 하나의 학습집단에 배치된 학습자는 다른 학습집단 회원의 온라인 학습 활동들을 읽어보거나 게시글, 응답, 코멘트를 추가할 수 없다.

모든 주제별 토의를 학습집단으로 나누고자 한다면, 어떤 설정도 할 필요가 없다. 자세한 사항은  :ref:`Specify that All ContentSpecific Discussion Topics are Cohorted` 를 참고하면 된다.

아니면 대부분의 콘텐츠별 게시판 주제를 전체 학습자에게 공개하고 일부만 학습 집단별로 분류할 수 있다.

.. _Specify that All ContentSpecific Discussion Topics are Cohorted:

*****************************************************************
모든 콘텐츠별 게시판 주제 학습 집단별로 나누기
*****************************************************************

콘텐츠별 게시판 주제의 기본 설정은 처음 강좌에 추가할 때 학습 집단별로 분류되는 것이다. 모든 주제별 토의를 학습집단으로 나누고자 한다면, 어떤 설정도 할 필요가 없다.

이 설정을 교수자 대시보드 학습집단 탭에서 확인할 수 있다.

#. 학습 관리 시스템에서 교수자를 선택하고 학습집단을 클릭한다.

#. 게시판 주제 학습 집단별 분류 유무 설정을 선택한다.

  .. image:: ../../../../shared/images/CohortDiscussionsSpecifyLink.png
    :alt: The link in the UI to specify whether content specific discussion
        topics are divided by cohort.
    :width: 800

**콘텐츠별 게시판 주제** 탭에 게시판 주제 언제나 학습 집단별로 분류가 선택되어 있는 것을 확인할 수 있다.

모든 콘텐츠별 게시판 주제는 학습 집단별로 분류되며 개별 콘텐츠별 게시판 주제의 학습집단 설정을 바꿀 수 없다.

.. image:: ../../../../shared/images/CohortDiscussionsAlwaysCohort.png
 :alt: Content specific discussion topics controls with the "Always cohort
  content specific discussion topics" option selected.
 :width: 500

게시판 주제의 일부만 학습 집단별로 분류하는 방법은 :ref:`Specify Some ContentSpecific Discussion Topics as Cohorted` 을 참고한다.

.. _Specify Some ContentSpecific Discussion Topics as Cohorted:

**************************************************************************
콘텐츠별 게시판 주제 일부만 학습 집단별로 분류 설정
**************************************************************************

콘텐츠별 게시판 주제의 기본 설정은 처음 강좌에 추가할 때 학습 집단별로 분류되는 것이다.

일부 게시판 주제만 학습 집단별로 분류하기 위해선 우선 모든 학습자에게 공개되도록 설정한 후 학습 집단별로 분류할 일부 주제만 선택해야 한다.

.. warning:: 학습집단 설정을 콘텐츠별 게시판 주제 항상 학습 집단별로 분류에서 콘텐츠별 게시판 주제 일부 학습 집단별로 분류로 설정을 변경하면 모든 콘텐츠별 게시판 주제를 학습자에게 공개하되 선택한 일부만 학습 집단별로 공개되는 것이다. 이는 기존에 학습 집단별로 나뉘어져 조회, 반응 및 답변이 제한되었던 글은 이제 모든 학습자에게 공개된다는 의미이다.

   설정을 바꿀 때 일어날 수 있는 결과를 명심하고 집단 설정을 변경해야 한다. 자세한 사항은 :ref:`Altering Cohort Configuration`  를 참고하면 된다.

콘텐츠별 게시판 주제 일부만 학습 집단별로 분류하기 위해.

#. 학습 관리 시스템에서 교수자를 선택하고 학습집단을 클릭한다.

#. 게시판 주제 학습 집단별 분류 유무 설정을 선택한다.

   .. image:: ../../../../shared/images/CohortDiscussionsSpecifyLink.png
    :alt: The link in the UI to specify whether content specific discussion
        topics are divided by cohort.
    :width: 800

#. 콘텐츠별 게시판 주제 탭에서 콘텐츠별 게시판 주제 일부 학습 집단별로 분류를 선택한다.

   .. warning:: 설정을 바꿀 때 일어날 수 있는 결과를 명심하고 집단 설정을 변경해야 한다. 자세한 사항은 :ref:`Altering Cohort Configuration`  를 참고하면 된다.

   강좌에 추가하는 콘텐츠별 게시판 주제는 모든 학습자에게 공개된다. 콘텐츠별 게시판 주제를 편집할 수 있게 된다.

#. 학습 집단별로 공개할 각 콘텐츠별 게시판 주제 옆 체크박스를 선택한다.

   .. image:: ../../../../shared/images/CohortDiscussionsCohortSelected.png
     :alt: Content specific discussion topics controls with the "Cohort
      selected content specific discussion topics" option selected.
     :width: 500

#. 저장을 선택한다.

   콘텐츠별 게시판 주제 변경사항이 저장된다. 선택한 콘텐츠별 게시판 주제는 학습 집단별로 분류된다. 기타 콘텐츠별 게시판 주제는 모든 학습자에게 공개된다.

학습 집단별로 분류된 게시판에 대해선  :ref:`Moderating Discussions for Cohorts`  를 참고하면 된다.
