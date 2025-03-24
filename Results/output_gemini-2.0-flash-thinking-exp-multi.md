# 01-704-1008
## Task1: Clinical Review Results
患者ID: 01-704-1008
* 2012年06月01日 (Day -225): 手足の振戦 (軽度)、筋 stiffness (中等度)、動作緩慢 (重度) の有害事象発現
* 2012年11月25日 (Day -49): 総ビリルビン値が基準値上限超え (1.3 mg/dL, 基準範囲: 0.2-1.2 mg/dL)、甲状腺刺激ホルモン (TSH) 値が基準値下限を下回る (0.24 uIU/mL, 基準範囲: 0.32-5 uIU/mL)
* 2013年02月09日 (Day 28): 血清蛋白値が基準値下限を下回る (5.8 g/dL、基準範囲: 6-8 g/dL)、尿酸値が基準値下限を下回る (2.4 mg/dL、基準範囲: 2.5-7.5 mg/dL)
* 2013年02月21日 (Day 40): 動作緩慢 (重度) の有害事象が回復
* 2013年02月25日 (Day 44): クレアチンキナーゼ (CK) 値が基準値上限超え (189 U/L, 基準範囲: 21-169 U/L)、筋 stiffness (中等度)、洞性徐脈 (中等度) の有害事象継続中、最終診察、試験中止

---
患者ID: 01-704-1008
* クエリNo.1:
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AETERM = TRANSIENT ISCHEMIC ATTACKS, AE.AESEV = SEVERE
    * 医療機関への問い合わせ文面: 重度の一過性脳虚血発作 (TRANSIENT ISCHEMIC ATTACKS) は医学的に妥当な有害事象か、治験薬との因果関係、発現日、持続期間、症状、転帰、処置について医学的見解をご教示ください。
    * 判断理由: 重大な有害事象であり、患者の安全性に影響を与える可能性があり、臨床試験の評価に重要な影響を与えるため、医学的妥当性を確認する必要があります。

* クエリNo.2:
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD=BILI, LB.LBNRIND=HIGH (2012-11-25)
    * 医療機関への問い合わせ文面: スクリーニング時のビリルビン高値 (LB.LBTESTCD=BILI, LB.LBNRIND=HIGH) の原因、臨床的な解釈と医学的妥当性についてご説明ください。
    * 判断理由: 肝機能障害を示唆する可能性があり、患者の安全性に影響を与える可能性があるため、医学的妥当性を確認する必要があります。

* クエリNo.3:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: MH.MHTERM=HYPOTHYROIDISM, LB.LBTESTCD=TSH, LB.LBNRIND=LOW (2012-11-25)
    * 医療機関への問い合わせ文面: 既往歴の甲状腺機能低下症 (MH.MHTERM=HYPOTHYROIDISM) とスクリーニング時の甲状腺刺激ホルモン (TSH) 低値 (LB.LBTESTCD=TSH, LB.LBNRIND=LOW) の関連性について、SYNTHROIDの投与状況と合わせて
## Task2: DM Review Results
全体的なデータ品質の評価:
総合評価: 一部問題あり
データクリーニング/再調査が必要な項目: AE.AESTDTC, EX.EXSTDTC, CM.CMENDTC, LB.LBTESTCD=BILI, LB.LBORRES=1.3, RELREC.RELTYPE, 日付データ形式, Study Day関連変数, DMドメインとSUPPDMドメインのレコード数, LBドメインのデータ型 (LBORRES, LBORNRLO, LBORNRHI)

問題点:
問題No.: 1
変数名と値: AE.AESTDTC=2012-06-01, EX.EXSTDTC=2013-01-13
矛盾の内容: 有害事象「TREMOR IN HANDS, LEGS」の開始日が2012-06-01と記録されており、治験薬投与開始日 (2013-01-13) より200日以上前です。治験薬投与前に有害事象が発現している可能性があり、データの矛盾が疑われます。
問題点の原因（推測）: データ入力時の誤り、またはAE開始日の誤りの可能性があります。
対応策（提案）: AEドメインとEXドメインの原資料を照合し、AE開始日と治験薬投与開始日の整合性を検証してください。必要に応じてデータ修正を依頼してください。

問題No.: 2
変数名と値: LB.LBTESTCD=BILI, LB.LBORRES=1.3, LBNRIND=HIGH, LB.LBORNRLO=0.2, LB.LBORNRHI=1.2
矛盾の内容:  総ビリルビン値が1.3 mg/dLと基準範囲上限 (1.2 mg/dL) を超えています。LBNRIND="HIGH" フラグが立っており、臨床的に注意が必要な可能性があります。
問題点の原因（推測）:  患者の肝機能異常、一過性の生理的変動、または検査エラーなどが考えられます。
対応策（提案）:  LBドメインのBILI値について、医学的妥当性を評価してください。必要に応じて、再検査、追加検査、または医療専門家による医学的評価を検討してください。また、AEドメインに肝機能異常に関連する有害事象が報告されていないか確認してください。

問題No.: 3
変数名と値: CM.CMENDTC = null (MULTIVITAMIN, 複数レコード)
矛盾の内容: 併用薬 MULTIVITAMIN の投与終了日が欠損しています。併用薬の曝露期間を正確に把握するため、終了日の記録が望ましいです。
問題点の原因（推測）: データ入力の抜け、または長期継続投与のため終了日を記録しない運用ルールである可能性があります。
対応策（提案）: 医療機関にMULTIVITAMINの投与終了日を確認し、可能であればデータを更新してください。終了日が不明な場合は、その理由をデータ備考欄に記録することを推奨します。Define.xmlに備考欄を追加することも検討ください。

問題No.: 4
変数名と値: RELREC.RDOMAIN = AE, RELREC.IDVARVAL = "   3", RELREC.RELTYPE = ""
矛盾の内容: RELRECドメインにおいて、AEドメイン (AESEQ=3) とDSドメイン (DSSEQ=1) のレコードが関連付けられていますが、RELTYPE が空欄で関連の種類が不明です。
問題点の原因（推測）: RELRECデータ作成時の不備、またはDefine.xmlのRELTYPE定義漏れの可能性があります。
対応策（提案）: RELRECドメインの原資料またはデータ作成手順を確認し、AEとDSの関連の種類を特定し、RELTYPE に適切な値を入力してください。Define.xml の修正も検討してください。

問題No.: 5
変数名と値: 日付データ形式 (CMDTC, CMSTDTC, CMENDTC, AEDTC, AESTDTC, AEENDTC, LBDTC, SCDTC, MHDTC, MHSTDTC, DSDTC, DSSTDTC, EXSTDTC, EXENDTC, SEDTC, SEENDTC, SVDTC, SVENDTC, QSDTC, DMDTC, RFSTDTC, RFENDTC, RFXSTDTC, RFXENDTC, RFICDTC, RFPENDTC, DTHDTC, VSDTC, SVSTDTC, SVENDTC, CMSTDTC, CMENDTC, AESTDTC, AEENDTC, DSSTDTC, DSDTC, MHSTDTC, MHDTC, SCDTC)
矛盾の内容:  日付データの形式が "YYYY-MM-DD" 形式と "YYYY" 形式、"" (空文字) が混在しており、データ形式が統一されていません。
問題点の原因（推測）: データ入力時の形式不統一、またはシステム間のデータ変換エラー
対応策（提案）:  日付データ形式を "YYYY-MM-DD" 形式に統一することを推奨します。欠損値は NULL 値などで明示的に表現してください。Define.xml とデータ形式の整合性を確保してください。

問題No.: 6
変数名と値: Study Day 変数 (LBDY, CMSTDY, CMENDY, AESTDY, AEENDY, DSSTDY, MH.MHDY, SCDY, DMDY, VSDY, VISITDY) と対応する Date/Time 変数 (LBDTC, CMSTDTC, CMENDTC, AESTDTC, AEENDTC, DSSTDTC, MHDTC, SCDTC, DMDTC, VSDTC, SVSTDTC, SVENDTC)
矛盾の内容: Study Day 変数と Date/Time 変数で日付のずれや矛盾が見られます。
問題点の原因（推測）: Study Day の計算ロジックの誤り、または参照日 (DM.RFSTDTC) の誤り、データ入力時の人為的なミス
対応策（提案）: Study Day の計算ロジック (Define.xml 参照) を再確認し、データ全体の整合性を検証してください。DM.RFSTDTC の正確性も確認してください。

問題No.: 7
変数名と値: DM.AGE = 76, SUPPDM レコード数 > DM レコード数
矛盾の内容: DMドメインのレコード数 (1件) より SUPPDMドメインのレコード数 (3件) が多く、データの重複または不整合が疑われます。
問題点の原因（推測）: SUPPDMドメインのデータ作成ロジックのエラー、またはデータの重複登録
対応策（提案）: SUPPDMドメインのデータ作成ロジックを見直し、DMドメインとのレコード数の整合性を確認してください。データ重複登録の可能性も調査してください。

問題No.: 8
変数名と値: LB.LBORRES, LB.LBORNRLO, LB.LBORNRHI (DataType="string"), LBSTRESN (DataType="float")
矛盾の内容:  LBORRES, LBORNRLO, LBORNRHI のデータ型が "string" 型である一方、LBSTRESN は "float" 型であり、データ型に一貫性がありません。数値データとして扱う変数のデータ型は統一することを推奨します。
問題点の原因（推測）: データ型定義の不統一、またはデータ変換時のエラー
対応策（提案）: LBORRES, LBORNRLO, LBORNRHI のデータ型を数値型 (float または decimal) に修正し、Define.xml の定義と整合性を持たせてください。

クエリ:
患者ID: 01-704-1008
クエリNo.: 1
臨床試験結果への影響度合い: Critical
変数名と値: AE.AETERM=TREMOR IN HANDS, LEGS, AE.AESTDTC=2012-06-01, EX.EXTRT=XANOMELINE, EX.EXSTDTC=2013-01-13
医療機関への問い合わせ文面: 患者ID 01-704-1008 の有害事象「TREMOR IN HANDS, LEGS (AESEQ=1)」の発現日が治験薬投与開始日より前 (2012-06-01 vs 2013-01-13) となっています。AE開始日の記録に誤りがないか、原資料をご確認いただけますでしょうか。

患者ID: 01-704-1008
クエリNo.: 2
臨床試験結果への影響度合い: Major
変数名と値: LB.LBTESTCD=BILI, LB.LBORRES=1.3
医療機関への問い合わせ文面: 患者ID 01-704-1008 のWeek 1 (SCREENING 1) の検査値において、総ビリルビン値が基準範囲上限を超えています (1.3 mg/dL vs 基準範囲上限 1.2 mg/dL)。データ入力ミスかどうか、あるいは医学的に評価された再検査データがございましたらご提供いただけますでしょうか。また、関連する有害事象の報告の有無についても併せてご教示ください。

患者ID: 01-704-1008
クエリNo.: 3
臨床試験結果への影響度合い: Major
変数名と値: CM.CMENDTC (MULTIVITAMIN)
医療機関への問い合わせ文面: 患者ID 01-704-1008 の併用薬 MULTIVITAMIN (CMSEQ=2, 5, 8, 11, 14, 17, 19) の投与終了日が未記録です。MULTIVITAMIN の投与は Week 6 (VISITNUM=7) 以降も継続していますでしょうか？もし終了している場合は、投与終了日をご教示ください。

患者ID: 01-704-1008
クエリNo.: 4
臨床試験結果への影響度合い: Minor
変数名と値: RELREC.RDOMAIN = AE, RELREC.IDVARVAL = "   3", RELREC.RELTYPE = ""
医療機関への問い合わせ文面: 患者ID 01-704-1008 のRELRECドメインにおいて、AEドメインとDSドメインの関連レコード (RELID=01-704-1008-E05) が存在しますが、RELTYPEが空欄です。AEとDSの関連の種類をご教示いただけますでしょうか。
## Task3: Protocol Deviation Review Results
患者ID: 01-704-1008
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=BILI, LBORRES=1.3, LBNRIND=HIGH (SCREENING 1)
        逸脱内容:  被験者01-704-1008のスクリーニング1 (SCREENING 1) における総ビリルビン値が1.3 mg/dLと基準範囲上限を超過しており、Reference Range Indicator (LBNRIND) でもHIGHフラグが立っています。プロトコル除外基準[27b]に抵触する可能性があります。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
        判断理由:  JSONデータ (LBドメイン) において、LBTESTCD=BILI (総ビリルビン) の検査値が基準範囲上限を超過していることが示唆されています。Define.xmlには具体的な基準範囲の記述がないものの、プロトコル除外基準 [27b] に抵触する可能性があるため、臨床的な意義とプロトコル逸脱の有無について確認が必要です。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=TSH, LBORRES=0.24, LBNRIND=LOW (SCREENING 1)
        逸脱内容: 被験者01-704-1008のスクリーニング1 (SCREENING 1) における甲状腺刺激ホルモン (TSH) 値が0.24 uIU/mLと基準範囲下限を下回っており、Reference Range Indicator (LBNRIND) でもLOWフラグが立っています。プロトコル除外基準[28b]に抵触する可能性があります。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [28b]
        判断理由: JSONデータ (LBドメイン) において、LBTESTCD=TSH (甲状腺刺激ホルモン) の検査値が基準範囲下限を下回っていることが示唆されています。Define.xmlには具体的な基準範囲の記述がないものの、プロトコル除外基準 [28b] に抵触する可能性があるため、臨床的な意義とプロトコル逸脱の有無について確認が必要です。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=PROT, LBORRES=5.8, LBNRIND=LOW (WEEK 4)
        逸脱内容: 被験者01-704-1008のWEEK 4 (4週) における総蛋白値が5.8 g/dLと基準範囲下限を下回っており、Reference Range Indicator (LBNRIND) でもLOWフラグが立っています。
        プロトコル該当箇所: 3.9.3.3. Clinical Laboratory Tests
        判断理由: JSONデータ (LBドメイン) において、LBTESTCD=PROT (総蛋白) の検査値が基準範囲下限を下回っていますが、プロトコルに具体的な基準逸脱時の対応に関する記述はありません。ただし、臨床検査値異常として、臨床的な意義と対応について確認することが望ましいと考えられます。

    逸脱No.: 4
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHDECOD = HYPOTHYROIDISM, CM.CMTRT = SYNTHROID
        逸脱内容:  被験者01-704-1008のMedical History (MH) ドメインにHYPOTHYROIDISM (甲状腺機能低下症) の既往歴が記録されています。プロトコル除外基準[19]では、内分泌系疾患の既往歴（未治療の甲状腺機能低下症を含む）が除外基準として規定されています。一方、Concomitant Medications (CM) ドメインにはSYNTHROID (甲状腺機能低下症治療薬) の併用が記録されており、甲状腺機能低下症の治療状況について確認が必要です。
        プロトコル該当箇所: 3.4.2.2 Exclusion Criteria [19]
        判断理由: MHドメインとCMドメインのデータから、甲状腺機能低下症の治療状況が不明であり、プロトコル除外基準 [19] に抵触する可能性があるため、確認が必要です。

    逸脱No.: 5
        臨床試験結果への影響度合い: Major
        変数名と値: DS.DSTERM=ADVERSE EVENT, DSDECOD=ADVERSE EVENT (WEEK 6)
        逸脱内容:  被験者01-704-1008はWEEK 6 (6週) に有害事象 (ADVERSE EVENT) により治験を中止しています。Adverse Events (AE) ドメインには複数の有害事象 (TREMOR IN HANDS, LEGS, MUSCLE STIFFNESS, SLOWNESS of MOVEMENT) が記録されており、これらの有害事象が治験中止の理由となった可能性があります。
        プロトコル該当箇所: 3.10.1. Discontinuations, 3.9.3.2.1. Adverse Event Reporting Requirements
        判断理由: DSドメインに治験中止理由がADVERSE EVENTと記録されており、AEドメインに複数の有害事象が記録されていることから、有害事象と治験中止の関連性を確認する必要があります。有害事象の内容、重症度、治験薬との因果関係について、詳細な情報収集と医学的評価が必要です。

クエリ:
患者ID: 01-704-1008
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=BILI, LBORRES=1.3, LBNRIND=HIGH (SCREENING 1)
        医療機関への問い合わせ文面:
            治験参加者ID: 01-704-1008 のスクリーニング検査（SCREENING 1）における総ビリルビン値について確認させてください。LBドメインのBILI（総ビリルビン）検査において、LBORRESの値が1.3 mg/dLと基準値上限を超過しており、LBNRINDもHIGHフラグが立っています。プロトコル3.4.2.2の除外基準[27b]に抵触する可能性があります。

            1.  治験実施医療機関における総ビリルビン検査の基準値範囲と、基準値上限をご教示ください。
            2.  被験者01-704-1008のスクリーニング検査時の総ビリルビン値1.3 mg/dLは、基準値上限を超過していますでしょうか？
            3.  基準値上限を超過している場合、治験責任医師は、当該基準値超過について臨床的にSignificant（重要）と判断されましたでしょうか？
            4.  Significantと判断された場合、プロトコル除外基準[27b]に基づき、本症例は治験対象から除外されるべき症例に該当すると判断されましたでしょうか？
            5.  除外基準に抵触すると判断されたにも関わらず、本症例が治験に登録された理由をご教示ください。
            6.  再検査を実施された場合、検査結果をご教示ください。
            7.  本症例が除外基準[27b]に抵触すると判断された場合、治験参加者の組み入れ状況について、治験審査委員会（IRB）に報告された内容と、IRBの承認状況をご教示ください。

            本件は、治験参加者の選択基準に関わる重要な疑義事項と考えられます。お忙しいところ恐縮ですが、速やかにご回答いただけますようお願いいたします。
        判断理由: プロトコル逸脱の可能性 (選択基準/除外基準違反) が高く、治験の根幹に関わる重要な疑義であるため、詳細な情報を早急に収集し、医学的妥当性を評価する必要がある。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=TSH, LBORRES=0.24, LBNRIND=LOW (SCREENING 1)
        医療機関への問い合わせ文面:
            治験参加者ID: 01-704-1008 のスクリーニング検査（SCREENING 1）における甲状腺刺激ホルモン（TSH）値について確認させてください。LBドメインのTSH検査において、LBORRESの値が0.24 uIU/mLと基準値下限を下回っており、LBNRINDもLOWフラグが立っています。プロトコル3.4.2.2の除外基準[28b]に抵触する可能性があります。

            1.  治験実施医療機関における甲状腺刺激ホルモン（TSH）検査の基準値範囲と、基準値下限をご教示ください。
            2.  被験者01-704-1008のスクリーニング検査時の甲状腺刺激ホルモン（TSH）値0.24 uIU/mLは、基準値下限を下回っていますでしょうか？
            3.  基準値下限を下回っている場合、治験責任医師は、当該基準値超過について臨床的にSignificant（重要）と判断されましたでしょうか？
            4.  Significantと判断された場合、プロトコル除外基準[28b]に基づき、本症例は治験対象から除外されるべき症例に該当すると判断されましたでしょうか？
            5.  除外基準に抵触すると判断されたにも関わらず、本症例が治験に登録された理由をご教示ください。
            6.  再検査を実施された場合、検査結果をご教示ください。
            7.  プロトコル除外基準[28b]には、「甲状腺機能検査値が基準範囲外」の場合、除外とありますが、具体的にどの検査項目が基準範囲外であった場合に除外となるか、プロトコルの規定をご教示ください。

            本件は、治験参加者の選択基準に関わる重要な疑義事項と考えられます。お忙しいところ恐縮ですが、速やかにご回答いただけますようお願いいたします。
        判断理由: プロトコル逸脱の可能性 (選択基準/除外基準違反) が高く、治験の根幹に関わる重要な疑義であるため、詳細な情報を早急に収集し、医学的妥当性を評価する必要がある。

    クエリNo.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHDECOD = HYPOTHYROIDISM, CM.CMTRT = SYNTHROID
        医療機関への問い合わせ文面:
            被験者01-704-1008のMedical History (MH) ドメインに甲状腺機能低下症（HYPOTHYROIDISM）の既往歴が記録されています。一方、Concomitant Medications (CM) ドメインにはSYNTHROID（甲状腺ホルモン製剤、一般名：レボチロキシンナトリウム）の併用が記録されており、甲状腺機能低下症の治療状況について確認させてください。

            1.  被験者01-704-1008の甲状腺機能低下症は、治験登録前に診断・治療開始されていますでしょうか？診断・治療開始時期をご教示ください。
            2.  併用薬SYNTHROIDは、甲状腺機能低下症に対して、治験登録前から投与されていますでしょうか？投与開始時期と投与量をご教示ください。
            3.  併用薬SYNTHROIDは、治験期間中も継続して投与される予定でしょうか？投与量変更の予定の有無についてもご教示ください。
            4.  プロトコル3.4.2.2の除外基準[19]では、「内分泌系疾患の既往歴（未治療の甲状腺機能低下症を含む）」が規定されています。本症例は、甲状腺機能低下症が治療されていると判断して治験に登録されたという理解でよろしいでしょうか？

            本件は、治験参加者の選択基準に関わる重要な疑義事項と考えられます。お忙しいところ恐縮ですが、速やかにご回答いただけますようお願いいたします。
        判断理由: プロトコル逸脱の可能性 (選択基準/除外基準違反) が高く、治験の根幹に関わる重要な疑義であるため、詳細な情報を早急に収集し、医学的妥当性を評価する必要がある。

    クエリNo.: 4
        臨床試験結果への影響度合い: Major
        変数名と値: DS.DSTERM=ADVERSE EVENT, DSDECOD=ADVERSE EVENT (WEEK 6), AEドメインの有害事象 (TREMOR IN HANDS, LEGS, MUSCLE STIFFNESS, SLOWNESS of MOVEMENT)
        医療機関への問い合わせ文面:
            被験者01-704-1008はWEEK 6 (6週) に有害事象 (ADVERSE EVENT) により治験中止となっております。DSドメインには治験中止理由がADVERSE EVENTと記録されており、AEドメインには複数の有害事象 (TREMOR IN HANDS, LEGS, MUSCLE STIFFNESS, SLOWNESS of MOVEMENT) が記録されています。

            1.  治験中止の理由となった有害事象のMedDRA Preferred Term (PT) と、重症度、治験薬との因果関係について、治験責任医師の見解をご教示ください。
            2.  治験中止に至った有害事象について、治験実施計画書 (プロトコル) およびICFに記載されている有害事象と種類や重症度に差異はありますでしょうか？差異がある場合、詳細をご教示ください。
            3.  治験中止に至った有害事象について、発現日、消失日、処置、転帰をご教示ください。
            4.  治験中止時までの治験薬投与状況（投与量、投与期間、投与日数など）と、治験中止後の有害事象の経過についてご教示ください。
            5.  治験中止の判断は、治験責任医師による医学的判断でしょうか、治験依頼者との協議によるものでしょうか、ご教示ください。

            本件は、治験参加者の安全性に関わる重要な疑義事項と考えられます。お忙しいところ恐縮ですが、速やかにご回答いただけますようお願いいたします。
        判断理由: 重大なプロトコル逸脱 (試験中止) に関連する疑義であり、治験参加者の安全性を評価するために、詳細な情報を早急に収集し、医学的妥当性を評価する必要がある。

# 01-703-1076
## Task1: Clinical Review Results
患者ID: 01-703-1076
* 2013年10月16日 (Day -9): 
    * 検査値異常: Albumin 高値 (4.9 g/dL, 基準上限値 4.6 g/dL), Cholesterol 高値 (307 mg/dL, 基準上限値 286 mg/dL), Protein 高値 (8.1 g/dL, 基準上限値 8.0 g/dL), Urate 高値 (7.8 mg/dL, 基準上限値 7.5 mg/dL)
* 2013年11月20日 (Day 27): 
    * 検査値異常: Calcium 高値 (10.5 mg/dL, 基準上限値 10.3 mg/dL), Cholesterol 高値 (319 mg/dL, 基準上限値 286 mg/dL), Protein 高値 (8.4 g/dL, 基準上限値 8.0 g/dL)
    * 有害事象: BENIGN PROSTATIC HYPERPLASIA (中等度), BIOPSY PROSTATE (中等度)
* 2013年11月23日 (Day 30): 
    * 有害事象: APPLICATION SITE DERMATITIS (軽度), APPLICATION SITE PRURITUS (軽度)
* 2013年11月25日 (Day 32): 
    * 有害事象: HYPERHIDROSIS (軽度)
* 2013年12月04日 (Day 41): 
    * 検査値異常: Urate 高値 (8.4 mg/dL, 基準上限値 7.5 mg/dL)
    * 有害事象: APPLICATION SITE DERMATITIS (軽度), APPLICATION SITE PRURITUS (軽度), HYPERCHOLESTEROLAEMIA (中等度), HYPERHIDROSIS (軽度)
* 2013年12月17日 (Day 54): 
    * 検査値異常: Urate 高値 (7.9 mg/dL, 基準上限値 7.5 mg/dL)
    * 有害事象: APPLICATION SITE PRURITUS (中等度)
* 2013年12月24日 (Day 61): 
    * 検査値異常: Urate 高値 (7.8 mg/dL, 基準上限値 7.5 mg/dL)
* 2014年01月21日 (Day 89): 
    * 検査値異常: Urate 高値 (値不明, 基準上限値 7.5 mg/dL)

---
患者ID: 01-703-1076
クエリなし
## Task2: DM Review Results
全体的なデータ品質の評価:
総合評価: 要修正
データクリーニング/再調査が必要な項目: CM.CMENDTC, CM.CMSTDTC, LB.LBORRES, LB.LBORRESU, LB.LBSTRESC, LB.LBSTRESN, LB.LBSTRESU, LB.URATE, QS.QSORRES, QS.QSORRESU, QS.QSSTRESC, QS.QSSTRESN, QS.QSSTRESU, VS.VSORRES, VS.VSORRESU, VS.VSSTRESC, VS.VSSTRESN, VS.VSSTRESU

問題点:
問題No.: 1
* 変数名と値: CM.CMENDTC (null), CM.CMENDY (null)
* 矛盾の内容: 併用薬 (CM) ドメインにおいて、アスピリンなど複数visitにわたる併用薬でCMENDTCおよびCMENDYが欠損しているレコードと、CORTISONE, LAC-HYDRIN, LIPITOR, MEVACORのようにCMENDTC, CMENDYがnullではないレコードが混在しており、データの一貫性、網羅性に欠ける。併用薬の投与期間は、有害事象評価や有効性評価において重要な情報となるため、終了日が不明なデータの取扱いに注意が必要である。
* 問題点の原因（推測）: データ入力時のエラー、併用薬が継続中のため終了日が未入力、またはデータ収集手順におけるCMENDTC/CMENDYの必須性の認識不足などが考えられる。特に、複数visitにデータが存在するアスピリンでCMENDTCが欠損しているケースは、データの不整合が疑われる。
* 対応策（提案）:
    1. CMENDTC, CMENDYがnullとなっているレコード（特にアスピリンなど複数visitにわたる併用薬）について、原資料（CRFなど）を確認し、併用薬の投与状況（継続中/終了）と終了日を特定する。
    2. 併用薬が終了している場合は、CMENDTC, CMENDYを更新する。
    3. 併用薬が継続中の場合は、CMENDTCをnullのままにする理由を記録する（SDTMのREASND変数など）。
    4. Define-XMLを確認し、CMENDTC, CMENDYの必須性に関する定義を確認する。必須項目として定義されている場合は、データ入力者に再教育を実施し、データ収集手順を徹底する。

問題No.: 2
* 変数名と値: CM.CMSTDTC = 2010
* 矛盾の内容: CM.CMSTDTC（併用薬開始日）がCMDTC（データ収集日）よりも過去の日付（2010年）となっているレコードが複数存在する。データ収集日（CMDTC）は2013年以降であり、CMSTDTCとして2010年は過去すぎる可能性が考えられる。
* 問題点の原因（推測）: データ入力時の誤り（年部分の桁間違い、誤った日付の選択など）、またはCMドメインのデータ定義の誤り（過去の併用薬も収集対象としているなど）の可能性が考えられる。
* 対応策（提案）:
    1. CM.CMSTDTCが2010年となっているレコードについて、原資料（CRFなど）を確認し、CMSTDTCの日付が正しいか検証する。
    2. CM.CMSTDTCが誤っている場合は、正しい日付に修正する。
    3. Define.xmlのCM.CMSTDTCの定義（データ型、フォーマット、必須性など）を確認し、データ定義に誤りがないか確認する。必要に応じてDefine-XMLを修正する。

問題No.: 3
* 変数名と値: LB.LBORRESU, LB.LBSTRESU (単位不一致), LB.LBTESTCD=URATE, LBORRES=7.8 ~ 8.4 mg/dL, LBSTRESN=463.944 ~ 499.632 umol/L, LBSTNRHI=446 umol/L, QSドメイン、VSドメインの単位
* 矛盾の内容:
    * LBドメイン: LBORRES (Original Units) と LBSTRESC (Standard Units) で単位が異なる場合がある。例：アルブミンのLBORRESUは "g/dL"、LBSTRESUは "g/L"。単位換算自体は意図的と思われるが、全てのLBTESTCDで単位変換が適切か要確認。また、Urate (尿酸) 検査値が基準範囲上限超過 (LBSTRESN: 463.944 ~ 499.632 umol/L, LBSTNRHI: 446 umol/L)。LBNRIND=HIGHだが臨床的意義不明。
    * QSドメイン、VSドメイン: LBドメインと同様に、QSORRESU, QSSTRESU, VSORRESU, VSSTRESU で単位情報が欠損、または標準値への変換が不適切なレコードが散見される。特にURINALYSISドメイン、評点項目で顕著。Define.xmlでLBUNIT, QSUNIT, VSUNITのCodeListが定義されているにも関わらず、データに反映されていない。
    * Define.xmlに単位変換に関するcomputation methodの定義がない。
* 問題点の原因（推測）: 単位変換ロジックの不備、データ入力時の単位の誤り、またはデータ変換処理における単位情報の欠落が考えられる。LB.URATE高値はデータ入力または検査値評価時の判断に疑義が残る。
* 対応策（提案）:
    1. LBドメイン全体のLBORRESとLBSTRESC、QSドメイン、VSドメインの単位換算が正しく行われているか検証する。特にURINALYSISドメイン、評点項目を重点的に確認する。
    2. LB.URATE高値について、医療機関に医学的妥当性を確認するクエリを発行する。
    3. Define-XMLにcomputation methodの定義を追加し、単位換算のルールを明記することを検討する。
    4. Define.xmlのLBSTRESU, QSSTRESU, VSSTRESUのCodeList制約とデータ内容の乖離を解消するため、Define-XMLの修正、またはデータ側の修正を検討する。

問題No.: 4
* 変数名と値: DS.DSDECOD (row 1), DS.DSTERM (row 2)
* 矛盾の内容: DSドメインのrow 1のDSDECODの値が "ADVERSE EVENT" であるのに対し、row 2のDSTERMの値が "FINAL LAB VISIT" となっている。DSDECODとDSTERMはカテゴリと用語が整合している必要がある。ADVERSE EVENTカテゴリに対して、FINAL LAB VISIT用語は不適切。
* 問題点の原因（推測）: データ入力時の用語選択ミス、またはカテゴリと用語の対応関係の誤解。
* 対応策（提案）:
    1. DSドメインのrow 2のDSTERMの値が "FINAL LAB VISIT" であるレコードについて、原資料（CRFなど）を確認し、DSTERMとDSDECODの適切な値を特定し修正する。
    2. データ入力担当者に対して、DSドメインにおけるDSTERMとDSDECODの用語選択に関する教育を徹底する。

クエリ:
患者ID: 01-703-1076
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMENDTC (null), CM.CMSEQ = 1, 4, 7, 10, 13, 16, 19, 23, 28, 33
    * 医療機関への問い合わせ文面: 患者ID 01-703-1076 の 併用薬（CM）ドメインについて、CMSEQ が 1, 4, 7, 10, 13, 16, 19, 23, 28, 33 のレコードの 併用薬終了日（CMENDTC）が欠損していますが、併用薬は継続中でしょうか？終了している場合、終了日を教えてください。
    * 判断理由: 併用薬の投与期間は、有害事象評価や有効性評価において重要な情報となるため、CMENDTCの欠損はデータの解釈に影響を与える可能性がある。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBORRESU, LB.LBSTRESU (単位不一致)
    * 医療機関への問い合わせ文面: 患者ID 01-703-1076 の 臨床検査（LB）ドメインについて、LBORRESU と LBSTRESU で単位が異なる項目が複数存在しますが、単位換算は意図的なものでしょうか？意図的な場合、単位換算のルールについて説明をお願いします。
    * 判断理由: 単位の不一致はデータの誤解を招く可能性があるため、単位換算の意図とルールを確認し、データの正確性を担保する必要がある。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMSTDTC (複数のレコードで2010年)
    * 医療機関への問い合わせ文面: 患者ID 01-703-1076 のCMドメインにおいて、併用薬CMTRT=ASPIRIN, TIMOPTIC, LOPIDのCMSTDTC（併用薬開始日）が2010年となっています。データ収集日（CMDTC）は2013年以降となっており、CMSTDTCの日付が過去すぎるように見受けられます。CMSTDTCの日付は正しいか、もし誤っている場合は正しい日付をご教示いただけますでしょうか。
    * 判断理由: CMドメインの併用薬開始日が不適切である可能性があり、データの正確性を確認する必要があるため。併用薬の開始日が誤っている場合、薬物相互作用の評価や、有害事象との関連性の評価に影響を与える可能性がある。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD=URATE, LBORRES=7.8 ~ 8.4 mg/dL, LBSTRESN=463.944 ~ 499.632 umol/L, LBSTNRHI=446 umol/L
    * 医療機関への問い合わせ文面: 患者ID 01-703-1076のLBドメインにおいて、Urate (尿酸) の検査値が基準範囲上限を超過 (LBSTRESN: 463.944 ~ 499.632 umol/L, LBSTNRHI: 446 umol/L) していますが、臨床的に問題ない範囲と判断してよろしいでしょうか？  医学的解釈についてご教示ください。
    * 判断理由: LB.URATEが基準範囲上限を超過しているものの、臨床的な意義が不明なため、医療機関に医学的妥当性を確認する必要がある。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1076
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=[MEVACOR, LIPITOR, CORTISONE, ASPIRIN, LOPID, TIMOPTIC], CMDECOD=[UNCODED, ACETYLSALICYLIC ACID]
        逸脱内容: 併用薬に関するプロトコル逸脱の疑義。MEVACOR, LIPITOR, CORTISONE, LOPID, TIMOPTIC, ASPIRINといった複数の薬剤が併用されており、プロトコルで禁止されている薬剤が含まれている可能性があります。特にMEVACORとLIPITORはHMG-CoA還元酵素阻害薬（スタチン系薬剤）、CORTISONEはコルチコステロイドであり、プロトコルでの扱いを確認する必要があります。また、一部併用薬（CORTISONE, LAC-HYDRIN, LIPITOR, MEVACOR, TIMOPTIC）がUNCODEDで記録されており、詳細な薬剤情報が不明です。
        プロトコル該当箇所: 3.8. Concomitant Therapy, 3.4.2.2. Exclusion Criteria (EXCL31) (プロトコルに併用禁止薬リストの明確な記載がない場合は「プロトコルに併用禁止薬リストの明確な記載なし」と記述)
        判断理由: CMドメインに記録された複数の併用薬について、プロトコル上の扱いが不明確であり、臨床試験結果に影響を与える可能性があります。特にMEVACOR, LIPITOR, CORTISONE, ASPIRIN, LOPIDは、治験薬との相互作用や安全性に影響を与える懸念があります。また、UNCODEDデータが含まれているため、正確な評価を行うためには医療機関への確認が必要です。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: SV.VISIT=AE FOLLOW-UP
        逸脱内容: SVドメインに記録されたAE FOLLOW-UP (VISITNUM=101) の実施が、プロトコルで規定された評価スケジュールからの逸脱の疑義があります。AE FOLLOW-UP自体は臨床的に必要となる場合もありますが、計画外のvisitとして、評価スケジュールからの逸脱として記録しておくことが適切と考えられます。
        プロトコル該当箇所: Protocol Attachment LZZT.1 Schedule of Events for Protocol H2Q-MC-LZZT(c), TVドメイン
        判断理由: SVドメインに記録されたAE FOLLOW-UP (VISITNUM=101) が、プロトコルで規定された評価スケジュールに明記されているか不明なため、逸脱の疑義ありと判断しました。

    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=[MEVACOR, LIPITOR, CORTISONE, LAC-HYDRIN, TIMOPTIC, ASPIRIN, LOPID], CMDECOD=[UNCODED, ACETYLSALICYLIC ACID]
        医療機関への問い合わせ文面:
        被験者01-703-1076に併用されている薬剤について、プロトコル3.8項「併用療法」または除外基準EXCL31に抵触していないか、また、治験薬との相互作用はないか確認が必要です。
        つきましては、以下の点についてご回答ください。
        1. プロトコルにおける併用薬に関する規定（併用禁止薬リスト、併用注意薬リストなど）をご提供ください。
        2. Concomitant Medications (CM) ドメインに記録されている以下の薬剤について、詳細な情報（具体的な薬剤名（商品名、一般名）、投与量、投与頻度、投与経路、投与期間、投与理由・適応疾患）をご提供ください。
            - ASPIRIN
            - CORTISONE
            - LAC-HYDRIN
            - LIPITOR
            - LOPID
            - MEVACOR
            - TIMOPTIC
        3. 特に、MEVACOR, LIPITOR, CORTISONE, ASPIRIN, LOPID の併用について、プロトコル上の許容範囲、および治験薬の効果に与える影響に関する治験責任医師の見解をご説明ください。

        判断理由: 併用薬に関するプロトコル遵守状況を詳細に確認し、被験者の安全性と臨床試験データの信頼性を確保するため、医療機関への問い合わせが必要と判断しました。特にMEVACOR, LIPITOR, CORTISONE, ASPIRIN, LOPID は、臨床試験結果に影響を与える可能性が高いため、詳細な情報を収集し、専門家の意見を求めることが重要です。

    クエリNo.: 2 (オプション)
        臨床試験結果への影響度合い: Minor
        変数名と値: SV.VISIT=AE FOLLOW-UP
        医療機関への問い合わせ文面:
        SVドメインに記録されているAE FOLLOW-UP (VISITNUM=101) は、プロトコルで計画されたvisit scheduleに含まれていますか？
        計画外のvisitである場合、実施理由と、評価項目（特にQuestionnairesドメインのデータ）への影響についてご説明ください。
        判断理由: AE FOLLOW-UP visit がプロトコルで計画されたものか確認し、評価スケジュールからの逸脱の有無と、臨床試験の評価項目に与える影響を把握するため、必要に応じてクエリを発行します。

クエリなし

# 01-701-1153
## Task1: Clinical Review Results
**1. 症例サマリーの作成:**

**患者ID:** 01-701-1153
*   2013年10月13日 (Day 21): 食欲亢進 (Adverse Event) が発現しました。
*   2013年12月16日 (Day 85): 尿検査でケトン体 1+ (ABNORMAL) が検出されました。
*   2014年01月08日 (Day 112): 血液検査でコレステロール値 310 mg/dL (HIGH) が検出されました。(基準範囲上限: 300 mg/dL)

---

**2. クエリの作成 (必要な場合のみ):**

*   **患者ID:** 01-701-1153
    *   **クエリNo.: 1**
        *   **臨床試験結果への影響度合い:** Major
        *   **変数名と値:** LB.LBTESTCD=CHOL, VISIT=WEEK 16, LBORRES=310, LBSTRESC=HIGH
        *   **医療機関への問い合わせ文面:**
            *   患者ID 01-701-1153 のWeek 16 (2014年01月08日) におけるコレステロール値が 310 mg/dL と基準値上限を超過 (HIGH) しています。
            *   安全性および医学的妥当性の観点から、以下の点についてご教示ください。
                1.  本患者のベースラインからのコレステロール値の変動推移と、臨床的な意義について
                2.  高コレステロール血症の原因として考えられる要因（食事、遺伝的要因、二次性疾患、併用薬など）
                3.  治験実施計画書に規定された除外基準に抵触しないか
                4.  患者の安全性確保のために追加で実施すべき検査や対応
        *   **判断理由:**
            *   コレステロール値の基準値上限超過は、医学的に懸念される状態であり、患者の安全性に関わる可能性があるため、Majorと判断しました。
            *   治験薬との因果関係、医学的妥当性、臨床試験の継続可否について、総合的に評価するために、医療機関への問い合わせが必要と考えられます。

    *   **クエリNo.: 2**
        *   **臨床試験結果への影響度合い:** Minor
        *   **変数名と値:** LB.LBTESTCD=KETONES, VISIT=WEEK 12, LBORRES=1, LBSTRESC=ABNORMAL
        *   **医療機関への問い合わせ文面:**
            *   患者ID 01-701-1153 のWeek 12 (2013年12月16日) の尿検査でケトン体が 1+ 検出されています。
            *   医学的妥当性の観点から、以下の点についてご教示ください。
                1.  ケトン体陽性が検出された背景因子 (食事、運動、脱水など)
                2.  臨床的に問題となる可能性
                3.  追加で実施すべき検査や対応
        *   **判断理由:**
            *   ケトン体陽性は、一般的に臨床的な意義が低い軽微な異常値と考えられますが、念のため医療機関に医学的解釈を確認することが望ましいと判断し、Minorとしました。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: LB.CHOL (LBSEQ=221), AE.AESTDTC, EXドメインの治験薬投与期間, DM.DMDTC, DM.DMDY, CM.CMSTDTC, LB.LBTESTCD=COLORのVISIT情報

問題点:
* 問題No.: 1
    * 変数名と値: LB.LBTESTCD=CHOL, LB.LBORRES=310 mg/dL (WEEK 16)
    * 矛盾の内容: LBドメインのCholesterol値が基準範囲上限(LBORNRHI=300 mg/dL)を超過。LBNRIND="HIGH"と異常値フラグは立っているが、医学的妥当性の確認が必要。
    * 問題点の原因（推測）: 患者の検査値異常、またはデータ入力時の誤りの可能性は低い。
    * 対応策（提案）: 医療機関にLB.CHOL値が医学的に問題ないか、また再検査が必要か等を確認する。

* 問題No.: 2
    * 変数名と値: AE.AESTDTC = 2013-10-13, EX.EXSTDTC = 2013-09-23, EX.EXENDTC = 2013-10-08
    * 矛盾の内容: 有害事象（AETERM=INCREASED APPETITE, AESEQ=1,2）の発現日(AESTDTC=2013-10-13)が、治験薬投与期間(EX.EXENDTC=2013-10-08)より後になっている。時系列矛盾の疑い。
    * 問題点の原因（推測）: データ入力時の誤り、EXドメインの投与期間の記録誤り、またはAE開始日の誤りの可能性。
    * 対応策（提案）: 医療機関に原資料を確認し、AE.AESTDTCとEXドメインの治験薬投与期間の記録を修正する。治験薬と有害事象の因果関係を再検討する。

* 問題No.: 3
    * 変数名と値: DM.DMDTC = 2013-09-06, DM.DMDY = -17
    * 矛盾の内容: DMドメインのデータ収集日(DMDTC=2013-09-06)が、計画訪問日(DM.DMDY = -17)と矛盾している。
    * 問題点の原因（推測）: DM.DMDTCまたはDM.DMDYのデータ入力時の誤り、VISITDYの計算誤り。
    * 対応策（提案）: DM.DMDTCとDM.DMDYの整合性を原資料で確認し、必要に応じて修正する。

* 問題No.: 4
    * 変数名と値: CM.CMSTDTC = 2011, CM.CMDTC = 2013-09-06
    * 矛盾の内容: CMドメインの併用薬開始日(CM.CMSTDTC = 2011)がデータ収集日(CM.CMDTC = 2013-09-06)より過去になっている。CMSTDTCはCMDTC以前の日付であるべき。
    * 問題点の原因（推測）: CM.CMSTDTCのデータ入力時の誤り（年が誤っている可能性）。
    * 対応策（提案）: CM.CMSTDTCとCMDTCの整合性を原資料で確認し、必要に応じて修正する。

* 問題No.: 5
    * 変数名と値: LB.LBTESTCD = COLOR, VISIT = UNSCHEDULED 5.1, UNSCHEDULED 9.2, UNSCHEDULED 9.3
    * 矛盾の内容: LBドメインの尿検査(COLOR, KETONES, PH, SPGRAV, UROBIL)が、計画外のUNSCHEDULED VISITで実施されている。プロトコル上の検査計画との整合性、データ収集の意図が不明。
    * 問題点の原因（推測）: プロトコルで計画外の検査が許可されているか不明、データ入力時のVISIT情報の誤りの可能性。
    * 対応策（提案）: 医療機関にUNSCHEDULED VISITでのURINALYSISカテゴリ検査実施の意図とプロトコル規定を確認する。

クエリ:
* 患者ID: 01-701-1153
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: AE.AESTDTC = 2013-10-13, EX.EXSTDTC = 2013-09-23, EX.EXENDTC = 2013-10-08 (EXSEQ=1)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1153 において、有害事象「食欲亢進 (INCREASED APPETITE)」(AESEQ=1,2) の発現日（2013-10-13）が、治験薬（プラセボ）投与期間（2013-09-23～2013-10-08）と矛盾しているように見えます。原資料を確認いただき、有害事象の正確な発現日、治験薬投与期間をご教示ください。もしデータに誤りがない場合、治験薬（プラセボ）と有害事象の因果関係に関する治験責任医師の見解をご教示ください。
        * 判断理由: 治験薬と有害事象の因果関係評価に関わる重要な矛盾であり、データの信頼性を損なう可能性があるため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD = CHOL, LB.LBORRES = 310 mg/dL (WEEK 16)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1153 のWEEK 16におけるコレステロール値が基準範囲上限を超過しています。データ入力値が正しいか原資料をご確認ください。真値の場合、医学的に臨床上問題ないか、治験責任医師の見解をご教示ください。
        * 判断理由: コレステロール値異常値は患者安全性に関わる可能性があり、医学的評価の確認が必要なため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DM.DMDTC = 2013-09-06, DM.DMDY = -17
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1153 のDMドメインにおいて、データ収集日(DMDTC)と計画訪問日(DM.DMDY)に矛盾が見られます。DMドメインのデータ収集日と計画訪問日の原資料をご確認いただき、正しい日付をご教示ください。
        * 判断理由: DMドメインのデータ収集日の不整合は、データ全体の正確性に疑念を生じさせるため、早急な確認と修正が必要である。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC = 2011, CM.CMDTC = 2013-09-06
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1153 のCMドメインにおいて、併用薬開始日(CMSTDTC)がデータ収集日(CMDTC)より過去になっています。CMドメインの併用薬開始日とデータ収集日の原資料をご確認いただき、正しい日付をご教示ください。
        * 判断理由: CMドメインの開始日とデータ収集日の矛盾は、データ入力 या 収集プロセスのエラーを示唆する可能性があり、データ品質全体に影響を与える可能性があるため。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD = COLOR, VISIT = UNSCHEDULED 5.1, UNSCHEDULED 9.2, UNSCHEDULED 9.3
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1153 のLBドメインにおいて、UNSCHEDULED VISITで尿検査(COLOR等)が複数回実施されています。UNSCHEDULED VISITで尿検査を実施した意図についてご教示いただけますでしょうか。
        * 判断理由: 計画外の検査の実施理由を確認し、データの解釈を明確にするため。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1153
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: QS.QSTESTCD=MMTOT, VISIT=BASELINE
        逸脱内容: ベースライン時のMMSEスコアが欠損しており、選択基準INCL03「MMSEスコア 10〜23」を満たしているか不明。選択基準を満たさない可能性があり、プロトコル逸脱に該当する。
        プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [3]
        判断理由: MMSEスコアは重要な選択基準であり、欠損はプロトコル逸脱の可能性を示唆する。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=CHOL, VISIT=WEEK 16, LBORRES=310 mg/dL, LBORNRLO=156 mg/dL, LBORNRHI=300 mg/dL, LBNRIND=HIGH
        逸脱内容: WEEK 16のコレステロール値が基準範囲上限を超過。除外基準EXCL27に抵触する可能性があり、プロトコル逸脱の可能性がある。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
        判断理由: コレステロール値の異常値は除外基準に抵触する可能性があり、臨床試験結果に影響を与える可能性がある。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CMTRT=TYLENOL
        逸脱内容: 治験期間中に併用薬TYLENOLを使用。プロトコルに併用禁止薬の規定がないため、現時点ではプロトコル逸脱と断定できないが、試験結果に影響を与える可能性があり、確認が望ましい。
        プロトコル該当箇所: プロトコルに併用禁止薬に関する明確な記述なし
        判断理由: TYLENOLの併用がプロトコルに抵触するか不明だが、臨床試験結果への影響を考慮し、確認事項として検出。

    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: LBTESTCD=CHOL, VISIT=WEEK 16, LBORRES=310 mg/dL
        医療機関への問い合わせ文面: 
        被験者01-701-1153のWEEK 16のコレステロール値が基準値上限を超過していますが、臨床医学的に問題がないか、またプロトコルで規定された対応が取られているか確認をお願いいたします。
        判断理由: プロトコルで規定された臨床検査の基準値からの逸脱の可能性があるため、臨床試験結果への影響を評価するために医療機関への確認が必要と判断しました。

    クエリNo.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: CMTRT=TYLENOL
        医療機関への問い合わせ文面: 
        被験者01-701-1153において、併用薬としてTYLENOLが記録されています。TYLENOLは本試験プロトコルにおいて併用禁止薬に該当しますでしょうか。併用可能な場合、治験薬との相互作用について問題ないか、念のため確認させてください。
        判断理由: プロトコル上、TYLENOLの併用可否が不明なため、医療機関に確認し、プロトコル遵守状況を明確にする必要があると判断しました。

# 01-704-1009
## Task1: Clinical Review Results
**症例サマリー:**

**患者ID:** 01-704-1009
* 2013年08月20日 (Day -7): スクリーニング1回目の検査にて、コレステロール (CHOL) およびヘモグロビン (HGB) が基準値より低い (LOW)。併用薬としてBENADRYL, BUFFERIN, MULTIVITAMIN, VITAMIN Eを服用。
* 2013年08月24日 (Day -3): スクリーニング2回目の来院。併用薬としてBENADRYL, BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN Eを服用。
* 2013年08月27日 (Day 1): ベースライン来院。併用薬としてBUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN Eを服用。
* 2013年09月05日 (Day 10): 有害事象 FATIGUE (疲労) および MALAISE (倦怠感) が発現（軽度）。
* 2013年09月14日 (Day 19): WEEK 2回目の来院。検査値ALT、CL、SODIUMが基準値上限を超過 (HIGH)。検査値HCT、HGB、LYM、RBCが基準値下限を下回る (LOW)。有害事象 RASH (発疹) が発現（軽度）。併用薬としてBUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN Eを服用。
* 2013年09月17日 (Day 22): 有害事象 DIZZINESS (めまい) が発現（軽度）。
* 2013年09月22日 (Day 27): 有害事象 CHRONIC KIDNEY DISEASE (慢性腎臓病) および NAUSEA (悪心) が発現（軽度）。
* 2013年09月23日 (Day 28): 有害事象 NAUSEA (悪心) および CHRONIC KIDNEY DISEASE (慢性腎臓病) が回復/解消。
* 2013年09月27日 (Day 32): 有害事象 MALAISE (倦怠感) が回復/解消。ただし、倦怠感はその後も未回復として記録されている。
* 2013年10月02日 (Day 37): WEEK 4回目の来院、最終来院、治験中止。有害事象 DIZZINESS (めまい)、FATIGUE (疲労)、RASH (発疹)、MALAISE (倦怠感) が未回復/未解消。併用薬としてBUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN Eを服用。治験中止理由は「TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS (時間がかかりすぎる、今後のホルター検査を拒否)」。

---

**クエリ:**

**患者ID:** 01-704-1009
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: DS.DSTERM = "TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS"
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 の WEEK 4 (2013-10-02) の Dispositon (DS) ドメインにおいて、治験中止理由が「TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS (時間がかかりすぎる、今後のホルター検査を拒否)」と記録されています。
        * WEEK 4 は主要評価項目測定時期と推察されますが、主要評価項目データに欠損はないでしょうか。主要評価項目に欠損がある場合、治験結果に与える影響について評価してください。
        * また、治験中止の理由に医学的な事象が含まれている可能性も考慮し、治験中止に至った経緯について、詳細をご教示ください。
    * 判断理由:
        * 治験中止理由が「TOO TIME CONSUMING;PT REFUSED FUTURE HOLTERS」とあり、治験実施医療機関の判断による中止か、治験参加者希望による中止か、詳細不明です。
        * WEEK 4は主要評価項目測定時期であり、データ欠損の有無は有効性評価に大きく影響するため、影響度を Major としました。
        * 治験中止の理由に医学的な事象が含まれている可能性も考慮し、詳細な経緯を確認する必要があると判断しました。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD = ALT, LB.LBORRES = 39, VISIT = WEEK 2, LBNRIND = HIGH
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 の WEEK 2 (2013-09-14) の 臨床検査値 (LB) ドメインにおいて、アラニンアミノトランスフェラーゼ (ALT) が 39 U/L と基準値上限を超えています。
        * ALT値上昇の原因、および臨床的な意義についてご評価ください。治験薬との関連性、肝機能障害の可能性、再検査の実施有無、ALT上昇に対する処置、経過観察の有無について、医学的見解をご共有ください。
    * 判断理由:
        * ALT値の上昇は肝機能障害を示唆する可能性があり、患者の安全性に関わる重要な情報であるため、医療機関への確認が必要です。
        * 治験薬との因果関係、臨床的な対応、今後の経過観察について確認が必要なため、臨床試験結果への影響度合いを Major としました。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = SODIUM, LB.LBORRES = 146, VISIT = WEEK 2, LBNRIND = HIGH
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 の WEEK 2 (2013-09-14) の 臨床検査値 (LB) ドメインにおいて、ナトリウム (SODIUM) が 146 mEq/L と基準値上限を超えています。
        * ナトリウム値が上昇した原因、および臨床的な意義についてご評価ください。脱水、食事、腎機能障害など、考えられる要因と、ナトリウム値上昇に対する処置、経過観察の有無について、医学的見解をご共有ください。
    * 判断理由:
        * ナトリウム値の上昇は、脱水や腎機能障害などを示唆する可能性があり、医学的妥当性の観点から確認します。
        * クエリNo.2のALT上昇に比べると、臨床的な緊急性は低いと考えられ、臨床試験結果への影響度合いは Minor と判断しました。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = CHOL, LB.LBORRES = 138 mg/dL (WEEK 2), LBORRES = 144 mg/dL (SCREENING 1), LBNRIND = LOW
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 において、スクリーニング1 (Day -7) および WEEK 2 (Day 14) の検査でコレステロール (CHOL) が基準値下限を下回っています。
        * コレステロール値低下の原因、および臨床的な意義についてご評価ください。栄養状態、吸収不良、肝機能障害など、考えられる要因と、コレステロール値低下に対する処置、経過観察の有無について、医学的見解をご共有ください。
    * 判断理由:
        * コレステロール値の低下は、栄養状態や吸収不良など、様々な要因が考えられます。臨床的な意義を確認するため医療機関への確認が必要ですが、臨床的な緊急性は低いと考えられ、臨床試験結果への影響度合いは Minor と判断しました。

* クエリNo.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = HGB, LB.LBORRES = 11.1 g/dL (WEEK 2), LBORRES = 12.4 g/dL (SCREENING 1), LBNRIND = LOW, LB.LBTESTCD = HCT, LB.LBORRES = 33.0 % (WEEK 2), LBNRIND = LOW, LB.LBTESTCD = RBC, LB.LBORRES = 3.70 MILL/uL (WEEK 2), LBNRIND = LOW, LB.LBTESTCD = LYM, LB.LBORRES = 0.72 THOU/uL (WEEK 2), LBNRIND = LOW
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 において、WEEK 2 (Day 14) の検査でヘモグロビン (HGB)、ヘマトクリット (HCT)、赤血球数 (RBC)、リンパ球数 (LYM) が基準値下限を下回っています。
        * これらの検査値低下の原因、および臨床的な意義についてご評価ください。貧血、炎症反応、骨髄抑制など、考えられる要因と、これらの検査値低下に対する処置、経過観察の有無について、医学的見解をご共有ください。
    * 判断理由:
        * 複数の血液検査値で基準値下限を下回る結果が確認されており、貧血や炎症反応など、潜在的な病態を把握するために医療機関に確認することが望ましいと判断しました。
        * クエリNo.2のALT上昇に比べると、臨床的な緊急性は低いと考えられ、臨床試験結果への影響度合いは Minor と判断しました。

* クエリNo.: 6
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM=DIZZINESS, AE.AEENDY=null, AE.AEOUT=NOT RECOVERED/NOT RESOLVED, AE.AETERM=FATIGUE, AE.AEENDY=null, AE.AEOUT=NOT RECOVERED/NOT RESOLVED, AE.AETERM=MALAISE, AE.AEENDY=32, AE.AEOUT=NOT RECOVERED/NOT RESOLVED, AE.AETERM=RASH, AE.AEENDY=null, AE.AEOUT=NOT RECOVERED/NOT RESOLVED
    * 医療機関への問い合わせ文面:
        * 患者ID 01-704-1009 において、複数の有害事象（めまい、疲労、倦怠感、発疹）がWEEK4の最終観察時まで未回復です。
        * これらの有害事象に対する、治験実施医療機関における対応 ( symptom management) について、情報をご共有ください。
        * 特に、治験中止理由に「PT REFUSED FUTURE HOLTERS (今後のホルター検査を拒否)」とありますが、有害事象とホルター検査拒否との関連性について、医療機関の見解をご教示ください。
    * 判断理由:
        * 複数の有害事象が長期にわたり未回復であり、患者のQOL (生活の質) に影響を与えている可能性、および治験中止理由に繋がっている可能性を考慮し、医療機関への確認が必要と判断しました。
        * ただし、重篤な有害事象ではないため、臨床試験結果への影響度合いは Minor としました。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, LB.LBSTRESC, LB.LBSTRESN, LB異常値とAEの関連, AE重複レコード, AEとEXの投与期間の整合性, DS.DSDTC, LB.LBDTC, VS.SYSBP

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMSTDTC, CM.CMDTC (日付不整合)
    * 矛盾の内容: 複数のCMレコードでCM開始日(CMSTDTC)がデータ収集日(CMDTC)より未来日になっている。特にCMSTDTCの年が2009年となっているレコードはCMDTCの2013年と大きく乖離しており、誤りの可能性が高い。
    * 問題点の原因（推測）: データ入力時の日付誤り（年号の誤り、未来日の誤入力）
    * 対応策（提案）: 医療機関にCM.CMSTDTCの日付の正誤を確認し、必要に応じて修正を依頼する。

* 問題No.: 2
    * 変数名と値: LB.LBSTRESN, LB.LBSTRESC (不一致)
    * 矛盾の内容: LBドメインのLBSTRESN（数値結果）とLBSTRESC（文字結果）の値が一部レコードで一致しない。LBSTRESNがnullであるにもかかわらずLBSTRESCに値が設定されているレコード、LBSTRESNとLBSTRESCで数値が異なるレコードが存在する。
    * 問題点の原因（推測）: データ入力時の転記ミス、データ変換ロジックの不備
    * 対応策（提案）: データ入力元資料（CRF）と照合し、LBSTRESNとLBSTRESCの値を修正する。データ変換ロジックに不備がある場合は修正する。

* 問題No.: 3
    * 変数名と値: AE.AETERM (MALAISE), AE.AESEQ (2, 4) (AE重複の疑義)
    * 矛盾の内容: AEドメインにMALAISE（倦怠感）がAESEQ=2と4で重複して報告されている。開始日、終了日が一部重複しており、同一の有害事象を複数回記録した可能性がある。
    * 問題点の原因（推測）: AEデータ入力時の重複登録、または異なるMALAISEイベントの誤登録の可能性
    * 対応策（提案）: 医療機関にAE AESEQ=2と4のMALAISEが同一事象か別事象か確認し、重複であれば削除、別事象であればそれぞれ内容を確認する。

* 問題No.: 4
    * 変数名と値: AE.AETERM (DIZZINESS, NAUSEA), EX.EXENDTC, AE.AESTDTC (AEとEXの投与期間の不整合)
    * 矛盾の内容: AE.AETERMがDIZZINESS（めまい）とNAUSEA（吐き気）の有害事象について、AE.AESTDTC（有害事象開始日）がEX.EXENDTC（治験薬最終投与日）より後になっている。治験薬投与終了後に発現した有害事象であり、治験薬との因果関係が低い可能性がある。
    * 問題点の原因（推測）: 治験薬との因果関係が低い有害事象、またはデータ入力時の日付誤りの可能性
    * 対応策（提案）: 医療機関にAE DIZZINESS、NAUSEAの治験薬との因果関係について再評価を依頼する。

* 問題No.: 5
    * 変数名と値: CM.CMENDTC (空欄), CM.CMTRT (BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN E) (CM終了日欠損)
    * 矛盾の内容: CM.CMENDTC (Concomitant Medication 終了日) が空欄となっているBUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN Eについて、Concomitant Medicationが終了しているか不明。
    * 問題点の原因（推測）: データ未入力、またはConcomitant Medicationが継続中の可能性
    * 対応策（提案）: 医療機関にConcomitant Medicationが終了しているか確認し、終了している場合はCM.CMENDTCを追記するよう依頼する。継続中の場合は、CMENDTCは空欄のままで問題ない。

* 問題No.: 6
    * 変数名と値: LB.LBDTC, DS.DSDTC, VISITDY, VISITNUM (VISIT情報不整合)
    * 矛盾の内容: LBドメインとDSドメインにおいて、LBDTC, DSDTC の VISITDY が VISITNUM (WEEK2) と整合していない。VISITDYが19日目であるのに対し、VISITNUMが14日目(WEEK2)となっている。
    * 問題点の原因（推測）: VISITNUM (計画) と VISITDY (実績) のデータ入力時の不整合、またはVISIT情報そのものの誤り
    * 対応策（提案）: VISITNUM, VISITDY, LBDTC, DSDTC の情報が整合しているか確認し、必要であれば修正。

* 問題No.: 7
    * 変数名と値: VS.VSTESTCD = SYSBP, VISIT = BASELINE, VSPOS = SUPINE, VSORRES = 146 (VS高値)
    * 矛盾の内容: VS.SYSBP (仰臥位) が 146 mmHg とやや高値。プロトコルに組み入れ基準/除外基準に関する詳細な記述はないが、一般的に高血圧は注意が必要な状態であり、安全性評価の観点から問題となる可能性がある。
    * 問題点の原因（推測）: 患者のデータ入力時の偶発的な高血圧、または継続的な高血圧の可能性
    * 対応策（提案）: 患者のMedical History (MH) ドメインに高血圧の既往歴がないか確認。もし高血圧の既往歴がない場合、Week 2, Week 4 のVSデータも確認し、継続的に高血圧が認められるようであれば、医学的評価が必要となる可能性を考慮。

* 問題No.: 8
    * 変数名と値: LB.LBTESTCD (ALT, CL, SODIUM), VISIT = WEEK2 (LB軽度高値)
    * 矛盾の内容: LB.ALT, LB.CL, LB.SODIUM が Week2 で軽度高値。臨床的な意義は低い可能性もあるが、念のため確認。
    * 問題点の原因（推測）: 患者の生理的な変動、または試験薬の影響
    * 対応策（提案）: 臨床検査値の変動が臨床的に意義があるかどうか、治験責任医師に確認。

クエリ:
* 患者ID: 01-704-1009
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC, CMDTC
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 の併用薬データについて、CM開始日 (CMSTDTC) がデータ収集日 (CMDTC) より過去になっているレコードが複数あります。原資料をご確認いただき、CM開始日の日付に誤りがないか確認してください。特に、BENADRYL, BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN E のCMレコードの開始年 (CMSTDTCの年) に誤りがないか確認をお願いいたします。もし誤りがある場合は、正しい日付をご教示ください。
        * 判断理由: CM開始日の誤りは併用薬の評価に影響し、臨床試験データの信頼性を損なう可能性があるため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBSTRESN, LB.LBSTRESC
        * 医療機関への問い合わせ文面: LBドメインのLBSTRESN（数値結果）とLBSTRESC（文字結果）の値に不一致が複数箇所見られます。原資料をご確認いただき、LBSTRESNとLBSTRESCの正しい値を回答ください。
        * 判断理由: LB検査結果の数値データと文字データの不一致は、データの正確性に疑義を生じさせるため、早急な確認と修正が必要である。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AETERM = MALAISE (AESEQ=2, 4)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 に 倦怠感 (MALAISE) の有害事象が2件 (AESEQ=2, AESEQ=4) 報告されています。これらは同一の有害事象の重複記録でしょうか？重複記録の場合は、単一のレコードに統合してください。異なる事象の場合は、それぞれの事象について、より詳細な情報 (発現日、重症度、治験薬との因果関係など) をご提供ください。
        * 判断理由: 有害事象の重複記録は、安全性評価に影響を与えるため、正確性を確認する必要がある。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC (空欄), CM.CMTRT (BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN E)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 の 併用薬 BUFFERIN, CLARITIN, MULTIVITAMIN, VITAMIN E は投与終了していますでしょうか？終了している場合、CM終了日 (CMENDTC) を教えてください。
        * 判断理由: CM終了日の欠損はデータの完全性を損なうため、確認しデータ品質を向上させる。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBDTC, DS.DSDTC, VISITDY, VISITNUM
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 の 臨床検査(LB) および 治験薬投与(DS) のデータにおいて、データ採取日/投与日の VISITDY (治験薬投与からの日数) が VISITNUM (計画訪問) とずれています。VISITNUM, VISITDY, LBDTC, DSDTC の情報が正しく整合しているか確認し、必要であれば修正してください。
        * 判断理由: VISIT関連情報の不整合は、データ解釈に混乱を招く可能性があるため、整合性を確認する。

    * クエリNo.: 6
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD = ALT, CL, SODIUM, VISIT = WEEK2
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 の 臨床検査値 ALT, CL, SODIUM が Week2 で基準値上限を超えています。臨床的に問題がないか念のため治験責任医師にご確認ください。
        * 判断理由: 臨床検査値の軽度な基準値外れについて、医学的見地から臨床的な意義がないことを確認するため。

    * クエリNo.: 7
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: VS.VSTESTCD = SYSBP, VISIT = BASELINE, VSPOS = SUPINE, VSORRES = 146
        * 医療機関への問い合わせ文面: 患者ID 01-704-1009 の ベースライン時の仰臥位での収縮期血圧が146mmHgとやや高めです。患者の高血圧の既往歴や、他に注意すべき医学的問題がないか確認してください。
        * 判断理由: ベースライン時の血圧高値について、患者の医学的背景情報を確認し、安全性上の懸念がないことを確認するため。

クエリなし
## Task3: Protocol Deviation Review Results
患者ID: 01-704-1009
* 逸脱No.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMTRT = BENADRYL, CLARITIN
    * 逸脱内容: 併用薬として報告されているBENADRYLとCLARITINは、中枢神経抑制作用や眠気等の副作用が知られており、プロトコルで併用が禁止されている可能性がある。プロトコルで併用が禁止されている薬剤リスト、または併用注意とされている薬剤リストに、BENADRYLとCLARITINが含まれていないか確認が必要である。併用禁止薬に該当する場合、臨床試験の評価項目（特に認知機能評価）や安全性評価に影響を与える可能性がある。
    * プロトコル該当箇所: プロトコルの併用禁止薬、併用注意薬に関するセクション
    * 判断理由: BENADRYLとCLARITINは、臨床試験の評価項目に影響を与える可能性があるため、プロトコルにおける取扱いを確認する必要がある。

* 逸脱No.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD=ALT, LBORRES=39 U/L (レコード37, LBSEQ=37)
    * 逸脱内容: 臨床検査値（ALT）が基準値上限を超過している。プロトコル exclusion criteria [27b] に抵触する可能性がある。ただし、Define.xml及びSUPPLBドメインからデータ取得・SDTMデータ作成手順は遵守されていると判断される。
    * プロトコル該当箇所: 3.9.3.3 臨床検査テスト、EXCLUDE CRITERIA [27b]
    * 判断理由: ALT値が施設基準範囲上限を超過しているが、データ作成手順は遵守されている。ALT値上昇の原因、臨床的意義について治験担当医師の見解を確認することが望ましい。

* 逸脱No.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD=SODIUM, LBORRES=146 mEq/L (レコード60, LBSEQ=60)
    * 逸脱内容: 臨床検査値（ナトリウム）が基準値上限を超過している。プロトコル exclusion criteria [27b] に抵触する可能性がある。ただし、Define.xml及びSUPPLBドメインからデータ取得・SDTMデータ作成手順は遵守されていると判断される。
    * プロトコル該当箇所: 3.9.3.3 臨床検査テスト、EXCLUDE CRITERIA [27b]
    * 判断理由: ナトリウム値が施設基準範囲上限を超過しているが、データ作成手順は遵守されている。ナトリウム値上昇の原因、臨床的意義について治験担当医師の見解を確認することが望ましい。

* 逸脱No.: 4
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: MH.MHTERM=MYOCARDIAL INFARCTION, MH.MHSTDTC=空白
    * 逸脱内容: 既往歴「MYOCARDIAL INFARCTION（心筋梗塞）」の発症時期が不明。プロトコル除外基準EXCL17「過去5年以内の重篤な心血管障害の病歴」に抵触する可能性がある。
    * プロトコル該当箇所: 除外基準 EXCL17
    * 判断理由: 既往歴「MYOCARDIAL INFARCTION」がプロトコル除外基準 EXCL17 に抵触する可能性があるため、医療機関に確認が必要。

* 逸脱No.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMDECOD: UNCODED (全併用薬)
    * 逸脱内容: 併用薬の標準化された薬剤名（CMDECOD）が全てUNCODEDで報告されている。Define.xmlにはValueListが定義されているにもかかわらず、データ上UNCODEDとなっている。
    * プロトコル該当箇所: プロトコルに併用薬の標準化に関する具体的な規定の記載なし (Define.xmlとSDTMに準拠)。
    * 判断理由: Define.xmlとデータに不整合が見られるため、データ品質管理上の逸脱の可能性がある。

* 逸脱No.: 6
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMDOSUの値リストがDefine.xmlに定義されていない
    * 逸脱内容: 併用薬の投与単位（CMDOSU）の値リストがDefine.xmlに定義されていない。
    * プロトコル該当箇所: プロトコルにCMDOSUの値リストに関する具体的な規定の記載なし (Define.xmlとSDTMに準拠)。
    * 判断理由: Define.xmlのメタデータ定義に不備がある可能性がある。

* 逸脱No.: 7
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.VISIT = WEEK 2, LB.VISITDY = 19 (レコード37, LBSEQ=37, LBTESTCD=ALT)
    * 逸脱内容: 臨床検査(LB)ドメインのWEEK 2のVISITにおいて、一部レコードのVISITDYが19日となっており、計画されたVISITDY (14日) から逸脱している可能性がある。
    * プロトコル該当箇所: VISIT SCHEDULE (プロトコル添付資料 LZZT.1)
    * 判断理由: データ入力エラーまたは評価スケジュール逸脱の疑義がある。

* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMTRT = BENADRYL, CLARITIN, CMSTDTC, CMENDTC
    * 医療機関への問い合わせ文面:
        被験者01-704-1009にて併用が報告されているBENADRYL、CLARITINについて、プロトコルにおける併用禁止/注意薬の規定に抵触するかご教示ください。抵触する場合は、投与開始日、投与終了日、投与量、投与経路、投与理由の詳細をご回答ください。
    * 判断理由: プロトコルにおける併用薬規定への抵触の可能性を確認するため。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: MH.MHTERM=MYOCARDIAL INFARCTION, MH.MHSTDTC=空白
    * 医療機関への問い合わせ文面:
        被験者01-704-1009の既往歴「MYOCARDIAL INFARCTION（心筋梗塞）」について、発症時期の詳細（5年以内かどうか）をご教示ください。
    * 判断理由: プロトコル除外基準EXCL17抵触の可能性を確認するため。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.VISIT = WEEK 2, LB.VISITDY = 19 (レコード37, LBSEQ=37, LBTESTCD=ALT)
    * 医療機関への問い合わせ文面:
        被験者01-704-1009の臨床検査(LB)ドメイン、WEEK 2 VISIT (LBSEQ=37, LBTESTCD=ALT) のVISITDYが19日となっています。データ入力エラーまたは評価スケジュールからの逸脱の疑いがあるため、VISITDY19日がデータ入力誤りでないか、意図的な評価日変更があったか等、事実確認と理由をご回答ください。
    * 判断理由: LBドメインのVISITDYが評価スケジュールからずれている原因を特定するため。

# 01-704-1010
## Task1: Clinical Review Results
患者ID: 01-704-1010
* 2014年04月11日 (Day 50): 検査値ビリルビンが基準値上限を超過 (1.3 mg/dL, 基準値: 0.2 - 1.2 mg/dL) (WEEK 6)
* 2014年05月30日 (Day 99): 検査値ビリルビンが基準値上限を超過 (1.3 mg/dL, 基準値: 0.2 - 1.2 mg/dL) (UNSCHEDULED 9.2)
* 2014年07月05日 (Day 135): 有害事象 下痢、嘔吐 発現 (軽度)
* 2014年07月06日 (Day 136): 有害事象 関節痛、挫傷、皮膚剥離、皮膚裂傷 発現 (軽度)
* 2014年07月06日 (Day 136): 有害事象 下痢、嘔吐 軽快
* 2014年07月09日 (Day 139): 検査値ビリルビンが基準値上限を超過 (1.3 mg/dL, 基準値: 0.2 - 1.2 mg/dL) (WEEK 20)
* 2014年07月09日 (Day 139): 検査値カルシウムが基準値下限を下回る (8.3 mg/dL, 基準値: 8.4 - 10.3 mg/dL) (WEEK 20)
* 2014年07月09日 (Day 139): 試験中止 (PATIENT IS MOVING, WITHDRAWAL BY SUBJECT) (WEEK 20, Day 139)
* 2014年07月09日 (Day 139): 有害事象 関節痛、挫傷、皮膚剥離、皮膚裂傷 継続中

---
患者ID: 01-704-1010
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD=BILI, LB.LBORRES=1.3 mg/dL (WEEK 6, UNSCHEDULED 9.2, WEEK 20)
    * 医療機関への問い合わせ文面:
        患者ID 01-704-1010 において、ビリルビン値がWeek 6、Unscheduled 9.2、Week 20と、複数回にわたり基準値上限を超過しています。肝機能障害の可能性も考慮し、医学的な解釈と対応をご教示ください。
    * 判断理由:
        ビリルビン値の上昇が複数回認められ、肝機能障害、ひいては治験薬の投与継続や患者の安全性に影響を与える可能性があるため、医学的な解釈と対応について医療機関に問い合わせる必要があると判断しました。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LBTESTCD=CA, LBORRES=8.3 mg/dL (WEEK 20)
    * 医療機関への問い合わせ文面:
        患者ID 01-704-1010 において、カルシウム値がWeek 20で基準値下限を下回っていますが、臨床的に懸念される事項はありますか？
    * 判断理由:
        カルシウム値の低下は軽微であり、直ちに臨床的に重大な懸念を生じさせる可能性は低いと考えられますが、念のため医学的な解釈について医療機関に問い合わせることとしました。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM = DIABETES MELLITUS, MH.MHTERM = ALZHEIMER'S DISEASE, HYPERTENSION
    * 医療機関への問い合わせ文面: 
        患者ID 01-704-1010 において、Adverse EventとしてDIABETES MELLITUS (E01) が報告されていますが、Medical HistoryにあるALZHEIMER'S DISEASEやHYPERTENSIONと病態的に関連がある可能性はありますでしょうか。Adverse EventのDIABETES MELLITUSのMedDRA LLT/DECODには膀胱炎(CYSTITIS)が登録されていますが、Reported Term for the Adverse Event (AETERM) は DIABETES MELLITUS となっており、用語の不一致が見られます。DIABETES MELLITUS (E01) の詳細について確認させてください。
    * 判断理由:
        Adverse EventとMedDRA用語、Reported Termに不一致が見られるDIABETES MELLITUS (E01) の詳細について確認し、Medical Historyとの関連性を評価する必要があるため、医療機関への問い合わせが必要と判断しました。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CMドメイン、EXドメイン、MHドメインの日付整合性、LBドメインのBILI (ビリルビン) および CA (カルシウム) の異常値、AEドメインとDSドメインの終了日欠損

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMDTC, CM.CMSTDTC (CMドメイン全般の日付関連変数)
    * 矛盾の内容: 併用薬 (CM) ドメインにおいて、データ収集日 (CMDTC) が併用薬開始日 (CMSTDTC) より未来の日付となっているレコードが複数存在する。具体的には、CMDTCが2014年であるのに対し、CMSTDTCが2012年となっている例や、CMDTC="2014-02-08"に対してCMSTDTC="2012"などの矛盾が散見される。
    * 問題点の原因（推測）: データ入力時の誤り、特に日付の年の部分の誤記の可能性。
    * 対応策（提案）: 医療機関にCMドメインの日付情報の再確認と修正を依頼する。特に、各併用薬の開始日・終了日とデータ収集日が実際の記録と一致しているか確認する。

* 問題No.: 2
    * 変数名と値: EX.VSDTC, EX.EXSTDTC (EXドメイン全般の日付関連変数)
    * 矛盾の内容: 治験薬投与 (EX) ドメインにおいて、データ収集日 (VSDTC) が治験薬投与開始日 (EXSTDTC) より未来の日付となっているレコードが複数存在する。具体的には、VSDTC="2014-02-08"に対してEXSTDTC="2014-02-21"などの矛盾が散見される。
    * 問題点の原因（推測）: データ入力時の日付誤りの可能性。
    * 対応策（提案）: 医療機関にEXドメインの日付情報の再確認と修正を依頼する。特に、治験薬の投与開始日・終了日とデータ収集日が実際の記録と一致しているか確認する。

* 問題No.: 3
    * 変数名と値: MH.MHDTC, MH.MHSTDTC (MHドメイン全般の日付関連変数)
    * 矛盾の内容: 既往歴 (MH) ドメインにおいて、データ収集日 (MHDTC) が既往歴開始日 (MHSTDTC) より未来の日付となっているレコードが複数存在する。具体的には、MHDTC="2014-02-08"に対してMHSTDTC="2006-01-02"などの矛盾が散見される。
    * 問題点の原因（推測）: データ入力時の日付誤りの可能性。
    * 対応策（提案）: 医療機関にMHドメインの日付情報の再確認と修正を依頼する。特に、各既往歴の開始日とデータ収集日が実際の記録と一致しているか確認する。

* 問題No.: 4
    * 変数名と値: AE.AEENDTC (複数レコード), CM.CMENDTC (多数レコード)
    * 矛盾の内容: AEドメインのAEENDTC、CMドメインのCMENDTCに欠損値が散見される。特にCM.CMENDTCの欠損が多いため、併用薬の投与終了日が不明となっている症例が多いことが懸念される。AEドメインでは有害事象の継続期間、CMドメインでは併用薬の投与期間が不明確になる。
    * 問題点の原因（推測）: データ収集時の未記入、データ入力時の転記漏れ、または併用薬が継続中のため終了日が未入力の可能性。
    * 対応策（提案）: 
        1. AE.AEENDTCについては、医療機関に問い合わせ、有害事象の継続期間を確認し、終了日を特定できる場合はデータを追記する。有害事象が継続中の場合は、その旨を記録し、今後のデータ更新で終了日を追記するよう依頼する。
        2. CM.CMENDTCについては、併用薬の種類、投与期間、投与目的などを考慮し、医療機関に問い合わせ、投与終了日を特定できる場合はデータを追記する。併用薬が投与継続中の場合は、終了日を追跡するプロセスを確立する。

* 問題No.: 5
    * 変数名と値: LB.LBTESTCD=BILI, LBORRES=1.3mg/dL, LBNRIND=HIGH (WEEK 6, 9.2, 20)
    * 矛盾の内容: Bilirubin値が基準範囲上限 (LBORNRHI=1.2 mg/dL) を超えている (LBORRES=1.3mg/dL) レコードが複数回 (WEEK 6, UNSCHEDULED 9.2, WEEK 20) 報告されている。臨床的に意義のある異常値かどうか不明。
    * 問題点の原因（推測）: 患者の肝機能異常、またはデータ入力時の誤りの可能性。
    * 対応策（提案）: 
        1. Define.xmlに定義されているLB.LBTESTCD="BILI"の基準範囲に関する情報を確認する。
        2. プロトコルにBilirubin値異常に関する規定がないか確認する。
        3. 医療機関にLBドメインとAEドメイン、MHドメインを再調査し、Bilirubin値上昇の原因、および臨床的な意義について評価を依頼する。関連する有害事象の有無も確認する。

* 問題No.: 6
    * 変数名と値: LB.LBTESTCD=CA, LB.LBNRIND=LOW, LBORRES=8.3 mg/dL (WEEK 20)
    * 矛盾の内容: カルシウム (CA) 検査値が基準範囲下限 (LBORNRLO=8.4 mg/dL) を下回っている (LBORRES=8.3 mg/dL)。
    * 問題点の原因（推測）: 患者のカルシウム代謝異常、またはデータ入力時の誤りの可能性。
    * 対応策（提案）: 医療機関にLBドメインのカルシウム値が低い理由を確認し、臨床的に問題がないか確認する。

* 問題No.: 7
    * 変数名と値: DS.DTHDTC: null (1レコード), DM.DTHFL: null (1レコード)
    * 矛盾の内容: Disposition (DS) ドメインにおいて、患者ID 01-704-1010 の死亡日 (DTHDTC) が欠損しており、Demographicsデータ (DM) の死亡フラグ (DTHFL) も空欄となっている。
    * 問題点の原因（推測）: データ入力時の欠落、またはFinal Lab Visit (DSDECOD=FINAL LAB VISIT) 時点で死亡が確認されていなかった可能性。ただし、DSDECOD="WITHDRAWAL BY SUBJECT"のレコードも存在するため、データ矛盾の可能性も否定できない。
    * 対応策（提案）: 医療機関に問い合わせ、患者の転帰、特に死亡に関する情報を確認する。死亡日が未報告の場合は、死亡日を確認し、データ修正を依頼する。死亡していない場合は、DSドメインのデータ自体の見直しが必要となる可能性がある。

* 問題No.: 8
    * 変数名と値: SV.VISIT = UNSCHEDULED 9.2, SV.VISITDY = null
    * 矛盾の内容: 計画外のVisit(UNSCHEDULED 9.2)において、VISITDYがNullとなっている。Define.xml上はVISITDYは必須項目ではないため、データ形式としては問題ない。
    * 問題点の原因（推測）: 非計画的なVisitのため、VISITDYが設定されていない。
    * 対応策（提案）: データ上は形式的な問題はないものの、VISITDYは計画されたStudy Dayを記録する変数であるため、UNSCHEDULED VISITにVISITDYがNullで記録されていることがデータ仕様として意図されたものか、データ作成者に確認する。

クエリ:
* 患者ID: 01-704-1010
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: CM.CMDTC, CM.CMSTDTC (CMドメイン全般の日付関連変数)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 の併用薬 (CM) データについて、データ収集日 (CMDTC) が併用薬開始日 (CMSTDTC) より過去の日付となっている矛盾が複数レコードで見られます。データの信頼性に関わる重要な問題であるため、CMドメイン全般の日付情報の再確認と修正を最優先でお願いいたします。特に、各併用薬の開始日 (CMSTDTC) および終了日 (CMENDTC)、データ収集日 (CMDTC) が、記録と一致しているかご確認ください。
        * 判断理由: CMドメインの日付矛盾はデータ品質を根幹から揺るがす可能性があり、早急な修正が必要と判断されるため、臨床試験結果への影響度をCriticalとしました。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: DS.DTHDTC: null, DM.DTHFL: null
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 のDispositionデータ (DS) において、死亡日 (DTHDTC) が空欄となっております。患者様の転帰は死亡でしょうか。死亡の場合、死亡日をご教示ください。もし死亡されていない場合、DSドメインのデータに誤りがある可能性がありますので、データ全体の再確認をお願いいたします。
        * 判断理由: 患者の死亡は安全性評価における最重要事項であり、データ欠損は看過できないため、臨床試験結果への影響度をCriticalとしました。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=BILI, LBORRES=1.3mg/dL, LBNRIND=HIGH (WEEK 6, 9.2, 20)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 の臨床検査値データについて、ビリルビン (BILI) 値が複数回にわたり基準範囲上限を超過 (1.3 mg/dL) しています。肝機能障害の可能性も考慮し、臨床的な意義について医学的見解をご教示ください。また、関連する有害事象 (肝機能障害、黄疸など) の発現状況についても併せてご回答ください。
        * 判断理由: ビリルビン高値は肝機能障害を示唆し、患者の安全性に関わる可能性があるため、臨床試験結果への影響度をMajorとしました。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AEENDTC: null (複数レコード)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 の有害事象データ (AE) において、終了日 (AEENDTC) が空欄となっているレコードが複数件ございます。有害事象の転帰と経過を把握するため、各有害事象の終了日をご確認いただき、ご回答をお願いいたします。
        * 判断理由: 有害事象の終了日不明は、安全性評価に支障をきたす可能性があるため、臨床試験結果への影響度をMajorとしました。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=CA, LB.LBNRIND=LOW, LBORRES=8.3 mg/dL (WEEK 20)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 の臨床検査値データについて、カルシウム (CA) 値が基準範囲下限を下回っています。臨床的に問題ない可能性もありますが、念のため医学的妥当性について治験責任医師の見解をご確認ください。
        * 判断理由: カルシウム低値は臨床的に直ちに重篤な影響を及ぼす可能性は低いと考えられるものの、医学的妥当性の確認はデータレビューとして必要であるため、臨床試験結果への影響度をMinorとしました。

    * クエリNo.: 6
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC = null (多数レコード)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 の併用薬データにおいて、CMENDTC（併用薬終了日）がNullとなっているレコードが複数あります。データ品質向上のため、CMENDTCのデータをご提供いただけますでしょうか。
        * 判断理由: 併用薬終了日の欠損は、データ解釈や解析における精度を低下させる可能性があるため、臨床試験結果への影響度をMinorとしました。

    * クエリNo.: 7
        * 臨床試験結果への影響度合い: None
        * 変数名と値: SV.VISIT = UNSCHEDULED 9.2, SV.VISITDY = null
        * 医療機関への問い合わせ文面: 患者ID 01-704-1010 のSVドメイン、VISIT=UNSCHEDULED 9.2 のレコードについて、VISITDYがNullとなっています。計画外のUNSCHEDULED VISITではVISITDYはNullで記録するのが正しい仕様でしょうか。仕様について確認させてください。
        * 判断理由: データ仕様に関する確認であり、データ自体の臨床的な解釈や臨床試験結果に直接的な影響はないと考えられるため、臨床試験結果への影響度をNoneとしました。
## Task3: Protocol Deviation Review Results
患者ID: 01-704-1010
逸脱No.: 1
臨床試験結果への影響度合い: Major
変数名と値: LB.LBTESTCD=BILI, LBORRES=1.3 mg/dL (WEEK 6, UNSCHEDULED 9.2, WEEK 20)
逸脱内容: 被験者01-704-1010において、複数回（WEEK 6, UNSCHEDULED 9.2, WEEK 20）のBilirubin検査で基準範囲上限超過（1.3 mg/dL）。プロトコル除外基準 [27b] に抵触の可能性。
プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
判断理由: プロトコル除外基準にて総ビリルビン値の基準値超過が除外基準とされているため、逸脱の可能性あり。肝機能検査値異常は安全性評価に影響するため重大な逸脱と判断。

逸脱No.: 2
臨床試験結果への影響度合い: Major
変数名と値: LB.LBTESTCD=CA, LBORRES=8.3 mg/dL (WEEK 20)
逸脱内容: 被験者01-704-1010において、WEEK 20のCalcium検査で基準範囲下限を下回る値 (8.3 mg/dL) が確認。プロトコル除外基準 [27b] に抵触の可能性。
プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
判断理由: プロトコル除外基準にて血清カルシウム値の基準値未満が除外基準とされているため、逸脱の可能性あり。電解質検査値異常は安全性に影響するため重大な逸脱と判断。

逸脱No.: 3
臨床試験結果への影響度合い: Minor
変数名と値: VISIT = UNSCHEDULED 9.2
逸脱内容: プロトコルに規定されていないUNSCHEDULED 9.2 Visitが実施されている。評価スケジュール逸脱の可能性。
プロトコル該当箇所: プロトコルの評価スケジュールに関するセクション
判断理由: プロトコルで計画されたVisitスケジュール以外にVisitが実施されており、評価スケジュールからの逸脱の可能性があるため。

患者ID: 01-704-1010
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=BILI, LB.LBORRES=1.3 mg/dL, LB.LBTESTCD=CA, LBORRES=8.3 mg/dL, DM.AGE, DM.SEX, MH.MHTERM, MMSEスコア, Modified Hachinski Ischemic Scale スコア, CNSイメージング実施と結果
        医療機関への問い合わせ文面:
        被験者01-704-1010の選択基準充足状況と臨床検査値について、以下の点をご確認ください。
        1. 組み入れ基準 MMSE スコア (10〜23) を満たしていますか？ スコアと評価日をご教示ください。
        2. 組み入れ基準 Modified Hachinski Ischemic Scale スコア (≤ 4) を満たしているか、スコアと評価日をご教示ください。
        3. 組み入れ基準 CNSイメージング (CT スキャンまたは MRI) は実施され、ADと互換性があると判断されていますか？ 実施日、判断日、判断医師をご教示ください。
        4. Bilirubin値1.3 mg/dL (WEEK 6, 9.2, 11) および Calcium値8.3 mg/dL (WEEK 20) は、データ入力誤りではないでしょうか？ 臨床的に問題ないと判断されている場合、その理由をご教示ください。
        判断理由: プロトコル逸脱の可能性のあるBilirubinとCalciumの検査値異常、および組み入れ基準の充足状況について、治験担当医師に確認が必要なため。

    クエリNo.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: VISIT = UNSCHEDULED 9.2
        医療機関への問い合わせ文面:
        患者ID 01-704-1010 で記録されている UNSCHEDULED 9.2 のVisitについて、以下の点をご確認ください。
        1. UNSCHEDULED 9.2 Visit は、プロトコルで計画されたVisitスケジュールに含まれていますか？
        2. 計画外のVisitである場合、実施された理由と、取得データが臨床試験評価項目に与える影響についてご説明ください。
        判断理由: 計画外のUNSCHEDULED 9.2 Visitの実施理由と臨床試験への影響を評価するため、医療機関への確認が必要なため。

    クエリNo.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMDECOD = CIPRO
        医療機関への問い合わせ文面:
        併用薬CIPROはプロトコルで併用禁忌に指定されていますか？
        1. 併用薬CIPROは、プロトコル3.4.2.2項 (除外基準) または 3.8項 (併用療法) に記載されている併用禁止薬に該当しないかご確認ください。
        2. 併用が許可されている場合、その理由と根拠をご教示ください。
        3. 併用が禁止されている場合、投与期間と臨床試験への影響についてご評価ください。
        判断理由: 併用薬CIPROがプロトコルで禁止されている薬剤に該当するか不明なため、医療機関に確認し、プロトコル逸脱の有無と臨床試験への影響を評価する必要があるため。

# 01-701-1015
## Task1: Clinical Review Results
**症例サマリー:**

患者ID: 01-701-1015
* 2013年12月26日 (Day -7): スクリーニング1回目の検査にて、ALP（アルカリホスファターゼ）低値、Anisocytes（異形赤血球）異常高値、AST（アスパート酸アミノトランスフェラーゼ）高値が確認されました。
* 2014年01月16日 (Day 15): WEEK 2の検査にて、ALT（アラニンアミノトランスフェラーゼ）高値が確認されました。有害事象として、軽度の適用部位紅斑、適用部位そう痒症、下痢が報告されました。
* 2014年01月30日 (Day 29): WEEK 4の検査にて、MCV（平均赤血球容積）低値が確認されました。
* 2014年06月18日 (Day 168): WEEK 24の検査にて、MCV低値と尿比重低値が確認されました。

---

**クエリ:**

患者ID: 01-701-1015
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AESER = Y, AE.AEOUT = RECOVERED/RESOLVED, AE.AETERM = DIARRHOEA
    * 医療機関への問い合わせ文面: 下痢 (DIARRHOEA) がSerious Event (AESER = Y) と報告されていますが、重症度(AESEV)はMildであり、Outcome of Adverse Event (AEOUT) はRECOVERED/RESOLVEDと報告されています。Serious Eventと判断された理由、重症度と転帰の矛盾について確認させてください。
    * 判断理由: 下痢がSerious Eventとして報告されている理由は不明であり、データの正確性を確認する必要があるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMINDC, CM.CMSTDTC, CM.CMENDTC, CM.CMENDY, LB.LBTESTCD (ALP, ALT, AST, MCV, SPGRAV, ANISO), LB.LBORRESU (ANISO, SPGRAV, COLOR, KETONES, PH, UROBIL), LB.LBSTRESC

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMTRT = ASPIRIN, TYLENOL, CALCIUM, PREMARIN, HYDROCORTISONE, NEOSPORIN /USA/, CMINDC = PROPHYLAXIS OR NON-THERAPEUTIC USE, 空欄
    * 矛盾の内容: CM.CMTRTに記録された複数の併用薬について、CMINDC (投与目的) がPROPHYLAXIS OR NON-THERAPEUTIC USE（予防または非治療的使用）または空欄となっており、具体的なindicationが不明です。特にASPIRIN、TYLENOLについてはMHドメインに既往歴の記載がなく、医学的な妥当性の確認が必要です。
    * 問題点の原因（推測）: データ入力時のindication記録漏れ、または不十分な記録。
    * 対応策（提案）: 医療機関にCM.CMTRT = ASPIRIN, TYLENOL, CALCIUM, PREMARIN, HYDROCORTISONE, NEOSPORIN /USA/ の具体的な投与目的（Indication）の詳細を確認するためのクエリを発行し、回答に基づき医学的妥当性を評価してください。

* 問題No.: 2
    * 変数名と値: CM.CMSTDTC = 2003, 2006 (複数レコード)
    * 矛盾の内容: CMドメインの複数のレコードにおいて、併用薬開始日 (CMSTDTC) の年が2003年、2006年と記録されており、データ収集日 (CMDTC) (2013-12-26以降) との乖離が大きいです。CMSTDTCの値が日付として不適切である可能性があります。
    * 問題点の原因（推測）: データ入力時の年号誤り、または日付フォーマットの誤認識。
    * 対応策（提案）: 医療機関にCM.CMSTDTCの正しい日付を確認し、データ修正が必要です。

* 問題No.: 3
    * 変数名と値: LB.LBTESTCD = ALP, LB.LBORRES = 34 (SCREENING 1) など、LB.LBTESTCD = AST, ALT, MCV, SPGRAV, ANISO で基準値外れ
    * 矛盾の内容: Laboratory Tests Results (LB) ドメインにおいて、複数の検査項目 (ALP, ALT, AST, MCV, SPGRAV, ANISO) で基準範囲外の値 (LOW, HIGH, ABNORMAL) が検出されました。
    * 問題点の原因（推測）: 患者の基礎疾患または状態による異常値、データ入力時の誤り、測定機器のエラーなどが考えられます。
    * 対応策（提案）: 医療機関に対し、LBドメインで基準値外れとなっている検査値について、以下の点を確認するクエリを発行してください。
        1.  各検査値の異常値は、医学的にSignificantな異常値と判断されるか？
        2.  基準値外れの原因として考えられる医学的な理由はあるか？
        3.  ALP, ALT, AST高値に関して、AEドメインに関連する有害事象の報告はあるか？
        4.  SPGRAV低値について、臨床的にSignificantな異常値と判断されるか？
        5.  MCV低値について、臨床的にSignificantな異常値と判断されるか？
        6.  ANISO異常値について、臨床的にSignificantな異常値と判断されるか？
        医療機関からの回答に基づき、データの修正、医学的解釈の追記、または追加のデータ収集などの対応を検討してください。

* 問題No.: 4
    * 変数名と値: LB.LBORRESU = "NO UNITS" (ANISO, SPGRAV, COLOR, KETONES, PH, UROBIL)
    * 矛盾の内容: LBドメインの一部の検査項目でオリジナル単位 (LBORRESU) が "NO UNITS" となっています。単位が欠損していることで、検査値の解釈に影響が出る可能性があります。
    * 問題点の原因（推測）: データ入力時の単位選択漏れ、Define.xmlの単位定義の不備などが考えられます。
    * 対応策（提案）: 医療機関にLBドメインのANISO, SPGRAV, COLOR, KETONES, PH, UROBILの正しい単位情報を確認し、データ修正が必要です。Define.xmlに単位定義が不足している場合は、Define.xmlの修正も検討してください。

* 問題No.: 5
    * 変数名と値: CM.CMENDTC = null, CM.CMENDY = null (複数レコード)
    * 矛盾の内容: CMドメインの複数レコードで併用薬終了日 (CMENDTC) と併用薬終了時Study Day (CMENDY) が欠損値となっています。併用薬の使用状況を正確に把握する上で、終了日の情報は重要です。
    * 問題点の原因（推測）: 併用薬が継続中のため未入力、データ入力時の未入力、または情報収集の不足が考えられます。
    * 対応策（提案）: 医療機関にCMドメインのCMENDTCとCMENDYが欠損しているレコードについて、併用薬の投与状況を確認し、終了日が不明な場合は、併用薬が継続中なのか、すでに終了している場合は終了日を特定し、データ補完を検討してください。

* 問題No.: 6
    * 変数名と値: LB.LBSTRESCとLB.LBSTRESNに同じ値 (複数レコード)
    * 矛盾の内容: LBドメインの複数のレコードで、標準結果（文字）(LBSTRESC) と標準結果（数値）(LBSTRESN) の両方に同じ値が記録されています。SDTMの仕様上、LBSTRESCとLBSTRESNは相互排他的に使用されるべきであり、両方に値が存在するのは不適切です。
    * 問題点の原因（推測）: データ入力システムの設定ミス、またはデータハンドリングの誤りが考えられます。
    * 対応策（提案）: Define.xmlを確認し、LBSTRESCとLBSTRESNのどちらの変数を使用すべきか定義を確認してください。Define.xmlの定義に従い、不適切な変数のデータを削除するなどのデータクリーニングを実施してください。Define.xmlの修正が必要な場合は、修正を検討してください。

クエリ:
患者ID: 01-701-1015
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: CM.CMSTDTC = 2003
    * 医療機関への問い合わせ文面: 患者ID 01-701-1015 の Concomitant Medication (CM) ドメインの CMSTDTC に '2003' という不正な日付が記録されています。CMTRT=ASPIRIN, TYLENOL, CALCIUM, PREMARIN, HYDROCORTISONE, NEOSPORIN /USA/  のCMSTDTC の正しい日付をご教示ください。
    * 判断理由: CM開始日が不正な日付のため、併用薬の投与期間の評価に影響を及ぼし、データの信頼性を損なう可能性があります。臨床試験全体の解釈に影響を与える可能性があるため、Criticalと判断しました。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMTRT = ASPIRIN, TYLENOL, CALCIUM, PREMARIN, HYDROCORTISONE, NEOSPORIN /USA/, CM.CMINDC = 空欄, PROPHYLAXIS OR NON-THERAPEUTIC USE
    * 医療機関への問い合わせ文面: 患者ID 01-701-1015 の 併用薬 ASPIRIN, TYLENOL, CALCIUM, PREMARIN, HYDROCORTISONE, NEOSPORIN /USA/ の投与目的（Indication）の詳細について確認させてください。特に、併用薬 ASPIRIN, TYLENOL については、Medical History (MH) ドメインに既往歴の記載が確認できませんでした。これらの併用薬の投与目的と、既往歴との関連性についてご教示ください。
    * 判断理由: 併用薬の投与目的が不明な場合、患者の安全性や臨床試験結果の解釈に影響を与える可能性があります。特に既往歴との関連性が不明なASPIRIN、TYLENOLについては、早急な確認が必要です。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD = ALP, AST, ALT, MCV, SPGRAV, ANISO, LB.LBORRES
    * 医療機関への問い合わせ文面: 患者ID 01-701-1015 の Laboratory Tests Results (LB) ドメインにおいて、複数の検査項目で基準範囲外の値が検出されました。
        1.  ALP低値 (SCREENING 1): 医学的にSignificantな異常値と判断されますか？
        2.  ALT高値 (WEEK 2): 医学的にSignificantな異常値と判断されますか？また、関連する有害事象は報告されていますか？
        3.  AST高値 (SCREENING 1): 医学的にSignificantな異常値と判断されますか？また、関連する有害事象は報告されていますか？
        4.  MCV低値 (WEEK 4, WEEK 16): 医学的にSignificantな異常値と判断されますか？
        5.  SPGRAV低値 (WEEK 24): 医学的にSignificantな異常値と判断されますか？
        6.  ANISO異常値 (SCREENING 1): 医学的にSignificantな異常値と判断されますか？
        各検査値の基準範囲外れについて、医学的見解と対応方針をご教示ください。
    * 判断理由: 複数の臨床検査値で基準範囲外れが確認されており、患者の安全性に関わる可能性があるため、医療機関への確認が必要です。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBORRESU = "NO UNITS" (ANISO, SPGRAV, COLOR, KETONES, PH, UROBIL)
    * 医療機関への問い合わせ文面: 患者ID 01-701-1015 の Laboratory Tests Results (LB) ドメインにおいて、一部検査項目のオリジナル単位 (LBORRESU) が "NO UNITS" となっています。ANISO, SPGRAV, COLOR, KETONES, PH, UROBIL の正しい単位情報をご教示ください。
    * 判断理由: 単位欠損はデータの解釈を困難にする可能性がありますが、臨床的な重大な影響は低いと考えられるため、影響度合いはMinorとしました。

* クエリNo.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMENDTC = null, CM.CMENDY = null
    * 医療機関への問い合わせ文面: 患者ID 01-701-1015 の 併用薬データについて、併用薬終了日 (CMENDTC) と 併用薬終了時Study Day (CMENDY) が欠損しているレコードが複数存在します。CMTRT=ASPIRIN, CALCIUM, HYDROCORTISONE, NEOSPORIN /USA/, PREMARIN のCMENDTC, CMENDYについて、可能な範囲で情報をご提供ください。併用薬が継続中の場合は、その旨お知らせください。
    * 判断理由: 併用薬の終了日が不明な場合、併用薬の使用状況の把握が不完全になる可能性がありますが、臨床的な重大な影響は低いと考えられるため、影響度合いはMinorとしました。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1015
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DM.AGE, DM.SEX, DM.RACE, DM.ETHNIC, MH.MHTERM, QS.QSTESTCD, LB.LBTESTCD=AST, LB.LBORRES=40 U/L (SCREENING 1), LB.LBTESTCD=ALT, LB.LBORRES=41 U/L, LB.LBSTNRHI=34 U/L, LB.LBNRIND=HIGH, LB.LBTESTCD=ALB, VISITNUM=10, VISITDY=126, QS.MMSE
        逸脱内容:
            * 選択基準 INCL03, INCL04, INCL05 のMMSEスコア、Modified Hachinski Ischemic Scale score、CNS imaging (CT scan or MRI of brain) のデータがJSONデータから確認できません。
            * 除外基準 EXCL14, EXCL17 に抵触するMedical Historyの疑い（ALZHEIMER'S DISEASE, PALPITATIONS）。
            * スクリーニング検査（VISITNUM=1）において、AST（アスパート酸アミノトランスフェラーゼ）値が基準値上限を超過。
            * WEEK 2 (VISITNUM=4) におけるアラニンアミノトランスフェラーゼ (ALT) が基準上限値を超過 (41 U/L, 基準上限値: 34 U/L)。
            * 臨床検査(Albumin)の実施日が、計画されたVisit Day(WEEK 16, VISITDY=112)から14日遅延。
        プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [3], [4], [5], 3.4.2.2. Exclusion Criteria [14], [17], [27b], 3.9. Efficacy, Pharmacokinetic, and Safety Evaluations, Protocol Attachment LZZT.1. Schedule of Events for Protocol H2Q-MC-LZZT(c)
        判断理由: 選択/除外基準の充足性をデータから判断できず、複数のプロトコル逸脱の疑いがあるため。

    クエリNo.: 1
        臨床試験結果への影響度合い: Critical
        変数名と値: TI.INCL03, TI.INCL04, TI.INCL05, TI.EXCL14, TI.EXCL17, LB.LBTESTCD=AST, LB.LBORRES=40 U/L (SCREENING 1), LB.LBTESTCD=ALT, LB.LBORRES=41 U/L, LB.LBSTNRHI=34 U/L, LB.LBNRIND=HIGH, QS.MMSE
        医療機関への問い合わせ文面:
            被験者01-701-1015の選択/除外基準および臨床検査値について、以下の点をご確認ください。
            1. スクリーニング時MMSEスコアはプロトコルで規定された選択基準（MMSEスコア10〜23）を満たしていましたでしょうか。
            2. Modified Hachinski Ischemic Scale scoreは4以下でしたでしょうか。
            3. CNS imaging（CTスキャンまたはMRI）はADと互換性がありましたでしょうか。
            4. Medical HistoryにあるALZHEIMER'S DISEASE、PALPITATIONSは、プロトコルで規定された除外基準 (精神疾患の既往歴、重篤な心血管障害の既往歴) に抵触しないと医学的に判断されましたでしょうか。
            5. スクリーニング1におけるAST値が基準値上限を超過していますが、組み入れ基準を満たすと判断された医学的な理由についてご説明ください。また、Lilly Reference Range III におけるASTの基準上限値をご教示ください。
            6. WEEK 2 (VISITNUM=4) におけるアラニンアミノトランスフェラーゼ (ALT) が基準上限値を超過 (41 U/L, 基準上限値: 34 U/L) していますが、臨床的に問題ないと判断されましたでしょうか。判断された場合、医学的な理由をご説明ください。
        判断理由: 
            * 選択/除外基準および臨床検査値に関する複数の疑義事項があり、データの医学的妥当性、プロトコル

# 01-701-1111
## Task1: Clinical Review Results
患者ID: 01-701-1111
* 2012年08月25日 (Day -13): スクリーニング1回目の検査にて、尿検査で比重が低い (SPGRAV LOW)。血液検査では赤血球数も低い (RBC LOW)。
* 2012年09月02日 (Day -5): 軽度の紅斑 (ERYTHEMA MILD) および掻痒 (PRURITUS MILD) を発症。
* 2012年09月04日 (Day -3): 局所感染症 (LOCALISED INFECTION MODERATE) 発症。
* 2012年09月05日 (Day -2): スクリーニング2回目のバイタルサイン測定時、DIABP (拡張期血圧) が低い (60 mmHg)。
* 2012年09月07日 (Day 1): ベースライン来院、治験薬投与開始。尿意切迫 (MICTURITION URGENCY MILD) 発症。
* 2012年09月13日 (Day 7): 関節痛 (ARTHRALGIA MODERATE) および蜂巣炎 (CELLULITIS MODERATE) を発症。
* 2012年09月17日 (Day 11): Week 2来院。血液検査にて平均赤血球容積 (MCV HIGH) が基準範囲上限超え、異型リンパ球 (ANISO ABNORMAL) が認められる。尿検査で尿比重が基準範囲下限を下回る (SPGRAV LOW)。治験薬投与中止、治験中止 (ADVERSE EVENT)。

---
患者ID: 01-701-1111
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AETERM = LOCALISED INFECTION, AE.AESTDY = -61
    * 医療機関への問い合わせ文面: 有害事象「LOCALISED INFECTION」の開始日が治験薬投与開始日より前（-61日）ですが、治験薬との因果関係、プロトコルで規定された有害事象報告の対象となるかについてご教示ください。
    * 判断理由: LOCALISED INFECTIONが治験薬投与前から存在する場合、治験薬との因果関係がない可能性があり、安全性評価に影響を与える可能性があるため。
* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD = MCV, RBC, SPGRAV, ANISO, VISIT = WEEK 2, LBNRIND = HIGH (MCV), LOW (RBC, SPGRAV), ABNORMAL (ANISO)
    * 医療機関への問い合わせ文面: WEEK 2の検査値において、MCV高値、RBC低値、SPGRAV低値、ANISO ABNORMALが認められます。これらの検査値異常の原因、患者の臨床状態、プロトコルで規定された除外基準に抵触しないかについてご教示ください。
    * 判断理由: 検査値異常は、患者の安全性に関わる可能性があり、また、プロトコル逸脱に該当する可能性があるため。
* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMENDTC (空欄)
    * 医療機関への問い合わせ文面: 併用薬ドメイン (CM) において、CMENDTC が空欄となっているデータが複数あります。これらは継続中の併用薬であると考えられますが、データマネジメント上、CMENDTC には終了日または未終了を示すコード等の入力が必要です。CMENDTC の取り扱いについて、データセンターの方針をご確認ください。
    * 判断理由: CMENDTC が空欄のままでは、併用薬の投与期間が不明確となり、データの完全性および解析の正確性に影響を及ぼす可能性があるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, AE.AEENDTC, CM.CMSTDTC, CM.CMENDTC, CM.CMINDC, CM.CMDOSU, LB.MCV, LB.LBNRIND, VS.VSORRES, DS.DSTERM

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC (2012-09-02), EX.EXSTDTC (2012-09-07) (AEレコード1, 2, 3, 4, 5, 7, 8)
    * 矛盾の内容: 複数の有害事象 (ARTHRALGIA, CELLULITIS, ERYTHEMA, PRURITUS, LOCALISED INFECTION, MICTURITION URGENCY) の開始日が、治験薬投与開始日よりも先行している。治験薬との因果関係を評価する上で矛盾が生じる可能性、またはデータ入力誤りの可能性がある。
    * 問題点の原因（推測）: データ入力時の日付誤り、または有害事象開始日の記録誤りの可能性。
    * 対応策（提案）: 医療機関に原資料を確認し、AE開始日と治験薬投与開始日の矛盾についてデータ修正の要否を確認する。

* 問題No.: 2
    * 変数名と値: CM.CMSTDTC, CM.CMENDTC (19xx, 2006年)
    * 矛盾の内容: 複数の併用薬 (CMドメイン) の開始日 (CM.CMSTDTC) および終了日 (CM.CMENDTC) に、データ収集期間 (2012-2013年) と比較して過去すぎる日付 (19xx年、2006年) が記録されている。データ入力時の誤り、または長期にわたる併用薬の使用状況の記録の可能性がある。CM.CMENDTC が null のレコードも存在し、併用薬の継続状況が不明。
    * 問題点の原因（推測）: データ入力時の年号誤り、長期継続の併用薬、CMENDTC の記録漏れの可能性。
    * 対応策（提案）: 医療機関にCM開始日と終了日の記録が正しいか確認し、データ修正の要否を確認する。CMENDTC が null のレコードについては、併用薬が継続中か終了しているか確認し、必要に応じてデータ追記を依頼する。

* 問題No.: 3
    * 変数名と値: CM.CMINDC (null)
    * 矛盾の内容: 全ての併用薬レコードで投与目的 (CMINDC) が欠損している。併用薬の臨床的な意義を評価する上で情報が不足している。
    * 問題点の原因（推測）: データ入力時の欠落、データ収集時の未収集、または必須項目としての認識不足。
    * 対応策（提案）: 医療機関に CMINDC の欠損理由を確認し、可能な場合はデータ追記を依頼する。Define.xml に CMINDC を必須項目として定義することを検討する。

* 問題No.: 4
    * 変数名と値: CM.CMDOSU ("VIAL", "TABLET"), CM.CMDOSE (0.075, 0.625, 2.5), Define.xml (CM.CMDOSE dataType="integer")
    * 矛盾の内容: CM.CMDOSU に用量単位として不適切な剤形 ("VIAL", "TABLET") が記録されているレコード、CM.CMDOSE に Define.xml の定義 (integer) と異なる小数値が記録されているレコードが存在する。Define.xml の定義と実際のデータに不整合がある。
    * 問題点の原因（推測）: CM.CMDOSU はデータ入力時の選択肢誤り、CM.CMDOSE は Define.xml の定義誤り、またはデータ登録システムのデータ型チェックの不備。
    * 対応策（提案）: CM.CMDOSU のデータ入力値を修正する。Define.xml の CM.CMDOSE の dataType を decimal 型に変更する。データ登録システムのデータ型チェック設定を見直す。

* 問題No.: 5
    * 変数名と値: LB.MCV (101 fL), LB.LBSTNRHI (100 fL), LB.LBNRIND (LOW, HIGH)
    * 矛盾の内容: LB.MCV 値が基準範囲上限を超えている (HIGH)。RBC, SPGRAV が LOW (低値) を示すレコードも存在する。臨床検査値が基準範囲外であり、臨床的な意義の確認が必要。
    * 問題点の原因（推測）: 患者の病態による異常値、検査エラー、またはデータ入力時の誤りの可能性。
    * 対応策（提案）: 医療機関に LB.MCV, RBC, SPGRAV の値が臨床的に問題ないか確認し、医学的解釈と患者の状況に関する情報を収集する。必要に応じて再検査を実施する。

* 問題No.: 6
    * 変数名と値: VS.VSORRES ("062.3", "098.8")
    * 矛盾の内容: VS.HEIGHT, VS.TEMP の VSORRES 値が "0" で始まっている。数値データとして不適切であり、データ入力誤りの可能性がある。
    * 問題点の原因（推測）: データ入力時のタイプミス、データ処理システムの不具合。
    * 対応策（提案）: VS.VSORRES の値を修正する。データ入力システムのエラーチェック機能を強化する。

* 問題No.: 7
    * 変数名と値: AE.AEENDTC (null)
    * 矛盾の内容: 複数のAEレコードで AEENDTC (有害事象終了日) が欠損している。有害事象の転帰評価に影響する可能性。
    * 問題点の原因（推測）: データ入力時の未入力、有害事象が未回復/未軽快。
    * 対応策（提案）: AE終了日を確認し、記録漏れであれば追記、継続中の場合はその旨を記録する。

* 問題No.: 8
    * 変数名と値: DS.DSTERM (ADVERSE EVENT), DS.DSDECOD (ADVERSE EVENT)
    * 矛盾の内容: DS.DSTERM と DS.DSDECOD に同じ用語 (ADVERSE EVENT) が使用されており、DSTERM の詳細な記述が不足している。
    * 問題点の原因（推測）: DSTERM への詳細用語の記載漏れ、データ入力の不備。
    * 対応策（提案）: DSTERM に具体的な Disposition Event の内容を記載するように修正する。（例: Adverse event leading to discontinuation）。データ入力ガイダンスを修正する。

Define.xmlの修正候補:
* 項目名: CM.CMDOSE
    * 現状の定義: dataType="integer"
    * 修正案: dataType="decimal"

クエリ:
* 患者ID: 01-701-1111
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMINDC (全レコード空欄)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1111 の併用療法 (CMドメイン) データについて、投与目的 (CMINDC) が全レコードで欠損しています。各併用薬の投与目的について、可能な範囲でご教示いただけますでしょうか。
        * 判断理由: 併用薬の投与目的は、患者背景や治験薬との相互作用評価に重要な情報であり、臨床試験の解釈に影響を与える可能性があるため、重要度「Major」と判断しました。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC=2012-09-02, EX.EXSTDTC=2012-09-07 (AEレコード1, 2, 4, 7, 8), AE.AESTDTC=2012-07-08, EX.EXSTDTC=2012-09-07 (AEレコード3)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1111 の有害事象 (AEドメイン) データにおいて、複数の有害事象 (ERYTHEMA, PRURITUS, ARTHRALGIA, CELLULITIS, LOCALISED INFECTION) の開始日 (AESTDTC) が治験薬投与開始日 (EX.EXSTDTC) より早くなっています。データに矛盾がないか、各有害事象の開始日 (AESTDTC) が正しいか、原資料をご確認いただけますでしょうか。
        * 判断理由: 有害事象の開始日が治験薬投与開始日より早い場合、治験薬との因果関係評価に影響を与える重要な矛盾であるため、重要度「Major」と判断しました。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBNRIND=LOW (RBC, SPGRAV), LB.LBTESTCD=MCV, LB.LBNRIND=HIGH
        * 医療機関への問い合わせ文面: 患者ID 01-701-1111 の臨床検査値 (LBドメイン) データにおいて、RBC (赤血球数) および SPGRAV (尿比重) が LOW (低値)、MCV (平均赤血球容積) が HIGH (高値) と基準範囲外となっています。これらの検査値異常について、臨床的な意義と患者様の状態について、医学的なご見解をご教示いただけますでしょうか。
        * 判断理由: 基準範囲外の臨床検査値は、患者の安全性に関わる可能性があり、臨床試験の評価にも影響を与える可能性があるため、重要度「Major」と判断しました。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: VS.VSORRES="062.3" (HEIGHT), VS.VSORRES="098.8" (TEMP)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1111 のバイタルサイン (VSドメイン) データにおいて、身長 (HEIGHT) と体温 (TEMP) の VSORRES の値が "0" で始まっています。データ入力時の誤りの可能性がありますので、該当データが正しい値
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1111
    逸脱No.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: LB.LBTESTCD=MCV, LB.LBORRES=101, LB.LBORRESU=fL, VISIT=WEEK 2
    逸脱内容: 
        被験者01-701-1111のMCV（平均赤血球容積）値が101 fLであり、WEEK 2のVISITにおいて基準範囲上限を超過している可能性があります。プロトコルの除外基準EXCL27では、「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」が規定されており、MCVがこの除外基準に該当するかどうか、また、治験参加者のMCV値がLilly Reference Range IIIの基準範囲を超過しているか確認が必要です。
    プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
    判断理由: 
        報告された臨床検査データ（LBドメイン）において、治験参加者のMCV値が基準範囲上限を超過している可能性があります。プロトコルで規定された除外基準EXCL27に抵触するかどうかを確認するため、プロトコル逸脱として検出しました。選択基準INCL03（MMSEスコア10〜23）に関するMMSEスコアの欠損も、プロトコル遵守状況の観点から重要であり、合わせて確認が必要です。

    逸脱No.: 2
    臨床試験結果への影響度合い: Minor
    変数名と値: LB.LBTESTCD=RBC, LB.LBORRES=3.80 (SCREENING 1), 3.70 (WEEK 2), LB.LBORNRLO=3.9, LBNRIND=LOW
    逸脱内容: 
        被験者01-701-1111において、Laboratory Tests ResultsドメインのRBC（Erythrocytes）検査結果が、SCREENING 1およびWEEK 2のVISITにおいて基準値下限を下回っています。LBNRINDはLOWと判定されていますが、臨床的な意義が不明です。
    プロトコル該当箇所: プロトコルには具体的な基準値範囲の記載なし。Define.xmlにLB.LBORNRLO, LB.LBORNRHIの定義あり。プロトコル 3.4.2.2 除外基準 [27b]項、添付資料 LZZT.1 スケジュール
    判断理由: 
        RBC低値は基準値外れではあるものの、LBNRINDはLOWであり、臨床的な意義が不明です。プロトコル逸脱と断定するには情報が不足しているため、医療機関へのクエリで臨床的意義を確認する必要があると判断しました。

    逸脱No.: 3
    臨床試験結果への影響度合い: Major
    変数名と値: CMTRT=KEFLEX, CMSTDTC=2012-07-08
    逸脱内容: 
        被験者01-701-1111は、治験薬投与開始前61日から治験薬と併用してKEFLEXを服用しています。プロトコルで併用禁止薬の規定、または選択・除外基準に併用薬に関する規定がある場合、プロトコル逸脱に該当する可能性があります。
    プロトコル該当箇所: プロトコルの併用療法、選択・除外基準に関するセクション
    判断理由: 
        CMドメインのデータにおいて、KEFLEXのCMSTDTCが2012-07-08であり、DMドメインの治験薬初回投与日RFXSTDTC（2012-09-07）より61日前に開始されています。プロトコルに併用薬に関する規定があるかどうか確認が必要であるため、プロトコル逸脱の疑いとして検出しました。

    逸脱No.: 4
    臨床試験結果への影響度合い: Unknown
    変数名と値: AE.AEACN=(空欄)
    逸脱内容: 
        Adverse EventsドメインのAEACN（Action Taken with Study Treatment）がすべてのレコードで空欄となっています。Define.xmlには「AEACN=Null (data on action taken concerning study treatment was not collected)」とありますが、データ収集の意図が不明です。
    プロトコル該当箇所: Define.xml
    判断理由: 
        AEドメインのAEACN（Study Treatmentとの処置）変数が空欄となっている理由と、データ収集の意図を確認するため、プロトコル逸脱の疑いとして検出しました。

    逸脱No.: 5
    臨床試験結果への影響度合い: Major
    変数名と値: QS.MMITM01〜MMITM06, QS.ACTOT (欠損)
    逸脱内容: 
        被験者01-701-1111のMMSEスコアがデータに含まれていません。プロトコルで規定された選択基準INCL03（MMSEスコア10〜23）を満たしているか確認が必要です。
    プロトコル該当箇所: 3.4.2.1. 選択基準 [3]
    判断理由: 
        選択基準INCL03では、MMSEスコアが10〜23であることが求められていますが、提供されたJSONデータにはMMSEスコアの合計値がQSドメインに含まれていません。MMSEスコアが選択基準を満たしているか確認する必要があります。

    クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: LB.LBTESTCD=MCV, LB.LBORRES=101, LB.LBORRESU=fL, VISIT=WEEK 2, LB.LBTESTCD=RBC, LB.VISIT=WEEK 2, LB.LBNRIND=LOW, LBSTRESN=3.7, QS.MMITM01〜MMITM06, QS.ACTOT (欠損), CMTRT=KEFLEX, CMSTDTC=2012-07-08
    医療機関への問い合わせ文面: 
        治験参加者01-701-1111について、以下の点についてご回答ください。

        1.  WEEK 2の臨床検査データにおいて、MCV値が101 fLと基準範囲上限を超過しております。プロトコル除外基準EXCL27の「Laboratory test values exceeding the Lilly Reference Range III」にMCVが含まれるか、Lilly Reference Range IIIにおけるMCVの基準範囲をご教示ください。MCV高値が除外基準に該当する場合、治験参加者の組み入れの妥当性について再検討が必要となる可能性があります。

        2.  SCREENING 1およびWEEK 2のVISITでRBC（Erythrocytes）検査結果が基準値下限を下回っています。LBNRINDはLOWと判定されていますが、RBC低値の臨床的な意義についてご意見を伺えますでしょうか。プロトコルで規定された選択基準・除外基準に抵触するかどうかの判断と合わせてご回答をお願いいたします。RBC低値の原因、治験薬投与との関連性、実施された臨床的な対応、治験継続への影響についてもご教示ください。

        3.  併用薬KEFLEXについて、以下の点をご確認させてください。
            a.  KEFLEXはプロトコルで規定されている併用禁止薬に該当しますでしょうか。
            b.  選択・除外基準に併用薬に関する規定はありますでしょうか。
            c.  併用が許可されている場合、KEFLEXの投与開始日が治験薬投与開始前61日であることはプロトコル遵守状況に影響を与えますでしょうか。

        4.  MMSEスコア（MMSE合計点）をご提供ください。

    判断理由: 
        治験参加者01-701-1111のプロトコル遵守状況について、複数の懸念事項が検出されました。MCV高値、RBC低値、MMSEスコア欠損、併用薬KEFLEXの使用に関して、プロトコル逸脱の可能性や臨床的な疑義事項を確認するため、医療機関への問い合わせが必要と判断しました。

    クエリNo.: 2
    臨床試験結果への影響度合い: None
    変数名と値: AE.AEACN=(空欄)
    医療機関への問い合わせ文面:
        Adverse EventsドメインのAEACN（Action Taken with Study Treatment）がすべてのレコードで空欄となっています。Define.xmlには「AEACN=Null (data on action taken concerning study treatment was not collected)」とありますが、AEACNを空欄でデータ提出することが本試験のデータマネジメント計画書（DMP）で意図されている運用で間違いないでしょうか。
    判断理由: AEドメインのAEACN変数が空欄である理由について、データマネジメント上の意図を確認するため。

# 01-703-1299
## Task1: Clinical Review Results
**患者ID:** 01-703-1299
* 2012年09月28日 (Day 17): 検査値でアルブミン低下 (3.4 g/dL、基準値: 3.5-4.6 g/dL) が認められました (LOWと判定)。
* 2012年09月27日 (Day 16) - 2012年10月06日 (Day 25): 有害事象として上気道感染症が発現しました (軽度、未回復)。
* 2012年12月05日 (Day 85): 検査値でナトリウム低下 (134 mEq/L、基準値: 135-145 mEq/L) が認められました。
* 2013年03月01日 (Day 171): 有害事象として低血圧 (軽度) が発現し、2013年3月13日まで未回復です。
* 2013年03月01日 (Day 171): 有害事象として頻脈 (軽度) が発現し、2013年3月13日まで未回復です。
* 2013年03月01日 (Day 171): 有害事象として緑内障が悪化し、中等度であり、1992年から継続、2013年3月13日まで未回復です。
* 2013年03月13日 (Day 183): 有害事象として低血圧 (中等度) が発現し、2013年3月13日まで未回復です。
* 2013年03月13日 (Day 183): 有害事象として頻脈 (中等度) が発現し、2013年3月13日まで未回復です。
* 2013年03月13日 (Day 183): 有害事象として心筋梗塞 (中等度) が発現し、2013年3月13日まで未回復です。

---
**患者ID:** 01-703-1299
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AETERM = MYOCARDIAL INFARCTION, AE.AESEV = MODERATE, AE.AESTDTC = 2013-03-13
    * 医療機関への問い合わせ文面: 患者ID: 01-703-1299 に心筋梗塞 (中等度) の有害事象が報告されています。発症日、詳細な症状、治験薬との因果関係、患者の転帰についてご教示ください。
    * 判断理由: 心筋梗塞は重篤な有害事象であり、患者の安全性に直接影響を与える可能性があります。治験薬との因果関係によっては、臨床試験の継続に影響を及ぼす可能性があります。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AETERM = HYPOTENSION, AE.AESEV = MODERATE, AE.AESTDTC = 2013-03-01, AE.AETERM = TACHYCARDIA, AE.AESEV = MODERATE, AE.AESTDTC = 2013-03-01, CM.CMTRT = TIMOPTIC
    * 医療機関への問い合わせ文面: 患者ID: 01-703-1299 では、2013年3月1日と2013年3月13日にかけて、中等度の低血圧と頻脈が継続して発現しています。併用薬TIMOPTIC (チモロール) はβ遮断薬であり、これらの有害事象との関連が疑われます。併用状況、投与量、投与期間、有害事象発症日時の詳細、TIMOPTIC継続の必要性についてご教示ください。
    * 判断理由: 中等度の低血圧と頻脈が継続していることは、患者の安全性において懸念事項です。併用薬TIMOPTICとの関連性を確認し、治験薬との相互作用や患者への影響を評価する必要があります。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LBTESTCD = ALB, VISIT = WEEK 2, LBSTRESC = 34, LBNRIND = LOW
    * 医療機関への問い合わせ文面: 患者ID: 01-703-1299 のWeek 2のアルブミン値が基準範囲を下回っています。臨床的に問題となる可能性は低いと考えられますが、念のため、アルブミン低下の原因について、治験担当医師の見解をご確認ください。
    * 判断理由: Week 2でアルブミンが基準値下限をわずかに下回っていますが、その他の検査値は正常範囲内であり、臨床的に重大な懸念事項ではありません。ただし、治験プロトコルや脱落基準に抵触するかどうかの確認のため、治験担当医師に確認することが望ましいと判断しました。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM = HYPOTENSION (軽度), AE.AESTDTC = 2013-03-01, AE.AEENDTC = "", AE.AETERM = TACHYCARDIA (軽度), AE.AESTDTC = 2013-03-01, AE.AEENDTC = ""
    * 医療機関への問い合わせ文面: 2013年3月1日に開始された軽度の低血圧と頻脈は、2013年3月13日の最終評価時まで転帰が「NOT RECOVERED/NOT RESOLVED」となっています。その後の状況について、治験担当医師にご確認ください。
    * 判断理由: 軽度の低血圧と頻脈が治験期間中に発現し、最終評価時まで未回復である点は安全性において懸念されます。患者の安全性確保のため、詳細な状況把握と適切な医学的判断が必要と考えられます。ただし、症状が軽度であり、臨床試験結果への影響は小さいと考えられるため、重要度をMinorとしました。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: クエリNo.1, クエリNo.2, クエリNo.3

問題点:
* 問題No.1:
    * 変数名と値: AE.AESTDTC = 1992-09-07 (AEレコードNo.1, 3), EX.EXSTDTC = 2012-09-12
    * 矛盾の内容: 
        * AEドメインの有害事象「GLAUCOMA」（AEレコードNo.1）および「UPPER RESPIRATORY TRACT INFECTION」（AEレコードNo.3）の開始日が1992年9月7日と記録されており、試験期間（2012年9月〜2013年3月）および治験薬投与開始日（EX.EXSTDTC: 2012-09-12）と大きく乖離している。
        * 時間軸の整合性から、有害事象の発現日が治験薬投与開始日より20年も前であることは不自然であり、データ入力時の誤りの可能性が高い。
    * 問題点の原因（推測）: データ入力ミス（年号の誤入力、日付の誤入力など）、または過去の病歴をAEドメインに誤って記録した可能性。
    * 対応策（提案）: 
        * クエリを発行し、医療機関にAE.AESTDTCの記録が正しいか確認する。
        * データ入力ミスの場合、正しい日付に修正を依頼する。
        * 患者の既往歴である場合、MHドメインへの移動を検討する。

* 問題No.2:
    * 変数名と値: CM.CMSTDTC = 1992
    * 矛盾の内容: CMドメインのCMSTDTC (併用薬開始日) が1992年となっており、試験期間 (2012年9月7日〜2013年3月13日) と矛盾。患者のDMドメイン (DM.RFSTDTC: 2012-09-12) からも併用薬開始日が試験開始前であるべきだが、1992年は過去過ぎて不自然。
    * 問題点の原因（推測）: データ入力時の誤り、年号の入力ミス
    * 対応策（提案）: 医療機関にCMSTDTCが1992年となっている理由を確認し、正しい開始日を特定する。

* 問題No.3:
    * 変数名と値: LB.LBORRES(ALB) = 3.4 g/dL, LB.LBNRIND = LOW, VISIT: WEEK 2
    * 矛盾の内容: 
        * LBドメインのAlbumin検査値が、Define.xmlに定義された基準範囲 (3.5 - 4.6 g/dL) を下回るLow値 (3.4 g/dL) である。
        * LBNRIND (Reference Range Indicator) が "LOW" となっており、Define.xmlの定義とデータは整合している。
        * 医学的にAlbumin値の軽度なLow値が臨床的に重要となるかは、他の検査値や患者の臨床状態と合わせて判断する必要がある。
    * 問題点の原因（推測）: データ入力時の誤り、または患者の臨床状態による検査値異常の可能性。
    * 対応策（提案）: 
        * データ入力ミスでないか、原資料（CRFなど）を確認する。
        * 医療機関にLB検査値異常値（Albumin Low）の医学的妥当性を確認するためのクエリを発行する。

クエリの作成:
* 患者ID: 01-703-1299
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC = 1992-09-07 (AEレコードNo.1, 3), EX.EXSTDTC = 2012-09-12
        * 医療機関への問い合わせ文面:
          治験実施医療機関担当者様

          治験課題名：CDISCPILOT01試験

          治験参加者ID：01-703-1299

          クリニカルデータマネージャーです。

          SDTMデータセットAEドメインのデータについてお問合せです。

          患者ID: 01-703-1299の有害事象「GLAUCOMA」（AEレコードNo.1）と「UPPER RESPIRATORY TRACT INFECTION」（AEレコードNo.3）の開始日（AE.AESTDTC）が1992年9月7日と記録されています。
          治験薬初回投与日(DM.RFXSTDTC)は2012年9月12日であり、有害事象開始日として20年も過去の日付が記録されているのは不自然です。

          つきましては、AE.AESTDTCに記録された日付1992年9月7日は正しい日付でしょうか？
          もしデータ入力誤りの場合、正しい日付をご教示いただけますでしょうか。

          お忙しいところ恐縮ですが、ご回答よろしくお願いいたします。

          クリニカルデータマネージャー
        * 判断理由:
            有害事象の発現日の誤りは、有害事象と治験薬の因果関係の評価を誤らせる可能性があり、データの信頼性に関わるため、重要度が高いと判断しました。

    * クエリNo.2:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC = 1992 (CMレコードNo.1)
        * 医療機関への問い合わせ文面:
          治験実施医療機関担当者様

          治験課題名：CDISCPILOT01試験

          治験参加者ID：01-703-1299

          クリニカルデータマネージャーです。

          SDTMデータセットCMドメインのデータについてお問合せです。

          患者ID 01-703-1299 の併用薬 (CMTRT=TIMOPTIC, CMSEQ=1) の開始日 (CMSTDTC) が1992年と記録されています。
          試験期間と開始日が大きく乖離しており、データ入力の誤りの可能性が高いと考えられます。

          CMSTDTCの正しい日付をご教示いただけますでしょうか。

          お忙しいところ恐縮ですが、ご回答よろしくお願いいたします。

          クリニカルデータマネージャー
        * 判断理由: 併用薬の開始日は、治験薬との相互作用や有害事象の評価に重要な情報であり、データの正確性を確認する必要があるため、重要度が高いと判断しました。

    * クエリNo.3:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBORRES(ALB) = 3.4 g/dL, LB.LBNRIND = LOW, VISIT: WEEK 2
        * 医療機関への問い合わせ文面:
          治験実施医療機関担当者様

          治験課題名：CDISCPILOT01試験

          治験参加者ID：01-703-1299

          クリニカルデータマネージャーです。

          SDTMデータセットLBドメインのデータについてお問合せです。

          患者ID: 01-703-1299のWEEK 2 (VISITNUM=4) のAlbumin (LBTESTCD=ALB) の検査値が基準範囲を下回るLow値 (3.4 g/dL) で報告されています。

          医学的に見て、このAlbumin Low値は臨床的に問題がない値であるという理解でよろしいでしょうか。
          治験責任医師の見解を伺いたく、ご回答をお願いいたします。

          お忙しいところ恐縮ですが、ご回答よろしくお願いいたします。

          クリニカルデータマネージャー
        * 判断理由:
          LBドメインのAlbumin検査値が基準範囲を下回っているものの、軽度なLow値であり、臨床的な影響はMinorであると判断しました。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1299
    *   逸脱No.: 1
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMTRT = TIMOPTIC
        *   逸脱内容: 併用薬TIMOPTICの使用。プロトコルに併用禁止薬に関する明確な記述がないため、現時点ではプロトコル逸脱と断定できませんが、緑内障治療薬であり臨床試験結果に影響を与える可能性があるため、プロトコル逸脱の疑義として検出します。
        *   プロトコル該当箇所: プロトコル 3.8 併用療法、3.4.2.2 除外基準 (詳細な規定はプロトコルに明記されていません)
        *   判断理由: プロトコルおよびDefine.xmlを確認しましたが、TIMOPTICの併用に関する明確な規定がないため、プロトコル逸脱と断定できません。しかし、TIMOPTICの使用が臨床試験結果に影響を与える可能性を考慮し、念のためMinor逸脱として検出しました。

    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMTRT = TIMOPTIC
        *   医療機関への問い合わせ文面:
            治験薬併用状況について確認させてください。

            被験者ID: 01-703-1299

            現在、併用薬としてTIMOPTIC（チモロール）が投与されていることを確認しました。
            TIMOPTICは緑内障治療薬ですが、本治験プロトコルにおいて、緑内障治療薬の併用は許可されていますでしょうか。
            また、TIMOPTICの使用が本臨床試験の結果に影響を与える可能性について、専門医のご意見を伺いたく存じます。

            ご回答いただけますようお願いいたします。
        *   判断理由: 併用薬TIMOPTICの使用がプロトコルで許可されているか不明な点、および臨床試験結果への影響の可能性を考慮し、医療機関への確認が必要と判断しました。

# 01-703-1096
## Task1: Clinical Review Results
患者ID: 01-703-1096
* 2012年12月05日 (Day -51): スクリーニング1回目の検査では、ヘマトクリット、ヘモグロビン、赤血球数、平均赤血球ヘモグロビン量、平均赤血球ヘモグロビン濃度、平均赤血球容積、白血球数、好塩基球数、好酸球数、リンパ球数、単球数、血小板数、アルブミン、アルカリホスファターゼ、アラニンアミノトランスフェラーゼ、アスパラギン酸アミノトランスフェラーゼ、総ビリルビン、尿素窒素、カルシウム、コレステロール、クレアチンキナーゼ、クロール、クレアチニン、γ-GTP、血糖、カリウム、リン、総蛋白、ナトリウム、尿酸、甲状腺刺激ホルモン、尿比重、pH (尿) が基準範囲内でしたが、多くの項目で基準範囲の下限または上限に近い値が観察されました。
* 2012年12月19日 (Day -37): スクリーニング1回目の診察時に、既往歴として聴覚低下（軽度）とアルツハイマー病が確認されました。また、この日の検査で好塩基球数、ヘマトクリット、ヘモグロビン、リンパ球数、平均赤血球ヘモグロビン量、平均赤血球ヘモグロビン濃度、平均赤血球容積、単球数、血小板数、赤血球数が正常範囲内であることを再確認しました。
* 2012年12月29日 (Day -27): ビタミンB12の検査値が基準値範囲内であり、前回値よりも増加していることが確認されました。
* 2013年01月23日 (Day -2): スクリーニング2回目の検査では、白血球数がやや増加しましたが、その他の検査値は概ね正常範囲内でした。
* 2013年02月09日 (Day 16): 2週目の検査で、アルカリホスファターゼが 89 U/L と、正常範囲内ではあるもののベースラインからわずかに上昇しました。
* 2013年02月23日 (Day 30): 4週目の検査で、体重が 185.0 LB と、WEEK 2 (Day 16) の178.0 LBから増加しました。その他の検査値は正常範囲内でした。
* 2013年03月29日 (Day 64): WEEK 6の診察時に、患者は追跡不能となり、試験中止となりました。

---

患者ID: 01-703-1096
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: DM.AGE = 49
    * 医療機関への問い合わせ文面:
        * 患者ID 01-703-1096 のDM.AGE（年齢）が49歳と記録されていますが、プロトコルの組み入れ基準では50歳以上である必要があります。患者登録時の年齢について、医療機関に記録の確認を依頼します。もし組み入れ基準を満たしていない場合、プロトコル逸脱として取り扱うべきか、治験審査委員会（IRB）に諮る必要性を検討します。
    * 判断理由:
        * 患者の年齢がプロトコルで規定された組み入れ基準を満たしていない可能性があり、プロトコル逸脱に該当する疑いがあります。組み入れ基準の逸脱は、臨床試験の対象集団の適切性や試験結果の解釈に影響を与える可能性があるため、重要度の高いクエリとして対応します。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 要修正
* データクリーニング/再調査が必要な項目: DM.DMDTC, LB.LBDTCとLB.LBDYの整合性、AEドメイン、CMドメイン

問題点:
* 問題No.1:
    * 変数名と値: DM.DMDTC = 2012-12-19, DM.RFSTDTC = 2013-01-25
    * 矛盾の内容: DMドメインのDMDTC (データ収集日) が、DM.RFSTDTC (治験薬初回投与日) より過去の日付で記録されています。データ収集日が治験薬初回投与日より過去であることは、時間軸の整合性として不自然です。
    * 問題点の原因（推測）: データ入力時の誤り、またはDMDTCとRFSTDTCの日付の定義理解の誤りの可能性があります。
    * 対応策（提案）: DM.DMDTCの日付が正しいかどうか、原資料（症例報告書など）を確認し、必要であれば修正してください。

* 問題No.2:
    * 変数名と値: LB.LBDTC, LB.LBDY
    * 矛盾の内容: LB.LBDTC (2012-12-05T11:30) が LB.LBDY (-51) より前の日付になっている。LBDTCはSpecimen Collectionの日時、LBDYはSpecimen CollectionのStudy Dayを示す変数であり、LBDTCがLBDYより前の日付になるのは、定義上矛盾している。
    * 問題点の原因（推測）: データ入力時の誤り、またはStudy Dayの計算ロジックの誤り
    * 対応策（提案）: データ入力者にLBDTCとLBDYの整合性について確認し、必要に応じてデータ修正を行う。Study Dayの計算ロジックが正しいか、Define.xml、プロトコル、DMP等を確認する。

* 問題No.3:
    * 変数名と値: AEドメイン (データセット全体が空)
    * 矛盾の内容: AEドメインにレコードが1件も存在しない。Define.xmlにはAEドメインの定義が存在し、有害事象データの収集が意図されているにもかかわらず、データが全く記録されていない。
    * 問題点の原因（推測）: データ入力時のエラー、データ抽出/変換時のエラー、または意図的にデータが記録されなかった可能性（プロトコル逸脱）。
    * 対応策（提案）: AEドメインのデータが存在しない理由を調査し、データ入力/収集プロセスに問題がないか確認する。もしデータ入力漏れであれば、データの再入力が必要。

* 問題No.4:
    * 変数名と値: CMドメイン (データセット全体が空)
    * 矛盾の内容: CMドメインにレコードが1件も存在しない。Define.xmlにはCMドメインの定義が存在し、併用薬データの収集が意図されているにもかかわらず、データが全く記録されていない。
    * 問題点の原因（推測）: データ入力時のエラー、データ抽出/変換時のエラー、または意図的にデータが記録されなかった可能性（プロトコル逸脱）。
    * 対応策（提案）: CMドメインのデータが存在しない理由を調査し、データ入力/収集プロセスに問題がないか確認する。もしデータ入力漏れであれば、データの再入力が必要。

* 問題No.5:
    * 変数名と値: すべてのドメインのrecords=0（一部ドメインを除く）
    * 矛盾の内容: ほとんどのSDTMドメインでデータレコード数が0件であり、臨床試験データが不足している状態です。DM, DS, LB, QS, SV, VS, EX, SEドメインはデータレコードが存在しますが、AE, CM, RELREC, SUPPAE, SUPPDM, SUPPDS, SUPPLBドメインはデータレコードが0件です。TA, TE, TI, TS, TVドメインは参照データのため、データレコードが0件でも問題ありません。
    * 問題点の原因（推測）: データ抽出・作成時のエラー、またはデータ自体が未収集の可能性があります。特にSUPP**ドメインでデータレコードが0件であることは、SDTMデータ作成においてSupplemental Qualifierが未適用である可能性を示唆しています。
    * 対応策（提案）: データ作成部門にデータ再抽出・再作成を依頼し、データが未収集の場合はデータ収集プロセスを見直す必要があります。Supplemental Qualifierが意図的に適用されていない場合は、その理由を確認し、データレビュー計画書に記録することを推奨します。

クエリ:
* 患者ID: 01-703-1096
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DM.DMDTC = 2012-12-19, DM.RFSTDTC = 2013-01-25
        * 医療機関への問い合わせ文面: 患者ID 01-703-1096 のDMドメインにおいて、DMDTC (データ収集日) が RFSTDTC (治験薬初回投与日) より過去の日付で記録されています。DMDTC の日付が 2012-12-19 で正しいか、誤りであれば正しい日付をご教示ください。
        * 判断理由: データ収集日（DMDTC）が治験薬初回投与日（RFSTDTC）より過去になっていることは、データの時間軸における整合性違反の疑いがあり、データの信頼性を損なう可能性があります。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1096
    逸脱No.: 1
        臨床試験結果への影響度合い: Critical
        変数名と値: DM.AGE = 49
        逸脱内容: 被験者01-703-1096は、DMドメインの年齢が49歳であり、プロトコルで規定された選択基準（50歳以上の男性および閉経後の女性、INCL01）を満たしていません。選択基準違反は臨床試験の対象集団の適切性に関わる重大な逸脱であり、臨床試験結果の解釈に影響を与える可能性があります。
        プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [1]
        判断理由: DMドメインの年齢データがプロトコルの選択基準を満たしていないため、選択基準逸脱と判断しました。選択基準違反は臨床試験のvalidityを損なう可能性があります。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE
        逸脱内容: 被験者01-703-1096は、MHドメインに "ALZHEIMER'S DISEASE" の病歴があります。プロトコルの除外基準 (EXCL12) に「重篤な神経学的疾患の診断」が含まれており、アルツハイマー病がこれに該当する可能性があります。ただし、Medical Historyにある "ALZHEIMER'S DISEASE" が治験の主要評価項目であるアルツハイマー病と同一であるか、あるいは併存疾患であるか不明なため、プロトコル逸脱の疑いとして検出しました。除外基準違反は臨床試験の対象集団の適切性に関わる逸脱であり、臨床試験結果の解釈に影響を与える可能性があります。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [12]
        判断理由: MHドメインのデータとプロトコルの除外基準を比較した結果、病歴に関する基準に抵触する可能性があるため、プロトコル逸脱の疑いとして検出しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: DS.DSTERM = UNABLE TO CONTACT PATIENT (LOST TO FOLLOW-UP), DS.DSDECOD = LOST TO FOLLOW-UP, VISIT = WEEK 6
        逸脱内容: 被験者01-703-1096は、WEEK 6で追跡不能（LOST TO FOLLOW-UP）により治験薬投与を中止しました。プロトコルで規定された治験薬投与期間（26週間）を満了していません。ただし、DSドメインのデータから、治験薬投与中止の理由が追跡不能（LOST TO FOLLOW-UP）であり、プロトコルで許容されている治験薬投与中止の理由に該当する可能性があります。治験薬投与中止がプロトコル逸脱にあたるかどうかは、プロトコルの詳細な規定と、治験薬投与中止の理由の詳細な評価に基づいて判断する必要があります。
        プロトコル該当箇所: 3.1. Summary of Study Design, 3.10. Patient Disposition Criteria
        判断理由: 治験薬投与期間がプロトコル未達であるものの、追跡不能による中止はプロトコルで許容されている可能性があるため、Minorのプロトコル逸脱と判断しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.VISIT = UNSCHEDULED 1.3, VS.VISIT = AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL, QS.VISIT = WEEK 2, WEEK 4, SV.VISIT = UNSCHEDULED 1.1, UNSCHEDULED 1.2, UNSCHEDULED 1.3, AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL
        逸脱内容: LBドメイン、VSドメイン、QSドメイン、SVドメインに記録されているUNSCHEDULED 1.1, UNSCHEDULED 1.2, UNSCHEDULED 1.3, AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL, WEEK 2, WEEK 4のVISITが、TVドメイン（Trial Visits）に定義されていません。これらのVISITは、プロトコルで計画された評価スケジュールに含まれていない可能性があります。
        プロトコル該当箇所: 3.1. Summary of Study Design, Protocol Attachment LZZT.1. Schedule of Events for Protocol H2Q-MC-LZZT(c)
        判断理由: JSONデータに含まれる複数のVISIT名が、Define.xmlのTVドメインに定義されていないため、評価スケジュールからの逸脱、またはデータ入力時のVISIT名誤りの可能性があります。

クエリNo.: 1
    臨床試験結果への影響度合い: Critical
    変数名と値: DM.AGE = 49
    医療機関への問い合わせ文面:
    被験者01-703-1096のDMドメインにおける年齢が49歳と記録されています。プロトコルで規定されている選択基準では、50歳以上である必要があるとされています。被験者01-703-1096は選択基準を満たしているか、再度ご確認いただけますでしょうか。もし選択基準を満たしていない場合、登録の妥当性についてご説明ください。
    判断理由: 選択基準である年齢に関する疑義であり、回答によってはプロトコル逸脱となる可能性があるため、重要度「Critical」と判断しました。

クエリNo.: 2
    臨床試験結果への影響度合い: Major
    変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE
    医療機関への問い合わせ文面:
    被験者01-703-1096 のMHドメインにおいて、Medical History に "ALZHEIMER'S DISEASE" の記載があります。プロトコルでは重篤な神経学的疾患は除外基準とされていますが、Medical History に記載されたアルツハイマー病は、今回の治験における評価対象疾患と併存するMedical Historyなのか、あるいは過去の誤診の可能性や、治験登録基準を満たすアルツハイマー病とは別の疾患を指しているのか、詳細をご確認いただけますでしょうか。
    判断理由: 除外基準に抵触するMedical Historyの疑義があり、回答によってはプロトコル逸脱となる可能性があるため、重要度「Major」と判断しました。

クエリNo.: 3
    臨床試験結果への影響度合い: Major
    変数名と値: LB.VISIT = UNSCHEDULED 1.3, VS.VISIT = AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL, QS.VISIT = WEEK 2, WEEK 4, SV.VISIT = UNSCHEDULED 1.1, UNSCHEDULED 1.2, UNSCHEDULED 1.3, AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL
    医療機関への問い合わせ文面:
    LBドメイン、VSドメイン、QSドメイン、SVドメインに記録されているUNSCHEDULED 1.1, UNSCHEDULED 1.2, UNSCHEDULED 1.3, AMBUL ECG PLACEMENT, AMBUL ECG REMOVAL, WEEK 2, WEEK 4のVISITについて、プロトコルで計画されたVISITスケジュールとDefine.xmlのTVドメインに定義されているVISIT定義に整合性があるか確認してください。もし整合性がない場合、VISIT名が誤っている可能性があります。正しいVISIT名と、UNSCHEDULED VISITが実施された理由をご回答ください。
    判断理由: 評価スケジュール逸脱の疑義があり、回答によってはプロトコル逸脱となる可能性があるため、重要度「Major」と判断しました。

クエリNo.: 4
    臨床試験結果への影響度合い: Major
    変数名と値: CMドメイン, AEドメイン
    医療機関への問い合わせ文面:
    被験者01-703-1096のCMドメインとAEドメインのデータが空欄ですが、データ入力漏れの可能性はありますでしょうか。もしデータ入力漏れではなく、併用薬や有害事象がなかった場合、その理由と医学的妥当性についてご教示いただけますでしょうか。
    判断理由: CMドメインとAEドメインは、臨床試験において重要な安全性情報を記録するドメインであり、データが空欄であることの医学的妥当性を確認する必要があるため、医療機関への問い合わせが必要と判断しました。

# 01-701-1148
## Task1: Clinical Review Results
患者ID: 01-701-1148
* 2012年MM月DD日 (Day 不明): 消化不良 (中等度、未回復/未解決、関連性なし)
* 2013年07月29日 (Day -25): 気分沈滞 (中等度、未回復/未解決、関連性なし)
* 2013年08月25日 (Day 3): 適用部位紅斑 (軽度、未回復/未解決、可能性あり)、適用部位そう痒症 (軽度、未回復/未解決、可能性あり)
* 2013年10月12日 (Day 51): 下気道感染 (中等度、未回復/未解決、関連性なし)
* 2013年10月18日 (Day 57): 血液検査（EOS - 好酸球）で基準値上限超え (High)
* 2013年12月15日 (Day 115): 側腹部痛 (中等度、回復/解決、関連性なし)
* 2013年12月17日 (Day 117): 尿道結石 (中等度、回復/解決、関連性なし)
* 2014年01月03日 (Day 134): 鼻出血 (軽度、回復/解決、関連性なし)
* 2014年02月08日 (Day 170): 血液検査（EOS - 好酸球）で基準値上限超え (High)
* 2014年02月12日 (Day 174): 日光角化症 (軽度、未回復/未解決、関連性なし)

---
クエリなし
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMTRT, CM.CMDECOD, CM.CMENDTC, CM.CMENDY, CM.CMSTDTC, CM.CMDTC, AE.AESTDTC, AE.AEENDTC, AE.AEENDY, LB.LBNRIND, AEドメインとLBドメインの関連性

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMTRT, CM.CMDECOD (CMレコード No.1-23, 24-36)
    * 矛盾の内容: CM.CMTRT (併用薬名) に薬剤名が記録されているにもかかわらず、CMDECOD (標準化医薬品名) が "UNCODED" となっているレコードが多数存在する。特に、CIMETIDINE, FLUOROPLEX, HYDROCODONE W/APAP, NAPROXEN, SULFAMETHOXAZOLE, TUMS, TYLENOL で顕著である。
    * 問題点の原因（推測）: データ入力時のコーディング未実施、またはDefine.xmlやMedDRA辞書とのマッピング不備。
    * 対応策（提案）: CMDECOD に MedDRA 等の標準化辞書に基づいた医薬品コードを登録する。Define.xml および MedDRA辞書との整合性を確認し、必要に応じて修正する。医療機関へのクエリで未コード化となっている理由を確認する。

* 問題No.: 2
    * 変数名と値: CM.CMENDTC = "" (欠損), CM.CMENDY = null (CMレコード No.3, 5, 6, 7, 8, 11-24, 28, 32, 36), CM.CMENDTC = null (レコード3)
    * 矛盾の内容: CMドメインにおいて、CMENDTC (Medication End Date/Time) および CMENDY (Medication End Day) が欠損しているレコードが複数存在する。特に FLUOROPLEX (レコードNo.3) と TYLENOL (レコードNo.24-36) で欠損が目立つ。
    * 問題点の原因（推測）: データ入力時の欠落、または併用薬が継続中のため意図的に欠損させている可能性。
    * 対応策（提案）: 医療機関に CMENDTC および CMENDY の欠損理由を確認し、データ修正が必要か判断する。意図的な欠損の場合は、SDTM の QNAM/QVAL などの Qualifier 変数に欠損理由を記録することを検討する。

* 問題No.: 3
    * 変数名と値: CM.CMSTDTC, CM.CMDTC, CM.CMENDTC (CMレコード No.1, 2, 4, 9, 10, 19, 24, 28, 31, 32, 35, 36), AE.AESTDTC = 2013-12-17 (AE No.6), EX.EXSTDTC = 2013-08-23 (EX No.1), CM.CMSTDTC = "2011", "2006" (CMドメイン #11-#23, #24-#36), AE.AESTDTC = "2012-02" (AEドメイン #8)
    * 矛盾の内容:
        * 複数のCMレコードで、CMSTDTC、CMDTC、CMENDTCの日付に整合性の疑義がある。CMDTCがCMSTDTCやCMENDTCと大きく異なる日付になっている。特にCMレコード No.28, 31, 32 の CMENDTC は過去の年 (2006年、2011年) となっており、CMDTC (2013-08-14, 2014-02-08, 2014-02-20) との乖離が大きい。
        * AEレコード No.6 の AESTDTC (Adverse Event Start Date) が 2013-12-17 と EXレコード No.1 の EXSTDTC (Exposure Start Date) 2013-08-23 より後になっている。治験薬投与開始前に有害事象が発現するのは矛盾している。
        * CM.CMSTDTC および AE.AESTDTC が日付形式として不適切なデータ（年のみ、年月のみ）で入力されているレコードが存在する。
    * 問題点の原因（推測）: 日付データ入力時の誤り、または異なるイベントの日付の誤入力。CMENDTC の過去日付は年号の誤入力の可能性。
    * 対応策（提案）: CMSTDTC, CMDTC, CMENDTC, AE.AESTDTC の日付を原資料と照合し、データ入力エラーの場合は修正する。日付の整合性について医療機関に確認する。CMENDTC が過去の日付になっているレコードは、年号誤りの可能性も考慮し確認する。日付が年または年月のみで記録されているデータは、可能な限り詳細な日付を医療機関に確認する。

* 問題No.: 4
    * 変数名と値: LB.LBTESTCD = EOS, VISIT = WEEK 24, LBNRIND = HIGH, LBORRES = 0.76 (LBレコード No.271)
    * 矛盾の内容: Week 24 の Eosinophils (EOS) 検査値が基準範囲上限を超えている (LBNRIND=HIGH)。
    * 問題点の原因（推測）: 患者の検査値異常、治験薬または併用薬の影響、基礎疾患、合併症、またはデータ入力エラーの可能性。
    * 対応策（提案）: 医療機関に EOS 高値の臨床的意義、患者の臨床状態、併用薬、基礎疾患、合併症などを確認する。AE ドメインに関連する有害事象が記録されていない理由を確認し、データの整合性を検証する。データ入力値に誤りがないか確認する。

* 問題No.: 5
    * 変数名と値: LBドメインのLBSTRESCとLBSTRESNの値
    * 矛盾の内容: LBSTRESC (標準形式での文字結果/所見) と LBSTRESN (標準単位での数値結果/所見) の値が一致しないレコードが複数存在する。
    * 問題点の原因（推測）: 単位変換ロジックの誤り、データ変換エラー、またはデータ入力エラー。
    * 対応策（提案）: データマネジメントチームは、LBSTRESC と LBSTRESN の変換ロジック、データ変換プロセス、およびデータ入力値を再確認し、不一致の原因を特定して修正する。

クエリ:
* 患者ID: 01-701-1148
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMTRT, CM.CMDECOD (全CMレコード)
        * 医療機関への問い合わせ文面: CMドメインのCMTRT (併用薬名) にUNCODEDと記録されているレコードが多数ありますが、CMDECOD (標準化医薬品名) が未コード化となっている理由をご確認ください。CMレコードのCIMETIDINE (CMレコード No.1, 2) は、CYMETIDINEのタイプミスである可能性はありますか？CMDECODには、MedDRA等の標準化辞書に基づく医薬品名をご登録ください。
        * 判断理由: CMDECODのUNCODEDはSDTMデータとして問題があり、データ品質を損なうため。CIMETIDINEのタイプミスは薬剤名特定に影響を及ぼす可能性があるため、修正の必要性について確認が必要なため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMENDTC = "", CM.CMENDY = NULL (CMドメイン #3, #5, #6, #7, #8, #11-24, #28, #32, #36)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1148 の CMドメインにおいて、CMENDTC および CMENDY が欠損しているレコードが複数あります。CMENDTC（併用薬終了日）とCMENDY（併用薬終了日（試験日））は必須項目であると考えられます。欠損理由をご確認ください。
        * 判断理由: 併用薬の投与期間が不明確であり、データの解釈に影響を与える可能性があるため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC = 2013-12-17 (AE No.6)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1148、Adverse Event No.6 のAdverse Event Start Date (AESTDTC) が治験薬投与開始日より前になっています。AESTDTC (2013-12-17) は日付として正しいでしょうか？正しい場合、治験薬投与開始前にAdverse Event が発現した状況について詳細をご教示ください。
        * 判断理由: Adverse Event開始日が治験薬投与開始日より前である場合、治験薬との因果関係の評価に影響を与える可能性があるため。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD = EOS, LBNRIND = HIGH (WEEK 24)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1148、Week 24のEosinophils (EOS) 検査値が基準範囲上限を超えています。EOS高値について、臨床的な意義と、関連する有害事象の有無についてご教示いただけますでしょうか。
        * 判断理由: 臨床的にEOS上昇の原因を特定し、患者の安全性を評価するために必要な情報であるため。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMSTDTC = "2011", "2006" (CMドメイン #11-#23, #24-#36), AE.AESTDTC = "2012-02" (AEドメイン #8)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1148 の CMドメインおよび AEドメインにおいて、CMSTDTC（併用薬開始日）とAE.AESTDTC（有害事象開始日）が年または年月のみで日付が特定できないレコードがあります。可能な範囲で結構ですので、CMSTDTC および AE.AESTDTC の日付を特定してください。
        * 判断理由: 併用薬および有害事象の開始日が不明確であり、詳細なデータ分析の精度に影響を与える可能性があるため。

    * クエリNo.: 6
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMSTDTC, CM.CMDTC, CM.CMENDTC (CMレコード No.1, 2, 4, 9, 10, 19, 24, 28, 31, 32, 35, 36)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1148 のCMドメイン、レコード[1, 2, 4, 9, 10, 19, 24, 28, 31, 32, 35, 36] の併用薬開始日 (CMSTDTC)、データ収集日 (CMDTC)、併用薬終了日 (CMENDTC) の日付に整合性の疑義があります。原資料を確認し、矛盾がないかご確認ください。特に、レコード28, 31, 32のCMENDTCの日付 (2006年、2011年) がCMDTCと大きく乖離していますが、誤りではないでしょうか？
        * 判断理由: CM日付の不整合は、併用薬の使用期間を正しく把握できず、データ分析の信頼性を損なう可能性があるため。

クエリなし
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1148
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT = CIMETIDINE, CMSTDTC = 2014-01-25, CMENDTC = 2014-02-08
        逸脱内容: 被験者01-701-1148は、WEEK24およびWEEK26にシメチジンを併用しています。シメチジンはCYP阻害薬であり、治験薬ザノメリンとの薬物相互作用のリスクが懸念されます。プロトコルに併用禁止薬リストが明示されていないため、シメチジンが禁止薬に該当するか不明であり、プロトコル遵守状況を確認する必要があります。
        プロトコル該当箇所: プロトコル 3.8. Concomitant Therapy, 3.4.2.2 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list).
        判断理由: シメチジンと治験薬の併用による薬物相互作用のリスクが懸念されるため、プロトコル逸脱の可能性があると判断しました。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT = HYDROCODONE W/APAP, CMSTDTC = 2013-12-16, CMENDTC = 2013-12-17
        逸脱内容: 被験者01-701-1148は、WEEK20に麻薬性鎮痛薬であるHYDROCODONE W/APAPを併用しています。中枢神経系への影響や呼吸抑制作用などが懸念され、治験薬との相互作用や患者の安全性の観点からプロトコル遵守状況を確認する必要があります。プロトコルに併用禁止薬リストの記載がないため、HYDROCODONE W/APAPが禁止薬に該当するか不明です。
        プロトコル該当箇所: プロトコル 3.8. Concomitant Therapy, 3.4.2.2 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list).
        判断理由: 麻薬性鎮痛薬と治験薬の併用による中枢神経系への影響のリスクが懸念されるため、プロトコル逸脱の可能性があると判断しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT = NAPROXEN, CMSTDTC = 2013-12-16, CMENDTC = 2013-12-17
        逸脱内容: 被験者01-701-1148は、WEEK20にNAPROXENを併用しています。プロトコルに併用禁止薬リストの記載がないため、NAPROXENが禁止薬に該当するか不明であり、プロトコル遵守状況を確認する必要があります。
        プロトコル該当箇所: プロトコル 3.8. Concomitant Therapy, 3.4.2.2 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list).
        判断理由: NAPROXENと治験薬の併用がプロトコル遵守状況に与える影響を確認するため、プロトコル逸脱の可能性があると判断しました。

患者ID: 01-701-1148
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT = CIMETIDINE, FLUOROPLEX, HYDROCODONE W/APAP, HYDROCORTISONE, NAPROXEN, SULFAMETHOXAZOLE, TUMS, TYLENOL
        医療機関への問い合わせ文面:
        被験者01-701-1148に併用されている以下の薬剤について、プロトコルで併用が禁止されている薬剤に該当するか、ご回答ください。

        *   CIMETIDINE
        *   FLUOROPLEX
        *   HYDROCODONE W/APAP
        *   HYDROCORTISONE
        *   NAPROXEN
        *   SULFAMETHOXAZOLE
        *   TUMS
        *   TYLENOL

        併用が禁止されている薬剤に該当する場合、それぞれの薬剤について、投与開始日、投与終了日、投与量、投与経路、投与理由を教えてください。プロトコルからの逸脱に該当するかどうか、医学的妥当性の観点を含めてご回答をお願いいたします。
        判断理由: CMドメインデータに記録されている併用薬のプロトコルにおける取扱いを確認するため、医療機関への問い合わせが必要と判断しました。併用禁止薬に該当する場合、プロトコル逸脱となり、臨床試験結果に影響を与える可能性があるため、クエリの優先度をMajorとしました。

# 01-701-1118
## Task1: Clinical Review Results
患者ID: 01-701-1118
* 2000年12月10日 (Day -4840): 併用薬としてアスピリン325mg PRN、MULTIVITAMIN 1 TABLET QD を開始。
* 2003年 (Day 不明): 咳嗽 (COUGH) の有害事象が発現、軽度、未回復/未解決。
* 2014年02月27日 (Day -13): スクリーニング1回目の検査値は全て正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。Medical HistoryとしてALZHEIMER'S DISEASE, HEMORRHOIDS, HEADACHE, INDIGESTION, WRIST FRACTURE, PNEUMOTHORAX, HYPEROPIA, SINUSITIS が報告。
* 2014年03月10日 (Day -1): スクリーニング2回目の併用薬としてアスピリン、マルチビタミンを継続。
* 2014年03月12日 (Day 1): ベースライン測定。ADAS-Cog(11) Subscore 26, WORD RECALL TASK 5, NAMING OBJECTS AND FINGERS (REFER TO 5 C 1, DELAYED WORD RECALL 10, COMMANDS 0, CONSTRUCTIONAL PRAXIS 3, IDEATIONAL PRAXIS 1, ORIENTATION 4, WORD RECOGNITION 10, ATTENTION/VISUAL SEARCH TASK 12, MAZE SOLUTION 6 sec, SPOKEN LANGUAGE ABILITY 0, COMPREHENSION OF SPOKEN LANGUAGE 0, WORD FINDING DIFFICULTY IN SPONTANEOUS S 1, RECALL OF TEST INSTRUCTIONS 1。DAD, NPI-X 実施。併用薬としてアスピリン、マルチビタミンを継続。
* 2014年03月25日 (Day 14): WEEK 2の検査値はEosinophils 0.09 THOU/uL (正常範囲)と減少以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。NPI-X 実施。
* 2014年04月09日 (Day 28): WEEK 4の検査値はSodium 134 mEq/L (正常範囲下限)とわずかに低下以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。NPI-X 実施。
* 2014年04月23日 (Day 42): WEEK 6の検査値はEosinophils 0.17 THOU/uL (正常範囲)とわずかに増加以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。NPI-X 実施。
* 2014年05月08日 (Day 56): WEEK 8の検査値はCalcium 8.6 mg/dL (正常範囲下限)とわずかに低下以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。ADAS-Cog(11) Subscore 19, WORD RECALL TASK 5, NAMING OBJECTS AND FINGERS (REFER TO 5 C 0, DELAYED WORD RECALL 7, COMMANDS 0, CONSTRUCTIONAL PRAXIS 3, IDEATIONAL PRAXIS 0, ORIENTATION 1, WORD RECOGNITION 10, ATTENTION/VISUAL SEARCH TASK 10, MAZE SOLUTION 7 sec, SPOKEN LANGUAGE ABILITY 0, COMPREHENSION OF SPOKEN LANGUAGE 0, WORD FINDING DIFFICULTY IN SPONTANEOUS S 0, RECALL OF TEST INSTRUCTIONS 0。NPI-X 実施。CIBIC: EXTENT OF CHANGE, IF ANY, SINCE BASELINE NO CHANGE (4)。
* 2014年06月05日 (Day 86): WEEK 12の検査値はPH 5.0 (正常範囲下限), PHOSが基準値下限に近い値 (3.0 mg/dL) である以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。ADAS-Cog(11) Subscore 17, WORD RECALL TASK 4, NAMING OBJECTS AND FINGERS (REFER TO 5 C 0, DELAYED WORD RECALL 6, COMMANDS 0, CONSTRUCTIONAL PRAXIS 2, IDEATIONAL PRAXIS 0, ORIENTATION 1, WORD RECOGNITION 10, ATTENTION/VISUAL SEARCH TASK 11, MAZE SOLUTION 9 sec, SPOKEN LANGUAGE ABILITY 0, COMPREHENSION OF SPOKEN LANGUAGE 0, WORD FINDING DIFFICULTY IN SPONTANEOUS S 0, RECALL OF TEST INSTRUCTIONS 0。NPI-X 実施。PH 5.0 (正常範囲下限)。Specific Gravity 1.030 (正常範囲)。Urobilinogen 0 (正常範囲)。
* 2014年07月02日 (Day 113): WEEK 16の検査値はBlood Urea Nitrogen 17 mg/dL (正常範囲上限をわずかに超える), Cholesterol 204 mg/dL (正常範囲上限に近い), Glucose 106 mg/dL (正常範囲上限に近い)とわずかに上昇以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。ADAS-Cog(11) Subscore 17, WORD RECALL TASK 5, NAMING OBJECTS AND FINGERS (REFER TO 5 C 0, DELAYED WORD RECALL 6, COMMANDS 0, CONSTRUCTIONAL PRAXIS 2, IDEATIONAL PRAXIS 0, ORIENTATION 1, WORD RECOGNITION 10, ATTENTION/VISUAL SEARCH TASK 11, MAZE SOLUTION 9 sec, SPOKEN LANGUAGE ABILITY 0, COMPREHENSION OF SPOKEN LANGUAGE 0, WORD FINDING DIFFICULTY IN SPONTANEOUS S 0, RECALL OF TEST INSTRUCTIONS 0。NPI-X 実施。CIBIC: EXTENT OF CHANGE, IF ANY, SINCE BASELINE MARKED IMPROVEMENT (1)。
* 2014年07月30日 (Day 141): WEEK 20の検査値はBlood Urea Nitrogen 18 mg/dL (正常範囲上限をわずかに超える)とわずかに上昇以外は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。NPI-X 実施。
* 2014年08月27日 (Day 169): WEEK 24の検査値は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。ADAS-Cog(11) Subscore 15, WORD RECALL TASK 5, NAMING OBJECTS AND FINGERS (REFER TO 5 C 0, DELAYED WORD RECALL 8, COMMANDS 0, CONSTRUCTIONAL PRAXIS 2, IDEATIONAL PRAXIS 0, ORIENTATION 1, WORD RECOGNITION 7, ATTENTION/VISUAL SEARCH TASK 18, MAZE SOLUTION 7 sec, SPOKEN LANGUAGE ABILITY 0, COMPREHENSION OF SPOKEN LANGUAGE 0, WORD FINDING DIFFICULTY IN SPONTANEOUS S 0, RECALL OF TEST INSTRUCTIONS 0。NPI-X 実施。PH 6.0 (正常範囲)。Specific Gravity 1.026 (正常範囲)。Urobilinogen 0 (正常範囲)。CIBIC: EXTENT OF CHANGE, IF ANY, SINCE BASELINE MARKED WORSENING (7)。
* 2014年09月09日 (Day 182): WEEK 26の検査値は正常範囲内。併用薬としてアスピリン、マルチビタミンを継続。NPI-X DELUSIONS PRESENT, HALLUCINATIONS PRESENT, AGITATION/AGRESSION PRESENT, DEPRESSION/DYSPHORIA PRESENT, ANXIETY PRESENT, EUPHORIA/ELATION PRESENT, APATHY/INDIFFERENCE PRESENT, DISINHIBITION PRESENT, IRRITABILITY/LABILITY PRESENT, ABERRANT MOTOR BEHAVIOR PRESENT, NIGHT-TIME BEHAVIOR PRESENT, APPETITE/EATING CHANGE PRESENT はいずれも "ABSENT"。DELUSIONS Score, HALLUCINATIONS Score, AGITATION/AGRESSION Score, DEPRESSION/DYSPHORIA Score, ANXIETY Score, EUPHORIA/ELATION Score, APATHY/INDIFFERENCE Score, DISINHIBITION Score, IRRITABILITY/LABILITY Score, ABERRANT MOTOR BEHAVIOR Score, NIGHT-TIME BEHAVIOR Score, APPETITE/EATING CHANGE Score はいずれも 0。PROTOCOL COMPLETED, FINAL LAB VISIT。

---

**クエリ:**

**患者ID: 01-701-1118**
*   **クエリNo.: 1**
    *   **臨床試験結果への影響度合い:** Major
    *   **変数名と値:** AE.AESTDTC = 2003
    *   **医療機関への問い合わせ文面:**
        治験参加者の有害事象「咳嗽 (COUGH)」の開始日について確認させてください。現在、データ上では2003年となっており、治験期間以前に発症しているように見受けられます。もしデータ入力の誤りであれば、正確な開始日時の情報をご提供いただけますでしょうか。この有害事象の開始日が治験期間外であるか否かによって、安全性評価に影響が生じる可能性があるため、回答をよろしくお願いいたします。
    *   **判断理由:**
        報告された有害事象「咳嗽 (COUGH)」の開始日(2003年)が、治験期間（DMドメインのRFSTDTC: 2014年3月12日以降）より前であるため、データの正確性を確認する必要がある。もし誤りであれば、データの修正が必要となる。有害事象の評価期間に影響を与える可能性があり、臨床試験の安全性評価に関わる重要な疑義事項であるため、「臨床試験結果への影響度合い」はMajorと判断した。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMDTC, CM.CMSTDTC, CM.CMENDTC, AE.AESTDTC, EX.EXSTDTC, LB.LBDTC, Define.xmlのdataType定義 (LBDTC)

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC = 2003, EX.EXSTDTC = 2014-03-12
    * 矛盾の内容: 有害事象（AEドメイン）の開始日（2003年）が、治験薬の初回投与日（EXドメイン、2014年3月12日）よりも10年以上前になっており、時間軸の矛盾が認められます。有害事象が治験薬投与前に発現している可能性は低いと考えられます。
    * 問題点の原因（推測）: AEドメインのAESTDTC（有害事象開始日）のデータ入力誤り、または、CM（併用薬）ドメインに登録されるべき有害事象がAEドメインに誤って登録された可能性。
    * 対応策（提案）: 医療機関にAESTDTCの記録を確認し、正しい日付への修正、またはデータ登録ドメインの修正を依頼してください。

* 問題No.: 2
    * 変数名と値: CM.CMSTDTC = 2000-12-10, CM.CMDTC = 2014-02-27 (CMレコード1行目)
    * 矛盾の内容: 併用薬（CMドメイン）の開始日（2000年12月10日）が、データ収集日（2014年2月27日）よりも13年以上前になっており、時間軸の矛盾が認められます。
    * 問題点の原因（推測）: CMドメインのCMSTDTC（併用薬開始日）のデータ入力誤り。
    * 対応策（提案）: 医療機関にCMSTDTCの記録を確認し、正しい日付への修正を依頼してください。

* 問題No.: 3
    * 変数名と値: CM.CMENDTC = "" (複数のCMレコード)
    * 矛盾の内容: 併用薬（CMドメイン）の終了日 (CMENDTC) が、複数のレコードで欠損しています。特に、アスピリンとマルチビタミンは複数visitにわたって記録されているにもかかわらず、CMENDTCが欠損していることは不自然です。
    * 問題点の原因（推測）: データ入力時の未入力、または併用薬が継続中で終了日が未定のため未入力の可能性。
    * 対応策（提案）: 医療機関にCMENDTCの記録を確認し、終了日が判明している場合はデータ修正、継続中の場合はその旨をデータに反映するよう依頼してください。

* 問題No.: 4
    * 変数名と値: Define.xmlのdataType定義 (LBDTC) = date, JSONデータのdataType定義 (LBDTC) = datetime
    * 矛盾の内容: Define.xmlとJSONデータで、LBドメインのLBDTC（検査実施日）のデータ型定義が異なっています。Define.xmlではdate型、JSONデータではdatetime型と定義されています。
    * 問題点の原因（推測）: Define.xmlの記述誤り、またはDefine.xmlのバージョンが古い可能性。
    * 対応策（提案）: Define.xmlのLBDTCのdataTypeをdatetimeに修正することを提案します。Define-XMLのバージョンを最新のものに更新することも推奨します。

クエリ:
* 患者ID: 01-701-1118
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: AE.AESTDTC = 2003 (AEドメイン), EX.EXSTDTC = 2014-03-12 (EXドメイン)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1118 の有害事象データについて、咳嗽（COUGH）の開始日（AESTDTC）が2003年と記録されています。治験薬の初回投与日（EXドメイン）は2014年3月12日ですが、有害事象の開始日が治験薬投与開始日より10年以上も前になっているのは医学的に不自然です。咳嗽の正確な開始日をご確認いただけますでしょうか。また、咳嗽と治験薬との因果関係について、改めて評価をお願いいたします。
        * 判断理由: 有害事象の開始日は、治験薬との因果関係を評価する上で最も重要な情報の一つです。開始日が治験薬投与前である場合、治験薬との因果関係が否定される可能性があり、臨床試験の主要評価項目に影響を及ぼす可能性があります。データの信頼性を確保するために、早急な確認と修正が必要です。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC = 2000-12-10 (CMドメイン)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1118 の併用薬データについて、アスピリン（CMTRT=ASPIRIN, CMSEQ=1）の開始日（CMSTDTC）が2000年12月10日と記録されています。データ収集日（CMDTC=2014-02-27）と比較して非常に古い日付となっており、データの誤りが疑われます。アスピリンの正確な開始日について、原資料をご確認いただけますでしょうか。
        * 判断理由: 併用薬の情報は、患者背景や治験薬の効果に影響を与える可能性があり、データの正確性が重要です。特に開始日は、併用薬の使用状況を把握する上で重要な情報となります。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC = "" (CMドメイン)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1118 の併用薬データについて、複数のレコードで投与終了日（CMENDTC）が空欄となっています。これらの併用薬は現在も継続中でしょうか？終了している場合は、終了日をご教示いただけますでしょうか。
        * 判断理由: 併用薬の終了日は、患者の併用薬状況を把握し、より詳細な解析を行う上で有益な情報ですが、臨床試験の主要な評価項目に直接的な影響を与える可能性は低いと考えられます。

Define.xmlの修正候補:
* ItemGroupDef OID="LB" 内の ItemDef OID="LB.LBDTC" の dataType を date から datetime に修正する。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1118
    逸脱No.: 1
        臨床試験結果への影響度合い: Major/Minor
        変数名と値: CM.CMTRT = ASPIRIN, CM.CMINDC = PROPHYLAXIS OR NON-THERAPEUTIC USE, CM.CMSTDTC = 2000-12-10, CM.CMENDTC = "" (欠損)
        逸脱内容:
            被験者01-701-1118において、併用薬としてアスピリンがスクリーニング1からWEEK26まで継続して投与されている。CM.CMINDC（Indication）が "PROPHYLAXIS OR NON-THERAPEUTIC USE" となっており、治験薬の効果に影響を与える可能性も否定できません。また、CM.CMSTDTCにデータ入力時のエラーと思われる古い日付（2000-12-10）が記録されています。CM.CMENDTCが欠損しており、併用薬の使用期間が不明確です。プロトコルには併用禁止薬に関する明確な記述が見当たらず、現時点ではプロトコル逸脱と断定できません。
        プロトコル該当箇所: プロトコルセクション3.8 (併用療法) およびセクション3.4.2.2 (除外基準), Define.xml ValueList.CM.CMROUTE, ValueList.CM.CMDOSFRQ
        判断理由:
            アスピリンは一般的なOTC薬であり、低用量アスピリンは心血管イベントの予防目的で使用されることがあります。しかし、アスピリンは抗血小板薬であり、本臨床試験の評価項目（特に安全性評価、出血リスク）に影響を与える可能性があります。プロトコルにアスピリンの併用に関する明確な規定がないため、現時点では逸脱と断定できませんが、データ入力エラーの可能性、治験薬への影響、患者の安全性、データ品質の観点から医療機関への確認が必要と判断しました。

患者ID: 01-701-1118
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = ASPIRIN, CM.CMSTDTC, CM.CMENDTC
        医療機関への問い合わせ文面:
            治験参加者01-701-1118において、以下の併用薬に関する情報に疑義があります。医療機関にて回答をお願いいたします。

            1. 併用薬：ASPIRIN
                * 投与の医学的理由、投与量、投与期間についてご教示ください。
                * CMINDC（Indication）が「PROPHYLAXIS OR NON-THERAPEUTIC USE」となっていますが、具体的な使用目的について教えてください。
                * 本臨床試験におけるアスピリン投与の医学的妥当性について治験責任医師の見解を伺いたいです。特に、本臨床試験の評価項目（安全性評価、出血リスク、有効性評価）に与える影響について懸念されます。

            2. データ品質
                * CM.CMSTDTCに記録されている2000-12-10は誤りの可能性があると考えられます。正しい開始日を教えてください。
                * 併用薬MULTIVITAMINのCMENDTC（投与終了日）が欠損していますが、最終投与日あるいは投与継続状況について教えてください。投与終了日が不明な場合、投与継続中として扱う理由とその根拠をご教示ください。

            3. プロトコル遵守
                * プロトコル上、アスピリンの併用は許可されていますでしょうか。
                * 併用可能な場合、アスピリンと治験薬の併用に関する規定（投与量の調整や観察項目、併用注意など）はありますか？

            本クエリは、患者様の安全確保、データの医学的妥当性の検証、およびプロトコル遵守状況の確認を目的としています。ご多忙のところ恐縮ですが、ご回答いただけますようお願い申し上げます。
        判断理由:
            プロトコル逸脱の疑いを明確にするため、また、データ

# 01-703-1403
## Task1: Clinical Review Results
**1. 症例サマリーの作成:**

患者ID: 01-703-1403
* 2012年11月28日 (Day -14): スクリーニング1回目の検査で、尿酸値が基準値上限を超過 (7.7 mg/dL、基準値: 2.5-7.5 mg/dL)
* 2012年12月05日 (Day -7): スクリーニング1回目のバイタルサイン測定で、体重が増加 (173.0 LB -> 177 LB)。
* 2012年12月12日 (Day 1): ベースライン訪問。
* 2012年12月12日 (Day 1): 体重減少 (WEIGHT DECREASED) の有害事象発現（中等度）。
* 2012年12月13日 (Day 2): 下痢 (DIARRHOEA) および嘔吐 (VOMITING) の有害事象発現（いずれも中等度、治験薬との因果関係はProbable）。
* 2012年12月14日 (Day 3): 下痢、嘔吐の有害事象が軽快。
* 2012年12月15日 (Day 4): 胸部不快感 (CHEST DISCOMFORT) の有害事象発現（軽度、治験薬との因果関係はProbable）。
* 2012年12月16日 (Day 5): 胸部不快感の有害事象が軽快。
* 2012年12月19日 (Day 8): WEEK 2訪問、最終 лаборатория 訪問。
    * 尿酸値が基準値内 (7.5 mg/dL、基準値: 2.5-7.5 mg/dL) に改善。
    * 体重減少 (WEIGHT DECREASED) の有害事象が継続中。
    * ADVERSE EVENTにより治験薬投与中止。
* 2013年01月08日 (Day 27): AEフォローアップ訪問。体重減少 (WEIGHT DECREASED) の有害事象は回復 (RECOVERED/RESOLVED)。再発性体重減少 (WEIGHT DECREASED) の有害事象発現 (AE No.5, 中等度)。

---

**2. クエリの作成:**

患者ID: 01-703-1403
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LBTESTCD=URATE, LBORRES=7.7 mg/dL (SCREENING 1)
    * 医療機関への問い合わせ文面: 患者のスクリーニング1回目の検査において、尿酸値が基準範囲上限を超過 (7.7 mg/dL [基準範囲: 2.5-7.5 mg/dL]) しています。治験責任医師に、医学的に臨床的な意義があるかどうか、また、再検査の必要性についてご評価いただきたいです。尿酸値上昇の原因として考えられる要因（食事、脱水、既往歴、併用薬など）があれば、併せてご教示ください。
    * 判断理由: 尿酸値の上昇は、高尿酸血症や痛風のリスク因子となる可能性があり、医学的に注意が必要です。特に、選択・除外基準に抵触する可能性も考慮し、臨床的な意義を確認する必要があります。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: DM.ACTARMCD: Xan_Lo, DM.ACTARM: Xanomeline Low Dose, DM.ARMCD: Xan_Hi, DM.ARM: Xanomeline High Dose
    * 医療機関への問い合わせ文面: DMドメインのACTARMCD (Actual Arm Code) およびACTARM (Actual Arm Description) の値が、TAドメイン、TVドメインで定義されているPlanned Arm (ARMCD, ARM) の Xanomeline High Dose と一致していません。DMドメインのACTARMCDとACTARMの記録に、データ入力誤りの可能性はないでしょうか。記録に誤りがない場合、ACTARMCDとACTARMにXanomeline Low Doseが記録されている理由をご教示ください。
    * 判断理由: DMドメインのACTARMとACTARMCDの値が、Planned Armと一致していないことはデータの不整合性を示唆し、データの正確性を確認する必要があるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMDECOD, CM.CMINDC, DS.DSSPID, VS.VSLOC, LB.LBORRESU, LB.LBTESTCD=URATE

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMDECOD = UNCODED, CM.CMINDC = ""
    * 矛盾の内容: 併用薬CIPRO (シプロフロキサシン) の標準化された薬剤名 (CMDECOD) が未コード化 (UNCODED) であり、適応症 (CMINDC) が空欄です。Define.xmlではCMDECODはWHODRUGコードリストを参照することになっていますが、データが準拠していません。
    * 問題点の原因（推測）: データ入力時またはSDTM変換時のエラー、CMDECODのコード設定漏れ、CMINDCの入力漏れ
    * 対応策（提案）: CMDECODに適切なWHODRUGコードを設定するか、UNCODEDの理由をSUPPCM等で説明することを検討してください。CMINDCについて原資料を確認し、情報を追記するか、欠損理由をSDTMまたはSUPPドメインで説明することを検討してください。Define.xmlのCM.CMDECOD ItemDefのCodeListRef削除も検討ください。

* 問題No.: 2
    * 変数名と値: DS.DSSPID = "" (DSSEQ=2), DS.DSSPID = " 5" (DSSEQ=1)
    * 矛盾の内容: DispositionドメインのDSSPID (Sponsor-Defined Identifier) の値に一貫性がありません。DSSEQ=2のレコードではDSSPIDが空欄、DSSEQ=1では意図しないスペース (" 5") が含まれています。
    * 問題点の原因（推測）: データ入力時のタイプミス、データ入力規則の不徹底、意図的な欠損値
    * 対応策（提案）: DSSPID=" 5" が意図的なデータ入力を医療機関に確認し、タイプミスであれば修正を依頼してください。DSSEQ=2のDSSPIDが意図的な欠損値か確認し、意図的な欠損値の場合は理由をSDTMまたはSUPPドメインで説明することを検討してください。

* 問題No.: 3
    * 変数名と値: VS.VSLOC = "" (複数のレコード)
    * 矛盾の内容: Vital Signsドメインの複数のレコードでVSLOC (測定部位) が空欄となっています。VSLOCは測定部位を示す重要な情報であり、データ品質上の懸念があります。
    * 問題点の原因（推測）: データ入力ミス、データ収集時の記録漏れ
    * 対応策（提案）: VSLOCがデータ入力ミスか意図的な欠損値か原資料で確認し、データ入力ミスの場合は修正、意図的な欠損値の場合は欠損理由をSDTMまたはSUPPドメインで説明することを検討してください。

* 問題No.: 4
    * 変数名と値: LB.LBORRESU = NULL (多数のレコード)
    * 矛盾の内容: Laboratory Tests Resultsドメインの多数のレコードでLBORRESU (Original Units) がNULLとなっています。LBORRESUがNULLの場合、LBORRES (Original Units) の単位が不明となり、データの解釈が困難になります。
    * 問題点の原因（推測）: データ入力時またはSDTM変換時のエラー
    * 対応策（提案）: LBORRESUがNULLとなっている原因を調査し、可能な限りLBORRESUに適切な単位を設定するデータ修正を検討してください。

* 問題No.: 5
    * 変数名と値: LB.LBTESTCD=URATE, LB.LBORRES=7.7 (SCREENING 1)
    * 矛盾の内容: SCREENING 1の尿酸値 (URATE) が基準値上限を超過 (HIGH) しています。医学的に、臨床的意義の確認が必要です。
    * 問題点の原因（推測）: 患者特性による一時的な高値、データ入力誤り、検査機器エラー
    * 対応策（提案）: 医療機関にURATE高値の原因と臨床的意義について問い合わせ、臨床的に問題がないか、再検査の必要性について確認してください。

* Define.xmlの修正候補:
    * CM.CMDECOD ItemDef の CodeListRef (DRUGDICT) がデータと整合していないため、CodeListRef を削除することを検討する。
    * DS.DSCAT ItemDef に、DSTERM="ADVERSE EVENT" の場合の適切なカテゴリを明記することを検討する。
    * CM.CMINDC ItemDef を必須項目 (Mandatory="Yes") に修正することを検討する。

クエリ:
* 患者ID: 01-703-1403
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMDECOD = UNCODED, CM.CMINDC = "", CMTRT: CIPRO
        * 医療機関への問い合わせ文面: 併用薬CIPRO (CMTRT) の CMDECOD (標準化された薬剤名) が UNCODED、CMINDC (適応症) が空文字で登録されています。CMDECOD に対応する標準用語 (WHODRUGコードなど) が存在するか、CMINDC (適応症) を原資料で確認し、データ修正をお願いできますでしょうか。もし UNCODED が適切、または CMINDC が不明な場合は、その理由をご教示ください。
        * 判断理由: 併用薬情報は患者の安全性評価において重要であり、標準用語、適応症が不明な場合、データの解釈や分析に影響を与える可能性があるため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: DS.DSSPID = " 5" (DSSEQ=1), DS.DSSPID = "" (DSSEQ=2)
        * 医療機関への問い合わせ文面: DSドメインのDSSPID (Sponsor-Defined Identifier) の値に一貫性がありません。DSSEQ=1のDSSPID=" 5" のスペースは意図的なものでしょうか。DSSEQ=2のDSSPIDは意図的な欠損値でしょうか、データ入力ミスでしょうか。原資料をご確認いただき、データ修正または欠損理由のご教示をお願いします。
        * 判断理由: データ入力の一貫性に関するクエリであり、データ品質管理の観点から確認が必要な事項であるため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: VS.VSLOC = "" (複数のレコード)
        * 医療機関への問い合わせ文面: VSドメインの複数のレコードでVSLOC (測定部位) が空欄です。測定部位が不明なデータについて、理由をご教示いただけますでしょうか。
        * 判断理由: バイタルサイン測定の解釈において、測定部位は重要な情報となる可能性があり、データ品質向上のため確認を行うことが望ましい。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBORRESU = NULL (多数のレコード)
        * 医療機関への問い合わせ文面: LBドメインの多数のレコードでLBORRESU (Original Units) がNULLです。LBORRESUがNULLとなっている原因をご調査いただき、可能な限りLBORRESUに適切な単位を設定してデータ修正をご検討いただけますでしょうか。
        * 判断理由: 臨床検査値の単位が不明な場合、臨床的な解釈や安全性評価に支障をきたす可能性があり、データ品質上、早急な対応が必要と考えられるため。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=URATE, LB.LBORRES=7.7 (SCREENING 1), LB.LBORRES=7.5 (WEEK 2)
        * 医療機関への問い合わせ文面: 患者ID 01-703-1403 のSCREENING 1とWEEK 2の尿酸値 (LBTESTCD=URATE) について質問です。SCREENING 1では7.7 mg/dLと高値でしたが、WEEK 2では7.5 mg/dLと正常範囲内でした。1. SCREENING 1とWEEK 2のURATE値は測定値として正しいでしょうか？再検査データがあればご提供ください。2. SCREENING 1でURATE値が高値であった原因として、医学的に考えられる理由があれば教えてください。3. 患者は高尿酸血症や痛風の既往歴がありますか？
        * 判断理由: 尿酸値は通常短期間で大きく変動することは考えにくいため、データの信頼性を確認し、医学的な解釈を明確にする必要
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1403
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DM.ARMCD = Xan_Hi, DM.ACTARMCD = Xan_Lo, EX.EXTRT = XANOMELINE, EX.EXDOSE = 54mg
        逸脱内容: 計画された投与群（Planned Arm: Xan_Hi）と実際の投与群（Actual Arm: Xan_Lo）がDMドメインで一致していません。実際の治験薬投与量（EX.EXDOSE = 54mg）は低用量群（Xan_Lo）に相当し、意図された投与計画からの逸脱が示唆されます。治験薬の割付不一致は、臨床試験のblind性を損なう可能性があり、主要なプロトコル逸脱にあたる可能性があります。
        プロトコル該当箇所: 3.5 患者割付, 3.6 投与量と投与方法
        判断理由: 計画された投与と実際の投与に矛盾があり、プロトコルで規定された患者割付手順からの逸脱、またはデータ入力の誤りの可能性があります。治験薬の有効性評価に重大な影響を与える可能性があるため、臨床試験結果への影響度合いはMajorと判断しました。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = CIPRO, CM.CMCLAS = UNCODED
        逸脱内容: 併用薬としてCIPRO（シプロフロキサシン）が投与されていますが、薬剤クラス（CMCLAS）がUNCODEDであり、詳細な薬剤情報が不明です。プロトコルに併用禁止薬リストが存在する場合、CIPROが該当する可能性があるため、薬剤クラスと併用可否の確認が必要です。併用禁止薬に該当する場合、プロトコル逸脱となります。
        プロトコル該当箇所: 3.8 併用療法, 3.4.2.2 除外基準 [31b]
        判断理由: 併用薬CIPROがプロトコルで禁じられている薬剤に該当する可能性があるため、プロトコル逸脱の疑いとして検出しました。薬剤クラスが不明なため、医療機関への確認が必要と判断しました。臨床試験結果に影響を与える可能性があるため、Majorと判断しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD = URATE, LB.LBORRES = 7.7 mg/dL, LBNRIND = HIGH (SCREENING 1)
        逸脱内容: スクリーニング時の尿酸値が基準値上限を超過（HIGH）しています。除外基準[27b]には、Lilly Reference Range III を超える臨床検査値が除外基準として記載されていますが、具体的な尿酸値の基準値は不明です。Lilly Reference Range IIIにおける尿酸値の基準値と、逸脱該当の有無を確認する必要があります。
        プロトコル該当箇所: 3.4.2.2 除外基準 [27b]
        判断理由: スクリーニング時の尿酸値が基準値上限を超過しているものの、プロトコルおよびDefine.xmlからは具体的な基準値が不明なため、現時点ではMinor逸脱の疑いとして検出しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MH.MHSEV = 空欄
        逸脱内容: 病歴（Medical History）にアルツハイマー病（ALZHEIMER'S DISEASE）の既往歴が記録されていますが、重症度（MHSEV）が空欄です。病歴の重症度は必須データ項目ではありませんが、患者背景を把握する上で重要な情報であるため、データ品質の観点からMinor逸脱として検出しました。
        プロトコル該当箇所: 3.4.2.1 選択基準, 3.9.3.1 安全性の評価項目
        判断理由: アルツハイマー病の既往歴自体は選択基準違反ではありませんが、病歴の重症度欠損はデータ品質上の問題としてMinor逸脱と判断しました。

    逸脱No.: 5
        臨床試験結果への影響度合い: Minor
        変数名と値: AE.AETERM = CHEST DISCOMFORT, AE.AESTDTC = 2012-12-15, AE.AEENDTC = 2012-12-16
        逸脱内容: 有害事象（Adverse Event）として報告されたCHEST DISCOMFORT（胸部不快感）の持続期間が1日と短期間です。報告された期間が医学的に妥当であるか、データ入力誤りの可能性も含めて確認が必要です。
        プロトコル該当箇所: 3.9.3.2.1 有害事象報告要件
        判断理由: 有害事象の持続期間が短く、医学的妥当性の観点から確認が必要なため、データ入力誤りの可能性も考慮しMinor逸脱として検出しました。

患者ID: 01-703-1403
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT=CIPRO, CMINDC=
        医療機関への問い合わせ文面:
        CDISCPILOT01試験、被験者01-703-1403の併用薬CIPROについて、以下の点についてご教示ください。

        1.  CIPROは本試験プロトコルにおける併用禁止薬に該当しますでしょうか？
        2.  CIPRO投与の医学的理由（CMINDC: 適応症）をご教示ください。
        3.  CIPROの投与期間、投与量、投与経路についてご教示ください。
        4.  CIPROの併用がプロトコル逸脱となる場合、本試験の評価項目に与える影響について、治験担当医の見解をお聞かせください。

        ご多忙のところ恐縮ですが、ご回答いただけますようお願い申し上げます。
        判断理由: 併用薬CIPROがプロトコル逸脱に該当するかの確認、および投与の医学的妥当性を評価するために、医療機関への問い合わせが必要と判断しました。併用禁止薬に該当する場合、臨床試験の評価項目に重大な影響を与える可能性があるため、臨床試験結果への影響度合いはMajorと判断しました。

# 01-701-1028
## Task1: Clinical Review Results
**症例サマリー**

* 患者ID: 01-701-1028
    * 2013年07月11日 (Day -8): スクリーニング1回目、MCH（平均赤血球ヘモグロビン量）が基準値上限超え (37pg [基準値範囲: 26-34pg])、MCV（平均赤血球容積）が基準値上限超え (104fL [基準値範囲: 80-100fL])。
    * 2013年07月01日 (Day -17): 適用部位紅斑（有害事象）が発現 (軽度、未回復)。
    * 2013年08月08日 (Day 21): 適用部位掻痒感（有害事象）が発現 (軽度、未回復)。
    * 2013年09月10日 (Day 54): 8週目の検査でCK（クレアチンキナーゼ）が基準値上限超え (317U/L [基準値範囲: 22-198U/L])。
    * 2013年11月06日 (Day 111): 16週目の検査でAnisocytes（異形赤血球）およびMacrocytes（大球赤血球）が異常値、Calcium（カルシウム）が基準値下限を下回る (8.0mg/dL [基準値範囲: 8.4-10.3mg/dL])、MCH（平均赤血球ヘモグロビン量）が基準値上限超え (35pg [基準値範囲: 26-34pg])、MCV（平均赤血球容積）が基準値上限超え (103fL [基準値範囲: 80-100fL])。
    * 2013年12月04日 (Day 139): 20週目の検査でAnisocytes（異形赤血球）が異常値、MCH（平均赤血球ヘモグロビン量）が基準値上限超え (35pg [基準値範囲: 26-34pg])、MCV（平均赤血球容積）が基準値上限超え (102fL [基準値範囲: 80-100fL])。
    * 2014年01月06日 (Day 172): 24週目の検査でMacrocytes（大球赤血球）とPOLYCHR（多染赤血球）が異常値、MCV（平均赤血球容積）が基準値上限超え (104fL [基準値範囲: 80-100fL])。
    * 2014年01月14日 (Day 180): 26週目の検査でMacrocytes（大球赤血球）が異常値、MCH（平均赤血球ヘモグロビン量）が基準値上限超え (35pg [基準値範囲: 26-34pg])、MCV（平均赤血球容積）が基準値上限超え (106fL [基準値範囲: 80-100fL])。

---

**クエリ**

* 患者ID: 01-701-1028
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=ANISO, LB.LBTESTCD=MACROCY, LBNRIND=ABNORMAL (Week 16)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1028 の Week 16 (2013年11月06日) の臨床検査値データにおいて、血液検査項目である異形赤血球 (ANISO) と大球性赤血球 (MACROCY) でABNORMAL (異常) が報告されています。臨床的な意義、および治験薬との因果関係について評価をお願いします。
        * 判断理由: 貧血や骨髄異形成症候群などが疑われる異常所見であり、臨床的に重要な情報であるため、クエリ発行が必要と判断しました。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=CK, LBNRIND=HIGH (Week 8)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1028 の Week 8 (2013年09月10日) の臨床検査値データにおいて、血液検査項目であるクレアチンキナーゼ (CK) でHIGH (高値) が報告されています。再検査の必要性を含め、臨床的な意義について評価をお願いします。
        * 判断理由:  クレアチンキナーゼ (CK) の上昇は、筋肉系の副作用や心筋障害の可能性も考慮する必要があるため、念のため医療機関に専門家の意見を求めることが適切と考えられます。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMINDC (空欄)
        * 医療機関への問い合わせ文面: 併用薬 HYDROCORTISONE (HYDROCORTISONE) の投与目的 (適応疾患、症状など) を教えてください。
        * 判断理由: 併用薬 HYDROCORTISONE の投与目的が不明であるため、医学的妥当性の観点から確認が必要です。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=MCH, LB.LBTESTCD=MCV, LBNRIND=HIGH (Screening 1)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1028 の Screening 1 (2013年07月11日) の臨床検査値データにおいて、血液検査項目である平均赤血球ヘモグロビン (MCH) と平均赤血球容積 (MCV) でHIGH (高値) が報告されています。治験薬投与前のデータではありますが、医学的な疑義がないか確認をお願いします。
        * 判断理由: スクリーニング時のデータであり、直ちに臨床的な問題となる可能性は低いと考えられますが、医学的妥当性の観点から念のため確認します。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, EX.EXSTDTC, LB.LBTESTCD(CK, MCV, CA, ANISO, MACROCY, POLYCHR), CM.CMSTDTC, CM.CMDTC, LB.LBORRESU/LBSTRESU, QS.QSBLFL, CM.CMENDY

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC = 2013-07-01, EX.EXSTDTC = 2013-07-19
    * 矛盾の内容: AEドメインの有害事象「APPLICATION SITE ERYTHEMA」の開始日が、EXドメインの治験薬投与開始日より前になっている。時系列矛盾が疑われる。
    * 問題点の原因（推測）: データ入力時の誤り、またはAE開始日の誤記の可能性。
    * 対応策（提案）: 医療機関に原資料を確認し、AE開始日とEX開始日の正当性を検証し、必要に応じてデータ修正を依頼する。

* 問題No.: 2
    * 変数名と値: LB.LBTESTCD = CK, LB.LBORRES = 317, LBNRIND = HIGH (LBSEQ=142)
    * 矛盾の内容: WEEK 8のCreatine Kinase (CK) 検査値が基準値上限を超過。
    * 問題点の原因（推測）: 治験薬の影響、患者の基礎疾患、または検査エラーの可能性。
    * 対応策（提案）: 
        1. Define.xmlとプロトコルでCK基準値と臨床的意義を確認。
        2. MH、AEドメインでCK上昇に関連する既往歴や有害事象を確認。
        3. 医療機関にCK上昇の原因、再検査の実施、医学的解釈を問い合わせる。

* 問題No.: 3
    * 変数名と値: LB.LBTESTCD = MCV (Ery. Mean Corpuscular Volume), LB.LBORRES = 104-106 fL (複数Visit)
    * 矛盾の内容: Ery. Mean Corpuscular Volume (MCV) が複数Visitで基準範囲上限を超過。
    * 問題点の原因（推測）: 患者の基礎疾患（ビタミンB12/葉酸欠乏症）、データ入力誤りの可能性。
    * 対応策（提案）: 
        1. LBドメインの他の血液検査値を確認。
        2. MHドメインにビタミンB12/葉酸欠乏症の既往歴を確認。
        3. 医療機関にMCV上昇の原因を問い合わせる。

* 問題No.: 4
    * 変数名と値: LB.LBTESTCD = CA (Calcium), LB.LBORRES = 8.0 mg/dL (WEEK 16)
    * 矛盾の内容: Calcium (CA) がWEEK 16で基準範囲下限を下回っている。
    * 問題点の原因（推測）: 治験薬の影響、患者の基礎疾患、食事摂取状況による影響の可能性。
    * 対応策（提案）: 
        1. LBドメインの他の電解質検査値を確認。
        2. CMドメインにカルシウム低下を引き起こす併用薬がないか確認。
        3. 医療機関にCA低下の原因を問い合わせる。

* 問題No.: 5
    * 変数名と値: LB.LBTESTCD = ANISO, MACROCY, POLYCHR, LBORRES = 1 NO UNITS (複数Visit)
    * 矛盾の内容: Anisocytes, Macrocytes, Polychromasia が複数Visitで異常値 (ABNORMAL)。
    * 問題点の原因（推測）: 患者の基礎疾患（血液疾患）、検査エラーの可能性。
    * 対応策（提案）: 
        1. LBドメインの他の血液検査値を確認。
        2. MHドメインに血液疾患の既往歴を確認。
        3. 医療機関にANISO, MACROCY, POLYCHR 異常値の原因を問い合わせる。

* 問題No.: 6
    * 変数名と値: LB.LBORRESU, LB.LBSTRESU (複数レコード)
    * 矛盾の内容: LBORRESUとLBSTRESUで単位が異なっている項目が複数存在する。
    * 問題点の原因（推測）: データ変換時の単位換算ミス、Define.xml定義と実際のデータ単位の不整合の可能性。
    * 対応策（提案）: 
        1. Define.xmlのLBSTRESU定義とデータ単位を照合。
        2. データ変換プログラムの単位換算ロジック見直し。
        3. Define.xmlのLBSTRESU単位定義修正（修正候補として後述）。

* 問題No.: 7
    * 変数名と値: QS.QSBLFL = "Y" または "" (missing)
    * 矛盾の内容: QSドメインのBaseline Flag (QSBLFL) が "Y" と "" (missing) で混在。
    * 問題点の原因（推測）: データ入力時の不統一、Define.xml定義とデータ作成手順書の不整合の可能性。
    * 対応策（提案）: 
        1. Define.xmlとデータ作成手順書でQSBLFL定義を確認。
        2. データ入力担当者にQSBLFL入力ルールを再周知。
        3. QSBLFLが"" (missing) のレコードのBaseline Flag要否確認とデータ修正。

* 問題No.: 8
    * 変数名と値: CM.CMSTDTC (複数レコード), CM.CMDTC (複数レコード)
    * 矛盾の内容: CMドメインでCMSTDTC (Medication Start Date) がCMDTC (Date/Time of Collection) と同じ日付のレコードが複数あり、CMSTDTCの日付フォーマットがYYYY-MM形式で不完全。
    * 問題点の原因（推測）: データ入力時の誤り、情報収集時の日付誤り、CMSTDTCの日付情報欠損の可能性。
    * 対応策（提案）: 医療機関に原資料確認を依頼し、日付の正当性を検証、データ形式をYYYY-MM-DDに修正、CMENDTC等欠損値の解消を検討。

* 問題No.: 9
    * 変数名と値: CM.CMENDTC, CM.CMENDY (NULL値)
    * 矛盾の内容: CMドメインのCMENDTC, CMENDYにNULL値が散見される。
    * 問題点の原因（推測）: 併用薬が継続中のため未入力、またはデータ欠損の可能性。
    * 対応策（提案）: 
        1. Define.xmlとプロトコルでCMENDTC, CMENDYが必須項目か確認。
        2. 医療機関に併用薬の投与状況を確認し、終了日が不明な場合は理由を確認。
        3. データ欠損の場合は、可能な範囲でデータ収集。

Define.xmlの修正候補:
* CM.CMSTDTCのDataTypeについて、Partial Date形式 (YYYY-MM) を許容することをDefinition Description注釈に追加する。
* ValueListDef、ItemDef OID="LB.LBSTRESU" に、LBドメインで使用されている単位が網羅されていないため、必要に応じて修正する。

クエリ:
* 患者ID: 01-701-1028
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: AE.AESTDTC = 2013-07-01, EX.EXSTDTC = 2013-07-19
        * 医療機関への問い合わせ文面:
            患者ID: 01-701-1028
            有害事象(APPLICATION SITE ERYTHEMA)の開始日(2013-07-01)が、治験薬(XANOMELINE 54mg)の開始日(2013-07-19)より前になっています。
            AE開始日、EX開始日に誤りがないか、カルテ等の記録をご確認いただけますでしょうか。
        * 判断理由: 有害事象と治験薬の因果関係評価に影響を及ぼす可能性があり、データの信頼性を確保するため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD = CK, LB.LBORRES = 317, LBNRIND = HIGH (LBSEQ=142)
        * 医療機関への問い合わせ文面:
            患者ID: 01-701-1028
            WEEK 8の臨床検査値で、CK (Creatine Kinase) が基準値上限を超過 (317 U/L, 基準値上限 198 U/L) しています。
            CK上昇の原因として考えられる事項（患者の合併症、既往歴、併用薬、治験薬との関連性など）、および再検査の実施状況についてご教示ください。
            臨床的に特記事項があれば併せてお知らせください。
        * 判断理由: CK上昇が治験薬の安全性評価に影響を及ぼす可能性があるため、医学的評価と対応を確認するため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMSTDTC (2013-04), CM.CMDTC (2013-07-11)
        * 医療機関への問い合わせ文面:
            患者ID: 01-701-1028
            併用薬(CMSEQ=1, 2)の開始日(CMSTDTC)がデータ収集日(CMDTC)より前になっている件、および日付フォーマットがYYYY-MM形式になっている件について、原資料をご確認いただき、可能な範囲で修正のご協力をお願いできますでしょうか。
        * 判断理由: データ品質の向上
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1028
    逸脱No.: 1
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMTRT = CENTRUM, CM.CMDECOD = UNCODED, CM.CMSTDTC = 2013-04
        逸脱内容: 
            被験者01-701-1028は、治験期間中に併用禁止薬の疑いがあるCENTRUMを併用しています。プロトコルに併用禁止薬リストの明記がないため、現時点ではプロトコル逸脱とは断定できません。
        プロトコル該当箇所: 
            3.8項 Concomitant Therapy, 3.4.2.2項 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list)
        判断理由: 
            CENTRUMはビタミン剤であり、一般的に臨床試験への影響は小さいと考えられます。しかし、プロトコルに詳細な併用禁止薬規定がないため、念のためプロトコル逸脱の疑いとして検出しました。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = HYDROCORTISONE, CM.CMDECOD = HYDROCORTISONE, CM.CMSTDTC = 2013-08-08, CM.CMINDC = "", CMROUTE = "TOPICAL"
        逸脱内容: 
            被験者01-701-1028は、治験期間中に副腎皮質ステロイドであるHYDROCORTISONEを併用しています。CMINDCが空欄のため適応症は不明ですが、CMROUTEがTOPICALであることから外用薬である可能性が示唆されます。ステロイドの使用は治験薬の効果に影響を与える可能性があるため、プロトコル逸脱の疑義として検出しました。
        プロトコル該当箇所: 
            3.8項 Concomitant Therapy, 3.4.2.2項 Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list)
        判断理由: 
            プロトコルに併用禁止薬リストの明記がなく、HYDROCORTISONE（全身性コルチコステロイド）が併用禁止薬に該当するか不明です。しかし、ステロイドの使用は治験薬の効果に影響を与える可能性があるため、医療機関への確認が必要と判断しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=MCV, LB.VISIT=SCREENING 1, LBORRES=104 fL, LBORNRLO=80 fL, LBORNRHI=100 fL, LBNRIND=HIGH
        逸脱内容: 
            被験者01-701-1028のスクリーニング1回目のMCV値が基準範囲上限を超過しています。プロトコルで規定された除外基準に抵触する可能性があります。
        プロトコル該当箇所: 
            3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.
        判断理由: 
            プロトコル除外基準EXCL27では、基準値上限を超える臨床検査値が除外基準として規定されています。MCVが除外基準の「etc.」に含まれるか不明なため、プロトコル逸脱の疑いとして検出しました。ただし、MCV逸脱は軽微であり、臨床的意義の判断が必要となるため、臨床試験結果への影響はMinorと判断しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Major
        変数名と値: LBTESTCD: CK, VISIT: WEEK 8, LBORRES: 317, LBORNRLO: 22, LBORNRHI: 198, LBNRIND: HIGH
        逸脱内容: 
            被験者01-701-1028のWEEK 8のCreatine Kinase (CK) 値が基準値上限を超過(317 U/L, 基準値上限: 198 U/L)。プロトコルで規定された除外基準に抵触する可能性があります。
        プロトコル該当箇所: 
            3.4.2.2. Exclusion Criteria [27b]
        判断理由: 
            プロトコル除外基準EXCL27では、基準値上限を超える臨床検査値が除外基準として規定されています。LBドメインのデータにおいて、被験者01-701-1028のWEEK 8のCK値が基準値上限を超過しているため、プロトコル逸脱の可能性があると判断しました。CK値異常は患者の安全性に関わる可能性があるため、臨床試験結果への影響度合いはMajorと判断しました。

クエリ:
    患者ID: 01-701-1028
        クエリNo.: 1
            臨床試験結果への影響度合い: Minor
            変数名と値: CM.CMTRT = HYDROCORTISONE
            医療機関への問い合わせ文面: 
                治験参加者 01-701-1028 に併用されているヒドロコルチゾンについて、詳細な情報を確認したく、ご回答をお願いいたします。
                1.  ヒドロコルチゾンの投与経路と剤形を教えてください。（外用薬でしょうか？内服薬でしょうか？）
                2.  ヒドロコルチゾンの投与目的（適応症）を教えてください。
                3.  治験責任医師は、本併用がプロトコルに抵触しない、あるいは臨床試験結果に影響を与えないと判断されていますでしょうか。併せてご見解をお聞かせください。
            判断理由: 
                併用薬HYDROCORTISONEの治験への影響を評価するために、投与経路、適応症、治験責任医師の見解を確認する必要があるため。

        クエリNo.: 2
            臨床試験結果への影響度合い: Major
            変数名と値: LBTESTCD: CK, VISIT: WEEK 8, LBORRES: 317, LBORNRLO: 22, LBORNRHI: 198, LBNRIND: HIGH
            医療機関への問い合わせ文面: 
                治験参加者 01-701-1028 のWEEK 8の臨床検査値データについてお伺いします。 Laboratory Tests Resultsデータセット（LBドメイン）のWEEK 8 (VISITNUM=8) において、Creatine Kinase (CK) の検査値が基準範囲上限 (198 U/L) を超える 317 U/L と報告されています。
                プロトコル 3.4.2.2 Exclusion Criteria [27b] に「Laboratory test values exceeding the Lilly Reference Range III for the patient's age in any of the following analytes: creatinine, total bilirubin, SGOT, SGPT, etc.」という除外基準の記載がありますが、CK はこの「etc.」に含まれるか、あるいは別の基準値超過として除外基準に該当する可能性はありますでしょうか。
                本検査値について、臨床的意義についてご評価頂けますでしょうか。治験への参加継続について、治験責任医師の見解を伺いたく存じます。
            判断理由: 
                CK値が基準値上限を超過しているデータは、プロトコル除外基準に抵触する可能性があり、プロトコル逸脱に該当するか確認が必要である。また、CK値異常は患者の安全性に関わる可能性があるため、医療機関への問い合わせが必要と判断しました。

# 01-701-1387
## Task1: Clinical Review Results
患者ID: 01-701-1387
* 2014年02月23日 (Day -17): スクリーニング1回目のバイタルサイン測定（臥位）で拡張期血圧146 mmHgと高値。併用薬ECOTRIN開始。
* 2014年03月18日 (Day 7): 軽度DIARRHOEA（下痢）、HYPERHIDROSIS（多汗症）発現。
* 2014年03月25日 (Day 14): 2週目の検査でナトリウム146 mEq/Lと高値。PROTOCOL VIOLATION、FINAL LAB VISITと診断され、治験中止。
* 2014年08月27日 (Day 169): 最終評価RETRIEVAL VISIT。ADAS-COGスコアはベースラインから59まで悪化、CIBICはMODERATE WORSENINGと評価。バイタルサイン測定（臥位）で収縮期血圧175mmHgと高値。FINAL RETRIEVAL VISITと診断。

---

患者ID: 01-701-1387
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: DS.DSTERM=PROTOCOL VIOLATION, DSDECOD=PROTOCOL VIOLATION
    * 医療機関への問い合わせ文面:
        プロトコル逸脱の内容、詳細な状況、臨床試験結果に与える影響についてご教示ください。
    * 判断理由:
        治験中止理由がプロトコル違反であり、臨床試験のデータ解釈に影響を与える可能性があるため、詳細な内容を把握し、データの信頼性を評価する必要がある。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: VS.VSTESTCD=SYSBP, VS.VSORRES=175 mmHg (RETRIEVAL, SUPINE)
    * 医療機関への問い合わせ文面:
        RETRIEVAL時のバイタルサイン測定で、臥位での収縮期血圧が175mmHgと高値でした。測定時の状況、高血圧の原因、既往歴、降圧剤の使用状況、対応についてご教示ください。
    * 判断理由:
        収縮期血圧175mmHgは高血圧クリーゼに相当する可能性があり、患者の安全性に影響を与える可能性があるため、背景情報と対応を確認する必要がある。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD=SODIUM, LB.LBORRES=146 mEq/L (WEEK 2)
    * 医療機関への問い合わせ文面:
        WEEK 2の検査値でナトリウム高値（146 mEq/L）が確認されました。再検査の実施有無、臨床的に特記すべき事項、実施された対応についてご教示ください。
    * 判断理由:
        ナトリウム高値は医学的に注意が必要な所見であり、治験薬との関連性や患者の安全性に影響がないか確認するため、医療機関への問い合わせが必要と判断した。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM=DIARRHOEA, AE.AESEV=MILD, AE.AEREL=REMOTE, AE.AEOUT=RECOVERED/RESOLVED
    * 医療機関への問い合わせ文面:
        有害事象DIARRHOEA（下痢）について、発現状況、治験薬との因果関係、重症度、転帰について、治験責任医師の見解を伺いたく存じます。
    * 判断理由:
        DIARRHOEA（下痢）は治験薬との関連性がREMOTEと評価されているものの、有害事象として報告されており、詳細な状況を確認することで、今後の安全性評価に資すると考えられるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, EX.EXSTDTC, VS.VSTESTCD (DIABP), LB.LBTESTCD (SODIUM), CM.CMDTC, CM.CMSTDTC, CM.CMENDTC

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC=2014-03-18, EX.EXSTDTC=2014-03-12
    * 矛盾の内容: AEドメインの有害事象開始日が、EXドメインの治験薬投与開始日より先行しており、時系列に矛盾が認められます。
    * 問題点の原因（推測）: データ入力時の誤り、または有害事象開始日の記録誤りの可能性。
    * 対応策（提案）: 医療機関にAE開始日とEX開始日の記録の正確性を確認し、必要であれば修正を依頼してください。

* 問題No.: 2
    * 変数名と値: VS.VSTESTCD=DIABP, VS.VSORRES=146 mmHg (SCREENING 1, SUPINE)
    * 矛盾の内容: SCREENING 1の仰臥位での拡張期血圧が146 mmHgと異常高値を示しています。他の測定日では正常範囲内であり、単独で突出した高血圧値です。
    * 問題点の原因（推測）: データ入力時の誤り、測定時のノイズ、または一過性の血圧上昇の可能性。
    * 対応策（提案）:
        1. VSドメインのデータ入力値を再確認してください。
        2. 医療機関に問い合わせ、患者のベースライン時の血圧値と測定状況（体位、測定環境など）を確認してください。

* 問題No.: 3
    * 変数名と値: LB.LBTESTCD=SODIUM, LB.LBSTRESN=146 mmol/L, LB.LBSTNRHI=145 mmol/L (WEEK 2)
    * 矛盾の内容: WEEK 2のナトリウム検査値が146 mmol/Lと、Define.xmlに定義された基準範囲上限値 (145 mmol/L) をわずかに超過しています。
    * 問題点の原因（推測）: データ入力時の誤り、または患者の生理的な変動による一過性の高値の可能性。
    * 対応策（提案）:
        1. LBドメインのデータ入力値を再確認してください。
        2. 医療機関に問い合わせ、患者の臨床状態（脱水症状の有無等）を確認してください。
        3. 必要に応じて再検査を実施するか、医学的レビューを依頼してください。

* 問題No.: 4
    * 変数名と値: CM.CMDTC = 2014-02-23, CM.CMSTDTC = 2012 (1行目)
    * 矛盾の内容: 併用薬CMドメインにおいて、データ収集日 (CMDTC) が2014年であるのに対し、併用薬開始日 (CMSTDTC) が2012年となっており、時間軸の整合性に矛盾が認められます。
    * 問題点の原因（推測）: データ入力時の誤り、またはCMSTDTCの年情報誤りの可能性。
    * 対応策（提案）: CMドメインのCMDTCとCMSTDTCの日付の妥当性をデータ作成者に確認し、必要に応じて修正してください。

* 問題No.: 5
    * 変数名と値: CM.CMENDTC = null (全レコード)
    * 矛盾の内容: 併用薬CMドメインのCMENDTC（併用薬終了日）がすべてのレコードで欠損しています。
    * 問題点の原因（推測）: 併用薬が継続中のため、CMENDTCが未入力である可能性。またはデータ入力のルールが不明確である可能性。
    * 対応策（提案）: CMENDTCが欠損している理由を確認し、意図的な欠損であるか、データ入力ルールの見直しが必要か検討してください。

クエリ:
* 患者ID: 01-701-1387
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC=2014-03-18, EX.EXSTDTC=2014-03-12
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1387 の有害事象 (AETERM: DIARRHOEA, AESEQ: 1) の開始日 (AESTDTC: 2014-03-18) が、治験薬の投与開始日 (EXSTDTC: 2014-03-12) より後になっています。AE開始日の記録に誤りがないか、治験薬投与開始日の記録に誤りがないか、あるいは両データに記録誤りがないか確認してください。記録に誤りがある場合は、正しい日付に修正してください。
        * 判断理由: 有害事象と治験薬投与の時系列関係の矛盾は、データ信頼性、因果関係評価に影響するため、医療機関への確認と修正が重要。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=SODIUM, LB.VISIT=WEEK 2, LB.LBSTRESN=146 mmol/L
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1387 の WEEK 2 におけるナトリウム検査値 (LBTESTCD=SODIUM, LBSTRESN=146 mmol/L) が基準範囲上限 (LBSTNRHI=145 mmol/L) をわずかに超過しています。データ入力時の誤りの可能性も考えられますが、念のため、患者様の臨床状態、特に脱水症状やナトリウム値に影響を与える可能性のある疾患の有無、および他の関連する検査値に異常がないかをご確認いただけますでしょうか。
        * 判断理由: 基準範囲をわずかに超過しているのみで臨床的な影響は小さいと予想されるが、念のため医療機関に確認することが望ましい。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: VS.VSTESTCD=DIABP, VS.VSORRES=146 mmHg (SCREENING 1, SUPINE)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1387 のスクリーニング1 (SCREENING 1) のバイタルサイン測定において、仰臥位での拡張期血圧 (VS.VSTESTCD=DIABP, VSPOS=SUPINE) が146 mmHgと異常高値を示しています。測定時の患者の状態（緊張、体位、測定方法など）と、その後の血圧推移についてご教示ください。この血圧値がプロトコル逸脱に該当するか、治験継続に影響がないかについてもご意見を伺いたいです。
        * 判断理由: スクリーニング時の血圧異常値は、患者組み入れ基準や安全性評価に関わる可能性があり、臨床的に重要。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMDTC = 2014-02-23, CM.CMSTDTC = 2012 (1行目)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1387 の併用薬データについて、以下の点をご確認ください。
            1.  CMドメインのCMDTC（データ収集日）が2014年であるのに対し、CMSTDTC（併用薬開始日）が2012年となっています。CMSTDTCの日付は正しいですか？正しい場合、2012年から2014年の間にECOTRINを継続して服用していたという理解で良いですか？
            2.  CMENDTC（併用薬終了日）がすべてのレコードで欠損しています。併用薬は継続中であり終了日が未定ということで良いですか？
        * 判断理由: 併用薬開始日とデータ収集日の矛盾はデータの信頼性を損なうため、医療機関への確認と修正が重要。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMTRT=ECOTRIN, AE.AETERM=DIARRHOEA
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1387 において、併用薬として ECOTRIN (アスピリン) がWeek2まで継続投与されています。また、同患者には治験薬投与期間中に下痢 (DIARRHOEA) の有害事象が発現しています。因果関係 (AEREL) は "REMOTE" (関連性なし) と評価されていますが、念のため、併用薬と有害事象の関連について、医療機関の見解をご確認いただけますでしょうか。
        * 判断理由: 因果関係は低いと評価されているものの、併用薬と有害事象の関連性を明確にするため、医療機関への確認が望ましい。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1387
    逸脱No.: 1
        臨床試験結果への影響度合い: Critical
        変数名と値: CMTRT=ECOTRIN, CMSTDTC=2012, CMDTC=2014-03-25
        逸脱内容: 被験者01-701-1387は、併用禁止薬である可能性のあるECOTRIN（アスピリン）を、試験期間中に複数回にわたって併用している。CM.CMSTDTCが2012年と記録されており、治験薬投与開始日（DM.RFXSTDTC=2014-03-12）よりも前からECOTRINを服用している可能性がある。ECOTRINの併用はプロトコルで禁止されているか、または注意が必要な薬剤に該当する可能性があり、患者の安全性と試験結果に影響を与える可能性がある。
        プロトコル該当箇所: プロトコルに併用禁止薬リストの記載があるか確認が必要
        判断理由: ECOTRIN（アスピリン）は、特に高齢者においては出血リスクを高める可能性があり、臨床試験の安全性に重大な影響を与える可能性がある。プロトコルで併用が禁止されている場合、明確なプロトコル逸脱となる。また、CMドメインのデータにおいて、併用薬の開始日がデータ収集日よりも未来になっているという時間軸の矛盾が認められる。データ入力ミスが疑われる。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: DSDECOD=PROTOCOL VIOLATION, DSDTC=2014-03-25, VISIT=WEEK 2
        逸脱内容: DSドメインにプロトコル逸脱の記録があり、被験者01-701-1387において、WEEK 2のVISIT時に「PROTOCOL VIOLATION」が発生したことが記録されている。具体的な逸脱内容は不明であり、臨床試験の実施および評価項目に影響を与えている可能性がある。
        プロトコル該当箇所: プロトコル逸脱に関する定義、報告手順 (プロトコルに詳細な記載がない場合は、一般的な手順に準拠)
        判断理由: プロトコル逸脱は、臨床試験のデータ品質や信頼性を損なう可能性があり、詳細な内容を確認する必要がある。特に、WEEK 2という比較的早期の段階で発生しているため、その後の試験結果に影響を与えている可能性も考慮する必要がある。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LBTESTCD=SODIUM, LBNRIND=HIGH, VISIT=WEEK 2, LBDTC=2014-03-25T10:40
        逸脱内容: 被験者01-701-1387において、WEEK 2の検査で血中ナトリウム値が基準値上限を超えている（HIGH）。血中ナトリウム値の一過性の上昇は、臨床的に大きな問題とならない場合もある。
        プロトコル該当箇所: 臨床検査値異常時の対応に関する規定 (プロトコルに詳細な記載がない場合は、一般的な手順に準拠)
        判断理由: 血中ナトリウム値の一過性の上昇は、臨床的に大きな問題とならない場合もあるが、他の逸脱事象（PROTOCOL VIOLATION）と同時期に発生していること、またECOTRINの併用も考慮すると、念のため臨床的な意義を確認することが望ましい。

クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: CMTRT=ECOTRIN, CMSTDTC=2012, DSDECOD=PROTOCOL VIOLATION
    医療機関への問い合わせ文面:
    治験実施医療機関の担当者様

    CDISCPILOT01試験、患者ID: 01-701-1387 において、DSドメインに「PROTOCOL VIOLATION」のイベントが記録され、また併用薬としてECOTRIN（アスピリン）が記録されています。

    つきましては、大変お手数ですが、下記の点についてご回答いただけますようお願いいたします。

    1.  DSドメインに記録されたプロトコル逸脱（DSTERM = PROTOCOL VIOLATION）について、逸脱の詳細な内容、発生日時、関連するプロトコル条項、臨床試験結果に与える可能性のある影響についてご教示ください。
    2.  被験者01-701-1387に併用されているECOTRIN（アスピリン）の投与理由と、プロトコルにおける併用薬規定への適合性についてご説明ください。ECOTRINはプロトコルで併用が禁止されている薬剤、または注意が必要な薬剤に該当する可能性があります。
    3.  併用されているECOTRINの開始日が2012年と記録されていますが、治験薬投与開始日（2014年3月12日）よりも前になっている理由をご教示ください。CMSTDTC、CMDTC、CMENDTCの正しい日付をご確認ください。
    4.  プロトコル逸脱とECOTRINの併用に関連性がある場合、詳細をご教示ください。
    5.  現在、プロトコル逸脱に対して、是正措置は講じられていますでしょうか。もし是正措置が講じられている場合、その内容についてご教示ください。

    ご多忙のところ恐縮ですが、ご回答よろしくお願いいたします。

    判断理由: ECOTRINの併用状況とプロトコル逸脱の関連性を包括的に確認し、データ

# 01-701-1034
## Task1: Clinical Review Results
患者ID: 01-701-1034
* 2014年06月24日 (Day -7): スクリーニング1にて、併用薬CALCIUM, ESTROGEN NOS, EX-LAX, IRON, LEVOTHROID, VITAMIN C, VITAMIN E が開始されました。検査値Anisocytes(ANISO) 異常値 (1 NO UNITS)、Ery. Mean Corpuscular Volume (MCV) 高値 (102 fL, 基準値: 80-100 fL)、MCH高値、TSH低値 (0.27 uIU/mL, 基準値: 0.32-5 uIU/mL) が確認されました。
* 2014年07月15日 (Day 15): WEEK 2にて、検査値ALP低値 (34 U/L, 基準値: 35-115 U/L)、Macrocytes(MACROCY) 異常値 (1 NO UNITS)、Ery. Mean Corpuscular Volume (MCV) 高値 (106 fL, 基準値: 80-100 fL) が確認されました。
* 2014年07月29日 (Day 29): WEEK 4にて、検査値ALP低値 (36 U/L, 基準値: 35-115 U/L)、Anisocytes(ANISO) 異常値 (1 NO UNITS)、Erythrocytes (RBC) 低値 (3.80 MILL/uL, 基準値: 3.9-5.5 MILL/uL)、Ery. Mean Corpuscular Volume (MCV) 高値 (103 fL, 基準値: 80-100 fL) が確認されました。
* 2014年08月11日 (Day 42): WEEK 6にて、検査値ALP低値 (33 U/L, 基準値: 35-115 U/L)、Anisocytes(ANISO) 異常値 (1 NO UNITS)、Ery. Mean Corpuscular Volume (MCV) 高値 (103 fL, 基準値: 80-100 fL) が確認されました。
* 2014年08月26日 (Day 57): WEEK 8にて、検査値ALP低値 (29 U/L, 基準値: 35-115 U/L)、Ery. Mean Corpuscular Volume (MCV) 高値 (101 fL, 基準値: 80-100 fL) が確認されました。
* 2014年09月25日 (Day 87): WEEK 12にて、併用薬HYDROCORTISONEが開始されました。検査値ALP低値 (34 U/L, 基準値: 35-115 U/L)、Ery. Mean Corpuscular Volume (MCV) 高値 (101 fL, 基準値: 80-100 fL) が確認されました。有害事象としてApplication Site Pruritusが発現しました。
* 2014年10月21日 (Day 113): WEEK 16にて、検査値ALP低値 (34 U/L, 基準値: 35-115 U/L)、Ery. Mean Corpuscular Hemoglobin (MCH) 高値 (35 pg, 基準値: 26-34 pg)、Ery. Mean Corpuscular Volume (MCV) 高値 (103 fL, 基準値: 80-100 fL)、Macrocytes(MACROCY) 異常値 (1 NO UNITS) が確認されました。
* 2014年11月18日 (Day 141): WEEK 20にて、検査値ALP低値 (31 U/L, 基準値: 35-115 U/L)、Ery. Mean Corpuscular Hemoglobin (MCH) 高値 (33 pg, 基準値: 26-34 pg)、Ery. Mean Corpuscular Volume (MCV) 高値 (102 fL, 基準値: 80-100 fL)、Macrocytes(MACROCY) 異常値 (1 NO UNITS) が確認されました。有害事象としてMalignant Hypertensionが発現しました。
* 2014年12月17日 (Day 170): WEEK 24にて、検査値Ery. Mean Corpuscular Hemoglobin (MCH) 高値 (37 pg, 基準値: 26-34 pg)、Ery. Mean Corpuscular Volume (MCV) 高値 (102 fL, 基準値: 80-100 fL)、Sodium 低値 (134 mEq/L, 基準値: 135-145 mEq/L)、Erythrocytes (RBC) 低値 (3.50 MILL/uL, 基準値: 3.9-5.5 MILL/uL)、Macrocytes(MACROCY) 異常値 (1 NO UNITS)、Anisocytes(ANISO) 異常値 (1 NO UNITS) が確認されました。
* 2014年12月30日 (Day 183): WEEK 26にて、検査値ALP低値 (27 U/L, 基準値: 35-115 U/L)、Anisocytes(ANISO) 異常値 (1 NO UNITS)、Ery. Mean Corpuscular Hemoglobin (MCH) 高値 (35 pg, 基準値: 26-34 pg)、Ery. Mean Corpuscular Volume (MCV) 高値 (102 fL, 基準値: 80-100 fL)、Sodium 低値 (134 mEq/L, 基準値: 135-145 mEq/L)、Erythrocytes (RBC) 低値 (3.70 MILL/uL, 基準値: 3.9-5.5 MILL/uL)、Thyrotropin (TSH) 低値 (0.27 uIU/mL, 基準値: 0.32-5 uIU/mL) が確認されました。

---
患者ID: 01-701-1034
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD = ALP, LBORRES=27-34 U/L (Low); LB.LBTESTCD = ANISO, LBORRES=1 NO UNITS (Abnormal); LB.LBTESTCD = MACROCY, LBORRES=1 NO UNITS (Abnormal); LB.LBTESTCD = RBC, LBORRES=3.50-3.80 MILL/uL (Low); LB.LBTESTCD = MCH, LBORRES=35-37 pg (High); LB.LBTESTCD = MCV, LBORRES=101-106 fL (High); LB.LBTESTCD = SODIUM, LBORRES=134 mEq/L (Low); LBTESTCD=TSH, LBORRES=0.27 uIU/mL (Low)
    * 医療機関への問い合わせ文面: 患者ID 01-701-1034 のALP低値、Anisocytes異常値、Macrocytes異常値、RBC低値、MCH高値、MCV高値、Sodium低値、TSH低値について、医学的に特記すべき事項、あるいは治験薬との関連性についてご教示ください。
    * 判断理由: 複数の検査項目で基準値外れが認められ、医学的妥当性の観点から臨床試験結果に影響を与える可能性があるため、医療機関への問い合わせが必要と判断しました。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: VS.VSTESTCD = SYSBP, VS.VSORRES > 180 (複数回); VS.VSTESTCD = DIABP, VS.VSORRES > 100 (複数回)
    * 医療機関への問い合わせ文面: 患者ID 01-701-1034 のバイタルサインSYSBP, DIABPについて、Week24まで高血圧の傾向が認められています。医学的なリスクと、治験薬との関連性についてご教示ください。
    * 判断理由: 治験期間中に高血圧の傾向が継続しており、患者の安全性に懸念があるため、医療機関への問い合わせが必要と判断しました。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM = APPLICATION SITE PRURITUS, AE.AEREL = PROBABLE; AE.AETERM = MALIGNANT HYPERTENSION, AE.AEREL = POSSIBLE
    * 医療機関への問い合わせ文面: 患者ID 01-701-1034 に報告されている有害事象 APPLICATION SITE PRURITUS, MALIGNANT HYPERTENSION について、詳細な症状、重症度、治験薬との因果関係、処置、転帰についてご教示ください。
    * 判断理由: 報告されている有害事象の内容と治験薬との関連性を確認し、医学的妥当性を評価する必要があるため、医療機関への問い合わせが必要と判断しました。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CMSTDTC = 1960 (ESTROGEN NOS, CMSEQ=2)
    * 医療機関への問い合わせ文面: 併用薬ESTROGEN NOS (CMSEQ=2) の開始日について、1960年で正しいか、誤りであれば正しい日付を教えてください。
    * 判断理由: 併用薬の開始日は患者背景や既往歴を評価する上で重要な情報であり、誤りの可能性があるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMDTC, CM.CMSTDTC, CM.CMENDTC, CM.CMSTDY, CM.CMENDY, MH.MHTERM, LB.LBORRES

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMSTDTC = 2012, 1960 (複数レコード)
    * 矛盾の内容: 併用薬開始日（CMSTDTC）がデータ収集日（CMDTC）よりも過去の日付（2012年, 1960年）で記録されており、時間軸の整合性が取れていない。
    * 問題点の原因（推測）: データ入力時の誤り、またはCMSTDTCの年のみが誤っている可能性。
    * 対応策（提案）: 医療機関にCM開始日（CMSTDTC）が正しいか確認する。

* 問題No.: 2
    * 変数名と値: CM.CMDTCとCM.CMSTDTC (複数のレコードでCMDTC > CMSTDTCとなっている)
    * 矛盾の内容: 併用薬CM.CMDTC（データ収集日）がCM.CMSTDTC（併用薬開始日）より未来の日付になっている。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータ収集日の誤りの可能性。
    * 対応策（提案）: 医療機関にCMDTCとCMSTDTCの日付が正しいか確認し、必要に応じて修正を依頼してください。

* 問題No.: 3
    * 変数名と値: CM.CMENDTC = null (すべてのレコード)
    * 矛盾の内容: ほとんどのレコードでCM.CMENDTC（Concomitant Medicationの終了日）が欠損しており、併用薬の投与状況が不明確。
    * 問題点の原因（推測）: データ入力時の欠損、またはConcomitant Medicationが継続中のため終了日が未入力。
    * 対応策（提案）: CM.CMENDTCが欠損している理由を確認し、必要に応じて終了日を追記するか、欠損理由を示すコードリストを適用することを検討してください。

* 問題No.: 4
    * 変数名と値: CM.CMSTDY = null, CM.CMENDY = null (すべてのレコード)
    * 矛盾の内容: すべてのレコードでCM.CMSTDY（Concomitant Medication開始日のStudy Day）とCM.CMENDY（Concomitant Medication終了日のStudy Day）が欠損。日付情報が存在するにもかかわらず、Study Dayが算出されていない。
    * 問題点の原因（推測）: Study Dayの算出処理の未実施、またはデータ変換時のエラー。
    * 対応策（提案）: CM.CMSTDYとCM.CMENDYを算出する処理を実施し、データを追記してください。

* 問題No.: 5
    * 変数名と値: CM.CMTRT = ESTROGEN NOS, MH.MHTERM = HYSTERECTOMY
    * 矛盾の内容: CMドメインでエストロゲン製剤が併用薬として記録されている一方で、MHドメインに子宮摘出術（HYSTERECTOMY）の既往歴が記録されており、医学的に矛盾する可能性がある。
    * 問題点の原因（推測）: データ入力時の誤り、または併用薬と既往歴の記録の誤り、あるいは医学的に妥当な理由がある可能性。
    * 対応策（提案）: 医療機関に併用薬と既往歴の記録が正しいか、医学的に妥当な理由があるか確認する。

* 問題No.: 6
    * 変数名と値: LB.LBTESTCD = ALP, LBORRES = 34, LBORNRLO = 35, LBNRIND = LOW
    * 矛盾の内容: ALP (アルカリフォスファターゼ) 検査において、LBORRES (34 U/L) がLBORNRLO (35 U/L) の下限基準値よりも低いにもかかわらず、LBNRIND (Reference Range Indicator) が "LOW" となっている。
    * 問題点の原因（推測）: データ入力時の誤り、またはLBNRINDの判定ロジックの誤り。
    * 対応策（提案）: LB検査値と基準範囲、LBNRINDの判定が正しいか確認する。

クエリ:
患者ID: 01-701-1034
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMSTDTC = 2012, 1960 (複数レコード)
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 の併用薬情報について、開始日（CMSTDTC）がデータ収集日（CMDTC）より過去となるデータが複数あります。CMドメインのデータと記録を照合し、CM開始日の日付に誤りがないか確認ください。
        * CMドメイン全レコード
    * 判断理由: 併用薬の開始日は、データ解釈において重要な情報であり、誤っている場合、臨床試験の評価に影響を及ぼす可能性があるため。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMTRT = ESTROGEN NOS, MH.MHTERM = HYSTERECTOMY
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 の併用薬と既往歴について、CMドメインにエストロゲン製剤の使用、MHドメインに子宮摘出術の既往歴が記録されています。医学的に併用が矛盾する可能性があるため、併用薬と既往歴の記録に誤りがないか、または医学的に併用が妥当である理由についてご回答ください。
    * 判断理由: 併用薬と既往歴の矛盾は、患者の安全性やデータ解釈に影響を与える可能性があるため、重要度の高いクエリと判断しました。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = ALP, LBORRES = 34, LBORNRLO = 35, LBNRIND = LOW
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 のALP検査値について、検査結果 (LBORRES) が基準範囲 (LBORNRLO) を下回っているにもかかわらず、Reference Range Indicator (LBNRIND) が "LOW" となっています。LB検査値、基準範囲、LBNRIND判定の記録に誤りがないかご確認ください。
    * 判断理由: LB検査値とLBNRINDの矛盾は、データの正確性に疑義を生じさせる軽微な問題であるため。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMENDTC = null (すべてのレコード)
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 の併用薬データについて、Medication終了日（CMENDTC）がすべてのレコードで欠損しています。併用薬の投与状況を確認し、終了日が不明な場合は理由をご教示ください。
    * 判断理由: CMENDTCの欠損は、データの完全性に関わる軽微な問題であるため。

* クエリNo.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMSTDTC, CM.CMDTC (日付の前後関係の矛盾)
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 の併用薬データについて、データ収集日 (CMDTC) が投薬開始日 (CMSTDTC) よりも未来になっている事例が複数件あります。日付の記録に誤りがないか、再度確認をお願いします。
    * 判断理由: データ入力時の単純な誤りの可能性が高く、データの信頼性を損なう軽微な問題であるため。

* クエリNo.: 6
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMSTDY, CM.CMENDY (null)
    * 医療機関への問い合わせ文面: 
        治験参加者ID 01-701-1034 の併用薬データについて、CMSTDYとCMENDYがNullになっています。可能であれば、Study Dayを追記ください。
    * 判断理由: データ解析の利便性に関わる軽微な問題
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1034
    逸脱No.: 1
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC, CM.CMDTC (CMSEQ: 2, 3, 4, 5, 6, 7, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96)
        逸脱内容: 併用薬ドメイン（CM）において、複数のレコードで併用薬開始日 (CMSTDTC) がデータ収集日 (CMDTC) より過去の日付で記録されている。具体的には、CALCIUM、IRON、LEVOTHROID、VITAMIN C、VITAMIN E、ESTROGEN NOSなどの併用薬でCMSTDTCがCMDTCよりも古い日付となっている。データ入力時の誤り、または過去の記録を誤って登録した可能性が考えられる。
        プロトコル該当箇所: 3.9.5. Appropriateness and Consistency of Measurements, データマネジメント手順書 (データ入力に関する一般的な注意)
        判断理由: SDTMデータ標準では日付の整合性が重要であり、CMドメインにおける日付の矛盾はデータ品質上の問題となる。ただし、これらの併用薬は一般的なサプリメントや基礎疾患治療薬であり、本試験の主要評価項目や患者安全性に直接的な影響を与える可能性は低いと判断されるため、臨床試験結果への影響度はMinorとした。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = ESTROGEN NOS, DM.SEX = F, DM.AGE = 77, CM.CMINDC = PROPHYLAXIS OR NON-THERAPEUTIC USE, CM.CMCLAS = UNCODED
        逸脱内容: 被験者01-701-1034は77歳の女性患者であり、併用薬としてエストロゲン製剤（ESTROGEN NOS）を使用している。併用目的は「PROPHYLAXIS OR NON-THERAPEUTIC USE（予防または非治療的使用）」と記録されている。プロトコル上、閉経後女性は組み入れ可能であるが、併用禁止薬リストにエストロゲン製剤に関する明記された規定はない。しかし、エストロゲン製剤の種類、投与量、投与期間、併用目的の詳細が不明であり、本試験の評価項目である認知機能や安全性に影響を与える可能性がある。
        プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [1], 3.4.2.2. Exclusion Criteria [31b], 3.8 Concomitant Therapy
        判断理由: プロトコル上、閉経後女性の組み入れは許可されているものの、エストロゲン製剤の使用に関する規定が不明確である。また、エストロゲン製剤が認知機能に与える影響は医学的に無視できない可能性があり、本試験の主要評価項目に影響を及ぼす懸念がある。さらに、併用目的が「PROPHYLAXIS OR NON-THERAPEUTIC USE」と予防的な使用である点も、医学的妥当性の観点から懸念される。これらの理由から、プロトコル逸脱の疑いありと判断し、臨床試験結果への影響度合いはMajorとした。

クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: CM.CMTRT = ESTROGEN NOS, DM.SEX = F, DM.AGE = 77, CM.CMINDC = PROPHYLAXIS OR NON-THERAPEUTIC USE
    医療機関への問い合わせ文面: 
    治験責任医師殿

    CDISCPILOT01試験、患者ID: 01-701-1034の併用薬「ESTROGEN NOS」について、以下の点についてご照会いたします。

    1.  **併用薬の詳細情報:**
        *   エストロゲン製剤の具体的な製品名
        *   投与量、投与経路、投与開始日、投与期間
        *   併用理由、医学的妥当性

    2.  **プロトコルとの整合性:**
        *   併用薬「ESTROGEN NOS」が、プロトコル3.4.2.2 Exclusion Criteria [31b] で規定されている併用禁止薬リストに該当するかどうか。
        *   該当しない場合、プロトコルで併用が禁止されていない薬剤でも、治験薬や評価項目に影響を与える可能性がある薬剤の併用は、プロトコル逸脱に該当するという解釈で相違ないか。

    3.  **治験薬および評価項目への影響:**
        *   併用薬「ESTROGEN NOS」が、本試験の治験薬および評価項目（特に認知機能評価）に与える影響に関する医師の見解。
        *   臨床試験結果の解釈に影響を与える可能性について。

    4.  **治験審査委員会への確認:**
        *   本症例におけるエストロゲン製剤の併用について、プロトコル逸脱に該当するかどうか、治験審査委員会の見解を伺いたい。

    ご多忙の折とは存じますが、本症例の評価のため、ご回答いただけますようお願い申し上げます。

    判断理由: プロトコル逸脱の疑いを明確にし、患者の安全性と試験データの信頼性を確保するため、医療機関へのクエリ発行が必要と判断した。クエリ内容としては、併用薬の詳細情報、プロトコルとの整合性、治験薬および評価項目への影響、治験審査委員会の見解など、プロトコル逸脱の判断に必要な情報を網羅的に問い合わせる必要があるため。また、併用薬がプロトコルに抵触する場合、臨床試験結果に重大な影響を与える可能性があるため、クエリの重要度をMajorとした。

# 01-701-1146
## Task1: Clinical Review Results
**1. 症例サマリー**

**患者ID:** 01-701-1146

* 2008年 (Day -13): スクリーニング1回目より前から、BECONASE (2 PUFF, PRN, NASAL)、DOCUSATE (2 TABLET, QD, ORAL)、MINERALS NOS (15 TABLET, PRN, ORAL)、MOTRIN (1 TABLET, PRN, ORAL)、MULTIVITAMIN (1 TABLET, QD, ORAL)、PREMARIN (0.625 mg, QD, ORAL)、PROVERA (2.5 ug, QD, ORAL) を併用。
* 2013年05月07日 (Day -7): スクリーニング1回目。ALP（アルカリホスファターゼ）が基準値下限を下回る低値 (33 U/L)。
* 2013年05月20日 (Day 1): ベースライン。治験薬（XANOMELINE 54mg）を開始。
* 2013年05月21日 (Day 2): PAROXETINE (2 TABLET, TID, ORAL) を併用開始 (2013年05月22日 (Day 3) に中止)。
* 2013年06月01日 (Day 13): 軽度の適用部位刺激感発現。
* 2013年06月03日 (Day 14): 2週。ALPは正常値範囲内となるも、再度基準値下限を下回る低値 (35 U/L)。
* 2013年06月10日 (Day 22): 適用部位紅斑（軽度）および適用部位そう痒症（軽度）発現。HYDROCORTISONE, TOPICAL (1 VIAL, PRN, TOPICAL) を併用開始。
* 2013年06月16日 (Day 28): 4週。ALPは再び基準値下限を下回る低値 (34 U/L)。適用部位紅斑（軽度）および適用部位そう痒症（軽度）が継続。
* 2013年06月22日 (Day 34): 適用部位疼痛（中等度）発現。
* 2013年06月26日 (Day 38): 適用部位刺激感（中等度）および適用部位小胞（中等度）発現。
* 2013年06月30日 (Day 42): 6週。ALPは引き続き基準値下限を下回る低値 (29 U/L)。適用部位紅斑、適用部位そう痒症は中等度に悪化。適用部位疼痛、適用部位刺激感、適用部位小胞も継続中。治験薬を81mgに増量。治験薬をADVERSE EVENTにより中止。
* 2013年07月15日 (Day null): AEフォローアップ。適用部位紅斑、適用部位刺激感、適用部位疼痛、適用部位小胞は未回復/未解決。

---

**2. クエリ**

患者ID: 01-701-1146
* クエリNo.1:
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" (複数の適用部位関連有害事象)
    * 医療機関への問い合わせ文面: 適用部位紅斑、適用部位掻痒感、適用部位疼痛、適用部位刺激感、適用部位小胞といった複数の適用部位関連有害事象が、最終観察日である2013年7月15日まで未回復/未解決と報告されています。これらの有害事象の重症度、持続期間、患者への影響、及び治験薬との因果関係について、詳細な情報をご提供いただけますでしょうか。特に、Grade 3以上の重症度であった有害事象、治験薬との因果関係が「確実」または「可能性大」と判断された有害事象については、その理由と医学的妥当性について詳しくご説明ください。
    * 判断理由: 複数の適用部位関連有害事象が長期にわたり未回復であり、患者のQOL（生活の質）に影響を与えている可能性が考えられます。治験薬との因果関係や重症度によっては、臨床試験の継続や評価に影響を及ぼす可能性があります。
* クエリNo.2:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = "ALP", LB.LBNRIND = "LOW" (アルカリホスファターゼ低値)
    * 医療機関への問い合わせ文面: ALP（アルカリホスファターゼ）が、スクリーニング時からWEEK 6にかけて継続的に基準値下限を下回る低値で推移しています。ALP低値の原因、医学的意義、及び臨床試験への影響についてご説明いただけますでしょうか。
    * 判断理由: ALP低値は、臨床的に大きな懸念事項ではない可能性がありますが、ALP低値が継続している原因を確認し、医学的妥当性を評価する必要があります。
* クエリNo.3:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMTRT = "PAROXETINE", CM.CMSTDTC = "2013-05-21", CM.CMENDTC = "2013-05-22" (パロキセチン併用)
    * 医療機関への問い合わせ文面: 併用薬としてパロキセチンが、CMSTARTDTC="2013-05-21"、CMENDDTC="2013-05-22"と、2日間のみ投与されています。パロキセチンの投与目的、投与期間が2日間と短い理由、および臨床試験への影響についてご説明いただけますでしょうか。
    * 判断理由: パロキセチンの投与期間が非常に短いため、データ入力誤りの可能性があります。投与目的と投与期間を確認し、データの正確性を検証する必要があります。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, CM.CMDTC, CM.CMDECOD, CM.CMENDTC, CM.CMDOSU, CM.CMSTDTC, CM.CMTRT, CM.CMENDY, DS.DSDECOD, DS.DSTERM, EX.EXSTDTC, LBドメインの異常値, 欠損値の理由

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC < EX.EXSTDTC (AE No.1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11)
    * 矛盾の内容: 複数の有害事象において、開始日 (AESTDTC) が治験薬投与開始日 (EX.EXSTDTC) より早い、または同時期。因果関係 (AEREL) が関連ありと評価されているAEも含むため、再評価が必要。
    * 問題点の原因（推測）: データ入力ミス、AEとEXの日付解釈の誤り、または治験薬と無関係なAEの可能性。
    * 対応策（提案）: 医療機関にAEとEXの日付、因果関係を原資料で確認。データ修正と因果関係の再評価を検討。

* 問題No.: 2
    * 変数名と値: CM.CMDTC > CM.CMSTDTC (CMドメイン全般)
    * 矛盾の内容: ほぼ全ての併用薬でデータ収集日 (CMDTC) が開始日 (CMSTDTC) より後。データ収集日と開始日が同じVisitでも同様。
    * 問題点の原因（推測）: データ入力ミス、CMDTCとCMSTDTCの定義誤解、データ収集日の記録方法の誤りの可能性。
    * 対応策（提案）: データマネジメントチーム内でCMDTCとCMSTDTCの定義と入力方法を再確認・修正。医療機関へのデータ再確認も検討。

* 問題No.: 3
    * 変数名と値: CM.CMENDTC (過去の日付、欠損)
    * 矛盾の内容: 併用薬終了日 (CMENDTC) がデータ収集日 (CMDTC) より過去、または欠損。終了日が過去の場合はデータ入力ミス、欠損の場合は投与状況の確認が必要。
    * 問題点の原因（推測）: データ入力ミス、終了日未記録、データ取得時の情報不足。
    * 対応策（提案）: CM.CMENDTCがCMDTCより過去のレコードは原資料確認。欠損レコードは医療機関に終了日、または投与継続状況を確認。

* 問題No.: 4
    * 変数名と値: CM.CMDOSU の単位 (ug, mg)
    * 矛盾の内容: 併用薬の投与単位 (CMDOSU) が "ug" と "mg" で混在。PROVERA (CMSEQ=7) が "ug" 表記だが、一般的に "mg" が妥当。
    * 問題点の原因（推測）: データ入力時の単位選択ミス、Define.xmlと異なる単位使用。
    * 対応策（提案）: 医療機関にPROVERAの投与単位を確認。Define.xmlのCMDOSU定義と整合性確認。

* 問題No.: 5
    * 変数名と値: CM.CMTRT = "UNCODED" (複数レコード)
    * 矛盾の内容: 併用薬名 (CMTRT) が "UNCODED" で薬剤名不明。
    * 問題点の原因（推測）: コーディングエラー、データ取得時の薬剤名不明。
    * 対応策（提案）: 医療機関に問い合わせ、薬剤名特定。

* 問題No.: 6
    * 変数名と値: LB.ALP (Alkaline Phosphatase) のLowフラグ
    * 矛盾の内容: LBドメインのALP検査値が複数回 Low (低い) と判定されている。臨床的にALP低値が問題ないか、または他に原因がないか確認が必要。
    * 問題点の原因（推測）: 患者の特性、または検査値異常の可能性。
    * 対応策（提案）: 
LBドメインのALP検査値について、臨床的に問題がないか、ALP低値となる要因（既往歴、併用薬など）がないか確認する。

クエリの作成:
患者ID: 01-701-1146
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AESTDTC, EX.EXSTDTC, EX.EXENDTC (AE No.1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11)
    * 医療機関への問い合わせ文面:
        治験参加者01-701-1146に発現した有害事象と治験薬投与期間の整合性について、原資料をご確認ください。特に、治験薬との因果関係がProbableまたはPossibleと評価されている以下の有害事象について、発現日が治験薬投与期間以前となっており、矛盾が認められます。
        - APPLICATION SITE ERYTHEMA (AESEQ=1, 2, 5, 7)
        - APPLICATION SITE IRRITATION (AESEQ=3, 11)
        - APPLICATION SITE PAIN (AESEQ=9)
        - APPLICATION SITE PRURITUS (AESEQ=6, 8)
        - APPLICATION SITE VESICLES (AESEQ=10)
        - FATIGUE (AESEQ=4)
        - RASH (AESEQ=1, 2)
        つきましては、上記有害事象の発現日、治験薬投与開始日・終了日について、原資料をご確認いただき、記録に誤りがないかご回答ください。もし記録に誤りがある場合は、修正をお願いいたします。また、治験薬との因果関係について再評価をお願いいたします。
    * 判断理由: 治験薬と有害事象の因果関係評価に重大な影響を与える可能性があり、患者の安全性評価にも関わる重要なデータであるため、早急な確認と修正が必要です。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMTRT = "UNCODED" (複数レコード)
    * 医療機関への問い合わせ文面:
        患者ID 01-701-1146 の併用薬 (CM) ドメインにおいて、薬剤名 (CMTRT) が "UNCODED" となっているレコード (CMSEQ=1, 2, 3, 4, 5, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61) が複数レコードございます。
        大変お手数ですが、原資料をご確認いただき、具体的にどのような薬剤が投与されていたか、薬剤名 (CMTRT) をご回答いただけますでしょうか。
    * 判断理由: 併用薬情報は、患者背景や治験薬との相互作用、安全性評価において重要なデータとなるため、薬剤名の特定が必要です。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMENDTC, CM.CMENDY (欠損レコード、過去の日付レコード)
    * 医療機関への問い合わせ文面:
        患者ID 01-701-1146 の併用薬 (CM) ドメインにおいて、併用薬の終了日 (CMENDTC, CMENDY) が欠損、またはデータ収集日 (CMDTC) より過去になっているレコードが多数ございます。
        つきましては、該当レコード (CMSEQ=1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61) について、併用薬の正確な終了日 (CMENDTC)、または投与継続状況について、原資料をご確認いただきご回答ください。
        終了日が不明な場合は、可能な範囲で結構ですので、投与期間がわかる情報をご提供いただけますでしょうか。
    * 判断理由: 併用薬の投与期間は、データ解析や患者背景を把握する上で重要な情報となるため、可能な限り正確な情報を収集する必要があります。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMDOSU, CM.CMTRT (PROVERA)
    * 医療機関への問い合わせ文面:
        患者ID 01-701-1146 の併用薬 PROVERA (CMSEQ=7) の投与単位 (CMDOSU) が "ug" (マイクログラム) と記録されています。PROVERAの一般的な投与単位は "mg" (ミリグラム) であると認識しておりますが、記録に誤りがないか、
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1146
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMSTDTC, CM.CMENDTC, CM.CMDTC (CMドメインの複数の変数)
        逸脱内容: 併用薬CMドメインにおいて、CMSTDTC（併用薬開始日）とCMENDTC（併用薬終了日）が2008年となっているレコードが複数存在するが、CMDTC（データ収集日）が2013年5月以降となっており、データに時間的な矛盾が生じている。データ入力時の誤りの可能性が考えられる。また、複数の併用薬（DOCUSATE, BECONASE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERA, HYDROCORTISONE, TOPICAL）でCMENDTC（投与終了日）が空欄となっており、投与状況が不明である。
        プロトコル該当箇所: プロトコルには直接的な該当箇所はなし（データ品質管理に関する規定）。Define.xmlのCMドメイン定義、SDTM Concomitant Medications Domainの定義。
        判断理由: CMドメインにおける日付の矛盾と、投与終了日の欠損は、データの信頼性を損なう重大な問題であり、臨床試験の解釈に影響を与える可能性があるため、Majorと判断した。データの正確性確認と、プロトコル遵守状況の確認が必要である。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=ALP, LB.LBNRIND=LOW (臨床検査値)
        逸脱内容: 複数の検査でアルカリホスファターゼ（ALP）が基準値下限を下回っている。プロトコルで規定された臨床検査基準範囲からの逸脱の可能性がある。
        プロトコル該当箇所: プロトコルには臨床検査基準範囲に関する具体的な記述はない。Define.xmlに検査項目の基準範囲に関する情報が含まれている可能性がある。
        判断理由: ALP低値は、臨床的に重大な影響を与える可能性は低いと考えられるが、治験薬との関連性や、臨床試験結果に与える影響について確認するため、Minorとした。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CMTRT=PAROXETINE, CMSTDTC=2013-05-21 (併用薬パロキセチン)
        逸脱内容: 併用薬パロキセチンの開始日が治験薬初回投与日（2013-05-20）より後であり、プロトコルで規定された併用薬に関する規定に抵触している可能性がある。
        プロトコル該当箇所: プロトコルの併用薬に関するセクション（具体的なセクション番号は不明）
        判断理由: 併用薬開始日が治験薬投与開始日より後である点は、プロトコル逸脱の可能性がある。ただし、プロトコルの詳細な規定が不明なため、臨床試験結果への影響度合いはMinorと判断した。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CMTRT=PAROXETINE, CMENDTC=2013-05-22 (併用薬パロキセチン)
        逸脱内容: 併用薬パロキセチンの投与期間が1日と非常に短い。臨床的に効果が期待できない期間であり、データ入力誤りの可能性がある。
        プロトコル該当箇所: プロトコルには併用薬の投与期間に関する明確な規定はないが、臨床的妥当性の観点から逸脱の疑義あり。
        判断理由: 併用薬の投与期間が極端に短い点はデータの信頼性に関わる問題であり、確認が必要であるため、Minorとした。

    逸脱No.: 5
        臨床試験結果への影響度合い: Minor
        変数名と値: CMTRT=PROVERA, CMDOSU="2.5 ug" (併用薬PROVERA)
        逸脱内容: 併用薬PROVERAの投与単位が「ug」と記録されている。PROVERAの一般的な投与単位は「mg」であり、「ug」単位は臨床的に不自然である。データ入力誤りの可能性がある。
        プロトコル該当箇所: プロトコルには併用薬の投与単位に関する明確な規定はないが、臨床的妥当性の観点から逸脱の疑義あり。
        判断理由: 併用薬の投与単位が臨床的に不自然であり、データの正確性を確認する必要があるため、Minorとした。

患者ID: 01-701-1146
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMSTDTC, CM.CMENDTC, CM.CMDTC (CMドメインの日付変数), CMTRT (併用薬名)
        医療機関への問い合わせ文面: 
        治験薬併用状況について、CMドメインのデータに複数の疑義があります。

        1.  CMドメインのデータに日付の矛盾があります。
            患者ID: 01-701-1146
            CMSEQ: 5, 6, 7, 9, 12, 13, 14, 16, 17, 19, 20, 21, 23, 24, 26, 27, 28, 31, 32, 34, 35, 36, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61
            CMTRT: BECONASE, DOCUSATE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERA
            CMSTDTC: 2008
            CMENDTC: "" (空欄)
            CMDTC: 2013-05-07, 2013-05-18, 2013-05-20, 2013-06-03, 2013-06-16, 2013-06-18, 2013-06-30, 2013-07-15 (レコードによって異なる)
            CMSTDTCとCMENDTCが2008年と記録されているにもかかわらず、CMDTC（データ収集日）が2013年となっている理由をご教示ください。データ入力時の誤りの可能性も考えられますので、併用薬の開始日と終了日について、原資料をご確認いただけますでしょうか。

        2.  併用薬DOCUSATE, BECONASE, MINERALS NOS, MOTRIN, MULTIVITAMIN, PREMARIN, PROVERA, HYDROCORTISONE, TOPICALについて、投与終了日（CMENDTC）が空欄となっています。これらの併用薬は現在も投与中でしょうか。投与が終了している場合、投与終了日を教えてください。

        3.  併用薬PAROXETINEについて、投与期間が1日（CMSTDTC: 2013-05-21、CMENDTC: 2013-05-22）と記録されていますが、データ入力誤りの可能性はないか確認してください。もしデータ入力誤りでない場合、1日のみの投与となった理由を教えてください。

        4.  併用薬PROVERAについて、投与単位が「ug」と記録されています (CMDOSU = "2.5 ug")。投与単位が正しいか確認してください。PROVERAは一般的に「mg」単位で投与される薬剤ですが、「ug」単位で投与された事例はありますか？もしデータ入力誤りであれば、正しい投与量と投与単位を教えてください。

        5.  治験薬投与期間中に併用が開始されたパロキセチン (CMTRT=PAROXETINE, CMSTDTC=2013-05-21) について、投与開始の医学的理由と、プロトコルで許容された併用薬であることを確認してください。もしパロキセチンがプロトコルで禁止された併用薬に該当する場合、プロトコル逸脱として治験への影響を評価する必要があります。

        上記について、医療機関にて原資料をご確認いただき、回答いただけますようお願いいたします。

        判断理由: CMドメインのデータ品質に関する複数の疑義をまとめて医療機関に確認するため。データの正確性を確認し、プロトコル遵守状況を評価するために、早急な回答が必要である。

クエリNo.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=ALP, LB.LBORNRLO, LB.LBORNRHI (ALP基準範囲)
        医療機関への問い合わせ文面: 
        臨床検査値（LBドメイン）の基準範囲について確認です。
        LBドメインのALP（アルカリホスファターゼ）検査において、基準範囲下限値（LBORNRLO）と上限値（LBORNRHI）がすべてのレコードで同じ値（下限値: 35 U/L、上限値: 115 U/L）で記録されています。
        これはデータ入力の効率化のためと思われますが、念のため、本試験で適用されているALPの基準範囲情報源（検査施設基準値、Define-XML、プロトコル等）と、LBデータに記録されている基準範囲が一致していることを確認していただけますでしょうか。

        判断理由: LBドメインの基準範囲データの記録方法が効率化されている可能性があるため、データの正確性を保証するために、基準範囲の出典と記録された値の整合性を確認する。

# 01-701-1180
## Task1: Clinical Review Results
患者ID: 01-701-1180

症例サマリー:
* 2013年01月28日 (Day -15): スクリーニング1回目、血清尿酸値が基準値上限超え (7.9 mg/dL, 基準値 3.3-7.5 mg/dL、HIGH)。
* 2013年02月12日 (Day 1): ベースライン、嘔吐 (軽度) 発現 (治験薬との因果関係なし、未回復)。
* 2013年02月15日 (Day 4): 排尿意欲 (軽度) 発現 (治験薬との因果関係は関連性あり、未回復)。
* 2013年02月25日 (Day 14): 嘔吐 (軽度) が回復。血清尿酸値が基準値上限超え (8.1 mg/dL, 基準値 3.3-7.5 mg/dL、HIGH)。
* 2013年03月06日 (Day 23): 鼻咽頭炎 (軽度) 発現 (治験薬との因果関係なし、回復)。
* 2013年03月11日 (Day 28): 頭痛 (中等度) 発現 (治験薬との因果関係なし、未回復)。血清尿酸値が基準値上限超え (7.6 mg/dL, 基準値 3.3-7.5 mg/dL、HIGH)。
* 2013年03月19日 (Day 36): 適用部位紅斑、適用部位そう痒症、適用部位小水疱 (各々中等度) 発現 (治験薬との因果関係は関連性あり、未回復)。尿意切迫は回復。
* 2013年03月23日 (Day 40): 治験薬投与中止 (ADVERSE EVENT)。最終 лаборатория 来院、血清尿酸値が基準値内 (5.9 mg/dL, 基準値 3.3-7.5 mg/dL、NORMAL) に回復。
* 2013年04月07日 (Day -): 有害事象フォローアップ。

---
クエリ:
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AETERM = SUDDEN DEATH (AESEQ=6), DS.DSTERM = ADVERSE EVENT (DSSEQ=1), AE.AELLT = URINARY URGENCY (AESEQ=6), AE.AEDECOD = MICTURITION URGENCY (AESEQ=6)
    * 医療機関への問い合わせ文面:
        患者ID 01-701-1180 において、AEドメインの6番目のレコードAETERMに「SUDDEN DEATH」、DSドメインの1番目のレコードDSTERMに「ADVERSE EVENT」と、異なる重篤な有害事象が記録されています。また、AE6番目のレコードのAELLTとAEDECODには「URINARY URGENCY」「MICTURITION URGENCY」と排尿意欲に関する用語が記録されており、内容に矛盾が認められます。
        つきましては、患者ID 01-701-1180 のSUDDEN DEATHの報告の真偽、DSドメインにおけるDSTERMの正確性、およびAEドメイン6番目のレコードAELLT/AEDECODとAETERMの矛盾について、原資料を確認し、正確な情報をご回答ください。
    * 判断理由:
        SUDDEN DEATH は死亡に繋がる可能性のある重篤な有害事象であり、その報告の真偽は患者の安全性評価、及び臨床試験結果の解釈に重大な影響を及ぼします。AEドメインとDSドメインでSUDDEN DEATHの記載に不一致が見られる上、AEドメイン内でもAETERMとAELLT/AEDECODで用語の矛盾が認められるため、データ入力誤りや記録の不整合性が強く疑われます。原資料を確認し、正確な情報を把握することは、データの信頼性を確保し、患者の安全性を最優先に考慮する上で、非常に重要であると判断しました。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CMTRT=HISMANAL, CMSTDTC=2013-03-25
    * 医療機関への問い合わせ文面:
        治験参加中の患者ID 01-701-1180 に併用が確認されたヒスマーナル (CMTRT=HISMANAL, CMSTDTC=2013-03-25) の投与は、本臨床試験プロトコルにおいて禁止されていますか？
        ヒスマーナルはQT延長のリスクが知られている薬剤であり、治験薬との相互作用によるQT延長、ひいては重篤な不整脈や突然死のリスクが懸念されます。併用状況についてプロトコルからの逸脱がないか、またQT延長リスクの観点から医学的な妥当性について、医療機関の見解を伺いたいと存じます。
    * 判断理由:
        プロトコルおよびDefine.xml を確認した限りでは、ヒスマーナルが明確に禁忌薬としてリストアップされている記述は見当たりませんでした。しかしながら、ヒスマーナル（アステミゾール）はQT延長症候群を引き起こす可能性が添付文書等で指摘されており、治験薬との併用によるQT延長リスクは否定できません。患者の安全性を最優先に考慮し、プロトコル逸脱の可能性とQT延長リスクについて、医療機関に確認する必要があると判断しました。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = URATE, LBORRES = 7.9 mg/dL (SCREENING 1), 8.1 mg/dL (WEEK 2), 7.6 mg/dL (WEEK 4), LBNRIND = HIGH (VISIT=SCREENING 1, WEEK 2, WEEK 4)
    * 医療機関への問い合わせ文面:
        患者ID 01-701-1180 の臨床検査値データにおいて、尿酸値 (LB.LBTESTCD = URATE) がスクリーニング1 (SCREENING 1) から Week 4 にかけて継続的に基準値上限を超過 (LBNRIND = HIGH) しています。
        本患者の高尿酸血症について、臨床的な意義と、考えられる原因について医療機関のご見解を伺いたいと存じます。また、高尿酸血症に関連する医学的な対応（食事指導、生活指導、治療介入など）が実施されているかについても、併せてご教示ください。
    * 判断理由:
        尿酸値の継続的な基準値上限超過は、高尿酸血症、ひいては痛風や腎機能障害発症のリスク増加を示唆する可能性があります。特に、高齢のアルツハイマー病患者では、これらの合併症がQOL（生活の質）を著しく損なう恐れがあります。患者の安全性を確保する観点から、高尿酸血症の臨床的意義と原因、並びに医療機関における対応状況について確認することは医学的に妥当と判断しました。ただし、緊急性を要するクリティカルな疑義ではないため、臨床試験結果への影響度合いはMinorと評価しました。

---
クエリなし
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, CM.CMSTDTC, CM.CMENDTC, CM.CMENDY, CM.VISIT, DS.DSSPID, DS.DSDTC, EX.EXSTDTC, EX.EXENDTC, LB.LBNRIND (URATE)

問題点:
* 問題No.1:
    * 変数名と値: AE.AESTDTC (2002, 2013-02-15), EX.EXSTDTC (2013-02-12)
    * 矛盾の内容: AEドメインの有害事象開始日 (AE.AESTDTC) が、EXドメインの治験薬投与開始日 (EX.EXSTDTC) より過去、または大幅に過去の日付になっているレコードが存在する。時系列矛盾、データの信頼性、および治験薬との因果関係の評価に疑義が生じる。
    * 問題点の原因（推測）: データ入力時の誤り、AE開始日の誤記、またはSUPPAEドメインのAETRTEMフラグの誤りの可能性。
    * 対応策（提案）: 医療機関に原資料を確認し、正確なAE開始日を特定する。AETRTEMフラグが "N" で正しいか確認する。データ修正が必要か判断する。

* 問題No.2:
    * 変数名と値: CM.CMSTDTC (2006), CM.CMENDTC (2006, 欠損), CM.CMENDY (欠損)
    * 矛盾の内容: CMドメインの併用薬開始日 (CM.CMSTDTC) に治験実施期間より過去の日付 (2006年) が複数レコードで記録されている。CM終了日 (CM.CMENDTC) とCMENDY（併用薬終了日（治験薬投与からの日数））が複数のレコードで欠損しており、併用薬の投与期間が不明確。
    * 問題点の原因（推測）: データ入力時の誤り、患者の過去の併用薬情報を誤って記録、併用薬が継続中のため終了日が未入力、またはデータ入力漏れの可能性。
    * 対応策（提案）: CMドメインの併用薬開始日とデータ収集日の整合性を確認し、特に2006年の日付が正しいかどうか再調査する。医療機関に原資料を確認し、CM終了日を確認する。投与継続中の場合は、CMENDTCを空欄のままにし、継続中の理由を記録する。

* 問題No.3:
    * 変数名と値: CM.VISIT (AE FOLLOW-UP), CM.VISITDY (欠損)
    * 矛盾の内容: CMドメインの特定のレコードで、VISIT (Visit名) が "AE FOLLOW-UP" となっているにもかかわらず、CM.VISITDY (Planned Study Day of Visit) が欠損している。AEフォローアップVisitで収集されるべきCMデータか、プロトコル上の定義と矛盾している可能性がある。
    * 問題点の原因（推測）: AE FOLLOW-UP Visitにおけるデータ収集の意図が不明確、またはAE FOLLOW-UP VisitにVISITDYが設定されていない可能性。
    * 対応策（提案）: プロトコルまたは関連資料を確認し、AE FOLLOW-UP VisitでのCMデータ収集の意図と、VISITDYの定義を確認する。意図しないデータ収集であれば、データの取り扱いを検討する。定義に基づいてVISITDYを追記する。

* 問題No.4:
    * 変数名と値: DS.DSDTC (データ形式混在), DS.DSSPID (欠損)
    * 矛盾の内容: DS.DSDTC (Dispositionデータ収集日) のデータ形式がdatetimeとdateで混在しており、データ形式の統一が必要。DSドメインの特定のレコードでDSSPID (Sponsor-Defined Identifier) が欠損している。
    * 問題点の原因（推測）: データ入力システムの設定ミス、データ収集時の手順の不統一、データ入力時の未入力、またはDSSPID付与ルールの不適用。
    * 対応策（提案）: DS.DSDTC のデータ形式をdatetime型に統一する。Define.xmlのデータ型定義もdatetimeに修正する。データ作成者にDSSPID欠損の理由を確認し、修正が必要か検討する。

* 問題No.5:
    * 変数名と値: 日付/日時変数の年表記 (2桁年表記レコード混在)
    * 矛盾の内容: CM, AE, EXドメインの日付変数 (CMSTDTC, CMENDTC, AEAESTDTC, AEENDTC, EXSTDTC, EXENDTC) において、年部分が2桁で記録されているレコードが存在する。SDTMの日付変数はYYYY-MM-DD形式（4桁年）で記録されるべきであり、Define.xmlの定義とも不整合。
    * 問題点の原因（推測）: データ入力時のフォーマット誤り。
    * 対応策（提案）: 日付変数の年部分を4桁 (YYYY) に修正する。Define.xmlのItemDef要素のDataType属性が"date"であることを確認する。

* 問題No.6:
    * 変数名と値: LB.LBNRIND = HIGH (LBTESTCD = URATE)
    * 矛盾の内容: LBドメインで LBNRIND（基準範囲外フラグ）が "HIGH" であるレコードが複数存在する。検査項目は URATE（尿酸）であり、基準値超え自体はデータ矛盾ではないが、医学的評価が必要となる可能性がある。
    * 問題点の原因（推測）: 患者の尿酸値が基準範囲を超過。
    * 対応策（提案）: LB.LBNRIND="HIGH" のレコードについて、臨床的な意義を医学専門家にご確認ください。

クエリの作成:
* 患者ID: 01-701-1180
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AETERM = HEADACHE, AE.AESTDTC = 2002 (問題No.1)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 の有害事象「HEADACHE」（AESEQ=4）の発現日が2002年と記録されています。治験薬投与開始日（2013年2月12日）より大幅に過去の日付となっており、データの正確性を確認させていただきたく、原資料をご確認いただけますでしょうか。もし記録に誤りがある場合は、正しい発現日をご教示ください。
        * 判断理由: 有害事象開始日が治験期間外であり、データ信頼性に関わるため、また治験薬との因果関係評価に影響を及ぼす可能性があるため、重要度をMajorと判断しました。

    * クエリNo.2:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC = 2013-02-15, EX.EXSTDTC = 2013-02-12 (問題No.1)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 の有害事象「MICTURITION URGENCY」(AESEQ=5) および「SUDDEN DEATH」(AESEQ=6) の開始日について確認させてください。記録されている開始日（2013年2月15日）が治験薬投与開始日（2013年2月12日）よりも後になっていますが、日付の記録に誤りがないか、原資料をご確認いただけますでしょうか。
        * 判断理由: 有害事象開始日が治験薬投与開始日より後であり、時系列矛盾の可能性があるため、データの正確性を確認する必要がある。治験薬との因果関係評価にも影響を及ぼす可能性があるため、重要度をMajorと判断しました。

    * クエリNo.3:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMTRT = CENTRUM, CM.CMSTDTC = 2006 (問題No.2)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 の併用薬「CENTRUM」（CMSEQ=1, 2, 3, 4, 5, 8, 9, 12）の開始日が2006年と記録されています。治験実施期間（2013年）より前となっており、データの正確性を確認させていただきたく、原資料をご確認いただけますでしょうか。もし記録に誤りがある場合は、正しい開始日をご教示ください。
        * 判断理由: 併用薬開始日が治験期間外であり、データの正確性を確認するため、重要度をMinorと判断しました。

    * クエリNo.4:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC = 欠損 (CMTRT = HISMANAL, MEDROL DOSEPAK など) (問題No.2)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 の併用薬「HISMANAL」「MEDROL DOSEPAK」など（CMSEQ=3, 4, 5, 8, 9, 10, 12）の終了日が空欄となっています。これらの併用薬は現在も投与継続中でしょうか？ 終了日が判明する場合は、原資料をご確認いただき、ご教示いただけますでしょうか。
        * 判断理由: 併用薬の投与状況を把握し、データの完全性を高めるため、重要度をMinorと判断しました。

    * クエリNo.5:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.VISIT (AE FOLLOW-UP) (問題No.3)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 のAEフォローアップVisit（VISITNUM=101）に記録されている併用薬情報（CMドメイン、CMSEQ=11-17）についてお伺いします。AEフォローアップVisitで併用薬情報を収集する意図がございましたでしょうか。もし意図がない場合、これらのデータは誤って記録された可能性がありますので、ご確認いただけますでしょうか。
        * 判断理由: AEフォローアップVisitでのCMデータ収集意図が不明確であり、データの解釈に影響を与える可能性があるため、重要度をMinorと判断しました。

    * クエリNo.6:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: DS.DSSPID = 欠損 (DSDECOD = ADVERSE EVENT) (問題No.4)
        * 医療機関への問い合わせ文面:
            患者ID 01-701-1180 のDispositionドメイン、DSDECOD=ADVERSE EVENT (DSSEQ=1) のレコードで、DSSPID (Sponsor-Defined Identifier) が欠損しております。DSSPIDが欠損している理由について、ご確認いただけますでしょうか。
        * 判断理由: DSSPIDは識別子として重要であり、欠損理由を把握しデータ品質を向上させるため、重要度をMinorと判断しました。

Define.xmlの修正候補:
* ItemDef (AE.AEDTC, CM.CMDTC, DS.DSDTC, LB.LBDTC, SV.SVSTDTC, SV.SVENDTC, DM.RFICDTC, DM.RFPENDTC, DM.DTHDTC, DM.RFXSTDTC, DM.RFXENDTC) の DataType を "datetime" に修正する。（問題No.4 関連）
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1180
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMENDTC (空欄)
        逸脱内容: 併用薬終了日が未記録 (CMSEQ=12, 17, 14, 16, 13)。SDTMデータ標準未準拠、データ品質問題、またはデータ入力エラーの可能性。
        プロトコル該当箇所: SDTM CMドメインのCMENDTC変数の定義 (プロトコルに明記された該当箇所なし)
        判断理由: データ品質保証のため、データマネージャーによる確認が必要。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHTERM = DEPRESSION (ANXIETY), MH.MHSTDTC = 空欄
        逸脱内容: Medical Historyのうつ病エピソード発症時期不明。選択除外基準 EXCL13 抵触の可能性。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [13]
        判断理由: スクリーニング期間3ヶ月以内のうつ病エピソードは除外基準。発症時期不明のため、プロトコル逸脱の可能性あり。

    逸脱No.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT=HISMANAL, CMSTDTC=2013-03-25
        逸脱内容: 併用薬HISMANALは併用禁止薬の疑い。プロトコルに併用禁止薬リストの記載がなく、該当性不明。
        プロトコル該当箇所: 3.8. Concomitant Therapy, 3.4.2.2. Exclusion Criteria [31b]
        判断理由: HISMANALが併用禁止薬に該当する場合、選択基準逸脱となる可能性。

    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMENDTC (空欄), CMSEQ=12, 17, 14, 16, 13
        医療機関への問い合わせ文面: 患者ID 01-701-1180、CMSEQ=12, 17, 14, 16, 13の併用薬CMENDTC（併用薬終了日）をご教示ください。投与継続中の場合はその旨お知らせください。
        判断理由: CMENDTC欠損はデータ品質問題。データの正確性のため医療機関に確認が必要。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHTERM = DEPRESSION (ANXIETY), MH.MHSTDTC = 空欄
        医療機関への問い合わせ文面: 治験責任医師殿。被験者01-701-1180のMedical History「DEPRESSION (ANXIETY)」の発症時期（MHSTDTC）をご教示ください。スクリーニング期間（2013年1月28日）より3ヶ月以内の発症か否かを確認させていただきます。
        判断理由: うつ病エピソードが選択除外基準に抵触するか確認するため、医療機関への情報確認が必要。

    クエリNo.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: CMTRT=HISMANAL
        医療機関への問い合わせ文面: 被験者01-701-1180の併用薬HISMANALは、プロトコル上の併用禁止薬に該当しますでしょうか。該当する場合、治験薬投与前に適切なWashout期間を設けられましたでしょうか。
        判断理由: HISMANALの併用がプロトコル逸脱に該当するか不明。併用禁止薬該当の有無、Washout期間の有無を確認する必要がある。

クエリなし

# 01-703-1279
## Task1: Clinical Review Results
患者ID: 01-703-1279
* 2013年04月27日 (Day -16): スクリーニング 1回目の検査で、ヘマトクリット値51.0% (基準値上限48%)、ヘモグロビン値15.9 g/dL (基準値上限15.8 g/dL)と、基準値上限を超える高値であった。また、バイタルサイン検査において、仰臥位および立位での収縮期血圧、立位での拡張期血圧が高値であった。
* 2013年05月11日 (Day -2): スクリーニング 2回目のバイタルサイン検査において、立位での収縮期血圧および拡張期血圧が高値であった。
* 2013年05月13日 (Day 1): ベースライン訪問時の検査で、ヘマトクリット値51.0% (基準値上限48%)、ヘモグロビン値15.9 g/dL (基準値上限15.8 g/dL)と、引き続き基準値上限を超える高値であった。また、バイタルサイン検査において、立位での収縮期血圧および拡張期血圧が高値であり、体重減少(56.25kg -> 55.79kg)が認められた。ADAS-Cog(11)サブスコアは28、NPI-X(9)トータルスコアは24であった。治験薬（XANOMELINE 54mg）の投与が開始された。
* 2013年06月22日 (Day 41): 2週目の訪問時にDisability Assessment for Dementia (DAD)の食事に関する項目で、「食べたいという意思決定」が「不可能」(ベースライン時は「可能」)に変化した。Neuropsychiatric Inventory (NPI-X) において、妄想、焦燥・興奮、不安、夜間行動、食欲・食事の変化などのNPI-XスコアがベースラインからWeek 2にかけて悪化した。バイタルサイン検査では、仰臥位および立位での収縮期血圧、仰臥位での拡張期血圧が高値を示し、体重減少(55.79kg -> 54.89kg)が認められた。立位3分後の拡張期血圧、脈拍数、収縮期血圧が測定不能であった。患者は「CAREGIVER BECAME ILL (介護者の病気)」を理由に治験を中止した（治験薬最終投与日: 2013年06月03日）。

---
患者ID: 01-703-1279
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: VS.VISIT=WEEK 2, VSTPT=AFTER STANDING FOR 3 MINUTES, VSSTAT=NOT DONE (DIABP, PULSE, SYSBP)
    * 医療機関への問い合わせ文面: Week 2 (Day 41) のVisitにおいて、立位3分後のバイタルサイン (拡張期血圧、脈拍数、収縮期血圧) が測定不能 (VSSTAT=NOT DONE) となっています。測定不能であった理由をご教示ください。
    * 判断理由: 患者の安全性を評価する上で、バイタルサインは重要な指標となるため、測定不能理由を確認する必要があります。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: VS.VSSTAT (VISITNUM=4、VSTESTCD=DIABP, PULSE, SYSBP、VSPOS=STANDING), VS.VSORRES (VSSEQ=12, 25, 37), VS.VSSTRESN (VSSEQ=12, 25, 37), QSドメインのデータ重複, AEドメインのデータ欠損, LBドメインのHCT、HGB高値

問題点:
* 問題No.1: バイタルサイン測定データ (VSドメイン) の欠損
    * 変数名と値: VS.VSSTAT = "NOT DONE", VS.VSORRES = "", VS.VSSTRESN = null, VSTESTCD = DIABP, PULSE, SYSBP, VSPOS = STANDING, VISITNUM = 4
    * 矛盾の内容: VISITNUM=4（WEEK 2）の立位でのDiastolic Blood Pressure, Pulse Rate, Systolic Blood Pressureにおいて、測定が実施されなかったことを示す "NOT DONE" がVSSTATに記録されていますが、VSORRES, VSSTRESN が欠損している理由が不明です。データ入力ミス、測定機器の不具合、患者の状態不良、または測定自体がプロトコルで必須ではなかったなど、様々な原因が考えられます。
    * 問題点の原因（推測）: データ入力時の選択ミス、測定機器の不具合、患者の状態不良により測定不能、またはプロトコルで必須項目ではない可能性。
    * 対応策（提案）: 医療機関にデータが欠損している理由を確認し、データ入力ミスであれば修正、測定が実施されなかった場合は理由とプロトコル逸脱として扱うべきか検討を依頼する。

* 問題No.2: 質問票データ (QSドメイン) の重複
    * 変数名と値: QSドメイン (USUBJID="01-703-1279") の複数レコード、VISIT=BASELINEとVISIT=WEEK 2でデータ重複
    * 矛盾の内容: QSドメインにおいて、患者ID 01-703-1279 の VISIT=BASELINE と VISIT=WEEK 2 で、QSTESTCD, QSTEST, QSCAT など主要な変数の値が同一のレコードが重複して存在しています。データ重複の意図が不明であり、データ整合性の観点から問題となる可能性があります。
    * 問題点の原因（推測）: データ登録システムの不具合、データ抽出時のエラー、または意図的なデータ重複の可能性。
    * 対応策（提案）: データ重複が意図的なものかどうか、データ登録・抽出プロセスを確認し、意図的でない場合は重複データを削除するなどのデータクリーニングを実施する。

* 問題No.3: 有害事象データ (AEドメイン) の欠損
    * 変数名と値: AEドメイン (データセット全体) - レコード数0件
    * 矛盾の内容: AEドメインにAdverse Eventデータが全く登録されていません。臨床試験において有害事象の評価は最重要事項の一つであり、データが完全に欠損していることは、データ収集または登録プロセスにおける重大な問題を示唆している可能性があります。
    * 問題点の原因（推測）: データ入力遅延、データ抽出・変換・ロード (ETL) プロセスのエラー、システム上の問題、または本当に有害事象が発生しなかった可能性も考えられますが、データ欠損の状況からデータ収集・登録プロセスの問題、またはデータ自体の欠損の可能性が高いと考えられます。
    * 対応策（提案）: データマネジメントチームは、AEドメインのデータが意図的に未登録であるか、データ収集または登録プロセスに問題があるのか早急に調査し、データ入力漏れであれば医療機関に確認の上、データの修正と再登録を指示してください。

* 問題No.4: 臨床検査値異常 (LBドメイン)
    * 変数名と値: LB.LBNRIND = "HIGH", LB.LBTESTCD = HCT, HGB
    * 矛盾の内容: LBドメインのヘマトクリット (HCT) とヘモグロビン (HGB) の検査結果が基準値上限を超え、LBNRIND（基準範囲指標）が "HIGH" となっています。Define.xmlの定義上は基準範囲外の値ですが、医学的妥当性の観点から臨床的な意義を確認する必要があります。
    * 問題点の原因（推測）: 患者の生理的な変動、脱水、検査エラー、または疾患による異常値の可能性。
    * 対応策（提案）: 医療機関に問い合わせを行い、HCTとHGBが高値を示していることの臨床的な意義について医学的コメントを求め、患者の安全性に影響がないか確認してください。必要に応じて、再検査や追加の臨床的評価を検討してください。

クエリ:
* 患者ID: 01-703-1279
    * クエリNo.1: バイタルサイン測定データ (VSドメイン) 欠損理由の確認とデータ修正
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: VS.VSSTAT = "NOT DONE", VS.VSORRES = "", VS.VSSTRESN = null, VSTESTCD = DIABP, PULSE, SYSBP, VSPOS = STANDING, VISITNUM = 4
        * 医療機関への問い合わせ文面: 患者ID 01-703-1279、WEEK 2 (VISITNUM=4) のバイタルサインデータについて、立位でのDiastolic Blood Pressure、Pulse Rate、Systolic Blood Pressure が未測定 (VSSTAT=NOT DONE) となっています。データが欠損している理由、および測定が実施されなかった理由についてご教示ください。データ入力の誤りによる欠損でしたら、正しいデータへの修正をお願いいたします。測定が実施されなかった場合、再測定が可能かどうか、また測定未実施の理由についてご回答ください。
        * 判断理由: バイタルサインは患者の安全性を評価する上で重要なデータであり、その欠損はデータ品質に影響を与えるため、データ欠損の理由と可能な限りのデータ収集・修正が必要と判断しました。

    * クエリNo.2: 有害事象データ (AEドメイン) のデータ有無確認とデータ提供依頼
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: AEドメイン (データセット全体) - レコード数0件
        * 医療機関への問い合わせ文面: 患者ID 01-703-1279 を含む全患者の有害事象データ (AEドメイン) がデータセットに登録されていません。データが意図的に未登録であるか、データ入力漏れ等の理由で欠損している可能性があります。AEドメインのデータ有無についてご確認いただき、データが未提供の場合は、速やかにご提供いただけますようお願いいたします。
        * 判断理由: 安全性評価における最重要データであるAEドメインのデータが完全に欠損しているため、早急にデータ有無を確認し、データ取得が必要と判断しました。データ欠損はデータ品質に重大な影響を与えるだけでなく、患者安全性評価を著しく損なう可能性があります。

    * クエリNo.3: 臨床検査値異常 (LBドメイン) の医学的解釈の確認
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBNRIND = "HIGH", LB.LBTESTCD = HCT, HGB
        * 医療機関への問い合わせ文面: 患者ID 01-703-1279 の臨床検査値データについて、Hematocrit (HCT) と Hemoglobin (HGB) の検査値が基準範囲上限を超過 (LBNRIND=HIGH) しています。これらの検査値異常について、臨床的な意義と患者の安全性に影響がないか医学的見解をご教示ください。臨床的意義、患者背景、合併症などを考慮した上で、コメントをいただけますと幸いです。
        * 判断理由: 基準値範囲外の臨床検査値であり、患者の安全性に関わる可能性があるため、医学的見解を確認し、必要に応じて追加対応を検討する必要があると判断しました。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1279
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE (ASSISTANT3), VS.VISIT: WEEK 2, VS.VSTESTCD: SYSBP, VS.VSSTAT: NOT DONE, VS.VSTESTCD: DIABP, VS.VSSTAT: NOT DONE, VS.VSTESTCD: DIABP, VS.VSTPT: AFTER STANDING FOR 3 MINUTES, VS.VSORRES: 空欄, VSTESTCD:PULSE, VS.VSPOS:STANDING (3 minutes), VSORRES=NOT DONE, VS.VSTESTCD: SYSBP, VS.VSTPT: AFTER STANDING FOR 3 MINUTES, VS.VSORRES: 空欄 (ASSISTANT1, ASSISTANT2, ASSISTANT5)
        逸脱内容: 
            Medical Historyにおいてアルツハイマー病の既往歴 (ASSISTANT3)。WEEK 2のVISITにおいて、立位での収縮期血圧と拡張期血圧、脈拍測定が未実施 (ASSISTANT1, ASSISTANT2, ASSISTANT5)。特に立位3分後の血圧と脈拍が欠測 (ASSISTANT2, ASSISTANT5)。Medical Historyのアルツハイマー病既往歴は、プロトコル除外基準に抵触する可能性があり、臨床試験結果に影響を与える可能性がある (ASSISTANT3)。Vital Signs測定の未実施は、プロトコルで規定された評価項目が実施されていない可能性を示唆する (ASSISTANT1, ASSISTANT2, ASSISTANT5)。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [12] Diagnosis of serious neurological conditions (ASSISTANT3), Protocol Attachment LZZT.1. Schedule of Events for Protocol H2Q-MC-LZZT(c), 3.9.3.4.1 Vital Sign Determination (ASSISTANT1, ASSISTANT2, ASSISTANT5)
        判断理由: 
            Medical HistoryのALZHEIMER'S DISEASEの記載は、Serious neurological conditionsという除外基準に抵触する可能性があり、選択・除外基準違反に該当する可能性がある (ASSISTANT3)。Vital Signs測定の未実施は、評価スケジュール違反に該当する (ASSISTANT1, ASSISTANT2, ASSISTANT5)。Medical Historyの既往歴はMajor、Vital Signs測定未実施はMinorと評価されるが、より重大な違反であるMedical Historyの逸脱を優先し、全体の影響度合いをMajorと判断する。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: DS.DSDTC=2013-06-22, SV.SVENDTC=2013-06-22, EX.EXENDTC=2013-06-03, DM.RFENDTC=2013-06-22 (ASSISTANT4)
        逸脱内容: 最終観察日と最終投与日が一致していない (ASSISTANT4)。
        プロトコル該当箇所: 3.10 Patient Disposition Criteria, 3.9.1 Efficacy, 3.9.3 Safety Evaluations (ASSISTANT4)
        判断理由: 最終観察日が最終投与日より後になっている点はプロトコルからの逸脱と判断されるが、臨床試験結果への影響は小さいと考えられるため、Minorの逸脱とする (ASSISTANT4)。

クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE (ASSISTANT3)
    医療機関への問い合わせ文面:
        被験者01-703-1279のMedical HistoryドメインにALZHEIMER'S DISEASEの既往歴が記録されています。
        治験責任医師にご確認いただきたい事項として、
        1. 被験者01-703-1279のアルツハイマー病の診断は、プロトコルの選択基準INCL02のProbable ADの診断に合致するか。
        2. もし合致する場合、除外基準EXCL12のSerious neurological conditionsに該当しないという医学的見解で選択基準を満たすと判断された理由をご教示ください。
    判断理由: Medical HistoryのALZHEIMER'S DISEASEの記載が選択基準と除外基準の両方に抵触する可能性があるため、プロトコル逸脱の可能性を判断するために、治験責任医師による医学的判断の確認が必要となる (ASSISTANT3)。

# 01-703-1258
## Task1: Clinical Review Results
Error
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, CM.CMDTC, CM.CMSTDY, CM.CMENDY, VISITDY, LB.LBORRES, LB.LBSTRESC

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMSTDTC, CM.CMENDTC (rows 1-28)
    * 矛盾の内容: CMドメインの併用薬開始日(CMSTDTC)と終了日(CMENDTC)の年が、一部のレコードで2010年、2011年、2012年、2013年と混在しており、DMドメインの治験薬投与期間（2012年7月20日〜2013年1月21日）と照らし合わせると、時系列に矛盾している可能性があります。特に、多くのレコードで併用薬投与期間が治験薬投与期間より前になっている点は、データの信頼性を損なう懸念があります。
    * 問題点の原因（推測）: データ入力時の年誤り、またはCMデータの日付が治験期間外の過去データである可能性、もしくはCMドメインとDMドメインの日付関連性の誤解。
    * 対応策（提案）: CMドメインのCMSTDTCとCMENDTCについて、原資料（CRF）と照合し、記録されている年が正しいか医療機関に確認してください。データ入力誤りの場合は修正が必要です。CMデータが治験期間外の過去データである場合は、本治験との関連性を確認し、データ使用の妥当性を検討してください。

* 問題No.: 2
    * 変数名と値: LB.LBORRES, LB.LBSTRESC (rows 1, 10, 19, 30, 37, 40, 44, 50, 60, 66, 70, 77, 86, 91, 98, 108, 119, 128, 139, 150, 160, 169, 177, 184, 191, 198, 205, 215, 224, 235, 245, 254, 264, 272, 279, 286など多数)
    * 矛盾の内容: LBドメインにおいて、LBORRES (オリジナル単位結果) と LBSTRESC (標準単位結果) の値が一致しないレコードが複数存在します。Define.xmlの定義ではLBSTRESCはLBORRESの標準単位変換値とされていますが、データ上矛盾が見られます。
    * 問題点の原因（推測）: LBSTRESCのデータ変換処理の不具合、またはデータ入力時の誤りの可能性があります。
    * 対応策（提案）: LBドメインのLBORRESとLBSTRESCの値の整合性について、データ仕様書またはデータ処理手順書を確認してください。LBSTRESCのデータ変換ロジックを見直し、必要であればデータ再作成とDefine.xmlの修正を検討してください。

* 問題No.: 3
    * 変数名と値: 複数の臨床検査値 (ALT, AST, EOS, SODIUM), LBNRIND = HIGH
    * 矛盾の内容: LBドメインで複数の臨床検査値異常（基準値上限超過）が確認されました。特にALT, AST, EOS, SODIUMでHIGHフラグが立っています。これらの検査値異常と、報告されている有害事象（DIZZINESS, UPPER RESPIRATORY TRACT INFECTION）、併用薬（ALEVE）との関連性について医学的な精査が必要です。
    * 問題点の原因（推測）: 治験薬、併用薬、基礎疾患、あるいはデータ入力誤りなど、複数の原因が考えられます。
    * 対応策（提案）: 
        1. LBドメイン、AEドメイン、CMドメイン、MHドメインを突合し、検査値異常と有害事象、併用薬、既往歴との関連性を詳細に調査してください。
        2. 治験責任医師にLB検査値異常の臨床的な意義について確認し、医学的判断を依頼してください。
        3. 必要に応じて、追加の臨床検査や画像検査の実施、治験薬または併用薬の投与状況の確認を検討してください。

クエリ:
患者ID: 01-703-1258
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: CM.CMSTDTC, CM.CMENDTC (rows 1-28)
    * 医療機関への問い合わせ文面:
        患者ID 01-703-1258 の併用薬データにおいて、CM開始日 (CMSTDTC) および CM終了日 (CMENDTC) の年がDMドメインの治験薬投与期間（2012年7月20日〜2013年1月21日）と矛盾しているレコードが複数あります。CMドメインのMedication Start DateとMedication End Dateについて、以下の点をご確認ください。
            1.  記録されている併用薬の投与期間は正しいか？
            2.  CM開始日、CM終了日の日付（年、月、日）は原資料と一致しているか？
            3.  データ入力時に誤りがあった場合は、正しい日付に修正ください。
        併用薬投与期間と治験薬投与期間の整合性は、データ品質において非常に重要です。ご多忙のところ恐縮ですが、早急にご確認とご回答をお願いいたします。
    * 判断理由: 併用薬の投与期間は、治験薬の効果や有害事象の評価に影響を与える重要な情報であり、その日付の誤りはデータ全体の信頼性を損なう可能性があります。データの正確性を確保するため、クリティカルなクエリとして対応が必要です。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LB.LBTESTCD = ALT, AST, EOS, SODIUM, LBNRIND = HIGH
    * 医療機関への問い合わせ文面:
        患者ID 01-703-1258 の臨床検査データにおいて、以下の検査項目で基準値上限を超える高値が確認されました。
            * ALT（アラニンアミノトランスフェラーゼ）
            * AST（アスパート酸アミノトランスフェラーゼ）
            * EOS（好酸球数）
            * SODIUM（ナトリウム）
        これらの検査値異常について、以下の点についてご回答ください。
            1.  検査値異常の原因として考えられる疾患や病態はありますか？
            2.  治験薬または併用薬との関連性は考えられますか？
            3.  患者の安全性に影響を与える可能性はありますか？
            4.  臨床的に追加で実施すべき検査や対応はありますか？
        患者の安全性を評価する上で重要な情報となりますので、ご多忙のところ恐縮ですが、医学的見解をご回答いただけますようお願いいたします。
    * 判断理由: 臨床検査値異常は、患者の安全性に関わる重要な情報であり、治験薬の投与継続や患者管理に影響を与える可能性があります。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1258
    *   逸脱No.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: AE.AETERM=DIZZINESS, AE.AESEV=SEVERE, AE.AESER=Y
        *   逸脱内容: 重度かつ重篤な有害事象「DIZZINESS（めまい）」の発現
        *   プロトコル該当箇所: 3.9.3.2. Adverse Events, 3.9.3.2.2. Serious Adverse Events
        *   判断理由: 重大な有害事象（重度かつ重篤なDIZZINESS）は、患者の安全性に重大な影響を及ぼす可能性があり、臨床試験の評価項目や継続に影響を与える可能性があるため、臨床試験結果への影響度合いをMajorと判断しました。プロトコルで規定された重度または重篤な有害事象の報告手順と照らし合わせ、逸脱の有無を確認する必要があります。

    *   逸脱No.: 2
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LB.LBTESTCD=ALT, LBORRES=43 U/L (SCREENING 1), LBORNRLO=6 U/L, LBORNRHI=32 U/L, LBNRIND=HIGH
        *   逸脱内容: スクリーニング検査時のALT（アラニンアミノトランスフェラーゼ）値が基準範囲上限を超過
        *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III
        *   判断理由: スクリーニング検査においてALT値が基準範囲上限を超過しており、プロトコルの除外基準EXCL27に抵触する可能性があります。ただし、逸脱値はわずかであり、その後のALT値は正常範囲内へ推移しているため、臨床試験結果への影響は限定的と考えられます。Define.xmlおよびプロトコル断片からはLilly Reference Range III の詳細が不明なため、Minorと評価しました。

    *   逸脱No.: 3
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LB.LBTESTCD=AST, LBORRES=36 U/L (SCREENING 1), LBORNRLO=9 U/L, LBORNRHI=34 U/L, LBNRIND=HIGH
        *   逸脱内容: スクリーニング検査時のAST（アスパラギン酸アミノトランスフェラーゼ）値が基準範囲上限を超過
        *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III
        *   判断理由: スクリーニング検査においてAST値が基準範囲上限を超過しており、プロトコルの除外基準EXCL27に抵触する可能性があります。ただし、逸脱値はわずかであり、その後のAST値は正常範囲内へ推移しているため、臨床試験結果への影響は限定的と考えられます。Define.xmlおよびプロトコル断片からはLilly Reference Range III の詳細が不明なため、Minorと評価しました。

    *   逸脱No.: 4
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LB.LBTESTCD=EOS, LBORRES=0.59 THOU/uL (SCREENING 1), LBORNRLO=0 THOU/uL, LBORNRHI=0.57 THOU/uL, LBNRIND=HIGH
        *   逸脱内容: スクリーニング検査時のEOS（好酸球）値が基準範囲上限を超過
        *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III
        *   判断理由: スクリーニング検査においてEOS値が基準範囲上限を超過しており、プロトコルの除外基準EXCL27に抵触する可能性があります。ただし、逸脱値はわずかであり、その後のEOS値は正常範囲内へ推移しているため、臨床試験結果への影響は限定的と考えられます。Define.xmlおよびプロトコル断片からはLilly Reference Range III の詳細が不明なため、Minorと評価しました。

    *   逸脱No.: 5
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: LB.LBTESTCD=SPGRAV, LBORRES=1.032 NO UNITS (SCREENING 1), LBORNRLO=1.006 NO UNITS, LBORNRHI=1.03 NO UNITS, LBNRIND=HIGH
        *   逸脱内容: スクリーニング検査時のSPGRAV（尿比重）値が基準範囲上限を超過
        *   プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III
        *   判断理由: スクリーニング検査においてSPGRAV値が基準範囲上限を超過しており、プロトコルの除外基準EXCL27に抵触する可能性があります。ただし、尿比重は生理的変動が大きく、臨床的な意義は限定的である可能性も考慮されるため、臨床試験結果への影響は軽微と考えられます。Define.xmlおよびプロトコル断片からはLilly Reference Range III の詳細が不明なため、Minorと評価しました。

    *   逸脱No.: 6
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMTRT = ALEVE, CM.CMDECOD = NAPROXEN SODIUM, CM.CMSTDTC = 2011, CM.CMDTC = 2012-07-10
        *   逸脱内容: 併用薬ALEVE（ナプロキセンナトリウム）の治験期間中の使用
        *   プロトコル該当箇所: 3.8. Concomitant Therapy
        *   判断理由: 被験者01-703-1258は、治験期間中にALEVE（ナプロキセンナトリウム）を併用しています。CMドメインのデータからは併用開始日が治験薬投与開始日より前である可能性が示唆されるものの、ALEVEがプロトコルで禁止されている併用薬かどうかは不明です。プロトコルの併用薬に関する規定と照合し、併用が許可されているか、またはプロトコル逸脱に該当するか確認が必要です。現時点では情報不足のため、臨床試験結果への影響度合いはMinorと判断しました。

    *   逸脱No.: 7
        *   臨床試験結果への影響度合い: Minor
        *   変数名と値: CM.CMENDTC=2013-01-20, EX.EXENDTC=2013-01-11, CM.CMTRT = HYDROCORTISONE
        *   逸脱内容: 併用薬HYDROCORTISONEの終了日が治験薬の終了日より後
        *   プロトコル該当箇所: 3.8. Concomitant Therapy
        *   判断理由: 併用薬HYDROCORTISONEのCMENDTCが治験薬EXENDTCより後になっており、併用薬の使用期間が治験薬投与期間と重複している可能性があります。プロトコルに併用薬に関する規定（投与期間の制限など）がある場合、逸脱となる可能性があります。ただし、HYDROCORTISONEは一般的な薬剤であり、短期間の使用であれば臨床試験結果に大きな影響を与えない可能性も考慮し、臨床試験結果への影響度合いはMinorと判断しました。プロトコル上の併用薬規定と照合し、逸脱の有無を確認する必要があります。

患者ID: 01-703-1258
    *   クエリNo.: 1
        *   臨床試験結果への影響度合い: Major
        *   変数名と値: LB.LBTESTCD=ALT, LB.LBORRES=43 U/L (SCREENING 1), LB.LBTESTCD=AST, LB.LBORRES=36 U/L (SCREENING 1), LB.LBTESTCD=EOS, LB.LBORRES=0.59 THOU/uL (SCREENING 1), LB.LBTESTCD=SPGRAV, LBORRES=1.032 (SCREENING 1)
        *   医療機関への問い合わせ文面:
            被験者01-703-1258のスクリーニング1回目検査データについて、以下の点をご確認ください。

            1.  スクリーニング1回目検査時のALT値43 U/L、AST値36 U/L、EOS値0.59 THOU/uL、SPGRAV値1.032は、プロトコルで規定されたLilly Reference Range IIIの基準範囲外に該当しますか？該当する場合、各検査項目の基準範囲と、本被験者の検査値が基準範囲を逸脱している程度についてご教示ください。
            2.  上記臨床検査値が基準範囲外である場合、治験責任医師は、本被験者を治験に組み入れることがプロトコルに適合すると判断されましたか？
            3.  治験責任医師が組入れ可能と判断された場合、その医学的根拠をご教示ください。

            本件は、プロトコル3.4.2.2の除外基準[27b]および治験参加基準に関わる重要な確認事項です。治験の

# 01-701-1181
## Task1: Clinical Review Results
患者ID: 01-701-1181
* 2013年11月26日 (Day -9): スクリーニング1来院時の検査値において、アルブミン (ALB) が基準値下限を下回る低値 (3.2 g/dL, 基準範囲 3.5-4.6 g/dL) でした。
* 2013年12月09日 (Day 5): Week 2来院時、中等度 (MODERATE) の激越 (AGITATION) の有害事象が発現しました (MedDRA: 激越 AGITATION)。同日、治験薬の投与が中止されました。
* 2013年12月12日 (Day 8): Week 2来院時の検査において、アルブミン (ALB) 値は基準範囲内まで回復しました。
* 2014年05月23日 (Day 170): Retrieval来院時のバイタルサイン測定において、臥位、立位1分後、立位3分後のいずれの体位でも、収縮期血圧 (SYSBP) および拡張期血圧 (DIABP) が低下傾向にありました。また、立位1分後および立位3分後の脈拍数 (PULSE) が増加傾向にありました (立位1分後: 100 BEATS/MIN, 立位3分後: 98 BEATS/MIN)。体温 (TEMP) は、Week 2来院時に引き続き、今回も基準値範囲を下回る低値 (97.0 F, 36.11 C) でした。

---

患者ID: 01-701-1181
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AETERM = AGITATION, AE.AESEV = MODERATE, CM.CMTRT = MOTRIN
    * 医療機関への問い合わせ文面:
        有害事象「激越」発現時の状況、特に併用薬「MOTRIN」との関連性について確認してください。有害事象と併用薬の開始・終了日、投与量、投与経路、投与頻度など、詳細な情報をご提供ください。また、有害事象に対する処置、転帰についてもご教示ください。
    * 判断理由:
        有害事象「激越」は中等度であり、患者の安全性に関わる可能性があります。また、併用薬「MOTRIN」との関連性が不明なため、情報収集が必要です。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD=ALB, LBORRES=3.2 g/dL (SCREENING 1)
    * 医療機関への問い合わせ文面:
        治験参加患者のスクリーニング検査（SCREENING 1）において、Albumin（アルブミン）値が基準値下限を下回っています(3.2 g/dL)。臨床的に懸念される事項はありますでしょうか。
    * 判断理由:
        症例サマリー作成時に、スクリーニング検査でAlbumin値が基準値下限を下回っていることを確認しました。Define.xmlを確認したところ、LBドメインのLBNRIND変数は、検査値が基準範囲外かどうかを示すReference Range Indicatorであることがわかりました。今回のデータではLBNRIND="LOW"となっており、基準範囲を下回ることが示唆されています。
        ただし、Albumin値の低下は、栄養状態や肝機能など様々な要因で変動しうるため、直ちに臨床的に問題となるわけではありません。念のため、治験担当医師に医学的な解釈を確認することが望ましいと考えられます。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: VS.VSTESTCD = [DIABP, SYSBP, PULSE, TEMP], VISIT = RETRIEVAL
    * 医療機関への問い合わせ文面:
        Retrieval来院時のバイタルサイン（血圧、脈拍数、体温）の変動について、臨床的な意義をご評価ください。特に、血圧低下と脈拍数増加の関連性、脱水や体液喪失の可能性についてご検討ください。
    * 判断理由:
        Retrieval来院時のバイタルサインの変動は、臨床的に問題となる可能性は低いと考えられますが、念のため専門家の意見を確認することが望ましいと判断しました。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: DS.DSTERM = ADVERSE EVENT, DS.DSDECOD = ADVERSE EVENT, VISIT = WEEK 2
    * 医療機関への問い合わせ文面:
        Dispositionドメインにおいて、治験中止理由が「ADVERSE EVENT」となっていますが、WEEK 2という早期に治験中止となった理由、詳細な背景因子についてご説明ください。特に、有害事象「激越」が治験中止の直接的な理由であるか否か、治験薬との因果関係についてご教示ください。
    * 判断理由:
        治験薬との因果関係が疑われる有害事象により、患者が早期に治験中止となっている場合、臨床試験の評価項目に重大な影響を与える可能性があります。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMENDTC, CM.CMINDC, DS.DSTERM, DS.DSDECOD, DS.DSDTC, DS.DSSTDTC, DS.DSSTDY, LB.LBORRES (Albumin), VS.VSORRES (体温、脈拍数、拡張期血圧), VS.VSDTC, VS.VISITDY, VS.VSDY, SUPPドメイン全般

問題点:
* 問題No.1: 日付変数の形式不統一と不整合
    * 変数名と値: CM.CMSTDTC, CM.CMENDTC, EX.EXENDTC, AE.AESTDTC, AE.AEENDTC, DS.DSSTDTC, LB.LBDTC, MH.MHSTDTC, QS.QSDTC, SV.SVSTDTC, SV.SVENDTC, VS.VSDTC (Subject: 01-701-1181)
    * 矛盾の内容:
        * CMドメインのCMSTDTC, CMENDTC、EXドメインのEXENDTC、AEドメインのAESTDTC, AEENDTC、DSドメインのDSSTDTC、MHドメインのMHSTDTC、QSドメインのQSDTC、SVドメインのSVSTDTC, SVENDTC、VSドメインのVSDTCの日付形式がYYYY-MM-DD形式で統一されておらず、YYYY年のみ、空欄、DateTime形式などが混在している。
        * 具体的には、CM.CMSTDTCに1985や2012-06-04などの年のみの値、CM.CMENDTCに空文字列""、DS.DSDTCにDateTime形式、LB.LBDTCにDateTime形式などが見られる。
        * 一方で、CMDTC, AEDTC, DMDTC, EXSTDTC, QS.QSDY, SV.VISITDYなど、YYYY-MM-DD形式の日付項目も存在する。
        * Define.xmlの定義と照らし合わせると、DataType="date"であるべき項目と"datetime"であるべき項目が混在しており、データ形式の不統一が認められる。
        * また、AE.AESTDTC, AE.AEENDTC (2013-12-09) がAEDTC (2013-12-12) より過去の日付となっており、時間軸の整合性にも矛盾が認められる。
    * 問題点の原因（推測）:
        * データ入力時の形式不統一、または誤ったデータ型の選択。
        * Define.xmlの定義とSDTMデータの形式が一致していない。
    * 対応策（提案）:
        * Define.xmlを修正し、日付変数のデータ型をdateまたはdatetimeのいずれかに統一することを提案する。
        * 修正後のDefine.xmlに基づき、SDTMデータを再作成し、日付形式を統一することを推奨する。
        * 医療機関に日付項目の正確な形式と値を再確認し、データ修正を依頼する。
        * 特にCMENDTCの欠損値、CMSTDTCの過去日付、AE関連の日付の不整合、DSドメインの欠損値について、医療機関に詳細な理由と修正を問い合わせる。

* 問題No.2: DSドメインの欠損値
    * 変数名と値: DS.DSTERM, DS.DSDECOD, DS.DSDTC, DS.DSSTDTC, DS.DSSTDY (DSSEQ=2, 3) が空欄
    * 矛盾の内容: DSドメインのDSSEQ=2, 3のレコードにおいて、DSTERM, DSDECOD, DSDTC, DSSTDTC, DSSTDYが欠損している。特にDSDECODとDSSTDTCはDefine.xmlで必須項目と定義されている。
    * 問題点の原因（推測）: データ入力時のエラー、データ収集の不備、または意図的な欠損の可能性。
    * 対応策（提案）:
        * 医療機関にDSドメインの欠損値の理由を確認し、データ入力エラーや収集漏れの場合は、データ修正を依頼する。
        * 意図的な欠損である場合は、その理由と医学的な妥当性を確認する。

* 問題No.3: LBドメインのAlbumin低値
    * 変数名と値: LB.LBTESTCD=ALB, LB.VISIT=SCREENING 1, LB.LBORRES=3.2, LBSTRESN=32, LBNRIND=LOW (LBSEQ=1)
    * 矛盾の内容: Albumin (ALB) の検査値が基準値下限を下回るLow (3.2 g/dL) である。Define.xmlに定義された基準値下限 (LBORNRLO) は 3.5 g/dL。
    * 問題点の原因（推測）: 患者の基礎疾患、栄養状態、または臨床的に意義のある検査値異常の可能性。データ入力ミスや検査エラーの可能性も考慮。
    * 対応策（提案）:
        * 医療機関にLBドメインのALB (LBSEQ=1) の検査値が正しいか確認するクエリを発行する。
        * Albumin低値の臨床的な意義について医師に評価を依頼し、患者の健康状態や治験薬との関連性を検討する。
        * 必要に応じて、追加の臨床検査やAEドメインとの関連性調査を行う。

* 問題No.4: VSドメインのバイタルサイン異常値
    * 変数名と値: VS.VSTESTCD = TEMP, VSORRES = 095.2 (VSSEQ=50, VISIT=WEEK 2), VS.VSTESTCD = PULSE, VSORRES = 100 (VSSEQ=30, VISIT=RETRIEVAL, VSPOS=STANDING), VS.VSTESTCD = DIABP, VSORRES = 47 (VSSEQ=14, VISIT=RETRIEVAL, VSPOS=STANDING)
    * 矛盾の内容:
        * 体温 (TEMP) が95.2°F (35.11℃) と低体温。
        * 立位での脈拍数 (PULSE) が100 beats/minと頻脈。
        * 立位での拡張期血圧 (DIABP) が47 mmHgと低血圧。
        * これらの値は、臨床的に異常値であり、患者の安全性の観点から懸念される。
    * 問題点の原因（推測）: 測定誤差、患者の状態変化（疾患、有害事象）の可能性。
    * 対応策（提案）:
        * 医療機関にVSドメインのTEMP, PULSE, DIABPの測定値が正しいか確認するクエリを発行する。
        * バイタルサイン異常値について、測定時の状況、患者の状態、既往歴、併用薬などを詳細に確認し、医学的な妥当性を評価する。
        * 必要に応じて、AEドメイン（有害事象）との関連性を調査し、患者の安全性に影響がないか確認する。

* 問題No.5: VSドメインの日付と計画訪問日の不整合
    * 変数名と値: VS.VSDTC, VS.VISITDY, VS.VSDY (VSSEQ=1, 2, 3, 17, 18, 19, 32, 33, 34, 47)
    * 矛盾の内容: VSドメインにおいて、データ収集日 (VSDTC) と計画訪問日 (VISITDY) の間にずれが認められるレコードが複数存在する。また、VSDY (Study Day of Vital Signs) と VISITDY (Planned Study Day of Visit) の値が一致していないレコードも存在する。
    * 問題点の原因（推測）: データ入力時の誤り、VISITDYの自動計算ロジックの不備、または計画外の訪問日におけるデータ収集の可能性。
    * 対応策（提案）:
        * 医療機関にVSドメインのVSDTC, VISITDY, VSDYの記録について確認し、データ入力誤りや不整合があれば修正を依頼する。
        * VISITDYの自動計算ロジックに不備がないか確認し、必要に応じて修正する。

* 問題No.6: SUPPドメインのデータ欠損
    * 変数名と値: SUPPDSドメインの全レコード欠損、SUPPDM, SUPPAE, SUPPLBドメインのIDVARVAL, QEVAL, QORIG, QLABEL, QNAM, IDVAR が多数欠損
    * 矛盾の内容: SUPPDSドメインに至っては全レコードが欠損しており、SUPPDM, SUPPAE, SUPPLBドメインもIDVARVALなどの主要なQualifier変数が欠損しているレコードが散見される。SUPPドメインはSupplemental Qualifierデータセットであり、本来であればQualifier情報が記録されるべきである。
    * 問題点の原因（推測）: SUPPドメインのデータ収集が実施されていない、SDTMデータ作成時のデータ変換・マッピング処理の不備、またはDefine.xmlの定義とデータ構造の不整合の可能性。
    * 対応策（提案）:
        * SUPPドメインのデータ収集状況を医療機関に確認し、データが未収集の場合は、データ収集方法と手順を見直す。
        * SDTMデータ作成プロセス（データ抽出、変換、マッピング処理）を見直し、SUPPドメインのデータが正しく出力されるように修正する。
        * Define.xmlにおけるSUPPドメインの定義（ItemGroupDef, ItemDef, ValueListDefなど）がSDTMIGに準拠し、データ構造と整合しているか確認する。

Define.xmlの修正候補:
* DM.RFXENDTCのDataTypeを"date"から"datetime"へ修正 (問題No.4に関連)
* VS.VSTPTNUMまたはVS.VSELTMのDataTypeと形式を統一 (問題No.5に関連)

クエリ:
* 患者ID: 01-701-1181
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC, CM.CMDTC (CMドメイン全般)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1181 の併用薬 (CMドメイン) データについて、CMTRT が CALCIUM MAGNESIUM, POTASSIUM, TYLENOL, VITAMIN C, VITAMIN E のレコードで、開始日 (CMSTDTC) がデータ収集日 (CMDTC) より過去の1985年 (VITAMIN E は 2012-06-04) と記録されています。データ入力誤りの可能性が考えられますので、記録された日付が正しいか、記録誤りであれば正しい日付をご教示いただけますでしょうか。
        * 判断理由: 併用薬開始日は、治験薬との相互作用や有害事象評価に不可欠な情報であり、誤りの可能性が高いため、重要度「Major」と判断しました。

    * クエリNo.2:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMENDTC (CMドメイン全般)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1181 の併用薬 (CMドメイン) データについて、CMTRT が CALCIUM MAGNESIUM, POTASSIUM, TYLENOL, VITAMIN C, VITAMIN E のレコードで、終了日 (CMENDTC) が空欄となっています。併用薬が中止されている場合は中止日を、継続中の場合はその旨をご教示いただけますでしょうか。
        * 判断理由: 併用薬終了日も、併用薬の評価において重要な情報であり、欠損となっている理由を確認する必要があるため、重要度「Major」と判断しました。

    * クエリNo.3:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMINDC, CM.CMTRT = MOTRIN (CMSEQ=21)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1181 の併用薬 (CMドメイン) データについて、CMTRT が MOTRIN (イブプロフェン) のレコード (CMSEQ=21) の適応 (CMINDC) が空欄となっています。MOTRIN の投与目的 (適応疾患) をご教示いただけますでしょうか。
        * 判断理由: CMINDCは必須項目ではないものの、データの質の観点から、可能な限り情報を収集することが望ましいため、重要度「Minor」と判断しました。

    * クエリNo.4:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DSドメイン全般 (DSSEQ=2, 3)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1181 の Disposition (DS) ドメインにおいて、DSSEQ=2, 3 のレコードで DSTERM, DSDECOD, DSDTC, DSSTDTC, DSSTDY が空欄となっています。データ入力時またはデータ収集時のエラーの可能性が考えられます。該当レコードの正確な情報をご提供いただけますでしょうか。特に、DSDECOD (Standardized Disposition Term) と DSSTDTC (Start Date/Time of Disposition Event) は必須項目となりますので、必ずご確認をお願いいたします。
        * 判断理由: DSドメインの主要な識別子と日時変数が広範囲に欠損しており、データセット全体の解釈を困難にする可能性があるため、重要度「Major」と判断しました。

    * クエリNo.5:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD = ALB, LBORRES = 3.2, LBNRIND = LOW (LBSEQ=1, VISIT=SCREENING 1)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1181 の臨床検査値 (LBドメイン) において、スクリーニング1 (VISIT=SCREENING 1) のアルブミン値 (ALB, LBSEQ=1) が基準値下限を下回るLow (3.2 g/dL) と報告されています。検査値が
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1181
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DM.ACTARMCD: Xan_Lo, DM.ARMCD: Xan_Hi
        逸脱内容: 治験薬がプロトコルで計画されたXanomeline High Doseではなく、Xanomeline Low Doseで投与されている可能性が高いです。DMドメインの計画された投与群(ARMCD, ARM)と実際の投与群(ACTARMCD, ACTARM)に不一致が認められます。
        プロトコル該当箇所: 3.5 Patient Assignment, 3.6 Dosage and Administration, TA, DM
        判断理由: 計画された投与量と実際の投与量が異なる場合、プロトコル逸脱に該当し、臨床試験の主要評価項目に影響を与える可能性があります。治験薬の誤投与は患者の安全性にも関わるため、影響度合いをMajorと判断しました。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=ALB, LB.LBORRES=3.2, LB.LBORRESU=g/dL
        逸脱内容: 被験者01-701-1181のスクリーニング検査において、アルブミン値が基準範囲を下回っています。
        プロトコル該当箇所: プロトコルの選択/除外基準セクション、または臨床検査基準値に関する規定箇所 (具体的なページ番号は不明)
        判断理由: LBドメインの臨床検査データにおいて、アルブミン値が基準範囲を下回っています。Define.xmlのLBドメイン定義より、LBORNRLO (基準範囲下限) が3.5 g/dLと示唆されるため、基準範囲を下回っている可能性があります。ただし、プロトコルに具体的な基準範囲の規定が不明なため、逸脱の程度と臨床試験への影響度合いをMinorと判断しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMTRT = MOTRIN
        逸脱内容: 被験者01-701-1181に併用薬MOTRIN (イブプロフェン) の使用が記録されています。提供された情報からは、MOTRINの使用がプロトコル逸脱に該当するかどうか判断できません。
        プロトコル該当箇所: プロトコルの併用薬に関するセクション (該当箇所が不明なため、要確認)
        判断理由: Define.xml および JSON データからは、併用薬「MOTRIN」に関する具体的なプロトコル規定への違反は特定できません。プロトコル本文を確認し、併用禁止薬リスト、投与量、投与期間などの規定と照合する必要があります。現時点ではプロトコル逸脱の可能性と臨床試験への影響度合いをMinorと判断しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC: 1985-01-01 (複数の併用薬レコードで確認)
        逸脱内容: 併用薬開始日が1985年と記録されており、データ入力時の誤り、または情報収集時の誤りの可能性があります。
        プロトコル該当箇所: 3.8. Concomitant Therapy
        判断理由: 併用薬開始日の誤りは、データの信頼性を損なう可能性がありますが、臨床試験の主要評価項目への直接的な影響はMinorと考えられます。ただし、データの正確性を確保するために確認が必要です。

患者ID: 01-701-1181
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DM.ACTARMCD, DM.ARMCD
        医療機関への問い合わせ文面:
        被験者01-701-1181のDMドメインにおいて、計画されたArm (ARMCD: Xan_Hi, Xanomeline High Dose) と実際のArm (ACTARMCD: Xan_Lo, Xanomeline Low Dose) に不一致が認められます。計画された投与群と実際の投与群が異なる理由、および臨床試験結果への影響についてご教示ください。治験薬はプロトコルで規定されたArmに沿って正しく投与されていますでしょうか。もし誤りがある場合、理由と今後の対応についてご教示ください。
        判断理由: 計画された投与量と実際の投与量の不一致は、プロトコル逸脱の可能性があり、臨床試験の主要評価項目に影響を与える可能性があるため、重要度「Major」と判断しました。データの正確性と患者への適切な投与を確認するために、医療機関への問い合わせが必要です。

    クエリNo.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMTRT=MOTRIN
        医療機関への問い合わせ文面:
        被験者01-701-1181が併用薬としてMOTRIN (イブプロフェン) を使用している記録があります。MOTRINはプロトコルで併用が禁止されている薬剤に該当しないか、あるいは使用に際してプロトコルで規定された条件 (使用量、期間など) を遵守しているか確認して頂けますでしょうか。
        判断理由: MOTRIN (イブプロフェン) がプロトコルで併用禁止薬に該当するか不明であり、プロトコル遵守状況を確認する必要があるため、医療機関への問い合わせが必要です。併用薬の使用状況は患者の安全性や試験結果の解釈に影響を与える可能性があるため、重要度「Minor」と判断しました。

    クエリNo.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=ALB, LB.LBORRES=3.2, LB.LBORRESU=g/dL
        医療機関への問い合わせ文面:
        被験者01-701-1181のスクリーニング検査におけるアルブミン値 (3.2 g/dL) が基準範囲を下回っていますが、本値はプロトコルの選択基準・除外基準に抵触しないか、また臨床的に問題がないかご教示ください。
        判断理由: アルブミン低値がプロトコル逸脱に該当するか不明であり、選択/除外基準への抵触の有無と臨床的意義を確認する必要があるため、医療機関への問い合わせが必要です。臨床検査値の基準範囲外の値は、患者組み入れの適切性に関わる可能性があるため、重要度「Minor」と判断しました。

    クエリNo.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC
        医療機関への問い合わせ文面:
        被験者01-701-1181のCMドメインにおいて、複数の併用薬の開始日 (CMSTDTC) が1985年となっています。これはデータ入力の誤りである可能性が考えられます。併用薬の開始日について、記録の再確認と修正をお願いできますでしょうか。
        判断理由: データ入力の誤りの可能性があり、データの品質管理の観点から正確性を確保するため、医療機関への問い合わせが必要です。データ修正依頼のため、重要度「Minor」と判断しました。

# 01-704-1017
## Task1: Clinical Review Results
**症例サマリー:**

患者ID: 01-704-1017
* 2013年09月20日 (Day -16): スクリーニング1回目、77歳男性。医学的既往歴としてアルツハイマー病、心疾患、性欲亢進、ST上昇、心筋梗塞、心臓発作、ST低下、3血管バイパスグラフト、期外収縮が報告された。併用薬としてアスピリン81mgを1日1回経口投与開始。臨床検査でクレアチニン高値 (1.8 mg/dL) が確認された。MMSE 23点、Modified Hachinski Ischemic Score 0点。
* 2013年09月27日 (Day -9): スクリーニング2回目。併用薬アスピリン継続。
* 2013年10月06日 (Day 1): ベースライン来院、治験薬ザノメリン54mg貼付剤、併用薬プレマリン0.625mg（隔日経口投与）投与開始。ADAS-Cog(11) 27点。Disability Assessment for Dementia (DAD)合計スコアは96点から0点に低下、Neuropsychiatric Inventory (NPI-X)合計スコアは61点から16点に低下。
* 2013年10月18日 (Day 13): AMBUL ECG PLACEMENT (visit 3.5)。
* 2013年10月19日 (Day 14): Week 2来院、治験薬ザノメリン81mg貼付剤に増量。有害事象として心筋梗塞（軽度）および心室中隔欠損症発現、治験薬との因果関係は「関連なし」、転帰は「回復」。臨床検査でアルブミン低値 (3.3 g/dL, 基準値下限3.5 g/dL)、BUN高値 (29 mg/dL, 基準値上限24 mg/dL)、クレアチニン高値 (1.8 mg/dL, 基準値上限1.6 mg/dL) およびリン低値が確認された。
* 2013年11月01日 (Day 27): Week 4来院、最終臨床検査。臨床検査でアルブミン低値 (3.4 g/dL, 基準値下限3.5 g/dL) が再確認された。
* 2013年11月05日 (Day 31): 有害事象として掻痒感、発疹（軽度）発現、治験薬との因果関係は「おそらく関連あり」、転帰は「未回復」。
* 2013年11月09日 (Day 35): Week 4来院。有害事象として脳梗塞後遺症（重度）、インフルエンザ（重度）発現、治験薬との因果関係はいずれも「関連なし」、転帰はいずれも「未回復」。
* 2013年11月11日 (Day 37): AMBUL ECG REMOVAL (visit 6)。
* 2013年11月18日 (Day 44): 有害事象としてインフルエンザ転帰「回復」。脳梗塞後遺症は「未回復」。
* 2013年11月19日 (Day 45): 有害事象として心筋梗塞転帰「回復」。
* 2013年11月22日 (Day 48): 有害事象として発疹、掻痒感転帰「回復」。
* 2013年11月24日 (Day 50): Week 6来院、ADVERSE EVENTにより治験中止。有害事象として発疹、掻痒感再発（いずれも軽度）、治験薬との因果関係は「おそらく関連あり」、転帰は「未回復」。
* 2013年12月06日 (Day 62): AEフォローアップ来院。有害事象として発疹、掻痒感転帰「回復」。

---
**クエリ:**

患者ID: 01-704-1017
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AETERM = BRAIN DEATH, AE.AELLT = FLU
    * 医療機関への問い合わせ文面: 有害事象「BRAIN DEATH」のMedDRA LLTが「FLU」と報告されていますが、データ入力誤りの可能性はないでしょうか。原資料を確認し、正しくはインフルエンザ (Influenza) ではなく、脳死 (Brain death) で報告すべきではないでしょうか。
    * 判断理由: 重大な有害事象である脳死が、インフルエンザ（FLU）と関連付けられているのは医学的に不自然であり、データの信頼性を損なう可能性があります。原資料を確認し、正確なMedDRA LLTに修正する必要があります。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: AE.AETERM = LATE EFFECTS OF CEREBRAL INFRACTION, AE.AESEV = SEVERE, AE.AEOUT = NOT RECOVERED/NOT RESOLVED, AE.AEENDTC = 2013-11-18, MH.MHTERM = ALZHEIMER'S DISEASE
    * 医療機関への問い合わせ文面: 脳梗塞後遺症（LATE EFFECTS OF CEREBRAL INFRACTION）が重度であり、治癒/回復していないにもかかわらず、治験を継続した理由を確認してください。プロトコルで規定された中止基準に抵触していないか、治験を継続することが患者の安全上問題ないか、医学的見地からご説明ください。また、脳梗塞後遺症は、既往歴のアルツハイマー病と病態関連が考えられますが、医学的に妥当でしょうか。
    * 判断理由: 脳梗塞後遺症は神経学的重篤な既往歴であり、治験継続の可否、及び安全性評価に影響を与える可能性があります。プロトコル逸脱の可能性、及び医学的妥当性を確認する必要があります。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AE.AETERM = MYOCARDIAL INFARCTION, AE.AEREL = PROBABLE, EX.EXTRT = XANOMELINE
    * 医療機関への問い合わせ文面: 有害事象「MYOCARDIAL INFARCTION (心筋梗塞)」と治験薬ザノメリンの因果関係が「PROBABLE (可能性あり)」と評価されています。心筋梗塞発症時の状況（発症日、重症度、症状、臨床検査値、心電図所見など）、既往歴、併用薬、除外基準抵触の有無、治験薬との因果関係について、治験責任医師の見解を原資料に基づき詳細にご説明ください。
    * 判断理由: 心筋梗塞は重大な有害事象であり、治験薬との因果関係が疑われる場合、患者の安全性に重大な懸念が生じます。詳細な情報に基づいて、治験薬との因果関係を慎重に評価する必要があります。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = ALB (アルブミン), LB.LBORRES = 3.3-3.4 g/dL (低値); LB.LBTESTCD = BUN (BUN), LB.LBORRES = 29 mg/dL (高値), VISIT = WEEK 2, WEEK 4
    * 医療機関への問い合わせ文面:
        治験薬投与中のWeek2およびWeek4の臨床検査値データにおいて、アルブミン低下およびBUN上昇が確認されています。これらの検査値異常について、臨床的意義、原因、患者の背景因子（既往歴、併用薬、食事摂取量、脱水 등）、治験薬との関連性、
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMTRTとDM.SEXの不整合, CM.CMSTDTCの日付形式, LB.BUNの変動と臨床的意義, LB.CREATの異常値, AEドメインのMedDRA用語関連の欠損値, CM.CMENDTC, AE.AEENDTC, AE.AEENDY, EX.EXENDTC, DS.DSTERM

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMTRT=PREMARIN, DM.SEX=M
    * 矛盾の内容: 併用薬PREMARINは女性ホルモン剤であり、DMドメインの性別が男性(M)であることと矛盾しています。
    * 問題点の原因（推測）: データ入力時の誤り、またはDMドメインの性別情報が誤っている可能性。
    * 対応策（提案）: 医療機関に性別および併用薬情報の再確認を依頼し、データの修正が必要か判断してください。

* 問題No.: 2
    * 変数名と値: CM.CMSTDTC=2000 (複数レコード)
    * 矛盾の内容: CMドメインのCMSTDTC（併用薬開始日）がYYYY-MM-DD形式ではなく、年のみのYYYY形式で入力されています。Define.xmlの定義ではDataType="date"となっており、形式が不適切です。
    * 問題点の原因（推測）: データ入力時の形式誤り。
    * 対応策（提案）: 医療機関にCMSTDTCの正しい日付形式での再入力を依頼してください。Define-xmlのDataType定義が正しい場合は、JSONデータの形式をYYYY-MM-DD形式に修正する必要があります。

* 問題No.: 3
    * 変数名と値: LB.LBTESTCD=BUN, LBORRES=29 mg/dL (Week 2)
    * 矛盾の内容: LBドメインのBlood Urea Nitrogen (BUN) が Week 2 で基準値上限を超えています (基準値上限はDefine.xmlより 24 mg/dL)。
    * 問題点の原因（推測）: 治験薬または併用薬の影響、あるいは疾患による影響、または検査値の一時的な変動。
    * 対応策（提案）: 医療機関にBUN値上昇の臨床的な意義、およびAEドメインに関連する有害事象の報告有無を確認してください。

* 問題No.: 4
    * 変数名と値: LB.LBTESTCD=CREAT, LBORRES=1.8 mg/dL (WEEK 2)
    * 矛盾の内容: LBドメインのCreatinine検査値が基準範囲上限を超えている。Define.xmlの定義から、LB.LBORNRLO=0.8, LBORNRHI=1.6 mg/dLが基準範囲。
    * 問題点の原因（推測）: データ入力時のエラー、または被験者の腎機能異常の可能性。
    * 対応策（提案）: データ入力時のエラーの可能性をデータマネジメント担当者に確認。医療機関にLB異常値の原因を確認し、医学的に問題がないか確認。

* 問題No.: 5
    * 変数名と値: AEドメインのAELLT, AELLTCD, AEDECOD, AEPTCD, AEHLT, AEHLTCD, AEHLGT, AEHLGTCD, AEBODSYS, AEBDSYCD, AESOC, AESOCCDがNULL
    * 矛盾の内容: AEドメインのMedDRA用語 (LLT, PT, HLT, HLGT, SOC) に関連する変数が、多くのレコードでNULL値となっている。Define.xml上は必須項目ではないが、AEデータの詳細を把握する上で重要な情報が欠落している可能性。
    * 問題点の原因（推測）: MedDRAコード化が未実施、またはコード化時に該当するMedDRA用語が見つからなかった可能性。データ収集・入力システムの不備により、MedDRA用語が適切に記録されなかった可能性。
    * 対応策（提案）: データマネジメント担当者にMedDRAコード化の状況を確認。MedDRA用語がNULLとなっているAEレコードについて、原資料（CRF等）を確認し、MedDRA用語が取得可能か確認。必要に応じて、臨床チームにMedDRA用語の選定について指示を仰ぐ。

* 問題No.: 6
    * 変数名と値: CM.CMENDTC (null), CM.CMENDY (null) (CMSEQ: 1, 2, 3, 5, 7, 10, 12, 14)
    * 矛盾の内容: CMドメインのアスピリンの併用薬終了日 (CMENDTC) および 併用薬終了時の試験日 (CMENDY) が複数レコードで欠損しており、併用薬の投与期間が不明です。
    * 問題点の原因（推測）: データ入力時の転記漏れ、または、意図的な欠損（例：継続中の薬剤のため終了日を記録しない運用）。
    * 対応策（提案）: CMドメインのデータ入力者に、アスピリンの併用状況と終了日について確認し、必要に応じてデータ修正を依頼してください。

* 問題No.: 7
    * 変数名と値: AE.AEENDTC (null), AE.AEENDY (null) (AESEQ: 8)
    * 矛盾の内容: AEドメインの有害事象（VENTRICULAR SEPTAL DEFECT）の終了日 (AEENDTC) および 有害事象終了時の試験日 (AEENDY) が欠損しており、有害事象の継続期間が不明です。
    * 問題点の原因（推測）: データ入力時の転記漏れ、または、意図的な欠損（例：継続中の有害事象のため終了日を記録しない運用）。
    * 対応策（提案）: AEドメインのデータ入力者に、VENTRICULAR SEPTAL DEFECT の有害事象の経過と終了日について確認し、必要に応じてデータ修正を依頼してください。

* 問題No.: 8
    * 変数名と値: AE.AETERM = "BRAIN DEATH", AE.AEOUT = "RECOVERED/RESOLVED"
    * 矛盾の内容: 有害事象が「脳死」であるにもかかわらず、転帰が「回復/解決」と記録されている。医学的に矛盾している。
    * 問題点の原因（推測）: AEドメインのデータ入力誤り（AEOUTの選択誤り）、またはAETERMのコーディング誤りの可能性。
    * 対応策（提案）: 医療機関にAE.AETERMとAE.AEOUTの記録が正しいか確認するクエリを発行。

* 問題No.: 9
    * 変数名と値: AE.AEENDTC ('2013-11-18'), AE.AEENDY (44), DS.DSSTDTC ('2013-11-24'), DS.DSSTDY (50) (AESEQ: 3, DSSEQ: 1)
    * 矛盾の内容: AEドメインの有害事象（BRAIN DEATH）終了日 (AEENDTC) が、DSドメインのADVERSE EVENT の Disposition Event 開始日 (DSSTDTC) よりも前になっており、時系列的に矛盾しています。
    * 問題点の原因（推測）: データ入力時の日付誤り、または、BRAIN DEATH と ADVERSE EVENT Disposition Event の関連性の誤解。
    * 対応策（提案）: AE および DS ドメインのデータ入力者に、BRAIN DEATH の有害事象と ADVERSE EVENT Disposition Event の関連性、および、日付の正当性について確認し、必要に応じてデータ修正を依頼してください。

* 問題No.: 10
    * 変数名と値: EX.EXENDTC ('2013-10-19'), EX.EXENDY (14), EX.EXSTDTC ('2013-10-20'), EX.EXSTDY (15) (EXSEQ: 1, 2)
    * 矛盾の内容: EXドメインの治験薬投与期間に重複が見られます。EXSEQ=1の治験薬投与終了日 (EXENDTC) が、EXSEQ=2の治験薬投与開始日 (EXSTDTC) よりも前になっています。
    * 問題点の原因（推測）: データ入力時の日付誤り、または、治験薬投与計画の意図しない変更。
    * 対応策（提案）: EXドメインのデータ入力者に、治験薬の投与計画と投与期間の正当性について確認し、必要に応じてデータ修正を依頼してください。

* 問題No.: 11
    * 変数名と値: DS.DSTERM (空白) (DSSEQ: 2)
    * 矛盾の内容: DSドメインのFINAL LAB VISIT の Disposition Event Term (DSTERM) が空白です。
    * 問題点の原因（推測）: データ入力時の転記漏れ。
    * 対応策（提案）: DSドメインのデータ入力者に、DSSEQ が 2 のレコードの DSTERM を確認し、適切な用語を追記するか、空白の理由を明確にしてください。

クエリ:
* 患者ID: 01-704-1017
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMTRT=PREMARIN, DM.SEX=M
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の併用薬 (CM) データについて、PREMARIN (CMSEQ=4, 6, 8, 12, 13, 14) が女性ホルモン剤ですが、DMドメインの性別 (SEX) が男性 (M) となっています。データ入力誤りの可能性がないか、医療機関に確認してください。
        * 判断理由: DM.SEXとCM.CMTRTの性別不整合は、データの信頼性を損なう可能性があり、臨床試験結果の解釈に影響を与える可能性があるため、Majorと判断。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMSTDTC=2000 (複数レコード)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の併用薬 (CM) データについて、CMSTDTC (Medication Start Date) が 2000 となっているレコードが複数ありますが、日付形式がYYYY-MM-DD形式と異なっています。データ入力時の誤りの可能性がないか、医療機関に確認してください。
        * 判断理由: CMSTDTCの日付形式の誤りは、データ品質上の問題であり、データクリーニングで修正可能と考えられるため、Minorと判断。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=BUN, LBORRES=29 mg/dL (Week 2)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の臨床検査 (LB) データについて、Blood Urea Nitrogen (BUN) が Week 2 で 29 mg/dL と基準値上限を超えています。 AE (Adverse Event) ドメインで関連する有害事象の報告有無と、臨床的な意義について医療機関に確認してください。
        * 判断理由: LB検査値の一時的な逸脱であり、AEとの直接的な関連性が不明なため、Minorと判断。ただし、医学的評価が必要な可能性があるため、医療機関への確認を推奨。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=CREAT, LBORRES=1.8 mg/dL (WEEK 2)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 のWEEK 2 (2013-10-19) の臨床検査値データについて質問です。LBTESTCD=CREAT (クレアチニン) の検査値が 1.8 mg/dL と基準範囲上限 (1.6 mg/dL) を超えています。考えられる原因と、医学的な解釈についてご教示いただけますでしょうか。再検査の必要性についてもご検討ください。
        * 判断理由: クレアチニン高値は腎機能障害を示唆する可能性があり、患者の安全性に関わる重要な情報であるため、医療機関への確認が必要と判断しました。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AETERM = "BRAIN DEATH", AE.AEOUT = "RECOVERED/RESOLVED"
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 のAEドメインの有害事象（AE.AETERM）が「脳死」と記録されていますが、転帰（AE.AEOUT）が「回復/解決」となっています。AE.AETERMとAE.AEOUTの記録に矛盾がないか、医学的に妥当な転帰であるか確認してください。
        * 判断理由: AE.AETERMとAE.AEOUTの単一ドメイン内整合性に関する疑義。有害事象の重篤度と転帰の妥当性を確認するため。

    * クエリNo.: 6
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AEENDTC ('2013-11-18'), AE.AEENDY (44), DS.DSSTDTC ('2013-11-24'), DS.DSSTDY (50) (AESEQ: 3, DSSEQ: 1)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の 有害事象（BRAIN DEATH）終了日と、ADVERSE EVENT の Disposition Event 開始日の時系列に矛盾が見られます。それぞれのイベント発生日と関連性についてご教示ください。
        * 判断理由: データ整合性の問題。時系列矛盾はデータ解釈に影響を与える可能性があり、正確な情報を把握する必要がある。

    * クエリNo.: 7
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: EX.EXENDTC ('2013-10-19'), EX.EXENDY (14), EX.EXSTDTC ('2013-10-20'), EX.EXSTDY (15) (EXSEQ: 1, 2)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の 治験薬投与期間に重複が見られます。治験薬の投与計画と投与期間についてご教示ください。
        * 判断理由: データ整合性の問題。治験薬投与期間の重複は、薬物曝露量や有効性評価に影響を与える可能性があり、正確な情報を把握する必要がある。

    * クエリNo.: 8
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC (null), CM.CMENDY (null) (CMSEQ: 1, 2, 3, 5, 7, 10, 12, 14)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 のConcomitant Medication (CM) ドメインのレコード (CMSEQ: 1, 2, 3, 5, 7, 10, 12, 14) において、Medicationの終了日 (CMENDTC, CMENDY) が欠損しています。Medicationの終了日を確認し、ご回答ください。
        * 判断理由: データ品質の向上。アスピリンは継続的な使用が想定される薬剤であり、終了日が欠損している理由を確認する必要がある。

    * クエリNo.: 9
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: AE.AEENDTC (null), AE.AEENDY (null) (AESEQ: 8)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 のAdverse Event (AE) ドメインのレコード (AESEQ: 8) において、Adverse Eventの終了日 (AEENDTC, AEENDY) が欠損しています。Adverse Eventの終了日を確認し、ご回答ください。
        * 判断理由: データ品質の向上。有害事象の経過を正確に把握するため、終了日を確認する必要がある。

    * クエリNo.: 10
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: DS.DSTERM (空白) (DSSEQ: 2)
        * 医療機関への問い合わせ文面: 患者ID 01-704-1017 の FINAL LAB VISIT の Disposition Event Term (DSTERM) が空白ですが、適切な用語をご教示ください。
        * 判断理由: データ品質の向上。DSTERM は DISPOSITION EVENT ドメインの主要な情報であり、適切な用語を記録することが望ましい。
## Task3: Protocol Deviation Review Results
患者ID: 01-704-1017
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: LB.LBTESTCD=CREAT, LB.LBORRES=1.8 mg/dL
    *   逸脱内容: スクリーニング1 (VISITNUM=1) において、臨床検査値Creatinine (クレアチニン) が基準値上限を超過 (LBORRES=1.8 mg/dL, LBORNRHI=1.6 mg/dL)。プロトコルで規定された除外基準 (EXCL27) に抵触する可能性があります。
    *   プロトコル該当箇所: TI.EXCL27
    *   判断理由: プロトコル除外基準EXCL27では、Laboratory test values exceeding the Lilly Reference Range IIIが規定されており、本データにおいて基準値上限超過が確認されたため、プロトコル逸脱の疑いがあると判断しました。

*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, VERBATIM_0572, VERBATIM_0608, VERBATIM_0806, VERBATIM_0811, VERBATIM_0954, VERBATIM_1153, VERBATIM_1486, VERBATIM_1608, MHCAT=PRIMARY DIAGNOSIS, SIGNIFICANT PRE-EXISTING CONDITION, HISTORICAL DIAGNOSIS
    *   逸脱内容: Medical History (MH) ドメインに、アルツハイマー病および複数の心疾患関連病名 (CARDIAC DISORDER, MYOCARDIAL INFARCTION, HEART ATTACK, TRIPLE VESSEL BYPASS GRAFT, SKIPPED BEATS) の既往歴が記録されています。選択基準 INCL02 (アルツハイマー病の診断) を満たすか、除外基準 EXCL17 (過去5年以内の重篤な心血管障害の既往歴) に抵触するかが不明確であり、プロトコル逸脱の疑いがあります。
    *   プロトコル該当箇所: TI.INCL02, TI.EXCL17
    *   判断理由: Medical History にアルツハイマー病および複数の心疾患の記載があり、選択基準 INCL02 の確認、および除外基準 EXCL17 に抵触する可能性が懸念されるため、プロトコル逸脱の疑いがあると判断しました。

*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMTRT=ASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN
    *   逸脱内容: Concomitant Medications (CM) ドメインに、併用薬としてASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN が記録されています。プロトコルに併用禁止薬リストの記載がなく、これらの薬剤が併用可能か不明なため、プロトコル逸脱の疑いとして検出します。
    *   プロトコル該当箇所: プロトコルの Concomitant Therapy (併用療法) セクション (詳細なリストは添付資料に記載されている可能性あり)
    *   判断理由: プロトコル本文およびDefine.xmlには併用禁止薬リストの記載が確認できませんでした。しかし、一般的に臨床試験プロトコルには併用禁止薬に関する規定が存在することが多いため、プロトコル逸脱の可能性を考慮し、疑義ありとして検出しました。

患者ID: 01-704-1017
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: LB.LBTESTCD=CREAT, LB.LBORRES=1.8 mg/dL
    *   医療機関への問い合わせ文面:
        被験者01-704-1017のスクリーニング1におけるクレアチニン値1.8 mg/dLについて、以下の点をご確認ください。

        1.  当該値は、プロトコルで規定された除外基準EXCL27（Laboratory test values exceeding the Lilly Reference Range III）に抵触しますか？ Lilly Reference Range III におけるクレアチニンの基準範囲と、逸脱の有無についてご回答ください。
        2.  除外基準に抵触する場合、治験責任医師は組み入れ基準/除外基準を逸脱したにも関わらず、当該被験者を登録した理由をご教示ください。
        3.  治験継続の可否について、治験依頼者の方針をご指示ください。

    *   判断理由: プロトコル逸脱の可能性 (選択基準逸脱) があり、治験継続の可否、データの取り扱いについて確認が必要となるため、医療機関への問い合わせが必須と判断しました。

*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: MH.MHTERM=ALZHEIMER'S DISEASE, VERBATIM_0572, VERBATIM_0608, VERBATIM_0806, VERBATIM_0811, VERBATIM_0954, VERBATIM_1153, VERBATIM_1486, VERBATIM_1608
    *   医療機関への問い合わせ文面:
        被験者01-704-1017のMedical History (MH) ドメインに記載された既往歴について、以下の点をご確認ください。

        1.  Medical History に記載されている心疾患 (CARDIAC DISORDER, MYOCARDIAL INFARCTION, HEART ATTACK, TRIPLE VESSEL BYPASS GRAFT, SKIPPED BEATS) の詳細 (各疾患名、発症時期、重症度、治療内容、直近5年以内の発症の有無など) を教えてください。除外基準 EXCL17 (過去5年以内の重篤な心血管障害の既往歴) に抵触しないか確認するため。
        2.  Medical History に PRIMARY DIAGNOSIS として ALZHEIMER'S DISEASE の記載がありますが、Inclusion criteria INCL02 (アルツハイマー病の診断) を満たすことを確認できる医学的資料 (診断基準、検査結果など) をご提供ください。

    *   判断理由: 選択基準 INCL02 および 除外基準 EXCL17 への抵触の疑義があるため、詳細な情報を医療機関に確認し、プロトコル逸脱の有無を判断する必要があるため、医療機関への問い合わせが必要と判断しました。

*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Major
    *   変数名と値: CM.CMTRT=ASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN
    *   医療機関への問い合わせ文面:
        治験薬と併用が懸念される薬剤について、プロトコル上の扱いと被験者の併用状況を確認させてください。

        1.  プロトコルにおいて、ASPIRIN (アスピリン), HYDROCORTISONE, TOPICAL (ヒドロコルチゾン外用薬), PREMARIN (プレマリン、結合型エストロゲン) は併用禁止薬に指定されていますか？ 併用禁止薬リスト、または併用に関する規定があればご提供ください。
        2.  被験者01-704-1017に投与された併用薬（ASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN）について、プロトコルにおける併用可否の判断と、併用が許可されている場合はその理由と根拠をご教示ください。

    *   判断理由: 併用薬 ASPIRIN, HYDROCORTISONE, TOPICAL, PREMARIN のプロトコル上の扱いが不明であり、プロトコル逸脱に該当する可能性があるため、医療機関への問い合わせが必要と判断しました。

# 01-701-1363
## Task1: Clinical Review Results
**患者ID:** 01-701-1363
* 2013年06月12日 (Day 14): ヘモグロビン値が基準範囲を下回る (LOW)。
* 2013年07月10日 (Day 42): ヘマトクリット値、ヘモグロビン値、白血球数が基準範囲を下回る (HCT: LOW, HGB: LOW, WBC: LOW)。
* 2013年07月16日 (Day 48): 軽度の適用部位そう痒症 (APPLICATION SITE PRURITUS) が発現。
* 2013年07月24日 (Day 56): 白血球数が基準範囲を下回る (WBC: LOW)。
* 2013年08月21日 (Day 84): ヘマトクリット値、ヘモグロビン値、赤血球数が基準範囲を下回る (HCT: LOW, HGB: LOW, RBC: LOW)。
* 2013年10月13日 (Day 137): 軽度の背部痛 (BACK PAIN) が発現。
* 2013年10月14日 (Day 138): ヘモグロビン値が基準範囲を下回る (HGB: LOW)。
* 2013年10月15日 (Day 139): 背部痛 (BACK PAIN) が未回復/未解決。
* 2013年11月13日 (Day 168): ヘモグロビン値が基準範囲を下回る (HGB: LOW)。背部痛 (BACK PAIN) が回復/解決。
* 2013年11月27日 (Day 182): ヘモグロビン値、白血球数が基準範囲を下回る (HGB: LOW, WBC: LOW)。

---
**患者ID:** 01-701-1363
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LBTESTCD = HCT, HGB, RBC, WBC (ヘマトクリット、ヘモグロビン、赤血球数、白血球数)
    * 医療機関への問い合わせ文面: 血液検査値（ヘマトクリット、ヘモグロビン、赤血球数、白血球数）が基準値範囲を下回る傾向にあります。臨床的な意義と、試験継続の可否について、専門医のご意見を伺いたいと存じます。特に、貧血や白血球減少症のリスク、および処置についてご教示ください。
    * 判断理由: 複数の血液検査項目で基準範囲を下回る値が継続的に認められており、Grade 3の貧血や白血球減少症に該当する可能性があります。患者の安全性に影響を与える懸念があるため、臨床的な意義を確認する必要があります。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMドメイン (併用薬), LBドメイン (検査値)
    * 医療機関への問い合わせ文面: 併用薬（ASA、HYDROCORTISONE、ICY HOT、MAALOX、MOTRIN、MULTIVITAMIN）と、LBドメインで変動が認められる検査値との間に、臨床的に懸念される相互作用はありますでしょうか？医学的な見解をご教示ください。
    * 判断理由: 併用薬と検査値変動の関連性を評価し、医学的妥当性を確認するため。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: QSTESTCD=ACTOT, CIBIC (ADAS-Cog(11) Subscore, CIBIC)
    * 医療機関への問い合わせ文面: ADAS-Cog(11) Subscore および CIBIC+ の評価スコアが悪化傾向にありますが、認知機能と全般臨床症状の悪化は、臨床試験の評価項目に影響を与える可能性がありますでしょうか？医学的な見解をご教示ください。
    * 判断理由: 主要評価項目および副次評価項目である認知機能検査、全般臨床症状評価の悪化傾向について、臨床試験の評価項目に与える影響を確認するため。
## Task2: DM Review Results
全体的なデータ品質の評価:
総合評価: 一部問題あり
データクリーニング/再調査が必要な項目: 患者ID: 01-701-1363, 問題点No.1, 問題点No.2, 問題点No.3, 問題点No.4, 問題点No.5

問題点:
問題No.: 1
    変数名と値: AE.AESTDTC = 1986 (AESEQ=2, 4)
    矛盾の内容: AEドメインの複数の有害事象の開始日が1986年となっており、患者の年齢や試験期間と矛盾している。データ入力時の誤りの可能性が高い。
問題点の原因（推測）: データ入力時の誤り
対応策（提案）: 医療機関に original source data を確認し、AESTDTC を修正する必要があります。

問題No.: 2
    変数名と値: CM.CMDTC, CM.CMSTDTC (複数レコード)
    矛盾の内容: CMドメインにおいて、データ収集日CMDTCが、併用薬開始日CMSTDTCよりも後の日付になっているレコードが複数存在する。データ入力またはデータ収集プロセスの誤りの可能性。
問題点の原因（推測）: データ入力時の日付誤りの可能性、またはデータ収集プロセスの不備の可能性。
対応策（提案）: 医療機関にCMドメインのCMDTCとCMSTDTCの日付の整合性について確認し、必要に応じてデータ修正を依頼してください。

問題No.: 3
    変数名と値: CM.CMENDTC, CM.CMENDY (複数レコード)
    矛盾の内容: CMドメインの併用薬データにおいて、CMENDTCとCMENDYが複数レコードで欠損。投与期間が重要な情報となる薬剤の終了日が不明な理由を確認する必要がある。
問題点の原因（推測）: データ入力時の欠落、またはPRN (必要時) 投与の薬剤で投与期間が定まっていない可能性。
対応策（提案）: CMENDTC, CMENDYが欠損しているレコードについて、医療機関に併用薬の投与終了日を確認するクエリを発行してください。PRN投与の薬剤であれば、投与終了日を記録する必要があるか、データ収集手順を確認してください。

問題No.: 4
    変数名と値: LB.LBTESTCD = BILI, LB.LBORRES = <0.2, LB.LBSTRESN = null
    矛盾の内容: LBドメインのビリルビン検査値レコードで、LBORRESが範囲値("<0.2")であるにもかかわらず、LBSTRESNがnull。Define.xmlの定義とデータの不整合。
問題点の原因（推測）: "<0.2"という範囲値は数値に変換できないため、LBSTRESNにnullが格納されたと考えられます。
対応策（提案）: Define.xmlの定義 अनुसार、LBSTRESNには数値データを格納するようにデータ修正を検討してください。もし範囲値をLBSTRESNに格納することが必須の場合、Define.xmlの修正を検討してください (DataTypeをstringに変更するなど)。臨床的に意義のある値として扱うために、例えば"<0.2"を数値の"0.1"などに変換することを検討してください。

問題No.: 5
    変数名と値: LB.LBTESTCD = HGB, LBNRIND = LOW (複数レコード)
    矛盾の内容: LBドメインでヘモグロビン値が複数回LOWと判定されているが、AEドメインに貧血関連の有害事象報告がない。臨床的な解釈と対応を確認する必要がある。
問題点の原因（推測）: 患者が貧血を合併しているにもかかわらず、有害事象として報告されていない。または、検査値異常が臨床的に重要でないと判断され、有害事象として報告されなかった可能性。
対応策（提案）: 医療機関にHGB値がLOWであることの臨床的な解釈を確認するクエリを発行してください。貧血に関連する有害事象の有無、およびHGB値低下に対する処置の有無を確認してください。

クエリ:
患者ID: 01-701-1363
クエリNo.: 1
    臨床試験結果への影響度合い: Critical
    変数名と値: AE.AESTDTC = 1986 (AESEQ=2, 4)
    医療機関への問い合わせ文面: 患者ID 01-701-1363 の有害事象データについて、AESTDTC（有害事象開始日）が1986年となっているAESEQ=2, 4のレコードはデータ入力の誤りではないでしょうか。Original source data を確認いただき、正しい日付をご教示ください。
    判断理由: AESTDTC の誤りはデータ品質に重大な影響を与えるため、最優先で確認が必要。

クエリNo.: 2
    臨床試験結果への影響度合い: Major
    変数名と値: CM.CMDTC, CM.CMSTDTC (複数レコード)
    医療機関への問い合わせ文面: 患者ID 01-701-1363 の併用薬データについて、データ収集日CMDTCが併用薬開始日CMSTDTCよりも後の日付になっているレコードが複数あります。記録されている日付が正しいか確認いただけますでしょうか。もし誤りがある場合は、正しい日付への修正をお願いいたします。
    判断理由: CMドメインの日付矛盾はデータの論理的な整合性に関わる問題であり、早急な確認と修正が必要。

クエリNo.: 3
    臨床試験結果への影響度合い: Major
    変数名と値: CM.CMENDTC, CM.CMENDY (複数レコード)
    医療機関への問い合わせ文面: 併用薬[薬剤名: (CMTRTの値), CMSEQ: (CMSEQの値)]の投与終了日 (CMENDTC) と投与終了日（治験薬投与からの日数）(CMENDY) が欠損しています。投与終了日を確認し、ご回答ください。PRN投与の薬剤の場合、投与終了日の記録は必須でしょうか？
    判断理由: 併用薬の投与期間は安全性評価に重要であり、欠損値の理由と対応を確認する必要があるため。

クエリNo.: 4
    臨床試験結果への影響度合い: Major
    変数名と値: LB.LBTESTCD = HGB, LBNRIND = LOW (複数レコード)
    医療機関への問い合わせ文面: 患者ID 01-701-1363 の臨床検査値データにおいて、ヘモグロビン値が複数回LOWと判定されています。貧血に関連する有害事象は報告されていませんが、HGB値低下の原因、および臨床的な解釈についてご教示いただけますでしょうか。また、HGB値低下に対して何らかの処置が実施された場合は、その内容についてもご教示ください。
    判断理由: HGB値低下は患者の安全性に関わる可能性があり、医学的解釈と対応を確認する必要があるため。

クエリNo.: 5
    臨床試験結果への影響度合い: Minor
    変数名と値: LB.LBTESTCD = BILI, LB.LBORRES = <0.2, LB.LBSTRESN = null
    医療機関への問い合わせ文面: LBドメインのビリルビン検査値データで、LBORRES（オリジナル値）が"<0.2"となっているレコードがありますが、LBSTRESN（標準値）がnullとなっています。LBSTRESNに適切な値を入力いただくか、LBSTRESNに範囲値を格納する場合の対応についてご検討いただけますでしょうか。
    判断理由: LBSTRESNのnull値はデータ品質上の問題であり、修正または対応を検討する必要があるが、臨床的な緊急性は高くないと判断。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1363
*   逸脱No.: 1
    *   臨床試験結果への影響度合い: Major (アシスタント1, 4), Minor (アシスタント2)
    *   変数名と値: CMTRT = ASA, CMDECOD = UNCODED, CMSTDTC = 1986
    *   逸脱内容: 被験者01-701-1363は、複数のVisitにおいてASA（アスピリン）を併用薬として使用しており、プロトコルで併用禁止薬に指定されている可能性がある。
    *   プロトコル該当箇所: プロトコル3.8項 併用療法、3.4.2.2項 除外基準 (併用禁止薬リストが記載されている場合)
    *   判断理由: ASAは抗血小板薬であり、臨床試験の種類によっては併用が禁止される場合がある。プロトコルに併用禁止薬リストの記載があれば確認が必要。アシスタント1, 4は臨床試験結果への影響度合いをMajor、アシスタント2はMinorと評価しているが、安全性を考慮し、より影響度の高いMajorの可能性も考慮して判断する。

*   逸脱No.: 2
    *   臨床試験結果への影響度合い: Minor (アシスタント2, 3, 4)
    *   変数名と値: CMTRT = HYDROCORTISONE, CMDECOD = HYDROCORTISONE, CMSTDTC = 2013-09-19
    *   逸脱内容: 被験者01-701-1363は、複数のVisitにおいてHYDROCORTISONE（ヒドロコルチゾン）を併用薬として使用しており、プロトコルで併用禁止薬に指定されている可能性がある。
    *   プロトコル該当箇所: プロトコル3.8項 併用療法、3.4.2.2項 除外基準 (併用禁止薬リストが記載されている場合)
    *   判断理由: HYDROCORTISONEは副腎皮質ステロイドであり、臨床試験の種類によっては併用注意が必要となる場合がある。プロトコルに併用禁止薬リストの記載があれば確認が必要。アシスタント2, 3, 4は臨床試験結果への影響度合いをMinorと評価している。

*   逸脱No.: 3
    *   臨床試験結果への影響度合い: Minor (アシスタント2, 4)
    *   変数名と値: CMTRT = MOTRIN, CMDECOD = UNCODED, CMSTDTC = 2013-10-01
    *   逸脱内容: 被験者01-701-1363は、WEEK 20のVisitにおいてMOTRIN（イブプロフェン）を併用薬として使用しており、プロトコルで併用禁止薬に指定されている可能性がある。
    *   プロトコル該当箇所: プロトコル3.8項 併用療法、3.4.2.2項 除外基準 (併用禁止薬リストが記載されている場合)
    *   判断理由: MOTRIN（イブプロフェン）はNSAIDsであり、臨床試験の種類によっては併用注意が必要となる場合がある。プロトコルに併用禁止薬リストの記載があれば確認が必要。アシスタント2, 4は臨床試験結果への影響度合いをMinorと評価している。

*   逸脱No.: 4
    *   臨床試験結果への影響度合い: Minor (アシスタント5)
        *   変数名と値: LB.HGB = 10.8 g/dL (WEEK 6), 10.3 g/dL (WEEK 12), 11.3 g/dL (WEEK 16), 11.2 g/dL (WEEK 20), 10.9 g/dL (WEEK 24), 11.4 g/dL (WEEK 26)
        *   逸脱内容: 被験者01-701-1363において、複数回にわたりヘモグロビン値が基準値下限を下回っている。
        *   プロトコル該当箇所: プロトコル除外基準27, 28
        *   判断理由: LBドメインのデータにおいて、ヘモグロビン値が複数回にわたり基準値下限を下回っている。貧血を示唆する可能性があり、患者の安全性に影響を与える可能性がある。現時点では臨床的な重篤度や治験薬との因果関係は不明なため、Minor逸脱と判断。

患者ID: 01-701-1363
*   クエリNo.: 1
    *   臨床試験結果への影響度合い: Major (アシスタント4), None (アシスタント1, 2, 3, 5)
    *   変数名と値: CMTRT = ASA, CMDECOD = UNCODED, CMSTDTC = 1986
    *   医療機関への問い合わせ文面:
        被験者01-701-1363の併用薬ASA（アスピリン）の使用について確認させてください。プロトコルで規定されている併用禁止薬リストにASAは含まれていますでしょうか。もし含まれている場合、投与開始日（1986）と試験期間が重複しているため、プロトコル逸脱となる可能性があります。ASA使用の医学的妥当性と、治験薬への影響について評価をお願いします。
    *   判断理由: ASAは臨床試験において注意が必要な併用薬であり、プロトコルで併用が禁止されている可能性があります。ASAの使用がプロトコル逸脱に該当するかどうか、また臨床試験結果に与える影響を評価するため、医療機関への確認が必要です。アシスタント4は臨床試験結果への影響度合いをMajorと評価。

*   クエリNo.: 2
    *   臨床試験結果への影響度合い: Minor (アシスタント4), None (アシスタント1, 2, 3, 5)
    *   変数名と値: CMTRT = HYDROCORTISONE, CMDECOD = HYDROCORTISONE, CMSTDTC = 2013-09-19
    *   医療機関への問い合わせ文面:
        被験者01-701-1363の併用薬HYDROCORTISONE（ヒドロコルチゾン）の使用について確認させてください。プロトコルで規定されている併用禁止薬リストにHYDROCORTISONEは含まれていますでしょうか。もし含まれている場合、投与開始日（2013-09-19）と試験期間が重複しているため、プロトコル逸脱となる可能性があります。HYDROCORTISONE使用の医学的妥当性と、治験薬への影響について評価をお願いします。
    *   判断理由: HYDROCORTISONEは臨床試験において注意が必要な併用薬であり、プロトコルで併用が禁止されている可能性があります。HYDROCORTISONEの使用がプロトコル逸脱に該当するかどうか、また臨床試験結果に与える影響を評価するため、医療機関への確認が必要です。アシスタント4は臨床試験結果への影響度合いをMinorと評価。

*   クエリNo.: 3
    *   臨床試験結果への影響度合い: Minor (アシスタント4), None (アシスタント1, 2, 3, 5)
    *   変数名と値: CMTRT = MOTRIN, CMDECOD = UNCODED, CMSTDTC = 2013-10-01
    *   医療機関への問い合わせ文面:
        被験者01-701-1363の併用薬MOTRIN（イブプロフェン）の使用について確認させてください。プロトコルで規定されている併用禁止薬リストにMOTRINは含まれていますでしょうか。もし含まれている場合、投与期間（2013-10-01 - 2013-10-01）が試験期間と重複しているため、プロトコル逸脱となる可能性があります。MOTRIN使用の医学的妥当性と、治験薬への影響について評価をお願いします。
    *   判断理由: MOTRIN（イブプロフェン）はNSAIDsであり、臨床試験の種類によっては併用注意が必要となる場合がある。MOTRINの使用がプロトコル逸脱に該当するかどうか、また臨床試験結果に与える影響を評価するため、医療機関への確認が必要です。アシスタント4は臨床試験結果への影響度合いをMinorと評価。

# 01-703-1335
## Task1: Clinical Review Results
**1. 症例サマリーの作成:**

**患者ID:** 01-703-1335
* 2014年02月21日 (Day -24): 検査値 (Creatine Kinase) が基準値上限超え (209 U/L)。
* 2014年03月15日 (Day 15): 有害事象 MULTIPLE SCLEROSIS RELAPSE (軽度) 発現。
* 2014年03月15日 (Day 15): 有害事象 ATRIOVENTRICULAR BLOCK SECOND DEGREE (軽度) 発現。
* 2014年03月31日 (Day 15): 検査値 (Creatine Kinase) が基準値上限超え (219 U/L)。
* 2014年03月30日 (Day 14): 有害事象 ATRIOVENTRICULAR BLOCK SECOND DEGREE (軽度) 軽快。
* 2014年05月01日 (Day 46): 有害事象 MULTIPLE SCLEROSIS RELAPSE (軽度) は未回復。
* 2014年05月24日 (Day 69): 治験薬投与中止 (PROTOCOL VIOLATION)。

---

**2. クエリの作成 (必要な場合のみ):**

**患者ID:** 01-703-1335
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: DSDECOD = PROTOCOL VIOLATION, DSTERM = PROTOCOL VIOLATION, DSDTC = 2014-05-24
    * 医療機関への問い合わせ文面:
        * 患者ID: 01-703-1335 の治験薬投与終了理由が「PROTOCOL VIOLATION (プロトコル違反)」と報告されています。具体的にどのようなプロトコル違反があったのか、詳細をご教示ください。
    * 判断理由: 治験薬の早期中止は、有効性および安全性評価に重大な影響を与える可能性があります。プロトコル違反の内容を把握し、臨床試験への影響を評価する必要があります。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: AEAETERM = MULTIPLE SCLEROSIS RELAPSE, MHDECOD = ALZHEIMER'S DISEASE
    * 医療機関への問い合わせ文面:
        * 患者ID: 01-703-1335 において、有害事象として「MULTIPLE SCLEROSIS RELAPSE (多発性硬化症再発)」が報告されていますが、Medical History (既往歴) には「ALZHEIMER'S DISEASE (アルツハイマー病)」のみが記載されており、「MULTIPLE SCLEROSIS (多発性硬化症)」の記載はありません。
        * 報告された有害事象「MULTIPLE SCLEROSIS RELAPSE」は、Medical Historyの記載誤りである可能性はないでしょうか。Medical Historyに「MULTIPLE SCLEROSIS」の既往歴がある場合、選択・除外基準に抵触する可能性があります。
        * もしMedical Historyの記載が誤りではなく、新規の有害事象の報告である場合、詳細な医学的情報と治験薬との因果関係についてご教示ください。
    * 判断理由: Medical HistoryとAdverse Eventの記載内容に矛盾があり、データの正確性を確認する必要があります。Medical Historyの誤りである場合、選択・除外基準の逸脱、安全性評価に影響を与える可能性があります。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LBTESTCD = CK, LBNRIND = HIGH
    * 医療機関への問い合わせ文面:
        * 患者ID: 01-703-1335 において、検査値 CK (Creatine Kinase) が複数回にわたり基準値上限を超えています。
        * 2014年02月21日 (Day -24) に 209 U/L、2014年03月31日 (Day 15) に 219 U/Lと高値を示していますが、その原因、医学的な意義についてご教示ください。
        * また、CK上昇に対して医療機関としてどのような対応をとられたか、ご教示ください。
    * 判断理由: 治験薬投与下でCK上昇が複数回認められており、患者の安全性評価のため、臨床的な意義と対応を確認する必要があります。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AESTDTC, EX.EXSTDTC, DS.DSSTDTC, SV.SVENDTC, LB.LBORRES (CK), CMドメイン

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC, EX.EXSTDTC (AEレコード1, 2)
    * 矛盾の内容: AEドメインの複数の有害事象レコードで、有害事象開始日 (AESTDTC) がEXドメインの治験薬投与開始日 (EXSTDTC) より前になっている。具体的には、AEレコード1のAESTDTC (2014-04-01) がEX row 1のEXSTDTC (2014-03-17) より遅い日付である一方、AEレコード2のAESTDTC (2014-03-15) はEX row 1のEXSTDTCより早い日付となっている。
    * 問題点の原因（推測）: データ入力時の誤り、または有害事象と治験薬投与の時系列に関する記録の誤り、定義解釈の相違の可能性。
    * 対応策（提案）: 医療機関にAE発現日と治験薬投与開始日の記録を照合し、矛盾の原因特定とデータ修正の要否を確認する。

* 問題No.: 2
    * 変数名と値: DS.DSSTDTC, SV.SVENDTC (DSレコード1, SVレコードWEEK 6, WEEK 7)
    * 矛盾の内容: DSドメインのDisposition Event Start Date (DSSTDTC) とSVドメインのSubject Visits End Date (SVENDTC) が同じ日付 (2014-05-24) であり、DSレコード (PROTOCOL VIOLATION, FINAL LAB VISIT) の内容とSVドメインのWEEK 7訪問データの存在が矛盾している可能性がある。
    * 問題点の原因（推測）: SVドメインのWEEK 7データ誤登録、DSデータ登録日の調整、またはデータ入力時の解釈の相違。
    * 対応策（提案）: 医療機関に最終訪問日、データ登録日、SVドメインWEEK 7データの正当性を確認し、必要に応じてデータ修正を依頼する。

* 問題No.: 3
    * 変数名と値: CMドメイン (データセット全体)
    * 矛盾の内容: CMドメインにデータレコードが1件も存在しない。併用薬データが欠損している。
    * 問題点の原因（推測）: データ抽出/登録漏れ、または併用薬データが意図的に収集されなかった可能性。Define.xmlにはCMドメインの定義が存在するため、データ収集が意図されていた可能性が高い。
    * 対応策（提案）: 医療機関にCMドメインのデータ収集状況を確認し、未収集の場合はデータ収集手順の見直しとデータ入力、またはデータ提供を依頼する。

* 問題No.: 4
    * 変数名と値: LB.LBTESTCD=CK, LB.LBORRES=209, 219 U/L, LB.LBORNRLO=21 U/L, LB.LBORNRHI=169 U/L (LBレコード30, 67)
    * 矛盾の内容: LBドメインの検査項目 CK (Creatine Kinase) が、複数回にわたり基準範囲上限 (LB.LBORNRHI=169 U/L) を超える高値 (LB.LBORRES=209, 219 U/L) を示している。
    * 問題点の原因（推測）: データ入力ミス、または被験者の臨床検査値異常の可能性。
    * 対応策（提案）: 医療機関にLB検査値 (CK) の異常値の原因、臨床的意義、およびAEドメインへの関連有害事象の報告有無を確認する。

* 問題No.: 5
    * 変数名と値: AE.AESTDTC, AE.AEDTC (AEレコード2)
    * 矛盾の内容: AEドメインのレコード2において、有害事象開始日 (AESTDTC: 2014-03-15) がデータ収集日 (AEDTC: 2014-03-31) より早い日付となっている。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータ収集日の記録誤りの可能性。
    * 対応策（提案）: 医療機関にAESTDTCとAEDTCの日付の記録を確認し、必要に応じて修正を依頼する。

クエリ:
* 患者ID: 01-703-1335
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC, EX.EXSTDTC (AEレコード1, 2)
        * 医療機関への問い合わせ文面:
            患者ID 01-703-1335 の有害事象データについて、治験薬投与開始日と有害事象発現日の矛盾が複数箇所で確認されました。
            AEレコード1 (事象名: MULTIPLE SCLEROSIS RELAPSE) およびAEレコード2 (事象名: ATRIOVENTRICULAR BLOCK SECOND DEGREE) の有害事象開始日 (AESTDTC) と、治験薬投与開始日 (EX.EXSTDTC=2014-03-17) の記録に誤りがないか、 Medical Record 等で確認をお願いいたします。
            もし記録に誤りがある場合は、正しい日付をご教示ください。
        * 判断理由: クロスドメイン整合性レビューで、治験薬投与開始日と有害事象発現日の矛盾が複数認められ、データの信頼性に関わる重要な問題であるため、早急な確認と修正が必要と判断した。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=CK, LB.LBORRES=209, 219 U/L (LBレコード30, 67)
        * 医療機関への問い合わせ文面:
            患者ID 01-703-1335 の臨床検査値データについて、LBドメインの検査項目CK (Creatine Kinase) で基準値上限を超える高値が複数回 (LBSEQ=30, 67) 報告されています。
            CK高値の原因として考えられる要因 (薬剤性、疾患等) 、および臨床的な意義について、Medical Record等で確認をお願いいたします。
            また、CK高値に関連する有害事象がAEドメインに報告されているかどうかも併せてご教示ください。
        * 判断理由: CK値異常は患者の安全性に関わる可能性があり、臨床試験の主要評価項目に影響を与える可能性があるため、Medical Record等の原資料確認による正確な情報把握と、臨床的な解釈、安全性評価に必要な情報を得るために、医療機関への問い合わせが必要と判断した。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CMドメイン (Concomitant Medications)
        * 医療機関への問い合わせ文面:
            患者ID 01-703-1335 の併用薬データ (CMドメイン) が登録されていません。
            Medication history 
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1335
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DS.DSDECOD=PROTOCOL VIOLATION, DS.DSTERM=PROTOCOL VIOLATION
        逸脱内容: 治験薬投与中にプロトコル逸脱が発生し、治験が中止されています。具体的な逸脱内容については不明です。
        プロトコル該当箇所: プロトコル全体、プロトコル逸脱に関する定義、治験中止基準
        判断理由: DSドメインに「PROTOCOL VIOLATION」の記述があり、治験中止の理由となっていることから、臨床試験の実施および結果に重大な影響を与えるプロトコル逸脱である可能性が高いと判断しました。

患者ID: 01-703-1335
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: DS.DSDECOD=PROTOCOL VIOLATION, DS.DSTERM=PROTOCOL VIOLATION
        医療機関への問い合わせ文面:
            患者ID 01-703-1335 のWEEK 6 (2014-05-24) に記録されているPROTOCOL VIOLATIONについて、詳細な内容（逸脱の種類、具体的な状況、逸脱理由、臨床試験結果に与える可能性のある影響など）をご教示ください。
        判断理由: DSドメインにプロトコル逸脱の記録があるにもかかわらず、JSONデータからは詳細な逸脱内容が不明であるため、医療機関への問い合わせが必要と判断しました。プロトコル逸脱の内容によっては臨床試験結果に重大な影響を与える可能性があるため、早急な内容の確認が必要です。

    クエリNo.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=CK, LBORRES=209, 219 (WEEK 2, WEEK 4), LBNRIND=HIGH (WEEK 2, WEEK 4)
        医療機関への問い合わせ文面:
            患者ID 01-703-1335 において、臨床検査値データCreatine Kinase (CK) が WEEK 2 と WEEK 4 で基準値上限を超過しています。
            詳細を確認させて頂きたく、以下の点についてご回答をお願いいたします。
            1. Creatine Kinase (CK) 高値について、臨床的な意義と患者様の状態についてご評価ください。
            2. Creatine Kinase (CK) 高値の原因として考えられる要因（治験薬の影響、合併症、 آزمایش های آزمایشگاهی のエラー等）についてご検討ください。
            3. Creatine Kinase (CK) 高値に対する再検査や препаративной 処置の実施状況についてご教示ください。
        判断理由: LBドメインの臨床検査値において、Creatine Kinase (CK) が基準値上限を超えているデータが複数回確認されました。CK値の上昇は、筋肉損傷や薬剤性ミオパチーなどが原因として考えられるため、念のため医療機関に問い合わせ、臨床的な意義や対応について確認する必要があると判断しました。

# 01-701-1383
## Task1: Clinical Review Results
患者ID: 01-701-1383
* 2013年02月07日 (Day 4): 適用部位そう痒症、適用部位疼痛が発現（いずれも軽度、治験薬との関連性はおそらくあり、転帰は回復）。
* 2013年03月23日 (Day 48): 適用部位紅斑、適用部位そう痒症が発現（いずれも軽度、治験薬との関連性は可能性あり）。適用部位紅斑は2013年03月26日(Day 51)に回復、適用部位そう痒症は未回復。
* 2013年04月12日 (Day 68): 適用部位紅斑、適用部位刺激感（投与部位灼熱感）、適用部位そう痒症が発現（適用部位紅斑、適用部位そう痒症は軽度、適用部位刺激感は中等度、治験薬との関連性はいずれも可能性あり、転帰はいずれも未回復）。
* 2013年05月07日 (Day 93): 適用部位小水疱が発現（軽度、治験薬との関連性は可能性あり、2013年05月24日(Day 110)に回復）。
* 2013年06月24日 (Day 141): 胸部不快感、頭痛が発現（いずれも軽度、治験薬との関連性は関連なし、2013年06月24日(Day 141)に回復）。
* 2013年07月17日 (Day 164): 血圧上昇、咳嗽が発現（いずれも中等度、治験薬との関連性は関連なし）。咳嗽は2013年07月26日 (Day 173)に回復、血圧上昇はYYYY年07月25日 (Day 172)に回復。

---
患者ID: 01-701-1383
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: CM.CMSTDTC = 2012-03 (複数レコード)
    * 医療機関への問い合わせ文面: 併用薬開始日 (CMSTDTC) がデータ収集日 (CMDTC) より過去の日付 (2012-03) となっているレコードが複数ありますが、データ入力時の誤りではないでしょうか。
    * 判断理由: CMドメインの併用薬開始日 (CMSTDTC) がデータ収集日 (CMDTC) より過去の日付になっていることは、データ矛盾と考えられます。併用薬の開始日がデータ収集日より過去であることは医学的にありえますが、2012年3月という日付はデータ収集日 (2013年) より1年以上前であり、データ入力誤りの可能性が高いと判断しました。データの正確性を確認するため、医療機関への問い合わせが必要と考えられます。
## Task2: DM Review Results
Error
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1383
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=CEPHALEXIN, CM.HYDROCORTISONE, CM.PROMETHAZINE HCL W/CODEINE
        逸脱内容: 併用薬としてCEPHALEXIN、HYDROCORTISONE、PROMETHAZINE HCL W/CODEINEが投与されている。これらの薬剤はプロトコルで併用禁止薬に指定されている可能性がある。
        プロトコル該当箇所: プロトコル 3.8 Concomitant Therapy, 3.4.2.2 Exclusion Criteria [31b] (併用禁止薬リストに関する記述)
        判断理由: CEPHALEXIN (抗生物質)、HYDROCORTISONE (ステロイド)、PROMETHAZINE HCL W/CODEINE (麻薬性鎮咳薬) は、臨床試験の結果に影響を与える可能性があり、プロトコルで併用が禁止されている可能性があるため、逸脱の疑いとして検出。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC=2012-03, DM.RFSTDTC=2013-02-04, CM.CMDTC=2013-01-22
        逸脱内容: 併用薬CENTRUM SILVERの開始日（CM.CMSTDTC=2012-03）が治験薬投与開始日（DM.RFSTDTC=2013-02-04）より前であるにもかかわらず、データ収集日（CM.CMDTC=2013-01-22）がMedication Start Date（CM.CMSTDTC）より大幅に後になっている。データ入力時の誤りの可能性がある。
        プロトコル該当箇所: プロトコルには併用薬のデータ収集に関する具体的な規定はないが、SDTMのCMドメインの定義、データマネジメントの一般的な原則
        判断理由: CMドメインとDMドメインのデータ内容に時間軸の矛盾が見られる。データ入力時の誤記の可能性、またはCMデータの記録方法に疑義があるため、データ品質上の懸念として検出。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMDECOD=UNCODED (複数レコード)
        逸脱内容: 複数の併用薬 (CENTRUM SILVER, CEPHALEXIN, PROMETHAZINE HCL W/CODEINEなど) のCMDECOD値がUNCODEDとなっている。標準的な薬剤名へのコーディングが実施されていない可能性があり、データ品質上の懸念がある。
        プロトコル該当箇所: データ品質に関する規定 (例: データコーディング手順、データ品質保証に関する規定)
        判断理由: CMDECODがUNCODEDであることは、データの標準化処理が不十分である可能性を示唆する。データ品質管理上の問題として検出。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMENDTC="", CM.CMENDY=null (HYDROCORTISONEなど一部レコード)
        逸脱内容: 一部の併用薬（HYDROCORTISONEなど）でCMENDTC（Medication End Date）とCMENDY（Medication End Day）が欠損しており、併用薬の使用期間が不明確。
        プロトコル該当箇所: プロトコルには併用薬のデータ収集に関する具体的な規定はないが、SDTMのCMドメインの定義、データマネジメントの一般的な原則
        判断理由: CMENDTCとCMENDYの欠損は、データ収集の不備またはデータ入力時の誤りの可能性がある。併用薬の使用状況を正確に把握するために、データ品質上の懸念として検出。

患者ID: 01-701-1383
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=CEPHALEXIN
        医療機関への問い合わせ文面: 
            被験者01-701-1383に併用されているCEPHALEXINについて、以下の点について回答してください。
            1. 投与理由と医学的妥当性
            2. 投与期間
            3. 治験薬および評価項目への影響
            4. CEPHALEXINはプロトコルで併用禁止薬に該当するか否か
            医学的に妥当である場合は、その理由と治験への影響について考察した文書をご提出ください。
        判断理由: CEPHALEXINはプロトコルで併用禁止薬に指定されている可能性があり、臨床試験結果への影響が懸念されるため、医療機関への問い合わせが必要。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=HYDROCORTISONE
        医療機関への問い合わせ文面: 
            被験者01-701-1383に併用されているHYDROCORTISONEについて、以下の点について回答してください。
            1. 投与理由と医学的妥当性
            2. 投与期間
            3. 治験薬および評価項目への影響
            4. HYDROCORTISONEはプロトコルで併用禁止薬に該当するか否か
            医学的に妥当である場合は、その理由と、治験への影響について考察した文書をご提出ください。
        判断理由: HYDROCORTISONEはプロトコルで併用禁止薬に指定されている可能性があり、臨床試験結果への影響が懸念されるため、医療機関への問い合わせが必要。

    クエリNo.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=PROMETHAZINE HCL W/CODEINE
        医療機関への問い合わせ文面: 
            被験者01-701-1383に併用されているPROMETHAZINE HCL W/CODEINEについて、以下の点について回答してください。
            1. 投与理由と医学的妥当性
            2. 投与期間
            3. 治験薬および評価項目への影響
            4. PROMETHAZINE HCL W/CODEINEはプロトコルで併用禁止薬に該当するか否か
            医学的に妥当である場合は、その理由と、治験への影響について考察した文書をご提出ください。
        判断理由: PROMETHAZINE HCL W/CODEINEはプロトコルで併用禁止薬に指定されている可能性があり、臨床試験結果への影響が懸念されるため、医療機関への問い合わせが必要。

# 01-701-1047
## Task1: Clinical Review Results
患者ID: 01-701-1047
* 2013年02月12日 (Day 1): HIATUS HERNIA (中等度) の有害事象が発現。
* 2013年02月25日 (Day 14): HIATUS HERNIA (中等度) の有害事象が回復/解消。検査値 Phosphate が基準範囲を下回り低い値 (3.0 mg/dL, 基準範囲: 2.2-5.1 mg/dL)。
* 2013年03月06日 (Day 23): UPPER RESPIRATORY TRACT INFECTION (軽度) の有害事象が発現。
* 2013年03月10日 (Day 27): 
    * バイタルサイン測定（立位）で拡張期血圧が高い値 (121 mmHg, 124 mmHg)。また、収縮期血圧も立位で高値 (185 mmHg, 183 mmHg) を示す。
    * 検査値 Phosphate が基準範囲を下回り低い値 (3.1 mg/dL, 基準範囲: 2.2-5.1 mg/dL)。
    * 有害事象 HYPERTENSION (軽度), LEFT BUNDLE BRANCH BLOCK (軽度) が発現。
    * 併用薬としてROBITUSSIN-DMとSUDAFEDを開始。
    * UPPER RESPIRATORY TRACT INFECTION (軽度) の有害事象が未回復/未解消。
* 2013年03月29日 (Day 46): 検査値 Phosphate が基準範囲を下回り低い値 (2.5 mg/dL, 基準範囲: 2.2-5.1 mg/dL)。
* 2013年04月07日 (Day 55): 検査値 Phosphate が基準範囲を下回り低い値 (2.5 mg/dL, 基準範囲: 2.2-5.1 mg/dL)。
* 2013年07月28日 (Day 167): 質問票(NPI-X) Disinhibition スコア悪化 (Baseline 1 から 6 へ)。質問票(ADAS-Cog 11項目) 合計スコア悪化 (Baseline 10 から 19 へ)。

---
患者ID: 01-701-1047
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値:
        * AE.AETERM = HYPERTENSION
        * AE.AEDECOD = BUNDLE BRANCH BLOCK LEFT
        * VS.VSTESTCD = DIABP, SYSBP (Visit: WEEK 4, VSPOS=STANDING)
        * VS.VSORRES = 121, 124, 185, 183 mmHg (Visit: WEEK 4, VSPOS=STANDING)
    * 医療機関への問い合わせ文面:
        * 患者ID: 01-701-1047 において、WEEK 4 (Day 28) の診察時のバイタルサイン測定で高血圧 (立位で収縮期血圧185mmHg、拡張期血圧124mmHg) が確認されました。また、有害事象としてHYPERTENSION (高血圧) および BUNDLE BRANCH BLOCK LEFT (左脚ブロック) が報告されています。
            1. 高血圧と左脚ブロック発現の時系列、詳細な症状、重症度、医学的な因果関係についてご教示ください。
            2. 左脚ブロックはBaseline (Day 1) 以前から存在していた既往歴でしょうか、治験薬投与開始後に発現した有害事象でしょうか。
            3. 降圧剤の使用状況と、今回の高血圧発現後の対応についてご教示ください。
            4. 選択・除外基準の「A history within the last 5 years of a serious cardiovascular disorder」、「Evidence from ECG recording at screening of any listed condition」に抵触する可能性はないでしょうか。プロトコル逸脱に該当しないか、ご見解をご教示ください。
    * 判断理由:
        * Week 4 (Day 28) の診察時のバイタルサイン測定でGrade 2以上の高血圧が確認され、安全性上の懸念があるため、臨床試験への影響度合いはMajorと判断しました。
        * 左脚ブロックの既往歴、発現時期、高血圧との関連性、プロトコル逸脱の可能性について、医療機関への確認が必要と判断しました。
* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LBTESTCD=PHOS, LBORRES=3.0 mg/dL (Day 14), 3.1 mg/dL (Day 27), 2.5 mg/dL (Day 46)
    * 医療機関への問い合わせ文面:
        * 該当患者の検査値 Phosphate (LBTESTCD=PHOS) が、Day 14, Day 27, Day 46で基準範囲を下回っています。
        * 臨床的に意義のある低リン血症であるかどうかご評価ください。
        * 臨床的に意義のある低リン血症である場合、処置内容についてご教示ください。
    * 判断理由:
        * Phosphate の値が継続的に基準範囲を下回っている点について、臨床的な意義を確認する必要があるため。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: 患者ID: 01-701-1047, CM.CMDTC, CM.CMSTDTC, CM.CMENDTC, AE.AEENDTC, CM.CMSTDY, CM.CMENDY, LB.LBDTC, LB.VISITDY, LB.LBDY, VS.VISITDY, VS.VSDY, EX.EXENDTC, EX.EXENDY

問題点:
* 問題No.: 1
    * 変数名と値: AE.AESTDTC, EX.EXSTDTC, EX.EXENDTC
    * 矛盾の内容: AEドメインの有害事象開始日 (2013-03-10) が、EXドメインの治験薬投与終了日 (2013-03-09) より後。時系列矛盾の疑い。
    * 問題点の原因（推測）: データ入力誤り、または治験薬投与終了後の有害事象発現の医学的理由。
    * 対応策（提案）: 医療機関にAE開始日とEX投与期間の矛盾を確認し、データ修正要否を判断。

* 問題No.: 2
    * 変数名と値: CM.CMDTC, CM.CMSTDTC
    * 矛盾の内容: CMドメイン1行目のCMDTC (2013-01-22) がCM.CMSTDTC (2009) より未来。データ収集日より過去に併用薬開始は矛盾。
    * 問題点の原因（推測）: データ入力誤り、CMDTCまたはCMSTDTCの日付誤記。
    * 対応策（提案）: データ入力者にCMドメイン1行目の日付の正当性を確認、必要に応じて修正。

* 問題No.: 3
    * 変数名と値: CM.CMENDTC, AE.AEENDTC
    * 矛盾の内容: CM.CMENDTC, AE.AEENDTC が空欄または空文字列。Define.xmlではDate型定義。データ形式不正。
    * 問題点の原因（推測）: データ入力時の未記入、またはデータ転送エラー、あるいは継続中の可能性。
    * 対応策（提案）: CM.CMENDTC, AE.AEENDTC の正確な日付、または継続中か否かを医療機関に確認し、データ修正。Define.xml修正も検討。

* 問題No.: 4
    * 変数名と値: CM.CMSTDY, CM.CMENDY, LB.VISITDY, LB.LBDY, VS.VISITDY, VS.VSDY
    * 矛盾の内容: CM, LB, VSドメインの**DY**変数 (Study Day) にNull値が多発。Define.xmlではInteger型定義。値が入力されるべき。
    * 問題点の原因（推測）: データ入力エラー、データ変換時の問題。
    * 対応策（提案）: 各ドメインの**DTC**, **VISITNUM**変数から**DY**変数を再計算し、データ補完。

* 問題No.: 5
    * 変数名と値: LB.LBDTC (日付のみ), VS.VSDTC (日時), Define.xml (VS.VSDTC: date型)
    * 矛盾の内容: LB.LBDTCは時間情報欠損、VS.VSDTCは時間情報あり。Define.xmlのVS.VSDTCはdate型定義。データ形式とDefine.xml定義の不整合。
    * 問題点の原因（推測）: データ入力/変換時の形式不統一、Define.xmlの定義誤り。
    * 対応策（提案）: LBドメインの時間情報を確認し補完。Define.xmlのVS.VSDTCをdatetime型に修正を検討 (Define.xmlの修正候補参照)。

Define.xmlの修正候補:
* ItemDef OID="VS.VSDTC"のdataTypeを"date"から"datetime"へ修正。

クエリ:
* 患者ID: 01-701-1047
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC: 2013-03-10 (HYPERTENSION), EX.EXSTDTC: 2013-02-12 (PLACEBO), EX.EXENDTC: 2013-03-09 (PLACEBO)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1047 において、有害事象「HYPERTENSION」の開始日と治験薬「PLACEBO」の投与期間に矛盾があります。データ入力誤りまたは医学的に妥当な理由があるか確認ください。
        * 判断理由: AE開始日とEX投与期間の矛盾は、治験薬と有害事象の因果関係評価に影響する可能性があり、臨床試験結果への影響は大きいと判断されるため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC (複数レコード), CM.CMENDTC (複数レコード)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1047 のCMドメイン、CMSEQ=1, 2, 3, 4, 5, 6, 7, 8 の併用薬について、CMSTDTC, CMENDTCの正しい日付 (YYYY-MM-DD形式) を教えてください。
        * 判断理由: 併用薬情報は安全性評価や治験薬との相互作用評価に重要。CMSTDTC, CMENDTCの日付不正はこれらの評価に影響を与える可能性があるため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: AE.AEENDTC (複数レコード)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1047 のAEドメイン、AESEQ=4 の有害事象（HYPERTENSION）について、AEENDTC（有害事象終了日）が空欄ですが、終了日をご教示ください。継続中の場合は、その旨お知らせください。
        * 判断理由: AE.AEENDTCの欠損は有害事象の期間把握を困難にするが、臨床試験主要評価項目への影響は限定的と判断されるため。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBDTC (時間情報), VS.VSDTC (時間情報), VISITDY (全ドメイン), LBDY, VSDY (LB, VSドメイン)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1047 のLB, VSドメインの時間情報欠損、VISITDY, LBDY, VSDYの欠損について、可能な範囲で原資料をご確認いただき、データ補完をお願いします。
        * 判断理由: 時間情報や**DY**変数の欠損は、データ解析の利便性を損なうものの、臨床試験結果の解釈に直接的な影響は少ないと判断されるため。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1047
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=ALEVE, CM.CMDECOD=NAPROXEN SODIUM, CM.CMSTDTC=2009
        逸脱内容: 併用薬ALEVE（CMDECOD: NAPROXEN SODIUM）が治験期間中に複数回使用されており、プロトコルで併用が禁止されている可能性があります。また、CM.CMSTDTC（併用薬開始日）が2009年とデータ収集日（2013-01-22）より前であり、データ入力時の誤りの可能性も指摘されます。併用薬FELDENE（フェルデン、一般名：ピロキシカム）もSCREENING 2 (-1日目) に使用開始され、試験薬初回投与日以前に投与終了していますが、併用禁止薬である可能性も考慮する必要があります。
        プロトコル該当箇所: 3.8. Concomitant Therapy, プロトコルの併用禁止薬リスト、選択・除外基準
        判断理由: 複数のアシスタントが指摘するように、ALEVE (NAPROXEN SODIUM) とFELDENE (PIROXICAM) は非ステロイド性抗炎症薬（NSAIDs）であり、プロトコルでNSAIDsが併用禁止薬として指定されている場合、プロトコル逸脱に該当する可能性があります。特にFELDENEについては、SCREENING 2 で使用が開始されており、選択・除外基準に抵触する可能性も考慮されます。CM.CMSTDTCの2009年という日付は、データ入力誤りの可能性を示唆しており、併用薬の使用状況の正確性に疑念が生じます。これらの併用薬の使用状況と、プロトコルにおける併用禁止薬規定、選択・除外基準との適合性を確認する必要があります。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.VISITNUM = 6.1, LB.VISIT = UNSCHEDULED 6.1, CM.CMSTDY = null, CM.CMENDY = null, AE.AEENDTC=2013-03-05, AE.AESTDTC=2013-03-06
        逸脱内容: 計画外のUNSCHEDULED 6.1 訪問で臨床検査が実施されており、評価スケジュールからの逸脱の可能性があります。また、複数の併用薬（ALEVE, CENTRUM, PAPAYA, PSORCON, ROBITUSSIN-DM, SUDAFED, SYNTHROID）でCMSTDYおよびCMENDYがNull値で記録されており、データ欠損として扱う必要があります。さらに、有害事象「UPPER RESPIRATORY TRACT INFECTION」の終了日（2013-03-05）が開始日（2013-03-06）より前日になっており、日付の矛盾が見られます。
        プロトコル該当箇所: 3.9. 評価、薬物動態、および安全性評価、プロトコルの評価スケジュールに関するセクション、Define.xmlおよびSDTMIG
        判断理由: 計画外訪問での臨床検査実施は、プロトコルで逸脱となる可能性があります。CMドメインにおけるCMSTDY/CMENDYのNull値はSDTMIG上許容されますが、データ品質の観点から問題があります。AEドメインの日付矛盾はデータ入力エラーを示唆します。これらのデータの問題点は、臨床試験のデータの質と解釈に影響を与える可能性があるため、逸脱またはデータ品質に関する懸念事項として検出されました。

クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: CMTRT=FELDENE, CMSTDTC=2013-02-10, CMENDTC=2013-02-01, MH.MHTERM=HYPERTENSION, AE.AETERM=HYPERTENSION
    医療機関への問い合わせ文面:
        被験者01-701-1047の併用薬FELDENE（フェルデン）およびALEVE（NAPROXEN SODIUM）の使用状況、既往歴の高血圧、治験期間中に発現した高血圧について、以下の点をご確認ください。

        1.  FELDENEおよびALEVEはプロトコルで併用禁止薬に指定されていますでしょうか？併用禁止薬の場合、使用はプロトコル逸脱に該当しますでしょうか？
        2.  併用禁止薬に指定されている場合、FELDENEおよびALEVEの使用はプロトコル逸脱に該当しますでしょうか？治験責任医師はプロトコル逸脱として判断されていますでしょうか？
        3.  プロトコル逸脱と判断されている場合、その逸脱内容は治験依頼者に報告されていますでしょうか？
        4.  FELDENEおよびALEVE使用時の医学的状況と、治験薬への影響について治験責任医師の見解を伺えますでしょうか？
        5.  既往歴の高血圧 (HYPERTENSION) の重症度と、選択基準・除外基準における心血管系疾患に関する規定への適合性について確認させてください。本被験者の組み入れが適切であったか、治験参加に影響を与える可能性のある事項がないかご回答ください。
        6.  有害事象「高血圧 (HYPERTENSION)」の詳細な内容、重症度、治験薬との因果関係、現在の状況（継続、回復など）と未回復の場合の理由と今後の見込み、治験薬の投与継続の可否と投与量変更の有無、併用薬（降圧剤など）の投与状況、治験参加継続の意思についてご回答ください。

        プロトコルの[併用禁止薬、選択・除外基準、有害事象報告]に関するセクションをご参照いただき、本件がプロトコル逸脱に該当するか、治験継続に影響を与える可能性のある事項がないかご回答ください。
    判断理由: FELDENEとALEVEの併用、既往歴・有害事象としての高血圧は、プロトコル逸脱および被験者の安全性に関わる重要な懸念事項であり、臨床試験の主要評価項目に影響を与える可能性があります。医療機関への問い合わせを通して、これらの疑義事項を明確にし、医学的妥当性とプロトコル遵守状況を評価する必要があるため、重要度の高いクエリとして作成しました。

クエリNo.: 2
    臨床試験結果への影響度合い: Minor
    変数名と値: CM.CMSTDTC=2009, AE.AEENDTC=2013-03-05, AE.AESTDTC=2013-03-06, LB.VISITNUM = 6.1, LB.VISIT = UNSCHEDULED 6.1, CM.CMSTDY = null, CM.CMENDY = null
    医療機関への問い合わせ文面:
        被験者01-701-1047のデータ入力に関する以下の点について、データ修正 অথবা 確認のご対応をお願いいたします。

        1.  併用薬ALEVE（NAPROXEN SODIUM）の開始日（CM.CMSTDTC）が2009年となっていますが、データ入力誤りの可能性はないでしょうか。正しい開始日をご教示ください。
        2.  有害事象「UPPER RESPIRATORY TRACT INFECTION」の終了日（AE.AEENDTC）が開始日（AE.AESTDTC）より前日となっています。日付の入力誤りの可能性はないでしょうか。正しい日付をご教示ください。
        3.  計画外訪問UNSCHEDULED 6.1 (LB.VISITNUM = 6.1, LB.VISIT = UNSCHEDULED 6.1) で臨床検査が実施された理由と、当該訪問がプロトコルで計画された評価スケジュールからの逸脱に該当するかどうかについてご回答ください。
        4.  併用薬（ALEVE, CENTRUM, PAPAYA, PSORCON, ROBITUSSIN-DM, SUDAFED, SYNTHROID）のCMSTDY（開始日（Study Day））およびCMENDY（終了日（Study Day））がNull値となっています。可能な範囲で結構ですので、CMSTDYおよびCMENDYの値をご提供いただけますでしょうか。

        ご多忙のところ恐縮ですが、データの正確性確保のため、ご協力をお願いいたします。
    判断理由: データ入力誤りの可能性のあるCM.CMSTDTC, AE.AEENDTC, AE.AESTDTCと、データ品質向上のために確認が必要なLB.VISIT情報、CM.CMSTDY, CM.CMENDYに関するクエリを、データマネージャーとして作成しました。これらのクエリは、臨床試験データの信頼性を高めるために重要です。

クエリなし

# 01-701-1023
## Task1: Clinical Review Results
## 1. 症例サマリー

**患者ID:** 01-701-1023

* 2012年07月22日 (Day -14): スクリーニング1
* 2012年08月03日 (Day -2): スクリーニング2
* 2012年08月05日 (Day 1): ベースライン
* 2012年08月07日 (Day 3): 紅斑 (ERYTHEMA) が発現 (軽度、治癒状況：未回復/未解決、因果関係：関連性あり)
* 2012年08月26日 (Day 22): 第二度房室ブロック (ATRIOVENTRICULAR BLOCK SECOND DEGREE) が発現 (軽度、治癒状況：未回復/未解決、因果関係：関連性あり)
* 2012年08月27日 (Day 23): WEEK 2 (2週目)
    * 紅斑 (ERYTHEMA) が発現 (軽度、治癒状況：未回復/未解決、因果関係：関連性あり)
    * 局所性紅斑 (LOCALIZED ERYTHEMA) が発現 (中等度、治癒状況：未回復/未解決、因果関係：関連性あり)
    * AST (アスパラギン酸アミノトランスフェラーゼ) が 25 U/L に上昇 (基準値上限: 36 U/L)
    * ALT (アラニンアミノトランスフェラーゼ) が 30 U/L に上昇 (基準値上限: 43 U/L)
    * ヘマトクリット (HCT) がスクリーニング1 (Day -14) の49.0%から46.0%に低下
    * ヘモグロビン (HGB) がスクリーニング1 (Day -14) の16.2 g/dLから14.9 g/dLに低下
    * 赤血球数 (RBC) がスクリーニング1 (Day -14) の5.30 MILL/uLから4.80 MILL/uLに低下
* 2012年08月30日 (Day 26): 紅斑 (ERYTHEMA) が軽快
* 2012年09月02日 (Day 29): WEEK 4 (4週目)
    * 治験薬投与中止 (ADVERSE EVENT)
    * 紅斑 (ERYTHEMA) が発現 (軽度、治癒状況：回復/解決、因果関係：関連性あり)
    * AST (アスパラギン酸アミノトランスフェラーゼ) が 30 U/L に上昇 (基準値上限: 36 U/L)
    * ALT (アラニンアミノトランスフェラーゼ) が 38 U/L に上昇 (基準値上限: 43 U/L)
* 2013年02月18日 (Day 198): RETRIEVAL (回収)
    * 試験終了 (FINAL RETRIEVAL VISIT)
    * CIBIC (ベースラインからの変化の程度) が "MINIMAL WORSENING" (わずかに悪化) と評価
    * ADAS-Cog(11) Subscore (ADAS-COG(11) サブスコア) が 12 に悪化 (ベースライン: 13)
    * Disability Assessment for Dementia (DAD) の複数項目 (DAITM16, DAITM24, DAITM29, DAITM31, DAITM34, DAITM36, DAITM37, DAITM38, DAITM39, DAITM40) が "N" (いいえ) または "NA" (該当なし) と評価
    * Neuropsychiatric Inventory - Revised (NPI-X) (神経精神医学的インベントリー改訂版) の複数項目 (NPITM09, NPITM10, NPITM11, NPITM12) が "ABSENT" (なし) と評価

---

## 2. クエリの作成

**患者ID: 01-701-1023**

* **クエリNo.:** 1
    * **臨床試験結果への影響度合い:** Critical
    * **変数名と値:** AE.AETERM = ATRIOVENTRICULAR BLOCK SECOND DEGREE, AE.AESEV = MILD, AE.AEREL = POSSIBLE, AE.AEOUT = "NOT RECOVERED/NOT RESOLVED"
    * **医療機関への問い合わせ文面:**
        治験参加者01-701-1023に治験薬との因果関係が「POSSIBLE」と評価された「ATRIOVENTRICULAR BLOCK SECOND DEGREE（房室ブロック2度）」が2012年08月26日に発現し、2012年08月27日時点でも未回復と記録されています。

        1.  第二度房室ブロックのType I/Type II、Mobitz I/Mobitz II、Wenckebachの有無、発現時の心電図波形など、詳細な臨床所見をご教示ください。
        2.  第二度房室ブロック発現に対する処置内容と、最終的な転帰（治癒、未回復など）についてご教示ください。
        3.  治験薬と第二度房室ブロックとの因果関係について、治験責任医師による再評価の結果をご教示ください。「POSSIBLE」という評価が適切か、あるいはより因果関係が高い／低い評価に変更すべきか、ご意見をお聞かせください。
        4.  治験プロトコルに規定された除外基準「Evidence from ECG recording at screening of any listed condition. (スクリーニング時の心電図記録から、いずれかの状態の証拠)」に抵触する可能性がないか、スクリーニング時の心電図データを含めた関連データをご確認ください。
        5.  第二度房室ブロックの発現状況を踏まえ、治験継続の可否に関する専門医のご意見をご提供ください。

    * **判断理由:**
        第二度房室ブロックは、重篤な不整脈や心停止を引き起こす可能性のある心臓伝導系の異常であり、患者の安全性に直接関わるクリティカルな有害事象です。
        治験薬との因果関係が「POSSIBLE」と評価されている点、および2012年08月27日時点で未回復であることから、患者の安全性を最優先に考慮し、詳細な情報を収集して専門家の意見を求める必要があると判断しました。
        また、スクリーニング時の心電図データを確認し、プロトコル逸脱の可能性も検討する必要があります。

* **クエリNo.:** 2
    * **臨床試験結果への影響度合い:** Minor
    * **変数名と値:** AE.AETERM = ERYTHEMA, AE.AEOUT = "NOT RECOVERED/NOT RESOLVED" (AESEQ=1,2,3), AE.AEOUT = "RECOVERED/RESOLVED" (AESEQ=4)
    * **医療機関への問い合わせ文面:**
        治験参加者01-701-1023に報告された紅斑（ERYTHEMA）について、以下の点をご確認ください。

        1.  2012年08月07日発現の紅斑（AESEQ=1, 2, 3）と、2012年09月02日発現の紅斑（AESEQ=4）は、それぞれ別の有害事象として報告されていますが、臨床的に同一の事象の再発と捉えることは可能でしょうか。
        2.  2012年08月07日発現の紅斑（AESEQ=1, 2, 3）は、2012年08月27日時点で「未回復／未解決」と記録されていますが、最終的な転帰はどのようになっているでしょうか。
        3.  紅斑の重症度、発現部位、持続期間、患者のQOLへの影響など、詳細な臨床情報をご提供ください。

    * **判断理由:**
        紅斑は治験において頻繁に報告される有害事象ですが、治癒状況や再発状況、患者への影響を正確に把握することは重要です。
        複数の紅斑イベントが報告されており、転帰の情報に一部矛盾が見られるため、臨床的な解釈と正確な情報を医療機関に確認することで、データの質を高めることを目的としています。
        紅斑自体は重篤な有害事象ではありませんが、患者のQOLや治験薬の忍容性評価に影響を与える可能性があるため、「Minor」としてクエリを作成しました。

* **クエリNo.:** 3
    * **臨床試験結果への影響度合い:** Minor
    * **変数名と値:** LB.LBTESTCD = [HCT, HGB, RBC], LB.VISIT = WEEK 2, LB.LBBLFL = "Y", LB.VISIT[Baseline] = SCREENING 1
    * **医療機関への問い合わせ文面:**
        治験参加者01-701-1023において、WEEK 2の検査でヘマトクリット(HCT)、ヘモグロビン(HGB)、赤血球数(RBC)の低下が認められます。
        これらの検査値低下について、脱水、出血、溶血、あるいは他の要因が考えられますでしょうか。臨床所見や背景情報と合わせてご意見をお聞かせください。
        特に、貧血に関連する自覚症状（めまい、ふらつき、易疲労感など）の有無について、確認をお願いします。

    * **判断理由:**
        ヘマトクリット、ヘモグロビン、赤血球数の低下は、貧血を示唆する可能性があります。
        今回のデータでは、WEEK 2 の一時的な変動であり、臨床的に直ちに問題となる可能性は低いと考えられますが、貧血の原因精査や患者の安全性を確認するため、背景情報を医療機関に確認することは有益と考えられます。
        臨床試験の主要評価項目に直接的な影響を与える可能性は低いと判断し、「Minor」としてクエリを作成しました。

* **クエリNo.:** 4
    * **臨床試験結果への影響度合い:** Minor
    * **変数名と値:** QS.QSTESTCD = "DAITM31", QS.QSORRES = "NA", QS.QSCAT = "FINANCE AND CORRESPONDE"
    * **医療機関への問い合わせ文面:**
        Disability Assessment for Dementia (DAD) の質問票項目 DAITM31 (請求書の支払い) の回答が RETRIEVAL (回収) 訪問時に "NA" (該当なし) となっています。

        1.  この "NA" は、評価対象外を意味する "Not Applicable" (非該当)  でしょうか、それともデータ欠損を示す "Not Available" (データなし)  でしょうか。記録時の意図についてご教示ください。
        2.  評価が "Not Applicable" (非該当)  の場合、請求書の支払いを評価対象外とした理由をご教示ください。

    * **判断理由:**
        Disability Assessment for Dementia (DAD) は、患者の日常生活における機能障害を評価する重要な指標です。
        質問項目 DAITM31 (請求書の支払い) の回答が "NA" となっている理由が不明確であり、データの解釈に疑義が生じる可能性があります。
        "NA" の意図を明確にすることで、データの正確性を向上させ、DAD の評価の妥当性を確認することを目的としています。
        DAD は副次評価項目であり、臨床試験全体の結果に重大な影響を与える可能性は低いと判断し、「Minor」としてクエリを作成しました。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: AE.AEENDTC, AE.AEENDY, CM.CMENDTC, CM.CMENDY, CM.CMSTDTC, DS.DSDECOD, DS.DSTERM, DS.DSSPID, DS.DSSTDTC, DS.VISIT, DS.VISITDY, DM.RFICDTC, DM.DTHDTC, DM.DTHFL, EX.EXENDTC, EX.EXENDY, MH.MHSPID, MH.MHSEV, QS.QSORRESU, QS.QSSTRESC, QS.QSSTRESU, SV.SVENDTC, SV.VISITDY, VS.VSLOC, VS.VSSTAT, VS.VSTPT, VS.VSTPTNUM, VS.VSELTM, VS.VSTPTREF

問題点:
* 問題No.1:
    * 変数名と値: AE.AEENDTC (AEレコードNo.4), 空欄
    * 矛盾の内容: AEレコードNo.4の有害事象（AETERM=ERYTHEMA）は、AEOUT（転帰）が「RECOVERED/RESOLVED」であるにもかかわらず、AEENDTC（有害事象終了日）が空欄となっている。転帰が「RECOVERED/RESOLVED」の場合、AEENDTCは日付が入力されるべきである。
    * 問題点の原因（推測）: データ入力時の欠落または誤り
    * 対応策（提案）: 医療機関にAEENDTCの正確な日付を確認し、データを修正する。

* 問題No.2:
    * 変数名と値: DS.DSTERM (DSレコードNo.2, 3), 空欄, DS.DSSPID, DS.VISIT, DS.VISITDY (欠損値多数), DS.DSDECOD (値: ""), DS.DSSTDTC (値: "")
    * 矛盾の内容: DSドメインにおいて、DSTERM（報告されたDispositionイベント名）が空欄となっているレコードが存在する。また、DSDECOD（標準化されたDisposition用語）とDSSTDTC（Dispositionイベント開始日）はDefine.xmlで必須変数と定義されているにもかかわらず、欠損値が認められる。さらに、DSSPID（Sponsor-Defined Identifier）、VISIT（Visit Name）、VISITDY（Planned Study Day of Visit）にも欠損値が多数見られる。これらの欠損値は、データの完全性と解釈可能性を損なう。
    * 問題点の原因（推測）: データ入力時の不備、データ収集プロセスの不備、または意図的な欠損の可能性が考えられる。意図的な欠損の場合、その理由を明確にする必要がある。
    * 対応策（提案）:
        1.  データ提出元にDSドメインのDSTERM, DSSPID, VISIT, VISITDY, DSDECOD, DSSTDTC の欠損値について確認し、修正を依頼する。
        2.  欠損が意図的なものである場合は、その理由を明確に記録する。
        3.  Define.xmlおよびプロトコルを参照し、必須項目であるDSDECODとDSSTDTCが欠損している原因を特定し、データ収集プロセスの改善を検討する。

* 問題No.3:
    * 変数名と値: CM.CMSTDTC (CMレコードNo.1-21), 2006
    * 矛盾の内容: CMドメインのCMSTDTC（併用薬開始日）が2006年となっている。DMドメインのRFSTDTC（治験薬初回投与日）は2012年であり、併用薬開始日が治験薬初回投与日より6年以上前となっている。医学的に矛盾はない可能性もあるが、データの妥当性を確認する必要がある。
    * 問題点の原因（推測）: 併用薬の開始日が治験薬投与開始日より前である可能性、またはデータ入力誤りの可能性
    * 対応策（提案）: 医療機関にCMSTDTCの日付が正しいか、またはデータ入力誤りでないかを確認する。併用薬の種類（ASPIRIN, MYLANTA, TUMS）から、長期にわたる使用も考えられるため、医学的な妥当性も確認する。

クエリ:
* 患者ID: 01-701-1023
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Critical
        * 変数名と値: DS.DSTERM (値: ""), DS.DSDECOD (値: ""), DS.DSSTDTC (値: "")
        * 医療機関への問い合わせ文面:
            DSドメインのDSSEQ=2, 3のレコードにおいて、DSTERM, DSDECOD, DSSTDTC が欠損しています。DSTERM, DSDECOD, DSSTDTC の適切な値をご教示ください。特にDSDECOD, DSSTDTCは必須項目ですので、早急な修正をお願いします。
        * 判断理由: DSDECODとDSSTDTCはDispositonドメインの必須変数であり、欠損はデータ品質に重大な影響を与えるため、Criticalと判断しました。

    * クエリNo.2:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AEENDTC (AEレコードNo.4), 空欄
        * 医療機関への問い合わせ文面:
          有害事象「ERYTHEMA」（レコードNo.4、AESEQ=4）について、転帰が「RECOVERED/RESOLVED」（AEOUT=RECOVERED/RESOLVED）と報告されていますが、有害事象終了日が空欄となっています。有害事象終了日（AEENDTC）をご教示ください。
        * 判断理由: AEENDTCは有害事象の期間を特定するために重要な項目であり、データの正確性を確保する必要があるため、影響度をMajorと判断しました。

    * クエリNo.3:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: DS.DSTERM, DS.DSSPID, DS.VISIT, DS.VISITDY (欠損値)
        * 医療機関への問い合わせ文面:
            DSドメインのDSTERM, DSSPID, VISIT, VISITDYに欠損値が散見されます。これらの欠損値は、データ入力時のエラーによるものか、意図的なものか確認をお願いします。意図的な欠損である場合、その理由をご教示ください。
        * 判断理由: DSTERM, DSSPID, VISIT, VISITDY は必須項目ではないものの、Dispositionイベントの内容を把握するために有用な項目であり、データの可読性を向上させるため、影響度をMinorと判断しました。

    * クエリNo.4:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMSTDTC (CMレコードNo.1-21), 2006
        * 医療機関への問い合わせ文面:
          併用薬ドメインのレコードNo.1-21について、CMSTDTC（併用薬開始日）が2006年となっていますが、DMドメインのRFSTDTC（治験薬初回投与日）は2012年です。併用薬開始日が治験薬投与開始日より前であることは医学的に矛盾がないか、またはデータ入力誤りでないかをご確認ください。
        * 判断理由: CMSTDTCは併用薬の投与期間を特定するために重要な項目であり、データの医学的妥当性を確認するため、影響度をMinorと判断しました。
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1023
    逸脱No.: 1
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC = 2006, CM.CMENDTC = null, CM.CMTRT = ASPIRIN
        逸脱内容: 併用薬アスピリンの開始日が試験開始前（2006年）で終了日が未記録。試験期間中に併用されているか不明確。
        プロトコル該当箇所: 3.8 併用療法（併用薬に関する規定はあるが、使用期間に関する規定は不明確）
        判断理由: CMドメインにおける併用薬の使用期間のデータ不備。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: AE.AESTDTC = 2012-08-07, AE.AEENDTC = 2012-08-30, AE.AEDTC = 2012-08-27, AETERM = ERYTHEMA
        逸脱内容: 有害事象ERYTHEMAの開始日と終了日がデータ収集日より後。データ入力の誤りの可能性。
        プロトコル該当箇所: 3.9.3.2.1 有害事象報告要件（日付の整合性に関する規定は不明確）
        判断理由: AEドメインにおける日付の矛盾。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMDECOD = UNCODED, CMINDC = "", CMCLAS = UNCODED (MYLANTA, TUMS)
        逸脱内容: 併用薬MYLANTA, TUMSの標準化された薬剤名、適応症、薬剤クラスが未記録またはUNCODED。
        プロトコル該当箇所: 3.8 併用療法（併用薬の情報記録に関する規定は不明確）
        判断理由: CMドメインにおける薬剤情報（CMDECOD, CMINDC, CMCLAS）の欠損。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE, MHCAT = PRIMARY DIAGNOSIS
        逸脱内容: 病歴にアルツハイマー病（PRIMARY DIAGNOSIS）が記録されているが、選択基準INCL02との合致状況が不明確。
        プロトコル該当箇所: 3.4.2.1 選択基準 [2]
        判断理由: MHドメインの病歴とプロトコルの選択基準の照合が必要。

患者ID: 01-701-1023
    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = ASPIRIN
        医療機関への問い合わせ文面: 患者01-701-1023の併用薬アスピリンについて、プロトコルでの併用許可、使用目的、治験期間中の使用状況（継続/中止、中止日）をご教示ください。
        判断理由: アスピリンの併用状況と詳細情報を確認し、プロトコル遵守状況を評価するため。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = MYLANTA, TUMS
        医療機関への問い合わせ文面: 患者01-701-1023の併用薬MYLANTA, TUMSについて、プロトコルでの併用許可、標準化された薬剤名（CMDECOD）、使用目的（CMINDC）、薬剤クラス（CMCLAS）をご教示ください。
        判断理由: MYLANTA, TUMSの併用状況と薬剤詳細情報を確認し、プロトコル遵守状況を評価するため。

    クエリNo.: 3
        臨床試験結果への影響度合い: Major
        変数名と値: MH.MHTERM = ALZHEIMER'S DISEASE
        医療機関への問い合わせ文面: 患者01-701-1023の病歴におけるアルツハイマー病（PRIMARY DIAGNOSIS）は、プロトコルの選択基準INCL02「probable AD as defined by NINCDS and ADRDA guidelines」を満たすものとして治験責任医師によって判断されていますか？ 選択基準との合致状況について、詳細をご教示ください。
        判断理由: アルツハイマー病の病歴が選択基準を満たすか確認し、患者組み入れの適切性を評価するため。

# 01-702-1082
## Task1: Clinical Review Results
**症例サマリー:**

患者ID: 01-702-1082
* 2013年07月24日 (Day -2): ALT (アラニンアミノトランスフェラーゼ) 検査値が基準値上限を超過 (37 U/L、基準範囲: 6-32 U/L)。AST (アスパート酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (44 U/L、基準範囲: 9-34 U/L)。BUN (血中尿素窒素) 検査値が基準値上限を超過 (27 mg/dL、基準範囲: 4-24 mg/dL)。WBC (白血球数) 検査値が基準値上限を超過 (14.77 THOU/uL、基準範囲: 3.8-10.7 THOU/uL)。尿検査でURINE ANALYSIS ABNORMAL (尿分析異常) が報告された。好中球数増加、白血球数増加の有害事象が発現 (軽度)。
* 2013年07月26日 (Day 1): 尿検査でURINE ANALYSIS ABNORMAL (尿分析異常) が報告された。AST (アスパート酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (41 U/L、基準範囲: 9-34 U/L)。
* 2013年08月08日 (Day 14): ALT (アラニンアミノトランスフェラーゼ) 検査値が基準値上限を超過 (35 U/L、基準範囲: 6-32 U/L)。AST (アスパート酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (41 U/L、基準範囲: 9-34 U/L)。CK (クレアチンキナーゼ) 検査値が基準値上限を超過 (320 U/L、基準範囲: 21-169 U/L)。白血球数増加、好中球数増加の有害事象は回復。
* 2013年08月24日 (Day 30): AST (アスパート酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (35 U/L、基準範囲: 9-34 U/L)。
* 2013年09月02日 (Day 39): 直腸出血 (RECTAL HAEMORRHAGE) の有害事象が発現 (軽度)。BUN (血中尿素窒素) 検査値が基準値上限を超過 (30 mg/dL、基準範囲: 4-24 mg/dL)。
* 2013年09月06日 (Day 43): 直腸出血 (RECTAL HAEMORRHAGE) の有害事象は未回復。
* 2013年09月09日 (Day 46): 適用部位刺激感 (APPLICATION SITE IRRITATION) の有害事象が発現 (軽度)。
* 2013年09月24日 (Day 61): 適用部位刺激感 (APPLICATION SITE IRRITATION) の有害事象は回復。
* 2013年09月28日 (Day 65): AST (アスパート酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (36 U/L、基準範囲: 9-34 U/L)。CK (クレアチンキナーゼ) 検査値が基準値上限を超過 (177 U/L、基準範囲: 21-169 U/L)。HCT (ヘマトクリット) 検査値が基準値上限を超過 (42 %、基準範囲: 34-48 %)。WBC (白血球数) 検査値が基準値上限を超過 (10.76 THOU/uL、基準範囲: 3.8-10.7 THOU/uL)。直腸出血 (RECTAL HAEMORRHAGE) の有害事象は回復。適用部位刺激感 (APPLICATION SITE IRRITATION) の有害事象が再発 (軽度)。
* 2013年10月12日 (Day 79): 皮膚刺激 (SKIN IRRITATION) の有害事象が発現 (中等度)。
* 2013年10月31日 (Day 98): 適用部位刺激感 (APPLICATION SITE IRRITATION) の有害事象は回復。皮膚刺激 (SKIN IRRITATION) の有害事象は継続中。
* 2013年11月17日 (Day 115): 蛋白 (Protein) 検査値が基準値上限を超過 (8.1 g/dL、基準範囲: 6-8 g/dL)。ケトン体 (Ketones) 検査値が異常値 (1 NO UNITS)。WBC (白血球数) 検査値が基準値上限を超過 (14.38 THOU/uL、基準範囲: 3.8-10.7 THOU/uL)。PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS'PILLS'" (患者はパッチが不便で痒いと感じ、錠剤を希望している) の理由により試験中止。皮膚刺激 (SKIN IRRITATION) の有害事象は回復。

---

**クエリ:**

患者ID: 01-702-1082
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: DS.DSTERM = PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS'PILLS'", AE.AETERM=APPLICATION SITE IRRITATION, AE.AETERM=SKIN IRRITATION, CM.CMTRT=HYDROCORTISONE, TOPICAL
    * 医療機関への問い合わせ文面: 
        治験薬の貼付部位の刺激感と皮膚刺激により治験中止となりました。貼付部位、貼付方法、HYDROCORTISONE, TOPICAL (外用ハイドロコルチゾン) の使用状況と皮膚症状の詳細 (重症度、発現部位、持続時間、具体的な症状、治験薬との因果関係、治験中止との関連性) について医療機関の見解をご確認ください。
    * 判断理由: 
        治験薬の貼付部位の刺激感と皮膚刺激は、患者が治験中止に至った理由であり、患者QOLを損なうだけでなく、臨床試験の継続や評価項目にも影響を与える重要な疑義事項であるため、詳細な情報が必要です。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = KETONES, LBSTRESC = 1, LBNRIND = ABNORMAL (WEEK 12)
    * 医療機関への問い合わせ文面:
        試験終了時 (WEEK 12) の尿検査でケトン体がAbnormal (1 NO UNITS) でした。糖尿病の既往歴、血糖値の変動、食事摂取量、脱水、飢餓状態、尿路感染症の可能性など、ケトン尿検出の医学的な背景について医療機関にご確認ください。
    * 判断理由:
        尿中ケトン体陽性は、患者の代謝状態異常を示唆する可能性があり、安全性に関わる懸念事項であるため、医学的妥当性を検証する必要があります。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = PROT, LBNRIND = HIGH (WEEK 12)
    * 医療機関への問い合わせ文面: 
        試験終了時 (WEEK 12) に蛋白検査値が基準値上限を超過していました。脱水、炎症、腎機能障害、肝機能、既往歴、併用薬、尿検査値など、蛋白検査値上昇の医学的な背景について医療機関にご確認ください。
    * 判断理由:
        蛋白検査値上昇は、様々な病態を示唆する可能性があり、患者の安全性に関わる可能性があるため、医学的妥当性を検証する必要があります。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = WBC, LBNRIND = HIGH (SCREENING 1, WEEK 6, WEEK 8, WEEK 12)
    * 医療機関への問い合わせ文面: 
        白血球数増加が複数回認められます。感染症、炎症性疾患、薬剤性など、白血球数増加の原因について、白血球分画、炎症マーカー (CRP値など) の変動、発熱の有無、併用薬投与状況と合わせて医療機関にご確認ください。
    * 判断理由:
        白血球数増加の原因を特定し、患者の安全性に問題がないか確認する必要があるため、詳細な情報が必要です。

* クエリNo.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: LB.LBTESTCD = ALT, LBNRIND = HIGH (UNSCHEDULED 1.1, WEEK 2), LB.LBTESTCD = AST, LBNRIND = HIGH (UNSCHEDULED 1.1, WEEK 2, WEEK 8)
    * 医療機関への問い合わせ文面:
        ALT, AST の肝機能検査値上昇が複数回認められます。肝疾患の既往歴、アルコール摂取歴、薬剤性肝障害、ALT, AST 以外の肝機能検査値、肝炎ウイルス検査、画像検査、併用薬など、肝機能検査値上昇の原因について医療機関にご確認ください。
    * 判断理由:
        ALT, AST の肝機能検査値上昇の原因を特定し、患者の安全性に問題がないか確認する必要があるため、詳細な情報が必要です。

* クエリNo.: 6
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: VS.VSTESTCD = SYSBP, VSORRES = 96 mmHg (WEEK 6), VSORRES = 86 mmHg (WEEK 6), VS.VSTESTCD = DIABP, VSORRES = 50 mmHg (WEEK 6), VSORRES = 52 mmHg (WEEK 6)
    * 医療機関への問い合わせ文面:
        治験薬投与期間中に収縮期血圧、拡張期血圧の低下が認められています。血圧低下時の患者の自覚症状、起立性低血圧の有無、Visit 6 (AMBUL ECG REMOVAL) における血圧測定時の体位、血圧低下に対する処置、Visit 6 以降の血圧推移、SpO2 値、心電図所見について医療機関にご確認ください。
    * 判断理由:
        治験薬投与との関連性が疑われる血圧低下の原因と臨床的意義、患者の安全性について検証する必要があるため、詳細な情報が必要です。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目:
    * LBドメインの検査値異常とAEドメインの関連性
    * VSドメインのバイタルサイン異常とAEドメインの関連性
    * AEドメインのAEACN
    * DSドメインのDSTERMとCMドメインのCMTRTの関連性
    * EX.EXENDTCの矛盾
    * VSドメインにおける欠損値 (特に SCREENING 2, STANDING)
    * LB.LBSTRESCとLB.LBSTRESNのデータ型と値の不整合
    * VSドメインにおけるVSORRESのデータ型不整合

問題点:
* 問題No.: 1
    * 変数名と値: LBドメインの複数検査項目 (ALT, AST, BUN, CK, HCT, VITB12, WBC, KETONES, PROT) における LBNRIND=HIGH / ABNORMAL
    * 矛盾の内容: LBドメインにおいて、複数の検査項目で基準値外の異常値（HIGH, ABNORMAL）が確認されたが、AEドメインに関連する有害事象の報告がない。
    * 問題点の原因（推測）:
        * 検査値異常が有害事象として適切に報告されていない。
        * データ入力時にAEドメインへの登録漏れがあった可能性。
        * 治験薬または併用薬の影響、患者の基礎疾患による検査値異常の可能性。
        * データ入力時のエラーの可能性。
    * 対応策（提案）:
        * 医療機関にLBドメインの検査値異常とAEドメインの関連性について問い合わせる。
        * 関連する有害事象がAEドメインに報告されていない場合は、データの修正または追加を依頼する。
        * 検査値異常の原因（治験薬との関連性、基礎疾患等）について、治験担当医師の見解を確認する。

* 問題No.: 2
    * 変数名と値: VSドメインにおける DIABP, PULSE, SYSBP の異常値 (HIGH) および欠損 (VISIT=SCREENING 2, VSPOS=STANDING)
    * 矛盾の内容: VSドメインにおいて、SYSBPでHighの異常値が複数回確認されたが、AEドメインに関連する有害事象の報告がない。また、SCREENING 2の立位でのバイタルサイン測定値が欠損している。
    * 問題点の原因（推測）:
        * 検査値異常が有害事象として適切に報告されていない。
        * データ入力時にAEドメインへの登録漏れがあった可能性。
        * 測定自体の実施漏れ、またはデータ入力時の選択肢誤りの可能性。
        * データ入力時の欠落、または意図的にデータ収集が行われなかった可能性。
    * 対応策（提案）:
        * 医療機関にVSドメインのバイタルサイン異常とAEドメインの関連性について問い合わせる。
        * 関連する有害事象がAEドメインに報告されていない場合は、データの修正または追加を依頼する。
        * 医療機関にデータ欠損の理由を確認し、可能であれば測定値を再入手する。
        * VISIT=SCREENING 2 における立位でのバイタルサイン測定がプロトコル上必須であるか確認する。

* 問題No.: 3
    * 変数名と値: AE.AEACN (NULL)
    * 矛盾の内容: AEドメインのAEACN（治験薬との処置）が全てNULLになっている。Define.xmlの定義では必須項目ではないが、データ品質として再調査が望ましい。
    * 問題点の原因（推測）:
        * データ入力時のエラー。
        * データ収集/入力手順における不備の可能性。
        * 意図的にデータが収集されなかった、または「処置なし」と判断された可能性。
    * 対応策（提案）:
        * AE.AEACNがNULLとなっている理由をデータマネジメントチームに確認する。
        * 必要に応じて、データ入力手順の見直しや医療機関への再確認を検討する。

* 問題No.: 4
    * 変数名と値: DS.DSTERM ("PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS'PILLS'"), CM.CMTRT ("HYDROCORTISONE, TOPICAL"), EX.EXTRT ("XANOMELINE")
    * 矛盾の内容: DSドメインの治験薬投与中止理由にパッチ剤による皮膚刺激を示唆する記述がある一方で、CMドメインに皮膚刺激緩和を目的としたHYDROCORTISONE, TOPICALが投与されている。EXドメインの治験薬とCMドメインの併用薬の投与期間に矛盾が認められる。
    * 問題点の原因（推測）:
        * 治験薬による皮膚刺激が発生し、その緩和のためにHYDROCORTISONE, TOPICALが処方された可能性。
        * CMドメインのHYDROCORTISONE, TOPICALの投与期間が、EXドメインの治験薬投与期間よりも長く記録されているデータ入力エラーの可能性。
        * 併用薬HYDROCORTISONE, TOPICALが治験薬投与終了後も継続された可能性。
    * 対応策（提案）:
        * 医療機関にDS.DSTERMとCM.CMTRTの関連性、およびHYDROCORTISONE, TOPICALの投与意図について問い合わせる。
        * 治験薬による皮膚刺激への対応がプロトコルに準拠しているか確認する。
        * CMドメインのHYDROCORTISONE, TOPICALの投与期間が医学的に妥当か確認する。長期投与の場合はクエリ発行を検討する。

* 問題No.: 5
    * 変数名と値: EX.EXENDTC (2013-08-08), EX.EXSTDTC (2013-07-26) (EXSEQ=1)
    * 矛盾の内容: EXドメインのレコード (EXSEQ=1) において、治験薬終了日 (EXENDTC) が治験薬開始日 (EXSTDTC) より早い日付で記録されている。治験薬の投与期間として矛盾が生じている。
    * 問題点の原因（推測）: データ入力時の誤り、または意図的なデータ修正の可能性。
    * 対応策（提案）: 医療機関にEXドメインの該当レコード (EXSEQ=1) の EXSTDTC および EXENDTC の日付が正しいかどうか確認し、必要に応じて修正を依頼する。

* 問題No.: 6
    * 変数名と値: LB.LBSTRESCとLB.LBSTRESNのデータ型不整合、VS.VSORRESのデータ型不整合
    * 矛盾の内容: LB.LBSTRESC（文字型）とLB.LBSTRESN（数値型）の値がデータ形式と内容が一致していない。VS.VSORRES（文字型）に数値データが格納され、データ型と内容が一致していない。Define.xmlの定義と実際のデータに不整合が見られる。
    * 問題点の原因（推測）:
        * データ作成時のスクリプトまたは仕様書の誤り。
        * Define.xmlの定義とデータ作成ロジックの不整合。
        * データ入力時の書式設定の誤り、データ変換時のエラー。
    * 対応策（提案）:
        * データ作成者に確認し、LB.LBSTRESCに適切な文字データが格納されるように修正するか、Define.xmlの定義を修正する。
        * データ入力ルールを見直し、VS.VSORRESに不要な"0"が入力されないように修正する。または、データ変換スクリプトを修正する。
        * Define.xmlと実際のデータの定義を一致させるように修正する。（Define.xmlの修正候補として記録）

クエリ:

患者ID: 01-702-1082
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: EX.EXENDTC, EX.EXSTDTC (EXSEQ=1)
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Exposure (EX) データセットの EXSEQ=1 レコードについて、治験薬 XANOMELINE の投与終了日 (EXENDTC) 2013-08-08 が 投与開始日 (EXSTDTC) 2013-07-26 より早い日付となっています。投与期間として矛盾が生じているため、EXSTDTC および EXENDTC の日付が正しいか、記録誤りがないかをご確認ください。もし記録誤りの場合、正しい日付への修正をお願いいたします。
    * 判断理由: 治験薬の投与期間は主要評価項目や安全性評価に影響を与える重要なデータであるため。

* クエリNo.: 2
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: LBドメインの複数検査項目 (ALT, AST, BUN, CK, HCT, VITB12, WBC, KETONES, PROT) における LBNRIND=HIGH / ABNORMAL, AEドメイン全般
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Laboratory Tests Results (LB) データセットにおいて、複数の検査項目で基準値外の異常値が確認されました。
        * 血液検査: ALT、AST、BUN、CK、HCT、VITB12、WBC (LBNRIND=HIGH)
        * 尿検査: KETONES (LBNRIND=ABNORMAL)
        * 血液検査: PROT (LBNRIND=HIGH)
        これらの検査値異常に関連する有害事象はAEドメインに報告されていますでしょうか。もし有害事象として報告すべき事象がある場合、AEドメインへの追加をお願いいたします。
    * 判断理由: 複数の臨床検査項目の異常値は患者の安全性に影響を与える可能性があり、臨床的に重要と考えられるため。

* クエリNo.: 3
    * 臨床試験結果への影響度合い: Major
    * 変数名と値: VS.VSTESTCD (SYSBP), VS.VSORRES (150, 150, 160), AEドメイン全般
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Vital Signs (VS) データセットにおいて、収縮期血圧（SYSBP）が高い値で複数回確認されました。
        * SCREENING 1 (SUPINE): 150 mmHg
        * SCREENING 1 (STANDING): 150 mmHg
        * WEEK 4 (SUPINE): 160 mmHg
        収縮期血圧の上昇に関連する有害事象はAEドメインに報告されていますでしょうか。もし有害事象として報告すべき事象がある場合、AEドメインへの追加をお願いいたします。
    * 判断理由: 収縮期血圧の上昇は、患者の安全性に影響を与える可能性があり、臨床的に重要と考えられるため。

* クエリNo.: 4
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: VS.VSTESTCD=DIABP, VS.VSPOS=STANDING, VISITNUM=2 における VSORRES, VSSTAT
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Vital Signs (VS) データセットにおいて、VISITNUM=2（SCREENING 2）の立位での拡張期血圧（DIABP）の結果が未実施 (VSSTAT=NOT DONE) となっています。立位でのバイタルサイン測定が未実施となった理由をご教示ください。もし測定が実施されたにも関わらず未入力となっている場合、測定値をご提供いただけますでしょうか。
    * 判断理由: バイタルサイン測定はプロトコルで規定されている重要な評価項目であり、データの欠損理由を確認し、可能であればデータを収集することが望ましい。

* クエリNo.: 5
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AEACN (NULL)
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Adverse Events (AE) データセットにおいて、「治験薬との処置 (AEACN)」が全てのレコードで空欄となっています。AEACN が空欄となっている理由についてご教示いただけますでしょうか。
    * 判断理由: データ品質の観点から、AEACNがNULLとなっている理由を確認することは有益であるため。

* クエリNo.: 6
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: DS.DSTERM ("PT FINDS PATCHES"INCONVENIENT & ITCHY;PT PREFERS'PILLS'"), CM.CMTRT ("HYDROCORTISONE, TOPICAL")
    * 医療機関への問い合わせ文面: 患者ID 01-702-1082 の Disposition (DS) データセットの治験薬投与中止理由 (DSTERM) に「パッチ剤が不便と痒みがある」との記載があります。また、Concomitant Medications (CM) データセットには、HYDROCORTISONE, TOPICAL (外用薬) の投与記録があります。皮膚刺激緩和のためHYDROCORTISONE, TOPICAL が処方されたと理解してよろしいでしょうか。HYDROCORTISONE, TOPICAL の投与開始日と投与終了日をご教示ください。
    * 判断理由: DSドメインとCMドメインの記述内容の関連性を確認し、データの整合性を高めることは有益であるため。
## Task3: Protocol Deviation Review Results
患者ID: 01-702-1082
    * 逸脱No.: 1
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMTRT = HYDROCORTISONE, TOPICAL
        * 逸脱内容: 併用薬としてHYDROCORTISONE, TOPICALが投与されています。治験薬ザノメリンTTSと併用した場合の薬物相互作用や、皮膚への局所的な影響が懸念されます。プロトコル上、併用禁止薬に指定されていませんが、治験薬の効果に影響を与える可能性があるため、プロトコル逸脱の疑義として検出します。
        * プロトコル該当箇所: 3.8. Concomitant Therapy, 3.4.2.2. Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list).
        * 判断理由: プロトコルに併用禁止薬リストの明記はないものの、治験薬と外用剤の併用による潜在的なリスクと治験結果への影響を考慮し、プロトコル逸脱の疑義として検出しました。

    * 逸脱No.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=ALT, LB.LBORRES=37 U/L (UNSCHEDULED 1.1), 35 U/L (WEEK 2), LB.LBSTRESC=HIGH (UNSCHEDULED 1.1, WEEK 2)
        * 逸脱内容: ALT値がUNSCHEDULED 1.1とWEEK 2で基準範囲上限を超過しています。除外基準EXCL27（Laboratory test values exceeding the Lilly Reference Range III for the patient's age）に抵触する可能性があります。
        * プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
        * 判断理由: 複数の検査でALT値が基準範囲上限を超過しており、プロトコル除外基準に抵触する可能性があるため、臨床試験の実施に影響を与えるMajor逸脱と判断しました。

    * 逸脱No.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD=AST, LB.LBORRES=44 U/L (UNSCHEDULED 1.1), 41 U/L (WEEK 2), 35 U/L (WEEK 4), 36 U/L (WEEK 8), LB.LBSTRESC=HIGH (UNSCHEDULED 1.1, WEEK 2, WEEK 4, WEEK 8)
        * 逸脱内容: AST値がUNSCHEDULED 1.1、WEEK 2、WEEK 4、WEEK 8で基準範囲上限を超過しています。除外基準EXCL27（Laboratory test values exceeding the Lilly Reference Range III for the patient's age）に抵触する可能性があります。
        * プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b]
        * 判断理由: 複数の検査でAST値が基準範囲上限を超過しており、プロトコル除外基準に抵触する可能性があるため、臨床試験の実施に影響を与えるMajor逸脱と判断しました。

患者ID: 01-702-1082
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMTRT = HYDROCORTISONE, TOPICAL
        * 医療機関への問い合わせ文面: 
            治験参加者の併用薬HYDROCORTISONE, TOPICALについて確認させてください。
            1.  HYDROCORTISONE, TOPICALは、プロトコルで併用が禁止されている薬剤に該当しますでしょうか？
            2.  該当する場合、HYDROCORTISONE, TOPICALの投与開始日、投与量、投与期間、投与経路、投与理由をご教示ください。
        * 判断理由: 併用薬HYDROCORTISONE, TOPICALの使用状況とプロトコルとの整合性を確認し、逸脱の有無と臨床試験への影響を評価するため、医療機関への問い合わせが必要と判断しました。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: QS.MMITM01-06, DM.AGE
        * 医療機関への問い合わせ文面: 
            選択基準INCL03（MMSEスコアが10〜23）およびINCL01（50歳以上）を満たしていることを確認するため、以下の情報をご提供ください。
            1. ミニメンタルステート検査（MMSE）の合計スコアと、各項目の点数（MMITM01〜06）
            2. 患者の年齢
        * 判断理由: 選択基準INCL01およびINCL03に抵触していないか確認する必要があるため、MMSEスコアと年齢に関するクエリを発行します。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.ALT, LB.AST, LB.BUN, LB.HCT, LB.WBC, LB.TSH, LB.VITB12
        * 医療機関への問い合わせ文面: 
            除外基準EXCL27およびEXCL28（臨床検査値異常）への抵触の可能性について確認させてください。
            1. ALT (UNSCHEDULED 1.1, WEEK 2でHIGH)、AST (UNSCHEDULED 1.1, WEEK 2, WEEK 4, WEEK 8でHIGH)、BUN (SCREENING 1, UNSCHEDULED 1.1, WEEK 6でHIGH)、HCT (SCREENING 1でHIGH)、WBC (SCREENING 1, WEEK 6, WEEK 8, WEEK 12でHIGH) が基準値上限を超過していますが、臨床的に有意な逸脱と判断されましたか？
            2. TSH、VITB12が基準値範囲外ですが、これらは中央検査機関で測定された値ですか？
            3. 除外基準EXCL27またはEXCL28に抵触すると判断された場合、治験責任医師はプロトコルからの逸脱を判断されましたか？
            4. 上記検査値異常に対する再検査の実施状況と、臨床的な意義についてご意見を伺いたいと存じます。
        * 判断理由: 除外基準EXCL27およびEXCL28に抵触する可能性のある臨床検査値異常が複数認められるため、医療機関に詳細な状況と医学的判断を確認する必要があると判断しました。

クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMTRT = HYDROCORTISONE, TOPICAL, TI.EXCL31
        * 医療機関への問い合わせ文面: 併用薬HYDROCORTISONE, TOPICALは、除外基準EXCL31で禁じられているmedications within 1 month prior to enrollment (see list)に該当しますか？
        * 判断理由: 除外基準EXCL31（Treatment with medications within 1 month prior to enrollment (see list)）に抵触する可能性があるため、医療機関に併用薬HYDROCORTISONE, TOPICALが除外基準リストに該当するか確認する必要がある。

# 01-701-1097
## Task1: Clinical Review Results
**症例サマリー:**

患者ID: 01-701-1097
* 2013年12月23日 (Day -7): CENTRUMをSCREENING 1から併用開始 (PROPHYLAXIS OR NON-THERAPEUTIC USE)
* 2013年12月30日 (Day -1): CENTRUMをSCREENING 2で併用継続
* 2014年01月01日 (Day 1): CENTRUMをBASELINEで併用継続
* 2014年01月15日 (Day 15): CENTRUMをWEEK 2で併用継続
* 2014年01月29日 (Day 29): 検査値Eosinophils (好酸球) が基準値上限超え (HIGH)、CENTRUMをWEEK 4で併用継続
* 2014年02月04日 (Day 30): CENTRUMをAMBUL ECG REMOVALで併用継続
* 2014年02月11日 (Day 42): CENTRUMをWEEK 6で併用継続
* 2014年02月20日 (Day 51): PRURITUS GENERALISED (全身性掻痒症) および APPLICATION SITE VESICLES (適用部位小水疱) が発現 (いずれも軽度、APPLICATION SITE VESICLES はRECOVERED/RESOLVED)、HYDROCORTISONEをWEEK 8から併用開始 (5日間、QD、TOPICAL)
* 2014年02月21日 (Day 52): APPLICATION SITE PRURITUS (適用部位掻痒症) が発現 (軽度、未回復)
* 2014年02月26日 (Day 57): CENTRUMをWEEK 8で併用継続
* 2014年03月21日 (Day 80): PRURITUS GENERALISED (全身性掻痒症) が再発 (中等度、RECOVERED/RESOLVED)
* 2014年03月26日 (Day 85): 検査値Eosinophils (好酸球) が基準値上限超え (HIGH)、CENTRUMをWEEK 12で併用継続、HYDROCORTISONEをWEEK 12から併用開始 (3日間、QD、TOPICAL)
* 2014年03月31日 (Day 90): PRURITUS GENERALISED (全身性掻痒症) が再々発 (中等度、RECOVERED/RESOLVED)
* 2014年04月19日 (Day 109): NASAL CONGESTION (鼻閉) および PHARYNGOLARYNGEAL PAIN (咽喉頭痛) が発現 (いずれも軽度、RECOVERED/RESOLVED)、PRURITUS GENERALISED (全身性掻痒症) が再々々発 (中等度、RECOVERED/RESOLVED)
* 2014年04月23日 (Day 113): CENTRUMをWEEK 16で併用継続、HYDROCORTISONEをWEEK 16から併用開始 (5日間、QD、TOPICAL)、APPLICATION SITE PRURITUS (適用部位掻痒症) が悪化 (中等度、未回復)
* 2014年05月21日 (Day 141): CENTRUMをWEEK 20で併用継続、APPLICATION SITE PRURITUS (適用部位掻痒症) が発現
* 2014年05月23日 (Day 143): HYDROCORTISONEを併用開始 (PRN、TOPICAL)
* 2014年06月18日 (Day 169): CENTRUMをWEEK 24で併用継続、HYDROCORTISONEをWEEK 24から併用開始 (PRN、TOPICAL、開始日のみ記載、終了日不明)
* 2014年07月09日 (Day 190): 試験完了、FINAL LAB VISIT (最終検査)、CENTRUMをWEEK 26で併用継続、HYDROCORTISONEをWEEK 26で併用継続 (PRN、TOPICAL、開始日のみ記載、終了日不明)

---

**クエリ:**

患者ID: 01-701-1097
* クエリNo.: 1
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: AE.AETERM="APPLICATION SITE PRURITUS", CM.CMTRT="HYDROCORTISONE"
    * 医療機関への問い合わせ文面: 治験参加患者 01-701-1097 に適用部位掻痒症が継続していますが、併用薬のヒドロコルチゾン軟膏は症状コントロールに寄与していますか？もし寄与していない場合、治験薬との因果関係についてどのように評価しますか？
    * 判断理由: 患者に適用部位掻痒症が継続的に発現しており、治験薬との関連性が疑われる。症状コントロールと治験薬との因果関係について確認するため。
* クエリNo.: 2
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CM.CMDOSU=VIAL, CM.CMDOSFRQ=QD, CM.CMROUTE=TOPICAL (HYDROCORTISONE)
    * 医療機関への問い合わせ文面: 併用薬HYDROCORTISONEについて、投与剤形、投与頻度、投与経路がTABLET, QD, ORAL以外で投与された理由を確認してください。
    * 判断理由: 併用薬HYDROCORTISONEの投与経路、剤形、投与頻度が想定と異なるため、データ入力誤りの可能性、プロトコル逸脱の可能性を確認するため。
* クエリNo.: 3
    * 臨床試験結果への影響度合い: None
    * 変数名と値: LB.LBTESTCD=EOS, VISIT=WEEK 8, VISIT=WEEK 12, LBORRES=0.89 THOU/uL, LBORRES=0.87 THOU/uL
    * 医療機関への問い合わせ文面: 治験実施医療機関に、Week 8 および Week 12 における好酸球増加の原因について、治験責任医師の見解を伺ってください。治験薬との因果関係、併用薬、患者の基礎疾患（アレルギー性疾患の既往等）など、考えられる要因について情報提供を依頼してください。
    * 判断理由: Week 8 および Week 12 で好酸球数増加 (HIGH) が確認されました。治験薬との因果関係は「POSSIBLE」と評価されていますが、治験薬投与との関連性が否定できません。臨床的に意義のある好酸球増多症である可能性を考慮し、念のため医療機関に背景因子等について問い合わせを行います。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMENDTC, AE.AESTDTC, AE.AEENDTC, LB.LBDTC, LB.LBNRIND (EOS), QS.QSDTC, QS.QSTORRES, DM.DMDTC

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMENDTC, CM.CMDTC (CMSEQ=9)
    * 矛盾の内容: CM.CMENDTC（併用薬終了日）がCM.CMDTC（併用薬データ収集日）より前の日付（2014-02-25 vs 2014-02-26）になっています。併用薬の投与期間がデータ収集日より前に終了しているのは矛盾している可能性があります。
    * 問題点の原因（推測）: データ入力時の誤り、または併用薬終了日がデータ収集日より前である正当な理由が存在する可能性。
    * 対応策（提案）: CMドメインのデータ収集日と併用薬終了日の整合性を確認し、必要であれば医療機関に確認します。

* 問題No.: 2
    * 変数名と値: CM.CMENDTC (null) (HYDROCORTISONE, CMSEQ=5, 16, 18)
    * 矛盾の内容: CMドメインの HYDROCORTISONE (CMSEQ=5, 16, 18) のレコードにおいて、CMENDTC（併用薬終了日）が空欄です。HYDROCORTISONEの投与が継続しているのか、終了日が不明確です。
    * 問題点の原因（推測）: データ入力時の未入力、または併用薬が継続投与で終了日が未定のため空欄となっている可能性。
    * 対応策（提案）: CMドメインの併用薬HYDROCORTISONEの投与状況（継続/終了）を確認し、終了している場合はCMENDTCを更新、継続中の場合は空欄の理由を確認します。Define.xmlにCMENDTC, CMENDYの必須/非必須属性を追記することを検討する。

* 問題No.: 3
    * 変数名と値: AE.AESTDTC (2014-01-03, 2014-02-21), EX.EXSTDTC (2014-01-01, 2014-01-01) (AESEQ=4, 10)
    * 矛盾の内容: AEドメインのAdverse Event Start Date/Time (AESTDTC) が、EXドメインのTreatment Start Date/Time (EXSTDTC) より早い日付で記録されています。治験薬投与前にAdverse Event が発現している可能性、またはデータ入力時の誤りの可能性があります。
    * 問題点の原因（推測）: データ入力ミス、または治験薬投与開始前に有害事象が発現
    * 対応策（提案）: 医療機関にAESTDTCとEXSTDTCの整合性について確認し、必要に応じてデータ修正を依頼してください。

* 問題No.: 4
    * 変数名と値: AE.AEENDTC (null) (AESEQ=1, 2, 10)
    * 矛盾の内容: AE.AEENDTC（有害事象終了日）が空欄です。APPLICATION SITE PRURITUSの有害事象が継続しているのか、終了日が不明確です。
    * 問題点の原因（推測）: データ入力時の誤り、または有害事象が継続中で終了日が未定のため空欄となっている可能性。
    * 対応策（提案）: AEドメインの有害事象APPLICATION SITE PRURITUSの転帰状況（治癒/未治癒）を確認し、治癒している場合はAEENDTCを更新、未治癒の場合は空欄の理由を確認します。

* 問題No.: 5
    * 変数名と値: LB.LBDTCとVISITDYのずれ
    * 矛盾の内容: VISITDY（計画されたVisit Day）とLBDY（検査実施日）にずれが見られます。Row Index 5では、VISITDYが57日目であるのに対し、VISITはWEEK 8（56日目）となっています。
    * 問題点の原因（推測）: 検査実施日の記録ミス、またはVisit windowによるずれの可能性。
    * 対応策（提案）: LBドメインのLBDTCとVISITDYのずれが許容範囲内か、プロトコル照らし合わせて確認します。逸脱している場合は、データの修正が必要か検討します。

* 問題No.: 6
    * 変数名と値: LB.LBTESTCD=EOS, LBNRIND=HIGH (WEEK 8, WEEK 12)
    * 矛盾の内容: 患者 01-701-1097 において、Week 8 と Week 12 の好酸球（EOS）検査値が基準範囲上限を超えています。しかし、AEドメインには、EOS増加と関連する有害事象（例：好酸球増加症、アレルギー反応など）の報告が見当たりません。
    * 問題点の原因（推測）:
        * データ入力時のLBNRINDの誤り
        * 臨床判断により、治験担当医が好酸球増加を臨床的に問題なしと判断した可能性
        * AEドメインへの有害事象の報告漏れ
    * 対応策（提案）: クエリNo.3を発行し、医療機関にLB検査値異常とAEドメインの関連有害事象の有無を確認します。

* 問題No.: 7
    * 変数名と値: QS.QSTORRES (ACITM08, 空欄)
    * 矛盾の内容: 質問票データ (QS) のWORD RECOGNITION (ACITM08) の結果が空欄となっているレコードが存在する。
    * 問題点の原因（推測）: データ入力時の脱落、または評価が実施されなかった可能性。
    * 対応策（提案）: QSドメインのWORD RECOGNITION (ACITM08) 評価が空欄となっているレコードについて、医療機関にデータ確認を依頼し、必要に応じて修正を依頼する。

* 問題No.: 8
    * 変数名と値: QS.QSDTCとVISITDYのずれ
    * 矛盾の内容: VISITDY（計画されたVisit Day）とQSDY（検査実施日）にずれが見られます。LBドメインと同様に、VISITDYとQSDYにずれが見られます。
    * 問題点の原因（推測）: 検査実施日の記録ミス、またはVisit windowによるずれの可能性。
    * 対応策（提案）: QSドメインのQSDTCとVISITDYのずれが許容範囲内か、プロトコル照らし合わせて確認します。逸脱している場合は、データ修正が必要か検討します。

* 問題No.: 9
    * 変数名と値: DM.DMDTC (2013-12-23), DM.RFSTDTC (2014-01-01)
    * 矛盾の内容: DM.DMDTC（ demographics情報の収集日）がDM.RFSTDTC（治験薬初回投与日）よりも過去の日付になっています。一般的に demographics情報は治験薬投与開始前、または投与開始日当日に収集されるべきであり、DM.DMDTCがDM.RFSTDTCより過去日付であることは、データ収集プロセスに矛盾がある可能性を示唆しています。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータ収集日の誤りの可能性。
    * 対応策（提案）: DM.DMDTCの日付が正しいか、医療機関に確認してください。もし誤りの場合、修正が必要です。

クエリ:
* 患者ID: 01-701-1097
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: AE.AESTDTC (2014-01-03, 2014-02-21), EX.EXSTDTC (2014-01-01, 2014-01-01)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 の AE (Adverse Event) ドメイン、AESEQ=4, 10 の有害事象について、Adverse Event Start Date/Time (AESTDTC) が Treatment Start Date/Time (EXSTDTC) よりも先行して記録されています。治験薬投与前に有害事象が発現した状況は医学的に矛盾している可能性があり、データの正確性を確認させて頂きたく、AESTDTCの日付がEXSTDTCより早い理由についてご回答いただけますでしょうか。もしデータ入力誤りの場合は、修正をお願いいたします。
        * 判断理由: クロスドメインでの日付の矛盾はデータ整合性における重大な問題であり、臨床試験の解釈に影響を与える可能性があるため、重要度を Major と判断しました。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMENDTC: "", CM Row Index: 17, 18 (HYDROCORTISONE, CMSEQ=5)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 の併用薬 HYDROCORTISONE (CMSEQ=5) の投与終了日 (CMENDTC, CMENDY) が空欄となっています。投与は継続中でしょうか、終了している場合は終了日をご教示ください。
        * 判断理由: 併用薬の投与期間は、有害事象との関連性や治験薬の効果に影響を与える可能性があるため、重要な項目です。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD=EOS, LB.VISIT=WEEK 8, LB.LBNRIND=HIGH, LB.LBORRES=0.89 THOU/uL, LB.VISIT=WEEK 12, LB.LBNRIND=HIGH, LB.LBORRES=0.87 THOU/uL
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 の Week 8 と Week 12 の臨床検査データにおいて、好酸球（EOS）の値が基準範囲上限を超えていることを確認しました。これらの検査値異常に関して、有害事象（アレルギー反応や好酸球増加症など）は報告されていますでしょうか？もし有害事象が報告されていない場合、好酸球増加の原因として臨床的に懸念される事項はありますでしょうか？治験担当医の見解を伺いたく、ご回答をお願いいたします。
        * 判断理由: 治験薬との関連性が否定できない検査値異常であり、患者の安全性に関わる可能性があるため、念のため医療機関に背景と医学的解釈を確認することが望ましいと判断しました。ただし、現時点では重篤な有害事象の報告はなく、データ品質への影響は限定的と考えられるため、臨床試験結果への影響度はMinorと判断しました。

    * クエリNo.: 4
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: QS.QSTORRES (QSTESTCD=ACITM08, VISIT=BASELINE, WEEK 8, WEEK 16, WEEK 24)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 の質問票データにおいて、アルツハイマー病評価尺度 - 認知下位尺度 (ADAS-Cog) のWORD RECOGNITION (ACITM08) の評価結果が複数のVisitで空欄となっています。評価が実施されなかった理由、または評価結果をご教示ください。
        * 判断理由: 認知機能評価項目であり、データの欠損は解析に影響を与える可能性があります。

    * クエリNo.: 5
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: CM.CMENDTC: "", CM Row Index: 17, 18 (HYDROCORTISONE, CMSEQ=16, 18)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 の併用薬 HYDROCORTISONE (CMSEQ=5) の投与終了日 (CMENDTC, CMENDY) が空欄となっています。投与は継続中でしょうか、終了している場合は終了日をご教示ください。
        * 判断理由: 併用薬の投与期間は、有害事象との関連性や治験薬の効果に影響を与える可能性があるため、重要な項目です。

    * クエリNo.: 6
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DM.DMDTC (2013-12-23), DM.RFSTDTC (2014-01-01)
        * 医療機関への問い合わせ文面: 患者ID 01-701-1097 のDemographics情報収集日（DM.DMDTC）が治験薬初回投与日（DM.RFSTDTC）より過去の日付となっています。DM.DMDTCに記録されている日付は正しいでしょうか？もし誤りの場合は、正しい日付をご教示ください。
        * 判断理由: DM.DMDTCの日付の誤りは、データの信頼性を損なう可能性があります。データ収集日を正しく把握することは、データ解釈の正確性を担保するために重要です。

クエリなし
## Task3: Protocol Deviation Review Results
患者ID: 01-701-1097
    逸脱No.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBTESTCD=SODIUM, LB.LBORRES=134 mEq/L (SCREENING 1)
        逸脱内容: スクリーニング検査（SCREENING 1）において、血清ナトリウム値が基準範囲を下回る低ナトリウム血症（134 mEq/L）が確認されました。プロトコルで規定された除外基準[27b]に抵触する可能性があります。
        プロトコル該当箇所: 除外基準 [27b] Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes:  ↑↓ serum sodium
        判断理由: SDTMデータセットLBドメインの臨床検査データにおいて、患者01-701-1097のスクリーニング検査時の血清ナトリウム値がプロトコルで規定された基準範囲を下回っている可能性があり、選択基準逸脱に該当する疑いがあるため。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: LB.LBNRIND=HIGH (EOS, WEEK 8, WEEK 12), LB.LBNRIND=HIGH (LYM, WEEK 4)
        逸脱内容: 治験参加者の臨床検査値において、好酸球数（EOS）およびリンパ球数（LYM）が基準範囲外の高値を示しています。
            * 好酸球数 (EOS): WEEK 8, WEEK 12で基準範囲上限超え
            * リンパ球数 (LYM): WEEK 4で基準範囲上限超え
        プロトコル該当箇所: 除外基準 [27b] Laboratory test values exceeding the Lilly Reference Range III for the patient’s age in any of the following analytes:  ↑↓ white blood cell count
        判断理由: プロトコルで規定された除外基準[27b]の臨床検査値異常に該当する可能性があり、臨床試験結果に影響を与える可能性があるため。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC = 2013-10, DM.RFSTDTC = 2014-01-01
        逸脱内容: 併用薬CENTRUMの開始日（2013年10月）が、Subject Reference Start Date/Time（2014年01月01日）より前です。
        プロトコル該当箇所: プロトコルに併用薬の開始時期に関する規定は明記されていないが、SDTM Conformance GuideではCMSTDTCはRFSTDTC以降であることが推奨されている。
        判断理由: SDTM Conformance GuideではCMSTDTCはRFSTDTC以降であることが推奨されているものの、必須ではありません。プロトコルに併用薬の開始時期に関する明確な規定はなく、医学的な妥当性の観点からも臨床試験の実施に大きな影響はないと考えられるため、Minor Deviationと判断しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMTRT=HYDROCORTISONE, CMROUTE=TOPICAL
        逸脱内容: 併用薬としてHYDROCORTISONE（外用）が使用されています。プロトコルでは全身性コルチコステロイドは併用禁止薬とされていますが、外用剤であるHYDROCORTISONEが全身性コルチコステロイドに該当するか不明確です。
        プロトコル該当箇所: 3.8. Concomitant Therapy, 3.4.2.2. Exclusion Criteria [31b] Treatment with medications within 1 month prior to enrollment (see list). k) Systemic corticosteroids including but not limited to ...
        判断理由: プロトコルで併用が禁止されているのはsystemic corticosteroids（全身性コルチコステロイド）であり、外用剤であるHYDROCORTISONEが該当するかどうか不明なため、プロトコル逸脱の疑いとして検出しました。ただし、外用剤であるため、全身性の薬剤と比較して臨床試験への影響は小さいと考えられ、影響度合いはMinorと判断しました。

クエリNo.: 1
    臨床試験結果への影響度合い: Major
    変数名と値: LB.LBTESTCD=SODIUM, LB.LBORRES=134 mEq/L (SCREENING 1)
    医療機関への問い合わせ文面:
        患者ID 01-701-1097 のスクリーニング検査（SCREENING 1）における血清ナトリウム値について確認させてください。
        血清ナトリウム値が134 mEq/Lと基準範囲を下回っておりますが、本試験プロトコルにおける血清ナトリウム値の基準範囲（Lilly Reference Range III）をご教示いただけますでしょうか。
        また、被験者01-701-1097の血清ナトリウム値134 mEq/Lは、プロトコルで規定された基準範囲内であるか、範囲外であるか、ご回答をお願いいたします。
        基準範囲外である場合、選択基準逸脱として取り扱うべきか、治験責任医師の見解と併せてご回答をお願いいたします。
    判断理由: プロトコル除外基準[27b]に抵触する可能性のある血清ナトリウム値の異常値について、基準範囲と照らし合わせて医療機関に確認する必要があるため。

クエリNo.: 2
    臨床試験結果への影響度合い: Major
    変数名と値: LB.LBNRIND=HIGH (EOS, WEEK 8, WEEK 12), LB.LBNRIND=HIGH (LYM, WEEK 4)
    医療機関への問い合わせ文面:
        患者ID 01-701-1097 の臨床検査値異常（好酸球数およびリンパ球数増加）について確認させてください。
        LBドメインデータにおいて、以下の検査項目でReference Range Indicator (LBNRIND) が異常値 (HIGH) を示しています。
          - EOS (WEEK 8): LBNRIND=HIGH
          - EOS (WEEK 12): LBNRIND=HIGH
          - LYM (WEEK 4): LBNRIND=HIGH
        これらの検査値異常について、以下の点について医療情報に基づきご回答をお願いいたします。
        1. 患者の組み入れ基準（選択基準/除外基準）逸脱に該当するか否か
        2. 臨床試験結果に影響を与える可能性の有無
        3. 治験責任医師の見解（臨床的な解釈と対応方針）
    判断理由: プロトコル除外基準[27b]に抵触する可能性のある臨床検査値異常について、選択基準逸脱の該当性、臨床試験結果への影響、治験責任医師の見解を確認するため。

クエリNo.: 3
    臨床試験結果への影響度合い: Minor
    変数名と値: CM.CMTRT = HYDROCORTISONE, CM.CMROUTE = TOPICAL
    医療機関への問い合わせ文面:
        患者ID 01-701-1097 における併用薬 HYDROCORTISONE（外用）の使用について確認させてください。
        プロトコル 3.8項 および 3.4.2.2項（除外基準[31b]）では、全身性コルチコステロイドは併用禁止薬とされていますが、HYDROCORTISONE外用剤の使用は

# 01-703-1086
## Task1: Clinical Review Results
**1. 症例サマリーの作成:**

患者ID: 01-703-1086
* 2012年08月31日 (Day -2): 白血球数 (Leukocytes) が基準値下限を下回る (LOW)。
* 2012年09月13日 (Day 12): 適用部位刺激 (APPLICATION SITE IRRITATION) が発現。軽度 (MILD)。
* 2012年09月16日 (Day 15): 
    * 適用部位刺激 (APPLICATION SITE IRRITATION) の重症度が中等度 (MODERATE) に悪化。
    * AST (アスパラギン酸アミノトランスフェラーゼ) 検査値が基準値上限を超過 (HIGH)。
* 2012年09月30日 (Day 29): 適用部位刺激 (APPLICATION SITE IRRITATION) の重症度が重度 (SEVERE) に悪化。
* 2012年10月02日 (Day 31): 好酸球 (Eosinophils) 検査値が基準値上限を超過 (HIGH)。
* 2012年10月09日 (Day 38): 悪寒 (CHILLS) が発現。軽度 (MILD)。
* 2012年10月13日 (Day 42): 
    * 適用部位刺激 (APPLICATION SITE IRRITATION) の重症度が軽度 (MILD) に改善。
    * 好酸球 (Eosinophils) 検査値がさらに基準値上限を超過 (HIGH)。
* 2012年10月27日 (Day 56): 
    * 適用部位刺激 (APPLICATION SITE IRRITATION) の重症度が中等度 (MODERATE) に悪化。
    * 好酸球 (Eosinophils) 検査値が依然として基準値上限を超過 (HIGH)。
    * クレアチンキナーゼ (CK) 検査値が基準値上限を超過 (HIGH)。
* 2012年11月27日 (Day 87): クレアチンキナーゼ (CK) 検査値が基準値上限を超過 (HIGH)。
* 2012年12月24日 (Day 114): 
    * 試験中止 (ADVERSE EVENT)。
    * 白血球数 (Leukocytes) 検査値が基準値下限を下回る (LOW)。
    * クレアチンキナーゼ (CK) 検査値が基準値上限を超過 (HIGH)。
* 2013年01月02日 (Day 123): 適用部位刺激 (APPLICATION SITE IRRITATION) は未回復。
* 2013年03月26日 (Day 206): 白血球数 (Leukocytes) 検査値が基準値下限を下回る (LOW)。

---

**2. クエリの作成:**

クエリなし
## Task2: DM Review Results
データ整合性レビュー報告

全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMDTC, EX.EXENDTC, DM.RFXENDTC, DS.DSDTC, DM.RFXSTDTC, LB.LBSTRESN (AST, CK, EOS, WBC), LBNRIND, QSドメインの欠損値, DM.DTHDTC, DM.DTHFL, DM.RFICDTC, QS.QSORRESU, QS.QSSTRESU

問題点:
* 問題No.1: 日付の矛盾 (CMドメイン)
    * 変数名と値: CM.CMSTDTC, CM.CMDTC (CMドメインのレコード1-19)
    * 矛盾の内容: 併用薬データにおいて、データ収集日 (CMDTC) が薬剤の併用開始日 (CMSTDTC) より前になっているレコードが複数存在する。データ収集日にCMデータが確定している必要があり、併用開始日がデータ収集日より未来日であることは考えにくい。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータ収集日の記録誤りの可能性。
    * 対応策（提案）: 医療機関にCM.CMSTDTCとCMDTCの記録が正しいか確認するクエリを発行し、記録に誤りがあれば修正を依頼する。

* 問題No.2: 日付の矛盾 (EXとDMドメイン)
    * 変数名と値: EX.EXENDTC, DM.RFXENDTC
    * 矛盾の内容: 治験薬終了日 (EX.EXENDTC) がDMドメインの最終投与日 (DM.RFXENDTC) より後になっている。EXドメインとDMドメインで治験薬投与期間の整合性が取れていない。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータセット間のデータ転送時のエラーの可能性。
    * 対応策（提案）: 医療機関にEX.EXENDTCとDM.RFXENDTCの記録が正しいか確認するクエリを発行し、記録に誤りがあれば修正を依頼する。

* 問題No.3: 日付の矛盾 (DSとDMドメイン)
    * 変数名と値: DS.DSDTC, DM.RFXSTDTC (DSドメイン 1, 2行目)
    * 矛盾の内容: Dispositionドメインのデータ収集日時 (DS.DSDTC) がDMドメインの初回投与日 (DM.RFXSTDTC) より前になっている。データ収集日時が初回投与日より前なのは時間軸として矛盾している。
    * 問題点の原因（推測）: データ入力時の誤り、またはデータ収集日の記録誤りの可能性。
    * 対応策（提案）: 医療機関にDS.DSDTCとDM.RFXSTDTCの記録が正しいか確認するクエリを発行し、記録に誤りがあれば修正を依頼する。

* 問題No.4: 臨床検査値の異常値 (LBドメイン)
    * 変数名と値: LB.LBTESTCD (AST, CK, EOS, WBC), LB.LBNRIND (HIGH, LOW), VISIT (SCREENING 1, WEEK 2, WEEK 4, WEEK 6, WEEK 8, WEEK 12, WEEK 16, UNSCHEDULED 1.1)
    * 矛盾の内容: LBドメインの複数の臨床検査項目 (AST, CK, EOS, WBC) で、複数のVISITにわたり基準範囲外の値 (HIGH, LOW) が継続して確認された。特にCK, EOS, WBCは複数のVISITで基準範囲外となっている。
    * 問題点の原因（推測）: 患者の基礎疾患、治験薬の影響、または一過性の生理的変動、データ入力の誤りなどが考えられる。
    * 対応策（提案）: 
        1.  医療機関にLBドメインで報告された検査値異常について、臨床的な意義を確認するクエリを発行する。
        2.  Define.xmlにLB検査値の基準範囲 (LBSTNRHI, LBSTNRLO) の定義が不足している場合は追記する。
        3.  Define.xmlのLBNRINDの値リストに、HIGH_CK, HIGH_AST, HIGH_EOS, LOW_WBC のような具体的な逸脱区分を追加し、臨床的な意義を区別できるようにDefine.xmlの修正を検討する。
        4.  必要に応じて、LBドメインの異常値とAEドメインの有害事象の関連性を調査する。

* 問題No.5: DMドメインの欠損値
    * 変数名と値: DM.DTHDTC, DM.DTHFL, DM.RFICDTC
    * 矛盾の内容: DMドメインの死亡日 (DTHDTC)、死亡フラグ (DTHFL)、IC同意日 (RFICDTC) が欠損している。
    * 問題点の原因（推測）: データ未入力、データ収集の意図的な省略、または情報が取得できなかった。
    * 対応策（提案）: DM.DTHDTC、DTHFL、RFICDTCがデータ収集必須項目であるかプロトコルまたはDefine.xmlで確認する。必須項目の場合、医療機関にデータの再確認と理由の確認を行うクエリを発行する。

* 問題No.6: QSドメインの欠損値
    * 変数名と値: QSドメインのQSSCAT, QSORRESU, QSSTRESU, QSBLFL, QSDRVFL
    * 矛盾の内容: 質問票データ (QS) ドメインにおいて、サブカテゴリ (QSSCAT)、オリジナル単位 (QSORRESU)、標準単位 (QSSTRESU)、ベースラインフラグ (QSBLFL)、派生フラグ (QSDRVFL) に欠損値が多数認められる。
    * 問題点の原因（推測）: データ入力時の脱落、データ変換処理の不備、または質問票の特性上、該当項目が常に必須ではない可能性。
    * 対応策（提案）: データ作成部門に欠損値発生の原因を確認し、データ再入力、データ変換処理の見直し、またはDefine.xmlの修正（必須項目の見直し）を検討する。Define.xml上で必須と定義されている項目が欠損している場合は、データの再入力が必要となる。

クエリ:
* 患者ID: 01-703-1086
    * クエリNo.1:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMDTC, CM.CMSTDTC, CM.CMENDTC
        * 医療機関への問い合わせ文面: 
        患者ID 01-703-1086 の併用薬データについて、データ収集日 (CMDTC) が薬剤の投与終了日 (CMENDTC) より後になっているレコードが複数あります。記録に誤りがないか、データ収集日、併用薬開始日、併用薬終了日を再確認し、修正が必要な場合は修正をお願いします。
        * 判断理由: 併用薬の投与期間とデータ収集日の矛盾は、データ全体の時間軸の整合性を損なう可能性があり、臨床判断に影響を与える可能性があるため、重要度が高いと判断しました。

    * クエリNo.2:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: EX.EXENDTC, DM.RFXENDTC
        * 医療機関への問い合わせ文面: 
        患者ID 01-703-1086 の治験薬データについて、治験薬終了日 (EXENDTC) がDMドメインの最終投与日 (RFXENDTC) より後になっているレコードがあります。記録に誤りがないか、治験薬終了日、最終投与日を再確認し、修正が必要な場合は修正をお願いします。
        * 判断理由: 治験薬投与期間とDMドメインの最終投与日の矛盾は、治験薬の曝露期間の評価に影響を与える可能性があり、臨床判断に影響を与える可能性があるため、重要度が高いと判断しました。

    * クエリNo.3:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DS.DSDTC, DM.RFXSTDTC
        * 医療機関への問い合わせ文面: 
        患者ID 01-703-1086 のDispositionデータについて、データ収集日時 (DSDTC) がDMドメインの初回投与日 (RFXSTDTC) より前になっているレコードがあります。記録に誤りがないか、データ収集日時、初回投与日を再確認し、修正が必要な場合は修正をお願いします。
        * 判断理由: Dispositionイベントの日付が初回投与日より前になっている矛盾は、データ全体の時間軸の整合性を損なう可能性があり、臨床判断に影響を与える可能性があるため、重要度が高いと判断しました。

    * クエリNo.4:
        * 臨床試験結果への影響度合い: Minor
        * 変数名と値: LB.LBTESTCD (AST, CK, EOS, WBC), LB.LBNRIND (HIGH, LOW)
        * 医療機関への問い合わせ文面: 
        患者ID 01-703-1086 の臨床検査値データにおいて、AST、CK、EOSが基準範囲上限超過、WBCが基準範囲下限を下回る検査値異常が複数回報告されています。これらの検査値異常について、臨床的な解釈、患者様の状態、治験薬との関連性について可能な範囲でご教示ください。
        * 判断理由: 基準範囲外の臨床検査値は、安全性評価において重要な情報であり、臨床的な解釈を確認することはデータレビューにおいて重要であるため。

    * クエリNo.5:
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: DM.DTHDTC, DM.DTHFL, DM.RFICDTC
        * 医療機関への問い合わせ文面: 
        患者ID 01-703-1086 のDemographicsドメインにおいて、死亡日、死亡フラグ、インフォームドコンセント日が欠損しています。これらの情報は重要な患者背景情報となりますので、可能な範囲でご回答をお願いします。
        * 判断理由: 欠損しているDMドメインの項目は重要な患者背景情報であり、データ品質を向上させるために可能な限り情報を収集する必要があるため。

Define.xmlの修正候補:
*   LBドメイン: LBNRIND の値リストに "HIGH_CK", "HIGH_AST", "HIGH_EOS", "LOW_WBC" などの具体的な逸脱区分を追加し、臨床的な意義を区別できるように修正することを提案します。また、LBSTNRHI, LBSTNRLO のItemDef定義に基準範囲情報を明記することを推奨します。
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1086
    逸脱No.: 1
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMTRT = CALAMINE, CORTISONE
        逸脱内容: 併用薬としてCALAMINE、CORTISONEが使用されていますが、プロトコルで併用が禁止されている薬剤リストに該当するか不明です。
        プロトコル該当箇所: プロトコル 3.8 Concomitant Therapy, 3.4.2.2 Exclusion Criteria [31b]
        判断理由: CALAMINE、CORTISONEが併用禁止薬リストに該当する可能性があるため、プロトコル逸脱の疑いとして検出しました。医療機関へのクエリにて併用状況を確認する必要があります。

    逸脱No.: 2
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.VISIT = UNSCHEDULED 1.1
        逸脱内容: 計画された評価スケジュールに含まれない「UNSCHEDULED 1.1」のVisitが実施されています。
        プロトコル該当箇所: Protocol Attachment LZZT.1. Schedule of Events for Protocol H2Q-MC-LZZT(c)
        判断理由: LBドメインに計画外のVISITNUM=1.1のデータが存在するため、評価スケジュールからの逸脱の疑いとして検出しました。ただし、Define.xml上はUNSCHEDULED VISITが定義されているため、軽微な逸脱の可能性があります。

    クエリNo.: 1
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT = CORTISONE, CALAMINE
        医療機関への問い合わせ文面: 
            被験者01-703-1086に併用が記録されているCORTISONE、CALAMINEについて、以下の点をご確認ください。
            1.  CORTISONE、CALAMINEはプロトコルで併用が禁止されている薬剤に該当しますでしょうか？
            2.  併用が禁止されている場合、投与開始日、投与量、投与経路、投与期間、および治験薬との併用期間をご教示ください。
            3.  プロトコル逸脱に該当する場合、治験責任医師の見解と、臨床試験結果への影響、今後の対応についてご回答ください。
        判断理由: 併用薬CORTISONE、CALAMINEがプロトコルで併用禁止されている薬剤に該当するか不明なため、医療機関に確認が必要です。併用禁止薬に該当する場合、プロトコル逸脱となり、臨床試験結果に影響を与える可能性があります。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: AE.AETERM = APPLICATION SITE IRRITATION, AE.AEOUT, AE.AEENDTC
        医療機関への問い合わせ文面: 
            被験者01-703-1086で複数回報告されているAdverse Event (APPLICATION SITE IRRITATION) の転帰について、以下の点をご確認ください。
            1.  Adverse Event (AESEQ=1, 2, 3, 6) それぞれの正確なEnd Date (AEENDTC) をご教示ください。
            2.  Adverse Event (AESEQ=1, 2, 3) のOutcome (AEOUT) が "NOT RECOVERED/NOT RESOLVED" と記録されていますが、Week 16 (VISITNUM=10) 以降もAdverse Eventは継続していましたでしょうか？
            3.  Adverse Event (AESEQ=6) のOutcome (AEOUT) が "RECOVERED/RESOLVED" と記録されていますが、Adverse Eventは本当にWeek 16 (VISITNUM=10) 以前にRECOVERED/RESOLVEDしましたでしょうか？
            4.  もしデータに誤りがある場合、修正されたデータをご提供ください。
        判断理由: Adverse Event (APPLICATION SITE IRRITATION) のEnd Date (AEENDTC) が全て同じ日付で記録されており、データ入力時のエラーの可能性があります。また、Outcome (AEOUT) の情報も矛盾しているため、医学的妥当性の観点から医療機関への確認が必要です。

# 01-703-1042
## Task1: Clinical Review Results
**症例サマリー:**

患者ID: 01-703-1042
* 2012年12月27日 (Day -65): スクリーニング1回目の検査にて、ALT 135 U/L (基準値上限超過)、AST 145 U/L (基準値上限超過)と、肝機能酵素の上昇が確認されました。
* 2013年02月21日 (Day -9):  非計画的な検査1.1回目で、血清ナトリウム値が基準値下限を下回る (133 mEq/L)。
* 2013年03月04日 (Day 3):  WEEK 2の期間に下痢を発症（軽度）。
* 2013年03月05日 (Day 4):  WEEK 2の期間に不眠症を発症（軽度）。
* 2013年03月28日 (Day 27):  WEEK 4の検査で、異形赤血球 (Anisocytes) が異常値 (1) を示しました。平均赤血球容積 (MCV) が基準値上限を超過 (101 fL)。また、血清ナトリウム値が基準値上限を超過 (146 mEq/L)。
* 2013年08月31日 (Day 183):  WEEK 26の検査にて、AST 38 U/L (基準値上限超過)と、ASTの基準値上限超過が再度確認されました。

---

**クエリの作成:**

患者ID: 01-703-1042
* クエリNo.1:
    * 臨床試験結果への影響度合い: Critical
    * 変数名と値: LB.LBTESTCD = "ALT", "AST", "SODIUM" (LBドメイン)
    * 医療機関への問い合わせ文面:
        患者ID: 01-703-1042において、スクリーニング1回目とWEEK26の検査で肝機能酵素 (ALT, AST) の上昇、UNSCHEDULED 1.1で低ナトリウム血症が確認されています。
        1.  肝機能酵素上昇 (ALT, AST) の原因、詳細な臨床所見、及び肝機能障害の有無について教えてください。
        2.  低ナトリウム血症 (SODIUM 133 mEq/L) の原因、詳細な臨床所見、及び電解質検査の再検査実施の有無について教えてください。降圧剤（NORVASC）との関連も考慮ください。
        3.  これらの検査値異常について、治験薬との関連性について治験担当医師の見解を教えてください。
        4.  患者の安全性確保のために行った対応（休薬、中止、用量変更、追加検査、専門医へのコンサルテーション等）があれば、具体的に教えてください。
        5.  治験継続の可否について、治験担当医師の見解を教えてください。
    * 判断理由:
        ALT、ASTの上昇は肝機能障害、低ナトリウム血症は電解質異常を示唆し、患者の安全性に重大な影響を与える可能性があります。
        治験薬との因果関係、考えられる原因、患者の臨床状態、治験継続の可否について確認が必要と判断しました。
        臨床試験の主要評価項目である安全性と有効性の評価に影響を与える可能性があるため、Criticalと判断しました。

* クエリNo.2:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: QS.QSTESTCD = "DAITM29" (QSドメイン), VISIT = "BASELINE"
    * 医療機関への問い合わせ文面:
        DISABILITY ASSESSMENT FOR DEMENTIA (DAD) の質問項目DAITM29 (RETURN FROM THE STORE) のBASELINE評価がNA (96) となっています。
        NAと判断された理由について、詳細をご教示ください。
        データ入力誤りの可能性も考慮し、回答をお願いします。
    * 判断理由:
        DAITM29は日常生活動作に関する重要な評価項目であり、NA (該当せず) の理由を確認することで、評価の妥当性を検証する必要があると考えられます。
        データの正確性を確認するため、Minorクエリとして医療機関への確認を提案します。

* クエリNo.3:
    * 臨床試験結果への影響度合い: Minor
    * 変数名と値: CMドメイン CMENDTC (併用薬終了日) が空欄となっているデータ
    * 医療機関への問い合わせ文面:
        CMドメインにおいて、CMENDTC (併用薬終了日) が空欄となっている併用薬が複数あります。
        1.  CMENDTCが空欄となっている併用薬の投与状況（継続中、中止日不明など）について教えてください。
        2.  併用薬が継続中の場合、CMENDTCを更新する予定はありますか。
        3.  CMENDTCが不明な場合は、不明となっている理由と、今後の情報収集計画について教えてください。
    * 判断理由:
        CMENDTC欠損は併用薬の使用状況を不明確にし、安全性評価やデータ解釈に影響を与える可能性があります。
        データの品質管理の観点から、CMENDTCの情報を収集し、データの正確性を向上させるため、Minorクエリとして医療機関への確認を提案します。
## Task2: DM Review Results
全体的なデータ品質の評価:
* 総合評価: 一部問題あり
* データクリーニング/再調査が必要な項目: CM.CMSTDTC, CM.CMDTC, CM.CMENDTC, LB.LBORRES (ALT, AST, SODIUM, MCV, AST), LB.LBNRIND (ALT, AST, SODIUM, MCV, AST), LBドメインのnull値項目

問題点:
* 問題No.: 1
    * 変数名と値: CM.CMSTDTC, CMDTC (CMドメイン全般)
    * 矛盾の内容: 併用薬開始日 (CM.CMSTDTC) がデータ収集日 (CM.CMDTC) より未来の日付になっているレコード、および併用薬開始日がデータ収集日より過去になっているレコードが複数存在する。論理的に矛盾しているか、データ入力時の誤りの可能性がある。
    * 問題点の原因（推測）: データ入力時の日付誤り、データ収集日の記録ミス
    * 対応策（提案）: 医療機関にCMドメインのCMSTDTCとCMDTCの日付の整合性についてMedical History情報を参照の上、データ確認を依頼し、必要に応じてデータ修正を行う。

* 問題No.: 2
    * 変数名と値: CM.CMENDTC (CMドメイン row 2-14)
    * 矛盾の内容: CMドメインのrow 2-14において、CMENDTCとCMENDYが欠損している。CMTRTはNORVASCであり、継続的な投与が想定される薬剤であるにもかかわらず、投与終了日が記録されていない。
    * 問題点の原因（推測）: データ入力時の欠落、またはNORVASCのような慢性疾患治療薬では投与終了日を記録しない運用ルール
    * 対応策（提案）: データ入力者にCMENDTCとCMENDYがnullとなっている理由を確認、Define.xml/プロトコル/CRFと照らし合わせ、医療機関への問い合わせも検討する。

* 問題No.: 3
    * 変数名と値: LB.LBTESTCD (ALT, AST, SODIUM, MCV, AST), LB.LBORRES, LB.LBNRIND (LBドメイン row 3, 4, 26, 63, 132, 334, 40, 41, 77, 78, 100, 112, 114, 117, 118, 121, 122, 126, 127, 131, 134, 135, 136, 140, 143, 144, 147, 148, 151, 152, 156, 157, 161, 164, 165, 166, 170, 173, 174, 177, 178, 181, 182, 186, 187, 191, 194, 195, 196, 200, 203, 204, 207, 208, 211, 212, 216, 217, 222, 223, 226, 227, 231, 232, 236, 237, 238, 239, 242, 243, 244, 245, 249, 250, 253, 254, 255, 256, 259, 260, 261, 265, 266, 267, 268, 269, 272, 273, 274, 275, 279, 280, 283, 284, 285, 286, 289, 290, 291, 295, 296, 297, 298, 299, 302, 303, 304, 305, 309, 310, 313, 314, 318, 319, 323, 324, 328, 329, 333, 334, 337, 338, 339, 340, 344, 345, 348, 349, 350, 351, 354, 355, 359, 360)
    * 矛盾の内容: LBドメインにおいてALT、AST、SODIUM、MCV、ASTに異常値（HIGH/LOW）が報告されているが、AEドメインに関連する有害事象の報告が見当たらない。また、LBTESTCD="ANISO", "AST"のレコードでLBSTRESC, LBSTRESNなどが欠損している。
    * 問題点の原因（推測）: データ入力時のエラー、臨床的に重要でない一過性の変動、関連する有害事象の見落とし、またはAEドメインへの記録漏れ、LBドメインのデータ欠損、Define.xmlの定義とデータ型の不整合
    * 対応策（提案）: 
        * 症例記録を再確認し、データ入力ミスがないか確認する。
        * 臨床的に意義のある異常値かどうか、治験責任医師に確認する。
        * 必要に応じて、AEドメインに有害事象を追記する。
        * データ入力者にLBドメインのデータ欠損理由を確認する。
        * Define.xmlのdataType修正、データ作成プロセス見直しを検討する。

クエリの作成:
* 患者ID: 01-703-1042
    * クエリNo.: 1
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMSTDTC, CMDTC (CMドメイン全般)
        * 医療機関への問い合わせ文面: 患者ID 01-703-1042 の併用薬データについて、CM.CMSTDTC (併用薬開始日) と CMDTC (データ収集日) の日付の整合性 Medical History 情報を参照の上、再度ご確認いただけますでしょうか。CM.CMSTDTC が CMDTC より未来、または過去の日付となっているレコードが複数件ございます。
        * 判断理由: 併用薬開始日の妥当性に関する重要な疑義のため。

    * クエリNo.: 2
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: CM.CMENDTC = null (CMドメイン row 2-14), CM.CMENDY = null (CMドメイン row 2-14)
        * 医療機関への問い合わせ文面: 患者ID 01-703-1042 の併用薬 NORVASC (CMSEQ=1, 3, 6, 9, 12, 16, 19, 22, 25, 28, 31, 34, 37, 40) の投与終了日 (CMENDTC) と投与終了時の治験薬投与日数 (CMENDY) が空欄となっています。NORVASCの投与状況（投与継続中、投与終了日など）をご確認いただけますでしょうか。
        * 判断理由: 併用薬の投与期間は重要な情報のため。

    * クエリNo.: 3
        * 臨床試験結果への影響度合い: Major
        * 変数名と値: LB.LBTESTCD="ALT", LB.LBORRES="135" (SCREENING 1)
        * 医療機関への問い合わせ文面: 患者ID 01-703-1042 のスクリーニング1回目 (VISITNUM=1) のALT (アラニンアミノトランスフェラーゼ) の検査値が135 U/Lと基準範囲上限を大きく超えています。データ入力値に誤りがないか、医療機関にて Medical History 
## Task3: Protocol Deviation Review Results
患者ID: 01-703-1042
    逸脱No.: 1
        臨床試験結果への影響度合い: Critical
        変数名と値: QS.QSTESTCD=ACTOT, QS.QSSTRESN=9, VISIT=WEEK 24
        逸脱内容: WEEK 24のMMSEスコアが9点であり、プロトコルで規定された選択基準（MMSEスコア 10-23）を満たしていません。選択基準を満たさないデータは、臨床試験の主要評価項目に影響を与える可能性があります。
        プロトコル該当箇所: 3.4.2.1. Inclusion Criteria [3]
        判断理由: MMSEスコアがプロトコルで定められた選択基準からの逸脱。主要評価項目への影響が懸念されるため、Criticalと判断しました。

    逸脱No.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=NORVASC, CM.CMCLAS=CARDIOVASCULAR SYSTEM
        逸脱内容: 併用薬NORVASC（AMLODIPINE）はカルシウムチャンネルブロッカーであり、プロトコルで併用が禁止されている可能性があります。禁止薬の併用は、治験結果に影響を与える可能性があります。
        プロトコル該当箇所: 3.8. Concomitant Therapy, 3.4.2.2. Exclusion Criteria [31c]
        判断理由: プロトコルで併用が禁止されている可能性のある薬剤が併用されている。治験結果に影響を与える可能性があるため、Majorと判断しました。

    逸脱No.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: LB.LBTESTCD=ALT, LBORRES=135, LBORNRLO=6, LBORNRHI=43, LBNRIND=HIGH, VISIT=SCREENING 1
                 LB.LBTESTCD=AST, LBORRES=145, LBORNRLO=11, LBORNRHI=36, LBNRIND=HIGH, VISIT=SCREENING 1
        逸脱内容: スクリーニング検査においてALT値 (135 U/L) およびAST値 (145 U/L) が基準範囲上限を超過しています。プロトコルで規定された選択除外基準 [27b] に抵触する可能性があります。
        プロトコル該当箇所: 3.4.2.2. Exclusion Criteria [27b] Laboratory test values exceeding the Lilly Reference Range III
        判断理由: スクリーニング時の臨床検査値異常であり、プロトコルの選択除外基準に関わる可能性があります。治験薬投与開始前に判明しているため、臨床試験結果への影響はMinorと判断しました。

    逸脱No.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC=2009, CM.CMENDTC=null (ビタミンC, ビタミンE)
        逸脱内容: ビタミンC、ビタミンEのCMSTDTC（併用薬開始日）が2009年となっており、試験期間（2013年）と矛盾しています。データ入力時の誤りの可能性があります。
        プロトコル該当箇所: プロトコルには併用薬の開始日に関する明確な規定はない。
        判断理由: CMドメインの併用薬開始日が試験期間と矛盾しており、データの信頼性に疑義が生じる可能性があります。データ修正の必要性を考慮し、Minorと判断しました。

    逸脱No.: 5
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMENDTC = null (薬剤名: NORVASC)
        逸脱内容: 併用薬NORVASCのCMENDTC（併用薬終了日）がNull (未記入) です。データの完全性の観点から逸脱の疑いがあります。
        プロトコル該当箇所: プロトコルには併用薬の終了日に関する明確な規定はないが、データ収集全般に関するセクションを参照。
        判断理由: データマネジメントの観点から、併用薬の終了日が不明であることはデータの信頼性を損なう可能性があります。データ修正の必要性を考慮し、Minorと判断しました。

    クエリNo.: 1
        臨床試験結果への影響度合い: Critical
        変数名と値: QS.QSTESTCD=ACTOT, QS.QSSTRESN=9, VISIT=WEEK 24
        医療機関への問い合わせ文面: 患者ID 01-703-1042 のWEEK 24のMMSEスコアが9点と、選択基準から逸脱しているデータが報告されています。データ入力に誤りがないか、医療機関にて再度確認をお願いします。もしデータ入力に誤りがなくMMSEスコアが9点であった場合、プロトコル逸脱となるため、治験責任医師の見解を伺いたいと存じます。MMSEスコアが選択基準を下回った要因について、医学的な見解と合わせてご回答ください。
        判断理由: MMSEスコアが選択基準範囲外である疑義について、データの正確性と医学的解釈を確認する必要があるため。

    クエリNo.: 2
        臨床試験結果への影響度合い: Major
        変数名と値: CM.CMTRT=NORVASC, CM.CMCLAS=CARDIOVASCULAR SYSTEM
        医療機関への問い合わせ文面: 患者ID 01-703-1042 の併用薬NORVASC (AMLODIPINE) の使用について確認させてください。NORVASCは、プロトコルで併用が禁止されているカルシウムチャンネルブロッカーに該当する可能性があります。NORVASCが併用禁止薬に該当するかどうか、医療機関の見解を伺います。該当する場合、本併用はプロトコル逸脱となるため、NORVASC使用の医学的な理由と、治験薬への影響についてご回答ください。
        判断理由: 併用薬NORVASCがプロトコルで禁止されている薬剤に該当する疑義について、医療機関に確認し、併用状況の医学的妥当性と治験薬への影響を評価する必要があるため。

    クエリNo.: 3
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMSTDTC=2009 (ビタミンC, ビタミンE)
        医療機関への問い合わせ文面: 患者ID 01-703-1042 の併用薬（ビタミンC、ビタミンE）の開始日について、CMSTDTCに2009年と記録されていますが、データ入力に誤りはないでしょうか。記録に誤りがある場合は、正しい開始日をご教示ください。
        判断理由: 併用薬開始日の記録が試験期間と矛盾しているデータ入力エラーの疑いがあるため、医療機関にデータ確認を依頼し、データの質を向上させるため。

    クエリNo.: 4
        臨床試験結果への影響度合い: Minor
        変数名と値: CM.CMENDTC=null (NORVASC)
        医療機関への問い合わせ文面: 患者ID 01-703-1042 の併用薬（NORVASC）の終了日について、CMENDTCが未記入となっています。NORVASCは投与終了していますでしょうか。投与が終了している場合は、終了日をご教示ください。投与が継続している場合は、終了日不明のままで問題ありません。
        判断理由: 併用薬終了日が未記入であることについて、データの欠損がないか確認し、データ品質を向上させるため。

