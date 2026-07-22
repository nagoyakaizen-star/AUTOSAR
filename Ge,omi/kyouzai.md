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
* 
