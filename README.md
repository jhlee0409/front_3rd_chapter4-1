# 프론트엔드 배포 파이브라인

## 배포 flow

![deploy flow](deploy.drawio.png)

1. 기본적으로 `main` 브랜치에 `push`가 일어나면 workflow가 동작합니다.
2. 정적으로 build `/out`폴더 내의 모든 파일이 s3에 업로드됩니다.
3. cloudfront를 통해 서비스를 서빙 중입니다.
   - `--paths "/*"`를 경로로 지정하여 캐시된 모든 파일을 무효화하고 최신 버전을 제공합니다.

## 주요 링크

- S3 버킷 웹사이트 엔드포인트: for-hanghae-fe-3rd
- CloudFrount 배포 도메인 이름: d1x6ezuaiwwi4x

## 주요 개념

- GitHub Actions과 CI/CD 도구: \***\*\_\*\***
- S3와 스토리지: \***\*\_\*\***
- CloudFront와 CDN: \***\*\_\*\***
- 캐시 무효화(Cache Invalidation): \***\*\_\*\***
- Repository secret과 환경변수: \***\*\_\*\***
