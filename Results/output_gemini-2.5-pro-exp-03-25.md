# 01-704-1017のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 77歳、性別は男性、人種は白色人種、民族はヒスパニックまたはラティーノではない。本試験ではXanomeline High Dose群に割り付けられ、実際に同群の治験薬投与を受けた。居住国はUSA。

*   **イベント推移:**

|日付|Study Day, Visit|イベント内容|
|:---|:---|:---|
|2000年05月15日|N/A|既往歴: 心筋梗塞 (Myocardial Infarction) 発症|
|2006年12月16日|N/A|既往歴: 三枝バイパス移植術 (Triple vessel bypass graft) 実施|
|2011年03月27日|N/A|既往歴: アルツハイマー病 (Alzheimer's Disease) 発症 (Primary Diagnosis)|
|2013年09月20日|Day -16, Visit 1 (SCREENING 1)|既往歴として心疾患、性欲亢進、心電図ST上昇/低下、心筋梗塞、期外収縮 (いずれも軽度) を報告。MMSEスコア: 21点。Hachinski Ischemic Score: 0点。検査: クレアチニン 1.8 mg/dL (基準値上限超過)。バイタルサイン: 起立性低血圧の傾向あり (臥位 144/70 mmHg → 立位1分後 130/76 mmHg)。|
|2013年09月27日|Day -9, Visit 2 (SCREENING 2)|バイタルサイン: 起立性低血圧の傾向持続 (臥位 132/66 mmHg → 立位1分後 126/70 mmHg)。|
|2013年10月06日|Day 1, Visit 3 (BASELINE)|治験薬 Xanomeline 54 mg Patch (QD) 投与開始。ADAS-Cog(11) スコア: 27点。NPI-X Total スコア: 61点。バイタルサイン: 起立性低血圧の傾向持続 (臥位 144/70 mmHg → 立位1分後 120/66 mmHg)。併用薬 Premarin 0.625mg QOD 開始。|
|2013年10月19日|Day 14, Visit 4 (WEEK 2)|治験薬 Xanomeline 81 mg Patch (QD) へ増量 (Day 15から)。有害事象: 心筋梗塞 (軽度、非重篤、治験薬中止と記録あるが投与は継続、因果関係なし、Day 45に回復)。有害事象: 心室中隔欠損 (軽度、非重篤、因果関係なし、未回復)。有害事象: 脳梗塞後遺症 (重度、非重篤、因果関係なし、Day 44まで継続)。検査: BUN 29 mg/dL (基準値上限超過)、アルブミン 3.3 g/dL (基準値下限未満)。バイタルサイン: 血圧低下傾向 (臥位 112/60 mmHg)、徐脈傾向 (臥位 68 bpm)。NPI-X Total スコア: 22点。|
|2013年10月29日|Day 24|併用薬 Premarin 終了。|
|2013年11月01日|Day 27, Visit 5 (WEEK 4) (DS: FINAL LAB VISIT)|検査: アルブミン 3.4 g/dL (基準値下限未満)。|
|2013年11月05日|Day 31|有害事象: そう痒症 (軽度、非重篤、因果関係: Probable、Day 48に回復)。有害事象: 発疹 (軽度、非重篤、因果関係: Probable、Day 48に回復)。|
|2013年11月06日|Day 32|併用薬 Hydrocortisone topical 開始 (Rash/Pruritus治療目的と推察)。|
|2013年11月09日|Day 35, Visit 5 (WEEK 4)|バイタルサイン: 起立性低血圧持続 (臥位 124/66 mmHg → 立位1分後 110/60 mmHg)。NPI-X Total スコア: 38点。|
|2013年11月18日|Day 44|有害事象: 脳死 (重度、非重篤、因果関係なし、同日回復と記録)。治験薬 Xanomeline 81 mg Patch 投与終了。|
|2013年11月19日|Day 45|有害事象: 心筋梗塞 回復。|
|2013年11月22日|Day 48|有害事象: そう痒症 回復。有害事象: 発疹 回復。併用薬 Hydrocortisone topical 終了。|
|2013年11月24日|Day 50, Visit 7 (WEEK 6)|Disposition: 有害事象により試験中止。ADAS-Cog(11) スコア: 30点 (ベースラインから悪化)。CIBIC+ スコア: 4 (変化なし)。NPI-X Total スコア: 16点 (ベースラインから改善傾向だが変動あり、幻覚スコア1が出現)。バイタルサイン: 起立性低血圧持続 (臥位 132/60 mmHg → 立位1分後 114/60 mmHg)、徐脈傾向 (臥位 64 bpm)。|
|2013年12月06日|Day 62, Visit 101 (AE FOLLOW-UP)|試験参加終了。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** 有害事象「脳死 (Brain Death)」が重度 (Severe) かつ非重篤 (Not Serious) と評価され、さらに同日中に回復 (Recovered/Resolved) したと記録されている。これは医学的にあり得ない内容であり、極めて重大なデータ誤記または報告エラーが疑われる。参加者の状態に関する記録の信頼性に根本的な疑問が生じる。
        *   **根拠:** 「脳死」は定義上、不可逆的な全脳機能の喪失であり、回復することはあり得ない。また、脳死は最も重篤な状態であり、「非重篤」という評価は矛盾する。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'BRAIN DEATH'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'SEVERE'`
            *   `[有害事象の転帰(AEOUT)] = 'RECOVERED/RESOLVED'`
            *   `[有害事象終了日(AEENDTC)] = '2013-11-18'`
            *   `[有害事象終了日(Study Day)(AEENDY)] = 44`
    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** 有害事象「心筋梗塞 (Myocardial Infarction)」(Day 14発現) の評価に矛盾がある。軽度 (Mild) かつ非重篤 (Not Serious) と評価されているが、心筋梗塞は通常、重篤なイベントである。また、治験薬に対する処置 (Action Taken) が「治験薬中止 (DRUG WITHDRAWN)」と記録されているにも関わらず、因果関係 (Causality) は「なし (NONE)」と評価されている。これらの評価の医学的妥当性に疑問がある。既往歴 (2000年) に心筋梗塞があり、今回のイベントが再発なのか新規なのか、また治験薬との関連性について再評価が必要。
        *   **根拠:** 心筋梗塞は一般的に入院を要する重篤な状態であり、軽度/非重篤という評価は通常考えにくい。治験薬中止の判断と因果関係否定の評価が同時に存在するのは不自然。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'MYOCARDIAL INFARCTION'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'MILD'`
            *   `[治験薬に対する処置(AEACN)] = 'DRUG WITHDRAWN'`
            *   `[因果関係(AEREL)] = 'NONE'`
            *   `[有害事象開始日(Study Day)(AESTDY)] = 14`
            *   `[既往歴の報告用語(MH.MHTERM)] = 'MYOCARDIAL INFARCTION'`
            *   `[既往歴開始日(MH.MHSTDTC)] = '2000-05-15'`
    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** ベースライン時から起立性低血圧の傾向が見られ、治験薬投与開始後（特に81mgへの増量後）に血圧低下および徐脈の傾向が認められる。Xanomelineはムスカリン作動薬であり、これらの心血管系への影響（徐脈、血圧低下）は薬理作用として予期される可能性がある。Day 14に報告された心筋梗塞との関連も含め、治験薬の安全性プロファイルとして注意深く評価する必要がある。
        *   **根拠:** ムスカリン作動薬は副交感神経刺激作用を持ち、心拍数低下や血管拡張による血圧低下を引き起こす可能性がある。VSデータの経時的変化パターンがこれを示唆している。
        *   **関連データ:**
            *   VSドメインの血圧 (SYSBP, DIABP) および脈拍数 (PULSE) データ (特にSupineとStandingの比較、経時変化)
            *   EXドメインの投与記録 (EXTRT='XANOMELINE', EXDOSE=54, 81)
            *   AEドメインの心血管系イベント (Myocardial Infarction)
    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Day 50に「有害事象 (ADVERSE EVENT)」を理由に試験を中止しているが、原因となった具体的な有害事象が特定できない。RELRECデータではRash (軽度、回復済) と関連付けられているが、軽度の回復済みAEが中止理由となるのは考えにくい。Day 44に記録された「脳死」はデータ信頼性に問題があり、Day 14-45の「心筋梗塞」は回復済みと記録されている。中止理由の妥当性について確認が必要。
        *   **根拠:** 試験中止という重要な決定の根拠となる有害事象が不明確であり、データの解釈および安全性評価に影響を与える。
        *   **関連データ:**
            *   `[Dispositionの報告用語(DS.DSTERM)] = 'ADVERSE EVENT'`
            *   `[Disposition開始日(Study Day)(DS.DSSTDY)] = 50`
            *   RELRECドメインデータ (RELID='01-704-1017-E11')
            *   AEドメインデータ (AESEQ=1, 3, 5, 7など)
    *   **指摘No.:** M-5
        *   **重要度:** Major
        *   **内容:** 有効性評価指標であるADAS-Cog(11)スコアがベースラインの27点からWeek 6 (Day 50) で30点へと悪化している。また、CIBIC+スコアはWeek 6で4 (変化なし) であった。NPI-X Totalスコアはベースラインから改善傾向を示唆する可能性もあるが、評価時期によって変動が大きい。全体として、本症例において治験薬の有効性を示す明確なエビデンスはなく、むしろ認知機能の悪化が示唆されている。
        *   **根拠:** 主要評価項目であるADAS-Cogが悪化し、CIBIC+が不変であることは、有効性が認められない、あるいは疾患が進行している可能性を示す。
        *   **関連データ:**
            *   `[質問票項目短縮名(QS.QSTESTCD)] = 'ACTOT'`, `[質問票評価日(Study Day)(QS.QSDY)] = 1`, `[標準形式での文字結果(QS.QSSTRESC)] = '27'`
            *   `[質問票項目短縮名(QS.QSTESTCD)] = 'ACTOT'`, `[質問票評価日(Study Day)(QS.QSDY)] = 50`, `[標準形式での文字結果(QS.QSSTRESC)] = '30'`
            *   `[質問票項目短縮名(QS.QSTESTCD)] = 'CIBIC'`, `[質問票評価日(Study Day)(QS.QSDY)] = 50`, `[標準形式での文字結果(QS.QSSTRESC)] = '4'`
            *   QSドメインのNPI-X関連データ (NPTOT, NPITMxS)
    *   **指摘No.:** M-6
        *   **重要度:** Minor
        *   **内容:** 有害事象「脳梗塞後遺症 (Late effects of cerebral infarction)」が重度 (Severe) かつ非重篤 (Not Serious) と評価されている。重度の神経学的後遺症が非重篤と評価されることの妥当性について疑問がある。
        *   **根拠:** 一般的に、重度の神経学的後遺症は患者の機能に重大な影響を与え、重篤と評価されることが多い。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'SEVERE'`
    *   **指摘No.:** M-7
        *   **重要度:** Minor
        *   **内容:** 有害事象として「心室中隔欠損 (Ventricular Septal Defect)」が報告されている。これは通常、先天性疾患であり、医学的既往歴 (MH) として記録されるべき事象である可能性が高い。AEとしての報告が適切か確認が必要。
        *   **根拠:** 心室中隔欠損は構造的な心疾患であり、治験期間中に新たに発症する有害事象とは考えにくい。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'VENTRICULAR SEPTAL DEFECT'`
            *   `[有害事象開始日(Study Day)(AESTDY)] = 14`
    *   **指摘No.:** M-8
        *   **重要度:** Minor
        *   **内容:** Day 31に発現した発疹 (Rash) およびそう痒症 (Pruritus) に対し、Day 32からHydrocortisone外用薬が使用され、Day 48に両AEとも回復している。治験薬との関連はProbableと評価されており、プロトコル3.9.3.4で言及されている皮膚反応の可能性と、それに対する処置は時系列的に見て妥当と考えられる。
        *   **根拠:** AEの発現時期、併用薬の使用開始時期、AEの回復時期が整合している。
        *   **関連データ:**
            *   AEドメイン (AESEQ=5, 6, 7, 8)
            *   CMドメイン (CMTRT='HYDROCORTISONE, TOPICAL')
    *   **指摘No.:** M-9
        *   **重要度:** Minor
        *   **内容:** 検査値において、Screening時のクレアチニン高値、Week 2のBUN一過性高値、Week 2およびWeek 4のアルブミン低値が認められる。クレアチニンとBUNはその後正常化または基準値付近に戻っており、アルブミンの低下も軽度であるため、現時点での臨床的意義は限定的と考えられるが、腎機能や栄養状態の変動として留意すべき。
        *   **根拠:** 検査値の変動は認められるが、変動幅や持続期間から直ちに重大な問題とは判断し難い。
        *   **関連データ:**
            *   LBドメイン (LBTESTCD='CREAT', 'BUN', 'ALB')

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Critical
        *   **内容:** AEドメインの「脳死 (Brain Death)」(AESEQ=3) の記録において、重症度 (Severe)、重篤度 (Not Serious)、転帰 (Recovered/Resolved)、終了日 (Day 44) の組み合わせが論理的・医学的に破綻している。データの信頼性に極めて重大な問題がある。
        *   **根拠:** M-1の根拠と同じ。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'BRAIN DEATH'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'SEVERE'`
            *   `[有害事象の転帰(AEOUT)] = 'RECOVERED/RESOLVED'`
            *   `[有害事象終了日(AEENDTC)] = '2013-11-18'`
    *   **指摘No.:** D-2
        *   **重要度:** Major
        *   **内容:** AEドメインの「心筋梗塞 (Myocardial Infarction)」(AESEQ=1) の記録において、重症度 (Mild)、重篤度 (Not Serious)、治験薬に対する処置 (Drug Withdrawn)、因果関係 (None) の間に論理的な矛盾がある。また、治験薬に対する処置が「治験薬中止」と記録されているにも関わらず、EXドメインではDay 44まで治験薬が継続投与されている記録と矛盾する。
        *   **根拠:** M-2の根拠に加え、AEACNとEXデータの不整合。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'MYOCARDIAL INFARCTION'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'MILD'`
            *   `[治験薬に対する処置(AEACN)] = 'DRUG WITHDRAWN'`
            *   `[因果関係(AEREL)] = 'NONE'`
            *   EXドメインデータ (EXENDTC='2013-11-18')
    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** DSドメインで中止理由が「有害事象」(Day 50) と記録されているが、RELRECデータでは中止 (DSSEQ=1) と関連付けられているAEが「発疹 (Rash)」(AESEQ=5, 7) となっている。Rashは軽度でありDay 48に回復済みのため、Day 50の中止理由としては整合性が低い。他の重篤なAE（心筋梗塞、脳死）との関連も不明確であり、中止理由の記録に矛盾または不備がある可能性が高い。
        *   **根拠:** DSレコードとRELRECレコードで示唆される中止理由が、AEドメインの記録（重症度、転帰）と整合しない。
        *   **関連データ:**
            *   `[Dispositionの報告用語(DS.DSTERM)] = 'ADVERSE EVENT'`
            *   `[Disposition開始日(Study Day)(DS.DSSTDY)] = 50`
            *   RELRECドメインデータ (RELID='01-704-1017-E11')
            *   AEドメインデータ (AESEQ=5, 7, AEOUT='RECOVERED/RESOLVED', AEENDY=48)
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** QSドメインのNPI-Xにおいて、複数の項目でスコア (NPITMxS) と、その算出根拠となる頻度 (Frequency, NPITMxF) および重症度 (Severity, NPITMxV) の値との間に矛盾が見られる (例: NPITM11S Baseline=0 だが F=4, S=3)。これにより、算出されているNPI-X Total Score (NPTOT) の信頼性も低い。有効性評価の信頼性に影響を与える。
        *   **根拠:** スコアとその構成要素の値が計算上一致しない。
        *   **関連データ:**
            *   QSドメインのNPI-X関連データ (QSCAT='NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)')、特にNPITM11S, NPITM12S, NPTOTと対応するF, Vの値。
    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** AEドメインの「脳梗塞後遺症 (Late effects of cerebral infarction)」(AESEQ=4) の記録において、重症度 (Severe) と重篤度 (Not Serious) が矛盾している可能性がある。
        *   **根拠:** M-6の根拠と同じ。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'`
            *   `[重篤度(AESER)] = 'N'`
            *   `[重症度(AESEV)] = 'SEVERE'`
    *   **指摘No.:** D-6
        *   **重要度:** Minor
        *   **内容:** AEドメインの「心室中隔欠損 (Ventricular Septal Defect)」(AESEQ=2) の有害事象終了日 (AEENDTC) が欠損している。先天性疾患であり継続していると解釈可能だが、記録としては不完全。
        *   **根拠:** 必須ではないかもしれないが、日付変数に欠損がある。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'VENTRICULAR SEPTAL DEFECT'`
            *   `[有害事象終了日(AEENDTC)] = ''`
    *   **指摘No.:** D-7
        *   **重要度:** Minor
        *   **内容:** QSドメインのDAD評価において、ベースラインで「該当なし (NA)」と評価された項目 (DAITM04, DAITM30, DAITM31, DAITM32) が、Week 6で「いいえ (N)」と評価されている。評価基準の変更があったのか、あるいはデータ入力の誤りか確認が必要。
        *   **根拠:** 評価結果の経時変化として論理的でない可能性がある。
        *   **関連データ:**
            *   QSドメインのDAD関連データ (QSCAT='DISABILITY ASSESSMENT FOR DEMENTIA (DAD)')、特にQSTESTCD='DAITM04', 'DAITM30', 'DAITM31', 'DAITM32' のQSORRES/QSSTRESCの値。
    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** SVドメインのVisit 101 (AE FOLLOW-UP) の Planned Study Day of Visit (VISITDY) が欠損している。TVドメインでも対応するVISITDYはNull。
        *   **根拠:** タイミング変数に欠損がある。
        *   **関連データ:**
            *   `[Visit Number(SV.VISITNUM)] = 101`
            *   `[Planned Study Day of Visit(SV.VISITDY)] = null`
    *   **指摘No.:** D-9
        *   **重要度:** Minor
        *   **内容:** DMドメインの Date/Time of Informed Consent (RFICDTC) が欠損している。
        *   **根拠:** 重要な日付情報が欠損している。
        *   **関連データ:**
            *   `[Date/Time of Informed Consent(DM.RFICDTC)] = ''`

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[12a] (Stroke or vascular dementia) への抵触の可能性。MH/AEとして「脳梗塞後遺症」が報告されており、これが除外基準に該当しないか確認が必要。Hachinskiスコアは0点だが、後遺症の存在は評価が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [12] a)
        *   **根拠:** MH/AEデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'LATE EFFECTS OF CEREBRAL INFARCTION'`
            *   `[質問票項目短縮名(QS.QSTESTCD)] = 'MHITM10'`, `[標準形式での文字結果(QS.QSSTRESC)] = '0'` (Hachinski Score)
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[16b] (Evidence from ECG recording at screening of any listed condition) への抵触の可能性。MHとして「心電図ST上昇」「心電図ST低下」「期外収縮」が報告されており、Screening時のECG所見が除外基準に該当しなかったか確認が必要（ECGデータ自体は提供されていない）。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [16b]
        *   **根拠:** MHデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   `[既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0806'` (ST SEGMENT ELEVATED)
            *   `[既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_1153'` (ST SEGMENT DEPRESSED)
            *   `[既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_1608'` (SKIPPED BEATS / EXTRASYSTOLES)
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[17] (A history within the last 5 years of a serious cardiovascular disorder) への抵触の可能性。MHとして複数の心血管系既往歴（MI 2000年、Bypass 2006年）およびSignificant Pre-existing Condition（Cardiac disorder, MI, ST elevation/depression, Extrasystoles）が報告されている。5年以内の「Serious」な疾患に該当しなかったか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [17]
        *   **根拠:** MHデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   MHドメインの心血管系関連データ (MHCAT='SIGNIFICANT PRE-EXISTING CONDITION', MHBODSYS='CARDIAC DISORDERS', 'INVESTIGATIONS')
    *   **指摘No.:** P-4
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[27b] (Laboratory test values exceeding the Lilly Reference Range III) への抵触の可能性。Screening時のクレアチニン値 (1.8 mg/dL) がDefine.xml上の基準範囲 (0.8-1.6 mg/dL) を超えている。これがプロトコルで規定する「Lilly Reference Range III」を超えている場合、除外基準違反となる。Reference Range IIIの具体的な値と照合が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [27b]
        *   **根拠:** LBデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   `[Lab Test or Examination Short Name(LB.LBTESTCD)] = 'CREAT'`
            *   `[Visit Number(LB.VISITNUM)] = 1`
            *   `[Result or Finding in Original Units(LB.LBORRES)] = '1.8'`
            *   `[Reference Range Upper Limit in Orig Unit(LB.LBORNRHI)] = '1.6'`
    *   **指摘No.:** P-5
        *   **重要度:** Major
        *   **逸脱の可能性:** 除外基準[31b] v) (Estrogen supplements... stable for at least 3 months prior to enrollment) 違反の可能性。併用薬Premarin (Estrogen supplement) がDay 1から開始されており、3ヶ月間の安定投与期間の要件を満たしていない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [31b] v)
        *   **根拠:** CMデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   `[Reported Name of Drug, Med, or Therapy(CM.CMTRT)] = 'PREMARIN'`
            *   `[Start Date/Time of Medication(CM.CMSTDTC)] = '2013-10-06'`
            *   `[Study Day of Start of Medication(CM.CMSTDY)] = 1`
    *   **指摘No.:** P-6
        *   **重要度:** Major
        *   **逸脱の可能性:** AE「心筋梗塞」に対する処置記録と実際の投与記録の矛盾。AE記録では「治験薬中止 (DRUG WITHDRAWN)」とされているが、EXドメインではDay 44まで投与が継続されている。プロトコルで規定されたAE発生時の処置（中止基準など）が遵守されたか、あるいは記録が不正確である可能性。
        *   **プロトコル該当箇所:** Section 3.10.1 (Discontinuations)
        *   **根拠:** AEデータとEXデータの不整合。
        *   **関連データ:**
            *   `[報告された有害事象(AETERM)] = 'MYOCARDIAL INFARCTION'`
            *   `[治験薬に対する処置(AEACN)] = 'DRUG WITHDRAWN'`
            *   EXドメインデータ (EXENDTC='2013-11-18')
    *   **指摘No.:** P-7
        *   **重要度:** Major
        *   **逸脱の可能性:** Week 4のNPI-X評価がDay 35に実施されており、Planned Day 28から7日遅れている。プロトコル3.9で規定されたVisit Window (±3日) を逸脱している。
        *   **プロトコル該当箇所:** Section 3.9 (Visits 4, 5, 7, 8, and 13 should occur within 3 days of their scheduled date)
        *   **根拠:** QSデータの日付とプロトコルのスケジュール規定の照合。
        *   **関連データ:**
            *   `[Visit Number(QS.VISITNUM)] = 5` (Week 4)
            *   `[Planned Study Day of Visit(QS.VISITDY)] = 28`
            *   `[Study Day of Finding(QS.QSDY)] = 35` (NPI-X)
    *   **指摘No.:** P-8
        *   **重要度:** Major
        *   **逸脱の可能性:** Week 6の有効性評価 (ADAS-Cog, CIBIC+, DAD, NPI-X) がDay 50に実施されており、Planned Day 42から8日遅れている。プロトコル3.9で規定されたVisit Window (±3日) を逸脱している。
        *   **プロトコル該当箇所:** Section 3.9 (Visits 4, 5, 7, 8, and 13 should occur within 3 days of their scheduled date)
        *   **根拠:** QSデータの日付とプロトコルのスケジュール規定の照合。
        *   **関連データ:**
            *   `[Visit Number(QS.VISITNUM)] = 7` (Week 6)
            *   `[Planned Study Day of Visit(QS.VISITDY)] = 42`
            *   `[Study Day of Finding(QS.QSDY)] = 50`
    *   **指摘No.:** P-9
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[14] (A history of mental illness within the last 5 years) への抵触の可能性。MHとして「性欲亢進 (Libido increased)」(精神障害) が報告されている。これが除外基準に該当しないか確認が必要。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [14]
        *   **根拠:** MHデータとプロトコル除外基準の照合。
        *   **関連データ:**
            *   `[既往歴の報告用語(MH.MHTERM)] = 'VERBATIM_0608'` (LIBIDO INCREASED)
            *   `[Body System or Organ Class(MH.MHBODSYS)] = 'PSYCHIATRIC DISORDERS'`
    *   **指摘No.:** P-10
        *   **重要度:** Minor
        *   **逸脱の可能性:** 除外基準[28b] (Central laboratory test values below reference range for folate...) の確認不備の可能性。Screening時のFolate検査データが提供されていないため、基準を満たしていたか確認できない。
        *   **プロトコル該当箇所:** Section 3.4.2.2 [28b]
        *   **根拠:** プロトコルで要求される可能性のある検査データが欠損している。
        *   **関連データ:** LBドメインにFolateのデータなし。
    *   **指摘No.:** P-11
        *   **重要度:** Minor
        *   **逸脱の可能性:** 治験薬の増量タイミングについて、プロトコル本文での記載が不明瞭。EXデータではDay 15に増量されているが、これが計画通りか確認が必要。
        *   **プロトコル該当箇所:** Section 3.1, Figure LZZT.1, Section 3.6.2
        *   **根拠:** EXデータとプロトコル記載内容の照合。
        *   **関連データ:**
            *   EXドメインデータ (EXDOSE, EXSTDTC, EXENDTC)
            *   TAドメインデータ (ARMCD='Xan_Hi')
            *   TEドメインデータ (ETCD='HIS', 'HIM', 'HIE')
            *   SEドメインデータ
    *   **指摘No.:** P-12
        *   **重要度:** Minor
        *   **逸脱の可能性:** DSドメインに記録されている「FINAL LAB VISIT」(Visit 5, Day 27) が、プロトコル上の予定されたVisitではない可能性がある。Unscheduled Visitか、あるいはVisit 5の記録の一部か確認が必要。
        *   **プロトコル該当箇所:** Protocol Attachment LZZT.1 (Schedule of Events)
        *   **根拠:** DSデータとプロトコルのVisitスケジュールの照合。
        *   **関連データ:**
            *   `[Standardized Disposition Term(DS.DSDECOD)] = 'FINAL LAB VISIT'`
            *   `[Visit Number(DS.VISITNUM)] = 5`
            *   `[Study Day of Start of Disposition Event(DS.DSSTDY)] = 27`

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象として報告された「報告された有害事象」が「BRAIN DEATH」について、重症度が「SEVERE」、重篤度が「N」、転帰が「RECOVERED/RESOLVED」、終了日が「2013-11-18」と記録されています。脳死は回復不能な状態であり、重篤な事象です。記録内容が医学的にあり得ないため、当該イベントの詳細（実際のイベント、重症度、重篤度、転帰、日付）を至急確認し、修正をお願いします。患者様の状態に関する正確な情報把握と安全性評価のために不可欠です。
        *   **クエリ文面（英語）:** Regarding the reported AE Term 'BRAIN DEATH' (Severity='SEVERE', Serious='N', Outcome='RECOVERED/RESOLVED', End Date='2013-11-18'): This record is medically implausible as brain death is irreversible and serious. Please urgently verify and correct the details (actual event, severity, seriousness, outcome, dates). Accurate information is critical for patient safety assessment.
        *   **判断理由:** 報告されたイベントの内容が医学的にあり得ず、データの信頼性に重大な疑義があるため。患者の実際の状態と転帰を正確に把握する必要がある。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='BRAIN DEATH', AE.AESEV='SEVERE', AE.AESER='N', AE.AEOUT='RECOVERED/RESOLVED', AE.AEENDTC='2013-11-18']
            *   [関連する医学的知見: 脳死の定義と予後]
    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-2)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 有害事象「報告された有害事象」が「MYOCARDIAL INFARCTION」について、重症度が「MILD」、重篤度が「N」、治験薬に対する処置が「DRUG WITHDRAWN」、因果関係が「NONE」と記録されています。心筋梗塞の重症度/重篤度評価、および治験薬中止の判断と因果関係否定の評価に矛盾があるように思われます。既往歴にも心筋梗塞がありますが、今回のイベントの詳細（新規/再発、診断根拠、実際の重症度/重篤度、治験薬との関連性評価）について確認し、必要に応じて修正をお願いします。
        *   **クエリ文面（英語）:** Regarding the AE Term 'MYOCARDIAL INFARCTION' (Severity='MILD', Serious='N', Action Taken='DRUG WITHDRAWN', Causality='NONE'): There appear to be inconsistencies in the assessment. Please confirm details (new/recurrent, diagnosis basis, actual severity/seriousness, relationship to study drug) and revise if necessary. Patient has a history of MI.
        *   **判断理由:** 有害事象の評価（重症度、重篤度、処置、因果関係）に矛盾があり、医学的妥当性の確認が必要なため。安全性評価の正確性を担保する必要がある。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='MYOCARDIAL INFARCTION', AE.AESEV='MILD', AE.AESER='N', AE.AEACN='DRUG WITHDRAWN', AE.AEREL='NONE', MH.MHTERM='MYOCARDIAL INFARCTION']
            *   [関連する医学的知見: 心筋梗塞の一般的評価]
    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** バイタルサインにおいて、ベースライン時から起立性低血圧の傾向があり、治験薬投与開始後に血圧低下および徐脈の傾向が認められます。特にWeek 2以降の臥位/立位での血圧・脈拍変動について、治験薬との関連性を含めた臨床的な評価と、必要に応じた対応（例：投与量調整、追加検査）についてコメントをお願いします。
        *   **クエリ文面（英語）:** Vital signs show a tendency towards orthostatic hypotension from baseline, with decreased BP and pulse rate after study drug initiation (esp. after dose increase). Please assess the clinical significance including relationship to study drug, focusing on postural changes in BP/pulse from Week 2 onwards, and comment on any actions taken.
        *   **判断理由:** 治験薬との関連が疑われる心血管系の安全性シグナル（起立性低血圧、徐脈）が認められるため、臨床評価と対応の確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: VSドメインのSYSBP, DIABP, PULSEデータ (特にVS.VSPOS='SUPINE' vs 'STANDING', 経時変化)]
            *   [関連する医学的知見: ムスカリン作動薬の心血管系への作用]
    *   **クエリNo.:** Q-4 (関連指摘No.: M-4, D-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Dispositionにおいて、「Dispositionの報告用語」が「ADVERSE EVENT」により試験中止と記録されています（Study Day 50）。RELRECデータではAE「発疹 (Rash)」と関連付けられていますが、Rashは軽度でDay 48に回復済みです。中止の判断根拠となった具体的な有害事象名とその詳細（重症度、重篤度、治験薬との関連等）を確認し、記録の修正をお願いします。
        *   **クエリ文面（英語）:** Subject discontinued due to 'ADVERSE EVENT' on Study Day 50 (DS). RELREC links this to 'RASH', which was mild and resolved on Day 48. Please clarify the specific AE leading to discontinuation, provide details (severity, seriousness, causality), and correct the record if necessary.
        *   **判断理由:** 試験中止理由が不明確であり、RELRECデータとの整合性も低いため、正確な中止理由の特定が必要。
        *   **判断根拠:**
            *   [関連するデータ: DS.DSTERM='ADVERSE EVENT', DS.DSSTDY=50, RELRECデータ (RELID='01-704-1017-E11'), AEドメイン (AESEQ=5, 7)]
    *   **クエリNo.:** Q-5 (関連指摘No.: M-5, D-4)
        *   **重要度:** Major
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 質問票「NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)」において、複数の項目（例: NPITM11S Baseline）で算出されたスコアと、その基となる頻度・重症度の値に矛盾が見られます。記録を確認し、正しい頻度、重症度、およびスコアに修正をお願いします。NPI-X Total Scoreの正確性にも影響するため、ご確認をお願いします。
        *   **クエリ文面（英語）:** In the NPI-X questionnaire, inconsistencies were found between calculated scores (e.g., NPITM11S Baseline=0) and the corresponding Frequency/Severity values (F=4, S=3). Please review the source data and correct the Frequency, Severity, and Score values as needed. This affects the NPI-X Total Score accuracy.
        *   **判断理由:** 有効性評価項目のスコア計算に矛盾があり、データの信頼性に影響するため修正が必要。
        *   **判断根拠:**
            *   [関連するデータ: QSドメインのNPI-X関連データ (NPITMxS, NPITMxF, NPITMxV, NPTOT)]
    *   **クエリNo.:** Q-6 (関連指摘No.: P-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Screening時 (Visit 1) の検査結果において、「クレアチニン」が「1.8 mg/dL」であり、提供された基準範囲 (0.8-1.6 mg/dL) を超えています。プロトコル除外基準[27b]では「Lilly Reference Range III」を超える場合に除外と規定されています。本結果が除外基準に抵触しなかったか、基準値と照合した上でご確認ください。
        *   **クエリ文面（英語）:** At Screening (Visit 1), the Creatinine level was '1.8 mg/dL', exceeding the provided reference range (0.8-1.6 mg/dL). Protocol exclusion criterion [27b] refers to exceeding 'Lilly Reference Range III'. Please confirm if this result met the inclusion criteria by verifying against the specified reference range.
        *   **判断理由:** 除外基準違反の可能性があり、被験者の適格性を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: LB.LBTESTCD='CREAT', LB.VISITNUM=1, LB.LBORRES='1.8', LB.LBORNRHI='1.6']
            *   [関連するプロトコル箇所: Section 3.4.2.2 [27b]]
    *   **クエリNo.:** Q-7 (関連指摘No.: P-6, D-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 有害事象「心筋梗塞」において、「治験薬に対する処置」が「DRUG WITHDRAWN」と記録されていますが、ExposureデータではDay 44まで治験薬が投与された記録となっています。実際の治験薬投与状況とAE記録を確認し、矛盾がある場合は修正をお願いします。
        *   **クエリ文面（英語）:** For the AE 'MYOCARDIAL INFARCTION', 'Action Taken with Study Treatment' is recorded as 'DRUG WITHDRAWN', but Exposure data shows treatment continued until Day 44. Please verify the actual treatment administration and AE record, and correct any discrepancies.
        *   **判断理由:** AE発生時の処置記録と実際の投与記録に矛盾があり、データの正確性を確認する必要があるため。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='MYOCARDIAL INFARCTION', AE.AEACN='DRUG WITHDRAWN', EXドメインデータ (EXENDTC='2013-11-18')]
    *   **クエリNo.:** Q-8 (関連指摘No.: P-5)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 併用薬「PREMARIN」がStudy Day 1から開始されています。プロトコル除外基準[31b] v) では、Estrogen supplementsは登録前3ヶ月間安定投与されていることが要求されています。本薬剤の使用がプロトコル規定に適合していたかご確認ください。
        *   **クエリ文面（英語）:** Concomitant medication 'PREMARIN' was started on Study Day 1. Protocol exclusion criterion [31b] v) requires estrogen supplements to be stable for at least 3 months prior to enrollment. Please confirm if the use of this medication complied with the protocol requirements.
        *   **判断理由:** 除外基準違反（併用薬規定）の可能性があるため、確認が必要。
        *   **判断根拠:**
            *   [関連するデータ: CM.CMTRT='PREMARIN', CM.CMSTDY=1]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [31b] v)]
    *   **クエリNo.:** Q-9 (関連指摘No.: P-7, P-8)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Week 4のNPI-X評価が予定日(Day 28)から7日遅れのDay 35に、Week 6の有効性評価（ADAS-Cog, CIBIC+, DAD, NPI-X）が予定日(Day 42)から8日遅れのDay 50に実施されています。プロトコルではこれらのVisit Windowは±3日と規定されています。評価時期が遅れた理由と、プロトコル逸脱に該当するかご確認ください。
        *   **クエリ文面（英語）:** NPI-X assessment at Week 4 was performed on Day 35 (7 days late from planned Day 28). Efficacy assessments at Week 6 were performed on Day 50 (8 days late from planned Day 42). The protocol specifies a +/- 3 day window for these visits. Please provide the reason for the delay and confirm if this constitutes a protocol deviation.
        *   **判断理由:** プロトコルで規定された評価スケジュールからの逸脱の可能性があり、理由の確認と逸脱としての報告要否の判断が必要なため。評価の信頼性に影響する可能性がある。
        *   **判断根拠:**
            *   [関連するデータ: QS.VISITNUM=5, QS.VISITDY=28, QS.QSDY=35 (NPI-X); QS.VISITNUM=7, QS.VISITDY=42, QS.QSDY=50]
            *   [関連するプロトコル箇所: Section 3.9 (Visit Window)]
    *   **クエリNo.:** Q-10 (関連指摘No.: M-6, D-5)
        *   **重要度:** Minor
        *   **発行担当者:** DM
        *   **医療機関への問い合わせ文面:** 有害事象「報告された有害事象」が「LATE EFFECTS OF CEREBRAL INFARCTION」について、重症度が「SEVERE」、重篤度が「N」と記録されています。評価内容に誤りがないかご確認ください。
        *   **クエリ文面（英語）:** Regarding the AE Term 'LATE EFFECTS OF CEREBRAL INFARCTION', Severity is 'SEVERE' and Serious is 'N'. Please confirm if this assessment is correct.
        *   **判断理由:** 重症度と重篤度の評価に矛盾の可能性があり、データ品質確認のため。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', AE.AESEV='SEVERE', AE.AESER='N']
    *   **クエリNo.:** Q-11 (関連指摘No.: D-9)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Demographicsデータにおいて、「Date/Time of Informed Consent」が記録されていません。同意取得日を確認し、追記をお願いします。
        *   **クエリ文面（英語）:** The 'Date/Time of Informed Consent' is missing in the Demographics data. Please provide the date of informed consent.
        *   **判断理由:** GCP上重要な同意取得日の記録が欠損しているため。
        *   **判断根拠:**
            *   [関連するデータ: DM.RFICDTC='']
    *   **クエリNo.:** Q-12 (関連指摘No.: P-10)
        *   **重要度:** Minor
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** Screening時の検査データにFolateの結果が含まれていません。プロトコル除外基準[28b]の確認のため、Folateの検査結果、または検査未実施の場合はその理由をお知らせください。
        *   **クエリ文面（英語）:** Folate test result is missing from the Screening laboratory data. To confirm compliance with exclusion criterion [28b], please provide the Folate result or the reason if the test was not performed.
        *   **判断理由:** 除外基準の確認に必要な検査データが欠損しているため。
        *   **判断根拠:**
            *   [関連するデータ: LBドメインにFolateデータなし]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [28b]]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: P-1)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** MH/AEで報告されている「脳梗塞後遺症」が、プロトコル除外基準[12a]「Stroke or vascular dementia」に該当しなかったかの判断根拠を内部で確認・記録する。Hachinskiスコアは0点だが、後遺症の臨床的詳細が不明なため、選択基準適合性の判断プロセスを確認する必要がある。収集データのみでは最終判断不可。
        *   **判断理由:** 除外基準抵触の可能性について、判断根拠を明確化するため。問い合わせても医療機関側で追加情報がない可能性が高い。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='LATE EFFECTS OF CEREBRAL INFARCTION', QSデータ(Hachinski Score=0)]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [12] a)]
    *   **確認事項No.:** I-2 (関連指摘No.: P-2)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** MHで報告されている心電図関連所見（ST上昇/低下、期外収縮）が、プロトコル除外基準[16b]に該当しなかったかの判断根拠を内部で確認・記録する。Screening時のECGデータがレビュー対象に含まれていないため、適格性評価プロセスを確認する必要がある。
        *   **判断理由:** 除外基準抵触の可能性について、判断根拠を明確化するため。問い合わせても医療機関側で追加情報がない可能性が高い。
        *   **判断根拠:**
            *   [関連するデータ: MH.MHTERM='VERBATIM_0806', 'VERBATIM_1153', 'VERBATIM_1608']
            *   [関連するプロトコル箇所: Section 3.4.2.2 [16b]]
    *   **確認事項No.:** I-3 (関連指摘No.: P-3)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** MHで報告されている複数の心血管系既往歴およびSignificant Pre-existing Conditionが、プロトコル除外基準[17]「A history within the last 5 years of a serious cardiovascular disorder」に該当しなかったかの判断根拠を内部で確認・記録する。Seriousの定義や評価基準が不明なため、適格性評価プロセスを確認する必要がある。
        *   **判断理由:** 除外基準抵触の可能性について、判断根拠を明確化するため。問い合わせても医療機関側で追加情報がない可能性が高い。
        *   **判断根拠:**
            *   [関連するデータ: MHドメインの心血管系関連データ]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [17]]
    *   **確認事項No.:** I-4 (関連指摘No.: M-7)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** AEとして報告された「心室中隔欠損」は、先天性疾患でありMHに記載されるべき事象と考えられる。AEとしての報告の妥当性について内部で検討し、必要であればコーディングルール等を確認する。患者安全性への直接的な影響は小さい。
        *   **判断理由:** ドメイン間のデータ分類の適切性に関する確認。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='VENTRICULAR SEPTAL DEFECT']
            *   [関連する医学的知見: 心室中隔欠損は通常先天性]
    *   **確認事項No.:** I-5 (関連指摘No.: M-8)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** AE「発疹」「そう痒症」と併用薬「Hydrocortisone topical」の使用時期、転帰は整合しており、プロトコルで予期される皮膚反応とその対処として妥当と考えられる。内部記録として残す。
        *   **判断理由:** データ間の整合性が確認できたため、記録として残す。
        *   **判断根拠:**
            *   [関連するデータ: AEドメイン (AESEQ=5, 6, 7, 8), CMドメイン (CMTRT='HYDROCORTISONE, TOPICAL')]
            *   [関連するプロトコル箇所: Section 3.9.3.4]
    *   **確認事項No.:** I-6 (関連指摘No.: M-9)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** 検査値の変動（クレアチニン、BUN、アルブミン）は認められるが、一過性または軽微であり、現時点で明らかな臨床的意義や安全性への影響は小さいと判断される。経過観察所見として内部記録に残す。
        *   **判断理由:** 臨床的意義が小さいと判断される検査値変動のため。
        *   **判断根拠:**
            *   [関連するデータ: LBドメイン (LBTESTCD='CREAT', 'BUN', 'ALB') の経時変化]
    *   **確認事項No.:** I-7 (関連指摘No.: D-7)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QS (DAD) における評価値のNAからNへの変化について、データ入力規則や評価方法を確認する。評価の信頼性への影響は限定的と考えられる。
        *   **判断理由:** データの一貫性に関する軽微な疑義であり、内部でのルール確認で対応可能と判断。
        *   **判断根拠:**
            *   [関連するデータ: QSドメインのDAD関連データ (QSTESTCD='DAITM04', 'DAITM30', 'DAITM31', 'DAITM32')]
    *   **確認事項No.:** I-8 (関連指摘No.: D-6)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** AE「心室中隔欠損」のAEENDTC欠損について記録する。先天性疾患のため継続していると解釈でき、評価への影響は小さい。
        *   **判断理由:** 必須項目ではない可能性があり、臨床的影響が小さいため。
        *   **判断根拠:**
            *   [関連するデータ: AE.AETERM='VENTRICULAR SEPTAL DEFECT', AE.AEENDTC='']
    *   **確認事項No.:** I-9 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** SV Visit 101 (AE FOLLOW-UP) の VISITDY 欠損について記録する。評価への影響は小さい。
        *   **判断理由:** 軽微なデータ欠損のため。
        *   **判断根拠:**
            *   [関連するデータ: SV.VISITNUM=101, SV.VISITDY=null]
    *   **確認事項No.:** I-10 (関連指摘No.: P-11)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** High Dose群の治験薬増量タイミング (Day 15) がプロトコル計画通りであったか、プロトコル本文および関連文書（例：薬剤管理手順書など）を再確認する。SEドメインとの整合性は取れているように見える。
        *   **判断理由:** プロトコル記載の不明瞭さによる確認事項。現時点では明らかな逸脱とは断定できないため。
        *   **判断根拠:**
            *   [関連するデータ: EX, TA, TE, SEドメインデータ]
            *   [関連するプロトコル箇所: Section 3.1, Figure LZZT.1, Section 3.6.2]
    *   **確認事項No.:** I-11 (関連指摘No.: P-12)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** DSドメインに記録されている「FINAL LAB VISIT」(Visit 5, Day 27) の位置づけを確認する。Visit 5の一部としての記録か、Unscheduled Visitか。評価への影響は小さい。
        *   **判断理由:** データ分類に関する軽微な確認事項。
        *   **判断根拠:**
            *   [関連するデータ: DS.DSDECOD='FINAL LAB VISIT', DS.VISITNUM=5, DS.DSSTDY=27]
            *   [関連するプロトコル箇所: Protocol Attachment LZZT.1]

# 01-703-1042のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 64歳、性別は男性、人種はWHITE、民族はNOT HISPANIC OR LATINO、Planned ArmはPlacebo、Actual ArmはPlacebo、国はUSA。

*   **イベント推移:**

|日付|Study Day, Visit|イベント内容|
|:---|:---|:---|
|2012年12月27日|Day -65, Visit 1 (Screening 1)|[アラニンアミノトランスフェラーゼ(ALT)] = 135 U/L (基準値6-43, HIGH), [アスパラギン酸アミノトランスフェラーゼ(AST)] = 145 U/L (基準値11-36, HIGH)。臨床的に有意な肝酵素上昇。|
|2013年02月21日|Day -9, Visit 1.1 (Unscheduled 1.1)|[ALT] = 19 U/L, [AST] = 29 U/L。肝酵素は正常化。[ナトリウム(Sodium)] = 133 mEq/L (基準値135-145, LOW)。軽度低ナトリウム血症。|
|2013年02月23日|Day -7, Visit 1 (Screening 1)|既往歴としてアルツハイマー病 (2008年開始)、肺気腫 (軽度)、冠動脈疾患 (軽度)、関節炎 (軽度) などが報告された。[MMSEスコア] = 23 (基準内)。[Hachinski Ischemic Scaleスコア] = 1 (基準内)。|
|2013年02月28日|Day -2, Visit 2 (Screening 2)|バイタルサイン測定。|
|2013年03月02日|Day 1, Visit 3 (Baseline)|治験薬（プラセボ）投与開始。[ADAS-Cog(11) Subscore] = 14。[NPI-X (9) Total Score] = 3。|
|2013年03月04日|Day 3|有害事象「下痢 (DIARRHOEA)」(軽度, 因果関係: POSSIBLE) 発現。|
|2013年03月05日|Day 4|有害事象「下痢」回復。併用薬「KAOPECTATE」を1回使用。|
|2013年03月05日|Day 4|有害事象「不眠症 (INSOMNIA)」(軽度, 因果関係: REMOTE) 発現。|
|2013年03月06日|Day 5|有害事象「不眠症」回復。|
|2013年03月14日|Day 13, Visit 4 (Week 2)|[体重(Weight)] = 73.03 kg (ベースラインから-1.36 kg)。[NPI-X (9) Total Score] = 6 (ベースラインから悪化)。|
|2013年03月28日|Day 27, Visit 5 (Week 4)|[Ery. Mean Corpuscular Volume(MCV)] = 101 fL (基準値80-100, HIGH)。[ナトリウム(Sodium)] = 146 mEq/L (基準値135-145, HIGH)。[Anisocytes] = 1 (ABNORMAL)。[体重(Weight)] = 73.94 kg。[NPI-X (9) Total Score] = 4。|
|2013年04月13日|Day 43, Visit 7 (Week 6)|[体重(Weight)] = 73.48 kg。[NPI-X (9) Total Score] = 3。|
|2013年04月27日|Day 57, Visit 8 (Week 8)|[体重(Weight)] = 74.39 kg (ベースラインと同じ)。[ADAS-Cog(11) Subscore] = 9 (ベースラインから改善)。|
|2013年05月11日|Day 71, Visit 8.1 (Week 10 (T))|[NPI-X (9) Total Score] = 4。|
|2013年05月25日|Day 85, Visit 9 (Week 12)|[体重(Weight)] = 76.66 kg (ベースラインから+2.27 kg)。[NPI-X (9) Total Score] = 6。|
|2013年06月08日|Day 99, Visit 9.1 (Week 14 (T))|[NPI-X (9) Total Score] = 6。|
|2013年06月22日|Day 113, Visit 10 (Week 16)|[体重(Weight)] = 75.75 kg。[ADAS-Cog(11) Subscore] = 7 (ベースラインから改善)。[CIBIC+ Extent of Change] = 4 (No Change)。[DAD]一部項目で悪化・改善あり。[NPI-X (9) Total Score] = 4。|
|2013年07月06日|Day 127, Visit 10.1 (Week 18 (T))|[NPI-X (9) Total Score] = 4。|
|2013年07月20日|Day 141, Visit 11 (Week 20)|[体重(Weight)] = 74.39 kg (ベースラインと同じ)。[NPI-X (9) Total Score] = 4。|
|2013年08月03日|Day 155, Visit 11.1 (Week 22 (T))|[NPI-X (9) Total Score] = 3。|
|2013年08月09日|Day 161, Visit 12 (Week 24)|治験薬（プラセボ）投与終了。[体重(Weight)] = 74.39 kg (ベースラインと同じ)。[ADAS-Cog(11) Subscore] = 9 (ベースラインから改善)。[CIBIC+ Extent of Change] = 4 (No Change)。[DAD]一部項目で改善・悪化あり。[NPI-X (9) Total Score] = 2 (ベースラインから改善)。|
|2013年08月31日|Day 183, Visit 13 (Week 26)|試験完了。[アスパラギン酸アミノトランスフェラーゼ(AST)] = 38 U/L (基準値11-36, HIGH)。軽度上昇。[体重(Weight)] = 74.39 kg (ベースラインと同じ)。[NPI-X (9) Total Score] = 2 (ベースラインから改善)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Critical
        *   **内容:** Screening時 (Day -65) に臨床的に有意な肝酵素上昇 ([アラニンアミノトランスフェラーゼ(ALT)] = 135 U/L, [アスパラギン酸アミノトランスフェラーゼ(AST)] = 145 U/L) が認められた。これは組み入れ基準[EXCL27b] (Laboratory test values exceeding the Lilly Reference Range III) に抵触する可能性があった。Unscheduled Visit (Day -9) で正常化が確認されているが、この変動の原因と、組み入れ判断の妥当性について医学的な確認が必要である。参加者の安全性確保の観点から重要。
        *   **根拠:** 肝酵素の著明な上昇は肝障害を示唆し、薬剤投与のリスク評価に影響する。組み入れ前に原因が特定され、リスクが評価されるべきであった。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 19, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -9, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 29, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'
    *   **指摘No.:** M-2
        *   **重要度:** Minor
        *   **内容:** Week 4 (Day 27) に軽度の[Ery. Mean Corpuscular Volume(MCV)]高値 (101 fL) と[Anisocytes]異常 (1) が認められた。これは軽度の大球性貧血を示唆する可能性がある。Screening時に[Vitamin B12(VITB12)]は正常範囲内であったが、葉酸 (Folate) のデータがない。臨床的意義は低い可能性が高いが、原因について考慮が必要。
        *   **根拠:** 大球性貧血の原因検索は通常行われる。ただし、変動は軽微であり一過性の可能性もある。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101, [Reference Range Indicator(LB.LBNRIND)] = 'HIGH'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1, [Reference Range Indicator(LB.LBNRIND)] = 'ABNORMAL'
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'VITB12', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 196.2548, [Reference Range Indicator(LB.LBNRIND)] = 'NORMAL'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** LBドメインのScreening 1の検体採取日 ([Study Day of Specimen Collection(LB.LBDY)] = -65) が、SVドメインのScreening 1 Visit日 ([Planned Study Day of Visit(SV.VISITDY)] = -7) やDMドメインの収集日 ([Study Day of Collection(DM.DMDY)] = -7) と大きく乖離している。データ入力エラーの可能性が高い。医学的評価への影響は小さいと考えられる。
        *   **根拠:** 同一Visit内のイベント日付は近接しているはずである。
        *   **関連データ:**
            *   [Study Day of Specimen Collection(LB.LBDY)] = -65 (LBドメイン, VISITNUM=1)
            *   [Planned Study Day of Visit(SV.VISITDY)] = -7 (SVドメイン, VISITNUM=1)
            *   [Study Day of Collection(DM.DMDY)] = -7 (DMドメイン)
    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** QS, VS, LBドメインにおいて、評価実施日 (--DY) と計画Visit日 (VISITDY) に1-2日のずれが散見される。プロトコルにVisit Windowの規定がないため逸脱とは断定できないが、記録しておく。評価の信頼性への影響は小さいと考えられる。
        *   **根拠:** 計画日と実施日のずれは臨床試験では起こりうるが、Visit Windowの遵守は重要。
        *   **関連データ:**
            *   例: [Study Day of Finding(QS.QSDY)] = 57 vs [Planned Study Day of Visit(SV.VISITDY)] = 56 (Visit 8)
            *   例: [Study Day of Vital Signs(VS.VSDY)] = 13 vs [Planned Study Day of Visit(SV.VISITDY)] = 14 (Visit 4)
            *   例: [Study Day of Specimen Collection(LB.LBDY)] = 13 vs [Planned Study Day of Visit(SV.VISITDY)] = 14 (Visit 4)
    *   **指摘No.:** D-3
        *   **重要度:** Critical
        *   **内容:** Screening時の肝酵素 (ALT, AST) が基準値上限の3倍を超える異常高値であった。これは臨床的に重要な異常値である。
        *   **根拠:** 基準値を大幅に超える検査値は、医学的評価と安全性評価において重要。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145
    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** [Date/Time of Informed Consent(DM.RFICDTC)] が欠損している。また、プロトコル上Screeningで評価が必要な葉酸 (Folate) の検査データがLBドメインに存在しない。これらの欠損は、参加者の権利保護や適格性評価の確認に影響を与える。
        *   **根拠:** 同意取得日と必須検査データの欠損は、GCP遵守および評価の信頼性に関わる。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
            *   LBドメインに [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'FOLATE' のレコードが存在しない。

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Critical
        *   **逸脱の可能性:** 除外基準[EXCL27b] (Laboratory test values exceeding the Lilly Reference Range III) に抵触していた可能性がある。Screening時 (Day -65) のALT (135 U/L) およびAST (145 U/L) は基準値上限 (ALT: 43, AST: 36) を大幅に超えていた。Unscheduled Visit (Day -9) で正常化したが、組み入れ時点での適格性判断の妥当性に疑義がある。参加者の安全性とデータの信頼性に影響する。
        *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [27b]
        *   **根拠:** プロトコルで規定された除外基準に該当する検査値異常がScreening時に認められた。
        *   **関連データ:**
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135
            *   [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145
    *   **指摘No.:** P-2
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得に関する記録が不十分である。[Date/Time of Informed Consent(DM.RFICDTC)] が欠損しており、治験手順開始前に適切に同意が取得されたか確認できない。参加者の権利保護に関する重要な逸脱の可能性がある。
        *   **プロトコル該当箇所:** Section 5.1 Informed Consent
        *   **根拠:** 同意取得の記録はGCP上必須である。
        *   **関連データ:**
            *   [Date/Time of Informed Consent(DM.RFICDTC)] = ''
    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 組み入れ/除外基準の確認に必要な一部の評価データが提供されていない。具体的には、[INCL05] CNSイメージング、[EXCL16b] Screening ECG、[EXCL28b] 葉酸 (Folate)、[EXCL29b] 梅毒スクリーニングの結果が確認できない。これらの評価が実施され、基準を満たしていたか不明であり、プロトコル遵守に疑義がある。参加者の安全性とデータの信頼性に影響する。
        *   **プロトコル該当箇所:** Section 3.4.2.1 Inclusion Criteria [5], Section 3.4.2.2 Exclusion Criteria [16b], [28b], [29b]
        *   **根拠:** プロトコルで規定された組み入れ/除外基準の確認がデータ上できない。
        *   **関連データ:**
            *   関連するドメイン (例: IE, PE, LB) に該当データなし。
    *   **指摘No.:** P-4
        *   **重要度:** Minor
        *   **逸脱の可能性:** 各評価の実施日 (--DY) が計画Visit日 (VISITDY) と一致していない場合がある。プロトコル (Section 3.1) にはVisit Windowに関する記載があるが、具体的な許容範囲は不明。提供データのみでは逸脱とは断定できないが、Visit Windowを遵守していたか確認が必要。評価の信頼性に軽微な影響を与える可能性がある。
        *   **プロトコル該当箇所:** Section 3.1 Summary of Study Design (Visit schedule and window)
        *   **根拠:** 評価タイミングのずれは、データの解釈に影響を与える可能性がある。
        *   **関連データ:**
            *   例: [Study Day of Finding(QS.QSDY)] = 57 vs [Planned Study Day of Visit(SV.VISITDY)] = 56 (Visit 8)

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-3, P-1)
        *   **重要度:** Critical
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Screening 1 (2012-12-27, Day -65) において、「アラニンアミノトランスフェラーゼ」が「135 U/L」、「アスパラギン酸アミノトランスフェラーゼ」が「145 U/L」と基準値を大幅に超える高値でした。これは除外基準[27b]に抵触する可能性がありましたが、Unscheduled Visit 1.1 (2013-02-21, Day -9) で正常化が確認されています。Screening時の肝酵素高値の原因、および正常化を確認して組み入れを判断した経緯について詳細をご教示ください。また、関連する臨床症状の有無についてもご確認ください。参加者の安全性確保および組み入れ適格性確認のため、ご回答をお願いいたします。
        *   **クエリ文面（英語）:** At Screening 1 (2012-12-27, Day -65), ALT was 135 U/L and AST was 145 U/L, significantly exceeding reference ranges. This potentially violated exclusion criterion [27b]. Values normalized by Unscheduled Visit 1.1 (2013-02-21, Day -9). Please provide details on the cause of the elevated liver enzymes at screening and the rationale for enrollment after normalization. Also confirm if there were any related clinical symptoms. This information is needed to ensure subject safety and confirm eligibility.
        *   **判断理由:** Screening時の著明な肝酵素上昇は除外基準抵触の可能性があり、組み入れ判断の妥当性と参加者の安全性確認のため、原因と経緯の確認が必須であるため。
        *   **判断根拠:**
            *   [関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ALT', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 135 / [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'AST', [Study Day of Specimen Collection(LB.LBDY)] = -65, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 145]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [27b]]
            *   [関連する医学的知見: 肝酵素異常は肝機能障害を示唆し、薬剤投与リスク評価に重要]
    *   **クエリNo.:** Q-2 (関連指摘No.: D-4, P-2)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** DMドメインの「Date/Time of Informed Consent」が欠損しています。治験手順開始前に、患者（または代諾者）および介護者から適切にインフォームド・コンセントが取得された日付をご確認の上、ご報告ください。参加者の権利保護の観点から確認が必要です。
        *   **クエリ文面（英語）:** The Date/Time of Informed Consent (DM.RFICDTC) is missing. Please confirm and provide the date when informed consent was obtained from the subject (or legally acceptable representative) and caregiver, prior to initiating any study procedures. This is required to ensure protection of subject rights.
        *   **判断理由:** 同意取得日の記録はGCP上必須であり、参加者の権利が保護されていることを確認するため。
        *   **判断根拠:**
            *   [関連するデータ: [Date/Time of Informed Consent(DM.RFICDTC)] = '']
            *   [関連するプロトコル箇所: Section 5.1 Informed Consent]
            *   [関連する医学的知見: GCP要件]
    *   **クエリNo.:** Q-3 (関連指摘No.: P-3, D-4)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** プロトコルで規定されているScreening時の評価のうち、CNSイメージング (Inclusion Criteria [5])、ECG (Exclusion Criteria [16b])、梅毒スクリーニング (Exclusion Criteria [29b])、および葉酸検査 (Exclusion Criteria [28b]) の結果が提供データに含まれていません。これらの評価が実施され、結果が組み入れ/除外基準を満たしていたことをご確認ください。適格性確認のためご回答をお願いいたします。
        *   **クエリ文面（英語）:** Results for protocol-required screening assessments are missing from the provided data: CNS imaging (Incl [5]), ECG (Excl [16b]), Syphilis screening (Excl [29b]), and Folate test (Excl [28b]). Please confirm these assessments were performed and that the results met the inclusion/exclusion criteria. This confirmation is needed for eligibility verification.
        *   **判断理由:** 組み入れ/除外基準の遵守を確認するために必須の評価結果が不明であるため。
        *   **判断根拠:**
            *   [関連するデータ: 該当データなし]
            *   [関連するプロトコル箇所: Section 3.4.2.1 [5], Section 3.4.2.2 [16b], [28b], [29b]]
            *   [関連する医学的知見: 適格性確認は試験の科学的妥当性と安全性確保に不可欠]
    *   **クエリNo.:** Q-4 (関連指摘No.: M-2, D-3)
        *   **重要度:** Minor
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** Visit 5 (Week 4, Day 27) の検査にて、「Ery. Mean Corpuscular Volume」が「101 fL」と基準値上限を超え、「Anisocytes」が「1」 (ABNORMAL) と報告されています。これらの所見について臨床的な意義およびフォローアップの有無をご確認ください。
        *   **クエリ文面（英語）:** At Visit 5 (Week 4, Day 27), MCV was 101 fL (above upper limit) and Anisocytes was reported as '1' (ABNORMAL). Please assess the clinical significance of these findings and confirm if any follow-up was performed.
        *   **判断理由:** 軽微な検査値異常であるが、念のため臨床的意義を確認するため。
        *   **判断根拠:**
            *   [関連するデータ: [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'MCV', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 101 / [Lab Test or Examination Short Name(LB.LBTESTCD)] = 'ANISO', [Study Day of Specimen Collection(LB.LBDY)] = 27, [Numeric Result/Finding in Standard Units(LB.LBSTRESN)] = 1]
            *   [関連する医学的知見: 大球性貧血の可能性]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** LBドメインのScreening 1の検体採取日 (Day -65) と、SV/DMドメインのScreening 1 Visit日/収集日 (Day -7) が一致していない。データ入力エラーの可能性が高いため、内部で確認し修正を検討する。医学的評価への影響は限定的。
        *   **判断理由:** データ品質の問題であり、内部での修正が適切と判断されるため。
        *   **判断根拠:**
            *   [関連するデータ: [Study Day of Specimen Collection(LB.LBDY)] = -65 (LB, VISITNUM=1), [Planned Study Day of Visit(SV.VISITDY)] = -7 (SV, VISITNUM=1), [Study Day of Collection(DM.DMDY)] = -7 (DM)]
    *   **確認事項No.:** I-2 (関連指摘No.: D-2, P-4)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** QS, VS, LBドメインにおいて、評価実施日 (--DY) と計画Visit日 (VISITDY) に1-2日のずれが散見される。プロトコル (Section 3.1) に記載されているVisit Window (Visit 4, 5, 7, 8, 13 は±3日、Visit 9, 10, 11, 12 は±4日) を確認し、逸脱がないか内部で評価・記録する。提供データ範囲内では大きな逸脱は見られず、影響は小さいと判断。
        *   **判断理由:** Visit Window遵守の確認はプロトコル遵守の観点から必要だが、大きな逸脱は見られず、内部確認で十分と判断されるため。
        *   **判断根拠:**
            *   [関連するデータ: 各ドメインの--DYとVISITDYの比較]
            *   [関連するプロトコル箇所: Section 3.1 Summary of Study Design]
    *   **確認事項No.:** I-3 (関連指摘No.: P-1)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor/CRA
        *   **疑義事項/確認内容:** MHとして報告されている冠動脈疾患、肺気腫、関節炎が、プロトコルの除外基準 [EXCL17], [EXCL20], [EXCL22] (過去5年の重篤な疾患) に該当しないと判断された根拠を内部で確認し、記録する。MILDと記録されており重篤ではないと判断された可能性が高い。
        *   **判断理由:** 組み入れ判断の根拠を確認・記録するため。医療機関への問い合わせは不要と判断。
        *   **判断根拠:**
            *   [関連するデータ: MHドメインのMHTERM, MHSEV]
            *   [関連するプロトコル箇所: Section 3.4.2.2 Exclusion Criteria [17], [20], [22]]
    *   **確認事項No.:** I-4 (関連指摘No.: D-4)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** QS (DAD) のDAITM29 (RETURN FROM THE STORE) がベースラインでNA (96) と記録されている。この項目がなぜ適用不能 (Not Applicable) と判断されたのか、理由を内部で確認・記録する。評価への影響は限定的。
        *   **判断理由:** データ欠損の理由を明確にするため。評価への影響は小さいと判断。
        *   **判断根拠:**
            *   [関連するデータ: [Question Short Name(QS.QSTESTCD)] = 'DAITM29', [Visit Number(QS.VISITNUM)] = 3, [Finding in Original Units(QS.QSORRES)] = 'NA', [Numeric Finding in Standard Units(QS.QSSTRESN)] = 96]

# 01-701-1111のデータ統合レビュー報告

## 1. 症例サマリー

*   **患者背景:**
    年齢は 81歳、性別は女性、人種は白色人種、民族はヒスパニックまたはラテン系ではない。計画された投与群コードは Xan_Lo (Xanomeline Low Dose)、実際の投与群コードは Xan_Lo (Xanomeline Low Dose)。国は USA。治験薬初回投与日 (Subject Reference Start Date/Time) は 2012年9月7日。治験薬最終投与日 (Subject Reference End Date/Time) は 2012年9月17日。参加終了日 (Date/Time of End of Participation) は 2013年2月22日。

*   **イベント推移:**

|日付|Study Day, Visit|イベント内容|
|:---|:---|:---|
|2012年8月25日|Day -13, Visit 1 (SCREENING 1)|スクリーニング実施。既往歴としてアルツハイマー病 (2009年発症)、高血圧、難聴 (軽度)、食道裂孔ヘルニア (軽度)、足関節浮腫 (軽度)、耳鳴 (軽度)、骨粗鬆症 (軽度)、限局性感染症 (軽度)、関節炎 (軽度)、眼鏡装用、甲状腺機能低下症、背部痛、静脈瘤、副鼻腔炎など多数あり。MMSEスコア23点、Hachinskiスコア1点。赤血球数 3.8 TI/L (基準値下限未満)。|
|2012年9月2日|Day -5|有害事象「紅斑」(軽度) 発現。有害事象「そう痒症」(軽度) 発現。併用薬「HYDROCORTISONE, TOPICAL」開始。|
|2012年9月4日|Day -3|併用薬「HYDROCORTISONE, TOPICAL」終了。|
|2012年9月5日|Day -2, Visit 2 (SCREENING 2)|スクリーニング2 Visit実施。|
|2012年9月7日|Day 1, Visit 3 (BASELINE)|治験薬「XANOMELINE」54 mg/日 経皮投与開始。有害事象「紅斑」「そう痒症」回復/解消。有害事象「尿意切迫」(軽度) 発現。ADAS-Cog(11) ベースラインスコア: 7。NPI-X ベースラインスコア: 2。|
|2012年9月13日|Day 7|有害事象「関節痛」(中等度) 発現。有害事象「蜂巣炎」(中等度) 発現。|
|2012年9月16日|Day 10|治験薬「XANOMELINE」投与終了。|
|2012年9月17日|Day 11, Visit 4 (WEEK 2)|有害事象により治験中止。最終ラボ評価実施。赤血球数 3.7 TI/L (基準値下限未満)、MCV 101 fL (基準値上限超過)、尿比重 1.004 (基準値下限未満)、アニソサイトーシス 1 (異常)。立位血圧低下傾向 (収縮期: Baseline 135/136 -> Week 2 110/112 mmHg)。ADAS-Cog(11) スコア: 5 (ベースラインから改善)。NPI-X スコア: 1 (ベースラインから改善)。CIBIC+ スコア: 4 (変化なし)。有害事象「関節痛」「蜂巣炎」「尿意切迫」「限局性感染症」は未回復/未解決。|
|2012年9月29日|Day 23, Visit 101 (AE FOLLOW-UP)|有害事象フォローアップ Visit実施。|
|2013年2月22日|Day 169, Visit 201 (RETRIEVAL)|Retrieval Visit実施。ADAS-Cog(11) スコア: 9 (ベースラインから悪化)。NPI-X スコア: 45 (ベースラインから著明悪化、特に妄想、興奮/攻撃性、不安、脱抑制、易刺激性)。CIBIC+ スコア: 5 (軽度悪化)。|

## 2. 統合レビュー結果

*   **【医学的レビュー】からの指摘事項:**
    *   **指摘No.:** M-1
        *   **重要度:** Major
        *   **内容:** 有害事象の評価（関連性、処置、転帰）に疑問がある。Day 11の中止理由となった「関節痛」「蜂巣炎」および治験薬投与開始日に発現した「尿意切迫」について、治験薬との関連性 (AEREL) が "NONE" とされているが、関節痛や尿意切迫はXanomeline（ムスカリン作動薬）の作用機序から関連が否定できない可能性がある。また、これらのAEに対する処置 (AEACN) が記録されておらず、転帰 (AEOUT) も中止時点 (Day 11) で "NOT RECOVERED/NOT RESOLVED" のままで、その後のフォローアップ情報がない。特に蜂巣炎の転帰は重要である。安全性評価の妥当性に影響する。
        *   **根拠:** Xanomelineはムスカリン作動薬であり、関節痛や泌尿器症状を引き起こす可能性があるという一般的な医学知識。有害事象の評価とフォローアップは参加者の安全性確保に不可欠である。
        *   **関連データ:**
            *   [報告された有害事象の用語(AE.AETERM)] = 'ARTHRALGIA', [有害事象開始日(Study Day)(AE.AESTDY)] = 7, [重症度/強度(AE.AESEV)] = 'MODERATE', [因果関係(AE.AEREL)] = 'NONE', [有害事象の処置(AE.AEACN)] = '', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [報告された有害事象の用語(AE.AETERM)] = 'CELLULITIS', [有害事象開始日(Study Day)(AE.AESTDY)] = 7, [重症度/強度(AE.AESEV)] = 'MODERATE', [因果関係(AE.AEREL)] = 'NONE', [有害事象の処置(AE.AEACN)] = '', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [報告された有害事象の用語(AE.AETERM)] = 'MICTURITION URGENCY', [有害事象開始日(Study Day)(AE.AESTDY)] = 1, [重症度/強度(AE.AESEV)] = 'MILD', [因果関係(AE.AEREL)] = 'NONE', [有害事象の処置(AE.AEACN)] = '', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [標準化された処置用語(DS.DSDECOD)] = 'ADVERSE EVENT', [Disposition事象の開始日(Study Day)(DS.DSSTDY)] = 11

    *   **指摘No.:** M-2
        *   **重要度:** Major
        *   **内容:** Day -61から続く「限局性感染症」(AE) および併用薬「KEFLEX」(Cephalexin) の長期投与について、臨床的な詳細が不明である。Day 7に発現した「蜂巣炎」との関連性や、KEFLEXの有効性・長期投与の妥当性が評価できない。適応症 (CMINDC) も記録されていない。感染症の遷延は参加者の安全性に関わる可能性がある。
        *   **根拠:** 抗菌薬の長期使用は耐性菌や副作用のリスクを伴うため、適応と効果の評価が重要であるという一般的な医学知識。
        *   **関連データ:**
            *   [報告された有害事象の用語(AE.AETERM)] = 'LOCALISED INFECTION', [有害事象開始日(Study Day)(AE.AESTDY)] = -61, [重症度/強度(AE.AESEV)] = 'MODERATE', [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED'
            *   [報告された薬剤、医学療法、または治療法の名前(CM.CMTRT)] = 'KEFLEX', [薬剤開始日(Study Day)(CM.CMSTDY)] = -61, [薬剤終了日(Study Day)(CM.CMENDY)] = null, [適応症(CM.CMINDC)] = ''

    *   **指摘No.:** M-3
        *   **重要度:** Major
        *   **内容:** Week 2 (Day 11) のバイタルサイン測定において、ベースラインと比較して立位時の収縮期血圧が低下している（1分後: 136→112 mmHg, 3分後: 135→110 mmHg）。起立性低血圧の可能性が示唆されるが、有害事象として報告されていない。Xanomelineはコリン作動薬であり血圧低下のリスクがあるため、この所見は臨床的に重要であり、AEとしての評価・報告が必要だった可能性がある。
        *   **根拠:** Xanomelineの薬理作用とバイタルサインデータとの関連性。未報告の有害事象の可能性。
        *   **関連データ:**
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure', [被験者のバイタルサイン測定時の姿勢(VS.VSPOS)] = 'STANDING', [Visit名(VS.VISIT)] = 'BASELINE', [標準単位での数値結果/所見(VS.VSSTRESN)] = 136, 135
            *   [バイタルサイン検査名(VS.VSTEST)] = 'Systolic Blood Pressure', [被験者のバイタルサイン測定時の姿勢(VS.VSPOS)] = 'STANDING', [Visit名(VS.VISIT)] = 'WEEK 2', [標準単位での数値結果/所見(VS.VSSTRESN)] = 112, 110

    *   **指摘No.:** M-4
        *   **重要度:** Major
        *   **内容:** Retrieval Visit (Day 169、治験中止約5ヶ月後) におけるNPI-Xスコアがベースライン (2点) やWeek 2 (1点) と比較して著しく悪化 (45点) している。特に妄想、興奮/攻撃性、不安、脱抑制、易刺激性の項目が悪化している。これは疾患進行による可能性が高いと考えられるが、治験薬中止後の影響（例：離脱症状、リバウンド現象）の可能性も完全に否定はできない。臨床的に顕著な変化であり、原因は不明確ながらも注目すべき所見である。
        *   **根拠:** 有効性評価指標の著しい変動。治験薬中止後の経過観察の重要性。
        *   **関連データ:**
            *   [質問名(QS.QSTEST)] = 'NPI-X (9) Total Score', [Visit名(QS.VISIT)] = 'BASELINE', [標準単位での数値所見(QS.QSSTRESN)] = 2
            *   [質問名(QS.QSTEST)] = 'NPI-X (9) Total Score', [Visit名(QS.VISIT)] = 'WEEK 2', [標準単位での数値所見(QS.QSSTRESN)] = 1
            *   [質問名(QS.QSTEST)] = 'NPI-X (9) Total Score', [Visit名(QS.VISIT)] = 'RETRIEVAL', [標準単位での数値所見(QS.QSSTRESN)] = 45

    *   **指摘No.:** M-5
        *   **重要度:** Minor
        *   **内容:** Week 2 (Day 11) の検査でMCVが101 fLと基準値上限 (100 fL) をわずかに超えている。Screening時 (97 fL) から上昇している。大球性貧血の初期変化の可能性も考えられるが、逸脱の程度は軽微であり、他の血液検査項目に著変はない。臨床的意義は低い可能性が高い。
        *   **根拠:** 検査値の軽度異常。他のデータとの関連性の低さ。
        *   **関連データ:**
            *   [検査項目名(LB.LBTEST)] = 'Ery. Mean Corpuscular Volume', [Visit名(LB.VISIT)] = 'SCREENING 1', [標準単位での数値結果/所見(LB.LBSTRESN)] = 97, [基準範囲指標(LB.LBNRIND)] = 'NORMAL'
            *   [検査項目名(LB.LBTEST)] = 'Ery. Mean Corpuscular Volume', [Visit名(LB.VISIT)] = 'WEEK 2', [標準単位での数値結果/所見(LB.LBSTRESN)] = 101, [基準範囲指標(LB.LBNRIND)] = 'HIGH'

*   **【データ整合性】観点からの指摘事項:**
    *   **指摘No.:** D-1
        *   **重要度:** Minor
        *   **内容:** 有害事象「紅斑」と「そう痒症」について、同じ開始日・終了日で異なる収集日 (Visit 2とVisit 4) の記録が存在し、転帰 (AEOUT) が矛盾している (Visit 2収集分は未回復、Visit 4収集分は回復)。Visit 4時点では回復しているはずであり、Visit 2収集分の転帰情報が古いままになっているか、データの入力・管理に問題がある可能性がある。主要な評価への影響は小さいと考えられる。
        *   **根拠:** 同一事象に対する記録の重複と矛盾。
        *   **関連データ:**
            *   [報告された有害事象の用語(AE.AETERM)] = 'ERYTHEMA', [連番(AE.AESEQ)] = 1, [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [収集日時(AE.AEDTC)] = '2012-09-05'
            *   [報告された有害事象の用語(AE.AETERM)] = 'ERYTHEMA', [連番(AE.AESEQ)] = 4, [有害事象の転帰(AE.AEOUT)] = 'RECOVERED/RESOLVED', [収集日時(AE.AEDTC)] = '2012-09-17'
            *   [報告された有害事象の用語(AE.AETERM)] = 'PRURITUS', [連番(AE.AESEQ)] = 2, [有害事象の転帰(AE.AEOUT)] = 'NOT RECOVERED/NOT RESOLVED', [収集日時(AE.AEDTC)] = '2012-09-05'
            *   [報告された有害事象の用語(AE.AETERM)] = 'PRURITUS', [連番(AE.AESEQ)] = 5, [有害事象の転帰(AE.AEOUT)] = 'RECOVERED/RESOLVED', [収集日時(AE.AEDTC)] = '2012-09-17'

    *   **指摘No.:** D-2
        *   **重要度:** Minor
        *   **内容:** 既往歴 (MH) の「LOCALIZED INFECTION」と有害事象 (AE) の「LOCALISED INFECTION」が同一事象を指している可能性があるが、情報が一致しない。MHでは重症度が「MILD」、AEでは「MODERATE」。MHの開始日は不明 (収集日はDay -13)、AEの開始日はDay -61。データの整合性に問題がある可能性。主要な評価への影響は小さいと考えられる。
        *   **根拠:** 同一と考えられる事象に関するドメイン間での情報不一致。
        *   **関連データ:**
            *   [報告された医学的履歴の用語(MH.MHTERM)] = 'VERBATIM_1224', [重症度/強度(MH.MHSEV)] = 'MILD', [履歴収集日時(MH.MHDTC)] = '2012-08-25', [医学的履歴事象の開始日時(MH.MHSTDTC)] = ''
            *   [報告された有害事象の用語(AE.AETERM)] = 'LOCALISED INFECTION', [重症度/強度(AE.AESEV)] = 'MODERATE', [有害事象開始日(Study Day)(AE.AESTDY)] = -61

    *   **指摘No.:** D-3
        *   **重要度:** Major
        *   **内容:** 中止理由となった可能性のある有害事象「関節痛」「蜂巣炎」および治験薬との関連が疑われる「尿意切迫」について、処置 (AEACN) が記録されておらず、転帰 (AEOUT) も中止後の情報がない。安全性評価に必要な情報が欠損している。 (医学的レビュー M-1 と関連)
        *   **根拠:** 安全性評価における重要情報の欠損。
        *   **関連データ:** AEドメインの該当レコード (M-1参照)

    *   **指摘No.:** D-4
        *   **重要度:** Major
        *   **内容:** 併用薬「KEFLEX」について、適応症 (CMINDC)、標準化薬剤名 (CMDECOD)、薬剤分類 (CMCLAS) が記録されていない。長期投与されている薬剤であり、その理由や分類が不明なことは安全性評価（特に感染症との関連評価）に影響する。(医学的レビュー M-2 と関連)
        *   **根拠:** 安全性評価に関連する併用薬情報の欠損。
        *   **関連データ:** CMドメインの KEFLEX のレコード (M-2参照)

    *   **指摘No.:** D-5
        *   **重要度:** Minor
        *   **内容:** 除外基準[28b]の確認に必要なビタミンB12、葉酸の検査結果がLBドメインに含まれていない。ただし、被験者は組み入れられているため、基準を満たしていたと推測される。記録としての欠損。
        *   **根拠:** 選択/除外基準確認に必要なデータの欠損。
        *   **関連データ:** LBドメイン

    *   **指摘No.:** D-6
        *   **重要度:** Major
        *   **内容:** 同意取得日 (DM.RFICDTC) が欠損している。GCP上、治験実施前に同意取得とその日付の記録は必須である。
        *   **根拠:** GCP要件に関する重要情報の欠損。
        *   **関連データ:** [同意説明文書への署名日時(DM.RFICDTC)] = ''

    *   **指摘No.:** D-7
        *   **重要度:** Major
        *   **内容:** プロトコルで規定されているECG、24時間ホルター心電図 (Ambulatory ECG)、薬物動態 (PK) 測定に関するデータがJSONに含まれていない。これらの評価が実施されなかったのか、データが欠損しているのか不明。安全性評価およびPK評価に影響する。(プロトコル遵守 P-1 と関連)
        *   **根拠:** プロトコル規定の重要な評価に関するデータの欠損。
        *   **関連データ:** ECG, EG, PC ドメインデータが存在しない

    *   **指摘No.:** D-8
        *   **重要度:** Minor
        *   **内容:** DAD評価 (QS) において、"Going on an outing" に関連する複数の項目 (DAITM25-29) がWeek 2で "Not Applicable (NA)" となっているが、その理由が不明。ベースラインやRetrievalでは評価されているため、一時的に外出が不可能だったのか、評価者が判断できなかったのか等、解釈に影響する可能性がある。
        *   **根拠:** 有効性評価データの解釈に必要な情報の不足。
        *   **関連データ:** QSドメイン DAITM25-29 の Week 2 (VISITNUM=4) のレコード

*   **【プロトコル遵守】観点からの指摘事項 (逸脱の可能性):**
    *   **指摘No.:** P-1
        *   **重要度:** Major
        *   **逸脱の可能性:** プロトコル (Attachment LZZT.1, Section 3.9.3.4.2) で規定されているスクリーニング時のECG、Visit 2での24時間ホルター心電図、Visit 4 (中止時) でのECG、および複数回のPKサンプリングが実施されなかった、あるいはデータが収集・記録されなかった可能性がある。これらは重要な安全性評価およびPK評価であり、未実施またはデータ欠損はプロトコルからの逸脱にあたる可能性がある。参加者の安全性監視および試験評価の信頼性に影響する。(データ整合性 D-7 と関連)
        *   **プロトコル該当箇所:** Attachment LZZT.1 (Schedule of Events), Section 3.9.3.4.2 (Cardiovascular Safety Measures), Section 3.9.2 (Pharmacokinetics)
        *   **根拠:** プロトコルで規定された評価のデータ欠損。
        *   **関連データ:** ECG, EG, PC ドメインデータが存在しない

    *   **指摘No.:** P-2
        *   **重要度:** Minor
        *   **逸脱の可能性:** プロトコル (Section 3.10.1) では、早期中止時に用量を漸減する手順（25cm2パッチを除去し、50cm2パッチをET Visitまで継続）が記載されているが、EXドメインの記録ではDay 10で投与が終了しており、漸減が行われたか不明確である。プロトコルで規定された中止手順からの逸脱の可能性がある。安全性への影響は小さいかもしれないが、手順遵守の観点から問題。
        *   **プロトコル該当箇所:** Section 3.10.1 (Discontinuations)
        *   **根拠:** 治験薬投与記録とプロトコル規定の中止手順との不一致の可能性。
        *   **関連データ:** [治験薬投与終了日時(EX.EXENDTC)] = '2012-09-16', [治験薬投与終了日(Study Day)(EX.EXENDY)] = 10

    *   **指摘No.:** P-3
        *   **重要度:** Major
        *   **逸脱の可能性:** 同意取得日 (DM.RFICDTC) が記録されておらず、治験手順開始前に同意が適切に取得されたか確認できない。また、選択基準[5]であるCNS imagingの結果がデータに含まれておらず、確認できない。これらはGCPおよびプロトコル遵守の観点から重要であり、逸脱の可能性がある。(データ整合性 D-6 と関連)
        *   **プロトコル該当箇所:** Section 5.1 (Informed Consent), Section 3.4.2.1 [5] (Inclusion Criteria)
        *   **根拠:** GCPおよびプロトコルで要求される情報の欠損。
        *   **関連データ:** [同意説明文書への署名日時(DM.RFICDTC)] = '', CNS imaging データなし

## 3. 疑義事項

*   **医療機関へのクエリ:**
    *   **クエリNo.:** Q-1 (関連指摘No.: M-1, D-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者（USUBJID: 01-701-1111）について、有害事象「関節痛」(2012/9/13発現)、「蜂巣炎」(2012/9/13発現)、「尿意切迫」(2012/9/7発現) が報告されています。これらの事象はDay 11の治験中止理由と関連している可能性がありますが、治験薬との因果関係がいずれも「NONE」と評価されています。特に「関節痛」と「尿意切迫」は治験薬の作用機序との関連も考えられますので、因果関係評価の根拠について、また、これらの事象に対して行われた処置、および治験中止後の転帰について詳細をご教示ください。参加者の安全性評価のために確認が必要です。
        *   **クエリ文面（英語）:** Regarding subject 01-701-1111, AEs 'ARTHRALGIA' (onset 2012-09-13), 'CELLULITIS' (onset 2012-09-13), and 'MICTURITION URGENCY' (onset 2012-09-07) were reported. Causality for all is 'NONE', but Arthralgia/Micturition Urgency could be related to study drug. Please clarify causality assessment basis, actions taken, and outcome after study discontinuation for these AEs, especially as they may relate to the discontinuation on Day 11. This information is needed for safety assessment.
        *   **判断理由:** 中止理由となった可能性のあるAEおよび薬理作用と関連しうるAEについて、関連性評価の根拠、処置、転帰の情報が不足しており、安全性評価に不可欠なため。
        *   **判断根拠:**
            *   [関連するデータ: AEドメイン (AESEQ=6, 7, 8), DSドメイン (DSSEQ=1)]
            *   [関連するプロトコル箇所: Section 3.9.3 (Safety), 3.10.1 (Discontinuations)]
            *   [関連する医学的知見: Xanomelineの薬理作用]

    *   **クエリNo.:** Q-2 (関連指摘No.: M-2, D-4)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者（USUBJID: 01-701-1111）について、併用薬「KEFLEX」が2012年7月8日 (Day -61) から長期にわたり投与されていますが、適応症が不明です。また、同日発現の有害事象「限局性感染症」およびDay 7発現の「蜂巣炎」との関連も不明です。「KEFLEX」の具体的な適応症、および「限局性感染症」「蜂巣炎」の臨床経過と「KEFLEX」による治療効果について詳細をご教示ください。感染症管理と安全性評価のために確認が必要です。
        *   **クエリ文面（英語）:** Subject 01-701-1111 has been taking concomitant medication 'KEFLEX' since 2012-07-08 (Day -61), but the indication is missing. Please provide the indication for KEFLEX. Also, clarify the clinical course of AE 'LOCALISED INFECTION' (onset Day -61) and 'CELLULITIS' (onset Day 7), and the effectiveness of KEFLEX treatment for these conditions. This information is needed for safety assessment regarding infection management.
        *   **判断理由:** 長期抗菌薬投与の適応と効果、および関連する感染症AEの詳細が不明であり、安全性評価に不可欠なため。
        *   **判断根拠:**
            *   [関連するデータ: CMドメイン (CMTRT='KEFLEX'), AEドメイン (AETERM='LOCALISED INFECTION', 'CELLULITIS')]
            *   [関連するプロトコル箇所: Section 3.8 (Concomitant Therapy), 3.9.3 (Safety)]
            *   [関連する医学的知見: 抗菌薬の適正使用]

    *   **クエリNo.:** Q-3 (関連指摘No.: M-3)
        *   **重要度:** Major
        *   **発行担当者:** Medical Monitor
        *   **医療機関への問い合わせ文面:** 患者（USUBJID: 01-701-1111）について、Week 2 (Day 11) のバイタルサイン測定で立位時の収縮期血圧低下（1分後: 112 mmHg, 3分後: 110 mmHg）が認められました。ベースライン（1分後: 136 mmHg, 3分後: 135 mmHg）からの変化が大きいですが、有害事象としての報告はありません。この血圧低下について、臨床的な評価（症状の有無など）と、有害事象として報告する必要性についてご判断をお願いします。
        *   **クエリ文面（英語）:** For subject 01-701-1111, VS data at Week 2 (Day 11) show a decrease in standing systolic BP (1min: 112 mmHg, 3min: 110 mmHg) compared to baseline (1min: 136 mmHg, 3min: 135 mmHg). This potential orthostatic hypotension was not reported as an AE. Please assess the clinical significance (e.g., symptoms) and determine if AE reporting is required.
        *   **判断理由:** バイタルサインの変動が潜在的な有害事象（起立性低血圧）を示唆しており、AEとしての評価・報告が必要か確認するため。
        *   **判断根拠:**
            *   [関連するデータ: VSドメイン (VSTESTCD='SYSBP', VSPOS='STANDING', VISITNUM=3, 4)]
            *   [関連するプロトコル箇所: Section 3.9.3 (Safety)]
            *   [関連する医学的知見: 起立性低血圧の診断基準、Xanomelineの副作用]

    *   **クエリNo.:** Q-4 (関連指摘No.: D-6, P-3)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者（USUBJID: 01-701-1111）について、同意取得日 (Date/Time of Informed Consent) が記録されていません。治験実施前に適切に同意が取得されたことを確認するため、同意取得日をご提供ください。GCP遵守の観点から記録が必要です。
        *   **クエリ文面（英語）:** For subject 01-701-1111, the Date/Time of Informed Consent (RFICDTC) is missing in the DM domain. Please provide the date when informed consent was obtained to confirm GCP compliance.
        *   **判断理由:** GCP要件である同意取得日の記録が欠損しているため。
        *   **判断根拠:**
            *   [関連するデータ: [同意説明文書への署名日時(DM.RFICDTC)] = '']
            *   [関連するプロトコル箇所: Section 5.1 (Informed Consent)]
            *   [関連する医学的知見: GCP]

    *   **クエリNo.:** Q-5 (関連指摘No.: P-1, D-7)
        *   **重要度:** Major
        *   **発行担当者:** CRA
        *   **医療機関への問い合わせ文面:** 患者（USUBJID: 01-701-1111）について、プロトコルで規定されているスクリーニング時のECG、Visit 2での24時間ホルター心電図、およびVisit 4 (中止時) でのECGの実施記録または結果データが見当たりません。これらの検査が実施されたか、実施された場合はその結果をご提供いただけますでしょうか。安全性評価のために重要な情報です。
        *   **クエリ文面（英語）:** For subject 01-701-1111, records or results for protocol-specified ECGs (Screening, Visit 4/ET) and Ambulatory ECG (Visit 2) are missing. Please confirm if these assessments were performed and provide results if available. This is important for safety evaluation.
        *   **判断理由:** プロトコルで規定された重要な安全性評価の実施状況・結果が不明なため。
        *   **判断根拠:**
            *   [関連するデータ: ECG, EGドメインデータ欠損]
            *   [関連するプロトコル箇所: Attachment LZZT.1, Section 3.9.3.4.2, 3.9.4]

*   **内部確認事項 (問い合わせ不要):**
    *   **確認事項No.:** I-1 (関連指摘No.: M-4)
        *   **重要度:** Major
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Retrieval Visit (Day 169) におけるNPI-Xスコアの著しい悪化 (Baseline 2 -> Retrieval 45) を確認。治験中止から約5ヶ月経過しており疾患進行の可能性が高いが、治験薬中止との関連（離脱症状等）の可能性も念のため考慮し、内部で議論・記録する。他の症例でも同様の傾向がないか注視する。
        *   **判断理由:** 臨床的に顕著な変化であり、原因特定は困難でも、安全性監視の観点から内部での認識共有と記録が必要と判断したため。医療機関への問い合わせは、時間経過と疾患特性から有益な情報が得られる可能性が低いと判断。
        *   **判断根拠:**
            *   [関連するデータ: QSドメイン (QSTESTCD='NPTOT', VISITNUM=3, 4, 201)]
            *   [関連するプロトコル箇所: Section 3.9.3 (Safety)]
            *   [関連する医学的知見: アルツハイマー病の自然経過、薬剤離脱症状]

    *   **確認事項No.:** I-2 (関連指摘No.: M-5)
        *   **重要度:** Minor
        *   **確認担当者:** Medical Monitor
        *   **疑義事項/確認内容:** Week 2 (Day 11) のMCV高値 (101 fL) を確認。逸脱度は軽微であり、他の所見との関連も薄いため、現時点では追加アクション不要と判断。今後のデータで変動があれば再評価する。
        *   **判断理由:** 臨床的意義が低い可能性が高く、緊急性がないため内部確認のみとする。
        *   **判断根拠:**
            *   [関連するデータ: LBドメイン (LBTESTCD='MCV', VISITNUM=1, 4)]

    *   **確認事項No.:** I-3 (関連指摘No.: D-1)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** 有害事象「紅斑」「そう痒症」の記録に重複と転帰の矛盾があることを確認。Visit 4で回復済みのため、Visit 2収集分の転帰を修正するか、あるいは記録方法について内部で検討する。主要評価への影響は小さい。
        *   **判断理由:** データ品質の問題であり、修正要否を内部で判断するため。
        *   **判断根拠:**
            *   [関連するデータ: AEドメイン (AESEQ=1, 2, 4, 5)]

    *   **確認事項No.:** I-4 (関連指摘No.: D-2)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** MHとAEにおける「LOCALIZED INFECTION」の記録矛盾（重症度、開始日）を確認。データソースを確認し、修正要否を内部で検討する。
        *   **判断理由:** データ品質の問題であり、修正要否を内部で判断するため。
        *   **判断根拠:**
            *   [関連するデータ: MHドメイン (MHTERM='VERBATIM_1224'), AEドメイン (AETERM='LOCALISED INFECTION')]

    *   **確認事項No.:** I-5 (関連指摘No.: D-5)
        *   **重要度:** Minor
        *   **確認担当者:** DM
        *   **疑義事項/確認内容:** ビタミンB12、葉酸の検査結果データが欠損していることを記録する。除外基準[28b]に関連するが、組み入れ済みのため問題はなかったと推測される。
        *   **判断理由:** データの欠損状況を記録するため。
        *   **判断根拠:**
            *   [関連するデータ: LBドメイン]
            *   [関連するプロトコル箇所: Section 3.4.2.2 [28b]]

    *   **確認事項No.:** I-6 (関連指摘No.: D-8)
        *   **重要度:** Minor
        *   **確認担当者:** DM/CRA
        *   **疑義事項/確認内容:** DAD評価の"Going on an outing"関連項目がWeek 2でNAとなっている理由について、可能であればソースデータ等で確認し、記録する。有効性評価の解釈の補助情報とする。
        *   **判断理由:** 有効性データの解釈に関する補足情報であり、問い合わせるほどではないと判断。
        *   **判断根拠:**
            *   [関連するデータ: QSドメイン (DAITM25-29, VISITNUM=4)]

    *   **確認事項No.:** I-7 (関連指摘No.: P-2)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** プロトコル規定の中止時用量漸減が実施されたか不明確であることを記録する。EXデータではDay 10終了となっている。
        *   **判断理由:** プロトコル逸脱の可能性を記録するため。安全性への大きな影響は考えにくい。
        *   **判断根拠:**
            *   [関連するデータ: EXドメイン (EXENDTC, EXENDY)]
            *   [関連するプロトコル箇所: Section 3.10.1]

    *   **確認事項No.:** I-8 (関連指摘No.: P-3)
        *   **重要度:** Minor
        *   **確認担当者:** CRA
        *   **疑義事項/確認内容:** 選択基準[5]であるCNS imagingの結果がデータに含まれていないことを記録する。組み入れ時に確認されたはずだが、記録がない。
        *   **判断理由:** 組み入れ時の確認事項であり、事後確認の優先度は低いが記録は必要。
        *   **判断根拠:**
            *   [関連するデータ: CNS imagingデータなし]
            *   [関連するプロトコル箇所: Section 3.4.2.1 [5]]

    *   **確認事項No.:** I-9 (関連指摘No.: P-1, D-7)
        *   **重要度:** Minor
        *   **確認担当者:** CRA/DM
        *   **疑義事項/確認内容:** PKサンプルの採取状況に関するデータが欠損していることを記録する。
        *   **判断理由:** PK評価に関するデータ欠損状況を記録するため。
        *   **判断根拠:**
            *   [関連するデータ: PCドメインデータなし]
            *   [関連するプロトコル箇所: Section 3.9.2]