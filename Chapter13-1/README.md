# 13장. 컴퓨터 보안

보안의 핵심은 여러분과 여러분의 물건을 여러분이 정의한 안전함에 따라 유지하는 것이다.
보안은 기술적인 문제만은 아니다. 사회적인 문제다.
여러분과 여러분의 물건, 그리고 여러분의 안전에 대한 정의는
모두 다른 사람과 다른 사람의 물건, 그들의 안전에 대한 정의와 균형을 맞춰야 한다. = 사회적 약속 또는 합의가 되어 있어야 한다.

보안은 여러분의 정보를 사적으로 유지하는 것으로부터 생겨난다. (비밀번호를 입력해야만 내 계죄에 접근할 수 있는 것 처럼)
요즘은 데이터 수집이 만연하기 때문에 여기저기 흩어져 있는 정보를 더 쉽게 연결할 수 있어서 프라이버시 보호가 더 힘들어졌다.
데이터 수집의 만연으로 인해 프라이버시를 지키는 일은 어려워지고 있고, 여러분의 보안은 점점 더 나빠지고 있다. 그럼 왜 점점 보안이 어려워지고 있는지를 살펴보도록 하자.

---

## 보안과 프라이버시 개요

### 위협 모델

위협 모델이란 보안이 필요한 대상 목록과 각 보안 대상에 가해질 수 있는 공격을 열거하여, 이런 공격을 방어하는 방법을 설계할 수 있게 한다. 그리고 위협 모델에 따라 적합한 방어를 설계해야 한다.
어떻게? 위협 모델을 잘 이해하는 것이 중요한데
얼마 만큼의 비용을 들여, 어느 정도 수준의 보안을 할 것인가를 계산하는 것이다.
사물함같은 경우, 경비원을 고용하여 철통방어를 한다면 안전하겠지만, 이것은 비용이 너무 많이 들고 학교 측에서는 이를 감당할 수 없을 것이다. 그리고 학교 사물함에는 보통 학생들이 귀가를 하고 나면 중요한 물건들은 없을 것이기 때문에 이렇게까지 큰 비용을 들여 보안을 하는 것 보다는 자물쇠를 사용하는 것 정도가 알맞을 수 있다.

컴퓨터 세계에서의 자멸적 보안 요소로는 복잡한 패턴의 패스워드를 예로 들 수 있다.
복잡한 패스워드 조합 패턴과 주기적으로 패스워드 변경을 유도하는 것은 결국 사용자가 스스로 쉽게 추측할 수 있는 패스워드를 선택해 사용하거나, 패스워드를 어딘가 메모해두도록 만든다.

결론은 위협과 위협에 대비한 방어 사이에 균형을 맞춰야 한다.
목표는 공격자가 통과하려면 비싸지만 방어자에겐 비용이 적게 드는 방어를 사용하는 것이다.
인터넷은 공격 비용은 극적으로 줄여주는데 방어 비용은 줄여주지 못한다는 부작용이 있다.

### 신뢰

위협 모델을 정할 때 가장 어려운 부분이 신뢰할 대상을 정하는 것이다.
컴퓨터 보안 세계에서 신뢰는, 여러분이 선택할 수는 없지만 의존해야 하는 대상을 가리키는 말이다.
(그러나 제어할 수 없는 대상을 신뢰할 때마다 보안은 감소하고, 신뢰할 대상을 추가할 때마다 보안은 더 악화된다.)
보안을 아주 높이기 위해선 꼭 필요한 대상만 신뢰해야 하지만 컴퓨터를 사용하면 수많은 서드파티 하드웨어나 소프트웨어에 의존해야 하며, 내가 이들을 신뢰하지 않더라도 사용하기 위해선 어쩔 수 없이 의존해야 한다.
이런 상황에서 지금으로서는 세 가지 유형의 신뢰 위반을 고려할 수 있다.

1. 의도적 : 소니 BMG의 루트킷 사건. 소니 BMG의 CD를 통해 사용자 컴퓨터에 루트킷이 설치되었던 문제를 가리킴. 루트킷은 소니가 cd 복제를 방지하게끔 만든 소프트웨어였으나, 사용자 동의 없이 설치된 점과 사용자의 컴퓨터 보안을 취약하게 만드는 점에서 문제가 되었음. 이처럼 의도적으로 신뢰를 위반한 경우.
2. 무능 : 지멘스는 자사 산업 제어 시스템 중 일부의 패스워드를 하드코딩했다. 이런 경우 해당 패스워드만 알아내면 누구든 제어 시스템에 접근할 수 있다. 이런 식의 보안 처리로 인한 사건들이 많았는데, 이것은 잘못될게 뭐 있겠어?라는 위협 모델이 모호성에 의한 보안이라는 사고 방식과 어우러진 것에 기인한다.
3. 부정직 : 미국 국립 표준 기술 연구소가 미국 국가 안보국에서 온 전문가의 도움을 받아 만든 암호 표준이 알고 보니 미국 국가안보국 전문가들이 의도적으로 표준을 약화시켰다는 것이 드러났다. 이런 식의 부정직함에 의한 신뢰 위반도 존재한다. ㄷㄷ
   신뢰 위반은 이와 같이 매우 흔하다. 이런 유형의 위반으로 인해 공격자가 비밀리에 안전하게 정보를 빼내는 경우를 표현하는 클렙토그래피(kleptography)라는 단어가 생겨났다. 사용자도 모르게 암호화되지 않은 정보를 빼낼 수 있게 하는 여러 가지 수단 또한 클렙토그래피 라고 한다.
   최근에는 CUP 아키텍처 설계 취약점을 이용한 스펙터/멜트다운 공격(유저 모드 프로그램이 OS 메모리 영역에 접근해 보안 정보를 읽는 공격), 취약점 공격 (시스템에 있는 취약점을 의도적으로 악용하는 공격)도 발견되었다.

#### 통신 보안

통신에서의 보안은 신뢰할 대상을 직접 보거나 고를 수 없다. 이럴 때 어떻게 나와 상대방의 거래가 안전하게 성립되었는지를 보장할 수 있을까?
이 문제의 해법은 크립토그래피다. 여러분과 여러분의 메시지를 받을 수신자만 아는 비밀코드를 사용해 암호화해서 보내면 수신자는 이것을 복호화 한다. 제대로 설계된 암호 시스템은 당사자 사이에 신뢰하는 요소의 수를 감소시킨다. 그래서 암호화되어 읽을 수 없는 통신 내용이 중간에 노출돼도 그리 큰 위험이 아니다.

#### 현대 - 보안이 점점 어려워지고 있는 이유?

연결된 컴퓨터 시대는 물리적 보안 문제를 통신 보안 문제와 결합시켰다.
인터넷상에서는 공격자가 더 이상 사람이 아니다. 프로그램이 공격한다. 공격자가 프로그램이기 때문에 매 초 수천번 여러분의 기계를 깨기 위한 공격을 시도한다.
공격에는 주로 두 가지 유형이 있다.
첫번째 공격 유형인 크립토그래피 시스템 공격은 상대적으로 드물고, 잘 설계된 시스템을 공격하기는 어렵다.
두번째 유형인 사회적 공격은 트릭을 써서 사용자가 자신의 컴퓨터에 소프트웨어를 직접 설치하게 만든다.
2009년, 온라인 뱅킹 취약점 공격은 누군가가 은행 계정에 로그인하면 그 계정의 돈을 공격자 계정으로 송금한 후 은행 사이트가 보여주는 웹 페이지를 고쳐서 송금 사실을 감추어 계정 주인이 눈치채지 못하게 한다. 이로 인해 종이로 된 은행 거래 명세서를 보지 않는 한, 공격을 눈치채기가 극히 어렵다.
현대 기술로 인해 어떤 것이 진본인지 결정하기가 점점 어려워지고 있는것도 문제다. 이제는 딥페이크라는 사실적인 사진, 오디오, 비디오를 만들어내기가 너무 쉬워졌기 때문이다.
SNS를 통해 여러분에 대한 메타데이터를 얻는 것 또한 쉬워졌다. 온라인 활동은 먼 곳에서도 추적할 수 있기 때문에 소수의 인력으로도 이것이 가능해졌다. 휴대폰 시스템 또한 여러분을 추적할 수 있게 만드는 요소이다.

이렇듯 현대에는 보안을 위협하는 요소가 산재해 있고, 보안을 위협하는 요소가 꼭 해커 뿐만이 아니라 기업, 국가가 될 수도 있다는 사실을 알아보았다.
그럼 어떻게 진정한 보안을 달성할 수 있을까?? 다음 분이 설명해주실거다.