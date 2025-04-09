## 🧹 0단계: 공통 준비 사항

### 🔹 GitHub에 저장소(Repo) 만들기

1. GitHub 로그인
2. 오른쪽 상단 `+` 버튼 → **New repository**
3. 저장소 이름 입력 (예: `my-first-repo`)
4. Private/Public 선택
5. `README`는 체크 안해도 됨 → **Create repository**

> 이때 나오는 `https://github.com/username/repo.git` 주소를 깨지하세요!

---

## 🧑‍💻 1. **VS Code로 GitHub에 올린기**

### ✅ 단계별 요약

#### 📂 1. 로컬 프로젝트 폴더 만들기

```bash
mkdir my-project
cd my-project
code .
```

#### 🧱 2. Git 초기화 및 커미트

VS Code 좌측 Source Control (🔃) 아이콘 클릭 → "Initialize Repository"

파일 생성 후 (예: `index.html`), 변경사항 Stage → Commit (메시지 입력 후 ✔️ 클릭)

#### 🌐 3. 원격 저장소 연결 (VS Code 터링에서)

```bash
git remote add origin https://github.com/username/my-first-repo.git
git branch -M main
git push -u origin main
```

#### 🔐 4. GitHub 인증 (처음 한 번만)

- GitHub ID 입력
- 비밀번호 자리에 **Token 붙여넣기**

---

## 🧱 2. **Git Bash로 GitHub에 올린기**

### ✅ 단계별 요약

#### 📁 1. 폴더 및 Git 초기화

```bash
mkdir my-project
cd my-project
git init
```

#### 📄 2. 파일 만든 후 커미트

```bash
echo "# My First Git Project" > README.md
git add .
git commit -m "first commit"
```

#### 🔗 3. 원격 저장소 연결 및 푸시

```bash
git remote add origin https://github.com/username/my-first-repo.git
git branch -M main
git push -u origin main
```

#### 🔐 4. 인증 과정

- GitHub ID → Token 입력

✅ 이후는 `git add . → git commit -m "" → git push` 만 복쟬하면 됩니다!

---

## 🖥️ 3. **GitHub Desktop으로 올린기**

### ✅ 단계별 요약

#### 1️⃣ GitHub Desktop 설치 및 로그인

- [https://desktop.github.com](https://desktop.github.com) 에서 다운로드
- GitHub 계정 로그인

#### 2️⃣ 새 저장소 만들기

- **File > New Repository**
- 이름, 로컬 경로 지정 → Create Repository

#### 3️⃣ 파일 추가 및 Commit

- 로컬 폴더 열어서 파일 추가 (예: `index.html`)
- GitHub Desktop으로 돌아와서 변경사항 확인
- Commit 메시지 입력 후 → **Commit to main**

#### 4️⃣ GitHub 저장소에 Publish

- **Publish repository** 버튼 클릭
- Private/Public 선택 → Publish

→ 이제 GitHub.com에 가면 코드가 올린 것을 확인 가능!

---

## 💡 마무리 핀

| 상황                                | 최규 방법      |
| ----------------------------------- | -------------- |
| **GUI 선호 / 쉬운 사용**            | GitHub Desktop |
| **IDE에서 바로 사용 / 편리한 통합** | VS Code        |
| **명령어에 익시가하거나 학습 중**   | Git Bash       |

끝났습니다.
