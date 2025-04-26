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