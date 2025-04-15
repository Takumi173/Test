# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    [Age(AGE)]は 77歳、[Sex(SEX)]は男性、[Race(RACE)]はWHITE、[Ethnicity(ETHNIC)]はNOT HISPANIC OR LATINO、[Description of Planned Arm(ARM)]はXanomeline High Dose、[Description of Actual Arm(ACTARM)]はXanomeline High Dose、[Country(COUNTRY)]はUSA。ベースラインは2013-10-06 ([Subject Reference Start Date/Time(RFSTDTC)])。最終治験薬投与は2013-11-18 ([Date/Time of Last Study Treatment(RFXENDTC)])、最終参加日は2013-12-06 ([Date/Time of End of Participation(RFPENDTC)])。
*   **イベント推移:**
    *   2011-03-27: [Reported Term for the Medical History(MH.MHTERM)] = 'ALZHEIMER'S DISEASE' 発症 ([Start Date/Time of Medical History Event(MH.MHSTDTC)])。
    *   2013-09-20 (Day -16): Screening 1 Visit。主要な既往歴として[Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK' (2000年)、[Reported Term for the Medical History(MH.MHTERM)] = 'TRIPLE VESSEL BYPASS GRAFT' (2006年)あり。MMSEスコア 21点。ベースライン検査で[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT' (クレアチニン) が 1.8 mg/dL ([Reference Range Indicator(LB.LBNRIND)] = 'HIGH', 基準値上限 1.6 mg/dL)。
    *   2013-10-06 (Day 1): Baseline Visit。治験薬 [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE' 54 mg/day ([Dose per Administration(EX.EXDOSE)]) 投与開始 ([Start Date/Time of Treatment(EX.EXSTDTC)])。併用薬 [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN' 開始 ([Start Date/Time of Medication(CM.CMSTDTC)])。[ADAS-COG(11) Subscore(QS.QSTESTCD)] = 'ACTOT' ベースライン値 27点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])。[NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT' ベースライン値 61点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])。
    *   2013-10-19 (Day 14): Week 2 Visit。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION' ([Severity/Intensity(AE.AESEV)] = 'MILD') 発現 ([Start Date/Time of Adverse Event(AESTDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT' ([Severity/Intensity(AE.AESEV)] = 'MILD') 発現 ([Start Date/Time of Adverse Event(AESTDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION' ([Severity/Intensity(AE.AESEV)] = 'SEVERE') 発現 ([Start Date/Time of Adverse Event(AESTDTC)])。検査値で[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN' (BUN) が 29 mg/dL ([Reference Range Indicator(LB.LBNRIND)] = 'HIGH', 基準値上限 24 mg/dL)、[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB' (アルブミン) が 3.3 g/dL ([Reference Range Indicator(LB.LBNRIND)] = 'LOW', 基準値下限 3.5 g/dL)。[NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT' 22点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])。
    *   2013-10-20 (Day 15): 治験薬 [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE' 81 mg/day ([Dose per Administration(EX.EXDOSE)]) へ増量 ([Start Date/Time of Treatment(EX.EXSTDTC)])。
    *   2013-10-29 (Day 24): 併用薬 [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN' 終了 ([End Date/Time of Medication(CM.CMENDTC)])。
    *   2013-11-01 (Day 27): Week 4 Visitの検査実施日 ([Date/Time of Specimen Collection(LB.LBDTC)])。検査値で[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB' (アルブミン) が 3.4 g/dL ([Reference Range Indicator(LB.LBNRIND)] = 'LOW', 基準値下限 3.5 g/dL)。[Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT' の記録あり ([Start Date/Time of Disposition Event(DS.DSSTDTC)])。
    *   2013-11-05 (Day 31): 有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH' ([Severity/Intensity(AE.AESEV)] = 'MILD', [Causality(AE.AEREL)] = 'PROBABLE') 発現 ([Start Date/Time of Adverse Event(AESTDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS' ([Severity/Intensity(AE.AESEV)] = 'MILD', [Causality(AE.AEREL)] = 'PROBABLE') 発現 ([Start Date/Time of Adverse Event(AESTDTC)])。
    *   2013-11-06 (Day 32): 併用薬 [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL' 開始 ([Start Date/Time of Medication(CM.CMSTDTC)])。
    *   2013-11-09 (Day 35): Week 4 Visit実施日 ([Start Date/Time of Visit(SV.SVSTDTC)])。[NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT' 38点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])。
    *   2013-11-18 (Day 44): 治験薬 [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE' 81 mg/day 投与終了 ([End Date/Time of Treatment(EX.EXENDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH' ([Severity/Intensity(AE.AESEV)] = 'SEVERE') 発現・同日回復 ([Start Date/Time of Adverse Event(AESTDTC)], [End Date/Time of Adverse Event(AEENDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION' 回復 ([End Date/Time of Adverse Event(AEENDTC)])。
    *   2013-11-19 (Day 45): 有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION' 回復 ([End Date/Time of Adverse Event(AEENDTC)])。
    *   2013-11-22 (Day 48): 有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH' 回復 ([End Date/Time of Adverse Event(AEENDTC)])。有害事象 [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS' 回復 ([End Date/Time of Adverse Event(AEENDTC)])。併用薬 [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL' 終了 ([End Date/Time of Medication(CM.CMENDTC)])。
    *   2013-11-24 (Day 50): Week 6 Visit。[ADAS-COG(11) Subscore(QS.QSTESTCD)] = 'ACTOT' 30点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])。[EXTENT OF CHANGE, IF ANY, SINCE BASELINE(QS.QSTESTCD)] = 'CIBIC' 4 (No Change) ([Numeric Finding in Standard Units(QS.QSSTRESN)])。[NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT' 16点 ([Numeric Finding in Standard Units(QS.QSSTRESN)])、[HALLUCINATIONS FREQUENCY(QS.QSTESTCD)]='NPITM02F' が 1 で初報告。有害事象による中止 ([Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT') ([Start Date/Time of Disposition Event(DS.DSSTDTC)])。
    *   2013-12-06 (Day 62): AE Follow-up Visit。試験参加終了日 ([Date/Time of End of Participation(DM.RFPENDTC)])。

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象として[Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'が報告され、同日に回復([Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED')と記録されている。脳死からの同日回復は医学的にありえず、事象名または転帰・終了日の記録が誤っている可能性が極めて高い。これが実際に重篤な神経学的イベントを示唆する場合、参加者の安全性に重大な影響があった可能性、あるいはデータの信頼性に致命的な問題があることを示唆する。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Severity/Intensity(AE.AESEV)] = 'SEVERE', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-11-18', [End Date/Time of Adverse Event(AEENDTC)] = '2013-11-18', [Outcome of Adverse Event(AEOUT)] = 'RECOVERED/RESOLVED', [Study Day of Start of Adverse Event(AESTDY)] = 44, [Study Day of End of Adverse Event(AEENDY)] = 44. 一般的な医学的知見。
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day 14に有害事象[Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'が[Severity/Intensity(AE.AESEV)] = 'MILD'、[Causality(AE.AEREL)] = 'NONE'で報告されている。心筋梗塞は通常重篤であり、Mildとの評価は疑問。また、[Action Taken with Study Treatment(AEACN)] = 'DRUG WITHDRAWN'と記録されているにも関わらず、翌日(Day 15)に治験薬が増量されている点は矛盾している。患者は心筋梗塞の既往歴([Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', 2000年)があり、新たな心イベントのリスク評価と治験薬との関連性評価([Causality(AE.AEREL)] = 'NONE')は慎重に行うべき。評価の妥当性とデータの一貫性に疑義がある。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION', [Severity/Intensity(AE.AESEV)] = 'MILD', [Causality(AE.AEREL)] = 'NONE', [Action Taken with Study Treatment(AEACN)] = 'DRUG WITHDRAWN', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19' (Day 14). [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (Day 15). [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2000-05-15'. 一般的な医学的知見。
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Day 50に有害事象により試験が中止されている([Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT')。しかし、記録されている有害事象はいずれもDay 50以前に終了・回復しているか、中止理由としては軽微(Rash/Pruritus: Mild, Resolved Day 48)または関連性が低い(VSD: Mild, Congenital?)ように見える。中止に至った具体的な有害事象が不明確であり、安全性評価の観点から確認が必要。RELRECではRash AE (AESPID E11)が中止(RELID 01-704-1017-E11)と関連付けられているが、軽微であり既に回復しているため疑わしい。
        *   **根拠:** [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DSSTDTC)] = '2013-11-24' (Day 50). AEドメインの各事象の転帰・終了日。RELRECデータ。
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** ベースラインの[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT' (クレアチニン) が1.8 mg/dLであり、基準範囲上限(1.6 mg/dL)を超えている。プロトコル除外基準[27b]では、基準値を超える検査値は除外対象となりうる（臨床的に意義がないと判断され文書化された場合を除く）。適格性評価と除外基準適用の妥当性について確認が必要。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Result or Finding in Original Units(LB.LBORRES)] = '1.8', [Original Units(LB.LBORRESU)] = 'mg/dL', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6', [Visit Name(LB.VISIT)] = 'SCREENING 1', [Baseline Flag(LB.LBBLFL)] = 'Y'. Protocol Section 3.4.2.2 Exclusion Criteria [27b].
    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** 有害事象として[Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'がDay 14に発現している。しかし、MHドメインには脳梗塞の既往歴が明記されていない（心筋梗塞は記載あり）。過去の脳梗塞イベントの有無、および本AEが新規イベントなのか既往歴の再燃・後遺症なのか、治験薬との関連性評価を含めて確認が必要。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19' (Day 14). MHドメインデータ。
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** 有害事象として[Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'がDay 14に発現している。心室中隔欠損症は通常先天性疾患であり、治験期間中に新たに出現する有害事象として報告するのは不適切と考えられる。既往歴としての報告漏れ、あるいは別の心イベントの誤記の可能性がないか確認が必要。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT', [Severity/Intensity(AE.AESEV)] = 'MILD', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19' (Day 14). 一般的な医学的知見。
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** Day 14およびDay 27の検査で[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB' (アルブミン) が基準値下限を下回っている([Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 33 g/L, 34 g/L, 基準値下限 35 g/L)。軽度の低下であり、臨床的意義は不明だが、患者の栄養状態や全身状態との関連で留意すべき所見。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 33, [Study Day of Specimen Collection(LB.LBDY)] = 14. [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 34, [Study Day of Specimen Collection(LB.LBDY)] = 27. [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 35.
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** Day 14の検査で[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN' (BUN) が基準値上限を上回っている([Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 10.353 mmol/L, 基準値上限 8.6 mmol/L)。Day 27には正常化しており一過性の変動の可能性が高いが、脱水や腎機能への影響について留意。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 10.353, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 14. [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 8.6.

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** AE「MYOCARDIAL INFARCTION」([AESEQ]=1)の記録において、[Action Taken with Study Treatment(AEACN)]='DRUG WITHDRAWN'とされているが、EXドメインではその翌日に治験薬が増量されている。AEに対する処置と実際の投薬記録が矛盾しており、どちらかの記録が誤っている可能性が高い。安全性評価と曝露量評価に影響する。
        *   **根拠:** [Sequence Number(AE.AESEQ)] = 1, [Action Taken with Study Treatment(AEACN)] = 'DRUG WITHDRAWN', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19'. [Sequence Number(EX.EXSEQ)] = 2, [Dose per Administration(EX.EXDOSE)] = 81, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20'.
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** Day 50に有害事象により中止([Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT')と記録されているが、AEドメインの記録からは中止の原因となったAEが特定できない（終了日・転帰との不整合）。中止理由の特定は安全性評価において重要。
        *   **根拠:** [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DSSTDTC)] = '2013-11-24' (Day 50). AEドメインの各レコードの[End Date/Time of Adverse Event(AEENDTC)], [Outcome of Adverse Event(AEOUT)]. RELRECデータ。
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** Visit 5 (Week 4)の検査データ([Visit Number(LB.VISITNUM)]=5)の採取日([Date/Time of Specimen Collection(LBDTC)])が '2013-11-01' (Day 27) となっているが、Visit 5の来院日([Start Date/Time of Visit(SV.SVSTDTC)])は '2013-11-09' (Day 35) と記録されている。検査日と来院日が一致しておらず、データの帰属Visitが正しいか確認が必要。評価の信頼性に影響する。
        *   **根拠:** [Visit Number(LB.VISITNUM)] = 5, [Date/Time of Specimen Collection(LBDTC)] = '2013-11-01T10:45', [Study Day of Specimen Collection(LB.LBDY)] = 27. [Visit Number(SV.VISITNUM)] = 5, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-09', [Planned Study Day of Visit(SV.VISITDY)] = 28.
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** DSドメインに[Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT' というマイルストーンがDay 27 ([Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-01') に記録されている。これはVisit 5 (Week 4)に関連付けられているが、その後のVisit (Visit 6, 7) や最終参加日 (Day 62) を考慮すると時期尚早であり、このイベントの意味合いと記録の妥当性が不明。
        *   **根拠:** [Sequence Number(DS.DSSEQ)] = 2, [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT', [Category for Disposition Event(DS.DSCAT)] = 'OTHER EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-01', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 27, [Visit Number(DS.VISITNUM)] = 5. SVドメイン、DMドメインの[Date/Time of End of Participation(RFPENDTC)].
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** AEドメインに[Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION' が報告されているが、MHドメインには対応する脳梗塞の既往歴が明記されていない。既往歴データの完全性に疑義がある。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'. MHドメインデータ。
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** AEドメインに[Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT' が報告されている。これは通常先天性疾患であり、治療期間中に発現した有害事象としての報告は不適切。データの分類・入力エラーの可能性がある。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19'. 一般的な医学的知見。
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** RELRECデータは、Rash AE (AESPID E11, AESEQ 5, 7) と AEによる中止 (DSSEQ 1) を関連付けている ([Relationship Identifier(RELREC.RELID)] = '01-704-1017-E11')。しかし、Rashは軽微であり中止日(Day 50)より前に回復(Day 48)しているため、この関連付けは臨床的な時間経過と一致しない可能性がある。データの関連付けの正確性に疑問があるが、評価への影響は限定的か。
        *   **根拠:** RELRECデータ, AEデータ ([Sequence Number(AE.AESEQ)] = 5, 7), DSデータ ([Sequence Number(DS.DSSEQ)] = 1).
    *   **指摘No.:** D-8
        *   **重要度:** Critical
        *   **内容:** AE「BRAIN DEATH」([AESEQ]=3)の開始日([Start Date/Time of Adverse Event(AESTDTC)])と終了日([End Date/Time of Adverse Event(AEENDTC)])が同日('2013-11-18')となっている。これは医学的にありえず、データ入力エラーの可能性が高い。データの正確性に重大な問題がある。
        *   **根拠:** [Sequence Number(AE.AESEQ)] = 3, [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-11-18', [End Date/Time of Adverse Event(AEENDTC)] = '2013-11-18'.
    *   **指摘No.:** D-9
        *   **重要度:** Critical
        *   **内容:** DMドメインの[Date/Time of Informed Consent(DM.RFICDTC)]が欠損している。インフォームド・コンセントの取得日時はGCP遵守および参加者の権利保護を確認する上で必須の情報であり、欠損は重大な問題。
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = ''.

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** インフォームド・コンセント取得日の記録がないため、治験手順開始前に同意が適切に取得されたか確認できない。GCP違反の可能性。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = ''. (D-9と関連)
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** ベースラインのNPI-Xで[DEPRESSION/DYSPHORIA Score(QS.QSTESTCD)]='NPITM04S'が9点（頻度3, 重症度3）と記録されている。プロトコル除外基準[13]では「3ヶ月以内のDSM-IV基準を満たすうつ病エピソード」を除外している。NPI-XスコアのみではDSM-IV基準を満たすか不明だが、評価が必要だった可能性がある。適格性評価が不十分だった可能性は低いが留意。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [13]
        *   **根拠:** [Question Short Name(QS.QSTESTCD)] = 'NPITM04S', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 9, [Baseline Flag(QS.QSBLFL)] = 'Y'.
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 患者は心筋梗塞(2000年)、冠動脈バイパス術(2006年)の既往があり、スクリーニング時にも心臓関連の所見が複数記録されている。プロトコル除外基準[17]では「過去5年以内の重篤な心血管系障害」を除外している。既往歴は5年以上前だが、現在の状態が「重篤」でないかの評価が重要。Day 14の心筋梗塞AE報告も踏まえ、適格性評価の妥当性に疑問が残る。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** MHドメインデータ ([Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT', 'CARDIAC DISORDER', etc.). AEドメインデータ ([Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-10-19').
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** ベースラインのクレアチニン値が基準値上限を超えていた。プロトコル除外基準[27b]に抵触する可能性がある。臨床的に意義がないと判断された場合、その旨の文書化が必要とプロトコルに記載されているが、その確認がデータからはできない。適格性評価プロセスが不十分だった可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Result or Finding in Original Units(LB.LBORRES)] = '1.8', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6', [Visit Name(LB.VISIT)] = 'SCREENING 1'. (M-4と関連)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬Premarin (エストロゲン製剤) がDay 1に開始されている。プロトコル除外基準[31b] v) では、エストロゲン補充療法は許可されるが、登録前3ヶ月間用量が安定している必要がある。Day 1開始はこの安定性要件に違反する。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] v)
        *   **根拠:** [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06' (Day 1).
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 5 (Week 4) が Day 35 に実施された。プロトコル規定の Visit Window (Day 28 +/- 3日 = Day 25-31) から逸脱している。評価タイミングのずれが有効性・安全性評価に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Windows: Visits 4, 5, 7, 8, 13 should occur within 3 days of their scheduled date)
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 5, [Visit Name(SV.VISIT)] = 'WEEK 4', [Planned Study Day of Visit(SV.VISITDY)] = 28, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-09' (Day 35).
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 7 (Week 6) が Day 50 に実施された。プロトコル規定の Visit Window (Day 42 +/- 3日 = Day 39-45) から逸脱している。評価タイミングのずれが有効性・安全性評価に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Windows: Visits 4, 5, 7, 8, 13 should occur within 3 days of their scheduled date)
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 7, [Visit Name(SV.VISIT)] = 'WEEK 6', [Planned Study Day of Visit(SV.VISITDY)] = 42, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-24' (Day 50).
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルではAmbulatory ECGはVisit 2/3で実施と記載されているが、本症例ではVisit 3.5 (Day 13) に配置、Visit 6 (Day 37) に除去という追加のAmbulatory ECG実施記録がある。プロトコル外の評価が実施された可能性、あるいは記録エラーの可能性がある。
        *   **プロトコル該当箇所:** Section 3.1, Section 3.9.3.4.2
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 3.5, [Visit Name(SV.VISIT)] = 'AMBUL ECG PLACEMENT', [Planned Study Day of Visit(SV.VISITDY)] = 13. [Visit Number(SV.VISITNUM)] = 6, [Visit Name(SV.VISIT)] = 'AMBUL ECG REMOVAL', [Planned Study Day of Visit(SV.VISITDY)] = 30.

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-8)
        *   **重要度:** Critical
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として報告された「Reported Term for the Adverse Event」が「BRAIN DEATH」について、[Start Date/Time of Adverse Event] 2013-11-18に発現し、同日に[Outcome of Adverse Event]が「RECOVERED/RESOLVED」と記録されています。脳死からの同日回復は医学的に考えられません。事象名、転帰、終了日が正確かご確認ください。もし重篤な神経学的イベントが発生していた場合は、詳細な臨床経過と最終的な診断をご報告ください。参加者の安全性に関わる重大な情報、またはデータの正確性に関する重大な疑義のため、緊急にご確認をお願いします。
        *   **EDCに発出するクエリ文面（英語）:** Regarding the AE with Reported Term 'BRAIN DEATH' (AESEQ=3), the Start Date is recorded as 2013-11-18 and the Outcome is 'RECOVERED/RESOLVED' with an End Date of 2013-11-18. Recovery/resolution on the same day as onset for 'BRAIN DEATH' is medically implausible. Please confirm the accuracy of the AE Term, Outcome, and End Date. If a serious neurological event occurred, please provide detailed clinical course and final diagnosis. Urgent confirmation is required due to potential critical impact on patient safety assessment or critical data integrity issue.
        *   **判断理由:** 報告された事象名と転帰の組み合わせが医学的にありえず、重大な安全性イベントの見落とし、またはデータの信頼性を著しく損なう記録エラーの可能性があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Sequence Number(AE.AESEQ)] = 3, [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH', [Severity/Intensity(AE.AESEV)] = 'SEVERE', [Start Date/Time of Adverse Event(AESTDTC)] = '2013-11-18', [End Date/Time of Adverse Event(AEENDTC)] = '2013-11-18', [Outcome of Adverse Event(AEOUT)] = 'RECOVERED/RESOLVED']
            *   [関連する医学的知見: 脳死の定義と予後]
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1, D-9)
        *   **重要度:** Critical
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 本被験者のデモグラフィック情報において、「Date/Time of Informed Consent」が記録されていません。治験実施計画書 Section 5.1 およびGCP遵守の観点から、インフォームド・コンセントが治験関連手順開始前に適切に取得されたことを確認する必要があります。同意取得日時をご提供ください。参加者の権利保護に関する重要な確認事項です。
        *   **EDCに発出するクエリ文面（英語）:** The 'Date/Time of Informed Consent' (RFICDTC) is missing in the Demographics domain for this subject. To ensure compliance with Protocol Section 5.1 and GCP, confirmation is required that informed consent was obtained prior to any study-related procedures. Please provide the date/time of informed consent. This is critical for verifying protection of participant rights.
        *   **判断理由:** 同意取得日の欠損はGCP違反の可能性があり、参加者の権利が保護されているか確認できないため。
        *   **判断根拠:**
            *   [関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '']
            *   [関連するプロトコル箇所: Section 5.1 Informed Consent]
            *   [関連する医学的知見: GCP原則]
    *   **クエリNo.:** Q-3 (関連指摘No.: M-2, D-1)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14に発現した有害事象「Reported Term for the Adverse Event」が「MYOCARDIAL INFARCTION」について、[Severity/Intensity]が「MILD」、[Causality]が「NONE」、[Action Taken with Study Treatment]が「DRUG WITHDRAWN」と記録されています。しかし、翌日Day 15には治験薬が増量されています。心筋梗塞の重症度評価、因果関係評価（患者は心筋梗塞の既往あり）、処置（治験薬中止 vs 増量）の記録に矛盾や疑問点があります。記録内容が正確か、臨床経過と併せて再評価・ご確認ください。特に治験薬の処置に関する記録の整合性をご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** Regarding the AE 'MYOCARDIAL INFARCTION' (AESEQ=1) starting on Day 14 (2013-10-19), the Severity is recorded as 'MILD', Causality as 'NONE', and Action Taken as 'DRUG WITHDRAWN'. However, the EX domain shows a dose increase on the following day (Day 15, 2013-10-20). There are inconsistencies/questions regarding the recorded Severity, Causality assessment (given patient's MH of MI), and Action Taken (Drug Withdrawn vs Dose Increase). Please review the clinical course and confirm the accuracy of these AE details, especially the consistency of the Action Taken record.
        *   **判断理由:** 有害事象の評価と処置に関する記録の矛盾・不整合は、安全性評価の妥当性とデータの信頼性に影響するため。
        *   **判断根拠:**
            *   [関連するデータ: AE(AESEQ=1), EX(EXSEQ=2), MH(MHTERM='HEART ATTACK')]
            *   [関連する医学的知見: 心筋梗塞の重症度、治験薬との関連評価]
    *   **クエリNo.:** Q-4 (関連指摘No.: M-3, D-2)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor/CRA
        *   **医療機関への問い合わせ文面:** Day 50に「Standardized Disposition Term」が「ADVERSE EVENT」により試験中止と記録されています。しかし、AEログからは中止の直接的な原因となった有害事象が特定できません（例：記録されているAEは中止日以前に回復済み、軽微、等）。中止の判断に至った具体的な有害事象名とその臨床的判断についてご確認ください。RELRECではRashが関連付けられていますが軽微で回復済みです。
        *   **EDCに発出するクエリ文面（英語）:** The subject was discontinued from the study due to 'ADVERSE EVENT' (DSDECOD) on Day 50 (2013-11-24) according to the Disposition domain (DSSEQ=1). However, the specific AE leading to discontinuation cannot be clearly identified from the AE log (e.g., recorded AEs resolved before Day 50, were mild, etc.). Please clarify the specific Adverse Event term and clinical reasoning that led to the decision for discontinuation. RELREC links this to Rash AE (AESPID E11), but this was mild and resolved on Day 48.
        *   **判断理由:** 試験中止理由は安全性評価における重要な情報であり、不明確な点はデータの解釈と評価の信頼性に影響するため。
        *   **判断根拠:**
            *   [関連するデータ: DS(DSSEQ=1), AEドメインデータ, RELRECデータ]
            *   [関連するプロトコル箇所: Section 3.10.1 Discontinuations]
    *   **クエリNo.:** Q-5 (関連指摘No.: M-4, P-4)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時の検査で「Lab Test or Examination Short Name」が「CREAT」の値が1.8 mg/dLであり、基準値上限(1.6 mg/dL)を超えています。治験実施計画書 Section 3.4.2.2 除外基準[27b]では、基準値を超える検査値は除外対象となりえます。本件について臨床的に意義がないと判断され、適格と判断された場合、その旨が文書化されている必要があります。適格性評価に関する記録をご確認の上、ご回答ください。
        *   **EDCに発出するクエリ文面（英語）:** The baseline laboratory result for 'Creatinine' (LBTESTCD='CREAT') at Screening 1 was 1.8 mg/dL, which is above the upper reference limit (1.6 mg/dL). Protocol Section 3.4.2.2 Exclusion Criterion [27b] states that lab values exceeding the reference range may lead to exclusion unless judged not clinically significant and documented. Please confirm that the clinical significance of this elevated creatinine level was assessed and documented, confirming the subject's eligibility.
        *   **判断理由:** 除外基準に抵触する可能性のある検査値異常があり、適格性評価の妥当性を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: LB(LBTESTCD='CREAT', LBORRES='1.8', LBORNRHI='1.6', VISIT='SCREENING 1')]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「Reported Name of Drug, Med, or Therapy」が「PREMARIN」について、[Start Date/Time of Medication]が治験薬開始日と同じ2013-10-06と記録されています。治験実施計画書 Section 3.4.2.2 除外基準[31b] v) では、エストロゲン製剤の使用は許可されていますが、登録前3ヶ月間用量が安定している必要があります。Day 1からの開始はこの規定に適合しません。投与開始日の記録が正しいか、また、この逸脱が適格性に与える影響について評価・記録されているかご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** Concomitant medication 'PREMARIN' (CMTRT) is recorded as starting on 2013-10-06 (Day 1), the same day as study treatment initiation. Protocol Section 3.4.2.2 Exclusion Criterion [31b] v) permits estrogen supplements only if the dosage has been stable for at least 3 months prior to enrollment. Starting on Day 1 does not meet this stability requirement. Please confirm the accuracy of the start date and confirm if the impact of this deviation on eligibility was assessed and documented.
        *   **判断理由:** 併用薬に関する除外基準違反の可能性があり、適格性評価の妥当性を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: CM(CMTRT='PREMARIN', CMSTDTC='2013-10-06')]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] v)]
    *   **クエリNo.:** Q-7 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **発行担当者（推定）:** DM/CRA
        *   **医療機関への問い合わせ文面:** Visit 5 (Week 4)について、検査([Lab Test or Examination Short Name]など)の「Date/Time of Specimen Collection」が2013-11-01 (Day 27)と記録されていますが、来院日([Visit Name] = 'WEEK 4')の「Start Date/Time of Visit」は2013-11-09 (Day 35)となっています。検査採取日と来院日が一致していません。どちらの日付が正しいか、または検査がVisit 5とは別のタイミングで実施されたのかご確認ください。データの帰属Visitの正確性を確認する必要があります。
        *   **EDCに発出するクエリ文面（英語）:** For Visit 5 (Week 4), the 'Date/Time of Specimen Collection' (LBDTC) for laboratory tests (e.g., LBTESTCD='ALB') is recorded as 2013-11-01 (Day 27), but the 'Start Date/Time of Visit' (SVSTDTC) for Visit 5 (VISIT='WEEK 4') is recorded as 2013-11-09 (Day 35). The lab collection date does not match the visit date. Please confirm which date is correct, or clarify if the labs were collected at a different time point than Visit 5. Accuracy of data attribution to the visit is required.
        *   **判断理由:** 検査データとVisitデータの日付不整合は、データの時間的関係性の解釈や評価の信頼性に影響するため。
        *   **判断根拠:**
            *   [関連するデータ: LB(VISITNUM=5, LBDTC='2013-11-01T10:45'), SV(VISITNUM=5, SVSTDTC='2013-11-09')]
    *   **クエリNo.:** Q-8 (関連指摘No.: D-4)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/DM
        *   **医療機関への問い合わせ文面:** Dispositionドメインに、「Standardized Disposition Term」が「FINAL LAB VISIT」というイベントがDay 27 (2013-11-01)に記録されています。これはVisit 5 (Week 4)に関連付けられていますが、被験者はその後も試験に参加しています（最終参加日 Day 62）。この「FINAL LAB VISIT」が何を意味するのか、なぜこのタイミングで記録されたのかご確認ください。記録の意図と正確性の確認が必要です。
        *   **EDCに発出するクエリ文面（英語）:** An event with Standardized Disposition Term 'FINAL LAB VISIT' (DSDECOD) is recorded in the Disposition domain (DSSEQ=2) on Day 27 (DSSTDTC=2013-11-01), associated with Visit 5. However, the subject continued participation until Day 62. Please clarify the meaning of this 'FINAL LAB VISIT' event and why it was recorded at this time point. Confirmation of the intent and accuracy of this record is needed.
        *   **判断理由:** 時期尚早と思われるマイルストーン記録は、被験者のステータスやデータ解釈に混乱を招く可能性があるため。
        *   **判断根拠:**
            *   [関連するデータ: DS(DSSEQ=2, DSDECOD='FINAL LAB VISIT', DSSTDTC='2013-11-01'), DM(RFPENDTC='2013-12-06')]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-8)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** Subject Visitsドメインに、Visit 3.5 (Day 13)「AMBUL ECG PLACEMENT」およびVisit 6 (Day 37)「AMBUL ECG REMOVAL」の記録があります。治験実施計画書 Section 3.9.3.4.2ではAmbulatory ECGはVisit 2/3での実施が規定されていますが、この追加実施の理由は何でしょうか？治験実施計画書からの逸脱、または記録エラーの可能性がありますのでご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** The Subject Visits domain records Visit 3.5 'AMBUL ECG PLACEMENT' on Day 13 and Visit 6 'AMBUL ECG REMOVAL' on Day 37. Protocol Section 3.9.3.4.2 specifies Ambulatory ECG collection at Visit 2/3. Please clarify the reason for this additional Ambulatory ECG procedure. This may represent a protocol deviation or a recording error.
        *   **判断理由:** プロトコル規定外の評価手順の実施または記録エラーの可能性があり、プロトコル遵守状況とデータの正確性を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: SV(VISITNUM=3.5, VISIT='AMBUL ECG PLACEMENT'), SV(VISITNUM=6, VISIT='AMBUL ECG REMOVAL')]
            *   [関連するプロトコル箇所: Section 3.1, Section 3.9.3.4.2]
    *   **クエリNo.:** Q-10 (関連指摘No.: M-5, D-5)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor/CRA
        *   **医療機関への問い合わせ文面:** 有害事象として「Reported Term for the Adverse Event」が「LATE EFFECTS OF CEREBRAL INFARCTION」と報告されていますが、Medical Historyには脳梗塞の既往が明記されていません。被験者に脳梗塞/脳卒中の既往歴があるかご確認ください。もし既往歴がある場合、Medical Historyへの追記をご検討ください。もし既往歴がない場合、この有害事象名の診断根拠と詳細をお知らせください。
        *   **EDCに発出するクエリ文面（英語）:** The AE 'LATE EFFECTS OF CEREBRAL INFARCTION' (AETERM) was reported starting Day 14. However, the Medical History domain does not explicitly list a history of cerebral infarction or stroke. Please confirm if the subject has a history of cerebral infarction/stroke. If yes, please consider updating the Medical History domain. If no, please provide the basis for the diagnosis and details of this AE term.
        *   **判断理由:** AEと既往歴の不整合は、AEの評価（新規発現か既往の悪化か）や患者背景の正確な把握に影響するため。
        *   **判断根拠:**
            *   [関連するデータ: AE(AETERM='LATE EFFECTS OF CEREBRAL INFARCTION'), MHドメインデータ]
    *   **クエリNo.:** Q-11 (関連指摘No.: M-6, D-6)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor/CRA
        *   **医療機関への問い合わせ文面:** 有害事象として「Reported Term for the Adverse Event」が「VENTRICULAR SEPTAL DEFECT」とDay 14に発現したと報告されています。心室中隔欠損症は通常先天性であり、治療期間中に発現する有害事象としての報告は適切でない可能性があります。この事象名の報告経緯と診断根拠をご確認ください。既往歴として報告すべき事象ではないでしょうか？
        *   **EDCに発出するクエリ文面（英語）:** The AE 'VENTRICULAR SEPTAL DEFECT' (AETERM) was reported as starting on Day 14. Ventricular Septal Defect is typically a congenital condition, and reporting it as a treatment-emergent AE may be inappropriate. Please confirm the circumstances and diagnostic basis for reporting this term as an AE. Should this have been reported as Medical History instead?
        *   **判断理由:** 先天性疾患を有害事象として報告することはデータの分類として不適切であり、データの正確性と解釈に影響するため。
        *   **判断根拠:**
            *   [関連するデータ: AE(AETERM='VENTRICULAR SEPTAL DEFECT', AESTDTC='2013-10-19')]
            *   [関連する医学的知見: 心室中隔欠損症は先天性疾患]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/DM
        *   **疑義事項/確認内容:** Visit 5 (Week 4) が Day 35 に実施され、プロトコル規定の Visit Window (Day 25-31) から逸脱している。逸脱理由を特定し、評価データ（特にNPI-X）への影響を評価・記録する。
        *   **判断理由:** Visit Window逸脱はプロトコル逸脱に該当するが、医療機関への問い合わせで追加情報が得られる可能性は低く、内部での影響評価と記録が適切と判断したため。
        *   **判断根拠:**
            *   [関連するデータ: SV(VISITNUM=5, SVSTDTC='2013-11-09', VISITDY=28)]
            *   [関連するプロトコル箇所: Section 3.1]
    *   **確認事項No.:** I-2 (関連指摘No.: P-7)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/DM
        *   **疑義事項/確認内容:** Visit 7 (Week 6) が Day 50 に実施され、プロトコル規定の Visit Window (Day 39-45) から逸脱している。逸脱理由を特定し、評価データ（ADAS-Cog, CIBIC+, DAD, NPI-X）への影響を評価・記録する。
        *   **判断理由:** Visit Window逸脱はプロトコル逸脱に該当するが、医療機関への問い合わせで追加情報が得られる可能性は低く、内部での影響評価と記録が適切と判断したため。
        *   **判断根拠:**
            *   [関連するデータ: SV(VISITNUM=7, SVSTDTC='2013-11-24', VISITDY=42)]
            *   [関連するプロトコル箇所: Section 3.1]
    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **疑義事項/確認内容:** 患者の心血管系既往歴（MI 2000年, Bypass 2006年等）と除外基準[17]（過去5年以内の重篤な心血管系障害）との関連について、適格性評価の根拠を内部で再確認・文書化する。特にDay 14のMI AE報告を踏まえ、スクリーニング時の評価が適切であったかを確認する。
        *   **判断理由:** 適格性に関する重要な判断であり、内部での評価根拠の明確化が必要なため。医療機関への問い合わせでは、当時の判断根拠の詳細な再現が困難な可能性がある。
        *   **判断根拠:**
            *   [関連するデータ: MHドメインデータ, AE(AETERM='MYOCARDIAL INFARCTION')]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]]
    *   **確認事項No.:** I-4 (関連指摘No.: M-7)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** Medical Monitor/DM
        *   **疑義事項/確認内容:** Day 14およびDay 27に軽度のアルブミン低値を認めた。臨床的意義は現時点で不明。他の症例でも同様の傾向がないか、全体データで確認する。本症例については特段のアクション不要。
        *   **判断理由:** 軽微な検査値異常であり、現時点で臨床的意義が低く、緊急性がないため内部確認事項とする。
        *   **判断根拠:**
            *   [関連するデータ: LB(LBTESTCD='ALB', LBNRIND='LOW', LBDY=14, 27)]
    *   **確認事項No.:** I-5 (関連指摘No.: M-8)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** Medical Monitor/DM
        *   **疑義事項/確認内容:** Day 14に一過性のBUN高値を認めた。Day 27には正常化。臨床的意義は低いと考えられる。他の症例でも同様の傾向がないか、全体データで確認する。本症例については特段のアクション不要。
        *   **判断理由:** 一過性で軽微な検査値異常であり、臨床的意義が低く、緊急性がないため内部確認事項とする。
        *   **判断根拠:**
            *   [関連するデータ: LB(LBTESTCD='BUN', LBNRIND='HIGH', LBDY=14), LB(LBTESTCD='BUN', LBNRIND='NORMAL', LBDY=27)]
    *   **確認事項No.:** I-6 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **疑義事項/確認内容:** RELRECデータにおけるRash AEとAEによる中止の関連付け([Relationship Identifier(RELREC.RELID)] = '01-704-1017-E11')について、時間経過や重症度からみて臨床的な関連性は低い可能性があることを記録する。データの関連付けロジックを確認する必要があるかもしれない。
        *   **判断理由:** データ間の関連付けに関する疑問点だが、主要な評価への影響は限定的と考えられ、内部での確認・記録に留める。
        *   **判断根拠:**
            *   [関連するデータ: RELRECデータ, AE(AESEQ=5, 7), DS(DSSEQ=1)]
    *   **確認事項No.:** I-7 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** ベースラインNPI-Xでうつ症状が報告されていた点について、除外基準[13]（DSM-IV基準）との関連で適格性が評価されたことを内部で確認・記録する。
        *   **判断理由:** 適格性に関する確認だが、MMSEスコアや他の基準を満たしており、NPI-Xスコアのみで不適格となる可能性は低いため、内部確認とする。
        *   **判断根拠:**
            *   [関連するデータ: QS(QSTESTCD='NPITM04S', QSSTRESN=9, QSBLFL='Y')]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [13]]

# [01-703-1042]のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    [Age(AGE)]は 64歳、[Sex(SEX)]は男性、[Race(RACE)]はWHITE、[Ethnicity(ETHNIC)]はNOT HISPANIC OR LATINO。教育歴 ([EDUCATION LEVEL(SCTEST)]) は 12年。主な既往歴として、[Reported Term for the Medical History(MHTERM)] = 'ALZHEIMER'S DISEASE' (Primary Diagnosis, 2008年発症)、[Reported Term for the Medical History(MHTERM)] = 'EMPHYSEMA' (Mild)、[Reported Term for the Medical History(MHTERM)] = 'CORONARY ARTERY DISEASE' (Mild)、[Reported Term for the Medical History(MHTERM)] = 'ARTHRITIS' (Mild) がある。
*   **イベント推移:**
    *   2012年12月27日 (Day -65): Screening 1 Visit時の検査にて、[Alanine Aminotransferase(LBTEST='Alanine Aminotransferase')] = 135 U/L (HIGH)、[Aspartate Aminotransferase(LBTEST='Aspartate Aminotransferase')] = 145 U/L (HIGH) を認めた。
    *   2013年02月21日 (Day -9): Unscheduled Visit 1.1。検査にて、[Alanine Aminotransferase(LBTEST='Alanine Aminotransferase')] = 19 U/L (NORMAL)、[Aspartate Aminotransferase(LBTEST='Aspartate Aminotransferase')] = 29 U/L (NORMAL) と改善。[Sodium(LBTEST='Sodium')] = 133 mmol/L (LOW) を認めた。
    *   2013年03月02日 (Day 1): Baseline Visit。Placebo投与開始。[ADAS-COG(11) Subscore(QSTEST='ADAS-COG(11) Subscore')] = 14。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 3。[Diastolic Blood Pressure(VSTEST='Diastolic Blood Pressure')] (Supine) = 56 mmHg、[Systolic Blood Pressure(VSTEST='Systolic Blood Pressure')] (Supine) = 130 mmHg、[Pulse Rate(VSTEST='Pulse Rate')] (Supine) = 60 bpm。
    *   2013年03月04日 (Day 3): 有害事象 [Reported Term for the Adverse Event(AETERM)] = 'DIARRHOEA' ([Severity/Intensity(AESEV)] = MILD) 発現。治験薬との関連 [Causality(AEREL)] = POSSIBLE。
    *   2013年03月05日 (Day 4): 有害事象 [Reported Term for the Adverse Event(AETERM)] = 'DIARRHOEA' 消失 ([Outcome of Adverse Event(AEOUT)] = RECOVERED/RESOLVED)。同日、有害事象 [Reported Term for the Adverse Event(AETERM)] = 'INSOMNIA' ([Severity/Intensity(AESEV)] = MILD) 発現。治験薬との関連 [Causality(AEREL)] = REMOTE。併用薬 [Reported Name of Drug, Med, or Therapy(CMTRT)] = 'KAOPECTATE' を下痢に対して1回投与。
    *   2013年03月06日 (Day 5): 有害事象 [Reported Term for the Adverse Event(AETERM)] = 'INSOMNIA' 消失 ([Outcome of Adverse Event(AEOUT)] = RECOVERED/RESOLVED)。
    *   2013年03月14日 (Day 13): Week 2 Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 6。
    *   2013年03月28日 (Day 27): Week 4 Visit。[Ery. Mean Corpuscular Volume(LBTEST='Ery. Mean Corpuscular Volume')] = 101 fL (HIGH)、[Sodium(LBTEST='Sodium')] = 146 mmol/L (HIGH)、[Anisocytes(LBTEST='Anisocytes')] = 1 (ABNORMAL)。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 4。
    *   2013年04月27日 (Day 57): Week 8 Visit。[ADAS-COG(11) Subscore(QSTEST='ADAS-COG(11) Subscore')] = 9。
    *   2013年05月11日 (Day 71): Week 10 (T) Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 4。
    *   2013年05月25日 (Day 85): Week 12 Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 6。
    *   2013年06月08日 (Day 99): Week 14 (T) Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 6。
    *   2013年06月22日 (Day 113): Week 16 Visit。[ADAS-COG(11) Subscore(QSTEST='ADAS-COG(11) Subscore')] = 7。[EXTENT OF CHANGE, IF ANY, SINCE BASELINE(QSTEST='EXTENT OF CHANGE, IF ANY, SINCE BASELINE')] (CIBIC+) = 4 (NO CHANGE)。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 4。
    *   2013年07月06日 (Day 127): Week 18 (T) Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 4。
    *   2013年07月20日 (Day 141): Week 20 Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 4。
    *   2013年08月03日 (Day 155): Week 22 (T) Visit。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 3。
    *   2013年08月09日 (Day 161): Week 24 Visit (計画日Day 168より7日早い)。[ADAS-COG(11) Subscore(QSTEST='ADAS-COG(11) Subscore')] = 9。[EXTENT OF CHANGE, IF ANY, SINCE BASELINE(QSTEST='EXTENT OF CHANGE, IF ANY, SINCE BASELINE')] (CIBIC+) = 4 (NO CHANGE)。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 2。
    *   2013年08月31日 (Day 183): Week 26 Visit。治験完了 ([Standardized Disposition Term(DSDECOD)] = COMPLETED)。[Aspartate Aminotransferase(LBTEST='Aspartate Aminotransferase')] = 38 U/L (HIGH)。[NPI-X (9) Total Score(QSTEST='NPI-X (9) Total Score')] = 2。

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Minor
        *   **内容:** 患者は既往歴として冠動脈疾患 ([Reported Term for the Medical History(MHTERM)] = 'CORONARY ARTERY DISEASE') が報告されているが、高血圧の既往歴 ([Reported Term for the Medical History(MHTERM)]) はなく、Modified Hachinski Ischemic Scoreの質問 ([Question Short Name(QSTESTCD)] = 'MHITM09') でも高血圧歴は「ABSENT」とされている。一方で、併用薬として降圧薬であるノルバスク（アムロジピン）([Reported Name of Drug, Med, or Therapy(CMTRT)] = 'NORVASC') を治験開始前から継続して使用している。ノルバスクが冠動脈疾患の治療目的で使用されている可能性も考えられるが、適応症 ([Indication(CMINDC)]) が記録されていないため不明確である。背景情報の整合性として確認が望ましい。
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE', [Severity/Intensity(MH.MHSEV)] = 'MILD'; [Question Short Name(QS.QSTESTCD)] = 'MHITM09', [Finding in Original Units(QS.QSORRES)] = 'ABSENT'; [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-01-27', [Indication(CM.CMINDC)] = '' (欠損)。一般的な医学的知見として、アムロジピンは高血圧および狭心症に適応がある。
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Screening 1 (Day -65) の検査で、[Alanine Aminotransferase(LBTEST='Alanine Aminotransferase')] = 135 U/L、[Aspartate Aminotransferase(LBTEST='Aspartate Aminotransferase')] = 145 U/L と基準値上限 (ALT: 43 U/L, AST: 36 U/L) を超える高値を認めている。これは除外基準 [27b] 「Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes: ... ↑ SGOT, ↑ SGPT」に抵触する可能性がある。Unscheduled Visit 1.1 (Day -9) では正常化しているが、Screening時の異常値に対する臨床的意義の評価（例：一過性で臨床的に問題なし）と、それに基づく適格性判断の記録が確認できない。参加者の安全確保とプロトコル遵守の観点から確認が必要。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 43, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65; Protocol Section 3.4.2.2 [27b]。
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 27) に [Ery. Mean Corpuscular Volume(LBTEST='Ery. Mean Corpuscular Volume')] = 101 fL (HIGH, 基準上限 100)、[Sodium(LBTEST='Sodium')] = 146 mmol/L (HIGH, 基準上限 145)、[Anisocytes(LBTEST='Anisocytes')] = 1 (ABNORMAL) が認められた。また、Week 26 (Day 183) に [Aspartate Aminotransferase(LBTEST='Aspartate Aminotransferase')] = 38 U/L (HIGH, 基準上限 36) が認められた。いずれも基準値からの逸脱は軽微であり、関連する有害事象も報告されていないため、臨床的な意義は低い可能性が高いが、念のため記録する。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 100, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 27; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 146, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 27; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '1', [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL', [Study Day of Specimen Collection(LB.LBDY)] = 27; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 38, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 183。AEドメインに関連する有害事象の報告なし。
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** 有効性評価項目のDAD (Disability Assessment for Dementia) の一部項目において、ベースラインからWeek 24にかけて一貫性のない変動が見られる（例: DAITM20, DAITM24, DAITM29, DAITM30, DAITM31, DAITM32, DAITM33, DAITM34, DAITM37, DAITM38, DAITM39）。プラセボ群であり、評価者や患者の状態による変動の可能性も考えられるため、現時点では大きな懸念とは判断しないが、記録として残す。
        *   **根拠:** QSドメインの[Category of Question(QSCAT)] = 'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)' の各項目 ([Question Short Name(QSTESTCD)] = DAITMxx) の[Numeric Finding in Standard Units(QSSTRESN)] の経時変化。

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** Visit 12 (Week 24) の実施日 ([Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09') は Study Day 161 に相当する。これは計画された Study Day ([Planned Study Day of Visit(SV.VISITDY)] = 168) から7日早く、プロトコルで規定された Visit Window (±4日) を逸脱している可能性がある。有効性評価の信頼性に影響する可能性があるため、逸脱理由の確認が必要。
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 12, [Visit Name(SV.VISIT)] = 'WEEK 24', [Planned Study Day of Visit(SV.VISITDY)] = 168, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09' (Day 161)。Protocol Section 3.1 「Visits 9, 10, 11, and 12 should occur within 4 days of their scheduled date.」
    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** 同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) がDMドメインに記録されていない。同意取得は治験参加の前提であり、GCP遵守の観点から極めて重要。同意取得日とその記録の確認が必要。
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)。GCP原則。
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** Screening 1 Visit ([Visit Name(SV.VISIT)] = 'SCREENING 1') の実施日 ([Start Date/Time of Visit(SV.SVSTDTC)] = '2013-02-23', Day -7) に対し、同Visitで実施されたはずの臨床検査 (LB) の検体採取日 ([Date/Time of Specimen Collection(LB.LBDTC)]) が '2012-12-27T12:45' (Day -65) と記録されており、Visit実施日と大きく乖離している。Screening検査がVisit期間外で行われた可能性があり、プロトコル遵守およびデータ品質の観点から確認が必要。
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 1, [Visit Name(SV.VISIT)] = 'SCREENING 1', [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-02-23'; [Visit Number(LB.VISITNUM)] = 1, [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45', [Study Day of Specimen Collection(LB.LBDY)] = -65。
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** AE, MH, CMドメインにおいて、MedDRAコードやWHODrugコード、ATC分類などのコーディング関連変数 ([Lowest Level Term Code(AE.AELLTCD)], [Preferred Term Code(AE.AEPTCD)], [High Level Term Code(AE.AEHLTCD)], [High Level Group Term Code(AE.AEHLGTCD)], [Body System or Organ Class Code(AE.AEBDSYCD)], [Primary System Organ Class Code(AE.AESOCCD)], [Dictionary-Derived Term(MH.MHDECOD)], [Standardized Medication Name(CM.CMDECOD)], [Medication Class(CM.CMCLAS)] など) が一部欠損している。また、CMの適応症 ([Indication(CM.CMINDC)]) も一部欠損している。データクリーニングプロセスでの確認が必要。
        *   **根拠:** AE, MH, CMドメインの各変数における欠損値。

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [27b] 違反の可能性。Screening 1 (Day -65) の検査で ALT (135 U/L), AST (145 U/L) が基準値上限を超過していた。プロトコルでは臨床的に意義がないと判断されれば組み入れ可能とあるが、その判断記録が不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 43, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65。
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準 [3] 違反の可能性。MMSEスコア (10-23) が選択基準であるが、QSドメインにMMSEの評価記録が見当たらない。適格性の確認ができない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [3]
        *   **根拠:** QSドメインに [Question Short Name(QSTESTCD)] = 'MMITMxx' のレコードが存在しない。
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準 [5] 違反の可能性。1年以内のCNS imaging (CT or MRI) がADと矛盾しないことが選択基準であるが、実施記録や結果に関する情報がデータに含まれていない。適格性の確認ができない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5]
        *   **根拠:** 関連するデータドメイン（例: Procedures (PR)など、もし存在すれば）に記録がない。
    *   **指摘No.:** P-4
        *   **重要度:** Critical
        *   **逸脱の可能性:** 選択基準 [6] 違反の可能性。同意取得が選択基準であるが、同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) が記録されていない。GCP違反の可能性。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [6], Section 5.1
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)。
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [16b] 違反の可能性。Screening ECGで特定の所見がないことが除外基準であるが、ECGの実施記録や結果に関する情報がデータに含まれていない。適格性の確認ができない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [16b]
        *   **根拠:** 関連するデータドメイン（例: ECG Test Results (EG)など、もし存在すれば）に記録がない。
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [17] 違反の可能性。5年以内の重篤な心血管疾患が除外基準であるが、患者は冠動脈疾患 ([Reported Term for the Medical History(MHTERM)] = 'CORONARY ARTERY DISEASE', [Severity/Intensity(MHSEV)] = 'MILD') の既往を持つ。これがプロトコル上の "serious cardiovascular disorder" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17]
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE', [Severity/Intensity(MH.MHSEV)] = 'MILD'。
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [20] 違反の可能性。5年以内の重篤な呼吸器疾患が除外基準であるが、患者は肺気腫 ([Reported Term for the Medical History(MHTERM)] = 'EMPHYSEMA', [Severity/Intensity(MHSEV)] = 'MILD') の既往を持つ。これがプロトコル上の "serious respiratory disorder" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [20]
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'EMPHYSEMA', [Severity/Intensity(MH.MHSEV)] = 'MILD'。
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [22] 違反の可能性。5年以内の重篤なリウマチ性疾患が除外基準であるが、患者は関節炎 ([Reported Term for the Medical History(MHTERM)] = 'ARTHRITIS', [Severity/Intensity(MHSEV)] = 'MILD') の既往を持つ。これがプロトコル上の "serious rheumatologic disorder" に該当しないかの確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [22]
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', [Severity/Intensity(MH.MHSEV)] = 'MILD'。
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [28b] 違反の可能性。Screening時のFolateが基準値以下でないことが除外基準であるが、LBドメインにFolateの検査結果が見当たらない。適格性の確認ができない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [28b]
        *   **根拠:** LBドメインに [Lab Test or Examination Short Name(LBTESTCD)] = 'FOLATE' のレコードが存在しない。
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [29b] 違反の可能性。梅毒スクリーニング陽性が除外基準であるが、検査結果に関する情報がデータに含まれていない。適格性の確認ができない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [29b]
        *   **根拠:** 関連するデータドメイン（例: LBなど）に記録がない。
    *   **指摘No.:** P-11
        *   **重要度:** Major
        *   **逸脱の可能性:** 評価スケジュールの逸脱。Visit 12 (Week 24) の実施日が計画日 (Day 168) に対し7日早く (Day 161)、プロトコル規定の Visit Window (±4日) を逸脱している。
        *   **プロトコル該当箇所:** Section 3.1
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 12, [Visit Name(SV.VISIT)] = 'WEEK 24', [Planned Study Day of Visit(SV.VISITDY)] = 168, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09' (Day 161)。
    *   **指摘No.:** P-12
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening手順の逸脱の可能性。Screening 1 Visit (Day -7) の臨床検査 (LB) 検体採取日が Visit 実施日より大幅に前 (Day -65) である。Screening検査は通常、同意取得後、規定されたScreening期間内に実施されるべき。
        *   **プロトコル該当箇所:** Section 3.1 (Screening期間に関する規定), Section 5.1 (同意取得)
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 1, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-02-23'; [Visit Number(LB.VISITNUM)] = 1, [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45'。
    *   **指摘No.:** P-13
        *   **重要度:** Critical
        *   **逸脱の可能性:** 安全性評価の未実施の可能性。プロトコルでは、Screening (Visit 1) および複数の治療期Visitで12誘導心電図 (ECG) の実施、Visit 2で24時間ホルター心電図 (Ambulatory ECG) の実施が規定されているが、これらのデータが見当たらない。心血管系の安全性評価は本試験において重要であり、未実施であれば重大なプロトコル逸脱となる。
        *   **プロトコル該当箇所:** Section 3.9.3.1, Section 3.9.3.4.2, Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 関連するデータドメイン（例: EGなど）に記録がない。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-2, P-4)
        *   **重要度:** Critical
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、インフォームド・コンセントの取得日が記録されておりません。GCP遵守のため、同意取得日を確認し、記録をお願いいたします。同意取得前に治験関連手順が開始されていないかも併せてご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, the Date/Time of Informed Consent (RFICDTC) is missing in the DM domain. Please confirm the date of informed consent and update the record accordingly. Please also confirm that no study-related procedures were performed before informed consent was obtained. This is critical for GCP compliance.
        *   **判断理由:** 同意取得は治験参加の大前提であり、記録の欠損はGCP違反の可能性があるため、緊急の確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.1 [6], Section 5.1]
            *   [関連する医学的知見: GCP原則]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, P-1)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、Screening 1 Visit時の検査 (2012-12-27実施) でアラニンアミノトランスフェラーゼが 135 U/L、アスパラギン酸アミノトランスフェラーゼが 145 U/L と基準値を超えていました。これは除外基準[27b]に抵触する可能性があります。Unscheduled Visit (2013-02-21実施) では正常化していますが、Screening時の異常値に対する臨床的意義の評価（例：臨床的に意義なし）と、それに基づく適格性判断の根拠について、カルテ等の記録を確認し、ご回答ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, lab results from Screening 1 visit (collected on 2012-12-27) show elevated ALT (135 U/L) and AST (145 U/L), exceeding the upper limits of normal (ALT: 43 U/L, AST: 36 U/L). This potentially violates exclusion criterion [27b]. Although values normalized at the Unscheduled Visit (2013-02-21), please confirm the clinical significance assessment for the screening abnormalities (e.g., 'not clinically significant') and the basis for the eligibility decision, referencing source documents.
        *   **判断理由:** 除外基準に抵触する可能性のある検査値異常がScreening時に認められており、適格性判断の根拠を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65; [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = -65]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.2 [27b]]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-13)
        *   **重要度:** Critical
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、プロトコルで規定されている12誘導心電図 (ECG) および24時間ホルター心電図 (Ambulatory ECG) の実施記録が見当たりません。これらの検査が実施されたか、結果を含めてご確認ください。未実施の場合はその理由をお知らせください。心血管系の安全性評価は本試験で重要です。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, there are no records for the protocol-specified 12-lead ECGs and the 24-hour Ambulatory ECG (scheduled at Visit 2). Please confirm if these assessments were performed and provide the results. If not performed, please provide the reason. Cardiovascular safety assessment is critical in this study.
        *   **判断理由:** プロトコルで規定された重要な安全性評価が実施されたか不明であり、確認が必要なため。
        *   **判断根拠:**
            *   [関連するデータ: ECG/Ambulatory ECGデータなし]
            *   [関連するプロトコル箇所: Protocol Section 3.9.3.1, 3.9.3.4.2, Attachment LZZT.1]
    *   **クエリNo.:** Q-4 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、選択基準[3]であるMMSEスコア (10-23) の評価記録が見当たりません。Screening時にMMSEが実施されたか、スコアを含めてご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, the MMSE assessment record, required by inclusion criterion [3] (score 10-23), is missing in the QS domain. Please confirm if MMSE was performed during screening and provide the score.
        *   **判断理由:** 主要な選択基準の遵守状況を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: QSドメインにMMSEデータなし]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.1 [3]]
    *   **クエリNo.:** Q-5 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、選択基準[5]である1年以内のCNS imaging (CT or MRI) の実施記録および結果（ADと矛盾しないこと）に関する情報が見当たりません。実施状況と結果の確認をお願いいたします。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, information regarding CNS imaging (CT or MRI) performed within 1 year prior to screening, as required by inclusion criterion [5], is missing. Please confirm if imaging was performed and that the results were compatible with AD.
        *   **判断理由:** 主要な選択基準の遵守状況を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: 関連データなし]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.1 [5]]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、除外基準[16b]に関連するScreening ECGの結果情報が見当たりません。ECGが実施され、除外基準に該当する所見がなかったかご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, results for the Screening ECG, required to confirm non-violation of exclusion criterion [16b], are missing. Please confirm that the ECG was performed and that no exclusionary findings were present.
        *   **判断理由:** 安全性に関する除外基準の遵守状況を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: ECGデータなし]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.2 [16b]]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-6, P-7, P-8)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者ID 1042は、既往歴として冠動脈疾患 (Mild)、肺気腫 (Mild)、関節炎 (Mild) が報告されています。これらがそれぞれ除外基準[17] (serious cardiovascular disorder)、[20] (serious respiratory disorder)、[22] (serious rheumatologic disorder) に該当しないと判断された根拠について、カルテ等の記録を確認し、ご回答ください。
        *   **EDCに発出するクエリ文面（英語）:** Subject 1042 has a medical history of Coronary Artery Disease (Mild), Emphysema (Mild), and Arthritis (Mild). Please confirm the basis for determining that these conditions did not meet the definition of "serious" disorders as specified in exclusion criteria [17], [20], and [22], respectively, referencing source documents.
        *   **判断理由:** 除外基準の遵守状況（既往歴の重症度評価）を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'CORONARY ARTERY DISEASE', [Severity/Intensity(MH.MHSEV)] = 'MILD'; [Reported Term for the Medical History(MH.MHTERM)] = 'EMPHYSEMA', [Severity/Intensity(MH.MHSEV)] = 'MILD'; [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', [Severity/Intensity(MH.MHSEV)] = 'MILD']
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.2 [17], [20], [22]]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-9)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、除外基準[28b]に関連するScreening時のFolate検査結果が見当たりません。検査が実施され、基準値を下回っていなかったかご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, the Folate lab result from screening, required to confirm non-violation of exclusion criterion [28b], is missing. Please confirm if the test was performed and that the result was not below the reference range.
        *   **判断理由:** 除外基準の遵守状況を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: LBドメインにFolateデータなし]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.2 [28b]]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-10)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、除外基準[29b]に関連する梅毒スクリーニング検査の結果情報が見当たりません。検査が実施され、陽性でなかったかご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, results for the Syphilis screening, required to confirm non-violation of exclusion criterion [29b], are missing. Please confirm if the test was performed and that the result was not positive.
        *   **判断理由:** 除外基準の遵守状況を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: 関連データなし]
            *   [関連するプロトコル箇所: Protocol Section 3.4.2.2 [29b]]
    *   **クエリNo.:** Q-10 (関連指摘No.: D-1, P-11)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、Visit 12 (Week 24) の実施日 (2013-08-09, Study Day 161) が、計画日 (Study Day 168) より7日早く、プロトコルで規定された Visit Window (±4日) を逸脱しています。逸脱理由についてご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, Visit 12 (Week 24) was conducted on 2013-08-09 (Study Day 161), which is 7 days earlier than the planned Study Day 168 and outside the protocol-specified visit window (±4 days). Please confirm the reason for this deviation.
        *   **判断理由:** プロトコルからの逸脱であり、有効性評価の信頼性に影響する可能性があるため、理由を確認する必要がある。
        *   **判断根拠:**
            *   [関連するデータ: [Visit Number(SV.VISITNUM)] = 12, [Planned Study Day of Visit(SV.VISITDY)] = 168, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09']
            *   [関連するプロトコル箇所: Protocol Section 3.1]
    *   **クエリNo.:** Q-11 (関連指摘No.: D-3, P-12)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、Screening 1 Visit (2013-02-23実施) の臨床検査検体採取日が 2012-12-27 と記録されており、Visit実施日と大きく異なります。検体採取日およびVisit日の記録が正しいか、またScreening手順が適切に行われたかご確認ください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, the specimen collection date for Screening 1 labs is recorded as 2012-12-27, which is significantly different from the Screening 1 visit date (2013-02-23). Please verify the accuracy of both dates and confirm that screening procedures were conducted appropriately.
        *   **判断理由:** データ品質およびプロトコル遵守の観点から確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: [Visit Number(SV.VISITNUM)] = 1, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-02-23'; [Visit Number(LB.VISITNUM)] = 1, [Date/Time of Specimen Collection(LB.LBDTC)] = '2012-12-27T12:45']
            *   [関連するプロトコル箇所: Protocol Section 3.1, 5.1]
    *   **クエリNo.:** Q-12 (関連指摘No.: M-1)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **医療機関への問い合わせ文面:** 患者ID 1042について、併用薬ノルバスク ([Reported Name of Drug, Med, or Therapy(CMTRT)] = 'NORVASC') の適応症 ([Indication(CMINDC)]) が記録されていません。可能であれば適応症（例：冠動脈疾患治療）を追記してください。
        *   **EDCに発出するクエリ文面（英語）:** For Subject 1042, the Indication (CMINDC) for the concomitant medication 'NORVASC' is missing. If available, please provide the indication (e.g., treatment for Coronary Artery Disease).
        *   **判断理由:** 背景情報の補足のため。
        *   **判断根拠:**
            *   [関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC', [Indication(CM.CMINDC)] = '' (欠損)]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** Medical Monitor
        *   **疑義事項/確認内容:** Week 4にMCV高値、Sodium高値、Anisocytes異常、Week 26に軽度のAST高値が認められたが、いずれも逸脱は軽微で一過性または臨床的に大きな変動ではなく、関連するAEも報告されていない。現時点では追加のアクションは不要と判断するが、今後のレビューでも同様の所見がないか注意する。
        *   **判断理由:** 臨床的な影響が小さいと考えられるため、医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   [関連するデータ: LBドメインの該当レコード (M-3参照)]
            *   [関連する医学的知見: 軽微な検査値異常の臨床的意義]
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **疑義事項/確認内容:** AE, MH, CMドメインでコーディング関連変数や適応症が一部欠損している。データマネジメントプロセスにおいて、コーディングの完了状況を確認し、必要に応じて修正・追記を行う。
        *   **判断理由:** データクリーニングの一環として内部で対応可能であり、現時点で安全性や評価の信頼性に大きな影響はないと判断されるため。
        *   **判断根拠:**
            *   [関連するデータ: AE, MH, CMドメインの欠損値 (D-4参照)]
    *   **確認事項No.:** I-3 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** Medical Monitor / Statistician
        *   **疑義事項/確認内容:** DADスコアの一部の項目で一貫性のない変動が見られる。プラセボ群であり、評価のばらつきや患者の状態変動による影響も考えられる。統計解析時にデータ全体の傾向を確認する。
        *   **判断理由:** プラセボ群のデータであり、個別の変動に対する問い合わせは不要と判断。全体的な傾向は統計解析で評価されるため。
        *   **判断根拠:**
            *   [関連するデータ: QSドメインのDAD関連レコード (M-4参照)]

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 81歳、性別は女性、人種は白色人種、民族はヒスパニックまたはラテン系ではなく、計画された投与群および実際の投与群は Xanomeline Low Dose であった。主要診断はアルツハイマー病 (2009年発症)。主な既往歴として、高血圧、甲状腺機能低下症、関節炎、骨粗鬆症、白内障手術歴、基底細胞癌 (2007年)、難聴、耳鳴などがある。主な継続併用薬として、Lisinopril (高血圧)、Synthroid (甲状腺機能低下症)、Premarin/Provera (ホルモン補充療法?)、Keflex (適応不明)、Motrin (PRN) がある。
*   **イベント推移:**
    *   2012年08月25日 (Day -13): スクリーニング検査実施。MMSEスコア 23点、Hachinskiスコア 1点。ベースライン検査にて、[Erythrocytes(RBC)] = 3.80 (基準値 3.9-5.5, LOW)。
    *   2012年09月02日 (Day -5): 有害事象「ERYTHEMA」(Mild) および「PRURITUS」(Mild) 発現 (治験薬との関連性なし)。
    *   2012年09月02日-04日 (Day -5 to -3): 併用薬「HYDROCORTISONE, TOPICAL」使用。
    *   2012年09月07日 (Day 1): 治験薬 Xanomeline 54mg Patch 投与開始。ベースライン評価実施。ADAS-Cog(11) スコア 7。NPI-X Total スコア 2 (Agitation/Aggression Score=1, Disinhibition Score=1)。有害事象「MICTURITION URGENCY」(Mild) 発現 (治験薬との関連性なし)。有害事象「ERYTHEMA」「PRURITUS」寛解。
    *   2012年09月13日 (Day 7): 有害事象「ARTHRALGIA」(Moderate) および「CELLULITIS」(Moderate) 発現 (いずれも治験薬との関連性なし)。
    *   2012年09月16日 (Day 10): 治験薬投与終了。
    *   2012年09月17日 (Day 11): Week 2 Visit 評価実施。ADAS-Cog(11) スコア 5 (ベースラインから改善)。CIBIC+ スコア 4 (No Change)。NPI-X Total スコア 1 (Disinhibition Score=1, ベースラインから改善)。検査にて [Ery. Mean Corpuscular Volume(MCV)] = 101 (基準値 80-100, HIGH)、[Erythrocytes(RBC)] = 3.70 (基準値 3.9-5.5, LOW)、[Specific Gravity(SPGRAV)] = 1.004 (基準値 1.006-1.03, LOW)、[Anisocytes(ANISO)] = 1 (ABNORMAL)。有害事象「ARTHRALGIA」「CELLULITIS」「MICTURITION URGENCY」は未寛解。有害事象により治験中止。
    *   2012年09月29日 (Day 23?): AE Follow-up Visit 実施 (Planned Study Day 不明)。
    *   2013年02月22日 (Day 169): Retrieval Visit 評価実施。ADAS-Cog(11) スコア 9 (Week 2から悪化、ベースラインより悪化)。CIBIC+ スコア 5 (Minimal worsening)。NPI-X Total スコア 45 (Week 2から著しく悪化、妄想、興奮/攻撃性、抑うつ、不安、脱抑制、易刺激性が出現/悪化)。

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象「ARTHRALGIA」(関節痛) の治験薬との関連性が「NONE」と評価されているが、既往歴に「ARTHRITIS」(関節炎) があり、その悪化の可能性や、頻度は低いものの治験薬 (Xanomeline) の影響も完全には否定できない。関連性評価の再検討が必要ではないか。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Causality(AE.AEREL)] = 'NONE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-13'(Day 7). [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS', [Severity/Intensity(MH.MHSEV)] = 'MILD'. 一般的な医学的知見として、Xanomelineのようなコリン作動薬で関節痛は典型的ではないが、薬剤起因性の可能性は常に考慮すべき。
    *   **指摘No.:** M-2
        *   **重要度:** Critical
        *   **内容:** Day 11 に有害事象により治験中止 ([Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT') と記録されているが、中止の原因となった可能性のある有害事象「ARTHRALGIA」および「CELLULITIS」の治験薬との関連性 ([Causality(AE.AEREL)]) がいずれも「NONE」と評価されている。中止判断の根拠となった事象とその評価に矛盾がある可能性があり、参加者の安全性評価とデータの信頼性に重大な影響を与えうる。中止判断に至った詳細な経緯（どのAEが主因か、重症度の推移、医師の判断根拠など）の確認が必要。
        *   **根拠:** [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-09-17'(Day 11). [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Causality(AE.AEREL)] = 'NONE'. [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS', [Causality(AE.AEREL)] = 'NONE'. RELRECデータによると、AE SEQ=7 (ARTHRALGIA) のみが DS SEQ=1 (ADVERSE EVENT) と関連付けられている。
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「MICTURITION URGENCY」(尿意切迫) の治験薬との関連性が「NONE」と評価されている。Xanomeline はムスカリン作動薬であり、膀胱収縮作用を介して尿意切迫を引き起こす可能性があるため、関連性評価の再検討が必要ではないか。既往歴に「INCONTINENCE」もある。
        *   **根拠:** [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY', [Severity/Intensity(AE.AESEV)] = 'MILD', [Causality(AE.AEREL)] = 'NONE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-07'(Day 1). [Reported Term for the Medical History(MH.MHTERM)] = 'INCONTINENCE', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2006'. 一般的な医学的知見として、ムスカリン作動薬は泌尿器系への影響（頻尿、尿意切迫など）がありうる。
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11) の検査で [Ery. Mean Corpuscular Volume(LB.MCV)] = 101 (HIGH) および [Erythrocytes(LB.RBC)] = 3.70 (LOW) が認められ、大球性貧血が示唆される。ベースライン (Day -13) でも [Erythrocytes(LB.RBC)] = 3.80 で基準下限付近であった。高齢者であり、ビタミンB12や葉酸欠乏のリスクも考慮される。臨床的意義について評価し、必要であればフォローアップ検査（ビタミンB12、葉酸など）の実施を検討すべき。
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 11. [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.70, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 11. [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.80, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = -13. 一般的な医学的知見として、MCV高値とRBC低値は大球性貧血を示唆する。

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「ERYTHEMA」が AESEQ=1 と AESEQ=4 で、「PRURITUS」が AESEQ=2 と AESEQ=5 で、それぞれ2回記録されている。開始日は同じ (Day -5) だが、収集日と終了日が異なる。同一イベントの再評価か、データ入力エラーの可能性がある。データの重複や評価の混乱を招く可能性があるが、治験薬投与前の事象であり、安全性評価への大きな影響は限定的と考えられる。
        *   **根拠:** [Sequence Number(AE.AESEQ)] = 1, [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-02', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07', [Date/Time of Collection(AE.AEDTC)] = '2012-09-05'. [Sequence Number(AE.AESEQ)] = 4, [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-02', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07', [Date/Time of Collection(AE.AEDTC)] = '2012-09-17'. 同様に PRURITUS (AESEQ=2, 5) も記録されている。
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** RELREC ドメインにおいて、治験中止理由となった有害事象のうち「ARTHRALGIA」(AESEQ=7) は Disposition レコード (DSSEQ=1) と関連付けられているが、「CELLULITIS」(AESEQ=8) は関連付けられていないように見える。中止理由の完全な把握という点でデータの完全性にわずかな影響があるかもしれないが、主要な中止理由 (AE) は記録されており、評価への影響は小さい。
        *   **根拠:** RELRECドメインのレコード参照。[Related Domain Abbreviation(RELREC.RDOMAIN)] = 'AE', [Identifying Variable(RELREC.IDVAR)] = 'AESEQ', [Identifying Variable Value(RELREC.IDVARVAL)] = '   7', [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16'. [Related Domain Abbreviation(RELREC.RDOMAIN)] = 'DS', [Identifying Variable(RELREC.IDVAR)] = 'DSSEQ', [Identifying Variable Value(RELREC.IDVARVAL)] = '   1', [Relationship Identifier(RELREC.RELID)] = '01-701-1111-E16'. AESEQ=8 に対応する RELREC レコードがない。
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** Subject Visits (SV) ドメインにおいて、Visit Name が「AE FOLLOW-UP」([Visit Number(SV.VISITNUM)] = 101) のレコードで、[Planned Study Day of Visit(SV.VISITDY)] が null となっている。Unscheduled Visit であるため Planned Study Day がないのは通常許容されるが、データ標準として確認が必要。評価への影響は小さい。
        *   **根拠:** [Visit Number(SV.VISITNUM)] = 101, [Visit Name(SV.VISIT)] = 'AE FOLLOW-UP', [Planned Study Day of Visit(SV.VISITDY)] = null.
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** Demographics (DM) ドメインにおいて、[Date/Time of Informed Consent(DM.RFICDTC)] が欠損している。同意取得日の確認は、GCP遵守および参加者の権利保護の観点から重要である。
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = "".

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[5]で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施および結果確認の記録がない。参加者の適格性確認が不十分であり、安全性および評価の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 関連するデータ（例: 画像検査結果を示すドメインや変数）が提供されたJSONデータに含まれていない。
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[6]「Investigator has obtained informed consent signed by the patient (and/or legal representative) and by the caregiver」の確認に必要な同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) がデータにない。同意取得の確認はGCP遵守および参加者の権利保護の基本であり、逸脱している場合、重大な問題となる。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [6], Section 5.1 Informed Consent
        *   **根拠:** [Date/Time of Informed Consent(DM.RFICDTC)] = "". (指摘 D-4 と関連)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[14]「A history within the last 5 years of the following: a) Schizophrenia b) Bipolar Disease c) Ethanol or psychoactive drug abuse or dependence」に該当する可能性がある既往歴「EATING DISORDER」([Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009') が存在する。Eating Disorder が除外基準の精神疾患 (Mental illness) に含まれるか、またその重症度について確認が必要。不適格な患者が登録された可能性があり、安全性および評価の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [14]
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0702', [Dictionary-Derived Term(MH.MHDECOD)] = 'EATING DISORDER', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'. スクリーニング日 (2012-08-25) から5年以内。
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b]で要求されている「Evidence from ECG recording at screening of any listed condition」の確認記録がない。スクリーニング時のECG実施および結果確認が不明であり、心血管系のリスクを持つ不適格な患者が登録された可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** スクリーニング時のECGデータが提供されたJSONデータに含まれていない。
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[25]「A history within the last 5 years of a primary or recurrent malignant disease」に該当する可能性がある既往歴「BASAL CELL CARCINOMA」([Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2007') が存在する。プロトコルでは例外として「resected... basal cell carcinoma」は許容されるが、この症例の基底細胞癌が切除済み (resected) であったかどうかの情報がない。不適格な患者が登録された可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [25]
        *   **根拠:** [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0951', [Dictionary-Derived Term(MH.MHDECOD)] = 'BASAL CELL CARCINOMA', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2007'. スクリーニング日 (2012-08-25) から5年以内。切除に関する情報なし。
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[27b]「Laboratory test values exceeding the Lilly Reference Range III...」に該当する可能性がある。ベースライン (Day -13) の検査で [Erythrocytes(LB.RBC)] = 3.80 であり、提供された基準値 (3.9-5.5) を下回っている。これがプロトコルで規定された Lilly Reference Range III に基づく基準値であり、逸脱が臨床的に有意でないと判断された根拠が不明な場合、不適格な患者が登録された可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.80, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.9, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 5.5, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = -13.
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b]「Central laboratory test values below reference range for folate...」の確認に必要なベースラインの葉酸 (Folate) 検査結果の記録がない。ビタミンB12、TSHは基準値内。葉酸欠乏が見逃されている可能性は低いかもしれないが、適格性確認が完全ではない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** LBドメインに Folate の検査結果レコードがない。
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[29b]「Positive syphilis screening with confirmatory testing」の確認記録がない。スクリーニング時の梅毒検査実施および結果確認が不明であり、不適格な患者が登録された可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 関連する検査結果（例: RPR, FTA-Abs）が提供されたJSONデータに含まれていない。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-2)
        *   **重要度:** Critical
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 は Study Day 11 に有害事象により治験を中止されましたが、中止の判断根拠となった有害事象（関節痛、蜂窩織炎）の治験薬との関連性はいずれも「関連なし」と評価されています。治験中止の判断に至った具体的な理由（どの事象が主因か、重症度の判断、治験薬との関連性評価の詳細な根拠など）について、詳細をご教示いただけますでしょうか。参加者の安全性評価とデータの正確性確保のため、ご確認をお願いいたします。
        *   **EDCに発出するクエリ文面（英語）:** Subject 01-701-1111 discontinued the study on Study Day 11 due to an Adverse Event, as recorded in the DS domain. However, the causality for the AEs 'ARTHRALGIA' (AESEQ=7) and 'CELLULITIS' (AESEQ=8), which occurred prior to discontinuation, were both assessed as 'NONE' (not related to study drug). Please clarify the specific reason for study discontinuation and provide details on the assessment that led to this decision (e.g., which AE was the primary reason, severity assessment, detailed rationale for causality assessment). This information is needed to ensure accurate safety assessment and data integrity.
        *   **判断理由:** 中止理由とAE評価の間に矛盾があり、安全性評価とデータの信頼性に重大な影響を与えるため、医療機関での判断根拠を確認する必要がある。
        *   **判断根拠:**
            *   [関連するデータ: [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-09-17'(Day 11), [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Causality(AE.AEREL)] = 'NONE', [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS', [Causality(AE.AEREL)] = 'NONE']
            *   [関連するプロトコル箇所: Section 3.10.1 Discontinuations]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「ARTHRALGIA」(関節痛) の治験薬との関連性が「関連なし」と評価されています。本患者には既往歴として「ARTHRITIS」(関節炎) がありますが、今回の関節痛が既往歴の悪化なのか、あるいは治験薬の影響の可能性も考慮された上での評価でしょうか。関連性評価の根拠について、補足情報があればご教示ください。
        *   **EDCに発出するクエリ文面（英語）:** Regarding the AE 'ARTHRALGIA' (AESEQ=7), the causality was assessed as 'NONE'. The subject has a medical history of 'ARTHRITIS'. Was the possibility of this AE being related to the study drug considered, or was it assessed as an exacerbation of the pre-existing condition? Please provide clarification or further details on the rationale for the causality assessment.
        *   **判断理由:** 安全性評価の妥当性を確認するため、関連性評価の根拠を確認する必要がある。
        *   **判断根拠:**
            *   [関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Causality(AE.AEREL)] = 'NONE', [Reported Term for the Medical History(MH.MHTERM)] = 'ARTHRITIS']
            *   [関連する医学的知見: 薬剤起因性関節痛の可能性、既往歴悪化の可能性]
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「MICTURITION URGENCY」(尿意切迫) の治験薬との関連性が「関連なし」と評価されています。治験薬 Xanomeline はムスカリン作動薬であり、理論的に尿意切迫を引き起こす可能性があります。既往歴に「INCONTINENCE」もありますが、今回の事象と治験薬との関連性の可能性について、再度ご検討・ご評価いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** Regarding the AE 'MICTURITION URGENCY' (AESEQ=6), the causality was assessed as 'NONE'. Since Xanomeline is a muscarinic agonist, it could potentially cause urinary urgency. The subject also has a history of 'INCONTINENCE'. Please review and confirm the causality assessment considering the pharmacological properties of the study drug.
        *   **判断理由:** 安全性評価の妥当性を確認するため、薬剤の作用機序を考慮した関連性評価の再確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY', [Causality(AE.AEREL)] = 'NONE', [Reported Term for the Medical History(MH.MHTERM)] = 'INCONTINENCE']
            *   [関連する医学的知見: ムスカリン作動薬の副作用]
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者（推定）:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 11 の検査にて、赤血球平均容積 (MCV) が 101 fL と高値、赤血球数 (RBC) が 3.70 TI/L と低値でした。大球性貧血の可能性も考えられますが、臨床的な意義について評価をお願いします。また、フォローアップ検査（例：ビタミンB12、葉酸など）の必要性についてもご検討ください。
        *   **EDCに発出するクエリ文面（英語）:** On Study Day 11, lab results showed high MCV (101 fL) and low RBC (3.70 TI/L), suggesting possible macrocytic anemia. Please assess the clinical significance of these findings. Also, please consider if follow-up tests (e.g., Vitamin B12, Folate) are warranted.
        *   **判断理由:** 参加者の潜在的な健康問題（貧血）に対応するため、臨床的意義の評価とフォローアップの必要性確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 11. [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.70, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 11.]
            *   [関連する医学的知見: 大球性貧血の診断と評価]
    *   **クエリNo.:** Q-5 (関連指摘No.: D-4, P-2)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 の同意取得日が記録されていません。プロトコル選択基準[6]およびGCP遵守の観点から、同意取得日をご提供いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** The Date of Informed Consent (RFICDTC) for subject 01-701-1111 is missing in the DM domain. Please provide the date when informed consent was obtained to confirm compliance with inclusion criterion [6] and GCP requirements.
        *   **判断理由:** 同意取得の確認はGCPの基本要件であり、参加者の権利保護に不可欠なため。
        *   **判断根拠:**
            *   [関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ""]
            *   [関連するプロトコル箇所: Section 3.4.2.1 [6], Section 5.1]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 について、プロトコル選択基準[5]で要求されている「過去1年以内のCNSイメージング（CTまたはMRI）」の実施記録または結果が見当たりません。実施日と結果（ADとの整合性）について情報をご提供いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** For subject 01-701-1111, documentation confirming CNS imaging (CT or MRI) within the past year, compatible with AD (Inclusion Criterion [5]), was not found in the submitted data. Please provide the date and result of the CNS imaging.
        *   **判断理由:** 参加者の適格性を確認するために必須の情報が不足しているため。
        *   **判断根拠:**
            *   [関連するデータ: 該当データなし]
            *   [関連するプロトコル箇所: Section 3.4.2.1 [5]]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 の既往歴に「EATING DISORDER」(摂食障害、2009年発症) が記録されています。プロトコル除外基準[14]では「過去5年以内の精神疾患 (Mental illness)」が除外対象となっていますが、この摂食障害が除外基準に該当しないと判断された根拠についてご教示いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** Subject 01-701-1111 has a medical history of 'EATING DISORDER' starting in 2009. Exclusion criterion [14] excludes subjects with a history of mental illness within the last 5 years. Please confirm if this condition was reviewed and determined not to meet the exclusion criterion, and provide the rationale.
        *   **判断理由:** 参加者の適格性に関する重要な確認事項であり、除外基準該当の有無を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Dictionary-Derived Term(MH.MHDECOD)] = 'EATING DISORDER', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009']
            *   [関連するプロトコル箇所: Section 3.4.2.2 [14]]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 について、プロトコル除外基準[16b]で要求されているスクリーニング時のECG実施記録または結果が見当たりません。スクリーニングECGの実施日と結果（除外基準に該当する所見がなかったこと）について情報をご提供いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** For subject 01-701-1111, documentation confirming the screening ECG and its results (confirming no exclusionary findings per Exclusion Criterion [16b]) was not found in the submitted data. Please provide the date and results of the screening ECG.
        *   **判断理由:** 参加者の適格性と安全性を確認するために必須の情報が不足しているため。
        *   **判断根拠:**
            *   [関連するデータ: 該当データなし]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [16b]]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 の既往歴に「BASAL CELL CARCINOMA」(基底細胞癌、2007年発症) が記録されています。プロトコル除外基準[25]では「過去5年以内の悪性腫瘍」が除外対象ですが、例外として「切除された基底細胞癌」は許容されます。この基底細胞癌が切除済み (resected) であったかご確認の上、ご回答いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** Subject 01-701-1111 has a medical history of 'BASAL CELL CARCINOMA' starting in 2007. Exclusion criterion [25] excludes subjects with a history of malignant disease within the last 5 years, but allows for resected basal cell carcinoma. Please confirm if this basal cell carcinoma was resected.
        *   **判断理由:** 参加者の適格性に関する重要な確認事項であり、除外基準の例外規定を満たすか確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Dictionary-Derived Term(MH.MHDECOD)] = 'BASAL CELL CARCINOMA', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2007']
            *   [関連するプロトコル箇所: Section 3.4.2.2 [25]]
    *   **クエリNo.:** Q-10 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA/Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 のベースライン検査 (Study Day -13) において、赤血球数 (RBC) が 3.80 TI/L と基準値 (3.9-5.5) を下回っていました。プロトコル除外基準[27b]では基準値を超える検査値が除外対象とされていますが、この RBC 低値が臨床的に問題なく、除外基準に該当しないと判断された根拠についてご教示いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** At baseline (Study Day -13), subject 01-701-1111 had a low RBC count (3.80 TI/L, range 3.9-5.5). Exclusion criterion [27b] refers to lab values exceeding the reference range. Please confirm that this low RBC value was considered not clinically significant and did not meet any exclusion criteria, and provide rationale if available.
        *   **判断理由:** 参加者の適格性に関する確認事項であり、基準値逸脱が除外基準に該当しないと判断された根拠を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.80, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = -13]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [27b]]
    *   **クエリNo.:** Q-11 (関連指摘No.: P-8)
        *   **重要度:** Major
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 について、プロトコル除外基準[29b]で要求されている梅毒スクリーニング検査の実施記録または結果が見当たりません。梅毒スクリーニング検査の実施日と結果について情報をご提供いただけますでしょうか。
        *   **EDCに発出するクエリ文面（英語）:** For subject 01-701-1111, documentation confirming syphilis screening (Exclusion Criterion [29b]) was not found in the submitted data. Please provide the date and result of the syphilis screening test.
        *   **判断理由:** 参加者の適格性を確認するために必須の情報が不足しているため。
        *   **判断根拠:**
            *   [関連するデータ: 該当データなし]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [29b]]
    *   **クエリNo.:** Q-12 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** CRA
        *   **医療機関への問い合わせ文面:** 患者 01-701-1111 について、プロトコル除外基準[28b]の確認に必要なベースラインの葉酸 (Folate) 検査結果が見当たりません。検査を実施されている場合は結果をご提供いただけますでしょうか。もし未実施の場合はその旨をお知らせください。
        *   **EDCに発出するクエリ文面（英語）:** For subject 01-701-1111, the baseline Folate lab result (required for Exclusion Criterion [28b]) was not found in the submitted data. Please provide the result if available, or confirm if the test was not performed.
        *   **判断理由:** 参加者の適格性確認に必要な情報が一部不足しているため。
        *   **判断根拠:**
            *   [関連するデータ: LBドメインに Folate のレコードなし]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [28b]]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **疑義事項/確認内容:** 有害事象「ERYTHEMA」および「PRURITUS」がそれぞれ2回記録されている (AESEQ=1,4 および AESEQ=2,5)。開始日は同一だが収集日・終了日が異なる。データマネジメントプロセスにおいて、これが同一イベントの再評価記録なのか、あるいは重複入力等のエラーなのかを確認する。実質的な評価への影響は小さいと判断されるため、医療機関への問い合わせは不要。
        *   **判断理由:** データクリーニングの一環として内部で解決可能であり、安全性や有効性評価への直接的な影響が小さいため。
        *   **判断根拠:**
            *   [関連するデータ: AEドメインの AESEQ=1, 2, 4, 5 のレコード]
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **疑義事項/確認内容:** RELREC ドメインにおいて、中止理由となった有害事象のうち「CELLULITIS」(AESEQ=8) が Disposition レコード (DSSEQ=1) と関連付けられていないように見える。データモデリングまたはデータ入力上の問題の可能性。データの一貫性確保のため内部で確認する。主要な中止理由は AE と特定されており、評価への影響は限定的。
        *   **判断理由:** データ構造や入力に関する問題の可能性が高く、内部での確認・修正が適切なため。
        *   **判断根拠:**
            *   [関連するデータ: RELRECドメイン、AEドメイン(AESEQ=8)、DSドメイン(DSSEQ=1)]
    *   **確認事項No.:** I-3 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **発行担当者（推定）:** DM
        *   **疑義事項/確認内容:** SV ドメインの Visit「AE FOLLOW-UP」(VISITNUM=101) で VISITDY が null となっている。SDTM IG等に基づき、Unscheduled Visit における VISITDY の扱いとして適切か、データ標準の観点から確認する。評価への影響はないと判断。
        *   **判断理由:** データ標準に関する確認であり、内部で対応可能なため。
        *   **判断根拠:**
            *   [関連するデータ: SVドメイン (VISITNUM=101)]
            *   [関連するDefine.xml箇所: SV.VISITDY 定義]