---
layout: post
title:  "깃허브 초보자의 깃페이지 만들기"
date:   2024-07-28 18:01:35 +0900
categories: jekyll update
---

코로나로 1.5년, 코로나 휴유증(놀았다는 뜻)으로 약 1년,
공부를 시작한지 얼마 되지 않았는데 벌써 고학년이라
뭘 제대로 알지 못하는 것 같은데... 음... 아는 거라도 모아놔야 
기록이 모이지 않을까하여 개설했습니다. 

https://daniazie.github.io/page2/

다니아가 알려준대로 만들었어요 :-)


### 1. Jekyll 설치하기

#### 1.1. 필수 패키지 설치

먼저, Ruby와 RubyGems를 설치합니다. 설치 방법은 아래 링크를 참조하세요:
- [Ruby 다운로드](https://www.ruby-lang.org/en/downloads/)
- [RubyGems 다운로드](https://rubygems.org/pages/download)

#### 1.2. Jekyll과 Bundler 설치

터미널을 열고, Ruby 설치가 완료된 후 아래 명령어를 실행하세요:

```bash
gem install jekyll bundler
```

### 2. Jekyll 프로젝트 생성

#### 2.1. 프로젝트 폴더 생성 및 이동

새로운 폴더를 만들고 해당 폴더로 이동합니다. 예를 들어, `tutorial` 폴더를 만들고 이동합니다.

```bash
mkdir tutorial
cd tutorial
```

#### 2.2. Jekyll 사이트 초기화

현재 디렉토리(폴더)에 Jekyll 사이트를 초기화합니다. (마침표 필수)

```bash
jekyll new --skip-bundle .
```

### 3. Visual Studio Code에서 프로젝트 열기

VS Code를 열고, `tutorial` 폴더를 엽니다.

### 4. Gemfile 편집

#### 4.1. Gemfile 열기

VS Code에서 `Gemfile`을 열고 아래 부분을 수정합니다.

```ruby
# gem "jekyll"
gem "github-pages", group: :jekyll_plugins
```

#### 4.2. Gemfile 패키지 설치

터미널에서 아래 명령어를 실행하여 Gemfile에 명시된 패키지를 설치합니다.

```bash
bundle install
```

### 5. GitHub와 연결하기

#### 5.1. GitHub CLI 설치 및 로그인

GitHub CLI를 설치하고 로그인합니다. 설치는 [GitHub CLI 다운로드](https://cli.github.com/)를 참고하세요. 터미널에서 아래 명령어를 실행합니다.

```bash
gh auth login
```

#### 5.2. GitHub 레포지토리 생성

GitHub에서 새 레포지토리를 생성합니다. 레포지토리 이름을 `[아이디].github.io`로 설정합니다. SSH 링크를 복사합니다.

#### 5.3. 로컬 레포지토리 초기화 및 원격 레포지토리 추가

터미널에서 아래 명령어를 실행하여 로컬 레포지토리를 초기화하고 원격 레포지토리를 추가합니다.

```bash
git init
git remote add origin git@github.com:username/username.github.io.git
```

#### 5.4. 파일 커밋 및 푸시

아래 명령어를 실행하여 변경된 파일을 커밋하고 푸시합니다.

```bash
git add .
git commit -m "First commit"
git push origin master
```

### 6. GitHub Pages 설정

#### 6.1. GitHub Pages 활성화

GitHub 레포지토리 설정(Settings)에서 Pages 섹션으로 이동합니다. Source를 "Deploy from a branch"로 설정하고, Branch를 "master" 또는 "main"으로 설정합니다.

### 7. 사이트 설정

#### 7.1. _config.yml 파일 편집

VS Code에서 `_config.yml` 파일을 열고 사이트 이름, 설명 등을 변경합니다.

### 8. 글 작성

#### 8.1. Markdown 파일 생성

글을 작성할 때, `_posts` 폴더에 `YYYY-MM-DD-주제.markdown` 형식으로 파일을 생성합니다. 파일 내용은 아래와 같이 작성합니다.

```markdown
---
layout: post
title:  "글 주제"
date:   YYYY-MM-DD HH:MM:SS
categories: 카테고리
---

여기에 글 내용을 작성하세요.
```

#### 8.2. 파일 커밋 및 푸시

아래 명령어를 실행하여 새 글을 커밋하고 푸시합니다.

```bash
git add .
git commit -m "Uploaded first post"
git push origin master
```

### 9. Chirpy 테마 사용 (선택사항)

#### 9.1. Chirpy 템플릿 사용

Chirpy 템플릿을 사용하여 새로운 레포지토리를 생성합니다. [Chirpy 스타터 레포지토리](https://github.com/cotes2020/chirpy-starter)에서 "Use this template" 버튼을 클릭하여 새 레포지토리를 생성합니다.

#### 9.2. 로컬 레포지토리 초기화 및 원격 레포지토리 연결

위와 동일하게 로컬 레포지토리를 초기화하고 원격 레포지토리와 연결합니다.

```bash
git init
git remote add origin git@github.com:username/username.github.io.git
git pull origin master
```

#### 9.3. Chirpy 설치

터미널에서 아래 명령어를 실행하여 Chirpy를 설치합니다.

```bash
bundle
```

#### 9.4. _config.yml 파일 편집

VS Code에서 `_config.yml` 파일을 열고 필요한 설정을 변경합니다.
