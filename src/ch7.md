# 7. PGP -- Pretty Good Privacy

## 7.1. copyright
   THE CYPHERNOMICON: Cypherpunks FAQ and More, Version 0.666,
   1994-09-10, Copyright Timothy C. May. All rights reserved.
   請參閱詳細的免責聲明。在「合理使用」條款下可以使用簡短章節，並註明出處，但請勿將我的話冠上你的名字。

## 7.2. SUMMARY: PGP -- Pretty Good Privacy
### 7.2.1. 主要觀點
  - PGP 是目前最重要的 crypto 工具，它單槍匹馬地將 public key 方法傳播到了全世界
  - 許多其他工具正建立在它的基礎之上
### 7.2.2. 與其他章節的關聯
  - 諷刺的是，幾乎不需要了解 PGP 如何運作的細節；有大量的專家專門研究這些
### 7.2.3. 何處尋找更多資訊
  - newsgroups 刊載最新的評論；只要閱讀幾週，許多事情就會浮現
  - 關於 PGP 的各種 FAQ
  + 甚至有一整本書，由 Simpson Garfinkel 撰寫：
    -   PGP: Pretty Good Privacy
          作者 Simson Garfinkel
          第一版 1994 年 11 月 (預計)
          250 頁 (預計), ISBN: 1-56592-098-8, $17.95 (預計)
### 7.2.4. 雜項評論
  - 有大量的 ftp sites, URLs 等等，而且這些都在變動
  - 本文件不可能隨時更新這些資訊——請參閱 newsgroups 中的指標以獲取最新站點

## 7.3. Introduction
### 7.3.1. 為什麼 PGP 值得擁有自己的章節？
  - 像 Clipper 一樣，PGP 是一個太大的議題集，不能沒有自己的章節
### 7.3.2. "Cypherpunks 對 PGP 的迷戀是什麼？"
  - 諷刺的是，我們在 1992 年 9 月的第一次會議，恰好與 PGP 2.0 發布相隔幾天。Arthur Abraham 提供了 2.0 的磁片，並附有雷射列印的標籤。2.0 版是 PGP 第一個真正有用的版本（我是這麼聽說的……我從未試過 1.0 版，它的發行量有限）。所以 PGP 和 Cypherpunks 共享一段歷史——而且 Phil Zimmermann 也參加過一些實體會議。
  - 一個實用、可用、易懂的工具。相當容易使用。相比之下，許多其他發展更為抽象，不適合愛好者和業餘人士使用。光是這一點就確保了 PGP 的崇高地位（這對其他工具的開發者來說可能是一個教訓）。
### 7.3.3. 這裡的觀點集中在 PGP，但也可能適用於類似的 crypto 程式，例如商業 RSA 套件（整合到 mailers、商業程式等中）。

## 7.4. What is PGP?
### 7.4.1. "什麼是 PGP？"
### 7.4.2. "為什麼開發 PGP？"
### 7.4.3. 誰開發了 PGP？

## 7.5. Importance of PGP
### 7.5.1. PGP 2.0 在一個重要的時刻到來
  - 在 1992 年 9 月，正是 Cypherpunks 在加州奧克蘭舉行第一次會議的那一週。（Arthur Abraham 為分發的 PGP 2.0 磁片印製了看起來很專業的標籤。普遍感覺我們是在「正確的時間」組成的。）
  - 就在 Clipper 公告引發對 public key cryptography 的強烈興趣前 6 個月
### 7.5.2. PGP 一直是輿論重大轉變的催化劑
  - 已經教育了成千上萬的使用者了解 strong crypto 的本質
  - 導致了其他工具的出現，包括 encrypted remailers、digital money 的實驗等
### 7.5.3. "如果這東西這麼重要，為什麼不是每個人都對他們的訊息進行 digitally signing？"
  - （以我為例。我從不簽署我的訊息，這份 FAQ 也沒有簽名。也許我以後會。）
  - 便利性、易用性，「所有 crypto 都是經濟學」
  - host Unix機器的不安全性（虛幻的）
  - 需要與 mailers 更好的整合
### 7.5.4. Ripem 似乎已經死了；alt.security.ripem 的流量幾乎為零。PGP 顯然已經贏得了使用者社群的心；現在它是「合法的」……

## 7.6. PGP Versions
### 7.6.1. PGP 版本和實作
  - 2.6ui 是與 2.3 相容的版本
  + 版本 2.6 和 2.6ui 之間有什麼區別？
    - "PGP 2.6 由 MIT 分發，在法律上可供美國和加拿大居民使用。它使用 RSAREF library。它有防止與早期版本 PGP 互通的程式碼。
       "PGP 2.6ui 是 PGP 2.3a 的修改版，功能幾乎與 MIT PGP 2.6 相同，但沒有 MIT PGP 2.6 的「殘廢代碼」。它在法律上僅供美國和加拿大以外地區使用。" [Rat <ratinox@ccs.neu.edu>, alt.security.pgp, 1994-07-03]
  + DOS
    - 版本
    + Pretty Good Shell
      - "當你的 Microsoft Mail 支援外部編輯器時，你可能想試試 PGS (Pretty Good Shell)，在幾個 ftp sites 可以找到 PGS099B.ZIP。它讓你可以從 shell 執行 PGP，並提供一種簡單的方式來編輯/加密檔案。" [HHM LIMPENS, 1994-07-01]
  - Windows
  + Sun
    - "我猜你應該可以使用 PGPsendmail，可在 ftp.atnf.csiro.au:/pub/people/rgooch 取得" [eric@terra.hacktic.nl (Eric Veldhuyzen), PGP support for Sun's Mailtool?, alt.security.pgp, 1994-06-29]
    + Mark Grant <mark@unicorn.com> 一直在開發一個工具來取代 Sun 的 mailtool。"Privtool ("Privacy Tool") 旨在成為標準 Sun Workstation mailtool 程式的 PGP 感知替代品，具有類似的使用者介面和對 PGP-signing 和 PGP-encryption 的自動支援。" [MG, 1994-07-03]
      - "目前，Beta 版本可從 ftp.c2.org 的 /pub/privtool 中取得，檔名為 privtool-0.80.tar.Z，我附上了 README.1ST 檔案，以便你在下載之前檢查功能和錯誤……目前該程式需要 Xview toolkit 來構建，並且僅在 SunOS 4.1 和 Solaris 2.1 上編譯過。"
  + MacPGP
    - 2.6ui: 有問題、炸彈的報告（移除 System folder 中由先前版本設定的 Preferences）
    - "MacPGP 2.6ui 與 MIT 的 MacPGP 2.6 完全相容，但提供了幾個優點，其中一個主要優點是 MacPGP 2.6ui 可透過 AppleScript 控制。這是一個非常強大的功能，並且已經有預先寫好的 AppleScripts 可用。一套稱為 Interim Macintosh PGP Interface (IMPI) 的 AppleScripts 支援透過 drag-n-drop、finder 選擇、剪貼簿對檔案進行加密、解密和簽署，所有這些都可以從系統選單中存取。也存在 Eudora AppleScripts 來將 MacPGP 與郵件程式 Eudora 介接。
       
       "MacPGP 2.6ui v1.2 可透過 anonymous ftp 從以下取得：
       
       FTP SITE                 DIRECTORY
       CONTENTS
       --------                 ---------
       --------
       ftp.darmstadt.gmd.de     pub/crypto/macintosh/MacPGP
       MacPGP 2.6ui, source
       
       
       2.6ui 的 AppleScripts 僅供美國和加拿大公民使用
       透過 anonymous ftp 從以下取得：
       
       FTP SITE                 DIRECTORY
       CONTENTS
       --------                 ---------
       --------
       ftp.csn.net              mpj
       IMPI & Eudora scripts
       
       MacPGP 2.6ui, source
       [phinely@uhunix.uhcc.Hawaii.Edu (Peter Hinely),
       alt.security.pgp, 1994-06-28]
  - Amiga
  + VMS
    - 據說 2.6ui 可以在 VMS 下編譯和執行。
  + 德語版本
    - MaaPGP0,1T1,1
    - dtp8//dtp,dapmqtadt,gmd,de/ilaomilg/MaaP
    - Ahpiqtoph_Pagalies@hh2.maus.
    - (來源: andreas.elbert@gmd.de (A.Elbert). by way of qwerty@netcom.com (-=Xenon=-), 3-31-94
### 7.6.2. 存在哪些版本的 PGP？
  - PGP 2.7 是 ViaCrypt 的 PGP 2.6 商業版本
### 7.6.3. PGP 2.6 議題
  - 在媒體和討論群組中，關於 2.5, 2.6, 2.6ui 及其各種版本的議題存在很多困惑。動機、陰謀論等都被討論過。我不像名單上的其他人那樣參與其中，所以我經常也很困惑。
  + 以下是 Phil Zimmermann 針對一篇誤導性新聞報導的回應：
    - "PGP 2.6 將永遠能夠讀取舊版本的訊息、簽名和金鑰，即使在 9 月 1 日之後。舊版本將無法讀取 PGP 2.6 在 9 月 1 日之後產生的訊息、簽名和金鑰。這是一個完全不同的情況。人們有充分的理由切換到 PGP 2.6，因為它將能夠處理兩種資料格式，而舊版本則不能。在 9 月之前，新 PGP 將繼續產生舊版本可以讀取的舊格式，但在該日期之後將開始產生新格式。這種延遲讓每個人都有時間獲取新版本的 PGP，這樣他們就不會受到變更的影響。Key servers 仍然能夠攜帶舊格式製作的金鑰，因為 PGP 2.6 仍然可以毫無問題地讀取它們。" [Phil Zimmermann, 1994-07-07, 也發佈到 Usenet groups] [此處所有日期均指 1994 年]
    - "我開發 PGP 2.6 是為了由 MIT 發布，我認為這個新安排是 PGP 法律地位的突破，對所有 PGP 使用者都有利。我敦促所有 PGP 使用者切換到 PGP 2.6，並放棄早期版本。用這個新版本的 PGP 廣泛取代舊版本符合建立 PGP 標準的未來計畫。" [Phil Zimmermann, 1994-07-07, 也發佈到 Usenet groups]
### 7.6.4. PGP 版本 2.6.1
  - "MIT 將很快發布 Pretty Good Privacy (PGP) 2.6.1 版。我想明天吧。MSDOS 發布檔名將是 pgp261.zip，原始碼將在 pgp261s.zip 中。MIT FTP 站點是 net-dist@mit.edu，在 pub/PGP 目錄中。" [由 Derek Atkins 更正為：net-dist.mit.edu，不是 net-dist@mit.edu。]
     
     "這個新版本比 2.6 版有很多錯誤修復。我希望這是這個 PGP 原始碼家族的最後一個版本。我們一直在開發一個全新的 PGP 版本，從頭開始重寫，它更乾淨、更快，更適合我們計畫的未來增強功能。在這個 2.6.1 版本之後，所有 PGP 開發工作都將轉向這個新代碼庫。" [Phil Zimmermann, Cypherpunks list, 1994-09-02]

## 7.7. Where to Get PGP?
### 7.7.1. "我在哪裡可以在 CompuServe 上獲得 PGP？"
  - 注意：我無法追蹤各種 crypto 套件的主要 ftp sites，更不用說像這樣的服務資訊了。但是，這裡有：
  - "截至 1994 年 7 月 5 日："
     GO EURFORUM / Utilities   PGP26UI.ZIP   PGP 2.6ui
     GO PWOFORUM / New uploads PGP26.ZIP     PGP 2.6
      PWOFORUM 也有原始碼和文件，加上一些 PGP 的 shell 工具。2.3a 版也還在。" [cannon@panix.com, Kevin Martin, PGP on Compuserve??, alt.security.pgp, 1994-07-08]
### 7.7.2. 離線 PGP
  + ftp.informatik.uni-hamburg.de:/pub/virus/crypt/pgp/tools/pgp-elm.zip
    - 另一個地方：Crosspoint: ftp.uni-kl.de:/pub3/pc/dos/terminal/xpoint XP302*.EXE
  + "我強烈推薦 Offline AutoPGP v2.10。它可以與幾乎任何支援 .QWK 封包的離線郵件閱讀器無縫運作。共享軟體註冊費為 10.00 美元。作者是 Staale Schumacher，奧斯陸大學的學生，聯絡方式 staale@ifi.uio.no。該程式現在應該在美國的 bbs 上廣泛可用。我經常使用該程式處理 bbs 郵件。這真是一個相當不錯的作品。如果你找不到它，給我留個條子。"
     [bhowatt@eis.calstate.edu Brent H. Howatt, PGP in an offline reader?, alt.security.pgp, 1994-07-05]
    - oak.oakland.edu 在 /pub/msdos/offline, 版本 2.11
    - ftp.informatik.uni-hamburg.de:/pub/virus/crypt/pgp/tools/apgp211.zip
### 7.7.3. "我應該擔心獲取和編譯 PGP 原始碼嗎？"
  - 嗯，除非你是 PGP 內部的專家，何必麻煩呢？而且隨機數產生器中的一個微妙錯誤甚至連 Colin Plumb 都曾忽略了一段時間。
  - 原始碼可用的價值在於其他人如果願意，可以確認執行檔與原始碼對應。這_可以_做到對我來說就足夠了。（策略：保留代碼一段時間，等待缺陷或漏洞的報告，然後放心地使用。）
  - 簽名可以被檢查。也許有一天會有時間戳記版本。
  - 坦白說，一個人的訊息或假名身分透過其他方式暴露的機率比 PGP 被攻破的機率高得多。發送訊息時的失誤有時會洩露身分，無意中的評論和風格線索也是如此。

## 7.8. How to Use PGP
### 7.8.1. PGP 如何運作？
### 7.8.2. "我應該如何儲存我的金鑰的秘密部分？我可以背下來嗎？"
  - 現代 ciphers 使用的金鑰遠遠超出了記憶（甚至輸入！）的範圍。金鑰通常儲存在個人的家用機器上，或相當安全的機器上，或磁片上。Passphrase 應該始終背下來或寫下來（呃）放在錢包或其他類似的地方。掛在脖子上的安全「dongles」，或戒指或手錶，最終可能會被使用。Smartcards 和 PDAs 是一個更有可能的中間解決方案（許多 PC 現在有 PCMCIA 卡插槽）。
### 7.8.3. "我如何簽署訊息？"
  - 參見 PGP 文件
  + 然而，這在 List 上被提出過，並且：
    -
    + pgp -sta +clearsig=on message.txt
      -
      - 那是來自 pgpdoc2.txt。希望有幫助。你可能
         希望設定你的郵件
      - user agent 在退出你的
         預設訊息編輯器時呼叫此命令，
      - 將 "message.txt" 設定為你的編輯器呼叫的
         臨時訊息
      - 檔案。               <Russell Whitaker,
         whitaker@sgi.com, 4-15-94, Cypherpunks>
### 7.8.4. 為什麼 PGP 不更容易使用？
  - 與其他可能的 crypto 應用（如 digital money 或投票系統）相比，它實際上_非常_容易使用
  - 語義鴻溝……學習
### 7.8.5. 我應該如何學習 PGP？
### 7.8.6. "PGP 與其他程式整合的狀況如何？"
  + 編輯器
    + emacs
      + emacs 支援 pgp，可能有各種版本（我看過幾個不同套件的報告）..內建語言當然有幫助
        - Rick Busdiecker <rfb@lehman.com> 有一個 emacs 前端可用於 PGP
        - Jin S. Choi <jsc@monolith.MIT.EDU> 曾經描述過他用 elisp 寫的一個支援 GNU emacs 的套件："mailcrypt"
        - 可能還有更多
  + Mailers
    - 也就是說，有沒有任何 mailers 與 PGP 有良好的連結？需要掛鉤到現有的 mailers
    + emacs
      + emacs 支援 pgp，可能有各種版本（我看過幾個不同套件的報告）..內建語言當然有幫助
        - Rick Busdiecker <rfb@lehman.com> 有一個 emacs 前端可用於 PGP
        - Jin S. Choi <jsc@monolith.MIT.EDU> 曾經描述過他用 elisp 寫的一個支援 GNU emacs 的套件："mailcrypt"
        - 可能還有更多
    - elm
    - Eudora
    + PGP sendmail 等
      - "獲取 PGPsendmail Suite，幾天前在這裡宣布過。可從 anonymous ftp 取得：
         ftp.atnf.csiro.au: pub/people/rgooch   (澳洲)
         ftp.dhp.com: pub/crypto/pgp/PGPsendmail(美國)
         ftp.ox.ac.uk: src/security  (英國)... 它的運作方式是
         包裹常規的 sendmail 程式，所以
         你可以獲得所有 mailers 的自動加密，而不僅僅是
         Rmail。" [Richard Gooch, alt.security.pgp, 1994-07-10]
    + MIME
      - MIME 和 PGP <Derek Atkins, 4-6-94>
      - [以下資料取自 remijn@athena.research.ptt.nl 轉發給 Cypherpunks list 的公告，1994-07-05]
      - "MIME [RFC-1341, RFC-1521] 定義了一種格式和通用框架，用於在 Internet 郵件中表示各種資料類型。本文件定義了一種特定的 MIME 資料類型，即 application/pgp 類型，用於 Internet 郵件中的「相當好」的隱私、身分驗證和加密。application/pgp MIME 類型旨在促進跨各種硬體和軟體平台的私人郵件的更廣泛互通。
  + Newsreaders
    - 對於自動簽署/驗證，以及從 newsreader 內部發送電子郵件很有用
    - yarn
    - tin
    - 據報導 "yarn" newsreader 內建了 PGP。
### 7.8.7. "我應該多久更換一次我的金鑰？"
  - Hal Finney 指出，許多人似乎認為 PGP 金鑰是準永久的。事實上，從不更換金鑰是招致災難的邀請，因為金鑰可能會以各種方式洩露（按鍵記錄程式、隨處亂放的磁片，甚至 rf 監控），並且可能被破解。
  - "
  + "什麼是更換金鑰的好間隔？我建議
     大約每年一次
    - 有道理，特別是如果基礎設施可以
       發展得更容易
    - 傳播金鑰變更。金鑰應該在時間上重疊，
       這樣你製作
    - 一個新金鑰並開始使用它，同時繼續支援
       舊金鑰一段
    - 時間。<Hal Finney, hfinney@shell.portal.com, 4-15-94,
       cypherpunks>
  - Hal 也建議 remailer 站點更頻繁地更換金鑰，也許每月一次。

## 7.9. Keys, Key Signings, and Key Servers
### 7.9.1. Web of trust 與階層式金鑰管理
  - Phil Zimmermann 的一個關鍵創新是使用 "web of trust" 模型來進行分散式金鑰信任。
  - 局部性，使用者承擔成本
  - 相比之下，政府估計每年需要 10-20 億美元來為大部分人口營運金鑰認證機構
  - "PGP 是關於選擇和構建適合你需求的 web of trust。PGP 支援完全去中心化、個人化的 web of trust，也支援你能想像到的最結構化、官僚化的中心化方案。僅依賴個人化 web of trust 的一個問題是它限制了你的通訊對象範圍。我們不能指望 Phil Zimmermann 和少數知名人士簽署每個人的金鑰，我也不想將我的私人通訊限制在我認識和信任的人，加上那些金鑰被我認識和信任的人簽署的人。" [William Stallings, SLED key verification, alt.security.pgp, 1994-09-01]
### 7.9.2. 簽署他人金鑰的實用方法
  + 簽署你認識並希望通訊的人的金鑰
    - 面對面相遇（"這是我的金鑰。"）
  + 信任——在不同程度上——由你認識的其他人簽署的金鑰
    - web-of-trust
  - 信任——在較小程度上——金鑰註冊處的人的金鑰
### 7.9.3. Key Servers
  + 有幾個主要站點似乎很穩定
    + MIT PGP Public Key Server
      - 透過 www.eff.org
    + 漢堡大學的 Vesselin Bontchev 營運一個非常穩定的站點：
      - Ftp:    ftp.informatik.uni-hamburg.de
         IP:     134.100.4.42
         Dir:    /pub/virus/crypt/pgp/
         File:   pubkring.pgp
         E-Mail: pgp-public-keys@fbihh.informatik.uni-hamburg.de
    - pgpkeys.io.com
  + http://martigny.ai.mit.edu/~bal/pks-commands.html
    - 這是一個在蘇黎世的 PGP keyserver。<Russell Whitaker, 7 April 1994>
    -
### 7.9.4. PGP key fingerprints 的使用
  - "Key fingerprints 的較好用途之一是包含在簽名檔和其他金鑰本身太龐大的地方。透過廣泛傳播 fingerprint，未檢測到偽造金鑰的機會會降低，因為有更多管道讓 fingerprint 到達接收者，也有更多管道讓金鑰擁有者看到網路上任何偽造的 fingerprints。[Bill Stewart, 1994-08-31]
### 7.9.5. "地址變更該如何處理？舊金鑰必須撤銷嗎？"
  - 未來的 PGP 版本可能會處理得更好
  - 一種方法是發布……"User-id revocation certificates 是一個*好*主意，PGP 金鑰格式允許它們——也許有一天 PGP 會對此做點什麼。" [Paul Allen, alt.security.pgp, 1994-07-01]
  - 持久的電子郵件地址是一種方法。有些人使用像 ACM 這樣的組織來提供此服務（例如，Phil Zimmermann 是 prz@acm.org）。其他人使用重新映射服務。例如，"我註冊了 SLED (Stable Large E-mail Database)，這是一個交叉引用資料庫，用於隨著時間的推移將舊的、過時的電子郵件地址與當前的連結起來……任何使用此金鑰的人將始終能夠透過以 "blbrooks..." 為關鍵字進行搜尋在 SLED 上找到我。因此我的金鑰和相關簽名始終保持有效……如果你對 SLED 感興趣，它的地址是 sled@drebes.com。" [Robert Brooks, alt.security.pgp, 1994-07-01]
### 7.9.6. "我如何確保我的金鑰沒有被篡改？"
  + 保持你的 private key 安全
    + 如果在不安全的機器上，採取措施保護它
      - 離線儲存（Perry Metzger 每天早上載入他的金鑰，並在離開機器時移除它）
    + 背下你的 PGP passphrase 並且不要寫下來，至少不要寫在 private key 可用的任何地方附近
      - 交給律師的密封信封、保險箱等都是可能性
      - 鑑於如果 passphrase 永久遺失幾乎不可能恢復檔案，我建議將其儲存在_某個地方_，儘管安全性略有損失（這是一個爭論的話題……我個人覺得知道我的記憶在某處有備份會更舒服）
  - Colin Plumb 指出，如果有人可以存取你的個人 keyring，他們可能也可以存取你的 PGP 程式並*直接*對其進行修改。
  - Derek Atkins 在 sci.crypt 上回答了一個類似的問題："當然。你可以使用 PGP 來驗證你的 keyring，並使用 web-of-trust，你可以讓它驗證你簽署的所有金鑰上的簽名，並遞迴遍歷你的朋友圈。要驗證你自己的金鑰沒有被破壞，你可以用你的 secret key 簽署一些東西，然後嘗試驗證它。這將確保你的 public key 沒有被破壞。" [Derek Atkins, sci.crypt, 1994-07-06]
### 7.9.7. "為什麼需要金鑰撤銷？"
  - 金鑰撤銷是 "ebb-of-trust"
  - "有許多真正的原因。也許你被迫簽署了金鑰，或者你認為金鑰簽署不正確，或者那個人不再使用該電子郵件地址，因為他們失去了帳戶，或者你不相信金鑰與 userID 的綁定是有效的，原因有很多。" [Derek Atkins, 4-28-94]
### 7.9.8. "Is-a-person" 註冊處
  + 有人提議政府可以且應該建立「法人」註冊處。這在 crypto 社群中被稱為 "is-a-person" 憑證，各種論文（特別是 Fiat-Shamir）已經處理了這些問題
    - 惡意政府的欺騙
    - 人員追蹤的危險
  + 我們在這裡需要非常小心！
    - 這可能會限制 'ad hoc crypto' 的傳播（我指的是出於個人使用以外的原因使用本地生成的金鑰……digital cash, pseudonyms 等）
    - 任何「發放」許可證以允許生成金鑰的系統都是危險的！
  + 可能是政府想要進入的一個領域。
    - 類似 Fiat-Shamir "passport" 議題（Murdoch, 利比亞例子）
  - 我支持自由市場——對我可以使用哪些註冊處沒有限制
### 7.9.9. Keyservers（此列表不斷變化，但大多數共享金鑰，所以只需要一個）。發送 "help" 訊息。欲了解最新資訊，請關注 alt.security.pgp。
  - 截至 1994 年 8 月，主要 keyservers 上約有 6000 個金鑰。
  - pgp-public-keys@martigny.ai.mit.edu
  - pgp-public-keys@dsi.unimi.it
  - pgp-public-keys@kub.nl
  - pgp-public-keys@sw.oz.au
  - pgp-public-keys@kiae.su
  - pgp-public-keys@fbihh.informatick.uni-hamburg.de
  - wasabi.io.com 提供透過 finger 獲取 public keys（我無法讓它運作）
### 7.9.10. "什麼是 key fingerprints 以及為什麼使用它們？"
  - "分發 key fingerprint 允許 J. Random Human 將透過一種方法提供的金鑰與透過另一種方法提供的金鑰相關聯。例如，現在我有 Betsi 金鑰的 fingerprint，我可以驗證我看到的任何其他聲稱的 Betsi 金鑰是否真實……讀取和交叉檢查 32 個字元的 fingerprints 比整個 key block 容易得多，特別是隨著簽名的增加和 key block 大小的增長。" [Paul Robichaux, 1994-08-29]
### 7.9.11. Betsi
  - Bellcore
  - key signing
### 7.9.12. 關於對 keyservers 的攻擊……
  + 對 keyservers 的洪水攻擊已經開始；這可能是試圖透過使用淫穢、種族主義、性別歧視的短語作為金鑰名稱來關閉 keyservers（Cypherpunks 不會支持因為像辱罵、冒犯性語言這樣微不足道的事情而關閉站點，但許多其他人會。）
    - "看來有些幼稚的混蛋玩得很開心，生成偽造的 PGP 金鑰並將它們上傳到公共 keyservers。這是我在 keyserver 上發現的一些金鑰：...[金鑰省略]..." [staalesc@ifi.uio.no, alt.security.pgp, 1994-09-05]

## 7.10. PGP Front Ends, Shells, and Tools
### 7.10.1. 許多可以在這個 ftp site 找到：
  + ftp.informatik.uni-hamburg.de:/pub/virus/crypt/pgp/shells/
    - 用於 PGP 的各種 shells 和前端
### 7.10.2. William Stallings 在 Usenet 貼文中這樣說：
  - "PGPShell: 直接在 DOS 版本上執行，不需要 Windows。介面不錯，簡單。freeware
     
     "PGP Winfront: freeware windows 前端。使用「控制台」風格，以緊湊的方式顯示許多選項。
     
     "WinPGP: shareware ($45)。使用下拉式選單風格，這在許多 Windows 應用程式中很常見。" [William Stallings, Looking for PGP front end, alt.security, 1994-08-31]
### 7.10.3. Rick Busdiecker <rfb@lehman.com> 有一個 emacs 前端可用於 PGP
### 7.10.4. Pr0duct Cypher 的工具：
  + ftp.informatik.uni-hamburg.de:/pub/virus/crypt/pgp/tools/PGPTools.tar.gz
    - Pr0duct Cypher 的工具，以及其他一般工具

## 7.11. Other Crypto Programs And Tools
### 7.11.1. 其他 Ciphers 和工具
  - RIPEM
  - PEM
  - MD5
  + SFS (Secure FileSystem) 1.0
    - "SFS (Secure FileSystem) 是一組程式，用於建立和管理多個加密磁碟卷，並在 DOS 和 Windows 下執行。每個卷看起來像一個普通的 DOS 磁碟機，但儲存在其上的所有資料都在個別磁區層級進行加密……SFS 1.1 是一個維護版本，修復了 1.0 中的一些小問題，並增加了使用者建議的一些功能。有關變更的更多詳細資訊在 README 檔案中給出。" [Peter Gutmann, sci.crypt, 1994-08-25]
    - 與 CFS 不是同一個東西！
    - 使用 MDC/SHS hash 的 512-bit 金鑰。（快速）
    - 只能在 386 或更好的機器上運作（V. Bontchev 說）
    - 原始碼不可用？
    - 實作為 device driver（而不是像 SecureDrive 那樣的 TSR）
    - "容易受到一種特殊形式的攻擊，這在 sci.crypt 中提到過一次，並在 SFS 文件中有詳細描述。看看「加密考量」一節。" [Vesselin Bontchev, sci.crypt, 1994-07-01]
    - 比較 SFS 和 SecureDrive："兩個套件在使用者介面方面大致相當，但 SFS 似乎快得多。而且來自各個人的評論（先前的訊息串）似乎表明它也更「安全」。" [Bill Couture <coutu001@gold.tc.umn.edu> , sci.crypt, 1994-0703]
  + SecureDrive
    - 加密磁碟（總是要非常小心！）
    - SecureDrive 1.3D, 128-bit IDEA cypher 基於 passphrase 的 MD5 hash
    - 實作為 TSR（而不是像 CFS 那樣的 device driver）
    - 原始碼可用
    + 報告了一些問題（你的情況可能有所不同）
      - "我的加密磁碟機破壞檔案遇到了一些困難。在我的硬碟上安裝 secure drive 1.3d 後，我發現各種檔案被損壞，並且多次存取磁碟機後出現一堆交叉連結的檔案。" [Vaccinia@uncvx1.oit.unc.edu, 1994-07-01]
    - 其他人報告在 DOS 和 Windows 下使用都很滿意
    - 沒有報告 OS/2 或 Mac 版本；有人說必須使用 OS/2 device driver（例如 Stacker for OS/2 使用的）
  + SecureDevice
    - "如果你在其他地方找不到，我有它在 ftp://ftp.ee.und.ac.za/pub/crypto/secdev13.arj，但那是在飽和的 64kbps 連結的末端。" [Alan Barrett, 1994-07-01]
### 7.11.2. MDC 和 SHS (與 SHA 相同？)
  - "MDC cyphers 被認為是安全的，其強度取決於反轉它們使用的 cryptographic hash function 的難度。SHS 由 NSA 設計，被認為是安全的。可能有其他方法攻擊 MDC cyphers，但沒有被允許發言的人知道這些方法。" [Vesselin Bontchev, sci.crypt, 1994-07-01]
  + Secure Hash Standard 的演算法是公開的，因此可以分析和測試弱點（與 Skipjack 形成強烈對比）。
    - 可能在未來的 PGP 版本中取代 MD5（傳言）
  - MDC 的速度："這是一個速度權衡。MDC 比 IDEA 快幾倍，所以 SFS 比 SecureDrive 快幾倍。但 MDC 較未經證實。" [Colin Plumb, sci.crypt, 1994-07-04]
  + 關於 SHA 問題的傳言
    - "另一個大新聞是 Secure Hash Algorithm (SHA) 的安全問題，在 94 年 4 月的 DDJ 中討論過。NSA 的密碼學家發現了演算法的一個問題。他們不會告訴任何人它是什麼，甚至不說有多嚴重，但他們承諾很快會修復。每個人都屏息以待。" [Bruce Schneier, reprot on Eurocrypt '94, 1994-07-01]
### 7.11.3. Stego 程式
  + DOS
    - S-Tools (或 Stools?)。DOS？加密在 .gif 和 .wav (SoundBlaster 格式) 檔案中。可以設定不顯示內部有加密檔案。
  - Windows
  + Macintosh
    - Stego
    + 聲音程式
      - marielsn@Hawaii.Edu (Nathan Mariels) 寫了一個程式，"獲取一個檔案並使用使用者輸入的密碼的 MD5 hash 用 IDEA 加密它。然後將檔案儲存在聲音檔案的最低位元（或多個位元，使用者可選）中。"
### 7.11.4. "關於 "Pretty Good Voice Privacy" 或 "Voice PGP" 和其他語音程式呢？"
  + 據說有幾個團體，包括 Phil Zimmermann 領導的一個，正在研究類似的東西。大多數使用商業上廣泛可用的聲音輸入卡，類似 "SoundBlaster" 卡。
    - 專有硬體或 DSPs 通常是失敗的，因為人們無法輕易獲得硬體；純軟體解決方案（可能依賴內建硬體，或現成的附加卡，如 SoundBlasters）是較好的。
  + 做這樣一個專案有許多重要理由：
    - 擴散更多 crypto 工具和系統
    - 搶在 "Digital Telephony II" 和 Clipper 類型系統之前推出；讓工具如此普及以至於難以取締
    - 人們以比電子郵件更自然的方式理解語音通訊，所以不使用 PGP 的人可能仍會使用語音加密系統
  + Eric Blossom 有他自己的努力，並在 Cypherpunks 會議上展示了硬體：
    - "目前我們的主要努力是開發一系列可擴展的協定，用於點對點連結上的加密和語音。我們打算盡可能使用現有標準。
       
       "我們目前計畫建立在 PPP 的 RFCs 之上（見 RFCs 1549, 1548, 和 1334）。基本想法是增加一個新的 Link Control Protocol（或可能是 Network Control Protocol），它將協商基數和模數並執行 DH key exchange。RFCs 已經支援某些形式的 Authentication。我們正在研究其他的。" [Eric Blossom, 1994-04-14]
  + 建立在 Macintoshes 和 Windows 的多媒體功能之上可能是一個更容易的方法
    - 幾乎所有的 Macs 和 Windows 機器很快都將具備多媒體/視聽功能
    - "我意識到設計一個帶有 Vocoder、數據機和一些 cpu 能力來進行加密的安全電話是完全可能的，但我認為一個更容易的解決方案可能即將出現……我相信 Microsoft 和許多其他人正在探索將電話連接到 PC，這樣人們就可以做像把週末樂趣的照片傳送給朋友這樣的事情。當 PC 可以輕鬆存取電話通訊時，開發加密對話應該就像為 Windows 寫程式一樣容易 :-)。" [Peter Wayner, 1993--07-08]
### 7.11.5. Random Number Generators
  - 一個巨大的領域……
  + 混沌系統，擺
    - 可能有意想不到的週期性（相空間圖顯示吸引盆，即使行為看似隨機）
### 7.11.6. "NIST 和 RSADSI 關於 DSS 的爭議情況如何？"
  - NIST 聲稱它不侵犯專利
  - RSADSI 購買了 Schnorr 專利並聲稱 DSS 侵犯了它
  - NIST 不做保證，也不賠償使用者 [Reginald Braithwaite-Lee, talk.politics.crypto, 1994-07-04]
### 7.11.7. "有沒有像 telnet 或 "talk" 這樣使用 pgp 的程式？"
  - "不知道 Telnet，但我希望能看到 "talk" 像那樣安全……它存在。（也就是 PGP 化的 ytalk。）看看 ftp.informatik.uni-hamburg.de:/pub/virus/crypto/pgp/tools/pgptalk.2.0.tar.gz" [Vesselin Bontchev, alt.security.pgp, 1994-07-4]
### 7.11.8. Digital Timestamping
  + 有兩種口味：
    - 玩具或遊戲版本
    - 真實或商業版本
  + 對於遊戲版本，發送訊息給 "timestamp@lorax.mv.com"，它將被加上時間戳記並返回。顯然這不能證明什麼，尚未在法庭上測試過，僅依賴於時間戳記者的聲譽。（一個致命缺陷：重置電腦上的系統時鐘從而更改日期是微不足道的。）
    - "傳聞"等價物：由*不*使用 Haber 和 Stornetta 的 "widely witnessed event" 方法的伺服器提供的時間戳記
  - Haber 和 Stornetta 的版本當然更令人印象深刻，因為它依賴於比僅僅信任他們正確設定了電腦系統時鐘更強大的東西！

## 7.12. Legal Issues with PGP
### 7.12.1. "RSA Data Security Inc. 對 PGP 的立場是什麼？"
 I. 他們強烈反對早期版本
II. 反對意見
    - 侵犯 PKP 專利（聲稱侵權，但未在法庭上測試）
    - 打破了先前看到的嚴格控制
    - 給 public key 方法帶來了不必要的關注（我認為 PGP 也幫助了 RSA 和 RSADSI）
    - Zimmermann 和 Bidzos 之間的嫌隙
III. 反對意見
    - 侵犯 PKP 專利（聲稱侵權，但未在法庭上測試）
    - 打破了先前看到的嚴格控制
    - 給 public key 方法帶來了不必要的關注（我認為 PGP 也幫助了 RSA 和 RSADSI）
    - Zimmermann 和 Bidzos 之間的嫌隙
IV. 關於訴訟、行動等的談論
 V. 2.6 MIT 的和解可能減輕了緊張局勢；純屬猜測
### 7.12.2. "PGP 是合法還是非法的"？
### 7.12.3. "RSADSI 和 PRZ 之間還有衝突嗎？"
  - 顯然沒有。MIT 2.6 的談判似乎已經埋葬了所有這些積怨。至少在官方上。我聽說仍然有敵意，但不再浮於表面。（而且 RSADSI 現在面臨訴訟和專利訴訟。）

## 7.13. Problems with PGP, Flaws, Etc.
### 7.13.1. 關於可能攻擊 PGP 的推測
  + 定期會有問題報告，大多數只是謠言。這些大多被更有知識的人駁回。當然，真正的缺陷可能存在，就像任何軟體一樣。
    - Colin Plumb 承認 PGP 2.6 的隨機數產生過程中有一個缺陷，將在後續版本中修復。
  + 散播恐懼、不確定和懷疑
    - 關於 PGP 版本安全性的謠言
    - 選擇性起訴 PGP 使用者
    - 死亡威脅（類似針對 Bidzos 的）
  - 在使用者社群中播種混亂
  - 使其分裂（也許透過多個、不互通的版本……就像我們現在開始看到的？）
### 7.13.2. NSA 知道 PGP 的什麼缺陷？
  - 他們不說。諷刺的是，這違反了他們章程中關於使商業安全更強大的部分。現在 PGP 是合法的，他們應該幫助使其更強大，當然不應該對他們知道的弱點保持沉默。但要他們幫助加強 PGP 其實不太可能。
### 7.13.3. PGP 定時炸彈
  - （正如我在別處說過的，這一切都變得很混亂。許多版本、許多站點、許多觀點、許多工具、許多 shells、許多其他東西。幸運的是，大部分都是廢話。）
  - 我不對透過使用 2.6ui 避免「定時炸彈」採取任何立場——出於各種原因。這是別人的評論："我想藉此機會鼓勵你升級到 2.6ui，這將克服 mit 的定時炸彈，並且不排除 PGP 2.3a 解密訊息……不要使用 MIT 的 2.6，使用可從 soda.berkeley.edu : /pub/cypherpunks/pgp 獲得的 PGP 2.6ui" [Matrix at Cypherpunks, BLACK THURSAY!, alt.security.pgp, 1994-09-01]
  + 也可以用 "legal kludge" 擊敗：
    - ftp.informatik.uni-hamburg.de : /pub/virus/crypt/pgp/legal_kludge.txt
### 7.13.4. Spoofing
  - "適當的時間限制，特別是即時限制，可以用來阻礙，甚至可能擊敗 spoofing 攻擊。但是對於 store-and-forward 電子郵件系統（如 PGP 設計配合的），這些限制通常無法設定。" [Ken Pizzini , sci.crypt, 1994-07-05]
### 7.13.5. "我們怎麼知道 PGP 沒有後門或其他重大缺陷？畢竟，我們不都是程式設計師或密碼學家。"
  - 是的，但我們許多人是。許多人分析過 PGP 的原始碼，自己編譯過代碼（這是獲取執行檔的一種相當常見的方式），並檢查過隨機數產生器、質數的選擇以及所有其他數學運算。
  + 只需要一個眼尖的人就能揭發插入缺陷或後門的陰謀。這還沒有發生。（雖然 Colin Plumb 承認 2.6 的 RNG 有輕微弱點……正在修復中。）
    - "雖然有原始碼可用並不能保證程式是安全的，但它有很大幫助。即使許多使用者不是程式設計師或密碼學家，其他人是，其中許多人會仔細檢查代碼，並公開大聲疾呼他們注意到或認為注意到的弱點。例如，顯然這裡曾對 PGP 2.6 中的 xorbytes() 錯誤進行過大討論。將此與商業程式對比，那裡的這種錯誤可能會多年未被發現。" [Paul Rubin, alt.security.pgp, 1994-09-06]
### 7.13.6. "我可以在我不控制的機器上執行 PGP 嗎，例如校園電腦系統？"
  - 當然，但 sysops 和其他人可能因此能夠存取你的金鑰和 passphrase。只有使用者直接控制且與其他機器有足夠防火牆隔離的機器，才提供合理數量的安全性。如果 PGP 程式在公司電腦或大學網路上執行，爭論 1024-bit keylengths 是否「足夠」是相當沒有意義的。安全的幻覺可能存在，但沒有真正的安全性。太多人自欺欺人地認為他們的訊息是安全的。他們的電子身分無法被 spoofed。
  - 我對各種 elm 和 emacs PGP 套件不感興趣（存在幾個這樣的 shells 和 wrappers）。任何 sysop 不僅可以獲取儲存在他系統上的你的 secret key，而且當你將 passphrase 輸入 PGP 程式時（假設你會……許多人也自動化這部分），他也可以擷取你的 passphrase。因為這個 sysop 或他的一個同夥隨後可以破壞你的郵件，以「你」的名義簽署訊息和合約，我認為這完全不可接受。其他人顯然不這麼認為。
  - 能做什麼？我們許多人只在家用機器上，或我們直接控制的機器上執行 PGP。有些在這些機器上使用 PGP 的人至少採取措施更好地保護事物……例如，Perry Metzger 曾經描述過他每天經歷的多階段過程，以他覺得準安全的方式重新載入他的金鑰材料。
  - 直到 "Internet-in-a-box" 或 TIA 類型的產品更加普及，許多人將把家庭或辦公室機器連接到他們不控制的其他系統。（為了更清楚地說明這一點：你希望你的電子貨幣從你的 sysop 和他的朋友可以監控的帳戶中流出嗎？絕不。"Electronic purses"，可能是 smart cards, Newton 類型的 PDAs, 或 dongle 類型的戒指或吊墜，顯然是需要的。這是另一個完整的討論。）

## 7.14. The Future of PGP
### 7.14.1. "PGP 對一般的 public key 方法，特別是 RSA Data Security Inc. 是有幫助還是有害？"
  - 結果尚未定論，但總的來說，我認為 RSADSI 的地位因 PGP 產生的宣傳而得到幫助。PGP 的使用者在許多情況下將「畢業」到完全授權的版本。公司隨後將使用 RSADSI 的產品。
  + 有趣的是，PGP 可以做 RSADSI 不準備做的「激進」事情。（Cypherpunks 熟悉的用途。）
    - 繞過出口限制就是這方面的一個例子
    - 納入實驗性 digital cash 系統
  - 寄生通常會增加演化的速度。PGP 肯定有助於在 RSADSI 下點火。
### 7.14.2. Stealth PGP
  - Xenon, Nik, S-Tools,
### 7.14.3. "我們應該致力於一個更進階的版本，一個 *Really Good Privacy* 嗎？"
  - 說起來容易做起來難……強烈的時間承諾
  - 不清楚需要什麼……
### 7.14.4. "可以對 PGP 進行更改和改進嗎？"
  - 我認為這是我們這個時代最大的諷刺之一，Phil Zimmermann 譴責 Tom Rollins 對他提供的 PGP 版本進行各種更改。
  + 議題：
    - Phil 的聲譽，以及 PGP 的聲譽
    - 智慧財產權
    - GNU Public license
    - PGP 的名稱本身
    - 考慮到 RSA 說過大致相同的話，即 PGP 會降低 public key 的聲譽（特別是因為 Phil 是一個「業餘愛好者」，這正是 PRZ 用來批評 Tom Rollins 的措辭！）
  - 我不在這裡表明立場……我不知道細節。只是一些諷刺。

## 7.15. Loose Ends
### 7.15.1. 登入、密碼等的安全措施
  - 避免透過網路輸入密碼（例如在 rlogins 或 telnets 中）。如果某人或某個 agent 索要你的密碼，請保持偏執。
  - 可以使用 encrypted telnet，或像 Kerberos 之類的東西，以避免在機器之間以明文發送密碼。有很多方法，幾乎沒有一種被普遍使用（至少我從未見過）。
