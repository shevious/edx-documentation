.. _Adding Tooltips to a Problem:

==============================
문제에 말풍선 추가하기
==============================

학습자가 개념이나 문제를 잘 이해할 수 있도록 말풍선을 추가할 수 있다. 말풍선은 말풍선 아이콘 위로 마우스를 가져갔을 때 학습자에게 보여진다.

다음 예는 두가지 말풍선을 보여준다. “ROI”의 정의를 보여주는 말풍선이 보여지고 있다.

.. image:: ../../../shared/images/tooltip.png
 :alt: An example of a tooltip from a learner's point of view.
 :width: 500

.. note::
  스크린 리더를 이용하는 학습자에게 말풍선은 스크린 리더가 말풍선에 고정되었을 때 보여진다.

말풍선 추가를 위해 보여질 텍스트를  ``clarification`` 요소로 감싼다. 예를 들어 다음 문제는 두 가지 말풍선이 있다.

.. code-block:: xml

  <problem>
      <text>
          <p>Given the data in Table 7 <clarification>Table 7: "Example PV
            Installation Costs", Page 171 of Roberts textbook</clarification>,
            compute the ROI <clarification><strong>ROI</strong>: Return on
            Investment</clarification> over 20 years.
          </p>
       . . .
