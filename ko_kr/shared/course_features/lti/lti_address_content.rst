.. _Determining Content Addresses:

#####################################
콘텐츠 주소 작성하기
#####################################

.. only:: Partners

  .. note:: 이 기능은 현재 개발 중이다. K-MOOC은 소수의 협력 기관과 함께 테스트서버에 이 기능을 사용하기 위해 테스트 중이다.

기존 강좌의 콘텐츠를 다른 시스템에 추가하기 위해 K-MOOC 학습 관리 시스템을 사용해 추가할 콘텐츠의 식별자를 찾고 이를 LTI URL 형식으로 바꿔야 한다.

.. contents::
   :local:
   :depth: 2

스프레드시트 등의 도구를 사용하는 것이 강좌 ID와 외부 학습 관리 시스템에 추가할 각 사용 ID를 정리하는데 도움이 된다.

.. _Find the Course ID:

********************
강좌 ID 찾기
********************

강좌의 식별자는 다음 중 하나의 형태를 갖는다.

* ``{key type}:{org}+{course}+{run}``, 예를 들어,  ``course-v1:edX+DemoX+2014``

* ``{org}/{course}/{run}``, 예를 들어, ``edX/DemoX/2014``

2014년 가을 이후에 시작된 강좌는 첫 형식의 ID를 갖고 이전의 강좌는 두번째 형식의 ID를 갖는다.

강좌 ID를 찾기 위해.

#. K-MOOC 학습 관리 시스템에서 강좌를 연다.

#. 브라우저에 나타난 URL에서 강좌 ID를 찾는다.

예를 들어 “Blended Learning with edX” 강좌의 홈 화면을 연다. 홈 화면의 URL은 ``https://courses.edx.org/courses/course-v1:edX+BlendedX+1T2015/info``  이다. 이 URL에서 강좌 ID가  ``course-v1:edX+BlendedX+1T2015`` 임을 알 수 있다.

다른 예로는 K-MOOC DemoX 강좌다. URL은 ``https://edge.edx.org/courses/edX/DemoX/2014/info`` 이고 강좌 ID는  ``edX/DemoX/2014``  가 된다.

동일한 강좌 ID는 강좌 내 모든 콘텐츠에 적용된다.

.. _Finding the Usage ID for Course Content:

****************************************
강좌 콘텐츠의 사용 ID 찾기
****************************************

특정 구성요소, 학습활동 혹은 소주제의 식별자는 다음과 같은 형태를 갖는다.

* ``{key type}:{org}+{course}+{run}+type@{type}+block@{display name}``, 예를 들어, ``block-v1:edX+DemoX+2014+type@sequential+block@basic_questions``

* ``i4x:;_;_{org};_{course};_{type};_{display name}``, 예를 들어,  ``i4x:;_;_edX;_DemoX;_sequential;_basic_questions``

2014년 가을 이후에 시작된 강좌는 첫 형식의 ID를 갖고 이전의 강좌는 두번째 형식의 ID를 갖는다.

다음 개념은 소주제, 학습활동 및 구성요소를 나타내는 사용 식별자에 쓰인다.

.. list-table::
   :widths: 45 45
   :header-rows: 1

   * - K-MOOC 스튜디오
     - 페이지 소스
   * - 소주제
     - 순차적
   * - 학습활동
     - 세로
   * - 구성요소
     - 문제, html 및 동영상

위의 사용 ID 예제는 “sequential”을 포함하므로 소주제라는 것을 알 수 있다.

몇가지 방법을 사용해 강좌 내 콘텐츠의 사용 ID를 찾을 수 있다.

K-MOOC 강좌의 학습활동이나 구성요소의 사용 ID를 찾기 위해 다음과 같은 방법을 사용할 수 있다.

* K-MOOC 학습 관리 시스템에서 오류 검출 정보를 조회한다.

* 페이지 소스를 조회한다.

* 강좌 구조를 조회한다

K-MOOC 강좌의 소주제 사용 ID를 찾기 위해 다음과 같은 방법을 사용할 수 있다.

* :ref:`View the page source<View the Page Source for the Usage ID>`.

* :ref:`View the course structure API<View the Course Structure API for the Usage ID>`.

.. note:: 사용 ID 검색 절차를 위해 운영팀이나 관리팀 권한이 필요하다.

.. _View Staff Debug Info for the Usage ID:

==========================================
사용 ID 오류 검출 정보 조회하기
==========================================

LMS에서 사용 ID를 검색하기 위해.

#. K-MOOC 학습 관리 시스템에서 강좌를 연다.

#. 강좌를 선택하고 구성요소나 학습활동 페이지로 간다.

#. 오류 검출 정보를 선택한다.

#. 구성요소의 사용 ID를 찾기 위해 위치를 파악한다.

   예를 들어, ``location = block-v1:edX+BlendedX+1T2015+type@html+block@2114b1b8fd7947d28fba53414459ff01``

#. 학습활동의 사용 ID를 찾기 위해 스크롤을 내린다.

   예를 들어, ``parent  block-v1:edX+BlendedX+1T2015+type@vertical+block@ae7d9c34c2f34f7aa793ed7b55543ae5``

비교적 최근에 만들어진 강좌의 경우 사용 ID 값이  ``block-v1`` 로 시작하고 오래된 강좌는  ``i4x://`` 로 시작한다. 스프레드시트를 사용해 위치 식별자를 정리하고 있다면 사용 ID 값을 선택하고 이를 스프레드시트에 붙여넣기하면 된다.

오류 검출 정보 뷰어를 닫기 위해서 뷰어 밖의 브라우저 페이지를 선택한다.

:ref:`Staff Debug Info`  에 자세한 안내가 나와있다.

.. _View the Page Source for the Usage ID:

==========================================
사용 ID의 페이지 소스 조회하기
==========================================

소주제, 학습활동 및 구성요소의 사용 ID를 찾기 위해 K-MOOC 강좌의 HTML 페이지를 조회한다.

소주제, 학습활동 및 구성요소의 사용 ID를 찾기 위해.

#. K-MOOC 학습 관리 시스템에서 강좌를 연다.

#. 강좌를 선택하고 LMS에 추가할 콘텐츠가 있는 페이지에 접속한다.

#. 페이지의 HTML 소스를 연다. 예를 들어 크롬 브라우저에선 페이지를 오른쪽 클릭하고 페이지 소스 보기를 클릭한다.

#. 브라우저의 기능 찾기를 사용해  ``data-usage-id`` 를 찾는다. 이 속성에 사용 ID가 있다.

#. 사용 ID 값을 확인해 강좌의 어느 부분을 나타내는지 알아낸다: 소주제 (sequential), 학습활동 (vertical) 혹은 특정 구성요소 (문제, HTML, 및 동영상)

   .. important:: 원하는 콘텐츠의 사용 ID가 첫 검색 결과에 나오지 않을 수도 있다. 반드시  ``data-usage-id`` 를 sequential, vertical, 문제, HTML 및 동영상에서 찾아 원하는 콘텐츠를 원하는 콘텐츠를 표시한다.


예를 들어 K-MOOC 데모 강좌의 소주제 링크를 원한다고 해보자. 강좌를 열어 문제에 들어가 페이지 소스 조회를 위해 마우스 오른쪽 클릭을 한다.   ``data-usage-id``  를 찾으면 첫 결과가  ``block-v1:edX+DemoX+Demo_Course+type@sequential+block@basic_questions``  로 나온다. 이 사용 ID 값이  ``sequential``  을 찾아 나온 소주제라는 것을 확인한다.

조금 더 복잡한 예제로 K-MOOC DemoX 강좌의 드래그 앤 드랍 문제의 사용 ID를 원한다고 해보자. 드래그 앤 드랍 문제는 강좌 첫 주의 첫 과제의 2번째 문제다. 페이지 소스 조회 후  ``data-usage-id``  를 찾으면 첫 결과가 소주제(sequential)로 검색된다. 다시 검색하면 첫 사용 ID와 살짝 다른 “vertical”이라는 값이 포함된 사용 ID를 볼 수 있는데 이는 학습활동이라는 것을 뜻한다. 세번째로 과제에서 첫 문제(problem)의 사용 ID를 얻을 수 있다.  다시 검색하면 과제의 두번째 문제의 사용 ID를 얻을 수 있다:  ``block-v1:edX+DemoX+Demo_Course+type@problem+block@d2e35c1d294b4ba0b3b1048615605d2a`` 

스프레드시트를 활용해 위치 식별자를 정리하고 있다면 따옴표 안의 사용 ID 값을 선택하거나 ISO 코드를 선택해 스프레드시트에 붙여넣기 할 수 있다.

.. _View the Course Structure API for the Usage ID:

===============================================
사용 ID의 강좌 구조 API 조회하기
===============================================

K-MOOC 강좌 구조 API는 JSON 형식의 모든 항목의 사용 식별자를 포함한 강좌에 대한 정보를 담고 있다.

강좌 API를 조회하기 위해 다음 형식의 URL을 검색한다.

  ``https://{host}/api/course_structure/v0/course_structures/{course_id}``

강좌 구조 API 조회를 위해 반드시 운영팀이나 관리팀 권한이 있어야 한다.

강좌 구조 API에서 사용 ID를 찾기 위해.

#. 브라우저에서 강좌 구조 API의 URL을 입력한다.

   예를 들어 K-MOOC 데모 강좌의 강좌 구조 API를 위해 다음 URL을 입력한다.

   ``https://edge.edx.org/api/course_structure/v0/course_structures/course-v1:edX+DemoX+Demo_Course``

#. 엔터를 누른다. 브라우저에 강좌 구조 API가 나타난다.

#. ``HTTP 200 OK`` 메시지가 나오는 것을 확인한다.

   다른 HTTP 반응 값을 받았을 경우 강좌 운영팀이나 관리팀 권한이 있는지 확인하고 올바른 URL을 입력했는지 확인한다.

API는 강좌의 root 사용 ID를 보여주며 강좌의 blocks로 이어진다. 각 block은 강좌의 하나의 항목에 대한 정보를 보여주며 sequential, vertical, 문제, HTML 및 동영상 식별자를 보여준다. 각 block은 각 항목의 display_name을 포함하고 이를 통해 특정 소주제, 학습활동 및 구성요소를 찾을 수 있다.

예를 들어 다음 block은 하나의 (children 값으로 표시된)동영상 구성요소를 포함하는 학습활동(vertical)을 나타낸다.

.. code-block:: json

  {
      "block-v1:edX+231_LTI+Fall_2015+type@vertical+block@7b3606b362c74222ba2d0c06e433df08": {
          "id": "block-v1:edX+231_LTI+Fall_2015+type@vertical+block@7b3606b362c74222ba2d0c06e433df08",
          "type": "vertical",
          "parent": null,
          "display_name": "1st Video",
          "graded": false,
          "format": null,
          "children": [
              "block-v1:edX+231_LTI+Fall_2015+type@video+block@fe187ddccab84398aa051f6937a213a7"
          ]
      },

이 학습활동의 사용 ID는 “id”의 값이다.

  ``block-v1:edX+231_LTI+Fall_2015+type@vertical+block@7b3606b362c74222ba2d0c06e433df08``

비교적 최근에 만들어진 강좌의 경우 사용 ID 값이 ``block-v1`` 로 시작하고 오래된 강좌는 ``i4x://`` 로 시작한다.

스프레드시트를 사용해 위치 식별자를 정리하고 있다면 따옴표 안의 사용 ID 값을 선택하고 이를 스프레드시트에 붙여넣기하면 된다.

************************
LTI URL 만들기 
************************

LMS에 추가할 K-MOOC 콘텐츠를 나타내기 위해 다음 형식의 URL을 제공해야 한다.

  ``https://{host}/lti_provider/courses/{course_id}/{usage_id}``

LTI URL을 construct(구성)하기 위해 강좌 ID와 특정 콘텐츠 ID를 추가한다.

소주제 LTI URL의 경우 다음과 같이 “sequential”을 포함한다.

  ``https://edx-lti.org/lti_provider/courses/course-v1:edX+DemoX+2014/block-v1:edX+DemoX+2014+type@sequential+block@basic_questions``

  ``https://edx-lti.org/lti_provider/courses/edX/DemoX/2014/i4x:;_;_edX;_DemoX;_sequential;_graded_simulations``

학습활동 LTI URL의 경우 다음과 같이 “vertical”을 포함한다.

  ``https://edx-lti.org/lti_provider/courses/course-v1:edX+DemoX+Demo_Course/block-v1:edX+DemoX+Demo_Course+type@vertical+block@vertical_3888db0bc286``

  ``https://edx-lti.org/lti_provider/courses/edX/DemoX/2014/i4x:;_;_edX;_DemoX;_vertical;_d6cee45205a449369d7ef8f159b22bdf``

HTML 구성요소 LTI URL의 경우 다음과 같이 “html+block”이나 “html”을 포함한다.

  ``https://edx-lti.org/lti_provider/courses/course-v1:edX+DemoX+Demo_Course/block-v1:edX+DemoX+Demo_Course+type@html+block@f9f3a25e7bab46e583fd1fbbd7a2f6a0``

  ``https://edx-lti.org/lti_provider/courses/edX/DemoX/2014/i4x:;_;_edX;_DemoX;_html;_2b94658d2eee4d85ae13f83bc24cfca9``

