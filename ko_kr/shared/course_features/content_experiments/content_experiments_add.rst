.. _Add Content Experiments to Your Course:

#########################################
콘텐츠 실험 추가하기
#########################################

이 장은 강좌에 콘텐츠 실험을 추가하는 법에 대해 다룬다.

.. contents::
  :local:
  :depth: 1

********************************************
콘텐츠 실험을 추가하기 전에
********************************************

강좌에 콘텐츠 실험을 추가하기 전에 반드시 다음을 수행해야 한다.

* :ref:`Enable Content Experiments`
* :ref:`Set up Group Configurations in edX Studio`

.. _Add a Content Experiment in Studio:

********************************************
스튜디오에서 콘텐츠 실험 추가하기
********************************************

학습활동이나 컨테이너 페이지에 콘텐츠 실험을 추가할 수 있다.  `Create Content for Groups in the Content Experiment`_  에 제시된 바와 같이, 컨테이너 페이지의 콘텐츠 실험 안에서 모든 그룹의 콘텐츠를 생성하고 확인한다. 

학습활동에서 학습자에게 콘텐츠 실험에 참여하고 있다는 안내나 실험명이 보이지 않는다. 학습자는 자신이 속한 학습그룹에 설정된 콘텐츠만을 볼 수 있다. 콘텐츠 실험이 있는 학습활동은 다른 학습활동과 차이가 없다.

스튜디오에서 콘텐츠 실험을 설정하려면.

#. `Create the content experiment`_.
#. `Create content for groups in the content experiment`_.

콘텐츠 실험을 설정한 후에 그룹 설정을 변경할 수 있다.  `Change the Group Configuration for a Content Experiment`_  에서 확인한다.

===============================
콘텐츠 실험 만들기
===============================

#. 학습활동 구성 페이지에서, **새로운 요소 추가** 아래에 있는 **고급** 을 선택한다.

#. **콘텐츠 실험** 을 선택한다.

   새로운 콘텐츠 실험을 학습활동에 추가한다.

   .. image:: ../../../../shared/images/content_experiment_block.png
    :width: 800
    :alt: An image showing the content experiment component in a unit page in
        Studio.

   다른 요소처럼 콘텐츠 실험 작업을 하면된다. 더 많은 정보가 필요하면  :ref:`Developing Course Components`  를 확인한다.

#. 콘텐츠 실험 구성요소를 열기 위해 **그룹 설정 선택하기** 혹은 **수정** 을 클릭한다.

   .. image:: ../../../../shared/images/content_experiment_editor.png
    :alt: An image of the content experiment editor in Studio.
    :width: 800

#. **그룹설정** 다음에 그룹설정을 선택한다.

#. **사용 가능한 이름 영역** 안에 사용할 이름을 등록한다. 등록된 이름은 스튜디오에서만 사용하고 학습자는 입력값을 보지 못한다.

#. **저장** 을 클릭한다.

콘텐츠 실험은 다른 요소들과 같이 제시되었다. 더 많은 정보가 필요하면  :ref:`Components that Contain Other Components`  에서 확인한다.

.. note:: 콘텐츠 실험은 복사할 수 없다. 

이제 콘텐츠 실험에서 그룹별 콘텐츠를 만들 수 있다.

=====================================================
콘텐츠 실험에 학습그룹별 콘텐츠 만들기
=====================================================

콘텐츠 실험 구성요소에서 그룹 설정을 선택한 후, **보기** 를 클릭한다.

자동 생성된 콘텐츠 실험은 선택한 그룹 설정에서 정의된 각 그룹이 포함된 컨테이너가 나타난다. 예를 들어, 그룹 A와 그룹 B로 정의한 그룹 설정을 선택하면 다음의 페이지가 나타난다.

.. image:: ../../../../shared/images/content_experiment_container.png
 :alt: An image of the content experiment page in Studio, with two groups.
 :width: 800

두 그룹을 위한 각각의 콘텐츠를 추가한다. 더 많은 정보를 보기위해  :ref:`Components that Contain Other Components`  를 살펴본다. 

예를 들어, 그룹 A에 HTML 요소와 동영상을 추가할 수 있다.

.. image:: ../../../../shared/images/a_b_test_child_expanded.png
 :alt: An image of an expanded content experiment component with an HTML and
     video component.
 :width: 800

.. note::
  실험에서 하나의 그룹에는 콘텐츠가 없는 것이 타당하며 유용하다. 예를 들어, 한 그룹은 동영상이 있고 다른 그룹은 어떤 콘텐츠도 없다면 학습자가 동영상으로 학습할 때의 효과를 분석해볼 수 있다.

========================================================
콘텐츠 실험에서 그룹 설정 변경하기
========================================================

콘텐츠 실험의 그룹 설정을 변경할 수 있다. 실험 그룹의 설정을 바꾸면, 새로운 그룹에 구성요소를 추가해야 한다. 이전 그룹에서 이용된 구성요소를 사용할 수 있고 또한 새로운 요소를 만들어 이용할 수 있다.

.. warning::
  학습자가 인지하고 있는 실험의 그룹설정을 변경하는 것은 실험 결과에 영향을 미칠 것이다. 그룹 설정을 변경하기 위하여.

#. 콘텐츠 실험이 있는 **학습활동** 페이지를 연다.

#. 콘텐츠 실험 구성요소에서 **수정** 을 클릭한다.

   .. image:: ../../../../shared/images/content_experiment_editor_group2.png
    :alt: An image of the content experiment editor in Studio, with a group
        configuration selected.
    :width: 800

#. 다른 그룹 설정을 선택한다.

#. **저장** 을 클릭한다.

#. 콘텐츠 실험에서 새로운 그룹에 구성요소를 추가해야 한다. 보기 를 클릭하여 콘텐츠 실험을 연다.

   새롭게 설정한 그룹은 비어 있다. 이전 설정에서 그룹에 추가했던 구성요소는 **비활성화 그룹** 으로 영역을 이동했다.

   .. image:: ../../../../shared/images/inactive_groups.png
    :alt: An image of a content experiment in Studio, with components in an
        inactive group.
    :width: 800

#. 새로운 그룹에 비활성화 그룹 에서 구성요소를 끌어 온다. 또한 새로운 그룹에는 새로운 요소를 만들 수 있다.

.. import OLX-content experiment doc that's shared in OLX guide.

.. include:: ../../../../shared/course_features/content_experiments/subsection_content_experiments_OLX.rst
