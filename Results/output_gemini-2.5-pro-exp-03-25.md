# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    77歳、男性、人種: WHITE、民族: NOT HISPANIC OR LATINO。 (DM.AGE=77, DM.SEX=M, DM.RACE=WHITE, DM.ETHNIC=NOT HISPANIC OR LATINO)

*   **イベント推移:**
    *   2013年09月20日 (Day -16): スクリーニング。ベースライン検査実施。クレアチニンが高値 (LB.LBTESTCD='CREAT', LBSTRESC=159.12 umol/L, LBNRIND='HIGH')。既往歴としてアルツハイマー病、心血管系疾患（心筋梗塞、CABG等）あり (MH)。
    *   2013年10月06日 (Day 1): 治験薬 Xanomeline 54mg/日 投与開始 (EX.EXTRT='XANOMELINE', EXDOSE=54, EXSTDY=1)。ベースライン有効性評価実施 (QS)。ADAS-Cog(11) 27点、NPI-X Total 61点。併用薬 Premarin 投与開始 (CM.CMTRT='PREMARIN', CMSTDY=1)。
    *   2013年10月19日 (Day 14): 有害事象「MYOCARDIAL INFARCTION」(Mild) 発現 (AE.AETERM='MYOCARDIAL INFARCTION', AESEV='MILD', AESTDY=14)。有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」(Severe) 発現 (AE.AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', AESEV='SEVERE', AESTDY=14)。有害事象「VENTRICULAR SEPTAL DEFECT」(Mild) 発現 (AE.AETERM='VENTRICULAR SEPTAL DEFECT', AESEV='MILD', AESTDY=14)。BUNが一過性に高値 (LB.LBTESTCD='BUN', LBNRIND='HIGH')。アルブミンが低値 (LB.LBTESTCD='ALB', LBNRIND='LOW')。NPI-X評価実施 (QS.QSDY=14)。
    *   2013年10月20日 (Day 15): 治験薬 Xanomeline 81mg/日 に増量 (EX.EXTRT='XANOMELINE', EXDOSE=81, EXSTDY=15)。
    *   2013年10月29日 (Day 24): 併用薬 Premarin 投与終了 (CM.CMTRT='PREMARIN', CMENDY=24)。
    *   2013年11月01日 (Day 27): 検査実施。アルブミンが低値継続 (LB.LBTESTCD='ALB', LBNRIND='LOW')。BUNは正常化。クレアチニンは正常範囲内。
    *   2013年11月05日 (Day 31): 有害事象「RASH」(Mild) 発現 (AE.AETERM='RASH', AESEV='MILD', AESTDY=31)。有害事象「PRURITUS」(Mild) 発現 (AE.AETERM='PRURITUS', AESEV='MILD', AESTDY=31)。いずれも治験薬との関連性は Probable。
    *   2013年11月06日 (Day 32): 併用薬 Hydrocortisone topical 投与開始 (CM.CMTRT='HYDROCORTISONE, TOPICAL', CMSTDY=32)。
    *   2013年11月09日 (Day 35): NPI-X評価実施 (QS.QSDY=35)。
    *   2013年11月18日 (Day 44): 有害事象「BRAIN DEATH」(Severe) 発現 (AE.AETERM='BRAIN DEATH', AESEV='SEVERE', AESTDY=44)。有害事象「LATE EFFECTS OF CEREBRAL INFARCTION」終了 (AEENDY=44)。治験薬 Xanomeline 投与終了 (EX.EXENDY=44)。
    *   2013年11月19日 (Day 45): 有害事象「MYOCARDIAL INFARCTION」終了 (AEENDY=45)。
    *   2013年11月22日 (Day 48): 有害事象「RASH」「PRURITUS」終了 (AEENDY=48)。併用薬 Hydrocortisone topical 投与終了 (CMENDY=48)。
    *   2013年11月24日 (Day 50): Week 6 有効性評価実施 (QS)。ADAS-Cog(11) 30点 (ベースラインから3点悪化)、CIBIC+ 4 (No Change)、NPI-X Total 16点 (ベースラインから改善)。有害事象「BRAIN DEATH」終了 (AEOUT='RECOVERED/RESOLVED', AEENDY=44)。治験中止 (DS.DSDECOD='ADVERSE EVENT', DSSTDY=50)。
    *   2013年12月06日: AEフォローアップ Visit (SV.VISIT='AE FOLLOW-UP')。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** ベースラインのクレアチニン値が基準値上限を超えて高値 (LB.LBTESTCD='CREAT', LBSTRESC=159.12 umol/L, LBSTNRHI=141)。プロトコル除外基準 EXCL27b (Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in ... creatinine) に抵触する可能性がある。Reference Range III の具体的な閾値は不明だが、腎機能低下が示唆され、治験参加の適格性に疑義がある。
        *   **根拠:** LB.LBTESTCD='CREAT', LB.VISITNUM=1, LBSTRESC=159.12, LBSTNRHI=141, LBNRIND='HIGH'; Protocol Section 3.4.2.2 [27b]
    *   **指摘No.:** M-2
        *   **重要度:** Critical
        *   **内容:** 重篤と考えられる有害事象（LATE EFFECTS OF CEREBRAL INFARCTION (Severe), BRAIN DEATH (Severe)）が報告されているにも関わらず、重篤性フラグ (AESER) が全て "N" (非重篤) となっている。プロトコル 3.9.3.2.2 の Serious Adverse Event の定義（生命を脅かす、入院、永続的な障害など）に基づくと、これらの事象は重篤に該当する可能性が高い。重篤性の評価が不適切である可能性があり、規制当局への報告義務にも影響する。
        *   **根拠:** AE.AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', AE.AESEV='SEVERE', AE.AESER='N'; AE.AETERM='BRAIN DEATH', AE.AESEV='SEVERE', AE.AESER='N'; Protocol Section 3.9.3.2.2
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 併用薬 Premarin (ESTROGENS CONJUGATED) の投与開始日 (CMSTDTC=2013-10-06) が治験薬開始日 (DM.RFSTDTC=2013-10-06) と同日であり、プロトコル 3.4.2.2 [31b] v) で要求されている「投与量が少なくとも3ヶ月間安定していること」という条件を満たしていない可能性がある。
        *   **根拠:** CM.CMTRT='PREMARIN', CMSTDTC='2013-10-06'; DM.RFSTDTC='2013-10-06'; Protocol Section 3.4.2.2 [31b] v)
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 有害事象「MYOCARDIAL INFARCTION」(AESEQ=1, AESTDY=14) が Mild と報告されているが、MH に心筋梗塞の既往歴があり、本症例は心血管リスクが高い。Mild という重症度評価、および治験薬との関連性評価 (AEREL=NONE) が妥当か、医学的に慎重な評価が必要。また、この AE により治験薬が中止された (AEACN=DRUG WITHDRAWN) と記録されているが、実際の投与は Day 44 まで継続されており矛盾がある (D-1参照)。
        *   **根拠:** AE.AETERM='MYOCARDIAL INFARCTION', AESEV='MILD', AEREL='NONE', AEACN='DRUG WITHDRAWN', AESTDY=14; MH.MHDECOD='MYOCARDIAL INFARCTION'; EX.EXENDY=44
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「VENTRICULAR SEPTAL DEFECT」(AESEQ=2, AESTDY=14) が報告されている。これは通常先天性疾患であり、77歳男性で新規に発現・診断されることは考えにくい。報告内容（事象名、発現日）の妥当性に疑義がある。MH に関連記載はない。
        *   **根拠:** AE.AETERM='VENTRICULAR SEPTAL DEFECT', AESTDY=14; DM.AGE=77, DM.SEX=M
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** 治験薬投与中に血圧低下傾向が認められる (例: Day 1 立位 SYSBP 120-130 mmHg → Day 14 立位 SYSBP 104-106 mmHg)。Xanomeline はコリン作動薬であり、血圧低下は薬理作用として想定されうる。一般的な医学的知見に基づくと、起立性低血圧等のリスクに注意が必要だが、記録されている値自体は必ずしも異常とは言えない。
        *   **根拠:** VS.VSTESTCD='SYSBP', VSPOS='STANDING', VSSTRESN (Day 1 vs Day 14, 35, 50)

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** AE ドメインで「MYOCARDIAL INFARCTION」(AESEQ=1) に対する治験薬の処置 (AEACN) が "DRUG WITHDRAWN" と記録されているが、EX ドメインでは治験薬 (Xanomeline) が Day 44 まで投与継続されている (EXENDY=44)。AEACN の記録と実際の投与状況が矛盾している。
        *   **根拠:** AE.AESEQ=1, AEACN='DRUG WITHDRAWN'; EX.USUBJID='01-704-1017', EXENDY=44
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「RASH」(AESEQ=5, 7) および「PRURITUS」(AESEQ=6, 8) が、それぞれ同一のイベントに対して重複して記録されているように見える。AESTDY, AEENDY は同一だが、AEOUT (転帰) が異なっている (NOT RECOVERED/NOT RESOLVED vs RECOVERED/RESOLVED)。RELREC でも関連付けられている (RELID=01-704-1017-E11)。データの更新・管理方法に問題がある可能性。
        *   **根拠:** AE.AESEQ=5, 7 (AETERM='RASH', AESTDY=31, AEENDY=48, AEOUT='NOT RECOVERED/NOT RESOLVED' vs 'RECOVERED/RESOLVED'); AE.AESEQ=6, 8 (AETERM='PRURITUS', AESTDY=31, AEENDY=48, AEOUT='NOT RECOVERED/NOT RESOLVED' vs 'RECOVERED/RESOLVED'); RELREC.RELID='01-704-1017-E11'
    *   **指摘No.:** D-3
        *   **重要度:** Critical
        *   **内容:** DS ドメインで治験中止理由が「ADVERSE EVENT」(DSDECOD='ADVERSE EVENT', DSSTDY=50) と記録されているが、中止の原因となった具体的な有害事象が特定できない。RELREC では RASH/PRURITUS (AESEQ=5, 7) が関連付けられているが、医学的には BRAIN DEATH (AESEQ=3, AESTDY=44) や MYOCARDIAL INFARCTION (AESEQ=1, AESTDY=14) が中止理由としてより考えられる。中止日 (DSSTDY=50) も AE 終了日や治験薬最終投与日 (EXENDY=44) とずれている。
        *   **根拠:** DS.DSDECOD='ADVERSE EVENT', DSSTDY=50; RELREC.IDVAR='DSSEQ', RELREC.IDVARVAL='1', RELREC.RELID='01-704-1017-E11'; AE.AESEQ=3, 4, 5, 6, 7, 8; EX.EXENDY=44
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** CM ドメインで ASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN の記録が Visit ごとに複数存在するが、投与期間 (CMSTDTC/CMENDTC) が重複または同一であり、冗長な記録となっている。
        *   **根拠:** CM.CMTRT='ASPIRIN', CM.CMTRT='HYDROCORTISONE, TOPICAL', CM.CMTRT='PREMARIN' の複数レコード
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** 重要な変数に欠損や不適切な値が見られる。
            *   AEACN (治験薬に対する処置): 多くの AE で空欄。特に重篤な可能性のある AE (AESEQ=3, 4) で空欄。
            *   AESER (重篤性): 全ての AE で "N"。医学的に重篤と考えられる事象が含まれる (M-2参照)。
            *   AEENDTC/AEENDY: AESEQ=2 (VENTRICULAR SEPTAL DEFECT) で欠損。
            *   CMDECOD/CMCLAS/CMINDC: HYDROCORTISONE, PREMARIN で未コード化または空欄。
            *   CMSTDTC: ASPIRIN で年のみ記録 ("2000")。
            *   CMENDTC: ASPIRIN で欠損。
            *   MHSTDTC: 一部 MH で欠損。
        *   **根拠:** AE, CM, MH ドメインの各変数

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** 患者が除外基準 [27b] (特定の臨床検査値異常) に抵触していた可能性がある。ベースラインのクレアチニン値が高値であり、プロトコルで規定された Reference Range III を超えていた可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LB.LBTESTCD='CREAT', LB.VISITNUM=1, LBNRIND='HIGH'
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 患者が除外基準 [31b] v) (特定の併用薬) に抵触していた可能性がある。Premarin の投与が治験開始前から3ヶ月以上安定していなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] v)
        *   **根拠:** CM.CMTRT='PREMARIN', CMSTDTC='2013-10-06'; DM.RFSTDTC='2013-10-06'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 有効性評価を含む Visit の実施タイミングが、プロトコルで規定された Visit Window から逸脱している。Visit 5 (Week 4) は予定 Day 28 に対して Day 35 (Window ±3日外)、Visit 7 (Week 6) は予定 Day 42 に対して Day 50 (Window ±3日外) に実施された。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Window の記載あり)
        *   **根拠:** SV.VISITNUM=5, SVSTDTC='2013-11-09' (Day 35); SV.VISITNUM=7, SVSTDTC='2013-11-24' (Day 50); TV.VISITNUM=5, VISITDY=28; TV.VISITNUM=7, VISITDY=42
    *   **指摘No.:** P-4
        *   **重要度:** Critical
        *   **逸脱の可能性:** 重篤な有害事象の報告手順が遵守されていない可能性がある。医学的に重篤と考えられる AE (脳梗塞後遺症、脳死) が非重篤 (AESER='N') として報告されている。
        *   **プロトコル該当箇所:** Section 3.9.3.2.2 (Serious Adverse Events の定義と報告義務)
        *   **根拠:** AE.AESEQ=3, 4, AESER='N'
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 患者が除外基準 [17] (5年以内の serious な心血管系疾患) に抵触していた可能性がある。MH に複数の心血管系既往歴があるが、一部開始日が不明なため、5年以内の該当イベントの有無が確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17]
        *   **根拠:** MH ドメイン (CARDIAC DISORDER, ST SEGMENT ELEVATED/DEPRESSED, EXTRASYSTOLES 等で MHSTDTC が欠損)
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 患者が選択基準 [3] (MMSE スコア 10-23) を満たしていなかった可能性がある。MMSE スコアデータが提供されていないため確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [3]
        *   **根拠:** QS ドメインに MMSE データなし

*   **有効性評価観点からの指摘事項:**
    *   **指摘No.:** E-1
        *   **重要度:** Minor
        *   **内容:** Week 6 (Visit 7) の有効性評価の実施日が、プロトコルで規定された Visit Window (Day 42 ± 3日) から逸脱している (Day 50 に実施)。評価タイミングのずれが結果に影響を与えた可能性は低いと考えられるが、プロトコル逸脱に該当する。
        *   **根拠:** QS.VISITNUM=7, QSDY=50; TV.VISITNUM=7, VISITDY=42; Protocol Section 3.1
    *   **指摘No.:** E-2
        *   **重要度:** Minor
        *   **内容:** 有効性評価の結果に一貫性が見られない。認知機能 (ADAS-Cog) は悪化している一方で、精神症状 (NPI-X) は改善傾向を示している。全般印象 (CIBIC+) は変化なし。これらの結果の乖離について、AE の影響や評価時期のずれなどを考慮して解釈する必要がある。
        *   **根拠:** QS.QSTESTCD='ACTOT' (Baseline 27 -> Week 6 30); QS.QSTESTCD='NPTOT' (Baseline 61 -> Week 6 16); QS.QSTESTCD='CIBIC' (Week 6 = 4)
    *   **指摘No.:** E-3
        *   **重要度:** Minor
        *   **内容:** DAD スコアの一部の項目で、ベースライン時に NA (Not Applicable) と評価されていたものが、Week 6 で評価可能 (Yes/No) になっている (DAITM04, DAITM30, DAITM31, DAITM32)。評価方法の一貫性について確認が必要かもしれないが、患者の状態変化による可能性もある。
        *   **根拠:** QS.QSTESTCD in ('DAITM04', 'DAITM30', 'DAITM31', 'DAITM32'), QSSTRESC (Visit 3 vs Visit 7)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-1)
        *   **重要度:** Critical
        *   **医療機関への問い合わせ文面:** "Screening Visit (Visit 1, 2013-09-20) で測定されたクレアチニン値 (1.8 mg/dL, 159.12 umol/L) が基準値上限 (1.6 mg/dL, 141 umol/L) を超えていました。プロトコル除外基準 Section 3.4.2.2 [27b] では、基準値を超える特定の検査値は除外対象とされています。当該患者が適格基準を満たしていたか、逸脱に該当しないと判断された根拠についてご確認ください。"
        *   **判断理由:** 選択/除外基準の違反は試験の妥当性に重大な影響を与えるため。
        *   **判断根拠:**
            *   LB.USUBJID='01-704-1017', LBTESTCD='CREAT', VISITNUM=1, LBORRES='1.8', LBORRESU='mg/dL', LBSTRESC='159.12', LBSTNRHI=141, LBNRIND='HIGH'
            *   Protocol Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-5, P-4)
        *   **重要度:** Critical
        *   **医療機関への問い合わせ文面:** "有害事象として LATE EFFECTS OF CEREBRAL INFARCTION (Severe, Day 14発現) および BRAIN DEATH (Severe, Day 44発現) が報告されていますが、重篤性 (AESER) が 'N' (非重篤) と記録されています。プロトコル Section 3.9.3.2.2 の重篤な有害事象の定義に基づき、これらの事象の重篤性評価 (AESER および関連する AESDTH, AESHOSP, AESLIFE, AESDISAB 等) が適切であったか再確認し、必要であれば修正をお願いします。"
        *   **判断理由:** 重篤な有害事象の評価と報告は患者の安全性および規制要件遵守の観点から極めて重要であるため。
        *   **判断根拠:**
            *   AE.USUBJID='01-704-1017', AESEQ=4, AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', AESEV='SEVERE', AESER='N'
            *   AE.USUBJID='01-704-1017', AESEQ=3, AETERM='BRAIN DEATH', AESEV='SEVERE', AESER='N'
            *   Protocol Section 3.9.3.2.2
    *   **クエリNo.:** Q-3 (関連指摘No.: M-4, D-1)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "有害事象 MYOCARDIAL INFARCTION (AESEQ=1, Day 14発現) について、AEACN が 'DRUG WITHDRAWN' と記録されていますが、EX ドメインでは治験薬投与が Day 44 まで継続されています。実際の治験薬に対する処置（中止、中断、用量変更なし等）と、もし中止された場合はその日付を明確にしてください。"
        *   **判断理由:** 有害事象発生時の治験薬の処置に関する記録の矛盾は、安全性評価に影響するため。
        *   **判断根拠:**
            *   AE.USUBJID='01-704-1017', AESEQ=1, AEACN='DRUG WITHDRAWN', AESTDY=14
            *   EX.USUBJID='01-704-1017', EXENDY=44
    *   **クエリNo.:** Q-4 (関連指摘No.: D-3)
        *   **重要度:** Critical
        *   **医療機関への問い合わせ文面:** "治験中止記録 (DS) によると、中止理由は 'ADVERSE EVENT' (Day 50) となっています。中止の直接的な原因となった有害事象名を具体的に特定し、ご報告ください。また、中止日 (Day 50) が治験薬最終投与日 (Day 44) や関連する可能性のある AE の終了日と異なりますが、中止日が Day 50 で正しいかご確認ください。"
        *   **判断理由:** 治験中止理由の特定と日付の正確性は、安全性評価および試験結果の解釈に不可欠であるため。
        *   **判断根拠:**
            *   DS.USUBJID='01-704-1017', DSDECOD='ADVERSE EVENT', DSSTDY=50
            *   AE.USUBJID='01-704-1017' (複数のAEあり)
            *   EX.USUBJID='01-704-1017', EXENDY=44
    *   **クエリNo.:** Q-5 (関連指摘No.: M-3, P-2)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "併用薬 Premarin (Estrogens Conjugated) について、投与開始日 (CMSTDTC) が 2013-10-06 (Day 1) と記録されています。プロトコル Section 3.4.2.2 [31b] v) では、Estrogen supplements は投与量が少なくとも3ヶ月間安定している場合にのみ許可されています。治験参加前に3ヶ月以上の安定投与期間があったかご確認ください。もし治験開始時からの新規投与であれば、プロトコル逸脱に該当する可能性があります。"
        *   **判断理由:** 併用禁止/制限薬に関するプロトコル遵守状況を確認するため。
        *   **判断根拠:**
            *   CM.USUBJID='01-704-1017', CMTRT='PREMARIN', CMSTDTC='2013-10-06'
            *   Protocol Section 3.4.2.2 [31b] v)
    *   **クエリNo.:** Q-6 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "Medical History に複数の心血管系既往歴が記録されていますが、一部 (CARDIAC DISORDER, ST SEGMENT ELEVATED/DEPRESSED, EXTRASYSTOLES 等) で発症/診断年月日 (MHSTDTC) が不明です。プロトコル除外基準 Section 3.4.2.2 [17] (過去5年以内の serious な心血管系疾患) に抵触する既往歴がなかったか、可能な範囲で発症/診断時期をご確認ください。"
        *   **判断理由:** 患者の適格性確認のため。
        *   **判断根拠:**
            *   MH.USUBJID='01-704-1017', MHDECOD in ('CARDIAC DISORDER', 'ELECTROCARDIOGRAM ST SEGMENT ELEVATION', 'ELECTROCARDIOGRAM ST SEGMENT DEPRESSION', 'EXTRASYSTOLES'), MHSTDTC=(Missing)
            *   Protocol Section 3.4.2.2 [17]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "選択基準 Section 3.4.2.1 [3] では、MMSE スコアが 10-23 であることが規定されています。スクリーニング時に実施された MMSE のスコアをご報告ください。"
        *   **判断理由:** 患者の適格性確認のため。
        *   **判断根拠:**
            *   Protocol Section 3.4.2.1 [3]
            *   QS ドメインに MMSE データなし
    *   **クエリNo.:** Q-8 (関連指摘No.: P-3, E-1)
        *   **重要度:** Minor
        *   **医療機関への問い合わせ文面:** "Visit 5 (Week 4) および Visit 7 (Week 6) の実施日が、プロトコルで規定された Visit Window (それぞれ Day 28±3日、Day 42±3日) から逸脱していました (実施日: Day 35, Day 50)。逸脱理由について記録があればお知らせください。"
        *   **判断理由:** プロトコル逸脱の理由を確認・記録するため。
        *   **判断根拠:**
            *   SV.USUBJID='01-704-1017', VISITNUM=5, SVSTDTC='2013-11-09' (Day 35)
            *   SV.USUBJID='01-704-1017', VISITNUM=7, SVSTDTC='2013-11-24' (Day 50)
            *   Protocol Section 3.1
    *   **クエリNo.:** Q-9 (関連指摘No.: M-5, D-5)
        *   **重要度:** Minor
        *   **医療機関への問い合わせ文面:** "有害事象 VENTRICULAR SEPTAL DEFECT (AESEQ=2, Day 14発現) について、報告内容をご確認ください。これは通常先天性疾患ですが、77歳での新規発現として報告されています。また、終了日 (AEENDTC) が欠損しています。事象の確認と終了日の追記をお願いします。"
        *   **判断理由:** 報告内容の医学的妥当性の確認とデータ欠損の補完のため。
        *   **判断根拠:**
            *   AE.USUBJID='01-704-1017', AESEQ=2, AETERM='VENTRICULAR SEPTAL DEFECT', AESTDY=14, AEENDTC=(Missing)
            *   DM.AGE=77

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** AE ドメインにおいて、RASH (AESEQ=5, 7) および PRURITUS (AESEQ=6, 8) が重複して記録され、転帰 (AEOUT) が異なっている。RELREC の情報から同一イベントの記録不備と判断。データマネジメント部門にてデータクリーニング要否を検討。
        *   **判断理由:** データの一貫性に関わる問題だが、医療機関への問い合わせで解決する性質のものではなく、内部でのデータ処理の問題と考えられるため。
        *   **判断根拠:**
            *   AE.USUBJID='01-704-1017', AESEQ=5, 7; AESEQ=6, 8
            *   RELREC.RELID='01-704-1017-E11'
    *   **確認事項No.:** I-2 (関連指摘No.: D-4, D-5)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** CM ドメインの ASPIRIN, HYDROCORTISONE, PREMARIN の記録が冗長である。また、ASPIRIN の開始年のみ記録、終了日欠損、HYDROCORTISONE, PREMARIN のコード化情報欠損が見られる。データ標準と品質に関する問題として記録。
        *   **判断理由:** データ入力・構造上の問題であり、内部でのデータ標準化や品質管理プロセスで対応すべき事項のため。
        *   **判断根拠:**
            *   CM.USUBJID='01-704-1017'
    *   **確認事項No.:** I-3 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** AEACN (治験薬に対する処置) や MHSTDTC (既往歴開始日) の欠損が多い。今後のデータ収集・入力品質向上のための参考情報として記録。
        *   **判断理由:** データ完全性に関する問題だが、個別の問い合わせで全て解決するとは限らず、全体的な品質改善の観点から内部で記録・検討すべき事項のため。
        *   **判断根拠:**
            *   AE.USUBJID='01-704-1017', AEACN=(Missing)
            *   MH.USUBJID='01-704-1017', MHSTDTC=(Missing)
    *   **確認事項No.:** I-4 (関連指摘No.: E-2)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** 有効性評価項目間で結果の傾向に乖離が見られる (ADAS-Cog悪化 vs NPI-X改善)。AE の影響や評価時期のずれも考慮し、統計解析および結果解釈時に留意する。
        *   **判断理由:** データ間の解釈に関する事項であり、医療機関への問い合わせではなく、内部での解析・考察で対応すべき事項のため。
        *   **判断根拠:**
            *   QS.USUBJID='01-704-1017' (ADAS-Cog, NPI-X, CIBIC+ の結果)
    *   **確認事項No.:** I-5 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** VS データで血圧低下傾向が認められる。薬理作用として想定されうる範囲であり、現時点で追加のアクションは不要だが、安全性モニタリングの一環として記録。
        *   **判断理由:** 医学的に想定される変動であり、安全性上の懸念が直ちに生じるレベルではないため、内部記録に留める。
        *   **判断根拠:**
            *   VS.USUBJID='01-704-1017', VSTESTCD='SYSBP', 'DIABP'

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    64歳、男性、白人、非ヒスパニックまたはラティーノ。本試験ではPlacebo群に割り付けられた (計画/実績)。米国在住。教育歴12年。

*   **イベント推移:**
    *   不明 (2008年07月23日): 既往歴としてアルツハイマー病と診断 (MH.MHTERM='ALZHEIMER'S DISEASE', MH.MHSTDTC='2008-07-23')。
    *   不明 (2009年): 既往歴として腸ポリープ切除術 (MH.MHTERM='INTESTINAL POLYPECTOMY', MH.MHSTDTC='2009')。
    *   不明 (2009年): ビタミンC (500mg QD)、ビタミンE (200mg QD) 服用開始 (CM.CMTRT='VITAMIN C'/'VITAMIN E', CM.CMSTDTC='2009')。
    *   不明: 既往歴として肺気腫 (軽度)、冠動脈疾患 (軽度)、関節炎 (軽度) あり (MH.MHTERM='VERBATIM_0087'/'VERBATIM_0409'/'VERBATIM_1309')。
    *   不明 (1997年): 既往歴として肺膿瘍ドレナージ術 (MH.MHTERM='VERBATIM_1084', MH.MHSTDTC='1997')。
    *   2013年01月27日 (Day -34): Norvasc (Amlodipine) 5mg QD 服用開始 (CM.CMTRT='NORVASC', CM.CMSTDTC='2013-01-27')。
    *   2012年12月27日 (Day -65): Screening 1 Visit。
        *   ALT 135 U/L (HIGH, 基準値上限43の約3.1倍)、AST 145 U/L (HIGH, 基準値上限36の約4.0倍) (LB.LBTESTCD='ALT'/'AST')。
        *   MMSE Total Score 23点 (計算値)、Modified Hachinski Ischemic Score 1点 (計算値) (QS)。
    *   2013年02月21日 (Day -9): Unscheduled Visit 1.1。
        *   ALT 19 U/L (NORMAL)、AST 29 U/L (NORMAL) (LB.LBTESTCD='ALT'/'AST')。
        *   Sodium 133 mEq/L (LOW, 基準値 135-145) (LB.LBTESTCD='SODIUM')。
    *   2013年03月02日 (Day 1): Baseline Visit。治験薬 Placebo 投与開始 (EX.EXTRT='PLACEBO', EX.EXSTDTC='2013-03-02')。
        *   ADAS-Cog(11) Total Score 14点 (QS.QSTESTCD='ACTOT')。
        *   NPI-X Total Score 3点 (QS.QSTESTCD='NPTOT')。
    *   2013年03月04日 (Day 3): 有害事象「Diarrhoea」(MILD) 発現 (AE.AETERM='DIARRHOEA', AE.AESTDTC='2013-03-04')。
    *   2013年03月05日 (Day 4):
        *   有害事象「Diarrhoea」(MILD) 回復 (AE.AEENDTC='2013-03-05')。
        *   有害事象「Insomnia」(MILD) 発現 (AE.AETERM='INSOMNIA', AE.AESTDTC='2013-03-05')。
        *   Kaopectate 1 Tbsp ONCE 服用 (Diarrhoeaに対する処置) (CM.CMTRT='KAOPECTATE', CM.CMSTDTC='2013-03-05', CM.CMENDTC='2013-03-05')。
    *   2013年03月06日 (Day 5): 有害事象「Insomnia」(MILD) 回復 (AE.AEENDTC='2013-03-06')。
    *   2013年03月28日 (Day 27): Week 4 Visit。
        *   Sodium 146 mEq/L (HIGH, 基準値 135-145) (LB.LBTESTCD='SODIUM')。
        *   MCV 101 fL (HIGH, 基準値 80-100) (LB.LBTESTCD='MCV')。
        *   Anisocytes 1 (ABNORMAL) (LB.LBTESTCD='ANISO')。
    *   2013年04月27日 (Day 57): Week 8 Visit。
        *   ADAS-Cog(11) Total Score 9点 (QS.QSTESTCD='ACTOT')。
    *   2013年06月22日 (Day 113): Week 16 Visit。
        *   ADAS-Cog(11) Total Score 7点 (QS.QSTESTCD='ACTOT')。
        *   CIBIC+ Score 4 (No Change) (QS.QSTESTCD='CIBIC')。
    *   2013年08月09日 (Day 161): Week 24 Visit。
        *   ADAS-Cog(11) Total Score 9点 (QS.QSTESTCD='ACTOT')。
        *   CIBIC+ Score 4 (No Change) (QS.QSTESTCD='CIBIC')。
    *   2013年08月31日 (Day 183): Week 26 Visit (最終Visit)。
        *   AST 38 U/L (HIGH, 基準値 11-36) (LB.LBTESTCD='AST')。
        *   治験完了 (DS.DSDECOD='COMPLETED')。
        *   治験薬 Placebo 投与終了 (EX.EXENDTC='2013-08-31')。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Screening Visit 1 (Day -65) において、ALT (135 U/L, 基準値上限の約3.1倍) および AST (145 U/L, 基準値上限の約4.0倍) の高値が認められた。これはプロトコルの除外基準 [27b] に抵触する可能性があった。しかし、Unscheduled Visit 1.1 (Day -9) で正常化しており、治験参加は継続された。Screening時の高値の原因は不明だが、一過性であったと考えられる。
        *   **根拠:** LB.LBTESTCD='ALT', LB.LBSTRESN=135, LB.LBSTNRHI=43 (Day -65); LB.LBTESTCD='AST', LB.LBSTRESN=145, LB.LBSTNRHI=36 (Day -65); LB.LBTESTCD='ALT'/'AST', LB.LBNRIND='NORMAL' (Day -9); Protocol Section 3.4.2.2 [27b].
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 27) にMCVの軽度高値 (101 fL, 基準値 80-100) および Anisocytes 異常が認められた。貧血やビタミン欠乏との明確な関連はなく、その後の検査では正常化しているため、臨床的意義は低い可能性が高い。
        *   **根拠:** LB.LBTESTCD='MCV', LB.LBSTRESN=101, LB.LBNRIND='HIGH' (Day 27); LB.LBTESTCD='ANISO', LB.LBSTRESC='1', LB.LBNRIND='ABNORMAL' (Day 27); LB.LBTESTCD='HGB'/'HCT' (正常範囲); LB.LBTESTCD='VITB12' (Screening時正常).

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** CMドメインにて、Vitamin C (CMSEQ=1など) および Vitamin E (CMSEQ=2など) の開始日 (CMSTDTC) が '2009' と年のみ記録されており、Study Day (CMSTDY) が欠損している。
        *   **根拠:** CM.CMTRT='VITAMIN C'/'VITAMIN E', CM.CMSTDTC='2009', CM.CMSTDY=null.
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** CMドメインのKaopectate (CMSEQ=13) について、薬剤の投与日 (CMSTDTC/CMENDTC) は2013-03-05 (Day 4) と記録されているが、収集日 (CMDTC) が2013-03-14 (Day 13) と大きく乖離している。記録日の誤りか確認が必要。
        *   **根拠:** CM.CMSEQ=13, CM.CMSTDTC='2013-03-05', CM.CMENDTC='2013-03-05', CM.CMDTC='2013-03-14'.
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** CMドメインにて、Norvasc, Vitamin C, Vitamin E の Indication (CMINDC) が欠損している。
        *   **根拠:** CM.CMTRT='NORVASC'/'VITAMIN C'/'VITAMIN E', CM.CMINDC=''.
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** CMドメインのKaopectate (CMSEQ=13) について、薬剤名が標準化されておらず (CMDECOD=UNCODED)、適応 (CMINDC) および薬剤分類 (CMCLAS) が欠損している。AEのDiarrhoeaとの関連が推測されるが、確認が必要。
        *   **根拠:** CM.CMSEQ=13, CM.CMDECOD='UNCODED', CM.CMINDC='', CM.CMCLAS='UNCODED'.
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** CMドメインにて、Vitamin C (CMSEQ=1など) および Vitamin E (CMSEQ=2など) の標準薬剤名 (CMDECOD) および薬剤分類 (CMCLAS) が 'UNCODED' となっている。標準化が必要。
        *   **根拠:** CM.CMTRT='VITAMIN C'/'VITAMIN E', CM.CMDECOD='UNCODED', CM.CMCLAS='UNCODED'.
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** AEドメインにて、報告された有害事象 (Diarrhoea, Insomnia) のMedDRA関連コード (AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCD) が欠損している。
        *   **根拠:** AE.AESEQ=1, 2 における各種コード変数が null.
    *   **指摘No.:** D-7
        *   **重要度:** Major
        *   **内容:** MHドメインにて、一部の既往歴 (MHTERM='ALZHEIMER'S DISEASE', 'VERBATIM_XXXX') でMedDRA関連コード (MHLLT, MHDECOD, MHHLT, MHHLGT) が欠損またはVerbatimのままとなっている。また、一部の既往歴で開始日 (MHSTDTC) が欠損している。
        *   **根拠:** MHドメインの各レコードにおけるコード変数および MHSTDTC の値。
    *   **指摘No.:** D-8
        *   **重要度:** Major
        *   **内容:** LBドメインに、Screeningで測定が必要な Folate のデータが存在しない。
        *   **根拠:** LBデータに LBTESTCD='FOLATE' のレコードが存在しない。Protocol Section 3.4.2.2 [28b].
    *   **指摘No.:** D-9
        *   **重要度:** Major
        *   **内容:** LBドメインのUrinalysisについて、Screening Visit 1で測定が必要とプロトコルに記載されている項目 (Protein, Blood, Nitrite, Microscopic examination) のデータが存在しない。
        *   **根拠:** LBデータに Visit 1 における該当 LBTESTCD のレコードが存在しない。Protocol Section 3.9.3.3 Table LZZT.1.

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening時のALT/AST高値により、除外基準 [27b] に抵触していた可能性がある。再検査で正常化したため最終的に組み入れられたと推測されるが、逸脱と判断されなかった根拠の記録が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LB.LBTESTCD='ALT'/'AST' (Day -65) の値。
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [28b] の確認に必要な Folate の検査データが欠損しており、適格性評価が不十分であった可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [28b]
        *   **根拠:** LBデータに LBTESTCD='FOLATE' のレコードが存在しない。
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening時に実施すべきUrinalysisの一部項目 (Protein, Blood, Nitrite, Microscopic examination) が未測定または未報告であり、プロトコル規定の安全性評価が遵守されていない可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.3 Table LZZT.1
        *   **根拠:** LBデータに Visit 1 における該当 LBTESTCD のレコードが存在しない。
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 12 (Week 24) の実施日 (Day 161) が、プロトコルで規定されたVisit Window (Day 164-172) から逸脱している。
        *   **プロトコル該当箇所:** Section 3.1 (Visit Window規定)
        *   **根拠:** SV.VISITNUM=12, SV.SVSTDTC='2013-08-09' (Day 161); TV.VISITNUM=12, TV.VISITDY=168.

*   **有効性評価観点からの指摘事項:**
    *   **指摘No.:** E-1
        *   **重要度:** Minor
        *   **内容:** DAD (Disability Assessment for Dementia) の個々の項目において、ベースラインからWeek 24にかけて改善・悪化・変動が見られ、一貫性に欠けるように見える箇所がある。ただし、Placebo群であり、全体スコアでの評価が主となるため、現時点での臨床的意義は限定的と考えられる。Visit 12の実施日逸脱 (P-4) が影響している可能性も考慮。
        *   **根拠:** QSドメインの DAITM** レコード (例: DAITM20, 24, 29, 30-33, 34, 37-39)。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **医療機関への問い合わせ文面:** "CMドメインのKaopectate (CMSEQ=13) について、薬剤の投与日 (CMSTDTC/CMENDTC) は2013-03-05 (Day 4) と記録されていますが、収集日 (CMDTC) が2013-03-14 (Day 13) となっています。収集日が正しいかご確認ください。もし記録誤りであれば修正をお願いします。"
        *   **判断理由:** データ収集日と実際のイベント日の乖離はデータの正確性に影響するため確認が必要。
        *   **判断根拠:**
            *   CM.CMSEQ=13, CM.CMSTDTC='2013-03-05', CM.CMENDTC='2013-03-05', CM.CMDTC='2013-03-14'
    *   **クエリNo.:** Q-2 (関連指摘No.: D-4)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "CMドメインのKaopectate (CMSEQ=13) について、薬剤名が標準化されておらず (CMDECOD=UNCODED)、適応 (CMINDC) および薬剤分類 (CMCLAS) が欠損しています。AEとしてDiarrhoeaが報告されていますが、本薬剤の適応がDiarrhoeaであったかご確認ください。また、可能であれば標準薬剤名をご提供ください。"
        *   **判断理由:** 併用薬の正確な特定と適応の確認は安全性評価に重要であるため。
        *   **判断根拠:**
            *   CM.CMSEQ=13, CM.CMDECOD='UNCODED', CM.CMINDC='', CM.CMCLAS='UNCODED'
            *   AE.AETERM='DIARRHOEA' (AESEQ=1)
    *   **クエリNo.:** Q-3 (関連指摘No.: D-8, P-2)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "Screening Visit 1で測定が必要な検査項目のうち、Folateの結果が報告されていません。プロトコル 3.4.2.2 [28b] の除外基準確認に必要です。測定状況と結果についてご確認ください。もし未測定の場合は理由をお知らせください。"
        *   **判断理由:** 選択/除外基準の遵守確認に必須の検査データが欠損しているため。
        *   **判断根拠:**
            *   LBデータに LBTESTCD='FOLATE' のレコードが存在しない
            *   プロトコル該当箇所: Section 3.4.2.2 [28b]
    *   **クエリNo.:** Q-4 (関連指摘No.: D-9, P-3)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "Screening Visit 1で実施されたUrinalysisについて、プロトコル 3.9.3.3 Table LZZT.1 に記載のある Protein, Blood, Nitrite, Microscopic examination の結果が報告されていません。測定状況と結果についてご確認ください。もし未測定の場合は理由をお知らせください。"
        *   **判断理由:** プロトコルで規定されたScreening時の安全性評価項目が欠損しているため。
        *   **判断根拠:**
            *   LBデータに Visit 1 における該当 LBTESTCD のレコードが存在しない
            *   プロトコル該当箇所: Section 3.9.3.3 Table LZZT.1
    *   **クエリNo.:** Q-5 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "Visit 12 (Week 24) の実施日 (SVSTDTC = 2013-08-09, Day 161) が、プロトコル 3.1 で規定されたVisit Window (計画日 Day 168 ± 4日 = Day 164-172) から逸脱しています。逸脱理由についてご確認ください。"
        *   **判断理由:** 主要評価時期のVisit Window逸脱は有効性評価の信頼性に影響を与える可能性があるため、理由の確認が必要。
        *   **判断根拠:**
            *   SV.VISITNUM=12, SV.SVSTDTC='2013-08-09' (Day 161)
            *   TV.VISITNUM=12, TV.VISITDY=168
            *   プロトコル該当箇所: Section 3.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-1, P-1)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** Screening Visit 1 (Day -65) でALT (135 U/L), AST (145 U/L) が基準値上限を大幅に超えていたが、Unscheduled Visit 1.1 (Day -9) で正常化し、治験参加が継続された。プロトコル 3.4.2.2 [27b] の除外基準に抵触する可能性があったが、再検査結果に基づき適格と判断された経緯を記録する。
        *   **判断理由:** 選択基準に関する重要な逸脱の可能性があったが、治験開始前に解決しており、治験も完了しているため、医療機関への問い合わせは不要と判断。経緯の記録は必要。
        *   **判断根拠:**
            *   LB.LBTESTCD='ALT'/'AST' (Day -65, Day -9)
            *   プロトコル該当箇所: Section 3.4.2.2 [27b]
    *   **確認事項No.:** I-2 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** Week 4 (Day 27) にMCV (101 fL) の軽度高値とAnisocytes (Abnormal) が認められたが、その後の検査では正常化している。臨床的意義は低いと判断。記録として残す。
        *   **判断理由:** 軽度かつ一過性の検査値異常であり、他のデータとの関連も薄いため問い合わせ不要。記録として残す。
        *   **判断根拠:**
            *   LB.LBTESTCD='MCV', LB.LBNRIND='HIGH' (Day 27)
            *   LB.LBTESTCD='ANISO', LB.LBNRIND='ABNORMAL' (Day 27)
    *   **確認事項No.:** I-3 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** CMドメインにて、Vitamin C (CMSEQ=1など) および Vitamin E (CMSEQ=2など) の開始日 (CMSTDTC) が '2009' と年のみ記録されており、Study Day (CMSTDY) が欠損している。長期使用のサプリメントであり、治験期間中の使用は確認されているため、現時点での問い合わせは不要と判断。記録として残す。
        *   **判断理由:** データの完全性の問題だが、長期使用のサプリメントであり、治験の主要評価への影響は小さいと判断されるため。
        *   **判断根拠:**
            *   CM.CMTRT='VITAMIN C'/'VITAMIN E', CM.CMSTDTC='2009', CM.CMSTDY=null
    *   **確認事項No.:** I-4 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** CMドメインにて、Norvasc, Vitamin C, Vitamin E の Indication (CMINDC) が欠損している。NorvascはMHの心疾患、Vitamin C/Eは"PROPHYLAXIS OR NON-THERAPEUTIC USE"との記載から、欠損の影響は限定的と判断。記録として残す。
        *   **判断理由:** 適応が他情報から推測可能、または非治療目的であるため、問い合わせの優先度は低い。
        *   **判断根拠:**
            *   CM.CMTRT='NORVASC'/'VITAMIN C'/'VITAMIN E', CM.CMINDC=''
            *   MH.MHTERM='VERBATIM_0409' (Coronary Artery Disease)
            *   CM.CMINDC='PROPHYLAXIS OR NON-THERAPEUTIC USE' (Vitamin C/E)
    *   **確認事項No.:** I-5 (関連指摘No.: D-5)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** CMドメインにて、Vitamin C (CMSEQ=1など) および Vitamin E (CMSEQ=2など) の標準薬剤名 (CMDECOD) および薬剤分類 (CMCLAS) が 'UNCODED' となっている。WHODrug等を用いた標準化が必要。内部データマネジメント/コーディングチームへ確認依頼。
        *   **判断理由:** データ標準化は解析に必須であり、内部での対応が必要なため。
        *   **判断根拠:**
            *   CM.CMTRT='VITAMIN C'/'VITAMIN E', CM.CMDECOD='UNCODED', CM.CMCLAS='UNCODED'
    *   **確認事項No.:** I-6 (関連指摘No.: D-6)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** AEドメインにて、Diarrhoea (AESEQ=1) および Insomnia (AESEQ=2) のMedDRA関連変数 (AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCD) が欠損している。MedDRAコーディングの実施状況を確認し、未完了であれば対応を依頼。
        *   **判断理由:** MedDRAコーディングは安全性解析に必須であり、内部での対応が必要なため。
        *   **判断根拠:**
            *   AE.AESEQ=1, 2 における各種コード変数が null
    *   **確認事項No.:** I-7 (関連指摘No.: D-7)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** MHドメインにて、一部の既往歴 (MHTERM='ALZHEIMER'S DISEASE', 'VERBATIM_XXXX') でMedDRA関連変数 (MHLLT, MHDECOD, MHHLT, MHHLGT) が欠損またはVerbatimのままとなっている。MedDRAコーディングの実施状況を確認し、未完了であれば対応を依頼。
        *   **判断理由:** 背景情報の標準化は解析に重要であり、内部での対応が必要なため。
        *   **判断根拠:**
            *   MHドメインの各レコードにおけるコード変数
    *   **確認事項No.:** I-8 (関連指摘No.: E-1)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** DADの個々の項目 (DAITM20, 24, 29, 30-33, 34, 37-39) で、ベースラインからWeek 24にかけて改善・悪化・変動が見られ、一貫性に欠けるように見える箇所がある。Placebo群であり個別の変動は起こりうるため、現時点では問い合わせ不要。全体スコアおよびサブスコアでの評価を注視する。Visit 12の実施日逸脱 (P-4) が影響している可能性も考慮。
        *   **判断理由:** Placebo群であり、個々の項目の変動は許容範囲と考えられる。全体スコアでの評価が主となるため。
        *   **判断根拠:**
            *   QSドメインの DAITM** レコード
            *   DM.ACTARM='Placebo'

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    81歳、女性、白人、非ヒスパニックまたはラティーノ (DM)。アルツハイマー病の既往歴あり (MH, 2009年発症)。教育歴22年 (SC)。

*   **イベント推移:**
    *   2012年07月08日 (Day -61): 併用薬「KEFLEX」開始 (CM)。同日、有害事象「LOCALISED INFECTION」(Moderate) 発現 (AE, 未回復のまま治験期間中継続)。
    *   2012年08月25日 (Day -13): スクリーニング1来院 (SV)。MMSE 23点相当 (QS)、Hachinskiスコア 1点 (QS)。身長 158.24 cm (VS)、体重 60.33 kg (VS)。検査にて赤血球数(RBC) 低値 (LB, 3.8 TI/L, 基準値 3.9-5.5)。
    *   2012年09月02日 (Day -5): 有害事象「ERYTHEMA」(Mild) 発現 (AE)。有害事象「PRURITUS」(Mild) 発現 (AE)。併用薬「HYDROCORTISONE, TOPICAL」開始 (CM)。
    *   2012年09月04日 (Day -3): 併用薬「HYDROCORTISONE, TOPICAL」終了 (CM)。
    *   2012年09月05日 (Day -2): スクリーニング2来院 (SV)。
    *   2012年09月07日 (Day 1): ベースライン来院 (SV)。治験薬「XANOMELINE」54 mg パッチ投与開始 (EX)。体重 59.88 kg (VS)。有害事象「ERYTHEMA」(Mild) および「PRURITUS」(Mild) 回復 (AE)。有害事象「MICTURITION URGENCY」(Mild) 発現 (AE, 未回復)。ADAS-Cog(11) スコア 7 (QS)、NPI-X Total スコア 2 (QS)。
    *   2012年09月13日 (Day 7): 有害事象「ARTHRALGIA」(Moderate) 発現 (AE, 未回復)。有害事象「CELLULITIS」(Moderate) 発現 (AE, 未回復)。
    *   2012年09月16日 (Day 10): 治験薬「XANOMELINE」54 mg パッチ投与終了 (EX)。
    *   2012年09月17日 (Day 11): Week 2 来院 (SV)。有害事象により治験中止 (DS)。体重 60.78 kg (VS)。検査にて赤血球数(RBC) 低値 (LB, 3.7 TI/L)、平均赤血球容積(MCV) 高値 (LB, 101 fL, 基準値 80-100)、尿比重(Specific Gravity) 低値 (LB, 1.004, 基準値 1.006-1.03)、Anisocytes 異常 (LB)。ADAS-Cog(11) スコア 5 (QS)、CIBIC+ スコア 4 (No Change) (QS)、NPI-X Total スコア 1 (QS)。
    *   2012年09月29日 (Day 23): AEフォローアップ来院 (SV, VISITNUM=101)。
    *   2013年02月22日 (Day 169): Retrieval来院 (SV, VISITNUM=201)。ADAS-Cog(11) スコア 9 (QS)、CIBIC+ スコア 5 (Minimal worsening) (QS)、NPI-X Total スコア 45 (QS)。

## 2. 統合レビュー結果

*   **医学的観点からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 7に発現した有害事象「ARTHRALGIA」(Moderate) および「CELLULITIS」(Moderate) が治験中止 (Day 11) の原因と記録されている (DS, RELREC)。しかし、AEドメインにおける治験薬との関連性評価 (AEREL) が "NONE" となっている。治験薬投与中に発現し、中止に至った有害事象の関連性評価が "NONE" であることは医学的に疑問があり、評価の再確認が必要。
        *   **根拠:** AE.AETERM = 'ARTHRALGIA', AE.AESEV = 'MODERATE', AE.AESTDY = 7, AE.AEREL = 'NONE'; AE.AETERM = 'CELLULITIS', AE.AESEV = 'MODERATE', AE.AESTDY = 7, AE.AEREL = 'NONE'; DS.DSDECOD = 'ADVERSE EVENT', DS.DSSTDY = 11; RELREC.RDOMAIN = 'AE', RELREC.IDVARVAL = '   7', RELREC.RELID = '01-701-1111-E16'; RELREC.RDOMAIN = 'DS', RELREC.IDVARVAL = '   1', RELREC.RELID = '01-701-1111-E16'; プロトコル 3.9.3.2.1 (AE報告要件)。
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** スクリーニング時 (Day -13) および Week 2 (Day 11) で赤血球数 (RBC) が基準値下限を下回っている (LB.LBTESTCD='RBC', LB.LBNRIND='LOW')。Week 2 ではさらに平均赤血球容積 (MCV) が基準値上限を上回っている (LB.LBTESTCD='MCV', LB.LBNRIND='HIGH')。これは大球性貧血を示唆する可能性がある。高齢者やアルツハイマー病患者ではビタミンB12や葉酸欠乏による貧血も考慮されるが、スクリーニング時のVitB12, Folateは基準値内。治験薬との関連は不明だが、臨床的な評価が必要。
        *   **根拠:** LB.LBTESTCD = 'RBC', LB.LBDY = -13, LB.LBSTRESC = '3.8', LB.LBNRIND = 'LOW'; LB.LBTESTCD = 'RBC', LB.LBDY = 11, LB.LBSTRESC = '3.7', LB.LBNRIND = 'LOW'; LB.LBTESTCD = 'MCV', LB.LBDY = 11, LB.LBSTRESC = '101', LB.LBNRIND = 'HIGH'; LB.LBTESTCD = 'VITB12', LB.LBDY = -13, LB.LBNRIND = 'NORMAL'; LB.LBTESTCD = 'FOLATE' (データなし、プロトコル 3.4.2.2[28b]で評価項目)。一般的な医学的知見。
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Week 2 (Day 11) の尿検査で比重 (Specific Gravity) が基準値下限を下回っている (LB.LBTESTCD='SPGRAV', LB.LBNRIND='LOW')。尿濃縮力の低下を示唆する可能性があり、脱水や腎機能との関連を考慮する必要がある。ただし、同日のBUN, Creatinineは基準値内。
        *   **根拠:** LB.LBTESTCD = 'SPGRAV', LB.LBDY = 11, LB.LBSTRESC = '1.004', LB.LBNRIND = 'LOW'; LB.LBTESTCD = 'BUN', LB.LBDY = 11, LB.LBNRIND = 'NORMAL'; LB.LBTESTCD = 'CREAT', LB.LBDY = 11, LB.LBNRIND = 'NORMAL'。一般的な医学的知見。
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Week 2 (Day 11) のバイタルサイン測定において、臥位から立位への体位変換後に収縮期血圧が低下する傾向が見られる (Supine 125 mmHg -> Standing 1min 112 mmHg -> Standing 3min 110 mmHg)。起立性低血圧の可能性を考慮する必要がある。治験薬 (Xanomeline) はコリン作動薬であり、一般的に徐脈や血圧低下を引き起こす可能性があるため、関連を注視すべき。
        *   **根拠:** VS.VSTESTCD = 'SYSBP', VS.VSPOS = 'SUPINE', VS.VSDY = 11, VS.VSSTRESC = '125'; VS.VSTESTCD = 'SYSBP', VS.VSPOS = 'STANDING', VS.VSTPT = 'AFTER STANDING FOR 1 MINUTE', VS.VSDY = 11, VS.VSSTRESC = '112'; VS.VSTESTCD = 'SYSBP', VS.VSPOS = 'STANDING', VS.VSTPT = 'AFTER STANDING FOR 3 MINUTES', VS.VSDY = 11, VS.VSSTRESC = '110'。一般的な医学的知見 (コリン作動薬の副作用)。

*   **データ整合性観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** CMドメインにおいて、継続使用されている薬剤 (KEFLEX, LISINOPRIL, MOTRIN, PREMARIN, PROVERA, SYNTHROID) がVisitごとに別レコードとして記録されているように見える (CMSEQが異なる)。CMENDTC/CMENDYが多くのレコードで欠損しており、本来は開始日と終了日で1レコードとして表現されるべき。データ構造が不適切であり、正確な併用薬使用期間の把握が困難。
        *   **根拠:** CMドメインのデータ構造。CM.USUBJID = '01-701-1111' の複数レコード。SDTM IGのCMドメイン構造の原則。
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** AEドメインにおいて、治験薬投与中に発現し、治験中止理由と関連付けられている有害事象「ARTHRALGIA」(AESEQ=7) および「CELLULITIS」(AESEQ=8) の関連性評価 (AEREL) が "NONE" となっている。治験中止理由との整合性が取れておらず、データの信頼性に疑義がある。
        *   **根拠:** AE.AEREL = 'NONE' (for AESEQ=7, 8); DS.DSDECOD = 'ADVERSE EVENT'; RELREC (AE.AESEQ=7 と DS.DSSEQ=1 の関連)。
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、「ERYTHEMA」(AESEQ=1, 4) および「PRURITUS」(AESEQ=2, 5) が重複して記録されているように見える。開始日(AESTDTC)と終了日(AEENDTC)は同じだが、記録日(AEDTC)と転帰(AEOUT)が異なる。Visit 2 (Day -2) 時点の記録では未回復、Visit 4 (Day 11) 時点の記録では回復となっている。同一事象の追跡記録が別レコードになっている可能性、あるいは再発の可能性もあるが、記録方法が不明瞭。
        *   **根拠:** AE.AETERM = 'ERYTHEMA', AE.AESEQ = 1, 4; AE.AETERM = 'PRURITUS', AE.AESEQ = 2, 5。
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、多くの薬剤で標準化された薬剤名 (CMDECOD) および薬剤分類 (CMCLAS) が "UNCODED" となっている。データ解析のためには標準辞書 (例: WHODRUG) によるコーディングが必要。
        *   **根拠:** CM.CMDECOD = 'UNCODED', CM.CMCLAS = 'UNCODED' のレコード多数。
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、PREMARIN (CMSEQ=2, 8, 15, 21, 27, 33) および PROVERA (CMSEQ=3, 9, 16, 22, 28, 34) の用法 (CMDOSFRQ) が欠損している。
        *   **根拠:** CM.CMTRT = 'PREMARIN' or 'PROVERA', CM.CMDOSFRQ = (Missing)。
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、長期併用薬の Study Day (CMSTDY, CMENDY) が一部欠損している。CMSTDTC が年のみ (例: '2006', '1983') の場合に計算できていない。
        *   **根拠:** CM.CMSTDTC = '2006', CM.CMSTDY = null など。
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** RELRECドメインで、治験中止理由のAE (AESEQ=7, ARTHRALGIA) とDSレコード (DSSEQ=1) が RELID='01-701-1111-E16' で関連付けられている。しかし、AE.AESPID は 'E16' であり、RELID と一致しているように見えるが、AE.AESEQ=8 (CELLULITIS) も Day 7 に発現しており、中止との関連が不明確。RELREC の関連付けの正確性、および中止理由となったAEの特定が必要。
        *   **根拠:** RELREC.RELID = '01-701-1111-E16'; AE.AESPID = 'E16' (for AESEQ=7); AE.AESTDY = 7 (for AESEQ=7, 8); DS.DSSTDY = 11。

*   **プロトコル遵守観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[5] (CNS imaging compatible with AD within past 1 year) の確認記録がない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5]
        *   **根拠:** MHドメインや他のドメインにCNS imagingに関する記載が見当たらない。
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b] (Screening ECG findings) の確認記録がない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [16b]
        *   **根拠:** VSドメインや他のドメインにScreening ECGの結果に関する記載が見当たらない。
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[27b] (Laboratory test values exceeding reference range)。スクリーニング時のRBC低値が臨床的に有意でないと判断されたかどうかの記録がない。プロトコルでは逸脱が臨床的に有意でない場合、医師の判断を文書化する必要があると規定されている。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LB.LBTESTCD = 'RBC', LB.LBDY = -13, LB.LBNRIND = 'LOW'。医師の判断に関する記録がデータ上ない。
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[31b][v] (Estrogen supplements)。PREMARIN (結合型エストロゲン) を使用しているが、登録前3ヶ月間の用量安定性に関する確認記録がない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b][v]
        *   **根拠:** CM.CMTRT = 'PREMARIN', CM.CMSTDTC = '1996'。用量安定性に関する記録がデータ上ない。
    *   **指摘No.:** P-5
        *   **重要度:** Critical
        *   **逸脱の可能性:** 有害事象による早期治験中止 (Day 11)。プロトコルでは26週間の投与期間が計画されている。
        *   **プロトコル該当箇所:** Section 3.1 (Study Design), Section 3.10.1 (Discontinuations)
        *   **根拠:** DS.DSDECOD = 'ADVERSE EVENT', DS.DSSTDY = 11; EX.EXENDY = 10。

*   **有効性評価観点からの指摘事項:**
    *   **指摘No.:** E-1
        *   **重要度:** Major
        *   **内容:** 治験中止後のRetrieval Visit (Day 169) において、副次評価項目であるNPI-X Totalスコアがベースラインの2点、Week 2の1点から45点へと著しく悪化している。他の有効性評価項目 (ADAS-Cog, CIBIC+) の悪化と比較しても変動が大きい。この急激な悪化の理由（治験薬中止の影響、疾患の自然経過、他の要因）について考察が必要。
        *   **根拠:** QS.QSTESTCD = 'NPTOT', QS.QSDY = 1, QS.QSSTRESN = 2; QS.QSDY = 11, QS.QSSTRESN = 1; QS.QSDY = 169, QS.QSSTRESN = 45。QS.QSTESTCD = 'ACTOT', QS.QSDY = 1, QS.QSSTRESN = 7; QS.QSDY = 11, QS.QSSTRESN = 5; QS.QSDY = 169, QS.QSSTRESN = 9。QS.QSTESTCD = 'CIBIC', QS.QSDY = 11, QS.QSSTRESN = 4; QS.QSDY = 169, QS.QSSTRESN = 5。
    *   **指摘No.:** E-2
        *   **重要度:** Minor
        *   **内容:** DADスコアにおいて、ベースライン、Week 2、Retrieval間で一部項目の回答が Yes(1)/No(0) から Not Applicable(96) へ、あるいはその逆へと変化している (例: DAITM25, DAITM27, DAITM28, DAITM29, DAITM37, DAITM38, DAITM39)。NAの理由や評価の一貫性について確認が必要な場合がある。
        *   **根拠:** QS.QSCAT = 'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)' の各項目データ。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-2, D-7)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "有害事象「ARTHRALGIA」(AESEQ=7) および「CELLULITIS」(AESEQ=8) がDay 7に発現し、Day 11に有害事象を理由に治験が中止されています。しかし、AEドメインではこれらの事象の治験薬との関連性(AEREL)が「NONE」と記録されています。治験中止の判断根拠となった有害事象と治験薬との関連性について、再度評価・確認し、必要であれば修正してください。RELRECではAESEQ=7が中止理由と関連付けられていますが、中止の直接的な原因となった事象を特定し、コメントで補足してください。"
        *   **判断理由:** 治験中止理由となった有害事象の関連性評価は、安全性評価において重要であり、現在の記録には矛盾があるため。
        *   **判断根拠:**
            *   AE.AEREL = 'NONE' (for AESEQ=7, 8)
            *   DS.DSDECOD = 'ADVERSE EVENT', DS.DSSTDY = 11
            *   RELREC (AE.AESEQ=7 と DS.DSSEQ=1 の関連)
            *   プロトコル Section 3.9.3.2.1
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "プロトコル選択基準[5]では、登録前1年以内のアルツハイマー病と矛盾しないCNS画像所見が必要です。本症例の適格性確認において、CNS画像所見が確認された日付と結果（基準を満たすこと）をコメント等で追記してください。"
        *   **判断理由:** 選択基準の遵守を確認するために必要な情報がデータ上欠落しているため。
        *   **判断根拠:**
            *   データ上にCNS imagingに関する記録がない。
            *   プロトコル Section 3.4.2.1 [5]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **医療機関への問い合わせ文面:** "プロトコル除外基準[16b]では、スクリーニング時のECG所見に基づき除外が規定されています。本症例の適格性確認において、スクリーニングECGが実施され、除外基準に該当しないことが確認された日付と結果をコメント等で追記してください。"
        *   **判断理由:** 除外基準の遵守を確認するために必要な情報がデータ上欠落しているため。
        *   **判断根拠:**
            *   データ上にScreening ECGに関する記録がない。
            *   プロトコル Section 3.4.2.2 [16b]
    *   **クエリNo.:** Q-4 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **医療機関への問い合わせ文面:** "有害事象「ERYTHEMA」(AESEQ=1, 4) および「PRURITUS」(AESEQ=2, 5) が、異なる記録日(AEDTC)で報告されています (Visit 2時点とVisit 4時点)。Visit 4時点の記録 (AESEQ=4, 5) は、Visit 2時点の記録 (AESEQ=1, 2) の追跡情報（転帰の更新）でしょうか、あるいは事象の再発でしょうか。記録内容をご確認の上、必要であれば修正またはコメントで補足してください。"
        *   **判断理由:** 同一と思われる事象が複数レコードで報告されており、データの正確性と解釈を明確にするため。
        *   **判断根拠:**
            *   AE.AETERM = 'ERYTHEMA', AE.AESEQ = 1, 4
            *   AE.AETERM = 'PRURITUS', AE.AESEQ = 2, 5

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** CMドメインのデータ構造が不適切（継続薬がVisitごとに記録）。データマネジメント担当部署にて、データクリーニング方針に基づき修正、またはデータハンドリング規約を確認する。正確な併用期間の特定が必要な解析では注意が必要。
        *   **判断理由:** データ構造の問題であり、医療機関への問い合わせではなく内部での対応が必要。データ品質と解析への影響を考慮しMajorとした。
        *   **判断根拠:**
            *   CMドメインのデータ構造
            *   SDTM IG
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** CMドメインの多くの薬剤でCMDECOD, CMCLASが"UNCODED"。コーディング担当部署にてWHODRUG等を用いた標準コーディングを実施する。
        *   **判断理由:** 標準的なデータ処理プロセスの一部であり、内部での対応が必要。
        *   **判断根拠:**
            *   CM.CMDECOD = 'UNCODED', CM.CMCLAS = 'UNCODED' のレコード多数
    *   **確認事項No.:** I-3 (関連指摘No.: M-2, P-3)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** スクリーニング時のRBC低値について、除外基準[27b]に関連して臨床的に有意でないと判断されたか確認。データ上記録はないが、登録されていることから、治験責任医師により問題なしと判断された可能性が高い。記録として残す。Week 2でのMCV高値と合わせた貧血の可能性について、医学的レビュー担当者内で情報共有する。
        *   **判断理由:** 登録されている事実から大きな問題はないと推測されるが、基準値逸脱と医師の判断文書化の要件について記録に残す。
        *   **判断根拠:**
            *   LB.LBTESTCD = 'RBC', LB.LBDY = -13, LB.LBNRIND = 'LOW'
            *   プロトコル Section 3.4.2.2 [27b]
    *   **確認事項No.:** I-4 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** PREMARIN使用に関する除外基準[31b][v]（用量安定性）の確認記録がない。1996年から使用されており、安定している可能性が高いと推測される。記録として残す。
        *   **判断理由:** 長期使用薬であり問題ない可能性が高いが、確認記録がない点を記録。
        *   **判断根拠:**
            *   CM.CMTRT = 'PREMARIN', CM.CMSTDTC = '1996'
            *   プロトコル Section 3.4.2.2 [31b][v]
    *   **確認事項No.:** I-5 (関連指摘No.: E-1)
        *   **重要度:** Major
        *   **疑義事項/確認内容:** Retrieval Visit時のNPI-Xスコアの著明な悪化について、有効性評価チームおよびメディカルモニターで情報共有し、治験薬中止の影響や疾患進行との関連について考察する。
        *   **判断理由:** 有効性評価の解釈に影響を与える可能性のある重要な変化であり、内部での議論が必要。
        *   **判断根拠:**
            *   QS.QSTESTCD = 'NPTOT' のスコア推移
    *   **確認事項No.:** I-6 (関連指摘No.: D-5, D-6)
        *   **重要度:** Minor
        *   **疑義事項/確認内容:** CMドメインにおけるCMDOSFRQの欠損、CMSTDY/CMENDYの欠損について、データマネジメント担当部署で確認し、可能であれば修正する。
        *   **判断理由:** データ完全性のための内部確認事項。
        *   **判断根拠:**
            *   CMドメインの欠損値