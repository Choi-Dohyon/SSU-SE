# Markdown 확장 구문 알아보기

## 목차
> 1. [표 만들기](#표-만들기)
>
> 2. [체크리스트 만들기](#체크리스트-만들기)
>
> 3. [취소선](#취소선)
>
> 4. [자동 링크](#자동-링크)
>
> 5. [인용문](#인용문)

## 표 만들기  

</br>

확장 구문에서는 표를 만드는 것도 가능합니다.

다음과 같이 작성하면 표가 만들어집니다.

    |     | 1 번 | 2 번 | 3 번 |
    | --- | --- | --- | --- |
    | 철수 |  O  |  X  |  O  |
    | 영희 |  X  |  X  |  O  |
    | 민수 |  O  |  O  |  O  |

ex1 )

|     | 1 번 | 2 번 | 3 번 |
| --- | --- | --- | --- |
| 철수 |  O  |  X  |  O  |
| 영희 |  X  |  X  |  O  |
| 민수 |  O  |  O  |  O  |

| 문자로 둘러쌓인 부분을 셀이라고 합니다. 셀에는 표에 넣을 내용을 적으면 됩니다.

그리고 `| --- | --- | --- | --- |` 이렇게 첫번째 행과 나머지 행들을 나누는 두번째 행이 있습니다.

이 두번째 행이 있어야 비로소 표가 만들어집니다.

</br>

표를 만드는 법을 더 자세히 알아봅시다.

        |     | 1 번 | 2 번 | 3 번 |
        :--: | ------: | :- | --- 
        철수 |  O  |  X  |  O  |
        | 영희 |  X  |  X  |  O  
        민수 |  O  |  O  |  O  

ex2 )

|     | 1 번 | 2 번 | 3 번 |
:--: | ------: | :- | --- 
철수 |  O  |  X  |  O  |
| 영희 |  X  |  X  |  O  
민수 |  O  |  O  |  O  

ex2를 통해 알 수 있는 점은 다음과 같습니다.

> 1. 맨 앞 또는 맨 뒤에 있는 | 문자는 사용하지 않아도 됩니다.
>
> 2. 2번째 행에 들어가는 - 문자의 길이는 상관없습니다.
>
> 3. 2번째 행에서 : 문자를 사용해 셀들의 위치를 정렬할 수 있습니다.
>       * -의 좌측에 :을 붙이면 좌측 정렬
>       * -의 우측에 :을 붙이면 우측 정렬
>       * -의 양옆에 :을 붙이면 가운데 정렬

</br>

* **주의사항**
    * 첫번째 행과 두번째 행의 셀의 갯수는 같아야 합니다.
    * 첫번째 행과 두번째 행보다 셀의 갯수가 적은 행은 나머지 부분이 빈 셀로 채워집니다.
    * 첫번째 행과 두번째 행보다 셀의 갯수가 많은 행은 초과된만큼 셀이 삭제됩니다.

## 체크리스트 만들기

</br>

체크된 목록과 체크되지 않은 목록을 한 번에 볼 수 있는 체크리스트를 만들어 봅시다.

    - [x] 양파
    - [ ] 당근
    - [ ] 고추
    - [x] 마늘

ex1 )
- [x] 양파
- [ ] 당근
- [ ] 고추
- [x] 마늘

ex1을 보면 `- [x]` 표시가 된 항목은 체크가 되어 있고, `- [ ]` 표시가 된 항목은 체크가 되어 있지 않은 걸 알 수 있습니다.

</br>

리스트와 마찬가지로 체크리스트 안에 체크리스트를 넣는 것 또한 가능합니다.

    - [x] 양파
    - [ ] 당근
    - [ ] 고추
    - [x] 마늘
        - [ ] 통마늘
        - [x] 다진 마늘

## 취소선

</br>

Markdown에서 취소선을 쓰는 방법을 알아봅시다.

두 개의 물결표(~)로 텍스트를 감싸면 취소선을 만들 수 있습니다.

    ~~취소선~~ 사용하기  
    
~~취소선~~ 사용하기

* **주의사항**
    취소선은 같은 단락 내에서 물결표를 사용해야 취소선이 만들어집니다.
    
    다음과 같이 작성해도 취소선은 만들어지지 않습니다.
    
        그는 ~~그녀와
        
        함께~~ 거리를 걷고있었다.
        
## 자동 링크

</br>

기본 구문에서는 링크를 생성하기 위해서 몇몇작업이 필요했지만, 확장 구문에서는 자동으로 링크를 생성되게 할 수 있습니다.

    www.google.com
    
    http://google.com
    
    https://google.com
 
ex1 ) 

> www.google.com
>
> http://google.com
>    
> https://google.com

`www.`, `http://`, 또는 `https://` 뒤에 알파벳, 숫자, _ 문자, - 문자로 이루어진 주소를 적으면 링크가 생성됩니다.

</br>

자동 링크 뒤에 다음과 같은 문자들이 붙어있어도 링크 주소에 포함되지 않습니다.

> - ?
> 
> - !
> 
> - .
> 
> - ,
> 
> - :
> 
> - \*
> 
> - _
> 
> - ~

ex2 ) www.google.com?

ex2처럼 말이죠.

</br>

자동 링크가 ' ) ' 문자로 끝나면 링크 전체의 괄호 갯수를 검사하게 됩니다.

- > ex3 ) www.google.com/search?q=(markdown)
  >
  > ex3의 경우에는 ' ( ' 문자와 ' ) ' 문자의 갯수가 같으므로 **(markdown)의 검색 화면** 링크가 생성됩나다.

- > ex4 ) www.google.com/search?q=((markdown))
  >
  > ex4도 마찬가지로 **((markdown))의 검색 화면** 링크가 생성됩니다.

- > ex5 ) www.google.com/search?q=(mark)down)
  >
  > 하지만 ex5처럼 ' ) ' 문자가 더 많으면 링크 맨 뒤의 ' ) ' 문자는 링크에 포함되지 않습니다.
  >
  > 그래서 **(mark)down의 검색 화면** 링크가 생성됩니다.

</br>

이번에는 자동링크가 ' ; ' 문자로 끝나는 경우입니다.

자동 링크에 ' & ' 라는 문자가 포함되어 있고, ' & ' 문자와 ' ; ' 문자 사이가 알파벳으로 구성이 되어 있다면

' & ' 문자부터 ' ; ' 문자까지는 링크에 포함되지 않습니다.

ex6 ) www.google.com/search?q=markdown&abcdef;

</br>

오토링크에 ' < ' 문자가 있으면 그 부분부터는 링크에 포함되지 않습니다.

ex7 ) www.google.com</search?q=markdown

ex7의 링크는 markdown의 검색 화면이 아닌 구글 홈페이지로 연결됩니다.

</br>

