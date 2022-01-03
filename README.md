# Git 版本控制系統

強大的非中心式的版本控制系統

![「檢查專案中的潛在問題」GitHub Actions 作業流程狀態標章](https://github.com/libre-knowledge/git/actions/workflows/check-potential-problems.yml/badge.svg "本專案使用 GitHub Actions 自動化檢查專案中的潛在問題") [![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white "本專案使用 pre-commit 檢查專案中的潛在問題")](https://github.com/pre-commit/pre-commit) [![REUSE 規範遵從狀態標章](https://api.reuse.software/badge/github.com/libre-knowledge/git "本專案遵從 REUSE 規範降低軟體授權合規成本")](https://api.reuse.software/info/github.com/libre-knowledge/git)

## 特色

* 能有效率地處理大規模的版控庫
* 最早使用於 Linux 作業系統核心開發，後被大多數軟體專案採用
* 為分散式（非中心式）版本控制系統，大多數非涉及遠端操作可直接於本地進行

## 基本概念

### <ruby>修訂版<rp>(</rp><rt>revision</rt><rp>)</rp></ruby>、<ruby>修訂版提交<rp>(</rp><rt>commit（名詞）</rt><rp>)</rp></ruby>

版本控制系統中內容變動的單位，在 Git 版本控制系統中<ruby>修訂版<rp>(</rp><rt>revision</rt><rp>)</rp></ruby>跟 commit 的名詞部份意義相同

### <ruby>修訂歷史<rp>(</rp><rt>history</rt><rp>)</rp></ruby>

被版本控制的內容所變動的歷程，在 Git 版本控制系統中<ruby>修訂歷史<rp>(</rp><rt>history</rt><rp>)</rp></ruby>是由一系列互相連接的<ruby>修訂版提交<rp>(</rp><rt>commit（名詞）</rt><rp>)</rp></ruby>所構成

### <ruby>有向無環圖<rp>(</rp><rt>Directed acyclic graph</rt><rp>)</rp></ruby>

Git 版本控制系統<ruby>修訂歷史<rp>(</rp><rt>history</rt><rp>)</rp></ruby>所構成的<ruby>圖形<rt>graph</rt></ruby>，有方向性（較早的<ruby>修訂版提交<rp>(</rp><rt>commit（名詞）</rt><rp>)</rp></ruby>指向較晚的<ruby>修訂版提交<rp>(</rp><rt>commit（名詞）</rt><rp>)</rp></ruby>）但不存在首尾為同一<ruby>修訂版提交<rp>(</rp><rt>commit（名詞）</rt><rp>)</rp></ruby>之組成<ruby>環路<rt>cycle</rt></ruby>的狀況

### <ruby>提交<rp>(</rp><rt>commit（動詞）</rt><rp>)</rp></ruby>

提交新的<ruby>修訂版<rp>(</rp><rt>revision</rt><rp>)</rp></ruby>到<ruby>版控庫<rt>repository</rt></ruby>中的動作

### 新修訂版<ruby>準備區域<rt>staging area</rt></ruby>

在提交前集中要加進新修訂版中的內容變更的地方，又稱為 index

### Git <ruby>掛勾程序<rt>hook</rt></ruby>

可以<ruby>掛接<rt>hook (v.)</rt></ruby>在特定 Git 操作，在其運行前/後觸發執行的程序，參閱 githooks(5) 的<ruby>使用手冊頁面<rt>manpage</rt></ruby>

## 常用的 Git 子命令

* init  
  初始化一版控庫
* config  
  配置系統全域、使用者全域或版控庫範圍的 Git 設定選項
* status  
  查詢版控庫當前狀態
* add  
  將內容變更移入<ruby>新修訂版準備區域<rp>(</rp><rt>staging area</rt><rp>)</rp></ruby>
* rm  
  將被版控檔案移除並將此變更移入<ruby>新修訂版準備區域<rp>(</rp><rt>staging area</rt><rp>)</rp></ruby>
* commit  
  建立一新<ruby>修訂版<rp>(</rp><rt>revision</rt><rp>)</rp></ruby>並將其提交進版控庫
* diff  
  查看修訂版參照間的內容差異
* log  
  查看版本紀錄
* remote  
  管理遠端版控庫
* push  
  將本地版控庫當前分支歷史推送至遠端版控庫
* pull  
  將遠端版控庫追蹤分之歷史拉取並合併回本地版控庫當前分支
* reset  
  重設參照指標及/或當前工作樹內容

## 解決方案

* [The Common .gitignore Templates](https://github.com/the-common/gitignore-templates)  
  提供可快速引入專案中的 Git 版本追蹤排除規則
* [The Common Gitattributes Template](https://github.com/the-common/gitattributes-templates)  
  提供可快速引入專案中的 Git 檔案路徑屬性配置檔
* [Git 版本控制忽略規則範本](https://github.com/brlin-tw/Git_ignore_rules_template)  
  提供多種情境適用之 Git 版本追蹤忽略規則
* [gitignore - A collection of useful .gitignore templates](https://github.com/github/gitignore)  
  由 GitHub 所維護的多情境適用之 Git 追蹤排除規則範本

## 參考資料

### 中文教學文件

※使用的專有術語翻譯可能會有不精確的情況，以原文為主

* Git 官方教學用書：  
  [Git - Book](https://git-scm.com/book/zh-tw/v2)
* [連猴子都能懂的Git入門指南 | 貝格樂（Backlog）](https://backlog.com/git-tutorial/tw/)

### 原文教學文件

* [Git - gittutorial Documentation](https://git-scm.com/docs/gittutorial)
* [Git - Reference](https://git-scm.com/docs)
* [Git - gitglossary Documentation](https://git-scm.com/docs/gitglossary)

### 其他

* [透過 HTTP 與 HTTPS 連接 Git 儲存庫時如何記憶常用密碼 | The Will Will Web](https://blog.miniasp.com/post/2014/05/22/Credential-Store-for-Git-HTTP-HTTPS)
* [撰寫有效的 Git Commit Message | Fourdesire Blog](https://blog.fourdesire.com/2018/07/03/%E6%92%B0%E5%AF%AB%E6%9C%89%E6%95%88%E7%9A%84-git-commit-message/)

---

本主題為[自由知識協作平台](https://libre-knowledge.github.io/)的一部分，除部份特別標註之經合理使用(fair use)原則使用的內容外允許公眾於授權範圍內自由使用

如有任何問題，歡迎於本主題的[議題追蹤系統](https://github.com/libre-knowledge/git/issues)創建新議題反饋
