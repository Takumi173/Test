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