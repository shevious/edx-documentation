.. _Drag and Drop:

##################################
드래그 앤 드롭 문제(기존)
##################################

.. note::
    이 드래그 앤 드롭 문제 형식은 신 버전으로 대체되었다. 신 드래그 앤 드롭 문제는 더욱 많은 기능을 제공하므로 신 버전을 쓰는 것을 권장한다. 자세한 사항은  :ref:`drag_and_drop_problem` 를 참고하면 된다.

.. warning::

 * **기존 드래그 앤 드롭 문제는 장애가 있는 학습자가 사용할 수 없으며 스마트폰 등 터치 스크린을 사용하는 장치에서 사용할 수 없다. 이 문제 형식을 사용한다면 풀 수 없는 학습자를 위한 방안을 마련하거나 채점이 되지 않는 문제로 두는 것이 좋다.**

   접근성 높은 콘텐츠를 만드는 자세한 방법은 :ref:`Accessibility Best Practices for Course Content Development` 를 참고하면 된다.
   
 * **정답 보기** 버튼은 드래그 앤 드롭 문제에서 사용할 수 없다. 기본적으로 **정답 보기** 옵션은 **사용하지 않음** 으로 설정되어 있다. 문제 구성요소에서 이 설정을 바꾸면 학습 관리 시스템에 **정답 보기** 버튼이 보이지만 작동하지 않는다.

.. note:: K-MOOC은 이 문제 유형에 대해 부분적인 지원을 제공한다.

드래그 앤 드롭 문제에서 학습자는 텍스트나 이미지를 드래그하여 이미지의 특정 위치에 드롭하여 질문에 응답한다.

.. image:: ../../../shared/images/DragAndDropProblem.png
 :alt: Image of a drag and drop problem

*********************************
드래그 앤 드롭 문제 만들기
*********************************

학습자가 이미지 위로 라벨을 드래그 하는 간단한 드래그 앤 드롭 문제를 만들려면, 학습자가 라벨을 드래그하여 드롭할 이미지를 업로드 한 다음, 문제 구성요소를 만든다.

#. **파일 업로드** 페이지에서, 이미지 파일을 업로드한다. 파일 업로드에 대한 자세한 내용은 :ref:`Add Files to a Course` 을 참조한다.
#. 문제를 만들려는 학습활동에서, **신규 구성요소 추가** 아래에 문제 를 클릭한 다음, **고급** 탭을 클릭한다.
#. **드래그 앤 드롭** 을 클릭한다.
#. 표시되는 구성 요소에서 **편집** 을 클릭한다.
#. 구성요소 편집기에서 예제 텍스트를 문제 텍스트로 대체한다.
#. ``<drag_and_drop_input>``  태그에서, 파일 업로드 페이지에서 **https://studio.edx.org/c4x/edX/DemoX/asset/L9_buckets.png** 을 이미지 파일의 URL로 대체한다 **(예, /static/Image.png )**.
#. 하나 이상의 ``<draggable>`` 태그에 대하여, 라벨 속성의 텍스트를 학습자가 드래그 할 라벨의 텍스트로 대체한다. 예를 들어, 학습자가 이미지에 “아이슬란드”라는 단어를 드래그하기 원한다면, 새로운 태그는 다음과 유사할 것이다.

   ``<draggable id="1" label="Iceland"/>``

8. 사용하고자 하는 모든 라벨에 대하여 이전 단계를 반복한다. id 속성은 각  ``<draggable>`` 태그에 대해 다르다는 것을 확인한다.
#. 이미지에서 특정 영역의 좌표와 반지름을 결정한다.

#. ``correct_answer = {`` 아래에 다음 양식을 사용하여 각 라벨에 대한 항목을 추가한다. 이 값은 픽셀이다.

    ``'id':    [[x coordinate, y coordinate], radius]``

    예를 들어, 이미지가 600 픽셀의 너비 및 400 픽셀의 높이를 가지며, 학습자가 이미지의 왼쪽 위 부분 영역에는 아이슬란드 라벨을, 이미지의 오른쪽 아래 부분 근처에는 스웨덴 라벨을 드래그 하기를 원하는 경우, 코드는 다음과 유사하다 (여기에서 2는 스웨덴 라벨을 위한 ID이다.)

    .. code-block:: xml

        correct-answer = {
                '1':    [[50, 50], 75]
                '2':    [[550, 350], 75]}

    .. note:: Make sure the code contains the closing curly brace (**}**).
#. **저장** 을 클릭한다.


==========================================
Drag and Drop 문제 코드 샘플
==========================================

이미지에 표시되는 드래그 드롭 문제를 만들려면, K-MOOC에서 두 개의 파일을 다운로드 한 후, 파일 업로드 페이지로 이 파일을 업로드하고 난 다음, 문제 구성 요소에 문제에 대한 코드를 추가해야 한다.

#. 다음 파일을 다운로드한다

  * Allopurinol.gif
  * AllopurinolAnswer.gif

  .zip 저장소에서 위의 두 파일을 다운로드 하려면, http://files.edx.org/DragAndDropProblemFiles.zip 를 클릭한다.

#. **파일 업로드** 페이지로 Allopurinol.gif 및 AllopurinolAnswer.gif 파일을 업로드 한다.
#. 문제를 만들려는 학습활동에서, **신규 구성요소 추가** 아래에 **문제** 를 클릭하고 난 다음, **고급** 탭을 클릭한다.
#. **드래그 앤 드롭** 을 클릭한다.
#. 표시되는 구성요소에서, **편집** 을 클릭한다.
#. 구성요소 편집기에서, 예제 코드를 다음 코드로 대체한다.
#. **저장** 을 클릭한다.

**문제 코드 ** :

.. code-block:: xml

  <problem>
    <p> Allopurinol is a drug used to treat and prevent gout, a very painful form of arthritis. Once only a “rich man’s disease”, gout has become more and more common in recent decades – affecting about 3 million people in the United States alone. Deposits of needle-like crystals of uric acid in connective tissue or joint spaces cause the symptoms of swelling, stiffness and intense pain. Individuals with gout overproduce uric acid because they cannot eliminate it efficiently. Allopurinol treats and prevents gout by stopping the overproduction of uric acid through inhibition of an enzyme required for the synthesis of uric acid. </p>
    <p> You are shown one of many possible molecules. On the structure of allopurinol below, identify the functional groups that are present by dragging the functional group name listed onto the appropriate target boxes on the structure. If you want to change an answer, you have to drag off the name as well. You may need to scroll through the names of functional groups to see all options. </p>
    <customresponse>
      <drag_and_drop_input no_labels="true" one_per_target="true" target_outline="true" img="/static/Allopurinol.gif">
        <draggable can_reuse="true" label="methyl" id="1"/>
        <draggable can_reuse="true" label="hydroxyl" id="2"/>
        <draggable can_reuse="true" label="amino" id="3"/>
        <draggable can_reuse="true" label="carboxyl" id="4"/>
        <draggable can_reuse="true" label="aldehyde" id="5"/>
        <draggable can_reuse="true" label="phosphate" id="6"/>
        <draggable can_reuse="true" label="sulfhydryl" id="7"/>
        <draggable can_reuse="true" label="phenyl" id="8"/>
        <draggable can_reuse="true" label="none" id="none"/>
        <target id="0" h="53" w="66" y="55.100006103515625" x="131.5"/>
        <target id="1" h="113" w="55" y="140.10000610351562" x="181.5"/>
      </drag_and_drop_input>
      <answer type="loncapa/python">
  correct_answer = [
      {'draggables': ['2'], 'targets': ['0' ], 'rule':'unordered_equal' },
      {'draggables': ['none'], 'targets': ['1' ], 'rule':'unordered_equal' }]
  if draganddrop.grade(submission[0], correct_answer):
      correct = ['correct']
  else:
      correct = ['incorrect']
      </answer>
    </customresponse>
    <solution>
      <img src="/static/AllopurinolAnswer.gif"/>
    </solution>
  </problem>


.. _Drag and Drop Problem XML:

*********************************
Drag and Drop 문제 XML
*********************************

.. code-block:: xml

 <problem>
     <customresponse>
         <p>Drag each word in the scrollbar to the bucket that matches the number of
         letters in the word.</p>
         <drag_and_drop_input img="https://studio.edx.org/c4x/edX/DemoX/asset/L9_buckets.png">
             <draggable id="1" label="a"/>
             <draggable id="2" label="bog"/>
             <draggable id="3" label="droll"/>
             <draggable id="4" label="oboe"/>
             <draggable id="5" label="swain"/>
             <draggable id="6" label="in"/>
             <draggable id="7" label="onyx"/>
             <draggable id="8" label="of"/>
             <draggable id="9" label="tap"/>
             <draggable id="10" label="strop"/>
             <draggable id="11" label="few"/>
         </drag_and_drop_input>
         <answer type="loncapa/python">
             correct_answer = {
                 '1':      [[70, 150], 121],
                 '6':      [[190, 150], 121],
                 '8':      [[190, 150], 121],
                 '2':      [[310, 150], 121],
                 '9':      [[310, 150], 121],
                 '11':     [[310, 150], 121],
                 '4':      [[420, 150], 121],
                 '7':      [[420, 150], 121],
                 '3':      [[550, 150], 121],
                 '5':      [[550, 150], 121],
                 '10':     [[550, 150], 121]}
             if draganddrop.grade(submission[0], correct_answer):
                 correct = ['correct']
             else:
                 correct = ['incorrect']
         </answer>
     </customresponse>
 </problem>

.. code-block:: xml

 <problem>
     <customresponse>
         <p>Label the hydrogen atoms connected with the left carbon atom.</p>
         <drag_and_drop_input img="https://studio.edx.org/c4x/edX/DemoX/asset/ethglycol.jpg"
         target_outline="true" one_per_target="true" no_labels="true"
         label_bg_color="rgb(222, 139, 238)">
             <draggable id="1" label="Hydrogen" />
             <draggable id="2" label="Hydrogen" />
             <target id="t1_o" x="10" y="67" w="100" h="100"/>
             <target id="t2" x="133" y="3" w="70" h="70"/>
             <target id="t3" x="2" y="384" w="70" h="70"/>
             <target id="t4" x="95" y="386" w="70" h="70"/>
             <target id="t5_c" x="94" y="293" w="91" h="91"/>
             <target id="t6_c" x="328" y="294" w="91" h="91"/>
             <target id="t7" x="393" y="463" w="70" h="70"/>
             <target id="t8" x="344" y="214" w="70" h="70"/>
             <target id="t9_o" x="445" y="162" w="100" h="100"/>
             <target id="t10" x="591" y="132" w="70" h="70"/>
         </drag_and_drop_input>
         <answer type="loncapa/python">
             correct_answer = [{
                 'draggables': ['1', '2'],
                 'targets': ['t2', 't3', 't4' ],
                 'rule':'anyof'
             }]
             if draganddrop.grade(submission[0], correct_answer):
                 correct = ['correct']
             else:
                 correct = ['incorrect']
         </answer>
     </customresponse>
 </problem>


========
태그
========

* ``<customresponse>``: 문제가 사용자 지정 응답 문제임을 나타낸다.
* ``<drag_and_drop_input>``: 사용자 지정 응답 문제는 드래그 앤 드롭 문제임을 나타낸다.
* ``<draggable>``: 학습자 기본 이미지 위로 드래그 하는 단일 개체를 지정한다.
* ``<target>``: draggable이 끌어다 놓아야 하는 기본 이미지 위의 위치를 지정한다.

**Tag:** ``<drag_and_drop_input>``

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - img (필수사항)
       - 기본 이미지가 될 이미지의 상대적인 경로이다. 드래그 할 수 있는 모든 것은 다 이미지 위로 끌어 올 수 있다.
     * - target_outline
       - 윤곽선 (회색 파선)이 (대상이 지정된 경우) 대상 주변에 그려질 수 있는지 여부를 지정한다. 그것은 ‘true’ 또는 ‘false’ 가 될 수 있다. 지정되어 있지 않으면 그 대상은 윤곽선이 필요 없다.
     * - one_per_target
       - 하나 이상의 드래그 될 수 있는 것이 단일 대상에 놓여지도록 허용 여부를 지정한다. 그것은 ‘true’ 또는 ‘false’가 될 수 있다. 지정되어 있지 않으면 기본 값은 ‘true’이다.
     * - no_labels (필수)
       - 기본값은 false 이며, 라벨이 설정되지 않은 경우 기본 행동에서, 라벨은 id로부터 얻어진다. no_labels이 true 이면, 라벨은 id에서 자동으로 채워지지 않으며, 라벨을 설정할 수 없고, 단지 아이콘만 얻을 수 있다.

  Children

     * ``<draggable>``
     * ``<target>``

**Tag:** ``<draggable>``

드래그 앤 드롭 문제에서 단일의 드래그될 수 있는 개체를 지정한다.

이용자가 슬라이더로부터 끌어 기본 이미지 위에 놓아야만 하는 것이다. 끌기 작업 후, 드래그될 수 있는 것의 중심이 이미지의 직사각형 크기 밖에 있는 경우, 그것은 슬라이더로 반환될 것이다.

채점자가 작업하려면, 각각의 드래그 될 수 있는 것은 고유 ID를 가지고 있어야 한다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - id (필수)
       - 개체의 고유 식별자이다.
     * - label (선택)
       - 이용자에게 표시되는 텍스트 라벨이다.
     * - icon (선택)
       - 드래그 될 수 있는 것이 이미지라면, 이미지 파일에 대한 상대적 경로이다.
     * - can_reuse
       - true 또는 false, 기본값은 false이다. true 인 경우 같은 드래그는 여러 번 사용될 수 있다.

  Children

  (none)

**Tag:** ``<target>``

학습자가 드래그할 수 있는 항목을 끌어다 놓아야 하는 기본 이미지 위의 위치를 지정한다. 디자인에 따라, 드래그할 수 있는 항목의 중심이 대상 내에 있는 경우, (즉, [[x, y], [x + w, y + h]] 에 의해 정의된 사각형에서), 위치는 대상 내에 있다. 그렇지 않으면, 위치는 외부이다.

하나 이상의 대상을 지정하고, 학습자는 대상 외부에 있는 위치에 드래그할 항목을 놓아야 하는 경우, 드래그할 항목은 슬라이더로 반환된다.

대상을 지정하지 않으면, 학습자는 드래그할 항목을 기본 이미지의 아무 곳에 놓을 수 있다.

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - id (필수)
       - 대상 개체의 고유 식별자.
     * - x
       - 대상의 상단 왼쪽 모서리에 배치 될 기본 이미지상의 X-좌표.
     * - y
       - 대상의 상단 왼쪽 모서리에 배치 될 기본 이미지상의 Y-좌표.
     * - w
       - 픽셀로 대상의 너비.
     * - h
       - 픽셀로 대상의 높이.

  Children

  (none)

**********************
드래그가 가능한 대상
**********************

때때로 기본 이미지 상에서만 대상을 가지고, 이러한 대상에 대해서만 모두 드래그하는 것은 충분하지 않다. 드래그 할 자체가 대상 (또는 많은 대상)이 되어야 하는 복잡한 문제의 경우, 다음과 같은 확장된 구문이 사용될 수 있다.

::

    ...
    <draggable {attribute list}>
        <target {attribute list} />
        <target {attribute list} />
        <target {attribute list} />
        ...
    </draggable>
    ...

위의 태그에 있는 속성 목록 (``draggable`` and ``target``) 은 정상적인 ``draggable`` 및 ``target`` 태그와 동일하다. 유일한 차이점은 내부 대상 위치 좌표를 지정할 경우이다. (내부 대상을 포함하고 있는) 본래 드래그 가능한, 왼쪽 위 모서리에서 내부 대상의 오프셋을 설정 하려면 ``x`` 및 ``y`` 속성을 사용하도록 한다.


=====================================
드래그가 가능한 대상의 한계
=====================================

* 현재 드래그가 가능한 대상의 중첩 수준에 제한이 있다.

  비록 대상 자신이 드래그가 가능한지, 그런 대상이 많이 있더라도, 드래그 앤 드롭 문제는 대상의 최대 두 가지 수준만 있는 경우 채점될 것이다. 첫 번째 수준은 기본 대상이다. 그들은 기본 이미지에 부착된다. 두 번째 수준은 드래그가 가능하도록 정의된 대상이다.

* 또 다른 한계는 다른 대상에 대해 대상 범위가 확인되지 않는다는 것이다.

  대상이 서로 중복되지 않도록 확인해야 한다. 또한 드래그가 가능한 대상은 실제 본래 드래그의 대상보다 더 작아야 함을 확인해야 한다. 기술적으로 이것은 필수적이진 않지만 유용성 관점에서는 바람직하다.

* 기본 대상이 정의되어 있는 경우에만 드래그가 가능한 대상을 가질 수 있다 (기본 대상은 기본 이미지에 부착된다.).

  기본 대상이 없는 경우, 단일 수준의 중첩(기본 이미지에 대한 드래그)만을 가질 수 있다. 이 경우 사용자는 기본 이미지에 대한 각 드래블이 가능한 대상의 (x, y) 위치를 보고받을 것이다.


**********************
정답 양식
**********************

드래그가 가능한 대상에 대한 답안을 지정하려면, `Answer format for targets on draggables`_  를 참조하도록 한다.

두 가지 정답 양식이 있다: 짧은 양식과 긴 양식.

짧은 형식에서, 정답은 ``draggable_id`` 를 ``target_id`` 로 매핑(mapping)하는 것이다

    correct_answer = {'grass':     [[300, 200], 200], 'ant': [[500, 0], 200]}
    correct_answer = {'name4': 't1', '7': 't2'}

긴 형식에서, 정답은 dicts의 목록이다. 모든 dict는 세 가지 열쇠를 가진다
``draggables``, ``targets`` 및 ``rule``. 예를들면 ::

    correct_answer = [
    {
      'draggables':   ['7', '8'],
      'targets':  ['t5_c', 't6_c'],
      'rule': 'anyof'
    },
    {
      'draggables': ['1', '2'],
      'targets': ['t2_h', 't3_h', 't4_h', 't7_h', 't8_h', 't10_h'],
      'rule': 'anyof'
    }]

“드래그가 가능한 것”은 드래그가 가능한 대상들의 목록이다. “대상”은 드래그 되어야 하는 대상들의 목록이다.

.. Caution::
  ``correct_answer`` 목록 내부 dicts에 있는 드래그가 가능하도록 하는 것은 서로 교차하지 않아야 한다.

(draggable id 7에 대하여) 틀린 경우 ::

    correct_answer = [
    {
      'draggables':   ['7', '8'],
      'targets':  ['t5_c', 't6_c'],
      'rule': 'anyof'
    },
    {
      'draggables': ['7', '2'],
      'targets': ['t2_h', 't3_h', 't4_h', 't7_h', 't8_h', 't10_h'],
      'rule': 'anyof'
    }]

규칙은:

* ``exact``: ``user_answer`` 에 드래그가 가능한 대상들은 정답에 있는 대상과 동일하다. 예를 들어, ``correct_answer`` 이 다음과 같은 경우, 7과 8 에 대하여 드래그가 가능한 경우, 이용자는 대상1에 대해서는 7을 끌어 놓아야 하며, 대상2에 대해서는 8을 끌어 놓아야 한다 ::

    correct_answer = [
      {
      'draggables':   ['7', '8'],
      'targets':  ['tartget1', 'target2'],
      'rule': 'exact'
    }]


* ``unordered_equal``: •	순서 없이 대상으로 드래그될 수 있도록 한다. 대상1 또는 대상2에 대해 7을, 대상 2 또는 대상 1에 대해서 8을 끌어와야 하는 학습자를 위해, 7과 8은 다른 대상이어야 하며, 정답은 다음과 같아야 한다 ::

    correct_answer = [
    {
      'draggables':   ['7', '8'],
      'targets':  ['tartget1', 'target2'],
      'rule': 'unordered_equal'
    }]


* ``anyof``: •	모든 대상으로 드래그가 가능하도록 한다. 대상1 또는 대상2에 대해 7과 8을 끌어야 하는 학습자를 위해, 다음의 모두는 규칙anyof 에 따라 올바르다. ::

    correct_answer = [
    {
      'draggables':   ['7', '8'],
      'targets':  ['tartget1', 'target2'],
      'rule': 'anyof'
    }]

``can_reuse`` i이 true(참) 이면, 드래그가 가능한 대상은 a, b의 c 및 10개의 대상을 가지게 된다. 이것은 4개의 ``a`` 드래그 가능한 대상을  [``target1``,  ``target4``, ``target7``, ``target10``]; 로 끌 수 있도록 허용한다.  ``a`` 를 4 번을 쓸 필요가 없다. 또한 이렇게 하면 ``b`` 대상2 및 대상5에 대해 대상2 또는 대상5로 끌도록 허용할 것이다. ::

    correct_answer = [
        {
          'draggables': ['a'],
          'targets': ['target1',  'target4', 'target7', 'target10'],
          'rule': 'unordered_equal'
        },
        {
          'draggables': ['b'],
          'targets': ['target2', 'target5', 'target8'],
          'rule': 'anyof'
        },
        {
          'draggables': ['c'],
          'targets': ['target3', 'target6', 'target9'],
          'rule': 'unordered_equal'
        }]

가끔 학습자는 두개의  ``b`` 대상만을 끌 수 있도록 허용하기 원한다. 이 경우에  ``anyof+number`` 또는 ``unordered_equal+number`` 규칙을 사용해야 한다. ::

    correct_answer = [
        {
          'draggables': ['a', 'a', 'a'],
          'targets': ['target1',  'target4', 'target7'],
          'rule': 'unordered_equal+number'
        },
        {
          'draggables': ['b', 'b'],
          'targets': ['target2', 'target5', 'target8'],
          'rule': 'anyof+number'
        },
        {
          'draggables': ['c'],
          'targets': ['target3', 'target6', 'target9'],
          'rule': 'unordered_equal'
        }]

드래그가 가능한 대상의 동일한 수에 대해, 대상마다 여러 개의 드래그가 없다면 (one_per_target = ‘true’), ``anyof`` 는 ``unordered_equal`` 와 동일하다.

``can_reuse=true`` 인 경우, 긴 양식의 정답만을 사용해야 한다.

=======================================
드래그 가능한 대상에 대한 답안 양식
=======================================

위에서 설명한 경우와 같이, 답안은 각각의 드래그가 가능한 대상에 대한 정확한 위치를 제공해야 한다 (드래그가 가능한 대상이 놓여져야 하는 위치). 드래그가 가능한 대상이 그 자체가 드래그가 가능한 대상에 놓아야 하는 경우, 답안은 대상-드래그가 가능한 대상-을 포함해야 한다.

예를 들어, 3개의 드래그가 가능한 대상 - ``up``, ``s``, 및 ``p`` 을 가진다고 가정한다. 드래그가 가능한 대상은 ``s`` 와 ``p`` 는 자체에 대상을 가진다. 좀 더 구체적으로, ``p`` 는 세 개의 대상 - ``1``, ``2``, 및 ``3`` 을 가진다. 첫 번째 요구사항은 기본 이미지에 특정 대상에  ``s`` 와 ``p`` 를 배치하는 것이다. 두 번째 요구사항은 드래그가 가능한 대상 ``up`` 이   ``p`` 의 특정 대상에 배치되는 것이다. 아래는 문제에서 발췌된 부분이다. ::

    <draggable id="up" icon="/static/images/images_list/lcao-mo/up.png" can_reuse="true" />

    <draggable id="s" icon="/static/images/images_list/lcao-mo/orbital_single.png" label="s orbital" can_reuse="true" >
        <target id="1" x="0" y="0" w="32" h="32"/>
    </draggable>

    <draggable id="p" icon="/static/images/images_list/lcao-mo/orbital_triple.png" can_reuse="true" label="p orbital" >
      <target id="1" x="0" y="0" w="32" h="32"/>
      <target id="2" x="34" y="0" w="32" h="32"/>
      <target id="3" x="68" y="0" w="32" h="32"/>
    </draggable>

    ...

    correct_answer = [
        {
          'draggables': ['p'],
          'targets': ['p-left-target', 'p-right-target'],
          'rule': 'unordered_equal'
        },
        {
          'draggables': ['s'],
          'targets': ['s-left-target', 's-right-target'],
          'rule': 'unordered_equal'
        },
        {
          'draggables': ['up'],
          'targets': ['p-left-target[p][1]', 'p-left-target[p][2]', 'p-right-
             target[p][2]', 'p-right-target[p][3]',],
          'rule': 'unordered_equal'
        }
    ]

비록 드래그가 가능한 하나의 대상이 하나 이상의 사슬에 포함된 경우일지라도 모든 드래그가 가능한 대상에 대한 규칙을 지정해야 한다.


*************
채점 규칙
*************

#. 학습자의 답안과 정답은 같은 형식으로 분석된다.
   ::

    group_id: group_draggables, group_targets, group_rule

  ``group_id`` 는 서수이다. 정답에서 모든 dict에 대하여 증가하는 
  ``group_id`` 는 0, 1, 2,...로 할당된다.

  사용자 답안에서 드래그가 가능한 것은 정답의 똑같은 드래그 가능한 곳이 있는 group_id에 추가된다. ::

    If correct_draggables[group_0] = [t1, t2] then
    user_draggables[group_0] are all draggables t1 and t2 from the user answer:
    [t1] or [t1, t2] or [t1, t2, t2] etc..

#. 사용자 답안에서 모든 그룹에 대해, 해당 그룹의 드래그 가능에 대하여, 그룹 규칙에  ``number`` 가 있는 경우, set()이 적용된다. 규칙에  ``number`` 가 없으면, set은 적용되지 않는다. ::

    set() : [t1, t2, t3, t3] -> [t1, t2, ,t3]

  이 단계에서 모든 그룹에 대하여, 드래그 가능 목록은 동일한다.

#. 모든 그룹에 대하여, 대상 목록은 해당 그룹에 대한 규칙을 사용하여 비교된다.


==========================
Set 과  ``+number``
==========================

``set()`` 과 ``+number`` 는 재사용 가능한 드래그의 경우에 대해서만 필요하다. 다른 경우에는 목록에 동등한 드래그 가능 대상이 없으며 따라서 set()은 아무것도 하지 않는다.

* ``set()`` 작동은 “드래그 가능한 대상의 수는 어떤 수라도 대상에 끌 수 있다”의 경우에 대한 규칙을 만들 수 있도록 허용한다. ::

    {
      'draggables': ['draggable_1'],
      'targets': ['target3', 'target6', 'target9'],
      'rule': 'anyof'
    }

* 끌어다 놓을 수 있는 대상의 수를 정하고 싶을 때,  ``number`` •	규칙은 재사용 가능한 드래그의 경우에 대해 사용된다. 이 예제에서는 draggables_1의 두 가지 사례만이 끌어질 수 있다. ::

    {
      'draggables': ['draggable_1', 'draggable_1'],
      'targets': ['target3', 'target6', 'target9'],
      'rule': 'anyof+number'
    }


* ``exact`` 규칙을 사용할 때, 어떤 재사용 가능한 드래그가 어느 대상에 있는지 인식할 수 없기 때문에,  ``number`` 는 필요 없다. 예를 들면 ::

    {
      'draggables': ['draggable_1', 'draggable_1', 'draggable_2'],
      'targets': ['target3', 'target6', 'target9'],
      'rule': 'exact'
    }


    이 예를 제대로 다루기 위해 draggable_1 와 draggable_2 를 위해 다른 규정을 적용한다.

* ``unordered_equal`` (또는 ``exact``) 에 대하여, 대상 길이가 드래그 가능한 대상의 수에 대한 제약을 제공할 것이므로 그룹에 드래그 가능한 동일한 대상만 있는 경우,  ``number`` 는 필요 없다. ::

    {
      'draggables': ['draggable_1'],
      'targets': ['target3', 'target6', 'target9'],
      'rule': 'unordered_equal'
    }

  즉, ``draggable_1`` 만을 유일하게 끌어올 수 있다.

* 하지만 목록에 하나 이상의 다른 재사용 가능한 드래그를 가지는 경우, ``number`` 규칙을 사용할 수 있다. ::

    {
      'draggables': ['draggable_1', 'draggable_1', 'draggable_2'],
      'targets': ['target3', 'target6', 'target9'],
      'rule': 'unordered_equal+number'
    }

``number`` 를 사용하지 않는 경우, 드래그 가능 대상 목록은 
[``draggable_1``, ``draggable_2``]로 설정될 것이다.

