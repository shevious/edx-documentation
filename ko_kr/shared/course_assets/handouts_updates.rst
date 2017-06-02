.. _Adding Course Updates and Handouts:

######################################################
공지사항 및 학습 자료 추가하기
######################################################

Studio에서 공지사항 및 학습 자료를 추가할 수 있다. 학습자는 **홈** 탭에서 공지사항 및 학습 자료를 볼 수 있다.

.. image:: ../../../shared/images/course_info.png
 :alt: The Home page as it appears to students, with a "Course Updates
       & News" section containing a dated post and a "Course Handouts" frame
       with a list of links.

.. contents:: Section Contents
   :local:
   :depth: 1

.. _Add a Course Update:

**********************
Add a Course Update
**********************

학습자에게 시험, 강좌 일정 변경 등을 알리기 위해 공지사항을 추가할 수 있다. 공지사항을 올리자마자 학습자는 이를 조회할 수 있다.

각 공지사항엔 날짜가 반드시 있어야 한다. 학습 관리 시스템에서 공지사항은 **홈** 화면에 날짜에 따라 역 시간순 (가장 최신이 맨 위에 온다)으로 표기된다.

공지사항을 추가하려면.

#. **콘텐츠** 메뉴에서 **공지사항** 을 선택한다.
#. **새 공지사항** 을 클릭한다.
#. 텍스트 편집기에 내용을 입력한다.

   * HTML 태그 형식을 사용해 공지사항에 대한 텍스트를 입력한다. 현재 :ref:`visual editor<The Visual Editor>` 는 제공되지 않는다.
    HTML로 직접작성이 어렵다면 아래의 방법을 따르면 좋다.
    (https://html-online.com/editor/ 접속하여 에디터 내에서 내용 작성 -> 소스버튼 클릭 -> 소스 복사해서 공지사항에 붙여넣기)


     .. note:: 외부에서 텍스트를 복사하여 텍스트 편집기에 붙여넣기를 한다면 반드시 검토를 해야 한다. 일부 어플리케이션은 자동으로 따옴표나 ’를 바꾸기 때문에 다시 한번 확인이 필요하다.

   * 공지사항의 날짜를 입력해야 한다. 기본 설정으로 금일 날짜가 입력되지만, 달력 도구를 이용하거나 다른 날짜를 입력해서 바꿀 수 있다. 또한 날짜는 정리와 확인의 목적만을 위해 사용된다.

#. **게시하기** 를 클릭한다. 즉시 **홈** 화면에 반영된다.

.. The following step allows installations that use the edX mobile apps to send
.. a push notification to the app when an update is added. Alison, DOC-1814,
.. June 2015

.. only:: Open_edX

.. _Add Course Handouts:

***************************
학습 자료 추가하기
***************************

“파일 업로드” 메뉴를 통해 업로드 한 파일을 학습 자료로 지정할 수 있다. 학습자는 **홈** 화면에서 각 학습 자료에 대한 링크를 볼 수 있다.

학습 자료를 지정하기 전에 강좌에  :ref:`add the file<Add Files to a Course>` 하고 Studio URL을 복사해야 한다. Studio 파일 업로드 페이지를 새 탭으로 열면 작업이 더욱 수월해진다.

학습 자료를 지정하기 위해.

#. **콘텐츠** 메뉴에서 **공지사항** 을 선택한다.
#. 화면 오른쪽의 **학습 자료** 에서, **편집** 을 클릭한다.
#. 열리는 편집기에서 HTML 형식을 사용해 기존에 업로드한 파일에 대한 링크를 다음 예제와 같이 추가한다.

   .. code-block:: html

     <p><a href="/static/Syllabus_Fall2016.pdf" target="_blank">Syllabus</a></p>
     <p><a href="/static/Glossary_v3.pdf" target="_blank">Glossary</a></p>

#. **저장** 을 클릭한다.
