# 103022300024 - Jack Kelvin - MKPEL

Proyek Basic Java Maven dengan pipeline CI/CD menggunakan GitHub Actions.

## Pipeline Overview

| Stage | Poin | Deskripsi |
|---|---|---|
| Continuous Integration | 25 | Build dengan Maven |
| Continuous Testing | 25 | Unit Test dengan JUnit |
| Continuous Inspection | 35 | Code analysis dengan SonarCloud + JaCoCo |
| Continuous Delivery/Deploy | 15 | Package & upload JAR artifact |

## Cara Setup SonarCloud

1. Buat akun di [sonarcloud.io](https://sonarcloud.io)
2. Import repository GitHub ini
3. Buat **SONAR_TOKEN** di SonarCloud → My Account → Security
4. Tambahkan secret di GitHub repo → Settings → Secrets → `SONAR_TOKEN`
5. Update `sonar.organization` di `maven.yml` sesuai organization SonarCloud kamu

## Struktur Proyek

```
src/
├── main/java/
│   ├── Counter.java
│   └── Driver.java
└── test/java/
    └── CounterTest.java
```
