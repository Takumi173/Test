# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 77歳、性別は男性、人種はWHITE、民族はNOT HISPANIC OR LATINO、計画された治療群コードは Xan_Hi (Xanomeline High Dose)、実際の治療群コードは Xan_Hi (Xanomeline High Dose)、国は USA。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2013年09月20日|Day -16 (Visit 1: SCREENING 1)|既往歴: アルツハイマー病 (2011年発症)、心疾患、リビドー亢進、ST上昇、心筋梗塞 (2000年)、ST低下、冠動脈バイパス術 (2006年)、期外収縮。MMSEスコア 21。Hachinskiスコア 0。クレアチニン 1.8 mg/dL (基準値超過)。立位血圧変動は正常範囲内。|
|2013年09月27日|Day -9 (Visit 2: SCREENING 2)|立位血圧変動は正常範囲内。|
|2013年10月06日|Day 1 (Visit 3: BASELINE)|治験薬 Xanomeline 54 mg パッチ投与開始。ADAS-Cog(11)スコア 27。NPI-X合計スコア 61 (妄想、興奮/攻撃性、抑うつ/不快気分、不安、無関心/無感情、易刺激性/不安定性、異常な運動行動)。併用薬 Premarin 開始。立位血圧変動は正常範囲内。|
|2013年10月18日|Day 13 (Visit 3.5: AMBUL ECG PLACEMENT)|立位1分後に収縮期血圧が臥位から24mmHg低下 (起立性低血圧の可能性)。|
|2013年10月19日|Day 14 (Visit 4: WEEK 2)|有害事象「心筋梗塞」(軽度)、「心室中隔欠損」(軽度)、「脳梗塞の後遺症」(高度) 発現。治験薬中止と記録あるが、翌日増量投与開始されており矛盾。BUN 29 mg/dL (基準値超過)。アルブミン 3.3 g/dL (基準値未満)。NPI-X合計スコア 22 (ベースラインから改善)。血圧全体的に低下傾向。治験薬 Xanomeline 54 mg 投与終了。|
|2013年10月20日|Day 15|治験薬 Xanomeline 81 mg パッチ投与開始 (プロトコル計画より早期の増量)。|
|2013年10月29日|Day 24|併用薬 Premarin 投与終了。|
|2013年11月01日|Day 27 (Visit 5の前)|Disposition Eventとして "FINAL LAB VISIT" 記録。アルブミン 3.4 g/dL (基準値未満)。|
|2013年11月05日|Day 31|有害事象「発疹」(軽度)、「そう痒症」(軽度) 発現 (治験薬との関連: Probable)。|
|2013年11月06日|Day 32|併用薬 Hydrocortisone, topical 開始。|
|2013年11月09日|Day 35 (Visit 5: WEEK 4)|NPI-X合計スコア 38 (Week 2から悪化)。立位3分後に収縮期血圧が臥位から18mmHg低下 (起立性低血圧の可能性)。|
|2013年11月18日|Day 44|有害事象「脳死」(高度、非重篤、回復/軽快と記録) 発現 (医学的に矛盾)。治験薬 Xanomeline 81 mg 投与終了。|
|2013年11月19日|Day 45|有害事象「心筋梗塞」終了。|
|2013年11月22日|Day 48|有害事象「発疹」、「そう痒症」終了。併用薬 Hydrocortisone, topical 終了。|
|2013年11月24日|Day 50 (Visit 7: WEEK 6)|有害事象により試験中止。ADAS-Cog(11)スコア 30 (ベースラインから悪化)。CIBIC+スコア 4 (変化なし)。NPI-X合計スコア 16 (Week 4から改善、幻覚が新規発現)。立位3分後に収縮期血圧が臥位から20mmHg低下 (起立性低血圧の可能性)。|
|2013年12月06日|Day 62 (Visit 101: AE FOLLOW-UP)|参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死」が報告されているが、重篤度が「非重篤(N)」、転帰が「回復/軽快(Recovered/Resolved)」と記録されており、医学的にあり得ない組み合わせである。事象名自体の誤り、重篤性評価の誤り、転帰評価の誤りの可能性が極めて高い。これが試験中止理由である可能性も示唆されるが、記録の不備により判断できない。参加者の安全性評価に重大な影響を与える。
        *   **根拠:** 「脳死」は定義上、不可逆的な全脳機能の喪失であり、回復することはありえない。また、脳死は通常、生命を脅かす状態（SAE基準の Is Life Threatening または Results in Death）に該当する。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Serious Event(AE.AESER)] = 'N'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18' (Day 44)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18' (Day 44)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「心筋梗塞」がDay 14に報告されている。MHに心筋梗塞の既往歴 (2000年) があり、再発の可能性も考えられるが、治験薬との関連性評価 (AEREL=NONE) や処置 (AEACN=DRUG WITHDRAWN と記録されているが実際は増量) に疑問がある。心血管系リスクの高い患者であり、評価の妥当性を確認する必要がある。
        *   **根拠:** 心筋梗塞は重篤なイベントであり、治験薬との関連性評価は慎重に行う必要がある。処置記録と実際の投与記録に矛盾があるため、評価の信頼性が低い。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Serious Event(AE.AESER)] = 'N'
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19' (Day 14)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2000-05-15'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (Day 15, 81mg開始)
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 治療期間中 (Day 13, 35, 50) に複数回、立位での収縮期血圧低下 (臥位から15mmHg以上) が観察されており、起立性低血圧の可能性が示唆される。特にDay 13, 50では20mmHg以上の低下が見られる。プロトコルでは心血管系の安全性（失神など）をモニタリングすることになっている (Section 3.9.3.4.2)。Xanomelineはムスカリン作動薬であり、心血管系への影響（徐脈、血圧低下）が知られているため、薬剤関連の可能性も考慮すべきである。
        *   **根拠:** 起立性低血圧は転倒リスクを高め、高齢者では特に注意が必要。薬剤の副作用として一般的。
        *   **関連データ:**
            *   VSドメインの血圧データ (SYSBP, DIABP) at Day 13, 35, 50 (VSPOS=SUPINE vs STANDING)
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** スクリーニング時 (Day -16) のクレアチニン値が 1.8 mg/dL であり、基準範囲 (0.8-1.6 mg/dL) を超過している。これは除外基準 EXCL27b (Laboratory test values exceeding the Lilly Reference Range III for... creatinine) に抵触する可能性があるが、被験者は組み入れられている。組み入れ判断の妥当性について確認が必要。Day 14には正常範囲内に改善している。
        *   **根拠:** 除外基準違反は参加者の安全性リスクを高め、試験データの解釈に影響を与える可能性がある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
            *   プロトコル Section 3.4.2.2 [27b]
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** Day 50のNPI-X評価で幻覚 (Hallucinations) が新規に報告されている (Score 1)。Xanomelineの副作用として精神症状が起こる可能性も考慮される。
        *   **根拠:** 有効性評価項目であるNPI-Xの変化であり、安全性との関連も考慮すべき。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM02S'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1
            *   [Study Day of Finding(QS.QSDY)] = 50
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** Day 14にBUNの一過性上昇 (29 mg/dL, Ref: 4-24)、Day 14およびDay 27にアルブミンの低値 (3.3, 3.4 g/dL, Ref: 3.5-4.6) が認められる。臨床的な意義は現時点では不明だが、腎機能や栄養状態の変動として留意すべき。
        *   **根拠:** 軽微な検査値異常だが、他の所見との関連で重要となる可能性がある。
        *   **関連データ:**
            *   LBドメインのBUN, ALBデータ at Day 14, 27

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死」について、事象名(AETERM)、重篤度(AESER='N')、転帰(AEOUT='RECOVERED/RESOLVED')の組み合わせが論理的に矛盾している。データの正確性に重大な疑義があり、安全性評価に影響する。
        *   **根拠:** 医学的に脳死は非重篤でもなく、回復/軽快するものでもない。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Serious Event(AE.AESER)] = 'N'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** 有害事象「心筋梗塞」(AESEQ=1) の処置として「治験薬中止 (DRUG WITHDRAWN)」(AE.AEACN) と記録されているが、EXドメインでは心筋梗塞発現の翌日 (Day 15) から治験薬が増量投与 (54mg→81mg) されている。AEとEXの記録が完全に矛盾しており、実際の処置と曝露量評価の信頼性に重大な影響を与える。
        *   **根拠:** AEに対する処置記録と実際の投薬記録が一致しない。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19' (Day 14)
            *   [Sequence Number(EX.EXSEQ)] = 2
            *   [Dose per Administration(EX.EXDOSE)] = 81
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (Day 15)
    *   **指摘No.:** D-3
        *   **重要度:** Critical
        *   **内容:** DSドメインで試験中止理由が「有害事象 (ADVERSE EVENT)」(DSDECOD) と記録されているが、どの有害事象 (AESEQ) が中止の原因となったか特定できない。RELRECドメインにもDSとAEを明確に関連付ける情報がない (RELIDは同じだがRELTYPEが空)。中止理由の特定は安全性評価において重要である。
        *   **根拠:** 中止理由となったイベントが不明確なため、因果関係やリスク評価が困難。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
            *   AEドメイン全体
            *   RELRECドメイン
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** DSドメインでの試験中止日 (DS.DSSTDTC = 2013-11-24, Day 50) と、EXドメインでの最終投与日 (EX.EXENDTC = 2013-11-18, Day 44) が一致しない。中止決定後に投与が継続されたのか、あるいは記録の誤りか不明。曝露期間の評価に影響する。
        *   **根拠:** 中止日と最終投与日が異なる。
        *   **関連データ:**
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-11-18' (Day 44)
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「心室中隔欠損」が報告されているが、通常これは先天性疾患であり、MHドメインに記録がない。AEとしての報告の妥当性、およびMHとの不整合。
        *   **根拠:** 先天性疾患は通常AEではなくMHに記録される。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   MHドメイン全体
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 有害事象「脳梗塞の後遺症」が報告されている。MHドメインに脳梗塞自体の明確な記録はない（心筋梗塞、冠動脈バイパス術はある）。AEとしての報告の妥当性、およびMHとの関連が不明確。
        *   **根拠:** 後遺症がAEとして報告される場合の基準が不明確。MHとの関連も要確認。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   MHドメイン全体
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** QSドメインのDay 50のNPI-X評価において、幻覚の頻度(NPITM02F)、重症度(NPITM02V)、苦痛度(NPITM02D)、スコア(NPITM02S)が記録されているが、幻覚の有無を問う質問(NPITM02)の記録がない。データ入力漏れの可能性。
        *   **根拠:** 関連する質問項目間でデータが欠損している。
        *   **関連データ:**
            *   QSドメイン at QSDY=50, QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', QSSCAT='HALLUCINATIONS'
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** 併用薬「HYDROCORTISONE, TOPICAL」について、標準化薬剤名(CMDECOD)および薬剤分類(CMCLAS)が「UNCODED」となっている。データ標準化が必要。
        *   **根拠:** データ標準化の不備。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [Medication Class(CM.CMCLAS)] = 'UNCODED'
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** SUPPAEドメインにおいて、全てのAEに治療期発現フラグ(AETRTEM)が'Y'と付与されている。「心室中隔欠損」や「脳梗塞の後遺症」が治療期発現と判断されている根拠が不明。
        *   **根拠:** フラグ付与の妥当性に疑問。
        *   **関連データ:**
            *   SUPPAEドメイン (QNAM='AETRTEM')
            *   AEドメイン (AETERM='VENTRICULAR SEPTAL DEFECT', 'LATE EFFECTS OF CEREBRAL INFARCTION')
    *   **指摘No.:** D-10
        *   **重要度:** Minor
        *   **内容:** RELRECドメインのRELTYPE（関連性の種類）が全て空欄である。レコード間の関連性の意味が不明確。
        *   **根拠:** 必須ではないが、関連性を解釈するために重要な情報が欠損。
        *   **関連データ:**
            *   RELRECドメイン全体

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 EXCL27b (特定の検査値異常) に抵触する可能性がある。スクリーニング時 (Day -16) のクレアチニン値が 1.8 mg/dL であり、基準範囲 (Lilly Reference Range III, Define.xmlでは0.8-1.6 mg/dL) を超過している。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** スクリーニング時の検査値が除外基準に該当する可能性がある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 EXCL17 (過去5年以内の重篤な心血管系障害) に抵触する可能性がある。MHに心筋梗塞 (2000年)、冠動脈バイパス術 (2006年)、不整脈（期外収縮）の既往歴がある。これらが「重篤な心血管系障害」に該当しないと判断された根拠が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17]
        *   **根拠:** MHに記載のある心血管系の既往歴が除外基準に該当する可能性がある。
        *   **関連データ:**
            *   MHドメイン (MHTERM = 'HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT', 'SKIPPED BEATS' / MHDECOD = 'MYOCARDIAL INFARCTION', 'TRIPLE VESSEL BYPASS GRAFT', 'EXTRASYSTOLES')
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験薬の増量時期がプロトコル規定と異なる。High Dose群 (Xan_Hi) はプロトコル上、Week 8で54mgから81mg (75cm2) に増量される計画だが、本症例ではWeek 2後 (Day 15) に増量されている。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design, Figure LZZT.1)
        *   **根拠:** EXドメインの記録がプロトコルの投与計画と異なる。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 1, [Dose per Administration(EX.EXDOSE)] = 54, [End Date/Time of Treatment(EX.EXENDTC)] = '2013-10-19' (Day 14)
            *   [Sequence Number(EX.EXSEQ)] = 2, [Dose per Administration(EX.EXDOSE)] = 81, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (Day 15)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬 Premarin (Estrogens Conjugated) の使用がプロトコル規定に反する可能性がある。プロトコルでは、エストロゲン補充療法は登録前3ヶ月間用量が安定している場合に限り許可されるが、本症例ではスクリーニング時には使用しておらず、治験薬開始日 (Day 1) から使用開始されている。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] v)
        *   **根拠:** CMドメインの記録がプロトコルの併用薬規定と異なる。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1)
            *   CMドメイン (スクリーニング期間の記録)
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** NPI-Xの評価スケジュールがプロトコル規定（2週間隔）と異なる可能性がある。Week 2 (Day 14) と Week 4 (Day 35) の間隔が3週間以上空いている。
        *   **プロトコル該当箇所:** Section 3.9.1.1
        *   **根拠:** QSドメインの評価日がプロトコル規定の間隔と異なる。
        *   **関連データ:**
            *   QSドメイン (QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)') の QSDY
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬 Hydrocortisone, topical の使用目的が不明確。プロトコル Section 3.6.2 ではパッチ貼付部位への Hydrocortisone cream (1%) の使用が指示されているが、CMドメインの記録がこれに該当するのか、別途の治療目的なのか不明。Indication が記録されていない。
        *   **プロトコル該当箇所:** Section 3.6.2, Section 3.4.2.2 [31b] k) (Systemic corticosteroidsは禁止)
        *   **根拠:** CM記録とプロトコル指示の関連性が不明確。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Indication(CM.CMINDC)] = ''

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1, D-3)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として「脳死」が報告されていますが、重篤度が「無」、転帰が「回復/軽快」と記録されています。これは医学的に考えられない組み合わせです。事象名、重篤度、転帰について、記録内容を至急ご確認ください。また、この事象がDay 50の試験中止理由と関連があるかどうかも含め、詳細な臨床経過をお知らせください。
        *   **クエリ文面（英語）:** The AE 'BRAIN DEATH' is reported with Severity 'N' and Outcome 'RECOVERED/RESOLVED'. This combination is medically implausible. Please urgently verify the AE term, seriousness, and outcome. Also, clarify if this event is related to the study discontinuation on Day 50 and provide detailed clinical course.
        *   **判断理由:** 報告されたAEの内容に重大な医学的矛盾があり、参加者の安全性評価およびデータの信頼性に致命的な影響を与えるため。中止理由の特定も不可欠。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Serious Event(AE.AESER)] = 'N', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18', [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24'
            *   関連する医学的知見: 脳死の定義、SAE報告基準
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14に有害事象「心筋梗塞」が報告され、処置として「治験薬中止」と記録されていますが、翌日Day 15から治験薬が増量されています。実際の処置内容と、治験薬との関連性評価（「無し」と記録）の根拠についてご確認ください。既往歴との関連も含め、評価をお願いします。
        *   **クエリ文面（英語）:** AE 'MYOCARDIAL INFARCTION' on Day 14 has Action Taken 'DRUG WITHDRAWN', but EX shows dose increase on Day 15. Please confirm the actual action taken and the rationale for causality assessment ('NONE'), considering patient's medical history.
        *   **判断理由:** AEに対する処置記録と実際の投与記録が矛盾しており、安全性評価と曝露量評価の信頼性に影響するため。関連性評価の妥当性確認も必要。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1), EX (EXSEQ=1, 2), MH (MHTERM='HEART ATTACK')
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 治験期間中、複数回（Day 13, 35, 50）立位での血圧低下が認められます。起立性低血圧の症状（めまい、ふらつき等）の有無、および臨床的な評価についてご確認ください。
        *   **クエリ文面（英語）:** Postural drops in systolic blood pressure were observed on multiple occasions (Day 13, 35, 50). Please confirm if the patient experienced symptoms of orthostatic hypotension (e.g., dizziness, lightheadedness) and provide clinical assessment.
        *   **判断理由:** 起立性低血圧の兆候があり、転倒リスクや薬剤関連の可能性を評価する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: VSドメインの血圧データ (Day 13, 35, 50)
            *   関連する医学的知見: 起立性低血圧の症状、ムスカリン作動薬の副作用
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時 (Day -16) のクレアチニン値が「1.8 mg/dL」であり、基準範囲 (0.8-1.6 mg/dL) を超過しています。これは除外基準 EXCL27b に抵触する可能性がありますが、組み入れられています。組み入れ適格と判断された根拠、および逸脱として報告されているかご確認ください。
        *   **クエリ文面（英語）:** Screening Creatinine on Day -16 was '1.8 mg/dL', exceeding the reference range (0.8-1.6 mg/dL). This potentially violates Exclusion Criterion EXCL27b. Please confirm the rationale for eligibility assessment and if this was reported as a protocol deviation.
        *   **判断理由:** 除外基準違反の可能性があり、参加者の安全性とデータの信頼性に影響するため。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='CREAT', LBDY=-16)
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-5 (関連指摘No.: M-1, D-3)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Day 50に「有害事象」を理由に試験が中止されていますが、原因となった具体的な有害事象が特定できません。中止の判断根拠となった有害事象（事象名と発現日）を特定し、ご報告ください。
        *   **クエリ文面（英語）:** Study discontinuation on Day 50 was due to 'ADVERSE EVENT'. Please identify the specific adverse event(s) (term and onset date) that led to this decision.
        *   **判断理由:** 試験中止の具体的な理由が不明であり、安全性評価に不可欠な情報が欠落しているため。
        *   **判断根拠:**
            *   関連するデータ: DS (DSDECOD='ADVERSE EVENT', DSSTDTC='2013-11-24'), AEドメイン全体
    *   **クエリNo.:** Q-6 (関連指摘No.: D-2)
        *   **重要度:** Critical
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「心筋梗塞」(発現日 Day 14) の記録では処置が「治験薬中止」となっていますが、投与記録 (EX) では翌日 Day 15 から増量投与が開始されています。どちらの記録が正しいかご確認ください。必要に応じて記録を修正してください。
        *   **クエリ文面（英語）:** AE 'MYOCARDIAL INFARCTION' (onset Day 14) record indicates 'DRUG WITHDRAWN', but EX record shows dose increase started on Day 15. Please verify which record is correct and revise accordingly.
        *   **判断理由:** AE処置と投与記録の矛盾は、データの信頼性に重大な影響を与えるため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1, AEACN='DRUG WITHDRAWN'), EX (EXSEQ=2, EXDOSE=81, EXSTDTC='2013-10-20')
    *   **クエリNo.:** Q-7 (関連指摘No.: D-4)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 試験中止日 (Disposition) が「2013-11-24」(Day 50) ですが、治験薬の最終投与日 (Exposure) が「2013-11-18」(Day 44) となっています。日付が一致しません。最終投与日、または中止日の記録をご確認ください。
        *   **クエリ文面（英語）:** Study discontinuation date (DS.DSSTDTC) is '2013-11-24' (Day 50), but the last date of study treatment (EX.EXENDTC) is '2013-11-18' (Day 44). Please verify the correct date(s).
        *   **判断理由:** 中止日と最終投与日の不一致は、曝露期間の正確な評価を妨げるため。
        *   **判断根拠:**
            *   関連するデータ: DS (DSSTDTC='2013-11-24'), EX (EXENDTC='2013-11-18')
    *   **クエリNo.:** Q-8 (関連指摘No.: P-3, D-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本被験者は Xanomeline High Dose 群ですが、治験薬が Day 15 (Week 2 後) に 54mg から 81mg へ増量されています。プロトコルでは Week 8 での増量が計画されています。増量時期が早まった理由と、これがプロトコル逸脱として報告されているかご確認ください。
        *   **クエリ文面（英語）:** This subject in Xanomeline High Dose arm had dose increased from 54mg to 81mg on Day 15 (after Week 2), while protocol planned dose increase at Week 8. Please provide reason for early dose increase and confirm if reported as deviation.
        *   **判断理由:** プロトコルからの投与計画逸脱の可能性があり、有効性・安全性評価に影響するため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン (EXDOSE, EXSTDTC)
            *   関連するプロトコル箇所: Section 3.1 (Figure LZZT.1)
    *   **クエリNo.:** Q-9 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬 Premarin が Day 1 から Day 24 まで使用されています。プロトコルでは、エストロゲン補充療法は登録前3ヶ月間用量が安定している場合に許可されますが、本症例では Day 1 から開始されています。使用理由と、これがプロトコル逸脱として報告されているかご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication Premarin was used from Day 1 to Day 24. Protocol allows estrogen supplements only if dose was stable for 3 months prior to enrollment. Please clarify reason for use starting Day 1 and confirm if reported as deviation.
        *   **判断理由:** プロトコルの併用薬規定からの逸脱の可能性があり、確認が必要なため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='PREMARIN', CMSTDTC, CMENDTC)
            *   関連するプロトコル箇所: Section 3.4.2.2 [31b] v)
    *   **クエリNo.:** Q-10 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 既往歴に心筋梗塞 (2000年)、冠動脈バイパス術 (2006年)、期外収縮が記録されています。除外基準 EXCL17 (過去5年以内の重篤な心血管系障害) に該当しないと判断された根拠についてご確認ください。
        *   **クエリ文面（英語）:** Medical history includes Myocardial Infarction (2000), Triple Vessel Bypass Graft (2006), and Extrasystoles. Please confirm the rationale for determining these did not meet Exclusion Criterion EXCL17 (serious cardiovascular disorder within last 5 years).
        *   **判断理由:** 除外基準該当性の判断根拠を確認し、参加者の安全性確保と適格性評価の妥当性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 [17]
    *   **クエリNo.:** Q-11 (関連指摘No.: P-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬として「HYDROCORTISONE, TOPICAL」が Day 32 から Day 48 まで記録されていますが、使用目的（Indication）が記載されていません。プロトコルで規定されているパッチ貼付部位への使用か、あるいは別の治療目的かご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication 'HYDROCORTISONE, TOPICAL' (Day 32-48) is recorded without an indication. Please clarify if this was for application site use as per protocol (Sec 3.6.2) or for another therapeutic purpose.
        *   **判断理由:** 併用薬の使用目的が不明確であり、プロトコル遵守状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='HYDROCORTISONE, TOPICAL', CMINDC='')
            *   関連するプロトコル箇所: Section 3.6.2

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「心室中隔欠損」は先天性疾患であり、AEとしての報告は不適切と思われる。MHへの記載漏れの可能性もあるが、臨床的影響は小さいと判断。データクリーニング時に修正を検討。
        *   **判断理由:** データの一貫性に関する問題だが、安全性や有効性評価への直接的な影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: AE (AETERM='VENTRICULAR SEPTAL DEFECT'), MHドメイン
            *   関連する医学的知見: 心室中隔欠損は先天性心疾患。
    *   **確認事項No.:** I-2 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** AE「脳梗塞の後遺症」の報告について、MHとの関連を確認。MHに明確な脳梗塞の記載はないが、心血管系の既往歴は豊富。ベースラインからの変化であればAE報告も考えられるが、重症度「高度」の根拠は不明。臨床的影響は限定的と判断。
        *   **判断理由:** 報告の妥当性に疑問はあるが、他の重大なイベントに比べ影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: AE (AETERM='LATE EFFECTS OF CEREBRAL INFARCTION'), MHドメイン
    *   **確認事項No.:** I-3 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** Day 50のNPI-X評価で幻覚の有無(NPITM02)の記録が欠損している。他の関連項目(頻度、重症度等)は記録あり。データ入力漏れの可能性が高い。評価への影響は軽微。
        *   **判断理由:** データ欠損だが、他の項目から状況は推測可能であり、評価への影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSDY=50, QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', QSSCAT='HALLUCINATIONS')
    *   **確認事項No.:** I-4 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CM「HYDROCORTISONE, TOPICAL」の標準化コード(CMDECOD, CMCLAS)が欠損。データ標準化プロセスで対応する。
        *   **判断理由:** データ品質の問題であり、標準化プロセスで修正可能。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='HYDROCORTISONE, TOPICAL')
    *   **確認事項No.:** I-5 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** SUPPAEの治療期発現フラグ(AETRTEM)が、先天性疾患や後遺症と思われるAEにも 'Y' と付与されている。フラグ付与ロジックを確認する必要があるが、個々の症例評価への影響は小さい。
        *   **判断理由:** 導出フラグの妥当性確認が必要だが、直接的な安全性・有効性評価への影響は限定的。
        *   **判断根拠:**
            *   関連するデータ: SUPPAE (QNAM='AETRTEM'), AEドメイン
    *   **確認事項No.:** I-6 (関連指摘No.: D-10)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** RELRECドメインのRELTYPEが空欄。関連性の種類が不明だが、現状のレビューではRELIDのみで関連を追跡可能。
        *   **判断理由:** 情報欠損だが、レビューへの影響は限定的。
        *   **判断根拠:**
            *   関連するデータ: RELRECドメイン
    *   **確認事項No.:** I-7 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 14のBUN一過性上昇。Day 27には正常化しており、臨床的に大きな問題とは考えにくい。
        *   **判断理由:** 一過性の検査値異常であり、臨床的意義は低いと判断。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='BUN', LBDY=14, 27)
    *   **確認事項No.:** I-8 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 14, 27のアルブミン低値。軽度であり、他の肝機能検査値は正常範囲内。臨床的意義は低いと判断。
        *   **判断理由:** 軽度の検査値異常であり、他の所見と合わせて総合的に問題なしと判断。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='ALB', LBDY=14, 27), 他の肝機能検査データ
    *   **確認事項No.:** I-9 (関連指摘No.: DS)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** Day 27に "FINAL LAB VISIT" というDisposition Eventが記録されている。プロトコル外のVisitであり、早期中止に関連する検査と思われるが、記録方法として適切か内部で確認。
        *   **判断理由:** 記録方法の標準化に関する内部確認事項。
        *   **判断根拠:**
            *   関連するデータ: DS (DSDECOD='FINAL LAB VISIT')
    *   **確認事項No.:** I-10 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** NPI-Xの評価間隔が一部プロトコル規定（2週間隔）から逸脱している。評価の信頼性への影響は軽微と判断。
        *   **判断理由:** 軽微なスケジュール逸脱であり、評価への影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)') の QSDY
            *   関連するプロトコル箇所: Section 3.9.1.1

Error generating content for 01-703-1042: Invalid operation: The `response.parts` quick accessor requires a single candidate, but but `response.candidates` is empty.

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 81歳、性別は女性、人種は白色人種、民族はヒスパニックまたはラティーノではない。本試験ではXanomeline Low Dose群に割り付けられた (計画/実績)。治験薬初回投与日は2012年9月7日 (Day 1)、最終投与日は2012年9月16日 (Day 10)。有害事象により2012年9月17日 (Day 11) に治験を中止した。最終観察日は2013年2月22日 (Day 169)。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2009年04月04日|N/A|既往歴: アルツハイマー病 (Primary Diagnosis)|
|2012年07月08日|Day -61|既往歴/AE: 限局性感染症 (Localized infection, Moderate) 発現 (継続中)。同日より併用薬 KEFLEX (セファレキシン) 500mg QID 経口投与開始 (継続中)。|
|2012年08月25日|Day -13 (SCREENING 1)|MMSE Total Score: 23 (Recall 0/3)。Modified Hachinski Ischemic Score: 1。検査: 赤血球数 3.8 TI/L (基準値下限未満)。既往歴: 高血圧症、甲状腺機能低下症など多数あり。併用薬: Lisinopril, Motrin (PRN), Premarin, Provera, Synthroid (いずれも継続中)。|
|2012年09月02日|Day -5|AE: 紅斑 (Erythema, Mild)、そう痒症 (Pruritus, Mild) 発現。|
|2012年09月02日|Day -5|併用薬: HYDROCORTISONE, TOPICAL 1 VIAL PRN 局所投与開始。|
|2012年09月04日|Day -3|併用薬: HYDROCORTISONE, TOPICAL 投与終了。|
|2012年09月05日|Day -2 (SCREENING 2)|バイタルサイン: 立位時脈拍 94 (1分後), 89 (3分後) と臥位 (84) から上昇。|
|2012年09月07日|Day 1 (BASELINE)|治験薬 XANOMELINE 54 mg PATCH QD TRANSDERMAL 投与開始。AE: 紅斑、そう痒症 軽快/回復。AE: 尿意切迫 (Micturition Urgency, Mild) 発現 (継続中)。ADAS-Cog(11) Total Score: 7。NPI-X Total Score: 2 (Agitation/Aggression=1, Disinhibition=1)。|
|2012年09月13日|Day 7|AE: 関節痛 (Arthralgia, Moderate)、蜂巣炎 (Cellulitis, Moderate) 発現 (いずれも継続中)。|
|2012年09月16日|Day 10|治験薬 XANOMELINE 投与終了。|
|2012年09月17日|Day 11 (WEEK 2)|Disposition: 有害事象 (関節痛、蜂巣炎) により治験中止。検査: 赤血球数 3.7 TI/L (基準値下限未満、ベースラインから低下)、MCV 101 fL (基準値上限超え)、尿比重 1.004 (基準値下限未満)、Anisocytes 1+ (異常)。バイタルサイン: 立位時収縮期血圧低下傾向 (臥位125→立位112/110 mmHg)。ADAS-Cog(11) Total Score: 5 (ベースラインから改善)。CIBIC+: 4 (No Change)。NPI-X Total Score: 1 (ベースラインから改善)。|
|2012年09月29日|Day 23 (AE FOLLOW-UP)|AEフォローアップのための来院。|
|2013年02月22日|Day 169 (RETRIEVAL)|最終観察来院。ADAS-Cog(11) Total Score: 9 (ベースラインから悪化)。CIBIC+: 5 (Minimal Worsening)。NPI-X Total Score: 45 (ベースライン/Week 2から著しく悪化、特に妄想、興奮/攻撃性、抑うつ、不安、脱抑制、易刺激性)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 11の治験中止理由とされた有害事象「関節痛 (ARTHRALGIA)」および「蜂巣炎 (CELLULITIS)」(いずれもDay 7発現、Moderate) について、治験薬との関連性が「NONE」と評価されている。これらのAEは治験薬投与期間中に発現しており、特に蜂巣炎は感染症であるが、関節痛については治験薬との関連を完全に否定できるか疑問が残る。中止の判断に至ったAEの評価として、関連性評価の根拠が不明確である。
        *   **根拠:** 有害事象の発現時期と治験薬投与期間の重複。治験中止の判断に影響する重要な評価であるため。一般的な医学知識として、薬剤による関節痛は起こりうる。
        *   **関連データ:**
            *   [報告された有害事象の用語(AE.AETERM)] = 'ARTHRALGIA', 'CELLULITIS'
            *   [有害事象開始日(Study Day)(AE.AESTDY)] = 7
            *   [重症度/強度(AE.AESEV)] = 'MODERATE'
            *   [因果関係(AE.AEREL)] = 'NONE'
            *   [標準化された処置用語(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [処置の開始日(Study Day)(DS.DSSTDY)] = 11
            *   [治験薬投与開始日(Study Day)(EX.EXSTDY)] = 1
            *   [治験薬投与終了日(Study Day)(EX.EXENDY)] = 10
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11) のバイタルサイン測定において、臥位から立位への体位変換後に収縮期血圧の低下傾向（臥位125mmHg、立位1分後112mmHg、3分後110mmHg）が認められる。ベースライン（臥位129mmHg、立位1分後136mmHg、3分後135mmHg）と比較して立位収縮期血圧が20mmHg以上低下しており、起立性低血圧の可能性がある。Xanomelineはコリン作動薬であり、起立性低血圧は既知の副作用となりうる。この所見が有害事象として評価・報告されていない。
        *   **根拠:** バイタルサインの測定結果とベースラインからの変化。治験薬（Xanomeline）の薬理作用（コリン作動性）と既知の副作用プロファイル。参加者の安全性（転倒リスク等）に関わる可能性がある。
        *   **関連データ:**
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure'
            *   [測定の実施日(Study Day)(VS.VSDY)] = 11
            *   [バイタルサインの被験者の位置(VS.VSPOS)] = 'SUPINE', 'STANDING'
            *   [標準単位での数値結果/所見(VS.VSSTRESN)] = 125 (Supine), 112 (Standing 1min), 110 (Standing 3min)
            *   AEドメインに起立性低血圧や関連する症状（めまい等）の報告なし。
    *   **指摘No.:** M-3
        *   **重要度:** Critical
        *   **内容:** Retrieval Visit (Day 169) で評価されたNPI-Xスコアが、ベースラインの2点、Week 2の1点から45点へと著しく悪化している。特に妄想 (Score 12)、興奮/攻撃性 (Score 8)、抑うつ/不快気分 (Score 3)、不安 (Score 6)、脱抑制 (Score 12)、易刺激性/情緒不安定 (Score 4) の項目で高いスコアが記録されている。この著しい精神症状の悪化は、治験薬中止後のリバウンド現象、疾患の自然経過、あるいは他の要因によるものか不明だが、臨床的に非常に重要であり、参加者の状態や介護者の負担増大を示唆する。この悪化が有害事象として評価・報告されていない。
        *   **根拠:** NPI-Xスコアの著しい悪化。アルツハイマー病の精神症状は重要であり、その急激な悪化は参加者の安全性とQOLに重大な影響を与える可能性がある。治験薬中止との時間的関連も考慮する必要がある。
        *   **関連データ:**
            *   [質問票名(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [質問票の実施日(Study Day)(QS.QSDY)] = 1, 11, 169
            *   [質問票の短い名前(QS.QSTESTCD)] = 'NPTOT' (Total Score), 'NPITM01S' (Delusions), 'NPITM03S' (Agitation/Aggression), 'NPITM04S' (Depression/Dysphoria), 'NPITM05S' (Anxiety), 'NPITM08S' (Disinhibition), 'NPITM09S' (Irritability/Lability)
            *   [標準単位での数値結果/所見(QS.QSSTRESN)] = NPTOT: 2 (Day 1), 1 (Day 11), 45 (Day 169); NPITM01S: 0 (Day 1), 0 (Day 11), 12 (Day 169); NPITM03S: 1 (Day 1), 0 (Day 11), 8 (Day 169); NPITM04S: 0 (Day 1), 0 (Day 11), 3 (Day 169); NPITM05S: 0 (Day 1), 0 (Day 11), 6 (Day 169); NPITM08S: 1 (Day 1), 1 (Day 11), 12 (Day 169); NPITM09S: 0 (Day 1), 0 (Day 11), 4 (Day 169)
            *   AEドメインにこれらの精神症状悪化に関する報告なし。
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11) の血液検査で、赤血球数 (RBC) が3.7 TI/Lとベースライン (3.8 TI/L) からさらに低下し基準値下限 (3.9 TI/L) を下回り、平均赤血球容積 (MCV) が101 fLとベースライン (97 fL) から上昇し基準値上限 (100 fL) を超えている。大球性貧血の可能性を示唆する所見である。治験薬との関連は不明だが、臨床的に意義のある変化の可能性があり、原因精査やフォローアップが必要。Retrieval Visit (Day 169) での検査データがなく、転帰が不明である。
        *   **根拠:** 検査値の基準値逸脱とベースラインからの変化。貧血は参加者の全身状態に影響を与える可能性がある。原因によっては治験薬との関連も考慮する必要がある。
        *   **関連データ:**
            *   [検査項目名(LB.LBTEST)] = 'Erythrocytes', 'Ery. Mean Corpuscular Volume'
            *   [検査測定値(LB.LBSTRESN)] = RBC: 3.8 (Day -13), 3.7 (Day 11); MCV: 97 (Day -13), 101 (Day 11)
            *   [基準範囲指標(LB.LBNRIND)] = RBC: LOW (Day -13, Day 11); MCV: NORMAL (Day -13), HIGH (Day 11)
            *   [既往歴の報告用語(MH.MHTERM)] = 'HYPOTHYROIDISM' (甲状腺機能低下症は貧血の原因となりうるが、TSHは正常)
            *   除外基準 [28b] (VitB12/Folate低値) は満たしているはず。

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11) のバイタルサインで起立性低血圧を示唆する所見があるが、AEドメインに対応する報告がない。医学的評価に影響を与える可能性のあるデータの不整合。
        *   **根拠:** VSドメインとAEドメイン間のデータの不一致。
        *   **関連データ:**
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure'
            *   [測定の実施日(Study Day)(VS.VSDY)] = 11
            *   [標準単位での数値結果/所見(VS.VSSTRESN)] = 125 (Supine), 112 (Standing 1min), 110 (Standing 3min)
            *   AEドメインに起立性低血圧や関連症状の報告なし。
    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** Retrieval Visit (Day 169) のNPI-Xスコアで精神症状の著しい悪化が示されているが、AEドメインに対応する報告がない。安全性評価の妥当性に重大な影響を与える可能性のあるデータの不整合。
        *   **根拠:** QSドメインとAEドメイン間のデータの不一致。
        *   **関連データ:**
            *   [質問票名(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [質問票の実施日(Study Day)(QS.QSDY)] = 169
            *   [質問票の短い名前(QS.QSTESTCD)] = 'NPTOT'
            *   [標準単位での数値結果/所見(QS.QSSTRESN)] = 45
            *   AEドメインに精神症状悪化の報告なし。
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** プロトコルで規定されているScreeningおよびVisit 4のECG、Visit 2のAmbulatory ECG、Visit 3およびVisit 4の薬物動態測定（PK）のデータが提供されていない。これらのデータは安全性評価（特に心血管系）およびPK評価に不可欠であり、欠損している場合、評価の信頼性が損なわれる。
        *   **根拠:** 必須評価項目のデータ欠損。
        *   **関連データ:**
            *   ECG, PKに関連するドメインデータなし。
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** DM.RFENDTC (Subject Reference End Date/Time) が '2012-09-17' (Day 11) と記録されているが、Define.xmlのCommentでは "Date/time of last study drug treatment derived from EX" と記載されており、EX.EXENDTC (Date/Time of Last Study Treatment) '2012-09-16' (Day 10) と一致すべきである。データとメタデータの定義に不整合がある。
        *   **根拠:** DMドメインのデータとDefine.xmlの定義との不一致。
        *   **関連データ:**
            *   [被験者参照終了日時(DM.RFENDTC)] = '2012-09-17'
            *   [治験薬投与終了日時(EX.EXENDTC)] = '2012-09-16'
            *   Define.xml ItemDef OID="DM.RFENDTC" Comment
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 中止理由となったAE (ARTHRALGIA, CELLULITIS) の開始日 (AESTDY=7) と、Disposition Event (ADVERSE EVENT) の記録日 (DSSTDY=11) に4日間のずれがある。RELRECで関連付けられているが、日付が異なる。
        *   **根拠:** AEドメインとDSドメイン間の日付データの不一致。
        *   **関連データ:**
            *   [有害事象開始日(Study Day)(AE.AESTDY)] = 7 (AESEQ=7, 8)
            *   [処置の開始日(Study Day)(DS.DSSTDY)] = 11 (DSSEQ=1)
            *   RELRECデータ
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** SVドメインにおいて、Visit 101 (AE FOLLOW-UP) および Visit 501 (Rash followup) の計画日 (VISITDY) が欠損している。TVドメインの定義でもnullのためデータとしては整合しているが、フォローアップの計画日が不明確である。
        *   **根拠:** SVドメインの必須情報（計画日）の欠損。
        *   **関連データ:**
            *   [来院番号(SV.VISITNUM)] = 101, 501
            *   [来院予定日(Study Day)(SV.VISITDY)] = null
            *   [来院番号(TV.VISITNUM)] = 101, 501
            *   [来院予定日(Study Day)(TV.VISITDY)] = null

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [14] (過去5年以内の精神疾患) への抵触の可能性。既往歴として「EATING DISORDER」が2009年に記録されている。プロトコルではSchizophrenia, Bipolar, Substance abuseが例示されているが、Eating disorderが"Mental illness"に該当するか確認が必要。ただし、発症が5年以上前のため、抵触しない可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [14]
        *   **根拠:** MHデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0702' (EATING DISORDER)
            *   [既往歴イベントの開始日時(MH.MHSTDTC)] = '2009'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [21] (過去5年以内の重篤な泌尿生殖器疾患) への抵触の可能性。既往歴として「BLADDER INFECTION」(2002年)、「INCONTINENCE」(2006年)が記録されている。これらが"Serious"に該当するか確認が必要。ただし、発症が5年以上前のため、抵触しない可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [21]
        *   **根拠:** MHデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0361' (BLADDER INFECTION), 'VERBATIM_1545' (INCONTINENCE)
            *   [既往歴イベントの開始日時(MH.MHSTDTC)] = '2002', '2006'
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [24] (過去5年以内の重篤な感染症) への抵触の可能性。既往歴として「LOCALIZED INFECTION」が2012年7月8日（Study Day -61）に記録されている。治験開始直前であり、これが"Serious"に該当するか確認が必要。ModerateのAEとして記録されており、併用薬(Keflex)も投与されているため、重篤ではない可能性が高いが、確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [24]
        *   **根拠:** MHデータとプロトコル除外基準の照合。発症時期が治験開始直前であるため。
        *   **関連データ:**
            *   [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_1224' (LOCALIZED INFECTION)
            *   [既往歴イベントの開始日時(MH.MHSTDTC)] = '2012-07-08'
            *   [重症度/強度(MH.MHSEV)] = 'MILD' (Significant Pre-existing Conditionとして) / [重症度/強度(AE.AESEV)] = 'MODERATE' (AEとして)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された評価（ECG, Ambulatory ECG, PK）が実施されていない、またはデータが報告されていない可能性。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 (Cardiovascular Safety Measures), Section 3.9.2 (Pharmacokinetics), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 必須評価項目のデータ欠損。
        *   **関連データ:**
            *   ECG, PKに関連するドメインデータなし。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-3, D-2)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 169のNPI-X評価において、合計スコアがベースラインの2点から45点へと著しく増加しており、特に妄想、興奮/攻撃性、抑うつ、不安などの項目で悪化が見られます。この精神症状の悪化について臨床的に評価いただき、有害事象としての報告が必要かご判断ください。
        *   **クエリ文面（英語）:** On Study Day 169 NPI-X, the total score markedly increased to 45 from baseline 2, with worsening in delusions, agitation/aggression, depression, anxiety etc. Please clinically evaluate this worsening of psychiatric symptoms and determine if AE reporting is required.
        *   **判断理由:** 参加者の精神状態の著しい悪化が示唆されており、安全性評価および適切な対応（AE報告含む）が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [質問票名(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', [質問票の実施日(Study Day)(QS.QSDY)] = 169, [質問票の短い名前(QS.QSTESTCD)] = 'NPTOT', [標準単位での数値結果/所見(QS.QSSTRESN)] = 45
            *   関連するプロトコル箇所: Section 3.9.3.2 (Clinical Adverse Events)
            *   関連する医学的知見: アルツハイマー病における精神症状の変動、薬剤離脱症状の可能性。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象名「ARTHRALGIA」および「CELLULITIS」について、治験中止の理由とされていますが、治験薬との関連性が「NONE」と評価されています。評価根拠について詳細をご教示ください。
        *   **クエリ文面（英語）:** Regarding AEs 'ARTHRALGIA' and 'CELLULITIS', which led to study discontinuation, causality is assessed as 'NONE'. Please provide details on the assessment basis.
        *   **判断理由:** 治験中止理由となったAEの関連性評価の妥当性を確認し、安全性評価の信頼性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [報告された有害事象の用語(AE.AETERM)] = 'ARTHRALGIA', 'CELLULITIS', [因果関係(AE.AEREL)] = 'NONE', [標準化された処置用語(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   関連するプロトコル箇所: Section 3.9.3.2 (Clinical Adverse Events)
            *   関連する医学的知見: 薬剤誘発性関節痛の可能性。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-2, D-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11のバイタルサインにおいて、臥位から立位への体位変換後に収縮期血圧の低下傾向（臥位125mmHg、立位1分後112mmHg、3分後110mmHg）が認められます。起立性低血圧の可能性について評価いただき、有害事象としての報告が必要かご判断ください。
        *   **クエリ文面（英語）:** On Study Day 11 VS, a decrease in systolic BP upon standing was noted (Supine 125mmHg, Standing 1min 112mmHg, 3min 110mmHg). Please assess for potential orthostatic hypotension and determine if AE reporting is required.
        *   **判断理由:** 潜在的な安全性リスク（起立性低血圧）の評価と、必要に応じたAE報告を促すため。
        *   **判断根拠:**
            *   関連するデータ: [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure', [測定の実施日(Study Day)(VS.VSDY)] = 11, [標準単位での数値結果/所見(VS.VSSTRESN)] = 125, 112, 110
            *   関連するプロトコル箇所: Section 3.9.3.2 (Clinical Adverse Events), Section 3.9.3.4.1 (Vital Sign Determination)
            *   関連する医学的知見: コリン作動薬による起立性低血圧の可能性。
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11の検査結果において、赤血球数が3.7 TI/Lと低値、MCVが101 fLと高値を示しています。これらの所見の臨床的意義と、その後の転帰（Retrieval Visit等でのフォローアップ結果）についてご教示ください。
        *   **クエリ文面（英語）:** On Study Day 11 labs, RBC was low (3.7 TI/L) and MCV was high (101 fL). Please provide the clinical significance and outcome (e.g., follow-up results at Retrieval Visit) of these findings.
        *   **判断理由:** 臨床的に意義のある可能性のある検査値異常の原因と転帰を確認し、参加者の安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [検査項目名(LB.LBTEST)] = 'Erythrocytes', 'Ery. Mean Corpuscular Volume', [検査測定値(LB.LBSTRESN)] = 3.7, 101, [基準範囲指標(LB.LBNRIND)] = 'LOW', 'HIGH'
            *   関連するプロトコル箇所: Section 3.9.3.3 (Clinical Laboratory Tests)
            *   関連する医学的知見: 大球性貧血の原因検索の必要性。
    *   **クエリNo.:** Q-5 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「LOCALIZED INFECTION」が2012年7月8日（Study Day -61）に記録されています。プロトコル除外基準24（過去5年以内の重篤な感染症）に該当しないかご確認ください。特に、"Serious"（重篤）な感染症ではなかったことの確認をお願いします。
        *   **クエリ文面（英語）:** Medical history notes 'LOCALIZED INFECTION' on 2012-07-08 (Study Day -61). Please confirm if this meets exclusion criterion 24 (Serious infectious disease within last 5 years), specifically confirming it was not considered 'Serious'.
        *   **判断理由:** 治験開始直前の感染症であり、除外基準抵触の可能性を明確に否定する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_1224', [既往歴イベントの開始日時(MH.MHSTDTC)] = '2012-07-08'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [24]
    *   **クエリNo.:** Q-6 (関連指摘No.: D-3, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているScreeningおよびVisit 4のECG、Visit 2のAmbulatory ECG、Visit 3およびVisit 4の薬物動態測定（PK）のデータが提供されていません。実施状況とデータ提供についてご確認ください。未実施の場合はその理由をお知らせください。
        *   **クエリ文面（英語）:** Data for protocol-specified ECG (Screening, Visit 4), Ambulatory ECG (Visit 2), and PK (Visit 3, 4) are missing. Please confirm if performed and provide data, or provide reason if not performed.
        *   **判断理由:** プロトコル遵守状況の確認と、安全性・PK評価に必要なデータの収集のため。
        *   **判断根拠:**
            *   関連するデータ: ECG, PKに関連するドメインデータなし。
            *   関連するプロトコル箇所: Section 3.9.3.4.2, Section 3.9.2, Attachment LZZT.1
    *   **クエリNo.:** Q-7 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「EATING DISORDER」が2009年に記録されています。プロトコル除外基準14（過去5年以内の精神疾患）に該当しないかご確認ください。
        *   **クエリ文面（英語）:** Medical history notes 'EATING DISORDER' in 2009. Please confirm if this meets exclusion criterion 14 (Mental illness within last 5 years).
        *   **判断理由:** 除外基準抵触の可能性を念のため確認するため。
        *   **判断根拠:**
            *   関連するデータ: [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0702', [既往歴イベントの開始日時(MH.MHSTDTC)] = '2009'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [14]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「BLADDER INFECTION」(2002年)、「INCONTINENCE」(2006年)が記録されています。プロトコル除外基準21（過去5年以内の重篤な泌尿生殖器疾患）に該当しないかご確認ください。
        *   **クエリ文面（英語）:** Medical history notes 'BLADDER INFECTION' (2002) and 'INCONTINENCE' (2006). Please confirm if these meet exclusion criterion 21 (Serious GU disorder within last 5 years).
        *   **判断理由:** 除外基準抵触の可能性を念のため確認するため。
        *   **判断根拠:**
            *   関連するデータ: [既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0361', 'VERBATIM_1545', [既往歴イベントの開始日時(MH.MHSTDTC)] = '2002', '2006'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [21]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** DM.RFENDTC (Subject Reference End Date/Time) が '2012-09-17' (Day 11) と記録されているが、Define.xmlのCommentに基づくとEX.EXENDTC (Date/Time of Last Study Treatment) '2012-09-16' (Day 10) と一致すべき。データとメタデータの定義に不整合がある。
        *   **判断理由:** データとメタデータの不整合だが、日付が1日違いであり、治験中止日 (Day 11) と一致しているため、臨床的な解釈への影響は小さいと判断。内部記録に留める。
        *   **判断根拠:**
            *   関連するデータ: [被験者参照終了日時(DM.RFENDTC)] = '2012-09-17', [治験薬投与終了日時(EX.EXENDTC)] = '2012-09-16'
            *   関連するプロトコル箇所: なし (Define.xmlの定義との不整合)
    *   **確認事項No.:** I-2 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 中止理由となったAE (ARTHRALGIA, CELLULITIS) の開始日 (AESTDY=7) と、Disposition Event (ADVERSE EVENT) の記録日 (DSSTDY=11) に4日間のずれがある。
        *   **判断理由:** AE発生から中止決定・記録までにタイムラグが生じることは臨床的にあり得るため、許容範囲内と判断。内部記録に留める。
        *   **判断根拠:**
            *   関連するデータ: [有害事象開始日(Study Day)(AE.AESTDY)] = 7, [処置の開始日(Study Day)(DS.DSSTDY)] = 11
            *   関連するプロトコル箇所: なし
    *   **確認事項No.:** I-3 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** SVドメインにおいて、Visit 101 (AE FOLLOW-UP) および Visit 501 (Rash followup) の計画日 (VISITDY) が欠損している。
        *   **判断理由:** TVドメインの定義でもnullのためデータとしては整合している。実施日は記録されており、評価への影響は限定的と判断。内部記録に留める。
        *   **判断根拠:**
            *   関連するデータ: [来院番号(SV.VISITNUM)] = 101, 501, [来院予定日(Study Day)(SV.VISITDY)] = null
            *   関連するプロトコル箇所: Attachment LZZT.1 (Schedule of Eventsでは計画日が明記されていない)