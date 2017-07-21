.. _Image Mapped Input:

###########################
이미지맵 입력 문제
###########################

.. note:: K-MOOC은 이 문제 유형에 대해 부분적인 지원을 제공한다.

“이미지 클릭 문제”라고도 부르는 이미지맵 입력 문제에서, 학습자는 이미지에 정의된 영역 내부를 클릭한다. 문제 내 좌표를 포함하여 이 영역을 정의할 수 있다.

.. image:: ../../../shared/images/ImageMappedInput-Simple.png
 :width: 500
 :alt: Problem that asks learners to click inside Egypt on a map of Africa.

다음과 같은 영역을 지정할 수 있다.

* 하나의 직사각형 영역. 자세한 사항은 :ref:`Specify a Rectangular Region` 를 참고하면 된다.
* 다수의 직사각형 영역들. 자세한 사항은 :ref:`Specify Multiple Rectangular Regions` 를 참고하면 된다.
* 하나의 사용자 정의 영역. 자세한 사항은 :ref:`Specify an Irregular Region` 를 참고하면 된다.

.. note:: 이미지를 포함한 문제를 만들 때 반드시 접근성을 위해 대체 텍스트를 입력해야 한다. 자세한 사항은 :ref:`Best Practices for Describing Images` 을 참고하면 된다.

****************************************
이미지맵 문제 만들기
****************************************

이미지맵 입력 문제를 만들기 위해.

#. :ref:`Determine Coordinates`.

#. :ref:`Create an IMI Problem in Studio`.

.. _Determine Coordinates:

============================
이미지 정보 모으기
============================

이미지맵 입력 문제를 만들기 위해 다음 요소가 필요하다.

   * 픽셀 단위의 이미지 높이 및 너비.
   * 학습자가 클릭할 영역 혹은 영역들의 좌표 조합.

이미지 정보를 모으기 위해 Microsoft Paint와 같은 이미지 편집 도구를 사용하면 된다.

.. note:: 이미지의 좌표는 좌측 상단을 (0,0)에 두고 우측 하단으로 갈수록 숫자가 크게 한다.

* 직시각형 영역을 지정하기 위해 좌측 상단 구석과 우측 하단 구석의 좌표 2개가 필요하다.

* 다수의 직사각형 영역을 지정하기 위해 각 직사각형에 대한 좌측 상단 구석과 우측 하단 구석의 좌표 2개씩이 필요하다.

* 사용자 정의 영역을 지정하기 위해 3개 이상의 좌표가 필요하다. Studio는 이 좌표를 바탕으로 가장 간단한 도형을 그리며 좌표 입력 순서는 상관없다.

  예를 들어 삼각형을 그리고 싶다면 좌표가 3개 필요하며 팔각형엔 8개 필요하다.

.. _Create an IMI Problem in Studio:

================================================
Studio에서 이미지맵 입력 문제 만들기
================================================

#. Studio에서 이미지를 **파일 및 업로드** 페이지에 업로드하고 파일 경로를 적어놓는다. 자세한 사항은 :ref:`Add Files to a Course` 를 참고하면 된다.
#. 문제를 만들고자 하는 학습 활동의 문제, **신 구성요소 추가** 를 클릭하고 고급 탭을 선택한다.
#. **이미지맵 입력** 을 클릭한다.
#. 나타나는 구성요소에서 **편집** 을 클릭한다.
#. 구성요소 편집기에서 예제 문제 텍스트를 지우고 새 텍스트를 입력한다.
#. ``<imageinput>`` 요소에서.

   #. ``src`` 속성의 예제 파일 경로를 새 파일 경로로 바꾼다.

   #. 이미지 접근성을 높이기 위해 대체 텍스트를 추가한다. 자세한 사항은 :ref:`Best Practices for Describing Images` 를 참고하면 된다.

   #. ``width`` 와  ``height`` 속성의 예제 값을 추가하는 이미지에 맞게 바꾼다.

   #. ``rectangle`` 예제 속성을 지정하기 원하는 영역의 크기와 모양에 맞게 바꾼다. 자세한 사항은 :ref:`Specify a Rectangular Region` , :ref:`Specify Multiple Rectangular Regions` , 와 :ref:`Specify an Irregular Region` 를 참고하면 된다.

#. **저장** 을 클릭한다.

.. _Specify a Rectangular Region:

직사각형 영역 지정하기
****************************************

직사각형 영역을 지정하기 위해 ``<imageinput>`` 요소의 ``rectangle`` 속성을 바꾼다.

* 직사각형 좌측 상단 구석과 우측 하단 구석의 좌표를 (x,y) 형태로 지정한다.
* 각 좌표를 괄호 안에 입력한다.
* –를 이용해 좌표를 구분한다.
* 좌표들을 따옴표 안에 입력한다.


예를 들어 다음  ``rectangle`` 속성은 두 좌표를 이용해 직사각형을 하나 만든다.

``rectangle="(338,98)-(412,168)"``

**문제코드**:

.. code-block:: xml

 <problem>

  <p>What country is home to the Pyramids as well as the cities of
  Cairo and Memphis? Click the country on the map below.</p>

  <imageresponse>
    <imageinput src="/static/Africa.png" width="600" height="638"
  rectangle="(338,98)-(412,168)" alt="Map of Africa" />
  </imageresponse>

  <solution>
    <div class="detailed-solution">

      <p>Explanation</p>

      <p>Egypt is home to not only the Pyramids, Cairo, and Memphis, but also the
  Sphinx and the ancient Royal Library of Alexandria.</p>

    </div>
  </solution>

 </problem>

.. _Specify Multiple Rectangular Regions:

다수의 직사각형 영역 지정하기
****************************************

이미지에서 하나 이상의 직사각형 영역을 지정할 수 있다.

.. image:: ../../../shared/images/ImgMapInput_Mult.png
 :width: 350
 :alt: Problem that asks learners to click inside one of three rectangles

다수의 직사각형 영역 을 지정하기 위해 ``<imageinput>`` 요소의 ``rectangle`` 속성을 바꾼다.

* 각 직사각형의 좌측 상단 구석과 우측 하단 구석의 좌표를 (x,y) 형태로 지정한다.
* 각 좌표를 괄호 안에 입력한다.
* – 를 이용해 좌표를 구분한다.
* 각 직사각형을 ; 로 구분한다.
* 모든 좌표들을 따옴표 안에 입력한다.

예를 들어 다음  ``rectangle`` 속성은 두 좌표를 이용해 직사각형을 세개 만든다.

``rectangle="(62,94)-(262,137);(306,41)-(389,173);(89,211)-(187,410)"``

**문제코드**:

.. code-block:: xml

 <problem>

  <p>In the following image, click inside any of the rectangles.</p>

    <imageresponse>

      <imageinput src="/static/imageresponse_multipleregions.png" width="450"
        height="450" rectangle="(62,94)-(262,137);(306,41)-(389,173);(89,211)-
        (187,410)" alt="Three rectangles on a white background" />

    </imageresponse>

 </problem>

.. _Specify an Irregular Region:

사용자 지정 영역 지정하기
****************************************

하나의 사용자 지정 영역을 지정할 수 있다.

.. image:: ../../../shared/images/ImgMapInput_Irreg.png
  :width: 500
  :alt: Problem that asks learners to click inside a pentagon.

하나의 사용자 지정 영역을 지정하기 위해  ``<imageinput>`` 요소의 ``rectangle`` 속성을 바꾼다.

* ``rectangle`` 을 ``region`` 로 바꾼다.
* 순서 상관없이 3개 이상의 좌표를 입력한다.
* 각 좌표를 **괄호가 아닌** 대괄호([])에 입력한다.
* ,와 띄어쓰기로 각 점들을 구분한다.
* 모든 좌표를 대괄호 안에 작성한다.
* 대괄호를 따옴표 안에 입력한다.

예를 들어 다음  ``regions`` 속성은 오각형을 만든다.

``regions="[[219,86], [305,192], [305,381], [139,381], [139,192]]"``

**문제코드**:

.. code-block:: xml

 <problem>

  <p>In the following image, click inside the pentagon.</p>

  <imageresponse>

    <imageinput src="/static/imageresponse_irregularregions.jpg" width="600"
    height="204" regions="[[219,86], [305,192], [305,381], [139,381],
    [139,192]]" alt ="A series of 10 shapes including a circle, triangle,
    trapezoid, pentagon, star, and octagon" />

  </imageresponse>

 </problem>

.. _Image Mapped Input Problem XML:

******************************
이미지맵 입력 문제 XML
******************************

==========
템플릿
==========

.. code-block:: xml

  <problem>

    <p>Problem text</p>

        <imageresponse>

         <imageinput src="IMAGE FILE PATH" width="NUMBER" height="NUMBER"
         rectangle="(X-AXIS,Y-AXIS)-(X-AXIS,Y-AXIS)" alt="DESCRIPTION OF
         IMAGE" />

        </imageresponse>

  </problem>

=====
태그
=====

* ``<imageresponse>``: 문제가 이미지맵 입력 문제임을 나타낸다.
* ``<imageinput>``: 학습자가 클릭해야 하는 파일에서 이미지 파일 및 영역을 지정한다.

**Tag:** ``<imageresponse>``

문제가 이미지맵 입력 문제임을 나타낸다.

  속성

  (없음)

  Children

  * ``<imageinput>``

**Tag:** ``<imageinput>``

학습자가 클릭해야 하는 파일에서 이미지 파일 및 영역을 지정한다.

  속성들

   .. list-table::
      :widths: 20 80

      * - 속성
        - 설명
      * - ``src`` (필수)
        - 이미지의 URL
      * - ``height`` (필수)
        - 픽셀 단위로 이미지의 높이
      * - ``width`` (필수)
        - 픽셀 단위로 이미지의 너비
      * - ``rectangle`` (필수)
        - 학습자가 클릭해야 할 지역을 의미하는 좌표 조합
      * - ``alt`` (필수)
        - 접근성을 위한 이미지 설명

  Children

  (없음)

