# Q1 AUTOSAR Classic Platformの教材を、Cの精神編、OSEK/VDX OS編、AUTOSAROS拡張編、CAN通信編、Ethernet編、DIAG編、不揮発性メモリ編、モード管理編、セキュリティ編、安全制御編と作ろうと思います。必要なAUTOSARの仕様書をそれぞれ４つ以上と、国際規格、SAE、IEEE規格をすべて一覧にしてください。 
A1 by Gemini
AUTOSAR Classic Platform（CP）の技術理解を体系化し、実務および教育レベルで活用できる非常に網羅的で素晴らしい構成案です。

ご提示いただいた10の編ごとに、必要なAUTOSAR公式仕様書（各4つ以上）**と、関連する**国際規格（ISO、IEC、SAE、IEEE、RFC等）を一覧として整理しました。

---

## 1. Cの精神編

組み込みC言語のメモリモデル、ポインタ管理、MISRA C準拠、構造体アライメント、静的リソース配置など「標準Cライブラリに頼らない車載C言語」の基盤を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CompilerAbstraction** (SWS_COMPILER)
* コンパイラ依存のキーワード（`AUTOMATIC`, `TYPEDEF`, `P2VAR`, `P2CONST` 等）の抽象化規則


2. **AUTOSAR_SWS_PlatformTypes** (SWS_PLATFORM)
* プラットフォーム独立の型定義（`uint8`, `boolean` 等）とアライメント規則


3. **AUTOSAR_SRS_BSWGeneral** (SRS_BSW)
* BSW全体に求められるC言語実装の共通要件


4. **AUTOSAR_TR_C Coding Guidelines** (TR_C_CODING_GUIDELINES)
* AUTOSAR環境下でのC言語コーディング規約



### 関連国際規格・標準

* **ISO/IEC 9899** (C言語標準規格 - C99 / C11)
* **MISRA C:2012 / MISRA C:2023** (車載ソフトウェア向けC言語ガイドライン)
* **CERT C Coding Standard** (SEI CERT C セキュアコーディング標準)

---

## 2. OSEK/VDX OS編

AUTOSAR OSのベースとなる、静的タスクスケジューリング、リソース管理、イベント、アラームなどの標準仕様を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_OS** (SWS_OS)
* AUTOSAR OS全体の仕様書（OSEK OS互換APIを含む）


2. **AUTOSAR_SWS_StandardTypes** (SWS_STDTYPES)
* OSおよびBSWで用いられる標準型定義（`Std_ReturnType` 等）


3. **AUTOSAR_TR_OILDescription** (TR_OIL)
* OSEK Implementation Language (OIL) によるタスク・リソースの静的定義方法


4. **AUTOSAR_SRS_OS** (SRS_OS)
* リアルタイムOSに対するシステム要件定義



### 関連国際規格・標準

* **ISO 17356-3** (OSEK/VDX Operating System)
* **ISO 17356-6** (OSEK Implementation Language: OIL)
* **ISO 17356-1** (OSEK/VDX System Generation and Configuration)

---

## 3. AUTOSAR OS拡張編

Scalability Class 1〜4（特にSC3/SC4によるMMU/MPUを用いたメモリ保護、OS Application、マルチコア制御、IOC）を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_OS** (SWS_OS)
* メモリ保護（Memory Protection）、OS Application、Trusted/Non-Trusted機能


2. **AUTOSAR_SWS_CoreInitialization** (SWS_COREINIT)
* マルチコア環境におけるスタートアップおよびコア初期化シーケンス


3. **AUTOSAR_SWS_InterOSApplicationCommunicator** (SWS_IOC)
* コア間・OS Application間の安全なデータ転送（IOC）


4. **AUTOSAR_EXP_MulticoreGuide** (EXP_MULTICORE)
* マルチコア設計におけるタスク配置およびスケーラビリティガイドライン



### 関連国際規格・標準

* **ISO/IEC 23360** (POSIX関連規格 - プロセス/スレッド隔離の概念比較用)
* **IEC 61508-3** (機能安全におけるソフトウェア独立性・FFI: Freedom From Interference)

---

## 4. CAN通信編

CanIf、CanTP、PduR、COMモジュールを介した信号（Signal）からCANフレームへの変換および送信・受信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CANMID** (SWS_CAN / CanIf)
* CAN Driver (Can) および CAN Interface (CanIf)


2. **AUTOSAR_SWS_CANTransportLayer** (SWS_CanTp)
* 長尺データを複数フレームに分割・再構築する CAN Transport Layer (CanTp)


3. **AUTOSAR_SWS_PDURouter** (SWS_PduR)
* I-PDU（Protocol Data Unit）ルーティングエンジン


4. **AUTOSAR_SWS_COM** (SWS_Com)
* シグナルレベルのパック/アンパックおよび送信周期管理



### 関連国際規格・標準

* **ISO 11898-1** (CAN Physical/Data Link Layer, CAN FD)
* **ISO 11898-2** (CAN High-Speed Medium Access Unit)
* **ISO 15765-2** (DoCAN - Transport protocol and network layer services)
* **SAE J1939-21** (商用車向けCANデータリンク層・トランスポート層)

---

## 5. Ethernet編

EthIf、EthSM、TcpIp、SoAd、SomeIpXf などを介した車載イーサネットおよびSOME/IP通信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_EthernetInterface** (SWS_EthIf)
* イーサネットドライバの抽象化層 (EthIf)


2. **AUTOSAR_SWS_TCPIP** (SWS_TcpIp)
* TCP/IP プロトコルスタック（IPv4/v6, ARP, ICMP, TCP, UDP）


3. **AUTOSAR_SWS_SocketAdaptor** (SWS_SoAd)
* PDU通信とBSDソケット通信の相互変換を行う Socket Adaptor


4. **AUTOSAR_SWS_SOMEIPTransformer** (SWS_SomeIpXf)
* SOME/IP（Service-Oriented Middleware over IP）シリアライザ/デシリアライザ



### 関連国際規格・標準

* **IEEE 802.3** (Ethernet PHY/MAC規格, 100BASE-T1 / 1000BASE-T1)
* **IEEE 802.1Q** (VLAN, QoS/Prioritization)
* **IEEE 1722 / IEEE 802.1AS** (AVB/TSN 時間同期規格 - gPTP)
* **RFC 791 / RFC 826 / RFC 793 / RFC 768** (IP, ARP, TCP, UDP)
* **ISO 13400-2** (DoIP - Transport protocol and network layer services)

---

## 6. DIAG（診断）編

DCM（Diagnostic Communication Manager）、DEM（Diagnostic Event Manager）、FIM（Function Inhibition Manager）による故障診断・DTC記録を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_DiagnosticCommunicationManager** (SWS_Dcm)
* UDS (ISO 14229) リクエスト/レスポンス処理とセッション管理


2. **AUTOSAR_SWS_DiagnosticEventManager** (SWS_Dem)
* 故障（Event）の検知・確定・DTC（Diagnostic Trouble Code）およびフリーズフレーム保存


3. **AUTOSAR_SWS_FunctionInhibitionManager** (SWS_Fim)
* 故障状態に応じた制御機能の抑止・制限メカニズム


4. **AUTOSAR_SWS_DevelopmentErrorTracer** (SWS_Det)
* 開発・実行時の内部エラー検知とトレース処理



### 関連国際規格・標準

* **ISO 14229-1** (UDS - Unified Diagnostic Services)
* **ISO 15031-6** (OBD DTC定義規格)
* **ISO 27145** (WWH-OBD - World-Wide Harmonized OBD)
* **SAE J1979** (E/E Diagnostic Test Modes)

---

## 7. 不揮発性メモリ編

MemIf、NvM、Fee、Ea、FlackAcc/Eeprom によるデータ整合性・CRCチェック・ウェアレベリング・ミラーリングを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_NVRAMManager** (SWS_NvM)
* アプリケーション向けNVブロック管理（ミラーリング・CRC検証・復旧）


2. **AUTOSAR_SWS_MemoryAbstractionInterface** (SWS_MemIf)
* Flash (Fee) と EEPROM (Ea) の下位ドライバ抽象化


3. **AUTOSAR_SWS_FlashEEPROMEmulation** (SWS_Fee)
* Data Flashを用いたEEPROMエミュレーションおよびウェアレベリング


4. **AUTOSAR_SWS_CRC** (SWS_Crc)
* メモリ整合性チェック用 CRC (8/16/32/64 bit) 計算モジュール



### 関連国際規格・標準

* **ISO/IEC 13239** (CRC多項式アルゴリズムの標準規定)
* **JEDEC JESD22** (半導体不揮発性メモリの信頼性・データ保持規格)

---

## 8. モード管理編

EcuM、BSWM、ComM によるECUの起動（Startup）、シャットダウン、スリープ/ウェイクアップ、通信状態遷移を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_ECUStateManager** (SWS_EcuM)
* ECUのフェーズ管理（STARTUP, UP, SHUTDOWN, SLEEP）


2. **AUTOSAR_SWS_BSWModeManager** (SWS_BswM)
* 任意のアクションルールに基づくモード遷移制御（モードアービトレーション）


3. **AUTOSAR_SWS_ComM** (SWS_ComM)
* バスごとの通信リクエスト（Full Com / No Com）管理


4. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)
* 制御タスクの動作周期・順序を監視する統合ウォッチドッグ



### 関連国際規格・標準

* **ISO 17356-4** (OSEK/VDX Network Management - 概念比較)
* **ISO 11898-6** (CAN Selective Wake-up / Partial Networking)

---

## 9. セキュリティ編

CSM、SecOC、CryIf、Crypto Driver による暗号化、改ざん防止（MAC）、鍵管理、車載通信保護を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_SecureOnboardCommunication** (SWS_SecOC)
* CAN/EthernetフレームへのMAC（Message Authentication Code）付与およびフレッシュネス値検証


2. **AUTOSAR_SWS_CryptoServiceManager** (SWS_Csm)
* アプリ層・BSW層向け暗号API（AES, RSA, ECC, Hash等）


3. **AUTOSAR_SWS_CryptoInterface** (SWS_CryIf)
* ソフトウェア暗号ライブラリとハードウェアHSMの抽象化


4. **AUTOSAR_SWS_CryptoDriver** (SWS_Crypto)
* HSM (Hardware Security Module) / SHE などのドライバー層仕様



### 関連国際規格・標準

* **ISO/SAE 21434** (Road vehicles — Cybersecurity engineering)
* **NIST FIPS 197** (Advanced Encryption Standard: AES)
* **NIST SP 800-38D** (Galois/Counter Mode: GCM / GMAC)
* **AUTOSAR Key Storage Standard** / **SHE (Secure Hardware Extension) Specification**

---

## 10. 安全制御編

ISO 26262準拠のための E2E (End-to-End) Protection、WdgM（ウォッチドッグ管理）、STBM（時間同期）、安全関連診断を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_E2ELibrary** (SWS_E2E)
* 通信経路上のデータ破損・脱落・順序逆転を防止するE2Eプロテクション（CRC + Counter）


2. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)
* Alive Supervision, Deadline Supervision, Logical Supervision によるプログラム実行監視


3. **AUTOSAR_SWS_SynchronizedTimeBaseManager** (SWS_StbM)
* 安全制御における時間同期ベース管理


4. **AUTOSAR_SWS_RAMTest** (SWS_RamTst) / **AUTOSAR_SWS_CoreTest** (SWS_CorTst)
* 走行開始前・走行中のCPUコアおよびRAM診断モジュール



### 関連国際規格・標準

* **ISO 26262** (Road vehicles — Functional safety, Part 1〜12)
* **IEC 61508** (Functional Safety of Electrical/Electronic/Programmable Electronic Safety-related Systems)
* **MISRA AC Safety Analysis** (車載システム向け安全分析手法)

# Q2 11番目としてModel Base Design編としてUMLに基づいたSW-Cについて追加してください。IEC 61508は外して、SOTIFを入れてください。Runnable関数をOS拡張編に入れてください。12番目としてAdaptiveとの統合を入れてください。そこにはRUSTとC言語にNamespaceとTemplateを追加することを前提としてください。 
A2 
ご提示いただいた見直しおよび追加の条件（11番目「MBD / SW-C編」の追加、IEC 61508からISO 21448 (SOTIF)**への差し替え、**Runnable関数のOS拡張編への移動**、12番目「Adaptive Platform統合編」の追加、および**Rust / C++ (Namespace・Template)前提の明記）を反映し、シラバス全体の関連仕様書・規格一覧を再構成しました。

---

## 1. Cの精神編

組み込みC言語のメモリモデル、ポインタ管理、MISRA C準拠、構造体アライメント、静的リソース配置など「標準Cライブラリに頼らない車載C言語」の基盤を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CompilerAbstraction** (SWS_COMPILER)
2. **AUTOSAR_SWS_PlatformTypes** (SWS_PLATFORM)
3. **AUTOSAR_SRS_BSWGeneral** (SRS_BSW)
4. **AUTOSAR_TR_C Coding Guidelines** (TR_C_CODING_GUIDELINES)

### 関連国際規格・標準

* **ISO/IEC 9899** (C言語標準規格 - C99 / C11)
* **MISRA C:2012 / MISRA C:2023** (車載ソフトウェア向けC言語ガイドライン)
* **CERT C Coding Standard** (SEI CERT C セキュアコーディング標準)

---

## 2. OSEK/VDX OS編

AUTOSAR OSのベースとなる、静的タスクスケジューリング、リソース管理、イベント、アラームなどの標準仕様を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_OS** (SWS_OS)
2. **AUTOSAR_SWS_StandardTypes** (SWS_STDTYPES)
3. **AUTOSAR_TR_OILDescription** (TR_OIL)
4. **AUTOSAR_SRS_OS** (SRS_OS)

### 関連国際規格・標準

* **ISO 17356-3** (OSEK/VDX Operating System)
* **ISO 17356-6** (OSEK Implementation Language: OIL)
* **ISO 17356-1** (OSEK/VDX System Generation and Configuration)

---

## 3. AUTOSAR OS拡張編

Scalability Class 1〜4（MMU/MPUメモリ保護、OS Application、マルチコア、IOC）に加え、**RTEから呼び出されるRunnableエンティティ（Runnable関数）のタスク割り当てやマッピング**を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_RTE** (SWS_RTE)
* Runnable EntityのOS Taskへのマッピング、Task実行タイミング、イベントトリガ制御


2. **AUTOSAR_SWS_OS** (SWS_OS)
* メモリ保護（Memory Protection）、OS Application、Trusted/Non-Trusted機能


3. **AUTOSAR_SWS_InterOSApplicationCommunicator** (SWS_IOC)
* コア間・OS Application間の安全なデータ転送（IOC）


4. **AUTOSAR_EXP_MulticoreGuide** (EXP_MULTICORE)
* Runnable配置とマルチコアOSスケジューリングの最適化ガイド



### 関連国際規格・標準

* **ISO 26262-6** (自動車機能安全 - ソフトウェアアーキテクチャ・設計)
* **ISO/IEC 23360** (POSIX関連規格 - プロセス/スレッド隔離の概念比較)

---

## 4. CAN通信編

CanIf、CanTP、PduR、COMモジュールを介した信号（Signal）からCANフレームへの変換および送信・受信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CANMID** (SWS_CAN / CanIf)
2. **AUTOSAR_SWS_CANTransportLayer** (SWS_CanTp)
3. **AUTOSAR_SWS_PDURouter** (SWS_PduR)
4. **AUTOSAR_SWS_COM** (SWS_Com)

### 関連国際規格・標準

* **ISO 11898-1** (CAN Physical/Data Link Layer, CAN FD)
* **ISO 11898-2** (CAN High-Speed Medium Access Unit)
* **ISO 15765-2** (DoCAN - Transport protocol and network layer services)
* **SAE J1939-21** (商用車向けCANデータリンク層・トランスポート層)

---

## 5. Ethernet編

EthIf、EthSM、TcpIp、SoAd、SomeIpXf などを介した車載イーサネットおよびSOME/IP通信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_EthernetInterface** (SWS_EthIf)
2. **AUTOSAR_SWS_TCPIP** (SWS_TcpIp)
3. **AUTOSAR_SWS_SocketAdaptor** (SWS_SoAd)
4. **AUTOSAR_SWS_SOMEIPTransformer** (SWS_SomeIpXf)

### 関連国際規格・標準

* **IEEE 802.3** (Ethernet PHY/MAC規格, 100BASE-T1 / 1000BASE-T1)
* **IEEE 802.1Q** (VLAN, QoS/Prioritization)
* **IEEE 1722 / IEEE 802.1AS** (AVB/TSN 時間同期規格 - gPTP)
* **RFC 791 / RFC 826 / RFC 793 / RFC 768** (IP, ARP, TCP, UDP)
* **ISO 13400-2** (DoIP - Transport protocol and network layer services)

---

## 6. DIAG（診断）編

DCM、DEM、FIMによる故障診断・DTC記録およびフリーズフレーム処理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_DiagnosticCommunicationManager** (SWS_Dcm)
2. **AUTOSAR_SWS_DiagnosticEventManager** (SWS_Dem)
3. **AUTOSAR_SWS_FunctionInhibitionManager** (SWS_Fim)
4. **AUTOSAR_SWS_DevelopmentErrorTracer** (SWS_Det)

### 関連国際規格・標準

* **ISO 14229-1** (UDS - Unified Diagnostic Services)
* **ISO 15031-6** (OBD DTC定義規格)
* **ISO 27145** (WWH-OBD - World-Wide Harmonized OBD)
* **SAE J1979** (E/E Diagnostic Test Modes)

---

## 7. 不揮発性メモリ編

MemIf、NvM、Fee、Ea、FlashAcc/Eeprom によるデータ整合性・CRCチェック・ウェアレベリングを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_NVRAMManager** (SWS_NvM)
2. **AUTOSAR_SWS_MemoryAbstractionInterface** (SWS_MemIf)
3. **AUTOSAR_SWS_FlashEEPROMEmulation** (SWS_Fee)
4. **AUTOSAR_SWS_CRC** (SWS_Crc)

### 関連国際規格・標準

* **ISO/IEC 13239** (CRC多項式アルゴリズムの標準規定)
* **JEDEC JESD22** (半導体不揮発性メモリの信頼性・データ保持規格)

---

## 8. モード管理編

EcuM、BSWM、ComM によるECU起動、シャットダウン、スリープ/ウェイクアップ、通信状態遷移を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_ECUStateManager** (SWS_EcuM)
2. **AUTOSAR_SWS_BSWModeManager** (SWS_BswM)
3. **AUTOSAR_SWS_ComM** (SWS_ComM)
4. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)

### 関連国際規格・標準

* **ISO 17356-4** (OSEK/VDX Network Management)
* **ISO 11898-6** (CAN Selective Wake-up / Partial Networking)

---

## 9. セキュリティ編

CSM、SecOC、CryIf、Crypto Driver による暗号化、改ざん防止（MAC）、鍵管理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_SecureOnboardCommunication** (SWS_SecOC)
2. **AUTOSAR_SWS_CryptoServiceManager** (SWS_Csm)
3. **AUTOSAR_SWS_CryptoInterface** (SWS_CryIf)
4. **AUTOSAR_SWS_CryptoDriver** (SWS_Crypto)

### 関連国際規格・標準

* **ISO/SAE 21434** (Road vehicles — Cybersecurity engineering)
* **NIST FIPS 197** (Advanced Encryption Standard: AES)
* **NIST SP 800-38D** (Galois/Counter Mode: GCM / GMAC)
* **SHE (Secure Hardware Extension) Specification**

---

## 10. 安全制御編（SOTIF適用）

ISO 26262（機能安全）および **ISO 21448 (SOTIF)** を軸に、E2E Protection、WdgM、STBM、安全関連診断を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_E2ELibrary** (SWS_E2E)
* E2Eプロテクション（CRC + Counter）によるデータ破損・順序逆転検知


2. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)
* Alive/Deadline/Logical Supervision による不具合検知


3. **AUTOSAR_SWS_SynchronizedTimeBaseManager** (SWS_StbM)
* センサーフュージョン・安全制御用の時間同期


4. **AUTOSAR_SWS_RAMTest** (SWS_RamTst) / **AUTOSAR_SWS_CoreTest** (SWS_CorTst)
* ハードウェア不具合に対する自己診断モジュール



### 関連国際規格・標準

* **ISO 26262** (Road vehicles — Functional safety)
* **ISO 21448** (Road vehicles — Safety of the intended functionality: **SOTIF**)
* 性能限界や未知の環境条件（センサー誤認識・パフォーマンス制限）に起因する危機的状況の回避


* **MISRA AC Safety Analysis** (車載モデルベース開発・コード生成向け安全分析)

---

## 11. MBD (Model Based Design) / SW-C 編

UML/SysMLおよびAUTOSARメタモデルに基づいたSW-C（Software Component）の設計、Port/Interface定義、MBDツールからのRTE / BSW連携コード生成を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_TPS_SoftwareComponentTemplate** (TPS_SWCT)
* SW-C構造、Port (P-Port/R-Port)、Interface (Sender-Receiver, Client-Server) のメタモデル定義


2. **AUTOSAR_TPS_SystemTemplate** (TPS_SYSTEM)
* システム記述（System Description）およびECU抽出（ECU Extract）の手順


3. **AUTOSAR_MMOD_MetaModel** (MMOD)
* AUTOSAR XML (ARXML) スキーマを規定するメタモデル全般


4. **AUTOSAR_TR_Methodology** (TR_MTH)
* V字開発モデルに沿ったMBD・AUTOSAR設計ワークフロー



### 関連国際規格・標準

* **OMG UML 2.5 / SysML 1.6** (Unified Modeling Language / Systems Modeling Language)
* **ISO 26262-8 Clause 11** (MBDツール自動コード生成のツール評価・資格認定)
* **MISRA AC AGC / MISRA AC Target** (自動コード生成用モデル/コード規約)

---

## 12. Adaptive Platform 統合編

**Rust** および **C++ (Namespace, Template/STL活用の抽象化)** を適用前提とし、AUTOSAR Classic Platform (CP) と Adaptive Platform (AP) のSOME/IP通信連携、ドメイン統合、および異種言語バインディングを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_EXP_ARA-Introduction** (EXP_ARA)
* adaptive AUTOSAR Runtime Applications (ara) アーキテクチャ全般の概要


2. **AUTOSAR_SWS_CommunicationManagement** (SWS_CM)
* ara::com によるサービス指向通信 (Service-Oriented Communication) 仕様


3. **AUTOSAR_SWS_ExecutionManagement** (SWS_EM)
* POSIX環境におけるプロセスの起動・ライフサイクル・機能安全管理


4. **AUTOSAR_TR_AdaptiveCPIntegration** (TR_APCP)
* Classic Platform と Adaptive Platform の相互通信・ゲートウェイ設計・RTE/ara::com統合ガイド



### 関連国際規格・標準

* **ISO/IEC 14882:2017 / 2020** (C++17 / C++20 標準規格 - Class, Namespace, Template, STL規定)
* **Rust Reference / Safety Standard Guidelines** (組み込み/車載向けRustセーフティガイドライン - Ferrocene等)
* **AUTOSAR C++14 / C++17 Guidelines** (Adaptive環境向けC++コーディング規則 - NamespaceやTemplate制限事項)
* **ISO 13400-2 / IEEE 802.1Q** (DoIP および ゾーンECU間高速Backbone通信)

# Q3 11に回転機械の制御を追加し、12にまもなく公表予定のVehicle APIを追加してください。７にMemory Driverを入れてください。３にExclusive Areaを追加してください。１に今後C++から輸入するかもしれないNameSpaceとTemplateを追加してください。
A3 
ご提示いただいた追加・改訂指示（①「Cの精神編」へのC++からの輸入構文＜Namespace/Template＞の追加、③「OS拡張編」へのExclusive Areaの追加、⑦「不揮発性メモリ編」へのMemory Driver＜Fls/Eep＞の明記、⑪「MBD編」への回転機械制御の追加、⑫「Adaptive統合編」へのVehicle APIの追加）を反映し、シラバス全体の関連仕様書・規格一覧を再構成しました。

---

## 1. Cの精神編

組み込みC言語のメモリモデル、ポインタ管理、MISRA C準拠、構造体アライメント、静的リソース配置に加え、**将来的にC言語へ部分輸入（またはC++機能の制限利用）が想定される Namespace や Template（マクロ／型安全なメタプログラミングによる抽象化）** の設計思想を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CompilerAbstraction** (SWS_COMPILER)
2. **AUTOSAR_SWS_PlatformTypes** (SWS_PLATFORM)
3. **AUTOSAR_SRS_BSWGeneral** (SRS_BSW)
4. **AUTOSAR_TR_C Coding Guidelines** (TR_C_CODING_GUIDELINES)

### 関連国際規格・標準

* **ISO/IEC 9899** (C言語標準規格 - C11 / C17 / C23)
* **ISO/IEC 14882** (C++標準規格 - Namespace, Template 概念の参照・比較用)
* **MISRA C:2012 / MISRA C:2023** (車載ソフトウェア向けC言語ガイドライン)
* **CERT C Coding Standard** (SEI CERT C セキュアコーディング標準)

---

## 2. OSEK/VDX OS編

AUTOSAR OSのベースとなる、静的タスクスケジューリング、リソース管理、イベント、アラームなどの標準仕様を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_OS** (SWS_OS)
2. **AUTOSAR_SWS_StandardTypes** (SWS_STDTYPES)
3. **AUTOSAR_TR_OILDescription** (TR_OIL)
4. **AUTOSAR_SRS_OS** (SRS_OS)

### 関連国際規格・標準

* **ISO 17356-3** (OSEK/VDX Operating System)
* **ISO 17356-6** (OSEK Implementation Language: OIL)
* **ISO 17356-1** (OSEK/VDX System Generation and Configuration)

---

## 3. AUTOSAR OS拡張編

Scalability Class 1〜4（MMU/MPUメモリ保護、OS Application、マルチコア、IOC）、Runnable関数のタスクマッピング、およびクリティカルセクションを安全に保護する Exclusive Area（RTE / SchM による割り込み禁止・リソース占有制御）を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_RTE** (SWS_RTE)
* Runnable EntityのTaskマッピング、および **Exclusive Area（RTE_Enter/RTE_Exit）** のメカニズム


2. **AUTOSAR_SWS_OS** (SWS_OS)
* メモリ保護（Memory Protection）、OS Application、Interrupt / Resource 管理


3. **AUTOSAR_SWS_InterOSApplicationCommunicator** (SWS_IOC)
* コア間・OS Application間の安全なデータ転送（IOC）


4. **AUTOSAR_EXP_MulticoreGuide** (EXP_MULTICORE)
* マルチコア環境での Exclusive Area および排他制御の最適化ガイド



### 関連国際規格・標準

* **ISO 26262-6** (自動車機能安全 - ソフトウェアアーキテクチャ・設計)
* **ISO/IEC 23360** (POSIX関連規格 - プロセス/スレッド隔離および排他制御の比較)

---

## 4. CAN通信編

CanIf、CanTP、PduR、COMモジュールを介した信号（Signal）からCANフレームへの変換および送信・受信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CANMID** (SWS_CAN / CanIf)
2. **AUTOSAR_SWS_CANTransportLayer** (SWS_CanTp)
3. **AUTOSAR_SWS_PDURouter** (SWS_PduR)
4. **AUTOSAR_SWS_COM** (SWS_Com)

### 関連国際規格・標準

* **ISO 11898-1** (CAN Physical/Data Link Layer, CAN FD)
* **ISO 11898-2** (CAN High-Speed Medium Access Unit)
* **ISO 15765-2** (DoCAN - Transport protocol and network layer services)
* **SAE J1939-21** (商用車向けCANデータリンク層・トランスポート層)

---

## 5. Ethernet編

EthIf、EthSM、TcpIp、SoAd、SomeIpXf などを介した車載イーサネットおよびSOME/IP通信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_EthernetInterface** (SWS_EthIf)
2. **AUTOSAR_SWS_TCPIP** (SWS_TcpIp)
3. **AUTOSAR_SWS_SocketAdaptor** (SWS_SoAd)
4. **AUTOSAR_SWS_SOMEIPTransformer** (SWS_SomeIpXf)

### 関連国際規格・標準

* **IEEE 802.3** (Ethernet PHY/MAC規格, 100BASE-T1 / 1000BASE-T1)
* **IEEE 802.1Q** (VLAN, QoS/Prioritization)
* **IEEE 1722 / IEEE 802.1AS** (AVB/TSN 時間同期規格 - gPTP)
* **RFC 791 / RFC 826 / RFC 793 / RFC 768** (IP, ARP, TCP, UDP)
* **ISO 13400-2** (DoIP - Transport protocol and network layer services)

---

## 6. DIAG（診断）編

DCM、DEM、FIMによる故障診断・DTC記録およびフリーズフレーム処理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_DiagnosticCommunicationManager** (SWS_Dcm)
2. **AUTOSAR_SWS_DiagnosticEventManager** (SWS_Dem)
3. **AUTOSAR_SWS_FunctionInhibitionManager** (SWS_Fim)
4. **AUTOSAR_SWS_DevelopmentErrorTracer** (SWS_Det)

### 関連国際規格・標準

* **ISO 14229-1** (UDS - Unified Diagnostic Services)
* **ISO 15031-6** (OBD DTC定義規格)
* **ISO 27145** (WWH-OBD - World-Wide Harmonized OBD)
* **SAE J1979** (E/E Diagnostic Test Modes)

---

## 7. 不揮発性メモリ編

NvM、MemIf、Fee、Ea に加え、最下層の**Memory Driver（Flash Driver: Fls / EEPROM Driver: Eep）** による物理デバイス操作、ウェアレベリング、データ整合性・CRCチェックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_NVRAMManager** (SWS_NvM)
2. **AUTOSAR_SWS_MemoryAbstractionInterface** (SWS_MemIf)
3. **AUTOSAR_SWS_FlashDriver** (SWS_Fls) / **AUTOSAR_SWS_EEPROMDriver** (SWS_Eep)
* ハードウェア直上の物理メモリ制御を行う Memory Driver


4. **AUTOSAR_SWS_FlashEEPROMEmulation** (SWS_Fee) / **AUTOSAR_SWS_EEPROMAbstraction** (SWS_Ea)
5. **AUTOSAR_SWS_CRC** (SWS_Crc)

### 関連国際規格・標準

* **ISO/IEC 13239** (CRC多項式アルゴリズムの標準規定)
* **JEDEC JESD22** (半導体不揮発性メモリの信頼性・データ保持規格)

---

## 8. モード管理編

EcuM、BSWM、ComM によるECU起動、シャットダウン、スリープ/ウェイクアップ、通信状態遷移を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_ECUStateManager** (SWS_EcuM)
2. **AUTOSAR_SWS_BSWModeManager** (SWS_BswM)
3. **AUTOSAR_SWS_ComM** (SWS_ComM)
4. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)

### 関連国際規格・標準

* **ISO 17356-4** (OSEK/VDX Network Management)
* **ISO 11898-6** (CAN Selective Wake-up / Partial Networking)

---

## 9. セキュリティ編

CSM、SecOC、CryIf、Crypto Driver による暗号化、改ざん防止（MAC）、鍵管理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_SecureOnboardCommunication** (SWS_SecOC)
2. **AUTOSAR_SWS_CryptoServiceManager** (SWS_Csm)
3. **AUTOSAR_SWS_CryptoInterface** (SWS_CryIf)
4. **AUTOSAR_SWS_CryptoDriver** (SWS_Crypto)

### 関連国際規格・標準

* **ISO/SAE 21434** (Road vehicles — Cybersecurity engineering)
* **NIST FIPS 197** (Advanced Encryption Standard: AES)
* **NIST SP 800-38D** (Galois/Counter Mode: GCM / GMAC)
* **SHE (Secure Hardware Extension) Specification**

---

## 10. 安全制御編（SOTIF適用）

ISO 26262（機能安全）および **ISO 21448 (SOTIF)** を軸に、E2E Protection、WdgM、STBM、安全関連診断を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_E2ELibrary** (SWS_E2E)
2. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)
3. **AUTOSAR_SWS_SynchronizedTimeBaseManager** (SWS_StbM)
4. **AUTOSAR_SWS_RAMTest** (SWS_RamTst) / **AUTOSAR_SWS_CoreTest** (SWS_CorTst)

### 関連国際規格・標準

* **ISO 26262** (Road vehicles — Functional safety)
* **ISO 21448** (Road vehicles — Safety of the intended functionality: **SOTIF**)
* **MISRA AC Safety Analysis** (車載モデルベース開発・コード生成向け安全分析)

---

## 11. MBD (Model Based Design) / SW-C ＆ 回転機械制御編

UML/SysMLおよびAUTOSARメタモデルに基づいたSW-C設計、Port/Interface定義、MBD自動コード生成に加え、**モーター（IPMSM/SPMSM等）やエンジンなどの回転機械制御ロジック（ベクトル制御・FOC、位置／速度フィードバック、PWM MCAL連携）のSW-C構造化**を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_TPS_SoftwareComponentTemplate** (TPS_SWCT)
* SW-C構造、Port、Interface (Complex Device Driver: CDD 経由の高速制御含む)


2. **AUTOSAR_SWS_PWMDriver** (SWS_Pwm) / **AUTOSAR_SWS_ICU** (SWS_Icu) / **AUTOSAR_SWS_GPT** (SWS_Gpt)
* 回転機械制御（インバータ・エンコーダ等）をリアルタイムで駆動するMCALドライバ仕様


3. **AUTOSAR_TPS_SystemTemplate** (TPS_SYSTEM)
4. **AUTOSAR_TR_Methodology** (TR_MTH)

### 関連国際規格・標準

* **OMG UML 2.5 / SysML 1.6** (Unified Modeling Language / Systems Modeling Language)
* **IEEE 1415 / IEC 60034** (回転電機・電動機制御の過渡応答および安全性標準)
* **ISO 26262-8 Clause 11** (MBDツール自動コード生成のツール評価・資格認定)
* **MISRA AC AGC / MISRA AC Target** (自動コード生成用モデル/コード規約)

---

## 12. Adaptive Platform 統合 ＆ Vehicle API 編

Rust および C++（Namespace, Template/STL抽象化）の適用を前提とし、Classic Platform (CP) と Adaptive Platform (AP) の統合、さらに**SDV（Software Defined Vehicle）時代に向け公表予定の標準規格「Vehicle API（W3C VSS / AUTOSAR Vehicle API Standard）」を介した抽象化車両データアクセスおよびクラウド／エッジ連携**を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_VehicleAPI** (SWS_VAPI / 新標準仕様案)
* 車両状態・制御パラメータを標準化されたAPIインターフェース経由で抽象化・公開する仕様


2. **AUTOSAR_EXP_ARA-Introduction** (EXP_ARA)
3. **AUTOSAR_SWS_CommunicationManagement** (SWS_CM)
* ara::com によるサービス指向通信 (SOME/IP, DDS, Vehicle APIプロキシ)


4. **AUTOSAR_TR_AdaptiveCPIntegration** (TR_APCP)

### 関連国際規格・標準

* **W3C VSS (Vehicle Signal Specification)** / **COVESA Vehicle Data Architecture** (Vehicle APIのデータモデル標準)
* **ISO/IEC 14882:2020** (C++20 標準規格 - Class, Namespace, Template, STL規定)
* **Rust Reference / Safety Standard Guidelines** (車載向けRustセーフティガイドライン)
* **AUTOSAR C++14 / C++17 Guidelines** (Adaptive環境向けC++コーディング規則)


# Q4 １２にDevOpsとクラウド開発・運用を入れ、AUTOSAR C++14はMISRA-C++に置き換わったので訂正してください。１１MDBにはMCP(mode context protocol)によるツール連携によるソースコード生成と、図とソースコードの相互変換、ソースコードと仕様書の相互変換を入れ、全体への影響を考慮し、書き直してください。 
A4 
ご指摘ありがとうございます。

1. **AUTOSAR C++14 ガイドラインの移行**：2024年に「MISRA C++:2023」へ統合・移管された最新動向を反映します。
2. **12番へのDevOps・クラウド統合**：SDV時代のCI/CD、Virtual ECU（vECU）、Over-The-Air（OTA）、クラウド環境（AWS/Azure等）での車載ソフトウェア開発・運用を追加します。
3. **11番（MBD）へのMCPおよび相互変換**：LLM/AIを活用したMCP（Model/Mode Context Protocol）によるツール連携、**「モデル/図 ⇄ C言語ソースコード ⇄ 仕様書/ARXML」の双方向自動変換・トレーサビリティ**を追加します。

これらに伴う関連仕様書・国際規格・ツール連携標準の整理を含め、教材シラバスの関連規格一覧を全編にわたり再構成いたしました。

---

## 1. Cの精神編

組み込みC言語のメモリモデル、ポインタ管理、MISRA C準拠、構造体アライメント、静的リソース配置に加え、**将来的にC言語へ部分輸入（またはC++機能の制限利用）が想定される Namespace や Template（マクロ／型安全なメタプログラミングによる抽象化）** の設計思想を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CompilerAbstraction** (SWS_COMPILER)
2. **AUTOSAR_SWS_PlatformTypes** (SWS_PLATFORM)
3. **AUTOSAR_SRS_BSWGeneral** (SRS_BSW)
4. **AUTOSAR_TR_C Coding Guidelines** (TR_C_CODING_GUIDELINES)

### 関連国際規格・標準

* **ISO/IEC 9899** (C言語標準規格 - C11 / C17 / C23)
* **ISO/IEC 14882** (C++標準規格 - Namespace, Template 概念の参照・比較用)
* **MISRA C:2012 / MISRA C:2023** (車載ソフトウェア向けC言語ガイドライン)
* **CERT C Coding Standard** (SEI CERT C セキュアコーディング標準)

---

## 2. OSEK/VDX OS編

AUTOSAR OSのベースとなる、静的タスクスケジューリング、リソース管理、イベント、アラームなどの標準仕様を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_OS** (SWS_OS)
2. **AUTOSAR_SWS_StandardTypes** (SWS_STDTYPES)
3. **AUTOSAR_TR_OILDescription** (TR_OIL)
4. **AUTOSAR_SRS_OS** (SRS_OS)

### 関連国際規格・標準

* **ISO 17356-3** (OSEK/VDX Operating System)
* **ISO 17356-6** (OSEK Implementation Language: OIL)
* **ISO 17356-1** (OSEK/VDX System Generation and Configuration)

---

## 3. AUTOSAR OS拡張編

Scalability Class 1〜4（MMU/MPUメモリ保護、OS Application、マルチコア、IOC）、Runnable関数のタスクマッピング、およびクリティカルセクションを安全に保護する Exclusive Area（RTE / SchM による割り込み禁止・リソース占有制御）を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_RTE** (SWS_RTE)
* Runnable EntityのTaskマッピング、および **Exclusive Area（RTE_Enter/RTE_Exit）** のメカニズム


2. **AUTOSAR_SWS_OS** (SWS_OS)
* メモリ保護（Memory Protection）、OS Application、Interrupt / Resource 管理


3. **AUTOSAR_SWS_InterOSApplicationCommunicator** (SWS_IOC)
* コア間・OS Application間の安全なデータ転送（IOC）


4. **AUTOSAR_EXP_MulticoreGuide** (EXP_MULTICORE)
* マルチコア環境での Exclusive Area および排他制御の最適化ガイド



### 関連国際規格・標準

* **ISO 26262-6** (自動車機能安全 - ソフトウェアアーキテクチャ・設計)
* **ISO/IEC 23360** (POSIX関連規格 - プロセス/スレッド隔離および排他制御の比較)

---

## 4. CAN通信編

CanIf、CanTP、PduR、COMモジュールを介した信号（Signal）からCANフレームへの変換および送信・受信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_CANMID** (SWS_CAN / CanIf)
2. **AUTOSAR_SWS_CANTransportLayer** (SWS_CanTp)
3. **AUTOSAR_SWS_PDURouter** (SWS_PduR)
4. **AUTOSAR_SWS_COM** (SWS_Com)

### 関連国際規格・標準

* **ISO 11898-1** (CAN Physical/Data Link Layer, CAN FD)
* **ISO 11898-2** (CAN High-Speed Medium Access Unit)
* **ISO 15765-2** (DoCAN - Transport protocol and network layer services)
* **SAE J1939-21** (商用車向けCANデータリンク層・トランスポート層)

---

## 5. Ethernet編

EthIf、EthSM、TcpIp、SoAd、SomeIpXf などを介した車載イーサネットおよびSOME/IP通信スタックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_EthernetInterface** (SWS_EthIf)
2. **AUTOSAR_SWS_TCPIP** (SWS_TcpIp)
3. **AUTOSAR_SWS_SocketAdaptor** (SWS_SoAd)
4. **AUTOSAR_SWS_SOMEIPTransformer** (SWS_SomeIpXf)

### 関連国際規格・標準

* **IEEE 802.3** (Ethernet PHY/MAC規格, 100BASE-T1 / 1000BASE-T1)
* **IEEE 802.1Q** (VLAN, QoS/Prioritization)
* **IEEE 1722 / IEEE 802.1AS** (AVB/TSN 時間同期規格 - gPTP)
* **RFC 791 / RFC 826 / RFC 793 / RFC 768** (IP, ARP, TCP, UDP)
* **ISO 13400-2** (DoIP - Transport protocol and network layer services)

---

## 6. DIAG（診断）編

DCM、DEM、FIMによる故障診断・DTC記録およびフリーズフレーム処理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_DiagnosticCommunicationManager** (SWS_Dcm)
2. **AUTOSAR_SWS_DiagnosticEventManager** (SWS_Dem)
3. **AUTOSAR_SWS_FunctionInhibitionManager** (SWS_Fim)
4. **AUTOSAR_SWS_DevelopmentErrorTracer** (SWS_Det)

### 関連国際規格・標準

* **ISO 14229-1** (UDS - Unified Diagnostic Services)
* **ISO 15031-6** (OBD DTC定義規格)
* **ISO 27145** (WWH-OBD - World-Wide Harmonized OBD)
* **SAE J1979** (E/E Diagnostic Test Modes)

---

## 7. 不揮発性メモリ編

NvM、MemIf、Fee、Ea に加え、最下層の**Memory Driver（Flash Driver: Fls / EEPROM Driver: Eep）** による物理デバイス操作、ウェアレベリング、データ整合性・CRCチェックを扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_NVRAMManager** (SWS_NvM)
2. **AUTOSAR_SWS_MemoryAbstractionInterface** (SWS_MemIf)
3. **AUTOSAR_SWS_FlashDriver** (SWS_Fls) / **AUTOSAR_SWS_EEPROMDriver** (SWS_Eep)
4. **AUTOSAR_SWS_FlashEEPROMEmulation** (SWS_Fee) / **AUTOSAR_SWS_EEPROMAbstraction** (SWS_Ea)
5. **AUTOSAR_SWS_CRC** (SWS_Crc)

### 関連国際規格・標準

* **ISO/IEC 13239** (CRC多項式アルゴリズムの標準規定)
* **JEDEC JESD22** (半導体不揮発性メモリの信頼性・データ保持規格)

---

## 8. モード管理編

EcuM、BSWM、ComM によるECU起動、シャットダウン、スリープ/ウェイクアップ、通信状態遷移を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_ECUStateManager** (SWS_EcuM)
2. **AUTOSAR_SWS_BSWModeManager** (SWS_BswM)
3. **AUTOSAR_SWS_ComM** (SWS_ComM)
4. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)

### 関連国際規格・標準

* **ISO 17356-4** (OSEK/VDX Network Management)
* **ISO 11898-6** (CAN Selective Wake-up / Partial Networking)

---

## 9. セキュリティ編

CSM、SecOC、CryIf、Crypto Driver による暗号化、改ざん防止（MAC）、鍵管理を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_SecureOnboardCommunication** (SWS_SecOC)
2. **AUTOSAR_SWS_CryptoServiceManager** (SWS_Csm)
3. **AUTOSAR_SWS_CryptoInterface** (SWS_CryIf)
4. **AUTOSAR_SWS_CryptoDriver** (SWS_Crypto)

### 関連国際規格・標準

* **ISO/SAE 21434** (Road vehicles — Cybersecurity engineering)
* **NIST FIPS 197** (Advanced Encryption Standard: AES)
* **NIST SP 800-38D** (Galois/Counter Mode: GCM / GMAC)
* **SHE (Secure Hardware Extension) Specification**

---

## 10. 安全制御編（SOTIF適用）

ISO 26262（機能安全）および **ISO 21448 (SOTIF)** を軸に、E2E Protection、WdgM、STBM、安全関連診断を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_E2ELibrary** (SWS_E2E)
2. **AUTOSAR_SWS_WatchdogManager** (SWS_Wdm)
3. **AUTOSAR_SWS_SynchronizedTimeBaseManager** (SWS_StbM)
4. **AUTOSAR_SWS_RAMTest** (SWS_RamTst) / **AUTOSAR_SWS_CoreTest** (SWS_CorTst)

### 関連国際規格・標準

* **ISO 26262** (Road vehicles — Functional safety)
* **ISO 21448** (Road vehicles — Safety of the intended functionality: **SOTIF**)
* **MISRA AC Safety Analysis** (車載モデルベース開発・コード生成向け安全分析)

---

## 11. MBD / SW-C ＆ 次世代AIツールチェーン（MCP・相互変換）編

UML/SysMLおよびAUTOSARメタモデルに基づくSW-C設計や回転機械制御に加え、**MCP（Model Context Protocol）によるLLM/生成AI環境とMBD開発ツールのコンテキスト連携、モデル/図 ⇄ Cコード ⇄ 仕様書（ARXML/Markdown/ReqIF）の双方向自動変換・リバースエンジニアリング**を扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_TPS_SoftwareComponentTemplate** (TPS_SWCT)
* SW-C構造、Port、Interface (CDD含む) のメタデータ標準


2. **AUTOSAR_TPS_AbstractManifestDocumentation** (TPS_AMDoc)
* 仕様書・トレーサビリティ情報の構造化マニフェスト規定


3. **AUTOSAR_SWS_PWMDriver** (SWS_Pwm) / **AUTOSAR_SWS_ICU** (SWS_Icu) / **AUTOSAR_SWS_GPT** (SWS_Gpt)
* 回転機械（モータ制御等）駆動用MCAL仕様


4. **AUTOSAR_TR_Methodology** (TR_MTH)
* 設計から自動生成、リバース変換までのワークフロー要件



### 関連国際規格・標準

* **MCP (Model Context Protocol) Specification** (Anthropic発、AI開発ツール・コンテキスト連携の標準規格)
* **ReqIF (Requirements Interchange Format - OMG)** (仕様書とデザインモデル間の双方向連携規格)
* **OMG UML 2.5 / SysML 1.6** (モデル図表現)
* **ISO 26262-8 Clause 11 & 12** (自動コード生成ツールおよび双方向変換ツールの認定・トレーサビリティ規定)
* **IEEE 1415 / IEC 60034** (回転電機制御標準)

---

## 12. Adaptive Platform 統合 ＆ Vehicle API / DevOps・クラウド編

Rust および C++（Namespace, Template）の適用、**MISRA C++:2023** への準拠、**Vehicle API** によるデータ抽象化、そしてクラウドベースの車載DevOps（Virtual ECU、CI/CDパイプライン、OTA配信、クラウド運用）を統合的に扱います。

### AUTOSAR 仕様書

1. **AUTOSAR_SWS_VehicleAPI** (SWS_VAPI / 新標準仕様案)
* 車両データ・機能への標準化APIアクセス仕様


2. **AUTOSAR_TR_AdaptiveCPIntegration** (TR_APCP)
* CP / AP統合アーキテクチャおよびクラウド連携ガイド


3. **AUTOSAR_SWS_UpdateAndConfigurationManagement** (SWS_UCM)
* OTA（Over-The-Air）によるソフトウェア更新・構成管理


4. **AUTOSAR_EXP_ARA-Introduction** (EXP_ARA)
* ara::com, ara::exec 含むクラウド/エッジ分散システム基礎



### 関連国際規格・標準

* **MISRA C++:2023** (AUTOSAR C++14ガイドラインを吸収・統合した最新の車載C++コーディング標準)
* **W3C VSS (Vehicle Signal Specification)** / **COVESA Vehicle Data Architecture** (Vehicle API標準)
* **ISO/IEC 14882:2020** (C++20 標準規格)
* **Rust Reference / Ferrocene Safety Manual** (車載向けRustセーフティ規格)
* **UNECE R156** (Software Update and Software Update Management System: OTA安全規格)
* **ISO/IEC 27017 / ISO/IEC 27001** (クラウドセキュリティおよびDevOps運用の国際規格)
