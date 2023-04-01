# Computer Network
-----------------
## 1강 정리
#### Application Layer

<br/><br/>


- ### HTTP (Hyper Text Transfer Protocol) :
*Web은 HTTP의 별칭* <br/>
- >W3 상에서 정보를 주고 받을 수 있는 프로토콜<br/>
 주로 문서를 주고 받으며 TCP를 사용함.<br/>
 TCP는 reliable trasport 하기 떄문에 패킷의 손실없이 송수신가능<br/>
대신 UDP보다 비싼 비용을 내야함. Network resource에 대한 비용.<br/>
 HTTP/3 부터는 UDP를 사용.<br/>
Client <--> Server 간 요청,응답 프로토콜로 구성됨.<br/>
굉장히 단순한 프로토콜. 저장 등 다른 기능이 없음.
<br/><br/>

 - #### W3 (World Wide Web) :
 
  인터넷에 연결된 컴퓨터를 통해 사람들이 정보를 공유할 수 있는 전세계적 정보 공간
<br/><br/>

- #### 인터넷 프로토콜 슈트(영어: Internet Protocol Suite) : 

인터넷에서 컴퓨터들이 서로 정보를 주고받는 데 쓰이는 통신규약(프로토콜)의 모음이다. 인터넷 프로토콜 슈트 중 TCP와 IP가 가장 많이 쓰이기 때문에 TCP/IP 프로토콜 슈트라고도 불린다.
<br/><br/>

- #### TCP와 IP
    - > UDP : unreliable, connectionless, no flow control, no congestion control<br/>
    - > TCP : reliable, connection-oriented, flow control, congestion control<br/>

TCP/IP는 패킷 통신 방식의 인터넷 프로토콜인 IP (인터넷 프로토콜)와 전송 조절 프로토콜인 TCP (전송 제어 프로토콜)로 이루어져 있다.<br/> IP는 패킷 전달 여부를 보증하지 않고, 패킷을 보낸 순서와 받는 순서가 다를 수 있다.(unreliable datagram service)<br/>TCP는 IP 위에서 동작하는 프로토콜로, 데이터의 전달을 보증하고 보낸 순서대로 받게 해준다.<br/> HTTP, FTP, SMTP 등 TCP를 기반으로 한 많은 수의 애플리케이션 프로토콜들이 IP 위에서 동작하기 때문에, 묶어서 TCP/IP로 부르기도 한다.
<br/><br/>

- #### TCP (Transmission Control Protocol):  
전송제어 프로토콜
    IP(Internet Protocol Suite)의 핵심.
    TCP/IP라고도 부름
     TCP는 근거리 통신망이나 인트라넷, 인터넷에 연결된 컴퓨터에서 실행되는 프로그램 간에 일련의 옥텟을 안정적으로, 순서대로, 에러없이 교환할 수 있게 한다. TCP는 전송 계층에 위치한다.
<br/><br/>


- #### UDP 사용자 데이터그램 프로토콜(User Datagram Protocol) :  

인터넷 프로토콜 스위트의 주요 프로토콜 가운데 하나

<br/><br/>




패킷스위칭의 단점 :  너무 많은 양의 데이터가 라우터에 할당되면
1. 큐에서 대기하는 시간. 딜레이가 늘어남
2. 큐에 공간이 없어서 패킷유실이 일어남

현재 인터넷상에서 유실되는 99.9% 는 패킷스위칭의 과부하.

<br/><br/>



<br/><br/>

 - Server 와 Client

 client는 뭔가를 필요로 할 때 Action을 취함

 server는 항상 같은 위치에서 기다려야함 = 고정된 주소
 <br/>
 Program을 OS 위에서 실행시키면 Process가 된다.
 process 사이의 communication을 할 때
 <br/><br/>
 <br/>
 엄청나게 많은 process중에서 단 하나를 찾아야함.
 <br/>
Socket interface : OS에서 inter-process-communication을 위해 만들어준 구멍



-> IP주소를 통해 addressing 만으로는 부족 (건물 정도로 생각)

->  port number (한 건물안의 호실 정도로 생각)



**process들 사이의 communication**
process를 어떻게 addressing을 하느냐?
ip주소와 port number의 결합으로 만든 socket으로 addressing한다!

### application 계층 :
OS에서 제공하는 (transport 계층에서 제공) 정보를 받는다. 하지만 신뢰성 이외의 어떠한 기능도 아래계층에서 해주지 않고 있다.
 
 보안개념이 없다.
보안은 결국 어플리케이션 계층에서 담당하게 됨.

-  internet transport protocols services

    1. TCP service : **reliable transport** between sending process와 receiving process (flow control, congestion control  제공)
    2. UDP service : **unreliable data** transfer between sending and receiving process

**가장 큰 차이는 신뢰성 유무**


### 




클라이언트, 웹브라우저가 HTTP request message 를 보내기 위해서는 TCP connection이 먼저 생성되어야 한다.<br/>
즉, TCP connection message를 먼저 주고받아야한다.


*프로토콜의 이름을 먼저 이해하고 프로토콜에서 사용하는 format,field(header...등등)을 이해하기.*<br/>
*쿠키 :  웹사이트에서 사용자에게 부여한 번호. 추적당하는 것*

-  cache 캐시 

데이터를 미리 복사해놓는 임시 장소를 가리킴
    1. 다시 계산하는 시간 절약
    2. 캐시에 접근하는 시간이  원래 data에 접근하는 시간보다 짧을 떄 사용


Web caches = proxy server
goal : satisfy client request without involving origin

-  프록시서버 : 

클라이언트가 자신을 통해 다른 네트워크 서비스에 간접적으로 접속할 수 있게 
해주는 컴퓨터시 스템, 응용 프로그램

-----------------

## 2강 정리

*cache가 생기면 인터넷이 빨라진다.*
 
 HTTP 설명 끝.
트래픽 등등 여러가지 문제 발생 - >  캐시를 두거나 계층화 
- #### DNS(domain name system)
host domain name - IP address(network address) 의  column

이 큰 DATA base를 관리하기 위해 server를 분산, 계층화 시켜놓음.
관리가 용이 + 검색이 빠르게...


#### TLD (top-level domain) servers : <br/>
com, org, net, edu, aero, jobs, and all top-level country domains
<br/>

#### Authoritative DNS servers : <br/>
organization's own DNS servers, proiding authoritatve hostname to IP mappings for organization's named hosts

컴퓨터의 IP주소 존재 -> 컴퓨터의 이름은 있을수도 없을수도 있다.

- > TCP는 준비동작이 필요,대신 유실될 수 있다. X<br/>
그래서 DNS 는 UDP 소켓으로 작동한다. - > UDP가 빠르니까, 근데 유실 가능성이 있다.<br/>
DNS에서 송수신하는 메세지 자체는 매우 작다.<br/>
host name과address 등등이
유실되도 작은 메세지 이므로 리스크가 작다.<br/>
통화를 1분 할건데 전화번호 알아내는게 1분걸린다?? TCP<br/>
전화번호 알아내는데 빠르다! UDP

----


## 3강 정리

- Socket 이란?
process 와 process 사이에 메세지 교환을 할 때(network programming을 하고자 할 때) <br/>process 와 process 사이의 interface가 존재해야함. 이것이 Socket !<br/>
프로세스는 컴퓨터에서 연속적으로 실행되고 있는 컴퓨터 프로그램<br/>

### OS가 운영체제가 제공하는 2가지 서비스<br/>
TCP , UDP 두가지 각각 Socket이 존재함

- TCP : sock-stream
- UDP : sock-dgram

운영체제에서 제공하는 시스템<br/>
웹 클라이언트와 웹 서버

bind시킨다 = matching시킨다

### TCP server
1.  socket() : create an endpoint for communication
2.  bind() : assign a local protocol address to the socket
3. listen() : make socket a passive socket, waiting for connection request
4. accept() : extract the first connection request on the queue of pending connections, create a new connected socket, and return a new file descriptor referring to that socket, (blocks until connection from client is established)
5. connect() : initiate a connection on a socket
6. read() : read data from a file descriptor
7. process request

### TCP client
- socket()
- connect()
- write()

#### Function :
- socket : int domain, int type, int protocol
- bind : int sockfd, struct sockaddr *my_addr, int addrlen
- listen : int sockfd, int backlog(여러 클라이언트로부터 동시에 접속을 받을 때 처리)
- accept : int sockfd, struct sockaddr *addr, int *addrlen
- connect : int sockfd, struct sockaddr *serv_addr, int addrlen
- read : int fd, void *buf, size_t count
- write : int fd, const void *buf, size_t count

----------------

## 4강 정리
- e-mail : <br/>
1. user agent
2. mail server
3. simple mail transfer protocol (SMTP) (mail access protocols)


보내는 서버와 받는 서버가 따로 존재한다.<br/>

**user client   --SMTP-->  sender server  --SMTP-->  receiver server --SMTP-->  user client**

### Transprot layer
**Applincation layer 바로 밑에 존재 - 조금 더 구체화되어 있다.**<br/>

**TCP 혹은 UDP segment를 상대방 TCP,UDP 쪽으로 전달**

- > HTTP와 같은 Application layer의 전송단위를 Message라고 부른다.<br/>
이 Message가 Socket을 통해 내려오게 되면 Transport layer의 전송단위인 Segment로 들어간다.<br/>
TCP와 UDP는 segment이다. segement는 header와 data로 구성되어 있다.<br/>
이 때 Message는  data부분으로 들어가게 되고 header에는 TCP와 UDP의 port number가 들어간다.(전송하기 위한 부가적인 설명)<br/>
Network later로 내려오게 되면 IP packet이 되고, IP packet은 header와 data로 구성되어 있다.<br/>이 때 segment는 packet의 data부분으로 들어가게 된다.<br/>
Link layer로 내려오게 되면 frame이 되고, frame은 header와 data로 구성되어 있고 IP packet은 frame의 data부분에 들어가게 된다.<br/>

1. Application layer의 전송단위 : Message
2. Transport layer의 전송단위 : Segment
    - Segment : header + data(Message)
3. Network layer의 전송단위 : IP packet
    - IP packet : header + data(Segment)
4. Link layer의 전송단위 : frame
    - frame : header + data(IP packet)

/*TCP는 UDP에 비해 기능이 많다.*/ <br/>
**공통 기능 : multiplexing, demultiplexing**<br/>
Process에서 message를 보냈을 때 알맞는 목적지 process에 전달해주는 것이 multiplexing/demultipexing이다.<br/>

- UDP : Connectionless demuxing<br/>
socket과 socket 사이 1:1대응이 아니다. <br/>
source port와 destination port가 같은지 확인하고 전달한다.<br/>

- TCP : Connection-oriented demuxing<br/>
socket과 socket 사이 1:1대응이다. <br/>
두 socket끼리 연결되어있다. <br/>
TCP socket들은 고유의 번호를 가지는게 아니라 고유의 index,ID를 가진다.<br/>
    - TCP ID = Source IP address + source port 번호 + destination IP address + destination port 번호<br/>

- > Socket과 Port는 같은 개념이 아니다.<br/>
하나의 process가 여러개의 socket을 가질 수 있다.<br/>
sender의 ip, port, receiver의 ip, port 조합 -> 유일하게 한 개!<br/>

