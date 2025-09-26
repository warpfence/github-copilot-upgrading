# upgraded 폴더 구조 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일 및 디렉터리 구조를 그대로 복사한 디렉터리입니다. 이 폴더는 Python 2.5 기반의 레거시 코드를 최신 Python 버전으로 업그레이드하는 작업 공간으로 사용됩니다.

## 디렉터리 및 파일 구조

- MANIFEST.in: 패키징에 포함할 파일 목록을 지정하는 설정 파일
- README.rst: 프로젝트 설명서 (reStructuredText 형식)
- distribute-0.6.10.tar.gz: distribute 패키지 소스 아카이브 (구버전 패키징 도구)
- distribute_setup.py: distribute 설치 스크립트
- setup.py: 프로젝트 설치 및 배포를 위한 파이썬 스크립트
- docs/: 프로젝트 문서 관련 디렉터리
  - build/: 빌드된 문서(HTML, doctree 등)
  - source/: Sphinx 문서 소스(rst, conf.py 등)
- guachi/: 주요 파이썬 소스 코드 디렉터리
  - __init__.py: guachi 패키지 초기화 파일
  - config.py: 설정 관련 코드
  - database.py: 데이터베이스 관련 코드
  - tests/: 테스트 코드 디렉터리
    - test_configmapper.py: configmapper 테스트
    - test_configurations.py: 설정 관련 테스트
    - test_database.py: 데이터베이스 테스트
    - test_integration.py: 통합 테스트
- guachi.egg-info/: 패키징 메타데이터 디렉터리
  - PKG-INFO, SOURCES.txt, dependency_links.txt, top_level.txt 등

## 활용 목적

- 이 디렉터리는 레거시 코드를 최신 Python 환경에 맞게 점진적으로 업그레이드하고, 테스트 및 문서화 작업을 수행하는 데 사용됩니다.
- 기존 구조와 동일하게 복사되어 있으므로, 변경 전/후 비교 및 점진적 마이그레이션이 용이합니다.
