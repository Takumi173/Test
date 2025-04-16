# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
77歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年03月27日発症、PRIMARY DIAGNOSIS）、心筋梗塞（2000年05月15日発症）、冠動脈バイパス術（2006年12月16日実施）が報告されている。Significant Pre-existing Conditionとして心疾患、リビドー亢進、心電図異常（ST上昇・低下）、期外収縮も報告されている。教育歴は12年。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年09月20日|Day -16 (SCREENING 1)|スクリーニング検査実施。既往歴、併用薬（アスピリン）、人口統計学的情報、教育歴、MMSE、MHIS (Score 0) 評価。臨床検査値にてクレアチニン 1.8 mg/dL (High)。バイタルサイン測定（立位1分後 SBP -24 mmHg）。|
|2013年09月27日|Day -9 (SCREENING 2)|バイタルサイン測定。|
|2013年10月06日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg Patch 投与開始。併用薬 Premarin 開始。バイタルサイン測定（立位1分後 SBP -24 mmHg）。ADAS-Cog(11) Total Score 27。NPI-X Total Score 61。DAD評価実施。|
|2013年10月18日|Day 13 (AMBUL ECG PLACEMENT)|バイタルサイン測定（立位1分後 SBP -24 mmHg）。|
|2013年10月19日|Day 14 (WEEK 2)|有害事象「Myocardial Infarction」(Mild, Causality=NONE, Action Taken=DRUG WITHDRAWN?)、「Ventricular Septal Defect」(Mild, Causality=NONE)、「Late effects of cerebral infarction」(Severe, Causality=NONE) 発現。臨床検査値にてBUN 29 mg/dL (High)、Albumin 3.3 g/dL (Low)。バイタルサイン測定。NPI-X Total Score 22 (改善)。治験薬 Xanomeline 54 mg Patch 投与終了。|
|2013年10月20日|Day 15 (N/A)|治験薬 Xanomeline 81 mg Patch 投与開始 (増量)。|
|2013年10月29日|Day 24 (N/A)|併用薬 Premarin 投与終了。|
|2013年11月01日|Day 27 (N/A)|臨床検査値測定 (WEEK 4 Visit関連)。BUN 23 mg/dL (Normal)、Albumin 3.4 g/dL (Low)。Disposition Event 'FINAL LAB VISIT' 記録。|
|2013年11月05日|Day 31 (N/A)|有害事象「Rash」(Mild, Causality=PROBABLE)、「Pruritus」(Mild, Causality=PROBABLE) 発現。|
|2013年11月06日|Day 32 (N/A)|併用薬 Hydrocortisone, topical 開始。|
|2013年11月09日|Day 35 (WEEK 4)|バイタルサイン測定。NPI-X Total Score 38 (悪化)。(Visit Window逸脱)|
|2013年11月18日|Day 44 (N/A)|有害事象「Brain Death」(Severe, Causality=NONE, Outcome=RECOVERED/RESOLVED?) 発現。治験薬 Xanomeline 81 mg Patch 投与終了。|
|2013年11月19日|Day 45 (N/A)|有害事象「Myocardial Infarction」が回復。|
|2013年11月22日|Day 48 (N/A)|有害事象「Rash」、「Pruritus」が回復。併用薬 Hydrocortisone, topical 終了。|
|2013年11月24日|Day 50 (WEEK 6)|治験中止（有害事象のため）。バイタルサイン測定（立位3分後 SBP -20 mmHg）。ADAS-Cog(11) Total Score 30 (悪化)。CIBIC+ Score 4 (No Change)。NPI-X Total Score 16 (改善)、Hallucinations 新規出現。DAD評価実施。(Visit Window逸脱)|
|2013年12月06日|Day 62 (AE FOLLOW-UP)|AEフォローアップVisit。治験参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** Day 44に発現した有害事象「Brain Death」の転帰が「RECOVERED/RESOLVED」と記録されている。これは医学的にありえず、データの誤りである可能性が極めて高い。事象名自体も確認が必要であり、これが治験中止の直接的な原因と考えられる。治験薬との関連性 (Causality='NONE') も再評価が必要。参加者の安全に関わる重大な記録不備。
        *   **根拠:** 「Brain Death」は不可逆的な状態であり、「回復/軽快」という転帰はありえないという一般的な医学知識。治験中止理由が「ADVERSE EVENT」であること。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 44
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 14に有害事象「Myocardial Infarction」(Mild) が報告されている。患者は心筋梗塞および冠動脈バイパス術の既往があり、心血管リスクが高い。治験薬 (Xanomeline) はコリン作動薬であり心血管系への影響（徐脈、血圧低下等）が知られているため、報告された関連性評価 (Causality='NONE') が妥当か、慎重な再評価が必要。また、Action Takenが 'DRUG WITHDRAWN' となっているが、実際には用量が増量されており矛盾している。
        *   **根拠:** 患者の既往歴、Xanomelineの薬理作用に関する一般的な医学知識、AE記録とEX記録の矛盾。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 14
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT'
            *   [Sequence Number(EX.EXSEQ)] = 2
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 15
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Day 14に有害事象「Late effects of cerebral infarction」(Severe) が報告されている。開始日がDay 14であることから新規イベントのようにも読めるが、事象名からは既往の脳梗塞後遺症の悪化とも考えられる。重症度がSevereと評価されている点も踏まえ、イベントの性質（新規発症か既往の悪化か）と臨床的評価の詳細を確認する必要がある。
        *   **根拠:** 事象名と発現日の関係性、重症度評価。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   [Sequence Number(AE.AESEQ)] = 4
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 14
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Day 14に有害事象「Ventricular Septal Defect」(Mild) が報告されている。成人での新規発症は考えにくく、先天性のものが偶然発見されたか、あるいは心エコー所見などの誤記の可能性がある。臨床的な影響は小さいと考えられる。
        *   **根拠:** VSDの病態に関する一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   [Sequence Number(AE.AESEQ)] = 2
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** ベースライン (Day 1) および治験薬投与中 (Day 13, Day 50) に、立位での収縮期血圧低下 (-20 mmHg以上) が複数回観察されている。Xanomelineは血圧低下を引き起こす可能性があるため、症候性起立性低血圧のリスクが懸念される。関連する症状（めまい、ふらつき等）の有無や、有害事象としての報告要否について確認が必要。
        *   **根拠:** VSデータの測定値、Xanomelineの薬理作用に関する一般的な医学知識。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', 'DIABP', 'PULSE'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', 'STANDING'
            *   [Study Day of Vital Signs(VS.VSDY)] = 1, 13, 50 (他スクリーニング日も含む)
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** 有効性評価指標の結果に一貫性がない。ADAS-Cog(11)はベースラインから悪化 (27→30)、CIBIC+は不変 (4)、NPI-Xは変動しつつ全体的に改善傾向 (61→16) だが幻覚が新規出現、DADは項目により改善/悪化が混在している。治験薬の明確な有効性を示す結果とは言えず、評価の信頼性について疑問が残る。
        *   **根拠:** QSドメインの各評価項目の経時変化の比較。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'NPTOT', 'DAITM*'
            *   [Study Day of Finding(QS.QSDY)] = 1, 14, 35, 50

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「Brain Death」(AESEQ=3) の転帰 (AEOUT) が 'RECOVERED/RESOLVED' と記録されており、医学的にありえない。データ入力エラーの可能性が極めて高く、死亡情報の正確性に関わるため修正が必要。
        *   **根拠:** 医学的常識との矛盾。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 有害事象「Myocardial Infarction」(AESEQ=1) に対する処置 (AEACN) が 'DRUG WITHDRAWN' と記録されているが、治験薬投与記録 (EXドメイン, EXSEQ=2) ではDay 15から用量が増量され投与が継続されている。記録間の矛盾があり、実際の処置と投与状況の確認が必要。
        *   **根拠:** AEドメインとEXドメイン間のデータ不整合。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Sequence Number(EX.EXSEQ)] = 2
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 15
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 治験薬投与記録 (EXドメイン, EXSEQ=2) において、Visit Name (EX.VISIT='WEEK 2') および Planned Study Day of Visit (EX.VISITDY=14) と、実際の投与開始日 (EX.EXSTDTC='2013-10-20', EX.EXSTDY=15) に1日のずれがある。記録の正確性の問題だが、臨床評価への影響は小さいと考えられる。
        *   **根拠:** EXドメイン内のVisit情報と日付情報の不整合。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 2
            *   [Visit Name(EX.VISIT)] = 'WEEK 2'
            *   [Planned Study Day of Visit(EX.VISITDY)] = 14
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20'
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 15
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 治験中止イベント (DSSEQ=1, DSDECOD='ADVERSE EVENT') の発生日 (DSSTDY=50) が、原因と考えられるAE 'Brain Death' (AESTDY=44) の発生日と異なる。また、RELRECデータではこの中止イベント (DSSEQ=1) がAE 'RASH' (AESEQ=5, 7) と関連付けられているが、医学的には 'Brain Death' が中止理由として妥当と考えられる。RELRECの関連付けやDSの記録に問題がある可能性。
        *   **根拠:** DS, AE, RELRECドメイン間の論理的な不整合。
        *   **関連データ:**
            *   [Sequence Number(DS.DSSEQ)] = 1
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
            *   [Sequence Number(AE.AESEQ)] = 3 (Brain Death)
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 44
            *   [Identifying Variable(RELREC.IDVAR)] = 'DSSEQ', 'AESEQ'
            *   [Identifying Variable Value(RELREC.IDVARVAL)] = '   1', '   5', '   7'
            *   [Relationship Identifier(RELREC.RELID)] = '01-704-1017-E11'
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** Disposition Eventとして 'FINAL LAB VISIT' (DSSEQ=2) が記録されているが、収集日時 (DSDTC) が同日のLB測定日時 (LBDTC) と一致しており、単なる検査測定イベントを誤ってDispositionとして記録している可能性がある。Disposition Eventの定義として不適切。
        *   **根拠:** DSイベントの性質と収集日時の関連性。
        *   **関連データ:**
            *   [Sequence Number(DS.DSSEQ)] = 2
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT'
            *   [Date/Time of Collection(DS.DSDTC)] = '2013-11-01T10:45'
            *   [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-11-01T10:45' (Visit 5, Week 4)
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** Week 6 (Day 50) のNPI-X評価において、幻覚 (Hallucinations) の有無を問う質問 (QS.QSTESTCD='NPITM02') の結果が 'ABSENT' (QSSTRESN=0) であるにも関わらず、頻度 (NPITM02F)、重症度 (NPITM02V)、介護者苦痛度 (NPITM02D) にスコア (1, 1, 2) が入力されている。データに矛盾があり、評価の信頼性に影響する。
        *   **根拠:** QSドメイン内の同一評価項目におけるデータ不整合。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM02', 'NPITM02F', 'NPITM02V', 'NPITM02D'
            *   [Visit Number(QS.VISITNUM)] = 7
            *   [Study Day of Finding(QS.QSDY)] = 50
            *   [Character Result/Finding in Std Format(QS.QSSTRESC)] = '0', '1', '1', '2'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0, 1, 1, 2
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** DAD評価において、Baseline (Day 1) で 'NA' (Not Applicable) と評価された項目 (DAITM04, 30, 31, 32) が、Week 6 (Day 50) では 'N' (No) と評価されている。BaselineでNAと評価された理由、およびWeek 6で評価可能となった理由が不明。評価の一貫性に疑問があるが、主要評価項目ではないため影響は限定的。
        *   **根拠:** QSドメイン内の同一評価項目の経時変化における評価不能理由の不整合。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM04', 'DAITM30', 'DAITM31', 'DAITM32'
            *   [Study Day of Finding(QS.QSDY)] = 1, 50
            *   [Character Result/Finding in Std Format(QS.QSSTRESC)] = '96' (Day 1), '0' (Day 50)
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** 併用薬 Hydrocortisone, topical (CMSEQ=9, 11, 13) の Standardized Medication Name (CMDECOD) および Medication Class (CMCLAS) が 'UNCODED' となっている。標準辞書へのコーディングが必要。
        *   **根拠:** CMドメインのデータ標準化の不備。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [Medication Class(CM.CMCLAS)] = 'UNCODED'
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** AEドメインおよびMHドメインにおいて、MedDRAコーディング関連変数 (AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCD, MHLLT, MHDECOD, MHHLT, MHHLGT) に欠損が見られるレコードがある。コーディングが未完了か、辞書バージョン等の問題の可能性。データの完全性の問題。
        *   **根拠:** AE, MHドメインにおける必須または期待される変数の欠損。
        *   **関連データ:** AE, MHドメインの複数レコード

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が記録されていない。プロトコル 5.1項では治験手順開始前の同意取得が必須であり、同意取得の確認ができない。参加者の権利保護の観点から問題。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** DMドメインの必須情報（同意取得日）の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 患者は心筋梗塞 (2000年) および冠動脈バイパス術 (2006年) の既往があり、Significant Pre-existing Conditionとして複数の心疾患関連所見が報告されている。除外基準 [17] (A history within the last 5 years of a serious cardiovascular disorder) に抵触しないか、より慎重な評価が必要だった可能性がある。適格性判断の妥当性に疑問。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** MHドメインの既往歴と除外基準の照合。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT', 'CARDIAC DISORDER', 'ST SEGMENT ELEVATED', 'ST SEGMENT DEPRESSED', 'EXTRASYSTOLES'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2000-05-15', '2006-12-16', (他は不明)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時のクレアチニン値 (1.8 mg/dL) が基準値上限 (1.6 mg/dL) を超えており、除外基準 [27b] に該当する可能性がある。プロトコルでは臨床的に問題ないと判断された場合は登録可能だが、その判断と文書化が行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LBデータの値と除外基準の照合。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -16
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬 Premarin (エストロゲン補充療法) が治験開始日 (Day 1) から投与されている。除外基準 [31b] v) では、エストロゲン補充療法は登録前3ヶ月以上安定投与されている場合にのみ許容される。この条件を満たしておらず、プロトコル逸脱の可能性が高い。有効性評価への影響も考えられる。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] v)
        *   **根拠:** CMデータの投与開始日と除外基準の照合。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 1
    *   **指摘No.:** P-5
        *   **重要度:** Critical
        *   **逸脱の可能性:** 治験薬の投与計画からの逸脱。プロトコルではHigh Dose群はWeek 8で54mgから81mgへ増量する計画だが、本症例ではWeek 2 (Day 15) で増量されている。これは明確なプロトコル逸脱であり、特に有害事象「Myocardial Infarction」発現直後の増量であることから、参加者の安全性リスクを高めた可能性があり、有効性・安全性評価の解釈にも重大な影響を与える。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design), Figure LZZT.1
        *   **根拠:** EXドメインの投与記録とプロトコルの投与計画の比較。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 1, 2
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Dose per Administration(EX.EXDOSE)] = 54, 81
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 1, 15
            *   [Study Day of End of Treatment(EX.EXENDY)] = 14, 44
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** Week 4 Visit (Visit 5) の一部評価 (VS, QS) がDay 35に実施されており、プロトコル規定のVisit Window (予定日 Day 28 ± 3日) を逸脱している。評価の信頼性に影響を与える可能性。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design) - Visit Window規定
        *   **根拠:** VS, QSデータの測定日とプロトコルのスケジュール規定の比較。
        *   **関連データ:**
            *   [Visit Number(VS.VISITNUM)] = 5, [Study Day of Vital Signs(VS.VSDY)] = 35
            *   [Visit Number(QS.VISITNUM)] = 5, [Study Day of Finding(QS.QSDY)] = 35
            *   [Visit Number(SV.VISITNUM)] = 5, [Planned Study Day of Visit(SV.VISITDY)] = 28
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** Week 6 Visit (Visit 7) の評価 (VS, QS) がDay 50に実施されており、プロトコル規定のVisit Window (予定日 Day 42 ± 3日) を逸脱している。評価の信頼性に影響を与える可能性。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design) - Visit Window規定
        *   **根拠:** VS, QSデータの測定日とプロトコルのスケジュール規定の比較。
        *   **関連データ:**
            *   [Visit Number(VS.VISITNUM)] = 7, [Study Day of Vital Signs(VS.VSDY)] = 50
            *   [Visit Number(QS.VISITNUM)] = 7, [Study Day of Finding(QS.QSDY)] = 50
            *   [Visit Number(SV.VISITNUM)] = 7, [Planned Study Day of Visit(SV.VISITDY)] = 42

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1, D-4)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「Brain Death」(AESEQ=3) について、「Outcome of Adverse Event」が「RECOVERED/RESOLVED」と記録されていますが、これは正確でしょうか？ 事象名、転帰、および治験中止 (DSSEQ=1) との関連について確認・修正をお願いします。参加者の最終的な状態と中止理由の正確な把握のため、ご協力をお願いいたします。
        *   **クエリ文面（英語）:** Regarding AE 'Brain Death' (AESEQ=3), the Outcome of Adverse Event is recorded as 'RECOVERED/RESOLVED'. Please confirm if this is correct. Please review and correct the event term, outcome, and its relationship to study discontinuation (DSSEQ=1) to ensure accurate reporting of the participant's final status and reason for withdrawal.
        *   **判断理由:** 死亡に関連する可能性のある重大な有害事象の転帰記録が医学的にありえず、データの正確性と参加者の最終状態の把握に重大な問題があるため。治験中止理由の特定にも関わる。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Sequence Number(AE.AESEQ)] = 3, [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Sequence Number(DS.DSSEQ)] = 1
            *   関連する医学的知見: 脳死は不可逆的な状態である。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-2, P-5)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「Myocardial Infarction」(AESEQ=1) に対する「Action Taken with Study Treatment」が「DRUG WITHDRAWN」と記録されていますが、治験薬投与記録 (EX) ではDay 15から用量が増量されています。実際の処置（治験薬の中止、継続、用量変更）と投与の経緯について確認・修正をお願いします。また、心筋梗塞の既往がある患者での再発であり、治験薬との関連性 (Causality) について再度ご評価いただけますでしょうか。
        *   **クエリ文面（英語）:** For AE 'Myocardial Infarction' (AESEQ=1), the Action Taken with Study Treatment is 'DRUG WITHDRAWN', but EX domain shows dose escalation on Day 15. Please confirm/correct the actual action taken (discontinuation, continuation, dose change) and treatment course. Also, given the patient's history of MI, please re-assess the Causality to the study drug.
        *   **判断理由:** 重大な有害事象発生時の治験薬の処置に関する記録が矛盾しており、実際の対応と安全管理の状況が不明確なため。また、治験薬の安全性評価に関わる重要な情報であるため。プロトコルからの投与計画逸脱にも関連する。
        *   **判断根拠:**
            *   関連するデータ: [Sequence Number(AE.AESEQ)] = 1, [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN', [Causality(AE.AEREL)] = 'NONE', [Sequence Number(EX.EXSEQ)] = 2, [Study Day of Start of Treatment(EX.EXSTDY)] = 15
            *   関連するプロトコル箇所: Section 3.1 (投与計画)
            *   関連する医学的知見: 患者の既往歴、Xanomelineの心血管系への影響。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「Late effects of cerebral infarction」(AESEQ=4) がDay 14に発現し、「Severity/Intensity」が「SEVERE」と記録されています。これは新規発症の脳梗塞後遺症ですか、それとも既往の脳梗塞後遺症の悪化でしょうか？ 事象の詳細と臨床的な評価についてお知らせください。
        *   **クエリ文面（英語）:** Regarding AE 'Late effects of cerebral infarction' (AESEQ=4) starting Day 14, recorded as 'SEVERE'. Was this a new onset or worsening of pre-existing sequelae? Please provide details and clinical assessment.
        *   **判断理由:** 重症と評価された神経学的イベントの性質が不明確であり、安全性評価のために詳細情報が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION', [Sequence Number(AE.AESEQ)] = 4, [Severity/Intensity(AE.AESEV)] = 'SEVERE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 14
    *   **クエリNo.:** Q-4 (関連指摘No.: M-5)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** ベースラインおよび治験期間中に立位での「Systolic Blood Pressure」の低下 (-20 mmHg以上) が複数回認められます (例: Study Day 1, Study Day 13)。起立性低血圧に関連する症状（めまい、ふらつき等）は観察されましたか？ 有害事象としての報告が必要かご評価をお願いします。
        *   **クエリ文面（英語）:** Postural drops in Systolic Blood Pressure (>20 mmHg) were noted on multiple occasions (e.g., Study Day 1, Study Day 13). Were any symptoms associated with orthostatic hypotension (e.g., dizziness, lightheadedness) observed? Please assess if AE reporting is required.
        *   **判断理由:** 治験薬との関連が疑われる血圧低下が観察されており、症候性の有無を確認し、参加者の安全性評価を行う必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', 'STANDING', [Study Day of Vital Signs(VS.VSDY)] = 1, 13, 50 (他も含む)
            *   関連する医学的知見: Xanomelineの血圧への影響。
    *   **クエリNo.:** Q-5 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 「Date/Time of Informed Consent」の記録がありません。同意取得日と、最初の治験関連手順（スクリーニング検査等）の実施日を確認し、記録をお願いします。参加者の権利保護の確認に必要です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please confirm and record the date of informed consent and the date of the first study-related procedure (e.g., screening tests) to ensure participant rights protection.
        *   **判断理由:** 同意取得は治験参加の基本であり、記録がない場合はGCP上の問題となるため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
    *   **クエリNo.:** Q-6 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の「Creatinine」が「1.8 mg/dL」と基準値上限 (1.6 mg/dL) を超えていましたが、登録されています。プロトコル (Section 3.4.2.2 [27b]) に従い、臨床的に問題ないと判断された根拠について、コメントまたは記録をお願いします。
        *   **クエリ文面（英語）:** Screening Creatinine was 1.8 mg/dL (ULN 1.6 mg/dL), exceeding the reference range per protocol exclusion criteria [27b]. Please provide documentation or comment confirming the assessment that this finding was not clinically significant, allowing enrollment.
        *   **判断理由:** 除外基準に該当する可能性のある検査値異常があり、適格性判断の根拠を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Result or Finding in Original Units(LB.LBORRES)] = '1.8', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6', [Study Day of Specimen Collection(LB.LBDY)] = -16
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「PREMARIN」が治験開始日 (Study Day 1) から投与されています。プロトコル (Section 3.4.2.2 [31b] v)) では、エストロゲン補充療法は登録前3ヶ月以上安定投与されていることが条件ですが、この条件を満たしていますか？ 投与開始日と安定投与期間について確認をお願いします。
        *   **クエリ文面（英語）:** Concomitant medication 'PREMARIN' was started on Study Day 1. Protocol (Section 3.4.2.2 [31b] v)) requires estrogen supplements to be stable for at least 3 months prior to enrollment. Please confirm if this criterion was met, verifying the start date and duration of stable dosing before enrollment.
        *   **判断理由:** 併用薬の使用がプロトコルの規定（除外基準）に違反している可能性があり、適格性と評価への影響を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN', [Study Day of Start of Medication(CM.CMSTDY)] = 1
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] v)
    *   **クエリNo.:** Q-8 (関連指摘No.: P-6, P-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 4 Visit (Visit 5) および Week 6 Visit (Visit 7) の一部評価が、プロトコルで規定されたVisit Window (予定日±3日) を超えて実施されています (それぞれStudy Day 35, Study Day 50)。逸脱理由と、評価結果の信頼性への影響についてコメントをお願いします。
        *   **クエリ文面（英語）:** Some assessments for Week 4 Visit (Visit 5) and Week 6 Visit (Visit 7) were performed outside the protocol-specified visit window (±3 days), on Study Day 35 and Study Day 50, respectively. Please provide the reason for deviation and comment on the potential impact on data reliability.
        *   **判断理由:** 評価スケジュールの逸脱があり、データの信頼性への影響を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [Study Day of Vital Signs(VS.VSDY)] = 35, 50; [Study Day of Finding(QS.QSDY)] = 35, 50; [Planned Study Day of Visit(SV.VISITDY)] = 28, 42
            *   関連するプロトコル箇所: Section 3.1 (Visit Window規定)
    *   **クエリNo.:** Q-9 (関連指摘No.: D-6)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** Week 6 の NPI-X評価において、「HALLUCINATIONS PRESENT」が「ABSENT」(スコア0) と記録されている一方、「HALLUCINATIONS FREQUENCY」、「HALLUCINATIONS SEVERITY」、「HALLUCINATIONS DISTRESS」にはスコア (1, 1, 2) が入力されています。どちらの記録が正しいか確認・修正をお願いします。
        *   **クエリ文面（英語）:** For the Week 6 NPI-X assessment, 'HALLUCINATIONS PRESENT' (NPITM02) is recorded as 'ABSENT' (score 0), but scores (1, 1, 2) are entered for Frequency (NPITM02F), Severity (NPITM02V), and Distress (NPITM02D). Please clarify which entry is correct and revise accordingly.
        *   **判断理由:** 同一評価項目内でデータが矛盾しており、評価結果の信頼性を損なうため修正が必要。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'NPITM02', 'NPITM02F', 'NPITM02V', 'NPITM02D', [Visit Number(QS.VISITNUM)] = 7, [Character Result/Finding in Std Format(QS.QSSTRESC)] / [Numeric Finding in Standard Units(QS.QSSTRESN)]
*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有害事象「Ventricular Septal Defect」(AESEQ=2) の事象名が適切か内部で確認する。成人での新規発症は考えにくいため、心エコー所見等の誤記の可能性を考慮。ただし、重症度はMildであり、臨床的な影響は小さいと判断されるため、医療機関への問い合わせは不要とする。
        *   **判断理由:** 臨床的影響が小さく、データの解釈に大きな影響を与えないと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT', [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   関連する医学的知見: VSDの病態。
    *   **確認事項No.:** I-2 (関連指摘No.: M-6)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価指標 (ADAS-Cog, CIBIC+, NPI-X, DAD) 間の結果に一貫性が見られない点について、統計解析担当者と情報を共有し、最終的な有効性評価の解釈において注意を払う必要があることを記録する。
        *   **判断理由:** 試験の主要な目的である有効性評価の解釈に影響を与える可能性があるため、内部での認識共有と記録が必要。
        *   **判断根拠:**
            *   関連するデータ: QSドメインの有効性評価データ
    *   **確認事項No.:** I-3 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 治験薬投与記録 (EXドメイン, EXSEQ=2) におけるVisit情報と実際の投与開始日の1日のずれについて、データ入力プロセスまたはソースデータを確認する。臨床評価への直接的な影響は小さいと判断されるため、内部確認とする。
        *   **判断理由:** データの品質に関する問題だが、投与期間全体の評価への影響は限定的と判断されるため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン (EXSEQ=2) のVisit関連変数と日付変数
    *   **確認事項No.:** I-4 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** Disposition Eventとして記録された 'FINAL LAB VISIT' (DSSEQ=2) が、SDTM IGおよびプロトコルにおけるDisposition Eventの定義として適切か、データ標準担当者と確認する。データの意味づけに関する問題。
        *   **判断理由:** データ標準の遵守と一貫性確保のため内部確認が必要だが、主要な評価への影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: DSドメイン (DSSEQ=2), LBドメイン (Visit 5)
            *   関連資料: SDTM IG, プロトコル
    *   **確認事項No.:** I-5 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** DAD評価において、Baselineで 'NA' と評価された項目がWeek 6で 'N' と評価されている点について、評価手順やデータ入力規則、NAの定義を確認する。評価の一貫性に関する問題だが、影響は小さい。
        *   **判断理由:** データ品質の問題だが、主要評価項目ではなく影響は限定的。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (DAD関連項目)
    *   **確認事項No.:** I-6 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 併用薬 Hydrocortisone, topical の標準病名 (CMDECOD) および薬剤クラス (CMCLAS) が未コード化 ('UNCODED') であるため、コーディング担当者に修正を依頼する。
        *   **判断理由:** データ標準化と完全性のための修正が必要だが、緊急性は低い。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMSEQ=9, 11, 13)
    *   **確認事項No.:** I-7 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインおよびMHドメインにおいて、MedDRAコーディング関連変数に欠損が見られるため、コーディング担当者に状況を確認し、必要に応じてコーディングの完了を依頼する。
        *   **判断理由:** データの完全性を高めるための確認が必要だが、緊急性は低い。
        *   **判断根拠:**
            *   関連するデータ: AE, MHドメインのコーディング関連変数
    *   **確認事項No.:** I-8 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor, CRA
        *   **疑義事項/確認内容:** 患者の心血管系の既往歴・併存疾患が除外基準 [17] (Serious cardiovascular disorder within last 5 years) に抵触しなかったか、適格性判断の妥当性について内部で再評価し、議論の結果を記録する。
        *   **判断理由:** 適格性判断は試験の科学的妥当性と参加者の安全性に影響するため、内部での確認と記録が必要。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]
    *   **確認事項No.:** I-9 (関連指摘No.: P-5)
        *   **重要度:** Critical
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** High Dose群における治験薬の増量タイミングがプロトコル計画 (Week 8) から逸脱し、Week 2で実施された件について、重大なプロトコル逸脱として記録し、逸脱の原因（サイトの誤解、指示ミス等）を調査・文書化する。
        *   **判断理由:** 参加者の安全性と試験の科学的妥当性に重大な影響を与える可能性のあるプロトコル逸脱であり、原因究明と記録が必須。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.1, Figure LZZT.1
    *   **確認事項No.:** I-10 (関連指摘No.: 評価スケジュール)
        *   **重要度:** Major
        *   **確認担当者:** CRA, DM
        *   **疑義事項/確認内容:** プロトコルで規定されているPK採血 (Visits 3, 4, 5, 7, 9, 11) の実施状況を確認する。提供されたLBデータにはPK関連項目が見当たらないため、データが別途存在するのか、未実施なのかを確認し、未実施の場合は理由を記録する。
        *   **判断理由:** 試験目的（PK評価）の達成に関わるため、実施状況の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (PK関連データなし)
            *   関連するプロトコル箇所: Section 3.9.2
    *   **確認事項No.:** I-11 (関連指摘No.: 評価スケジュール)
        *   **重要度:** Major
        *   **確認担当者:** CRA, DM
        *   **疑義事項/確認内容:** プロトコルで規定されているAmbulatory ECG (Visit 2) の実施状況と結果を確認する。関連データ (EGドメイン等) が提供されていないため、実施有無と結果データが存在するか確認し、未実施・データ欠損の場合は理由を記録する。
        *   **判断理由:** 安全性評価（特に心血管系）に関する重要な評価であり、実施状況の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: (EGドメイン等なし)
            *   関連するプロトコル箇所: Section 3.9.3.4.2, 3.9.4

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
64歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2008年7月発症）、肺気腫（SIGNIFICANT PRE-EXISTING CONDITION、MILD）、冠動脈疾患（SIGNIFICANT PRE-EXISTING CONDITION、MILD）、関節炎（SIGNIFICANT PRE-EXISTING CONDITION、MILD）、肺膿瘍ドレナージ術（HISTORICAL DIAGNOSIS、1997年）、腸ポリープ切除術（HISTORICAL DIAGNOSIS、2009年）が報告されている。教育レベルは12年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65 (SCREENING 1)|臨床検査実施。アラニンアミノトランスフェラーゼ (ALT) が 135 U/L (基準値上限 43 U/L)、アスパラギン酸アミノトランスフェラーゼ (AST) が 145 U/L (基準値上限 36 U/L) と高値 (HIGH) を示す。|
|2013年02月21日|Day -9 (UNSCHEDULED 1.1)|臨床検査実施。ALT (19 U/L)、AST (29 U/L) は正常化 (NORMAL)。ナトリウム (Sodium) が 133 mmol/L と軽度低値 (LOW, 基準値下限 135 mmol/L)。|
|2013年02月23日|Day -7 (SCREENING 1)|MMSE評価 (スコア23点相当)、Hachinski Ischemic Scale評価 (スコア1点)。身長、体重、体温、血圧、脈拍測定。既往歴、教育レベル収集。|
|2013年03月02日|Day 1 (BASELINE)|治験薬 (Placebo) 投与開始。ベースライン評価実施 (VS, LB, ADAS-Cog, NPI-X, DAD)。ADAS-COG(11) Subscore (ACTOT) = 14。NPI-X (9) Total Score (NPTOT) = 3。|
|2013年03月04日|Day 3 (N/A)|有害事象「下痢 (DIARRHOEA)」(MILD, POSSIBLE) 発現。|
|2013年03月05日|Day 4 (N/A)|有害事象「不眠症 (INSOMNIA)」(MILD, REMOTE) 発現。併用薬「KAOPECTATE」使用開始 (同日終了)。有害事象「下痢 (DIARRHOEA)」回復。|
|2013年03月06日|Day 5 (N/A)|有害事象「不眠症 (INSOMNIA)」回復。|
|2013年03月14日|Day 13 (WEEK 2)|NPI-X評価 (NPTOT=6)。|
|2013年03月28日|Day 27 (WEEK 4)|臨床検査実施。Ery. Mean Corpuscular Volume (MCV) が 101 fL と軽度高値 (HIGH, 基準値上限 100 fL)。ナトリウム (Sodium) が 146 mmol/L と軽度高値 (HIGH, 基準値上限 145 mmol/L)。アニソサイトーシス (Anisocytes) が 1 (ABNORMAL)。NPI-X評価 (NPTOT=4)。|
|2013年04月27日|Day 57 (WEEK 8)|ADAS-Cog評価 (ACTOT=9, Baselineから改善)。NPI-X評価 (NPTOT=0, Baselineから改善)。|
|2013年05月11日|Day 71 (WEEK 10 (T))|NPI-X評価 (NPTOT=4)。|
|2013年05月25日|Day 85 (WEEK 12)|ADAS-Cog評価 (ACTOT=9)。NPI-X評価 (NPTOT=6)。|
|2013年06月08日|Day 99 (WEEK 14 (T))|NPI-X評価 (NPTOT=6)。|
|2013年06月22日|Day 113 (WEEK 16)|ADAS-Cog評価 (ACTOT=7, Baselineから改善)。CIBIC+評価 (スコア4, NO CHANGE)。DAD評価実施。NPI-X評価 (NPTOT=4)。|
|2013年07月06日|Day 127 (WEEK 18 (T))|NPI-X評価 (NPTOT=4)。|
|2013年07月20日|Day 141 (WEEK 20)|NPI-X評価 (NPTOT=4)。|
|2013年08月03日|Day 155 (WEEK 22 (T))|NPI-X評価 (NPTOT=3)。|
|2013年08月09日|Day 161 (WEEK 24)|ADAS-Cog評価 (ACTOT=9, Week 16から悪化)。CIBIC+評価 (スコア4, NO CHANGE)。DAD評価実施。NPI-X評価 (NPTOT=2)。|
|2013年08月31日|Day 183 (WEEK 26)|臨床検査実施。ASTが 38 U/L と軽度高値 (HIGH, 基準値上限 36 U/L)。NPI-X評価 (NPTOT=2)。治験薬投与終了。治験完了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Minor
        *   **内容:** 治験終了時 (Day 183) にアスパラギン酸アミノトランスフェラーゼ (AST) が 38 U/L と基準値上限 (36 U/L) をわずかに超える軽度高値を示した。スクリーニング時 (Day -65) にはALT (135 U/L), AST (145 U/L) の顕著な高値があったが、治験開始前 (Day -9) には正常化していた経緯がある。Placebo投与期間中の軽微な変動であり、関連する有害事象や併用薬もないため、臨床的意義は低いと考えられるが、肝機能の変動として記録・注視が必要。
        *   **根拠:** スクリーニング時の肝酵素上昇の既往と、治験終了時の軽度AST上昇。Placebo群であること、変動が軽微であることから臨床的意義は低いと判断。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 183
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 38
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** Day 4に使用された併用薬「KAOPECTATE」について、適応症 (CM.CMINDC) が欠損している。Day 3-4に有害事象「下痢」が報告されており、時間的な関連から下痢に対する使用と推測されるが、記録の完全性に欠ける。医学的評価への影響は小さい。
        *   **根拠:** CMINDCの欠損。AEとの時間的関連性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'KAOPECTATE'
            *   [Sequence Number(CM.CMSEQ)] = 13
            *   [Indication(CM.CMINDC)] = '' (欠損)
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-05'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-03-04'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-03-05'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) がデータセットに記録されていない。プロトコル 5.1 に基づき、治験手順開始前にインフォームド・コンセントの取得は必須である。記録の欠損はGCP上の問題となる可能性があるが、治験が開始されていることから同意は取得されていると推測される。評価への直接的な影響は小さい。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** DM.RFICDTCの欠損。プロトコル要件。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時 (Day -65) のアラニンアミノトランスフェラーゼ (ALT) およびアスパラギン酸アミノトランスフェラーゼ (AST) が基準値上限を大幅に超えており (ALT 135 U/L, AST 145 U/L)、プロトコル Exclusion Criterion [27b] (Laboratory test values exceeding the Lilly Reference Range III for... SGPT, SGOT) に該当した可能性がある。治験参加前 (Day -9) に正常化しているが、当初除外基準に該当した可能性があり、参加を許可した医学的判断（臨床的に意義なし等）とその記録がプロトコル上必要である。この記録が確認できない場合、適格性評価の妥当性に疑義が生じ、参加者の安全性評価にも影響しうる。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** スクリーニング時のLBデータ。プロトコルの除外基準。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 19, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 29, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の葉酸 (Folate) の検査データが提供されておらず、Exclusion Criterion [28b] (Central laboratory test values below reference range for folate...) の評価が完全にはできない。他のデータから問題となる可能性は低いと考えられるが、適格性評価の一部が不完全である。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** Folateデータの欠損。プロトコルの除外基準。
        *   **関連データ:** LBドメインにFolateのデータなし。
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 12 (WEEK 24) の実施日 (SV.SVSTDTC = 2013-08-09, Day 161) が、計画日 (SV.VISITDY = 168) より7日早い。プロトコル 3.1 で規定された Visit Window (Visit 12 は ±4日) から逸脱している。Visit 12 は主要評価項目の測定時期であり、規定からの逸脱はデータの信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design) - Visit Window規定
        *   **根拠:** SVドメインのVISITNUM, VISITDY, SVSTDTC。プロトコルのVisit Window規定。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 12
            *   [Visit Name(SV.VISIT)] = 'WEEK 24'
            *   [Planned Study Day of Visit(SV.VISITDY)] = 168
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09' (Day 161)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor/CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時 (2012年12月27日) の検査結果についてお伺いします。「アラニンアミノトランスフェラーゼ」が「135 U/L」、「アスパラギン酸アミノトランスフェラーゼ」が「145 U/L」と高値であり、除外基準 [27b] に該当した可能性があります。その後の検査 (2013年2月21日) では正常化していますが、治験参加を可能と判断された根拠（例：一過性の原因特定、臨床的に意義なしとの判断）に関する記録について確認させていただけますでしょうか。参加者の安全確保と適格性確認のため、ご教示ください。
        *   **クエリ文面（英語）:** Regarding screening labs on 2012-12-27: ALT was 135 U/L and AST was 145 U/L, potentially meeting Exclusion Criterion [27b]. Values normalized on 2013-02-21. Please confirm and provide documentation for the rationale allowing study participation (e.g., transient cause identified, deemed not clinically significant). This is for patient safety and eligibility verification.
        *   **判断理由:** 除外基準に該当した可能性のある検査値異常について、適格性判断の根拠を確認し、参加者の安全とデータの信頼性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT'/'AST', [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135/145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
            *   関連する医学的知見: 肝機能検査異常の評価、薬剤性肝障害のリスク評価
    *   **クエリNo.:** Q-2 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 12 (WEEK 24) の実施日について確認させてください。「Start Date/Time of Visit」が「2013-08-09」 (Study Day 161) と記録されていますが、計画日 (Day 168) より7日早く、プロトコルで規定された Visit Window (±4日) から逸脱している可能性があります。実施日についてご確認いただけますでしょうか。主要評価項目の評価時期であり、データの信頼性確保のため確認が必要です。
        *   **クエリ文面（英語）:** Please confirm the date for Visit 12 (WEEK 24). The recorded Start Date/Time of Visit is 2013-08-09 (Study Day 161), which is 7 days earlier than the planned Day 168 and appears outside the protocol-specified window (±4 days). Verification is needed for data reliability as this is a key efficacy assessment visit.
        *   **判断理由:** 主要評価時期であるVisitの実施日がプロトコル規定の許容範囲から逸脱している可能性があり、データの信頼性に影響するため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Visit Number(SV.VISITNUM)] = 12, [Visit Name(SV.VISIT)] = 'WEEK 24', [Planned Study Day of Visit(SV.VISITDY)] = 168, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09'
            *   関連するプロトコル箇所: Section 3.1 (Visit Window規定)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 併用薬「KAOPECTATE」の「Indication」(CM.CMINDC) が欠損している。AE「DIARRHOEA」との時間的関連から下痢への使用と推測されるが、記録の完全性の問題として内部で記録する。医学的評価への影響は小さいと判断。
        *   **判断理由:** データ欠損だが、他の情報から推測可能であり、臨床的な安全性や有効性評価への影響は限定的と判断したため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'KAOPECTATE', [Indication(CM.CMINDC)] = '' (欠損), [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-05', AE「DIARRHOEA」 (Day 3-4)
    *   **確認事項No.:** I-2 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 「Date/Time of Informed Consent」(DM.RFICDTC) が欠損している。同意取得は治験実施の前提であるが、記録がない。他の文書（例：Source Document Verification記録、同意説明文書コピー保管状況）で確認可能か、あるいはデータ入力漏れとして内部で記録・管理する。参加者の権利保護の観点からは重要だが、治験が進行・完了している状況から同意は取得済みと判断し、医療機関への緊急の問い合わせは不要と判断。
        *   **判断理由:** GCP上の記録不備だが、治験実施状況から同意取得は確実視され、安全性や評価への直接的な影響は現時点ではないと判断したため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   関連するプロトコル箇所: Section 5.1
    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** スクリーニング時の葉酸 (Folate) データが欠損しており、Exclusion Criterion [28b] の評価が不完全である。他の血液検査値や臨床状態から問題となる可能性は低いと考えられるが、適格性評価の不備として内部で記録する。
        *   **判断理由:** 適格性評価の一部がデータ欠損により不完全だが、他の情報からリスクが高いとは考えにくいため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインにFolateデータなし。
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]
    *   **確認事項No.:** I-4 (関連指摘No.: M-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 治験終了時 (Day 183) にASTが軽度高値 (38 U/L) であった点を記録する。Placebo群であり、臨床的意義は低いと考えられるが、スクリーニング時の肝酵素上昇歴と合わせて、安全性情報として内部で把握しておく。
        *   **判断理由:** 軽微な検査値異常であり、Placebo群であるため緊急性は低いが、過去の異常歴との関連で念のため記録が必要と判断。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = 183, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 38, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
81歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2009年発症）、高血圧、難聴、食道裂孔ヘルニア、足関節浮腫、耳鳴、骨粗鬆症、局所感染、関節炎、甲状腺機能低下症、静脈瘤、副鼻腔炎が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年07月08日|Day -61 (N/A)|有害事象「LOCALISED INFECTION」(Moderate) 発現 (治験薬開始前から持続)|
|2012年08月25日|Day -13 (SCREENING 1)|MMSE実施 (スコア18点程度と推定)、Hachinski Ischemic Scale実施 (スコア1点)。検査にて赤血球(RBC)低値 (3.80)。起立性低血압を示唆する可能性のある血圧変動あり (臥位137/74→立位3分後122/65)。|
|2012年09月02日|Day -5 (N/A)|有害事象「ERYTHEMA」(Mild)、「PRURITUS」(Mild) 発現。|
|2012年09月05日|Day -2 (SCREENING 2)|起立性低血圧を示唆する可能性のある血圧変動あり (臥位137/63→立位1分後121/74)。|
|2012年09月07日|Day 1 (BASELINE)|治験薬「XANOMELINE」 (54 mg Patch) 投与開始。有害事象「ERYTHEMA」、「PRURITUS」回復。有害事象「MICTURITION URGENCY」(Mild) 発現。ADAS-Cog(11)スコア: 7。NPI-X Totalスコア: 2。|
|2012年09月13日|Day 7 (N/A)|有害事象「ARTHRALGIA」(Moderate)、「CELLULITIS」(Moderate) 発現。|
|2012年09月16日|Day 10 (N/A)|治験薬「XANOMELINE」投与終了。|
|2012年09月17日|Day 11 (WEEK 2)|有害事象により治験中止 (DS.DSTERM='ADVERSE EVENT')。ADAS-Cog(11)スコア: 5 (ベースラインから改善)。CIBIC+スコア: 4 (No Change)。NPI-X Totalスコア: 1 (ベースラインから改善)。検査にてMCV高値 (101)、RBC低値 (3.70)、Specific Gravity低値 (1.004)、Anisocytes異常 (1)。起立性低血圧を示唆する可能性のある血圧変動あり (臥位125/60→立位3分後110/60)。|
|2012年09月29日|Day 23 (AE FOLLOW-UP)|AEフォローアップのための来院。|
|2013年02月22日|Day 169 (RETRIEVAL)|Retrieval Visit実施。ADAS-Cog(11)スコア: 9 (Week 2から悪化)。CIBIC+スコア: 5 (Minimal Worsening)。NPI-X Totalスコア: 45 (Week 2から著しく悪化、特にDelusions, Agitation/Aggression, Depression/Dysphoria, Anxiety, Disinhibition, Irritability/Labilityのスコアが高い)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Study Day 11に有害事象により治験中止となっている。RELRECデータによるとAE#7「ARTHRALGIA」(関節痛, Moderate)が中止理由(DS#1)と関連付けられている。しかし、同時期(Study Day 7)にAE#8「CELLULITIS」(蜂窩織炎, Moderate)も発現しており、こちらも中止に関与した可能性がある。中止に至った詳細な経緯と医学的判断の妥当性を確認する必要がある。
        *   **根拠:** 有害事象による中止は、参加者の安全性と試験継続の妥当性に関わる重要なイベントである。中止理由とその評価の正確性は、安全性評価の信頼性に影響する。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-09-17'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA' (AESEQ=7)
            *   [Severity/Intensity(AE.AESEV)] = 'MODERATE' (AESEQ=7)
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-13' (AESEQ=7)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS' (AESEQ=8)
            *   [Severity/Intensity(AE.AESEV)] = 'MODERATE' (AESEQ=8)
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-13' (AESEQ=8)
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16' (AE#7とDS#1を関連付け)

    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Week 2 (Study Day 11)のバイタルサイン測定において、臥位から立位3分後に収縮期血圧が15mmHg低下しており(125→110 mmHg)、起立性低血圧の可能性が示唆される。Screening時にも同様の傾向が見られたが、Baselineでは見られなかった。治験薬Xanomelineはコリン作動薬であり、起立性低血圧や失神を引き起こす可能性があるため、この血圧変動の臨床的意義と治験薬との関連性を評価する必要がある。プロトコルでは除外基準[15]で失神の既往を、[17]で重篤な心血管系疾患を除外している。
        *   **根拠:** 起立性低血圧は転倒や失神のリスクを高め、参加者の安全性に影響を与える可能性がある。治験薬との関連が疑われる場合、安全性評価において重要である。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 125
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 3 MINUTES', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 110
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 60
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 3 MINUTES', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 60
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 85
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Visit Name(VS.VISIT)] = 'WEEK 2', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 3 MINUTES', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 84

    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Retrieval Visit (Study Day 169)で評価されたNPI-X Totalスコアが45と、Baseline (2) およびWeek 2 (1) と比較して著しく悪化している。特に妄想、興奮/攻撃性、抑うつ/不快気分、不安、脱抑制、易刺激性/不安定性のスコアが高い。治験中止後の疾患進行によるものか、あるいは評価時の状況や評価自体の妥当性に問題があった可能性も考慮される。この急激な悪化について、臨床的な背景を確認する必要がある。
        *   **根拠:** 有効性評価（副次評価項目）の信頼性に関わる。また、患者の状態が急激に悪化した可能性があり、医学的なフォローアップが必要か確認する必要がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'BASELINE', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 2
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'WEEK 2', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 45
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM01S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 12
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM03S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 8
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM04S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 3
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM05S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 6
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM08S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 12
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM09S', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4

    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Study Day 11)の血液検査で、MCV高値(101 fL, 基準値上限100)、RBC低値(3.70 TI/L, 基準値下限3.9)、Anisocytes異常(1)が認められた。Screening時もRBCは低値(3.80)であった。大球性貧血の可能性が考えられるが、Screening時のビタミンB12は基準値内であった（葉酸データはなし）。これらの検査値異常の臨床的意義と原因について評価が必要である。
        *   **根拠:** 貧血は患者の全身状態やQOLに影響を与える可能性があり、原因によっては治療介入が必要となる。治験薬との関連も評価する必要がある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Visit Name(LB.VISIT)] = 'WEEK 2', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Visit Name(LB.VISIT)] = 'WEEK 2', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.7, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Visit Name(LB.VISIT)] = 'WEEK 2', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '1', [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Visit Name(LB.VISIT)] = 'SCREENING 1', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.8, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Visit Name(LB.VISIT)] = 'SCREENING 1', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 388.8206, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'

    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「MICTURITION URGENCY」(尿意切迫, Mild)が治験薬投与開始日(Day 1)に発現し、治験中止時(Day 11)まで回復していない。Xanomelineはコリン作動薬であり、尿意切迫は既知のクラス副作用として考えられる。重症度はMildであり、中止理由とはなっていないため、医学的な緊急性は低いと考えられる。
        *   **根拠:** 治験薬の既知の薬理作用と一致する可能性のある有害事象であり、安全性プロファイルの評価において考慮すべき情報である。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY' (AESEQ=6)
            *   [Severity/Intensity(AE.AESEV)] = 'MILD' (AESEQ=6)
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-07' (AESEQ=6)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AESEQ=6)
            *   [TREATMENT EMERGENT FLAG(SUPPAE.QVAL)] = 'Y' (AESEQ=6)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** RELRECデータにより、中止理由(DS#1 'ADVERSE EVENT')とAE#7 'ARTHRALGIA'が関連付けられている。しかし、AE#8 'CELLULITIS'もAE#7と同時期(Day 7)に発現しており、重症度も同じ(Moderate)であるため、こちらも中止に関与した可能性がある。中止理由となったAEがどちらか、あるいは両方なのか明確にする必要がある。
        *   **根拠:** 中止理由の正確な特定は、安全性評価の正確性に不可欠である。
        *   **関連データ:**
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16' (AE#7とDS#1を関連付け)
            *   [Sequence Number(AE.AESEQ)] = 7, [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-13'
            *   [Sequence Number(AE.AESEQ)] = 8, [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-13'
            *   [Sequence Number(DS.DSSEQ)] = 1, [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-09-17'

    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** Retrieval Visit (Day 169)で評価されたNPI-X Totalスコアが45と著しく高い。Baseline (2) やWeek 2 (1) と比較して急激な悪化であり、データの入力ミスや評価エラーの可能性も否定できない。あるいは、患者の状態が実際に急激に悪化した可能性もある。データの妥当性を確認する必要がある。
        *   **根拠:** 有効性評価データの信頼性に関わる。異常な値は、データエラーまたは臨床的に重要な変化を示唆する可能性がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'RETRIEVAL', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 45
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'BASELINE', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 2
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Name(QS.VISIT)] = 'WEEK 2', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1

    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11)の血液検査で、MCV高値、RBC低値、Anisocytes異常が報告されている。これらの異常値が臨床的に意味を持つ可能性があるため（医学的レビューM-4参照）、データ入力エラーでないことを確認する必要がある。
        *   **根拠:** 異常値はデータエラーまたは医学的に重要な所見の可能性があるため、確認が必要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Visit Name(LB.VISIT)] = 'WEEK 2', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Visit Name(LB.VISIT)] = 'WEEK 2', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.7, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Visit Name(LB.VISIT)] = 'WEEK 2', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '1', [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL'

    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 併用薬としてHYDROCORTISONE, TOPICALが2012-09-02から2012-09-04まで使用されている。これは治験薬開始前であり、同時期に発現したAE#1(ERYTHEMA), AE#2(PRURITUS)の治療目的と考えられる。プロトコル3.6.2では治験薬貼付部位への塗布が指示されているが、それとは異なる使用目的・時期である。
        *   **根拠:** データの背景を理解するために記録しておくべき情報。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2012-09-02'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2012-09-04'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA' (AESEQ=1), [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-02', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS' (AESEQ=2), [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-02', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬HYDROCORTISONE, TOPICALの使用が、プロトコル3.6.2で指示された治験薬貼付前の使用とは異なる目的・時期で行われている可能性がある。ただし、治験薬開始前のAE治療目的であれば許容される可能性が高い。
        *   **プロトコル該当箇所:** Section 3.6.2 TTS Administration Procedures
        *   **根拠:** プロトコルで規定された手順との差異がある可能性があるが、臨床的な妥当性は高いと考えられる。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2012-09-02'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2012-09-04'

    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 既往歴としてEating Disorderが2009年に報告されている。プロトコル除外基準[14]では「A history within the last 5 years of ... Ethanol or psychoactive drug abuse or dependence」を除外としている。Eating Disorderがこれに該当するかは不明確だが、5年以内の精神疾患歴として確認が必要かもしれない。ただし、他の精神疾患（統合失調症、双極性障害）は明記されているがEating Disorderは明記されていない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [14]
        *   **根拠:** 除外基準に抵触する可能性がゼロではないが、明記されていないため逸脱とは断定できない。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0702'
            *   [Dictionary-Derived Term(MH.MHDECOD)] = 'EATING DISORDER'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'

    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル3.10.1では、治験中止時に用量を漸減する（25cm2パッチを除去し、50cm2パッチを中止visitまで継続する）よう指示されている。本症例はStudy Day 11に中止となっているが、この漸減投与が適切に実施されたかデータからは不明である。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** プロトコルで規定された中止手順の遵守は、安全性確保のために重要である。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-09-17' (Day 11)
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2012-09-16' (Day 10)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1, P-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11に有害事象により治験中止となっています。中止理由として報告された有害事象名「ARTHRALGIA」と関連付けられていますが、同時期に有害事象名「CELLULITIS」も発現しています。中止の判断に至った具体的な理由と経緯、および関連した有害事象について詳細をご教示ください。また、プロトコル3.10.1に記載されている中止時の治験薬漸減投与（25cm2パッチの除去）は実施されましたでしょうか。ご確認をお願いいたします。
        *   **クエリ文面（英語）:** The subject discontinued the study on Study Day 11 due to an adverse event. The AE Term 'ARTHRALGIA' is linked as the reason. However, the AE Term 'CELLULITIS' also occurred around the same time. Please provide details on the specific reason(s) and circumstances leading to discontinuation. Also, please confirm if the dose tapering procedure at discontinuation (removal of the 25cm2 patch) described in protocol section 3.10.1 was performed.
        *   **判断理由:** 中止理由の正確な特定と中止手順の遵守確認は、安全性評価の信頼性確保とGCP遵守の観点から必要であるため。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='ADVERSE EVENT', DS.DSSTDTC='2012-09-17', AE.AETERM='ARTHRALGIA'(AESEQ=7), AE.AETERM='CELLULITIS'(AESEQ=8), RELREC.RELID='01-701-1111-E16'
            *   関連するプロトコル箇所: Protocol Section 3.10.1, 3.9.3.2.1
            *   関連する医学的知見: 有害事象による中止理由の特定、プロトコル遵守

    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Week 2 (Study Day 11)のバイタルサイン測定にて、臥位の収縮期血圧が「125 mmHg」、立位3分後の収縮期血圧が「110 mmHg」と記録されており、起立性低血圧の可能性が示唆されます。この血圧変動について、臨床的な意義（症状の有無など）および治験薬との関連性について評価をお願いいたします。
        *   **クエリ文面（英語）:** On Week 2 (Study Day 11), Vital Signs show Supine Systolic Blood Pressure was '125 mmHg' and Standing Systolic Blood Pressure after 3 minutes was '110 mmHg', suggesting possible orthostatic hypotension. Please assess the clinical significance (e.g., presence of symptoms) and the relationship to the study drug.
        *   **判断理由:** 起立性低血圧は転倒・失神リスクを高める可能性があり、治験薬との関連も含め参加者の安全性を確保するために評価が必要なため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='SYSBP', VS.VISIT='WEEK 2', VS.VSPOS='SUPINE', VS.VSSTRESN=125; VS.VSTESTCD='SYSBP', VS.VISIT='WEEK 2', VS.VSPOS='STANDING', VS.VSTPT='AFTER STANDING FOR 3 MINUTES', VS.VSSTRESN=110
            *   関連するプロトコル箇所: Protocol Section 3.9.3.4.1, 3.4.2.2 [15], [17]
            *   関連する医学的知見: コリン作動薬の副作用（起立性低血圧、失神）、高齢者の転倒リスク

    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Retrieval Visit (Study Day 169)にて評価されたNPI-X (9) Total Scoreが「45」と、Baseline (2) やWeek 2 (1) と比較して著しく悪化しています。この評価結果は、患者様の状態を正確に反映したものか、あるいは評価時の状況やデータ入力等に影響する要因がなかったか、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** At the Retrieval Visit (Study Day 169), the NPI-X (9) Total Score was '45', which is a significant worsening compared to Baseline (2) and Week 2 (1). Please confirm if this result accurately reflects the subject's condition and if there were any factors affecting the assessment or data entry.
        *   **判断理由:** 有効性評価データの信頼性を確認するとともに、患者の状態が急激に悪化した可能性について臨床的な背景を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD='NPTOT', QS.VISIT='RETRIEVAL', QS.QSSTRESN=45; QS.QSTESTCD='NPTOT', QS.VISIT='BASELINE', QS.QSSTRESN=2; QS.QSTESTCD='NPTOT', QS.VISIT='WEEK 2', QS.QSSTRESN=1
            *   関連するプロトコル箇所: Protocol Section 2.2 (Secondary Objectives), 4.3.1
            *   関連する医学的知見: アルツハイマー病の進行、精神症状の変動、評価尺度の信頼性

    *   **クエリNo.:** Q-4 (関連指摘No.: M-4, D-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Week 2 (Study Day 11)の血液検査にて、Ery. Mean Corpuscular Volumeが「101 fL」(基準値上限100)、Erythrocytesが「3.70 TI/L」(基準値下限3.9)、Anisocytesが「1」(異常)と報告されています。これらの検査値異常について、臨床的な意義および考えられる原因について評価をお願いいたします。
        *   **クエリ文面（英語）:** On Week 2 (Study Day 11), lab results show MCV '101 fL' (ULN 100), RBC '3.70 TI/L' (LLN 3.9), and Anisocytes '1' (Abnormal). Please assess the clinical significance and potential cause of these findings.
        *   **判断理由:** 貧血の可能性があり、参加者の健康状態および治験薬との関連を評価する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='MCV', LB.VISIT='WEEK 2', LB.LBSTRESN=101, LB.LBNRIND='HIGH'; LB.LBTESTCD='RBC', LB.VISIT='WEEK 2', LB.LBSTRESN=3.7, LB.LBNRIND='LOW'; LB.LBTESTCD='ANISO', LB.VISIT='WEEK 2', LB.LBSTRESC='1', LB.LBNRIND='ABNORMAL'
            *   関連するプロトコル箇所: Protocol Section 3.9.3.3
            *   関連する医学的知見: 貧血の診断と原因検索

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有害事象「MICTURITION URGENCY」が治験薬投与開始日に発現している。Xanomelineのコリン作動性副作用の可能性があり、安全性プロファイルの一部として記録する。重症度はMildであり、中止理由とはなっていないため、現時点での追加アクションは不要と判断。
        *   **判断理由:** 治験薬の既知の薬理作用と一致する可能性のある軽微な有害事象であり、安全性データベースへの記録で十分と判断したため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='MICTURITION URGENCY'(AESEQ=6), AE.AESEV='MILD', AE.AESTDTC='2012-09-07', SUPPAE.QVAL='Y'
            *   関連する医学的知見: コリン作動薬の副作用

    *   **確認事項No.:** I-2 (関連指摘No.: D-4, P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA, DM
        *   **疑義事項/確認内容:** 併用薬HYDROCORTISONE, TOPICALが治験薬開始前に使用されている。同時期のAE(ERYTHEMA, PRURITUS)の治療目的と考えられ、プロトコル3.6.2の指示とは異なるが臨床的に妥当な使用と判断される。プロトコル逸脱とはせず、内部記録とする。
        *   **判断理由:** 治験薬投与期間外の使用であり、AE治療という妥当な理由があるため、重大な問題とは判断しない。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='HYDROCORTISONE, TOPICAL', CM.CMSTDTC='2012-09-02', CM.CMENDTC='2012-09-04', AE#1, AE#2
            *   関連するプロトコル箇所: Protocol Section 3.6.2

    *   **確認事項No.:** I-3 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA, Medical Monitor
        *   **疑義事項/確認内容:** 既往歴として5年以内のEating Disorderが報告されている。プロトコル除外基準[14]では精神疾患として統合失調症、双極性障害、薬物乱用/依存を明記しているが、Eating Disorderは明記されていない。厳密には除外基準抵触の可能性を完全には否定できないが、明記されていないこと、他の基準を満たしていることから、逸脱とは判断せず内部記録とする。
        *   **判断理由:** プロトコル上の記載が不明確であり、他の基準は満たしているため、現時点では逸脱とせず記録に留める。
        *   **判断根拠:**
            *   関連するデータ: MH.MHDECOD='EATING DISORDER', MH.MHSTDTC='2009'
            *   関連するプロトコル箇所: Protocol Section 3.4.2.2 [14]