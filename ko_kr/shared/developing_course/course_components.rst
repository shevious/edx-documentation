.. _Developing Course Components:

###################################
구성요소
###################################

학습활동을 만들기 전에, 우선 다음 사항을 이해해야 한다.

.. contents::
  :local:
  :depth: 1

구성요소의 종류에 대한 더 자세한 안내는 아래 링크에 있다.

* :ref:`Course Components Index`
* :ref:`Exercises and Tools Index`

.. _What is a Component:

********************
구성요소란?
********************

구성요소는 학습활동의 부분으로, 실제 강좌 콘텐츠라고 볼 수 있다. 1개의 학습활동은 1개 이상의 구성요소를 포함할 수 있다.

기본적으로, Studio에는 다음 구성요소가 있다.

* **게시판** 은 학습자들이 토의를 할 수 있는 구성요소다. 학습자는 여기서 주제에 관한 아이디어를 다른 학습자와 공유할 수 있다.
* **HTML** 은 텍스트, 이미지 등 학습 도구를 강좌에 추가할 수 있는 구성요소다. HTML에 콘텐츠를 입력하려면 HTML을 사용해야 한다.
* **문제** 는 다양한 유형의 연습과 문제를 강좌에 추가할 수 있는 구성요소다. 유형은 선다형 문제부터 회로 문제까지 다양하게 있다.
* **동영상** 은 학습에 유용한 동영상을 추가할 수 있는 구성요소다.

.. _Add a Component:

********************
구성요소 추가하기
********************

강좌개요에서 **+새로운 학습활동** 을 클릭한 후, 바뀐 페이지의 신규 구성요소 추가 에서 원하는 구성요소 유형을 클릭한다.

.. image:: ../../../shared/images/AddNewComponent.png
  :alt: The controls for the default component types you can add: Discussion,
      HTML, Problem, and Video.

각 구성요소에 대한 상세한 도움말을 다음에서 확인할 수 있다.

- :ref:`Working with Discussion Components`
- :ref:`Working with HTML Components`
- :ref:`Working with Problem Components`
- :ref:`Working with Video Components`

구성요소를 추가한 후, :ref:`Publish a Unit` 작업이 이루어져야 학습자가 이를 볼 수 있다.

.. _Edit a Component:

********************
구성요소 편집하기
********************

구성요소를 편집하려면, **편집** 을 클릭한다.

.. image:: ../../../shared/images/unit-edit.png
  :alt: A component with the Edit icon indicated in the toolbar.
  :width: 400

편집하려는 구성요소에 나오는 안내에 따라, 편집을 시작하면 된다.

구성요소를 편집한 후, :ref:`Publish a Unit` 를 하지 않으면 학습자가 변경사항을 볼 수 없다는 것에 유의한다.

=====================================
구성요소 메뉴명 설정하기
=====================================

메뉴명은 LMS의 구성요소 상단에 제목 형식으로 나타나며 Insights에서 구성요소에 대해 알려주는 역할을 한다.

다음 그림은 Studio, LMS와 Insights에서 나타나는 메뉴명을 보여준다.

.. image:: ../../../shared/images/display_names_problem.png
 :alt: The identifying display name for a problem in Studio, the LMS, and
     Insights.
 :width: 800

메뉴명은 구성요소에 대해 쉽게 알 수 있도록 만드는 것이 좋다.

구성요소 메뉴명을 설정하려면.

#. 구성요소 영역에서 편집을 클릭한다.

   * 게시판 혹은 동영상 구성요소에선 메뉴명을 포함한 설정 목록이 나온다.

   * HTML이나 문제 구성요소에선 편집창이 나오고 설정을 클릭해 메뉴명을 포함한 설정 목록을 확인할 수 있다.

#. 메뉴명에 이름을 입력한다.

  .. image:: ../../../shared/images/display-name.png
   :alt: The settings dialog box for a problem component.
   :width: 500

#. 저장을 클릭한다.

구성요소의 유형별로 설정 대화상자가 다르지만, 모든 대화상자에 메뉴명 영역이 있다.

.. _Duplicate a Component:

**********************
구성요소 복사하기
**********************

구성요소를 복사하면, 구성요소 사본이 첫 번째 구성요소 바로 아래에 추가된다. 그러면 사본을 수정할 수 있다. 대부분의 경우, 구성요소를 복사하여 사본을 편집하는 것이 신규 구성요소를 만드는 것 보다 빠르다.

구성요소를 복사하려면, 구성요소 영역의 오른쪽 상단에서 복사 아이콘을 클릭하면 된다.

.. image:: ../../../shared/images/unit-dup.png
  :alt: Image of a unit with Duplicate icon circled.

그 후 편집중인 구성요소의 안내를 따라 진행한다.

구성요소를 복사해서 만든 구성요소는  :ref:`Publish a Unit` 후에 학습자에게 공개될 수 있다.

.. note::  콘텐츠 실험은 복사할 수 없다.

.. _Delete a Component:

**********************
구성요소 삭제하기
**********************

.. caution::
 구성요소를 삭제할 것인지 다시 확인해보길 권한다. 삭제 후에는 되돌릴 수 없기 때문이다.

구성요소를 삭제하려면.

#. 구성요소 영역의 오른쪽 상단에서 삭제 아이콘을 클릭하면 된다.

.. image:: ../../../shared/images/unit-delete.png
  :alt: Image of a unit with Delete icon circled.

2. 삭제 여부를 확인하는 대화상자가 뜨면, **네, 구성요소를 삭제합니다.** 를 클릭한다..

구성요소를 삭제하더라도,  :ref:`Publish a Unit`  하기 전에는 학습자가 볼 수 있다는 것에 유의한다.

.. _Components that Contain Other Components:

******************************************
다른 구성요소를 포함하는 구성요소
******************************************

특별한 경우, 구성요소 속에 다른 구성요소를 넣을 수 있다. 예를 들어 콘텐츠 실험 등을 포함할 경우로, 구성요소 속에 다른 구성요소를 만들어야 한다. 이에 관해선 :ref:`Creating Content Experiments` 에 더 자세한 안내가 있다.

이렇게 다른 구성요소를 포함하는 구성요소를 상위 라고 부르고, 포함된 구성요소를 하위 라고 부른다.

학습활동 페이지에서, 상위 구성요소가 보기 링크와 함께 나타난다:

.. image:: ../../../shared/images/component_container.png
 :alt: Image of a unit page with a parent component.


==================================================
상위 구성요소 편집하기
==================================================

상위 구성요소는 콘텐츠를 직접 포함하지 않는다. 하위 구성요소에 HTML, 동영상, 문제 등의 콘텐츠가 포함된다.

상위 구성요소는 메뉴명을 가진다. 학습활동이 아직 게시되지 않은 상태일 때, 상위 구성요소의 설정 을 클릭하면 메뉴명을 바꿀 수 있다.

.. note::
  콘텐츠 실험 등 특수한 유형의 상위 구성요소는 편집 방식이 조금 다를 수 있다.


======================================
하위 구성요소 편집하기
======================================

상위 구성요소의 보기 를 클릭하면, 모든 하위 구성요소를 볼 수 있다. 다음 예시에서, 하위 구성요소 A가 HTML과 동영상을 포함하고 있다.

.. image:: ../../../shared/images/child-components-a.png
 :alt: Image of an expanded child component.

하위 구성요소 명 옆의 화살표를 클릭하면 구성요소의 콘텐츠를 접거나 펼 수 있다.

.. image:: ../../../shared/images/child-components.png
 :alt: Image of a child component page.

구성요소와 관련된 작업은 다음 링크와 같다.

* `Edit a Component`_
* `Duplicate a Component`_
* `Delete a Component`_

======================================
하위 구성요소 추가하기
======================================

구성요소가 초안이라면, 상위 구성요소에 하위 구성요소를 추가할 수 있다.

하위 구성요소를 추가하려면, 상위 구성요소를 열어 펼친다. 이후 상위 구성요소 안에서, 신규 구성요소 추가 아래에 있는, 원하는 구성요소 유형을 선택한다.

.. image:: ../../../shared/images/AddNewComponent.png
  :alt: Image of adding a new component.

구성요소와 관련해서 더 자세한 도움말은 아래에 있다.

- :ref:`Working with Discussion Components`
- :ref:`Working with HTML Components`
- :ref:`Working with Problem Components`
- :ref:`Working with Video Components`


======================================
XML
======================================

XML에서 상위와 하위 구성요소를 만든 후, 그것을 Studio로 가져와서 요소들의 구성이 원하는 대로 되어 있는지 확인한다.

XML 파일 작업 및 용어에 대한 안내는  `EdX Open Learning XML Guide <https://edx.readthedocs.org/projects/edx-open-learning-xml/en/latest/>`_  에 있다.

다음 예시는 XML로 학습활동과 구성요소를 만들고 가져왔을 때, Studio에서 어떻게 보이는지를 나타낸다.

학습활동의 XML은 아래와 같은데.

.. code-block:: xml

    <vertical display_name="Unit 1">
        <html url_name="6a5cf0ea41a54b209e0815147896d1b2"/>
        <vertical url_name="131a499ddaa3474194c1aa2eced34455"/>
    </vertical>

위의  ``<vertical url_name="131a499ddaa3474194c1aa2eced34455"/>`` 는 하위 구성요소를 포함한 상위 구성요소를 참조한다.

.. code-block:: xml

    <vertical display_name="Parent Component">
        <vertical url_name="2758bbc495dd40d59050da15b40bd9a5"/>
        <vertical url_name="c5c8b27c2c5546e784432f3b2b6cf2ea"/>
    </vertical>

상위 구성요소에 의해 참조된 verticals는 강좌의 실제 콘텐츠를 포함한 하위 구성요소를 의미한다.

.. code-block:: xml

    <vertical display_name="Child Component A">
        <html url_name="4471618afafb45bfb86cbe511973e225"/>
        <video url_name="fbd800d0bdbd4cb69ac70c47c9f699e1"/>
    </vertical>

.. code-block:: xml

    <vertical display_name="Child Component B">
        <html url_name="dd6ef295fda74a639842e1a49c66b2c7"/>
        <problem url_name="b40ecbe4ed1b4280ae93e2a158edae6f"/>
    </vertical>

이론적으로 강좌에서 사용할 수 있는 구성요소의 중첩(nesting)에는 제한이 없다.


======================================
중첩된 구성요소에 대한 학습자 보기
======================================

학습자를 위해, 모든 상위와 하위 구성요소는 학습활동 페이지에 나타난다. 다음 예는 위에서 설명한 학습활동의 학습자 보기 상태를 보여준다.

.. image:: ../../../shared/images/nested_components_student_view.png
 :alt: Image of the learner's view of nested components.

.. note::
 중첩된 구성요소가 적용된 화면은 상위 학습활동이 적용된 화면을 따른다. 상위 학습활동은 중첩된 구성요소를 보기 위해 학습자 들에게 공개되어야 한다. 자세히 보기 위해,  :ref:`Unit States and Visibility to Students` 를 살펴 본다.


*******************************
하위 구성요소의 재 조직화
*******************************

다른 객체를 사용하는 드래그 앤 드롭과정(끌어놓기 과정)을 통해 하위 구성요소를 재조직할 수 있다. 이동용 마우스 포인트(화살표 4개)로 바뀔때까지 화면의 오른쪽 하단으로 요소를 움직인다. 그리고 원하는 지점으로 요소를 클릭해서 드래그 한다.

또한, 중첩되어 있는 요소들이 많을 때 두 상위요소가 확장된다면, 하위 구성요소를 다른 상위 구성요소로 드래그 할 수 있다. 예를 들어, 하위 구성요소 A에서 동영상 구성요소를 선택하고 하위 구성요소 B로 드래그 할 수 있다. 동영상 구성요소를 선택하여 하위 구성요소 B로 이동한 것처럼, 움직이는 구성요소는 새로운 지점에서 점선의 개요가 나타날 때 마우스 버튼을 놓는다.

.. image:: ../../../shared/images/drag_child_component.png
 :alt: Image of dragging a child component to a new location

하위 구성요소를 상위 구성요소의 바깥으로 드래그해서 빼내어, 상위 구성요소의 수준으로 이동시킬 수 있다.

.. note::
  콘텐츠 실험을 위해, 하위 구성요소를 테스트(실험) 집단 밖으로 드래그 할 수 없다.

.. include:: ../../../links/links.rst
