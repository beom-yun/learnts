# Typescript Programming

typescript 설치

```bash
$ npm i -g typescript
$ tsc --version
```

ts-node 설치

```bash
$ npm i -g ts-node
$ ts-node -v
```

- tsc : ts 코드를 js 코드로 변환, node 명령어로 js 실행해야 함
- ts-node : ES5로 변환 + 실행

package.json 생성

```bash
$ npm init --y
```

<br>

|   npm i 옵션   | 의미                                                                                        |
| :------------: | :------------------------------------------------------------------------------------------ |
|   --save[-S]   | 프로젝트 실행할 때 필요한 패키지로 설치, package.json 파일의 'dependencies' 항목에 등록     |
| --save-dev[-D] | 프로젝트 개발할 때만 필요한 패키지로 설치, package.json 파일의 'devDpendencies' 항목에 등록 |

<br>

@types/node 설치 (Promise와 같은 타입을 사용하기위함)

```bash
$ npm i -D @types/node
```

다른 사람이 작성한 프로젝트를 전달받아 이용할 시, 가장 먼저 package.json 파일이 있는 디렉토리에서 다음 명령을 실행

```bash
$ npm i
```

tsconfig.json 생성

```bash
$ tsc --init
```

- tsconfig.json : 타입스크립트 컴파일러의 설정 파일

비구조화 할당 & 잔여 연산자

```ts
let address: any = {
  country: "Korea"
  city: 'Seoul'
  address1: 'Gangnam-gu'
  address2: 'Sinsa-dong 123-456'
  address3: '789 street, 2 Fllor ABC building'
};
const { country, city, ...detail } = address  // ... 잔여연산자

console.log(detail)
// { address1: 'Gangnam-gu'
//   address2: 'Sinsa-dong 123-456'
//   address3: '789 street, 2 Fllor ABC building' }
```

전개 연산자

- 여러 객체를 merge한 새로운 객체를 만들 때 사용

```ts
let part1 = { name: "jane" },
let part2 = { age: 22 },
let part3 = { city: "Seoul", country: "Kr" };
let merged = { ...part1, ...part2, ...part3 };  // ... 전개연산자

console.log(merged);
// { name: 'jane', age: 22, city: 'Seoul', country: 'Kr' }
```
