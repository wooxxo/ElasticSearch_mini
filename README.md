## 💳 우리카드 실제 데이터 분석을 통한 잠재 고객 유치 전략
**우리카드의 실제 카드 데이터**를 기반으로 소비 패턴을 분석하여 인사이트를 도출한 프로젝트입니다.

`Elasticsearch`와 `Kibana`를 활용하여 **대규모 카드 데이터를 분석**하고, 이를 **시각화**하였습니다.


## 👥 Contributors
|       배기영       |       권순재        |      양규리        |       우승연       |
| :-----------------: | :-----------------: | :----------------: | :----------------: |
| [<img width="160px" src="https://github.com/bbky323.png">](https://github.com/bbky323) | [<img width="160px" src="https://github.com/Soooonnn.png">](https://github.com/Soooonnn) | [<img width="160px" src="https://github.com/ygreee0320.png">](https://github.com/ygreee0320) | [<img width="160px" src="https://github.com/wooxxo.png">](https://github.com/wooxxo) |
| [@bbky323](https://github.com/bbky323) | [@Soooonnn](https://github.com/Soooonnn) | [@ygreee0320](https://github.com/ygreee0320) | [@wooxxo](https://github.com/wooxxo) |


## 🛠 Tech Stack
<div>
<img src="https://img.shields.io/badge/elasticsearch-3db9ac?style=for-the-badge&logo=elasticsearch&logoColor=white"> 
<img src="https://img.shields.io/badge/kibana-f04e98?style=for-the-badge&logo=kibana&logoColor=white">   
<img src="https://img.shields.io/badge/duckDB-FCC624?style=for-the-badge&logo=duckdb&logoColor=black"> 
</div>

---

## 📖 배경 및 필요성
### 잠재고객이란?
- 디지털 채널에 가입하지 않았으나, 실물 카드는 사용하는 사용자: 아날로그 진성 고객
- 디지털 채널에 가입은 했으나 이용하지 않고, 카드는 사용하는 사용자: 디지털 휴면(Dormant) 고객


**📉 우리카드, 회원수 감소 지속**
> 우리카드가 전업 카드사 중 유일하게 신용카드 전체 회원수 감소 추세가 지속되고 있는 것으로 나타났다. 
업계 관계자는 "신규 신용카드 회원 유치는 실제 카드사 수익과 직결되고 본업 경쟁력을 가늠할 수 있다"며 "카드사 입장에서는 신규 회원 유치에 온 힘을 쏟을 수 밖에 없다”고 말했다.

- 출처 : 시사저널e([https://www.sisajournal-e.com/news](https://www.sisajournal-e.com/news/articleView.html?idxno=410112))

**모집비용 절감 카드는 우리…신용판매로 위기 돌파**
> 마이데이터 서비스를 통해 우리WON카드 회원을 확보하고 이탈은 방지해 모집비용 절감 효과를 내겠다는 복안이다.
우리카드 측은 "마이데이터 기반으로 차별화된 상품 추천과 서비스 제공을 할 예정"이라고 설명했다.

- 출처: https://www.ibtomato.com/mobile/mView.aspx?no=11933

**계열사 서비스 한곳에… 우리금융 ‘WON뱅킹’ 종합금융 승부**
> “우리WON뱅킹은 … 통합해 마케팅 비용을 줄이고 효율성을 높일 수 있다.”
“우리금융은 고객 데이터를 활용한 맞춤형 마케팅을 지속하겠다는 계획이다.”

- 출처: https://www.asiatoday.co.kr/kn/view.php?key=20251015010003825

위와 같이 회원 수가 감소하는 상황속에서, 이탈을 막고 충성 고객으로 전환할 수 있는 잠재 고객 유치는 매우 중요하며,
고객이 디지털 채널에 가입함으로써 이를 해결할 수 있다고 판단했습니다.

### 🔑 고객이 디지털 채널에 가입함으로써 얻을 수 있는 이점
1. **행동 데이터 확보**
    1. 고객의 행동 데이터를 확보하여 니즈를 파악한 후, 상황에 맞게 대출 등 상품 권유 가능
    2. 예시) “A씨가 앱에 들어와서 '자동차 대출' 상품을 3초간 보다가 나갔네?", "마이데이터를 보니 요즘 주식 투자를 의 앱 유입을 유도

- **여성 타겟**: "생활 밀착형 베네핏 큐레이터" (Retail & Life) → 신규 가입자 유치
	- 앱을 **생활비 절약 비서**로 포지셔닝
	- 디지털 채널 솔루션: "핫딜 & 생활비 분석" 대시보드
		- 서비스: 우리WON카드 앱 내 주요 마트(이마트, 홈플러스 등) 및 온라인 몰의 실시간 할인 정보를 제공
		- Action: 가계 관리 비중이 높은 3050 여성을 위해 특정 마트 할인 쿠폰을 앱 내에서만 단독 증정
		- 마케팅: "장바구니 물가 방어 완료" 혹은 "자녀 병원비 페이백 적립 완료" 등의 감성적이고 실용적인 메시지를 활용하여 여성 사용자의 앱 유입을 유도

