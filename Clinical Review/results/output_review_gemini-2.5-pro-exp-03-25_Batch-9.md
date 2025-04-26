# 01-704-1009のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    83歳、男性、WHITE (NOT HISPANIC OR LATINO)。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2009年02月03日発症）、間欠性頭痛、季節性アレルギー、関節炎、心筋梗塞、前立腺肥大が報告されている。教育レベルは16年であった。

*   **イベント推移:**

|日付（YYYY-MM-DD）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013-08-20|Day -7 (SCREENING 1)|Screening実施。MMSE 21点、Hachinski Ischemic Score 0点。身長 179.07 cm、体重 64.86 kg。LB: ヘモグロビン 12.4 g/dL (LOW)、コレステロール 144 mg/dL (LOW)。他の主要な検査値は基準値内。|
|2013-08-24|Day -3 (SCREENING 2)|バイタルサイン測定。大きな変動なし。|
|2013-08-27|Day 1 (BASELINE)|治験薬Xanomeline Low Dose (54mg パッチ) 投与開始。体重 66.68 kg。ADAS-Cog(11) Total Score 22点。NPI-X Total Score 0点。DAD評価実施。|
|2013-09-05|Day 10 (N/A)|有害事象「倦怠感」(MILD) 発現 (治験薬との関連: POSSIBLE)。|
|2013-09-13|Day 18 (AMBUL ECG PLACEMENT)|バイタルサイン測定。立位3分後の拡張期血圧 86 mmHg。|
|2013-09-14|Day 19 (WEEK 2)|有害事象「発疹」(MILD) 発現 (治験薬との関連: POSSIBLE)。LB: ALT 39 U/L (HIGH、基準値上限の約1.1倍)、ヘモグロビン 11.1 g/dL (LOW)、ヘマトクリット 33.0 % (LOW)、赤血球数 3.70 MILL/uL (LOW)、リンパ球 0.72 THOU/uL (LOW)、塩化物 113 mEq/L (HIGH)、ナトリウム 146 mEq/L (HIGH)。他の主要な検査値は基準値内またはベースラインから大きな変動なし。NPI-X Total Score 0点。PK採血実施 (15:00)。|
|2013-09-17|Day 22 (N/A)|有害事象「めまい」(MILD) 発現 (治験薬との関連: REMOTE)。|
|2013-09-22|Day 27 (N/A)|有害事象「慢性腎臓病」(MILD, SERIOUS='Y') 発現 (治験薬との関連: POSSIBLE)。|
|2013-09-23|Day 28 (N/A)|有害事象「慢性腎臓病」回復。|
|2013-09-25|Day 30 (N/A)|治験薬投与終了。|
|2013-09-27|Day 32 (N/A)|有害事象「倦怠感」回復。|
|2013-10-02|Day 37 (WEEK 4)|有害事象「倦怠感」、「発疹」、「めまい」は未回復。ADAS-Cog(11) Total Score 26点 (Baselineから4点悪化)。CIBIC+ 4点 (No Change)。NPI-X Total Score 0点。DAD評価実施。被験者都合（時間的制約、ホルター拒否）により治験中止。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 既往歴として「心筋梗塞」が報告されている。プロトコル除外基準[17]では「5年以内の重篤な心血管障害」は除外対象である。心筋梗塞の発症時期が不明なため、適格性に疑義がある。83歳という年齢を考慮すると5年以上前の可能性もあるが、確認が必要。
        *   **根拠:** プロトコル除外基準[17]、MHデータ。参加者の安全性と適格性に関わる。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'MYOCARDIAL INFARCTION'
            *   [Age(DM.AGE)] = 83
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)の検査でALT値が基準値上限を超えて上昇している(39 U/L, 基準値上限35 U/L)。AST値も基準値上限付近(35 U/L, 基準値上限36 U/L)である。ベースライン(ALT 24, AST 27)からの上昇であり、治験薬投与開始後に発生している。肝障害を示唆する有害事象は報告されていないが、薬剤性肝障害の可能性を考慮する必要がある。プロトコル3.9.3.3項のモニタリング基準（>120 IUで週次再検、>400 IU等で即時再検/中止考慮）には達していないが、上昇傾向には注意が必要。
        *   **根拠:** LBデータ、一般的な医学知識（薬剤性肝障害）。参加者の安全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 39, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 35, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 35, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)の検査でヘモグロビン(HGB)、ヘマトクリット(HCT)、赤血球数(RBC)、リンパ球(LYM)が基準値下限を下回っている(LOW)。ベースラインと比較しても低下傾向が見られる。貧血や免疫系への影響の可能性があり、臨床的な評価が必要。関連する有害事象は報告されていない。
        *   **根拠:** LBデータ、一般的な医学知識（貧血、リンパ球減少）。参加者の安全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 6.88866, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 7.76, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HCT', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.33, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 0.37, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.7, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'LYM', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.72, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 0.8, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)の検査で塩化物(CL)とナトリウム(SODIUM)が基準値上限を超えている(HIGH)。脱水や腎機能障害との関連を考慮する必要がある。同日のBUN, CREATは基準値内だが、ベースラインからやや上昇傾向。関連する有害事象は報告されていない（ただし、Day 27に「慢性腎臓病」AEが報告されている）。
        *   **根拠:** LBデータ、一般的な医学知識（電解質異常）。参加者の安全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CL', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 113, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 112, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 146, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** 有効性評価において、主要評価項目の一つであるADAS-Cog(11) Total ScoreがBaselineの22点からWeek 4で26点へと悪化している。一方で、もう一つの主要評価項目であるCIBIC+はWeek 4で「変化なし(4点)」、副次評価項目のNPI-X Total Scoreは一貫して0点、DADスコアも大きな変化は見られない。ADAS-Cogの悪化と他の評価指標との間に乖離が見られ、治験薬の有効性評価の解釈に影響を与える可能性がある。認知機能のみが悪化し、全般的印象や日常生活動作、精神症状に変化がない理由について考察が必要。
        *   **根拠:** QSデータ、試験の目的（有効性評価）。評価の信頼性に関わる。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 22
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 26
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 4
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 4, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0
            *   QS DADデータ (DAITM01-DAITM40)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「慢性腎臓病」が重篤(AESER='Y')と報告されているが、開始日(Day 27)から終了日(Day 28)までが1日であり、転帰が「回復」となっている。重篤な慢性腎臓病が1日で回復することは通常考えにくく、事象名、重篤度評価、期間、転帰の間に矛盾がある可能性が高い。入院等の記録もなく、重篤性の判断根拠が不明。参加者の安全性評価に重大な影響を与えうる。
        *   **根拠:** AEデータ、一般的な医学知識。データの信頼性、安全性評価の妥当性に関わる。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 6
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'CHRONIC KIDNEY DISEASE'
            *   [Serious Event(AE.AESER)] = 'Y'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-09-22'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-09-23'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Requires or Prolongs Hospitalization(AE.AESHOSP)] = 'N'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 有害事象「倦怠感」について、同じ開始日(Day 10)で2つのレコード(AESEQ=2, 4)が存在する。AESEQ=2では終了日・転帰が未記載(NOT RECOVERED/NOT RESOLVED)、AESEQ=4では終了日(Day 32)があり転帰が「回復」となっている。重複入力または修正漏れの可能性があり、データの正確性に問題がある。
        *   **根拠:** AEデータ。データ品質に関わる。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 2, [Reported Term for the Adverse Event(AE.AETERM)] = 'MALAISE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-09-05', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-09-27', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Sequence Number(AE.AESEQ)] = 4, [Reported Term for the Adverse Event(AE.AETERM)] = 'MALAISE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-09-05', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-09-27', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** MH「心筋梗塞」の開始日(MHSTDTC)が欠損している。除外基準[17]（5年以内の重篤な心血管障害）の評価に影響する。
        *   **根拠:** MHデータ、プロトコル除外基準[17]。適格性評価の信頼性に関わる。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'MYOCARDIAL INFARCTION', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)にALT値の上昇が認められたが、関連する肝機能障害等の有害事象が報告されていない。未報告AEの可能性。
        *   **根拠:** LBデータ、AEデータ。安全性評価の完全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 39, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   AEドメインに肝関連事象なし
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)にHGB, HCT, RBC, LYMの低値が認められたが、関連する貧血、白血球減少等の有害事象が報告されていない。未報告AEの可能性。
        *   **根拠:** LBデータ、AEデータ。安全性評価の完全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HCT', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'LYM', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   AEドメインに関連事象なし
    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 19)にCl, Naの高値が認められたが、関連する電解質異常、脱水等の有害事象が報告されていない。未報告AEの可能性。
        *   **根拠:** LBデータ、AEデータ。安全性評価の完全性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CL', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Visit Number(LB.VISITNUM)] = 4, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   AEドメインに関連事象なし
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、一部薬剤の開始日(CMSTDTC)や終了日(CMENDTC)が年のみ、または年月のみで記録されており、精度が低い。曝露期間の正確な評価に影響する可能性があるが、限定的。
        *   **根拠:** CMデータ。データ品質に関わる。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'BENADRYL', [Start Date/Time of Medication(CM.CMSTDTC)] = '2009', [End Date/Time of Medication(CM.CMENDTC)] = '2013-08'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'BUFFERIN', [Start Date/Time of Medication(CM.CMSTDTC)] = '2009'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'VITAMIN E', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-04'
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** QSドメインのDAD評価において、BaselineでNA(Not Applicable)と回答された項目がWeek 4でY(Yes)となっている箇所がある(DAITM26, 29, 35)。また、BaselineでYだった項目がWeek 4でNAとなっている箇所もある(DAITM37, 38, 39)。NAの定義（以前からやっていない、または機会がなかった）を考慮すると、Baselineでの記録誤りか、あるいは活動状況の変化を示唆する可能性がある。データ解釈に注意が必要だが、全体評価への影響は限定的か。
        *   **根拠:** QSデータ。データ品質、有効性評価の解釈に関わる。
        *   **関連データ:**
            *   QS DADデータ (DAITM18, 19, 20, 26, 29, 31, 32, 35, 37, 38, 39)
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、心筋梗塞以外の既往歴についても開始日(MHSTDTC)が欠損しているものが多い。適格性評価への影響は限定的と思われるが、データ完全性の観点からは問題。
        *   **根拠:** MHデータ。データ品質に関わる。
        *   **関連データ:**
            *   MHドメインのMHSTDTCが空のレコード
    *   **指摘No.:** D-10
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、MedDRAコーディング関連変数（AELLT, AELLTCD, AEDECOD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCD）が欠損している。コーディング未完了の可能性。
        *   **根拠:** AEデータ。データ完全性に関わる。
        *   **関連データ:**
            *   AEドメインの上記変数が空のレコード
    *   **指摘No.:** D-11
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、一部薬剤の標準化薬剤名(CMDECOD)や薬剤分類(CMCLAS)が'UNCODED'となっている。薬剤相互作用等の評価に影響する可能性があるが、薬剤名(CMTRT)から判断可能。
        *   **根拠:** CMデータ。データ完全性に関わる。
        *   **関連データ:**
            *   CMドメインのCMDECOD, CMCLASが'UNCODED'のレコード

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[17]「5年以内の重篤な心血管障害」に抵触している可能性がある。既往歴に「心筋梗塞」があるが発症日が不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** MHデータ。適格性、参加者の安全性に関わる。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'MYOCARDIAL INFARCTION', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** Visitスケジュールからの逸脱。Week 2 (Visit 4) および Week 4 (Visit 5) の実施日が、プロトコルで規定されたVisit Window（それぞれ±3日）から外れている (Day 19, Day 37)。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit Window規定)
        *   **根拠:** SVデータ、TVデータ。データ信頼性、プロトコル遵守に関わる。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 4, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-09-14' (Day 19), [Planned Study Day of Visit(TV.VISITDY)] = 14
            *   [Visit Number(SV.VISITNUM)] = 5, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-10-02' (Day 37), [Planned Study Day of Visit(TV.VISITDY)] = 28
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 評価スケジュールの逸脱または欠損。
            *   CIBIC+のBaseline評価が欠損している。
            *   ADAS-Cog, CIBIC+, DADがプロトコル規定外のVisit 5 (Week 4)で実施されている（中止に伴う評価の可能性はある）。
            *   PK採血がプロトコル規定のVisit 3で実施されていない。Visit 4での採血時間帯が不明確。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Section 3.9.2 Pharmacokinetics
        *   **根拠:** QSデータ、LBデータ。データ信頼性、評価計画の遵守に関わる。
        *   **関連データ:**
            *   QSドメインで [Visit Number(QS.VISITNUM)] = 3 かつ [Question Short Name(QS.QSTESTCD)] = 'CIBIC' のレコードなし
            *   QSドメインで [Visit Number(QS.VISITNUM)] = 5 のADAS-Cog, CIBIC+, DADレコード
            *   LBドメインで [Visit Number(LB.VISITNUM)] = 3 のPK関連レコードなし
            *   [Visit Number(LB.VISITNUM)] = 4, [Date/Time of Specimen Collection(LB.LBDTC)] = '2013-09-14T15:00'
    *   **指摘No.:** P-4
        *   **重要度:** Critical
        *   **逸脱の可能性:** 同意取得日(RFICDTC)が記録されていない。治験手順開始前に同意が取得されているか確認できない。GCP違反の可能性。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** DMデータ。参加者の権利保護に関わる。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用制限薬であるBENADRYL (Diphenhydramine) の服用状況が不明確。除外基準[31b] r では投与開始3日前までに中止が必要だが、記録されている開始日('2009')と終了日('2013-08')では、組み入れ時(Day 1, 2013-08-27)に規定通り中止されていたか判断できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] r
        *   **根拠:** CMデータ。適格性、安全性、有効性評価への影響の可能性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'BENADRYL', [Start Date/Time of Medication(CM.CMSTDTC)] = '2009', [End Date/Time of Medication(CM.CMENDTC)] = '2013-08'
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** Screening時(Day -7)に除外基準[27b]に該当しうる検査値異常（HGB低値、Cholesterol低値）が認められた。プロトコルでは臨床的に意義がないと判断されれば組み入れ可能とされているが、その判断記録がデータ上確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LBデータ。適格性評価プロセスの確認。
        *   **関連データ:**
            *   [Visit Number(LB.VISITNUM)] = 1, [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   [Visit Number(LB.VISITNUM)] = 1, [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CHOL', [Reference Range Indicator(LB.LBNRIND)] = 'LOW'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-4)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、同意取得日の記録がありません。治験手順開始前に適切に同意が取得されていたか確認し、同意取得日をお知らせください。これは参加者の権利保護に関する重要な確認事項です。
        *   **クエリ文面（英語）:** For subject 1009, the Date/Time of Informed Consent is missing. Please confirm that informed consent was obtained prior to any study procedures and provide the date of consent. This is critical for participant rights protection.
        *   **判断理由:** 同意取得の確認はGCP遵守および参加者の権利保護の観点から必須であるため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(DM.USUBJID)] = '01-704-1009', [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号「1009」の有害事象「慢性腎臓病」(AESEQ=6)について、重篤と報告されていますが、発現から1日で回復となっています。事象名、重篤度評価、期間、転帰に矛盾がある可能性があります。重篤と判断された根拠（入院、生命を脅かす等）および実際の臨床経過について詳細を確認し、必要であれば記録を修正してください。参加者の安全性評価の正確性のために重要です。
        *   **クエリ文面（英語）:** For subject 1009, AE 'CHRONIC KIDNEY DISEASE' (AESEQ=6) is reported as Serious (Y) but resolved in 1 day (AESTDTC=2013-09-22, AEENDTC=2013-09-23). Please clarify the basis for the seriousness assessment (e.g., hospitalization) and the clinical course, and correct the record if necessary. This is critical for accurate safety assessment.
        *   **判断理由:** 重篤有害事象の報告内容に矛盾があり、安全性評価の正確性を担保するために確認が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(AE.USUBJID)] = '01-704-1009', [Sequence Number(AE.AESEQ)] = 6, [Reported Term for the Adverse Event(AE.AETERM)] = 'CHRONIC KIDNEY DISEASE', [Serious Event(AE.AESER)] = 'Y', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-09-22', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-09-23', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
    *   **クエリNo.:** Q-3 (関連指摘No.: M-1, D-3, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号「1009」の既往歴「心筋梗塞」について、発症日の記録がありません。プロトコル除外基準（5年以内の重篤な心血管障害）への抵触を確認するため、心筋梗塞の発症年月をお知らせください。参加者の適格性と安全性確保のために必要です。
        *   **クエリ文面（英語）:** For subject 1009, the onset date for Medical History 'MYOCARDIAL INFARCTION' is missing. To confirm eligibility regarding exclusion criterion 17 (serious cardiovascular disorder within 5 years), please provide the onset date (year/month). This is needed for eligibility and safety assurance.
        *   **判断理由:** 除外基準への抵触を確認し、参加者の適格性と安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(MH.USUBJID)] = '01-704-1009', [Reported Term for the Medical History(MH.MHTERM)] = 'MYOCARDIAL INFARCTION', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17]
    *   **クエリNo.:** Q-4 (関連指摘No.: M-2, D-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、Week 2 (Study Day 19) の検査でアラニンアミノトランスフェラーゼが「39 U/L」と基準値上限を超えています。関連する有害事象は報告されていませんが、この検査値異常の臨床的な意義について評価をお願いします。薬剤性肝障害の可能性も考慮し、追跡検査の必要性等についてもご判断ください。
        *   **クエリ文面（英語）:** For subject 1009, ALT was 39 U/L (above upper limit) on Week 2 (Day 19). No related AE was reported. Please assess the clinical significance of this finding, considering potential drug-induced liver injury and the need for follow-up tests.
        *   **判断理由:** 潜在的な肝機能障害のリスクを評価し、適切な対応（追跡検査、AE報告等）を促すため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(LB.USUBJID)] = '01-704-1009', [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Visit Number(LB.VISITNUM)] = 4, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 39, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   関連するプロトコル箇所: Section 3.9.3.3 Clinical Laboratory Tests
            *   関連する医学的知見: 薬剤性肝障害の可能性
    *   **クエリNo.:** Q-5 (関連指摘No.: M-3, D-5)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、Week 2 (Study Day 19) の検査でヘモグロビン、ヘマトクリット、赤血球数、リンパ球が基準値下限を下回っています。関連する有害事象は報告されていませんが、これらの検査値異常の臨床的な意義（貧血、免疫抑制等）について評価をお願いします。
        *   **クエリ文面（英語）:** For subject 1009, HGB, HCT, RBC, and LYM were below lower limits on Week 2 (Day 19). No related AEs were reported. Please assess the clinical significance of these findings (e.g., anemia, immunosuppression).
        *   **判断理由:** 潜在的な血液学的異常のリスクを評価し、適切な対応を促すため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(LB.USUBJID)] = '01-704-1009', [Visit Number(LB.VISITNUM)] = 4, LBレコード (HGB, HCT, RBC, LYM) で [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
            *   関連する医学的知見: 貧血、リンパ球減少
    *   **クエリNo.:** Q-6 (関連指摘No.: M-4, D-6)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、Week 2 (Study Day 19) の検査で塩化物とナトリウムが基準値上限を超えています。関連する有害事象は報告されていませんが、これらの電解質異常の臨床的な意義（脱水、腎機能等）について評価をお願いします。
        *   **クエリ文面（英語）:** For subject 1009, Chloride and Sodium were above upper limits on Week 2 (Day 19). No related AEs were reported. Please assess the clinical significance of these electrolyte abnormalities (e.g., dehydration, renal function).
        *   **判断理由:** 潜在的な電解質異常のリスクと原因を評価し、適切な対応を促すため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(LB.USUBJID)] = '01-704-1009', [Visit Number(LB.VISITNUM)] = 4, LBレコード (CL, SODIUM) で [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   関連する医学的知見: 電解質異常、脱水、腎機能
    *   **クエリNo.:** Q-7 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号「1009」の併用薬「BENADRYL」について、記録されている終了年月が「2013-08」です。プロトコルでは投与開始3日前までに中止が必要ですが、治験薬開始日(2013-08-27)の3日前までに確実に中止されていたか確認し、正確な中止日をお知らせください。
        *   **クエリ文面（英語）:** For subject 1009, the recorded end date for concomitant medication 'BENADRYL' is '2013-08'. The protocol requires discontinuation 3 days prior to study drug initiation (2013-08-27). Please confirm the exact stop date to ensure compliance.
        *   **判断理由:** 除外基準[31b]rの遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(CM.USUBJID)] = '01-704-1009', [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'BENADRYL', [End Date/Time of Medication(CM.CMENDTC)] = '2013-08', [Date/Time of First Study Treatment(DM.RFXSTDTC)] = '2013-08-27'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] r
    *   **クエリNo.:** Q-8 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 患者番号「1009」の有害事象「倦怠感」について、同じ開始日で2つのレコード(AESEQ=2, 4)が記録されており、転帰が異なります。重複入力または修正漏れの可能性がありますので、正しい情報をご確認の上、不要なレコードを削除または修正してください。
        *   **クエリ文面（英語）:** For subject 1009, AE 'MALAISE' has two records (AESEQ=2, 4) with the same start date but different outcomes. Please review, correct the information, and delete the duplicate/incorrect record if necessary.
        *   **判断理由:** データの一貫性と正確性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Unique Subject Identifier(AE.USUBJID)] = '01-704-1009', [Sequence Number(AE.AESEQ)] = 2 and 4, [Reported Term for the Adverse Event(AE.AETERM)] = 'MALAISE'
    *   **クエリNo.:** Q-9 (関連指摘No.: P-2, P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、Visit 4 (Week 2) および Visit 5 (Week 4) の実施日が規定のVisit Windowから逸脱しています。また、BaselineでのCIBIC+評価が欠損しており、Visit 5で予定外の有効性評価が実施されています。これらの逸脱および欠損/追加評価の理由をお知らせください。
        *   **クエリ文面（英語）:** For subject 1009, Visit 4 (Week 2) and Visit 5 (Week 4) occurred outside the protocol-defined window. Baseline CIBIC+ is missing, and unscheduled efficacy assessments were done at Visit 5. Please provide reasons for these deviations/missing/extra assessments.
        *   **判断理由:** プロトコル逸脱の理由を確認し、データの信頼性への影響を評価するため。
        *   **判断根拠:**
            *   関連するデータ: SV, QSデータ
            *   関連するプロトコル箇所: Section 3.1, 3.9.1.1
    *   **クエリNo.:** Q-10 (関連指摘No.: P-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号「1009」について、Screening時の検査でヘモグロビンとコレステロールが基準値下限を下回っていました。プロトコルでは臨床的に意義がないと判断されれば組み入れ可能ですが、その判断を行った記録（例：医師のコメント）についてご確認ください。
        *   **クエリ文面（英語）:** For subject 1009, screening labs showed low Hemoglobin and Cholesterol. The protocol allows enrollment if deemed not clinically significant. Please confirm documentation of the investigator's clinical significance assessment.
        *   **判断理由:** 適格性評価プロセスの確認のため。
        *   **判断根拠:**
            *   関連するデータ: LBデータ (Visit 1)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor/DM
        *   **疑義事項/確認内容:** 有効性評価においてADAS-Cog(11)が悪化している一方で、CIBIC+やNPI-X, DADでは変化が見られない。この乖離について、患者の状態（例：AEの影響、協力度）や評価の状況（例：評価者間のばらつき）等、考えられる要因を内部で考察し、記録する。中止前の最終評価であるため、解釈には注意が必要。
        *   **判断理由:** 有効性評価結果の解釈に影響する可能性のある所見だが、医療機関への問い合わせで追加情報が得られる可能性は低いと判断したため。内部での医学的・統計的評価が必要。
        *   **判断根拠:**
            *   関連するデータ: QSデータ (ADAS-Cog, CIBIC+, NPI-X, DAD)
    *   **確認事項No.:** I-2 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMデータの一部で開始日・終了日の精度が低い（年のみ、年月のみ）。データ入力規則の遵守状況を確認し、必要であればデータクリーニングプロセスで対応を検討する。本症例の評価への直接的な影響は小さいと判断。
        *   **判断理由:** データ品質の問題だが、主要な評価への影響は限定的であり、内部でのデータ管理プロセスで対応可能と判断したため。
        *   **判断根拠:**
            *   関連するデータ: CMデータ
    *   **確認事項No.:** I-3 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QS DAD評価におけるNA回答の変動について記録する。データ入力時の誤りか、実際の活動状況の変化か不明だが、全体スコアへの影響は限定的と考えられる。同様のパターンが他の症例でも見られるか確認する。
        *   **判断理由:** データ解釈上の注意点だが、クエリ発行による明確化は困難であり、評価への影響も小さいと判断したため。
        *   **判断根拠:**
            *   関連するデータ: QS DADデータ
    *   **確認事項No.:** I-4 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHデータの開始日欠損が多い点について記録する。心筋梗塞以外は適格性への影響は小さいが、データ完全性の観点から問題。データ収集・入力プロセスを確認する。
        *   **判断理由:** データ完全性の問題だが、本症例の主要な評価への影響は限定的であり、内部でのプロセス確認事項としたため。
        *   **判断根拠:**
            *   関連するデータ: MHデータ
    *   **確認事項No.:** I-5 (関連指摘No.: D-10, D-11)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEおよびCMドメインのコーディング未完了/欠損について記録する。データクリーニングおよびコーディングプロセスで対応が必要。最終的な安全性集計・評価に影響するため、完了をモニターする。
        *   **判断理由:** データ完全性の問題であり、最終的な集計・評価には重要だが、現時点での個別症例レビューとしては内部確認事項としたため。
        *   **判断根拠:**
            *   関連するデータ: AE, CMデータ

---

# 01-704-1010のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
80歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2006年発症、Primary Diagnosis）、高血圧症（軽度、Significant Pre-existing Condition）、膝蓋骨骨折（1994年）、鼠径ヘルニア（複数回、1957年～1986年）が報告されている。教育歴は14年。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2014年02月07日|Day -14 (SCREENING 1)|スクリーニング検査実施。主要な検査値は基準値内（Bilirubin 1.1 mg/dL, Calcium 9.0 mg/dL, Creatinine 1.3 mg/dL, Sodium 144 mEq/L, Potassium 4.5 mEq/L, ALT 9 U/L, AST 16 U/L, WBC 6.59 THOU/uL, HGB 16.8 g/dL, HCT 51.0%, Platelet 191 THOU/uL）。TSH, Vit B12も正常範囲内。|
|2014年02月08日|Day -13 (SCREENING 1)|身長 177.8 cm, 体重 81.65 kg。血圧は高値傾向（臥位 168/90 mmHg, 立位1分後 152/88 mmHg, 立位3分後 168/92 mmHg）。脈拍は正常範囲内。MMSEスコア 17点、Modified Hachinski Ischemic Score 1点。|
|2014年02月19日|Day -2 (SCREENING 2)|バイタルサイン測定。血圧は高値傾向（臥位 158/86 mmHg, 立位1分後 152/84 mmHg, 立位3分後 158/84 mmHg）。|
|2014年02月21日|Day 1 (BASELINE)|治験薬（Placebo）投与開始。ベースラインバイタルサイン測定。体重 80.97 kg。血圧は高値傾向（臥位 162/92 mmHg, 立位1分後 170/92 mmHg, 立位3分後 168/90 mmHg）。ベースライン有効性評価実施（ADAS-Cog(11)スコア 26点、NPI-X合計スコア 6点、DAD合計スコア 83.9%）。|
|2014年02月27日|Day 7 (N/A)|有害事象「DIABETES MELLITUS」（軽度、重篤）発現。併用薬「CIPRO」開始。|
|2014年03月06日|Day 14 (N/A)|有害事象「DIABETES MELLITUS」回復/解消。併用薬「CIPRO」終了。|
|2014年03月08日|Day 16 (WEEK 2)|検査値測定（主要項目は基準値内）。バイタルサイン測定（立位血圧高値傾向 160/92 mmHg）。NPI-X評価（合計スコア 3点）。|
|2014年03月23日|Day 31 (WEEK 4)|検査値測定（主要項目は基準値内）。バイタルサイン測定（血圧はやや高値傾向）。NPI-X評価（合計スコア 2点）。|
|2014年04月11日|Day 50 (WEEK 6)|検査値測定（Bilirubin 1.3 mg/dL [高値]）。バイタルサイン測定（血圧は高値傾向）。NPI-X評価（合計スコア 3点）。|
|2014年04月24日|Day 63 (WEEK 8)|検査値測定（主要項目は基準値内）。バイタルサイン測定（血圧は高値傾向）。有効性評価実施（ADAS-Cog(11)スコア 23点、CIBIC+スコア 4 [変化なし]、DAD合計スコア 77.4%、NPI-X合計スコア 5点）。|
|2014年04月25日|Day 64 (N/A)|併用薬「NORVASC」（Amlodipine）5mg QD 開始（高血圧治療目的と推察）。|
|2014年05月08日|Day 77 (WEEK 10 (T))|NPI-X評価（合計スコア 3点）。|
|2014年05月16日|Day 85 (WEEK 12)|バイタルサイン測定（血圧は以前より低下傾向）。NPI-X評価（合計スコア 1点）。|
|2014年05月30日|Day 99 (UNSCHEDULED 9.2)|予定外検査値測定（Bilirubin 1.3 mg/dL [高値]）。NPI-X評価（合計スコア 2点）。|
|2014年06月13日|Day 113 (WEEK 16)|検査値測定（主要項目は基準値内）。バイタルサイン測定（血圧は低下傾向）。有効性評価実施（ADAS-Cog(11)スコア 30点、CIBIC+スコア 3 [軽度改善]、DAD合計スコア 80.6%、NPI-X合計スコア 1点）。|
|2014年06月27日|Day 127 (WEEK 18 (T))|NPI-X評価（合計スコア 0点）。|
|2014年07月05日|Day 135 (N/A)|有害事象「DIARRHOEA」（軽度）、「VOMITING」（軽度）発現。併用薬「IMODIUM A-D」、「TUMS」開始。|
|2014年07月06日|Day 136 (N/A)|有害事象「ARTHRALGIA」（軽度）、「CONTUSION」（軽度）、「EXCORIATION」（軽度）、「SKIN LACERATION」（軽度）発現。有害事象「DIARRHOEA」、「VOMITING」回復/解消。併用薬「IMODIUM A-D」、「TUMS」終了。|
|2014年07月08日|Day 138 (N/A)|治験薬（Placebo）投与終了。|
|2014年07月09日|Day 139 (WEEK 20)|治験中止（理由：患者転居）。最終検査値測定（Bilirubin 1.3 mg/dL [高値]、Calcium 8.3 mg/dL [低値]、Creatinine 1.5 mg/dL [正常]）。最終バイタルサイン測定（体重 79.38 kg）。最終有効性評価実施（ADAS-Cog(11)スコア 30点、CIBIC+スコア 3 [軽度改善]、DAD合計スコア 90.3%、NPI-X合計スコア 1点）。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象「DIABETES MELLITUS」(AESEQ=1) が重篤 (Serious=Y) と報告されているが、重症度は軽度 (Mild) であり、血糖値データや併用薬からは重篤と判断する根拠が見当たらない。重篤性の評価基準が不明であり、安全性評価の妥当性に疑義がある。
        *   **根拠:** 重篤な有害事象の定義（入院、生命を脅かす等）に合致するか不明。血糖値は期間中正常範囲内。インスリン等の関連治療薬投与なし。MHに糖尿病既往なし。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIABETES MELLITUS'
            *   [Sequence Number(AE.AESEQ)] = 1
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Serious Event(AE.AESER)] = 'Y'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2014-02-27'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2014-03-06'
            *   LB (GLUC) データ
            *   CM データ
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Study Day 136に複数の有害事象（関節痛、打撲、表皮剥離、皮膚裂傷）が集中して発現している。同日に下痢・嘔吐は回復している。これらの事象は転倒など、報告されていない先行イベントを示唆する可能性がある。発生状況と原因について確認が必要であり、参加者の安全確保の観点から重要である。
        *   **根拠:** 同日に複数の外傷関連と思われるAEが報告されていることは、単一の原因（例：転倒）による可能性が高い。未報告のイベントがあれば、安全性評価に影響する。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', 'CONTUSION', 'EXCORIATION', 'SKIN LACERATION'
            *   [Sequence Number(AE.AESEQ)] = 6, 7, 4, 5
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2014-07-06'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** 軽度のビリルビン高値が複数回（Day 50, 99, 139）認められる。他の肝機能検査値は正常であり、Placebo群であることから臨床的意義は低い可能性が高いが、持続的な変動として記録する。
        *   **根拠:** 基準値上限 (1.2 mg/dL or 21 umol/L) をわずかに超える程度 (1.3 mg/dL or 22.23 umol/L)。ALT, AST, ALP, GGTは正常。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BILI'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 22.23 (Day 50, 99, 139)
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 21
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** 最終評価時 (Day 139) に軽度のカルシウム低値 (8.3 mg/dL) が認められる。基準値下限 (8.4 mg/dL or 2.1 mmol/L) をわずかに下回る程度であり、臨床的意義は低い可能性が高い。
        *   **根拠:** 基準値からの逸脱が軽微。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CA'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 2.07085 (Day 139)
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 2.1
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 試験期間中に約1.6kgの体重減少（Baseline 80.97 kg -> Day 139 79.38 kg）が認められる。高齢者であり注意は必要だが、減少幅は大きくなく、関連するAE報告もないため、臨床的意義は低いと判断される。
        *   **根拠:** 体重変化率 約2%。食欲不振等のAE報告なし。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'WEIGHT'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 80.97 (Day 1), 79.38 (Day 139)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「DIABETES MELLITUS」(AESEQ=1) の重篤度 (Serious=Y) が、他のデータ（Severity=Mild, 血糖値正常, 関連薬なし）と整合していない。データの正確性に疑義があり、安全性評価に影響する可能性がある。
        *   **根拠:** 医学的レビュー(M-1)で指摘した通り、重篤と判断する臨床的根拠がデータ上見当たらない。
        *   **関連データ:**
            *   AEドメイン (AESEQ=1)
            *   LBドメイン (LBTESTCD='GLUC')
            *   CMドメイン
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。Define.xmlには「Date of informed consent was not entered in database」とコメントがあるが、同意取得は治験手順開始前に必須であり、その日付が記録されていないことはデータの完全性の問題であり、GCP遵守の観点からも重要である。
        *   **根拠:** GCP要件。治験手順開始日（Screening Visit: 2014-02-08）より前に同意が取得されたことを確認する必要がある。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-02-08' (Visit 1)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 既往歴「HYPERTENSION」の開始日 (MH.MHSTDTC) が欠損している。既往歴の詳細な開始日は必須ではない場合が多く、評価への影響は小さいと考えられる。
        *   **根拠:** 既往歴情報であり、発症時期が不明なことは臨床現場でも起こりうる。他のデータ（VS, CM）から高血圧の存在は裏付けられている。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0342' (Hypertension)
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = (欠損)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が記録されておらず、治験手順開始前に適切に同意が取得されたか確認できない。GCP違反の可能性がある。
        *   **プロトコル該当箇所:** 5.1 Informed Consent
        *   **根拠:** GCPでは、治験関連手順開始前に被験者から自由意思による同意を文書で得ることが必須とされている。同意日の記録欠損により、この遵守状況を確認できない。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-02-08' (Visit 1)
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験中止時の治験薬漸減手順（プロトコル 3.10.1）が実施されなかった可能性がある。EXデータでは中止前日まで通常投与が継続されている。
        *   **プロトコル該当箇所:** 3.10.1 Discontinuations
        *   **根拠:** プロトコルでは中止時に用量漸減（25cm2パッチ除去後、50cm2パッチを中止Visitまで継続）が指示されているが、EXデータ上はそのような漸減期間が見られない。ただしPlacebo群であるため安全性への影響は小さい。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2014-07-08'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2014-07-09'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「DIABETES MELLITUS」（AESEQ=1、開始日2014-02-27）について、「重篤なイベント」が「Y」と報告されていますが、重症度は「軽度」であり、関連する検査値異常や治療介入も記録されていません。重篤と判断された具体的な理由（例：入院、生命を脅かす等）について詳細をご教示ください。安全性評価の正確性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding AE 'DIABETES MELLITUS' (AESEQ=1, Start Date 2014-02-27), 'Serious Event' is reported as 'Y', but 'Severity/Intensity' is 'MILD' and no related lab abnormalities or interventions are recorded. Please provide details on the reason for classifying this event as serious (e.g., hospitalization, life-threatening).
        *   **判断理由:** 重篤性の評価が他の臨床データと矛盾しており、安全性評価の妥当性を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1), LB (GLUC), CM
            *   関連するプロトコル箇所: 3.9.3.2.2 Serious Adverse Events
            *   関連する医学的知見: 重篤な有害事象の定義
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor / CRA
        *   **医療機関への問い合わせ文面:** Study Day 136（2014-07-06）に、「関節痛」、「打撲」、「表皮剥離」、「皮膚裂傷」が同時に報告されています。これらの有害事象の発生経緯について詳細をご教示ください。特に、転倒などの先行するイベントがなかったかご確認ください。参加者の安全確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** On Study Day 136 (2014-07-06), multiple AEs ('ARTHRALGIA', 'CONTUSION', 'EXCORIATION', 'SKIN LACERATION') were reported concurrently. Please provide details on the circumstances leading to these events. Specifically, please confirm if a preceding event, such as a fall, occurred.
        *   **判断理由:** 未報告のイベント（例：転倒）の可能性があり、参加者の安全性評価に影響するため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=4, 5, 6, 7)
            *   関連するプロトコル箇所: 3.9.3.2 Adverse Event Reporting Requirements
            *   関連する医学的知見: 高齢者の転倒リスク、複数外傷の同時発生
    *   **クエリNo.:** Q-3 (関連指摘No.: D-3, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 「インフォームド・コンセントの日付/時刻」(DM.RFICDTC) が記録されていません。治験実施計画書およびGCPに従い、治験関連手順開始前に同意が取得されている必要があります。同意取得日をご確認の上、ご報告ください。参加者の権利保護の観点から、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** The 'Date/Time of Informed Consent' (DM.RFICDTC) is missing. Please confirm and provide the date when informed consent was obtained, ensuring it was prior to the initiation of any study procedures as required by the protocol and GCP.
        *   **判断理由:** 同意取得日の確認はGCP遵守および参加者の権利保護の観点から必須であるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC (欠損), SV.SVSTDTC (Visit 1)
            *   関連するプロトコル箇所: 5.1 Informed Consent
            *   関連する医学的知見: GCP原則

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 軽度のビリルビン高値が複数回観察された。Placebo群であり、他の肝機能検査は正常範囲内のため、現時点での臨床的意義は低いと判断。傾向として内部で記録し、今後のデータで同様の傾向が見られるか注視する。
        *   **判断理由:** Placebo群であり、上昇の程度も軽微なため、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB (Bilirubin, ALT, AST, ALP, GGT)
    *   **確認事項No.:** I-2 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 最終評価時に軽度のカルシウム低値が観察された。逸脱の程度は軽微であり、臨床的意義は低いと判断。内部記録のみとする。
        *   **判断理由:** 逸脱が軽微であり、単発の所見である可能性が高いため、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB (Calcium)
    *   **確認事項No.:** I-3 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 試験期間中に軽度の体重減少が観察された。減少幅は大きくなく、関連するAE報告もないため、臨床的に重大な問題とは考えにくい。内部記録のみとする。
        *   **判断理由:** 減少幅が小さく、臨床症状も伴わないため、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: VS (Weight), AEドメイン
    *   **確認事項No.:** I-4 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 既往歴「HYPERTENSION」の開始日が欠損している。既往歴の詳細な開始日は必須情報ではなく、評価への影響は限定的と判断。修正は不要。
        *   **判断理由:** データ欠損による評価への影響が小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHSTDTC (欠損)
    *   **確認事項No.:** I-5 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA / Medical Monitor
        *   **疑義事項/確認内容:** 治験中止時の治験薬漸減手順が実施されなかった可能性がある。Placebo群であるため安全性への影響は小さいと考えられるが、プロトコル遵守の観点から記録する。
        *   **判断理由:** Placebo群であり、安全性リスクが低いため医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: EX, DS
            *   関連するプロトコル箇所: 3.10.1 Discontinuations

---

# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    77歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、計画された治療群および実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年03月27日発症、PRIMARY DIAGNOSIS）、心筋梗塞（2000年05月15日発症）、冠動脈バイパス術（2006年12月16日実施）が報告されている。教育歴は12年。治験薬初回投与日（Reference Start Date）は2013年10月06日、治験薬最終投与日（Reference End Date）は2013年11月18日。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年09月20日|Day -16 (SCREENING 1)|身長 170.18 cm, 体重 63.5 kg。血圧(臥位) 144/70 mmHg, (立位1分) 130/76 mmHg, (立位3分) 130/74 mmHg。脈拍(臥位) 76 bpm, (立位1分) 84 bpm, (立位3分) 80 bpm。クレアチニン 1.8 mg/dL (基準値上限1.6を超えHIGH)。MMSE 21点。Hachinski Ischemic Score 0点。|
|2013年09月27日|Day -9 (SCREENING 2)|血圧(臥位) 132/66 mmHg, (立位1分) 126/70 mmHg, (立位3分) 124/66 mmHg。脈拍(臥位) 70 bpm, (立位1分) 80 bpm, (立位3分) 76 bpm。|
|2013年10月06日|Day 1 (BASELINE)|治験薬Xanomeline 54mg Patch投与開始。血圧(臥位) 144/70 mmHg, (立位1分) 120/66 mmHg, (立位3分) 130/68 mmHg。脈拍(臥位) 76 bpm, (立位1分) 72 bpm, (立位3分) 80 bpm。体重 63.05 kg。ADAS-Cog(11) Total Score 27点。NPI-X Total Score 61点。併用薬Premarin 0.625mg QOD開始。|
|2013年10月18日|Day 13 (AMBUL ECG PLACEMENT)|血圧(臥位) 134/64 mmHg, (立位1分) 110/66 mmHg, (立位3分) 116/70 mmHg。脈拍(臥位) 72 bpm, (立位1分) 80 bpm, (立位3分) 80 bpm。|
|2013年10月19日|Day 14 (WEEK 2)|治験薬Xanomeline 54mg Patch投与終了。有害事象「Myocardial Infarction」(MILD, 関連性なし, 処置: Drug Withdrawn, Day 45に回復/解決), 「Ventricular Septal Defect」(MILD, 関連性なし, 未回復/未解決), 「Late effects of cerebral infarction」(SEVERE, 関連性なし, Day 44まで未回復/未解決) 発現。血圧(臥位) 112/60 mmHg, (立位1分) 106/58 mmHg, (立位3分) 104/56 mmHg (ベースラインより低下傾向)。脈拍(臥位) 68 bpm, (立位1分) 68 bpm, (立位3分) 68 bpm。アルブミン 3.3 g/dL (LOW)。BUN 29 mg/dL (HIGH)。クレアチニン 1.6 mg/dL (NORMAL)。NPI-X Total Score 22点 (ベースラインより改善)。|
|2013年10月20日|Day 15 (N/A)|治験薬Xanomeline 81mg Patch投与開始 (増量)。|
|2013年10月29日|Day 24 (N/A)|併用薬Premarin投与終了。|
|2013年11月01日|Day 27 (WEEK 4)|アルブミン 3.4 g/dL (LOW)。Disposition: FINAL LAB VISIT (OTHER EVENT)。|
|2013年11月05日|Day 31 (N/A)|有害事象「Rash」(MILD, 関連性Probable, Day 48に回復/解決), 「Pruritus」(MILD, 関連性Probable, Day 48に回復/解決) 発現。|
|2013年11月06日|Day 32 (N/A)|併用薬Hydrocortisone, Topical 開始。|
|2013年11月09日|Day 35 (WEEK 4)|血圧(臥位) 124/66 mmHg, (立位1分) 110/60 mmHg, (立位3分) 106/60 mmHg。脈拍(臥位) 72 bpm, (立位1分) 72 bpm, (立位3分) 76 bpm。NPI-X Total Score 38点 (Week 2より悪化)。|
|2013年11月11日|Day 37 (AMBUL ECG REMOVAL)|Visit実施。|
|2013年11月18日|Day 44 (N/A)|治験薬Xanomeline 81mg Patch最終投与。有害事象「Brain Death」(SEVERE, 関連性なし, 回復/解決と記録されているが医学的に疑義あり) 発現・同日終了？ 有害事象「Late effects of cerebral infarction」終了。|
|2013年11月19日|Day 45 (N/A)|有害事象「Myocardial Infarction」終了 (回復/解決)。|
|2013年11月22日|Day 48 (N/A)|有害事象「Rash」「Pruritus」終了 (回復/解決)。併用薬Hydrocortisone, Topical 終了。|
|2013年11月24日|Day 50 (WEEK 6)|Disposition: ADVERSE EVENTにより試験中止。血圧(臥位) 132/60 mmHg, (立位1分) 114/60 mmHg, (立位3分) 112/56 mmHg。脈拍(臥位) 64 bpm, (立位1分) 68 bpm, (立位3分) 64 bpm。ADAS-Cog(11) Total Score 30点 (ベースラインより悪化)。CIBIC+ Score 4 (No Change)。NPI-X Total Score 16点 (Week 4より改善)。|
|2013年12月06日|Day 62 (AE FOLLOW-UP)|参加終了日。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「Brain Death」(Day 44, SEVERE) の転帰が「RECOVERED/RESOLVED」と記録されているが、これは医学的にあり得ない。DMドメインに死亡フラグや死亡日の記録はないが、このAEは死亡を示唆する可能性が極めて高い。患者の最終的な状態について緊急の確認が必要。
        *   **根拠:** Brain Deathは不可逆的な脳機能の停止であり、回復/解決は定義上ありえない。一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BRAIN DEATH'
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-18'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Subject Death Flag(DM.DTHFL)] = '' (欠損)
            *   [Date/Time of Death(DM.DTHDTC)] = '' (欠損)
    *   **指摘No.:** M-2
        *   **重要度:** Critical
        *   **内容:** 有害事象「Myocardial Infarction」(Day 14, MILD) が報告されている。既往歴に心筋梗塞と冠動脈バイパス術があり心血管リスクが高い患者である。治験薬との関連性は「NONE」とされているが、発現時期（治験薬投与開始後）を考慮すると慎重な評価が必要。重症度が「MILD」とされている点も、心筋梗塞としては軽微すぎる可能性があり、評価の妥当性に疑問がある。また、Action Takenが「DRUG WITHDRAWN」と記録されているにも関わらず、翌日に治験薬が増量されており、記録と実際の処置に重大な矛盾がある。患者の安全性確保の観点から、事象の詳細、評価の妥当性、実際の処置について緊急の確認が必要。
        *   **根拠:** 心筋梗塞は通常、重篤なイベントであり、MILDとの評価は一般的ではない。既往歴からリスクが高い患者での発症であり、治験薬との関連性を安易に否定すべきではない。処置記録の矛盾は患者の安全管理上の重大な問題を示唆する。一般的な医学知識、プロトコル 3.9.3.2.2 (SAE), 3.10.1 (Discontinuations)。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (81mg dose)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「Late effects of cerebral infarction」(Day 14, SEVERE) が報告されている。重症度がSEVEREであり、Day 44まで継続している。治験薬との関連は「NONE」とされているが、患者の状態悪化に寄与した可能性や、アルツハイマー病の進行との鑑別について、より詳細な情報が必要。
        *   **根拠:** 重症な神経学的イベントであり、患者のQOLや安全性評価に影響する。一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-18'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 有害事象「Ventricular Septal Defect」(Day 14, MILD) が報告されている。これは通常先天性の心疾患であり、成人での新規発症は考えにくい。既往歴に記載がなく、スクリーニング時の心電図所見との関連も不明。報告内容の正確性（誤診や別の事象の誤記の可能性）、臨床的意義について確認が必要。
        *   **根拠:** 疾患の性質と発症時期の不一致。一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VENTRICULAR SEPTAL DEFECT'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '' (欠損)
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「Rash」および「Pruritus」(Day 31, MILD) は治験薬との関連が「PROBABLE」と評価されており、Xanomeline TTSの副作用の可能性が高い。Hydrocortisone Topicalによる治療で回復している。
        *   **根拠:** 治験薬との時間的関連、薬剤クラスの既知の副作用プロファイル。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH', 'PRURITUS'
            *   [Causality(AE.AEREL)] = 'PROBABLE'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** スクリーニング時 (Day -16) のクレアチニン値が1.8 mg/dLと基準値上限 (1.6 mg/dL) を超えており、プロトコルの除外基準 [27b] に抵触する可能性がある。Week 2では正常化しているが、腎機能には注意が必要であり、適格性について確認が必要。
        *   **根拠:** プロトコル除外基準抵触の可能性。腎機能低下は薬剤の安全性に影響しうる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.8' (Day -16), '1.6' (Day 14)
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day -16), 'NORMAL' (Day 14)
            *   プロトコル Section 3.4.2.2 [27b]
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** Week 2 (Day 14) のBUN値が29 mg/dLと基準値上限 (24 mg/dL) を超えている。脱水や腎機能低下の可能性を示唆するが、Week 4では正常化している。クレアチニン値の変動と合わせて軽微な変動と考えられる。
        *   **根拠:** 一過性の基準値逸脱。一般的な医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '29' (Day 14), '23' (Day 27)
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '24'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day 14), 'NORMAL' (Day 27)
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** Week 2 (Day 14) および Week 4 (Day 27) のアルブミン値が基準値下限 (3.5 g/dL) を下回っている (3.3, 3.4 g/dL)。軽度の低下であり、臨床的意義は限定的かもしれないが、栄養状態や他の臨床所見との関連で注意が必要。
        *   **根拠:** 軽度の基準値逸脱。一般的な医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '3.3' (Day 14), '3.4' (Day 27)
            *   [Reference Range Lower Limit in Orig Unit(LB.LBORNRLO)] = '3.5'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (Day 14, Day 27)
    *   **指摘No.:** M-9
        *   **重要度:** Major
        *   **内容:** 治験薬投与開始後、特にWeek 2 (Day 14) で血圧低下傾向が見られる (例: 立位収縮期血圧 Baseline 120 -> Week 2 104 mmHg)。起立性低血圧の可能性も示唆される (臥位と立位の収縮期血圧差がWeek 2で6-8 mmHg程度だが、拡張期血圧は立位で低下傾向)。心血管系AE (心筋梗塞) との時間的関連も考慮し、臨床的な意義について評価が必要。
        *   **根拠:** 薬剤投与後の血圧変動パターン。心血管リスクの高い患者背景。一般的な医学知識。
        *   **関連データ:**
            *   VSドメインの血圧データ (SYSBP, DIABP)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYOCARDIAL INFARCTION'
    *   **指摘No.:** M-10
        *   **重要度:** Minor
        *   **内容:** 主要評価項目であるADAS-Cog(11) Total ScoreはBaseline 27からWeek 6 (Day 50) で30に悪化。CIBIC+はWeek 6で4 (No Change)。本症例において有効性を示唆する結果ではない。
        *   **根拠:** 有効性評価指標の経時変化。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)]
    *   **指摘No.:** M-11
        *   **重要度:** Minor
        *   **内容:** 副次評価項目であるNPI-X Total ScoreはBaseline 61から変動が大きい (Week 2: 22, Week 4: 38, Week 6: 16)。一貫した改善傾向は見られず、有効性の評価は困難。
        *   **根拠:** 有効性評価指標の経時変化。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)]

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** AE「Myocardial Infarction」の処置 (AEACN='DRUG WITHDRAWN') とEXドメインの記録 (AE発生翌日に治験薬増量) が矛盾している。患者の安全性管理とデータの信頼性に重大な影響を与える。
        *   **根拠:** ドメイン間の論理的な不整合。
        *   **関連データ:**
            *   [Action Taken with Study Treatment(AE.AEACN)] = 'DRUG WITHDRAWN' (AESEQ=1)
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-10-20' (EXSEQ=2, Dose=81mg)
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-19' (AESEQ=1)
    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** AE「Brain Death」の転帰 (AEOUT='RECOVERED/RESOLVED') が医学的にありえず、DMドメインの死亡情報 (DTHFL, DTHDTC) が欠損していることと合わせて、患者の最終状態に関するデータに重大な不整合がある。試験結果の解釈に影響する。
        *   **根拠:** 医学的常識との矛盾、必須情報の欠損。
        *   **関連データ:**
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED' (AESEQ=3)
            *   [Subject Death Flag(DM.DTHFL)] = '' (欠損)
            *   [Date/Time of Death(DM.DTHDTC)] = '' (欠損)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** AE「Ventricular Septal Defect」の終了日 (AEENDTC) が欠損している。イベントの継続状況が不明確だが、転帰は未回復/未解決と記録されており、主要な評価への影響は限定的か。
        *   **根拠:** データの欠損。
        *   **関連データ:**
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '' (欠損) (AESEQ=2)
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** DSドメインのAEによる中止理由について、RELRECデータからはAE「RASH」(MILD) が関連付けられているが、他の重篤/重症AEとの関連が記録されておらず、実際の中止理由が不明確。中止理由の特定は安全性評価において重要。
        *   **根拠:** DSとAE/RELREC間の関連情報の不整合または不明瞭さ。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT' (DSSEQ=1)
            *   RELRECデータ (RELID='01-704-1017-E11' が DSSEQ=1, AESEQ=5, AESEQ=7 に関連)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH' (AESEQ=5, 7)
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** DSドメインにプロトコル外の「FINAL LAB VISIT」(Day 27) が記録されている。このVisitの目的と、試験中止との関連が不明。データの解釈に影響する可能性がある。
        *   **根拠:** 予定外のイベント記録。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT' (DSSEQ=2)
            *   [Category for Disposition Event(DS.DSCAT)] = 'OTHER EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-01'
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 併用薬Hydrocortisone TopicalのIndication (CMINDC) が欠損している。AEとの関連から推測は可能だが、記録としては不備。
        *   **根拠:** 必須ではないが重要な情報の欠損。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Indication(CM.CMINDC)] = '' (欠損)
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** 併用薬PremarinのIndication (CMINDC) が欠損している。
        *   **根拠:** 必須ではないが重要な情報の欠損。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'
            *   [Indication(CM.CMINDC)] = '' (欠損)
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** MHドメインの既往歴用語とAEドメインの有害事象用語に不一致が見られる (例: HEART ATTACK vs MYOCARDIAL INFARCTION)。コーディングによる標準化はされている可能性があるが、一貫性の観点からは注意が必要。
        *   **根拠:** 用語の不一致。
        *   **関連データ:**
            *   MH.MHTERM, AE.AETERM
    *   **指摘No.:** D-9
        *   **重要度:** Major
        *   **内容:** AE「Rash」および「Pruritus」がそれぞれ2回 (異なるAESEQで) 記録されている。記録日 (AEDTC) は異なるが、他の情報は同一。重複記録なのか、イベントの再発・悪化なのか不明瞭。中止理由との関連 (RELREC) もあり、正確なイベント把握が必要。
        *   **根拠:** 同一イベントの複数回記録。
        *   **関連データ:**
            *   AEドメイン (AESEQ=5, 7 for RASH; AESEQ=6, 8 for PRURITUS)
    *   **指摘No.:** D-10
        *   **重要度:** Minor
        *   **内容:** AE「Myocardial Infarction」の終了日 (Day 45) が治験薬最終投与日 (Day 44) より後になっている。医学的にはありうるが、AEACN='DRUG WITHDRAWN' との関連で確認が望ましい。
        *   **根拠:** 日付の前後関係。
        *   **関連データ:**
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-19' (AESEQ=1)
            *   [Date/Time of Last Study Treatment(DM.RFXENDTC)] = '2013-11-18'
    *   **指摘No.:** D-11
        *   **重要度:** Minor
        *   **内容:** スクリーニング時のクレアチニン高値、Week 2のBUN高値は基準値逸脱。医学的レビュー(M-6, M-7)で指摘済み。
        *   **根拠:** 基準値からの逸脱。
        *   **関連データ:** LB.LBTESTCD='CREAT', 'BUN'
    *   **指摘No.:** D-12
        *   **重要度:** Minor
        *   **内容:** Week 2, Week 4のアルブミン低値は基準値逸脱。医学的レビュー(M-8)で指摘済み。
        *   **根拠:** 基準値からの逸脱。
        *   **関連データ:** LB.LBTESTCD='ALB'
    *   **指摘No.:** D-13
        *   **重要度:** Minor
        *   **内容:** AE「Ventricular Septal Defect」の終了日欠損。D-3で指摘済み。
        *   **根拠:** データの欠損。
        *   **関連データ:** AE.AEENDTC (AESEQ=2)
    *   **指摘No.:** D-14
        *   **重要度:** Minor
        *   **内容:** CM Indicationの一部欠損。D-6, D-7で指摘済み。
        *   **根拠:** データの欠損。
        *   **関連データ:** CM.CMINDC
    *   **指摘No.:** D-15
        *   **重要度:** Major
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。プロトコル遵守の確認に必須の情報。
        *   **根拠:** 必須情報の欠損。
        *   **関連データ:** [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が欠損しており、プロトコルで要求される同意取得手続き (Inclusion [6]) が適切に行われたか確認できない。参加者の権利保護に関わる。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [6], Section 5.1
        *   **根拠:** 必須情報の欠損。
        *   **関連データ:** [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時のECG所見 (MH: ST segment elevation/depression, Extrasystoles) が、除外基準 [16b] に該当する可能性がある。ECGデータの詳細な評価が必要だが、データが提供されていないため判断不可。不適格な患者が登録された可能性。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [16b]
        *   **根拠:** MHデータと除外基準の照合。必要なECGデータ欠損。
        *   **関連データ:** MHドメイン (MHTERM='VERBATIM_0806', 'VERBATIM_1153', 'VERBATIM_1608')
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 既往歴に心筋梗塞 (2000年) と冠動脈バイパス術 (2006年) があり、除外基準 [17] の「serious cardiovascular disorder」に該当する可能性が高い。5年以内のイベントではないが、患者の安全性リスクを考慮すると適格性に疑問がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17]
        *   **根拠:** MHデータと除外基準の照合。
        *   **関連データ:** MHドメイン (MHTERM='HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT')
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時のクレアチニン値 (1.8 mg/dL) が基準値上限 (1.6 mg/dL) を超えており、除外基準 [27b] に抵触する可能性がある。不適格な患者が登録された可能性。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LBデータと除外基準の照合。
        *   **関連データ:** LBドメイン (LBTESTCD='CREAT', LBORRES='1.8', LBNRIND='HIGH' at Day -16)
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** High Dose群の投与レジメンについて、プロトコル内の記載 (3.1 Figure LZZT.1 vs 3.6.2) に曖昧さがあるが、EXドメインの記録 (Day 1-14: 54mg, Day 15-44: 81mg) はFigure LZZT.1の計画と一致しているように見える。逸脱の可能性は低いが、プロトコル記載の明確化が望ましい。
        *   **プロトコル該当箇所:** Section 3.1, Figure LZZT.1, Section 3.6.2
        *   **根拠:** EXデータとプロトコル記載の照合。
        *   **関連データ:** EXドメイン
    *   **指摘No.:** P-6
        *   **重要度:** Critical
        *   **逸脱の可能性:** 有害事象「Myocardial Infarction」(Day 14) 発生にも関わらず、翌日 (Day 15) に治験薬を高用量 (81mg) に増量している。プロトコルの安全性監視 (3.9.4) や中止基準 (3.10.1) の観点から、極めて不適切な対応であり、重大なプロトコル逸脱の可能性が高い。患者の安全性を著しく損なう行為。
        *   **プロトコル該当箇所:** Section 3.9.4, Section 3.10.1
        *   **根拠:** AE発生後の不適切な治験薬増量。
        *   **関連データ:** AEドメイン (AESEQ=1), EXドメイン (EXSEQ=2)
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験薬最終投与日 (Day 44) とAEによる中止日 (Day 50) にずれがある。臨床的な判断によるものかもしれないが、記録として明確化が必要。
        *   **プロトコル該当箇所:** Section 3.10.1
        *   **根拠:** 日付のずれ。
        *   **関連データ:** DM.RFXENDTC, DS.DSSTDTC (DSSEQ=1)
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたWeek 6 (Visit 7) 以降の臨床検査 (血液学、生化学) が実施されていない可能性がある。DSドメインのDay 27の「FINAL LAB VISIT」が最後の検査か？安全性モニタリングの逸脱。
        *   **プロトコル該当箇所:** Section 3.9.3.3, Protocol Attachment LZZT.1
        *   **根拠:** LBデータの欠損とプロトコルスケジュールの比較。
        *   **関連データ:** LBドメイン, DSドメイン (DSSEQ=2)
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたECG評価 (Visit 4以降定期的、Ambulatory ECG at Visit 2) のデータが提供されておらず、実施状況が不明。心血管リスクの高い患者であり、安全性モニタリングの逸脱の可能性。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2, Section 3.9.4, Protocol Attachment LZZT.1
        *   **根拠:** 必要な安全性評価データの欠損。
        *   **関連データ:** (ECGデータなし)
    *   **指摘No.:** P-10
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルで規定されたPK測定 (Visit 3, 4, 5, 7, 9, 11) のデータが提供されておらず、実施状況が不明。主要な評価項目ではないが、逸脱の可能性。
        *   **プロトコル該当箇所:** Section 3.9.2, Protocol Attachment LZZT.1
        *   **根拠:** 必要な評価データの欠損。
        *   **関連データ:** (PKデータなし)
    *   **指摘No.:** P-11
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 5 (Week 4) および Visit 7 (Week 6) の実施日が、プロトコルで規定されたVisit Window (+/-3日) を逸脱している (+7日, +8日)。評価スケジュールの逸脱であり、データの信頼性に影響する可能性。
        *   **プロトコル該当箇所:** Section 3.1
        *   **根拠:** SVデータとプロトコル規定の比較。
        *   **関連データ:** SVドメイン (SVSTDTC for VISITNUM=5, 7)
    *   **指摘No.:** P-12
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日欠損のため、同意取得と治験手順開始の関係が確認できない。P-1で指摘済み。
        *   **プロトコル該当箇所:** Section 5.1
        *   **根拠:** 必須情報の欠損。
        *   **関連データ:** DM.RFICDTC
    *   **指摘No.:** P-13
        *   **重要度:** Major
        *   **逸脱の可能性:** AEによる中止理由がRELRECデータからはMILDなRashとされているが、他の重篤/重症AEが発生しており、記録された中止理由の妥当性に疑問がある。プロトコル 3.10.1 に基づく適切な中止判断が行われたか不明。D-4で指摘済み。
        *   **プロトコル該当箇所:** Section 3.10.1
        *   **根拠:** DS/RELRECデータとAEデータの比較。
        *   **関連データ:** DS, RELREC, AEドメイン
    *   **指摘No.:** P-14
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル 3.10.1 で規定されている中止時の治験薬漸減投与が実施されたか不明。EXドメインではDay 44まで81mgが投与された記録のみ。
        *   **プロトコル該当箇所:** Section 3.10.1
        *   **根拠:** EXデータとプロトコル規定の比較。
        *   **関連データ:** EXドメイン

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-2)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象名「BRAIN DEATH」がStudy Day 44に報告され、転帰が「RECOVERED/RESOLVED」と記録されています。Brain Deathは通常回復しない状態ですが、患者様の最終的な状態（死亡されたか、別の状態であったか等）について詳細な情報と記録の修正をお願いします。DMドメインの死亡フラグ、死亡日も未入力です。患者様の最終転帰の正確な把握は安全性評価に不可欠です。
        *   **クエリ文面（英語）:** The AE Term 'BRAIN DEATH' was reported on Study Day 44 with an Outcome of 'RECOVERED/RESOLVED'. As Brain Death is typically irreversible, please provide details on the subject's final status (e.g., death, other condition) and correct the record accordingly. Death flag and date are also missing in DM. Accurate final outcome is crucial for safety assessment.
        *   **判断理由:** 患者の最終転帰に関する重大な不整合であり、死亡の可能性が高いため、緊急の確認と修正が必要。参加者の状態把握と安全性評価の根幹に関わる。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='BRAIN DEATH', AE.AEOUT='RECOVERED/RESOLVED', AE.AESTDTC='2013-11-18', AE.AEENDTC='2013-11-18', DM.DTHFL='', DM.DTHDTC=''
            *   関連する医学的知見: Brain Deathの定義。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-1, P-6)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 14に有害事象名「MYOCARDIAL INFARCTION」が報告されています。重症度が「MILD」、治験薬との関連性が「NONE」と評価されていますが、心筋梗塞としては評価が軽微に思われます。評価根拠をご教示ください。また、処置が「DRUG WITHDRAWN」と記録されているにも関わらず、翌日Study Day 15に治験薬が増量されています。実際の処置と記録の矛盾について確認し、修正をお願いします。心血管リスクの高い患者様であり、正確な評価と処置の記録が安全性確保に不可欠です。
        *   **クエリ文面（英語）:** AE Term 'MYOCARDIAL INFARCTION' was reported on Study Day 14, assessed as 'MILD' severity and 'NONE' relationship to study drug. This assessment seems unusually mild for MI. Please provide rationale. Also, Action Taken is 'DRUG WITHDRAWN', but EX shows dose increase on Day 15. Please confirm/correct the discrepancy between record and actual action. Accurate assessment/action record is vital for this high-risk patient's safety.
        *   **判断理由:** 重篤な可能性のあるAEの評価妥当性への疑義と、処置記録の重大な矛盾。患者の安全性管理とデータの信頼性に直結する。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='MYOCARDIAL INFARCTION', AE.AESEV='MILD', AE.AEREL='NONE', AE.AEACN='DRUG WITHDRAWN', AE.AESTDTC='2013-10-19', EX.EXSTDTC='2013-10-20', EX.EXDOSE=81, MHデータ (心筋梗塞、CABG既往)
            *   関連する医学的知見: 心筋梗塞の一般的重症度。
            *   関連するプロトコル箇所: Section 3.9.4, 3.10.1
    *   **クエリNo.:** Q-3 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 14に有害事象名「VENTRICULAR SEPTAL DEFECT」が報告されています。これは通常先天性疾患ですが、既往歴には記載がありませんでした。本イベントの診断根拠、臨床的意義、および成人での新規発症と考えられる理由について詳細をご教示ください。報告内容の正確性確認のためお願いします。
        *   **クエリ文面（英語）:** AE Term 'VENTRICULAR SEPTAL DEFECT' was reported on Study Day 14. This is typically congenital, but not in MH. Please provide diagnostic basis, clinical significance, and reason for considering new onset in an adult. This is for confirming report accuracy.
        *   **判断理由:** 報告されたイベントと患者背景（年齢、既往歴）との医学的な不整合。データの正確性確認が必要。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='VENTRICULAR SEPTAL DEFECT', AE.AESTDTC='2013-10-19', MHドメイン
            *   関連する医学的知見: 心室中隔欠損症の病態。
    *   **クエリNo.:** Q-4 (関連指摘No.: M-6, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時 (Study Day -16) のクレアチニンが「1.8 mg/dL」であり、施設基準値上限「1.6 mg/dL」を超えています。プロトコル除外基準 3.4.2.2 [27b] に抵触する可能性があります。本患者様の適格性評価について、逸脱に該当しないと判断された根拠をご教示ください。
        *   **クエリ文面（英語）:** Screening Creatinine on Study Day -16 was '1.8 mg/dL', exceeding the site's upper limit of '1.6 mg/dL'. This may potentially violate protocol exclusion criterion 3.4.2.2 [27b]. Please provide the rationale for determining the subject eligible despite this value.
        *   **判断理由:** 除外基準抵触の可能性があり、患者適格性の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='CREAT', LB.LBORRES='1.8', LB.LBORNRHI='1.6', LB.LBNRIND='HIGH' (Day -16)
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-5 (関連指摘No.: D-15, P-1, P-12)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日（Date/Time of Informed Consent）がDMドメインに入力されていません。プロトコル遵守（Inclusion [6], Section 5.1）の確認のため、同意取得日をご提供ください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing in the DM domain. Please provide the date to confirm compliance with protocol requirements (Inclusion [6], Section 5.1).
        *   **判断理由:** 同意取得はGCPの根幹であり、日付の確認は必須。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC='' (欠損)
            *   関連するプロトコル箇所: Section 3.4.2.1 [6], Section 5.1
    *   **クエリNo.:** Q-6 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Medical Historyにスクリーニング時のECG所見として「ST SEGMENT ELEVATED」「ST SEGMENT DEPRESSED」「EXTRASYSTOLES」が報告されています。これらの所見がプロトコル除外基準 3.4.2.2 [16b] に記載の具体的な条件に該当しないか、評価結果をご教示ください。適格性確認のためお願いします。
        *   **クエリ文面（英語）:** MH reports screening ECG findings 'ST SEGMENT ELEVATED', 'ST SEGMENT DEPRESSED', 'EXTRASYSTOLES'. Please confirm whether these findings met any specific conditions listed in exclusion criterion 3.4.2.2 [16b]. This is for eligibility confirmation.
        *   **判断理由:** スクリーニングECG所見が除外基準に抵触する可能性があり、適格性の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン (MHTERM='VERBATIM_0806', 'VERBATIM_1153', 'VERBATIM_1608')
            *   関連するプロトコル箇所: Section 3.4.2.2 [16b]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Medical Historyに心筋梗塞（2000年）および冠動脈バイパス術（2006年）の既往が報告されています。プロトコル除外基準 3.4.2.2 [17] の「serious cardiovascular disorder」に該当する可能性があります。本患者様の適格性評価について、逸脱に該当しないと判断された根拠をご教示ください。
        *   **クエリ文面（英語）:** MH reports history of Myocardial Infarction (2000) and CABG (2006). This may potentially meet exclusion criterion 3.4.2.2 [17] 'serious cardiovascular disorder'. Please provide the rationale for determining the subject eligible despite this history.
        *   **判断理由:** 既往歴が除外基準に抵触する可能性があり、適格性の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン (MHTERM='HEART ATTACK', 'TRIPLE VESSEL BYPASS GRAFT')
            *   関連するプロトコル箇所: Section 3.4.2.2 [17]
    *   **クエリNo.:** Q-8 (関連指摘No.: D-4, P-13)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DispositionとしてStudy Day 50に「ADVERSE EVENT」により中止と記録されています。RELRECデータではAE「RASH」が関連付けられていますが、これはMILDな事象です。他に重篤/重症なAE（Brain Death, Myocardial Infarction, Late effects of cerebral infarction）も発生していますが、これらが中止理由でしょうか？実際の中止理由となったAEについて確認し、記録の修正をお願いします。
        *   **クエリ文面（英語）:** Disposition on Study Day 50 is 'ADVERSE EVENT'. RELREC links this to AE 'RASH' (MILD). However, other severe/serious AEs (Brain Death, MI, Late effects of cerebral infarction) occurred. Please confirm the actual AE leading to discontinuation and correct the record if necessary.
        *   **判断理由:** 記録された中止理由と臨床経過に乖離があり、正確な中止理由の特定が必要。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='ADVERSE EVENT' (DSSEQ=1), RELRECデータ, AEドメイン
            *   関連するプロトコル箇所: Section 3.10.1
    *   **クエリNo.:** Q-9 (関連指摘No.: P-11)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 5 (Week 4) の実施日が予定日 Study Day 28に対しStudy Day 35、Visit 7 (Week 6) の実施日が予定日 Study Day 42に対しStudy Day 50 となっており、プロトコル規定のVisit Window (+/-3日) を逸脱しています。逸脱理由をご教示ください。
        *   **クエリ文面（英語）:** Visit 5 (Week 4) was conducted on Study Day 35 (planned Day 28) and Visit 7 (Week 6) on Study Day 50 (planned Day 42). Both deviate from the protocol-specified visit window (+/-3 days). Please provide the reason for these deviations.
        *   **判断理由:** プロトコルからの逸脱であり、理由の記録が必要。評価タイミングのずれがデータ解釈に影響する可能性。
        *   **判断根拠:**
            *   関連するデータ: SV.SVSTDTC (VISITNUM=5, 7), TV.VISITDY (VISITNUM=5, 7)
            *   関連するプロトコル箇所: Section 3.1
    *   **クエリNo.:** Q-10 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 14に有害事象名「LATE EFFECTS OF CEREBRAL INFARCTION」が重症度「SEVERE」で報告されています。本イベントの具体的な症状や臨床経過、アルツハイマー病の進行との関連について、詳細な情報をご提供ください。
        *   **クエリ文面（英語）:** AE Term 'LATE EFFECTS OF CEREBRAL INFARCTION' (Severity 'SEVERE') was reported on Study Day 14. Please provide more details on the specific symptoms, clinical course, and relationship to Alzheimer's disease progression for this event.
        *   **判断理由:** 重症なイベントであり、患者の状態を正確に把握するために詳細情報が必要。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', AE.AESEV='SEVERE', AE.AESTDTC='2013-10-19'
    *   **クエリNo.:** Q-11 (関連指摘No.: M-9)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 治験薬投与開始後、特にStudy Day 14 (Week 2) において血圧低下傾向が見られます。起立性低血圧の症状の有無や、同時期に発現した有害事象「Myocardial Infarction」との関連を含め、この血圧変動の臨床的意義について評価をお願いします。
        *   **クエリ文面（英語）:** A trend of decreased blood pressure was observed after study drug initiation, particularly on Study Day 14 (Week 2). Please assess the clinical significance of this BP change, including any symptoms of orthostatic hypotension and its potential relation to the concurrent AE 'Myocardial Infarction'.
        *   **判断理由:** 心血管リスクの高い患者における血圧低下であり、臨床的意義とAEとの関連評価が必要。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (SYSBP, DIABP), AEドメイン (AESEQ=1)
    *   **クエリNo.:** Q-12 (関連指摘No.: D-9)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「RASH」がAESEQ=5と7で、「PRURITUS」がAESEQ=6と8で、それぞれ2回記録されています。開始日、終了日、重症度等は同じですが、記録日(AEDTC)が異なります。これらは重複記録でしょうか、それともイベントの再発・悪化等でしょうか？ご確認の上、必要であれば記録の修正をお願いします。
        *   **クエリ文面（英語）:** AE 'RASH' is recorded twice (AESEQ=5, 7) and 'PRURITUS' twice (AESEQ=6, 8). Dates, severity etc. are identical, but collection dates (AEDTC) differ. Are these duplicate entries, or recurrence/worsening? Please clarify and correct if necessary.
        *   **判断理由:** データの一貫性と正確性確保のため、重複記録の可能性を確認する必要がある。中止理由との関連もあり重要。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=5, 6, 7, 8), RELRECデータ
    *   **クエリNo.:** Q-13 (関連指摘No.: D-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 27にDispositionとして「FINAL LAB VISIT」が記録されています。これはプロトコル上の予定Visitではありませんが、どのような理由で実施されたのでしょうか？治験中止の決定と関連がありますか？
        *   **クエリ文面（英語）:** Disposition 'FINAL LAB VISIT' was recorded on Study Day 27. This was not a scheduled visit per protocol. Please clarify the reason for this visit. Was it related to the decision for study discontinuation?
        *   **判断理由:** 予定外のイベント記録であり、その背景と意義を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: DSドメイン (DSSEQ=2), TVドメイン
    *   **クエリNo.:** Q-14 (関連指摘No.: P-8, P-9, P-10)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではWeek 6以降も定期的な臨床検査（血液学、生化学）、ECG、および特定のVisitでのPK測定が規定されていますが、本症例ではWeek 4 (Study Day 27) 以降の臨床検査データ、およびECG、PKデータが提供されていません。これらの評価は実施されなかったのでしょうか？実施されなかった場合、その理由をご教示ください。
        *   **クエリ文面（英語）:** Protocol requires lab tests (Hem/Chem), ECGs after Week 6, and PK sampling at specific visits. Data for labs after Day 27, ECGs, and PK are missing. Were these assessments not performed? If not, please provide the reason.
        *   **判断理由:** プロトコルで規定された安全性およびPK評価の実施状況を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: LB, (ECG/PKデータなし)
            *   関連するプロトコル箇所: Section 3.9.2, 3.9.3.3, 3.9.3.4.2, Protocol Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** AE「Rash」「Pruritus」は治験薬との関連がProbableと評価されており、既知の副作用プロファイルと一致する。Hydrocortisoneで管理され回復しており、現時点では追加のアクションは不要と判断。
        *   **判断理由:** 既知の副作用であり、適切に管理・回復しているため、医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=5, 6, 7, 8), CMドメイン
    *   **確認事項No.:** I-2 (関連指摘No.: M-7, M-8)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 2のBUN高値、Week 2/4のアルブミン低値は一過性または軽度であり、他の臨床所見と合わせて現時点では重大な懸念とは判断しない。ただし、腎機能や栄養状態の変動として記録しておく。
        *   **判断理由:** 臨床的意義が限定的と考えられる軽微な検査値異常であり、問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='BUN', 'ALB')
    *   **確認事項No.:** I-3 (関連指摘No.: M-10, M-11)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** ADAS-Cog(11)の悪化、NPI-Xの変動が見られ、本症例では有効性は示唆されない。試験中止までの期間が短いため評価は限定的。有効性評価の全体集計時に考慮する。
        *   **判断理由:** 個別症例の有効性データであり、現時点で追加アクションは不要。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSCAT='ALZHEIMER''S DISEASE ASSESSMENT SCALE', 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)')
    *   **確認事項No.:** I-4 (関連指摘No.: D-3, D-13)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「Ventricular Septal Defect」の終了日欠損。転帰は未回復/未解決であり、主要評価への影響は小さいと判断。可能であれば他のクエリと併せて確認する。
        *   **判断理由:** 主要評価への影響が小さいデータの欠損。
        *   **判断根拠:**
            *   関連するデータ: AE.AEENDTC (AESEQ=2)
    *   **確認事項No.:** I-5 (関連指摘No.: D-6, D-7, D-14)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインのIndication欠損。他の情報から推測可能であり、データの解釈への影響は小さい。修正は必須ではない。
        *   **判断理由:** 主要評価への影響が小さいデータの欠損。
        *   **判断根拠:**
            *   関連するデータ: CM.CMINDC
    *   **確認事項No.:** I-6 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MH/AE用語の不一致。コーディング辞書による標準化が行われている前提で、現時点では問題視しない。データクリーニングプロセスで確認されるべき事項。
        *   **判断理由:** コーディングによる標準化が期待されるため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM, AE.AETERM, MH.MHDECOD, AE.AEDECOD
    *   **確認事項No.:** I-7 (関連指摘No.: D-10)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「Myocardial Infarction」の終了日が治験薬最終投与日より後である点。医学的にありうる範囲であり、他の矛盾点（AEACN）が解決されれば問題ない可能性が高い。
        *   **判断理由:** 医学的に説明可能な日付関係。
        *   **判断根拠:**
            *   関連するデータ: AE.AEENDTC (AESEQ=1), DM.RFXENDTC
    *   **確認事項No.:** I-8 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** High Dose群の投与レジメンについて、プロトコル記載に曖昧さがあるが、実施された投与 (Day 1-14: 54mg, Day 15-44: 81mg) はプロトコル図と一致。逸脱とは判断しない。
        *   **判断理由:** 実際の投与がプロトコル内の計画図と一致しているため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.1 Figure LZZT.1
    *   **確認事項No.:** I-9 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 治験薬最終投与日 (Day 44) とAEによる中止日 (Day 50) のずれ。中止決定プロセスによるものと考えられ、重大な逸脱とは判断しない。
        *   **判断理由:** 臨床現場では起こりうる日付のずれ。
        *   **判断根拠:**
            *   関連するデータ: DM.RFXENDTC, DS.DSSTDTC (DSSEQ=1)
    *   **確認事項No.:** I-10 (関連指摘No.: P-14)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 中止時の治験薬漸減投与の実施状況が不明。EXデータからは確認できないが、記録がないだけで実施された可能性もある。主要な評価への影響は小さい。
        *   **判断理由:** 記録の欠損であり、実施されなかったと断定できない。主要評価への影響小。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン
            *   関連するプロトコル箇所: Section 3.10.1