# GO 언어를 이용한 HTTP 1.1 클라이언트 구현

<details>
   <summary>
      1. Keep-Alive는 기본적으로 유효합니다. 다만 통신이 완료 된 뒤에도 세션을 유지를 시킬려면 client에서 꼭 절차는 무엇일까요?
   </summary>

   - reponse.Body를 끝가지 읽고난 후에 닫아야 됩니다.
</details>

<details>
   <summary>
      2. 증명서를 만드는 기본 흐름은 어떻게 되나요?
   </summary>

   1. OpenSSL 커멘트로 비밀 키 파일을 만든다
   2. 인증서 요청 파일을 만든다.
   3. 인증서 요청 파일에 서명해서 인증서를 만든다.
</details>
   