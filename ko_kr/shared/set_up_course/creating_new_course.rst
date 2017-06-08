.. _Creating a New Course:

###########################
신규 강좌 만들기
###########################

Studio를 활용해서 신규 강좌 만드는 방법을 알아봅시다.

.. contents::
  :local:
  :depth: 1

.. only:: Partners

   강좌 제작 생성 권한이 있을 때에만 테스트서버에서 강좌를 만들 수 있다. 
   자세한 사항은 테스트서버에서 Studio 사용하기를 참고하면 된다.
   K-MOOC 관리자만이 kmooc.kr에서 강좌를 만들 수 있다


또 하나의 강좌를 만드는 방법은 관리자의 승인 하에 기존 강좌를 재개강하는 것이다. 
이에 대한 자세한 사항은 :ref:`Rerun a Course` 를 참고하면 된다.

또한, XML에서 강좌를 편집하거나 백업할 때 :ref:`Export a Course` 와 :ref:`Import a Course` 를 할 수 있다. 

.. _Identifying the Course:

**************************
강좌 설정하기
**************************

강좌를 만들기 위해 다음과 같은 정보가 필요하다.

* **강좌 이름** : 강좌명이 만약 영어일 경우, 예를 들어 “Sets, Maps and Symmetry Groups”와 같이, 각 단어의 첫 알파벳을 대문자화(Capitalization)해야 한다.

* **기관** : 강좌 URL의 일부이므로, 공백이나 특수문자를 제외하고 영어 알파벳으로 입력해야 한다. 고급 설정에서 학습자가 볼 명칭을 새롭게 설정할 수 있다.

* **강좌 번호** : 이 강좌의 고유번호로 ‘KMOOC01’과 같이, 강좌 제공 기관의 영문 약자와 제공 기관의 몇 번째 강좌인지 ``영문과 숫자의`` 조합으로 입력한다.

  강좌별 운영번호에 강좌를 시작할 학기를 입력해야 한다. 예를 들어 2014SOND 혹은 T2_2014 형태로 입력하면 되고, 띄어쓰기나 특수문자를 사용할 수 없다.

  강좌별 운영번호에 입력하는 값은 개강일과 관련이 없으며, 자세한 사항은 :ref:`Scheduling
  Your Course`.
  를 참고하면 된다.

  기관, 강좌 번호 및 강좌별 운영번호는 URL을 만드는데 사용되며 길이 제한이 있기 때문에 65자 이내로 작성하여야 한다.


.. important:: 기관, 강좌 번호, 강좌별 운영번호는 강좌를 만든 뒤에는 변경할 수 없다

.. _Create a New Course:

*******************
신규 강좌 만들기
*******************

강좌를 만들기 위한 방법은 다음과 같다.

#. Studio에 로그인한다.

#. **새 강좌** 를 클릭한다.


#. :ref:`Identifying the Course` 를 입력하고 **만들기** 를 클릭한다.

   .. image:: ../../../shared/images/new_course_info.png
     :width: 600
     :alt: The course creation page in Studio, showing the fields required for
      creating a new course: Course Name, Organization, Course Number, and
      Course Run.

  강좌를 만들면 :ref:`Developing Your Course Outline` 페이지가 열린다. 아직 어떤 콘텐츠도 만들지 않았으므로, 페이지가 비어 있을 것이다.
  자세한 사항은 :ref:`Getting Started with Course Content Development` 를 참고하면 된다.


.. _Edit Your Course:

************************
강좌 편집하기
************************

  강좌를 만들면, 강좌가 Studio에서 자동으로 열리게 되며 교수자 및 강좌 운영팀은 편집을 시작할 수 있다. 
  다른 구성원을  :ref:`Add Course Team Members`  추가하거나 :ref:`Developing Your Course Outline`  
  :ref:`Scheduling Your Course` 을 설정할 수 있고 강좌 개요를 만들 수 있다.


  Studio의 **강좌** 대시보드에는 강좌 관리 권한을 가지고 있는 모든 강좌 목록이 나타난다.

.. image:: ../../../shared/images/open_course.png
  :width: 600
  :alt: Image of the course on the Studio dashboard.

  강좌를 편집하기 위해서 강좌명을 클릭하면 **강좌 개요** 페이지가 열린다.


.. include:: ../../../links/links.rst
