# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    77歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年03月27日発症、PRIMARY DIAGNOSIS）、心筋梗塞（2000年05月15日発症、HISTORICAL DIAGNOSIS）、冠動脈バイパス術（2006年12月16日実施、HISTORICAL DIAGNOSIS）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2013年09月20日|Day -16 (Visit 1)|スクリーニング開始。MMSEスコア21、Hachinskiスコア0。既往歴としてアルツハイマー病、心筋梗塞、冠動脈バイパス術あり。検査値にてクレアチニンが1.8 mg/dLと基準値上限(1.6 mg/dL)を超過 (HIGH)。|
|2013年09月27日|Day -9 (Visit 2)|スクリーニング継続。|
|2013年10月06日|Day 1 (Visit 3)|治験薬 Xanomeline 54 mg/day 投与開始。ベースライン評価実施。ADAS-Cog(11)スコア 27、NPI-X Totalスコア 61。併用薬として PREMARIN 0.625 mg QOD 開始。|
|2013年10月18日|Day 13 (Visit 3.5)|AMBUL ECG PLACEMENT実施。|
|2013年10月19日|Day 14 (Visit 4)|有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」(重症度 SEVERE、関連性 NONE) 発現。有害事象「MYOCARDIAL INFARCTION」(重症度 MILD、関連性 NONE) 発現。有害事象「VENTRICULAR SEPTAL DEFECT」(重症度 MILD、関連性 NONE) 発現。検査値にてBUNが29 mg/dLと基準値上限(24 mg/dL)を超過 (HIGH)、アルブミンが3.3 g/dLと基準値下限(3.5 g/dL)未満 (LOW)。血圧・脈拍がベースラインより低下傾向 (臥位 112/60 mmHg, 68 bpm)。起立性低血圧の可能性あり (立位3分 104/56 mmHg)。NPI-X Totalスコア 22 (ベースラインから改善)。|
|2013年10月20日|Day 15 (N/A)|治験薬 Xanomeline 81 mg/day へ増量。|
|2013年10月29日|Day 24 (N/A)|併用薬 PREMARIN 終了。|
|2013年11月01日|Day 27 (N/A)|検査実施 (DSドメインに 'FINAL LAB VISIT' の記録あり)。アルブミン 3.4 g/dL (LOW)、クレアチニン 1.6 mg/dL (正常上限)、BUN 23 mg/dL (正常上限)。|
|2013年11月05日|Day 31 (N/A)|有害事象「PRURITUS」(重症度 MILD、関連性 PROBABLE) 発現。有害事象「RASH」(重症度 MILD、関連性 PROBABLE) 発現。|
|2013年11月06日|Day 32 (N/A)|併用薬 HYDROCORTISONE, TOPICAL 開始 (Rash/Pruritusに対する処置と推測)。|
|2013年11月09日|Day 35 (Visit 5)|血圧・脈拍はDay 14より回復傾向 (臥位 124/66 mmHg, 72 bpm)。NPI-X Totalスコア 38 (Day 14から悪化)。|
|2013年11月18日|Day 44 (N/A)|有害事象「BRAIN DEATH」(重症度 SEVERE、関連性 NONE) 発現、同日回復 (RECOVERED/RESOLVED) と記録 (医学的に不整合)。治験薬 Xanomeline 投与終了。|
|2013年11月19日|Day 45 (N/A)|有害事象「MYOCARDIAL INFARCTION」回復。|
|2013年11月22日|Day 48 (N/A)|有害事象「PRURITUS」回復。有害事象「RASH」回復。併用薬 HYDROCORTISONE, TOPICAL 終了。|
|2013年11月24日|Day 50 (Visit 7)|治験中止 (理由: ADVERSE EVENT)。ADAS-Cog(11)スコア 30 (ベースラインから悪化)。CIBIC+スコア 4 (NO CHANGE)。NPI-X Totalスコア 16 (Day 35から改善)。NPI-Xにて「HALLUCINATIONS」が新たに出現。|
|2013年12月06日|Day 62 (Visit 101)|AE FOLLOW-UP Visit。最終観察日。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「BRAIN DEATH」がDay 44に発現し、同日に「RECOVERED/RESOLVED」として報告されている。Brain Deathは死亡であり回復することは医学的にありえないため、事象名、転帰、日付のいずれか、またはすべてが誤っている可能性が極めて高い。参加者の実際の状態と転帰の確認が最優先事項である。
        *   **根拠:** Brain Deathの医学的定義と転帰に関する一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Subject Death Flag(DM.DTHFL)] = '' (記録なし)
            *   [Date/Time of Death(DM.DTHDTC)] = '' (記録なし)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「MYOCARDIAL INFARCTION」がDay 14に発現。重症度が「MILD」と評価されているが、心筋梗塞としては軽微すぎる評価の可能性がある。また、治験薬との関連性が「NONE」と評価されているが、治験薬開始後14日目の発現であり、特にコリン作動薬の心血管系への影響を考慮すると、関連性の再評価が必要かもしれない。さらに、処置として「DRUG WITHDRAWN」と記録されているが、実際の治験薬投与終了日(Day 44)や治験中止日(Day 50)と時期が一致せず、中止判断の経緯が不明確である。
        *   **根拠:** 心筋梗塞の一般的な重症度分類、コリン作動薬の潜在的な心血管系副作用に関する医学知識、データ間の不整合。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-19'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-11-18'
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」がDay 14に重症度「SEVERE」で発現。既往歴（心筋梗塞、冠動脈バイパス術）から脳血管イベントのリスクは高いと考えられるが、治験薬開始直後の重症イベントであり、治験薬との関連性評価「NONE」が妥当か、詳細な臨床経過の確認が必要。
        *   **根拠:** 脳血管イベントのリスク因子と発症時期に関する医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Causality(AE.AEREL)] = 'NONE'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 有害事象「VENTRICULAR SEPTAL DEFECT」がDay 14に発現。77歳男性における心室中隔欠損の新規発症は通常考えにくく、先天性の顕在化、心筋梗塞等の合併症、あるいは診断・報告誤りの可能性を考慮する必要がある。診断根拠と発症経緯の確認が必要。
        *   **根拠:** 心室中隔欠損症の病態に関する医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「RASH」および「PRURITUS」がDay 31に発現し、Day 48に回復。治験薬との関連性は「PROBABLE」と評価。プロトコルにも記載されているXanomeline TTSで予想される有害事象。DSの中止理由と関連付けられているが、重症度・転帰から主要な中止理由かは疑問。
        *   **根拠:** プロトコル記載情報、AEの重症度と転帰。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS', 'RASH'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-05'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-22'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Causality(AE.AEREL)] = 'PROBABLE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** スクリーニング時(Day -16)のクレアチニン値が1.8 mg/dLと基準値上限(1.6 mg/dL)を超過しており、プロトコルの除外基準 EXCL27b に抵触する可能性がある。その後の測定では正常上限値に戻っているが、スクリーニング時の値の臨床的意義と適格性評価の妥当性について確認が必要。
        *   **根拠:** プロトコル除外基準、検査値の臨床的意義に関する医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** Day 14のBUN値が29 mg/dLと基準値上限(24 mg/dL)を超過。Day 27には正常上限に戻っている。クレアチニン値の変動と合わせて腎機能や脱水等の可能性を考慮する必要があるが、一過性の変動の可能性もある。
        *   **根拠:** 検査値の臨床的意義に関する医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 14
            *   [Result or Finding in Original Units(LB.LBORRES)] = '29'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '24'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** Day 14およびDay 27のアルブミン値が基準値下限(3.5 g/dL)未満 (3.3, 3.4 g/dL)。低アルブミン血症。臨床的意義は不明だが、栄養状態や肝腎機能との関連を考慮。
        *   **根拠:** 検査値の臨床的意義に関する医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 14, 27
            *   [Result or Finding in Original Units(LB.LBORRES)] = '3.3', '3.4'
            *   [Reference Range Lower Limit in Orig Unit(LB.LBORNRLO)] = '3.5'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** M-9
        *   **重要度:** Major
        *   **内容:** Day 14に血圧低下（ベースライン臥位144/70→Day 14臥位112/60）および起立性低血圧を示唆する所見（立位3分で収縮期-40mmHg）を認める。脈拍も低下傾向。Xanomeline（コリン作動薬）の薬理作用の可能性があり、安全性上の懸念がある。その後のVisitでは回復傾向が見られる。
        *   **根拠:** コリン作動薬の薬理作用、バイタルサインの臨床的意義に関する医学知識。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', 'DIABP', 'PULSE'
            *   [Study Day of Vital Signs(VS.VSDY)] = 1, 14, 35, 50
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = (各値)
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', 'STANDING'
    *   **指摘No.:** M-10
        *   **重要度:** Major
        *   **内容:** 併用薬 PREMARIN (Estrogens Conjugated) がDay 1からDay 24まで投与されている。プロトコルではエストロゲン補充療法は許可されているが、「dosage must be stable for at least 3 months prior to enrollment」という条件がある。Day 1からの開始はこの条件を満たしておらず、プロトコル違反（除外基準 EXCL31b [v] 抵触）の可能性がある。
        *   **根拠:** プロトコル規定 (3.4.2.2 [31v])。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2013-10-29'
    *   **指摘No.:** M-11
        *   **重要度:** Minor
        *   **内容:** Day 50のNPI-X評価で、ベースラインでは報告のなかった「HALLUCINATIONS」が新たに出現している。治験薬との関連性を考慮する必要がある。
        *   **根拠:** 有効性評価指標の変化。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM02F', 'NPITM02V'
            *   [Study Day of Finding(QS.QSDY)] = 50
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1, 1
    *   **指摘No.:** M-12
        *   **重要度:** Minor
        *   **内容:** 有効性評価の結果に一貫性が見られない（ADAS-Cog悪化、CIBIC+不変、NPI-X改善）。ただし、評価期間が短く（Day 50で中止）、評価時期も限られているため、明確な有効性の判断は困難。
        *   **根拠:** 複数の有効性評価指標間の結果比較。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'NPTOT'
            *   [Study Day of Finding(QS.QSDY)] = 1, 50
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = (各値)
    *   **指摘No.:** M-13
        *   **重要度:** Critical
        *   **内容:** 本症例では、短期間に複数の重篤となりうるAE（心筋梗塞、脳梗塞後遺症疑い、心室中隔欠損疑い、医学的にありえない脳死報告）が発生しており、データの質と信頼性、特にAE報告の正確性に重大な懸念がある。また、治験薬中止の判断経緯、スクリーニング時の除外基準抵触の可能性、併用薬に関するプロトコル違反の可能性など、複数の問題点が指摘されており、参加者の安全性が適切に管理され、試験が計画通りに実施されていたか全体として疑問がある。
        *   **根拠:** M-1, M-2, M-3, M-4, M-6, M-10 およびデータ整合性に関する指摘事項 (D-1, D-3, D-9, P-1, P-2, P-6, P-7)。
        *   **関連データ:** AE, LB, CM, DS, DM ドメイン全体。

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「MYOCARDIAL INFARCTION」(AESEQ=1) に関する記録に不整合がある。処置として「DRUG WITHDRAWN」と記録されているが、EXドメインの治験薬最終投与日(EXENDTC=Day 44)と一致しない。また、DSドメインの治験中止イベント(DSDECOD='ADVERSE EVENT', DSSTDY=Day 50)とも時期が異なる。治験薬中止の正確な日付と理由、および中止イベントとの関連が不明確であり、安全性評価の解釈に影響を与える可能性がある。
        *   **根拠:** AE.AEACN, EX.EXENDTC, DS.DSSTDTC, DS.DSDECOD間の日付と内容の不一致。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-11-18' (Day 44)
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** DSドメインの治験中止イベント(DSSEQ=1, DSDECOD='ADVERSE EVENT', DSSTDY=Day 50)が、RELRECドメインを介してAE「RASH」(AESEQ=5, 7)と関連付けられている。しかし、AE「RASH」は重症度「MILD」であり、Day 48に「RECOVERED/RESOLVED」と記録されているため、Day 50の中止理由としては時期と転帰が一致しない。中止の真の理由が不明確であり、安全性評価に影響する。
        *   **根拠:** DS.DSSTDTC, AE.AEENDY, AE.AESEV, AE.AEOUT, RELREC間の情報の不一致。
        *   **関連データ:**
            *   [Sequence Number(DS.DSSEQ)] = 1
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
            *   [Relationship Identifier(RELREC.RELID)] = '01-704-1017-E11'
            *   [Sequence Number(AE.AESEQ)] = 5, 7
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-22' (Day 48)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
    *   **指摘No.:** D-3
        *   **重要度:** Critical
        *   **内容:** 有害事象「BRAIN DEATH」(AESEQ=3) の転帰が「RECOVERED/RESOLVED」と記録されており、医学的にありえない。また、DMドメインに死亡フラグ(DTHFL)や死亡日(DTHDTC)の記録がない。これは重大なデータエラーであり、患者の実際の転帰に関する情報の信頼性を著しく損なう。
        *   **根拠:** AE.AEOUTと医学的事実との矛盾、DMドメインとの不整合。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18' (Day 44)
            *   [Subject Death Flag(DM.DTHFL)] = ''
            *   [Date/Time of Death(DM.DTHDTC)] = ''
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** DSドメインにDay 27の「FINAL LAB VISIT」(DSSEQ=2)が記録されているが、対応するVisit記録がSVドメインに存在しない。LBドメインにはDay 27のデータが存在する。予定外の検査Visitであった可能性が高いが、Visit記録との不整合がある。評価への影響は小さいと考えられる。
        *   **根拠:** DSドメインとSVドメイン間のVisit記録の不一致。
        *   **関連データ:**
            *   [Sequence Number(DS.DSSEQ)] = 2
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-01' (Day 27)
            *   SVドメインにVisitNum=5 (Day 28)はあるが、Day 27に対応するVisitNumなし。
            *   [Study Day of Specimen Collection(LB.LBDY)] = 27 のデータあり。
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 併用薬「PREMARIN」について、Indication(CM.CMINDC)が記録されていない。医学的評価やプロトコル遵守（除外基準）の確認に影響する可能性がある。
        *   **根拠:** CMドメイン内の必須情報の欠損。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Indication(CM.CMINDC)] = ''
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 併用薬「HYDROCORTISONE, TOPICAL」について、Indication(CM.CMINDC)が記録されていない。AE「RASH」「PRURITUS」との関連が推測されるが、記録としては不完全。
        *   **根拠:** CMドメイン内の必須情報の欠損。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Indication(CM.CMINDC)] = ''
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** QSドメインのNPI-X Total Score (QSTESTCD='NPTOT') の算出根拠がDefine.xmlやデータからは不明確（例：9項目合計か全項目合計か）。有効性評価の正確な解釈のために確認が必要。
        *   **根拠:** 評価指標の計算方法の不明瞭さ。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT'
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM01S'...'NPITM12S'
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** AE「PRURITUS」(AESEQ=6, 8) および「RASH」(AESEQ=5, 7) が、異なる収集日(AEDTC)で複数回報告されているように見える（開始日・終了日は同じ）。経過観察のための再評価記録の可能性があるが、データの意図が不明確。
        *   **根拠:** 同一イベントに対する複数レコードの存在。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 5, 6, 7, 8
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH', 'PRURITUS'
            *   [Date/Time of Collection(AE.AEDTC)] = '2013-11-09', '2013-11-24'
    *   **指摘No.:** D-9
        *   **重要度:** Major
        *   **内容:** DMドメインの「Date/Time of Informed Consent」(DM.RFICDTC) が欠損している。治験手順開始前に適切な同意が得られていたかを確認するために必須の情報であり、欠損はGCP遵守の観点から問題となる可能性がある。
        *   **根拠:** 必須情報の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** D-10
        *   **重要度:** Minor
        *   **内容:** SVドメインのVisit「AE FOLLOW-UP」(VISITNUM=101) において、「Planned Study Day of Visit」(SV.VISITDY) が欠損している。予定外Visitであるため計画日がないのは許容される可能性があるが、記録としては不完全。
        *   **根拠:** タイミング情報の欠損。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 101
            *   [Visit Name(SV.VISIT)] = 'AE FOLLOW-UP'
            *   [Planned Study Day of Visit(SV.VISITDY)] = null

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 EXCL27b (基準値を超える臨床検査値) への抵触の可能性。スクリーニング時(Day -16)のクレアチニン値(1.8 mg/dL)が基準値上限(1.6 mg/dL)を超過していた。プロトコルでは臨床的に有意でないと判断されれば組み入れ可能とされているが、その判断と文書化が行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** スクリーニング時の検査結果とプロトコル除外基準の照合。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 EXCL31b [v] (エストロゲン補充療法は登録前3ヶ月間用量安定であること) への抵触の可能性。併用薬 PREMARIN が治験開始日(Day 1)から投与開始されており、3ヶ月安定投与の条件を満たしていない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31v]
        *   **根拠:** 併用薬の投与開始日とプロトコル除外基準の照合。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験薬の投与量変更時期がプロトコル規定と異なる可能性。High Dose群はプロトコル Figure LZZT.1 では Week 8 で 54mg から 81mg へ増量するように示唆されているが、EXドメインでは Day 15 (Week 2 終了後) に増量されている。プロトコル本文での詳細な投与計画との照合が必要。
        *   **プロトコル該当箇所:** Section 3.1 (Figure LZZT.1), Section 3.6.2
        *   **根拠:** 投与記録(EX)とプロトコル図の比較。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 1, 2
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Dose per Administration(EX.EXDOSE)] = 54, 81
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-06', '2013-10-20'
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 1, 15
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** Day 27に予定外の検査Visitが実施された可能性。プロトコル上のWeek 4 (Day 28) Visit Window (+/- 3 days) 内ではあるが、DSドメインに 'FINAL LAB VISIT' と記録されているため、予定外Visitの可能性が高い。逸脱とは断定できないが、記録の不整合がある。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Window), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** DSドメインの記録とSVドメインの記録の比較、プロトコルスケジュールとの照合。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-01' (Day 27)
            *   SVドメインにDay 27のVisit記録なし。
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** NPI-Xの評価スケジュールがプロトコル規定（2週間隔）と一致していない可能性がある。Visit 4 (Day 14) と Visit 5 (Day 35) の間隔が約3週間空いている。電話インタビューでの評価記録があれば遵守している可能性もある。
        *   **プロトコル該当箇所:** Section 3.9.1.1
        *   **根拠:** QSドメインの評価日とプロトコル規定の評価間隔の比較。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT' (および関連するNPI-X項目)
            *   [Study Day of Finding(QS.QSDY)] = 1, 14, 35, 50
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験手順開始前にインフォームド・コンセントが取得されていなかった可能性。同意取得日(DM.RFICDTC)が欠損しているため確認できない。
        *   **プロトコル該当箇所:** Section 5.1
        *   **根拠:** 必須情報の欠損とGCP要件。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2013-10-06'
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験中止の判断と記録が不適切である可能性。中止理由(ADVERSE EVENT)と関連するAE記録、治験薬投与中止記録との間に不整合が見られる(D-1, D-2)。適切な中止判断が行われ、正確に記録されているか確認が必要。
        *   **プロトコル該当箇所:** Section 3.10.1
        *   **根拠:** DS, AE, EXドメイン間のデータ不整合。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-24' (Day 50)
            *   関連するAE, EXデータ (D-1, D-2参照)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-3)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として「BRAIN DEATH」が報告され、同日に「RECOVERED/RESOLVED」と記録されていますが、これは医学的に考えられません。患者様の実際の状態と転帰（死亡された場合は死亡日を含む）について、詳細な情報と記録の修正をお願いいたします。患者様の最終的な状態確認は最優先事項です。
        *   **クエリ文面（英語）:** The AE 'BRAIN DEATH' was reported with an outcome of 'RECOVERED/RESOLVED' on the same day (2013-11-18), which is medically impossible. Please provide details on the patient's actual condition and final outcome (including date of death if applicable) and correct the record accordingly. Confirmation of the patient's final status is critical.
        *   **判断理由:** 報告されたAEの転帰が医学的にありえず、患者の実際の状態が不明であるため、安全性確保とデータの正確性確認のために緊急の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18'
            *   関連する医学的知見: Brain Deathの定義と予後。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-1, P-7)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14に発現した有害事象「MYOCARDIAL INFARCTION」について、重症度が「MILD」と評価されていますが、評価根拠をお知らせください。また、治験薬との関連性が「NONE」と評価されていますが、再評価をお願いします。処置として「DRUG WITHDRAWN」とありますが、治験薬の実際の最終投与日と中止理由、およびDay 50の治験中止イベント「ADVERSE EVENT」との関連を含め、中止に至った経緯を詳細にご確認ください。
        *   **クエリ文面（英語）:** Regarding the AE 'MYOCARDIAL INFARCTION' on Day 14: Please provide the basis for the 'MILD' severity assessment. Please also reassess the causality ('NONE' reported). The action taken is 'DRUG WITHDRAWN', but this conflicts with the last dose date (Day 44) and discontinuation event (Day 50). Please clarify the exact date and reason for drug withdrawal and the circumstances leading to study discontinuation.
        *   **判断理由:** AE評価の妥当性、治験薬との関連性、および治験中止理由と時期に関する情報が不整合であり、安全性評価とデータの信頼性確保のために確認が必要。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1), EX, DS (DSSEQ=1) ドメインの関連レコード。
            *   関連する医学的知見: 心筋梗塞の重症度、コリン作動薬の心血管リスク。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14に発現した有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」（重症度 SEVERE）について、詳細な臨床経過（症状、診断根拠、治療など）と、治験薬との関連性評価（「NONE」と報告）の根拠をお知らせください。
        *   **クエリ文面（英語）:** Regarding the AE 'LATE EFFECTS OF CEREBRAL INFARCTION' (Severity 'SEVERE') reported on Day 14, please provide detailed clinical information (symptoms, diagnostic basis, treatment) and the rationale for assessing causality as 'NONE'.
        *   **判断理由:** 重症AEの詳細情報と治験薬との関連性評価の根拠が不明なため、安全性評価のために確認が必要。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=4)
            *   関連する医学的知見: 脳血管イベントのリスクと評価。
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14に発現した有害事象「VENTRICULAR SEPTAL DEFECT」について、診断根拠（心エコー所見など）と発症経緯（先天性の顕在化、心筋梗塞の合併症など）の詳細をお知らせください。
        *   **クエリ文面（英語）:** Regarding the AE 'VENTRICULAR SEPTAL DEFECT' reported on Day 14, please provide the diagnostic basis (e.g., echocardiogram findings) and details on the onset circumstances (e.g., manifestation of congenital defect, complication of MI).
        *   **判断理由:** 成人におけるVSD発症は稀であり、診断の妥当性と背景を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=2)
            *   関連する医学的知見: 心室中隔欠損症の病態。
    *   **クエリNo.:** Q-5 (関連指摘No.: M-6, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時(2013-09-20)のクレアチニンが「1.8 mg/dL」と基準値上限(1.6 mg/dL)を超えており、除外基準 EXCL27b に抵触する可能性があります。プロトコル上、臨床的に有意でないと判断されれば組み入れ可能ですが、その判断根拠と、判断が文書化されているかご確認ください。
        *   **クエリ文面（英語）:** The screening Creatinine level on 2013-09-20 was '1.8 mg/dL' (ULN 1.6), potentially meeting exclusion criterion EXCL27b. The protocol allows inclusion if deemed not clinically significant. Please confirm the rationale for this assessment and if it was documented.
        *   **判断理由:** 除外基準抵触の可能性があり、適格性評価の妥当性を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='CREAT', LBDY=-16)
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-6 (関連指摘No.: M-10, P-2, D-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「PREMARIN」が治験開始日(2013-10-06)から投与されていますが、プロトコル除外基準 EXCL31b [v] では「登録前3ヶ月間用量が安定していること」が求められています。この条件を満たさない薬剤が投与された理由と、本薬剤の適応症についてご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication 'PREMARIN' was started on 2013-10-06 (Day 1). Protocol exclusion criterion EXCL31b[v] requires estrogen supplements to be stable for 3 months prior to enrollment. Please clarify the reason for administering this medication despite not meeting the stability criteria and provide the indication for its use.
        *   **判断理由:** 除外基準抵触の可能性があり、プロトコル遵守状況と併用薬情報の完全性を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='PREMARIN', CMSTDTC='2013-10-06')
            *   関連するプロトコル箇所: Section 3.4.2.2 [31v]
    *   **クエリNo.:** Q-7 (関連指摘No.: D-9, P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日時の記録がありません。治験手順開始（2013-10-06）前に、適切なインフォームド・コンセントが取得されていたことを確認し、同意取得日時をお知らせください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please confirm that informed consent was obtained prior to the start of study procedures (2013-10-06) and provide the date/time of consent.
        *   **判断理由:** 同意取得の確認はGCP遵守の基本であり、記録の欠損は重大な問題であるため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: Section 5.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5, D-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** DSの中止理由(ADVERSE EVENT)とAE「RASH」/「PRURITUS」がRELRECで関連付けられているが、AEの重症度(MILD)と転帰(RECOVERED/RESOLVED)から、これらが主要な中止理由とは考えにくい。他のAE（特にMI）との関連も含め、中止理由を内部で再検討・記録する。クエリQ-2の回答により明確化される可能性がある。
        *   **判断理由:** データ間の不整合はあるが、AE自体は軽微で回復しており、他の重大なAEが存在するため、直接的なクエリは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: DS (DSSEQ=1), AE (AESEQ=5, 6, 7, 8), RELREC
    *   **確認事項No.:** I-2 (関連指摘No.: M-7)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 14のBUN高値は一過性であり、クレアチニンも正常上限に戻っているため、現時点での緊急性は低い。ただし、腎機能低下のリスクは念頭に置き、関連するクエリQ-5の回答を待つ。
        *   **判断理由:** 一過性の変動であり、臨床的に安定しているように見えるため。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='BUN', LBDY=14, 27)
    *   **確認事項No.:** I-3 (関連指摘No.: M-8)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 14, 27の低アルブミン血症。臨床的意義は現時点では不明確。他のデータとの明確な関連も乏しいため、内部確認・記録に留める。
        *   **判断理由:** 臨床的意義が不明確で、他のデータとの関連が薄いため。
        *   **判断根拠:**
            *   関連するデータ: LB (LBTESTCD='ALB', LBDY=14, 27)
    *   **確認事項No.:** I-4 (関連指摘No.: M-9)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 14の血圧・脈拍低下および起立性低血圧の所見。治験薬の薬理作用として考えられ、その後回復傾向もあるため緊急クエリは不要と判断。ただし、重要な安全性情報として内部で記録し、同様の事象がないか他の症例でも注意する。
        *   **判断理由:** 治験薬との関連が疑われる安全性所見だが、回復傾向が見られるため。
        *   **判断根拠:**
            *   関連するデータ: VS (VSTESTCD='SYSBP', 'DIABP', 'PULSE', VSDY=1, 14, 35, 50)
            *   関連する医学的知見: コリン作動薬の副作用。
    *   **確認事項No.:** I-5 (関連指摘No.: M-11)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 50のNPI-X評価で「HALLUCINATIONS」が新たに出現。一過性の可能性もあり、他の精神症状スコアは改善しているため、内部確認・記録に留める。
        *   **判断理由:** 他の精神症状は改善傾向であり、単発の報告であるため。
        *   **判断根拠:**
            *   関連するデータ: QS (QSTESTCD='NPITM02F', 'NPITM02V', 'NPTOT', QSDY=50)
    *   **確認事項No.:** I-6 (関連指摘No.: M-12)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/Statistician
        *   **疑義事項/確認内容:** 有効性評価指標間の結果に一貫性がない。評価期間が短いため解釈は困難。内部での議論・記録に留める。
        *   **判断理由:** 評価期間が短く、明確な結論が出せないため。
        *   **判断根拠:**
            *   関連するデータ: QS (QSTESTCD='ACTOT', 'CIBIC', 'NPTOT', QSDY=1, 50)
    *   **確認事項No.:** I-7 (関連指摘No.: D-4, P-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** Day 27に予定外の検査Visitが実施された可能性。Visit Window内ではあるが、DS記録との整合性を内部で確認・記録する。
        *   **判断理由:** プロトコル逸脱とは断定できず、評価への影響も小さいため。
        *   **判断根拠:**
            *   関連するデータ: DS (DSSEQ=2), SV, LB (LBDY=27)
            *   関連するプロトコル箇所: Section 3.1
    *   **確認事項No.:** I-8 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 併用薬「HYDROCORTISONE, TOPICAL」のIndicationが欠損している。AEとの関連から適応症は明らかであり、クエリは不要と判断。内部で記録修正を検討する。
        *   **判断理由:** 適応症が明らかであり、評価への影響が小さいため。
        *   **判断根拠:**
            *   関連するデータ: CM (CMTRT='HYDROCORTISONE, TOPICAL'), AE (AETERM='RASH', 'PRURITUS')
    *   **確認事項No.:** I-9 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM/Statistician
        *   **疑義事項/確認内容:** NPI-X Total Score (NPTOT) の計算根拠を確認する。SAP等の文書を参照し、データが計算ロジックに従っているか検証する。
        *   **判断理由:** 有効性評価の正確性に関わるが、内部文書で確認可能な事項であるため。
        *   **判断根拠:**
            *   関連するデータ: QS (QSTESTCD='NPTOT' および関連項目)
    *   **確認事項No.:** I-10 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「RASH」/「PRURITUS」の重複報告疑いについて、データの意図を確認する。収集日が異なるため、経過観察のための再評価記録の可能性が高い。必要に応じてデータ修正を検討。
        *   **判断理由:** データ構造の問題であり、評価への影響は小さいと考えられるため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=5, 6, 7, 8)
    *   **確認事項No.:** I-11 (関連指摘No.: D-10)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE FOLLOW-UP Visit (VISITNUM=101) の Planned Study Day (VISITDY) が欠損している。予定外Visitのため許容される可能性が高い。内部確認に留める。
        *   **判断理由:** 予定外Visitの性質上、計画日がないことは一般的であり、評価への影響は小さいため。
        *   **判断根拠:**
            *   関連するデータ: SV (VISITNUM=101)
    *   **確認事項No.:** I-12 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **確認担当者:** CRA/Medical Monitor
        *   **疑義事項/確認内容:** 治験薬の投与量変更時期がプロトコル規定と異なる可能性がある。プロトコル本文（Figure LZZT.1だけでなく）でHigh Dose群の投与計画（54mgから81mgへの増量時期）を再確認し、EXドメインの記録（Day 15に増量）と比較する。逸脱が確認された場合は記録する。
        *   **判断理由:** プロトコル遵守の確認が必要だが、まずは内部でのプロトコル再確認が先決であるため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.1 (Figure LZZT.1), Section 3.6.2
    *   **確認事項No.:** I-13 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** NPI-Xの評価スケジュールがプロトコル規定（2週間隔）と一部ずれている。電話インタビューでの評価記録が存在するか確認する。逸脱であれば軽微な逸脱として記録する。
        *   **判断理由:** 評価間隔のずれが評価結果に与える影響は限定的と考えられるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (NPI-X関連)
            *   関連するプロトコル箇所: Section 3.9.1.1

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
64歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2008年7月23日発症）、肺気腫（SIGNIFICANT PRE-EXISTING CONDITION、MILD）、冠動脈疾患（SIGNIFICANT PRE-EXISTING CONDITION、MILD）、関節炎（SIGNIFICANT PRE-EXISTING CONDITION、MILD）が報告されている。また、肺膿瘍ドレナージ術（1997年）、腸ポリープ切除術（2009年）の既往がある。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65 (SCREENING 1)|LB検査実施。Alanine Aminotransferase (ALT) が 135 U/L (HIGH)、Aspartate Aminotransferase (AST) が 145 U/L (HIGH) と基準値上限の3倍を超える高値。|
|2013年02月21日|Day -9 (UNSCHEDULED 1.1)|LB検査実施。ALT (19 U/L)、AST (29 U/L) ともに正常化。Sodium が 133 mmol/L (LOW)。|
|2013年02月23日|Day -7 (SCREENING 1)|VS測定、MH収集、SC収集、QS(Modified Hachinski Ischemic Score, Mini-Mental State Examination)実施。|
|2013年02月28日|Day -2 (SCREENING 2)|VS測定。|
|2013年03月02日|Day 1 (BASELINE)|治験薬(Placebo)投与開始。VS測定、LB検査、QS(ADAS-Cog, DAD, NPI-X)実施。ADAS-Cog(11) Total Score = 14。NPI-X Total Score = 3。|
|2013年03月04日|Day 3 (N/A)|有害事象「DIARRHOEA」(MILD, POSSIBLE) 発現。|
|2013年03月05日|Day 4 (N/A)|有害事象「DIARRHOEA」回復。有害事象「INSOMNIA」(MILD, REMOTE) 発現。併用薬「KAOPECTATE」投与開始・終了。|
|2013年03月06日|Day 5 (N/A)|有害事象「INSOMNIA」回復。|
|2013年03月13日|Day 12 (AMBUL ECG PLACEMENT)|VS測定。|
|2013年03月14日|Day 13 (WEEK 2)|VS測定、LB検査、QS(NPI-X)実施。NPI-X Total Score = 6 (ベースラインより悪化)。|
|2013年03月28日|Day 27 (WEEK 4)|VS測定、LB検査、QS(NPI-X)実施。Ery. Mean Corpuscular Volume (MCV) が 101 fL (HIGH)。Sodium が 146 mmol/L (HIGH)。NPI-X Total Score = 4。|
|2013年03月30日|Day 29 (AMBUL ECG REMOVAL)|VS測定。|
|2013年04月13日|Day 43 (WEEK 6)|VS測定、LB検査、QS(NPI-X)実施。NPI-X Total Score = 3。|
|2013年04月27日|Day 57 (WEEK 8)|VS測定、LB検査、QS(ADAS-Cog, NPI-X)実施。ADAS-Cog(11) Total Score = 9 (ベースラインから改善)。NPI-X Total Score = 0 (ベースラインから改善)。|
|2013年05月11日|Day 71 (WEEK 10 (T))|QS(NPI-X)実施。NPI-X Total Score = 4。|
|2013年05月25日|Day 85 (WEEK 12)|VS測定、LB検査、QS(ADAS-Cog, NPI-X)実施。ADAS-Cog(11) Total Score = 9。NPI-X Total Score = 6。|
|2013年06月08日|Day 99 (WEEK 14 (T))|QS(NPI-X)実施。NPI-X Total Score = 6。|
|2013年06月22日|Day 113 (WEEK 16)|VS測定、LB検査、QS(ADAS-Cog, CIBIC+, DAD, NPI-X)実施。ADAS-Cog(11) Total Score = 7 (ベースラインから改善)。CIBIC+ = 4 (NO CHANGE)。DAD項目の一部に変化あり。NPI-X Total Score = 4。|
|2013年07月06日|Day 127 (WEEK 18 (T))|QS(NPI-X)実施。NPI-X Total Score = 4。|
|2013年07月20日|Day 141 (WEEK 20)|VS測定、LB検査、QS(NPI-X)実施。NPI-X Total Score = 4。|
|2013年08月03日|Day 155 (WEEK 22 (T))|QS(NPI-X)実施。NPI-X Total Score = 3。|
|2013年08月09日|Day 161 (WEEK 24)|VS測定、LB検査、QS(ADAS-Cog, CIBIC+, DAD, NPI-X)実施。治験薬(Placebo)投与終了。ADAS-Cog(11) Total Score = 9。CIBIC+ = 4 (NO CHANGE)。DAD項目の一部に変化あり。NPI-X Total Score = 2。|
|2013年08月31日|Day 183 (WEEK 26)|VS測定、LB検査、QS(NPI-X)実施。治験終了 (COMPLETED)。Aspartate Aminotransferase (AST) が 38 U/L (HIGH)。NPI-X Total Score = 2。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Minor
        *   **内容:** スクリーニング時(Day -65)にALTおよびASTの著明な上昇（基準値上限の3倍超）が認められたが、その後の再検査(Day -9)では正常化している。原因は不明だが、治験薬投与開始前には改善しており、治験期間中の安全性への直接的な影響は小さいと考えられる。
        *   **根拠:** 一過性の肝酵素上昇であり、治験開始時には正常範囲内であった。MHに肝疾患の記載はない。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45', [Result or Finding in Original Units(LB.LBORRES)] = '135', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45', [Result or Finding in Original Units(LB.LBORRES)] = '145', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-02-21T13:30', [Result or Finding in Original Units(LB.LBORRES)] = '19', [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-02-21T13:30', [Result or Finding in Original Units(LB.LBORRES)] = '29', [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 治験終了時(Day 183)に軽微なAST上昇(38 U/L、基準値上限36 U/L)が認められた。他の肝酵素は正常範囲内であり、臨床的な意義は低い可能性が高い。
        *   **根拠:** 軽微な上昇であり、単独の所見である。Placebo群である。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-08-31T11:00', [Result or Finding in Original Units(LB.LBORRES)] = '38', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Placebo群であるが、ADAS-Cogスコアに改善傾向が見られる一方、CIBIC+評価は「変化なし」であった。有効性評価指標間での乖離が見られるが、Placebo反応や評価者間の評価基準の差などが考えられ、現時点で医学的に大きな問題とは考えにくい。
        *   **根拠:** Placebo群における変動であり、各評価指標の特性の違いも考慮される。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 14
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 8, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 9
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 10, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 7
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 12, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 9
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 10, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 12, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** スクリーニング時に実施されたはずのMMSEのデータがQSドメインに記録されていない。プロトコルの適格性基準（Inclusion Criteria [3]: MMSE 10-23）を満たしているか確認できない。
        *   **根拠:** 適格性判断に必要なデータが欠損している。
        *   **関連データ:**
            *   QSドメイン全体
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 併用薬であるKAOPECTATEおよびNORVASCについて、Indication（CMINDC）が記録されていない。AEとの関連や服薬理由の明確化のためには情報が必要だが、安全性評価への直接的な影響は限定的。
        *   **根拠:** データ完全性の観点からの指摘。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'KAOPECTATE', [Sequence Number(CM.CMSEQ)] = 13
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC', [Sequence Number(CM.CMSEQ)] = 3, 6, 9, 12, 16, 19, 22, 25, 28, 31, 34, 37, 40
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 有害事象DIARRHOEAおよびINSOMNIAについて、Action Taken with Study Treatment（AEACN）が記録されていない。治験薬への影響評価に必要だが、Placebo群であり、事象も軽度で回復しているため影響は小さい。
        *   **根拠:** データ完全性の観点からの指摘。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA', [Sequence Number(AE.AESEQ)] = 1
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'INSOMNIA', [Sequence Number(AE.AESEQ)] = 2
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** Visit 1 (Planned Day -7) のLBデータ採取日 (LBDTC) が '2012-12-27' (Study Day -65) となっており、Visit 1の他のデータ (VS, QS, MH, SC) の収集日 ('2013-02-23', Study Day -7) と大きく乖離している。データ入力エラーまたはVisit定義と実際の運用に齟齬がある可能性があり、データの信頼性に影響を与える可能性がある。
        *   **根拠:** 同一Visit内のデータ収集日に大きな不整合がある。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 1, [Planned Study Day of Visit(SV.VISITDY)] = -7, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-02-23'
            *   [Visit Number(LB.VISITNUM)] = 1, [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45', [Study Day of Specimen Collection(LB.LBDY)] = -65
            *   [Visit Number(VS.VISITNUM)] = 1, [Date/Time of Measurements(VS.VSDTC)] = '2013-02-23', [Study Day of Vital Signs(VS.VSDY)] = -7
            *   [Visit Number(QS.VISITNUM)] = 1, [Date/Time of Finding(QS.QSDTC)] = '2013-02-23', [Study Day of Finding(QS.QSDY)] = -7
            *   [Visit Number(MH.VISITNUM)] = 1, [Date/Time of History Collection(MH.MHDTC)] = '2013-02-23', [Study Day of History Collection(MH.MHDY)] = -7
            *   [Visit Number(SC.VISITNUM)] = 1, [Date/Time of Collection(SC.SCDTC)] = '2013-02-23', [Study Day of Examination(SC.SCDY)] = -7

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[3] (MMSE score of 10 to 23) を満たしているか確認できない。MMSEスコアデータが欠損しているため。適格性の確認ができないことは、参加者の保護およびデータの信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [3]
        *   **根拠:** 適格性基準の確認に必要なデータが欠損している。
        *   **関連データ:**
            *   QSドメイン全体
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[6] (Investigator has obtained informed consent signed by the patient (and/or legal representative) and by the caregiver) を満たしているか確認できない。同意取得日 (DM.RFICDTC) が記録されていないため。GCP遵守の観点から重大な問題となる可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [6], Section 5.1 Informed Consent
        *   **根拠:** 同意取得の記録が欠損している。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b] (Evidence from ECG recording at screening of any listed condition) を満たしているか確認できない。スクリーニング時のECGデータが提供されていないため。不適格な患者が登録された場合、安全性リスクが高まる可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** 適格性基準の確認に必要なデータが欠損している。
        *   **関連データ:**
            *   ECGデータなし
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された有効性評価項目であるCIBIC+の評価がWeek 8およびWeek 12で実施されていない（データ欠損）。主要評価項目の一つであり、試験の有効性評価の信頼性に影響を与える。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルで規定された評価が欠損している。
        *   **関連データ:**
            *   QSドメイン (QSTESTCD='CIBIC', VISITNUM=8 or 12 のレコードが存在しない)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された有効性評価項目であるDADの評価がWeek 8およびWeek 12で実施されていない（データ欠損）。副次評価項目であり、試験の有効性評価の信頼性に影響を与える。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルで規定された評価が欠損している。
        *   **関連データ:**
            *   QSドメイン (QSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', VISITNUM=8 or 12 のレコードが存在しない)
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** Ambulatory ECGの実施時期がプロトコル記載 (Visit 2で装着、Visit 3で除去) と異なり、Visit 3.5 (Day 12) で装着、Visit 6 (Day 29) で除去されている。安全性評価のスケジュールからの逸脱であり、評価のタイミングが適切であったか確認が必要。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** 実際の実施時期がプロトコル規定と異なる。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 3.5, [Visit Name(SV.VISIT)] = 'AMBUL ECG PLACEMENT', [Planned Study Day of Visit(SV.VISITDY)] = 13, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-03-13'
            *   [Visit Number(SV.VISITNUM)] = 6, [Visit Name(SV.VISIT)] = 'AMBUL ECG REMOVAL', [Planned Study Day of Visit(SV.VISITDY)] = 30, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-03-30'
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたECG評価が、スクリーニング時および治験期間中（Visit 4, 5, 7, 8, 9, 10, 11, 12, 13）に実施された記録がない。安全性モニタリング計画からの逸脱であり、参加者の安全性監視に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルで規定された安全性評価が実施された記録がない。
        *   **関連データ:**
            *   ECGデータなし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-1, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時に実施されたMini-Mental State Examination (MMSE) のスコアをご提供ください。選択基準[3]（MMSEスコア 10-23）への適合性を確認するために必要です。
        *   **クエリ文面（英語）:** Please provide the Mini-Mental State Examination (MMSE) score obtained during screening (Visit 1). This is required to confirm eligibility per Inclusion Criterion [3] (MMSE score 10-23).
        *   **判断理由:** 患者の適格性を確認するために必須のデータが欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: QSドメインにMMSEデータなし
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [3]
    *   **クエリNo.:** Q-2 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日（Date/Time of Informed Consent）をご提供ください。GCP要件である同意取得の確認に必要です。
        *   **クエリ文面（英語）:** Please provide the Date/Time of Informed Consent. This is required to confirm appropriate consenting procedure per GCP requirements.
        *   **判断理由:** GCP遵守を確認するために必須のデータが欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
    *   **クエリNo.:** Q-3 (関連指摘No.: P-3, P-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時(Visit 1)および治験期間中(Visit 4, 5, 7, 8, 9, 10, 11, 12, 13)に実施されたECGの結果をご提供ください。除外基準[16b]への適合性確認およびプロトコルで規定された安全性モニタリングのために必要です。
        *   **クエリ文面（英語）:** Please provide ECG results from Screening (Visit 1) and during the study (Visits 4, 5, 7, 8, 9, 10, 11, 12, 13). This is required to confirm eligibility per Exclusion Criterion [16b] and for safety monitoring as per protocol.
        *   **判断理由:** 適格性確認および安全性モニタリングに必要なデータが欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: ECGデータなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [16b], Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1 Schedule of Events
    *   **クエリNo.:** Q-4 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 8 (Visit 8) および Week 12 (Visit 9) におけるCIBIC+評価が実施されたか、また実施された場合はその結果をご提供ください。主要評価項目の一つであり、評価の欠損は試験結果の信頼性に影響します。
        *   **クエリ文面（英語）:** Please confirm if CIBIC+ assessment was performed at Week 8 (Visit 8) and Week 12 (Visit 9). If performed, please provide the results. This is a primary endpoint and missing data impacts the reliability of efficacy evaluation.
        *   **判断理由:** 主要有効性評価項目のデータが欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSTESTCD='CIBIC', VISITNUM=8 or 12 のレコードが存在しない)
            *   関連するプロトコル箇所: Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
    *   **クエリNo.:** Q-5 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 8 (Visit 8) および Week 12 (Visit 9) におけるDAD評価が実施されたか、また実施された場合はその結果をご提供ください。副次評価項目であり、評価の欠損は試験結果の信頼性に影響します。
        *   **クエリ文面（英語）:** Please confirm if DAD assessment was performed at Week 8 (Visit 8) and Week 12 (Visit 9). If performed, please provide the results. This is a secondary endpoint and missing data impacts the reliability of efficacy evaluation.
        *   **判断理由:** 副次有効性評価項目のデータが欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', VISITNUM=8 or 12 のレコードが存在しない)
            *   関連するプロトコル箇所: Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
    *   **クエリNo.:** Q-6 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Ambulatory ECGの装着がVisit 3.5 (Day 12)、除去がVisit 6 (Day 29) と記録されていますが、プロトコルではVisit 2装着、Visit 3除去と規定されています。実施時期が異なった理由をご教示ください。
        *   **クエリ文面（英語）:** Ambulatory ECG placement is recorded at Visit 3.5 (Day 12) and removal at Visit 6 (Day 29), while the protocol specifies placement at Visit 2 and removal at Visit 3. Please clarify the reason for this discrepancy in timing.
        *   **判断理由:** プロトコルで規定された安全性評価のスケジュールからの逸脱の理由を確認するため。
        *   **判断根拠:**
            *   関連するデータ: SVドメイン (VISITNUM=3.5, 6)
            *   関連するプロトコル箇所: Section 3.1 Summary of Study Design, Protocol Attachment LZZT.1 Schedule of Events
    *   **クエリNo.:** Q-7 (関連指摘No.: M-1)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時(2012年12月27日)のアラニンアミノトランスフェラーゼが「135 U/L」、アスパラギン酸アミノトランスフェラーゼが「145 U/L」と高値でしたが、その後の再検査(2013年2月21日)では正常化しています。初回高値の原因について、追加情報があればご提供ください。
        *   **クエリ文面（英語）:** On 2012-12-27 (Screening), ALT was 135 U/L and AST was 145 U/L (High). Subsequent results on 2013-02-21 were normal. Please provide any available information regarding the cause of the initial elevated liver enzymes.
        *   **判断理由:** スクリーニング時の異常値の原因を可能な範囲で特定するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='ALT'/'AST', LBDTC='2012-12-27T12:45', '2013-02-21T13:30')
    *   **クエリNo.:** Q-8 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬として記録されている「KAOPECTATE」および「NORVASC」について、それぞれのIndication（適応症）をご提供ください。
        *   **クエリ文面（英語）:** Please provide the indication for the concomitant medications 'KAOPECTATE' (CMSEQ=13) and 'NORVASC' (CMSEQ=3, etc.).
        *   **判断理由:** データ完全性の向上およびAEや既往歴との関連を確認するため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='KAOPECTATE'/'NORVASC', CMINDC='')
    *   **クエリNo.:** Q-9 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「DIARRHOEA」(AESEQ=1) および「INSOMNIA」(AESEQ=2) について、治験薬に対して取られた処置（Action Taken with Study Treatment）をご提供ください。
        *   **クエリ文面（英語）:** Please provide the Action Taken with Study Treatment for AE 'DIARRHOEA' (AESEQ=1) and 'INSOMNIA' (AESEQ=2).
        *   **判断理由:** データ完全性の向上および有害事象への対応を確認するため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='DIARRHOEA'/'INSOMNIA', AEACN='')

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2, M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 最終Visitでの軽微なAST上昇、および有効性評価指標（ADAS-Cog改善 vs CIBIC+不変）間の乖離が認められる。Placebo群であり、臨床的意義は低いと判断されるため、現時点での追加アクションは不要。傾向監視を行う。
        *   **判断理由:** Placebo群における軽微な変動であり、安全性や有効性評価の信頼性への影響は限定的と判断したため。
        *   **判断根拠:**
            *   関連するデータ: LB(AST, Day 183), QS(ACTOT, CIBIC+)
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** Visit 1において、LBデータの収集日(Day -65)と他のドメインのデータ収集日(Day -7)に大きなずれがある。Study Dayの計算自体は整合しているが、Visit 1の定義と実際のデータ収集タイミングに不整合がある可能性。試験全体で同様の事象がないか、データマネジメント計画等を確認する必要がある。
        *   **判断理由:** データの信頼性に関わる可能性のあるシステム的な問題かもしれないため、内部での確認が必要。医療機関への問い合わせでは解決しない可能性。
        *   **判断根拠:**
            *   関連するデータ: SV, LB, VS, QS, MH, SC ドメインのVisit 1データ
    *   **確認事項No.:** I-3 (関連指摘No.: P-2, P-9, P-10, P-11, P-16)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** スクリーニング関連データ（CNS imaging, Folate, Syphilis, HbA1c）およびPKサンプルデータが欠損している。これらは適格性確認や探索的目的のデータであり、主要/副次評価項目の評価に必須ではないため、収集対象外であったか、あるいは欠損していても試験評価への影響は限定的と判断。アクション不要。
        *   **判断理由:** 試験の主要な目的（有効性・安全性評価）への影響が小さい、または収集対象外のデータである可能性が高いため。
        *   **判断根拠:**
            *   関連するデータ: 該当データ欠損
            *   関連するプロトコル箇所: Section 3.4.2, 3.9.2
    *   **確認事項No.:** I-4 (関連指摘No.: P-5, P-6, P-7)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** MHにあるCoronary Artery Disease, Emphysema, Intestinal Polypectomy (2009) が除外基準の "Serious" disorderに該当するか。いずれも MILD または過去の手術であり、プロトコルの例示からも除外基準に抵触しない可能性が高いと判断。アクション不要。
        *   **判断理由:** 既往歴の重症度から判断し、適格性に問題ないと判断したため。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17], [18], [20]
    *   **確認事項No.:** I-5 (関連指摘No.: P-8)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時の肝酵素高値（除外基準[27b]関連）。再検査で正常化しており、最終的に適格と判断されたと推測される。プロトコルに逸脱時の明確な判断基準記載はないが、結果的に問題はなかったと判断。アクション不要。
        *   **判断理由:** 再検査で基準を満たしており、治験参加が許可されたと考えられるため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (ALT, AST at Day -65 and Day -9)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    81歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、計画された治療群および実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2009年診断）、高血圧、甲状腺機能低下症、骨粗鬆症、関節炎、難聴（軽度）、耳鳴（軽度）、静脈瘤（軽度）、食道裂孔ヘルニア（軽度）、足首浮腫（軽度）、局所感染（軽度）、背部痛（軽度）、副鼻腔炎（軽度）、眼鏡着用、虫垂切除術（1946年）、結核（1952年）、直腸出血（1981年）、痔核（1981年）、複数の骨折（手首、足、膝、肘、肋骨、いずれも1986年）、膀胱炎（2002年）、咳（2002年）、皮膚付属器腫（2006年）、失禁（2006年）、基底細胞癌（2007年）、摂食障害（2009年）、黄斑変性症（2012年）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年08月25日|Day -13 (Visit 1)|Screening開始。MMSE 23点。Hachinski Ischemic Score 1点。赤血球数(RBC) 3.8 TI/L (基準値3.9-5.5、LOW)。|
|2012年09月02日|Day -5 (N/A)|有害事象「ERYTHEMA」(紅斑) (MILD) 発現。有害事象「PRURITUS」(掻痒) (MILD) 発現。併用薬「HYDROCORTISONE, TOPICAL」開始。|
|2012年09月04日|Day -3 (N/A)|併用薬「HYDROCORTISONE, TOPICAL」終了。|
|2012年09月07日|Day 1 (Visit 3, BASELINE)|治験薬「XANOMELINE」54mg パッチ (Low Dose) 投与開始。有害事象「ERYTHEMA」「PRURITUS」回復/解決。有害事象「MICTURITION URGENCY」(尿意切迫) (MILD) 発現。ADAS-Cog(11) Total Score 7点。NPI-X Total Score 2点。|
|2012年09月13日|Day 7 (N/A)|有害事象「ARTHRALGIA」(関節痛) (MODERATE) 発現。有害事象「CELLULITIS」(蜂窩織炎) (MODERATE) 発現。|
|2012年09月16日|Day 10 (N/A)|治験薬「XANOMELINE」投与終了。|
|2012年09月17日|Day 11 (Visit 4, WEEK 2)|治験中止 (Disposition: ADVERSE EVENT, 関連AE: ARTHRALGIA)。MCV 101 fL (基準値80-100、HIGH)。赤血球数(RBC) 3.7 TI/L (基準値3.9-5.5、LOW)。尿比重(SPGRAV) 1.004 (基準値1.006-1.03、LOW)。ADAS-Cog(11) Total Score 5点 (ベースラインから2点改善)。CIBIC+ 4点 (NO CHANGE)。NPI-X Total Score 1点 (ベースラインから1点改善)。AE「ERYTHEMA」「PRURITUS」の記録あり(開始日Day -5, 終了日Day 1, 転帰RECOVERED/RESOLVED)。AE「LOCALISED INFECTION」(Day -61発現)、「MICTURITION URGENCY」(Day 1発現)、「ARTHRALGIA」(Day 7発現)、「CELLULITIS」(Day 7発現) 継続中。|
|2012年09月29日|Day 23 (Visit 101)|AE FOLLOW-UP Visit実施。|
|2013年02月22日|Day 169 (Visit 201)|RETRIEVAL Visit実施。ADAS-Cog(11) Total Score 9点 (ベースラインから2点悪化)。CIBIC+ 5点 (MINIMAL WORSENING)。NPI-X Total Score 45点 (ベースラインから43点悪化)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「ERYTHEMA」(紅斑)および「PRURITUS」(掻痒)について、Day -5に発現しDay 1に回復した記録(AESEQ=1, 2)と、Visit 4 (Day 11)で収集された記録(AESEQ=4, 5)が存在する。後者の記録も開始日Day -5、終了日Day 1、転帰RECOVERED/RESOLVEDとなっており、記録の重複または矛盾の可能性がある。ただし、治験薬投与期間外の事象であり、臨床的な影響は小さいと考えられる。
        *   **根拠:** 同一と思われる事象が異なる収集日で記録されており、データの正確性に疑問がある。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Sequence Number(AE.AESEQ)] = 1, 4
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS', [Sequence Number(AE.AESEQ)] = 2, 5
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-02' (for AESEQ 1, 2, 4, 5)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07' (for AESEQ 1, 2, 4, 5)
            *   [Date/Time of Collection(AE.AEDTC)] = '2012-09-05' (for AESEQ 1, 2), '2012-09-17' (for AESEQ 4, 5)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED' (for AESEQ 1, 2, 4, 5)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「MICTURITION URGENCY」(尿意切迫、AESEQ=6)が治験薬開始日(Day 1)に発現しているが、治験薬との関連性(AEREL)が「NONE」と評価されている。治験薬Xanomelineはムスカリン作動薬であり、薬理作用として尿意切迫を引き起こす可能性があるため、関連性評価の妥当性に疑問がある。SUPPAEでは治療関連有害事象フラグ(AETRTEM)が「Y」となっている点も考慮すると、再評価が必要である。
        *   **根拠:** 治験薬の薬理作用（ムスカリン作動作用）と有害事象の発現時期（投与開始日）から、関連性の可能性が否定できない。安全性評価の正確性に影響する可能性がある。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY'
            *   [Sequence Number(AE.AESEQ)] = 6
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-07' (Day 1)
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Qualifier Variable Name(SUPPAE.QNAM)] = 'AETRTEM', [Data Value(SUPPAE.QVAL)] = 'Y' (for AESEQ=6)
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 治験中止理由が「ADVERSE EVENT」(DS.DSTERM)であり、RELRECデータから「ARTHRALGIA」(関節痛、AESEQ=7)が関連付けられている。しかし、同時期に他の有害事象「CELLULITIS」(蜂窩織炎、AESEQ=8、Moderate)、「MICTURITION URGENCY」(AESEQ=6、Mild)や、検査値異常「RBC低値」「MCV高値」も認められている。中止決定に至った総合的な医学的判断、および中止の主たる理由となった「ARTHRALGIA」の詳細（部位、発現状況、処置、重症度評価の根拠など）が不明確である。
        *   **根拠:** 中止理由の背景にある医学的判断が不明確であり、症例の安全性評価および解釈に影響を与える可能性がある。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 11
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16' (linking DSSEQ=1 and AESEQ=7)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Sequence Number(AE.AESEQ)] = 7, [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 7
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS', [Sequence Number(AE.AESEQ)] = 8, [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 7
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY', [Sequence Number(AE.AESEQ)] = 6, [Severity/Intensity(AE.AESEV)] = 'MILD', [Study Day of Start of Adverse Event(AE.AESTDY)] = 1
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.7, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 11
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 11
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11)の検査で赤血球数(RBC)の低値 (3.7 TI/L, 基準値3.9-5.5) およびMCVの高値 (101 fL, 基準値80-100) が認められた。ベースライン(Day -13)でもRBCは低値(3.8 TI/L)であり、MCVは正常範囲上限(97 fL)であった。貧血、特に大球性貧血の可能性が示唆される。81歳女性であることを考慮すると臨床的に重要であり、原因検索やフォローアップが必要となる可能性がある。
        *   **根拠:** 基準値から逸脱した検査値異常であり、潜在的な健康リスクを示唆する可能性がある。安全性評価に影響する。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.8 (Day -13), 3.7 (Day 11), [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (both)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 97 (Day -13), 101 (Day 11), [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL' (Day -13), 'HIGH' (Day 11)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 7.4472 (Day -13), 7.57132 (Day 11) (いずれも正常範囲内)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HCT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.37 (Day -13), 0.37 (Day 11) (いずれも正常範囲内)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 388.8206 (Day -13, 正常範囲内)
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** MHドメインに「LOCALIZED INFECTION」(Significant Pre-existing Condition)の記録があり、AEドメインにも「LOCALISED INFECTION」(AESEQ=3)が開始日Day -61で記録されている。これらは同一の事象である可能性が高いが、記録が分かれている。AEの転帰は「NOT RECOVERED/NOT RESOLVED」であり、治験期間中も継続していたと解釈できる。
        *   **根拠:** 同一事象が異なるドメインに記録されている可能性があり、データの一貫性に影響する。ただし臨床的な解釈への影響は小さい。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1224', [Dictionary-Derived Term(MH.MHDECOD)] = 'LOCALISED INFECTION', [Category for Medical History(MH.MHCAT)] = 'SIGNIFICANT PRE-EXISTING CONDITION'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LOCALISED INFECTION', [Sequence Number(AE.AESEQ)] = 3, [Study Day of Start of Adverse Event(AE.AESTDY)] = -61, [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「ERYTHEMA」(AESEQ=1, 4)および「PRURITUS」(AESEQ=2, 5)について、同一開始日(Day -5)・終了日(Day 1)の記録が、異なる収集日(Visit 2, Visit 4)で2回ずつ存在する。記録の重複またはVisit 4での再確認時の入力ミスの可能性がある。
        *   **根拠:** 同一イベントの重複記録はデータ品質の問題であり、AE発生件数の集計等に影響する可能性があるが、本件は治験薬投与前の事象であり、転帰も明確なため、医学的評価への影響は小さい。
        *   **関連データ:** (M-1に同じ)
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** ADAS-Cog(11) Total Score (QS.ACTOT) の値が、元データである各項目(QS.ACITMxx)の合計値と一致しない。Baseline (合計13 vs ACTOT 7), Week 2 (合計9 vs ACTOT 5), Retrieval (合計14 vs ACTOT 9) のいずれの時点でも不整合が見られる。
        *   **根拠:** 主要評価項目の一つであるADAS-CogのTotal Scoreの計算に誤りがある可能性があり、有効性評価の信頼性に直接影響する。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 7 (Baseline), 5 (Week 2), 9 (Retrieval)
            *   [Question Short Name(QS.QSTESTCD)] = 'ACITM01'-'ACITM08', 'ACITM11'-'ACITM14' の各値
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** DADスコアの一部の項目(DAITM25-29, 31, 37-39)において、ベースライン、Week 2、Retrievalの間でスコア(0, 1, 96=NA)の変動が見られる。特にベースラインで0(No)だったものがWeek 2で1(Yes)になり、Retrievalで再び0(No)に戻るなどの変動があり、評価の一貫性や記録の正確性に疑問が生じる可能性がある。また、一部項目でNA(Not Applicable)が使用されているが、その理由がデータからは不明確である。
        *   **根拠:** 副次評価項目であるDADスコアのデータ品質に関する問題。評価の信頼性に影響する可能性があるが、主要評価項目ではないためMinorとした。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM01'-'DAITM40' の各時点での [Character Result/Finding in Std Format(QS.QSSTRESC)] の値
    *   **指摘No.:** D-4
        *   **重要度:** Critical
        *   **内容:** 同意取得日時 (DM.RFICDTC) が欠損している。
        *   **根拠:** 同意取得は治験参加の前提であり、治験関連手技開始前に適切に行われたかを確認できない。GCP遵守および参加者の権利保護の観点から極めて重要。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2012-08-25' (Visit 1)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **内容:** スクリーニング時に実施されるべき評価の一部について、データが提供されておらず実施状況を確認できない。具体的には、Inclusion Criteria [5] のCNS imaging、Exclusion Criteria [16b] のECG、Exclusion Criteria [29b] のSyphilis screeningの結果が不明である。また、Exclusion Criteria [25] のBasal Cell Carcinomaの既往、[26] のHearing loss/Eyeglasses wearerが適格基準を満たしていたかの確認も必要である。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5], Section 3.4.2.2 Exclusion Criteria [16b], [25], [26], [29b], Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 適格性の確認は参加者の安全性確保と試験データの妥当性担保の基本であり、必要な情報が不足している。
        *   **関連データ:**
            *   MH, LB, VSドメインに関連データなし (ECG, Imaging, Syphilis)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0951', [Dictionary-Derived Term(MH.MHDECOD)] = 'BASAL CELL CARCINOMA', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2007'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEARING LOSS', [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1384', [Dictionary-Derived Term(MH.MHDECOD)] = 'CORRECTIVE LENS USER'
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **内容:** 同意取得日時 (DM.RFICDTC) の記録が欠損しており、最初の治験関連手技（Screening Visit 1: 2012-08-25）の前にインフォームド・コンセントが適切に取得されたかを確認できない。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** GCPの基本原則であり、参加者の権利保護に関わる重大な逸脱の可能性がある。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2012-08-25' (Visit 1)
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **内容:** 治験薬投与手順（Hydrocortisone cream塗布、貼付時間、ローテーション）および中止時の漸減投与手順（プロトコル3.10.1）が遵守されていたか、提供されたデータからは確認できない。
        *   **プロトコル該当箇所:** Section 3.6.2 TTS Administration Procedures, Section 3.10.1 Discontinuations
        *   **根拠:** 投与手順の逸脱は有効性・安全性評価に影響する可能性があるが、データからは確認不能であり、SDV等での確認が必要。現時点ではMinorとする。
        *   **関連データ:** EXドメインには手順に関する情報なし。
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **内容:** プロトコルではスクリーニング時(Visit 1)および治験期間中の複数VisitでECG測定が規定されているが、本症例ではECGデータが提供されていない。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.4.2 Cardiovascular Safety Measures, Section 3.9.4 Safety Monitoring
        *   **根拠:** ECGは重要な安全性評価項目であり、データ欠損は安全性モニタリングの妥当性に影響を与える。
        *   **関連データ:** ECGドメインデータなし。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-2, D-4)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日時の記録が欠損しています。最初の治験関連手技（Screening Visit 1、2012年8月25日）より前にインフォームド・コンセントが適切に取得されたことを確認するため、同意取得日時をお知らせください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please provide the date/time of informed consent to confirm it was obtained before the first study procedure (Screening Visit 1 on 2012-08-25).
        *   **判断理由:** GCP遵守および参加者の権利保護の確認に必須の情報が欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損), [Start Date/Time of Visit(SV.SVSTDTC)] = '2012-08-25' (Visit 1)
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「MICTURITION URGENCY」(尿意切迫、AESEQ=6)が治験薬投与開始日(Day 1)に発現していますが、治験薬との関連性が「NONE」と評価されています。治験薬Xanomelineの薬理作用を考慮すると関連性が疑われます。関連性評価について再検討をお願いします。
        *   **クエリ文面（英語）:** Regarding AE 'MICTURITION URGENCY' (AESEQ=6) starting on Day 1, the causality (AEREL) is 'NONE'. Considering the pharmacology of Xanomeline, a relationship is suspected. Please reassess the causality.
        *   **判断理由:** 治験薬の安全性プロファイル評価の正確性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY', [Sequence Number(AE.AESEQ)] = 6, [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-07', [Causality(AE.AEREL)] = 'NONE'
            *   関連する医学的知見: Xanomelineはムスカリン作動薬であり、副作用として尿意切迫が起こりうる。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 治験中止理由が「ADVERSE EVENT」であり、「ARTHRALGIA」(関節痛、AESEQ=7)と関連付けられています。中止決定に至った総合的な医学的判断、および「ARTHRALGIA」の詳細（部位、発現状況、処置、重症度評価の根拠など）について、可能な範囲で情報を提供してください。
        *   **クエリ文面（英語）:** The reason for study discontinuation is 'ADVERSE EVENT', linked to 'ARTHRALGIA' (AESEQ=7). Please provide details on the overall medical judgment leading to discontinuation and specifics of the arthralgia (location, onset, treatment, basis for severity rating).
        *   **判断理由:** 症例の安全性評価および中止理由の正確な把握のため。
        *   **判断根拠:**
            *   関連するデータ: [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 11, [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Sequence Number(AE.AESEQ)] = 7, [Severity/Intensity(AE.AESEV)] = 'MODERATE'
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Week 2 (Day 11)の検査にて、赤血球数が「3.7 TI/L」(基準値3.9-5.5)、MCVが「101 fL」(基準値80-100)と記録されています。これらの検査値異常の臨床的意義について評価をお願いします。また、追跡検査が実施されていれば結果をお知らせください。
        *   **クエリ文面（英語）:** On Week 2 (Day 11), RBC was 3.7 TI/L (ref 3.9-5.5) and MCV was 101 fL (ref 80-100). Please assess the clinical significance of these findings. If follow-up tests were performed, please provide results.
        *   **判断理由:** 潜在的な健康リスク（貧血）の評価と適切なフォローアップ確認のため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.7, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 11. [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 11.
    *   **クエリNo.:** Q-5 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** ADAS-Cog(11) Total Score (ACTOT)について、記録されている値 (Baseline: 7, Week 2: 5, Retrieval: 9) が、各時点の個別項目スコアの合計値と一致しません。正しいTotal Scoreを確認し、必要であれば修正をお願いします。
        *   **クエリ文面（英語）:** Regarding ADAS-Cog(11) Total Score (ACTOT), the recorded values (Baseline: 7, Week 2: 5, Retrieval: 9) do not match the sum of individual item scores. Please confirm the correct Total Score and revise if necessary.
        *   **判断理由:** 主要評価項目のデータの正確性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'ACITM01'-'ACITM08', 'ACITM11'-'ACITM14' の各値
    *   **クエリNo.:** Q-6 (関連指摘No.: P-1, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の適格性評価について確認させてください。1) Inclusion Criteria [5] CNS imaging、Exclusion Criteria [16b] ECG、[29b] Syphilis screeningの結果をご提供ください。2) Exclusion Criteria [25] Basal Cell Carcinomaの既往、[26] Hearing loss/Eyeglasses wearerについて、適格と判断された根拠をお知らせください。3) プロトコルで規定されているECG測定が実施されなかった理由、またはデータが欠損している理由をお知らせください。
        *   **クエリ文面（英語）:** Regarding screening eligibility: 1) Please provide results for Inclusion [5] CNS imaging, Exclusion [16b] ECG, [29b] Syphilis screening. 2) Please provide rationale for eligibility considering Exclusion [25] Basal Cell Carcinoma history, [26] Hearing loss/Eyeglasses wearer. 3) Please provide reason why required ECGs were not performed or data is missing.
        *   **判断理由:** 参加者の適格性および安全性評価の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: MH, LB, VSドメインに関連データなし (ECG, Imaging, Syphilis)。MHドメインの関連既往歴。ECGデータ欠損。
            *   関連するプロトコル箇所: Section 3.4.2.1, 3.4.2.2, Protocol Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「ERYTHEMA」(AESEQ=1, 4)および「PRURITUS」(AESEQ=2, 5)の記録が重複している可能性がある。Visit 4での再確認時に過去の事象として記録された可能性が高い。データクリーニング時に確認し、必要に応じて修正を検討する。臨床的影響は小さいと判断されるため医療機関への問い合わせは不要。
        *   **判断理由:** データ品質の問題であり、内部での確認・修正で対応可能と判断したため。
        *   **判断根拠:**
            *   関連するデータ: (M-1に同じ)
    *   **確認事項No.:** I-2 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHの「LOCALIZED INFECTION」とAEの「LOCALISED INFECTION」(AESEQ=3)は同一事象の可能性が高い。記録の一貫性のため、内部でデータの整理・統合を検討する。
        *   **判断理由:** データの一貫性に関する問題であり、内部での対応が可能と判断したため。
        *   **判断根拠:**
            *   関連するデータ: (M-5に同じ)
    *   **確認事項No.:** I-3 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor / Statistician
        *   **疑義事項/確認内容:** DADスコアの一部の項目で時点間の変動が大きい。特にRetrieval Visitでのスコアは、同VisitでのNPI-Xの著明な悪化と合わせて解釈する必要がある。評価の一貫性や記録の正確性に留意し、データ解析時に考慮する。
        *   **判断理由:** 副次評価項目の解釈に関する留意事項であり、内部での記録・検討で対応可能と判断したため。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'DAITM01'-'DAITM40' の各時点での [Character Result/Finding in Std Format(QS.QSSTRESC)] の値, [Question Short Name(QS.QSTESTCD)] = 'NPTOT'
    *   **確認事項No.:** I-4 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 治験薬投与手順（Hydrocortisone cream塗布、貼付時間、ローテーション）および中止時の漸減投与手順の遵守状況がデータから確認できない。次回のSDV等で原資料を確認し、逸脱があれば記録する。
        *   **判断理由:** データからは確認できないプロトコル遵守事項であり、SDVでの確認が適切と判断したため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.6.2, 3.10.1
    *   **確認事項No.:** I-5 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor / DM
        *   **疑義事項/確認内容:** プロトコルで規定されているECGデータが本症例で欠損している。安全性評価（特に心血管系）の重要なデータが不足している点を記録し、他の安全性データ（VS, AE）と合わせて慎重に評価する。データ欠損の理由が判明しない場合、安全性評価の限界として記録する。
        *   **判断理由:** 重要な安全性データの欠損であり、評価への影響を内部で記録・検討する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: ECGデータなし
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1, Section 3.9.3.4.2, 3.9.4