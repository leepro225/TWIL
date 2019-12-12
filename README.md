# TWIL
today what I learn

▶ 값의 깊은 복사와 얕은 복사
const object1 = {
  a: 1,
  b: 2,
};

const object2 = Object.assign({}, object1, {a: 100});

console.log(object2.a); //100
console.log(object2.b); //2

이렇게 하면 복합형의 깊은 복사가 가능하지만, 객체의 값이 복합형인 경우 그 복합형은 얕은 복사가 되는 한계가 있음.
그럴경우 스프레드 연산자를 사용

const original = { a : {b : 2}};
let copy = {...original};
copy.a.b = 100; 
console.log(original.a.b);  //expected: 2 but actual: 100

http://hochulshin.com/javascript-best-deepcopy/
