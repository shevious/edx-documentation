.. _Google Instant Hangout:

###########################################
구글 Instant Hangout 도구
###########################################

.. note:: K-MOOC은 이 도구에 대해 부분적 지원을 제공한다.

.. contents::
  :local:
  :depth: 1

.. _Hangouts_Overview:

*****************
개관
*****************

학습자가 강좌에서 직접 Instant Hangout에 참여할 수 있는 권한을 추가할 수 있다.

Instant Hangout으로, 학습자는 다음을 수행할 수 있다.

* 라이브 비디오와 목소리를 통해 상호 작용한다.
* 화면을 공유하고 함께 비디오를 시청한다.
* 문서를 공동 작업한다.

Instant Hangout 의 전반적인 특징에 대하여,  `Google Hangouts page <http://www.google.com/+/learnmore/hangouts/>`_  (구글 행아웃 페이지)를 참조하도록 한다.

.. note::
 Instant Hangout에 참여하고 싶은 학습자는 구글 계정이 있어야 한다. 강좌 운영팀은 이를 학습자에게 공지해야 한다.

.. _Whitelisting Your Domain for Google Hangouts:

*********************************************
Google Hangout 화이트리스트에 도메인 추가하기
*********************************************

K-MOOC 사이트에서 운영중이라면 Google Hangout 사용을 위해 도메인이 화이트리스트에 추가되어 있어야 한다.

.. _Instant Hangouts in Your Course:

**********************************
Instant Hangout
**********************************

1개 이상의 Instant Hangout을 강좌에 추가할 수 있다. 예를 들어,

* 한 페이지에서, 전체 강좌 진행 중, 학습자에게 Hangout(행아웃)을 제공하기 위해서 Instant Hangout을 추가할 수 있다. 더 많은 정보는 :ref:`Adding Pages to a Course` 를 참고하도록 한다. 

* HTML 구성요소에서, 특정 강좌 학습활동에서 작업하는 학습자에게 행아웃을 제공하기 위해서 Instant Hangout을 추가할 수 있다. HTML 구성요소 만들기에 대한 더 자세한 내용은 :ref:`Working with HTML Components` 를 참조하도록 한다.

Instant Hangout은 Hangout(행아웃)으로부터 열리는 페이지에만 적용된다. 예를 들어, 한 강좌의 학습활동에서 Hangout(행아웃)에 참여한 학습자는 그 Hangout(행아웃)에 참여한 학습자들끼리만 상호 작용하고, 다른 학습활동에서 Hangout(행아웃)에 참여하는 학습자는 다른 Hangout(행아웃) 내에서 상호 작용한다.

.. _The Learner Experience:

*************************
학습자 경험
*************************

강좌에 Instant Hangout을 추가할 때, Hangout(행아웃)과 관련된 버튼과 안내가 해당 페이지에 나타난다. 다음 예제는 강좌 학습활동에 있는 버튼과 안내를 보여준다. 버튼은 학습자가 Hangout(행아웃)을 시작할 수 있고 첫 번째 참가자가 될 수 있다는 메세지가 포함되어 있다.

.. image:: ../../../shared/images/hangout_unit.png
 :alt: Image of the instant hangout control on a unit.
 :width: 600

**Hangout(행아웃)** 을 시작하려면, 학습자는 **Hangout (행아웃)** 시작 을 클릭한다. (첫 번째 학습자가 **Hangout(행아웃)** 시작 을 클릭하면, 다른 학습자는 **Hangout(행아웃)** 에 참여하기 버튼을 보게 된다.)

다음 예제에서는 **Hangout(행아웃)** 이 이미 시작 되었을 때 페이지에 있는 버튼과 안내를 보여준다. **Hangout(행아웃)에 참여하기** 버튼이 있으며, 다른 학습자가 이미 **Hangout(행아웃)** 에 참여하고 있음을 보여준다.

.. image:: ../../../shared/images/hangout_static_page.png
 :alt: Image of the instant hangout control on a page.
 :width: 600

Hangout(행아웃)에 참여하려면, 학습자는 **Hangout(행아웃)에 참여하기** 를 클릭한다.

이미 로그인한 경우, 구글에 로그인하라는 메시지가 표시된다.

.. image:: ../../../shared/images/google_login.png
 :alt: Image of the Google login page.
 :width: 400

구글 계정이 없는 학습자는 로그인 페이지에서 만들 수 있다. 

학습자가 구글에 로그인 한 후, Hangout은 별도 브라우저 창에서 열린다.

.. image:: ../../../shared/images/GoogleHangout_WithPeople.png
 :alt: Image of the instant hangout.
 :width: 600

.. _Limitations:

****************
제한점
****************

현재, 최대 10명의 학습자만 단일 Instant Hangout에 참여할 수 있다. 이를 강좌 안내자료에 알려야 한다.

강좌에서 다른 페이지에서 시작된 Hangout(행아웃)에 있는 학습자는 별도로 계산된다. 그래서 한 학습활동에서 시작된 Hangout(행아웃)에 10명의 학습자가 참여할 수 있고, 다른 학습활동에서 시작된 Hangout(행아웃)에도 다른 10명의 학습자가 참여할 수 있다.

.. _Create the Instant Hangout:

**************************************************
Instant Hangout 만들기
**************************************************

강좌에 Instant Hangout을 만들려면.

#. `instant hangout JavaScript file from GitHub <https://raw.github.com/google/instant-hangouts/master/instanthangouts-0.1.0.js>`_ .

#. 컴퓨터에서 이 파일의 텍스트를 텍스트 편집기로 복사하고, JavaScript 파일로 해당 파일을 저장한다 (즉, 파일을 저장할 때, 확장자명을 .txt 에서 .js 로 변경한다)

   .. note::
     서식을 포함하지 않는 원본 GitHub 파일을 복사하는지 확인한다. 서식이 지정된 파일을 복사하지 않도록 한다. 모든 서식지정은 JavaScript가 제대로 작동하지 않도록 하기 때문이다.

#. 강좌에서 **파일 업로드** 페이지로 JavaScript 파일을 업로드한다. 더 자세한 내용은 :ref:`Add Files to a Course` 를 참고하도록 한다.

#. 페이지 또는 HTML 구성요소에서 HTML 편집기를 연다.

   .. note::
    다른 곳에서 텍스트를 복사해 HTML 에디터에 붙여 넣을 때 반드시 검토하여야 한다. 일부 프로그램은 “straight”버전에서 “smart”나 “curly” 버전으로 따옴표와 ’를 자동으로 고친다. → 재확인부탁드립니다~ 그래서 올바른 “straight” 따옴표가 사용되었는지 확인하여야 한다.

#. 첫 번째 줄에, <script> 태그에서 업로드 한 JavaScript 파일을 추가한다. 이때 완전한 열기 및 닫기 태그를 사용해야 한다.

   예를 들어, JavaScript 파일 이름이 ``instanthangouts-0.1.0.js`` 이면, 다음과 같이 입력한다. ::

     <script src='/static/instanthangouts-0.1.0.js'></script>

#. .<script> 태그 뒤에, 다음을 추가한다. ::

    <div class='instanthangouts'/>

#. 원하는 모든 텍스트와 태그를 추가한다.

   예를 들어, 완전한 HTML은 다음과 같이 될 수 있다.

   ::

    <p>Join an instant hangout by selecting the button below. You can use the
    hangout to have live video discussions with other learners.</p>
    <script
    src='/static/instanthangouts-0.1.0.js'></script>
    <div class='instanthangouts'/>

#. Test the instant hangout in your course.

=============================
JavaScript 파일 업데이트하기
=============================

구글은 정기적으로 Instant Hangout JavaScript파일을 업데이트한다. 업데이트 알림을 수신하려면,  `instant hangouts repository page <https://github.com/google/instant-hangouts/>`_ 로 이동한 다음, 페이지의 오른쪽 위 영역에서 보기 를 클릭한다.

강좌에서 업데이트 된 JavaScript 파일을 사용하려면, 저장소로부터 JavaScript를 강좌에 업로드 한 파일과 같은 이름을 가지는 파일로 복사한다. 새로운 파일을 업로드 하는 경우, 새 파일은 이전 파일을 대체한다.

.. warning::
  업로드된 파일의 파일 이름에 버전 번호를 포함하는 경우, JavaScript 파일을 업데이트할 때마다 Instant Hangout 제어를 포함하는 페이지 또는 모든 HTML 구성요소를 편집해야 한다.
