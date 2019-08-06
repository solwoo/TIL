## display: grid;

#### grid-column-start

: <integer> / span <integer>

<integer> <= 포함하고 시작함

<integer>은 칸이 아닌 선을 가르킨다.



#### grid-column-end

: <integer> / span <integer>

해당 숫자는 비포함 < <integer>



=> start 와 end 는 바뀔 수 있음. 그럴때는 두 개의 역할이 교환된다.



#### grid-column

: grid-column-start && grid-column-end



#### grid-row

: grid-column 과 동일하다.



#### grid-area

: grid-column && grid-row



#### order

: 하나의 grid를 기준으로 order를 정할 수 있다. 사용법은 z-index와 동일하다.



#### grid-template-columns

: <length> / <percentage> / <flex> / max-content / min-content / minmax(min, max)

fractional = fr

각 fr 단위들은 사용가능한 공간을 하나로 공유하여 할당한다. 

Ex) 1fr 3fr 로 설정시, 공간이 4개의 동일한 크기로 공유된다.



#### grid-template-rows

: grid-template-columns 와 동일



#### grid-template

: grid-template-columns && grid-template-rows



