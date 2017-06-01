====================================
간편 편집기에서 힌트 설정하기
====================================

간편 편집기에서 다음과 같이 힌트를 설정할 수 있다.

::

  ||Hint 1||
  ||Hint 2||
  ||Hint n||

.. note:: 
  힌트 수에 제한은 없으며 학습자는 한번에 하나의 힌트를 보고 힌트를 다시 눌러서 다음 힌트를 볼 수 있다.


예를 들어 다음 문제는 힌트가 두 개 있다.

::

  ||A fruit is the fertilized ovary from a flower.||
  ||A fruit contains seeds of the plant.||

======================================
고급 편집기에서 힌트 설정하기
======================================

고급 편집기에서 ``<demandhint>`` 요소 내의 ``<hint>`` 요소에서 힌트를 설정한다.

.. code-block:: xml

  <demandhint>
    <hint>Hint 1</hint>
    <hint>Hint 2</hint>
    <hint>Hint 3</hint>
  </demandhint>

예를 들어 다음 XML은 힌트를 두 개 보여준다.

.. code-block:: xml

  <demandhint>
    <hint>A fruit is the fertilized ovary from a flower.</hint>
    <hint>A fruit contains seeds of the plant.</hint>
  </demandhint>
