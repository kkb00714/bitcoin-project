# bitcoin-project

-----------------

    ※ 비트코인
        => 개인과 개인의 전자 화폐 시스템


    ※ 이중 지불에 대한 문제가 존재
        - 이중 지불이란? 


    ※ 블록체인이란?
    => 데이터들이 연결되어 있는 형태
    
    - 블록은 크게 거래정보와 이전 블록에 대해 담겨있음

    (거래정보) => 특정 시간동안 블록체잉ㄴ 사용자들이 비트코인을 전송하는 등의 정보가 담겨있고

    (이전블록) => 블록(직전의 거래 정보) 에 대한 정보를 담고있음

        => 이렇게 차곡차곡 쌓인 정보들을 블록체인을 운영하는 노드라고 하는 컴퓨터가 서로 나누어 가지면서 하나의 블록체인 네트워크가 구성됨.

    ※ 블록체인은 중앙 집권화된 서버가 없이, 누구나 노드를 운영할 수 있는 컴퓨터만 있으면 참여할 수 있는 탈 중앙화된 개인과 개인간의 거래 시스템을 만들 수 있음.

    
    ※ 특징
        - 탈중앙화 : 중앙 집권하고 있는 형태가 아닌, 노드만 운영할 수 있으면 참여할 수 있는 것.

        - 보안성 : 악의적인 목적을 가지고 노드를 운영하는 사람이 있다면, 블록체인 네트워크로부터 배제될 것.

            +) 51% Attack! 
            => 작업증명 (PoW) 알고리즘에서 나오는 용어!
            => 블록체인 전체 연산량의 50% 이상을 보유한 채굴자는 압도적인 채굴량을 바탕으로 전체 네트워크를 마음대로 결정할 수 있게 되어 51% 공격을 감행할 수 있다는 의미

            참조) https://steemit.com/kr/@brownbears/51-attack

        - 투명성 : 누구나 노드에 참여할 수 있음 (누구나 블록을 볼 수 있다는 것) => 매우 중요한 블록체인의 특징. 

        - 확장성 : 누구나 참여자가 될 수 있지만, 개선을 통해 더 좋은 블록체인을 만들 수 있다는 의미! 


    ※ 해시(hash)
        => 함수는 특정한 값을 넣었을 때, 특정한 결괏값이 나오는 것
        => 해시함수는 조금 특별한 알고리즘을 통해 값을 출력

        - 특징
            => 해시함수를 돌렸을 때, 항상 같은 길이의 데이터가 출력됨
            => 역산이 되지 않는 단방향 함수. 해시값으로부터 원래의 값을 얻어낼 수 없음. 


    ※ 블록 생성 과정
        => 다양한 거래에 관한 요청 발생 
        => 거래 내역 하나하나를 해시함수를 통해서 해시값으로 변환 (거래 해시값 생성)
        => 거래 해시값을 묶어서 다시 한 번 해시 진행
        => 이 때, 거래 갯수가 홀수인 경우, 마지막 거래를 한번 더 복사하여 해시값을 만듦.
        => 이러한 과정을 반복하면 단 하나의 해시값이 남게 되는데, 이를 머클루트 해시값이라고 함. 
        => 생성된 머클루트 해시값을 블록에 저장. (새로운 블록이 탄생)


    ※ 블록에는 머클루트 해시값 외에도, 블록의 소프트웨어 버전, 이전블록 해시, 블록 생성 시간, 난이도, Nonce 값 등을 가지게 됨


    ※ 채굴이란? 
    => ~(최?근 그래픽카드의 가격을 상승시킨 주범.....)~  블록 생성과정을 거쳐 만들어진 블록은 채굴 과정을 통해 검증 절차에 들어감
    => 블록 생성 시간, 난이도, Nonce에 따라 영향을 받아 채굴을 진행

    ※ 블록의 구조
        - 현재 블록 해시
        - 블록 헤더
        - 거래 개수
        - 블록 바디

    -------------------

    ※ 채굴 (Mining)
    => 생성된 블록을 검증해 나가는 것을 채구링라고 함
    => 채굴에 성공한 채굴자에게 가상화폐를 지급함으로써 보다 적극적으로 채굴이라는 활동에 동참하도록 함

        ※ Nonce 값 찾기 
            => 블록체인에서 목표값 이하의 블록 해시를 찾기 위해 임시로 사용하는 숫자. (임시값이라고도 함)
            참조) https://ziwookim.tistory.com/65

        ※ 비트코인에서는 이러한 채굴행위를 통해 생성되는 블록의 시간을 10분으로 맞춰둠. (10분 이상: 난이도 하락 / 10분 이하 : 난이도 상승)


    ※ Proof Of Work (PoW) : 작업 증명 방식
    => CPU 동작이 한 번 작업증명을 충족하는 데 동원됐다면, 해당 블록은 작업을 재수행하지 않고는 변경될 수 없음.

    => 만일 다수의 CPU 파워가 정직한 노드에 의해 통제된다면, 가장 정직한 사슬이 가장 빠르게 늘어나 다른 경쟁 사슬을 압도(outpace) 할 것.

    ※ Proof Of Stake (PoS): 지분 증명 방식
    => 블록을 검증하는 방식을 지분을 통해 결정하는 방식.

    ※ PoW vs PoS
    => 검증 방식  <검증 방식>  지분 증명
    => 전력 소비 많음  <전력 소비>  전력 소비 적음
    => 컴퓨터 파워  <네트워크 지분>  가상화폐 보유량 
    => 가상 화폐  <통화>  가상화폐


    -------------------


    ※ 2세대 블록체인, 이더리움
    => 차세대 스마트 컨트랙트와 탈중앙화된 어플리케이션 플랫폼

    ※ 비트코인의 한계점

    => TPS(Transaction Per Second) : 초당 처리할 수 있는 거래량
    => Bitcoin : 7TPS

    ※ 스마트 컨트랙트
    => 계약 시 중개인이 필요 없도록 하는 것
    => 코드에 내용이 명시되어 있고, 해당 내용은 한 번 저장되면 수정할 수 없는 블록체인에 저장됨 (따라서 중개인이 필요없음)

    ※ 이더리움이 제공하려는 것은 완벽한 튜링완전(turing-complete) 프로그래밍 언어가 심어진 블록체인

    ※ Decentralized Application (Dapp)
    => 블록체인 상에서 제공되는 서비스


    -------------------


    ※ 탈중앙화 앱, Dapp
    => 서비스를 블록체인으로부터 제공받게 됨. 즉, 블록체인으로부터 서비스를 제공받는 어플리케이션.

    ※ 특징
        - 서비스에도 블록체인의 특징이 잘 반영되어 있음
        ex) DeFi (탈중앙화 금융), 
        PancakeSwap(사용자로부터 가상화폐 환전 서비스를 제공 => 이 때 발생한 수수료를 가상화폐를 맡긴 사람들에게 나누어주는 방식)
        
    ※ Decentralized Autonomous Organization (DAO, 탈 중앙화 자율 조직)
    
    ※ Company vs DAO
        - 수직적 구조   <조직 구조>   수평적 구조

        - 법   <의사 결정 규약>   코드(스마트 컨트랙트)
        
        - 중앙 집권, 간접 민주주의   <의사 결정 구조>   분산형 거버넌스, 직접 민주주의

        - 기존 화폐   <거래 방식>   암호화폐, NFT

    ※ DAO's deilemma 
        - 특정 몇 명이 토큰을 독점한다면 기존의 자본주의 체제와 차이가 없음

        - 개발자, 컨텐츠 제공자, 사용자가 모두 공평하게 토큰을 나누어 가지고 있으면 책임 소재가 불분명해짐. 


    -------------------


    ※ Wallet(지갑) 
    => 블록체인에 존재하는 가상화폐를 보관하는 지갑

    ※ 블록체인에 존재하는 가상화폐에 접근할 수 있는 일종의 접근 권한이 바로 Wallet(지갑)

    ※ 대칭키 방식
        - 하나의 key 값을 주고 암호화 및 복호화를 진행
        => key를 탈취당할 경우 심각한 보안문제 

    ※ 공개키, 개인키 방식
        - 암호화 할 때는 공개키 사용, 복호화 시에는 개인키 사용
        

    ※ Wallet 종류 간단하게

        - Paper Wallet : Key값을 종이에 적어서 보관하는 방법
            => 보관만 잘 할 수 있다면 상당히 안정적인 방법 

        - Cold Wallet : USB와 비슷한 형태로 되어있음. (인터넷과 단절되어 있음)
            => 가상화폐를 사용할 때마다 따로 연결해주어야 해서 불편.

        - Hot Wallet : 네트워크가 연결되어있는 PC, 모바일에 설치해서 사용.
            => 탈취의 위험성이 있지만 간편한 사용이 장점

        - BitGo

    ※ 메타마스크 지갑 설치

    ※ 니모닉(Mnemonic) : 개인키를 단어들로 바꿔서 외우기 간편하게 만들어주는 기능

        - 니모닉 작동 방식

        => 개인키를 12개로 분할
        => 0000부터 1111까지의 알파벳 순서가 존재하는 사전이 존재
        => 12개의 key를 하나하나 사전의 단어와 매칭하여 12개의 단어 조합을 만듦

        => 따라서 니모닉은 순서가 존재!!


    ※ Public Key가 있는데, 일종의 계좌번호와 같음

    ※ Account detail 에서 qr코드를 사용하여 가상화폐를 입금받을 수 있음
    => 개인 키 표시 버튼을 눌러서 비밀번호를 입력하면 Private Key를 볼 수 있음. ※ 단!! 절대 노출되어서는 안 됨 ※

    ※ Polygon Chain
    => 이더리움과 같은 환경으로 되어있는 체인
        참고) 이더리움이 아닌 체인(Solana)도 있음 (이더리움 킬러라는 별명도 있음)


    ※ Faucet 을 사용하여 실습용 가상화폐를 제공받을 수 있음

    ※ 이더리움이 제공하려는 것은 완벽한 튜링완전(turing-complete) 프로그래밍 언어가 심어진 블록체인 


    -------------------


    ※ EVM (Etherium virtual Machine) - 환경
    

