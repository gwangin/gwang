# Computer Network
- cache 캐시 :데이터를 미리 복사해놓는 임시 장소를 가리킴
    1. 다시 계산하는 시간 절약
    2. 캐시에 접근하는 시간이  원래 data에 접근하는 시간보다 짧을 떄 사용
- HTTP (Hyper Text Transfer Protocol) : W3 상에서 정보를 주고 받을 수 있는 프로토콜
 주로 문서를 주고 받으며 TCP를 사용함.
 HTTP/3 부터는 UDP를 사용.
Client <--> Server 간 요청,응답 프로토콜로 구성됨.

 - W3 (World Wide Web) : 인터넷에 연결된 컴퓨터를 통해 사람들이 정보를 공유할 수 있는 전세계적 정보 공간

 - TCP (Transmission Control Protocol): 전송제어 프로토콜
    IP(Internet Protocol Suite)의 핵심.
    TCP/IP라고도 부름
     TCP는 근거리 통신망이나 인트라넷, 인터넷에 연결된 컴퓨터에서 실행되는 프로그램 간에 일련의 옥텟을 안정적으로, 순서대로, 에러없이 교환할 수 있게 한다. TCP는 전송 계층에 위치한다.

     TCP와 IP
TCP/IP는 패킷 통신 방식의 인터넷 프로토콜인 IP (인터넷 프로토콜)와 전송 조절 프로토콜인 TCP (전송 제어 프로토콜)로 이루어져 있다. IP는 패킷 전달 여부를 보증하지 않고, 패킷을 보낸 순서와 받는 순서가 다를 수 있다.(unreliable datagram service) TCP는 IP 위에서 동작하는 프로토콜로, 데이터의 전달을 보증하고 보낸 순서대로 받게 해준다. HTTP, FTP, SMTP 등 TCP를 기반으로 한 많은 수의 애플리케이션 프로토콜들이 IP 위에서 동작하기 때문에, 묶어서 TCP/IP로 부르기도 한다.

-  인터넷 프로토콜 스위트(영어: Internet Protocol Suite)는 인터넷에서 컴퓨터들이 서로 정보를 주고받는 데 쓰이는 통신규약(프로토콜)의 모음이다. 인터넷 프로토콜 슈트 중 TCP와 IP가 가장 많이 쓰이기 때문에 TCP/IP 프로토콜 슈트라고도 불린다.

- UDP 사용자 데이터그램 프로토콜(User Datagram Protocol) :  인터넷 프로토콜 스위트의 주요 프로토콜 가운데 하나


- 프록시서버 : 클라이언트가 자신을 통해 다른 네트워크 서비스에 간접적으로 접속할 수 있게 해주는 컴퓨터시 스템, 응용 프로그램


패킷스위칭의 단점 :  너무 많은 양의 데이터가 라우터에 할당되면
1. 큐에서 대기하는 시간. 딜레이가 늘어남
2. 큐에 공간이 없어서 패킷유실이 일어남

현재 인터넷상에서 유실되는 99.9% 는 패킷스위칭의 과부하.

 application 계층 관점

 메세지가 어떤 라우터를 거처가며 어떤 패킷유실을 일으키는지 아직은 생각하지 않는다.

 Server 와 Client

 client는 뭔가를 필요로 할 때 Action을 취함

 server는 항상 같은 위치에서 기다려야함 = 고정된 주소
 
 process 사이의 communication

 Program을 OS 위에서 실행시키면 Process가 된다.

Socket interface : OS에서 inter-process-communication을 위해 만들어준 구멍

엄청나게 많은 process중에서 단 하나를 찾아야함.

-> IP주소를 통해 addressing 만으로는 부족 (건물 정도로 생각)

->  port number (한 건물안의 호실 정도로 생각)

