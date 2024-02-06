### 세팅

```
# .env 파일 생성, github settings secrets actions 참고
MYSQL_ROOT_PASSWORD=${{secrets.MYSQL_ROOT_PASSWORD}}
MYSQL_DATABASE=${{secrets.MYSQL_DATABASE}}
MYSQL_USER=${{secrets.MYSQL_USER}}
MYSQL_PASSWORD=${{secrets.MYSQL_PASSWORD}}
```

### 빌드

```
$ docker compose build
```

### 로컬 서비스 시작

```
$ docker compose up -d
```


### 로컬 서비스 중지

```
$ docker compose down
```

### 서비스

```
# nginx
localhost:80

# fastapi
localhost:8000

# mariadb
localhost:3306
```

### 디렉토리 구조 
```
project/
|-- app/
|   |-- main.py             # FastAPI 애플리케이션 코드
|   |-- requirements.txt    # Python 종속성
|-- mariadb/
|   |-- conf.d/
|       |-- my.cnf          # MariaDB 설정
|   |-- data/               # MariaDB data 마운트
|-- nginx/
|   |-- conf.d/
|       |-- nginx.conf      # Nginx 구성 파일
|-- .github/
|   |-- workflows/
|       |-- deploy.yml      # GitHub Actions 배포 워크플로우
|-- .dockerignore           # 환경 변수
|-- .env                    # 환경 변수
|-- .gitignore              # 환경 변수
|-- docker-compose.yml      # Docker Compose 구성
|-- Dockerfile              # FastAPI Dockerfile
|-- README.md               # 프로젝트 문서
```