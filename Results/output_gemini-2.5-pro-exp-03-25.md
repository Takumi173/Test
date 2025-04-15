# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 77歳、性別は男性、人種はWHITE、民族はNOT HISPANIC OR LATINO、治験実施国はUSAである。本試験の計画治療群はXanomeline High Doseであり、実際に割り付けられた治療群もXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年発症）、心筋梗塞（2000年発症）、冠動脈バイパス術（2006年実施）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2013年09月20日|Day -16 (Visit 1)|スクリーニング来院。教育歴は12年。Modified Hachinski Ischemic Scoreは0点。MMSE評価実施（想起課題スコア0点）。既往歴として心筋梗塞（2000年）、冠動脈バイパス術（2006年）、その他心疾患関連の既往歴・合併症が複数報告された。検査にてクレアチニン高値 (1.8 mg/dL, 基準範囲 0.8-1.6)。|
|2013年10月06日|Day 1 (Visit 3)|ベースライン来院。治験薬Xanomeline 54 mgパッチ投与開始。ADAS-Cog(11)スコア 27点。NPI-X合計スコア 61点（妄想、興奮/攻撃性、抑うつ/不快気分、不安、無感情/無関心、易刺激性/不安定性、異常な運動行動、夜間行動、食欲/摂食変化の項目で症状あり）。併用薬としてPremarin投与開始。|
|2013年10月18日|Day 13 (Visit 3.5)|Ambulatory ECG装着。|
|2013年10月19日|Day 14 (Visit 4)|来院。有害事象「心筋梗塞」(軽度) 発現。有害事象「心室中隔欠損」(軽度) 発現。有害事象「脳梗塞の後遺症」(高度) 発現。検査にてBUN高値 (29 mg/dL, 基準範囲 4-24)、アルブミン低値 (3.3 g/dL, 基準範囲 3.5-4.6)。NPI-X合計スコア 22点（ベースラインから改善）。|
|2013年10月20日|Day 15|治験薬をXanomeline 81 mgパッチに増量。|
|2013年10月29日|Day 24|併用薬Premarin投与終了。|
|2013年11月01日|Day 27|検査来院（DSイベントとして記録）。検査にてアルブミン低値 (3.4 g/dL, 基準範囲 3.5-4.6)。クレアチニン、BUNは基準範囲内。|
|2013年11月05日|Day 31|有害事象「そう痒症」(軽度、治験薬との関連：Probable) 発現。有害事象「発疹」(軽度、治験薬との関連：Probable) 発現。|
|2013年11月06日|Day 32|併用薬「HYDROCORTISONE, TOPICAL」投与開始（発疹/そう痒症に対する治療と推察）。|
|2013年11月09日|Day 35 (Visit 5)|来院（予定日Day 28から逸脱）。NPI-X合計スコア 38点（Week 2から悪化）。|
|2013年11月11日|Day 37 (Visit 6)|Ambulatory ECG除去。|
|2013年11月18日|Day 44|治験薬Xanomeline 81 mgパッチ投与終了（AE心筋梗塞のため）。有害事象「脳死」(高度) 発現、同日終了（転帰：回復/軽快と記録されているが医学的に矛盾）。有害事象「脳梗塞の後遺症」終了。|
|2013年11月19日|Day 45|有害事象「心筋梗塞」終了。|
|2013年11月22日|Day 48|有害事象「そう痒症」終了。有害事象「発疹」終了。併用薬「HYDROCORTISONE, TOPICAL」投与終了。|
|2013年11月24日|Day 50 (Visit 7)|来院（予定日Day 42から逸脱）。治験中止（理由：有害事象）。ADAS-Cog(11)スコア 30点（ベースラインから悪化）。CIBIC+スコア 4点（変化なし）。NPI-X合計スコア 16点（Week 4から改善、幻覚が新たに出現）。|
|2013年12月06日|Day 62 (Visit 101)|AEフォローアップ来院。試験参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死」(AETERM='BRAIN DEATH') がDay 44に発現し、同日に「回復/軽快」(AEOUT='RECOVERED/RESOLVED') したと記録されている。脳死は不可逆的な状態であり、「回復/軽快」という転帰は医学的にあり得ない。患者の死亡に関する情報（DM.DTHFL, DM.DTHDTC）は欠損している。患者の生命状態に関する極めて重大なデータの矛盾であり、安全性評価の根幹に関わる。
        *   **根拠:** 脳死の医学的定義。データの内部矛盾。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18' (Day 44)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18' (Day 44)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Subject Death Flag(DM.DTHFL)] = '' (Missing)
            *   [Date/Time of Death(DM.DTHDTC)] = '' (Missing)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 14に有害事象「心筋梗塞」(AETERM='MYOCARDIAL INFARCTION') が発現し、治験薬中止 (AEACN='DRUG WITHDRAWN') となっている。患者は心筋梗塞および冠動脈バイパス術の既往があるため再発の可能性は否定できないが、治験薬投与開始から2週間後という発現時期は治験薬との関連も考慮する必要がある。関連性は「NONE」と評価されているが、評価の妥当性について再確認が必要。
        *   **根拠:** 有害事象の発現時期と治験薬投与期間の近接性。患者の既往歴。安全性評価の重要性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19' (Day 14)
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-06' (Day 1)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK' (Start Date: 2000-05-15)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'TRIPLE VESSEL BYPASS GRAFT' (Start Date: 2006-12-16)
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「脳梗塞の後遺症」(AETERM='LATE EFFECTS OF CEREBRAL INFARCTION') が高度 (AESEV='SEVERE') でDay 14からDay 44まで持続したと報告されている。心筋梗塞 (AESEQ=1) と同じ日に発現している。脳梗塞の既往はMHにはない。心筋梗塞に伴う血栓塞栓性の脳梗塞の可能性も考えられるが、「後遺症」という用語の妥当性、および心筋梗塞との関連性について医学的な評価が必要。
        *   **根拠:** 有害事象の重症度と持続期間。心筋梗塞との時間的関連性。用語の医学的妥当性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19' (Day 14)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18' (Day 44)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION' (Start Date: Day 14)
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 有効性評価において、ADAS-Cog(11)スコアはベースラインの27点からWeek 6 (Day 50) には30点へと悪化したが、NPI-X合計スコアはベースラインの61点からWeek 6には16点へと改善している。CIBIC+は変化なし。認知機能の悪化と行動症状の改善という乖離が見られる。治験薬中止に至った心筋梗塞の影響や、評価時期（Day 50は最終投与後6日経過）も考慮する必要があるが、有効性の評価としては一貫性に欠ける可能性がある。
        *   **根拠:** 異なる有効性評価指標間での結果の乖離。評価時期と臨床イベントとの関連。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Study Day of Finding(QS.QSDY)] = 1, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 27
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Study Day of Finding(QS.QSDY)] = 50, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 30
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Study Day of Finding(QS.QSDY)] = 1, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 61
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Study Day of Finding(QS.QSDY)] = 50, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 16
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Study Day of Finding(QS.QSDY)] = 50, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4
            *   [Study Day of End of Treatment(EX.EXENDY)] = 44
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 14 (for MI)
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50 (Discontinuation due to AE)
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** ベースライン後の血圧測定において、収縮期・拡張期ともに低下傾向が見られ、起立性低血圧を示唆する所見（例：ベースライン 臥位144/70 → 立位1分 120/66）も認められる。Xanomelineはムスカリン作動薬であり、心血管系への影響（徐脈、血圧低下）が知られている。本症例は心血管系の既往があり高齢であるため、血圧低下はリスクとなりうる。報告されたAEに失神はないが、注意が必要な所見である。
        *   **根拠:** バイタルサインの経時変化。薬剤の薬理作用。患者背景（年齢、既往歴）。
        *   **関連データ:**
            *   VSドメインの血圧データ (SYSBP, DIABP)
            *   [Age(DM.AGE)] = 77
            *   MHドメインの心血管系既往歴

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死」(AESEQ=3) の転帰が「回復/軽快」と記録されており、医学的に矛盾している。これはデータの信頼性を著しく損なう重大なエラーである。
        *   **根拠:** 医学的常識との矛盾。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 有害事象「心筋梗塞」(AESEQ=1) に対する処置として「治験薬中止」(AEACN='DRUG WITHDRAWN') が記録されているが、最終投与日はDay 44 (EX.EXENDY)、有害事象による中止日 (DS.DSSTDY) はDay 50と記録されており、治験薬の正確な中止日が不明確である。安全性および曝露期間の評価に影響する。
        *   **根拠:** ドメイン間（AE, EX, DS）の日付情報の不整合。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Study Day of End of Treatment(EX.EXENDY)] = 44 (for EXSEQ=2)
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50 (for DSDECOD='ADVERSE EVENT')
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 有害事象「発疹」(AESEQ=5, 7) および「そう痒症」(AESEQ=6, 8) が、同一期間・重症度・関連性で重複して記録されているように見える。しかし、転帰 (AEOUT) が異なり（未回復 vs 回復/軽快）、収集日 (AEDTC) も異なる。RELRECではAESEQ=5と7が中止イベント (DSSEQ=1) に関連付けられているが、中止理由は心筋梗塞 (AESEQ=1) と考えられる。これらのAE記録が重複なのか、異なる評価時点を表すのか、またRELRECの関連付けが正しいのか不明確であり、データの解釈に混乱を招く。
        *   **根拠:** ドメイン内およびドメイン間（AE, RELREC, DS）のデータ不整合・矛盾。
        *   **関連データ:**
            *   AEドメイン (AESEQ=5, 6, 7, 8)
            *   RELRECドメイン (RELID='01-704-1017-E11')
            *   DSドメイン (DSSEQ=1)
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 併用薬「HYDROCORTISONE, TOPICAL」について、標準化薬剤名 (CMDECOD) が「UNCODED」、投与単位 (CMDOSU) が「VIAL」、適応 (CMINDC) が欠損している。プロトコルでは予防的投与が規定されているが、この記録が予防的投与かAE治療か不明確。データの品質が低く、プロトコル遵守状況やAEとの関連性の評価が困難。
        *   **根拠:** 必須情報の欠損、標準化用語の不使用、疑わしい単位。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [Dose Units(CM.CMDOSU)] = 'VIAL'
            *   [Indication(CM.CMINDC)] = '' (Missing)
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** ECGデータが提供されていない。本試験ではECGおよびAmbulatory ECGによる心血管系安全性の評価が重要であり（プロトコル 3.9.3.4.2, 3.9.4）、特に本症例は心血管系の既往歴があり、心筋梗塞を発現しているため、ECGデータの欠損は安全性評価の妥当性に重大な影響を与える。
        *   **根拠:** 安全性評価に必要な重要データの欠損。
        *   **関連データ:** なし (ECGドメイン欠損)
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** PKデータが提供されていない。プロトコルではPK/PD解析が計画されており（プロトコル 4.8）、血中濃度と有効性・安全性の関連を評価するためにPKデータは重要である。
        *   **根拠:** 試験目的の達成に必要なデータの欠損。
        *   **関連データ:** なし (PKドメイン欠損)
    *   **指摘No.:** D-7
        *   **重要度:** Major
        *   **内容:** Week 4 (Visit 5) の来院日 (SV.SVSTDTC) は2013-11-09 (Day 35) であるが、同Visitで収集された検査データ (LB) の収集日時 (LB.LBDTC) は2013-11-01T10:45 (Day 27) と記録されている。来院日と検査収集日が8日間も乖離しており、データの信頼性に疑義が生じる。
        *   **根拠:** ドメイン間（SV, LB）の日付情報の不整合。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 5, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-09'
            *   [Visit Number(LB.VISITNUM)] = 5, [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-11-01T10:45'
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、いくつかの既往歴（Significant Pre-existing Conditionとしてリストされている心疾患関連等）の開始日 (MHSTDTC) が欠損している。イベントの発生時期が不明なため、治験中のイベントとの関連性評価が困難になる場合がある。
        *   **根拠:** 評価に必要な情報の欠損。
        *   **関連データ:** MHドメイン (MHSTDTCが欠損しているレコード)
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** DSドメインにおいて、Day 27のイベントが「FINAL LAB VISIT」と記録されている。これは治験中止前の最終検査来院を意味すると思われるが、用語として一般的でなく、他のマイルストーンとの区別がつきにくい可能性がある。ただし、DSCAT='OTHER EVENT' であり、臨床的な影響は小さい。
        *   **根拠:** 標準的でない用語の使用。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT'
            *   [Category for Disposition Event(DS.DSCAT)] = 'OTHER EVENT'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が欠損しているため、同意取得が治験関連手順開始（最初のスクリーニング手順はDay -16）より前に行われたか確認できない。同意取得前の手順実施はGCP違反であり、参加者の権利保護に関わる重大な逸脱となる。
        *   **プロトコル該当箇所:** 5.1 Informed Consent
        *   **根拠:** 参加者の権利保護に関する重要情報の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (Missing)
            *   [Study Day of History Collection(MH.MHDY)] = -16
            *   [Study Day of Examination(SC.SCDY)] = -16
            *   [Study Day of Vital Signs(VS.VSDY)] = -16
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時 (Day -16) のクレアチニン値が1.8 mg/dLであり、基準範囲上限 (1.6 mg/dL) を超えている。プロトコル除外基準 [27b] では、基準範囲を超える検査値は除外対象となる（臨床的に意義がないとモニター医師が判断し文書化した場合を除く）。適格性に関する確認が必要。不適格な患者の組み入れは安全性リスクを高め、データの解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準に該当する可能性のある検査値異常。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬Premarin (エストロゲン製剤) が治験薬投与開始日 (Day 1) に開始されている。プロトコル除外基準 [31v] では、エストロゲン補充療法は登録前3ヶ月間用量が安定している場合にのみ許可される。Day 1での開始はこの規定に違反する可能性がある。エストロゲンは認知機能に影響を与える可能性があり、有効性評価の交絡因子となりうる。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [31v]
        *   **根拠:** 併用薬に関する規定からの逸脱の可能性。有効性評価への潜在的影響。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル 3.6.2 では、治験薬パッチ貼付前後に毎日予防的にヒドロコルチゾンクリームを使用することが規定されている。CMドメインにはDay 32-48のヒドロコルチゾン投与記録があるが、これがプロトコル規定の予防的投与なのか、AE（発疹/そう痒症）に対する治療なのか不明確である（薬剤名未コード化、単位VIALなど詳細不明）。もし予防的投与が実施されていなかった場合、プロトコル逸脱となる。
        *   **プロトコル該当箇所:** 3.6.2 TTS Administration Procedures
        *   **根拠:** プロトコルで規定された処置の実施状況が不明確。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-11-06' (Day 32)
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2013-11-22' (Day 48)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** Week 4 (Visit 5) および Week 6 (Visit 7) の来院日が、プロトコルで規定された来院予定日からの許容期間（±3日）を逸脱している (Week 4: Day 35 vs 予定Day 28±3日; Week 6: Day 50 vs 予定Day 42±3日)。評価スケジュールの逸脱は、特に有効性評価データの解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** 3.1 Summary of Study Design (Visit schedule and windows)
        *   **根拠:** 規定された評価スケジュールからの逸脱。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 5, [Planned Study Day of Visit(SV.VISITDY)] = 28, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-09' (Day 35)
            *   [Visit Number(SV.VISITNUM)] = 7, [Planned Study Day of Visit(SV.VISITDY)] = 42, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-24' (Day 50)
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** SVドメインにVisit 3.5 (AMBUL ECG PLACEMENT, Day 13) および Visit 6 (AMBUL ECG REMOVAL, Day 37) が記録されているが、プロトコル本文 (3.9.3.4.2) ではAmbulatory ECGはVisit 2/3での実施のみ記載されており、この追加実施に関する記載がない。Schedule of Events (Attachment LZZT.1) にも記載がない。計画外の評価手順の実施、または文書化されていないプロトコル変更の可能性がある。
        *   **プロトコル該当箇所:** 3.9.3.4.2 Cardiovascular Safety Measures, Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルに記載のない評価手順の実施記録。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 3.5, [Visit Name(SV.VISIT)] = 'AMBUL ECG PLACEMENT', [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-10-18' (Day 13)
            *   [Visit Number(SV.VISITNUM)] = 6, [Visit Name(SV.VISIT)] = 'AMBUL ECG REMOVAL', [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-11' (Day 37)
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験薬の増量 (54mg→81mg) がDay 15 (Week 2終了後) に行われている。プロトコルの図 (Figure LZZT.1) ではWeek 8での増量が示唆されているように見えるが、SEドメインのElement定義 (HIS: High_Start, HIM: High_Middle) やTEドメインのElement期間 (HIS: P2W, HIM: P22W) はWeek 2での切り替えを示唆しており、EXデータと整合する。図の解釈が誤っているか、図が簡略化されている可能性が高い。プロトコル本文での明確な増量スケジュールの記載を確認する必要があるが、データ上は計画通り実施された可能性が高い。
        *   **プロトコル該当箇所:** Figure LZZT.1, TE/SEドメイン定義
        *   **根拠:** プロトコル内の情報（図 vs Element定義）間の不一致の可能性。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 1, [Dose per Administration(EX.EXDOSE)] = 54, [Study Day of End of Treatment(EX.EXENDY)] = 14
            *   [Sequence Number(EX.EXSEQ)] = 2, [Dose per Administration(EX.EXDOSE)] = 81, [Study Day of Start of Treatment(EX.EXSTDY)] = 15
            *   [Element Code(SE.ETCD)] = 'HIS', [End Date/Time of Element(SE.SEENDTC)] = '2013-10-19' (Day 14)
            *   [Element Code(SE.ETCD)] = 'HIM', [Start Date/Time of Element(SE.SESTDTC)] = '2013-10-19' (Day 14)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象について、「報告された用語」が「BRAIN DEATH」、「転帰」が「RECOVERED/RESOLVED」と記録されています (発現日: 2013-11-18)。脳死からの回復は医学的にあり得ません。記録内容をご確認いただき、正確な事象名、転帰、および患者様の状態（死亡された場合は死亡日を含む）について至急ご報告ください。これは患者様の安全性に関する極めて重要な確認事項です。
        *   **クエリ文面（英語）:** Regarding the AE reported on 2013-11-18: the Reported Term for the Adverse Event is 'BRAIN DEATH' and the Outcome of Adverse Event is 'RECOVERED/RESOLVED'. Recovery from brain death is medically impossible. Please urgently verify and provide the correct AE term, outcome, and patient status (including date of death if applicable). This is critical for patient safety information.
        *   **判断理由:** 患者の生命状態に関する重大なデータ矛盾の解消、および正確な安全性情報の確保のため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18'
            *   関連する医学的知見: 脳死の定義と予後。
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意説明文書の取得日に関する記録（「Date/Time of Informed Consent」）が欠損しています。最初の治験関連手順実施日（2013-09-20）より前に、適切に同意が取得されていたことを確認するため、同意取得日をご報告ください。これは参加者の権利保護に関する重要な確認事項です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please provide the date when informed consent was obtained to confirm it was prior to the first study procedure on 2013-09-20. This is crucial for verifying participant rights protection according to GCP.
        *   **判断理由:** GCP遵守（同意取得のタイミング）の確認、参加者の権利保護の確認のため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (Missing), First procedure date = 2013-09-20 (Day -16)
            *   関連するプロトコル箇所: 5.1 Informed Consent
    *   **クエリNo.:** Q-3 (関連指摘No.: M-2, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「心筋梗塞」について、「治験薬との関連性」が「NONE」と評価されていますが、治験薬投与開始（Day 1）から14日後の発現であり、評価の再確認をお願いします。また、本有害事象による治験薬中止に関して、「治験薬中止」の処置が記録されていますが、最終投与日（EXドメイン）はDay 44、中止イベント発生日（DSドメイン）はDay 50と記録にずれがあります。正確な治験薬最終投与日と中止理由となったイベント発生日をご確認ください。
        *   **クエリ文面（英語）:** Regarding AE 'MYOCARDIAL INFARCTION' starting Day 14: Causality is 'NONE'. Please re-evaluate considering onset 14 days after starting study drug. Also, Action Taken is 'DRUG WITHDRAWN', but last dose date (EX) is Day 44 and AE discontinuation date (DS) is Day 50. Please confirm the exact last dose date and the date of the event leading to discontinuation.
        *   **判断理由:** 安全性評価（因果関係）の妥当性確認、および曝露期間・中止理由の正確な把握のため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1), EX (EXSEQ=2), DS (DSSEQ=1), MH (Cardiac history)
            *   関連する医学的知見: 薬剤誘発性心血管イベントの可能性。
    *   **クエリNo.:** Q-4 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象について、「報告された用語」が「LATE EFFECTS OF CEREBRAL INFARCTION」、「重症度」が「SEVERE」と記録されています (発現日: Day 14-44)。脳梗塞の既往歴は報告されていません。この事象は同日に発現した心筋梗塞に関連するものか、あるいは別のイベントか、また「後遺症」という用語が適切か、臨床的な詳細と評価をご教示ください。
        *   **クエリ文面（英語）:** Regarding AE 'LATE EFFECTS OF CEREBRAL INFARCTION' (Severe, Day 14-44): No prior history of stroke reported in MH. Please clarify the clinical details, assessment of whether this event is related to the concomitant MI (onset Day 14), and if the term 'LATE EFFECTS' is appropriate.
        *   **判断理由:** 重大な有害事象の内容と原因の特定、および用語の医学的妥当性確認のため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=4, AESEQ=1), MH
            *   関連する医学的知見: 心筋梗塞と脳梗塞の関連。
    *   **クエリNo.:** Q-5 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「発疹」(AESEQ=5, 7) および「そう痒症」(AESEQ=6, 8) が、同一期間で重複して記録されているように見えますが、「転帰」が異なっています (AESEQ 5/6: 未回復, AESEQ 7/8: 回復/軽快)。これらが同一事象の異なる時点での評価なのか、あるいは記録誤りかご確認ください。また、RELRECで発疹 (AESEQ 5, 7) が中止イベント (DSSEQ=1) に関連付けられていますが、中止理由は心筋梗塞 (AESEQ=1) と思われます。関連付けが正しいかご確認ください。
        *   **クエリ文面（英語）:** AE 'RASH' (AESEQ=5, 7) and 'PRURITUS' (AESEQ=6, 8) appear duplicated for the same period but have conflicting Outcomes (Not Recovered vs Recovered). Please clarify if these are separate assessments or data errors. Also, RELREC links RASH (AESEQ 5, 7) to the discontinuation event (DSSEQ=1), but AE MI (AESEQ=1) seems the likely cause. Please verify the relationship in RELREC.
        *   **判断理由:** データの一貫性と正確性の確保、およびイベント間の関連性の明確化のため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1, 5, 6, 7, 8), RELREC, DS (DSSEQ=1)
    *   **クエリNo.:** Q-6 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時 (2013-09-20) の検査結果について、「クレアチニン」が「1.8 mg/dL」であり、施設基準範囲上限 (1.6 mg/dL) を超えています。プロトコル除外基準 [27b] に該当する可能性があります。この検査値異常について臨床的な意義を評価し、組み入れが適切であったか、またその判断が文書化されているかご確認ください。
        *   **クエリ文面（英語）:** Screening lab result (2013-09-20) for Creatinine was 1.8 mg/dL, exceeding the upper reference limit (1.6 mg/dL). This potentially meets exclusion criterion [27b]. Please confirm if the clinical significance was assessed, if enrollment was appropriate, and if this assessment was documented per protocol.
        *   **判断理由:** 患者の適格性確認、プロトコル遵守の確認のため。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='CREAT', LBDY=-16)
            *   関連するプロトコル箇所: 3.4.2.2 Exclusion Criteria [27b]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬について、「報告された薬剤名」が「PREMARIN」の薬剤が、治験薬投与開始日と同じ2013-10-06に開始されています。プロトコル除外基準 [31v] では、エストロゲン補充療法は登録前3ヶ月間用量が安定している必要があります。この薬剤の使用状況と、プロトコル規定への適合性についてご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication 'PREMARIN' was started on 2013-10-06 (Day 1), the same day as study treatment initiation. Protocol exclusion criterion [31v] requires estrogen supplements to be stable for 3 months prior to enrollment. Please verify the usage details and confirm compliance with the protocol.
        *   **判断理由:** プロトコル遵守（除外基準）の確認、有効性評価への潜在的影響の評価のため。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='PREMARIN', CMSTDTC='2013-10-06')
            *   関連するプロトコル箇所: 3.4.2.2 Exclusion Criteria [31v]
    *   **クエリNo.:** Q-8 (関連指摘No.: D-4, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「HYDROCORTISONE, TOPICAL」 (投与期間: Day 32-48) について、「標準化薬剤名」が「UNCODED」、「投与単位」が「VIAL」、「適応」が未記載です。プロトコルでは予防的なヒドロコルチゾンクリームの使用が規定されていますが、この記録が予防的投与か、AE（発疹/そう痒症）治療か不明確です。正確な薬剤名、剤形、単位、使用目的（予防 or 治療）をご確認ください。
        *   **クエリ文面（英語）:** Regarding Concomitant Medication 'HYDROCORTISONE, TOPICAL' (Day 32-48): Standardized Name is 'UNCODED', Dose Unit is 'VIAL', and Indication is missing. The protocol mandates prophylactic hydrocortisone cream. Please clarify if this record represents prophylactic use or AE treatment, and provide the correct drug name, form, unit, and purpose.
        *   **判断理由:** データ品質の向上、プロトコル遵守状況の確認、AEとの関連性評価のため。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='HYDROCORTISONE, TOPICAL')
            *   関連するプロトコル箇所: 3.6.2 TTS Administration Procedures
    *   **クエリNo.:** Q-9 (関連指摘No.: P-5, D-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 4 (Visit 5) および Week 6 (Visit 7) の来院日が、予定日からの許容期間（±3日）を逸脱しています (Week 4: Day 35 [予定Day 28], Week 6: Day 50 [予定Day 42])。逸脱理由をご記載ください。また、Week 4来院日 (Day 35) と同Visitの検査収集日 (Day 27) が一致しません。正確な検査収集日をご確認ください。
        *   **クエリ文面（英語）:** Visit 5 (Week 4) occurred on Day 35 (planned Day 28±3) and Visit 7 (Week 6) on Day 50 (planned Day 42±3), outside the protocol window. Please provide reason for deviation. Also, for Visit 5, the visit date (Day 35) and lab collection date (Day 27) do not match. Please confirm the correct lab collection date.
        *   **判断理由:** プロトコル遵守（評価スケジュール）の確認、データ整合性の確認のため。
        *   **判断根拠:**
            *   関連するデータ: SV (VISITNUM=5, 7), LB (VISITNUM=5)
            *   関連するプロトコル箇所: 3.1 Summary of Study Design
    *   **クエリNo.:** Q-10 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 3.5 (Day 13) および Visit 6 (Day 37) にAmbulatory ECGの装着・除去が記録されていますが、プロトコル本文には記載がありません。これらの実施が計画されていたものか、計画外であったか、また実施理由についてご確認ください。
        *   **クエリ文面（英語）:** Ambulatory ECG placement/removal is recorded for Visit 3.5 (Day 13) and Visit 6 (Day 37), which are not described in the protocol text. Please confirm if these procedures were planned or unscheduled, and provide the reason for conducting them.
        *   **判断理由:** プロトコル遵守（計画外手順）の確認のため。
        *   **判断根拠:**
            *   関連するデータ: SV (VISITNUM=3.5, 6)
            *   関連するプロトコル箇所: 3.9.3.4.2 Cardiovascular Safety Measures, Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-5, D-6)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 本レビュー用に提供されたデータセットにECGおよびPKドメインが含まれていない。これらのデータが収集されているか、別途保管されているか、あるいは収集されていないのかを内部（データマネジメント、統計担当等）で確認する必要がある。特にECGは本症例の安全性評価に不可欠。
        *   **判断理由:** レビューに必要な重要データが提供データに含まれていないため、データの所在と利用可能性を確認する必要がある。医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: 提供されたJSONデータセット（ECG, PKドメイン欠損）
            *   関連するプロトコル箇所: 3.9.3.4.2, 3.9.2
    *   **確認事項No.:** I-2 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインで一部既往歴の開始日が欠損している。データの完全性の観点からは望ましくないが、主要な既往歴（アルツハイマー病、心筋梗塞、バイパス術）の開始日は記録されており、治験中のイベント評価への影響は限定的と考えられる。内部記録としてデータ欠損を認識する。
        *   **判断理由:** 影響は限定的と考えられるが、データの不完全性として記録しておくべき事項。医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン
    *   **確認事項No.:** I-3 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** DSDECOD='FINAL LAB VISIT' という用語が標準的でない可能性がある。ただし、DSCAT='OTHER EVENT' であり、臨床的な意味合い（Week 4の検査来院）は文脈から理解可能であり、評価への影響は小さい。用語標準化の検討材料として内部で記録する。
        *   **判断理由:** データ品質に関する軽微な指摘であり、評価への影響は小さい。医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: DSドメイン (DSSEQ=2)
    *   **確認事項No.:** I-4 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** 治験薬の増量タイミングがプロトコルの図とSE/TE/EXデータで異なるように見える（図: Week 8 vs データ: Week 2）。SE/TE/EXデータは一貫しており、図が簡略化されているか、本文や修正版でWeek 2での増量が規定されている可能性が高い。プロトコル本文/修正版を再確認し、意図されたスケジュールであったか内部で確認する。データ上は計画通り実施された可能性が高く、逸脱の可能性は低いと判断。
        *   **判断理由:** プロトコル内の情報不一致の可能性はあるが、データの一貫性から計画通り実施された可能性が高く、影響は小さいと考えられるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: EX, SE, TEドメイン
            *   関連するプロトコル箇所: Figure LZZT.1

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 64歳、性別は男性、人種は白色人種、民族はヒスパニックまたはラテン系ではない。本試験ではプラセボ群に割り付けられた（計画された治療アームコード: Pbo, 実際の治療アームコード: Pbo）。居住国はアメリカ合衆国。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65 (Visit 1)|スクリーニング検査実施。肝酵素高値（アラニンアミノトランスフェラーゼ(ALT) = 135 U/L [基準値上限の約3.1倍], アスパラギン酸アミノトランスフェラーゼ(AST) = 145 U/L [基準値上限の約4.0倍]）を認める。|
|2013年02月21日|Day -9 (Visit 1.1)|Unscheduled Visit。肝酵素値は正常化（ALT=19 U/L, AST=29 U/L）。ナトリウム値が低値（133 mmol/L [基準値下限135]）。|
|2013年02月23日|Day -7 (Visit 1)|既往歴としてアルツハイマー病（2008年開始）、肺気腫（軽度）、冠動脈疾患（軽度）、関節炎（軽度）あり。肺膿瘍ドレナージ歴（1997年）、腸ポリープ切除術歴（2009年）あり。MMSEスコア23点、Hachinski Ischemic Scaleスコア1点。身長177.8cm、体重76.2kg。教育レベル12年。|
|2013年03月02日|Day 1 (Visit 3)|ベースライン。プラセボ投与開始。ADAS-Cog(11) Total Score 14点、NPI-X Total Score 3点。体重74.39kg。|
|2013年03月04日|Day 3|有害事象「下痢」(軽度, 因果関係: Possible) 発現。|
|2013年03月05日|Day 4|有害事象「下痢」回復。有害事象「不眠症」(軽度, 因果関係: Remote) 発現。併用薬「KAOPECTATE」を1回投与（下痢に対する処置と推察）。|
|2013年03月06日|Day 5|有害事象「不眠症」回復。|
|2013年03月14日|Day 13 (Visit 4)|体重73.03kg。NPI-X Total Score 6点。|
|2013年03月28日|Day 27 (Visit 5)|MCV高値（101 fL [基準値上限100]）、Anisocytes異常（1+）。ナトリウム値が高値（146 mmol/L [基準値上限145]）。体重73.94kg。NPI-X Total Score 4点。|
|2013年04月27日|Day 57 (Visit 8)|ADAS-Cog(11) Total Score 9点。NPI-X Total Score 4点。体重74.39kg。|
|2013年05月25日|Day 85 (Visit 9)|ADAS-Cog(11) Total Score 9点。NPI-X Total Score 6点。体重76.66kg。|
|2013年06月22日|Day 113 (Visit 10)|ADAS-Cog(11) Total Score 7点。CIBIC+スコア 4 (変化なし)。NPI-X Total Score 4点。体重75.75kg。|
|2013年07月20日|Day 141 (Visit 11)|NPI-X Total Score 4点。体重74.39kg。|
|2013年08月09日|Day 161 (Visit 12)|プラセボ投与終了（EXSEQ=2）。ADAS-Cog(11) Total Score 9点。CIBIC+スコア 4 (変化なし)。NPI-X Total Score 2点。体重74.39kg。|
|2013年08月10日|Day 162|プラセボ投与開始（EXSEQ=3）。|
|2013年08月31日|Day 183 (Visit 13)|プラセボ投与終了（EXSEQ=3）。試験完了。AST軽度高値（38 U/L [基準値上限36]）。NPI-X Total Score 2点。体重74.39kg。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有効性評価項目の一つであるDAD (Disability Assessment for Dementia) のスコアに一貫性のない変動が見られる。特にWeek 16とWeek 24の間で、複数の項目（例: DAITM20 軽食準備, DAITM24 電話伝言, DAITM33 金銭管理など）において、可能(Y)/不可能(N)/該当なし(NA)の回答が大きく変動している。この変動は、実際の機能変化を反映しているのか、評価方法や評価者によるばらつき、あるいはデータ入力の問題なのか不明であり、DAD評価の信頼性に疑問が生じる。
        *   **根拠:** DADは日常生活動作の能力を評価する重要な副次評価項目である。評価結果の信頼性が低い場合、試験の有効性評価（特に日常生活動作に関する副次目的）の解釈に影響を与える可能性がある。プラセボ群での変動としても一貫性が乏しい。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM20', [Finding in Original Units(QS.QSORRES)] = 'Y' (Day 1), 'N' (Day 113), 'Y' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM24', [Finding in Original Units(QS.QSORRES)] = 'N' (Day 1), 'N' (Day 113), 'Y' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM29', [Finding in Original Units(QS.QSORRES)] = 'NA' (Day 1), 'N' (Day 113), 'N' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM30', [Finding in Original Units(QS.QSORRES)] = 'N' (Day 1), 'N' (Day 113), 'Y' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM33', [Finding in Original Units(QS.QSORRES)] = 'Y' (Day 1), 'N' (Day 113), 'Y' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM34', [Finding in Original Units(QS.QSORRES)] = 'Y' (Day 1), 'Y' (Day 113), 'N' (Day 161)
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM37', [Finding in Original Units(QS.QSORRES)] = 'N' (Day 1), 'Y' (Day 113), 'Y' (Day 161)
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** スクリーニング時 (Day -65) にALTおよびASTの顕著な上昇 (基準値上限の3-4倍) が認められたが、Unscheduled Visit (Day -9) で正常化している。除外基準 [27b] に抵触する可能性があったが、一過性であり治験薬投与開始前に回復したため、臨床的に意義なしと判断され登録されたと推察される。
        *   **根拠:** スクリーニング時の異常値は適格性評価において重要だが、治験薬投与前に正常化が確認されており、安全性への直接的なリスクは低いと考えられる。プロトコル上も臨床的に意義がない場合は登録可能とされている。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135 (Day -65), 19 (Day -9)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145 (Day -65), 29 (Day -9)
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day -65), 'NORMAL' (Day -9)
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** 治療期間中に軽微な検査値異常が散見される（Week 4 MCV高値/Anisocytes異常/Sodium高値、Week 26 AST高値、Unscheduled Visit Sodium低値）。しかし、これらは一過性または軽度であり、関連する有害事象の報告もないため、現時点での臨床的意義は低いと考えられる。
        *   **根拠:** 検査値異常は軽微であり、特定のパターンや進行性を示唆するものではない。有害事象との時間的な関連も認められない。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day 27)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1, [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL' (Day 27)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 146, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day 27)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 133, [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (Day -9)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 38, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day 183)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** Medical History (MH) および Questionnaire (QS) では高血圧の既往歴 (HISTORY OF HYPERTENSION) が "ABSENT" と記録されているが、Concomitant Medications (CM) では降圧薬であるアムロジピン (NORVASC) が治験開始前 (Day -34) から継続して使用されている。高血圧の有無に関する情報に矛盾があり、適格性評価（除外基準 [17]f: Uncontrolled hypertension）や安全性評価（併用薬と既往歴の関連）に影響を与える可能性がある。
        *   **根拠:** 適格性基準の遵守確認、および併用薬と既往歴の整合性は、データの信頼性と参加者の安全性確保に不可欠である。高血圧の管理状況によっては安全性リスク評価も変わる可能性がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'MHITM09', [Finding in Original Units(QS.QSORRES)] = 'ABSENT' (Day -7)
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-01-27' (Day -34), [End Date/Time of Medication(CM.CMENDTC)] = '' (継続中)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** Medical History (MH) ドメインにおいて、いくつかの既往歴（肺気腫、冠動脈疾患、関節炎）について、開始日 (Start Date/Time of Medical History Event, MHSTDTC) が記録されていない。
        *   **根拠:** 開始日の欠損は、既往歴の評価において情報の完全性を損なう可能性があるが、これらの既往歴は治験開始前から存在し、MILDと評価されているため、現時点での評価への影響は限定的と考えられる。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0087' (Emphysema), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0409' (Coronary Artery Disease), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1309' (Arthritis), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** Exposure (EX) ドメインにおいて、プラセボの投与記録が2つのレコード (EXSEQ=2, EXSEQ=3) に分割されている（Day 14-161 と Day 162-183）。開始日と終了日は連続しており、投与自体は継続されていたと解釈できる。
        *   **根拠:** データ入力やシステム上の理由による分割の可能性があり、投与実態や評価への影響は低いと考えられる。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 2, [Study Day of Start of Treatment(EX.EXSTDY)] = 14, [Study Day of End of Treatment(EX.EXENDY)] = 161
            *   [Sequence Number(EX.EXSEQ)] = 3, [Study Day of Start of Treatment(EX.EXSTDY)] = 162, [Study Day of End of Treatment(EX.EXENDY)] = 183

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 既往歴として冠動脈疾患 (MILD) が報告されている。プロトコル除外基準 [17] では「serious cardiovascular disorder」が除外対象となっている。MILDと評価されており、降圧薬（アムロジピン）で管理されている状況から、除外基準には該当しないと判断された可能性が高いが、記録上確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** 適格性基準の遵守は試験の科学的妥当性の根幹である。MILDとの記載があるため逸脱の可能性は低いが、念のため確認。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0409' (Coronary Artery Disease), [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時 (Day -65) の肝酵素高値 (ALT 135 U/L, AST 145 U/L) は、プロトコル除外基準 [27b] の「Laboratory test values exceeding the Lilly Reference Range III」に該当する可能性がある。しかし、プロトコルでは臨床的に意義がない場合は登録可能とされており、Day -9に正常化が確認されているため、逸脱にはあたらないと判断された可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** スクリーニング時の異常値とその後の正常化が確認されており、登録判断の妥当性は高いと考えられるが、記録として確認。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135 (Day -65), 19 (Day -9)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145 (Day -65), 29 (Day -9)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Disability Assessment for Dementia (DAD) の評価結果についてお伺いします。特にWeek 16 (Day 113) と Week 24 (Day 161) の間で、いくつかの項目（例：「軽食やスナックを準備または調理する」(DAITM20)、「電話メッセージを書いて伝える」(DAITM24)、「お金を適切に扱う」(DAITM33)、「薬を服用することを決める」(DAITM34) など）の回答に大きな変動が見られます。この変動の理由（例：患者さんの状態変化、評価時の状況、評価者間の差異など）について、詳細をお知らせいただけますでしょうか。有効性評価の信頼性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding the Disability Assessment for Dementia (DAD) results, significant fluctuations were observed between Week 16 (Day 113) and Week 24 (Day 161) for several items (e.g., 'PREPARE OR COOK A LIGHT MEAL OR A SNACK' (DAITM20), 'WRITE AND CONVEY A TELEPHONE MESSAGE' (DAITM24), 'HANDLE ADEQUATELY HIS/HER MONEY' (DAITM33), 'DECIDE TO TAKE HIS/HER MEDICATIONS' (DAITM34)). Please clarify the reason for these fluctuations (e.g., change in subject's condition, assessment circumstances, inter-rater variability) to ensure the reliability of the efficacy assessment.
        *   **判断理由:** DADスコアの変動の一貫性がなく、有効性評価（日常生活動作）の信頼性に影響を与える可能性があるため、変動理由の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのDAD関連データ (QSTESTCD=DAITM*, VISITNUM=3, 10, 12)
            *   関連するプロトコル箇所: Section 2.2 (Secondary Objectives), Section 3.9.1.1 (Efficacy Measures - DAD), Section 4.3.1 (Efficacy Variables to be Analyzed)
            *   関連する医学的知見: アルツハイマー病患者の日常生活動作能力評価の重要性、評価のばらつき要因。
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者さんの高血圧に関する情報について確認させてください。病歴 (MH) および質問票 (QS) では「高血圧の既往歴」が「なし (Absent)」と記録されていますが、併用薬 (CM) では降圧薬である「NORVASC」が治験開始34日前から継続して使用されています。患者さんの高血圧の診断状況（診断の有無、診断日など）および治療歴について、ご確認いただけますでしょうか。適格性確認および安全性評価のため、情報の整合性確保にご協力をお願いいたします。
        *   **クエリ文面（英語）:** Please clarify the subject's hypertension status. Medical History (MH) and Questionnaire (QS) record 'HISTORY OF HYPERTENSION' as 'Absent', but Concomitant Medications (CM) show continuous use of 'NORVASC' (amlodipine) since Day -34. Please confirm the subject's hypertension diagnosis and treatment history for eligibility verification and safety assessment.
        *   **判断理由:** 高血圧の既往歴と降圧薬使用の間に矛盾があり、適格性基準（除外基準[17]f）の遵守確認と、安全性評価（既往歴と併用薬の関連）のために正確な情報が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'MHITM09', [Finding in Original Units(QS.QSORRES)] = 'ABSENT'; [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-01-27'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]f
            *   関連する医学的知見: 高血圧管理の重要性、降圧薬の使用目的。

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2, P-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時 (Day -65) のALT/AST高値は除外基準 [27b] に該当する可能性があったが、Day -9に正常化しており、臨床的に意義なしと判断され登録されたと推察される。参加者の安全性への直接的リスクは低く、プロトコル逸脱にはあたらないと判断。
        *   **判断理由:** 治験薬投与前に正常値への回復が確認されており、プロトコル上も臨床的に意義がない場合は登録が許容されるため、医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALT'/'AST' (Day -65, Day -9)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 治療期間中に散見された軽微な検査値異常（Week 4 MCV高値/Anisocytes異常/Sodium高値、Week 26 AST高値、Unscheduled Visit Sodium低値）は、一過性または軽度であり、関連するAE報告もないため、現時点での臨床的意義は低いと判断。
        *   **判断理由:** 異常の程度が軽微であり、特定のパターンや進行性を示唆せず、AEとの関連もないため、現時点では医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: LBドメインの該当データ (Day -9, 27, 183)
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** MHの冠動脈疾患はMILDと評価されており、降圧薬で管理されている状況から、除外基準 [17] の「serious cardiovascular disorder」には該当しないと判断されたと推察される。
        *   **判断理由:** MILDとの評価があり、管理されている状況を考慮すると、プロトコル逸脱の可能性は低いと判断されるため、医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM='VERBATIM_0409', MH.MHSEV='MILD'; CM.CMTRT='NORVASC'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]
    *   **確認事項No.:** I-4 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインにおける一部既往歴の開始日 (MHSTDTC) 欠損。治験開始前の長期にわたる既往の場合、正確な日付が不明なケースも考えられる。
        *   **判断理由:** 既往歴自体は記録されており、評価への影響は限定的と考えられるため、現時点では医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: MHドメインのMHSTDTC欠損レコード
    *   **確認事項No.:** I-5 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** EXドメインのプラセボ投与記録が2レコードに分割されている。開始日・終了日は連続しており、投与は継続されていたと解釈可能。
        *   **判断理由:** データ構造上の問題の可能性が高く、投与実態や評価への影響はないと考えられるため、医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン (EXSEQ=2, 3)

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 81歳、性別は女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験薬投与群（計画/実際）は Xanomeline Low Dose。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年08月25日|Day -13 (Screening 1)|MMSE スコア 23点、Hachinski スコア 1点。既往歴にアルツハイマー病 (2009年発症)、高血圧、甲状腺機能低下症など多数あり。継続併用薬として LISINOPRIL, MOTRIN(PRN), PREMARIN, PROVERA, SYNTHROID, KEFLEX(Day -61から)あり。検査にて赤血球数(RBC)が基準値下限未満 (3.80)。|
|2012年09月02日|Day -5|有害事象「紅斑」(MILD), 「そう痒症」(MILD) 発現。|
|2012年09月02日-04日|Day -5 to -3|併用薬「HYDROCORTISONE, TOPICAL」使用。|
|2012年09月07日|Day 1 (Baseline)|治験薬「XANOMELINE」54mg パッチ投与開始 (Low Dose群)。有害事象「紅斑」「そう痒症」回復。有害事象「排尿切迫」(MILD) 発現 (未回復)。ADAS-Cog(11) スコア 7点。NPI-X Total スコア 2点。|
|2012年09月13日|Day 7|有害事象「関節痛」(MODERATE), 「蜂巣炎」(MODERATE) 発現 (いずれも未回復、治験薬との関連性評価は NONE)。|
|2012年09月16日|Day 10|治験薬「XANOMELINE」投与終了。|
|2012年09月17日|Day 11 (Week 2)|有害事象「関節痛」を理由に治験中止 (Disposition Event)。MCV が基準値上限超え (101 fL)、尿比重が基準値下限未満 (1.004)。ADAS-Cog(11) スコア 5点 (Baselineから改善)。CIBIC+ スコア 4 (No Change)。NPI-X Total スコア 1点 (Baselineから改善)。|
|2012年09月29日|Day 23 (AE Follow-up)|計画外 Visit。|
|2013年02月22日|Day 169 (Retrieval)|Retrieval Visit 実施。ADAS-Cog(11) スコア 9点 (Baseline/Week 2から悪化)。CIBIC+ スコア 5 (Minimal Worsening)。NPI-X Total スコア 45点 (Baseline/Week 2から著しく悪化、特に妄想、興奮/攻撃性、脱抑制のスコアが高い)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 7 に発現した有害事象「関節痛」および「蜂巣炎」（いずれも中等度）について、治験薬との関連性が「NONE」と評価されているが、発現時期（投与開始後1週間）を考慮すると再評価が必要ではないか。特に関節痛は治験中止理由とされているため、関連性評価の妥当性は重要である。蜂巣炎は感染症であり関連性は低い可能性が高いが、関節痛については慎重な評価が求められる。
        *   **根拠:** 有害事象の発現時期と治験薬投与期間の近接性。中止理由となった事象の評価の重要性。一般的な医学知識として薬剤起因性の関節痛も存在する。
        *   **関連データ:**
            *   [報告された有害事象名(AE.AETERM)] = 'ARTHRALGIA', [開始日(Study Day)(AE.AESTDY)] = 7, [重症度(AE.AESEV)] = 'MODERATE', [関連性(AE.AEREL)] = 'NONE', [転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [報告された有害事象名(AE.AETERM)] = 'CELLULITIS', [開始日(Study Day)(AE.AESTDY)] = 7, [重症度(AE.AESEV)] = 'MODERATE', [関連性(AE.AEREL)] = 'NONE', [転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [標準化された Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [開始日(Study Day)(DS.DSSTDY)] = 11
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16' (AE.AESEQ=7 と DS.DSSEQ=1 を関連付け)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 1 に発現した有害事象「排尿切迫」（軽度）について、治験薬との関連性が「NONE」と評価されているが、治験薬 Xanomeline はムスカリン作動薬であり、膀胱収縮を促進し尿意切迫を引き起こす可能性がある。既知の薬理作用から関連性を疑うべきであり、評価の妥当性に疑問がある。
        *   **根拠:** 治験薬の薬理作用（ムスカリン M1 受容体作動薬）。有害事象の発現時期（投与開始日）。
        *   **関連データ:**
            *   [報告された有害事象名(AE.AETERM)] = 'MICTURITION URGENCY', [開始日(Study Day)(AE.AESTDY)] = 1, [重症度(AE.AESEV)] = 'MILD', [関連性(AE.AEREL)] = 'NONE', [転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Day 11 の検査で MCV が基準値上限を超えている (101 fL)。Baseline (Day -13) は 97 fL。同日の赤血球数(RBC)は Baseline 同様、基準値下限未満。大球性貧血の可能性も考えられるが、変動は軽度であり、他の血液系パラメータに異常はない。臨床的意義は現時点では不明。
        *   **根拠:** 検査値の基準値逸脱。ベースラインからの変動。
        *   **関連データ:**
            *   [検査項目コード(LB.LBTESTCD)] = 'MCV', [検査日(Study Day)(LB.LBDY)] = 11, [検査結果(数値)(LB.LBSTRESN)] = 101, [基準範囲フラグ(LB.LBNRIND)] = 'HIGH', [基準範囲上限(LB.LBSTNRHI)] = 100
            *   [検査項目コード(LB.LBTESTCD)] = 'MCV', [検査日(Study Day)(LB.LBDY)] = -13, [検査結果(数値)(LB.LBSTRESN)] = 97, [基準範囲フラグ(LB.LBNRIND)] = 'NORMAL'
            *   [検査項目コード(LB.LBTESTCD)] = 'RBC', [検査日(Study Day)(LB.LBDY)] = 11, [検査結果(数値)(LB.LBSTRESN)] = 3.7, [基準範囲フラグ(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Day 11 の尿検査で比重が基準値下限を下回っている (1.004)。Baseline (Day -13) は 1.007 (正常範囲内)。脱水や腎機能低下を示唆する他の所見（VS, BUN/CREAT）はなく、臨床的意義は低い可能性が高い。
        *   **根拠:** 検査値の基準値逸脱。ベースラインからの変動。他の関連データとの比較。
        *   **関連データ:**
            *   [検査項目コード(LB.LBTESTCD)] = 'SPGRAV', [検査日(Study Day)(LB.LBDY)] = 11, [検査結果(数値)(LB.LBSTRESN)] = 1.004, [基準範囲フラグ(LB.LBNRIND)] = 'LOW', [基準範囲下限(LB.LBSTNRLO)] = 1.006
            *   [検査項目コード(LB.LBTESTCD)] = 'SPGRAV', [検査日(Study Day)(LB.LBDY)] = -13, [検査結果(数値)(LB.LBSTRESN)] = 1.007, [基準範囲フラグ(LB.LBNRIND)] = 'NORMAL'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** DM ドメインの「Subject Reference End Date/Time」(DM.RFENDTC) が '2012-09-17' となっているが、EX ドメインの「End Date/Time of Treatment」(EX.EXENDTC) は '2012-09-16' であり、1日のずれがある。Define.xml によると DM.RFENDTC は EX からの導出変数であり、EX.EXENDTC が直接の投与終了日と考えられるため、DM.RFENDTC の値が誤っている可能性がある。臨床的な影響は小さいと考えられる。
        *   **根拠:** ドメイン間の日付データの不一致。Define.xml の変数定義。
        *   **関連データ:**
            *   [Subject Reference End Date/Time(DM.RFENDTC)] = '2012-09-17'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2012-09-16'
            *   [Study Day of End of Treatment(EX.EXENDY)] = 10
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** CM ドメインにおいて、多くの薬剤で「Standardized Medication Name」(CM.CMDECOD), 「Indication」(CM.CMINDC), 「Medication Class」(CM.CMCLAS) が欠損、または 'UNCODED' となっている。薬剤名の標準化や分類、使用理由が不明なため、併用禁止・制限薬の正確なチェックや、有害事象との関連性評価が困難になる可能性がある。データの品質と評価の信頼性に影響する。
        *   **根拠:** 重要な変数の欠損。Define.xml での変数定義。
        *   **関連データ:**
            *   CM ドメインの複数レコード (例: CMSEQ=6, 12, 19, 25, 31, 37 (KEFLEX); CMSEQ=4, 10, 17, 23, 29, 35 (LISINOPRIL) など)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択/除外基準の完全な確認に必要なデータが不足している。具体的には、選択基準[1] (Postmenopausal status)、選択基準[5] (CNS imagingの結果がADと矛盾しないことの確認)、除外基準[16b] (Screening時のECG結果)、除外基準[28b] (Screening時の葉酸値) のデータがない。これにより、被験者が適格基準を完全に満たしていたかどうかの検証ができない。参加者の安全性確保およびデータの信頼性の観点から問題となる可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 (Inclusion Criteria), 3.4.2.2 (Exclusion Criteria)
        *   **根拠:** プロトコルで要求されている適格性確認データの一部が提供されたデータセットに含まれていない。
        *   **関連データ:**
            *   DM, MH, LB, VS ドメインに関連データなし
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 同意取得日の記録 (DM.RFICDTC) が欠損している。GCP では同意取得日時の記録が求められるため、記録不備にあたる。治験手順は Day -13 から開始されており、同意自体はそれ以前に取得されていると推測されるが、記録がない。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** 必須記録事項の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (空欄)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Attachment LZZT.1 (Schedule of Events) によると、Visit 3 (Baseline) および Visit 4 (Week 2) で ECG および Pharmacokinetics (PK) 用の採血が規定されているが、提供されたデータセットにはこれらのデータが含まれていない。これがデータの欠損ではなく、評価が実施されなかった場合、プロトコルからの逸脱となる。特に ECG は安全性評価、PK は薬物動態評価に必須であり、実施されなかった場合、試験の評価に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Attachment LZZT.1 (Schedule of Events), Section 3.9.2 (Pharmacokinetics), Section 3.9.3.4.2 (Cardiovascular Safety Measures)
        *   **根拠:** プロトコルで規定された評価のデータがデータセットに存在しない。
        *   **関連データ:**
            *   ECG ドメインデータなし
            *   PK パラメータ/濃度データなし (LB ドメインにも関連データなし)
            *   [Visit Name(SV.VISIT)] = 'BASELINE', 'WEEK 2'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「関節痛」および「蜂巣炎」について、治験薬との関連性が「NONE」と記録されていますが、発現時期（投与開始後7日目）を考慮し、関連性の再評価をお願いできますでしょうか。特に関節痛は治験中止の理由とされていますので、発現状況や臨床経過の詳細（部位、症状の程度、治療内容など）についても確認させていただけますでしょうか。参加者の安全性評価のために情報が必要です。
        *   **クエリ文面（英語）:** Regarding the AEs 'ARTHRALGIA' and 'CELLULITIS' (started Day 7), causality is recorded as 'NONE'. Please reassess causality considering the onset timing (7 days after starting study drug). As 'ARTHRALGIA' led to study discontinuation, please also provide details on clinical course.
        *   **判断理由:** 中止理由となった有害事象および同時期に発現した有害事象の関連性評価の妥当性を確認し、参加者の安全性評価を確実にするため。
        *   **判断根拠:**
            *   関連するデータ: [報告された有害事象名(AE.AETERM)] = 'ARTHRALGIA', 'CELLULITIS', [開始日(Study Day)(AE.AESTDY)] = 7, [関連性(AE.AEREL)] = 'NONE', [標準化された Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   関連するプロトコル箇所: Section 3.9.3.2.1 (Adverse Event Reporting Requirements)
            *   関連する医学的知見: 薬剤起因性関節痛の可能性。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「排尿切迫」について、治験薬との関連性が「NONE」と記録されていますが、治験薬（Xanomeline）はムスカリン作動薬であり、薬理作用として排尿切迫を引き起こす可能性があります。関連性の再評価をお願いできますでしょうか。参加者の安全性評価のために情報が必要です。
        *   **クエリ文面（英語）:** Regarding the AE 'MICTURITION URGENCY' (started Day 1), causality is recorded as 'NONE'. As the study drug (Xanomeline) is a muscarinic agonist known to potentially cause urinary urgency, please reassess causality.
        *   **判断理由:** 治験薬の既知の薬理作用と一致する有害事象の関連性評価の妥当性を確認し、参加者の安全性評価を確実にするため。
        *   **判断根拠:**
            *   関連するデータ: [報告された有害事象名(AE.AETERM)] = 'MICTURITION URGENCY', [開始日(Study Day)(AE.AESTDY)] = 1, [関連性(AE.AEREL)] = 'NONE'
            *   関連するプロトコル箇所: Section 3.9.3.2.1 (Adverse Event Reporting Requirements)
            *   関連する医学的知見: ムスカリン作動薬の副作用。
    *   **クエリNo.:** Q-3 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 被験者の適格性確認のため、以下の情報をご提供いただけますでしょうか。1) 除外基準[16b]確認のためのスクリーニング時ECG結果、2) 除外基準[28b]確認のためのスクリーニング時葉酸値、3) 選択基準[5]確認のための1年以内のCNSイメージング結果がADと矛盾しないことの確認記録、4) 選択基準[1]確認のためのPostmenopausalであることの確認記録。参加者の適格性担保のために必要です。
        *   **クエリ文面（英語）:** To confirm subject eligibility, please provide: 1) Screening ECG result (Excl Crit [16b]), 2) Screening Folate level (Excl Crit [28b]), 3) Confirmation record that CNS imaging within 1 year is compatible with AD (Incl Crit [5]), 4) Confirmation record of postmenopausal status (Incl Crit [1]).
        *   **判断理由:** プロトコルで規定された選択/除外基準の遵守を確認し、参加者の適格性とデータの信頼性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: DM, MH, LB ドメインに関連データなし
            *   関連するプロトコル箇所: Section 3.4.2.1, 3.4.2.2 (Inclusion/Exclusion Criteria)
    *   **クエリNo.:** Q-4 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル Schedule of Events によると、Visit 3 (Baseline) および Visit 4 (Week 2) で ECG と Pharmacokinetics (PK) 用の採血が規定されていますが、データが提出されておりません。これらの評価の実施状況をご確認の上、データをご提出いただくか、未実施の場合はその理由をお知らせください。安全性および PK 評価の信頼性確保のために必要です。
        *   **クエリ文面（英語）:** Per protocol Schedule of Events, ECG and PK sampling were scheduled for Visit 3 (Baseline) and Visit 4 (Week 2), but data are missing. Please confirm if these assessments were performed and provide data, or state reason if not done.
        *   **判断理由:** プロトコルで規定された重要な安全性評価 (ECG) および PK 評価の実施状況を確認し、試験評価の信頼性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: ECG/PK データなし
            *   関連するプロトコル箇所: Attachment LZZT.1 (Schedule of Events), Section 3.9.2, 3.9.3.4.2
    *   **クエリNo.:** Q-5 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日の記録がありません。GCP遵守のため、同意取得日をご確認の上、ご報告ください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please provide the date the informed consent was obtained.
        *   **判断理由:** GCP遵守のため、必須記録事項である同意取得日を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (空欄)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
    *   **クエリNo.:** Q-6 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 併用薬として記録されている KEFLEX, LISINOPRIL, MOTRIN, PROVERA, SYNTHROID, HYDROCORTISONE について、可能であれば標準化された薬剤名、使用理由（適応）、薬剤分類の情報をご提供いただけますでしょうか。データの標準化と品質向上のために必要です。
        *   **クエリ文面（英語）:** For concomitant medications KEFLEX, LISINOPRIL, MOTRIN, PROVERA, SYNTHROID, HYDROCORTISONE, please provide standardized medication name (CMDECOD), indication (CMINDC), and medication class (CMCLAS) if available. Needed for data standardization.
        *   **判断理由:** データの標準化と品質を向上させ、併用薬に関する評価（禁忌薬チェック、AEとの関連評価等）の精度を高めるため。
        *   **判断根拠:**
            *   関連するデータ: CM ドメインの複数レコードで CMDECOD, CMINDC, CMCLAS が欠損/UNCODED
            *   関連するプロトコル箇所: Section 3.8 (Concomitant Therapy)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3, M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 11 の検査値異常（MCV高値、尿比重低値）を記録する。MCV高値はベースラインからの上昇が見られるが軽度であり、RBC低値もベースラインから継続している。尿比重低値も他の所見からは臨床的意義は低いと考えられる。現時点では追加の確認は不要と判断するが、今後のデータで同様の傾向が見られる場合は注意が必要。
        *   **判断理由:** 変動が軽微であり、他の臨床データと合わせて現時点での臨床的意義は低いと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD = 'MCV', 'SPGRAV' at LBDY=11
    *   **確認事項No.:** I-2 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** DM.RFENDTC と EX.EXENDTC の日付が1日ずれていることを記録する。EX.EXENDTC (2012-09-16) が実際の最終投与日であり、DM.RFENDTC (2012-09-17) は導出エラーの可能性が高い。解析等への影響は軽微と判断。
        *   **判断理由:** 導出変数の軽微な不整合であり、主要な評価への影響は小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFENDTC, EX.EXENDTC
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時 (Day -13) の赤血球数(RBC)が基準値下限未満 (3.80) であったことを記録する。プロトコルの除外基準[27b]ではヘモグロビン等は挙げられているがRBCは明記されていない。軽度の低下であり、臨床的に問題ないと治験責任医師が判断し、組み入れられたと推測される。
        *   **判断理由:** 除外基準に明記されておらず、逸脱の程度も軽微であるため。
        *   **判断根拠:**
            *   関連するデータ: [検査項目コード(LB.LBTESTCD)] = 'RBC', [検査日(Study Day)(LB.LBDY)] = -13, [検査結果(数値)(LB.LBSTRESN)] = 3.8, [基準範囲フラグ(LB.LBNRIND)] = 'LOW'
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]