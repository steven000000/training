# training

本課程除訓練學生了解行動裝置程式設計、架構、原理以及應用服務外，並著重在介紹相關之證照考試，如：TQC+認證。配合課程研讀相關資料，並鼓勵同學們參加TQC+認證，以期增加同學未來職場上的競爭力。

另外，為了縮短資訊業界嚴重的學用落差，並且強化畢業後的競爭力，這門課除了教導目前最火紅的手機App開發外，更重要的是教導許多目前在業界中常見的工具、技術、觀念。如共同協作、版本控管、專案管理.....等。

有興趣修課的同學請務必看看下面文章，了解目前業界生態：

* [寫給大學生的程式技能 Cheatsheets](http://blog.xdite.net/posts/2013/11/22/opensource-cheatsheets)
* [業界與學界，深刻的鴻溝](http://blog.caesarchi.com/2013/12/blog-post_22.html)
* [TonyQ對於第二篇的回應](https://www.facebook.com/notes/10151828753826709)

## 本學期作業繳交方式

每一次上課都會新增一個目錄，請同學們同步老師的repo之後，再繳交作業上來。

以EX1為例，若R9543002要繳交作業的話，檔案目錄結構應該如下

* EX1/R9543002/aaa.png
* EX1/R9543002/bbb.png

EX1後面直接帶學號就可以了，不用另外帶班級、姓名喔，統一格式也比較容易讓老師及助教批改。

## 如何將自己的repo更新到老師repo的最新版本

步驟2只要做第一次就好，之後若要持續更新到老師repo的最新版本，則只要執行步驟3即可。

### 1. 打開Git Shell

1. 開始-&gt;所有程式-&gt;GitHub. Inc.-&gt;Git Shell

### 2. 將自己的repo與老師的repo連結

1. `git remote -v`：先檢查自己的repo是否與老師的repo連結。若出現以下內容，則表示連結成功；若無則執行第二步驟
```
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ucs0065/training.git (fetch)
upstream  https://github.com/ucs0065/training.git (push)
```
2. `git remote add upstream https://github.com/ucs0065/training.git`：將老師的repo連結到自己的repo中，執行後則再執行第一步驟，檢查是否已連結成功
3. 若第二步驟打錯字，則可以使用`git remote rm upstream`刪除連結後，再從第一步驟重新執行

### 3. 將自己的repo更新到老師的最新版本

1. `git fetch upstream`：將老師repo的最新版本，抓到本機先暫存起來
2. `git checkout master`：將自己repo的branch切換到主線(master)
3. `git merge upstream/master`：將本機暫存老師repo的最新版本，合併到自己repo裡面
4. 回GitHub for Windows，按下`Sync`即完成更新

# References

* [Markdown 語法說明](http://markdown.tw/)
* [Dillinger - 一套Markdown的線上編輯器](http://dillinger.io/)
