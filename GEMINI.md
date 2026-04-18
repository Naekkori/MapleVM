# GEMINI.md

## 프로젝트 개요
이 프로젝트는 MapleStory Worlds(MSW) 환경 내에서 mLua를 사용하여 구현된 8086 프로세서 기반의 가상머신(MapleVM)입니다.

## 주요 구성 요소
- **MapleVM (MapleStory Worlds Project):** 가상머신을 실행하고 UI 및 환경을 제어하는 메인 프로젝트입니다.
- **MapleBIOS:** 가상머신에서 실행되는 BIOS 펌웨어 코드로, NASM으로 작성되어 바이너리로 컴파일됩니다.
- **img-To-MapleVM-FDD-Dataset:** 디스크 이미지를 가상머신용 데이터셋 형식으로 변환하는 도구입니다.

## 개발 및 빌드 안내
- **BIOS 빌드:** `MapleBIOS` 폴더의 코드를 수정 후 `nasm`을 통해 `bios.bin`을 생성합니다.
- **데이터셋 변환:** `img-To-MapleVM-FDD-Dataset` 폴더 내의 파이썬 스크립트를 사용하여 디스크 이미지를 변환합니다.
- **VM 실행:** MapleStory Worlds Maker를 통해 메인 프로젝트를 실행하여 VM 환경을 구동합니다.

## 개발 컨벤션
- 모든 코드(mLua)는 MSW 환경 규약을 준수해야 합니다.
- 한국어를 사용하며, 주석은 명확하게 작성합니다.
- 복잡한 로직은 `CodeBlock`이나 별도의 `.mlua` 파일로 모듈화합니다.
- 시스템 관련 설정은 `Global/WorldConfig.config`를 확인합니다.
