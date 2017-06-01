.. _Annotation:

###################
주석 문제
###################

.. note:: K-MOOC은 이 문제 유형에 대해 부분적 지원을 제공한다.

주석 문제에서 교수자는 텍스트 블록내의 특정 텍스트를 강조 표시한 다음, 강조된 텍스트에 대한 질문을 한다. 학습자가 강조 표시된 텍스트 위로 마우스를 움직일 때 질문이 나타난다. 또한 질문은 학습자의 응답 칸과 함께 텍스트 블록 아래 부분에 나타난다.


.. image:: ../../../shared/images/AnnotationExample.png
  :alt: An example annotation problem.

.. contents::
  :local:
  :depth: 1

*****************************
주석 문제 설정
*****************************

주석 문제를 추가하기 전에 Studio에서 주석 문제를 설정해야 한다.

Studio에서 주석 문제를 설정하기 위해 **고급 설정** 페이지에서 ``"annotatable"`` 키를 **고급 모듈 목록** 에 추가한다. (키 값은 반드시 “ “ 사이에 입력해야 한다) 자세한 사항은 :ref:`Enable Additional Exercises and Tools` 을 참고하면 된다.


****************************
주석 문제 만들기
****************************

주석 문제를 만들려면 주석 고급 구성 요소를 강좌에 추가하고, **문제의 지침** 및 **토의 안내** 부분을 추가한 다음, 문제의 **주석 문제** 부분을 추가해야 한다.

============================================
지침 및 토의 안내 추가하기
============================================

**문제의 지침 및 토의 안내** 부분을 추가하려면,


#. 문제를 만들려고 하는 학습활동에서 신규 구성요소 추가 아래에 **고급** 을 클릭한다.

#. 문제 유형 목록에서 **주석** 을 클릭한다

#. 표시되는 구성 요소에서 **편집** 을 클릭한다.

#. 구성요소 편집기에서, 예제 코드를 본인의 코드로 바꾼다.

#. **저장** 을 클릭한다.


=================================
주석 문제 추가
=================================

**주석 문제** 부분 추가를 위해

#. 주석 구성요소에서, 새로운 빈 고급 문제 구성 요소를 만든다.

#. 고급 문제 구성요소에서 다음 코드를 붙여 넣고 본인의 정보로 직접 대체한다.

   .. code-block:: xml

       <problem>
           <annotationresponse>
               <annotationinput>
                 <text>PLACEHOLDER: Text of annotation</text>
                   <comment>PLACEHOLDER: Text of question</comment>
                   <comment_prompt>PLACEHOLDER: Type your response below:</comment_prompt>
                   <tag_prompt>PLACEHOLDER: In your response to this question, which tag below do you choose?</tag_prompt>
                 <options>
                   <option choice="incorrect">PLACEHOLDER: Incorrect answer (to make this option a correct or partially correct answer, change choice="incorrect" to choice="correct" or choice="partially-correct")</option>
                   <option choice="correct">PLACEHOLDER: Correct answer (to make this option an incorrect or partially correct answer, change choice="correct" to choice="incorrect" or choice="partially-correct")</option>
                   <option choice="partially-correct">PLACEHOLDER: Partially correct answer (to make this option a correct or partially correct answer, change choice="partially-correct" to choice="correct" or choice="incorrect")
                   </option>
                 </options>
               </annotationinput>
           </annotationresponse>
           <solution>
             <p>PLACEHOLDER: Detailed explanation of solution</p>
           </solution>
         </problem>

#. **저장** 을 클릭한다.
