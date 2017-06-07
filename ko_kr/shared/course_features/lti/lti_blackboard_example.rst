.. _edX as an LTI Provider to Blackboard:

###############################################
예제: K-MOOC을 Blackboard의 LTI 제공자로 활용하기
###############################################

.. only:: Partners

  .. note:: 이 기능은 현재 개발중이다. K-MOOC은 소수의 협력 기관과 함께 테스트서버에 이 기능을 사용하기 위해 테스트 중이다.

K-MOOC 강좌 콘텐츠를 Blackboard LMS에서 사용하기 위해 강좌에 새 프로그램과 외부 도구 모듈을 추가해야 한다.

.. note:: 이 예제는 외부 도구를 사용한다. 이 도구는 언제든지 변동이 있을 수 있기 때문에 이 장의 설명은 정확하지 않을 수 있다.

#. Blackboard에서 강좌를 선택한다.

#. 강좌 제어 패널에서 사용자 정의를 선택한다. 가용 도구에서 LTI 도구가 활성화 되었음을 확인한다.

#. Content Area 페이지를 열고 콘텐츠 만들기 메뉴에서 웹 링크를 선택한다.

   .. image:: ../../../../shared/images/lti_blackboard_contentarea.png
     :alt: An image of the Blackboard navigation choices from Content Area to
         Build Content to Web Link.

#. 웹 링크 생성 페이지에서 추가할 K-MOOC 콘텐츠의 이름과 URL을 입력한다.

   URL이 K-MOOC 강좌 콘텐츠를 위한 LTI URL이 된다. 예를 들어  ``https://edx-lti.org/lti_provider/courses/course-v1:edX+DemoX+2014/block-1:edX+DemoX+Demo_Course+type@problem+block@d2e35c1d294b4ba0b3b1048615605d2a``.

   .. image:: ../../../../shared/images/lti_blackboard_create_link.png
     :alt: The Blackboard Create Web Link page with example name and URL
         values.

   :ref:`Determining Content Addresses`  에 자세한 안내가 나와있다.

#. 콘텐츠가 원하는 대로 나오는지 확인한다.

   .. image:: ../../../../shared/images/lti_blackboard_example.png
     :alt: An edX drag and drop problem shown as part of a course running on a
      Blackboard system.


