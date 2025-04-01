# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    77歳、男性、人種: WHITE、民族: NOT HISPANIC OR LATINO。本試験のXanomeline High Dose群に割り付けられた。

*   **イベント推移:**
    *   2011年03月27日 (Day 不明): 既往歴としてアルツハイマー病発症 (MH.MHTERM = 'ALZHEIMER\'S DISEASE', MH.MHSTDTC = '2011-03-27')
    *   2000年 (Day 不明): アスピリン (81mg/日) 服用開始 (CM.CMTRT = 'ASPIRIN', CM.CMSTDTC = '2000')
    *   2000年05月15日 (Day 不明): 既往歴として心筋梗塞発症 (MH.MHTERM = 'HEART ATTACK', MH.MHSTDTC = '2000-05-15')
    *   2006年12月16日 (Day 不明): 既往歴として冠動脈バイパス術施行 (MH.MHTERM = 'TRIPLE VESSEL BYPASS GRAFT', MH.MHSTDTC = '2006-12-16')
    *   2013年09月20日 (Day -16): スクリーニング来院 (Visit 1)。
        *   クレアチニン値が基準値上限超 (1.8 mg/dL, 基準範囲 0.8-1.6) (LB.LBTESTCD = 'CREAT', LB.LBORRES = '1.8', LB.LBNRIND = 'HIGH')。
        *   MMSEスコア 21点 (QS.QSTESTCD = 'MMITM01'-'MMITM06')。
        *   Hachinski Ischemic Scaleスコア 0点 (QS.QSTESTCD = 'MHITM01'-'MHITM13')。
        *   複数の心血管系既往歴あり (MH)。
    *   2013年10月06日 (Day 1): ベースライン来院 (Visit 3)。
        *   治験薬Xanomeline 54 mgパッチ投与開始 (EX.EXTRT = 'XANOMELINE', EX.EXDOSE = 54, EX.EXSTDY = 1)。
        *   Premarin (エストロゲン製剤) 0.625 mg 隔日投与開始 (CM.CMTRT = 'PREMARIN', CM.CMSTDY = 1)。
        *   ADAS-Cog(11) Total Score 27点 (QS.QSTESTCD = 'ACTOT', QS.QSSTRESN = 27)。
        *   NPI-X Total Score 61点 (QS.QSTESTCD = 'NPTOT', QS.QSSTRESN = 61)。
    *   2013年10月19日 (Day 14): Week 2 来院 (Visit 4)。
        *   治験薬Xanomeline 54 mgパッチ投与終了 (EX.EXENDY = 14)。
        *   有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」(重症度: SEVERE) 発現 (AE.AETERM, AESEQ=4, AESTDY=14)。
        *   有害事象「MYOCARDIAL INFARCTION」(重症度: MILD) 発現。治験薬中止措置 (AE.AETERM, AESEQ=1, AESTDY=14, AEACN='DRUG WITHDRAWN')。
        *   有害事象「VENTRICULAR SEPTAL DEFECT」(重症度: MILD) 発現 (AE.AETERM, AESEQ=2, AESTDY=14)。
        *   アルブミン値が基準値下限未満 (3.3 g/dL, 基準範囲 3.5-4.6) (LB.LBTESTCD = 'ALB', LB.LBORRES = '3.3', LB.LBNRIND = 'LOW')。
        *   BUN値が基準値上限超 (29 mg/dL, 基準範囲 4-24) (LB.LBTESTCD = 'BUN', LB.LBORRES = '29', LB.LBNRIND = 'HIGH')。
        *   クレアチニン値は正常範囲内 (1.6 mg/dL) に改善 (LB.LBTESTCD = 'CREAT', LB.LBORRES = '1.6', LB.LBNRIND = 'NORMAL')。
        *   NPI-X Total Score 22点 (QS.QSTESTCD = 'NPTOT', QS.QSSTRESN = 22)。
    *   2013年10月20日 (Day 15): 治験薬Xanomeline 81 mgパッチ投与開始 (EX.EXTRT = 'XANOMELINE', EX.EXDOSE = 81, EX.EXSTDY = 15)。
    *   2013年10月29日 (Day 24): Premarin投与終了 (CM.CMENDY = 24)。
    *   2013年11月01日 (Day 27): Week 4 の臨床検査実施。
        *   アルブミン値が基準値下限未満 (3.4 g/dL) (LB.LBTESTCD = 'ALB', LB.LBORRES = '3.4', LB.LBNRIND = 'LOW')。
        *   BUN値は正常範囲内 (23 mg/dL) に改善 (LB.LBTESTCD = 'BUN', LB.LBORRES = '23', LB.LBNRIND = 'NORMAL')。
        *   Dispositionとして「FINAL LAB VISIT」が記録 (DS.DSDECOD = 'FINAL LAB VISIT', DS.DSSTDY = 27)。
    *   2013年11月05日 (Day 31):
        *   有害事象「PRURITUS」(重症度: MILD, 関連性: PROBABLE) 発現 (AE.AETERM, AESEQ=6, AESTDY=31)。
        *   有害事象「RASH」(重症度: MILD, 関連性: PROBABLE) 発現 (AE.AETERM, AESEQ=5, AESTDY=31)。
    *   2013年11月06日 (Day 32): Hydrocortisone Topical投与開始 (CM.CMTRT = 'HYDROCORTISONE, TOPICAL', CM.CMSTDY = 32)。
    *   2013年11月09日 (Day 35): Week 4 来院 (Visit 5)。
        *   NPI-X Total Score 38点 (QS.QSTESTCD = 'NPTOT', QS.QSSTRESN = 38)。
    *   2013年11月18日 (Day 44):
        *   治験薬Xanomeline 81 mgパッチ投与終了 (EX.EXENDY = 44)。
        *   有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」終了 (AE.AEENDY = 44)。
        *   有害事象「BRAIN DEATH」(重症度: SEVERE) 発現および同日終了 (AE.AETERM, AESEQ=3, AESTDY=44, AEENDY=44)。転帰は「RECOVERED/RESOLVED」と記録。
    *   2013年11月19日 (Day 45): 有害事象「MYOCARDIAL INFARCTION」終了 (AE.AEENDY = 45)。転帰は「RECOVERED/RESOLVED」と記録。
    *   2013年11月22日 (Day 48):
        *   有害事象「PRURITUS」終了 (AE.AEENDY = 48)。
        *   有害事象「RASH」終了 (AE.AEENDY = 48)。
        *   Hydrocortisone Topical投与終了 (CM.CMENDY = 48)。
    *   2013年11月24日 (Day 50): Week 6 来院 (Visit 7)。
        *   ADAS-Cog(11) Total Score 30点 (QS.QSTESTCD = 'ACTOT', QS.QSSTRESN = 30)。
        *   NPI-X Total Score 16点 (QS.QSTESTCD = 'NPTOT', QS.QSSTRESN = 16)。
        *   有害事象により試験中止 (DS.DSDECOD = 'ADVERSE EVENT', DS.DSSTDY = 50)。
    *   2013年12月06日 (Day 62): AE Follow-up 来院 (Visit 101)。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **内容:** 有害事象「MYOCARDIAL INFARCTION」(心筋梗塞) の重症度が「MILD」、重篤度が「N」(非重篤) と報告されている。心筋梗塞は通常、重篤な有害事象 (SAE) として扱われるべきであり、評価が不適切である可能性が高い。また、治験薬中止の措置が取られているにも関わらず、治験薬との関連性が「NONE」(なし) と評価されている点も医学的に疑問が残る。既往歴に心筋梗塞があるため、再発の可能性も考慮されるが、評価の一貫性が欠けている。
        *   **根拠:** AE.AETERM = 'MYOCARDIAL INFARCTION', AE.AESEQ = 1, AE.AESEV = 'MILD', AE.AESER = 'N', AE.AEACN = 'DRUG WITHDRAWN', AE.AEREL = 'NONE', AE.AESTDY = 14; MH.MHTERM = 'HEART ATTACK', MH.MHSTDTC = '2000-05-15'; プロトコル 3.9.3.2.2 Serious Adverse Events 定義
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **内容:** 有害事象「BRAIN DEATH」(脳死) の転帰が「RECOVERED/RESOLVED」(回復/軽快) と報告されている。脳死からの回復は医学的にありえず、報告内容に重大な誤りがある。また、重篤度も「N」(非重篤) となっている点も不適切。事象名、重篤度、転帰の報告が根本的に誤っている可能性が高い。
        *   **根拠:** AE.AETERM = 'BRAIN DEATH', AE.AESEQ = 3, AE.AESEV = 'SEVERE', AE.AESER = 'N', AE.AEOUT = 'RECOVERED/RESOLVED', AE.AESTDY = 44, AE.AEENDY = 44
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「VENTRICULAR SEPTAL DEFECT」(心室中隔欠損症) が報告されている。これは通常先天性疾患であり、成人で有害事象として発現することは考えにくい。既往歴(MH)にも記載がなく、Day 14に発現したとされている点も不自然。報告の妥当性を確認する必要がある。
        *   **根拠:** AE.AETERM = 'VENTRICULAR SEPTAL DEFECT', AE.AESEQ = 2, AE.AESTDY = 14
    *   **指摘No.:** M-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」が報告されている。事象名として一般的ではなく、AEDECODは「CEREBRAL INFARCTION」(脳梗塞) となっている。発症日(Day 14)は治験薬開始後であり、重症度はSEVEREとされている。転帰はNOT RECOVERED/NOT RESOLVEDだが終了日(Day 44)が記録されている。事象名の定義、重症度評価、転帰と終了日の整合性について確認が必要。
        *   **根拠:** AE.AETERM = 'LATE EFFECTS OF CEREBRAL INFARCTION', AE.AEDECOD = 'CEREBRAL INFARCTION', AE.AESEQ = 4, AE.AESEV = 'SEVERE', AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED', AE.AESTDY = 14, AE.AEENDY = 44
    *   **指摘No.:** M-5
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 治験薬投与開始後、血圧および脈拍の低下傾向が認められる (例: Day 14 立位3分後 SYSBP=104, DIABP=56; Day 50 立位3分後 SYSBP=112, DIABP=56)。Xanomelineはムスカリン作動薬であり、心血管系への影響 (徐脈、血圧低下) が知られている。患者は高齢で心血管系の既往歴も複数有するため、これらの変動は臨床的に注意が必要。ただし、明らかな症候性低血圧等の報告はない。
        *   **根拠:** VSドメインデータ (SYSBP, DIABP, PULSE); MHドメインデータ (心血管系既往歴); 一般的な医学知識 (ムスカリン作動薬の作用)

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「RASH」(AESEQ=5, 7) および「PRURITUS」(AESEQ=6, 8) について、同一事象に対するレコードが重複しているように見える。開始日、終了日、事象名は一致しているが、AESEQ、AEDTC、AEOUTが異なるレコードが存在する (例: AESEQ=5のAEOUTは'NOT RECOVERED/NOT RESOLVED'、AESEQ=7のAEOUTは'RECOVERED/RESOLVED')。データ入力エラーの可能性が高い。
        *   **根拠:** AE.AETERM = 'RASH', AE.AESEQ = 5, 7, AE.AESTDY = 31, AE.AEENDY = 48; AE.AETERM = 'PRURITUS', AE.AESEQ = 6, 8, AE.AESTDY = 31, AE.AEENDY = 48; RELRECドメインデータ
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Dispositionドメインに、中止理由(DSSEQ=1, DSDECOD='ADVERSE EVENT')とは別に、「FINAL LAB VISIT」(DSSEQ=2, DSDECOD='FINAL LAB VISIT', DSSTDY=27) が記録されている。通常、Dispositionドメインには試験完了、中止理由、または主要なマイルストーンが記録されるが、「最終検査来院」がDispositionイベントとして記録されるのは一般的ではない。記録の意図と妥当性を内部で確認する必要がある。
        *   **根拠:** DS.DSDECOD = 'FINAL LAB VISIT', DS.DSSEQ = 2, DS.DSSTDY = 27; SDTM IG for DS domain
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** LB, VS, QSドメインにおいて、予定来院日 (VISITDY) と実際の測定日 (--DY) の間に大きなずれが見られる場合がある (例: Visit 7/Week 6 は Planned Day 42 に対し、LB, VS, QSのActual Dayは50)。プロトコルで規定された来院ウィンドウ (Visits 4, 5, 7, 8, 13 は ±3日、Visits 9, 10, 11, 12 は ±4日) を逸脱している可能性がある。
        *   **根拠:** LB.VISITDY, LB.LBDY; VS.VISITDY, VS.VSDY; QS.VISITDY, QS.QSDY; SV.VISITDY, SV.SVSTDTC; プロトコル 3.1

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[27b] (臨床検査値異常) への抵触の可能性。ベースライン前のスクリーニング時 (Day -16) のクレアチニン値が1.8 mg/dLであり、基準範囲 (0.8-1.6 mg/dL) を超えている。プロトコルでは「Laboratory test values exceeding the Lilly Reference Range III... creatinine...」を除外基準としている。適格性評価の妥当性確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LB.LBTESTCD = 'CREAT', LB.LBORRES = '1.8', LB.LBNRIND = 'HIGH', LB.LBORNRLO = '0.8', LB.LBORNRHI = '1.6', LBDY = -16
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[31v] (併用薬: エストロゲン) の規定違反の可能性。Premarin (エストロゲン製剤) がDay 1から投与開始されているが、プロトコルでは「Estrogen supplements are permitted... but dosage must be stable for at least 3 months prior to enrollment.」と規定されている。ベースラインからの新規投与はプロトコル違反の可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31v]
        *   **根拠:** CM.CMTRT = 'PREMARIN', CM.CMSTDY = 1
    *   **指摘No.:** P-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 来院スケジュールからの逸脱。Visit 5 (Week 4) の実施日 (Day 35) が予定日 (Day 28) から7日遅れており、プロトコル規定の許容範囲 (±3日) を逸脱している。Visit 7 (Week 6) の実施日 (Day 50) も予定日 (Day 42) から8日遅れており、許容範囲 (±3日) を逸脱している。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit window description)
        *   **根拠:** SV.VISITNUM = 5, SV.VISITDY = 28, SV.SVSTDTC = '2013-11-09' (Day 35); SV.VISITNUM = 7, SV.VISITDY = 42, SV.SVSTDTC = '2013-11-24' (Day 50)
    *   **指摘No.:** P-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 安全性評価 (臨床検査) のスケジュール逸脱の可能性。プロトコルではVisit 7 (Week 6) で臨床検査 (Hematology/Chemistry) が予定されているが、LBドメインにはDay 50 (Visit 7実施日) のデータが存在しない。DSドメインにDay 27の「FINAL LAB VISIT」が記録されていることと関連があるか不明だが、予定された検査が実施されていない可能性がある。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** LBドメイン (Day 50のデータなし); DS.DSDECOD = 'FINAL LAB VISIT', DS.DSSTDY = 27

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **医療機関への問い合わせ文面:** "Day 14に発現した有害事象「MYOCARDIAL INFARCTION」(AESEQ=1) について、重症度が'MILD'、重篤度が'N' (非重篤)、治験薬との関連性が'NONE'と報告されています。心筋梗塞は通常重篤であり、治験薬中止措置も取られていることから、報告された重症度、重篤度、および関連性の評価が適切かご確認ください。必要に応じて修正をお願いします。"
        *   **判断理由:** 有害事象の評価（重症度、重篤度、関連性）が医学的一般常識および臨床経過（治験薬中止）と乖離しており、患者の安全性評価および試験結果の解釈に重大な影響を与えるため。
        *   **判断根拠:**
            *   AE.AETERM = 'MYOCARDIAL INFARCTION', AE.AESEQ = 1, AE.AESEV = 'MILD', AE.AESER = 'N', AE.AEACN = 'DRUG WITHDRAWN', AE.AEREL = 'NONE', AE.AESTDY = 14
            *   プロトコル Section 3.9.3.2.2 Serious Adverse Events 定義
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **医療機関への問い合わせ文面:** "Day 44に発現・終了した有害事象「BRAIN DEATH」(AESEQ=3) について、転帰が'RECOVERED/RESOLVED'、重篤度が'N' (非重篤) と報告されています。脳死からの回復はありえず、重篤度の評価も不適切です。事象名、重篤度、転帰について報告内容をご確認の上、修正をお願いします。本事象が実際に発生したのか、あるいは報告エラーなのか明確にしてください。"
        *   **判断理由:** 報告内容が医学的にありえず、データの信頼性を著しく損なうため。患者の実際の状態と報告の整合性を確認する必要がある。
        *   **判断根拠:**
            *   AE.AETERM = 'BRAIN DEATH', AE.AESEQ = 3, AE.AESEV = 'SEVERE', AE.AESER = 'N', AE.AEOUT = 'RECOVERED/RESOLVED', AE.AESTDY = 44, AE.AEENDY = 44
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Day 14に発現した有害事象「VENTRICULAR SEPTAL DEFECT」(AESEQ=2) について、心室中隔欠損症は通常先天性疾患ですが、有害事象として報告されています。本事象が治験期間中に新たに診断されたものか、既往歴の見落とし等他の理由によるものかご確認ください。発症日(Day 14)の妥当性についてもご確認ください。"
        *   **判断理由:** 有害事象報告の妥当性に疑問があり、患者背景情報の正確性に関わるため。
        *   **判断根拠:**
            *   AE.AETERM = 'VENTRICULAR SEPTAL DEFECT', AE.AESEQ = 2, AE.AESTDY = 14
            *   MHドメイン (VSDの記載なし)
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Day 14に発現した有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」(AESEQ=4, AEDECOD='CEREBRAL INFARCTION') について、事象名が一般的ではありません。また、転帰が'NOT RECOVERED/NOT RESOLVED'であるにも関わらず終了日(Day 44)が入力されています。事象名の詳細、および転帰と終了日の整合性についてご確認ください。"
        *   **判断理由:** 事象名の不明瞭さ、および転帰と終了日の不整合により、データの解釈が困難なため。
        *   **判断根拠:**
            *   AE.AETERM = 'LATE EFFECTS OF CEREBRAL INFARCTION', AE.AEDECOD = 'CEREBRAL INFARCTION', AE.AESEQ = 4, AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED', AE.AEENDY = 44
    *   **クエリNo.:** Q-5 (関連指摘No.: D-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** "有害事象「RASH」(AESEQ=5, 7) および「PRURITUS」(AESEQ=6, 8) について、同一期間の事象に対して複数のレコードが存在し、一部で転帰(AEOUT)が異なっています。重複レコードの要否、および正しい転帰をご確認の上、修正をお願いします。"
        *   **判断理由:** データの一貫性を確保するため。
        *   **判断根拠:**
            *   AE.AETERM = 'RASH', AE.AESEQ = 5, AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED'; AE.AESEQ = 7, AE.AEOUT = 'RECOVERED/RESOLVED'
            *   AE.AETERM = 'PRURITUS', AE.AESEQ = 6, AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED'; AE.AESEQ = 8, AE.AEOUT = 'RECOVERED/RESOLVED'
    *   **クエリNo.:** Q-6 (関連指摘No.: P-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "スクリーニング時 (Day -16) のクレアチニン値が1.8 mg/dL (基準範囲 0.8-1.6 mg/dL) であり、プロトコル除外基準[27b] (臨床検査値異常) に該当する可能性があります。本患者が適格と判断された理由、あるいは除外基準に該当しないと判断された根拠についてご確認ください。"
        *   **判断理由:** 患者選択の適格性に関わる重大な疑義であり、プロトコル遵守を確認するため。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'CREAT', LB.LBORRES = '1.8', LB.LBNRIND = 'HIGH', LB.LBORNRLO = '0.8', LB.LBORNRHI = '1.6', LBDY = -16
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [27b]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "併用薬 Premarin (エストロゲン製剤) がDay 1から投与開始されています。プロトコル除外基準[31v]では、エストロゲン補充療法は登録前3ヶ月間用量が安定している場合にのみ許容されると規定されています。本剤の投与開始がプロトコル規定に適合しているかご確認ください。"
        *   **判断理由:** 併用薬に関するプロトコル規定違反の可能性があり、適格性およびデータ解釈に影響するため。
        *   **判断根拠:**
            *   CM.CMTRT = 'PREMARIN', CM.CMSTDY = 1
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [31v]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-3, D-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Visit 5 (Week 4) および Visit 7 (Week 6) の実施日が、予定日 (それぞれDay 28, Day 42) からプロトコルで規定された許容範囲 (±3日) を超えて遅延しています (それぞれDay 35, Day 50)。遅延理由についてご確認ください。"
        *   **判断理由:** プロトコルで規定された評価スケジュールからの逸脱であり、データの評価に影響する可能性があるため。
        *   **判断根拠:**
            *   SV.VISITNUM = 5, SV.VISITDY = 28, SV.SVSTDTC = '2013-11-09' (Day 35)
            *   SV.VISITNUM = 7, SV.VISITDY = 42, SV.SVSTDTC = '2013-11-24' (Day 50)
            *   プロトコル Section 3.1
    *   **クエリNo.:** Q-9 (関連指摘No.: P-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Visit 7 (Week 6, 実施日 Day 50) で予定されていた臨床検査 (血液学・生化学) のデータがLBドメインに見当たりません。検査が実施されなかったのか、あるいは報告漏れかご確認ください。Day 27にDSドメインで'FINAL LAB VISIT'が記録されていることとの関連があれば併せてご教示ください。"
        *   **判断理由:** プロトコルで規定された安全性評価が実施されなかった可能性があり、患者の安全性監視およびデータ完全性に関わるため。
        *   **判断根拠:**
            *   LBドメイン (Day 50のデータなし)
            *   プロトコル Attachment LZZT.1 Schedule of Events
            *   DS.DSDECOD = 'FINAL LAB VISIT', DS.DSSTDY = 27

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** 治験薬投与後の血圧・脈拍低下傾向を認める。Xanomelineの薬理作用の可能性があり、心血管系既往歴のある高齢者であるため臨床的に注意が必要だが、現時点で症候性のイベント報告はない。内部で医学的監視を継続する。
        *   **判断理由:** 有害事象報告はないが、薬剤の安全性プロファイルと患者背景を考慮し、継続的な監視が必要と判断。医療機関への問い合わせは現時点では不要。
        *   **判断根拠:**
            *   VSドメインデータ (SYSBP, DIABP, PULSE)
            *   MHドメインデータ (心血管系既往歴)
            *   一般的な医学知識 (ムスカリン作動薬の作用)
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Dispositionドメインに「FINAL LAB VISIT」(DSSEQ=2) が記録されている。SDTM IGの定義上、DSドメインへの記録が適切か内部で検討・確認する。
        *   **判断理由:** データ標準の適用に関する内部確認事項であり、医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   DS.DSDECOD = 'FINAL LAB VISIT', DS.DSSEQ = 2
            *   SDTM Implementation Guide
    *   **確認事項No.:** I-3 (関連指摘No.: なし)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** MHドメインの多くのレコードで開始日(MHSTDTC)が欠損している。CMドメインのAspirinで開始Study Day(CMSTDY)が欠損している。データの完全性に関する問題として記録する。
        *   **判断理由:** データの欠損だが、既往歴や長期使用薬であり、試験評価への直接的な影響は限定的と考えられるため内部確認とする。
        *   **判断根拠:**
            *   MHドメイン (MHSTDTC欠損レコード)
            *   CM.CMTRT = 'ASPIRIN', CM.CMSTDY = null

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    *   64歳、男性、人種: WHITE、民族: NOT HISPANIC OR LATINO。教育歴: 12年。
    *   既往歴として、アルツハイマー病 (Primary Diagnosis, 2008年発症)、肺気腫 (Mild)、冠動脈疾患 (Mild)、関節炎 (Mild)、肺膿瘍ドレナージ術後 (1997年)、腸ポリープ切除術後 (2009年) を有する。
    *   併用薬として、Norvasc (Amlodipine) をDay -34から継続、Vitamin C、Vitamin Eを2009年から継続している。

*   **イベント推移:**
    *   2012年12月27日 (Day -65): Screening 1 Visit。臨床検査にてALT (135 U/L, 基準値上限の3.1倍)、AST (145 U/L, 基準値上限の4.0倍) の高値を認める (LBNRIND=HIGH)。
    *   2013年02月21日 (Day -9): Unscheduled 1.1 Visit。臨床検査にてALT (19 U/L)、AST (29 U/L) は正常化。Sodium (133 mEq/L) が基準値下限 (135) を下回り低値 (LBNRIND=LOW)。
    *   2013年03月02日 (Day 1): Baseline Visit。Placebo投与開始。バイタルサインにて臥位血圧 130/56 mmHg、立位1分後 108/66 mmHg、立位3分後 110/68 mmHg。臥位脈拍 60 bpm、立位1分後 80 bpm、立位3分後 82 bpm。起立性低血圧の可能性あり。
    *   2013年03月04日 (Day 3): 有害事象「DIARRHOEA」(Mild) 発現。
    *   2013年03月05日 (Day 4): 有害事象「DIARRHOEA」回復。有害事象「INSOMNIA」(Mild) 発現。併用薬「KAOPECTATE」を1 Tbsp服用。
    *   2013年03月06日 (Day 5): 有害事象「INSOMNIA」回復。
    *   2013年03月28日 (Day 27): Week 4 Visit。臨床検査にてAnisocytes (1, LBNRIND=ABNORMAL)、MCV (101 fL, LBNRIND=HIGH)、Sodium (146 mEq/L, LBNRIND=HIGH) を認める。
    *   2013年07月20日 (Day 141): Week 20 Visit。体温 37.44 C (99.4 F) を認める。
    *   2013年08月09日 (Day 161): Week 24 Visit。予定日 (Day 168) より7日早く実施。
    *   2013年08月31日 (Day 183): Week 26 Visit (最終投与日)。臨床検査にてAST (38 U/L) が基準値上限 (36) をわずかに上回り高値 (LBNRIND=HIGH)。体温 37.56 C (99.6 F) を認める。試験完了 (DSDECOD=COMPLETED)。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **内容:** Screening 1 (Day -65) におけるALT (135 U/L)、AST (145 U/L) の高値 (基準値上限の3倍超) は、プロトコル除外基準 [27b] (Laboratory test values exceeding the Lilly Reference Range III for... SGOT, SGPT) に抵触する可能性がある。Unscheduled Visit (Day -9) で正常化しているが、登録時の適格性判断の妥当性について確認が必要。
        *   **根拠:** LB.LBTESTCD='ALT', LB.LBORRES='135', LB.LBORNRHI='43', LB.LBNRIND='HIGH', LB.LBDY=-65; LB.LBTESTCD='AST', LB.LBORRES='145', LB.LBORNRHI='36', LB.LBNRIND='HIGH', LB.LBDY=-65; プロトコル Section 3.4.2.2 [27b]
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Unscheduled Visit (Day -9) で低ナトリウム血症 (133 mEq/L)、Week 4 (Day 27) で高ナトリウム血症 (146 mEq/L) を認めており、電解質バランスの変動が大きい。また、Week 4 (Day 27) でAnisocytes異常およびMCV高値 (101 fL) を認めており、血液学的異常の可能性が示唆される。これらの異常に関連する有害事象は報告されていない。原因や臨床的意義について評価が必要。
        *   **根拠:** LB.LBTESTCD='SODIUM', LB.LBORRES='133', LB.LBNRIND='LOW', LB.LBDY=-9; LB.LBTESTCD='SODIUM', LB.LBORRES='146', LB.LBNRIND='HIGH', LB.LBDY=27; LB.LBTESTCD='ANISO', LB.LBORRES='1', LB.LBNRIND='ABNORMAL', LB.LBDY=27; LB.LBTESTCD='MCV', LB.LBORRES='101', LB.LBNRIND='HIGH', LB.LBDY=27; AEドメインに関連報告なし
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Baseline (Day 1) のバイタルサインにおいて、臥位から立位への体位変換時に収縮期血圧が22mmHg低下し (130→108 mmHg)、脈拍が20bpm増加しており (60→80 bpm)、起立性低血圧の可能性が示唆される。患者背景 (64歳男性、アルツハイマー病) を考慮すると転倒リスクに注意が必要。関連する有害事象は報告されていない。
        *   **根拠:** VS.VSTESTCD='SYSBP', VS.VSPOS='SUPINE', VS.VSORRES='130', VS.VSDY=1; VS.VSTESTCD='SYSBP', VS.VSPOS='STANDING', VS.VSTPT='AFTER STANDING FOR 1 MINUTE', VS.VSORRES='108', VS.VSDY=1; VS.VSTESTCD='PULSE', VS.VSPOS='SUPINE', VS.VSORRES='60', VS.VSDY=1; VS.VSTESTCD='PULSE', VS.VSPOS='STANDING', VS.VSTPT='AFTER STANDING FOR 1 MINUTE', VS.VSORRES='80', VS.VSDY=1; AEドメインに関連報告なし

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** LBドメインのUnscheduled 1.1 Visit (VISITNUM=1.1) において、Planned Study Day of Visit (VISITDY) が欠損している。Study Day of Specimen Collection (LBDY=-9) は記録されている。
        *   **根拠:** LB.VISITNUM=1.1, LB.VISITDY=null, LB.LBDY=-9
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** MHドメインおよびCMドメインにおいて、一部レコードでコーディング関連変数 (MHDECOD, MHLLT, MHHLT, MHHLGT, CMDECOD, CMCLAS) が欠損している。また、MHドメインの一部レコードで開始日 (MHSTDTC)、CMドメインの継続投与薬剤で終了日 (CMENDTC, CMENDY) が欠損している。
        *   **根拠:** MH.MHTERM in ('ALZHEIMER''S DISEASE', 'VERBATIM_0087', 'VERBATIM_0409', 'VERBATIM_1084', 'VERBATIM_1169', 'VERBATIM_1309'); CM.CMTRT in ('KAOPECTATE', 'VITAMIN C', 'VITAMIN E', 'NORVASC')
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 臨床検査値 (LB) およびバイタルサイン (VS) で認められた以下の異常値/所見について、関連する有害事象 (AE) が報告されていない。
            *   Screening時の肝酵素高値 (ALT 135, AST 145)
            *   Day -9の低ナトリウム血症 (133 mEq/L)
            *   Day 27の高ナトリウム血症 (146 mEq/L)
            *   Day 27のAnisocytes異常、MCV高値 (101 fL)
            *   Baselineの起立性低血圧の可能性
            *   Week 20, 26の微熱
        *   **根拠:** LBドメイン、VSドメインの該当レコード; AEドメインに関連報告なし
    *   **指摘No.:** D-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** SUPPLBドメインのLBTMSHI (LAB RESULT/UPPER LIMIT OF NORMAL) の値が、LBドメインの値 (LBSTRESN / LBSTNRHI) から計算される値と一致しないレコードが複数存在する。特にScreening 1 (Day -65) のALT (LBSEQ=3) およびAST (LBSEQ=4) のLBTMSHI値 (それぞれ0.3, 0.7) は、計算値 (それぞれ3.14, 4.03) と大きく乖離している。
        *   **根拠:** SUPPLB.QNAM='LBTMSHI', SUPPLB.IDVARVAL='       3', SUPPLB.QVAL='0.3'; LB.LBSEQ=3, LB.LBSTRESN=135, LB.LBSTNRHI=43; SUPPLB.QNAM='LBTMSHI', SUPPLB.IDVARVAL='       4', SUPPLB.QVAL='0.7'; LB.LBSEQ=4, LB.LBSTRESN=145, LB.LBSTNRHI=36

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 選択基準 [5] (CNS imaging compatible with AD within past 1 year) の適合性に関するデータが提供されていない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5]
        *   **根拠:** 関連データなし
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 選択基準 [6] (Investigator has obtained informed consent signed by the patient (and/or legal representative) and by the caregiver) に関する記録 (DM.RFICDTC) が欠損している。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [6]
        *   **根拠:** DM.RFICDTC=null
    *   **指摘No.:** P-3
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **内容:** Screening 1 (Day -65) におけるALT (135 U/L)、AST (145 U/L) の高値は、除外基準 [27b] (Laboratory test values exceeding the Lilly Reference Range III for... SGOT, SGPT) に抵触する可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LB.LBTESTCD='ALT', LB.LBORRES='135', LB.LBORNRHI='43', LB.LBNRIND='HIGH', LB.LBDY=-65; LB.LBTESTCD='AST', LB.LBORRES='145', LB.LBORNRHI='36', LB.LBNRIND='HIGH', LB.LBDY=-65
    *   **指摘No.:** P-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Visit 12 (Week 24) の実施日 (Day 161) が、予定日 (Planned Day 168) より7日早く、プロトコルで規定された許容範囲 (±4日) を逸脱している。
        *   **プロトコル該当箇所:** Section 3.1 (Figure LZZT.1), Section 3.9 (Visit schedule description)
        *   **根拠:** SV.VISITNUM=12, SV.SVSTDTC='2013-08-09' (Day 161); TV.VISITNUM=12, TV.VISITDY=168

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-3, D-4)
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **医療機関への問い合わせ文面:** "Screening 1 (Day -65) の臨床検査にてALT 135 U/L (基準値上限43)、AST 145 U/L (基準値上限36) と高値が報告されています。これは除外基準[27b]に抵触する可能性があります。Unscheduled Visit (Day -9) では正常化していますが、登録時の適格性判断の根拠についてご確認ください。また、SUPPLBデータでは、これらの検査値に基づくLBTMSHIの値が計算値と大きく異なります。元データをご確認ください。"
        *   **判断理由:** 選択/除外基準の遵守は試験の妥当性と被験者の安全性に不可欠であり、重大な逸脱の可能性があるため。SUPPLBデータの不整合も併せて確認が必要。
        *   **判断根拠:**
            *   LB.LBTESTCD='ALT', LB.LBORRES='135', LB.LBORNRHI='43', LB.LBNRIND='HIGH', LB.LBDY=-65
            *   LB.LBTESTCD='AST', LB.LBORRES='145', LB.LBORNRHI='36', LB.LBNRIND='HIGH', LB.LBDY=-65
            *   SUPPLB.QNAM='LBTMSHI', SUPPLB.IDVARVAL='       3', SUPPLB.QVAL='0.3'
            *   SUPPLB.QNAM='LBTMSHI', SUPPLB.IDVARVAL='       4', SUPPLB.QVAL='0.7'
            *   プロトコル該当箇所: Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Day -9に低ナトリウム血症 (133 mEq/L)、Day 27に高ナトリウム血症 (146 mEq/L)、Anisocytes異常、MCV高値 (101 fL) が報告されています。これらの異常に関連する有害事象は報告されていません。これらの検査値異常の原因、臨床的意義、および有害事象報告の要否について評価・ご確認ください。"
        *   **判断理由:** 臨床的に意義のある検査値異常が複数認められ、その原因評価と有害事象としての報告要否を確認する必要があるため。
        *   **判断根拠:**
            *   LB.LBTESTCD='SODIUM', LB.LBORRES='133', LB.LBNRIND='LOW', LB.LBDY=-9
            *   LB.LBTESTCD='SODIUM', LB.LBORRES='146', LB.LBNRIND='HIGH', LB.LBDY=27
            *   LB.LBTESTCD='ANISO', LB.LBORRES='1', LB.LBNRIND='ABNORMAL', LB.LBDY=27
            *   LB.LBTESTCD='MCV', LB.LBORRES='101', LB.LBNRIND='HIGH', LB.LBDY=27
            *   AEドメインに関連報告なし
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, D-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Baseline (Day 1) のバイタルサインにて、臥位から立位への体位変換時に収縮期血圧が22mmHg低下し、起立性低血圧の可能性が示唆されます。関連する有害事象（めまい、ふらつき等）は報告されていません。この所見の臨床的評価および有害事象報告の要否についてご確認ください。"
        *   **判断理由:** 起立性低血圧は転倒リスクを高める可能性があり、患者の安全性に関わるため。有害事象としての評価・報告が必要か確認するため。
        *   **判断根拠:**
            *   VS.VSTESTCD='SYSBP', VS.VSPOS='SUPINE', VS.VSORRES='130', VS.VSDY=1
            *   VS.VSTESTCD='SYSBP', VS.VSPOS='STANDING', VS.VSTPT='AFTER STANDING FOR 1 MINUTE', VS.VSORRES='108', VS.VSDY=1
            *   AEドメインに関連報告なし
    *   **クエリNo.:** Q-4 (関連指摘No.: P-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Visit 12 (Week 24) は予定日 (Day 168) より7日早い Day 161 に実施されており、プロトコル規定の許容範囲 (±4日) を逸脱しています。逸脱理由についてご確認ください。"
        *   **判断理由:** プロトコルで規定された評価スケジュールからの逸脱は、データの解釈に影響を与える可能性があるため。
        *   **判断根拠:**
            *   SV.VISITNUM=12, SV.SVSTDTC='2013-08-09' (Day 161)
            *   TV.VISITNUM=12, TV.VISITDY=168
            *   プロトコル該当箇所: Section 3.9

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** LBドメイン Unscheduled 1.1 Visit (VISITNUM=1.1) の VISITDY が欠損している。LBDY (-9) は存在するため、VISITDYをLBDYから補完するか、欠損のままとするか内部で決定する。
        *   **判断理由:** LBDYが存在するため、データの解釈への影響は小さい。データクリーニング方針に基づき対応を決定。
        *   **判断根拠:**
            *   LB.VISITNUM=1.1, LB.VISITDY=null, LB.LBDY=-9
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** MHドメインおよびCMドメインにおいて、一部レコードでコーディング関連変数および日付変数が欠損している。コーディング作業の進捗確認、および欠損情報の回収要否を検討する。
        *   **判断理由:** データ完全性の観点から確認が必要だが、現時点で安全性や有効性評価への大きな影響はないと判断。
        *   **判断根拠:**
            *   MHドメイン、CMドメインの該当レコード
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** 選択基準 [5] (CNS imaging) の適合性に関する記録を確認する。Source Data Verification (SDV) 等で確認済みか、別途確認が必要か判断する。
        *   **判断理由:** 選択基準の確認は重要だが、他の基準は満たしており、試験も完了しているため緊急性は低い。記録の有無を確認する。
        *   **判断根拠:**
            *   プロトコル該当箇所: Section 3.4.2.1 [5]
    *   **確認事項No.:** I-4 (関連指摘No.: P-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** 選択基準 [6] (Informed consent) の取得記録 (DM.RFICDTC) が欠損している。SDV等で同意取得が確認されているか、記録の修正が必要か確認する。
        *   **判断理由:** 同意取得は必須だが、試験が完了していることから取得自体はされている可能性が高い。記録の完全性の問題として対応。
        *   **判断根拠:**
            *   DM.RFICDTC=null
            *   プロトコル該当箇所: Section 3.4.2.1 [6]
    *   **確認事項No.:** I-5 (関連指摘No.: D-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **疑義事項/確認内容:** SUPPLB.LBTMSHI の値が計算値と異なる問題について、計算ロジックの誤りか、データ入力/変換エラーか原因を調査し、必要に応じて修正する。
        *   **判断理由:** 派生変数とはいえ、元データとの整合性が取れていないのは問題。データの信頼性に関わるため確認・修正が必要。
        *   **判断根拠:**
            *   SUPPLB.QNAM='LBTMSHI' のレコードと対応するLBレコード

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    *   本症例は81歳、女性、人種: WHITE、民族: NOT HISPANIC OR LATINO の被験者である。
    *   治験薬として Xanomeline Low Dose (54 mg patch QD) が割り付けられ、実際に投与された (ARMCD: Xan_Lo, ACTARMCD: Xan_Lo)。
    *   治験薬の初回投与日 (RFSTDTC) は 2012-09-07 (Day 1)、最終投与日 (RFXENDTC) は 2012-09-16 (Day 10) であった。
    *   有害事象により Day 11 (2012-09-17) に治験を中止した。最終的な試験参加終了日 (RFPENDTC) は Day 169 (2013-02-22) の Retrieval Visit であった。
    *   主要な既往歴として、アルツハイマー病 (Primary Diagnosis, 2009年発症)、高血圧、甲状腺機能低下症、変形性関節症、骨粗鬆症、白内障手術歴などが報告されている。

*   **イベント推移:**
    *   2012-07-08 (Day -61): 有害事象「LOCALISED INFECTION」(Moderate) 発現。併用薬「KEFLEX」開始。
    *   2012-08-25 (Day -13): Screening Visit 1。
        *   臨床検査(LB): RBC (Erythrocytes) が基準値下限未満 (LOW, 3.8 TI/L)。
        *   MMSEスコア 23点、Hachinski Ischemic Scaleスコア 1点。
    *   2012-09-02 (Day -5): 有害事象「ERYTHEMA」(Mild) および「PRURITUS」(Mild) 発現。併用薬「HYDROCORTISONE, TOPICAL」開始。
    *   2012-09-04 (Day -3): 併用薬「HYDROCORTISONE, TOPICAL」終了。
    *   2012-09-05 (Day -2): Screening Visit 2。
    *   2012-09-07 (Day 1): Baseline Visit。治験薬「XANOMELINE」(54 mg patch QD) 投与開始。
        *   有害事象「ERYTHEMA」および「PRURITUS」が回復/解決 (Outcome: RECOVERED/RESOLVED)。
        *   有害事象「MICTURITION URGENCY」(Mild) 発現。治験薬との関連性なしと評価。Treatment Emergent。
    *   2012-09-13 (Day 7): 有害事象「ARTHRALGIA」(Moderate) 発現。治験薬との関連性なしと評価。Treatment Emergent。
    *   2012-09-13 (Day 7): 有害事象「CELLULITIS」(Moderate) 発現。治験薬との関連性なしと評価。Treatment Emergent。
    *   2012-09-16 (Day 10): 治験薬「XANOMELINE」投与終了。
    *   2012-09-17 (Day 11): Week 2 Visit。有害事象により治験中止。
        *   臨床検査(LB): MCV (Ery. Mean Corpuscular Volume) が基準値上限超過 (HIGH, 101 fL)、RBC (Erythrocytes) が基準値下限未満 (LOW, 3.7 TI/L)、SPGRAV (Specific Gravity) が基準値下限未満 (LOW, 1.004)、ANISO (Anisocytes) が異常 (ABNORMAL, 1)。
        *   有害事象「LOCALISED INFECTION」、「MICTURITION URGENCY」、「ARTHRALGIA」、「CELLULITIS」は未回復/未解決。
        *   認知機能評価 (QS): ADAS-Cog(11) スコア 5 (Baseline: 7)。CIBIC+ スコア 4 (No Change)。NPI-X Total スコア 1 (Baseline: 2)。
    *   2012-09-29 (Day 23): AE Follow-up Visit (Visit 101)。
    *   2013-02-22 (Day 169): Retrieval Visit (Visit 201)。
        *   認知機能評価 (QS): ADAS-Cog(11) スコア 9。CIBIC+ スコア 5 (Minimal worsening)。NPI-X Total スコア 45。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Day 1に発現した有害事象「MICTURITION URGENCY」(排尿切迫) について、治験薬との関連性(AEREL)が 'NONE' と評価されている。しかし、治験薬 Xanomeline はムスカリン作動薬であり、膀胱平滑筋への作用による排尿切迫は薬理学的に想定される副作用である。一般的な医学的知見に基づくと、治験薬との関連を除外することは困難であり、関連性の再評価が必要である。
        *   **根拠:** AE.AETERM = 'MICTURITION URGENCY', AE.AESTDY = 1, AE.AEREL = 'NONE'; EX.EXTRT = 'XANOMELINE'; 一般的な医学知識 (ムスカリン作動薬の副作用)
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Day 11に有害事象を理由に治験が中止されている (DS.DSTERM = 'ADVERSE EVENT')。しかし、中止の直接的な原因となった有害事象が特定されていない。Day 11時点で複数の有害事象 (LOCALISED INFECTION, ARTHRALGIA, CELLULITIS, MICTURITION URGENCY) が未回復であり、特に CELLULITIS (蜂窩織炎) は重症度が Moderate であるため、中止の要因となった可能性が高いと考えられるが、明確化が必要である。
        *   **根拠:** DS.DSTERM = 'ADVERSE EVENT', DS.DSSTDY = 11; AE.AESEQ in [3, 6, 7, 8], AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED'
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象として報告された「LOCALISED INFECTION」(AESEQ=3) の重症度(AESEV)は 'MODERATE' であるが、既往歴(MH)として報告された同名の「LOCALISED INFECTION」(MHSEQ=6) の重症度(MHSEV)は 'MILD' となっており、評価に不一致が見られる。
        *   **根拠:** AE.AETERM = 'LOCALISED INFECTION', AE.AESEV = 'MODERATE', AE.AESTDY = -61; MH.MHTERM = 'LOCALISED INFECTION', MH.MHSEV = 'MILD'
    *   **指摘No.:** M-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Day 11の血液検査において、MCV高値 (101 fL)、RBC低値 (3.7 TI/L)、Anisocytosis (ABNORMAL) が認められた。Screening時からRBC低値は存在したが、MCV高値とAnisocytosisはDay 11で新たに出現または悪化している。これらの血液学的変化の臨床的意義（例：大球性貧血の可能性、薬剤性の可能性など）について評価が必要である。
        *   **根拠:** LB.LBTESTCD = 'MCV', LB.LBDY = 11, LB.LBNRIND = 'HIGH'; LB.LBTESTCD = 'RBC', LB.LBDY = 11, LB.LBNRIND = 'LOW'; LB.LBTESTCD = 'ANISO', LB.LBDY = 11, LB.LBNRIND = 'ABNORMAL'

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「ERYTHEMA」および「PRURITUS」について、同一の開始日(AESTDY = -5)を持つレコードが複数存在する (ERYTHEMA: AESEQ 1, 4; PRURITUS: AESEQ 2, 5)。AESEQ 1, 2 は終了日・転帰が不明瞭で収集日がDay -2、AESEQ 4, 5 は終了日がDay 1で転帰が回復済み、収集日がDay 11となっている。これはDay 11のVisitで過去のAEの転帰を更新した記録と思われるが、データの重複または記録方法の誤りの可能性がある。
        *   **根拠:** AE.AETERM = 'ERYTHEMA', AE.AESTDY = -5, AE.AESEQ in [1, 4]; AE.AETERM = 'PRURITUS', AE.AESTDY = -5, AE.AESEQ in [2, 5]
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** AEドメインにおいて、MedDRAコーディングに関連する変数 (AELLT, AELLTCD, AEDECOD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBDSYCD, AESOCCD) が全てのレコードで欠損している。有害事象の標準化と集計・分析に必須の情報であり、コーディングプロセスの確認が必要。
        *   **根拠:** AEドメインの該当変数列が全て欠損
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** CMドメインにおいて、多くのレコードで薬剤の標準名(CMDECOD)、適応症(CMINDC)、薬剤分類(CMCLAS)が欠損しているか、'UNCODED' となっている。データ品質の観点から、可能な限り情報を補完することが望ましい。
        *   **根拠:** CMドメインの該当変数列に欠損または 'UNCODED' が多数存在
    *   **指摘No.:** D-4
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 併用薬「PREMARIN」および「PROVERA」のレコードにおいて、Dose Units (CMDOSU) および Dosing Frequency (CMDOSFRQ) が欠損している。
        *   **根拠:** CM.CMTRT = 'PREMARIN', CM.CMDOSU = '', CM.CMDOSFRQ = ''; CM.CMTRT = 'PROVERA', CM.CMDOSU = '', CM.CMDOSFRQ = ''

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 選択基準[5]「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の遵守を確認できるデータがない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 関連するデータドメイン（例: IE, 手順記録など）が存在しないか、情報が記録されていない。
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[16b]「Evidence from ECG recording at screening of any listed condition」の遵守を確認できるデータがない。Screening時のECG実施・評価記録が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** ECGドメインが存在しないか、Screening Visit (Visit 1 or 2) のECGデータが記録されていない。
    *   **指摘No.:** P-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **逸脱の可能性:** 除外基準[25]「A history within the last 5 years of a primary or recurrent malignant disease (with exceptions...)」について、既往歴(MH)に「BASAL CELL CARCINOMA」(2007年発症) が存在する。これがプロトコル記載の例外規定（切除済み等）に該当するか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [25]
        *   **根拠:** MH.MHTERM = 'BASAL CELL CARCINOMA', MH.MHSTDTC = '2007'
    *   **指摘No.:** P-4
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **逸脱の可能性:** 除外基準[27b]「Laboratory test values exceeding the Lilly Reference Range III...」について、Screening時(Day -13)のRBCが基準値下限未満(LOW)であった。これが除外基準に抵触しないと判断された根拠が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LB.LBTESTCD = 'RBC', LB.LBDY = -13, LB.LBNRIND = 'LOW'
    *   **指摘No.:** P-5
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** プロトコルのSchedule of Events (Attachment LZZT.1) では、Visit 4 (Week 2) でECGを実施することになっているが、対応するデータが見当たらない。評価スケジュールの逸脱の可能性がある。
        *   **プロトコル該当箇所:** Attachment LZZT.1 Schedule of Events
        *   **根拠:** ECGドメインが存在しないか、Visit 4 のECGデータが記録されていない。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, M-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** Day 11に有害事象により治験中止となっていますが、中止の主たる原因となった有害事象名をご教示ください。また、Day 1発現の有害事象「MICTURITION URGENCY」(AESEQ=6) について、治験薬との関連性は「NONE」と報告されていますが、治験薬の薬理作用を考慮し、関連性評価について再度ご確認ください。
        *   **判断理由:** 治験中止理由の明確化と、薬理作用から関連が疑われる有害事象の関連性評価の妥当性を確認するため。
        *   **判断根拠:**
            *   DS.DSTERM = 'ADVERSE EVENT', DS.DSSTDY = 11
            *   AE.AETERM = 'MICTURITION URGENCY', AE.AESTDY = 1, AE.AEREL = 'NONE'
            *   プロトコル Section 3.9.3.2.1 (AE報告), Section 1 (薬剤情報)
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** 選択基準[5]を満たしたことを確認するため、スクリーニング前1年以内に実施されたCNSイメージング（CTまたはMRI）の結果がADと矛盾しないことを確認した記録をご提示ください。
        *   **判断理由:** 選択基準遵守の確認のため。
        *   **判断根拠:**
            *   プロトコル Section 3.4.2.1 [5]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-2, P-5)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** スクリーニング時(Visit 1または2)およびVisit 4のECGが実施・評価された記録をご提示ください。除外基準[16b]に該当する所見がなかったこと、およびVisit 4での評価が実施されたことをご確認ください。
        *   **判断理由:** 除外基準遵守および評価スケジュール遵守の確認のため。
        *   **判断根拠:**
            *   プロトコル Section 3.4.2.2 [16b], Attachment LZZT.1
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** Day 11の血液検査にてRBC低値、MCV高値、Anisocytosisが認められています。これらの所見の臨床的意義および原因について、担当医師の見解をご教示ください。
        *   **判断理由:** 臨床検査値異常の臨床的意義を確認し、患者の安全性評価を行うため。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'MCV', LB.LBDY = 11, LB.LBNRIND = 'HIGH'
            *   LB.LBTESTCD = 'RBC', LB.LBDY = 11, LB.LBNRIND = 'LOW'
            *   LB.LBTESTCD = 'ANISO', LB.LBDY = 11, LB.LBNRIND = 'ABNORMAL'
    *   **クエリNo.:** Q-5 (関連指摘No.: D-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** 有害事象「ERYTHEMA」(AESEQ 1, 4) および「PRURITUS」(AESEQ 2, 5) について、複数のレコードが存在します。Day 11に収集されたAESEQ 4, 5の記録は、Day 1に回復したイベントの最終的な転帰報告と思われますが、記録が正しいかご確認ください。必要であれば修正をお願いします。
        *   **判断理由:** データの一貫性を確保するため。
        *   **判断根拠:**
            *   AE.AETERM = 'ERYTHEMA', AE.AESTDY = -5, AE.AESEQ in [1, 4]
            *   AE.AETERM = 'PRURITUS', AE.AESTDY = -5, AE.AESEQ in [2, 5]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** 除外基準[25]に関連し、既往歴の「BASAL CELL CARCINOMA」(2007年発症) について、プロトコル記載の例外規定（切除済み等）に該当することをご確認ください。
        *   **判断理由:** 除外基準遵守の確認のため。
        *   **判断根拠:**
            *   MH.MHTERM = 'BASAL CELL CARCINOMA', MH.MHSTDTC = '2007'
            *   プロトコル Section 3.4.2.2 [25]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-4)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** 除外基準[27b]に関連し、スクリーニング時(Day -13)のRBC低値(3.8 TI/L)について、臨床的に問題なく、除外基準に抵触しないと判断された根拠をご教示ください。
        *   **判断理由:** 除外基準遵守の確認のため。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'RBC', LB.LBDY = -13, LB.LBNRIND = 'LOW'
            *   プロトコル Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-8 (関連指摘No.: D-4)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** 併用薬「PREMARIN」(CMSEQ 2他) および「PROVERA」(CMSEQ 3他) について、Dose Units (CMDOSU) および Dosing Frequency (CMDOSFRQ) が欠損しています。情報をご提供ください。
        *   **判断理由:** データの完全性を向上させるため。
        *   **判断根拠:**
            *   CM.CMTRT = 'PREMARIN', CM.CMDOSU = '', CM.CMDOSFRQ = ''
            *   CM.CMTRT = 'PROVERA', CM.CMDOSU = '', CM.CMDOSFRQ = ''

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** AE "LOCALISED INFECTION" と MH "LOCALISED INFECTION" の重症度評価が異なる (AE: Moderate, MH: Mild)。AE報告時の評価が優先されることが多いが、データ入力時の不整合の可能性も考慮。現時点では修正依頼はせず、記録として残す。
        *   **判断理由:** 臨床的な影響は小さいと考えられ、データの解釈に大きな支障はないため。
        *   **判断根拠:**
            *   AE.AETERM = 'LOCALISED INFECTION', AE.AESEV = 'MODERATE'
            *   MH.MHTERM = 'LOCALISED INFECTION', MH.MHSEV = 'MILD'
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **疑義事項/確認内容:** AEドメインのMedDRAコーディング関連変数が欠損している。コーディング担当部署に連絡し、コーディング作業の状況を確認し、完了を依頼する。
        *   **判断理由:** 標準化された有害事象データの集計・分析に必須であり、データの品質と信頼性に影響するため。
        *   **判断根拠:**
            *   AEドメインの AELLT, AEDECOD 等の変数が欠損
    *   **確認事項No.:** I-3 (関連指摘No.: D-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** CMドメインの薬剤コーディング(CMDECOD)、適応症(CMINDC)、分類(CMCLAS)の入力が不十分。データマネジメントプロセス内で、可能な範囲での情報補完や標準化を検討する。
        *   **判断理由:** データの品質向上と、将来的な集計・分析の精度向上のため。
        *   **判断根拠:**
            *   CMドメインの該当変数列に欠損または 'UNCODED' が多数存在