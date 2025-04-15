# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 77歳、性別は男性、人種は白色人種、民族はヒスパニックまたはラテン系ではない。教育レベルは12年。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2011年03月27日|N/A|既往歴: アルツハイマー病 発症|
|2000年05月15日|N/A|既往歴: 心筋梗塞 発症|
|2006年12月16日|N/A|既往歴: 冠動脈バイパス術 (Triple Vessel Bypass Graft)|
|2013年09月20日|Day -16 (Screening 1)|既往歴: 心疾患 (MILD), 性欲亢進 (MILD), ST上昇 (MILD), ST低下 (MILD), 期外収縮 (MILD)。MMSEスコア: 21。Hachinskiスコア: 0。クレアチニン: 1.8 mg/dL (High)。併用薬: アスピリン 81mg QD (2000年より継続)。|
|2013年09月27日|Day -9 (Screening 2)|特記事項なし。|
|2013年10月06日|Day 1 (Baseline)|治験薬 Xanomeline 54mg Patch QD 開始。ADAS-Cog(11) Total Score: 27。NPI-X Total Score: 61 (妄想, 焦燥/攻撃性, 抑うつ/不快気分, 不安, 無感情/無関心, 過敏性/不安定性,異常な運動行為がベースラインで存在)。併用薬: Premarin 0.625mg QOD 開始。|
|2013年10月19日|Day 14 (Week 2)|有害事象: 心筋梗塞 (Mild, 治験薬中止, 因果関係なし) 発現 (Day 14-45)。心室中隔欠損症 (Mild, 因果関係なし) 発現 (Day 14-)。脳梗塞後遺症 (Severe, 因果関係なし) 発現 (Day 14-44)。BUN: 29 mg/dL (High)。アルブミン: 3.3 g/dL (Low)。立位血圧低下傾向 (106/58 mmHg)。NPI-X Total Score: 22 (ベースラインから改善)。|
|2013年10月20日|Day 15|治験薬 Xanomeline 81mg Patch QD へ増量。|
|2013年10月29日|Day 24|併用薬: Premarin 0.625mg QOD 終了。|
|2013年11月01日|Day 27 (Week 4 Lab)|Disposition: FINAL LAB VISIT (Other Event)。アルブミン: 3.4 g/dL (Low)。|
|2013年11月05日|Day 31|有害事象: 発疹 (Mild, 因果関係Probable) 発現 (Day 31-48)。そう痒症 (Mild, 因果関係Probable) 発現 (Day 31-48)。|
|2013年11月06日|Day 32|併用薬: Hydrocortisone, topical 開始 (発疹/そう痒症の治療目的か)。|
|2013年11月09日|Day 35 (Week 4)|NPI-X Total Score: 38 (Week 2から一部悪化)。立位血圧低下傾向 (110/60 mmHg)。|
|2013年11月18日|Day 44|治験薬 Xanomeline 81mg Patch QD 終了。有害事象: 脳死 (Severe, 因果関係なし) 発現・回復 (Day 44)。脳梗塞後遺症 終了 (Day 44)。|
|2013年11月19日|Day 45|有害事象: 心筋梗塞 回復 (Day 45)。|
|2013年11月22日|Day 48|有害事象: 発疹 回復 (Day 48)。そう痒症 回復 (Day 48)。併用薬: Hydrocortisone, topical 終了。|
|2013年11月24日|Day 50 (Week 6)|ADAS-Cog(11) Total Score: 30 (ベースラインから悪化)。CIBIC+ Score: 4 (No Change)。NPI-X Total Score: 16 (Week 4から改善、幻覚が新たに出現)。立位血圧低下傾向 (114/60 mmHg)。Disposition: ADVERSE EVENT (有害事象による中止)。|
|2013年12月06日|Day 62 (AE Follow-up)|試験参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「心筋梗塞」が重症度Mildと評価されているにも関わらず、治験薬中止(AEACN=DRUG WITHDRAWN)の措置が取られています。また、治験薬との因果関係は「なし」(AEREL=NONE)と評価されていますが、発症時期(Day 14)は治験薬投与期間中であり、Xanomeline（ムスカリン作動薬）の心血管系への影響（徐脈、血圧低下など）を考慮すると、因果関係の評価は慎重に行う必要があります。特に本症例は心筋梗塞や冠動脈バイパス術の既往があり、リスクが高いと考えられます。重症度評価、因果関係評価、および治験薬中止の判断根拠について医学的な妥当性の確認が必要です。
        *   **根拠:** 心筋梗塞は重篤なイベントであり、治験薬の安全性プロファイル評価において重要。ムスカリン作動薬の既知の心血管系への影響。患者の心血管系既往歴。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 14
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 45
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'MYOCARDIAL INFARCTION', 'CARDIAC DISORDER', 'TRIPLE VESSEL BYPASS GRAFT', etc.
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 有害事象として「心室中隔欠損症」(Ventricular Septal Defect)が報告されています。これは通常先天性疾患であり、治験薬との関連なし(AEREL=NONE)の評価は妥当と考えられます。しかし、Medical History (MH)ドメインに対応する記載がありません。既往歴として把握されていたか確認が必要です。
        *   **根拠:** VSDは通常先天性であり、AEではなくMHに記録されるべき情報。データの完全性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   [Sequence Number(AE.AESEQ)] = 2
            *   [Causality(AE.AEREL)] = 'NONE'
            *   MHドメイン全体
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「脳梗塞後遺症」(Late effects of cerebral infarction)が重症度Severeで報告されています。発症時期(Day 14)は治験薬投与期間中ですが、因果関係は「なし」(AEREL=NONE)と評価されています。Medical History (MH)ドメインには脳梗塞の明確な既往歴がなく、Hachinskiスコアも0です。スクリーニング前の脳梗塞の有無、本AEの診断根拠、および因果関係評価の妥当性について確認が必要です。
        *   **根拠:** 重症度Severeの神経学的イベントであり、安全性評価上重要。MHとの不整合。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   [Sequence Number(AE.AESEQ)] = 4
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 14
            *   MHドメイン全体
            *   [Question Short Name(QS.QSTESTCD)] = 'MHITM10' (History of Strokes), [Character Result/Finding in Std Format(QS.QSSTRESC)] = '0'
    *   **指摘No.:** M-4
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死」(Brain Death)が重症度Severeで報告されています。発症日(Day 44)は治験薬投与終了日と同日であり、転帰はResolvedとなっていますが、「脳死」の転帰がResolvedというのは医学的に考えにくいです。診断の経緯、転帰の詳細、および因果関係評価(AEREL=NONE)の妥当性について確認が必要です。先行する心筋梗塞や脳梗塞後遺症との関連も考慮する必要があります。
        *   **根拠:** 「脳死」は極めて重篤なイベントであり、その診断と転帰の記録は正確である必要がある。Resolvedという転帰は通常ありえない。治験薬との関連評価も重要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 44
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 44
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** スクリーニング時にクレアチニン高値(1.8 mg/dL)、Week 2にBUN高値(29 mg/dL)、Week 2およびWeek 4にアルブミン低値(3.3, 3.4 g/dL)が認められています。これらは軽度の腎機能低下や低栄養状態を示唆する可能性がありますが、高齢者やアルツハイマー病患者ではしばしば見られる所見でもあります。MHに腎疾患や低栄養の記載はありません。これらの検査値異常の臨床的意義について、他の所見と合わせて評価が必要です。
        *   **根拠:** 検査値異常の臨床的意義の評価。潜在的な合併症の可能性。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 159.12, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Baseline Flag(LB.LBBLFL)] = 'Y'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 10.353, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 14
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 33, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 14
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 34, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 27
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** ベースラインおよび治験薬投与期間を通じて、立位での血圧低下傾向（起立性低血圧の可能性）が認められます (例: Day 1 Supine 144/70 -> Standing 120/66, Day 14 Standing 104/56)。Xanomelineは心血管系への影響が知られており、心血管系既往歴のある本症例では特に注意が必要です。失神などのリスク評価が必要です。
        *   **根拠:** 起立性低血圧は転倒や失神のリスクを高める。治験薬の作用機序と患者背景（心血管既往）からリスクが高い。
        *   **関連データ:**
            *   VSドメインの血圧データ (SYSBP, DIABP) 全般 (特にVSPOS='SUPINE' vs 'STANDING')
            *   MHドメインの心血管系既往歴
    *   **指摘No.:** M-7
        *   **重要度:** Critical
        *   **内容:** Dispositionドメイン(DS)によると、本症例はDay 50に「ADVERSE EVENT」を理由に試験を中止しています。しかし、AEドメインの記録からは、どの有害事象が直接の中止理由となったのか特定できません（心筋梗塞、脳梗塞後遺症、脳死など複数の重篤なイベントが発生）。中止に至った具体的な有害事象とその評価について明確にする必要があります。
        *   **根拠:** 試験中止理由は安全性評価において極めて重要。中止理由の特定ができないと、治験薬の安全性プロファイルを正確に評価できない。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
            *   AEドメイン全体 (特にAESEQ=1, 3, 4)
    *   **指摘No.:** M-8
        *   **重要度:** Major
        *   **内容:** 有効性評価において、主要評価項目であるADAS-Cog(11)はベースラインから悪化(27→30)、CIBIC+は変化なし(Score 4)であったのに対し、副次評価項目であるNPI-X合計スコアはベースラインから改善傾向(61→16)を示しています。有効性評価指標間で結果に乖離が見られます。NPI-Xの改善は認められるものの、認知機能や全般的な臨床状態の改善は見られず、むしろ悪化しています。重篤な安全性イベントも考慮すると、本症例における治験薬のベネフィット・リスクバランスは不良であった可能性が高いです。
        *   **根拠:** 試験の主要目的（有効性評価）に対する結果の解釈。異なる評価指標間の結果の一貫性。安全性情報との統合的な評価。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 27 (Day 1), 30 (Day 50)
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4 (Day 50)
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 61 (Day 1), 22 (Day 14), 38 (Day 35), 16 (Day 50)
            *   AEドメイン全体

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** AE「心筋梗塞」(AESEQ=1)において、Action Taken with Study Treatment(AE.AEACN)が「DRUG WITHDRAWN」と記録されていますが、Exposure(EX)ドメインに対応する投与中断や中止の記録がありません。また、Disposition(DS)ドメインの中止理由AEの発生日(DSSTDY=50)とも時期が異なります(AEENDY=45)。実際の治験薬の投与状況（中止日）とAEACNの記録の整合性を確認する必要があります。
        *   **根拠:** 治験薬の曝露情報と安全性イベントの関連性を正確に評価するために、投与記録とAE記録の整合性が不可欠。評価の信頼性に影響。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1, [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN', [Study Day of End of Adverse Event(AE.AEENDY)] = 45
            *   EXドメイン全体
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** AEドメインで「心室中隔欠損症」(AESEQ=2)が報告されていますが、Medical History(MH)ドメインに対応する記載がありません。先天性疾患であり、通常MHに記録されるべき情報です。
        *   **根拠:** ドメイン間のデータ整合性。既往歴情報の完全性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   MHドメイン全体
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** AEドメインで「脳梗塞後遺症」(AESEQ=4)が報告されていますが、Medical History(MH)ドメインに脳梗塞の既往歴がありません。
        *   **根拠:** ドメイン間のデータ整合性。既往歴情報と有害事象報告の整合性。安全性評価の妥当性に影響。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   MHドメイン全体
    *   **指摘No.:** D-4
        *   **重要度:** Critical
        *   **内容:** Disposition(DS)ドメインで中止理由が「ADVERSE EVENT」(DSSTDY=50)と記録されていますが、AEドメインの記録からは、どの中止理由となったAE（心筋梗塞、脳死、脳梗塞後遺症など）を指すのか特定できません。AEの転帰日(AEENDY)もDSSTDY=50と一致しません。
        *   **根拠:** 中止理由の特定は安全性評価において極めて重要。ドメイン間の関連性が不明確。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
            *   AEドメイン全体 (特にAESEQ=1, 3, 4のAEENDY)
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** スクリーニング時の臨床検査(LB)でクレアチニン高値が認められましたが、Medical History(MH)ドメインに腎機能障害の記載がありません。
        *   **根拠:** ドメイン間のデータ整合性。検査値異常と既往歴の整合性。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Baseline Flag(LB.LBBLFL)] = 'Y'
            *   MHドメイン全体
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** Questionnaires(QS)ドメインのNPI-X評価において、Week 6 (Day 50)に幻覚(Hallucinations Score 1)が報告されていますが、AEドメインに対応する有害事象が報告されていません。NPI-Xで新たに検出された精神症状はAEとして報告されるべきか確認が必要です。
        *   **根拠:** ドメイン間のデータ整合性。有効性評価データと安全性（AE）報告の整合性。未報告AEの可能性。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM02S', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1, [Study Day of Finding(QS.QSDY)] = 50
            *   AEドメイン全体
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** Questionnaires(QS)ドメインのDAD評価において、一部の項目(DAITM04, 30, 31, 32)がベースライン(Day 1)でNA(Not Applicable, QSSTRESN=96)と評価されていますが、Week 6 (Day 50)ではN(No, QSSTRESN=0)と評価されています。ベースラインでNAと評価された理由が不明確です。
        *   **根拠:** データの一貫性。評価の妥当性。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM04', 'DAITM30', 'DAITM31', 'DAITM32'
            *   [Study Day of Finding(QS.QSDY)] = 1, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 96
            *   [Study Day of Finding(QS.QSDY)] = 50, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、「発疹」と「そう痒症」に関連する記録(AESEQ=5, 6, 7, 8)が複数存在し、AESPIDやRELRECでの関連付けが一貫していません。同一イベントに対する記録方法として適切か確認が必要です。
        *   **根拠:** ドメイン内データの一貫性。記録の標準化。
        *   **関連データ:**
            *   AEドメイン (AESEQ=5, 6, 7, 8)
            *   RELRECドメイン (RELID='01-704-1017-E11')
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** AE「発疹」(AESEQ=5, 7)および「そう痒症」(AESEQ=6, 8)について、終了日(AEENDTC='2013-11-22', AEENDY=48)は同一ですが、転帰(AEOUT)が「RECOVERED/RESOLVED」と「NOT RECOVERED/NOT RESOLVED」の両方で記録されています。記録の矛盾。
        *   **根拠:** ドメイン内データの一貫性。論理的な矛盾。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 5, [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [Study Day of End of Adverse Event(AE.AEENDY)] = 48
            *   [Sequence Number(AE.AESEQ)] = 7, [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Study Day of End of Adverse Event(AE.AEENDY)] = 48
            *   [Sequence Number(AE.AESEQ)] = 6, [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [Study Day of End of Adverse Event(AE.AEENDY)] = 48
            *   [Sequence Number(AE.AESEQ)] = 8, [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Study Day of End of Adverse Event(AE.AEENDY)] = 48
    *   **指摘No.:** D-10
        *   **重要度:** Minor
        *   **内容:** Concomitant Medications(CM)ドメインの「HYDROCORTISONE, TOPICAL」(CMSEQ=9, 11, 13)について、Standardized Medication Name(CM.CMDECOD)およびMedication Class(CM.CMCLAS)が「UNCODED」となっています。標準辞書でのコーディングが必要です。
        *   **根拠:** データの標準化。データ品質。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [Medication Class(CM.CMCLAS)] = 'UNCODED'
    *   **指摘No.:** D-11
        *   **重要度:** Minor
        *   **内容:** Questionnaires(QS)ドメインのNPI-X評価において、「食欲/摂食変化」(NPITM12)の記録に一貫性がありません。ベースライン(Day 1)ではFrequency(F)が欠損、Week 2(Day 14)ではSeverity(V)/Distress(D)が欠損、Week 6(Day 50)ではFrequency(F)が欠損しています。
        *   **根拠:** ドメイン内データの一貫性。評価データの完全性。
        *   **関連データ:**
            *   QSドメイン (QSTESTCD='NPITM12F', 'NPITM12V', 'NPITM12D')
    *   **指摘No.:** D-12
        *   **重要度:** Minor
        *   **内容:** Questionnaires(QS)ドメインのNPI-X評価において、「夜間行動」(NPITM11)のスコア(S)がベースライン(Day 1)、Week 4(Day 35)、Week 6(Day 50)でいずれも0と記録されていますが、同評価時点でのFrequency(F)やSeverity(V)は0でない値が記録されています。スコアは Frequency * Severity で計算されるため、記録に矛盾があります。
        *   **根拠:** ドメイン内データの一貫性。計算結果と元データの整合性。評価の信頼性。
        *   **関連データ:**
            *   QSドメイン (QSTESTCD='NPITM11F', 'NPITM11V', 'NPITM11S')
    *   **指摘No.:** D-13
        *   **重要度:** Minor
        *   **内容:** Questionnaires(QS)ドメインのNPI-X評価において、「食欲/摂食変化」(NPITM12)のスコア(S)がベースライン(Day 1)、Week 2(Day 14)でいずれも0と記録されていますが、同評価時点でのFrequency(F)やSeverity(V)は0でない値が記録されています（例: Baseline Severity=1）。スコアは Frequency * Severity で計算されるため、記録に矛盾があります。
        *   **根拠:** ドメイン内データの一貫性。計算結果と元データの整合性。評価の信頼性。
        *   **関連データ:**
            *   QSドメイン (QSTESTCD='NPITM12F', 'NPITM12V', 'NPITM12S')
    *   **指摘No.:** D-14
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、MedDRAコーディング関連変数（AELLT, AELLTCD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCD）の多くが欠損しています。コーディングが未完了である可能性があります。
        *   **根拠:** データの完全性。標準化。
        *   **関連データ:**
            *   AEドメイン全体
    *   **指摘No.:** D-15
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、MedDRAコーディング関連変数（MHLLT, MHDECOD, MHHLT, MHHLGT, MHBODSYS）の一部が欠損しています。コーディングが未完了である可能性があります。
        *   **根拠:** データの完全性。標準化。
        *   **関連データ:**
            *   MHドメイン全体

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[5]である「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施記録が確認できません。適格性確認が不十分である可能性があります。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 選択基準の遵守確認。適格性の担保。
        *   **関連データ:**
            *   該当データなし (確認が必要)
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **逸脱の可能性:** 選択基準[6]である同意取得の記録(DM.RFICDTC)が欠損しています。同意取得前に治験関連手順が開始された場合、重大なGCP違反となります。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [6], Section 5.1 Informed Consent
        *   **根拠:** 参加者の権利保護。GCP遵守。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b]の確認に必要なスクリーニング時のECG記録、およびプロトコル Section 3.9.3.4.2 で規定されている治験期間中のECG記録が確認できません。心血管系の安全性評価が不十分である可能性があります。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b], Section 3.9.3.4.2 Cardiovascular Safety Measures
        *   **根拠:** 除外基準の遵守確認。プロトコルで規定された安全性評価の実施。
        *   **関連データ:**
            *   該当データなし (確認が必要)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** MHに複数の心血管系既往（心筋梗塞 2000年、冠動脈バイパス術 2006年、他）が記録されています。除外基準[17]「A history within the last 5 years of a serious cardiovascular disorder」に該当しないかの確認が必要です。5年以上前のイベントであっても、現在の状態が「serious」と判断される場合は除外対象となる可能性があります。適格性評価の妥当性確認が必要です。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** 除外基準の遵守確認。参加者の安全性確保。
        *   **関連データ:**
            *   MHドメイン全体
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時のクレアチニン値が基準値上限を超えており(1.8 mg/dL)、除外基準[27b]に抵触する可能性があります。プロトコルでは臨床的に意義がないと判断されれば組み入れ可能とされていますが、その判断記録が確認できません。適格性評価の妥当性確認が必要です。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準の遵守確認。参加者の安全性確保。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Result or Finding in Original Units(LB.LBORRES)] = '1.8', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6', [Baseline Flag(LB.LBBLFL)] = 'Y'
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b]の確認に必要なFolateの検査データが欠損しています。適格性確認が不十分である可能性があります。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準の遵守確認。
        *   **関連データ:**
            *   LBドメイン (LBTESTCD='FOLATE'の記録なし)
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[29b]の確認に必要な梅毒スクリーニングの実施記録が確認できません。適格性確認が不十分である可能性があります。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 除外基準の遵守確認。
        *   **関連データ:**
            *   該当データなし (確認が必要)
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[31b] v)では、エストロゲン補充療法は投与量が3ヶ月以上安定している場合に限り許可されますが、本症例ではPremarinがDay 1から開始されており、この条件を満たしていない可能性があります。除外基準違反の可能性があります。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] v)
        *   **根拠:** 除外基準の遵守確認。併用薬規定の遵守。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1)
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** AE「心筋梗塞」発生時に治験薬が中止された(AEACN=DRUG WITHDRAWN)と記録されていますが、EXドメインに投与中止の記録がなく、DSドメインの中止日(Day 50)とも異なります。プロトコル逸脱（記録不備）の可能性があります。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations (中止時の記録)
        *   **根拠:** 治験薬投与記録の正確性。プロトコル遵守。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1, [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   EXドメイン全体
            *   DSドメイン全体
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルではVisit 7 (Week 6)以降も臨床検査（血液学、生化学）が規定されていますが、本症例ではVisit 5 (Day 27)以降の検査データがありません。特に中止時(Day 50)の検査が未実施であることは、安全性評価の観点から問題となる可能性があります。プロトコルからの逸脱（評価未実施）の可能性があります。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.3 Clinical Laboratory Tests
        *   **根拠:** プロトコルで規定された安全性評価の実施。
        *   **関連データ:**
            *   LBドメイン (Day 27以降のデータなし)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
    *   **指摘No.:** P-11
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルでは治験期間中に複数回のECG評価が規定されていますが（例: Visit 4, 5, 7など）、実施記録が確認できません。心血管系の安全性評価が不十分である可能性があります。プロトコルからの逸脱（評価未実施）の可能性があります。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.4.2 Cardiovascular Safety Measures
        *   **根拠:** プロトコルで規定された安全性評価の実施。
        *   **関連データ:**
            *   該当データなし (確認が必要)
    *   **指摘No.:** P-12
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルではVisit 2で24時間Ambulatory ECGの実施が規定されていますが、実施記録が確認できません。心血管系の安全性評価が不十分である可能性があります。プロトコルからの逸脱（評価未実施）の可能性があります。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.4.2 Cardiovascular Safety Measures
        *   **根拠:** プロトコルで規定された安全性評価の実施。
        *   **関連データ:**
            *   該当データなし (確認が必要)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-9, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「心筋梗塞」について、重症度が「MILD」と評価されているにも関わらず、治験薬中止の措置(Action Taken with Study Treatmentが「DRUG WITHDRAWN」)が取られています。また、治験薬との因果関係は「NONE」と評価されています。重症度評価、因果関係評価の根拠、および治験薬中止に至った判断の詳細についてご教示ください。加えて、Exposureドメインに治験薬の投与中止記録がありません。実際の最終投与日をご確認いただけますでしょうか。本患者は心血管系の既往歴があり、治験薬の安全性評価において重要な情報となります。
        *   **クエリ文面（英語）:** Regarding the AE 'MYOCARDIAL INFARCTION' (AESEQ=1), Severity is 'MILD' but Action Taken is 'DRUG WITHDRAWN' and Causality is 'NONE'. Please provide details on the rationale for severity/causality assessment and the decision to withdraw the drug. Also, EX domain lacks discontinuation record. Please confirm the actual last dose date. This information is crucial for safety assessment given the patient's cardiovascular history.
        *   **判断理由:** 重篤な有害事象の評価と治験薬中止判断の妥当性、および因果関係評価の妥当性を確認し、参加者の安全性評価の正確性を担保するため。また、治験薬曝露期間を正確に把握するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION', [Sequence Number(AE.AESEQ)] = 1, [Severity/Intensity(AE.AESEV)] = 'MILD', [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN', [Causality(AE.AEREL)] = 'NONE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 14, EXドメイン全体, MHドメイン全体
            *   関連するプロトコル箇所: Section 3.9.3.2 Adverse Events, Section 3.10.1 Discontinuations
            *   関連する医学的知見: 心筋梗塞の重症度評価、薬剤との因果関係評価、ムスカリン作動薬の心血管系への影響
    *   **クエリNo.:** Q-2 (関連指摘No.: M-4, D-4, M-7)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「脳死」がDay 44に報告され、転帰が「RECOVERED/RESOLVED」と記録されています。「脳死」からの回復は医学的に考えられません。診断の経緯（診断基準、評価内容）および実際の転帰について詳細をご確認ください。また、本症例はDay 50に有害事象を理由に試験を中止していますが、中止の直接的な原因となった有害事象（心筋梗塞、脳死、脳梗塞後遺症など）を特定し、ご教示ください。参加者の最終的な状態を正確に把握し、安全性を評価するために必要です。
        *   **クエリ文面（英語）:** AE 'BRAIN DEATH' (AESEQ=3) reported on Day 44 has Outcome 'RECOVERED/RESOLVED', which is medically implausible. Please confirm the diagnostic process and the actual outcome. Also, the subject discontinued due to AE on Day 50 (DS). Please specify which AE (e.g., MI, Brain Death, Cerebral Infarction) led to discontinuation. This is critical for accurate safety assessment.
        *   **判断理由:** 極めて重篤なイベントである「脳死」の診断と転帰記録の正確性を確認するため。また、試験中止理由を特定し、治験薬の安全性評価の信頼性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Sequence Number(AE.AESEQ)] = 3, [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED', [Study Day of Start/End of Adverse Event(AE.AESTDY/AEENDY)] = 44, [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 50
            *   関連する医学的知見: 脳死の定義と予後
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, D-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「脳梗塞後遺症」が重症度「SEVERE」で報告されていますが、Medical Historyドメインに脳梗塞の既往歴の記載がありません。スクリーニング前の脳梗塞の有無、および今回報告されたAEの診断根拠（画像所見など）についてご確認ください。治験期間中に発症したイベントであれば、因果関係評価(AEREL=NONE)の根拠も併せてご教示ください。
        *   **クエリ文面（英語）:** AE 'LATE EFFECTS OF CEREBRAL INFARCTION' (AESEQ=4, Severity=SEVERE) is reported, but no history of stroke is found in MH domain. Please confirm any pre-study stroke history and the diagnostic basis for this AE (e.g., imaging). If occurred during the study, please provide rationale for causality assessment (AEREL=NONE).
        *   **判断理由:** 重篤な神経学的イベントの診断根拠と既往歴との整合性を確認し、安全性評価の正確性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION', [Sequence Number(AE.AESEQ)] = 4, [Severity/Intensity(AE.AESEV)] = 'SEVERE', [Causality(AE.AEREL)] = 'NONE', MHドメイン全体
            *   関連する医学的知見: 脳梗塞の診断
    *   **クエリNo.:** Q-4 (関連指摘No.: M-2, D-2)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象として「心室中隔欠損症」が報告されていますが、Medical Historyドメインに対応する記載がありません。通常、先天性疾患は既往歴として記録されます。本件が既往歴として把握されていたか、またMedical Historyへの追記が必要かご確認ください。
        *   **クエリ文面（英語）:** AE 'VENTRICULAR SEPTAL DEFECT' (AESEQ=2) is reported, but not listed in MH domain. As this is typically a congenital condition, please confirm if it was known pre-study and if MH domain needs update.
        *   **判断理由:** データの完全性とドメイン間整合性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT', MHドメイン全体
            *   関連する医学的知見: VSDは通常先天性疾患
    *   **クエリNo.:** Q-5 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル選択基準[5]では、「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」が必要とされていますが、提供されたデータからは実施記録を確認できませんでした。スクリーニング時に本基準を満たしていたか、実施状況と結果（ADとの整合性）についてご確認ください。
        *   **クエリ文面（英語）:** Protocol inclusion criterion [5] requires 'CNS imaging compatible with AD within past 1 year'. We could not confirm its implementation from the provided data. Please confirm if this criterion was met at screening, including the date and result compatibility with AD.
        *   **判断理由:** 選択基準の遵守を確認し、被験者の適格性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: 該当データなし
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [5]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-2)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日(Date/Time of Informed Consent)が記録されていません。同意取得日をご確認の上、ご回答ください。同意取得前に治験関連手順が開始されていないか確認するために重要です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (RFICDTC) is missing in DM domain. Please confirm and provide the date. This is critical to ensure no study procedures were performed before consent was obtained.
        *   **判断理由:** 同意取得の事実と日付を確認し、参加者の権利保護とGCP遵守を担保するため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [6], Section 5.1 Informed Consent
    *   **クエリNo.:** Q-7 (関連指摘No.: P-3, P-11)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではスクリーニング時(除外基準[16b])および治験期間中(例: Visit 4, 5, 7)にECG評価が規定されていますが、提供されたデータからは実施記録を確認できませんでした。ECGの実施状況（実施日、各Visitでの実施有無）および結果（特に除外基準に該当する所見の有無）についてご確認ください。心血管系の安全性評価に不可欠な情報です。
        *   **クエリ文面（英語）:** Protocol requires ECG at screening (Exclusion [16b]) and during the study (e.g., Visits 4, 5, 7). We could not confirm implementation from the provided data. Please confirm ECG execution dates/visits and results, especially regarding findings listed in exclusion criteria. This is essential for cardiovascular safety assessment.
        *   **判断理由:** プロトコルで規定された重要な安全性評価（ECG）の実施状況を確認し、除外基準遵守と安全性監視の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: 該当データなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [16b], Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1
    *   **クエリNo.:** Q-8 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Medical Historyに複数の心血管系既往（心筋梗塞 2000年、冠動脈バイパス術 2006年など）が記録されています。プロトコル除外基準[17]「A history within the last 5 years of a serious cardiovascular disorder」に該当しないと判断された根拠について、詳細をご教示いただけますでしょうか。参加者の安全性確保の観点から確認が必要です。
        *   **クエリ文面（英語）:** MH domain lists multiple cardiovascular histories (e.g., MI in 2000, Bypass in 2006). Please provide the rationale for determining that the patient did not meet exclusion criterion [17] ('serious cardiovascular disorder within the last 5 years'). Confirmation is needed for patient safety.
        *   **判断理由:** 除外基準の適格性判断の根拠を確認し、リスクの高い参加者の安全性が確保されていたか検証するため。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン全体
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時のクレアチニン値が1.8 mg/dLであり、基準値上限(1.6 mg/dL)を超えています。これはプロトコル除外基準[27b]に抵触する可能性がありますが、被験者は組み入れられています。プロトコルでは臨床的に意義がない場合は組み入れ可能とされています。本件について臨床的に意義なしと判断された根拠（医師の評価コメントなど）についてご教示ください。
        *   **クエリ文面（英語）:** Screening Creatinine was 1.8 mg/dL (Ref High: 1.6 mg/dL), potentially meeting exclusion criterion [27b]. The protocol allows inclusion if deemed not clinically significant. Please provide the documented rationale for this assessment.
        *   **判断理由:** 除外基準に抵触する可能性のある検査値異常に対する適格性判断の根拠を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Result or Finding in Original Units(LB.LBORRES)] = '1.8', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6', [Baseline Flag(LB.LBBLFL)] = 'Y'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
    *   **クエリNo.:** Q-10 (関連指摘No.: P-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[28b]の確認に必要なFolateの検査結果がデータに含まれていません。スクリーニング時にFolate検査が実施されたかご確認ください。
        *   **クエリ文面（英語）:** Folate test result, required for exclusion criterion [28b], is missing from the data. Please confirm if the Folate test was performed at screening.
        *   **判断理由:** 除外基準の確認に必要な検査の実施状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='FOLATE'の記録なし)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]
    *   **クエリNo.:** Q-11 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[29b]の確認に必要な梅毒スクリーニングの実施記録がデータに含まれていません。スクリーニング時に梅毒スクリーニングが実施されたか、およびその結果をご確認ください。
        *   **クエリ文面（英語）:** Syphilis screening result, required for exclusion criterion [29b], is missing from the data. Please confirm if syphilis screening was performed and provide the result.
        *   **判断理由:** 除外基準の確認に必要な検査の実施状況と結果を確認するため。
        *   **判断根拠:**
            *   関連するデータ: 該当データなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [29b]
    *   **クエリNo.:** Q-12 (関連指摘No.: P-8)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬としてPremarin (エストロゲン)がDay 1から開始されています。プロトコル除外基準[31b] v)では、エストロゲン補充療法は投与量が3ヶ月以上安定している場合に限り許可されています。本症例がこの基準を満たしていたか（例えば、治験前から同用量で継続していたかなど）ご確認ください。満たしていない場合、除外基準違反となります。
        *   **クエリ文面（英語）:** Concomitant medication Premarin (estrogen) was started on Day 1. Protocol exclusion [31b] v) permits estrogen only if the dose has been stable for at least 3 months prior to enrollment. Please confirm if this criterion was met (e.g., continuation of stable dose from pre-study). If not, this is a potential protocol violation.
        *   **判断理由:** 除外基準および併用薬規定の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] v)
    *   **クエリNo.:** Q-13 (関連指摘No.: P-10)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではVisit 7 (Week 6)以降も臨床検査（血液学、生化学）の実施が規定されていますが、Visit 5 (Day 27)以降の検査データがありません。特に中止時(Day 50)の検査が重要となります。Visit 7以降の検査が実施されなかった理由をご確認ください。プロトコルからの逸脱（評価未実施）の可能性があります。
        *   **クエリ文面（英語）:** Protocol requires lab tests (Hematology, Chemistry) after Visit 5 (Day 27), including at discontinuation (Day 50). However, data after Day 27 is missing. Please clarify the reason why these tests were not performed, especially at the time of discontinuation. This is a potential deviation from the protocol schedule.
        *   **判断理由:** プロトコルで規定された安全性評価の実施状況を確認するため。中止時の安全性データ欠損は評価の信頼性に影響する。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (Day 27以降のデータなし), DSドメイン (DSSTDY=50)
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.3 Clinical Laboratory Tests
    *   **クエリNo.:** Q-14 (関連指摘No.: P-12)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではVisit 2で24時間Ambulatory ECGの実施が規定されていますが、提供されたデータからは実施記録を確認できませんでした。Ambulatory ECGの実施状況についてご確認ください。心血管系の安全性評価に重要な検査です。
        *   **クエリ文面（英語）:** Protocol requires a 24-hour Ambulatory ECG at Visit 2. We could not confirm its implementation from the provided data. Please confirm if the Ambulatory ECG was performed. This is an important cardiovascular safety assessment.
        *   **判断理由:** プロトコルで規定された重要な安全性評価の実施状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: 該当データなし
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 (Schedule of Events), Section 3.9.3.4.2 Cardiovascular Safety Measures
    *   **クエリNo.:** Q-15 (関連指摘No.: D-6)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Week 6 (Day 50)のNPI-X評価で幻覚(Hallucinations Score 1)が報告されていますが、AEドメインに対応する有害事象が報告されていません。NPI-Xで新たに確認された精神症状について、有害事象としての評価および報告が必要かご確認ください。
        *   **クエリ文面（英語）:** NPI-X at Week 6 (Day 50) shows Hallucinations (Score 1), but no corresponding AE is reported in the AE domain. Please assess if this newly identified symptom should be reported as an Adverse Event.
        *   **判断理由:** 未報告の有害事象の可能性を確認し、安全性データの完全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'NPITM02S', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1, [Study Day of Finding(QS.QSDY)] = 50, AEドメイン全体
            *   関連するプロトコル箇所: Section 3.9.3.2 Clinical Adverse Events
    *   **クエリNo.:** Q-16 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DAD評価において、一部の項目(DAITM04, 30, 31, 32)がベースライン(Day 1)でNA(Not Applicable)と評価されています。評価ができなかったのか、あるいは実際に適用外（例：過去に実施していなかった活動）だったのか、NAと評価された理由をご確認ください。
        *   **クエリ文面（英語）:** For DAD assessment, some items (DAITM04, 30, 31, 32) were marked NA (Not Applicable) at Baseline (Day 1). Please clarify the reason for the NA assessment (e.g., unable to assess, or activity genuinely not applicable to the subject historically).
        *   **判断理由:** 評価データの妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSTESTCD='DAITM04', 'DAITM30', 'DAITM31', 'DAITM32', QSDY=1, QSSTRESN=96)
    *   **クエリNo.:** Q-17 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「発疹」(AESEQ 5, 7)および「そう痒症」(AESEQ 6, 8)について、終了日は同一(Day 48)ですが、転帰(Outcome of Adverse Event)が「RECOVERED/RESOLVED」と「NOT RECOVERED/NOT RESOLVED」の両方で記録されています。正しい最終的な転帰をご確認の上、修正をお願いします。
        *   **クエリ文面（英語）:** For AE 'RASH' (AESEQ 5, 7) and 'PRURITUS' (AESEQ 6, 8), the end date (Day 48) is the same, but the Outcome (AEOUT) is recorded as both 'RECOVERED/RESOLVED' and 'NOT RECOVERED/NOT RESOLVED'. Please confirm the correct final outcome and revise the records accordingly.
        *   **判断理由:** データ内の矛盾を解消し、記録の正確性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=5, 6, 7, 8 の AEOUT, AEENDY)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5, D-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時のクレアチニン高値、Week 2のBUN高値、Week 2/4のアルブミン低値について、臨床的な意義と他のデータ（特に心血管系イベント、体重変化など）との関連性を内部で評価・記録する。MHに腎機能障害や低栄養の記載がない点も留意する。これらの異常値が治験薬の安全性や有効性評価に与える影響は限定的と考えられるため、医療機関への問い合わせは不要と判断。
        *   **判断理由:** 軽微な検査値異常であり、直ちに介入が必要なレベルではないため。内部での総合的な評価で十分と判断。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (CREAT, BUN, ALB), MHドメイン, VSドメイン (WEIGHT)
    *   **確認事項No.:** I-2 (関連指摘No.: M-6)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** ベースラインおよび治験期間を通じて起立性低血圧の傾向が認められる。心血管系既往歴のあるリスクの高い症例であり、治験薬（ムスカリン作動薬）の影響も考えられるため、失神等のリスクについて内部で評価し、記録する。ただし、具体的なAEとして失神は報告されておらず、血圧低下も著明ではないため、現時点での緊急クエリは不要と判断。
        *   **判断理由:** 失神等の具体的なイベントは発生していないが、潜在的なリスクとして認識し、内部評価を行う必要があるため。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (SYSBP, DIABP), MHドメイン
    *   **確認事項No.:** I-3 (関連指摘No.: M-8)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価指標間で結果に乖離（ADAS-Cog悪化 vs NPI-X改善）が見られる。症例の全体像（重篤な安全性イベントの発生、早期中止）を踏まえ、有効性の評価結果の解釈について内部で議論・考察し、記録する。個別のデータ修正を求めるものではないため、内部確認とする。
        *   **判断理由:** 評価指標間の乖離は臨床試験では起こりうることであり、データそのものの誤りというより解釈の問題であるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (ACTOT, CIBIC, NPTOT), AEドメイン, DSドメイン
    *   **確認事項No.:** I-4 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「発疹」「そう痒症」の記録方法（複数のAESEQ、異なるAESPID、一部のみRELRECで関連付け）に一貫性がない可能性がある。データマネジメント計画書（DMP）やコーディングガイドラインを確認し、同様のケースでの標準的な記録方法と比較検討する。データ解釈への影響は小さいと判断されるため内部確認とする。
        *   **判断理由:** データ解釈への影響は小さいと考えられる記録方法の問題であるため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=5, 6, 7, 8), RELRECドメイン
    *   **確認事項No.:** I-5 (関連指摘No.: D-10)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 併用薬「HYDROCORTISONE, TOPICAL」の標準化コーディング(CMDECOD, CMCLAS)が未実施("UNCODED")。標準辞書（例: WHODrug）を用いたコーディングが必要。データクリーニングプロセスの一環として対応する。
        *   **判断理由:** データ標準化に関する問題であり、内部のデータマネジメントプロセスで対応可能なため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='HYDROCORTISONE, TOPICAL', CMDECOD='UNCODED', CMCLAS='UNCODED')
    *   **確認事項No.:** I-6 (関連指摘No.: D-11, D-12, D-13)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** NPI-Xの一部の項目（食欲/摂食変化、夜間行動）で、Frequency/Severity/Distressの欠損や、Score計算の矛盾が見られる。データ入力規則やプログラミングされたスコア計算ロジックを確認し、データの正確性を検証する。必要に応じて修正を行う。評価全体への影響は限定的と考えられるため内部確認とする。
        *   **判断理由:** データ入力または計算ロジックの問題と考えられ、内部で検証・修正が可能であるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSTESTCD='NPITM11F', 'NPITM11V', 'NPITM11S', 'NPITM12F', 'NPITM12V', 'NPITM12D', 'NPITM12S')
    *   **確認事項No.:** I-7 (関連指摘No.: D-14, D-15)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインおよびMHドメインにおいて、MedDRAコーディング関連変数の多くが欠損している。コーディングプロセスが完了しているか、あるいは遅延しているか状況を確認する。データクリーニングプロセスの一環として対応する。
        *   **判断理由:** コーディングの進捗状況確認であり、内部プロセスで対応可能なため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン, MHドメインのコーディング関連変数

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 64歳、性別は男性、人種はWHITE、民族はNOT HISPANIC OR LATINO、治験参加国はUSA、割り付けられた治験群（計画）はPlacebo、実際の治験群はPlaceboである。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65 (Visit 1)|アラニンアミノトランスフェラーゼが「135」(U/L) で基準値上限(43 U/L)を超過 (HIGH)。アスパラギン酸アミノトランスフェラーゼが「145」(U/L) で基準値上限(36 U/L)を超過 (HIGH)。 (Screening時の肝酵素上昇)|
|2013年02月21日|Day -9 (Visit 1.1)|アラニンアミノトランスフェラーゼが「19」(U/L) で基準値内 (NORMAL)。アスパラギン酸アミノトランスフェラーゼが「29」(U/L) で基準値内 (NORMAL)。 (肝酵素正常化)|
|2013年02月21日|Day -9 (Visit 1.1)|ナトリウムが「133」(mmol/L) で基準値下限(135 mmol/L)未満 (LOW)。 (一過性の軽度低ナトリウム血症)|
|2013年02月23日|Day -7 (Visit 1)|既往歴としてアルツハイマー病 (Primary Diagnosis, 2008年発症)、肺気腫 (軽度)、冠動脈疾患 (軽度)、関節炎 (軽度) が報告された。肺膿瘍ドレナージ (1997年)、腸ポリープ切除術 (2009年) の既往あり。|
|2013年02月23日|Day -7 (Visit 1)|Mini-Mental State Examination (MMSE) の合計スコアが「23」。Modified Hachinski Ischemic Scoreの合計スコアが「1」。|
|2013年03月02日|Day 1 (Visit 3)|治験薬 (Placebo) 投与開始。|
|2013年03月02日|Day 1 (Visit 3)|ADAS-Cog(11) Subscoreが「14」(Baseline)。NPI-X (9) Total Scoreが「3」(Baseline)。|
|2013年03月04日|Day 3|有害事象「DIARRHOEA」(軽度, 治験薬との関連の可能性: POSSIBLE) 発現。|
|2013年03月05日|Day 4|有害事象「DIARRHOEA」回復。|
|2013年03月05日|Day 4|有害事象「INSOMNIA」(軽度, 治験薬との関連の可能性: REMOTE) 発現。併用薬「KAOPECTATE」開始 (Diarrhoea治療目的か)。|
|2013年03月06日|Day 5|有害事象「INSOMNIA」回復。併用薬「KAOPECTATE」終了。|
|2013年03月14日|Day 13 (Visit 4)|NPI-X (9) Total Scoreが「6」。|
|2013年03月28日|Day 27 (Visit 5)|赤血球平均容積 (MCV) が「101」(fL) で基準値上限(100 fL)を超過 (HIGH)。Anisocytesが「1」(ABNORMAL)。ナトリウムが「146」(mmol/L) で基準値上限(145 mmol/L)を超過 (HIGH)。 (一過性の検査値異常)|
|2013年03月28日|Day 27 (Visit 5)|NPI-X (9) Total Scoreが「4」。|
|2013年04月13日|Day 43 (Visit 7)|NPI-X (9) Total Scoreが「3」。|
|2013年04月27日|Day 57 (Visit 8)|ADAS-Cog(11) Subscoreが「9」。|
|2013年05月11日|Day 71 (Visit 8.1)|NPI-X (9) Total Scoreが「4」。|
|2013年05月25日|Day 85 (Visit 9)|NPI-X (9) Total Scoreが「6」。|
|2013年06月08日|Day 99 (Visit 9.1)|NPI-X (9) Total Scoreが「6」。|
|2013年06月22日|Day 113 (Visit 10)|ADAS-Cog(11) Subscoreが「7」。Clinician's Interview-Based Impression of Change (CIBIC+) が「4」(No Change)。Disability Assessment for Dementia (DAD) の項目「PREPARE OR COOK A LIGHT MEAL OR A SNACK」が「N」(0) に変化。|
|2013年06月22日|Day 113 (Visit 10)|NPI-X (9) Total Scoreが「4」。|
|2013年07月06日|Day 127 (Visit 10.1)|NPI-X (9) Total Scoreが「4」。|
|2013年07月20日|Day 141 (Visit 11)|NPI-X (9) Total Scoreが「4」。|
|2013年08月03日|Day 155 (Visit 11.1)|NPI-X (9) Total Scoreが「3」。|
|2013年08月09日|Day 161 (Visit 12)|ADAS-Cog(11) Subscoreが「9」。Clinician's Interview-Based Impression of Change (CIBIC+) が「4」(No Change)。Disability Assessment for Dementia (DAD) の複数項目に変化あり (改善・悪化混在)。|
|2013年08月09日|Day 161 (Visit 12)|NPI-X (9) Total Scoreが「2」。|
|2013年08月31日|Day 183 (Visit 13)|アスパラギン酸アミノトランスフェラーゼが「38」(U/L) で基準値上限(36 U/L)を超過 (HIGH)。 (軽度のAST上昇)|
|2013年08月31日|Day 183 (Visit 13)|NPI-X (9) Total Scoreが「2」。|
|2013年08月31日|Day 183 (Visit 13)|Disposition Eventとして「COMPLETED」および「FINAL LAB VISIT」が記録された。治験終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   指摘事項なし

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 同意取得日時の記録が欠損している。治験開始前に適切な同意が得られていたか確認できない。これは参加者の権利保護とGCP遵守の観点から重要な問題である。
        *   **根拠:** プロトコル5.1では治験手順開始前のインフォームド・コンセント取得が必須とされている。DMドメインのRFICDTCが欠損している。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「DIARRHOEA」の開始日と、その治療薬と考えられる「KAOPECTATE」の開始日に1日のずれがある。臨床的にはあり得るが、記録の正確性について確認が望ましい。
        *   **根拠:** AEの開始日と関連する治療薬の開始日は通常近接している、あるいは一致することが期待される。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-03-04'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 3
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'KAOPECTATE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-05'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 4
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 既往歴として「ARTHRITIS」が報告されているが、関連する併用薬（鎮痛薬など）の記録がない。関節炎に対する治療が行われていなかったのか、あるいは報告漏れか確認が必要。
        *   **根拠:** 関節炎は通常、症状緩和のための薬剤使用を伴うことがある。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS'
            *   CMドメインに関連薬剤の記録なし
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 各ドメインの測定日/実施日 (--DY) と対応するVisitの計画日 (VISITDY) に1日のずれが見られる箇所がある。これは実際の測定日と計画日のずれであり、臨床的に大きな問題はないと考えられるが、一貫性の観点から留意すべき点である。
        *   **根拠:** データの一貫性チェック。
        *   **関連データ:**
            *   例: [Study Day of Vital Signs(VS.VSDY)] = 13, [Planned Study Day of Visit(VS.VISITDY)] = 14 (Visit 4)
            *   例: [Study Day of Finding(QS.QSDY)] = 57, [Planned Study Day of Visit(QS.VISITDY)] = 56 (Visit 8)
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** MH, CM, AEドメインにおいて、コーディング関連変数（例: MHDECOD, CMDECOD, AELLT, AEDECOD）が一部欠損している。データコーディングが未完了である可能性があり、最終的なデータ品質に影響する可能性がある。
        *   **根拠:** データ完全性のチェック。
        *   **関連データ:**
            *   MHドメインのMHDECOD, MHLLTなど
            *   CMドメインのCMDECOD, CMCLAS ('UNCODED')
            *   AEドメインのAELLT, AEDECODなど
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、一部の既往歴の開始日 (MHSTDTC) が年のみ、または欠損している。正確な発症時期が不明である。
        *   **根拠:** データ完全性のチェック。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'EMPHYSEMA', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'LUNG ABSCESS DRAINAGE', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '1997'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'INTESTINAL POLYPECTOMY', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[5]である「過去1年以内のADに合致するCNS画像所見」の確認データがない。適格性評価の根拠が不十分である可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 適格性確認に必要な情報がデータセットに含まれていない。
        *   **関連データ:**
            *   該当データなし
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[6]である「患者（および/または法定代理人）と介護者によって署名されたインフォームド・コンセントの取得」が確認できない。同意取得日(DM.RFICDTC)が欠損しているため。参加者の権利保護に関する重大な逸脱の可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [6], 5.1 Informed Consent
        *   **根拠:** 同意取得日のデータ(DM.RFICDTC)が欠損している。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b]である「スクリーニング時のECG所見（左脚ブロック、徐脈、洞停止、2度/3度房室ブロック等）」の確認データがない。適格性評価の根拠が不十分である可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** 適格性確認に必要なECGデータがデータセットに含まれていない。
        *   **関連データ:**
            *   該当データなし
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[17]「過去5年以内の重篤な心血管系疾患」について、既往歴に「CORONARY ARTERY DISEASE」(軽度) がある。これがプロトコル上の "Serious" に該当しないか、また併用薬(Norvasc)で適切に管理されているかの確認が必要。適格性評価の妥当性に疑義がある。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** MHデータと除外基準の照合。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE'
            *   [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC'
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[18]「過去5年以内の重篤な消化器疾患」について、既往歴に「INTESTINAL POLYPECTOMY」(2009年) がある。これが "Serious" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [18]
        *   **根拠:** MHデータと除外基準の照合。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'INTESTINAL POLYPECTOMY'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[20]「過去5年以内の重篤な呼吸器疾患」について、既往歴に「EMPHYSEMA」(軽度) がある。これが "Serious" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [20]
        *   **根拠:** MHデータと除外基準の照合。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'EMPHYSEMA'
            *   [Severity/Intensity(MH.MHSEV)] = 'MILD'
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[22]「過去5年以内の重篤なリウマチ性疾患」について、既往歴に「ARTHRITIS」(軽度) がある。これが "Serious" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [22]
        *   **根拠:** MHデータと除外基準の照合。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS'
            *   [Severity/Intensity(MH.MHSEV)] = 'MILD'
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[27b]「スクリーニング時の臨床検査値異常（クレアチニン、総ビリルビン、SGOT、SGPT等）」について、ALT(SGPT)とAST(SGOT)が基準値を超過していた。再検査で正常化しているものの、初回検査値が除外基準に抵触していた可能性があり、組み入れ判断の妥当性について確認が必要。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LBデータと除外基準の照合。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 19, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 29, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** P-9
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b]「葉酸、ビタミンB12の基準値下限未満、甲状腺機能検査の基準範囲外」の確認に必要な葉酸 (Folate) の検査データがない。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 適格性確認に必要な検査データがデータセットに含まれていない。
        *   **関連データ:**
            *   LBドメインにFolateのデータなし
    *   **指摘No.:** P-10
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[29b]「梅毒スクリーニング陽性（確認検査含む）」の確認データがない。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 適格性確認に必要な検査データがデータセットに含まれていない。
        *   **関連データ:**
            *   LBドメインに梅毒関連検査のデータなし
    *   **指摘No.:** P-11
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[30b]「HbA1c基準値超（IDDM患者のみ）」の確認データがない。患者がIDDMであるかどうかの情報もない。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [30b]
        *   **根拠:** 適格性確認に必要な検査データがデータセットに含まれていない。
        *   **関連データ:**
            *   LBドメインにHbA1cのデータなし
    *   **指摘No.:** P-12
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたVisit (Visit 1, 4, 5, 7, 8, 9, 10, 11, 12, 13, ET) でのECG実施記録がない。安全性評価の重要な項目が実施されていない可能性がある。
        *   **プロトコル該当箇所:** Attachment LZZT.1 Schedule of Events, 3.9.3.4.2 Cardiovascular Safety Measures
        *   **根拠:** 実施されるべき評価のデータがデータセットに含まれていない。
        *   **関連データ:**
            *   ECGドメインデータなし
    *   **指摘No.:** P-13
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたVisit (Visit 3, 4, 5, 7, 9, 11) での薬物動態測定用採血 (PK sampling) の記録がない。試験目的の一部であるPK評価が実施されていない可能性がある。
        *   **プロトコル該当箇所:** Attachment LZZT.1 Schedule of Events, 3.9.2 Pharmacokinetics
        *   **根拠:** 実施されるべき評価のデータがデータセットに含まれていない。
        *   **関連データ:**
            *   PK関連ドメインデータなし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 選択基準[5]「過去1年以内のADに合致するCNS画像所見」について、実施日と結果、および適格性評価について確認させてください。
        *   **クエリ文面（英語）:** Regarding Inclusion Criterion [5] "CNS imaging compatible with AD within past 1 year", please confirm the date, results, and eligibility assessment.
        *   **判断理由:** 選択基準の遵守を確認し、被験者の適格性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: 3.4.2.1 [5]
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日時が記録されていません。選択基準[6]およびGCP遵守の観点から、同意取得日時の情報を提供してください。治験手順開始前に同意が取得されていたことを確認させてください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Per Inclusion Criterion [6] and GCP, please provide the date/time of consent and confirm it was obtained before any study procedures began.
        *   **判断理由:** 参加者の権利保護とGCP遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: 3.4.2.1 [6], 5.1
    *   **クエリNo.:** Q-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 除外基準[16b]に関連するスクリーニング時のECG結果が確認できません。ECGの実施日、結果、および適格性評価について確認させてください。
        *   **クエリ文面（英語）:** Screening ECG results related to Exclusion Criterion [16b] are not available. Please confirm the ECG date, results, and eligibility assessment.
        *   **判断理由:** 除外基準の遵守を確認し、被験者の適格性と安全性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: 3.4.2.2 [16b]
    *   **クエリNo.:** Q-4 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 既往歴として「冠動脈疾患」(軽度) が報告されています。除外基準[17]「過去5年以内の重篤な心血管系疾患」に該当しないと判断された根拠、および併用中の「NORVASC」による管理状況について確認させてください。
        *   **クエリ文面（英語）:** Medical History reports 'Coronary Artery Disease' (Mild). Please confirm the rationale for not meeting Exclusion Criterion [17] "serious cardiovascular disorder within 5 yrs" and confirm the condition is adequately managed with 'NORVASC'.
        *   **判断理由:** 除外基準の遵守を確認し、被験者の適格性と安全性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE', [Severity/Intensity(MH.MHSEV)] = 'MILD', [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC'
            *   関連するプロトコル箇所: 3.4.2.2 [17]
    *   **クエリNo.:** Q-5 (関連指摘No.: P-8)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時(Study Day -65)のアラニンアミノトランスフェラーゼが「135」(U/L)、アスパラギン酸アミノトランスフェラーゼが「145」(U/L)と高値でした。除外基準[27b]への該当性および組み入れ判断の経緯（再検査結果を含む）について確認させてください。
        *   **クエリ文面（英語）:** At screening (Day -65), ALT was 135 U/L and AST was 145 U/L (HIGH). Please confirm assessment against Exclusion Criterion [27b] (lab abnormalities) and the rationale for enrollment (including re-test results).
        *   **判断理由:** 除外基準の遵守を確認し、被験者の適格性と安全性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALT'/LB.LBDY=-65/LB.LBSTRESN=135, LB.LBTESTCD='AST'/LB.LBDY=-65/LB.LBSTRESN=145, LB.LBTESTCD='ALT'/LB.LBDY=-9/LB.LBSTRESN=19, LB.LBTESTCD='AST'/LB.LBDY=-9/LB.LBSTRESN=29
            *   関連するプロトコル箇所: 3.4.2.2 [27b]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-12)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているVisitでのECG実施記録が確認できません。各規定VisitでのECG実施状況について確認させてください。未実施の場合は理由をお知らせください。
        *   **クエリ文面（英語）:** ECG records for protocol-specified visits (e.g., V4, V5, V7, V8, V9, V10, V11, V12, V13) are missing. Please confirm if ECGs were performed as scheduled. If not performed, please provide the reason.
        *   **判断理由:** プロトコル遵守（評価スケジュール）と安全性監視の実施状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: Attachment LZZT.1, 3.9.3.4.2
    *   **クエリNo.:** Q-7 (関連指摘No.: P-13)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているVisitでの薬物動態測定用採血 (PK sampling) の記録が確認できません。各規定VisitでのPK採血実施状況について確認させてください。未実施の場合は理由をお知らせください。
        *   **クエリ文面（英語）:** Pharmacokinetic (PK) sampling records for protocol-specified visits (V3, V4, V5, V7, V9, V11) are missing. Please confirm if PK samples were collected as scheduled. If not collected, please provide the reason.
        *   **判断理由:** プロトコル遵守（評価スケジュール）と試験目的達成可能性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: Attachment LZZT.1, 3.9.2
    *   **クエリNo.:** Q-8 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「関節炎」が報告されていますが、関連する治療薬の使用記録がありません。関節炎に対する治療薬の使用有無について確認させてください。
        *   **クエリ文面（英語）:** Medical History reports 'Arthritis', but no related concomitant medications (e.g., analgesics) are recorded. Please confirm if any medication was used for arthritis during the study.
        *   **判断理由:** データ完全性の確認のため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', CMドメインに関連薬剤なし
            *   関連するプロトコル箇所: なし
    *   **クエリNo.:** Q-9 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「腸ポリープ切除術」(2009年) が報告されています。除外基準[18]「過去5年以内の重篤な消化器疾患」に該当しないと判断された根拠を確認させてください。
        *   **クエリ文面（英語）:** Medical History reports 'Intestinal Polypectomy' (2009). Please confirm the rationale for not meeting Exclusion Criterion [18] "serious gastrointestinal disorder within 5 yrs".
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'INTESTINAL POLYPECTOMY', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'
            *   関連するプロトコル箇所: 3.4.2.2 [18]
    *   **クエリNo.:** Q-10 (関連指摘No.: P-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「肺気腫」(軽度) が報告されています。除外基準[20]「過去5年以内の重篤な呼吸器疾患」に該当しないと判断された根拠を確認させてください。
        *   **クエリ文面（英語）:** Medical History reports 'Emphysema' (Mild). Please confirm the rationale for not meeting Exclusion Criterion [20] "serious respiratory disorder within 5 yrs".
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'EMPHYSEMA', [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   関連するプロトコル箇所: 3.4.2.2 [20]
    *   **クエリNo.:** Q-11 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として「関節炎」(軽度) が報告されています。除外基準[22]「過去5年以内の重篤なリウマチ性疾患」に該当しないと判断された根拠を確認させてください。
        *   **クエリ文面（英語）:** Medical History reports 'Arthritis' (Mild). Please confirm the rationale for not meeting Exclusion Criterion [22] "serious rheumatologic disorder within 5 yrs".
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   関連するプロトコル箇所: 3.4.2.2 [22]
    *   **クエリNo.:** Q-12 (関連指摘No.: P-9)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の葉酸 (Folate) の検査結果がありません。除外基準[28b]の確認のため、結果を提供してください。
        *   **クエリ文面（英語）:** Screening Folate lab result is missing. Please provide the result to confirm eligibility against Exclusion Criterion [28b].
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインにFolateデータなし
            *   関連するプロトコル箇所: 3.4.2.2 [28b]
    *   **クエリNo.:** Q-13 (関連指摘No.: P-10)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の梅毒検査結果がありません。除外基準[29b]の確認のため、結果を提供してください。
        *   **クエリ文面（英語）:** Screening syphilis test result is missing. Please provide the result to confirm eligibility against Exclusion Criterion [29b].
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインに梅毒関連検査データなし
            *   関連するプロトコル箇所: 3.4.2.2 [29b]
    *   **クエリNo.:** Q-14 (関連指摘No.: P-11)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時のHbA1c検査結果がありません。患者がインスリン依存性糖尿病(IDDM)であるか、およびIDDMの場合のHbA1c結果について確認させてください（除外基準[30b]）。
        *   **クエリ文面（英語）:** Screening HbA1c result is missing. Please confirm if the patient has IDDM and, if so, provide the HbA1c result to confirm eligibility against Exclusion Criterion [30b].
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインにHbA1cデータなし
            *   関連するプロトコル箇所: 3.4.2.2 [30b]
    *   **クエリNo.:** Q-15 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「DIARRHOEA」の開始日(Study Day 3)と併用薬「KAOPECTATE」の開始日(Study Day 4)に1日のずれがあります。記録が正しいかご確認ください。
        *   **クエリ文面（英語）:** There is a 1-day discrepancy between the start date of AE 'DIARRHOEA' (Day 3) and the start date of CM 'KAOPECTATE' (Day 4). Please confirm if the dates are recorded correctly.
        *   **判断理由:** データ整合性の確認のため。
        *   **判断根拠:**
            *   関連するデータ: AE.AESTDY=3, CM.CMSTDY=4 (KAOPECTATE)
            *   関連するプロトコル箇所: なし

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** VS, QSドメイン等で、測定/実施Study Day (--DY) とVisit計画Study Day (VISITDY) に1日のずれが散見される。これは実際の測定日と計画日のずれと考えられ、臨床的な影響は小さいと判断されるため医療機関への問い合わせは不要。データハンドリング conventions を確認し、一貫性を記録する。
        *   **判断理由:** 臨床的影響が小さく、データ入力やシステム上の一般的なずれの可能性が高いため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSDY, VS.VISITDY, QS.QSDY, QS.VISITDY など
    *   **確認事項No.:** I-2 (関連指摘No.: D-5, D-7, D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MH, CM, AEドメインでコーディング関連変数が一部欠損している。コーディングプロセスが未完了の可能性があるため、担当部署に進捗を確認し、完了を促す。最終データセットでの完全性を確保する。
        *   **判断理由:** データ品質の問題であり、内部プロセスで対応可能と判断されるため。
        *   **判断根拠:**
            *   関連するデータ: MHDECOD, CMDECOD, AELLT など
    *   **確認事項No.:** I-3 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインで一部の既往歴開始日 (MHSTDTC) が欠損または不完全（年のみ）。これは病歴聴取の限界や記録ルールの可能性があり、医療機関への問い合わせで必ずしも明確になるとは限らない。データ入力ルールを確認し、現状を記録する。
        *   **判断理由:** 情報取得が困難な可能性があり、臨床評価への影響も限定的と判断されるため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHSTDTC
    *   **確認事項No.:** I-4 (関連指摘No.: なし)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Screening時の肝酵素高値 (ALT 135, AST 145) に対し、再検査で正常化を確認して組み入れたと推測される。この経緯と判断について内部で記録・共有する。
        *   **判断理由:** 組み入れ時の重要な判断事項であり、記録として残すことが望ましいが、既に解決済みであり医療機関への再確認は不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB (ALT, AST at Day -65 and Day -9)
            *   関連するプロトコル箇所: 3.4.2.2 [27b]

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 81歳、性別は女性、人種は白色人種、民族はヒスパニックまたはラテン系ではない。計画された投与群および実際の投与群は Xanomeline 低用量群 (Xanomeline Low Dose)。居住国は USA。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit)|イベント内容|
|:---|:---|:---|
|2012年07月08日|Day -61|有害事象「局所感染」(LOCALISED INFECTION) 発現 (Moderate, 未回復)。併用薬 KEFLEX (Cephalexin) 投与開始。|
|2012年08月25日|Day -13 (Screening 1)|MMSEスコア: 23点 (Recall 0/3)。Hachinski Ischemic Score: 1点。既往歴としてアルツハイマー病 (2009年発症)、高血圧、甲状腺機能低下症、骨粗鬆症など多数あり。検査: 赤血球数 (RBC) 低値 (3.8 TI/L)。|
|2012年09月02日|Day -5|有害事象「紅斑」(ERYTHEMA) 発現 (Mild)。有害事象「そう痒症」(PRURITUS) 発現 (Mild)。併用薬 HYDROCORTISONE, TOPICAL 投与開始。|
|2012年09月04日|Day -3|併用薬 HYDROCORTISONE, TOPICAL 投与終了。|
|2012年09月07日|Day 1 (Baseline)|治験薬 Xanomeline 54 mg パッチ投与開始。有害事象「紅斑」「そう痒症」回復。有害事象「排尿切迫」(MICTURITION URGENCY) 発現 (Mild, 未回復)。ADAS-Cog(11) Subscore: 7点。NPI-X Total Score: 2点。体重 59.88 kg。|
|2012年09月13日|Day 7|有害事象「関節痛」(ARTHRALGIA) 発現 (Moderate, 未回復)。有害事象「蜂巣炎」(CELLULITIS) 発現 (Moderate, 未回復)。|
|2012年09月16日|Day 10|治験薬 Xanomeline 54 mg パッチ投与終了。|
|2012年09月17日|Day 11 (Week 2)|有害事象により試験中止。検査: 赤血球数 (RBC) 低値 (3.7 TI/L)、平均赤血球容積 (MCV) 高値 (101 fL)、尿比重 (SPGRAV) 低値 (1.004)、アニソサイトーシス異常 (ABNORMAL)。バイタルサイン: 立位での収縮期血圧低下傾向 (臥位125→立位3分後110 mmHg)。ADAS-Cog(11) Subscore: 5点。CIBIC+: 4 (No Change)。NPI-X Total Score: 1点。体重 60.78 kg。|
|2013年02月22日|Day 169 (Retrieval)|ADAS-Cog(11) Subscore: 9点 (Baseline比悪化)。CIBIC+: 5 (Minimal worsening)。NPI-X Total Score: 45点 (Baseline/Week 2から著しく悪化)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 11に有害事象により試験中止となっているが、中止の直接的な原因となったAEの詳細が不明確。Day 7に中等度の関節痛と蜂巣炎が発現しており、これらが中止理由である可能性が高い（RELRECで関節痛と中止が関連付けられている）。蜂巣炎は感染症であり、局所感染の既往・継続もあるため、臨床的に重要。中止判断の妥当性、AEの重篤度評価、治験薬との関連性評価、実施された処置、最終的な転帰について詳細な情報が必要。参加者の安全性評価に影響する。
        *   **根拠:** DSレコードで中止理由が「ADVERSE EVENT」と記載。AEレコードでDay 7に関節痛と蜂巣炎（いずれもModerate, 未回復）が報告。RELRECでAE SEQ=7 (関節痛) と DS SEQ=1 (中止) が関連付けられている。プロトコルでは重篤な有害事象や安全性懸念による中止が規定されている。
        *   **関連データ:**
            *   [標準化された処置用語(DS.DSDECOD)] = 'ADVERSE EVENT' (DS)
            *   [処置イベントの開始日(DS.DSSTDTC)] = '2012-09-17' (DS)
            *   [報告された有害事象の用語(AE.AETERM)] = 'ARTHRALGIA', [有害事象の開始日(AE.AESTDTC)] = '2012-09-13', [重症度/強度(AE.AESEV)] = 'MODERATE', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AE, AESEQ=7)
            *   [報告された有害事象の用語(AE.AETERM)] = 'CELLULITIS', [有害事象の開始日(AE.AESTDTC)] = '2012-09-13', [重症度/強度(AE.AESEV)] = 'MODERATE', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AE, AESEQ=8)
            *   [関連レコード識別子(RELREC.RELID)] = '01-701-1111-E16' (RELREC)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 11の血液検査で赤血球数(RBC)の低値継続と平均赤血球容積(MCV)の高値化（基準値上限超）が認められる。大球性貧血の可能性を示唆しており、臨床的な評価が必要。原因として、基礎疾患（アルツハイマー病、甲状腺機能低下症）、加齢、栄養状態、薬剤性（Xanomeline含む）などが考えられる。特に治験薬投与期間中にMCVが上昇している点は注目すべき。参加者の安全性評価に影響する。
        *   **根拠:** 一般的な医学知識として、RBC低値とMCV高値は大球性貧血を示唆する。薬剤が原因となる場合もある。
        *   **関連データ:**
            *   [検査/検査略称(LB.LBTESTCD)] = 'RBC', [検査結果(数値)(LB.LBSTRESN)] = 3.7, [基準範囲指標(LB.LBNRIND)] = 'LOW', [検査日(Study Day)(LB.LBDY)] = 11
            *   [検査/検査略称(LB.LBTESTCD)] = 'MCV', [検査結果(数値)(LB.LBSTRESN)] = 101, [基準範囲指標(LB.LBNRIND)] = 'HIGH', [検査日(Study Day)(LB.LBDY)] = 11
            *   [検査/検査略称(LB.LBTESTCD)] = 'VITB12', [検査結果(数値)(LB.LBSTRESN)] = 388.8206, [基準範囲指標(LB.LBNRIND)] = 'NORMAL', [検査日(Study Day)(LB.LBDY)] = -13
            *   [検査/検査略称(LB.LBTESTCD)] = 'TSH', [検査結果(数値)(LB.LBSTRESN)] = 1.25, [基準範囲指標(LB.LBNRIND)] = 'NORMAL', [検査日(Study Day)(LB.LBDY)] = -13
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Day 11のバイタルサイン測定で、立位での収縮期血圧低下傾向が認められる（臥位125 mmHgから立位3分後110 mmHgへ15 mmHg低下）。起立性低血圧の可能性があり、臨床的な評価が必要。Xanomelineはコリン作動薬であり血圧低下を引き起こす可能性がある。高齢、高血圧既往、併用薬（Lisinopril）も影響因子となりうる。失神リスクなど参加者の安全性に関わる可能性がある。
        *   **根拠:** 一般的な医学知識として、臥位から立位への収縮期血圧20mmHg以上の低下は起立性低血圧とされる。コリン作動薬の副作用として血圧低下が知られている。
        *   **関連データ:**
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure', [バイタルサイン被験者の位置(VS.VSPOS)] = 'SUPINE', [標準単位での数値結果/所見(VS.VSSTRESN)] = 125, [バイタルサインの試験日(Study Day)(VS.VSDY)] = 11
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure', [バイタルサイン被験者の位置(VS.VSPOS)] = 'STANDING', [標準単位での数値結果/所見(VS.VSSTRESN)] = 110, [計画的な時点名(VS.VSTPT)] = 'AFTER STANDING FOR 3 MINUTES', [バイタルサインの試験日(Study Day)(VS.VSDY)] = 11
            *   [報告された有害事象の用語(AE.AETERM)] に失神やめまいの報告なし。
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Retrieval Visit (Day 169) におけるNPI-XスコアがBaseline (2点) やWeek 2 (1点) と比較して著しく悪化 (45点) している。特に妄想、興奮/攻撃性、脱抑制、易刺激性/不安定性のスコアが高い。治験薬中止後長期間経過しており、薬剤効果の評価は困難だが、疾患の急速な進行、薬剤中止による影響（離脱症状等）、あるいは他の要因による精神症状の悪化が考えられ、医学的な評価が必要。
        *   **根拠:** NPI-Xはアルツハイマー病の行動・心理症状 (BPSD) を評価する指標。スコアの急激な悪化は臨床的に重要。
        *   **関連データ:**
            *   [質問票の質問名(QS.QSTEST)] = 'NPI-X (9) Total Score', [標準単位での数値結果/所見(QS.QSSTRESN)] = 45, [質問票の試験日(Study Day)(QS.QSDY)] = 169
            *   [質問票の質問名(QS.QSTEST)] = 'DELUSIONS Score', [標準単位での数値結果/所見(QS.QSSTRESN)] = 12, [質問票の試験日(Study Day)(QS.QSDY)] = 169
            *   [質問票の質問名(QS.QSTEST)] = 'AGITATION/AGRESSION Score', [標準単位での数値結果/所見(QS.QSSTRESN)] = 8, [質問票の試験日(Study Day)(QS.QSDY)] = 169
            *   [質問票の質問名(QS.QSTEST)] = 'DISINHIBITION Score', [標準単位での数値結果/所見(QS.QSSTRESN)] = 12, [質問票の試験日(Study Day)(QS.QSDY)] = 169
            *   [質問票の質問名(QS.QSTEST)] = 'IRRITABILITY/LABILITY Score', [標準単位での数値結果/所見(QS.QSSTRESN)] = 4, [質問票の試験日(Study Day)(QS.QSDY)] = 169

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、紅斑 (AESEQ=1, 4) と そう痒症 (AESEQ=2, 5) がそれぞれ2回記録されている。開始日、終了日、重症度、関連性、転帰、AESPIDが同一であり、重複記録の可能性がある。収集日 (AEDTC) のみが異なる (2012-09-05 vs 2012-09-17)。再発なのか記録エラーなのか確認が必要。データの正確性に影響するが、臨床的な影響は小さいと考えられる。
        *   **根拠:** 同一内容のイベントが異なる収集日で記録されている。
        *   **関連データ:**
            *   [報告された有害事象の用語(AE.AETERM)] = 'ERYTHEMA', [シーケンス番号(AE.AESEQ)] = 1, 4
            *   [報告された有害事象の用語(AE.AETERM)] = 'PRURITUS', [シーケンス番号(AE.AESEQ)] = 2, 5
            *   [収集日/時間(AE.AEDTC)] = '2012-09-05' (AESEQ 1, 2), '2012-09-17' (AESEQ 4, 5)
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** QSドメインのDAD評価において、Baseline (Day 1) と Week 2 (Day 11) で回答が大きく変動しており、特に "NA" (Not Applicable) の使用が一貫していないように見える (例: DAITM25, DAITM26, DAITM27, DAITM28, DAITM29)。Baselineで "N" や "Y" だったものがWeek 2で "NA" になっている。これはデータ入力エラー、評価者/情報提供者の解釈の揺れ、あるいは患者の状態変化を反映している可能性があるが、データの信頼性に疑問が生じる。DADは副次評価項目であり、評価の信頼性に影響を与える可能性がある。
        *   **根拠:** 同一項目に対する短期間での回答カテゴリ（特にNAの使用）の不一致。
        *   **関連データ:**
            *   [質問票の質問略称(QS.QSTESTCD)] = 'DAITM25', [元の結果/所見(QS.QSORRES)] = 'N' (Day 1), 'NA' (Day 11)
            *   [質問票の質問略称(QS.QSTESTCD)] = 'DAITM26', [元の結果/所見(QS.QSORRES)] = 'Y' (Day 1), 'NA' (Day 11)
            *   [質問票の質問略称(QS.QSTESTCD)] = 'DAITM27', [元の結果/所見(QS.QSORRES)] = 'NA' (Day 1), 'NA' (Day 11)
            *   [質問票の質問略称(QS.QSTESTCD)] = 'DAITM28', [元の結果/所見(QS.QSORRES)] = 'NA' (Day 1), 'NA' (Day 11)
            *   [質問票の質問略称(QS.QSTESTCD)] = 'DAITM29', [元の結果/所見(QS.QSORRES)] = 'N' (Day 1), 'NA' (Day 11)
    *   **指摘No.:** D-3
        *   **重要度:** Major （M-2と関連）
        *   **内容:** LBドメインにおいて、RBCがScreening (Day -13) およびWeek 2 (Day 11) で基準値下限を下回っている。MCVがWeek 2 (Day 11) で基準値上限を上回っている。SPGRAVがWeek 2 (Day 11) で基準値下限を下回っている。これらは基準値からの逸脱であり、データ入力エラーの可能性も完全には否定できないが、医学的な評価が必要（M-2, M-3参照）。
        *   **根拠:** LBレコードのLBNRINDが 'LOW' または 'HIGH' となっている。
        *   **関連データ:**
            *   [検査/検査略称(LB.LBTESTCD)] = 'RBC', [基準範囲指標(LB.LBNRIND)] = 'LOW' (Day -13, Day 11)
            *   [検査/検査略称(LB.LBTESTCD)] = 'MCV', [基準範囲指標(LB.LBNRIND)] = 'HIGH' (Day 11)
            *   [検査/検査略称(LB.LBTESTCD)] = 'SPGRAV', [基準範囲指標(LB.LBNRIND)] = 'LOW' (Day 11)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** QSドメインのNPI-X評価において、Baseline (Day 1) および Week 2 (Day 11) では項目ごとのFrequency, Severity, Distressの記録がなく、項目別Score (NPITMxxS) とTotal Score (NPTOT) のみが記録されている。一方、Retrieval (Day 169) ではFrequency, Severity, Distressが記録され、Scoreが計算されている。記録方法が一貫しておらず、Baseline/Week 2のScore算出根拠がデータから直接追跡できない。ただしTotal Scoreは記録されているため、主要な評価への影響は限定的かもしれない。
        *   **根拠:** QSレコードにおいて、QSTESTCDがNPITMxxF, NPITMxxV, NPITMxxDのレコードがDay 1, Day 11に存在しない。
        *   **関連データ:**
            *   QSドメインの Day 1, Day 11, Day 169 の NPI-X関連レコード
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** プロトコル上、Visit 4 (Day 11) で実施されるべきECG、Visit 3 (Day 1) で実施されるべきPKサンプリング、Visit 4 (Day 11) で実施されるべきPKサンプリングのデータがJSONデータに含まれていない。また、Visit 2/3で実施されるべきAmbulatory ECGのデータもない。これらのデータは安全性評価（ECG, Ambulatory ECG）およびPK評価に必須であり、欠損している場合は評価の信頼性に重大な影響を与える。データ収集・入力漏れか、意図的な未収集か確認が必要。
        *   **根拠:** プロトコル 3.9.1.1, 3.9.2, 3.9.3.4.2, Attachment LZZT.1 で規定された評価のデータがJSONに含まれていない。
        *   **関連データ:**
            *   ECGドメインデータなし
            *   PK関連ドメインデータなし
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** QSドメインのNPI-X Total Score (NPTOT) のラベルは「NPI-X (9) Total Score」となっているが、Retrieval Visit (Day 169) のデータを見ると、12項目（NPITM01S～NPITM12S）のスコアの合計値 (45) がNPTOTとして記録されているように見える。プロトコル 4.3.1 では「sleep, appetite, euphoria domainsを除く」と記載されており、9項目での集計が意図されている可能性がある。ラベルと実際の計算内容に齟齬がある可能性があり、確認が必要。評価の解釈に影響する可能性があるが、算出根拠が明確になれば修正可能。
        *   **根拠:** ラベル名とデータ内容の不一致の可能性。プロトコル記載との齟齬の可能性。
        *   **関連データ:**
            *   [質問票の質問略称(QS.QSTESTCD)] = 'NPTOT', [質問票の質問名(QS.QSTEST)] = 'NPI-X (9) Total Score'
            *   QSドメインの Day 169 の NPITMxxS レコード

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 4 (Week 2, Day 11) において、プロトコル (Attachment LZZT.1) で予定されていない有効性評価（ADAS-Cog, CIBIC+, DAD）が実施されている。これらは主要評価項目（ADAS-Cog, CIBIC+）および副次評価項目（DAD）であり、計画外のタイミングでの実施はプロトコルからの逸脱にあたる。評価の信頼性や解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** QSドメインのデータで、Visit 4 (VISITNUM=4) に QSTESTCD が 'ACITM01'-'ACITM14', 'ACTOT', 'CIBIC', 'DAITM01'-'DAITM40' のレコードが存在する。
        *   **関連データ:**
            *   QSドメインの VISITNUM=4 のレコード
    *   **指摘No.:** P-2
        *   **重要度:** Major （D-5と関連）
        *   **逸脱の可能性:** プロトコルで規定されているECG評価 (Visit 4)、Ambulatory ECG評価 (Visit 2/3)、PKサンプリング (Visit 3, 4) が実施されなかった、あるいはデータが記録されなかった可能性がある。これらは安全性評価およびPK評価において重要な手順であり、未実施またはデータ欠損はプロトコルからの逸脱であり、評価の信頼性を損なう。
        *   **プロトコル該当箇所:** Protocol Section 3.9.2, 3.9.3.4.2, Attachment LZZT.1
        *   **根拠:** JSONデータに該当するドメインまたはレコードが存在しない。
        *   **関連データ:**
            *   ECGドメインデータなし
            *   PK関連ドメインデータなし
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル 3.10.1 では、早期中止時に治験薬を漸減投与する（25cm2パッチを除去し、50cm2パッチを中止Visitまで継続）よう指示されている。EXデータではDay 10に投与終了と記録されており、中止日 (Day 11) 前日に終了している。漸減投与が適切に行われたか不明確であり、プロトコルからの逸脱の可能性がある。安全性への影響は小さいと考えられる。
        *   **プロトコル該当箇所:** Protocol Section 3.10.1
        *   **根拠:** EX.EXENDTC が '2012-09-16' (Day 10)、DS.DSSTDTC が '2012-09-17' (Day 11)。
        *   **関連データ:**
            *   [終了日/時間(EX.EXENDTC)] = '2012-09-16'
            *   [処置イベントの開始日(DS.DSSTDTC)] = '2012-09-17'
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 選択基準 [27b] に関して、Screening時のRBC値が基準値下限を下回っていた。プロトコルでは「exceeding」と記載されているが、下回る場合も逸脱とみなされる可能性がある。臨床的に有意でないと判断され組み入れられた可能性が高いが、基準適用の解釈について確認が必要。結果的に組み入れられているため影響は小さい。
        *   **プロトコル該当箇所:** Protocol Section 3.4.2.2 [27b]
        *   **根拠:** LBデータとプロトコル記載の比較。
        *   **関連データ:**
            *   [検査/検査略称(LB.LBTESTCD)] = 'RBC', [検査結果(数値)(LB.LBSTRESN)] = 3.8, [基準範囲指標(LB.LBNRIND)] = 'LOW', [検査日(Study Day)(LB.LBDY)] = -13

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11に有害事象により試験中止となっています。中止の判断に至った有害事象（関節痛、蜂巣炎、あるいはその他）について、重篤度、治験薬との関連性評価、実施された処置、および最終的な転帰（未回復とのことですが、その後の経過を含む）を詳細にご報告ください。特に蜂巣炎の評価について、詳細な臨床所見と判断根拠をお知らせください。
        *   **クエリ文面（英語）:** The subject discontinued the study on Study Day 11 due to an adverse event. Please provide details on the specific AE(s) leading to discontinuation (Arthralgia, Cellulitis, or other?), including seriousness assessment, causality assessment to study drug, actions taken, and final outcome (including follow-up status as it was reported as 'Not Recovered'). For Cellulitis, please provide detailed clinical findings and assessment basis.
        *   **判断理由:** 中止理由となったAEの詳細情報が不明確であり、参加者の安全性評価および中止判断の妥当性を確認するために必要。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='ADVERSE EVENT', AE.AETERM='ARTHRALGIA'(AESEQ=7), AE.AETERM='CELLULITIS'(AESEQ=8), AE.AEOUT='NOT RECOVERED/NOT RESOLVED'
            *   関連するプロトコル箇所: Protocol Section 3.9.3.2, 3.10.1
            *   関連する医学的知見: 有害事象による中止基準、関節痛・蜂巣炎の臨床的重要性
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11の検査にて、赤血球数が3.7 TI/Lと低値が続き、平均赤血球容積が101 fLと高値（基準値上限超）を示しています。これらの所見（大球性貧血の可能性）について、臨床的な意義および考えられる原因（基礎疾患、治験薬との関連を含む）について評価とコメントをお願いします。
        *   **クエリ文面（英語）:** On Study Day 11 labs, RBC count remained low (3.7 TI/L) and MCV was high (101 fL, above ULN). Please assess the clinical significance of these findings (potential macrocytic anemia) and provide comments on possible causes, including relationship to underlying conditions and study drug.
        *   **判断理由:** 基準値逸脱が認められ、治験薬との関連も否定できないため、参加者の安全性評価に必要。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='RBC', LB.LBSTRESN=3.7, LB.LBNRIND='LOW' (Day 11); LB.LBTESTCD='MCV', LB.LBSTRESN=101, LB.LBNRIND='HIGH' (Day 11)
            *   関連するプロトコル箇所: Protocol Section 3.9.3.3
            *   関連する医学的知見: 大球性貧血の原因、薬剤性貧血の可能性
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11のバイタルサインにて、臥位から立位3分後に収縮期血圧が15 mmHg低下しています（臥位125 mmHg → 立位110 mmHg）。起立性低血圧の可能性について、臨床的な意義（症状の有無を含む）および考えられる原因（治験薬との関連を含む）について評価とコメントをお願いします。
        *   **クエリ文面（英語）:** On Study Day 11 vital signs, systolic blood pressure dropped by 15 mmHg upon standing for 3 minutes (Supine 125 mmHg -> Standing 110 mmHg). Please assess the clinical significance of potential orthostatic hypotension (including presence/absence of symptoms) and comment on possible causes, including relationship to the study drug.
        *   **判断理由:** 起立性低血圧を示唆する所見であり、失神等のリスク評価のため、臨床的意義の確認が必要。治験薬との関連も評価する必要がある。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='SYSBP', VS.VSPOS='SUPINE', VS.VSSTRESN=125 (Day 11); VS.VSTESTCD='SYSBP', VS.VSPOS='STANDING', VS.VSSTRESN=110, VS.VSTPT='AFTER STANDING FOR 3 MINUTES' (Day 11)
            *   関連するプロトコル箇所: Protocol Section 3.9.3.4.1
            *   関連する医学的知見: 起立性低血圧の定義、コリン作動薬の副作用
    *   **クエリNo.:** Q-4 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DAD評価について、Baseline (Study Day 1) と Week 2 (Study Day 11) の間で、特に外出関連の項目（DAITM25～DAITM29）などで回答（「はい」「いいえ」「該当なし」）が一貫していません。例えば、「外出を試みる」はDay 1で「いいえ」でしたがDay 11で「該当なし」となっています。これらの回答の変動理由、特に「該当なし」と判断された根拠についてご確認ください。
        *   **クエリ文面（英語）:** Regarding the DAD assessment, responses (Yes/No/Not Applicable) appear inconsistent between Baseline (Day 1) and Week 2 (Day 11), particularly for outing-related items (DAITM25-DAITM29). For example, 'Undertake to go out' was 'No' on Day 1 but 'NA' on Day 11. Please clarify the reason for these discrepancies, especially the rationale for using 'NA'.
        *   **判断理由:** 副次評価項目であるDADデータの信頼性を確保するため、回答の不一致理由を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのDAD関連レコード (DAITM25-DAITM29など) のQSORRES値 (Day 1 vs Day 11)
            *   関連するプロトコル箇所: Protocol Section 3.9.1.1 (DAD評価)
    *   **クエリNo.:** Q-5 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 4 (Week 2, Study Day 11) において、プロトコルで予定されていない有効性評価（ADAS-Cog, CIBIC+, DAD）が実施されています。実施された理由についてご確認ください。
        *   **クエリ文面（英語）:** Efficacy assessments (ADAS-Cog, CIBIC+, DAD) were performed at Visit 4 (Week 2, Study Day 11), which were not scheduled per protocol (Attachment LZZT.1). Please clarify the reason for performing these assessments at this visit.
        *   **判断理由:** プロトコルからの逸脱であり、主要/副次評価項目のデータであるため、実施理由の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: QSドメインの VISITNUM=4 の ADAS-Cog, CIBIC+, DAD 関連レコード
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 (Schedule of Events)
    *   **クエリNo.:** Q-6 (関連指摘No.: D-5, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで Visit 4 (Study Day 11) に予定されていたECGデータ、Visit 3 (Study Day 1) および Visit 4 (Study Day 11) に予定されていたPKサンプル採取データ、Visit 2/3 に予定されていたAmbulatory ECGデータが報告されていません。これらの評価・サンプル採取が実施されなかったのか、あるいはデータが未報告なのかご確認ください。実施されなかった場合はその理由をお知らせください。
        *   **クエリ文面（英語）:** Data for ECG scheduled at Visit 4 (Day 11), PK samples scheduled at Visit 3 (Day 1) and Visit 4 (Day 11), and Ambulatory ECG scheduled at Visit 2/3 are missing. Please confirm if these procedures/collections were not performed or if the data has not yet been reported. If not performed, please provide the reason.
        *   **判断理由:** 安全性評価およびPK評価に必要なデータが欠損しており、プロトコル逸脱の可能性があるため確認が必要。評価の信頼性に影響する。
        *   **判断根拠:**
            *   関連するデータ: ECG, PK関連ドメインデータなし
            *   関連するプロトコル箇所: Protocol Section 3.9.2, 3.9.3.4.2, Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEの紅斑 (AESEQ=1, 4) と そう痒症 (AESEQ=2, 5) が重複して記録されている可能性。収集日のみ異なる。再発ではなく、Week 2 Visit (Day 11) で過去のAEを再確認した際に誤って再入力された可能性が高い。臨床的な影響は小さいと判断されるため、内部でデータクリーニング対象として検討する。
        *   **判断理由:** データ入力エラーの可能性が高く、臨床的影響が小さいため医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン AESEQ=1, 2, 4, 5
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QS (NPI-X) のBaseline/Week 2でFrequency/Severity/Distressの記録がなくScoreのみ記録されている。Retrieval Visitでは詳細記録あり。記録方法の不一致。Total Scoreは存在するため評価への影響は限定的。EDCシステムの設定や入力手順の問題の可能性。今後のデータ入力の一貫性確保のため、必要であれば手順見直しを検討。
        *   **判断理由:** データの一貫性の問題だが、主要な評価指標は存在するため影響は小さい。内部での確認・対応で十分と判断。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン NPI-X関連レコード (Day 1, 11 vs Day 169)
    *   **確認事項No.:** I-3 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM / Biostatistician
        *   **疑義事項/確認内容:** NPI-X Total Score (NPTOT) のラベルが「NPI-X (9) Total Score」である一方、データ上は12項目合計の可能性がある。プロトコル 4.3.1 の記載（sleep, appetite, euphoria除く）と齟齬があるか確認が必要。解析プログラムや仕様書を確認し、必要であれば修正する。
        *   **判断理由:** ラベルと内容の不一致の可能性であり、内部での定義・計算方法の確認で解決可能と判断。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD='NPTOT', QS.QSTEST='NPI-X (9) Total Score', Day 169のNPITMxxSレコード
            *   関連するプロトコル箇所: Protocol Section 4.3.1
    *   **確認事項No.:** I-4 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 早期中止時の治験薬漸減投与がプロトコル通り実施されたか不明確。EXデータでは中止前日に投与終了となっている。漸減投与の有無について、可能であればサイトスタッフへのヒアリング等で確認し記録する。安全性への影響は小さいと考えられる。
        *   **判断理由:** 軽微なプロトコル逸脱の可能性であり、安全性への影響が小さいと考えられるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: EX.EXENDTC, DS.DSSTDTC
            *   関連するプロトコル箇所: Protocol Section 3.10.1
    *   **確認事項No.:** I-5 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor / CRA
        *   **疑義事項/確認内容:** Screening時のRBC低値が選択基準 [27b] に抵触しなかったか確認。プロトコル記載は「exceeding」だが、下回る場合も含むか、あるいは臨床的に有意でないと判断されたか。今後の同様ケースの判断基準を明確にするため、内部で議論・記録する。
        *   **判断理由:** 基準適用の解釈に関する事項であり、結果的に組み入れられているため影響は小さい。内部での確認・記録で十分と判断。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='RBC', LB.LBNRIND='LOW' (Day -13)
            *   関連するプロトコル箇所: Protocol Section 3.4.2.2 [27b]