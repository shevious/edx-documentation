.. _Getting Started with Course Content Development:

###############################################
강좌 콘텐츠
###############################################

:ref:`Setting up your Course Index` 에서의 작업이 모두 끝났다면, 이제 강좌 콘텐츠를 개발할 차례다.

이 장은 강좌 콘텐츠 개발 단계의 개요이다. 상세 내용은 하단 링크를 참조한다.

.. contents::
  :local:
  :depth: 1

.. _Understanding Course Building Blocks:

************************************************
강좌의 기본 구성요소 이해하기
************************************************

시작하기 전에, 강좌를 이루는 기본 요소를 이해하도록 하자.

* :ref:`Developing Your Course Outline` 에서 강좌의 콘텐츠 구성 등 전체 구성을 한 눈에 볼 수 있다.
* :ref:`Developing Course Sections` 는 강좌에서 가장 상위 범주에 해당한다. 순차적으로 공개되는 주제를 보면 개강일 이후 강좌가 어떻게 진행되는지 그 흐름을 알 수도 있고, 강좌가 어떻게 구성되어 있는지를 한 눈에 볼 수 있기도 하다. 각 주제는 1개 이상의 소주제를 가진다.
* :ref:`Developing Course Subsections` 는 주제의 하위 개념으로, 주제에서 1개 이상의 학습활동이 포함된 소주제로 나뉘게 된다. 소주제를 살펴보면 그 강좌에서 무엇을 중점으로 두는지 이해할 수 있게 된다.
* :ref:`Developing Course Units` 은 소주제의 일부로서, 학습자가 소주제를 클릭하면 한 번에 하나씩 그 내용을 볼 수 있다.
* :ref:`Developing Course Components` 는 학습활동의 부분으로, 실제 강좌 콘텐츠라고 볼 수 있다. 1개의 학습활동은 1개 이상의 구성요소를 포함할 수 있다.

.. _Creating New Course Content:

****************************************
신규 콘텐츠 만들기
****************************************

강좌를 이루는 기본 요소를 이해했다면, 이제 강좌 콘텐츠를 Studio에서 개발할 차례이다.

먼저 :ref:`Developing Your Course Outline` 에서  :ref:`Create a Section`, :ref:`Create a Subsection`,  :ref:`Create a Unit` 의 순서로 만들 수 있다.

성적에 반영되는 소주제 설정도 할 수 있다. 세부사항은 :ref:`Set the Assignment Type and Due Date for a Subsection` 을 참고한다.

:ref:`Add a Component` 페이지에서 구성요소를 추가할 수도 있다.

이 외에도,  :ref:`Controlling Content Visibility` 에 따라 학습활동 게시와 공개일 설정을 통해 콘텐츠를 학습자에게 보이거나 감추는 것을 설정할 수 있다.

이러한 콘텐츠 제작 과정을 아래 도표와 같이 요약할 수 있다:

.. image:: ../../../shared/images/workflow-create-content.png
 :alt: Diagram of the content creation process

콘텐츠 개발 과정에서 모바일 환경을 포함한 모든 환경에서 콘텐츠를 테스트해보는 것이 원활한 강좌 운영에 도움이 될 것이다. 자세한 사항은 :ref:`Designing For a Mobile Experience` 을 참고하면 된다.

.. note:: 모바일 환경에서는 강좌의 업데이트가 다소 느릴수 있다. 특히 새로운 강좌 내용은 안드로이드 환경에서 최대 1시간 뒤에 업데이트 될 수도 있다.


.. _Making Course Content Visible to Students:

*****************************************
콘텐츠 공개하기
*****************************************

콘텐츠를 만들 때, 이를 학습자에게 공개할 것인지 여부와 공개 시점을 설정할 수 있다. 아래 항목들에 관해 공개 설정이 가능하다:

* :ref:`Set Start and End Dates`
* :ref:`Set a Section Release Date` 와 :ref:`Set a Subsection Release Date`
* :ref:`configuring_prerequisite_content`
* :ref:`Hide a Unit from Students`
* :ref:`Hide a Unit from Students` 
* :ref:`Content Groups`

공개 설정에 대한 자세한 안내는 :ref:`Controlling Content Visibility` 을 참고한다.

.. _Making Course Content Searchable:

***********************************
콘텐츠 검색 기능 활성화하기
***********************************

학습자는 :ref:`Working with HTML Components` 의 강좌 텍스트와 동영상 자막을 강좌 내용 탭의 왼쪽 상단의 검색 박스에서 검색할 수 있다.

강좌 운영팀이 :ref:`Publish a Unit` 하면 Studio가 자동으로 콘텐츠에 색인 작업을 수행하게 된다.

필요한 경우, 본인이 직접 색인 작업을 수행할 수도 있다. 강좌 개요 페이지의 오른쪽 상단에서 **재인덱스** 를 클릭한다.

.. _Revising Content:

****************************
콘텐츠 변경하기
****************************

언제든지 강좌 콘텐츠를 변경할 수 있다.

* 강좌 개요에서 주제, 소주제, 학습활동 재구성 하면, 변경된 콘텐츠를 학습자가 곧바로 볼 수 있다.

* :ref:`Edit a Unit`  또는  :ref:`Add a Component` 할 때, 변경된 콘텐츠를 학습자가 보게 하려면 반드시  :ref:`Publish a Unit` 해야 한다.

다음은 강좌 콘텐츠 변경에 따라 학습자 공개 상태를 요약해서 보여주는 도표이다:

.. image:: ../../../shared/images/workflow-revise-content.png
 :alt: Diagram of the content creation process

콘텐츠 개발 과정에서 모바일 환경을 포함한 모든 환경에서 콘텐츠를 테스트해보는 것이 원활한 강좌 운영에 도움이 될 것이다. 자세한 사항은  :ref:`Designing For a Mobile Experience` 을 참고하면 된다.

.. note:: 모바일 환경에서는 강좌의 업데이트가 다소 느릴수 있다. 특히 새로운 강좌 내용은 안드로이드 환경에서 최대 1시간 뒤에 업데이트 될 수도 있다.
