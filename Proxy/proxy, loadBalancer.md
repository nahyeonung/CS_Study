# proxy, loadBalancer

### Proxy

- 대리, 대용물 ⇒ 남을 대신해서 일을 처리한다는 의미 정도로 해석하면 된다.

### Proxy Server

- 서버와 클라이언트 간의 중계 서버로서 통신을 대신 수행하는 역할
- 캐시/보안/트래픽 분산 등 여러 장점을 가질 수 있다.

시각적으로 표현하면 다음과 같다.

![](https://github.com/nahyeonung/CS_Study/blob/main/images/proxyServer.png)

### Proxy Server 종류

- Foward Proxy
- Reverse Proxy

### Foward Proxy

- 클라이언트 대신 서버에 요청을 보내주는 역할

![](https://github.com/nahyeonung/CS_Study/blob/main/images/fowardProxy.png)

### Foward Proxy 이점

- 캐싱 ⇒ 클라이언트가 요청했던 데이터를 front proxy에 저장한 후 같은 데이터를 요청하면 서버단을 거치지 않고 response ⇒ 전송 시간 절약, 외부 요청 감소
- 익명성 ⇒ 클라이언트의 정보를 감추고 마치 프록시의 정보인 것처럼 서버에 전송 ⇒ 서버가 받은 IP는 클라이언트 IP가 아닌 proxy IP

### Reverse Proxy

- 서버 대신 클라이언트에 응답을 보내주는 역할

![](https://github.com/nahyeonung/CS_Study/blob/main/images/reverseProxy.png)

### Reverse Proxy 이점

- 캐싱 ⇒ Foward Proxy 캐싱과 동일
- 보안 ⇒ 서버 정보를 클라언트로부터 숨김 ⇒ client는 Reverse Proxy를 실제 서버라고 생각하여 요청 ⇒ 실제 서버의 IP가 노출되지 않음
- 로드 밸런싱(중요!!!!!!!!!)

### 로드 밸런싱(Load Balancing)

- 부하분산, 즉 해야할 작업을 나누어 서버의 부하를 분산시키는 것<span style="color:red">(apache server의 c10k 문제를 보완하기 위한 방법)</span>

### 로드 밸런서(Load Balancer)

- 여러 대의 서버가 분산 처리할 수 있도록 요청을 나누어주는 서비스

![](https://github.com/nahyeonung/CS_Study/blob/main/images/loadBalancer.png)

### 로드 밸런서 종류

- L2
- L3
- L4 ⇒ 전송계층에서의 로드밸런싱
- L7 ⇒  응용계층에서의 로드밸런싱(ex. url)