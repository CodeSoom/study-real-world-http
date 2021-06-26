# HTTP/2의 시맨틱스: 새로운 활용 사례


<details>
   <summary>
      1. 픽셀 비율은 어떻게 계산되는가?
   </summary>

   * 논리 해상도와 물리해상도의 비율
</details>

<details>
   <summary>
      2. 시맨틱 웹에서 HTTP로 텍스트를 전달하면 의미를 다룬다는 것은?
   </summary>

* 페이지에 포함된 정보를 분석해서 정보를 집약하거나 검색하는 과정을 사람 손을 거치지 않게 하는 것.
</details>

<details>
   <summary>
      3. 시맨틱 웹세계에서 어떤 관계성 안에서 의미를 기술하려하는가?
   </summary>

   - 주어
   - 술어
   - 목적어
   - 3개를 통틀어 트러플이라 지칭
</details>

<details>
   <summary>
      4. AMP(Accelearted Mobile Page)는 어는 콘텐츠에 적합한가?
   </summary>

   - 정적 웹 콘텐츠
     - 뉴스
     - 요리법
     - 영화목록
     - 제품 페이지
     - 리뷰 
     - 동영상
     - 블로그 
     - etc...
</details>

<details>
   <summary>
      5. AMP가 빠른 비밀은?
   </summary>

   - 크롤러 또는 스파이더가 AMP 페이지가 있는 것을 인식하면, 모든 내용을 구굴의 배포 전용 고속 캐시 서버(CDN: 콘텐츠 전송 네트워크)에 복사.
   - 페이지 구성을 고정화함으로써 페이지 로딩의 고속화를 달성
   - 페이지 구성이 고정화되므로 CDN 지원이 쉬어졌다.
   - 콘텐츠를 CDN 쪾에 업로드함으로써 자바스크립트 파일을 캐시에 올리기 쉬워졌다
   - 콘텐츠를 서버 쪽에 업로드할 때 태그를 수정해 고속화가 이루어졌다.
   ※각각의 기능들은 개별 기술이지만 서로 연동하여 작동한다 라잌 톱니바퀴.
</details>

<details>
   <summary>
      6. HLS(HTTP Live Streaming)의 장점과 단점?
   </summary>

   - 장점
   - 전세계 라우터가 지원하는 HTTP를 사용 할 수 있다.
   - 일반 웹서버와 동일한 서버 및 CDN을 사용 할 수 있다.
   - 단점
     - 청크별로 다운로드가 끝나지 앟으면, 재생이 시작되지 않으므로 지연이 발생.
     - 지원되지 않는 환경이 많다.
     - 콘텐츠 보호 DRM(Digital Rights Management)에 제약이 있다.
</details>

<details>
   <summary>
      7. MPEG-DASH(Dynamic Adaptive Streaming ove HTTP)와 HLS의 재생 벙법의 차이는?
   </summary>

  - HLS
     - 브라우저 자체에서 HLS의 .m3u8 파일을 해석해서 재생하는 시스템이 포함되있다.
     - 미디어 플레이어 프레임워크를 이용하여 브라우저 이외에서도 재상 할 수 있음.
   - MPEG-DASH
     - 데이터분석은 자바스크립트로
     - 동영상 재생은 브라우저의 고덱을 자바스크립트에서 다루는 API, HTML5 Media Source Extensions을 이용
</details>



