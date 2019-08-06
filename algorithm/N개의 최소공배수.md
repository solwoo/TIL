## N개의 최소공배수



###### 문제 설명

두 수의 최소공배수(Least Common Multiple)란 입력된 두 수의 배수 중 공통이 되는 가장 작은 숫자를 의미합니다. 예를 들어 2와 7의 최소공배수는 14가 됩니다. 정의를 확장해서, n개의 수의 최소공배수는 n 개의 수들의 배수 중 공통이 되는 가장 작은 숫자가 됩니다. n개의 숫자를 담은 배열 arr이 입력되었을 때 이 수들의 최소공배수를 반환하는 함수, solution을 완성해 주세요.

##### 제한 사항

- arr은 길이 1이상, 15이하인 배열입니다.
- arr의 원소는 100 이하인 자연수입니다.

##### 입출력 예

| arr        | result |
| ---------- | ------ |
| [2,6,8,14] | 168    |
| [1,2,3]    | 6      |



나의 풀이 

<1st> 배열중 가장 큰 수를 기준으로 x1, x2, x3... 하며 나머지 원소들이 나누어 떨어지는지 계산한다.

```javascript
function solution(arr) {
  
  let maxNum = arr[arr.length - 1];
  let subMaxNum = maxNum;
  let result = false;
  
  function isTrue (currentValue) {
    return maxNum % currentValue === 0;
  }
  
  while(!reult) {
    result = arr.every(isTrue);
    maxNum += subMaxNum;
  }
  
  return maxNum - subMaxNum;
  
}
```



<2nd> 소인수분해를 이용하여 구한다. (실패!)

```javascript
function solution(arr) {
  arr.sort((a, b) => a-b);
  const maxNum = arr.pop();

  const result = (array, max) => {
    let commonMultiple = max;
    for(let el of array) { // 2, 6, 8
      let remainMax = max;
      let remainEl = el;
      if(max % el) {
        while(remainEl > 1) {
          console.log(remainEl);
          for(let i = 2; i * i <= max; i++) { // 해당 수의 sqrt
            if(el % i === 0) {
              if(remainMax % i === 0) {
                remainMax /= i;
                remainEl /= i;
                break;
              } else {
                remainEl /= i;
                commonMultiple *= i;
                break;
              }
            }
          }
        }
        commonMultiple *= remainEl;
      }
    }

    return commonMultiple;

  }

  return result(arr, maxNum);
  
}

console.log(solution([1,2,3]));
```

