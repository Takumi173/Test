# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    77歳、男性 (Sex: M)、白色人種 (Race: WHITE)、ヒスパニックまたはラテン系ではない (Ethnicity: NOT HISPANIC OR LATINO)。治験薬割付は Xanomeline High Dose (ARM: Xanomeline High Dose)。
*   **イベント推移:**
    *   2011年03月27日: 既往歴としてアルツハイマー病 (Primary Diagnosis) の診断。
    *   2013年09月20日 (Day -16): スクリーニング1。臨床検査にてクレアチニン(CREAT)が高値 (1.8 mg/dL, 基準上限1.6 mg/dL)。
    *   2013年10月06日 (Day 1): ベースライン。治験薬 Xanomeline 54 mg/day (経皮パッチ, QD) 投与開始 (EX.EXSTDTC)。併用薬として Premarin (Estrogens Conjugated) 0.625 mg (QOD, 経口) 投与開始 (CM.CMSTDTC)。
    *   2013年10月19日 (Day 14): Week 2 Visit。臨床検査にてアルブミン(ALB)が低値 (3.3 g/dL, 基準下限3.5 g/dL)、BUNが高値 (29 mg/dL, 基準上限24 mg/dL)。有害事象「心筋梗塞 (MYOCARDIAL INFARCTION)」(MILD, 治験薬との関連なし) 発現 (AE.AESTDY)。有害事象「脳梗塞後遺症 (LATE EFFECTS OF CEREBRAL INFRACTION)」(SEVERE, 治験薬との関連なし) 発現 (AE.AESTDY、ただしReported TermとMedDRA Term不一致あり)。有害事象「心室中隔欠損症 (VENTRICULAR SEPTAL DEFECT)」(MILD, 治験薬との関連なし) 発現 (AE.AESTDY)。
    *   2013年10月20日 (Day 15): 治験薬 Xanomeline を 81 mg/day に増量 (EX.EXSTDTC)。
    *   2013年10月29日 (Day 24): 併用薬 Premarin 投与終了 (CM.CMENDTC)。
    *   2013年11月01日 (Day 27): 臨床検査実施 (DSレコードに "FINAL LAB VISIT" として記録あり、Visit 5に関連付け)。アルブミン(ALB)が低値 (3.4 g/dL, 基準下限3.5 g/dL)。
    *   2013年11月05日 (Day 31): 有害事象「掻痒感 (PRURITUS)」(MILD, 治験薬との関連 Probable) 発現 (AE.AESTDY)。有害事象「発疹 (RASH)」(MILD, 治験薬との関連 Probable) 発現 (AE.AESTDY)。
    *   2013年11月06日 (Day 32): 併用薬 Hydrocortisone (Topical) 投与開始 (CM.CMSTDTC、掻痒感/発疹の治療目的と推察)。
    *   2013年11月09日 (Day 35): Week 4 Visit (予定Day 28より遅延)。起立性低血圧の傾向 (立位3分後 SYSBP=106, DIABP=60)。
    *   2013年11月18日 (Day 44): 有害事象「脳死 (BRAIN DEATH)」(SEVERE, 治験薬との関連なし) 発現 (AE.AESTDY、ただしReported TermとMedDRA Term不一致、転帰記録にも矛盾あり)。有害事象「脳梗塞後遺症 (LATE EFFECTS OF CEREBRAL INFRACTION)」終了 (AE.AEENDY)。治験薬 Xanomeline 81 mg/day 投与終了 (EX.EXENDTC)。
    *   2013年11月19日 (Day 45): 有害事象「心筋梗塞 (MYOCARDIAL INFARCTION)」回復 (AE.AEENDY)。
    *   2013年11月22日 (Day 48): 有害事象「掻痒感 (PRURITUS)」、「発疹 (RASH)」終了/回復 (AE.AEENDY、ただし一部レコードでは未回復)。併用薬 Hydrocortisone (Topical) 投与終了 (CM.CMENDY)。
    *   2013年11月24日 (Day 50): Week 6 Visit (予定Day 42より遅延)。起立性低血圧の傾向 (立位3分後 SYSBP=112, DIABP=56)。有害事象により治験中止 (DS.DSTERM="ADVERSE EVENT", DS.DSSTDY=50)。
    *   2013年12月06日 (Day 62): AEフォローアップVisit (SV.VISITNUM=101)。参加終了 (DM.RFPENDTC)。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **内容:** 有害事象「脳死 (BRAIN DEATH)」(AESEQ=3) の報告内容に重大な矛盾がある。AETERM/AELLTとAEDECOD("INFLUENZA")が一致せず、AEOUT="RECOVERED/RESOLVED" (Day 44) は医学的にありえない。また、重篤度(AESER="N")も疑わしい。報告の正確性と患者の実際の状態について緊急の確認が必要。
        *   **根拠:** AE.AETERM = 'BRAIN DEATH', AE.AEDECOD = 'INFLUENZA', AE.AEOUT = 'RECOVERED/RESOLVED', AE.AEENDY = 44, AE.AESER = 'N'
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「心筋梗塞 (MYOCARDIAL INFARCTION)」(AESEQ=1) の重症度が軽度(MILD)とされているが、処置が薬剤中止(AEACN="DRUG WITHDRAWN")と記録されている。軽度の心筋梗塞で治験薬を中止する判断は一般的ではなく、重症度評価の妥当性、あるいは処置記録の正確性に疑問がある。既往歴 (MH) の心疾患との関連も含めて評価が必要。
        *   **根拠:** AE.AETERM = 'MYOCARDIAL INFARCTION', AE.AESEV = 'MILD', AE.AEACN = 'DRUG WITHDRAWN', MH.MHTERM = 'MYOCARDIAL INFARCTION' (MHSEQ=4, 7)
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「心室中隔欠損症 (VENTRICULAR SEPTAL DEFECT)」(AESEQ=2) は先天性疾患であり、通常77歳で新規発症するものではない。既往歴(MH)にも記載がなく、AEとしての報告は医学的に不適切である可能性が高い。MHへの記載漏れか、あるいは全く別の事象の誤報告の可能性を検討する必要がある。
        *   **根拠:** AE.AETERM = 'VENTRICULAR SEPTAL DEFECT', AE.AESTDY = 14, DM.AGE = 77, MHドメインに該当記載なし
    *   **指摘No.:** M-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「脳梗塞後遺症 (LATE EFFECTS OF CEREBRAL INFRACTION)」(AESEQ=4) について、AETERMとMedDRAコード由来の用語(AELLT/AEDECOD="CARDIAC DISORDER")および器官分類(AEBODSYS="CARDIAC DISORDERS")が一致していない。事象の特定が不正確であり、適切な評価が困難。コーディングエラーの可能性が高い。
        *   **根拠:** AE.AETERM = 'LATE EFFECTS OF CEREBRAL INFRACTION', AE.AELLT = 'CARDIAC DISORDER', AE.AEDECOD = 'CARDIAC DISORDER', AE.AEBODSYS = 'CARDIAC DISORDERS'
    *   **指摘No.:** M-5
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 併用薬 Premarin (Estrogens Conjugated) が男性(DM.SEX=M)に投与されている。通常、男性への適応はないため、投与理由と妥当性について確認が必要。また、プロトコルでは3ヶ月以上の安定使用が条件だが、Day 1から新規に開始されており、プロトコル逸脱の可能性もある(P-2参照)。
        *   **根拠:** CM.CMTRT = 'PREMARIN', CM.CMSTDTC = '2013-10-06' (Day 1), DM.SEX = 'M', プロトコル3.4.2.2[31v]
    *   **指摘No.:** M-6
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 治験薬投与期間中、特に投与量増量後(Day 15以降)に起立性低血圧の傾向が認められる(VSドメイン)。Xanomelineはムスカリン作動薬であり、血圧低下は予期される作用の可能性がある。しかし、関連する有害事象（めまい、ふらつき等）の報告がない。症状の有無について確認が望ましい。
        *   **根拠:** VS.VSTESTCD = 'SYSBP'/'DIABP', VS.VSPOS = 'STANDING', VS.VSDY = 14, 35, 50 など, AEドメインに関連報告なし

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 治験中止理由 (DS.DSTERM="ADVERSE EVENT", Day 50) となった具体的な有害事象がAEドメインから特定できない。AEドメインの記録（特にAESEQ=3 "BRAIN DEATH", AESEQ=4 "LATE EFFECTS OF..." の不整合、AESEQ=5,6,7,8 "PRURITUS"/"RASH" の重複/転帰不一致）に問題があり、中止理由の特定を困難にしている。RELRECではRASH(AESEQ=5,7)と中止イベント(DSSEQ=1)が関連付けられているが、RASHは軽度であり中止理由としては疑問。
        *   **根拠:** DS.DSTERM = 'ADVERSE EVENT', DS.DSSTDY = 50, AEドメイン, RELREC.RELID = '01-704-1017-E11'
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「掻痒感 (PRURITUS)」および「発疹 (RASH)」が重複して記録されている可能性がある (AESEQ=5と8、AESEQ=6と7)。開始日・終了日は同一だが、収集日(AEDTC)と転帰(AEOUT)が異なるレコードが存在する。データの冗長性と不整合が生じている。
        *   **根拠:** AE.AETERM = 'PRURITUS' (AESEQ=5, 8), AE.AETERM = 'RASH' (AESEQ=6, 7), AE.AESTDY = 31, AE.AEENDY = 48, AE.AEOUT (異なる), AE.AEDTC (異なる)
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 有害事象「心筋梗塞」(AESEQ=1) の処置(AEACN="DRUG WITHDRAWN")と、実際の治験薬投与記録(EXドメイン、Day 44まで継続)が矛盾している。処置記録が不正確。
        *   **根拠:** AE.AEACN = 'DRUG WITHDRAWN' (AESEQ=1), EX.EXENDTC = '2013-11-18' (Day 44)
    *   **指摘No.:** D-4
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「掻痒感 (PRURITUS)」および「発疹 (RASH)」(AESEQ=5,6,7,8) に対する処置として併用薬 Hydrocortisone (Topical) が投与されているが(CMドメイン Day 32-48)、AEドメインの処置(AEACN)が空白となっている。処置記録の欠損。
        *   **根拠:** AE.AETERM = 'PRURITUS'/'RASH', AE.AEACN = '', CM.CMTRT = 'HYDROCORTISONE, TOPICAL', CM.CMSTDY = 32, CM.CMENDY = 48
    *   **指摘No.:** D-5
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「脳梗塞後遺症」(AESEQ=4) の転帰(AEOUT)が "NOT RECOVERED/NOT RESOLVED" となっているが、終了日(AEENDTC/AEENDY=Day 44)が記録されている。矛盾している。
        *   **根拠:** AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED', AE.AEENDTC = '2013-11-18', AE.AEENDY = 44 (AESEQ=4)
    *   **指摘No.:** D-6
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「心室中隔欠損症」(AESEQ=2) の終了日(AEENDTC/AEENDY)が欠損している。転帰は "NOT RECOVERED/NOT RESOLVED"。
        *   **根拠:** AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED', AE.AEENDTC = '', AE.AEENDY = null (AESEQ=2)
    *   **指摘No.:** D-7
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Visit 5 (Week 4, Planned Day 28) の臨床検査(LB)の実施日(LBDTC)が Day 27 となっており、同Visitの他の評価(VS, QS)やVisit自体の実施日(SV, Day 35)と異なる。DSドメインに Day 27 の "FINAL LAB VISIT" (Visit 5と記録) があるため、この日に検査が行われた可能性が高いが、Visit番号の割り当てや記録方法に一貫性がない可能性がある。
        *   **根拠:** LB.LBDTC where LB.VISITNUM=5 (2013-11-01, LBDY=27), SV.SVSTDTC/SVENDTC where SV.VISITNUM=5 (2013-11-09), VS/QS.VSDTC/QSDTC where VS/QS.VISITNUM=5 (2013-11-09), DS.DSSTDTC where DS.DSDECOD='FINAL LAB VISIT' (2013-11-01)

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** スクリーニング時(Day -16)のクレアチニン値(LB.LBSTRESN=159.12 umol/L)が基準範囲上限(LB.LBSTNRHI=141)を超えている。プロトコルの除外基準[27b]に抵触する可能性がある。適格性の再評価や逸脱としての記録が必要。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes: ↑ creatinine...
        *   **根拠:** LB.LBTESTCD = 'CREAT', LB.LBSTRESN = 159.12, LB.LBSTNRHI = 141, LB.LBDY = -16
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 併用薬 Premarin (Estrogens Conjugated) の使用が、プロトコルで規定された安定使用条件（3ヶ月以上）を満たしていない（Day 1から新規開始）。また、男性への投与であり、医学的妥当性も疑問(M-5参照)。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [31v] Estrogen supplements are permitted during the study, but dosage must be stable for at least 3 months prior to enrollment.
        *   **根拠:** CM.CMTRT = 'PREMARIN', CM.CMSTDTC = '2013-10-06' (Day 1), DM.SEX = 'M'
    *   **指摘No.:** P-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Xanomeline High Dose群の投与計画について、プロトコル3.1の図ではWeek 8までは54mg、それ以降に81mgへ増量と示唆されるが、本症例ではDay 15から81mgへ増量されている(EXドメイン)。プロトコル本文に明確な増量スケジュールの記載がないため断定はできないが、図に従うならばプロトコルからの逸脱の可能性がある。
        *   **プロトコル該当箇所:** 3.1 Summary of Study Design (Figure LZZT.1)
        *   **根拠:** EX.EXTRT = 'XANOMELINE', EX.EXDOSE = 81, EX.EXSTDY = 15
    *   **指摘No.:** P-4
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Visit 5 (Week 4) の臨床検査(LB)の実施日(Day 27)が、プロトコルで規定されたVisit Window (Planned Day 28 +/- 3 days) から逸脱している可能性がある。Visit自体の実施日(Day 35)も逸脱している。
        *   **プロトコル該当箇所:** 3.1 Summary of Study Design (Visit Windowの記述)
        *   **根拠:** LB.LBDY = 27, SV.SVSTDY = 35 for VISITNUM=5 (Planned Day 28 +/- 3 days)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **臨床試験結果/安全性への影響度合い:** Critical
        *   **医療機関への問い合わせ文面:** "有害事象「BRAIN DEATH」(AESEQ=3, Day 44発現)について、MedDRAコードが「INFLUENZA」と記録され、転帰が「RECOVERED/RESOLVED」となっています。また重篤性が「N」と報告されています。報告された事象名、MedDRAコード、重篤性、転帰が患者の実際の状態を正確に反映しているかご確認ください。また、本有害事象が治験中止(Day 50)の理由となった事象でしょうか？ 中止理由となった具体的な有害事象名と、その重篤性、治験薬との関連性、転帰を併せてご確認ください。"
        *   **判断理由:** 報告内容に医学的に重大な矛盾があり、患者の安全性評価および中止理由の特定に不可欠なため。
        *   **判断根拠:**
            *   AE.AETERM = 'BRAIN DEATH', AE.AEDECOD = 'INFLUENZA', AE.AEOUT = 'RECOVERED/RESOLVED', AE.AEENDY = 44, AE.AESER = 'N' (AESEQ=3)
            *   DS.DSTERM = 'ADVERSE EVENT', DS.DSSTDY = 50
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "有害事象「MYOCARDIAL INFARCTION」(AESEQ=1, Day 14発現)について、重症度が「MILD」と報告されていますが、処置(AEACN)が「DRUG WITHDRAWN」と記録されています。しかし、治験薬はDay 44まで継続投与されています。本有害事象の重症度評価は適切でしょうか？ また、実際に行われた処置（薬剤中止の有無を含む）についてご確認ください。"
        *   **判断理由:** 有害事象の重症度評価と処置記録の間に矛盾があり、安全性評価の正確性を確認するため。
        *   **判断根拠:**
            *   AE.AETERM = 'MYOCARDIAL INFARCTION', AE.AESEV = 'MILD', AE.AEACN = 'DRUG WITHDRAWN' (AESEQ=1)
            *   EX.EXENDTC = '2013-11-18' (Day 44)
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, D-6)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "有害事象「VENTRICULAR SEPTAL DEFECT」(AESEQ=2, Day 14発現)について、本疾患は通常先天性であり、77歳での新規発症は考えにくいです。本報告は正しいでしょうか？ 既往歴への記載漏れ、あるいは別の事象の誤報告の可能性はありませんか？ また、本有害事象の終了日が未入力です。ご確認ください。"
        *   **判断理由:** AE報告の医学的妥当性に疑義があり、データの正確性を確認する必要があるため。
        *   **判断根拠:**
            *   AE.AETERM = 'VENTRICULAR SEPTAL DEFECT', AE.AESTDY = 14, DM.AGE = 77
            *   AE.AEENDTC = '', AE.AEENDY = null (AESEQ=2)
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4, D-5)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "有害事象「LATE EFFECTS OF CEREBRAL INFRACTION」(AESEQ=4, Day 14発現)について、報告された用語とMedDRAコード(AELLT/AEDECOD='CARDIAC DISORDER')が一致していません。正しい事象名とMedDRAコードをご確認ください。また、転帰(AEOUT)が'NOT RECOVERED/NOT RESOLVED'ですが、終了日(AEENDTC/AEENDY=Day 44)が入力されています。転帰と終了日の情報をご確認ください。"
        *   **判断理由:** 有害事象の特定と評価が不正確であり、修正が必要なため。
        *   **判断根拠:**
            *   AE.AETERM = 'LATE EFFECTS OF CEREBRAL INFRACTION', AE.AEDECOD = 'CARDIAC DISORDER', AE.AEBODSYS = 'CARDIAC DISORDERS', AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED', AE.AEENDY = 44 (AESEQ=4)
    *   **クエリNo.:** Q-5 (関連指摘No.: P-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "スクリーニング時(Day -16)のクレアチニン値(LBTESTCD='CREAT')が基準範囲上限を超えており(1.8 mg/dL、基準上限1.6 mg/dL)、除外基準[27b]に該当する可能性があります。本被験者の適格性についてどのように判断されましたか？ プロトコル逸脱として報告されていますか？ ご確認ください。"
        *   **判断理由:** 除外基準抵触の可能性があり、被験者の適格性とプロトコル遵守状況を確認するため。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'CREAT', LB.LBORRES = '1.8', LB.LBORNRHI = '1.6', LB.LBDY = -16
            *   プロトコル 3.4.2.2 [27b]
    *   **クエリNo.:** Q-6 (関連指摘No.: D-2, D-4)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** "有害事象「PRURITUS」(AESEQ=5, 8) および「RASH」(AESEQ=6, 7)について、同一期間の事象が複数回報告され、転帰(AEOUT)が異なっています。これは重複報告でしょうか、あるいは異なるイベントでしょうか？ また、これらの事象に対して併用薬Hydrocortisoneが使用されていますが、AEの処置(AEACN)が未入力です。記録をご確認・修正ください。"
        *   **判断理由:** データの一貫性と完全性を確保するため。
        *   **判断根拠:**
            *   AE.AETERM = 'PRURITUS' (AESEQ=5, 8), AE.AETERM = 'RASH' (AESEQ=6, 7), AE.AEOUT, AE.AEDTC
            *   AE.AEACN = '' (AESEQ=5,6,7,8)
            *   CM.CMTRT = 'HYDROCORTISONE, TOPICAL', CM.CMSTDY = 32, CM.CMENDY = 48

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5, P-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **疑義事項/確認内容:** 併用薬 Premarin が男性に投与され、かつプロトコルの安定使用条件を満たしていない。プロトコル逸脱の可能性が高い。内部で逸脱として記録し、必要に応じて当局報告等を検討する。男性への投与理由については特定困難だが、記録として残す。
        *   **判断理由:** プロトコル逸脱の可能性が高く、内部での記録と対応検討が必要なため。医療機関に理由を問い合わせても不明瞭な回答となる可能性が高い。
        *   **判断根拠:**
            *   CM.CMTRT = 'PREMARIN', CM.CMSTDTC = '2013-10-06' (Day 1), DM.SEX = 'M'
            *   プロトコル 3.4.2.2 [31v]
    *   **確認事項No.:** I-2 (関連指摘No.: P-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **疑義事項/確認内容:** Xanomeline High Dose群の投与計画について、プロトコル本文と図の間で増量タイミングの解釈に齟齬が生じる可能性がある。Day 15からの81mgへの増量がプロトコル逸脱にあたるか、プロトコル記載の曖昧さによるものか、内部で解釈を統一し、必要であれば逸脱として記録する。
        *   **判断理由:** プロトコルの解釈に関わる問題であり、内部での確認と統一見解が必要なため。
        *   **判断根拠:**
            *   EX.EXTRT = 'XANOMELINE', EX.EXDOSE = 81, EX.EXSTDY = 15
            *   プロトコル 3.1 Figure LZZT.1
    *   **確認事項No.:** I-3 (関連指摘No.: M-6)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** VSデータで起立性低血圧の傾向が認められるが、AE報告がない。治験薬との関連も考えられるため、今後の安全性評価において同様の傾向がないか注視する。現時点ではクエリ発行は不要と判断。
        *   **判断理由:** 症状の有無が不明であり、現時点での緊急性は低いが、安全性シグナルとして内部で認識しておく必要があるため。
        *   **判断根拠:**
            *   VS.VSTESTCD = 'SYSBP'/'DIABP', VS.VSPOS = 'STANDING' (複数時点)
            *   AEドメインに関連報告なし
    *   **確認事項No.:** I-4 (関連指摘No.: D-7, P-4)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Visit 5の臨床検査日(Day 27)とVisit実施日(Day 35)にずれがあり、Visit Windowからも逸脱している可能性がある。DSレコードにDay 27の"FINAL LAB VISIT"がVisit 5として記録されていることから、記録方法の問題の可能性が高い。データクリーニングの一環として内部で確認し、必要に応じてデータ修正または記録方法の標準化を検討する。
        *   **判断理由:** データの一貫性に関わる問題であり、内部での確認・修正が適切なため。
        *   **判断根拠:**
            *   LB.LBDTC where LB.VISITNUM=5 (LBDY=27)
            *   SV.SVSTDTC/SVENDTC where SV.VISITNUM=5 (Day 35)
            *   DS.DSSTDTC where DS.DSDECOD='FINAL LAB VISIT' (Day 27)
            *   プロトコル 3.1
    *   **確認事項No.:** I-5 (関連指摘No.: なし)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** MHドメインにおいて、多くの既往歴で開始日(MHSTDTC)が欠損している。主要な既往歴(Alzheimer's Disease, Heart Attack, Triple Vessel Bypass Graft)には日付があるが、他の"SIGNIFICANT PRE-EXISTING CONDITION"と分類された事象の開始日が不明。データの完全性の観点から記録するが、現時点で治験の評価に大きな影響はないと判断。
        *   **判断理由:** データの完全性に関する問題だが、主要な情報は得られており、緊急性は低い。
        *   **判断根拠:**
            *   MH.MHSTDTC = '' (MHSEQ=1, 2, 3, 4, 5, 6)

```

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    64歳、男性、人種: WHITE、民族: NOT HISPANIC OR LATINO。計画アーム/実施アーム: Placebo (Pbo)。

*   **イベント推移:**
    *   2012年12月27日 (Day -65, Screening 1): 臨床検査にてALT (135 U/L, 基準値: 6-43), AST (145 U/L, 基準値: 11-36) が基準値上限を大幅に超過 (LBNRIND='HIGH')。他の検査値はほぼ基準値内。
    *   2013年02月21日 (Day -9, Unscheduled 1.1): 臨床検査にてALT (19 U/L), AST (29 U/L) は基準値内に正常化。Sodiumが基準値下限を下回る (133 mEq/L, 基準値: 135-145)。
    *   2013年03月02日 (Day 1, Baseline): Placebo投与開始。ベースラインバイタルサイン測定。立位1分後に収縮期血圧が臥位から22mmHg低下 (130 -> 108 mmHg)。
    *   2013年03月04日 (Day 3): 有害事象「DIARRHOEA」(MILD) 発現。治験薬との関連: POSSIBLE。
    *   2013年03月05日 (Day 4): 有害事象「INSOMNIA」(MILD) 発現。治験薬との関連: REMOTE。併用薬「KAOPECTATE」を1回投与 (有害事象 DIARRHOEA のため)。
    *   2013年03月06日 (Day 5): 有害事象「DIARRHOEA」回復/解消。有害事象「INSOMNIA」回復/解消。
    *   2013年03月14日 (Day 13, Week 2): 特に注目すべき検査値変動なし。
    *   2013年03月28日 (Day 27, Week 4): 臨床検査にてMCVが基準値上限をわずかに超える (101 fL, 基準値: 80-100)。Sodiumが基準値上限をわずかに超える (146 mEq/L, 基準値: 135-145)。
    *   2013年04月13日 (Day 43, Week 6): 特に注目すべき検査値変動なし。MCVは基準値内に回復 (98 fL)。Sodiumも基準値内に回復 (142 mEq/L)。
    *   ... (以降、大きな変動や新規AEなし) ...
    *   2013年08月31日 (Day 183, Week 26): Placebo投与終了。試験完了。臨床検査にてASTが基準値上限をわずかに超える (38 U/L, 基準値: 11-36)。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Screening 1 (Day -65) において、ALTおよびASTが基準値上限を大幅に超えていた (それぞれ正常上限の約3.1倍、4.0倍)。これはプロトコル除外基準[27b]に抵触する可能性があったが、治験薬投与開始前のUnscheduled Visit 1.1 (Day -9) までに正常範囲内に回復している。投与期間中の肝機能検査値は、最終投与日(Day 183)のAST軽度上昇を除き、概ね基準値内で推移している。プラセボ投与例であり、治験薬との関連は考えにくい。
        *   **根拠:** LB.LBTESTCD='ALT', LBSTRESN=135, LBSTNRHI=43, LBDY=-65; LB.LBTESTCD='AST', LBSTRESN=145, LBSTNRHI=36, LBDY=-65; LB.LBTESTCD='ALT', LBSTRESN=19, LBDY=-9; LB.LBTESTCD='AST', LBSTRESN=29, LBDY=-9; LB.LBTESTCD='AST', LBSTRESN=38, LBDY=183; プロトコル Section 3.4.2.2 Exclusion Criteria [27b]
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Week 4 (Day 27) にMCVが一過性に基準値上限をわずかに超えた (101 fL, Ref: 80-100)。ビタミンB12は基準値内であり、貧血関連の既往歴やAE報告もない。次回以降の測定では基準値内に戻っており、臨床的意義は低いと考えられる。
        *   **根拠:** LB.LBTESTCD='MCV', LBSTRESN=101, LBSTNRHI=100, LBDY=27; LB.LBTESTCD='MCV', LBSTRESN=98, LBDY=43.
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Unscheduled Visit 1.1 (Day -9) でSodiumが基準値下限を下回り (133 mEq/L, Ref: 135-145)、Week 4 (Day 27) で基準値上限をわずかに上回った (146 mEq/L, Ref: 135-145)。いずれも投与開始前または投与初期の変動であり、次回以降の測定では基準値内に戻っている。関連するAE報告もなく、臨床的意義は低いと考えられる。
        *   **根拠:** LB.LBTESTCD='SODIUM', LBSTRESN=133, LBSTNRLO=135, LBDY=-9; LB.LBTESTCD='SODIUM', LBSTRESN=146, LBSTNRHI=145, LBDY=27; LB.LBTESTCD='SODIUM', LBSTRESN=142, LBDY=43.

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。プロトコルでは同意取得が必須であり、記録の欠損は問題である。ただし、SEドメインのScreening Element開始日 (SE.SESTDTC='2013-02-23') が同意日である可能性があり、これがScreening Visit 1の実施日 (SV.SVSTDTC='2013-02-23') と一致するため、手順自体は遵守されている可能性が高い。
        *   **根拠:** DM.RFICDTC = "" (Missing); SE.ETCD='SCRN', SE.SESTDTC='2013-02-23'; SV.VISITNUM=1, SV.SVSTDTC='2013-02-23'; プロトコル Section 3.4.1, Section 5.1.
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** AE, MH, CMドメインにおいて、辞書コーディング（MedDRA, WHODRUG）が行われていない、またはデータに含まれていない項目（--DECOD, --LLT, --PTCD, --SOC 等）が多数存在する。データ解析およびレビューの精度に影響する。
        *   **根拠:** AE.AEDECOD, AE.AELLTCD 等が欠損; MH.MHDECOD, MH.MHLLT 等が一部欠損またはVerbatim; CM.CMDECOD, CM.CMCLAS が一部 'UNCODED'.
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 複数のVisitにおいて、実際の評価日 (--DY) が計画された評価日 (VISITDY) より1日早い (例: Week 2 Visit は VISITDY=14 だが、実際の評価は LBDY=13, VSDY=13)。プロトコルで規定されたVisit Window (±3日 or ±4日) の範囲内ではあるが、一貫してずれが生じている。
        *   **根拠:** LB, VS, QS, SV ドメインの --DY と VISITDY の比較 (例: VISITNUM=4, VISITDY=14 vs LBDY=13, VSDY=13); プロトコル Section 3.9.

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 選択基準[5]「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の確認状況が不明。データセットにImaging結果が含まれていないため、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** JSONデータにImaging結果を示すドメインや変数が存在しない。
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[16b]「Evidence from ECG recording at screening of any listed condition」の確認状況が不明。データセットにECG結果が含まれていないため、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** JSONデータにECG結果を示すドメイン(EG)が存在しない。
    *   **指摘No.:** P-3
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[28b]「Central laboratory test values below reference range for folate...」の確認状況が不明。データセットにFolateの検査結果が含まれていないため、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** LBドメインにLBTESTCD='FOLATE'のレコードが存在しない。
    *   **指摘No.:** P-4
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 除外基準[29b]「Positive syphilis screening with confirmatory testing」の確認状況が不明。データセットに梅毒検査結果が含まれていないため、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** LBドメインに梅毒関連のLBTESTCDのレコードが存在しない。
    *   **指摘No.:** P-5
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **逸脱の可能性:** 評価スケジュールの逸脱。Visit 8 (Week 8) における Disability Assessment for Dementia (DAD) の評価が実施されていない可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.1.1, Attachment LZZT.1 Schedule of Events
        *   **根拠:** QSドメインにおいて、VISITNUM=8 に対応するDAITM* (DAD項目) のレコードが存在しない。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 の同意取得日 (DM.RFICDTC) がデータベース上で欠損しています。同意取得日を特定できる文書（例：同意説明文書の署名ページ）に基づき、正確な同意取得日をご報告ください。もし特定できない場合は、その旨をご連絡ください。"
        *   **判断理由:** 同意取得はGCPの根幹であり、日付の欠損は重大な記録不備であるため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042', DM.RFICDTC = "" (Missing)
            *   プロトコル Section 5.1
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、選択基準[5]（過去1年以内のADに適合するCNS画像所見）を満たしていたことを確認できる記録（例：画像診断レポートの日付と所見概要）をご提示ください。"
        *   **判断理由:** 選択基準の充足を確認するため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.4.2.1 Inclusion Criteria [5]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、除外基準[16b]（スクリーニングECGでの特定の所見）に該当しなかったことを確認できる記録（例：スクリーニングECGレポートの日付と所見）をご提示ください。"
        *   **判断理由:** 安全性に関わる除外基準の充足を確認するため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [16b]
    *   **クエリNo.:** Q-4 (関連指摘No.: P-3)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、除外基準[28b]（葉酸値が基準値未満）に該当しなかったことを確認するため、スクリーニング時の葉酸 (Folate) の検査結果をご報告ください。"
        *   **判断理由:** 除外基準の充足を確認するため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [28b]
            *   LBドメインに Folate データ欠損
    *   **クエリNo.:** Q-5 (関連指摘No.: P-4)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、除外基準[29b]（梅毒スクリーニング陽性）に該当しなかったことを確認するため、スクリーニング時の梅毒検査の結果をご報告ください。"
        *   **判断理由:** 除外基準の充足を確認するため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [29b]
            *   LBドメインに梅毒関連データ欠損
    *   **クエリNo.:** Q-6 (関連指摘No.: P-5)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、Visit 8 (Week 8) の Disability Assessment for Dementia (DAD) の評価データがデータベース上で確認できませんでした。Visit 8 で DAD が実施されたか、実施されなかった場合はその理由をご確認の上、ご報告ください。実施されていた場合はデータの提出をお願いします。"
        *   **判断理由:** Secondary endpoint である DAD の評価スケジュール逸脱の可能性を確認するため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.9.1.1, Attachment LZZT.1
            *   QSドメインに VISITNUM=8 の DAITM* レコード欠損
    *   **クエリNo.:** Q-7 (関連指摘No.: P-6)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、プロトコルで規定されたVisit (Visit 1, 4, 5, 7, 8, 9, 10, 11, 12, 13) で実施されたECGデータがデータベース上で確認できませんでした。各VisitでのECG実施状況をご確認の上、未提出の場合はデータの提出をお願いします。"
        *   **判断理由:** 安全性評価に必要なデータが欠損しているため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Attachment LZZT.1
            *   JSONデータに EG ドメイン欠損
    *   **クエリNo.:** Q-8 (関連指摘No.: P-7)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "患者 01-703-1042 について、プロトコルで規定されたVisit (Visit 3, 4, 5, 7, 9, 11) で実施された薬物動態評価用採血データ (Xanomeline濃度) がデータベース上で確認できませんでした。各Visitでの採血実施状況をご確認の上、未提出の場合はデータの提出をお願いします。"
        *   **判断理由:** PK評価に必要なデータが欠損しているため。
        *   **判断根拠:**
            *   DM.USUBJID = '01-703-1042'
            *   プロトコル Section 3.9.2
            *   JSONデータに PK 関連ドメイン欠損

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Screening 1 (Day -65) でのALT, AST高値。治験薬投与前に正常化しており、プラセボ投与例であるため、現時点での安全性懸念は低い。記録として残す。
        *   **判断理由:** 投与前の変動であり、その後正常化しているため、現時点で医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   LB.LBTESTCD in ('ALT', 'AST'), LBDY=-65, LBNRIND='HIGH'
            *   LB.LBTESTCD in ('ALT', 'AST'), LBDY=-9, LBNRIND='NORMAL'
    *   **確認事項No.:** I-2 (関連指摘No.: M-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Week 4 (Day 27) でのMCV一過性高値。次回以降正常化しており、臨床的意義は低いと判断。記録として残す。
        *   **判断理由:** 一過性の変動であり、関連所見もないため問い合わせ不要。
        *   **判断根拠:**
            *   LB.LBTESTCD='MCV', LBSTRESN=101, LBNRIND='HIGH', LBDY=27
            *   LB.LBTESTCD='MCV', LBSTRESN=98, LBNRIND='NORMAL', LBDY=43
    *   **確認事項No.:** I-3 (関連指摘No.: M-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Sodiumの一過性の基準値逸脱 (Day -9 低値, Day 27 高値)。変動幅は小さく、次回以降正常化しており、臨床的意義は低いと判断。記録として残す。
        *   **判断理由:** 一過性の軽微な変動であり、関連所見もないため問い合わせ不要。
        *   **判断根拠:**
            *   LB.LBTESTCD='SODIUM', LBSTRESN=133, LBNRIND='LOW', LBDY=-9
            *   LB.LBTESTCD='SODIUM', LBSTRESN=146, LBNRIND='HIGH', LBDY=27
            *   LB.LBTESTCD='SODIUM', LBSTRESN=142, LBNRIND='NORMAL', LBDY=43
    *   **確認事項No.:** I-4 (関連指摘No.: D-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **疑義事項/確認内容:** AE, MH, CMドメインにおける辞書コーディング（MedDRA, WHODRUG）の未実施または欠損。データマネジメント担当部門にてコーディング作業の状況を確認・推進する必要がある。
        *   **判断理由:** データクリーニングおよび解析に必要な作業であり、内部での対応が必要。
        *   **判断根拠:**
            *   AE, MH, CM ドメインの --DECOD, --LLT 等の変数に欠損または 'UNCODED' が存在する。
            *   Define.xml で MedDRA 8.0, WHODRUG 200604 が指定されている。
    *   **確認事項No.:** I-5 (関連指摘No.: D-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** 多くのVisitで実際の評価日 (--DY) が計画日 (VISITDY) より1日早い。プロトコルで規定されたVisit Window内ではあるため逸脱ではないが、一貫して発生している理由は不明。Study Dayの計算方法 (--DTC - RFSTDTC + 1) は標準的であり、データ入力または日付管理の問題の可能性。記録として残す。
        *   **判断理由:** Visit Window内であり、臨床評価への影響は小さいため、現時点での問い合わせは不要。
        *   **判断根拠:**
            *   複数のドメイン(SV, LB, VS, QS)で VISITNUM と VISITDY, --DY を比較。
            *   プロトコル Section 3.9 (Visit Window規定)

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    *   年齢: 81 歳 (DM.AGE)
    *   性別: Female (DM.SEX)
    *   人種: WHITE (DM.RACE)
    *   民族: NOT HISPANIC OR LATINO (DM.ETHNIC)
    *   投与群 (計画): Xanomeline Low Dose (DM.ARM)
    *   投与群 (実際): Xanomeline Low Dose (DM.ACTARM)

*   **イベント推移:**
    *   2012年7月8日 (Day -61): 有害事象「LOCALISED INFECTION」(MODERATE) 発現 (AE.AESTDY = -61)。同日より併用薬 KEFLEX (Cephalexin) 500mg QID 開始 (CM.CMSTDY = -61)。
    *   2012年8月25日 (Day -13): スクリーニング来院 (Visit 1)。
        *   臨床検査 (LB) で Erythrocytes (RBC) が基準値下限未満 (3.8 TI/L, LBNRIND='LOW')。その他主要な検査値は基準範囲内。
        *   既往歴としてアルツハイマー病 (2009年発症)、高血圧、甲状腺機能低下症、骨粗鬆症、関節炎、難聴、耳鳴、黄斑変性、基底細胞癌 (2007年) など多数あり。
        *   併用薬として KEFLEX, LISINOPRIL, MOTRIN(PRN), PREMARIN, PROVERA, SYNTHROID が継続中。
    *   2012年9月2日 (Day -5): 有害事象「ERYTHEMA」(MILD), 「PRURITUS」(MILD) 発現 (AE.AESTDY = -5)。
    *   2012年9月2日 (Day -5)～2012年9月4日 (Day -3): 併用薬 HYDROCORTISONE, TOPICAL を使用 (CM.CMSTDY = -5, CM.CMENDY = -3)。
    *   2012年9月5日 (Day -2): スクリーニング来院 (Visit 2)。
    *   2012年9月7日 (Day 1): ベースライン来院 (Visit 3)。
        *   治験薬 Xanomeline 54mg Patch QD 投与開始 (EX.EXSTDY = 1)。
        *   有害事象「MICTURITION URGENCY」(MILD) 発現 (AE.AESTDY = 1)。
        *   有害事象「ERYTHEMA」(MILD), 「PRURITUS」(MILD) 回復 (AE.AEENDY = 1)。
        *   ベースラインのバイタルサイン (VS) では臥位・立位での血圧、脈拍に特記すべき異常なし。
    *   2012年9月13日 (Day 7): 有害事象「ARTHRALGIA」(MODERATE), 「CELLULITIS」(MODERATE) 発現 (AE.AESTDY = 7)。
    *   2012年9月16日 (Day 10): 治験薬 Xanomeline 投与終了 (EX.EXENDY = 10)。
    *   2012年9月17日 (Day 11): Week 2 来院 (Visit 4)。
        *   有害事象により治験中止 (DS.DSDECOD = 'ADVERSE EVENT', DS.DSSTDY = 11)。中止理由は ARTHRALGIA (AESEQ=7) と関連付けられている (RELREC)。
        *   臨床検査 (LB) で Ery. Mean Corpuscular Volume (MCV) が基準値上限超 (101 fL, LBNRIND='HIGH')、Anisocytes (ANISO) が ABNORMAL、Erythrocytes (RBC) が引き続き基準値下限未満 (3.7 TI/L, LBNRIND='LOW')、Specific Gravity (SPGRAV) が基準値下限未満 (1.004, LBNRIND='LOW')。
        *   バイタルサイン (VS) では、立位1分後および3分後に収縮期血圧が臥位から10mmHg以上低下 (Supine: 125, Standing 1min: 112, Standing 3min: 110)。拡張期血圧は大きな変動なし。
        *   質問票調査 (QS) ADAS-COG(11) Total Score = 5 (Baseline: 7)。NPI-X Total Score = 1 (Baseline: 2)。
    *   2012年9月29日 (Day 23?): AEフォローアップ来院 (Visit 101)。
    *   2013年2月22日 (Day 169): Retrieval 来院 (Visit 201)。
        *   有害事象 ARTHRALGIA, CELLULITIS, LOCALISED INFECTION, MICTURITION URGENCY はすべて未回復 (AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED')。
        *   質問票調査 (QS) ADAS-COG(11) Total Score = 9。NPI-X Total Score = 45。ベースラインおよびWeek 2と比較して悪化。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** Day 7に発現した有害事象「CELLULITIS」(MODERATE) に対する処置記録がCMドメインにない。Cellulitisは細菌感染症であり、通常は抗菌薬治療が必要となる。既存のKEFLEX投与が Day -61 から継続されているが、これが Day 7 の Cellulitis に対する適切な治療であったか不明であり、患者の安全管理上、確認が必要。
        *   **根拠:** AE.AETERM = 'CELLULITIS', AE.AESTDY = 7, AE.AESEV = 'MODERATE'; CMドメインでDay 7以降に開始された関連する可能性のある薬剤記録なし。
    *   **指摘No.:** M-2
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **内容:** 治験薬投与期間中に発現した有害事象「ARTHRALGIA」(中止理由)、「CELLULITIS」、「MICTURITION URGENCY」について、治験薬との関連性 (AEREL) が全て 'NONE' と評価されている。MICTURITION URGENCY は治験薬の薬理作用 (ムスカリン作動性) から関連が否定できず、ARTHRALGIA は中止理由となった事象であるため、関連性評価が 'NONE' であることの医学的根拠を確認する必要がある。SUPPAE ドメインではこれらのAEは Treatment Emergent Flag (AETRTEM) = 'Y' となっており、評価に一貫性がない可能性もある。
        *   **根拠:** AE.AETERM = 'ARTHRALGIA', 'CELLULITIS', 'MICTURITION URGENCY'; AE.AESTDY = 7, 7, 1; AE.AEREL = 'NONE'; SUPPAE.QNAM = 'AETRTEM', SUPPAE.QVAL = 'Y' for AESEQ = 6, 7, 8; 一般的な医学的知見 (Xanomeline の薬理作用)。
    *   **指摘No.:** M-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Day 11 の臨床検査で MCV 高値、RBC 低値、Anisocytes 異常が認められ、大球性貧血の可能性が示唆される。Screening時からRBC低値は認められていた。Vitamin B12は正常だが、葉酸 (Folate) のデータがなく、欠乏による影響の可能性を完全に否定できない。関連する有害事象の報告はないが、貧血の評価が十分であったか確認することが望ましい。
        *   **根拠:** LB.LBTESTCD = 'MCV', LB.LBSTRESN = 101, LB.LBNRIND = 'HIGH', LB.LBDY = 11; LB.LBTESTCD = 'RBC', LB.LBSTRESN = 3.7, LB.LBNRIND = 'LOW', LB.LBDY = 11; LB.LBTESTCD = 'ANISO', LB.LBSTRESC = '1', LB.LBNRIND = 'ABNORMAL', LB.LBDY = 11; LB.LBTESTCD = 'VITB12', LB.LBSTRESN = 388.8, LB.LBNRIND = 'NORMAL', LB.LBDY = -13。

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 有害事象「ERYTHEMA」および「PRURITUS」について、ほぼ同一内容のレコードが2件ずつ存在する (AESEQ=1 と 4、AESEQ=2 と 5)。AESTDTC, AEENDTCは同一だが、AEOUT (転帰) が異なる ('NOT RECOVERED/NOT RESOLVED' と 'RECOVERED/RESOLVED')。AEENDTC が Day 1 と記録されているため、'RECOVERED/RESOLVED' が正しいと考えられ、AESEQ=1 および AESEQ=2 は重複または誤記録の可能性がある。
        *   **根拠:** AE records for USUBJID='01-701-1111', AETERM='ERYTHEMA' (AESEQ=1, 4) and AETERM='PRURITUS' (AESEQ=2, 5)。AE.AEENDTC = '2012-09-07' (Day 1)。AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED' for AESEQ=1, 2; AE.AEOUT = 'RECOVERED/RESOLVED' for AESEQ=4, 5。
    *   **指摘No.:** D-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 多くのドメイン (AE, CM, MH) で、MedDRAコードやWHODrugコードに関連する変数 (例: AE.AELLTCD, AE.AEPTCD, CM.CMDECOD, MH.MHDECOD) が欠損している。また、CMドメインでは投与量・単位・頻度・経路、MHドメインでは発現日などの重要な情報が一部欠損している。データの完全性の観点から問題がある。
        *   **根拠:** AE, CM, MH ドメインの各変数における欠損値。Define.xml ではコーディング辞書が指定されている。
    *   **指摘No.:** D-3
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** QSドメインの DAD (Disability Assessment for Dementia) に関するレコードで、Week 2 (Visit 4, Day 11) において QSTESTCD が DAITM25～DAITM29 (Going on an outing 関連) の項目で QSSTRESN = 96 (Not Applicable) となっている。Baseline (Visit 3, Day 1) では一部項目が Yes/No で評価されており、評価不能となった理由が不明。
        *   **根拠:** QS records for USUBJID='01-701-1111', QSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', QSTESTCD in ('DAITM25', 'DAITM26', 'DAITM27', 'DAITM28', 'DAITM29') where VISITNUM=4。Compare with VISITNUM=3。

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** Screening時の臨床検査でRBC (赤血球数) が基準値下限未満であった (LB.LBSTRESN=3.8, LB.LBSTNRLO=3.9)。除外基準[27b]には "Laboratory test values exceeding the Lilly Reference Range III" と上限超過が主に記載されているが、"↑↓ hemoglobin, ↑↓ white blood cell count" のように低下も除外対象となる可能性を示唆する記載もある。RBCは明記されていないが、基準値外であるため、組み入れが適切であったか確認が必要。ただし、Hemoglobinは基準範囲内であり、臨床的に大きな問題とは判断されなかった可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LB.LBTESTCD = 'RBC', LB.LBSTRESN = 3.8, LB.LBSTNRLO = 3.9, LB.LBNRIND = 'LOW', LB.VISITNUM = 1, LB.LBBLFL = 'Y'。
    *   **指摘No.:** P-2
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **内容:** 既往歴 (MH) に Eating disorder (2009年) の記載がある。除外基準[14]では「A history within the last 5 years of the following: ... Ethanol or psychoactive drug abuse or dependence」などが挙げられているが、Eating disorder がこれに該当するか、あるいは他の "mental illness" として除外対象となるか、プロトコルの詳細定義に基づき確認が必要。2012年のScreening時点で5年以内 (2007年以降) に該当するかは不明瞭（MHSTDTC='2009'）。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [14]
        *   **根拠:** MH.MHTERM = 'VERBATIM_0702', MH.MHDECOD = 'EATING DISORDER', MH.MHSTDTC = '2009'。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Day 7に発現した有害事象「CELLULITIS」(Moderate) について、併用薬記録に新規の抗菌薬投与が見られません。既存のKEFLEX投与 (Day -61開始) が本件に対する治療であったか、あるいは他の処置が行われたかご確認ください。また、転帰が「NOT RECOVERED/NOT RESOLVED」となっていますが、その後の経過についてもご確認ください。"
        *   **判断理由:** Cellulitis に対する適切な治療が行われたか、患者の安全性を確認するため。
        *   **判断根拠:**
            *   AE.AETERM = 'CELLULITIS', AE.AESTDY = 7, AE.AESEV = 'MODERATE', AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED'
            *   CMドメイン: Day 7以降の新規抗菌薬記録なし。CM.CMTRT = 'KEFLEX', CM.CMSTDY = -61 (継続中)。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **臨床試験結果/安全性への影響度合い:** Major
        *   **医療機関への問い合わせ文面:** "Day 11の治験中止理由となった有害事象「ARTHRALGIA」(Day 7発現, Moderate)、および同時期に発現した「CELLULITIS」(Day 7発現, Moderate)、Day 1に発現した「MICTURITION URGENCY」(Mild)について、治験薬との関連性(AEREL)が全て 'NONE' と評価されています。特に中止理由となった事象や、薬理作用から関連が疑われる事象について、関連性評価の根拠を再確認し、必要であれば修正してください。"
        *   **判断理由:** 有害事象の適切な評価（特に中止理由との関連性）を確認し、治験薬の安全性プロファイルを正確に把握するため。
        *   **判断根拠:**
            *   AE.AETERM = 'ARTHRALGIA', 'CELLULITIS', 'MICTURITION URGENCY'; AE.AESTDY = 7, 7, 1; AE.AEREL = 'NONE'; AE.AESEV = 'MODERATE', 'MODERATE', 'MILD'
            *   DS.DSTERM = 'ADVERSE EVENT', DS.DSSTDY = 11
            *   RELREC: DSSEQ=1 related to AESEQ=7 ('ARTHRALGIA')
            *   SUPPAE.QNAM = 'AETRTEM', SUPPAE.QVAL = 'Y' for AESEQ = 6, 7, 8
            *   一般的な医学的知見 (Xanomeline の薬理作用)
    *   **クエリNo.:** Q-3 (関連指摘No.: D-1)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** "有害事象「ERYTHEMA」および「PRURITUS」について、転帰(AEOUT)が異なる類似の記録が2件ずつ (AESEQ=1, 4 および AESEQ=2, 5) 存在します。終了日(AEENDTC)がいずれも Day 1 と記録されているため、転帰が 'RECOVERED/RESOLVED' である AESEQ=4 および AESEQ=5 が正しい記録と考えられます。AESEQ=1 および AESEQ=2 が重複または誤記録であれば削除してください。"
        *   **判断理由:** データの一貫性を確保し、正確な有害事象情報を得るため。
        *   **判断根拠:**
            *   AE records for USUBJID='01-701-1111', AETERM='ERYTHEMA' (AESEQ=1, 4) and AETERM='PRURITUS' (AESEQ=2, 5)
            *   AE.AEENDTC = '2012-09-07' (Day 1) for AESEQ=1, 2, 4, 5
            *   AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED' for AESEQ=1, 2
            *   AE.AEOUT = 'RECOVERED/RESOLVED' for AESEQ=4, 5
    *   **クエリNo.:** Q-4 (関連指摘No.: D-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **医療機関への問い合わせ文面:** "Week 2 (Visit 4, Day 11) の DAD評価 (QS) において、外出関連の項目 (DAITM25-DAITM29) が 'Not Applicable' と記録されています。Baseline (Visit 3) では評価可能であった項目も含まれていますが、Week 2で評価不能となった理由をご確認ください。"
        *   **判断理由:** 評価データの欠損理由を明確にし、データの解釈を可能にするため。
        *   **判断根拠:**
            *   QS records for USUBJID='01-701-1111', QSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', QSTESTCD in ('DAITM25'...'DAITM29') where VISITNUM=4 show QSSTRESN=96.
            *   QS records for VISITNUM=3 show values other than 96 for some of these items.

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** AE, CM, MHドメインにおいて、MedDRA/WHODrugコード関連変数やその他の重要変数に欠損値が多数存在する。データマネジメント担当者にコーディング状況および欠損値の理由を確認し、可能な範囲でデータの補完を検討する。
        *   **判断理由:** データの完全性と品質を確保するため。コーディングやデータ入力プロセスの問題である可能性が高く、まずは内部での確認が適切。
        *   **判断根拠:**
            *   AE, CM, MH ドメインにおける欠損値 (例: AE.AEPTCD, CM.CMDECOD, MH.MHDECOD, CM.CMDOSE など)
    *   **確認事項No.:** I-2 (関連指摘No.: P-1, M-3)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** Screening時のRBC低値が除外基準[27b]に抵触しないか、およびWeek 2でのMCV高値・Anisocytes異常を含む貧血傾向の臨床的意義について、メディカルモニター/担当医師と協議する。除外基準の解釈と、組み入れ判断の妥当性を確認する。貧血の進行や関連症状の有無を再確認する。
        *   **判断理由:** プロトコル遵守と患者の安全性評価の観点から、内部での医学的判断と解釈の確認が必要。現時点で明らかな安全性リスクや重大な逸脱とは判断できないため、内部確認とする。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'RBC', LB.LBSTRESN = 3.8, LB.LBSTNRLO = 3.9, LB.VISITNUM = 1
            *   LB.LBTESTCD = 'MCV', LB.LBSTRESN = 101, LB.LBSTNRHI = 100, LB.VISITNUM = 4
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [27b]
    *   **確認事項No.:** I-3 (関連指摘No.: P-2)
        *   **臨床試験結果/安全性への影響度合い:** Minor
        *   **疑義事項/確認内容:** 既往歴の Eating disorder (2009年) が除外基準[14] (5年以内の精神疾患歴) に該当するか、プロトコルの定義および治験責任医師の判断根拠を確認する。
        *   **判断理由:** プロトコル遵守の確認。日付から5年以内に該当する可能性は低いが、"mental illness" の解釈を確認するため内部記録とする。
        *   **判断根拠:**
            *   MH.MHTERM = 'VERBATIM_0702', MH.MHDECOD = 'EATING DISORDER', MH.MHSTDTC = '2009'
            *   プロトコル Section 3.4.2.2 Exclusion Criteria [14]