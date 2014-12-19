#Git Objects

Git 核心是物件儲存，物件包含了資料檔案、歷史記錄訊息、作者資訊、日期、branch 訊息等資訊。

Git 由四種物件組合而成，包含：

##Blobs

Blob 儲存檔案內容sha-1，與檔名無關，Git 使用內容定址檔案系統(content-addressable filesystem)
Blob 沒有 metadata，沒有檔名資訊。

檔案內容相同Git 只會儲存一份，相同的檔案內容，檔案sha-1 也會一樣。

##Tree

Tree Object 儲存檔案目錄資訊，包含目錄底下的檔案名稱、blob sha-1、檔案類型、路徑名稱。

##Commits

Commit Object 儲存commit 作者、commit 時間、commit 作者。

每個commit 都會指向一個Tree Object ，除了一開始的第一個commit object

##Tags

Tag Object 通常儲存專案版本號(如 Ver-1.0.1)，Tag 是一個好閱讀標簽名稱物件。

======================

Git 是一個定址檔案系統(content-addressable filesystem)，透過物件指向連接檔案。


