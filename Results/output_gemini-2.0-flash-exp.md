# 01-701-1146
## Task1: Clinical Review Results
## 1. 症例サマリーの作成:

**患者ID:** 01-701-1146

*   2013年05月07日 (Day -13): スクリーニング検査で、Alkaline Phosphatase (ALP) が 33 U/L と基準範囲下限を下回る。
*   2013年05月16日 (Day -4): Rashが発生。
*   2013年06月01日 (Day 13): Application Site Irritationが発生し、2013年06月02日 (Day 14)に回復。
*   2013年06月03日 (Day 15): Fatigueが発生。
*   2013年06月10日 (Day 22): Application Site ErythemaとApplication Site Pruritusが発生。
*   2013年06月16日 (Day 28): Application Site Erythemaが発現、Moderateに悪化。
*   2013年06月22日 (Day 34): Application Site Painが発現。
*   2013年06月26日 (Day 38): Application Site IrritationとApplication Site Vesiclesが発現。
*   2013年06月30日 (Day 42): Application Site ErythemaとApplication Site Pruritusが発現。ALPが 29 U/L と基準範囲下限を下回る。
*   2013年06月30日 (Day 42): Adverse Eventが発生したため、治験を中断。

---

## 2. クエリの作成 (必要な場合のみ):

**患者ID:** 01-701-1146

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AETERM = APPLICATION SITE ERYTHEMA, AESTDTC = 2013-06-10, AESEV = Moderate (7番のAE)
        *   AE.AETERM = APPLICATION SITE PRURITUS, AESTDTC = 2013-06-10, AESEV = Moderate (8番のAE)
        *   CM.CMTRT = HYDROCORTISONE, TOPICAL, CMSTDTC = 2013-06-12 (18, 19, 20, 21番のCM)
    *   **医療機関への問い合わせ文面:** Application Site ErythemaとApplication Site Pruritusが発現した2日後の2013-06-12に、HYDROCORTISONE, TOPICALを投与していますが、これはプロトコルに違反していないでしょうか？
    *   **判断理由:** hydrocortisone topical が投与された時期と、Application Site Erythema, Application Site Pruritusの発現時期が近いことから、局所症状の治療として投与された可能性があります。局所療法が許可されているかどうかの確認が必要です。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   AE.AETERM = RASH, AESTDTC = 2013-05-16, AEENDTC = 2013-06-02 (1番, 2番のAE)
        *   AE.AETERM = APPLICATION SITE IRRITATION, AESTDTC = 2013-06-01, AEENDTC = 2013-06-02 (3番のAE)
    *   **医療機関への問い合わせ文面:** RashとApplication Site Irritationに対し、何か処置は行われましたか？
    *   **判断理由:** RashとApplication Site Irritationが発現していますが、詳細な処置に関する情報が不足しているため、医療機関への確認が必要と考えられます。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:**
        *   DM.USUBJID = 01-701-1146, DTHDTC = "", RFPENDTC = "2013-07-15"
        *   DS.USUBJID = 01-701-1146, DSDECOD = "ADVERSE EVENT", DSSTDTC = "2013-06-30"
    *   **医療機関への問い合わせ文面:** USUBJIDが01-701-1146の被験者は、Adverse Eventにより試験を早期終了していますが、その後の追跡調査は適切に行われていますか？
    *   **判断理由:** 
        *   プロトコルに定められた追跡調査が適切に実施されているか確認する必要があります。
        *   DMドメインのRFPENDTC（Date/Time of End of Participation）が2013-07-15となっており、これはAE発生後のAE FOLLOW-UPのVisitと一致しています。DSドメインのDSSTDTC（Start Date/Time of Disposition Event）が2013-06-30で、これはWEEK6のVisitと一致しています。このことから、AE発生後の追跡調査が行われている可能性はありますが、DMドメインに死亡日が記録されていないため、追跡調査の内容を確認する必要があります。


## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMENDTC, CM.CMDOSU, MH.MHSTDTC

問題点:

*   問題No.: 1
    *   変数名と値: CM.CMENDTC = "" (空文字)
    *   矛盾の内容: USUBJIDが"01-701-1146"の被験者のConcomitant Medications (CM) データにおいて、BECONASEとDOCUSATEのCMENDTCが空文字になっています。CMENDTCは、Define.xmlにおいて必須ではありませんが、MedicationのEnd Date/Timeを示す重要な変数です。値が存在しない理由を確認する必要があります。
    *   問題点の原因（推測）: データ入力時の誤り、またはMedicationが継続して使用されているためEnd Dateが未定である可能性があります。
    *   対応策（提案）: 
        1.  CMENDTCが空文字になっている理由を医療機関に確認する。
        2.  Medicationがまだ継続している場合は、最新のCMENDTCを入力する。
        3.  Medicationが終了している場合は、終了日をCMENDTCに正しく入力する。

*   問題No.: 2
    *   変数名と値: CM.CMDOSU = "ug"
    *   矛盾の内容: USUBJIDが"01-701-1146"の被験者のConcomitant Medications (CM) データにおいて、PROVERAのCMDOSUが"ug"となっています。CMDOSE(Dose per Administration)が2.5の場合、単位が"ug"であることは、医学的に考えにくいです。ugではなくmgである可能性を考慮し、CMDOSUの値が正しいかどうかを確認する必要があります。
    *   問題点の原因（推測）: データ入力時の単位の誤り。
    *   対応策（提案）: 
        1.  CMDOSUの値が正しいかどうかを医療機関に確認する。
        2.  単位が誤っている場合は、正しい単位に修正する。

*   問題No.: 3
    *   変数名と値: MH.MHSTDTC = "" (空文字)
    *   矛盾の内容: USUBJIDが"01-701-1146"の被験者のMedical History (MH) データにおいて、POLYARTHRITISとHEARING LOSSのMHSTDTCが空文字になっています。MHSTDTCは、Define.xmlにおいて必須ではありませんが、Medical History EventのStart Date/Timeを示す変数です。値が存在しない理由を確認する必要があります。
    *   問題点の原因（推測）: データ入力時の誤り、または発症時期が不明である可能性があります。
    *   対応策（提案）: 
        1.  MHSTDTCが空文字になっている理由を医療機関に確認する。
        2.  MHSTDTCが不明な場合は、可能な範囲で推定し、入力する。

クエリの作成:

*   患者ID: 01-701-1146
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMENDTC = "" (空文字)
        *   医療機関への問い合わせ文面: USUBJIDが"01-701-1146"の被験者について、BECONASEとDOCUSATEの最終投与日をご教示ください。
        *   判断理由: 併用薬の投与期間は、有害事象の評価や有効性の評価に影響を与える可能性があるため。
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMDOSU = "ug"
        *   医療機関への問い合わせ文面: USUBJIDが"01-701-1146"の被験者について、PROVERAの投与単位はugで正しいでしょうか？
        *   判断理由: 併用薬の投与量は、安全性や有効性の評価に影響を与える可能性があるため。
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: MH.MHSTDTC = "" (空文字)
        *   医療機関への問い合わせ文面: USUBJIDが"01-701-1146"の被験者について、POLYARTHRITISとHEARING LOSSの発症時期をご教示ください。
        *   判断理由: 既往歴の発症時期は、試験結果の解釈に影響を与える可能性があるため。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1146

逸脱No.: 1
*   臨床試験結果への影響度合い: Minor
*   変数名と値: CM.CMDOSU = "ug", CM.CMDOSE = 2.5, CM.CMTRT = "PROVERA"
*   逸脱内容: 被験者01-701-1146は、PROVERA（メドロキシプロゲステロン酢酸エステル）を2.5ug/日 投与されている。プロトコルに違反している可能性。
*   プロトコル該当箇所:
*   判断理由: Proveraの一般的な投与量はmg単位であり、ug単位での投与は通常ありえない。単位の誤記、もしくは投与量の誤りの可能性がある。

クエリNo.: 1
*   臨床試験結果への影響度合い: Minor
*   変数名と値: CM.CMDOSU = "ug", CM.CMDOSE = 2.5, CM.CMTRT = "PROVERA"
*   医療機関への問い合わせ文面: 被験者01-701-1146に投与されているPROVERAの投与量と単位について確認させてください。正しくは2.5mgではないでしょうか？
*   判断理由: PROVERAの投与量単位がugと記録されているのは医学的に見て不自然であり、mgの誤記である可能性が高いため、確認が必要である。

# 01-703-1096
## Task1: Clinical Review Results
患者ID: 01-703-1096

*   2012年12月05日 (Day -51): スクリーニング検査で、Albumin 3.7 g/dL, Alkaline Phosphatase 98 U/L, Alanine Aminotransferase 12 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.09 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 11 mg/dL, Calcium 8.6 mg/dL, Cholesterol 195 mg/dL, Creatine Kinase 101 U/L, Chloride 110 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.11 THOU/uL, Gamma Glutamyl Transferase 8 U/L, Glucose 87 mg/dL, Hematocrit 45.0 %, Hemoglobin 13.8 g/dL, Potassium 4.8 mEq/L, Ketones 0, Lymphocytes 1.25 THOU/uL, Ery. Mean Corpuscular Hemoglobin 26 pg, Ery. Mean Corpuscular HGB Concentration 31 g/dL, Ery. Mean Corpuscular Volume 84 fL, Monocytes 0.35 THOU/uL, Sodium 141 mEq/L, pH 5.0, Phosphate 3.7 mg/dL, Platelet 219 THOU/uL, Protein 6.3 g/dL, Erythrocytes 5.40 MILL/uL, Specific Gravity 1.021, Thyrotropin 0.79 uIU/mL, Urate 4.1 mg/dL, Urobilinogen 0, Leukocytes 5.43 THOU/uL.
*   2012年12月19日 (Day -37): Hearing Decreased (MILD), 教育年数 6 YEARS。
*   2012年12月19日 (Day -37): Vital Signs 測定。Diastolic Blood Pressure (SUPINE) 74 mmHg, Diastolic Blood Pressure (STANDING) 62 mmHg, Diastolic Blood Pressure (STANDING) 78 mmHg, Systolic Blood Pressure (SUPINE) 132 mmHg, Systolic Blood Pressure (STANDING) 126 mmHg, Systolic Blood Pressure (STANDING) 130 mmHg, Pulse Rate (SUPINE) 78 BEATS/MIN, Pulse Rate (STANDING) 72 BEATS/MIN, Pulse Rate (STANDING) 84 BEATS/MIN, Temperature 098.0 F, Weight 180.0 LB。
*   2012年12月19日 (Day -37): Lymphocytes 1.45 THOU/uL。
*   2012年12月19日 (Day -37): Basophils 0.04 THOU/uL。
*   2012年12月19日 (Day -37): Eosinophils 0.07 THOU/uL。
*   2012年12月19日 (Day -37): Hematocrit 39.0 %。
*   2012年12月19日 (Day -37): Hemoglobin 12.6 g/dL。
*   2012年12月19日 (Day -37): Ery. Mean Corpuscular Hemoglobin 27 pg。
*   2012年12月19日 (Day -37): Ery. Mean Corpuscular HGB Concentration 32 g/dL。
*   2012年12月19日 (Day -37): Ery. Mean Corpuscular Volume 84 fL。
*   2012年12月19日 (Day -37): Monocytes 0.39 THOU/uL。
*   2012年12月19日 (Day -37): Modified Hachinski Ischemic Score 測定 (ABRUPT ONSET: ABSENT, STEPWISE DETERIORATION: ABSENT, FLUCTUATING COURSE: ABSENT, NOCTURNAL CONFUSION: ABSENT, RELATIVE PRESERVATION OF PERSONALITY: ABSENT, DEPRESSION: ABSENT, SOMATIC COMPLAINTS: ABSENT, EMOTIONAL INCONTINENCE: ABSENT, HISTORY OF HYPERTENSION: ABSENT, HISTORY OF STROKES: ABSENT, EVIDENCE OF ASSOCIATED ATHEROSCLEROSIS: ABSENT, FOCAL NEUROLOGICAL SYMPTOMS: ABSENT, FOCAL NEUROLOGICAL SIGNS: ABSENT)。
*   2012年12月19日 (Day -37): Mini-Mental State 測定 (WHAT IS THE (YEAR) (SEASON) (DATE) ?: 4, WHERE ARE WE: (STATE) (COUNTRY) (TOWN) ?: 3, NAME 3 OBJECTS: 1 SECOND TO SAY EACH.: 3, SERIAL 7'S. 1 POINT FOR EACH CORRECT.: 5, ASK FOR THE 3 OBJECTS REPEATED ABOVE.: 0, NAME A PENCIL, AND WATCH (2 POINTS): 7)。
*   2012年12月29日 (Day -27): ビタミンB12 203 pg/mL。
*   2013年01月23日 (Day -2): 血清検査で、Albumin 3.6 g/dL, Alkaline Phosphatase 87 U/L, Alanine Aminotransferase 11 U/L, Aspartate Aminotransferase 17 U/L, Basophils 0.05 THOU/uL, Bilirubin 0.3 mg/dL, Blood Urea Nitrogen 17 mg/dL, Calcium 8.7 mg/dL, Cholesterol 179 mg/dL, Creatine Kinase 85 U/L, Chloride 109 mEq/L, Color N, Creatinine 0.8 mg/dL, Eosinophils 0.06 THOU/uL, Gamma Glutamyl Transferase 8 U/L, Glucose 95 mg/dL, Hematocrit 39.0 %, Hemoglobin 12.7 g/dL, Potassium 4.9 mEq/L, Ketones 0, Lymphocytes 1.47 THOU/uL, Ery. Mean Corpuscular Hemoglobin 27 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 83 fL, Monocytes 0.45 THOU/uL, Sodium 143 mEq/L, pH 5.0, Phosphate 3.2 mg/dL, Platelet 260 THOU/uL, Protein 6.5 g/dL, Erythrocytes 4.70 MILL/uL, Specific Gravity 1.027, Thyrotropin 0.86 uIU/mL, Urate 3.8 mg/dL, Urobilinogen 0, Leukocytes 7.13 THOU/uL。
*   2013年01月25日 (Day 1): 
    *   ADAS-Cog(11) Subscore 16
    *   UNDERTAKE TO WASH HIMSELF/HERSELF: Yes
    *   UNDERTAKE TO BRUSH HIS/HER TEETH: Yes
    *   DECIDE TO CARE FOR HIS/HER HAIR: Yes
    *   PREPARE FOR WASHING, TAKING A BATH: Yes
    *   WASH AND DRY COMPLETELY SAFELY: Yes
    *   BRUSH HIS/HER TEETH: Yes
    *   CARE FOR HIS/HER HAIR: Yes
    *   UNDERTAKE TO DRESS HIMSELF/HERSELF: Yes
    *   CHOOSE APPROPRIATE CLOTHING: Yes
    *   DRESS HIMSELF/HERSELF: Yes
    *   DRESS HIMSELF/HERSELF COMPLETELY: Yes
    *   UNDRESS HIMSELF/HERSELF COMPLETELY: Yes
    *   DECIDE TO USE THE TOILET AT APPROPRIATE: Yes
    *   USE THE TOILET WITHOUT "ACCIDENTS": Yes
    *   DECIDE THAT HE/SHE NEEDS TO EAT: Yes
    *   CHOOSE APPROPRIATE UTENSILS: Yes
    *   EAT HIS/HER MEALS AT A NORMAL PACE: Yes
    *   UNDERTAKE TO PREPARE A LIGHT MEAL: Yes
    *   ADEQUATELY PLAN A LIGHT MEAL OR SNACK: Yes
    *   PREPARE OR COOK A LIGHT MEAL OR A SNACK: Yes
    *   ATTEMPT TO TELEPHONE SOMEONE: Yes
    *   FIND AND DIAL A TELEPHONE NUMBER CORRECT: No
    *   CARRY OUT A TELEPHONE CONVERSATION: Yes
    *   WRITE AND CONVEY A TELEPHONE MESSAGE: No
    *   UNDERTAKE TO GO OUT: Yes
    *   ADEQUATELY ORGANIZE AN OUTING: No
    *   GO OUT AND REACH A FAMILIAR DESTINATION: Yes
    *   SAFELY TAKE CAR, BUS, TAXI: No
    *   RETURN FROM THE STORE: No
    *   INTEREST IN HIS/HER PERSONAL AFFAIRS: No
    *   PAY HIS/HER BILLS: No
    *   ORGANIZE HIS/HER CORRESPONDENCE: Yes
    *   HANDLE ADEQUATELY HIS/HER MONEY: No
    *   DECIDE TO TAKE HIS/HER MEDICATIONS: Yes
    *   TAKE HIS/HER MEDICATIONS AS PRESCRIBED: Yes
    *   SHOW AN INTEREST IN LEISURE ACTIVITY: Yes
    *   TAKE AN INTEREST IN HOUSEHOLD CHORES: Yes
    *   PLAN AND ORGANIZE HOUSEHOLD CHORES: No
    *   COMPLETE HOUSEHOLD CHORES: No
    *   STAY SAFELY AT HOME BY HIMSELF/HERSELF: Yes
*   2013年02月09日 (Day 16):
    *  Modified Hachinski Ischemic Score 測定。URATE 3.9 mg/dL, Blood Urea Nitrogen 16 mg/dL, CA 9.2 mg/dL, CHOL 190 mg/dL, CL 107 mEq/L, CREAT 0.9 mg/dL, GGT 11 U/L, Potassium 4.6 mEq/L, SODIUM 140 mEq/L, PHOS 3.9 mg/dL.
*   2013年02月09日 (Day 16):
    *   DEPRESSION/DYSPHORIA FREQUENCY 1
    *   DEPRESSION/DYSPHORIA SEVERITY 1
    *   DEPRESSION/DYSPHORIA DISTRESS 2
    *   DEPRESSION/DYSPHORIA Score 1
    *   AGITATION/AGRESSION FREQUENCY 1
    *   AGITATION/AGRESSION SEVERITY 1
    *   AGITATION/AGRESSION DISTRESS 2
    *   AGITATION/AGRESSION Score 1
    *   APATHY/INDIFFERENCE FREQUENCY 1
    *   APATHY/INDIFFERENCE SEVERITY 1
    *   APATHY/INDIFFERENCE DISTRESS 2
    *   APATHY/INDIFFERENCE Score 1
    *   ABERRANT MOTOR BEHAVIOR FREQUENCY 3
    *   ABERRANT MOTOR BEHAVIOR SEVERITY 2
    *   ABERRANT MOTOR BEHAVIOR DISTRESS 3
    *   ABERRANT MOTOR BEHAVIOR Score 6
    *   NIGHT-TIME BEHAVIOR FREQUENCY 4
    *   NIGHT-TIME BEHAVIOR SEVERITY 1
    *   NIGHT-TIME BEHAVIOR DISTRESS 0
    *   NIGHT-TIME BEHAVIOR Score 0
    *   APPETITE/EATING CHANGE FREQUENCY 1
    *   APPETITE/EATING CHANGE SEVERITY 2
    *   APPETITE/EATING CHANGE DISTRESS 0
    *   APPETITE/EATING CHANGE Score 0
    *   NPI-X (9) Total Score 10
*   2013年02月09日 (Day 16): Vital Signs 測定。Systolic Blood Pressure (STANDING) 150 mmHg, Diastolic Blood Pressure (STANDING) 80 mmHg, Pulse Rate (STANDING) 74 BEATS/MIN。
*   2013年02月23日 (Day 30):
    *  Blood Urea Nitrogen 16 mg/dL, Ca 8.8 mg/dL, CHOL 184 mg/dL, CL 106 mEq/L, CREAT 0.9 mg/dL, GGT 11 U/L, GLUC 94 mg/dL, K 4.6 mEq/L, PHOS 3.8 mg/dL, PROT 6.5 g/dL, SODIUM 140 mEq/L, URATE 3.8 mg/dL, Basophils 0.05 THOU/uL, EOS 0.07 THOU/uL, HGB 12.5 g/dL, LYM 1.63 THOU/uL, MCH 27 pg, NPI-X (9) Total Score 13, Anistocytes, DELUSIONS Score 0, HALLUCINATIONS Score 0, Agitation/Aggression Score 2, Anxiety Score 0, APATHY/INDIFFERENCE Score 3, Disinhibition Score 0, IRRITABILITY/LABILITY Score 2, ABERRANT MOTOR BEHAVIOR Score 4, NIGHT-TIME BEHAVIOR Score 0, APPETITE/EATING CHANGE Score 0, MCHC , 0.9 mg/dL, MCV fL, Monocytes 0.54 THOU/uL, Platelet 232 THOU/uL, RBC 4.70 MILL/uL, SPGRAV, TSH, UROBIL, Wbc 6.03 THOU/uL.
*  2013年02月23日 (Day 30): Vital Signs 測定。Systolic Blood Pressure (STANDING) 140 mmHg, Diastolic Blood Pressure (STANDING) 80 mmHg, Pulse Rate (STANDING) 78 BEATS/MIN。
*   2013年03月29日 (Day 64): UNABLE TO CONTACT PATIENT (LOST TO FOLLOW-UP)。

---

**クエリ:**

患者ID: 01-703-1096

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** DS.DSTERM = "UNABLE TO CONTACT PATIENT (LOST TO FOLLOW-UP)", DS.DSSTDTC = "2013-03-29"
    *   **医療機関への問い合わせ文面:** 
        *   USUBJIDが01-703-1096の被験者が、WEEK 6の訪問時に「UNABLE TO CONTACT PATIENT (LOST TO FOLLOW-UP)」と記録されています。プロトコルでは、WEEK 24に評価を行うために、早期中止された被験者を呼び戻すように指示されています。この被験者を追跡する努力は行われましたか？もしそうであれば、どのような結果が得られましたか？
    *   **判断理由:** 主要評価項目であるADAS-CogとCIBIC+スコアに影響を与える可能性があるため。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** EX.EXTRT = "PLACEBO", EX.EXDOSE = 0, EX.EXSTDTC = "2013-02-10", EX.EXENDTC = "2013-03-16"
    *   **医療機関への問い合わせ文面:** 
        *   USUBJIDが01-703-1096の被験者は、2013-02-10から2013-03-16までプラセボ投与を受けていると記録されています。DS.DSTERMが "UNABLE TO CONTACT PATIENT (LOST TO FOLLOW-UP)"であるにもかかわらず、これは矛盾しています。
    *   **判断理由:** 矛盾しているため。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTEST = "MMITM04", QSORRES="5"
    *   **医療機関への問い合わせ文面:** 
        *  MMITM04は"SERIAL 7'S. 1 POINT FOR EACH CORRECT."という質問ですが、回答が7であることはあり得ません。0から5の間であるべきです。
    *   **判断理由:** QSドメインの矛盾。

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: 
    *   DM.RFICDTC
    *   VS.VSORRES

問題点:

*   問題No.: 1
    *   変数名と値: DM.RFICDTC = ""
    *   矛盾の内容: DM.RFICDTC が欠損している。プロトコルには「倫理審査委員会が承認したインフォームドコンセントは、試験の性質を説明した後、患者（および/または法定代理人）および介護者によって署名される」と記載されており、DM.RFICDTC にはインフォームドコンセントの署名日時が記録されるはずである。しかし、データが欠損している。
    *   問題点の原因（推測）: 
        *   データ入力エラー
        *   インフォームドコンセント未取得
    *   対応策（提案）: インフォームドコンセントの取得状況を確認し、日付を修正または追記する。

*   問題No.: 2
    *   変数名と値: VS.VSORRES = "080" (VSSEQ=16,17,18)
    *   矛盾の内容: VS.VSORRES の値が "080" と "80" で混在している。Define.xmlでは VSORRES のデータ型は text であり、VSSTRESN のデータ型は decimal であるため、VSORRES に数値の 0 が含まれる文字列が記録されている場合、データ型変換時にエラーが発生する可能性がある。
    *   問題点の原因（推測）: データ入力時のタイプミス
    *   対応策（提案）: VSORRES の値を "80" に修正する。

クエリ:

*   患者ID: 01-703-1096
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: DM.RFICDTC = ""
        *   医療機関への問い合わせ文面:
            *   DM.RFICDTC（インフォームドコンセント取得日時）が空欄になっています。インフォームドコンセントを取得した日付と時刻をご教示ください。もしインフォームドコンセントが取得されていない場合、理由をご説明ください。
        *   判断理由: インフォームドコンセントは臨床試験参加に必須であり、その取得日は重要な情報であるため。


## Task3: Protocol Deviation Review Results
患者ID: 01-703-1096
    *   逸脱No.: 1
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: DM.AGE = 49, TS.AGEMIN = 50 years
        *   逸脱内容: 被験者01-703-1096は、年齢が49歳であり、プロトコルで規定されている最小年齢50歳という組み入れ基準を満たしていません。
        *   プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [1]
        *   判断理由: DMドメインのAGE変数が49歳であるのに対し、TSドメイン（Trial Summary）のAGEMIN変数が50歳と定義されているため、組み入れ基準に違反していると判断しました。
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: DM.AGE = 49
        *   医療機関への問い合わせ文面: 被験者01-703-1096のDM.AGEが49歳となっていますが、登録時の年齢を確認してください。
        *   判断理由: DMドメインのAGE変数が49歳となっていますが、データ入力時の誤りの可能性も考慮し、念のため医療機関に確認します。



# 01-703-1279
## Task1: Clinical Review Results
患者ID: 01-703-1279

* 2013年04月27日 (Day -16):
    *   医学的既往歴として、アルツハイマー病および関節炎の既往歴が報告されています。
    *   MMSEは7点。 Modified Hachinski Ischemic Scaleは0点。
    *   身長:162.56cm, 体重:56.25kg, 体温:36.33℃
    *   バイタルサイン測定は、臥位、立位1分後、立位3分後の血圧と脈拍が記録されています。
    *   臨床検査では、HCTとHGBが高値でした。
* 2013年05月11日 (Day -2):
    *   バイタルサイン測定は、臥位、立位1分後、立位3分後の血圧と脈拍が記録されています。
    *   体温:36℃
* 2013年05月13日 (Day 1):
    *   ADAS-Cog(11) Subscore: 28点。NPI-X (9) Total Score: 24点。
    *   開始された治験薬はXANOMELINE 54mg、投与経路は経皮。
    *   バイタルサイン測定は、臥位、立位1分後、立位3分後の血圧と脈拍が記録されています。
    *   体重:55.79kg, 体温:36.56℃
* 2013年06月22日 (Day 41):
    *   ADAS-COGは28点から43点に悪化。NPI-X (9) Total Scoreは24点から43点に悪化。
    *   Disterbility Assesment for Dementiaの多くの項目で、自立度が低下。
    *   起立3分後の血圧が測定されていません。
    *   体重:54.89kg, 体温:36.33℃

---

患者ID: 01-703-1279

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   VS.VSSTAT (Day 41, 立位3分後): "NOT DONE"
    *   **医療機関への問い合わせ文面:**
        *   Day 41（WEEK 2）の立位3分後の血圧が「NOT DONE」となっていますが、測定されなかった理由を教えてください。
    *   **判断理由:**
        *   プロトコルでは、立位での血圧測定は1分後と3分後の両方で実施されることが定められています。
        *   立位3分後の血圧測定が実施されなかった場合、起立性低血圧の評価に影響が出る可能性があります。
*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   QS.QSTESTCD (Day 41): ADAS-COG, NPIのスコアが、Day1と比較して悪化
    *   **医療機関への問い合わせ文面:**
        *   ADAS-COGとNPIのスコアが、Day1と比較してWEEK2で悪化していますが、その理由を教えてください。
    *   **判断理由:**
        *   認知機能、精神症状が悪化している場合、安全性に影響を及ぼす可能性があります。
*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:**
        * DS.DSTERM: "CAREGIVER BECAME ILL"
    *   **医療機関への問い合わせ文面:**
        *   治験を中止した理由が「CAREGIVER BECAME ILL」となっていますが、詳細を教えてください。また、その理由が本治験に影響を与える可能性はありますか。
    *   **判断理由:**
        *  主要評価項目であるADAS-Cog, CIBIC+の評価がなされないまま治験が中止されており、有効性の評価が困難です。また、安全性に影響を及ぼす可能性もあります。
*   **クエリNo.:** 4
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   QS.DAITM15(Day 1): "Y"
        *   QS.DAITM15(Day 41): "N"
        *   QS.DAITM40(Day 1): "Y"
        *   QS.DAITM40(Day 41): "N"
    *   **医療機関への問い合わせ文面:**
        *   Disability Assessment for Dementia (DAD)のQ40(STAY SAFELY AT HOME BY HIMSELF/HERSELF)と、Q15(DECIDE THAT HE/SHE NEEDS TO EAT)について、DAY1では「Y」、WEEK2では「N」と回答されています。ADLが低下した理由を教えてください。
    *   **判断理由:**
        *   DADのQ40(STAY SAFELY AT HOME BY HIMSELF/HERSELF)と、Q15(DECIDE THAT HE/SHE NEEDS TO EAT)は、ADLを評価する上で重要な項目です。
## Task2: DM Review Results
```markdown
全体的なデータ品質の評価:
    総合評価: 一部問題あり
    データクリーニング/再調査が必要な項目: MH.MHSTDTC, DS.DSDTC, VS.VSSTAT, VSの欠損値, QS.QSORRES, QS.QSSTRESN

問題点:
    問題No.: 1
        変数名と値: DM.MHSTDTC = "" (Medical Historyドメイン)
        矛盾の内容: MH.MHSTDTCが""（空）である。Define.xmlでは必須変数と定義されているため、空の値は許容されない。
        問題点の原因（推測）: データ入力時のエラーまたは情報不足。
        対応策（提案）: MH.MHSTDTCに適切な日付を入力するか、データが収集されなかった理由を特定する。Define.xmlの定義を見直すことも検討。

    問題No.: 2
        変数名と値: DS.DSDTC = "2013-04-27T11:00"
        矛盾の内容: DS.VISITが"SCREENING 1"であるにも関わらず、DSDTCが時刻情報を持っている。一般的に、スクリーニングのようなイベントでは時刻情報は不要と考えられる。
        問題点の原因（推測）: データ入力時の誤り、またはデータ収集手順の不備。
        対応策（提案）: 
          1.  DSDTCから時刻情報を削除する。
          2.  時刻情報が必要な理由がある場合は、その根拠を明確にする。

    問題No.: 3
        変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE" (Medical Historyドメイン), TI.IETEST = "Diagnosis of probable AD as defined by NINCDS and the ADRDA guidelines" (Trial Inclusion/Exclusion Criteria)
        矛盾の内容: USUBJIDが"01-703-1279"の被験者のMedical Historyに「ALZHEIMER'S DISEASE」の既往歴が登録されている。しかし、この試験はアルツハイマー病患者を対象としているため、組み入れ基準を満たしている必要がある。Medical Historyに記載されているアルツハイマー病が、今回の試験に登録されたアルツハイマー病と同一の病状を指しているか確認が必要。
        問題点の原因（推測）: 
            1.  Medical Historyの記載が誤っている。
            2.  登録されたアルツハイマー病と過去のアルツハイマー病が異なる。
        対応策（提案）: 
            1.  医療機関にMedical Historyの記載内容を確認する。
            2.  登録時の詳細な病歴を確認し、組み入れ基準を満たしているか再評価する。

    問題No.: 4
        変数名と値: VS.VSSTAT = "NOT DONE", VS.VSTEST = "Diastolic Blood Pressure" (Vital Signsドメイン)
        矛盾の内容: USUBJIDが"01-703-1279"の被験者のWEEK 2のVISITにおいて、Diastolic Blood PressureのAFTER STANDING FOR 3 MINUTESの測定が"NOT DONE"となっている。しかし、他の時点の血圧測定は実施されている。
        問題点の原因（推測）: 
            1.  測定忘れ
            2.  患者の状態により測定できなかった
        対応策（提案）: 
            1.  測定されなかった理由を特定するために、医療機関に問い合わせを行う。
            2.  プロトコルに規定された血圧測定手順が遵守されているか確認する。

    問題No.: 5
        変数名と値: 複数のQSレコード (Questionnairesドメイン)
        矛盾の内容: DAITM15, DAITM19, DAITM20, DAITM21, DAITM22, DAITM25, DAITM26, DAITM27, DAITM28, DAITM29, DAITM30, DAITM31, DAITM32, DAITM33, DAITM34, DAITM35, DAITM37, DAITM38, DAITM39, DAITM40などの多くのDisability Assessment for Dementia (DAD)質問項目において、ベースライン（VISITNUM=3）では"Y"（はい）と回答されているにもかかわらず、WEEK 2（VISITNUM=4）では"N"（いいえ）と回答されている。症状の悪化が急速に進んでいる可能性がある。
        問題点の原因（推測）:
            1.  評価の誤りまたは評価者間での基準の相違
            2.  患者の状態の急速な悪化
            3.  データ入力時の誤り
        対応策（提案）:
            1.  医療機関に詳細な症状の経過と評価の根拠を確認する。
            2.  評価者間トレーニングを実施し、評価基準の統一を図る。

    問題No.: 6
        変数名と値: QSORRES, QSSTRESN (Questionnairesドメイン)
        矛盾の内容: ADAS-COG評価項目(ACITM01-ACITM14)において、QSORRESの値(文字列)とQSSTRESNの値(数値)が一致している。ADAS-COG評価項目のQSSTRESNは計算によって得られるはずなので、QSORRESの値をそのままコピーしている可能性がある。Define.xmlのComputationMethodを確認する必要がある。
        問題点の原因（推測）: データ入力時の誤り、またはデータ変換ロジックの誤り。
        対応策（提案）:
            1.  ADAS-COG評価項目のQSSTRESNの計算方法を再確認し、データ変換ロジックに誤りがないか確認する。
            2.  データ入力担当者に対し、QSSTRESNの計算方法を再教育する。

クエリの作成 (必要な場合のみ):
    患者ID: 01-703-1279
        クエリNo.: 1
            臨床試験結果への影響度合い: Major
            変数名と値: DS.DSTERM = "CAREGIVER BECAME ILL", DS.DSSTDTC = "2013-06-22"
            医療機関への問い合わせ文面: 
             *   DS.DSTERMが「CAREGIVER BECAME ILL」となっていますが、詳細な状況（病名、重症度、患者への影響など）について教えてください。
             *   本件が、臨床試験に登録されている被験者の継続的な介護にどのような影響を与えたか教えてください。
            判断理由: 
                *   治験責任医師が被験者の継続的な介護に重大な影響を及ぼすと判断した場合、治験を中止することがあります。
                *   介護者の状況は、被験者のADL、認知機能、行動に影響を与える可能性があり、臨床試験の結果に影響を与える可能性があります。

```
## Task3: Protocol Deviation Review Results
**患者ID:** 01-703-1279
*   **逸脱No.:** 1
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, DSDTC = 2013-06-22, EXENDTC = 2013-06-03, VISIT = WEEK 2
    *   **逸脱内容:** 被験者はWEEK2（2013-06-22）に脱落しているが、治験薬の最終投与日は2013-06-03であり、投与期間が26週間の試験において、投与期間が大幅に短い。
    *   **プロトコル該当箇所:**
        *   セクション 3.1 Summary of Study Design
        *   セクション 3.10 Patient Disposition Criteria
    *   **判断理由:** 試験デザインでは26週間の投与期間が計画されているが、被験者はそれよりも大幅に短い期間で治験薬投与を中止している。

*   **逸脱No.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSTESTCD = DIABP, VS.VISIT = WEEK 2, VS.VSTPT = AFTER STANDING FOR 3 MINUTES, VS.VSSTAT = NOT DONE
    *   **逸脱内容:** 
        *   治験参加者は、WEEK2の診察時に、立位3分後のDiastolic Blood Pressure (DIABP)測定が実施されていない。
        *   Vital Signs測定手順の不履行
    *   **プロトコル該当箇所:** 3.9.3.4.1 Vital Sign Determination
    *   **判断理由:** Vital Signs測定手順の不履行はプロトコルからの逸脱にあたる。

*   **逸脱No.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSTESTCD = SYSBP, VS.VISIT = WEEK 2, VS.VSTPT = AFTER STANDING FOR 3 MINUTES, VS.VSSTAT = NOT DONE
    *   **逸脱内容:**
        *   治験参加者は、WEEK2の診察時に、立位3分後のSystolic Blood Pressure(SYSBP)測定が実施されていない。
        *   Vital Signs測定手順の不履行
    *   **プロトコル該当箇所:** 3.9.3.4.1 Vital Sign Determination
    *   **判断理由:** Vital Signs測定手順の不履行はプロトコルからの逸脱にあたる。

*   **逸脱No.:** 4
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM15, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD) 質問票の評価において、 
        *   「DECIDE THAT HE/SHE NEEDS TO EAT」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 5
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM19, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「ADEQUATELY PLAN A LIGHT MEAL OR SNACK」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 6
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM20, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「PREPARE OR COOK A LIGHT MEAL OR A SNACK」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 7
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM21, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「ATTEMPT TO TELEPHONE SOMEONE」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 8
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM22, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「FIND AND DIAL A TELEPHONE NUMBER CORRECT」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 9
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM24, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「WRITE AND CONVEY A TELEPHONE MESSAGE」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 10
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM25, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「UNDERTAKE TO GO OUT」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 11
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM26, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「ADEQUATELY ORGANIZE AN OUTING」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 12
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM27, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「GO OUT AND REACH A FAMILIAR DESTINATION」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 13
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM28, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「SAFELY TAKE CAR, BUS, TAXI」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 14
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM29, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「RETURN FROM THE STORE」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 15
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM30, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「INTEREST IN HIS/HER PERSONAL AFFAIRS」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 16
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM31, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「PAY HIS/HER BILLS」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 17
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM32, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「ORGANIZE HIS/HER CORRESPONDENCE」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 18
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM33, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「HANDLE ADEQUATELY HIS/HER MONEY」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 19
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM34, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「DECIDE TO TAKE HIS/HER MEDICATIONS」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 20
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM35, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「TAKE HIS/HER MEDICATIONS AS PRESCRIBED」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 21
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM37, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「TAKE AN INTEREST IN HOUSEHOLD CHORES」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 22
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM38, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「PLAN AND ORGANIZE HOUSEHOLD CHORES」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 23
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM39, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「COMPLETE HOUSEHOLD CHORES」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 24
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = DAITM40, VISIT = WEEK 2, QSORRES = N
    *   **逸脱内容:** 
        *   Disability Assessment for Dementia (DAD)質問票の評価において、 
        *   「STAY SAFELY AT HOME BY HIMSELF/HERSELF」項目の評価が「N」となっている。
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 25
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM01F, VISIT = WEEK 2, NPITM01F = 3, NPITM01V = 2, NPITM01D = 4
    *   **逸脱内容:** 
        *    NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   DELUSIONS 
            * FREQUENCY:3
            * SEVERITY: 2
            * DISTRESS: 4
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 26
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM03F, VISIT = WEEK 2, NPITM03F = 4, NPITM03V = 2, NPITM03D = 4
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   AGITATION/AGRESSION
            * FREQUENCY:4
            * SEVERITY: 2
            * DISTRESS: 4
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 27
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM04F, VISIT = WEEK 2, NPITM04F = 3, NPITM04V = 2, NPITM04D = 3
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   DEPRESSION/DYSPHORIA
            * FREQUENCY:3
            * SEVERITY: 2
            * DISTRESS: 3
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 28
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM05F, VISIT = WEEK 2, NPITM05F = 3, NPITM05V = 2, NPITM05D = 3
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   ANXIETY
            * FREQUENCY:3
            * SEVERITY: 2
            * DISTRESS: 3
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 29
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM07F, VISIT = WEEK 2, NPITM07F = 3, NPITM07V = 2, NPITM07D = 3
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   APATHY/INDIFFERENCE
            * FREQUENCY:3
            * SEVERITY: 2
            * DISTRESS: 3
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 30
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM10F, VISIT = WEEK 2, NPITM10F = 3, NPITM10V = 1, NPITM10D = 2
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   ABERRANT MOTOR BEHAVIOR
            * FREQUENCY:3
            * SEVERITY: 1
            * DISTRESS: 2
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 31
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM11F, VISIT = WEEK 2, NPITM11F = 3, NPITM11V = 2, NPITM11D = 3
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   NIGHT-TIME BEHAVIOR
            * FREQUENCY:3
            * SEVERITY: 2
            * DISTRESS: 3
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 32
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT, QSTESTCD = NPITM12F, VISIT = WEEK 2, NPITM12F = 3, NPITM12V = 1, NPITM12D = 2
    *   **逸脱内容:** 
        *   NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)質問票の評価において、
        *   APPETITE/EATING CHANGE
            * FREQUENCY:3
            * SEVERITY: 1
            * DISTRESS: 2
        *   「CAREGIVER BECAME ILL」という脱落理由を考慮すると、評価の妥当性に疑義が残る。
    *   **プロトコル該当箇所:** 3.9.1.1 Efficacy Measures
    *   **判断理由:** 質問票の回答に影響を与える事象が発生している可能性があり、評価の妥当性に疑義が残るため。

*   **逸脱No.:** 33
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSDTCとSV.SVSTDTCの乖離
    *   **逸脱内容:** QS.QSDTC (2013-05-13)と、対応するSV.SVSTDTC (2013-05-13)が一致している必要があるが、データセット全体を通して確認した結果、タイムスタンプが設定されていないため判断できない。
    *   **プロトコル該当箇所:** 不明
    *   **判断理由:** データ収集時のタイムスタンプ取得に関するプロトコルの指示が不明確なため。

*   **逸脱No.:** 34
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VSTPT が""(null)である。
    *   **逸脱内容:** 
        *   Vital Signsデータセット(VS)において、TEMP (体温)とWEIGHT (体重)のVSTPT(Planned Time Point Name)がnullである。
        *   プロトコルで規定された時間点の情報が欠落している。
    *   **プロトコル該当箇所:** 3.9.3.4.1 Vital Sign Determination
    *   **判断理由:** 
        *   Vital Signs測定手順において、体温と体重は時間点との関連が不明確であるため。

*   **逸脱No.:** 35
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = ALZHEIMER'S DISEASE
    *   **逸脱内容:**
        *   Medical HistoryにALZHEIMER'S DISEASEの既往歴がある。
        *   TI(Trial Incl/Excl)にExclusion Criteria（EXCL12）として "Diagnosis of serious neurological conditions" が存在する。
        *   医学的既往歴と除外基準の整合性に疑義がある。
    *   **プロトコル該当箇所:** Section 3.4.2.2 Exclusion Criteria [12] Diagnosis of serious neurological conditions
    *   **判断理由:**
        *   TI(Trial Incl/Excl)にExclusion Criteriaとして "Diagnosis of serious neurological conditions" が存在するため、AD診断がEXCL12に抵触しないか確認が必要。

---
**クエリ:**
*   **患者ID:** 01-703-1279
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** DSDECOD = WITHDRAWAL BY SUBJECT
        *   **医療機関への問い合わせ文面:**
            *   被験者01-703-1279がWEEK2で試験を中止した理由が「CAREGIVER BECAME ILL」とのことですが、具体的にどのような状況だったのか、詳細を教えてください。特に、Disability Assessment for Dementia (DAD)やRevised Neuropsychiatric Inventory (NPI-X)質問票の回答に影響を与える可能性はありましたでしょうか。
        *   **判断理由:**
            *   治験薬の投与期間が短く、WEEK2のDAD質問票のいくつかの項目において評価が「N」となっている。
            *   脱落理由が質問票の評価に影響を与えている可能性がある。
            *   脱落理由と質問票の回答内容について、医療機関への確認が必要である。

*   **患者ID:** 01-703-1279
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** MH.MHTERM = ALZHEIMER'S DISEASE
        *   **医療機関への問い合わせ文面:**
            *   被験者01-703-1279のMedical HistoryにおいてALZHEIMER'S DISEASEが記録されていますが、登録時の診断基準と症状の程度について詳細な情報をご提供いただけますでしょうか？
            *   特に、この状態がプロトコルの除外基準EXCL12（Diagnosis of serious neurological conditions）に該当しないという判断の根拠についてご説明をお願いいたします。
        *   **判断理由:**
            *   DMデータに72歳とあるため、本試験の対象となる軽度から中程度のアルツハイマー病患者である可能性が高い。
            *   念のため、ALZHEIMER'S DISEASEの診断がEXCL12の除外基準に抵触しないか確認するため、医療機関への問い合わせが必要。



# 01-704-1008
## Task1: Clinical Review Results
患者ID: 01-704-1008

*   2012年11月25日 (Day -49): スクリーニング検査でビリルビン値が1.3 mg/dL (基準値上限1.2 mg/dL) と高値を示す。甲状腺刺激ホルモン(TSH)が0.24 uIU/mL (基準値下限0.32 uIU/mL) と低値を示す。
*   2012年06月01日 (Day -225): 四肢の振戦、筋硬直、動作緩慢といった有害事象が発現。
*   2013年01月06日 (Day -7): スクリーニング検査で教育レベルが12年と報告される。
*   2013年01月13日 (Day 1): 
    *   ベースライン評価として、ワード・リコール・タスクが7点、物体と指の名前付けが0点、遅延ワード・リコールが6点、指示が1点、構成的実行が3点、観念的実行が0点、見当識が0点、単語認識が0点、注意/視覚探索タスクが13点、迷路課題が11秒、発語能力が0点、口頭言語の理解度が2点、自発発話における単語検索困難が1点、テスト指示の想起が1点と報告される。ADAS-Cog(11)サブスコアは15点。Disability Assessment for Dementia (DAD)の各項目はすべて「Y」(1点)と評価される。
    *   神経精神症状評価（NPI-X）では妄想、幻覚、アパシー/無関心、脱抑制の項目は「なし」と評価される。不安の頻度は1、重症度は2、介護者の苦痛は1と評価される。
*   2013年01月28日 (Day 16): 
    *   NPI-Xの各項目を評価した結果、すべての項目で症状は認められなかった。
    *   アルブミンが3.7 g/dL (基準値下限3.5 g/dL)と基準値内。ガンマグルタミルトランスフェラーゼ(GGT)が8 U/L (基準値範囲5-50 U/L)と基準値内。
*   2013年02月09日 (Day 28): 
    *   NPI-Xの評価において不安の頻度が2、重症度が2、介護者の苦痛度が4に増加。
    *   検査値プロテイン5.8 g/dL (基準値下限6.0 g/dL)と低値を示す。尿酸値が2.4 mg/dL (基準値下限2.5 mg/dL)と低値を示す。
*   2013年02月25日 (Day 44): 
    *   WEEK6の最終検査でクレアチンキナーゼ(CK)が189 U/L (基準値上限169 U/L)と高値を示す。ADVERSE EVENTが発生し、ADVERSE EVENTとして処理された。
    *    NPI-Xの評価において不安の頻度が3、重症度が3、介護者の苦痛度が3に増加。

---

患者ID: 01-704-1008

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AESTDTC = 2012-06-01
        *   AE.AEENDTC = 2013-02-21 (AESEQ=2のみ)
    *   **医療機関への問い合わせ文面:** 有害事象「TREMOR IN HANDS, LEGS」、「MUSCLE STIFFNESS」、「SLOWNESS of MOVEMENT」の開始日について、正しくはいつでしょうか？
        また、有害事象「SLOWNESS of MOVEMENT」の治癒日は2013年2月21日で正しいでしょうか？
    *   **判断理由:** Medical Historyには2011年10月17日にアルツハイマー病と診断された記録がある。今回、Adverse Eventとして記録されている有害事象の開始日が2012年6月1日となっており、Medical Historyに記録されているアルツハイマー病の診断日よりも前である。
        アルツハイマー病と診断される前から兆候が見られていた可能性も考えられるが、TREMOR IN HANDS, LEGS (手足の振戦), MUSCLE STIFFNESS (筋硬直), SLOWNESS of MOVEMENT (動作緩慢)は、アルツハイマー病の症状と類似しているため、Adverse Eventとして扱うべきかMedical Historyとして扱うべきか判断に迷う。
        定義上は、Adverse Eventは投与後に発生した有害事象を指すため、開始日を確認する必要がある。
*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   VS.VSTESTCD = TEMP
        *   VS.VSORRES = 098.4
    *   **医療機関への問い合わせ文面:** 体温測定(TEMP)の original units (VSORRES) が098.4となっておりますが、98.4の間違いではないでしょうか？
    *   **判断理由:** データ入力時のtypoの可能性がある。
*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   QS.QSTESTCD = DAITM24
        *   QS.QSSTRESC (WEEK6) = 0
    *   **医療機関への問い合わせ文面:** DADの質問項目DAITM24(WRITE AND CONVEY A TELEPHONE MESSAGE)について、week6の回答がN(0)になっていますが、これは以前からできなかったのか、それとも新たに出来なくなったのか、カルテを確認してください。
    *   **判断理由:** MMSE, CIBIC, DAD, NPI-Xの結果から、認知機能は悪化傾向にある。DADの質問項目WRITE AND CONVEY A TELEPHONE MESSAGEの結果が悪化していることと整合性が取れる。


## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMSTDTC, CM.CMENDTC, AE.AESTDTC, AE.AEENDTC, VS.VSDTC

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** CM.CMTRT = MULTIVITAMIN, CM.CMSTDTC = "2004", CM.CMENDTC = null
    *   **矛盾の内容:** CM.CMTRT (マルチビタミン) のCMSTDTCが2004年となっているが、これは試験開始日(2013-01-13)よりも9年前である。また、CMENDTCがnullとなっており、併用薬の使用期間が不明。
    *   **問題点の原因（推測）:** データ入力エラー、または情報収集時の不備。
    *   **対応策（提案）:** 
        1.  医療機関にCMSTDTCの正確な日付を確認する。
        2.  CMENDTCの値を確認し、必要であれば修正する。

*   **問題No.2:**
    *   **変数名と値:** CM.CMTRT = SYNTHROID, CM.CMSTDTC = "2012-12-09", CM.CMENDTC = "2013-02-07", DM.RFSTDTC = "2013-01-13"
    *   **矛盾の内容:** 甲状腺ホルモン剤であるSYNTHROIDのCMENDTCが2013年2月7日となっているが、これはDM.RFENDTC (2013-02-25)よりも早い。SYNTHROIDは継続的に服用する薬剤である可能性が高く、試験期間中も服用していたのであれば矛盾が生じる。
    *   **問題点の原因（推測）:** データ入力エラー、または情報収集時の不備。
    *   **対応策（提案）:** 
        1.  医療機関にCMENDTCの正確な日付を確認する。
        2.  2013年2月7日以降もSYNTHROIDを継続して服用していたか確認する。
        3.  継続して服用していた場合、CMENDTCをDM.RFENDTC以降の日付に修正する。

*   **問題No.3:**
    *   **変数名と値:** CM.CMTRT = TYLENOL, CM.CMSTDTC = "1986", CM.CMENDTC = null
    *   **矛盾の内容:** CM.CMTRT (TYLENOL) のCMSTDTCが1986年となっているが、これは試験開始日(2013-01-13)よりも27年前である。また、CMENDTCがnullとなっており、併用薬の使用期間が不明。
    *   **問題点の原因（推測）:** データ入力エラー、または情報収集時の不備。頓服薬であるため、正確な服用期間が記録されていない可能性がある。
    *   **対応策（提案）:** 
        1.  医療機関にCMSTDTCの正確な日付を確認する。
        2.  TYLENOLは頓服薬であると考えられるため、CMENDTCはnullのままで良いか確認する。

*   **問題No.4:**
    *   **変数名と値:** AE.AETERM = TREMOR IN HANDS, LEGS, AE.AESTDTC = "2012-06-01", AE.AEENDTC = null, DM.RFSTDTC = "2013-01-13"
    *   **矛盾の内容:** AE.AESTDTC (2012-06-01) がDM.RFSTDTC (2013-01-13)よりも前である。TREMOR IN HANDS, LEGSは治験薬投与前から存在していたことになる。SUPPAE.QVALでAETRTEM = "Y"となっているため、矛盾が生じる。
    *   **問題点の原因（推測）:** データ入力エラー、または有害事象の開始日の誤り。
    *   **対応策（提案）:** 
        1.  AESTDTCの正確な日付を確認する。
        2.  治験薬投与前からTREMOR IN HANDS, LEGSが存在していた場合、SUPPAE.QVALの値を"N"に修正することを検討する。

*   **問題No.5:**
    *   **変数名と値:** AE.AETERM = MUSCLE STIFFNESS, AE.AESTDTC = "2012-06-01", AE.AEENDTC = null, DM.RFSTDTC = "2013-01-13"
    *   **矛盾の内容:** AE.AESTDTC (2012-06-01) がDM.RFSTDTC (2013-01-13)よりも前である。MUSCLE STIFFNESSは治験薬投与前から存在していたことになる。SUPPAE.QVALでAETRTEM = "Y"となっているため、矛盾が生じる。
    *   **問題点の原因（推測）:** データ入力エラー、または有害事象の開始日の誤り。
    *   **対応策（提案）:** 
        1.  AESTDTCの正確な日付を確認する。
        2.  治験薬投与前からMUSCLE STIFFNESSが存在していた場合、SUPPAE.QVALの値を"N"に修正することを検討する。

*   **問題No.6:**
    *   **変数名と値:** AE.AETERM = SLOWNESS of MOVEMENT, AE.AESTDTC = "2012-06-01", AE.AEENDTC = "2013-02-21", DM.RFSTDTC = "2013-01-13"
    *   **矛盾の内容:** AE.AESTDTC (2012-06-01) がDM.RFSTDTC (2013-01-13)よりも前である。SLOWNESS of MOVEMENTは治験薬投与前から存在していたことになる。SUPPAE.QVALでAETRTEM = "Y"となっているため、矛盾が生じる。
    *   **問題点の原因（推測）:** データ入力エラー、または有害事象の開始日の誤り。
    *   **対応策（提案）:** 
        1.  AESTDTCの正確な日付を確認する。
        2.  治験薬投与前からSLOWNESS of MOVEMENTが存在していた場合、SUPPAE.QVALの値を"N"に修正することを検討する。

*   **問題No.7:**
    *   **変数名と値:** LB.LBTESTCD = TSH, LB.LBORRES = "0.24", LB.LBORNRLO = "0.32", LBNRIND = "LOW", VISIT = "SCREENING 1"
    *   **矛盾の内容:** 甲状腺刺激ホルモン (TSH) の値が基準範囲より低い (0.24 < 0.32) にもかかわらず、 Exclusion Criteria 28 に「Central laboratory test values below reference range for folate, and vitamin B12, and outside reference range for thyroid function tests.」と記載されているため、組み入れ基準を満たしているか確認が必要となる。
    *   **問題点の原因（推測）:** TSH以外の甲状腺機能検査値が正常範囲内であったか、または治験責任医師が臨床的に問題ないと判断した可能性がある。
    *   **対応策（提案）:**
        1.  Define.xmlに「The values that were used to specify abnormal test results with FLAG in LB domain(SUPPLB or LB field)」のような記述を追加し、除外基準の判断に使用されたデータを示す。
        2.  症例の除外基準を再度確認する。

*   **問題No.8:**
    *   **変数名と値:** VS.VSTESTCD = TEMP, VS.VSORRES = "098.4", VSDTC = "2013-02-25"
    *   **矛盾の内容:** VSORRESが"098.4"となっており、数値として不適切である。先頭の0は入力ミスと考えられる。
    *   **問題点の原因（推測）:** データ入力エラー
    *   **対応策（提案）:** 
        1.  医療機関にVSORRESの正確な値を確認する。
        2.  正しい値に修正する。

**クエリの作成:**

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = MULTIVITAMIN, CM.CMSTDTC = "2004", CM.CMENDTC = null
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008の併用薬MULTIVITAMINの開始日（CMSTDTC）が2004年となっておりますが、正 しい日付をご教示ください。また、MULTIVITAMINの終了日（CMENDTC）をご教示ください。
        *   **判断理由:** 併用薬の使用期間は、安全性評価や薬物相互作用の評価に重要な情報であるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = SYNTHROID, CM.CMSTDTC = "2012-12-09", CM.CMENDTC = "2013-02-07"
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008の併用薬SYNTHROIDの終了日（CMENDTC）が2013年2月7日となっておりますが、正 しい日付をご教示ください。特に、試験終了日（2013年2月25日）まで継続して服用していたか否かを確認させてください。
        *   **判断理由:** 併用薬の使用期間は、安全性評価や薬物相互作用の評価に重要な情報であるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMTRT = TYLENOL, CM.CMSTDTC = "1986", CM.CMENDTC = null
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008の併用薬TYLENOLの開始日（CMSTDTC）が1986年となっておりますが、正 しい日付をご教示ください。TYLENOLは頓服薬であると考えられますが、服用頻度など、使用状況についても可能な範囲で情報提供をお願いいたします。
        *   **判断理由:** 併用薬の使用状況は、安全性評価に影響する可能性があるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 4
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** AE.AETERM = TREMOR IN HANDS, LEGS, AE.AESTDTC = "2012-06-01"
        *   **医療機関への問い合わせ文面:**
             被験者01-704-1008に発生した有害事象「TREMOR IN HANDS, LEGS」の開始日（AESTDTC）が2012年6月1日となっておりますが、正しい日付をご教示ください。特に、治験薬投与前に既に症状が存在していたか否かを確認させてください。
        *   **判断理由:** 治験薬との因果関係を評価する上で、有害事象の発現時期は非常に重要な情報であるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 5
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** AE.AETERM = MUSCLE STIFFNESS, AE.AESTDTC = "2012-06-01"
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008に発生した有害事象「MUSCLE STIFFNESS」の開始日（AESTDTC）が2012年6月1日となっておりますが、正しい日付をご教示ください。特に、治験薬投与前に既に症状が存在していたか否かを確認させてください。
        *   **判断理由:** 治験薬との因果関係を評価する上で、有害事象の発現時期は非常に重要な情報であるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 6
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** AE.AETERM = SLOWNESS of MOVEMENT, AE.AESTDTC = "2012-06-01"
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008に発生した有害事象「SLOWNESS of MOVEMENT」の開始日（AESTDTC）が2012年6月1日となっておりますが、正しい日付をご教示ください。特に、治験薬投与前に既に症状が存在していたか否かを確認させてください。
        *   **判断理由:** 治験薬との因果関係を評価する上で、有害事象の発現時期は非常に重要な情報であるため。

*   **患者ID:** 01-704-1008
    *   **クエリNo.:** 7
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** VS.VSTESTCD = TEMP, VS.VSORRES = "098.4"
        *   **医療機関への問い合わせ文面:**
            被験者01-704-1008の体温（TEMP）が"098.4"となっておりますが、正しい値をご教示ください。
        *   **判断理由:** バイタルサインのデータ正確性は安全性評価に影響を与える可能性があるため。

クエリなし

## Task3: Protocol Deviation Review Results
患者ID: 01-704-1008
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2011-10-17
    *   逸脱内容: 被験者の医学的病歴にアルツハイマー病が含まれている。プロトコルの除外基準には、重篤な神経学的状態の診断が含まれており、アルツハイマー病もこれに該当する可能性がある。
    *   プロトコル該当箇所: 除外基準12
    *   判断理由: Medical History (MH) ドメインには「ALZHEIMER'S DISEASE」という病歴が含まれており、プロトコルの除外基準に抵触する可能性があるため。

患者ID: 01-704-1008
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2011-10-17
    *   医療機関への問い合わせ文面: 被験者「01-704-1008」の医学的病歴にある「ALZHEIMER'S DISEASE」は、本試験に登録する上で除外基準に該当する「重篤な神経学的状態」と判断された根拠について、詳細な医学的判断と理由をご教示ください。
    *   判断理由: 
        *   プロトコルの除外基準に「重篤な神経学的状態」が含まれており、アルツハイマー病がこれに該当するかどうかを確認する必要があるため。
        *   除外基準の解釈は治験の対象集団に影響を与え、試験結果の解釈にも影響を与える可能性があるため。


# 01-701-1383
## Task1: Clinical Review Results
**1. 症例サマリー**

*   **患者ID:** 01-701-1383
    *   2013年01月22日 (Day -13): スクリーニング1回目の検査で、Albumin 3.9 g/dL, Alkaline Phosphatase 66 U/L, Alanine Aminotransferase 17 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 8 mg/dL, Calcium 8.9 mg/dL, Cholesterol 213 mg/dL, Creatine Kinase 96 U/L, Chloride 107 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.07 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 95 mg/dL, Hematocrit 40.0 %, Hemoglobin 13.7 g/dL, Potassium 4.3 mEq/L, Ketones 0, Lymphocytes 1.77 THOU/uL, Ery. Mean Corpuscular Hemoglobin 32 pg, Ery. Mean Corpuscular HGB Concentration 34 g/dL, Ery. Mean Corpuscular Volume 94 fL, Monocytes 0.26 THOU/uL, Sodium 143 mEq/L, pH 6.0, Phosphate 4.0 mg/dL, Platelet 341 THOU/uL, Protein 6.8 g/dL, Erythrocytes 4.30 MILL/uL, Specific Gravity 1.011, Thyrotropin 3.66 uIU/mL, Urate 3.3 mg/dL, Urobilinogen 0, Leukocytes 5.08 THOU/uL.
    *   2013年02月07日 (Day 4): Application site pruritusとApplication site painが発生し、軽度であったが、プロバブルと判断された。
    *   2013年02月19日 (Day 16): Week2回目の検査で、Albumin 3.8 g/dL, Alkaline Phosphatase 66 U/L, Alanine Aminotransferase 17 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 12 mg/dL, Calcium 9.4 mg/dL, Cholesterol 203 mg/dL, Creatine Kinase 75 U/L, Chloride 106 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.10 THOU/uL, Gamma Glutamyl Transferase 14 U/L, Glucose 87 mg/dL, Hematocrit 40.0 %, Hemoglobin 12.9 g/dL, Potassium 4.8 mEq/L, Ketones 0, Lymphocytes 1.28 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 32 g/dL, Ery. Mean Corpuscular Volume 92 fL, Monocytes 0.31 THOU/uL, Sodium 139 mEq/L, pH 6.0, Phosphate 3.8 mg/dL, Platelet 341 THOU/uL, Protein 6.6 g/dL, Erythrocytes 4.40 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.5 mg/dL, Urobilinogen 0, Leukocytes 6.73 THOU/uL.
    *   2013年03月12日 (Day 37): Week4回目の検査で、Albumin 4.0 g/dL, Alkaline Phosphatase 61 U/L, Alanine Aminotransferase 14 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.4 mg/dL, Blood Urea Nitrogen 9 mg/dL, Calcium 9.1 mg/dL, Cholesterol 177 mg/dL, Creatine Kinase 119 U/L, Chloride 105 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.06 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 87 mg/dL, Hematocrit 38.0 %, Hemoglobin 12.5 g/dL, Potassium 4.4 mEq/L, Ketones 0, Lymphocytes 1.78 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 93 fL, Monocytes 0.29 THOU/uL, Sodium 137 mEq/L, pH 6.0, Phosphate 4.0 mg/dL, Platelet 308 THOU/uL, Protein 6.5 g/dL, Erythrocytes 4.10 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.2 mg/dL, Urobilinogen 0, Leukocytes 5.28 THOU/uL.
    *   2013年03月14日 (Day 39): Baselineから投与されたXanomeline 54mgが、この日まで投与された。
    *   2013年03月23日 (Day 48): Application site erythemaとApplication site pruritusが発生し、軽度であったが、ポッシブルと判断された。
    *   2013年03月19日 (Day 44): Week6回目の検査で、Albumin 3.9 g/dL, Alkaline Phosphatase 63 U/L, Alanine Aminotransferase 17 U/L, Aspartate Aminotransferase 23 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 9 mg/dL, Calcium 9.4 mg/dL, Cholesterol 183 mg/dL, Creatine Kinase 95 U/L, Chloride 106 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.05 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 86 mg/dL, Hematocrit 39.0 %, Hemoglobin 13.0 g/dL, Potassium 4.5 mEq/L, Ketones 0, Lymphocytes 1.36 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 34 g/dL, Ery. Mean Corpuscular Volume 91 fL, Monocytes 0.27 THOU/uL, Sodium 137 mEq/L, pH 6.0, Phosphate 4.0 mg/dL, Platelet 330 THOU/uL, Protein 6.8 g/dL, Erythrocytes 4.30 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.5 mg/dL, Urobilinogen 0, Leukocytes 4.56 THOU/uL.
    *   2013年04月02日 (Day 58): Week8回目の検査で、Albumin 4.0 g/dL, Alkaline Phosphatase 56 U/L, Alanine Aminotransferase 18 U/L, Aspartate Aminotransferase 25 U/L, Basophils 0.05 THOU/uL, Bilirubin 0.3 mg/dL, Blood Urea Nitrogen 10 mg/dL, Calcium 9.1 mg/dL, Cholesterol 177 mg/dL, Creatine Kinase 142 U/L, Chloride 105 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.13 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 83 mg/dL, Hematocrit 40.0 %, Hemoglobin 12.6 g/dL, Potassium 3.5 mEq/L, Ketones 0, Lymphocytes 1.59 THOU/uL, Ery. Mean Corpuscular Hemoglobin 29 pg, Ery. Mean Corpuscular HGB Concentration 32 g/dL, Ery. Mean Corpuscular Volume 90 fL, Monocytes 0.23 THOU/uL, Sodium 139 mEq/L, pH 6.0, Phosphate 3.6 mg/dL, Platelet 356 THOU/uL, Protein 6.8 g/dL, Erythrocytes 4.40 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.4 mg/dL, Urobilinogen 0, Leukocytes 4.48 THOU/uL. Application site erythemaとApplication site pruritusが継続し、軽度であったが、ポッシブルと判断された。
    *   2013年04月12日 (Day 68): Application site irritationが発生し、軽度であったが、ポッシブルと判断された。
    *   2013年04月30日 (Day 86): Week12回目の検査で、Albumin 3.9 g/dL, Alkaline Phosphatase 57 U/L, Alanine Aminotransferase 13 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.6 mg/dL, Blood Urea Nitrogen 13 mg/dL, Calcium 9.0 mg/dL, Cholesterol 190 mg/dL, Creatine Kinase 85 U/L, Chloride 110 mEq/L, Color N, Creatinine 1.0 mg/dL, Eosinophils 0.29 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 94 mg/dL, Hematocrit 38.0 %, Hemoglobin 12.9 g/dL, Potassium 4.6 mEq/L, Ketones 0, Lymphocytes 1.72 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 34 g/dL, Ery. Mean Corpuscular Volume 90 fL, Monocytes 0.31 THOU/uL, Sodium 139 mEq/L, pH 5.0, Phosphate 4.5 mg/dL, Platelet 296 THOU/uL, Protein 6.5 g/dL, Erythrocytes 4.20 MILL/uL, Specific Gravity 1.022, Thyrotropin 3.66 uIU/mL, Urate 3.6 mg/dL, Urobilinogen 0, Leukocytes 5.67 THOU/uL. Application site erythemaとApplication site irritationが継続し、軽度であったが、ポッシブルと判断された。
    *   2013年05月07日 (Day 93): Application site vesiclesが発生し、軽度であったが、ポッシブルと判断された。
    *   2013年05月30日 (Day 116): Week16回目の検査で、Albumin 4.0 g/dL, Alkaline Phosphatase 60 U/L, Alanine Aminotransferase 19 U/L, Aspartate Aminotransferase 25 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 10 mg/dL, Calcium 9.6 mg/dL, Cholesterol 186 mg/dL, Creatine Kinase 99 U/L, Chloride 105 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.22 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 92 mg/dL, Hematocrit 39.0 %, Hemoglobin 13.4 g/dL, Potassium 4.2 mEq/L, Ketones 0, Lymphocytes 1.77 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 87 fL, Monocytes 0.35 THOU/uL, Sodium 138 mEq/L, pH 6.0, Phosphate 3.9 mg/dL, Platelet 346 THOU/uL, Protein 7.0 g/dL, Erythrocytes 4.40 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.0 mg/dL, Urobilinogen 0, Leukocytes 5.07 THOU/uL。Application site irritationとApplication site pruritusが発生し、中等度であったが、ポッシブルと判断された。
    *   2013年06月24日 (Day 141): HeadacheとChest discomfortが発生し、軽度であったが、いずれも関連なしと判断された。
    *   2013年06月25日 (Day 142): Week20回目の検査で、Albumin 4.2 g/dL, Alkaline Phosphatase 64 U/L, Alanine Aminotransferase 19 U/L, Aspartate Aminotransferase 21 U/L, Basophils 0.05 THOU/uL, Bilirubin 0.4 mg/dL, Blood Urea Nitrogen 12 mg/dL, Calcium 8.8 mg/dL, Cholesterol 202 mg/dL, Creatine Kinase 128 U/L, Chloride 108 mEq/L, Color N, Creatinine 1.0 mg/dL, Eosinophils 0.21 THOU/uL, Gamma Glutamyl Transferase 12 U/L, Glucose 88 mg/dL, Hematocrit 40.0 %, Hemoglobin 13.1 g/dL, Potassium 4.5 mEq/L, Ketones 0, Lymphocytes 1.90 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 92 fL, Monocytes 0.35 THOU/uL, Sodium 143 mEq/L, pH 6.0, Phosphate 4.1 mg/dL, Platelet 314 THOU/uL, Protein 7.0 g/dL, Erythrocytes 4.30 MILL/uL, Specific Gravity 1.016, Thyrotropin 3.66 uIU/mL, Urate 3.5 mg/dL, Urobilinogen 0, Leukocytes 5.91 THOU/uL。
    *   2013年07月17日 (Day 164): 血圧上昇を伴うCoughが発生し、中等度であったが、関連なしと判断された。
    *   2013年07月30日 (Day 177): Week24回目の検査で、Albumin 4.1 g/dL, Alkaline Phosphatase 58 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 8 mg/dL, Calcium 9.6 mg/dL, Cholesterol 185 mg/dL, Creatine Kinase 113 U/L, Chloride 105 mEq/L, Color N, Creatinine 1.0 mg/dL, Eosinophils 0.09 THOU/uL, Gamma Glutamyl Transferase 11 U/L, Glucose 88 mg/dL, Hematocrit 38.0 %, Hemoglobin 12.9 g/dL, Potassium 4.4 mEq/L, Ketones 0, Lymphocytes 1.63 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 34 g/dL, Ery. Mean Corpuscular Volume 90 fL, Monocytes 0.34 THOU/uL, Sodium 139 mEq/L, pH 7.0, Phosphate 3.9 mg/dL, Platelet 370 THOU/uL, Protein 7.0 g/dL, Erythrocytes 4.20 MILL/uL, Specific Gravity 1.017, Thyrotropin 3.66 uIU/mL, Urate 3.2 mg/dL, Urobilinogen 0, Leukocytes 5.53 THOU/uL. 血圧上昇を伴う咳が軽快した。
    *   2013年08月06日 (Day 184): Week26回目の検査で、Albumin 3.8 g/dL, Alkaline Phosphatase 53 U/L, Alanine Aminotransferase 14 U/L, Aspartate Aminotransferase 17 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 10 mg/dL, Calcium 9.0 mg/dL, Cholesterol 188 mg/dL, Creatine Kinase 98 U/L, Chloride 107 mEq/L, Color N, Creatinine 0.9 mg/dL, Eosinophils 0.09 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 95 mg/dL, Hematocrit 37.0 %, Hemoglobin 12.4 g/dL, Potassium 4.1 mEq/L, Ketones 0, Lymphocytes 1.78 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 91 fL, Monocytes 0.33 THOU/uL, Sodium 143 mEq/L, pH 6.0, Phosphate 3.9 mg/dL, Platelet 315 THOU/uL, Protein 6.5 g/dL, Erythrocytes 4.10 MILL/uL, Specific Gravity 1.017, Thyrotropin 3.66 uIU/mL, Urate 3.3 mg/dL, Urobilinogen 0, Leukocytes 5.57 THOU/uL.

---

**2. クエリの作成**

*   **患者ID:** 01-701-1383
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2013-03-23, AE.AEENDTC = 2013-03-26, AE.AETERM = APPLICATION SITE ERYTHEMA (AESEQ=3)
        *   **医療機関への問い合わせ文面:**
            *   Application site erythema（AE.AETERM）のAESTDTCとAEENDTCが矛盾している可能性があります。SDTMの仕様では、AEENDTCがAESTDTCよりも早い日付になることは許容されていません。症例01-701-1383について、Application site erythemaの正確なAESTDTCとAEENDTCをご教示ください。
        *   **判断理由:**
            *   AEドメインの重要な変数であるAESTDTCとAEENDTCの値に矛盾が認められるため、データの正確性を確認する必要がある。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**  VS.DIABP (Visit 12, Week 24, Position SUPINE) = 98 mmHg
        *   **医療機関への問い合わせ文面:**
            *   Visit 12 (Week 24) における仰臥位でのDiastolic Blood Pressure (VS.DIABP)が98 mmHgと高めですが、この値に影響を与えた要因（例: 測定時の状況、患者の状態など）はありますでしょうか？
        *   **判断理由:**
            *   安全性に関する重要な指標である血圧の異常値について、その原因や背景を確認し、患者の安全性を評価する必要がある。


## Task2: DM Review Results
### データ整合性レビュー

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMSTDTC, AE.AESTDTC, VS.VSDTC, 全般的な日付の整合性

*   **問題点:**

    *   **問題No.: 1**
        *   **変数名と値:** CM.CMTRT = CENTRUM SILVER, CM.CMSTDTC = "2012-03", CM.CMDTCの複数の日付 = "2013-01-22"など
        *   **矛盾の内容:** USUBJIDが "01-701-1383" の被験者の併用薬（CM）データにおいて、CMSTDTC（薬剤の開始日）がすべて2012年3月と記録されていますが、CMDTC（データ収集日）は2013年の日付です。CMSTDTCがCMDTCより10ヶ月以上古い日付となっており、矛盾しています。
        *   CMTRTがCENTRUM SILVERであるすべてのレコードでCMSTDTCが"2012-03"となっています。
        *   また、CEPHALEXINとHYDROCORTISONEのCMTRTのレコードでは、CMENDTCに値が入っているものと入っていないものが混在しています。
        *   HYDROCORTISONEのCMTRTのレコードでは、CMDTCに値が入っているにもかかわらずCMENDTCが空欄となっています。
        *   CENTRUUM SILVERのCMTRTのレコードでは、CMSTDYとCMENDYがNULLとなっています。
    *   **問題点の原因（推測）:**
        *   データ入力エラーの可能性。
        *   併用薬の開始日の記録方法の誤り（月のみ記録など）。
    *   **対応策（提案）:**
        *   CMSTDTC、CMENDTC、CMDTCについて原資料を確認し、正しい日付に修正してください。CMENDTCが存在しない場合はNULLを設定してください。CMSTDYとCMENDYも再計算してください。
        *   CMTRTがCENTRUM SILVERであるすべてのレコードについて、CMSTDTCが本当にすべて同じ日付で良いか確認してください。
        *   HYDROCORTISONEのCMTRTのレコードについて、CMENDTCが空欄で良いか確認してください。
    *   **問題No.: 2**
        *   **変数名と値:** DM.RFSTDTC = "2013-02-04", DM.RFXSTDTC = "2013-02-04", CM.CMSTDTC = "2012-03" (複数レコード)
        *   **矛盾の内容:** DM.RFSTDTC（Subject Reference Start Date/Time）およびDM.RFXSTDTC（Date/Time of First Study Treatment）は、治験薬の最初の投与日を示すものですが、CM.CMSTDTC（Concomitant Medication Start Date/Time）は2012年3月となっており、治験薬投与開始日よりも前の日付となっています。
    *   **問題点の原因（推測）:**
        *   データ入力エラーの可能性。
        *   併用薬の開始日の記録方法の誤り（月のみ記録など）。
    *   **対応策（提案）:**
        *   CM.CMSTDTCについて原資料を確認し、DM.RFSTDTCおよびDM.RFXSTDTCとの整合性を確認してください。
        *   必要に応じてCM.CMSTDTCを修正してください。
    *   **問題No.: 3**
        *   **変数名と値:** AE.AESTDTC = "2013-03-23", AE.AEDTC = "2013-04-02" (APPLICATION SITE ERYTHEMA, AESEQ=3), AE.AESTDTC = "2013-02-07", AE.AEDTC = "2013-02-19"(APPLICATION SITE PRURITUS, AESEQ=1,5)
        *   **矛盾の内容:** AE.AEDTC（Date/Time of Collection）は有害事象が報告された日付ですが、AE.AESTDTC（Start Date/Time of Adverse Event）よりも後の日付になっています。AE.AEDTCがAE.AESTDTCより前の日付であるべきです。
    *   **問題点の原因（推測）:**
        *   データ入力エラーの可能性。
        *   データ収集日の誤り。
    *   **対応策（提案）:**
        *   AE.AESTDTCとAE.AEDTCについて原資料を確認し、矛盾を修正してください。
    *   **問題No.: 4**
        *   **変数名と値:** VS.VSDTC = "2013-01-22", DM.DMDTC = "2013-01-22", DM.RFSTDTC = "2013-02-04"
        *   **矛盾の内容:** DM.RFSTDTC（Subject Reference Start Date/Time）は2013年2月4日ですが、VS.VSDTC（Date/Time of Measurements）は2013年1月22日、DM.DMDTC(Date/Time of Collection)も2013年1月22日となっています。DM.RFSTDTCはDM.DMDTCよりも前の日付になることは通常ありません。
    *   **問題点の原因（推測）:**
        *   データ入力エラーの可能性。
        *   DM.RFSTDTCの記録方法の誤り。
    *   **対応策（提案）:**
        *   DM.RFSTDTCについて原資料を確認し、DM.DMDTCおよびVS.VSDTCとの整合性を確認してください。
        *   必要に応じてDM.RFSTDTCを修正してください。
    *   **問題No.: 5**
        *   **変数名と値:** EX.EXENDTC = "2013-02-19", EX.EXSTDTC = "2013-02-04",EXDOSE = "54", 4, "WEEK 2", 14, EX.EXENDTC = "2013-07-30", EX.EXSTDTC = "2013-02-20", EXDOSE = "81"
        *   **矛盾の内容:** 治験薬を54mg投与した期間は2013-02-04から2013-02-19までで16日間であるのに対し、その後81mgに増量してWEEK2(2013-02-20)から投与を開始し、WEEK24(2013-07-30)まで投与したと解釈できます。しかし、AEデータを見ると、適用部位の掻痒感、紅斑、刺激感などの有害事象がWEEK2(2013-02-19)よりも後であるWEEK8(2013-04-02)以降も継続して発生しています。治験薬との関連性がPROBABLEあるいはPOSSIBLEと判断されているにもかかわらず、治験薬との因果関係が評価された後に減量や投与中止などの処置が取られていません。
    *   **問題点の原因（推測）:**
        *   有害事象に対する処置の記録漏れの可能性。
        *   データ入力時のAESTDTC、AEENDTCまたはAEACNの記録漏れ。
        *   EXとAEのデータ間の関連性の評価の不備。
    *   **対応策（提案）:**
        *   有害事象発生時の処置（AEACN）について、原資料を確認してください。
        *   EXデータとAEデータの関連性を再評価し、必要に応じて処置の実施状況を確認してください。

### クエリの作成

*   患者ID: 01-701-1383
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMSTDTC, CM.CMDTC
        *   医療機関への問い合わせ文面:
            *   患者ID "01-701-1383" の併用薬CENTRUM SILVERについて、投与開始日（CMSTDTC）とデータ収集日（CMDTC）に矛盾が見られます。
            *   CMSTDTCは2012年3月となっていますが、CMDTCは2013年1月22日以降となっています。
            *   正しい投与開始日とデータ収集日をご教示ください。
        *   判断理由: 併用薬の使用期間が正確に把握できない場合、安全性や有効性の評価に影響を及ぼす可能性があります。
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC、AE.AEENDTC、EX.EXSTDTC、EX.EXENDTC、AE.AEACN
        *   医療機関への問い合わせ文面:
            *   患者ID "01-701-1383" において、治験薬投与期間中に適用部位の掻痒感、紅斑、刺激感などの有害事象が複数回発生しています。
            *   治験薬との関連性（AEREL）がPOSSIBLEまたはPROBABLEと評価されているにもかかわらず、治験薬の投与量変更や投与中止などの処置（AEACN）が記録されていません。
            *   これらの有害事象に対する臨床的な判断と対応についてご教示ください。
        *   判断理由: 治験薬との関連性が疑われる有害事象に対する適切な対応がなされなかった場合、患者の安全性が損なわれる可能性があります。また、有害事象が治験薬の効果に影響を与えている可能性も考慮する必要があります。
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: DM.RFSTDTC, DM.DMDTC, VS.VSDTC
        *   医療機関への問い合わせ文面:
            *   患者ID "01-701-1383" において、Subject Reference Start Date/Time (DM.RFSTDTC)とDate/Time of Collection(DM.DMDTC, VS.VSDTC)に矛盾が見られます。
            *   DM.RFSTDTCは2013-02-04ですが、DM.DMDTCとVS.VSDTCは2013-01-22となっています。
            *    Subject Reference Start Date/Time (DM.RFSTDTC)は正しく2013-02-04で良いか、DM.DMDTC、VS.VSDTCのどちらかの日付に誤りがないか確認をお願いします。
        *   判断理由: 登録日に関する矛盾のため、重要度はMinorと判断しました。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1383
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, DM.AGE = 72
    *   逸脱内容: この被験者はアルツハイマー病の病歴を有している。プロトコルの除外基準EXCL12に抵触する可能性がある。EXCL12では「重篤な神経学的状態の診断」を除外基準としている。アルツハイマー病が「重篤な神経学的状態」に該当するかどうかは医学的判断が必要。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [12]
    *   判断理由: MHデータセットにアルツハイマー病の既往歴があるため、除外基準に抵触する可能性がある。

*   患者ID: 01-701-1383
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, DM.AGE = 72
        *   医療機関への問い合わせ文面:
            *   被験者01-701-1383の医学的病歴について、以下の点を確認させてください。
                1.  アルツハイマー病の診断時期と重症度。
                2.  選択基準INCL02（NINCDSおよびADRDAガイドラインによるprobable ADの診断）を満たしているか。
                3.  アルツハイマー病の病歴が、除外基準EXCL12（重篤な神経学的状態の診断）に該当するか否かについての医師の判断。重篤と判断された場合、その理由。
        *   判断理由: アルツハイマー病の病歴が選択基準を満たす一方で、除外基準にも抵触する可能性があるため、治験の適格性を確認する必要がある。


# 01-703-1299
## Task1: Clinical Review Results
```markdown
患者ID: 01-703-1299

*   2012年09月07日 (Day -5): Medical Historyとしてアルツハイマー病、緑内障、聴力低下、関節炎、乳がん、乳房切除術、腸閉塞が報告された。
*   2012年09月27日 (Day 16): 有害事象として上気道感染症が発症。
*   2012年09月28日 (Day 17): 血清アルブミン値が基準範囲を下回る3.4 g/dL (基準範囲: 3.5-4.6 g/dL) を記録。
*   2012年09月28日 (Day 17): 上気道感染症による発熱のため緊急受診。
*   2012年12月05日 (Day 85): 血清ナトリウム値が基準範囲を下回る134 mEq/L (基準範囲: 135-145 mEq/L) を記録。
*   2013年03月01日 (Day 171): 有害事象として低血圧、頻脈が発症。
*   2013年03月13日 (Day 183): 有害事象として心筋梗塞が発症。

```

---

患者ID: 01-703-1299

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AESTDTC: 1992
    *   **医療機関への問い合わせ文面:**
        *   有害事象「緑内障」の開始日が1992年となっていますが、これは医学的既往歴として登録されるべきではないでしょうか？有害事象と判断された理由についてご教示ください。
        *   また、医学的既往歴と有害事象の関連について、治験依頼者として見解をご教示ください。
    *   **判断理由:**
        *   Define.xmlにAESTDTCは「Start Date/Time of Adverse Event」と定義されている。
        *   DM.RFSTDTC（治験開始日）は2012-09-12であり、AESTDTCが1992年であることは、有害事象の定義と矛盾する可能性がある。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AESTDTC: 2013-03-01
        *   AE.AEENDTC: "" (NULL)
        *   AE.AEOUT: "NOT RECOVERED/NOT RESOLVED"
    *   **医療機関への問い合わせ文面:**
        *   有害事象「低血圧」について、AESTDTCは2013-03-01ですが、AEENDTCが空欄であり、AEOUTが「NOT RECOVERED/NOT RESOLVED」となっています。これは、有害事象が未だ継続中であることを意味しますが、最終観察日である2013-03-13との整合性について確認させてください。
    *   **判断理由:**
        *   Define.xmlにAEENDTCは「End Date/Time of Adverse Event」と定義されている。
        *   試験終了時に未回復の有害事象は、その後の転帰を評価する必要がある。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AESTDTC: 2013-03-01
        *   AE.AEENDTC: "" (NULL)
        *   AE.AEOUT: "NOT RECOVERED/NOT RESOLVED"
    *   **医療機関への問い合わせ文面:**
        *   有害事象「頻脈」について、AESTDTCは2013-03-01ですが、AEENDTCが空欄であり、AEOUTが「NOT RECOVERED/NOT RESOLVED」となっています。これは、有害事象が未だ継続中であることを意味しますが、最終観察日である2013-03-13との整合性について確認させてください。
    *   **判断理由:**
        *   Define.xmlにAEENDTCは「End Date/Time of Adverse Event」と定義されている。
        *   試験終了時に未回復の有害事象は、その後の転帰を評価する必要がある。

*   **クエリNo.:** 4
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        * AE.AESTDTC: 2013-03-01
        * AE.AEENDTC: "" (NULL)
        * AE.AEOUT: "NOT RECOVERED/NOT RESOLVED"
        * AE.AESEQ: 4,6,5,7,8
    *   **医療機関への問い合わせ文面:**
        *   複数の有害事象について，転帰がNOT RECOVERED/NOT RESOLVEDとなっています．治験薬投与終了後も継続している有害事象について，治験担当医師の見解を伺います．
    *   **判断理由:**
        *   治験薬投与終了後も改善が見られない有害事象は，治験薬との因果関係，および，被験者の安全性に影響を及ぼす可能性があるため．

*   **クエリNo.:** 5
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   VS.VSTPT: "AFTER STANDING FOR 1 MINUTE"
        *   VS.VSTPT: "AFTER STANDING FOR 3 MINUTES"
    *   **医療機関への問い合わせ文面:**
        *   バイタルサイン測定において、立位での血圧および脈拍測定時に、1分後と3分後の2回の測定がありますが、これはプロトコルで定められた手順に沿ったものでしょうか？測定方法について、プロトコルからの逸脱がないか確認させてください。
    *   **判断理由:**
        *   プロトコルに詳細な手順が記載されている場合、手順からの逸脱はデータの解釈に影響を与える可能性があるため。
```
## Task2: DM Review Results
```markdown
### 全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: 
  * CM.CMTRT, AE.AETERM, MH.MHTERMにおけるUncoded用語の使用
  * AE.AESTDTC, AE.AEENDTC
  * LB.LBDTC, LB.LBDY
  * VS.VSTPTNUM, VS.VSTPTREF, VS.VSELTM

### 問題点:

* **問題No.1:**
    * **変数名と値:** CM.CMTRT = "UNCODED" (複数レコード)
    * **矛盾の内容:** CM.CMTRT (Reported Name of Drug, Med, or Therapy) に "UNCODED" が使用されている。Define.xmlには、CMTRTはControlled Termで定義されていない。しかし、CMDECODにStandardized Medication Nameが期待されているにもかかわらず、CMTRTがUNCODEDであることは、データの標準化という観点から問題がある。
    * **問題点の原因（推測）:** MedDRAなどの標準的な辞書に該当する用語がない場合に、データマネジメント担当者が便宜的に入力した可能性がある。
    * **対応策（提案）:**
        1.  医療機関にCMTRTの具体的な薬剤名を確認する。
        2.  確認した薬剤名でCMDECODを更新する。必要であれば、MedDRA等の標準辞書を用いてコード化する。

* **問題No.2:**
    * **変数名と値:** AE.AETERM = "GLAUCOMA" (AESEQ=3), MH.MHTERM = "GLAUCOMA" (MHSEQ=1)
    * **矛盾の内容:** USUBJIDが同一人物で、AE.AETERMとMH.MHTERMに同じGLAUCOMAが記録されている。しかし、AE.AESTDTCに日付(1992)が設定されているにもかかわらず、AETRTEM (TREATMENT EMERGENT FLAG) が "N" となっている。
    * **問題点の原因（推測）:** GlaucomaはMedical Historyに記載されている既往歴であるため、治験中に発症したものではないと考えられる。
    * **対応策（提案）:**
        1.  AE.AETERMに登録されているGLAUCOMAが、新規に発症したものなのか、既存の症状なのかを医療機関に確認する。
        2.  もし既存の症状であれば、AE.AETERMへの記録は誤りであるため削除する。

*   **問題No.3:**

    *   **変数名と値:** AE.AESTDTC = "1992" (AESEQ=3), AE.AEENDTC = "" (AESEQ=3)
    *   **矛盾の内容:**
        *   AE.AESTDTCに1992年という年のみが記録されており、日付の形式として不完全。
        *   AE.AEENDTCが空欄。
    *   **問題点の原因（推測）:**
        *   データ入力時に詳細な日付が不明であったか、誤って年のみが入力された可能性がある。
        *   有害事象が現在も継続中である可能性がある。
    *   **対応策（提案）:**
        1.  医療機関に正確な開始日を確認する。
        2.  ADAMデータセットにおけるAENDTCの取り扱いについて、統計担当者と協議する。

*   **問題No.4:**
    *   **変数名と値:** AE.AETERM = "HYPOTENSION" (AESEQ=4), AE.AESTDTC = "2013-03-01", EX.EXSTDTC = "2012-09-12"
    *   **矛盾の内容:**
        *   DM.RFXSTDTC (Date/Time of First Study Treatment) が2012-09-12であるのに対し、有害事象HYPOTENSIONの発現日 (AE.AESTDTC) が2013-03-01となっており、治験薬投与開始後に発生した有害事象である。SUPPAE.QVALにAETRTEM = "Y"が設定されているため、TREATMENT EMERGENT FLAGがTrueであることを示している。しかし、AEREL (Causality) が "REMOTE" となっており、治験薬との因果関係が低いと判断されている。
        *  MHにHypertensionの記載がない。
        *  VSの血圧値を確認したが、高血圧の疑われるデータは確認できなかった。
    *   **問題点の原因（推測）:**
        *   併用薬の影響、または別の原因による低血圧の可能性がある。
    *   **対応策（提案）:**
        1.  AETERMに登録されているHYPOTENSIONが、新規に発症したものなのか、既存の症状なのかを医療機関に確認する。
        2.  MHにHypertensionの記載がない理由を医療機関に確認する。
        3.  VSドメインに、低血圧に関連するデータがないか確認する。必要であれば、VSドメインに不足しているデータがないか、医療機関に確認する。
        4.  治験薬との因果関係（AEREL）の判断理由を、治験担当医師に確認する。

*   **問題No.5:**
    *   **変数名と値:** AE.AETERM = "TACHYCARDIA" (AESEQ=6,7), AE.AESTDTC = "2013-03-01", EX.EXSTDTC = "2012-09-12"
    *   **矛盾の内容:**
        *   AE.AESTDTCが2013-03-01となっており、治験薬投与開始後に発生した有害事象である。SUPPAE.QVALにAETRTEM = "Y"が設定されているため、TREATMENT EMERGENT FLAGがTrueであることを示している。しかし、AEREL (Causality) が "REMOTE" となっており、治験薬との因果関係が低いと判断されている。
        * VSのPULSEを確認すると、WEEK26のSUPINEで104、立位で108, 100 beats/MINと高い値が確認できる。他のVisitでは100を超えるデータは確認できなかった。
    *   **問題点の原因（推測）:**
        *   治験薬の影響、または別の原因による頻脈の可能性がある。
    *   **対応策（提案）:**
        1.  AETERMに登録されているTACHYCARDIAが、新規に発症したものなのか、既存の症状なのかを医療機関に確認する。
        2.  VSドメインに、頻脈に関連するデータがないか確認する。特に、2013-03-01以降のデータに異常がないか確認する。
        3.  治験薬との因果関係（AEREL）の判断理由を、治験担当医師に確認する。

*   **問題No.6:**
    *   **変数名と値:** AE.AETERM = "MYOCARDIAL INFARCTION" (AESEQ=8), AE.AESTDTC = "2013-03-13", EX.EXSTDTC = "2012-09-12"
    *   **矛盾の内容:**
        *   AE.AESTDTCが2013-03-13となっており、治験薬投与開始後に発生した有害事象である。SUPPAE.QVALにAETRTEM = "Y"が設定されている。しかし、AEREL (Causality) が "REMOTE" となっており、治験薬との因果関係が低いと判断されている。
        * DM, MHに心筋梗塞の既往歴がない。
    *   **問題点の原因（推測）:**
        *   被験者の状態、併用薬、または別の要因が原因で心筋梗塞が発生した可能性がある。
    *   **対応策（提案）:**
        1.  AETERMに登録されているMYOCARDIAL INFARCTIONが、新規に発症したものなのか、既存の症状なのかを医療機関に確認する。
        2.  MHに心筋梗塞の既往歴がない理由を医療機関に確認する。
        3.  治験薬との因果関係（AEREL）の判断理由を、治験担当医師に確認する。
        4.  心筋梗塞発生時の詳細な状況（時間、症状、処置など）を医療機関から入手し、治験薬との関連性を検討する。
        5.  必要に応じて、治験安全性委員会（DSMB）に報告する。

*   **問題No.7:**
    *   **変数名と値:** LB.LBDTCとLB.LBDYの矛盾
    *   **矛盾の内容:** LB.LBDTC (Date/Time of Specimen Collection) と LB.LBDY (Study Day of Specimen Collection) の日付にずれがある。例えば、1行目の場合、LBDTCは"2012-09-04T13:30"だが、LBDYは"-8"となっている。しかし、DM.RFSTDTCが"2012-09-12"なので、LBDTCが"2012-09-04"の場合、LBDYは-8となるのが正しい。
    *   **問題点の原因（推測）:** LB.LBDYの計算ロジックに誤りがあるか、DM.RFSTDTCが正しくない可能性がある。
    *   **対応策（提案）:**
        1.  DM.RFSTDTCが正しいことを確認する。
        2.  LB.LBDYの計算ロジックを確認する。
        3.  LB.LBDTCとLB.LBDYの整合性が取れるように修正する。

*   **問題No.8:**
    *   **変数名と値:** AE.AETERM = "UPPER RESPIRATORY TRACT INFECTION" (AESEQ=1,2), AE.AESTDTC = "2012-09-27", AE.AEENDTC = "2012-10-06", EX.EXSTDTC = "2012-09-12"
    *   **矛盾の内容:** AE(AESEQ=1,2).AESTDYが16となっているが、EX.EXSTDTC = "2012-09-12"からAESTDTC = "2012-09-27"までの日数は15日であり、計算が合わない。
    *   **問題点の原因（推測）:** AESTDYの計算ロジックに誤りがあるか、EXSTDTCが正しくない可能性がある。
    *   **対応策（提案）:**
        1.  EX.EXSTDTCが正しいことを確認する。
        2.  AE.AESTDYの計算ロジックを確認する。
        3.  AE.AESTDTCとAE.AESTDYの整合性が取れるように修正する。

*   **問題No.9:**

    *   **変数名と値:** VS.VSTPTNUM, VS.VSTPTREF, VS.VSELTMがNULLになっているレコードが存在する。
    *   **矛盾の内容:** 
    VSドメインでは、血圧や脈拍などのバイタルサインを、被験者の状態（立位、仰臥位）ごとに、測定タイミングをずらして複数回測定している。測定タイミングはVSTPT, VSTPTNUM, VSELTM, VSTPTREFで定義されている。これらの変数がNULLの場合、いつ測定されたデータなのか判断することができない。
    *   **問題点の原因（推測）:** 必須のデータ収集項目であるにもかかわらず、データが欠損している。
    *   **対応策（提案）:**
        1.  VS.VSTPTNUM, VS.VSTPTREF, VS.VSELTMがNULLになっているレコードについて、データが欠損している理由を確認する。
        2.  データが欠損している場合、医療機関に問い合わせて、不足しているデータを収集する。
        3.  Define.xmlにVSTPTNUMが必須項目として定義されているにも関わらず、JSONデータにNULLが含まれている。Define.xmlの記述が正しいか確認する。

### クエリの作成 (必要な場合のみ):

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "UNCODED" (複数レコード)
        *   **医療機関への問い合わせ文面:**
            *   CM.CMTRTに「UNCODED」と記録されている併用薬について、具体的な薬剤名を教えてください。
            *   薬剤名が判明した場合、その薬剤のMedDRAコード（CMDECOD）も教えてください。
        *   **判断理由:** 併用薬は、有害事象の評価や薬物相互作用の評価に影響を与える重要な情報であるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "GLAUCOMA" (AESEQ=3), MH.MHTERM = "GLAUCOMA" (MHSEQ=1)
        *   **医療機関への問い合わせ文面:**
            *   AE.AETERMに登録されているGlaucomaは、新規に発症したものですか、それとも既存の症状ですか？
            * 新規に発症したものではない場合、AEへの登録は誤りと考えられます。
            * MHにGlaucomaの記載がありますが、AEにもGlaucomaが記録されている理由を教えてください。
        *   **判断理由:** 有害事象の正確な評価のため、GlaucomaがMedical Historyに記載されている既往歴なのか、Adverse Eventとして新たに発生したものなのかを確認する必要があるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = "1992" (AESEQ=3), AE.AEENDTC = "" (AESEQ=3)
        *   **医療機関への問い合わせ文面:**
            *   Glaucoma (AE.AESEQ=3) のAESTDTC (有害事象の開始日) の正確な日付を教えてください。
            *   AEENDTC (有害事象の終了日) が空欄になっていますが、Glaucomaは現在も継続中ですか？
        *   **判断理由:**
            *   AESTDTCが正確でない場合、有害事象の評価期間に影響を与える可能性があるため。
            *   AEENDTCが不明な場合、有害事象の継続期間や転帰の評価に影響を与える可能性があるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 4**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "HYPOTENSION" (AESEQ=4), AE.AESTDTC = "2013-03-01", EX.EXSTDTC = "2012-09-12"
        *   **医療機関への問い合わせ文面:**
            *   AE.AETERMに登録されているHYPOTENSIONは、新規に発症したものですか、それとも既存の症状ですか？
            *   MHにHypertensionの記載がない理由を教えてください。
            *   VSドメインに、低血圧に関連するデータがないか確認してください。特に、2013-03-01以降のデータに異常がないか確認してください。
            *   治験薬との因果関係（AEREL）をREMOTEと判断した理由を教えてください。
        *   **判断理由:** 安全性評価に重要な情報であり、治験薬との関連を正しく判断する必要があるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 5**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "TACHYCARDIA" (AESEQ=6,7), AE.AESTDTC = "2013-03-01", EX.EXSTDTC = "2012-09-12"
        *   **医療機関への問い合わせ文面:**
            *   AE.AETERMに登録されているTACHYCARDIAは、新規に発症したものですか、それとも既存の症状ですか？
            *   VSドメインに、頻脈に関連するデータがないか確認してください。特に、2013-03-01以降のデータに異常がないか確認してください。
            *   治験薬との因果関係（AEREL）をREMOTEと判断した理由を教えてください。
        *   **判断理由:** 安全性評価に重要な情報であり、治験薬との関連を正しく判断する必要があるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 6**
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** AE.AETERM = "MYOCARDIAL INFARCTION" (AESEQ=8), AE.AESTDTC = "2013-03-13", EX.EXSTDTC = "2012-09-12"
        *   **医療機関への問い合わせ文面:**
            *   AE.AETERMに登録されているMYOCARDIAL INFARCTIONは、新規に発症したものですか、それとも既存の症状ですか？
            *   MHに心筋梗塞の既往歴がない理由を教えてください。
            *   治験薬との因果関係（AEREL）をREMOTEと判断した理由を教えてください。
            *   心筋梗塞発生時の詳細な状況（時間、症状、処置など）を教えてください。
        *   **判断理由:** 重大な有害事象であり、患者の安全性に直接関わるため。治験薬との関連を正しく判断し、適切な対応を取る必要があるため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 7**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBDTCとLB.LBDYの不整合 (複数レコード)
        *   **医療機関への問い合わせ文面:**
            *  LB.LBDTCとLB.LBDYにずれがあることを確認しました。検体採取日と検査日の情報に誤りがないか確認してください。
        *   **判断理由:** データの一貫性を保つため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 8**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM = "UPPER RESPIRATORY TRACT INFECTION" (AESEQ=1,2), AE.AESTDTC = "2012-09-27", AE.AEENDTC = "2012-10-06", EX.EXSTDTC = "2012-09-12"
        *   **医療機関への問い合わせ文面:**
             *   AEのUPPER RESPIRATORY TRACT INFECTIONのAESTDYが16となっていますが、EX.EXSTDTCとAESTDTCの日付から計算すると15日になるはずです。AESTDYの日付に誤りがないか確認してください。
        *   **判断理由:** データの一貫性を保つため。

*   **患者ID:** 01-703-1299
    *   **クエリNo.: 9**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** VS.VSTPTNUM, VS.VSTPTREF, VS.VSELTMがNULLになっているレコード (複数レコード)
        *   **医療機関への問い合わせ文面:**
            *    VS.VSTPTNUM, VS.VSTPTREF, VS.VSELTMがNULLになっているバイタルサインデータについて、測定タイミングに関する情報をご提供ください。
        *   **判断理由:** バイタルサインの測定タイミングは、データの解釈や評価に不可欠な情報であるため。

### Define.xmlの修正候補

とくになし
```
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1299
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMTRT = TIMOPTIC, DM.AGE = 81
    *   逸脱内容: 被験者01-703-1299はTIMOPTICを併用していますが、プロトコルで併用禁止薬に指定されている可能性があります。プロトコルの併用禁止薬リストを確認する必要があります。
    *   プロトコル該当箇所: プロトコル3.8 Concomitant Therapy、3.4.2.2 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list).
    *   判断理由: CMドメインにTIMOPTICの記録があり、これがプロトコルで指定された併用禁止薬に該当するかどうか不明なため。
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMTRT = TIMOPTIC, CM.CMSTDTC = 1992
    *   医療機関への問い合わせ文面: 被験者01-703-1299が併用しているTIMOPTICは、プロトコルの併用禁止薬リストに該当するか確認してください。また、TIMOPTICの使用開始時期(CMSTDTC)が1992年となっていますが、治験参加前30日以内の使用状況について確認してください。
    *   判断理由: 併用薬がプロトコルに抵触するかどうかと、治験薬投与開始前の使用期間を確認する必要があるため。

患者ID: 01-703-1299
*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: AE.AETERM = GLAUCOMA, MH.MHTERM = GLAUCOMA
    *   逸脱内容: 有害事象として報告されたGLAUCOMAが、Medical HistoryにもGLAUCOMAとして記録されています。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria
    *   判断理由: 選択基準に影響を与える可能性があるため、GLAUCOMAの重症度と発症時期について確認が必要です。
*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = GLAUCOMA, AE.AETERM = GLAUCOMA,MH.MHSEV = MILD
    *   医療機関への問い合わせ文面: 被験者01-703-1299の緑内障（GLAUCOMA）の診断時期、種類、重症度について確認してください。特に、(1)本治験への参加に影響を与える可能性のある除外基準に該当するかどうか、(2) Medical HistoryとAdverse EventにGlaucomaと記載されているが、それぞれの詳細について確認してください。
    *   判断理由: 選択基準に影響を与える可能性があるため、詳細な情報を収集する必要があるため。

クエリなし

# 01-703-1086
## Task1: Clinical Review Results
患者ID: 01-703-1086

*   2012年08月22日 (Day -11): スクリーニング検査で、医学的既往歴としてアルツハイマー病の診断が確認されました。
*   2012年08月31日 (Day -2): 白血球数が低い (1 THOU/uL, 基準値: 3.8 - 10.7 THOU/uL) ことが確認されました。
*   2012年09月13日 (Day 12): 貼付部位に軽度から重度の刺激感が発生しました。
*   2012年09月16日 (Day 15): AST (アスパラギン酸アミノトランスフェラーゼ) が基準値上限を超えました (40 U/L, 基準値: 11 - 36 U/L)。
*   2012年10月02日 (Day 31): 好酸球数が基準値上限を超えました (0.60 THOU/uL, 基準値: 0 - 0.57 THOU/uL)。
*   2012年10月09日 (Day 38): 悪寒が出現しました。
*   2012年10月13日 (Day 42): 好酸球数がさらに増加しました (1.11 THOU/uL, 基準値: 0 - 0.57 THOU/uL)。
*   2012年10月27日 (Day 56): 好酸球数は減少しましたが、依然として基準値上限を超えています (0.69 THOU/uL, 基準値: 0 - 0.57 THOU/uL)。
*   2012年12月24日 (Day 114): 好酸球数は基準値内に戻りました (0.11 THOU/uL, 基準値: 0 - 0.57 THOU/uL)。
*   2013年01月02日 (Day 123): 貼付部位の刺激感はまだ解消されていません。
*   2013年03月26日 (Day 206): 貼付部位の刺激感がようやく解消しました。

---

患者ID: 01-703-1086

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" (AESEQ=1,2,3)
        *   AE.AEOUT = "RECOVERED/RESOLVED" (AESEQ=6)
    *   **医療機関への問い合わせ文面:** 
    AE (貼付部位刺激) の転帰について確認します。AESEQ=1,2,3 では転帰が "NOT RECOVERED/NOT RESOLVED" となっていますが、AESEQ=6 では "RECOVERED/RESOLVED" となっています。これは矛盾している可能性があります。貼付部位刺激の正確な転帰について教えてください。
    *   **判断理由:** 
    有害事象の転帰は、安全性評価において重要な要素です。データに矛盾がある場合、正確な評価ができません。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   LB.WBC = 1 THOU/uL (LBDY=-2)
        *   LB.WBC = 1.2 THOU/uL (LBDY=15)
        *   LB.WBC = 1.1 THOU/uL (LBDY=31)
        *   LB.WBC = 1 THOU/uL (LBDY=42)
        *   LB.WBC = 1.3 THOU/uL (LBDY=56)
        *   LB.WBC = 0.9 THOU/uL (LBDY=87)
        *   LB.WBC = 0.8 THOU/uL (LBDY=114)
    *   **医療機関への問い合わせ文面:** 
    LB (臨床検査) における白血球数減少について確認します。WBC が一貫して基準値範囲を下回っています。臨床的な意義や、他に原因となる事象がないか確認してください。
    *   **判断理由:** 
    WBC 減少は、安全性評価において重要な要素です。
## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMDTC, DS.DSDTC, LB.LBDY, LB.LBDTC, AE.AESTDTC

問題点:

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC (2012-09-30), CM.CMDTC (2012-09-30)
    *   **矛盾の内容:** USUBJIDが"01-703-1086"のCMドメインにおいて、CMSTDTCとCMDTCが同じ日付で記録されているが、複数のCMTRTレコードにおいて、CMSTDTCがCMDTCより前の日付（例えば、CMSTDTCが2012-09-15でCMDTCが2012-09-16）になっている矛盾がある。
    *   **問題点の原因（推測）:** データ入力エラー、日付記録の誤り。
    *   **対応策（提案）:** 
        *   CMSTDTCとCMDTCの日付の記録方法について、データ入力手順書を確認し、CMDTCにCMSTDTCより前の日付が記録されることがないように、データ入力担当者へ再教育を行う。
        *   症例記録を照合し、CMSTDTCとCMDTCの正しい日付を特定し、必要に応じて修正する。

*   **問題No.2:**
    *   **変数名と値:** DS.DSDTC (2012-12-24), DSSTDTC (2012-12-24)
    *   **矛盾の内容:** USUBJIDが"01-703-1086"のDSドメインにおいて、ADVERSE EVENTと記載されているレコードのDSDTCとDSSTDTCが同じ日付で記録されているが、DSDTCはタイムスタンプ（時間情報を含む）であるのに対し、DSSTDTCは日付のみである。FINAL LAB VISITのレコードでは、DSDTCには時間情報が含まれている。
    *   **問題点の原因（推測）:** データ入力時の不整合、またはデータ変換時の問題。
    *   **対応策（提案）:**
        *   DSDTCの時間情報の記録方法について、データ入力手順書を確認し、必要に応じて修正する。
        *   時間情報が必要な場合は、DSSTDTCにも時間情報を記録するか、DSDTCのみを使用するように変更する。
        *   Define.xmlのDSDTCの説明を修正し、時間情報を含むことを明記する。

*   **問題No.3:**
    *   **変数名と値:** LB.LBDTC (2012-08-19T14:50), LB.LBDY (-14)
    *   **矛盾の内容:** USUBJIDが"01-703-1086"のLBドメインにおいて、LBDTCが2012-08-19T14:50であるのに対し、LBDYが-14となっている。DMドメインのDMDTC（2012-08-22）を基準日とすると、つじつまが合わない。
    *   **問題点の原因（推測）:** LBDYの計算に使用された基準日がDM.DMDTCと異なる、またはデータ入力エラー。
    *   **対応策（提案）:**
        *   LBDYの計算に使用した基準日を確認し、DM.DMDTCとの整合性を確認する。
        *   必要に応じてLBDYの値を修正する。

*   **問題No.4:**
    *   **変数名と値:** AE.AESTDTC (2012-09-13), AEENDTC (2013-01-02)
    *   **矛盾の内容:** USUBJIDが"01-703-1086"のAEドメインにおいて、全てのAETERMがAPPLICATION SITE IRRITATIONであるレコードのAESTDTCが2012-09-13で共通しているが、AESTDTCが同じ日付で、AESEQが異なる複数のレコードが存在する。治験薬の投与開始日（DM.RFSTDTC）は2012-09-02である。
    *   **問題点の原因（推測）:** 複数の有害事象が同時に発生したか、データ入力時の誤り。
    *   **対応策（提案）:**
        *   症例記録を照合し、AESTDTCとAESEQが正しい組み合わせになっているか確認する。
        *   APPLICATION SITE IRRITATIONが実際に複数回発生しているのであれば問題ないが、記録が誤っている場合は修正する。

*   **問題No.5:**
    *   **変数名と値:** DM.DMDTC (2012-08-22), DM.DMDY (-11)
    *   **矛盾の内容:** USUBJIDが"01-703-1086"のDMドメインにおいて、DMDTCが2012-08-22であるのに対し、DMDYが-11となっている。DMドメインにはRFSTDTC (2012-09-02)が記録されているが、仮にこれを基準日とした場合でも、つじつまが合わない。
    *   **問題点の原因（推測）:** DMDYの計算に使用された基準日がRFSTDTCと異なる、またはデータ入力エラー。
    *   **対応策（提案）:**
        *   DMDYの計算に使用した基準日を確認し、RFSTDTCとの整合性を確認する。
        *   必要に応じてDMDYの値を修正する。
        *   Define.xmlのDMDYの計算方法にRFSTDTCを使用することを明記する。

クエリの作成：

*   **患者ID:** 01-703-1086
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC, CM.CMDTC
        *   **医療機関への問い合わせ文面:** 患者ID 01-703-1086 において、併用薬CALAMINEおよびCORTISONEのCMSTDTC（薬剤投与開始日）とCMDTC（データ収集日）に矛盾が見られます。記録に誤りがないかご確認ください。
        *   **判断理由:** CMSTDTCは併用薬の使用期間を特定するために重要であり、データの正確性は臨床試験の結果に影響を与える可能性があります。

*   **患者ID:** 01-703-1086
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBDY, DM.DMDTC
        *   **医療機関への問い合わせ文面:** 患者ID 01-703-1086 において、検査値データセット(LB)の検査実施日(LBDY)と、人口統計データセット(DM)のデータ収集日(DMDTC)との関係が不明確です。検査実施日(LB.LBDTC)を基に、LBDYを再計算し、DM.DMDTCとの整合性を確認してください。
        *   **判断理由:** LBDYが正しく計算されていない場合、検査値の評価に影響を及ぼし、臨床試験の結果に影響を与える可能性があります。

*   **患者ID:** 01-703-1086
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AESTDTC
        *   **医療機関への問い合わせ文面:** 患者ID 01-703-1086 において、有害事象（APPLICATION SITE IRRITATION）の発現日が全て2012-09-13となっています。AESTDTCは有害事象の開始日を記録する項目ですが、複数の事象が全て同じ日に発生したという記録で問題ないでしょうか。
        *   **判断理由:** 併用薬が複数回投与されている可能性を考慮し、データ収集の正確性を確認する必要があるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-703-1086
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MHSTDTC = 2011-04-27, DM.RFSTDTC = 2012-09-02
    *   逸脱内容: 被験者のAlzheimer's Diseaseの診断日が、Reference Start Date/Time（RFSTDTC）より前である。DM.RFSTDTCは通常、最初の治験薬投与日を示すため、MHSTDTCがこれより前であることは医学的既往歴として矛盾はない。しかし、本試験のプロトコルでは、exclusion criteriaに神経疾患の診断があるため、Alzheimer's Diseaseの診断がDM.RFSTDTCより前に確定している場合、選択基準に抵触する可能性がある。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [12] Diagnosis of serious neurological conditions.
    *   判断理由: MHSTDTCがDM.RFSTDTCより前であること自体は必ずしも逸脱ではないが、選択基準との関連で確認が必要。

*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MHSTDTC = 2011-04-27, DM.RFSTDTC = 2012-09-02
    *   医療機関への問い合わせ文面:
        被験者01-703-1086のAlzheimer's Diseaseの診断日（2011-04-27）は、治験薬投与開始日（2012-09-02）より前ですが、神経学的状態に関する選択基準（3.4.2.2 Exclusion Criteria [12] Diagnosis of serious neurological conditions.）を満たしているか確認してください。Alzheimer's Diseaseの診断は、選択基準に影響を与える可能性があります。
    *   判断理由: プロトコル遵守状況を確認するために、医療機関への問い合わせが必要であるため。


# 01-701-1363
## Task1: Clinical Review Results
## 症例サマリー

**患者ID:** 01-701-1363

*   2013年05月20日 (Day -10): スクリーニング検査で、既往歴としてアルツハイマー病、不整脈、関節炎、貧血、頭痛、意識消失、湿疹、聴力低下、便秘、消化不良、股関節痛、立ちくらみ、背中の上部の痛み、肩の痛み、近視が報告された。教育年数は13年。Albumin 4.1 g/dL, Alkaline Phosphatase 43 U/L, Alanine Aminotransferase 9 U/L, Aspartate Aminotransferase 20 U/L, Basophils 0.02 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 16 mg/dL, Calcium 9.5 mg/dL, Cholesterol 211 mg/dL, Creatine Kinase 84 U/L, Chloride 107 mEq/L, Color N, Creatinine 1.2 mg/dL, Eosinophils 0.02 THOU/uL, Gamma Glutamyl Transferase 8 U/L, Glucose 88 mg/dL, Hematocrit 37.0 %, Hemoglobin 11.5 g/dL, Potassium 4.1 mEq/L, Ketones 0, Lymphocytes 1.44 THOU/uL, Ery. Mean Corpuscular Hemoglobin 27 pg, Ery. Mean Corpuscular HGB Concentration 31 g/dL, Ery. Mean Corpuscular Volume 86 fL, Monocytes 0.26 THOU/uL, Sodium 140 mEq/L, pH 5.0, Phosphate 4.1 mg/dL, Platelet 255 THOU/uL, Protein 7.4 g/dL, Erythrocytes 4.30 MILL/uL, Specific Gravity 1.025, Thyrotropin 1.36 uIU/mL, Urate 4.9 mg/dL, Urobilinogen 0, Vitamin B12 713 pg/mL, Leukocytes 4.99 THOU/uL.ASA 650mg, MAALOX 3 tsp, アルツハイマー病治療薬、うつ病治療薬、睡眠薬、抗ヒスタミン薬、筋肉弛緩薬、モノアミン酸化酵素阻害薬、副交感神経遮断薬、MULTIVITAMIN 1 TABLETを服用。
*   2013年05月30日 (Day 1): Placebo投与開始。ADAS-COG(11)サブスコアは15、Dementia (DAD)の日常生活動作は自立している。
*   2013年06月15日 (Day 17): 悪心発症(軽度)。
*   2013年07月16日 (Day 48): 適用部位掻痒感の発症(軽度)。
*   2013年10月13日 (Day 137): 背部痛の発症(軽度)。HYDROCORTISONE 1 VIAL, ICY HOT 1 VIAL, MOTRIN 400mgを服用開始
*   2013年10月15日 (Day 139): 背部痛が回復。
*  2013年11月27日 (Day 182): 試験完了。

---

## クエリ

*   **患者ID:** 01-701-1363
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AESTDTC = "1986" (HEADACHE), AE.AEENDTC = "" (HEADACHE)
        *   **医療機関への問い合わせ文面:** 頭痛のAESTDTCとAEENDTCが1986と空欄になっていますが、正しく記録されているか確認してください。
        *   **判断理由:** AESTDTCとAEENDTCは日付を示す変数であり、1986という値や空欄は不適切である可能性があります。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.DAITM21 = 'NA', QS.DAITM22 = 'NA' (WEEK 8), QS.DAITM21 = 'N', QS.DAITM22 = 'NA' (WEEK 16), QS.DAITM21 = 'N', QS.DAITM22 = 'N' (WEEK 24)
        *   **医療機関への問い合わせ文面:** 
            *   DADの質問項目「DAITM21:電話をかけようとするか」と「DAITM22:電話番号を探して正しくダイヤルできるか」について、WEEK 8とWEEK 16で「NA（該当しない）」、WEEK 24で「N（いいえ）」と回答されています。「該当しない」から「いいえ」に変化した理由、または評価方法に一貫性がない理由について説明をお願いします。
        *   **判断理由:** 
            *   DADは日常生活における機能障害を評価するものであり、患者の状態変化を正確に捉える必要があります。評価方法が一貫していない場合、DADの結果に影響を及ぼす可能性があります。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** HGB = 10.8 g/dL (WEEK 6), HGB = 10.3 g/dL (WEEK 12), HGB = 10.9 g/dL (WEEK 24)
        *   **医療機関への問い合わせ文面:** 
            *  ヘモグロビン値が正常範囲下限を下回っています。貧血の原因について評価されていますか？
        *   **判断理由:** 
            * ヘモグロビン値の低下は貧血を示唆し、患者の健康状態に影響を与える可能性があります。


## Task2: DM Review Results
```markdown
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目:
    * AE.AESTDTC, AE.AEENDTC
    * DM.DMDYと各ドメインの**DY変数
    * CM.CMTRTとMH.MHTERM, AE.AETERMとの整合性
    * LB.LBORRESの値

問題点:
* **問題No.1:**
    * **変数名と値:** AE.AESTDTC="1986", AE.AEENDTC=NULL (AE Record 2,4), AE.AESTDTC="2013-10-13", AE.AEENDTC="2013-10-15"(AE Record 5), AE.AESTDTC="2013-10-13", AE.AEENDTC="2013-10-15"(AE Record 6)
    * **矛盾の内容:** AE.AESTDTC（有害事象開始日）が、DM.RFSTDTC（治験薬初回投与日）より前の日付（1986年）になっている。DM.RFSTDTC="2013-05-30"であるため、有害事象が治験薬投与前に発生していることになり、矛盾が発生する。 AE Record 5,6では、AESTDTCとAEENDTCが同じ日付だが、AE Record 2,4では、AEENDTCがNULLとなっている。
    * **問題点の原因（推測）:**
        * データ入力時の誤り
        * システムエラー
        * 治験実施計画書からの逸脱
    * **対応策（提案）:**
        * AE.AESTDTC、AE.AEENDTCについて、原資料を確認し、正しい日付に修正する。
        * 必要に応じて、データ入力手順またはシステムに改善を加える。

* **問題No.2:**
    * **変数名と値:** DM.DMDY=-10, LB.LBDY=-10, CM.VISITDY=-7, MH.MHDY=-10, VS.VSDY=-10, QS.QSDY=1
    * **矛盾の内容:** DM.RFSTDTC（治験薬初回投与日）と各ドメインのDY変数との関係に矛盾が発生している可能性がある。DM.RFSTDTC="2013-05-30"に対して、DM.DMDY=-10, LB.LBDY=-10, CM.VISITDY=-7, MH.MHDY=-10, VS.VSDY=-10, QS.QSDY=1となっており、整合性が取れているか確認が必要である。
    * **問題点の原因（推測）:**
        * 日付計算の誤り
        * データ入力時の誤り
    * **対応策（提案）:**
        * DM.RFSTDTCと各ドメインのDY変数の計算ロジックを確認する。
        * 必要に応じて、原資料を確認し、正しい日付に修正する。

* **問題No.3:**
    * **変数名と値:** CM.CMTRT="ASA" (複数のレコード), MH.MHTERM="ALZHEIMER'S DISEASE"
    * **矛盾の内容:** USUBJID="01-701-1363"の被験者は、CMにASA（アセチルサリチル酸）を服用しているが、MHにALZHEIMER'S DISEASE（アルツハイマー病）の既往歴がある。ASAは、一般的にアルツハイマー病の治療薬ではないため、CM.CMINDC（Indication）が欠損していることも含めて、矛盾がないか確認が必要である。
    * **問題点の原因（推測）:**
        * 併用薬の記録が不完全である。
        * データ入力時の誤り
    * **対応策（提案）:**
        * CM.CMINDCを正しく記録する。
        * MHとCMの記録に矛盾がないか、原資料を再確認する。
        * 必要に応じて、ASA服用の理由を医療機関に問い合わせる。

* **問題No.4:**
    * **変数名と値:** LB.LBORRES="<0.2" (Bilirubin, Week 24)
    * **矛盾の内容:** LB.LBORRESに"<"記号が含まれており、数値データとして扱えない可能性がある。
    * **問題点の原因（推測）:**
        * 検査結果が検出限界以下であった場合に"<"記号を使用している。
    * **対応策（提案）:**
        * LBSTRESC, LBSTRESNに適切な値を設定する。例：LBSTRESC="<3.42"、LBSTRESN=3.42 (またはNULL)
        * 必要に応じて、データハンドリング手順を明確化する。

全体的なデータ品質の評価:

* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目:
    * AE.AESTDTC, AE.AEENDTC
    * DM.DMDYと各ドメインのDY変数
    * CM.CMTRTとMH.MHTERM, AE.AETERMとの整合性
    * LB.LBORRESの値

問題点:
* **問題No.1:**
    * **変数名と値:** AE.AESTDTC="1986", AE.AEENDTC=NULL (AE Record 2,4), AE.AESTDTC="2013-10-13", AE.AEENDTC="2013-10-15"(AE Record 5), AE.AESTDTC="2013-10-13", AE.AEENDTC="2013-10-15"(AE Record 6)
    * **矛盾の内容:** AE.AESTDTC（有害事象開始日）が、DM.RFSTDTC（治験薬初回投与日）より前の日付（1986年）になっている。DM.RFSTDTC="2013-05-30"であるため、有害事象が治験薬投与前に発生していることになり、矛盾が発生する。 AE Record 5,6では、AESTDTCとAEENDTCが同じ日付だが、AE Record 2,4では、AEENDTCがNULLとなっている。
    * **問題点の原因（推測）:**
        * データ入力時の誤り
        * システムエラー
        * 治験実施計画書からの逸脱
    * **対応策（提案）:**
        * AE.AESTDTC、AE.AEENDTCについて、原資料を確認し、正しい日付に修正する。
        * 必要に応じて、データ入力手順またはシステムに改善を加える。

* **問題No.2:**
    * **変数名と値:** DM.DMDY=-10, LB.LBDY=-10, CM.VISITDY=-7, MH.MHDY=-10, VS.VSDY=-10, QS.QSDY=1
    * **矛盾の内容:** DM.RFSTDTC（治験薬初回投与日）と各ドメインのDY変数との関係に矛盾が発生している可能性がある。DM.RFSTDTC="2013-05-30"に対して、DM.DMDY=-10, LB.LBDY=-10, CM.VISITDY=-7, MH.MHDY=-10, VS.VSDY=-10, QS.QSDY=1となっており、整合性が取れているか確認が必要である。
    * **問題点の原因（推測）:**
        * 日付計算の誤り
        * データ入力時の誤り
    * **対応策（提案）:**
        * DM.RFSTDTCと各ドメインのDY変数の計算ロジックを確認する。
        * 必要に応じて、原資料を確認し、正しい日付に修正する。

* **問題No.3:**
    * **変数名と値:** CM.CMTRT="ASA" (複数のレコード), MH.MHTERM="ALZHEIMER'S DISEASE"
    * **矛盾の内容:** USUBJID="01-701-1363"の被験者は、CMにASA（アセチルサリチル酸）を服用しているが、MHにALZHEIMER'S DISEASE（アルツハイマー病）の既往歴がある。ASAは、一般的にアルツハイマー病の治療薬ではないため、CM.CMINDC（Indication）が欠損していることも含めて、矛盾がないか確認が必要である。
    * **問題点の原因（推測）:**
        * 併用薬の記録が不完全である。
        * データ入力時の誤り
    * **対応策（提案）:**
        * CM.CMINDCを正しく記録する。
        * MHとCMの記録に矛盾がないか、原資料を再確認する。
        * 必要に応じて、ASA服用の理由を医療機関に問い合わせる。

* **問題No.4:**
    * **変数名と値:** LB.LBORRES="<0.2" (Bilirubin, Week 24)
    * **矛盾の内容:** LB.LBORRESに"<"記号が含まれており、数値データとして扱えない可能性がある。
    * **問題点の原因（推測）:**
        * 検査結果が検出限界以下であった場合に"<"記号を使用している。
    * **対応策（提案）:**
        * LBSTRESC, LBSTRESNに適切な値を設定する。例：LBSTRESC="<3.42"、LBSTRESN=3.42 (またはNULL)
        * 必要に応じて、データハンドリング手順を明確化する。

患者ID: 01-701-1363
* クエリNo.1:
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AESTDTC="1986", AE.AEENDTC=NULL (AE Record 2,4)
    * 医療機関への問い合わせ文面:
        * 被験者ID: 01-701-1363のAdverse Event(AE)データについて質問です。
        * AETERMが"HEADACHE"のAEについて、AESTDTC（有害事象開始日）が1986年となっていますが、DM.RFSTDTC（治験薬初回投与日）より前の日付です。
        * 正しいAESTDTCとAEENDTCをご教示ください。
    * 判断理由: 有害事象の開始日が治験薬投与前である場合、治験薬との因果関係を評価できなくなるため、臨床試験の信頼性に影響を与える可能性がある。

* クエリNo.2:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMTRT="ASA" (複数のレコード), MH.MHTERM="ALZHEIMER'S DISEASE"
    * 医療機関への問い合わせ文面:
        * 被験者ID: 01-701-1363のConcomitant Medication(CM)とMedical History(MH)データについて質問です。
        * CMにASA（アセチルサリチル酸）の記録がありますが、MHにALZHEIMER'S DISEASE（アルツハイマー病）の既往歴があります。
        * ASAは、アルツハイマー病に対して一般的に使用される薬剤ではないため、CMのASA服用のIndication（CMINDC）をご教示ください。
    * 判断理由: 併用薬の適応が不明確な場合、データの解釈や他の有害事象との関連性を評価する際に不確実性が生じる可能性がある。

```
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1363

逸脱No.: 1

臨床試験結果への影響度合い: Minor
変数名と値: LB.LBDTC (2013-10-14T08:22), VISIT (WEEK 20)
逸脱内容: 検査日がWEEK20（計画されたStudy Day 140）より2日早い（Study Day 138）。
プロトコル該当箇所: スケジュールに関する記載が不足しているため、特定できず
判断理由: LBドメインのデータにおいて、LBDTC（検査日）がVISIT（計画されたスケジュール）と一致しない場合がある。一般的に、臨床検査はプロトコルで定められたVISITの計画された期間内に行われるべきであり、逸脱は検査のタイミングがプロトコルの要件から外れている場合に発生する。LB.LBDTC (2013-10-14T08:22) はWEEK20（Study Day 140）に該当すると考えられるが、実際の日付は2013-10-14であり、検査日がずれている。

逸脱No.: 2

臨床試験結果への影響度合い: Minor
変数名と値: HGB (各VISITで11.5g/dLを下回る)
逸脱内容: スクリーニング後、ヘモグロビン値が継続的に基準値下限を下回っている。
プロトコル該当箇所: 
[27b] Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes: ↑ creatinine, ↑ total bilirubin, ↑ SGOT, ↑ SGPT, ↑ alkaline phosphatase, ↑ GGT, ↑↓ hemoglobin, ↑↓ white blood cell count, ↑↓ platelet count, ↑↓ serum sodium, potassium, or calcium.

判断理由: 
TI(Trial Inclusion/Exclusion Criteria)に記載されているように、選択基準には、治験への参加を許可するための臨床検査値の範囲が含まれています。LBドメインのデータから、被験者のヘモグロビン(HGB)値が、スクリーニング検査後、一貫して正常範囲を下回っていることが判明しました。ヘモグロビンの基準範囲は11.5-15.8 g/dLですが、WEEK2からWEEK26までの測定値は11.5 g/dLを下回っています。
```


# 01-701-1148
## Task1: Clinical Review Results
**1. 症例サマリー**

*   **患者ID:** 01-701-1148
    *   2013年08月14日 (Day -9): スクリーニング1回目の検査で、白血球数、ヘマトクリット、ヘモグロビン、血小板数など、複数の血液検査項目が正常範囲内。総ビリルビン、尿素窒素、カルシウム、コレステロール、クレアチンキナーゼ、クロール、カリウムなどの血清生化学検査も正常範囲内。尿検査では、色、ケトン体、pH、比重、ウロビリノゲンが正常。主観的特性として、教育レベルは15年。
    *   2013年08月14日 (Day -9): TUMS、TYLENOLをPRNで服用。
    *   2013年08月23日 (Day 1): 初めてXANOMELINE54mgのパッチをTRANSDERMALで投与。
    *   2013年08月25日 (Day 3): 貼付部位紅斑と貼付部位そう痒感が発現、軽度。
    *   2013年10月12日 (Day 51): 下気道感染症を発症、中等度。
    *   2013年11月10日 (Day 80): 下気道感染症が未回復。
    *   2013年12月15日 (Day 115): 側腹部痛を発症、中等度。
    *   2013年12月17日 (Day 117): 尿路結石を発症、中等度だが、同日に回復。側腹部痛も回復。
    *   2013年12月17日 (Day 117): HYDROCODONE W/APAP、NAPROXENを服用。
    *   2014年01月03日 (Day 134): 鼻出血を発症、軽度で、同日に回復。
    *   2014年01月10日 (Day 141): 尿路結石、側腹部痛、鼻出血が回復。
    *   2014年01月25日 (Day 156): CIMETIDINEを服用。
    *   2014年02月08日 (Day 170): うつ病を発症、ACTINIC KERATOSIS（日光角化症）を発症、中等度。
    *   2014年02月12日 (Day 174): FLUOROPLEXをTOPICALでBID投与開始。
    *   2014年02月20日 (Day 182): プロトコルを完了。ACTINIC KERATOSIS（日光角化症）は軽度で、未回復。最終検査では、好酸球数が基準値超え。

---

**2. クエリの作成**

*   **患者ID:** 01-701-1148
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2013-07-29, AE.AEDTC = 2014-02-08
        *   **医療機関への問い合わせ文面:** 
            *   有害事象「うつ病」の発現日（AESTDTC）が2013年7月29日となっていますが、これは試験開始日（2013年8月23日）より前です。有害事象の終了日は2014年2月8日ですが、これは最終観察日と一致しています。
            *   1) 2013年7月29日に発症した有害事象「うつ病」は、本試験の治験薬投与前から存在していた既往歴と解釈して良いか？
            *   2) もし既往歴ではなく、治験薬投与後に発症した有害事象である場合、発現日の日付に誤りがないか確認してください。
            *   3) 有害事象の経過（AEOUT）は「NOT RECOVERED/NOT RESOLVED（未回復）」で正しいか確認してください。
        *   **判断理由:**
            *   DM.RFSTDTC（試験開始日）が2013-08-23であるのに対し、AE.AESTDTC（有害事象「うつ病」の発現日）が2013-07-29となっており、矛盾しています。
            *   Define.xmlの定義では、AE.AESTDTCは「Start Date/Time of Adverse Event」とされており、試験期間中に発現した有害事象の開始日を記録することが想定されています。
            *   DMドメインとAEドメインのデータの矛盾は、データの信頼性を損ない、安全性評価に影響を与える可能性があります。
            *　本症例の既往歴（MH）には「DEPRESSED MOOD（抑うつ気分）」が軽度で存在しています。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2012-02, AE.AEDTC = 2014-02-08
        *   **医療機関への問い合わせ文面:** 
            *   有害事象「消化不良」の発現日が2012年2月となっていますが、これは試験開始日（2013年8月23日）より前です。また、AESTDTCのデータ型は日付型（YYYY-MM-DD）ですが、提供されたデータは年月（YYYY-MM）のみです。
            *   1) 2012年2月に発症した有害事象「消化不良」は、本試験の治験薬投与前から存在していた既往歴と解釈して良いか？
            *   2) もし既往歴ではなく、治験薬投与後に発症した有害事象である場合、発現日の日付に誤りがないか確認してください。
            *   3) AESTDTCには、正確な日付（YYYY-MM-DD）を入力してください。
            *   4) 有害事象の経過（AEOUT）は「NOT RECOVERED/NOT RESOLVED（未回復）」で正しいか確認してください。
        *   **判断理由:**
            *   DM.RFSTDTC（試験開始日）が2013-08-23であるのに対し、AE.AESTDTC（有害事象「消化不良」の発現日）が2012-02となっており、矛盾しています。
            *   Define.xmlの定義では、AE.AESTDTCは「Start Date/Time of Adverse Event」とされており、試験期間中に発現した有害事象の開始日を記録することが想定されています。
            *   DMドメインとAEドメインのデータの矛盾は、データの信頼性を損ない、安全性評価に影響を与える可能性があります。
            *   本症例の既往歴（MH）には「INDIGESTION（消化不良）」が軽度で存在しています。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.EOS = 0.76, LB.LBNRIND = "HIGH", LBDTC = "2014-02-08T14:40"
        *   **医療機関への問い合わせ文面:**
            *   検査値EOS（好酸球）が、2014-02-08T14:40に0.76 THOU/uLと基準範囲外の高値を示しています。
            *   １）この時の患者の状態に特記事項はありましたでしょうか？
        *   **判断理由:**
            *   Week24の好酸球の値のみHighであるため、臨床的に意義があるかどうか判断できません。


## Task2: DM Review Results
データ整合性レビュー：

* 全体的なデータ品質の評価:
    * 総合評価: 一部問題あり
    * データクリーニング/再調査が必要な項目: CM.CMENDTC、CM.CMENDY、AE.AESTDTC、AE.AEENDTC

* 問題点:
    * 問題No.: 1
        * 変数名と値: CM.CMENDTC = "”、CM.CMENDY = null
        * 矛盾の内容: CM.CMENDTCが欠損しているにもかかわらず、CM.CMENDYがnullでないレコードが存在する。CM.CMENDTCが""である場合、CM.CMENDYもnullであるべき。
        * 問題点の原因（推測）: データ入力エラー
        * 対応策（提案）: CM.CMENDTCが""の場合、CM.CMENDYをnullに修正する。
    * 問題No.: 2
        * 変数名と値: CM.CMSTDTC = "2011"
        * 矛盾の内容: CM.CMSTDTCが日付として不完全。
        * 問題点の原因（推測）: データ入力時の誤り、または情報不足。
        * 対応策（提案）: 正確なCMSTDTCを医療機関に確認し、データを修正する。
    * 問題No.: 3
        * 変数名と値: AE.AESTDTC = “2012-02”, AE.AEENDTC = ““
        * 矛盾の内容: AE.AESTDTCが日付として不完全。
        * 問題点の原因（推測）: データ入力時の誤り、または情報不足。
        * 対応策（提案）: 正確なAESTDTCを医療機関に確認し、データを修正する。AEENDTCは有害事象が未解決のためnullが適切。
    * 問題No.: 4
        * 変数名と値: LB.LBDTCの日時と対応する訪問(VISIT, VISITNUM)の不整合
        * 矛盾の内容: LBDTCの日付がVISITで計画された期間外である。
        * 問題点の原因（推測）: LBDTCの日付誤り、VISITのデータ誤り、またはプロトコルからの逸脱。
        * 対応策（提案）: LBDTCの日付とVISITの整合性を確認し、必要に応じて修正する。
    * 問題No.: 5
        * 変数名と値: AE.AESTDTC = “2013-07-29”, AE.AEENDTC = ““
        * 矛盾の内容: AE.AESTDYが負の値になっている。
        * 問題点の原因（推測）: AESTDTCが試験開始日より前になっている。
        * 対応策（提案）: AE.AESTDTC、AEENDTCの日付の正誤を確認し、必要であれば修正する。
    * 問題No.: 6
        * 変数名と値: LB.LBNRIND = "HIGH"かつLB.LBSTRESNが正常範囲内の値
        * 矛盾の内容: 血液検査結果が基準範囲内であるにもかかわらず、LBNRINDがHIGHになっている
        * 問題点の原因（推測）: データ入力ミス、または基準範囲の誤り
        * 対応策（提案）: LBSTRESNが基準範囲内であることを確認した上で、LBNRINDを"NORMAL"に修正する。

クエリの作成：

* 患者ID: 01-701-1148
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: CM.CMENDTC = "2011"
        * 医療機関への問い合わせ文面:
            * 同時服用薬TUMSについて、終了日（CMENDTC）が2011年となっていますが、正しい日付を教えてください。
        * 判断理由:
            * 治験期間中に服用していた可能性があり、データ修正の必要性があるため。
    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC = “2013-07-29”, AE.AEENDTC = ““
        * 医療機関への問い合わせ文面:
            * 有害事象「DYSPEPSIA」について、開始日（AESTDTC）が2012-02となっていますが、正しい日付を教えてください。
            * 終了日が空欄ですが、有害事象は解決しましたでしょうか。
        * 判断理由:
            * 治験期間中に有害事象が発現しているかどうかを正確に把握するため。
    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBSEQ = 271, LB.LBTESTCD = “EOS”, LB.LBNRIND = "HIGH", LB.LBSTRESN =0.76, LB.LBSTNRHI=0.57
        * 医療機関への問い合わせ文面:
            * 好酸球(EOS)の値が0.76で基準範囲上限が0.57ですが、臨床的に問題ないか確認してください。
        * 判断理由:
            * 臨床的に問題がある場合、関連する有害事象を確認する必要があるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1148
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2010-12-12
    *   逸脱内容: 既往歴にアルツハイマー病の記載がある。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria
    *   判断理由: プロトコルの除外基準12(a)に「認知症」の診断が記載されているため。ただし、DMドメインでは対象患者は「probable mild to moderate Alzheimer's Disease」と診断されているため、データに矛盾が発生している。

*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, DM.ACTARM = Xanomeline High Dose
    *   医療機関への問い合わせ文面:
        被験者01-701-1148の既往歴にアルツハイマー病の記載がありますが、これは誤りでしょうか？もしアルツハイマー病の診断が確定している場合、除外基準に抵触する可能性があります。アルツハイマー病の診断が確定しているかどうか、確定している場合、治験薬投与開始前に診断されていたか確認をお願いします。



# 01-701-1180
## Task1: Clinical Review Results
1.  **症例サマリーの作成:**

**患者ID:** 01-701-1180

*   2013年01月28日 (Day -15): スクリーニング検査で Urate (7.9 mg/dL) が基準値上限を超えています。
*   2013年02月12日 (Day 1): 嘔吐 (Vomiting) が発現し、軽度 (Mild) と報告されています。ADAS-Cog(11) Subscoreは30、各Disability Assessment for Dementia (DAD) 項目は、電話、外出、財務と書簡、薬、娯楽と家事に関する項目を含め、ほとんどが「はい」と評価されています。EAT His/Her Meals at a Normal Pace は N (いいえ)と評価されています。
*   2013年02月15日 (Day 4): 頻尿 (Micturition Urgency) が発現し、軽度 (Mild) と報告されています。
*   2013年02月25日 (Day 14): 頻尿が継続中です。頭痛 (Headache) が発現し、中程度 (Moderate) と報告されています。
*   2013年03月06日 (Day 23): 鼻咽頭炎 (Nasopharyngitis) が発症しました。
*   2013年03月11日 (Day 28): 鼻咽頭炎は治癒しましたが、頭痛は継続中です。Urate (7.6 mg/dL) が依然として基準値上限を超えています。
*   2013年03月19日 (Day 36): 適用部位紅斑 (Application Site Erythema)、適用部位掻痒感 (Application Site Pruritus)、および適用部位小水疱 (Application Site Vesicles) が発現し、すべて中程度 (Moderate) と報告されています。頻尿は治癒しました。
*   2013年03月23日 (Day 40): 最終検査を実施。Urate (5.9 mg/dL) は基準値内です。
*   2013年04月07日 (Day 55): AEフォローアップ。

---

2.  **クエリの作成 (必要な場合のみ):**

**患者ID:** 01-701-1180

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AETERM = SUDDEN DEATH
        *   AE.AESTDTC = 2013-02-15
    *   **医療機関への問い合わせ文面:** 2013年2月15日に「突然死」と報告されていますが、転帰は「回復」と報告されています。これは矛盾していると考えられます。「報告された症状」と「転帰」について、医療機関に確認してください。
    *   **判断理由:** SDTM AEドメインでは、AEOUT（転帰）は、AETERM（有害事象）のイベントが最終的にどうなったかを示す重要な変数です。通常、「死亡」と「回復」という転帰は両立しません。
*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   MH.MHTERM = DEPRESSION (ANXIETY)
        *   MH.MHSTDTC = ""
    *   **医療機関への問い合わせ文面:** 患者の病歴として、「うつ病（不安）」が報告されていますが、MHSTDTC（病歴イベントの開始日時）が空欄です。うつ病の開始日について、医療機関に確認してください。
    *   **判断理由:** MHSTDTCは、MHドメインでMedical Historyの開始日を示す重要な変数です。この情報が欠落していると、患者の病歴を正確に把握することが困難になります。
*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   AE.AETERM = APPLICATION SITE ERYTHEMA
        *   AE.AETERM = APPLICATION SITE PRURITUS
        *   AE.AETERM = APPLICATION SITE VESICLES
        *   AE.AESTDTC = 2013-03-19
        *   AE.AEENDTC = ""
    *   **医療機関への問い合わせ文面:** 適用部位紅斑、適用部位掻痒感、適用部位小水疱の有害事象が2013年3月19日に発現していますが、AEENDTC（有害事象の終了日時）が空欄です。これらの有害事象の転帰と終了日について、医療機関に確認してください。
    *   **判断理由:** AEENDTCは、有害事象の転帰を評価する上で重要な変数です。この情報が欠落していると、有害事象の持続期間や転帰を正確に把握することが困難になります。


## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: AE.AESTDTC, AE.AEENDTC, DS.DSSTDTC, LB.LBDTC, MH.MHSTDTC, QS.QSDTC, VS.VSDTC, 

問題点:

*   **問題No.1:**
    *   **変数名と値:** AE.AESTDTC = "2002", AE.AEENDTC = "", AETERM = "HEADACHE"
    *   **矛盾の内容:** AE.AESTDTCの値が2002年となっており、他のAEデータやDMデータから逸脱している。試験期間と照らし合わせても不自然。AEENDTCが欠損していることも不自然。
    *   **問題点の原因（推測）:** データ入力時の誤り、またはAEの開始日が不明。
    *   **対応策（提案）:** 
    *   医療機関にAESTDTCとAEENDTCの日付を確認する。
    *   AESTDTCが誤りの場合、正しい日付に修正する。
    *   AEENDTCが不明な場合、状況に応じて適切な値を設定するか、理由を記録する。

*   **問題No.2:**
    *   **変数名と値:** AE.AESTDTC = "2013-02-15", AEENDTC = "2013-03-19", AETERM = "MICTURITION URGENCY", AE.AESEQ = 3
    *   **矛盾の内容:** AE.AESTDY = 4, AESTDTC = "2013-02-15"とAE.AEDTC = "2013-02-25"から、有害事象の開始日が治験薬投与前になっている。
    *   **問題点の原因（推測）:** 因果関係の評価に影響を与える可能性があるため、データ誤りの可能性を考慮する。
    *   **対応策（提案）:** EXドメインで治験薬の投与開始日を確認し、矛盾がある場合は、AESTDTCを修正する。

*   **問題No.3:**
    *   **変数名と値:** DS.DSSTDTC = "2013-03-23", DSDTC = "2013-03-23T12:45", VISIT = "WEEK 6", DSTERM = "FINAL LAB VISIT"
    *   **矛盾の内容:** LBドメインのデータを見ると、WEEK6の検査はLBDTC="2013-03-23T12:45"に実施されている。DS.DSDTCとLB.LBDTCの値は同じ日付だが、DS.DSSTDTCが時間情報を持たないため、厳密には一致しない可能性がある。
    *   **問題点の原因（推測）:** DSドメインとLBドメイン間の時間情報の粒度が異なる。
    *   **対応策（提案）:** DSDTCの時間情報をDSSTDTCに反映させる、または、DSSTDTCに時間情報がない理由を記録する。

*   **問題No.4:**
    *   **変数名と値:** LB.LBDTC
    *   **矛盾の内容:** LB.LBDTCはdatetime型だが、DM.RFSTDTC（2013-02-12）より前の日付（例：2013-01-28）が存在する。
    *    **問題点の原因（推測）:** データ入力ミス、または治験薬投与前に実施された検査。
    *   **対応策（提案）:** 
    *   LBDTCの日付がDM.RFSTDTCより前の日付になっている理由を確認する。
    *   治験薬投与前に実施された検査の場合、プロトコルに違反していないか確認する。

*   **問題No.5:**
    *   **変数名と値:** CM.CMSTDTC="2006"
    *   **矛盾の内容:** CM.CMSTDTC, CMENDTCの値が不適切。この試験のDM.RFSTDTC="2013-02-12"であり、6年前のデータが混入している。
    *   **問題点の原因（推測）:** 
    *   データ入力時の誤り
    *   **対応策（提案）:**
    *   CMSTDTCとCMENDTCの日付を再確認し、必要であれば修正する。
    *   矛盾が解消されない場合は、データ収集時の記録を参照し、正確な日付を特定する。

*   **問題No.6:**
    *   **変数名と値:** MH.MHSTDTC=""
    *   **矛盾の内容:** 既往歴(MH)の開始日が欠損している。
    *   **問題点の原因（推測）:**
    *   データ入力時の誤り
    *   **対応策（提案）:**
    *   MHSTDTCの日付を再確認し、必要であれば修正する。
    *   MHTERM="DEPRESSION (ANXIETY)"のため、DM.DMDTCとAEのデータから、関連するAESTDTCを調査する。

*   **問題No.7:**
    *   **変数名と値:** RELREC.RELTYPEが空欄
    *   **矛盾の内容:** RELTYPEは必須変数であるにもかかわらず値が存在しない。
    *   **問題点の原因（推測）:** データの登録漏れ、またはデータ処理の誤り
    *   **対応策（提案）:** RELTYPEに適切な値を設定する。

*   **問題No.8:**
    *   **変数名と値:** DS.DSTERM = "ADVERSE EVENT", DS.DSDECOD = "ADVERSE EVENT", RELREC.RDOMAIN = "AE", RELREC.IDVARVAL = "9"
    *   **矛盾の内容:** RELRECデータセットにおいて、DSドメインのレコード（ADVERSE EVENT）とAEドメインのレコード（APPLICATION SITE ERYTHEMA）がRELTYPEで関連付けられていない。RELTYPEが空欄。
    *   **問題点の原因（推測）:** データ登録時の関連付け漏れ。
    *   **対応策（提案）:** RELTYPEに適切な関係の種類（例：HAS AE）を設定する。

クエリの作成:

患者ID: 01-701-1180
*   **クエリNo.1:**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDTC = "2002", AE.AEENDTC = ""
    *   **医療機関への問い合わせ文面:**
    患者ID 01-701-1180 の有害事象 HEADACHE の開始日と終了日について確認させてください。現在、開始日が2002年、終了日が空欄となっています。
    *   **判断理由:** 有害事象の開始日は、治験薬との因果関係を評価する上で重要な情報です。ADの治療薬開発において、HEADACHEは重要な有害事象である可能性があり、データが正しくない場合、安全性評価に影響を与える可能性があります。
*   **クエリNo.2:**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** CM.CMSTDTC="2006"
    *   **医療機関への問い合わせ文面:**
    患者ID 01-701-1180 の併用薬CENTRUMの開始日について確認させてください。CMSTDTC="2006"となっていますが、DM.RFSTDTC="2013-02-12"との整合性が取れません。
    *   **判断理由:** CMSTDTCは併用薬の使用状況を把握する上で重要な情報です。日付が正しくない場合、併用薬が臨床試験に与える影響を正しく評価できない可能性があります。

*   **クエリNo.3:**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.DAITM17, baseline = N, week6 = Y
    *   **医療機関への問い合わせ文面:**
    患者ID 01-701-1180 のDisability Assessment for Dementia (DAD)質問項目17、EAT HIS/HER MEALS AT A NORMAL PACE の回答について確認させてください。
    ベースラインでは"N", WEEK6では"Y"と回答されています。DADは介護者が評価しますが、MMSEで10-23の患者さんの食事ペースが、6週間で変化することは考えにくいです。
    *   **判断理由:** DADスコアの信頼性向上。


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1180

*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2008-09-21
    *   逸脱内容: この患者はアルツハイマー病の病歴を有しており、TIドメインのEXCL12「重篤な神経疾患の診断」という除外基準に抵触する可能性がある。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [12] Diagnosis of serious neurological conditions, including
    *   判断理由: 
        *   TIドメインのEXCL12には「重篤な神経疾患の診断」という除外基準があり、MHドメインには「ALZHEIMER'S DISEASE」の病歴があるため、除外基準に抵触する可能性があります。ただし、TIドメインのEXCL12の基準には具体的な疾患の重症度に関する記述がないため、臨床試験への影響度合いはMajorとします。
        *   アルツハイマー病の診断基準（軽度、中等度）と、本試験への組み入れ基準との整合性を確認する必要があります。

患者ID: 01-701-1180
*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = DEPRESSION (ANXIETY)
    *   逸脱内容: 
        *   この患者はうつ病（不安）の病歴を有しており、TIドメインのEXCL13「スクリーニングの3ヶ月以内のDSM-IV基準を満たすうつ病エピソード」またはEXCL14「過去5年以内の精神疾患の病歴」という除外基準に抵触する可能性があります。
        *   DMドメインにはDTHFL（Subject Death Flag）がないため、本件はTIドメインのEXCL12「重篤な神経疾患の診断」の除外基準にも抵触する可能性があります。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [13] Episode of depression meeting DSM-IV criteria within 3 months of screening. [14] A history within the last 5 years
    *   判断理由:
        *   TIドメインにはEXCL13「スクリーニングの3ヶ月以内のDSM-IV基準を満たすうつ病エピソード」またはEXCL14「過去5年以内の精神疾患の病歴」という除外基準があり、MHドメインには「DEPRESSION (ANXIETY)」の病歴があるため、除外基準に抵触する可能性があります。ただし、TIドメインのEXCL13とEXCL14の基準には具体的な疾患の重症度に関する記述がないため、臨床試験への影響度合いはMajorとします。
        *   うつ病の診断基準（DSM-IV、発症時期、重症度）と、本試験への組み入れ基準との整合性を確認する必要があります。

患者ID: 01-701-1180
*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBTESTCD = URATE, LB.LBORRES = 7.9, LB.LBORNRHI = 7.5, VISIT = SCREENING 1
    *   逸脱内容: スクリーニング検査において、尿酸値が基準範囲上限を超過している。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.
    *   判断理由:
        *   TIドメインのEXCL27には「検査値が施設基準範囲外の場合」という除外基準があり、LBドメインには「URATE」の検査値が基準範囲外のため、除外基準に抵触する可能性があります。
        *   TIドメインのEXCL27の基準には具体的な逸脱の程度に関する記述がないため、臨床試験への影響度合いはMinorとします。

患者ID: 01-701-1180
*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Critical
    *   変数名と値: QS.QSTESTCD = MHITM04, QSORRES = ABSENT, VISIT = SCREENING 1
    *   逸脱内容: 改訂版Hachinski虚血スコア項目の4. 夜間錯乱について「いいえ」と回答されている。
    *   プロトコル該当箇所: 
        *   3.4.2.1. Inclusion Criteria [4] Modified Hachinski Ischemic Scale score of <= 4. (Protocol Attachment LZZT.8).
        *   Protocol Attachment LZZT.8: Hachinski Ischemic Scale
    *   判断理由:
        *   MMSEと並んで、Modified Hachinski Ischemic Scale（MHIS）はADと診断するための重要な評価指標です。
        *   ハキンスキー虚血スコアは、アルツハイマー病（AD）と血管性認知症（VaD）を鑑別するために用いられる指標であり、4点以下がADの可能性が高いとされます。
        *  しかし、本研究では Modified Hachinski Ischemic Scale（MHIS）を使用することになっており、データセットには、modifiedとunmodifiedのデータが混在している可能性があります。
        *  Modified Hachinski Ischemic Scale（MHIS）を使用した場合、今回のデータからは合計スコアを算出できません。MHITM07にPRESENT(1点)と記録されていること以外はすべてABSENT(0点)であり、MHITM07を除いた残りの項目の値が全て0点であった場合でもMHISが4点以下であるとは断定できません。Modified Hachinski Ischemic Scale（MHIS）のスコアによっては、組み入れ基準を満たさない可能性があり、臨床試験結果への影響度合いはCriticalと考えられます。

患者ID: 01-701-1180
*   逸脱No.: 5
    *   臨床試験結果への影響度合い: Critical
    *   変数名と値: QS.QSTESTCD = MMITM05, QSORRES = 0, VISIT = SCREENING 1
    *   逸脱内容: MMSE項目の5. 三語想起が0点である。
    *   プロトコル該当箇所: 
        *   3.4.2.1. Inclusion Criteria [3] MMSE score of 10 to 23.
        *   Protocol Attachment LZZT.6: Mini-Mental State Examination (MMSE)
    *   判断理由:
        *   MMSEは認知機能を評価するための重要な指標であり、MMSEの合計スコアが10〜23点の範囲内であることが組み入れ基準となっています。
        *   しかし、MMSEの各項目の値が合計スコアにどのように影響するかは不明です。MMITM05の0点という値が、MMSEの合計スコアを10点未満にする要因となる場合、組み入れ基準を満たさない可能性があり、臨床試験結果への影響度合いはCriticalと考えられます。

*   患者ID: 01-701-1180
    *   逸脱No.: 6
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AETERM = SUDDEN DEATH
        *   逸脱内容:
            *   有害事象としてSUDDEN DEATHが報告されています。
        *   プロトコル該当箇所:
            *   3.9.3.2.2. Serious Adverse Events
        *   判断理由:
            *   SUDDEN DEATHは、生命を脅かす可能性のある重篤な有害事象であり、臨床試験の安全性評価に重大な影響を与える可能性があります。

*   患者ID: 01-701-1180
    *   逸脱No.: 7
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: EX.EXDOSE = 54mg -> 81mg
        *   逸脱内容:
            *   治験薬の投与量がプロトコルに違反している可能性があります。
            *   DMドメインでは、本被験者のARM(Description of Planned Arm)は、Xanomeline High Doseとなっています。
            *   しかしながらTSドメインでは、High Doseは81mgの投与を計画していることに対し、1回目の投与量が54mgとなっています。
            *   Xanomeline High Doseに割り当てられた被験者に対して、初期投与量が54mgで開始されることがプロトコルで許可されているかを確認する必要があります。
        *   プロトコル該当箇所:
            *   3.1 Summary of Study Design, 3.6 Dosage and Administration
        *   判断理由:
            *   EXドメインに記録されている投与量（EXDOSE）が、プロトコルで規定された投与量と一致しているかどうかを確認する必要があります。プロトコルに違反している場合、有効性評価に影響を与える可能性があります。
            *   投与量の変更がプロトコルで許可されている場合や、何らかの理由で投与量を変更する必要があった場合、その理由が記録されているか確認する必要があります。

*   患者ID: 01-701-1180
    *   逸脱No.: 8
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: VS.VSTESTCD = TEMP, VS.VSORRES = 99.2, VISIT = WEEK 6
        *   逸脱内容: Week6の体温が99.2Fと高い。
        *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria
        *   判断理由:
            *   発熱の原因が感染症などの除外基準に合致するかどうか確認が必要です。
            *   TI.IETESTに発熱に関する明確な記述はありませんが、EXCL24の感染症に該当する可能性があります。
            *   重篤な感染症でない場合は問題ありません。

患者ID:
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Critical
    *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE
    *   医療機関への問い合わせ文面:
        *   被験者のアルツハイマー病の診断時期、重症度、および現在の状態について詳細な情報をご提供ください。
        *   Modified Hachinski Ischemic Scale 評価に使用したデータと、そのスコアの算出根拠をご提示ください。
        *   Modified Hachinski Ischemic Scale の各項目の評価根拠について、詳細をご説明ください。
        *   MMSEの各項目の評価根拠について、詳細をご説明ください。
    *   判断理由:
        *   MHにあるALZHEIMER'S DISEASEの病歴はTIのEXCL12に抵触する可能性があり、組み入れ基準を満たしているか確認する必要があるため。
        *   除外基準に抵触するかどうかを判断するために、詳細な病歴が必要です。

*   患者ID:
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM = DEPRESSION (ANXIETY)
        *   医療機関への問い合わせ文面:
            *   被験者のDEPRESSION (ANXIETY) の診断時期、種類、重症度、および最近のエピソード（特にスクリーニング前3ヶ月以内）について詳細な情報をご提供ください。
            *   使用された診断基準（DSM-IVなど）をご提示ください。
            *   DHEA, HISMANAL, MEDROL DOSEPAK, MELATONIN, NEOSPORIN /USA/, SUDAFED, WESTCORT と DEPRESSION (ANXIETY) の関連性についてご提示ください。
        *   判断理由:
            *   MHにあるDEPRESSION (ANXIETY) の病歴はTIのEXCL13, EXCL14に抵触する可能性があり、組み入れ基準を満たしているか確認する必要があるため。
            *   除外基準に抵触するかどうかを判断するために、詳細な病歴が必要です。

患者ID: 01-701-1180
*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBTESTCD = URATE, LB.LBORRES = 7.9, LB.LBORNRHI = 7.5
    *   医療機関への問い合わせ文面:
        *   スクリーニング時の尿酸値が基準範囲を超えていますが、この逸脱について臨床的な判断は行われていますでしょうか？
        *   もし判断が行われている場合、その内容と根拠をご提示ください。
    *   判断理由:
        *   TIドメインのEXCL27に抵触する可能性があるため、尿酸値上昇の原因や臨床的な意義を確認する必要があるため。

クエリなし


# 01-701-1034
## Task1: Clinical Review Results
 
 ### 1. 症例サマリーの作成:
 
 **患者ID:** 01-701-1034
 
 *   2014年06月24日 (Day -7): スクリーニング検査で、白血球は7.10 THOU/uLで正常範囲内。総コレステロールは298 mg/dLで正常範囲内だが上限に近い。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。血液検査では異型リンパ球が1%、アニソサイト1+と異常所見が見られる。甲状腺刺激ホルモン(TSH)は0.27 uIU/mLと低い。
 *   2014年07月15日 (Day 15): 血液検査で白血球数8.35 THOU/uLで正常範囲内。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。総コレステロールは271 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が34 U/Lと基準値下限を下回っている。赤血球の平均容積（MCV）が106 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト1+と異常所見が見られる。
 *   2014年07月29日 (Day 29): 血液検査で白血球数5.66 THOU/uLで正常範囲内。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。総コレステロールは284 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が36 U/Lと基準値範囲内。赤血球数が3.80 MILL/uLと基準値下限を下回っている。血液検査では異型リンパ球0、アニソサイト1+と異常所見が見られる。
 *   2014年08月11日 (Day 42): 血液検査で白血球数10.46 THOU/uLで正常範囲内。総コレステロールは223 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が33 U/Lと基準値下限を下回っている。赤血球数が3.70 MILL/uLと基準値下限を下回っている。血液検査では異型リンパ球0、アニソサイト1+と異常所見が見られる。
 *   2014年08月26日 (Day 57): 血液検査で白血球数6.90 THOU/uLで正常範囲内。総コレステロールは291 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が29 U/Lと基準値下限を下回っている。赤血球数が4.00 MILL/uLで正常範囲内。赤血球の平均容積（MCV）が101 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト0と異常所見が見られる。
 *   2014年08月27日 (Day 58): 治験薬投与部位に軽度の掻痒感を伴う紅斑が発生。
 *   2014年09月25日 (Day 87): 血液検査で白血球数7.45 THOU/uLで正常範囲内。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。総コレステロールは261 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が34 U/Lと基準値下限を下回っている。赤血球数が3.80 MILL/uLと基準値下限を下回っている。赤血球の平均容積（MCV）が101 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト0と異常所見が見られる。
 *   2014年10月21日 (Day 113): 血液検査で白血球数6.72 THOU/uLで正常範囲内。総コレステロールは277 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が34 U/Lと基準値下限を下回っている。赤血球数が3.80 MILL/uLと基準値下限を下回っている。赤血球の平均血色素量（MCH）が35 pgと基準値上限を超えている。赤血球の平均容積（MCV）が103 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト1+と異常所見が見られる。
 *   2014年11月02日 (Day 125): 軽度の疲労感が出現。
 *   2014年11月18日 (Day 141): 血液検査で白血球数8.26 THOU/uLで正常範囲内。総コレステロールは236 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が31 U/Lと基準値下限を下回っている。赤血球数が3.90 MILL/uLで正常範囲内。赤血球の平均血色素量（MCH）が33 pgで正常範囲内。赤血球の平均容積（MCV）が102 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト1+と異常所見が見られる。
 *   2014年12月17日 (Day 170): 血液検査で白血球数9.71 THOU/uLで正常範囲内。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。総コレステロールは236 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が40 U/Lと基準値範囲内。赤血球数が3.50 MILL/uLと基準値下限を下回っている。赤血球の平均血色素量（MCH）が37 pgと基準値上限を超えている。赤血球の平均ヘモグロビン濃度（MCHC）が36 g/dLで正常範囲内。赤血球の平均容積（MCV）が102 fLと基準値上限を超えている。血液検査では異型リンパ球0、マクロサイト1+と異常所見が見られる。
 *   2014年12月30日 (Day 183): 血液検査で白血球数9.08 THOU/uLで正常範囲内。尿検査ではpH5.0、ケトン体0、ウロビリノゲン0で正常。総コレステロールは208 mg/dLで正常範囲内。アルカリホスファターゼ(ALP)が27 U/Lと基準値下限を下回っている。赤血球数が3.70 MILL/uLと基準値下限を下回っている。赤血球の平均血色素量（MCH）が35 pgと基準値上限を超えている。赤血球の平均容積（MCV）が102 fLと基準値上限を超えている。血液検査では異型リンパ球0、アニソサイト1+と異常所見が見られる。

 ### 2. クエリの作成
 
 *   **患者ID:** 01-701-1034
     *   **クエリNo.:** 1
         *   **臨床試験結果への影響度合い:** Major
         *   **変数名と値:**
             *   AE.AETERM = APPLICATION SITE PRURITUS
             *   AE.AESTDTC = 2014-08-27
             *   AE.AEENDTC = "" (NULL)
             *   LB.LBTESTCD = EOS
             *   LB.LBDTC = 2014-08-26
             *   LB.LBORRES = 0.09
             *   LB.LBDTC = 2014-09-25
             *   LB.LBORRES = 0.10
         *   **医療機関への問い合わせ文面:**
             *   治験参加者01-701-1034に2014年8月27日から治験薬投与部位に掻痒感を伴う紅斑が発生していますが、現在も継続中でしょうか？
             *   もしそうであれば、治験薬との因果関係について治験担当医師の見解を教えてください。
             *   本事象発生前後の好酸球の値に変化はありましたでしょうか？
             *   もしあれば、本事象と好酸球増多症との関連性について治験担当医師の見解を教えてください。
         *   **判断理由:**
             *   8/27から紅斑が発生しているが、AEENDTCがNULLであり、治験終了時まで継続している可能性がある。
             *   治験薬との関連がPROBABLEと判断されている。
             *  添付資料に、治験薬投与による皮膚炎と好酸球増多の関連性が示唆されている。
             *   9/25にNPI_T14項目の検査を実施している。
             *   プロトコルに以下の記述があり、安全性評価に重要な情報であるため。
 >  If needed, the edges of the patch may be secured with a special adhesive tape that will be provided. If daily doses are reduced, improperly administered, or if a patch becomes detached and requires application of a new patch on three or more days in any 30-day period, the CRO research physician will be notified.

 *   **患者ID:** 01-701-1034
     *   **クエリNo.:** 2
         *   **臨床試験結果への影響度合い:** Minor
         *   **変数名と値:**
             *   VS.VSTESTCD = SYSBP, DIABP
             *   VS.VSDTC (WEEK24) = 2014-12-17
             *   QS.NPITM03 (WEEK24) =1
         *   **医療機関への問い合わせ文面:**
             *   治験参加者01-701-1034の2014-12-17のバイタルサインは、起立時に収縮期血圧が198mmHg、拡張期血圧が97mmHgと高血圧の基準を超えています。
             *  Week18(T)のNPI調査で、介護者は興奮/攻撃性の頻度と重症度と介護者の苦痛について、数値が改善しています。これらの症状に関連した薬剤投与の併用または非併用に関する医療記録を調査して、これらの症状を緩和するために使用されると予想される薬剤の種類と投与量に関する情報を提供していただけますでしょうか?
         *   **判断理由:**
            *  Week24に高血圧の傾向がある。
            *  Week6に、介護者の評価ではあるが興奮/攻撃性が見られている。
            * 77歳と高齢であることからも、安全性に懸念がある。

 *   **患者ID:** 01-701-1034
     *   **クエリNo.:** 3
         *   **臨床試験結果への影響度合い:** Minor
         *   **変数名と値:**
             *   LB.LBTESTCD = TSH
             *   LB.LBDTC (SCREENING 1) = 2014-06-24
             *   LB.LBORRES = 0.27
         *   **医療機関への問い合わせ文面:**
             *   治験参加者01-701-1034の甲状腺刺激ホルモン(TSH)が、スクリーニング時に基準範囲を下回っています。
             *   本データから、被験者は甲状腺機能低下症の治療を受けている可能性が示唆されます。
             *   併用薬にLEVOTHROID（甲状腺ホルモン剤）の投与が確認できますが、MHドメイン（Medical History）にはHYPOTHYROIDISMの既往歴しか記録されていません。
             *   本被験者のHYPOTHYROIDISMについて、罹患時期、LEVOTHROIDの投与開始時期、投与量、および甲状腺機能に関する直近の臨床検査データをご提供いただけますでしょうか？
         *   **判断理由:**
             *  DMドメインの既往歴とCMドメインの投薬状況、LB検査値に矛盾がある。


## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり、要修正
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, AE.AETERM, VS.VSPOS, LB.LBSEQ, LB.LBDTC

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC = "2012", CM.CMENDTC = "" (null)
    *   **矛盾の内容:** CM.CMSTDTCは2012年と記録されているが、日付の形式が不完全。また、CM.CMENDTCが欠損している。
        カルシウムの摂取期間が不明確。他の薬剤のCMENDTCは1960, 1977, 1946, 1949, 1977などの過去年号が記録されており、矛盾している可能性がある。Estrogenの投与終了日が1960年で、開始日と一致している。
        HYDROCORTISONEのCMSTDTCが2014-08-27で固定されているが、CMENDTCが2014-12-30などばらつきがあり、矛盾している可能性がある。
    *   **問題点の原因（推測）:** データ入力時の誤り、またはデータ収集時の不備。
    *   **対応策（提案）:**
        *   医療機関にCM.CMSTDTCとCM.CMENDTCの正確な日付を確認する。
        *   必要に応じて、CM.CMENDTCに終了日を入力するか、薬剤が継続されている場合は適切な処置を行う（例：データ更新）。
        *   EstrogenとHYDROCORTISONEのCMENDTCの妥当性を検証する。

*   **問題No.2:**
    *   **変数名と値:** AE.AETERM = "MALIGNANT HYPERTENSION", MH.MHTERM = "BLOOD PRESSURE INCREASED"
    *   **矛盾の内容:** USUBJIDが01-701-1034の患者は、AE.AETERMとして "MALIGNANT HYPERTENSION"が報告されている一方で、MH.MHTERMとして "BLOOD PRESSURE INCREASED"という既往歴がある。
        高血圧は一般的な疾患であり、AD患者の試験への参加に影響を与える可能性がある。登録時に存在していた高血圧と、試験中に発症した高血圧を区別する必要がある。
    *   **問題点の原因（推測）:**
        *   AEとMHで使用されている辞書（MedDRA）のバージョンが異なり、コーディングにずれが発生した可能性がある。
        *   AE.AETERMに"MALIGNANT HYPERTENSION"と記録されたものの、実際にはそこまで重篤な状態ではなかった可能性がある。
    *   **対応策（提案）:**
        *   医療機関に問い合わせて、有害事象と既往歴の詳細な情報を確認し、正確なMedDRAコードを特定する。
        *   必要に応じて、AE.AETERMまたはMH.MHTERMを適切な用語に修正する。

*   **問題No.3:**
    *   **変数名と値:** LB.LBSEQの連番
    *   **矛盾の内容:** LBドメインにおいて、LBSEQが被験者内で一意に連続していない。LBSEQは各被験者内で一意である必要がある。
    *   **問題点の原因（推測）:** データの抽出、変換、ロード（ETL）プロセスにおけるエラー、データのソートまたはフィルタリングの問題、あるいはデータ入力エラー。
    *   **対応策（提案）:**
        *   データ抽出、変換、ロード（ETL）プロセスを見直し、LBSEQが被験者毎に正しく連番になっているか確認する。
        *   データ入力手順を見直し、データ入力者に対してLBSEQの連番に関するトレーニングを実施する。
        *   Define.xmlにLBSEQの連番に関する制約が定義されている場合は、その制約がデータに適用されていることを確認する。

*   **問題No.4:**
    *   **変数名と値:** VS.VSPOSの値
    *   **矛盾の内容:** 仰臥位(SUPINE)と立位(STANDING)の血圧測定が、スクリーニング1,スクリーニング2, ベースライン、各WEEKで実施されているが、AMBUL ECG REMOVAL（心電図除去）のVISITでも実施されている。しかし、TV(Trial Visit)にはAMBUL ECG REMOVALのVISITに、ARMCD(Planned Arm Code), ARM（Description of Planned Arm)が定義されていない。
    *   **問題点の原因（推測）:** プロトコルで計画された内容と、SVドメインに登録されたVISITの情報に不整合が発生している。
    *   **対応策（提案）:**
        *   TVドメインにAMBUL ECG REMOVALのVISITを定義し、ARMCD, ARMを登録する。
        *   VSドメインのAMBUL ECG REMOVALの血圧測定が、必須でなければ削除することも検討する。

*   **問題No.5:**
    *   **変数名と値:** TSHの検査値
    *   **矛盾の内容:** USUBJIDが"01-701-1034"の被験者のTSH（甲状腺刺激ホルモン）の検査結果が、スクリーニング1で "0.27 uIU/mL" とLOWの範囲外れの値を示している。しかし、除外基準28には「甲状腺機能検査が基準範囲外の場合は除外」とある。
    *   **問題点の原因（推測）:** 試験登録時のデータに誤りがあるか、除外基準の解釈に誤りがあった可能性がある。
    *   **対応策（提案）:** スクリーニング時のTSH値が除外基準を満たしているか確認し、組み入れ可能であった理由を検証する。

*   **問題No.6:**
    *   **変数名と値:** LB.LBDTCの日付とLB.VISITDYの値
    *   **矛盾の内容:** 
    LBドメインにおいて、LBDTCの日付から計算されるべきLB.LBDY（Study Day of Specimen Collection）の値が、VISITDY（Planned Study Day of Visit）と一致していない箇所がある。LBDTCの日付とLB.VISITDYの値にずれが発生している場合、データ収集日と計画された来院日に不整合が発生している可能性がある。
        *   例：Albuminの検査(LBSEQ=167)
            *   LBDTC: 2014-09-25T15:40
            *   LBDY: 87
            *   VISIT: WEEK 12
            *   VISITDY: 84
    *   **問題点の原因（推測）:**
        *   検査実施日の記録ミス
        *   計画外の検査の実施
        *   LB.LBDYの計算ロジックのエラー
    *   **対応策（提案）:**
        *   LBDTCとLB.VISITDYのずれが発生している理由を調査し、LBDTCが正しい日付であるか確認する。
        *   Define.xmlに定義されたLB.LBDYの計算ロジックが正しく実装されているか検証する。
        *   必要に応じて、LBDTCまたはLB.VISITDYの値を修正する。

**クエリの作成:**

*   **患者ID:** 01-701-1034
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC, CM.CMENDTC (CALCIUM, ESTROGEN NOS, HYDROCORTISONE)
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1034において、CALCIUM, ESTROGEN NOS, HYDROCORTISONEのCM（併用薬）の開始日と終了日について、記録に誤りがないか確認してください。特に、開始日と終了日が矛盾していないか、HYDROCORTISONEのCMSTDTCが固定されている理由をご確認ください。
        *   **判断理由:** 併用薬の使用期間は、有害事象の評価や薬物相互作用の可能性を評価する上で重要な情報です。不正確な日付は、これらの評価に影響を与える可能性があります。

*   **患者ID:** 01-701-1034
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM, MH.MHTERM
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1034において、AE（有害事象）として報告された "MALIGNANT HYPERTENSION" と、MH（既往歴）として報告された "BLOOD PRESSURE INCREASED" について、詳細な病歴と診断情報をご確認ください。
            *   Maligant Hypertensionは重篤な有害事象であり、高血圧との関連性を確認する必要がある。
        *   **判断理由:** 
            *   DM（Demographics）ドメインとAE(Adverse Event), MH(Medical History)ドメイン間の整合性を確認するため。
            *    不適切な高血圧の管理は、試験の安全性評価に影響を与える可能性があります。

*   **患者ID:** 01-701-1034
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBDTC, LB.VISITDY
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1034の各検査について、検体採取日（LB.LBDTC）と計画された来院日（LB.VISITDY）にずれが発生している理由をご確認ください。特に、計画外の検査が実施された場合、その詳細（理由、日付など）をご提供ください。
        *   **判断理由:**
            *   検査データの信頼性を確保し、プロトコルからの逸脱がないか確認するため。
            *   検査データの解釈に影響を与える可能性があるため。


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1034
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値:
        *   LB.LBTESTCD: TSH
        *   LB.LBORRES: 0.27
        *   LB.LBORRESU: uIU/mL
        *   LB.LBORNRLO: 0.32
        *   LB.LBORNRHI: 5
        *   LB.LBNRIND: LOW
    *   逸脱内容: 
        *   被験者01-701-1034のスクリーニング検査において、甲状腺刺激ホルモン（TSH）の値が0.27 uIU/mLと基準範囲下限を下回っている。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [28b]
    *   判断理由: 
        *   プロトコルでは、「Central laboratory test values below reference range for folate, and vitamin B12, and outside reference range for thyroid function tests」を除外基準としています。
        *  LBドメインのデータを確認した結果、LBTESTCDが"TSH"の検査結果において、LBORRESの値が0.27 uIU/mLであり、LBORNRLO（基準範囲下限）の値0.32 uIU/mLを下回っています。したがって、除外基準[28b]に抵触している可能性があります。
        *  ただし、プロトコルには「Patients will be allowed to enroll with results of 0.03 to 6.2 if patients are taking stable doses of exogenous thyroid supplements, with normal free thyroid index, and show no clinical signs or symptoms of thyroid abnormality.」という記述があり、甲状腺機能検査値が基準範囲外でも、甲状腺ホルモン剤を服用しており、臨床的に問題がない場合は登録可能と解釈できます。
*   クエリの作成 (必要な場合のみ):

    *   患者ID: 01-701-1034
        *   クエリNo.: 1
            *   臨床試験結果への影響度合い:（Minor）
            *   変数名と値:
                *   LB.LBTESTCD: TSH
                *   LB.LBORRES: 0.27
                *   LB.LBORRESU: uIU/mL
                *   LB.LBORNRLO: 0.32
                *   LB.LBORNRHI: 5
            *   医療機関への問い合わせ文面: 被験者01-701-1034は、甲状腺刺激ホルモン（TSH）の検査値が基準範囲を下回っていますが、甲状腺ホルモン剤の投与を受けていますか？ 
 また、遊離甲状腺ホルモン値は正常範囲内ですか？甲状腺機能異常を示す臨床症状や兆候は認められますか？
            *   判断理由:
                *   プロトコルでは、甲状腺機能検査値が基準範囲外でも、甲状腺ホルモン剤を服用しており、臨床的に問題がない場合は登録可能とされています。
                *   したがって、治験担当医師に確認し、甲状腺ホルモン剤の投与状況と臨床症状に関する情報を収集する必要があります。


# 01-704-1010
## Task1: Clinical Review Results
## 1. 症例サマリーの作成:

**患者ID: 01-704-1010**

*   2014年02月07日 (Day -14): Albumin 4.2 g/dL、Alkaline Phosphatase 61 U/L、Alanine Aminotransferase 9 U/L、Aspartate Aminotransferase 16 U/L、Basophils 0.07 THOU/uL、Bilirubin 1.1 mg/dL、Blood Urea Nitrogen 15 mg/dL、Calcium 9.0 mg/dL、Cholesterol 190 mg/dL、Creatine Kinase 67 U/L、Chloride 109 mEq/L、Color N、Creatinine 1.3 mg/dL、Eosinophils 0.19 THOU/uL、Gamma Glutamyl Transferase 10 U/L、Glucose 108 mg/dL、Hematocrit 51.0 %、Hemoglobin 16.8 g/dL、Potassium 4.5 mEq/L、Ketones 0、Lymphocytes 1.49 THOU/uL、MCH 32 pg、MCHC 33 g/dL、MCV 95 fL、Monocytes 0.48 THOU/uL、Sodium 144 mEq/L、pH 5.0、Phosphate 2.9 mg/dL、Platelet 191 THOU/uL、Protein 6.9 g/dL、RBC 5.30 MILL/uL、Specific Gravity 1.027、Thyrotropin 2.24 uIU/mL、Urate 5.5 mg/dL、Urobilinogen 0、Vitamin B12 620 pg/mL、Leukocytes 6.59 THOU/uL。
*   2014年02月08日 (Day -13): Medical Historyとして、ALZHEIMER'S DISEASE、VERBATIM_0257、VERBATIM_0342、VERBATIM_0472が報告された。教育レベルは14年。
*   2014年02月21日 (Day 1): ベースライン検査。
*   2014年02月27日 (Day 7): Bladder Infection発生（軽度）。
*   2014年03月05日 (Day 13): Bladder Infectionが回復。
*   2014年03月08日 (Day 16): Albumin 3.9 g/dL、Alkaline Phosphatase 64 U/L、Alanine Aminotransferase 6 U/L、Aspartate Aminotransferase 13 U/L、Basophils 0.07 THOU/uL、Bilirubin 1.1 mg/dL、Blood Urea Nitrogen 17 mg/dL、Calcium 8.8 mg/dL、Cholesterol 159 mg/dL、Creatine Kinase 43 U/L、Chloride 108 mEq/L、Color N、Creatinine 1.3 mg/dL、Eosinophils 0.11 THOU/uL、Gamma Glutamyl Transferase 14 U/L、Glucose 82 mg/dL、Hematocrit 50.0 %、Hemoglobin 15.7 g/dL、Potassium 4.0 mEq/L、Ketones 0、Lymphocytes 1.12 THOU/uL、MCH 31 pg、MCHC 32 g/dL、MCV 97 fL、Monocytes 0.37 THOU/uL、Sodium 139 mEq/L、pH 5.0、Phosphate 3.2 mg/dL、Platelet 265 THOU/uL、Protein 6.6 g/dL、RBC 5.10 MILL/uL、Specific Gravity 1.021、Urate 6.0 mg/dL、Urobilinogen 0、Leukocytes 6.59 THOU/uL。
*   2014年03月23日 (Day 31): Albumin 4.1 g/dL、Alkaline Phosphatase 66 U/L、Alanine Aminotransferase 14 U/L、Aspartate Aminotransferase 14 U/L、Basophils 0.07 THOU/uL、Bilirubin 1.2 mg/dL、Blood Urea Nitrogen 15 mg/dL、Calcium 9.1 mg/dL、Cholesterol 191 mg/dL、Creatine Kinase 41 U/L、Chloride 106 mEq/L、Color N、Creatinine 1.3 mg/dL、Eosinophils 0.19 THOU/uL、Gamma Glutamyl Transferase 12 U/L、Glucose 82 mg/dL、Hematocrit 50.0 %、Hemoglobin 15.9 g/dL、Potassium 4.1 mEq/L、Ketones 0、Lymphocytes 1.44 THOU/uL、MCH 31 pg、MCHC 32 g/dL、MCV 97 fL、Monocytes 0.33 THOU/uL、Sodium 138 mEq/L、pH 5.0、Phosphate 3.5 mg/dL、Platelet 169 THOU/uL、Protein 6.9 g/dL、RBC 5.20 MILL/uL、Specific Gravity 1.025、Urate 5.1 mg/dL、Urobilinogen 0、Leukocytes 6.34 THOU/uL。
*   2014年04月11日 (Day 50): Albumin 4.3 g/dL、Alkaline Phosphatase 64 U/L、Alanine Aminotransferase 7 U/L、Aspartate Aminotransferase 15 U/L、Basophils 0.05 THOU/uL、**Bilirubin 1.3 mg/dL (HIGH)**、Blood Urea Nitrogen 14 mg/dL、Calcium 9.2 mg/dL、Cholesterol 183 mg/dL、Creatine Kinase 53 U/L、Chloride 111 mEq/L、Color N、Creatinine 1.3 mg/dL、Eosinophils 0.13 THOU/uL、Gamma Glutamyl Transferase 12 U/L、Glucose 75 mg/dL、Hematocrit 50.0 %、Hemoglobin 16.5 g/dL、Potassium 4.3 mEq/L、Ketones 0、Lymphocytes 1.19 THOU/uL、MCH 32 pg、MCHC 33 g/dL、MCV 97 fL、Monocytes 0.39 THOU/uL、Sodium 143 mEq/L、pH 5.0、Phosphate 3.0 mg/dL、Platelet 211 THOU/uL、Protein 7.3 g/dL、RBC 5.20 MILL/uL、Urate 5.6 mg/dL、Urobilinogen 0、Leukocytes 6.50 THOU/uL。
*   2014年04月24日 (Day 63): Albumin 3.9 g/dL、Alkaline Phosphatase 56 U/L、Alanine Aminotransferase 7 U/L、Aspartate Aminotransferase 14 U/L、Basophils 0.04 THOU/uL、Bilirubin 0.9 mg/dL、Blood Urea Nitrogen 13 mg/dL、Calcium 8.6 mg/dL、Cholesterol 166 mg/dL、Creatine Kinase 56 U/L、Chloride 109 mEq/L、Creatinine 1.3 mg/dL、Eosinophils 0.12 THOU/uL、Gamma Glutamyl Transferase 10 U/L、Glucose 93 mg/dL、Hematocrit 48.0 %、Hemoglobin 15.5 g/dL、Potassium 4.3 mEq/L、Ketones 0、Lymphocytes 1.02 THOU/uL、MCH 31 pg、MCHC 32 g/dL、MCV 97 fL、Monocytes 0.38 THOU/uL、Sodium 142 mEq/L、pH 5.0、Phosphate 2.4 mg/dL、Platelet 175 THOU/uL、Protein 6.5 g/dL、RBC 5.00 MILL/uL、Specific Gravity 1.025、Urate 5.1 mg/dL、Urobilinogen 0、Leukocytes 6.37 THOU/uL。
*   2014年05月16日 (Day 85): Albumin 4.5 g/dL、Alkaline Phosphatase 62 U/L、Alanine Aminotransferase 8 U/L、Aspartate Aminotransferase 15 U/L、Basophils 0.05 THOU/uL、Bilirubin 1.1 mg/dL、Blood Urea Nitrogen 12 mg/dL、Calcium 9.0 mg/dL、Cholesterol 197 mg/dL、Creatine Kinase 59 U/L、Chloride 107 mEq/L、Creatinine 1.3 mg/dL、Eosinophils 0.12 THOU/uL、Gamma Glutamyl Transferase 12 U/L、Glucose 95 mg/dL、Hematocrit 48.0 %、Hemoglobin 15.7 g/dL、Potassium 4.4 mEq/L、Ketones 0、Lymphocytes 1.16 THOU/uL、MCH 32 pg、MCHC 33 g/dL、MCV 96 fL、Monocytes 0.35 THOU/uL、Sodium 141 mEq/L、pH 5.0、Phosphate 3.3 mg/dL、Platelet 192 THOU/uL、Protein 7.2 g/dL、RBC 5.00 MILL/uL、Specific Gravity 1.025、Urate 4.9 mg/dL、Urobilinogen 0、Leukocytes 7.04 THOU/uL。
*   2014年07月05日 (Day 135): Diarrhoea、Vomiting、Arthralgia、Contusion、Excoriation、Skin Laceration。
*   2014年07月06日 (Day 136): Diarrhoea、Vomiting、Arthralgia、Contusion、Excoriation、Skin Laceration。
*   2014年07月09日 (Day 139): Albumin 4.0 g/dL、Alkaline Phosphatase 52 U/L、Alanine Aminotransferase 12 U/L、Aspartate Aminotransferase 21 U/L、Basophils 0.07 THOU/uL、**Bilirubin 1.3 mg/dL (HIGH)**、Blood Urea Nitrogen 17 mg/dL、**Calcium 8.3 mg/dL (LOW)**、Cholesterol 151 mg/dL、Creatine Kinase 106 U/L、Chloride 112 mEq/L、Color N、Creatinine 1.5 mg/dL、Eosinophils 0.10 THOU/uL、Gamma Glutamyl Transferase 15 U/L、Glucose 77 mg/dL、Hematocrit 48.0 %、Hemoglobin 15.6 g/dL、Potassium 3.9 mEq/L、Ketones 0、Lymphocytes 1.02 THOU/uL、MCH 32 pg、MCHC 33 g/dL、MCV 98 fL、Monocytes 0.56 THOU/uL、Sodium 144 mEq/L、pH 5.0、Phosphate 3.4 mg/dL、Platelet 191 THOU/uL、Protein 6.7 g/dL、RBC 4.90 MILL/uL、Specific Gravity 1.028、Urate 6.6 mg/dL、Urobilinogen 0、Leukocytes 7.15 THOU/uL。

---

## 2. クエリの作成

**患者ID: 01-704-1010**

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   LB.LBTESTCD: BILI
        *   LB.LBNRIND: HIGH (Week 6, Week 20)
    *   **医療機関への問い合わせ文面:**
        *   Bilirubin値がWeek 6とWeek 20で基準範囲を超えて高値を示していますが、臨床的に特記すべき事項はありますか？肝機能障害を示唆する他の検査値に異常値はありますか？
    *   **判断理由:**
        *   Bilirubin高値は肝機能障害を示唆する可能性があり、安全性上の懸念となるため。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   LB.LBTESTCD: CA
        *   LB.LBNRIND: LOW (Week 20)
    *   **医療機関への問い合わせ文面:**
        *   カルシウム値がWeek 20で基準範囲を下回っていますが、臨床的に特記すべき事項はありますか？
    *   **判断理由:**
        *   カルシウム低値は、神経伝達や骨代謝に影響を与える可能性があり、安全性上の懸念となるため。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   AE.AETERM: DIARRHOEA, VOMITING, ARTHRALGIA, CONTUSION, EXCORIATION, SKIN LACERATION
        *   AE.AESTDTC: 2014-07-05, 2014-07-06
        *   AE.AEOUT: NOT RECOVERED/NOT RESOLVED, RECOVERED/RESOLVED
    *   **医療機関への問い合わせ文面:**
        *  2014年7月5日から7月6日にかけて、DIARRHOEA、VOMITING、ARTHRALGIA、CONTUSION、EXCORIATION、SKIN LACERATIONといった複数の有害事象が発現していますが、それぞれの事象について、AEOUT（転帰）がRECOVERED/RESOLVEDまたはNOT RECOVERED/NOT RESOLVEDとなっています。
        これらの有害事象は、開始日・終了日が同じであることから、何らかの単一の要因によるものでしょうか？
        また、それぞれの事象の重症度と、治験薬との因果関係について評価をお願いします。
    *   **判断理由:**
        *   複数の有害事象が短期間に集中して発生しているため、その関連性と治験薬との関連性を確認する必要がある。

*   **クエリNo.: 4**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   DS.DSTERM: PATIENT IS MOVING
        *   DS.DSDECOD: WITHDRAWAL BY SUBJECT
        *   DS.DSDTC: 2014-07-09
        *   AE.AETERM: ARTHRALGIA, CONTUSION, EXCORIATION, SKIN LACERATION
        *   AE.AESTDTC: 2014-07-06
    *   **医療機関への問い合わせ文面:**
        *  2014年7月9日に「PATIENT IS MOVING (WITHDRAWAL BY SUBJECT)」という治験中止が報告されています。
        治験中止の3日前に、ARTHRALGIA、CONTUSION、EXCORIATION、SKIN LACERATIONといった複数の有害事象が発現していますが、治験中止の理由との関連について評価をお願いします。
        また、患者が移動する理由の詳細について教えてください。
    *   **判断理由:**
        *  治験中止と有害事象発現のタイミングが近いため、関連性を確認する必要がある。

## Task2: DM Review Results
```markdown
 全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMDTC, CM.CMSTDTC, CM.CMENDTCにおける日付データの整合性

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (1行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 2
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (12行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 3
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (27行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 4
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (33行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 5
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (39行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 6
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (45行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。
* 問題No.: 7
    * 変数名と値: CM.CMDTC = 2014-02-08, CM.CMSTDTC = 2012, CM.CMENDTC = null (51行目)
    * 矛盾の内容: CMドメインにおいて、CMDTC（収集日）がCMSTDTC（Medication開始日）より未来の日付になっている。Medicationの開始日が未来になることは通常ありえないため、データの矛盾が考えられる。
    * 問題点の原因（推測）: データ入力エラー、日付記録時の誤り
    * 対応策（提案）: 
        1.  CMDTC、CMSTDTCそれぞれのCRF上の値を確認し、転記ミスがないか確認する。
        2.  CMDTCが誤っている場合、正しい日付に修正する。
        3.  CMSTDTCが誤っている場合、正しい日付に修正する。

* 問題No.: 8
    * 変数名と値: USUBJID = 01-704-1010, AE.AETERM = DIABETES MELLITUS, CM.CMTRT = CIPRO
    * 矛盾の内容: USUBJID=01-704-1010 の被験者は、AEドメインでDIABETES MELLITUSが報告されているが、CMドメインでは、糖尿病治療薬の投与が確認できない。
    * 問題点の原因（推測）: CMデータにConcomitant Medicationsの入力漏れがあるか、DIABETES MELLITUSがMedical Historyに記録されているにもかかわらず、現在治療を受けていない可能性がある。
    * 対応策（提案）: 
        1.  CMドメインにConcomitant Medicationsの入力漏れがないか確認する。
        2.  Medical History（MHドメイン）にDIABETES MELLITUSの記録があるか確認する。
        3.  DIABETES MELLITUSがMedical Historyに記録されているにもかかわらず、現在治療を受けていない場合、その理由をCRFで確認する。

* 問題No.: 9
    * 変数名と値: DM.RFENDTC = "2014-07-09", DS.DSSTDTC = "2014-07-09" , DS.DSTERM = "PATIENT IS MOVING"
    * 矛盾の内容: DMドメインのRFENDTC（Subject Reference End Date/Time）とDSドメインのDSSTDTC（Start Date/Time of Disposition Event）が同じ日付であり、DSTERM（Reported Term for the Disposition Event）が「PATIENT IS MOVING（患者が引っ越し）」となっている。しかし、TSドメインの定義ではTrial Lengthが26週（182日）であり、DMドメインのRFSTDTC（Subject Reference Start Date/Time）が"2014-02-21"であることから、試験期間を最後まで完了していないことがわかる。
    * 問題点の原因（推測）: 患者の引っ越しによる試験からの早期離脱。
    * 対応策（提案）: 特に対応は不要。ただし、DS.DSTERM の内容が本当に引っ越しによるものか確認。

クエリの作成:
* 患者ID: 01-704-1010
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMTRT = CIPRO
        * 医療機関への問い合わせ文面:
            01-704-1010 の被験者は、DIABETES MELLITUSの既往歴がありますが、現在糖尿病の治療を受けていますでしょうか？もし治療を受けている場合、投与されている薬剤名と投与開始日、投与量についてご教示ください。
        * 判断理由: 糖尿病治療薬の投与の有無は、血糖値などの臨床検査値に影響を与え、試験結果の解釈に影響を与える可能性があるため。

```
## Task3: Protocol Deviation Review Results
患者ID: 01-704-1010

*   **逸脱No.:** 1
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMDTC: 2014-02-08, CM.CMSTDTC: 2012
    *   **逸脱内容:** 
        *   CM.CMSTDTCの値が2012となっており、CM.CMDTC（2014-02-08）より過去の日付になっています。
    *   **プロトコル該当箇所:** 特に指定なし (SDTMIG 一般原則)
    *   **判断理由:**
        *   CMSTDTCはCMドメインにおける薬剤の開始日ですが、データ収集日（CMDTC）より未来であるべきです。データ収集が行われていない時点での服薬開始はあり得ないため、矛盾が発生しています。

*   **逸脱No.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DS.DSTERM: PATIENT IS MOVING, DS.DSDECOD: WITHDRAWAL BY SUBJECT, DSDTC: 2014-07-09, EX.EXENDTC: 2014-07-08
    *   **逸脱内容:**
        *   DS.DSDTCとDS.DSSTDTC（2014-07-09）が、EX.EXENDTC（2014-07-08）より後の日付になっています。
        *   被験者は試験薬を最終投与した日（EXENDTC）より後に、試験から脱落することは通常ありえません。
    *   **プロトコル該当箇所:** 特に指定なし (SDTMIG 一般原則)
    *   **判断理由:**
        *   一般的に、患者の試験薬投与終了日よりも後に、試験から脱落することは考えにくいです。
        *   データ入力または転記の誤りの可能性があります。

*   **逸脱No.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.VISIT: UNSCHEDULED 9.2, LB.VISITDY: null
    *   **逸脱内容:**
        *   計画されたVISITDY（Planned Study Day of Visit）がNULLになっています。
    *   **プロトコル該当箇所:** 特に指定なし
    *   **判断理由:**
        *   予定外の検査であるため VISITDY が NULL であることは許容されますが、可能であれば治験責任医師に確認し、VISITDYを特定することを推奨します。

*   **逸脱No.:** 4
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM: ALZHEIMER'S DISEASE, MH.MHSTDTC: 2006-01-02
    *   **逸脱内容:**
        *  Medical Historyにアルツハイマー病（ALZHEIMER'S DISEASE）の既往歴が登録されています。
        *  TI.IETESTのINCL02（アルツハイマー病の診断基準）とEXCL12（重篤な神経系の疾患）との整合性に矛盾が生じる可能性があります。
    *   **プロトコル該当箇所:**
        *   3.4.2.1 Inclusion Criteria [2]
        *   3.4.2.2 Exclusion Criteria [12]
    *   **判断理由:**
        *  DMドメインでアルツハイマー病と診断された被験者が、MHドメインでもアルツハイマー病の既往歴を持つことは、選択基準と除外基準に抵触する可能性があります。
        *  プロトコルで定められた選択基準、除外基準との整合性を確認する必要があります。

*   **逸脱No.:** 5
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** AE.AETERM: DIABETES MELLITUS, AESTDTC: 2014-02-27, AEENDTC: 2014-03-06
    *   **逸脱内容:**
        *   DIABETES MELLITUS（糖尿病）はMedical Historyに記載すべき内容ですが、Adverse Eventとして報告されています。
    *   **プロトコル該当箇所:** 特に指定なし
    *   **判断理由:**
        *   DIABETES MELLITUS（糖尿病）は通常、Adverse Eventではなく、Medical Historyとして記録されるべきです。
        *   MedDRA辞書との整合性、また、有害事象と判断した理由を確認する必要があります。

*   **逸脱No.:** 6
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSTEST: Height, VSORRES: 070.0, VSORRESU: IN, VSSTRESC: 177.8, VSSTRESU: cm
    *   **逸脱内容:**
        *   身長が「070.0 IN (インチ)」と記録されています。 1インチは約2.54cmなので、70インチは約177.8cmとなり、VSSTRESCに矛盾はありません。しかし、80歳の高齢者の身長として70インチは非常に高い可能性があります。
    *   **プロトコル該当箇所:** 特になし
    *   **判断理由:**
        *   記録された身長が医学的に妥当であるか、単位の誤りがないか確認するために、クエリを発行することを推奨します。

*   **逸脱No.:** 7
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD: BILI, LBDTC: 2014-04-11T09:45, LBNRIND: HIGH, LBORNRHI: 1.2, LBORRES: 1.3
    *   **逸脱内容:**
        *   Bilirubin値が基準範囲上限を超えています。
        *   LBTMSHI値が定義されていません。
    *   **プロトコル該当箇所:** 特になし
    *   **判断理由:**
        *   Bilirubin値が基準範囲上限を超えています。
        *   ただし、LBドメインにLBTMSHI(LAB RESULT/UPPER LIMIT OF NORMAL)がありません。SUPPLBドメインには定義されています。
        *   SUPPLB.QVALをLBドメインのLBSTNRHIの値と比較してHigh/Lowの判定が正しく行われているか確認する必要があります。

*   **逸脱No.:** 8
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DS.DSTERM: PATIENT IS MOVING, DS.DSDECOD: WITHDRAWAL BY SUBJECT, LB.VISITNUM: 11
    *   **逸脱内容:**
        *   SubjectがWEEK20(VISITNUM=11)で試験を中止している。
        *   WBCがWEEK20(VISITNUM=11)に測定されている。
    *   **プロトコル該当箇所:** 特になし
    *   **判断理由:**
        *   DSドメインのDSDTC(Date/Time of Collection)に2014-07-09が設定されており、この日WEEK20のデータが収集されているのでFinal lab visitも同日に行われた可能性があります。
        *   DSDTCとLB.LBDTCが同じ日付であることから、整合性がとれていると考えられます。

**クエリの作成 (必要な場合のみ):**

*   **患者ID:** 01-704-1010
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** MH.MHTERM: ALZHEIMER'S DISEASE, MH.MHSTDTC: 2006-01-02
        *   **医療機関への問い合わせ文面:**
            *   Medical Historyにアルツハイマー病（ALZHEIMER'S DISEASE）の既往歴が登録されていますが、本試験ではInclusion criteriaで「Diagnosis of probable AD as defined by NINCDS and the ADRDA guidelines」と定められており、Exclusion criteriaで「Diagnosis of serious neurological conditions」が除外されています。
            *   カルテを確認し、Medical HistoryのALZHEIMER'S DISEASEは今回の治験における診断と同一のものか、あるいは過去の診断で現在は除外診断となっているか確認してください。
            *   もしMedical HistoryのALZHEIMER'S DISEASEが今回の治験における診断と異なる場合は、その旨を回答ください。
        *   **判断理由:**
            *   プロトコルで定められた選択基準、除外基準との整合性を確認する必要があります。

*   **患者ID:** 01-704-1010
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** VS.VSTEST: Height, VSORRES: 070.0, VSORRESU: IN, VSSTRESC: 177.8, VSSTRESU: cm
        *   **医療機関への問い合わせ文面:**
            *   患者ID 01-704-1010の身長データについて、CRFまたは原資料を確認し、VSORRESの値（070.0）の単位がインチ（IN）で正しいか確認してください。
            *   もし単位が誤っている場合は、正しい身長と単位を報告してください。
        *   **判断理由:**
            *   記録された身長が医学的に妥当であるか、単位の誤りがないか確認する必要があるため。

*   **患者ID:** 01-704-1010
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM: DIABETES MELLITUS, AESTDTC: 2014-02-27, AEENDTC: 2014-03-06
        *   **医療機関への問い合わせ文面:**
            *   患者ID 01-704-1010にDIABETES MELLITUS（糖尿病）がAdverse Eventとして報告されていますが、有害事象と判断した根拠についてカルテを確認し詳細を教えてください。
        *   **判断理由:**
            *  DIABETES MELLITUS（糖尿病）は通常、既往歴として記録されるべき情報であるため。



# 01-701-1111
## Task1: Clinical Review Results
```markdown
患者ID: 01-701-1111
    * 2012年08月25日 (Day -13): スクリーニング1回目。Albumin 3.6 g/dL、Alkaline Phosphatase 64 U/L、Alanine Aminotransferase 23 U/L、Aspartate Aminotransferase 28 U/L、Basophils 0.04 THOU/uL、Bilirubin 0.4 mg/dL、Blood Urea Nitrogen 7 mg/dL、Calcium 8.9 mg/dL、Cholesterol 221 mg/dL、Creatine Kinase 60 U/L、Chloride 105 mEq/L、Creatinine 0.9 mg/dL、Eosinophils 0.04 THOU/uL、Gamma Glutamyl Transferase 10 U/L、Glucose 96 mg/dL、Hematocrit 37.0 %、Hemoglobin 12.0 g/dL、Potassium 3.9 mEq/L、Ketones 0 NO UNITS、Lymphocytes 2.08 THOU/uL、Ery. Mean Corpuscular Hemoglobin 32 pg、Ery. Mean Corpuscular HGB Concentration 33 g/dL、Ery. Mean Corpuscular Volume 97 fL、Monocytes 0.37 THOU/uL、Sodium 137 mEq/L、pH 6.0 NO UNITS、Phosphate 3.1 mg/dL、Platelet 255 THOU/uL、Protein 7.2 g/dL、Erythrocytes 3.80 MILL/uL (LOW)、Specific Gravity 1.007 NO UNITS、Thyrotropin 1.25 uIU/mL、Urate 3.2 mg/dL、Urobilinogen 0 NO UNITS、Vitamin B12 527 pg/mL、Leukocytes 4.59 THOU/uL。
    * 2012年09月02日 (Day -5): 紅斑（軽度）発現。
    * 2012年09月05日 (Day -2): 紅斑（軽度）、瘙痒症（軽度）発現。
    * 2012年09月07日 (Day 1): キサンメリン54mg投与開始。
    * 2012年09月13日 (Day 7): 関節痛（中等度）、蜂巣炎（中等度）発現。
    * 2012年09月17日 (Day 11): Week2, Erythrocytes 3.70 MILL/uL (LOW), Ery. Mean Corpuscular Volume 101 fL (HIGH), Specific Gravity 1.004 NO UNITS (LOW), Anisocytes 1 NO UNITS (ABNORMAL)。有害事象として関節痛、蜂巣炎、紅斑、排尿切迫。
    * 2013年02月22日 (Day 169): 最終回収訪問。

---

患者ID: 01-701-1111
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値:
            * LB.LBDTC: 2012-09-17T11:48
            * LB.LBY: 11
            * LB.LBTESTCD: ANISO
            * LB.LBORRES: 1
            * LB.LBNRIND: ABNORMAL
            * AE.AETERM: ARTHRALGIA
            * AE.AESTDTC: 2012-09-13
            * AE.AEENDTC: (NULL)
            * AE.AESTDY: 7
        * 医療機関への問い合わせ文面: AnisocytesがABNORMAL (2012-09-17)ですが、関節痛(2012-09-13)との関連はありますか？
        * 判断理由: 試験薬投与開始後にAnisocytesがABNORMALとなり、関節痛と発現日が近接しているため、因果関係を確認する必要があると考えます。
```

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMENDTC, AE.AESTDTC, AE.AEENDTC, QS.QSORRES, QS.QSSTRESN, VS.VSTPT, VS.VSTPTNUM, DAITM25, DAITM26, DAITM27, DAITM28, DAITM29

問題点:

*   問題No.1:
    *   変数名と値: CM.CMENDTC = "", CM.CMSTDTC = "2012-07-08"
    *   矛盾の内容: 複数のConcomitant Medications (CMTRT = 'KEFLEX', 'LISINOPRIL', 'MOTRIN')において、CMENDTCが欠損している。CMSTDTCが提供されているにもかかわらずCMENDTCが欠損していることは、データ収集または記録の際に問題があった可能性を示唆する。
    *   問題点の原因（推測）: データ入力エラー、またはCMENDTCが必須項目ではなかったために未入力のままになっている可能性がある。
    *   対応策（提案）: 
        1.  医療機関に問い合わせを行い、CMENDTCの値を確認する。
        2.  CMENDTCが欠損している理由を特定し、データ収集手順を見直す。
        3.  必要に応じて、Define.xmlを更新し、CMENDTCを必須項目として定義するか、欠損値の理由を明確にする。
*   問題No.2:
    *   変数名と値: AE.AESTDTC = "2012-09-02", AE.AEENDTC = ""
    *   矛盾の内容: ARTHRALGIA(関節痛), CELLULITIS(蜂窩織炎), LOCALIZED INFECTION(局所感染), MICTURITION URGENCY(頻尿)についてAEENDTCがNULLになっている。AESTDTCが提供されているにもかかわらずAEENDTCが欠損していることは、データ収集または記録の際に問題があった可能性を示唆する。
    *   問題点の原因（推測）: データ入力エラー、またはAEENDTCが必須項目ではなかったために未入力のままになっている可能性がある。
    *   対応策（提案）: 
        1.  医療機関に問い合わせを行い、AEENDTCの値を確認する。
        2.  AEENDTCが欠損している理由を特定し、データ収集手順を見直す。
        3.  必要に応じて、Define.xmlを更新し、AEENDTCを必須項目として定義するか、欠損値の理由を明確にする。
*   問題No.3:
    *   変数名と値: QS.QSTESTCD = "DAITM25", QSORRES = "NA"(WEEK2), "N"(BASELINE), "Y"(RETRIEVAL), QSTEST = "UNDERTAKE TO GO OUT"
    *   矛盾の内容: DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の質問項目DAITM25（外出の試み）の結果が一貫していない。
        *   ベースライン: N (いいえ)
        *   WEEK 2: NA (該当なし)
        *   RETRIEVAL: Y (はい)
        ベースラインで「いいえ」と回答しているにもかかわらず、WEEK 2で「該当なし」となっている。これは、データ収集または記録の際に問題があった可能性を示唆する。
    *   問題点の原因（推測）:
        *   データ入力エラー
        *   患者の状態変化: WEEK 2の時点では患者が外出を試みることができなかった何らかの理由が存在した可能性がある。
        *   質問の解釈の違い: 介護者が質問の意図を誤解している可能性がある。
    *   対応策（提案）:
        1.  医療機関に問い合わせを行い、DAITM25の回答が「該当なし」と記録された理由を確認する。
        2.  患者の状態変化に関する情報を収集し、記録する。
        3.  DAITM25に対する質問の意図を明確化し、介護者への説明を徹底する。
*   問題No.4:
    *   変数名と値: QS.QSTESTCD = "DAITM27", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL), QSTEST = "GO OUT AND REACH A FAMILIAR DESTINATION"
    *   矛盾の内容: DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の質問項目DAITM27（安全に交通機関を利用できるか）の結果が一貫していない。
        *   ベースライン: NA (該当なし)
        *   WEEK 2: NA (該当なし)
        *   RETRIEVAL: Y (はい)
    *   問題点の原因（推測）:
        *   データ入力エラー
        *   患者の状態変化: ベースラインとWEEK 2の時点では患者が交通機関を利用する機会がなかった可能性がある。
        *   質問の解釈の違い: 介護者が質問の意図を誤解している可能性がある。
    *   対応策（提案）:
        1.  医療機関に問い合わせを行い、DAITM27の回答が「該当なし」と記録された理由を確認する。
        2.  患者の状態変化に関する情報を収集し、記録する。
        3.  DAITM27に対する質問の意図を明確化し、介護者への説明を徹底する。
*   問題No.5:
    *   変数名と値: QS.QSTESTCD = "DAITM26", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL), QSTEST = "ADEQUATELY ORGANIZE AN OUTING"
    *   矛盾の内容: DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の質問項目DAITM26（外出の計画を立てられるか）の結果が一貫していない。
        *   ベースライン: Y (はい)
        *   WEEK 2: NA (該当なし)
        *   RETRIEVAL: Y (はい)
    *   問題点の原因（推測）:
        *   データ入力エラー
        *   患者の状態変化: WEEK 2の時点では患者が外出の計画を立てることができなかった何らかの理由が存在した可能性がある。
        *   質問の解釈の違い: 介護者が質問の意図を誤解している可能性がある。
    *   対応策（提案）:
        1.  医療機関に問い合わせを行い、DAITM26の回答が「該当なし」と記録された理由を確認する。
        2.  患者の状態変化に関する情報を収集し、記録する。
        3.  DAITM26に対する質問の意図を明確化し、介護者への説明を徹底する。
*   問題No.6:
    *   変数名と値: QS.QSTESTCD = "DAITM28", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL), QSTEST = "SAFELY TAKE CAR, BUS, TAXI"
    *   矛盾の内容: DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の質問項目DAITM28（安全に交通機関を利用できるか）の結果が一貫していない。
        *   ベースライン: NA (該当なし)
        *   WEEK 2: NA (該当なし)
        *   RETRIEVAL: Y (はい)
    *   問題点の原因（推測）:
        *   データ入力エラー
        *   患者の状態変化: ベースラインとWEEK 2の時点では患者が交通機関を利用する機会がなかった可能性がある。
        *   質問の解釈の違い: 介護者が質問の意図を誤解している可能性がある。
    *   対応策（提案）:
        1.  医療機関に問い合わせを行い、DAITM28の回答が「該当なし」と記録された理由を確認する。
        2.  患者の状態変化に関する情報を収集し、記録する。
        3.  DAITM28に対する質問の意図を明確化し、介護者への説明を徹底する。
*   問題No.7:
    *   変数名と値: QS.QSTESTCD = "DAITM29", QSORRES = "NA"(WEEK2), "N"(BASELINE), "Y"(RETRIEVAL), QSTEST = "RETURN FROM THE STORE"
    *   矛盾の内容: DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の質問項目DAITM29（買い物から帰ってこられるか）の結果が一貫していない。
        *   ベースライン: N (いいえ)
        *   WEEK 2: NA (該当なし)
        *   RETRIEVAL: Y (はい)
    *   問題点の原因（推測）:
        *   データ入力エラー
        *   患者の状態変化: WEEK 2の時点では患者が買い物から帰ってくることができなかった何らかの理由が存在した可能性がある。
        *   質問の解釈の違い: 介護者が質問の意図を誤解している可能性がある。
    *   対応策（提案）:
        1.  医療機関に問い合わせを行い、DAITM29の回答が「該当なし」と記録された理由を確認する。
        2.  患者の状態変化に関する情報を収集し、記録する。
        3.  DAITM29に対する質問の意図を明確化し、介護者への説明を徹底する。
*   問題No.8:
    *   変数名と値: VS.VSTPT = "", VS.VSTPTNUM = null
    *   矛盾の内容: バイタルサイン(VS)のデータにおいて、VSTPT（Planned Time Point Name）と VSTPTNUM（Planned Time Point Number）の値が一部欠損している。これらの変数は、バイタルサイン測定のタイミングを特定するために重要である。
    *   問題点の原因（推測）: データ入力時のエラー、またはデータ収集プロセスの不備が考えられる。Define.xmlでは必須項目ではないため、未入力のままになっている可能性がある。
    *   対応策（提案）:
        1.  データが欠損している理由を調査する。
        2.  可能な限り、オリジナルデータソース（CRFなど）を参照して欠損データを補完する。
        3.  もしデータ補完が不可能であれば、欠損データの理由を特定し、今後のデータ収集プロセスの改善を検討する。
        4.  必要に応じて、Define.xmlを修正しVSTPT、VSTPTNUMを必須項目とする。
*   問題No.9:
    *   変数名と値: RELREC.IDVARVAL = " 7", RELREC.RELID = "01-701-1111-E16", AE.AESEQ= 7, AE.AETERM= "ARTHRALGIA"
    *   矛盾の内容: USUBJID:01-701-1111のRELRECレコードにおいて、AEドメインとの関連が定義されている。IDVARVALは"   7"(スペースを含む)となっている。AEドメインのAESEQの値は数値型であり、0埋めは不要と思われる。
    *   問題点の原因（推測）: RELREC.IDVARVALの生成ロジックに問題がある可能性がある。
    *   対応策（提案）:
        1.  RELREC.IDVARVALの生成ロジックを確認し、不要なスペースを削除する。
        2.  RELRECデータセット全体で同様の問題がないか確認する。

クエリの作成:

*   患者ID: 01-701-1111
    *   クエリNo.1:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMENDTC = "", CM.CMSTDTC = "2012-07-08"
        *   医療機関への問い合わせ文面:
            *   Sequence Numberが6,12,19,25,31,37のKEFLEXについて、投与終了日(CMENDTC)が未記入ですが、投与を中止した日をご教示ください。
            *   Sequence Numberが4,10,17,23,29,35のLISINOPRILについて、投与終了日(CMENDTC)が未記入ですが、投与を中止した日をご教示ください。
            *   Sequence Numberが5,11,18,24,30,36のMOTRINについて、投与終了日(CMENDTC)が未記入ですが、投与を中止した日をご教示ください。
        *   判断理由: 併用薬の使用期間は、治験薬の効果や有害事象の評価に影響を与える重要な情報である。CMENDTCが欠損している場合、併用薬の影響を正確に評価することができない。
    *   クエリNo.2:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC = "2012-09-13", AE.AEENDTC = ""
        *   医療機関への問い合わせ文面:
            *   Sequence Numberが7のARTHRALGIA(関節痛)について、有害事象の終了日(AEENDTC)が未記入ですが、いつ症状が消失しましたか？
        *   判断理由: 有害事象の継続期間は、治験薬の安全性を評価する上で重要な情報である。
    *   クエリNo.3:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC = "2012-09-13", AE.AEENDTC = ""
        *   医療機関への問い合わせ文面:
            *   Sequence Numberが8のCELLULITIS(蜂窩織炎)について、有害事象の終了日(AEENDTC)が未記入ですが、いつ症状が消失しましたか？
        *   判断理由: 有害事象の継続期間は、治験薬の安全性を評価する上で重要な情報である。
    *   クエリNo.4:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC = "2012-07-08", AE.AEENDTC = ""
        *   医療機関への問い合わせ文面:
            *   Sequence Numberが3のLOCALISED INFECTION(局所感染)について、有害事象の終了日(AEENDTC)が未記入ですが、いつ症状が消失しましたか？
        *   判断理由: 有害事象の継続期間は、治験薬の安全性を評価する上で重要な情報である。
    *   クエリNo.5:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC = "2012-09-07", AE.AEENDTC = ""
        *   医療機関への問い合わせ文面:
            *   Sequence Numberが6のMICTURITION URGENCY(頻尿)について、有害事象の終了日(AEENDTC)が未記入ですが、いつ症状が消失しましたか？
        *   判断理由: 有害事象の継続期間は、治験薬の安全性を評価する上で重要な情報である。
    *   クエリNo.6:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.QSTESTCD = "DAITM25", QSORRES = "NA"(WEEK2), "N"(BASELINE), "Y"(RETRIEVAL)
        *   医療機関への問い合わせ文面:
            *   DADの質問項目DAITM25（外出の試み）について、ベースラインで「いいえ」と回答しているにもかかわらず、WEEK 2で「該当なし」と回答されている理由をご教示ください。
        *   判断理由: DADは認知機能評価の重要な指標であり、回答の不整合は評価に影響を与える可能性があるため。
    *   クエリNo.7:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.QSTESTCD = "DAITM27", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL)
        *   医療機関への問い合わせ文面:
            *   DADの質問項目DAITM27（安全に交通機関を利用できるか）について、WEEK 2で「該当なし」と回答されている理由をご教示ください。
        *   判断理由: DADは認知機能評価の重要な指標であり、回答の不整合は評価に影響を与える可能性があるため。
    *   クエリNo.8:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.QSTESTCD = "DAITM26", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL)
        *   医療機関への問い合わせ文面:
            *   DADの質問項目DAITM26（外出の計画を立てられるか）について、WEEK 2で「該当なし」と回答されている理由をご教示ください。
        *   判断理由: DADは認知機能評価の重要な指標であり、回答の不整合は評価に影響を与える可能性があるため。
    *   クエリNo.9:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.QSTESTCD = "DAITM28", QSORRES = "NA"(WEEK2), "Y"(BASELINE), "Y"(RETRIEVAL)
        *   医療機関への問い合わせ文面:
            *   DADの質問項目DAITM28（安全に交通機関を利用できるか）について、WEEK 2で「該当なし」と回答されている理由をご教示ください。
        *   判断理由: DADは認知機能評価の重要な指標であり、回答の不整合は評価に影響を与える可能性があるため。
    *   クエリNo.10:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.QSTESTCD = "DAITM29", QSORRES = "NA"(WEEK2), "N"(BASELINE), "Y"(RETRIEVAL)
        *   医療機関への問い合わせ文面:
            *    DADの質問項目DAITM29（買い物から帰ってこられるか）について、WEEK 2で「該当なし」と回答されている理由をご教示ください。
        *   判断理由: DADは認知機能評価の重要な指標であり、回答の不整合は評価に影響を与える可能性があるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1111

*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC=2012-08-25, CM.CMENDTC=2006
    *   逸脱内容: 併用薬LisinoprilのCMENDTCがCMSTDTCより過去の日付になっている。
    *   プロトコル該当箇所: データ整合性、データの矛盾
    *   判断理由: CMENDTCはCMSTDTCより後の日付になるはず。

*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=31, LB.LBORRES=3.80, LB.LBORNRLO=3.9
    *   逸脱内容: スクリーニング1回目のRBC(Erythrocytes)が基準値範囲外(LOW)
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria 27b
    *   判断理由: 選択基準 TI.EXCL27 に「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」とある。

*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=69, LB.LBORRES=3.70, LB.LBORNRLO=3.9
    *   逸脱内容: 4週目のRBC(Erythrocytes)が基準値範囲外(LOW)
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria 27b
    *   判断理由: 選択基準 TI.EXCL27 に「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」とある。

*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=70, LB.LBORRES=1.004, LB.LBORNRLO=1.006
    *   逸脱内容: 4週目のSPGRAV(Specific Gravity)が基準値範囲外(LOW)
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria 27b
    *   判断理由: 選択基準 TI.EXCL27 に「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」とある。

*   逸脱No.: 5
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: QS.QSTESTCD=DAITM25, QSORRES=NA
    *   逸脱内容: DAD質問項目25の回答に"NA"が入力されている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures d) Disability Assessment for Dementia (DAD):
    *   判断理由: DAD質問項目25への回答は、実施されている場合、"Y"または"N"のいずれかであるべき。

*   逸脱No.: 6
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: QS.QSTESTCD=DAITM26, QSORRES=NA
    *   逸脱内容: DAD質問項目26の回答に"NA"が入力されている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures d) Disability Assessment for Dementia (DAD):
    *   判断理由: DAD質問項目26への回答は、実施されている場合、"Y"または"N"のいずれかであるべき。

*   逸脱No.: 7
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: QS.QSTESTCD=DAITM27, QSORRES=NA
    *   逸脱内容: DAD質問項目27の回答に"NA"が入力されている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures d) Disability Assessment for Dementia (DAD):
    *   判断理由: DAD質問項目27への回答は、実施されている場合、"Y"または"N"のいずれかであるべき。

*   逸脱No.: 8
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: QS.QSTESTCD=DAITM28, QSORRES=NA
    *   逸脱内容: DAD質問項目28の回答に"NA"が入力されている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures d) Disability Assessment for Dementia (DAD):
    *   判断理由: DAD質問項目28への回答は、実施されている場合、"Y"または"N"のいずれかであるべき。

*   逸脱No.: 9
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: QS.QSTESTCD=DAITM29, QSORRES=NA
    *   逸脱内容: DAD質問項目29の回答に"NA"が入力されている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures d) Disability Assessment for Dementia (DAD):
    *   判断理由: DAD質問項目29への回答は、実施されている場合、"Y"または"N"のいずれかであるべき。
---
患者ID: 01-701-1111
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMENDTC
    *   医療機関への問い合わせ文面: Lisinoprilの最終服用日（CMENDTC）が2006年となっていますが、これは正しくありません。正しい年月日を教えてください。
    *   判断理由: データの矛盾を解消し、正確な併用薬情報を把握するため。

*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=31, LB.LBORRES=3.80
    *   医療機関への問い合わせ文面: スクリーニング1回目のRBC(Erythrocytes)が基準値範囲外(LOW)ですが、TI.EXCL27の除外基準に抵触しない理由についてご説明ください。
    *   判断理由: 除外基準に抵触するかどうかを確認し、データの正確性を担保するため。

*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=69, LB.LBORRES=3.70
    *   医療機関への問い合わせ文面: 4週目のRBC(Erythrocytes)が基準値範囲外(LOW)ですが、TI.EXCL27の除外基準に抵触しない理由についてご説明ください。
    *   判断理由: 除外基準に抵触するかどうかを確認し、データの正確性を担保するため。

*   クエリNo.: 4
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBSEQ=70, LB.LBORRES=1.004
    *   医療機関への問い合わせ文面: 4週目のSPGRAV(Specific Gravity)が基準値範囲外(LOW)ですが、TI.EXCL27の除外基準に抵触しない理由についてご説明ください。
    *   判断理由: 除外基準に抵触するかどうかを確認し、データ

# 01-701-1153
## Task1: Clinical Review Results
はい、承知いたしました。それでは、臨床試験データのレビューとクエリ作成を行います。

## 1. 症例サマリーの作成

**患者ID:** 01-701-1153

*   2013年09月06日 (Day -17): スクリーニング1回目の検査で、尿比重が1.003と低い (LBORNRHI: 1.03, LBORNRLO: 1.006)。
*   2013年12月16日 (Day 85): Week12の検査で、尿中ケトン体が1+と異常値を示す。
*   2013年10月13日 (Day 21): 有害事象として食欲亢進が発現。
*   2013年11月18日 (Day 57): 食欲亢進のため、治験薬が投与中止となるも、有害事象は回復せず。
*   ADCS評価において、Week8からWeek24にかけて、object naming, attention/visual search task, maze solution, spoken language ability, comprehension of spoken language などの項目でスコアが悪化している。Disability Assessment for Dementia (DAD) においては、洗体、適切な服の選択、排泄、調理、電話、外出、金銭管理など、多くの項目で自立度が低下している。NPI-Xにおいては、妄想の頻度・重症度、不耐性、夜間行動において悪化が認められる。

---

## 2. クエリの作成

*   **患者ID:** 01-701-1153
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:**
            *   AE.AEACN = "DRUG WITHDRAWN" (2013-11-18)
            *   AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" (2013-11-18)
        *   **医療機関への問い合わせ文面:**
        2013年11月18日に治験薬が投与中止となっていますが、有害事象（食欲亢進）の転帰が「未回復」のままとなっています。有害事象はその後回復しましたか？　最終観察日（2014年4月1日）までの転帰をご教示ください。
        *   **判断理由:**
        治験薬中止後も有害事象が継続していた場合、治験薬との因果関係の評価に影響を及ぼす可能性があります。

    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   LB.SPGRAV (Specific Gravity) = 1.003 (2013-09-06)
            *   LB.LBNRIND = LOW (2013-09-06)
        *   **医療機関への問い合わせ文面:**
        2013年9月6日の尿検査で尿比重が1.003と低い値を示していますが、臨床的に問題となる所見は見られましたか？
        *   **判断理由:**
        尿比重が低い原因を確認し、臨床的な意義を判断する必要があると考えられます。

    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   QS.NPITM07F (APATHY/INDIFFERENCE FREQUENCY)
            *   QS.NPITM07V (APATHY/INDIFFERENCE SEVERITY)
            *   QS.NPITM07D (APATHY/INDIFFERENCE DISTRESS)
        *   **医療機関への問い合わせ文面:**
        NPI-Xの無関心に関する評価において、Week16で項目への該当がみられなくなりました。該当しなくなった理由をご教示ください。
        *   **判断理由:**
        NPI-Xは介護者の主観的な評価であるため、評価が変動する理由を確認する必要があると考えられます。

    *   **クエリNo.: 4**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   DAITM20 (PREPARE OR COOK A LIGHT MEAL OR A SNACK)
        *   **医療機関への問い合わせ文面:**
        DADの調理に関する評価において、Week8のQVALがNA (96) となっています。N/Aと評価した理由をご教示ください。
        *   **判断理由:**
        DADは介護者の主観的な評価であるため、評価がNAとなった理由を確認する必要があると考えられます。


## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTCとCM.CMDTCの整合性、MH.MHSTDTCの欠損、LB.LBDTCとSV.SVSTDTCの整合性

問題点:

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC = "2011"、CM.CMDTC = "2013-09-06"
    *   **矛盾の内容:** USUBJIDが"01-701-1153"のCMドメインにおいて、CMSTDTC（投薬開始日）が2011年となっているにもかかわらず、CMDTC（データ収集日）が2013年9月6日となっており、CMSTDTCがCMDTCよりも未来の日付になっています。
    *   **問題点の原因（推測）:** データ入力時の誤り、またはCMSTDTCが正しくない可能性があります。Define.xmlではデータ型はDateとして定義されています。
    *   **対応策（提案）:** 
        *   CMSTDTCの妥当性を確認し、必要に応じて修正してください。
        *   CMDTCの日付がCMTRTの開始日より前になっている場合は、CMDTCの日付が正しいか確認してください。

*   **問題No.2:**
    *   **変数名と値:** MH.MHSTDTC = ""
    *   **矛盾の内容:** USUBJIDが"01-701-1153"のMHドメインにおいて、MHSTDTC（病歴イベントの開始日）が""（空）となっています。
    *   **問題点の原因（推測）:** データ入力時の誤り、あるいは情報が欠損している可能性があります。
    *   **対応策（提案）:**
        *   症例記録を確認し、MHSTDTCが欠損している理由を特定してください。
        *  必要であれば、医療機関に問い合わせて正確な日付を取得してください。

*   **問題No.3:**
    *   **変数名と値:** LB.LBDTC, SV.SVSTDTC
    *   **矛盾の内容:** LB.LBDTCはLBドメインの検査実施日時ですが、対応するSVドメインに検査実施日時と一致するデータが存在しません。データセットの中には、LB.VISITNUMにUnscheduledと記載されているものがあり、このことが原因でSVにデータが存在しない可能性があります。
    *   **問題点の原因（推測）:** 
        *   LBドメインとSVドメインの日時情報の不一致。
        *   LB検査が計画外（Unscheduled）で実施されたため、SVにVisit情報が存在しない。
    *   **対応策（提案）:**
        *   LBドメインとSVドメインの日時情報の整合性を確認してください。
        *   計画外の検査に関するデータ収集プロセスを確認してください。

クエリの作成:

*   **患者ID:** 01-701-1153
    *   **クエリNo.:1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC = "2011"、CM.CMDTC = "2013-09-06"
        *   **医療機関への問い合わせ文面:**
            *   CMTRT（薬剤名: TYLENOL）の開始日について。
            *   記録されている開始日（2011年）は、データ収集日（2013年9月6日）よりも前ですが、これは正しいですか？もし誤りがある場合、正しい開始日を教えてください。
            *   もし開始日が正しく、データ収集日にTYLENOLを服用していた場合、CMINDC（適応）をご教示ください。
        *   **判断理由:** CMSTDTCはCMTRTの評価において重要な情報であるため、データが正しいか確認が必要です。開始時期によっては、試験薬との相互作用や安全性評価に影響を与える可能性があります。
*   **患者ID:** 01-701-1153
    *   **クエリNo.:2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:**
            *   MHTERM（病歴名: ALZHEIMER'S DISEASE, VERBATIM_0120, VERBATIM_0239, VERBATIM_0301, VERBATIM_0390, VERBATIM_0688, VERBATIM_0705, VERBATIM_1443, VERBATIM_1751, VERBATIM_1769）の開始日について。
            *   記録されている開始日が空欄となっていますが、これは正しいですか？もし誤りがある場合、正しい開始日をご教示ください。
        *   **判断理由:** MHSTDTCはMHTERMの評価において重要な情報であるため、データが正しいか確認が必要です。


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1153
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DM.AGE = 79
    *   逸脱内容: 被験者01-701-1153は、治験参加時の年齢が79歳です。
    *   プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [1]
    *   判断理由: 年齢に関する選択基準（50歳以上）は満たしていますが、TSドメインのTSPARMCDがAGEMAXのレコード(AGEMAX Planned Maximum Age of Subjects No maximum)とAGEMINのレコード (AGEMIN Planned Minimum Age of Subjects 50 years)から、特に年齢上限が定められていないことがわかります。 したがって、これはプロトコルからの逸脱とはみなされません。

*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMDTC = "2013-09-06" (TYLENOL), DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: USUBJID「01-701-1153」のCMドメインにおいて、CMSTDTCが2011年であるにもかかわらず、CMDTC（データ収集日）が2013-09-06となっており、CM開始日よりCMDTCが後になっている。
    *   プロトコル該当箇所: データ収集の正確性に関する一般的な記述（具体的なセクションは特定できず）
    *   判断理由: 一般的に、データ収集はイベント発生後に行われるべきです。しかし、CMSTDTCの年が2011年と2年前であるため、データ入力時の誤りの可能性があります。

*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBDTC = "2013-09-06T14:50", DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: USUBJID「01-701-1153」のLBドメインにおいて、LBのデータ収集日(LBDTC)が検体採取日であり、DMドメインの治験薬初回投与日(RFSTDTC)より前の日付になっている。
    *   プロトコル該当箇所: データ収集の正確性に関する一般的な記述（具体的なセクションは特定できず）
    *   判断理由: DM.RFSTDTCは治験薬初回投与日であるため、LBのデータ収集日(LBDTC)がこれよりも前であるのは不自然です。データ入力時の誤りの可能性があります。

*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: VS.VSDTC = "2013-09-06", DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: USUBJID「01-701-1153」のVSドメインにおいて、VSのデータ収集日(VSDTC)がDMドメインの治験薬初回投与日(RFSTDTC)より前の日付になっている。
    *   プロトコル該当箇所: データ収集の正確性に関する一般的な記述（具体的なセクションは特定できず）
    *   判断理由: DM.RFSTDTCは治験薬初回投与日であるため、VSのデータ収集日(VSDTC)がこれよりも前であるのは不自然です。データ入力時の誤りの可能性があります。

*   逸脱No.: 5
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: QS.QSDTC = "2013-09-06", DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: USUBJID「01-701-1153」のQSドメインにおいて、QSのデータ収集日(QSDTC)がDMドメインの治験薬初回投与日(RFSTDTC)より前の日付になっている。
    *   プロトコル該当箇所: データ収集の正確性に関する一般的な記述（具体的なセクションは特定できず）
    *   判断理由: DM.RFSTDTCは治験薬初回投与日であるため、QSのデータ収集日(QSDTC)がこれよりも前であるのは不自然です。データ入力時の誤りの可能性があります。

*   逸脱No.: 6
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: AE.AESTDTC = "2013-10-13", DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: USUBJID「01-701-1153」のAEドメインにおいて、有害事象開始日(AESTDTC)が治験薬初回投与日(DM.RFSTDTC)より後になっている。
    *   プロトコル該当箇所: 3.9.3.2.1. Adverse Event Reporting Requirements
    *   判断理由: 特に問題ありません。

*   逸脱No.: 7
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DS.DSDTC = "2014-04-01", DM.RFENDTC = "2014-03-16"
    *   逸脱内容: USUBJID「01-701-1153」のDSドメインにおいて、DSDTCが最終投与日（DM.RFENDTC）より後になっている。
    *   プロトコル該当箇所: 3.  10.1 Discontinuations, 3.10.1.1 Retrieval of Discontinuations
    *   判断理由: 治験薬の投与終了後のデータであるため、特に問題ありません。

*   逸脱No.: 8
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBDY = -17, DM.DMDY = -17
    *   逸脱内容: USUBJID「01-701-1153」のLBドメインとDMドメインにおいて、LBの治験薬投与開始からの試験日(LBDY)とDMの治験薬投与開始からの試験日(DMDY)が、DM.RFSTDTCとLB.LBDTC/DM.DMDTCの差分から算出される日数と一致しない。
    *   プロトコル該当箇所: データ収集の正確性に関する一般的な記述（具体的なセクションは特定できず）
    *   判断理由: LBDYとDMDYの値が負の数であることから、治験薬投与開始日より前の日付であることがわかります。LBとDMのデータ収集日がDMドメインの治験薬初回投与日(RFSTDTC)より前の日付になっていることと合わせて、DM.RFSTDTC、LB.LBDTC、DM.DMDTCのいずれかのデータに誤りがある可能性があります。
*   逸脱No.: 9
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.LBBLFL = "Y" (各検査値), VISIT = "SCREENING 1"
    *   逸脱内容: スクリーニング1回目の検査結果にLBBLFL="Y"が設定されています。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: LBBLFLはBaseline Flagを示す変数であり、SDTMIGではBaseline Flagについて、以下のように定義されています。
    "LBBLFL (Baseline Flag) should be populated as “Y” if the laboratory test result represents a baseline assessment for the subject."。
    したがって、不適切なデータの可能性があります。

*   逸脱No.: 10
    *   臨床試験結果への影響度合い: None
    *   変数名と値: DM.DTHFL = "", DM.DTHDTC = ""
    *   逸脱内容: 死亡に関するデータ（DTHDTC, DTHFL）が未入力です。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 死亡していない被験者であるため、未入力であることは問題ありません。

*   逸脱No.: 11
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: SC.SCORRES = "6", SC.SCORRESU = "YEARS"
    *   逸脱内容: 教育年数が6年である。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 特に問題ありません。

*   逸脱No.: 12
    *   臨床試験結果への影響度合い: None
    *   変数名と値: DM.ACTARMCD = "Pbo", DM.ARMCD = "Pbo"
    *   逸脱内容: 計画された投与群と実際の投与群が一致している。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 特に問題ありません。

*   逸脱No.: 13
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DS.DSTERM = "PROTOCOL COMPLETED", DS.DSDECOD = "COMPLETED"
    *   逸脱内容: 治験を完了している。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 特に問題ありません。

*   逸脱No.: 14
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHBODSYS = "BLOOD AND LYMPHATIC SYSTEM DISORDERS" MHTERM = "VERBATIM_0120", MHDECOD = "ANAEMIA" MHSTDTC = "1977"
    *   逸脱内容: 既往歴に貧血の病歴がある
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria 
    *   判断理由: データからは貧血の重症度や具体的な状態が不明なため、必須除外基準に抵触するかどうか判断できません。

*   逸脱No.: 15
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHBODSYS = "NEOPLASMS BENIGN, MALIGNANT AND UNSPECIFIED (INCL CYSTS AND POLYPS)", MHTERM = "VERBATIM_0688", MHDECOD = "SKIN CANCER" MHSTDTC = "2010"
    *   逸脱内容: 既往歴に皮膚がんの病歴がある
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [25]
    *   判断理由: データからは皮膚がんの種類や治療状況が不明なため、必須除外基準に抵触するかどうか判断できません。

*   逸脱No.: 16
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE"
    *   逸脱内容: 既往歴にアルツハイマー病の診断がある。
    *   プロトコル該当箇所: 3.4.2.1 Inclusion Criteria [2]
    *   判断理由: アルツハイマー病患者を対象とした臨床試験であるため問題ありません。

*   逸脱No.: 17
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: VS.SYSBP = 144 mmHg (SCREENING 1, SUPINE), VS.SYSBP = 150 mmHg (SCREENING 2, SUPINE), DM.RFSTDTC = "2013-09-23"
    *   逸脱内容: スクリーニング時の血圧が140mmHgを超えている。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [17]
    *   判断理由: 
        DM.RFSTDTC(治験薬初回投与日)の時点では、161mmHgまで上昇しているため、組み入れ基準を満たしているか確認が必要です。

*   逸脱No.: 18
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.SPGRAV = "1.003", VISIT = "SCREENING 1"
    *   逸脱内容: スクリーニング1回目で尿比重が基準値(1.006-1.03)を下回る。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 除外基準に関連する項目ではないため、臨床的な判断が必要となる可能性があります。

*   逸脱No.: 19
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: QS.QSTESTCD = "MMITM01" - "MMITM06", VISIT = "SCREENING 1", QSORRESの値
    *   逸脱内容: MMSEスコアが10-23の範囲内であることの確認が必要です
    *   プロトコル該当箇所: 3.4.2.1 Inclusion Criteria [3]
    *   判断理由: データセットにはMMSEの各項目のデータは含まれていますが、合計スコアが計算されていません。MMSEの合計スコアが10-23の基準を満たしているか確認が必要です。

*   逸脱No.: 20
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: QS.QSTESTCD = "MHITM01" - "MHITM13", VISIT = "SCREENING 1", QSORRESの値
    *   逸脱内容: Modified Hachinski Ischemic Scale score が <= 4 であることの確認が必要です
    *   プロトコル該当箇所: 3.4.2.1 Inclusion Criteria [4]
    *   判断理由: データセットにはModified Hachinski Ischemic Scaleの各項目のデータは含まれていますが、合計スコアが計算されていません。Modified Hachinski Ischemic Scale scoreの合計スコアが4以下を満たしているか確認が必要です。

*   逸脱No.: 21
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: QS.NPITM12 = "ABSENT", VISIT = "WEEK 26", QSTEST = "APPETITE/EATING CHANGE PRESENT"
    *   逸脱内容: 最終評価のWeek26の評価でAPPETITE/EATING CHANGE PRESENTでABSENTが選択されている。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 特に問題ありません。

*   逸脱No.: 22
    *   臨床試験結果への影響度合い: None
    *   変数名と値: EX.EXTRT = "PLACEBO", DM.ARM = "Placebo"
    *   逸脱内容: USUBJID「01-701-1153」の被験者はPLACEBO群に割り付けられている。
    *   プロトコル該当箇所: (該当箇所なし)
    *   判断理由: 特に問題ありません。

**クエリ:**
*   患者ID: 01-701-1153
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE" MHSTDTC = "2005-05-13"
        *   医療機関への問い合わせ文面: 
            「被験者01-701-1153の既往歴にあるアルツハイマー病の診断は、本試験の選択基準を満たすものとして治験責任医師が判断したものでしょうか。
            また、MHDECODが空白ですが、医学辞書を用いて標準化された用語に置き換えることは可能でしょうか。」
        *   判断理由: 
            本試験はアルツハイマー病患者を対象としていますが、MHドメインにアルツハイマー病の病歴が含まれているため、Medical Historyのアルツハイマー病が本試験の選択基準として適切に評価されたものかどうかを確認する必要があります。
            MHDECODが空白である理由を確認します。
*   患者ID: 01-701-1153
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE" MHSTDTC = "2005-05-13"
        *   医療機関への問い合わせ文面: 
            「被験者01-701-1153の登録を承認する前に、DMドメインの治験薬初回投与日(RFSTDTC)2013-09-23時点で、基準[17]に抵触しないことを確認してください。試験登録時（DM.RFSTDTC）の血圧値が、高血圧の基準を満たしていなかったか確認してください。」
        *   判断理由: 
            DM.RFSTDTC(治験薬初回投与日)の時点では、161mmHgまで上昇しているため、基準[17]に抵触しないことを確認する必要があります。

*   患者ID: 01-701-1153
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: QSTESTCD = "MHITM01" - "MHITM13"
        *   医療機関への問い合わせ文面: 
            「被験者01-701-1153のModified Hachinski Ischemic Scale scoreの合計値を確認してください。プロトコルの組み入れ基準４に合致していますでしょうか？」
        *   判断理由:
         Modified Hachinski Ischemic Scale score は重要な組み入れ基準であり、この基準を満たしているか否かで、被験者の適格性が大きく左右されるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 4
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: QSTESTCD = "MMITM01" - "MMITM06"
        *   医療機関への問い合わせ文面: 
            「被験者01-701-1153のMMSEの合計値を確認してください。プロトコルの組み入れ基準３に合致していますでしょうか？」
        *   判断理由:
            MMSEは認知機能を評価する上で重要であり、本試験の組み入れ基準３に関わる項目であるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 5
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMSTDTC, CM.CMDTC
        *   医療機関への問い合わせ文面: 
            CMSTDTCの年が2011年であるにもかかわらず、CMDTC（データ収集日）が2013-09-06となっている理由について、CM開始日とCMデータ収集日の矛盾について確認してください。
        *   判断理由: データ品質の確保のため、矛盾している可能性のあるデータについて確認する必要があるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 6
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: LB.LBDTC, DM.RFSTDTC
        *   医療機関への問い合わせ文面: 
            LBの検体採取日(LB.LBDTC)が治験薬初回投与日(DM.RFSTDTC)より前の日付になっている理由について、データが正しく収集されたか確認してください。
        *   判断理由:
            DM.RFSTDTCは治験薬初回投与日であるため、LBのデータ収集日(LBDTC)がこれよりも前であるのは不自然であるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 7
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: VS.VSDTC, DM.RFSTDTC
        *   医療機関への問い合わせ文面: 
            VSのデータ収集日(VSDTC)が治験薬初回投与日(DM.RFSTDTC)より前の日付になっている理由について、データが正しく収集されたか確認してください。
        *   判断理由:
            DM.RFSTDTCは治験薬初回投与日であるため、VSのデータ収集日(VSDTC)がこれよりも前であるのは不自然であるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 8
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: QS.QSDTC, DM.RFSTDTC
        *   医療機関への問い合わせ文面: 
            QSのデータ収集日(QSDTC)が治験薬初回投与日(DM.RFSTDTC)より前の日付になっている理由について、データが正しく収集されたか確認してください。
        *   判断理由:
            DM.RFSTDTCは治験薬初回投与日であるため、QSのデータ収集日(QSDTC)がこれよりも前であるのは不自然であるため。

*   患者ID: 01-701-1153
    *   クエリNo.: 9
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: LB.LBBLFL = "Y" (各検査値), VISIT = "SCREENING 1"
        *   医療機関への問い合わせ文面:
            スクリーニング1回目の検査結果にLBBLFL="Y"が設定されている理由について、治験実施計画書に沿ったデータが入力されているか確認してください。
        *   判断理由:
            LBBLFL はBaseline Flagを示す変数であり、SDTMIGではBaseline Flagについて、
             "LBBLFL (Baseline Flag) should be populated as “Y” if the laboratory test result represents a baseline assessment for the subject."と定義されているため、不適切なデータの可能性があります。

クエリあり


# 01-704-1017
## Task1: Clinical Review Results
1. 症例サマリーの作成:

*   **患者ID:** 01-704-1017
    *   2013年09月20日 (Day -16): スクリーニング検査でクレアチニンが1.8 mg/dL (基準値上限: 1.6 mg/dL) と高値を示す。
    *   2013年10月06日 (Day 1): ベースライン評価。ADAS-Cog(11) サブスコアは27。
    *   2013年10月19日 (Day 14): 週2の検査でアルブミンが3.3 g/dL (基準値下限: 3.5 g/dL) と低値を示す。BUNが29 mg/dL (基準値上限: 24 mg/dL) と高値を示す。ミオカルディアル梗塞、LATE EFFECTS OF CEREBRAL INFRACTION、VENTRICULAR SEPTAL DEFECTの有害事象発現。
    *   2013年11月01日 (Day 27): 週4の検査でアルブミンが3.4 g/dL (基準値下限: 3.5 g/dL) と低値を示す。
    *   2013年11月05日 (Day 31): PRURITUS、RASHの有害事象発現。
    *   2013年11月09日 (Day 35): 週4の検査。BRAIN DEATHの有害事象発現。
    *   2013年11月18日 (Day 44): BRAIN DEATHの有害事象がRECOVERED/RESOLVEDとなる。
    *   2013年11月24日 (Day 50): ADVERSE EVENTにより試験中止。
    *   2013年12月06日 (AE FOLLOW-UP): 試験終了。

---

2. クエリの作成 (必要な場合のみ):

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:**
            *   AE.AETERM = "LATE EFFECTS OF CEREBRAL INFRACTION"
            *   AE.AESTDTC = "2013-10-19"
            *   AE.AEENDTC = "2013-11-18"
            *   AE.AESEV = "SEVERE"
        *   **医療機関への問い合わせ文面:**
            *   有害事象「LATE EFFECTS OF CEREBRAL INFRACTION」について、MedDRA(ver.8.0) のLLT、PT、HLT、HLGTに該当する用語とそのコードを教えてください。
            *   「LATE EFFECTS OF CEREBRAL INFRACTION」の有害事象の重症度(AE.AESEV)が「SEVERE」と報告されていますが、医学的に妥当ですか？
        *   **判断理由:**
            *   医学的に妥当な有害事象の評価を行う上で、MedDRAコードの確認は重要であるため。
            *   プロトコルに定義された有害事象の重症度評価の基準と照らし合わせ、医学的にSEVERな状態がいつからいつまで継続したのか確認する必要があるため。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:**
            *   AE.AETERM = "MYOCARDIAL INFARCTION"
            *   AE.AESTDTC = "2013-10-19"
            *   AE.AEENDTC = "2013-11-19"
        *   **医療機関への問い合わせ文面:**
            *   有害事象「MYOCARDIAL INFARCTION」について、MedDRA(ver.8.0) のLLT、PT、HLT、HLGTに該当する用語とそのコードを教えてください。
            *  「MYOCARDIAL INFARCTION」は、プロトコルで「A history within the last 5 years of a serious cardiovascular disorder」として除外基準に指定されています。本症例は組み入れ基準を満たしていたか、再度確認してください。
            *   もし組み入れ基準を満たさない場合、本症例が組み入れられた理由と、その後の対応について説明してください。
        *   **判断理由:**
            *   医学的に妥当な有害事象の評価を行う上で、MedDRAコードの確認は重要であるため。
            *   プロトコル違反の疑いがあり、臨床試験のデータ品質に影響を与える可能性があるため。
            *   組入れ基準を満たさない被験者のデータは、試験結果に影響を与える可能性があるため。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:**
            *   AE.AETERM = "PRURITUS", "RASH"
            *   AE.AESTDTC = "2013-11-05"
            *   AE.AEENDTC = "2013-11-22"
            *   DS.DSDECOD = "ADVERSE EVENT"
            *   DS.DSSTDTC = "2013-11-24"
        *   **医療機関への問い合わせ文面:**
            *  「PRURITUS」, 「RASH」は、治験薬投与部位に発生した局所的な反応ですか？もしそうであれば、臨床試験実施計画書に記載されている局所性皮膚反応の評価基準に照らし合わせて重症度を評価してください。
            *   治験薬の投与中止(2013-11-18)から、「ADVERSE EVENT」による試験中止(2013-11-24)までの期間が短いですが、投与中止の判断は適切ですか？
        *   **判断理由:**
            *   治験薬と有害事象の因果関係を評価するために、詳細な情報が必要となるため。
            *  有害事象が治験薬と関連する場合、適切な投与中止基準に沿って判断されているか確認する必要があるため。
    *   **クエリNo.:** 4
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   LB.LBTESTCD = "ALB"
            *   LB.VISIT = "WEEK 2", "WEEK 4"
            *   LB.LBORNRLO = "3.5"
            *   LB.LBORRES = "3.3", "3.4"
        *   **医療機関への問い合わせ文面:**
            *   検査値「ALB」について、WEEK 2とWEEK 4で基準値下限を下回っています。臨床的に特記すべき症状や、対応はありましたか？
        *   **判断理由:**
            *   アルブミン値の低下が臨床的に重要かどうかを確認するため。
    *   **クエリNo.:** 5
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   LB.LBTESTCD = "BUN"
            *   LB.VISIT = "WEEK 2"
            *   LB.LBORNRHI = "24"
            *   LB.LBORRES = "29"
        *   **医療機関への問い合わせ文面:**
            *   検査値「BUN」について、WEEK 2で基準値上限を上回っています。臨床的に特記すべき症状や、対応はありましたか？
        *   **判断理由:**
            *   BUN値の上昇が臨床的に重要かどうかを確認するため。
    *   **クエリNo.:** 6
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:**
            *   QS.QSTESTCD = "DAITM04", "DAITM30", "DAITM31", "DAITM32", "DAITM33"
            *   QS.VISIT = "BASELINE"
            *   QS.QSORRES = "NA"
        *   **医療機関への問い合わせ文面:**
            * Disability Assessment for Dementia (DAD)の評価項目DAITM04, DAITM30, DAITM31, DAITM32, DAITM33について、ベースラインで"NA"と評価された理由を教えてください。
        *   **判断理由:**
            *   "NA"の評価が妥当かどうかを確認するため。


## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, MH.MHSTDTC, AE.AESTDTC, AE.AEENDTC, RELREC.RELID, 各種スコアの算出

問題点:

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC = "2000"
    *   **矛盾の内容:** CM.CMSTDTCの値が"2000"となっているレコードが複数存在する。日付として不適切。
    *   **問題点の原因（推測）:** データ入力時の誤り。
    *   **対応策（提案）:** 原資料を確認し、正しい日付に修正。

*   **問題No.2:**
    *   **変数名と値:** CM.CMENDTC = null
    *   **矛盾の内容:** CM.CMENDTCの値がnullとなっているレコードが複数存在する。
    *   **問題点の原因（推測）:** 投与が継続しているか、データ入力時の誤り。
    *   **対応策（提案）:** 投与が継続している場合は、最終投与日を確認し、CMENDTCを更新。データ入力時の誤りの場合は、原資料を確認し修正。

*   **問題No.3:**
    *   **変数名と値:** MH.MHSTDTC = ""
    *   **矛盾の内容:** MH.MHSTDTCの値が空文字となっているレコードが存在する。
    *   **問題点の原因（推測）:** 開始日が不明、またはデータ入力時の誤り。
    *   **対応策（提案）:** 開始日が不明な場合は、その旨を記録。データ入力時の誤りの場合は、原資料を確認し修正。

*   **問題No.4:**
    *   **変数名と値:** AE.AEENDTC = ""
    *   **矛盾の内容:** AE.AEENDTCの値が空文字となっているレコードが存在する。
    *   **問題点の原因（推測）:** 症状が継続中、またはデータ入力時の誤り。
    *   **対応策（提案）:** 症状が継続中の場合は、その旨を記録。データ入力時の誤りの場合は、原資料を確認し修正。

*   **問題No.5:**
    *   **変数名と値:** AE.AESTDTC, AE.AEENDTC
    *   **矛盾の内容:** AE.AESTDTCとAE.AEENDTCの日付の整合性が一部とれていない。AE0004とAE0005, AE0006とAE0007でAESTDTCがAEENDTCより未来の日付になっている。
    *   **問題点の原因（推測）:** データ入力時の誤り、または有害事象の継続期間の記録が不正確。
    *   **対応策（提案）:** 原資料を確認し、日付を修正。

*   **問題No.6:**
    *   **変数名と値:** RELREC.RELID
    *   **矛盾の内容:** AE0005 (AESEQ = 5), AE0007 (AESEQ = 7)とDS0001 (DSSEQ = 1)の3つのレコードでRELRECがAE0006と関連付けられていない。RELTYPEが空欄。
    *   **問題点の原因（推測）:** 関連レコードの指定漏れ。
    *   **対応策（提案）:** 本来関連付けられるべきAEレコードを確認し、RELIDとRELTYPEを修正。

*   **問題No.7:**
    *   **変数名と値:** QS.QSSTRESN, NPI-X関連の変数
    *   **矛盾の内容:** QSドメインのスコアリングに疑義。NPI-Xの各項目のスコア(=周波数x重症度)と、NPI-X(9) Total Scoreに整合性があるか確認する必要がある。
    *   **問題点の原因（推測）:** スコアリングロジックの誤り、計算間違い、またはデータ入力時の誤り。
    *   **対応策（提案）:** スコアリングロジックを確認し、必要に応じて再計算。

クエリの作成:

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** CM.CMSTDTC = "2000"
        *   **医療機関への問い合わせ文面:** 
            *   CM.CMSTDTC（併用薬開始日）が2000年となっていますが、正 しい日付をご教示ください。
        *   **判断理由:**
            *   併用薬の使用期間に影響するため。

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMENDTC = null
        *   **医療機関への問い合わせ文面:** 
            *   CM.CMENDTC（併用薬終了日）が空欄ですが、併用薬は終了していますか？終了している場合は、終了日をご教示ください。
        *   **判断理由:**
            *   併用薬の使用状況を正確に把握する必要があるため。

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHSTDTC = ""
        *   **医療機関への問い合わせ文面:** 
            *   MH.MHSTDTC（既往歴開始日）が空欄となっていますが、開始日をご教示ください。
        *   **判断理由:**
            *   医学的背景を把握する必要があるため。

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 4
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC, AE.AEENDTC
        *   **医療機関への問い合わせ文面:** 
            *   AE.AESTDTC（有害事象開始日）とAE.AEENDTC（有害事象終了日）に矛盾があります。正しい日付をご教示ください。
        *   **判断理由:**
            *   有害事象の評価において、正確な発現時期は重要であるため。

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 5
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** RELREC.RELID
        *   **医療機関への問い合わせ文面:** 
            *   RELRECレコードにおいて、AE0005 (AESEQ = 5), AE0007 (AESEQ = 7)とDS0001 (DSSEQ = 1)の3つのレコードでRELRECがAE0006と関連付けられていません。RELTYPEが空欄となっていますが、関連する有害事象をご教示ください。
        *   **判断理由:**
            *   有害事象と処置の関連性を正確に把握する必要があるため。

*   **患者ID:** 01-704-1017
    *   **クエリNo.:** 6
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.QSSTRESN, NPI-X関連の変数
        *   **医療機関への問い合わせ文面:** 
            *   NPI-Xのスコアについて、各項目のスコアと合計スコアに整合性があるか確認をお願いします。
        *   **判断理由:**
            *   評価項目の信頼性を担保するため。

## Task3: Protocol Deviation Review Results
患者ID: 01-704-1017

*   **逸脱No.: 1**
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** MH.MHTERM = ALZHEIMER'S DISEASE, MHDTC = 2011-03-27
    *   **逸脱内容:** 被験者01-704-1017は、Medical Historyにおいて、アルツハイマー病の発症日が2011年3月27日と記録されている。しかし、Inclusion Criteriaの[2]には「Diagnosis of probable AD as defined by NINCDS and the ADRDA guidelines」と記載されているのみで、罹病期間に関する規定はない。EXCL14には「A history of mental illness within the last 5 years」と記載されているが、アルツハイマー病はこれに該当しないと考えられる。ただし、治験薬の選択基準には、罹病期間が短いほど効果が高いという前提がある場合がある。
    *   **プロトコル該当箇所:** 3.4.2.1. Inclusion Criteria [2], 3.4.2.2. Exclusion Criteria [14]
    *   **判断理由:** プロトコルに明確な規定はないものの、治験薬の効果に影響を与える可能性があるため。

*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** MH.MHTERM = ALZHEIMER'S DISEASE, MHDTC = 2011-03-27
    *   **医療機関への問い合わせ文面:** 被験者01-704-1017のアルツハイマー病診断日（2011年3月27日）は、本試験のプロトコルにおいて、治験薬の効果に影響を与える可能性はありますか？もしそうであれば、具体的にどのような影響が考えられますか？
    *   **判断理由:** プロトコルに明確な規定はないものの、治験薬の効果に影響を与える可能性があるため。

患者ID: 01-704-1017

*   **逸脱No.: 2**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** AE.AETERM = LATE EFFECTS OF CEREBRAL INFRACTION, AESTDTC = 2013-10-19
    *   **逸脱内容:** 被験者01-704-1017に「LATE EFFECTS OF CEREBRAL INFRACTION（脳梗塞後遺症）」というAdverse Eventが発現している。これはExclusion CriteriaのEXCL12「Diagnosis of serious neurological conditions.」に該当する可能性がある。Medical Historyにも心疾患の既往歴がある。
    *   **プロトコル該当箇所:** 3.4.2.2 Exclusion Criteria [12], MH
    *   **判断理由:** 脳梗塞後遺症は神経系の重篤な状態とみなされる可能性があり、プロトコルからの逸脱となる可能性があるため。ただし、ADAMINDのレビューでは、この被験者は除外基準を満たしていると判断された。

*   **クエリNo.: 2**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AETERM = LATE EFFECTS OF CEREBRAL INFRACTION, AESTDTC = 2013-10-19, MH.MHTERM = MYOCARDIAL INFARCTION
    *   **医療機関への問い合わせ文面:** 被験者01-704-1017に認められた脳梗塞後遺症は、本試験の選択基準に照らし合わせて「組み入れ可能」と判断された理由は何ですか？詳細な医学的見解をお聞かせください。また、心筋梗塞の既往歴がありますが、組み入れ基準を満たすと判断した理由もお聞かせください。
    *   **判断理由:** 
  
        *   脳梗塞後遺症と心筋梗塞の既往歴がプロトコルに抵触するかどうか、確認する必要があるため。

患者ID: 01-704-1017

*   **逸脱No.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT = ASPIRIN, CMSTDTC = 2000
    *   **逸脱内容:** 被験者01-704-1017は、Concomitant Medicationsとしてアスピリンを2000年から服用している。プロトコルに併用禁止薬に関する記述はないが、アスピリンの長期投与が試験結果に影響を与える可能性を考慮する必要がある。特に、APOE4キャリアの場合、アスピリンの効果が異なる可能性が考えられる。
    *   **プロトコル該当箇所:** 3.8 Concomitant Therapy
    *   **判断理由:** プロトコルに明確な規定はないものの、併用薬が試験結果に影響を与える可能性があるため。

*   **クエリNo.: 3**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CM.CMTRT = ASPIRIN, CMSTDTC = 2000, DM.APOE4 (?)
    *   **医療機関への問い合わせ文面:** 被験者01-704-1017のアスピリン長期投与は、本試験の結果に影響を与える可能性はありますか？特に、APOE4キャリアである場合、どのような影響が考えられますか？
    *   **判断理由:** アスピリンの長期投与が試験結果に影響を与える可能性を考慮する必要があるため。

# 01-702-1082
## Task1: Clinical Review Results
患者ID: 01-702-1082

*   2013年07月03日 (Day -23): スクリーニング検査にて、BUN (25 mg/dL, 基準範囲 4-24 mg/dL) が高値、HCT (49.0 %, 基準範囲 34-48 %) が高値、WBC (14.77 THOU/uL, 基準範囲 3.8-10.7 THOU/uL) が高値、VITB12 (946 pg/mL, 基準範囲 200-900 pg/mL) が高値を示す。
*   2013年07月07日 (Day -19): 白血球数が増加、尿検査異常が見られる。
*   2013年07月24日 (Day -2): UNSCHEDULED 1.1回目の検査にて、ALT (37 U/L, 基準範囲 6-32 U/L) が高値、AST (44 U/L, 基準範囲 9-34 U/L) が高値、BUN (27 mg/dL, 基準範囲 4-24 mg/dL) が高値を示す。
*   2013年07月26日 (Day 1): ベースライン検査。
*   2013年08月08日 (Day 14): WEEK 2の検査にて、CK (320 U/L, 基準範囲 21-169 U/L) が高値を示す。
*   2013年09月02日 (Day 39): 矩直腸出血が発生。
*   2013年09月09日 (Day 46): 皮膚刺激が発生。
*   2013年09月24日 (Day 61): 申請部位に炎症が見られる。
*   2013年10月12日 (Day 79): 皮膚刺激が発生。
*   2013年11月17日 (Day 115): WEEK 12の検査にて、Protein (8.1 g/dL, 基準範囲 6-8 g/dL) が高値を示す。ケトン体尿検査で異常値が見られる。被験者がパッチによる痒みを訴え、ピルを希望したため、試験を中止。

---

**患者ID:** 01-702-1082

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBNRIND = HIGH (AST, ALT, BUN, WBC), LB.LBSTRESN (VITB12)
    *   **医療機関への問い合わせ文面:**
        *   スクリーニング時の検査値（BUN, HCT, VITB12, WBC）が高い理由は何か？
        *   2013-07-24にALT, ASTが上昇している理由は何か？
        *   治験薬投与開始後もALT, AST, WBCは高い値で推移しているが、医学的に問題はないか？
        *  2013-09-04にSYSBPが96 mmHgまで低下しているが、原因は何か？
    *   **判断理由:** スクリーニング検査で複数の検査項目で基準値外の結果が出ている。治験薬投与後も肝機能関連の検査値で基準値超過が散見される。また、QT延長やBrugada症候群などの心血管系の除外基準に抵触していないか確認する必要がある。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AEOUT = "NOT RECOVERED/NOT RESOLVED"
    *   **医療機関への問い合わせ文面:**
        *   Neutrophil Count IncreasedとUrine Analysis Abnormalは治験終了時に回復/解決していないが、理由は何か？
        *   これらは、治験薬投与との関連性はあるか？
        *   他に徴候や症状はなかったか？
    *   **判断理由:** 治験薬との関連が否定できない場合、治験結果に影響を及ぼす可能性があるため。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** DS.DSTERM = PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS'PILLS'"
    *   **医療機関への問い合わせ文面:**
        *   治験を中止した理由は、被験者がHYDROCORTISONE, TOPICALをWEEK8とWEEK12で使用したことと関連があるか？
        *   「パッチが不便でかゆい」という訴えは、紅斑、湿疹、皮膚炎などの局所性皮膚反応と関連があるか？
        *    2013-11-17に実施された「FINAL LAB VISIT」は、治験薬投与終了後、30日以内に行われているか？
    *   **判断理由:**
        *   添付文書に皮膚刺激が記載されている場合、治験薬との因果関係を評価する必要があるため。
        *   HYDROCORTISONE, TOPICALの使用状況と皮膚刺激の発生時期を比較し、因果関係を評価する必要があるため。
        *   プロトコルに治験薬投与終了後の検査に関する規定がある場合、それに準拠しているか確認する必要があるため。


## Task2: DM Review Results
全体的なデータ品質の評価:
*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CMの併用薬、DSのDSDTCとDSSTDTC、LBのLBDTC

問題点:

*   **問題No.1:**
    *   **変数名と値:** CM.CMSTDTC = "2013-09-24", CM.CMENDTC = "2013-10-31" (1行目) CM.CMSTDTC = "2013-09-24", CM.CMENDTC = "2013-10-31" (2行目) CM.CMDTC = "2013-09-28" (1行目), CM.CMDTC = "2013-11-17" (2行目)
    *   **矛盾の内容:** 2行のCMデータにおいて、CMSTDTCとCMENDTCが同じであり、CMDTCの値が異なっている。2行目のCMDTCはCMENDTCより後の日付になっている。
    *   **問題点の原因（推測）:** データ入力エラー、またはデータ収集時の日付の誤り。
    *   **対応策（提案）:** CMSTDTC、CMENDTC、CMDTCの整合性を確認し、必要に応じて修正。

*   **問題No.2:**
    *   **変数名と値:** DS.DSDTC = "2013-11-17T12:20", DS.DSSTDTC = "2013-11-17" (2行目)
    *   **矛盾の内容:** 2行目のDSデータにおいて、DSDTCがタイムスタンプを含み、DSSTDTCが日付のみである。DSDTCは必須項目ではないが、タイムスタンプの情報があることで、DSSTDTCに時間情報がないことが不自然に見える。
    *   **問題点の原因（推測）:** データ入力時の不整合、またはデータ収集方法の違い。
    *   **対応策（提案）:** DSDTCとDSSTDTCの形式を統一するか、またはDSDTCの時間情報を欠損させるかを検討。

*   **問題No.3:**
    *   **変数名と値:** LB.LBDTC = "2013-07-03T14:00" (1行目), DM.RFSTDTC = "2013-07-26"
    *   **矛盾の内容:** 1行目のLBデータにおいて、LBDTCがDM.RFSTDTCより前の日付になっている。
    *   **問題点の原因（推測）:** データ入力エラー、またはLBDTCの誤り。
    *   **対応策（提案）:** LBDTCがDM.RFSTDTCより前の日付になっているLBデータを調査し、修正が必要かどうか判断。

クエリ:

*   **患者ID:** 01-702-1082
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "HYDROCORTISONE, TOPICAL", CM.CMSTDTC = "2013-09-24", CM.CMENDTC = "2013-10-31" (1行目) CM.CMTRT = "HYDROCORTISONE, TOPICAL", CM.CMSTDTC = "2013-09-24", CM.CMENDTC = "2013-10-31" (2行目) CM.CMDTC = "2013-09-28" (1行目), CM.CMDTC = "2013-11-17" (2行目)
        *   **医療機関への問い合わせ文面:** 併用薬HYDROCORTISONE, TOPICALについて、CMSTDTC、CMENDTC、CMDTCに矛盾が見られます。CMSTDTC、CMENDTC、CMDTCの正しい日付と時間を確認してください。
        *   **判断理由:** 併用薬の使用期間が不明確であるため、試験結果に影響を与える可能性がある。

*   **患者ID:** 01-702-1082
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSDTC = "2013-11-17T12:20", DS.DSSTDTC = "2013-11-17" (2行目)
        *   **医療機関への問い合わせ文面:** 2つめのDSTERM (FINAL LAB VISIT) のDSDTCとDSSTDTCにずれがあるようです。DSDTCに時間情報が必要か、DSSTDTCと合わせるべきか確認してください。
        *   **判断理由:** DSDTCとDSSTDTCの不整合は、データ品質の問題を引き起こす可能性がある。

*   **患者ID:** 01-702-1082
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBDTC = "2013-07-03T14:00" (1行目), DM.RFSTDTC = "2013-07-26"
        *   **医療機関への問い合わせ文面:** 最初の検査 (ALB) の実施日が最初の投薬日より前になっています。矛盾がないか確認してください。
        *   **判断理由:** 臨床検査データの信頼性を確保するため。

## Task3: Protocol Deviation Review Results
患者ID: 01-702-1082

逸脱No.: 1
臨床試験結果への影響度合い: Major
変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2007-05-17
逸脱内容: 被験者01-702-1082は、Medical Historyにアルツハイマー病の既往歴があります。プロトコルTIに記載されたExclusion Criteria EXCL12「認知症の重篤な神経学的状態の診断」に違反している可能性があります。アルツハイマー病の診断は組み入れ基準INCL02にも記載されており、medical historyに出ていることと矛盾します。
プロトコル該当箇所: Inclusion Criteria [2], Exclusion Criteria [12]
判断理由: 
TIデータセットのEXCL12には「認知症の重篤な神経学的状態の診断」が除外基準として定義されています。
MHデータセットに「アルツハイマー病」の既往歴がある場合、EXCL12に抵触する可能性があります。

患者ID: 01-702-1082
クエリNo.: 1
臨床試験結果への影響度合い: Major
変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSTDTC = 2007-05-17
医療機関への問い合わせ文面:
被験者01-702-1082のアルツハイマー病の診断時期、重症度、および現在の状態について、詳細な情報を提供してください。特に、組み入れ基準を満たす「probable AD」の診断と、除外基準に抵触する「重篤な神経学的状態」に該当するかどうかを明確にしてください。
判断理由:
MHデータセットにアルツハイマー病の既往歴がある被験者について、プロトコル除外基準EXCL12との整合性を確認するため。


# 01-701-1023
## Task1: Clinical Review Results
### 症例サマリー

*   **患者ID:** 01-701-1023
    *   2012年07月22日 (Day -14): スクリーニング1回目。既往歴としてアルツハイマー病、足の蜂窩織炎、腰痛、高血圧、陰茎プロテーゼ挿入、筋肉痛、食道逆流症、食道裂孔ヘルニア、消化不良、頭痛、肘の骨折、上腕の痺れ、副鼻腔炎、虫垂炎、虫垂切除、外傷性疼痛、湿疹、坐骨神経痛、皮膚掻痒症の病歴がある。併用薬としてアスピリン (325mg, PRN, 経口)、ミランタ (1 Tbsp, PRN, 経口)、TUMS (1 Tablet, PRN, 経口) を服用。
    *   2012年08月05日 (Day 1): ベースライン。EXドメインによると、プラセボ投与が開始された（0mg, パッチ, QD, 経皮投与）。
        ADAS-Cog(11)サブスコアは13。NPI-Xでは、妄想は認められず、Agitation/Aggressionのスコアが1、Depression/Dysphoriaのスコアが4、Anxietyのスコアが4。DADの各項目はすべて「Y」（できる）と評価されている。
    *   2012年08月07日 (Day 3): 有害事象として紅斑が発現 (軽度、転帰は未回復)。
    *   2012年08月26日 (Day 22): Ambulatory ECG placement。
    *   2012年08月27日 (Day 23): AEとして、2度の房室ブロックが発現 (軽度、転帰は未回復)。NPI-Xでは、Delusionsの頻度が3、重症度が1。
    *   2012年09月02日 (Day 29): AEとして、紅斑が発現 (軽度、転帰は回復)。CIBICは「MINIMAL IMPROVEMENT (わずかな改善)」。DADの項目で、「HANDLE ADEQUATELY HIS/HER MONEY」のみ「N (できない)」。
    *   2013年02月18日 (Day 198): Retrieval。ADAS-Cog(11)サブスコアは12。CIBICは「MINIMAL WORSENING (わずかな悪化)」。NPI-Xでは、Irritability/Labilityの評価で異常が見られる。

---

### クエリ

*   **患者ID:** 01-701-1023
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:**
            *   AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
            *   AE.AESTDTC = "2012-08-26"
        *   **医療機関への問い合わせ文面:** 2度の房室ブロックが2012年8月26日に発症とのことですが、AESTDTCが2012年8月26日となっています。不整脈の正確な発症日を教えてください。
        *   **判断理由:** 2度の房室ブロックは重大な有害事象であり、正確な発症日の特定は因果関係の評価に不可欠です。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:**
            *   CM.CMTRT = "MYLANTA", CM.CMDECOD = "UNCODED"
            *   CM.CMTRT = "TUMS", CM.CMDECOD = "UNCODED"
        *   **医療機関への問い合わせ文面:** 併用薬のミランタとTUMSのCMDECODが"UNCODED"となっています。該当する標準化された薬剤名に更新してください。
        *   **判断理由:** 併用薬の標準化は、薬剤の相互作用評価や安全性解析において重要です。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** QS.QSTESTCD = "DAITM31", VISIT = "RETRIEVAL", QSORRES = "NA"
        *   **医療機関への問い合わせ文面:** DAD質問票の項目DAITM31 "PAY HIS/HER BILLS" (請求書の支払い) について、Retrieval（回収）時の回答が "NA" (該当なし) となっています。
        これは、対象者がもはや請求書の支払いを試みなくなったことを意味しますか、それとも単に評価できなかったことを意味しますか？
        *   **判断理由:** DADは主要評価項目であり、ADLの評価として重要であるため、回答が"NA"となった理由を明確にする必要
## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMDECOD, MH.MHTERM, MH.MHDECOD

**問題点:**

*   **問題No.: 1**
    *   **変数名と値:** CM.CMTRT="MYLANTA", CM.CMDECOD="UNCODED"
    *   **矛盾の内容:** 複数のCMレコードにおいて、CMTRT(服用薬)が"MYLANTA"であるにもかかわらず、CMDECOD(標準化された薬剤名)が"UNCODED"となっている。 MYLANTAは一般名であるため、CMDECODには対応する標準化された薬剤名が入るべき。
    *   **問題点の原因（推測）:** データ入力時、またはMedDRA等の標準的な辞書との照合時に、MYLANTAに対する適切な標準化された薬剤コードが見つからなかった。
    *   **対応策（提案）:**
        1.  医療機関にMYLANTAの具体的な成分・薬品名の確認
        2.  確認した情報をもとに、MedDRA等の標準的な辞書を用いてCMDECODを修正

*   **問題No.: 2**
    *   **変数名と値:** CM.CMTRT="TUMS", CM.CMDECOD="UNCODED"
    *   **矛盾の内容:** 複数のCMレコードにおいて、CMTRT(服用薬)が"TUMS"であるにもかかわらず、CMDECOD(標準化された薬剤名)が"UNCODED"となっている。 TUMSは制酸薬のブランド名であり、CMDECODには対応する標準化された薬剤名が入るべき。
    *   **問題点の原因（推測）:** データ入力時、またはMedDRA等の標準的な辞書との照合時に、TUMSに対する適切な標準化された薬剤コードが見つからなかった。
    *   **対応策（提案）:**
        1.  医療機関にTUMSの具体的な成分の確認
        2.  確認した成分をもとに、MedDRA等の標準的な辞書を用いてCMDECODを修正

*   **問題No.: 3**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0073", MH.MHDECOD="CELLULITIS"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0073"となっている。 VERBATIM_0073という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0073の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 4**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0249", MH.MHDECOD="GASTROOESOPHAGEAL REFLUX DISEASE"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0249"となっている。 VERBATIM_0249という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0249の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 5**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0291", MH.MHDECOD="BACK PAIN"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0291"となっている。 VERBATIM_0291という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0291の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 6**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0342", MH.MHDECOD="HYPERTENSION"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0342"となっている。 VERBATIM_0342という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0342の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 7**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0388", MH.MHDECOD="PENILE PROSTHESIS INSERTION"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0388"となっている。 VERBATIM_0388という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0388の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 8**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0461", MH.MHDECOD="MYALGIA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0461"となっている。 VERBATIM_0461という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0461の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 9**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0596", MH.MHDECOD="HYPOAESTHESIA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0596"となっている。 VERBATIM_0596という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0596の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 10**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0699", MH.MHDECOD="HIATUS HERNIA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0699"となっている。 VERBATIM_0699という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0699の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 11**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0788", MH.MHDECOD="APPENDICITIS"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0788"となっている。 VERBATIM_0788という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0788の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 12**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0800", MH.MHDECOD="DYSPEPSIA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0800"となっている。 VERBATIM_0800という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0800の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 13**
    *   **変数名と値:** MH.MHTERM="VERBATIM_0929", MH.MHDECOD="HEADACHE"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_0929"となっている。 VERBATIM_0929という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_0929の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 14**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1002", MH.MHDECOD="UPPER LIMB FRACTURE"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1002"となっている。 VERBATIM_1002という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1002の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 15**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1042", MH.MHDECOD="DYSPNOEA EXERTIONAL"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1042"となっている。 VERBATIM_1042という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1042の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 16**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1154", MH.MHDECOD="ECZEMA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1154"となっている。 VERBATIM_1154という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1154の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 17**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1200", MH.MHDECOD="SCIATICA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1200"となっている。 VERBATIM_1200という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1200の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 18**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1364", MH.MHDECOD="PRURITUS"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1364"となっている。 VERBATIM_1364という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1364の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 19**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1532", MH.MHDECOD="MYOPIA"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1532"となっている。 VERBATIM_1532という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1532の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 20**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1554", MH.MHDECOD="INGUINAL HERNIA REPAIR"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1554"となっている。 VERBATIM_1554という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1554の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 21**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1617", MH.MHDECOD="PAIN TRAUMA ACTIVATED"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1617"となっている。 VERBATIM_1617という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1617の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 22**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1769", MH.MHDECOD="SINUSITIS"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1769"となっている。 VERBATIM_1769という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1769の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 23**
    *   **変数名と値:** MH.MHTERM="VERBATIM_1775", MH.MHDECOD="APPENDICECTOMY"
    *   **矛盾の内容:** MHTERM(報告された病名)が"VERBATIM_1775"となっている。 VERBATIM_1775という名称から、データ入力時の原文がそのまま入っている可能性が疑われる。
    *   **問題点の原因（推測）:** データ入力時に原文を意味のある語彙に置き換える処理がされていない。
    *   **対応策（提案）:**
        1.  VERBATIM_1775の原文を調査
        2.  調査した原文を基に、MedDRA等の標準的な辞書を用いてMHDECODを修正

*   **問題No.: 24**
    *   **変数名と値:** RELREC.RELID="01-701-1023-E09"
    *   **矛盾の内容:** RELRECデータセットに、AEドメインのAESEQ=2に関連する情報が記録されているが、AELLTCD, AEPTCD, AEHLTCD, AEHLGTCD, AEBDSYCD, AESOCCDがNULLとなっている。 AEドメインのデータがNULLの場合、RELRECに記録する必要はないと考えられる。
    *   **問題点の原因（推測）:** AEに存在しないAELLTCD等の情報をRELRECに記録しようとしたため。
    *   **対応策（提案）:** AELLTCD等の情報が存在しない場合、RELRECへの記録は行わない。

**クエリの作成:**

*   **患者ID:** 01-701-1023
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT="MYLANTA", CM.CMDECOD="UNCODED"
        *   **医療機関への問い合わせ文面:**
            *   治験参加者ID: 01-701-1023の併用薬MYLANTAについて質問です。
            *   MYLANTAの具体的な成分名、または薬品名を教えてください。
            *   もしMYLANTAの成分が複数ある場合、それぞれの成分名と投与量をご教示ください。
        *   **判断理由:**
            *   併用薬の情報は、試験結果に影響を与える可能性のある重要な情報であるため。

*   **患者ID:** 01-701-1023
    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT="TUMS", CM.CMDECOD="UNCODED"
        *   **医療機関への問い合わせ文面:**
            *   治験参加者ID: 01-701-1023の併用薬TUMSについて質問です。
            *   TUMSの具体的な成分名を教えてください。
            *   もしTUMSの成分が複数ある場合、それぞれの成分名と投与量をご教示ください。
        *   **判断理由:**
            *   併用薬の情報は、試験結果に影響を与える可能性のある重要な情報であるため。

*   **患者ID:** 01-701-1023
    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** MH.MHTERM like "VERBATIM_%"
        *   **医療機関への問い合わせ文面:**
            *   治験参加者ID: 01-701-1023のMedical Historyについて質問です。
            *   MHTERMが"VERBATIM_***"となっているMedical Historyについて、具体的な病名を教えてください。
        *   **判断理由:**
            *   MHTERMは原文がそのまま入力されている可能性が高く、標準病名に変換する必要があるため。


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1023
  *   逸脱No.: 1
      *   臨床試験結果への影響度合い: Minor
      *   変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE
      *   逸脱内容: 被験者01-701-1023は、Medical Historyに「ALZHEIMER'S DISEASE」の既往歴がある。
      *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria
      *   判断理由: TI.IETESTのEXCL12に「Diagnosis of serious neurological conditions.」とあり、アルツハイマー病が除外基準に該当するため。

患者ID: 01-701-1023
  *   クエリNo.: 1
      *   臨床試験結果への影響度合い: Major
      *   変数名と値: QS.DAITM31 = 96 (Not Applicable)
      *   医療機関への問い合わせ文面:
          *   Disability Assessment for Dementia (DAD) の質問項目 "PAY HIS/HER BILLS" (DAITM31) に対して、RETRIEVAL (Visit 201) 時に "NA" (96) と回答されています。これは、QVAL の定義から逸脱している可能性があります。
          *   この患者は、"PAY HIS/HER BILLS"という行動を、RETRIEVAL (Visit 201) 時に実施できなかった、または評価不能であった理由を教えてください。
      *   判断理由: DADは認知機能の低下に伴う日常生活動作の障害を評価するものであり、可能な限りすべての項目について評価されるべきです。


# 01-701-1181
## Task1: Clinical Review Results
患者ID: 01-701-1181

*   2013年11月26日 (Day -9): スクリーニング1回目の検査で、アルブミン値が基準範囲を下回る (3.2 g/dL, 基準範囲: 3.5-4.6 g/dL)。
*   2013年12月05日 (Day 1): ベースライン評価。ADAS-Cog(11)サブスコアは32。DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の複数の項目で、介護なしではADL（日常生活動作）が困難であることが示唆されている。NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)において、Agitation/Agressionのスコアが2、Depression/Dysphoriaのスコアが1、Anxietyのスコアが2、Apathy/Indifferenceのスコアが4と評価された。
*   2013年12月09日 (Day 5): Agitationが発生（中程度の強度）。
*   2013年12月12日 (Day 8): Week2回目の検査。DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の項目に改善が見られず、telephonig、going on an outingなどの項目が悪化している。ADAS-Cog(11)サブスコアは39に悪化。NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)において、Depression/Dysphoriaのスコアが9、Anxietyのスコアが4と悪化。
*   2014年05月23日 (Day 170): 最終評価。ADAS-Cog(11)サブスコアは38。CIBICのスコアは5（Minimal Worsening）。NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)において、Hallucinationsのスコアが6、Agitation/Agressionのスコアが4、Depression/Dysphoriaのスコアが4、Aberrant Motor Behaviorのスコアが6、Irritability/Labilityのスコアが2と悪化。

---

患者ID: 01-701-1181

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AEOUT: RECOVERED/RESOLVED
        *   QS.QSTESTCD: ACTOT
        *   QS.QSTESTCD: CIBIC
        *   QS.QSTESTCD: NPITM03S, NPITM04S, NPITM10S
    *   **医療機関への問い合わせ文面:** Agitation（2013年12月09日発現）の転帰はRECOVERED/RESOLVEDとありますが、ADAS-Cog, CIBIC, NPI-Xの結果をみると、認知機能、精神症状は悪化しています。Agitation発生前後の精神状態について、詳しく教えてください。
    *   **判断理由:** Agitationと認知機能テスト、精神症状評価の結果に矛盾が見られるため、Agitationが認知機能に与える影響について評価するため。

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, DM.ACTARMCD, DM.ACTARM, AE.AETERM, RELREC.RELID

問題点:

*   問題No.1:
    *   変数名と値: CM.CMSTDTC = "1985", CM.CMENDTC = "" (Null) (複数レコード)
    *   矛盾の内容: 
        *   CMドメインにおいて、CMSTDTCが1985年と過去の日付で記録されているにもかかわらず、CMENDTCがNull（欠損）となっているデータが複数存在します。これは、Concomitant Medicationsの開始日が記録されているにもかかわらず、終了日が記録されていないことを意味します。
        *   DMドメインのRFSTDTC（Subject Reference Start Date/Time）は2013-12-05であり、CMの記録と矛盾しています。
    *   問題点の原因（推測）:
        *   データ入力時の誤り。
        *   CMENDTCの取得漏れ、またはConcomitant Medicationが継続している場合にNullが許容されている。
    *   対応策（提案）:
        1.  CMENDTCがNullとなっている症例について、Medicationが終了しているか確認し、終了日を記録する。
        2.  CMSTDTCが過去の日付（1985年）となっている理由を確認する。
        3.  Define.xmlのCMENDTCにNullが許容される旨を追記する。

*   問題No.2:
    *   変数名と値: DM.ACTARMCD = "Xan_Lo", DM.ACTARM = "Xanomeline Low Dose", TA.ARMCD = "Xan_Hi", TA.ARM = "Xanomeline High Dose"
    *   矛盾の内容: DMドメインにおけるACTARMCD（Actual Arm Code）とACTARM（Description of Actual Arm）が、それぞれ "Xan_Lo"（Xanomeline Low Dose）となっています。一方、Trial Arms (TA)ドメインでは、"Xan_Hi"（Xanomeline High Dose）の情報が提供されています。これは、被験者が実際に投与されたArmと、Trial Armsとして計画されたArmが一致していない可能性を示唆しています。
    *   問題点の原因（推測）:
        *   DMドメインのACTARMCDとACTARMへのデータ入力誤り。
        *   治験薬の割り当て（Randomization）手続きの不備、または実施計画書からの逸脱。
    *   対応策（提案）:
        1.  DMドメインに記録されているACTARMCDおよびACTARMの値が正しいか、治験の割付記録と照合する。
        2.  TAドメインに記録されている情報が、DMドメインに正しく反映されているか確認する。

*   問題No.3:
    *   変数名と値: AE.AETERM = "AGITATION"
    *   矛盾の内容:
        *   AEドメインにはAgitation（激越）という有害事象が報告されています。しかし、NPI-XのQuestionnaires (QS)ドメインにおいて、関連する評価項目（NPITM03: Agitation/Aggression）のスコアがBaselineからWeek2にかけて減少しています。
        *   RELREC.RELIDがAE.AETERMと一致していない
    *   問題点の原因（推測）:
        *   NPI-Xは介護者が回答するため、評価時点での患者の状態と介護者の認識にずれが生じている可能性がある。
        *   有害事象の詳細な情報（重症度、発現期間など）が不足しているため、NPI-Xとの関連性を正確に評価できない。
        *   RELREC.RELIDの命名規則が不明確。
    *   対応策（提案）:
        1.  有害事象（Agitation）の重症度、発現時期、持続期間、処置内容などの詳細情報を収集し、NPI-Xのスコア変動との関連性を検討する。
        2.  NPI-X調査時の患者の状態について、詳細な情報を収集する。
        3.  RELREC.RELIDの命名規則を確認し、必要に応じて修正する。

クエリの作成:

*   患者ID: 01-701-1181
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMSTDTC = "1985", CM.CMENDTC = "" (Null) (複数レコード)
        *   医療機関への問い合わせ文面:
            *   CMドメインにおいて、CMSTDTC（Concomitant Medicationの開始日）が1985年と記録されているMedicationについて、現在も継続して服用しているか、いつ服用を中止したか教えてください。
        *   判断理由:
            *   Medicationの服用期間は、有害事象の評価や、試験結果に影響を与える可能性があるため。

*   患者ID: 01-701-1181
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: DM.ACTARMCD = "Xan_Lo", DM.ACTARM = "Xanomeline Low Dose", TA.ARMCD = "Xan_Hi", TA.ARM = "Xanomeline High Dose"
        *   医療機関への問い合わせ文面:
            *   DMドメインにおいて、治験薬のACTARM（Description of Actual Arm）が "Xanomeline Low Dose" と記録されています。この患者は、プロトコルで計画された治験薬と異なるものが投与された可能性があります。実際に投与された治験薬の内容と、その理由を教えてください。
        *   判断理由:
            *   治験薬の投与内容は、主要評価項目に直接影響を与えるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1181
  * 逸脱No.: 1
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMSTDTC = 1985
    * 逸脱内容: 併用薬（CALCIUM MAGNESIUM, POTASSIUM, TYLENOL, VITAMIN C）のCMSTDTCに1985が記録されています。1985は⻑すぎる過去の日付であり、データの信憑性に疑義が残ります。
    * プロトコル該当箇所: プロトコルに併用薬の期間に関する規定はないため、逸脱とは断定できません。
    * 判断理由: CMSTDTCは併用薬の開始⽇を記録するフィールドですが、⻑すぎる過去の年が記録されているため、データの誤記の可能性があります。

  * 逸脱No.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMENDTC = 2012-06-04, CMSTDTC = 2013-11-26
    * 逸脱内容: 併用薬（VITAMIN E）のCMENDTCが2012-06-04であり、CMSTDTC（2013-11-26）よりも過去の日付です。
    * プロトコル該当箇所: プロトコルに併用薬の期間に関する規定はないため、逸脱とは断定できません。
    * 判断理由: CMENDTCは併用薬の終了⽇を記録するフィールドですが、CMSTDTCよりも過去の日付が記録されているため、データの誤記の可能性があります。

  * 逸脱No.: 3
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: DM.ACTARMCD = Xan_Lo, EX.EXTRT = XANOMELINE
    * 逸脱内容: USUBJIDが01-701-1181の被験者は、DMドメインにおいて計画されたARM（DM.ARMCD）がXan_Hi（Xanomeline High Dose）であるにもかかわらず、実際に投与された薬剤（EX.EXTRT）がXANOMELINE 54mgであり、ACTARMCD（Xan_Lo）と一致していません。
    * プロトコル該当箇所: 3.6 Dosage and Administration
    * 判断理由: DM.ARMCDとEX.EXTRTの不一致は、被験者がプロトコルに違反した治療を受けている可能性を示唆します。DM.ARMCDは計画された治療群を、EX.EXTRTは実際に投与された治療を反映するため、これらが一致しない場合、投与計画からの逸脱が疑われます。

  * 逸脱No.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AESTDTC = 2013-12-09, EX.EXSTDTC = 2013-12-05
    * 逸脱内容: AE（有害事象）のAESTDTC（有害事象開始日）が2013-12-09であり、EX（投与）のEXSTDTC（投与開始日）2013-12-05より後です。
    * プロトコル該当箇所: プロトコルに有害事象の発生時期に関する規定はないため、逸脱とは断定できません。
    * 判断理由: 
AESTDTCは有害事象が発⽣した⽇を記録するフィールドであり、EXSTDTC（治験薬の投与開始⽇）より後の日付であることは矛盾しません。ただし、有害事象が投与開始前に発⽣した場合、データの誤記の可能性があります。

  * 逸脱No.: 5
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MHDTC = 2013-11-26
    * 逸脱内容: 選択基準INCL02に「NINCDSおよびADRDAガイドラインで定義された、考えられるADの診断」と規定されていますが、MHにALZHEIMER'S DISEASEの既往歴が登録されているため、組み入れ基準を満たしているか確認が必要です。
    * プロトコル該当箇所: 3.4.2.1 Inclusion Criteria
    * 判断理由: 
ADの診断基準を満たす必要がありますが、Medical HistoryにADの既往歴があると、現在の状態を正確に評価できているか疑念が残るため、選択基準を満たしているかどうかの確認が必要です。

  * 逸脱No.: 6
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: QS.QSTESTCD = MHITM04, QSORRES = PRESENT
    * 逸脱内容: QSドメインのModified Hachinski Ischemic Scoreにおいて、MHITM04（Nocturnal Confusion）がPRESENTと記録されています。Modified Hachinski Ischemic Scaleは虚血性病変の存在を示す指標であり、スコアが高いほど血管性認知症の可能性が高まります。
    * プロトコル該当箇所: 3.4.2.1 Inclusion Criteria
    * 判断理由: 
組み入れ基準INCL04にて、Modified Hachinski Ischemic Scale scoreが4以下であることが求められています。Nocturnal Confusionの存在はスコアを増加させる可能性があり、組み入れ基準を満たさない可能性があります。

    
*   **患者ID:** 01-701-1181
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** DM.ARMCD = Xan_Hi, EX.EXTRT = XANOMELINE
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1181について、DMドメインに記録されている計画された治療群（ARMCD）と、実際に投与された治験薬（EXTRT）が異なっている原因を教えてください。
            *   治験薬の投与量、投与期間、投与経路に誤りがないか確認してください。
        *   **判断理由:**
            *   DM.ARMCDとEX.EXTRTの不一致は、治験薬の誤投与を示唆する可能性があり、臨床試験の主要評価項目に影響を与える可能性があります。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.QSTESTCD = MHITM04, QSORRES = PRESENT
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1181のModified Hachinski Ischemic Scaleの各項目の評価根拠を教えてください。
            *   特に、MHITM04（Nocturnal Confusion）がPRESENTと評価された理由について、具体的な臨床所見や検査結果などの詳細情報を提供してください。
            *   Modified Hachinski Ischemic Scaleの合計スコアを算出し、4以下であることを確認してください。
        *   **判断理由:**
            *   Modified Hachinski Ischemic Scaleのスコアが組み入れ基準を満たしているか確認することは、対象集団の適切性を保証するために重要です。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CMSTDTC = 1985, CMENDTC = 2012-06-04, 2013-11-26
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1181が報告した併用薬の開始日（CMSTDTC）と終了日（CMENDTC）について、記録に誤りがないか確認してください。
            *   特に、CALCIUM MAGNESIUM, POTASSIUM, TYLENOL, VITAMIN CのCMSTDTCが1985年、VITAMIN EのCMENDTCが2012年6月4日となっている点について、その理由をご説明ください。
            *   正確な開始日と終了日が不明な場合は、その旨を報告してください。
        *   **判断理由:**
            *   併用薬の正確な開始日と終了日を把握することは、安全性評価や薬物相互作用の評価において重要です。誤った日付が記録されている場合、正確な評価が困難になる可能性があります。


# 01-703-1335
## Task1: Clinical Review Results
**1. 症例サマリー:**

*   **患者ID:** 01-703-1335
    *   2013年12月28日 (Day -79): スクリーニング検査で、Albumin 3.8 g/dL, Alkaline Phosphatase 55 U/L, Alanine Aminotransferase 22 U/L, Aspartate Aminotransferase 26 U/L, Bilirubin 0.4 mg/dL, Blood Urea Nitrogen 17 mg/dL, Calcium 9.4 mg/dL, Cholesterol 237 mg/dL, Creatine Kinase 153 U/L, Glucose 105 mg/dL, Phosphate 4.5 mg/dL, Protein 6.9 g/dL, Urate 4.9 mg/dL, Color N, Ketones 0, pH 5.0, Specific Gravity 1.019, Urobilinogen 0 と測定された。
    *   2014年02月21日 (Day -24): スケジュール外検査で、Albumin 3.7 g/dL, Alkaline Phosphatase 51 U/L, Alanine Aminotransferase 24 U/L, Aspartate Aminotransferase 24 U/L, Basophils 0.07 THOU/uL, Bilirubin 0.4 mg/dL, Blood Urea Nitrogen 18 mg/dL, Calcium 9.3 mg/dL, Cholesterol 258 mg/dL, Creatine Kinase 209 U/L (High), Chloride 111 mEq/L, Creatinine 1.2 mg/dL, Eosinophils 0.06 THOU/uL, Gamma Glutamyl Transferase 15 U/L, Glucose 96 mg/dL, Hematocrit 41.0 %, Hemoglobin 13.4 g/dL, Potassium 4.9 mEq/L, Ketones 0, Lymphocytes 1.77 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 32 g/dL, Ery. Mean Corpuscular Volume 93 fL, Monocytes 0.36 THOU/uL, Sodium 145 mEq/L, pH 5.0, Phosphate 4.6 mg/dL, Platelet 342 THOU/uL, Protein 6.9 g/dL, Erythrocytes 4.40 MILL/uL, Specific Gravity 1.011, Thyrotropin 0.87 uIU/mL, Urate 4.8 mg/dL, Urobilinogen 0, Vitamin B12 287 pg/mL, Leukocytes 7.01 THOU/uL と測定された。
    *   2014年03月15日 (Day -2): Multiple Sclerosis Relapse と Atrioventricular Block Second Degree の有害事象が発生。
    *   2014年03月17日 (Day 1): Xanomeline 54 mg の投与開始。
    *   2014年03月30日 (Day 14): Atrioventricular Block Second Degree の有害事象が回復。
    *   2014年03月31日 (Day 15): Alkaline Phosphatase 59 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 23 U/L, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 17 mg/dL, Calcium 9.7 mg/dL, Cholesterol 253 mg/dL, Creatine Kinase 219 U/L (High), Chloride 99 mEq/L, Creatinine 1.3 mg/dL, Eosinophils 0.04 THOU/uL, Gamma Glutamyl Transferase 15 U/L, Glucose 66 mg/dL, Hematocrit 43.0 %, Hemoglobin 14.2 g/dL, Potassium 4.3 mEq/L, Ketones 0, Lymphocytes 1.86 THOU/uL, Ery. Mean Corpuscular Hemoglobin 30 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 91 fL, Monocytes 0.50 THOU/uL, Sodium 137 mEq/L, pH 5.0, Phosphate 3.9 mg/dL, Platelet 328 THOU/uL, Protein 7.8 g/dL, Erythrocytes 4.70 MILL/uL, Specific Gravity 1.026, Urate 4.9 mg/dL, Urobilinogen 0, Leukocytes 7.88 THOU/uL と測定された。
    *    2014年03月31日 (Day 15):  Delusions: FREQUENCY 2, SEVERITY 1, DISTRESS 1, Score 2。 AGITATION/AGRESSION: FREQUENCY 3, SEVERITY 1, DISTRESS 2, Score 3。 DEPRESSION/DYSPHORIA: FREQUENCY 2, SEVERITY 1, DISTRESS 0, Score 2。
    *   2014年04月01日 (Day 16): Xanomeline 81 mg の投与開始。
    *   2014年04月13日 (Day 28): Alkaline Phosphatase 55 U/L, Alanine Aminotransferase 25 U/L, Aspartate Aminotransferase 25 U/L, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 19 mg/dL, Calcium 9.3 mg/dL, Cholesterol 219 mg/dL, Creatine Kinase 134 U/L, Chloride 103 mEq/L, Creatinine 1.2 mg/dL, Eosinophils 0.03 THOU/uL, Gamma Glutamyl Transferase 17 U/L, Glucose 101 mg/dL, Hematocrit 39.0 %, Hemoglobin 13.7 g/dL, Potassium 3.8 mEq/L, Ketones 0, Lymphocytes 1.48 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 87 fL, Monocytes 0.44 THOU/uL, Sodium 138 mEq/L, pH 5.0, Phosphate 3.7 mg/dL, Platelet 320 THOU/uL, Protein 6.9 g/dL, Erythrocytes 4.50 MILL/uL, Specific Gravity 1.026, Urate 4.9 mg/dL, Urobilinogen 0, Leukocytes 7.42 THOU/uL と測定された。
    *  2014年04月13日 (Day 28): AGITATION/AGRESSION: FREQUENCY 4, SEVERITY 3, DISTRESS 4, Score 12
    *   2014年05月01日 (Day 46): Multiple Sclerosis Relapse の有害事象が終了。
    *   2014年05月24日 (Day 69): Albumin 3.7 g/dL, Alkaline Phosphatase 57 U/L, Alanine Aminotransferase 17 U/L, Aspartate Aminotransferase 14 U/L, Bilirubin 0.4 mg/dL, Blood Urea Nitrogen 19 mg/dL, Calcium 9.1 mg/dL, Cholesterol 262 mg/dL, Creatine Kinase 105 U/L, Chloride 107 mEq/L, Creatinine 1.1 mg/dL, Eosinophils 0.05 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 81 mg/dL, Hematocrit 43.0 %, Hemoglobin 14.3 g/dL, Potassium 4.2 mEq/L, Ketones 0, Lymphocytes 1.56 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 92 fL, Monocytes 0.34 THOU/uL, Sodium 145 mEq/L, pH 5.0, Phosphate 4.1 mg/dL, Platelet 320 THOU/uL, Protein 6.8 g/dL, Erythrocytes 4.70 MILL/uL, Specific Gravity 1.016, Urate 3.8 mg/dL, Urobilinogen 0, Leukocytes 6.67 THOU/uL, WORD RECALL TASK 10, NAMING OBJECTS AND FINGERS (REFER TO 5 C 3, DELAYED WORD RECALL 10, COMMANDS 4, CONSTRUCTIONAL PRAXIS 3, IDEATIONAL PRAXIS 4, ORIENTATION 7, MAZE SOLUTION 240 sec, SPOKEN LANGUAGE ABILITY 5, COMPREHENSION OF SPOKEN LANGUAGE 5, WORD FINDING DIFFICULTY IN SPONTANEOUS S 5, RECALL OF TEST INSTRUCTIONS 5, ADAS-COG(11) Subscore 61.5, EXTENT OF CHANGE, IF ANY, SINCE BASELINE MINIMAL WORSENING 5, UNDERTAKE TO WASH HIMSELF/HERSELF N 0, NEUROPSYCHIATRIC INVENTORY - REVISED (NPI-X)  DISTRESS 3 と測定された。

---

**2. クエリの作成 (必要な場合のみ):**

*   **患者ID:** 01-703-1335
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = 2014-03-15, AE.AEENDTC = 2014-03-30, EX.EXSTDTC = 2014-03-17
        *   **医療機関への問い合わせ文面:**
            *   有害事象「Atrioventricular Block Second Degree」のAESTDTCが2014-03-15、治験薬のEXSTDTCが2014-03-17となっています。AESTDTCとEXSTDTCの整合性を確認してください。
        *   **判断理由:**
            *   有害事象発生日が治験薬投与開始日より前になっているため、因果関係の評価に影響を及ぼす可能性があります。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** DS.DSDTC = 2014-05-24, LB.LBDTC = 2014-05-24, AE.AEENDTC = 2014-05-01, VS.VSDTC = 2014-05-24, QS.QSDTC = 2014-05-24, EX.EXENDTC = 2014-05-07
        *   **医療機関への問い合わせ文面:**
            *   最終観察日（DS.DSDTC, LB.LBDTC, VS.VSDTC, QS.QSDTC）は2014-05-24ですが、治験薬のEXENDTCは2014-05-07となっています。最終投与日と観察日の整合性を確認してください。
        *   **判断理由:**
            *   複数のドメインで日付の矛盾が発生しています。プロトコル違反に繋がる可能性もあります。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSTERM = "PROTOCOL VIOLATION"
        *   **医療機関への問い合わせ文面:**
            *   治験中止理由が「PROTOCOL VIOLATION」となっています。違反内容の詳細について教えてください。
        *   **判断理由:**
            *   プロトコルからの逸脱は、試験結果の解釈に影響を与える可能性があります。
    *   **クエリNo.:** 4
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE"
        *   **医療機関への問い合わせ文面:**
            *   既往歴に「ALZHEIMER'S DISEASE」の記載がありますが、有害事象として「MULTIPLE SCLEROSIS RELAPSE」が報告されています。多発性硬化症の既往歴の有無と、今回の再発が試験に与える影響について評価してください。
        *   **判断理由:**
            *  多発性硬化症は除外基準に該当する可能性があり、安全性に影響を及ぼす可能性があるため、確認が必要です。


## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: AE.AESTDTC, AE.AEENDTC, DM.DMDY, DS.DSSTDY, EX.EXENDTC, LB.LBDY, MH.MHDY, QS.QSDY, SV.VISITDY, VS.VSDY

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** AE.AESTDTC = 2014-03-15, AE.AEENDTC = 2014-03-30
    *   **矛盾の内容:** USUBJIDが"01-703-1335"の被験者において、AESEQ=2の有害事象のAEENDTCがAESTDTCよりも前の日付になっている。
    *   **問題点の原因（推測）:** データ入力エラー
    *   **対応策（提案）:** 
    1.  原資料を確認する。
    2.  AEENDTCとAESTDTCの日付が正しいことを確認する。
    3.  日付が誤っている場合は修正する。

*   **問題No.2:**
    *   **変数名と値:** AE.AESTDTC = 2014-04-01, AE.AEENDTC = 2014-05-01
    *   **矛盾の内容:** USUBJIDが"01-703-1335"の被験者において、AESEQ=1の有害事象MULTIPLE SCLEROSIS RELAPSEとATRIOVENTRICULAR BLOCK SECOND DEGREEが同時に発生している。MHTERMにALZHEIMER'S DISEASEとVERBATIM_1309(ARTHRITIS)のMedical Historyがある状態で、MULTIPLE SCLEROSIS RELAPSEが発症することは医学的に矛盾している可能性がある。
    *   **問題点の原因（推測）:** 
        1.  誤った有害事象の記録。
        2.  Medical Historyの記録の誤り。
        3.  被験者の状態に関する情報が不足している。
    *   **対応策（提案）:** 
        1.  原資料と照合し、AETERM、AESTDTC、AEENDTCが正しいか確認する。
        2.  MHTERMのALZHEIMER'S DISEASE、VERBATIM_1309(ARTHRITIS)の記載が正しいか確認する。
        3.  医療機関に問い合わせ、医学的な妥当性を確認する。

*   **問題No.3:**
    *   **変数名と値:** DM.DMDY = -17, DS.DSSTDY = 69, EX.EXENDY = 52, LB.LBDY = -79, MH.MHDY = -17, QS.QSDY = 69, SV.VISITDY = -7, VS.VSDY = -17
    *   **矛盾の内容:** 各ドメインにおいて、日付から計算されるべきDY変数が負の値をとっている。
    *   **問題点の原因（推測）:** RFSTDTCの値が正しくない。
    *   **対応策（提案）:**
        1.  DM.RFSTDTCの値が正しいか確認する。
        2.  Define.xmlに記載された、`COMPMETHOD.STUDY_DAY`の計算方法が正しいか確認する。

*   **問題No.4:**
    *   **変数名と値:** SV.VISIT = "AMBUL ECG PLACEMENT", SV.VISITDY = 13
    *   **矛盾の内容:** DS domainにPROTOCOL VIOLATIONが発生したのがWEEK6(VISITNUM=7)である一方、SV domainではAMBUL ECG PLACEMENTがWEEK2とWEEK4の間のタイミング(VISITNUM=3.5)で実施されている。
    *   **問題点の原因（推測）:** 
        1.  VISITの実施タイミングがプロトコルから逸脱している。
        2.  データ入力時の誤り。
        3.  スケジュールが被験者によって異なっている。
    *   **対応策（提案）:** 
        1.  SV domainに記録されているVISITの実施日(SVSTDTC)が正しいか、DM domainのRFSTDTCと合わせて確認する。
        2.  VISITの実施タイミングがプロトコルに準拠しているか確認する。

*   **問題No.5:**
    *   **変数名と値:** SV.VISIT = "WEEK 6", DS.DSTERM = "FINAL LAB VISIT", LB.VISIT = "WEEK 6", QS.VISIT = "WEEK 6", VS.VISIT = "WEEK 6"
    *   **矛盾の内容:** DS domainにFINAL LAB VISITが発生したのがWEEK6(VISITNUM=7)である一方、LB/QS/VS domainではWEEK6のデータが収集されている。
    *   **問題点の原因（推測）:** 
        1.  FINAL LAB VISITと、通常予定されていたWEEK6のVISITが、同じ日に実施されている。
        2.  FINAL LAB VISIT時に、本来は実施されないはずのLB/QS/VS domainのデータが収集されている。
        3.  データ入力時の誤り。
    *   **対応策（提案）:** 
        1.  DS domainに記録されているDSDTCと、LB/QS/VS domainに記録されているLBDTC/QSDTC/VSDTCを比較し、同じ日付かどうかを確認する。
        2.  DS domainにFINAL LAB VISITが発生した理由を確認する。
        3.  LB/QS/VS domainのデータが収集された理由を確認する。

*   **問題No.6:**
    *   **変数名と値:** QSTESTCD=NPITM03, QS.QSTEST = "AGITATION/AGRESSION PRESENT",  QS.QSORRES = "ABSENT"
    *   **矛盾の内容:** 
        - NPI-Xのデータにおいて、BASELINE(VISITNUM=3)ではAGITATION/AGRESSION PRESENTとなっている(NPITM03S=12)にもかかわらず、WEEK6(VISITNUM=7)ではABSENT(NPITM03S=0)となっている。
        - NPI-Xのデータにおいて、WEEK2(VISITNUM=4)で一旦スコアが低下(NPITM03S=3)するものの、WEEK4(VISITNUM=5)ではBASELINEと同じスコア(NPITM03S=12)まで戻っている。
    *   **問題点の原因（推測）:** 
        1.  ADの症状特性による自然変動。
        2.  評価者の主観による評価のばらつき。
        3.  データ入力時の誤り。
    *   **対応策（提案）:** 
        1.  NPI-Xのデータが正しく転記されているか原資料と照合する。
        2.  評価者に対して評価方法のトレーニングを実施する。

*   **問題No.7:**
    *   **変数名と値:** AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
    *   **矛盾の内容:** AE domainに報告されている有害事象ATRIOVENTRICULAR BLOCK SECOND DEGREEは、除外基準(16b)に抵触する可能性がある。
    *   **問題点の原因（推測）:** 
        1.  MEDICAL HISTORYに同様の疾患の記載がない。
        2.  ATRIOVENTRICULAR BLOCK SECOND DEGREEは、一過性のものだった。
        3.  データ入力時の誤り。
    *   **対応策（提案）:**
        1.  原資料を確認し、ATRIOVENTRICULAR BLOCK SECOND DEGREEのAETERM、AESTDTC、AEENDTC、AESEVが正しいか確認する。
        2.  詳細な心電図データを確認する。
        3.  除外基準に抵触するかどうか、治験責任医師に確認する。

**クエリの作成:**

*   **患者ID:** 01-703-1335
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC, AE.AEENDTC (不整合な日付)
        *   **医療機関への問い合わせ文面:** USUBJIDが"01-703-1335"の被験者の、AESEQ=2の有害事象について、AESTDTCとAEENDTCの日付が正しいか確認してください。もし日付が誤っている場合は、正しい日付をご教示ください。
        *   **判断理由:** 有害事象の期間が正しく評価されない可能性があるため。

*   **患者ID:** 01-703-1335
    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** AE.AETERM = "MULTIPLE SCLEROSIS RELAPSE", MH.MHTERM = "ALZHEIMER'S DISEASE"
        *   **医療機関への問い合わせ文面:** USUBJIDが"01-703-1335"の被験者について、Medical HistoryにALZHEIMER'S DISEASEの記載があるにもかかわらず、MULTIPLE SCLEROSIS RELAPSEがAdverse Eventとして報告されています。これらの情報の整合性をご確認ください。特に、MULTIPLE SCLEROSIS RELAPSEは本当に発生した事象なのか、また、既往歴にALZHEIMER'S DISEASEと診断されたことは正しかったのか、ご確認ください。
        *   **判断理由:** 
            1.  2つの事象の併発は医学的に矛盾している可能性があり、データの信頼性に影響を与えるため。
            2.  ADの評価項目への影響を考慮し、重要なデータと判断したため。

*   **患者ID:** 01-703-1335
    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = "ATRIOVENTRICULAR BLOCK SECOND DEGREE"
        *   **医療機関への問い合わせ文面:** USUBJIDが"01-703-1335"の被験者に発生した有害事象ATRIOVENTRICULAR BLOCK SECOND DEGREEについて、詳細な状況（発現日、重症度、持続時間、処置、転帰など）をご教示ください。特に、今回のATRIOVENTRICULAR BLOCK SECOND DEGREEは、(1)一過性のものであったのか (2) 慢性的なものなのか (3) 治験薬との因果関係はどのように評価されたか、について詳しくお教えください。
        *   **判断理由:** 
            1.  ATRIOVENTRICULAR BLOCK SECOND DEGREEは、重篤な有害事象であり、治験薬の安全性評価に重要な情報であるため。
            2.  ATRIOVENTRICULAR BLOCK SECOND DEGREEが、治験への参加資格に影響を与える可能性があるため。

*   **患者ID:** 01-703-1335
    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSTERM = "PROTOCOL VIOLATION", SV.VISIT = "AMBUL ECG PLACEMENT"
        *   **医療機関への問い合わせ文面:** USUBJIDが"01-703-1335"の被験者について、DS domainにPROTOCOL VIOLATIONが発生した時期と、SV domainにAMBUL ECG PLACEMENTを実施した時期に矛盾がないか確認してください。もし矛盾がある場合、正しい時期をご教示ください。
        *   **判断理由:** プロトコルからの逸脱はデータの解釈に影響を与える可能性があるため。


## Task3: Protocol Deviation Review Results
患者ID: 01-703-1335
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: DSDECOD = "PROTOCOL VIOLATION", DSDTC = "2014-05-24", DSSTDY = 69, AGE = 67, ARMCD = "Xan_Hi"
    *   逸脱内容: 67歳の患者が、Xanomeline High Dose群に割り付けられているにもかかわらず、PROTOCOL VIOLATIONによりWEEK 6 (Study Day 69) に試験を中止している。プロトコルには、試験薬の中止基準に関する詳細な記述がないため、逸脱の程度をMajorと判断した。
    *   プロトコル該当箇所: 3.10 Patient Disposition Criteria
    *   判断理由: DSデータセットには、試験からの脱落事由が記録されている。USUBJIDが"01-703-1335"の被験者は、「PROTOCOL VIOLATION」により試験を中止している。この情報と、DMデータセットに記録された年齢、割り付けられた試験薬の情報から、プロトコルからの逸脱を検出した。
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: DSDECOD = "PROTOCOL VIOLATION", DSDTC = "2014-05-24", DSSTDY = 69
    *   医療機関への問い合わせ文面:
        *   被験者01-703-1335がWEEK 6 (Study Day 69) にPROTOCOL VIOLATIONを理由に試験を中止したとのことですが、具体的な理由をご教示ください。
        *   PROTOCOL VIOLATIONの内容が、本試験の評価項目に影響を与える可能性のあるものかご教示ください。
        *   治験薬の投与を継続した場合、被験者の安全性に影響を与える可能性はありましたか？
    *   判断理由: 
    DSデータセットには、試験からの脱落事由として「PROTOCOL VIOLATION」と記録されているが、具体的な内容が不明である。この内容によっては、本試験の評価項目に影響を与える可能性があるため、重要度の高いクエリとして作成した。
クエリなし


# 01-701-1028
## Task1: Clinical Review Results
## 1. 症例サマリーの作成:

**患者ID:** 01-701-1028

*   **2013年07月11日 (Day -8):** スクリーニング1回目の検査で、Ery. Mean Corpuscular Hemoglobin (MCH) が基準値上限を超えて37 pg (基準値: 26-34 pg) と高い。Ery. Mean Corpuscular Volume (MCV) が基準値上限を超えて104 fL (基準値: 80-100 fL) と高い。
*   **2013年11月06日 (Day 111):** Week16の検査で、AnisocytesとMacrocytesが認められる。Calciumが基準値下限を下回り8.0 mg/dL (基準値: 8.4-10.3 mg/dL) と低い。

---

## 2. クエリの作成:

**患者ID:** 01-701-1028

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   LB.LBDTC (Anisocytes): 2013-11-06T10:08
        *   LB.LBTESTCD (Aniso): ANISO
        *   LB.LBORRES (Aniso): 1
        *   LB.LBNRIND (Aniso): ABNORMAL
        *   LB.LBDTC (Macrocytes): 2013-11-06T10:08
        *   LB.LBTESTCD (Macrocytes): MACROCY
        *   LB.LBORRES (Macrocytes): 1
        *   LB.LBNRIND (Macrocytes): ABNORMAL
    *   **医療機関への問い合わせ文面:** Week 16 (2013年11月06日) の検査において、AnisocytesとMacrocytesが確認されました。これらの細胞が確認された原因について、医学的に考えられる理由をご教示ください。また、これらは治験薬と関連があると考えられますか？
    *   **判断理由:** AnisocytesとMacrocytesは通常、正常な血液中には存在しない異常な赤血球です。貧血、鉄欠乏、ビタミンB12欠乏などが原因として考えられます。治験薬との関連性を評価するため、医療機関への確認が必要です。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   LB.LBDTC (Calcium): 2013-11-06T10:08
        *   LB.LBTESTCD (Calcium): CA
        *   LB.LBORRES (Calcium): 8.0
        *   LB.LBORNRHI (Calcium): 8.4
        *   LB.LBNRIND (Calcium): LOW
    *   **医療機関への問い合わせ文面:** Week 16 (2013年11月06日) の検査において、血清カルシウム値が基準範囲を下回っています。カルシウム低下の原因について、医学的に考えられる理由をご教示ください。また、治験薬と関連があると考えられますか？
    *   **判断理由:** 低カルシウム血症は、副甲状腺機能低下症、ビタミンD欠乏、腎不全など、様々な原因で起こり得ます。神経機能や心機能に影響を与える可能性があるため、治験薬との関連性を評価する必要があります。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   AE.AETERM: PARKINSON'S DISEASE
        *   AE.AESTDTC: 2013-07-01
        *   AE.AEENDTC: "" (NULL)
    *   **医療機関への問い合わせ文面:** 報告されている有害事象「パーキンソン病」はMedical Historyに登録されているALZHEIMER'S DISEASEとデータ登録間違いではないか確認してください。
    *   **判断理由:** 
MHのデータに「ALZHEIMER'S DISEASE」の登録があるため、AEの「PARKINSON'S DISEASE」が誤りである可能性を考慮しました。

## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMTRT, AE.AESTDTC, EX.EXSTDTC, LB.LBDTC, MH.MHTERM

**問題点:**

*   **問題No.1:**
    *   **変数名と値:** CM.CMTRT = "CENTRUM", CM.CMSTDTC = "2013-04"
    *   **矛盾の内容:** CMSTDTCがYYYY-MM形式で記録されているが、DM.RFSTDTC="2013-07-19"であり、治験薬投与開始前に服用している併用薬の開始日として不適切。また、CMSTDTCが2013年4月であるにもかかわらず、VISITNUMが1（SCREENING 1, 2013-07-11）から13（WEEK 26, 2014-01-14）まで記録されており、投薬期間と矛盾している。
*   **問題点の原因（推測）:** CMSTDTCの日付入力ミス。
*   **対応策（提案）:** CMSTDTCの正しい日付を確認し修正する。または、CENTRUMの服用状況について治験担当医師に確認する。

*   **問題No.2:**
    *   **変数名と値:** AE.AETERM = "PARKINSON'S DISEASE", AESTDTC = "2013-07-01"
    *   **矛盾の内容:** AETERMが「PARKINSON'S DISEASE」となっているが、これはMedDRAのLLTではなく、既往歴（MH）として記録されるべき情報である。Medical History (MH)に「ALZHEIMER'S DISEASE」の既往歴があることと、AEに「PARKINSON'S DISEASE」が記録されていることも矛盾している可能性がある。
*   **問題点の原因（推測）:** AETERMの選択ミス。
*   **対応策（提案）:** AETERMの妥当性を確認し、必要であればMedical Historyに登録する。

*   **問題No.3:**
    *   **変数名と値:** EX.EXSTDTC = "2013-07-19", EXENDTC = "2013-08-01" と EX.EXSTDTC = "2014-01-07", EXENDTC = "2014-01-14"
    *   **矛盾の内容:** Xanomelineの投与期間がそれぞれ14日間と7日間となっており、週単位のVISIT情報と一致しない。TE.TEDUR="P2W"（2週間）と矛盾している。
*   **問題点の原因（推測）:** 投与期間の記録ミス、あるいは計画からの逸脱。
*   **対応策（提案）:** EXSTDTCとEXENDTCが正しく反映されているか、治験担当医師に確認する。

*   **問題No.4:**
    *   **変数名と値:** LB.LBDTCがWEEK 24で "2014-01-06T10:00"、WEEK 26で "2014-01-14T11:10"。
    *   **矛盾の内容:** DS.DSDTCとLB.LBDTCの日付が一部一致しない。具体的には、WEEK26（最終投与日）のLBTMTCが2014-01-14となっているが、DS.DSDTC(DSTERM=FINAL LAB VISIT)も2014-01-14であり、最終検査が最終投与日と同時に行われたことを示唆する。一般的に最終検査は投与終了後に行われるため、矛盾している可能性がある。
*   **問題点の原因（推測）:** データ入力ミス、または検査実施日の誤り。
*   **対応策（提案）:** 最終検査日（LB.LBDTC）と最終投与日（EX.EXENDTC）の整合性を確認する。

*   **問題No.5:**
    *   **変数名と値:** DM.MHSTDTC = "2009-12-16"
    *   **矛盾の内容:** 6行目の「ALZHEIMER'S DISEASE」の既往歴にMHSTDTC="2009-12-16"という具体的な日付が記録されている。
*   **問題点の原因（推測）:** 遡及的な問診による、詳細な問診情報の取得。
*   **対応策（提案）:** 特に問題はないが、詳細な既往歴の起点を記録することの妥当性を確認する。

*   **問題No.6:**
    *   **変数名と値:** LB domainのHEMATOLOGYにおいて、POLYCHR, MACROCY, ANISO等、検査コードがABNORMALと評価されている。
    *   **矛盾の内容:** ABNORMALがAE domainに報告されていない。
*   **問題点の原因（推測）:** 
        *   AE報告基準に達していない軽微な異常、または
        *   AEと判断されなかった理由が存在。
*   **対応策（提案）:**
        *   ANISO, MACROCY, POLYCHRの異常値について、治験担当医師にAEとして報告すべきかどうか確認する。
        *   報告されない場合、その判断基準を明確化する。

**クエリの作成:**

*   **患者ID:** 01-701-1028
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMTRT = "CENTRUM", CM.CMSTDTC = "2013-04"
        *   **医療機関への問い合わせ文面:**
            *   被験者01-701-1028の併用薬CENTRUMの開始日について、記録された2013年4月という日付は正確ですか？
            *   正確でない場合、正しい開始年月日をご教示ください。
            *   2013年7月11日以前にCENTRUMを服用していた場合、投与期間とVISIT情報との整合性についてご説明ください。
        *   **判断理由:** CMSTDTCの不整合は、併用薬の評価に影響を及ぼし、ひいては試験結果の解釈に影響を与える可能性があるため。

    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** AE.AETERM = "PARKINSON'S DISEASE", AESTDTC = "2013-07-01"
        *   **医療機関への問い合わせ文面:**
            *   有害事象として報告された「PARKINSON'S DISEASE」は、Medical Historyの間違いではないか確認してください。
            *  Medical Historyに記録されているALZHEIMER'S DISEASEと矛盾がないか確認してください。
        *   **判断理由:** 正確な既往歴と有害事象の把握は、安全性評価において重要であるため。

    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** EX.EXSTDTC = "2013-07-19", EXENDTC = "2013-08-01" と EX.EXSTDTC = "2014-01-07", EXENDTC = "2014-01-14"
        *   **医療機関への問い合わせ文面:**
            *   治験薬Xanomelineの投与期間について、EX domainに記録されている開始日と終了日が、VISIT情報（2週間ごと）と一致しているか確認してください。
            *  もし投与計画からの逸脱があった場合は、その理由と詳細についてご説明ください。
        *   **判断理由:** 治験薬の投与期間は主要な評価項目に影響を与える可能性があり、データの正確性が重要であるため。

    *   **クエリNo.4:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB domainのHEMATOLOGYにおいて、POLYCHR, MACROCY, ANISO等、検査コードがABNORMALと評価。
        *   **医療機関への問い合わせ文面:**
            *   血液検査の結果、POLYCHR(多染色性赤血球), MACROCY(大赤血球症), ANISO(不同赤血球症)などの異常値が確認されました。
            *  これらの異常値は、有害事象として報告すべきものでしょうか？もしそうでない場合、その理由をご説明ください。
        *   **判断理由:** AE domainとLB domainの情報の整合性を高めることで、より正確な安全性評価に貢献するため。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1028

逸脱No.: 1
臨床試験結果への影響度合い: Minor
変数名と値: DM.DMDY = -8
逸脱内容: DM.DMDYの値が負の値(-8)で、データの収集日(DMDTC)が基準日(RFSTDTC)より前になっている。DMドメインのDMDYは、データの収集日(DMDTC)から患者の基準開始日(RFSTDTC)までの日数を表すため、正の値または0である必要があります。
プロトコル該当箇所: SDTMIG 3.1.2のDMドメインに関する記述
判断理由: DM.DMDYは、DMドメインの定義において、データの収集日(DMCDTC)から患者の基準開始日(RFSTDTC)までの日数を表す必要があります。DMDYが負の値であることは、データ収集日が基準開始日より前であることを意味し、これは定義に反します。

逸脱No.: 2
臨床試験結果への影響度合い: Minor
変数名と値: LB.LBDTC = "2014-01-06T10:00", LB.LBDY = 172
逸脱内容: LB.LBDTCの日付(2014-01-06)から計算されるべきLB.LBDYの値が172であるのに対し、実際には168日後であるべきです。
プロトコル該当箇所: SDTMIG 3.1.2のLBドメインに関する記述、COMPMETHOD.STUDY_DAY
判断理由: LB.LBDYは、LBドメインの定義において、LBDTCから試験開始日(RFSTDTC)までの日数を表す必要があります。LBDTCの日付とLBDYの値に矛盾が見られるため逸脱と判断しました。

逸脱No.: 3
臨床試験結果への影響度合い: Minor
変数名と値: LB.LBDTC = "2013-08-14T13:24", LB.LBDY = 27
逸脱内容: LB.LBDTCの日付(2013-08-14)から計算されるべきLB.LBDYの値が27であるのに対し、実際には26日後であるべきです。
プロトコル該当箇所: SDTMIG 3.1.2のLBドメインに関する記述、COMPMETHOD.STUDY_DAY
判断理由: LB.LBDYは、LBドメインの定義において、LBDTCから試験開始日(RFSTDTC)までの日数を表す必要があります。LBDTCの日付とLBDYの値に矛盾が見られるため逸脱と判断しました。

患者ID: 01-701-1028
クエリNo.: 1
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMDECOD = "UNCODED"
医療機関への問い合わせ文面: 
Concomitant Medications(CM)ドメインにおいて、被験者(USUBJID)=01-701-1028のCMTRT(Reported Name of Drug, Med, or Therapy)=CENTRUMのCMDECOD(Standardized Medication Name)がUNCODEDとなっています。CENTRUMの標準化されたMedDRAコードをご教示ください。
判断理由: CMDECODはMedDRA等の標準化された辞書を用いてコーディングされるべきですが、UNCODEDとなっているため、より詳細な情報の収集が必要です。標準化されたMedDRAコードを確認することで、データ品質の向上に繋がります。

患者ID: 01-701-1028
クエリNo.: 2
臨床試験結果への影響度合い: None
変数名と値: MH.MHDECOD = ""
医療機関への問い合わせ文面: 
Medical History(MH)ドメインにおいて、被験者(USUBJID)=01-701-1028のMHTERM(Reported Term for the Medical History)=ALZHEIMER'S DISEASEのMHDECOD(Dictionary-Derived Term)が空欄となっています。ALZHEIMER'S DISEASEの標準化されたMedDRAコードをご教示ください。
判断理由: MHDECODはMedDRA等の標準化された辞書を用いてコーディングされるべきですが、空欄となっているため、より詳細な情報の収集が必要です。標準化されたMedDRAコードを確認することで、データ品質の向上に繋がります。

患者ID: 01-701-1028
クエリNo.: 3
臨床試験結果への影響度合い: None
変数名と値: MH.MHDECOD = ""
医療機関への問い合わせ文面: 
Medical History(MH)ドメインにおいて、被験者(USUBJID)=01-701-1028のMHTERM(Reported Term for the Medical History)=VERBATIM_1006のMHDECOD(Dictionary-Derived Term)が空欄となっています。LIPECTOMYの標準化されたMedDRAコードをご教示ください。
判断理由: MHDECODはMedDRA等の標準化された辞書を用いてコーディングされるべきですが、空欄となっているため、より詳細な情報の収集が必要です。標準化されたMedDRAコードを確認することで、データ品質の向上に繋がります。

患者ID: 01-701-1028
クエリNo.: 4
臨床試験結果への影響度合い: None
変数名と値: MH.MHDECOD = ""
医療機関への問い合わせ文面: 
Medical History(MH)ドメインにおいて、被験者(USUBJID)=01-701-1028のMHTERM(Reported Term for the Medical History)=VERBATIM_1775のMHDECOD(Dictionary-Derived Term)が空欄となっています。APPENDECTOMYの標準化されたMedDRAコードをご教示ください。
判断理由: MHDECODはMedDRA等の標準化された辞書を用いてコーディングされるべきですが、空欄となっているため、より詳細な情報の収集が必要です。標準化されたMedDRAコードを確認することで、データ品質の向上に繋がります。


# 01-703-1258
## Task1: Clinical Review Results
患者ID: 01-703-1258

*   2012年07月10日 (Day -10): ALT 43 U/L (基準範囲 6-32 U/L), AST 36 U/L (基準範囲 9-34 U/L), EOS 0.59 THOU/uL (基準範囲 0-0.57 THOU/uL), SPGRAV 1.032 (基準範囲 1.006-1.03)と基準値より高い。
*   2012年07月31日 (Day 12): MONO 1.07 THOU/uL (基準範囲 0.12-0.92 THOU/uL)と基準値より高い。
*   2012年08月01日 (Day 13): DIZZINESS (DIZZINESS)が発現。
*   2012年08月11日 (Day 23): UPPER RESPIRATORY TRACT INFECTION (UPPER RESPIRATORY INFECTION)が発現。
*   2012年09月04日 (Day 47): APPLICATION SITE DERMATITIS (APPLICATION SITE RASH)が発現。
*   2012年09月14日 (Day 57): APPLICATION SITE DERMATITIS (APPLICATION SITE RASH)が発現。WBC 10.80 THOU/uL (基準範囲 3.8-10.7 THOU/uL)と基準値より高い。
*   2012年10月02日 (Day 75): DIZZINESS (DIZZINESS)が発現。
*   2013年01月21日 (Day 186): ADVERSE EVENT (ADVERSE EVENT)が発現。

---

患者ID: 01-703-1258

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AETERM = APPLICATION SITE DERMATITIS
        *   AE.AESTDTC = 2012-09-04
        *   AE.AEENDTC = 2013-01-25
    *   **医療機関への問い合わせ文面:**
        *   治験参加者のAPPLICATION SITE DERMATITISについて質問です。
        *   AE.AESTDTCとAE.AEENDTCに記録されているAPPLICATION SITE DERMATITISの期間について、より詳細な情報（発現日、症状、重症度、処置内容、転帰など）をご教示ください。
        *   APPLICATION SITE DERMATITISと診断された根拠についてご教示ください。
        *   本有害事象と治験薬の因果関係について、治験担当医師の見解をご教示ください。
    *   **判断理由:**
        *   APPLICATION SITE DERMATITISが4ヶ月以上に渡って継続しており、治験薬との関連が疑われるため、詳細を確認する必要がある。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AETERM = DIZZINESS
        *   AE.AESTDTC = 2012-08-01
        *   AE.AEENDTC = 2012-10-01
        *   AE.AESEV = SEVERE
    *   **医療機関への問い合わせ文面:**
        *   治験参加者のDIZZINESSについて質問です。
        *   AE.AESTDTCとAE.AEENDTCに記録されているDIZZINESSの期間について、より詳細な情報（発現日、症状、重症度、処置内容、転帰など）をご教示ください。
        *   DIZZINESSの重症度が「SEVERE」と判断された根拠についてご教示ください。
        *   DIZZINESSの原因、及び治験薬との因果関係について、治験担当医師の見解をご教示ください。
        *   必要に応じて神経学的検査は実施されましたか？実施された場合、結果をご教示ください。
    *   **判断理由:**
        *   DIZZINESSが重症であり、転倒等のリスクがあるため、詳細を確認する必要がある。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   LB.LBTESTCD = EOS
        *   LB.LBDTC (2012-07-10) = 0.59 THOU/uL (HIGH)
        *   LB.LBDTC (2012-09-04) = 0.90 THOU/uL (HIGH)
        *   LB.LBDTC (2012-09-14) = 1.09 THOU/uL (HIGH)
        *   LB.LBDTC (2012-10-09) = 0.75 THOU/uL (HIGH)
        *   LB.LBDTC (2012-11-05) = 0.70 THOU/uL (HIGH)
    *   **医療機関への問い合わせ文面:**
        *   治験参加者のEOS（好酸球）について質問です。
        *   好酸球が増加している原因について、治験担当医師の見解をご教示ください。
        *   何らかの基礎疾患、アレルギー、寄生虫感染症、または薬剤による影響は考えられますか？
        *   好酸球増加に対する処置は行われましたか？
    *   **判断理由:**
        *   好酸球増加が持続しており、APPLICATION SITE DERMATITISとの関連も考えられるため、詳細を確認する必要がある。

*   **クエリNo.:** 4
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:**
        *   VS.VSTESTCD = SYSBP
        *   VS.VSDTC (2012-07-10) = 164 mmHg
    *   **医療機関への問い合わせ文面:**
        *   治験参加者のSYSBP（収縮期血圧）について質問です。
        *   スクリーニング検査（2012-07-10）において、立位での収縮期血圧が164mmHgと高値ですが、高血圧の既往歴（MHドメイン）に矛盾はありませんか？
        *   TIMOPTIC（CMドメイン）はβ遮断薬ですが、β遮断薬を使用しているにも関わらず、スクリーニング時の血圧が高い理由をご教示ください。
        *   高血圧の基準を満たしているにもかかわらず、選択/除外基準に違反していない理由をご教示ください。
    *   **判断理由:**
        *   選択/除外基準、既往歴、併用薬の整合性を確認する必要がある。
## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目:
    *   CM.CMTRTとMHの整合性
    *   CM.CMSTDTCの日付
    *   DS.DSDTCとDS.VISITの整合性
    *   LB.LBNRINDの評価

問題点:

*   問題No.1:
    *   変数名と値: CM.CMTRT = "ALEVE", CM.CMDECOD = "NAPROXEN SODIUM", MH.MHBODSYS = "RESPIRATORY SYSTEM"
    *   矛盾の内容: CMTRTとしてALEVE（解読後: NAPROXEN SODIUM）が記録されているにもかかわらず、MedDRAのMHBODSYSがRESPIRATORY SYSTEMとなっている。NAPROXEN SODIUMは一般的に解熱鎮痛剤として使用され、RESPIRATORY SYSTEMの疾患に使用されるとは限らないため、CMINDC（Indication）が空白であることも合わせて、医学的に矛盾している可能性がある。
    *   問題点の原因（推測）: データ入力時のコーディングミス、または原資料に不正確な情報が記載されている可能性。
    *   対応策（提案）:
        1.  CMINDCに具体的な症状や疾患名が記録されていれば、MHBODSYSを適切なものに修正する。
        2.  原資料を確認し、ALEVEが呼吸器系の疾患に対して使用されていたか確認する。
        3.  呼吸器系の疾患に使用されていない場合は、MHBODSYSをより適切な分類（例: Musculoskeletal and Connective Tissue Disorders）に修正する。

*   問題No.2:
    *   変数名と値: CM.CMSTDTC = "2011"
    *   矛盾の内容: CM.CMSTDTCは、併用薬の使用開始日を示す変数だが、日付が年のみで記録されている。
    *   問題点の原因（推測）: データ入力時の不備、または原資料に詳細な日付情報がない可能性。
    *   対応策（提案）: 原資料を確認し、可能な限り正確な日付（月、日）を特定する。不明な場合は、月日をNULL値として記録し、SDTMのImputation Method（--IM）変数を活用して欠損理由を説明する。

*   問題No.3:
    *   変数名と値: DS.DSDTC = "2012-12-31T11:30", DS.VISIT = "WEEK 24"
    *   矛盾の内容: DS.DSDTCは2012-12-31T11:30であるにもかかわらず、DS.VISITがWEEK 24となっている。DM.RFSTDTCが2012-07-20であるため、矛盾している可能性がある。
    *   問題点の原因（推測）: データ入力時の日付誤り、またはDSDECODの選択ミス。
    *   対応策（提案）: 原資料を確認し、DSDTCの日付、時刻が正しいか検証する。必要に応じてDSTERM、DSDECOD、DSCATを見直す。

*   問題No.4:
    *   変数名と値: LB.LBTESTCD = "SPGRAV", LB.LBORRES = "1.032", LB.LBORNRLO = "1.006", LB.LBORNRHI = "1.03", LB.LBNRIND = "HIGH"
    *   矛盾の内容: LBORRES（原値）が1.032で、LBORNRHI（基準範囲上限）が1.03であるため、一見するとLBNRINDは「HIGH」（高値）で矛盾はない。しかし、LBORRESU（原単位）が"NO UNITS"となっており、SPGRAV（尿比重）に単位がないのは不自然である。
    *   問題点の原因（推測）: データ入力時の単位の誤り、またはDefine.xmlの定義ミス。
    *   対応策（提案）:
        1.  原資料を確認し、尿比重の単位が正しく記録されているか確認する。
        2.  単位が正しくない場合は、修正する。
        3.  単位に誤りがない場合は、尿比重の基準範囲とLBNRINDの評価が正しいか、医学的専門家の意見を求める。
        4.  Define.xmlに単位に関する定義が正しく記述されているか確認する。

    *   Define.xmlの修正候補:
        1.  LB.LBORRESUのCodeListに、尿比重で使用される一般的な単位（例: "g/mL"）を追加する。

*   問題No.5:
    *   変数名と値: AE.AETERM = "APPLICATION SITE DERMATITIS", RELREC.IDVARVAL = "   4",RELTYPE = "relationship identifier" ,RELID = "01-703-1258-E08"
    *   矛盾の内容: Related Recordsドメイン(RELREC)のRELID (関連識別子)の値がAEドメインのAESPIDの値と一致しない。AETERMが適用部位皮膚炎であり、局所的な有害事象であることから、治験薬との関連が疑われる。一方、Concomitant Medications(CM)では、対象の有害事象発生期間中にHYDROCORTISONE (副腎皮質ホルモン)が投与されている。
    *   問題点の原因（推測）: データ入力時のコーディングミス、RELREC.RELIDの設定誤り。
    *   対応策（提案）: 
        1.  症例記録を確認し、RELREC.RELIDとAE.AESPIDが正確に転記されているか確認。
        2.  適用部位皮膚炎の開始日とHYDROCORTISONEの投与期間を確認し、関連性を評価する。
        3.  HYDROCORTISONEで症状が改善した場合、因果関係(AEREL)の再評価を検討する。

クエリの作成 (必要な場合のみ):

*   患者ID: 01-703-1258
    *   クエリNo.1:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMTRT = "ALEVE", CM.CMDECOD = "NAPROXEN SODIUM", MH.MHBODSYS = "RESPIRATORY SYSTEM"
        *   医療機関への問い合わせ文面:
            *   患者[01-703-1258]の併用薬ALEVE（NAPROXEN SODIUM）について、投与目的（適応疾患）を教えてください。特に呼吸器系の疾患に使用されていましたでしょうか？
        *   判断理由:
            *   併用薬の使用目的は、安全性評価において重要です。
            *   得られた回答によっては、安全性解析に影響を及ぼす可能性があります。

    *   クエリNo.2:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMSTDTC = "2011"
        *   医療機関への問い合わせ文面:
            *   患者[01-703-1258]の併用薬ALEVE（NAPROXEN SODIUM）の使用開始日について、可能な限り詳細な日付（月日）を教えてください。
        *   判断理由:
            *   併用薬の使用期間を特定することで、有害事象との関連性をより正確に評価できます。

    *   クエリNo.3:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: DS.DSDTC = "2012-12-31T11:30", DS.VISIT = "WEEK 24"
        *   医療機関への問い合わせ文面:
            *   患者[01-703-1258]の最終検査の実施日時を教えてください。特に、DS.DSDTCに記載された日付、時刻が正しいかどうかの確認をお願いいたします。
        *   判断理由:
            *   治験薬投与終了後の検査データに影響を及ぼす可能性がある。

    *   クエリNo.4:
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: VS.VSPOS
        *   医療機関への問い合わせ文面:
            *   体位をSUPINE,STANDINGで測定した場合、どのように手順化されていますか？
        *   判断理由:
            *   血圧は体位によって変化するため、測定手順の標準化が不可欠です。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1258
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CMSTDTC=2011, VISIT="SCREENING 1", VISITNUM=1
    *   逸脱内容: 患者01-703-1258において、スクリーニング1 (VISITNUM=1) で開始された併用薬ALEVE (CMTRT="ALEVE") の開始日(CMSTDTC)が2011年であり、試験基準日（Reference Start Date）である2012年7月20日より前である。しかし、本試験の治験薬投与開始日(RFXSTDTC)は2012年7月20日であり、治験薬投与期間中にCMの投与が行われている。一般的に、CMデータセットは治験薬投与期間中に投与された薬剤を記録するため、矛盾が発生している。
    *   プロトコル該当箇所: 特に併用薬の投与期間に関する詳細な規定はプロトコルに明記されていない。
    *   判断理由: 一般的にCMデータセットは治験薬投与期間中に投与された薬剤を記録するため。

*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LBTESTCD=EOS, VISIT="SCREENING 1", LBORRES="0.59", LBORNRHI="0.57"
    *   逸脱内容: 好酸球(EOS)の検査結果(LBORRES)が0.59 THOU/uLであり、基準範囲上限(LBORNRHI)の0.57 THOU/uLを超えている。しかし、DM.AGEが78歳であるため、TIのEXCL27の基準範囲外となるかどうかは、Lilly Reference Range III を確認する必要がある。
    *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
    *   判断理由: 除外基準に該当するかどうかは、Lilly Reference Range III を確認する必要がある。

*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LBTESTCD=SPGRAV, VISIT="SCREENING 1", LBORRES="1.032", LBORNRHI="1.03"
    *   逸脱内容: 尿比重(SPGRAV)の結果(LBORRES)が1.032であり、基準範囲上限(LBORNRHI)の1.03を超えている。
    *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
    *   判断理由: 臨床的に問題があるかどうか確認が必要。

*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MHDTC=2012-07-10, MHTERM="ALZHEIMER'S DISEASE", MHSTDTC="2006-02-17"
    *   逸脱内容: 既往歴にアルツハイマー病（ALZHEIMER'S DISEASE）の記載があり、MHSTDTC（2006-02-17）とMHDTC（2012-07-10）から、本試験参加以前からアルツハイマー病の診断を受けている。しかしながら、TI(Trial Inclustion/Exclusion Criteria)にアルツハイマー病患者を対象とする旨の記載しかなく、罹患期間に関する規定が存在しないためプロトコルからの逸脱とは断定できない。
    *   プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [2]に「PROBABLE Alzheimer’s diseaseの診断」としか記載されていない。
    *   判断理由: TIにアルツハイマー病患者を対象とする旨の記載しかなく、罹患期間に関する規定が存在しない。

*   逸脱No.: 5
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: ALT=43, AST=36, EOS=0.59, SPGRAV=1.032
    *   逸脱内容: スクリーニング検査において、ALT, AST, EOS, SPGRAV が基準値範囲外。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria 27b, 28b
    *   判断理由: 
        *   TI の EXCL27 に「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」と記載されている。今回の逸脱は、スクリーニング時の検査値異常のため、EXCL27に抵触する可能性がある。
        *  TIのEXCL28に「Central laboratory test values below reference range for folate, and vitamin B12, and outside reference range for thyroid function tests.」と記載されている。

*   逸脱No.: 6
    *   臨床試験結果への影響度合い: None
    *   変数名と値: AE="DIZZINESS", AESTDTC=2012-08-01, AEENDTC=2012-10-01, EXSTDTC=2012-07-20, EXENDTC=2013-01-11
    *   逸脱内容: 01-703-1258に、治験薬投与開始後、2012-08-01から2012-10-01までDIZZINESS(めまい)のAEが発生している。しかし、CMデータセットには、DIZZINESSの原因となりうる薬剤は投与されていない。
    *   プロトコル該当箇所: 3.8 Concomitant Therapy
    *   判断理由: 併用禁止薬に該当する薬剤の投与はないため、プロトコル遵守。

**クエリ:**

*   患者ID: 01-703-1258
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CMSTDTC=2011, VISIT="SCREENING 1", VISITNUM=1
        *   医療機関への問い合わせ文面: 併用薬ALEVEの投与は治験薬投与期間中に継続していましたか？
        *   判断理由: 併用薬ALEVEの投与が治験薬投与期間中に継続していた場合、CMデータセットに矛盾が発生するため。

*   患者ID: 01-703-1258
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LBTESTCD=EOS, VISIT="SCREENING 1", LBORRES="0.59", LBORNRHI="0.57", DM.AGE=78
        *   医療機関への問い合わせ文面: スクリーニング時の好酸球(EOS)の結果が基準範囲外ですが、治験実施計画書3.4.2.2に記載されているLilly Reference Range III において除外基準に該当するか確認してください。
        *   判断理由: 除外基準に該当するか否かを確認するため。

*   患者ID: 01-703-1258
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LBTESTCD=SPGRAV, VISIT="SCREENING 1", LBORRES="1.032", LBORNRHI="1.03"
        *   医療機関への問い合わせ文面: スクリーニング時の尿比重(SPGRAV)の結果が基準範囲外ですが、臨床的に問題がないことを確認してください。
        *   判断理由: 基準範囲外の理由を確認するため。

*   患者ID: 01-703-1258
    *   クエリNo.: 4
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: MH="ALZHEIMER'S DISEASE", MHSTDTC="2006-02-17"
        *   医療機関への問い合わせ文面: 01-703-1258のアルツハイマー病診断確定時期と、組み入れ基準を満たしているか、詳細な情報を教えてください。
        *   判断理由: スクリーニング時に診断基準を満たしているか確認する必要があるため。



# 01-703-1042
## Task1: Clinical Review Results
## 1. 症例サマリーの作成:

**患者ID:** 01-703-1042

*   2012年12月27日 (Day -65): スクリーニング検査にて、ALT (135 U/L, 上限値43 U/L) およびAST (145 U/L, 上限値36 U/L) が高値。
*   2013年03月04日 (Day 3): 下痢 (軽度) の有害事象発現。
*   2013年03月05日 (Day 4): 不眠症 (軽度) および下痢 (軽度) の有害事象が発現。
*   2013年03月05日 (Day 4): 下痢 (軽度) の有害事象が回復。
*   2013年03月06日 (Day 5): 不眠症 (軽度) の有害事象が回復。
*   2013年03月28日 (Day 27): 検査にて、Anisocytes (1, 異常) が認められる。
*   2013年03月28日 (Day 27): 検査にて、MCV (101 fL, 上限値100 fL) が高値。
*   2013年02月21日 (Day -9): 検査にて、ナトリウム (133 mEq/L, 下限値135 mEq/L) が低値。
*   2013年03月28日 (Day 27): 検査にて、ナトリウム (146 mEq/L, 上限値145 mEq/L) が高値。

---

## 2. クエリの作成

**患者ID:** 01-703-1042

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = ALT, LB.LBORRES = 135, LB.LBDTC = 2012-12-27, LB.LBORNRLO = 6, LB.LBORNRHI = 43
    *   **医療機関への問い合わせ文面:**
        スクリーニング検査 (2012-12-27) において、ALT値が基準範囲外（135 U/L, 基準範囲 6-43 U/L）ですが、被験者は組み入れ基準を満たしていると判断されました。ALT値が基準範囲を超過しているにもかかわらず組み入れ可能と判断した医学的根拠についてご教示ください。
    *   **判断理由:**
        プロトコルの選択基準に、臨床検査値が Lilly Reference Range III を超える場合は除外すると規定されています。ALTは肝機能検査の指標であり、基準値からの逸脱は潜在的な肝疾患を示唆する可能性があります。

*   **クエリNo.:** 2
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** LB.LBTESTCD = AST, LB.LBORRES = 145, LB.LBDTC = 2012-12-27, LB.LBORNRLO = 11, LB.LBORNRHI = 36
    *   **医療機関への問い合わせ文面:**
        スクリーニング検査 (2012-12-27) において、AST値が基準範囲外（145 U/L, 基準範囲 11-36 U/L）ですが、被験者は組み入れ基準を満たしていると判断されました。AST値が基準範囲を超過しているにもかかわらず組み入れ可能と判断した医学的根拠についてご教示ください。
    *   **判断理由:**
        プロトコルの選択基準に、臨床検査値が Lilly Reference Range III を超える場合は除外すると規定されています。ASTは肝機能検査の指標であり、基準値からの逸脱は潜在的な肝疾患を示唆する可能性があります。

*   **クエリNo.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = SODIUM, LB.LBORRES = 133, LB.LBDTC = 2013-02-21, LB.LBORNRLO = 135, LB.LBORNRHI = 145
    *   **医療機関への問い合わせ文面:**
        2013年02月21日の検査において、血清ナトリウム値が基準範囲を下回っています（133 mEq/L, 基準範囲 135-145 mEq/L）。この低ナトリウム血症の原因について、臨床的に評価された情報があればご提供ください。
    *   **判断理由:**
        低ナトリウム血症は、神経症状や精神症状を悪化させる可能性があり、認知機能評価に影響を与える可能性があります。

*   **クエリNo.:** 4
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBTESTCD = SODIUM, LB.LBORRES = 146, LB.LBDTC = 2013-03-28, LB.LBORNRLO = 135, LB.LBORNRHI = 145
    *   **医療機関への問い合わせ文面:**
        2013年03月28日の検査において、血清ナトリウム値が基準範囲を上回っています（146 mEq/L, 基準範囲 135-145 mEq/L）。この高ナトリウム血症の原因について、臨床的に評価された情報があればご提供ください。
    *   **判断理由:**
       高ナトリウム血症は、脱水または他の電解質異常を示唆している可能性があり、認知機能に影響を与える可能性があります。

*   **クエリNo.:** 5
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** QS.QSTESTCD = DAITM20, QS.QSORRES = N, QS.QSDTC = 2013-06-22, VISIT = WEEK 16, DAITM20の定義
    *   **医療機関への問い合わせ文面:**
        DISABILITY ASSESSMENT FOR DEMENTIA (DAD)のWEEK16において、PREPARE OR COOK A LIGHT MEAL OR A SNACK (DAITM20)  の結果が "N" (いいえ) と回答されています。一方、BASELINE, WEEK24においては"Y"（はい）と回答されており、WEEK16でのみ出来ていない状況です。詳細な状況について医療機関からの情報をご提供ください。
    *   **判断理由:**
       DISABILITY ASSESSMENT FOR DEMENTIA (DAD)の結果が一貫していないため、DAITM20に関して確認が必要です。

## Task2: DM Review Results
全体的なデータ品質の評価:
*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMENDTC, LB.LBDY

問題点:

問題No.1:
*   変数名と値: CM.CMENDTC = "2009" (複数レコード)
*   矛盾の内容: CM.CMENDTCに"2009"という年のみが記録されているレコードが複数存在します。併用薬の終了日は、通常、開始日と同程度の精度で記録されるべきであり、年のみの記録は不適切です。
*   問題点の原因（推測）: データ入力時の不備、または情報源からの不正確なデータ収集。
*   対応策（提案）: 
    1.  医療機関に問い合わせを行い、正確なCMENDTC（日付、または少なくとも月を含む日付）を確認してください。
    2.  問い合わせの結果、正確な日付が得られない場合は、プロトコルに照らし合わせてCMENDTCをどのように扱うかを検討し、データ処理計画書（Data Handling Plan）に明記してください。

問題No.2:
*   変数名と値: LB.LBDYとLBDTCから計算されるStudy Dayにずれがある
*   矛盾の内容: LB.LBDTCとLB.LBDYの値に矛盾が見られます。LBDTCから計算されるべき理論上のLBDYと実際のLBDYにずれがある場合、データ収集または計算に誤りがある可能性があります。
*   問題点の原因（推測）: LB.LBDTCとLB.LBDYのデータ入力時の不備、またはLBDTCからLBDYを計算するロジックのエラー。
*   対応策（提案）: LBDTCからLBDYを再計算し、矛盾を修正してください。Define.xmlに記載されたComputationMethod OID="COMPMETHOD.STUDY_DAY"に従って計算されているか確認してください。
---

クエリの作成：
患者ID: 01-703-1042
*   クエリNo.1:
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMENDTC = "2009"
    *   医療機関への問い合わせ文面:
        *   患者ID 01-703-1042について、CMSEQ=1, 2, 3 で記録されているVITAMIN C, VITAMIN Eの併用薬の最終投与日（CMENDTC）が"2009"となっています。可能な範囲で、より詳細な日付（月日）をご教示いただけますでしょうか？
    *   判断理由: 併用薬の投与期間は、試験結果に影響を与える可能性のある重要な情報であるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-703-1042
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, MH.MHSTDTC=2008-07-23
    *   逸脱内容: 既往歴としてAlzheimer's Diseaseの診断を受けている。治験実施計画書3.4.2.2 Exclusion CriteriaのEXCL12に「Serious illness which required hospitalization within 3 months of screening」と記載されており、EXCL12のDiagnosis of serious neurological conditionsにも該当する可能性がある
    *   プロトコル該当箇所: 3.4.2.2
    *   判断理由: TI.IETESTCD=EXCL12の除外基準違反の疑いがある

患者ID: 01-703-1042
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, MH.MHSTDTC=2008-07-23
    *   医療機関への問い合わせ文面:
        *   被験者01-703-1042は、スクリーニング時にアルツハイマー病の既往歴が報告されています。
        *   アルツハイマー病の診断は、スクリーニング開始前3ヶ月以内の入院を必要とするほどの重篤な状態でしたでしょうか？
        *   また、プロトコルの除外基準EXCL12「Serious illness which required hospitalization within 3 months of screening」に該当するかどうかを判断するため、詳細な病歴と症状の程度についてご教示ください。
    *   判断理由: 除外基準EXCL12に抵触するかを確認するため



# 01-701-1118
## Task1: Clinical Review Results
患者ID: 01-701-1118

*   2014年02月27日 (Day -13): スクリーニング検査で、Albumin 3.9 g/dL, Alkaline Phosphatase 65 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 15 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.7 mg/dL, Blood Urea Nitrogen 15 mg/dL, Calcium 9.1 mg/dL, Cholesterol 178 mg/dL, Creatine Kinase 110 U/L, Chloride 108 mEq/L, Color N, Creatinine 1.0 mg/dL, Eosinophils 0.32 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 73 mg/dL, Hematocrit 45.0 %, Hemoglobin 15.6 g/dL, Potassium 4.7 mEq/L, Ketones 0, Lymphocytes 1.94 THOU/uL, Ery. Mean Corpuscular Hemoglobin 32 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 92 fL, Monocytes 0.73 THOU/uL, Sodium 141 mEq/L, pH 6.0, Phosphate 3.9 mg/dL, Platelet 268 THOU/uL, Protein 7.0 g/dL, Erythrocytes 4.90 MILL/uL, Specific Gravity 1.030, Thyrotropin 1.85 uIU/mL, Urate 4.2 mg/dL, Urobilinogen 0, Vitamin B12 289 pg/mL, Leukocytes 7.89 THOU/uL.

*   2014年03月10日 (Day -2): スクリーニング2の検査。

*   2014年03月12日 (Day 1): ベースラインの検査。

*   2014年03月12日 (Day 1): 併用薬としてAspirin(325mg, PRN, Oral), Multivitamin(1 tablet, QD, Oral)の投与が開始された。
*   2014年03月12日 (Day 1): ADAS-CogのWORD RECALL TASKで5点、NAMING OBJECTS AND FINGERS (REFER TO 5 Cで1点、DELAYED WORD RECALLで10点、COMMANDSで0点、CONSTRUCTIONAL PRAXISで3点、IDEATIONAL PRAXISで1点、ORIENTATIONで4点、WORD RECOGNITIONで10点、ATTENTION/VISUAL SEARCH TASKで12点、MAZE SOLUTIONで6sec、SPOKEN LANGUAGE ABILITYで0点、COMPREHENSION OF SPOKEN LANGUAGEで0点、WORD FINDING DIFFICULTY IN SPONTANEOUS Sで1点、RECALL OF TEST INSTRUCTIONSで1点、ADAS-COG(11) Subscoreで26点。NPI-XのDELUSIONS PRESENT, HALLUCINATIONS PRESENT, AGITATION/AGRESSION PRESENT, DEPRESSION/DYSPHORIA PRESENT, ANXIETY PRESENT, EUPHORIA/ELATION PRESENT, APATHY/INDIFFERENCE PRESENTで0点、MHITM08~13で0点。
*   2014年03月26日 (Day 14): WEEK2の検査. Albumin 4.2 g/dL, Alkaline Phosphatase 76 U/L, Alanine Aminotransferase 7 U/L, Aspartate Aminotransferase 13 U/L, Basophils 0.02 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 13 mg/dL, Calcium 9.0 mg/dL, Cholesterol 194 mg/dL, Creatine Kinase 41 U/L, Chloride 110 mEq/L, Color N, Creatinine 1.0 mg/dL, Eosinophils 0.09 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 88 mg/dL, Hematocrit 45.0 %, Hemoglobin 15.5 g/dL, Potassium 4.6 mEq/L, Ketones 0, Lymphocytes 1.40 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 88 fL, Monocytes 0.39 THOU/uL, Sodium 142 mEq/L, pH 6.0, Phosphate 4.1 mg/dL, Platelet 285 THOU/uL, Protein 7.1 g/dL, Erythrocytes 5.10 MILL/uL, Specific Gravity 1.033, Urate 4.7 mg/dL, Urobilinogen 0, Leukocytes 6.07 THOU/uL.

*   2014年03月26日 (Day 14): AETERMにCOUGH(MILD)が報告された。

*   2014年04月09日 (Day 29): WEEK4の検査。Albumin 4.4 g/dL, Alkaline Phosphatase 67 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 14 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.6 mg/dL, Blood Urea Nitrogen 12 mg/dL, Calcium 9.3 mg/dL, Cholesterol 176 mg/dL, Creatine Kinase 49 U/L, Chloride 100 mEq/L, Creatinine 1.2 mg/dL, Eosinophils 0.08 THOU/uL, Gamma Glutamyl Transferase 13 U/L, Glucose 92 mg/dL, Hematocrit 44.0 %, Hemoglobin 15.6 g/dL, Potassium 4.7 mEq/L, Lymphocytes 1.72 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 88 fL, Monocytes 0.54 THOU/uL, Sodium 134 mEq/L, Phosphate 4.0 mg/dL, Platelet 308 THOU/uL, Protein 7.4 g/dL, Erythrocytes 5.00 MILL/uL, Urate 4.1 mg/dL, Urobilinogen 0, Leukocytes 5.89 THOU/uL

*   2014年04月23日 (Day 43): WEEK6の検査。Albumin 4.1 g/dL, Alkaline Phosphatase 62 U/L, Alanine Aminotransferase 11 U/L, Aspartate Aminotransferase 15 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 15 mg/dL, Calcium 9.2 mg/dL, Cholesterol 184 mg/dL, Creatine Kinase 42 U/L, Chloride 103 mEq/L, Creatinine 1.1 mg/dL, Eosinophils 0.17 THOU/uL, Gamma Glutamyl Transferase 14 U/L, Glucose 94 mg/dL, Hematocrit 42.0 %, Hemoglobin 15.5 g/dL, Potassium 4.8 mEq/L, Lymphocytes 2.05 THOU/uL, Ery. Mean Corpuscular Hemoglobin 33 pg, Ery. Mean Corpuscular HGB Concentration 37 g/dL, Ery. Mean Corpuscular Volume 90 fL, Monocytes 0.42 THOU/uL, Sodium 139 mEq/L, Phosphate 4.1 mg/dL, Platelet 274 THOU/uL, Protein 7.0 g/dL, Erythrocytes 4.70 MILL/uL, Urate 4.0 mg/dL, Urobilinogen 0, Leukocytes 6.59 THOU/uL.

*   2014年05月08日 (Day 58): WEEK8の検査。Albumin 3.9 g/dL, Alkaline Phosphatase 67 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 18 U/L, Basophils 0.05 THOU/uL, Bilirubin 0.6 mg/dL, Blood Urea Nitrogen 12 mg/dL, Calcium 8.6 mg/dL, Cholesterol 204 mg/dL, Creatine Kinase 49 U/L, Chloride 104 mEq/L, Creatinine 1.0 mg/dL, Eosinophils 0.17 THOU/uL, Gamma Glutamyl Transferase 18 U/L, Glucose 69 mg/dL, Hematocrit 45.0 %, Hemoglobin 15.7 g/dL, Potassium 4.3 mEq/L, Lymphocytes 2.80 THOU/uL, Ery. Mean Corpuscular Hemoglobin 32 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 91 fL, Monocytes 0.88 THOU/uL, Sodium 139 mEq/L, Phosphate 3.3 mg/dL, Platelet 334 THOU/uL, Protein 7.2 g/dL, Erythrocytes 4.90 MILL/uL, Urate 4.6 mg/dL, Urobilinogen 0, Leukocytes 8.22 THOU/uL。

*   2014年06月05日 (Day 86): WEEK12の検査。Albumin 4.0 g/dL, Alkaline Phosphatase 70 U/L, Alanine Aminotransferase 16 U/L, Aspartate Aminotransferase 13 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 11 mg/dL, Calcium 8.9 mg/dL, Cholesterol 177 mg/dL, Creatine Kinase 36 U/L, Chloride 106 mEq/L, Color N, Creatinine 1.2 mg/dL, Eosinophils 0.13 THOU/uL, Gamma Glutamyl Transferase 15 U/L, Glucose 106 mg/dL, Hematocrit 47.0 %, Hemoglobin 15.7 g/dL, Potassium 4.2 mEq/L, Ketones 0, Lymphocytes 1.62 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 33 g/dL, Ery. Mean Corpuscular Volume 92 fL, Monocytes 0.45 THOU/uL, Sodium 142 mEq/L, pH 5.0, Phosphate 3.0 mg/dL, Platelet 293 THOU/uL, Protein 7.2 g/dL, Erythrocytes 5.10 MILL/uL, Specific Gravity 1.030, Urate 3.8 mg/dL, Urobilinogen 0, Leukocytes 6.33 THOU/uL.

*   2014年07月02日 (Day 113): WEEK16の検査。Albumin 4.1 g/dL, Alkaline Phosphatase 65 U/L, Alanine Aminotransferase 15 U/L, Aspartate Aminotransferase 18 U/L, Basophils 0.03 THOU/uL, Bilirubin 0.6 mg/dL, Blood Urea Nitrogen 17 mg/dL, Calcium 9.2 mg/dL, Cholesterol 188 mg/dL, Creatine Kinase 88 U/L, Chloride 106 mEq/L, Creatinine 1.1 mg/dL, Eosinophils 0.16 THOU/uL, Gamma Glutamyl Transferase 14 U/L, Glucose 87 mg/dL, Hematocrit 44.0 %, Hemoglobin 15.6 g/dL, Potassium 4.5 mEq/L, Lymphocytes 1.67 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 88 fL, Monocytes 0.52 THOU/uL, Sodium 141 mEq/L, Phosphate 3.5 mg/dL, Platelet 304 THOU/uL, Protein 7.2 g/dL, Erythrocytes 5.00 MILL/uL, Urate 4.2 mg/dL, Urobilinogen 0, Leukocytes 6.69 THOU/uL。

*   2014年07月30日 (Day 141): WEEK20の検査。Albumin 4.1 g/dL, Alkaline Phosphatase 62 U/L, Alanine Aminotransferase 13 U/L, Aspartate Aminotransferase 14 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.6 mg/dL, Blood Urea Nitrogen 18 mg/dL, Calcium 9.2 mg/dL, Cholesterol 195 mg/dL, Creatine Kinase 41 U/L, Chloride 102 mEq/L, Creatinine 1.2 mg/dL, Eosinophils 0.08 THOU/uL, Gamma Glutamyl Transferase 15 U/L, Glucose 93 mg/dL, Hematocrit 45.0 %, Hemoglobin 15.7 g/dL, Potassium 4.2 mEq/L, Lymphocytes 1.65 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 35 g/dL, Ery. Mean Corpuscular Volume 88 fL, Monocytes 0.51 THOU/uL, Sodium 139 mEq/L, Phosphate 4.3 mg/dL, Platelet 324 THOU/uL, Protein 7.1 g/dL, Erythrocytes 5.10 MILL/uL, Urate 5.0 mg/dL, Urobilinogen 0, Leukocytes 7.01 THOU/uL。

*   2014年08月27日 (Day 169): WEEK24の検査。Albumin 4.2 g/dL, Alkaline Phosphatase 58 U/L, Alanine Aminotransferase 13 U/L, Aspartate Aminotransferase 11 U/L, Basophils 0.11 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 14 mg/dL, Calcium 9.2 mg/dL, Cholesterol 186 mg/dL, Creatine Kinase 36 U/L, Chloride 105 mEq/L, Color N, Creatinine 1.1 mg/dL, Eosinophils 0.09 THOU/uL, Gamma Glutamyl Transferase 15 U/L, Glucose 92 mg/dL, Hematocrit 48.0 %, Hemoglobin 15.3 g/dL, Potassium 4.6 mEq/L, Ketones 0, Lymphocytes 1.57 THOU/uL, Ery. Mean Corpuscular Hemoglobin 31 pg, Ery. Mean Corpuscular HGB Concentration 32 g/dL, Ery. Mean Corpuscular Volume 96 fL, Monocytes 0.52 THOU/uL, Sodium 142 mEq/L, pH 6.0, Phosphate 4.2 mg/dL, Platelet 313 THOU/uL, Protein 6.8 g/dL, Erythrocytes 5.00 MILL/uL, Specific Gravity 1.026, Urate 4.2 mg/dL, Urobilinogen 0, Leukocytes 7.10 THOU/uL。

*   2014年09月09日 (Day 182): WEEK26の検査。Albumin 3.9 g/dL, Alkaline Phosphatase 56 U/L, Alanine Aminotransferase 10 U/L, Aspartate Aminotransferase 12 U/L, Basophils 0.04 THOU/uL, Bilirubin 0.5 mg/dL, Blood Urea Nitrogen 12 mg/dL, Calcium 8.4 mg/dL, Cholesterol 189 mg/dL, Creatine Kinase 50 U/L, Chloride 104 mEq/L, Creatinine 1.1 mg/dL, Eosinophils 0.11 THOU/uL, Gamma Glutamyl Transferase 16 U/L, Glucose 89 mg/dL, Hematocrit 42.0 %, Hemoglobin 14.9 g/dL, Potassium 4.1 mEq/L, Lymphocytes 1.72 THOU/uL, Ery. Mean Corpuscular Hemoglobin 32 pg, Ery. Mean Corpuscular HGB Concentration 36 g/dL, Ery. Mean Corpuscular Volume 89 fL, Monocytes 0.44 THOU/uL, Sodium 139 mEq/L, Phosphate 4.6 mg/dL, Platelet 271 THOU/uL, Protein 6.7 g/dL, Erythrocytes 4.70 MILL/uL, Specific Gravity 1.026, Urate 5.2 mg/dL, Urobilinogen 0, Leukocytes 5.95 THOU/uL。

*   2014年09月09日 (Day 182): 最終検査が実施され、試験を完了した。

---
患者ID: 01-701-1118

クエリなし

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTCとCM.CMENDTC、MH.MHSTDTC、AE.AESTDTC

問題点:

*   問題No.1:
    *   変数名と値: CM.CMSTDTC="2000-12-10", CM.CMENDTC=""
    *   矛盾の内容: USUBJID="01-701-1118"のCMドメインにおいて、CMSTDTCが2000年12月10日となっているレコードが複数存在するが、これはDMドメインのRFSTDTC="2014-03-12"（Subject Reference Start Date/Time）より13年以上も前である。CMSTDTCは、通常、RFSTDTC以降であるべきであり、医学的に考えても同時期にConcomitant Medicationsを使用しているとは考えにくい。また、CMENDTCが欠損している。
*   問題点の原因（推測）: データ入力エラー、日付の誤記、またはデータの変換エラー
*   対応策（提案）: CMSTDTCとCMENDTCの正確性を確認するため、原資料との照合が必要。CMENDTCが不明な場合は、その理由を特定し、必要に応じて欠損値として扱う。

*   問題No.2:
    *   変数名と値: MH.MHSTDTC="1991"
    *   矛盾の内容: USUBJID="01-701-1118"のMHドメインにおいて、MHSTDTCが1991年となっているレコードが存在するが、これはDMドメインのRFSTDTC="2014-03-12"（Subject Reference Start Date/Time）より23年も前である。
*   問題点の原因（推測）: データ入力エラー、日付の誤記、またはデータの変換エラー
*   対応策（提案）: MHSTDTCの正確性を確認するため、原資料との照合が必要。

*   問題No.3:
    *   変数名と値: AE.AESTDTC="2003"
    *   矛盾の内容: USUBJID="01-701-1118"のAEドメインにおいて、AESTDTCが2003年となっているレコードが存在するが、これはDMドメインのRFSTDTC="2014-03-12"（Subject Reference Start Date/Time）より11年も前である。
*   問題点の原因（推測）: データ入力エラー、日付の誤記、またはデータの変換エラー
*   対応策（提案）: AESTDTCの正確性を確認するため、原資料との照合が必要。

クエリの作成:

*   患者ID: 01-701-1118
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: CM.CMSTDTC="2000-12-10", CM.CMENDTC=""
        *   医療機関への問い合わせ文面:
            *   CM.CMTRT="ASPIRIN"のCMSTDTCが2000年12月10日となっていますが、これは登録日（2014年3月12日）よりも13年以上前です。
            *   CMSTDTCに誤りがないか、CMENDTCが欠損している理由と正確な日付をご教示ください。
        *   判断理由: 併用薬の使用開始日が試験参加より大幅に前であることは不自然であり、データの信頼性に疑義が生じるため。

*   患者ID: 01-701-1118
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHSTDTC="1991"
        *   医療機関への問い合わせ文面:
            *   MH.MHTERM="WRIST FRACTURE"のMHSTDTCが1991年となっていますが、登録日（2014年3月12日）よりも23年も前です。
            *   MHSTDTCに誤りがないか、正確な日付をご教示ください。
        *   判断理由: 既往歴の使用開始日が試験参加より大幅に前であることは不自然であり、データの信頼性に疑義が生じるため。

*   患者ID: 01-701-1118
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AESTDTC="2003"
        *   医療機関への問い合わせ文面:
            *   AETERM="COUGH"のAESTDTCが2003年となっていますが、登録日（2014年3月12日）よりも11年も前です。
            *   AESTDTCに誤りがないか、正確な日付をご教示ください。
        *   判断理由: 有害事象の発現日が試験参加より大幅に前であることは不自然であり、データの信頼性に疑義が生じるため。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1118
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMENDTC = "2000-12-10" (すべてのアスピリンのCMENDTC)
    *   逸脱内容: 併用薬アスピリンの終了日が2000-12-10となっており、CMSTDTC（2014年の日付）より過去の日付になっている。データの誤入力の可能性がある。
    *   プロトコル該当箇所: プロトコルには併用薬の終了日に関する規定はないが、論理的にCMENDTCはCMSTDTC以降の日付であるべき。
    *   判断理由: CMENDTCはCMSTDTCより後の日付になるのが一般的だが、本データでは整合性が取れていない。

患者ID: 01-701-1118
*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: AE.AESTDTC = "2003"
    *   逸脱内容: 有害事象COUGHの発現開始年が2003年となっており、DM.RFSTDTC（2014-03-12）より過去の日付になっている。データの誤入力の可能性がある。
    *   プロトコル該当箇所: プロトコルには、AE開始日に関する規定はないが、DM.RFSTDTC以降の日付になるのが一般的である。
    *   判断理由: AE発現開始日は通常、治験薬投与開始日以降であるべきだが、本データでは整合性が取れていない。

患者ID: 01-701-1118
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DM.RFPENDTC = "2014-09-09T13:28", DS.DSDTC = "2014-09-09T13:28", LB.LBDTC =  "2014-09-09T13:28"
    *   医療機関への問い合わせ文面: 
        *   患者01-701-1118のDM.RFPENDTC（参加終了日）、DS.DSDTC（最終観察日）、LB.LBDTC（最終検査日）がすべて同じ日付と時間ですが、これは正しいですか？
        *   もし最終検査が、最終観察日より前に実施されている場合、その理由を教えてください。
    *   判断理由: DM、DS、LBドメインの最終日がすべて同じ場合、データ入力時の誤りの可能性があるため。

クエリなし


# 01-701-1015
## Task1: Clinical Review Results
患者ID: 01-701-1015

* 2013年12月26日 (Day -7): スクリーニング検査で、アルカリホスファターゼ(ALP)が34 U/Lと基準範囲を下回り(LBORNRLO: 35 U/L)、Anisocytesが「1」と異常値を示す。白血球の検査値は正常範囲内。アスパラギン酸アミノトランスフェラーゼ(AST)が40 U/Lと基準範囲を上回る(LBORNRHI: 34 U/L)。
* 2014年01月03日 (Day 2): 開始日、終了日がともに「2014-01-03」であることから、局所投与のネオスポリン（Neosporin）を1日のみ使用した。
* 2014年01月11日 (Day 10): 下痢を発症。
* 2014年01月16日 (Day 15): アラニンアミノトランスフェラーゼ(ALT)が41 U/Lと基準範囲を上回る(LBORNRHI: 34 U/L)。紅斑と掻痒感を訴える。
* 2014年07月02日 (Day 182): 最終検査。

---

患者ID: 01-701-1015

* **クエリNo.1:**
    * **臨床試験結果への影響度合い:** Minor
    * **変数名と値:** AE.AEOUT=NOT RECOVERED/NOT RESOLVED
    * **医療機関への問い合わせ文面:**
        *   有害事象「適用部位紅斑」と「適用部位掻痒」の転帰が「未回復/未解決」となっていますが、week26の最終観察時にも症状は継続していましたでしょうか？
    *   **判断理由:**
        *   AEドメインの転帰に関する情報がNOT RECOVERED/NOT RESOLVEDとなっているにもかかわらず、その後の経過観察に関する情報がないため。
        *   データが不足している場合、最終評価に影響を及ぼす可能性があるため、問い合わせが必要と判断しました。
*   **クエリNo.2:**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LB.LBDTC=2014-03-05T12:25, LB.VISIT=WEEK 8, LB.VISITDY=56
    *   **医療機関への問い合わせ文面:**
        *   LBドメインにおいて、visitdyが56であるにもかかわらず、LBDTC（Date/Time of Specimen Collection）が2014-03-05T12:25となっています。これはweek8に相当する日付と思われますが、visitdyとLBDYとの整合性について確認をお願いします。
    *   **判断理由:**
        *   計画されたvisitdyと実際の日付が一致しない場合、データ収集または記録に誤りがあった可能性があります。日付のずれが臨床試験の結果に影響を与える可能性は低いですが、データの正確性を確認するために問い合わせが必要です。
*   **クエリNo.3:**
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** VS.VSPOS=STANDING, VS.VSTPT=AFTER STANDING FOR 3 MINUTES
    *   **医療機関への問い合わせ文面:**
        *   バイタルサイン測定において、立位での血圧および脈拍測定は、起立後1分と3分の2回測定されています。プロトコル上、測定タイミングに特に指示がない場合、1分後と3分後のどちらを優先すべきでしょうか？
    *   **判断理由:**
        *   プロトコルに詳細な指示がない場合、測定タイミングのずれがデータの解釈に影響を与える可能性があります。
## Task2: DM Review Results
クリニカルデータマネージャーとして、データ整合性レビューとクエリ作成を実施します。

**1. データ整合性レビュー:**

*   **全体的なデータ品質の評価:**

    *   総合評価: 一部問題あり
    *   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, LB.LBDTC, LB.LBDYとVS.VSDTC, VS.VSDY の矛盾

*   **問題点:**

    *   **問題No.1:** CM.CMSTDTCとCM.CMENDTCの矛盾
        *   **変数名と値:** CM.CMSTDTC = "2003", CM.CMENDTC = ""
        *   **矛盾の内容:** CM.CMSTDTCが2003年となっており、CM.CMDTCの2013年12月26日より10年前の設定となっている。
        *  **問題点の原因（推測）:** データの誤入力。CMSTDTCはCMCMDTCより後の日付になることは考えにくい。
        *   **対応策（提案）:** CM.CMSTDTCの値をCM.CMDTCの値と同一、またはCM.CMDTCより後の日付に修正する必要がある。

    *   **問題No.2:** CM.CMSTDTCとCM.CMENDTCの矛盾
        *   **変数名と値:** CM.CMSTDTC = "2014-03-27", CM.CMENDTC = ""
        *   **矛盾の内容:** 
HydrocortisoneのCMENDTCが空欄。
Neosporin のCMDTCとCMSTDTC,CMENDTCが矛盾。
        *   **問題点の原因（推測）:** データの誤入力、またはデータ未入力。
        *   **対応策（提案）:** HydrocortisoneとNeosporin のCMENDTCを調査し、適切な値を入力する。CMENDTCが空欄の場合、その理由を記載する。

    *   **問題No.3:** LB.LBDTCとLB.LBDYの矛盾
        *   **変数名と値:** LB.LBDTC = "2014-03-05T12:25", LB.LBDY = 63
        *   **矛盾の内容:** LBDTCの日付は2014-03-05だが、LBDY（Study Day of Specimen Collection）は63となっており、DM.RFSTDTC（2014-01-02）からの日数を計算すると一致しない。
        *   **問題点の原因（推測）:** データの誤入力、または計算間違い。
        *   **対応策（提案）:** LB.LBDTCとLB.LBDYの整合性を確認し、必要に応じて修正する。LBDTCからLBDYを再計算する。

    *   **問題No.4:** LB.LBDTCとLB.LBDYの矛盾
        *   **変数名と値:** LB.LBDTC = "2014-05-07T11:21", LB.LBDY = 126
        *   **矛盾の内容:** LBDTCの日付は2014-05-07だが、LBDY（Study Day of Specimen Collection）は126となっており、DM.RFSTDTC（2014-01-02）からの日数を計算すると一致しない。
        *   **問題点の原因（推測）:** データの誤入力、または計算間違い。
        *   **対応策（提案）:** LB.LBDTCとLB.LBDYの整合性を確認し、必要に応じて修正する。LBDTCからLBDYを再計算する。
     *   **問題No.5:** VS.VSDTCとVS.VSDYの矛盾
        *   **変数名と値:** VS.VSDTC = "2014-03-05", VS.VDY = 63
        *   **矛盾の内容:** VSDTCの日付は2014-03-05だが、VSDY（Study Day of Vital Signs）は63となっており、DM.RFSTDTC（2014-01-02）からの日数を計算すると一致しない。
        *   **問題点の原因（推測）:** データの誤入力、または計算間違い。
        *   **対応策（提案）:** VS.VSDTCとVS.VDYの整合性を確認し、必要に応じて修正する。VSDTCからVDYを再計算する。
    *   **問題No.6:** 
        *   **変数名と値:** LB.LBTEST = "Ery. Mean Corpuscular Hemoglobin"
        *   **矛盾の内容:** LBTESTは200文字まで定義されているが、"Ery." が省略されている。正しくは、"Erythrocyte Mean Corpuscular Hemoglobin"とすべき。
        *   **問題点の原因（推測）:** データの切り捨て。
        *   **対応策（提案）:** LB.LBTESTの値を見直し、正しく記載する。

**2. クエリの作成:**

*   **患者ID:** 01-701-1015
    *   **クエリNo.1:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC, CM.CMENDTC
        *   **医療機関への問い合わせ文面:**
            *   CMSEQ=1,5,9,13,18,23,28,33,38,43,49,55,61のAspirin について、CMSTDTCに誤りがないか確認してください。
            *  CMSEQ=48,54,60,66のHydrocortisone について、CMENDTCを更新してください。
            *   CMSEQ=17,22,27,32,37,42,47,53,59,65のNeosporin について、CMDTCとCMSTDTC,CMENDTCが矛盾していますが、正しい日付を入力してください。
        *   **判断理由:** 
CMSTDTCは薬剤の投与開始日であり、評価期間を特定する上で重要な情報である。誤った日付はデータの解釈に影響を与える可能性がある。
CMENDTCも同様に、薬剤の投与終了日として、薬剤の曝露期間を特定する上で重要である。空欄はデータが欠損していることを意味し、正確な評価を妨げる。

*   **患者ID:** 01-701-1015
    *   **クエリNo.2:**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBDY, LB.LBDTC
        *   **医療機関への問い合わせ文面:**
            *   LBSEQ=134-136のALT,について、LBDTC（2014-03-05T12:25）とLBDY (63)に矛盾がないか確認してください。
            *   LBSEQ=199-200のALT,について、LBDTC（2014-05-07T11:21）とLBDY (126)に矛盾がないか確認してください。
        *   **判断理由:** LB.LBDYとLB.LBDTCは検査日を示す重要な情報であり、矛盾がある場合、検査時期の特定や他のデータとの関連性に影響を及ぼす可能性がある。

*   **患者ID:** 01-701-1015
    *   **クエリNo.3:**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTEST = "Ery. Mean Corpuscular Hemoglobin"
        *   **医療機関への問い合わせ文面:**
            LB.LBTESTについて、"Ery." が省略されています。"Erythrocyte Mean Corpuscular Hemoglobin"の記載に修正可能か確認ください。
        *   **判断理由:** LBTESTは検査項目名であり、データの正確性を担保する上で重要である。

## Task3: Protocol Deviation Review Results
患者ID: 01-701-1015

*   **逸脱No.:** 1
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** CMDECOD = "UNCODED" (NEOSPORIN /USA/), CMDOSU = "VIAL"
    *   **逸脱内容:** 併用薬として使用されたNEOSPORIN /USA/ が、標準化された薬剤名(CMDECOD)としてUNCODEDと記録されている。CMDOSU(Dose Units) がVIALとなっているが、単位として不適切である。
    *   **プロトコル該当箇所:** プロトコル3.8 Concomitant Therapy に、併用薬に関する規定があると思われるが、詳細な情報がないため特定できず。
    *   **判断理由:** Define.xmlのCMドメインの定義では、CMDECODは標準化された薬剤名であるべきだが、UNCODEDとなっている。またCMDOSUの値がVIALであることは医学的に意味をなさない。

*   **逸脱No.:** 2
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** MHDECOD = "" (ALZHEIMER'S DISEASE)
    *   **逸脱内容:** 病歴として記録されたアルツハイマー病(ALZHEIMER'S DISEASE)が、標準化された病名(MHDECOD)として空欄となっている。
    *   **プロトコル該当箇所:** プロトコル3.4.2.1 Inclusion Criteria [2]に診断基準の定義の記載があるが、診断名の標準化に関する規定はない。
    *   **判断理由:** Define.xmlのMHドメインの定義では、MHDECODはDictionary-Derived Termであるべきだが、空欄となっている。

*   **逸脱No.:** 3
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LBTESTCD = "ANISO", LBORRES = "1"
    *   **逸脱内容:** スクリーニング検査(SCREENING 1)において、血液検査の結果(ANISO: 異型赤血球)が異常値(ABNORMAL)を示している。
    *   **プロトコル該当箇所:** プロトコル3.4.2.2 Exclusion Criteria [27b]に、除外基準として「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」という記載がある。異型赤血球がこの基準に該当するか不明。
    *   **判断理由:** スクリーニング時の検査で異常値が確認されているため、除外基準に抵触する可能性がある。

*   **逸脱No.:** 4
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LBTESTCD = "AST", LBORRES = "40"
    *   **逸脱内容:** スクリーニング検査(SCREENING 1)において、血液検査の結果(AST: アスパラギン酸アミノトランスフェラーゼ)が基準値上限を超えている(HIGH)。
    *   **プロトコル該当箇所:** プロトコル3.4.2.2 Exclusion Criteria [27b]に、除外基準として「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」という記載がある。AST(SGOT) がこの基準に該当する。
    *   **判断理由:** スクリーニング時の検査で基準値上限を超えているため、除外基準に抵触する可能性がある。

*   **逸脱No.:** 5
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LBTESTCD = "MCV", LBORRES = "78"
    *   **逸脱内容:** 5回目の訪問(WEEK 4)において、血液検査の結果(MCV: 平均赤血球容積)が基準値下限を下回っている(LOW)。
    *   **プロトコル該当箇所:** プロトコル3.4.2.2 Exclusion Criteria [27b]に、除外基準として「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」という記載がある。
    *   **判断理由:** 5回目の訪問(WEEK 4)は、組み入れ基準を満たすかの評価タイミングではないため、除外基準には抵触しない。

*   **逸脱No.:** 6
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** LBTESTCD = "SPGRAV", LBORRES = "1.005"
    *   **逸脱内容:** 12回目の訪問(WEEK 24)において、尿検査の結果(SPGRAV: 尿比重)が基準値下限を下回っている(LOW)。
    *   **プロトコル該当箇所:** プロトコル3.4.2.2 Exclusion Criteria [27b]に、除外基準として「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」という記載がある。
    *   **判断理由:** 12回目の訪問(WEEK 24)は、組み入れ基準を満たすかの評価タイミングではないため、除外基準には抵触しない。

*   **逸脱No.:** 7
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE", TI.IETEST = "Diagnosis of probable AD as defined by NINCDS and the ADRDA guidelines"
    *   **逸脱内容:** 被験者の病歴にアルツハイマー病の記載がある。しかし、アルツハイマー病の診断は、組み入れ基準(INCL02)でNINCDSとADRDAのガイドラインに定義されている「probable AD」であることが求められている。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [2]
    *   **判断理由:** Medical History(MH)に記録された病名が、組み入れ基準で規定された診断基準を満たしているか確認する必要がある。もし満たしていなければプロトコル逸脱となる。

*   **逸脱No.:** 8
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** QS.QSTESTCD = "MHITM04", QSORRES = "ABSENT", TI.IETEST = "Modified Hachinski Ischemic Scale score of <= 4"
    *   **逸脱内容:** Modified Hachinski Ischemic Scaleの評価項目の一つであるNocturnal Confusion (夜間錯乱) が、評価の結果Absent (なし) と判定されている。Modified Hachinski Ischemic Scaleの合計スコアが4以下でなければならないという組み入れ基準(INCL04)を満たしているか確認する必要がある。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [4]
    *   **判断理由:** Modified Hachinski Ischemic Scaleの合計スコアが4を超えている場合、組み入れ基準を満たしていないため、プロトコル逸脱となる。

*   **逸脱No.:** 9
    *   **臨床試験結果への影響度合い:** Critical
    *   **変数名と値:** QS.QSTESTCD = "MMITM01", QSORRES = "4" , TI.IETEST = "MMSE score of 10 to 23."
    *   **逸脱内容:** MMSEの評価項目である "WHAT IS THE (YEAR) (SEASON) (DATE) ?" の評価が4点である。MMSEの合計スコアが10から23の間でなければならないという組み入れ基準(INCL03)を満たしているか確認する必要がある。
    *   **プロトコル該当箇所:** 3.4.2.1 Inclusion Criteria [3]
    *   **判断理由:** MMSEの合計スコアが10点未満、または23点を超えている場合、組み入れ基準を満たしていないため、プロトコル逸脱となる。

*   **逸脱No.:** 10
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDTC = "2014-01-03", EX.EXSTDTC = "2014-01-02"
    *   **逸脱内容:** 有害事象(AE) の開始日(AESTDTC)が、治験薬の投与開始日(EX.EXSTDTC)よりも早い。
    *   **プロトコル該当箇所:** 3.9.3.2.1 Adverse Event Reporting Requirements
    *   **判断理由:** 一般的に、有害事象は治験薬の投与後に発生すると考えられる。AESTDTCがEXSTDTCよりも早い場合、因果関係の評価に影響を与える可能性がある。

*   **逸脱No.:** 11
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** VSLOC = "ORAL CAVITY" and LBTESTCD = "COLOR" (Specific Gravity), KETONES, PH, UROBIL"
    *   **逸脱内容:** 尿検査(LB)とバイタルサイン(VS)で、採取部位(VSLOC)がORAL CAVITYとなっている。尿検査は尿から、バイタルサインは一般的に口腔から採取しない。
    *   **プロトコル該当箇所:** 3.9.3.3. Clinical Laboratory Tests
    *   **判断理由:** 検体採取部位が明らかに不適切なため、データの信頼性に疑義が生じる。

*   **逸脱No.:** 12
    *   **臨床試験結果への影響度合い:** None
    *   **変数名と値:** LB.LBDY = "63", VS.VSDY = "56"(ALP, Albumin, Chol, Creatinine, etc.)
    *   **逸脱内容:** 臨床検査(LB)とバイタルサイン(VS)で、VISIT(WEEK 8)の検査日(LBDY,VSDY)が異なっている。
    *   **プロトコル該当箇所:** 3.9.3.3. Clinical Laboratory Tests
    *   **判断理由:** LBDYとVSDYに1週間程度のずれが生じているが、検査日のずれは軽微であり、臨床的な解釈に大きな影響はないと考えられる。

*   **逸脱No.:** 13
    *   **臨床試験結果への影響度合い:** None
    *   **変数名と値:** LB.LBDY = "126", VS.VSDY = "112"(ALP, Albumin, Chol, Creatinine, etc.)
    *   **逸脱内容:** 臨床検査(LB)とバイタルサイン(VS)で、VISIT(WEEK 16)の検査日(LBDY,VSDY)が異なっている。
    *   **プロトコル該当箇所:** 3.9.3.3. Clinical Laboratory Tests
    *   **判断理由:** LBDYとVSDYに2週間程度のずれが生じているが、検査日のずれは軽微であり、臨床的な解釈に大きな影響はないと考えられる。

*   **逸脱No.:** 14
    *   **臨床試験結果への影響度合い:** None
    *   **変数名と値:** LB.LBDY = "29", VS.VSDY = "15"(ALP, Albumin, Chol, Creatinine, etc.)
    *   **逸脱内容:** 臨床検査(LB)とバイタルサイン(VS)で、VISIT(WEEK 4)の検査日(LBDY,VSDY)が異なっている。
    *   **プロトコル該当箇所:** 3.9.3.3. Clinical Laboratory Tests
    *   **判断理由:** LBDYとVSDYに2週間程度のずれが生じているが、検査日のずれは軽微であり、臨床的な解釈に大きな影響はないと考えられる。

---

**クエリ:**

*   **患者ID:** 01-701-1015
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE"
        *   **医療機関への問い合わせ文面:**
            被験者01-701-1015は、病歴にアルツハイマー病の記載がありますが、組み入れ基準で規定されているNINCDS/ADRDAガイドラインに準拠した「probable AD」の診断基準を満たしているか確認してください。
        *   **判断理由:** MHに記録された病名が、組み入れ基準で規定された診断基準を満たしているか確認する必要がある。もし満たしていなければプロトコル逸脱となる。

*   **患者ID:** 01-701-1015
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CMDECOD = "UNCODED" (NEOSPORIN /USA/), CMDOSU = "VIAL"
        *   **医療機関への問い合わせ文面:**
            被験者01-701-1015に投与されたNEOSPORIN /USA/ について、より詳細な薬剤名と剤形に関する情報を教えてください。特に、CMDOSU(投与単位)がVIALとなっていることの妥当性について確認させてください。
        *   **判断理由:** 報告された併用薬データの正確性を確認し、必要に応じて修正することで、データ品質を向上させることができます。

*   **患者ID:** 01-701-1015
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LBTESTCD = "ANISO", LBORRES = "1", LBREF = "ABNORMAL"
        *   **医療機関への問い合わせ文面:**
            被験者01-701-1015のスクリーニング検査におけるANISO（異型赤血球）の異常値について、臨床的な意義をご教示ください。また、この異常値がプロトコルの除外基準に該当するかどうかについて、治験責任医師の見解をお聞かせください。
        *   **判断理由:** 報告された臨床検査データの正確性を確認し、治験責任医師の医学的な判断に基づいてプロトコルからの逸脱を評価するため。

*   **患者ID:** 01-701-1015
    *   **クエリNo.:** 4
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LBTESTCD = "AST", LBORRES = "40", LBREF = "HIGH"
        *   **医療機関への問い合わせ文面:**
            被験者01-701-1015のスクリーニング検査におけるAST（アスパラギン酸アミノトランスフェラーゼ）の高値について、臨床的な意義をご教示ください。また、この高値がプロトコルの除外基準に該当するかどうかについて、治験責任医師の見解をお聞かせください。
        *   **判断理由:** 報告された臨床検査データの正確性を確認し、治験責任医師の医学的な判断に基づいてプロトコルからの逸脱を評価するため。

クエリなし


# 01-701-1387
## Task1: Clinical Review Results
患者ID: 01-701-1387
*   2014年02月23日 (Day -17): スクリーニング1回目の訪問。
    *   既往歴として、アルツハイマー病、多発性関節炎、鼻炎、肺炎、基底細胞癌、体位性めまい、失神、義歯装着、白内障、足関節浮腫、手のしびれ、扁桃摘出、抜歯が報告されている。
    *   教育レベルは12年。
    *   ADAS-Cog(11)サブスコアは44、ワード・リコール・タスクは9、オブジェクトと指の命名は4、遅延ワード・リコールは10、コマンドは2、構成的実行は4、観念的実行は2、見当識は7、ワード・リコーニションは6、注意/視覚探索タスクは0、迷路課題は240秒、発話能力は1、口頭言語の理解度は3、自発的な発話における単語検索困難は2、検査指示の想起は4。
    *   改訂神経精神インベントリー(NPI-X)総合スコアは26。妄想の頻度、重症度、苦痛はすべて0。幻覚の頻度は1、重症度は2、苦痛は0。興奮／攻撃性の頻度、重症度、苦痛はすべて0。うつ病／不快気分、不安、高揚／多幸症、無関心／無感情はすべて欠如。脱抑制の頻度は4、重症度は3、苦痛は3。易刺激性／易怒性の頻度、重症度、苦痛はすべて0。異常行動の頻度は4、重症度は3、苦痛は0。夜間行動の頻度は2、重症度は2、苦痛は0。食欲／摂食行動の変化は欠如。
    *   Disability Assessment for Dementia (DAD)総合スコアは1。各項目の内訳は、清潔保持：0、着衣：1、排泄：1、摂食：1、食事の準備：0、電話：0、外出：0、財務と通信：0、投薬：96、レジャーと家事：1。
    *   修正ハキンスキー虚血スコアは0。
    *   ECOTRINを頓服で内服。
    *   バイタルサイン：体温35.94℃、仰臥位での収縮期血圧72mmHg、拡張期血圧146mmHg、脈拍数74回/分。起立1分後の収縮期血圧136mmHg、拡張期血圧72mmHg、脈拍数82回/分。起立3分後の収縮期血圧137mmHg、拡張期血圧79mmHg、脈拍数79回/分。身長162.56cm、体重60.78kg。
    *   臨床検査：アルブミン40g/L、アルカリホスファターゼ68U/L、アラニンアミノトランスフェラーゼ12U/L、アスパラギン酸アミノトランスフェラーゼ18U/L、好塩基球0.05GI/L、ビリルビン6.84umol/L、血中尿素窒素4.641mmol/L、カルシウム2.37025mmol/L、コレステロール5.12028mmol/L、クレアチンキナーゼ50U/L、クロール105mmol/L、クレアチニン106.08umol/L、好酸球0.2GI/L、γ-GT12U/L、グルコース5.38447mmol/L、ヘマトクリット0.41、ヘモグロビン8.12986mmol/L、カリウム5.1mmol/L、白血球7.41GI/L、MCH1.8618fmol(Fe)、MCHC19.8592mmol/L、MCV93fL、リンパ球2.41GI/L、単球0.4GI/L、血小板191GI/L、リン5.0、総タンパク質73g/L、赤血球4.4TI/L、ナトリウム143mmol/L、尿酸4.3mg/dL、ケトン0、pH5.0、比重1.026、ウロビリノゲン0、甲状腺刺激ホルモン0.93mU/L、ビタミンB12 272.986pmol/L
*   2014年03月08日 (Day -4): スクリーニング2回目の訪問。
    *   ECOTRINを頓服で内服。
    *   バイタルサイン：仰臥位での拡張期血圧81mmHg、脈拍数72回/分。起立1分後の収縮期血圧138mmHg、拡張期血圧78mmHg、脈拍数80回/分。起立3分後の収縮期血圧146mmHg、拡張期血圧82mmHg、脈拍数84回/分。体温36.67℃。
*   2014年03月12日 (Day 1): ベースライン訪問。
    *   ECOTRINを頓服で内服。
    *   治験薬（プラセボ）投与開始。
    *   ADAS-Cog(11)サブスコアは44、ワード・リコール・タスクは9、オブジェクトと指の命名は4、遅延ワード・リコールは10、コマンドは2、構成的実行は4、観念的実行は2、見当識は7、ワード・リコーニションは6、注意/視覚探索タスクは0、迷路課題は240秒、発話能力は1、口頭言語の理解度は3、自発的な発話における単語検索困難は2、検査指示の想起は4。
    *   Disability Assessment for Dementia (DAD)総合スコアは1。各項目の内訳は、清潔保持：0、着衣：1、排泄：1、摂食：1、食事の準備：0、電話：0、外出：0、財務と通信：0、投薬：96、レジャーと家事：1。
    *   改訂神経精神インベントリー(NPI-X)総合スコアは26。妄想の頻度、重症度、苦痛はすべて0。幻覚の頻度は1、重症度は2、苦痛は0。興奮／攻撃性の頻度、重症度、苦痛はすべて0。うつ病／不快気分、不安、高揚／多幸症、無関心／無感情はすべて欠如。脱抑制の頻度は4、重症度は3、苦痛は3。易刺激性／易怒性の頻度、重症度、苦痛はすべて0。異常行動の頻度は4、重症度は3、苦痛は0。夜間行動の頻度は2、重症度は2、苦痛は0。食欲／摂食行動の変化は欠如。
    *   バイタルサイン：仰臥位での収縮期血圧159mmHg、拡張期血圧69mmHg、脈拍数75回/分。起立1分後の収縮期血圧136mmHg、拡張期血圧75mmHg、脈拍数79回/分。起立3分後の収縮期血圧134mmHg、拡張期血圧74mmHg、脈拍数80回/分。体温36.61℃、体重59.42kg。
*   2014年03月18日 (Day 7): 下痢、多汗症が発生。
*   2014年03月25日 (Day 14): 2週目の訪問。
    *   ECOTRINを頓服で内服。
    *   プロトコル違反のため、治験を中止。
    *   FINAL LAB VISIT実施。
    *   ADAS-Cog(11)サブスコアは44、ワード・リコール・タスクは8、オブジェクトと指の命名は3、遅延ワード・リコールは10、コマンドは3、構成的実行は4、観念的実行は3、見当識は5、ワード・リコーニションは9、注意/視覚探索タスクは0、迷路課題は240秒、発話能力は1、口頭言語の理解度は3、自発的な発話における単語検索困難は1、検査指示の想起は4。
    *   Disability Assessment for Dementia (DAD)総合スコアは0。各項目の内訳は、清潔保持：0、着衣：0、排泄：1、摂食：1、食事の準備：1、電話：0、外出：0、財務と通信：0、投薬：0、レジャーと家事：0。
    *   改訂神経精神インベントリー(NPI-X)総合スコアは2。妄想の頻度、重症度、苦痛はすべて0。幻覚の頻度、重症度、苦痛はすべて0。興奮／攻撃性の頻度、重症度、苦痛はすべて0。うつ病／不快気分、不安、高揚／多幸症、無関心／無感情はすべて欠如。脱抑制の頻度は1、重症度は1、苦痛は0。易刺激性／易怒性の頻度、重症度、苦痛はすべて0。異常行動の頻度は1、重症度は1、苦痛は0。夜間行動の頻度、重症度、苦痛はすべて0。食欲／摂食行動の変化は欠如。
    *   バイタルサイン：仰臥位での収縮期血圧135mmHg、拡張期血圧67mmHg、脈拍数73回/分。起立1分後の収縮期血圧130mmHg、拡張期血圧60mmHg、脈拍数86回/分。起立3分後の収縮期血圧129mmHg、拡張期血圧61mmHg、脈拍数83回/分。体温36.39℃、体重60.78kg。
    *   臨床検査：アルブミン39g/L、アルカリホスファターゼ58U/L、アラニンアミノトランスフェラーゼ12U/L、アスパラギン酸アミノトランスフェラーゼ20U/L、好塩基球0.04GI/L、ビリルビン6.84umol/L、血中尿素窒素5.355mmol/L、カルシウム2.22055mmol/L、コレステロール5.0427mmol/L、クレアチンキナーゼ55U/L、クロール112mmol/L、クレアチニン106.08umol/L、好酸球0.14GI/L、γ-GT10U/L、グルコース5.60651mmol/L、ヘマトクリット0.37、ヘモグロビン7.88162mmol/L、カリウム4.8mmol/L、白血球6.67GI/L、MCH1.8618fmol(Fe)、MCHC21.1004mmol/L、MCV88fL、リンパ球1.72GI/L、単球0.34GI/L、血小板185GI/L、リン5.0、総タンパク質72g/L、赤血球4.2TI/L、ナトリウム146mmol/L、尿酸4.5mg/dL、ケトン0、pH5.0、比重1.017、ウロビリノゲン0
*   2014年08月27日 (Day 169): 最終検索訪問。
    *   ECOTRINを頓服で内服。
    *   ADAS-Cog(11)サブスコアは59、ワード・リコール・タスクは9、オブジェクトと指の命名は3、遅延ワード・リコールは10、コマンドは3、構成的実行は5、観念的実行は5、見当識は7、ワード・リコーニションは10、注意/視覚探索タスクは0、迷路課題は240秒、発話能力は4、口頭言語の理解度は4、自発的な発話における単語検索困難は4、検査指示の想起は5。
    *   Disability Assessment for Dementia (DAD)総合スコアは96。各項目の内訳は、清潔保持：0、着衣：1、排泄：1、摂食：0、食事の準備：1、電話：0、外出：96、財務と通信：1、投薬：96、レジャーと家事：1。
    *   改訂神経精神インベントリー(NPI-X)総合スコアは16。妄想の頻度、重症度、苦痛はすべて0。幻覚の頻度は1、重症度は1、苦痛は0。興奮／攻撃性の頻度は2、重症度は3、苦痛は0。うつ病／不快気分、不安、高揚／多幸症、無関心／無感情はすべて欠如。脱抑制の頻度、重症度、苦痛はすべて0。易刺激性／易怒性の頻度、重症度、苦痛はすべて0。異常行動の頻度は3、重症度は3、苦痛は0。夜間行動は欠如。食欲／摂食行動の変化の頻度は1、重症度は1、苦痛は0。

---

患者ID: 01-701-1387
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Critical
    *   変数名と値: DS.DSTERM = "PROTOCOL VIOLATION", DS.DSDECOD = "PROTOCOL VIOLATION", DS.DSSTDTC = "2014-03-25", AE.AESTDTC = "2014-03-18", AE.AEENDTC = "2014-03-18"
    *   医療機関への問い合わせ文面:
        *   プロトコル違反の内容と、その違反がDSドメインに記録された2014年3月25日より前に発生したかどうかを確認してください。もしプロトコル違反が2014年3月25日より前に発生していた場合、Week2のVISITを実施したことの妥当性について説明してください。
        *  AEドメインに記録された下痢と多汗症の発現日が2014年3月18日となっていますが、治験薬の投与開始日（2014年3月12日）より前です。これらの有害事象は治験薬との関連性がないと判断された理由と、医学的な妥当性について説明してください。
    *   判断理由:
        *   DSドメインとAEドメインのデータに矛盾が認められました。DS.DSDECODが"PROTOCOL VIOLATION"であることから、プロトコルからの逸脱が治験に影響を与えた可能性があります。また、AEドメインの有害事象の発現日が治験薬投与開始日前であるため、医学的な妥当性を確認する必要があります。
## Task2: DM Review Results
**全体的なデータ品質の評価:**

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMDTC, CM.CMSTDTC, AE.AESTDTC, VS.VSORRES, VS.VSTPT, AE.AETERMとMH.MHTERMの整合性

**問題点:**

*   **問題No.: 1**
    *   **変数名と値:** CM.CMDTC = "2014-02-23", CM.CMSTDTC = "2012" (すべてレコード)
    *   **矛盾の内容:** CMドメインにおいて、CMDTC（Date/Time of Collection）がCMSTDTC（Start Date/Time of Medication）よりも未来の日付になっている。CMDTCはデータ収集日であり、CMSTDTCは服薬開始日であるため、CMDTCがCMSTDTCより前の日付になることは通常ありえない。
        *   レコード1: CMDTC = "2014-02-23", CMSTDTC = "2012"
        *   レコード2: CMDTC = "2014-03-08", CMSTDTC = "2012"
        *   レコード3: CMDTC = "2014-03-12", CMSTDTC = "2012"
        *   レコード4: CMDTC = "2014-03-25", CMSTDTC = "2012"
        *   レコード5: CMDTC = "2014-08-27", CMSTDTC = "2012"
    *   **問題点の原因（推測）:** データ入力エラー、日付フォーマットの誤解、またはCMSTDTCの年のみ記録というプロトコルの指示。
    *   **対応策（提案）:** CMDTCとCMSTDTCの正確な日付をデータソースで確認し、必要に応じて修正する。CMSTDTCに年しか記録しないことがプロトコルの指示である場合、その理由を明確にするためのメモを追加する。
*   **問題No.: 2**
    *   **変数名と値:** AE.AESTDTC = "2014-03-18", EX.EXSTDTC = "2014-03-12", EX.EXENDTC = "2014-03-25"
    *   **矛盾の内容:** AEドメインにおいて、AESTDTC（Start Date/Time of Adverse Event）がEXドメインのEXSTDTC（Start Date/Time of Treatment）より前になっている。治験薬投与前に有害事象が発生することは通常ない。
        *   AESTDTC = "2014-03-18" は、EXSTDTC = "2014-03-12" と EXENDTC = "2014-03-25" の期間に含まれている。
    *   **問題点の原因（推測）:** データ入力エラー、有害事象の開始日の誤り。
    *   **対応策（提案）:** AE.AESTDTCの正確な日付をデータソースで確認し、必要に応じて修正する。
*   **問題No.: 3**
    *   **変数名と値:** VS.VSORRES = "146" (DIABP, 1レコード目)
    *   **矛盾の内容:**  DMドメインにおいて、対象者の年齢は87歳である。VSドメインの1レコード目のDIABP（Diastolic Blood Pressure）の値が146 mmHgとなっており、高齢者のDIABPとしては異常値である可能性がある。他のバイタルサイン（SYSBP、PULSE）との整合性も確認する必要がある。
    *   **問題点の原因（推測）:** データ入力エラー、測定エラー、または患者の病歴によるもの。
    *   **対応策（提案）:** VS.VSORRESの正確な値をデータソースで確認し、必要に応じて修正する。DMとVSの他の変数との関連性を確認する。
*   **問題No.: 4**
    *   **変数名と値:** DS.DSTERM = "PROTOCOL VIOLATION", DS.VISIT = "WEEK 2"
    *   **矛盾の内容:** DSドメインにおいて、治験中止理由（DSTERM）が「PROTOCOL VIOLATION（プロトコル違反）」であるにもかかわらず、VISIT（Visit Name）が「WEEK 2」となっている。
    *   **問題点の原因（推測）:** データ入力エラー、またはプロトコルからの逸脱。
    *   **対応策（提案）:** プロトコル違反の内容と、それがWEEK 2の時点で発生したことを確認する。必要であれば、データソースを修正する。
*   **問題No.: 5**
    *   **変数名と値:** QS.DAITM19, QS.DAITM20, QS.DAITM25, QS.DAITM26, QS.DAITM27, QS.DAITM28, QS.DAITM29, DAITM34, DAITM35のRETRIEVALのQSORRESの値が"NA"となっている。
    *   **矛盾の内容:**　DISABILITY ASSESSMENT FOR DEMENTIA (DAD)に関する質問で、RETRIEVALの段階で実施されているにもかかわらず、"NA"となっている項目がある。RETRIEVALは治験薬投与終了後の評価であるため、本来であれば"NA"ではなく、ADLの評価が記録されるべきである。
    *   **問題点の原因（推測）:** 質問に対する回答が不可能、あるいは評価が実施されなかった。
    *   **対応策（提案）:** これらの項目が"NA"となっている理由を調査し、可能であれば適切なADL評価を収集する。
*   **問題No.: 6**
    *   **変数名と値:** AE.AETERM (Diarrhoea, Hyperhidrosis) と MH.MHTERMに記録されている過去の病歴
    *   **矛盾の内容:** AEに記録されている有害事象（Diarrhoea, Hyperhidrosis）が、MHに記録されている過去の病歴と関連があるかどうか確認が必要。Diarrhoeaを引き起こす可能性のある既往歴（胃腸疾患など）やHyperhidrosisを引き起こす可能性のある疾患の有無を調査する必要がある。
    *   **問題点の原因（推測）:** 
    *   **対応策（提案）:** AE.AETERMとMH.MHTERMの整合性を確認し、関連性がある場合はその旨を記録する。

**クエリの作成:**

*   **患者ID:** 01-701-1387
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMDTC = "2014-02-23", CM.CMSTDTC = "2012" (すべてレコード)
        *   **医療機関への問い合わせ文面:**
            *   CMドメインにおいて、CMDTC（Date/Time of Collection）がCMSTDTC（Start Date/Time of Medication）よりも未来の日付になっています。CMSTDTCの正しい日付（年、月、日）をご教示ください。
        *   **判断理由:** CMSTDTCの誤りは、併用薬の投与期間の解析に影響を与える可能性があり、主要評価項目に影響を及ぼす可能性があるため。
*   **患者ID:** 01-701-1387
    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AESTDTC = "2014-03-18", EX.EXSTDTC = "2014-03-12", EX.EXENDTC = "2014-03-25"
        *   **医療機関への問い合わせ文面:**
            *   AEドメインにおいて、AESTDTC（有害事象開始日）が2014-03-18となっていますが、EXドメインのEXSTDTC（治験薬投与開始日）は2014-03-12です。有害事象が治験薬投与前に発生したことになりますが、AESTDTCに誤りがないかご確認ください。
        *   **判断理由:** AESTDTCの誤りは、有害事象と治験薬の因果関係の評価に影響を与える可能性があり、患者の安全性評価に影響するため。
*   **患者ID:** 01-701-1387
    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** VS.VSORRES = "146" (DIABP, 1レコード目)
        *   **医療機関への問い合わせ文面:**
            *   87歳の患者さんのDIABPが146mmHgと高くなっていますが、測定に誤りがないか、あるいは患者さんの高血圧の既往歴や合併症について情報をご提供いただけますでしょうか？
        *   **判断理由:** VSORRESの異常値は、患者の安全に関わる可能性があり、データの信頼性を確認する必要があるため。
*   **患者ID:** 01-701-1387
    *   **クエリNo.: 4**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** DS.DSTERM = "PROTOCOL VIOLATION", DS.VISIT = "WEEK 2"
        *   **医療機関への問い合わせ文面:**
            *   DSドメインにおいて、治験中止理由がPROTOCOL VIOLATIONとなっていますが、具体的な違反内容についてご教示ください。
        *   **判断理由:** プロトコルからの重大な逸脱は、試験結果の解釈に影響を与え、規制当局への報告が必要となる可能性があるため。
*   **患者ID:** 01-701-1387
    *   **クエリNo.: 5**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** QS.DAITM19, QS.DAITM20, QS.DAITM25, QS.DAITM26, QS.DAITM27, QS.DAITM28, QS.DAITM29, DAITM34, DAITM35のRETRIEVALのQSORRESの値が"NA"となっている。
        *   **医療機関への問い合わせ文面:**
            *   DISABILITY ASSESSMENT FOR DEMENTIA (DAD)に関する質問で、RETRIEVAL（中止から24週後）の段階で、ADLの評価がNAとなっている項目が複数ありますが、評価が実施できなかった理由についてご教示ください。
        *   **判断理由:** 評価が欠損している場合、試験結果に影響を与える可能性があるため。


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1387
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMSTDTC=2012, CM.CMDTC=2014-02-23, CM.VISIT=SCREENING 1
    *   逸脱内容: 併用薬ECOTRINの開始日がReference Start Date/Timeより前になっている。CM.CMSTDTCが不適切。
    *   プロトコル該当箇所: プロトコルには併用薬に関する具体的な開始時期の規定はないが、一般的に試験期間外の薬剤使用は試験結果に影響を与える可能性がある。
    *   判断理由: CM.CMSTDTCがStudy開始より前であるため、データの正確性に疑義が生じる。

患者ID: 01-701-1387
*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DS.DSTERM=PROTOCOL VIOLATION, DS.VISIT=WEEK 2, DS.DSSTDTC=2014-03-25
    *   逸脱内容: 試験からのDiscontinuation理由がProtocol Violationである。
    *   プロトコル該当箇所: 3.10.1 Discontinuations 
    *   判断理由:PROTOCOL VIOLATIONにより試験を中止しているので詳細を確認する必要がある。

患者ID: 01-701-1387
*   逸脱No.: 3
    *   臨床試験結果への影響度合い: None
    *   変数名と値: VS.VSTEST=Diastolic Blood Pressure, VS.VISIT=SCREENING 1, VS.VSORRES=146
    *   逸脱内容: 仰臥位でのDiastolic Blood Pressureが146mmHg.
    *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [17]
    *   判断理由: スクリーニング時にUncontrolled hypertensionの基準を満たしている可能性がある。
患者ID: 01-701-1387
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: DS.DSTERM=PROTOCOL VIOLATION, DS.VISIT=WEEK 2, DS.DSSTDTC=2014-03-25
    *   医療機関への問い合わせ文面:
        *   被験者01-701-1387のWeek2（2014-03-25）での試験中止理由が「PROTOCOL VIOLATION」と報告されていますが、具体的にどのようなプロトコル違反があったのか教えてください。
        *   そのPROTOCOL VIOLATIONは、本試験の主要評価項目に影響を与える可能性はありますか？
    *   判断理由:プロトコル逸脱の内容によっては、試験結果に重大な影響を与える可能性があるため。

# 01-703-1403
## Task1: Clinical Review Results
```markdown
患者ID: 01-703-1403

YYYY年MM月DD日 (Day XX):

2012年12月05日 (Day -7): 教育レベルは12年。
2012年12月12日 (Day 1): 体重が177 LB。
2012年12月12日 (Day 1): 体重減少の有害事象が発生（開始）。
2012年12月13日 (Day 2): 軽度Myasthenia Gravis悪化、嘔吐の有害事象が発生（開始）。
2012年12月14日 (Day 3): 軽度Myasthenia Gravis悪化、嘔吐の有害事象が回復（終了）。
2012年12月15日 (Day 4): 胸部不快感の有害事象が発生（開始）。
2012年12月16日 (Day 5): 胸部不快感の有害事象が回復（終了）。
2012年12月19日 (Day 8): 体重減少の有害事象が継続。
2012年12月19日 (Day 8): 体重が165 LB。
2012年12月19日 (Day 8): 最終検査。
2013年01月08日 (Day 不明): 体重減少の有害事象が回復（終了）。

---

患者ID: 01-703-1403
  クエリNo.: 1
   臨床試験結果への影響度合い: Major
   変数名と値: AE.AEOUT = "NOT RECOVERED/NOT RESOLVED", AE.AEENDTC = "2012-12-19"
   医療機関への問い合わせ文面:
      有害事象「体重減少」について、2012年12月19日の時点では「未回復」と記録されていますが、その後の経過と最終的な転帰（回復/未回復）を確認してください。
   判断理由:
      安全性評価において、有害事象の転帰は重要な情報であり、データが矛盾しているため。

患者ID: 01-703-1403
  クエリNo.: 2
   臨床試験結果への影響度合い: Minor
   変数名と値: DM.ACTARMCD = "Xan_Lo", DM.ARM = "Xanomeline High Dose"
   医療機関への問い合わせ文面:
      DMドメインにおいて、ACTARM（Actual Arm）とARM（Planned Arm）が異なっています。患者はXanomeline Low Doseに割り当てられていますが、ARMはXanomeline High Doseとなっています。この不一致の原因を確認してください。
   判断理由:
      ACTARMとARMの一致は、患者が意図された治療を受けているかを確認するために重要です。
```
## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: DM.ACTARM, EX.EXSTDTCとEX.EXENDTC, MH.MHSTDTC, AEとRELRECの関連性, LB.LBORRESとLB.LBSTRESCの単位換算

問題点:

*   **問題No.1:**
    *   **変数名と値:** DM.ARMCD = "Xan\_Hi", DM.ARM = "Xanomeline High Dose", DM.ACTARMCD = "Xan\_Lo", DM.ACTARM = "Xanomeline Low Dose"
    *   **矛盾の内容:** 計画された投与群(DM.ARMCD, DM.ARM)と実際の投与群(DM.ACTARMCD, DM.ACTARM)が異なっている。DM.ARMCDとDM.ARMはXanomeline High Doseを計画された投与群として示しているが、DM.ACTARMCDとDM.ACTARMはXanomeline Low Doseを実際の投与群として示している。
    *   **問題点の原因（推測）:**
        *   データ入力エラー
        *   治験薬の割り当て間違い
        *   プロトコルからの逸脱
    *   **対応策（提案）:** 治験担当者に確認し、DM.ACTARMCDとDM.ACTARMをDM.ARMCDとDM.ARMと一致させるか、または差異の理由を特定する。

*   **問題No.2:**
    *   **変数名と値:** EX.EXSTDTC = "2012-12-12", EX.EXENDTC = "2012-12-13", AE.AESTDTC = "2012-12-12", AE.AEENDTC = "2012-12-19" (AEのWEIGHT DECREASED), DS.DSSTDTC = "2012-12-19"
    *   **矛盾の内容:** EX (Exposure) ドメインでは、治験薬の投与期間が2012-12-12から2012-12-13となっているが、AE (Adverse Event) ドメインでは、体重減少(WEIGHT DECREASED)の有害事象の期間が2012-12-12から2012-12-19となっている。DS(Disposition)ドメインでは、ADVERSE EVENTが2012-12-19に発生している。EXドメインの投与期間とAEドメインの有害事象の期間に矛盾がある。
    *   **問題点の原因（推測）:**
        *   AEのAESTDTCとAEENDTC、DSのDSSTDTCの日付の誤り
        *   EXとAE/DSの関連性の誤り
    *   **対応策（提案）:**
        *   原資料を確認し、EX.EXSTDTC、EX.EXENDTC、AE.AESTDTC、AE.AEENDTC、DS.DSSTDTCの日付が正しいことを確認する。
        *   AEとDSがEXと関連付けられていることが正しいか確認する。

*   **問題No.3:**
    *   **変数名と値:** MH.MHTERM = "ALZHEIMER'S DISEASE", MH.MHSTDTC = "2010-12-07"
    *   **矛盾の内容:** Medical Historyに登録されているAlzheimer's Diseaseの発症日が試験開始前2年より前になっている。
    *   **問題点の原因（推測）:**
        *   データ入力エラー
        *   MH.MHSTDTCの誤り
        *   TIドメインとの不整合
    *   **対応策（提案）:**
        *   原資料を確認し、MH.MHSTDTCの日付が正しいことを確認する。
        *   TIドメインを確認し、Exclusion Criteriaに抵触していないか確認する。

*   **問題No.4:**
    *   **変数名と値:** RELREC.IDVARVAL = " 2", RELID="01-703-1403-E01", AE.AESEQ=2, AE.AETERM = "MYASTHENIA GRAVIS AGGRAVATED", DS.DSDECOD="ADVERSE EVENT"
    *   **矛盾の内容:** USUBJIDが01-703-1403の被験者において、RELRECドメインでAEドメイン(AESEQ=2, AETERM = "MYASTHENIA GRAVIS AGGRAVATED")とDSドメイン(DSDECOD="ADVERSE EVENT")がRELID "01-703-1403-E01"で関連付けられている。しかし、RELIDはAEドメインのadverse eventとdisposition eventの関連性を示しているが、MH(Medical History)には"MYASTHENIA GRAVIS AGGRAVATED"に対応するデータがない。また、RELRECに記載されているAESEQの前に半角スペースが入っている。
    *   **問題点の原因（推測）:**
        *   RELRECテーブルのAEとDSの関連性の誤り
        *   データ入力エラー
    *   **対応策（提案）:**
        *   原資料を確認し、RELRECテーブルのAEとDSの関連性が正しいことを確認する。
        *   MHドメインに"MYASTHENIA GRAVIS AGGRAVATED"に対応するデータがあるか確認する。
        *   RELRECのAESEQに半角スペースが入っていることについて、許容されるべきか確認する。

*   **問題No.5:**
    *   **変数名と値:** LB.LBORRES = "4.1", LB.LBORRESU = "g/dL", LB.LBSTRESC = "41", LB.LBSTRESU = "g/L" (LBTESTCD=ALB)
    *   **矛盾の内容:** Albuminの検査結果について、LBORRES(Original Units)が4.1 g/dLで、LBSTRESC(Standard Units)が41 g/Lとなっている。単位がg/dLからg/Lに変換されているが、本来であれば4.1 g/dL = 41 g/Lとなるため、LBORRESとLBSTRESCで矛盾はない。しかし、他の検査項目も確認したところ、Bilirubin, Blood Urea Nitrogen, Calcium, Cholesterol, Creatinine, Phosphateについても、mg/dLからumol/Lまたはmmol/Lへの変換が行われているにもかかわらず、同様に単位換算が行われていないように見える。
    *   **問題点の原因（推測）:**
        *   LBORRESからLBSTRESCへの変換ロジックの誤り
    *   **対応策（提案）:**
        *   LBORRESからLBSTRESCへの変換ロジックを確認し、正しい単位換算が行われるように修正する。
        *   必要に応じてDefine.xmlのComputationMethodを修正する。

クエリの作成:

*   **患者ID:** 01-703-1403
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Critical
        *   **変数名と値:** DM.ARMCD = "Xan\_Hi", DM.ARM = "Xanomeline High Dose", DM.ACTARMCD = "Xan\_Lo", DM.ACTARM = "Xanomeline Low Dose"
        *   **医療機関への問い合わせ文面:** 
            *   被験者01-703-1403について、計画された投与群（DM.ARMCD, DM.ARM）と実際の投与群（DM.ACTARMCD, DM.ACTARM）が異なっています。DM.ARMCDとDM.ARMはXanomeline High Doseを計画された投与群として示していますが、DM.ACTARMCDとDM.ACTARMはXanomeline Low Doseを実際の投与群として示しています。どちらの投与群が正しいか確認してください。もしDM.ACTARMCDとDM.ACTARMが正しい場合、その理由（プロトコルからの逸脱など）も併せてご回答ください。
        *   **判断理由:** 投与群の誤りは、有効性と安全性の評価に重大な影響を与える可能性があるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-703-1403
逸脱No.: 1
臨床試験結果への影響度合い: Minor
変数名と値: DM.ACTARMCD: Xan_Lo, EX.EXTRT: XANOMELINE
逸脱内容: 被験者はXanomeline High Dose群に割り当てられたにもかかわらず、Xanomeline Low Dose（DM.ACTARMCD）で治療を受けており、治験薬（EX.EXTRT）が投与されている。
プロトコル該当箇所:
*   セクション3.5 Patient Assignment: 患者は、治験薬としてXanomeline High Dose群に割り当てられること。
*   TSドメインでは、54mgと81mgの2種類の投与量が規定されている。
判断理由: DM.ARMCDとEX.EXTRTの値が一致しない。被験者はXanomeline High Dose群に割り当てられたにもかかわらず、DM.ACTARMCDとEX.EXTRTから判断すると、Xanomeline Low Doseで治療を受けている。

患者ID: 01-703-1403
クエリNo.: 1
臨床試験結果への影響度合い: Major
変数名と値: DM.ARMCD: Xan_Hi
医療機関への問い合わせ文面:
被験者01-703-1403は、DMドメインにおいてXanomeline High Dose群に割り当てられていますが、実際に投与された治験薬の用量（EXDOSE）と投与群（ACTARMCD）を確認してください。もし投与間違いがあった場合、その理由と、治験薬の投与計画に沿った用量が投与された期間を教えてください。
判断理由: 治験薬の投与間違いは、試験結果に重大な影響を与える可能性があるため。


# 01-701-1097
## Task1: Clinical Review Results
患者ID: 01-701-1097

*   2013年12月23日 (Day -9): スクリーニング1回目の検査で、ナトリウムが基準値より低い(134 mEq/L, 基準値: 135-145 mEq/L)
*   2014年02月26日 (Day 57): APPLICATION SITE PRURITUS (適用部位掻痒) の有害事象が発生、軽度と判断。APPLICATION SITE VESICLES (適用部位小胞) の有害事象が発生、軽度と判断。PRURITUS GENERALISED (全身性掻痒) の有害事象が発生、中等度と判断。
*   2014年02月26日 (Day 57): 好酸球数が基準値超え (0.89 THOU/uL, 基準値: 0-0.57 THOU/uL)
*   2014年03月26日 (Day 85): PRURITUS GENERALISED (全身性掻痒) の有害事象が発生、中等度と判断。好酸球数が基準値超え (0.87 THOU/uL, 基準値: 0-0.57 THOU/uL)
*   2014年04月23日 (Day 113): NASAL CONGESTION (鼻閉) の有害事象が発生、軽度と判断。PHARYNGOLARYNGEAL PAIN (咽喉頭痛) の有害事象が発生、軽度と判断。PRURITUS GENERALISED (全身性掻痒) の有害事象が発生、中等度と判断。
*   2014年05月21日 (Day 141): APPLICATION SITE PRURITUS (適用部位掻痒) の有害事象が発生。

---

患者ID: 01-701-1097
*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDTC = 2014-02-21, AE.AEENDTC = "" (APPLICATION SITE PRURITUS, AESEQ=4) および AE.AESTDTC = 2014-02-21, AE.AEENDTC = "" (APPLICATION SITE PRURITUS, AESEQ=10)
    *   **医療機関への問い合わせ文面:** APPLICATION SITE PRURITUS (適用部位掻痒) のAESEQ=4とAESEQ=10について、AEENDTC (有害事象終了日) が空欄ですが、有害事象は現在も継続中でしょうか？
    *   **判断理由:** APPLICATION SITE PRURITUS (適用部位掻痒) が2014年02月21日に発症してから、AEENDTC (有害事象終了日) が空欄のままになっています。APPLICATION SITE PRURITUS (適用部位掻痒) は治癒せずにWEEK 26まで続いていると解釈できます。重要な有害事象であるAPPLICATION SITE PRURITUS (適用部位掻痒) がいつ治癒したのか、または治癒していないのかを確認する必要があります。APPLICATION SITE PRURITUS (適用部位掻痒) は投与部位に発生しているため、治験薬との関連も疑われます。
## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMSTDTC, AE.AESTDTC, AE.AEENDTC, LB.LBDTC, VS.VSDTC, 

問題点:

*   問題No.: 1
    *   変数名と値: CM.CMTRT = "CENTRUM", CM.CMSTDTC = "2013-10"
    *   矛盾の内容: CMTRT(CENTRUM) の CMSTDTC がすべて "2013-10" となっており、CMDTC(2013-12-23, 2013-12-30, 2014-01-01など)と年月の整合性がとれていません。また、CMENDTCがないため、いつまでCENTRUMを服用していたのか不明です。
    *   問題点の原因（推測）: CMSTDTC のデータ入力時の誤り。または、CMENDTCが本来入力されるべきところ欠損している。
    *   対応策（提案）: CMTRT(CENTRUM)のCMSTDTC, CMENDTCの値を、原資料（CRFなど）で確認し、修正してください。

*   問題No.: 2
    *   変数名と値: AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2014-02-21", AE.AEENDTC = "" (レコード4)
    *   矛盾の内容: AE04とAE10で、AETERM（APPLICATION SITE PRURITUS）のAESTDTC（2014-02-21）が同じですが、AEDTCがそれぞれ2014-02-26と2014-05-21と異なっています。APPLICATION SITE PRURITUSが、2回発生したADイベントなのか、同じADイベントが続いているのか確認が必要です。
    *   問題点の原因（推測）: AEのデータ入力時の誤り
    *   対応策（提案）: AETERM（APPLICATION SITE PRURITUS）が、2回発生したADイベントなのか、同じADイベントが続いているのか、症例担当者に確認し、AESTDTC、AEENDTC, AEDTCの値を修正してください。

*   問題No.: 3
    *   変数名と値: VS.VSTESTCD = "TEMP", VS.VSORRES = "93.7", VS.VSORRESU = "F" (レコード133)
    *   矛盾の内容: 体温が93.7Fは、医学的に生存困難な低体温であり、データ異常値の可能性が高い。
    *   問題点の原因（推測）: VSORRES のデータ入力時の誤り。
    *   対応策（提案）: VSORRES の値を、原資料（CRFなど）で確認し、修正してください。

クエリ:
*   患者ID: 01-701-1097
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMTRT = "CENTRUM", CM.CMSTDTC = "2013-10"
        *   医療機関への問い合わせ文面:
            *   被験者01-701-1097の併用薬CENTRUMの投与開始日について、記録されている2013年10月は、データ収集日の2013-12-23より前であることは確認できますが、より正確な開始年月日を教えてください。
            *   また、CENTRUMの投与終了日を教えてください。
        *   判断理由: 併用薬の投与期間は、試験結果に影響を与える可能性があるため。
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2014-02-21", AE.AEENDTC = "" (レコード4), AEDTC = "2014-02-26",
                                   AE.AETERM = "APPLICATION SITE PRURITUS", AE.AESTDTC = "2014-02-21", AE.AEENDTC = "" (レコード10), AEDTC = "2014-05-21"
        *   医療機関への問い合わせ文面:
            *   被験者01-701-1097に発生した有害事象APPLICATION SITE PRURITUSについて、開始日が同じ2014年02月21日のADイベントは、それぞれ別のイベントとして扱うべきか、もしくは1つのイベントとして扱うべきか判断するための情報を教えてください。
            *   また、もし別のイベントとして扱う場合、レコード10のADイベントAPPLICATION SITE PRURITUSの開始日（AESTDTC）は2014年02月21日で正しいか、教えてください。
        *   判断理由: 類似した有害事象が複数回発生している場合、正確なイベントの把握が必要です。
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Critical
        *   変数名と値: VS.VSTESTCD = "TEMP", VS.VSORRES = "93.7", VS.VSORRESU = "F" (レコード133)
        *   医療機関への問い合わせ文面:
            *   被験者01-701-1097の体温について、記録されている93.7Fは正しい値ですか？もしそうでない場合、正しい値を教えてください。
        *   判断理由: 医学的にありえない異常値であるため。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1097
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: DM.AGE = 68, TI.IETEST = Males and postmenopausal females at least 50 years of age.
    *   逸脱内容: 被験者01-701-1097は男性(DM.SEX = M)であり、組み入れ基準[1]「50歳以上の男性および閉経後の女性」を満たしているため、DM.AGEの68歳という年齢情報は冗長である。
    *   プロトコル該当箇所: 3.4.2.1 Inclusion Criteria [1]
    *   判断理由: プロトコルでは、50歳以上という年齢基準は組み入れ基準を満たすための必要条件ではない。年齢はDMドメインで必須の情報ではないため、逸脱とはみなさない。

患者ID: 01-701-1097
*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: CM.CMSTDTC = "2013-10", VISITNUM = 1, VISIT = "SCREENING 1"
    *   逸脱内容: 併用薬CENTRUMの開始日がスクリーニング期間中（VISITNUM=1, VISIT="SCREENING 1"）に記録されているが、CMSTDTCの日付がYYYY-MM形式で提供されているため、正確な開始日が不明。
    *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [31b]
    *   判断理由: CMSTDTCがYYYY-MM形式のため、併用禁止薬の服薬期間から除外する必要があるか判断できない。
    
患者ID: 01-701-1097
*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.SODIUM = 134, LBNRIND = LOW, VISIT = "SCREENING 1"
    *   逸脱内容: スクリーニング1(VISIT="SCREENING 1")において、ナトリウム値が134 mEq/Lと基準範囲(135-145 mEq/L)を下回っている。
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [27b]
    *   判断理由: スクリーニング時の検査値異常は、除外基準に抵触する可能性がある。ただし、臨床的意義は担当医師の判断に委ねられている。

患者ID: 01-701-1097
*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE", MHSTDTC = "2005-09-22"
    *   逸脱内容: Medical Historyにアルツハイマー病（ALZHEIMER'S DISEASE）の既往歴があり、Exclusion Criteria[12]に抵触する可能性がある
    *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [12]
    *   判断理由: この試験の組み入れ対象は「軽度から中程度のアルツハイマー病」患者である。Medical Historyに「アルツハイマー病」の記載がある場合、試験への組み入れ基準を満たさない可能性がある。

患者ID: 01-701-1097
*   逸脱No.: 5
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: LB.EOS = 0.89, LBNRIND = HIGH, VISIT = "WEEK 8"、LB.EOS = 0.87, LBNRIND = HIGH, VISIT = "WEEK 12"
    *   逸脱内容: Week8とWeek12で好酸球の値が基準値上限(0.57 THOU/uL)を超えている。
    *   プロトコル該当箇所: 3.9.3.4 Other Safety Measures
    *   判断理由: プロトコルに規定された手順（3.9.3.4）に従い、好酸球増加の原因特定と適切な対応（繰り返しの検査など）が実施されているか確認する必要がある。

患者ID: 01-701-1097
*   逸脱No.: 6
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: QS.DAITM27 = NA, VISIT = "WEEK 24"、QS.DAITM28 = NA, VISIT = "WEEK 24"、QS.DAITM29 = NA, VISIT = "WEEK 24"
    *   逸脱内容: Disability Assessment for Dementia (DAD)において、WEEK24の３項目が「NA（非該当）」となっている。
    *   プロトコル該当箇所: 3.9.1.1 Efficacy Measures
    *   判断理由: 可能な限りすべての評価項目についてデータを収集する必要がある。評価が「非該当」と判断された理由を確認する必要がある。

*   患者ID: 01-701-1097
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE", MHSTDTC = "2005-09-22"
        *   医療機関への問い合わせ文面:
            被験者01-701-1097のMedical Historyに「ALZHEIMER'S DISEASE」の記載がありますが、本試験の対象は「軽度から中程度のアルツハイマー病」とされています。Medical HistoryのALZHEIMER'S DISEASEは、本試験で評価対象となるアルツハイマー病と同一の病状を指すものか、あるいは過去の病歴を示すものかご教示ください。また、組み入れ基準を満たしているかどうかの判断根拠をご説明ください。
        *   判断理由: 試験への適格性を確認するため。

*   患者ID: 01-701-1097
    *   クエリNo.: 2
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMSTDTC = "2013-10", VISITNUM = 1, VISIT = "SCREENING 1"
        *   医療機関への問い合わせ文面:
            被験者01-701-1097の併用薬CENTRUMのCMSTDTCがYYYY-MM形式で記録されています。正確なCMSTDTC（YYYY-MM-DD形式）をご教示ください。
        *   判断理由: 併用禁止薬に該当するかどうかを正確に判断するために、正確な開始日を把握する必要があるため。

*   患者ID: 01-701-1097
    *   クエリNo.: 3
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LB.EOS = 0.89, LBNRIND = HIGH, VISIT = "WEEK 8"、LB.EOS = 0.87, LBNRIND = HIGH, VISIT = "WEEK 12"
        *   医療機関への問い合わせ文面:
            被験者01-701-1097は、Week8とWeek12において好酸球の値が基準値上限を超えていますが、本プロトコルで規定された手順（3.9.3.4）に従い、好酸球増加の原因特定と適切な対応（繰り返しの検査など）が実施されているか、ご回答ください。
        *   判断理由: プロトコルで規定された手順が遵守されているかどうか確認するため。

*   患者ID: 01-701-1097
    *   クエリNo.: 4
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: QS.DAITM27 = NA, VISIT = "WEEK 24"、QS.DAITM28 = NA, VISIT = "WEEK 24"、QS.DAITM29 = NA, VISIT = "WEEK 24"
        *   医療機関への問い合わせ文面:
            被験者01-701-1097のWEEK24のDisability Assessment for Dementia (DAD)について、DAITM27、DAITM28、DAITM29の3項目がNA（非該当）と評価されています。評価がNAとなった理由についてご回答ください。
        *   判断理由: 有効性評価の完全性を担保するため、評価が「非該当」と判断された理由を確認し、データ収集における潜在的な問題点を特定するため。

# 01-704-1009
## Task1: Clinical Review Results
患者ID: 01-704-1009

*   2013年08月20日 (Day -7): BENADRYL (25 mg, PRN, ORAL) および BUFFERIN (325 mg, PRN, ORAL) を併用開始。MULTIVITAMIN (1 TABLET, QD, ORAL) および VITAMIN E (400 IU, QD, ORAL) も併用。
*   2013年08月24日 (Day -1): BENADRYL (25 mg, PRN, ORAL) および BUFFERIN (325 mg, PRN, ORAL) を併用。CLARITIN (10 mg, QD, ORAL) を併用開始 (2013年08月21日開始)。MULTIVITAMIN (1 TABLET, QD, ORAL) および VITAMIN E (400 IU, QD, ORAL) も併用。
*   2013年08月27日 (Day 1): BUFFERIN (325 mg, PRN, ORAL) および CLARITIN (10 mg, QD, ORAL) を併用。MULTIVITAMIN (1 TABLET, QD, ORAL) および VITAMIN E (400 IU, QD, ORAL) も併用。
*   2013年09月05日 (Day 10): FATIGUE および MALAISE (いずれもMILD) を発現。
*   2013年09月14日 (Day 19): BUFFERIN (325 mg, PRN, ORAL) および CLARITIN (10 mg, QD, ORAL) を併用。MULTIVITAMIN (1 TABLET, QD, ORAL) および VITAMIN E (400 IU, QD, ORAL) も併用。RASH (MILD) を発現。ALTが基準値上限を超過 (39 U/L, 基準値上限: 35 U/L)。ヘモグロビン (HGB) が基準値下限を下回る (11.1 g/dL, 基準値下限: 12.5 g/dL)。リンパ球 (LYM) が基準値下限を下回る (0.72 THOU/uL, 基準値下限: 0.8 THOU/uL)。血中ナトリウム (SODIUM) が基準値上限を超える (146 mEq/L, 基準値上限: 145 mEq/L)。AMBUL ECG PLACEMENT を実施。
*   2013年09月15日 (Day 20): 治験薬 (XANOMELINE, 54 mg, TRANSDERMAL) 投与開始。
*   2013年09月17日 (Day 22): DIZZINESS (MILD) を発現。
*   2013年09月22日 (Day 27): NAUSEA (MILD) を発現。
*   2013年09月23日 (Day 28): NAUSEA 軽快。
*   2013年09月25日 (Day 30): 治験薬 (XANOMELINE, 54 mg, TRANSDERMAL) 投与終了。
*   2013年09月27日 (Day 32): MALAISE 軽快。
*   2013年10月02日 (Day 37): BUFFERIN (325 mg, PRN, ORAL) および CLARITIN (10 mg, QD, ORAL) を併用。MULTIVITAMIN (1 TABLET, QD, ORAL) および VITAMIN E (400 IU, QD, ORAL) も併用。DIZZINESS, CHRONIC KIDNEY DISEASE, MALAISE, NAUSEAを発現。ADAS-Cog(11) Subscore がベースラインから悪化 (22 から 26 へ増加)。Disability Assessment for Dementia (DAD) への回答は、多くの項目で "Y" (1) から "NA" (96) へと変化。試験を中止。

---
患者ID: 01-704-1009

*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" (DIZZINESS, FATIGUE, RASH)
    *   医療機関への問い合わせ文面: DIZZINESS, FATIGUE, RASH について、2013年10月02日以降の転帰を教えてください。
    *   判断理由: 転帰が未解決の有害事象は、患者の安全性評価に影響を与える可能性があります。

*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: LB.LBTESTCD = "HGB", VISIT = "WEEK 2", LBSTRESN = 11.1 "g/dL"
    *   医療機関への問い合わせ文面: ヘモグロビン (HGB) の値が 2013年9月14日に 11.1 g/dL と低下していますが、臨床的な対応は行われましたか？
    *   判断理由: ヘモグロビンの低下は貧血を示唆し、患者の健康状態に影響を与える可能性があります。

*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: DS.DSTERM = "TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS", DSDECOD = "WITHDRAWAL BY SUBJECT"
    *   医療機関への問い合わせ文面: 2013年10月02日に「時間消費が多すぎるため、PTは将来のホルターを拒否した」との理由で試験を中止していますが、詳細な経緯と、この判断が安全性に影響を与えないことを確認してください。
    *   判断理由: 試験中止の理由は、安全性に影響を与える可能性があります。

*   クエリNo.: 4
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: VS.VSTESTCD = "SYSBP", VISIT = "BASELINE", VSTPT = "AFTER LYING DOWN FOR 5 MINUTES", VSORRES = 146 "mmHg"
    *   医療機関への問い合わせ文面: ベースライン測定時の血圧がやや高いですが、降圧剤の投与など、血圧を下げるための対応は行われましたか？
    *   判断理由: 基準値上限を大きく超える血圧ではないものの、高血圧の既往歴 (MH.MHTERM = "HISTORY OF HYPERTENSION") があるため。

*   クエリNo.: 5
    *   臨床試験結果への影響度合い: Minor
    *   変数名と値: 質問票の回答 (DISABILITY ASSESSMENT FOR DEMENTIA (DAD)) が、BASELINE (3) から WEEK 4 (5) にかけて、ほとんどの項目で "Y" (1) から "NA" (96) に変化
    *   医療機関への問い合わせ文面:  DISABILITY ASSESSMENT FOR DEMENTIA (DAD) への回答について、質問の意図を正しく理解できているか確認してください。
    *   判断理由: ADAS-Cog(11) Subscore がベースラインから悪化しているにもかかわらず、DADスコアも悪化していることの整合性を確認するため。

---

## Task2: DM Review Results
データ整合性レビューとクエリ作成を開始します。

**1. データ整合性レビュー:**

*   **全体的なデータ品質の評価:**
    *   総合評価: 一部問題あり
    *   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, LB.ALT, LB.CL, LB.HGB, LB.LYM, LB.SODIUM, QS.DAITM18, QS.DAITM19, QS.DAITM20

*   **問題点:**
    *   **問題No.: 1**
        *   **変数名と値:** CM.CMSTDTC = "2009", CM.CMENDTC = "2013-08" (1行目), CM.CMSTDTC = "2009", CM.CMENDTC = "2013-08" (2行目), CM.CMSTDTC = "2009", CM.CMENDTC = "" (3行目), CM.CMSTDTC = "2009", CM.CMENDTC = "" (4行目), CM.CMSTDTC = "2009", CM.CMENDTC = "" (5行目), CM.CMSTDTC = "2009", CM.CMENDTC = "" (6行目), CM.CMSTDTC = "2009", CM.CMENDTC = "" (7行目), CM.CMSTDTC = "2013-08-21", CM.CMENDTC = "" (9行目), CM.CMSTDTC = "2013-08-21", CM.CMENDTC = "" (10行目), CM.CMSTDTC = "2013-08-21", CM.CMENDTC = "" (11行目), CM.CMSTDTC = "2013-08-08", CM.CMENDTC = "" (13行目), CM.CMSTDTC = "2013-08-08", CM.CMENDTC = "" (14行目), CM.CMSTDTC = "2013-08-08", CM.CMENDTC = "" (15行目), CM.CMSTDTC = "2013-08-08", CM.CMENDTC = "" (16行目), CM.CMSTDTC = "2013-04", CM.CMENDTC = "" (17行目), CM.CMSTDTC = "2013-04", CM.CMENDTC = "" (18行目), CM.CMSTDTC = "2013-04", CM.CMENDTC = "" (19行目), CM.CMSTDTC = "2013-04", CM.CMENDTC = "" (20行目), CM.CMSTDTC = "2013-04", CM.CMENDTC = "" (21行目)
        *   **矛盾の内容:** CMSTDTCとCMENDTCの値が日付として不適切。CMSTDTCが2009年となっている場合、試験期間（2013年）と矛盾する。CMENDTCが欠損している場合、併用薬の使用期間が不明確になる。
        *   **問題点の原因（推測）:** データ入力時の誤り、またはデータの変換/加工時の問題。
        *   **対応策（提案）:**
            1.  CMドメインのデータソース（CRFなど）を確認し、CMSTDTCとCMENDTCの正確な日付を特定する。
            2.  必要に応じて、データ入力者に問い合わせて、正しい日付を取得する。
            3.  CMENDTCが欠損している理由を確認し、必要に応じて補完する。

    *   **問題No.: 2**
        *   **変数名と値:** LB.LBTESTCD = "ALT", LB.LBORRES = "39", LB.LBNRIND = "HIGH" (37行目)
        *   **矛盾の内容:** ALT (アラニンアミノトランスフェラーゼ) の値が39 U/Lで、LB.LBORNRHIが35 U/Lであるにもかかわらず、LBNRINDが"HIGH"となっている。
        *   **問題点の原因（推測）:** データ入力時の誤り、またはLBNRINDの判定ロジックの誤り。
        *   **対応策（提案）:**
            1.  LBドメインのデータソース（検査レポートなど）を確認し、ALTの正確な値を特定する。
            2.  LBNRINDの判定ロジックが正しく実装されているか確認する。

    *   **問題No.: 3**
        *   **変数名と値:** LB.LBTESTCD = "CL", LBORRES = "113", LBNRIND = "HIGH" (45行目)
        *   **矛盾の内容:**  CL (塩化物) の値が113 mEq/Lで、LBORNRHIが112 mEq/Lであるにもかかわらず、LBNRINDが"HIGH"となっている。
        *   **問題点の原因（推測）:** データ入力時の誤り、またはLBNRINDの判定ロジックの誤り。
        *   **対応策（提案）:**
            1. LBドメインのデータソースを確認し、CLの正確な値を特定する。
            2. LBNRINDの判定ロジックが正しく実装されているか確認する。

    *   **問題No.: 4**
        *   **変数名と値:** LB.LBTESTCD = "HGB", LBORRES = "12.4", LBNRIND = "LOW" (17行目), LB.LBTESTCD = "HGB", LBORRES = "11.1", LBNRIND = "LOW" (52行目)
        *   **矛盾の内容:** Hemoglobin (HGB) の検査結果がReference Range Lower Limit (LBORNRLO) を下回っているにもかかわらず、Baseline Flag（LBBLFL）が"Y"に設定されている。
        *   **問題点の原因（推測）:** HGB検査値の異常値（LOW）とBaseline Flagの関連性の誤り、またはLBBLFLの設定ロジックの誤り。
        *   **対応策（提案）:**
            1.  LBドメインのデータソースを確認し、HGBの正確な値を特定する。
            2.  LBBLFLの設定ロジックが正しく実装されているか確認する。

    *   **問題No.: 5**
        *   **変数名と値:** LB.LBTESTCD = "LYM", LBORRES = "0.72", LBNRIND = "LOW" (55行目)
        *   **矛盾の内容:** リンパ球数 (LYM) の検査結果がReference Range Lower Limit (0.8) を下回っているにもかかわらず、Reference Range Indicator（LBNRIND）が"LOW"に設定されている。
        *   **問題点の原因（推測）:** LYM検査値の異常値（LOW）とLBNRINDの関連性の誤り。
        *   **対応策（提案）:**
            1.  LBドメインのデータソースを確認し、LYMの正確な値を特定する。
            2.  LBNRINDの設定ロジックが正しく実装されているか確認する。

    *   **問題No.: 6**
        *   **変数名と値:** LB.LBTESTCD = "SODIUM", LBORRES = "146", LBNRIND = "HIGH" (60行目)
        *   **矛盾の内容:**  ナトリウム (SODIUM) の値が146 mEq/Lで、LBORNRHIが145 mEq/Lであるにもかかわらず、LBNRINDが"HIGH"となっている。
        *   **問題点の原因（推測）:** データ入力時の誤り、またはLBNRINDの判定ロジックの誤り。
        *   **対応策（提案）:**
            1. LBドメインのデータソースを確認し、SODIUMの正確な値を特定する。
            2. LBNRINDの判定ロジックが正しく実装されているか確認する。

    *   **問題No.: 7**
        *   **変数名と値:** QS.QSTESTCD = "DAITM18", QSORRES = "Y", QSSTRESC = "96" (4018行目), QS.QSTESTCD = "DAITM19", QSORRES = "NA", QSSTRESC = "96" (4019行目), QS.QSTESTCD = "DAITM20", QSORRES = "NA", QSSTRESC = "96" (4020行目)
        *   **矛盾の内容:** QSORRESが"Y"または"NA"であるにもかかわらず、QSSTRESCが"96"となっている。QSSTRESCが96の場合、QSORRESはNAである必要がある。
        *   **問題点の原因（推測）:** データ入力時の矛盾、またはQSSTRESCの導出ロジックの誤り。
        *   **対応策（提案）:**
            1.  QSドメインのデータソースを確認し、DAITM18, DAITM19, DAITM20の正確な値を特定する。
            2.  QSSTRESCの導出ロジックが正しく実装されているか確認する。

**2. クエリの作成:**

*   **患者ID:** 01-704-1009
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** CM.CMSTDTC, CM.CMENDTC
        *   **医療機関への問い合わせ文面:** 患者ID: 01-704-1009 の併用薬(CM)データについて、CMTRT (薬剤名) ごとに、CMSTDTC (併用薬開始日) と CMENDTC (併用薬終了日) の日付を正確に教えてください。特に、以下の点について確認をお願いします。
            *   BENADRYL, BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN E のCMSTDTCが2009年または2013年8月など不完全な日付になっていますが、正しい日付を教えてください。
            *   BUFFERIN, CLARITIN, MULTIVITAMIN のCMENDTCが欠損していますが、併用を中止した場合は、中止日を教えてください。
        *   **判断理由:** 併用薬の開始日と終了日は、患者の安全性評価や有効性評価に重要な情報であり、不正確な日付は解析結果に影響を与える可能性があります。

    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "ALT", LB.LBORRES
        *   **医療機関への問い合わせ文面:** 患者ID: 01-704-1009 のALT検査値について、Week2 (VISITNUM=4) のLBORRES（オリジナル値）が39 U/Lですが、データソースに記録されている検査値と単位を教えてください。LBNRINDが"HIGH"となっている根拠 (施設基準値等) についても情報があればご提供ください。
        *   **判断理由:**  ALT検査値は肝機能評価に重要な指標であり、誤った値は安全性評価に影響を与える可能性があります。

    *   **クエリNo.: 3**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "CL", LBORRES
        *   **医療機関への問い合わせ文面:** 患者ID: 01-704-1009 のCL検査値について、Week2 (VISITNUM=4) のLBORRES（オリジナル値）が113 mEq/Lですが、データソースに記録されている検査値と単位を教えてください。LBNRINDが"HIGH"となっている根拠 (施設基準値等) についても情報があればご提供ください。
        *   **判断理由:**  CL検査値は電解質評価に重要な指標であり、誤った値は安全性評価に影響を与える可能性があります。

    *   **クエリNo.: 4**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "HGB", LBORRES（1行目のHGB）, VISITNUM
        *   **医療機関への問い合わせ文面:** 患者ID: 01-704-1009 のHGB検査値について、SCREENING 1 (VISITNUM=1) とWEEK2 (VISITNUM=4) のLBORRES（オリジナル値）がそれぞれ12.4 g/dL, 11.1 g/dLとなっていますが、データソースに記録されている検査値を教えてください。
        *   **判断理由:**  HGB検査値は貧血評価に重要な指標であり、誤った値は安全性評価に影響を与える可能性があります。

    *   **クエリNo.: 5**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD = "SODIUM", LBORRES
        *   **医療機関への問い合わせ文面:** 患者ID: 01-704-1009 のSODIUM検査値について、Week2 (VISITNUM=4) のLBORRES（オリジナル値）が146 mEq/Lですが、データソースに記録されている検査値と単位を教えてください。LBNRINDが"HIGH"となっている根拠 (施設基準値等) についても情報があればご提供ください。
        *   **判断理由:**  SODIUM検査値は電解質評価に重要な指標であり、誤った値は安全性評価に影響を与える可能性があります。

## Task3: Protocol Deviation Review Results
**患者ID:** 01-704-1009
*   **逸脱No.:** 1
    *   **臨床試験結果への影響度合い:** Minor
    *   **変数名と値:** DSDECOD = "WITHDRAWAL BY SUBJECT", VISIT = "WEEK 4", DSDTC = "2013-10-02", EXENDTC = "2013-09-25"
    *   **逸脱内容:** 治験薬の投与期間が、プロトコルに規定された26週間よりも短い。
    *   **プロトコル該当箇所:** 3.1 Summary of Study Design
    *   **判断理由:** プロトコル3.1には、試験期間が26週間と規定されているが、DSデータセットによると、被験者01-704-1009はWEEK4で治験を中止している。一方、EXデータセットではEXENDTCが2013-09-25となっており、治験薬の投与期間が26週間に満たないことがわかる。

*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** DSDECOD, DSTERM
    *   **医療機関への問い合わせ文面:**
        *   被験者01-704-1009がWEEK4で治験を中止した理由について、詳細な医学的理由を教えてください。特に、DSTERMに記載された「TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS」という理由が、治験薬または疾患に起因するものかどうかを明確にしてください。
    *   **判断理由:** 治験薬との因果関係を評価する必要があるため。

クエリなし

# 01-701-1047
## Task1: Clinical Review Results
患者ID: 01-701-1047
*   2013年01月22日 (Day -21): スクリーニング検査で、年齢85歳、女性、白人と判明。既往歴としてアルツハイマー病、乾癬、手のしびれ、食道裂孔ヘルニア、浮腫性足、関節炎、甲状腺機能低下症、副鼻腔炎、痔核、子宮摘出、潰瘍、胆嚢摘出、白内障手術の病歴が報告された。併用薬として、ALEVE、CENTRUM、FELDENE、PAPAYA、PSORCON、SYNTHROIDを服用。
*   2013年02月12日 (Day 1): ベースライン測定。ADASSUBは10、DISABは複数項目で1点、NPI-Xのスコアは2。
*   2013年02月25日 (Day 14): Week2。PHOS (リン酸塩) が正常値範囲内だが減少。NPI-XのDISINHIBITIONスコアが1点。
*   2013年03月06日 (Day 23): 上気道感染症を発症。
*   2013年03月10日 (Day 27): HYPERTENSION (高血圧) の有害事象が発生。DISINHIBITION症状が悪化 (スコア6点)。
*   2013年03月29日 (Day 46): ADVERSE EVENT (有害事象) により試験中止。
*   2013年04月07日 (Day 55): 最終検査。PHOS (リン酸塩) が正常値範囲内だが減少。GLUC (グルコース) が正常値範囲内だが減少。
*   2013年07月28日 (Day 168): 転帰検査。NPI-Xスコアが悪化。

---

患者ID: 01-701-1047
*   **クエリNo.:** 1
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:**
        *   AE.AETERM = HYPERTENSION
        *   AE.AESTDTC = 2013-03-10
        *   VS.SYSBP (STANDING, AFTER STANDING FOR 1 MINUTE) = 185 mmHg (2013-03-10)
        *   VS.DIABP (STANDING, AFTER STANDING FOR 1 MINUTE) = 121 mmHg (2013-03-10)
    *   **医療機関への問い合わせ文面:**
        *   Day27(2013-03-10)に高血圧の有害事象が発現していますが、この時の血圧値(起立1分後)は185/121mmHgと非常に高い値を示しています。
        *   １）本有害事象発現以前に、高血圧に関連する既往歴や徴候はありましたでしょうか？
        *   ２）治験薬との因果関係について、治験担当医師はどのように判断されましたでしょうか？
        *   ３）高血圧発現時の状況について、詳細な情報をご教示いただけますでしょうか？（例：患者の自覚症状、血圧測定時の体位、使用した血圧計の種類、測定環境、再測定の有無、医療従事者の対応など）
        *   ４）高血圧発現後、血圧はどのように推移しましたでしょうか？また、高血圧に対する治療は行われましたでしょうか？
    *   **判断理由:**
        *   治験薬との因果関係、高血圧の重症度、及び、治験実施計画書からの逸脱の有無を評価する必要があるため。
        *   高血圧は、重篤な心血管イベントのリスクを高める可能性があり、患者の安全性に影響を与える可能性があるため。
        *   プロトコルの除外基準 [17] に、「A history within the last 5 years of a serious cardiovascular disorder, including f) Uncontrolled hypertension.」という項目があり、組み入れ基準を満たしているか確認する必要があるため。
        *   本件は緊急性の高い事象であるため、速やかに情報を収集し、適切な対応を検討する必要があるため。

---

疑義事項なし

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, AE.AEENDTC, VS.VSORRES, VS.VSSTRESN, DS.VISITNUM, LB.LBDTC

問題点:

*   問題No.: 1
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = null
    *   矛盾の内容: 複数のCMレコードにおいて、CMSTDTCに西暦のみが記録され、CMENDTCが欠損している。
    *   問題点の原因（推測）: CMENDTCが必須項目ではないため、CM開始時にCMENDTCが収集されなかったか、データ入力時にCMENDTCが脱落した可能性がある。
    *   対応策（提案）: CMENDTCが欠損している理由を確認し、可能であればCMENDTCを補完する。CMENDTCが補完できない場合は、CMTRTの中止日を他のドメイン（DS, AE等）から確認することを検討する。

*   問題No.: 2
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = ""
    *   矛盾の内容: 一部のCMレコードにおいて、CMSTDTCに西暦のみが記録され、CMENDTCが空文字となっている。
    *   問題点の原因（推測）: CMENDTCが必須項目ではないため、CM開始時にCMENDTCが収集されなかったか、データ入力時にCMENDTCが脱落した可能性がある。
    *   対応策（提案）: CMENDTCが空文字となっている理由を確認し、可能であればCMENDTCを補完する。CMENDTCが補完できない場合は、CMTRTの中止日を他のドメイン（DS, AE等）から確認することを検討する。

*   問題No.: 3
    *   変数名と値: CM.CMSTDTC = "2013-02-10", CM.CMENDTC = "2013-02-01"
    *   矛盾の内容: CMレコードにおいて、CMENDTCがCMSTDTCより前の日付になっている。
    *   問題点の原因（推測）: データ入力時の誤り
    *   対応策（提案）: CMENDTC, CMSTDTCの日付が正しいか確認する。

*   問題No.: 4
    *   変数名と値: AE.AEENDTC = ""
    *   矛盾の内容: AEレコードにおいて、AEENDTCが空文字になっている。
    *   問題点の原因（推測）: AEENDTCが必須項目ではないため、AE開始時にAEENDTCが収集されなかったか、データ入力時にAEENDTCが脱落した可能性がある。
    *   対応策（提案）: AEENDTCが空文字となっている理由を確認し、可能であればAEENDTCを補完する。

*   問題No.: 5
    *   変数名と値: AE.AESTDY = 23, AE.AEENDY = 22
    *   矛盾の内容: AEレコードにおいて、AEENDYがAESTDYより前の日付になっている。
    *   問題点の原因（推測）: データ入力時の誤り
    *   対応策（提案）: AEENDTC, AESTDTCの日付が正しいか確認する。

*   問題No.: 6
    *   変数名と値: DS.VISITNUM = 6.1
    *   矛盾の内容: DSレコードにおいて、VISITNUM=6.1となっているが、TVドメインにVISITNUM=6.1のレコードが存在するにもかかわらず、VISITが"UNSCHEDULED 6.1"となっている。本来であれば、DS.VISITはTV.VISITと一致すべきである。
    *   問題点の原因（推測）: データ入力時の誤り、もしくはデータ作成ロジックの不備。
    *   対応策（提案）: DS.VISITの値が正しいか確認する。

*   問題No.: 7
    *   変数名と値: LB.VISITNUM = 6.1, LB.LBDTCがNULL
    *   矛盾の内容: LBレコードにおいて、VISITNUM=6.1のレコードが存在するが、LBDTCがNULLとなっている。
    *   問題点の原因（推測）: データ入力時の誤り、もしくはデータ作成ロジックの不備。
    *   対応策（提案）: LBDTCの値がNULLとなっている理由を確認し、可能であればLBDTCを補完する。

*   問題No.: 8
    *   変数名と値: VS.VSORRES = "121", VS.VSSTRESN = 121, VSTESTCD = "DIABP", VISIT = "WEEK 4", VSPOS = "STANDING"
    *   矛盾の内容: VISIT="WEEK 4"の血圧測定において、VSORRES, VSSTRESNが121mmHgと異常値を示している。また、USUBJID="01-701-1047"において、他のVSレコードと比較してDIABPの値が極端に高い。
    *   問題点の原因（推測）: データ入力時の誤り、測定機器の不具合、または患者の生理的な状態の異常。
    *   対応策（提案）: VS.VSORRES, VS.VSSTRESNの値が正しいか確認する。可能であれば、測定時の状況（患者の状態、測定機器の状態など）を調査し、データの信憑性を評価する。

*   問題No.: 9
    *   変数名と値: VS.VSORRES = "185", VS.VSSTRESN = 185, VSTESTCD = "SYSBP", VISIT = "WEEK 4", VSPOS = "STANDING"
    *   矛盾の内容: VISIT="WEEK 4"の血圧測定において、VSORRES, VSSTRESNが185mmHgと異常値を示している。また、USUBJID="01-701-1047"において、他のVSレコードと比較してSYSBPの値が極端に高い。
    *   問題点の原因（推測）: データ入力時の誤り、測定機器の不具合、または患者の生理的な状態の異常。
    *   対応策（提案）: VS.VSORRES, VS.VSSTRESNの値が正しいか確認する。可能であれば、測定時の状況（患者の状態、測定機器の状態など）を調査し、データの信憑性を評価する。

クエリの作成:

患者ID: 01-701-1047

*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = null, CM.CMTRT = "ALEVE"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047について、ALEVE（CMTRT）の服用開始時期（CMSTDTC）は2009年と記録されていますが、正確な日付をご教示ください。また、服用終了時期（CMENDTC）が不明のため、服用終了時期、または現在も服用中であるかをご教示ください。
    *   判断理由: 
        CMTRT, CMSTDTC, CMENDTCは、併用薬の評価において重要な情報であり、データの正確性が求められるため。

*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = null, CM.CMTRT = "CENTRUM"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047について、CENTRUM（CMTRT）の服用開始時期（CMSTDTC）は2002年と記録されていますが、正確な日付をご教示ください。また、服用終了時期（CMENDTC）が不明のため、服用終了時期、または現在も服用中であるかをご教示ください。
    *   判断理由: 
        CMTRT, CMSTDTC, CMENDTCは、併用薬の評価において重要な情報であり、データの正確性が求められるため。

*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC = "2013-02-10", CM.CMENDTC = "2013-02-01", CM.CMTRT = "FELDENE"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047について、FELDENE（CMTRT）の服用期間について確認させてください。記録によると、服用開始日（CMSTDTC）が2013年2月10日、服用終了日（CMENDTC）が2013年2月1日となっており、矛盾しています。正しい服用期間をご教示ください。
    *   判断理由: 
        CMTRT, CMSTDTC, CMENDTCは、併用薬の評価において重要な情報であり、データの正確性が求められるため。

*   クエリNo.: 4
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = null, CM.CMTRT = "PSORCON"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047について、PSORCON（CMTRT）の服用開始時期（CMSTDTC）は2009年と記録されていますが、正確な日付をご教示ください。また、服用終了時期（CMENDTC）が不明のため、服用終了時期、または現在も服用中であるかをご教示ください。
    *   判断理由: 
        CMTRT, CMSTDTC, CMENDTCは、併用薬の評価において重要な情報であり、データの正確性が求められるため。

*   クエリNo.: 5
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMSTDTC = "2009", CM.CMENDTC = null, CM.CMTRT = "SYNTHROID"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047について、SYNTHROID（CMTRT）の服用開始時期（CMSTDTC）は2009年と記録されていますが、正確な日付をご教示ください。また、服用終了時期（CMENDTC）が不明のため、服用終了時期、または現在も服用中であるかをご教示ください。
    *   判断理由: 
        CMTRT, CMSTDTC, CMENDTCは、併用薬の評価において重要な情報であり、データの正確性が求められるため。

*   クエリNo.: 6
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: AE.AEENDTC = "", AE.AETERM = "HYPERTENSION"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047に発現したHYPERTENSION（AETERM）について、治験薬投与開始日、治験薬投与終了日、転帰、AEREL(治験薬との因果関係)について確認させてください。
    *   判断理由: 
        AEENDTCが空欄のため、正確な有害事象の評価ができない可能性があるため。

*   クエリNo.: 7
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: VS.VSORRES = "121", VS.VSSTRESN = 121, VSTESTCD = "DIABP", VISIT = "WEEK 4", VSPOS = "STANDING"
    *   医療機関への問い合わせ文面: 
       被験者01-701-1047の4週目の血圧測定で、起立時の拡張期血圧（DIABP）が121mmHgと異常に高い値を示しています。この値が正しいか、再測定または確認をお願いします。また、測定時の患者の状態や状況についても情報があればご提供ください。
    *   判断理由: 
        高血圧は有害事象や試験中止の判断に影響を与える可能性があるため、正確なデータが必要です。

*   クエリNo.: 8
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: VS.VSORRES = "185", VS.VSSTRESN = 185, VSTESTCD = "SYSBP", VISIT = "WEEK 4", VSPOS = "STANDING"
    *   医療機関への問い合わせ文面: 
        被験者01-701-1047の4週目の血圧測定で、起立時の収縮期血圧（SYSBP）が185mmHgと異常に高い値を示しています。この値が正しいか、再測定または確認をお願いします。また、測定時の患者の状態や状況についても情報があればご提供ください。
    *   判断理由: 
        高血圧は有害事象や試験中止の判断に影響を与える可能性があるため、正確なデータが必要です。

Define.xmlの修正候補:

*   特になし


## Task3: Protocol Deviation Review Results
患者ID: 01-701-1047

逸脱No.: 1
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMSTDTC = "2009"
逸脱内容: 併用薬ALEVE、CENTRUM、PSORCON、SYNTHROIDの開始日が、DM.RFSTDTC（2013-02-12）より前である。
プロトコル該当箇所: 3.8
判断理由:  プロトコル3.8には併用療法に関する記載があるが、併用薬の開始時期に関する規定はない。ただし、治験薬投与開始後に開始された併用薬であれば、有害事象との関連を評価する必要がある。DM.RFSTDTCは治験薬の投与開始日であるため、併用薬の開始日がDM.RFSTDTCより前である場合は、治験薬との関連はないと考えられる。

逸脱No.: 2
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMSTDTC = "2013-02-01"、CM.CMENDTC = "2013-02-01"、CM.VISIT = "SCREENING 2"
逸脱内容: 併用薬FELDENEの開始日（2013-02-01）が終了日（2013-02-01）と一致しており、SCREENING 2（2013-02-10）に投与されている。
プロトコル該当箇所: 3.8
判断理由: プロトコル3.8には併用療法に関する記載があるが、併用薬の使用期間に関する規定はない。FELDENEの投与期間は、プロトコルで指定された除外基準[31b]に抵触しないか確認が必要。

逸脱No.: 3
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMSTDTC = "2012-10"、CM.VISIT = "SCREENING 1"
逸脱内容: 併用薬PAPAYAの開始日が、DM.RFSTDTC（2013-02-12）より前である。
プロトコル該当箇所: 3.8
判断理由: プロトコル3.8には併用療法に関する記載があるが、併用薬の開始時期に関する規定はない。ただし、治験薬投与開始後に開始された併用薬であれば、有害事象との関連を評価する必要がある。DM.RFSTDTCは治験薬の投与開始日であるため、併用薬の開始日がDM.RFSTDTCより前である場合は、治験薬との関連はないと考えられる。

逸脱No.: 4
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMSTDTC = "2013-03-07"、CM.VISIT = "WEEK 4"
逸脱内容: 併用薬ROBITUSSIN-DM、SUDAFEDの開始日が、CM.CMDTC（2013-03-10）より前である。
プロトコル該当箇所: 3.8
判断理由: 併用薬の開始日CMSTDTCとデータ収集日CMDTCが矛盾している。データエントリー時のエラーの可能性がある。

患者ID: 01-701-1047
クエリNo.: 1
臨床試験結果への影響度合い: Minor
変数名と値: CM.CMSTDTC = "2013-02-01"、CM.CMENDTC = "2013-02-01"、CM.CMTRT = "FELDENE"
医療機関への問い合わせ文面:
併用薬FELDENEについて、CMSTDTCおよびCMENDTCが2013-02-01となっていますが、投与期間は1ヶ月未満で除外基準[31b]に抵触しないことを確認してください。
判断理由: 
プロトコル除外基準[31b]では、特定の薬剤について1ヶ月以内の投与を禁止しているため、FELDENEの使用がこれに該当しないか確認が必要です。

# 01-703-1076
## Task1: Clinical Review Results
1.  **症例サマリーの作成:**

*   **患者ID:** 01-703-1076
    *   2013年10月17日 (Day -8): Hypercholesterolemia, Glaucoma, Hypertension, Goutの既往歴あり。教育レベルは10年。
    *   2013年11月16日 (Day 23): Biopsy Prostate発生、軽度。
    *   2013年11月20日 (Day 27): Benign Prostatic Hyperplasiaが発生、軽度。
    *   2013年11月23日 (Day 30): Application Site PruritusとApplication Site Dermatitisが発生、軽度。
    *   2013年11月25日 (Day 32): Hyperhidrosisが発生、軽度。
    *   2013年12月24日 (Day 61): ADVERSE EVENTが発生。
    *   2013年12月24日 (Day 61): FINAL LAB VISITが発生。
    *   2013年10月16日 (Day -9): Albumin値が4.9 g/dLと基準値上限を超えている。Cholesterol値が307 mg/dLと基準値上限を超えている。Urate値が7.8 mg/dLと基準値上限を超えている。Protein値が8.1 g/dLと基準値上限を超えている。
    *   2013年11月20日 (Day 27): Calcium値が10.5 mg/dLと基準値上限を超えている。
    *   2013年12月04日 (Day 41): Urate値が8.4 mg/dLと基準値上限を超えている。
    *   2013年12月17日 (Day 54): Urate値が7.9 mg/dLと基準値上限を超えている。
    *   2013年12月24日 (Day 61): Urate値が7.8 mg/dLと基準値上限を超えている。

---

2.  **クエリの作成 (必要な場合のみ):**

*   **患者ID:** 01-703-1076
    *   **クエリNo.:** 1
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** AE.AETERM = APPLICATION SITE PRURITUS (AESEQ=4), AE.AETERM = APPLICATION SITE PRURITUS (AESEQ=7), RELREC.RELID = 01-703-1076-E08
        *   **医療機関への問い合わせ文面:**  RELRECドメインにおいて、AEドメインのApplication Site Pruritus (AESEQ=4, 7)と関連付けられている事象の具体的な内容を教えてください。また、DSドメインに記録されたADVERSE EVENT (DSSEQ=1) は、Application Site Pruritusと関連がありますか？
        *   **判断理由:** RELRECドメインで関連付けられているAEの内容と、DSドメインに記録されたADVERSE EVENTが同一の事象を指しているかを確認する必要があるため。関連性の詳細を把握することで、有害事象の評価に影響を与える可能性がある。
    *   **クエリNo.:** 2
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.URATE (各VISIT)
        *   **医療機関への問い合わせ文面:**  LBドメインにおいて、Urate値がSCREENING 1からWEEK 12まで一貫して基準値上限を超えています。これは高尿酸血症の状態ですが、Medical Historyに「GOUT」の記載があります。現在、高尿酸血症に対する治療は行われていますか？また、プロトコルで規定された除外基準に抵触しないか確認してください。
        *   **判断理由:**  プロトコルに抵触する可能性を確認する必要があるため。
    *   **クエリNo.:** 3
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** CM.CMDECOD = UNCODED (各薬剤)
        *   **医療機関への問い合わせ文面:** CMドメインに記録されたCORTISONE, LIPITOR, LAC-HYDRIN, MEVACORについて、UNCODEDとなっています。これら併用薬について、可能な限りCMDECODに適切な値を設定してください。
        *   **判断理由:**  データ品質向上のため。

## Task2: DM Review Results
全体的なデータ品質の評価:

*   総合評価: 一部問題あり
*   データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, AE.AESTDTC, AE.AEENDTC

問題点:

*   問題No.1: CMドメインにおける日付の不整合
    *   変数名と値: CM.CMSTDTC = "2010"
    *   矛盾の内容: 複数のCMレコードにおいて、CMSTDTCが2010年と記録されています。しかし、他の日付（CMDTC）は2013年または2014年であり、矛盾しています。また、試験期間はDM.RFSTDTC（2013-10-25）からDM.RFENDTC（2013-12-24）であるため、2010年の日付は試験期間外です。
    *   問題点の原因（推測）: データ入力エラー、日付の解釈違い
    *   対応策（提案）:
        1.  CM.CMSTDTCの2010という値が正しいかどうか確認し、必要に応じて修正してください。
        2.  CMENDTCについても同様に確認し、必要に応じて修正してください。

*   問題No.2: AEドメインにおける日付の欠損
    *   変数名と値: AE.AEENDTC = ""(NULL)
    *   矛盾の内容: 複数のAEレコードにおいて、AEENDTCが欠損しています。有害事象がいつ終了したのか不明確です。
    *   問題点の原因（推測）: データ入力時の未記入、有害事象が継続中
    *   対応策（提案）:
        1.  AEENDTCが欠損している理由を確認してください。
        2.  有害事象が継続中の場合、その旨を記録するか、または適切な終了日を設定してください。

*   問題No.3: MHドメインにおけるMHTERMの欠損
    *   変数名と値: MH.MHTERM = "ALZHEIMER'S DISEASE"
    *   矛盾の内容: MHレコードにおいて、MHTERMが"ALZHEIMER'S DISEASE"とVerbatimで記録されていますがMHLLT,MHDECOD,MHHLT,MHHLGTの値が欠損しています。
    *   問題点の原因（推測）: データ入力時のコーディングエラー。
    *   対応策（提案）:
        1.　MHLLT,MHDECOD,MHHLT,MHHLGTに適切な値を設定してください。
        2.Define.xmlにMHTERMがNULLを許可していない定義になっている場合、修正を検討してください。

クエリの作成:

*   患者ID: 01-703-1076
    *   クエリNo.1:
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: CM.CMSTDTC = "2010"
        *   医療機関への問い合わせ文面:
            *   CMドメインにおいて、CMSTDTCが2010年となっているデータがありますが、これは誤りではないでしょうか？正しい開始年月日をご教示ください。
            *   CMENDTCがNULLとなっているデータがありますが、有害事象はいつ終了しましたでしょうか？
        *   判断理由:
            *   CMSTDTCは、薬剤の有効性や安全性を評価する上で重要な情報であるため。
            *   AEENDTCは、有害事象の期間を把握し、適切な対応を判断するために必要であるため。

## Task3: Protocol Deviation Review Results
患者ID: 01-703-1076
    *   逸脱No.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, MH.MHSTDTC=2012-08-27
        *   逸脱内容: 被験者01-703-1076は、既往歴としてアルツハイマー病を有している。
        *   プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [12] Diagnosis of serious neurological conditions
        *   判断理由: 除外基準12に、重篤な神経疾患の診断が含まれており、アルツハイマー病も該当する可能性があるため、プロトコルからの逸脱と判断しました。

患者ID: 01-703-1076
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, MH.MHSTDTC=2012-08-27
        *   医療機関への問い合わせ文面: 被験者01-703-1076のアルツハイマー病の診断時期、重症度、および現在の状態について詳細な情報をご提供ください。特に、この疾患が除外基準の「重篤な神経疾患」に該当するかどうかについてご意見をお聞かせください。
        *   判断理由: 被験者のアルツハイマー病が除外基準に合致するかを確認し、プロトコル逸脱の有無を確定するために、医療機関への問い合わせが必要と判断しました。

