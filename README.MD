# Typescript Programming

## 01. 타입스크립트와 개발 환경 만들기

<br>

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

<br>

---

<br>

## 02. 타입스크립트 프로젝트 생성과 관리

<br>

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
