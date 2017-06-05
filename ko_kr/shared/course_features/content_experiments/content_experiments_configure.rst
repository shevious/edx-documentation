.. _Configure Your Course for Content Experiments:

#####################################################
콘텐츠 실험을 위한 강좌 설정하기
#####################################################

이 장은 강좌에서 콘텐츠 실험을 사용하기 위한 방법에 대해 다룬다.

.. contents::
  :local:
  :depth: 1

.. _Enable Content Experiments:

****************************************
콘텐츠 실험을 활성화하기
****************************************

강좌에서 콘텐츠 실험을 활성화하기 위해, ``split_test`` 를 고급설정에서 고급 모듈 목록 에 추가한다.

.. note::
  ``split_test`` 는 콘텐츠 실험의 내부 K-MOOC 플랫폼 이름이다.

#. 환경 메뉴에서 고급환경 을 선택한다.

#. 고급환경 에서, 고급 모듈 목록 을 찾는다.

#. 고급 모듈 목록 칸에,  ``"split_test"`` 를 추가한다. 큰따옴표가 포함되었는지 확인한다.

   여러 개의 값이 있다면, 쉼표로 분리한다. 
   (``,``).

   예를 들어, 고급 모듈 목록 칸에 입력되는 텍스트는 다음과 같을 것이다:

   .. code-block:: json

     [
       "lti_consumer",
       "word_cloud",
       "split_test"
     ]

#. 페이지 하단에 다시 저장 을 클릭한다

.. _Overview of Group Configurations:

****************************************
그룹 설정 개관
****************************************

콘텐츠 실험을 만들기 전에 강좌에서 최소한 1개의 그룹을 설정해야 한다 .

그룹 설정은 실험에 참여하는 그룹의 수를 정한다. 콘텐츠 실험을 만들 때, 활용하기 위한 그룹 설정을 선택한다.

예를 들어, 강좌에서 다른 시기에 다른 2개의 실험을 원한다고 하자. 콘텐츠 실험에서, 학습자는 동영상을 보거나 읽기 과제를 한다. 어떤 그룹이 자료를 더 잘 학습하였는지 확인하기 위해 문제를 추가할 수 있다. 콘텐츠 실험에서, 2개의 실험 그룹에 학생들을 배정하기 위해 그룹 설정한다.

다른 콘텐츠 실험에서, 문제의 4개의 다른 유형을 이용하여 동일 질문을 보여 줄 수 있다. 이 콘텐츠 실험에서, 학습자들을 4개의 실험 그룹에 배정하도록 그룹을 설정한다.

=======================================
실험 그룹에 학습자 배정하기
=======================================

K-MOOC 플랫폼은 그룹 설정에서 학습자를 각 실험 그룹에 배정한다.

실험 그룹 배정의 특징은 다음과 같다:

* 다이나믹하다(역동적이다)

  K-MOOC 플랫폼은 학습자를 하나의 실험 그룹에 우선 배정하면, 학습자는 그룹 설정에 따른 콘텐츠 실험에 참여하게 된다.

* 무작위이다.

  학습자가 할당되는 실험그룹은 조정할 수 없다.

* 고르게 분포된다.

  K-MOOC 플랫폼은 실험 그룹들의 크기를 계속 점검하고, 새로운 학습자를 그룹에 고르게 배정한다. 예를 들어, 2개의 실험 그룹이 설정에 되어 있다면, 각 그룹은 강좌에 등록한 50%의 학습자를 포함하게 된다; 4개의 실험 그룹이 있다면, 각 그룹은 학습자의 25%씩 배정된다.

* 영구적이다.

  동일한 그룹 설정에 적용되는 콘텐츠 실험의 수와 관계 없이 학습자는 배정된 실험 그룹에 남아 있게 된다.

.. _Set up Group Configurations in edX Studio:

************************************************
Studio에서 실험 그룹 설정하기
************************************************

.. note::
  그룹을 설정하기 전에 콘텐츠 실험을 활성화 해야 한다.

그룹 설정을 하기 위해, 설정 메뉴에서, 그룹 설정 을 선택한다. 그룹 설정 페이지가 열린다.

이 페이지에서 그룹 설정을 생성하고, 편집하고, 삭제를 할 수 있다. 또한 그룹 설정을 사용하는 실험들을 볼 수 있다.

.. _Create a Group Configuration:

=============================
실험 그룹 설정 생성하기
=============================

항상 그룹 설정을 생성할 수 있다.

#. 그룹 설정 페이지에서, 실험 그룹 을 선택하고, 새 실험 그룹 을 클릭한다. 다음 페이지가 나타난다:

   .. image:: ../../../../shared/images/create-group-config.png
    :width: 800
    :alt: An image of the Create a New Group Configuration page in Studio.

#. 그룹 설정명 을 입력한다. 의미 있는 명칭을 이용 하는 것은 콘텐츠 실험을 만들 때 그룹 설정을 선택하기 때문이다. 학습자는 이 그룹 설정명을 알지 못한다.

#. 선택적으로, 새로운 그룹 설정에 대한 설명을 입력한다.

#. 기본적으로, 새로운 설정은 2개의 그룹이 포함되어 있다. 그룹을 수정하거나 필요에 따라 추가 혹은 삭제할 수 있다. 그룹 설정은 최소 1개의 그룹은 있어야 한다.

   * 그룹 명을 필요한 만큼 수정한다. Studio의 학습 활동 페이지에서 그룹 명을 볼 수 있다. 그러나, 학습자는 그룹명을 볼 수 없다.
   * 설정에 또다른 **그룹을 추가하기** 위해 다른 **그룹 추가** 를 클릭한다.
   * 기존의 그룹의 오른쪽에 **X** 를 클릭하여 설정으로부터 제거할 수 있다. 그룹 설정에는 최소 1개의 그룹이 있어야 한다.

#. **생성** 을 클릭하여 새 그룹 설정을 저장한다.

그러면 그룹 설정은 페이지에 나타난다. 설정에 포함된 그룹의 수를 볼 수 있고, 설정이 강좌에서 사용되는지 여부를 볼 수 있다:

.. image:: ../../../../shared/images/group_configurations_one_listed.png
 :width: 800
 :alt: The Group Configurations page with one group configuration listed.

.. _Edit a Group Configuration:

=============================
그룹 설정 편집하기
=============================

.. important:: 그룹 설정의 명칭은 언제든지 변경할 수 있다. 그러나 운영중인 강좌에 현재 이용되는 그룹 설정의 성격을 변경하기 전에  `Guidelines for Modifying Group Configurations`_  을 살펴본다.

#. **그룹 설정** 페이지에서, 그룹 설정으로 가서 **편집** 을 클릭한다.

   .. image:: ../../../../shared/images/group_configurations_edit.png
    :alt: An image of the Group Configurations page with Edit button
        highlighted.
    :width: 800

   The following page opens:

   .. image:: ../../../../shared/images/save-group-config.png
    :alt: An image of the Edit a Group Configuration page.
    :width: 800

#. 필요하다면 명칭과 설명을 수정한다.

#. 필요하다면 설정에서 그룹을 수정한다.  `Create a Group Configuration`_  에 자세하게 안내되어 있다.

#. **저장** 을 클릭하여 변경사항을 저장한다.

.. _Delete a Group Configuration:

=============================
그룹 설정 삭제하기
=============================

.. note::
 콘텐츠 실험에서 현재 사용되지 않는 그룹 설정을 삭제할 수 있다. 콘텐츠 실험에서 사용되고 있는 그룹 설정은 삭제할 수 없다.

#. **그룹 설정** 페이지에서, 그룹 설정으로 이동하고 삭제 아이콘을 클릭한다.

   .. image:: ../../../../shared/images/group-configuration-delete.png
    :alt: An image of the Edit a Group Configuration page.
    :width: 800

#. 삭제를 확인하기 위해 메세지가 나타날 때, **삭제** 를 클릭한다.

.. _View Experiments that Use a Group Configuration:

===============================================
그룹 설정을 이용하는 실험 보기
===============================================

각 그룹 설정을 사용하는 실험을 볼 수 있다.

그룹 설정 페이지에서, 자세한 사항을 보기 위해 그룹명을 클릭한다. 그룹설정을 사용한 실험의 링크를 보게 된다:

.. image:: ../../../../shared/images/group_configurations_experiments.png
 :alt: An image of a group configuration with the experiments using the
     configuration circled.
 :width: 800

실험이 포함된 학습활동 페이지로 이동하기 위해 링크를 클릭한다.

===============================================
실험에서 그룹 설정 보기
===============================================

콘텐츠 실험 작업에서, 두가지 방법으로 실험에 사용되는 그룹 설정에 대해 볼 수 있다:

* 콘텐츠 실험을 포함하는 학습활동에서, 콘텐츠 실험 블럭에서, 그룹 설정명을 클릭한다.

  .. image:: ../../../../shared/images/content_experiment_group_config_link.png
   :alt: An image of the content experiment in the unit page with the group
     configuration link circled
   :width: 800

* 콘텐츠 실험페이지의 상단에, 그룹 설명명을 클릭한다.

  .. image:: ../../../../shared/images/content_experiment_page_group_config_link.png
   :alt: An image of the content experiment page with the group configuration
       link circled.
   :width: 800

이제 그룹 설정이 나타난다:

.. image:: ../../../../shared/images/group_configurations_experiments.png
 :alt: An image of the Group Configuration page with the experiments using it
     circled.
 :width: 800

콘텐츠 실험이 포함된 학습활동으로 돌아가기 위해 그룹 설정에 있는 링크를 이용할 수 있다.

.. import OLX-content experiment doc that's shared in OLX guide.

.. include:: ../../../../shared/course_features/content_experiments/subsection_content_experiments_group_modify_guidelines.rst

.. include:: ../../../../shared/course_features/content_experiments/subsection_content_experiments_policies.rst
