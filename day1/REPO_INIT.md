## 🧰 GitHub 연결 방식별 실습 가이드 (Init / Clone / Publish Branch)

이 문서는 GitHub 저장소에 코드를 올리는 3가지 주요 연결 방식인 `init`, `clone`, `publish branch`의 단계별 사용법을 설명합니다.

---

### ✅ 방법 1: 기존 폴더에서 `init`으로 GitHub 저장소 연결 후 Push

```bash
mkdir my-init-project
cd my-init-project
echo "# Init Repo" > README.md
git init
git add .
git commit -m "init commit"
git remote add origin https://github.com/username/my-init-repo.git
git branch -M main
git push -u origin main
```

> 이 방법은 이미 존재하는 로컬 폴더에 Git을 초기화하여 GitHub와 연결할 때 사용합니다.

---

### ✅ 방법 2: GitHub 저장소를 `clone`해서 로컬에 복제 후 작업

```bash
git clone https://github.com/username/my-clone-repo.git
cd my-clone-repo
echo "Hello Clone" > hello.txt
git add .
git commit -m "add hello.txt"
git push
```

> 이 방법은 GitHub에 존재하는 저장소를 로컬로 복제(clone)하여 코드 작업을 이어나갈 때 사용합니다.

---

### ✅ 방법 3: GitHub Desktop에서 Publish Branch로 연결 후 Push

1. GitHub Desktop에서 **File > New Repository** 선택
2. 저장소 이름, 경로 설정 후 Create Repository
3. 프로젝트 파일 추가
4. **Commit to main** 버튼 클릭
5. 상단에 있는 **Publish Branch** 버튼 클릭
6. GitHub에 자동으로 저장소가 생성되며 연결됨
7. 이후에는 Commit → Push 흐름으로 관리

> GUI 기반의 GitHub Desktop을 활용한 가장 직관적인 연결 및 업로드 방법입니다.

---

## 📌 비교 요약

| 방법             | 주요 특징                 | 추천 대상             |
| ---------------- | ------------------------- | --------------------- |
| `init`           | 기존 폴더를 GitHub에 연결 | 개인 프로젝트 시작 시 |
| `clone`          | 기존 GitHub 저장소 복제   | 팀 프로젝트 참여 시   |
| `publish branch` | GUI로 원클릭 연동         | 입문자, 비개발자      |

---

각 방식은 상황과 목적에 따라 선택할 수 있으며, 실무에서는 `clone` → `branch` → `PR` 흐름이 자주 사용됩니다.
