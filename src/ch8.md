# 8. Anonymity, Digital Mixes, and Remailers

## 8.1. copyright
   THE CYPHERNOMICON: Cypherpunks FAQ and More, Version 0.666,
   1994-09-10, Copyright Timothy C. May. All rights reserved.
   請參閱詳細的免責聲明。在「合理使用」條款下可以使用簡短章節，並註明出處，但請勿將我的話冠上你的名字。

## 8.2. SUMMARY: Anonymity, Digital Mixes, and Remailers
### 8.2.1. 主要觀點
  - Remailers 對於 anonymous 和 pseudonymous 系統至關重要，因為它們可以擊敗 traffic analysis
  - Cypherpunks remailers 已經成為主要的成功案例之一，大約在 Kleinpaste/Julf remailer(s) 出現時開始，但現在已擴展到許多站點
  - 要查看站點列表：finger remailer-list@kiwi.cs.berkeley.edu
     ( 或 http://www.cs.berkeley.edu/~raph/remailer-list.html)
  - Anonymity 總體上是一個核心理念
### 8.2.2. 與其他章節的關聯
  - Remailers 使其他技術成為可能
### 8.2.3. 何處尋找更多資訊
  - 關於 remailers 的書面資料（正式的，在書籍和期刊中）很少
  - David Chaum 的論文是一個開始
### 8.2.4. 雜項評論
  - 在我看來，這仍然是最混亂和令人困惑的章節之一。它需要更多的重寫和重組。
  + 部分原因是幾個因素
    - 大量的人致力於 remailers，貢獻想法、問題、代碼和其他東西
    - 有許多版本，許多站點，而且站點每天都在變化
    - 關於新功能有很多想法
    - 處於不斷變化的狀態
  - 這是一個實際試驗 remailers 既非常容易又非常有啟發性的領域……remailers 的「理論」是直截了當的（相比之下，例如 digital cash），而且學習經驗無論如何都比理論好。
  - 有大量的特性、想法、提案、討論點和其他此類東西。沒有 FAQ 可以開始涵蓋關於 remailers 的數千篇帖子所涵蓋的範圍。

## 8.3. Anonymity and Digital Pseudonyms
### 8.3.1. 為什麼 anonymity 如此重要？
  - 它允許逃離過去，這是重新開始的一個通常必不可少的元素（Western frontier、French Foreign Legion 等的一個重要功能，隨著 dossiers 無論我們去哪裡都跟著我們，我們正在失去這一點）
  - 它允許新的和多樣化的意見類型，如下所述
  - 更根本的是，anonymity 很重要，因為 identity 不像在我們的 dossier 社會中所宣稱的那樣重要。也就是說，如果 Alice 希望對 Bob 保持 anonymous 或 pseudonymous，Bob 不能「要求」她提供她的「真實」姓名。這是他們之間協商的問題。（Identity 不是免費的……它像任何其他憑證一樣，不能被要求，只能協商。）
  - 投票、閱讀習慣、個人行為……所有這些都是 privacy（= anonymity，實際上）至關重要的例子。下一節給出了 anonymity 的長長理由列表。
### 8.3.2. Anonymity 和 pseudonymity 有什麼區別？
  + 在一個層面上，沒有太多區別……我們經常在強烈的意義上使用術語 "digital pseudonym"，其中實際 identity 無法輕易推斷
    - 這在某種意義上是 "anonymity"
  - 但在另一個層面上，pseudonym 攜帶 reputations、credentials 等，並且_不是_ "anonymous"
  - 人們有時出於異想天開的原因使用 pseudonyms（例如，"From spaceman.spiff@calvin.hobbes.org Sep 6, 94 06:10:30"），有時為了將不同的 mailing lists 分開（為不同的群體使用不同的 personnas），等等。
### 8.3.3. Anonymity 的缺點
  - 誹謗和其他類似的對 reputations 的危險
  + 肇事逃逸行為（主要在 Net 上）
    + 另一方面，這種咆哮可以被忽略（KILL file）
      - 正面的 reputations
  - 基於身體威脅和追蹤的 accountability 丟失了
  + 實際問題。在 Cypherpunks list 上，我經常不那麼認真地對待 "anonymous" 訊息。
    - 它們通常比普通帖子更怪異和更具煽動性，也許有充分的理由，而且它們肯定更難被認真對待和回應。這是意料之中的。（我應該指出，一些 pseudonyms，如 Black Unicorn 和 Pr0duct Cypher，已經建立了信譽良好的 digital personnas，非常值得回覆。）
  - 否認債務和義務
  + 幼稚的 flames 和瘋狂的帖子
    - 種族主義、性別歧視等
    - 像 Apple 的 "Rumormonger"？
  - 但這些是使用 pseudonym 的理由，其中 pseudonym 的 reputation 很重要
  + 犯罪……謀殺、賄賂等
    - 這些在關於 crypto anarchy 的章節中有更詳細的討論，因為這是一個主要關注點（此類服務的 anonymous markets）
### 8.3.4. "Privacy 和 anonymity 將如何受到攻擊？"
  - 剛剛列出的缺點經常被引用為我們不能擁有 "anonymity" 的理由
  - 像許多其他 "computer hacker" 項目一樣，作為 "Four Horsemen" 的工具：毒販、洗錢者、恐怖分子和戀童癖者。
  - 作為非法行為的避風港，例如間諜活動、武器交易、非法市場等。
  + 逃稅（「如果我們看不到它，我們就無法對其徵稅。」）
    - 同樣的系統使 IRS 成為商業交易中的「沉默夥伴」，並讓 IRS 能夠存取——並要求——商業記錄
  + 「歧視」
    - 它使歧視成為可能（這_曾經_是可以的）
    - 排他性社區，老男孩網絡
### 8.3.5. "如何在 anonymous forums 中控制隨機指控和瘋狂謠言？"
  - 首先，隨機指控和道聽途說的陳述是現代生活的常態；八卦、小報、謠言等。我們不會過分擔心該做什麼來阻止所有這些道聽途說甚至虛假的評論。（一個令人不安的趨勢是起訴或威脅起訴的傾向。而且越來越多的態度是，一個人可以表達_意見_，但不能發表聲明，「除非它們能被證明。」這不是言論自由的意義所在！）
  - 其次，reputations 很重要。我們基於各種事物信任聲明，包括：過去的歷史、其他人對真實性的評價、我們掌握的外部事實以及動機。
### 8.3.6. "關於 anonymity 的法律觀點是什麼？"
  + 報導稱 Supreme Court 推翻了一項南方各州要求小冊子分發者表明身份的法律。（我對此沒有引用。）
    - 然而，Greg Broiles 提供了這段引文，來自 _Talley v. State of California_, 362 U.S. 60, 64-65, 80 S.Ct. 536, 538-539 (1960)：「Anonymous 小冊子、傳單、手冊甚至書籍在人類進步中發揮了重要作用。歷史上受迫害的群體和教派不時能夠匿名或根本無法批評壓迫性的做法和法律。」
       
       Greg 補充道：「它後來寫道『即使是支持通過我們憲法的 Federalist Papers，也是以虛構的名字發表的。很明顯，anonymity 有時是為了最具建設性的目的而被採用的。』」[Greg Broiles, 1994-04-12]
       
  + 當然，許多作家、記者和其他人使用 pseudonyms，並且沒有面臨法律訴訟。
    - 只要他們不使用它來逃稅、逃避法律判決、實施欺詐等。
  - 我聽說（沒有引用）「為了戴面具而戴面具」在許多司法管轄區是非法的。很難相信，因為許多其他偽裝同樣有效，而且據推測沒有被取締（假髮、鬍鬚、化妝等）。我假設法律與人們在「不適當」的地方戴滑雪面具等有關。如果是真的，那就是糟糕的法律。
### 8.3.7. Anonymous Systems 的其他一些用途：
  + Groupware 和 Anonymous Brainstorming 和 Voting
    - 基於 Lotus Notes 的系統，旨在鼓勵瘋狂的想法、害羞或過於禮貌的人的評論等
    - 這些系統最初可以在會議中開始，然後擴展到遠程站點，最終擴展到全國和國際論壇
    - NSA 可能會因這些趨勢而心臟病發作……
  + 加密訊息的「民主牆」
    - 可能使用延時金鑰（甚至 public key，用於閱讀 plaintext，在一段時間內不分發）
    - 在電子報紙的掩護下，擁有所有憲法保護：給編輯的信可以是 anonymous，廣告不需要篩選有效性，廣告聲明不是報紙的責任，等等。
  + Anonymous 評論和 hypertext（用於新型期刊）
    + 優點
      - 誠實
      - 增加話語的「溫度」
    + 缺點
      - 增加 flames
      - 故意誤導
  + Store-and-forward 節點
    - 用於促進 anonymous voting 和 anonymous 查詢（或閱讀）系統
    - Chaum 的 "mix"
    + 電話轉發系統，使用 digital money 支付服務費用
      - 和 TRMs？
  + Fiber optics
    + 隨著數百萬英里的鋪設，很難追蹤，包括私人建築物內幾乎無法追蹤的線路
      - 假設政府懷疑加密的 packets 正在進入 Apple 的建築物……如果沒有任何關於犯罪被協助和教唆的直接知識，政府可以要求從輸入到輸出的訊息映射嗎？
      - 也就是說，政府會要求完全披露所有 routings 嗎？
    - 高 bandwidth 意味著部署此類系統的自由度很大
  + 在系統內部，即使用者登錄到安全系統並獲得對其自己的處理器的存取權限
    - 在像 NCR/ATT 3600（甚至更大）這樣的 288 處理器系統中
    - 在他的 cryptonym 下，他可以存取某些檔案，生成其他檔案，並將訊息 untraceably 存放在其他 mail 位置，供其他 agents 或使用者稍後檢索和轉發……
    - 在某種意義上，他可以利用這種存取權限來啟動他自己的 agent processes（anonymity 對於許多基於 agent 的系統至關重要，digital money 也是如此）
  + 其他人將郵件攜帶到其他站點的經濟激勵……
    - 進一步擴散和隱藏真實功能
  + Binary systems（完成訊息需要兩個或更多部分）
    - 可能使用 viruses 和 worms 來處理分發這些訊息的複雜性
    - agents 可以處理轉移，agents 之間隔離，因此無法追蹤 routing（想想 "Double-Crossed" 中的場景，大麻包從飛機傳遞到船，再到直升機，再到卡車，再到汽車）
    - 這可以防止陰謀
  + Satellites
    + 物理安全性，因為必須擊落衛星才能停止廣播
      + 場景：WARC（或任何人）在 1996 年將廣播權授予某個國家或財團，然後該國家或財團接受任何和所有付費客戶
        - 現金
        - 衛星運營商的 BCCI
    + VSATs, L-Band, Satellites, Low-Earth Orbit
      - Very Small Aperture Terminals
      - L-Band……什麼頻率？
      + LEO，就像 Motorola 的 Iridium 一樣，提供了幾個優點
        - 低功率接收器和更小的天線
        - 發射成本低，因為尺寸小且對 10 年可靠性的需求較低
        - 避免了 "orbital slot" 許可證的泥潭（雖然我推測仍然涉及一些許可證）
      - 可以與脈衝或非正弦傳輸結合使用
### 8.3.8. "True Names"
### 8.3.9. 獲得 pseudonyms 的許多方法：
  - Telnet 到 "port 25" 或使用 SLIP 連接來更改 domain name；不是很安全
  - Remailers
### 8.3.10. "Pseudonymity 如何被破壞？"
  - 風格、headers、sig blocks 等方面的失誤
  - 無意中透過 remailers 洩露
  - remailers 的 traffic analysis（不太可能，至少對於非 NSA 對手而言）
  - 相關性，違反 "indistinguishability principle"
### 8.3.11. 雜項問題
  - 即使是 digital pseudonyms 也會變得令人困惑……最近有人誤以為 "Tommy the Tourist" 是一個實際的 digital pseudonym（當然這只是附加到所有通過特定 remailer 的帖子上的）。

## 8.4. Reasons for Anonymity and Digital Pseudonyms (and Untraceable E-Mail)
### 8.4.1. （理由太多了，而且這個問題經常被問到，所以我把這些各種理由收集在這裡。當然可以添加更多。）
### 8.4.2. 一般 Privacy
### 8.4.3. 身體威脅
  + "corporate terrrorism" 不是神話：毒販和其他「邊緣」商人每天都面臨這個問題
    - 勒索、威脅、綁架
  + 未來的許多企業可能不像傳統觀點認為的那樣「紳士」
    - 目睹 Intel 和 AMD 之間的惡意，然後想像它變得糟糕十倍
    - 國家競爭，即使在表面上合法的企業中（想想軍火商），也可能導致更多地使用暴力
    + Mafia 和其他有組織犯罪集團可能會試圖向市場參與者勒索付款或讓步，導致他們尋求 anonymous 系統的相對保護
      - 帶有 reputations
    + 請注意，呼籲受威脅者向警察尋求保護有幾個問題
      - 這些活動可能是非法的或處於非法邊緣（這就是 Mafia 經常介入的原因，也是為什麼它有時甚至可能產生積極影響，充當非法活動的警察）
      - 警察通常太忙而無法介入，因為如此多的身體犯罪堵塞了法院
  - 勒索和綁架可以使用這些 cryptoanarchy 技術來完成，從而導致一種軍備競賽
  + 受虐待的婦女和家庭可能需要相當於「證人保護計劃」的東西
    + 由於追蹤信用卡購買很容易，如果有適當的賄賂和/或法院命令（甚至 hacking），受虐待的妻子可能會尋求使用 pseudonyms 的信用卡
      - 一些信用卡公司可能會幫忙，作為一種政治正確的社會姿態
      + 或者像 NOW 和 Women Against Rape 這樣的團體甚至可能提供他們自己的卡
        - 也許由某種 escrow 基金支持
        - 可以是 debit cards
  + 參與 cyberspace 業務的人可能會擔心現實世界中的報復或勒索
    - 來自他們政府的威脅（出於所有通常的原因，加上回扣、關閉他們的威脅等）
    - 來自那些覬覦他們成功的人的掠奪……
### 8.4.4. Voting
  - 在西方社會，我們理所當然地認為投票應該是 "anonymous"——無法追蹤，無法關聯
  - 我們不會問人們「你有什麼要隱瞞的？」或告訴他們「如果你匿名做某事，那一定是非法的。」
  - 同樣的教訓應該適用於政府越來越要求提供身份證明的許多事情
  + Clubs, Organizations, Churches 等中的 Anonymous Voting
    + 傳播 CA 方法的主要途徑：「電子黑球」、加權投票（如股份數量）
      + 例如，一家公司發行 "voting tokens"，可以 anonymous 地用於投票
        - 甚至賣給其他人（就像賣股票一樣，除了只賣特定選舉的投票權更便宜，而且許多人不太關心選舉）
      + 一種防止 deep pockets 訴訟的方法，例如在種族歧視案件中
        - 其中董事因公司採取的某些行動而被起訴——anonymity 將給他一些法律保護，一些 "plausible deniability"
      + 可以建立系統（參見 Salomaa），其中一些 "supervotes" 擁有黑球權力，但這些否決權的使用與標準多數決投票無法區分
        - 即，除了投黑球的人，沒有人會知道是否使用了黑球！
        + 政府會尋求限制這種 protocol 嗎？
          - 聲稱歧視潛力或濫用投票權？
    + Justice Department（或 SEC）會尋求推翻 anonymous voting 嗎？
      - 作為邁向「完全披露」社會的潛在舉措的一部分？
      - 與反歧視法、accountability 等有關。
    + Reputation-Based Systems（Journals, Markets）中的 Anonymous Voting
      + 客戶可以對產品、服務質量、他們參與的各種交易進行投票
        - 不清楚投票權將如何分配
        - 這個想法是為了避免訴訟、供應商的制裁等（如 Bose 訴訟案）
      + Journals
        - 一個典型的例子，我必須包括在內，因為它結合了 anonymous refereeing（已經是標準的，以原始形式）、hypertext（鏈接到評論）和基本的言論自由問題
        - 這可能是一個早期的使用領域
      - 整個消費者評論領域可能是讓 CA bandwidth 啟動並運行的一種方式（大量的 PK-encrypted traffic 在各種 nets 中流動）
### 8.4.5. 維護言論自由
  - 保護言論
  + 避免因有爭議的言論而遭到報復
    - 這種言論可能有爭議、侮辱性、可怕、政治不正確、種族主義、性別歧視、物種歧視和其他可怕的……但 remailers 和 anonymity 使這一切都不可能停止
  - whistleblowing
  + 政治言論
    - KKK, Aryan Resistance League, Black National Front, 隨便什麼
    - 參見 Orson Scott Card 的小說 "Ender's Game" 中 "Locke" 和 "Demosthenes" 之間的「辯論」。
  - （其中許多原因也是為什麼 'data havens' 最終會建立起來……事實上，它們已經存在……homolka 審判等）
### 8.4.6. 採用不同的 personnas, pseudonyms
### 8.4.7. 選擇閱讀材料、觀看習慣等
  - 為了防止形成關於這方面的 dossiers，需要 anonymous 購買（現金適用於小件物品，不適用於視頻租賃等）
  + 視頻租賃
    - （注意：有「法律」規定此類發布是非法的，但是……）
  - 有線電視觀看習慣
  + 郵購
    - 是的，他們需要你的地址來發貨，但可能有 cutouts 可以脫鉤（例如，FedEx 有一天可能會提供這樣的服務
### 8.4.8. 請求資訊、服務、商品時的 Anonymity
  + 就像關於 Caller ID 和 900 號碼的爭議一樣：人們不希望他們的電話號碼（以及因此的身份）被輸入到巨大的消費者偏好 data banks 中
    - 關於他們買的東西，他們租的視頻，他們讀的書。等等。（各種法律保護其中一些領域，如圖書館書籍、視頻租賃）
    - 訂閱列表已經是一個蓬勃發展的轉售市場……隨著電子訂閱，這將變得更快、更精細地「調整」：因此渴望 anonymous 地訂閱
  + 一些可能需要 anonymity 的「敏感」服務的例子（特別是與計算機、modems、BBSes 相關）
    + 閱讀不尋常或敏感的群組：alt.sex.bondage 等
      - 或發帖到這些群組！
      - 最近關於 NAMBLA 的爭議可能會使這種保護對某些人來說更可取（同時呼籲限制！）
    - 發帖到這些群組，特別是考慮到記錄是永久的，並且政府機構閱讀和歸檔帖子（這是一件完全微不足道的事情）
    - 請求個人問題的幫助（相當於經常看到的 "Name Witheld"）
    + 討論有爭議的政治問題（誰知道 20 年後當發帖人尋求政治職位時，什麼會有爭議？）
      - 鑑於一些團體已經（1991 年）發布了他們試圖抹黑的人過去的帖子！
    + 注意：發帖到 BBS 群組或聊天線路與給編輯寫信之間的區別是顯著的
      - 部分是技術上的：編譯帖子記錄比剪輯給編輯的信要容易得多（儘管隨著掃描儀使這變得容易，這種情況將迅速改變）
      - 部分是社會學的：寫信的人知道信件將與過刊一起永久保存，合訂本將保存他們的話語數十年（並且可以想像會回來困擾他們），但發帖到 BBSes 的人可能認為他們的話語是暫時的
      + 還有其他一些因素
        - 沒有編輯
        - 沒有時間延遲（也沒有機會打電話給編輯並撤回匆忙或憤怒中寫的信）
        + 信件可以，而且經常是用 "Name Witheld" 簽名寫的——這目前在網絡上幾乎是不可能做到的
          - 儘管一些非正式的「轉發」服務已經如雨後春筍般湧現
  + 企業可能希望保護自己免受因員工評論而引起的訴訟
    + 通常的「這裡表達的觀點不是我雇主的觀點」可能不足以保護雇主免受訴訟
      - 想像種族主義或性別歧視的評論導致訴訟（或者至少被提出作為公司培養的「態度」類型的證據，例如，「我為 Intel 工作了 12 年，可以告訴你黑人是很差的工程師。」）
    + 員工可能會發表損害公司聲譽的評論
      - 注意：這與目前的情況不同，目前言論自由優先於公司關注，因為發布到 BBS 的帖子被廣泛傳播，可以被電子搜索（例如，AMD 律師搜索 1988-91 年的 UseNet 帖子，尋找任何 Intel 員工發布的玷污 AMD 芯片質量或其他方面的帖子），
    - 因此，公司的員工可能會通過採用 pseudonyms 來保護自己和他們的雇主
  + 企業可能在不想提醒競爭對手的情況下尋求資訊
    - 目前這是通過 agents、「高管獵頭公司」和律師完成的
    - 但它將如何演變以處理電子搜索？
    + 與提交 "Freedom of Information Act" 請求、專利等有一些類比
      + 隨著公司搜索成堆的電子歸檔材料變得有利可圖，這些「釣魚探險」將隨著時間的推移而增加
        - 環境影響研究、健康和安全披露等
        - 可能是某些公司專門從事的事情
  + Anonymous Consultation Services, Anonymous Stringers or Reporters
    + 想像一個資訊經紀人，也許在類似 AMIX 的服務上，擁有一個 stringers 網絡
      + 想想 Hallahan 的 The Trade 中的軍火交易通訊作者，他的 stringers 網絡為他提供提示和內幕消息
        - 可以使用安全的網絡，而不是在秘密地點會面，這是一個非常昂貴的提議（在時間和旅行方面）
        - 帶有 reputations, digital pseudonyms 等。
    + 他們可能不希望他們的真實身份被知曉
      - 來自雇主、前雇主、政府機構的威脅
      + 通過各種將變得更加普遍的犯罪行為進行騷擾（例如，可以輕易地僱用襲擊者甚至刺客）
        - 邁向 anonymity 的整體趨勢的一部分
      - 害怕訴訟、許可要求等
    + 此類 Anonymous Consultation Services 的候選人
      + 一份軍火交易通訊
        - 在準確性和及時資訊方面享有極好的聲譽
        + 有點像 Jane's 的電子形式
          - 伴隨著醜聞和政府關注
        - 但沒人知道它來自哪裡
        + 一個將其分發給訂閱者的站點將其與另一大批轉發材料一起獲得
          - NSA, FBI, Fincen 等試圖追蹤它
      + "Technology Insider" 報導各種新技術
        - 模仿 Hoffler 的 Microelectronics News，這是 Valley 二十年來領先的提示表
        - 編輯為提示付費，付款分兩部分：立即付款和依賴時間的付款，以便提示的準確性及其最終重要性（根據編輯的判斷）可以得到相應的獎勵
        + PK 系統，貢獻者能夠加密然後公開發布（使用他們自己的擴散手段）
          - 他們的訊息包含進一步的材料，如 authentications，發送付款的地方等
      + Lundberg 的 Oil Industry Survey（或類似的）
        - 即，一份相當傳統的通訊，作者是公開知名的
        - 在這種情況下，作者是已知的，但貢獻者的身份得到了很好的保護
      + 一份 Conspiracy Newsletter
        - 報導所有最新的不當行為理論（如本大綱的 "Conspiracies" 部分所述）
        + 一個皺褶：一個巨大的 hypertext web，貢獻者可以添加鏈接和節點
          + 自然地，他們的真實姓名——如果他們不關心現實世界的影響——或者他們的一個 digital pseudonyms（不妨使用 cryptonyms）被附上
            + 各種 reputations 算法
              - 曾經寫過的所有東西的總和，以某種方式通過其他評論、「投票」等來衡量
              - 一種移動平均線，考慮到學習會發生，就像研究人員可能會隨著時間的推移變得更好，並且隨著 reputation-based 系統被更好地理解，人們開始意識到仔細寫作的重要性
      + 以及所有中最具爭議的一個：Yardley 的 Intelligence Daily
        - 雖然它可能比每天更頻繁地發布！
        + 一位前特工在 90 年代中期建立了這個，通過 anonymous packet-switching 系統徵集稿件
          - 在接下來的幾年裡進行了改進
          - 方法的組合
        - 政府一直在努力確定編輯 "Yardley" 的身份
        - 他根據資訊的價值提供回報，甚至有一個 "Requests" 部分和一個 Classified Ad 部分
        - 一個 hypertext web，類似於上面的 Conspiracy Newsletter
        + 政府會試圖用虛假資訊抹黑通訊嗎？
          - 當然，這是 reputation-based 系統中的標準策略
          + 但 Yardley 已經為此開發了幾種過濾器
            - 逐漸建立 reputations 的 digital pseudonyms
            - 他自己的一種交叉檢查
            - 他甚至使用語言過濾器來分析文本
          + 那又怎樣？
            - 世界充滿了虛假資訊、謠言、謊言、半真半假的事實，不知何故事情還在繼續……
      + 其他類似 AMIX 的 Anonymous Services
        + 毒品價格和提示
          - 關於各種毒品質量的提示（例如，「幾個可靠的消息來源告訴我們，最新的 Maui Wowie 非常強烈，數字如下……」）
          + 毒品的合成（可能是單獨的訂閱）
            - 設計師毒品
            - 家庭實驗室
            - 避免檢測
        + The Hackers Daily
          - 關於 hacking 和 cracking 的提示
          - anonymous 系統本身（更多提示）
        - 產品評估（需要 anonymity 以允許誠實的評論，並更好地防止訴訟）
    + 報紙開始關注為新聞提示付費的趨勢
      - 由獨立的諮詢服務
      - 但他們能做什麼？
      + 嘗試訴訟，以防止涉及付款時的 anonymous 提示
        - 他們的律師引用逃稅和國家安全方面
  + Private Data Bases
    + 任何提供 data bases 存取權限的組織都必須擔心某人——心懷不滿的客戶、whistleblower、政府、任何人——會呼籲公開檔案
      - 根據各種 "Data Privacy" 法律
      - 或者只是一般情況（侵權法、訴訟、"discovery"）
    + 因此，將採取措施將實際數據與實際使用者隔離，也許通過 cutouts
      + 例如，數據服務出售存取權限，但通過無法追蹤的路徑將搜索分包給其他服務
        + 這可能無法在一般情況下被取締——儘管任何特定的交易後來都可能被宣布為非法等，此時鏈接被切斷並建立新的鏈接——因為這將取締所有分包安排！
          - 即，如果 Joe's Data Service 收取 1000 美元搜索 widgets，然後使用另一個可能短暫的（意味著 cutout）數據服務，訴訟最多只能迫使 Joe 停止使用這個無法追蹤的服務
          - 間接層次（以及阻止調查傳播的 firewalls）
  + Medical Polls（如 AIDS 調查、性行為調查等）
    + 回想一下參與者通過拋硬幣回答問題的方法……分析師仍然可以恢復重要的整體資訊，但 "phase" 丟失了
      - 即，回答 "Yes" 的個人對問題「你曾經有過 xyz 性行為嗎？」可能真的回答了 "No"，但他的答案被拋硬幣翻轉了
    + 研究人員甚至可能採用複雜的方法，其中保留明確的日記，但隨後在 anonymous mailing 系統下傳輸給研究人員
      - authentication、有效性等的明顯危險
  + 醫療測試：人們尋求 anonymity 的許多原因
    - AIDS 測試是卓越的例子
    - 但也測試可能影響可保性或就業的條件（例如，人們可能會去 Mexico 或其他地方的醫療避風港進行測試，如果保險公司得知「先決條件」，這些測試可能會導致不可保）
    + 除了 AIDS 和 STDs，提供 anonymous 諮詢可能既非法又違反醫學倫理
      - 也許人們會去其他國家旅行
### 8.4.9. 屬於某些 Clubs, Churches, or Organizations 的 Anonymity
  + 人們擔心如果他們的成員資格現在或以後被發現，會遭到報復或尷尬
    - 例如，屬於有爭議團體或俱樂部的教會成員
  - 主要或全部是不需要身體接觸或其他個人接觸的那些（有限的一組）
  - 類似於其他地方描述的基於 cell 的系統
  + anonymous clubs 或 organizations 的候選人
    - Earth First!, Act Up, Animal Liberation Front 等
    - NAMBLA 和類似的有爭議團體
  - 所有這些類型的團體都有非常直言不諱、非常顯眼的成員，甚至顯眼到尋求電視報導的程度
  - 但可能還有更多人會加入這些團體，如果他們的身份可以被屏蔽在公眾群體之外，為了他們的事業、他們的家庭等
  + 諷刺的是，公司對被認為對公司有敵意（或使他們面臨次要訴訟、索賠等）的外部活動的打擊可能會導致更多地使用 anonymous 系統
    - 團體中基於 cell 的成員資格
  - 團體中 anonymous 成員資格的增長（使用 pseudonyms）有利於增加那些否則害怕加入的人的成員資格，例如，激進的環保團體
### 8.4.10. 提供建議或資訊指針的 Anonymity
  - 假設有人說誰在出售某種非法或違禁產品……這也是非法的嗎？
  - hypertext 系統將使這不可避免
### 8.4.11. 評論、批評、反饋
  - 「這學期我正在為一個班級授課，明天我要：1) 告訴我的學生如何使用 remailer，以及 2) 徵求對我教學的 anonymous 反饋。
     
     「我想這會讓他們不那麼擔心提出誠實的建議和評論（當然，假設他們中有人費心的話）。」[Patrick J. LoPresti patl@lcs.mit.edu, alt.privacy.anon-server, 1994-09-08]
### 8.4.12. 防止訴訟、"deep pockets" 法律
  + 通過不允許實體的財富與行動相關聯
    - 這也通過隱藏資產起作用，但 IRS 對此不滿，因此取消發帖或郵寄名稱與實際實體的關聯通常更容易
  + "deep pockets"
    - 隱藏身份以阻止此類訴訟（無論出於何種原因，正確或錯誤地提起）將符合某些人的利益
    - 帖子和評論可能會使作者面臨誹謗、虛假陳述、不公平競爭等訴訟（在這些黑暗的州，言論自由就到此為止了）
    + 雇主也可能面臨同樣的訴訟，無論他們的員工從哪裡發帖
      - 基於脆弱的理由，即員工代表其雇主行事，例如，在 Usenet 上捍衛 Intel 產品
    - 順便說一句，這是人們尋求隱藏部分資產的方法的另一個原因——防止在 deep pockets 訴訟中被沒收（或家庭疾病，其中各種機構試圖扣押他們能扣押的任何人的資產）
    - 允許這些交易的同一台計算機也將允許更快地確定誰擁有最深的口袋！
  + 通過使實體免受可能引發訴訟等的「性別歧視」或「種族歧視」評論的影響
    - （別笑——許多公司越來越擔心他們的員工在 Usenet 上寫的東西可能會引發針對公司的訴訟。）
  + 許多交易在某些司法管轄區可能被視為非法
    + 即使在一些服務或商品提供者無法控制的司法管轄區
      - 例如：槍支製造商在 District of Columbia 對槍支死亡負責（儘管這最近被取消了）
    - 法律迷宮可能會導致一些人尋求 anonymity 以保護自己免受這個迷宮的侵害
  + 場景：Anonymous 器官捐贈庫
    + 例如，一種「營銷」稀有血型或任何東西的方法，而不會讓自己面臨強制捐贈或其他制裁
      - 「強制捐贈」涉及潛在接受者提起的訴訟
      - 至少在報價時……交易完成時會發生什麼是另一個領域
    - 以及一種避免越來越多的政府 stings 的方法
### 8.4.13. Journalism 和 Writing
  + 作家有採用 pseudonyms 的悠久傳統，原因多種多樣
    - 因為他們無法以 True Names 出版，因為他們_不想_他們的真實姓名被出版，為了好玩，等等。
    - George Elliot, Lewis Carroll, Saki, Mark Twain 等。
  - 記者
  + 電台唱片騎師
    - 一位為科技公司工作的 Cypherpunk 在他的兼職廣播工作中使用 "Arthur Dent" ("Hitchhiker's Guide") 的 "on air personna"……他告訴我，這是一種常見的情況
  + whistleblowers
    - 這是一個早期的用途
  + 政治敏感人士
    - "
    + 我隨後在 anon.penet.fi 上獲得了一個帳戶作為 "Lt.
      - Starbuck" 實體，所有後來的 FAQ 更新都來自該帳戶。
      - 出於當時看來很重要的原因，我承擔了
      - 成為 FAQ 的 moderator/editor。"
      - <an54835@anon.penet.fi, 4-3-94, alt.fan.karla-homolka>
  + 例子：Remailers 被用來繞過 Karla Homolka 案件的出版禁令
    - 各種 pseudonymous 作者發布定期更新
    - 加拿大非常驚愕！
  + 避免因寫作、編輯、分發或銷售「破壞性」材料而被起訴或索賠是 anonymous 系統出現的另一個原因：參與該過程的人將尋求使自己免受堵塞法院的各種侵權索賠的影響
    - x-rated 或其他「不可接受」材料的製片人、發行商、導演、作家甚至演員可能必須擁有 anonymous 系統的保護
    - 想像 fiber optics 以及視頻和脫口秀的激增……衛道士和檢察官將使用 "forum shopping" 來阻止存取，起訴製片人等。
### 8.4.14. 學術、科學或專業
  - 保護其他 reputations（專業、作者、個人等）
  - 更廣泛的行動和行為範圍（作者可以冒險）
  - 在 pseudonyms 下提出想法
  - 如果需要，稍後將這些 pseudonyms 鏈接到自己的 identity（credential transfer 的一個案例）
  - 提出不尋常的觀點
  - Peter Wayner 寫道：「我認為許多在技術新聞組閒逛的人會非常熟悉學術期刊實行的 anonymous review 程序。當審稿人可以暢所欲言地談論一篇論文而不必擔心報復時，這是有價值的。當然，每個人都向我保證，該系統從來都不是真正的 anonymous，因為總是只有三四個人有資格審查每篇論文。:-) ....也許我們應該特意對新聞組中的論文和想法發表 anonymous、技術性的評論，以促進 cypberspace 中 anonymous 評論文化的發展。」[Peter Wayner, 1993-02-09]
### 8.4.15. 醫療測試和治療
  - anonymous 醫療測試，如 AIDS 測試
### 8.4.16. 虐待、康復
  + 個人問題討論
    - 亂倫、強姦、情感、Dear Abby 等。
### 8.4.17. 繞過出口法
  - Anonymous remailers 已被用於繞過 ITARs……這就是 PGP 2.6 如何迅速且（我們希望！）untraceably 從 MIT 和美國站點傳播到 offshore 地點的方式。
### 8.4.18. 性群組，有爭議話題的討論
  - 各種 alt.sex 群組
  - 人們可能會感到尷尬，可能擔心雇主的影響，可能不希望家人和朋友看到他們的帖子，或者可能只是意識到 Usenet 在許多許多地方被歸檔，甚至可以在 CD-ROM 上獲得，並且在未來幾十年內將可以輕易搜索
  + 公開發布到 UseNet 和其他公告板的 100% 可追溯性非常扼殺自由表達，並成為使用 anonymous（或 pseudononymous）板和網絡的主要理由之一
    - 可能會呼籲制定法律禁止此類彙編，就像英國數據法一樣，但基本上，當帖子發送到成千上萬台機器並被許多這些節點和成千上萬的讀者永久歸檔時，幾乎無能為力
    - 讀者可能會將材料納入他們自己的帖子等（因此英國法律的荒謬性）
### 8.4.19. 避免政治間諜活動
  + 許多國家的 TLAs 監控幾乎所有的國際通信（以及大量的國內通信）
    - 公司和個人可能希望避免報復、制裁等。
    - 據報導，PGP 被幾個持不同政見的團體使用，幾個 Cypherpunks 參與協助他們。
    - 「……一個合法的應用是允許國際政治團體或公司交換 authenticated 訊息，而不會面臨被三個字母的美國機構、外國情報機構或第三方間諜/妥協的風險。」[Sean M. Dougherty, alt.privacy.anon-server, 1994-09-07]
### 8.4.20. 有爭議的政治討論，或政治團體、mailing lists 等的成員資格
  + 回想 House UnAmerican Activities Committee
    - 及其現代變體：「你現在是，或者曾經是 Cypherpunk 嗎？」
### 8.4.21. 防止跟蹤和騷擾
  - 避免物理追蹤（騷擾、"wannafucks"、跟蹤者等）
  - 婦女和其他人經常收到來自在許多新聞組中數量超過她們 20 比 1 的男性的 "wannafuck?" 訊息——pseudonyms 有幫助。
  - 鑑於 net I.D.s 可以輕易轉換為物理位置資訊，許多婦女可能會擔心。
  + 男性也可能擔心，鑑於例如 S. Boxx/Detweiler 發出的死亡威脅。
    - 碰巧，S. Boxx 威脅了我，而我讓我的家庭電話號碼和位置眾所周知……但我武裝好了，準備好了。
### 8.4.22. 壓力釋放閥：知道一個人可以逃離或前往邊疆而不背負過去
  - 也許高累犯率與這種無法逃脫有關……一旦成為罪犯，終身被標記（肯定被拒絕從事高薪工作）
### 8.4.23. 排除訴訟、傳票、捲入法律機器
### 8.4.24. 商業原因
  + 公司可以訂購供應品、資訊，而不露聲色
    - Disney 通過 anonymous cutouts 購買土地（以避免推高價格）
    - 秘密成分（傳說中，Coca Cola）
  - 避免上述的 "deep pockets" 綜合症
  - 擊敗分區和許可要求（例如，某種類型的業務可能不被「允許」在家庭辦公室進行，因此房主將不得不使用 cutouts 來躲避執法者）
  - 保護免受（和對）雇主的影響
  + 公司的員工可能不僅僅需要聲稱他們的觀點不是雇主的觀點
    - 例如，種族主義帖子可能會使 IBM 面臨制裁、指控
    + 因此，許多員工可能不得不進一步隔離他們的身份
      - blanc@microsoft.com 現在是 blanc@pylon.com……巧合？
  + 兼職員工（最初對 Black Net 和 AMIX 的擔憂）
    - 雇主可能有各種擔憂，因此員工需要隱藏身份
    - 注意這與許可和分區方面相交
  - 出版商、服務提供商
  + 某些類型的 Reputation-Based Systems 所需
    + 受人尊敬的科學家可能希望提出一個推測性的想法
      - 並且能夠稍後證明這確實是他的想法
### 8.4.25. 防止報復
  - whistleblowing
  + 組織抵制
    - （在規範言論自由的法律和 "SLAPP" 訴訟的時代）
  + visa 夥計們（Cantwell 和 Siegel）威脅那些評論的人要起訴
    - 那家發帖到 5,000 個群組的律師事務所……也再次提出了為什麼 Net 應該得到補貼的問題
  - 參與公共論壇
  + 正如一位因 Usenet 評論而被威脅起訴的人所說：
    - 「現在他們威脅我。僅僅因為我公開表達了我對他們極不負責任行為的看法。無論如何，我已經從我的站點取消了這篇文章，我公開為首先發布它道歉。我很害怕 :) 我收回我所有的話。下次將使用 anonymous 服務 :)」
### 8.4.26. 防止追蹤、監視、Dossier Society
  + 避免一般的 dossiers
    - 保存了太多的 dossiers；anonymity 允許人們至少稍微阻擋一下潮流
  + 獵頭、求職，在這些情況下透露身份並不總是一個好主意
    - 一些獵頭正在為你目前的雇主工作！
    - dossiers
### 8.4.27. 來自 Cypherpunks List 的一些例子
  + S, Boxx, aka Sue D. Nym, Pablo Escobar, The Executioner, 和 an12070
    - 但 Lawrence Detweiler 無論叫什麼名字
    + 他以幾種方式洩露了他的 pseudonym-true name 鏈接
      - 風格線索
      - 提到只有「另一個」可能聽說過的事情
      + sysops 承認某些鏈接
        - *不是* Julf，儘管 Julf 據推測知道 "an12070" 的身份
  + Pr0duct Cypher
    - Jason Burrell 指出：「以 Pr0duct Cypher 為例。許多人認為他/她正在做的事情(*)是一件好事，我見過他/她使用 Cypherpunk remailers 來隱藏他/她的身份....* 如果你不知道，他/她是編寫 PGPTOOLS 的人，以及 PGP 2.3a 的 hack 以解密用 2.6 編寫的訊息。我假設他/她這樣做是 anonymous 的，因為 ITAR 法規。」[J.B., 1994-09-05]
  + Black Unicorn
    - 是一位 Washington, D.C. 律師（我想）的 pseudonym，他在 Europe，特別是 Liechtenstein 和 Switzerland 與保守的銀行家和商人有業務聯繫。他參與 Cypherpunks 小組導致他採用了這個 pseudonym。
    - 諷刺的是，他與 S. Boxx/Detweiler 發生了爭執並威脅要採取法律行動。這導致了一場相當有啟發性的辯論發生。

## 8.5. Untraceable E-Mail
### 8.5.1. Remailers 的基本理念
  - 訊息被加密，信封套信封，從而使基於外觀的追蹤變得不可能。如果 remailer 節點對輸入和輸出之間的映射保密，「蹤跡」就會丟失。
### 8.5.2. 為什麼 untraceable mail 如此重要？
  + 請記住，"untraceable mail" 是普通郵件的默認情況，人們密封信封，貼上郵票，然後 anonymous 地將其投入信箱。不保留記錄，不需要回信地址（或確認），等等。
    - 區域郵戳顯示大致區域，但不顯示源郵箱
    + 我們許多人認為，如果今天首次引入目前的 anonymous mail 系統，將不會被「允許」
      - Postal Service 會要求個性化郵票、可驗證的回信地址等（不是萬無一失，或安全的，但是……）
  + 原因：
    - 防止編制誰在聯繫誰的 dossiers
    - 使聯繫成為個人事務
    - 許多實際用途：維護 pseudonyms、anonymous 合同、保護商業交易等。
### 8.5.3. Cypherpunks remailers 如何運作？
### 8.5.4. 簡單來說，我如何發送 anonymous mail？
### 8.5.5. Chaum 的 Digital Mixes
  - Digital mixes 如何運作？
### 8.5.6. "今天的 remailers 對 traffic analysis 安全嗎？"
  - 大多數不安全。許多關鍵的 digital mix 特性缺失，差距可能被利用。
  + 取決於使用的特性：
    - Reordering（例如，10 條訊息進，10 條訊息出）
    - Quantization 到固定大小（否則不同大小會給出線索）
    - 所有階段的 Encryption（當然，取決於客戶）
  - 但可能不安全，鑑於目前的 remailers 通常缺乏阻止 traffic analysis 的必要特性。Padding 是不確定的，batching 通常根本不做（人們珍惜速度，經常不選那些「太慢」的 remailers）
  - 最好將今天的 remailers 視為實驗，視為原型。

## 8.6. Remailers and Digital Mixes (A Large Section!)
### 8.6.1. 什麼是 remailers？
### 8.6.2. Cypherpunks remailers 與 Julf 的比較
  + 顯然，penet remailer 的長時間延遲正在增加。關於長達一週的延遲的投訴，回答是：
    - 「嗯，沒人阻止你使用優秀的 cypherpunk remailers 系列，從 remail@vox.hacktic.nl 開始。這些 remailers 完勝 anon.penet.fi。當天或最壞第二天服務，允許 PGP encryption，chaining，以及到 USENET 的 gateways。」[Mark Terka, The normal delay for anon.penet.fi?, alt.privacy.anon-server, 1994-08-19]
  + "Julf 的 remailer 負載有多大？"
    - 「我最近和 Julf 談過，他真正需要的是 750 美元/月和一次性 5000 美元來升級他的 feed/機器。我正在考慮贊助的可能性（但不要讓這阻止其他人嘗試）.....Julf 已經建立了一個擁有超過 100,000 人和 6000 條訊息/天的忠誠、信任的追隨者。升級他似乎是個好主意.....是的，還有其他 remailers。如果可以的話，讓我們使用它們，減輕 Julf 的負載。」[Steve Harris, alt.privacy.anon-server, 1994-08-22]
    - （現在如果對 Julf 的 remailer 的需求如此之高，似乎是部署某種收費系統的好機會，以支付進一步擴展的費用。毫無疑問，許多使用者會流失，但這就是商業的本質。）
### 8.6.3. "Remailers 如何運作？"
  - （MFAQ 也有一些答案。）
  - 簡單地說，它們通過獲取傳入的文本塊並尋找關於將剩餘文本塊發送到哪裡以及如何處理它（decryption、延遲、郵資等）的指令來工作
  + 一些 remailers 可以直接處理 Unix mail 程式的輸出，對 mail headers 進行操作
    - 程式名稱……
  + 我認為 Eric Hughes 在他研究這個問題的最初幾天想出的 "::" 格式結果是一個真正的勝利（也許可以與 John McCarthy 決定在 Lisp 中使用帶括號的 s-expressions 相媲美？）。
    - 它允許任意 chaining，所有具有標準 ASCII 文本的郵件訊息——我相信是所有 mailers——都可以使用 Cypherpunks remailers
### 8.6.4. "Remailers 有哪些用途？"
  - 這主要在其他章節中回答，概述了 anonymity 和 digital pseudonyms 的用途：remailers 當然是 anonymity 的使能技術。
  + 使用 remailers 來挫敗 traffic analysis
    - 一個有趣的評論來自我們小組之外的人，在討論斷開 U.K. 計算機與 Usenet 連接的提議時（因為英國關於誹謗、色情等的法律）：「PGP 隱藏了目標。Remailers 丟棄了源資訊。更偏執的 remailers 在重新發送時引入隨機延遲以挫敗 traffic analysis。你會驚訝於可以做什麼 :-).....如果你使用 chain，那麼第一個 remailer 知道你是誰，但目的地是加密的。最後一個 remailer 知道目的地但無法知道來源。中間的兩者都不知道。」[Malcolm McMahon, JANET (UK) to ban USENET?, comp.org.eff.talk, 1994-08-30]
    - 所以，消息正在傳播。注意對 Cyphepunks 類型 remailers 的強調，而不是 Julf 風格的 anonymous 服務。
  + 分發 anonymous 訊息的選項
    + 通過 remailers
      - 傳統方法
      - 優點：收件人不需要做任何特別的事情
      - 缺點：就是這樣——收件人可能不歡迎該訊息
    + 到 newsgroup
      - 一種訊息池
      - 優點：全球分發
    - 到 ftp 站點，或 Web 可訪問的站點
    - mailing list
### 8.6.5. "為什麼需要 remailers？"
  + Hal Finney 在 1993 年初的一個回答中很好地總結了原因。
    - 「Anonymous remailers 提供了幾個不同的優點。最簡單和最無爭議的優點之一是擊敗普通電子郵件上的 traffic analysis.....兩個希望私下交流的人可以使用 PGP 或其他加密系統來隱藏他們訊息的內容。但是他們正在相互交流的事實對許多人來說仍然是可見的：他們站點的 sysops 以及可能的中間站點，以及各種網絡窺探者。他們自然會渴望額外的隱私，這將掩蓋他們正在與誰交流以及他們在說什麼。
       
       "Anonymous remailers 使這成為可能。通過 remailers 在他們之間轉發郵件，同時仍然在（加密的）訊息內容中表明自己的身份，他們擁有比簡單加密更多的通信隱私。
       
       "（Cypherpunk 願景包括一個擁有成百上千個此類 remailers 運行的世界。郵件可以通過數十個此類服務反彈，與成千上萬的其他訊息混合，在每一步都重新加密。這應該使 traffic analysis 幾乎不可能。通過發送定期虛擬訊息，這些訊息只是在某個步驟被吞噬，人們甚至可以掩蓋他們_何時_在交流。）」[Hal Finney, 1993-02-23]
       
       "與 anonymous remailers 相關的更具爭議的願景在諸如 Vernor Vinge 的 "True Names" 或 Orson Scott Card 的 "Ender's Game" 等科幻小說中表達。這些描繪了計算機網絡廣泛使用的世界，但在其中許多人選擇通過 pseudonyms 參與。通過這種方式，他們可以提出不受歡迎的論點或參與不受歡迎的交易，而他們的活動不會與他們的真實身份聯繫起來。它還允許人們根據他們的想法質量而不是他們的工作、財富、年齡或地位來建立 reputations。」[Hal Finney, 1993-02-23]
  - 「這種方法的其他優點包括它擴展到電子在線交易。今天已經保留了許多我們金融交易的記錄——每次我們使用信用卡通過電話購買物品時，信用卡公司都會記錄下來。隨著時間的推移，甚至可能會收集並可能出售更多此類資訊。一個 Cypherpunk 願景包括能夠 anonymous 地進行交易，使用 "digital cash"，這將無法追溯到參與者。特別是對於購買「軟」產品，如音樂、視頻和軟件（這些最終都可能通過網絡交付），應該可以 anonymous 地進行此類交易。所以這是 anonymous mail 重要的另一個領域。」[Hal Finney, 1993-02-23]
### 8.6.6. "我實際上如何使用 remailer？"
  + （注意：Remailer 說明_經常_發布。我無法在這裡保持最新。諮詢各種 mailing lists 和 finger 站點，或使用 Web 文檔，以查找最新的說明、keys、uptimes 等_
    + Raph Levien 的 finger 站點非常令人印象深刻：
      + Raph Levien 有一個令人印象深刻的實用程序，可以 ping remailers 並報告 uptime：
        - finger remailer-list@kiwi.cs.berkeley.edu
        - 或使用 Web 在 http://www.cs.berkeley.edu/~raph/remailer-list.html
        - Raph Levien 還有一個 remailer chaining 腳本在 ftp://kiwi.cs.berkeley.edu/pub/raph/premail-0.20.tar.gz
  + Remailers 的 Keys
    - remailer-list@chaos.bsu.edu (Matthew Ghio 維護)
  + "為什麼 remailers 只對 headers 操作而不對訊息的 body 操作？為什麼 signatures 不被 remailers 剝離？"
    - 「構建忠實地傳遞訊息的整個 body 而不進行任何更改的 mailers 的原因是，它允許你通過該 mailer 發送任何 body 並依賴其忠實地到達目的地。」[John Gilmore, 93-01-01]
    - "::" 特殊形式是一個例外
    - 訊息 bodies 末尾的 Signature blocks 特別_不_應該被剝離，即使如果它們在無意中被意外留在裡面會導致安全漏洞。試圖剝離 sigs，它們有多種風格，將是一場噩夢，並且可能會剝離其他東西。此外，有些人可能想要附上 sig，即使是加密訊息。
    - 像往常一樣，任何人當然可以自由地擁有一個 remailer，它認為合適地處理訊息 bodies，但我預計這樣的 remailers 會失去客戶。
    - 另一種可能性是另一種特殊形式，例如 "::End"，可以用來界定要 remailed 的塊。但是很難讓這種「裝飾」被接受。
  + "Remailers 如何處理 subject lines？"
    - 以各種方式。有些忽略它，有些保留它，有些甚至可以接受指令來創建新的 subject line（也許在最後一個 remailer 中）。
    - 有理由不讓 subject line 通過 remailers 鏈傳播：它標記了訊息，因此使 traffic analysis 變得微不足道。但也有理由擁有 subject line——讓收件人更容易——因此存在這些添加 subject line 的方案。
  + "Nicknames 或 aliases 可以與 Cypherpunks remailers 一起使用嗎？"
    - 當然使用了 digitally signed IDs（例如 Pr0duct Cypher），但沒有在 remailing 和 mail-to-Usenet gateways 的字段中保留 nicknames。
    - 這也許可以作為一個額外的字段添加到 remailers 中。（我聽說 mail 字段比 Netnews 字段更能容忍添加的東西，使得 mail-to-News gateways 丟失額外的字段。）
    + 一些 remailer 站點支持它們
      - 「如果你想在 vox.hacktic.nl 分配一個 alias，只需要發送一些空郵件到 <ping@vox.hacktic.nl>，發送郵件的地址將被包含在 data-base 中.....由於 vox.hacktic.nl 在 UUCP 節點上，回覆可能需要一些時間，通常是 8 到 12 小時。」[Alex de Joode, <usura@vox.hacktic.nl>, 1994-08-29]
  + "Remailers 如何處理訊息的各個部分？它們會發送加密塊之後包含的東西嗎？它們應該嗎？Headers 呢？"
    + 顯然可以採取許多方法：
      - 按原樣發送所有內容，由發送者確保不留下任何罪證
      - 做出某些選擇
    - 我贊成發送所有內容，除非特別被告知不要這樣做，因為這對訊息的預期形式做出的假設較少，從而允許在設計新功能時有更大的靈活性。
    + 例如，這是 Matthew Ghio 對他的 remailer 所說的話：
      - 「加密訊息之後的所有內容都以明文形式傳遞。如果你不想要這個，你可以使用我的 remailer 的 cutmarks 功能將其刪除。（此外，remail@extropia.wimsey.com 不會附加加密訊息之後的文本。）這樣做的原因是它允許 anonymous 回覆。我可以為 remailer 創建一個 pgp 訊息，該訊息將被傳遞給我自己。我發送給你 PGP 訊息，你附加一些文本並將其發送到 remailer。Remailer 解密它並將其 remails 給我，我就收到了你的訊息。[M.G., alt.privacy.anon-server, 1994-07-03]
### 8.6.7. Remailer 站點
  - 當然，沒有站點的中央管理員，因此各種工具是開發自己的站點列表的最佳方式。（我懷疑我們許多人只是選定十幾個我們最喜歡的。隨著數百個 remailers 的出現，這將會改變；當然，將使用各種腳本程式來生成軌跡，處理嵌套加密等。）
  - Newsgroups alt.privacy.anon-server, alt.security.pgp 等經常報告最新的站點、工具等。
  + Remailers 的 Software
    + 運行 remailer 站點的 Software 可以在以下位置找到：
      - soda.csua.berkeley.edu 在 /pub/cypherpunks/remailer/
      - chaos.bsu.edu 在 /pub/cypherpunks/remailer/
  + 使用 Remailers 和 Keyservers 的說明
    + 關於如何使用 keyservers
      - 「如果你可以訪問 World Wide Web，請參閱此 URL: http://draco.centerline.com:8080/~franl/pgp/pgp-keyservers.html」[Fran Litterio, alt.security.pgp, 1994-09-02]
  + 識別 Remailer 站點
    + finger remailer-list@chaos.bsu.edu
      - 返回活動 remailers 的列表
      - 獲取更完整的資訊、keys 和說明，finger remailer.help.all@chaos.bsu.edu
      - gopher://chaos.bsu.edu/
    + Raph Levien 有一個令人印象深刻的實用程序，可以 ping remailers 並報告 uptime：
      - finger remailer-list@kiwi.cs.berkeley.edu
      - 或使用 Web 在 http://www.cs.berkeley.edu/~raph/remailer-list.html
      - Raph Levien 還有一個 remailer chaining 腳本在 ftp://kiwi.cs.berkeley.edu/pub/raph/premail-0.20.tar.gz
  + Remailer pinging
    - 「我編寫並安裝了一個 remailer pinging 腳本，它收集有關 remailer 特性和可靠性的詳細資訊。
       
          要使用它，只需 finger remailer-list@kiwi.cs.berkeley.edu
       
       在以下位置也有相同資訊的 Web 版本：
       http://www.cs.berkeley.edu/~raph/remailer-list.html」
       [Raph Levien, 1994-08-29]
  + 宕機的站點？？
    - tamsun.tamu.edu 和 tamaix.tamu.edu
### 8.6.8. "我如何在我的站點設置 remailer？"
  - 這不是給休閒使用者的，但肯定是可能的。
  - 「有人能幫我從檔案館安裝 remailer 腳本嗎？我沒有 Unix 經驗，完全不知道從哪裡開始。我甚至不知道這些是否需要 root 權限。任何幫助將不勝感激。」[Robert Luscombe, 93-04-28]
  - Sameer Parekh, Matthew Ghio, Raph Levien 都寫過說明....
### 8.6.9. "大多數 Cypherpunks remailers 是如何編寫的，使用什麼工具？"
  - 作為操作 mail 檔案、替換 headers 等的腳本
  - Perl, C, TCL
  - 「cypherpunks remailers 是用 Perl 編寫的，這有助於實驗和測試新接口。這個想法可能是最終將它們遷移到 C 以提高效率，但在這個實驗階段，我們可能想嘗試新想法，修改 Perl 腳本比 C 程式更容易。」[Hal Finney, 93-01-09]
  - 「我很欣賞 cypherpunks 的東西，但 perl 仍然不是一個非常廣泛使用的標準工具，而且我們並不是每個人都想學習另一種語言的來龍去脈……所以我確實為 C 版本鼓掌……」[Johan Helsingius, "Julf," 93-01-09]
### 8.6.10. 處理 Remailer 濫用
  + 燙手山芋
    - 一個被大量使用或懷疑被濫用的 remailer 可以選擇將其負載分配給其他 remailers。通常，他可以添加自己選擇的站點，而不是 remailing 到下一個站點。因此，他既可以減少對他的關注，也可以通過將部分流量分散到其他站點來增加掩護流量（它永遠不會減少他的流量，只是減少對他的關注）。
  + Flooding 攻擊
    - denial of service 攻擊
    - 就像在體育賽事中吹口哨一樣，混淆行動
    - DC-Nets，中斷（flooding 對 DC-Nets 的中斷與 mail bombs 對 remailers 的中斷是一個非常相似的問題）
  + "Remailers 如何處理濫用？"
    - 幾個 remailer 運營商已經關閉了他們的 remailers，要麼是因為他們厭倦了處理問題，要麼是因為其他人命令他們這樣做。
    - Source level 阻塞
    - 付費訊息：至少這讓濫用者_付費_並停止某些類型的 spamming/bombing 攻擊。
    - 破壞者在 Chaum 的 DC-Net 方案中以 anonymous 方式處理；這裡可能有一種方法可以使用它。
  + Karl Kleinpaste 是 remailers 的先驅（大約 1991-2 年）。他已經不再抱有幻想：
    - 「那裡有 3 個站點擁有我的軟件：anon.penet.fi, tygra, 和 uiuc.edu。我與 anon.penet.fi 的「普遍到達」政策有哲學上的分歧（其代碼現在是從我給 Julf 的原始軟件中分離出來的一個長期分離的菌株——事實上，到目前為止它可能是一個完全的重寫，我根本不知道）；....非常直率地說，曾兩次嘗試運行 anon servers，並且都因實際的法律困難而宕機，我不再信任人們使用它們了。」[Karl_Kleinpaste@cs.cmu.edu, alt.privacy.anon-server, 1994-08-29]
    - 參見 alt.privacy.anon-server 中的討論，了解更多關於他的 remailers 法律問題，以及他為什麼關閉他的
### 8.6.11. Remailers 的世代
  + 第一代 Remailer 特徵——現在（自 1992 年起）
    - Perl 腳本，簡單的 headers 處理，crypto
  + 第二代 Remailer 特徵——也許 1994 年
    - 某種形式的 digital postage（也許是簡單的優惠券或「郵票」）
    - 更靈活的異常處理
    - mail objects 可以告訴 remailer 使用什麼設置（延遲、latency 等）
  + 第三代 Remailer 特徵——1995-7？
    - protocol 協商
    + 類似 Chaum 的 "mix" 特徵
      - tamper-resistant 模塊（remailer 軟件在密封環境中運行，對操作員不可見）
  + 第四代 Remailer 特徵——1996-9？
    - 誰知道？
    - 基於 Agent（Telescript？）
    - 基於 DC-Net
### 8.6.12. Remailer identity escrow
  + 可能有一些用途……
    - 任何人會有什麼激勵？
    - 收件人可以 source-block 任何沒有某種手段應對嚴重濫用的 remailer……一個完美的自由市場解決方案
  - 也可能是強制性的
### 8.6.13. Remailer 特性
  + 有許多提議的變體、技巧和方法，它們可能會或可能不會增加整體 remailer 安全性（entropy, confusion）。這些經常在 list 上討論，一次一個。其中一些是：
    + 使用自己作為 remailer 節點。將流量路由回自己的系統。
      - 即使所有其他系統都受到損害……
    - 隨機延遲，超過滿足 reordering 要求所需的延遲
    - MIRVing，將 packet 分成多個部分發送
    - Encryption 當然是一個主要特性。
    + Digital postage。
      - 與其說是一個特性，不如說是一個獲得更多 remailers 並更好地支持它們的激勵/誘導。
  + "Remailer 網絡的特性是什麼？"
    - 已經考慮了大量的特性；有些是其他更基本特性的衍生物（例如，「隨機延遲」不是一個基本特性，而是實現真正需要的 "reordering" 的一種提議方式。而 "reordering" 只是實現傳入和傳出訊息 "decorrelation" 的方式）。
    + "Ideal Mix" 值得考慮，就像工程師研究 "ideal op amp" 一樣，無論是否可以構建一個。
      - 一個黑匣子，將傳入和傳出的 packets decorrelates 到某種程度的擴散
      - tamper-proof，因為外部世界看不到 decorrelation 的內部過程（Chaum 設想 tamper-resistant 或 tamper-responding 電路進行 decorrelation）
    + Real-World Mixes 的特性：
      + 傳入和傳出訊息的 Decorrelation。這是任何 mix 或 remailer 最基本的特性：模糊進入 mix 的任何訊息與離開 mix 的任何訊息之間的關係。如何實現這一點是這裡大多數特性的全部內容。
        - "Diffusion" 是通過 batching 或延遲實現的（危險：低流量擊敗簡單、固定的延遲）
        - 例如，在某個時間段內，20 條訊息進入一個節點。然後 20 條左右（可以更少，可以更多……沒有理由不添加訊息，或丟棄一些）訊息離開。
      + 應該支持 Encryption，否則 decorrelation 很容易通過簡單檢查 packets 被擊敗。
        - 顯然首選 public key encryption（否則 keys 在外部可用）
        - forward encryption，使用 D-H 方法，是一個值得探索的有用想法，傳輸後丟棄 keys....從而使傳票成為問題（例如，這已用於安全電話）。
      + Quanitzed packet 大小。顯然，packet 的大小（例如，3137 bytes）是訊息 identity 的強烈線索。Quantizing 到固定大小破壞了這個線索。
        + 但是由於有些訊息可能很小，有些很大，實際的折衷方案也許是 quantize 到幾個標準之一：
          - 小訊息，例如 5K
          - 中等訊息，例如 20K
          - 大訊息....以某種方式處理（也許拆分等）
        - 需要更多分析。
      + Reputation 和 Service
        - 營業多久了？
        - Logging 政策？訊息被 logged 嗎？
        - 按規定操作的期望
  + Remailer 使用的基本目標
    + 傳入和傳出訊息的 decorrelation
      - indistinguishability
      + "remailed 訊息沒有頭髮"（向那裡的黑洞迷致歉）
        - 沒有可用於進行關聯的區分特徵
        - 沒有先前外觀的「記憶」
    + 這通常意味著訊息大小 padding 到 quantized 大小
      - 有多少不同的大小取決於很多事情，如流量、其他訊息的大小等。
  + Encryption，當然
    - PGP
    - 否則，訊息很容易區分
  + Quantization 或 Padding：訊息
    - padded 到標準大小，或在大小上抖動以模糊原始大小。例如，典型短訊息為 2K，典型 Usenet 文章為 5K，長文章為 20K。（更長的訊息很難隱藏在大量更短的訊息中，但存在其他可能性：延遲長訊息直到積累了 N 條其他長訊息，將訊息拆分成更小的塊等。）
    + "Remailers 的 quanta 是什麼？也就是說，remailed 訊息的首選 packet 大小是多少？"
      - 在短期內，現在，remailed packet 大小幾乎就是它們開始時的大小，例如 3-6KB 左右。一些 remailers 可以 pad 到 quantized 水平，例如，到 5K 或 10K 或更多。水平尚未確定。
      - 從長遠來看，我懷疑會選擇更小的 packets。也許在 ATM packets 的粒度上。"ATM Remailers" 可能即將到來。（這稍微改變了 traffic analyis 的性質，因為 remailed packets 的_數量_增加了。
      - 一個反對論點：ATM 網絡不給發送者對 packets 的控制權……
      - 無論如何，我認為 packets 會變小，而不是變大。有趣的問題。
    - 「基於 Hal 的數字，我建議訊息大小的合理 quantization 是一組短的幾何增長值，即 1K, 4K, 16K, 64K。回想起來，這似乎是明顯的 quantization，而不是算術級數。」[Eric Hughes, 1994-08-29]
    - （Eudora 在 32K 時會窒息，因此在約 25K 時拆分訊息，以便在不進一步拆分的情況下留出評論空間。此類實際考慮可能很重要。）
  + Return Mail
    - 一個複雜的問題。可能沒有簡單的解決方案。
    + 方法：
      - 將加密訊息發布到 pool。發送者（提供了使用的 key）能夠通過 pools 和/或公開發布的性質 anonymous 地檢索。
      + Return envelopes，使用某種程序來確保 anonymity。由於軟件本質上永遠不安全（總是可以拆開），問題很複雜。安全性可以通過與返回路徑中的 remailers 安排對某些訊息做某些事情來獲得。
        - 發送者向 remailers 發送關於如何處理某些類型訊息的指令
        - 回覆的收件人無法推斷 identity，因為他無法訪問 remailers 擁有的指令。
        - 把這想像成 Alice 發送給 Bob 發送給 Charles....發送給 Zeke。Zeke 發送回覆給 Yancy，Yancy 有指令將其發送回 Xavier，依此類推回溯鏈條。只有當 Bob, Charles, ..., Yancy 串通時，才能推斷出反方向的映射。
        - 這些方案複雜嗎？是的。但許多其他 protocols 也是如此，例如將字體從屏幕傳輸到激光打印機
  + 訊息的 Reordering 至關重要
    + remailers 中的 latency 或 fanout
      + 比 "delay" 重要得多
        - 做一些計算！
        + 關於 "latency" 或 delay 的謠言不斷出現
          - X 的 "delay" 對於實現 reordering 既不必要也不充分（想一想）
      - 對於消除時間相關資訊，對於消除「區分標記」（"理想的 remailed 訊息沒有頭髮"）至關重要
  + Pay as you go, digital postage 的重要性
    + 標準市場問題
      - 市場是稀缺資源分配的方式
    - 減少 spamming, overloading, bombing
    - 擁堵定價
    - 改進的激勵
    + 反饋機制
      - 就像餐館很快看到影響一樣
    - 適用於除 remailers 之外的其他 crypto 用途
  + 雜項
    - 通過擁有自己的節點，進一步確保安全性（真的，所有其他節點的串通可能導致可追溯性，但這種串通代價高昂且會被揭露）
    + "public posting" 的想法非常有吸引力：最後一個節點在任何時候都不知道下一個節點是誰……他所知道的只是該節點的 public key
      + 那麼線路中的下一個節點如何獲得訊息，除了閱讀所有訊息之外？
        - 首先，通過 header 設置的某種順序對公開發布進行排序，安全性不會受到太大影響（例如，"Fred" 是某個長 P-K 的簡寫，因此收件人知道在 Fs 中查找……顯然他閱讀的不僅僅是 Fs）
    + 傳出訊息可以被 "broadcast"（發送到許多節點，通過字面廣播或公開發布，或通過隨機挑選許多節點）
      - 這種 "blackboard" 系統意味著不需要點對點通信
    + Timed-release 策略
      + 加密然後稍後釋放 key
        - "無害地"（如何？）
        - 通過 remailing 服務
        - DC-Net
        - 通過 escrow 服務或律師（但律師會因為向有爭議的數據釋放 key 而陷入困境嗎？）
        - 通過一系列此類釋放，key 可以被 "diffused"
        - 一些公司可能專門從事 timed-release，例如提供一個 P-K，private key 將在稍後某個時間釋放
      - 在 cryptoid 實體的生態系統中，這將增加自由度
      + 這減少了 retransmitters 的法律責任……他們可以準確地聲稱他們只是傳遞數據，他們無法知道 packets 的內容
        - 當然他們已經可以這樣聲稱，由於加密的性質
    + One-Shot Remailers
      - 「你可以從 mg5n+getid@andrew.cmu.edu 獲得一個 anonymous 地址。每次你請求一個 anon 地址，你會得到一個不同的。你可以獲得任意數量的地址。地址不會過期，所以也許這不是理想的 'one-shot' 系統，但它允許回覆而不將你連接到你的 'real name/address' 或你的任何其他 posts/nyms。」[Matthew Ghio, 1994-04-07]
### 8.6.14. Remailers 中需要的東西
  + return receipts
    - Rick Busdiecker 指出 "Return-Receipt-To: 字段的想法已經存在了一段時間，但語義從未確定。一些 mailer daemons 生成回覆，意味著位已交付。" [R.B., 1994-08-08]
  + 特殊處理指令
    - agents, daemons
    - 協商的程序
  + digital postage
    - 至關重要！
    - 解決許多問題，並激勵 remailers
  + padding
    + padding 到固定大小
      - padding 到 2 的固定冪將使平均訊息大小增加約三分之一
  - 大量的 remailers
  - 多個司法管轄區
  - 穩健性和一致性
  + 在安全硬件中運行
    - 無 logs
    - 操作員無監控
    - 擦除所有臨時檔案
  - 快速、流暢地實例化
  - 更好的 remailers 隨機化
### 8.6.15. Remailers 的雜項方面
  + "實際上需要多少個 remailer 節點？"
    - 我們努力獲得盡可能多的節點，將過程分配到許多司法管轄區和許多運營商。
    - 奇怪的是，單個 remailer（例如接收一百條訊息並發送一百條）可能發生與許多 remailers 一樣多的理論 diffusivity。我認為我們的直覺是，許多 remailers 提供更好的 diffusivity 和更好的隱藏。為什麼會這樣（如果是的話）需要比我目前看到的更仔細的思考。
    - 在元層面上，我們認為多個 remailers 減少了它們受到損害的機會（然而，這與 remailer 網絡的 diffusivity 沒有直接關係——重要，但沒有直接關係）。
    - （順便說一句，一種偷偷摸摸的想法是嘗試總是宣稱自己是 remailer 節點。如果訊息以某種方式追溯到自己的機器，可以聲稱：『是的，我是 remailer。』原則上，一個人可以是宇宙中唯一的 remailer，並且仍然具有足夠高的 diffusion 和 confusion。實際上，成為唯一的 remailer 將是非常危險的。）
    + Remailer 網絡中的 Diffusion 和 confusion
      + 考慮單個節點，一條訊息進入，兩條訊息離開；這本質上是最小的 "remailer op"
        - 從證明的角度來看，任何一條傳出訊息都可能是那條
        - 但兩者都無法被證明是
      - 現在想像這兩條訊息通過 10 個 remailers 發送……沒有增加額外的 confusion……為什麼？
      - 所以，有 10 條訊息進入 10 個 remailers 的鏈，如果 10 條離開……
      - N 個 remailers 的實際效果是確保其中一部分的妥協不會破壞整體安全性
  + "Remailers 如何處理地址錯誤的郵件？"
    - 取決於站點。一些運營商發回筆記（這本身引起關注），一些只是丟棄有缺陷的郵件。這是一個流動的領域。至少有一個 remailer (wimsey) 可以將錯誤訊息發布到訊息池——這個想法可以推廣以提供 "delivery receipts" 和其他反饋。
    - 類似 Chaum 的 Ideal mixes 據推測會丟棄格式不正確的郵件，儘管 agents 可能存在以預篩選郵件（當然不是強制性 agents，而是自願選擇的 agents）
    - 就像在許多領域一樣，不需要立法，只需要宣布政策，客戶選擇，以及 remailer 的 reputation。
    - 在自己的機器上穩健生成郵件的一個好理由，以盡量減少此類問題。
  + "NSA 能監控 remailers 嗎？他們有嗎？"
    + 當然他們_可以_以各種方式，要麼直接監控 Net 流量，要麼間接監控。他們是否_做_是未知的。
      - 有幾個謠言或偽造聲稱 NSA 經常在 penet remailer 將 anonymous IDs 鏈接到真實 IDs。
      + Cypherpunks remailers 如果使用得當，在關鍵方面更安全：
        - 很多
        - 不用於持久的、分配的 IDs
        - 支持 encryption：傳入和傳出訊息看起來完全不同
        - 支持 batching, padding 等
    - 運行良好的 remailers 將模糊/擴散傳入和傳出訊息之間的連接——remailer 的主要點！
  + 使用訊息池報告 remailer 錯誤
    - 訊息池如何用於 anonymous 地報告事情的一個好例子。
    - 「wimsey remailer 有一種巧妙的方法來 anonymous 地返回錯誤訊息。在發送給 wimsey 的訊息中指定一個對你有意義但不會識別你的 subject（如一組隨機字母）。此 subject 不會出現在 remailed 訊息中。然後訂閱 mailing list
       
       errors-request@extropia.wimsey.com
       
       通過發送帶有 Subject: subscribe 的訊息。你將收到一條 msg
       針對傳入訊息中檢測到的所有錯誤和所有被退回的訊息。」[anonymous, 93-08-23]
    - 這當然就像閱讀帶有只有你明白的神秘訊息的分類廣告。更重要的是，無法追溯到你。
  + 不同類型的 remailers 可能有作用
    - 支持 encryption 的，不支持的
    + 盡可能多地在非美國國家
      - 特別是對於*最後*一跳，以避免傳票問題
    - 一流的 remailers，remail 到*任何*地址
    + 僅 remail 到*其他 remailers* 的 remailers
      - 對於膽小的人，對於支持有限的人等有用。
    -
  + "Mail faking 應該作為 remailer 策略的一部分嗎？"
    - 「1. 如果你通過直接與 SMTP 對話來偽造郵件，進行傳出連接的站點的 IP 地址或域名將出現在 header 的某個 Received 字段中。」
       
       「2. 通過迂迴手段偽造郵件通常是不受歡迎的。這裡不需要採取後門方法——這在政治上是不好的，就像在 Internet 政治中一樣。」[Eric Hughes, 94-01-31]
    - 如果郵件真的可以一致且穩健地被偽造，那麼對 remailers 的需求就會減少，對吧？（實際上，仍然需要，因為 traffic analysis 可能會破壞任何 "Port 25" 偽造方案。）
    - 此外，這種策略不太可能隨著時間的推移而穩健，因為它依賴於利用短暫的缺陷和供應商的具體情況。這是一個糟糕的主意。
  + 讓 anonymous remailer 網絡廣泛部署的困難
    - 「棘手的部分是找到一種方法來保持 anonymity，而 Internet 上的大多數站點繼續仔細記錄流量，拒絕安裝新軟件（特別是 anon-positive 軟件），並且由對 identity 和懲罰持有簡單和過時觀點的人管理。」[Greg Broiles, 1994-08-08]
  + Remailer 挑戰：使鏈上的最後一條腿免受起訴
    + 策略 1：讓他們被宣佈為 common carriers，像電話公司或郵件遞送服務一樣
      + 例如，我們不會因為遞送非法包裹而起訴實際的包裹遞送員，甚至他們工作的公司
        - 假設承運人不知道內容
        - （我聽說有人聲稱只有與執法部門達成其他合作協議的承運人才能被視為 common carriers。）
    + 策略 2：訊息池
      + ftp 站點
        - 計劃讓使用者「訂閱」所有新訊息（因此，監控機構無法知道正在尋求哪些訊息，如果有的話）
        - 這繞過了關於 Usenet 上太多數量的投訴（文本訊息是其他流量的一小部分，特別是圖像，所以投訴只是潛在性之一）
    + 策略 3：Offshore remailers 作為最後一條腿
      - 可能由發送者設置，據推測他知道目的地
    - 大量的 "secondary remailers" 同意 remail 有限數量的……
  + "我們只是在玩弄 remailers 之類的東西嗎？"
    - 說這話讓我很痛苦，但是，是的，我們基本上只是在這裡玩耍！
    - Remailer 流量如此之低，padding 如此隨意，以至於在輸入和輸出之間建立相關性在密碼學上並不難做到。（用筆和紙類型的計算可能_看起來_很難，但對於 Fort 的 Crays 來說這將是兒戲。）
    - 即使對於任何特定訊息並非如此，維持一個持久的 ID——如 Pr0duct Cypher 所做的那樣，帶有 digital sigs——而不最終提供足夠的線索幾乎是不可能的。在這個時候。
    - 事情會變得更好。迫切需要更好和更詳細的 "cryptanalysis of remailer chains"。在那之前，我們確實只是在玩耍。（不過，玩耍可能是有用的。）
  + "不要給他們任何提示" 原則（對於 remailers）
    - 避免提供任何資訊
    - 不要說哪些節點是 sources，哪些是 sinks；讓攻擊者假設每個人都是 remailer，一個 source
    - 不要說密碼有多長
    - 不要說 tit-for-tat 錦標賽中有多少輪

## 8.7. Anonymous Posting to Usenet
### 8.7.1. Julf 的 penet 系統歷來是 anonymous 發布到 Usenet 的主要方式（由 L. Detweiler 在他的 "an12070/S. Boxx" personna 中使用，不少於一位傑出人物）。這尤其是在發布到「支持」群組或情緒困擾群組的情況下。例如，alt.sexual.abuse.recovery。
### 8.7.2. Cryptographically secure remailes 現在越來越多地被使用（擴展定律和多個司法管轄區表明未來將使用更多）。
### 8.7.3. finger remailer.help.all@chaos.bsu.edu 給出這些結果 [截至 1994-09-07——使用前獲取當前結果！]
  - 「Anonymous 發布到 usenet 可以通過發送 anonymous mail 到以下 mail-to-usenet gateways 之一來進行：
     
     group.name@demon.co.uk
     group.name@news.demon.co.uk
     group.name@bull.com
     group.name@cass.ma02.bull.com
     group.name@undergrad.math.uwaterloo.ca
     group.name@charm.magnus.acs.ohio-state.edu
     group.name@comlab.ox.ac.uk
     group.name@nic.funet.fi
     group.name@cs.dal.ca
     group.name@ug.cs.dal.ca
     group.name@paris.ics.uci.edu (移除 headers)
     group.name.usenet@decwrl.dec.com (保留所有 headers)」
     

## 8.8. Anonymous Message Pools, Newsgroups, etc.
### 8.8.1. "為什麼有些人使用訊息池？"
  - 提供 untracable 通信
  - 訊息
  - 秘密
  - 交易
  + Pr0duct Cypher 是一個主要通過 anonymous pools 進行通信（針對給他的訊息）的人的好例子。最近有人問到這個問題，並評論道：
    - 「Pr0duct Cypher 選擇不將他或她的 "real life" identity 與用於簽署他或她編寫的軟件（PGP Tools, Magic Money, ?）的 'nym 聯繫起來。這是一個完全可以理解的情緒，鑑於 NSA 中的壞蘋果願意遠遠超出法律騷擾的範圍，並對具有高公眾知名度的人發出死亡威脅（參見關於 NSA 特工威脅要在停車場碾壓 RSA 的 Jim Bidzos 的線程）。」[Richard Johnson, alt.security.pgp, 1994-07-02]
### 8.8.2. alt.anonymous.messages 就是這樣一個 pool 群組
  - 儘管它主要用於測試訊息，討論 anonymity（儘管有更好的群組）等。
### 8.8.3. "會有真正的 anonymous newsgroups 嗎？"
  - 一個想法：newgroup 一個受控群組，其中只接受沒有 headers 和其他標識符的訊息。"Moderator"——可能是一個程式——只有在確保這一點後才會發布訊息。（可能是一個有趣的實驗。）
  + alt.anonymous.messages 由 Rick Busdiecker 在 1994-08 newgrouped。
    - 可以預見，早期的使用是由那些偶然發現該群組並將其歸咎於他們所希望的任何東西的人進行的。

## 8.9. Legal Issues with Remailers
### 8.9.1. Remailers 的法律地位是什麼？
  - 目前沒有法律反對它。
  - 沒有法律規定人們必須在訊息、電話（公用電話仍然合法）等上加上回信地址。
  - 與不必出示身份有關的法律（"flier" 案例，傳單分發者不必出示 ID）似乎適用於這種通信形式。
  + 然而，remailers 可能會受到抨擊：
    + Sysops, MIT 案例
      - 如果案件的判決是 sysop 創建有利於犯罪盜版的群組本身就是犯罪……這可能會使所有參與 remailers 的人都應受譴責，這對 remailers 來說可能是嚴重的
### 8.9.2. "Remailer logs 可以被傳喚嗎？"
  - 指望它發生，也許很快。FBI 一直在傳喚 Netcom 客戶（Lewis De Payne）的電子郵件檔案，可能是因為他們認為電子郵件會引導他們找到 uber-hacker Kevin Mitnick 的位置。如果當事人使用了 remailers，我相當肯定我們會看到對 remailer logs 的類似傳票。
  - 據我所知，remailers 沒有豁免權！
  + 不過，解決方案很明顯：
    - 使用許多 remailers，使通過鏈條反向傳喚變得非常費力、非常昂貴，並且很可能失敗（如果甚至有一方不合作，或者在法院管轄範圍之外等）
    - offshore, multi-jurisdictional remailers（由使用者選擇）
    - 不保留 remailer logs……銷毀它們（目前沒有法律規定任何人必須保留電子郵件記錄！這可能會改變……）
    - "forward secrecy"，類似 Diffie-Hellman forward secrecy
### 8.9.3. Remailers 將如何受到騷擾、攻擊和挑戰？
### 8.9.4. "可以對 remailer 運營商施加壓力以揭示 traffic logs 從而允許追蹤訊息嗎？"
  + 對於有人工操作且有 logs 的系統，當然。這就是為什麼我們希望在 remailers 中有幾樣東西：
    * 無訊息 logs
    * 許多 remailers
    * 多個法律司法管轄區，例如 offshore remailers（越多越好）
    * 完美執行指令的硬件實現（Chaum 的 digital mix）
### 8.9.5. 呼籲限制 anonymity
  + 孩子和網絡將導致許多人呼籲限制 nets，限制 anonymity 等。
    - 「但在這種令人興奮的現象背後有一個陰暗面，計算機新手很少理解這一點。因為它們
       提供與他人的即時接觸，並為參與者提供相當大的 anonymity，
       這些服務使人們——
       特別是懂電腦的孩子——可能會發現自己處於
       不愉快的、性露骨的社交場合.... 我逐漸
       開始採納這種觀點，這將在許多在線
       使用者中引起爭議，即 nicknames 和其他形式的 anonymity 的使用
       必須被消除或嚴格限制，以迫使在線人員
       至少對他們的言行承擔與
       現實社交遭遇中存在的相同的 accountability。」[Walter S. Mossberg,
       Wall Street Journal, 6/30/94, 由 Brad Dolan 提供]
    - Eli Brandt 對此提出了一個很好的回應：「對此的簡短回應：你想讓你孩子的名字、家庭住址和電話號碼對全世界所有那些潛伏的戀童癖者可用嗎？負責任的父母鼓勵他們的孩子使用 remailers。」
  - Supreme Court 說傳單分發者的身份不需要披露，pseudonyms 總體上有著悠久而崇高的傳統
  - BBS 運營商擁有 First Amendment 保護（例如，註冊要求將被扔掉，就像試圖註冊報紙一樣）
### 8.9.6. Remailers 和司法管轄區的選擇
  - Remailed 訊息的預期目標和主題材料很可能會影響所使用的 remailers 集合，特別是對於非常重要的「最後一個 remailer」（注意：永遠不需要告訴 remailers 他們是第一個、最後一個還是其他，但最後一個 remailer 實際上可能能夠分辨出他是最後一個……如果訊息對收件人是 plaintext，沒有嵌入額外的 remailer 命令，例如。）
  - 涉及兒童色情的訊息可能有一個位於像 Denmark 這樣兒童色情法律限制較少的州的 remailer 站點。批評 Islam 的訊息最好不要通過 Teheran 的最終 remailer 發送。Eric Hughes 稱之為 "regulatory arbitrage"，在不同程度上這已經是常見做法。
  - 當然，發送者選擇 remailer chain，所以這些常識概念可能不會被遵循。沒有什麼是完美的，習俗會演變。我可以想像開發選擇客戶的方案——remailer 可能不接受某些濫用者作為客戶，基於 digital pseudonyms < hairy）。
### 8.9.7. 限制使用 remailers 和 anonymous 系統的可能法律步驟
  - 讓 remailer 對內容負責，即無 common carrier 地位
  - 在各種 "anti-hacking" 法律中插入條款，將 anonymous 帖子定為犯罪
### 8.9.8. Crypto 和 remailers 可用於保護團體免受 "deep pockets" 訴訟
  - 產品（特別是軟件）可以「按原樣」出售，或帶有由 escrow 服務支持的合同（代碼保存在 escrow 存儲庫中，或錢保存在那裡以支持承諾）
  + 司法管轄區，法律和稅務，不能做 "reach backs"，使團體面臨比他們同意的更多的風險
    - 正如現實世界中的公司經常發生的那樣，這些公司因各種目的（石棉等）被徵稅和罰款
  - （對於那些想到這一點就恐慌的人來說，謹慎的補救措施是與正確的實體安排合同……可能為更少的產品支付更多費用。）
### 8.9.9. Anonymous remailers 可以用來誘捕人，或為調查收集資訊嗎？
  - 首先，目前的 remailers 如此之少，這不太可能。Julf 似乎不是 narc 類型，他位於 Finland。Cypherpunks remailers 目前主要由像我們這樣的人經營。
  - 然而，narcs 和 "red squads" 過去曾使用過此類 stings 和陷阱。期待 Mr. Policeman 最壞的情況。現在邪惡的 hackers 被認定為危險，期待朝這個方向發展。"Cryps" 顯然是 "crack" 交易商。
  - 但使用 CP remailers 支持的 encryption（Julf 的不支持），使得這基本上沒有實際意義。

## 8.10. Cryptanalysis of Remailer Networks
### 8.10.1. 需要對 Mixes 和 Remailers 進行更詳細的分析
  + "Remailer 系統是否已被充分 cryptanalyzed？"
    - 在我看來，沒有。很少進行計算，主要只是關於 remailer 節點產生了多少 "confusion" 的一些估計。
    - 但認為大量的複雜和混亂構成了一個強大的 crypto 系統是一個基本的錯誤……有點像認為 Enigma rotor machine 構成了一個好的 cipher 系統，按照今天的標準，僅僅因為通過 rotor 系統的路徑有數百萬種組合是可能的。並非如此。
  + 推導 Traffic 中的模式和推導 Nyms
    - Mathematical cryptology 的主要教訓是，看似隨機的事物實際上可以顯示出結構。這就是 cryptanalysis 的全部內容。
    - 同樣的情況適用於 digital mixes、電話網絡等中的「看似隨機」的訊息 traffic。"Cryptanalysis of remailers" 當然是可能的，取決於底層模型。（實際上，它總是可能的，只是可能不會產生任何結果，就像 ciphers 的 cryptanalysis 一樣。）
    + 關於 remailer cryptanalysis 中的時間相關性
      - 想像 Alice 和 Bob 通過 remailers 交流……一個觀察者，無法通過 remailers 跟蹤特定訊息，仍然可以注意到這兩個人發送和接收的訊息之間的成對相關性
      + 就像事件之間的時間相關性，即使中間路徑或事件是混亂的
        - 例如，如果在每艘潛艇離開 Holy Loch 的幾個小時內都有一個電話打到 Moscow，人們可能會得出關於誰是俄羅斯間諜的某些結論，不管是否知道中間路徑
        - 或者，離家更近一點，將一家銀行的提款與另一家銀行的存款聯繫起來，即使中間轉賬是混亂的
      + 僅僅因為它看起來 "random" 並不意味著它是
        - Scott Collins 推測 "dynamic Markov compressor" 可以識別或揭示 remailer 使用中的非隨機性
  - Remailers 的 Cryptanalysis 嚴重缺乏。關於 remailer 改進的帖子中有很大一部分對需要更多流量、更長延遲等提出了揮手示意般的論點。（我不是在指責，因為我也發表同樣的非正式、定性評論。需要的是對 remailer 安全性的嚴格分析。）
  - 我們真的沒有任何關於整體安全性的良好估計，作為流通訊息數量、latency（重新發送前存儲的訊息數量）、remailer hops 數量等的函數。這不是密碼學上「令人興奮」的工作，但仍然需要。學術界對 digital mixes 或 remailers 的關注不多，可能是因為 David Chaum 1981 年關於 "Untraceable E-Mail" 的論文涵蓋了大部分理論上有趣的材料。那，以及缺乏商業產品或廣泛使用。
  + 時間相關性可能會揭示個別訊息所缺乏的模式。也就是說，Alice 和 Bob 之間的反覆通信，即使是通過 remailers 進行的，即使內置了時間延遲/停留時間，也可能揭示發送/接收訊息中的非隨機相關性。
    - Scott Collins 推測，應用於 traffic 的 dynamic Markov compressor 將揭示此類相關性。（將此類測試應用於 digital cash 和其他此類系統將是有用的。）
    - 另一個經常被忽視的弱點是許多人發送測試訊息給自己，Phil Karn 指出了這一點：「人們經常讓自己被抓住的另一種方式是，他們不可避免地在有問題的偽造訊息之前發送測試訊息給自己。這在發送系統的 sendmail logs 中顯示得很清楚。如果你不信任鏈上的最後一台機器，這也是 remailer chains 需要考慮的一點。」[P.K., 1994-09-06]
  + 需要什麼：
    - 對某些術語達成一致（這不需要共識，只需要一篇寫得清楚的論文來事實上建立術語）
    - 一個公式，將 untraceability 的程度與進入 remailers 的主要因素聯繫起來：packet 大小和 quantization, latency（訊息數量）, remailer 政策, timing 等。
    - 此外，分析如何發起蓄意探測或攻擊以推斷 remailer 模式（例如，Fred 總是 remails 給 Josh 和 Suzy，很少給 Zeke）。
  - 我認為這種組合分析對於某人來說將是一篇不錯的小專著。
### 8.10.2. 一個非常需要的東西。Hal Finney 已經發布了一些計算（大約 1994-08-08），但迫切需要更多的工作。
### 8.10.3. 特別是，我們應該懷疑「跟蹤流量看起來肯定很複雜」這類揮手示意般的分析。人們認為通過添加「混亂」的技巧，如 MIRVing 訊息，安全性會增加。也許是，也許不是。但在可以自信地相信聲明之前，需要正式分析。
### 8.10.4. Remailers 和 entropy
  - mix 或 remailer 中進行的 "mixing" 的度量是什麼？
  - 關於 entropy 和 reordering 的揮手示意可能不太有用。
  + 回到 Shannon 的 entropy 概念，即衡量不確定性的程度……
    + 試圖「猜測」或「預測」離開一個節點的訊息將在何處退出系統
      - 沒有清晰的入口和出口點增加了一些難度，有點類似於擁有未知長度的密碼（攻擊者不能只是嘗試所有 10 個字符的密碼，因為他不知道長度）
      - 每個節點都是 remailer，沒有明確識別的 sources 和 sinks 的優點
  + 這種可預測性可能取決於 Alice 和 Bob 之間發送的_一系列_訊息……如何？
    - 似乎可能與 Persi Diaconis 關於 "perfect shuffles" 的工作有關（一個看起來很容易的問題，但直到最近才解決……應該讓我們感到安慰，我們無法解決這個問題的真正核心並不足為奇
### 8.10.5. Scott Collins 認為 remailer 網絡可以像分析 pseudorandom number generators 一樣進行 cryptanalyzed，例如，使用 dynamic Markov compressors (DNCs)。（我更懷疑：如果每個 remailer 使用 information-theoretically secure RNG 來 reorder 訊息，並且如果所有訊息大小相同且（當然）使用 information-theoretically secure (OTP) ciphers 加密，那麼在我看來，remailing 本身將是 information-theoretically secure。）

## 8.11. Dining Cryptographers
### 8.11.1. 這實際上是 "ideal digital mix"，從 Chaum 最初的硬件 mix 形式更新為純軟件形式。
### 8.11.2. David Chaum 1988 年在 Journal of Crypology (Vol 1, No 1) 上的論文概述了一種僅使用軟件（不需要 tamper-resistant 模塊）進行完全 untraceable 通信的方法
  - 環中的參與者（因此是 "dining cryptographers"）
  - Chaum 想像 3 位 cryptographers 正在吃晚飯，服務員通知他們晚餐已經付過錢了，也許是 NSA，也許是他們中的一個……他們希望確定這是哪一個，而不透露是誰付的錢！
  - 每個人拋硬幣（H 或 T）並展示給他左邊的鄰居
  + 每個人報告他看到的是 "same" 還是 "different"
    - 注意，有 2 個參與者，他們都已經知道對方的硬幣（都在左邊！）
  - 然而，希望發送訊息的人，例如 Chaum 的例子「我付了晚餐錢」，會說與他看到的相反的話
  + 對此的一些分析（從其中一位 cryptographers 的角度分析）表明，3 位 cryptographers 將知道他們中的一個付了錢（如果這個 protocol 被忠實執行），但 identity 無法被「定位」
    - 需要圖表……
  + 這可以推廣……
    + 更長的訊息
      - 使用多輪 protocol
    + 比拋硬幣更快
      - 每個參與者和他的左邊夥伴共享一個「預先拋出的」硬幣列表，例如存儲在 CD-ROM 或其他東西上的真正隨機位（放射性衰變、噪聲等）
      - 因此他們可以像讀取磁盤一樣快地「拋硬幣」
    + 同時訊息（collision）
      - 使用 back-off 和重試 protocols（像 Ethernet 使用的那樣）
    + 參與者的 collusion
      - 一個有趣的問題……記住參與者不限於簡單的環 topology
      - 可以形成各種 subgraphs
      - 擔心 collusion 的參與者可以選擇一個包含他懷疑會 collude 的人的 subgraph（一個棘手的問題）
    + 接收者的 anonymity
      - 可以使用 P-K 加密訊息到某個 P-K，然後 "broadcast" 它並強迫每個參與者嘗試解密它（只有 anonymous 收件人實際上會成功）
  - Chaum 完整的 1988 年 "Journal of Cryptology" 文章可在 Cypherpunks 檔案站點 ftp.soda.csua.edu 的 /pub/cypherpunks 中找到
### 8.11.3. "DC-Net" 意味著什麼
  - 一個通信參與者的系統（圖、子圖等），他們彼此之間不需要認識，可以傳達資訊，使得發送者和接收者都不為人知
  + 無條件的發送者 untraceability
    - 廣播者的 anonymity 可以是 information-theoretically secure，即真正無法破解，不需要關於 public key 系統、factoring 難度等的假設。
  + 接收者 untraceability 取決於 public-key protocols，因此 traceability 是 computationally-dependent
    - 但這被認為是安全的，當然
  + bandwidth 可以通過幾種方式增加
    - 共享 keys
    - 通過積累訊息進行塊傳輸
    - 訊息、subgraphs 等的層次結構

## 8.12. Future Remailers
### 8.12.1. "Next Generation Remailer 需要哪些特性？"
  + 一些目標
    - 總體而言，更接近 Chaum 1981 年關於 "Untraceable E-Mail" 的論文中概述的目標
    - Anonymity
    - Digital Postage, pay as you go, 市場定價
    - Traffic Analysis 被挫敗
  + Bulletproof 站點：
    - 擁有 offshore（美國境外）站點很好，但擁有能夠抵抗來自大學和公司站點管理員壓力的站點具有更大的實際後果。像 Netcom, Portal, 和 Panix 這樣的商業提供商，如果壓力增加，不能指望他們站出來戰鬥（這只是我的猜測，不是對他們骨幹的誹謗，無論是有機的還是 Internet）。
    - 在許多非美國國家定位 remailers 是一個好主意。就像洗錢一樣，許多國家意味著許多司法管轄區，以及一個國家控制的幾乎不可能。
  + Digital Postage, 或 Pay-as-you-Go 服務：
    - 服務的一些費用。就像電話服務、modem 時間、真正的郵資等。（但與高速公路駕駛不同，後者的使用在很大程度上得到了補貼。）
    - 這將減少 spamming，將激勵 remailer 服務更好地維護他們的系統，並將
    - 費率將按通常的方式由市場過程設定。「流量能承受什麼。」折扣、受青睞的客戶、回扣、優惠券等。那些不想收費的人不必收費（他們將不得不處理問題）。
  + 世代
    - 第一代——今天的 Remailer：
    - 第二代——不久的將來（約 1995 年）
    - 第三代-
    - 第四代——
### 8.12.2. Remailing 作為郵件過濾的副作用
  - Dean Tribble 提議……
  - 「聽起來計劃是提供一個方便的郵件過濾工具，它提供 remailer 能力作為副作用！傳播 remailers 的好方法！」[Hal Finney, 93-01-03]
### 8.12.3. "有沒有 remailers 為你提供一個 anonymous 帳戶，其他人可以向其發送訊息，然後以 PGP-encrypted 形式轉發給你？" [Mikolaj Habryn, 94-04]
  - 「是的，但它還沒有真正運行。給我幾個月時間，直到我為它獲得計算機 + netlink。（雖然它正在運行以進行測試，所以如果你想測試它，請給我發郵件，但它不是真正運行，所以不要*使用*它。）」[Sameer Parekh, 94-04-03]
### 8.12.4. "Remailer Alliances"
  + "Remailer's Guild"
    - 使不可靠有成本（驅逐），穩健、質量、可靠性等有收益（增加業務）
    - pings, 測試, 合作 remailing
    - 分散流量以降低攻擊的有效性
  - 執行 protocols
  - 例如，在最後一跳共享流量，以減少對任何單個 remailer 的攻擊

## 8.13. Loose Ends
### 8.13.1. Digital 間諜活動
  + 間諜網絡可以安全、untraceably、undetectably 運行
    - anonymous 聯繫人, pseudonyms
    - digital dead drops，全部以電子方式完成……沒有機會被接走，被揭露為 "illegal"（沒有外交掩護來拯救他的間諜）並被槍殺
  + 通信中的自由度如此之大，以至於控制所有這些基本上是不可能的
    - Teledesic/Iridium/etc. 衛星將進一步增加這種能力
  + 除非 crypto 被阻止——而且相對迅速和無情地——否則這裡描述的情況是不可阻擋的
    - 有些人稱之為 "espionage"，其他人只會稱之為自由通信
    - （保守公司或商業秘密的一些重要教訓……基本上，你不能。）
### 8.13.2. Remailers 可能需要一些 "fuzziness"
  + 例如，如果 remailer 有嚴格的政策積累 N 條訊息，然後 reordering 並 remailing 它們，攻擊者可以發送 N - 1 條訊息進去，並知道離開的 N 條訊息中哪一條是他們想要跟蹤的訊息；一些不確定性在這裡有幫助
    - 這種少量的 uncertainty 或 scatter 如何有幫助的數學是需要詳細分析的東西
  - 就像 keylength 問題一樣，留下一點 uncertainty 可能會有幫助
### 8.13.3. 試圖混淆竊聽者，通過添加他們可能會注意到的關鍵字
  + "remailer@csua.berkeley.edu" remailer 現在添加實際段落，例如最近的這個例子：
    - 「我修好了 SKS。它帶有一個瞄準鏡和一個俄羅斯夜視鏡。它是殺手級的。我的朋友認識一個非常好的槍匠，他有一個機械車間，知道如何將東西改裝成自動的。」
       
  - 這個策略有多有效是有爭議的
### 8.13.4. 對 anonymous 系統的限制
  - Anonymous AIDS 測試。自我測試套件已經在 FDA 審查了 5 年，但諮詢倡導者推遲了發布，理由是有些人會反應不佳，甚至可能在得到陽性測試結果後自殺……他們希望現有系統佔上風。（我提到這一點是為了表明 anonymous 系統有時會因意識形態原因而遭到反對。）
