---
title       : 'RubyとJekyllをインストールしローカルPCでデバッグ'
date        : 2020-04-06
categories  : posts
permalink   : /:categories/:year/:month/:day.html
tags        :
              - "GitHub Pages"
              - "Ruby"
              - "Jekyll"
---
  - GitHub上に作ったGitHub PagesのリポジトリをローカルPCにcloneし、デバッグできるよう環境設定した。

  - Rubyの最新版＋JekyllでローカルPC上に作った仮想サーバでは、昨日forkしてきたacademicpages.github.ioがライブラリの依存関係の問題でうまく立ち上がらなかった。そこで、[GitHub Pages : Dependency versions](https://pages.github.com/versions/)を参考に、少し古い```rubyinstaller-devkit-2.5.8-1-x64.exe```をインストールし、```Gemfile```を調整したらまくいった。

------