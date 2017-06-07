.. _Adding Pages to a Course:

###########################
강좌 메뉴 추가하기
###########################

이 장은 강좌에 기본으로 포함되어 있는 페이지 및 탭에 관한 설명과 이를 수정하는 방법, 강좌에 메뉴를 추가하는 방법에 대해 서술한다.

.. contents::
  :local:
  :depth: 2

.. _Default Pages:

*******************
기본 메뉴
*******************

기본적으로 강좌에는 다음과 같은 메뉴가 있다.

* 홈
* 강좌
* 게시판
* 위키
* 진행 상황

홈, 강좌는 필수 메뉴로 순서를 바꿀 수 없다. 하지만 게시판, 위키 및 진행 상황 메뉴는 순서를 바꿀 수 있고 위키와 진도 메뉴는 숨길 수 있으며 더 많은 메뉴를 추가할 수 있다.

.. _Add Page:

****************
새 메뉴
****************

강좌에 새 메뉴를 추가할 수 있다. 각 메뉴는 학습자의 탐색 바에 추가된다.

예를 들어 다음 탐색 바는 기본 메뉴와 함께 음악 이론 입문, 강좌 일정 및 보조자료 메뉴가 추가되어 있다.

.. image:: ../../../shared/images/page_bar_lms.png
 :width: 600
 :alt: Image of the navigation bar in the LMS.

강좌 운영팀은 성적 규정, 강좌 슬라이드, 또는 그 밖의 다른 목적으로 다른 메뉴를 만들 수 있다.

* HTML calendar:  :ref:`Code for Dynamic HTML Schedule` 에 있는 템플릿을 활용해서 만들 수 있다.

* Hangout: :ref:`Google Instant Hangout` 를 참고하라.

==============
강좌 메뉴 추가하기
==============

메뉴를 추가하기 위해.

#. Studio의 **콘텐츠** 에서 **강좌 메뉴** 를 선택한다.

#. **신규 메뉴** 를 클릭한다. **Empty** 제목을 가지는 페이지가 목록에 추가된다.

#. 새 메뉴의 행에서 **편집** 을 클릭하면 HTML 편집기가 열린다.

#. 사용자가 해당 메뉴를 누르면 보여주고 싶은 내용을 입력한다.

   편집기 사용에 관해선  :ref:`Options for Editing HTML Components` 에 자세히 나와있다.

   .. note::
    외부에서 텍스트를 복사하여 HTML 편집기에 붙여넣기를 한다면 반드시 검토를 해야 한다. 일부 어플리케이션은 자동으로 따옴표나 ’를 바꾸기 때문에 재확인이 필요하다.

#. **설정** 을 클릭해서 **메뉴명** 을 수정한다. 이 메뉴명이 강좌에서 학습자에게 보이게 된다.

#. **저장** 을 클릭한다.

강좌가 시작되면 학습자는 즉시 새 메뉴를 이용할 수 있다.

.. _Show or Hide the Course Wiki Page:

********************************************
위키 공개 설정하기
********************************************

기본적으로 강좌는 위키 및 진도 메뉴를 포함한다. 이 메뉴를 강좌에서 사용하는 방법은 :ref:`Course_Wiki` 와 :ref:`A Students View` 에 자세히 나와있다.

강좌를 만들 때 이 메뉴를 학습자에게 공개할지 여부를 결정할 수 있다. 만약 이 메뉴를 숨긴 후 생각이 바뀐다면 언제든지 다시 공개할 수 있다.

.. note:: **진도** 메뉴의 정보는 채점 반영 소주제가 있는 강좌에선 물론, 연습 문제만 있는 강좌에서도 학습자에게 학습 의욕을 고취시킬 수 있다. **진도** 메뉴를 숨기기 전에 학습자에게 줄 수 있는 긍정적인 효과를 고려해야 한다.

강좌 시작 이후 이 메뉴를 숨기거나 다시 공개하는 것은 최대한 피하는 것이 좋다. 예를 들어 학습자가 **위키** 항목을 북마크했는데, 강좌 운영팀이 위키 메뉴를 숨긴 경우, 학습자는 북마크를 통해 해당 **위키** 에 여전히 접근할 수 있다.

=======================================
위키 및 진도 메뉴 숨기거나 공개하기
=======================================

**위키** 나 **진도** 메뉴를 숨기거나 공개하려면.

#. **강좌** 를 선택하고 **메뉴** 를 클릭한다.


   .. image:: ../../../shared/images/pages_wiki_on.png
    :alt: The list of default course pages, with a show/hide icon for the Wiki
      and Progress pages only.

   .. note:: **위키** 와 **진도** 메뉴만이 숨기거나 공개할 수 있다.

#. **공개/숨기기** 아이콘을 클릭해 메뉴를 숨긴다. 다음 예와 같이 아이콘 모양이 메뉴가 숨김 상태임을 나타낸다.

   .. image:: ../../../shared/images/pages_wiki_off.png
    :alt: The default wiki page on the list of course pages, with the show/hide
     icon indicating that the page is currently hidden.

#. **공개/숨기기** 아이콘을 다시 클릭해 메뉴를 공개한다.

.. _Reorder Pages:

****************
메뉴 순서 바꾸기
****************

메뉴를 정렬하려면, 메뉴 오른쪽 끝 끌어서 재정렬하기 아이콘 위에 마우스 커서를 올린 후 원하는 위치로 메뉴를 클릭하여 끌어 옮긴다.

.. note:: 기본적으로 강좌에 포함된 홈 및 강좌 메뉴는 재배열할 수 없다.

.. _Delete a Page:

****************
메뉴 삭제하기
****************

강좌 운영팀이 추가한 메뉴는 삭제 가능하다. 메뉴를 삭제하기 위해 **휴지통** 아이콘을 클릭한다. 삭제를 확인하라는 메시지가 표시된다.

.. note::
  :ref:`default pages<Default Pages>` 는 삭제할 수 없다. 단, 위키와 진도 메뉴는 :ref:`hide<Show or Hide the Course Wiki Page>` 있다.

.. _Code for Dynamic HTML Schedule:

********************************
HTML Schedule 코드
********************************

강좌에서 HTML schedule을 제공하고 싶다면, 다음의 코드를 Raw HTML 편집기에 붙여넣으면 된다.

.. note::
  :ref:`raw HTML editor <The Raw HTML Editor>` 가 아닌 비주얼 편집기에 붙여넣기 하면 안된다.

.. code-block:: html

	<div class= "syllabus">

	<table style="width: 100%">
 		<col width="10%">
 		<col width="15%">
  		<col width="10%">
  		<col width="30%">
  		<col width="10%">
  		<col width="15%">
  		<col width="10%">

	<!-- Headings -->
 		 <thead>
    			<td class="day"> Wk of </td>
   			<td class="topic"> Topic </td>
   			<td class="reading"> Read </td>
    			<td class="video"> Lecture Sequence </td>
    			<td class="slides"> Slides </td>
    			<td class="assignment"> HW/Q </td>
			<td class="due"> Due </td>
  		</thead>

	<!-- Week 1 Row 1 -->
 		 <tr class="first">
   			<td class="day">10/22</td>
			<td class="topic">Topic 1</td>
			<td class="reading">Ch. 1</td>
    			<td class="video"><a href="#">L1: Title</a></td>
    			<td class="slides"><a href="#">L1</a></td>
    			<td class="assignment"><a href="#">HW 1</a></td>
    			<td class="due">11/04</td>
  		</tr>

	<!-- Week 1 Row 2 -->
    		<tr>
    			<td class="day"> </td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L2: Title</a></td>
    			<td class="slides"><a href="#">L2</a></td>
    			<td class="assignment">     </td>
   			 <td class="due">      </td>
  		</tr>

   		 <tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>

	<!-- Week 2 Row 1 -->
 		 <tr>
    			<td class="day">10/29</td>
    			<td class="topic">Topic 2</td>
    			<td class="reading">Ch. 2</td>
    			<td class="video"> <a href="#">L3: Title<a></td>
   			 <td class="slides"><a href="#">L3</a></td>
    			<td class="assignment"><a href="#">Quiz 1</a></td>
    			<td class="due">11/11</td>
 		 </tr>

	<!-- Week 2 Row 2 -->
 		<tr>
  			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L4: Title</a></td>
    			<td class="slides"><a href="#">L4</a> </td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>

	<!-- Week 3 Row 1 -->
  		<tr>
    			<td class="day">11/05</td>
    			<td class="topic">Topic 3</td>
    			<td class="reading">Ch. 3</td>
    			<td class="video"><a href="#">L5: Title</a></td>
    			<td class="slides"><a href="#">L5 </a></td>
    			<td class="assignment"><a href="#">HW 2</a></td>
    			<td class="due">11/18 </td>
  		</tr>

	<!-- Week 3 Row 2 -->
		<tr>
    			<td class="day"> </td>
    			<td class="topic"> </td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L6: Title</a></td>
    			<td class="slides"><a href="#">L6 </a></td>
    			<td class="video"></td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>

	<!-- Week 4 Row 1 -->
  		<tr>
    			<td class="day">11/12</td>
    			<td class="topic">Topic 4</td>
    			<td class="reading">Ch. 4</td>
    			<td class="video"><!--<a href="#">L7: Title</a>--> L7: Title</td>
    			<td class="slides"><!--<a href="#">L7</a>-->L7</td>
    			<td class="assignment"><!--<a href="#">Quiz 2</a>-->Quiz 2</td>
    			<td class="due"> 11/25 </td>
  		</tr>

	<!-- Week 4 Row 2 -->
    		<tr>
    			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L8: Title</a>-->L8: Title</td>
    			<td class="slides"><!--<a href="#">L8</a>-->L8</td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>

	<!-- Week 5 Row 1 -->
  		<tr>
    			<td class="day">11/19</td>
    			<td class="topic">Topic 5</td>
    			<td class="reading">Ch. 5</td>
    			<td class="video"><!--<a href="#">L9: Title</a>-->L9: Title</td>
    			<td class="slides"><!--<a href="#">L9</a>-->L9</td>
    <			td class="assignment"><!--<a href="#">HW 3</a>-->HW 3</td>
    			<td class="due"> 12/02 </td>
  		</tr>

	<!-- Week 5 Row 2 -->
   		<tr>
    			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L10: Title</a>-->L10: Title</td>
    			<td class="slides"><!--<a href="#">L10</a>-->L10 </td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>

	<!-- Week 6 Row 1 -->
  		<tr>
    			<td class="day">11/26</td>
    			<td class="topic">Topic 6</td>
    			<td class="reading">Ch. 6</td>
    			<td class="video"><!--<a href="#"><L11: Title</a>-->L11: Title </td>
    			<td class="slides"><!--<a href="#">L11</a>-->L11</td>
    			<td class="assignment"><!--<a href="#">HW 4</a>-->HW 4</td>
    			<td class="due">12/09</td>
  		</tr>

	<!-- Week 6 Row 2 -->
    		<tr>
			<td class="day"> </td>
    			<td class="topic"> </td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L12: Title</a>-->L12: Title</td>
    			<td class="slides"><!--<a href="#">L12</a>-->L12</td>
    			<td class="assignment"></td>
    			<td class="due">      </td>
		</tr>
	</table>
	</div>
