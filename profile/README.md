## K-Stable & WearHouse

**쇼핑몰 + 월렛 + 결제 네트워크 + 블록체인**


### Repository Map

- [`wearhouse-fe`](https://github.com/K-Stable/wearhouse-fe)  
  구매자(고객)용 프론트엔드

- [`wearhouse-seller-fe`](https://github.com/K-Stable/wearhouse-seller-fe)  
  판매자/운영자용 프론트엔드

- [`wearhouse-be`](https://github.com/K-Stable/wearhouse-be)  
  쇼핑몰 백엔드 

- [`wallet`](https://github.com/K-Stable/wallet)  
  Wallet App(iOS/Flutter) + Wallet Web + Wallet BE(NestJS), OpenAPI/SDK

- [`infra`](https://github.com/K-Stable/k-stable-pay-infra) / [`core`](https://github.com/K-Stable/core)  
  배포 인프라 + 결제 레일(core contracts / network components)

### Architecture

1. 쇼핑몰에서 스테이블코인 결제
2. Wallet에서 서명 생성 후 제출
3. Pay에서 Operator가 온체인 결제 명령 실행
4. L2에서 거래 처리 후 L1에 롤업 제출
6. Treasury에서 지갑 충전


### Tech Stack (Summary)

- Frontend: Next.js / Flutter(iOS)
- Backend: Spring(쇼핑몰), NestJS(지갑), Go(결제 레일/워커)
- Data: MySQL, Postgres, Redis
- Infra: AWS (ECS, RDS, ElastiCache, ECR, ALB, Route53)
- BlockChain: OP Stack (L2), Ethereum Sepolia (L1), EVM Smart Contracts



