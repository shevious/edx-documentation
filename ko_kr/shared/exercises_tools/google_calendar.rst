.. _Google Calendar Tool:

#####################
구글 캘린더 도구
#####################

.. note:: K-MOOC은 이 도구에 전체 지원을 제공한다.

본 장에서는 강좌에 구글 캘린더를 포함하는 방법을 설명한다.

.. contents::
  :local:
  :depth: 2

외부 사이트의 콘텐츠를 강좌에 사용하기 전에 반드시 장애가 있는 학습자에게 제공할 수 있는지 확인해야 한다. 자세한 사항은 :ref:`Accessibility Best Practices for Course Content Development` 를 참고하면 된다.

또한 강좌에서 문서, 스프레드시트, 이미지 등과 같은 구글 드라이브 파일을 사용할 수 있다. 더 자세한 내용은 :ref:`Google Drive Files Tool` 를 참고하도록 한다.

.. note:: 구글은 일부 지역 및 국가에서 사용이 불가능하다. 만약 특정 학습자의 지역에서 구글을 사용할 수 없다면 구글 드라이브 파일이나 구글 캘린더 자리에 “이미지 사용 불가” 메시지가 나올 수도 있다. K-MOOC은 이런 지역의 학습자를 위해 대체 방안을 마련할 것을 강력하게 권고한다.


*********
개관
*********

학습자가 강좌내용에서 볼 수 있도록 강좌에 구글 캘린더를 포함시킬 수 있다. 퀴즈 날짜, 근무 시간, 또는 학습자에게 관심이 될만한 다른 일정들을 공유하기 위해 구글 캘린더를 사용할 수 있다. 예를 들면:

.. image:: ../../../shared/images/google-calendar.png
  :alt: A Google Calendar in the course body.

*******************************************
구글 캘린더 활용하기
*******************************************

강좌에 구글 캘린더를 포함하려면 세 단계가 있다.

.. contents::
   :local:
   :depth: 1

.. _Enable the Google Calendars Tool:

================================================
강좌에서 구글 캘린더 활용하기
================================================

스튜디오 또는 OLX를 사용하여 강좌에서 구글 캘린더를 사용할 수 있다.

Studio에서 구글 캘린더를 설정하기 위해 ``"google-calendar"`` 키를 **고급 설정** 의 **고급 모듈 목록** 에 추가해야 한다. (키 값은 “ “ 사이에 입력해야 한다) 자세한 사항은 :ref:`Enable Additional Exercises and Tools` 를 참고하면 된다.

또는 OLX를 사용해 구글 캘린더 도구를 설정할 수 있다.

.. _Enable Google Calendars in OLX:

OLX에서 구글 캘린더 활용하기
**********************************************

강좌에서 구글 캘린더를 사용하려면, 강좌 구조를 정의 하는 XML 파일을 편집할 수 있다. 당신은  ``강좌`` element's ``고급 모듈`` 속성을 찾아서, 그것에 문자열 ``google-calendar`` 를 추가한다.

예를 들어, 다음 XML 코드는 강좌에서 구글 캘린더를 사용할 수 있게 만든다. 그것은 또한 구글 드라이브 파일을 활용할 수 있게 만든다.

.. code-block:: xml

  <course advanced_modules="[&quot;google-document&quot;,
      &quot;google-calendar&quot;]" display_name="Sample Course"
      start="2014-01-01T00:00:00Z">
      ...
  </course>

자세한 사항은  :ref:`olx:OLX Course Building Blocks` 을 참고하면 된다.

.. _Make the Google Calendar Public and Obtain Its ID:

===================================================
구글 캘린더 공개 및 ID 얻기
===================================================

강좌에 구글 캘린더를 추가할 수 있기 전에, 먼저 구글 캘린더를 공개하고 ID를 얻어야 한다.

.. important::
 여기에서 설명하는 작업은 제3자 소프트웨어 혹은 타사 소프트웨어를 사용한다. 소프트웨어가 소유자에 의해 변경될 수 있기 때문에 여기에 제공된 단계는 참고를 위한 것이며, 정확한 절차는 아니다.

구글 캘린더 공개하기
**********************************************

#. 구글 캘린더를 연다.
#. **설정 메뉴** 에서 **설정** 을 선택한다.
#. **캘린더** 탭을 선택한다.

   **캘린더** 탭에 여러 개의 캘린더가 있을 수 있다. 강좌 내용에서 공유하려는 캘린더를 찾는다.

#. 공유 열에 있는, 캘린더를 공유하기 위한 열에서, **설정 편집하기** 를 선택한다.
#. 이 캘린더 공유하기 탭을 클릭한 **이 캘린더 공개하기** 를 선택한다.

  .. image:: ../../../shared/images/google-calendar-settings.png
   :alt: Google Calendar settings.

#. **저장** 을 선택한다.

   캘린더 설정 페이지를 닫고, 캘린더 탭으로 돌아간다. 다음에서  :ref:`obtaining the Google Calendar's ID<Obtain the Google Calendar ID>` 에 대해 계속 알아보도록 한다.

.. _Obtain the Google Calendar ID:

구글 캘린더 ID 얻기
**********************************************

#. **캘린더** 탭에서 캘린더의 이름을 클릭한다.
#. **캘린더 세부 정보** 탭을 선택한다.
#. 캘린더 주소 라벨 옆의 3가지 색의 **XML** , **ICAL** , **HTML** 버튼의 오른쪽을 보게 된다. 괄호에서 캘린더 ID가 보일 것이다.

   .. image:: ../../../shared/images/google-calendar-address.png
     :width: 600
     :alt: Image of Calendar Address label with the calendar ID to the right.

   캘린더 ID는 다음 텍스트와 유사하다.

   ``abcdefghijklmnop1234567890@group.calendar.google.com``

   캘린더 ID를 선택 및 복사한다. 강좌에서 구글 캘린더 구성 요소를 설정하기 위해 이 값을 사용한다.

.. _Add a Google Calendar in the Course Body:

========================================
강좌 내용에 구글 캘린더 추가하기
========================================

강좌내용에 구글 캘린더를 추가 하려면, 스튜디오에서 고급 구성 요소를 만들거나 OLX에서 구글 캘린더 XBlock을 만든다.

.. _Add a Google Calendar Component in edX Studio:

스튜디오에서 구글 캘린더 구성 요소 추가하기
**********************************************

구글 캘린더 구성요소를 추가하기 전에, 강좌에서 구글 캘린더를 활용할 수 있다. :ref:`enable Google Calendars<Enable the Google Calendars Tool>` 를 확인한다.

구글 캘린더 구성 요소를 추가 하려면.

#. **강좌 개요** 페이지에서, 구글 캘린더 구성요소를 추가하고 싶은 학습활동을 연다.

#. **신규 구성요소 추가** 에서 **고급** 을 클릭한 후, **구글 캘린더** 를 선택한다.

   **새 구성 요소** 는 포함된 기본 구글 캘린더와 함께 학습활동에 추가된다.

   .. image:: ../../../shared/images/google-calendar-studio.png
    :width: 600
    :alt: The Google Calendar component in a unit page.

#. **편집** 을 선택한다.

   .. image:: ../../../shared/images/google-calendar-edit.png
    :width: 600
    :alt: The Google Calendar editor.

#. **표시 이름** 입력 필드에는 구성 요소에 대한 이름을 입력한다.

#. **공개 캘린더 ID** 입력 필드에는 :ref:`Obtain the Google Calendar ID` 작업에서 복사한 캘린더 ID를 붙여 넣는다.

#. **기본 보기** 입력 필드에 대하여, **월** , **주** 또는 **안건** 을 선택한다. 

   이것은 학습자가 볼 캘린더에 대한 초기 보기 혹은 (기본화면)이다. 각 학습자는 그 보기를 변경할 수 있다.

#. **저장** 을 선택한다.

학습자에게 구글 캘린더를 포함한 학습활동이 어떻게 보이는지  :ref:`Preview Course Content` 할 수 있다.


.. _Add a Google Calendar XBlock in OLX:

Add a Google Calendar XBlock in OLX
**********************************************

OLX에 구글 캘린더 XBlock를 추가 하려면,  ``google-calendar`` 요소를 만든다.  ``vertical`` 요소에 이 요소를 포함시킬 수 있거나 또는 ``vertical`` 요소 내에서 참고하는 해당 파일에 이 요소를 포함시킬 수 있다. 더 자세한 내용은 :ref:`olx:OLX Course Building Blocks` 를 참고하도록 한다.

예를 들면.

.. code-block:: xml

  <google-calendar url_name="4115e717366045eaae7764b2e1f25e4c"
    calendar_id="abcdefghijklmnop1234567890@group.calendar.google.com"
    default_view="1" display_name="Class Schedule"/>

 ``calendar_id`` 속성의 값은  :ref:`Obtain the Google Calendar ID` 작업에서 복사한 캘린더 ID이다.

.. note::
  K-MOOC 학습 관리 시스템은 구글 캘린더에 대한 height 및 width 값을 설정한다. 이러한 속성을 추가 하면,  LMS는 값을 무시한다.

**************************
구글 캘린더 변경하기
**************************

강좌에 포함되어 있는 구글 캘린더를 변경할 때, 학습자는 즉시 업데이트를 보게 된다. 구글 사용자 인터페이스를 통해 캘린더를 변경한다. 구글 캘린더의 구성 요소는 변경할 필요가 없다.

