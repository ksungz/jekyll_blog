```bash
# Homebrew설치 (반드시 Intel 기반의 Homebrew를 설치해야 합니다. - M1 사용자 주의)
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Ruby 설치 (2.6.6, x86 버전 설치) - 일반 MacOS는 Ruby 2.6.3을 포함하고 있으므로 설치하지 않고 Pass해도 됩니다. (rvm -> ruby -> jekyll 설치)
$ \curl -sSL https://get.rvm.io | bash -s stable
$ rvm install ruby-2.6.6
$ rvm use ruby-2.6.6
$ rvm --default use 2.6.6

# ruby 는 x86_64로 나와야 합니다.
$ ruby -v
ruby 2.6.6p146 (2020-03-31 revision 67876) [x86_64-darwin20]

# jekyll, bundler 설치
$ gem install jekyll bundler
```

```bash
# 내가 만든 깃헙 레파지토리 클론
$ git clone https://github.com/ksungz/jekyll_blog.git
'jekyll_blog'에 복제합니다...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0

$ cd jekyll_blog

# 테마 고르기
# http://jekyllthemes.org/
# https://jekyllthemes.io/

# 테마 적용 방법
# 1. fork
# ----- https://calgaryhomeless.tistory.com/1
# 2. 테마 저장소를 내 로컬에 clone 후 나의 저장소로 푸시
# ----- https://blog.chulgil.me/how-to-make-blog-using-github-4/
# 3. zip파일을 활용하여 파일 가져오기.
# ----- https://bit.ly/3guh5AV

# bundler로 필요 모듈 설치 (gemfile) --> npm의 package.json같은...?
$ bundle install
...


# jekyll로 컴파일 및 로컬 테스트
$ jekyll serve
Configuration file: /Users/a1101479/Documents/workspace/jekyll_blog/_config.yml
            Source: /Users/a1101479/Documents/workspace/jekyll_blog
       Destination: /Users/a1101479/Documents/workspace/jekyll_blog/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Jekyll Feed: Generating feed for posts
                    done in 0.299 seconds.
 Auto-regeneration: enabled for '/Users/a1101479/Documents/workspace/jekyll_blog'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.

## http://127.0.0.1:4000/ 를 브라우저에서 오픈하여 정상 노출 여부를 확인합니다.
```

## 글써보기
