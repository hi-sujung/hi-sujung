# MSA와 k8s를 통한 하이수정 고도화 프로젝트
about hisujung-msa-k8s

## Architecture Diagram
<img width="619" alt="스크린샷 2024-06-18 오후 9 54 33" src="https://github.com/hi-sujung/hisujung-msa-k8s/assets/100345983/ff795ff0-68f7-4a73-bb42-f09593655db4">

## Folder Structure
```
.
├── cloudflare
│   ├── notification
│   │     └── slack-gke.js
│   └── web
│         └── address.md
├── k8s-manifest
│   ├── hisujung-all.yaml
│   ├── hisujung-configmap.yaml
│   ├── hisujung-ingress.yaml
│   └── hisujung-secret.yaml
├── load-test
│   ├── hisujung-configmap.yaml
│   ├── hisujung-hpa.yaml
│   ├── hisujung-ingress.yaml
│   ├── hisujung-secret.yaml
│   └── hisujung-test.yaml
├── microservices
│   ├── auth-jwt
│   ├── crawling-external
│   ├── crawling-univ
│   ├── front-web
│   ├── member
│   ├── notice
│   ├── portfolio
│   ├── rabbitmq
│   └── recommend
├── scripts
│   └── k8s-script.sh
├── .gitignore
└── README.md
```

## About microservices
| 이름                 | 기능                                | k8s 오브젝트                               |
|---------------------|------------------------------------|------------------------------------------|
| [auth-jwt](https://github.com/hi-sujung/msa-auth-jwt) |                                    | Deployment, Service |
| [crawling-external](https://github.com/hi-sujung/msa-crawling-external) |                                    | CronJob |
| [crawling-univ](https://github.com/hi-sujung/msa-crawling-univ) |                                    | CronJob |
| [front-web ](https://github.com/hi-sujung/msa-front-web) |                                    | Deployment, Service |
| [member](https://github.com/hi-sujung/msa-member) | 회원가입(이메일 인증), 로그인, 로그아웃 | [Deployment](https://github.com/hi-sujung/hisujung-msa-k8s/blob/main/k8s-manifest/member/deployment.yaml), [Secret](https://github.com/hi-sujung/hisujung-msa-k8s/blob/main/k8s-manifest/member/secret.yaml), [Service](https://github.com/hi-sujung/hisujung-msa-k8s/blob/main/k8s-manifest/member/service.yaml) |
| [notice](https://github.com/hi-sujung/msa-notice) |                                    | ConfigMap, Deployment, Secret, Service |
| [portfolio](https://github.com/hi-sujung/msa-portfolio) |                                    | Deployment, Secret, Service |
| [rabbitmq](https://github.com/hi-sujung/msa-rabbitmq) |                                    | PVC, Secret, Service, StatefulSet |
| [recommend](https://github.com/hi-sujung/msa-recommend) |                                    | Deployment, Service |


## How to start
1.


## How to test
1. 


