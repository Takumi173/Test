# 01-701-1181のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    79歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、計画された治療群はXanomeline High Doseであったが、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2008年診断、PRIMARY DIAGNOSIS）が報告されている。その他、多数の既往歴（骨折、肺炎、気管支炎、手術歴など）を有する。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年11月26日|Day -9 (SCREENING 1)|Albumin値が基準値下限未満 (3.2 g/dL, Ref: 3.5-4.6)。立位での血圧低下傾向あり (Supine 137/59 mmHg, Standing 1min 113/56 mmHg)。MMSEスコア 10、Hachinski Ischemic Scaleスコア 2。|
|2013年12月03日|Day -2 (SCREENING 2)|立位での血圧低下傾向あり (Supine 142/61 mmHg, Standing 1min 128/63 mmHg)。|
|2013年12月05日|Day 1 (BASELINE)|治験薬 Xanomeline 54mg Patch (Low Dose) 投与開始。Baseline ADAS-Cog(11)スコア 32。Baseline NPI-X Totalスコア 10。|
|2013年12月09日|Day 5 (N/A)|有害事象「AGITATION」(中等度) 発現、同日回復。治験薬 Xanomeline 54mg Patch 投与終了。Motrin (Ibuprofen) 200mg 服用 (適応不明)。|
|2013年12月12日|Day 8 (WEEK 2)|治験中止 (理由: 有害事象)。最終検査来院。Albumin値は正常化 (3.9 g/dL)。立位での血圧変動あり (Standing 3min 146/71 mmHg)。ADAS-Cog(11)スコア 39 (Baselineから悪化)。NPI-X Totalスコア 20 (Baselineから悪化)。CIBIC+スコア 4 (変化なし)。|
|2013年12月20日|Day 16 (AE FOLLOW-UP)|AEフォローアップのための来院。|
|2014年05月23日|Day 170 (RETRIEVAL)|最終来院 (Retrieval Visit)。立位での顕著な血圧低下 (Supine 137/52 mmHg, Standing 1min 113/47 mmHg) および頻脈 (Supine 88 bpm, Standing 1min 100 bpm) を認める。ADAS-Cog(11)スコア 38 (Baselineから悪化)。NPI-X Totalスコア 26 (Baseline, Week 2からさらに悪化、幻覚・焦燥/攻撃性・易刺激性などが悪化/新規発現)。CIBIC+スコア 5 (軽度悪化)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 5に発現した有害事象「AGITATION」について、治験薬との関連性(Causality)が「NONE」と評価されているが、発現時期（治験薬開始後5日目）を考慮すると、治験薬（コリン作動薬）との関連を除外することは困難である可能性がある。Xanomelineは精神症状（興奮、錯乱など）を引き起こす可能性が知られているため、関連性の再評価が必要かもしれない。このAEが治験中止の理由となっているため、評価の妥当性は重要である。
        *   **根拠:** Xanomelineの薬理作用（ムスカリンM1アゴニスト）と一般的な副作用プロファイル。AE発現と治験薬投与期間の近接性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'AGITATION'
            *   [Severity/Intensity(AE.AESEV)] = 'MODERATE'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-12-09'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 5
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-12-09'
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 5
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 8
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-12-05'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-12-09'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Retrieval Visit (Day 170) において、顕著な起立性低血圧と頻脈が認められる。治験薬投与終了から長期間経過しているが、患者の循環器系の状態として医学的に注意が必要な所見である。アルツハイマー病の進行、他の併存疾患、併用薬、脱水などの影響も考えられるが、データからは原因特定は困難。
        *   **根拠:** バイタルサイン測定値。起立性低血圧は転倒リスクや心血管イベントリスクと関連する可能性がある。
        *   **関連データ:**
            *   [Visit Name(VS.VISIT)] = 'RETRIEVAL'
            *   [Study Day of Vital Signs(VS.VSDY)] = 170
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 137
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 52
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 88
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 113
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 47
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 100
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** NPI-XスコアがBaselineからWeek 2、Retrieval Visitにかけて悪化傾向を示している。特に幻覚、焦燥/攻撃性、易刺激性などが悪化または新規に出現している。治験薬中止後も悪化が続いていることから、疾患自体の進行が主因と考えられるが、短期間の治験薬投与の影響が完全に否定できるかは不明。患者の精神状態の変化として注目すべきである。
        *   **根拠:** QSドメインのNPI-Xスコアの経時変化。アルツハイマー病の自然経過。
        *   **関連データ:**
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'BASELINE', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 10
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'WEEK 2', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 20
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 26
            *   (各サブ項目のスコア変動も参照)
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Day 5にMotrin (Ibuprofen) 200mgが投与されているが、その適応（Indication）が記録されていない。同日にAE「AGITATION」が発現・回復しており、関連性の有無（例：鎮静目的、あるいはAEとは無関係の疼痛など）が不明である。
        *   **根拠:** データ欠損。AEとの時間的近接性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'MOTRIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-12-09'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 5
            *   [Indication(CM.CMINDC)] = '' (欠損)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'AGITATION'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-12-09'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** DMドメインにおいて、計画された治療群コード(Planned Arm Code)が「Xan_Hi」(Xanomeline High Dose)であるのに対し、実際の治療群コード(Actual Arm Code)が「Xan_Lo」(Xanomeline Low Dose)となっている。EXドメインの投与記録はLow Dose (54mg)であり、ACTARMCDと一致しているため、実際に投与されたのはLow Doseと考えられるが、計画との不一致の原因（ランダム化エラー、データ入力エラー等）を確認する必要がある。データの正確性と信頼性に影響する。
        *   **根拠:** DMドメイン内のARMCDとACTARMCDの不一致。EXドメインとのクロスチェック。
        *   **関連データ:**
            *   [Planned Arm Code(DM.ARMCD)] = 'Xan_Hi'
            *   [Description of Planned Arm(DM.ARM)] = 'Xanomeline High Dose'
            *   [Actual Arm Code(DM.ACTARMCD)] = 'Xan_Lo'
            *   [Description of Actual Arm(DM.ACTARM)] = 'Xanomeline Low Dose'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Dose per Administration(EX.EXDOSE)] = 54
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 有害事象「AGITATION」の発現・回復日(Study Day of Start of Adverse Event, Study Day of End of Adverse Event)がDay 5であるのに対し、Dispositionドメインで中止理由として記録されている「ADVERSE EVENT」の発生日(Study Day of Start of Disposition Event)がDay 8 (Week 2 Visit日)となっている。RELRECデータで両イベントは関連付けられているが、日付のずれについて、中止決定のプロセスを含めて確認が必要。
        *   **根拠:** AEドメインとDSドメイン間の日付不整合。RELRECデータ。
        *   **関連データ:**
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 5
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 5
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 8
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1181-E16' (AE.AESEQ=1 と DS.DSSEQ=1 を関連付け)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、Motrin (Ibuprofen) の適応(Indication)が記録されていない。また、他の多くの併用薬について、標準化された薬剤名(Standardized Medication Name)が「UNCODED」となっており、WHODrugコーディングが未完了または失敗している可能性がある。データ品質の問題。
        *   **根拠:** CMドメインのデータ欠損および未コードデータ。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'MOTRIN', [Indication(CM.CMINDC)] = ''
            *   複数のCMレコードで [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** LBドメインに毒性グレード(Toxicity Grade)を示す変数（例: LBTOXGR）が含まれていない。SUPPLBにはLBTMSHI (Result/ULN ratio) が記録されているが、CTCAE等に基づくGrade評価が行われたかは不明。プロトコルでの規定を確認する必要がある。
        *   **根拠:** LBドメインの変数構成。安全性評価の標準的な方法との比較。
        *   **関連データ:**
            *   LBドメイン全体
            *   SUPPLBドメイン (QNAM='LBTMSHI')

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Inclusion Criteria [5] で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施記録がJSONデータに含まれていない。適格性確認に必要な評価が実施されたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5]
        *   **根拠:** JSONデータに該当する記録がない。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** DMドメインの計画治療群(Planned Arm Code)と実際の治療群(Actual Arm Code)が異なっている（High Dose計画に対しLow Dose実施）。これはランダム化の誤りや割付手順の逸脱の可能性を示唆するが、データ入力ミスの可能性もある。EXデータはLow Dose投与を示しており、ACTARMCDと一致している。
        *   **プロトコル該当箇所:** Section 3.5 (Patient Assignment), Section 3.1 (Summary of Study Design - 3 arm)
        *   **根拠:** DMドメイン内のARMCDとACTARMCDの不一致。
        *   **関連データ:**
            *   [Planned Arm Code(DM.ARMCD)] = 'Xan_Hi'
            *   [Actual Arm Code(DM.ACTARMCD)] = 'Xan_Lo'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Dose per Administration(EX.EXDOSE)] = 54
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [27b] では、特定の臨床検査値が基準範囲を超える場合を除外基準としている。Screening時 (Day -9) のAlbumin値 (3.2 g/dL) が基準範囲 (3.5-4.6 g/dL) を下回っていた。これが除外基準に該当しなかったか、あるいは逸脱として扱われたか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LBデータのScreening時Albumin値。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB'
            *   [Visit Name(LB.VISIT)] = 'SCREENING 1'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '3.2'
            *   [Original Units(LB.LBORRESU)] = 'g/dL'
            *   [Reference Range Lower Limit in Orig Unit(LB.LBORNRLO)] = '3.5'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '4.6'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [29b] で要求されている「Positive syphilis screening with confirmatory testing」の実施記録がJSONデータに含まれていない。適格性確認に必要な評価が実施されたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [29b]
        *   **根拠:** JSONデータに該当する記録がない。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Section 3.9.1.1 では、主要評価項目のADAS-Cogおよび副次評価項目のDADはVisits 3, 8, 10, 12で実施すると規定されているが、本症例ではWeek 2 (Visit 4, Day 8) にも実施されている。中止に伴う評価の可能性があるが、プロトコル規定からの逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.1.1
        *   **根拠:** QSデータの評価時期とプロトコル規定の比較。
        *   **関連データ:**
            *   [Category of Question(QS.QSCAT)] = 'ALZHEIMER''S DISEASE ASSESSMENT SCALE', [Visit Name(QS.VISIT)] = 'WEEK 2'
            *   [Category of Question(QS.QSCAT)] = 'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', [Visit Name(QS.VISIT)] = 'WEEK 2'
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されているECG評価 (Visits 4, 5, 7, 8, 9, 10, 11, 12, 13)、Ambulatory ECG評価 (Visit 2)、およびPK採血 (Visits 3, 4, 5, 7, 9, 11) の記録がJSONデータに含まれていない。これらの安全性およびPK評価が実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2, Section 3.9.2, Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** JSONデータにEC, PC, PPドメインが含まれていない。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 4 (Week 2) はDay 8に実施されたが、Planned Study Day of VisitはDay 14である。プロトコル Section 3.1 ではVisit 4のVisit Windowを±3日 (Day 11-17) と規定しており、Day 8の実施はこのWindowから逸脱している。中止に関連する可能性はあるが、逸脱として記録・評価が必要。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Window規定), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** SVデータのVisit実施日とTVデータのPlanned Day、プロトコル規定のVisit Windowの比較。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 4
            *   [Visit Name(SV.VISIT)] = 'WEEK 2'
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-12-12' (Day 8)
            *   [Visit Number(TV.VISITNUM)] = 4
            *   [Planned Study Day of Visit(TV.VISITDY)] = 14
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日(Date/Time of Informed Consent)の記録がDMドメインにない (DM.RFICDTCが欠損)。治験手順開始前に適切に同意が取得されたか確認できない。GCP遵守の観点から重要。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** DMドメインのRFICDTC欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「AGITATION」について、治験薬との関連性(Causality)が「NONE」と評価されていますが、発現時期（治験薬開始5日目）や薬剤の特性を考慮すると、関連性が否定しきれない可能性も考えられます。関連性評価の根拠について、詳細な医学的判断をご教示ください。
        *   **クエリ文面（英語）:** Regarding the AE 'AGITATION', Causality is assessed as 'NONE'. Considering the timing (Day 5 after starting study drug) and drug characteristics, a relationship cannot be fully excluded. Please provide detailed medical reasoning for the causality assessment.
        *   **判断理由:** 有害事象の関連性評価は安全性評価の根幹であり、治験中止理由ともなっているため、評価の妥当性を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='AGITATION', AE.AEREL='NONE', AE.AESTDY=5, EX.EXSTDY=1, EX.EXENDY=5
            *   関連するプロトコル箇所: Section 3.9.3.2 (Adverse Events)
            *   関連する医学的知見: コリン作動薬の副作用プロファイル
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1, P-2)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** Demographicsドメインにおいて、計画された治療群(Description of Planned Arm)が「Xanomeline High Dose」と記録されていますが、実際の治療群(Description of Actual Arm)は「Xanomeline Low Dose」と記録されています。Exposureドメインの投与記録もLow Dose (54mg) と一致しています。計画治療群の記録が誤りである可能性が高いと考えられますが、ご確認の上、必要であれば修正をお願いします。
        *   **クエリ文面（英語）:** In the DM domain, the Planned Arm is 'Xanomeline High Dose', but the Actual Arm is 'Xanomeline Low Dose'. EX data shows Low Dose (54mg) was administered, consistent with Actual Arm. Please confirm if the Planned Arm record is incorrect and correct if necessary.
        *   **判断理由:** データの正確性を確保し、ランダム化割付と実際の投与内容の整合性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: DM.ARM='Xanomeline High Dose', DM.ACTARM='Xanomeline Low Dose', EX.EXDOSE=54
            *   関連するプロトコル箇所: Section 3.5 (Patient Assignment)
    *   **クエリNo.:** Q-3 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「AGITATION」はStudy Day 5に発現・回復していますが、Dispositionの記録では中止理由となった「ADVERSE EVENT」の発生日がStudy Day 8と記録されています。中止に至る判断プロセスと、Disposition記録の日付の妥当性についてご確認ください。
        *   **クエリ文面（英語）:** AE 'AGITATION' occurred and resolved on Study Day 5, but the Disposition record for 'ADVERSE EVENT' leading to discontinuation shows Study Day 8. Please confirm the decision process for discontinuation and the accuracy of the Disposition date.
        *   **判断理由:** 治験中止の経緯と記録の正確性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: AE.AESTDY=5, AE.AEENDY=5, DS.DSDECOD='ADVERSE EVENT', DS.DSSTDY=8, RELREC.RELID='01-701-1181-E16'
            *   関連するプロトコル箇所: Section 3.10.1 (Discontinuations)
    *   **クエリNo.:** Q-4 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル Inclusion Criteria [5] で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」について、実施記録が確認できません。本評価が実施されたか、またその結果（適格性判断を含む）についてご確認ください。
        *   **クエリ文面（英語）:** Protocol Inclusion Criterion [5] requires 'CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year'. No record found. Please confirm if this assessment was performed and provide results (including eligibility assessment).
        *   **判断理由:** 適格性基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: (該当データなし)
            *   関連するプロトコル箇所: Section 3.4.2.1 [5]
    *   **クエリNo.:** Q-5 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Screening 1 (Study Day -9) の検査結果で、Albuminが「3.2 g/dL」と基準値下限 (3.5 g/dL) を下回っています。プロトコル Exclusion Criteria [27b] に抵触しなかったか、臨床的な意義と適格性判断についてご確認ください。
        *   **クエリ文面（英語）:** At Screening 1 (Study Day -9), the Albumin level was '3.2 g/dL', below the lower limit of normal (3.5 g/dL). Please confirm the clinical significance, eligibility assessment, and if this met Exclusion Criterion [27b].
        *   **判断理由:** 適格性基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALB', LB.VISIT='SCREENING 1', LB.LBORRES='3.2', LB.LBORNRLO='3.5', LB.LBNRIND='LOW'
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル Exclusion Criteria [29b] で要求されている「Positive syphilis screening with confirmatory testing」について、実施記録が確認できません。本評価が実施されたか、またその結果（適格性判断を含む）についてご確認ください。
        *   **クエリ文面（英語）:** Protocol Exclusion Criterion [29b] requires 'Positive syphilis screening with confirmatory testing'. No record found. Please confirm if this assessment was performed and provide results (including eligibility assessment).
        *   **判断理由:** 適格性基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: (該当データなし)
            *   関連するプロトコル箇所: Section 3.4.2.2 [29b]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではADAS-CogおよびDADの評価はVisits 3, 8, 10, 12で規定されていますが、本症例ではVisit 4 (Week 2) でも評価が記録されています。この評価が実施された理由（例：中止に伴う評価）についてご確認ください。
        *   **クエリ文面（英語）:** Protocol specifies ADAS-Cog and DAD assessments at Visits 3, 8, 10, 12. However, data exists for Visit 4 (Week 2). Please confirm the reason for this assessment (e.g., due to discontinuation).
        *   **判断理由:** プロトコル遵守状況と評価データの妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: QS.QSCAT='ALZHEIMER''S DISEASE ASSESSMENT SCALE'/'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', QS.VISIT='WEEK 2'
            *   関連するプロトコル箇所: Section 3.9.1.1
    *   **クエリNo.:** Q-8 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているECG評価、Ambulatory ECG評価、およびPK採血の記録が提供されていません。これらの評価・採血が実施されたかご確認ください。実施されていた場合、結果をご提供ください。
        *   **クエリ文面（英語）:** Records for protocol-specified ECG, Ambulatory ECG, and PK sampling are missing. Please confirm if these were performed. If performed, please provide the results/data.
        *   **判断理由:** プロトコル遵守状況と、安全性・PK評価に必要なデータの有無を確認するため。
        *   **判断根拠:**
            *   関連するデータ: (該当データなし)
            *   関連するプロトコル箇所: Section 3.9.3.4.2, Section 3.9.2, Attachment LZZT.1
    *   **クエリNo.:** Q-9 (関連指摘No.: P-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 4 (Week 2) はStudy Day 8に実施されましたが、計画日(Planned Study Day of Visit)はDay 14であり、プロトコル規定のVisit Window (Day 11-17) から逸脱しています。実施日がDay 8で正しいか、また逸脱理由についてご確認ください。
        *   **クエリ文面（英語）:** Visit 4 (Week 2) was conducted on Study Day 8, but the planned day was Day 14. This deviates from the protocol visit window (Day 11-17). Please confirm if Day 8 is correct and provide the reason for the deviation.
        *   **判断理由:** プロトコル遵守状況とデータ信頼性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=4, SV.SVSTDTC='2013-12-12', TV.VISITNUM=4, TV.VISITDY=14
            *   関連するプロトコル箇所: Section 3.1, Attachment LZZT.1
    *   **クエリNo.:** Q-10 (関連指摘No.: P-8)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日(Date/Time of Informed Consent)の記録が確認できません。同意取得日をご教示ください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please provide the date when informed consent was obtained.
        *   **判断理由:** GCP遵守と参加者の権利保護を確認するため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC='' (欠損)
            *   関連するプロトコル箇所: Section 5.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-4, D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインのMotrinについてIndicationが欠損している。他の薬剤についてもCMDECODが未コード。データマネジメントプロセスにおいて、Indicationの必須性やコーディングルールを確認し、必要に応じてデータクリーニング計画を見直す。参加者の安全性や評価への直接的な影響は小さいと判断。
        *   **判断理由:** データ品質に関する事項であり、医療機関への問い合わせは不要と判断。内部プロセス確認が必要。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='MOTRIN', CM.CMINDC='', 複数のCMレコードでCM.CMDECOD='UNCODED'
            *   関連するプロトコル箇所: なし (データマネジメント計画に関連)
    *   **確認事項No.:** I-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Retrieval Visit (Day 170) で顕著な起立性低血圧と頻脈が観察された。治験薬投与終了後であるが、患者の安全性に関する重要な所見として内部で記録・共有する。他の症例でも同様の所見がないか注意する。
        *   **判断理由:** 患者の安全性に関する重要な観察事項であり、医療機関への問い合わせではなく内部での認識と記録が必要と判断。
        *   **判断根拠:**
            *   関連するデータ: VSドメインのRetrieval Visitデータ
            *   関連するプロトコル箇所: Section 3.9.3 (Safety)
    *   **確認事項No.:** I-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** NPI-Xスコアが悪化傾向にある。治験薬中止後も悪化しており、疾患進行が主因と考えられるが、患者の状態変化として内部で記録・共有する。有効性評価（副次）にも関連する。
        *   **判断理由:** 疾患進行と有効性評価に関連する重要な観察事項であり、内部での認識と記録が必要と判断。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのNPI-Xデータ
            *   関連するプロトコル箇所: Section 2.2 (Secondary Objectives), Section 4.3.1 (Efficacy Variables)
    *   **確認事項No.:** I-4 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインの多くの薬剤でWHODrugコーディングが未完了（CMDECOD="UNCODED"）。コーディングの進捗状況とプロセスを確認する。参加者の安全性や評価への直接的な影響は小さいが、データ標準化の観点から対応が必要。
        *   **判断理由:** データ品質と標準化に関する事項であり、内部での確認が必要。
        *   **判断根拠:**
            *   関連するデータ: 複数のCMレコードでCM.CMDECOD='UNCODED'
            *   関連するプロトコル箇所: なし (データマネジメント計画に関連)
    *   **確認事項No.:** I-5 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM / Medical Monitor
        *   **疑義事項/確認内容:** LBドメインにToxicity Grade (例: LBTOXGR) がない。プロトコルまたはSAP（統計解析計画書）でCTCAE Grade評価が規定されているか確認する。規定されている場合、データ欠損の可能性あり。規定されていない場合、現状のデータで問題ない。安全性評価の完全性に関わる可能性がある。
        *   **判断理由:** データ完全性と安全性評価方法に関する内部確認事項。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン全体, SUPPLBドメイン
            *   関連するプロトコル箇所: Section 3.9.3.3 (Clinical Laboratory Tests)
    *   **確認事項No.:** I-6 (関連指摘No.: P-9)
        *   **重要度:** Minor
        *   **確認担当者:** CRA / Medical Monitor
        *   **疑義事項/確認内容:** プロトコルでは中止時に用量漸減（25cm2パッチ除去、50cm2パッチ継続）が指示されているが、本症例で実施されたかはデータから不明（Day 5に投与終了）。漸減が行われなかった場合、軽微なプロトコル逸脱の可能性があるが、投与期間が短いため臨床的影響は小さいと判断。
        *   **判断理由:** データからは確認不能であり、臨床的影響も小さいと考えられるため内部確認に留める。
        *   **判断根拠:**
            *   関連するデータ: EX.EXENDTC='2013-12-09'
            *   関連するプロトコル箇所: Section 3.10.1

---

# 01-701-1363のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
81歳、女性、黒人またはアフリカ系アメリカ人（NOT HISPANIC OR LATINO）。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2005年10月20日発症）、不整脈（2011年）、貧血、頭痛、意識消失（2007年）、湿疹（2012年）、難聴、便秘、消化不良、関節痛（2012年）、浮動性めまい（2012年）、背部痛（2011年）、肩痛、近視が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年05月20日|Day -10 (SCREENING 1)|MMSEスコア 22点、Hachinski Ischemic Scaleスコア 1点。ヘモグロビン(HGB) 11.5 g/dL (基準範囲下限)。|
|2013年05月30日|Day 1 (BASELINE)|治験薬（Placebo）投与開始。ADAS-Cog(11) Total Score 15点。NPI-X Total Score 11点。臥位脈拍 51 bpm。|
|2013年06月12日|Day 14 (WEEK 2)|ヘモグロビン(HGB) 11.0 g/dL (低値)。立位3分後拡張期血圧 45 mmHg (臥位から低下)。|
|2013年06月14日|Day 16 (N/A)|有害事象「悪心」(軽度) 終了 (転帰: 回復/消失)。(終了日が開始日より前)|
|2013年06月15日|Day 17 (N/A)|有害事象「悪心」(軽度) 発現。|
|2013年06月25日|Day 27 (WEEK 4)|ヘモグロビン(HGB) 11.0 g/dL (低値)。赤血球数(RBC) 3.80 MILL/uL (低値)。|
|2013年06月27日|Day 29 (AMBUL ECG REMOVAL)|立位3分後収縮期血圧 97 mmHg (臥位から低下)。|
|2013年07月10日|Day 42 (WEEK 6)|ヘマトクリット(HCT) 33.0 % (低値)。ヘモグロビン(HGB) 10.8 g/dL (低値)。|
|2013年07月16日|Day 48 (N/A)|有害事象「適用部位そう痒感」(軽度) 発現 (転帰: 未回復/未消失)。|
|2013年07月24日|Day 56 (WEEK 8)|ヘモグロビン(HGB) 11.2 g/dL (低値)。白血球数(WBC) 3.60 THOU/uL (低値)。ADAS-Cog(11) Total Score 18点。CIBIC+ 5点 (Minimal worsening)。NPI-X Total Score 12点。|
|2013年08月21日|Day 84 (WEEK 12)|ヘマトクリット(HCT) 32.0 % (低値)。ヘモグロビン(HGB) 10.3 g/dL (低値、最低値)。赤血球数(RBC) 3.70 MILL/uL (低値)。|
|2013年09月18日|Day 112 (WEEK 16)|ヘモグロビン(HGB) 11.3 g/dL (低値)。ADAS-Cog(11) Total Score 22点。CIBIC+ 4点 (No Change)。NPI-X Total Score 10点。|
|2013年09月19日|Day 113 (N/A)|併用薬「HYDROCORTISONE」開始。|
|2013年10月01日|Day 125 (N/A)|併用薬「MOTRIN」開始・終了。|
|2013年10月13日|Day 137 (N/A)|有害事象「背部痛」(軽度) 発現。併用薬「ICY HOT」開始。|
|2013年10月14日|Day 138 (WEEK 20)|ヘモグロビン(HGB) 11.2 g/dL (低値)。立位3分後収縮期血圧 100 mmHg (臥位から低下)。NPI-X Total Score 10点。|
|2013年10月15日|Day 139 (N/A)|有害事象「背部痛」(軽度) 終了 (転帰: 回復/消失)。|
|2013年11月13日|Day 168 (WEEK 24)|ヘモグロビン(HGB) 10.9 g/dL (低値)。ADAS-Cog(11) Total Score 18点。CIBIC+ 5点 (Minimal worsening)。NPI-X Total Score 8点。|
|2013年11月27日|Day 182 (WEEK 26)|治験終了 (PROTOCOL COMPLETED)。ヘモグロビン(HGB) 11.4 g/dL (低値)。NPI-X Total Score 8点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 治療期間を通して持続的な貧血（ヘモグロビン低値）が認められる。ベースライン値（基準範囲下限）からさらに悪化しており（最低値 Day 84: 6.39 g/dL）、臨床的な注意が必要である。既往歴に貧血があるが、治療期間中の悪化要因について評価が必要。
        *   **根拠:** ヘモグロビン値が継続して基準範囲下限を下回っており、最低値はベースラインから有意に低下している。貧血は高齢者のQOLや認知機能にも影響しうるため、安全性評価上重要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 6.39218 (Day 84)
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 7.14
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (複数Visit)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ANEMIA'
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 立位での血圧低下傾向が複数回認められる。特にDay 29には臥位から立位3分後で収縮期血圧が19mmHg低下している。既往歴に浮動性めまいがあるため、起立性低血圧による症状発現のリスクに注意が必要。ただし、関連する有害事象の報告はない。
        *   **根拠:** 高齢者であり、アルツハイマー病患者は起立性低血圧のリスクが高い場合がある。既往歴との関連も考慮すると、潜在的な安全性リスクとして注意喚起が必要。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', 'DIABP'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', 'STANDING'
            *   [Study Day of Vital Signs(VS.VSDY)] = 29, 138 など
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'DIZZINESS'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** 有害事象「適用部位そう痒感」(Day 48発現)に対する治療薬と思われる「HYDROCORTISONE」の開始日(Day 113)が、AE発現日よりかなり遅い。治療開始の遅れがあったのか、あるいは記録誤りの可能性がある。
        *   **根拠:** 有害事象に対する適切な処置が行われたかを確認する必要がある。開始日の乖離が大きい。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 48
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 113

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「悪心」(AESEQ=1)の終了日(AEENDTC='2013-06-14', AEENDY=16)が開始日(AESTDTC='2013-06-15', AESTDY=17)より前になっている。日付の記録誤りの可能性が高く、イベントの期間評価に影響する。
        *   **根拠:** 開始日 <= 終了日の論理的整合性が取れていない。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'NAUSEA'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-06-15'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-06-14'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 17
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 16
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「背部痛」が2回記録されている(AESEQ=5, 6)。両方とも開始日Day 137、終了日Day 139、重症度MILDと同じ内容だが、収集日(AEDTC)が異なる(2013-10-14 vs 2013-11-13)。重複記録の可能性がある。
        *   **根拠:** 同一内容のイベントが異なる収集日で記録されている。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 5, 6
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BACK PAIN'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-13'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-10-15'
            *   [Date/Time of Collection(AE.AEDTC)] = '2013-10-14', '2013-11-13'
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 有害事象「適用部位そう痒感」(AESTDY=48)と、その治療薬と思われる併用薬「HYDROCORTISONE」(CMSTDY=113)の開始日に65日の乖離がある。医学的レビュー(M-3)とも関連。
        *   **根拠:** AEと関連する可能性のあるCMの開始日の整合性が低い。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 48
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 113
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 有害事象「背部痛」(AESTDY=137)に対する治療薬と思われる併用薬「MOTRIN」の開始日(CMSTDY=125)がAE発現日より12日前になっている。
        *   **根拠:** AEと関連する可能性のあるCMの開始日の整合性が低い。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BACK PAIN'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 137
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'MOTRIN'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 125
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** 臨床検査値で持続的なヘモグロビン低値が認められるが、対応する有害事象「貧血」が報告されていない。既往歴には貧血があるが、治療期間中の悪化はAEとして報告されるべき可能性がある。医学的レビュー(M-1)とも関連。
        *   **根拠:** 臨床的に意義のある検査値異常とAE報告の不一致。安全性評価の完全性に影響する可能性。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (複数Visit)
            *   AEドメインに 'ANEMIA' または関連する事象の報告なし。
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ANEMIA'
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 同意取得日(DM.RFICDTC)が欠損している。
        *   **根拠:** GCP上、同意取得日の記録は重要。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** 臨床検査値ビリルビン(LBTESTCD='BILI', LBSEQ=263)について、文字結果(LBSTRESC)は'<3.42'と記録されているが、数値結果(LBSTRESN)が欠損している。
        *   **根拠:** データ入力の不備または意図的な欠損か不明。ただし基準値内相当のため影響は小さい。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BILI'
            *   [Sequence Number(LB.LBSEQ)] = 263
            *   [Character Result/Finding in Std Format(LB.LBSTRESC)] = '<3.42'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = null

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 既往歴の「意識消失」(2007年)が除外基準[15]「過去5年以内の失神歴」に該当しないか確認が必要。ただし、記録上は5年以上前であり、プロトコルには抵触しない可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [15]
        *   **根拠:** 除外基準に類似する既往歴があるため、適格性を再確認。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2007'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b]で評価が必要な葉酸(Folate)の検査結果がLBデータに含まれていない。適格性評価がデータ上確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** プロトコルで規定された除外基準の評価に必要なデータが確認できない。ただし、適格性確認のみのデータは収集対象外の可能性あり。
        *   **関連データ:** LBドメインにFolateのデータなし。
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[30b]で評価が必要な糖化ヘモグロビン(A1C)の検査結果がLBデータに含まれていない。IDDM患者のみ必須であり、本症例がIDDMでないことの確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [30b]
        *   **根拠:** プロトコルで規定された除外基準の評価に必要なデータが確認できない。
        *   **関連データ:** LBドメインにHBA1Cのデータなし。
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 10.2 (UNSCHEDULED 10.2) が実施されているが、予定外Visitの理由が不明。
        *   **プロトコル該当箇所:** Section 3.1 Schedule of Events (予定外Visitに関する規定)
        *   **根拠:** 予定外の評価が実施された理由が不明確。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 10.2
            *   [Visit Name(SV.VISIT)] = 'UNSCHEDULED 10.2'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-5)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者様のヘモグロビン値が、ベースラインの11.5 g/dLから試験期間中に低下し、複数回の測定で基準値下限(11.5 g/dL、標準単位7.14 mmol/L)を下回っています（最低値 Day 84: 10.3 g/dL、標準単位6.39 mmol/L）。既往歴に貧血がありますが、この持続的なヘモグロビン低値について臨床的な評価と原因について確認をお願いします。貧血に対する追加検査や治療は行われましたでしょうか？
        *   **クエリ文面（英語）:** Patient's Hemoglobin level decreased during the study from baseline (11.5 g/dL) and was below the lower limit of normal (11.5 g/dL, SI: 7.14 mmol/L) at multiple visits (lowest: 10.3 g/dL, SI: 6.39 mmol/L on Day 84). History of anemia is reported. Please confirm the clinical assessment and cause of this persistent low Hemoglobin. Were additional tests or treatments for anemia performed?
        *   **判断理由:** ベースラインからの貧血の悪化が認められ、患者の安全性評価のために臨床的評価と対応の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)], [Reference Range Indicator(LB.LBNRIND)], [Reported Term for the Medical History(MH.MHTERM)] = 'ANEMIA'
            *   関連するプロトコル箇所: Section 3.9.3 Safety
            *   関連する医学的知見: 貧血の持続・悪化は臨床的に重要であり、原因検索や介入が必要となる場合がある。
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「悪心」(AESEQ=1)について、有害事象開始日(AESTDTC)が「2013-06-15」(Day 17)、有害事象終了日(AEENDTC)が「2013-06-14」(Day 16)と記録されており、終了日が開始日より前になっています。日付をご確認いただけますでしょうか。
        *   **クエリ文面（英語）:** Regarding AE 'NAUSEA' (AESEQ=1), the End Date (AEENDTC='2013-06-14', Day 16) is recorded before the Start Date (AESTDTC='2013-06-15', Day 17). Please verify the dates.
        *   **判断理由:** 有害事象の日付に明らかな矛盾があり、データの正確性確保のために確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Sequence Number(AE.AESEQ)] = 1, [Reported Term for the Adverse Event(AE.AETERM)] = 'NAUSEA', [Start Date/Time of Adverse Event(AE.AESTDTC)], [End Date/Time of Adverse Event(AE.AEENDTC)], [Study Day of Start of Adverse Event(AE.AESTDY)], [Study Day of End of Adverse Event(AE.AEENDY)]
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, D-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「適用部位そう痒感」(有害事象開始日(Study Day) 48)に対する併用薬「HYDROCORTISONE」について、投与開始日(Study Day)が113と記録されています。AE発現からかなり時間が経過していますが、この開始日で正しいでしょうか。もし治療開始が遅れた場合、その理由をお知らせください。
        *   **クエリ文面（英語）:** Regarding Concomitant Medication 'HYDROCORTISONE' (started Day 113) for AE 'APPLICATION SITE PRURITUS' (started Day 48), the start date is significantly later than the AE onset. Please confirm the medication start date. If treatment was delayed, please provide the reason.
        *   **判断理由:** AEに対する処置の開始タイミングが遅い可能性があり、記録の正確性または処置の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)], [Study Day of Start of Adverse Event(AE.AESTDY)], [Reported Name of Drug, Med, or Therapy(CM.CMTRT)], [Study Day of Start of Medication(CM.CMSTDY)]
            *   関連するプロトコル箇所: Section 3.9.3.2.1 Adverse Event Reporting Requirements
    *   **クエリNo.:** Q-4 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「背部痛」(有害事象開始日(Study Day) 137)に対する併用薬「MOTRIN」について、投与開始日(Study Day)が125と記録されており、AE発現より前になっています。開始日をご確認いただけますでしょうか。
        *   **クエリ文面（英語）:** Regarding Concomitant Medication 'MOTRIN' (started Day 125) for AE 'BACK PAIN' (started Day 137), the start date is recorded before the AE onset date. Please verify the medication start date.
        *   **判断理由:** AEとCMの日付の整合性が取れていないため、記録の正確性を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)], [Study Day of Start of Adverse Event(AE.AESTDY)], [Reported Name of Drug, Med, or Therapy(CM.CMTRT)], [Study Day of Start of Medication(CM.CMSTDY)]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 立位での血圧低下傾向と徐脈傾向が認められる。既往歴に浮動性めまいあり。関連するAE報告はないが、今後のレビューで症状発現に注意する。本症例はPlacebo群であり、治験薬との直接的な関連は低いと考えられる。
        *   **判断理由:** AE報告がなく、Placebo群であるため緊急性は低いが、潜在的リスクとして内部で認識しておくべき事項。
        *   **判断根拠:**
            *   関連するデータ: VSドメインデータ, [Reported Term for the Medical History(MH.MHTERM)] = 'DIZZINESS'
            *   関連する医学的知見: 高齢者、アルツハイマー病患者における起立性低血圧のリスク。
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「背部痛」が2回記録されている(AESEQ=5, 6)。収集日が異なるが内容は同一。重複記録の可能性があるため、データクリーニング時に確認する。臨床的な影響は小さいと判断。
        *   **判断理由:** データの一貫性に関する問題だが、安全性や有効性評価への影響は限定的。
        *   **判断根拠:**
            *   関連するデータ: AEドメインデータ (AESEQ=5, 6)
    *   **確認事項No.:** I-3 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** 同意取得日(DM.RFICDTC)が欠損している。治験開始前に同意取得済みと推測されるが、記録として不備。他症例でも同様の欠損がないか、データマネジメント計画等を確認する。
        *   **判断理由:** GCP上の記録不備だが、治験実施自体への影響は現時点では不明。システム的な問題かの確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **確認事項No.:** I-4 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 臨床検査値ビリルビン(LBSEQ=263)の数値結果(LBSTRESN)が欠損している。文字結果は'<3.42'であり基準値内相当のため、臨床的影響は小さいと判断。
        *   **判断理由:** データ欠損だが、臨床的な意義は低いと考えられる。
        *   **判断根拠:**
            *   関連するデータ: LBドメインデータ (LBSEQ=263)
    *   **確認事項No.:** I-5 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** 既往歴の「意識消失」(2007年)について、発症が5年以上前であるため、除外基準[15]「過去5年以内の失神歴」には抵触しないと判断。
        *   **判断理由:** プロトコル基準への適合性を確認し、問題ないと判断。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)], [Start Date/Time of Medical History Event(MH.MHSTDTC)]
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [15]
    *   **確認事項No.:** I-6 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 除外基準[28b]の評価に必要な葉酸(Folate)の検査結果がLBデータにない。前提知識に基づき、適格性確認のみに使用するデータは収集されないため、プロトコル逸脱ではないと判断。
        *   **判断理由:** 試験データ収集範囲に関する理解に基づき、問題ないと判断。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]
            *   前提知識: 適格性確認のみのデータは収集されない。
    *   **確認事項No.:** I-7 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 除外基準[30b]の評価に必要な糖化ヘモグロビン(A1C)の検査結果がLBデータにない。プロトコル上、IDDM患者のみ必須であり、本症例はIDDMではないと推測されるため、プロトコル逸脱ではないと判断。
        *   **判断理由:** プロトコル規定に基づき、検査不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [30b]
    *   **確認事項No.:** I-8 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 10.2 (UNSCHEDULED 10.2) が実施されているが、理由不明。他のデータとの明確な関連も見られないため、軽微な逸脱または記録漏れの可能性。安全性や有効性評価への影響は小さいと判断。
        *   **判断理由:** 予定外Visitだが、他のデータとの関連が薄く、影響が限定的と判断。
        *   **判断根拠:**
            *   関連するデータ: SVドメインデータ (VISITNUM=10.2)

---

# 01-701-1383のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
72歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、計画された治療群および実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2006年08月20日診断、PRIMARY DIAGNOSIS）、便秘（SIGNIFICANT PRE-EXISTING CONDITION, MILD）、耳鳴（SIGNIFICANT PRE-EXISTING CONDITION, MILD）、遠視（SIGNIFICANT PRE-EXISTING CONDITION, MILD）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年01月22日|Day -13 (SCREENING 1)|MMSE 22点、Hachinskiスコア 1点。身長 163.83 cm、体重 84.82 kg。|
|2013年02月04日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg/日 (TTS) 投与開始。ADAS-Cog(11) 11点、NPI-X Total 0点、DAD Total 97.4%。体重 84.82 kg。|
|2013年02月07日|Day 4 (N/A)|有害事象「APPLICATION SITE PAIN」(MILD, PROBABLE)、「APPLICATION SITE PRURITUS」(MILD, PROBABLE) 発現、同日回復。|
|2013年02月19日|Day 16 (WEEK 2)|NPI-X Total 1点 (Irritability/Lability)。体重 86.18 kg。|
|2013年02月20日|Day 17 (N/A)|治験薬 Xanomeline 81 mg/日 (TTS) に増量。|
|2013年03月12日|Day 37 (WEEK 4)|NPI-X Total 0点。体重 85.28 kg。|
|2013年03月19日|Day 44 (WEEK 6)|NPI-X Total 0点。体重 85.28 kg。|
|2013年03月23日|Day 48 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(MILD, POSSIBLE) 発現 (Day 51 回復)。有害事象「APPLICATION SITE PRURITUS」(MILD, POSSIBLE) 発現 (未回復)。|
|2013年04月02日|Day 58 (WEEK 8)|ADAS-Cog(11) 12点、CIBIC+ 4 (No Change)、DAD Total 100%、NPI-X Total 0点。体重 85.28 kg。カリウム 3.5 mEq/L (基準値下限付近)。|
|2013年04月12日|Day 68 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(MILD, POSSIBLE) 発現 (未回復)。有害事象「APPLICATION SITE IRRITATION」(MILD, POSSIBLE) 発現 (未回復)。|
|2013年04月16日|Day 72 (WEEK 10 (T))|NPI-X Total 0点。|
|2013年04月30日|Day 86 (WEEK 12)|NPI-X Total 0点。体重 84.37 kg。|
|2013年05月07日|Day 93 (N/A)|有害事象「APPLICATION SITE VESICLES」(MILD, POSSIBLE) 発現 (Day 110 回復)。|
|2013年05月14日|Day 100 (WEEK 14 (T))|併用薬 Hydrocortisone (Topical) 開始。NPI-X Total 0点。|
|2013年05月30日|Day 116 (WEEK 16)|ADAS-Cog(11) 13点、CIBIC+ 4 (No Change)、DAD Total 100%、NPI-X Total 0点。AE「APPLICATION SITE PRURITUS」が MODERATE に悪化。AE「APPLICATION SITE IRRITATION」が MODERATE に悪化。体重 84.82 kg。|
|2013年06月13日|Day 130 (WEEK 18 (T))|NPI-X Total 0点。|
|2013年06月24日|Day 141 (N/A)|有害事象「CHEST DISCOMFORT」(MILD, NONE)、「HEADACHE」(MILD, NONE) 発現、同日回復。|
|2013年06月25日|Day 142 (WEEK 20)|NPI-X Total 0点。体重 84.37 kg。|
|2013年07月09日|Day 156 (WEEK 22 (T))|NPI-X Total 0点。|
|2013年07月17日|Day 164 (N/A)|有害事象「BLOOD PRESSURE INCREASED」(MODERATE, NONE) 発現 (Day 173 回復)。|
|2013年07月19日|Day 166 (N/A)|併用薬 Cephalexin (500mg QID)、Promethazine HCL w/Codeine (2tsp Q6H) 開始。|
|2013年07月25日|Day 172 (N/A)|併用薬 Promethazine HCL w/Codeine 終了。|
|2013年07月30日|Day 177 (WEEK 24)|ADAS-Cog(11) 9点、CIBIC+ 5 (Minimal worsening)、DAD Total 100%、NPI-X Total 0点。臥位血圧 160/98 mmHg (高値)、立位1分後血圧 128/60 mmHg (起立性低血圧の可能性)。体重 83.01 kg。|
|2013年07月31日|Day 178 (N/A)|治験薬 Xanomeline 54 mg/日 (TTS) に減量。|
|2013年08月01日|Day 179 (N/A)|併用薬 Cephalexin 終了。|
|2013年08月06日|Day 184 (WEEK 26)|治験終了 (COMPLETED)。NPI-X Total 0点。体重 83.01 kg。臥位血圧 130/62 mmHg、立位1分後血圧 115/56 mmHg。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象「BLOOD PRESSURE INCREASED」の治験薬との関連性評価（NONE）および転帰評価（RECOVERED/RESOLVED on Day 173）の妥当性に疑問がある。Day 177に臥位で160/98 mmHgの高血圧が測定されており、AE回復後も高値が持続していた可能性がある。関連性評価の根拠が不明確。
        *   **根拠:** Xanomelineはコリン作動薬であり血圧への影響は個体差がある。併用薬（Cephalexin, Promethazine/Codeine）との関連も低いと考えられる。高血圧の既往歴はない。VSデータとの時間的な近接性から、関連性評価と転帰評価の再検討が必要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BLOOD PRESSURE INCREASED'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-07-17' (Day 164)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-07-26' (Day 173)
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 160, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 98, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 177のバイタルサイン測定において、臥位から立位1分後にかけて収縮期血圧が32mmHg、拡張期血圧が38mmHg低下しており、起立性低血圧の可能性が示唆される。関連する症状の有無や治験薬との関連性評価が必要。
        *   **根拠:** Xanomelineはコリン作動薬であり、起立性低血圧のリスクを高める可能性がある。高用量投与期間の後半で見られている。参加者の安全性に関わる可能性があるため確認が必要。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 160, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 98, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 128, [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 60, [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Week 24における有効性評価の結果に一貫性がない。ADAS-Cog(11)スコアはベースラインから改善しているが、CIBIC+スコアは悪化と評価されている。評価の信頼性に影響を与える可能性がある。
        *   **根拠:** 主要評価項目であるADAS-CogとCIBIC+の結果が乖離している。DADは改善・維持、NPI-Xは変動なしであり、全体的な有効性の解釈が困難。Day 178からの用量減量も影響している可能性がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 11
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 12, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 9
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 12, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 5
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Day 166から併用薬としてCephalexinとPromethazine/Codeineが使用されているが、対応する有害事象が報告されていない。未報告の有害事象（例：感染症、咳嗽など）が存在する可能性があり、安全性評価の完全性に影響する。
        *   **根拠:** 抗菌薬と鎮咳去痰作用のある薬剤が併用されていることから、何らかの感染症や呼吸器症状が存在した可能性が高い。これらの情報がないと、他のAEや治験薬の安全性プロファイルを正確に評価できない。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'CEPHALEXIN', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-07-19' (Day 166), [End Date/Time of Medication(CM.CMENDTC)] = '2013-08-01' (Day 179)
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PROMETHAZINE HCL W/CODEINE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-07-19' (Day 166), [End Date/Time of Medication(CM.CMENDTC)] = '2013-07-25' (Day 172)
            *   AEドメインに対応するイベント記録なし
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 複数の適用部位反応（紅斑、掻痒、刺激感、小水疱）が報告され、一部は中等度に悪化し未回復となっている。プロトコルで推奨されているHydrocortisoneクリームがDay 100から使用されているが、症状が持続・悪化している。
        *   **根拠:** 適用部位反応は経皮吸収型製剤でよく見られるが、持続・悪化する場合は患者のQOLやアドヒアランスに影響する可能性がある。現在の管理で十分か、継続的なモニタリングが必要。
        *   **関連データ:**
            *   AEドメインの適用部位反応関連イベント (AESEQ 1, 2, 3, 4, 5, 6, 7, 8, 9)
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-05-14' (Day 100)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** AE「BLOOD PRESSURE INCREASED」の転帰日（Day 173）と、VSで高値が記録された日（Day 177）に不整合がある。AEの転帰評価の正確性に疑問があり、医学的評価に影響する可能性がある。
        *   **根拠:** AEの回復日以降に、そのAEに関連する可能性のある異常値が記録されている。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BLOOD PRESSURE INCREASED'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-07-26' (Day 173)
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 160
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Date/Time of Measurements(VS.VSDTC)] = '2013-07-30' (Day 177), [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 98
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 併用薬CephalexinおよびPromethazine/Codeineの使用記録（CM）に対応する有害事象（AE）の記録がない。データの完全性に問題があり、安全性評価に影響する可能性がある。
        *   **根拠:** 薬剤の使用理由となるべき臨床イベントが記録されていない。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'CEPHALEXIN', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-07-19' (Day 166)
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PROMETHAZINE HCL W/CODEINE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-07-19' (Day 166)
            *   AEドメインに対応するイベント記録なし
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** Day 178からの治験薬用量減量について、その理由を示す記録（例：AEとの関連、医師の判断など）がデータセット内に見当たらない。投与情報の完全性に欠け、プロトコル遵守状況や有効性・安全性評価の解釈に影響する。
        *   **根拠:** 投与量変更という重要なイベントの背景情報が欠落している。
        *   **関連データ:**
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [End Date/Time of Treatment(EX.EXENDTC)] = '2013-07-30' (Day 177)
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 54, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-07-31' (Day 178)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** MHドメインのMHSTDTCの一部、AEドメインのMedDRAコード関連変数、CMドメインのCMDECOD/CMCLAS（UNCODED）およびCMENDTC/CMENDYの一部に欠損または未完了データが存在する。
        *   **根拠:** データ標準化や完全性の観点からの指摘。現時点での医学的評価や主要な評価への影響は限定的と考えられるが、最終的なデータ品質のためには修正が必要。
        *   **関連データ:**
            *   MHドメイン (MHSEQ 1, 2, 3) の MHSTDTC
            *   AEドメインの AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCD
            *   CMドメインの CMDECOD, CMCLAS ('UNCODED'), CMENDTC, CMENDY

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** Day 178から治験薬用量が81mgから54mgに減量されている。プロトコルでは早期中止時の漸減投与について記載があるが、本症例は完遂しており、この状況での減量の規定が見当たらない。理由不明な用量変更はプロトコルからの逸脱の可能性が極めて高く、有効性評価（特にWeek 24）の解釈に重大な影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1, 3.6.2, 3.10.1
        *   **根拠:** プロトコルに規定されていない状況での用量変更。
        *   **関連データ:**
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [End Date/Time of Treatment(EX.EXENDTC)] = '2013-07-30' (Day 177)
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 54, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-07-31' (Day 178)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'COMPLETED', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 184
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬Promethazine HCL w/Codeineの使用（Day 166-172）。Promethazine（抗ヒスタミン薬）とCodeine（麻薬性鎮痛薬）はプロトコル Section 3.4.2.2 [31 r, n] の禁止薬リストに含まれる薬剤に該当する。ただし、Section 3.8 ではCodeine含有鎮痛薬や抗ヒスタミン薬の一時的な使用について言及があり、許容される可能性もあるが、明確ではない。使用の妥当性について確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31 r, n], Section 3.8
        *   **根拠:** 禁止薬リストに含まれる薬剤の使用。ただし、例外規定の適用の可能性があるため確認が必要。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PROMETHAZINE HCL W/CODEINE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-07-19' (Day 166), [End Date/Time of Medication(CM.CMENDTC)] = '2013-07-25' (Day 172)
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 同意取得日（RFICDTC）が記録されていない。治験手順開始前に同意が適切に取得されたか確認できない。参加者の権利保護の観点から記録が必要。
        *   **プロトコル該当箇所:** Section 5.1
        *   **根拠:** GCPの基本要件である同意取得日の記録欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   [Date/Time of Collection(DM.DMDTC)] = '2013-01-22' (Day -13)
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の臨床検査値データが提供されていないため、除外基準（EXCL27, EXCL28, EXCL29, EXCL30）の遵守状況を確認できない。適格性評価の完全性に疑問が残る。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27, 28, 29, 30]
        *   **根拠:** 適格性判断に必要なデータが確認できない。
        *   **関連データ:** LBドメインにVisit 1 (Screening 1) のデータはあるが、これが除外基準判定に用いられたすべての検査項目を網羅しているか不明。特にEXCL27, 28, 29, 30で指定された項目がすべて含まれているか確認が必要（提供データからは確認可能）。
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験薬の初期投与量（Day 1-16: 54mg）および81mgへの増量タイミング（Day 17）について、プロトコル本文（3.1, 3.6.2）とFigure LZZT.1の間に解釈の齟齬を生む可能性がある。本文では初期投与54mgが示唆されるが、増量タイミングの明確な規定がない。投与計画の遵守状況の解釈に影響する可能性がある。
        *   **プロトコル該当箇所:** Section 3.1, Figure LZZT.1, Section 3.6.2
        *   **根拠:** プロトコル内の記載不整合の可能性。
        *   **関連データ:**
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 54, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-02-04' (Day 1)
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-02-20' (Day 17)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象名「BLOOD PRESSURE INCREASED」について。転帰が「RECOVERED/RESOLVED」、終了日が「2013-07-26」(Study Day 173)と記録されていますが、Study Day 177のバイタルサイン測定で臥位血圧が160/98 mmHgと高値でした。AEの転帰評価は適切でしょうか？また、治験薬との関連性評価が「NONE」とされていますが、その評価根拠について確認させてください。
        *   **クエリ文面（英語）:** Regarding the AE Term 'BLOOD PRESSURE INCREASED', the Outcome is 'RECOVERED/RESOLVED' and End Date is '2013-07-26' (Study Day 173). However, on Study Day 177, supine BP was 160/98 mmHg. Please confirm if the AE outcome assessment is appropriate. Also, please confirm the rationale for the causality assessment ('NONE').
        *   **判断理由:** AEの転帰評価とVSデータに矛盾があり、安全性評価の正確性を確認するため。また、治験薬との関連性評価の根拠を確認し、適切な安全性評価を行うため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='BLOOD PRESSURE INCREASED', AE.AEENDTC='2013-07-26', AE.AEOUT='RECOVERED/RESOLVED', AE.AEREL='NONE', VS.VSTESTCD='SYSBP'/'DIABP', VS.VSDTC='2013-07-30', VS.VSSTRESN=160/98
            *   関連するプロトコル箇所: Section 3.9.3.2 (Adverse Events)
            *   関連する医学的知見: 高血圧の評価基準、AE評価の原則
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 177のバイタルサイン測定において、臥位血圧160/98mmHgから立位1分後128/60mmHgへの血圧低下が認められました。起立性低血圧に関連する症状（めまい、ふらつき等）の有無について確認させてください。また、この血圧変動と治験薬との関連性について、医師の評価をお願いします。
        *   **クエリ文面（英語）:** On Study Day 177 vital signs, BP dropped from 160/98 mmHg (supine) to 128/60 mmHg (standing after 1 min). Please confirm if there were any symptoms related to orthostatic hypotension (e.g., dizziness, lightheadedness). Also, please provide the physician's assessment of the relationship to the study drug.
        *   **判断理由:** 起立性低血圧の可能性があり、症状の有無と治験薬との関連性を確認し、参加者の安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='SYSBP'/'DIABP', VS.VSDTC='2013-07-30', VS.VSSTRESN (Supine vs Standing)
            *   関連するプロトコル箇所: Section 3.9.3.4.1 (Vital Sign Determination)
            *   関連する医学的知見: 起立性低血圧の定義と症状、コリン作動薬の副作用
    *   **クエリNo.:** Q-3 (関連指摘No.: M-4, D-2, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 166からStudy Day 179に使用された併用薬「CEPHALEXIN」、およびStudy Day 166からStudy Day 172に使用された併用薬「PROMETHAZINE HCL W/CODEINE」について。これらの薬剤が処方された理由（適応となった病名や症状）をお知らせください。関連する有害事象が報告されていないようですので確認させてください。
        *   **クエリ文面（英語）:** Regarding concomitant medications 'CEPHALEXIN' (used from Study Day 166 to 179) and 'PROMETHAZINE HCL W/CODEINE' (used from Study Day 166 to 172), please provide the reason for prescription (indication/symptoms). No corresponding AE seems to be reported. Please confirm.
        *   **判断理由:** 併用薬の使用理由が不明であり、未報告のAEが存在する可能性があるため、データの完全性と安全性評価の正確性を確保するため。また、Promethazine/Codeineがプロトコル上許容される使用であったか確認するため。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='CEPHALEXIN', CM.CMSTDTC='2013-07-19', CM.CMENDTC='2013-08-01'; CM.CMTRT='PROMETHAZINE HCL W/CODEINE', CM.CMSTDTC='2013-07-19', CM.CMENDTC='2013-07-25'; AEドメインに対応記録なし
            *   関連するプロトコル箇所: Section 3.4.2.2 [31], Section 3.8, Section 3.9.3.2
    *   **クエリNo.:** Q-4 (関連指摘No.: P-1, D-3)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 治験薬の投与について。投与量がStudy Day 178から81mgから54mgに変更されていますが、その理由をお知らせください。本症例は治験を完遂しており、プロトコルに規定された早期中止時の漸減投与とは状況が異なると考えられます。プロトコル逸脱の可能性がありますので、詳細を確認させてください。
        *   **クエリ文面（英語）:** Regarding study drug administration, the dose was changed from 81mg to 54mg from Study Day 178. Please provide the reason for this dose reduction. As the subject completed the study, this differs from the tapering described for early discontinuation in the protocol. This may be a protocol deviation. Please clarify.
        *   **判断理由:** プロトコルに規定されていない可能性のある用量変更であり、その理由が不明なため。プロトコル遵守状況の確認と、有効性・安全性評価への影響を評価するために必須の情報。
        *   **判断根拠:**
            *   関連するデータ: EX.EXDOSE, EX.EXSTDTC, EX.EXENDTC; DS.DSDECOD='COMPLETED'
            *   関連するプロトコル箇所: Section 3.1, 3.6.2, 3.10.1
    *   **クエリNo.:** Q-5 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日について。DMドメインの「Date/Time of Informed Consent」が記録されていません。治験関連手順開始前に適切に同意が取得された日付を確認させていただけますでしょうか。
        *   **クエリ文面（英語）:** Regarding the date of informed consent, the 'Date/Time of Informed Consent' in the DM domain is missing. Could you please confirm the date when informed consent was obtained prior to the start of study procedures?
        *   **判断理由:** GCP遵守と参加者の権利保護の観点から、同意取得日の記録を確認するため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC=''
            *   関連するプロトコル箇所: Section 5.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3, P-1)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor/DM
        *   **疑義事項/確認内容:** Week 24における有効性評価結果の不一致（ADAS-Cog(11)改善 vs CIBIC+悪化）について、内部で要因を検討する。特にDay 178からの用量減量（P-1/Q-4で確認中）がWeek 24評価に影響した可能性を考慮し、最終的な有効性評価の解釈に注意を払う。
        *   **判断理由:** 主要評価項目間の結果不一致は試験結果の解釈に影響を与えるため、内部での検討・記録が必要。医療機関への問い合わせで解決する性質の問題ではない。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD='ACTOT'/'CIBIC', QS.VISITNUM=12; EXデータ (用量変更)
            *   関連するプロトコル箇所: Section 2.1 (Primary Objectives), 4.3 (Efficacy Analyses)
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHSTDTCの一部欠損、AEドメインのMedDRAコード関連変数、CMドメインのCMDECOD/CMCLAS（UNCODED）およびCMENDTC/CMENDYの一部に欠損または未完了データを確認。データクリーニングプロセスで対応し、データの完全性と標準化を図る。
        *   **判断理由:** データ品質の問題であり、標準的なデータマネジメントプロセスで対応可能。現時点で医学的評価や安全性への直接的な影響は小さいと判断。
        *   **判断根拠:**
            *   関連するデータ: MH, AE, CMドメインの該当変数
    *   **確認事項No.:** I-3 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** スクリーニング時の臨床検査値データが限定的であり、除外基準（EXCL27-30）の遵守を完全に確認できない。ただし、Visit 1のLBデータは提供されており、主要な項目は含まれている可能性が高い。適格性確認プロセスが適切に行われたか、関連文書（例：Source Data Verification記録）を内部で確認する。
        *   **判断理由:** 提供データのみでは完全な確認はできないが、重大な違反を示唆する情報はないため、内部確認に留める。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (Visit 1)
            *   関連するプロトコル箇所: Section 3.4.2.2 [27, 28, 29, 30]
    *   **確認事項No.:** I-4 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 治験薬の初期投与量（Day 1-16: 54mg）と増量タイミング（Day 17: 81mg）について、プロトコル本文（3.1）の記載「All patients receiving xanomeline will be started at 50 cm2 TTS Formulation E」に基づくと、初期投与は計画通りと解釈できる。増量タイミングの明確な規定はないが、Visit 4 (Day 16) 後であることから逸脱とは断定し難い。内部で解釈を統一し記録する。
        *   **判断理由:** プロトコル内の記載の曖昧さによる解釈の問題であり、明らかな逸脱とは言えないため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.1, Figure LZZT.1, Section 3.6.2
    *   **確認事項No.:** I-5 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 持続・悪化している適用部位反応について、Hydrocortisoneクリームによる管理が行われていることを確認。症状の程度は中等度であり、重篤ではないため、現時点では追加のアクションは不要と判断するが、同様の事象が集積するか注視する。
        *   **判断理由:** 治験薬で予想される範囲のAEであり、対症療法も行われているため。ただし、QOLへの影響を考慮し、傾向監視は必要。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (適用部位反応), CMドメイン (Hydrocortisone)
            *   関連するプロトコル箇所: Section 3.6.2, 3.9.3.4