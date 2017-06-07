.. _edX as an LTI Provider to Canvas:

##########################################
예제: K-MOOC을 Canvas의 LTI 제공자로 활용하기
##########################################

.. only:: Partners

  .. note:: 이 기능은 현재 개발중이다. K-MOOC은 소수의 협력 기관과 함께 테스트서버에 이 기능을 사용하기 위해 테스트 중이다.

K-MOOC 강좌 콘텐츠를 Canvas 학습 관리 시스템에서 사용하기 위해 강좌에 새 프로그램과 외부 도구 모듈을 추가해야 한다.

.. note:: 이 예제는 외부 도구를 사용한다. 이 도구는 언제든지 변동이 있을 수 있기 때문에 이 장의 설명은 정확하지 않을 수 있다.

#. Canvas에서 강좌를 선택한다. 설정에서 새 프로그램 추가를 선택한다.

   .. image:: ../../../../shared/images/lti_edit_external_app_Canvas.png
     :alt: The Canvas page where you enter identifying values for the edX host
         site as a LTI tool provider.

#. 모듈에서 외부 도구를 추가한다. URL이 K-MOOC 강좌 콘텐츠를 위한 LTI URL이 된다. 예를 들어 
   ``https://edx-lti.org/lti_provider/courses/course-v1:edX+DemoX+2014/block-v1:edX+DemoX+Demo_Course+type@problem+block@d2e35c1d294b4ba0b3b1048615605d2a``.

   .. image:: ../../../../shared/images/lti_edit_problem_Canvas.png
     :alt: The Canvas page where you add an external tool and supply the LTI
         URL.

   :ref:`Determining Content Addresses` 에 자세한 안내가 나와있다.

#. 콘텐츠가 원하는 대로 나오는지 확인한다.

   .. image:: ../../../../shared/images/lti_canvas_example2.png
     :alt: An edX drag and drop problem shown as part of a course running on a
      Canvas system.
