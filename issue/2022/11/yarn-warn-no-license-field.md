## 1. 상황

yarn 명령어를 실행 중, 다음과 같은 warning message를 만났다.
![](../../../public/images/yarn-warning-no-license.png)

## 2. 원인

../../../../ 경로에 있는 package.json 파일에 license field가 없다는 내용이다.\
전에 yarn을 통해 global 설치를 하면서, command를 `yarn add global [라이브러리]` 이처럼 잘못 입력하여 ../../../../ 경로에 package.json 파일이 생성된 것이다.

## 3. 방안

해당 경로로 이동하여 잘못 설치된 라이브러리를 제거하고, package.json 파일도 제거한다.

#### 3.1. 라이브러리 제거

- yarn remove global

#### 3.2. package.json 파일 제거

- rm -f package.json

## 4. 정리

## 5. 개념

```
참고 사이트: https://pages.michinobu.jp/t/yarnwarningnolicensefield.html
```
