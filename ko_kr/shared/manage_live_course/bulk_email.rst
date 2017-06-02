.. _Bulk Email:

##############################
전체 이메일
##############################

교수자 대시보드에서 강좌 수강생에게 전체 이메일을 보낼 수 있다. 메시지는 HTML 형식을 사용할 수 있으며, 강좌에 관한 비디오, 소셜 미디어 페이지와 기타 자료를 링크로 걸어둘 수 있다. 강좌 운영팀이나 교수자로 역할을 부여 받은 모든 강좌 참가자들은 강좌를 운영하기 전/중/후에 강좌 수강생과 소통하기 위해서 전체 메일을 사용할 수 있다.

학습자는 너무 다수의 이메일 받았을 때 그것을 읽지 않는 경향이 있다. 한 주에 하나 이상의 이메일을 보내지 않는 것이 좋다.

.. note:: 일부 강좌는 MailChimp 등의 외부 프로그램을 사용해 전체 이메일을 보낸다. K-MOOC 전체 이메일 서비스와 외부 프로그램을 동시에 사용하면 안된다. 하나 이상의 서비스를 사용해 발송하면 스팸 이메일로 분류될 가능성이 높기 때문이다.


이 장은 다음과 같은 주제를 다룬다.

.. contents::
  :local:
  :depth: 1

.. _bulk_email_message_addressing:

*************************
Message Addressing
*************************

교수자 대시보드에서 이메일을 보낼 때,  ~에게 옵션을 선택해 수신자를 선택한다. 하나 이상의 수신자를 선택할 수 있다. :ref:`Bulk Email Who Is Included or Excluded` 에 더 자세한 안내가 나와있다.

하나 이상의 수신자 그룹에 메시지를 보낼 때 중복 수신자는 자동으로 걸러지므로 하나 이상의 그룹에 소속되어 있어도 (강좌에 수강 신청한 강좌 운영자 등) 메시지는 한 통만 받게 된다.

다음과 같이 미리 정의된 그룹이 있다.

* **나** 는 전체에 이메일을 보내기 전에 테스트하기 위한 목적으로 사용한다.

* **운영팀과 교수자** 는 다른 강좌 운영팀 구성원에게 연락하기 위한 목적으로 사용한다. :ref:`Course_Staffing` 에 자세한 안내가 나와있다.

* **모든 학습자** 현재 수강 중인 학습자뿐만 아니라 관리팀에게 연락하기 위한 목적으로 사용한다. 이 그룹은 계정을 활성화하지 않았거나 이메일을 수신하지 않기로 선택한 학습자는 포함하지 않는다.

추가적으로 만약 강좌에서 학습집단을 활용하고 있다면 각 집단을 수신자로 지정할 수 있다.  :ref:`Bulk Email Cohorts` 에 더 자세한 안내가 나와있다.


.. _Bulk Email Who Is Included or Excluded:

=========================================
각 수신자 그룹에는 누가 포함되나?
=========================================

이메일을 미리 정의된 그룹에 보낼 때 각 그룹에 누가 포함되는지 알아야 한다.


.. list-table::
   :widths: 30 40 40
   :header-rows: 1

   * - 수신자 그룹
     - 포함되는 인원
     - 포함되지 않는 인원
   * - 운영팀과 관리자
     - * 운영자.
       * 관리자.
     - * **운영자** 또는 **관리자** 역할이 없는 베타테스터.
       * **운영팀** 이나 **관리팀** 역할이 없는 토의진행자.
       * **운영팀** 이나 **관리팀** 역할이 없는 게시판 관리자.
       * 게시판 커뮤니티 조교.
   * - 모든 학습자
     - * 전체 수강신청자(수강 신청을 했지만 아직 강좌페이지에 접속하지 않은 학습자 포함).
       * 강좌를 수강중인 강좌 운영팀.
     - * 계정 활성화 이메일 메시지에 응답하지 않은 학습자.
       * 학습자 대시보드의 이메일 설정에서 이메일을 받지 않기로 설정한 학습자.

.. note:: 그룹 복수 선택도 가능하다. 이 경우 복수 그룹에 속해 있는 사용자일지라도 이메일은 한 통만 받게 된다.


.. _Bulk Email Cohorts:

===================================================
학습집단의 학습자에게 이메일 보내기
===================================================

강좌에서 학습집단을 사용 중이라면 각 학습집단을 수신자 그룹으로 지정할 수 있다. 개별 학습집단이 수신자 그룹으로 지정되면 집단에 배정된 수강중인 학습자만을 포함하게 된다.

학습집단에 배정되지 않은 학습자는 포함되지 않는다. 아직 강좌 수강을 시작하지 않았거나 강좌 운영팀이 학습집단에 직접 배치하지 않았을 경우 발생할 수 있다. 이런 학습자가 확실하게 이메일을 받을 수 있도록 하려면 전체 학습자를 선택하면 된다.

기본 학습집단이 있다면 학습집단: 기본 그룹이라는 이름의 수신자 그룹도 가능하다.

.. note:: 학습자가 수강을 시작했을 때 아직 자동으로 배치된 학습집단이 존재하지 않는다면 기본 학습집단이 만들어진다. 자동으로 배치된 학습집단을 생성하기 전에 학습자가 수강을 시작한다면 자동으로 기본 학습집단에 배치된다. 직접 학습자를 기본 학습집단에서 다른 집단으로 옮길 수 있다. 모든 학습자 배치하기:  :ref:`Default Cohort Group` 에 더 자세한 안내가 나와있다.


.. _Options for Email Message Text:

*******************************
이메일 구성하기
*******************************

다음과 같이 이메일을 구성할 수 있다.

.. contents::
  :local:
  :depth: 1

=======
디자인
=======

이메일은 텍스트 형식과 링크를 포함한 HTML 디자인을 넣을 수 있다. 이메일 편집기는 스튜디오의 HTML 구성요소 편집기와 동일한 기능을 제공한다.

:ref:`Working with HTML Components`  에 더 자세한 안내가 나와있다.

======
이미지
======

이메일엔 이미지가 포함될 수 있다. 이미지를 추가하기 위해 먼저 강좌 파일 업로드 페이지에 이미지 파일을 올려야 한다. 이메일에 시스템이 이미지에 배정하는 웹 URL을 복사해서 넣어야 한다. 그 후 이메일 편집기에서 이미지 추가/편집 아이콘을 클릭해 웹 URL을 추가한다.

https:// 을 웹 URL에 다음 예제와 같이 추가해야 한다.

::

    https://courses.edx.org/asset-v1:{course}.x+{run}+type@asset+block@{image}.jpg

:ref:`Add Files to a Course` 에 더 자세한 안내가 나와있다.

=========
키워드
=========

이메일에는 각 이메일 수신자를 지칭하는 학습자 이름이나 ID와 같은 값이 포함될 수 있다. 학습 관리 시스템은 이러한 정보를 키워드로 대체하여 이메일을 보낸다.

:ref:`Use Keywords in Messages` 에 더 자세한 안내가 나와있다.

.. _Send_Bulk_Email:

**************************************************
이메일 보내기
**************************************************

.. Important:: 전체 이메일 보내기는 발송 후 취소할 수 없다.

   많은 대상에게 이메일을 보내기 전에 자신에게만 이메일을 보내 테스트한다. 원하는 대로 이메일이 작성되었고 링크나 미디어 기능이 작동하는지 확인한다.

강좌 수강생에게 이메일을 보내기 위해.

#. **적용 결과 보기** 를 클릭한다.

#. **교수자** 를 클릭한 후 이메일(EMAIL) 을 클릭한다.

#. **수신자** 드롭다운 목록에서 하나 이상의 대상을 선택한다.

   .. note:: :ref:`Bulk Email Who Is Included or Excluded` 를 참고하여 수신자 그룹을 지정한다.

#. 이메일 제목을 입력한다.

#. 이메일의 본문을 입력한다.

   :ref:`Options for Email Message Text` 에 이메일 작성에 관한 자세한 안내가 나와있다.

#. **이메일 발신** 을 클릭한다.

여러 강좌가 이메일을 동시에 발송했다면, 모든 수신자에게 이메일을 전송하는 데 약간의 시간이 걸릴 수 있다. 이메일 발신 버튼을 눌렀다면, 교수자 대시보드에서 벗어나 다른 작업을 수행하다가 나중에 돌아와서 확인해도 된다.


.. _Use Keywords in Messages:

****************************
이메일에 키워드 활용하기
****************************

이메일에 키워드를 포함할 수 있다. 키워드는 하나의 값으로서 이메일을 보낼 때 각 수신자를 지칭하는 값을 대체하는 것이다. 예를 들어  ``%%USER_FULLNAME%%`` 키워드를 사용하면 각 이메일에 수신자 이름이 포함된다.

.. note::
  이메일 제목에는 키워드를 사용하지 않는다. 제목에 포함된 키워드는 값이 배정되지 않으며 수신자에게 키워드 텍스트가 그대로 보이게 된다.

===================
키워드 종류
===================

다음 키워드를 사용할 수 있다.

* ``%%USER_ID%%`` - 수신자 ID
* ``%%USER_FULLNAME%%`` - 수신자 이름
* ``%%COURSE_DISPLAY_NAME%%`` - 강좌명
* ``%%COURSE_END_DATE%%`` - 강좌 종료일

===================
키워드 형식
===================

``%%Keyword%%`` 로 키워드를 설정한다. 모든 HTML 태그의 키워드를 이메일에 다음과 같이 쓸 수 있다.

::

  <h2>%%COURSE_DISPLAY_NAME%% Updates</h2>

  <p>Dear %%USER_FULLNAME%%, this is a reminder that the last day of the course
     is <b>%%COURSE_END_DATE%%</b></p>
  . . .

.. _Email_queuing:

****************************
이메일 발송 절차
****************************

이메일 발신 을 클릭하면, 서버는 전체 이메일 발송 작업을 시작한다. 서버는 일련의 여러 작업 단계를 최소 작업 단위(task)에 대입한다.

.. image:: ../../../shared/images/Bulk_email_states.png
       :alt: Flowchart of the possible states of a bulk email task.

전체 메일 전송 작업을 위한 작업 흐름 상태는 다음과 같다.

* 대기 행렬(Queuing): 전체 이메일 발송 작업이 실행되고, 백그라운드 처리를 위해 대기한다.
* 보류(Pending): 작업이 대기 되어 실행을 기다리고 있다.
* 시작(Started): 메일 전송 작업을 수행하기 위해 사전 작업이 진행된다.
* 진행(Progress): 메일 전송 작업이 진행된다.
* 성공(Success): 모든 메일 전송 하위 작업이 완료된다. 전체 메일 전송 작업은 일부 메일 전송 하위 작업이 실패하더라도 이 상태에서 있을 수 있음에 주목한다.
* 실패(Failure): 오류가 발생하고, 작업 처리가 성공적으로 완료되지 않았다.

전체 메일 전송 작업이 진행되는 동안 이메일(EMAIL) 페이지에서 **대기중인 작업 목록** 를 확인함으로써, 작업 흐름에 도달하는 데 걸리는 시간을 알아볼 수 있다.

.. image:: ../../../shared/images/Bulk_email_pending.png
       :alt: Information about an email message, including who submitted it
             and when, in tabular format

전체 메일 전송 작업이 완료되면, 이메일 발신 기록 을 확인하여 최종 상태를 확인할 수 있다.  :ref:`Email Task History Report` 을 참고하길 바란다.

.. _Review Sent Messages:

********************************
보낸 이메일 확인하기
********************************

강좌와 관련해서 전송된 모든 이메일 목록을 검토할 수 있다. 나열된 이메일은 제목, 보낸 사람, 보낸 날짜와 시간, 받은 사람 그리고 메일 내용까지 검토할 수 있다.

#. 적용 결과 보기를 클릭한다.

#. **교수자** 를 클릭한 후 **이메일(EMAIL)** 을 클릭한다.

#. 이메일 발신 기록 항목에 이메일 발송 내역 확인을 클릭한다. 보낸 이메일 목록이 뜬다.

   .. image:: ../../../shared/images/Bulk_email_list.png
    :alt: A tabular list of sent messages, with columns for subject, sent by,
          time sent, and number sent.

#. 메시지의 추가 정보를 검토하기 위해 이메일 제목을 클릭한다. 대화 상자에서 메시지가 열린다.

   .. image:: ../../../shared/images/Bulk_email_sent.png
    :alt: A dialog box with the subject, sent by, date and time sent, sent to,
          and message for an email message, and an option to Copy Email
          to Editor.

#. **새로운 이메일** 을 위해 기존의 메일을 선택적으로 사용할 경우, 편집기로 **이메일 복사하기** 를 클릭한다. 대화상자는 닫히고, **제목** 과 본문 필드에서 복사한 텍스트, 링크, 서식을 편집할 수 있다.

   이전에 보낸 메일을 복사하여 새로운 메일을 작성할 때, 모든 강좌 수강생에게 보내기 전에 철저히 검토하고 테스트해야 한다.

.. _Email Task History Report:

********************************
이메일 작업 이력
********************************

이메일 작업 이력 보고서는 메일을 전송한 사람, 시간과 전송한 사람의 수를 추적할 수 있다. 전송된 각 이메일에 대한 보고서에는 요청자 이름, 전송 날짜와 시간, 작업 진행 기간과 상태, 작업 등이 포함된다.

전송된 메일과 관련된 다음과 같은 질문에 답하기 위해 이 기록을 사용할 수 있다.

* 학습자가 강좌와 관련된 메일을 받은 빈도.
* 이메일이 성공적으로 전송되었는지 여부.
* 시간 경과에 따라 강좌와 관련된 메일을 받은 사람의 수의 변화.

이메일 발신 기록 보고서를 제출하려면.

#. 적용 결과 보기를 클릭한다.

#. **교수자** 를 클릭한 후 **메일** 을 클릭한다.

#. **이메일 발신 기록** 에서 **이메일 작업 이력 나타내기** 를 클릭한다. 다음 예시와 같은 보고서는 교수자 대시보드에 나타난다.

.. image:: ../../../shared/images/Bulk_email_history.png
       :width: 800
       :alt: A tabular report with a row for each message sent and columns for
        requester, date and time submitted, duration, state, task status, and
        task progress.

===========================
이메일 작업 이력 확인하기
===========================

상태가 성공일 경우, 작업 진행 열에 정보를 제공하는 메시지가 나타난다. 이 메시지는 “13,457명의 수신자에게 성공적으로 전달된 메시지(29명 읽지 않음) (13,486명 중)”와 같은 형식을 가질 수 있다. 이 메시지를 해석하기 위해서 다음을 알아야 한다:

* 첫 번째 숫자(“수신자”)는 선택한 수신자에게 보낸 메시지의 수를 나타낸다.

* 두 번째 숫자(“읽지 않음”)는 강좌에 등록되어 있으며, 계정이 활성화된 사용자 중 메시지를 받지 않은 사용자의 수를 나타낸다. 이 수는 강좌와 관련된 메일 수신을 거부한 학생의 수이다.

* 마지막 숫자(“총 사람 수”)는 메일을 전송할 때 (그들의 사용자 계정이 활성화되었으며) 강좌에 등록되어 있어 선택한 수신자에 있는 사용자의 수를 나타낸다.

  강좌 정보 페이지에 나타난 총 등록자 수는 계정 활성화 상태와 상관없이 현재 등록된 모든 학습자를 말하며, 결과적으로 위의 사람들의 총 수와 다를 수 있다.

만약 “수신자”와 “총 사람 수”가 같다면, “13,457명의 수신자에게 성공적으로 전달된 메시지”라는 메시지를 읽을 수 있을 것이다.

상태가 성공일 경우, 위의 메시지가 아닌 아래와 같이 다른 메시가 나타난다면  메일 전송의 전체 또는 일부 작업이 성공적이지 않음을 의미한다:

* “{메일 전송 시도한 수}의 수신자 중 {메일 전송 성공한 수}의 수신자에게 메일을 전송했습니다.”
* “{메일 전송 시도한 수}의 수신자에게 메일 전송에 실패했습니다.” 
* “메일을 전송할 수신자를 찾을 수 없습니다.”

**작업 진행** 메시지는 실패한 상태 인 작업에서 보이지 않는다.

.. _Example Messages to Students:

*********************************
Example Messages to Learners
*********************************

강좌 내의 소통을 위해 일반적인 강좌 일정보다 미리 강좌를 준비하면서, 다음 메일 예시를 사용할 수 있다.

.. contents::
  :local:
  :depth: 1

이러한 메시지는 메일 형태로 되어 있지만, 강좌 게시판 주제나 홈 페이지에 이러한 정보를 게시할 수 있다. 키워드는 사용할 수 없으며 키워드 사용을 위해선 반드시 이메일을 보내야 한다.

.. important::
 자신이 수강하는 강좌의 정보를 포함하고 학습자의 요구사항을 충족하며 각자의 목표와 성향을 반영하기 위해 이러한 메시지 서식을 수정한다. 프롬프트(지시 메시지)를 찾기 위해 {“and”} 문자를 검색하고, 그들을 각 강좌에 해당하는 값으로 바꾼다.

 이 메시지의 일부는 키워드를 포함한다. 강좌와 수신자를 특정하는 값은 키워드로 대체된다.

.. _Prelaunch Reminder:

====================
개강 전 알림 메일
====================

개강 전 알림 메일은 강좌 시작 날짜를 상기시키고, 강좌를 알리며 흥미를 유발시킨다. 메일 예시에서 강좌 시작 일자와 시간뿐만 아니라 학습자는 다음의 사항을 알아야 한다:

* 강좌와 함께 운영하는 소셜 미디어 사이트가 있다. 학습모임등의 모임 조직이나 다른 학습 커뮤니티 구축 기회를 제공할 수 있다.


강좌가 시작되기 전에 하나 이상의 메시지를 보낼 수 있다. 전송하고 싶은 다른 메시지를 작성하기 위해 아래의 내용으로 시작해 볼 수 있다. {중괄호} 안에 들어간 부분은 각 강좌에 적용되는 정보로 바꾼다. 또한, 키워드를 적절하게 활용해야 한다.

::

  Subject: {course number} Starts Soon!

  Hello %%USER_FULLNAME%%,

  We are excited that you are joining us for {course number}
  %%COURSE_DISPLAY_NAME%%, offered by {organization name} through edX. Class
  begins on {day}, {date} at {time} UTC (which is {time} {local time zone}).
  Note that edX courses use Coordinated Universal Time (UTC) for due dates and
  release times. You might want to verify the times in the course by using a
  time zone converter such as {link}.

  In case you haven't already found it, {course number} has its own official
  Facebook page {add link}. You can find videos and photos posted there before
  the course even begins.

  If this is your first edX course, consider enrolling in the edX Demo course
  {add link}. This course gives you an opportunity to explore the edX platform
  and learn how to answer problems and track your progress, before {course
  number} begins.

  Your {course number} course staff

.. _Launch Day Welcome:

===================
개강일 인사 메일
===================

개강일과 관련하여 학습자를 환영하고 해야 할 일들을 담은 이메일을 보낸다. 아래의 예문은 학습자에게 두 강좌를 소개하고 궁금하였던 점에 대한 답을 찾거나 강좌 운영팀원을 소개한다. 본 예문에서 괄호{ }안에 있는 내용을 검색하여 해당 강좌 정보로 변경한다.

::

  Subject: {course number} Starts Today!

  Hello everyone!

  At this time, edX course {course number} is available from your Dashboard
  {add link}, and the staff would like to officially welcome you to the course!
  You'll find materials for the first week on the Course page,
  including both video lectures and problem sets.

  Please take some time to go to the Home page to read the handouts
  and get familiar with course policies and philosophy.

  I will be your course lead and I hope you will all have a great time learning
  {subject}! It may be challenging, it may be frustrating, but it will be
  rewarding and you will learn a ton.

  On behalf of the staff, welcome, good luck, and have fun!

  {name} and the {course number} staff

.. _Verified Registration Reminder:

==============================================
이수증 안내 이메일
==============================================

개강을 하고 나면, 이메일을 보내 학습자들에게 이수 등록 마지막 일이 다가오고 있음을 알린다. 아래 예문를 활용하여 안내 메일 작성의 초안을 생각해보도록 한다. 괄호 {}안의 수치를 검색하여 자신 강좌에 맞는 정보로 교체하도록 한다. 반드시 키워드를 적절하게 활용하도록 한다.

::

  Subject: Earn an edX verified certificate for {course name}!

  Dear %%USER_FULLNAME%%,

  Interested in using an edX certificate to bolster a college application or to
  advance your career? With an edX verified certificate, you can demonstrate to
  colleges, employers, and colleagues that you successfully completed a
  challenging edX course, while helping to support the edX mission.

  We would like to remind you that {date} is the last day to register for a
  verified certificate in %%COURSE_DISPLAY_NAME%%. Registering for a
  certificate is easy! Just go to this course on your edX dashboard and click
  "Challenge Yourself".

  Good luck!

  {name} and the {course number} staff

.. _Weekly Highlights:

==================
주별 학습 주요 사항 안내 메일
==================

일주일에 한번씩 학습자에게 이메일을 보내는 것은 학습을 보다 적극적으로 하도록 하는 좋은 방법이다. 매 주말마다 학습자에게 이메일을 보내어 강좌에서 다루었던 내용을 요약하고 학습자에게 앞으로 제출해야 하는 과제 및 강좌의 전반적인 주요 쟁점을 정리해 준다. 또한, 게시판 토의를 활성화시키기 위하여, 흥미롭거나 중요한 게시물에 대해 강조를 할 수도 있고 해당 주제와 관련된 링크를 제공할 수도 있다.

이메일을 처음 작성할 때 아래 예시를 활용한다. 단, 자신의 강좌에 적절하지 않다고 생각되면 토의가 이루어지는 게시글에 대한 부분은 생략할 수 있다. 괄호 {}안의 내용을 자신 강좌에 맞게 수정한다. 반드시 키워드를 적절하게 활용하도록 한다.

::

  Subject: {Course Name} Week 1 Highlights

  We hope you all had a great week! Below, we have provided links to some
  exciting discussions that have been going on, and a Q&A video with
  {Professor} that recaps some of the questions that have come up this week.

  We'd also like to remind you to take this week's quiz by {date} at {time} UTC.
  The next module will be available on {Time and Date}.

  {Link to Video}

  Here are a few highlights from the discussion forum this week. Please join us
  online and keep the conversation going!

  * There has been quite a debate over whether urban stream restoration is
    possible and what types of restoration are desirable. How can we improve
    restoration practice and its outcomes? {Link to the Discussion}

  * Please continue to share your stories of urban stream restoration - there
    are many great examples here of what is possible! {Link to the Discussion}

  See you next week,
  {name} and the {course number} staff


.. _Midcourse Encouragement:

========================
참여 독려 메일
========================

강좌가 진행 중일 때, 학습자에게 메시지를 보내 학습 공동체를 활성화시킬 수 있고 학습자에게 마감일을 상기시키며 앞으로 진행될 주요 사항에 대해 다룰 수 있다.

아래 예시는 학습자들이 어떻게 강좌 일정을 따르고 게시판의 토의에 참여할 수 있는지를 나타내고 있다. 강좌가 진행 중일 때 여러 메시지를 보낼 수도 있다. 메시지를 처음 보낼 경우 아래의 예시를 활용할 수도 있다. 괄호 {}안의 내용을 자신 강좌에 맞게 수정한다. 반드시 키워드를 적절하게 활용하도록 한다.

::

  Subject: {course name} Announcements

  Dear students,

  We hope that you are learning a lot in {course number}! Remember that problem
  set {number} is due on {date} at {time} UTC. You can always check the
  schedule {add link} on the Home page to plan ahead.

  The contributions to the course discussions have been amazing. You'll also
  see on the Home page that we have made several of you community
  TAs to thank you for your thoughtful contributions. Keep those conversations
  going!

  We have a few additional announcements.

  * Week {number} on {subject} is now available on the Course page.

  * Problem set {number} is also available. It is due on {date} at {time} UTC.

  * Remember that the due dates for problem sets and exams are in UTC (the GMT
    time zone). See the current UTC time here {add link}. Please convert the
    times given to your own time zone!

  Wishing you continued success in the course,

  {name} and the {course number} staff

.. _Midcourse Events:

========================
주요 일정 안내 메일
========================

시험이나 다른 강좌의 주요 일정 이전에 메시지를 보내 시험에 대한 정보를 제공하고 규칙에 대해 이야기해 볼 수 있고, 학습자로 하여금 성공적으로 강좌를 이수할 수 있도록 격려할 수 있다:

* 시험 시간은 얼마나 되고 문제에 대한 해답은 언제 받을 수 있는가.

* 시험 시간 동안 오류나 다른 기타 쟁점에 대해 감독관과 어떻게 소통할 수 있는가.

* 시험 시간 동안 강좌 게시판 이용 가능 여부 (아래에 제시되는 예시에서는 게시판 이용이 가능하다.)

* 학습자 서약 위반은 어떻게 구성이 되는가.

* 채점자와 같이 외부인들이 겪을 수 있는 기술적인 한계가 있다면 어떤 것이 있는가.

괄호 {}안의 내용을 자신 강좌에 맞게 수정한다. 반드시 키워드를 적절하게 활용하도록 한다.

::

  Subject: {course number} Exam Info

  Hello %%USER_FULLNAME%%,

  Great job working through week {number}! As you know, the {course number}
  exam is next week. If you missed a problem set, you can still earn a
  certificate. Each problem set is worth only {number}% of the overall grade,
  but this exam is worth {number}%.

  Please read this important information about the exam before you begin taking
  it.

  * The exam starts on {date} at {time} UTC and must be finished by {date} at
    {time} UTC. Plan your schedule accordingly.

  * Be sure that you know what time the UTC deadline is in your time zone. See
    the current UTC time {add link}. No extensions will be given.

  * The exam is not timed. You can start, stop, and come back to it until the
    deadline.

  * Each exam question allows only one answer submission. If you accidentally
    click "Check", that problem cannot be reset for you.

  * The exam covers everything (video lectures, reading, and problem sets) from
    weeks {number}-{number}. If you missed any of these materials, you will
    want to review them before you take the exam.

  * You can use the textbook and the Internet to clarify your knowledge of exam
    topics, as long as you are not deliberately looking up answers to exam
    questions.

  * Course discussions will remain open during the exam, but anyone who posts
    an answer to an exam question will be violating the honor code and risk
    being removed from the class, forfeiting the certificate.

  * If you need to alert the staff to an issue with the exam while the exam is
    open, add a post to the General discussion topic and include [EXAM] in
    the subject line.

  * Check the Home page periodically. It is the fastest way the
    staff has to communicate any delays, corrections, or changes.

  Good luck!

  {name} and the {course number} staff

.. _Technical Issue:

========================
기술적 문제 관련 이메일
========================

예상하지 못한 시스템 장애가 발생할 경우, 이메일을 보내서 학습자들에게 해당 문제에 대한 위험을 알리고 해당 장애가 현재 처리 중이거나 해결 중이라는 상황을 알려서 안심시킨다. 이메일에는 장애 발생으로 강좌에 영향을 줄 경우, 관련 정보를 제공할 수 있다.

강좌가 진행 중일 동안 여러 가지 이유로 기술적인 문제가 발생한다. 그러므로 아래 예시는 현재 겪고 있는 문제가 어떤 것이냐에 따라 다르게 변경하여 적용해야 할 것이다. 주의해야 할 점은 해당 문제에 영향을 받는 학습자들을 안심시키도록 긍정적인 어조, 문제, 해결 방안의 상황, 그리고 다른 영향에 관련된 사항을 차분하고 간결하게 다루어야 한다는 점이다.

::

  Dear students,

  We've encountered a technical problem with {video, assignment, etc. name}.
  {We are working to resolve it now. / This issue has been fixed.}

  As a result of this issue, we have {extended the deadline for / rescored}
  this assignment so that it will not affect your grade.

  Thanks for your patience, and we look forward to continuing the course with
  you.

  {name} and the {course number} staff

.. _Course Farewell and Certificates:

=================================
종강 안내 및 이수증 안내 메일
=================================

종강하기 며칠 전쯤, 메시지를 보내 학습자들에게 강좌 설문조사, 이수에 관한 질문의 답변에 대한 안내를 함으로써 강좌 교재를 차후 활용할 수 있도록 해당 정보를 제공하도록 한다. 반드시 괄호 {}안에 있는 내용을 자신 강좌의 것으로 수정한다.

::

  Subject: {course number} Final Remarks

  Dear %%USER_FULLNAME%%,

  Thank you for making %%COURSE_DISPLAY_NAME%% so much fun these last few
  months! We had a great time getting to know you through the course
  discussions. We appreciate the effort that you put into this course, and we
  hope that you enjoyed learning {subject} through edX. With or without a
  certificate, you should be proud of your accomplishments.

  * Please take a few minutes to answer the exit survey, now available on the
    Course page. We will use your responses to improve the course in the
    future.

  * If you qualify for a certificate (overall score {number}% or higher), the
    edX dashboard will include a link to your certificate in the near future.
    While you may see the link in a few days, it can take up to two weeks edX
    to generate all of the course certificates.

  * As an enrolled student, you will have access to the lecture videos even
    after the course ends. Assessments will remain, but you will no longer be
    able to submit answers to any problem sets or exams with due dates.

  * The {course number} discussions close on {date} at {time} UTC. You will not
    be able to add to the discussions after that time, but you will be able to
    continue viewing all of the conversations that took place during the
    course.

  We hope that you share what you learned in {course number} with your
  colleagues, friends, and family.

  Good luck on the final exam and beyond!

  {name} and the {course number} staff

.. _New Course Run Announcement:

=================================
신규 강좌 개설 안내 메일
=================================

신규 강좌를 개설 할 때, 기존 운영 (혹은 여러 운영) 상태의 전체 이메일 활용하기를 선택하여 현재 수강중인 기존 학습자들에게 정보를 전달할 수 있다. 기존 운영상태에서 신규 강좌에 대해 학습자들에게 알리는 것은 토의의 질과 다양성 혹은 전세계적 관심사 및 기존 등록자수로 증명이 된 주제의 적절성과 같은, 강좌의 주요 측면에 대해 강조할 수 있는 기회를 부여한다. 또한 신규 강좌를 통해 추가된 새로운 특징들이나 내용에 대해서 공개할 수도 있다. 강좌가 얼마나 가치 있는지 강조함으로써 학습자들이 자신의 경험에 대해 다시 생각해보고 이에 대해 공유하며 흥미를 가지고 재등록을 할 수 있게 유도할 수 있는 것이다.

본 메시지 예시는 강좌를 이수하지 않은 학습자들 혹은 이수증 확인 및 기회를 가지지 못했던 학습자들에게 이를 위한 기회를 제공한다. 특히 학습자들로 하여금 동료 학습자들과 친구들을 통해 해당 강좌를 공유할 수 있도록 해준다.

본 예시를 통해 메시지를 작성할 때는 괄호 {}안의 내용을 자신 강좌에 맞게 수정한다.

::

  Subject: Announcing a new run of {course name}

  Hello {course number} learners,

  The next run of {course number} {course name} begins on {date}! We are glad
  to share this news with you, the students who made the earlier run{s} of
  {course number} so successful.

  {Success story from the previous run.}

  {New content or features for the upcoming run.}

  Perhaps you want to share the {course name} experience with a friend or
  colleague, earn an ID-verified certificate of achievement, or work through
  course content that you weren't able to complete before. When {course number}
  is offered in {time frame}, we welcome you to join the community of learners
  again.

  To learn more and to enroll, visit the {course name} page {add link}.

  We hope to see you in the course,

  The {course number} Staff
