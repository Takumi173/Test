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