# 9. Policy: Clipper, Key Escrow, and Digital Telephony

## 9.1. copyright
   THE CYPHERNOMICON: Cypherpunks FAQ and More, Version 0.666,
   1994-09-10, Copyright Timothy C. May. All rights reserved.
   請參閱詳細的免責聲明。在「合理使用」條款下可以使用簡短章節，並註明出處，但請勿將我的話冠上你的名字。

## 9.2. SUMMARY: Policy: Clipper, Key Escrow, and Digital Telephony
### 9.2.1. 主要觀點
  - Clipper 已成為主要的團結力量，因為 80% 的美國人和 95% 的計算機類型人員都反對它。
  - "Big Brother Inside"（老大哥在裡面）
### 9.2.2. 與其他章節的關聯
  - 主要聯繫是_法律_
  - 對加密限制的一些可能影響
### 9.2.3. 何處尋找更多資訊
  - 關於 Clipper 的文章有數百篇，幾乎出現在所有流行雜誌上。其中許多已發送到 Cypherpunks 列表，並可能在檔案中找到。（我有至少 80 MB 的 Cypherpunks 列表資料，其中很多是關於 Clipper 的報紙和雜誌文章！）
  + 更多 Clipper 資訊可以在以下位置找到：
    - 「一個好的來源是 Wired Online Clipper Archive。發送電子郵件至 info-rama@wired.com，不帶主題，在訊息正文中包含 'get help' 和 'get clipper/index' 字樣。」[students@unsw.EDU.AU, alt.privacy.clipper, 1994-09-01]
### 9.2.4. 雜項評論
  - 與其他幾個章節一樣，我不會試圖像某些人希望的那樣完整。只是有成千上萬頁的東西需要考慮。

## 9.3. Introduction
### 9.3.1. 什麼是 Clipper？
  - 政府持有萬能鑰匙
  - 與其他系統的類比
### 9.3.2. 為什麼大多數 Cypherpunks 反對 Clipper？
  - 害怕對加密的限制，破壞這麼多美好的可能性
### 9.3.3. 為什麼 Clipper 值得擁有自己的章節？
  - 1993 年 4 月 16 日宣布的 "Escrowed Encryption Standard" (EES) 對 Cypherpunks 和很大一部分美國人口來說是一個激勵事件。EES 最初被宣布為 "Clipper"，儘管 Clipper 這個名字已被兩個主要產品（Intergraph CPU 和 dBase 軟件工具）使用，政府後來放棄了這個名字。但為時已晚，"Clipper" 這個名字已經與整個提案不可磨滅地聯繫在一起。
### 9.3.4. "阻止 Clipper 是 Cypherpunks 的主要目標嗎？"
  - 有時看起來確實如此，因為自 1993 年 4 月 Clipper 宣布以來，Clipper 一直主導著話題。
  + 它已經變成這樣，在幾個領域進行了破壞活動
    - 反對它的遊說和教育（雖然是非正式的，但這種遊說已經取得了成功……看看紐約時報的文章）
    - "Big Brother Inside" 和 T 恤
    - 技術破壞（Matt Blaze……猶豫是否聲稱任何功勞，但他一直在我們的名單上，參加過會議等）
  - 雖然看起來如此，但 Clipper 只是其中一個方面……步驟……倡議。
  - 開發新的軟件工具、編寫代碼、部署 remailers 和 digital cash 是非常重要的長期項目。
  - Clipper key escrow 提案（4-93）在對 Cypherpunks 來說合適的時間出現，並成為主要焦點。緊急會議、分析等。

## 9.4. Crypto Policy Issues
### 9.4.1. Peter Denning 關於 crypto policy：
  + 由 Pat Farrell 提供，1994-08-20；Denning 的評論是 1992-01-22，在 Computers, Freedom, and Privacy 2 上發表。Peter D. 使用森林中的 "clearing"（空地）作為隱喻，人們在那裡見面交易、互動等。其他人稱之為市場、agoras 或僅僅是 "cyberspace"。
    - 「資訊技術正在產生一個空地，在這個空地中，除了政府之外，個人和公司也是關鍵參與者。政府控制網絡資訊流動的任何企圖都將被忽視或遭到公開敵視。除了直接涉及治理業務的資訊外，政府沒有實際方法可以控制資訊。它不應該嘗試。」[Peter Denning, PUBLIC POLICY FOR THE 21ST CENTURY, DRAFT 1/22/92]
  - 沒有關於這種觀點如何與他妻子的控制狂觀點相一致的消息。
### 9.4.2. 政府和特別是 NSA 是否會試圖獲得對 crypto 公司的某種控制權？
  + 推測，顯然沒有根據，即 RSA Data Security 受到 NSA 意願的影響
    - 選擇的 DES keys 有弱點？
  - 公司可能會受到合同（以及扣留合同）的巨大影響
### 9.4.3. NIST 和 DSS
### 9.4.4. 出口限制，軍需品清單，ITAR
### 9.4.5. 廉價出售給第三世界政府的舊 crypto 機器
  - 也許他們認為他們可以做一些改變並智勝 NSA（NSA 可能已經操縱了它，以便任何改變都是可檢測的並且可以被考慮在內）
  - 僅僅知道機器的類型就是一個巨大的優勢
### 9.4.6. 4/28/97 幾個 P-K 和 RSA 專利中的第一個到期
  + 美國專利號：4200770
    - 標題：Cryptographic Apparatus and Method
    - 發明者：Hellman, Diffie, Merkle
    - 受讓人：Stanford University
    - 申請日：1977 年 9 月 6 日
    - 授權日：1980 年 4 月 29 日
    - [到期日：1997 年 4 月 28 日]
  + 請記住，Public Key Partners（Stanford 和 M.I.T.，RSA Data Security 是許可證的主要分發者）持有的這幾項專利中的任何一項都可以阻止繞過其他專利的努力
    - 儘管這可能會在法庭上解決
### 9.4.7. 計算機系統內部將需要加密
  - 用於操作系統保護
  - 用於自主 agents（主動 agents）
  - 用於電子貨幣

## 9.5. Motivations for Crypto Laws
### 9.5.1. "執法部門和 FBI 擔心什麼？"
  - 「FBI 局長 Louis Freeh 很擔心。壞人開始看到光明，而且是數字化的。……Freeh 擔心一些非常討厭的人已經發現他們甚至不用離開家就可以進行攔路搶劫等等。更糟糕的是，對於 Freeh 和其他高級警察來說，通過使用一些非常基本的技術，精明的罪犯可以犯罪而不用擔心坐牢。
     
     「一些騙子、間諜、毒販、恐怖分子和欺詐者已經使用資訊時代的工具來智勝執法人員。黑客使用 PBX 來隱藏他們的蹤跡，因為他們敲詐電話公司並窺探其他人的檔案。重新編程的移動電話讓警察發瘋。」[LAN Magazine,"Is it 1984?," by Ted Bunker, August 1994]
  - 他們的恐懼有一定的道理……就像古騰堡時代的統治者可能對書籍的影響（行會的破裂、國家機密的傳播、色情、無神論等）有一些擔憂一樣。
### 9.5.2. "什麼激發了 Clipper？聯邦調查局希望獲得什麼？"
  - 表面上是為了阻止恐怖分子（如果允許替代方案，只有不成熟的恐怖分子才會被阻止）
  - 強制普通美國人接受標準
  - 可能限制 crypto 發展
  + Phil Karn 為 Clipper 提供了一個有趣的動機：
     「Key escrow 的存在只是因為 NSA 不想冒險受到指責，如果某個恐怖分子或毒販使用未託管的 NSA 生產的……恐怖分子或毒販可以輕易地去別處獲得其他強大的或更強大的算法而無需 key escrow，這一事實是無關緊要的。NSA 根本不在乎，只要*他們*不會為發生的任何事情受到指責。典型的 CYA（掩蓋屁股），僅此而已……類似的分析適用於關於密碼學的出口管制法規。」[Phil Karn, 1994-08-31]
    - Bill Sommerfeld 指出：「如果確實如此，Matt Blaze 的結果對他們來說應該是特別毀滅性的。」[B.S., 1994-09-01]
### 9.5.3. Steve Witham 對於為什麼像 Dorothy Denning 和 Donn Parker 這樣的人如此熱烈地支持 key escrow 有一個有趣的看法：
  - 「也許像 Dot 和 Don 這樣的人認為政府是一種類似系統管理員的工作。所以他們在這裡，安全專家就以下事情向系統管理員提供建議……
     
     設置權限
     分配配額
     註冊使用者並給他們密碼……
     決定哪些實用程序可用，哪些不可用
     決定使用者需要什麼軟件，並安裝它
              （勉強地，基於誰叫得最大聲）
     設置與其他機器的連接
     決定誰被允許從 "foreign hosts" 登錄
     設置郵件並運行
     從供應商處購買新硬件
     向供應商指定硬件
     ...
     
     「這些是計算機安全專家建議的事情。也許錘子專家把事情看作釘子。
     
     「只有一個國家不是政府擁有和管理的主機系統，公民不是客人或使用者。」
     [Steve Witham, Government by Sysadmin, 1994-03-23]
     
### 9.5.4. 誰會想使用 key escrow？
### 9.5.5. "強加密真的會阻礙政府計劃嗎？"
  - 是的，它將賦予公民外國政府多年來擁有的基本能力
  + 儘管有關於破譯者和 NSA 專業知識的討論，但簡單的事實是，多年來沒有主要的蘇聯密碼被破解
    + 回想一下評論，即 NSA 多年來沒有真正破解任何蘇聯系統
      - 除了像 Walker 案那樣獲得明文版本的情況，即發生人為錯誤的地方
  - 許多小說中關於大型計算機破解密碼的形象是荒謬的：現代密碼不會被破解（但許多第三世界國家及其大使館使用的原始密碼將繼續是兒戲，即使對於高中科學展覽項目來說……對於一個項目被撤下的 BCC 學生來說，這可能是一個小場景的好主意）
### 9.5.6. "為什麼政府想要短密鑰？"
  - 商業產品經常被黑客破解。NSA 實際上擁有幫助企業保護其秘密的章程；只是不能強大到讓他們無法破解。（當然，這一直是過去幾十年 NSA 兩方之間緊張關係的一部分。）
  + 那麼為什麼政府想要殘缺的密鑰長度？
    - 「問題是：如何在允許 NSA 存取的同時阻止黑客？明顯的答案是強算法和相對截斷的密鑰。」[Grady Ward, sci.crypt, 1994-08-15]

## 9.6. Current Crypto Laws
### 9.6.1. "Crypto 在美國以外的國家受到限制嗎？"
  - 許多國家對 crypto 的平民/私人使用有限制。有些甚至堅持公司要麼以明文發送所有傳輸，要麼向政府提供密鑰。例如菲律賓。當然，共產主義集團的政權，或者剩下的政權，可能會有各種限制 crypto 的法律。可能是嚴厲的法律……在許多文化中，使用 crypto 等同於間諜活動。

## 9.7. Crypto Laws Outside the U.S.
### 9.7.1. "國際託管和其他國家的 Crypto 政策？"
  - 本文件始終關注美國政策，不應讓非美國人感到自滿。許多國家已經對加密的私人使用制定了比美國甚至正在考慮（公開）的更嚴厲的政策。法國禁止私人 crypto，儘管據說執法有問題（但我肯定不想讓 DGSE 盯上我）。第三世界國家經常禁止 crypto，僅僅擁有看起來隨機的位可能意味著間諜罪定罪和上絞刑架。
  + 還有幾份報告稱，歐洲國家正準備在 key escrow 問題上跟隨美國
    - 挪威
    - 荷蘭
    - 英國
  + 6/94 在華盛頓特區舉行的一次會議，Whit Diffie 出席（並在 6/94 CP 會議上向我們報告），將國際託管安排作為主題，NIST 和 NSA 的 crypto 決策者描述了各種選擇
    - 壞消息，因為它可能允許雙邊條約取代基本權利
    - 可能是使 key escrow 成為強制性的計劃
    + 還有實際問題
      + 誰可以解碼國際通信？
        - 我們真的想讓法國人閱讀 Intel 的通信嗎？（回想 Matra-Harris）
      - 衛星？（像 Iridium）
      - 多國訊息呢，例如發布到 Internet 上訊息池的加密訊息……是否要與 100 個國家中的每一個進行託管？
### 9.7.2. "外國會使用基於美國的 key escrow 系統嗎？"
  - 壓力很大。大量合規證據。
### 9.7.3. "歐洲正在考慮 Key Escrow 嗎？"
  - 是的，非常肯定。有很多跡象表明這一點，來自歐洲和其他地方的居民的報告不斷傳來。歐洲人在公共政策問題上往往比較安靜（至少在某些領域）。
  - 「最新一期的 `Communications Week International' 告訴我們，歐盟資訊系統安全高級官員小組一直在考慮在歐洲標準化 key escrow 的計劃。
     
     「協議因關於誰應該持有密鑰的爭論而被擱置。法國和荷蘭希望跟隨 NSA 的領導，讓各國政府承擔這一角色；其他參與者希望使用者組織來做這件事。」[rja14@cl.cam.ac.uk (Ross Anderson), sci.crypt, Key Escrow in Europe too, 1994-06-29]
### 9.7.4. "各國關於加密和國際流量加密使用的法律是什麼？"
  + "法國真的禁止加密了嗎？"
    - 有反覆出現的報告稱法國不允許不受限制地使用加密。
    - 很難說。法律在書面上。但沒有跡象表明 PGP 的許多法國使用者正在被起訴。
    - 一個其領導人 Francois Mitterand 是納粹合作者，與 Petain 和 Vichy 政府合作（涉及 Klaus Barbie）的國家
  + 一些具體國家
    - （這裡需要更多資訊）
    + 德國
      - BND 與美國合作
    - 荷蘭
    - 俄羅斯
  + 資訊
    - 「查看 csrc.ncsl.nist.gov 的 ftp 站點，查找名為 "laws.wp" 之類的文件（有幾個這樣的，格式各異）。這包含 Georgetown 或 George Washington 或類似大學的幾個人為 NIST 所做的各國立場調查。」[Philip Fites, alt.security.pgp, 1994-07-03]
### 9.7.5. 法國計劃老大哥智能卡？
  - 「法國巴黎，1994 年 3 月 4 日 (NB) -- 法國政府已確認計劃用信用卡大小的 "smart card" 身份證取代公民的紙質身份證。
     .....
     「這些卡包含最近交易的詳細資訊，並充當小額交易的 "電子錢包"，使用個人識別碼 (PIN) 作為授權。"錢包交易" 通常與卡信用/借記系統分開，當錢包空了時，可以在合適的 ATM 或零售商終端從卡重新加載。」(Steve Gold/19940304)" [這是轉發給我發布的]
### 9.7.6. PTTs，關於 modem 使用的當地規則
### 9.7.7. "歐洲關於 "Data Privacy" 的法律是什麼，為什麼它們是一個如此糟糕的主意？"
  - 各個歐洲國家已經通過了關於在未經明確許可的情況下編制個人計算機記錄的法律。這適用於幾乎所有計算機化記錄——郵件列表、檔案、信用記錄、員工檔案等——儘管存在一些例外，而且一般來說，公司可以找到編制記錄並保持合法的方法。
  - 規則是可以辯論的，負擔不起律師和顧問費用的普通個人很可能會反覆違反法律。例如，將 Cypherpunks 列表上的人員帖子存儲在任何可按名稱檢索的系統中都將違反英國的 Data Privacy 法律。幾乎沒有這樣的案件會導致起訴（出於實際原因），並不意味著法律是可以接受的。
  - 對許多人來說，這些法律是一個「好主意」。但法律忽略了主要觀點，給人一種虛假的安全感（因為真正的檔案編制者很容易獲得豁免，或者是政府機構本身），並干涉人們對合法獲得的資訊的處理。（警惕像 ACLU 和 EFF 這樣的「民權」團體推動此類數據隱私法。Kapor 與 Lotus 和失敗的 "Marketplace" CD-ROM 產品的聯繫具有諷刺意味，不容忽視。）
  - 制定禁止保存某些類型記錄的法律是邀請 "data inspectors" 翻閱某人的檔案。或者某種抽查，甚至軟件 key escrow。
  - （強加密使這些法律難以執行。要麼法律消失，要麼擁有此類法律的國家將不得不限制強加密……這從長遠來看並沒有幫助。）
  - 同樣的觀點適用於善意的提議，即將雇主監控員工定為非法。這聽起來像是一個增強隱私的主意，但它踐踏了雇主確保工作完成、基本上按照他認為合適的方式經營業務等的權利。如果我僱用了一名程序員，他使用我的資源、我的網絡連接來進行非法操作，他會使我的公司面臨損害賠償，當然他也沒有做我付錢讓他做的工作。如果法律禁止我監控這種情況，或者至少隨機檢查，那麼他可以利用這條法律為自己謀利並損害我的利益。（再次強調僵化法律、非市場解決方案、博弈論的危險。）
### 9.7.8. 關於澳大利亞的情況
  + Matthew Gream [M.Gream@uts.edu.au] 通知我們，Oz 的出口情況與美國一樣好 [1994-09-06]（好像我們不知道……儘管我們都喜歡抨擊美國的法西斯法律，但很明顯，幾乎所有國家都在接受美國的新世界秩序行軍命令，而且其中許多國家已經制定了更具壓制性的 crypto 法律……出於顯而易見的原因，它們只是沒有得到美國那樣的討論）
    - 「好吧，去他的，我還以為我生活在一個限制較少的政權下——我可以告別我的軟件的國際市場了。]
    - （我保留了他直率的語言，以產生影響。）
### 9.7.9. "對於感興趣的人，NIST 有一份簡短的 FTP 文件，'Identification & Analysis of Foreign Laws & Regulations Pertaining to the Use of Commercial Encryption Products for Voice & Data Communications'。日期為 1994 年 1 月。" [Owen Lewis, Re: France Bans Encryption, alt.security.pgp, 1994-07-07]

## 9.8. Digital Telephony
### 9.8.1. "什麼是 Digital Telephony？"
  - Digital Telephony 法案，最初由布什提出，克林頓再次提出，在許多方面比 Clipper 糟糕得多。由於各種原因，它受到的關注較少。
  - 首先，有些人將其視為現有竊聽能力的擴展。而且，它是相當抽象的，發生在電話公司交換機的門後。
  - 影響是嚴重的：強制性竊聽和筆式記錄器（誰在給誰打電話）能力，對合規不足處以每天高達 10,000 美元的民事處罰，必須提供強制性協助等。
  - 如果通過，它可能會決定未來的技術。安裝它的電信公司將確保新興技術（例如，找到通過計算機線路傳輸語音的方法的 Cypherpunks）也被迫「遵守相同的規則」。被要求即使在小型系統中也安裝政府可訪問的竊聽點當然會有效地摧毀它們。
  - 另一方面，即使通過強制手段，使 Digital Telephony 可行也變得越來越困難。正如 FBI 的 Jim Kallstrom 所說：「今天將是國會解決這件事的最便宜的一天，」Kallstrom 說。「兩年後，它將成幾何級數地昂貴。」[LAN Magazine,"Is it 1984?," by Ted Bunker, August 1994]
  - 這給了我們一個目標：破壞讓 Digital Telephony 通過成為法律的最新嘗試，它可能會使其變得太棘手而*永遠*無法通過。
  + "今天將是最便宜的一天
    - 國會可以解決這件事，" Kallstrom 說。"兩年後，
    - 它將成幾何級數地昂貴。"
  - 訊息很明確：推遲 Digital Telephony。在輿論法庭上破壞它，傳播消息，讓它失敗。（重讀你的《孫子兵法》以獲取孫子關於與敵人戰鬥的提示。）
  -
### 9.8.2. "Digital Telephony 法案的危險是什麼？"
  - 它使竊聽對被竊聽者不可見。
  + 如果通過成為法律，它使中心局竊聽變得微不足道、自動化。
    - 「人們應該擔心的是新聞中沒有的內容（可能永遠不會有，直到它已經嵌入通信系統）。真正的 'Clipper' 將允許按需遠程竊聽。這對於全數字通信系統來說非常容易做到。如果你了解網絡路由器和協議，很容易想像將目標通信的副本 '重新路由' 到你想要的任何地方是多麼簡單……」[domonkos@access.digex.net (andy domonkos), comp.org.eff.talk, 1994-06-29]
### 9.8.3. "什麼是 Digital Telephony 提案/法案？
  - 幾年前提出……據說是 PGP 的靈感來源
  - 1994 年 2 月 4 日重新引入
  - 早期版本：
  + "1)  DIGITAL TELEPHONY PROPOSAL
    - 「為了確保執法部門繼續有能力進行法院
    - 授權的竊聽，政府應
    - 司法部和 FBI 的要求，提出了數字電話
    - 立法。1992 年 9 月提交給國會的版本
    - 將要求電子通信服務提供商
    - 和專用交換機 (PBX) 運營商確保
    - 政府合法攔截通信的能力不會
    - 因引入先進技術而被削減或完全阻止。」

## 9.9. Clipper, Escrowed Encyption Standard
### 9.9.1. Clipper 提案
  - 1993 年 4 月 16 日投下了一枚重磅炸彈。我們中的一些人看到了它的到來，因為我們一直在辯論……
### 9.9.2. "政府計劃 key escrow 多久了？"
  - 自 1989 年左右
  - 諷刺的是，我們大約提前六個月得到了警告
  - 我自己的 "A Trial Balloon to Ban Encryption" 提醒世界注意 D. Denning 的想法……她否認在宣布前一天知道 key escrow，我覺得這難以置信（不是說她是騙子，但是……）
  + Phil Karn 在 Clipper 宣布前幾週對 Dorothy Denning 教授說了這番話：
    - 「私人使用強密碼學首次提供了針對這種政府濫用的真正有效保障。這就是為什麼它必須繼續自由和不受管制。
    - 「我應該讚揚你為我們大家做了一項非常重要的服務，提出了這個問題。沒有什麼比你禁止或管制它的提議更能激起我們這些堅信公民有權使用密碼學的人的怒火了。我們這裡有許多人分享這種信念*並*擁有將其付諸實踐的技術技能。我向你保證，如果有必要，我們將為這一信念戰鬥到底。」[Phil Karn, 1993-03-23]
    -
    -
### 9.9.3. 技術上是 "Escrowed Encryption Standard" 或 EES。但幾乎每個人仍然稱之為 "Clipper"，即使 NSA 遲遲意識到 Intergraph 的產品多年來一直被稱為這個名字，就像同名的 Fairchild 處理器芯片一樣。以及同名的數據庫產品。我在 1993 年 4 月 16 日聽說這件事幾分鐘後就指出了這一點，並在 sci.crypt 上發表了評論。他們怎麼會如此無知，以至於在幾個月的工作中沒有看到我們許多人在幾秒鐘內看到的東西？
### 9.9.4. 對 Clipper 的需求
### 9.9.5. Key escrow 的進一步「理由」
  + 需要透露身份的 anonymous 諮詢
    - 自殺危機干預
    - 承認虐待、犯罪等（Tarasoff 法）
  - 聯邦調查局想要查看的公司記錄
  + 託管加密的一些合法需求
    - 對於公司，繞過離職、被解僱、已故員工的密碼，
### 9.9.6. 政府為什麼開發 Clipper？
### 9.9.7. "誰是指定的託管代理？"
  - 商務部 (NIST) 和財政部 (Secret Service)。
### 9.9.8. Whit Diffie
  - Miles Schmid 是架構師
  + 國際 key escrow
    - Denning 試圖為其辯護……
### 9.9.9. 相關計劃有哪些？
### 9.9.10. "Clipper" 和 "Skipjack" 這些名字從何而來？
  - 首先，NSA 和 NIST 選擇 "Clipper" 這個名字犯了大錯，這長期以來一直是 Fairchild 的 32 位 RISC 處理器（最早的之一）的名字，後來賣給了 Intergraph。它也是數據庫編譯器的名字。我們大多數人立即看到了這一點。
  -
  + Clippers 是船，skipjacks 也是（「一種小型帆船，具有
    - 像扁平 V 形的底部和垂直側面」Am Heritage. 3rd）。
    - 暗示航海主題，這符合
    - 該機構的切薩皮克環境（小船傳統上是
    + 機構處置可疑叛徒和間諜的方式）。
      -
    - 然而，Capstone 不是船，Tessera 也不是，所以趨勢失敗了。

## 9.10. Technical Details of Clipper, Skipjack, Tessera, and EES
### 9.10.1. Clipper 芯片製造細節
  + 正在使用 ARM6 核心
    - 但也有傳言稱 Tessera 中有 MIPS 核心
  - 據報導 MIPS 核心正在設計到未來版本中
  - National 也為 NSA 建造（並可能運營）了一條安全的晶圓製造線，據報導位於 Ft. Meade 的場地上——儘管我無法確認位置或 National 目前的參與程度。可能僅用於中等密度芯片，如密鑰材料（在安全條件下構建）。
### 9.10.2. "為什麼 Clipper 算法是機密的？"
  - 為了防止非託管版本，這些版本仍然可以使用（據推測是強大的）算法和硬件，但不被託管
  - 如果算法已知，cryptanalysis 總是更容易 :-}
  - 一般政府保密
  - 後門？
### 9.10.3. 如果 Clipper 有缺陷（Blaze LEAF Blower），它如何仍然對 NSA 有用？
  - 通過補貼成本破壞商業替代品（鑑於 Clipper 獲得的可怕公關，我認為這不會發生）
  - 法律或出口規則強制執行
  - Blaze 攻擊——目前——不容易使用（任何能夠使用它的人可能足夠複雜，無論如何都會使用預加密）
### 9.10.4. Clipper 的弱點呢？
  - 在許多人看來，這是一個有缺陷的方法。也就是說，爭論細節正中聯邦調查局下懷。
### 9.10.5. "Clipper 有哪些弱點？"
  - key escrow 的基本理念是對自由的侵犯
  + 存取密鑰
    - "
    + 「側面有一扇大門，上面有
      - 一個大霓虹燈標誌，寫著 "Cops and other Authorized People Only"（僅限警察和其他授權人員）；
      - 陷門是任何擁有傳真機的人都可以製作
      - 他們自己和 "Authorized Person" 徽章並走進去。
         <Bill Stewart, bill.stewart@pleasantonca.ncr.com, 4-15-94, sci.crypt>
  - Skipjack 算法中可能的後門
  + 託管密鑰的生成
    -
    + 「還有另一個陷門，那就是如果你能預測託管
      - 密鑰，通過竊取 Key Generation Bureau 用來
      - 設置它們的參數，你不需要從密鑰管理員那裡獲得託管密鑰，
      - 你可以自己生成它們。」<Bill Stewart, bill.stewart@pleasantonca.ncr.com, 4-15-94, sci.crypt>
### 9.10.6. Mykotronx
  - MYK-78e 芯片，延遲，VTI，保險絲
  - National Semiconductor 正在與 Mykotronx 合作，以更快地實現
     Clipper/Capstone/Skipjack/whatever 系統。（可能與 iPower 產品線直接相關，也可能不相關。此外，可能會使用 MIPS 處理器核心，而不是據說太慢的 ARM 核心。）
### 9.10.7. 對 EES 的攻擊
  - 破壞託管數據庫
  + 竊取它，從而導致信心崩潰
    - Perry Metzger 的提議
  - FUD
### 9.10.8. 為什麼算法是秘密的？
### 9.10.9. Skipjack 是 80 位，比 DES 的 56 位長 24 位。所以
### 9.10.10. "Matt Blaze 發現的 Tessera 錯誤有什麼影響？"
  - 技術上，Blaze 的工作是在 Tessera 卡上完成的，該卡實現了 Skipjack 算法。Clipper 電話系統可能略有不同，細節可能有所不同；Blaze 攻擊甚至可能不起作用，至少在實踐中不起作用。
  - 「上個月的公告是關於一個發現，即在普通 PC 上花費半小時左右的時間，使用者可以偽造一個虛假的 LEAF（政府用來訪問 Clipper 加密後門的數據）。有了這樣一個虛假的 LEAF，另一端的 Clipper 芯片將接受並解密通信，但後門對政府不起作用。」[ Steve Brinich, alt.privacy.clipper, 1994-07-04]
  - 「我的論文 "Protocol Failure in the Escrowed Encryption Standard" 的 "最終" 預印本（日期為 1994 年 8 月 20 日）現已可用。你可以通過匿名 ftp 從 research.att.com 的文件 /dist/mab/eesproto.ps 獲取 PostScript 形式。此版本取代了以前佔據同一文件的初步草案（6 月 3 日）版本。大部分內容是相同的，儘管少數章節有所擴展，並且現在糾正了一些小錯誤。」[Matt Blaze, 1994-09-04]

## 9.11. Products, Versions -- Tessera, Skipjack, etc.
### 9.11.1. "與 EES 相關的各種版本和產品有哪些？"
  - Clipper，MYK-78 芯片。
  - Skipjack。
  + Tessera。Escrowed Encryption Standard 的 PCMCIA 卡版本。
    - Matt Blaze 發現炸毀 LEAF 的方法的版本
    - National Semiconductor "iPower" 卡可能支持也可能不支持 Tessera（報告相互矛盾）。
### 9.11.2. AT&T Surety Communications
  - NSA 可能向他們施壓，要求他們不要發布基於 DES 的產品
### 9.11.3. Tessera 卡
  - iPower
  - Tessera 卡接口的規範可以在幾個地方找到，包括 "csrc.ncsl.nist.gov"--參見文件 cryptcal.txt [David Koontz, 1994-08-08]。

## 9.12. Current Status of EES, Clipper, etc.
### 9.12.1. "政府真的在 Clipper 上退縮了嗎？我聽說 Al Gore 給 Cantwell 眾議員寫了一封信，退縮了。"
  - 沒有，儘管 Clipper 已經失去了動力（公司對購買 Clipper 電話不感興趣，AT&T 在推出 "Surety" 電話方面非常遲緩）。
  - Gore 的公告實際上可能表明重點轉移到 "software key escrow"（我最好的猜測）。
  - 我們自己的 Michael Froomkin，一位律師，寫道：「這封信是無效的。它幾乎引用了 NIST 一年前向國會提供的證詞。從 eff www 服務器獲取 Leahy 參議員的反應副本。他看穿了它的空洞……除了 Cantwell 放棄了她的法案之外，什麼都沒有改變。」[A.Michael Froomkin, alt.privacy.clipper, 1994-09-05]

## 9.13. National Information Infrastructure, Digital Superhighway
### 9.13.1. 資訊高速公路上的炒作
  - 談論資訊高速公路而不使用至少一個過度使用的隱喻是違法的：路殺、收費站、超車道、路肩、入口匝道、出口匝道、超速、I-way、Infobahn 等。
  - 現在圍繞著突然流行的 Digital Superduperway 想法的大部分內容只不過是炒作。和瘋狂的隱喻。錯位的熱情，將切線發展與真正的進步混淆。就像自由意志主義者假設太空計劃是他們應該以某種方式致力於的事情一樣。
  - 例如，被大肆宣傳的 Net 上的 "Pizza Hut"（我想是家庭披薩頁面）。它已經被稱為「真正的 Internet 商業的第一個案例」。是的，就像多年前 Net 上的可樂機是 Internet 商業的例子一樣。純粹的炒作。麥迪遜大道的廢話。對我們的小報一代有好處。
### 9.13.2. "為什麼 National Information Infrastructure 是一個壞主意？"
  - NII = Information Superhighway = Infobahn = Iway = 十幾個其他據稱聰明和雙關的名字
  + Al Gore 的提議：
    - 連接醫院、學校、政府
    + 很難想像 Internet 的自由無政府狀態會持續下去……更有可能的影響：
      - "is-a-person" 憑證，即身份證明，因此跟蹤所有互動
      - 醫療和精神病記錄將成為其中的一部分（精神科醫生對此持懷疑態度，但在正在辯論的國家醫療保健計劃下，他們可能別無選擇，只能遵守）
  + 還有其他壞方面：
    - 政府控制、政府效率低下、政府窺探
    - 市場扭曲（「普遍接入」）
    - 限制創新
    - 不需要……其他網絡做得很好，並將被放置在需要的地方並由當地支付
### 9.13.3. NII, Video Dialtone
  + "Dialtone"
    - 電話公司提供輸入輸出連接，並對連接收費，不對內容做出裁決（與 "Common Carrier" 地位有關）
    + 對於視頻電纜，我不相信正在考慮類似的設置
      + 有線電視
        - Carl Kadie 對 Sternlight 的評論
### 9.13.4. Net 補貼的前景和危險
  - 「普遍接入」，特別是如果在醫療保健領域發生同樣的情況
  - 付費者制定規則
  + 但這種接入將附帶條件
    - 對 crypto 的限制
    -
  - 普遍接入也邀請更多的 spamming，類似 "Freenet" spams，其中人們不斷被驗證為新使用者：任何非付費的普遍接入系統都將對此敏感*或*將導致呼籲普遍 ID 系統（is-a-person credentialling）
### 9.13.5. NII, Superhighway, I-way
  - crypto 政策
  - 監管，許可

## 9.14. Government Interest in Gaining Control of Cyberspace
### 9.14.1. 除了 Clipper, Digital Telephony, 和 National Information Infrastructure，政府還對其他領域感興趣，例如電子郵件遞送（美國郵政服務提議）和一般網絡系統的維護。
### 9.14.2. Digital Telephony, ATM 網絡，和正在達成的交易
  - 正在達成交易的傳言
  - 新草案已出 [John Gilmore, 1994-08-03]
  - 全 ATM 速度的硬件加密
  - 和 SONET 網絡（實驗性，灣區？）
### 9.14.3. USPS 關於郵件、認證、對競爭影響等的計劃
  + 這可能對電子郵件和整個 cyberspace 產生毀滅性影響，特別是如果它與其他政府提議聯繫在一起，試圖獲得對 cyberspace 的控制。
    - Digital Telelphony, Clipper, 色情法律和年齡執行（Amateur Action 案）等。
  + "USPS 真的擁有第一類郵件的壟斷權嗎？"
    - 和 "路線"？
    - 「友好的郵局最近一直在訪問 2) 友好的郵局最近一直在訪問灣區公司的收發室，打開 FedX 等包裹（不受郵局第一類郵件隱私法的保護），並對通過 FedX 發送非時間敏感文件而本可以通過第一類郵件發送的公司處以罰款（我記得每次違規 10,000 美元）。」[Lew Glendenning, USPS digital signature annoucement, sci.crypt, 1994-08-23]（引用或新聞報導會使這更可信，但我聽說過類似的抽查。）
  - 政府機構競爭的問題眾所周知。首先，他們通常服務低劣……公務員工作，不可解僱的工人等。其次，他們通常不能因不履行職責而被起訴。第三，他們通常擁有政府授予的壟斷權。
  + USPS 的提議可能是試圖獲得對電子郵件業務控制權的第一槍……它從未控制過電子郵件，但它對第一類郵件的壟斷可能會被他們認為延伸到 cyberspace。
    - 注意：FedEx 和其他包裹和隔夜信件承運人面臨各種服務限制；例如，他們不能提供 "路線" 和由此產生的經濟效益。
    - USPS 接管電子郵件業務將意味著許多 Cypherpunks 目標的終結，包括 remailers, digital postage 等。
    - 挑戰將是盡快部署這些系統，使 USPS 的任何接管變得更加困難。

## 9.15. Software Key Escrow
### 9.15.1. （本節需要更多內容）
### 9.15.2. 事情發生得很快……
### 9.15.3. TIS, Carl Ellison, Karlsruhe
### 9.15.4. 對 key escrow 的反對意見
  - 「在房地產交易中持有存款是一個典型的例子。內置竊聽*不是*託管，除非政府是你合同的一方。正如名單上的某個人曾經說過的那樣，僅僅因為黑手黨稱自己為 "商人" 並不意味著他們是合法的；稱勒索竊聽為 "託管" 並不意味著它們是一種服務。
     
     「政府無權讓我獲得他們的許可才能用我選擇的任何語言與任何人談論任何事情，他們也無權堅持我從他們的朋友那裡購買 "通信保護服務" 來做到這一點，就像上述 "商人" 無權堅持我從*他們*那裡購買 "火災保險" 一樣。」[Bill Stewart, 1994-07-24]
### 9.15.5. Micali 的 "Fair Escrow"
  - 各種努力正在進行中
  - 這裡需要章節
  - 注意：Karlsruhe 會議的參與者報告說，一個德國小組可能在 Micali 申請專利前幾年就發布了關於軟件 key escrow 的內容（報告稱 NSA 官員 "很高興"）

## 9.16. Politics, Opposition
### 9.16.1. "Cypherpunks 應該對 Clipper 說什麼？"
  - 在這個列表和其他幾十個論壇上已經寫了大量的文章。
  - Eric Hughes 不久前說得很好：
  - 「相比之下，clipper 中假設的後門是一個江湖騙子的問題，關於如何使 key escrow 系統 '工作' 的討論也是如此。不要被騙去談論一個不重要的問題。如果有人想談論潛在的後門，拒絕推測。前門（key escrow）的存在使後門問題相形見絀。
     
     「如果有人想談論 key escrow 如何工作，拒絕詳細說明。說這個特定的 key escrow 系統不好，在很大程度上是在同謀說一般的 escrow 系統是可以的。始終爭辯說這個特定的 key escrow 系統不好，因為它是一個 key escrow 系統，而不是因為它有程序缺陷。
     
     「正確的問題是政府無權獲得我的私人通信。其他所有問題都是錯誤的問題，並分散了對這一核心問題的注意力。如果我們擊敗了一個特定的系統而沒有同時擊敗所有其他可能的此類系統，我們根本就沒有贏；我們只是推遲了清算的時間。」[ Eric Hughes, Work the work!, 1993-06-01]
### 9.16.2. 大多數美國人對 Clipper 和隱私有什麼看法？"
  - 對我們面臨的情況的見解
  + 「在上週 Yankelovich 為 Time/CNN 進行的一項針對 1,000 名美國人的民意調查中
    - Partners，三分之二的人說保護電話隱私更重要
    - 通話比保留警察進行竊聽的能力更重要。
    - 當被告知 Clipper Chip 時，80% 的人表示反對。」
    - Philip Elmer-Dewitt, "Who Should Keep the Keys", Time, Mar. 4, 1994
### 9.16.3. 有人真的支持 Clipper 嗎？
  + 實際上，託管形式有一些合法的用途：
    - 公司
    - 其他合夥企業
### 9.16.4. "誰反對 Clipper？"
  - 計算機協會 (ACM)。「USACM 敦促政府此時撤回 Clipper Chip 提案，並開始對加密政策進行公開審查。託管加密倡議引發了隱私、執法、競爭力和科學創新等必須公開討論的重要問題。」[US ACM, DC Office" <usacm_dc@acm.org>, USACM Calls for Clipper Withdrawal, press release, 1994-06-30]
### 9.16.5. "Key escrow 有什麼不好？"
  + 如果它是真正自願的，這可能有有效的用途。
    + 陷門在某些情況下是合理的嗎？
      + 希望恢復加密數據的公司
        + 幾種情況
          - 員工加密重要文件，然後死亡或以其他方式不可用
          + 員工在解密所有文件之前離開公司
            - 有些可能已歸檔，多年不需要打開
          - 員工可能要求 "贖金"（與病毒勒索案件密切相關）
          - 找到文件但原始加密者未知
      + 可能的情況是公司將強制執行加密算法，並保留 "主密鑰"
        - 就像陷門
        - 主密鑰的存在甚至可能不會在公司內部公開（以避免對安全、濫用等的擔憂）
      + 政府正試圖安裝陷門
        - S.266，最終失敗了（但在引起騷動之前）
  + 如果政府要求它……
    - Key escrow 意味著政府可以在你不知情的情況下進入你的家
  - key escrow 不是真正的託管……人們從 "託管" 服務中得到什麼回報？
### 9.16.6. 為什麼政府不應該擁有密鑰
  - 然後可以通過偽造訊息、栽贓證據來陷害人們
  - 可以為了自己的目的監視目標（歷史告訴我們，這可能包括賄賂、企業間諜活動、毒品走私、暗殺和各種非法和卑鄙的活動）
  - 可以破壞合同、交易等
  - 將使他們能夠訪問內部公司通信
  - 破壞此類合同和身份加密標準的整體有效性（動搖信心）
  - 賦予國王或國家冒充他人的權力是一種極大的不公正
  - 想像伊朗政府擁有後門來閱讀其臣民的秘密日記！
  - 第四修正案
  - 律師-委託人特權（有了陷門，無法知道政府沒有破壞保密性）
### 9.16.7. "Clipper 芯片如何被挫敗或擊敗？"
  - 政治上、市場上和技術上
  - 如果部署了，也就是說
  + 擊敗 Clipper 的方法
    - 預加密或超加密
    - LEAF blower
    - 插頭兼容、逆向工程芯片
    - 破壞
    - 破壞信心
    - 孫子
### 9.16.8. Clipper 如何在政治上被擊敗？
### 9.16.9. Clipper 如何在市場上被擊敗？
### 9.16.10. Clipper 如何在技術上被擊敗？
### 9.16.11. 問題
  + Clipper 問題和疑問
    - 大量的問題、評論、挑戰、趣聞、細節、議題
    - 整個新聞組致力於此
  + "什麼罪犯或恐怖分子會聰明到使用加密但愚蠢到使用 Clipper？"
    - 這是未解之謎之一。Clipper 的支持者對此保持沉默。暗示……
  + "為什麼不在使用 Clipper/EES 之前加密數據？"
    - 「為什麼你不能在 clipper 芯片之前加密數據？
       
       兩個答案：
       
       1) 你想與之通信的人將沒有硬件來
       解密你的數據，從統計上講。clipper 的美妙之處
       從 NSA 的角度來看是他們正在利用
       已安裝的電話基礎（他們希望）並使其
       不可能（再次，統計上）讓很大一部分
       流量不可竊聽。
       
       2) 他們不會許可像你這樣的壞人製造像
       你描述的系統那樣的設備。我敢打賭芯片分發將以
       防止大量此類系統
       被構建的方式進行，確保 (1) 仍然正確。」[Tom Knight, sci.crypt, 6-5-93]
       
    -
  + 強制性 key escrow 的含義是什麼？
    + "escrow" 是誤導性的……
      - 術語的錯誤使用
      - 暗示自願和可退還的情況
  + "如果 key escrow 是 "自願的"，有什麼大不了的？"
    - 稅收據說也是 "自願的"。
    - 智者為_可能的_甚至_可能的_事情做準備，而不僅僅是作為公共政策宣布的事情；政策可以而且確實會改變。有大量的先例表明 "自願" 系統被強制執行。
    - Clipper/EES 系統的形式暗示最終的強制地位；這種禁令的形式是可以辯論的。
  + "什麼是 'superencipherment'，它可以用來擊敗 Clipper 嗎？"
    - 預加密
    - 可以被視為非英語語言
    + Clipper 芯片怎麼會知道它（熵測量？）
      - 牽強
    - 不會解決流量分析問題
  - Clipper 和出口法之間有什麼聯繫？
  + "這不是讓 Clipper 數據庫成為成熟的目標嗎？"
    - 用於顛覆、破壞、間諜活動、盜竊
    - 據推測將保留備份，而_這些_也將成為目標
  + "Clipper 僅用於語音加密嗎？"
    - Clipper 是一個數據加密芯片，數字數據由位於芯片外部的 ADC 提供。原則上，它因此可以用於一般的數據加密。
    - 在實踐中，Clipper 這個名字通常與電話使用相關聯，而 "Capstone" 是數據標準（也有一些差異）。"Skipjack" 算法用於其中幾個提議的系統（Tessera 也是）。
### 9.16.12. "為什麼 Clipper 比我們現在擁有的更糟糕？"
  + John Gilmore 在一篇不錯的文章中回答了這個問題。我包括了整件事，包括對移動電話的離題，因為它提供了一些見解——並點名了一些 NSA 說謊者的名字——關於 NSA 和 NIST 如何利用他們的權力來阻礙真正的安全。
    - 「它更糟糕，因為市場一直在朝著提供真正的加密方向發展。
       
       「如果 Clipper 成功，它將通過取代真正的安全加密來實現。如果真正的安全加密進入大眾市場通信產品，Clipper 將失敗。重點不是讓警察使用幾個 Clippers；重點是使其成為全球標準，而不是讓帶有 RSA 和 Diffie-Hellman 的 3-key triple-DES 成為全球標準。
       
       「我們*現在*本可以在數字移動電話中擁有像樣的加密，如果不是因為 NSA 的 Jerry Rainville 的積極干預，他在 Ft. Meade 內部 '主持' 了一次標準委員會會議，關於出口管制向他們撒謊，以將委員會文件限制在一個小組內，並讓來自 Motorola 的一個願意受騙的人 Louis Finkelstein 提出一個孩子都能破解的加密方案。數字蜂窩的 IS-54 標準沒有描述加密方案——它在一個單獨的文件中描述，普通人無法獲得，即使它是官方認可標準的一部分。（猜猜誰認可標準機構——沒錯，曾經純潔的 NIST。）
       
       「它是秘密的原因是因為它明顯很弱。該系統生成一個 160 位的 "key"，然後簡單地將其與每個壓縮語音塊進行 XOR。取任何十個或二十個塊，通過將頻繁的語音模式（如靜音或字母 "A"）與塊的片段進行 XOR 來恢復密鑰，以產生對密鑰的猜測。你在幾個塊上嘗試每個猜測，在所有塊中產生解碼像語音的東西的可能性足夠小，你會知道什麼時候你的猜測是真正的密鑰。
       
       「NSA 今年也繼續在數字蜂窩標準委員會 (TR 45.3) 中胡搞。我鼓勵任何感興趣的人加入委員會，也許作為觀察員。聯繫華盛頓特區的電信工業協會並註冊。像任何標準委員會一樣，它向公眾開放，並在全國各地舉行會議。如果你是外國公民，我會借給你律師，因為委員會可能仍然認為他們必須將外國公民排除在密碼學的公開討論之外。不知何故，crypto 會議對此沒有問題；我認為這叫做第一修正案。NSA 知道這裡的法律——實際上它通過國務院執行它——但對委員會撒了謊。」[John Gilmore, "Why is clipper worse than "no encryption like we have," comp.org.eff.talk, 1994-04-27]
### 9.16.13. 關於信任政府
  - 「故事的寓意是什麼，UNCLE REMUS？……當政府發布任何公告（特別是否認）時，你應該弄清楚政府試圖讓你做什麼——然後做相反的事情。帶著復仇心理的逆向投資。在我提供的所有關於 Cypherpunks Channel 的建議中，這絕對是最確定的。」
     [Sandy Sandfort, 1994-07-17]
  - 如果美國的開國元勳能看到這個國家墮落成的腐敗、社會主義國家，他們會闖入導彈發射井並竊取核武器來對抗中央權力基地。
  + 可以信任政府來運行 key escrow 系統嗎？
    - 「我剛剛在新聞中聽到 1300 名 IRS 員工因未經授權訪問電子提交的所得稅申報表而受到紀律處分。……不過，我相信當 FBI 運行電話系統，郵局控制數字身份，希拉里照顧我們的健康時，他們會做得更好。」[Sandy Sandfort, 1994-07-19]
    - 這只是許多此類例子中的一個：水門事件（「我不是騙子！」）、伊朗門事件、軍火交易、CIA 的可卡因運輸、茶壺山醜聞、貪污、回扣、賄賂、暗殺、揚基-牛仔戰爭、波希米亞格羅夫、Casolaro、更多的殺戮、入侵、戰爭。一個太膽小而不敢承認輸掉戰爭的政府，並顯眼地避免與它未能征服的敵人（越南、朝鮮、古巴等）進行外交接觸，同時迅速成為它征服的國家的乾爹……美國似乎缺乏實用性。（我，我認為任何人告訴我不能與另一個國家的人進行貿易是錯誤的，無論是海地、南非、古巴、韓國，隨便什麼。Crypto anarchy 意味著我們將擁有_一些_繞過這些法律的方法，做出我們自己的道德決定，而不考慮我們目前居住的國家的普遍流行情緒。）

## 9.17. Legal Issues with Escrowed Encryption and Clipper
### 9.17.1. 正如 John Gilmore 在 "San Francisco Examiner" 的客座社論中所說，「……我們希望公眾看到一場嚴肅的辯論，關於為什麼為了拯救國家而應該燒毀憲法。」[J.G., 1994-06-26, quoted by S. Sandfort]
### 9.17.2. "我不明白 Clipper 如何賦予政府任何它尚未擁有的權力或能力。評論？"
### 9.17.3. Clipper 真的是自願的嗎？
### 9.17.4. 如果 Clipper 是自願的，誰會使用它？
### 9.17.5. 對 Crypto 平民使用的限制
### 9.17.6. "Crypto 在美國受到限制了嗎？"
### 9.17.7. "正在採取什麼法律步驟？"
  - Zimmermann
  - ITAR
### 9.17.8. 報告稱司法部在 EES 中具有合規執行角色 [某人從 Dorothy Denning 那裡聽到的，1994-07]，可能涉及檢查執法機構……
### 9.17.9. 狀態
  + "政府機構會使用 Clipper 嗎？"
    - 啊，尷尬的問題。他們聲稱他們會，但也有報告稱敏感機構不會使用它，Clipper 對他們來說太不安全（密鑰長度、託管數據的妥協等）。也可能有不同的程序（所有機構都是平等的，但有些機構比其他機構更平等）。
    - Clipper 被評級為非機密使用，因此這排除了許多機構和許多用途。一個有趣的雙重標準。
  + "政府正在從 Clipper 退縮嗎？"
    + 行業反對讓他們感到驚訝
      - 去年夏天的團體，Citicorp 等
    - 輿論
    - 社論評論
    - 所以他們可能正在準備替代方案
    - 以及 Gilmore 的 FOIA，Blaze 的攻擊，Denning 的非審查，算法的保密性
  + 不會起作用
    - 間諜不會使用它，兒童色情製作者可能不會使用它（如果存在替代方案，這可能是重點）
    - 恐怖分子不會使用它
  - Clipper 有麻煩嗎？
### 9.17.10. "Clipper 會是自願的嗎？"
  - 許多 Clipper 的支持者引用了 Clipper 的自願性質——正如一些政策聲明中所表達的那樣——並以此來反駁批評。
  + 然而，即使真正自願，也有一些問題
    + 政府試圖創建商業標準的不當角色
      - 儘管 NIST 的角色可以用來部分反駁這一點
    - 政府可以而且確實讓競爭對手處境艱難
    - 出口管制（官員對此有聲明）
  + 自願地位的引用：
    - 原始聲明說它將是自願的
    -（需要在這裡獲取一些聲明）
  + 最終強制地位的引用：
    - 「如果沒有這一舉措，政府最終將無力保衛國家。」[Louis Freeh, FBI 局長，各種來源]
    - Trusted Information Systems 的 Steven Walker 是許多認為如此的人之一：「基於他的分析，Walker 補充說，『我確信五年後他們會說 '這不起作用'，所以我們必須改變規則。』然後，他預測，Clipper 將被強制用於所有編碼通信。」[
  + 與其他自願計劃的相似之處
    - 稅收

## 9.18. Concerns
### 9.18.1. 憲法問題
  - 第四修正案
  - 律師-委託人隱私等
  + 聯邦調查局可以在沒有公開聽證會、記錄的情況下獲得訪問權限
    - 秘密情報法庭
    -
    + 「這是無可爭議的（據我所讀），在某些情況下
      - 聯邦情報界將被允許
      - 無需任何公開記錄的法院命令即可獲得 Clipper 密鑰。只有
      - 內部、機密程序將保護我們的
         隱私。」<Steve Waldman, steve@vesheu.sar.usf.edu, sci.crypt, 4-13-94>
### 9.18.2. "如果 Clipper 被廣泛採用，有哪些危險？"
  + 發送者/接收者 ID 無需去 key escrow 即可訪問
    - 這使得流量分析、聯繫人列表易於生成
  + 市場扭曲（「寒蟬效應」）作為政府計劃
    - 使替代方案昂貴，難以出口，成為懷疑的理由
    - 使用 ITAR 阻礙替代方案（如果 Cantwell 放寬密碼學出口管制的法案 (HR 3627) 通過，將有所幫助）
    + VHDL 實現可能
      - Lew Glendenning 推測，sci.crypt, 4-13-94
      - 回想 MIPS 連接（這裡要小心）
### 9.18.3. 市場問題
### 9.18.4. "Clipper 有哪些弱點？"
  + Carl Ellison 這樣分析：
    - 「看到人們忙著辯論 Skipjack 作為算法的質量及其強度審查的質量，這逗樂了我絞刑架幽默的骨頭。
       
       有人提議把你吊在大峽谷上，使用
       
               縫紉線
       綁在
               鋼鏈
       綁在
               毛線
       
       而你正在辯論鋼鏈是否經過了適當的 X 射線檢查，看看金屬是否有缺陷。
       
       「密鑰生成、芯片製造、法院命令、從託管機構獲得密鑰後的分發以及託管機構內密鑰的安全是一些真正的弱點。一旦這些像我使用 1024 位 RSA 和真正的隨機對話密鑰一樣強大，在對話雙方保持密鑰，中間沒有人能得到密鑰，那麼我們就需要看看中間的鋼鏈：Skipjack 本身。」[Carl Ellison, 1993-08-02]
    + Date: Mon, 2 Aug 93 17:29:54 EDT
       From: cme@ellisun.sw.stratus.com (Carl Ellison)
       To: cypherpunks@toad.com
       Subject: cross-post
       Status: OR
       
       Path: transfer.stratus.com!ellisun.sw.stratus.com!cme
       From: cme@ellisun.sw.stratus.com (Carl Ellison)
       Newsgroups: sci.crypt
       Subject: Skipjack review as a side-track
       Date: 2 Aug 1993 21:25:11 GMT
       Organization: Stratus Computer, Marlboro MA
       Lines: 28
       Message-ID: <23k0nn$8gk@transfer.stratus.com>
       NNTP-Posting-Host: ellisun.sw.stratus.com
       
       
       It amuses the gallows-humor bone in me to see people
       busily debating the
       quality of Skipjack as an algorithm and the quality of
       the review of its
       strength.
       
       Someone proposes to dangle you over the Grand Canyon
       using
       
               sewing thread
       tied to
               steel chain
       tied to
               knitting yarn
       
       and you're debating whether the steel chain has been X-
       rayed properly
       to see if there are flaws in the metal.
       
       Key generation, chip fabrication, court orders,
       distribution of keys once
       acquired from escrow agencies and safety of keys within
       escrow agencies are
       some of the real weaknesses.  Once those are as strong as
       my use of
       1024-bit RSA and truly random session keys in keeping
       keys on the two sides
       of a conversation with no one in the middle able to get
       the key, then we
       need to look at the steel chain in the middle: Skipjack
       itself.
       
      - 「密鑰生成、芯片製造、法院命令、從託管機構獲得密鑰後的分發以及託管機構內密鑰的安全是一些真正的弱點。一旦這些像我使用 1024 位 RSA 和真正的隨機對話密鑰一樣強大，在對話雙方保持密鑰，中間沒有人能得到密鑰，那麼我們就需要看看中間的鋼鏈：Skipjack 本身。」
### 9.18.5. 這對未來意味著什麼
### 9.18.6. Skipjack
### 9.18.7. 國家安全例外
  - grep Gilmore 的 FOIA，提到國家安全人員將擁有直接訪問權限，並且這不會向公眾提及
  + Clipper 提案中內置的 "National Security" 例外
    - 在旨在保護使用者隱私的程序鏈中留下了一個極其薄弱的環節。
    - 將可怕的監視權力
    - 技術上置於少數人手中，希望如此薄弱的鏈條
    - 能約束他們，這將是危險的愚蠢行為。這公然違背了
    - 歷史。<Steve Waldman, steve@vesheu.sar.usf.edu, 4-14-94, talk.politics.crypto>
### 9.18.8. 在我看來，任何關注 Clipper 細節而不是 key escrow 整體概念的做法都正中他們下懷。這並不是說 Blaze 和其他人的工作是被誤導的……事實上，這是非常好的工作。但普遍關注 Skipjack 的_細節_並不能減輕我對政府強制 crypto _原則_的擔憂。
   
   如果是 "house key escrow"（房屋鑰匙託管），並且關於鑰匙上允許的齒數細節缺失，如果齒的細節得到澄清，我們會鬆一口氣嗎？當然不會。我，我永遠不會使用 key escrow 系統，即使黑客和 Cypherpunks 的藍絲帶小組研究了設計並宣布它在密碼學上是健全的。
### 9.18.9. 關於 Clipper 的擔憂
  - 允許閱讀過去的通信
  + 當局可以——也許——閱讀很多東西，甚至是非法的，然後將其用於其他調查（舊的「我們有一個匿名提示」策略）
    - 「Clipper 的問題在於它為警察機構提供了顯著增強的目標獲取能力。沒有什麼可以阻止 NSA, ATF, FBI（或司法部的特別項目部門）審查所有互聯網流量，只要他們願意放棄在刑事起訴中使用它。」[dgard@netcom.com, alt.privacy.clipper, 1994-07-05]
### 9.18.10. 一些愛開玩笑的人建議新的託管機構應從像大赦國際和 ACLU 這樣的團體中選擇。我們大多數人反對 key escrow 的「理念」（想想被告知託管家庭照片、日記或房屋鑰匙），因此即使這些類型的懷疑團體作為託管代理也是不可接受的。

## 9.19. Loose Ends
### 9.19.1. "陷門——或某種形式的託管加密——在某些情況下是合理的嗎？"
  + 當然。個人、公司等可能希望使用 crypto 協議，允許他們即使丟失了密鑰也能解密，也許是通過找律師拿他們留給他的密封信封等。
    - 或者使用一種允許他們訪問的 "software key escrow" 形式
  + 希望恢復加密數據的公司
    + 幾種情況
      - 員工加密重要文件，然後死亡或以其他方式不可用
      + 員工在解密所有文件之前離開公司
        - 有些可能已歸檔，多年不需要打開
      - 員工可能要求 "贖金"（與病毒勒索案件密切相關）
      - 找到文件但原始加密者未知
  + 可能的情況是公司將強制執行加密算法，並保留 "主密鑰"
    - 就像陷門
    - 主密鑰的存在甚至可能不會在公司內部公開（以避免對安全、濫用等的擔憂）
  - 強制使用 key escrow，類似強制性 Clipper 系統，或者我們許多人認為正在為 software key escrow 開發的系統（SKE，也稱為 "GAK"，即 "government access to keys"（政府存取密鑰），由 Carl Ellison 提出）是完全不同的，是不可接受的。（Clipper 在這裡的許多地方都有討論。）
### 9.19.2. DSS
  + 關於專利、標準、許可等的持續混亂
    - 「FIPS186 是 DSS。NIST 認為 DSS 不侵犯 PKP 的專利。PKP（或至少 Jim Bidzos）認為它侵犯了。但由於各種原因，PKP 不會起訴政府。但 Bidzos 威脅要起訴侵權的私人當事方。敬請關注……」[Steve Wildstrom, sci.crypt, 1994-08-19]
    - 甚至 Taher ElGamal 也認為這是一個弱標準
  - 潛意識渠道問題
### 9.19.3. 美國在基本權利方面經常是虛偽的
  - 計劃 "解除" 海地人的武裝，就像我們對索馬里人所做的那樣（這使我們解除武裝的人更容易受到當地軍閥的攻擊）
  - 政府官員提議 "壓制" 盧旺達的一個廣播電台，他們認為該電台發出了錯誤的訊息！（在 "McNeil-Lehrer News Hour" 上聽到，1994-07-21]
### 9.19.4. "is-a-person" 和 RSA 風格的憑證
  + 一個危險的想法，即政府將堅持密鑰與人聯繫起來，每人只有一個
    - 這是 AOCE 系統的一個缺陷
    - 許多應用程序需要多次生成新密鑰
