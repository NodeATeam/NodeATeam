# NodeATeam
cli 사용법

지갑 복구
.\gaiacli.exe keys add icowellet --recover
  - 사용할 비밀번호 입력
  - 사용할 비밀번호 입력확인
  - 시드키 입력
  
지갑 주소 확인
.\gaiacli.exe keys list

지갑 잔고 확인
.\gaiacli.exe q account [지갑주소] --chain-id=cosmosbub-1 --node cosmos-public.nodeateam.com:26657

위임
gaiacli tx staking redelegate [FROM-VALIDATOR-ADDR] [TO-VALIDATOR-ADDR] [AMOUNT] --fees [FEES] --from [KEYNAME] --chain-id [CHAIN-ID] --node [NODE]

ex.
.\gaiacli.exe tx staking delegate cosmosvaloper14l0fp639yudfl46zauvv8rkzjgd4u0zk2aseys 1000000utom --fees 1000000uatom --from ico --chain-id cosmoshub-1 --node cosmos-public.nodeateam.com:26657

[FROM-VALIDATOR-ADDR] : 기존 검증인 주소(cosmosvaloper로시작)

[TO-VALIDATOR-ADDR] : 위임하고자 하는 검증인의 검증인주소를 입력(cosmosvaloper로 시작되는 주소)

(ATEAM 검증인주소 = cosmosvaloper14l0fp639yudfl46zauvv8rkzjgd4u0zk2aseys)

[AMOUNT] : 위임금액을 uatom으로 입력(1atom = 1000000uatom, 메인넷예:1000000uatom)

[FEES] : 지출할 fee를 uatom으로 입력(메인넷 예:100000uatom)(gaia-13001 테스트넷 예:200000photino)

[KEYNAME] : 사용할 지갑의 key 이름 입력

[CHAIN-ID] : 체인ID(메인넷 예:cosmoshub-1)
