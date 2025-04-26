# [01-701-1015]のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
63歳、女性、人種はWHITE、民族名はHISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2010年4月30日発症、Primary Diagnosis）、子宮摘出術（1986年）、甲状腺部分切除術（1973年）、扁桃摘出術（1973年）、胆石症（2012年）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年12月26日|Day -7 (SCREENING 1)|Screening実施。MMSE 23点、Hachinskiスコア 1点。ALP 34 U/L (基準値35-115, LOW)、AST 40 U/L (基準値9-34, HIGH)、Anisocytes 1 (ABNORMAL)。他検査は基準値内。血圧 立位3分後 147/57 mmHg。|
|2013年12月31日|Day -2 (SCREENING 2)|血圧 立位3分後 145/71 mmHg。|
|2014年01月02日|Day 1 (BASELINE)|治験薬(Placebo)投与開始。ベースライン評価実施。ADAS-Cog(11) 13点、NPI-X Total Score 0点、DAD 全項目Yes。|
|2014年01月03日|Day 2 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(Mild, Probable) 発現。|
|2014年01月03日|Day 2 (N/A)|有害事象「APPLICATION SITE PRURITUS」(Mild, Probable) 発現。|
|2014年01月03日|Day 2 (N/A)|併用薬「NEOSPORIN /USA/」(Topical, PRN) 開始。|
|2014年01月11日|Day 10 (N/A)|有害事象「DIARRHOEA」(Mild, Serious=Y, Remote) 発現 (終了日 Day 8 と矛盾)。|
|2014年01月16日|Day 15 (WEEK 2)|ALT 41 U/L (基準値6-34, HIGH)。|
|2014年01月30日|Day 29 (WEEK 4)|MCV 78 fL (基準値80-100, LOW)。ALTは正常化 (18 U/L)。|
|2014年03月05日|Day 63 (WEEK 8)|ADAS-Cog(11) 8点。CIBIC+ 4点 (No Change)。DAD 全項目Yes。NPI-X Total Score 0点。|
|2014年03月27日|Day 85 (N/A)|併用薬「HYDROCORTISONE」(Topical, PRN) 開始。|
|2014年03月26日|Day 84 (WEEK 12)|脈拍 52-54 bpm (やや低め)。|
|2014年05月07日|Day 126 (WEEK 16)|MCV 79 fL (基準値80-100, LOW)。収縮期血圧 152-163 mmHg (やや高め)。ADAS-Cog(11) 11点。CIBIC+ 4点 (No Change)。DAD 全項目Yes。NPI-X Total Score 0点。|
|2014年06月18日|Day 168 (WEEK 24)|SPGRAV 1.005 (基準値1.006-1.03, LOW)。ADAS-Cog(11) 8点。CIBIC+ 4点 (No Change)。DAD 全項目Yes。NPI-X Total Score 0点。|
|2014年07月02日|Day 182 (WEEK 26)|治験薬(Placebo)投与終了。試験完了。NPI-X Total Score 0点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象「DIARRHOEA」がSerious（重篤）と報告されているが、その理由（入院、生命を脅かす等）が不明。また、関連性がRemote（なし）と評価されているが、Placebo群であっても薬剤関連の可能性を完全に否定はできない。重篤性の評価根拠と関連性評価の再確認が必要。
        *   **根拠:** 有害事象の重篤性評価は参加者の安全性確保に不可欠。理由不明な重篤判定は安全性評価の信頼性を損なう。一般的な医学知識として、下痢が重篤となる状況（脱水による入院など）は存在する。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA'
            *   [Serious Event(AE.AESER)] = 'Y'
            *   [Causality(AE.AEREL)] = 'REMOTE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2014-01-11'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2014-01-09'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 副次評価項目であるDAD（Disability Assessment for Dementia）の評価結果が、ベースラインから試験終了まで一貫して全項目「Yes」（機能障害なし、スコア100%）となっている。アルツハイマー病患者において、ADLの機能障害が全く認められないというのは医学的に考えにくく、評価が適切に行われたか、あるいは評価基準の適用に問題がなかったか疑問がある。評価の信頼性に影響する可能性がある。
        *   **根拠:** アルツハイマー病は認知機能低下に伴いADL障害を呈することが一般的。Placebo群であってもベースラインから全く障害がないというのは非典型的であり、評価の妥当性を確認する必要がある。
        *   **関連データ:**
            *   [Category of Question(QS.QSCAT)] = 'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)'
            *   [Finding in Original Units(QS.QSORRES)] = 'Y' (for all DAITM* at all timepoints)
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1 (for all DAITM* at all timepoints)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「DIARRHOEA」の開始日（AESTDTC: 2014-01-11, AESTDY: 10）が終了日（AEENDTC: 2014-01-09, AEENDY: 8）よりも後になっており、日付が矛盾している。重篤と報告されたイベントであり、正確な期間の把握は安全性評価上重要。
        *   **根拠:** 開始日 <= 終了日の論理的整合性が担保されていない。重篤な有害事象に関するデータの不整合は、安全性評価の信頼性に影響を与える。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2014-01-11'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2014-01-09'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 10
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 8
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 治験薬投与記録（EX）において、Visit 4およびVisit 12の後、次の投与期間の開始日（EXSTDTC）がVisit日（SVSTDTC）の翌日として記録されている。通常、Visitで薬剤が交付され同日または翌日から使用開始されるが、記録方法として適切か確認が必要。医学的評価への影響は小さいと考えられる。
        *   **根拠:** 投与記録とVisit日の間のわずかなずれ。曝露期間の計算に軽微な影響を与える可能性があるが、全体的な安全性・有効性評価への影響は限定的。
        *   **関連データ:**
            *   Visit 4: [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-01-16', [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-01-17' (for EXSEQ=2)
            *   Visit 12: [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-06-18', [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-06-19' (for EXSEQ=3)
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 同意取得日（DM.RFICDTC）が欠損している。同意取得は治験参加の根幹であり、日付の記録はGCP遵守と参加者の権利保護の観点から必須。
        *   **根拠:** GCP要件。同意取得の事実と日付の記録は監査証跡として重要。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 有害事象（AE）ドメインにおいて、MedDRAコーディングに関連する変数（AELLT, AELLTCD, AEDECOD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBDSYCD, AESOCCD）が全て欠損している。有害事象の標準化と比較可能性のため、コーディングは必須。安全性評価の質に影響する。
        *   **根拠:** データ標準化の要件。コーディングがないと集計やシグナル検出が困難。
        *   **関連データ:**
            *   AEドメイン全体でコーディング関連変数が欠損
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 併用薬（CM）ドメインにおいて、一部薬剤（TYLENOL, NEOSPORIN）の標準化薬剤名（CMDECOD）および薬剤分類（CMCLAS）が"UNCODED"となっている。また、複数の薬剤で適応症（CMINDC）が欠損している。データ品質の問題だが、主要な評価への影響は限定的と考えられる。
        *   **根拠:** データ標準化と完全性の観点。ただし、薬剤名自体は記録されており、医学的評価への影響は小さい。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TYLENOL', 'NEOSPORIN /USA/'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [Medication Class(CM.CMCLAS)] = 'UNCODED'
            *   [Indication(CM.CMINDC)] = '' (ASPIRIN, TYLENOL, HYDROCORTISONE, NEOSPORINで欠損)
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 既往歴（MH）ドメインにおいて、一部のVerbatim Termに対してMedDRAコーディング（MHLLT, MHDECOD, MHHLT, MHHLGT）が行われていない。データ品質の問題だが、主要な評価への影響は限定的と考えられる。
        *   **根拠:** データ標準化の観点。ただし、Verbatim Termは記録されており、医学的評価への影響は小さい。
        *   **関連データ:**
            *   MHドメインの一部でコーディング関連変数が欠損

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された適格性確認の一部がデータ上確認できない。具体的には、CNS imaging（INCL05）、Screening ECG（EXCL16）、Syphilis screening（EXCL29）の実施結果を示すデータが存在しない。適格性の完全な確認ができず、試験の質や参加者の安全性確保に影響する可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [5], 3.4.2.2 Exclusion Criteria [16b], [29b]
        *   **根拠:** プロトコルで規定された選択/除外基準の確認は、試験の科学的妥当性と参加者の安全性を担保するために必須。
        *   **関連データ:**
            *   関連する検査データ（例：EGドメイン、関連するLBドメインの検査項目）がJSONデータに含まれていない。
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening時の臨床検査値において、除外基準[27b]に抵触する可能性のある逸脱が認められる（AST高値、ALP低値）。プロトコルではLilly Reference Range IIIを超える場合に除外とされているが、このReference Range IIIが不明なため確定的な判断はできない。しかし、基準値逸脱があるため、適格性について疑義がある。不適格な患者が登録された場合、安全性リスクや試験結果の解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準違反の可能性。参加者の安全性とデータの信頼性に関わる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '40', [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 34, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (at Visit 1)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALP', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '34', [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 35, [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (at Visit 1)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 8（Week 8）およびVisit 10（Week 16）の実施日が、プロトコルで規定されたVisit Window（Visit 8: ±3日、Visit 10: ±4日）から大きく逸脱している（Visit 8: Day 63 (計画Day 56 +7日)、Visit 10: Day 126 (計画Day 112 +14日)）。評価スケジュールからの逸脱は、特に有効性評価（ADAS-Cog, CIBIC+, DAD）の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** 3.1 Summary of Study Design (Visit Window規定)
        *   **根拠:** プロトコルで規定された評価スケジュールの遵守は、データの比較可能性と信頼性の確保に重要。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 8, [Planned Study Day of Visit(SV.VISITDY)] = 56, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-03-05' (Day 63)
            *   [Visit Number(SV.VISITNUM)] = 10, [Planned Study Day of Visit(SV.VISITDY)] = 112, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-05-07' (Day 126)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されているECG、Ambulatory ECG、および薬物動態（PK）測定のデータが提供されたJSONデータに含まれていない。これらのデータが収集されていない場合、プロトコル違反となり、安全性評価（心血管系）およびPK評価が不可能となる。データが存在するが提供されていない可能性もある。
        *   **プロトコル該当箇所:** 3.9.2 Pharmacokinetics, 3.9.3.1 Safety Measures, 3.9.3.4.2 Cardiovascular Safety Measures
        *   **根拠:** プロトコルで規定された重要な評価の未実施またはデータ欠損は、安全性監視と試験目的の達成に影響する。
        *   **関連データ:**
            *   EGドメイン、PCドメインのデータがJSONデータに含まれていない。

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「DIARRHOEA」について、重篤（Serious Eventが「Y」）と報告されていますが、重篤と判断された具体的な理由（例：入院、生命を脅かす状態など）をお知らせください。また、報告された開始日（Start Date/Time of Adverse Eventが「2014-01-11」）が終了日（End Date/Time of Adverse Eventが「2014-01-09」）より後になっており矛盾しています。正確な開始日と終了日をご確認ください。これらの情報は、参加者の安全性評価の正確性を確保するために必要です。
        *   **クエリ文面（英語）:** Regarding the AE Term 'DIARRHOEA', it is reported as Serious (Serious Event = 'Y'). Please provide the specific reason for the seriousness assessment (e.g., hospitalization, life-threatening). Also, the reported Start Date (2014-01-11) is after the End Date (2014-01-09), which is inconsistent. Please confirm the correct start and end dates. This information is needed to ensure accurate safety assessment.
        *   **判断理由:** 重篤有害事象の評価根拠不明および日付矛盾は、安全性評価の正確性と信頼性に影響するため、医療機関での確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'DIARRHOEA', [Serious Event(AE.AESER)] = 'Y', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2014-01-11', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2014-01-09'
            *   関連するプロトコル箇所: 3.9.3.2.2 Serious Adverse Events
            *   関連する医学的知見: 重篤性の定義に基づく評価が必要。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DAD（Disability Assessment for Dementia）評価について、ベースラインから試験期間中を通じて全項目が「Yes」（機能障害なし）と記録されています。アルツハイマー病患者さんであることを考慮すると、ADL機能が完全に保たれている評価結果となっています。評価が適切に行われたか、評価手順や患者さんの状態について再確認をお願いします。この確認は、副次評価項目の信頼性を担保するために必要です。
        *   **クエリ文面（英語）:** Regarding the DAD (Disability Assessment for Dementia) assessment, all items are recorded as 'Yes' (no impairment) from baseline throughout the study. Considering the patient has Alzheimer's disease, this result indicating fully preserved ADL function seems unusual. Please re-confirm if the assessment was performed correctly and verify the patient's condition regarding ADLs. This is needed to ensure the reliability of this secondary endpoint.
        *   **判断理由:** 副次評価項目の結果が医学的に非典型的であり、評価の妥当性に疑義があるため、医療機関での確認が必要。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのQSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)' の全記録
            *   関連するプロトコル箇所: 3.9.1.1 Efficacy Measures (DAD)
            *   関連する医学的知見: アルツハイマー病におけるADL障害の一般的経過。
    *   **クエリNo.:** Q-3 (関連指摘No.: P-1, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者適格性について確認させてください。プロトコルで要求されているCNS imaging（Inclusion Criterion [5]）、Screening ECG（Exclusion Criterion [16b]）、Syphilis screening（Exclusion Criterion [29b]）の結果を示す記録が見当たりません。これらの検査が実施され、適格性が確認されたかをお知らせください。また、Screening時の臨床検査で、Aspartate Aminotransferaseが「40 U/L」（基準上限「34 U/L」）、Alkaline Phosphataseが「34 U/L」（基準下限「35 U/L」）と基準値を逸脱していますが、Exclusion Criterion [27b]に基づき適格と判断された根拠（例：臨床的に意義なしとの判断）について記録をご確認の上、お知らせください。適格性の確認は、参加者の安全確保と試験の質のために不可欠です。
        *   **クエリ文面（英語）:** Please confirm subject eligibility. Records for CNS imaging (Incl [5]), Screening ECG (Excl [16b]), and Syphilis screening (Excl [29b]) required by the protocol are missing. Were these performed and eligibility confirmed? Also, screening labs show AST=40 U/L (ULN=34) and ALP=34 U/L (LLN=35), deviating from the reference range. Please confirm the basis for eligibility per Excl [27b] (e.g., judged not clinically significant). Eligibility confirmation is crucial for subject safety and study quality.
        *   **判断理由:** 適格性確認に必要な情報が欠けており、基準逸脱の可能性もあるため、医療機関での確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='AST', LB.LBSTRESC='40', LB.LBSTNRHI=34 (Visit 1); LB.LBTESTCD='ALP', LB.LBSTRESC='34', LB.LBSTNRLO=35 (Visit 1). 関連検査データの欠損。
            *   関連するプロトコル箇所: 3.4.2.1 Inclusion Criteria [5], 3.4.2.2 Exclusion Criteria [16b], [27b], [29b]
    *   **クエリNo.:** Q-4 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 8（計画Study Day 56）がStudy Day 63に、Visit 10（計画Study Day 112）がStudy Day 126に実施されており、プロトコルで規定されたVisit Window（それぞれ±3日、±4日）から逸脱しています。逸脱理由をお知らせください。評価スケジュールの遵守は、データの信頼性確保のために重要です。
        *   **クエリ文面（英語）:** Visit 8 (planned Day 56) was conducted on Day 63, and Visit 10 (planned Day 112) was conducted on Day 126, deviating from the protocol-specified visit windows (±3 days and ±4 days, respectively). Please provide the reason for these deviations. Adherence to the assessment schedule is important for data reliability.
        *   **判断理由:** プロトコルからの逸脱であり、評価の信頼性に影響する可能性があるため、理由の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=8, SV.VISITDY=56, SV.SVSTDTC='2014-03-05' (Day 63); SV.VISITNUM=10, SV.VISITDY=112, SV.SVSTDTC='2014-05-07' (Day 126)
            *   関連するプロトコル箇所: 3.1 Summary of Study Design (Visit Window規定)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** EXドメインのEXSTDTCがVisit日の翌日になっている箇所（Visit 4後、Visit 12後）がある。データ入力規則や導出ロジックを確認し、必要であれば修正する。投与期間の計算への影響は軽微と判断。
        *   **判断理由:** データ入力/導出ルールの確認で解決可能であり、医学的評価への影響が小さいため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: EX.EXSTDTC, SV.SVSTDTC (Visit 4, 12)
    *   **確認事項No.:** I-2 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 同意取得日（DM.RFICDTC）が欠損している。他のソースドキュメント（例：同意説明文書の控え）から日付を特定し、データに反映させる必要がある。同意取得自体は行われている前提で内部確認とするが、特定できない場合は医療機関への問い合わせが必要となる。
        *   **判断理由:** GCP遵守に関わる重要な記録欠損だが、まずは内部での特定を試みる。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC
            *   関連するプロトコル箇所: 5.1 Informed Consent
    *   **確認事項No.:** I-3 (関連指摘No.: D-4, D-5, D-6)
        *   **重要度:** Major (AE), Minor (CM, MH)
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインのMedDRAコーディング、CMドメインの一部薬剤のWHODrugコーディングおよび適応症、MHドメインの一部既往歴のMedDRAコーディングが未実施または不完全。コーディング担当部署/プロセスを確認し、コーディングを完了させる。AEコーディングの欠落は安全性評価に影響するためMajor、CM/MHはデータ品質の問題としてMinor。
        *   **判断理由:** データ標準化と完全性の問題であり、内部のデータマネジメントプロセスで対応可能。
        *   **判断根拠:**
            *   関連するデータ: AE, CM, MHドメインのコーディング関連変数およびCMINDC
    *   **確認事項No.:** I-4 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** プロトコルで規定されているECG、Ambulatory ECG、PK測定データが提供されたSDTMデータセットに含まれていない。これらのデータが収集されたか、データ転送や変換プロセスに問題がなかったか、内部（データマネジメント、関連部署）で確認する。これらのデータ欠損は安全性・PK評価の信頼性に影響する。
        *   **判断理由:** 重要な評価データの欠損であり、まずは内部でデータ収集・処理状況を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: EGドメイン、PCドメインの欠損
            *   関連するプロトコル箇所: 3.9.2, 3.9.3.1, 3.9.3.4.2

---

# 01-701-1023のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
64歳、男性、人種はWHITE、民族名はHISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2006年3月11日発症、Primary Diagnosis）、胃食道逆流症、筋肉痛、食道裂孔ヘルニア、消化不良、頭痛、労作性呼吸困難、近視（Significant Pre-existing Condition）が報告されている。その他、足の蜂巣炎（2009年）、腰痛（2007年）、高血圧（2005年10月）、陰茎プロステーシス挿入（2006年4月）、上腕のしびれ（1982年）、虫垂炎（1956年）、肘骨折（1963年）、湿疹（2007年）、坐骨神経痛（2005年）、皮膚のかゆみ（2009年）、鼠径ヘルニア修復（1999年）、外傷による疼痛（2006年4月）、副鼻腔炎（1978年）、虫垂切除（1956年）の既往歴がある。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年07月22日|Day -14 (SCREENING 1)|Modified Hachinski Ischemic Score 評価実施 (個々の項目スコアから合計5点と算出され、選択基準<=4を満たさない可能性あり)。教育レベル 14年。体重 78.47 kg。身長 162.56 cm。体温 36.56 C。血圧 (臥位) 130/86 mmHg, (立位1分) 132/89 mmHg, (立位3分) 140/90 mmHg。脈拍 (臥位) 65 bpm, (立位1分) 78 bpm, (立位3分) 74 bpm。臨床検査実施 (主要な異常なし)。|
|2012年08月03日|Day -2 (SCREENING 2)|体温 36.56 C。血圧 (臥位) 131/77 mmHg, (立位1分) 129/79 mmHg, (立位3分) 138/85 mmHg。脈拍 (臥位) 79 bpm, (立位1分) 91 bpm, (立位3分) 92 bpm。|
|2012年08月05日|Day 1 (BASELINE)|治験薬 (Placebo) 投与開始。体重 80.29 kg。体温 36.28 C。血圧 (臥位) 130/84 mmHg, (立位1分) 132/86 mmHg, (立位3分) 132/88 mmHg。脈拍 (臥位) 68 bpm, (立位1分) 80 bpm, (立位3分) 76 bpm。ADAS-Cog(11) Total Score: 13。NPI-X Total Score: 11。DAD 評価実施。|
|2012年08月07日|Day 3 (N/A)|有害事象「ERYTHEMA」(紅斑) (Mild) 発現 (AESEQ=1, 4)。有害事象「ERYTHEMA」(紅斑) (Moderate) 発現 (AESEQ=2)。(治験薬との関連: Probable)|
|2012年08月26日|Day 22 (AMBUL ECG PLACEMENT)|有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」(第二度房室ブロック) (Mild) 発現 (AESEQ=3)。(治験薬との関連: Possible)。体温 36.44 C。血圧 (臥位) 133/82 mmHg, (立位1分) 130/88 mmHg, (立位3分) 138/89 mmHg。脈拍 (臥位) 71 bpm, (立位1分) 79 bpm, (立位3分) 77 bpm。|
|2012年08月27日|Day 23 (WEEK 2)|体重 80.74 kg。体温 36.94 C。血圧 (臥位) 122/88 mmHg, (立位1分) 130/86 mmHg, (立位3分) 138/90 mmHg。脈拍 (臥位) 84 bpm, (立位1分) 92 bpm, (立位3分) 94 bpm。臨床検査実施 (主要な異常なし)。NPI-X Total Score: 10。|
|2012年08月30日|Day 26 (N/A)|有害事象「ERYTHEMA」(紅斑) (Mild) 回復/解消 (AESEQ=1, 4)。|
|2012年09月01日|Day 28 (N/A)|治験薬 (Placebo) 投与終了。|
|2012年09月02日|Day 29 (WEEK 4)|有害事象 (ERYTHEMA, AESEQ=2) により治験中止。体重 80.29 kg。体温 36.22 C。血圧 (臥位) 130/86 mmHg, (立位1分) 134/88 mmHg, (立位3分) 136/92 mmHg。脈拍 (臥位) 64 bpm, (立位1分) 76 bpm, (立位3分) 70 bpm。臨床検査実施 (主要な異常なし)。ADAS-Cog(11) Total Score: 8。CIBIC+: 3 (Minimal improvement)。NPI-X Total Score: 11。DAD 評価実施。|
|2013年02月18日|Day 198 (RETRIEVAL)|Retrieval Visit 実施。血圧 (臥位) 125/89 mmHg, (立位1分) 110/86 mmHg, (立位3分) 130/84 mmHg。脈拍 (臥位) 72 bpm, (立位1分) 84 bpm, (立位3分) 76 bpm。体温 36.56 C。ADAS-Cog(11) Total Score: 12。CIBIC+: 5 (Minimal worsening)。NPI-X Total Score: 5。DAD 評価実施 (ベースラインと比較し複数の項目で悪化)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 22に有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」(第二度房室ブロック) (Mild) が報告されている。本剤 (Xanomeline) はコリン作動薬であり心伝導系への影響が懸念される薬剤クラスであるため、Placebo群であっても心血管系の安全性評価は重要である。発現時の詳細な心電図所見、関連症状の有無、実施された処置、および治験中止判断への関与について確認が必要。プロトコル 3.9.4 では心血管系の安全性モニタリングが強調されている。
        *   **根拠:** 一般的な医学知識（コリン作動薬の心血管系への影響）、プロトコル 3.9.4 (Safety Monitoring)。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ATRIOVENTRICULAR BLOCK SECOND DEGREE'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-08-26'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 22
            *   [Causality(AE.AEREL)] = 'POSSIBLE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有効性評価の結果に一貫性が見られない。特に、Retrieval Visit (Day 198) において、NPI-X Total Score (NPTOT) はベースライン (Day 1) や Week 4 (Day 29) と比較して改善 (11→5) しているのに対し、ADAS-Cog(11) Total Score (ACTOT) は悪化 (Baseline 13, Week 4 8, Retrieval 12)、CIBIC+ も悪化 (Week 4: 3, Retrieval: 5)、DAD も複数の項目で悪化している。Placebo群での変動の可能性もあるが、NPI-X評価の妥当性やデータ品質について確認が必要。評価の信頼性に影響を与える可能性がある。
        *   **根拠:** 有効性評価指標間の結果の矛盾、一般的な疾患進行パターンとの比較。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 11
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 4, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 10
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 11
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 201, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 5
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 13
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 8
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 201, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 12
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 5, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 3
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 201, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 5
            *   DAD データ (QSドメイン、Visit 3, 5, 201)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) が欠損している。GCP遵守および参加者の権利保護の観点から、同意が適切に取得されていることの確認は必須である。
        *   **根拠:** GCP原則、プロトコル 5.1 (Informed Consent)。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** AE, CM, MH ドメインにおいて、MedDRA および WHODrug コーディングが不完全または欠損しているレコードが多数存在する (例: AE.AELLT, AE.AEDECOD, CM.CMDECOD='UNCODED', MH.MHDECOD='' など)。これはデータの標準化と品質に問題があり、安全性シグナルの検出や集計・解析に影響を与える可能性がある。
        *   **根拠:** データ標準化の要件 (SDTM)、データ品質管理。
        *   **関連データ:**
            *   AEドメインの AELLT, AEDECOD など
            *   CMドメインの CMDECOD, CMCLAS など
            *   MHドメインの MHLLT, MHDECOD など
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 有害事象「ERYTHEMA」(紅斑) について、AESEQ=1 と AESEQ=4 のレコードが、開始日、終了日、重症度 (Mild) が同一であり、重複記録の可能性がある。データクリーニングが必要。
        *   **根拠:** データの一貫性。
        *   **関連データ:**
            *   [Sequence Number(AE.AESEQ)] = 1, [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Severity/Intensity(AE.AESEV)] = 'MILD', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-08-07', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-08-30'
            *   [Sequence Number(AE.AESEQ)] = 4, [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Severity/Intensity(AE.AESEV)] = 'MILD', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-08-07', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-08-30'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** Modified Hachinski Ischemic Scale score が 5点 (MHITM07=1, MHITM10=2, MHITM12=2) と算出され、プロトコルで規定された選択基準 [4] (<= 4) を満たしていない可能性がある。これは参加者の適格性に関する重要な逸脱であり、試験結果の解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [4], Attachment LZZT.8 Hachinski Ischemic Scale
        *   **根拠:** QSデータに基づくスコア計算結果とプロトコル規定の比較。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'MHITM07', [Character Result/Finding in Std Format(QS.QSSTRESC)] = '1'
            *   [Question Short Name(QS.QSTESTCD)] = 'MHITM10', [Character Result/Finding in Std Format(QS.QSSTRESC)] = '2'
            *   [Question Short Name(QS.QSTESTCD)] = 'MHITM12', [Character Result/Finding in Std Format(QS.QSSTRESC)] = '2'
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 4 (Week 2) および Visit 3.5 (AMBUL ECG PLACEMENT) の実施日が、予定された Study Day (それぞれ Day 14, Day 13) から大幅に遅延している (それぞれ Day 23, Day 22 で実施、+9日)。プロトコル 3.1 で規定された Visit Window (+/- 3 days) を逸脱している。評価タイミングのずれは、特に PK 評価や安全性評価 (AE発現との前後関係など) の解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit Window), Attachment LZZT.1 Schedule of Events
        *   **根拠:** SVデータと TVデータ (Planned Study Day) の比較。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 4, [Planned Study Day of Visit(TV.VISITDY)] = 14, [Start Date/Time of Visit(SV.SVSTDTC)] = '2012-08-27' (Day 23)
            *   [Visit Number(SV.VISITNUM)] = 3.5, [Planned Study Day of Visit(TV.VISITDY)] = 13, [Start Date/Time of Visit(SV.SVSTDTC)] = '2012-08-26' (Day 22)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択/除外基準の判定に必要なデータの一部が欠損している (MMSEスコア、CNSイメージング結果、梅毒スクリーニング結果、葉酸値、スクリーニングECG所見)。これらの情報がないと、被験者が適格基準を完全に満たしていたかを確認できない。特に Hachinski スコアが基準値を超えている可能性 (P-1) や、後に AVB II が発現していることを考慮すると、スクリーニング時の評価が適切に行われたかの確認は重要。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria, Section 3.4.2.2 Exclusion Criteria
        *   **根拠:** プロトコルで要求される評価項目と提供データの比較。
        *   **関連データ:**
            *   QSドメイン (MMSEデータなし)
            *   LBドメイン (Folateデータなし)
            *   (ECG, イメージングデータは提供されていない)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) が記録されていない。プロトコル 5.1 および GCP に従い、治験関連手順開始前に同意が取得されている必要がある。同意取得の確認ができない場合、重大なGCP逸脱となる。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** GCP原則、プロトコル規定と提供データの比較。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時のModified Hachinski Ischemic Scoreについて、記録された個々の項目スコア（Somatic complaints=1, History of strokes=2, Focal neurological symptoms=2）から合計スコアが5点と算出されます。プロトコルでは選択基準としてスコアが4点以下と規定されていますが、本被験者の適格性について再確認をお願いします。
        *   **クエリ文面（英語）:** Regarding the Modified Hachinski Ischemic Score at screening, the calculated total score is 5 based on the recorded item scores (Somatic complaints=1, History of strokes=2, Focal neurological symptoms=2). The protocol inclusion criterion requires a score <=4. Please re-confirm the subject's eligibility.
        *   **判断理由:** 除外基準に抵触する可能性があり、被験者の適格性とデータの信頼性を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD = 'MHITM07', 'MHITM10', 'MHITM12' の QS.QSSTRESN 値
            *   関連するプロトコル箇所: Section 3.4.2.1 [4]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 22に有害事象「第二度房室ブロック」(重症度: Mild) が報告されています。発現時の詳細な心電図所見（例：Mobitz I型/II型、ブロック部位など）、関連する臨床症状（めまい、失神前兆など）の有無、実施された処置、および治験中止の判断への関与について、詳細な情報をご提供ください。
        *   **クエリ文面（英語）:** AE 'ATRIOVENTRICULAR BLOCK SECOND DEGREE' (Severity: Mild) was reported on Study Day 22. Please provide detailed information on ECG findings (e.g., Mobitz type I/II, block location), associated clinical symptoms (e.g., dizziness, presyncope), actions taken, and its contribution to the decision for study discontinuation.
        *   **判断理由:** Placebo群ではあるが心伝導障害であり、臨床的意義と安全性の評価、中止理由の明確化のために詳細情報が必要なため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=3) レコード
            *   関連するプロトコル箇所: Section 3.9.4 (Safety Monitoring)
            *   関連する医学的知見: AVブロックの臨床的意義、コリン作動薬の潜在的影響
    *   **クエリNo.:** Q-3 (関連指摘No.: D-1, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日 ([Date/Time of Informed Consent(DM.RFICDTC)]) が記録されていません。治験実施計画書およびGCPに従い、治験関連手順開始前に同意が取得されている必要があります。同意説明文書の署名日を確認し、正しい日付をご報告ください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (DM.RFICDTC) is missing. As per protocol and GCP, informed consent must be obtained before any study-related procedures. Please confirm the date the informed consent form was signed and provide the correct date.
        *   **判断理由:** GCP遵守および参加者の権利保護の確認に必須の情報であるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC = ''
            *   関連するプロトコル箇所: Section 5.1
    *   **クエリNo.:** Q-4 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 4 (Week 2) の実施日 (Study Day 23) および Visit 3.5 (AMBUL ECG PLACEMENT) の実施日 (Study Day 22) が、それぞれ予定日 (Day 14, Day 13) より9日遅れています。プロトコル規定の Visit Window (+/- 3日) を逸脱していますが、遅延理由と、評価結果（特にPK、安全性評価）への影響についてご説明ください。
        *   **クエリ文面（英語）:** Visit 4 (Week 2) on Study Day 23 and Visit 3.5 (AMBUL ECG PLACEMENT) on Study Day 22 were performed 9 days later than planned (Day 14 and Day 13, respectively), exceeding the protocol visit window (+/- 3 days). Please explain the reason for the delay and assess its potential impact on study assessments (esp. PK, safety).
        *   **判断理由:** プロトコルからの逸脱であり、評価タイミングのずれがデータ解釈に影響を与える可能性があるため。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=4, SV.SVSTDTC='2012-08-27'; SV.VISITNUM=3.5, SV.SVSTDTC='2012-08-26'; TV.VISITNUM=4, TV.VISITDY=14; TV.VISITNUM=3.5, TV.VISITDY=13
            *   関連するプロトコル箇所: Section 3.1
    *   **クエリNo.:** Q-5 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Retrieval Visit (Study Day 198) におけるNPI-X Total Score (5点) は、ベースライン (11点) やWeek 4 (11点) と比較して改善を示していますが、同VisitでのADAS-Cog(11) Total Score (12点) やCIBIC+ (5点: Minimal worsening) は悪化傾向を示しています。このNPI-X評価結果の妥当性について、評価時の状況等を踏まえてご確認ください。
        *   **クエリ文面（英語）:** At the Retrieval Visit (Study Day 198), the NPI-X Total Score (5) shows improvement compared to Baseline (11) and Week 4 (11). However, ADAS-Cog(11) Total Score (12) and CIBIC+ (5: Minimal worsening) at the same visit indicate deterioration. Please confirm the validity of the NPI-X assessment considering the circumstances at the time of evaluation.
        *   **判断理由:** 有効性評価指標間で結果に矛盾があり、評価の信頼性を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: QS (NPTOT, ACTOT, CIBIC) at Visit 3, 5, 201
            *   関連するプロトコル箇所: Section 2.1, 2.2 (Objectives)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「ERYTHEMA」(紅斑) について、AESEQ=1 と AESEQ=4 のレコードが重複している可能性が高い。開始日、終了日、重症度が同一。データクリーニングプロセスで確認し、必要であれば一方を削除する。医学的評価への影響は小さいと判断。
        *   **判断理由:** 明らかな重複記録の可能性が高く、内部でのデータクリーニングで対応可能と判断されるため。
        *   **判断根拠:**
            *   関連するデータ: AE (AESEQ=1, 4) レコード
    *   **確認事項No.:** I-2 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE, CM, MH ドメインにおける MedDRA/WHODrug コーディングの不備（欠損、UNCODED）。コーディング担当部署に連絡し、再コーディングまたは修正を依頼する。解析や安全性評価の正確性のために対応が必要。
        *   **判断理由:** データ標準化と品質に関わる問題であり、内部プロセスで対応すべき事項のため。
        *   **判断根拠:**
            *   関連するデータ: AE, CM, MH ドメインのコーディング関連変数
    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 選択/除外基準判定に必要なデータ（MMSEスコア、CNSイメージング結果、梅毒スクリーニング結果、葉酸値、スクリーニングECG所見）の一部が SDTM データセットに欠損している。これらのデータがソースドキュメントや他のシステムに存在するか確認する。特に Hachinski スコアの基準値超過の可能性 (P-1) と併せて、適格性確認プロセスが適切であったか内部でレビューする。
        *   **判断理由:** 被験者の適格性に関わる重要な情報であり、データ欠損の理由と適格性確認プロセスの妥当性を内部で確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: DM, QS, LB ドメインの欠損情報
            *   関連するプロトコル箇所: Section 3.4.2.1, 3.4.2.2

---

# 01-701-1028のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
71歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、計画された治療群および実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2009年12月16日発症、PRIMARY DIAGNOSIS）、脂肪腫（LIPOMA, SIGNIFICANT PRE-EXISTING CONDITION, MODERATE）、老視（PRESBYOPIA, SIGNIFICANT PRE-EXISTING CONDITION, MILD）、脂肪腫切除術（LIPECTOMY, HISTORICAL DIAGNOSIS, 1981年）、関節炎（ARTHRITIS, SIGNIFICANT PRE-EXISTING CONDITION, MODERATE）、虫垂切除術（APPENDECTOMY, HISTORICAL DIAGNOSIS, 1968年）が報告されている。教育レベル（EDUCATION LEVEL）は16年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年07月01日|Day -17 (N/A)|有害事象「PARKINSON'S DISEASE」(MILD, POSSIBLE, NOT RECOVERED/NOT RESOLVED) 発現 (治験薬開始前)|
|2013年07月11日|Day -8 (SCREENING 1)|赤血球平均ヘモグロビン量(MCH) = 37 pg (HIGH, 基準範囲 26-34)。赤血球平均容積(MCV) = 104 fL (HIGH, 基準範囲 80-100)。脈拍 54-59 bpm (やや低め)。|
|2013年07月19日|Day 1 (BASELINE)|治験薬 (Xanomeline 54 mg QD) 投与開始。ADAS-Cog(11) Subscore = 3。NPI-X (9) Total Score = 0。DAD Total Score = 40/40 (100%)。|
|2013年08月01日|Day 14 (WEEK 2)|NPI-X (9) Total Score = 0。|
|2013年08月02日|Day 15 (N/A)|治験薬投与量が 81 mg QD に変更。|
|2013年08月08日|Day 21 (N/A)|有害事象「APPLICATION SITE PRURITUS」(MILD, PROBABLE, NOT RECOVERED/NOT RESOLVED) 発現。併用薬「HYDROCORTISONE」(Topical, PRN) 使用開始。|
|2013年08月14日|Day 27 (WEEK 4)|MCH = 35 pg (HIGH)。MCV = 101 fL (HIGH)。NPI-X (9) Total Score = 0。|
|2013年08月29日|Day 42 (WEEK 6)|MCV = 101 fL (HIGH)。脈拍 56-62 bpm (やや低め)。NPI-X (9) Total Score = 0。|
|2013年09月10日|Day 54 (WEEK 8)|クレアチンキナーゼ(CK) = 317 U/L (HIGH, 基準範囲 22-198)。MCH = 35 pg (HIGH)。ADAS-Cog(11) Subscore = 2。CIBIC+ = 4 (No Change)。DAD Total Score = 40/40 (100%)。NPI-X (9) Total Score = 0。|
|2013年09月24日|Day 68 (WEEK 10 (T))|NPI-X (9) Total Score = 0。|
|2013年10月09日|Day 83 (WEEK 12)|MCV = 103 fL (HIGH)。NPI-X (9) Total Score = 0。|
|2013年10月23日|Day 97 (WEEK 14 (T))|NPI-X (9) Total Score = 0。|
|2013年11月06日|Day 111 (WEEK 16)|カルシウム(CA) = 8.0 mg/dL (LOW, 基準範囲 8.4-10.3)。アニソサイトーシス(ANISO) = 1 (ABNORMAL)。MCH = 35 pg (HIGH)。MCV = 102 fL (HIGH)。ADAS-Cog(11) Subscore = 4。CIBIC+ = 4 (No Change)。DAD Total Score = 39/40 (97.5%) (DAITM06=0)。NPI-X (9) Total Score = 0。|
|2013年11月20日|Day 125 (WEEK 18 (T))|NPI-X (9) Total Score = 0。|
|2013年12月04日|Day 139 (WEEK 20)|アニソサイトーシス(ANISO) = 1 (ABNORMAL)。MCH = 35 pg (HIGH)。NPI-X (9) Total Score = 0。|
|2013年12月18日|Day 153 (WEEK 22 (T))|NPI-X (9) Total Score = 0。|
|2014年01月06日|Day 172 (WEEK 24)|マクロサイトーシス(MACROCY) = 1 (ABNORMAL)。多染性赤血球(POLYCHR) = 1 (ABNORMAL)。MCV = 104 fL (HIGH)。ADAS-Cog(11) Subscore = 3。CIBIC+ = 4 (No Change)。DAD Total Score = 40/40 (100%)。NPI-X (9) Total Score = 0。|
|2014年01月07日|Day 173 (N/A)|治験薬投与量が 54 mg QD に変更。|
|2014年01月14日|Day 180 (WEEK 26)|マクロサイトーシス(MACROCY) = 1 (ABNORMAL)。MCH = 35 pg (HIGH)。MCV = 106 fL (HIGH)。脈拍 53-59 bpm (やや低め)。NPI-X (9) Total Score = 0。治験薬投与終了。Disposition: COMPLETED (プロトコル完了)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 治験薬投与開始前 (Day -17) に有害事象「PARKINSON'S DISEASE」(MILD, POSSIBLE) が報告されている。MHドメインにはパーキンソン病の記載がない。スクリーニング時の神経学的評価との整合性や、除外基準[12] (Diagnosis of serious neurological conditions) に抵触する可能性について確認が必要。患者の適格性評価の妥当性に疑義が生じる。
        *   **根拠:** 治験薬開始前の有害事象報告であり、患者のベースライン状態および適格性評価に影響する可能性がある。パーキンソン病はプロトコル除外基準に明記されている。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PARKINSON''S DISEASE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-07-01'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = -17
            *   [Causality(AE.AEREL)] = 'POSSIBLE'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Reported Term for the Medical History(MH.MHTERM)] にパーキンソン病の記載なし
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** ベースライン時から一貫して赤血球恒数（MCH, MCV）が高値を示しており、試験後半には形態異常（ANISO, MACROCY, POLYCHR）も出現している。これは大球性貧血を示唆する所見であり、臨床的な評価（原因検索、関連症状の有無）および治験薬との関連性評価が必要。患者の安全性に関わる可能性がある。
        *   **根拠:** 持続的かつ進行性の可能性のある検査値異常であり、貧血は患者のQOLや安全性に影響しうる。原因によっては治療介入が必要となる場合がある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCH', 'MCV', 'ANISO', 'MACROCY', 'POLYCHR'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' または 'ABNORMAL' (複数時点)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 185.9256 (Day -8, 基準範囲下限に近い)
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Day 54にクレアチンキナーゼ(CK)の一過性高値 (317 U/L, 基準範囲 22-198) が認められた。関連する有害事象（筋肉痛など）の報告はなく、その後の測定値は正常範囲内であるため臨床的意義は低い可能性があるが、記録として残す。
        *   **根拠:** 一過性の検査値異常であり、関連症状や持続性がないため、現時点でのリスクは低いと判断される。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 317 (Day 54)
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Day 111にカルシウム(CA)の一過性低値 (8.0 mg/dL, 基準範囲 8.4-10.3) が認められた。関連する有害事象の報告はなく、その後の測定値は正常範囲内であるため臨床的意義は低い可能性があるが、記録として残す。
        *   **根拠:** 一過性の軽微な基準値下限割れであり、関連症状や持続性がないため、現時点でのリスクは低いと判断される。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CA'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1.996 (Day 111, mmol/L換算値)
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** ベースラインおよび試験期間中、脈拍数が時折50 bpm台と低め（徐脈傾向）である。プロトコル除外基準[16b] (Bradycardia d50 beats per minute) には抵触していないが、Xanomelineはムスカリン作動薬であり徐脈のリスクがあるため、治験薬との関連も含め注意が必要。
        *   **根拠:** 治験薬の薬理作用と関連しうる所見であり、安全性モニタリング上、注意喚起が必要。ただし、基準値逸脱や症状報告はないため重要度はMinorとした。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 54 (Day -8), 56 (Day 42), 53 (Day 180) など
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** 主要評価項目 (ADAS-Cog(11), CIBIC+) および副次評価項目 (NPI-X, DAD) において、ベースラインから試験終了まで臨床的に意味のある改善が認められない。Xanomeline High Dose群の症例として、期待される有効性が示されていない可能性がある。
        *   **根拠:** 試験の目的（有効性評価）に関連する所見だが、個々の症例の結果であり、試験全体の評価が必要。
        *   **関連データ:**
            *   QSドメインのACTOT, CIBIC, NPTOT, DAITM** の各データ

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「PARKINSON'S DISEASE」は治験薬開始前 (Day -17) に発現しているが、SUPPAEドメインで治療期間発現フラグ（AETRTEM）が 'Y' となっている。これは通常、治験薬投与開始後に発現または悪化した事象に付与されるフラグであり、データの導出ロジックに誤りがある可能性がある。医学的評価への直接的な影響は小さいが、データ品質の問題として指摘する。
        *   **根拠:** データ導出ロジックの誤りは、他の症例や解析結果にも影響を与える可能性がある。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PARKINSON''S DISEASE'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = -17
            *   [Related Domain Abbreviation(SUPPAE.RDOMAIN)] = 'AE'
            *   [Identifying Variable(SUPPAE.IDVAR)] = 'AESEQ'
            *   [Identifying Variable Value(SUPPAE.IDVARVAL)] = '1'
            *   [Qualifier Variable Name(SUPPAE.QNAM)] = 'AETRTEM'
            *   [Data Value(SUPPAE.QVAL)] = 'Y'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 同意取得日（DM.RFICDTC）が欠損している。治験参加者の権利保護の観点から、治験手順開始前に適切に同意が取得されたことの確認は極めて重要であり、この日付の欠損は重大な記録不備である。
        *   **根拠:** GCPの基本原則およびプロトコル 5.1 に基づき、同意取得の記録は必須。欠損している場合、同意プロセスが適切に行われたか確認できない。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 報告されている2つの有害事象（PARKINSON'S DISEASE, APPLICATION SITE PRURITUS）について、終了日（AE.AEENDTC, AE.AEENDY）が記録されていない。転帰が「NOT RECOVERED/NOT RESOLVED」であるため試験終了まで継続したと推測されるが、データの完全性の観点からは終了日の記録が望ましい。
        *   **根拠:** データの完全性に関する指摘。転帰情報から状況は推測可能であり、医学的評価への影響は限定的。
        *   **関連データ:**
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '' (欠損)
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = null (欠損)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** スクリーニング時の葉酸（Folate）の検査データが欠損している。プロトコル除外基準[28b]では葉酸およびビタミンB12の基準範囲からの逸脱を除外項目としており、適格性評価のために必要なデータであった可能性がある。ただし、他のデータから除外基準違反が強く示唆されるわけではないため、影響は限定的と判断。
        *   **根拠:** 適格性評価に必要な可能性のあるデータの欠損。
        *   **関連データ:**
            *   LBドメインに Folate のレコードなし

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 選択基準[5]で要求されている CNS imaging の実施記録および結果がデータから確認できない。適格性確認が適切に行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 選択基準の遵守を確認するためのデータが不足している。
        *   **関連データ:** 関連データなし (記録の欠如)
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **逸脱の可能性:** 治験薬開始前に有害事象「PARKINSON'S DISEASE」が報告されている。これがスクリーニング時に診断されていた場合、除外基準[12]「Diagnosis of serious neurological conditions」の「Parkinson’s disease」に明確に違反する。患者の安全性および試験データの妥当性に重大な影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [12]
        *   **根拠:** 除外基準に該当する可能性のある状態での治験参加は、GCP違反であり、患者の安全性リスクを高め、データの解釈を困難にする。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PARKINSON''S DISEASE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-07-01'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = -17
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の赤血球恒数（MCH, MCV）が高値であった。これが除外基準[27b]「Laboratory test values exceeding the Lilly Reference Range III」に該当すると判断された場合、逸脱となる可能性がある。ただし、臨床的に重要でないと判断されれば逸脱とはならない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準に関連する検査値異常。ただし、臨床的意義の判断が必要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCH', 'MCV'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (Day -8)
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の甲状腺機能検査の一部（T3 Uptake, T4, Free Thyroid Index）のデータが欠損している。除外基準[28b]の評価が完全に行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準の評価に必要なデータの一部欠損。
        *   **関連データ:** LBドメインに関連データなし
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の梅毒検査（Syphilis screening）の実施記録および結果がデータから確認できない。除外基準[29b]の評価が適切に行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 除外基準の評価に必要なデータが不足している。
        *   **関連データ:** 関連データなし (記録の欠如)
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験薬投与量が Day 173 から 81mg から 54mg に変更されている。プロトコル 3.10.1 では早期中止時の漸減投与について記載があるが、プロトコル完了時の漸減投与については明記されていない。この投与量変更がプロトコルで規定されていない場合、逸脱となる可能性がある。投与量変更の根拠が不明確。
        *   **プロトコル該当箇所:** Section 3.6.2 (TTS Administration Procedures), Section 3.10.1 (Discontinuations)
        *   **根拠:** プロトコルに明記されていない投与量変更が行われた可能性がある。
        *   **関連データ:**
            *   [Sequence Number(EX.EXSEQ)] = 2, [Dose per Administration(EX.EXDOSE)] = 81, [End Date/Time of Treatment(EX.EXENDTC)] = '2014-01-06' (Day 172)
            *   [Sequence Number(EX.EXSEQ)] = 3, [Dose per Administration(EX.EXDOSE)] = 54, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-01-07' (Day 173)
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された Visit (Visits 1, 4, 5, 7, 8, 9, 10, 11, 12, 13) での ECG 実施記録がデータから確認できない。安全性評価がプロトコル通りに実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.1 (Safety Measures), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルで要求される安全性評価の実施記録がない。
        *   **関連データ:** 関連データなし (記録の欠如)
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された Visit 2 での Ambulatory ECG の実施記録がデータから確認できない。ベースラインの心血管安全性評価がプロトコル通りに実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 (Cardiovascular Safety Measures), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルで要求される安全性評価の実施記録がない。
        *   **関連データ:** 関連データなし (記録の欠如)
    *   **指摘No.:** P-9
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルで規定された Visit (Visits 3, 4, 5, 7, 9, 11) での薬物動態（PK）採血の実施記録がデータから確認できない。PK評価がプロトコル通りに実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.2 (Pharmacokinetics), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルで要求される評価の実施記録がない。
        *   **関連データ:** 関連データなし (記録の欠如)
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日（DM.RFICDTC）が欠損しており、治験手順開始前に適切に同意が取得されたことを確認できない。GCP違反の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** GCPの基本要件である同意取得プロセスの記録不備。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-2)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象名「PARKINSON'S DISEASE」が治験薬投与開始前の2013年7月1日に発現したと報告されています。この状態はスクリーニング時に診断されていたのでしょうか？ プロトコル除外基準[12]（重篤な神経疾患：パーキンソン病）との関連について評価をお願いします。また、この情報が既往歴（MH）ドメインに記載されていない理由についてもご確認ください。患者様の適格性と安全性に関わる重要な確認事項です。
        *   **クエリ文面（英語）:** Regarding the AE 'PARKINSON'S DISEASE' reported with AESTDTC='2013-07-01' (before study treatment start), was this condition diagnosed at screening? Please assess its relation to exclusion criterion [12] (Parkinson's disease). Also clarify why it's not in MH. This is crucial for eligibility and safety.
        *   **判断理由:** 除外基準に該当する可能性のある有害事象が治験薬開始前に報告されており、患者の適格性と安全性に重大な懸念があるため、緊急の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'PARKINSON''S DISEASE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-07-01', [Study Day of Start of Adverse Event(AE.AESTDY)] = -17
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [12]
            *   関連する医学的知見: パーキンソン病は進行性の神経変性疾患であり、治験参加の適格性に影響する。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, P-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** ベースライン時から一貫して赤血球平均ヘモグロビン量(MCH)および赤血球平均容積(MCV)が高値であり、試験後半には赤血球大小不同(Anisocytes)、大赤血球症(Macrocytes)、多染性(Polychromasia)も報告されています。大球性貧血が疑われますが、本件に関する臨床的な評価（原因検索、関連症状の有無など）と、治験薬との関連性についての医師の評価をご教示ください。
        *   **クエリ文面（英語）:** Lab results consistently show high MCH and MCV from baseline, with morphology changes (Anisocytes, Macrocytes, Polychromasia) later in the study, suggesting macrocytic anemia. Please provide clinical assessment (cause investigation, related symptoms) and physician's evaluation of relationship to study drug.
        *   **判断理由:** 持続的な検査値異常であり、患者の安全性評価のために原因検索と治験薬との関連評価が必要。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCH', 'MCV', 'ANISO', 'MACROCY', 'POLYCHR', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' or 'ABNORMAL' (複数時点)
            *   関連するプロトコル箇所: Section 3.9.3.3 (Clinical Laboratory Tests)
            *   関連する医学的知見: 大球性貧血の原因は多岐にわたり、適切な評価が必要。
    *   **クエリNo.:** Q-3 (関連指摘No.: D-2, P-10)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日（Date/Time of Informed Consent）が記録されていません。治験関連手順が開始される前に、患者様（または代諾者様）から適切にインフォームド・コンセントが取得されていたことを確認し、同意取得年月日をご提供ください。参加者の権利保護に関する重要な記録です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (RFICDTC) is missing. Please confirm that informed consent was properly obtained from the subject (or legally acceptable representative) prior to initiation of any study-related procedures and provide the date of consent. This is critical for participant rights protection.
        *   **判断理由:** 同意取得の記録はGCP上必須であり、参加者の権利保護を確認するために不可欠。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
            *   関連する医学的知見: GCP要件
    *   **クエリNo.:** Q-4 (関連指摘No.: P-7, P-8)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルでは、複数のVisitでECG検査、Visit 2で24時間ホルター心電図（Ambulatory ECG）の実施が規定されていますが、これらの検査の実施記録が確認できません。各規定Visitにて適切に実施されていたかご確認ください。心血管系の安全性評価に関する重要な確認事項です。
        *   **クエリ文面（英語）:** Protocol requires ECGs at multiple visits and a 24-hour Ambulatory ECG at Visit 2. Records confirming completion of these procedures are missing. Please confirm if these cardiovascular safety assessments were performed as scheduled per protocol.
        *   **判断理由:** プロトコルで規定された重要な安全性評価の実施状況を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: ECG, Ambulatory ECG のデータなし
            *   関連するプロトコル箇所: Section 3.9.3.4.2, Attachment LZZT.1
            *   関連する医学的知見: 心血管安全性評価の重要性
    *   **クエリNo.:** Q-5 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 治験薬投与記録（Exposure）について、Study Day 173 から投与量が 81mg から 54mg に変更されています。プロトコル完了に伴う計画的な減量でしょうか、あるいは他の理由による変更でしょうか？投与量変更の理由と、その指示についてご確認ください。
        *   **クエリ文面（英語）:** Regarding Exposure (EX), the dose was changed from 81mg to 54mg on Study Day 173. Was this a planned dose reduction for study completion, or due to another reason? Please clarify the reason for this dose change and confirm the instruction given.
        *   **判断理由:** プロトコルに明記されていない投与量変更の理由を確認し、プロトコル遵守状況を明確にする必要がある。
        *   **判断根拠:**
            *   関連するデータ: EXドメインの投与量変更記録
            *   関連するプロトコル箇所: Section 3.6.2, 3.10.1
    *   **クエリNo.:** Q-6 (関連指摘No.: P-1, P-4, P-5)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時に実施が必要とされている CNS imaging (選択基準[5])、甲状腺機能検査の一部 (除外基準[28b])、梅毒検査 (除外基準[29b]) の実施記録または結果が確認できません。これらの検査が実施され、患者様の適格性が適切に評価されたかご確認ください。
        *   **クエリ文面（英語）:** Records or results for screening CNS imaging (Inclusion [5]), some Thyroid function tests (Exclusion [28b]), and Syphilis screening (Exclusion [29b]) are missing. Please confirm if these tests were performed and subject eligibility was appropriately assessed.
        *   **判断理由:** 適格性評価に必要な検査の実施状況を確認するため。他のデータから不適格が強く示唆されるわけではないためMinorとした。
        *   **判断根拠:**
            *   関連するデータ: 関連データなし (記録の欠如)
            *   関連するプロトコル箇所: Section 3.4.2.1 [5], 3.4.2.2 [28b], [29b]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 治験薬開始前のAE「PARKINSON'S DISEASE」に対し、SUPPAE.AETRTEM が 'Y' となっている。これは導出ロジックのエラーの可能性が高い。AETRTEM の導出仕様を確認し、必要に応じて修正する。医学的評価への影響は小さいと判断。
        *   **判断理由:** データ導出ロジックの問題であり、内部での確認・修正が可能。
        *   **判断根拠:**
            *   関連するデータ: AE.AESTDY = -17, SUPPAE.QNAM = 'AETRTEM', SUPPAE.QVAL = 'Y'
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 54 の一過性 CK 高値 (317 U/L) を確認。関連 AE 報告なく、その後正常化しているため、現時点での追加アクションは不要と判断。ただし、安全性レビューにおいて留意事項として記録する。
        *   **判断理由:** 一過性であり臨床的意義が低い可能性が高い。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD = 'CK', LB.LBSTRESN = 317 (Day 54), その後の値は正常範囲内。AEドメインに関連報告なし。
    *   **確認事項No.:** I-3 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 111 の一過性低カルシウム血症 (8.0 mg/dL) を確認。関連 AE 報告なく、その後正常化しているため、現時点での追加アクションは不要と判断。ただし、安全性レビューにおいて留意事項として記録する。
        *   **判断理由:** 一過性であり臨床的意義が低い可能性が高い。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD = 'CA', LB.LBSTRESN = 1.996 (Day 111), その後の値は正常範囲内。AEドメインに関連報告なし。
    *   **確認事項No.:** I-4 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** ベースラインおよび試験期間中の徐脈傾向（50 bpm台）を確認。プロトコル除外基準には抵触せず、関連 AE 報告もないため、現時点での追加アクションは不要と判断。治験薬の薬理作用との関連可能性を考慮し、安全性監視において留意する。
        *   **判断理由:** 基準値逸脱や症状がなく、リスクは低いと判断されるが、薬理作用との関連で注意が必要。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD = 'PULSE', VS.VSSTRESN が複数時点で50台。
    *   **確認事項No.:** I-5 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/Statistician
        *   **疑義事項/確認内容:** 本症例（Xanomeline High Dose群）では、主要・副次有効性評価項目においてベースラインからの改善が見られなかったことを確認。個々の症例の結果であり、試験全体の有効性評価の文脈で解釈する。
        *   **判断理由:** 個別症例の有効性欠如は、それ自体が直ちに問題とはならない。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのACTOT, CIBIC, NPTOT, DADスコアの推移。
    *   **確認事項No.:** I-6 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE の終了日が未記載であることを確認。転帰が NOT RECOVERED/NOT RESOLVED であるため、試験終了日まで継続と解釈可能。データの完全性の観点から、可能であれば終了日を補完する方針を検討するが、医学的評価への影響は小さい。
        *   **判断理由:** 転帰情報から状況が推測でき、評価への影響が限定的。
        *   **判断根拠:**
            *   関連するデータ: AE.AEENDTC, AE.AEENDY が欠損。AE.AEOUT = 'NOT RECOVERED/NOT RESOLVED'。
    *   **確認事項No.:** I-7 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** スクリーニング時の葉酸（Folate）データ欠損を確認。除外基準[28b]評価に影響した可能性があるが、Vitamin B12は基準範囲内であり、大球性貧血を示唆する所見は治験開始後に顕在化したため、適格性への影響は限定的と判断。今後のデータ収集プロセス改善の参考とする。
        *   **判断理由:** 適格性への影響が限定的であり、事後的な対応は困難。
        *   **判断根拠:**
            *   関連するデータ: LBドメインに Folate のレコードなし。LB.LBTESTCD='VITB12' は基準範囲内。
    *   **確認事項No.:** I-8 (関連指摘No.: P-9)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** PK採血の実施記録がデータセットにないことを確認。プロトコル遵守の観点からは確認が必要だが、主要な安全性・有効性評価への影響は小さい。内部（例：ラボデータ連携状況など）で実施状況を確認する。
        *   **判断理由:** 主要評価項目への影響が小さく、内部確認で対応可能と判断。
        *   **判断根拠:**
            *   関連するデータ: PK関連ドメインのデータなし。
            *   関連するプロトコル箇所: Section 3.9.2

---

# 01-701-1034のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
77歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年09月29日発症、PRIMARY DIAGNOSIS）、甲状腺機能低下症（SIGNIFICANT PRE-EXISTING CONDITION）、遠視（SIGNIFICANT PRE-EXISTING CONDITION）、便秘（SIGNIFICANT PRE-EXISTING CONDITION）、腹痛（SIGNIFICANT PRE-EXISTING CONDITION）、関節炎（SIGNIFICANT PRE-EXISTING CONDITION）、血圧上昇（HISTORICAL DIAGNOSIS、2014年06月11日）が報告されている。その他、子宮摘出術（1960年）、扁桃摘出術（1946年）、虫垂切除術（1949年）、フェイスリフト（2011年08月21日）、足骨折（2004年）、脚骨折（2012年）、直腸瘻（1962年）の既往歴がある。教育レベルは9年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2014年06月24日|Day -7 (SCREENING 1)|ベースライン検査実施。血圧: 臥位163/58 mmHg、立位1分後183/73 mmHg、立位3分後151/79 mmHg (高血圧傾向)。脈拍: 臥位69 bpm、立位1分後76 bpm、立位3分後74 bpm。体重: 63.5 kg。ALP: 41 U/L (正常)。TSH: 0.27 uIU/mL (低値)。MCV: 102 fL (高値)。Anisocytes: 1 (異常)。Hachinski Ischemic Score: 0点。|
|2014年06月29日|Day -2 (SCREENING 2)|血圧: 臥位158/62 mmHg、立位1分後155/81 mmHg、立位3分後155/69 mmHg。脈拍: 臥位75 bpm、立位1分後79 bpm、立位3分後79 bpm。|
|2014年07月01日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg (Patch) 投与開始。血圧: 臥位163/60 mmHg、立位1分後177/75 mmHg、立位3分後168/82 mmHg。脈拍: 臥位76 bpm、立位1分後83 bpm、立位3分後80 bpm。体重: 62.6 kg。ADAS-Cog(11): 11点。NPI-X Total: 0点。DAD: 全項目1点。|
|2014年07月15日|Day 15 (WEEK 2)|治験薬 Xanomeline 54 mg 投与終了。血圧: 臥位183/81 mmHg、立位1分後191/101 mmHg、立位3分後161/84 mmHg (高値)。脈拍: 臥位86 bpm、立位1分後91 bpm、立位3分後86 bpm。体重: 62.6 kg。ALP: 34 U/L (低値)。MCV: 106 fL (高値)。NPI-X Total: 0点。|
|2014年07月16日|Day 16 (N/A)|治験薬 Xanomeline 81 mg (Patch) 投与開始。|
|2014年07月29日|Day 29 (WEEK 4)|血圧: 臥位165/71 mmHg、立位1分後170/69 mmHg、立位3分後169/71 mmHg。脈拍: 臥位87 bpm、立位1分後91 bpm、立位3分後88 bpm。体重: 63.96 kg。ALP: 36 U/L (正常)。MCV: 103 fL (高値)。RBC: 3.8 TI/L (低値)。NPI-X Total: 2点 (Disinhibition=1, Irritability/Lability=1)。|
|2014年08月11日|Day 42 (WEEK 6)|血圧: 臥位145/57 mmHg、立位1分後174/76 mmHg、立位3分後170/80 mmHg。脈拍: 臥位97 bpm、立位1分後93 bpm、立位3分後94 bpm。体重: 63.96 kg。ALP: 33 U/L (低値)。MCV: 103 fL (高値)。RBC: 3.7 TI/L (低値)。NPI-X Total: 3点 (Agitation/Aggression=1, Disinhibition=1, Irritability/Lability=1)。|
|2014年08月26日|Day 57 (WEEK 8)|血圧: 臥位188/73 mmHg、立位1分後197/80 mmHg、立位3分後198/76 mmHg (高値)。脈拍: 臥位78 bpm、立位1分後71 bpm、立位3分後71 bpm。体重: 63.05 kg。ALP: 29 U/L (低値)。MCV: 101 fL (高値)。ADAS-Cog(11): 12点。CIBIC+: 4 (No Change)。DAD: 全項目1点。NPI-X Total: 0点。|
|2014年08月27日|Day 58 (N/A)|有害事象「APPLICATION SITE PRURITUS」(Mild, Probable) 発現。併用薬 Hydrocortisone 開始。|
|2014年09月09日|Day 71 (WEEK 10 (T))|NPI-X Total: 1点 (Delusions=1)。|
|2014年09月25日|Day 87 (WEEK 12)|血圧: 臥位145/71 mmHg、立位1分後150/66 mmHg、立位3分後177/63 mmHg。脈拍: 臥位66 bpm、立位1分後70 bpm、立位3分後69 bpm。体重: 63.05 kg。ALP: 34 U/L (低値)。MCV: 101 fL (高値)。RBC: 3.8 TI/L (低値)。NPI-X Total: 0点。|
|2014年10月21日|Day 113 (WEEK 16)|血圧: 臥位154/87 mmHg、立位1分後183/77 mmHg、立位3分後186/72 mmHg。脈拍: 臥位74 bpm、立位1分後79 bpm、立位3分後78 bpm。体重: 64.41 kg。ALP: 34 U/L (低値)。MCV: 103 fL (高値)。MCH: 35 pg (高値)。RBC: 3.8 TI/L (低値)。ADAS-Cog(11): 14点。CIBIC+: 3 (Minimal Improvement)。DAD: 全項目1点。NPI-X Total: 0点。|
|2014年11月02日|Day 125 (N/A)|有害事象「MALIGNANT HYPERTENSION」(Mild, Possible) 発現。|
|2014年11月04日|Day 127 (WEEK 18 (T))|NPI-X Total: 5点 (Agitation/Aggression=3, Disinhibition=1, Irritability/Lability=1)。|
|2014年11月18日|Day 141 (WEEK 20)|血圧: 臥位167/78 mmHg、立位1分後181/77 mmHg、立位3分後185/72 mmHg。脈拍: 臥位86 bpm、立位1分後84 bpm、立位3分後80 bpm。体重: 64.86 kg。ALP: 31 U/L (低値)。MCV: 102 fL (高値)。NPI-X Total: 1点 (Irritability/Lability=1)。|
|2014年12月17日|Day 170 (WEEK 24)|治験薬 Xanomeline 81 mg 投与終了。血圧: 臥位178/81 mmHg、立位1分後198/97 mmHg、立位3分後164/98 mmHg (高値)。脈拍: 臥位96 bpm、立位1分後97 bpm、立位3分後91 bpm。体重: 65.32 kg。ALP: 40 U/L (正常)。MCV: 102 fL (高値)。MCH: 37 pg (高値)。RBC: 3.5 TI/L (低値)。SODIUM: 134 mEq/L (低値)。ADAS-Cog(11): 11点。CIBIC+: 4 (No Change)。DAD: 全項目1点。NPI-X Total: 1点 (Agitation/Aggression=1)。|
|2014年12月18日|Day 171 (N/A)|治験薬 Xanomeline 54 mg (Patch) 投与開始 (減量)。|
|2014年12月30日|Day 183 (WEEK 26)|治験薬 Xanomeline 54 mg 投与終了。試験完了。血圧: 臥位154/67 mmHg、立位1分後150/93 mmHg、立位3分後179/66 mmHg。脈拍: 臥位74 bpm、立位1分後86 bpm、立位3分後76 bpm。体重: 63.96 kg。ALP: 27 U/L (低値)。MCV: 102 fL (高値)。MCH: 35 pg (高値)。RBC: 3.7 TI/L (低値)。SODIUM: 134 mEq/L (低値)。NPI-X Total: 0点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「MALIGNANT HYPERTENSION」が報告されているが、重症度が「MILD」と評価されている点に重大な疑義がある。Malignant Hypertensionは通常、緊急治療を要する重篤な高血圧緊急症であり、臓器障害を伴うことが多い。VSデータでは実際に著しい高血圧（例: Day 57 SYSBP 198 mmHg, Day 170 SYSBP 198 mmHg）が記録されており、Severity=Mildとの評価は医学的に不適切である可能性が高い。用語選択の誤りか、評価が不十分である可能性があり、参加者の安全性リスク評価に重大な影響を与える。
        *   **根拠:** Malignant Hypertensionの医学的定義と重症度評価の一般的な基準との乖離。VSデータにおける顕著な高血圧記録。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MALIGNANT HYPERTENSION'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 125
            *   [Systolic Blood Pressure(VS.VSSTRESN)] = 198 (Day 57, Standing 3 min), 198 (Day 170, Standing 1 min)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** ベースラインから一貫して高血圧が認められ、治験期間中にさらに悪化する傾向が見られる（特にDay 15, 57, 170）。MHに「BLOOD PRESSURE INCREASED」の既往があるが、CMには降圧薬の使用記録がない。高血圧の管理が不十分であった可能性があり、参加者の安全性リスクが懸念される。
        *   **根拠:** VSデータにおける持続的な高血圧。MHデータ。CMデータ。
        *   **関連データ:**
            *   [Systolic Blood Pressure(VS.VSSTRESN)] = 163 (Day 1, Supine), 177 (Day 1, Standing 1 min), 168 (Day 1, Standing 3 min), 183 (Day 15, Supine), 191 (Day 15, Standing 1 min), 188 (Day 57, Supine), 197 (Day 57, Standing 1 min), 198 (Day 57, Standing 3 min), 178 (Day 170, Supine), 198 (Day 170, Standing 1 min)
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1680' (Decoded: BLOOD PRESSURE INCREASED)
            *   CMドメイン全般 (降圧薬なし)
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** ベースラインから持続的にMCV高値、MCH高値、RBC低値が認められ、大球性貧血を示唆する。Vitamin B12は正常範囲内であり、葉酸欠乏や薬剤性、その他の原因が考えられるが、関連する評価や対応の記録がない。臨床症状の有無や原因評価について情報が不足している。
        *   **根拠:** LBデータにおけるMCV, MCH, RBCの異常値持続。一般的な貧血評価の観点。
        *   **関連データ:**
            *   [Ery. Mean Corpuscular Volume(LB.LBSTRESN)] = 102 (Day -7), 106 (Day 15), 103 (Day 29), ..., 102 (Day 183) (全てHigh)
            *   [Ery. Mean Corpuscular Hemoglobin(LB.LBSTRESN)] = 2.11 (Day -7, Normal), ..., 2.17 (Day 113, High), 2.30 (Day 170, High), 2.17 (Day 183, High)
            *   [Erythrocytes(LB.LBSTRESN)] = 3.9 (Day -7, Normal), ..., 3.8 (Day 29, Low), 3.7 (Day 42, Low), ..., 3.5 (Day 170, Low), 3.7 (Day 183, Low)
            *   [Vitamin B12(LB.LBSTRESN)] = 436.7776 (Day -7, Normal)
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** ALP値がベースライン以降、複数時点で基準値下限を下回っている。臨床的意義は不明確なことが多いが、持続しているため記録しておく。
        *   **根拠:** LBデータにおけるALP低値の持続。
        *   **関連データ:**
            *   [Alkaline Phosphatase(LB.LBSTRESN)] = 41 (Day -7, Normal), 34 (Day 15, Low), 36 (Day 29, Normal), 33 (Day 42, Low), ..., 27 (Day 183, Low)
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 35 (for ALP)
    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** Day 171から治験薬が81mgから54mgに減量されている。減量の医学的理由（AEとの関連、忍容性など）が不明である。有効性・安全性評価の解釈に影響を与える可能性がある。
        *   **根拠:** EXデータの投与量変更記録。プロトコルに減量基準の記載が見当たらない。
        *   **関連データ:**
            *   [Dose per Administration(EX.EXDOSE)] = 54 (Day 1-15), 81 (Day 16-170), 54 (Day 171-183)
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** 試験終了間際 (Day 170, 183) に軽度の低ナトリウム血症が認められる。臨床的意義は低いと考えられるが、薬剤関連の可能性も否定できないため記録しておく。
        *   **根拠:** LBデータにおけるSodium低値。
        *   **関連データ:**
            *   [Sodium(LB.LBSTRESN)] = 134 (Day 170, Low), 134 (Day 183, Low)
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 135 (for Sodium)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** AE「MALIGNANT HYPERTENSION」の重症度「MILD」と、VSデータにおける著しい高血圧記録との間に医学的な整合性の問題がある。これは【医学的レビュー】M-1で指摘した内容と関連し、データの信頼性に重大な疑義を生じさせる。
        *   **根拠:** AE.AESEVとVS.VSSTRESNの比較。Malignant Hypertensionの医学的定義。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MALIGNANT HYPERTENSION'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Systolic Blood Pressure(VS.VSSTRESN)] = 198 (Day 57, Standing 3 min), 198 (Day 170, Standing 1 min)
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 治験薬の投与量がDay 171から減量されているが (EX.EXDOSE)、その理由を示すデータ（例: AEACNの変更、関連するAE記録など）が不足している。投与量変更の根拠が不明確であり、曝露量評価や有効性・安全性評価の解釈に影響する。
        *   **根拠:** EXドメインの投与量変更記録と、AE/CM/DSドメイン等における関連情報の欠如。
        *   **関連データ:**
            *   [Dose per Administration(EX.EXDOSE)] = 54 (Day 1-15), 81 (Day 16-170), 54 (Day 171-183)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** AE「APPLICATION SITE PRURITUS」の転帰が「NOT RECOVERED/NOT RESOLVED」であり、対応する併用薬「HYDROCORTISONE」の終了日 (CM.CMENDTC) が欠損している。これは治験終了までAEと投薬が継続していた可能性を示唆し、形式的には整合していると考えられるが、明確な終了情報がない。
        *   **根拠:** AE.AEOUTとCM.CMENDTCの関連性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '' (空欄)
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 同意取得日時 (DM.RFICDTC) が欠損している。GCP上、治験開始前に同意取得が必須であり、この情報の欠損は記録の完全性に関する重要な問題である。
        *   **根拠:** DM.RFICDTCの欠損。GCP要件。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (空欄)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 選択/除外基準の評価に必要なデータの一部（MMSEスコア、CNSイメージング結果、ベースラインECG所見など）が提供されたJSONデータに含まれていない。適格性確認データは収集されない前提のため、これらの基準を満たしていたかは不明だが、ベースラインの高血圧が除外基準[17] "Uncontrolled hypertension" に該当しなかったか、MCV高値が除外基準[27b]に抵触しなかったかなど、適格性評価の妥当性に疑問が残る。
        *   **プロトコル該当箇所:** Section 3.4.2.1 (Inclusion Criteria), 3.4.2.2 (Exclusion Criteria)
        *   **根拠:** 提供されたデータとプロトコルの選択/除外基準の照合。ベースラインのVSおよびLBデータ。
        *   **関連データ:**
            *   QSドメイン (MMSEスコアなし)
            *   [Systolic Blood Pressure(VS.VSSTRESN)] = 163 (Day 1, Supine), 177 (Day 1, Standing 1 min)
            *   [Ery. Mean Corpuscular Volume(LB.LBSTRESN)] = 102 (Day -7, High)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** Day 171からの治験薬減量 (81mg -> 54mg) が、プロトコルに記載された投与計画（Figure LZZT.1参照）からの逸脱である可能性がある。プロトコルには減量に関する規定が見当たらないため、逸脱と判断される可能性がある。この変更が有効性・安全性評価に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.6 (Dosage and Administration), Figure LZZT.1
        *   **根拠:** EXデータの投与量変更記録とプロトコルの投与計画の比較。
        *   **関連データ:**
            *   [Dose per Administration(EX.EXDOSE)] = 54 (Day 1-15), 81 (Day 16-170), 54 (Day 171-183)
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルで規定された評価の一部（ECG, Ambulatory ECG, Plasma Specimen）のデータが提供されたJSONに含まれていない。データが収集されなかったのか、単に提供されていないだけなのか不明。もし未実施であればプロトコル逸脱となる。
        *   **プロトコル該当箇所:** Section 3.9 (Efficacy, Pharmacokinetic, and Safety Evaluations), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 提供されたJSONデータとプロトコルの評価スケジュールの比較。
        *   **関連データ:** JSONデータ全体 (該当ドメイン/データなし)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が欠損しており、最初の治験手順実施 (Visit 1, 2014-06-24) より前に同意が取得されたか確認できない。もし同意取得前に手順が開始されていた場合、GCP違反となる。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** DM.RFICDTCの欠損。最初の治験手順日 (SV.SVSTDTC at Visit 1)。GCP要件。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (空欄)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-06-24' (Visit 1)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象名「MALIGNANT HYPERTENSION」について、重症度が「MILD」と記録されています。しかしながら、バイタルサインデータでは収縮期血圧が190 mmHgを超える記録が複数認められます。Malignant Hypertensionの診断根拠（臓器障害の有無など）と、重症度評価が「MILD」とされた理由について詳細をご教示ください。参加者の安全性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding the AE Term 'MALIGNANT HYPERTENSION', the Severity is recorded as 'MILD'. However, VS data show multiple SYSBP readings >190 mmHg. Please provide the basis for the Malignant Hypertension diagnosis (e.g., organ damage) and the rationale for the 'MILD' severity assessment. Confirmation is needed for patient safety.
        *   **判断理由:** Malignant Hypertensionの報告と重症度評価の間に重大な矛盾があり、参加者の安全性リスク評価とデータの信頼性に疑義があるため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'MALIGNANT HYPERTENSION', [Severity/Intensity(AE.AESEV)] = 'MILD', [Study Day of Start of Adverse Event(AE.AESTDY)] = 125, [Systolic Blood Pressure(VS.VSSTRESN)] = 198 (Day 57), 198 (Day 170)
            *   関連する医学的知見: Malignant Hypertensionの定義と臨床的重要性。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, P-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 本症例ではベースラインから高血圧が認められ、治験期間中も持続・悪化しています（例: Study Day 57 立位3分後 収縮期血圧 198 mmHg）。併用薬に降圧薬の使用記録がありませんが、高血圧に対する臨床評価と治療方針（降圧薬未使用の理由を含む）についてご教示ください。参加者の安全性確保の観点から確認が必要です。
        *   **クエリ文面（英語）:** Persistent hypertension was observed from baseline and during the study (e.g., SYSBP 198 mmHg on Day 57). No antihypertensive medication is recorded in CM. Please provide the clinical assessment and management plan for hypertension, including the rationale for not using antihypertensives. Confirmation is needed for patient safety.
        *   **判断理由:** 持続的な高血圧に対する管理が不明確であり、参加者の安全性リスクが懸念されるため。
        *   **判断根拠:**
            *   関連するデータ: VSドメインの血圧データ、MHドメインの既往歴、CMドメインの薬剤リスト。
            *   関連するプロトコル箇所: Section 3.4.2.2 [17] (Exclusion Criteria - Uncontrolled hypertension)
            *   関連する医学的知見: 高血圧管理の重要性。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-5, D-2, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 171から治験薬の投与量が81mgから54mgに減量されています。減量の理由（例：有害事象発現、忍容性等）について詳細をご教示ください。プロトコル遵守および評価への影響を確認するため、情報が必要です。
        *   **クエリ文面（英語）:** The study drug dose was reduced from 81mg to 54mg starting Day 171. Please provide the reason for this dose reduction (e.g., related to an AE, tolerability issue?). This information is needed to confirm protocol compliance and assess impact on evaluations.
        *   **判断理由:** プロトコルからの逸脱の可能性があり、減量の理由が不明なため、有効性・安全性評価の解釈に影響を与える可能性があるため。
        *   **判断根拠:**
            *   関連するデータ: [Dose per Administration(EX.EXDOSE)] = 54 (Day 1-15), 81 (Day 16-170), 54 (Day 171-183)
            *   関連するプロトコル箇所: Section 3.6 (Dosage and Administration), Figure LZZT.1
    *   **クエリNo.:** Q-4 (関連指摘No.: D-4, P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日時が記録されていません。最初の治験関連手順実施日（Visit 1: 2014年06月24日）より前に、適切にインフォームド・コンセントが取得されていたことを確認し、同意取得日をご報告ください。GCP遵守の確認のため必要です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (RFICDTC) is missing. Please confirm that informed consent was obtained prior to the first study procedure on 2014-06-24 and provide the date of consent. This is required for GCP compliance verification.
        *   **判断理由:** 同意取得の記録がなく、GCP遵守と参加者の権利保護の観点から確認が必須なため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (空欄), [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-06-24' (Visit 1)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
    *   **クエリNo.:** Q-5 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** ベースラインから赤血球平均容積 (MCV) の高値、赤血球ヘモグロビン量 (MCH) の高値、赤血球数 (RBC) の低値が持続しています。これらの所見に対する臨床的な評価（貧血症状の有無、原因検索など）と対応についてご教示いただけますでしょうか。安全性評価の補足情報として確認させてください。
        *   **クエリ文面（英語）:** Persistently high MCV, high MCH, and low RBC values are noted from baseline. Could you please provide the clinical assessment (e.g., anemia symptoms, investigation) and management for these findings? This is for supplementary safety assessment.
        *   **判断理由:** 大球性貧血を示唆する検査所見の原因や臨床的意義が不明なため、安全性評価の補足情報として確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LBドメインのMCV, MCH, RBCデータ。
            *   関連する医学的知見: 大球性貧血の原因と評価。

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 持続的なALP低値について、他の臨床情報と併せて医学的な意義を評価し、記録する。現時点では、他の重篤な所見との関連は薄く、直ちに介入が必要な状況とは考えにくい。
        *   **判断理由:** ALP低値単独での臨床的緊急性は低いと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: [Alkaline Phosphatase(LB.LBSTRESN)] データ。
    *   **確認事項No.:** I-2 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 試験終了間際の軽度低ナトリウム血症について、他の臨床情報と併せて医学的な意義を評価し、記録する。変動幅は小さく、臨床症状の報告もないため、現時点でのリスクは低いと判断。
        *   **判断理由:** 低ナトリウム血症の程度が軽微であり、臨床的な影響が小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: [Sodium(LB.LBSTRESN)] データ。
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA, DM
        *   **疑義事項/確認内容:** 選択基準[3] (MMSE score 10-23) を満たしていたか確認するデータがJSONに含まれていない。適格性確認データは収集されない前提であるため、逸脱とは断定できないが、適格性確認プロセスが適切に行われたか内部で確認・記録する。
        *   **判断理由:** 適格性確認データが収集されない前提のため、医療機関への問い合わせは不要だが、記録として残す。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (MMSEスコアなし)。
            *   関連するプロトコル箇所: Section 3.4.2.1 [3]
    *   **確認事項No.:** I-4 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor, CRA
        *   **疑義事項/確認内容:** ベースラインの高血圧が除外基準[17] "Uncontrolled hypertension" に該当しなかったか、およびMCV高値が除外基準[27b]に抵触しなかったかについて、適格性評価の妥当性を内部でレビューし記録する。
        *   **判断理由:** 適格性評価の判断根拠を確認するためだが、治験は完了しており、現時点での安全性への直接的な影響は限定的と判断。
        *   **判断根拠:**
            *   関連するデータ: VS, LB, MHデータ。
            *   関連するプロトコル箇所: Section 3.4.2.2 [17], [27b]
    *   **確認事項No.:** I-5 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM, CRA
        *   **疑義事項/確認内容:** プロトコルで規定されているECG, Ambulatory ECG, Plasma Specimenのデータが提供JSONに含まれていない件について、データ収集・管理状況を確認し記録する。収集済みで提供漏れか、未収集（逸脱）かを確認。
        *   **判断理由:** データの完全性に関する確認だが、治験は完了しており、現時点での安全性への直接的な影響は限定的と判断。
        *   **判断根拠:**
            *   関連するデータ: JSONデータ全体。
            *   関連するプロトコル箇所: Attachment LZZT.1 (Schedule of Events)

---

# 01-701-1047のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
85歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2009年7月26日発症、PRIMARY DIAGNOSIS）、乾癬（MILD）、感覚鈍麻（手のしびれ、MILD）、食道裂孔ヘルニア（MILD）、末梢性浮腫（足の浮腫、MILD）、関節炎（MILD）、甲状腺機能低下症（MILD）、副鼻腔炎（MILD）がSignificant Pre-existing Conditionとして報告されている。その他、膀胱炎、白内障手術、潰瘍、胆嚢摘出術、痔核、扁桃摘出術の既往歴あり。教育歴は8年。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年01月22日|Day -21 (SCREENING 1)|Screening Visit実施。MMSE 23点、Hachinski Score 0点。身長 148.59cm, 体重 66.23kg。臥位血圧 165/68 mmHg、立位血圧(1分後) 162/71 mmHg、(3分後) 161/83 mmHg。ベースライン検査値測定。|
|2013年02月10日|Day -2 (SCREENING 2)|Screening Visit実施。臥位血圧 159/65 mmHg、立位血圧(1分後) 152/86 mmHg、(3分後) 138/71 mmHg。|
|2013年02月12日|Day 1 (BASELINE)|治験薬（Placebo）投与開始。体重 67.13kg。臥位血圧 151/61 mmHg、立位血圧(1分後) 145/68 mmHg、(3分後) 167/78 mmHg。有害事象「HIATUS HERNIA」(Moderate) 発現（同日終了記録あり、データ不整合の可能性）。ADAS-Cog(11) Total Score 10点、NPI-X Total Score 2点。|
|2013年02月24日|Day 13 (AMBUL ECG PLACEMENT)|Ambulatory ECG装着 Visit。臥位血圧 146/72 mmHg、立位血圧(1分後) 137/56 mmHg、(3分後) 148/73 mmHg。|
|2013年02月25日|Day 14 (WEEK 2)|Week 2 Visit実施。体重 67.59kg。臥位血圧 145/72 mmHg、立位血圧(1分後) 146/84 mmHg、(3分後) 153/73 mmHg。検査値測定。有害事象「HIATUS HERNIA」転帰記録 (Recovered/Resolved)。NPI-X Total Score 1点。|
|2013年03月06日|Day 23 (N/A)|有害事象「UPPER RESPIRATORY TRACT INFECTION」(Mild) 発現（開始日と終了日に矛盾あり）。|
|2013年03月07日|Day 24 (N/A)|併用薬「ROBITUSSIN-DM」、「SUDAFED」開始。|
|2013年03月09日|Day 26 (N/A)|治験薬（Placebo）投与終了。|
|2013年03月10日|Day 27 (WEEK 4)|Week 4 Visit実施。体重 67.59kg。臥位血圧 135/72 mmHg、立位血圧(1分後) 185/121 mmHg、(3分後) 183/124 mmHg（立位時に著明な血圧上昇）。有害事象「HYPERTENSION」(Mild) 発現。検査値測定。NPI-X Total Score 1点。|
|2013年03月29日|Day 46 (AMBUL ECG REMOVAL)|Ambulatory ECG除去 Visit（予定Day 30から遅延）。治験中止（理由: ADVERSE EVENT - HYPERTENSION）。体重 67.13kg。臥位血圧 123/71 mmHg、立位血圧(1分後) 115/63 mmHg、(3分後) 123/57 mmHg。立位時頻脈（臥位78→立位90/87 bpm）。検査値測定。ADAS-Cog(11) Total Score 14点、NPI-X Total Score 1点。CIBIC+ 4点 (No Change)。|
|2013年04月07日|Day 55 (UNSCHEDULED 6.1)|最終検査Visit。検査値測定。|
|2013年07月28日|Day 167 (RETRIEVAL)|Retrieval Visit実施。臥位血圧 139/76 mmHg、立位血圧(1分後) 130/71 mmHg、(3分後) 139/65 mmHg。ADAS-Cog(11) Total Score 19点。NPI-X Total Score 8点。CIBIC+ 5点 (Minimal worsening)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 27に発現した有害事象「HYPERTENSION」について、Severityが「MILD」と評価されているが、同日の立位時血圧は185/121 mmHg、183/124 mmHgと著しい高値を示しており、医学的には中等度以上の評価が妥当と考えられる。本有害事象が治験中止理由とされている（DS, RELREC）ことから、Severity評価の妥当性について確認が必要である。85歳という高齢であり、顕著な血圧上昇は心血管イベントのリスクを高めるため、参加者の安全性確保の観点から重要である。
        *   **根拠:** VSデータにおける著しい血圧上昇値と、一般的な高血圧の重症度分類基準との乖離。高齢者の高血圧リスクに関する医学的知見。治験中止理由との関連性。
        *   **関連データ:**
            *   [有害事象名(AETERM)] = 'HYPERTENSION'
            *   [重症度/強度(AESEV)] = 'MILD'
            *   [有害事象開始日(AESTDTC)] = '2013-03-10' (Day 27)
            *   [報告されたDispositionイベントの用語(DSTERM)] = 'ADVERSE EVENT'
            *   [Dispositionイベントの標準化された用語(DSDECOD)] = 'ADVERSE EVENT'
            *   [Dispositionイベント開始日(DSSTDTC)] = '2013-03-29' (Day 46)
            *   [関連レコード(RELREC)]：AE SEQ=4 と DS SEQ=1 の関連付け
            *   [バイタルサイン検査名(VSTEST)] = 'Systolic Blood Pressure', [バイタルサインの位置(VSPOS)] = 'STANDING', [測定日時(VSDTC)] = '2013-03-10', [標準単位での数値結果(VSSTRESN)] = 185, 183
            *   [バイタルサイン検査名(VSTEST)] = 'Diastolic Blood Pressure', [バイタルサインの位置(VSPOS)] = 'STANDING', [測定日時(VSDTC)] = '2013-03-10', [標準単位での数値結果(VSSTRESN)] = 121, 124

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「HIATUS HERNIA」について、AESEQ=1とAESEQ=2で重複して記録されているように見える。AESEQ=1ではOutcomeがNOT RECOVERED/NOT RESOLVED、AESEQ=2ではRECOVERED/RESOLVEDとなっている。また、両レコードとも開始日(AESTDTC)と終了日(AEENDTC)が同日(2013-02-12)であり、AESEQ=2の転帰記録日(AEDTC=2013-02-25)と一致しない。記録の正確性に疑義があり、データの信頼性に影響する可能性がある。
        *   **根拠:** 同一事象と思われる記録の重複、日付情報の不整合。
        *   **関連データ:**
            *   [有害事象名(AETERM)] = 'HIATUS HERNIA'
            *   [シーケンス番号(AESEQ)] = 1, 2
            *   [有害事象開始日(AESTDTC)] = '2013-02-12' (for AESEQ=1, 2)
            *   [有害事象終了日(AEENDTC)] = '2013-02-12' (for AESEQ=1, 2)
            *   [有害事象の転帰(AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (for AESEQ=1), 'RECOVERED/RESOLVED' (for AESEQ=2)
            *   [収集日時(AEDTC)] = '2013-02-12' (for AESEQ=1), '2013-02-25' (for AESEQ=2)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「UPPER RESPIRATORY TRACT INFECTION」(AESEQ=3)について、開始日(AESTDTC=2013-03-06)が終了日(AEENDTC=2013-03-05)よりも後になっており、日付に矛盾がある。データ入力エラーの可能性が高く、イベント期間の評価に影響する。
        *   **根拠:** 開始日と終了日の論理的な矛盾。
        *   **関連データ:**
            *   [有害事象名(AETERM)] = 'UPPER RESPIRATORY TRACT INFECTION'
            *   [シーケンス番号(AESEQ)] = 3
            *   [有害事象開始日(AESTDTC)] = '2013-03-06'
            *   [有害事象終了日(AEENDTC)] = '2013-03-05'
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 併用薬(CM)ドメインにおいて、多くの薬剤でIndication(CMINDC)が欠損している。また、CENTRUM, FELDENE, PAPAYA, PSORCON, ROBITUSSIN-DM, SUDAFED, SYNTHROIDについて、Standardized Medication Name(CMDECOD)およびMedication Class(CMCLAS)が"UNCODED"または欠損となっている。データの完全性および標準化に問題があり、薬剤評価の精度に影響する可能性がある。
        *   **根拠:** 必須ではないが重要な情報の欠損、標準化の不備。
        *   **関連データ:**
            *   CMドメイン全体
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** AEドメインおよびMHドメインにおいて、MedDRAコーディングに関連する変数（AELLT, AELLTCD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCD, MHLLT, MHDECOD, MHHLT, MHHLGT, MHBODSYSなど）が欠損または未完了（Verbatimのまま）となっている箇所が多い。データの標準化が不十分であり、集計や安全性シグナル検出に影響する可能性がある。
        *   **根拠:** 標準化コーディングの不備。
        *   **関連データ:**
            *   AEドメイン全体
            *   MHドメイン全体
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** QSドメインのNPI-X Total Score (NPTOT) について、Day 167の計算結果(8点)が、同日の各項目スコアの合計（Depression(1)+Disinhibition(6)+Irritability(1)+Night-time Behavior(0) = 8点）と一致しているように見えるが、プロトコル4.3.1ではTotal Scoreは9項目（sleep, appetite, euphoriaを除く）で計算すると記載されている。Night-time Behaviorは計算に含まれるべき項目と思われるが、スコアが0のため結果に影響していない可能性がある。しかし、計算ロジックがプロトコルと一致しているか確認が必要。
        *   **根拠:** プロトコル記載の計算方法とデータからの推測の間の潜在的な不一致。
        *   **関連データ:**
            *   [質問票名(QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [質問票の簡単な名前(QSTESTCD)] = 'NPTOT', 'NPITM04S', 'NPITM08S', 'NPITM09S', 'NPITM11S'
            *   [標準単位での数値結果(QSSTRESN)] (Day 167)
            *   [派生フラグ(QSDRVFL)] = 'Y' (for NPTOT)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された選択/除外基準の確認に必要なデータの一部が欠損している。具体的には、Inclusion [5] (CNS imaging結果)、Inclusion [6] (同意取得日)、Exclusion [16b] (Screening ECG結果)、Exclusion [28b] (Folate値)、Exclusion [29b] (Syphilis screening結果)がデータから確認できない。特にScreening ECGの結果は心血管系のリスク評価に重要であり、欠損は参加者の安全性評価に影響を与える可能性がある。同意取得日の欠損は参加者の権利保護の観点から問題となる。
        *   **プロトコル該当箇所:** Section 3.4.2.1, 3.4.2.2
        *   **根拠:** プロトコルで要求される適格性確認データと提供データの比較。
        *   **関連データ:**
            *   DMドメイン (RFICDTC欠損)
            *   LBドメイン (Folateデータ欠損)
            *   (ECG, Imaging, Syphilisデータセットが存在しない)
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **逸脱の可能性:** プロトコルで規定された安全性およびPK評価に必要なデータが欠損している。具体的には、ECGデータ（Screening, Visits 4, 5, ETなど）、Ambulatory ECGデータ（Visit 2/3, Visit 3.5/6）、PKサンプルデータ（Visits 3, 4, 5など）が提供されていない。ECGおよびAmbulatory ECGは心血管系の安全性モニタリングに不可欠であり、これらのデータの欠損は参加者の安全性監視を著しく損なう可能性がある。PKデータの欠損は試験目的の一部（PK/PD解析）の達成を困難にする。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 (Cardiovascular Safety Measures), 3.9.2 (Pharmacokinetics), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルで要求される評価データと提供データの比較。安全性評価（特に心血管系）およびPK評価への影響。
        *   **関連データ:**
            *   (ECG, PKデータセットが存在しない)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された有効性評価の一部が予定通り実施されていない、またはデータが欠損している。ADAS-Cog, CIBIC+, DADはVisit 8, 10, 12でのデータがなく、NPI-XはVisit 6以降Retrieval Visitまでデータがない。これらの欠損は主要/副次評価項目の評価の信頼性を損なう可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.1.1 (Efficacy Measures), Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルで要求される評価スケジュールと提供データの比較。有効性評価への影響。
        *   **関連データ:**
            *   QSドメイン (ADAS-Cog, CIBIC+, DAD, NPI-Xデータ)
            *   SVドメイン (実施Visit)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験中止の判断プロセスと記録に不明瞭な点がある。中止理由は有害事象「HYPERTENSION」(Day 27発現)とされているが、中止イベント日(DSSTDTC)はDay 46である。AE発現から中止決定までに時間が空いている理由、およびその間の患者の状態や投与状況が不明である。また、AE SeverityがMildと評価されているにも関わらず中止に至った判断根拠がデータからは不明確である。プロトコル3.10.1の中止基準に照らして、判断の妥当性と記録の正確性を確認する必要がある。
        *   **プロトコル該当箇所:** Section 3.10.1 (Discontinuations)
        *   **根拠:** AE発現日と中止イベント日の乖離、AE重症度評価と中止判断の関連性の不明瞭さ。
        *   **関連データ:**
            *   [有害事象名(AETERM)] = 'HYPERTENSION'
            *   [重症度/強度(AESEV)] = 'MILD'
            *   [有害事象開始日(AESTDTC)] = '2013-03-10' (Day 27)
            *   [報告されたDispositionイベントの用語(DSTERM)] = 'ADVERSE EVENT'
            *   [Dispositionイベントの標準化された用語(DSDECOD)] = 'ADVERSE EVENT'
            *   [Dispositionイベント開始日(DSSTDTC)] = '2013-03-29' (Day 46)
            *   [関連レコード(RELREC)]：AE SEQ=4 と DS SEQ=1 の関連付け
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 6 (AMBUL ECG REMOVAL) が予定日 (Day 30) から大幅に遅延し、Day 46に実施されている。遅延理由が不明であり、プロトコルで規定された評価スケジュールからの逸脱の可能性がある。ただし、本Visitは主にAmbulatory ECGの除去が目的であり、主要な有効性評価Visitではないため、評価への影響は限定的かもしれないが、遅延理由は確認すべきである。
        *   **プロトコル該当箇所:** Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 予定Visit日と実際のVisit日の乖離。
        *   **関連データ:**
            *   [Visit名(VISIT)] = 'AMBUL ECG REMOVAL'
            *   [Visit番号(VISITNUM)] = 6
            *   [Visit開始日時(SVSTDTC)] = '2013-03-29' (Day 46)
            *   [予定されたVisitの治験日(VISITDY)] = 30 (TVドメインより)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「HYPERTENSION」について、Study Day 27の立位時血圧が185/121 mmHg、183/124 mmHgと著明な高値を示していますが、重症度が「MILD」と評価されています。この評価の根拠と、本有害事象による治験中止（Study Day 46）に至った経緯、および中止決定の詳細な理由について確認をお願いします。参加者の安全確保の観点から、適切な評価と判断であったかを確認させてください。
        *   **クエリ文面（英語）:** Regarding the AE 'HYPERTENSION' (started Day 27), Severity is 'MILD' despite standing BP 185/121 & 183/124 mmHg. This AE led to study discontinuation on Day 46. Please confirm the rationale for the severity assessment and provide details on the decision process for discontinuation. This is for patient safety assessment.
        *   **判断理由:** 有害事象の重症度評価が臨床データと乖離している可能性があり、治験中止判断の妥当性を確認する必要があるため。参加者の安全性評価に影響する。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='HYPERTENSION', AE.AESEV='MILD', AE.AESTDTC='2013-03-10', DS.DSTERM='ADVERSE EVENT', DS.DSSTDTC='2013-03-29', VSデータ(Day 27)
            *   関連するプロトコル箇所: Section 3.10.1 (Discontinuations)
            *   関連する医学的知見: 高血圧の重症度分類、高齢者の心血管リスク
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1, P-2)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本症例において、プロトコルで要求されている評価データの一部が確認できません。具体的には、選択/除外基準確認のためのScreening ECG結果、および治験期間中に実施予定であったECG、Ambulatory ECG、薬物動態(PK)測定データが欠損しています。これらのデータは参加者の安全性監視（特に心血管系）および試験評価に不可欠です。データが存在する場合は提出を、存在しない場合はその理由と安全性への影響評価についてご報告ください。
        *   **クエリ文面（英語）:** Data for protocol-required assessments are missing for this subject: Screening ECG results, and on-study ECG, Ambulatory ECG, and PK data. These data are critical for cardiovascular safety monitoring and study evaluation. Please provide the data if available, or report the reason for missing data and assess the impact on patient safety.
        *   **判断理由:** 心血管系の安全性モニタリングに必須なECG/Ambulatory ECGデータ、およびPK評価に必要なデータが欠損しており、参加者の安全性確保および試験評価の信頼性に重大な影響を与えるため。
        *   **判断根拠:**
            *   関連するデータ: (ECG, PKデータセットが存在しない)
            *   関連するプロトコル箇所: Section 3.9.3.4.2, 3.9.2, Attachment LZZT.1
    *   **クエリNo.:** Q-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本症例はStudy Day 46で治験を中止していますが、プロトコルで規定されているVisit 8, 10, 12等での有効性評価（ADAS-Cog, CIBIC+, DAD, NPI-X）が実施されていません。これらの評価が実施されなかった理由について確認をお願いします。有効性評価データの欠損は、試験結果の評価に影響を与える可能性があります。
        *   **クエリ文面（英語）:** This subject discontinued on Day 46. Protocol-specified efficacy assessments (ADAS-Cog, CIBIC+, DAD, NPI-X) at Visits 8, 10, 12 etc. were not performed. Please clarify the reason why these assessments were missed. Missing efficacy data may impact the evaluation of study results.
        *   **判断理由:** 主要/副次評価項目のデータが予定通り収集されておらず、試験の有効性評価の信頼性に影響を与えるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン, SVドメイン
            *   関連するプロトコル箇所: Section 3.9.1.1, Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1, D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインにて、「HIATUS HERNIA」の重複記録と日付矛盾、「UPPER RESPIRATORY TRACT INFECTION」の開始日・終了日矛盾が見られる。データクリーニングにて修正要否を検討する。医学的評価への影響は小さいと判断。
        *   **判断理由:** データ入力エラーの可能性が高く、臨床的な解釈への大きな影響はないと考えられるため、内部でのデータ修正・確認で対応可能と判断。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=1, 2, 3)
    *   **確認事項No.:** I-2 (関連指摘No.: D-3, D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインにおけるIndication欠損、未コード化薬剤、AE/MHドメインにおけるMedDRAコーディング未完了を確認。データ標準化プロセスの一環として対応する。集計や全体評価には影響しうるが、個別の医学的評価への影響は限定的。
        *   **判断理由:** データ標準化・完全性の問題であり、内部プロセスで対応可能と判断。
        *   **判断根拠:**
            *   関連するデータ: CM, AE, MHドメイン
    *   **確認事項No.:** I-3 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM/Stat
        *   **疑義事項/確認内容:** NPI-X Total Score (NPTOT) の計算ロジックについて、プロトコル記載（9項目合計）との整合性を確認する。Day 167のデータでは結果に影響はないように見えるが、他の時点も含めて確認が必要。
        *   **判断理由:** 計算ロジックの確認であり、内部での検証が可能と判断。評価への影響は小さい可能性。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (NPI-X関連)
            *   関連するプロトコル箇所: Section 4.3.1
    *   **確認事項No.:** I-4 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 選択/除外基準確認に必要なCNS imaging結果、Folate値、Syphilis screening結果がデータに含まれていない。医療機関のソースドキュメント等で適格性が確認されているか、内部で確認する。他の主要な基準は満たしているため、影響は限定的と判断。
        *   **判断理由:** 適格性確認は重要だが、他のデータから大きな問題は示唆されず、記録上の問題の可能性もあるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: DM, LB, MHドメイン
            *   関連するプロトコル箇所: Section 3.4.2.1, 3.4.2.2
    *   **確認事項No.:** I-5 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 同意取得日(RFICDTC)がデータに記録されていない。治験手順開始前に同意が取得されていることをソースドキュメント等で確認する。参加者の権利保護の観点から記録は必要だが、手続き自体は適切に行われている可能性が高いと判断し内部確認とする。
        *   **判断理由:** 同意取得は必須だが、記録上の問題の可能性が高く、内部での確認が可能と判断。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC
            *   関連するプロトコル箇所: Section 5.1
    *   **確認事項No.:** I-6 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 6 (AMBUL ECG REMOVAL) が予定日(Day 30)からDay 46へ大幅に遅延した理由について、可能であれば医療機関記録等で確認する。主要評価Visitではないため影響は小さいと判断。
        *   **判断理由:** スケジュール逸脱だが、主要評価への影響は小さく、内部確認で十分と判断。
        *   **判断根拠:**
            *   関連するデータ: SVドメイン (VISITNUM=6), TVドメイン (VISITNUM=6)
            *   関連するプロトコル箇所: Attachment LZZT.1

---

# 01-701-1097のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    68歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2005年9月22日発症、Primary Diagnosis）、失神（2013年1月1日発症、Significant Pre-existing Condition, Mild）、変形性膝関節症（Gonarthritis、Significant Pre-existing Condition, Mild）、副鼻腔炎（Sinusitis、Significant Pre-existing Condition, Mild）、歯肉炎（Gingivitis、2013年4月発症、Historical Diagnosis）、歯肉手術（Gingival Operation、2013年4月実施、Historical Diagnosis）が報告されている。治験薬初回投与は2014年1月1日、最終投与は2014年7月9日であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年12月23日|Day -9 (SCREENING 1)|Screening実施。Sodium 134 mmol/L (基準値 135-145, LOW)。MMSE 10点 (Inclusion Criteria [3] 10-23を満たす)。Hachinski Ischemic Score 1点 (Inclusion Criteria [4] <=4を満たす)。|
|2014年01月01日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg/day (Low Dose) 投与開始。ADAS-Cog(11) Total Score: 56.7。NPI-X Total Score: 4。|
|2014年01月03日|Day 3 (N/A)|有害事象「ERYTHEMA」(紅斑) 発現 (Mild, Possible)。|
|2014年01月15日|Day 15 (WEEK 2)|有害事象「ERYTHEMA」継続中。|
|2014年01月29日|Day 29 (WEEK 4)|Pulse Rate (Supine) 50 beats/min (ベースライン 60 bpm から低下、徐脈傾向)。Temperature 34.28 C (低体温、測定エラーの可能性も考慮)。|
|2014年02月11日|Day 42 (WEEK 6)|NPI-X Total Score: 3。|
|2014年02月20日|Day 51 (N/A)|有害事象「PRURITUS GENERALISED」(全身性そう痒症) 発現 (Moderate, Possible)。有害事象「APPLICATION SITE VESICLES」(適用部位小水疱) 発現 (Mild, Probable)。併用薬 HYDROCORTISONE (Topical) 投与開始 (QD)。|
|2014年02月21日|Day 52 (N/A)|有害事象「APPLICATION SITE PRURITUS」(適用部位そう痒症) 発現 (Mild, Possible)。|
|2014年02月22日|Day 53 (N/A)|有害事象「APPLICATION SITE VESICLES」回復。|
|2014年02月25日|Day 56 (N/A)|併用薬 HYDROCORTISONE (Topical, QD) 投与終了。|
|2014年02月26日|Day 57 (WEEK 8)|Eosinophils 0.89 GI/L (基準値 0-0.57, HIGH)。Pulse Rate (Supine) 54 beats/min (低値継続)。ADAS-Cog(11) Total Score: 54。CIBIC+: Minimal Improvement (3)。NPI-X Total Score: 2。有害事象「PRURITUS GENERALISED」回復。有害事象「APPLICATION SITE PRURITUS」継続中。|
|2014年03月21日|Day 80 (N/A)|有害事象「PRURITUS GENERALISED」再発 (Moderate, Possible)。併用薬 HYDROCORTISONE (Topical) 投与開始 (QD)。|
|2014年03月23日|Day 82 (N/A)|併用薬 HYDROCORTISONE (Topical, QD) 投与終了。|
|2014年03月26日|Day 85 (WEEK 12)|Eosinophils 0.87 GI/L (基準値 0-0.57, HIGH)。Lymphocytes 3.13 GI/L (基準値 0.8-3, HIGH)。NPI-X Total Score: 4。有害事象「PRURITUS GENERALISED」回復。有害事象「APPLICATION SITE PRURITUS」継続中。|
|2014年03月31日|Day 90 (N/A)|有害事象「PRURITUS GENERALISED」再発 (Moderate, Possible)。|
|2014年04月09日|Day 99 (WEEK 14 (T))|NPI-X Total Score: 1。|
|2014年04月18日|Day 108 (N/A)|併用薬 HYDROCORTISONE (Topical) 投与開始 (QD)。|
|2014年04月19日|Day 109 (N/A)|有害事象「PRURITUS GENERALISED」再発 (Moderate, Possible)。有害事象「PHARYNGOLARYNGEAL PAIN」(咽喉頭痛) 発現 (Mild, None)。有害事象「NASAL CONGESTION」(鼻閉) 発現 (Mild, None)。|
|2014年04月20日|Day 110 (N/A)|有害事象「PRURITUS GENERALISED」回復。|
|2014年04月22日|Day 112 (N/A)|有害事象「PHARYNGOLARYNGEAL PAIN」「NASAL CONGESTION」回復。併用薬 HYDROCORTISONE (Topical, QD) 投与終了。|
|2014年04月23日|Day 113 (WEEK 16)|ADAS-Cog(11) Total Score: 49。CIBIC+: No Change (4)。NPI-X Total Score: 0。有害事象「APPLICATION SITE PRURITUS」継続中。|
|2014年05月07日|Day 127 (WEEK 18 (T))|NPI-X Total Score: 1。|
|2014年05月21日|Day 141 (WEEK 20)|Diastolic BP (Standing, 1 min) 58 mmHg, (Standing, 3 min) 61 mmHg (ベースラインから低下、起立性低血圧の可能性)。Systolic BP (Standing, 1 min) 112 mmHg, (Standing, 3 min) 115 mmHg (ベースラインから低下、起立性低血圧の可能性)。NPI-X Total Score: 6 (悪化)。有害事象「APPLICATION SITE PRURITUS」が Moderate に悪化。|
|2014年05月23日|Day 143 (N/A)|併用薬 HYDROCORTISONE (Topical) 投与開始 (PRN)。|
|2014年06月04日|Day 155 (WEEK 22 (T))|NPI-X Total Score: 6 (悪化継続)。|
|2014年06月18日|Day 169 (WEEK 24)|ADAS-Cog(11) Total Score: 51。CIBIC+: Minimal Improvement (3)。NPI-X Total Score: 0 (改善)。有害事象「APPLICATION SITE PRURITUS」継続中 (Moderate)。|
|2014年07月09日|Day 190 (WEEK 26)|治験終了 (COMPLETED)。Creatinine 141.44 umol/L (基準値 71-141, 上限値)。Pulse Rate (Supine) 58 beats/min (低値継続)。NPI-X Total Score: 2。有害事象「ERYTHEMA」「APPLICATION SITE PRURITUS」継続中。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 既往歴として失神（Loss of consciousness）が2013年1月1日に報告されている。Screening Visit 1 (2013年12月23日) 時点で過去5年以内であり、プロトコル除外基準[15]「A history of syncope within the last 5 years.」に抵触する可能性が高い。不適格な患者が組み入れられた可能性があり、参加者の安全性リスク（特に本試験で徐脈や起立性低血圧傾向が見られるため）およびデータの妥当性に影響を与える。
        *   **根拠:** プロトコル除外基準[15]、MHドメインのデータ。失神既往は心血管系イベントのリスク因子であり、特に徐脈等を誘発する可能性のある薬剤投与下ではリスクが高まるという一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS (PASSED OUT)'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2013-01-01'
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2014-01-01'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 治験薬投与開始後、皮膚関連の有害事象（紅斑、全身性そう痒症、適用部位小水疱、適用部位そう痒症）が頻発している。特に適用部位そう痒症は持続し、Day 141には軽度から中等度に悪化している。Day 57およびDay 85には好酸球増多（基準値上限の約1.5倍）も認められており、治験薬に対するアレルギー反応の可能性が示唆される。Hydrocortisone外用薬が使用されているが、適用部位そう痒症は持続している。プロトコル 3.9.3.4 には皮膚反応と好酸球増多に関する記載があり、既知の事象と考えられるが、持続・悪化している点、および好酸球増多のフォローアップ状況について確認が必要。
        *   **根拠:** AEドメイン、LBドメイン（Eosinophils）、CMドメイン（Hydrocortisone）のデータ。プロトコル 3.9.3.4。薬剤性皮膚反応および好酸球増多に関する一般的な医学知識。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', 'PRURITUS GENERALISED', 'APPLICATION SITE VESICLES', 'APPLICATION SITE PRURITUS'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD', 'MODERATE'
            *   [Causality(AE.AEREL)] = 'POSSIBLE', 'PROBABLE'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'EOS'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.89 (Day 57), 0.87 (Day 85)
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 0.57
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** ベースライン時から脈拍数はやや低め（59-66 bpm）だが、治験薬投与中にさらに低下し、Day 29には50 bpmを記録している。その後も50 bpm台で推移している。プロトコル除外基準[16b]ではScreening時の徐脈（<=50 bpm）は除外対象。治療期間中の徐脈は安全性懸念であり、特に失神既往歴（M-1）のある本症例ではリスクが高い可能性がある。徐脈に関連する症状（めまい、ふらつき、失神等）の有無を確認する必要がある。また、プロトコル 3.9.4 に記載されているDSMBのレビュー対象となる可能性や、ECGモニタリングの結果との関連を確認する必要がある。
        *   **根拠:** VSドメイン（Pulse Rate）のデータ。プロトコル除外基準[16b]、安全性モニタリング計画（3.9.4）。徐脈の臨床的意義とリスクに関する一般的な医学知識。失神既往歴（M-1）との関連。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 50 (Day 29), 54 (Day 57), 58 (Day 85), 67 (Day 113), 61 (Day 141), 65 (Day 169), 58 (Day 190)
            *   [Baseline Flag(VS.VSBLFL)] = 'Y' (Day 1: 60 bpm)
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Week 20 (Day 141) のバイタルサイン測定時に、立位での血圧低下（臥位→立位1分で収縮期 -9 mmHg, 拡張期 -9 mmHg）が見られ、起立性低血圧の可能性が示唆される。他のVisitでは顕著な低下は見られないため一過性の可能性もあるが、失神既往歴（M-1）や徐脈傾向（M-3）を考慮すると注意が必要。関連する症状（めまい、ふらつき等）の有無を確認することが望ましい。
        *   **根拠:** VSドメイン（SYSBP, DIABP）のデータ。起立性低血圧の定義と臨床的意義に関する一般的な医学知識。失神既往歴（M-1）、徐脈傾向（M-3）との関連。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', 'DIABP'
            *   [Visit Name(VS.VISIT)] = 'WEEK 20'
            *   [Study Day of Vital Signs(VS.VSDY)] = 141
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] (Supine/Standing 1min/Standing 3min): SYSBP=121/112/115, DIABP=67/58/61
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** Week 26 (Day 190) のクレアチニン値が141.44 umol/Lであり、基準値上限（141 umol/L）に達している。ベースライン（123.76 umol/L）と比較して上昇傾向が見られる。腎機能低下の初期兆候の可能性も否定できないため、臨床的な意義について評価が必要。
        *   **根拠:** LBドメイン（Creatinine）のデータ。クレアチニン値の臨床的意義に関する一般的な医学知識。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 141.44 (Day 190), 123.76 (Day -9, Baseline)
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 141
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** 有効性評価指標（ADAS-Cog(11), CIBIC+, NPI-X Total Score）の結果に一貫性が見られない。ADAS-Cog(11)とCIBIC+は改善傾向を示しつつも変動があり、NPI-X Total Scoreは特に変動が大きい（Week 20, 22で悪化後、Week 24でベースライン以下に改善）。DADの個々の項目でも改善と悪化が混在している。治験薬の効果が一様でない可能性、評価のばらつき、あるいは他の要因（例：併存疾患、併用薬の影響は考えにくい）の影響などが考えられる。結果の解釈には注意が必要。
        *   **根拠:** QSドメインのデータ。有効性評価指標の解釈に関する一般的な知識。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'NPTOT'
            *   関連するQSレコード

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** MHドメインで報告された失神（Loss of consciousness）の開始日（MHSTDTC = 2013-01-01）が、治験薬初回投与日（DM.RFSTDTC = 2014-01-01）から見て1年以内であり、Screening Visit 1 (SV.SVSTDTC = 2013-12-23) 時点ではプロトコル除外基準[15]（過去5年以内の失神）に抵触する可能性がある。適格性評価とデータ間の整合性に疑義がある。
        *   **根拠:** MH, DM, SV ドメインの日付データ間の比較。プロトコル除外基準[15]。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS (PASSED OUT)'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2013-01-01'
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2014-01-01'
            *   [Start Date/Time of Visit(SV.SVSTDTC)] for VISITNUM=1 is '2013-12-23'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 29) の体温測定値が 34.28 C (93.7 F) と低体温を示している。他のVisitでの測定値は正常範囲内であるため、一過性の現象か測定エラーの可能性がある。臨床的な意義は低いと考えられるが、念のため確認が望ましい。
        *   **根拠:** VSドメインのデータ。体温の正常範囲に関する一般的な医学知識。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'TEMP'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 34.28
            *   [Study Day of Vital Signs(VS.VSDY)] = 29
    *   **指摘No.:** D-3
        *   **重要度:** Critical
        *   **内容:** DMドメインの「Date/Time of Informed Consent (DM.RFICDTC)」が欠損している。同意取得は治験参加の基本要件であり、治験手順開始前に適切に取得されたかを確認できない。GCP遵守および参加者の権利保護の観点から重大な問題。
        *   **根拠:** DMドメインのデータ欠損。GCP原則、プロトコル 3.4.2.1 [6]。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、一部の既往歴（GONARTHRITIS, SINUSITIS）の開始日（MHSTDTC）が欠損している。病歴の完全性の観点からは記録が望ましいが、主要な評価への影響は限定的と考えられる。
        *   **根拠:** MHドメインのデータ欠損。
        *   **関連データ:**
            *   [Dictionary-Derived Term(MH.MHDECOD)] = 'GONARTHRITIS', 'SINUSITIS'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '' (欠損)
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** QSドメインにおいて、Baseline (Visit 3, Day 1) の ADAS-Cog の項目「WORD RECOGNITION (ACITM08)」の結果 (QSORRES, QSSTRESC, QSSTRESN) が欠損している。Total Score (ACTOT) は算出されているようだが、元データの欠損はデータの品質に関わる。ただし、他の時点でのデータは存在し、Total Scoreへの影響も限定的かもしれない。
        *   **根拠:** QSドメインのデータ欠損。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACITM08'
            *   [Visit Number(QS.VISITNUM)] = 3
            *   [Finding in Original Units(QS.QSORRES)] = '' (欠損)
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** LBドメインにおいて、Screening時に必須とされている Folate の検査結果が報告されていない。プロトコル除外基準[28b]の確認ができない。
        *   **根拠:** LBドメインのデータ欠損。プロトコル除外基準[28b]。
        *   **関連データ:**
            *   LBドメインに Folate (LBTESTCD='FOLATE'など) のレコードが存在しない。

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[15]「A history of syncope within the last 5 years.」への抵触。MHデータより、Screening Visit 1 (2013-12-23) の約1年前に失神の既往 (2013-01-01) があり、5年以内に該当する。不適格な患者が組み入れられた可能性があり、参加者の安全性（特に徐脈・起立性低血圧傾向あり）および試験結果の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [15]
        *   **根拠:** MHデータとScreening日の比較。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS (PASSED OUT)'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2013-01-01'
            *   [Start Date/Time of Visit(SV.SVSTDTC)] for VISITNUM=1 is '2013-12-23'
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **逸脱の可能性:** 同意取得プロセスの遵守に関する疑義。DM.RFICDTC（同意取得日時）が欠損しているため、治験手順開始（Screening Visit 1: 2013-12-23）前に適切に同意が取得されたか確認できない。GCPの基本要件であり、参加者の権利保護に関わる重大な逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent, Section 3.4.2.1 Inclusion Criteria [6]
        *   **根拠:** DMデータの欠損。GCP原則。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   [Start Date/Time of Visit(SV.SVSTDTC)] for VISITNUM=1 is '2013-12-23'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b]の確認不足。Screening時の Folate 検査結果が欠損しており、基準値内であるか確認できない。適格性評価が不完全である可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** LBデータの欠損。
        *   **関連データ:**
            *   LBドメインに Folate のレコードが存在しない。
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[27b]（臨床検査値異常）への抵触の可能性。Screening時のSodium値が134 mmol/Lであり、提供されたLBデータの基準値（135-145 mmol/L）からは低値である。プロトコルでは「Lilly Reference Range III を超える場合」を除外としているため、この基準値が Lilly Reference Range III と同じであれば抵触する。臨床的に意義なしと判断された可能性もあるが、確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** LBデータの値と基準値の比較。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM'
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 134 (Day -9)
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 135
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 145

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-2, D-3)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、「Date/Time of Informed Consent」の記録が欠損しています。治験手順開始前に適切に同意が取得されたことを確認するため、同意取得日時の記録をご提出ください。これは参加者の権利保護およびGCP遵守の観点から極めて重要です。
        *   **クエリ文面（英語）:** For subject 01-701-1097, the 'Date/Time of Informed Consent' (DM.RFICDTC) is missing. Please provide the record of the date and time of informed consent to confirm it was obtained prior to study procedures. This is critical for participant rights and GCP compliance.
        *   **判断理由:** 同意取得は治験参加の絶対条件であり、記録の欠損はGCP遵守および参加者の権利保護に関する重大な懸念事項であるため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   関連するプロトコル箇所: Section 5.1, Section 3.4.2.1 [6]
            *   関連する医学的知見/規制要件: GCP原則
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1, M-1, D-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、既往歴として「Reported Term for the Medical History」が「LOSS OF CONSCIOUSNESS (PASSED OUT)」、「Start Date/Time of Medical History Event」が「2013-01-01」と記録されています。Screening Visit 1は2013年12月23日であり、プロトコル除外基準[15]（過去5年以内の失神）に抵触する可能性があります。適格性評価について再確認し、コメントをお願いします。
        *   **クエリ文面（英語）:** For subject 01-701-1097, MH Term 'LOSS OF CONSCIOUSNESS (PASSED OUT)' with Start Date '2013-01-01' is recorded. Screening Visit 1 was on 2013-12-23. This may conflict with exclusion criterion [15] (syncope within 5 years). Please re-confirm eligibility and comment.
        *   **判断理由:** 除外基準抵触の可能性があり、参加者の安全性リスクおよびデータの妥当性に影響するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS (PASSED OUT)', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2013-01-01', [Start Date/Time of Visit(SV.SVSTDTC)] for VISITNUM=1 = '2013-12-23'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [15]
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、治験期間中に「Pulse Rate」が50 bpm (Day 29) を記録するなど、徐脈傾向が見られます。失神の既往歴もあるため、徐脈に関連する症状（めまい、ふらつき、失神感など）の有無について確認し、ご報告ください。また、プロトコル 3.9.4 に基づく安全性モニタリング（ECG等）の結果と合わせて臨床的な評価をお願いします。
        *   **クエリ文面（英語）:** Subject 01-701-1097 shows bradycardia trend (Pulse Rate 50 bpm on Day 29). Given the history of syncope, please confirm and report any related symptoms (dizziness, lightheadedness, syncope). Please provide clinical assessment considering safety monitoring results (ECG, etc.) per protocol 3.9.4.
        *   **判断理由:** 徐脈は潜在的な安全性リスクであり、特に失神既往のある患者では注意深い観察と評価が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 50 (Day 29), etc. [Reported Term for the Medical History(MH.MHTERM)] = 'LOSS OF CONSCIOUSNESS (PASSED OUT)'
            *   関連するプロトコル箇所: Section 3.9.4
            *   関連する医学的知見: 徐脈のリスク、失神との関連
    *   **クエリNo.:** Q-4 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、皮膚関連の有害事象（特に適用部位そう痒症）が持続・悪化し、好酸球増多も認められています。Hydrocortisoneが使用されていますが、「APPLICATION SITE PRURITUS」は継続中です。現在の症状管理状況と、今後の対応方針についてお知らせください。また、好酸球増多のフォローアップ状況についてもご教示ください。
        *   **クエリ文面（英語）:** Subject 01-701-1097 has persistent/worsening skin AEs (esp. application site pruritus) and eosinophilia. Hydrocortisone is used, but pruritus continues. Please report current symptom management, future plan, and eosinophilia follow-up status.
        *   **判断理由:** 持続・悪化する有害事象と検査値異常に対する適切な管理状況を確認し、参加者の安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: AE, LB (EOS), CM (HYDROCORTISONE) ドメインの関連レコード
            *   関連するプロトコル箇所: Section 3.9.3.4
            *   関連する医学的知見: 薬剤性皮膚反応、アレルギー反応の管理
    *   **クエリNo.:** Q-5 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Week 20 (Day 141) に立位での血圧低下が認められました。起立性低血圧に関連する症状（めまい、ふらつき等）の有無について確認し、ご報告ください。
        *   **クエリ文面（英語）:** For subject 01-701-1097, postural hypotension was suggested on Week 20 (Day 141). Please confirm and report if any related symptoms (e.g., dizziness, lightheadedness) occurred.
        *   **判断理由:** 一過性の可能性もあるが、失神既往や徐脈傾向を考慮し、症状の有無を確認するため。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (Day 141 SYSBP, DIABP)
            *   関連する医学的知見: 起立性低血圧の症状
    *   **クエリNo.:** Q-6 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Week 26 (Day 190) の「Creatinine」が基準値上限 (141.44 umol/L) となっています。ベースラインからの上昇も見られます。このクレアチニン値上昇の臨床的意義について評価をお願いします。
        *   **クエリ文面（英語）:** For subject 01-701-1097, Creatinine level was at the upper limit of normal (141.44 umol/L) on Week 26 (Day 190), increased from baseline. Please assess the clinical significance of this finding.
        *   **判断理由:** 腎機能低下の可能性を評価するため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 141.44 (Day 190)
            *   関連する医学的知見: クレアチニン値と腎機能
    *   **クエリNo.:** Q-7 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Week 4 (Day 29) の「Temperature」が 34.28 C と記録されています。測定値が正しいか、あるいは測定エラーの可能性がないかご確認ください。
        *   **クエリ文面（英語）:** For subject 01-701-1097, Temperature was recorded as 34.28 C on Week 4 (Day 29). Please confirm if this value is correct or if there was a measurement error.
        *   **判断理由:** 異常値の正確性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'TEMP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 34.28 (Day 29)
    *   **クエリNo.:** Q-8 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Baseline (Visit 3) の ADAS-Cog の項目「Question Short Name」が「ACITM08」(WORD RECOGNITION) の結果が欠損しています。欠損理由についてご確認ください。
        *   **クエリ文面（英語）:** For subject 01-701-1097, the result for ADAS-Cog item 'ACITM08' (WORD RECOGNITION) at Baseline (Visit 3) is missing. Please clarify the reason for the missing data.
        *   **判断理由:** データの完全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSTESTCD='ACITM08', VISITNUM=3)
    *   **クエリNo.:** Q-9 (関連指摘No.: P-3, D-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Screening時に実施必須とされている Folate の検査結果が報告されていません。結果をご提出ください。
        *   **クエリ文面（英語）:** For subject 01-701-1097, the result for the Folate test required at Screening is missing. Please provide the result.
        *   **判断理由:** プロトコルで規定された適格性確認に必要な検査結果が欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインに Folate のレコードなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]
    *   **クエリNo.:** Q-10 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1097について、Screening時 (Day -9) の「Sodium」が 134 mmol/L と記録されており、提供された基準値 (135-145 mmol/L) では低値です。プロトコル除外基準[27b]（Lilly Reference Range III を超える検査値）への抵触有無について、臨床的意義の評価を含めて再確認し、コメントをお願いします。
        *   **クエリ文面（英語）:** For subject 01-701-1097, Sodium level at Screening (Day -9) was 134 mmol/L, which is low according to the provided reference range (135-145 mmol/L). Please re-confirm if this meets exclusion criterion [27b] (value exceeding Lilly Reference Range III), including clinical significance assessment.
        *   **判断理由:** 除外基準抵触の可能性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 134 (Day -9)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価指標（ADAS-Cog(11), CIBIC+, NPI-X Total Score, DAD項目）の結果に一貫性が見られない。特にNPI-X Total Scoreの変動が大きい。治験薬の効果が一様でない可能性や評価のばらつきが考えられる。最終的な有効性評価の際には、これらの変動要因を考慮する必要があるため、内部で記録・共有する。個別のデータポイントに問題があるわけではなく、医療機関への問い合わせは不要と判断。
        *   **判断理由:** データ自体に誤りがあるわけではなく、結果の解釈に関する内部での検討事項であるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメインの有効性評価データ
    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインにおいて、一部の既往歴（GONARTHRITIS, SINUSITIS）の開始日（MHSTDTC）が欠損している。これらの既往歴は主要評価項目や安全性評価への直接的な影響は小さいと考えられ、医療機関への問い合わせは不要と判断。データクリーニングプロセスの一環として記録する。
        *   **判断理由:** 欠損データが試験の主要な評価に与える影響は限定的と判断されるため。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン (MHDECOD='GONARTHRITIS', 'SINUSITIS', MHSTDTC='')

---

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
81歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2009年発症、PRIMARY DIAGNOSIS）、高血圧、骨粗鬆症、甲状腺機能低下症（いずれもSIGNIFICANT PRE-EXISTING CONDITION）が報告されている。教育レベルは22年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年08月25日|Day -13 (SCREENING 1)|スクリーニング評価実施。MMSE 23点、Hachinskiスコア 1点。ベースライン検査値: Erythrocytes (RBC) が 3.80 TI/L (基準値 3.9-5.5) で軽度低値。他は基準値内。併用薬としてKEFLEX, LISINOPRIL, MOTRIN, PREMARIN, PROVERA, SYNTHROIDを服用中。|
|2012年09月02日|Day -5 (N/A)|有害事象「ERYTHEMA」(紅斑, MILD)、「PRURITUS」(掻痒感, MILD) 発現。併用薬「HYDROCORTISONE, TOPICAL」開始。|
|2012年09月04日|Day -3 (N/A)|併用薬「HYDROCORTISONE, TOPICAL」終了。|
|2012年09月05日|Day -2 (SCREENING 2)|バイタルサイン測定。|
|2012年09月07日|Day 1 (BASELINE)|治験薬「XANOMELINE」54 mg (PATCH, QD) 投与開始。有害事象「ERYTHEMA」、「PRURITUS」が回復/解決。有害事象「MICTURITION URGENCY」(尿意切迫, MILD) 発現。ADAS-Cog(11) Subscore = 7。NPI-X (9) Total Score = 2。|
|2012年09月13日|Day 7 (N/A)|有害事象「ARTHRALGIA」(関節痛, MODERATE)、「CELLULITIS」(蜂窩織炎, MODERATE) 発現。|
|2012年09月16日|Day 10 (N/A)|治験薬「XANOMELINE」投与終了。|
|2012年09月17日|Day 11 (WEEK 2)|有害事象により試験中止。有害事象「ARTHRALGIA」、「CELLULITIS」、「MICTURITION URGENCY」は未回復。検査値: Ery. Mean Corpuscular Volume (MCV) が 101 fL (基準値 80-100) で高値、Erythrocytes (RBC) が 3.70 TI/L (基準値 3.9-5.5) で低値、Specific Gravity (SPGRAV) が 1.004 (基準値 1.006-1.03) で低値、Anisocytes (ANISO) が 1 (ABNORMAL)。ADAS-Cog(11) Subscore = 5。NPI-X (9) Total Score = 1。CIBIC+ = 4 (No Change)。|
|2012年09月29日|Day 23 (AE FOLLOW-UP)|有害事象フォローアップ Visit 実施。|
|2013年02月22日|Day 169 (RETRIEVAL)|Retrieval Visit 実施。ADAS-Cog(11) Subscore = 9。NPI-X (9) Total Score = 45。CIBIC+ = 5 (Minimal worsening)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 11に有害事象により試験中止となっているが、中止の直接原因となったAEの詳細が不明確。RELRECでは関節痛 (ARTHRALGIA, MODERATE, Day 7発現) が関連付けられているが、同日に蜂窩織炎 (CELLULITIS, MODERATE) も発現している。蜂窩織炎は中等度の感染症であり、治験薬との関連性評価 (AEREL=NONE) の妥当性、部位、治療内容、転帰（未回復）の詳細な評価が必要。入院の必要性など重篤性の評価も再確認が必要（AESER='N'）。尿意切迫 (MICTURITION URGENCY, MILD, Day 1発現) も未回復。これらのAEと治験薬 (Xanomeline: コリン作動薬) との関連性について医学的な再評価が推奨される。特に貼付剤による皮膚関連AE (紅斑、掻痒感、蜂窩織炎) が見られており、プロトコルでも注意喚起されているため、皮膚忍容性に関する懸念がある。
        *   **根拠:** 参加者の安全性評価の妥当性、早期中止理由の明確化、治験薬の安全性プロファイル評価のため。コリン作動薬の既知の副作用プロファイル、プロトコル 3.9.3.4 (Rash/Eosinophiliaの記載)。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 11
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ARTHRALGIA', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 7, [Causality(AE.AEREL)] = 'NONE', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'CELLULITIS', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Study Day of Start of Adverse Event(AE.AESTDY)] = 7, [Causality(AE.AEREL)] = 'NONE', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MICTURITION URGENCY', [Severity/Intensity(AE.AESEV)] = 'MILD', [Study Day of Start of Adverse Event(AE.AESTDY)] = 1, [Causality(AE.AEREL)] = 'NONE', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Related Records(RELREC)] linking DSSEQ=1 to AESEQ=7
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Day 11の検査で軽度の貧血傾向（MCV高値、RBC低値、赤血球大小不同症）が認められる。ベースラインでもRBCは低値であり、急激な変化ではないが、臨床的な意義について評価が必要。
        *   **根拠:** 安全性モニタリングの観点。高齢女性であり、他の要因も考えられるが、治験薬の影響も完全に否定できないため。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 100, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 11
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.70, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.9, [Reference Range Indicator(LB.LBNRIND)] = 'LOW', [Study Day of Specimen Collection(LB.LBDY)] = 11
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '1', [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL', [Study Day of Specimen Collection(LB.LBDY)] = 11
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Retrieval Visit (Day 169) におけるNPI-Xスコアがベースライン(2点)やWeek 2(1点)と比較して著しく悪化(45点)している。これは治験中止後の疾患進行を反映している可能性が高いが、中止前のAE（関節痛、蜂窩織炎、尿意切迫）や中止自体が精神症状に影響を与えた可能性も考慮する必要がある。
        *   **根拠:** 有効性評価の解釈、疾患経過の理解。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 2, [Visit Name(QS.VISIT)] = 'BASELINE'
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 1, [Visit Name(QS.VISIT)] = 'WEEK 2'
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 45, [Visit Name(QS.VISIT)] = 'RETRIEVAL'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「ERYTHEMA」および「PRURITUS」について、複数のレコード（AESEQ 1, 2, 4, 5）が存在し、転帰の記録日（Visit 4, Day 11）と実際の終了日（AEENDTC = Day 1）に不整合が見られる。データの重複または記録誤りの可能性があり、クリーニングが必要。
        *   **根拠:** データ品質と一貫性の確保。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'ERYTHEMA', [Sequence Number(AE.AESEQ)] = 1, 4
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'PRURITUS', [Sequence Number(AE.AESEQ)] = 2, 5
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-09-07' (for AESEQ 1, 2, 4, 5)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED' (for AESEQ 4, 5 at Visit 4)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「LOCALISED INFECTION」(AESEQ=3) の開始日 (AESTDTC = 2012-07-08, Day -61) が治験開始 (RFSTDTC = 2012-09-07, Day 1) よりかなり前であり、既往歴 (MHSEQ=6) と同一事象の可能性がある。AEとしての記録が適切か確認が必要。
        *   **根拠:** データ品質と正確性の確保。AEとMHの区別。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'LOCALISED INFECTION', [Sequence Number(AE.AESEQ)] = 3, [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-07-08'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1224', [Dictionary-Derived Term(MH.MHDECOD)] = 'LOCALISED INFECTION', [Sequence Number(MH.MHSEQ)] = 6
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 併用薬 (CM) ドメインにおいて、標準化薬剤名 (CMDECOD) および薬剤クラス (CMCLAS) が多くの薬剤で 'UNCODED' となっている。また、適応症 (CMINDC) が全件欠損、一部薬剤で投与頻度 (CMDOSFRQ) が欠損している。データの完全性と標準化が必要。
        *   **根拠:** データ品質、標準化、および後続の解析のため。
        *   **関連データ:**
            *   CMドメインの複数レコード ([Standardized Medication Name(CM.CMDECOD)], [Medication Class(CM.CMCLAS)], [Indication(CM.CMINDC)], [Dosing Frequency per Interval(CM.CMDOSFRQ)])
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 有害事象 (AE) ドメインにおいて、治験薬との関連性 (AEREL) が 'NONE' と記録されている。Define.xmlのコードリストには存在するが、一般的に使用される 'NOT RELATED' 等とは異なる。コードの意味合いを確認し、必要であれば修正またはコードリストの明確化が必要。
        *   **根拠:** データ品質と解釈の明確化。
        *   **関連データ:**
            *   AEドメインの複数レコード ([Causality(AE.AEREL)] = 'NONE')
            *   Define.xml CodeList OID="AECAUS"
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。治験手順開始前に適切な同意が得られたか確認できない。
        *   **根拠:** GCP遵守、参加者の権利保護。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** 選択/除外基準の確認に必要な情報が一部不足している。
            *   選択基準[5] CNS imagingの結果がデータに含まれていない。
            *   除外基準[16b] ECG at screeningの結果がデータに含まれていない。
            *   除外基準[28b] Folateの検査結果がデータに含まれていない。
            *   除外基準[29b] Syphilis screeningの結果がデータに含まれていない。
            これらの基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5], Section 3.4.2.2 [16b], [28b], [29b]
        *   **根拠:** 適格性確認の完全性。データの欠損。
        *   **関連データ:**
            *   関連するLBレコード、ECGレコードの欠損
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[14] Mental illness within 5 years に関して、MHに Eating disorder (2009年発症) が記録されている。これが除外基準に該当しないと判断された根拠が不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [14]
        *   **根拠:** 適格性確認の明確化。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0702', [Dictionary-Derived Term(MH.MHDECOD)] = 'EATING DISORDER', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '2009'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[27b] Lab values exceeding range に関して、Screening時のRBCが基準値をわずかに下回っていた。これが臨床的に問題ないと判断された根拠が不明確（プロトコル上、医師判断で許容される可能性はある）。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** 適格性確認の明確化。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'RBC', [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 3.80, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.9, [Study Day of Specimen Collection(LB.LBDY)] = -13
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が欠損しており、治験手順開始前に同意が適切に取得されたか確認できない。GCP違反の可能性。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** GCP遵守、参加者の権利保護。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者(01-701-1111)はStudy Day 11に有害事象により試験を中止されました。中止に関連する有害事象として、Study Day 7に発現した「関節痛」（中等度）および「蜂窩織炎」（中等度）が記録されています。これらの事象について、特に蜂窩織炎の部位、臨床経過、実施された治療、治験薬との関連性評価（「関連なし」と記録されています）の根拠、および重篤性（入院の要否など）について詳細をお知らせください。また、Study Day -61に発現したとされる「局所感染」がDay 11にAEとして記録されていますが、これは既往歴の再発でしょうか、あるいは別の事象でしょうか？ 詳細をご教示ください。
        *   **クエリ文面（英語）:** Subject 01-701-1111 discontinued the study on Day 11 due to an AE. AEs 'Arthralgia' (Moderate, onset Day 7) and 'Cellulitis' (Moderate, onset Day 7) are recorded around this time. Please provide details, especially for Cellulitis: site, clinical course, treatment, basis for causality assessment ('NONE' recorded), and seriousness (e.g., hospitalization). Also, 'Localised Infection' (onset Day -61) was recorded as an AE on Day 11. Was this a recurrence of MH or a new event? Please clarify.
        *   **判断理由:** 参加者の安全性評価の妥当性確認、早期中止理由の明確化、および治験薬の安全性プロファイル評価のため。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='ADVERSE EVENT', DS.DSSTDY=11, AE.AETERM='ARTHRALGIA', AE.AESEV='MODERATE', AE.AESTDY=7, AE.AEREL='NONE', AE.AEOUT='NOT RECOVERED/NOT RESOLVED', AE.AETERM='CELLULITIS', AE.AESEV='MODERATE', AE.AESTDY=7, AE.AEREL='NONE', AE.AEOUT='NOT RECOVERED/NOT RESOLVED', AE.AETERM='LOCALISED INFECTION', AE.AESTDTC='2012-07-08'
            *   関連するプロトコル箇所: Section 3.9.3.2 (Adverse Events), Section 3.10.1 (Discontinuations)
            *   関連する医学的知見: 蜂窩織炎は重篤化しうる感染症であり、適切な評価と管理が必要。貼付剤と皮膚感染症の関連。
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1, P-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者(01-701-1111)の適格性確認について、以下の点の情報をご提供ください。1) 選択基準[5]を満たすCNS imagingの結果。2) 除外基準[16b]に該当するスクリーニングECG所見がなかったことの確認。3) 除外基準[28b]を満たすFolate検査結果。4) 除外基準[29b]を満たすSyphilis screening結果。5) 除外基準[27b]について、スクリーニング時の赤血球数が基準値を下回っていましたが、臨床的に問題ないと判断された根拠。
        *   **クエリ文面（英語）:** Regarding eligibility confirmation for Subject 01-701-1111, please provide: 1) CNS imaging results confirming Inclusion Criterion [5]. 2) Confirmation that screening ECG met Exclusion Criterion [16b]. 3) Folate test result confirming Exclusion Criterion [28b]. 4) Syphilis screening result confirming Exclusion Criterion [29b]. 5) Rationale for deeming the screening RBC count (below lower limit) clinically insignificant per Exclusion Criterion [27b].
        *   **判断理由:** プロトコル遵守（適格性基準）の確認、およびデータの完全性確保のため。
        *   **判断根拠:**
            *   関連するデータ: 関連データの欠損 (CNS imaging, ECG, Folate, Syphilis), LB.LBTESTCD='RBC', LB.LBSTRESN=3.80, LB.LBNRIND='LOW' (Day -13)
            *   関連するプロトコル箇所: Section 3.4.2.1 [5], Section 3.4.2.2 [16b], [27b], [28b], [29b]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-4, D-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者(01-701-1111)の同意取得日（Date/Time of Informed Consent）が記録されていません。治験手順開始前に適切に同意が取得されたことを確認するため、同意取得日時をお知らせください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (DM.RFICDTC) for Subject 01-701-1111 is missing. To confirm that consent was obtained prior to study procedures, please provide the date and time of informed consent.
        *   **判断理由:** GCP遵守および参加者の権利保護の確認のため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC = '' (欠損)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
            *   関連する医学的知見: GCPの基本原則

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「ERYTHEMA」および「PRURITUS」について、重複記録の可能性と転帰記録日との不整合がある。データを確認し、必要に応じて修正する。参加者の安全性や評価への影響は小さいと判断されるが、データ品質維持のため確認・修正を行う。
        *   **判断理由:** データ品質と一貫性の確保。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ 1, 2, 4, 5), AE.AETERM, AE.AEENDTC, AE.AEOUT
    *   **確認事項No.:** I-2 (関連指摘No.: D-3, D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインの標準化（CMDECOD, CMCLAS）、欠損値（CMINDC, CMDOSFRQ）、およびAEドメインの関連性コード（AEREL='NONE'）について、コーディング規約やデータ標準を確認し、必要に応じて修正・標準化を行う。参加者の安全性や評価への直接的な影響は小さいが、データ品質と解析の準備のため対応が必要。
        *   **判断理由:** データ品質、標準化、および後続の解析のため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン、AEドメイン、Define.xml
    *   **確認事項No.:** I-3 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 本症例で見られた軽度の貧血傾向（RBC低値、MCV高値）について、他の症例データも確認し、治験薬との関連を示唆するシグナルがないか評価する。本症例のみでは臨床的意義は低いと判断されるが、集団としての傾向を確認する。
        *   **判断理由:** 安全性シグナルの探索。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='RBC', 'MCV', 'ANISO')
    *   **確認事項No.:** I-4 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 本症例で見られた皮膚関連AE（紅斑、掻痒感、蜂窩織炎）について、他の症例データも確認し、治験薬（貼付剤）との関連を示唆するシグナルがないか評価する。プロトコルでも言及されており、重要な安全性評価項目である。
        *   **判断理由:** 安全性シグナルの評価、治験薬のリスク評価。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='ERYTHEMA', 'PRURITUS', 'CELLULITIS')
            *   関連するプロトコル箇所: Section 3.9.3.4

---

# 01-701-1118のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
52歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2010年06月24日発症、PRIMARY DIAGNOSIS）、痔核（MILD）、頭痛（MODERATE）、消化不良（MILD）、遠視（MILD）、副鼻腔炎（MILD）（いずれもSIGNIFICANT PRE-EXISTING CONDITION）、手首骨折（1991年）、気胸（1988年）（いずれもHISTORICAL DIAGNOSIS）が報告されている。また、有害事象として咳（MILD、2003年発症、未回復）が報告されている（治療期間外イベント）。教育歴は14年。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2014年02月27日|Day -13 (SCREENING 1)|MMSEスコア 20点。Hachinski Ischemic Scaleスコア 1点。身長 180.34 cm、体重 71.67 kg。バイタルサイン、臨床検査値は概ね正常範囲内。|
|2014年03月10日|Day -2 (SCREENING 2)|バイタルサイン測定。|
|2014年03月12日|Day 1 (BASELINE)|治験薬（Placebo）投与開始。体重 71.22 kg。ADAS-Cog(11) Total Score 26点。NPI-X Total Score 0点。DAD 各項目=1。|
|2014年03月25日|Day 14 (AMBUL ECG PLACEMENT)|バイタルサイン測定。|
|2014年03月26日|Day 15 (WEEK 2)|体重 71.22 kg。NPI-X Total Score 0点。|
|2014年04月09日|Day 29 (WEEK 4)|体重 71.22 kg。NPI-X Total Score 0点。|
|2014年04月11日|Day 31 (AMBUL ECG REMOVAL)|バイタルサイン測定。|
|2014年04月23日|Day 43 (WEEK 6)|体重 71.22 kg。NPI-X Total Score 0点。|
|2014年05月08日|Day 58 (WEEK 8)|体重 72.58 kg (+1.36kg from Baseline)。ADAS-Cog(11) Total Score 19点 (改善)。CIBIC+ Score 4 (No Change)。DAD 各項目=1。NPI-X Total Score 0点。|
|2014年05月21日|Day 71 (WEEK 10 (T))|NPI-X Total Score 0点。|
|2014年06月05日|Day 86 (WEEK 12)|体重 73.48 kg (+2.26kg from Baseline)。CIBIC+ Score 7 (Marked Worsening)。DAD 各項目=1。NPI-X Total Score 0点。(ADAS-Cog(11) Total Score データなし)|
|2014年06月18日|Day 99 (WEEK 14 (T))|NPI-X Total Score 0点。|
|2014年07月02日|Day 113 (WEEK 16)|体重 73.03 kg (+1.81kg from Baseline)。ADAS-Cog(11) Total Score 17点 (改善)。CIBIC+ Score 1 (Marked Improvement)。DAD 各項目=1。NPI-X Total Score 0点。|
|2014年07月13日|Day 124 (WEEK 22 (T))|NPI-X Total Score 0点。(Visit実施日が予定日より早い)|
|2014年07月16日|Day 127 (WEEK 18 (T))|NPI-X Total Score 0点。|
|2014年07月30日|Day 141 (WEEK 20)|体重 71.67 kg (Baselineと同等)。収縮期血圧(立位1分後) 154 mmHg、体温 37.67 C (一過性の軽度上昇か)。DAD 各項目=1。NPI-X Total Score 0点。(ADAS-Cog(11) Total Score データなし)|
|2014年08月27日|Day 169 (WEEK 24)|体重 71.22 kg (Baselineと同等)。ADAS-Cog(11) Total Score 15点 (改善)。CIBIC+ Score 7 (Marked Worsening)。DAD 各項目=1。NPI-X Total Score 0点。|
|2014年09月09日|Day 182 (WEEK 26)|治験薬（Placebo）投与終了。体重 73.03 kg (+1.81kg from Baseline)。NPI-X Total Score 0点。治験完了 (COMPLETED)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 主要評価項目の一つであるCIBIC+の評価結果が、Week 8 (No Change), Week 12 (Marked Worsening), Week 16 (Marked Improvement), Week 24 (Marked Worsening)と大きく変動しており、一貫性に欠ける。特にWeek 16の著明改善とWeek 12/24の著明悪化の乖離が大きい。Placebo群であることを考慮すると、評価者間のばらつき、評価基準解釈の揺れ、あるいは患者の状態の実際の変動などが考えられるが、他のデータ（ADAS-CogやNPI-X）ではこの変動を裏付ける所見は乏しい。主要評価項目の信頼性に影響を与える可能性がある。
        *   **根拠:** CIBIC+は主要評価項目であり、その評価の信頼性は試験結果の解釈に不可欠である。大きな変動は評価の妥当性への疑問を生じさせる。一般的な臨床経過としても、短期間での著明改善と著明悪化の繰り返しは説明が難しい場合がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC'
            *   [Visit Number(QS.VISITNUM)] = 8, [Character Result/Finding in Std Format(QS.QSSTRESC)] = '4'
            *   [Visit Number(QS.VISITNUM)] = 12, [Character Result/Finding in Std Format(QS.QSSTRESC)] = '7'
            *   [Visit Number(QS.VISITNUM)] = 10, [Character Result/Finding in Std Format(QS.QSSTRESC)] = '1' (Visit 10 = Week 16)
            *   [Visit Number(QS.VISITNUM)] = 12, [Character Result/Finding in Std Format(QS.QSSTRESC)] = '7' (Visit 12 = Week 24)
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 8, 10, 12 (継続的な改善傾向)
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 3, 4, 5, 7, 8, 8.1, 9, 9.1, 10, 10.1, 11, 11.1, 12, 13 (常に0)
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 有害事象として報告されている「COUGH」の開始日が2003年であり、治験開始（2014年）よりかなり前である。SUPPAEのAETRTEMフラグも'N'であり、治療期間外のイベントである。これは既往歴（Medical History）として扱うべきデータと考えられる。
        *   **根拠:** AEドメインは通常、治験期間中に発現または悪化した事象を記録する。開始日が大幅に前であり、治療との関連がない事象はMHドメインが適切。データの帰属ドメインの問題であり、安全性評価への直接的な影響は小さい。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'COUGH'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2003'
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2014-03-12'
            *   [Qualifier Variable Name(SUPPAE.QNAM)] = 'AETRTEM', [Data Value(SUPPAE.QVAL)] = 'N'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** QSドメインのCIBIC+評価日（QSDTC）が、対応するVisitの実施日（SVSTDTC）と大きくずれている記録がある（例: Visit 8ではSVSTDTC='2014-05-08'に対しQSDTC='2014-07-08'）。評価がVisit時に行われていない可能性があり、評価の信頼性やプロトコル遵守（評価スケジュール）に影響する。
        *   **根拠:** プロトコルでは通常、評価は特定のVisitで実施される。評価日がVisit日と大幅に異なる場合、データの正確性や評価タイミングの妥当性に疑問が生じる。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC'
            *   [Visit Number(QS.VISITNUM)] = 8, [Date/Time of Finding(QS.QSDTC)] = '2014-07-08'
            *   [Visit Number(SV.VISITNUM)] = 8, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-05-08'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** DMドメインの同意取得日（RFICDTC）が欠損している。同意取得日と治験手順開始日の前後関係を確認できず、GCP遵守の観点から問題となる可能性がある。
        *   **根拠:** 同意取得は治験参加の基本であり、治験関連手順開始前に適切に行われている必要がある。同意日の記録欠損は、その確認を不可能にする。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** Visit 11.1 (WEEK 22 (T))について、SVドメインのVisit開始日(SVSTDTC='2014-07-13')が、先行するVisit 10.1 (WEEK 18 (T))のVisit開始日(SVSTDTC='2014-07-16')よりも前になっている。QSドメインの同Visitの評価日(QSDTC='2014-07-13')およびStudy Day(QSDY=124)はSVの日付と一致しているため、SVの日付が正しい可能性が高いが、Visit間の日付の逆転はデータ入力エラーまたは記録ミスの可能性を示唆する。
        *   **根拠:** Visitは通常時系列で進行するため、日付の逆転は論理的な不整合である。ただし、他のデータ（QS）との整合性から影響は限定的と考えられる。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 11.1, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-07-13'
            *   [Visit Number(SV.VISITNUM)] = 10.1, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-07-16'
            *   [Visit Number(QS.VISITNUM)] = 11.1, [Date/Time of Finding(QS.QSDTC)] = '2014-07-13', [Study Day of Finding(QS.QSDY)] = 124

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 主要評価項目であるCIBIC+の評価日が、プロトコルで規定されたVisit実施日と一致していない可能性がある（例: Visit 8）。評価スケジュールの逸脱に該当する可能性があり、評価の信頼性に影響を与えうる。
        *   **プロトコル該当箇所:** Section 3.9.1.1, Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** プロトコルでは評価は特定のVisitで実施されることが規定されている。評価日のずれはスケジュール逸脱の可能性を示唆する。
        *   **関連データ:** (D-1と同じ)
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC'
            *   [Visit Number(QS.VISITNUM)] = 8, [Date/Time of Finding(QS.QSDTC)] = '2014-07-08'
            *   [Visit Number(SV.VISITNUM)] = 8, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-05-08'
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 11.1 (WEEK 22 (T)) の実施日 (Day 124) が、予定されたStudy Day (VISITDY=154) から大きく逸脱している。Visit Windowからの逸脱の可能性がある。
        *   **プロトコル該当箇所:** Attachment LZZT.1 (Schedule of Events) - Visit Windowの許容範囲は明記されていないが、大幅なずれは逸脱とみなされる可能性がある。
        *   **根拠:** プロトコルで規定された評価スケジュールからの逸脱は、データの比較可能性や評価の信頼性に影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 11.1, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-07-13'
            *   [Planned Study Day of Visit(TV.VISITDY)] = 154 (TVドメインより)
            *   [Study Day of Finding(QS.QSDY)] = 124 (QSドメインより)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日（DM.RFICDTC）が欠損しているため、治験関連手順開始前に適切な同意が取得されたかを確認できない。GCP遵守違反の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** 同意取得は治験実施の必須要件であり、記録の欠損はコンプライアンス上の問題となる。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1, P-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor/CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1118について、主要評価項目であるCIBIC+の評価結果に大きな変動が見られます。Week 12とWeek 24の評価が「Marked Worsening (7)」である一方、Week 16の評価が「Marked Improvement (1)」となっています。この評価変動の理由と、評価の一貫性についてご確認ください。また、Week 8のCIBIC+評価日として記録されている「Date/Time of Finding」が「2014-07-08」であり、Visit実施日「2014-05-08」と約2ヶ月ずれています。評価がVisit時に実施されたか、日付記録が正しいかご確認ください。これらの点は主要評価項目の信頼性に関わるため、確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding patient 01-701-1118, significant fluctuations were observed in the CIBIC+ assessment, a primary endpoint. The score was '7' (Marked Worsening) at Week 12 and Week 24, but '1' (Marked Improvement) at Week 16. Please clarify the reason for this variability and confirm assessment consistency. Also, the CIBIC+ 'Date/Time of Finding' for Visit 8 is recorded as '2014-07-08', which differs significantly from the visit date '2014-05-08'. Please confirm if the assessment was performed during the visit and verify the date accuracy. Confirmation is needed due to the impact on primary endpoint reliability.
        *   **判断理由:** 主要評価項目であるCIBIC+の評価結果の変動が大きく、評価日にもずれが見られるため、評価の妥当性と信頼性を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD='CIBIC', QS.VISITNUM=8, 10, 12, QS.QSDTC, SV.SVSTDTC
            *   関連するプロトコル箇所: Section 2.1 (Primary Objectives), Section 3.9.1.1 (Efficacy Measures), Attachment LZZT.1 (Schedule of Events)
            *   関連する医学的知見: Placebo群における評価のばらつき、評価者間信頼性の問題。
    *   **クエリNo.:** Q-2 (関連指摘No.: D-2, P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1118について、「Date/Time of Informed Consent」が記録されていません。同意取得日と、治験関連の最初の手順が実施された日付を確認し、ご報告ください。GCP遵守の観点から、同意が手順開始前に適切に取得されていることの確認が必要です。
        *   **クエリ文面（英語）:** For patient 01-701-1118, the 'Date/Time of Informed Consent' is missing. Please confirm and provide the date of informed consent and the date of the first study-related procedure. This is required to verify GCP compliance regarding the timing of consent relative to study procedures.
        *   **判断理由:** 同意取得日の記録欠損はGCP遵守の確認を妨げるため、医療機関への確認が必要。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC (欠損)
            *   関連するプロトコル箇所: Section 5.1 (Informed Consent)
            *   関連する医学的知見: GCP原則

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM/Medical Monitor
        *   **疑義事項/確認内容:** 有害事象として報告されている「COUGH」は、開始日が2003年であり、治療期間外のイベント（AETRTEM='N'）であるため、既往歴（Medical History）として扱うのが適切か内部で検討・記録する。安全性評価への影響は小さいと判断。
        *   **判断理由:** データ帰属ドメインの問題であり、安全性評価への直接的な影響は小さい。医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='COUGH', AE.AESTDTC='2003', SUPPAE.QNAM='AETRTEM', SUPPAE.QVAL='N'
            *   関連するプロトコル箇所: Section 3.9.3.2 (Clinical Adverse Events)
    *   **確認事項No.:** I-2 (関連指摘No.: D-3, P-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** Visit 11.1 (WEEK 22 (T)) の実施日について、SVドメインの日付(2014-07-13)がVisit 10.1の日付(2014-07-16)より前になっている。QSドメインの日付およびStudy Day(124)からSVの日付が正しい可能性が高いが、Visit間の日付逆転と予定日(Day 154)からの逸脱があるため、内部で記録・確認する。評価への影響は限定的と判断。
        *   **判断理由:** データ入力エラーの可能性が高いが、他のデータとの整合性から評価への影響は小さい。Visit Windowからの逸脱については記録する。医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=10.1, 11.1, SV.SVSTDTC, QS.VISITNUM=11.1, QS.QSDTC, QS.QSDY, TV.VISITDY=154
            *   関連するプロトコル箇所: Attachment LZZT.1 (Schedule of Events)

---

# 01-701-1146のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
75歳、女性、WHITE、NOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2009年11月17日診断、PRIMARY DIAGNOSIS）、うつ病（SIGNIFICANT PRE-EXISTING CONDITION）、多発性関節炎（SIGNIFICANT PRE-EXISTING CONDITION）、難聴（SIGNIFICANT PRE-EXISTING CONDITION）、便秘（SIGNIFICANT PRE-EXISTING CONDITION）、心雑音（SIGNIFICANT PRE-EXISTING CONDITION）、膝痛（SIGNIFICANT PRE-EXISTING CONDITION）、副鼻腔炎（SIGNIFICANT PRE-EXISTING CONDITION）などが報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年05月07日|Day -13 (SCREENING 1)|MMSE 22点、Hachinskiスコア 1点。ALP 33 U/L (基準値35-115, LOW)。体温 37.3 C (微熱の可能性)。|
|2013年05月16日|Day -4 (N/A)|有害事象「RASH」(MILD) 発現。|
|2013年05月18日|Day -2 (SCREENING 2)|特に異常なし。|
|2013年05月20日|Day 1 (BASELINE)|治験薬 XANOMELINE 54 mg PATCH QD 開始。ALP 33 U/L (LOW) は継続。ADAS-Cog(11) 11点。NPI-X Total 4点 (Depression/Dysphoria 2点, Anxiety 2点)。|
|2013年05月21日|Day 2 (N/A)|併用薬 PAROXETINE 開始。|
|2013年05月22日|Day 3 (N/A)|併用薬 PAROXETINE 終了。|
|2013年06月01日|Day 13 (N/A)|有害事象「APPLICATION SITE IRRITATION」(MILD) 発現。|
|2013年06月02日|Day 14 (AMBUL ECG PLACEMENT)|有害事象「APPLICATION SITE IRRITATION」(MILD) 終了。有害事象「RASH」(MILD) 終了。立位時血圧・脈拍変動あり。|
|2013年06月03日|Day 15 (WEEK 2)|治験薬 XANOMELINE 54 mg 終了。立位1分後拡張期血圧 43 mmHg (ベースラインから低下、起立性低血圧の可能性)。ALP 35 U/L (NORMAL)。NPI-X Total 4点 (変化なし)。有害事象「FATIGUE」(MILD) 発現 (治験薬との関連: POSSIBLE)。|
|2013年06月04日|Day 16 (N/A)|治験薬 XANOMELINE 81 mg PATCH QD 開始 (増量)。|
|2013年06月10日|Day 22 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(MILD) 発現。有害事象「APPLICATION SITE PRURITUS」(MILD) 発現。|
|2013年06月12日|Day 24 (N/A)|併用薬 HYDROCORTISONE, TOPICAL 開始 (適用部位反応の治療目的か)。|
|2013年06月16日|Day 28 (WEEK 4)|ALP 34 U/L (LOW)。NPI-X Total 1点 (ベースラインから改善)。有害事象「APPLICATION SITE ERYTHEMA」が MODERATE に悪化。有害事象「APPLICATION SITE PRURITUS」が MODERATE に悪化。|
|2013年06月18日|Day 30 (AMBUL ECG REMOVAL)|臥位拡張期血圧 45 mmHg (低血圧傾向か)。|
|2013年06月22日|Day 34 (N/A)|有害事象「APPLICATION SITE PAIN」(MODERATE) 発現。|
|2013年06月26日|Day 38 (N/A)|治験薬 XANOMELINE 81 mg 終了 (早期中止)。有害事象「APPLICATION SITE IRRITATION」(MODERATE) 発現。有害事象「APPLICATION SITE VESICLES」(MODERATE) 発現。|
|2013年06月30日|Day 42 (WEEK 6)|治験中止 (理由: ADVERSE EVENT - 適用部位掻痒感)。臥位脈拍 52 bpm (徐脈傾向か)。ALP 29 U/L (LOW、さらに低下)。ADAS-Cog(11) 10点 (ベースラインから微改善)。CIBIC+ 4点 (No Change)。DAD Total 90% (ベースラインから改善傾向)。NPI-X Total 1点 (改善維持)。複数の適用部位反応およびFATIGUEは継続中 (未回復)。|
|2013年07月15日|Day 57 (AE FOLLOW-UP)|AE FOLLOW-UP Visit実施。AEの最終転帰不明。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 複数の適用部位反応（掻痒感、紅斑、刺激感、疼痛、小水疱）が発現・悪化し、治験中止に至っている。治験薬との関連性も高いと評価されており、安全性上の重要な問題である。中止後も未回復であり、AE FOLLOW-UP Visitでの最終的な転帰情報の確認が必要である。
        *   **根拠:** AEドメインの記録、DSドメインの中止理由、RELRECドメインの関連記録。経皮吸収型製剤で適用部位反応は予期される副作用の一つだが、重症度が悪化し中止に至っている点を重視。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE ERYTHEMA', 'APPLICATION SITE IRRITATION', 'APPLICATION SITE PAIN', 'APPLICATION SITE PRURITUS', 'APPLICATION SITE VESICLES'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD', 'MODERATE'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Relationship Identifier(RELREC.RELID)] = '01-701-1146-E13' (AE SEQ 6, 8 と DS SEQ 1 を関連付け)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Vital Signsにおいて、治験薬投与中に拡張期血圧の低下（Day 15 立位1分後 43mmHg, Day 30 臥位 45mmHg）および脈拍数の低下（Day 42 臥位 52bpm）が認められる。これらは起立性低血圧や徐脈を示唆し、治験薬（コリン作動薬）の薬理作用に関連する可能性がある。特に高齢者であるため、転倒などのリスクにつながる可能性があり、安全性上の懸念事項である。これらの所見はAEとして報告されていない。
        *   **根拠:** VSドメインのデータ推移。コリン作動薬の一般的な副作用（徐脈、血圧低下）。高齢者における起立性低血圧のリスク。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Study Day of Vital Signs(VS.VSDY)] = 15, [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 43
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Study Day of Vital Signs(VS.VSDY)] = 30, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 45
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Study Day of Vital Signs(VS.VSDY)] = 42, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 52
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** ALP値がベースラインで低値(33 U/L)であり、治験期間中に一過性の正常化(35 U/L)を認めるも、その後再度低下し、中止時点(Day 42)では29 U/Lとさらに低下している。他の肝機能検査(ALT, AST, Bilirubin)は正常範囲内であり、現時点での臨床的意義は不明である。
        *   **根拠:** LBドメインのデータ推移。ALP単独の軽度低下の臨床的意義は一般的に低いことが多い。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALP'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -13, 15, 28, 42
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 33, 35, 34, 29
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW', 'NORMAL', 'LOW', 'LOW'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 治験薬開始直後(Day 2-3)に抗うつ薬であるPAROXETINEが短期間投与されている。プロトコルでは抗うつ薬は1ヶ月のwashoutが必要と規定されており(3.4.2.2 [31b] j)、除外基準違反の可能性がある。投与理由（AE治療か既往歴のうつ病治療か等）およびプロトコル逸脱に該当するか確認が必要。短期間投与ではあるが、有効性・安全性評価への影響も考慮する必要がある。
        *   **根拠:** CMドメインの記録。プロトコル3.4.2.2 [31b] j)。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PAROXETINE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-05-21' (Day 2)
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2013-05-22' (Day 3)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** AE RASHについて、同じ開始日(2013-05-16)で2つのレコード(AESEQ=1, 2)が存在し、終了日と転帰が異なっている(AESEQ=1: 未回復、AESEQ=2: 回復/終了日2013-06-02)。データ入力エラーの可能性が高い。評価への直接的な影響は小さいと考えられるが、データの正確性の観点から確認が必要。
        *   **根拠:** AEドメイン内のデータ矛盾。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RASH'
            *   [Sequence Number(AE.AESEQ)] = 1, 2
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-05-16' (both)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '', '2013-06-02'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', 'RECOVERED/RESOLVED'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 多くの併用薬(CM)レコードで終了日(CMENDTC)が欠損している。特に、中止後も継続している可能性がある薬剤（HYDROCORTISONE TOPICAL, BECONASE, DOCUSATE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERA）について、中止後の使用状況が不明確である。AEフォローアップ期間中の安全性評価に影響する可能性がある。
        *   **根拠:** CMドメインの欠損データ。
        *   **関連データ:**
            *   [Domain Abbreviation(CM.DOMAIN)] = 'CM'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '' (multiple records)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** APPLICATION SITE ERYTHEMA (AESEQ=5, 7) と APPLICATION SITE PRURITUS (AESEQ=6, 8) が、同じ開始日で重症度のみ異なるレコードとして報告されている。これはイベントの悪化を示すための記録方法と考えられるが、データ構造としては冗長に見える。解釈は可能であり、評価への影響は小さい。
        *   **根拠:** AEドメインのデータ構造。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE ERYTHEMA', 'APPLICATION SITE PRURITUS'
            *   [Sequence Number(AE.AESEQ)] = 5, 7 and 6, 8
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-06-10' (for all four)
            *   [Severity/Intensity(AE.AESEV)] = 'MILD', 'MODERATE'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[31b] j)違反の可能性。抗うつ薬(PAROXETINE)が治験薬開始直後(Day 2-3)に投与されている。プロトコルでは1ヶ月のwashout期間が必要と規定されている。短期間投与であり影響は限定的かもしれないが、逸脱に該当する可能性がある。参加者の安全性や有効性評価に影響を与える可能性は低いと考えられるが、確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] j)
        *   **根拠:** CMドメインの記録とプロトコルの規定の照合。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PAROXETINE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-05-21'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2013-05-22'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験中止時の漸減投与不実施の可能性。プロトコル3.10.1では、中止時に用量を漸減するよう指示されているが、EXドメインには漸減投与の記録がない。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** EXドメインの記録とプロトコルの規定の照合。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-06-26' (for EXSEQ=2, 81mg dose)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-06-30'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[31b] k)で全身性ステロイドは禁止されているが、点鼻ステロイド(BECONASE)の使用が記録されている。局所投与であり許容される可能性が高いが、プロトコル上の明確な記載がないため確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] k)
        *   **根拠:** CMドメインの記録とプロトコルの規定の照合。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'BECONASE'
            *   [Route of Administration(CM.CMROUTE)] = 'NASAL'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1146は、複数の適用部位の有害事象によりDay 42に治験を中止されました。中止時点ではこれらの事象は未回復と記録されています。Day 57にAEフォローアップVisitが実施されていますが、これらの有害事象（適用部位紅斑、適用部位掻痒感、適用部位疼痛、適用部位刺激感、適用部位小水疱）および倦怠感の最終的な転帰について、詳細をお知らせください。また、適用部位反応の治療に使用されていた可能性のある「HYDROCORTISONE, TOPICAL」の最終使用日もご確認ください。
        *   **クエリ文面（英語）:** Subject 01-701-1146 discontinued on Day 42 due to multiple application site AEs, recorded as not recovered. AE follow-up visit was on Day 57. Please provide final outcome for AEs: Application Site Erythema, Pruritus, Pain, Irritation, Vesicles, and Fatigue. Also confirm last administration date for HYDROCORTISONE, TOPICAL.
        *   **判断理由:** 治験中止の原因となった有害事象の最終的な転帰を確認し、参加者の安全性を確保するため。また、関連する可能性のある併用薬の使用状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: AE.AEOUT='NOT RECOVERED/NOT RESOLVED' (for AESEQ 4, 5, 7, 8, 9, 10, 11), SV.VISIT='AE FOLLOW-UP', CM.CMTRT='HYDROCORTISONE, TOPICAL', CM.CMENDTC=''
            *   関連するプロトコル箇所: Section 3.9.3 (Safety), Section 3.10.1 (Discontinuations)
            *   関連する医学的知見: 有害事象の転帰確認は安全性評価の基本。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者01-701-1146のバイタルサインにおいて、Day 15に立位1分後の拡張期血圧が「43 mmHg」、Day 30に臥位拡張期血圧が「45 mmHg」、Day 42に臥位脈拍数が「52 bpm」と記録されています。これらの変動について、臨床的な意義（例：症候性の有無、起立性低血圧や徐脈の診断）を評価し、有害事象としての報告が必要かご判断ください。
        *   **クエリ文面（英語）:** VS data for subject 01-701-1146 shows: Day 15 standing Diastolic Blood Pressure 43 mmHg; Day 30 supine Diastolic Blood Pressure 45 mmHg; Day 42 supine Pulse Rate 52 bpm. Please assess the clinical significance (e.g., symptomatic? orthostatic hypotension? bradycardia?) and determine if AE reporting is required.
        *   **判断理由:** 潜在的な起立性低血圧や徐脈のリスクを評価し、参加者の安全性を確保するため。また、必要に応じて有害事象として適切に報告・評価するため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='DIABP', VS.VSDY=15, VS.VSSTRESN=43; VS.VSTESTCD='DIABP', VS.VSDY=30, VS.VSSTRESN=45; VS.VSTESTCD='PULSE', VS.VSDY=42, VS.VSSTRESN=52
            *   関連するプロトコル箇所: Section 3.9.3.4.1 (Vital Sign Determination), Section 3.9.3.2 (Clinical Adverse Events)
            *   関連する医学的知見: コリン作動薬による血圧・脈拍への影響、高齢者の起立性低血圧リスク。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-4, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1146について、治験薬開始後のDay 2からDay 3にかけて併用薬「PAROXETINE」が投与された記録があります。プロトコルでは抗うつ薬は1ヶ月のwashoutが必要とされています。この投与理由（例：有害事象治療、既往歴治療など）と、除外基準[31b] j)への抵触に関する評価についてご確認ください。
        *   **クエリ文面（英語）:** Subject 01-701-1146 received concomitant medication PAROXETINE on Day 2-3 post-randomization. Protocol requires 1-month washout for antidepressants (Exclusion [31b] j). Please clarify the reason for administration (e.g., AE treatment, pre-existing condition) and confirm assessment regarding exclusion criteria applicability.
        *   **判断理由:** プロトコル除外基準違反の可能性を確認し、記録するため。また、投与理由を明確にし、安全性・有効性評価への影響を判断するため。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='PAROXETINE', CM.CMSTDTC='2013-05-21', CM.CMENDTC='2013-05-22'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] j)
    *   **クエリNo.:** Q-4 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1146はDay 42に治験を中止されました。プロトコル3.10.1では中止時に治験薬を漸減投与するよう指示されていますが、漸減投与の記録がありませんでした。漸減投与が実施されなかった理由についてご確認ください。
        *   **クエリ文面（英語）:** Subject 01-701-1146 discontinued on Day 42. Protocol 3.10.1 specifies dose tapering upon discontinuation, but no record of tapering was found in EX domain. Please clarify the reason why dose tapering was not performed.
        *   **判断理由:** プロトコルからの逸脱の有無とその理由を確認し、記録するため。
        *   **判断根拠:**
            *   関連するデータ: EX domain, DS domain (DS.DSDECOD='ADVERSE EVENT', DS.DSSTDTC='2013-06-30')
            *   関連するプロトコル箇所: Section 3.10.1 Discontinuations
    *   **クエリNo.:** Q-5 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者01-701-1146の併用薬について、複数の薬剤で終了日が記録されていません。特にBECONASE, DOCUSATE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERAについて、治験終了後も使用が継続されたか、あるいは最終使用日をご確認ください。
        *   **クエリ文面（英語）:** For subject 01-701-1146, the end date (CMENDTC) is missing for several concomitant medications. Please confirm if BECONASE, DOCUSATE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERA were continued after study discontinuation, or provide the last administration date.
        *   **判断理由:** データの完全性を確保し、治験期間外の薬剤使用状況を把握するため。
        *   **判断根拠:**
            *   関連するデータ: CM.CMENDTC = '' for multiple records.
            *   関連するプロトコル箇所: N/A (General data quality)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE RASH (AESEQ=1, 2) の記録に矛盾（同一開始日で異なる終了日・転帰）がある。データ入力エラーの可能性が高いため、内部でデータクリーニングプロセスを通じて修正可能か確認する。評価への影響は小さいと判断。
        *   **判断理由:** データ品質の問題であり、内部での修正・確認が適切と判断したため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='RASH', AE.AESEQ=1, 2
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** ALP低値が持続・悪化傾向を示している。他の肝機能検査は正常であり、現時点での臨床的意義は不明。内部でこの所見を記録し、同様の傾向が他の症例でも見られるか等、今後の安全性シグナル検出のために注視する。参加者への直接的なリスクは低いと判断。
        *   **判断理由:** 現時点での臨床的意義は低いが、傾向として記録・監視する価値があると判断したため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALP', LB.LBNRIND='LOW'
    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/Medical Monitor
        *   **疑義事項/確認内容:** 併用薬として点鼻ステロイド(BECONASE)が使用されている。プロトコルでは全身性ステロイドは禁止されているが、局所投与(点鼻)の許容性について明確な記載がない。一般的な臨床試験の慣習や薬剤の特性から許容される可能性が高いと判断されるが、念のため内部で解釈を統一し記録する。参加者の安全性や評価への影響は小さいと判断。
        *   **判断理由:** プロトコルの解釈に関する事項であり、内部での確認・記録が適切と判断したため。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='BECONASE', CM.CMROUTE='NASAL'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] k)

---

# 01-701-1148のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
57歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2010年12月12日診断）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年07月29日|Day -25 (N/A)|有害事象「DEPRESSED MOOD」(MODERATE) 発現 (治験薬開始前)|
|2013年08月14日|Day -9 (SCREENING 1)|体重 86.18 kg。MMSE 21点、Hachinski Ischemic Score 1点。|
|2013年08月23日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg/day (パッチ剤、経皮投与) 開始。体重 87.09 kg。ADAS-Cog(11) 5点、NPI-X Total 16点。DAD Medications関連項目がNA。|
|2013年08月25日|Day 3 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(MILD, PROBABLE) 発現。|
|2013年08月25日|Day 3 (N/A)|有害事象「APPLICATION SITE PRURITUS」(MILD, PROBABLE) 発現。|
|2013年09月06日|Day 15 (N/A)|治験薬 Xanomeline 82 mg/day に増量。(プロトコル規定は81mg)|
|2013年09月19日|Day 28 (WEEK 4)|体重 88.91 kg。立位収縮期血圧 95 mmHg (3分後)。NPI-X Total 6点。|
|2013年10月12日|Day 51 (N/A)|有害事象「LOWER RESPIRATORY TRACT INFECTION」(MODERATE, NONE) 発現。|
|2013年10月18日|Day 57 (WEEK 8)|ADAS-Cog(11) 6点、CIBIC+ 5点 (Minimal worsening)、NPI-X Total 9点。併用薬 Hydrocortisone (外用) 開始 (Day 88)。|
|2013年11月10日|Day 80 (N/A)|有害事象「LOWER RESPIRATORY TRACT INFECTION」回復。|
|2013年11月17日|Day 87 (WEEK 12)|NPI-X Total 0点。|
|2013年12月13日|Day 113 (WEEK 16)|ADAS-Cog(11) 6点、CIBIC+ 4点 (No Change)、NPI-X Total 2点。|
|2013年12月15日|Day 115 (N/A)|有害事象「FLANK PAIN」(MODERATE, NONE) 発現。|
|2013年12月17日|Day 117 (N/A)|有害事象「FLANK PAIN」回復。有害事象「CALCULUS URETHRAL」(MODERATE, NONE) 発現、同日回復。|
|2014年01月03日|Day 134 (N/A)|有害事象「EPISTAXIS」(MILD, NONE) 発現、同日回復。|
|2014年01月10日|Day 141 (WEEK 20)|体重 90.27 kg。NPI-X Total 6点。|
|2014年01月24日|Day 155 (WEEK 22 (T))|NPI-X Total 23点 (他の時点と比較し突出して高い)。|
|2014年01月25日|Day 156 (N/A)|併用薬 Cimetidine 開始。|
|2014年02月08日|Day 170 (WEEK 24)|ADAS-Cog(11) 7点、CIBIC+ 5点 (Minimal worsening)、NPI-X Total 12点。Eosinophils 0.76 GI/L (基準値上限 0.57)。立位収縮期血圧 96 mmHg (1分後), 100 mmHg (3分後)。併用薬 Cimetidine 終了。|
|2014年02月09日|Day 171 (N/A)|治験薬 Xanomeline 216 mg/day に増量。(プロトコルからの逸脱の可能性)|
|2014年02月12日|Day 174 (N/A)|有害事象「ACTINIC KERATOSIS」(MILD, NONE) 発現。併用薬 Fluoroplex 開始。|
|2014年02月20日|Day 182 (WEEK 26)|治験薬投与終了。治験完了。体重 90.72 kg。Eosinophils 0.23 GI/L (正常化)。立位収縮期血圧 99 mmHg (1分後), 95 mmHg (3分後)。NPI-X Total 10点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 立位時の収縮期血圧がベースラインと比較して低下傾向にある（Day 28, 170, 182で95-100 mmHg）。Xanomelineはコリン作動薬であり、血圧低下を引き起こす可能性がある。起立性低血圧による転倒等のリスクが懸念されるが、関連する有害事象（めまい等）の報告はない。
        *   **根拠:** Xanomelineの薬理作用（コリン作動性）、バイタルサインの経時的変化。参加者の安全性（転倒リスク）。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 95, 96, 100, 99 (Day 28, 170, 182)
            *   [Study Day of Vital Signs(VS.VSDY)] = 28, 170, 182
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** NPI-X Total ScoreがWeek 22 (T) (Day 155) で23点と、他の時点（ベースライン16点、他の治療期間中0-12点）と比較して突出して高い。このVisitの各項目のFrequencyが軒並み高く記録されている。一時的な精神症状の急激な悪化があったのか、あるいはデータ測定・記録の信頼性に問題があるのか不明であり、有効性評価の解釈に影響を与える可能性がある。
        *   **根拠:** 有効性評価指標の経時的変化のパターンからの逸脱。評価の信頼性確保の観点。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 23
            *   [Study Day of Finding(QS.QSDY)] = 155
            *   [Visit Number(QS.VISITNUM)] = 11.1
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM04F', 'NPITM05F', 'NPITM07F', 'NPITM09F' など (Frequency項目)
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 3 or 4 (Day 155)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** Day 171からの治験薬投与量 (EXDOSE) が216 mgと記録されている。これはプロトコルで規定されたHigh Dose群の用量 (81 mg) から大きく逸脱している。記録ミスなのか、実際に過量投与が行われたのか不明。過量投与の場合、参加者の安全性に重大な影響を与える可能性があり、試験結果の解釈にも影響する。
        *   **根拠:** プロトコル規定用量との著しい乖離。参加者の安全性、データ信頼性への潜在的影響。
        *   **関連データ:**
            *   [Dose per Administration(EX.EXDOSE)] = 216
            *   [Dose Units(EX.EXDOSU)] = 'mg'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-02-09'
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 171
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** Day 15からの治験薬投与量 (EXDOSE) が82 mgと記録されている。プロトコルおよびTSドメインではHigh Dose群の維持用量は81 mgと記載されており、1mgの差異がある。記録ミスの可能性が高いが、臨床的な影響は小さいと考えられる。
        *   **根拠:** プロトコル規定用量との軽微な不一致。
        *   **関連データ:**
            *   [Dose per Administration(EX.EXDOSE)] = 82
            *   [Dose Units(EX.EXDOSU)] = 'mg'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-09-06'
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 15
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 有害事象「APPLICATION SITE ERYTHEMA」「APPLICATION SITE PRURITUS」はDay 3から発現し持続しているが、関連する可能性のある併用薬「HYDROCORTISONE」(外用) の開始日 (CMSTDTC) はDay 88と記録されており、80日以上のずれがある。AEに対する治療開始が遅れたのか、CMの記録開始日が誤っているのか、あるいはプロトコル規定の予防的使用と治療的使用の記録が混同されている可能性がある。
        *   **根拠:** AE発現日と関連治療薬開始日の時間的な不整合。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE ERYTHEMA', 'APPLICATION SITE PRURITUS'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-08-25' (Day 3)
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-11-18' (Day 88)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** DAD質問票のMedications関連項目 (DAITM34: DECIDE TO TAKE HIS/HER MEDICATIONS, DAITM35: TAKE HIS/HER MEDICATIONS AS PRESCRIBED) のベースライン (Day 1) の結果がNA (Not Applicable) と記録されているが、Week 8以降はY (Yes) となっている。ベースラインでNAと評価された理由が不明確（評価不能だったのか、該当しなかったのか等）。
        *   **根拠:** 有効性評価データの解釈における不明瞭さ。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM34', 'DAITM35'
            *   [Finding in Original Units(QS.QSORRES)] = 'NA'
            *   [Visit Number(QS.VISITNUM)] = 3
            *   [Study Day of Finding(QS.QSDY)] = 1
            *   [Finding in Original Units(QS.QSORRES)] = 'Y'
            *   [Visit Number(QS.VISITNUM)] = 8, 10, 12

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) がデータセットに記録されていない。プロトコルでは同意取得が必須であり (INCL06)、同意なしに治験手順を開始することはGCP違反となる。同意取得の事実と日付の確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.1, 3.4.2.1 [6], 5.1
        *   **根拠:** GCPの基本要件、参加者の権利保護。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬としてCimetidine (H2ブロッカー) がDay 156からDay 170まで使用されている。プロトコル 3.4.2.2 [31b] m) ではH2ブロッカーは原則使用禁止（1週間のWashout期間が必要）とされており、Axid (nizatidine) のみが症例ベースでの使用許可の可能性が言及されている。Cimetidineの使用はプロトコルからの逸脱の可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] m), Section 3.8
        *   **根拠:** 併用禁止薬の使用は安全性・有効性評価に影響を与える可能性がある。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'CIMETIDINE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2014-01-25' (Day 156)
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2014-02-08' (Day 170)
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬としてHydrocortisone (外用) がDay 88からPRNで使用されている。プロトコル 3.6.2 では、パッチ貼付前に予防的にHydrocortisone cream (1%) を使用することが規定されている。CMで報告されている使用が、この予防的使用なのか、あるいはAE（適用部位反応）に対する治療目的なのか不明確。治療目的であれば問題ないが、予防的使用であればCMドメインではなく、別の方法で記録されるべきかもしれない。使用目的の明確化が必要。
        *   **プロトコル該当箇所:** Section 3.6.2, Section 3.8
        *   **根拠:** データ記録の正確性、プロトコル手順の遵守確認。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-11-18' (Day 88)
            *   [Dosing Frequency per Interval(CM.CMDOSFRQ)] = 'PRN'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-1)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 171 (2014年2月9日) からの治験薬「XANOMELINE」について、「Dose per Administration」が「216 mg」と記録されています。プロトコル規定のHigh Doseは81 mgですが、この記録は正しいでしょうか？記録が誤っている場合は修正をお願いします。実際に216 mgが投与された場合は、その経緯と患者の安全性について詳細な情報を提供してください。過量投与の可能性があり、参加者の安全確保のため確認が必要です。
        *   **クエリ文面（英語）:** Regarding study drug XANOMELINE from Study Day 171 (2014-02-09), the Dose per Administration (EXDOSE) is recorded as 216 mg. The protocol specifies 81 mg for the High Dose arm. Is this record correct? If incorrect, please correct. If 216 mg was actually administered, please provide details on the circumstances and patient safety. This clarification is crucial due to potential overdose and participant safety.
        *   **判断理由:** プロトコル規定用量からの著しい逸脱であり、過量投与の可能性があるため、参加者の安全確保とデータの正確性確認が最優先。
        *   **判断根拠:**
            *   関連するデータ: [Dose per Administration(EX.EXDOSE)] = 216, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-02-09'
            *   関連するプロトコル箇所: Section 3.1, 3.6
            *   関連する医学的知見: 過量投与による予期せぬ有害事象リスク。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 立位時の収縮期血圧が、Day 28, 170, 182などで95-100 mmHgと、ベースライン時と比較して低下傾向が見られます。起立性低血圧に関連する症状（めまい、ふらつき等）の有無について確認し、臨床的な評価をお願いします。薬剤関連の血圧低下の可能性があり、参加者の安全確保（転倒リスク等）のため確認が必要です。
        *   **クエリ文面（英語）:** Standing systolic blood pressure shows a decreasing trend compared to baseline (e.g., 95-100 mmHg on Days 28, 170, 182). Please confirm if the patient experienced any symptoms related to orthostatic hypotension (e.g., dizziness, lightheadedness) and provide clinical assessment. This check is needed for participant safety (e.g., fall risk) due to potential drug-related hypotension.
        *   **判断理由:** 薬剤関連の可能性がある血圧低下傾向について、症状の有無を確認し、参加者の安全リスクを評価するため。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 95, 96, 100, 99 (Day 28, 170, 182)
            *   関連する医学的知見: コリン作動薬による血圧低下、起立性低血圧のリスク。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 22 (T) (Study Day 155) のNPI-X評価について、「NPI-X (9) Total Score」が「23」と、他の評価時点と比較して著しく高い値が記録されています。この期間の患者様の精神状態に特筆すべき変化があったのでしょうか？あるいは、評価時の記録内容に誤りがないかご確認ください。有効性評価の信頼性担保のため確認が必要です。
        *   **クエリ文面（英語）:** Regarding the NPI-X assessment at Week 22 (T) (Study Day 155), the NPI-X (9) Total Score (NPTOT) is recorded as 23, which is markedly higher than at other time points. Was there a significant change in the patient's mental state during this period, or could there be a recording error? Please verify the record and provide details on the patient's condition. This clarification is needed to ensure the reliability of efficacy assessment.
        *   **判断理由:** 有効性評価データの外れ値について、その原因（真の変動かエラーか）を特定し、評価の信頼性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 23, [Study Day of Finding(QS.QSDY)] = 155
            *   関連するプロトコル箇所: Section 3.9.1.1 (NPI-X)
    *   **クエリNo.:** Q-4 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本症例の「Date/Time of Informed Consent」が記録されていません。同意取得日を確認し、データ入力をお願いします。同意取得は治験参加の必須要件であり、記録の確認が必要です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (DM.RFICDTC) for this subject is missing. Please confirm the date of informed consent and enter the data. Confirmation of consent is essential for study participation.
        *   **判断理由:** 同意取得の記録はGCP遵守および参加者の権利保護の観点から必須であり、欠損しているため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = (欠損)
            *   関連するプロトコル箇所: Section 3.4.1, 5.1
    *   **クエリNo.:** Q-5 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬として「CIMETIDINE」がStudy Day 156から170まで使用された記録があります。プロトコルではH2ブロッカーの使用は原則禁止されていますが、使用理由、期間、用量について詳細をお知らせください。プロトコル遵守の観点から確認が必要です。
        *   **クエリ文面（英語）:** Concomitant medication CIMETIDINE (H2 blocker) was recorded from Study Day 156 to 170. The protocol generally prohibits H2 blockers. Please provide the reason for use, duration, and dose. This clarification is needed for protocol compliance assessment.
        *   **判断理由:** プロトコルで原則禁止されている薬剤の使用が記録されており、逸脱の可能性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'CIMETIDINE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2014-01-25', [End Date/Time of Medication(CM.CMENDTC)] = '2014-02-08'
            *   関連するプロトコル箇所: Section 3.4.2.2 [31b] m), Section 3.8
    *   **クエリNo.:** Q-6 (関連指摘No.: D-3, P-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「HYDROCORTISONE」(外用) がStudy Day 88からPRNで使用された記録があります。これは、有害事象（適用部位反応）に対する治療目的でしょうか、それともプロトコルで規定されているパッチ貼付前の予防的使用でしょうか？また、有害事象「APPLICATION SITE ERYTHEMA/PRURITUS」はStudy Day 3から発現していますが、併用薬開始日がDay 88となっている理由も併せてご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication HYDROCORTISONE (topical) was recorded as used PRN from Study Day 88. Was this for treatment of AE (application site reaction) or prophylactic use as specified in protocol 3.6.2? Also, please clarify why the start date is Day 88, while related AEs started on Day 3.
        *   **判断理由:** 併用薬の使用目的と開始日の記録の正確性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-11-18', [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE ERYTHEMA', 'APPLICATION SITE PRURITUS', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-08-25'
            *   関連するプロトコル箇所: Section 3.6.2, 3.8
    *   **クエリNo.:** Q-7 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DAD質問票のMedications関連項目（DAITM34, DAITM35）について、ベースライン (Study Day 1) の結果が「NA (Not Applicable)」と記録されていますが、Week 8以降は「Y (Yes)」となっています。ベースラインでNAと評価された理由（例：評価不能、質問が該当しなかった等）をお知らせください。
        *   **クエリ文面（英語）:** Regarding DAD questionnaire items DAITM34 and DAITM35 (Medications), the result at Baseline (Study Day 1) is recorded as 'NA' (Not Applicable), while results from Week 8 onwards are 'Y' (Yes). Please clarify the reason for the 'NA' assessment at baseline (e.g., unable to assess, question not applicable).
        *   **判断理由:** 有効性評価データの解釈を明確にするため、ベースライン評価の背景を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'DAITM34', 'DAITM35', [Finding in Original Units(QS.QSORRES)] = 'NA' (Day 1), 'Y' (Day 57 onwards)
            *   関連するプロトコル箇所: Protocol Attachment LZZT.5 (DAD)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 治験薬投与量について、Day 15からの記録が82 mgとなっている（プロトコル/TSでは81 mg）。1mgの差異であり臨床的影響は無視できると判断されるため、医療機関への問い合わせは不要とする。ただし、データ入力パターンとして他症例でも同様のずれがないか内部で確認する。
        *   **判断理由:** 臨床的影響が極めて小さく、記録ミスの可能性が高いため。
        *   **判断根拠:**
            *   関連するデータ: [Dose per Administration(EX.EXDOSE)] = 82, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-09-06'
            *   関連するプロトコル箇所: Section 3.1, 3.6
            *   関連するデータ: [Parameter Value(TS.TSVAL)] = '81' where [Trial Summary Parameter Short Name(TS.TSPARMCD)] = 'DOSE'

---

# 01-701-1153のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
79歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2005年5月13日発症、Primary Diagnosis）、貧血（1977年発症）、皮膚新生物切除（2010年実施）、皮膚癌（2010年発症）、副鼻腔炎（2011年発症）が報告されている。Significant Pre-existing Conditionとして、頭痛、Increased tendency to bruise、足関節浮腫、頸部痛、乱視が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年09月06日|Day -17 (SCREENING 1)|スクリーニング評価実施。MMSEスコア: 10、Hachinskiスコア: 1。身長: 156.21 cm、体重: 58.06 kg。Specific Gravity (尿比重): 1.003 (LOW)。他の主要な検査値、バイタルサインは基準値内。|
|2013年09月18日|Day -5 (SCREENING 2)|バイタルサイン測定。異常なし。|
|2013年09月23日|Day 1 (BASELINE)|治験薬（Placeboパッチ）投与開始。ベースライン評価実施。ADAS-Cog(11) Total Score: 48。NPI-X Total Score: 15。DAD Total Score (% Yes): 15%。バイタルサイン、検査値に特記すべき異常なし。|
|2013年10月08日|Day 16 (WEEK 2)|治験薬投与継続中。NPI-X Total Score: 15。バイタルサイン、検査値に特記すべき異常なし。|
|2013年10月13日|Day 21 (N/A)|有害事象「INCREASED APPETITE」(MILD) 発現。治験薬との関連: POSSIBLE。|
|2013年10月19日|Day 27 (WEEK 4)|治験薬投与継続中。NPI-X Total Score: 8。DAD Total Score (% Yes): 10%。バイタルサイン、検査値に特記すべき異常なし。|
|2013年10月19日|Day 27 (UNSCHEDULED 5.1)|Urinalysis実施。異常なし。|
|2013年11月04日|Day 43 (WEEK 6)|治験薬投与継続中。NPI-X Total Score: 9。バイタルサイン、検査値に特記すべき異常なし。|
|2013年11月06日|Day 45 (N/A)|有害事象「INCREASED APPETITE」 転帰: NOT RECOVERED/NOT RESOLVED (AESEQ=1の記録) / RECOVERED/RESOLVED (AESEQ=2の記録)。処置: DRUG WITHDRAWN (AESEQ=2の記録)。(データの不整合あり)|
|2013年11月18日|Day 57 (WEEK 8)|治験薬投与継続中。ADAS-Cog(11) Total Score: 47。CIBIC+: 4 (No Change)。NPI-X Total Score: 9。DAD Total Score (% Yes): 17.5%。バイタルサイン、検査値に特記すべき異常なし。|
|2013年12月02日|Day 71 (WEEK 10 (T))|治験薬投与継続中。NPI-X Total Score: 12。|
|2013年12月16日|Day 85 (WEEK 12)|治験薬投与継続中。NPI-X Total Score: 15。Urinalysis: Ketones 1 (ABNORMAL)。他の検査値、バイタルサインに特記すべき異常なし。|
|2013年12月18日|Day 87 (UNSCHEDULED 9.2)|Urinalysis実施。Ketones 0 (NORMAL)。|
|2013年12月30日|Day 99 (WEEK 14 (T))|治験薬投与継続中。NPI-X Total Score: 12。|
|2013年12月30日|Day 99 (UNSCHEDULED 9.3)|Urinalysis実施。異常なし。|
|2014年01月08日|Day 108 (WEEK 16)|治験薬投与継続中。ADAS-Cog(11) Total Score: 55。CIBIC+: 4 (No Change)。NPI-X Total Score: 5。DAD Total Score (% Yes): 12.5%。Cholesterol: 310 mg/dL (HIGH)。他の検査値、バイタルサインに特記すべき異常なし。|
|2014年02月11日|Day 142 (WEEK 20)|治験薬投与継続中。NPI-X Total Score: 17。DAD Total Score (% Yes): 15%。Cholesterol: 289 mg/dL (NORMAL)。他の検査値、バイタルサインに特記すべき異常なし。|
|2014年02月25日|Day 156 (WEEK 22 (T))|治験薬投与継続中。NPI-X Total Score: 6。|
|2014年03月11日|Day 170 (WEEK 24)|治験薬投与継続中。ADAS-Cog(11) Total Score: 52。CIBIC+: 4 (No Change)。NPI-X Total Score: 5。DAD Total Score (% Yes): 20%。バイタルサイン、検査値に特記すべき異常なし。|
|2014年03月16日|Day 175 (N/A)|治験薬（Placeboパッチ）投与終了。|
|2014年04月01日|Day 191 (WEEK 26)|試験完了。NPI-X Total Score: 6。バイタルサイン、検査値に特記すべき異常なし。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Minor
        *   **内容:** Week 16に一過性のコレステロール高値（310 mg/dL, 基準値上限300 mg/dL）が認められたが、前後（Week 12: 292 mg/dL, Week 20: 289 mg/dL）では基準値内であり、臨床的な意義は低いと考えられる。Placebo投与中であり、薬剤性の可能性は低い。
        *   **根拠:** 一過性の軽度な基準値逸脱であり、他の臨床所見との関連も見られないため。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CHOL'
            *   [Visit Number(LB.VISITNUM)] = 10
            *   [Study Day of Specimen Collection(LB.LBDY)] = 108
            *   [Result or Finding in Original Units(LB.LBORRES)] = '310'
            *   [Original Units(LB.LBORRESU)] = 'mg/dL'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '300'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Week 12に尿中ケトン体陽性（1+）が認められたが、直後のUnscheduled Visit (Day 87) では陰性化しており、一過性のものであった可能性が高い。臨床症状との関連も報告されておらず、臨床的意義は低いと考えられる。
        *   **根拠:** 一過性の所見であり、速やかに正常化しているため。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'KETONES'
            *   [Visit Number(LB.VISITNUM)] = 9
            *   [Study Day of Specimen Collection(LB.LBDY)] = 85
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL'
            *   [Visit Number(LB.VISITNUM)] = 9.2
            *   [Study Day of Specimen Collection(LB.LBDY)] = 87
            *   [Result or Finding in Original Units(LB.LBORRES)] = '0'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** 有害事象「INCREASED APPETITE」がDay 21に発現し、Day 45に消失したと記録されている。Placebo投与中のため治験薬との関連性は低いと考えられるが、NPI-XのAppetite/Eating Changeスコア（NPITM12S）はWeek 4 (Day 27) で0、Week 10 (T) (Day 71) で0と記録されており、AE報告との間に若干の齟齬が見られる可能性がある（ただしNPI-Xは過去2週間の評価）。臨床的な影響は小さいと考えられる。
        *   **根拠:** Placebo投与中であり、AEと有効性評価の軽微な齟齬の可能性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'INCREASED APPETITE'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 21
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 45
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM12S'
            *   [Visit Number(QS.VISITNUM)] = 5, 8.1
            *   [Study Day of Finding(QS.QSDY)] = 27, 71
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「INCREASED APPETITE」について、同一事象と思われる記録が2件（AESEQ=1, AESEQ=2）存在する。開始日は同一だが、終了日、転帰（AEOUT）、処置（AEACN）が異なる。AESEQ=1ではAEOUT='NOT RECOVERED/NOT RESOLVED', AEACN=空欄、AESEQ=2ではAEOUT='RECOVERED/RESOLVED', AEACN='DRUG WITHDRAWN'となっている。データの重複入力または修正過程での不整合の可能性があり、正確な有害事象情報の把握に影響する。
        *   **根拠:** 同一事象に対する矛盾した記録が存在するため。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'INCREASED APPETITE'
            *   [Sequence Number(AE.AESEQ)] = 1, 2
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-10-13'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-06'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', 'RECOVERED/RESOLVED'
            *   [Action Taken with Study Treatment(AE.AEACN)] = '', 'DRUG WITHDRAWN'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、TYLENOLの記録が各Visitで繰り返されている。CMSTDTCが全て'2011'となっており、CMENDTCが空欄であることから、2011年から継続してPRNで使用されていると解釈できるが、記録方法として適切か確認が必要。各Visitで記録する必要があるのか、あるいは初回記録のみでよいのか、データ入力規則を確認すべき。評価への影響は小さい。
        *   **根拠:** 記録の冗長性の可能性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TYLENOL'
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2011'
            *   [End Date/Time of Medication(CM.CMENDTC)] = ''
            *   [Sequence Number(CM.CMSEQ)] = 1-13
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** QSドメインのDAD評価において、DAITM20 (PREPARE OR COOK A LIGHT MEAL OR A SNACK) のWeek 8 (VISITNUM=8) の結果が 'NA' (Not Applicable) と記録されている。他のVisitでは 'N' (No) と記録されており、一貫性がない。NAと判断された理由が不明。評価への影響は小さいと考えられる。
        *   **根拠:** 同一評価項目に対する結果の不一致。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'DAITM20'
            *   [Visit Number(QS.VISITNUM)] = 8
            *   [Finding in Original Units(QS.QSORRES)] = 'NA'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 96
            *   [Visit Number(QS.VISITNUM)] = 3, 10, 12
            *   [Finding in Original Units(QS.QSORRES)] = 'N'
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 0

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルではPK採血がVisit 3, 4, 5, 7, 9, 11で規定されているが（Section 3.9.2）、提供されたLBデータにはPK関連のデータが含まれていない。PK採血が未実施であったか、データが欠損している可能性がある。本試験の主要目的にはPK評価は含まれていないため、影響は限定的と考えられる。
        *   **プロトコル該当箇所:** Section 3.9.2 Pharmacokinetics
        *   **根拠:** プロトコルで規定された評価が実施されていない、またはデータが存在しない可能性。
        *   **関連データ:** LBドメイン全体 (PKデータなし)
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** Urinalysisがプロトコル規定のVisit (4, 9, 12) 以外に、Unscheduled Visit (5.1, 9.2, 9.3) でも実施されている。逸脱ではあるが、安全性評価を強化する方向であり、参加者の安全性や評価の信頼性への悪影響はないと考えられる。実施理由は不明。
        *   **プロトコル該当箇所:** Section 3.9.3.3 Clinical Laboratory Tests, Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルで規定されていないタイミングでの検査実施。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'COLOR', 'KETONES', 'PH', 'SPGRAV', 'UROBIL'
            *   [Visit Number(LB.VISITNUM)] = 5.1, 9.2, 9.3
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の臨床検査値において、Specific Gravity (尿比重) が基準値下限 (1.006) を下回る 1.003 であった。プロトコル除外基準[27b]では "Laboratory test values exceeding the Lilly Reference Range III" が除外対象とされているが、下回る場合についての記載はない。また、Lilly Reference Range III の具体的な値も不明。臨床的に意義のある逸脱とは考えにくく、組み入れへの影響は小さい可能性が高いが、基準適合性の判断がデータ上からは完全にはできない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** スクリーニング時の検査値が基準値範囲外であった可能性。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SPGRAV'
            *   [Visit Number(LB.VISITNUM)] = 1
            *   [Result or Finding in Original Units(LB.LBORRES)] = '1.003'
            *   [Reference Range Lower Limit in Orig Unit(LB.LBORNRLO)] = '1.006'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-1)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「INCREASED APPETITE」について、2つの記録（AESEQ=1およびAESEQ=2）が存在し、転帰および処置の情報が異なっています（AESEQ=1: 転帰「NOT RECOVERED/NOT RESOLVED」、処置「記録なし」 / AESEQ=2: 転帰「RECOVERED/RESOLVED」、処置「DRUG WITHDRAWN」）。正しい情報を確認し、不要な記録を削除または修正してください。有害事象の正確な評価のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding AE 'INCREASED APPETITE', there are two records (AESEQ=1 and AESEQ=2) with conflicting outcome (AEOUT: 'NOT RECOVERED/NOT RESOLVED' vs 'RECOVERED/RESOLVED') and action taken (AEACN: blank vs 'DRUG WITHDRAWN'). Please verify the correct information and delete/correct the record(s) accordingly for accurate AE assessment.
        *   **判断理由:** 同一有害事象に対する矛盾した記録が存在し、データの正確性・信頼性に影響するため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=1, 2), AETERM='INCREASED APPETITE', AEOUT, AEACN
            *   関連するプロトコル箇所: Section 3.9.3.2 Adverse Event Reporting Requirements
            *   関連する医学的知見: なし (データ整合性の問題)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインのTYLENOLの記録が各Visitで繰り返されている。CMSTDTCが'2011'でCMENDTCが空欄であることから、継続使用と解釈される。データ入力規則を確認し、このような継続使用薬の記録方法が適切であるか、あるいは初回記録のみでよいのかを明確にする。評価への影響は小さいと判断。
        *   **判断理由:** データ入力規則の確認であり、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='TYLENOL', CMSTDTC='2011', CMENDTC='')
            *   関連するプロトコル箇所: なし (データマネジメント計画等を確認)
    *   **確認事項No.:** I-2 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QSドメインのDAD評価において、DAITM20 (PREPARE OR COOK A LIGHT MEAL OR A SNACK) のWeek 8の結果が 'NA' と記録されている点について確認。他のVisitでは 'N' であり、一貫性がない理由を考察する（例：一時的な状況変化、記録ミスなど）。評価への影響は小さいと判断。
        *   **判断理由:** 軽微なデータ不整合であり、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSTESTCD='DAITM20', VISITNUM=8, QSORRES='NA')
            *   関連するプロトコル箇所: なし
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** プロトコルで規定されているPK採血データがLBドメインに存在しない。PK評価は主要目的ではないため影響は限定的だが、採血が未実施だったのか、データ転送漏れ等の理由を確認し記録する。
        *   **判断理由:** 主要評価項目への影響はないが、プロトコル遵守状況の確認のため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (PKデータなし)
            *   関連するプロトコル箇所: Section 3.9.2 Pharmacokinetics
    *   **確認事項No.:** I-4 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** UrinalysisがUnscheduled Visitで実施されている。プロトコルからの逸脱ではあるが、安全性評価強化のため問題なしと判断。実施理由（例：臨床症状発現のため等）があれば記録を確認する。
        *   **判断理由:** 安全性への悪影響はなく、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (VISITNUM=5.1, 9.2, 9.3)
            *   関連するプロトコル箇所: Section 3.9.3.3 Clinical Laboratory Tests, Attachment LZZT.1 Schedule of Events
    *   **確認事項No.:** I-5 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** スクリーニング時の尿比重低値 (1.003) が除外基準[27b]に抵触しないか確認。プロトコルには基準値を「下回る」場合の規定がないこと、Lilly Reference Range IIIの詳細が不明なことから、組み入れは妥当であった可能性が高いと判断。ただし、念のため記録として残す。
        *   **判断理由:** 臨床的意義が低く、組み入れへの影響も小さい可能性が高いが、基準適合性の完全な確認がデータ上できないため記録。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='SPGRAV', VISITNUM=1, LBORRES='1.003', LBNRIND='LOW')
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]

---

# 01-701-1180のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
56歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2008年9月21日発症）、うつ病（不安）（SIGNIFICANT PRE-EXISTING CONDITION、Severity: MILD、開始日不明）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年01月28日|Day -15 (SCREENING 1)|MMSEスコア 19点 (Inclusion [3] 10-23点 適合)。Hachinskiスコア 1点 (Inclusion [4] <=4点 適合)。Urate 7.9 mg/dL (HIGH、基準値 3.3-7.5)。身長 180.34 cm、体重 88.91 kg。臥位血圧 146/86 mmHg、立位3分後血圧 138/90 mmHg。臥位脈拍 60 bpm、立位3分後脈拍 64 bpm。体温 36.94 C。|
|2013年02月10日|Day -2 (SCREENING 2)|臥位血圧 134/84 mmHg、立位3分後血圧 130/84 mmHg。臥位脈拍 60 bpm、立位3分後脈拍 66 bpm。体温 37.0 C。|
|2013年02月12日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg (PATCH, QD) 投与開始。有害事象「VOMITING」(Mild, Not Related) 発現、同日回復 (2件記録あり)。ADAS-Cog(11) スコア 30点。NPI-X Total Score 0点。DAD評価実施。臥位血圧 132/76 mmHg、立位3分後血圧 130/84 mmHg。臥位脈拍 66 bpm、立位3分後脈拍 70 bpm。体温 36.56 C。体重 89.81 kg。|
|2013年02月15日|Day 4 (N/A)|有害事象「MICTURITION URGENCY」(Mild, Possible) 発現。有害事象「SUDDEN DEATH」(Mild, Possible) 発現 (医学的に疑義あり)。|
|2013年02月24日|Day 13 (AMBUL ECG PLACEMENT)|臥位血圧 144/91 mmHg、立位3分後血圧 138/99 mmHg。臥位脈拍 71 bpm、立位3分後脈拍 78 bpm。体温 36.56 C。(血圧上昇傾向)|
|2013年02月25日|Day 14 (WEEK 2)|NPI-X Total Score 0点。Urate 8.1 mg/dL (HIGH)。臥位血圧 138/87 mmHg、立位3分後血圧 134/97 mmHg。臥位脈拍 68 bpm、立位3分後脈拍 74 bpm。体温 37.06 C。体重 90.27 kg。|
|2013年02月26日|Day 15 (N/A)|治験薬 Xanomeline 81 mg (PATCH, QD) へ増量。|
|2013年03月03日|Day 20 (N/A)|併用薬 ASPIRIN (2 TABLET, QD, ORAL) 開始。|
|2013年03月06日|Day 23 (N/A)|有害事象「NASOPHARYNGITIS」(Mild, Not Related) 発現。併用薬 SUDAFED (2 TABLET, QD, ORAL) 開始。|
|2013年03月07日|Day 24 (N/A)|有害事象「NASOPHARYNGITIS」回復。併用薬 SUDAFED 終了。|
|2013年03月09日|Day 26 (N/A)|併用薬 ASPIRIN 終了。|
|2013年03月11日|Day 28 (WEEK 4)|NPI-X Total Score 0点。Urate 7.6 mg/dL (HIGH)。臥位血圧 124/79 mmHg、立位3分後血圧 129/83 mmHg。臥位脈拍 67 bpm、立位3分後脈拍 71 bpm。体温 36.61 C。体重 89.36 kg。|
|2013年03月13日|Day 30 (AMBUL ECG REMOVAL)|臥位血圧 120/86 mmHg、立位3分後血圧 115/84 mmHg。臥位脈拍 61 bpm、立位3分後脈拍 70 bpm。体温 37.17 C。(起立性低血圧の可能性)|
|2013年03月18日|Day 35 (N/A)|治験薬 Xanomeline 81 mg 投与終了。|
|2013年03月19日|Day 36 (N/A)|有害事象「APPLICATION SITE ERYTHEMA」(Moderate, Possible) 発現。有害事象「APPLICATION SITE PRURITUS」(Moderate, Possible) 発現。有害事象「APPLICATION SITE VESICLES」(Moderate, Possible) 発現。有害事象「MICTURITION URGENCY」回復。有害事象「SUDDEN DEATH」回復 (医学的に疑義あり)。併用薬 ALOES (1 VIAL, QD, TOPICAL) 開始、同日終了。併用薬 WESTCORT (1 VIAL, BID, TOPICAL) 開始。|
|2013年03月21日|Day 38 (N/A)|併用薬 WESTCORT 終了。|
|2013年03月23日|Day 40 (WEEK 6)|有害事象により治験中止。ADAS-Cog(11) スコア 31点 (悪化)。CIBIC+ スコア 5 (Minimal worsening)。NPI-X Total Score 0点。DAD評価実施 (多くの項目で改善)。Urate 5.9 mg/dL (NORMAL)。臥位血圧 138/84 mmHg、立位3分後血圧 131/81 mmHg。臥位脈拍 58 bpm (徐脈傾向)、立位3分後脈拍 65 bpm。体温 37.33 C (微熱？)。体重 90.27 kg。|
|2013年03月24日|Day 41 (N/A)|併用薬 NEOSPORIN /USA/ (1 VIAL, PRN, TOPICAL) 開始、同日終了。|
|2013年03月25日|Day 42 (N/A)|併用薬 HISMANAL (10 mg, QD, ORAL) 開始 (併用禁止薬の可能性)。|
|2013年03月27日|Day 44 (N/A)|併用薬 DHEA (25 mg, QD, ORAL) 開始。併用薬 MELATONIN (2 mg, QD, ORAL) 開始。|
|2013年03月30日|Day 47 (N/A)|併用薬 DHEA 終了。併用薬 MELATONIN 終了。併用薬 MEDROL DOSEPAK (4 mg, PRN, ORAL) 開始 (併用禁止薬の可能性)。|
|2013年04月07日|Day 55 (AE FOLLOW-UP)|AE Follow-up Visit実施。参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象として「SUDDEN DEATH」が報告されているが、Severityが「MILD」、Outcomeが「RECOVERED/RESOLVED」と記録されている。これは医学的にありえず、報告用語または評価が根本的に誤っている可能性が高い。参加者の安全性に関わる極めて重大なデータ不整合であり、早急な確認が必要。
        *   **根拠:** 「突然死」が「軽度」であり、「回復/軽快」することは医学的にありえない。データの信頼性を著しく損ない、安全性評価に重大な影響を与える。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'SUDDEN DEATH'
            *   [Sequence Number(AE.AESEQ)] = 6
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-02-15'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-03-19'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 治験期間中に血圧および脈拍の変動が見られる。特にDay 13-14の血圧上昇傾向、Day 30の立位血圧低下（収縮期115mmHg）、Day 40の臥位脈拍58bpm（徐脈）は臨床的に注意が必要。Xanomelineはムスカリン作動薬であり、心血管系への影響（徐脈、血圧変動）が知られているため、これらの変動が治験薬と関連している可能性を考慮する必要がある。参加者の安全性モニタリングの観点から、これらの変動の臨床的意義について評価が必要。
        *   **根拠:** Xanomelineの薬理作用と、観察された血圧・脈拍の変動パターン。特に起立性低血圧や徐脈は転倒などのリスクにつながる可能性がある。
        *   **関連データ:**
            *   VSドメインの血圧・脈拍データ (Day 13, 14, 30, 40)
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', 'DIABP', 'PULSE'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有効性評価において、ADAS-Cog(11)およびCIBIC+の結果（悪化または変化なし）と、DADの結果（多くの項目で改善）に乖離が見られる。ADAS-Cog/CIBIC+は認知機能や全般的臨床症状の評価、DADは日常生活動作の介護者評価であり、評価側面の違いや評価者の違い（CIBIC+は臨床家、DADは介護者）が影響している可能性がある。しかし、この乖離は有効性の解釈に影響を与える可能性があり、理由について考察が必要。
        *   **根拠:** 主要評価項目（ADAS-Cog, CIBIC+）と副次評価項目（DAD）の結果の一貫性の欠如。
        *   **関連データ:**
            *   QSドメインのADAS-Cog(11) Total Score (QSTESTCD='ACTOT')
            *   QSドメインのCIBIC+ (QSTESTCD='CIBIC')
            *   QSドメインのDAD 各項目 (QSTESTCD='DAITM01' - 'DAITM40')

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** AEドメインに記録された「SUDDEN DEATH」(AESEQ=6)の転帰が「RECOVERED/RESOLVED」となっており、DMドメインの死亡フラグ(DTHFL)や死亡日(DTHDTC)が空欄であることと形式的には矛盾しないが、医学的にありえない記録となっている。これはデータ入力エラーまたは有害事象の評価・記録に関する重大な誤りを示唆しており、データの信頼性を著しく損なう。
        *   **根拠:** 医学的に「突然死」からの「回復/軽快」はありえない。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'SUDDEN DEATH'
            *   [Sequence Number(AE.AESEQ)] = 6
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Subject Death Flag(DM.DTHFL)] = ''
            *   [Date/Time of Death(DM.DTHDTC)] = ''
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** MHドメインに記録された既往歴「DEPRESSION (ANXIETY)」の開始日(MHSTDTC)が欠損している。プロトコルの除外基準[13]（スクリーニング前3ヶ月以内のうつ病エピソード）および[14]（過去5年以内の精神疾患歴）への適合性を正確に評価するために開始日情報が必要。
        *   **根拠:** 除外基準の評価に必要なデータが欠損している。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'DEPRESSION (ANXIETY)'
            *   [Sequence Number(MH.MHSEQ)] = 1
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** DMドメインの同意取得日時(RFICDTC)が欠損している。Define.xmlのコメントには「データベースに入力されなかった」とあるが、同意取得日と治験手順開始日の前後関係を確認できず、GCP遵守の観点から問題となる可能性がある。
        *   **根拠:** GCP上、同意取得は治験関連手順開始前に必須であり、その記録が必要。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** EXドメインの治験薬投与記録はDay 35 (2013-03-18)で終了しているが、DSドメインによると治験中止はDay 40 (2013-03-23)である。プロトコル3.10.1では、中止決定後、中止訪問まで漸減投与（50cm2パッチを継続）を行うと規定されているが、Day 36からDay 40までの投与記録が存在しない。漸減投与が行われなかったのか、データが欠損しているのか不明であり、実際の曝露量評価やプロトコル遵守状況の確認に影響する。
        *   **根拠:** 治験薬投与記録と中止日、およびプロトコルの中止時投与規定との間の不整合。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-03-18' (for EXSEQ=2)
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-03-23'
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、有害事象「VOMITING」が同じ発現日(2013-02-12)・回復日(2013-02-12)で2回記録されている(AESEQ=1, AESEQ=2)。重複記録の可能性がある。
        *   **根拠:** 同一事象が同一日に発現・回復で複数記録されている。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VOMITING'
            *   [Sequence Number(AE.AESEQ)] = 1, 2
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-02-12'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-02-12'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用禁止薬である可能性のあるHISMANAL (Astemizole) がDay 42から使用されている。プロトコル3.4.2.2 [31b] r) では、Hismanalは1週間のwashoutが必要と記載されており、治験期間中の使用は禁止されている可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] r) (p.22)
        *   **根拠:** プロトコルの併用禁止薬リストとCMデータとの照合。AstemizoleはQT延長リスクがあり、安全性上の懸念がある。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HISMANAL'
            *   [Sequence Number(CM.CMSEQ)] = 14
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-25' (Day 42)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用禁止薬である可能性のあるMEDROL DOSEPAK (Methylprednisolone, 全身性ステロイド) がDay 47から使用されている。プロトコル3.4.2.2 [31b] k) では、全身性ステロイドは2週間のwashoutが必要と記載されており、治験期間中の使用は禁止されている可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] k) (p.20)
        *   **根拠:** プロトコルの併用禁止薬リストとCMデータとの照合。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'MEDROL DOSEPAK'
            *   [Sequence Number(CM.CMSEQ)] = 17
            *   [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-30' (Day 47)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたECG評価（Screening, Visit 4, 5, 7, 8, 9, 10, 11, 12, 13, ET）および24時間ホルター心電図評価（Visit 2実施, Visit 3除去）に関するデータが提供されていない。これらの評価が実施されなかった場合、プロトコルからの逸脱となり、特に心血管系の安全性評価が不十分となる。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 (p.35), Schedule of Events (Attachment LZZT.1, p.53-54)
        *   **根拠:** プロトコルで規定された安全性評価のデータが存在しない。
        *   **関連データ:** (ECG, Holter ECGドメインデータなし)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された薬物動態(PK)評価のための採血（Visit 3, 4, 5, 7, 9, 11）に関するデータが提供されていない。PK評価が実施されなかった場合、プロトコルからの逸脱となる。
        *   **プロトコル該当箇所:** Section 3.9.2 (p.29), Schedule of Events (Attachment LZZT.1, p.53-54)
        *   **根拠:** プロトコルで規定されたPK評価のデータが存在しない。
        *   **関連データ:** (PKドメインデータなし)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[13]（スクリーニング前3ヶ月以内のうつ病エピソード）および[14]（過去5年以内の精神疾患歴）の評価に必要な既往歴「DEPRESSION (ANXIETY)」の開始日が不明であるため、適格性の確認が不十分である可能性がある。もし基準に抵触していた場合、プロトコル逸脱となる。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [13], [14] (p.13)
        *   **根拠:** 除外基準評価に必要な情報（既往歴開始日）の欠損。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'DEPRESSION (ANXIETY)'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日時(DM.RFICDTC)が欠損しており、治験手順開始前に同意が適切に取得されたか確認できない。GCP違反の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 (p.49)
        *   **根拠:** GCP要件である同意取得記録の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル3.10.1では、治験中止決定後、中止訪問まで漸減投与（50cm2パッチを継続）を行うと規定されているが、EXデータからはDay 35で投与が終了しており、Day 36以降の漸減投与の記録がない。規定通りの漸減投与が行われなかった場合、プロトコル逸脱となる。
        *   **プロトコル該当箇所:** Section 3.10.1 (p.38)
        *   **根拠:** プロトコルの中止時投与規定と投与記録の不整合。
        *   **関連データ:**
            *   EXドメインデータ (Day 35で終了)
            *   DSドメインデータ (Day 40で中止)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として報告された「Reported Term for the Adverse Event」が「SUDDEN DEATH」について、Severityが「MILD」、Outcome of Adverse Eventが「RECOVERED/RESOLVED」と記録されています。これは医学的に考えられない内容です。記録された事象名、重症度、転帰が正しいか、詳細な臨床経過と合わせて至急ご確認ください。もし記録誤りであれば、正しい情報に修正をお願いします。これは参加者の安全性評価に関する重大な疑義です。
        *   **クエリ文面（英語）:** Regarding the AE with Reported Term 'SUDDEN DEATH' (AESEQ 6), the Severity is recorded as 'MILD' and Outcome as 'RECOVERED/RESOLVED'. This is medically implausible. Please urgently verify the accuracy of the reported term, severity, and outcome along with detailed clinical course. If this is a recording error, please correct the information accordingly. This is a critical query regarding patient safety assessment.
        *   **判断理由:** 医学的にありえない有害事象の記録であり、データの信頼性と安全性評価に致命的な影響を与えるため、緊急の確認・修正が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Adverse Event(AE.AETERM)] = 'SUDDEN DEATH', [Sequence Number(AE.AESEQ)] = 6, [Severity/Intensity(AE.AESEV)] = 'MILD', [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   関連する医学的知見: 突然死は最も重篤な転帰であり、軽快・回復することはありえない。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 30のVital Signsにおいて、臥位血圧120/86mmHgに対し立位3分後血圧が115/84mmHgと収縮期血圧の低下が見られます。また、Study Day 40の臥位脈拍が58 bpmと記録されています。これらの心血管系の変動について、臨床的な評価（症状の有無、治験薬との関連性評価を含む）をお知らせください。
        *   **クエリ文面（英語）:** On Study Day 30, VS data shows Supine BP 120/86mmHg and Standing (3min) BP 115/84mmHg. On Study Day 40, Supine Pulse Rate was 58 bpm. Please provide clinical assessment for these cardiovascular changes (including presence/absence of symptoms and assessment of relationship to study drug).
        *   **判断理由:** 治験薬の既知のリスク（心血管系への影響）に関連する可能性のある所見であり、参加者の安全性確保のため臨床評価の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン Day 30, Day 40の血圧・脈拍データ
            *   関連する医学的知見: Xanomelineの心血管系への影響（起立性低血圧、徐脈）。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 42から併用薬として「Reported Name of Drug, Med, or Therapy」が「HISMANAL」の使用が記録されています。プロトコルでは治験期間中の使用が禁止されている可能性があります。使用理由、期間、および治験薬との関連性に関する評価をご確認の上、お知らせください。併用禁止薬の使用はプロトコル逸脱に該当する可能性があります。
        *   **クエリ文面（英語）:** Concomitant medication 'HISMANAL' use is recorded starting on Study Day 42. This medication may be prohibited during the study per protocol (Section 3.4.2.2 [31b] r). Please confirm the reason for use, duration, and assessment of relationship to study drug. Use of prohibited medication may constitute a protocol deviation.
        *   **判断理由:** プロトコルで禁止されている可能性のある薬剤の使用であり、安全性リスク評価とプロトコル遵守の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HISMANAL', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-25'
            *   関連するプロトコル箇所: Section 3.4.2.2 [31b] r)
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 47から併用薬として「Reported Name of Drug, Med, or Therapy」が「MEDROL DOSEPAK」の使用が記録されています。プロトコルでは全身性ステロイドの使用が禁止されている可能性があります。使用理由、期間、および治験薬との関連性に関する評価をご確認の上、お知らせください。併用禁止薬の使用はプロトコル逸脱に該当する可能性があります。
        *   **クエリ文面（英語）:** Concomitant medication 'MEDROL DOSEPAK' use is recorded starting on Study Day 47. Systemic corticosteroids may be prohibited during the study per protocol (Section 3.4.2.2 [31b] k). Please confirm the reason for use, duration, and assessment of relationship to study drug. Use of prohibited medication may constitute a protocol deviation.
        *   **判断理由:** プロトコルで禁止されている可能性のある薬剤の使用であり、安全性リスク評価とプロトコル遵守の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'MEDROL DOSEPAK', [Start Date/Time of Medication(CM.CMSTDTC)] = '2013-03-30'
            *   関連するプロトコル箇所: Section 3.4.2.2 [31b] k)
    *   **クエリNo.:** Q-5 (関連指摘No.: D-2, P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 既往歴として報告された「Reported Term for the Medical History」が「DEPRESSION (ANXIETY)」について、「Start Date/Time of Medical History Event」が記録されていません。プロトコルの除外基準（スクリーニング前3ヶ月以内のうつ病エピソード、過去5年以内の精神疾患歴）への適合性を確認するため、開始日をお知らせください。
        *   **クエリ文面（英語）:** For the reported Medical History term 'DEPRESSION (ANXIETY)', the Start Date/Time is missing. Please provide the start date to confirm eligibility against exclusion criteria (episode of depression within 3 months of screening, history of mental illness within last 5 years).
        *   **判断理由:** 除外基準適合性の確認に必要な情報が欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'DEPRESSION (ANXIETY)', [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   関連するプロトコル箇所: Section 3.4.2.2 [13], [14]
    *   **クエリNo.:** Q-6 (関連指摘No.: D-3, P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 「Date/Time of Informed Consent」が記録されていません。治験実施手順開始前にインフォームド・コンセントが適切に取得されたことを確認するため、同意取得日時をお知らせください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please provide the date and time of informed consent to confirm it was obtained prior to initiation of study procedures.
        *   **判断理由:** GCP遵守を確認するために必須の情報が欠損しているため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   関連するプロトコル箇所: Section 5.1
    *   **クエリNo.:** Q-7 (関連指摘No.: D-4, P-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Study Day 40に治験が中止されていますが、治験薬の投与記録はStudy Day 35で終了しています。プロトコルでは中止決定後、中止訪問まで漸減投与（50cm2パッチを継続）が規定されています。Study Day 36からDay 40までの治験薬投与状況（漸減投与の有無、実施日、用量）についてご確認ください。
        *   **クエリ文面（英語）:** Study was discontinued on Study Day 40, but the last EX record is on Study Day 35. Protocol requires dose tapering (continue 50cm2 patch) until the discontinuation visit. Please confirm the study drug administration status (tapering実施有無, dates, dose) from Study Day 36 to Day 40.
        *   **判断理由:** 実際の治験薬曝露量とプロトコル遵守状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: EXドメインデータ, DSドメインデータ
            *   関連するプロトコル箇所: Section 3.10.1
    *   **クエリNo.:** Q-8 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているECG評価（Screening, Visit 4, 5, 7）および24時間ホルター心電図評価（Visit 2実施, Visit 3除去）のデータが確認できません。これらの評価が実施されたか、実施された場合はデータをご提供ください。未実施の場合は理由をお知らせください。
        *   **クエリ文面（英語）:** Data for protocol-specified ECG assessments (Screening, Visits 4, 5, 7) and Ambulatory ECG (Visit 2 collection, Visit 3 removal) are missing. Please confirm if these assessments were performed. If performed, please provide the data. If not performed, please provide the reason.
        *   **判断理由:** 重要な安全性評価の実施状況とデータを確認するため。
        *   **判断根拠:**
            *   関連するデータ: (ECG, Holter ECGドメインデータなし)
            *   関連するプロトコル箇所: Section 3.9.3.4.2, Schedule of Events (Attachment LZZT.1)
    *   **クエリNo.:** Q-9 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されている薬物動態(PK)評価のための採血（Visit 3, 4, 5, 7）のデータが確認できません。これらの評価が実施されたか、実施された場合はデータをご提供ください。未実施の場合は理由をお知らせください。
        *   **クエリ文面（英語）:** Data for protocol-specified pharmacokinetic (PK) blood sampling (Visits 3, 4, 5, 7) are missing. Please confirm if these samples were collected. If collected, please provide the data. If not collected, please provide the reason.
        *   **判断理由:** PK評価の実施状況とデータを確認するため。
        *   **判断根拠:**
            *   関連するデータ: (PKドメインデータなし)
            *   関連するプロトコル箇所: Section 3.9.2, Schedule of Events (Attachment LZZT.1)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-5)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価において、ADAS-Cog(11)/CIBIC+の結果とDADの結果に乖離が見られる。DADは介護者評価であり主観が入りやすいこと、評価している側面（日常生活動作 vs 認知機能/全般印象）が異なることが原因の可能性がある。今後の解析において、この乖離について考慮し、有効性の解釈に注意する。問い合わせは不要と判断。
        *   **判断理由:** データ自体に誤りがあるとは考えにくく、評価指標の特性や評価者の違いによる乖離の可能性が高いため、内部での解釈の問題と判断。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのADAS-Cog, CIBIC+, DADデータ
            *   関連する医学的知見: 各評価尺度の特性、評価者によるバイアスの可能性。
    *   **確認事項No.:** I-2 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「VOMITING」が同日に2件記録されている(AESEQ=1, 2)。重複記録の可能性が高い。データクリーニングプロセスで確認し、必要であれば1件に統合する。医療機関への問い合わせは不要と判断。
        *   **判断理由:** データ入力上の問題と考えられ、臨床的な安全性評価への影響は小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=1, 2)
    *   **確認事項No.:** I-3 (関連指摘No.: P-10, P-11)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** スクリーニング時の適格性確認に関連する一部データ（CNS Imaging適合性、Screening ECG、Folate、Syphilis、HbA1c）が欠損している。また、Urate値が基準値上限を超えているが、これが除外基準に該当するか不明確。ただし、本試験では適格性確認のみに使用するデータは収集されない運用方針であるため、これらの欠損や不明確さが直ちに問題とはならない可能性が高い。適格性は他の情報（MMSE, Hachinskiスコア等）から概ね満たされていると判断される。内部記録として残し、必要に応じて全体的な適格性評価の際に再検討する。
        *   **判断理由:** 適格性確認データは収集されない前提であり、他の主要な基準は満たされているため、現時点での影響は小さいと判断。
        *   **判断根拠:**
            *   関連するデータ: MH, LB, QSドメインのスクリーニング時データ
            *   関連するプロトコル箇所: Section 3.4.2.1, 3.4.2.2
            *   前提知識: 適格性確認のみのデータは収集されない。

---

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

---

# 01-701-1387のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    87歳、女性、白人（NOT HISPANIC OR LATINO）。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS, 2003年8月17日発症）、多発性関節炎、鼻漏、体位性めまい、義歯装着、白内障、足首浮腫（末梢性浮腫）、手のしびれ（感覚鈍麻）（いずれもSIGNIFICANT PRE-EXISTING CONDITION）、肺炎（1940年）、基底細胞癌（2011年3月）、失神感（めまい）（2011年）、扁桃摘出術（1936年）、抜歯（2003年）（いずれもHISTORICAL DIAGNOSIS）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2014年02月23日|Day -17 (SCREENING 1)|MMSE 11点。Hachinski Ischemic Score 0点。臥位血圧 72/146 mmHg、立位血圧 136/72 mmHg (1分後), 137/79 mmHg (3分後)。(臥位の拡張期血圧が異常に高く、収縮期が低い値。記録ミスの可能性あり)|
|2014年03月08日|Day -4 (SCREENING 2)|臥位血圧 153/81 mmHg、立位血圧 138/78 mmHg (1分後), 146/82 mmHg (3分後)。|
|2014年03月12日|Day 1 (BASELINE)|治験薬（プラセボ）投与開始。臥位血圧 159/69 mmHg。体重 59.42 kg (Screeningから1.36kg減少)。ADAS-Cog(11) Total Score 44点。NPI-X Total Score 26点。|
|2014年03月18日|Day 7 (N/A)|有害事象「DIARRHOEA」(MILD) 発現、同日回復。有害事象「HYPERHIDROSIS」(MILD) 発現、同日回復。(いずれも治験薬との関連性はREMOTEと評価)|
|2014年03月25日|Day 14 (WEEK 2)|治験薬（プラセボ）投与終了。中止理由「PROTOCOL VIOLATION」。最終ラボ評価実施。立位拡張期血圧 60 mmHg (1分後), 61 mmHg (3分後) (Baselineから低下傾向)。Sodium 146 mmol/L (HIGH)。ADAS-Cog(11) Total Score 44点 (Baselineから変化なし)。CIBIC+ Minimal improvement (3)。NPI-X Total Score 2点 (Baselineから改善)。|
|2014年08月27日|Day 169 (RETRIEVAL)|最終来院。臥位収縮期血圧 175 mmHg (高値)。ADAS-Cog(11) Total Score 59点 (Baselineから悪化)。CIBIC+ Moderate worsening (6)。NPI-X Total Score 16点 (Week 2から悪化、Agitation/Aggressionが新たに出現)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** Day 14にプロトコル違反で治験が中止されているが、具体的な違反内容が不明である。これが患者の安全性（例：報告されていないAE、血圧変動、高Na血症など）や有効性評価の信頼性に関わる問題（例：評価の欠落、不適切な実施）に起因する可能性を排除できない。また、Retrieval Visit (Day 169)で臥位収縮期血圧が175mmHgと高値を示しており、安全性上の懸念がある。プラセボ投与中止後の認知機能・精神症状の悪化も認められる。
        *   **根拠:** 中止理由が不明確な場合、背景に重大な問題が隠れている可能性がある。高齢者であり複数の合併症を持つため、安全性リスクは元々高い。中止後の血圧上昇や有効性評価の悪化は、疾患進行の可能性もあるが、中止イベントとの関連も含めて慎重な評価が必要。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'PROTOCOL VIOLATION'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 14
            *   [Systolic Blood Pressure(VS.VSSTRESN)] = 175 (Visit 201, Supine)
            *   [Study Day of Vital Signs(VS.VSDY)] = 169
            *   [ADAS-COG(11) Subscore(QS.QSSTRESN)] = 59 (Visit 201)
            *   [EXTENT OF CHANGE, IF ANY, SINCE BASELINE(QS.QSSTRESN)] = 6 (Visit 201, CIBIC+)
            *   [NPI-X (9) Total Score(QS.QSSTRESN)] = 16 (Visit 201)
            *   [Age(DM.AGE)] = 87
            *   MHドメインの既往歴

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** Screening 1 (Day -17) の臥位血圧測定値について、収縮期血圧(SYSBP)が72 mmHg、拡張期血圧(DIABP)が146 mmHgと記録されている。拡張期が収縮期より著しく高い値となっており、医学的に考えにくいため、記録ミスまたは測定エラーの可能性が高い。他の時点での血圧値との整合性も低い。
        *   **根拠:** 通常、拡張期血圧が収縮期血圧を上回ることはない。データの信頼性に影響する可能性があるが、Screening時の単発の値であり、その後の評価への直接的な影響は限定的と考えられる。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 72, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Study Day of Vital Signs(VS.VSDY)] = -17
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 146, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Study Day of Vital Signs(VS.VSDY)] = -17
    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** 同意取得日 (DM.RFICDTC) のデータが欠損している。同意取得の有無および治験手順開始前の同意取得を確認できない。
        *   **根拠:** 同意取得はGCPの根幹であり、参加者の権利保護の観点から極めて重要。記録の欠損は重大な問題。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準[5]で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施有無および結果がデータから確認できない。除外基準[12a] Stroke or vascular dementia の除外にも関わるため、適格性評価が不十分である可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [5], Section 3.4.2.2 [12a]
        *   **根拠:** 適格性確認に必要な評価データが不足している。不適格な患者が登録された場合、安全性リスクや試験結果の解釈に影響を与える可能性がある。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-2
        *   **重要度:** Critical
        *   **逸脱の可能性:** 選択基準[6]で要求されている同意取得に関する記録 (DM.RFICDTC) が欠損している。プロトコル Section 5.1 にも同意取得の重要性が記載されている。同意が適切に取得されたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 [6], Section 5.1
        *   **根拠:** 同意取得はGCPの必須要件であり、参加者の権利保護の根幹。記録欠損は重大な逸脱の可能性を示す。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b]の確認に必要なScreening時のECG結果、およびプロトコル Section 3.9.3.4.2 で規定されているVisit 2でのAmbulatory ECG、Visit 4でのECGの実施有無・結果がデータから確認できない。心血管系のリスク評価が不十分である可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [16b], Section 3.9.3.4.2
        *   **根拠:** プロトコルで規定された重要な安全性評価が実施されたか不明。特に心血管リスクのある高齢者では重要。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening時の血圧測定値に異常値の可能性 (D-1) や高値 (臥位収縮期 153mmHg@Day-4, 159mmHg@Day1) が見られる。除外基準[17f] Uncontrolled hypertension に該当しなかったか、評価が適切であったか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17f]
        *   **根拠:** 適格性基準の遵守確認が必要。高血圧は心血管イベントのリスク因子であり、安全性に関わる。
        *   **関連データ:**
            *   VSドメインの血圧データ (Screening 1, Screening 2, Baseline)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[29b] Positive syphilis screening with confirmatory testing の確認に必要な梅毒スクリーニングの結果がデータから確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [29b]
        *   **根拠:** 適格性確認に必要な評価データが不足している。
        *   **関連データ:** (該当データなし)
    *   **指摘No.:** P-6
        *   **重要度:** Critical
        *   **逸脱の可能性:** Day 14に「PROTOCOL VIOLATION」で治験中止となっている。プロトコルからの逸脱があったことを示唆するが、具体的な逸脱内容が不明。これが重大な逸脱（例：同意不備、重篤なAE隠蔽、併用禁止薬使用、主要評価未実施など）である可能性を否定できない。
        *   **プロトコル該当箇所:** Section 3.10.1 (Discontinuations)
        *   **根拠:** 中止理由の詳細が不明なため、逸脱の重大性や参加者の安全性・評価の信頼性への影響を評価できない。GCP遵守の観点からも確認が必要。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'PROTOCOL VIOLATION'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 14

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** Screening 1 (2014-02-23) の臥位でのバイタルサインについて、「Systolic Blood Pressure」が「72」mmHg、「Diastolic Blood Pressure」が「146」mmHgと記録されています。拡張期血圧が収縮期血圧より著しく高い値ですが、記録が正しいかご確認ください。もし誤りであれば修正をお願いします。
        *   **クエリ文面（英語）:** Regarding vital signs at Screening 1 (2014-02-23) while supine, Systolic Blood Pressure is recorded as '72' mmHg and Diastolic Blood Pressure as '146' mmHg. The diastolic value is unusually high compared to systolic. Please confirm if the recorded values are correct. If incorrect, please correct.
        *   **判断理由:** データの正確性確認のため。他の時点のデータからみて異常値の可能性が高く、データ品質確保の観点から確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 72, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Study Day of Vital Signs(VS.VSDY)] = -17; [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 146, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Study Day of Vital Signs(VS.VSDY)] = -17
    *   **クエリNo.:** Q-2 (関連指摘No.: P-1, P-3, P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者適格性確認についてお伺いします。プロトコルで要求されているスクリーニング時のCNSイメージング(Section 3.4.2.1 [5])、ECG(Section 3.4.2.2 [16b])、梅毒スクリーニング(Section 3.4.2.2 [29b])、およびVisit 2でのAmbulatory ECG(Section 3.9.3.4.2)の実施有無と結果について、記録を確認し、適格基準を満たしていたかをご教示ください。
        *   **クエリ文面（英語）:** Regarding subject eligibility confirmation: Please confirm if the screening CNS imaging (Sec 3.4.2.1[5]), ECG (Sec 3.4.2.2[16b]), syphilis screening (Sec 3.4.2.2[29b]), and Visit 2 Ambulatory ECG (Sec 3.9.3.4.2) were performed and met the eligibility criteria as per protocol.
        *   **判断理由:** 患者の適格性を担保するために必須の評価データが不足しているため。評価の信頼性確保の観点から確認が必要。
        *   **判断根拠:**
            *   関連するプロトコル箇所: Section 3.4.2.1 [5], Section 3.4.2.2 [12a], [16b], [29b], Section 3.9.3.4.2
    *   **クエリNo.:** Q-3 (関連指摘No.: P-2, D-2)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日について、「Date/Time of Informed Consent」が記録されていません。同意取得日と、同意が治験手順開始（Subject Reference Start Date/Time: 2014-03-12）より前に行われたことを確認し、ご回答ください。
        *   **クエリ文面（英語）:** Regarding informed consent date: The 'Date/Time of Informed Consent' is missing. Please confirm the date of informed consent and that it was obtained before the start of study procedures (Subject Reference Start Date/Time: 2014-03-12).
        *   **判断理由:** GCP遵守および参加者の権利保護の観点から、同意取得日とそのタイミングの確認が必須であるため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損), [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2014-03-12'
            *   関連するプロトコル箇所: Section 3.4.2.1 [6], Section 5.1
    *   **クエリNo.:** Q-4 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Screening時およびBaseline時の血圧について、臥位収縮期血圧が高値（例: Day -4 153mmHg, Day 1 159mmHg）を示しています。除外基準[17f] Uncontrolled hypertensionに該当しないと判断された根拠をご教示ください。
        *   **クエリ文面（英語）:** Regarding blood pressure at Screening and Baseline: Supine systolic blood pressure readings were elevated (e.g., 153 mmHg on Day -4, 159 mmHg on Day 1). Please provide the rationale for determining that exclusion criterion [17f] 'Uncontrolled hypertension' was not met.
        *   **判断理由:** 適格性基準の遵守を確認し、患者の安全性リスクを評価するため。
        *   **判断根拠:**
            *   関連するデータ: VSドメインの血圧データ (Screening 1, Screening 2, Baseline)
            *   関連するプロトコル箇所: Section 3.4.2.2 [17f]
    *   **クエリNo.:** Q-5 (関連指摘No.: P-6, M-1)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Day 14の中止理由について、「Standardized Disposition Term」が「PROTOCOL VIOLATION」と記録されています。参加者の安全性や試験評価の信頼性に関わる可能性もあるため、具体的なプロトコル違反の内容について詳細をご教示ください。
        *   **クエリ文面（英語）:** Regarding the reason for discontinuation on Day 14: The 'Standardized Disposition Term' is recorded as 'PROTOCOL VIOLATION'. As this could potentially impact subject safety or data reliability, please provide specific details of the protocol violation.
        *   **判断理由:** 中止理由の詳細が不明であり、安全性、評価の信頼性、GCP遵守への影響を評価できないため。
        *   **判断根拠:**
            *   関連するデータ: [Standardized Disposition Term(DS.DSDECOD)] = 'PROTOCOL VIOLATION', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 14
            *   関連するプロトコル箇所: Section 3.10.1
    *   **クエリNo.:** Q-6 (関連指摘No.: M-1)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 14 (WEEK 2) の検査結果について、「Sodium」が「146」mmol/Lと基準値上限を超えています。本結果の臨床的な意義について評価をお願いします。必要であればフォローアップ結果もご教示ください。
        *   **クエリ文面（英語）:** Regarding lab results on Day 14 (WEEK 2): The Sodium level was 146 mmol/L, which is above the upper reference limit. Please assess the clinical significance of this finding and provide follow-up results if available/applicable.
        *   **判断理由:** 軽微な検査値異常であるが、臨床的意義を確認し、参加者の安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Character Result/Finding in Std Format(LB.LBSTRESC)] = '146', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', [Study Day of Specimen Collection(LB.LBDY)] = 14
    *   **クエリNo.:** Q-7 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Retrieval Visit (Day 169) のバイタルサインについて、臥位での「Systolic Blood Pressure」が「175」mmHgと高値です。本結果の臨床的な意義について評価をお願いします。必要であればフォローアップ結果もご教示ください。
        *   **クエリ文面（英語）:** Regarding vital signs at Retrieval Visit (Day 169): The supine Systolic Blood Pressure was 175 mmHg, which is elevated. Please assess the clinical significance of this finding and provide follow-up results if available/applicable.
        *   **判断理由:** 投与終了後の血圧高値であり、患者の安全性確保のため臨床的評価が必要。
        *   **判断根拠:**
            *   関連するデータ: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 175, [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', [Study Day of Vital Signs(VS.VSDY)] = 169

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Day 7に軽度の下痢と多汗症が発現し同日回復している。プラセボ投与期間中であり、治験薬との関連性は低い(REMOTE)と評価されている。有害事象として記録されていることを確認。
        *   **判断理由:** 軽微な一過性の事象であり、因果関係も低いと評価されているため、医療機関への問い合わせは不要と判断。記録として残す。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=1, 2)
    *   **確認事項No.:** I-2 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** SUPPLBドメインにLBTMSHI (LAB RESULT/UPPER LIMIT OF NORMAL) および ENDPOINT フラグが記録されている。これらの派生変数の定義、計算方法、および試験における具体的な使用目的について、統計解析計画書(SAP)等を参照し内部で確認する。
        *   **判断理由:** データ構造や派生変数の定義に関する内部確認事項であり、医療機関への問い合わせは不要。データ利用のために内部での明確化が必要。
        *   **判断根拠:**
            *   関連するデータ: SUPPLBドメイン

---

# 01-702-1082のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
84歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2007年05月17日発症、PRIMARY DIAGNOSIS）、月経前疼痛（軽度、SIGNIFICANT PRE-EXISTING CONDITION）、大動脈弁狭窄症（軽度、SIGNIFICANT PRE-EXISTING CONDITION）が報告されている。教育レベルは18年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年07月03日|Day -23 (SCREENING 1)|スクリーニング検査実施。主な異常値: BUN 25 mg/dL (HIGH), HCT 49.0% (HIGH), WBC 14.77 THOU/uL (HIGH), VITB12 946 pg/mL (HIGH)。MMSE=23, Hachinski=0。身長 154.94 cm, 体重 54.43 kg。|
|2013年07月07日|Day -19 (N/A)|有害事象「NEUTROPHIL COUNT INCREASED」(MILD), 「URINE ANALYSIS ABNORMAL」(MILD), 「WHITE BLOOD CELL COUNT INCREASED」(MILD) 発現。|
|2013年07月24日|Day -2 (SCREENING 2 / UNSCHEDULED 1.1)|検査実施。主な異常値: ALT 37 U/L (HIGH), AST 44 U/L (HIGH), BUN 27 mg/dL (HIGH)。立位1分でのバイタルサイン一部欠測。有害事象「URINE ANALYSIS ABNORMAL」終了。|
|2013年07月26日|Day 1 (BASELINE)|治験薬 Xanomeline 54mg パッチ投与開始。ベースライン評価実施。ADAS-Cog(11)=9, NPI-X Total=4 (Anxiety=4)。有害事象「NEUTROPHIL COUNT INCREASED」, 「WHITE BLOOD CELL COUNT INCREASED」終了。|
|2013年08月07日|Day 13 (AMBUL ECG PLACEMENT)|バイタルサイン測定。|
|2013年08月08日|Day 14 (WEEK 2)|検査実施。主な異常値: ALT 35 U/L (HIGH), AST 41 U/L (HIGH), CK 320 U/L (HIGH)。NPI-X Total=0。治験薬投与終了（EXレコード上）。|
|2013年08月09日|Day 15 (N/A)|治験薬 Xanomeline 54mg パッチ投与再開（EXレコード上）。|
|2013年08月24日|Day 30 (WEEK 4)|検査実施。主な異常値: AST 35 U/L (HIGH)。NPI-X Total=3 (Depression=1, Anxiety=1, Disinhibition=1)。DAD評価で「食事の必要性を判断する」が「いいえ」に変化。|
|2013年09月02日|Day 39 (N/A)|有害事象「RECTAL HAEMORRHAGE」(MILD) 発現。|
|2013年09月04日|Day 41 (AMBUL ECG REMOVAL)|バイタルサイン測定。臥位脈拍 50 bpm、立位3分後収縮期血圧 86 mmHg。|
|2013年09月06日|Day 43 (WEEK 6)|検査実施。主な異常値: BUN 30 mg/dL (HIGH), WBC 13.18 THOU/uL (HIGH)。NPI-X Total=3 (Depression=1, Anxiety=1, Disinhibition=1)。有害事象「RECTAL HAEMORRHAGE」終了。|
|2013年09月09日|Day 46 (N/A)|有害事象「APPLICATION SITE IRRITATION」(MILD) 発現。|
|2013年09月24日|Day 61 (N/A)|有害事象「APPLICATION SITE IRRITATION」終了。併用薬「HYDROCORTISONE, TOPICAL」開始。|
|2013年09月28日|Day 65 (WEEK 8)|検査実施。主な異常値: AST 36 U/L (HIGH), CK 177 U/L (HIGH), WBC 10.76 THOU/uL (HIGH)。体重 53.98 kg (-0.45kg from Baseline)。ADAS-Cog(11)=11, CIBIC+=4 (No Change)。NPI-X Total=2 (Depression=1, Anxiety=1)。DAD評価で一部項目改善。|
|2013年10月12日|Day 79 (WEEK 10 (T))|有害事象「SKIN IRRITATION」(MODERATE) 発現。NPI-X Total=6 (Depression=4, Disinhibition=2)。|
|2013年10月13日|Day 80 (N/A)|治験薬 Xanomeline 54mg パッチ投与終了。|
|2013年10月31日|Day 98 (N/A)|有害事象「SKIN IRRITATION」終了。併用薬「HYDROCORTISONE, TOPICAL」終了。|
|2013年11月17日|Day 115 (WEEK 12)|試験中止（自己都合：パッチが不便で痒い、錠剤を希望）。最終評価実施。主な異常値: KETONES 1 (ABNORMAL), PROT 8.1 g/dL (HIGH), WBC 14.38 THOU/uL (HIGH)。体重 50.8 kg (-3.63kg from Baseline, -3.18kg from Week 8)。ADAS-Cog(11)=8, CIBIC+=4 (No Change)。NPI-X Total=5 (Depression=1, Apathy=2, Disinhibition=1, Irritability=1)。DAD評価で複数項目悪化。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** スクリーニング時(Day -23)およびWeek 6(Day 43)以降、WBC高値が断続的に認められる。スクリーニング時のAE「WHITE BLOOD CELL COUNT INCREASED」はDay 1に回復と記録されているが、その後も高値が続いている。感染症や他の炎症を示唆する所見はAEや他のデータからは明確でないが、原因の評価が必要。
        *   **根拠:** WBCは炎症や感染の指標となる。持続的な高値は、潜在的な医学的問題を示唆する可能性がある。特に高齢者や基礎疾患を持つ患者では注意が必要。
        *   **関連データ:**
            *   [Leukocytes(LB.LBTESTCD)] = 'WBC'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -23, 1, 14, 30, 43, 65, 115
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 14.77, 8.86, 10.26, 9.13, 13.18, 10.76, 14.38
            *   [Reference Range Indicator(LB.LBNRIND)] = HIGH, NORMAL, NORMAL, NORMAL, HIGH, HIGH, HIGH
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'WHITE BLOOD CELL COUNT INCREASED'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = -19
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 1
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「RECTAL HAEMORRHAGE」(直腸出血) がDay 39-43に軽度で発現し回復しているが、治験薬との関連性が「NONE」と評価されている。Xanomelineはコリン作動薬であり、消化管への影響（潰瘍悪化、蠕動亢進など）の可能性は否定できない。評価根拠の確認が必要。
        *   **根拠:** コリン作動薬は消化管運動や分泌を亢進させる作用を持つため、消化管出血のリスクを考慮する必要がある。関連性評価の妥当性を確認することは安全性評価上重要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'RECTAL HAEMORRHAGE'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 39
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 43
            *   [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Causality(AE.AEREL)] = 'NONE'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 有害事象「APPLICATION SITE IRRITATION」(Day 46-61, MILD) および「SKIN IRRITATION」(Day 79-98, MODERATE) が発現。後者は中止理由（痒み）と関連している可能性が高い。Hydrocortisone topicalが使用され、AEは回復している。TTS製剤における皮膚刺激は一般的な副作用でありうるが、中等度の事象であり中止につながっているため、詳細な状況確認が望ましい。
        *   **根拠:** 経皮吸収製剤では適用部位の皮膚反応が問題となることがある。事象の程度と中止への影響を考慮すると、安全性評価として重要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE IRRITATION', 'SKIN IRRITATION'
            *   [Severity/Intensity(AE.AESEV)] = 'MILD', 'MODERATE'
            *   [Reported Term for the Disposition Event(DS.DSTERM)] = 'PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS\'PILLS\'"'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** ALT, ASTが投与前から複数回基準値上限を超えている (Day -2, 14, 30, 65)。CKもDay 14とDay 65で高値を示している。特にDay 14のCK値(320 U/L)は基準値上限(169 U/L)の約1.9倍。関連する筋肉系のAE報告はない。薬剤性肝障害や横紋筋融解症の可能性は低いかもしれないが、変動パターンとして注意が必要であり、臨床的意義の評価が必要。
        *   **根拠:** 肝酵素やCKの上昇は、薬剤による臓器障害の可能性を示唆する重要な安全性シグナルとなりうる。原因不明の変動は評価が必要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', 'AST', 'CK'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -2, 14, 30, 65
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = ALT(37, 35, 26, 24), AST(44, 41, 35, 36), CK(119, 320, 116, 177)
            *   [Reference Range Indicator(LB.LBNRIND)] = ALT(HIGH, HIGH, NORMAL, NORMAL), AST(HIGH, HIGH, HIGH, HIGH), CK(NORMAL, HIGH, NORMAL, HIGH)
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** BUNがスクリーニング時(Day -23, -2)およびWeek 6(Day 43)で基準値上限を超えている。クレアチニンは正常範囲内であり、腎機能障害の可能性は低いと考えられるが、脱水等の他の要因がないか注意が必要。
        *   **根拠:** BUNは腎機能以外にも脱水や食事（高蛋白食）などの影響を受ける。臨床的意義は低い可能性もあるが、念のため記録。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BUN'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -23, -2, 14, 30, 43, 65, 115
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 8.925, 9.639, 6.426, 7.14, 10.71, 8.568, 8.211
            *   [Reference Range Indicator(LB.LBNRIND)] = HIGH, HIGH, NORMAL, NORMAL, HIGH, NORMAL, NORMAL
    *   **指摘No.:** M-6
        *   **重要度:** Major
        *   **内容:** 最終評価時(Day 115)に尿中ケトン体が陽性(ABNORMAL)となっている。糖尿病の既往歴はなく、血糖値(GLUC)も正常範囲内。同時期に体重減少が顕著であることから、食事摂取不良や代謝状態の変化が関連している可能性がある。
        *   **根拠:** ケトン尿は、飢餓、脱水、糖尿病性ケトアシドーシスなどで見られる。体重減少と併せて、患者の栄養状態や全身状態の評価が必要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'KETONES'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 115
            *   [Character Result/Finding in Std Format(LB.LBSTRESC)] = '1'
            *   [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL'
            *   [Weight(VS.VSTESTCD)] = 'WEIGHT'
            *   [Study Day of Vital Signs(VS.VSDY)] = 115
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 50.8
    *   **指摘No.:** M-7
        *   **重要度:** Major
        *   **内容:** Day 41 (AMBUL ECG REMOVAL Visit) にて、臥位脈拍 50 bpm、立位3分後収縮期血圧 86 mmHgと、徐脈および低血圧傾向が認められる。Xanomelineはコリン作動薬であり、心血管系への影響（徐脈、血圧低下）が懸念される。関連する症状（めまい、ふらつき、失神など）の有無を確認する必要がある。
        *   **根拠:** コリン作動薬の薬理作用として徐脈や血圧低下が知られている。特に高齢者では失神等のリスクにつながる可能性があるため、症状の有無と臨床的意義の評価が重要。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', 'SYSBP'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', 'STANDING'
            *   [Study Day of Vital Signs(VS.VSDY)] = 41
            *   [Planned Time Point Name(VS.VSTPT)] = 'AFTER LYING DOWN FOR 5 MINUTES', 'AFTER STANDING FOR 3 MINUTES'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = PULSE(50), SYSBP(86)
    *   **指摘No.:** M-8
        *   **重要度:** Major
        *   **内容:** Week 8 (Day 65) から Week 12 (Day 115) にかけて、約7週間で3.18kgの体重減少 (-5.9%) が認められる。アルツハイマー病の進行に伴う食欲不振や、薬剤の影響、他の医学的問題などが考えられる。臨床的に有意な体重減少の可能性があり、原因評価が必要。
        *   **根拠:** 短期間での意図しない体重減少は、栄養状態の悪化や潜在的な疾患を示唆する可能性がある。原因の特定と適切な対応が必要。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'WEIGHT'
            *   [Study Day of Vital Signs(VS.VSDY)] = -23, 14, 30, 43, 65, 115
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 54.43, 54.43, 54.43, 54.43, 53.98, 50.8
    *   **指摘No.:** M-9
        *   **重要度:** Major
        *   **内容:** 有効性評価指標間で結果が一貫していない。ADAS-Cog(11)はWeek 12でベースラインより改善したが、CIBIC+は一貫して変化なし。NPI-X Total scoreはWeek 10以降ベースラインより悪化、DADもWeek 12で食事や金銭管理など複数の項目が悪化している。評価の信頼性や薬剤効果の解釈に影響を与える可能性。
        *   **根拠:** 複数の有効性評価指標を用いる場合、その結果の一貫性は評価の妥当性を判断する上で重要。大きな乖離がある場合は、その理由を考察する必要がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'NPTOT', 'DAITM*'
            *   [Visit Number(QS.VISITNUM)] = 3, 8, 9, 8.1 (NPI-X)
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] / [Finding in Original Units(QS.QSORRES)]

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「APPLICATION SITE IRRITATION」(Day 46-61) の終了日と、併用薬「HYDROCORTISONE, TOPICAL」の開始日(Day 61)が同日である。また、有害事象「SKIN IRRITATION」(Day 79-98) の期間中に同併用薬が使用されている(終了日Day 98)。AEとCMの記録タイミングや期間に若干のずれがある可能性があるが、臨床的な流れとしては矛盾しない。
        *   **根拠:** AEとそれに対する処置(CM)の日付関係は整合しているべきだが、記録上のわずかなずれは臨床的に大きな問題とならない場合もある。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE IRRITATION', 'SKIN IRRITATION'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 46, 79
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 61, 98
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'HYDROCORTISONE, TOPICAL'
            *   [Study Day of Start of Medication(CM.CMSTDY)] = 61
            *   [Study Day of End of Medication(CM.CMENDY)] = 98
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 有害事象「WHITE BLOOD CELL COUNT INCREASED」はDay 1に回復(AEENDY=1)と記録されているが、LBデータではその後もWBCが高値を示している(Day 43, 65, 115)。AEの転帰評価と実際の検査値データが矛盾している。安全性評価の正確性に影響する。
        *   **根拠:** AEの転帰と客観的データ(検査値)の整合性は、AE評価の妥当性を担保する上で重要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'WHITE BLOOD CELL COUNT INCREASED'
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 1
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED'
            *   [Leukocytes(LB.LBTESTCD)] = 'WBC'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 43, 65, 115
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 13.18, 10.76, 14.38
            *   [Reference Range Indicator(LB.LBNRIND)] = HIGH, HIGH, HIGH
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** Visit 2 (Day -2)において、立位1分後の拡張期血圧、収縮期血圧、脈拍数が欠測(VSSTAT = 'NOT DONE')となっている。欠測理由が不明。起立性低血圧の評価など、安全性評価の一部が不完全となる可能性がある。
        *   **根拠:** プロトコルで規定された測定値の欠損は、評価の完全性を損なう可能性がある。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', 'SYSBP', 'PULSE'
            *   [Vital Signs Position of Subject(VS.VSPOS)] = 'STANDING'
            *   [Visit Number(VS.VISITNUM)] = 2
            *   [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE'
            *   [Completion Status(VS.VSSTAT)] = 'NOT DONE'
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** QSドメインのNPI-Xデータにおいて、症状がない場合の記録方法に一貫性がないように見える。症状がない場合にFrequency, Severity, Distressが記録されずScore (NPITMxS) のみが0の場合と、Presentフラグ (NPITMx) がABSENTで記録されている場合がある。データ入力や処理の一貫性の問題の可能性。
        *   **根拠:** データ記録の一貫性はデータ品質の基本であり、解析時の誤解を防ぐために重要。
        *   **関連データ:**
            *   [Domain Abbreviation(QS.DOMAIN)] = 'QS'
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [Question Short Name(QS.QSTESTCD)] = 'NPITM04', 'NPITM04F', 'NPITM04V', 'NPITM04D', 'NPITM04S'
            *   [Visit Number(QS.VISITNUM)] = 3, 5
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 有害事象「NEUTROPHIL COUNT INCREASED」が報告されているが、対応する好中球数のLBデータが存在しない。AEの評価や背景情報の確認が困難。
        *   **根拠:** AEと関連する検査値データが存在しない場合、AE評価の客観性が低下する。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'NEUTROPHIL COUNT INCREASED'
            *   LBドメインに好中球(NEUT)のデータなし
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、既往歴「PREMENSTRUAL PAIN」および「AORTIC STENOSIS」の開始日(MHSTDTC)が記録されていない。データの完全性の観点から記録が望ましい。
        *   **根拠:** 既往歴の開始日は、イベントのタイムラインを理解する上で有用な情報。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'PREMENSTRUAL PAIN', 'VERBATIM_1100'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** D-7
        *   **重要度:** Major
        *   **内容:** DMドメインにおいて、インフォームド・コンセント取得日(RFICDTC)が記録されていない。GCP遵守およびプロトコル遵守の確認に不可欠な情報が欠損している。
        *   **根拠:** 同意取得日は、治験が倫理的に実施されていることを示す基本的な情報。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Inclusion Criteria [5]で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施有無および結果に関する情報がデータセットに含まれていない。選択基準を満たしているか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 選択基準の遵守は、試験の対象集団の均質性を担保し、結果の解釈可能性を確保するために重要。
        *   **関連データ:** 関連データなし (情報の欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Inclusion Criteria [6]で要求されているインフォームド・コンセントの取得に関する情報（取得日）がDM.RFICDTCに記録されていない。同意取得が治験手順開始前に行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [6], Section 5.1
        *   **根拠:** 同意取得はGCPの根幹であり、参加者の権利保護の観点から極めて重要。
        *   **関連データ:** [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [16b]で規定されているスクリーニング時のECG所見に関する情報、およびSection 3.9.3.4.2, 3.9.4で規定されている試験期間中のECG評価に関するデータがデータセットに含まれていない。除外基準該当の有無、および安全性モニタリングが適切に行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b], Section 3.9.3.4.2, Section 3.9.4
        *   **根拠:** 心血管系の安全性は本試験の重要な評価項目であり、規定された評価の実施と結果の確認は不可欠。
        *   **関連データ:** 関連データなし (情報の欠損)
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時(Day -23)のWBC値(14.77 THOU/uL)が基準値上限(10.7 THOU/uL)を超えており、Exclusion Criteria [27b]に抵触する可能性がある。プロトコルでは臨床的に意義がないと判断されれば組み入れ可とされているが、その判断記録が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準違反は、参加者の安全性リスクを高め、試験結果の妥当性に影響を与える可能性がある。
        *   **関連データ:**
            *   [Leukocytes(LB.LBTESTCD)] = 'WBC'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -23
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 14.77
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [28b]で評価が要求されているFolateの検査データがない。除外基準を満たしているか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準に関連する検査の未実施または未報告は、プロトコル逸脱の可能性を示す。
        *   **関連データ:** LBドメインにFolateのデータなし
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時(Day -23)のVitamin B12値(946 pg/mL)が基準値上限(900 pg/mL)を超えており、Exclusion Criteria [28b]に抵触する可能性がある。プロトコルではビタミンサプリメント服用中の場合は許容されるとあるが、サプリメント服用の記録がない。組み入れ判断の妥当性確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準違反の可能性があり、組み入れの妥当性を確認する必要がある。
        *   **関連データ:**
            *   [Vitamin B12(LB.LBTESTCD)] = 'VITB12'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -23
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 697.9588 (pmol/L)
            *   [Result or Finding in Original Units(LB.LBORRES)] = '946' (pg/mL)
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   CMドメインにビタミンサプリメントの記録なし
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [28b]で評価が要求されている甲状腺機能検査のうち、TSH以外のデータ(例: Free T4, T3 Uptakeなど)がない。除外基準を満たしているか完全に確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準に関連する検査が一部未実施または未報告の可能性がある。
        *   **関連データ:** LBドメインにTSH以外の甲状腺機能検査データなし
    *   **指摘No.:** P-8
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル Exclusion Criteria [29b]で要求されている梅毒スクリーニングの実施有無および結果に関する情報がない。除外基準を満たしているか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 除外基準に関連する検査の未実施または未報告の可能性がある。
        *   **関連データ:** 関連データなし (情報の欠損)
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験薬投与がDay 80で終了している。プロトコルではLow Dose群は26週間(約182日)の投与が計画されている。早期中止(Day 115)よりも前に投与が終了しており、その理由が不明。プロトコルからの逸脱の可能性。
        *   **プロトコル該当箇所:** Section 3.1 (Summary of Study Design), Figure LZZT.1
        *   **根拠:** 計画された投与期間からの逸脱は、有効性・安全性評価における薬剤曝露量の評価に影響を与える。
        *   **関連データ:**
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-07-26', '2013-08-09'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-08-08', '2013-10-13'
            *   [Study Day of Start of Treatment(EX.EXSTDY)] = 1, 15
            *   [Study Day of End of Treatment(EX.EXENDY)] = 14, 80
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-11-17'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 115
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル Section 3.9.3.4.2, 3.9.4で規定されているVisit 2での24時間Ambulatory ECGの実施有無および結果に関するデータがない。安全性モニタリング計画からの逸脱の可能性。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2, Section 3.9.4
        *   **根拠:** 規定された安全性評価の未実施は、参加者の安全性監視の点で問題となる可能性がある。
        *   **関連データ:** 関連データなし (情報の欠損)
    *   **指摘No.:** P-11
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 1 (Screening 1) の実施日(Day -23)が、計画日(Day -7)から16日早期にずれている。プロトコル Section 3.1ではスクリーニング期間は2週間以内とされているため、逸脱の可能性。
        *   **プロトコル該当箇所:** Section 3.1, Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** スクリーニング期間の規定からの逸脱は、適格性評価のタイミングに影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Name(SV.VISIT)] = 'SCREENING 1'
            *   [Visit Number(SV.VISITNUM)] = 1
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-07-03'
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2013-07-26'
            *   [Planned Study Day of Visit(TV.VISITDY)] = -7 (for VISITNUM=1)
    *   **指摘No.:** P-12
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 6 (AMBUL ECG REMOVAL) の実施日(Day 41)が、計画日(Day 30)から11日遅れている。プロトコルにVisit Windowの規定はないが、大幅な遅延。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 評価スケジュールの遅延は、データの時間的な比較可能性に影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Name(SV.VISIT)] = 'AMBUL ECG REMOVAL'
            *   [Visit Number(SV.VISITNUM)] = 6
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-09-04' (Day 41)
            *   [Planned Study Day of Visit(TV.VISITDY)] = 30 (for VISITNUM=6)
    *   **指摘No.:** P-13
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 8 (Week 8) の実施日(Day 65)が、計画日(Day 56)から9日遅れている。プロトコル Section 3.1ではVisit 8は+/-3日の許容範囲と記載されており、逸脱している。主要評価時期のずれであり、評価の信頼性に影響する可能性。
        *   **プロトコル該当箇所:** Section 3.1, Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 主要な評価時期のVisit Window逸脱は、データの解釈に影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Name(SV.VISIT)] = 'WEEK 8'
            *   [Visit Number(SV.VISITNUM)] = 8
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-09-28' (Day 65)
            *   [Planned Study Day of Visit(TV.VISITDY)] = 56 (for VISITNUM=8)
    *   **指摘No.:** P-14
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 8.1 (Week 10 (T)) の実施日(Day 79)が、計画日(Day 70)から9日遅れている。プロトコルにVisit Windowの規定はないが、遅延している。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 評価スケジュールの遅延。
        *   **関連データ:**
            *   [Visit Name(SV.VISIT)] = 'WEEK 10 (T)'
            *   [Visit Number(SV.VISITNUM)] = 8.1
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-10-12' (Day 79)
            *   [Planned Study Day of Visit(TV.VISITDY)] = 70 (for VISITNUM=8.1)
    *   **指摘No.:** P-15
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 9 (Week 12) の実施日(Day 115)が、計画日(Day 84)から31日遅れている。プロトコル Section 3.1ではVisit 9は+/-4日の許容範囲と記載されており、大幅に逸脱している。主要評価時期のずれであり、評価の信頼性に影響する可能性。
        *   **プロトコル該当箇所:** Section 3.1, Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 主要な評価時期の大幅なVisit Window逸脱は、データの解釈に重大な影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Name(SV.VISIT)] = 'WEEK 12'
            *   [Visit Number(SV.VISITNUM)] = 9
            *   [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-11-17' (Day 115)
            *   [Planned Study Day of Visit(TV.VISITDY)] = 84 (for VISITNUM=9)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-2, P-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時(2013-07-03)およびWeek 6(2013-09-06)以降複数回にわたり、「Leukocytes」が基準値上限を超えていますが、臨床的な意義および評価についてコメントをお願いします。また、スクリーニング時のWBC高値にもかかわらず適格と判断された根拠をお知らせください。有害事象「WHITE BLOOD CELL COUNT INCREASED」の転帰が「RECOVERED/RESOLVED」と記録されていますが、その後のWBC高値との関連について評価をお願いします。
        *   **クエリ文面（英語）:** WBC count was above the upper limit of normal at Screening (2013-07-03) and on multiple occasions from Week 6 (2013-09-06) onwards. Please comment on the clinical significance and assessment. Also, please provide the rationale for eligibility despite high WBC at screening. The AE 'WHITE BLOOD CELL COUNT INCREASED' outcome was 'RECOVERED/RESOLVED', please assess its relation to subsequent high WBC counts.
        *   **判断理由:** 持続するWBC高値の原因評価、スクリーニング時の適格性判断の妥当性確認、AE転帰評価の整合性確認のため。参加者の安全性評価に重要。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='WBC', LB.LBDY, LB.LBSTRESN, LB.LBNRIND, AE.AETERM='WHITE BLOOD CELL COUNT INCREASED', AE.AEOUT, AE.AEENDY
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
            *   関連する医学的知見: 持続する白血球増多症の原因検索の必要性
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「RECTAL HAEMORRHAGE」について、治験薬との関連性が「NONE」と評価されていますが、評価根拠について詳細をお知らせください。
        *   **クエリ文面（英語）:** Regarding the AE 'RECTAL HAEMORRHAGE', the causality (AEREL) was assessed as 'NONE'. Please provide details on the rationale for this assessment.
        *   **判断理由:** コリン作動薬の潜在的な消化管への影響を考慮し、AEの関連性評価の妥当性を確認するため。安全性評価の質に関わる。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='RECTAL HAEMORRHAGE', AE.AEREL='NONE'
            *   関連する医学的知見: コリン作動薬の副作用プロファイル
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「APPLICATION SITE IRRITATION」および「SKIN IRRITATION」について、特に後者は重症度が「MODERATE」と記録されています。症状の詳細（範囲、持続期間など）、中止理由との関連、および併用薬「HYDROCORTISONE, TOPICAL」による処置の効果について詳細をお知らせください。
        *   **クエリ文面（英語）:** Regarding AEs 'APPLICATION SITE IRRITATION' and 'SKIN IRRITATION' (Severity='MODERATE'), please provide details on symptoms (e.g., extent, duration), relation to withdrawal reason ('ITCHY'), and the effectiveness of the concomitant medication 'HYDROCORTISONE, TOPICAL'.
        *   **判断理由:** 中止理由と関連する可能性のある中等度のAEについて、詳細な情報を収集し、安全性プロファイルを正確に把握するため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM, AE.AESEV, DS.DSTERM, CM.CMTRT
            *   関連するプロトコル箇所: Section 3.10.1 (Discontinuations)
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 「Alanine Aminotransferase」、「Aspartate Aminotransferase」、および「Creatine Kinase」が複数回基準値上限を超えていますが、これらの変動の臨床的意義と評価についてコメントをお願いします。特にDay 14のCreatine Kinase高値(320 U/L)について評価をお願いします。
        *   **クエリ文面（英語）:** ALT, AST, and CK levels exceeded the upper limit of normal on multiple occasions. Please comment on the clinical significance and assessment of these fluctuations, especially the high CK value (320 U/L) on Day 14.
        *   **判断理由:** 肝酵素およびCKの変動に対する臨床的評価を確認し、潜在的な臓器障害のリスクを評価するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALT', 'AST', 'CK', LB.LBDY, LB.LBSTRESN, LB.LBNRIND
            *   関連する医学的知見: 薬剤性肝障害、横紋筋融解症のモニタリング
    *   **クエリNo.:** Q-5 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 「Blood Urea Nitrogen」が複数回基準値上限を超えていますが、臨床的な意義について評価をお願いします。
        *   **クエリ文面（英語）:** Blood Urea Nitrogen (BUN) levels exceeded the upper limit of normal on multiple occasions. Please assess the clinical significance.
        *   **判断理由:** 断続的なBUN高値の臨床的評価を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='BUN', LB.LBDY, LB.LBSTRESN, LB.LBNRIND
    *   **クエリNo.:** Q-6 (関連指摘No.: M-6)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 115の検査で尿中の「Ketones」が「ABNORMAL」と記録されています。同時期に体重減少も認められていますが、この所見の臨床的意義と評価についてコメントをお願いします。
        *   **クエリ文面（英語）:** Urine 'Ketones' were recorded as 'ABNORMAL' on Day 115. Weight loss was also observed around this time. Please comment on the clinical significance and assessment of this finding.
        *   **判断理由:** ケトン尿の原因と臨床的意義を確認し、患者の代謝状態や栄養状態を評価するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='KETONES', LB.LBDY, LB.LBNRIND, VS.VSTESTCD='WEIGHT', VS.VSDY, VS.VSSTRESN
            *   関連する医学的知見: ケトン尿と体重減少の関連
    *   **クエリNo.:** Q-7 (関連指摘No.: M-7)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Day 41に臥位での「Pulse Rate」が50 bpm、立位3分後の「Systolic Blood Pressure」が86 mmHgと記録されています。徐脈および低血圧に関連する症状（めまい、ふらつき等）の有無と、これらの所見の臨床的意義について評価をお願いします。
        *   **クエリ文面（英語）:** On Day 41, supine 'Pulse Rate' was 50 bpm and standing 'Systolic Blood Pressure' (after 3 min) was 86 mmHg. Please assess for any related symptoms (e.g., dizziness, lightheadedness) and comment on the clinical significance of these findings.
        *   **判断理由:** 薬剤起因性の徐脈・低血圧の可能性を評価し、関連症状の有無を確認するため。安全性評価上重要。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='PULSE', 'SYSBP', VS.VSPOS, VS.VSTPT, VS.VSDY, VS.VSSTRESN
            *   関連する医学的知見: コリン作動薬の心血管系への影響
    *   **クエリNo.:** Q-8 (関連指摘No.: M-8)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Week 8(Day 65)からWeek 12(Day 115)にかけて、「Weight」が53.98kgから50.8kgへと約3.2kg減少しています。この体重減少の原因と臨床的意義について評価をお願いします。
        *   **クエリ文面（英語）:** 'Weight' decreased by approx. 3.2 kg (from 53.98kg to 50.8kg) between Week 8 (Day 65) and Week 12 (Day 115). Please assess the cause and clinical significance of this weight loss.
        *   **判断理由:** 短期間での有意な体重減少の原因を特定し、患者の健康状態への影響を評価するため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='WEIGHT', VS.VSDY, VS.VSSTRESN
            *   関連する医学的知見: 高齢者の意図しない体重減少の評価
    *   **クエリNo.:** Q-9 (関連指摘No.: M-9)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有効性評価指標（ADAS-Cog(11), CIBIC+, NPI-X, DAD）の結果に一貫性が見られません（例: ADAS-Cog(11)は改善傾向だがCIBIC+は変化なし、NPI-XやDADは悪化傾向）。これらの結果の乖離について、治験医師の見解をお知らせください。
        *   **クエリ文面（英語）:** Efficacy assessments (ADAS-Cog(11), CIBIC+, NPI-X, DAD) show inconsistent results (e.g., ADAS-Cog(11) improved, CIBIC+ no change, NPI-X/DAD worsened). Please provide the investigator's perspective on these discrepancies.
        *   **判断理由:** 有効性評価結果の解釈の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのADAS-Cog, CIBIC+, NPI-X, DAD関連データ
            *   関連するプロトコル箇所: Section 2 (Objectives), Section 4.3 (Efficacy Analyses)
    *   **クエリNo.:** Q-10 (関連指摘No.: D-3, P-12)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 2 (2013-07-24)において、立位1分後のバイタルサイン（拡張期血圧、収縮期血圧、脈拍）が未測定（NOT DONE）となっています。測定されなかった理由をお知らせください。また、Visit 6 (AMBUL ECG REMOVAL) の実施が計画日より11日遅延していますが、理由をお知らせください。
        *   **クエリ文面（英語）:** On Visit 2 (2013-07-24), vital signs (DIABP, SYSBP, PULSE) after standing for 1 minute were 'NOT DONE'. Please provide the reason. Also, Visit 6 (AMBUL ECG REMOVAL) was delayed by 11 days from the planned date. Please provide the reason for the delay.
        *   **判断理由:** データ欠損およびスケジュール遅延の理由を確認し、記録の完全性とプロトコル遵守状況を明確にするため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSSTAT, VS.VISITNUM=2, VS.VSTPT='AFTER STANDING FOR 1 MINUTE', SV.VISITNUM=6, SV.SVSTDTC, TV.VISITDY (for VISITNUM=6)
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 (Schedule of Events)
    *   **クエリNo.:** Q-11 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「NEUTROPHIL COUNT INCREASED」が報告されていますが、対応する好中球数の検査データが提供されていません。データが存在する場合はご提供ください。存在しない場合はその旨をお知らせください。
        *   **クエリ文面（英語）:** AE 'NEUTROPHIL COUNT INCREASED' was reported, but corresponding neutrophil count lab data is missing. Please provide the data if available, or confirm if it was not collected.
        *   **判断理由:** AE評価に必要な検査データの有無を確認するため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='NEUTROPHIL COUNT INCREASED', LBドメイン
    *   **クエリNo.:** Q-12 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 既往歴として報告されている「Reported Term for the Medical History」が「PREMENSTRUAL PAIN」および「VERBATIM_1100」(Dictionary-Derived Term: AORTIC STENOSIS)について、「Start Date/Time of Medical History Event」が記録されていません。可能な範囲で開始日をお知らせください。
        *   **クエリ文面（英語）:** For MH terms 'PREMENSTRUAL PAIN' and 'VERBATIM_1100' (MHDECOD: AORTIC STENOSIS), the 'Start Date/Time of Medical History Event' (MHSTDTC) is missing. Please provide the start date if available.
        *   **判断理由:** データの完全性を向上させるため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM, MH.MHDECOD, MH.MHSTDTC
    *   **クエリNo.:** Q-13 (関連指摘No.: D-7, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 「Date/Time of Informed Consent」が記録されていません。同意取得日をお知らせください。
        *   **クエリ文面（英語）:** The 'Date/Time of Informed Consent' (RFICDTC) is missing. Please provide the date of informed consent.
        *   **判断理由:** GCP遵守およびプロトコル遵守（Inclusion Criteria [6]）の確認に必須の情報であるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC
            *   関連するプロトコル箇所: Section 3.4.2.1 [6], Section 5.1
    *   **クエリNo.:** Q-14 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル選択基準[5]で要求されている「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」の実施有無と結果について確認させてください。
        *   **クエリ文面（英語）:** Please confirm if 'CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year' was performed and reviewed, as required by protocol inclusion criterion [5].
        *   **判断理由:** 選択基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (情報の欠損)
            *   関連するプロトコル箇所: Section 3.4.2.1 [5]
    *   **クエリNo.:** Q-15 (関連指摘No.: P-3, P-10)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor / CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[16b]で評価が必要なスクリーニング時のECG所見、およびプロトコルで規定されているVisit 2での24時間Ambulatory ECG、ならびに試験期間中の定期的なECG検査の実施有無と結果について確認させてください。
        *   **クエリ文面（英語）:** Please confirm the performance and results of the screening ECG (Exclusion Criterion [16b]), the 24-hour Ambulatory ECG at Visit 2, and periodic ECGs during the study, as required by the protocol (Sections 3.9.3.4.2, 3.9.4).
        *   **判断理由:** 除外基準の遵守、および重要な安全性モニタリング計画の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (情報の欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 [16b], Section 3.9.3.4.2, Section 3.9.4
    *   **クエリNo.:** Q-16 (関連指摘No.: P-5)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[28b]で評価が必要なFolate検査の実施有無と結果について確認させてください。
        *   **クエリ文面（英語）:** Please confirm if the Folate test was performed and provide the result, as required for assessing protocol exclusion criterion [28b].
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (情報の欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 [28b]
    *   **クエリNo.:** Q-17 (関連指摘No.: P-6)
        *   **重要度:** Major
        *   **発行担当者:** CRA / Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時の「Vitamin B12」が946 pg/mLと基準値上限を超えています。プロトコル除外基準[28b]ではサプリメント服用中の場合は許容されるとありますが、併用薬等に記録がありません。サプリメント服用の有無と、組み入れ適格と判断された根拠についてお知らせください。
        *   **クエリ文面（英語）:** Screening 'Vitamin B12' level was 946 pg/mL (above ULN). Protocol exclusion criterion [28b] allows this if the patient is taking supplements, but no record was found. Please confirm supplement use and the rationale for eligibility.
        *   **判断理由:** 除外基準抵触の可能性があり、組み入れ判断の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='VITB12', LB.LBDY=-23, LB.LBORRES='946', LB.LBNRIND='HIGH', CMドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 [28b]
    *   **クエリNo.:** Q-18 (関連指摘No.: P-7)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[28b]で評価が必要な甲状腺機能検査について、TSH以外の項目（例: Free T4, T3 Uptake）の実施有無と結果について確認させてください。
        *   **クエリ文面（英語）:** Regarding thyroid function tests required for assessing protocol exclusion criterion [28b], please confirm if tests other than TSH (e.g., Free T4, T3 Uptake) were performed and provide the results.
        *   **判断理由:** 除外基準の遵守を完全に確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン
            *   関連するプロトコル箇所: Section 3.4.2.2 [28b]
    *   **クエリNo.:** Q-19 (関連指摘No.: P-8)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル除外基準[29b]で要求されている梅毒スクリーニングの実施有無と結果について確認させてください。
        *   **クエリ文面（英語）:** Please confirm if syphilis screening was performed and provide the result, as required for assessing protocol exclusion criterion [29b].
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (情報の欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 [29b]
    *   **クエリNo.:** Q-20 (関連指摘No.: P-9)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 治験薬の投与がDay 80 (2013-10-13) で終了していますが、試験中止日(Day 115)よりも前です。投与が早期に終了した理由をお知らせください。
        *   **クエリ文面（英語）:** Study drug exposure ended on Day 80 (2013-10-13), which is before the study discontinuation date (Day 115). Please provide the reason for early termination of exposure.
        *   **判断理由:** プロトコルからの逸脱の可能性があり、薬剤曝露期間に影響するため理由の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: EX.EXENDY=80, DS.DSSTDY=115
            *   関連するプロトコル箇所: Section 3.1, Figure LZZT.1
    *   **クエリNo.:** Q-21 (関連指摘No.: P-11, P-13, P-15)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 1 (計画日Day -7に対し実施日Day -23)、Visit 8 (計画日Day 56に対し実施日Day 65、許容範囲逸脱)、Visit 9 (計画日Day 84に対し実施日Day 115、許容範囲逸脱)の実施日が計画から大幅にずれています。遅延理由についてそれぞれお知らせください。
        *   **クエリ文面（英語）:** Visit 1 (Day -23 vs planned Day -7), Visit 8 (Day 65 vs planned Day 56, outside window), and Visit 9 (Day 115 vs planned Day 84, outside window) occurred significantly off schedule. Please provide reasons for these delays.
        *   **判断理由:** 複数のVisitで計画からの大幅なずれがあり、プロトコル遵守およびデータ品質の観点から理由の確認が必要。特に主要評価時期のずれは重要。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM, SV.SVSTDTC, TV.VISITDY, DM.RFSTDTC
            *   関連するプロトコル箇所: Section 3.1, Protocol Attachment LZZT.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: なし)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor / CRA
        *   **疑義事項/確認内容:** 併用薬としてHydrocortisone topicalが使用されている。プロトコル3.8項で明示的に許可されている薬剤ではないが、禁止リスト(3.4.2.2 [31b])にも含まれておらず、皮膚刺激に対する一般的な治療薬であるため、使用は許容されると判断。記録として残す。
        *   **判断理由:** プロトコル上の扱いが明確でないが、臨床的に妥当な使用であり、安全性や有効性評価への影響は小さいと判断されるため、内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='HYDROCORTISONE, TOPICAL'
            *   関連するプロトコル箇所: Section 3.8, Section 3.4.2.2 [31b]
    *   **確認事項No.:** I-2 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「APPLICATION SITE IRRITATION」の終了日(Day 61)とCM「HYDROCORTISONE, TOPICAL」の開始日(Day 61)が同日である点について、記録上のずれの可能性はあるが、臨床的な流れ（AE発現→処置開始）としては矛盾しないと判断。AE「SKIN IRRITATION」(Day 79-98)の期間中に同CMが使用されている点も臨床的に妥当。
        *   **判断理由:** データ間のわずかな日付のずれであり、臨床的な解釈に大きな影響を与えないと判断されるため、内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM, AE.AESTDY, AE.AEENDY, CM.CMTRT, CM.CMSTDY, CM.CMENDY
    *   **確認事項No.:** I-3 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QSドメインのNPI-Xデータにおいて、症状がない場合の記録方法（Scoreのみ記録 vs Presentフラグで記録）に一貫性がない可能性がある点について、データマネジメントプロセス内で確認し、必要であれば標準化ルールを再確認する。
        *   **判断理由:** データの一貫性に関する問題であり、解析への影響は限定的と考えられるため、内部での確認・対応とする。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (NPI-X関連)

---

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
64歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2008年発症）、肺気腫（MILD）、冠動脈疾患（MILD）、関節炎（MILD）、肺膿瘍ドレナージ（1997年実施）、腸ポリープ切除（2009年実施）が報告されている。教育レベルは12年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65 (SCREENING 1)|ALT (135 U/L) および AST (145 U/L) が基準値上限 (それぞれ43 U/L, 36 U/L) を超えて高値 (LBNRIND=HIGH)。|
|2013年02月21日|Day -9 (UNSCHEDULED 1.1)|ALT (19 U/L) および AST (29 U/L) が正常範囲内に回復。Sodiumが基準値下限 (135 mmol/L) を下回る低値 (133 mmol/L, LBNRIND=LOW)。|
|2013年02月23日|Day -7 (SCREENING 1)|MMSEスコア 23点。Hachinski Ischemic Score 1点。|
|2013年03月02日|Day 1 (BASELINE)|治験薬 (Placebo) 投与開始。ベースラインADAS-Cog(11)スコア 14点。ベースラインNPI-X Total Score 3点。ベースラインDADスコア 29/33点 (NA除く)。|
|2013年03月04日|Day 3 (N/A)|有害事象「DIARRHOEA」(MILD) 発現。|
|2013年03月05日|Day 4 (N/A)|有害事象「DIARRHOEA」回復。有害事象「INSOMNIA」(MILD) 発現。併用薬「KAOPECTATE」投与開始 (1 Tbsp, ONCE)。|
|2013年03月05日|Day 4 (N/A)|併用薬「KAOPECTATE」投与終了。|
|2013年03月06日|Day 5 (N/A)|有害事象「INSOMNIA」回復。|
|2013年03月14日|Day 13 (WEEK 2)|NPI-X Total Score 6点。|
|2013年03月28日|Day 27 (WEEK 4)|MCVが基準値上限 (100 fL) を超えて高値 (101 fL, LBNRIND=HIGH)。Sodiumが基準値上限 (145 mmol/L) を超えて高値 (146 mmol/L, LBNRIND=HIGH)。NPI-X Total Score 4点。|
|2013年04月13日|Day 43 (WEEK 6)|NPI-X Total Score 3点。|
|2013年04月27日|Day 57 (WEEK 8)|ADAS-Cog(11)スコア 9点。CIBIC+評価なし。DAD評価なし。|
|2013年05月11日|Day 71 (WEEK 10 (T))|NPI-X Total Score 4点。|
|2013年05月25日|Day 85 (WEEK 12)|NPI-X Total Score 6点。|
|2013年06月08日|Day 99 (WEEK 14 (T))|NPI-X Total Score 6点。|
|2013年06月22日|Day 113 (WEEK 16)|ADAS-Cog(11)スコア 7点。CIBIC+評価「NO CHANGE」(4)。DADスコア 30/33点 (NA除く)。NPI-X Total Score 4点。|
|2013年07月06日|Day 127 (WEEK 18 (T))|NPI-X Total Score 4点。|
|2013年07月20日|Day 141 (WEEK 20)|NPI-X Total Score 4点。|
|2013年08月03日|Day 155 (WEEK 22 (T))|NPI-X Total Score 3点。|
|2013年08月09日|Day 161 (WEEK 24)|ADAS-Cog(11)スコア 9点。CIBIC+評価「NO CHANGE」(4)。DADスコア 31/33点 (NA除く)。NPI-X Total Score 2点。|
|2013年08月31日|Day 183 (WEEK 26)|治験薬 (Placebo) 投与終了。試験完了。ASTが基準値上限 (36 U/L) をわずかに超えて高値 (38 U/L, LBNRIND=HIGH)。NPI-X Total Score 2点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Screening時 (Day -65) にALT (135 U/L) および AST (145 U/L) の顕著な上昇が認められた。Unscheduled Visit (Day -9) で正常化しているが、原因は不明。最終Visit (Day 183) でもASTの軽度上昇 (38 U/L) が認められている。肝機能障害のリスクや、背景にある未診断の肝疾患の可能性について評価が必要。
        *   **根拠:** ALT/ASTは肝細胞障害の指標であり、基準値の3倍を超える上昇は臨床的に重要。特に薬剤性肝障害やウイルス性肝炎、アルコール性肝障害などを鑑別する必要がある。最終Visitでの軽度上昇も、潜在的な問題を否定できない。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 43
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 19
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 29
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = 183, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 38, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36
            *   [Medical History Domain(MH.*)] (関連する肝疾患の記載なし)
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 27) にMCVの一過性高値 (101 fL, 基準値上限100 fL) が認められた。大球性貧血の可能性を示唆するが、他のVisitでは正常範囲内であり、HGB/HCTも正常範囲内。ビタミンB12は正常だが葉酸は未測定。臨床的な意義は低い可能性が高いが、念のため記録する。
        *   **根拠:** MCV高値は大球性貧血（ビタミンB12欠乏、葉酸欠乏など）を示唆する。一過性であり他の血算項目に異常がないため臨床的意義は低いと考えられるが、アルツハイマー病患者では栄養状態の変化も考慮すべき点である。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 100
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 9.12282
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HCT', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.46
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 153.4624
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Unscheduled Visit (Day -9) で軽度の低ナトリウム血症 (133 mmol/L, 基準値下限135)、Week 4 (Day 27) で軽度の高ナトリウム血症 (146 mmol/L, 基準値上限145) が認められた。変動の原因は不明だが、変動幅は小さく、他のVisitでは正常範囲内であるため、臨床的な意義は低い可能性が高い。
        *   **根拠:** ナトリウム値の異常は脱水、心不全、腎機能障害、薬剤性など様々な原因で起こりうる。変動が一過性であり軽度であることから、臨床的意義は低いと考えられる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 133, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 135
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 146, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 145

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。治験開始前に同意が取得されているか確認できない。ただし、他のデータ（Screening Visit日など）から、治験手順開始前に同意取得が行われた可能性は高い。
        *   **根拠:** GCP上、治験関連手順開始前の同意取得は必須である。日付の欠損は記録の不備を示す。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   [Start Date/Time of Visit(SV.SVSTDTC)] (Visit 1: 2013-02-23)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** Medical History (MH) ドメインにおいて、一部の既往歴（肺気腫、冠動脈疾患、関節炎）の開始日 (MHSTDTC) が欠損している。既往歴の評価に影響する可能性があるが、本試験の評価項目への直接的な影響は限定的と考えられる。
        *   **根拠:** データ完全性の観点からの指摘。開始日の欠損は、イベントの持続期間や発症時期の評価を困難にする。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0087' (EMPHYSEMA), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0409' (CORONARY ARTERY DISEASE), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_1309' (ARTHRITIS), [Start Date/Time of Medical History Event(MH.MHSTDTC)] = ''
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、MedDRAコーディングに関連する変数（AELLT, AELLTCD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCD）が欠損している。有害事象の標準化された分類・集計に影響する。
        *   **根拠:** データ標準化と集計・解析の観点からの指摘。コーディング情報の欠損は、安全性データの標準的な評価を妨げる。
        *   **関連データ:**
            *   [AE Domain(AE.*)] (関連するコーディング変数が欠損)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、一部の薬剤（KAOPECTATE, VITAMIN C, VITAMIN E）の標準薬剤名 (CMDECOD) および薬剤分類 (CMCLAS) が "UNCODED" となっている。併用薬の標準化された分類・集計に影響する。
        *   **根拠:** データ標準化と集計・解析の観点からの指摘。コーディング情報の欠損は、併用薬データの標準的な評価を妨げる。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'KAOPECTATE', [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED', [Medication Class(CM.CMCLAS)] = 'UNCODED'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'VITAMIN C', [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED', [Medication Class(CM.CMCLAS)] = 'UNCODED'
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'VITAMIN E', [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED', [Medication Class(CM.CMCLAS)] = 'UNCODED'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** Screening時 (Day -65) のALTおよびASTが基準値を大幅に超過していた（Exclusion Criteria [27b]）。プロトコルでは、臨床的に意義がないと判断された場合は組み入れ可能とされているが、その判断記録がデータからは確認できない。Unscheduled Visit (Day -9) で正常化しているため組み入れは行われたと考えられるが、基準値逸脱の評価と記録に関するプロトコル遵守状況の確認が必要。参加者の安全性に関わる基準であり、評価の信頼性にも影響しうる。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準に該当する可能性のある検査値異常が認められたにも関わらず、組み入れられている。プロトコルで規定された臨床的意義の評価と記録が行われたか不明。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 43
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 36
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 主要評価項目であるCIBIC+および副次評価項目であるDADが、プロトコルで規定されたVisit 8 (Week 8) で実施されていない。評価項目の欠測は試験の有効性評価の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** プロトコルで規定された評価スケジュールからの逸脱。主要/副次評価項目のデータ欠損は、有効性評価の感度や信頼性を低下させる可能性がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] (Visit 8のレコードなし)
            *   [Question Short Name(QS.QSTESTCD)] like 'DAITM%', [Visit Number(QS.VISITNUM)] (Visit 8のレコードなし)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** Visit 12 (Week 24) の実施日 (Day 161) が、計画日 (Day 168) より7日早く、プロトコルで規定された許容範囲 (+/- 4日) から逸脱している。主要評価項目の測定タイミングの逸脱であり、有効性評価の信頼性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit Windowに関する記載)
        *   **根拠:** プロトコルで規定されたVisit Windowからの逸脱。評価タイミングのずれは、特に変化率などを評価する場合に結果に影響を与える可能性がある。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 12, [Planned Study Day of Visit(SV.VISITDY)] = 168, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-08-09'
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2013-03-02' (Day 1)
            *   (Day 161 = 2013-08-09 - 2013-03-02 + 1)
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [28b] に関連する葉酸 (Folate) の検査が実施されていない。プロトコル上、基準値以下の場合は除外とされているため、適格性確認のための検査が未実施である。ただし、他のデータから除外基準違反を示唆する所見はなく、Placebo群であるため、試験結果への影響は限定的と考えられる。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** プロトコルで規定された除外基準判定に必要な検査の未実施。
        *   **関連データ:**
            *   [Laboratory Tests Results Domain(LB.*)] (Folateのレコードなし)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Screening時 (Study Day -65) のアラニンアミノトランスフェラーゼが「135 U/L」、アスパラギン酸アミノトランスフェラーゼが「145 U/L」と基準値を大幅に超えていましたが、除外基準[27b]に該当しないと判断された根拠（臨床的に意義がないと判断された理由）について、記録に基づきご教示ください。また、最終Visit (Study Day 183) でアスパラギン酸アミノトランスフェラーゼが「38 U/L」と再度軽度上昇していますが、こちらの臨床的意義についても評価をお願いします。
        *   **クエリ文面（英語）:** At Screening (Study Day -65), ALT was '135 U/L' and AST was '145 U/L', significantly exceeding the upper limits. Please provide the documented rationale for determining these findings were not clinically significant per exclusion criterion [27b]. Also, AST was mildly elevated again at the final visit (Study Day 183) to '38 U/L'. Please assess the clinical significance of this finding.
        *   **判断理由:** Screening時の肝酵素著明上昇にも関わらず被験者が組み入れられており、除外基準違反の可能性があるため。プロトコル遵守と参加者の安全性確保の観点から、当時の臨床判断の根拠を確認する必要がある。最終Visitでの再上昇についても、遅発性の影響や基礎疾患の可能性を評価するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALT'/LBSTRESN=135/LBDY=-65, LB.LBTESTCD='AST'/LBSTRESN=145/LBDY=-65, LB.LBTESTCD='AST'/LBSTRESN=38/LBDY=183
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
            *   関連する医学的知見: 肝機能検査異常の臨床的意義、除外基準の重要性。
    *   **クエリNo.:** Q-2 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルではVisit 8 (Week 8) でCIBIC+およびDADの評価が規定されていますが、本症例では実施記録がありません。未実施理由をご教示ください。
        *   **クエリ文面（英語）:** The protocol specifies CIBIC+ and DAD assessments at Visit 8 (Week 8). However, data for these assessments are missing for this subject at Visit 8. Please provide the reason for the assessments not being performed.
        *   **判断理由:** 主要評価項目および副次評価項目の欠測理由を確認し、プロトコル逸脱の有無と評価の信頼性への影響を判断するため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (Visit 8のCIBIC, DAITM* レコード欠損)
            *   関連するプロトコル箇所: Section 3.9.1.1, Protocol Attachment LZZT.1
    *   **クエリNo.:** Q-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Visit 12 (Week 24) の実施日 (2013-08-09, Study Day 161) が、計画日 (Study Day 168) より7日早く、プロトコル規定の許容範囲 (±4日) から逸脱しています。逸脱理由をご教示ください。
        *   **クエリ文面（英語）:** Visit 12 (Week 24) was conducted on 2013-08-09 (Study Day 161), which is 7 days earlier than the planned Study Day 168 and outside the protocol-specified window (±4 days). Please provide the reason for this deviation.
        *   **判断理由:** 主要評価項目の測定タイミングに関するプロトコル逸脱の理由を確認し、評価の信頼性への影響を判断するため。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=12, SV.VISITDY=168, SV.SVSTDTC='2013-08-09', DM.RFSTDTC='2013-03-02'
            *   関連するプロトコル箇所: Section 3.1

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 4 (Day 27) にMCVの一過性高値 (101 fL) が認められた。他の血算項目やVisitでの値は正常範囲内であり、ビタミンB12も正常。葉酸は未測定だが、臨床的意義は低いと判断。内部記録として残す。
        *   **判断理由:** 変動が一過性かつ軽微であり、他の関連データからも問題が示唆されないため、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='MCV'/LBSTRESN=101/LBDY=27, LB.LBTESTCD='HGB'/LBSTRESN=9.12282/LBDY=27, LB.LBTESTCD='HCT'/LBSTRESN=0.46/LBDY=27, LB.LBTESTCD='VITB12'/LBSTRESN=153.4624/LBDY=-9
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Unscheduled Visit (Day -9) での軽度低Na血症 (133 mmol/L)、Week 4 (Day 27) での軽度高Na血症 (146 mmol/L) が認められた。変動は軽微で一過性であり、臨床的意義は低いと判断。内部記録として残す。
        *   **判断理由:** 変動が軽微かつ一過性であり、他の関連データからも問題が示唆されないため、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='SODIUM'/LBSTRESN=133/LBDY=-9, LB.LBTESTCD='SODIUM'/LBSTRESN=146/LBDY=27
    *   **確認事項No.:** I-3 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 同意取得日 (DM.RFICDTC) が欠損している。他の日付情報（Screening Visit日など）から同意取得自体は行われている可能性が高い。データ入力・転記ミスの可能性。修正を試みるが、影響は軽微と判断。
        *   **判断理由:** GCP遵守の観点からは記録が必要だが、他の情報から同意取得の事実は推測でき、安全性や評価への直接的な影響は小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC=''
    *   **確認事項No.:** I-4 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインの一部既往歴で開始日 (MHSTDTC) が欠損。データ完全性の問題だが、評価への影響は限定的。
        *   **判断理由:** 既往歴の存在自体は記録されており、評価への影響が小さいため問い合わせ不要と判断。
        *   **判断根拠:**
            *   関連するデータ: MH.MHSTDTC='' (for EMPHYSEMA, CORONARY ARTERY DISEASE, ARTHRITIS)
    *   **確認事項No.:** I-5 (関連指摘No.: D-3, D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEおよびCMドメインでコーディング情報（MedDRA, WHODrug）が一部欠損している。データ標準化と集計に影響するが、個々の症例評価への影響は限定的。後続のデータクリーニングプロセスで対応。
        *   **判断理由:** データ品質の問題であり、集計・解析段階で問題となる可能性があるが、個別の症例レビューにおける緊急性は低いと判断。
        *   **判断根拠:**
            *   関連するデータ: AE.* (コーディング変数欠損), CM.CMDECOD='UNCODED', CM.CMCLAS='UNCODED'
    *   **確認事項No.:** I-6 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/Medical Monitor
        *   **疑義事項/確認内容:** 除外基準確認に必要な葉酸 (Folate) 検査が未実施。プロトコルからの逸脱だが、他のデータから適格性に問題がある可能性は低く、Placebo群であるため影響は小さいと判断。内部記録として残す。
        *   **判断理由:** 適格性確認手順の不備だが、他のデータから問題は示唆されず、安全性・有効性評価への直接的な影響は小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (Folateレコードなし)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]

---

# [01-703-1076]のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
69歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2012年8月27日発症、PRIMARY DIAGNOSIS）、心房細動ブロック（SIGNIFICANT PRE-EXISTING CONDITION, MILD）、緑内障（SIGNIFICANT PRE-EXISTING CONDITION, MILD）、高血圧（SIGNIFICANT PRE-EXISTING CONDITION, MILD）、痛風（SIGNIFICANT PRE-EXISTING CONDITION, MILD）が報告されている。教育レベルは10年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年10月16日|Day -9 (SCREENING 1)|臨床検査実施。アルブミン 49 g/L (基準値上限46, HIGH)、コレステロール 7.94 mmol/L (基準値上限7.4, HIGH)、蛋白 81 g/L (基準値上限80, HIGH)、尿酸 464 umol/L (基準値上限446, HIGH)。|
|2013年10月17日|Day -8 (SCREENING 1)|人口統計学的情報収集、バイタルサイン測定、病歴聴取、被験者特性収集、質問票調査（MMSE, MHIS）実施。MMSEスコア 23点、MHISスコア 1点。臥位血圧 152/92 mmHg。|
|2013年10月23日|Day -2 (SCREENING 2)|バイタルサイン測定。臥位血圧 150/92 mmHg。|
|2013年10月25日|Day 1 (BASELINE)|治験薬投与開始（Xanomeline 54mg QD）。バイタルサイン測定、質問票調査（ADAS-Cog, NPI-X, DAD）実施。ADAS-Cog(11) Totalスコア 6点、NPI-X Totalスコア 4点。|
|2013年11月06日|Day 13 (WEEK 2)|治験薬投与終了（Xanomeline 54mg QD）。臨床検査実施（尿酸 458 umol/L, HIGH）、バイタルサイン測定、質問票調査（NPI-X）実施。NPI-X Totalスコア 1点。|
|2013年11月07日|Day 14 (N/A)|治験薬投与開始（Xanomeline 81mg QD）。|
|2013年11月16日|Day 23 (N/A)|有害事象「BIOPSY PROSTATE」(MODERATE) 発現、同日回復。治験薬との関連なし。|
|2013年11月20日|Day 27 (WEEK 4)|有害事象「BENIGN PROSTATIC HYPERPLASIA」(MODERATE) 発現、未回復。治験薬との関連なし。臨床検査実施（カルシウム 2.62 mmol/L, HIGH; コレステロール 8.25 mmol/L, HIGH; 尿酸 458 umol/L, HIGH）、バイタルサイン測定、質問票調査（NPI-X, DAD）実施。NPI-X Totalスコア 3点。|
|2013年11月23日|Day 30 (N/A)|有害事象「APPLICATION SITE PRURITUS」(MILD) 発現、未回復。治験薬との関連性の評価はPROBABLE。有害事象「APPLICATION SITE DERMATITIS」(MILD) 発現、未回復。治験薬との関連性の評価はPROBABLE。|
|2013年11月25日|Day 32 (N/A)|有害事象「HYPERHIDROSIS」(MILD) 発現、未回復。治験薬との関連性の評価はPOSSIBLE。|
|2013年11月27日|Day 34 (N/A)|併用薬「LOPID」投与終了。|
|2013年11月28日|Day 35 (N/A)|併用薬「MEVACOR」投与開始。|
|2013年12月04日|Day 41 (WEEK 6)|有害事象「HYPERCHOLESTEROLAEMIA」(MODERATE) 記録（発現日2007年）、未回復。治験薬との関連なし。臨床検査実施（尿酸 500 umol/L, HIGH）、バイタルサイン測定、質問票調査（NPI-X）実施。NPI-X Totalスコア 5点。|
|2013年12月05日|Day 42 (N/A)|併用薬「CORTISONE」(Topical, PRN) 投与開始。|
|2013年12月12日|Day 49 (N/A)|併用薬「MEVACOR」投与終了。併用薬「LIPITOR」投与開始。|
|2013年12月17日|Day 54 (WEEK 8)|有害事象「APPLICATION SITE PRURITUS」の重症度がMILDからMODERATEに悪化。臨床検査実施（尿酸 470 umol/L, HIGH）、バイタルサイン測定、質問票調査（ADAS-Cog, CIBIC+, NPI-X, DAD）実施。ADAS-Cog(11) Totalスコア 10点、CIBIC+スコア 3 (Minimal improvement)、NPI-X Totalスコア 2点。|
|2013年12月18日|Day 55 (N/A)|併用薬「LAC-HYDRIN」(Topical, BID) 投与開始。|
|2013年12月24日|Day 61 (WEEK 12)|治験薬投与終了（Xanomeline 81mg QD）。有害事象により治験中止。最終臨床検査実施（尿酸 464 umol/L, HIGH）、最終バイタルサイン測定、最終質問票調査（ADAS-Cog, CIBIC+, NPI-X, DAD）実施。ADAS-Cog(11) Totalスコア 11点、CIBIC+スコア 3 (Minimal improvement)、NPI-X Totalスコア 2点。|
|2014年01月21日|Day 88 (AE FOLLOW-UP)|有害事象フォローアップのための来院。併用薬情報収集。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 30に発現した皮膚関連の有害事象（適用部位そう痒感、適用部位皮膚炎）が未回復のまま、Day 61に「有害事象」を理由に治験が中止されている。中止理由となった有害事象の詳細と、中止判断の妥当性について確認が必要。特に、そう痒感はDay 54にMILDからMODERATEへ悪化しており、参加者のQOLへの影響も考慮される。
        *   **根拠:** 有害事象の遷延と悪化、およびそれが治験中止理由となっていることから、参加者の安全性と試験継続への影響が大きい。プロトコル3.9.3.4では皮膚症状への言及があり、適切な管理と評価が行われていたか確認が必要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-23', [Severity/Intensity(AE.AESEV)] = 'MILD' -> 'MODERATE', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [Causality(AE.AEREL)] = 'PROBABLE'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE DERMATITIS', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-23', [Severity/Intensity(AE.AESEV)] = 'MILD', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [Causality(AE.AEREL)] = 'PROBABLE'
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT', [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-12-24'
            *   [Relationship Identifier(RELREC.RELID)] = '01-703-1076-E08' (AEとDSを関連付け)
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Day 32に有害事象「HYPERHIDROSIS」(多汗症、MILD) が発現し、未回復。治験薬Xanomelineはコリン作動薬であり、発汗亢進は薬理作用に基づく既知の副作用の可能性がある。治験薬との関連性はPOSSIBLEと評価されている。
        *   **根拠:** 一般的な医学知識として、コリン作動薬は発汗を促進する可能性がある。重症度はMILDであり、直接的な安全性リスクは低いと考えられるが、治験薬との関連が示唆されるため記録・確認が必要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'HYPERHIDROSIS', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-25', [Severity/Intensity(AE.AESEV)] = 'MILD', [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [Causality(AE.AEREL)] = 'POSSIBLE'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** Day 27に有害事象「BENIGN PROSTATIC HYPERPLASIA」(前立腺肥大症、MODERATE) が発現。Day 23には「BIOPSY PROSTATE」(前立腺生検) が実施され同日回復している。これらは関連するイベントと考えられるが、AEとしての記録は妥当か。両イベントとも治験薬との関連はなしと評価されている。
        *   **根拠:** イベント間の時間的近接性から関連が疑われる。AEとしての記録の適切性について確認が必要だが、治験薬との関連はなく、安全性への直接的な影響は小さいと考えられる。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BENIGN PROSTATIC HYPERPLASIA', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-20', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Causality(AE.AEREL)] = 'NONE'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BIOPSY PROSTATE', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2013-11-16', [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-11-16', [Severity/Intensity(AE.AESEV)] = 'MODERATE', [Causality(AE.AEREL)] = 'NONE'
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** 有害事象「HYPERCHOLESTEROLAEMIA」(高コレステロール血症) がDay 41に記録されているが、開始日は2007年となっている。既往歴(MH)には高コレステロール血症の記載がない。併用薬として脂質異常症治療薬 (LOPID, MEVACOR, LIPITOR) が使用・変更されており、高コレステロール血症の存在は示唆されるが、AEとしての記録時期と開始日の乖離、MHへの未記載はデータの信頼性に影響する可能性がある。治療薬変更の医学的妥当性も確認が必要。
        *   **根拠:** AEの開始日と記録日の大幅な乖離、MHとの不整合はデータ品質の問題を示唆する。また、併用薬の変更と合わせて、脂質管理の状況と治験への影響を評価する必要がある。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'HYPERCHOLESTEROLAEMIA', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2007', [Date/Time of Collection(AE.AEDTC)] = '2013-12-04', [Causality(AE.AEREL)] = 'NONE'
            *   MHドメインに高コレステロール血症の記録なし
            *   CMドメイン: LOPID (終了日 2013-11-27), MEVACOR (開始日 2013-11-28, 終了日 2013-12-12), LIPITOR (開始日 2013-12-12)
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** 臨床検査において、尿酸値(Urate)がスクリーニング時から一貫して基準値上限を超えて高い値を示している。既往歴(MH)には痛風(Gout)が記録されているが、併用薬(CM)に痛風治療薬の使用記録がない。痛風発作のリスク管理は適切に行われているか。
        *   **根拠:** 既往歴と検査値異常が一致しているが、治療薬の使用記録がない。潜在的な痛風発作のリスクと、それに対する管理状況を確認する必要がある。ただし、治験期間中に痛風発作のAEは報告されていない。
        *   **関連データ:**
            *   LBドメイン: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'URATE', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (複数回)
            *   MHドメイン: [Reported Term for the Medical History(MH.MHTERM)] = 'GOUT'
            *   CMドメイン: 痛風治療薬の記録なし
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 27) の臨床検査でカルシウム(CA)値が基準値上限をわずかに超えて高値を示した (2.62 mmol/L vs ULN 2.57)。他の時点では基準値内であり、一過性の変動の可能性がある。
        *   **根拠:** 一過性の軽度な基準値逸脱であり、他のデータとの関連も不明瞭なため、現時点での臨床的意義は低いと考えられるが、念のため記録する。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CA', [Visit Number(LB.VISITNUM)] = 5, [Character Result/Finding in Std Format(LB.LBSTRESC)] = '2.61975', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** スクリーニング時 (Day -9) の臨床検査でアルブミン(ALB)と総蛋白(PROT)が基準値上限をわずかに超えて高値を示した。その後の測定では基準値内となっている。
        *   **根拠:** 一過性の軽度な基準値逸脱であり、臨床的意義は低いと考えられる。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALB', [Visit Number(LB.VISITNUM)] = 1, [Character Result/Finding in Std Format(LB.LBSTRESC)] = '49', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'PROT', [Visit Number(LB.VISITNUM)] = 1, [Character Result/Finding in Std Format(LB.LBSTRESC)] = '81', [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** スクリーニング時の臥位収縮期血圧が150mmHgを超えており、やや高値。既往歴(MH)に高血圧が記録されているが、併用薬(CM)に降圧薬の使用記録がない。治験期間中の血圧は概ね安定しているように見えるが、最終測定時(Day 61)はやや低め(122/82 mmHg)。高血圧の管理状況について確認が必要。
        *   **根拠:** 既往歴とバイタルサイン所見が一致しているが、治療薬の使用記録がない。血圧管理の状況を確認する必要がある。
        *   **関連データ:**
            *   VSドメイン: [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Vital Signs Position of Subject(VS.VSPOS)] = 'SUPINE', Visit 1: 152 mmHg, Visit 2: 150 mmHg, Visit 9: 122 mmHg
            *   MHドメイン: [Reported Term for the Medical History(MH.MHTERM)] = 'HYPERTENSION'
            *   CMドメイン: 降圧薬の記録なし
    *   **指摘No.:** M-9
        *   **重要度:** Major
        *   **内容:** 有効性評価において、主要評価項目であるADAS-Cog(11) Totalスコアはベースラインの6点からWeek 12には11点へと悪化傾向を示している。一方、もう一つの主要評価項目であるCIBIC+スコアはWeek 8、Week 12ともに3点（Minimal improvement）であり、ベースラインからの改善を示唆している。副次評価項目のNPI-X Totalスコアはベースラインから改善傾向が見られるものの変動があり、DADスコアは一部項目で悪化が見られる。ADAS-Cogの悪化とCIBIC+の改善という結果には矛盾があり、有効性評価の全体的な解釈が困難。評価の信頼性について疑問がある。
        *   **根拠:** 主要評価項目間で結果の方向性が一致しておらず、有効性の評価が困難。特に認知機能評価(ADAS-Cog)の悪化は、CIBIC+の結果と整合しない可能性がある。試験の主要目的である有効性評価の信頼性に関わる問題。
        *   **関連データ:**
            *   QSドメイン: [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 6
            *   QSドメイン: [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 8, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 10
            *   QSドメイン: [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 9, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 11
            *   QSドメイン: [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 8, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 3
            *   QSドメイン: [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 9, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 3
            *   QSドメイン: NPI-X, DADの各時点データ

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「HYPERCHOLESTEROLAEMIA」の開始日(AESTDTC=2007)が、有害事象の収集日(AEDTC=2013-12-04)や治験開始日(RFSTDTC=2013-10-25)より大幅に前である。また、この情報は既往歴(MH)ドメインではなく有害事象(AE)ドメインに記録されている。データのドメイン間での不整合および記録の適切性に問題がある。
        *   **根拠:** AE開始日と収集日の大幅な乖離、およびMHではなくAEへの記録は、データの正確性とドメイン定義の遵守に関する問題を示唆する。これは医学的評価(M-4)にも影響を与える。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'HYPERCHOLESTEROLAEMIA', [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2007', [Date/Time of Collection(AE.AEDTC)] = '2013-12-04'
            *   MHドメインに高コレステロール血症の記録なし
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「APPLICATION SITE PRURITUS」が、異なるSequence Number (AESEQ=4, AESEQ=7) で記録されている。AESEQ=7はSeverityが悪化した時点の記録と考えられるが、RELRECで両者が同じRELIDに紐づけられている。AEの悪化を記録する方法として適切か、内部で確認が必要。
        *   **根拠:** 同一事象の複数レコード記録は、データの解釈や集計に影響を与える可能性がある。SDTM IGのガイダンスに沿った記録方法か確認が必要。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS', [Sequence Number(AE.AESEQ)] = 4, [Severity/Intensity(AE.AESEV)] = 'MILD'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE PRURITUS', [Sequence Number(AE.AESEQ)] = 7, [Severity/Intensity(AE.AESEV)] = 'MODERATE'
            *   [Relationship Identifier(RELREC.RELID)] = '01-703-1076-E08' (AESEQ=4, 7に共通)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 併用薬(CM)ドメインにおいて、複数の薬剤 (CORTISONE, LAC-HYDRIN, LIPITOR, LOPID, MEVACOR, TIMOPTIC) の標準化された薬剤名(CMDECOD)が"UNCODED"または空白となっている。
        *   **根拠:** 薬剤名の標準化は、データ集計や安全性評価（薬物相互作用など）の正確性のために重要。データ品質の問題。
        *   **関連データ:**
            *   CMドメインの複数レコードで [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED' または空白
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 併用薬(CM)ドメインにおいて、複数の薬剤 (CORTISONE, LAC-HYDRIN, LIPITOR, LOPID, MEVACOR, TIMOPTIC) の薬剤分類(CMCLAS)が"UNCODED"または空白となっている。
        *   **根拠:** 薬剤分類情報は、併用薬の傾向分析や安全性評価に有用。データ品質の問題。
        *   **関連データ:**
            *   CMドメインの複数レコードで [Medication Class(CM.CMCLAS)] = 'UNCODED' または空白
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 併用薬(CM)ドメインにおいて、LAC-HYDRINの用量(CMDOSE)が欠損している。
        *   **根拠:** 用量情報は併用薬の影響を評価する上で重要。データの完全性の問題。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'LAC-HYDRIN', [Dose per Administration(CM.CMDOSE)] = null
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 併用薬(CM)ドメインにおいて、ASPIRINの薬剤分類(CMCLAS)が"NERVOUS SYSTEM"と記録されている。これは一般的な分類（例：抗血小板薬）とは異なる。
        *   **根拠:** 不適切な分類は、データ集計や解釈に誤りを生じさせる可能性がある。データ品質の問題。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'ASPIRIN', [Medication Class(CM.CMCLAS)] = 'NERVOUS SYSTEM'
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** 臨床検査(LB)ドメインにおいて、ベースラインフラグ(LBBLFL)がVisit 1 (SCREENING 1) のデータにのみ 'Y' と付与されており、Visit 3 (BASELINE) のデータには付与されていない。
        *   **根拠:** ベースライン値の定義は解析において重要であり、フラグの付与が一貫していない場合、解析結果に影響を与える可能性がある。プロトコルやSAPでの定義と照らし合わせ、データの一貫性を確認する必要がある。
        *   **関連データ:**
            *   LBドメイン: [Baseline Flag(LB.LBBLFL)] = 'Y' (Visit 1のみ), [Visit Name(LB.VISIT)] = 'BASELINE' のレコードでは LBBLFL = ''
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** 臨床検査補足(SUPPLB)ドメインに、QNAM='ENDPOINT' というレコードが存在する。これが最終評価値を示すフラグである可能性が高いが、LBドメイン本体に相当する変数がなく、SUPPドメインで定義されている。
        *   **根拠:** 最終評価値の特定は解析において重要。フラグの定義とLBドメインとの関連を確認し、データ構造の妥当性を評価する必要がある。
        *   **関連データ:**
            *   SUPPLBドメイン: [Qualifier Variable Name(SUPPLB.QNAM)] = 'ENDPOINT', [Data Value(SUPPLB.QVAL)] = 'Y' (複数レコード)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b] (ECG所見) の評価が、提供されたデータからは不能。既往歴(MH)に「ATRIOVENTRICULAR BLOCK」が記録されており、これが除外基準に該当する可能性（Second or third degree heart block unless treated with a pacemaker）がある。ペースメーカー治療の有無に関する情報がなく、適格性が確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** 除外基準違反は参加者の安全性にリスクをもたらし、試験データの解釈にも影響を与える可能性がある。適格性を確認するための情報が不足している。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ATRIOVENTRICULAR BLOCK (SCHEDULED CARDIAC PACEMAKER INSERTION)' (ただし、ペースメーカー挿入が実施されたかは不明)
            *   ECGデータなし
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[17] (重篤な心血管系障害) の評価に関連し、既往歴(MH)の「ATRIOVENTRICULAR BLOCK」が「Clinically significant arrhythmia」や「Symptomatic sick sinus syndrome not treated with a pacemaker」に該当しないか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [17]
        *   **根拠:** 除外基準違反の可能性があり、参加者の安全性に関わるため確認が必要。P-1と関連。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'ATRIOVENTRICULAR BLOCK (SCHEDULED CARDIAC PACEMAKER INSERTION)'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 有害事象として「BENIGN PROSTATIC HYPERPLASIA」が報告されている。これが除外基準[21] (重篤な泌尿生殖器障害) の「Uncontrolled urinary retention」等に該当しないか確認が必要だが、現時点では情報不足。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [21]
        *   **根拠:** 除外基準抵触の可能性は低いと考えられるが、念のため確認。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'BENIGN PROSTATIC HYPERPLASIA'
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時の臨床検査値において、アルブミン、コレステロール、総蛋白、尿酸が基準値上限を超えている。除外基準[27b]では基準値逸脱は除外対象だが、「臨床的に意義がないと判断されれば組み入れ可、その判断は記録される」とある。この判断記録が確認できないため、適格性が不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 除外基準違反の可能性があり、適格性の確認が必要。特に尿酸値は既往歴の痛風と関連する可能性がある。
        *   **関連データ:**
            *   LBドメイン (Visit 1): ALB, CHOL, PROT, URATE が HIGH
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 併用薬として「TIMOPTIC」(点眼薬、β遮断薬) が使用されている。除外基準[31b]の d) Beta blockers の項目で、「Beta blocker eye drops for glaucoma will be considered on a case-by-case basis. Call medical monitor.」と記載されている。Medical Monitorによる使用承認の記録が確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] d)
        *   **根拠:** プロトコルで個別判断と記録が要求されている薬剤の使用について、その記録が確認できない。併用薬制限違反の可能性がある。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TIMOPTIC'
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'VERBATIM_0308' (MHDECOD='GLAUCOMA')
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬として「ASPIRIN」が使用されている。プロトコルの除外薬剤リスト(Section 3.4.2.2 [31b])には明記されていないが、使用が許可されているか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b]
        *   **根拠:** リスト外の薬剤使用について、プロトコル上の扱いを確認する必要がある。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'ASPIRIN'
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬として「LOPID」が治験開始後 Day 34 まで使用されている。プロトコルの除外薬剤リスト(Section 3.4.2.2 [31b])には明記されていないが、使用が許可されているか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b]
        *   **根拠:** リスト外の薬剤使用について、プロトコル上の扱いを確認する必要がある。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'LOPID', [End Date/Time of Medication(CM.CMENDTC)] = '2013-11-27'
    *   **指摘No.:** P-8
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験薬の投与計画と実績の整合性に疑問点あり。EXドメインではDay 1-13に54mg、Day 14-61に81mgが投与されている。これはSEドメインのElement Code HIS (High_Start), HIM (High_Middle) の期間と一致する。しかし、TA/TEドメインで定義されたHigh Dose群の計画 (HIS→HIM→HIE) や各Elementの期間定義 (TE.TEDUR) と完全には一致しない可能性がある。内部でのデータ構造とプロトコル計画の再確認が必要。
        *   **プロトコル該当箇所:** Section 3.1 Figure LZZT.1, TA/TEドメイン定義
        *   **根拠:** 投与計画と実績の不整合は、曝露量評価や有効性・安全性評価に影響を与える可能性がある。ただし、大きな逸脱とは考えにくいため内部確認とする。
        *   **関連データ:**
            *   EXドメイン: EXTRT='XANOMELINE', EXDOSE=54/81, EXSTDTC/EXENDTC
            *   SEドメイン: ETCD='HIS'/'HIM', SESTDTC/SEENDTC
            *   TA/TEドメイン定義
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルでは治験中止時に用量を漸減するよう規定されている（81mg→50mgへ）。しかし、EXドメインの記録ではDay 61に81mg投与が終了したのみで、漸減投与が行われた記録がない。プロトコルからの逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** プロトコルで規定された中止手順が遵守されていない可能性があり、安全性評価に影響する可能性がある。
        *   **関連データ:**
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [End Date/Time of Treatment(EX.EXENDTC)] = '2013-12-24'
    *   **指摘No.:** P-10
        *   **重要度:** Minor
        *   **逸脱の可能性:** 主要評価項目であるADAS-CogおよびCIBIC+の評価が、プロトコル規定のVisit 10 (Week 16) で実施されていない（Visit 9で中止のため）。中止前の最終評価がVisit 9 (Day 61) で行われたと考えられるが、評価スケジュールの逸脱とみなされるか確認が必要。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Schedule of Events (Attachment LZZT.1)
        *   **根拠:** 評価スケジュールの遵守は評価の信頼性に影響する。中止に伴う最終評価として許容されるか確認が必要。
        *   **関連データ:**
            *   QSドメイン: ADAS-Cog, CIBIC+ のデータは Visit 3, 8, 9 のみ存在。
    *   **指摘No.:** P-11
        *   **重要度:** Minor
        *   **逸脱の可能性:** NPI-Xの評価間隔がプロトコル規定の2週間隔と一部一致しない（Week 8からWeek 12が4週間隔）。電話インタビューでの実施記録が含まれているか不明。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures
        *   **根拠:** 評価スケジュールの遵守確認が必要。
        *   **関連データ:**
            *   QSドメイン: NPI-X のデータは Visit 3, 4, 5, 7, 8, 9 で存在。
    *   **指摘No.:** P-12
        *   **重要度:** Minor
        *   **逸脱の可能性:** DADの評価が、プロトコル規定のVisit 10 (Week 16) で実施されていない（Visit 9で中止のため）。P-10と同様の確認が必要。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Schedule of Events (Attachment LZZT.1)
        *   **根拠:** 評価スケジュールの遵守確認が必要。
        *   **関連データ:**
            *   QSドメイン: DAD のデータは Visit 3, 8, 9 のみ存在。
    *   **指摘No.:** P-13
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 9 (Week 12) の実施日(Day 61)が、プロトコルで規定されたVisit Window (Day 84 ± 4 days = Day 80-88) から逸脱している。中止に伴う最終評価のためと考えられるが、逸脱として記録・報告が必要か確認。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit Window規定)
        *   **根拠:** Visit Windowからの逸脱は評価のタイミングに影響を与える可能性がある。中止に伴う逸脱として許容されるか確認が必要。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 9, [Planned Study Day of Visit(SV.VISITDY)] = 84, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-12-24' (Day 61)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-1, P-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 既往歴として「ATRIOVENTRICULAR BLOCK (SCHEDULED CARDIAC PACEMAKER INSERTION)」が報告されていますが、除外基準[16b]および[17]への抵触がないことを確認するため、最終的な診断名、重症度（例：第何度ブロックか）、症状の有無、およびペースメーカー治療が実際に実施されたか、またその時期について詳細をお知らせください。スクリーニング時のECG所見についても確認させていただけますでしょうか。
        *   **クエリ文面（英語）:** Medical History reports 'ATRIOVENTRICULAR BLOCK (SCHEDULED CARDIAC PACEMAKER INSERTION)'. To confirm eligibility per exclusion criteria [16b] & [17], please provide final diagnosis details, severity (e.g., degree of block), symptoms, and confirm if pacemaker was implanted and when. Please also confirm screening ECG findings.
        *   **判断理由:** 除外基準違反の可能性があり、参加者の安全性確保のために心疾患の詳細な評価が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Reported Term for the Medical History(MH.MHTERM)] = 'ATRIOVENTRICULAR BLOCK (SCHEDULED CARDIAC PACEMAKER INSERTION)'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [16b], [17]
            *   関連する医学的知見: AVブロックは重症度により禁忌となる可能性がある。
    *   **クエリNo.:** Q-2 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の臨床検査において、アルブミン、コレステロール、総蛋白、尿酸の値が基準値上限を超えていました。プロトコル除外基準[27b]に基づき、これらの逸脱が臨床的に意義がないと判断された記録（医師の署名付きコメント等）をご提出いただけますでしょうか。
        *   **クエリ文面（英語）:** Screening lab results showed high values for Albumin, Cholesterol, Protein, and Urate. Per protocol exclusion criterion [27b], please provide documentation (e.g., signed investigator assessment) confirming these deviations were determined to be not clinically significant.
        *   **判断理由:** 除外基準違反の可能性があり、適格性の確認記録が必要なため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (Visit 1): ALB, CHOL, PROT, URATE が HIGH
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬として「TIMOPTIC」点眼薬が使用されています。プロトコル除外基準[31b] d)に基づき、Medical Monitorによる使用承認が必要とされています。承認が得られていることを示す記録をご提出いただけますでしょうか。
        *   **クエリ文面（英語）:** Concomitant medication 'TIMOPTIC' eye drops were used. Per protocol exclusion criterion [31b] d), Medical Monitor approval is required for beta blocker eye drops. Please provide documentation confirming this approval was obtained.
        *   **判断理由:** プロトコルで個別承認が要求されている併用薬について、承認記録の確認が必要なため。併用禁止/制限薬違反の可能性がある。
        *   **判断根拠:**
            *   関連するデータ: [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TIMOPTIC'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] d)
    *   **クエリNo.:** Q-4 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 本症例は有害事象により治験を中止されています。中止の直接的な原因となった有害事象（適用部位そう痒感、適用部位皮膚炎）について、中止決定時の重症度、範囲、および実施された処置、その後の転帰に関する詳細な情報をお知らせください。
        *   **クエリ文面（英語）:** This subject discontinued due to an Adverse Event. Please provide detailed information on the AE(s) leading to discontinuation (Application site pruritus, Application site dermatitis), including severity at time of decision, extent, actions taken, and final outcome.
        *   **判断理由:** 治験中止理由となった有害事象の詳細を把握し、安全性評価の妥当性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=4, 5, 7), DSドメイン (DSDECOD='ADVERSE EVENT')
            *   関連するプロトコル箇所: Section 3.10.1 Discontinuations
    *   **クエリNo.:** Q-5 (関連指摘No.: M-4, D-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象として「HYPERCHOLESTEROLAEMIA」が報告されていますが、開始日が2007年となっています。この情報は既往歴として記録すべきと思われますが、ご確認いただけますでしょうか。また、併用薬がLOPIDからMEVACOR、LIPITORへと変更されていますが、その理由と関連する臨床検査結果（脂質プロファイル等）についてもお知らせください。
        *   **クエリ文面（英語）:** AE 'HYPERCHOLESTEROLAEMIA' reported with start date 2007. Please confirm if this should be recorded as Medical History. Also, lipid-lowering therapy changed (LOPID->MEVACOR->LIPITOR). Please provide reason for change and relevant lab results (lipid profile).
        *   **判断理由:** データのドメイン間不整合の修正と、併用薬変更の医学的背景を確認し、安全性・有効性評価への影響を判断するため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='HYPERCHOLESTEROLAEMIA', AESTDTC='2007'), MHドメイン, CMドメイン (LOPID, MEVACOR, LIPITOR)
    *   **クエリNo.:** Q-6 (関連指摘No.: P-9)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 治験中止時の治験薬投与について、プロトコルでは用量を漸減するよう規定されていますが、記録上81mg投与が最終日となっています。漸減投与が実施されなかった理由についてご確認ください。
        *   **クエリ文面（英語）:** The protocol requires dose tapering upon discontinuation. Records indicate the last dose was 81mg. Please clarify why dose tapering was not performed or if the record is inaccurate.
        *   **判断理由:** プロトコル逸脱の可能性があり、中止時の手順遵守状況を確認するため。
        *   **判断根拠:**
            *   関連するデータ: EXドメイン (EXDOSE=81, EXENDTC='2013-12-24')
            *   関連するプロトコル箇所: Section 3.10.1 Discontinuations
    *   **クエリNo.:** Q-7 (関連指摘No.: M-9)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有効性評価について、ADAS-Cog(11)スコアが悪化している一方で、CIBIC+スコアは「Minimal improvement」と評価されています。この結果の解釈について、担当医師の臨床的なご見解をお聞かせください。
        *   **クエリ文面（英語）:** Regarding efficacy assessment, ADAS-Cog(11) score worsened while CIBIC+ was rated 'Minimal improvement'. Please provide the investigator's clinical interpretation of these findings.
        *   **判断理由:** 主要評価項目間の結果に乖離が見られ、有効性評価の信頼性を担保するために臨床的解釈を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (ACTOT, CIBIC)
            *   関連するプロトコル箇所: Section 2.1 Primary Objectives, Section 4.3 Efficacy Analyses

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有害事象「HYPERHIDROSIS」(多汗症) が報告されている。治験薬の薬理作用（コリン作動性）との関連が考えられるため、他の症例でも同様の事象が報告されていないか、安全性データベース等で傾向を確認する。
        *   **判断理由:** 重症度はMILDであり、単発の報告であれば緊急性は低い。まずは内部で傾向を確認する。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='HYPERHIDROSIS')
            *   関連する医学的知見: コリン作動薬の副作用
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「BENIGN PROSTATIC HYPERPLASIA」と「BIOPSY PROSTATE」の記録について、イベントの前後関係を確認し、AEとしての記録が適切かデータマネジメント手順に基づき確認する。
        *   **判断理由:** データ入力の適切性に関する確認であり、安全性への直接的な影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='BENIGN PROSTATIC HYPERPLASIA', 'BIOPSY PROSTATE')
    *   **確認事項No.:** I-3 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 尿酸値が一貫して高値であり、既往歴に痛風がある。痛風治療薬の併用がない点について、他の症例での管理状況も踏まえ、痛風発作のリスク評価やモニタリングの必要性を内部で検討する。
        *   **判断理由:** 治験期間中にAEは発生しておらず、緊急性は低い。内部でのリスク評価を行う。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='URATE'), MHドメイン (MHTERM='GOUT'), CMドメイン
    *   **確認事項No.:** I-4 (関連指摘No.: M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 4で一過性のカルシウム高値が認められた。他の症例でも同様の変動がないか確認し、臨床的な意義について内部で評価する。
        *   **判断理由:** 一過性の軽度な変動であり、緊急性は低い。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='CA', VISITNUM=5)
    *   **確認事項No.:** I-5 (関連指摘No.: M-7)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時のアルブミン、総蛋白の高値について、他のデータとの関連も含め臨床的な意義を内部で評価する。
        *   **判断理由:** 一過性の軽度な変動であり、臨床的意義は低いと考えられるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBTESTCD='ALB', 'PROT', VISITNUM=1)
    *   **確認事項No.:** I-6 (関連指摘No.: M-8)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時の血圧がやや高値であり、既往歴に高血圧があるが降圧薬の使用記録がない。他の症例での管理状況も踏まえ、本試験における高血圧管理の方針について内部で確認する。
        *   **判断理由:** 治験期間中の血圧は概ね安定しており、緊急性は低い。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (VSTESTCD='SYSBP', 'DIABP'), MHドメイン (MHTERM='HYPERTENSION'), CMドメイン
    *   **確認事項No.:** I-7 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「APPLICATION SITE PRURITUS」の重複記録について、AEの悪化や再発を記録する際のデータマネジメント手順を確認し、必要であれば修正または注釈を検討する。
        *   **判断理由:** データ構造の確認であり、医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=4, 7), RELRECドメイン
    *   **確認事項No.:** I-8 (関連指摘No.: D-3, D-4, D-5, D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 併用薬(CM)ドメインにおける薬剤名(CMDECOD)、薬剤分類(CMCLAS)の未コーディング・不適切分類、および用量(CMDOSE)の欠損について、データマネジメント担当部署にてコーディング辞書や手順に基づき修正・追記を行う。
        *   **判断理由:** データクリーニングの一環であり、内部での対応が可能。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン
    *   **確認事項No.:** I-9 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 臨床検査(LB)ドメインのベースラインフラグ(LBBLFL)の付与基準について、プロトコルおよびSAPを確認し、データの整合性を検証する。必要であればフラグの修正を行う。
        *   **判断理由:** データ定義と実装の確認であり、内部での対応が可能。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBBLFL)
            *   関連するプロトコル箇所: Section 4.2 Demographics and Patient Characteristics Measured at Baseline (ベースライン定義に関する記載の可能性)
    *   **確認事項No.:** I-10 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 臨床検査補足(SUPPLB)ドメインのQNAM='ENDPOINT'の定義と使用目的について、データ仕様書等を確認する。
        *   **判断理由:** データ構造と定義の確認であり、内部での対応が可能。
        *   **判断根拠:**
            *   関連するデータ: SUPPLBドメイン (QNAM='ENDPOINT')
    *   **確認事項No.:** I-11 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有害事象「BENIGN PROSTATIC HYPERPLASIA」が除外基準[21]に抵触しないか、症状等を確認し評価する。
        *   **判断理由:** 関連情報が限定的であり、現時点でのリスクは低いと考えられるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AETERM='BENIGN PROSTATIC HYPERPLASIA')
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [21]
    *   **確認事項No.:** I-12 (関連指摘No.: P-6, P-7)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/Medical Monitor
        *   **疑義事項/確認内容:** 併用薬「ASPIRIN」「LOPID」の使用がプロトコル上許容されるか、禁止・制限リストおよび一般的な併用薬に関する規定を確認する。
        *   **判断理由:** リストに明記されていない薬剤であり、安全性への大きな影響は考えにくいが、プロトコル遵守の観点から確認が必要。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='ASPIRIN', 'LOPID')
            *   関連するプロトコル箇所: Section 3.8 Concomitant Therapy, Section 3.4.2.2 Exclusion Criteria [31b]
    *   **確認事項No.:** I-13 (関連指摘No.: P-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** 治験薬投与実績(EX)と投与計画(TA/TE/SE)の整合性について、データ構造とプロトコル計画を詳細に照合し、記録方法に問題がないか確認する。
        *   **判断理由:** データ構造に関する確認であり、内部での対応が可能。
        *   **判断根拠:**
            *   関連するデータ: EX, SE, TA, TE ドメイン
            *   関連するプロトコル箇所: Section 3.1, 3.6
    *   **確認事項No.:** I-14 (関連指摘No.: P-10, P-11, P-12, P-13)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 有効性評価の実施タイミング(Visit 10での未実施、NPI-Xの間隔、Visit 9のWindow逸脱)について、治験中止に伴う最終評価としてプロトコル上許容されるか、逸脱として報告が必要か、試験の手順書等を確認する。
        *   **判断理由:** 評価スケジュールの逸脱は評価の信頼性に影響する可能性があるが、中止に伴うものであるため、まずは内部で手順を確認する。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン, SVドメイン
            *   関連するプロトコル箇所: Section 3.9.1.1, 3.1, Schedule of Events

---

# 01-703-1086のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
71歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（2011年4月27日発症）が報告されている。教育レベルは17年である。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年08月19日|Day -14 (SCREENING 1)|クレアチンキナーゼ(CK)高値 (256 U/L, 基準値上限の1.3倍)。|
|2012年08月22日|Day -11 (SCREENING 1)|MMSEスコア 17点。Hachinski Ischemic Scaleスコア 1点。|
|2012年08月31日|Day -2 (UNSCHEDULED 1.1)|白血球(WBC)低値 (1 THOU/uL, 基準値下限未満)。|
|2012年09月02日|Day 1 (BASELINE)|治験薬 (Xanomeline 54mg パッチ) 投与開始。ADAS-Cog(11)スコア 42点。NPI-X Totalスコア 9点。DAD Totalスコア 85% (34/40)。|
|2012年09月13日|Day 12 (N/A)|有害事象「APPLICATION SITE IRRITATION」(軽度) 発現。|
|2012年09月15日|Day 14 (AMBUL ECG PLACEMENT)|併用薬 Cortisone 1% (外用) 開始。|
|2012年09月16日|Day 15 (WEEK 2)|AST高値 (40 U/L, 基準値上限の1.1倍)。CK高値 (271 U/L, 基準値上限の1.4倍)。白血球(WBC)低値 (1.2 THOU/uL)。NPI-X Totalスコア 6点。|
|2012年09月30日|Day 29 (WEEK 4)|有害事象「APPLICATION SITE IRRITATION」が中等度に悪化。併用薬 Calamine (外用)、Cortisone 2.5% (外用) 開始。|
|2012年10月02日|Day 31 (AMBUL ECG REMOVAL)|好酸球(EOS)高値 (0.60 THOU/uL, 基準値上限の1.1倍)。白血球(WBC)低値 (1.1 THOU/uL)。|
|2012年10月09日|Day 38 (N/A)|有害事象「CHILLS」(軽度) 発現。|
|2012年10月13日|Day 42 (WEEK 6)|有害事象「APPLICATION SITE IRRITATION」が高度に悪化。CK高値 (208 U/L, 基準値上限の1.1倍)。好酸球(EOS)高値 (1.11 THOU/uL, 基準値上限の1.9倍)。白血球(WBC)低値 (1 THOU/uL)。NPI-X Totalスコア 3点。|
|2012年10月15日|Day 44 (N/A)|有害事象「CHILLS」回復。|
|2012年10月27日|Day 56 (WEEK 8)|CK高値 (239 U/L, 基準値上限の1.2倍)。好酸球(EOS)高値 (0.69 THOU/uL, 基準値上限の1.2倍)。白血球(WBC)低値 (1.3 THOU/uL)。ADAS-Cog(11)スコア 36点。CIBIC+評価: Minimal improvement (3)。DAD Totalスコア 87.5% (35/40)。NPI-X Totalスコア 10点 (Aberrant Motor Behaviorが出現)。|
|2012年11月10日|Day 70 (WEEK 10 (T))|NPI-X Totalスコア 10点。|
|2012年11月27日|Day 87 (WEEK 12)|白血球(WBC)低値 (0.9 THOU/uL)。NPI-X Totalスコア 8点。|
|2012年12月04日|Day 94 (N/A)|治験薬投与終了 (EXデータに基づく)。|
|2012年12月11日|Day 101 (WEEK 14 (T))|NPI-X Totalスコア 10点。|
|2012年12月13日|Day 103 (N/A)|併用薬 Calamine, Cortisone 1%, Cortisone 2.5% 終了。|
|2012年12月24日|Day 114 (WEEK 16)|有害事象により試験中止。CK高値 (289 U/L, 基準値上限の1.5倍)。白血球(WBC)低値 (0.8 THOU/uL)。ADAS-Cog(11)スコア 39点。CIBIC+評価: Minimal improvement (3)。DAD Totalスコア 75% (30/40)。NPI-X Totalスコア 9点。|
|2013年01月02日|Day 123 (AE FOLLOW-UP)|有害事象「APPLICATION SITE IRRITATION」回復。|
|2013年03月26日|Day 206 (RETRIEVAL)|Retrieval Visit実施。ADAS-Cog(11)スコア 39点。CIBIC+評価: Minimal improvement (3)。DAD Totalスコア 77.5% (31/40)。NPI-X Totalスコア 7点。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** スクリーニング時 (Day -2) から一貫して白血球数 (WBC) が基準値下限未満 (1.0 -> 1.2 -> 1.1 -> 1.0 -> 1.3 -> 0.9 -> 0.8 x10^3/uL) であり、治験終了時 (Day 114) にはさらに低下傾向が見られる。ベースライン前からの低値であり、治験薬との直接的な関連は不明確だが、持続的な白血球減少は感染症リスクを高める可能性があり、参加者の安全性にとって重大な懸念事項である。除外基準違反の可能性もある (P-1参照)。
        *   **根拠:** 一般的な医学知識として、持続的な白血球減少症は易感染状態を示唆し、重篤な感染症につながるリスクがある。特に高齢者や基礎疾患を持つ患者では注意が必要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'WBC'
            *   [Category for Lab Test(LB.LBCAT)] = 'HEMATOLOGY'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -2, 15, 31, 42, 56, 87, 114
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1, 1.2, 1.1, 1, 1.3, 0.9, 0.8
            *   [Standard Units(LB.LBSTRESU)] = 'GI/L'
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.8
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW' (all timepoints)
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** スクリーニング時 (Day -14) から断続的にクレアチンキナーゼ (CK) が基準値上限を超えて高値 (256 -> 271 -> 184 -> 208 -> 239 -> 197 -> 289 U/L) を示している。特に治験終了時 (Day 114) には最も高い値となっている。筋肉に関連する有害事象の報告はないが、持続的または悪化するCK高値は横紋筋融解症などの潜在的な筋障害リスクを示唆する可能性があり、安全性評価上注意が必要。
        *   **根拠:** 一般的な医学知識として、CK高値は筋損傷を示唆する。薬剤性が原因となることもあり、特に高値が持続・悪化する場合は横紋筋融解症などの重篤な状態への進展リスクを考慮する必要がある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK'
            *   [Category for Lab Test(LB.LBCAT)] = 'CHEMISTRY'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -14, 15, 31, 42, 56, 87, 114
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 256, 271, 184, 208, 239, 197, 289
            *   [Standard Units(LB.LBSTRESU)] = 'U/L'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 198
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH', 'HIGH', 'NORMAL', 'HIGH', 'HIGH', 'NORMAL', 'HIGH'
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 治験期間中 (Day 31, 42, 56) に好酸球数 (EOS) が基準値上限を超えて高値 (0.60 -> 1.11 -> 0.69 x10^3/uL) を示した。これは有害事象「APPLICATION SITE IRRITATION」の発現・悪化時期とおおむね一致しており、皮膚反応との関連が示唆される。好酸球増多はアレルギー反応や薬剤反応の可能性を示唆するため、臨床的意義の評価が必要。
        *   **根拠:** 一般的な医学知識として、好酸球増多はアレルギー反応、寄生虫感染、特定の薬剤に対する反応などで見られる。皮膚症状を伴う場合、薬剤性過敏症症候群 (DIHS/DRESS) などの可能性も念頭に置く必要があるが、本症例では他の所見（発熱、肝機能障害など）は顕著ではない。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'EOS'
            *   [Category for Lab Test(LB.LBCAT)] = 'HEMATOLOGY'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 31, 42, 56
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.6, 1.11, 0.69
            *   [Standard Units(LB.LBSTRESU)] = 'GI/L'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 0.57
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH' (all 3 timepoints)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE IRRITATION'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = 12
            *   [Severity/Intensity(AE.AESEV)] = MILD (Day 12), MODERATE (Day 29), SEVERE (Day 42), MILD (Day 123)
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** 有効性評価指標間で結果の傾向に一部乖離が見られる。ADAS-Cog(11)およびCIBIC+はベースラインと比較して改善傾向を示しているが、DAD TotalスコアはDay 114でベースラインより悪化し、NPI-X Totalスコアは期間中に変動が大きい（特にDay 56以降にAberrant Motor Behaviorが出現しスコアが悪化）。これらの乖離が治験薬の有効性評価の解釈に与える影響について、内部での議論が必要。
        *   **根拠:** 複数の有効性評価項目を用いる場合、結果の一貫性を確認することが重要。乖離が見られる場合、その理由（例：評価指標の特性、患者の状態変化、評価のばらつき）を考察する必要がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'DAITM01'-'DAITM40', 'NPTOT', 'NPITM10S'
            *   [Category of Question(QS.QSCAT)] = 'ALZHEIMER''S DISEASE ASSESSMENT SCALE', 'CLINICIAN''S INTERVIEW-BASED IMPRESSION OF CHANGE (CIBIC+)', 'DISABILITY ASSESSMENT FOR DEMENTIA (DAD)', 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [Visit Number(QS.VISITNUM)] = 3, 8, 10, 201 (ADAS-Cog, CIBIC+, DAD), 3, 4, 7, 8, 8.1, 9, 9.1, 10, 201 (NPI-X)
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = (各スコア値)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 治験薬の最終投与日 (EX.EXENDTC = 2012-12-04, Day 94) が、被験者の中止日 (DS.DSSTDTC = 2012-12-24, Day 114) と一致していない。実際の最終投与日を確認する必要があり、曝露期間の正確な評価に影響する。
        *   **根拠:** 曝露期間は安全性および有効性の評価において重要な情報であり、正確な記録が必要。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2012-12-04'
            *   [Study Day of End of Treatment(EX.EXENDY)] = 94
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-12-24'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 114
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 有害事象「CHILLS」について、期間が重複する2つのレコード (AESEQ=4, 5) が存在する。AESEQ=4の転帰は'NOT RECOVERED/NOT RESOLVED'、AESEQ=5の転帰は'RECOVERED/RESOLVED'となっている。RELRECに関連付けがないため別イベントとして扱われているが、同一イベントの転帰更新の可能性が高い。データの記録方法として適切か確認が必要だが、医学的評価への影響は小さい。
        *   **根拠:** 同一イベントは一意に識別されるべきであり、更新情報は元のレコードを修正するか、明確な関連付けを行うのが一般的。ただし、内容の解釈は可能。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'CHILLS'
            *   [Sequence Number(AE.AESEQ)] = 4, 5
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-10-09' (both)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-10-15' (both)
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AESEQ=4), 'RECOVERED/RESOLVED' (AESEQ=5)
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。GCP上記録が必要な情報だが、他のデータから治験参加前に同意が取得されていることは推測可能であり、評価への直接的な影響は小さい。
        *   **根拠:** GCP要件。ただし、治験開始日 (RFSTDTC) や初回投与日 (RFXSTDTC) は記録されており、同意が先行している蓋然性は高い。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (Missing)

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** スクリーニング時 (Day -2) の白血球数 (WBC) が1.0 x10^3/uLであり、基準値下限 (3.8 x10^3/uL) を下回っている。これは除外基準 EXCL27b「Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes: ... np white blood cell count」に抵触する可能性がある。適格性がないにも関わらず登録された可能性があり、参加者の安全性および試験結果の信頼性に重大な影響を与える。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** プロトコルで規定された除外基準に該当する検査値異常がスクリーニング時に確認されている。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'WBC'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -2
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1
            *   [Standard Units(LB.LBSTRESU)] = 'GI/L'
            *   [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.8
            *   [Reference Range Indicator(LB.LBNRIND)] = 'LOW'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 併用薬としてCortisone (1%および2.5%) が外用で使用されている。プロトコル 3.6.2 では皮膚刺激に対してHydrocortisone 1% クリームの使用が規定されている。薬剤名 (Cortisone vs Hydrocortisone) および用量 (2.5%) がプロトコル規定と異なる可能性がある。ただし、局所使用であり、皮膚AEに対する処置として医学的に妥当な範囲と考えられるため、安全性や評価への影響は小さいと判断される。
        *   **プロトコル該当箇所:** Section 3.6.2, Section 3.4.2.2 [31b] k) (Systemic corticosteroidsは禁止)
        *   **根拠:** 報告されている薬剤名・用量がプロトコル記載と異なる。ただし、局所ステロイドの使用自体はプロトコルで想定されている。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'CORTISONE'
            *   [Dose per Administration(CM.CMDOSE)] = 1, 2.5
            *   [Dose Units(CM.CMDOSU)] = '%'
            *   [Route of Administration(CM.CMROUTE)] = 'TOPICAL'
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** NPI-X評価が、プロトコルで規定されている2週間ごとのスケジュール (プロトコル 3.9.1.1) に対して、一部のVisit (Week 4, 5, 6, 12, 20, 24, 26相当の時期) で実施記録がない。電話インタビューでの実施記録が欠落している可能性がある。評価の欠損は評価の信頼性に影響しうるが、他の時点でのデータが存在するため影響は限定的と考えられる。
        *   **プロトコル該当箇所:** Section 3.9.1.1
        *   **根拠:** QSドメインのNPI-X (QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)') の記録が一部の期間で欠落している。
        *   **関連データ:**
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [Visit Number(QS.VISITNUM)] = 3, 4, 7, 8, 8.1, 9, 9.1, 10, 201
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** Urinalysis (尿検査) が、プロトコルで規定されたVisit (Visits 4, 9, 12) 以外 (Visit 10) でも実施されている。プロトコルからの逸脱であるが、追加の安全性評価であり、参加者の安全性や評価の信頼性への悪影響はないと考えられる。
        *   **プロトコル該当箇所:** Section 3.9.3.3, Schedule of Events (Attachment LZZT.1)
        *   **根拠:** LBドメインのUrinalysis (LBCAT='URINALYSIS') の記録がVisit 10に存在する。
        *   **関連データ:**
            *   [Category for Lab Test(LB.LBCAT)] = 'URINALYSIS'
            *   [Visit Number(LB.VISITNUM)] = 10

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号 1086 について、スクリーニング時 (2012年8月31日) の白血球数が 1.0 GI/L と基準値 (3.8-10.7 GI/L) を下回っており、除外基準 [27b] に抵触する可能性があります。また、治験期間中も一貫して低値が持続しています。本患者が適格と判断された根拠、および持続する白血球減少症の臨床的意義と安全性に関する評価について詳細をご教示ください。参加者の安全確保およびデータの信頼性担保の観点から確認が必要です。
        *   **クエリ文面（英語）:** Regarding subject 1086, the WBC count at screening (2012-08-31) was 1.0 GI/L, which is below the reference range (3.8-10.7 GI/L) and may violate exclusion criterion [27b]. Low WBC counts persisted throughout the study. Please provide the rationale for eligibility determination and assess the clinical significance and safety implications of the persistent leukopenia. This information is crucial for subject safety and data integrity.
        *   **判断理由:** スクリーニング時の除外基準抵触の可能性があり、適格性に疑義があるため。また、持続するWBC低値は参加者の安全性に重大なリスクをもたらす可能性があるため、臨床的評価が必要。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'WBC', [Study Day of Specimen Collection(LB.LBDY)] = -2, 15, 31, 42, 56, 87, 114, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1, 1.2, 1.1, 1, 1.3, 0.9, 0.8, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 3.8
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
            *   関連する医学的知見: 白血球減少症、易感染性、除外基準違反
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号 1086 について、スクリーニング時 (2012年8月19日) からクレアチンキナーゼ(CK)が断続的に高値を示し、治験終了時 (2012年12月24日) には 289 U/L となっています。筋肉に関連する有害事象の報告はありませんが、持続的なCK高値の臨床的意義と安全性に関する評価についてご教示ください。潜在的な筋障害リスクの観点から確認が必要です。
        *   **クエリ文面（英語）:** Regarding subject 1086, Creatine Kinase (CK) levels were intermittently elevated since screening (2012-08-19) and reached 289 U/L at study termination (2012-12-24). Although no muscle-related AEs were reported, please assess the clinical significance and safety implications of the persistent CK elevation, considering potential myopathy risk.
        *   **判断理由:** 持続的かつ悪化傾向のあるCK高値は、潜在的な筋障害リスクを示唆するため、臨床的な評価が必要。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK', [Study Day of Specimen Collection(LB.LBDY)] = -14, 15, 31, 42, 56, 87, 114, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 256, 271, 184, 208, 239, 197, 289, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 198
            *   関連する医学的知見: CK高値、筋障害、横紋筋融解症リスク
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号 1086 について、治験期間中 (Study Day 31, 42, 56) に好酸球数(EOS)の高値 (最大 1.11 GI/L) が認められました。これは有害事象「APPLICATION SITE IRRITATION」の悪化時期と一致していますが、好酸球増多の臨床的意義と安全性に関する評価についてご教示ください。アレルギー反応や薬剤反応の可能性の観点から確認が必要です。
        *   **クエリ文面（英語）:** Regarding subject 1086, elevated Eosinophil (EOS) counts (up to 1.11 GI/L) were observed during the study (Study Days 31, 42, 56), coinciding with worsening of AE 'APPLICATION SITE IRRITATION'. Please assess the clinical significance and safety implications of the eosinophilia, considering potential allergic or drug reactions.
        *   **判断理由:** 好酸球増多はアレルギー反応や薬剤反応を示唆する可能性があり、皮膚AEとの関連も含めて臨床的な評価が必要。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'EOS', [Study Day of Specimen Collection(LB.LBDY)] = 31, 42, 56, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.6, 1.11, 0.69, [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 0.57, [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE IRRITATION'
            *   関連する医学的知見: 好酸球増多症、アレルギー反応、薬剤反応
    *   **クエリNo.:** Q-4 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 患者番号 1086 について、治験薬の最終投与日として記録されている日付 (2012年12月4日、Study Day 94) が、有害事象による中止日 (2012年12月24日、Study Day 114) と一致していません。実際の最終投与日をご確認の上、修正をお願いします。正確な曝露期間の把握のため確認が必要です。
        *   **クエリ文面（英語）:** For subject 1086, the recorded End Date/Time of Treatment (2012-12-04, Study Day 94) does not match the disposition date due to AE (2012-12-24, Study Day 114). Please verify the actual last date of study drug administration and correct the record if necessary. This is needed for accurate exposure assessment.
        *   **判断理由:** 曝露期間の評価に影響するため、正確な最終投与日の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: [End Date/Time of Treatment(EX.EXENDTC)] = '2012-12-04', [Study Day of End of Treatment(EX.EXENDY)] = 94, [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-12-24', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 114

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-4)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価指標 (ADAS-Cog, CIBIC+, DAD, NPI-X) 間で結果の傾向に一部乖離が見られる。特にNPI-Xの変動が大きい。各指標の経時変化と相互関係について、統計解析担当者およびメディカルモニター間で解釈を議論し、最終的な有効性評価への影響を検討する。個々の指標の変動は疾患特性や評価時期による可能性もあり、直ちにクエリ発行は不要と判断。
        *   **判断理由:** 指標間の乖離は臨床試験では起こりうることであり、まずは内部での解釈・議論が必要。評価の信頼性を根本的に揺るがす矛盾とは現時点では判断できない。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのADAS-Cog, CIBIC+, DAD, NPI-X関連データ
    *   **確認事項No.:** I-2 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「CHILLS」について、期間が重複する2つのレコード (AESEQ=4, 5) が存在する。RELRECに関連付けがないが、内容から同一イベントの転帰更新の可能性が高い。データマネジメント手順として適切か確認し、必要であれば修正または注釈を追加する。医学的評価への影響は小さいと判断。
        *   **判断理由:** データ記録方法に関する軽微な不整合であり、内容の解釈は可能。医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ=4, 5), RELRECドメイン
    *   **確認事項No.:** I-3 (関連指摘No.: D-2, P-1の一部)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 同意取得日 (DM.RFICDTC) が欠損している。GCP要件に関する記録不備。医療機関でのソースドキュメント確認時に同意取得の事実と日付を確認し、内部記録として保管する。治験実施への影響は小さいと判断。
        *   **判断理由:** GCP上の記録不備だが、他の日付情報から同意取得が先行している蓋然性が高く、治験の進行や評価への影響は小さい。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '' (Missing)
            *   関連するプロトコル箇所: Section 5.1
    *   **確認事項No.:** I-4 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA, Medical Monitor
        *   **疑義事項/確認内容:** 併用薬としてCortisone (1%および2.5%) が外用で使用されている記録がある。プロトコルではHydrocortisone 1%の使用が規定されている。薬剤名・用量の差異について、処方の意図や実際の使用状況を内部で確認・考察する。局所使用であり安全性リスクは低いと考えられるため、医療機関への問い合わせは不要と判断。
        *   **判断理由:** プロトコル規定との軽微な差異であり、医学的妥当性は高いと考えられるため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT='CORTISONE')
            *   関連するプロトコル箇所: Section 3.6.2
    *   **確認事項No.:** I-5 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA, DM
        *   **疑義事項/確認内容:** NPI-X評価が一部の期間で欠落している可能性がある。プロトコルでは2週間ごとに電話インタビューでの実施も規定されているため、電話での評価記録が適切に転記されているか、あるいは実施されなかったのかを内部で確認する。他の有効性データがあるため、評価全体への影響は限定的と判断。
        *   **判断理由:** 評価スケジュールの逸脱の可能性があるが、影響は限定的であり、まずは内部での記録確認が必要。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)')
            *   関連するプロトコル箇所: Section 3.9.1.1
    *   **確認事項No.:** I-6 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Urinalysis (尿検査) が予定外のVisit 10で実施されている。プロトコルからの逸脱であるが、追加の安全性評価であり問題はないと判断。内部記録として残す。
        *   **判断理由:** プロトコル逸脱ではあるが、安全性評価を追加する方向であり、リスクはないため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (LBCAT='URINALYSIS', VISITNUM=10)
            *   関連するプロトコル箇所: Section 3.9.3.3, Schedule of Events (Attachment LZZT.1)

---

# 01-703-1096のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    49歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2006年12月20日発症、Primary Diagnosis）、軽度の聴力低下（Significant Pre-existing Condition）が報告されている。教育歴は6年 (EDUCATION LEVEL)。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年12月05日|Day -51 (N/A)|臨床検査実施 (LB)|
|2012年12月19日|Day -37 (SCREENING 1)|スクリーニング評価実施。MMSE=22点、Hachinski Ischemic Score=0点。身長 160.02 cm、体重 81.65 kg。バイタルサイン、臨床検査 (血液学) 実施。|
|2012年12月19日|Day -37 (UNSCHEDULED 1.1)|臨床検査実施 (血液学)|
|2012年12月29日|Day -27 (UNSCHEDULED 1.2)|臨床検査実施 (Vitamin B12)。結果は基準値下限付近 (149.8 pmol/L, 基準値 148-664)。|
|2013年01月23日|Day -2 (SCREENING 2 / UNSCHEDULED 1.3)|バイタルサイン、臨床検査実施。Vitamin B12は正常化 (230.2 pmol/L)。|
|2013年01月25日|Day 1 (BASELINE)|ベースライン評価実施。体重 81.19 kg。バイタルサイン測定 (臥位BP 142/70 mmHg, Pulse 74 bpm; 立位1分後BP 150/72 mmHg, Pulse 82 bpm)。ADAS-Cog(11) Total Score=16。DAD評価実施。NPI-X Total Score=13 (Agitation/Aggression, Anxiety, Apathy/Indifference, Irritability/Lability, Aberrant Motor Behaviorあり)。治験薬 (Placebo) 投与開始。|
|2013年02月08日|Day 15 (AMBUL ECG PLACEMENT)|バイタルサイン測定。|
|2013年02月09日|Day 16 (WEEK 2)|Visit実施。バイタルサイン測定 (臥位BP 140/74 mmHg, Pulse 66 bpm)。体重 80.74 kg。臨床検査実施。NPI-X Total Score=10 (Agitation/Aggression, Depression/Dysphoria, Apathy/Indifference, Irritability/Lability, Aberrant Motor Behaviorあり)。治験薬投与継続。|
|2013年02月23日|Day 30 (WEEK 4)|Visit実施。バイタルサイン測定 (臥位BP 150/80 mmHg, Pulse 78 bpm)。体重 83.92 kg (ベースラインから+2.73 kg)。臨床検査実施。NPI-X Total Score=13 (Agitation/Aggression, Depression/Dysphoria, Apathy/Indifference, Irritability/Lability, Aberrant Motor Behaviorあり)。Disposition Eventとして「FINAL LAB VISIT」記録。|
|2013年02月27日|Day 34 (AMBUL ECG REMOVAL)|バイタルサイン測定。|
|2013年03月16日|Day 51 (N/A)|治験薬 (Placebo) 最終投与日。|
|2013年03月29日|Day 64 (WEEK 6)|Disposition Eventとして「LOST TO FOLLOW-UP」記録。治験中止。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   指摘事項なし

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 患者の年齢 (Age) が49歳であり、選択基準 [1] (Males and postmenopausal females at least 50 years of age) を満たしていない可能性がある。女性 (Sex=F) であるが、閉経後 (Postmenopausal) かどうかの情報がDMドメインにないため、適格性を確認できない。年齢基準違反の場合、参加者の適格性に疑義が生じ、データの解釈に影響を与える可能性がある。
        *   **根拠:** DMドメインのデータとプロトコル選択基準 [1] の不一致。
        *   **関連データ:**
            *   [Age(DM.AGE)] = 49
            *   [Sex(DM.SEX)] = 'F'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** スクリーニング時 (Day -27) のビタミンB12 (Vitamin B12) の検査結果が基準値下限 (149.77 pmol/L, 基準値 148-664 pmol/L) であった。除外基準 [28b] (Central laboratory test values below reference range for ... vitamin B12) に抵触する可能性があったが、Day -2の再検査では正常範囲内 (230.19 pmol/L) であった。最終的に適格と判断されたと推測されるが、その経緯や判断根拠の記録がない。
        *   **根拠:** LBドメインのデータとプロトコル除外基準 [28b] の照合。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Visit Number(LB.VISITNUM)] = 1.2, [Study Day of Specimen Collection(LB.LBDY)] = -27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 149.7734, [Reference Range Lower Limit-Std Units(LB.LBSTNRLO)] = 148, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL' (ただし下限値に近い)
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Visit Number(LB.VISITNUM)] = 1.3, [Study Day of Specimen Collection(LB.LBDY)] = -2, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 230.1936, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 有害事象 (AE) および併用薬 (CM) のデータが全く報告されていない。アルツハイマー病患者であり、Placebo群とはいえ、試験期間中に有害事象や併用薬が全くなかったとは考えにくい。記録漏れの可能性があり、安全性評価の完全性に疑義が生じる。
        *   **根拠:** AEドメイン、CMドメインのレコード数が0であること。一般的な臨床試験におけるデータ収集状況との乖離。
        *   **関連データ:**
            *   AEドメイン: records = 0
            *   CMドメイン: records = 0
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 同意取得日時 (Date/Time of Informed Consent) がDMドメインで欠損している。同意取得は治験参加の基本であり、記録の欠損はGCP遵守および参加者の権利保護の観点から問題である。
        *   **根拠:** DMドメインの必須情報 (プロトコル 5.1) の欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損)
    *   **指摘No.:** D-5
        *   **重要度:** Critical
        *   **内容:** Lost to follow-upのため、主要評価項目であるADAS-CogおよびCIBIC+、ならびに副次評価項目であるDAD、NPI-Xの最終評価時点 (Week 24/26) のデータが欠損している。試験の主要目的である有効性評価が不可能であり、データの信頼性および試験の科学的妥当性に重大な影響を与える。
        *   **根拠:** QSドメインのデータがWeek 4 (NPI-X) またはBaseline (その他) までしか存在しないこと。DSドメインでLost to follow-upが記録されていること。
        *   **関連データ:**
            *   QSドメイン: Week 24/26に該当するデータなし
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'LOST TO FOLLOW-UP', [Study Day of Start of Disposition Event(DS.DSSTDY)] = 64
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 除外基準 [28b] の評価に必要な葉酸 (Folate)、および除外基準 [29b] の評価に必要な梅毒 (Syphilis) スクリーニングの検査データがLBドメインに存在しない。これらの検査が実施され、基準を満たしていたか確認できない。
        *   **根拠:** LBドメインに必要な検査項目データが存在しないこと。プロトコル除外基準の確認が不完全。
        *   **関連データ:**
            *   LBドメイン: LBTESTCD='FOLATE', 'SYPH' に該当するレコードなし

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準 [1] (Males and postmenopausal females at least 50 years of age) 違反の可能性。患者年齢が49歳であり、基準を満たしていない。女性であるが閉経後かの確認情報もない。参加者の適格性に疑義があり、プロトコルからの逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [1]
        *   **根拠:** DMデータの年齢と選択基準の不一致。
        *   **関連データ:**
            *   [Age(DM.AGE)] = 49
            *   [Sex(DM.SEX)] = 'F'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 選択基準 [5] (CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year) の遵守状況が不明。関連するデータが提供されていないため、スクリーニング時に適切な画像評価が行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5]
        *   **根拠:** 選択基準の確認に必要な情報の欠如。
        *   **関連データ:** なし
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 選択基準 [6] (Investigator has obtained informed consent...) の遵守状況が不明。同意取得日時 (DM.RFICDTC) が欠損しており、適切な同意取得が行われたか確認できない。参加者の権利保護に関する重要な逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [6], Section 5.1 Informed Consent
        *   **根拠:** 同意取得日の記録欠損。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損)
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [16b] (Evidence from ECG recording at screening of any listed condition) の遵守状況が不明。スクリーニング時のECGデータが提供されておらず、評価が行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** 除外基準の確認に必要な情報の欠如。
        *   **関連データ:** なし
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [28b] (Central laboratory test values below reference range for folate...) の遵守状況が一部不明。葉酸 (Folate) の検査データがなく、基準を満たしていたか確認できない。ビタミンB12は一時下限値付近だったが正常化。TSHは正常。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [28b]
        *   **根拠:** 除外基準の確認に必要な検査データの一部欠損。
        *   **関連データ:**
            *   LBドメイン: LBTESTCD='FOLATE' に該当するレコードなし
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準 [29b] (Positive syphilis screening) の遵守状況が不明。梅毒スクリーニングの検査データがなく、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 除外基準の確認に必要な検査データの欠損。
        *   **関連データ:**
            *   LBドメイン: LBTESTCD='SYPH' に該当するレコードなし
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準 [10] (Use of any investigational agent or approved Alzheimer’s therapeutic medication within 30 days prior to enrollment) および [31b] (Treatment with [specified] medications within [specified] washout periods...) の遵守状況が不明。併用薬 (CM) データが欠損しているため、禁止・制限薬の使用がなかったか確認できない。安全性および有効性評価に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [10], [31b], Section 3.8 Concomitant Therapy
        *   **根拠:** 併用薬データの欠損。
        *   **関連データ:**
            *   CMドメイン: records = 0
    *   **指摘No.:** P-8
        *   **重要度:** Critical
        *   **逸脱の可能性:** 主要評価項目 (ADAS-Cog, CIBIC+) および副次評価項目 (DAD, NPI-X) の最終評価 (Week 24/26) が実施されていない。Lost to follow-upによる中止のため、プロトコルで規定された評価スケジュールを完了できていない。試験の主要目的達成に不可欠なデータが欠損しており、科学的妥当性に重大な影響がある。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** QSデータの最終評価欠損、DSドメインの中止記録。
        *   **関連データ:**
            *   QSドメイン: Week 24/26に該当するデータなし
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'LOST TO FOLLOW-UP'
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたECG評価 (Visits 4, 5, 7, 8, 9, 10, 11, 12, 13) の実施記録がない。安全性モニタリング計画からの逸脱の可能性があり、参加者の安全性監視が適切に行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** ECGデータの欠損。
        *   **関連データ:** なし
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定された24時間 Ambulatory ECG (Visit 2) の実施記録がない。ベースラインの心血管安全性評価が適切に行われたか確認できない。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** Ambulatory ECGデータの欠損。
        *   **関連データ:** なし
    *   **指摘No.:** P-11
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルで規定された薬物動態 (PK) 測定用採血 (Visits 3, 4, 5, 7, 9, 11) の実施記録がない。
        *   **プロトコル該当箇所:** Section 3.9.2 Pharmacokinetics, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** PK関連データの欠損。
        *   **関連データ:** なし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: P-1, D-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者様のスクリーニング時の「年齢」が「49」歳と記録されていますが、選択基準[1]では50歳以上と規定されています。登録時の適格性についてご確認ください。また、女性の場合、閉経後 (Postmenopausal) であったかどうかも併せてご確認ください。
        *   **クエリ文面（英語）:** Subject age was 49 years at screening, but inclusion criterion 1 requires age >= 50. Please confirm eligibility and if female, confirm postmenopausal status.
        *   **判断理由:** 選択基準違反の可能性があり、参加者の適格性を明確にする必要があるため。
        *   **判断根拠:**
            *   関連するデータ: [Age(DM.AGE)] = 49, [Sex(DM.SEX)] = 'F'
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [1]
    *   **クエリNo.:** Q-2 (関連指摘No.: P-3, D-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者様の「同意取得日時」の記録がありません。同意取得日をご確認の上、ご報告ください。
        *   **クエリ文面（英語）:** Date of Informed Consent (RFICDTC) is missing. Please provide the date.
        *   **判断理由:** 同意取得は治験参加の必須要件であり、記録の欠損はGCP遵守の観点から確認が必要なため。
        *   **判断根拠:**
            *   関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = "" (欠損)
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
    *   **クエリNo.:** Q-3 (関連指摘No.: D-3, P-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA/Medical Monitor
        *   **医療機関への問い合わせ文面:** 本症例では、有害事象 (AE) および併用薬 (CM) の報告がありません。試験期間中にAEおよびCMが全くなかったのか、あるいは記録漏れかご確認ください。もし記録漏れであれば、追記をお願いいたします。
        *   **クエリ文面（英語）:** No Adverse Events (AE) or Concomitant Medications (CM) are reported for this subject. Please confirm if this is correct or if data is missing. If missing, please provide the data.
        *   **判断理由:** 安全性評価の完全性を担保するため、AE/CM情報の有無を明確にする必要があるため。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン records = 0, CMドメイン records = 0
            *   関連するプロトコル箇所: Section 3.9.3.2 Clinical Adverse Events, Section 3.8 Concomitant Therapy
    *   **クエリNo.:** Q-4 (関連指摘No.: P-9, P-10)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているスクリーニング時のECG (除外基準[16b]確認用)、Visit 4, 5でのECG、およびVisit 2での24時間ホルター心電図の実施記録/結果が見当たりません。これらの検査が実施されたかご確認ください。実施されていた場合は結果をご報告ください。
        *   **クエリ文面（英語）:** Screening ECG (Exclusion [16b]), protocol-required ECGs (Visits 4, 5), and Ambulatory ECG (Visit 2) data/reports are missing. Please confirm if performed and provide results/report.
        *   **判断理由:** 安全性モニタリング計画の遵守状況と、参加者の心血管系の安全性を確認するため。
        *   **判断根拠:**
            *   関連するデータ: ECG, Ambulatory ECGデータなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [16b], Section 3.9.3.4.2 Cardiovascular Safety Measures, Protocol Attachment LZZT.1 Schedule of Events
    *   **クエリNo.:** Q-5 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 選択基準[5]に関連し、スクリーニング前1年以内のCNSイメージング (CTまたはMRI) が実施され、結果がアルツハイマー病と矛盾しないことが確認されたか、記録をご確認ください。
        *   **クエリ文面（英語）:** Regarding Inclusion Criterion [5], please confirm that CNS imaging (CT or MRI) compatible with AD was performed within 1 year prior to screening and reviewed.
        *   **判断理由:** 選択基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [5]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-5, P-6, D-6)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 除外基準[28b]および[29b]の確認のため、スクリーニング時に葉酸 (Folate) および梅毒 (Syphilis) の検査が実施されたかご確認ください。実施されていた場合は結果をご報告ください。
        *   **クエリ文面（英語）:** For Exclusion Criteria [28b] and [29b], please confirm if Folate and Syphilis screening tests were performed at screening and provide results if available.
        *   **判断理由:** 除外基準の遵守を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LBドメインに該当データなし
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b], [29b]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM/Medical Monitor
        *   **疑義事項/確認内容:** スクリーニング時 (Day -27) のビタミンB12値が基準値下限であったが、Day -2の再検査で正常化していることを確認。除外基準[28b]には最終的に抵触しなかったと判断。
        *   **判断理由:** 再検査で正常化しており、医療機関への問い合わせは不要と判断。内部記録として残す。
        *   **判断根拠:**
            *   関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Study Day of Specimen Collection(LB.LBDY)] = -27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 149.7734; [Study Day of Specimen Collection(LB.LBDY)] = -2, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 230.1936
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [28b]
    *   **確認事項No.:** I-2 (関連指摘No.: D-5, P-8)
        *   **重要度:** Critical
        *   **確認担当者:** Medical Monitor/DM
        *   **疑義事項/確認内容:** 主要評価項目 (ADAS-Cog, CIBIC+) および副次評価項目 (DAD, NPI-X) の最終評価データが、Lost to follow-upのため欠損していることを確認。有効性評価への影響が大きい。
        *   **判断理由:** 中止理由が明確であり、医療機関への問い合わせでデータが得られる可能性は低いため、内部確認とする。ただし、試験結果の解釈に重大な影響があるため重要度はCritical。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン最終評価欠損, [Standardized Disposition Term(DS.DSDECOD)] = 'LOST TO FOLLOW-UP'
            *   関連するプロトコル箇所: Section 2.1 Primary Objectives, Section 3.9.1.1 Efficacy Measures
    *   **確認事項No.:** I-3 (関連指摘No.: P-11)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** PK測定用採血のデータがないことを確認。Lost to follow-upのため、予定されていた採血の一部が未実施となった可能性が高い。
        *   **判断理由:** Lost to follow-upが理由と考えられるため、内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: PK関連データなし, [Standardized Disposition Term(DS.DSDECOD)] = 'LOST TO FOLLOW-UP'
            *   関連するプロトコル箇所: Section 3.9.2 Pharmacokinetics
    *   **確認事項No.:** I-4 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 既往歴として軽度の聴力低下 (Hypoacusis, Mild) が報告されている。除外基準[26] (Visual, hearing, or communication disabilities impairing the ability to participate) との関連を確認。SeverityがMildであり、教育歴 (EDLEVEL=6) もあることから、治験参加に支障はなかったと判断。
        *   **判断理由:** SeverityがMildであり、他の情報からも参加可能であったと推測されるため内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: [Dictionary-Derived Term(MH.MHDECOD)] = 'HYPOACUSIS', [Severity/Intensity(MH.MHSEV)] = 'MILD', [Subject Characteristic Short Name(SC.SCTESTCD)] = 'EDLEVEL', [Result or Finding in Original Units(SC.SCORRES)] = '6'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [26]
    *   **確認事項No.:** I-5
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** ベースラインから一貫して収縮期血圧が140-150 mmHg台とやや高めであるが、Placebo群であり、試験期間中に大きな変動は見られないことを確認。
        *   **判断理由:** 臨床的に大きな変動はなく、Placebo群であるため、現時点では積極的な介入やクエリは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (SYSBP, DIABP)
    *   **確認事項No.:** I-6
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 4の体重がベースラインから約2.7kg増加していることを確認。臨床的意義は不明。
        *   **判断理由:** 体重変動の理由は不明だが、他のデータとの関連や臨床的な問題を示唆する所見がないため、内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: VSドメイン (WEIGHT)

---

# 01-703-1258のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
78歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2006年発症）、高コレステロール血症、緑内障、高血圧、糖尿病、関節炎、めまい（SIGNIFICANT PRE-EXISTING CONDITION）、食道狭窄、膀胱脱、子宮摘出術、虫垂切除術（HISTORICAL DIAGNOSIS）が報告されている。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年07月10日|Day -10 (SCREENING 1)|ALT高値 (43 U/L, 基準範囲 6-32 U/L), AST高値 (36 U/L, 基準範囲 9-34 U/L), 好酸球高値 (0.59 GI/L, 基準範囲 0-0.57 GI/L), 尿比重高値 (1.032, 基準範囲 1.006-1.03)。立位時収縮期血圧高値 (1分後 164 mmHg, 3分後 160 mmHg)。MMSEスコア 13点。Hachinski Ischemic Scaleスコア 2点。|
|2012年07月20日|Day 1 (BASELINE)|治験薬 (Xanomeline 54 mg/day) 投与開始。ADAS-Cog(11) Total Score: 49点。NPI-X Total Score: 13点。|
|2012年07月31日|Day 12 (AMBUL ECG PLACEMENT)|単球高値 (1.07 GI/L, 基準範囲 0.12-0.92 GI/L)。|
|2012年08月01日|Day 13 (WEEK 2)|有害事象「めまい」(Severe) 発現 (治験薬との関連性: NONE)。ALT高値 (39 U/L)。|
|2012年08月02日|Day 14 (N/A)|治験薬用量を27 mg/dayに減量。|
|2012年08月11日|Day 23 (N/A)|有害事象「上気道感染」(Mild) 発現 (治験薬との関連性: NONE)。|
|2012年08月17日|Day 29 (WEEK 4)|ALT高値 (38 U/L)。|
|2012年08月19日|Day 31 (AMBUL ECG REMOVAL)|有害事象「上気道感染」(Mild) 回復。|
|2012年09月04日|Day 47 (WEEK 6)|有害事象「適用部位皮膚炎」(Mild) 発現 (治験薬との関連性: PROBABLE)。併用薬「HYDROCORTISONE」 (Topical) 開始。好酸球高値 (0.90 GI/L)。併用薬「NORVASC (AMLODIPINE)」中止。NPI-X Total Score: 6点。|
|2012年09月14日|Day 57 (WEEK 8)|有害事象「適用部位皮膚炎」がModerateに悪化。好酸球高値 (1.09 GI/L)。白血球高値 (10.8 GI/L, 基準範囲 3.8-10.7 GI/L)。ADAS-Cog(11) Total Score: 46点。CIBIC+: 5 (Minimal worsening)。NPI-X Total Score: 16点。|
|2012年10月01日|Day 74 (N/A)|有害事象「めまい」(Severe) 回復。|
|2012年10月02日|Day 75 (N/A)|有害事象「めまい」(Moderate, Serious - 入院) 発現 (治験薬との関連性: NONE)。|
|2012年10月09日|Day 82 (WEEK 12)|好酸球高値 (0.75 GI/L)。NPI-X Total Score: 14点。|
|2012年11月05日|Day 109 (WEEK 16)|好酸球高値 (0.70 GI/L)。ナトリウム高値 (146 mmol/L, 基準範囲 135-145 mmol/L)。収縮期血圧高値 (臥位 154 mmHg)。ADAS-Cog(11) Total Score: 41.0点。CIBIC+: 4 (No change)。NPI-X Total Score: 27点。|
|2012年11月19日|Day 123 (WEEK 18 (T))|併用薬「TIMOPTIC (UNCODED)」中止。NPI-X Total Score: 14点。|
|2012年12月31日|Day 165 (WEEK 24)|有害事象「めまい」(Moderate, Serious) 回復。ADAS-Cog(11) Total Score: 42.2点。CIBIC+: 5 (Minimal worsening)。NPI-X Total Score: 15点。Disposition: FINAL LAB VISIT (Other Event)。|
|2013年01月01日|Day 166 (N/A)|治験薬用量を54 mg/dayに再増量。|
|2013年01月11日|Day 176 (N/A)|治験薬投与終了。|
|2013年01月21日|Day 186 (WEEK 26)|体重減少確認 (ベースラインから約2.7kg減)。NPI-X Total Score: 30点。Disposition: ADVERSE EVENT (試験中止)。|
|2013年01月25日|Day 190 (N/A)|有害事象「適用部位皮膚炎」(Mild) 回復。|
|2013年01月28日|Day 191 (AE FOLLOW-UP)|AEフォローアップVisit実施。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象「めまい」が治験薬投与期間中に重篤な事象（入院）として再発しています。治験薬との関連性は"NONE"と評価されていますが、発現時期（Day 13, Day 75）と治験薬投与期間が重なること、および重篤度を考慮すると、治験薬との関連性を再評価する必要があると考えられます。特にDay 14の用量減量やDay 166の再増量との時間的な関連性も考慮すべきです。参加者の安全性に関わる重要な指摘です。
        *   **根拠:** 重篤な有害事象の評価の妥当性、治験薬投与との時間的関連性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'DIZZINESS'
            *   [Sequence Number(AE.AESEQ)] = 2, 5
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE', 'MODERATE'
            *   [Serious Event(AE.AESER)] = 'N', 'Y'
            *   [Requires or Prolongs Hospitalization(AE.AESHOSP)] = 'N', 'Y'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-08-01', '2012-10-02'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-10-01', '2012-12-31'
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2012-07-20', '2012-08-02', '2013-01-01'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2012-08-01', '2012-12-31', '2013-01-11'
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** スクリーニング時(Day -10)にALTおよびASTが高値（基準値上限超過）でした。治験薬投与開始後も高値が持続しましたが、その後正常化しています。ベースラインからの高値であり治験薬による明確な悪化とは言えませんが、肝機能異常は重要な安全性懸念です。プロトコルの除外基準[27b]（臨床検査値異常）に抵触する可能性があったか、組み入れ判断の妥当性を確認する必要があります。
        *   **根拠:** ベースライン時の臨床検査値異常、肝機能に関する安全性懸念、プロトコル除外基準との関連。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', 'AST'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -10, 12, 29, 47, 57, 82, 109, 137, 165
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = (ALT: 43, 39, 38, 24, 25, 21, 27, 19, 19), (AST: 36, 29, 33, 23, 25, 20, 27, 19, 18)
            *   [Reference Range Indicator(LB.LBNRIND)] = (ALT: HIGH, HIGH, HIGH, NORMAL...), (AST: HIGH, NORMAL...)
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = (ALT: 32 U/L), (AST: 34 U/L)
            *   プロトコル Section 3.4.2.2 [27b]
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** スクリーニング時(Day -10)から好酸球増多が認められ、治験薬投与中に一貫して高値が持続し、Day 57には基準値上限の約2倍まで悪化しました。その後正常化しています。AEとして報告された適用部位皮膚炎との関連も考えられますが、薬剤性過敏症の可能性も考慮すべきです。プロトコル 3.9.3.4 に記載されている Eosinophilia Follow-up 手順が適切に実施されたか確認が必要です。
        *   **根拠:** 臨床検査値の持続的な異常、潜在的なアレルギー反応/過敏症の可能性、プロトコル規定のモニタリング手順。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'EOS'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -10, 12, 29, 47, 57, 82, 109, 137, 165
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.59, 0.50, 0.51, 0.90, 1.09, 0.75, 0.70, 0.27, 0.36
            *   [Reference Range Indicator(LB.LBNRIND)] = HIGH, NORMAL, NORMAL, HIGH, HIGH, HIGH, HIGH, NORMAL, NORMAL
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 0.57 GI/L
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE DERMATITIS'
            *   プロトコル Section 3.9.3.4
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Day 57に一過性の白血球高値(10.8 GI/L)が認められました。直近の感染症(URTI)はDay 31に回復しており、他の炎症を示唆するデータもありません。臨床的な意義は低いと考えられますが、記録として残します。
        *   **根拠:** 一過性の臨床検査値異常。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'WBC'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 57
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 10.8
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 10.7 GI/L
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** Day 109に一過性の高ナトリウム血症(146 mmol/L)が認められました。脱水等の臨床所見は報告されていません。臨床的な意義は低いと考えられますが、記録として残します。
        *   **根拠:** 一過性の臨床検査値異常。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'SODIUM'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 109
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 146
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 145 mmol/L
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** ベースラインからWeek 26にかけて約2.7kgの体重減少が認められました。アルツハイマー病の進行や食欲変化、あるいは治験薬の影響の可能性も考えられますが、他の臨床情報からは明らかな原因は特定できません。臨床的な意義は現時点では低いと考えられますが、記録として残します。
        *   **根拠:** バイタルサインの経時的変化。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'WEIGHT'
            *   [Study Day of Vital Signs(VS.VSDY)] = 1, 186
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 59.42, 56.7
            *   [Standard Units(VS.VSSTRESU)] = 'kg'
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** 併用薬NORVASC (AMLODIPINE) がDay 47に中止されていますが、中止理由は不明です。プロトコル上は使用可能な薬剤です。高血圧の既往歴があるため、中止後の血圧管理について確認が必要となる可能性がありますが、VSデータ上は大きな変動は見られません。
        *   **根拠:** 併用薬の中止理由不明。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'NORVASC'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'AMLODIPINE'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2012-09-04'
            *   [Study Day of End of Medication(CM.CMENDY)] = 47
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** 併用薬TIMOPTIC (UNCODED) がDay 123に中止されていますが、中止理由は不明です。緑内障の既往歴があり、プロトコル上、β遮断薬点眼はcase-by-caseで許可される可能性があります。
        *   **根拠:** 併用薬の中止理由不明。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TIMOPTIC'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2012-11-19'
            *   [Study Day of End of Medication(CM.CMENDY)] = 123
    *   **指摘No.:** M-9
        *   **重要度:** Major
        *   **内容:** 有効性評価指標であるADAS-Cog(11)スコア、CIBIC+、NPI-X Total Scoreの経時的な変化に一貫性が見られません。ADAS-Cog(11)は改善傾向後にやや悪化、CIBIC+は悪化と変化なしが混在、NPI-Xは変動が大きく特に後半で悪化しています。これらの結果の乖離について、医学的な観点からの解釈が必要です。評価の信頼性に関わる可能性があります。
        *   **根拠:** 複数の有効性評価指標間の結果の不一致。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', 'CIBIC', 'NPTOT'
            *   [Visit Number(QS.VISITNUM)] = 3, 8, 10, 12 (ADAS-Cog, CIBIC+), 3, 4, 5, 7, 8, 8.1, 9, 9.1, 10, 10.1, 11, 11.1, 12, 13 (NPI-X)
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = (ACTOT: 49, 46, 41.0, 42.2), (CIBIC: 5, 4, 5), (NPTOT: 13, 13, 11, 6, 16, 14, 14, 15, 27, 14, 18, 20, 15, 30)
    *   **指摘No.:** M-10
        *   **重要度:** Major
        *   **内容:** 治験薬の用量がDay 14に減量され、Day 166に再増量されています。この用量変更が、有効性評価指標（特に変動の大きいNPI-Xスコア）の推移に影響を与えている可能性があります。用量変更の理由と有効性への影響について医学的な考察が必要です。
        *   **根拠:** 治験薬用量変更と有効性評価結果の変動との時間的関連性。
        *   **関連データ:**
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2012-07-20', '2012-08-02', '2013-01-01'
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2012-08-01', '2012-12-31', '2013-01-11'
            *   [Dose per Administration(EX.EXDOSE)] = 54, 27, 54
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT'
            *   [Visit Number(QS.VISITNUM)] = 3, 4, 5, 7, 8, 8.1, 9, 9.1, 10, 10.1, 11, 11.1, 12, 13
            *   [Numeric Finding in Standard Units(QS.QSSTRESN)] = 13, 13, 11, 6, 16, 14, 14, 15, 27, 14, 18, 20, 15, 30

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** DSドメインの中止理由が"ADVERSE EVENT"と一般的です。RELRECデータから中止理由がAE「適用部位皮膚炎」 (RELID="01-703-1258-E08") に関連付けられていることが示唆されますが、AE「めまい」も重篤であり、中止理由の特定にはより詳細な情報が望ましいです。ただし、主要な評価への影響は限定的と考えられます。
        *   **根拠:** DSレコードとAE/RELRECレコード間の関連性、中止理由の具体性。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 186
            *   [Relationship Identifier(RELREC.RELID)] = '01-703-1258-E08'
            *   [Related Domain Abbreviation(RELREC.RDOMAIN)] = 'AE', 'DS'
            *   [Identifying Variable(RELREC.IDVAR)] = 'AESEQ', 'DSSEQ'
            *   [Identifying Variable Value(RELREC.IDVARVAL)] = '   4', '   6', '   7', '   1'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE DERMATITIS' (for AESEQ=4, 6, 7)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、同一イベント（適用部位皮膚炎）と思われる記録が複数行 (AESEQ=4, 6, 7) に分かれ、開始日・終了日は同じで重症度のみが異なって記録されています。イベントの経過を示す意図かもしれませんが、SDTM標準の記録方法として適切か確認が必要です。データの解釈に混乱を招く可能性がありますが、RELRECで関連付けられているため、大きな問題にはならないと考えられます。
        *   **根拠:** ドメイン内データの一貫性、SDTM記録方法の標準。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'APPLICATION SITE DERMATITIS'
            *   [Sequence Number(AE.AESEQ)] = 4, 6, 7
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-09-04' (all)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-01-25' (all)
            *   [Severity/Intensity(AE.AESEV)] = 'MILD', 'MODERATE', 'MILD'
    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、同一イベント（上気道感染）と思われる記録が複数行 (AESEQ=1, 3) に分かれ、開始日・終了日は同じで収集日(AEDTC)のみが異なって記録されています。これもイベントの経過を示す意図かもしれませんが、記録方法の適切性を確認する必要があります。
        *   **根拠:** ドメイン内データの一貫性。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'UPPER RESPIRATORY TRACT INFECTION'
            *   [Sequence Number(AE.AESEQ)] = 1, 3
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-08-11' (both)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-08-19' (both)
            *   [Date/Time of Collection(AE.AEDTC)] = '2012-08-17', '2012-09-04'
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** CMドメインの薬剤「TIMOPTIC」について、標準化された薬剤名 (CMDECOD) が"UNCODED"となっています。薬剤辞書を用いた標準化が必要です。データ品質の問題ですが、直接的な安全性・有効性評価への影響は小さいです。
        *   **根拠:** データ標準化の必要性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'TIMOPTIC'
            *   [Standardized Medication Name(CM.CMDECOD)] = 'UNCODED'
    *   **指摘No.:** D-5
        *   **重要度:** Major
        *   **内容:** DMドメインの同意取得日時 (RFICDTC) が欠損しています。同意取得は治験実施の基本であり、治験手順開始前に適切に行われたかを確認するために必須の情報です。参加者の権利保護に関わる重要な欠損です。
        *   **根拠:** 必須情報の欠損、GCP遵守。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** CMドメインにおいて、一部薬剤 (ALEVE, HYDROCORTISONE, NORVASC) の適応 (CMINDC) が欠損しています。薬剤使用理由の明確化のためには情報があった方が望ましいですが、安全性・有効性評価への直接的な影響は限定的です。
        *   **根拠:** データの完全性。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'ALEVE', 'HYDROCORTISONE', 'NORVASC'
            *   [Indication(CM.CMINDC)] = '' (欠損)
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** AEドメインにおいて、MedDRAコーディングに関連する変数 (AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCD) が欠損しています。有害事象の集計・評価のためにコーディングは必要ですが、現時点でのレビューへの影響は限定的です。コーディング作業の進捗確認が必要です。
        *   **根拠:** データ標準化・完全性。
        *   **関連データ:**
            *   AEドメインの各種MedDRAコード変数

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日時 (DM.RFICDTC) が欠損しており、治験手順開始前に適切な同意取得が行われたか確認できません。GCPの基本要件であり、参加者の権利保護の観点から重大な逸脱の可能性があります。
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent)
        *   **根拠:** GCP要件、参加者の権利保護。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2012-07-20'
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 糖尿病の既往歴があるにも関わらず、除外基準[30b]の確認に必要なHbA1cのデータがありません。プロトコルではIDDM患者またはScreening時の血糖値>200の場合に測定が必要とされていますが、血糖値データもScreening時のみです。スクリーニング手順が完全に遵守されていなかった可能性がありますが、他のデータから明らかな基準逸脱は示唆されていません。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [19], [30b]
        *   **根拠:** 除外基準確認に必要な検査の未実施の可能性。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'DIABETES'
            *   LBドメインにHBA1Cのデータなし
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** スクリーニング時の臨床検査値 (ALT, AST, EOS, SPGRAV) が基準値範囲外でした。除外基準[27b]では、臨床的に意義がないと判断されれば組み入れ可能とされていますが、その判断根拠が不明です。特に肝酵素高値は安全性に関わるため、組み入れが適切であったか確認が必要です。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** 除外基準に抵触する可能性のある検査値異常。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', 'AST', 'EOS', 'SPGRAV'
            *   [Study Day of Specimen Collection(LB.LBDY)] = -10
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** Day 14に治験薬用量が54mgから27mgに減量されていますが、プロトコルには用量減量の基準や手順に関する記載が見当たりません（Section 3.6 Dosage and Administration には記載なし）。減量の理由とプロトコル上の根拠が不明であり、計画外の用量変更（逸脱）の可能性があります。有効性・安全性評価への影響も懸念されます。
        *   **プロトコル該当箇所:** Section 3.6 (Dosage and Administration) - 減量基準の記載なし
        *   **根拠:** プロトコルに規定されていない用量変更。
        *   **関連データ:**
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2012-08-02'
            *   [Dose per Administration(EX.EXDOSE)] = 27
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** Day 166に治験薬用量が27mgから54mgに再増量されていますが、プロトコルには用量再増量の基準や手順に関する記載が見当たりません。これも計画外の用量変更（逸脱）の可能性があります。
        *   **プロトコル該当箇所:** Section 3.6 (Dosage and Administration) - 再増量基準の記載なし
        *   **根拠:** プロトコルに規定されていない用量変更。
        *   **関連データ:**
            *   [Start Date/Time of Treatment(EX.EXSTDTC)] = '2013-01-01'
            *   [Dose per Administration(EX.EXDOSE)] = 54
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルではVisit 13で化学・血液検査が規定されていますが、LBデータが存在しません。評価スケジュールの逸脱の可能性がありますが、最終Visit付近であり主要評価への影響は限定的と考えられます。
        *   **プロトコル該当箇所:** Section 3.9.3.3, Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 規定された検査の未実施。
        *   **関連データ:**
            *   LBドメインにVisit 13のデータなし
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルではVisit 4で尿検査が規定されていますが、LBデータが存在しません。評価スケジュールの逸脱の可能性がありますが、影響は限定的と考えられます。
        *   **プロトコル該当箇所:** Section 3.9.3.3, Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** 規定された検査の未実施。
        *   **関連データ:**
            *   LBドメインにVisit 4のUrinalysisデータなし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「めまい」について、Day 75に発現した事象が重篤（入院）と報告され、治験薬との関連性は「NONE」と評価されています。しかし、治験薬投与中に発現・回復を繰り返しており、重篤な事象であるため、治験薬との関連性について再評価をお願いできますでしょうか。特にDay 14の用量減量やDay 166の再増量との時間的関連性も踏まえてご検討ください。
        *   **クエリ文面（英語）:** Regarding the AE 'DIZZINESS', the event starting on Day 75 was reported as Serious (Required Hospitalization) with causality assessed as 'NONE'. Given the recurrence during study drug administration and its seriousness, please reassess the relationship to the study drug, considering the dose reduction on Day 14 and re-escalation on Day 166.
        *   **判断理由:** 重篤な有害事象であり、治験薬との関連性の評価は参加者の安全性確保に不可欠なため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='DIZZINESS', AE.AESER='Y', AE.AEREL='NONE', AE.AESTDTC='2012-10-02', EX.EXDOSE=27 (at event onset)
            *   関連するプロトコル箇所: Section 3.9.3.2.2 (Serious Adverse Events)
            *   関連する医学的知見: めまいは薬剤の副作用として一般的であり、用量変更との関連も考慮すべき。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時(Day -10)のアラニンアミノトランスフェラーゼが「43 U/L」、アスパラギン酸アミノトランスフェラーゼが「36 U/L」と基準値上限を超えていました。除外基準[27b]では臨床的に意義がないと判断されれば組み入れ可能とされていますが、組み入れを可能とした医学的判断根拠について記録をご確認の上、お知らせください。
        *   **クエリ文面（英語）:** At Screening (Day -10), ALT was '43 U/L' and AST was '36 U/L', exceeding the upper reference limits. Exclusion criterion [27b] allows inclusion if clinically non-significant. Please confirm the medical rationale for determining these values as not clinically significant, allowing enrollment.
        *   **判断理由:** 除外基準に抵触する可能性のある検査値異常があり、組み入れの妥当性を確認する必要があるため。参加者の安全性に関わる。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='ALT', 'AST', LB.LBDY=-10, LB.LBSTRESN=43, 36, LB.LBNRIND='HIGH'
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]
            *   関連する医学的知見: ベースラインの肝酵素高値は、治験薬による肝障害リスク評価において重要。
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** スクリーニング時から好酸球数が高値であり、治験期間中にさらに上昇しています（最大Day 57で1.09 GI/L）。プロトコル3.9.3.4に記載の好酸球増多に対するフォローアップ手順（定期的な血液検査等）は適切に実施されましたでしょうか。また、この好酸球増多の臨床的な意義について評価をお願いします。
        *   **クエリ文面（英語）:** Eosinophil counts were elevated from Screening (Day -10) and increased during the study (peak 1.09 GI/L on Day 57). Were the follow-up procedures for eosinophilia described in protocol section 3.9.3.4 (e.g., repeat hematology) performed appropriately? Please assess the clinical significance of this eosinophilia.
        *   **判断理由:** 持続的かつ悪化傾向を示した検査値異常であり、潜在的な過敏症リスクとプロトコル遵守の観点から確認が必要なため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='EOS', LB.LBDY=-10, 47, 57, 82, 109, LB.LBSTRESN=0.59, 0.90, 1.09, 0.75, 0.70, LB.LBNRIND='HIGH'
            *   関連するプロトコル箇所: Section 3.9.3.4
            *   関連する医学的知見: 好酸球増多はアレルギー反応や薬剤過敏症を示唆することがある。
    *   **クエリNo.:** Q-4 (関連指摘No.: D-5, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日時が記録されていません。記録をご確認いただき、同意取得日時をお知らせください。また、治験手順開始前に適切に同意が取得されていたことをご確認ください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent is missing. Please check records and provide the date/time of consent. Also, confirm that consent was obtained prior to initiation of any study procedures.
        *   **判断理由:** 同意取得はGCPの基本要件であり、参加者の権利保護を確認するために必須の情報であるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC='' (欠損)
            *   関連するプロトコル箇所: Section 5.1
    *   **クエリNo.:** Q-5 (関連指摘No.: P-4, P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 治験薬の用量がDay 14に54mgから27mgに減量され、Day 166に54mgに再増量されています。プロトコルには用量変更に関する規定が見当たりませんでしたが、これらの用量変更の理由について詳細をお知らせください。
        *   **クエリ文面（英語）:** The study drug dose was reduced from 54mg to 27mg on Day 14, and re-escalated to 54mg on Day 166. The protocol does not specify dose modification criteria. Please provide the reason(s) for these dose changes.
        *   **判断理由:** プロトコルに規定されていない用量変更が行われており、その理由と妥当性を確認する必要があるため。安全性・有効性評価に影響する可能性がある。
        *   **判断根拠:**
            *   関連するデータ: EX.EXDOSE, EX.EXSTDTC, EX.EXENDTC
            *   関連するプロトコル箇所: Section 3.6 (用量変更基準の記載なし)

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-9, M-10)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 有効性評価指標 (ADAS-Cog(11), CIBIC+, NPI-X Total Score) の結果に一貫性が見られず、特にNPI-Xスコアの変動が大きい。治験薬の用量変更（Day 14減量、Day 166再増量）との関連性も含め、医学的に評価し、本症例における有効性評価結果の解釈について内部で議論する。
        *   **判断理由:** 有効性評価の解釈に影響する可能性のある結果の不一致であり、内部での医学的評価と議論が必要なため。
        *   **判断根拠:**
            *   関連するデータ: QSドメイン (ACTOT, CIBIC, NPTOT), EXドメイン (用量変更履歴)
            *   関連するプロトコル箇所: Section 2 (Objectives), Section 4.3 (Efficacy Analyses)
    *   **確認事項No.:** I-2 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 試験中止理由がDSドメインで"ADVERSE EVENT"と記録されている。RELRECデータからは皮膚炎が主因と推測されるが、特定には至らない。データクリーニングプロセスにおいて、可能であればより具体的な中止理由を他の情報源（例：Source Document）から確認し、内部記録として残すことを検討する。
        *   **判断理由:** 中止理由の具体性はデータ品質向上の観点から望ましいが、主要評価への影響は限定的であり、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD, DS.DSSTDY, RELRECデータ, AEデータ
    *   **確認事項No.:** I-3 (関連指摘No.: D-2, D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインで、同一イベントと思われる記録が複数行に分かれて記録されている（AESEQ=4,6,7 および AESEQ=1,3）。SDTM IGのガイダンスに基づき、このような記録方法が適切か、あるいはデータ入力/マッピングの問題がないか内部で確認する。データの解釈に大きな支障はないため、緊急性は低い。
        *   **判断理由:** データ構造に関する軽微な疑義であり、内部での確認・標準化検討事項と判断。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン (AESEQ, AETERM, AESTDTC, AEENDTC, AESEV, AEDTC)
    *   **確認事項No.:** I-4 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CM「TIMOPTIC」が標準化されていない (CMDECOD=UNCODED)。データ標準化プロセスの一環として、薬剤辞書を用いて標準化を行う。
        *   **判断理由:** データ品質に関する問題であり、標準的なデータマネジメントプロセスで対応可能。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='TIMOPTIC', CM.CMDECOD='UNCODED'
    *   **確認事項No.:** I-5 (関連指摘No.: M-4, M-5, M-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 一過性のWBC高値 (Day 57)、高ナトリウム血症 (Day 109)、および緩やかな体重減少 (全体) が認められた。他の臨床情報と併せて評価した結果、現時点では臨床的に重大な意義を持つとは考えにくいため、医療機関への問い合わせは不要と判断。内部記録として残す。
        *   **判断理由:** 臨床的な影響が小さいと考えられる一過性の検査値変動および緩やかな体重変化のため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='WBC', 'SODIUM', VS.VSTESTCD='WEIGHT' および関連する臨床データ
    *   **確認事項No.:** I-6 (関連指摘No.: M-7, M-8, D-6)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 併用薬NORVASCおよびTIMOPTICの中止理由、および一部併用薬のIndicationが欠損している。情報の完全性の観点からは望ましくないが、これらの欠損が本試験の主要な安全性・有効性評価に与える影響は限定的と考えられるため、医療機関への問い合わせは必須ではないと判断。可能であれば他のクエリと併せて確認するか、内部で情報を補完する。
        *   **判断理由:** 主要評価への影響が小さいと考えられる情報の欠損のため。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン (CMTRT, CMDECOD, CMINDC, CMENDTC)
    *   **確認事項No.:** I-7 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 糖尿病の既往がある被験者について、除外基準[30b]の確認に必要なHbA1cデータが欠損している。スクリーニング手順の遵守状況について内部で確認する。他のデータから明らかな基準逸脱は示唆されていないため、重要度はMinorとする。
        *   **判断理由:** プロトコル遵守に関する疑義だが、現時点で重大な影響は確認されていないため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM='DIABETES', LBドメイン (HBA1Cデータなし)
            *   関連するプロトコル箇所: Section 3.4.2.2 [30b]
    *   **確認事項No.:** I-8 (関連指摘No.: P-6, P-7)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 13の化学・血液検査データ、Visit 4の尿検査データが欠損している。プロトコルで規定された評価スケジュールの逸脱であるが、試験の主要評価項目への影響は限定的と考えられるため、内部確認事項とする。
        *   **判断理由:** 評価スケジュールの逸脱だが、主要評価への影響が小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン (Visit 13 Chem/Hemat, Visit 4 Urinalysis データなし)
            *   関連するプロトコル箇所: Attachment LZZT.1 (Schedule of Events)
    *   **確認事項No.:** I-9 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインのMedDRAコーディング関連変数が欠損している。データ標準化プロセスの一環として、コーディング作業の進捗を確認し、完了させる必要がある。
        *   **判断理由:** データ標準化に関する内部作業事項のため。
        *   **判断根拠:**
            *   関連するデータ: AEドメインのMedDRAコード変数

---

# 01-703-1279のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    72歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった。主要な既往歴として、アルツハイマー病（PRIMARY DIAGNOSIS、2010年7月29日発症）、統合失調症様障害（SIGNIFICANT PRE-EXISTING CONDITION、重症度: MILD、発症日不明）が報告されている。教育レベルは12年であった。Intent to Treat Population FlagおよびSafety Population FlagはYであった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年04月27日|Day -16 (SCREENING 1)|MMSEスコア 14点、Hachinski Ischemic Score 0点。臨床検査にてヘマトクリット(HCT) 51.0 % (HIGH)、ヘモグロビン(HGB) 15.9 g/dL (HIGH) を認めた（臨床的意義は不明）。身長 162.56 cm、体重 56.25 kg。|
|2013年05月11日|Day -2 (SCREENING 2)|バイタルサイン測定。特記すべき異常なし。|
|2013年05月13日|Day 1 (BASELINE)|治験薬Xanomeline 54 mg (PATCH, QD, TRANSDERMAL) 投与開始。体重 55.79 kg。ADAS-Cog(11) Subscore 28点。NPI-X (9) Total Score 24点。DAD評価実施。|
|2013年06月03日|Day 22 (N/A)|治験薬投与終了（EX.EXENDTC）。|
|2013年06月22日|Day 41 (WEEK 2)|治験中止（理由: CAREGIVER BECAME ILL）。体重 54.89 kg（ベースラインから約0.9kg減少）。バイタルサイン測定（立位3分後の血圧・脈拍は未測定）。NPI-X (9) Total Score 43点（ベースラインから19点悪化、特にDelusions, Agitation/Aggression, Anxiety, Irritability/Lability, Aberrant Motor Behaviorのスコアが増加または出現）。DAD評価実施（一部項目でベースラインから悪化）。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** Day 41 (Week 2) におけるNPI-Xスコアの著しい悪化（ベースライン24点から43点へ増加）が認められる。特に妄想、興奮/攻撃性、不安、易刺激性/感情不安定、異常な運動行動の項目が悪化または新たに出現している。これは治験薬の副作用（精神症状の悪化）または原疾患（アルツハイマー病）の進行の可能性があるが、AEドメインには関連する有害事象の報告がない。参加者の安全性評価の観点から、このNPI-Xの悪化が有害事象に該当しないか、治験薬との関連性を含めて評価が必要である。
        *   **根拠:** NPI-Xスコアの急激な悪化は臨床的に重要であり、安全性評価に影響を与える可能性がある。Xanomelineはコリン作動薬であり、精神症状への影響は既知のリスクとして考慮すべきである。AEとして報告されていない点について確認が必要。
        *   **関連データ:**
            *   [NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 24, [Baseline Flag(QS.QSBLFL)] = 'Y'
            *   [NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 4, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 43
            *   [AEドメイン]: レコードなし
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 患者は統合失調症様障害（Schizophreniform disorder）の既往歴（重症度: MILD）を有する。NPI-Xの悪化とこの既往歴との関連性が考えられるが、既往歴の発症時期が不明なため、治験参加中の悪化との時間的な関連は不明確である。
        *   **根拠:** 精神疾患の既往は、治験薬による精神症状悪化のリスク因子となる可能性がある。ただし、AE報告がなく、NPI-X悪化の原因が既往歴の再燃か治験薬の影響か、あるいは原疾患の進行かはデータからは断定できない。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'SCHIZOPHRENIFORM DISORDERS'
            *   [Severity/Intensity(MH.MHSEV)] = 'MILD'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '' (欠損)
            *   [NPI-X (9) Total Score(QS.QSTESTCD)] = 'NPTOT', [Visit Number(QS.VISITNUM)] = 4, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 43

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** Day 41 (Visit 4, WEEK 2) のバイタルサイン測定において、立位3分後の血圧および脈拍データが欠損している（VSSTAT = 'NOT DONE'）。プロトコルで規定された測定手順が完了していない可能性があり、起立性低血圧等の評価が不十分となる可能性がある。
        *   **根拠:** 重要な安全性評価項目の一部が欠損している。ただし、立位1分後のデータは存在し、中止Visitでもあるため、評価への影響は限定的かもしれない。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'DIABP', [Visit Number(VS.VISITNUM)] = 4, [Planned Time Point Number(VS.VSTPTNUM)] = 817, [Character Result/Finding in Std Format(VS.VSSTRESC)] = '', [Completion Status(VS.VSSTAT)] = 'NOT DONE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE', [Visit Number(VS.VISITNUM)] = 4, [Planned Time Point Number(VS.VSTPTNUM)] = 817, [Character Result/Finding in Std Format(VS.VSSTRESC)] = '', [Completion Status(VS.VSSTAT)] = 'NOT DONE'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'SYSBP', [Visit Number(VS.VISITNUM)] = 4, [Planned Time Point Number(VS.VSTPTNUM)] = 817, [Character Result/Finding in Std Format(VS.VSSTRESC)] = '', [Completion Status(VS.VSSTAT)] = 'NOT DONE'
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 既往歴（MH）において、統合失調症様障害（Schizophreniform disorder）の開始日（MHSTDTC）が欠損している。除外基準[14]a（精神疾患既往歴が5年以内）への該当性を正確に判断するために開始日の情報が必要となる。
        *   **根拠:** 除外基準適合性の確認に必要な情報が欠損している。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'SCHIZOPHRENIFORM DISORDERS'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '' (欠損)
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 同意取得日（DM.RFICDTC）が欠損している。同意取得が治験手順開始前に行われたか確認できず、参加者の権利保護の観点から問題となる可能性がある。
        *   **根拠:** GCPの基本要件である同意取得の記録が不十分。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 治験薬投与終了日（EX.EXENDTC: Day 22）と治験中止日（DS.DSSTDTC: Day 41）の間に約3週間の期間がある。この期間の治験薬投与状況（中断など）が不明確である。
        *   **根拠:** 曝露期間の正確な把握と中止理由との関連性を理解するために確認が必要。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-06-03' (Day 22)
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-06-22' (Day 41)
            *   [Reported Term for the Disposition Event(DS.DSTERM)] = 'CAREGIVER BECAME ILL'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[14]a「A history within the last 5 years of the following: a) Schizophrenia」に違反している可能性がある。MHドメインに統合失調症様障害（Schizophreniform disorder）の既往歴が記録されているが、開始日が不明なため5年以内の発症か判断できない。Schizophreniform disorderが除外基準のSchizophreniaに該当するか、また発症時期について確認が必要。参加者の安全性リスク（精神症状悪化）やデータの解釈に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [14]a
        *   **根拠:** 除外基準に抵触する可能性のある既往歴が記録されており、かつ開始日が不明。
        *   **関連データ:**
            *   [Reported Term for the Medical History(MH.MHTERM)] = 'SCHIZOPHRENIFORM DISORDERS'
            *   [Start Date/Time of Medical History Event(MH.MHSTDTC)] = '' (欠損)
    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[5]「CNS imaging (CT scan or MRI of brain) compatible with AD within past 1 year」を満たしているか確認するためのデータ（検査実施日や結果を示す記録）が提供されていない。適格性確認が不十分な可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5], Section 3.4.2.2 Exclusion Criteria [5] (関連)
        *   **根拠:** 適格性確認に必要な情報が欠損している。
        *   **関連データ:** なし (関連データ欠損)
    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[16b]「Evidence from ECG recording at screening of any listed condition」を満たしているか確認するためのスクリーニング時のECGデータが提供されていない。適格性確認が不十分な可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [16b]
        *   **根拠:** 適格性確認に必要な情報が欠損している。
        *   **関連データ:** なし (ECGデータ欠損)
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[29b]「Positive syphilis screening」に該当しないか確認するための梅毒スクリーニング検査データが提供されていない。適格性確認が不十分な可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [29b]
        *   **根拠:** 適格性確認に必要な情報が欠損している。
        *   **関連データ:** なし (関連検査データ欠損)
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[31b]およびプロトコル3.8で規定されている併用禁止・制限薬を使用していなかったか確認するための併用薬（CM）データが提供されていない。プロトコル違反や、安全性・有効性評価への影響の可能性が否定できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b], Section 3.8 Concomitant Therapy
        *   **根拠:** 併用薬に関する情報が欠損しており、プロトコル遵守を確認できない。
        *   **関連データ:** なし (CMドメインレコードなし)
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 4 (WEEK 2) の実施日 (Day 41) が、計画日 (Planned Day 14) から大幅に遅延している。ただし、このVisitは治験中止Visitでもあるため、スケジュールからの逸脱はやむを得なかった可能性がある。評価の信頼性への影響は限定的と考えられる。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design, Protocol Attachment LZZT.1 Schedule of Events
        *   **根拠:** 実際のVisit日と計画日の乖離。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 4, [Visit Name(SV.VISIT)] = 'WEEK 2', [Planned Study Day of Visit(SV.VISITDY)] = 14, [Start Date/Time of Visit(SV.SVSTDTC)] = '2013-06-22' (Day 41)
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'WITHDRAWAL BY SUBJECT', [Visit Number(DS.VISITNUM)] = 4, [Study Day of Start of Disposition Event(DS.DSSTDY)] = 41
    *   **指摘No.:** P-7
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 4 (Day 41) において、プロトコル 3.9.3.4.1 で規定されている立位3分後のバイタルサイン測定が実施されていない（VSSTAT = 'NOT DONE'）。安全性評価手順の逸脱。
        *   **プロトコル該当箇所:** Section 3.9.3.4.1 Vital Sign Determination
        *   **根拠:** VSデータで未測定が記録されている。
        *   **関連データ:** (D-1と同じ)
    *   **指摘No.:** P-8
        *   **重要度:** Minor
        *   **逸脱の可能性:** NPI-X評価が、プロトコル 3.9.1.1 で規定されている2週間隔で実施されていない（Day 1とDay 41のみ）。ただし、Day 41は中止Visitであるため、最終評価として実施された可能性があり、評価スケジュールからの逸脱の影響は限定的かもしれない。
        *   **プロトコル該当箇所:** Section 3.9.1.1 Efficacy Measures
        *   **根拠:** QSデータの評価日間隔が2週間ではない。
        *   **関連データ:**
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', [Visit Number(QS.VISITNUM)] = 3, [Study Day of Finding(QS.QSDY)] = 1
            *   [Category of Question(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', [Visit Number(QS.VISITNUM)] = 4, [Study Day of Finding(QS.QSDY)] = 41
    *   **指摘No.:** P-9
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルスケジュール (Attachment LZZT.1) ではVisit 4 (WEEK 2) で臨床検査（化学・血液・尿）が予定されているが、対応するLBデータが提供されていない。安全性モニタリングに必要な検査が実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 Schedule of Events, Section 3.9.3.3 Clinical Laboratory Tests
        *   **根拠:** 予定されていたVisitでのLBデータが存在しない。
        *   **関連データ:** なし (Visit 4に対応するLBデータ欠損)
    *   **指摘No.:** P-10
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルスケジュール (Attachment LZZT.1) および Section 3.9.3.4.2, 3.9.4 ではVisit 1, 2 (Ambulatory), 3, 4 でECG測定が予定されているが、ECGデータが提供されていない。心血管系の安全性モニタリングが計画通り実施されなかった可能性がある。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 Schedule of Events, Section 3.9.3.4.2 Cardiovascular Safety Measures, Section 3.9.4 Safety Monitoring
        *   **根拠:** 予定されていたVisitでのECGデータが存在しない。
        *   **関連データ:** なし (ECGデータ欠損)
    *   **指摘No.:** P-11
        *   **重要度:** Critical
        *   **逸脱の可能性:** 同意取得日（DM.RFICDTC）が欠損しており、プロトコル 5.1 およびGCPで要求される「治験手順開始前の同意取得」が確認できない。参加者の権利保護に関する重大な逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** 同意日の記録が欠損している。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
    *   **指摘No.:** P-12
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[27b]に関連し、スクリーニング時(Day -16)のヘマトクリット(HCT)およびヘモグロビン(HGB)が基準値上限を超えている。プロトコルでは臨床的に意義がないと判断されれば組み入れ可能とされているが、その判断記録が確認できない。適格性評価プロセスが適切であったか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** 基準値逸脱の検査値があり、適格性判断の記録が不明。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HCT', [Study Day of Specimen Collection(LB.LBDY)] = -16, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 0.51, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'HGB', [Study Day of Specimen Collection(LB.LBDY)] = -16, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 9.86754, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、Study Day 41 (Visit 4) のNPI-X合計スコアが「43」点と、ベースラインの「24」点から著しく悪化しています。特に妄想、興奮/攻撃性、不安、易刺激性/感情不安定、異常な運動行動の項目が悪化または出現していますが、有害事象としての報告がありません。このNPI-Xの悪化について、臨床的な評価（有害事象該当性の判断、重症度、治験薬との関連性評価を含む）をお知らせください。参加者の安全性評価のために確認が必要です。
        *   **クエリ文面（英語）:** Regarding patient 01-703-1279, the NPI-X Total Score on Study Day 41 (Visit 4) was '43', a significant worsening from the baseline score of '24'. Worsening/new onset was noted particularly for Delusions, Agitation/Aggression, Anxiety, Irritability/Lability, and Aberrant Motor Behavior, but no corresponding AE was reported. Please provide clinical assessment of this NPI-X worsening (incl. AE determination, severity, relationship to study drug). This is needed for safety assessment.
        *   **判断理由:** NPI-Xの著しい悪化がAEとして評価・報告されているか確認し、参加者の安全性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: QS.QSTESTCD='NPTOT', QS.VISITNUM=3, QS.QSSTRESN=24; QS.QSTESTCD='NPTOT', QS.VISITNUM=4, QS.QSSTRESN=43; AEドメインレコードなし
            *   関連するプロトコル箇所: Section 3.9.3.2 Adverse Events, Section 3.9.1.1 NPI-X
            *   関連する医学的知見: Xanomelineの精神症状への影響の可能性。
    *   **クエリNo.:** Q-2 (関連指摘No.: D-1, P-7)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、Study Day 41 (Visit 4) のバイタルサイン測定で、立位3分後の血圧および脈拍が「未測定」 (NOT DONE) と記録されています。測定されなかった理由をお知らせください。プロトコルで規定された手順の遵守確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, on Study Day 41 (Visit 4), vital signs (BP and pulse) after standing for 3 minutes were recorded as 'NOT DONE'. Please provide the reason why these measurements were not performed. This is to confirm adherence to protocol procedures.
        *   **判断理由:** プロトコルで規定された測定の欠損理由を確認し、データ品質を確保するため。
        *   **判断根拠:**
            *   関連するデータ: VS.VISITNUM=4, VS.VSTPTNUM=817, VS.VSSTAT='NOT DONE'
            *   関連するプロトコル箇所: Section 3.9.3.4.1 Vital Sign Determination
    *   **クエリNo.:** Q-3 (関連指摘No.: D-2, P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、既往歴として報告されている「統合失調症様障害」 (SCHIZOPHRENIFORM DISORDERS) の発症日（開始日）が記録されていません。除外基準[14]a（精神疾患の既往歴が5年以内）への該当性を確認するため、発症日をお知らせください。適格性確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, the start date for the reported medical history 'SCHIZOPHRENIFORM DISORDERS' is missing. Please provide the onset date to confirm eligibility regarding exclusion criterion [14]a (history of mental illness within 5 years). This is required for eligibility verification.
        *   **判断理由:** 除外基準違反の可能性を確認し、参加者の適格性を担保するため。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM='SCHIZOPHRENIFORM DISORDERS', MH.MHSTDTC='' (欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [14]a
    *   **クエリNo.:** Q-4 (関連指摘No.: D-3, P-11)
        *   **重要度:** Critical
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、インフォームド・コンセント取得日（Date/Time of Informed Consent）が記録されていません。同意取得日および同意取得が治験手順開始前に行われたことを確認させてください。参加者の権利保護とGCP遵守の確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, the Date/Time of Informed Consent is missing. Please confirm the date of consent and that consent was obtained prior to any study procedures. This is critical for participant rights protection and GCP compliance.
        *   **判断理由:** 同意取得の記録はGCPの必須要件であり、参加者の権利保護の根幹に関わるため。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC='' (欠損)
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
    *   **クエリNo.:** Q-5 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、治験薬投与終了日（End Date/Time of Treatment）がStudy Day 22、治験中止日（Start Date/Time of Disposition Event）がStudy Day 41と記録されています。Study Day 23からDay 41までの間の状況（治験薬の投与中断など）について確認させてください。
        *   **クエリ文面（英語）:** For patient 01-703-1279, the End Date/Time of Treatment is recorded as Study Day 22, and the Start Date/Time of Disposition Event is Study Day 41. Please clarify the patient's status (e.g., study drug interruption) between Study Day 23 and Day 41.
        *   **判断理由:** 曝露期間と中止理由との関連性を明確にするため。
        *   **判断根拠:**
            *   関連するデータ: EX.EXENDTC='2013-06-03' (Day 22), DS.DSSTDTC='2013-06-22' (Day 41)
    *   **クエリNo.:** Q-6 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、除外基準[5]に関連し、過去1年以内のCNS画像検査（CTまたはMRI）がアルツハイマー病と矛盾しないことを確認した記録（検査日、結果概要など）をご提示ください。適格性確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, regarding exclusion criterion [5], please provide documentation (e.g., test date, result summary) confirming that CNS imaging (CT or MRI) within the past year was compatible with AD. This is required for eligibility verification.
        *   **判断理由:** 適格性確認に必要な情報が不足しているため。
        *   **判断根拠:**
            *   関連するデータ: なし
            *   関連するプロトコル箇所: Section 3.4.2.1 Inclusion Criteria [5]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、除外基準[16b]に関連し、スクリーニング時のECG検査で除外基準に該当する所見がなかったことを確認させてください。適格性確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, regarding exclusion criterion [16b], please confirm that the screening ECG showed no findings listed in the exclusion criteria. This is required for eligibility verification.
        *   **判断理由:** 適格性確認に必要な情報が不足しているため。
        *   **判断根拠:**
            *   関連するデータ: なし (ECGデータ欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [16b]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、除外基準[29b]に関連し、梅毒スクリーニング検査が陰性であったことを確認させてください。適格性確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, regarding exclusion criterion [29b], please confirm that the syphilis screening test was negative. This is required for eligibility verification.
        *   **判断理由:** 適格性確認に必要な情報が不足しているため。
        *   **判断根拠:**
            *   関連するデータ: なし (関連検査データ欠損)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [29b]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、併用薬（CM）のデータが報告されていません。治験期間中に併用薬がなかったか、あった場合は薬剤名、投与期間等をお知らせください。プロトコル遵守（除外基準[31b]、3.8）の確認および安全性・有効性評価のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, Concomitant Medications (CM) data are missing. Please confirm if there were any concomitant medications during the study. If yes, provide drug name(s), administration dates, etc. This is needed to verify protocol compliance (Excl Crit [31b], Sec 3.8) and for safety/efficacy assessment.
        *   **判断理由:** 併用禁止・制限薬の使用有無を確認し、プロトコル遵守、安全性・有効性評価の信頼性を確保するため。
        *   **判断根拠:**
            *   関連するデータ: なし (CMドメインレコードなし)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b], Section 3.8 Concomitant Therapy
    *   **クエリNo.:** Q-10 (関連指摘No.: P-9)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、プロトコルスケジュール上、Visit 4 (WEEK 2、実施日 Study Day 41) で臨床検査（化学・血液・尿）が予定されていましたが、検査結果の報告がありません。検査が実施されなかった理由をお知らせください。安全性モニタリングの確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, clinical laboratory tests (Chemistry/Hematology/Urinalysis) were scheduled for Visit 4 (WEEK 2, conducted on Study Day 41) per protocol, but no results were reported. Please provide the reason why the tests were not performed. This is required for safety monitoring confirmation.
        *   **判断理由:** 計画された安全性モニタリング検査の未実施理由を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (Visit 4に対応するLBデータ欠損)
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 Schedule of Events, Section 3.9.3.3 Clinical Laboratory Tests
    *   **クエリNo.:** Q-11 (関連指摘No.: P-10)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号01-703-1279について、プロトコルスケジュール上、Visit 1, 2 (Ambulatory), 3, 4 でECG測定が予定されていましたが、ECGデータの報告がありません。ECGが実施されなかった理由をお知らせください。心血管系の安全性モニタリングの確認のため。
        *   **クエリ文面（英語）:** For patient 01-703-1279, ECGs were scheduled for Visits 1, 2 (Ambulatory), 3, and 4 per protocol, but no ECG data were reported. Please provide the reason why ECGs were not performed. This is required for cardiovascular safety monitoring confirmation.
        *   **判断理由:** 計画された心血管系の安全性モニタリングの未実施理由を確認するため。
        *   **判断根拠:**
            *   関連するデータ: なし (ECGデータ欠損)
            *   関連するプロトコル箇所: Protocol Attachment LZZT.1 Schedule of Events, Section 3.9.3.4.2 Cardiovascular Safety Measures, Section 3.9.4 Safety Monitoring

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 患者の統合失調症様障害の既往歴と、Day 41に見られたNPI-Xスコアの悪化との関連性について内部で考察する。開始日不明のため時間的関連は不明確だが、リスク因子として認識しておく。AE報告がない点も考慮。
        *   **判断理由:** データからは因果関係を特定できず、医療機関への問い合わせで追加情報が得られる可能性は低い。内部での医学的評価と記録に留める。
        *   **判断根拠:**
            *   関連するデータ: MH.MHTERM='SCHIZOPHRENIFORM DISORDERS', MH.MHSTDTC='' (欠損), QS.QSTESTCD='NPTOT' (Day 1 vs Day 41)
    *   **確認事項No.:** I-2 (関連指摘No.: P-6)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 4 (WEEK 2) の実施日が計画日 (Day 14) から大幅に遅延 (Day 41) している。DSドメインの情報から、このVisitが治験中止Visitであったためと推測される。評価への影響は限定的と考えられるため、内部記録に留める。
        *   **判断理由:** 中止に伴うスケジュール変更と考えられ、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: SV.VISITNUM=4, SV.VISITDY=14, SV.SVSTDTC='2013-06-22' (Day 41); DS.VISITNUM=4, DS.DSSTDY=41
    *   **確認事項No.:** I-3 (関連指摘No.: P-8)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** NPI-X評価が2週間隔で実施されていない。Day 41の評価は中止に伴う最終評価として実施された可能性がある。評価スケジュール逸脱ではあるが、中止症例であることを考慮すると影響は限定的。内部記録に留める。
        *   **判断理由:** 中止に伴う評価スケジュールの変更と考えられ、医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: QS.QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)', QS.QSDY (Day 1, 41); DS.DSSTDY=41
    *   **確認事項No.:** I-4 (関連指摘No.: P-12)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** スクリーニング時のHCTおよびHGB高値について、プロトコル[27b]に基づき臨床的に有意でないと判断され組み入れられたと推測されるが、その判断プロセスが適切であったか内部で確認・記録する。
        *   **判断理由:** 軽微な基準値逸脱であり、組み入れられていることから臨床的に問題ないと判断された可能性が高い。医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='HCT'/'HGB', LB.LBDY=-16, LB.LBNRIND='HIGH'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]

---

# 01-703-1299のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
81歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はPlaceboであった。主要な既往歴として、アルツハイマー病（2011年09月16日発症、Primary Diagnosis）、気分循環性障害（軽度）、聴力低下（軽度）、関節炎（軽度）が報告されている。また、乳癌（2004年）、乳房切除術（2004年）、結腸切除術（2007年）、腸閉塞（2007年）の既往がある。教育レベルは12年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年09月04日|Day -8 (N/A)|スクリーニング検査（血液・尿）実施。臨床検査値に特記すべき異常なし。|
|2012年09月07日|Day -5 (SCREENING 1)|スクリーニング評価実施。MMSE 23点、Hachinski Ischemic Score 0点。身長 153.67 cm、体重 47.17 kg。バイタルサイン測定。既往歴、併用薬（Timoptic点眼薬 1992年～）、教育レベル情報収集。|
|2012年09月10日|Day -2 (SCREENING 2)|バイタルサイン測定。|
|2012年09月12日|Day 1 (BASELINE)|ベースライン評価実施。体重 45.36 kg。バイタルサイン測定。ADAS-Cog(11) Total 5点。NPI-X Total 7点 (抑うつ/不快気分 2点, 不安 2点, 無関心/無感情 2点, 易怒性/不安定性 1点)。DAD Total 36/37 (97%)。治験薬（Placeboパッチ）投与開始。|
|2012年09月27日|Day 16 (AMBUL ECG PLACEMENT)|バイタルサイン測定。有害事象「上気道感染」(軽度) 発現。|
|2012年09月28日|Day 17 (WEEK 2)|バイタルサイン測定。体重 45.36 kg。臨床検査実施（アルブミン 34 g/L [LOW, 基準値 35-46]）。NPI-X Total 4点 (興奮/攻撃性 1点, 不安 1点, 無関心/無感情 2点)。|
|2012年10月06日|Day 25 (N/A)|有害事象「上気道感染」回復。|
|2012年10月10日|Day 29 (WEEK 4)|バイタルサイン測定。体重 44.45 kg。臨床検査実施（異常値なし）。NPI-X Total 7点 (抑うつ/不快気分 2点, 不安 2点, 無関心/無感情 1点, 易怒性/不安定性 2点)。|
|2012年10月12日|Day 31 (AMBUL ECG REMOVAL)|バイタルサイン測定。|
|2012年10月24日|Day 43 (WEEK 6)|バイタルサイン測定。体重 44.45 kg。臨床検査実施（異常値なし）。NPI-X Total 5点 (抑うつ/不快気分 2点, 不安 1点, 無関心/無感情 2点)。|
|2012年11月07日|Day 57 (WEEK 8)|バイタルサイン測定。体重 45.36 kg。臨床検査実施（異常値なし）。ADAS-Cog(11) Total 7点。CIBIC+ 3点 (最小改善)。NPI-X Total 12点 (抑うつ/不快気分 2点, 不安 2点, 無関心/無感情 3点, 易怒性/不安定性 4点,異常な運動行動 1点)。DAD Total 36/37 (97%)。|
|2012年11月21日|Day 71 (WEEK 10 (T))|NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。|
|2012年12月05日|Day 85 (WEEK 12)|バイタルサイン測定。体重 45.36 kg。臨床検査実施（ナトリウム 134 mmol/L [LOW, 基準値 135-145]）。NPI-X Total 13点 (抑うつ/不快気分 3点, 不安 4点, 無関心/無感情 6点)。DAD Total 36/37 (97%)。|
|2012年12月19日|Day 99 (WEEK 14 (T))|NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。|
|2013年01月02日|Day 113 (WEEK 16)|バイタルサイン測定。体重 45.36 kg。臨床検査実施（異常値なし）。ADAS-Cog(11) Total 12点。CIBIC+ 4点 (変化なし)。NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。DAD Total 36/37 (97%)。|
|2013年01月16日|Day 127 (WEEK 18 (T))|NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。|
|2013年01月30日|Day 141 (WEEK 20)|バイタルサイン測定。体重 44.00 kg。臨床検査実施（異常値なし）。NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。DAD Total 36/37 (97%)。|
|2013年02月13日|Day 155 (WEEK 22 (T))|NPI-X Total 6点 (抑うつ/不快気分 3点, 不安 1点, 無関心/無感情 2点)。|
|2013年03月01日|Day 171 (WEEK 24)|バイタルサイン測定（立位1分後 BP 108/64 mmHg, Pulse 82 bpm）。体重 43.55 kg。臨床検査実施（異常値なし）。ADAS-Cog(11) Total 11点。CIBIC+ 4点 (変化なし)。NPI-X Total 5点 (抑うつ/不快気分 3点, 食欲/摂食変化 2点)。DAD Total 35/37 (95%)。有害事象「低血圧」(軽度) 発現。有害事象「頻脈」(軽度) 発現。|
|2013年03月13日|Day 183 (WEEK 26)|バイタルサイン測定（立位1分後 BP 88/56 mmHg, Pulse 108 bpm）。体重 43.55 kg。臨床検査実施（異常値なし）。NPI-X Total 12点 (抑うつ/不快気分 6点, 無関心/無感情 6点)。有害事象「低血圧」が中等度に悪化。有害事象「頻脈」が中等度に悪化。有害事象「心筋梗塞」(中等度) 発現。治験薬投与終了。治験終了（プロトコル完了）。|
|2013年03月27日|Day 197 (UNSCHEDULED 13.1)|治験参加終了日。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 試験終了間際（Day 171-183）に低血圧、頻脈、心筋梗塞が相次いで発現・悪化している。心筋梗塞は重篤な有害事象（SAE）である可能性が高く、患者の安全性に重大な影響を与えうる。Placebo群での発現ではあるが、81歳という高齢であり、背景因子（脱水、感染、他の薬剤影響など）を含めた詳細な臨床経過、SAEとしての評価、治験薬との関連性評価（REMOTEとされているが妥当か）の再確認が必要である。
        *   **根拠:** 心筋梗塞は生命を脅かす可能性のある重篤なイベントであり、その発現経緯（先行する低血圧・頻脈）と合わせて詳細な医学的評価が不可欠である。参加者の安全確保が最優先される。
        *   **関連データ:**
            *   [有害事象名(AE.AETERM)] = 'HYPOTENSION', [有害事象開始日(Study Day)(AE.AESTDY)] = 171, [重症度/強度(AE.AESEV)] = 'MILD' -> 'MODERATE' (AESEQ=4, 6)
            *   [有害事象名(AE.AETERM)] = 'TACHYCARDIA', [有害事象開始日(Study Day)(AE.AESTDY)] = 171, [重症度/強度(AE.AESEV)] = 'MILD' -> 'MODERATE' (AESEQ=5, 7)
            *   [有害事象名(AE.AETERM)] = 'MYOCARDIAL INFARCTION', [有害事象開始日(Study Day)(AE.AESTDY)] = 183, [重症度/強度(AE.AESEV)] = 'MODERATE' (AESEQ=8)
            *   [収縮期血圧(VS.VSSTRESN where VSTESTCD='SYSBP')] = 108 (Day 171, 立位1分後), 88 (Day 183, 立位1分後)
            *   [拡張期血圧(VS.VSSTRESN where VSTESTCD='DIABP')] = 64 (Day 171, 立位1分後), 56 (Day 183, 立位1分後)
            *   [脈拍数(VS.VSSTRESN where VSTESTCD='PULSE')] = 82 (Day 171, 立位1分後), 108 (Day 183, 立位1分後)
            *   [年齢(DM.AGE)] = 81
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** 有害事象として「GLAUCOMA」（緑内障）が記録されているが、開始日が1992年であり、明らかに既往歴である。併用薬として緑内障治療薬（Timoptic点眼）が1992年から使用されていることとも整合する。AEドメインではなくMHドメインに記録されるべき事象である。
        *   **根拠:** AEは治験期間中に発現または悪化した事象を記録するものであり、治験開始前の既往歴はMHに記録するのが適切である。データの分類に関する問題であり、直接的な安全性リスクや評価への影響は小さい。
        *   **関連データ:**
            *   [有害事象名(AE.AETERM)] = 'GLAUCOMA', [有害事象開始日(AE.AESTDTC)] = '1992' (AESEQ=3)
            *   [報告された薬剤名(CM.CMTRT)] = 'TIMOPTIC', [薬剤開始日(CM.CMSTDTC)] = '1992'
    *   **指摘No.:** M-3
        *   **重要度:** Minor
        *   **内容:** NPI-X Totalスコアが、ベースライン7点からWeek 8で12点、Week 12で13点と悪化傾向を示した後、Week 24で5点とベースライン以下に改善し、Week 26で再度12点に悪化している。Placebo群であることを考慮しても変動が大きいように見え、評価の一貫性や信頼性について確認が望ましい。
        *   **根拠:** 有効性評価指標の変動が大きい場合、評価方法のばらつきやデータ入力ミスの可能性も考慮する必要がある。ただしPlacebo群であり、変動が疾患の自然経過や測定誤差の範囲内である可能性も高い。
        *   **関連データ:**
            *   [質問票名(QS.QSCAT)] = 'NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)'
            *   [質問票項目名(QS.QSTESTCD)] = 'NPTOT'
            *   [数値結果(QS.QSSTRESN)] = 7 (Day 1), 4 (Day 17), 7 (Day 29), 5 (Day 43), 12 (Day 57), 6 (Day 71), 13 (Day 85), 6 (Day 99), 6 (Day 113), 6 (Day 127), 6 (Day 141), 6 (Day 155), 5 (Day 171), 12 (Day 183)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 同意取得日（DM.RFICDTC）が欠損している。治験関連手順が同意取得後に開始されたかを確認できず、GCP遵守および参加者の権利保護の観点から問題となる可能性がある。
        *   **根拠:** GCPでは、治験関連手順の開始前に被験者から文書による同意を得ることが必須とされている。同意日の欠損はこの確認を不可能にする。
        *   **関連データ:**
            *   [インフォームド・コンセント日付/時刻(DM.RFICDTC)] = '' (欠損)
            *   [治験薬初回投与日時(DM.RFXSTDTC)] = '2012-09-12'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** AEドメインのMedDRAコーディング関連変数（AELLT, AELLTCD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCD）が欠損している。これにより、有害事象の標準化された分類や集計、安全性シグナルの検出が困難になる。
        *   **根拠:** MedDRAコーディングは、有害事象データを標準化し、異なる試験間や規制当局への報告において一貫性のある評価を可能にするために不可欠である。欠損は安全性評価の質を低下させる。
        *   **関連データ:**
            *   AEドメイン全体
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** CMドメインの薬剤標準名（CMDECOD）および薬剤クラス（CMCLAS）が"UNCODED"となっている。併用薬の正確な特定や、プロトコルで規定された禁止・制限薬との照合、薬物相互作用の評価が困難になる。
        *   **根拠:** 薬剤名の標準化（例：WHODrugコーディング）は、併用薬の正確な評価と安全性リスク（薬物相互作用など）の特定に不可欠である。
        *   **関連データ:**
            *   CMドメイン全体
    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** 有害事象「UPPER RESPIRATORY TRACT INFECTION」がAESEQ=1とAESEQ=2で重複して記録されている。開始日・終了日は同一だが、収集日（AEDTC）と転帰（AEOUT）が異なる。データの正確性に問題があり、どちらが正しい記録か、あるいは意図的な記録（例：再発・再燃）なのか不明確。
        *   **根拠:** 同一期間の同一事象が異なる転帰で記録されており、データの矛盾が生じている。ただし、事象自体は軽度であり、安全性評価全体への影響は限定的と考えられる。
        *   **関連データ:**
            *   [有害事象名(AE.AETERM)] = 'UPPER RESPIRATORY TRACT INFECTION'
            *   [シーケンス番号(AE.AESEQ)] = 1, 2
            *   [有害事象開始日(AE.AESTDTC)] = '2012-09-27' (両方)
            *   [有害事象終了日(AE.AEENDTC)] = '2012-10-06' (両方)
            *   [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AESEQ=1), 'RECOVERED/RESOLVED' (AESEQ=2)
            *   [収集日時(AE.AEDTC)] = '2012-09-28' (AESEQ=1), '2012-10-10' (AESEQ=2)
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** MHドメインのMedDRAコーディング関連変数（MHLLT, MHDECOD, MHHLT, MHHLGT, MHBODSYS）が一部欠損または未コード（例：ALZHEIMER'S DISEASE）。既往歴の詳細な分類や集計が不完全となる。
        *   **根拠:** 既往歴の標準化は、患者背景の正確な把握や、AEとの関連評価に有用だが、AEやCMほど直接的な安全性・有効性評価への影響は大きくない場合がある。
        *   **関連データ:**
            *   MHドメイン全体
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 有害事象として記録されている「GLAUCOMA」は、開始日が1992年であり、AEドメインではなくMHドメインに記録されるべきである。CMドメインのTimoptic開始年と一致しており、データの配置場所の問題である。
        *   **根拠:** ドメイン間のデータ配置の不整合。医学的評価への直接的な影響は小さい。
        *   **関連データ:**
            *   [有害事象名(AE.AETERM)] = 'GLAUCOMA', [有害事象開始日(AE.AESTDTC)] = '1992' (AESEQ=3)
            *   [報告された薬剤名(CM.CMTRT)] = 'TIMOPTIC', [薬剤開始日(CM.CMSTDTC)] = '1992'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[31b]ではβ遮断薬は原則除外対象だが、併用薬としてTimoptic（β遮断薬点眼薬）が治験開始前から継続使用されている。プロトコルには「Beta blocker eye drops for glaucoma will be considered on a case-by-case basis. Call medical monitor.」との例外規定があるが、この症例で適切に評価・承認されたか不明。適格性評価が不適切だった可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [31b] (p.18)
        *   **根拠:** 除外基準に抵触する可能性のある薬剤の使用は、参加者の安全性および試験データの解釈に影響を与える可能性があるため、適格性評価の妥当性を確認する必要がある。
        *   **関連データ:**
            *   [報告された薬剤名(CM.CMTRT)] = 'TIMOPTIC'
            *   [薬剤開始日(CM.CMSTDTC)] = '1992'
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日（DM.RFICDTC）が欠損しているため、治験関連手順（例：スクリーニング検査、治験薬投与）が同意取得前に開始されていないか確認できない。GCP違反の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent (p.49)
        *   **根拠:** GCPの基本原則として、治験参加前に被験者から自由意思による同意を文書で得ることが求められる。同意取得のタイミングが不明確な場合、参加者の権利が保護されていない可能性がある。
        *   **関連データ:**
            *   [インフォームド・コンセント日付/時刻(DM.RFICDTC)] = '' (欠損)
            *   [治験薬初回投与日時(DM.RFXSTDTC)] = '2012-09-12'
            *   [スクリーニングVisit開始日(SV.SVSTDTC where VISITNUM=1)] = '2012-09-07'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者番号1299について、Study Day 183に有害事象名「心筋梗塞」が重症度「中等度」で報告されています。先行して低血圧と頻脈も報告されていますが、心筋梗塞の診断根拠（心電図変化、心筋逸脱酵素など）、臨床経過の詳細、実施された処置、および重篤な有害事象（SAE）としての評価状況について詳細をお知らせください。また、治験薬との関連性が「REMOTE」と評価されていますが、その評価根拠についてもご教示ください。参加者の安全確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding subject 1299, AE Term 'MYOCARDIAL INFARCTION' (Severity: MODERATE) was reported on Study Day 183, preceded by HYPOTENSION and TACHYCARDIA. Please provide details on the diagnostic basis (ECG, enzymes, etc.), clinical course, treatment, and SAE assessment status. Also, please clarify the rationale for the causality assessment of 'REMOTE'. This information is crucial for patient safety assessment.
        *   **判断理由:** 心筋梗塞は重篤な有害事象であり、患者の安全性に直結するため、詳細な情報と評価の確認が最優先で必要。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='MYOCARDIAL INFARCTION', AE.AESTDY=183, AE.AESEV='MODERATE', AE.AEREL='REMOTE'。先行するAE.AETERM='HYPOTENSION', 'TACHYCARDIA'および関連するVSデータ。
            *   関連するプロトコル箇所: Section 3.9.3.2.2 Serious Adverse Events (p.31)
            *   関連する医学的知見: 心筋梗塞の診断基準、重篤性、関連性評価の重要性。
    *   **クエリNo.:** Q-2 (関連指摘No.: D-3, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号1299について、「インフォームド・コンセント日付/時刻」が記録されていません。治験実施計画書 Section 5.1 に基づき、治験関連手順開始前に同意が取得されている必要があります。正確な同意取得日をご提供ください。GCP遵守と参加者の権利保護の観点から確認が必要です。
        *   **クエリ文面（英語）:** For subject 1299, the Date/Time of Informed Consent (DM.RFICDTC) is missing. Per protocol Section 5.1 and GCP, consent must be obtained before any study procedures. Please provide the exact date of informed consent. This is required to confirm GCP compliance and protection of participant rights.
        *   **判断理由:** 同意取得日の欠損はGCP遵守の確認を不可能にし、参加者の権利保護に関わるため、確認が必要。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC = '' (欠損)
            *   関連するプロトコル箇所: Section 5.1 Informed Consent (p.49)
            *   関連する医学的知見: GCPにおける同意取得の重要性。
    *   **クエリNo.:** Q-3 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者番号1299について、併用薬としてTimoptic点眼薬（β遮断薬）が治験開始前から使用されています。治験実施計画書 Section 3.4.2.2 除外基準[31b]ではβ遮断薬は原則除外ですが、緑内障治療のための点眼薬は例外規定があります。この患者において、例外規定に基づき使用が適切に評価・承認された記録についてご確認ください。適格性確認のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding subject 1299, concomitant medication Timoptic eye drops (beta-blocker) has been used since before study start. Protocol Section 3.4.2.2 Exclusion Criteria [31b] generally excludes beta-blockers, but allows eye drops for glaucoma on a case-by-case basis with monitor approval. Please confirm if the use of Timoptic was appropriately evaluated and approved per protocol exception for this subject. This is needed to verify eligibility.
        *   **判断理由:** 除外基準に抵触する可能性のある薬剤の使用について、プロトコルの例外規定が適切に適用されたか確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: CM.CMTRT='TIMOPTIC', CM.CMSTDTC='1992'
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [31b] (p.18)
    *   **クエリNo.:** Q-4 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 患者番号1299について、有害事象「上気道感染」が2回（AESEQ=1および2）記録されています。開始日・終了日は同一ですが、収集日と転帰が異なります。これは同一イベントの記録修正か、あるいは別のイベント（例：再発）でしょうか？ 正確な情報をご提供ください。
        *   **クエリ文面（英語）:** For subject 1299, AE 'UPPER RESPIRATORY TRACT INFECTION' is recorded twice (AESEQ=1 and 2) with the same start/end dates but different collection dates and outcomes. Is this a correction of the same event or a separate event (e.g., recurrence)? Please clarify and provide the correct information.
        *   **判断理由:** データの不整合があり、正確な有害事象の記録を確認する必要があるため。
        *   **判断根拠:**
            *   関連するデータ: AEドメインのAESEQ=1および2の記録。

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-2, D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインに記録されている「GLAUCOMA」（開始日1992年）は既往歴であるため、MHドメインへの移行を検討する。CMドメインのTimoptic使用歴と整合している。データクリーニングの一環として対応する。
        *   **判断理由:** データの分類・配置に関する問題であり、医療機関への問い合わせは不要。内部でのデータ修正で対応可能。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='GLAUCOMA', AE.AESTDTC='1992', CM.CMTRT='TIMOPTIC', CM.CMSTDTC='1992'
    *   **確認事項No.:** I-2 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor / DM
        *   **疑義事項/確認内容:** NPI-X Totalスコアの変動が大きい（特にWeek 24での改善とWeek 26での悪化）。Placebo群であり疾患の自然経過や評価のばらつきの可能性が高いが、データ入力ミスがないか、評価の一貫性に問題がなかったか内部で確認する。
        *   **判断理由:** Placebo群での変動であり、直ちに安全性や有効性評価の根幹を揺るがすものではないため、まずは内部確認とする。
        *   **判断根拠:**
            *   関連するデータ: QSドメインのNPI-X関連データ (QSTESTCD='NPTOT'など)
    *   **確認事項No.:** I-3 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AEドメインのMedDRAコーディングが未完了。安全性評価および集計のため、コーディング作業を完了させる必要がある。
        *   **判断理由:** データ標準化と評価に必須の作業であり、内部（DM担当）で対応すべき事項。
        *   **判断根拠:**
            *   関連するデータ: AEドメインのコーディング関連変数（AELLT, AEDECODなど）の欠損。
    *   **確認事項No.:** I-4 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** CMドメインの薬剤標準名（CMDECOD）および薬剤クラス（CMCLAS）が"UNCODED"。併用薬評価のため、薬剤コーディング（例：WHODrug）を完了させる必要がある。
        *   **判断理由:** データ標準化と評価に必須の作業であり、内部（DM担当）で対応すべき事項。
        *   **判断根拠:**
            *   関連するデータ: CMドメインのCMDECOD, CMCLASが"UNCODED"。
    *   **確認事項No.:** I-5 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインのMedDRAコーディングが一部未完了。既往歴データの標準化のため、コーディング作業を完了させることが望ましい。
        *   **判断理由:** データ標準化作業であり、内部（DM担当）で対応すべき事項。AEやCMほど緊急性は高くない。
        *   **判断根拠:**
            *   関連するデータ: MHドメインのコーディング関連変数（MHDECODなど）の欠損。

---

# 01-703-1335のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    67歳、女性、人種はBLACK OR AFRICAN AMERICAN、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2008年発症、PRIMARY DIAGNOSIS）、消化性潰瘍（2007年発症、HISTORICAL DIAGNOSIS）、関節炎（発症時期不明、SIGNIFICANT PRE-EXISTING CONDITION、重症度: MILD）が報告されている。教育レベルは11年であった。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2013年12月28日|Day -79 (SCREENING 1)|臨床検査実施 (例: CK 153 U/L, ALT 22 U/L)。|
|2014年02月21日|Day -24 (UNSCHEDULED 1.1)|臨床検査実施。クレアチンキナーゼ(CK)が209 U/Lと高値 (基準値上限169 U/L)。|
|2014年02月28日|Day -17 (SCREENING 1)|人口統計学的情報、既往歴、教育レベル収集。バイタルサイン測定 (例: 体重 55.79 kg)。MMSEスコア 10点、Hachinskiスコア 2点 (Focal Neurological Signs Present)。|
|2014年03月15日|Day -2 (SCREENING 2)|バイタルサイン測定。有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」(重症度: MILD) 発現。|
|2014年03月17日|Day 1 (BASELINE)|治験薬投与開始 (Xanomeline 54 mg Patch QD)。ベースライン評価実施。バイタルサイン測定 (例: 体重 55.34 kg)。ADAS-COG(11)スコア 57点。NPI-X Totalスコア 24点 (Agitation/Aggression 12点, Irritability/Lability 12点)。DAD評価実施。|
|2014年03月30日|Day 14 (AMBUL ECG PLACEMENT)|バイタルサイン測定 (臥位血圧 100/60 mmHg、ベースライン130/80 mmHgから低下傾向)。有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」回復。|
|2014年03月31日|Day 15 (WEEK 2)|臨床検査実施。CKが219 U/Lと引き続き高値。NPI-X Totalスコア 10点 (ベースラインから改善)。バイタルサイン測定 (体重 53.52 kg、ベースラインから1.8kg減少)。治験薬投与量変更準備 (54mg投与終了)。|
|2014年04月01日|Day 16 (N/A)|治験薬投与量増加 (Xanomeline 81 mg Patch QD)。有害事象「MULTIPLE SCLEROSIS RELAPSE」(重症度: MILD) 発現。|
|2014年04月13日|Day 28 (WEEK 4)|臨床検査実施。CK 134 U/L (正常化)。NPI-X Totalスコア 24点 (ベースラインレベルに悪化)。バイタルサイン測定 (体重 53.52 kg)。|
|2014年04月15日|Day 30 (AMBUL ECG REMOVAL)|バイタルサイン測定 (立位脈拍 100回/分、頻脈傾向)。|
|2014年05月01日|Day 46 (N/A)|有害事象「MULTIPLE SCLEROSIS RELAPSE」転帰: NOT RECOVERED/NOT RESOLVED。|
|2014年05月07日|Day 52 (N/A)|治験薬最終投与日。|
|2014年05月24日|Day 69 (WEEK 6)|治験中止 (理由: PROTOCOL VIOLATION)。最終評価実施。臨床検査実施。ADAS-COG(11)スコア 61.5点 (ベースラインから悪化)。CIBIC+スコア 5点 (Minimal worsening)。NPI-X Totalスコア 10点 (項目変動あり、Depression/Apathy出現)。DAD評価 (Leisure項目悪化)。バイタルサイン測定 (体重 54.43 kg)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「MULTIPLE SCLEROSIS RELAPSE」が治験薬増量後(Day 16)に発現し、回復していない。既往歴(MH)にはMSの記載がないため、新規発症か既往歴の報告漏れか不明。もし既往歴があれば除外基準(EXCL12: Serious neurological conditions)違反の可能性があり、参加者の安全性リスクとデータの妥当性に重大な影響を与える。
        *   **根拠:** AEデータとMHデータの不整合。MSは重篤な神経疾患であり、除外基準に該当する可能性がある。治験薬との関連は不明だが、増量直後の発現は時間的関連性がある。
        *   **関連データ:**
            *   [報告された有害事象名(AE.AETERM)] = 'MULTIPLE SCLEROSIS RELAPSE'
            *   [有害事象開始日(Study Day)(AE.AESTDY)] = 16
            *   [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   MHドメインにMSの記載なし
            *   プロトコル 3.4.2.2 Exclusion Criteria [12]
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Screening中(Day -2)に有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」が発現している。MildでDay 14に回復しているが、除外基準(EXCL16b: Second or third degree heart block)に抵触する可能性があった。Xanomelineはムスカリン作動薬であり心臓への影響（徐脈、房室ブロック等）は既知のリスクとして考慮すべきであり、本症例の適格性評価が適切だったか疑問。また、Day 14の臥位血圧低下(100/60)、Day 30の立位頻脈(100)も観察されており、心血管系への影響が示唆される。
        *   **根拠:** AEデータ、VSデータ、除外基準、治験薬の薬理作用（一般的な医学知識）。
        *   **関連データ:**
            *   [報告された有害事象名(AE.AETERM)] = 'ATRIOVENTRICULAR BLOCK SECOND DEGREE'
            *   [有害事象開始日(Study Day)(AE.AESTDY)] = -2
            *   [有害事象終了日(Study Day)(AE.AEENDY)] = 14
            *   [拡張期血圧(VS.VSSTRESN where VSTESTCD='DIABP', VSDY=14, VSPOS='SUPINE')] = 60
            *   [脈拍数(VS.VSSTRESN where VSTESTCD='PULSE', VSDY=30, VSPOS='STANDING', VSTPTNUM=816 or 817)] = 100
            *   プロトコル 3.4.2.2 Exclusion Criteria [16b]
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** 主要評価項目であるADAS-Cog(11)およびCIBIC+が悪化傾向を示しており、副次評価項目(NPI-X, DAD)も一貫した改善を示していない。全体として治験薬の有効性が示唆されず、むしろ疾患進行または薬剤による悪化の可能性も否定できない。
        *   **根拠:** QSドメインの有効性評価データ。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 3, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 57
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Visit Number(QS.VISITNUM)] = 7, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 61.5
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Visit Number(QS.VISITNUM)] = 7, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 5
            *   NPI-X, DADの各評価結果 (QSドメイン)
    *   **指摘No.:** M-4
        *   **重要度:** Minor
        *   **内容:** Screening時(Day -24)およびWeek 2(Day 15)にCK高値が認められたが、関連する有害事象（筋肉痛など）の報告がない。その後正常化しているため緊急性は低いが、原因は不明。
        *   **根拠:** LBデータとAEデータの比較。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK', [Study Day of Specimen Collection(LB.LBDY)] = -24, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 209, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK', [Study Day of Specimen Collection(LB.LBDY)] = 15, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 219, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   AEドメインに関連する事象報告なし
    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** Week 2(Day 15)までにベースラインから1.8kgの体重減少が見られたが、関連する有害事象（食欲不振など）の報告がない。その後やや回復傾向。
        *   **根拠:** VSデータとAEデータの比較。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'WEIGHT', [Study Day of Vital Signs(VS.VSDY)] = 1, [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 55.34
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'WEIGHT', [Study Day of Vital Signs(VS.VSDY)] = 15, [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 53.52
            *   AEドメインに関連する事象報告なし

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** MHドメインにMSの記載がないにも関わらず、AEドメインで「MULTIPLE SCLEROSIS RELAPSE」が報告されている。これは既往歴の報告漏れ、あるいはAE診断の誤りの可能性があり、患者の適格性評価および安全性評価の根幹に関わる重大な不整合である。
        *   **根拠:** MHドメインとAEドメインのクロスチェック。
        *   **関連データ:**
            *   MHドメインにMS関連のMHTERM/MHDECODなし
            *   [報告された有害事象名(AE.AETERM)] = 'MULTIPLE SCLEROSIS RELAPSE'
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** 治験中止日(DS.DSSTDY=69)と治験薬最終投与日(EX.EXENDY=52)が17日間乖離している。中止理由がProtocol Violationとされているが、投与終了から中止までの期間に何があったのか不明であり、曝露期間の評価や中止理由の解釈に影響を与える可能性がある。
        *   **根拠:** DSドメインとEXドメインの日付比較。
        *   **関連データ:**
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 69
            *   [Study Day of End of Treatment(EX.EXENDY)] = 52
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'PROTOCOL VIOLATION'
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** CM（併用薬）ドメインにデータが存在しない。アルツハイマー病、消化性潰瘍、関節炎の既往があり、MS再発やCK高値、AVブロックといったイベントも発生しているため、何らかの併用薬が存在する可能性が高い。併用薬情報の欠損は、有害事象の評価、薬物相互作用の評価、有効性評価、および併用禁止薬使用の有無確認に重大な影響を与える。
        *   **根拠:** CMドメインが空であること、およびMH/AE/LBデータとの関連性。
        *   **関連データ:**
            *   CMドメインのレコード数が0
            *   MH, AE, LBドメインのデータ
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** CK高値、体重減少、血圧/脈拍変動といった臨床的に注目すべき所見に対応する有害事象がAEドメインに記録されていない可能性がある。安全性プロファイルの評価が不完全になる恐れがある。
        *   **根拠:** LB, VSデータとAEデータのクロスチェック。
        *   **関連データ:**
            *   LB.LBTESTCD='CK'の高値記録
            *   VS.VSTESTCD='WEIGHT'の減少記録
            *   VSの血圧・脈拍変動記録
            *   AEドメインに対応する事象報告なし
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** Subject Elements (SE)ドメインとExposure (EX)ドメインの間で、Element期間（特にHigh_Middle）の開始日と終了日に不整合が見られる。SE開始日(Day 15)がEX開始日(Day 16)より早く、SE終了日(Day 69)がEX終了日(Day 52)より遅い。データの解釈に軽微な混乱を招く可能性があるが、主要な評価への影響は限定的と考えられる。
        *   **根拠:** SEドメインとEXドメインの日付比較。
        *   **関連データ:**
            *   [Element Code(SE.ETCD)] = 'HIM', [Start Date/Time of Element(SE.SESTDTC)] = '2014-03-31', [End Date/Time of Element(SE.SEENDTC)] = '2014-05-24'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE', [Dose per Administration(EX.EXDOSE)] = 81, [Start Date/Time of Treatment(EX.EXSTDTC)] = '2014-04-01', [End Date/Time of Treatment(EX.EXENDTC)] = '2014-05-07'

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** 除外基準違反の可能性が複数存在する。
            1.  **EXCL12 (Serious neurological conditions):** AEでMS再発が報告されており、もしMSの既往があれば本基準に違反する。MHに記載がない点が問題。
            2.  **EXCL16b (Second or third degree heart block):** Screening中にAVブロックII度が発現しており、Enrollment時点で回復していなければ本基準に違反する。
            3.  **EXCL27b (Laboratory test values exceeding range):** Screening中にCK高値(209 U/L)が基準値上限(169 U/L)を超過しており、本基準に違反する。
            これらの違反は、参加者の安全性に重大なリスクをもたらし、試験データの信頼性を著しく損なう可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [12], [16b], [27b]
        *   **根拠:** AE, LB, MHデータとプロトコル基準の比較。
        *   **関連データ:**
            *   [報告された有害事象名(AE.AETERM)] = 'MULTIPLE SCLEROSIS RELAPSE'
            *   [報告された有害事象名(AE.AETERM)] = 'ATRIOVENTRICULAR BLOCK SECOND DEGREE'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK', [Study Day of Specimen Collection(LB.LBDY)] = -24, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 209
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験薬がプロトコル規定の26週を待たずに早期に中止されている（Day 52投与終了、Day 69中止）。中止理由は「PROTOCOL VIOLATION」と記録されているが、具体的な内容が不明。有効性不十分や安全性懸念が背景にある可能性も考えられ、試験評価に影響する。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (26 weeks duration), Section 3.10.1 Discontinuations
        *   **根拠:** DS, EXデータとプロトコル規定期間の比較。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'PROTOCOL VIOLATION'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 69
            *   [Study Day of End of Treatment(EX.EXENDY)] = 52
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 治験中止時の漸減投与（プロトコル3.10.1指示）が実施されなかった可能性がある。EXデータではDay 52に81mg投与が突然終了しており、漸減投与（50cm2パッチへの変更）の記録がない。参加者の安全性に関わる手順逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** EXデータとプロトコル規定の中止手順の比較。
        *   **関連データ:**
            *   EXドメインに漸減投与の記録なし
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 適格性確認に必要な一部データ（CNS imaging結果、Syphilis screening結果、HbA1c結果、同意取得日）が欠損している。これにより、関連する選択/除外基準（Inclusion [5], Exclusion [29b], [30b], Inclusion [6]）の遵守を完全に確認できない。ただし、他のデータから現時点で重大な違反は強く示唆されないためMinorとする。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5], [6], Section 3.4.2.2 Exclusion Criteria [29b], [30b]
        *   **根拠:** 関連データの欠損。
        *   **関連データ:**
            *   関連するデータフィールドが欠損またはデータなし
    *   **指摘No.:** P-5
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 7 (Week 6) の実施日がPlanned Study Day 42に対し、Actual Study Day 69であり、プロトコルで規定されたVisit Window (±3 days) を逸脱している。中止に伴う最終評価の可能性が高いが、形式的には逸脱となる。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit schedule and window)
        *   **根拠:** SVデータとTVデータの比較。
        *   **関連データ:**
            *   [Visit Number(SV.VISITNUM)] = 7, [Start Date/Time of Visit(SV.SVSTDTC)] = '2014-05-24' (Day 69)
            *   [Visit Number(TV.VISITNUM)] = 7, [Planned Study Day of Visit(TV.VISITDY)] = 42
    *   **指摘No.:** P-6
        *   **重要度:** Minor
        *   **逸脱の可能性:** Urinalysisがプロトコル規定のVisit 4 (Week 2)で実施されていない可能性がある（LBデータにVisit 4のUrinalysis記録がない）。評価スケジュールの逸脱。
        *   **プロトコル該当箇所:** Section 3.9.3.3 Clinical Laboratory Tests, Attachment LZZT.1 Schedule of Events
        *   **根拠:** LBデータとプロトコル規定の評価スケジュールの比較。
        *   **関連データ:**
            *   LBドメインにVisit 4 (VISITNUM=4) のLBCAT='URINALYSIS'の記録なし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1, P-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として「MULTIPLE SCLEROSIS RELAPSE」が報告されていますが、既往歴にはMSの記載がありませんでした。本患者にMSの既往はありますでしょうか？もし既往がある場合、除外基準[12]に抵触する可能性があるため、詳細な病歴とEnrollment時の評価について確認させてください。もし既往がない場合、AE診断「MULTIPLE SCLEROSIS RELAPSE」の根拠と確定診断プロセスについて詳細をお知らせください。参加者の適格性と安全性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** AE 'MULTIPLE SCLEROSIS RELAPSE' was reported, but MS was not listed in MH. Does the subject have a history of MS? If yes, please provide details and confirm eligibility per Excl. Criterion [12]. If no history, please provide basis for AE diagnosis. This information is crucial for subject safety and eligibility assessment.
        *   **判断理由:** MHとAEの重大な不整合であり、適格性（除外基準違反）と安全性に直接関わるため、緊急の確認が必要。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='MULTIPLE SCLEROSIS RELAPSE', MHドメインにMS記載なし, プロトコル Section 3.4.2.2 [12]
            *   関連する医学的知見: MSは重篤な神経疾患。
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, P-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Screening Visit 2 (Study Day -2)で有害事象「ATRIOVENTRICULAR BLOCK SECOND DEGREE」が報告されています。Enrollment (Study Day 1) 時点の心電図所見および臨床状態について確認させてください。本有害事象は除外基準[16b]に該当する可能性があるため、適格性判断の根拠についてもお知らせください。参加者の安全性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** AE 'ATRIOVENTRICULAR BLOCK SECOND DEGREE' was reported on Day -2 (Screening). Please confirm ECG findings and clinical status at enrollment (Day 1). This AE may relate to Excl. Criterion [16b]. Confirm basis for eligibility determination for subject safety.
        *   **判断理由:** 除外基準違反の可能性があり、心血管系の安全性リスクに関わるため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='ATRIOVENTRICULAR BLOCK SECOND DEGREE', AE.AESTDY=-2, プロトコル Section 3.4.2.2 [16b]
            *   関連する医学的知見: AVブロックは重篤な不整脈であり、ムスカリン作動薬のリスク。
    *   **クエリNo.:** Q-3 (関連指摘No.: P-1, M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Unscheduled Visit 1.1 (Study Day -24) のクレアチンキナーゼが「209 U/L」と高値であり、除外基準[27b]に該当する可能性がありました。Enrollment時の適格性判断について、本検査結果をどのように評価されたか確認させてください。
        *   **クエリ文面（英語）:** On Day -24 (Unscheduled 1.1), Creatine Kinase was high (209 U/L), potentially meeting Excl. Criterion [27b]. Please confirm how this lab value was assessed for eligibility determination at enrollment.
        *   **判断理由:** 除外基準違反の可能性があったため、適格性評価の妥当性を確認する必要がある。ただし、その後正常化しているためMajorとした。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='CK', LB.LBDY=-24, LB.LBSTRESN=209, LB.LBNRIND='HIGH', プロトコル Section 3.4.2.2 [27b]
    *   **クエリNo.:** Q-4 (関連指摘No.: D-2, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本症例はStudy Day 69に「PROTOCOL VIOLATION」を理由に中止されていますが、治験薬の最終投与はStudy Day 52でした。Study Day 52に投与が終了した具体的な理由、および中止理由「PROTOCOL VIOLATION」の詳細についてお知らせください。
        *   **クエリ文面（英語）:** Subject discontinued on Day 69 due to 'PROTOCOL VIOLATION', but last dose was on Day 52. Please clarify the specific reason for stopping treatment on Day 52 and provide details for the 'PROTOCOL VIOLATION'.
        *   **判断理由:** 投与終了と中止日の乖離、および中止理由の詳細が不明であり、試験評価に影響するため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='PROTOCOL VIOLATION', DS.DSSTDY=69, EX.EXENDY=52
    *   **クエリNo.:** Q-5 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬(CM)のデータが報告されていません。本症例では複数の既往歴や有害事象（MS再発、AVブロック、CK高値等）が報告されています。併用薬（特にMS治療薬、心血管系薬剤、スタチン、精神科薬、関節炎治療薬、消化性潰瘍治療薬など）の使用有無について確認し、使用があった場合は詳細をご報告ください。併用禁止・制限薬の確認および安全性評価のため重要です。
        *   **クエリ文面（英語）:** Concomitant medication (CM) data is missing. Given the subject's MH and AEs (MS relapse, AV block, high CK), please confirm if any CMs were used (esp. for MS, cardiac, statins, psychotropics, arthritis, ulcer) and provide details if applicable. This is needed for safety/prohibited med assessment.
        *   **判断理由:** 併用薬情報の欠損は、安全性評価、有効性評価、プロトコル遵守（併用禁止薬）の確認に不可欠。
        *   **判断根拠:**
            *   関連するデータ: CMドメイン空, MH/AE/LBデータ
    *   **クエリNo.:** Q-6 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコル3.10.1では中止時に治験薬の漸減投与が指示されていますが、本症例ではStudy Day 52に81mg投与が終了した記録のみです。中止に際して、プロトコルに従った漸減投与（50cm2パッチへの変更）は実施されましたでしょうか？
        *   **クエリ文面（英語）:** Protocol 3.10.1 requires dose tapering upon discontinuation. Records show 81mg stopped on Day 52. Was the dose tapered down (changed to 50cm2 patch) as per protocol before final discontinuation?
        *   **判断理由:** プロトコルで規定された安全性に関わる手順の遵守状況を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: EXデータ, プロトコル Section 3.10.1
    *   **クエリNo.:** Q-7 (関連指摘No.: D-4, M-4, M-5)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** クレアチンキナーゼ高値、体重減少、血圧/脈拍変動が観察されましたが、関連する有害事象（例：筋肉痛、食欲不振、消化器症状、めまい、動悸など）の報告がありませんでした。これらの症状の有無について確認し、もし症状があった場合は有害事象としてご報告ください。安全性評価の完全性のために必要です。
        *   **クエリ文面（英語）:** High CK, weight loss, and BP/pulse fluctuations were observed, but no related AEs (e.g., myalgia, appetite loss, GI symptoms, dizziness, palpitations) were reported. Please confirm if subject experienced such symptoms and report as AE if applicable for complete safety assessment.
        *   **判断理由:** 臨床検査値やバイタルサインの異常に対応する症状の有無を確認し、未報告の有害事象がないか確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: LB(CK), VS(WEIGHT, DIABP, SYSBP, PULSE), AEドメイン

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** Subject Elements (SE)ドメインとExposure (EX)ドメインの期間不整合（特にHigh_Middle element）。データ入力または導出ロジックの問題の可能性。影響は軽微と判断されるが、データマネジメント内で原因を確認し、必要であれば修正または記録する。
        *   **判断理由:** 主要な評価への影響は限定的であり、内部でのデータクリーニングプロセスで対応可能と判断。
        *   **判断根拠:**
            *   関連するデータ: SE, EXデータ
    *   **確認事項No.:** I-2 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** 適格性確認に必要な一部データ（CNS imaging結果、Syphilis screening結果、HbA1c結果、同意取得日）が欠損している。他の情報から現時点で重大な違反は示唆されないが、欠損理由を可能な範囲で確認し記録する。試験全体のデータ品質管理の観点から留意。
        *   **判断理由:** 重大な違反を示唆する情報がないため緊急性は低いが、データの完全性に関する問題として記録。
        *   **判断根拠:**
            *   関連するデータフィールドの欠損
    *   **確認事項No.:** I-3 (関連指摘No.: P-5, P-6)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 7のVisit Window逸脱およびVisit 4でのUrinalysis未実施の可能性。これらは治験中止に関連する状況下で発生した可能性が高く、評価への影響は限定的と考えられるため、クエリ発行は不要と判断。プロトコル逸脱として記録する。
        *   **判断理由:** 中止という特殊状況を考慮すると、評価への実質的な影響は小さいと判断。
        *   **判断根拠:**
            *   関連するデータ: SV, TV, LBデータ
    *   **確認事項No.:** I-4 (関連指摘No.: M-6)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 本症例では有効性評価結果が悪化傾向を示している。個別のクエリは発行しないが、試験全体の有効性評価の観点から重要な所見であり、他の症例の傾向と合わせて評価する必要があるため記録する。
        *   **判断理由:** 個別症例の問題というより、試験全体の有効性評価に関わるため内部での検討事項とする。
        *   **判断根拠:**
            *   関連するデータ: QSドメインの有効性評価データ

---

# 01-703-1403のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
67歳、男性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline Low Doseであった（計画された治療群はXanomeline High Dose）。主要な既往歴として、アルツハイマー病（2010年12月7日発症）が報告されている。その他、難聴、右白内障、指の裂傷の既往歴がある。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年11月14日|Day -28 (N/A)|併用薬「CIPRO」投与開始|
|2012年11月28日|Day -14 (SCREENING 1)|検査値：Urate 7.7 mg/dL (基準値上限 7.5 mg/dL をわずかに超える)|
|2012年11月28日|Day -14 (N/A)|併用薬「CIPRO」投与終了|
|2012年12月05日|Day -7 (SCREENING 1)|MMSEスコア 23点、Hachinskiスコア 1点。教育歴 12年。|
|2012年12月10日|Day -2 (SCREENING 2)|Visit実施 (Planned Day -1から逸脱)|
|2012年12月12日|Day 1 (BASELINE)|治験薬「XANOMELINE」54mg (Low Dose) 投与開始。体重 80.29 kg。ADAS-Cog(11) 14点。NPI-X Total Score 1点 (Anxiety)。|
|2012年12月12日|Day 1 (BASELINE)|有害事象「WEIGHT DECREASED」(Moderate, 関連性なし) 発現 (終了日: 2012-12-19, Day 8)|
|2012年12月13日|Day 2 (N/A)|有害事象「MYASTHENIA GRAVIS AGGRAVATED」(Moderate, 関連性Probable) 発現 (終了日: 2012-12-14, Day 3)|
|2012年12月13日|Day 2 (N/A)|有害事象「VOMITING」(Moderate, 関連性Probable) 発現 (終了日: 2012-12-14, Day 3)|
|2012年12月13日|Day 2 (N/A)|治験薬「XANOMELINE」投与終了|
|2012年12月15日|Day 4 (N/A)|有害事象「CHEST DISCOMFORT」(Mild, 関連性Probable) 発現 (終了日: 2012-12-16, Day 5)|
|2012年12月19日|Day 8 (WEEK 2)|Visit実施 (Planned Day 14から逸脱)。体重 74.84 kg (ベースラインから約5.45kg減少)。検査値：Platelet 177 G/L (ベースライン 222 G/Lから減少、基準値内)。Urate 7.5 mg/dL (ベースライン 7.7 mg/dLから低下し基準値上限)。|
|2012年12月19日|Day 8 (WEEK 2)|有害事象により治験中止 (Disposition Event: ADVERSE EVENT)。有害事象「WEIGHT DECREASED」の転帰が「NOT RECOVERED/NOT RESOLVED」として記録される。|
|2013年01月08日|N/A (AE FOLLOW-UP)|Visit実施。有害事象「WEIGHT DECREASED」の転帰が「RECOVERED/RESOLVED」として記録される (開始日・終了日はDay 1-8のまま)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象として「MYASTHENIA GRAVIS AGGRAVATED」が報告され、治験薬との関連がProbableと評価され、治験中止に至っている。重症筋無力症はコリン作動薬により増悪する可能性があり、医学的に重要な有害事象である。もし被験者が重症筋無力症の既往を有していた場合、除外基準[12g]に抵触する可能性があり、参加者の安全性に重大なリスクをもたらした可能性がある。既往歴の有無を明確にする必要がある。
        *   **根拠:** 重症筋無力症はアセチルコリン受容体に対する自己免疫疾患であり、コリン作動薬（XanomelineはM1アゴニスト）はコリン作動性クリーゼを引き起こすリスクや症状増悪のリスクがある。プロトコル除外基準[12g]にMyasthenia gravisが含まれている。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYASTHENIA GRAVIS AGGRAVATED'
            *   [Severity/Intensity(AE.AESEV)] = 'MODERATE'
            *   [Causality(AE.AEREL)] = 'PROBABLE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-12-13' (Day 2)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-12-14' (Day 3)
            *   [Reported Term for the Disposition Event(DS.DSTERM)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2012-12-19' (Day 8)
            *   MHドメインには重症筋無力症の記載なし。
            *   プロトコル Section 3.4.2.2 [12g]

    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「WEIGHT DECREASED」が治験薬投与開始日(Day 1)から中止日(Day 8)にかけて報告され、実際に体重が約5.45kg減少している。しかし、治験薬との関連性は「NONE」と評価されている。嘔吐のAE(Day 2-3)も報告されており、治験薬との関連(Probable)が評価されていることから、体重減少との関連性評価「NONE」は疑問が残る。安全性評価の妥当性に影響する可能性がある。
        *   **根拠:** コリン作動薬の副作用として嘔吐や食欲不振があり、体重減少につながる可能性がある。短期間での5kg以上の体重減少は臨床的に無視できない。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'WEIGHT DECREASED' (AESEQ=1, 5)
            *   [Severity/Intensity(AE.AESEV)] = 'MODERATE'
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-12-12' (Day 1)
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2012-12-19' (Day 8)
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 80.29 (Day 1, WEIGHT)
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 74.84 (Day 8, WEIGHT)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'VOMITING' (AESEQ=3)
            *   [Causality(AE.AEREL)] = 'PROBABLE'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Major
        *   **内容:** 有害事象「WEIGHT DECREASED」が2つのレコード(AESEQ=1, 5)で報告されている。開始日、終了日、重症度、関連性は同一だが、収集日(AEDTC)と転帰(AEOUT)が異なる（Day 8時点では'NOT RECOVERED/NOT RESOLVED'、Day 27のAE Follow-up Visit時点では'RECOVERED/RESOLVED'）。これは同一事象のフォローアップ更新と考えられるが、重複登録の可能性も否定できない。データの正確性と解釈に影響を与える可能性がある。
        *   **根拠:** 同一の有害事象が複数のレコードで報告されており、転帰情報が異なる。
        *   **関連データ:**
            *   AEドメイン: AESEQ=1, AESEQ=5
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED' (AESEQ=1, AEDTC='2012-12-19')
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'RECOVERED/RESOLVED' (AESEQ=5, AEDTC='2013-01-08')
            *   SVドメイン: VISITNUM=101 (AE FOLLOW-UP), SVSTDTC='2013-01-08'

    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** DMドメインにおいて、計画された治療群コード(DM.ARMCD)が'Xan_Hi' (Xanomeline High Dose)であるのに対し、実際に割り付けられた治療群コード(DM.ACTARMCD)は'Xan_Lo' (Xanomeline Low Dose)となっている。EXドメインの投与記録(EXTRT='XANOMELINE', EXDOSE=54mg)はActual Arm Codeと一致している。Planned ArmとActual Armの不一致は、無作為化割付のエラー、あるいはデータ入力エラーの可能性を示唆し、試験の信頼性に影響を与える可能性がある。
        *   **根拠:** DMドメイン内のARMCDとACTARMCDの値が異なる。
        *   **関連データ:**
            *   [Planned Arm Code(DM.ARMCD)] = 'Xan_Hi'
            *   [Description of Planned Arm(DM.ARM)] = 'Xanomeline High Dose'
            *   [Actual Arm Code(DM.ACTARMCD)] = 'Xan_Lo'
            *   [Description of Actual Arm(DM.ACTARM)] = 'Xanomeline Low Dose'
            *   [Name of Actual Treatment(EX.EXTRT)] = 'XANOMELINE'
            *   [Dose per Administration(EX.EXDOSE)] = 54

    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 同意取得日(DM.RFICDTC)が欠損している。同意取得日は治験開始前の重要な日付であり、治験手順が同意取得後に行われたことを確認するために必須である。この欠損はGCP遵守の観点から問題となる可能性がある。
        *   **根拠:** Define.xmlではDM.RFICDTCは必須ではないが、GCP上、同意取得日と治験手順開始日の前後関係は重要。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = '' (欠損)
            *   [Subject Reference Start Date/Time(DM.RFSTDTC)] = '2012-12-12' (治験薬初回投与日)

    *   **指摘No.:** D-4
        *   **重要度:** Minor
        *   **内容:** MHドメインにおいて、一部の既往歴（難聴、白内障、指の裂傷）の開始日(MH.MHSTDTC)が欠損している。これらの既往歴は主要な評価項目や安全性に直接的な影響を与える可能性は低いと考えられるが、データの完全性の観点からは記録が望ましい。
        *   **根拠:** MHドメインの一部のレコードでMHSTDTCが欠損。
        *   **関連データ:**
            *   MHドメイン: MHSEQ=1, 2, 3 の MHSTDTC が欠損

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** 除外基準[12g]「Myasthenia gravis」違反の可能性。AEとして「MYASTHENIA GRAVIS AGGRAVATED」が報告されており、治験薬投与開始翌日に発現していることから、被験者が治験参加前から重症筋無力症を有していた可能性が疑われる。もし既往として存在した場合、除外基準違反となり、参加者の安全性に重大なリスクをもたらした可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [12g]
        *   **根拠:** AE「MYASTHENIA GRAVIS AGGRAVATED」の報告。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MYASTHENIA GRAVIS AGGRAVATED'
            *   MHドメインには重症筋無力症の記載なし。

    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[5] CNS imaging、[16b] Screening ECG、[28b] Folate、[29b] Syphilis screening、[30b] A1Cに関するデータが提供されておらず、これらの基準を満たしていたか確認できない。特にCNS imagingとScreening ECGはアルツハイマー病の診断確定や心血管リスク評価に重要であり、これらの基準を満たさないまま登録された場合、参加者の安全性や試験の科学的妥当性に影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5], Section 3.4.2.2 Exclusion Criteria [16b], [28b], [29b], [30b]
        *   **根拠:** 関連する検査・評価データがJSONデータに含まれていない。
        *   **関連データ:** 関連データなし

    *   **指摘No.:** P-3
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[27b]「Laboratory test values exceeding the Lilly Reference Range III」違反の可能性。Screening時のUrate値(7.7 mg/dL)が提供された基準値上限(7.5 mg/dL)をわずかに超えている。ただし、プロトコルでは臨床的に意義がないと判断されれば登録可能とされており、Week 2で正常化していることから、逸脱ではない可能性が高い。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** Screening時のLBデータ。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'URATE'
            *   [Result or Finding in Original Units(LB.LBORRES)] = '7.7'
            *   [Original Units(LB.LBORRESU)] = 'mg/dL'
            *   [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '7.5'
            *   [Visit Number(LB.VISITNUM)] = 1 (SCREENING 1)
            *   [Study Day of Specimen Collection(LB.LBDY)] = -14

    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** Visit 2 (SCREENING 2) の実施日(Day -2)がPlanned Study Day (Visitdy = -1)から1日ずれている。Visit 4 (WEEK 2) の実施日(Day 8)がPlanned Study Day (Visitdy = 14)から6日ずれている。これらはプロトコルで規定されたスケジュールからの逸脱の可能性があるが、Visit 4のずれは早期中止によるものと考えられ、臨床的な影響は小さいと判断される。
        *   **プロトコル該当箇所:** Section 3.1 Schedule of Events (Attachment LZZT.1), Section 3.1 Visit Window (記載なし、ただし逸脱は発生)
        *   **根拠:** SVデータとTVデータの比較。
        *   **関連データ:**
            *   SVドメイン: VISITNUM=2, SVSTDTC='2012-12-10' (Day -2) / VISITNUM=4, SVSTDTC='2012-12-19' (Day 8)
            *   TVドメイン: VISITNUM=2, VISITDY=-1 / VISITNUM=4, VISITDY=14

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, P-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として「MYASTHENIA GRAVIS AGGRAVATED」が報告され、治験中止に至っています。被験者が治験参加前に重症筋無力症の既往を有していたかご確認ください。既往歴がある場合、除外基準[12g]違反の可能性があり、参加者の安全性に関わるため、詳細な情報（診断日、重症度、治療歴など）をお知らせください。
        *   **クエリ文面（英語）:** The AE 'MYASTHENIA GRAVIS AGGRAVATED' was reported, leading to study discontinuation. Please confirm if the subject had a medical history of Myasthenia Gravis prior to study entry. If yes, this may be an Exclusion Criterion [12g] violation impacting subject safety. Provide details (diagnosis date, severity, treatment).
        *   **判断理由:** 除外基準違反の可能性があり、参加者の安全性に重大な影響を与えた可能性があるため、既往歴の有無を緊急に確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='MYASTHENIA GRAVIS AGGRAVATED', DS.DSTERM='ADVERSE EVENT', MHドメインに記載なし
            *   関連するプロトコル箇所: Section 3.4.2.2 [12g]
            *   関連する医学的知見: コリン作動薬による重症筋無力症増悪リスク

    *   **クエリNo.:** Q-2 (関連指摘No.: D-1, M-2)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「WEIGHT DECREASED」について、2つのレコード(AESEQ=1, 5)が存在し、転帰が異なります（収集日「2012-12-19」では「NOT RECOVERED/NOT RESOLVED」、収集日「2013-01-08」では「RECOVERED/RESOLVED」）。これはフォローアップによる更新と思われますが、最終的な転帰が「RECOVERED/RESOLVED」で正しいかご確認ください。また、治験薬との関連性が「NONE」と評価されていますが、嘔吐のAEも考慮し、関連性評価について再考をお願いできますでしょうか。
        *   **クエリ文面（英語）:** Regarding AE 'WEIGHT DECREASED', two records (AESEQ=1, 5) exist with different outcomes ('NOT RECOVERED/NOT RESOLVED' on 2012-12-19, 'RECOVERED/RESOLVED' on 2013-01-08). Please confirm the final outcome is 'RECOVERED/RESOLVED'. Also, causality is 'NONE'; considering the vomiting AE, please reassess the relationship to study drug.
        *   **判断理由:** 同一有害事象の転帰が異なって記録されており、データの正確性を確認する必要がある。また、体重減少の関連性評価が医学的に疑問であり、安全性評価の妥当性を確認する必要がある。
        *   **判断根拠:**
            *   関連するデータ: AEドメイン AESEQ=1, 5 (AETERM='WEIGHT DECREASED', AEREL='NONE', AEOUTの不一致), AEドメイン AESEQ=3 (AETERM='VOMITING', AEREL='PROBABLE'), VSドメイン WEIGHTの変動
            *   関連する医学的知見: コリン作動薬の副作用（嘔吐、食欲不振）と体重減少の関連

    *   **クエリNo.:** Q-3 (関連指摘No.: D-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Demographicsドメインにて、計画された治療群コードが「Xan_Hi」であるのに対し、実際に割り付けられた治療群コードが「Xan_Lo」と記録されています。Exposureドメインの記録は「Xan_Lo」と一致しています。計画された治療群と実際に割り付けられた治療群が異なっている理由、およびどちらが正しい情報かご確認ください。
        *   **クエリ文面（英語）:** In the DM domain, Planned Arm Code is 'Xan_Hi' but Actual Arm Code is 'Xan_Lo'. EX domain data matches 'Xan_Lo'. Please clarify the reason for this discrepancy between planned and actual arm assignment and confirm the correct information.
        *   **判断理由:** Planned ArmとActual Armの不一致は、無作為化割付やデータ記録に関する重大な問題の可能性があり、試験の信頼性に影響するため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: DM.ARMCD='Xan_Hi', DM.ACTARMCD='Xan_Lo', EX.EXTRT='XANOMELINE', EX.EXDOSE=54

    *   **クエリNo.:** Q-4 (関連指摘No.: D-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 同意取得日（Date/Time of Informed Consent）が記録されていません。治験手順開始前に同意が取得されていることを確認するため、同意取得日をお知らせください。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (RFICDTC) is missing. Please provide the date to confirm consent was obtained before study procedures began, as required by GCP.
        *   **判断理由:** 同意取得日の記録はGCP遵守の観点から必須であり、欠損しているため確認が必要。
        *   **判断根拠:**
            *   関連するデータ: DM.RFICDTC='' (欠損)
            *   関連するプロトコル箇所: Section 5.1 Informed Consent
            *   関連する医学的知見: GCP要件

    *   **クエリNo.:** Q-5 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されている選択/除外基準の確認に必要な情報の一部（CNS imagingの結果、Screening時のECG結果など）が提供されていません。被験者の適格性を確認するために、これらの情報をご提出いただけますでしょうか。
        *   **クエリ文面（英語）:** Required information to confirm eligibility criteria is missing (e.g., CNS imaging results, Screening ECG results). Please provide this information to verify subject eligibility per protocol.
        *   **判断理由:** 選択/除外基準の遵守は参加者の安全性と試験の妥当性に不可欠であり、確認に必要なデータが欠損しているため提出を依頼する必要がある。
        *   **判断根拠:**
            *   関連するデータ: 関連データ欠損
            *   関連するプロトコル箇所: Section 3.4.2.1 [5], Section 3.4.2.2 [16b], [28b], [29b], [30b]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-3)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 2 (Day 8) において、血小板数(Platelet)がベースライン(Day -14)から減少している（222 G/L -> 177 G/L）。基準値内ではあるが、減少傾向として留意する。他の血液系パラメータに異常はなく、治験薬投与期間も短いため、現時点では臨床的に重大な懸念とは判断しないが、同様の傾向が他の症例で見られないか注視する。
        *   **判断理由:** 減少は見られるものの基準値内であり、他のデータとの組み合わせで明らかなリスクを示唆するものではないため、医療機関への問い合わせは不要と判断。ただし、安全性監視の一環として内部で記録・注視する。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン Platelet値 (LBSEQ=29, 63)
            *   関連する医学的知見: 血小板数の変動要因

    *   **確認事項No.:** I-2 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHドメインにおいて、一部の既往歴（難聴、白内障、指の裂傷）の開始日(MH.MHSTDTC)が欠損している。これらの既往歴は主要評価項目や安全性に大きな影響はないと考えられるため、クエリ発行は不要とするが、データ欠損として記録する。
        *   **判断理由:** 欠損しているが、臨床的重要性は低いと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: MHドメイン MHSEQ=1, 2, 3 の MHSTDTC

    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/Medical Monitor
        *   **疑義事項/確認内容:** Screening時のUrate値が基準値上限をわずかに超えているが、プロトコル上、臨床的に意義がないと判断されれば登録可能である。Week 2で正常化しており、臨床的に問題なかった可能性が高い。除外基準違反ではないと判断された記録がソースドキュメントにあるか、必要に応じて確認する。
        *   **判断理由:** 軽微な基準値逸脱であり、プロトコルで許容される可能性があるため、緊急のクエリは不要。内部での確認事項とする。
        *   **判断根拠:**
            *   関連するデータ: LBドメイン Urate値 (LBSEQ=34, 66)
            *   関連するプロトコル箇所: Section 3.4.2.2 [27b]

    *   **確認事項No.:** I-4 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** Visit 2およびVisit 4の実施日がPlanned Study Dayからずれている。Visit 4のずれは早期中止に伴うものと考えられる。Visit 2のずれは1日であり、臨床的な影響は小さいと判断される。プロトコル逸脱として記録するが、クエリ発行は不要とする。
        *   **判断理由:** ずれの理由が推測可能であり、臨床的な影響が小さいと判断されるため。
        *   **判断根拠:**
            *   関連するデータ: SVドメイン、TVドメイン、DSドメイン
            *   関連するプロトコル箇所: Section 3.1 Schedule of Events (Attachment LZZT.1)

---

# [01-704-1008]のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
76歳、女性、人種はWHITE、民族はNOT HISPANIC OR LATINO。治験実施国はUSAであり、実際に割り付けられた治療群はXanomeline High Doseであった。主要な既往歴として、アルツハイマー病（2011年10月17日診断）、頭痛（MILD）、難聴（MILD）、甲状腺機能低下症（MILD）、右白内障摘出術（2012年7月21日実施）、乳房生検（正常、2012年1月実施）、虫垂切除術（1956年実施）が報告されている。教育レベルは12年であった。治験薬は2013年1月13日（Day 1）に開始され、2013年2月21日（Day 40）に最終投与された。有害事象により2013年2月25日（Day 44）に治験を中止した。

*   **イベント推移:**

|日付（YYYY年MM月DD日）|Study Day (Visit名)|イベント内容|
|:---|:---|:---|
|2012年06月01日|Day -225 (N/A)|有害事象「TREMOR IN HANDS, LEGS」(MILD) 発現 (治験開始前、未回復)|
|2012年06月01日|Day -225 (N/A)|有害事象「MUSCLE STIFFNESS」(MODERATE) 発現 (治験開始前、未回復、中止理由として関連付け)|
|2012年06月01日|Day -225 (N/A)|有害事象「SLOWNESS OF MOVEMENT」(SEVERE) 発現 (治験開始前)|
|2012年11月25日|Day -49 (SCREENING 1?)|Bilirubin (BILI) 高値 (1.3 mg/dL, 基準値上限 1.2)|
|2012年11月25日|Day -49 (SCREENING 1?)|Thyrotropin (TSH) 低値 (0.24 uIU/mL, 基準値下限 0.32)|
|2013年01月06日|Day -7 (SCREENING 1)|ベースライン評価開始。Systolic BP 168 mmHg (Supine)。Pulse 58 bpm (Supine)。|
|2013年01月06日|Day -7 (UNSCHEDULED 1.1)|Bilirubin (BILI) 正常化 (0.9 mg/dL)。TSH 正常化 (0.51 uIU/mL)。|
|2013年01月13日|Day 1 (BASELINE)|治験薬 Xanomeline 54 mg Patch 投与開始。ADAS-Cog(11) スコア: 15。NPI-X Total スコア: 2 (Anxiety スコア: 2)。Systolic BP 150 mmHg (Supine)。Pulse 58 bpm (Supine)。|
|2013年01月28日|Day 16 (WEEK 2)|NPI-X Total スコア: 0 (Anxiety スコア: 0)。|
|2013年01月29日|Day 17 (N/A)|治験薬 Xanomeline 81 mg Patch に増量。|
|2013年02月07日|Day 26 (N/A)|併用薬 Synthroid (Levothyroxine) 投与終了。|
|2013年02月09日|Day 28 (WEEK 4)|Protein (PROT) 低値 (5.8 g/dL, 基準値下限 6.0)。Urate (URATE) 低値 (2.4 mg/dL, 基準値下限 2.5)。NPI-X Total スコア: 4 (Anxiety スコア: 4)。|
|2013年02月21日|Day 40 (N/A)|有害事象「SLOWNESS OF MOVEMENT」回復。治験薬 Xanomeline 81 mg Patch 最終投与。|
|2013年02月25日|Day 44 (WEEK 6)|治験中止 (理由: ADVERSE EVENT)。Creatine Kinase (CK) 高値 (189 U/L, 基準値上限 169)。ADAS-Cog(11) スコア: 21 (ベースラインから悪化)。CIBIC+ スコア: 5 (Minimal worsening)。NPI-X Total スコア: 9 (Anxiety スコア: 9) (ベースラインから悪化)。Pulse 56 bpm (Supine), 52 bpm (Standing 1 min) (徐脈傾向)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「SLOWNESS OF MOVEMENT」(AESEQ=2) は治験開始前 (Day -225) に発現したと記録されているが、Requires or Prolongs Hospitalization (AESHOSP) が 'Y' となっている。治験期間中に回復 (Day 40) していることから、治験期間中の入院の可能性が高い。入院理由、期間、治験薬との関連性 (AEREL='NONE' と記録) の評価が妥当か、医学的に再評価が必要である。治験開始前の事象に入院フラグが付与されているデータ自体の信頼性にも疑問がある。
        *   **根拠:** 重篤な情報である入院と有害事象の開始日・関連性評価の間に矛盾があり、参加者の安全性評価に重大な影響を与える可能性がある。ムスカリン作動薬はパーキンソン症状（動作緩慢など）を悪化させる可能性も考慮すべき。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'SLOWNESS OF MOVEMENT'
            *   [Sequence Number(AE.AESEQ)] = 2
            *   [Severity/Intensity(AE.AESEV)] = 'SEVERE'
            *   [Requires or Prolongs Hospitalization(AE.AESHOSP)] = 'Y'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-06-01'
            *   [Study Day of Start of Adverse Event(AE.AESTDY)] = -225
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-02-21'
            *   [Study Day of End of Adverse Event(AE.AEENDY)] = 40
            *   [Causality(AE.AEREL)] = 'NONE'
            *   [Date/Time of First Study Treatment(DM.RFXSTDTC)] = '2013-01-13'

    *   **指摘No.:** M-2
        *   **重要度:** Critical
        *   **内容:** Day 44に有害事象 (ADVERSE EVENT) を理由に治験を中止しているが、中止の直接的な原因となった有害事象が不明確である。RELRECでは治験開始前 (Day -225) から持続している「MUSCLE STIFFNESS」(AESEQ=3, Moderate, 未回復) が中止理由 (DSSEQ=1) と関連付けられているが、これが中止の主たる理由とは考えにくい。中止日 (Day 44) にCreatine Kinase (CK) の上昇 (189 U/L) が認められており、これが中止に関連した可能性も考えられる。中止理由の特定と、その医学的評価の妥当性を確認する必要がある。
        *   **根拠:** 治験中止という重要な決定の根拠が不明確であり、安全性評価の信頼性に重大な影響を与える。CK上昇と中止の関連も評価が必要。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-02-25'
            *   [Study Day of Start of Disposition Event(DS.DSSTDY)] = 44
            *   [Sequence Number(DS.DSSEQ)] = 1
            *   [Relationship Identifier(RELREC.RELID)] = '01-704-1008-E05' (AE.AESEQ=3 と DS.DSSEQ=1 を関連付け)
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MUSCLE STIFFNESS'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-06-01'
            *   [Outcome of Adverse Event(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 44
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 189
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'

    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Week 6 (Day 44、中止日) にCreatine Kinase (CK) が基準値上限を超えて上昇 (189 U/L, 基準値上限 169 U/L) している。筋肉関連の有害事象は報告されていないが、治験開始前から持続している「MUSCLE STIFFNESS」(Moderate) との関連、または治験薬との関連の可能性について医学的な評価が必要である。
        *   **根拠:** 基準値を超える検査値異常であり、中止理由との関連も否定できないため、安全性評価上重要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CK'
            *   [Study Day of Specimen Collection(LB.LBDY)] = 44
            *   [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 189
            *   [Standard Units(LB.LBSTRESU)] = 'U/L'
            *   [Reference Range Upper Limit-Std Units(LB.LBSTNRHI)] = 169
            *   [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MUSCLE STIFFNESS' (AESEQ=3)

    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Week 6 (Day 44、中止日) のバイタルサイン測定において、立位1分後の脈拍数が52 bpmと徐脈傾向を示している。ベースライン時 (立位1分後 66 bpm) と比較しても低下している。Xanomelineはムスカリン作動薬であり徐脈のリスクがあるため、この徐脈の臨床的意義について評価が必要である。プロトコルでは心血管系の安全性を重視しており、徐脈（50 bpm未満）は除外/中止基準に関連する可能性がある。
        *   **根拠:** 治験薬の薬理作用と関連しうる所見であり、プロトコルで重要視されている心血管系の安全性評価に関連するため。
        *   **関連データ:**
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE'
            *   [Study Day of Vital Signs(VS.VSDY)] = 44
            *   [Visit Name(VS.VISIT)] = 'WEEK 6'
            *   [Planned Time Point Name(VS.VSTPT)] = 'AFTER STANDING FOR 1 MINUTE'
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 52
            *   [Standard Units(VS.VSSTRESU)] = 'BEATS/MIN'
            *   [Vital Signs Test Short Name(VS.VSTESTCD)] = 'PULSE' (Baseline, Day 1)
            *   [Numeric Result/Finding in Standard Units(VS.VSSTRESN)] = 66 (Standing 1 min)

    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** 主要評価項目であるADAS-Cog(11)およびCIBIC+、副次評価項目であるNPI-X Total Score、DADスコア（一部）が、ベースラインからWeek 6にかけて悪化を示している。Xanomeline High Dose群に割り付けられているにも関わらず有効性が示唆されず、むしろ悪化している点は医学的に懸念される。Phase II試験であることを考慮しても、期待される効果からの逸脱であり、薬剤の効果や用量設定の妥当性について疑問が生じる。
        *   **根拠:** 試験の主要な目的である有効性評価において、期待とは逆の結果が示唆されており、試験結果の解釈に影響を与える可能性がある。
        *   **関連データ:**
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Study Day of Finding(QS.QSDY)] = 1, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 15
            *   [Question Short Name(QS.QSTESTCD)] = 'ACTOT', [Study Day of Finding(QS.QSDY)] = 44, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 21
            *   [Question Short Name(QS.QSTESTCD)] = 'CIBIC', [Study Day of Finding(QS.QSDY)] = 44, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 5
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Study Day of Finding(QS.QSDY)] = 1, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 2
            *   [Question Short Name(QS.QSTESTCD)] = 'NPTOT', [Study Day of Finding(QS.QSDY)] = 44, [Numeric Finding in Standard Units(QS.QSSTRESN)] = 9
            *   DAD関連データ (DAITM24, DAITM31, DAITM36)

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「SLOWNESS OF MOVEMENT」(AESEQ=2) の開始日 (AESTDTC='2012-06-01') が治験薬初回投与日 (DM.RFXSTDTC='2013-01-13') より前であるにも関わらず、入院フラグ (AESHOSP) が 'Y' となっている。治験期間中に回復 (AEENDTC='2013-02-21') していることから、治験期間中の入院の可能性が高いが、開始日の記録と矛盾する。この不整合は、事象の評価（特に治験薬との関連性）や安全性の解釈に重大な影響を与えうる。
        *   **根拠:** 重篤な情報である入院とイベント発生日の記録に矛盾があり、データの信頼性を損なう。
        *   **関連データ:**
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'SLOWNESS OF MOVEMENT'
            *   [Sequence Number(AE.AESEQ)] = 2
            *   [Requires or Prolongs Hospitalization(AE.AESHOSP)] = 'Y'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-06-01'
            *   [End Date/Time of Adverse Event(AE.AEENDTC)] = '2013-02-21'
            *   [Date/Time of First Study Treatment(DM.RFXSTDTC)] = '2013-01-13'

    *   **指摘No.:** D-2
        *   **重要度:** Critical
        *   **内容:** Dispositionドメインで中止理由が「ADVERSE EVENT」(DSSEQ=1) と記録されているが、AEドメインのデータおよびRELRECドメインの情報から、中止の直接原因となったAEを明確に特定できない。RELRECでは治験開始前の事象「MUSCLE STIFFNESS」(AESEQ=3) が関連付けられているが、これが中止理由としては医学的に疑問が残る。中止決定の根拠となるデータが不明確である。
        *   **根拠:** 中止理由という重要な情報の根拠データが不明確であり、安全性評価の妥当性判断に影響する。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Sequence Number(DS.DSSEQ)] = 1
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-02-25'
            *   [Relationship Identifier(RELREC.RELID)] = '01-704-1008-E05'
            *   [Sequence Number(AE.AESEQ)] = 3
            *   [Reported Term for the Adverse Event(AE.AETERM)] = 'MUSCLE STIFFNESS'
            *   [Start Date/Time of Adverse Event(AE.AESTDTC)] = '2012-06-01'

    *   **指摘No.:** D-3
        *   **重要度:** Minor
        *   **内容:** SUPPAEドメインにおいて、治験薬投与開始前 (AESTDTC < DM.RFXSTDTC) に発現した有害事象 (AESEQ=1, 2, 3) に対しても Treatment Emergent Flag (QNAM='AETRTEM', QVAL='Y') が付与されている。通常、Treatment Emergent AEは治験薬投与開始後に発現または悪化した事象を指すため、データの定義と実際のフラグ付けに乖離がある可能性がある。
        *   **根拠:** データ定義の一貫性に関する問題。医学的評価への直接的な影響は限定的かもしれないが、解析時の集計等に影響する可能性がある。
        *   **関連データ:**
            *   SUPPAEデータ (QNAM='AETRTEM', QVAL='Y' for AESEQ=1, 2, 3)
            *   AEデータ (AESTDTC for AESEQ=1, 2, 3)
            *   DMデータ (DM.RFXSTDTC='2013-01-13')

    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** プロトコルで規定されているECGおよびAmbulatory ECGのデータが提供されていない。これらの検査は心血管系の安全性評価に不可欠であり、データ欠損は安全性評価の信頼性を損なう。
        *   **根拠:** プロトコルで規定された重要な安全性評価データが欠損している。
        *   **関連データ:**
            *   ECG, EG ドメインデータなし

    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** LBドメインにおいて、Screening Visit 1 (SV.SVSTDTC='2013-01-06', Day -7) に関連付けられているはずのデータの一部が、LBDTC='2012-11-25' (Day -49) となっている。データの採取日とVisitの紐付けが不正確である可能性があり、データのトレーサビリティに影響する。
        *   **根拠:** データの日付とVisit情報に不整合があり、データの品質に関わる問題。
        *   **関連データ:**
            *   LBデータ (LBDTC='2012-11-25T13:05' for VISITNUM=1)
            *   SVデータ (SVSTDTC='2013-01-06' for VISITNUM=1)

    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** 併用薬 Synthroid (Levothyroxine) が治験期間中 (Day 26) に中止されているが、中止理由が記録されていない。
        *   **根拠:** データの完全性に関する問題。
        *   **関連データ:**
            *   [Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'SYNTHROID'
            *   [End Date/Time of Medication(CM.CMENDTC)] = '2013-02-07'
            *   [Study Day of End of Medication(CM.CMENDY)] = 26

    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** EXドメインで示される治験薬の投与期間（54mg: Day 1-16, 81mg: Day 17-40）と、TA/TEドメインで示唆されるHigh Dose群の計画された投与 Element の期間が一致しない。
        *   **根拠:** 計画データと実施データの間の不整合。
        *   **関連データ:**
            *   EXデータ (EXDOSE, EXSTDY, EXENDY)
            *   TA/TEデータ (ETCD, ELEMENT, TEDUR for ARMCD='Xan_Hi')

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Minor
        *   **逸脱の可能性:** スクリーニング時の臨床検査値異常（Bilirubin高値、TSH低値）が除外基準[27b], [28b]に抵触する可能性がある。プロトコルでは、臨床的に意義がないと判断された場合は登録可能とされているが、その判断と記録が行われたか不明。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b], [28b]
        *   **根拠:** 除外基準に抵触する可能性のある検査値異常が確認されたが、登録継続の判断根拠が不明。ただし、ベースラインで正常化しているため重要度は低いと判断。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'BILI', [Result or Finding in Original Units(LB.LBORRES)] = '1.3', [Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.2', [Study Day of Specimen Collection(LB.LBDY)] = -49
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'TSH', [Result or Finding in Original Units(LB.LBORRES)] = '0.24', [Reference Range Lower Limit in Orig Unit(LB.LBORNRLO)] = '0.32', [Study Day of Specimen Collection(LB.LBDY)] = -49

    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコルで規定されたECGおよびAmbulatory ECG検査が実施されなかった、あるいはデータが収集されなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.9.3.4.2 Cardiovascular Safety Measures, Attachment LZZT.1 Schedule of Events
        *   **根拠:** 心血管系の安全性評価に関する重要な検査の実施状況が不明。
        *   **関連データ:**
            *   ECG, EG ドメインデータなし

    *   **指摘No.:** P-3
        *   **重要度:** Critical
        *   **逸脱の可能性:** 有害事象による中止判断の根拠が不明確である。RELRECで関連付けられているAE#3は治験開始前の事象であり、中止基準を満たすか疑問。中止日 (Day 44) のCK上昇が真の理由である可能性もあるが、記録と一致しない。中止基準の適用が適切に行われたか確認が必要。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** 治験中止という重要な判断の根拠が不明確であり、プロトコル遵守および安全性評価の妥当性に疑義がある。
        *   **関連データ:**
            *   [Standardized Disposition Term(DS.DSDECOD)] = 'ADVERSE EVENT'
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-02-25'
            *   RELREC, AE, LB関連データ (M-2, D-2参照)

    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコルでは有害事象による中止決定後、用量を54mgに漸減して中止診察まで継続すると規定されているが、EXデータではDay 40に81mg投与が終了しており、規定通りの漸減投与が行われなかった可能性がある。
        *   **プロトコル該当箇所:** Section 3.10.1 Discontinuations
        *   **根拠:** 中止時の投与手順に関するプロトコルからの逸脱の可能性。
        *   **関連データ:**
            *   [End Date/Time of Treatment(EX.EXENDTC)] = '2013-02-21' (for EXDOSE=81)
            *   [Study Day of End of Treatment(EX.EXENDY)] = 40
            *   [Start Date/Time of Disposition Event(DS.DSSTDTC)] = '2013-02-25'

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「SLOWNESS OF MOVEMENT」（AESEQ=2）について、開始日が治験薬投与開始前の「2012-06-01」と記録されていますが、「Requires or Prolongs Hospitalization」が「Y」となっています。この入院は治験期間中に発生したものでしょうか？ もし治験期間中の入院であれば、正確な入院期間と入院理由、および治験薬との関連性について再評価をお願いします。開始日の記録が正しいかどうかもご確認ください。参加者の安全性評価とデータの正確性確保のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Regarding AE 'SLOWNESS OF MOVEMENT' (AESEQ=2), AESTDTC is '2012-06-01' (pre-study), but AESHOSP is 'Y'. Did hospitalization occur during the study period? If yes, please provide exact dates, reason for hospitalization, and reassess causality (AEREL). Please also confirm the AESTDTC. Clarification needed for patient safety assessment and data accuracy.
        *   **判断理由:** 重篤な情報である入院と有害事象の記録に矛盾があり、参加者の安全性評価およびデータの信頼性に重大な影響を与えるため。
        *   **判断根拠:**
            *   関連するデータ: AE.AETERM='SLOWNESS OF MOVEMENT', AE.AESEQ=2, AE.AESHOSP='Y', AE.AESTDTC='2012-06-01', AE.AEENDTC='2013-02-21', AE.AEREL='NONE', DM.RFXSTDTC='2013-01-13'
            *   関連するプロトコル箇所: Section 3.9.3.2.2 Serious Adverse Events
            *   関連する医学的知見: データ間の矛盾、SAE報告の正確性

    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-2, P-3)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 本症例はStudy Day 44に有害事象により治験を中止していますが、中止の直接的な原因となった有害事象が記録から明確に判断できません。RELRECでは治験開始前から持続している「MUSCLE STIFFNESS」(AESEQ=3)が関連付けられていますが、これが中止理由でしょうか？ あるいは、中止日に認められたCreatine Kinase高値 (189 U/L) が中止判断に関与していますでしょうか？ 中止に至った具体的な有害事象とその評価について詳細をお知らせください。安全性評価の妥当性確認のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Subject discontinued due to AE on Day 44 (DS.DSDECOD='ADVERSE EVENT'). However, the specific AE causing discontinuation is unclear. RELREC links to pre-existing 'MUSCLE STIFFNESS' (AESEQ=3). Was this the reason, or was the elevated CK (189 U/L) on Day 44 involved? Please clarify the specific AE leading to discontinuation and provide details of the assessment. Needed for safety evaluation validity.
        *   **判断理由:** 治験中止の根拠が不明確であり、安全性評価の信頼性に重大な影響を与えるため。
        *   **判断根拠:**
            *   関連するデータ: DS.DSDECOD='ADVERSE EVENT', DS.DSSTDTC='2013-02-25', RELREC.RELID='01-704-1008-E05', AE.AESEQ=3, AE.AETERM='MUSCLE STIFFNESS', LB.LBTESTCD='CK', LB.LBSTRESN=189, LB.LBDY=44
            *   関連するプロトコル箇所: Section 3.10.1 Discontinuations
            *   関連する医学的知見: 中止理由の明確化の必要性

    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 44に測定されたCreatine Kinaseが「189 U/L」と基準値上限 (169 U/L) を超えていますが、このCK上昇の臨床的意義について評価をお願いします。原因として考えられること（例：筋肉関連の症状、運動、薬剤の影響など）があれば追記してください。
        *   **クエリ文面（英語）:** On Study Day 44, Creatine Kinase (CK) was 189 U/L (ULN 169 U/L). Please assess the clinical significance of this elevation. If known, please provide potential causes (e.g., muscle symptoms, exercise, drug effect).
        *   **判断理由:** 基準値を超える検査値異常であり、中止理由との関連も否定できないため、安全性評価上確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='CK', LB.LBDY=44, LB.LBSTRESN=189, LB.LBSTNRHI=169, LB.LBNRIND='HIGH'
            *   関連するプロトコル箇所: Section 3.9.3.3 Clinical Laboratory Tests
            *   関連する医学的知見: CK上昇の原因検索の必要性

    *   **クエリNo.:** Q-4 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Study Day 44のバイタルサイン測定において、立位1分後のPulse Rateが「52 beats/min」と徐脈傾向を認めています。この徐脈の臨床的意義について評価をお願いします。治験薬との関連性についてもご検討ください。
        *   **クエリ文面（英語）:** On Study Day 44, Pulse Rate after standing for 1 minute was 52 beats/min, indicating bradycardia tendency. Please assess the clinical significance of this finding and consider its relationship to the study drug.
        *   **判断理由:** 治験薬の薬理作用と関連しうる所見であり、プロトコルで重要視されている心血管系の安全性評価に関連するため。
        *   **判断根拠:**
            *   関連するデータ: VS.VSTESTCD='PULSE', VS.VSDY=44, VS.VSTPT='AFTER STANDING FOR 1 MINUTE', VS.VSSTRESN=52
            *   関連するプロトコル箇所: Section 3.9.3.4.1 Vital Sign Determination, Section 3.9.4 Safety Monitoring
            *   関連する医学的知見: ムスカリン作動薬による徐脈のリスク

    *   **クエリNo.:** Q-5 (関連指摘No.: D-4, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているECG検査（Visit 4, 5, 7）およびAmbulatory ECG検査（Visit 2）のデータが確認できません。これらの検査は実施されましたでしょうか？ 実施された場合は、結果をご提供ください。実施されなかった場合は、その理由をお知らせください。心血管系の安全性評価のため、ご確認をお願いいたします。
        *   **クエリ文面（英語）:** Data for protocol-required ECG (Visits 4, 5, 7) and Ambulatory ECG (Visit 2) are missing. Were these tests performed? If yes, please provide the results. If not performed, please provide the reason. Confirmation needed for cardiovascular safety assessment.
        *   **判断理由:** プロトコルで規定された重要な安全性評価の実施状況が不明であり、確認が必要なため。
        *   **判断根拠:**
            *   関連するデータ: ECG, EG ドメインデータなし
            *   関連するプロトコル箇所: Section 3.9.3.4.2 Cardiovascular Safety Measures, Attachment LZZT.1 Schedule of Events

    *   **クエリNo.:** Q-6 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** スクリーニング時の検査結果について、Bilirubinが「1.3 mg/dL」（基準値上限 1.2）、TSHが「0.24 uIU/mL」（基準値下限 0.32）と基準範囲外でしたが、プロトコル（Section 3.4.2.2 [27b], [28b]）に基づき、臨床的に意義がないと判断され登録が継続された記録はありますでしょうか？ ご確認をお願いします。
        *   **クエリ文面（英語）:** Screening labs showed Bilirubin 1.3 mg/dL (ULN 1.2) and TSH 0.24 uIU/mL (LLN 0.32), outside normal range. Was clinical significance assessed and documented as per protocol (Sec 3.4.2.2 [27b],[28b]) allowing enrollment? Please confirm.
        *   **判断理由:** 除外基準に抵触する可能性のある検査値異常に対する、プロトコルで要求される評価・記録の有無を確認するため。
        *   **判断根拠:**
            *   関連するデータ: LB.LBTESTCD='BILI', LB.LBORRES='1.3', LB.LBORNRHI='1.2'; LB.LBTESTCD='TSH', LB.LBORRES='0.24', LB.LBORNRLO='0.32' (at Screening)
            *   関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b], [28b]

    *   **クエリNo.:** Q-7 (関連指摘No.: P-4)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 本症例はStudy Day 44に治験を中止していますが、プロトコル（Section 3.10.1）で規定されている中止時の治験薬漸減投与（54mgに減量して中止診察まで継続）は実施されましたでしょうか？ 投与記録をご確認ください。
        *   **クエリ文面（英語）:** Subject discontinued on Day 44. Was the dose tapered down to 54mg until the early termination visit as per protocol (Sec 3.10.1)? Please confirm dosing records.
        *   **判断理由:** プロトコルで規定された中止時の手順が遵守されたか確認するため。
        *   **判断根拠:**
            *   関連するデータ: EX.EXENDTC='2013-02-21' (for EXDOSE=81), DS.DSSTDTC='2013-02-25'
            *   関連するプロトコル箇所: Section 3.10.1 Discontinuations

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-3)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 治験薬投与開始前に発現したAE (AESEQ=1, 2, 3) にTreatment Emergent Flag (AETRTEM='Y') が付与されている。SAP等でTreatment Emergentの定義を確認し、フラグ付与ロジックが適切か検証する。
        *   **判断理由:** データ定義とフラグ付与ロジックの内部確認が必要。医療機関への問い合わせは不要。
        *   **判断根拠:**
            *   関連するデータ: SUPPAE, AE, DMデータ (D-3参照)

    *   **確認事項No.:** I-2 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** LBドメインの一部データ (LBDTC='2012-11-25') がVisit 1 (SVSTDTC='2013-01-06') に紐づいている可能性がある。データのVisit帰属が正しいか、eDTデータ等との照合を含めて確認する。
        *   **判断理由:** データ品質に関する内部確認が必要。
        *   **判断根拠:**
            *   関連するデータ: LB, SVデータ (D-5参照)

    *   **確認事項No.:** I-3 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** 併用薬 Synthroid がDay 26に中止されているが理由不明。他のデータ（AE, LB等）から中止理由が推測できないか確認する。医療機関への問い合わせは必須ではないが、可能であれば確認を試みる。
        *   **判断理由:** データの完全性に関する確認。直接的なリスクは低いと判断。
        *   **判断根拠:**
            *   関連するデータ: CMデータ (D-6参照)

    *   **確認事項No.:** I-4 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** EXドメインの投与期間とTA/TEドメインの計画期間に不一致が見られる。計画からの逸脱として記録・管理する。
        *   **判断理由:** 計画と実施の差異に関する記録。
        *   **判断根拠:**
            *   関連するデータ: EX, TA, TEデータ (D-7参照)

---

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

