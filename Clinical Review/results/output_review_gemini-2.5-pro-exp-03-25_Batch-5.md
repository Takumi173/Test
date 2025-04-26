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