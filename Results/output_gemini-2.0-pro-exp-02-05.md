# 01-703-1335
## Task1: Clinical Review Results
**1. 症例サマリー:**

**患者ID: 01-703-1335**

*   2013年12月28日 (Day -79): スクリーニング検査実施。アルブミン、ALP、ALT、AST、ビリルビン、BUN、カルシウム、コレステロール、CK、クレアチニン、尿酸値は正常範囲内。
*   2014年02月21日 (Day -24): 非予定の検査実施。CK (209 U/L) が基準範囲上限を超過。
*   2014年03月15日 (Day -2): スクリーニング検査2実施。血圧、脈拍は正常範囲内。
*   2014年03月17日 (Day 1): ベースライン。ADAS-Cog(11)スコアは57点、NPI-X(9)合計スコアは24点、DAD合計スコアは4%。キサノメリン54mg投与開始。
*   2014年03月30日 (Day 14): Ambulatory ECG 装着。血圧低下（臥位60mmHg、立位60mmHg）、脈拍上昇（臥位88/min、立位96/min）を認める。
*   2014年03月31日 (Day 15): 2週目来院。血圧上昇（臥位88mmHg、立位90mmHg）、脈拍正常化（臥位72/min、立位70/min）を認める。CK (219 U/L) が基準範囲上限を超過。NPI-X(9)合計スコアは10点。同日、多発性硬化症の再発による第2度房室ブロックの有害事象発現。
*   2014年04月01日 (Day 16): キサノメリン81mgへ増量。
*   2014年04月13日 (Day 28): 4週目来院。血圧低下（臥位80mmHg、立位70mmHg）、脈拍上昇（臥位80/min、立位90/min）を認める。CK (134 U/L) は正常範囲内に回復。NPI-X(9)合計スコアは24点。
*   2014年04月15日 (Day 30): Ambulatory ECG 取り外し。血圧、脈拍は正常範囲内。
*   2014年05月01日 (Day 46): 第2度房室ブロックの有害事象が回復/寛解。
*   2014年05月07日 (Day 52): キサノメリン81mg投与終了。
*   2014年05月24日 (Day 69): 6週目来院。血圧、脈拍は正常範囲内。ADAS-Cog(11)スコアは61.5点、NPI-X(9)合計スコアは10点、CIBIC+スコアは5点（最小悪化）。プロトコル違反のため中止。

**2. クエリ:**

**患者ID: 01-703-1335**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE", AE.AEDECOD = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
    *   **医療機関への問い合わせ文面:** 報告された有害事象は「多発性硬化症の再発」と「第2度房室ブロック」ですが、多発性硬化症は除外基準に該当します。本症例の診断と、除外基準12「重篤な神経疾患の診断」への該当について、詳細な情報を確認させてください。
    *   **判断理由:** 患者背景の確認は、安全性評価の基本であり、除外基準抵触の可能性は、臨床試験の信頼性を損なう可能性があるため。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "PROTOCOL VIOLATION"
    *   **医療機関への問い合わせ文面:** プロトコル違反の内容について詳細な情報を確認させてください。
    *   **判断理由:** プロトコル違反の内容によっては、症例の評価除外が必要となる可能性があるため。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "CK", LB.LBORRES = "209", LB.LBDY = -24, LB.VISIT = "UNSCHEDULED 1.1"
    *   **医療機関への問い合わせ文面:** 2014年02月21日(Day -24)の非予定検査でCK値が基準範囲上限を超過していますが、この検査実施理由と臨床的意義について確認させてください。
    *   **判断理由:** CK値の上昇は、有害事象や基礎疾患との関連が考えられるため。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** AE.AESTDTC = "2014-04-01", AE.AEENDTC = "2014-05-01", AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE"
    *   **医療機関への問い合わせ文面:** 有害事象「多発性硬化症の再発」の開始日(2014-04-01)と終了日(2014-05-01)が、AEDECOD="ATRIOVENTRICULAR BLOCK SECOND DEGREE"の有害事象の開始日(2014-03-15)と終了日(2014-03-30)と矛盾しているように見えます。どちらの有害事象が「MULTIPLE SCLEROSIS RELAPSE」に該当するか、確認させてください。
    *   **判断理由:** 有害事象の正確な記録は、安全性評価に必須であるため。
*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** AE.AESTDTC = "2014-03-15", AE.AEENDTC = "2014-03-30", AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
    *   **医療機関への問い合わせ文面:** 有害事象「第2度房室ブロック」の開始日(2014-03-15)が、SV.SVSTDTC="2014-03-30"のAmbulatory ECG装着日より前になっています。正確な開始日を確認させてください。
    *   **判断理由:** 有害事象の正確な記録は、安全性評価に必須であるため。
*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD = "CIBIC", QS.QSORRES = "MINIMAL WORSENING", QS.QSDTC = "2014-05-24"
    *   **医療機関への問い合わせ文面:** CIBIC+の評価が「最小悪化」となっていますが、その根拠となった具体的な変化について、詳細な情報を確認させてください。
    *   **判断理由:** CIBIC+は主要評価項目の一つであり、評価の根拠を確認することは重要であるため。
*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD = "ACTOT", QS.QSSTRESN = 61.5, QS.QSDTC = "2014-05-24"
    *   **医療機関への問い合わせ文面:** ADAS-Cog(11)の合計スコアが、ベースライン(57点)から悪化(61.5点)していますが、その内訳と、悪化の要因について、詳細な情報を確認させてください。
    *   **判断理由:** ADAS-Cog(11)は主要評価項目の一つであり、スコア悪化の要因を確認することは重要であるため。
*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD = "NPTOT", QS.QSSTRESN = 10 (2014-03-31), 24 (2014-04-13), 10 (2014-05-24)
    *   **医療機関への問い合わせ文面:** NPI-X(9)合計スコアが、ベースライン(24点)から変動していますが、その内訳と、変動の要因について、詳細な情報を確認させてください。
    *   **判断理由:** NPI-X(9)は副次評価項目の一つであり、スコア変動の要因を確認することは重要であるため。
*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD = "DAITM40", QS.QSORRES = "Y" (2014-03-17), "N" (2014-05-24)
    *   **医療機関への問い合わせ文面:** DADの「一人で安全に家にいられる」の評価が、ベースライン(「はい」)から最終評価(「いいえ」)へ変化していますが、その理由について詳細な情報を確認させてください。
    *   **判断理由:** DADは副次評価項目の一つであり、評価変化の理由を確認することは重要であるため。

## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: AE, LB, QS, SUPPAE, SUPPLB

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** AE.AESTDTC = 2014-04-01, AE.AEENDTC = 2014-05-01, AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE"
    *   **矛盾の内容:** AE.AESTDTC (2014-04-01) が AE.AEENDTC (2014-05-01) より後になっている。また、有害事象名が "MULTIPLE SCLEROSIS RELAPSE" であるが、プロトコルでは多発性硬化症の既往は除外基準(EXCL12)となっている。
    *   **問題点の原因（推測）:** AE.AESTDTC, AE.AEENDTCの日付入力ミス、または、患者選択基準の誤り。
    *   **対応策（提案）:** AE.AESTDTC, AE.AEENDTC の日付を再確認する。患者が除外基準に抵触していないか確認する。

*   **問題No.2:**
    *   **変数名と値:** AE.AESTDTC = 2014-03-15, AE.AEENDTC = 2014-03-30, AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
    *   **矛盾の内容:** AE.AESTDTC (2014-03-15) が AE.AEDTC (2014-03-31) より前になっている。また、有害事象名が "ATRIOVENTRICULAR BLOCK SECOND DEGREE" であるが、プロトコルでは第二度房室ブロックの既往は除外基準(EXCL16)となっている。
    *   **問題点の原因（推測）:** AE.AESTDTC, AE.AEDTCの日付入力ミス、または、患者選択基準の誤り。
    *   **対応策（提案）:** AE.AESTDTC, AE.AEDTC の日付を再確認する。患者が除外基準に抵触していないか確認する。

*   **問題No.3:**
    *   **変数名と値:** LB.LBTESTCD = "CK", LB.VISITNUM = 1.1, LB.LBNRIND = "HIGH"
    *   **矛盾の内容:** 非定例外来(UNSCHEDULED 1.1)でCK値が基準範囲を超えている(HIGH)。
    *   **問題点の原因（推測）:** 有害事象の発生、または、その他の医学的な理由による検査値異常。
    *   **対応策（提案）:** 基準範囲を超えた理由を確認する。有害事象として報告すべきか検討する。

*   **問題No.4:**
    *   **変数名と値:** QS.QSTESTCD = "ACTOT", QS.VISITNUM = 7, QS.QSSTRESN = 61.5517241379
    *   **矛盾の内容:** QS.QSSTRESN (ADAS-COG(11) Subscore) が小数点以下6桁まで入力されている。Define.xmlでは、QS.QSSTRESNのデータタイプは整数(integer)と定義されている。
    *   **問題点の原因（推測）:** データ入力/転記ミス、または、Define.xmlの定義の誤り。
    *   **対応策（提案）:** Define.xmlの修正候補: QS.QSSTRESNのデータタイプをfloatに変更し、有効桁数を定義する。

*   **問題No.5:**
    *   **変数名と値:** SUPPAE.QNAM = "AETRTEM", SUPPAE.QVAL = "N"
    *   **矛盾の内容:** SUPPAE.QVAL = "N" (治験薬との関連性なし) となっているが、AE.AEREL = "NONE" (因果関係なし) となっている。
    *   **問題点の原因（推測）:** SUPPAE.QVAL または AE.AEREL の入力/評価ミス。
    *   **対応策（提案）:** AETRTEM, AERELの定義と、報告された有害事象と治験薬との関連性を再確認し、矛盾がないように修正する。

*   **問題No.6:**
    *   **変数名と値:** SUPPLB.QNAM = "LBTMSHI", SUPPLB.QVAL
    *   **矛盾の内容:** SUPPLB.QVALの値が、Define.xmlで定義されている表示形式(12.1)と一致しないものがある。
    *   **問題点の原因（推測）:** SUPPLB.QVALの計算/転記ミス、または、Define.xmlの定義の誤り。
    *   **対応策（提案）:** Define.xmlの修正候補: SUPPLB.QVALの表示形式が正しいか確認し、必要に応じて修正する。

**クエリ:**

*   **患者ID:** 01-703-1335
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2014-04-01, AE.AEENDTC = 2014-05-01, AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE"
        *   **医療機関への問い合わせ文面:** AE.AESTDTCが2014-04-01、AE.AEENDTCが2014-05-01と報告されていますが、AESTDTCがAEENDTCよりも後の日付になっています。正しい日付を教えてください。また、有害事象名が "MULTIPLE SCLEROSIS RELAPSE" と報告されていますが、多発性硬化症の既往は除外基準(プロトコル EXCL12)に該当します。患者選択基準を満たしているか、再度ご確認ください。
        *   **判断理由:** 有害事象の発現日と終了日の矛盾、および、除外基準に抵触する可能性のある有害事象の報告は、患者の安全性とデータの信頼性に影響するため。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2014-03-15, AE.AEENDTC = 2014-03-30, AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
        *   **医療機関への問い合わせ文面:** AE.AESTDTCが2014-03-15、AE.AEENDTCが2014-03-30と報告されていますが、AE.AEDTCは2014-03-31と報告されています。正しい日付を教えてください。また、有害事象名が "ATRIOVENTRICULAR BLOCK SECOND DEGREE" と報告されていますが、第二度房室ブロックの既往は除外基準(プロトコル EXCL16)に該当します。患者選択基準を満たしているか、再度ご確認ください。
        *   **判断理由:** 有害事象の発現日と収集日の矛盾、および、除外基準に抵触する可能性のある有害事象の報告は、患者の安全性とデータの信頼性に影響するため。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "CK", LB.VISITNUM = 1.1, LB.LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 非定例外来(Visit 1.1)でCK値が基準範囲を超えていますが、その理由を教えてください。有害事象として報告すべきでしょうか？
        *   **判断理由:** 基準範囲外の値は、有害事象の可能性を示唆するため。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** SUPPAE.QNAM = "AETRTEM", SUPPAE.QVAL = "N", AE.AEREL = "NONE"
        *   **医療機関への問い合わせ文面:** 有害事象 "MULTIPLE SCLEROSIS RELAPSE" および "ATRIOVENTRICULAR BLOCK SECOND DEGREE" について、SUPPAE.QVAL (AETRTEM) が "N"、AE.AEREL が "NONE" と報告されています。これらの有害事象と治験薬との関連性について、再評価をお願いします。
        *   **判断理由:** 有害事象と治験薬との関連性は、安全性評価の重要な要素であり、矛盾がある場合は確認が必要なため。

## Task3: Protocol Deviation Review Results
**1. プロトコル逸脱の検出**

**患者ID: 01-703-1335**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXENDTC: 2014-05-07, DS.DSTERM: PROTOCOL VIOLATION, DS.DSDTC: 2014-05-24
    *   **逸脱内容:** 被験者はプロトコルで規定された投与期間（Week6）を超えて治験薬を投与された。DSドメインのDSTERMおよびDSDTCより、プロトコル逸脱により試験を中止していることが確認できる。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design (Page 8)
    *   **判断理由:** プロトコルでは、治験薬の投与期間はWeek6までと規定されている。しかし、EXドメインのEXENDTCは2014-05-07であり、Week6を超えている。さらに、DSドメインのDSTERMが"PROTOCOL VIOLATION"、DSDTCが2014-05-24であり、プロトコル逸脱により試験を中止していることがわかる。

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM: MULTIPLE SCLEROSIS RELAPSE, AE.AESEV: MILD, AE.AESTDTC: 2014-04-01, AE.AEENDTC: 2014-05-01
    *   **逸脱内容:** 被験者は多発性硬化症の再発を発症している。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria [12] (Page 13)
    *   **判断理由:** プロトコルでは、多発性硬化症の既往歴のある患者は除外基準に該当する。AEドメインのAETERMが"MULTIPLE SCLEROSIS RELAPSE"であり、多発性硬化症の再発が報告されているため、除外基準違反と判断できる。

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM: ATRIOVENTRICULAR BLOCK SECOND DEGREE, AE.AESEV: MILD, AE.AESTDTC: 2014-03-15
    *   **逸脱内容:** 被験者は第2度房室ブロックを発症している。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria [16] (Page 13)
    *   **判断理由:** プロトコルでは、スクリーニング時のECGで第2度房室ブロックが認められる患者は除外基準に該当する。AEドメインのAETERMが"ATRIOVENTRICULAR BLOCK SECOND DEGREE"であり、第2度房室ブロックが報告されているため、除外基準違反と判断できる。

*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.VISIT: UNSCHEDULED 1.1, LB.LBDTC: 2014-02-21T13:00
    *   **逸脱内容:** 被験者は、予定外のVisit (UNSCHEDULED 1.1) にて臨床検査を受けている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design (Page 8), Protocol Attachment LZZT.1 Schedule of Events
    *   **判断理由:** プロトコルでは、UNSCHEDULED 1.1のVisitは予定されていない。LBドメインのVISITが"UNSCHEDULED 1.1"、LBDTCが2014-02-21T13:00であり、予定外のVisitで臨床検査が実施されているため、評価スケジュール違反と判断できる。ただし、臨床試験結果への影響は小さいと判断する。

* 　**逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBDY: -79 (LB.LBTESTCD = "ALB", "ALP", "ALT", "AST", "BILI", "BUN", "CA", "CHOL", "CK", "CREAT", "GGT", "GLUC", "PHOS", "PROT", "URATE", "UROBIL", "SPGRAV", "PH", "KETONES", "COLOR")
    *   **逸脱内容:** スクリーニング時の採血日が、プロトコルで規定された期間（-7日）よりも前に行われている。
    *   **プロトコル該当箇所:** 3.1 Summary of Study Design (Page 8)
    *   **判断理由:** プロトコルでは、スクリーニング期間は2週間以内（-14日～-1日）と規定されている。LBドメインのLBDYが-79であり、規定された期間よりも前に採血が行われている。ただし、医学的見地から、この程度の逸脱は臨床試験結果に影響を与えないと判断する。

**2. クエリの作成**

*   **患者ID: 01-703-1335**

    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** EX.EXENDTC: 2014-05-07, DS.DSTERM: PROTOCOL VIOLATION, DS.DSDTC: 2014-05-24
        *   **医療機関への問い合わせ文面:** 治験薬の投与がプロトコルで規定された期間（Week6）を超えて継続された理由を説明してください。また、プロトコル逸脱（投与期間超過）による試験中止の判断に至った経緯を説明してください。
        *   **判断理由:** プロトコルでは、治験薬の投与期間はWeek6までと規定されているが、EXドメインのEXENDTCは2014-05-07であり、Week6を超えている。DSドメインのDSTERMが"PROTOCOL VIOLATION"、DSDTCが2014-05-24であり、プロトコル逸脱により試験を中止していることがわかるため。

    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM: MULTIPLE SCLEROSIS RELAPSE, AE.AESEV: MILD, AE.AESTDTC: 2014-04-01
        *   **医療機関への問い合わせ文面:** 多発性硬化症の再発に関する詳細な情報（診断日、診断方法、症状、重症度、治療内容など）を

# 01-701-1023
## Task1: Clinical Review Results
**1. 症例サマリー:**

**患者ID: 01-701-1023**

*   2012年7月22日 (Day -14): スクリーニング1。既往歴として、アルツハイマー病、足蜂巣炎、胃食道逆流症、腰痛、高血圧、陰茎プロテーゼ挿入、筋肉痛、上腕のしびれ、裂孔ヘルニア、虫垂炎、消化不良、頭痛、肘骨折、労作性呼吸困難、湿疹、坐骨神経痛、かゆみのある皮膚、近視、鼠径ヘルニア修復、外傷誘発性疼痛、副鼻腔炎、虫垂切除術が報告された。併用薬としてアスピリン、Mylanta、Tumsが報告された。教育レベルは14年。Modified Hachinski Ischemic Scoreは5点(MHITM07, MHITM10, MHITM12の項目が陽性)。MMSEスコアは報告なし。
*   2012年8月3日 (Day -2): スクリーニング2。アスピリン、Mylanta、Tumsの併用継続。
*   2012年8月5日 (Day 1): ベースライン。プラセボ投与開始。ADAS-Cog(11)スコアは13点、NPI-X(9)合計スコアは11点。DADは全項目で自立(スコア1)。
*   2012年8月7日 (Day 3): 有害事象として紅斑(軽度、2件)発現。
*   2012年8月26日 (Day 22): 24時間ホルター心電図装着。
*   2012年8月27日 (Day 23): Week 2。プラセボ投与継続。有害事象として2度房室ブロック(軽度)発現。NPI-X(9)合計スコアは10点。
*   2012年8月30日 (Day 26): 紅斑(1件)消失。
*   2012年9月2日 (Day 29): Week 4。有害事象として紅斑(軽度)発現。ADAS-Cog(11)スコアは8点、CIBIC+スコアは3点(最小限の改善)、NPI-X(9)合計スコアは11点。最終検査来院、有害事象(紅斑)による中止。
*   2013年2月18日 (Day 198): 最終回収来院。CIBIC+スコアは5点(最小限の悪化)、ADAS-Cog(11)スコアは12点、NPI-X(9)合計スコアは5点。DADは、適切な器具の選択、電話メッセージの作成と伝達、買い物からの帰宅、請求書の支払い、お金の適切な管理、余暇活動への関心、家事への関心、家事の計画と組織化、家事の完了、一人で安全に家にいること、の項目で介助が必要(スコア0)。

**2. クエリ:**

**患者ID: 01-701-1023**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE", AE.AESEV = "MILD", AE.AESTDTC = "2012-08-26"
    *   **医療機関への問い合わせ文面:** 2012年8月26日に発現した2度房室ブロック(AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE")は、プロトコル上、除外基準(EXCL16b)に該当する可能性があります。医学的見地から、この有害事象の詳細な経過、重症度(AE.AESEV = "MILD"と報告されているが、詳細な臨床経過が不明)、および転帰について、追加情報を提供してください。特に、心電図所見(具体的にどのタイプの2度房室ブロックか、心拍数、QRS幅など)、自覚症状の有無、基礎疾患(心疾患の既往など)、併用薬(心機能に影響を与える可能性のある薬剤など)との関連、および臨床的意義について詳細な情報が必要です。
    *   **判断理由:** 2度房室ブロックは、プロトコル上、除外基準に該当する可能性のある重篤な有害事象であり、患者の安全性確保および臨床試験データの信頼性確保の観点から、詳細な情報に基づいた医学的評価が不可欠である。報告された重症度(軽度)と臨床経過との整合性、およびプロトコルからの逸脱の有無を確認する必要がある。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "ADVERSE EVENT", DS.DSTERM = "ADVERSE EVENT", DS.DSDTC = "2012-09-02"
    *   **医療機関への問い合わせ文面:** 有害事象(DS.DSTERM = "ADVERSE EVENT")による中止(DS.DSDECOD = "ADVERSE EVENT")と報告されていますが、具体的にどの有害事象が中止の理由となったのか、詳細な情報を提供してください。特に、中止の直接的な原因となった有害事象の名称(AE.AETERM)、発現日(AE.AESTDTC)、重症度(AE.AESEV)、転帰(AE.AEOUT)、および臨床試験薬との因果関係(AE.AEREL)について、詳細な情報が必要です。
    *   **判断理由:** 患者が有害事象により中止に至った場合、その有害事象が臨床試験薬との関連性の有無を含め、詳細に評価される必要がある。中止理由となった有害事象を特定し、その詳細な情報を収集することは、臨床試験データの解釈、特に安全性評価において極めて重要である。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "2006", MH.MHTERM = "ALZHEIMER'S DISEASE"
    *   **医療機関への問い合わせ文面:** アルツハイマー病(MH.MHTERM = "ALZHEIMER'S DISEASE")の診断年(MH.MHSTDTC = "2006")について、より詳細な日付(年月日まで)の提供をお願いします。
    *   **判断理由:** アルツハイマー病の診断時期は、患者背景情報として重要であり、病歴の正確な把握のために、可能な限り詳細な日付情報を収集することが望ましい。

*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_0249"
    *   **医療機関への問い合わせ文面:** 胃食道逆流症(MH.MHTERM = "VERBATIM_0249")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_0461"
    *   **医療機関への問い合わせ文面:** 筋肉痛(MH.MHTERM = "VERBATIM_0461")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_0699"
    *   **医療機関への問い合わせ文面:** 裂孔ヘルニア(MH.MHTERM = "VERBATIM_0699")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_0800"
    *   **医療機関への問い合わせ文面:** 消化不良(MH.MHTERM = "VERBATIM_0800")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_0929"
    *   **医療機関への問い合わせ文面:** 頭痛(MH.MHTERM = "VERBATIM_0929")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "", MH.MHTERM = "VERBATIM_1532"
    *   **医療機関への問い合わせ文面:** 近視(MH.MHTERM = "VERBATIM_1532")の発症時期(MH.MHSTDTC)について、可能な範囲で情報提供をお願いします。
    *   **判断理由:** 既往歴の正確な把握のため、可能な範囲で発症時期の情報を収集することが望ましい。

*   **クエリNo.: 10**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMSTDTC = "2006", CM.CMTRT = "ASPIRIN"
    *   **医療機関への問い合わせ文面:** アスピリン(CM.CMTRT = "ASPIRIN")の投与開始日(CM.CMSTDTC = "2006")について、より詳細な日付(年月日まで)の提供をお願いします。
    *   **判断理由:** 併用薬の投与開始時期は、有害事象との関連性などを評価する上で重要であり、可能な限り詳細な日付情報を収集することが望ましい。

*   **クエリNo.: 11**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMSTDTC = "2002", CM.CMTRT = "MYLANTA"
    *   **医療機関への問い合わせ文面:** Mylanta(CM.CMTRT = "MYLANTA")の投与開始日(CM.CMSTDTC = "2002")について、より詳細な日付(年月日まで)の提供をお願いします。
    *   **判断理由:** 併用薬の投与開始時期は、有害事象との関連性などを評価する上で重要であり、可能な限り詳細な日付情報を収集することが望ましい。

*   **クエリNo.: 12**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMSTDTC = "2002", CM.CMTRT = "TUMS"
    *   **医療機関への問い合わせ文面:** Tums(CM.CMTRT = "TUMS")の投与開始日(CM.CMSTDTC = "2002")について、より詳細な日付(年月日まで)の提供をお願いします。
    *   **判断理由:** 併用薬の投与開始時期は、有害事象との関連性などを評価する上で重要であり、可能な限り詳細な日付情報を収集することが望ましい。

## Task2: DM Review Results
**Overall Data Quality Evaluation:**

*   **総合評価:** 一部問題あり
*   **データクリーニング/再調査が必要な項目:**
    *   CMドメイン: CMSTDTC, CMENDTC, CMINDC, CMDECOD, CMCLAS
    *   AEドメイン: AESTDTC, AEENDTC, AEDECOD
    *   LBドメイン: LBDTC, LBORNRLO, LBORNRHI, LBSTNRLO, LBSTNRHI, LBNRIND
    *   QSドメイン: QSORRES, QSSTRESC, QSSTRESN
    *   RELRECドメイン

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC = "2006", "2002" (年のみ)
    *   **矛盾の内容:** CMSTDTCが年のみで記録されており、月日が欠損している。Define.xmlでは、CMSTDTCは"date"型と定義されている。
    *   **問題点の原因（推測）:** データ入力時の不備（月日の入力を忘れた、またはシステム上の問題で月日が記録されなかった）。
    *   **対応策（提案）:** 医療機関に問い合わせ、正確な開始日（年月）を確認する。

*   **問題No.2:**
    *   **変数名と値:** CM.CMENDTC = "" (欠損)
    *   **矛盾の内容:** CMENDTCが欠損している。ASPIRINは継続的に服用されている可能性があるため、終了日が欠損しているのは不適切。
    *   **問題点の原因（推測）:** データ入力時の不備（終了日の入力を忘れた）。
    *   **対応策（提案）:** 医療機関に問い合わせ、ASPIRINの服用が終了しているか、終了している場合はその日付を確認する。

*   **問題No.3:**
    *   **変数名と値:** CM.CMINDC = "" (欠損)
    *   **矛盾の内容:** ASPIRIN, MYLANTA, TUMSのCMINDCが欠損している。
    *   **問題点の原因（推測）:** データ入力時の不備（適応症の入力を忘れた）。
    *   **対応策（提案）:** 医療機関に問い合わせ、ASPIRIN, MYLANTA, TUMSの適応症を確認する。

*   **問題No.4:**
    *   **変数名と値:** CM.CMDECOD = "UNCODED", CM.CMCLAS = "UNCODED"
    *   **矛盾の内容:** MYLANTA, TUMSのCMDECOD, CMCLASが"UNCODED"となっている。
    *   **問題点の原因（推測）:** コーディング辞書に該当する語がなかった、またはコーディング担当者のミス。
    *   **対応策（提案）:** コーディング担当者に、MYLANTA, TUMSの適切なコードを調査し、再コーディングを依頼する。

*   **問題No.5:**
    *   **変数名と値:** AE.AESTDTC = "2012-08-26", AE.AEENDTC = "" (欠損)
    *   **矛盾の内容:** AE (AESEQ=3) のAESTDTCが、対応するSVレコード (VISITNUM=3.5) のSVENDTC ("2012-08-26") より後になっている。また、AEENDTCが欠損している。
    *   **問題点の原因（推測）:** データ入力時の不備（日付の入力ミス、または終了日の入力を忘れた）。
    *   **対応策（提案）:** 医療機関に問い合わせ、正確な有害事象の発現日と終了日を確認する。

*   **問題No.6:**
    *   **変数名と値:** AE.AEDECOD = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
    *   **矛盾の内容:** AEDECODがMedDRAでコーディングされていない。
    *   **問題点の原因（推測）:** コーディング担当者のミス、またはMedDRAに該当する語がない。
    *   **対応策（提案）:** コーディング担当者に、適切なMedDRAコードを調査し、再コーディングを依頼する。

*   **問題No.7:**
    *   **変数名と値:** LB.LBDTC = "2012-07-22T12:13" (一部)
    *   **矛盾の内容:** LBDTCに時刻が含まれているが、Define.xmlでは"date"型と定義されている。
    *   **問題点の原因（推測）:** Define.xmlの定義が誤っている。
    *   **対応策（提案）:** Define.xmlのLB.LBDTCのデータ型を"datetime"に修正する。

*   **問題No.8:**
    *   **変数名と値:** LB.LBORNRLO, LB.LBORNRHI, LB.LBSTNRLO, LB.LBSTNRHI (一部)
    *   **矛盾の内容:** LBORNRLO, LBORNRHI, LBSTNRLO, LBSTNRHIが数値ではなく文字列で記録されている。Define.xmlでは、これらは数値型と定義されている。
    *   **問題点の原因（推測）:** データ入力時の不備（数値ではなく文字列を入力した）。
    *   **対応策（提案）:** データを数値に修正する。

*   **問題No.9:**
    *   **変数名と値:** LB.LBNRIND (一部)
    *   **矛盾の内容:** LBSTRESNがLBSTNRLOとLBSTNRHIの範囲内にあるにもかかわらず、LBNRINDが"NORMAL"になっていないレコードがある。
    *   **問題点の原因（推測）:** LBNRINDの導出ロジックの誤り、またはデータ入力ミス。
    *   **対応策（提案）:** LBNRINDの導出ロジックを確認し、必要であれば修正する。

*   **問題No.10:**
    *   **変数名と値:** QS.QSORRES, QS.QSSTRESC, QS.QSSTRESN (一部)
    *   **矛盾の内容:** QSORRES, QSSTRESC, QSSTRESNの値が、QSTESTCDに対応する質問の回答として不適切（例：DAITM01に対して"Y"ではなく"1"が記録されている）。
    *   **問題点の原因（推測）:** データ入力時の不備、またはQSSTRESC, QSSTRESNの導出ロジックの誤り。
    *   **対応策（提案）:** 医療機関に問い合わせ、正しい回答を確認する。QSSTRESC, QSSTRESNの導出ロジックを確認し、必要であれば修正する。

*   **問題No.11:**
    *   **変数名と値:** RELREC.IDVARVAL = "   2", "   1"
    *   **矛盾の内容:** RELREC.IDVARVALの値に不要なスペースが含まれている。
    *   **問題点の原因（推測）:** データ入力時の不備（不要なスペースを入力した）。
    *   **対応策（提案）:** IDVARVALの値から不要なスペースを削除する。

**Define.xmlの修正候補:**

*   LB.LBDTCのデータ型を"date"から"datetime"に修正する。

**クエリ:**

*   **患者ID:** 01-701-1023
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC = "2006", "2002"
        *   **医療機関への問い合わせ文面:** ASPIRIN, MYLANTA, TUMSの服用開始日について、年だけでなく月日まで含めた正確な日付をご教示ください。
        *   **判断理由:** CMSTDTCは、投与期間を評価するための重要な変数であり、年のみの情報では不十分であるため。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMENDTC = ""
        *   **医療機関への問い合わせ文面:** ASPIRINの服用は現在も継続中でしょうか。終了している場合は、その日付をご教示ください。
        *   **判断理由:** CMENDTCは、投与期間を評価するための重要な変数であり、欠損しているのは不適切なため。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMINDC = ""
        *   **医療機関への問い合わせ文面:** ASPIRIN, MYLANTA, TUMSの服用理由（適応症）をご教示ください。
        *   **判断理由:** CMINDCは、併用薬の使用目的を把握するための重要な変数であり、欠損しているのは不適切なため。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = "2012-08-26"
        *   **医療機関への問い合わせ文面:** AESEQ=3 (2度房室ブロック) のAESTDTCは2012-08-26で正しいでしょうか。SVドメインのVISITNUM=3.5 (AMBUL ECG PLACEMENT) のSVENDTCは2012-08-26です。
        *   **判断理由:** AESTDTCが、対応するSVレコードのSVENDTCより後になっているため、矛盾している。

    *   **クエリNo.5:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AEENDTC = ""
        *   **医療機関への問い合わせ文面:** AESEQ=3 (2度房室ブロック) のAEENDTCが欠損しています。有害事象の終了日をご教示ください。
        *   **判断理由:** AEENDTCは、有害事象の期間を評価するための重要な変数であり、欠損しているのは不適切なため。

    *   **クエリNo.6:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.QSORRES, QS.QSSTRESC, QS.QSSTRESN (DAD, NPI-X)
        *   **医療機関への問い合わせ文面:** DADおよびNPI-Xの回答について、一部、数値ではなく"Y"や"N"などの文字で記録されている箇所があります。数値での回答をご教示ください。
        *   **判断理由:** Define.xmlで定義されたデータ型と異なる値が記録されているため。

## Task3: Protocol Deviation Review Results
**1. プロトコル逸脱の検出**

**患者ID: 01-701-1023**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM: "ALZHEIMER'S DISEASE", MH.MHSTDTC: "2006-03-11"
    *   **逸脱内容:** 被験者はアルツハイマー病と診断されているが、プロトコルではNINCDSおよびADRDAガイドラインによる「probable AD」の診断が必要とされている。JSONデータには、この診断基準を満たしているかどうかの情報が含まれていない。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria, [2]
    *   **判断理由:** プロトコルでは、選択基準としてNINCDSおよびADRDAガイドラインによる「probable AD」の診断を要求している。JSONデータのMHドメインには、アルツハイマー病の診断名（MHTERM="ALZHEIMER'S DISEASE"）は記録されているが、これが「probable AD」の診断基準を満たしているかどうかは不明である。
*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** QS.QSTESTCD: "MMITM01" - "MMITM06", QS.VISIT: "SCREENING 1", QS.QSDTC: "2012-07-22"
    *   **逸脱内容:** 被験者のスクリーニング時のMMSEスコアが記録されているが、合計スコアが報告されていない。プロトコルではMMSEスコアが10〜23点であることが選択基準とされている。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria, [3]
    *   **判断理由:** プロトコルでは、選択基準としてMMSEスコアが10〜23点であることを要求している。JSONデータのQSドメインには、スクリーニング時のMMSEの個々の項目のスコア(QSTESTCDが"MMITM01"から"MMITM06")は記録されているが、合計スコアが記録されていないため、選択基準を満たしているかどうかを判断できない。
*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** TI.IETESTCD: "INCL05", TI.IETEST: "CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year."
    *   **逸脱内容:** 過去1年以内のCNS画像診断（CTスキャンまたは脳MRI）でADと矛盾しない結果であること、という選択基準を満たしているかどうかの情報がない。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria, [5]
    *   **判断理由:** プロトコルでは、選択基準として過去1年以内のCNS画像診断（CTスキャンまたは脳MRI）でADと矛盾しない結果であることを要求している。JSONデータには、この基準を満たしているかどうかの情報が含まれていない。
*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM: "ATRIOVENTRICULAR BLOCK SECOND DEGREE", AE.AESTDTC: "2012-08-26"
    *   **逸脱内容:** 被験者に第二度房室ブロックの有害事象が報告されている。プロトコルでは、スクリーニング時のECG記録で、第二度または第三度房室ブロック（ペースメーカーで治療されている場合を除く）の所見がある被験者は除外基準に該当する。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria, [16]
    *   **判断理由:** プロトコルでは、除外基準としてスクリーニング時のECGで第二度または第三度房室ブロック（ペースメーカーで治療されている場合を除く）がある被験者を除外すると規定している。JSONデータのAEドメインには、被験者に第二度房室ブロック（AETERM="ATRIOVENTRICULAR BLOCK SECOND DEGREE"）が発現したことが報告されている。この有害事象はスクリーニング時（2012-07-22）以降に発生しているが、スクリーニング時のECGで同様の所見があった可能性を否定できない。
*   **逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT: "ASPIRIN", CM.CMSTDTC: "2006"
    *   **逸脱内容:** 被験者は2006年からアスピリンを使用している。プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria, [31]
    *   **判断理由:** プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。JSONデータのCMドメインには、被験者がアスピリンを使用していることが記録されているが、開始日が2006年であり、除外基準に該当するかどうかは不明である。ただし、併用薬として報告されているため、プロトコル違反の可能性は低い。
*   **逸脱No.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT: "MYLANTA", CM.CMSTDTC: "2002"
    *   **逸脱内容:** 被験者は2002年からMYLANTAを使用している。プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria, [31]
    *   **判断理由:** プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。JSONデータのCMドメインには、被験者がMYLANTAを使用していることが記録されているが、開始日が2002年であり、除外基準に該当するかどうかは不明である。ただし、併用薬として報告されているため、プロトコル違反の可能性は低い。
*   **逸脱No.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT: "TUMS", CM.CMSTDTC: "2002"
    *   **逸脱内容:** 被験者は2002年からTUMSを使用している。プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。
    *   **プロトコル該当箇所:** 3.4.2.2. Exclusion Criteria, [31]
    *   **判断理由:** プロトコルでは、登録前1ヶ月以内の特定の薬剤の使用は除外基準とされている。JSONデータのCMドメインには、被験者がTUMSを使用していることが記録されているが、開始日が2002年であり、除外基準に該当するかどうかは不明である。ただし、併用薬として報告されているため、プロトコル違反の可能性は低い。

**2. クエリの作成**

**患者ID: 01-701-1023**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM: "ALZHEIMER'S DISEASE", MH.MHSTDTC: "2006-03-11"
    *   **医療機関への問い合わせ文面:** アルツハイマー病の診断は、NINCDSおよびADRDAガイドラインによる「probable AD」の診断基準を満たしていますか？診断書等の関連資料を提出してください。
    *   **判断理由:** プロトコルの選択基準3.4.2.1 [2] に合致するか確認するため。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** QS.QSTESTCD: "MMITM01" - "MMITM06", QS.VISIT: "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時のMMSEの合計スコアを報告してください。
    *   **判断理由:** プロトコルの選択基準3.4.2.1 [3] (MMSEスコア10-23点)に合致するか確認するため。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** 該当なし
    *   **医療機関への問い合わせ文面:** 過去1年以内に実施されたCNS画像診断（CTスキャンまたは脳MRI）の結果、およびADと矛盾しない所見であることを示す報告書を提出してください。
    *   **判断理由:** プロトコルの選択基準 3.4.2.1 [5] に合致するか確認するため。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM: "ATRIOVENTRICULAR BLOCK SECOND DEGREE", AE.AESTDTC: "2012-08-26"
    *   **医療機関への問い合わせ文面:** 第二度房室ブロックの有害事象について、詳細な情報（診断、重症度、処置、転帰、治験薬との因果関係など）を報告してください。また、スクリーニング時のECGで同様の所見がなかったかどうかを確認し、ECGレポートを提出してください。
    *   **判断理由:** プロトコルの除外基準 3.4.2.2 [16] に抵触する可能性があるため、詳細な情報を確認する必要がある。
*   **クエリNo.: 5**
     *   **臨床試験結果への影響度合い:** Minor
     *   **変数名と値:** CM.CMTRT: "ASPIRIN", CM.CMSTDTC: "2006", CM.CMENDTC: ""
     *   **医療機関への問い合わせ文面:** アスピリンの使用は現在も継続中ですか？　継続中の場合、投与量、投与頻度、投与経路、および使用理由を報告してください。
     *   **判断理由:** プロトコル 3.4.2.2 [31] に記載されている除外基準に該当する薬剤の併用の有無を確認するため。
*   **クエリNo.: 6**
     *   **臨床試験結果への影響度合い:** Minor
     *   **変数名と値:** CM.CMTRT: "MYLANTA", CM.CMSTDTC: "2002", CM.CMENDTC: ""
     *   **医療機関への問い合わせ文面:** MYLANTAの使用は現在も継続中ですか？　継続中の場合、投与量、投与頻度、投与経路、および使用理由を報告してください。
     *   **判断理由:** プロトコル 3.4.2.2 [31] に記載されている除外基準に該当する薬剤の併用の有無を確認するため。
*   **クエリNo.: 7**
     *   **臨床試験結果への影響度合い:** Minor
     *   **変数名と値:** CM.CMTRT: "TUMS", CM.CMSTDTC: "2002", CM.CMENDTC: ""
     *   **医療機関への問い合わせ文面:** TUMSの使用は現在も継続中ですか？　継続中の場合、投与量、投与頻度、投与経路、および使用理由を報告してください。
     *   **判断理由:** プロトコル 3.4.2.2 [31] に記載されている除外基準に該当する薬剤の併用の有無を確認するため。


# 01-703-1258
## Task1: Clinical Review Results
**1. 症例サマリー:**

**患者ID: 01-703-1258**

*   2012年07月10日 (Day -10): スクリーニング1。既往歴として、アルツハイマー病(2006年2月17日発症)、高コレステロール血症、緑内障、高血圧、食道狭窄(2011年5月)、膀胱脱(2010年4月)、糖尿病、子宮摘出術(2010年4月)、関節炎、めまい、虫垂切除術(1952年)が報告されている。併用薬として、ALEVE, CALTRATE, NORVASC, TIMOPTIC, VITAMIN Eが報告されている。スクリーニング時の検査値で、ALT 43 U/L (基準範囲: 6-32 U/L), AST 36 U/L (基準範囲: 9-34 U/L)と軽度の上昇を認める。
*   2012年07月18日 (Day -2): スクリーニング2。
*   2012年07月20日 (Day 1): ベースライン。Xanomeline High Dose群に割り付けられた。試験薬投与開始。
*   2012年07月31日 (Day 12): Ambulatory ECG Placement。
*   2012年08月01日 (Day 13): Week 2。ALT 39 U/L (基準範囲: 6-32 U/L)と軽度の上昇を認める。
*   2012年08月11日 (Day 23): 上気道感染症発症。
*   2012年08月17日 (Day 29): Week 4。上気道感染症は回復/寛解。
*   2012年08月19日 (Day 31): Ambulatory ECG Removal。
*   2012年09月04日 (Day 47): Week 6。ALT 24 U/Lと基準範囲内に回復。AST 23 U/Lと基準範囲内に回復。同日、適用部位皮膚炎(発症日: 2012年9月4日)およびめまい(発症日: 2012年8月1日)発症。
*   2012年09月14日 (Day 57): Week 8。適用部位皮膚炎は継続中。めまいは重症度悪化(発症日: 2012年10月2日)。
*   2012年09月28日 (Day 71): Week 10 (電話)。
*   2012年10月01日 (Day 75): めまい回復/寛解。
*   2012年10月09日 (Day 82): Week 12。
*   2012年10月23日 (Day 96): Week 14 (電話)。
*   2012年11月05日 (Day 109): Week 16。
*   2012年11月19日 (Day 123): Week 18 (電話)。
*   2012年12月03日 (Day 137): Week 20。
*   2012年12月20日 (Day 154): Week 22 (電話)。
*   2012年12月31日 (Day 165): Week 24。めまい再発。
*   2013年01月21日 (Day 186): Week 26。有害事象(適用部位皮膚炎)のため試験中止。
*   2013年01月25日 (Day 190): 適用部位皮膚炎回復/寛解。
*   2013年01月28日 (Day 197): AE Follow-up。

**2. クエリ:**

**患者ID: 01-703-1258**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "DIZZINESS", AE.AESEQ = 2, AE.AESTDTC = "2012-08-01", AE.AEENDTC = "2012-10-01", AE.AESEV = "SEVERE"
    *   **医療機関への問い合わせ文面:** 2012年8月1日に発症した「めまい」について、重症度が「重度」と報告されていますが、医学的に妥当でしょうか。重症度の再評価をお願いします。
    *   **判断理由:** めまいは、患者のQOLを著しく低下させる可能性があり、重症度「重度」のめまいが約2ヶ月間継続していることは、安全性上の懸念がある。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "DIZZINESS", AE.AESEQ = 5, AE.AESTDTC = "2012-10-02", AE.AEENDTC = "2012-12-31", AE.AESEV = "MODERATE"
    *   **医療機関への問い合わせ文面:** 2012年10月2日に発症した「めまい」について、重症度が「中等度」と報告されていますが、医学的に妥当でしょうか。重症度の再評価をお願いします。
    *   **判断理由:** めまいは、患者のQOLを著しく低下させる可能性があり、重症度「中等度」のめまいが約3ヶ月間継続していることは、安全性上の懸念がある。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AESEQ = 4, 6, 7
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎が複数回報告されていますが、試験薬との因果関係は「PROBABLE」と判断されています。プロトコルでは、適用部位皮膚炎は試験薬との関連性が想定される有害事象として記載されています。因果関係の再評価をお願いします。
    *   **判断理由:** 適用部位皮膚炎は、試験薬との関連性が高い有害事象であり、因果関係が「PROBABLE」と判断されていることは、安全性評価に影響を与える可能性がある。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT = "TIMOPTIC", CM.CMDECOD = "UNCODED"
    *   **医療機関への問い合わせ文面:** 併用薬TIMOPTICの標準化された医薬品名(CMDECOD)が"UNCODED"となっています。正確な医薬品名を特定し、報告してください。
    *   **判断理由:** 併用薬は、有害事象との関連性や、有効性評価に影響を与える可能性があるため、正確な医薬品名の特定が必要である。
*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT = "VITAMIN E", CM.CMDECOD = "UNCODED"
    *   **医療機関への問い合わせ文面:** 併用薬VITAMIN Eの標準化された医薬品名(CMDECOD)が"UNCODED"となっています。正確な医薬品名を特定し、報告してください。
    *   **判断理由:** 併用薬は、有害事象との関連性や、有効性評価に影響を与える可能性があるため、正確な医薬品名の特定が必要である。
*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "VITB12", LB.LBORRES = "476", LB.LBORRESU = "pg/mL", LB.LBNRIND = "NORMAL"
    *   **医療機関への問い合わせ文面:** スクリーニング時のビタミンB12の値(476 pg/mL)は基準範囲内と報告されていますが、プロトコルでは除外基準として「中央検査機関の検査値が葉酸およびビタミンB12の基準範囲を下回る場合」と規定されています。Define.xmlによると、ビタミンB12の基準範囲は200-900 pg/mLです。基準範囲内であることの確認をお願いします。
    *   **判断理由:** プロトコルとDefine.xmlの基準範囲の定義に矛盾があるため、確認が必要である。
*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.59", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-07-10)
    *   **医療機関への問い合わせ文面:** スクリーニング時の好酸球数(EOS)が0.59 THOU/uLで、基準範囲上限(0.57 THOU/uL)をわずかに超えていますが、プロトコルでは除外基準として「検査値がLilly Reference Range IIIを超える場合」と規定されています。臨床的に問題がないことを確認してください。
    *   **判断理由:** わずかな基準範囲外の値であり、臨床的な意義は低い可能性があるが、プロトコルの除外基準に抵触する可能性があるため、確認が必要である。
*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.90", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-09-04)
    *   **医療機関への問い合わせ文面:** Week 6の好酸球数(EOS)が0.90 THOU/uLで、基準範囲上限(0.57 THOU/uL)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** 基準範囲を大きく超える値であり、臨床的な意義がある可能性があるため、確認が必要である。
*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "1.09", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-09-14)
    *   **医療機関への問い合わせ文面:** Week 8の好酸球数(EOS)が1.09 THOU/uLで、基準範囲上限(0.57 THOU/uL)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** 基準範囲を大きく超える値であり、臨床的な意義がある可能性があるため、確認が必要である。
*   **クエリNo.: 10**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.75", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-10-09)
    *   **医療機関への問い合わせ文面:** Week 12の好酸球数(EOS)が0.75 THOU/uLで、基準範囲上限(0.57 THOU/uL)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** 基準範囲を大きく超える値であり、臨床的な意義がある可能性があるため、確認が必要である。
*   **クエリNo.: 11**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.70", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-11-05)
    *   **医療機関への問い合わせ文面:** Week 16の好酸球数(EOS)が0.70 THOU/uLで、基準範囲上限(0.57 THOU/uL)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** 基準範囲を大きく超える値であり、臨床的な意義がある可能性があるため、確認が必要である。
*   **クエリNo.: 12**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "MONO", LB.LBORRES = "1.07", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-07-31)
    *   **医療機関への問い合わせ文面:** Week 2の単球数(MONO)が1.07 THOU/uLで、基準範囲上限(0.92 THOU/uL)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** 基準範囲を大きく超える値であり、臨床的な意義がある可能性があるため、確認が必要である。
*   **クエリNo.: 13**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "WBC", LB.LBORRES = "10.80", LB.LBORRESU = "THOU/uL", LB.LBNRIND = "HIGH" (2012-09-14)
    *   **医療機関への問い合わせ文面:** Week 8の白血球数(WBC)が10.80 THOU/uLで、基準範囲上限(10.7 THOU/uL)をわずかに超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** わずかな基準範囲外の値であり、臨床的な意義は低い可能性があるが、プロトコルの除外基準に抵触する可能性があるため、確認が必要である。
*   **クエリNo.: 14**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "SODIUM", LB.LBORRES = "146", LB.LBORRESU = "mEq/L", LB.LBNRIND = "HIGH" (2012-11-05)
    *   **医療機関への問い合わせ文面:** Week 16のナトリウム(SODIUM)が146 mEq/Lで、基準範囲上限(145 mEq/L)をわずかに超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** わずかな基準範囲外の値であり、臨床的な意義は低い可能性があるが、プロトコルの除外基準に抵触する可能性があるため、確認が必要である。
*   **クエリNo.: 15**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "SPGRAV", LB.LBORRES = "1.032", LB.LBORRESU = "NO UNITS", LB.LBNRIND = "HIGH" (2012-07-10)
    *   **医療機関への問い合わせ文面:** スクリーニング時の尿比重(SPGRAV)が1.032で、基準範囲上限(1.03)を超えています。臨床的に問題がないことを確認してください。
    *   **判断理由:** わずかな基準範囲外の値であり、臨床的な意義は低い可能性があるが、プロトコルの除外基準に抵触する可能性があるため、確認が必要である。

## Task2: DM Review Results
**Overall Data Quality Evaluation:**

*   **Overall Assessment:** Some issues requiring clarification or correction.
*   **Data Cleaning/Re-investigation Required:**
    *   CM.CMSTDTC, CM.CMENDTC, CM.CMENDY inconsistencies.
    *   LB.LBDY inconsistencies.
    *   AE.AESTDY, AE.AEENDY inconsistencies.
    *   Missing values in multiple domains.

**Issues:**

*   **Issue No. 1:**
    *   **Variable Name and Value:** CM.CMSTDTC, CM.CMENDTC, CM.CMENDY
    *   **Inconsistency:** For CMTRT = "HYDROCORTISONE", CM.CMSTDTC is consistently "2012-09-04" across multiple records (CMSEQ 36, 42, 47, 52, 57, 61, 65), while CM.CMENDTC is consistently "2013-01-20". CM.CMENDY values are also consistent (47, 185). This suggests a single, long-term use of hydrocortisone, not multiple distinct episodes. The multiple records with the same start and end dates, but different VISITNUM and VISIT values, are likely incorrect.
    *   **Possible Cause:** Data entry error; misunderstanding of how to record ongoing concomitant medications.
    *   **Proposed Solution:** Query the site to confirm the actual start and end dates of hydrocortisone use. If it was a single, continuous period of use, consolidate these records into one.

*   **Issue No. 2:**
    *   **Variable Name and Value:** CM.CMSTDTC, CM.CMENDTC, CM.CMENDY
    *   **Inconsistency:** For CMTRT = "NORVASC", CM.CMENDTC is "2012-09-04" across multiple records (CMSEQ 2, 7, 12, 17, 22, 27, 32), but CM.CMENDY is null for some records and 47 for others. This suggests the medication was stopped, but the end date/day is missing in some records.
    *   **Possible Cause:** Data entry error; incomplete data collection.
    *   **Proposed Solution:** Query the site to confirm the actual end date of NORVASC use for each instance where CM.CMENDTC is "2012-09-04" and CM.CMENDY is null.

*   **Issue No. 3:**
    *   **Variable Name and Value:** CM.CMSTDTC, CM.CMENDTC, CM.CMENDY
    *   **Inconsistency:** For CMTRT = "TIMOPTIC", CM.CMENDTC is consistently "2012-11-19", but CM.CMENDY is null.
    *   **Possible Cause:** Data entry error; incomplete data collection.
    *   **Proposed Solution:** Query the site to confirm the actual end date of TIMOPTIC use.

*   **Issue No. 4:**
    *   **Variable Name and Value:** LB.LBDY
    *   **Inconsistency:** For several LB records, LBDY is earlier than the study start date (DM.RFSTDTC = "2012-07-20"). For example, LBSEQ=1 has LBDY=-10, while VISITDY=-7.
    *   **Possible Cause:** Incorrect calculation of LBDY, possibly due to incorrect reference date used in the calculation.
    *   **Proposed Solution:** Review the LBDY calculation logic. Ensure that LBDY is calculated as (LBDTC - RFSTDTC) + 1.  The provided Define.xml states this is the correct calculation.

*   **Issue No. 5:**
    *   **Variable Name and Value:** AE.AESTDY, AE.AEENDY
    *   **Inconsistency:** For AESEQ=2 (DIZZINESS), AESTDY=75 and AEENDY=165. For AESEQ=5 (DIZZINESS), AESTDY and AEENDY are null. The reported start and end dates for these two events overlap.
    *   **Possible Cause:** Data entry error; incorrect calculation of study day; possible confusion between two separate dizziness events.
    *   **Proposed Solution:** Query the site to clarify the start and end dates/times of the dizziness events. Determine if these are two separate events or a single event with incorrect dates. Correct AESTDY and AEENDY accordingly.

*   **Issue No. 6:**
    *   **Variable Name and Value:** Multiple variables across multiple domains.
    *   **Inconsistency:** A large number of records have null values for CMSTDY, CMENDY, CMENDTC.
    *   **Possible Cause:** Data entry error; incomplete data collection.
    *   **Proposed Solution:** Review data entry procedures and ensure all required data is collected and entered.

**Queries:**

*   **Patient ID:** 01-703-1258
    *   **Query No.:** 1
        *   **Clinical Trial Result Impact:** Major
        *   **Variable Name and Value:** CM.CMTRT = "HYDROCORTISONE", CM.CMSTDTC, CM.CMENDTC, CM.CMENDY
        *   **Inquiry:** "Multiple records for HYDROCORTISONE (CMSEQ 36, 42, 47, 52, 57, 61, 65) have the same CMSTDTC (2012-09-04) and CMENDTC (2013-01-25). Please confirm if this represents a single, continuous period of HYDROCORTISONE use, or multiple distinct episodes. If a single period, please provide the correct start and end dates. If multiple episodes, please provide the correct start and end dates for each episode."
        *   **Reasoning:** Inconsistent data suggests a potential data entry error or misunderstanding of how to record ongoing medication use.

*   **Patient ID:** 01-703-1258
    *   **Query No.:** 2
        *   **Clinical Trial Result Impact:** Major
        *   **Variable Name and Value:** CM.CMTRT = "NORVASC", CM.CMENDTC, CM.CMENDY
        *   **Inquiry:** "Several records for NORVASC (CMSEQ 2, 7, 12, 17, 22, 27, 32) have CMENDTC = '2012-09-04', but CMENDY is missing for some of these records. Please provide the correct end date/day for these instances of NORVASC use."
        *   **Reasoning:** Missing end dates for a medication known to have stopped.

*   **Patient ID:** 01-703-1258
    *   **Query No.:** 3
        *   **Clinical Trial Result Impact:** Major
        *   **Variable Name and Value:** CM.CMTRT = "TIMOPTIC", CM.CMENDTC, CM.CMENDY
        *   **Inquiry:** "For TIMOPTIC, CMENDTC is consistently '2012-11-19', but CMENDY is missing. Please provide the correct end date/day for TIMOPTIC use."
        *   **Reasoning:** Missing end date for a medication.

*   **Patient ID:** 01-703-1258
    *   **Query No.:** 4
        *   **Clinical Trial Result Impact:** Major
        *   **Variable Name and Value:** AE.AETERM = "DIZZINESS", AE.AESTDTC, AE.AEENDTC, AE.AESTDY, AE.AEENDY
        *   **Inquiry:** "There are two records for DIZZINESS (AESEQ 2 and 5) with overlapping dates. AESEQ 2 has AESTDY=75 and AEENDY=165. AESEQ 5 has null values for AESTDY and AEENDY. Please clarify the start and end dates/times for each dizziness event. Are these two separate events, or is one record incorrect?"
        *   **Reasoning:** Overlapping dates and missing study day values suggest potential data entry errors or confusion between events.

*   **Patient ID:** 01-703-1258
    *   **Query No.:** 5
        *   **Clinical Trial Result Impact:** Minor
        *   **Variable Name and Value:** LB.LBDY
        *   **Inquiry:** "Several LB records have LBDY values that are earlier than the study start date (RFSTDTC = '2012-07-20'). For example, LBSEQ=1 has LBDY=-10. Please verify the accuracy of the LBDY calculation. It should be (LBDTC - RFSTDTC) + 1."
        *   **Reasoning:** LBDY should be relative to the study start date (RFSTDTC). Negative values before the study start date indicate a potential calculation error.

## Task3: Protocol Deviation Review Results
**Patient ID: 01-703-1258**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "NORVASC", CM.CMDECOD = "AMLODIPINE", CM.CMSTDTC = "2010", CM.CMENDTC = "2012-09-04"
    *   **逸脱内容:** プロトコル除外基準31bに抵触する。被験者は、プロトコルで禁止されているカルシウム拮抗薬（中枢神経系に作用しないものを除く）である「NORVASC (AMLODIPINE)」を併用している。開始日が2010年、終了日が2012-09-04であり、スクリーニング期間および治験薬投与期間中に使用している。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 31b
    *   **判断理由:** JSONデータのCMドメインに、禁止薬剤である「NORVASC (AMLODIPINE)」の併用記録がある。開始日が2010年、終了日が2012-09-04であり、スクリーニング期間および治験薬投与期間中に使用しているため、除外基準に抵触すると判断した。

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "TIMOPTIC", CM.CMDECOD = "UNCODED", CM.CMSTDTC = "2010", CM.CMENDTC = "2012-11-19"
    *   **逸脱内容:** プロトコル除外基準31bに抵触する。被験者は、プロトコルで禁止されているβ遮断薬点眼薬である「TIMOPTIC」を併用している。開始日が2010年、終了日が2012-11-19であり、スクリーニング期間および治験薬投与期間中に使用している。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 31b
    *   **判断理由:** JSONデータのCMドメインに、禁止薬剤である「TIMOPTIC」の併用記録がある。開始日が2010年、終了日が2012-11-19であり、スクリーニング期間および治験薬投与期間中に使用しているため、除外基準に抵触すると判断した。

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = "DIABETES", MH.MHDECOD = "DIABETES MELLITUS", MH.MHSTDTC = ""
    *   **逸脱内容:** プロトコル除外基準19, 30に抵触する可能性がある。被験者は糖尿病の既往があるが、MHSTDTCが不明であるため、過去5年以内の内分泌疾患の既往の有無が確認できない。また、インスリン依存性糖尿病患者の場合、HbA1c値が基準範囲を超えている可能性がある。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 19, 30
    *   **判断理由:** JSONデータのMHドメインに糖尿病の既往の記録があるが、MHSTDTCが不明であるため、過去5年以内の内分泌疾患の既往の有無が確認できない。また、LBドメインにHbA1cの記録がないため、除外基準30に抵触している可能性がある。

*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "ALT", LB.LBORRES = "43", LB.LBORRESU = "U/L", LB.LBORNRLO = "6", LB.LBORNRHI = "32", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **逸脱内容:** プロトコル除外基準27に抵触する。スクリーニング時のALT値が43 U/Lであり、Lilly Reference Range IIIの上限値32 U/Lを超えている。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 27
    *   **判断理由:** JSONデータのLBドメインに、スクリーニング時のALT値が基準範囲を超えている記録があるため。

*   **逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "AST", LB.LBORRES = "36", LB.LBORRESU = "U/L", LB.LBORNRLO = "9", LB.LBORNRHI = "34", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **逸脱内容:** プロトコル除外基準27に抵触する。スクリーニング時のAST値が36 U/Lであり、Lilly Reference Range IIIの上限値34 U/Lを超えている。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 27
    *   **判断理由:** JSONデータのLBドメインに、スクリーニング時のAST値が基準範囲を超えている記録があるため。

*   **逸脱No.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.59", LB.LBORRESU = "THOU/uL", LB.LBORNRLO = "0", LB.LBORNRHI = "0.57", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **逸脱内容:** プロトコル除外基準27に抵触する可能性がある。スクリーニング時の好酸球数(EOS)が0.59 THOU/uLであり、Lilly Reference Range IIIの上限値0.57 THOU/uLを超えている。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 27
    *   **判断理由:** JSONデータのLBドメインに、スクリーニング時の好酸球数(EOS)が基準範囲を超えている記録があるため。ただし、軽微な逸脱であり、臨床的意義は低い可能性がある。

*   **逸脱No.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "SPGRAV", LB.LBORRES = "1.032", LB.LBORRESU = "NO UNITS", LB.LBORNRLO = "1.006", LB.LBORNRHI = "1.03", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **逸脱内容:** プロトコル除外基準27に抵触する可能性がある。スクリーニング時の尿比重(SPGRAV)が1.032であり、Lilly Reference Range IIIの上限値1.03を超えている。
    *   **プロトコル該当箇所:** 3.4.2.2. 除外基準 27
    *   **判断理由:** JSONデータのLBドメインに、スクリーニング時の尿比重(SPGRAV)が基準範囲を超えている記録があるため。ただし、軽微な逸脱であり、臨床的意義は低い可能性がある。

*   **逸脱No.: 8**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "ADVERSE EVENT", DS.DSTERM = "ADVERSE EVENT", DS.DSSTDTC = "2013-01-21"
    *   **逸脱内容:** 有害事象による中止。被験者は有害事象により、プロトコルで規定された26週間の投与期間を完了せずに中止している。
    *   **プロトコル該当箇所:** 3.10.1. Discontinuations
    *   **判断理由:** JSONデータのDSドメインに、有害事象による中止の記録があるため。

**患者ID: 01-703-1258**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = "DIABETES", MH.MHDECOD = "DIABETES MELLITUS", MH.MHSTDTC = ""
    *   **医療機関への問い合わせ文面:** 糖尿病の既往(MH.MHTERM = "DIABETES", MH.MHDECOD = "DIABETES MELLITUS")の開始日(MHSTDTC)が不明です。正確な開始日を西暦で提供してください。また、インスリン依存性糖尿病であるか否かを確認してください。
    *   **判断理由:** プロトコル除外基準19（過去5年以内の重篤な内分泌疾患）および30（インスリン依存性糖尿病患者でHbA1c値が基準範囲を超える場合）への抵触の可能性を判断するため、正確な開始日とインスリン依存性の有無を確認する必要がある。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "ALT", LB.LBORRES = "43", LB.LBORRESU = "U/L", LB.LBORNRLO = "6", LB.LBORNRHI = "32", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **医療機関への問い合わせ文面:** スクリーニング時のALT値が43 U/Lであり、Lilly Reference Range IIIの上限値32 U/Lを超えています。臨床的に問題がないと判断された理由を説明してください。
    *   **判断理由:** プロトコル除外基準27では、ALT値が基準範囲を超える場合は除外対象となるが、臨床的に問題がないと判断された場合は例外となる。判断理由を確認する必要がある。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "AST", LB.LBORRES = "36", LB.LBORRESU = "U/L", LB.LBORNRLO = "9", LB.LBORNRHI = "34", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **医療機関への問い合わせ文面:** スクリーニング時のAST値が36 U/Lであり、Lilly Reference Range IIIの上限値34 U/Lを超えています。臨床的に問題がないと判断された理由を説明してください。
    *   **判断理由:** プロトコル除外基準27では、AST値が基準範囲を超える場合は除外対象となるが、臨床的に問題がないと判断された場合は例外となる。判断理由を確認する必要がある。

*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "EOS", LB.LBORRES = "0.59", LB.LBORRESU = "THOU/uL", LB.LBORNRLO = "0", LB.LBORNRHI = "0.57", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **医療機関への問い合わせ文面:** スクリーニング時の好酸球数(EOS)が0.59 THOU/uLであり、Lilly Reference Range IIIの上限値0.57 THOU/uLを超えています。臨床的に問題がないと判断された理由を説明してください。
    *   **判断理由:** プロトコル除外基準27では、好酸球数(EOS)が基準範囲を超える場合は除外対象となるが、臨床的に問題がないと判断された場合は例外となる。判断理由を確認する必要がある。

*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "SPGRAV", LB.LBORRES = "1.032", LB.LBORRESU = "NO UNITS", LB.LBORNRLO = "1.006", LB.LBORNRHI = "1.03", LB.LBNRIND = "HIGH", LB.VISIT = "SCREENING 1", LB.LBDTC = "2012-07-10T16:30"
    *   **医療機関への問い合わせ文面:** スクリーニング時の尿比重(SPGRAV)が1.032であり、Lilly Reference Range IIIの上限値1.03を超えています。臨床的に問題がないと判断された理由を説明してください。
    *   **判断理由:** プロトコル除外基準27では、尿比重(SPGRAV)が基準範囲を超える場合は除外対象となるが、臨床的に問題がないと判断された場合は例外となる。判断理由を確認する必要がある。

*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AESEV = "MILD", AE.AESTDTC = "2012-09-04", AE.AEENDTC = "2013-01-25"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の重症度(AESEV)が軽度から中等度、そして軽度へと変化しています。各時点での重症度判定の根拠となった具体的な皮膚症状（発赤、腫脹、そう痒感など）の詳細を教えてください。
    *   **判断理由:** 有害事象の重症度評価は、臨床試験の安全性評価において重要である。重症度判定の根拠を明確にする必要がある。

*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "DIZZINESS", AE.AESEV = "SEVERE", AE.AESTDTC = "2012-08-01", AE.AEENDTC = "2012-10-01"
    *   **医療機関への問い合わせ文面:** めまい(DIZZINESS)の重症度(AESEV)が重度と判定されています。重症度判定の根拠となった具体的な症状（回転性めまい、浮動性めまい、失神など）の詳細と、日常生活への影響について教えてください。
    *   **判断理由:** 有害事象の重症度評価は、臨床試験の安全性評価において重要である。重症度判定の根拠を明確にする必要がある。

*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "DIZZINESS", AE.AESEV = "MODERATE", AE.AESTDTC = "2012-10-02", AE.AEENDTC = "2012-12-31"
    *   **医療機関への問い合わせ文面:** めまい(DIZZINESS)の重症度(AESEV)が中等度と判定されています。重症度判定の根拠となった具体的な症状（回転性めまい、浮動性めまい、失神など）の詳細と、日常生活への影響について教えてください。
    *   **判断理由:** 有害事象の重症度評価は、臨床試験の安全性評価において重要である。重症度判定の根拠を明確にする必要がある。

*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "UPPER RESPIRATORY TRACT INFECTION", AE.AESEV = "MILD", AE.AESTDTC = "2012-08-11", AE.AEENDTC = "2012-08-19"
    *   **医療機関への問い合わせ文面:** 上気道感染(UPPER RESPIRATORY TRACT INFECTION)の具体的な症状（鼻汁、鼻閉、咽頭痛、咳など）と、その重症度（軽度、中等度、重度）を判定した根拠を教えてください。
    *   **判断理由:** 有害事象の重症度評価は、臨床試験の安全性評価において重要である。重症度判定の根拠を明確にする必要がある。

*   **クエリNo.: 10**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "UPPER RESPIRATORY TRACT INFECTION", AE.AESEV = "MILD", AE.AESTDTC = "2012-08-11", AE.AEENDTC = "2012-08-19"
    *   **医療機関への問い合わせ文面:** 上気道感染(UPPER RESPIRATORY TRACT INFECTION)が2回記録されていますが、同一の事象であると考えられます。同一の事象であるか確認してください。もし異なる事象である場合は、それぞれの事象について具体的な症状とその重症度を教えてください。
    *   **判断理由:** 同一の有害事象が重複して記録されている可能性があるため、確認が必要である。

*   **クエリNo.: 11**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "HYDROCORTISONE", CM.CMDOSE = "1", CM.CMDOSU = "VIAL", CM.CMROUTE = "TOPICAL", CM.CMSTDTC = "2012-09-04", CM.CMENDTC = "2013-01-20"
    *   **医療機関への問い合わせ文面:** HYDROCORTISONEの剤形(CMDOSFRM)がVIALとなっていますが、投与経路(CMROUTE)はTOPICALです。剤形と投与経路に矛盾があります。正しい情報を入力してください。
    *   **判断理由:** 剤形と投与経路に矛盾があるため、正しい情報を確認する必要がある。

*   **クエリNo.: 12**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "NORVASC", CM.CMDECOD = "AMLODIPINE", CM.CMSTDTC = "2010", CM.CMENDTC = "2012-09-04"
    *   **医療機関への問い合わせ文面:** NORVASC (AMLODIPINE)はプロトコルで併用が禁止されている薬剤です。2012-09-04に投与を終了していますが、プロトコル3.4.2.2除外基準31bでは、スクリーニング前1ヶ月以内の使用が除外基準となっています。本薬剤の使用について、プロトコルからの逸脱と判断しましたが、問題ないか確認してください。
    *   **判断理由:** プロトコルで禁止されている薬剤の併用が確認されたため、プロトコル逸脱の有無を確認する必要がある。

*   **クエリNo.: 13**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "TIMOPTIC", CM.CMDECOD = "UNCODED", CM.CMSTDTC = "2010", CM.CMENDTC = "2012-11-19"
    *   **医療機関への問い合わせ文面:** TIMOPTICはプロトコルで併用が禁止されている薬剤です。2012-11-19に投与を終了していますが、プロトコル3.4.2.2除外基準31bでは、スクリーニング前1ヶ月以内の使用が除外基準となっています。本薬剤の使用について、プロトコルからの逸脱と判断しましたが、問題ないか確認してください。
    *   **判断理由:** プロトコルで禁止されている薬剤の併用が確認されたため、プロトコル逸脱の有無を確認する必要がある。

*   **クエリNo.: 14**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "HYDROCORTISONE", CM.CMSTDTC = "2012-09-04", CM.CMENDTC = "2013-01-20"
    *   **医療機関への問い合わせ文面:** HYDROCORTISONEはプロトコル3.6.2. TTS Administration Proceduresに記載されている通り、TTS適用前に使用する薬剤です。CMドメインに記録されていますが、これはTTS適用前の使用で間違いないでしょうか。
    *   **判断理由:** プロトコルで規定されている使用方法と異なる使用方法で記録されている可能性があるため、確認が必要である。

*   **クエリNo.: 15**
     *   **臨床試験結果への影響度合い:** Major
     *   **変数名と値:** DS.DSDECOD = "ADVERSE EVENT", DS.DSTERM = "ADVERSE EVENT", DS.DSSTDTC = "2013-01-21"
     *   **医療機関への問い合わせ文面:** 有害事象による中止と記録されていますが、具体的にどのような有害事象により中止に至ったのか、詳細な情報をDSドメインではなく、AEドメインに記録してください。
     *   **判断理由:** 有害事象による中止の場合、具体的な有害事象名がDSドメインではなく、AEドメインに記録されるべきである。

* **クエリNo.: 16**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "FINAL LAB VISIT", DS.DSTERM = "FINAL LAB VISIT", DS.DSSTDTC = "2012-12-31"
    *   **医療機関への問い合わせ文面:** 最終検査来院(FINAL LAB VISIT)が2012-12-31に実施されていますが、これは有害事象による中止に伴う最終検査で間違いないでしょうか。
    *   **判断理由:** 有害事象による中止の場合、最終検査来院の日付が有害事象の終了日と一致しない可能性があるため、確認が必要である。

* **クエリNo.: 17**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "FINAL LAB VISIT", DS.DSTERM = "FINAL LAB VISIT", DS.DSSTDTC = "2012-12-31", DS.VISIT = "WEEK 24"
    *   **医療機関への問い合わせ文面:** 最終検査来院(FINAL LAB VISIT)がWEEK24に実施されていますが、プロトコル3.10.1. Discontinuationsには、「患者がVisit 12 (Week 24)より前に中止した場合、可能な限り24週目に再来院してもらい、完全な有効性評価を行う」と記載されています。有害事象による中止であるにも関わらず、WEEK24に最終検査来院が実施されている理由を説明してください。
    *   **判断理由:** プロトコルでは、有害事象による中止の場合、可能な限り24週目に再来院して評価を行うことになっているが、本症例では24週目に最終検査来院が実施されているため、その理由を確認する必要がある。

* **クエリNo.: 18**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSSTDTC = "2013-01-21", DS.DSSTDY = "186"
    *   **医療機関への問い合わせ文面:** 有害事象による中止日(DS.DSSTDTC)が2013-01-21、Study Dayが186日目となっています。DMドメインのRFSTDTCが2012-07-20であることから、DSSTDYは185日となるはずです。DSSTDYが正しいか確認してください。
    *   **判断理由:** DSSTDYの計算に誤りがある可能性があるため。

* **クエリNo.: 19**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSSTDTC = "2012-12-31", DS.DSSTDY = "165"
    *   **医療機関への問い合わせ文面:** 最終検査来院日(DS.DSSTDTC)が2012-12-31、Study Dayが165日目となっています。DMドメインのRFSTDTCが2012-07-20であることから、DSSTDYは164日となるはずです。DSSTDYが正しいか確認してください。
    *   **判断理由:** DSSTDYの計算に誤りがある可能性があるため。

* **クエリNo.: 20**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXENDTC = "2013-01-11"
    *   **医療機関への問い合わせ文面:** 治験薬の最終投与日が2013-01-11となっています。有害事象による中止日が2013-01-21であり、プロトコル3.10.1. Discontinuationsには、「患者の投与を中止することを決定した場合、患者の投与量を漸減させるために、直ちに25-cm2パッチを除去するよう指示する。患者には、早期中止の来院まで、50-cm2パッチを毎日適用するよう指示する。」と記載されています。最終投与日が2013-01-11となっている理由を説明してください。
    *   **判断理由:** プロトコルでは、有害事象による中止の場合、漸減期間を設けることになっているが、本症例では漸減期間が設けられていないように見えるため、確認が必要である。

* **クエリNo.: 21**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXENDY = "176"
    *   **医療機関への問い合わせ文面:** 治験薬の最終投与日のStudy Day(EX.EXENDY)が176日目となっています。DMドメインのRFSTDTCが2012-07-20、EX.EXENDTCが2013-01-11であることから、EXENDYは175日となるはずです。EXENDYが正しいか確認してください。
    *   **判断理由:** EXENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 22**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AEENDTC = "2013-01-25"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の終了日が2013-01-25となっています。有害事象による中止日が2013-01-21であり、プロトコル3.10.1. Discontinuationsには、「患者がVisit 12 (Week 24)より前に中止した場合、可能な限り24週目に再来院してもらい、完全な有効性評価を行う」と記載されています。有害事象終了日が2013-01-25となっている理由を説明してください。
    *   **判断理由:** 有害事象による中止の場合、有害事象の終了日が中止日以降になることは通常ないため、確認が必要である。

* **クエリNo.: 23**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AEENDY = "190"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の終了日のStudy Day(AE.AEENDY)が190日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AEENDTCが2013-01-25であることから、AEENDYは189日となるはずです。AEENDYが正しいか確認してください。
    *   **判断理由:** AEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 24**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "75"
    *   **医療機関への問い合わせ文面:** めまい(DIZZINESS)の開始日のStudy Day(AE.AESTDY)が75日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AESTDTCが2012-08-01であることから、AESTDYは13日となるはずです。AESTDYが正しいか確認してください。
    *   **判断理由:** AESTDYの計算に誤りがある可能性があるため。

* **クエリNo.: 25**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AEENDY = "165"
    *   **医療機関への問い合わせ文面:** めまい(DIZZINESS)の終了日のStudy Day(AE.AEENDY)が165日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AEENDTCが2012-10-01であることから、AEENDYは74日となるはずです。AEENDYが正しいか確認してください。
    *   **判断理由:** AEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 26**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "23", AE.AEENDY = "31"
    *   **医療機関への問い合わせ文面:** 上気道感染(UPPER RESPIRATORY TRACT INFECTION)の開始日と終了日のStudy Day(AE.AESTDY, AE.AEENDY)がそれぞれ23日目、31日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AESTDTCが2012-08-11、AE.AEENDTCが2012-08-19であることから、AESTDYは23日、AEENDYは31日となるはずです。AESTDYとAEENDYが正しいか確認してください。
    *   **判断理由:** AESTDYとAEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 27**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "47", AE.AEENDY = "190"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の開始日と終了日のStudy Day(AE.AESTDY, AE.AEENDY)がそれぞれ47日目、190日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AESTDTCが2012-09-04、AE.AEENDTCが2013-01-25であることから、AESTDYは47日、AEENDYは189日となるはずです。AESTDYとAEENDYが正しいか確認してください。
    *   **判断理由:** AESTDYとAEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 28**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "47", AE.AEENDY = "190"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の開始日と終了日のStudy Day(AE.AESTDY, AE.AEENDY)がそれぞれ47日目、190日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AESTDTCが2012-09-04、AE.AEENDTCが2013-01-25であることから、AESTDYは47日、AEENDYは189日となるはずです。AESTDYとAEENDYが正しいか確認してください。
    *   **判断理由:** AESTDYとAEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 29**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "47", AE.AEENDY = "190"
    *   **医療機関への問い合わせ文面:** 適用部位皮膚炎(APPLICATION SITE DERMATITIS)の開始日と終了日のStudy Day(AE.AESTDY, AE.AEENDY)がそれぞれ47日目、190日目となっています。DMドメインのRFSTDTCが2012-07-20、AE.AESTDTCが2012-09-04、AE.AEENDTCが2013-01-25であることから、AESTDYは47日、AEENDYは189日となるはずです。AESTDYとAEENDYが正しいか確認してください。
    *   **判断理由:** AESTDYとAEENDYの計算に誤りがある可能性があるため。

* **クエリNo.: 30**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDY = "23", AE.AEENDY = "31"
    *   **医療機関への問い合わせ文面:** 上気道感染(UPPER RESPIRATORY TRACT INFECTION)の開始日と終了日のStudy Day(AE.AESTDY, AE

# 01-703-1076
## Task1: Clinical Review Results
**1. 症例サマリー:**

*   **患者ID: 01-703-1076**
    *   2013年10月16日 (Day -9): スクリーニング検査で、アルブミン (4.9 g/dL, 基準範囲上限超え)、コレステロール (307 mg/dL, 基準範囲上限超え)、尿酸 (7.8 mg/dL, 基準範囲上限超え)、総蛋白 (8.1 g/dL, 基準範囲上限超え) が高値。
    *   2013年10月17日 (Day -8): スクリーニング1。既往歴として、アルツハイマー病、高コレステロール血症、緑内障、高血圧、痛風。併用薬としてアスピリン、ロピド、チモプティック。
    *   2013年10月23日 (Day -2): スクリーニング2。
    *   2013年10月25日 (Day 1): 治療開始。キサノメリン高用量群に割付。
    *   2013年11月20日 (Day 27): 4週目の診察。血清カルシウム (10.5 mg/dL, 基準範囲上限超え)、コレステロール (319 mg/dL, 基準範囲上限超え)、尿酸 (7.7 mg/dL, 基準範囲上限超え)、総蛋白 (8.4 g/dL, 基準範囲上限超え) が高値。良性前立腺肥大症、前立腺生検の有害事象報告。
    *   2013年11月23日 (Day 30): 適用部位そう痒、適用部位皮膚炎の有害事象報告。
    *   2013年12月4日 (Day 41): 6週目の診察。尿酸 (8.4 mg/dL, 基準範囲上限超え) が高値。高コレステロール血症、多汗症の有害事象報告。
    *   2013年12月17日 (Day 54): 8週目の診察。適用部位そう痒の有害事象報告 (中等度)。
    *   2013年12月24日 (Day 61): 有害事象 (適用部位そう痒、適用部位皮膚炎) により投与中止。

**2. クエリ:**

*   **患者ID: 01-703-1076**
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AESTDTC = "2013-11-23", AE.AESEV = "MILD"
        *   **医療機関への問い合わせ文面:** 2013年11月23日に発現した適用部位皮膚炎について、重症度が軽度と報告されていますが、2013年12月24日に有害事象による投与中止に至っています。投与中止に至るまでの経過、重症度の変化、処置、転帰について詳細な情報を提供してください。
        *   **判断理由:** 有害事象による投与中止は、安全性評価において重要なイベントです。軽度と報告された有害事象が投与中止に至った経緯を詳細に把握し、医学的に妥当な判断がなされたかを確認する必要があります。
    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2013-11-23", AE.AESEV = "MILD", "MODERATE"
        *   **医療機関への問い合わせ文面:** 2013年11月23日に発現した適用部位そう痒について、重症度が軽度、中等度と報告されていますが、2013年12月24日に有害事象による投与中止に至っています。投与中止に至るまでの経過、重症度の変化、処置、転帰について詳細な情報を提供してください。
        *   **判断理由:** 有害事象による投与中止は、安全性評価において重要なイベントです。軽度、中等度と報告された有害事象が投与中止に至った経緯を詳細に把握し、医学的に妥当な判断がなされたかを確認する必要があります。
    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM = "HYPERHIDROSIS", AE.AESTDTC = "2013-11-25"
        *   **医療機関への問い合わせ文面:** 2013年11月25日に発現した多汗症について、試験薬との因果関係は「可能性あり」と報告されています。多汗症の発現状況、重症度、経過、処置について詳細な情報を提供してください。
        *   **判断理由:** 多汗症は、コリン作動薬の既知の副作用である可能性があります。試験薬との因果関係が否定できないため、詳細な情報を収集し、安全性評価に役立てる必要があります。
    *   **クエリNo.: 4**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "CORTISONE", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているCORTISONEについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    *   **クエリNo.: 5**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "LAC-HYDRIN", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているLAC-HYDRINについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    *   **クエリNo.: 6**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "LIPITOR", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているLIPITORについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    *   **クエリNo.: 7**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "LOPID", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているLOPIDについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    *   **クエリNo.: 8**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "MEVACOR", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているMEVACORについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    *   **クエリNo.: 9**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "TIMOPTIC", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬として報告されているTIMOPTICについて、標準化された医薬品名 (CMDECOD) を提供してください。
        *   **判断理由:** 併用薬の正確な特定は、安全性評価において重要です。標準化された医薬品名を提供することで、他の報告との比較や、相互作用の可能性の評価が可能になります。
    * **クエリNo.: 10**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "CA", LB.VISIT = "WEEK 4", LBSTRESN = 2.61975, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月20日 (Week 4) の血清カルシウム値が 2.61975 mmol/L (10.5 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 11**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "CHOL", LB.VISIT = "SCREENING 1", LBSTRESN = 7.93902, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年10月16日 (スクリーニング時) のコレステロール値が 7.93902 mmol/L (307 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 12**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "CHOL", LB.VISIT = "WEEK 4", LBSTRESN = 8.24934, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月20日 (Week 4) のコレステロール値が 8.24934 mmol/L (319 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 13**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "SCREENING 1", LBSTRESN = 463.944, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年10月16日 (スクリーニング時) の尿酸値が 463.944 umol/L (7.8 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 14**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "WEEK 2", LBSTRESN = 457.996, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月6日 (Week 2) の尿酸値が 457.996 umol/L (7.7 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 15**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "WEEK 4", LBSTRESN = 457.996, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月20日 (Week 4) の尿酸値が 457.996 umol/L (7.7 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 16**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "WEEK 6", LBSTRESN = 499.632, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年12月4日 (Week 6) の尿酸値が 499.632 umol/L (8.4 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 17**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "WEEK 8", LBSTRESN = 469.892, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年12月17日 (Week 8) の尿酸値が 469.892 umol/L (7.9 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 18**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "URATE", LB.VISIT = "WEEK 12", LBSTRESN = 463.944, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年12月24日 (Week 12) の尿酸値が 463.944 umol/L (7.8 mg/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 19**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "PROT", LB.VISIT = "SCREENING 1", LBSTRESN = 81, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年10月16日 (スクリーニング時) の総蛋白値が 81 g/L (8.1 g/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 20**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "PROT", LB.VISIT = "WEEK 4", LBSTRESN = 84, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月20日 (Week 4) の総蛋白値が 84 g/L (8.4 g/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 21**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "ALB", LB.VISIT = "SCREENING 1", LBSTRESN = 49, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年10月16日 (スクリーニング時) のアルブミン値が 49 g/L (4.9 g/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 22**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "ALB", LB.VISIT = "WEEK 4", LBSTRESN = 48, LBNRIND = "HIGH"
        *   **医療機関への問い合わせ文面:** 2013年11月20日 (Week 4) のアルブミン値が 48 g/L (4.8 g/dL) と基準範囲上限を超えていますが、その後の経過と臨床的意義について説明してください。
        *   **判断理由:** 基準範囲上限を超える検査値は、潜在的な健康問題を示唆する可能性があります。その後の経過と臨床的意義を確認し、安全性評価に役立てる必要があります。
    * **クエリNo.: 23**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE", MH.MHSTDTC = "2012-08-27"
        *   **医療機関への問い合わせ文面:** アルツハイマー病の診断日 (2012-08-27) は、スクリーニング1 (2013-10-17) よりも前ですが、MHSTDTC が欠損値ではなく日付で報告されています。アルツハイマー病と診断された根拠 (診断基準、検査など) と、診断日を特定できた理由について詳細な情報を提供してください。
        *   **判断理由:** アルツハイマー病は、本試験の主要な対象疾患であり、診断の正確性は重要です。診断日と診断根拠を明確にすることで、患者背景の妥当性を評価できます。
    * **クエリNo.: 24**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM = "HYPERCHOLESTEROLEMIA", MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:** 高コレステロール血症のMHSTDTCが欠損値となっています。発現日を特定できない理由を説明してください。もし可能であれば、おおよその発現時期 (例: 2010年頃) を提供してください。
        *   **判断理由:** 既往歴の発現時期は、試験薬との因果関係を評価する上で重要な情報です。可能な範囲で発現時期を特定することで、安全性評価の精度を高めることができます。
    * **クエリNo.: 25**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM = "GLAUCOMA", MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:** 緑内障のMHSTDTCが欠損値となっています。発現日を特定できない理由を説明してください。もし可能であれば、おおよその発現時期 (例: 2010年頃) を提供してください。
        *   **判断理由:** 既往歴の発現時期は、試験薬との因果関係を評価する上で重要な情報です。可能な範囲で発現時期を特定することで、安全性評価の精度を高めることができます。
    * **クエリNo.: 26**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM = "HYPERTENSION", MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:** 高血圧のMHSTDTCが欠損値となっています。発現日を特定できない理由を説明してください。もし可能であれば、おおよその発現時期 (例: 2010年頃) を提供してください。
        *   **判断理由:** 既往歴の発現時期は、試験薬との因果関係を評価する上で重要な情報です。可能な範囲で発現時期を特定することで、安全性評価の精度を高めることができます。
    * **クエリNo.: 27**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM = "GOUT", MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:** 痛風のMHSTDTCが欠損値となっています。発現日を特定できない理由を説明してください。もし可能であれば、おおよその発現時期 (例: 2010年頃) を提供してください。
        *   **判断理由:** 既往歴の発現時期は、試験薬との因果関係を評価する上で重要な情報です。可能な範囲で発現時期を特定することで、安全性評価の精度を高めることができます。
    * **クエリNo.: 28**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM = "HYPERCHOLESTEROLAEMIA", AE.AESTDTC = "2007"
        *   **医療機関への問い合わせ文面:** 高コレステロール血症の有害事象報告がありますが、AESTDYがNULLです。AESTDYを算出できない理由を説明してください。もし可能であれば、おおよその発現時期 (例: 2007年頃) を提供してください。
        *   **判断理由:** 有害事象の発現時期は、試験薬との因果関係を評価する上で重要な情報です。可能な範囲で発現時期を特定することで、安全性評価の精度を高めることができます。
    * **クエリNo.: 29**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "ASPIRIN", CM.CMSTDTC = "2010"
        *   **医療機関への問い合わせ文面:** アスピリンの投与開始日が年 (2010年) しか報告されていません。正確な投与開始日 (YYYY-MM-DD) を提供してください。もし正確な日付が不明な場合は、その理由を説明し、可能な限り詳細な情報 (例: 2010年春頃) を提供してください。
        *   **判断理由:** 併用薬の投与開始日は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。可能な限り正確な日付を特定する必要があります。
    * **クエリNo.: 30**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = "TIMOPTIC", CM.CMSTDTC = "2012-11-13"
        *   **医療機関への問い合わせ文面:** チモプティックの投与開始日が2012-11-13と報告されています。プロトコルでは、点眼薬のチモプティックは、ケースバイケースで許容されると記載されています。この患者への投与が許容された理由、投与量、投与期間、および緑内障の重症度について、詳細な情報を提供してください。
        *   **判断理由:** プロトコルで制限されている併用薬の使用は、試験結果の解釈に影響を与える可能性があります。投与が許容された理由と、患者の状態を詳細に把握する必要があります。
    * **クエリNo.: 31**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSSTDTC = "2013-12-24", DS.DSSTDY = 61
        *   **医療機関への問い合わせ文面:** 2013年12月24日 (Day 61) に有害事象を理由に試験を中止していますが、中止理由となった有害事象の詳細 (AETERM, AESEV, AERELなど) を AE ドメインから特定できませんでした。中止理由となった有害事象の詳細を AE ドメインのデータと照合して確認し、報告してください。
        *   **判断理由:** 被験者の中止理由は、試験結果の解釈に影響を与える重要な情報です。DSドメインとAEドメインのデータの整合性を確認し、正確な中止理由を特定する必要があります。
    * **クエリNo.: 32**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSTERM = "FINAL LAB VISIT", DS.DSDECOD = "FINAL LAB VISIT"
        *   **医療機関への問い合わせ文面:** 最終検査来院 (FINAL LAB VISIT) が報告されていますが、これはプロトコルで規定された来院ではありません。この来院が実施された理由と、この来院で実施された評価項目について説明してください。
        *   **判断理由:** プロトコルで規定されていない来院は、試験データの解釈に影響を与える可能性があります。来院の理由と実施された評価項目を明確にする必要があります。
    * **クエリNo.: 33**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "" (アスピリン)
        *   **医療機関への問い合わせ文面:** アスピリンの投与終了日が報告されていません。投与が継続されている場合は、その旨を明記し、投与を終了している場合は、終了日を報告してください。
        *   **判断理由:** 併用薬の投与期間は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。
    * **クエリNo.: 34**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "" (チモプティック)
        *   **医療機関への問い合わせ文面:** チモプティックの投与終了日が報告されていません。投与が継続されている場合は、その旨を明記し、投与を終了している場合は、終了日を報告してください。
        *   **判断理由:** 併用薬の投与期間は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。
    * **クエリNo.: 35**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "" (コルチゾン)
        *   **医療機関への問い合わせ文面:** コルチゾンの投与終了日が報告されていません。投与が継続されている場合は、その旨を明記し、投与を終了している場合は、終了日を報告してください。
        *   **判断理由:** 併用薬の投与期間は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。
    * **クエリNo.: 36**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "" (LAC-HYDRIN)
        *   **医療機関への問い合わせ文面:** LAC-HYDRINの投与終了日が報告されていません。投与が継続されている場合は、その旨を明記し、投与を終了している場合は、終了日を報告してください。
        *   **判断理由:** 併用薬の投与期間は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。
    * **クエリNo.: 37**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "" (LIPITOR)
        *   **医療機関への問い合わせ文面:** LIPITORの投与終了日が報告されていません。投与が継続されている場合は、その旨を明記し、投与を終了している場合は、終了日を報告してください。
        *   **判断理由:** 併用薬の投与期間は、試験薬との相互作用や、有害事象との関連性を評価する上で重要な情報です。
    * **クエリNo.: 38**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "2013-11-27" (LOPID)
        *   **医療機関への問い合わせ文面:** LOPIDの投与終了日が2013-11-27と報告されていますが、これはスクリーニング期間中に該当します。プロトコルでは、スクリーニング期間中の脂質異常症治療薬の使用は除外基準とされています。この患者が試験に参加できた理由を説明してください。
        *   **判断理由:** プロトコル違反の疑いがあります。除外基準に該当する薬剤の使用は、試験結果の解釈に影響を与える可能性があります。
    * **クエリNo.: 39**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMENDTC = "2013-12-12" (MEVACOR)
        *   **医療機関への問い合わせ文面:** MEVACORの投与終了日が2013-12-12と報告されていますが、これは試験期間中に該当します。プロトコルでは、脂質異常症治療薬の併用は制限されていなかったと理解していますが、MEVACORの投与開始日と終了日、投与理由、および投与期間中の脂質値の変化について、詳細な情報を提供してください。
        *   **判断理由:** 併用薬の投与状況は、試験結果の解釈に影響を与える可能性があります。詳細な情報を収集し、安全性評価に役立てる必要があります。
    * **クエリNo.: 40**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.VISIT = "AE FOLLOW-UP", CM.CMDTC = "2014-01-21" (アスピリン、コルチゾン、LAC-HYDRIN、LIPITOR、チモプティック)
        *   **医療機関への問い合わせ文面:** AE FOLLOW-UP (2014-01-21) において、アスピリン、コルチゾン、LAC-HYDRIN、LIPITOR、チモプティックの併用が報告されています。これらの薬剤は、試験期間中に継続して投与されていたのか、それともAE FOLLOW-UP時に新たに投与が開始されたのかを明確にしてください。
        *   **判断理由:** 併用薬の投与状況は、試験結果の解釈に影響を与える可能性があります。特に、AE FOLLOW-UP時に新たに投与が開始された薬剤がある場合は、その理由と有害事象との関連性を評価する必要があります。
    * **クエリNo.: 41**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.VISIT = "AE FOLLOW-UP", CM.CMDTC = NULL (アスピリン、コルチゾン、LAC-HYDRIN、LIPITOR、チモプティック)
        *   **医療機関への問い合わせ文面:** AE FOLLOW-UP (2014-01-21) において、アスピリン、コルチゾン、LAC-HYDRIN、LIPITOR、チモプティックの併用が報告されていますが、CMDTCがNULLとなっています。これらの薬剤の正確な投与日を報告してください。
        *   **判断理由:** 併用薬の投与状況は、試験結果の解釈に影響を与える可能性があります。特に、AE FOLLOW-UP時に新たに投与が開始された薬剤がある場合は、その理由と有害事象との関連性を評価する必要があります。
    * **クエリNo.: 42**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.VISITNUM = 101 (アスピリン、コルチゾン、LAC-HYDRIN、LIPITOR、チモプティック)
        *   **医療機関への問い合わせ文面:** VISITNUM = 101 (AE FOLLOW-UP) は、Define.xmlで定義されたVISITNUMのコードリストに存在しません。VISITNUM = 101がAE FOLLOW-UPに対応することを確認し、Define.xmlの不備を修正してください。
        *   **判断理由:** Define.xmlは、データの構造を定義する重要なメタデータファイルです。コードリストの不備は、データの解釈や解析に影響を与える可能性があるため、修正が必要です。
    * **クエリNo.: 43**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** SV.VISIT = "AE FOLLOW-UP", SV.SVSTDTC = "201
## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM, LB, AE, QS, RELREC

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** CM.CMTRT = "CORTISONE", CM.CMDECOD = "UNCODED", CM.CMINDC = "", CM.CMCLAS = "UNCODED"
    *   **矛盾の内容:** CMドメインにおいて、CORTISONEの標準化された医薬品名(CMDECOD)、適応症(CMINDC)、医薬品分類(CMCLAS)が"UNCODED"または空欄となっている。これは、併用薬情報が適切にコード化されていないことを示している。
    *   **問題点の原因（推測）:** データ入力時に適切なコードが選択されなかった、またはコード化するための情報が不足していた可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、CORTISONEの具体的な製品名、適応症、医薬品分類を確認し、適切なコードを割り当てる。

*   **問題No.2:**
    *   **変数名と値:** CM.CMTRT = "LAC-HYDRIN", CM.CMDECOD = "UNCODED", CM.CMINDC = "", CM.CMCLAS = "UNCODED", CM.CMDOSE = null, CM.CMDOSU = ""
    *   **矛盾の内容:** CMドメインにおいて、LAC-HYDRINの標準化された医薬品名(CMDECOD)、適応症(CMINDC)、医薬品分類(CMCLAS)、投与量(CMDOSE)、投与単位(CMDOSU)が"UNCODED"、空欄、またはnullとなっている。これは、併用薬情報が不完全であることを示している。
    *   **問題点の原因（推測）:** データ入力時に必要な情報が入力されなかった、または情報が不足していた可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、LAC-HYDRINの具体的な製品名、適応症、医薬品分類、投与量、投与単位を確認し、適切な値を入力する。

*   **問題No.3:**
    *   **変数名と値:** LB.LBTESTCD = "COLOR", LB.LBORRES = "N", LB.LBORRESU = "NO UNITS", LB.LBSTRESC = "N", LB.LBSTRESN = null
    *   **矛盾の内容:** LBドメインの尿検査項目COLORにおいて、オリジナル単位(LBORRESU)が"NO UNITS"であるにも関わらず、文字結果(LBORRES, LBSTRESC)が"N"となっている。Define.xmlでは、COLORはCodeListを持つ変数として定義されているはずである。
    *   **問題点の原因（推測）:** データ入力時に、CodeListに基づいた選択肢が選択されず、自由記述で"N"と入力された可能性がある。または、Define.xmlの定義が不適切である可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、尿検査項目COLORの結果をCodeListに基づいた選択肢（例えば、"YELLOW", "STRAW", "AMBER"など）で再報告するよう依頼する。Define.xmlのCodeList定義も確認し、必要に応じて修正する。

*   **問題No.4:**
    *   **変数名と値:** LB.LBTESTCD = "KETONES", LB.LBORRES = "0", LB.LBORRESU = "NO UNITS", LB.LBSTRESC = "0", LB.LBSTRESN = 0
    *   **矛盾の内容:** LBドメインの尿検査項目KETONESにおいて、オリジナル単位(LBORRESU)が"NO UNITS"であるにも関わらず、文字結果(LBORRES, LBSTRESC)が"0"となっている。Define.xmlでは、KETONESはCodeListを持つ変数として定義されているはずである。
    *   **問題点の原因（推測）:** データ入力時に、CodeListに基づいた選択肢が選択されず、数値"0"が入力された可能性がある。または、Define.xmlの定義が不適切である可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、尿検査項目KETONESの結果をCodeListに基づいた選択肢（例えば、"NEGATIVE", "TRACE", "SMALL", "MODERATE", "LARGE"など）で再報告するよう依頼する。Define.xmlのCodeList定義も確認し、必要に応じて修正する。

*   **問題No.5:**
    *   **変数名と値:** LB.LBTESTCD = "UROBIL", LB.LBORRES = "0", LB.LBORRESU = "NO UNITS", LB.LBSTRESC = "0", LB.LBSTRESN = 0
    *   **矛盾の内容:** LBドメインの尿検査項目UROBILにおいて、オリジナル単位(LBORRESU)が"NO UNITS"であるにも関わらず、文字結果(LBORRES, LBSTRESC)が"0"となっている。Define.xmlでは、UROBILはCodeListを持つ変数として定義されているはずである。
    *   **問題点の原因（推測）:** データ入力時に、CodeListに基づいた選択肢が選択されず、数値"0"が入力された可能性がある。または、Define.xmlの定義が不適切である可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、尿検査項目UROBILの結果をCodeListに基づいた選択肢（例えば、"NORMAL", "SMALL", "MODERATE", "LARGE"など）で再報告するよう依頼する。Define.xmlのCodeList定義も確認し、必要に応じて修正する。

*   **問題No.6:**
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AELLT = "APPLICATION SITE RASH", AE.AEDECOD = "APPLICATION SITE DERMATITIS"
    *   **矛盾の内容:** AEドメインにおいて、有害事象"APPLICATION SITE DERMATITIS"に対して、報告された用語(AETERM)と標準化された用語(AEDECOD)が同じであるにも関わらず、低位語(AELLT)が"APPLICATION SITE RASH"となっている。MedDRAコーディングの整合性がとれていない。
    *   **問題点の原因（推測）:** MedDRAコーディング時に、適切な低位語が選択されなかった可能性がある。
    *   **対応策（提案）:** MedDRAコーディング担当者に連絡し、AELLTを"APPLICATION SITE DERMATITIS"に修正するよう依頼する。

*   **問題No.7:**
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE PRURITUS", AE.AELLT = "APPLICATION SITE ITCHING", AE.AEDECOD = "APPLICATION SITE PRURITUS"
    *   **矛盾の内容:** AEドメインにおいて、有害事象"APPLICATION SITE PRURITUS"に対して、報告された用語(AETERM)と標準化された用語(AEDECOD)が同じであるにも関わらず、低位語(AELLT)が"APPLICATION SITE ITCHING"となっている。MedDRAコーディングの整合性がとれていない。
    *   **問題点の原因（推測）:** MedDRAコーディング時に、適切な低位語が選択されなかった可能性がある。
    *   **対応策（提案）:** MedDRAコーディング担当者に連絡し、AELLTを"APPLICATION SITE PRURITUS"に修正するよう依頼する。

*   **問題No.8:**
    *   **変数名と値:** AE.AETERM = "BIOPSY PROSTATE", AE.AELLT = "BIOPSY OF PROSTATE", AE.AEDECOD = "BIOPSY PROSTATE"
    *   **矛盾の内容:** AEドメインにおいて、有害事象"BIOPSY PROSTATE"に対して、報告された用語(AETERM)、低位語(AELLT)、標準化された用語(AEDECOD)がすべて異なる表現になっている。MedDRAコーディングの整合性がとれていない。
    *   **問題点の原因（推測）:** MedDRAコーディング時に、適切な用語が選択されなかった可能性がある。
    *   **対応策（提案）:** MedDRAコーディング担当者に連絡し、AETERM, AELLT, AEDECODを統一するよう依頼する。

*   **問題No.9:**
    *   **変数名と値:** RELREC
    *   **矛盾の内容:** RELRECドメインにおいて、AEドメインのAESEQ=4とAESEQ=7のレコードが、同じRELID="01-703-1076-E08"で関連付けられている。しかし、これらのレコードはAETERMが異なり（APPLICATION SITE PRURITUSとAPPLICATION SITE DERMATITIS）、異なる有害事象である可能性が高い。
    *   **問題点の原因（推測）:** RELRECドメインのRELIDの割り当てが不適切である可能性がある。
    *   **対応策（提案）:** RELRECドメインのRELIDの割り当てルールを確認し、必要に応じて修正する。異なる有害事象には異なるRELIDを割り当てるべきである。

*   **問題No.10:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM19", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM19において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM19の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.11:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM20", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM20において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM20の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.12:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM20", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM20において、WEEK12のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM20の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.13:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM31", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM31において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM31の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.14:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM31", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM31において、WEEK12のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM31の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.15:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM37", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM37において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM37の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.16:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM37", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM37において、WEEK12のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM37の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.17:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM38", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM38において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM38の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.18:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM38", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM38において、WEEK12のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM38の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.19:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM39", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM39において、WEEK8のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM39の結果を"YES"または"NO"で再報告するよう依頼する。

*   **問題No.20:**
    *   **変数名と値:** QS.QSTESTCD = "DAITM39", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
    *   **矛盾の内容:** QSドメインのDAD, DAITM39において、WEEK12のデータでQSORRESが"N"、QSSTRESCが"0"となっている。DADの質問項目は"YES"または"NO"で回答されるべきであり、数値"0"は不適切である。
    *   **問題点の原因（推測）:** データ入力時に、"NO"の代わりに数値"0"が入力された可能性がある。
    *   **対応策（提案）:** 医療機関に問い合わせ、DAD, DAITM39の結果を"YES"または"NO"で再報告するよう依頼する。

**Define.xmlの修正候補:**

*   CM.CMDECOD, CM.CMINDC, CM.CMCLAS: CodeListの定義が不足している可能性がある。適切なCodeListを定義し、参照するように修正する。
*   LB.LBTESTCD = "COLOR", "KETONES", "UROBIL": LBORRESU="NO UNITS"となっているが、文字結果が入力されている。CodeListを定義し、LBORRES, LBSTRESCがCodeListから選択されるように修正する。

**クエリ:**

*   **患者ID:** 01-703-1076
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "CORTISONE", CM.CMDECOD = "UNCODED", CM.CMINDC = "", CM.CMCLAS = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬CORTISONEについて、具体的な製品名、適応症、医薬品分類を教えてください。
        *   **判断理由:** 併用薬情報は、患者の安全性評価および有効性評価に影響を与える可能性があるため、正確な情報が必要である。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "LAC-HYDRIN", CM.CMDECOD = "UNCODED", CM.CMINDC = "", CM.CMCLAS = "UNCODED", CM.CMDOSE = null, CM.CMDOSU = ""
        *   **医療機関への問い合わせ文面:** 併用薬LAC-HYDRINについて、具体的な製品名、適応症、医薬品分類、投与量、投与単位を教えてください。
        *   **判断理由:** 併用薬情報は、患者の安全性評価および有効性評価に影響を与える可能性があるため、正確な情報が必要である。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD = "COLOR", LB.LBORRES = "N", LB.LBORRESU = "NO UNITS"
        *   **医療機関への問い合わせ文面:** 尿検査項目COLORの結果を、"YELLOW", "STRAW", "AMBER"などの選択肢から選んで再報告してください。
        *   **判断理由:** 尿検査の結果は、患者の健康状態を評価するための重要な情報であり、CodeListに基づいた標準化された形式で報告される必要がある。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD = "KETONES", LB.LBORRES = "0", LB.LBORRESU = "NO UNITS"
        *   **医療機関への問い合わせ文面:** 尿検査項目KETONESの結果を、"NEGATIVE", "TRACE", "SMALL", "MODERATE", "LARGE"などの選択肢から選んで再報告してください。
        *   **判断理由:** 尿検査の結果は、患者の健康状態を評価するための重要な情報であり、CodeListに基づいた標準化された形式で報告される必要がある。

    *   **クエリNo.5:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD = "UROBIL", LB.LBORRES = "0", LB.LBORRESU = "NO UNITS"
        *   **医療機関への問い合わせ文面:** 尿検査項目UROBILの結果を、"NORMAL", "SMALL", "MODERATE", "LARGE"などの選択肢から選んで再報告してください。
        *   **判断理由:** 尿検査の結果は、患者の健康状態を評価するための重要な情報であり、CodeListに基づいた標準化された形式で報告される必要がある。

    *   **クエリNo.6:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM19", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM19(軽食の準備)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.7:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM20", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM20(軽食の調理)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.8:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM20", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM20(軽食の調理)について、WEEK12の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.9:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM31", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM31(請求書の支払い)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.10:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM31", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM31(請求書の支払い)について、WEEK12の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.11:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM37", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM37(家事への関心)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.12:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM37", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM37(家事への関心)について、WEEK12の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.13:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM38", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM38(家事の計画と組織化)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.14:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM38", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM38(家事の計画と組織化)について、WEEK12の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.15:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM39", QS.VISIT = "WEEK 8", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM39(家事の完了)について、WEEK8の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

    *   **クエリNo.16:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "DAITM39", QS.VISIT = "WEEK 12", QSORRES = "N", QSSTRESC = "0"
        *   **医療機関への問い合わせ文面:** DADのDAITM39(家事の完了)について、WEEK12の結果を"YES"または"NO"で再報告してください。
        *   **判断理由:** DADは"YES"または"NO"で回答される質問票であり、数値"0"は不適切である。

## Task3: Protocol Deviation Review Results
**1. プロトコル逸脱の検出**

**患者ID: 01-703-1076**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE", DM.AGE = 69, DM.SEX = "M"
    *   **逸脱内容:** 被験者はアルツハイマー病と診断されており、年齢が69歳、男性である。プロトコルでは、被験者は「50歳以上の男性および閉経後の女性」と規定されているが、アルツハイマー病の診断は除外基準に該当しない。しかし、プロトコル 3.4.2.1. Inclusion Criteria [2] には「NINCDSおよびADRDAガイドラインで定義されるprobable ADの診断」とあり、提供されたJSONデータにはNINCDS/ADRDAガイドラインに準拠しているかどうかの情報がない。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [1], [2]
    *   **判断理由:** JSONデータのDMドメイン、MHドメインの情報からは、プロトコルの選択基準を満たしているように見えるが、アルツハイマー病の診断がNINCDS/ADRDAガイドラインに準拠しているかどうかの情報が不足しているため、選択基準違反の可能性がある。

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DM.ARMCD = "Xan_Hi", EX.EXTRT = "XANOMELINE", EX.EXDOSE = 54, EX.EXDOSU = "mg", EX.EXSTDTC = "2013-10-25", EX.EXENDTC = "2013-11-06", EX.EXDOSFRQ = "QD"
    *   **逸脱内容:** 治験薬Xanomelineが54mg、1日1回(QD)投与されている。プロトコル3.6.2項では、「すべての患者は50cm2 TTS Formulation Eで開始される」と規定されている。しかし、提供されたJSONデータのEXドメインでは、最初の投与量が54mgとなっている。
    *   **プロトコル該当箇所:** 3.6.2 TTS Administration Procedures
    *   **判断理由:** プロトコルでは、最初の投与量は50cm2 TTS Formulation Eと規定されているが、JSONデータのEXドメインでは54mgとなっているため、投与量違反と判断した。

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "LOPID", CM.CMSTDTC = "2013-08-31", CM.CMENDTC = "2013-11-27"
    *   **逸脱内容:** 被験者はLOPIDを2013-08-31から2013-11-27まで使用している。プロトコル3.4.2.2 Exclusion Criteria [31] では、特定の薬剤の使用を除外基準としており、併用禁止薬のリストが提示されている。LOPIDがこのリストに含まれているかどうかが不明である。
    *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [31]
    *   **判断理由:** LOPIDがプロトコルで規定された併用禁止薬に該当するかどうかが不明であるため、併用禁止薬の使用に該当する可能性がある。

*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "MEVACOR", CM.CMSTDTC = "2013-11-28", CM.CMENDTC = "2013-12-12"
    *   **逸脱内容:** 被験者はMEVACORを2013-11-28から2013-12-12まで使用している。プロトコル3.4.2.2 Exclusion Criteria [31] では、特定の薬剤の使用を除外基準としており、併用禁止薬のリストが提示されている。MEVACORがこのリストに含まれているかどうかが不明である。
    *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [31]
    *   **判断理由:** MEVACORがプロトコルで規定された併用禁止薬に該当するかどうかが不明であるため、併用禁止薬の使用に該当する可能性がある。

*   **逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AESTDTC = "2013-11-23"
    *   **逸脱内容:** 2013-11-23に発現した有害事象「APPLICATION SITE DERMATITIS」が報告されている。プロトコル3.9.3.4. Safety Monitoringには、皮膚の発疹に関するフォローアップの指示があるが、フォローアップの実施状況が不明である。
    *   **プロトコル該当箇所:** 3.9.3.4. Safety Monitoring
    *   **判断理由:** 有害事象「APPLICATION SITE DERMATITIS」が報告されているが、プロトコルで指示されている皮膚の発疹に関するフォローアップが実施されたかどうかが不明である。

*   **逸脱No.: 6**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2013-11-23"
    *   **逸脱内容:** 2013-11-23に発現した有害事象「APPLICATION SITE PRURITUS」が報告されている。プロトコル3.9.3.4. Safety Monitoringには、皮膚の発疹に関するフォローアップの指示があるが、フォローアップの実施状況が不明である。
    *   **プロトコル該当箇所:** 3.9.3.4. Safety Monitoring
    *   **判断理由:** 有害事象「APPLICATION SITE PRURITUS」が報告されているが、プロトコルで指示されている皮膚の発疹に関するフォローアップが実施されたかどうかが不明である。

*   **逸脱No.: 7**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "HYPERHIDROSIS", AE.AESTDTC = "2013-11-25"
    *   **逸脱内容:** 2013-11-25に発現した有害事象「HYPERHIDROSIS」が報告されている。プロトコル3.9.3.4. Safety Monitoringには、多汗症に関するフォローアップの指示があるが、フォローアップの実施状況が不明である。
    *   **プロトコル該当箇所:** 3.9.3.4. Safety Monitoring
    *   **判断理由:** 有害事象「HYPERHIDROSIS」が報告されているが、プロトコルで指示されている多汗症に関するフォローアップが実施されたかどうかが不明である。

**2. クエリの作成**

**患者ID: 01-703-1076**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE"
    *   **医療機関への問い合わせ文面:** アルツハイマー病の診断は、NINCDS/ADRDAガイドラインに準拠していますか？診断の根拠となった具体的な検査結果（MMSEスコア、画像診断結果など）を提示してください。
    *   **判断理由:** プロトコル3.4.2.1 Inclusion Criteria [2] では、NINCDS/ADRDAガイドラインに基づくアルツハイマー病の診断が選択基準として規定されている。JSONデータには、この基準を満たしているかどうかの情報が含まれていないため、確認が必要である。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXTRT = "XANOMELINE", EX.EXDOSE = 54, EX.EXDOSU = "mg", EX.EXSTDTC = "2013-10-25"
    *   **医療機関への問い合わせ文面:** 治験薬Xanomelineの初回投与量が54mgとなっていますが、これはプロトコル3.6.2項で規定されている50cm2 TTS Formulation Eと異なります。54mgを投与した理由を説明してください。
    *   **判断理由:** プロトコル3.6.2項では、初回投与量は50cm2 TTS Formulation Eと規定されているが、JSONデータでは54mgとなっているため、確認が必要である。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "LOPID", CM.CMSTDTC = "2013-08-31"
    *   **医療機関への問い合わせ文面:** LOPIDはプロトコル3.4.2.2 Exclusion Criteria [31] の併用禁止薬リストに含まれていますか？含まれている場合、なぜ使用されたのですか？
    *   **判断理由:** プロトコル3.4.2.2 Exclusion Criteria [31] では、特定の薬剤の使用が除外基準として規定されている。LOPIDがこのリストに含まれているか、含まれている場合に投与された理由を確認する必要がある。

*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMTRT = "MEVACOR", CM.CMSTDTC = "2013-11-28"
    *   **医療機関への問い合わせ文面:** MEVACORはプロトコル3.4.2.2 Exclusion Criteria [31] の併用禁止薬リストに含まれていますか？含まれている場合、なぜ使用されたのですか？
    *   **判断理由:** プロトコル3.4.2.2 Exclusion Criteria [31] では、特定の薬剤の使用が除外基準として規定されている。MEVACORがこのリストに含まれているか、含まれている場合に投与された理由を確認する必要がある。

*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE DERMATITIS", AE.AESTDTC = "2013-11-23"
    *   **医療機関への問い合わせ文面:** 有害事象「APPLICATION SITE DERMATITIS」について、プロトコル3.9.3.4に記載されている皮膚の発疹に関するフォローアップは実施されましたか？実施された場合、その結果を提示してください。
    *   **判断理由:** プロトコル3.9.3.4では、皮膚の発疹に関するフォローアップが指示されているが、実施状況が不明であるため、確認が必要である。

*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2013-11-23"
    *   **医療機関への問い合わせ文面:** 有害事象「APPLICATION SITE PRURITUS」について、プロトコル3.9.3.4に記載されている皮膚の発疹に関するフォローアップは実施されましたか？実施された場合、その結果を提示してください。
    *   **判断理由:** プロトコル3.9.3.4では、皮膚の発疹に関するフォローアップが指示されているが、実施状況が不明であるため、確認が必要である。

*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "HYPERHIDROSIS", AE.AESTDTC = "2013-11-25"
    *   **医療機関への問い合わせ文面:** 有害事象「HYPERHIDROSIS」について、プロトコル3.9.3.4に記載されている多汗症に関するフォローアップは実施されましたか？実施された場合、その結果を提示してください。
    *   **判断理由:** プロトコル3.9.3.4では、多汗症に関するフォローアップが指示されているが、実施状況が不明であるため、確認が必要である。


# 01-703-1096
## Task1: Clinical Review Results
**症例サマリー:**

**患者ID: 01-703-1096**

*   2012年12月5日 (Day -51): スクリーニング検査。アルブミン 3.7 g/dL (基準範囲 3.5-4.6 g/dL), ALP 98 U/L (基準範囲 35-115 U/L), ALT 12 U/L (基準範囲 6-32 U/L), AST 20 U/L (基準範囲 9-34 U/L), ビリルビン 0.5 mg/dL (基準範囲 0.2-1.2 mg/dL), BUN 11 mg/dL (基準範囲 4-24 mg/dL), カルシウム 8.6 mg/dL (基準範囲 8.4-10.3 mg/dL), コレステロール 195 mg/dL (基準範囲 156-300 mg/dL), CK 101 U/L (基準範囲 21-169 U/L), クレアチニン 0.9 mg/dL (基準範囲 0.7-1.4 mg/dL)。
*   2012年12月19日 (Day -37): スクリーニング1。身長 160.02 cm, 体重 81.65 kg, 収縮期血圧 132 mmHg (臥位), 拡張期血圧 74 mmHg (臥位), 脈拍 78 bpm (臥位)。教育レベル6年。既往歴にアルツハイマー病 (2006年12月20日発症)、難聴 (発症日不明, 軽度)。Modified Hachinski Ischemic Score 0点。MMSE 17点。
*   2013年1月23日 (Day -2): スクリーニング2。収縮期血圧 140 mmHg (臥位), 拡張期血圧 82 mmHg (臥位), 脈拍 58 bpm (臥位)。
*   2013年1月25日 (Day 1): ベースライン。プラセボ投与開始。収縮期血圧 142 mmHg (臥位), 拡張期血圧 70 mmHg (臥位), 脈拍 74 bpm (臥位)。体重 81.19 kg。ADAS-Cog(11) 16点。NPI-X合計スコア 13点。
*   2013年2月8日 (Day 15): Ambulatory ECG 装着。収縮期血圧 150 mmHg (臥位), 拡張期血圧 80 mmHg (臥位), 脈拍 78 bpm (臥位)。
*   2013年2月9日 (Day 16): Week 2。収縮期血圧 140 mmHg (臥位), 拡張期血圧 74 mmHg (臥位), 脈拍 66 bpm (臥位)。体重 80.74 kg。NPI-X合計スコア 10点。
*   2013年2月23日 (Day 30): Week 4。収縮期血圧 150 mmHg (臥位), 拡張期血圧 80 mmHg (臥位), 脈拍 78 bpm (臥位)。体重 83.92 kg。NPI-X合計スコア 13点。
*   2013年2月27日 (Day 34): Ambulatory ECG 除去。収縮期血圧 140 mmHg (臥位), 拡張期血圧 80 mmHg (臥位), 脈拍 68 bpm (臥位)。
*   2013年3月29日 (Day 64): Week 6。追跡不能 (連絡不能) のため試験中止。

**クエリ:**

**患者ID: 01-703-1096**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSDECOD = "LOST TO FOLLOW-UP"
    *   **医療機関への問い合わせ文面:** 患者が追跡不能 (連絡不能) となった具体的な状況、最後に患者と連絡が取れた日時、連絡を試みた方法とその回数、患者の安否に関する情報 (可能な範囲で) を詳細に教えてください。
    *   **判断理由:** 患者が追跡不能となった理由は、試験結果の解釈、特に安全性評価に影響を与える可能性があるため、詳細な情報が必要である。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHSTDTC = "" (空欄)
    *   **医療機関への問い合わせ文面:** 既往歴「難聴」の発症日を可能な範囲で特定し、日付をYYYY-MM-DD形式で報告してください。日付が不明な場合は、おおよその時期（例：2000年頃、1995年夏）を記載してください。
    *   **判断理由:** 既往歴の発症日は、有害事象との関連性を評価する上で参考になる場合がある。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "COLOR", LB.LBORRES = "N", LB.LBSTRESC = "N"
    *   **医療機関への問い合わせ文面:** スクリーニング時 (Visit 1) および非定期来院1.3 (Visit 1.3) の尿検査 (COLOR) の結果が "N" (Normal) と報告されていますが、具体的な色調 (例: Yellow, Straw, Amber) を教えてください。
    *   **判断理由:** 尿の色調は、脱水や肝機能障害などの指標となる場合があるため、具体的な色調を確認する必要がある。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "KETONES", LB.LBORRES = "0", LB.LBSTRESC = "0"
    *   **医療機関への問い合わせ文面:** スクリーニング時 (Visit 1) および非定期来院1.3 (Visit 1.3) の尿検査 (KETONES) の結果が "0" と報告されていますが、具体的な結果 (例: Negative, Trace, Small, Moderate, Large) を教えてください。
    *   **判断理由:** 尿中ケトン体は、糖尿病や飢餓状態などの指標となる場合があるため、具体的な結果を確認する必要がある。
*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "UROBIL", LB.LBORRES = "0", LB.LBSTRESC = "0"
    *   **医療機関への問い合わせ文面:** スクリーニング時 (Visit 1) および非定期来院1.3 (Visit 1.3) の尿検査 (UROBIL) の結果が "0" と報告されていますが、具体的な結果 (例: Normal, Small, Moderate, Large) を教えてください。
    *   **判断理由:** 尿中ウロビリノーゲンは、肝機能障害や溶血性貧血などの指標となる場合があるため、具体的な結果を確認する必要がある。

## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: LB (LBTMSHI), MH (MHDECOD, MHLLT, MHHLT, MHHLGT, MHBODSYS), QS (QSTESTCD=CIBIC, NPITM01S, NPITM02S, NPITM03S, NPITM04S, NPITM05S, NPITM06S, NPITM07S, NPITM08S, NPITM09S, NPITM10S, NPITM11S, NPITM12S, NPTOT)

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** LB.LBTESTCD = "ALB", "ALP", "ALT", "AST", "BASO", "BILI", "BUN", "CA", "CHOL", "CK", "CL", "CREAT", "EOS", "GGT", "GLUC", "HCT", "HGB", "K", "LYM", "MCH", "MCHC", "MCV", "MONO", "PHOS", "PLAT", "PROT", "RBC", "SODIUM", "TSH", "URATE", "WBC" の SUPPBL.QNAM = "LBTMSHI"
    *   **矛盾の内容:** SUPPBL.QNAM = "LBTMSHI" は、Define.xml で "LAB RESULT/UPPER LIMIT OF NORMAL" と定義されていますが、SUPPLB.QVAL には様々な値 (例: "0.8", "0.9", "0.4", "0.6") が記録されており、上限値に統一されていません。
    *   **問題点の原因（推測）:** SUPPLB.QNAM = "LBTMSHI" の定義が誤っているか、データ入力時に誤った変数が選択された可能性があります。
    *   **対応策（提案）:** SUPPLB.QNAM = "LBTMSHI" の定義を再確認し、必要に応じて修正します。データ入力者に、正しい変数を選択するよう指示します。

*   **問題No.2:**
    *   **変数名と値:** MH.MHDECOD, MH.MHLLT, MH.MHHLT, MH.MHHLGT, MH.MHBODSYS
    *   **矛盾の内容:** MHドメインのMedDRA関連変数(MHDECOD, MHLLT, MHHLT, MHHLGT, MHBODSYS)に値が入力されていません。
    *   **問題点の原因（推測）:** MedDRAコーディングが実施されていない可能性があります。
    *   **対応策（提案）:** MedDRAコーディングを実施し、MHドメインのMedDRA関連変数を更新します。

*   **問題No.3:**
    *   **変数名と値:** QS.QSTESTCD = "CIBIC"
    *   **矛盾の内容:** QSドメインに CIBIC+ のデータが含まれていません。プロトコルでは、CIBIC+ は Visits 3, 8, 10, 12 で評価するとされています。
    *   **問題点の原因（推測）:** CIBIC+ のデータが収集されていないか、別のドメインに記録されている可能性があります。
    *   **対応策（提案）:** CIBIC+ のデータ収集状況を確認し、不足している場合は医療機関に問い合わせます。

*   **問題No.4:**
    *   **変数名と値:** QS.QSTESTCD = "NPITM01S", "NPITM02S", "NPITM03S", "NPITM04S", "NPITM05S", "NPITM06S", "NPITM07S", "NPITM08S", "NPITM09S", "NPITM10S", "NPITM11S", "NPITM12S", "NPTOT"
    *   **矛盾の内容:** NPI-Xのスコア (NPITMxxS, NPTOT) が、Define.xml で定義された計算方法と一致しない可能性があります。Define.xml では、「Total scores of "ALZHEIMER'S DISEASE ASSESSMENT SCALE" and "NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)" were derived as described in the SAP.」と記載されています。
    *   **問題点の原因（推測）:** NPI-Xのスコア計算方法が誤っているか、SAPに記載された計算方法と異なる可能性があります。
    *   **対応策（提案）:** SAPを参照し、NPI-Xのスコア計算方法を確認します。データと計算方法が一致しない場合は、データを修正します。

**クエリ:**

*   **患者ID:** 01-703-1096
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** MH.MHDECOD, MH.MHLLT, MH.MHHLT, MH.MHHLGT, MH.MHBODSYS
        *   **医療機関への問い合わせ文面:** MHドメインのMedDRA関連変数(MHDECOD, MHLLT, MHHLT, MHHLGT, MHBODSYS)に値が入力されていません。MedDRAコーディングを実施し、データを提供してください。
        *   **判断理由:** MHドメインはMedical Historyを記録する重要なドメインであり、MedDRAコーディングは標準化された用語で病歴を記録するために必須です。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "CIBIC"
        *   **医療機関への問い合わせ文面:** CIBIC+ のデータが QS ドメインに含まれていません。CIBIC+ の評価結果を提出してください。もし評価を実施していない場合は、その理由を説明してください。
        *   **判断理由:** CIBIC+ はプロトコルで規定された主要評価項目の一つであり、データが欠損していると主要評価項目の解析ができません。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM03S", VISIT = "BASELINE", QSORRES = "2", NPITM03F = "2", NPITM03V = "1"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM03" (AGITATION/AGRESSION)について、ベースライン時の頻度(NPITM03F)が"2"(週に約1回)、重症度(NPITM03V)が"1"(軽度)の場合、スコア(NPITM03S)は"2"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"2"と重症度"1"の積が"2"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM04S", VISIT = "WEEK 2", QSORRES = "1", NPITM04F = "1", NPITM04V = "1"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM04" (DEPRESSION/DYSPHORIA)について、WEEK 2時の頻度(NPITM04F)が"1"(週に1回未満)、重症度(NPITM04V)が"1"(軽度)の場合、スコア(NPITM04S)は"1"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"1"と重症度"1"の積が"1"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.5:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM05S", VISIT = "BASELINE", QSORRES = "4", NPITM05F = "2", NPITM05V = "2"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM05" (ANXIETY)について、ベースライン時の頻度(NPITM05F)が"2"(週に約1回)、重症度(NPITM05V)が"2"(中等度)の場合、スコア(NPITM05S)は"4"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"2"と重症度"2"の積が"4"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.6:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM07S", VISIT = "BASELINE", QSORRES = "3", NPITM07F = "3", NPITM07V = "1"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM07" (APATHY/INDIFFERENCE)について、ベースライン時の頻度(NPITM07F)が"3"(週に数回)、重症度(NPITM07V)が"1"(軽度)の場合、スコア(NPITM07S)は"3"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"3"と重症度"1"の積が"3"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.7:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM09S", VISIT = "BASELINE", QSORRES = "2", NPITM09F = "2", NPITM09V = "1"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM09" (IRRITABILITY/LABILITY)について、ベースライン時の頻度(NPITM09F)が"2"(週に約1回)、重症度(NPITM09V)が"1"(軽度)の場合、スコア(NPITM09S)は"2"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"2"と重症度"1"の積が"2"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.8:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPITM10S", VISIT = "BASELINE", QSORRES = "2", NPITM10F = "2", NPITM10V = "1"
        *   **医療機関への問い合わせ文面:** NPI-Xの質問項目"NPITM10" (ABERRANT MOTOR BEHAVIOR)について、ベースライン時の頻度(NPITM10F)が"2"(週に約1回)、重症度(NPITM10V)が"1"(軽度)の場合、スコア(NPITM10S)は"2"で正しいですか。もし正しくない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのスコアは、頻度と重症度の積で計算されると理解しています。提示されたデータでは、頻度"2"と重症度"1"の積が"2"と報告されており、計算が一致しているように見えますが、念のため確認します。

    *   **クエリNo.9:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPTOT", VISIT = "BASELINE", QSORRES = "13"
        *   **医療機関への問い合わせ文面:** NPI-Xのトータルスコア(NPTOT)について、ベースライン時の値が"13"と報告されています。これは、各質問項目のスコア(NPITM01S～NPITM12S)の合計値と一致しますか。もし一致しない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのトータルスコアは、各質問項目のスコアの合計値であると理解しています。提示されたデータと、個々の質問項目のスコアから計算される合計値が一致するか確認します。

    *   **クエリNo.10:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPTOT", VISIT = "WEEK 2", QSORRES = "10"
        *   **医療機関への問い合わせ文面:** NPI-Xのトータルスコア(NPTOT)について、WEEK 2時の値が"10"と報告されています。これは、各質問項目のスコア(NPITM01S～NPITM12S)の合計値と一致しますか。もし一致しない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのトータルスコアは、各質問項目のスコアの合計値であると理解しています。提示されたデータと、個々の質問項目のスコアから計算される合計値が一致するか確認します。

    *   **クエリNo.11:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = "NPTOT", VISIT = "WEEK 4", QSORRES = "13"
        *   **医療機関への問い合わせ文面:** NPI-Xのトータルスコア(NPTOT)について、WEEK 4時の値が"13"と報告されています。これは、各質問項目のスコア(NPITM01S～NPITM12S)の合計値と一致しますか。もし一致しない場合は、正しい値を報告してください。
        *   **判断理由:** NPI-Xのトータルスコアは、各質問項目のスコアの合計値であると理解しています。提示されたデータと、個々の質問項目のスコアから計算される合計値が一致するか確認します。

**Define.xmlの修正候補:**

*   SUPPLB.QNAM = "LBTMSHI" の CodeList を確認し、上限値のみを含むように修正するか、別の適切な定義に変更することを検討してください。
*   QS.QSTESTCD = "NPITM01S", "NPITM02S", "NPITM03S", "NPITM04S", "NPITM05S", "NPITM06S", "NPITM07S", "NPITM08S", "NPITM09S", "NPITM10S", "NPITM11S", "NPITM12S", "NPTOT" の計算方法を Define.xml の ComputationMethod に具体的に記述してください (例: NPITM03S = NPITM03F * NPITM03V)。

## Task3: Protocol Deviation Review Results
**1. プロトコル逸脱の検出**

**患者ID: 01-703-1096**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DM.AGE = 49, DM.AGEU = "YEARS"
    *   **逸脱内容:** 被験者の年齢が49歳であり、プロトコルで規定された年齢（50歳以上）を満たしていない。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria [1] Males and postmenopausal females at least 50 years of age.
    *   **判断理由:** DMドメインのAGEおよびAGEU変数の値から、被験者の年齢が49歳であることがわかる。これはプロトコルの選択基準に違反する。

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** QS.QSTESTCD = "MMITM05", QS.QSORRES = "0", QS.VISIT = "SCREENING 1"
    *   **逸脱内容:** スクリーニング時のMMSE検査における「3つの言葉の記銘」の得点(MMITM05)が0点であり、プロトコルで規定されたMMSEスコア(10点から23点)を満たさない可能性がある。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria [3] MMSE score of 10 to 23.
    *   **判断理由:** QSドメインのQSTESTCD, QSORRES, VISIT変数の値から、スクリーニング時のMMSE検査の一部である「3つの言葉の記銘」の得点が0点であることがわかる。MMSEの他の項目の得点が不明であるため、合計点がプロトコルの選択基準を満たさない可能性がある。

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBDY = -51, LB.VISIT = "SCREENING 1"
    *   **逸脱内容:** スクリーニング時の臨床検査(LB)の実施日が、参照開始日(DM.RFSTDTC = "2013-01-25")より51日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** LBドメインのLBDY変数およびDMドメインのRFSTDTC変数の値から、スクリーニング時の臨床検査が参照開始日の51日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DM.DMDY = -37, DM.VISIT = "SCREENING 1"
    *   **逸脱内容:** スクリーニング時のDMデータ収集日が、参照開始日(DM.RFSTDTC = "2013-01-25")より37日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** DMドメインのDMDYおよびRFSTDTC変数の値から、スクリーニング時のDMデータ収集が参照開始日の37日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

*   **逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSDY = -37, QS.VISIT = "SCREENING 1", QSTESTCD = "MHITM01" (Modified Hachinski Ischemic Score)
    *   **逸脱内容:** スクリーニング時のModified Hachinski Ischemic Score評価日が、参照開始日(DM.RFSTDTC = "2013-01-25")より37日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** QSドメインのQSDY変数およびDMドメインのRFSTDTC変数の値から、スクリーニング時のModified Hachinski Ischemic Score評価が参照開始日の37日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

*   **逸脱No.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSDY = -37, VS.VISIT = "SCREENING 1"
    *   **逸脱内容:** スクリーニング時のバイタルサイン測定日が、参照開始日(DM.RFSTDTC = "2013-01-25")より37日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** VSドメインのVSDY変数およびDMドメインのRFSTDTC変数の値から、スクリーニング時のバイタルサイン測定が参照開始日の37日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

*   **逸脱No.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** SC.SCDY = -37, SC.SCTESTCD = "EDLEVEL"
    *   **逸脱内容:** スクリーニング時の被験者の特性(SC)収集日が、参照開始日(DM.RFSTDTC = "2013-01-25")より37日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** SCドメインのSCDY変数およびDMドメインのRFSTDTC変数の値から、スクリーニング時の被験者の特性収集が参照開始日の37日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

*   **逸脱No.: 8**
    *   **変数名と値:** MH.MHDY = -37, MH.VISIT = "SCREENING 1"
    *   **逸脱内容:** スクリーニング時の病歴(MH)収集日が、参照開始日(DM.RFSTDTC = "2013-01-25")より37日前であり、プロトコルで規定されたスクリーニング期間（2週間以内）を超えている。
    *   **プロトコル該当箇所:** 3.1. Summary of Study Design The screening process should occur within 2 weeks of randomization (Visit 3 of the study).
    *   **判断理由:** MHドメインのMHDY変数およびDMドメインのRFSTDTC変数の値から、スクリーニング時の病歴収集が参照開始日の37日前に実施されたことがわかる。これはプロトコルのスクリーニング期間に関する記述に違反する。

**2. クエリの作成**

**患者ID: 01-703-1096**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DM.AGE = 49, DM.AGEU = "YEARS"
    *   **医療機関への問い合わせ文面:** 報告された被験者の年齢は49歳ですが、プロトコルでは50歳以上が選択基準となっています。被験者の年齢に誤りがないか確認してください。もし年齢が正しい場合、この被験者はプロトコル逸脱となります。
    *   **判断理由:** プロトコルの選択基準と報告された年齢が一致しないため。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** QS.QSTESTCD = "MMITM05", QS.QSORRES = "0", QS.VISIT = "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時のMMSE検査における「3つの言葉の記銘」(MMITM05)の得点が0点と報告されています。MMSEの合計点を確認してください。合計点が10点未満の場合、この被験者はプロトコル逸脱となります。
    *   **判断理由:** プロトコルの選択基準と報告されたMMSEの一部のスコアから、合計スコアが基準を満たさない可能性があるため。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBDY = -51, LB.VISIT = "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時の臨床検査(LB)が、参照開始日の51日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。この検査がスクリーニングとして適切であったか、再検査が必要か確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告された検査日が一致しないため。

*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DM.DMDY = -37, DM.VISIT = "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時のDMデータ収集が、参照開始日の37日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。このデータ収集がスクリーニングとして適切であったか確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告されたデータ収集日が一致しないため。

*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSDY = -37, QS.VISIT = "SCREENING 1", QSTESTCD = "MHITM01"
    *   **医療機関への問い合わせ文面:** スクリーニング時のModified Hachinski Ischemic Score評価が、参照開始日の37日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。この評価がスクリーニングとして適切であったか確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告された評価日が一致しないため。

*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSDY = -37, VS.VISIT = "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時のバイタルサイン測定が、参照開始日の37日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。この測定がスクリーニングとして適切であったか確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告された測定日が一致しないため。

*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** SC.SCDY = -37, SC.SCTESTCD = "EDLEVEL"
    *   **医療機関への問い合わせ文面:** スクリーニング時の被験者の特性収集が、参照開始日の37日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。このデータ収集がスクリーニングとして適切であったか確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告されたデータ収集日が一致しないため。

*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHDY = -37, MH.VISIT = "SCREENING 1"
    *   **医療機関への問い合わせ文面:** スクリーニング時の病歴収集が、参照開始日の37日前に実施されています。プロトコルではスクリーニング期間は2週間以内と規定されています。このデータ収集がスクリーニングとして適切であったか確認してください。
    *   **判断理由:** プロトコルのスクリーニング期間に関する記述と、報告されたデータ収集日が一致しないため。


# 01-704-1017
## Task1: Clinical Review Results
**1. 症例サマリー:**

**患者ID: 01-704-1017**

*   2013年09月20日 (Day -16): スクリーニング1。既往歴として、心疾患、性欲亢進、心電図ST上昇、心筋梗塞、心拍異常、大動脈バイパス術の既往あり。教育レベル12年。MMSEスコアは報告なし。Hachinski Ischemic Scaleスコアは0点。
*   2013年09月27日 (Day -9): スクリーニング2。
*   2013年10月06日 (Day 1): ベースライン。試験薬(Xanomeline High Dose)投与開始。ADAS-Cog(11) 27点、NPI-X 61点。DADは多くの項目で「いいえ」または「該当なし」。
*   2013年10月19日 (Day 14): Week 2。アルブミン 3.3 g/dL (低値)、BUN 29 mg/dL (高値)、クレアチニン 1.6 mg/dL (正常上限)。NPI-X 22点。試験薬(Xanomeline High Dose)増量。有害事象として心筋梗塞、心室中隔欠損発現。
*   2013年11月01日 (Day 27): Final Lab Visit。アルブミン 3.4 g/dL (低値)。
*   2013年11月05日 (Day 31): 有害事象として、そう痒症、発疹発現。
*   2013年11月09日 (Day 35): Week 4。NPI-X 38点。有害事象として、脳死、脳梗塞後遺症発現。
*   2013年11月18日 (Day 44): 有害事象として、脳死、脳梗塞後遺症の転帰は「回復/軽快」。
*   2013年11月19日 (Day 45): 有害事象として、心筋梗塞の転帰は「回復/軽快」。
*   2013年11月22日 (Day 48): 有害事象として、そう痒症、発疹の転帰は「回復/軽快」と「未回復/未軽快」の報告あり。
*   2013年11月24日 (Day 50): Week 6。ADAS-Cog(11) 30点、CIBIC+ 4点、NPI-X 16点。有害事象により試験中止。

**2. クエリ:**

**患者ID: 01-704-1017**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** AE.AETERM = "BRAIN DEATH", AE.AESDTH = "N"
    *   **医療機関への問い合わせ文面:** 有害事象として「脳死」が報告されていますが、死亡は否定されています(AESDTH = "N")。報告内容に矛盾がありますので、ご確認ください。
    *   **判断理由:** 患者の生死に関わる重大な有害事象であり、報告内容に矛盾があるため。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "LATE EFFECTS OF CEREBRAL INFRACTION", AE.AESEV = "SEVERE"
    *   **医療機関への問い合わせ文面:** 有害事象として「脳梗塞後遺症」が報告され、重症度が「重度」と評価されています。具体的な症状と経過について詳細な情報を提供してください。
    *   **判断理由:** 重大な有害事象であり、詳細な情報が必要なため。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "MYOCARDIAL INFARCTION", AE.AEREL = "NONE"
    *   **医療機関への問い合わせ文面:** 有害事象として「心筋梗塞」が報告されていますが、治験薬との因果関係が「なし」と評価されています。その根拠を説明してください。
    *   **判断理由:** 治験薬との因果関係評価は、安全性評価において重要であり、その根拠を確認する必要があるため。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "PRURITUS", AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" and "RECOVERED/RESOLVED"
    *   **医療機関への問い合わせ文面:** 同一の有害事象「そう痒症」に対して、「未回復/未軽快」と「回復/軽快」の相反する転帰が報告されています。正しい転帰を確認してください。
    *   **判断理由:** 有害事象の転帰は、安全性評価において重要であり、正確な情報が必要なため。
*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "RASH", AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" and "RECOVERED/RESOLVED"
    *   **医療機関への問い合わせ文面:** 同一の有害事象「発疹」に対して、「未回復/未軽快」と「回復/軽快」の相反する転帰が報告されています。正しい転帰を確認してください。
    *   **判断理由:** 有害事象の転帰は、安全性評価において重要であり、正確な情報が必要なため。
*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "CREAT", LB.LBORRES = "1.8" (2013-09-20), LB.LBNRIND = "HIGH"
    *   **医療機関への問い合わせ文面:** スクリーニング時のクレアチニン値が1.8 mg/dLであり、基準範囲上限(1.6 mg/dL)を超過しています。プロトコルでは除外基準に該当する可能性がありますが、選択基準抵触の有無についてご確認ください。
    *   **判断理由:** プロトコルでは除外基準に該当する可能性があるが、Define.xmlでは"If values exceed these laboratory reference ranges, clinical significance will be judged by the monitoring physicians. If the monitoring physician determines that the deviation from the reference range is not clinically significant, the patient may be included in the study."とされており、最終的には臨床的意義によって判断されるため。
*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHTERM = "LIBIDO INCREASED", MH.MHSEV = "MILD"
    *   **医療機関への問い合わせ文面:** 既往歴として「性欲亢進」が報告されていますが、具体的な症状と経過について詳細な情報を提供してください。
    *   **判断理由:** 症状の程度によっては、安全性評価に影響を与える可能性があるため。
*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHTERM = "ST SEGMENT ELEVATED", MH.MHSEV = "MILD"
    *   **医療機関への問い合わせ文面:** 既往歴として「ST上昇」が報告されていますが、具体的な症状と経過について詳細な情報を提供してください。
    *   **判断理由:** 症状の程度によっては、安全性評価に影響を与える可能性があるため。
*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHTERM = "ST SEGMENT DEPRESSED", MH.MHSEV = "MILD"
    *   **医療機関への問い合わせ文面:** 既往歴として「ST低下」が報告されていますが、具体的な症状と経過について詳細な情報を提供してください。
    *   **判断理由:** 症状の程度によっては、安全性評価に影響を与える可能性があるため。
*   **クエリNo.: 10**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MH.MHTERM = "SKIPPED BEATS", MH.MHSEV = "MILD"
    *   **医療機関への問い合わせ文面:** 既往歴として「心拍異常」が報告されていますが、具体的な症状と経過について詳細な情報を提供してください。
    *   **判断理由:** 症状の程度によっては、安全性評価に影響を与える可能性があるため。
*   **クエリNo.: 11**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT = "PREMARIN", CM.CMDOSE = 0.625, CM.CMDOSU = "mg", CM.CMDOSFRQ = "QOD"
    *   **医療機関への問い合わせ文面:** 併用薬としてPREMARINが報告されていますが、投与頻度がQOD(隔日投与)となっています。プロトコルでは、エストロゲン補充療法は安定した用量での投与が許容されていますが、隔日投与は安定した用量とみなされますか？
    *   **判断理由:** プロトコルとの整合性を確認するため。

## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: AE, DS, CM, LB, QS, RELREC

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** AE.AEOUT = "RECOVERED/RESOLVED", AE.AEENDTC = "2013-11-18" (AESEQ=3); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
    *   **矛盾の内容:** AE (AESEQ=3) は「回復/解決」と報告されているが、同日に別の有害事象 (DS.DSTERM = "ADVERSE EVENT") により試験を中止している。AEの転帰とDSの終了理由に矛盾がある。
    *   **問題点の原因（推測）:** AEの転帰の入力ミス、またはDSの終了理由の入力ミスの可能性がある。
    *   **対応策（提案）:** AEの転帰とDSの終了理由について、医療機関に確認する。

*   **問題No.2:**
    *   **変数名と値:** AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AEENDTC = "" (AESEQ=2); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
    *   **矛盾の内容:** AE (AESEQ=2) は「未回復/未解決」かつ終了日が欠損しているが、同日に別の有害事象 (DS.DSTERM = "ADVERSE EVENT") により試験を中止している。AEの転帰とDSの終了理由に矛盾がある。
    *   **問題点の原因（推測）:** AEの転帰の入力ミス、AE終了日の入力漏れ、またはDSの終了理由の入力ミスの可能性がある。
    *   **対応策（提案）:** AEの転帰、AE終了日、DSの終了理由について、医療機関に確認する。

*   **問題No.3:**
    *   **変数名と値:** AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AEENDTC = "" (AESEQ=8); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
    *   **矛盾の内容:** AE (AESEQ=8) は「未回復/未解決」かつ終了日が欠損しているが、同日に別の有害事象 (DS.DSTERM = "ADVERSE EVENT") により試験を中止している。AEの転帰とDSの終了理由に矛盾がある。
    *   **問題点の原因（推測）:** AEの転帰の入力ミス、AE終了日の入力漏れ、またはDSの終了理由の入力ミスの可能性がある。
    *   **対応策（提案）:** AEの転帰、AE終了日、DSの終了理由について、医療機関に確認する。

*   **問題No.4:**
    *   **変数名と値:** CM.CMTRT = "ASPIRIN", CM.CMSTDTC = "2000", CM.CMENDTC = ""
    *   **矛盾の内容:** アスピリンの投与開始日が2000年と報告されているが、これは試験開始のかなり前であり、不自然である。また、終了日が欠損している。
    *   **問題点の原因（推測）:** 投与開始日の入力ミス、または併用薬の記録方法に誤りがある可能性がある。
    *   **対応策（提案）:** アスピリンの投与開始日と終了日について、医療機関に確認する。

*   **問題No.5:**
    *   **変数名と値:** LB.LBTESTCD = "CREAT", LB.LBORRES = "1.8", LB.LBNRIND = "HIGH" (LBSEQ=13); DM.SEX = "M"
    *   **矛盾の内容:** スクリーニング時のクレアチニン値が1.8 mg/dLで「高値」と報告されている。男性(DM.SEX = "M")の場合、プロトコルで定義された除外基準 (EXCL27) に該当する可能性がある。
    *   **問題点の原因（推測）:** 基準範囲の設定ミス、または被験者の選択基準の確認漏れの可能性がある。
    *   **対応策（提案）:** スクリーニング時のクレアチニン値が除外基準に該当するかどうか、医療機関に確認する。

*   **問題No.6:**
    *   **変数名と値:** QS.QSTESTCD = "NPITM11F", QS.VISIT = "WEEK 4", QS.QSDTC = "2013-11-09" (QSSEQ=3113)
    *   **矛盾の内容:** NPI-Xの"NIGHT-TIME BEHAVIOR FREQUENCY" (NPITM11F) がWEEK 4 (2013-11-09) に評価されているが、SVドメインによると、WEEK4のVISITは2013-11-09ではなく、2013-11-01である。
    *   **問題点の原因（推測）:** QS.QSDTCの入力ミス、またはデータ収集日の記録ミス。
    *   **対応策（提案）:** NPI-Xの評価日について、医療機関に確認する。

*   **問題No.7:**
    *   **変数名と値:** RELREC.RELTYPE = ""
    *   **矛盾の内容:** RELRECドメインのRELTYPEが全て空欄になっている。
    *   **問題点の原因（推測）:** RELRECドメインのデータ入力規則の誤り、またはデータ入力漏れ。
    *   **対応策（提案）:** RELRECドメインのRELTYPEの入力規則を確認し、データ入力を修正する。

*   **問題No.8:**
    *   **変数名と値:** DS.DSTERM = "FINAL LAB VISIT", DS.DSDECOD = "FINAL LAB VISIT", DS.VISIT = "WEEK 4", DS.DSDTC = "2013-11-01T10:45"
    *   **矛盾の内容:** DSドメインで"FINAL LAB VISIT"がWEEK4に記録されているが、これはプロトコルで規定された最終検査のタイミングではない。
    *   **問題点の原因（推測）:** DS.DSTERM, DS.DSDECOD, DS.VISITの入力ミス、またはデータ収集時期の誤り。
    *   **対応策（提案）:** "FINAL LAB VISIT"の記録時期について、医療機関に確認する。

**クエリ:**

*   **患者ID:** 01-704-1017

    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AEOUT = "RECOVERED/RESOLVED", AE.AEENDTC = "2013-11-18" (AESEQ=3); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
        *   **医療機関への問い合わせ文面:** 有害事象(AESEQ=3)の転帰が「回復/解決」、終了日が2013-11-18と報告されていますが、2013-11-24に有害事象による中止が記録されています。有害事象の転帰と試験中止理由について、正しい情報をご提供ください。
        *   **判断理由:** 有害事象の転帰と試験中止理由が矛盾しており、臨床試験の評価に影響を与える可能性があるため。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AEENDTC = "" (AESEQ=2); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
        *   **医療機関への問い合わせ文面:** 有害事象(AESEQ=2)の転帰が「未回復/未解決」で終了日が空欄ですが、2013-11-24に有害事象による中止が記録されています。有害事象の転帰、終了日、および試験中止理由について、正しい情報をご提供ください。
        *   **判断理由:** 有害事象の転帰と終了日が不明確であり、試験中止理由との矛盾も存在するため、臨床試験の評価に影響を与える可能性がある。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AEENDTC = "" (AESEQ=8); DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", DS.DSDTC = "2013-11-24"
        *   **医療機関への問い合わせ文面:** 有害事象(AESEQ=8)の転帰が「未回復/未解決」で終了日が空欄ですが、2013-11-24に有害事象による中止が記録されています。有害事象の転帰、終了日、および試験中止理由について、正しい情報をご提供ください。
        *   **判断理由:** 有害事象の転帰と終了日が不明確であり、試験中止理由との矛盾も存在するため、臨床試験の評価に影響を与える可能性がある。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "ASPIRIN", CM.CMSTDTC = "2000", CM.CMENDTC = ""
        *   **医療機関への問い合わせ文面:** アスピリンの投与開始日が2000年と報告されていますが、これは正しいでしょうか。また、終了日が空欄ですが、現在も継続中でしょうか。正しい投与開始日と終了日（継続中の場合はその旨）をご提供ください。
        *   **判断理由:** 投与開始日が試験開始より大幅に前であり、終了日が不明確であるため、併用薬の正確な情報が必要である。

    *   **クエリNo.5:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD = "CREAT", LB.LBORRES = "1.8", LB.LBNRIND = "HIGH" (LBSEQ=13); DM.SEX = "M"
        *   **医療機関への問い合わせ文面:** スクリーニング時のクレアチニン値が1.8 mg/dLで「高値」と報告されています。この患者様は男性(DM.SEX = "M")であり、プロトコルで規定された除外基準に該当する可能性があります。この患者様の組み入れは適切であったか、ご確認をお願いします。
        *   **判断理由:** 除外基準に抵触する可能性のあるデータが報告されており、被験者の選択が適切であったか確認が必要である。

    *   **クエリNo.6:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.QSTESTCD = "NPITM11F", QS.VISIT = "WEEK 4", QS.QSDTC = "2013-11-09" (QSSEQ=3113)
        *   **医療機関への問い合わせ文面:** NPI-Xの"NIGHT-TIME BEHAVIOR FREQUENCY" (NPITM11F) がWEEK 4 (2013-11-09) に評価されたと記録されていますが、SVドメインの記録ではWEEK4のVISITは2013-11-01です。正しい評価日をご提供ください。
        *   **判断理由:** データ収集日が矛盾しており、正確な評価時期を確認する必要がある。

    *   **クエリNo.7:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** DS.DSTERM = "FINAL LAB VISIT", DS.DSDECOD = "FINAL LAB VISIT", DS.VISIT = "WEEK 4", DS.DSDTC = "2013-11-01T10:45"
        *   **医療機関への問い合わせ文面:** DSドメインで"FINAL LAB VISIT"がWEEK4に記録されていますが、これはプロトコルで規定された最終検査のタイミングと異なります。"FINAL LAB VISIT"がこのタイミングで実施された理由をご説明ください。
        *   **判断理由:** プロトコルで規定された最終検査の時期と異なるため、理由を確認する必要がある。

## Task3: Protocol Deviation Review Results
以下にプロトコル逸脱の検出結果と、必要に応じて作成したクエリを示します。

**患者ID: 01-704-1017**

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXENDTC: 2013-11-18, DS.DSTERM: ADVERSE EVENT, DS.DSDECOD: ADVERSE EVENT
    *   **逸脱内容:** 被験者は有害事象(AE)により投与を中止し、プロトコルを完了しなかった。
    *   **プロトコル該当箇所:** 3.10.1 Discontinuations
    *   **判断理由:** DSドメインのDSTERMおよびDSDECODが"ADVERSE EVENT"であり、EXドメインのEXENDTCが最終投与日を示しているため。プロトコル3.10.1には、「有害事象により試験を中止する場合がある」と記載されている。

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD: CREAT, LB.LBORRES: 1.8, LB.LBNRIND: HIGH (Visit 1, SCREENING 1)
    *   **逸脱内容:** スクリーニング時のクレアチニン値が基準範囲を上回っている。
    *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria, [27b]
    *   **判断理由:** プロトコル3.4.2.2の除外基準[27b]には、「クレアチニンがLilly Reference Range IIIを超える患者は除外する」と記載されている。提供されたJSONデータのLBドメインによると、Visit 1 (SCREENING 1)において、LBTESTCDがCREATのLBORRESは1.8 mg/dLであり、LBNRINDはHIGHとなっている。Define.xmlを参照すると、LBTESTCDがCREATの場合のLBORRESU (Original Units)はmg/dLであり、LBORNRLO (Reference Range Lower Limit in Orig Unit)は0.8、LBORNRHI (Reference Range Upper Limit in Orig Unit)は1.6である。したがって、報告された値は基準範囲を上回っている。

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM: MYOCARDIAL INFARCTION, MH.MHSTDTC: (blank), AE.AETERM: MYOCARDIAL INFARCTION, AE.AESTDTC: 2013-10-19
    *   **逸脱内容:** スクリーニング前5年以内に心筋梗塞の既往歴がある。
    *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria, [17]
    *   **判断理由:** プロトコル3.4.2.2の除外基準[17]には、「過去5年以内の重篤な心血管疾患の既往」が除外基準として記載されている。MHドメインに心筋梗塞(MYOCARDIAL INFARCTION)の既往が報告されており、AEドメインにも同一の事象が報告されている。AE.AESTDTCは2013-10-19であり、スクリーニング日(DM.DMDTC: 2013-09-20)から5年以内である。MH.MHSTDTCが空欄であるため、正確な発症日は不明だが、AEの発症日を根拠に除外基準に抵触すると判断した。

*   **逸脱No.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD: MHITM01-MHITM13, QS.QSORRES: すべて0 (Visit 1, SCREENING 1)
    *   **逸脱内容:** スクリーニング時に実施されたHachinski Ischemic Scaleのすべての項目が0点であり、合計スコアが0点である。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria, [4]
    *   **判断理由:** プロトコル3.4.2.1の選択基準[4]には、「Modified Hachinski Ischemic Scale score of <= 4」と記載されている。提供されたJSONデータのQSドメインによると、Visit 1 (SCREENING 1)において、QSTESTCDがMHITM01からMHITM13までのQSORRESはすべて0であり、合計スコアが0点である。これは選択基準を満たしているが、通常、認知症の診断を受けた患者において、Hachinski Ischemic Scaleのスコアが0点となることは稀である。

*   **逸脱No.: 5**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM: ALZHEIMER'S DISEASE, MH.MHSTDTC: 2011-03-27
    *   **逸脱内容:** スクリーニング時にアルツハイマー病と診断されている。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria [2]
    *   **判断理由:** プロトコル 3.4.2.1 選択基準[2]には、「NINCDSおよびADRDAガイドラインで定義されるprobable ADの診断」と記載されている。MHドメインのMHTERMが"ALZHEIMER'S DISEASE"、MHSTDTCが"2011-03-27"であり、スクリーニング日(DM.DMDTC: 2013-09-20)より前にアルツハイマー病と診断されていることがわかる。

*   **逸脱No.: 6**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** QS.QSTESTCD: MMITM01-MMITM06, QS.QSORRES: 1, 3, 3, 5, 0, 9 (Visit 1, SCREENING 1)
    *   **逸脱内容:** スクリーニング時に実施されたMMSEの合計スコアが21点である。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria, [3]
    *   **判断理由:** プロトコル3.4.2.1の選択基準[3]には、「MMSE score of 10 to 23」と記載されている。提供されたJSONデータのQSドメインによると、Visit 1 (SCREENING 1)において、QSTESTCDがMMITM01からMMITM06までのQSORRESを合計すると21点であり、選択基準を満たしている。

**クエリ:**

*   **患者ID: 01-704-1017**

    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** MH.MHTERM: MYOCARDIAL INFARCTION, MH.MHSTDTC: (blank)
        *   **医療機関への問い合わせ文面:** MHドメインに記録されている心筋梗塞(MYOCARDIAL INFARCTION)の正確な発症日を教えてください。
        *   **判断理由:** プロトコル3.4.2.2の除外基準[17]に該当するかどうかを確認するため、正確な発症日を特定する必要がある。

    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.QSTESTCD: MHITM01-MHITM13, QS.QSORRES: すべて0 (Visit 1, SCREENING 1)
        *   **医療機関への問い合わせ文面:** スクリーニング時に実施されたHachinski Ischemic Scaleのすべての項目が0点と記録されていますが、これは正しいでしょうか。認知症と診断された患者で、すべての項目が0点となることは稀であると考えられます。記録に誤りがないか、再確認をお願いします。
        *   **判断理由:** Hachinski Ischemic Scaleのスコアが0点であることは、通常、認知症の診断を受けた患者では稀であるため、記録の正確性を確認する必要がある。

    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD: CREAT, LB.LBORRES: 1.8, LB.LBNRIND: HIGH (Visit 1, SCREENING 1)
        *   **医療機関への問い合わせ文面:** スクリーニング時のクレアチニン値が基準範囲を上回っていますが、プロトコル3.4.2.2の除外基準[27b]に基づき、臨床的に問題ないと判断された理由を詳細に教えてください。
        *   **判断理由:** プロトコル3.4.2.2の除外基準[27b]には、「クレアチニンがLilly Reference Range IIIを超える患者は除外する」と記載されている。ただし、「臨床的に問題ないと判断された場合は、被験者を試験に含めることができる」とも記載されている。今回のケースがこれに該当するかどうかを確認するため、詳細な理由を問い合わせる必要がある。


# 01-702-1082
## Task1: Clinical Review Results
**1. 症例サマリー:**

**患者ID: 01-702-1082**

*   2013年7月3日 (Day -23): スクリーニング検査実施。白血球数 (WBC) 14.77 THOU/uL (高値)、BUN 25 mg/dL (高値)、HCT 49.0% (高値)、ビタミンB12 946 pg/mL (高値)。
*   2013年7月24日 (Day -2): 非定型検査1.1実施。ALT 37 U/L (高値)、AST 44 U/L (高値)、BUN 27 mg/dL (高値)。白血球数増加、尿検査異常の有害事象報告 (いずれも軽度)。
*   2013年7月26日 (Day 1): ベースライン評価。白血球数増加、尿検査異常の有害事象は継続中 (いずれも軽度)。低用量Xanomeline投与開始。
*   2013年8月8日 (Day 14): Week 2評価。白血球数増加、尿検査異常の有害事象は回復/寛解。クレアチンキナーゼ (CK) 320 U/L (高値)。
*   2013年9月6日 (Day 43): Week 6評価。直腸出血の有害事象報告 (軽度)。白血球数 (WBC) 13.18 THOU/uL (高値)。
*   2013年9月9日 (Day 46): 適用部位の発疹の有害事象報告 (軽度)。
*   2013年9月24日 (Day 61): 適用部位の発疹の有害事象は回復/寛解。
*   2013年9月28日 (Day 65): Week 8評価。直腸出血の有害事象は回復/寛解。白血球数 (WBC) 10.76 THOU/uL (高値)、CK 177 U/L (高値)。
*   2013年10月12日 (Day 79): Week 10 (電話)評価。皮膚刺激の有害事象報告 (中等度)。
*   2013年10月31日 (Day 98): 皮膚刺激の有害事象は回復/寛解。
*   2013年11月17日 (Day 115): Week 12評価。試験中止 (被験者による中止)。中止理由は「パッチが不便でかゆい。錠剤を希望」。白血球数 (WBC) 14.38 THOU/uL (高値)、尿中ケトン体 1 (異常)。

**2. クエリ:**

**患者ID: 01-702-1082**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "RECTAL HAEMORRHAGE", AE.AESEV = "MILD", AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AESTDTC = "2013-09-02", AE.AEENDTC = "2013-09-06"
    *   **医療機関への問い合わせ文面:** 2013年9月6日に報告された軽度の直腸出血 (AE.AETERM = "RECTAL HAEMORRHAGE") は、2013年9月6日に回復したと報告されていますが (AESEQ=7)、2013年9月28日の記録では未回復/未寛解とされています (AESEQ=8)。どちらが正しいか、確認してください。
    *   **判断理由:** 同一の有害事象 (直腸出血) に対して、異なる転帰 (AEOUT) が報告されており、矛盾しているため。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "WHITE BLOOD CELL COUNT INCREASED", AE.AESEV = "MILD", AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AESTDTC = "2013-07-07", AE.AEENDTC = "2013-07-26"
    *   **医療機関への問い合わせ文面:** 2013年7月24日に報告された白血球数増加 (AE.AETERM = "WHITE BLOOD CELL COUNT INCREASED") は、2013年7月26日に回復したと報告されていますが (AESEQ=1)、2013年8月8日の記録では未回復/未寛解とされています (AESEQ=5)。どちらが正しいか、確認してください。
    *   **判断理由:** 同一の有害事象 (白血球数増加) に対して、異なる転帰 (AEOUT) が報告されており、矛盾しているため。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = "URINE ANALYSIS ABNORMAL", AE.AESEV = "MILD", AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AESTDTC = "2013-07-07", AE.AEENDTC = "2013-07-24"
    *   **医療機関への問い合わせ文面:** 2013年7月24日に報告された尿検査異常 (AE.AETERM = "URINE ANALYSIS ABNORMAL") は、2013年7月24日に回復したと報告されていますが (AESEQ=3)、2013年7月26日の記録では未回復/未寛解とされています (AESEQ=4)。どちらが正しいか、確認してください。
    *   **判断理由:** 同一の有害事象 (尿検査異常) に対して、異なる転帰 (AEOUT) が報告されており、矛盾しているため。
*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "WBC", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** スクリーニング時 (2013-07-03)、Week 6 (2013-09-06)、Week 8 (2013-09-28)、Week 12 (2013-11-17) の白血球数 (WBC) が高値 (LBNRIND = "HIGH") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** 白血球数 (WBC) は安全性評価の重要な指標であり、基準範囲を逸脱する変動は、有害事象の可能性を示唆するため。
*   **クエリNo.: 5**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "CK", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** Week 2 (2013-08-08) および Week 8 (2013-09-28) のクレアチンキナーゼ (CK) が高値 (LBNRIND = "HIGH") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** クレアチンキナーゼ (CK) は安全性評価の重要な指標であり、基準範囲を逸脱する変動は、有害事象 (特に筋障害) の可能性を示唆するため。
*   **クエリNo.: 6**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "BUN", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** スクリーニング時 (2013-07-03)、非定型検査1.1 (2013-07-24)、Week 6 (2013-09-06) の血中尿素窒素 (BUN) が高値 (LBNRIND = "HIGH") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** 血中尿素窒素 (BUN) は安全性評価の重要な指標であり、基準範囲を逸脱する変動は、有害事象 (特に腎機能障害) の可能性を示唆するため。
*   **クエリNo.: 7**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "VITB12", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** スクリーニング時 (2013-07-03) のビタミンB12が基準範囲上限を超過しています (LBNRIND = "HIGH")。医学的に問題となるか、評価してください。
    *   **判断理由:** プロトコルでは、ビタミンB12が基準範囲下限を下回る場合を除外基準としていますが、上限を超える場合の規定がありません。医学的評価が必要です。
*   **クエリNo.: 8**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "PROT", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** Week 12 (2013-11-17) の総蛋白 (PROT) が高値 (LBNRIND = "HIGH") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** 総蛋白 (PROT) は安全性評価の重要な指標であり、基準範囲を逸脱する変動は、有害事象の可能性を示唆するため。
*   **クエリNo.: 9**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = "HCT", LB.LBSTRESN, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** スクリーニング時 (2013-07-03) のヘマトクリット (HCT) が高値 (LBNRIND = "HIGH") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** ヘマトクリット (HCT) は安全性評価の重要な指標であり、基準範囲を逸脱する変動は、有害事象の可能性を示唆するため。
*   **クエリNo.: 10**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = "KETONES", LB.LBSTRESC, LB.LBNRIND
    *   **医療機関への問い合わせ文面:** Week 12 (2013-11-17) の尿中ケトン体が異常 (LBNRIND = "ABNORMAL") です。医学的に問題となる変動か、評価してください。
    *   **判断理由:** 尿中ケトン体は安全性評価の指標であり、異常値は有害事象の可能性を示唆するため。ただし、他の検査値と比較して、臨床試験結果への影響はMinorと判断しました。
*   **クエリNo.: 11**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DS.DSTERM, DS.DSDECOD
    *   **医療機関への問い合わせ文面:** 2013年11月17日に「被験者による中止 (WITHDRAWAL BY SUBJECT)」が発生しています。中止理由が「パッチが不便でかゆい。錠剤を希望」とのことですが、プロトコルでは、皮膚刺激は有害事象として報告されるべきです。皮膚刺激は有害事象として報告されていましたか。報告されていれば、その詳細 (発現日、消失日、重症度、処置、転帰など) を教えてください。
    *   **判断理由:** 被験者の中止理由が有害事象 (皮膚刺激) に関連する可能性があり、有害事象の報告漏れの疑いがあるため。
*   **クエリNo.: 12**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** EX.EXSTDTC, EX.EXENDTC
    *   **医療機関への問い合わせ文面:** 2013年8月9日から2013年10月13日までの投与記録 (EX.EXSTDTC, EX.EXENDTC) がありません。投与状況を確認してください。
    *   **判断理由:** 投与記録 (EXドメイン) は、被験者の曝露状況を把握するための重要な情報であり、欠損はデータの解釈に影響を与える可能性があるため。
*   **クエリNo.: 13**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** SV.VISITNUM = 1.1, SV.VISIT = "UNSCHEDULED 1.1", SV.SVSTDTC = "2013-07-24", SV.SVENDTC = "2013-07-24"
    *   **医療機関への問い合わせ文面:** 非定型来院1.1 (2013年7月24日) が発生した理由を教えてください。
    *   **判断理由:** 非定型来院は、有害事象やプロトコル逸脱など、特別な理由で発生する可能性があるため。
*   **クエリNo.: 14**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** SV.VISITNUM = 8.1, SV.VISIT = "WEEK 10 (T)", SV.SVSTDTC = "2013-10-12", SV.SVENDTC = "2013-10-12"
    *   **医療機関への問い合わせ文面:** Week 10 (電話) (2013年10月12日) は、プロトコルで規定された来院ですか。
    *   **判断理由:** Define.xmlとプロトコルで規定された来院スケジュールに、Week 10 (電話) の記載がありません。
*   **クエリNo.: 15**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHSTDTC
    *   **医療機関への問い合わせ文面:** MH.MHSTDTC = "" (空欄) となっている、"Premenstrual pain" および "AORTIC STENOSIS" の発現日を特定してください。
    *   **判断理由:** 既往歴の発現日は、有害事象が治験薬投与前から存在していたかどうかを判断する上で重要であるため。

## Task2: DM Review Results
Error
## Task3: Protocol Deviation Review Results
Error

