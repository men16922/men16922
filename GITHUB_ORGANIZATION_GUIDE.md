# GitHub 저장소 정리 가이드

이 가이드는 GitHub 저장소를 효율적으로 정리하고 관리하기 위한 단계별 지침입니다.

## 📋 생성된 파일 목록

### 1. README_PROFILE.md
- **용도**: men16922/men16922 프로필 레포지토리의 README.md로 사용
- **위치**: 현재 디렉토리에 생성됨
- **내용**: 대표 프로젝트만 강조한 프로필 README

### 2. REPOSITORIES.md
- **용도**: 전체 68개 저장소의 완전한 분류 목록
- **위치**: 현재 디렉토리에 생성됨
- **내용**: 7개 테마별로 분류된 모든 저장소

### 3. .github_actions_update_repos.yml
- **용도**: 자동으로 REPOSITORIES.md를 업데이트하는 GitHub Actions 워크플로우
- **위치**: 현재 디렉토리에 생성됨 (나중에 .github/workflows/로 이동 필요)
- **실행 주기**: 매주 월요일 자정 (UTC)

## 🚀 적용 방법

### Step 1: 프로필 레포지토리 업데이트

```bash
# men16922 레포지토리로 이동
cd ~/Desktop/Career/men16922  # 또는 적절한 경로

# 만약 클론되어 있지 않다면:
git clone https://github.com/men16922/men16922.git
cd men16922

# README_PROFILE.md 내용을 README.md로 복사
cp ~/Desktop/Career/men16922.github.io/README_PROFILE.md ./README.md

# REPOSITORIES.md 파일 복사
cp ~/Desktop/Career/men16922.github.io/REPOSITORIES.md ./REPOSITORIES.md

# 변경사항 커밋 및 푸시
git add README.md REPOSITORIES.md
git commit -m "docs: Update README with featured projects and repository index

- Add featured projects section organized by theme
- Add REPOSITORIES.md with complete categorized list of 68 repositories
- Improve project discoverability and organization

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>"
git push origin main
```

### Step 2: GitHub Actions 워크플로우 설정 (선택사항)

자동 업데이트를 원하는 경우:

```bash
# men16922 레포지토리에서
mkdir -p .github/workflows

# GitHub Actions 파일 복사
cp ~/Desktop/Career/men16922.github.io/.github_actions_update_repos.yml ./.github/workflows/update-repos.yml

# 커밋 및 푸시
git add .github/workflows/update-repos.yml
git commit -m "ci: Add auto-update workflow for repository list

- Automatically updates REPOSITORIES.md every Monday
- Can be manually triggered via workflow_dispatch

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>"
git push origin main
```

## 🏷️ Step 3: Topic 태그 지정 (권장)

각 저장소에 테마별 topic 태그를 추가하면 더 쉽게 필터링할 수 있습니다:

### AI/LLM 프로젝트
```
topic: theme-ai-llm, ai, llm, machine-learning
```
- ai-brandy, ai-yanolja-summary, ai_faq, spring-ai, brandy-serverless
- kakaotalk-summarization, assistant-question-answering, prompt-engineering
- shopping-helper, News-Analysis-Prompt, blackcow

### DevOps & CI/CD
```
topic: theme-devops, devops, cicd, kubernetes, docker, aws
```
- docker-ci, DevOps_Part5, CloudFormation, k8s-exam, my-nodejs-app, DVA

### 마이크로서비스 & 백엔드
```
topic: theme-microservices, microservices, spring-cloud, backend
```
- catalog-service, config-service, order-service, user-service
- first-service, second-service, gateway, apigateway-service
- ecommerce, spring-cloud-config, example-gift, example-order
- sample-gateway, coupon-version-management

### 금융 & 결제
```
topic: theme-finance, payment, fintech
```
- Kakaopay, kakaomembership

### 성능 & 동시성
```
topic: theme-performance, performance, load-testing, concurrency
```
- artillery-script, cpu-bound-application, boardserver
- spring-redis-webflux, quartz-cluster

### 학습 & 연습
```
topic: theme-study, learning, tutorial, practice
```
- Coding, LeetCode, git-practice, git-flow-practice
- fastcampus-mysql, Certification, mcp-course
- Spring-Study, spring-study-new, spring-intro
- Spring-JPA-BASIC, jpashop, Spring-Test
- spring-batch, spring-reactive-1, spring-security-oauth2
- spring-security-basic, ThinkDataStructure, MongoDB
- React, React-CodeSandBox, FBTBProject
- UnificationKorea, R, NICE, OODP, tsid-demo-java21
- amplify-vite-react-template

### 개인 & 포트폴리오
```
topic: theme-personal, portfolio
```
- men16922, men16922.github.io

## 📊 Topic 태그를 사용한 필터링

Topic 태그를 지정한 후에는 다음과 같은 URL로 바로 필터링할 수 있습니다:

- AI/LLM: `https://github.com/men16922?tab=repositories&q=topic:theme-ai-llm`
- DevOps: `https://github.com/men16922?tab=repositories&q=topic:theme-devops`
- 마이크로서비스: `https://github.com/men16922?tab=repositories&q=topic:theme-microservices`
- 금융: `https://github.com/men16922?tab=repositories&q=topic:theme-finance`
- 성능: `https://github.com/men16922?tab=repositories&q=topic:theme-performance`
- 학습: `https://github.com/men16922?tab=repositories&q=topic:theme-study`
- 개인: `https://github.com/men16922?tab=repositories&q=topic:theme-personal`

## 🔄 유지보수

### 수동 업데이트
새로운 저장소를 추가하거나 기존 저장소 설명을 변경할 때:

1. REPOSITORIES.md 파일을 직접 수정
2. 변경사항을 커밋하고 푸시

### 자동 업데이트
GitHub Actions를 설정했다면:

1. 매주 월요일 자동으로 업데이트됨
2. 필요시 Actions 탭에서 수동으로 실행 가능

## ✨ 완료 체크리스트

- [ ] README_PROFILE.md를 men16922/men16922 레포의 README.md로 복사
- [ ] REPOSITORIES.md를 men16922/men16922 레포에 추가
- [ ] 프로필 레포지토리에 변경사항 푸시
- [ ] (선택) GitHub Actions 워크플로우 추가
- [ ] (선택) 각 저장소에 Topic 태그 지정

## 🎯 기대 효과

1. **프로필 개선**: 대표 프로젝트가 명확하게 드러남
2. **발견성 향상**: 테마별 분류로 원하는 프로젝트를 쉽게 찾을 수 있음
3. **전문성 강조**: AI/LLM, DevOps, 마이크로서비스 등 전문 분야가 명확히 드러남
4. **유지보수 편의성**: Topic 태그와 자동화로 관리가 용이함

## 📝 참고사항

- 총 68개의 저장소가 7개 테마로 분류되었습니다
- 각 테마는 일관된 네이밍 규칙(`theme-*`)을 따릅니다
- GitHub Actions는 GITHUB_TOKEN을 사용하므로 별도 설정이 필요 없습니다
- 수동 업데이트가 더 정확할 수 있으니, 자동화는 선택사항입니다

## 🆘 문제 해결

### Q: GitHub Actions가 실행되지 않아요
A: Actions 탭에서 워크플로우가 활성화되어 있는지 확인하세요.

### Q: REPOSITORIES.md 링크가 작동하지 않아요
A: 프로필 레포지토리에 파일이 제대로 푸시되었는지 확인하세요.

### Q: Topic 태그를 어떻게 추가하나요?
A: 각 저장소의 Settings > General > Topics에서 태그를 입력하세요.

---

작성일: 2025-11-22
작성자: Claude Code
