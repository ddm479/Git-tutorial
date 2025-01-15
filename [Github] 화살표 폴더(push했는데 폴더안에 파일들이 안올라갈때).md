[Github] 화살표 폴더(push했는데 폴더안에 파일들이 안올라갈때)
문제점: github에 push했는데 화살표 폴더 모양이 보이고 폴더안에 파일들이 올라가지 않았다.
원인: .git폴더가 상위폴더에만 있어야 하는데 올라가지 않은 해당폴더(하위폴더)에도 있어서 그러하다. 리액트나 타입스크립트 프로젝트 생성할 때 npx create-react-app "폴더명" 명령어를 사용하는데 이러면 자동으로 .git폴더가 생성된다. 
해결방안: 해당폴더의 .git폴더 삭제

참고 블로그: https://velog.io/@ohhyunji/Github-%ED%99%94%EC%82%B4%ED%91%9C-%ED%8F%B4%EB%8D%94push%ED%96%88%EB%8A%94%EB%8D%B0-%ED%8C%8C%EC%9D%BC-%EC%95%88%EC%97%90-%EB%82%B4%EC%9A%A9%EC%9D%B4-%EC%95%88%EC%98%AC%EB%9D%BC%EA%B0%88%EB%95%8C
