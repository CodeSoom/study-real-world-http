# HTTP/2의 신택스: 프로토콜 재정의

<details>
    <summary>
        1. HTTP/2에서 HTTP/1.1으로부터 무엇이 제일 달라졌는가?
    </summary>
  
  - 데이터표현
    1. 스트림을 사용해 바이너리 데이터를 다중으로 송신하는 구조로 변경했다.
    2. 스트림 내 우선 순위 설정과 서버 사이드에서 데이터 통신을 하는 서버 사이드 푸시를  구현했다.
    3. 헤더가 압축하게 되었다.
</details>

<details>
    <summary>
        2. HTTP/2에서 변경된 프로토콜 기반은 무엇인가? 그로서 장점은 무엇인가?
    </summary>

  - 바이너리 기반 프로토콜
  - 병렬 처리가 쉬워졌다.
  - socket layer에서 데이터를 프레임단위로 쉽게 분리할 수 있으므로, 수신측 TPC 소켓의 버퍼를 빠르게 비울 수 있고, 통신 상대에게 다음 데이터를 고속으로 요청할 수 있습니다.
</details>

<details>
    <summary>
        3. 플로 컨트롤은 어디에 이용되는 통신량 제어 처리인가? 무엇을 방지하는가?
    </summary>

  - 스트림을 효율적으로 흐르게 할려 할 떄
  - 통신 속도가 지나치게 차이나는 기기의 조합으로 통신할 때 빠른 쪽이 느린 쪽에 대량으로  패킷을 보내버려 처리할 수 없게 되는 사태를 방지
</details>

<details>
    <summary>
        4. 서버 푸시는 어는 용도로 사용되는가? 클라이언트에서 요구하기 전에 컨텐츠를 전송하는 방법은?
    </summary>

- CSS와 자바사크립트, 이미지 등 웹페이지를 구성하는 파일을 다운로드하는 용도로 이용.
- 푸시된 컨텐츠를 캐시에 넣는다. 사용자는 요청을 안해도 캐시로 인해 다운로드 된 것처럼  볼 수 있다.
</details>

<details>
    <summary>
        5. 헤더는 어떤 방식으로 압축되는가? 다른 압축 알고리즘들과의 차별점은 무엇인가?
    </summary>

  - HPack 방식
  - 사전에 외부 사전을 가지고 있다.
  - 동적 테이블에서 HTTP 헤더를 인덱스한 값만으로 표현 할 수 있으므로 보다 작은 크기로  송신화 가능
</details>

<details>
    <summary>
        6. HTTP/2의 전신은 무엇인가?
    </summary>

  - 구글에서 개발한 SPDY라는 대체 프로토콜
  - 개발했던 이유:
  - 그동안 HTTP가 개선해온 전송 속도를 한층 더 향상시키기 위해서
</details>

<details>
    <summary>
       7. Fetch API의 특징은 무엇인가?
    </summary>

  - XMLHttpRequest보다 오리진 서버 밖으로의 엑세스 등 CORS 제어가 쉬원진다.
  - 자바스크립트의 ㅗ던한 비동기 처리 작성 기법인 프로미스를 따른다.
  - 캐시를 세밀하게 제어할 수 있다.
  - 리퍼러 정책을 설정할 수 있다.
  - Service Worker 내에서 이용할 수 있다. 
    - XMLHttpsRequest로는 할 수 없는 일 중 제일 큰 포션
</details>

<details>
    <summary>
        8. server-sent events는 이벤트 전송을 어떻게 제공하는가?
    </summary>

  - 코멧의 롱 폴링과 청크 읍답을 조합한 방식으로. 
  - 이벤트 스트림으로라도 불리며, MIME Type은 text/event-stream입니다.
</details>

<details>
    <summary>
        9. 웹소켓은 무엇을 실현 시켜주는가?
    </summary>

  - 서버/클라이언트 사이에 오버헤드가 적은 양반향 통신을 실현합니다.   
  > OverHead wiki 정의:
  > any combination of excess or indirect computation time, memory, bandwidth, or  other resources that are required to perform a specific task.
</details>

<details>
    <summary>
        10. 웹소켓이 HTTP 기반 프로토콜과 다른점은?
    </summary>

  - 스테이트풀 통신 
</details>

<details>
    <summary>
        11. Socket.IO의 장점은
    </summary>

  - 웹소켓을 사용할 수 없을 떄는 XMLHttpRequest에 의한 롱 폴링으로 에뮬리이션해, 서버에서의 송신을 실현하는 기능이있다.
  - 웹소켓 단절 시 자동으로 재접속한다.
  - 클라이언트뿐만아니라 서버에서 사용 할 수있는 구현동 ㅣㅆ어, 클라이언트가 기대하는 절차로 폴백인 XMLHttpRequest 통신을 핸들링할 수 있다.
  - 로비 기능
</details>

<details>
    <summary>
         12. WebRTC(Web Real-Time Communication) 브라우저와 서버의 통신 이외에 어디에 사용될 수 있는가?
    </summary>

  - 서버를 사용하지 않는 브라우저끼리의 P2P 통신
</details>

<details>
    <summary>
        13. HTTP 웹 푸시는 오프라인 상태에서도 사용자에게 알림을 보낼 수 있는 통신을 할 수 있는가?
    </summary>

   - Service Worker
    - 브라우저의 HTML 렌더링 기능
    - 웹 서버와 프런트엔드 중간에 있는 프록시 서버와 같은 존재.
</details>

  













