## 목차

1. [Organization 멤버 및 Team 관리 규칙](#organization-team-rules)
2. [Repository 권한 규칙](#repository-permission-rules)
3. [Branch 관리 원칙](#branch-rules)
4. [Repository 이름 규칙](#repository-name-rules)
5. [Repository Description 작성 규칙](#repository-description-rules)
6. [Repository 이름 작성 원칙](#repository-name-principles)
7. [최종 예시](#examples)

---

## 빠른 링크

- [encore-ai-campus Organization](https://github.com/encore-ai-campus)
- [Repositories](https://github.com/orgs/encore-ai-campus/repositories)
- [New repository](https://github.com/organizations/encore-ai-campus/repositories/new)
- [Teams](https://github.com/orgs/encore-ai-campus/teams)
- [People](https://github.com/orgs/encore-ai-campus/people)

---

<a id="organization-team-rules"></a>

## 1. Organization 멤버 및 Team 관리 규칙

- Team 관리는 [encore-ai-campus Teams](https://github.com/orgs/encore-ai-campus/teams)에서 진행한다.
- Organization 멤버 관리는 [encore-ai-campus People](https://github.com/orgs/encore-ai-campus/people)에서 진행한다.
- 훈련생은 Outside collaborator가 아닌 Organization member로 초대한다.
- 훈련생은 소속 과정/기수에 해당하는 Team에 배정한다.
- Team 이름은 `{과정코드}-{기수번호}` 형식으로 작성한다.
  - 예: `AIO-00`, `MLO-00`, `MLE-00`
- Team Description에는 과정명을 작성한다.
  - 예: `AI 오케스트레이션 0기`, `MLOps 엔지니어 0기`, `머신러닝 엔지니어 0기`
- Organization Owner 권한은 강사 및 매니저 중 운영 담당자에게만 부여한다.
- Organization Owner는 최소 2명 이상 유지하되, 불필요하게 많은 인원에게 부여하지 않는다.
- 훈련생에게는 기본적으로 Organization Owner 또는 Repository Admin 권한을 부여하지 않는다.
- Repository 설정 변경 등 Admin 권한이 필요한 작업은 강사 또는 매니저가 수행한다.
- 특별한 사유로 Admin 권한이 필요한 경우, 기간과 범위를 제한하여 임시로 부여한 뒤 작업 완료 후 회수한다.

---

<a id="repository-permission-rules"></a>

## 2. Repository 권한 규칙

- Repository별 권한은 각 Repository의 `Settings > Collaborators and teams`에서 관리한다.

| 대상          | 권한                                     |
| ------------- | ---------------------------------------- |
| CAMPUS-ADMIN  | Organization Owner 또는 Repository Admin |
| 강사 / 매니저 | Repository Maintain 또는 Admin           |
| 팀장          | Repository Maintain                      |
| 팀원          | Repository Write                         |

---

<a id="branch-rules"></a>

## 3. Branch 관리 원칙

- Repository 생성 시 기본 브랜치명이 `main`인지 확인한다.
- 기본 브랜치는 `main`으로 고정한다.
- `main` 브랜치는 최종 검토가 완료된 산출물을 기준으로 관리한다.
- 작업 중인 내용은 별도 브랜치에서 관리하고, 검토 후 `main`에 반영한다.
- 필요 시 `dev`, `feature/{기능명}`, `fix/{수정명}`, `docs/{문서명}` 등의 브랜치를 사용할 수 있다.

---

<a id="repository-name-rules"></a>

## 4. Repository 이름 규칙

Repository 이름은 짧고 일관되게 작성한다.
Repository 생성은 [New repository](https://github.com/organizations/encore-ai-campus/repositories/new)에서 진행한다.

```text
{과정기수}-{프로젝트회차}-{프로젝트팀}[-구분]
```

### 구성 요소

| 항목         | 규칙                         | 예시                         |
| ------------ | ---------------------------- | ---------------------------- |
| 과정기수     | 소문자 과정 코드 + 기수 번호 | aio-00, mlo-00, mle-00       |
| 프로젝트회차 | p1, p2, p3, p4, fin          | p1, p2, fin                  |
| 프로젝트팀   | team{번호}                   | team1, team2, team10         |
| 구분         | 필요 시에만 작성             | fe, be, dev, ai, data, infra |

### 기본 예시

```text
mlo-00-p1-team1
mlo-00-p2-team2
mlo-00-p3-team3
mlo-00-p4-team4
mlo-00-fin-team1

aio-00-p1-team1
aio-00-fin-team2

mle-00-p2-team3
mle-00-fin-team4
```

### FE / BE 등 분리 시 예시

프로젝트를 프론트엔드, 백엔드, 개발환경 등으로 나누어 관리해야 하는 경우 마지막에 구분값을 붙인다.

```text
mlo-00-fin-team1-fe
mlo-00-fin-team1-be
mlo-00-fin-team1-dev

aio-00-p2-team3-fe
aio-00-p2-team3-be

mle-00-fin-team4-ai
mle-00-fin-team4-data
mle-00-fin-team4-infra
```

---

<a id="repository-description-rules"></a>

## 5. Repository Description 작성 규칙

Repository Description에는 프로젝트 설명을 작성한다.

```text
{프로젝트 설명}
```

### 예시

```text
AI 면접 코칭 서비스
```

```text
MLOps 기반 모델 배포 플랫폼
```

```text
RAG 기반 사내 문서 검색 챗봇
```

### 작성 규칙

- Repository 이름에는 프로젝트명을 넣지 않는다.
- 프로젝트 설명은 Repository Description에 작성한다.
- 프로젝트명이 확정되지 않은 경우 임시 프로젝트명을 작성한 뒤 확정 후 수정한다.

---

<a id="repository-name-principles"></a>

## 6. Repository 이름 작성 원칙

- 모든 문자는 영문 소문자를 사용한다.
- 단어 구분은 하이픈 `-`을 사용한다.
- 한글, 공백, 특수문자는 사용하지 않는다.
- 프로젝트팀명은 `team{번호}` 형식으로 작성한다. 예: `team1`, `team2`, `team10`
- 프로젝트회차는 `p1`, `p2`, `p3`, `p4`, `fin` 중 하나를 사용한다.
- `fe`, `be`, `dev` 등 구분값은 Repository를 분리해야 할 때만 사용한다.

---

<a id="examples"></a>

## 7. 최종 예시

| 과정   | 회차 | 팀     | Repository 이름     | Description                  |
| ------ | ---- | ------ | ------------------- | ---------------------------- |
| MLO-00 | 최종 | 1팀    | mlo-00-fin-team1    | MLOps 기반 모델 배포 플랫폼  |
| AIO-00 | 2차  | 3팀    | aio-00-p2-team3     | RAG 기반 문서 검색 챗봇      |
| MLE-00 | 최종 | 4팀 FE | mle-00-fin-team4-fe | 이미지 분류 서비스 Frontend  |
| MLE-00 | 최종 | 4팀 BE | mle-00-fin-team4-be | 이미지 분류 서비스 Backend   |
