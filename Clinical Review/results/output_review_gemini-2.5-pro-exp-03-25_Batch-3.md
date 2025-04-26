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