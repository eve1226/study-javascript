## 1. 배열 선언
```js
const arr1 = [1,2];
const arr2 = new Array();
```

## 2. 배열 위치
```js
const fruits = ['🍎', '🍌']
console.log(fruits); // 🍎🍌
console.log(fruits.length); // 2
console.log(fruits[0]); // 배열의 첫번째
console.log(fruits[1]); // 배열의 두번째
console.log(fruits[2]); // 배열의 세번째 값이 없으면 undefined
console.log(fruits[fruits.length - 1]); // 배열은 0부터 시작 총개수-1하면 마지막 배열 선택
console.clear();
```


## 3. 불러오기
* for
```js
for(let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```
* for of
```
for(let aaa of fruits) {
  console.log(aaa);
}
```
* forEach
```js
fruits.forEach(function (fruit, index, array) {  // forEach에는 fruit, index, array의 세가지 인자를 받아올 수 있다
  console.log(fruit, index, array);
});
// 아래와 같이 위 문장의 function문장과 중괄호를 생략 할 수 있음
fruits.forEach((fruit, index, array) => console.log(fruit, index, array));
fruits.forEach((fruit) => console.log(fruit));
```
## 4. 데이터 추가하기 
* push
```js
fruits.push('🍓','🍑') //마지막 배열로 추가됨
console.log(fruits);
```
* pop
```js
fruits.pop(); // 뒤에서 부터 삭제
console.log(fruits);
fruits.pop();
console.log(fruits);
delete (fruits[0]);   // delete로 지우면 공간은 남아 있고 데이터만 삭제됨
```

## 5. 앞에서 부터 데이터 추가하기 
* unshift
```js
fruits.unshift('🍓','🍋');
console.log(fruits);

// 앞에서 부터 데이터 지우기 shift: remove an item from the benigging
fruits.shift();
console.log(fruits);
fruits.shift();
console.log(fruits);

// 참고! 언시프트와 시프트로 데이터를 삭제하고 추가하는 방법은 팝 과 푸시를 사용하는거 보다 느리다 
```

## 6. 지정해서 지우기 
* splice
```js
fruits.push('🍓','🍑','🍋')
console.log(fruits);
fruits.splice(0, 1) // 첫번째 데이터 하나만 삭제 
console.log(fruits);
fruits.splice(1, 2) // 두번쨰 데이터부터 두개 삭제
console.log(fruits);
fruits.splice(1, 1,'🍆','🌶') // 두번째 데이터 하나만 삭제 후 가지와 고추를 추가 할 수 있다
console.log(fruits);
```

## 7. 배열과 배열의 연결!!
* concat
```js
const fruits2 = ['🍔', '🍕']
console.log(fruits2);
const newFruits = fruits.concat(fruits2);
console.log(newFruits);
```
## 8. 검색
* indexOf
```js
console.clear();
console.log(fruits);
console.log(fruits.indexOf('🍌')); // 결과값 0 (바나나가 몇번째 배열에 있는지 확인)
console.log(fruits.indexOf('🍖')); // 결과값 -1 (없는 데이터 검색시 -1로 나옴)
```
* includes
```js
console.log(fruits.includes('🍖')); // true와 false 로 결과 데이터 유무를 확인 할 수 있음
console.log(fruits.includes('🍌')); // 결과값 true
```
* astIndexOf
```js
console.clear();
fruits.push('🍎');
fruits.unshift('🍎');
console.log(fruits); // 맨앞과 맨뒤에 중복된 데이터가 있을 시 
console.log(fruits.lastIndexOf('🍎')); // 결과값 5  (LastIndexOf 는 중복된 데이터 중 마지막 데이터 위치를 찾아줌)
```
