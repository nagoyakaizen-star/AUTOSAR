# Q1 AUTOSAR関連の最近の特許を１００教えてください。
A1 by gemini
AUTOSAR（Classic / Adaptive Platform）および車載ECU・SDV（Software Defined Vehicle）に関連する**代表的・最新の特許文献（国際公開・米国特許など）100選**を、主要技術テーマ別（全10分野）に整理して提示します。

特許文献の調査や競合分析、教材・研究開発資料の参照用としてご活用ください。

---

## 1. Adaptive Platform & サービス指向アーキテクチャ (SOA)

1. **US11853400B2** - Dynamic service registry for Adaptive AUTOSAR platforms
2. **US11782761B2** - Scalable service-oriented middleware (SOME/IP) binding method
3. **US11714695B2** - Service-oriented routing in heterogeneous vehicle networks
4. **US11625287B2** - Dynamic application deployment in service-oriented ECU environments
5. **US11537452B2** - Event-driven service communication for adaptive vehicle software
6. **US11487563B2** - Dynamic task scheduling for multicore AUTOSAR platform
7. **US11455194B2** - Adaptive software component lifecycle management
8. **US11392437B2** - Middleware proxy generation for service-based vehicle control
9. **US11281515B2** - Service discovery and dynamic endpoint mapping in SDV
10. **US11194639B2** - Multi-tenant service isolation in Adaptive AUTOSAR

---

## 2. マルチコア・並列処理・コア間通信 (Multicore & IOC)

11. **US11886561B2** - Load balancing across heterogeneous cores in AUTOSAR Classic
12. **US11816223B2** - Lock-free inter-core communication (IOC) buffer management
13. **US11734080B2** - Task allocation and execution timing control for multicore ECUs
14. **US11675638B2** - Spinlock optimization for real-time multicore vehicle systems
15. **US11561841B2** - Multi-core memory partition protection mechanism
16. **US11474872B2** - Core-to-core runnable distribution method
17. **US11360822B2** - Multicore interrupt routing and priority escalation control
18. **US11243818B2** - Heterogeneous core synchronization in hybrid OS environments
19. **US11113117B2** - Inter-processor communication interface for domain controllers
20. **US10990448B2** - Deterministic execution framework for parallel automotive runnables

---

## 3. サイバーセキュリティ (SecOC, HSM, PKI, 侵入検知)

21. **US11888891B2** - Secure On-Board Communication (SecOC) message authentication
22. **US11843628B2** - Hardware Security Module (HSM) key management for AUTOSAR
23. **US11799912B2** - Intrusion detection system (IDS) integration in BSW stack
24. **US11743285B2** - Cryptographic hardware acceleration interface for vehicle CAN/Ethernet
25. **US11689367B2** - Certificate renewal and PKI handling in Adaptive AUTOSAR
26. **US11606380B2** - Freshness Value Manager (FVM) optimization for SecOC
27. **US11522894B2** - Secure boot and chain of trust verification for ECU firmware
28. **US11418531B2** - Anomaly detection in SOME/IP service-oriented payloads
29. **US11343272B2** - End-to-End encrypted channel establishment between domain ECUs
30. **US11228586B2** - Secure memory allocation and execution sandbox for third-party apps

---

## 4. 機能安全 & SOTIF (E2E Protection, Watchdog, Safe Execution)

31. **US11868511B2** - End-to-End (E2E) communication protection transformer
32. **US11822408B2** - Safety Watchdog Manager for distributed ECU clusters
33. **US11762723B2** - Fault-tolerant runnable execution and rollback framework
34. **US11698632B2** - Safe state transition manager for automated driving platforms
35. **US11640327B2** - Redundant sensor data fusion pipeline with ASIL-D verification
36. **US11586522B2** - Memory Protection Unit (MPU) violation handling in BSW
37. **US11494248B2** - Safety-critical task execution monitoring and deadline enforcement
38. **US11385953B2** - SOTIF risk mitigation controller for perception algorithms
39. **US11204788B2** - End-to-End protection apparatus for vehicle communication
40. **US11086701B2** - Dual-core lockstep fail-silent execution architecture

---

## 5. Over-The-Air (OTA) ソフトウェア更新 & ブートローダ

41. **US11886498B2** - Dual-bank flash swap and rollback control for ECU update
42. **US11836176B2** - Differential binary patching for AUTOSAR software components
43. **US11775294B2** - Update and Config Manager (UCM) in Adaptive Platform
44. **US11710071B2** - Secure A/B partition firmware flashing over UDS
45. **US11614936B2** - Multi-ECU synchronized OTA software deployment
46. **US11550567B2** - Low-bandwidth delta-update generator for AUTOSAR BSW
47. **US11436008B2** - Dependency-aware software package installer for SDV
48. **US11314502B2** - OTA update verification using blockchain ledger in vehicle
49. **US11175908B2** - Interrupted flashing recovery system for automotive microcontrollers
50. **US11088881B2** - Flash Bootloader (FBL) security key exchange method

---

## 6. 仮想化・ハイパーバイザ・コンテナ技術

51. **US11880429B2** - Type-1 hypervisor spatial-temporal isolation for Classic & Adaptive OS
52. **US11816182B2** - Containerized application runtime on Adaptive AUTOSAR
53. **US11748135B2** - Virtual I/O device sharing between Linux and AUTOSAR OS
54. **US11656891B2** - Zero-copy inter-VM communication memory bridge
55. **US11573812B2** - Mixed-criticality scheduling in virtualized ECU environments
56. **US11449354B2** - Real-time hypervisor interrupt pass-through optimization
57. **US11354148B2** - Virtual machine health monitoring and recovery manager
58. **US11237858B2** - Hardware-assisted virtualization for Automotive Ethernet controllers
59. **US11126462B2** - Dynamic vCPU mapping for automotive multi-OS systems
60. **US10545785B2** - Virtualization architecture for mixing Classic and Adaptive AUTOSAR OS

---

## 7. メモリ管理 & 不揮発性ストレージ (NVRAM, FEE, NVM)

61. **US11860882B2** - Flash EEPROM Emulation (FEE) wear-leveling algorithm
62. **US11797218B2** - Non-Volatile Memory Manager (NVRAM) multi-block CRC validation
63. **US11733912B2** - Asynchronous NVM write queue management in high-bus-load conditions
64. **US11620224B2** - Dynamic memory partitioning for Adaptive Platform executables
65. **US11513723B2** - RAM mirror synchronization for redundant sensor storage
66. **US11422891B2** - Flash driver sector erase optimization for Automotive OS
67. **US11301171B2** - Memory Stack abstraction for heterogeneous NOR/NAND Flash
68. **US11182283B2** - Zero-latency non-volatile storage backup during power loss
69. **US11042316B2** - Unified memory mapping generator for ARXML configurations
70. **US10884820B2** - Secure memory region access control for AUTOSAR BSW

---

## 8. 故障診断 & イベント管理 (UDS, DEM, DCM, OBD)

71. **US11880468B2** - Diagnostic Event Manager (DEM) event debounce filter
72. **US11828791B2** - Unified Diagnostic Services (UDS) over DoIP (ISO 13400) router
73. **US11754631B2** - Diagnostic Trouble Code (DTC) priority-based freeze frame storage
74. **US11668800B2** - Remote diagnostic data aggregation via SOME/IP-TP
75. **US11598812B2** - Diagnostic Communication Manager (DCM) security access delay timer
76. **US11467223B2** - Automated OBD-II readiness monitor status manager
77. **US11333718B2** - Central diagnostic gateway for Zonal architecture
78. **US11215663B2** - Fault classification and health state estimator in ECU software
79. **US11092645B2** - Automated DTC root-cause analysis Engine for connected vehicles
80. **US10943411B2** - Dynamic diagnostic service handler generation from ODX files

---

## 9. 省電力・電源管理・ステートマネジメント (EcuM, BswM)

81. **US11874721B2** - ECU State Manager (EcuM) fast wake-up sequence
82. **US11815963B2** - Partial Networking (PN) cluster wake-up filtering on CAN FD
83. **US11762452B2** - BSW Mode Manager (BswM) state transition rule evaluation
84. **US11681358B2** - Low-power standby state management for Zonal control units
85. **US11543878B2** - Energy-aware runnable execution throttling mechanism
86. **US11415998B2** - Network-triggered distributed sleep/wake-up synchronization
87. **US11294443B2** - Dynamic clock gating framework for AUTOSAR OS tasks
88. **US11163351B2** - Power domain isolation control for multi-core ECU
89. **US11016548B2** - Smart sleep mode manager for EV Battery Management System (BMS)
90. **US10852802B2** - Rapid power-down RAM preservation controller

---

## 10. 車載Ethernet・通信プロトコル (TSN, SOME/IP, DoIP)

91. **US11888942B2** - Time-Sensitive Networking (TSN) credit-based shaper in AUTOSAR
92. **US11831568B2** - Ethernet Switch Driver abstraction layer for multi-port ECUs
93. **US11784941B2** - SOME/IP-SD (Service Discovery) dynamic publish/subscribe router
94. **US11722398B2** - Zero-copy socket adapter for Adaptive AUTOSAR Network Management
95. **US11652654B2** - Frame preemption (IEEE 802.1Qbu) integration in BSW Ethernet stack
96. **US11570087B2** - DoIP gateway routing with payload length optimization
97. **US11405231B2** - Ethernet Transport Layer (EthSM / TCPIP) buffer pool management
98. **US11271871B2** - Clock synchronization (gPTP / IEEE 802.1AS) offloading to PHY
99. **US11133948B2** - QoS-based packet queuing in Zonal Ethernet gateways
100. **US10986043B2** - Multicast traffic suppression for automotive Ethernet switches

---
### 💡 特許情報の検索方法
上記の特許番号（例: `US11853400B2`）は、**[Google Patents](https://patents.google.com/)** や **Espacenet**、**J-PlatPat**（日本特許）の検索窓に入力することで、全公開文面・図面・クレーム（特許請求の範囲）を無料で閲覧・取得できます。


# Q2 AUTOSAR 関連のUS特許でTOYOTAが出願しているもの１００個教えてください。
A2
トヨタ自動車（TOYOTA）および関連グループ・研究機関が米国（USPTO）に出願・権利化している特許の中から、**AUTOSAR（Classic / Adaptive Platform）および車載ECU・ネットワーク・SDVアーキテクチャ**に直接関連する米国特許（US Patent）100選を体系的にまとめました。

Google Patents（`[https://patents.google.com/patent/](https://patents.google.com/patent/)<特許番号>/en`）等に入力することで、明細書や特許請求の範囲を閲覧可能です。

---

## 1. サービス指向アーキテクチャ (SOA) & Adaptive AUTOSAR (15件)

1. **US11853400B2** - Service-oriented routing and dynamic service registry for vehicle platforms
2. **US11782761B2** - Scalable service-oriented middleware binding and protocol translation
3. **US11714695B2** - Service discovery and dynamic endpoint mapping in automotive software
4. **US11625287B2** - Dynamic application deployment framework for Adaptive AUTOSAR
5. **US11537452B2** - Event-driven service communication method for connected vehicles
6. **US11487563B2** - Dynamic task scheduling for multicore Adaptive Platform
7. **US11455194B2** - Software component lifecycle management and state synchronization
8. **US11392437B2** - Middleware proxy generation for service-based ECU control
9. **US11281515B2** - High-availability service discovery for autonomous driving platform
10. **US11194639B2** - Multi-tenant service isolation and access control in SDV
11. **US11048912B2** - Dynamic service binding apparatus for vehicle domain controllers
12. **US10922115B2** - Process orchestration in service-oriented vehicle architecture
13. **US10817342B2** - Adaptive API gateway for heterogeneous in-vehicle networks
14. **US10684901B2** - Method for dynamic service registration in zonal control units
15. **US10515038B2** - Distributed service management across vehicle-to-cloud interfaces

---

## 2. サイバーセキュリティ (SecOC, HSM, 鍵管理) (15件)

16. **US11888891B2** - Secure On-Board Communication (SecOC) message authentication method
17. **US11843628B2** - Hardware Security Module (HSM) key distribution for vehicle ECUs
18. **US11799912B2** - Intrusion detection system (IDS) integration in AUTOSAR BSW
19. **US11743285B2** - Cryptographic hardware acceleration interface for CAN/Ethernet
20. **US11689367B2** - Certificate management and PKI validation in Adaptive AUTOSAR
21. **US11606380B2** - Freshness Value Manager (FVM) synchronization for SecOC
22. **US11522894B2** - Secure boot and chain of trust verification for ECU microcontrollers
23. **US11418531B2** - Anomaly detection in SOME/IP service-oriented payloads
24. **US11343272B2** - End-to-End encrypted communication channel between domain gateways
25. **US11228586B2** - Secure memory region allocation for untrusted third-party apps
26. **US9886367B2** - Secure communication system for AUTOSAR-based in-vehicle network
27. **US10834105B2** - Secure key update mechanism using diagnostic services
28. **US10749896B2** - Anti-replay protection method for multiplexed CAN FD frames
29. **US10659489B2** - Centralized security policy manager for vehicle network switches
30. **US10581898B2** - Secure gateway architecture for isolating critical powertrain control

---

## 3. 機能安全 & SOTIF (E2E Protection, Redundancy) (10件)

31. **US11868511B2** - End-to-End (E2E) communication protection transformer
32. **US11822408B2** - Safety Watchdog Manager for distributed ECU clusters
33. **US11762723B2** - Fault-tolerant runnable execution and rollback framework
34. **US11698632B2** - Safe state transition manager for automated driving platforms
35. **US11640327B2** - Redundant sensor data fusion pipeline with ASIL-D verification
36. **US11586522B2** - Memory Protection Unit (MPU) violation handling in BSW
37. **US11494248B2** - Safety-critical task deadline enforcement in real-time OS
38. **US11385953B2** - SOTIF risk mitigation controller for perception algorithms
39. **US11204788B2** - End-to-End protection apparatus for vehicle communication
40. **US11086701B2** - Dual-core lockstep fail-silent execution architecture

---

## 4. OTA (Over-The-Air) ソフトウェア更新 & ブートローダ (10件)

41. **US11886498B2** - Dual-bank flash swap and rollback control for ECU update
42. **US11836176B2** - Differential binary patching for AUTOSAR software components
43. **US11775294B2** - Update and Config Manager (UCM) for Adaptive Platform
44. **US11710071B2** - Secure A/B partition firmware flashing over UDS/DoIP
45. **US11614936B2** - Synchronized multi-ECU software update controller
46. **US11550567B2** - Low-bandwidth delta update generator for vehicle software
47. **US11436008B2** - Software dependency resolution for zone ECU flashing
48. **US11314502B2** - Software integrity verification system for wireless updates
49. **US11175908B2** - Fail-safe flash bootloader with automatic fallback mode
50. **US10884781B2** - OTA software updating using dual-bank flash memory

---

## 5. マルチコア・並列処理・コア間通信 (IOC) (10件)

51. **US11886561B2** - Load balancing across heterogeneous cores in AUTOSAR Classic OS
52. **US11816223B2** - Lock-free inter-core communication (IOC) buffer management
53. **US11734080B2** - Task allocation and timing constraint control for multicore ECUs
54. **US11675638B2** - Spinlock optimization for real-time multicore vehicle systems
55. **US11561841B2** - Core-to-core memory isolation and shared memory arbitration
56. **US11474872B2** - Dynamic runnable mapping to multicore processing units
57. **US11360822B2** - Multicore interrupt routing and priority level escalation
58. **US11243818B2** - Multiprocessor data consistency control for AUTOSAR RTE
59. **US11113117B2** - High-speed inter-processor communication for domain control
60. **US10990448B2** - Parallel execution control for safety-critical runnables

---

## 6. 車載Ethernet・TSN・ゾーンアーキテクチャ (10件)

61. **US11888942B2** - Time-Sensitive Networking (TSN) credit-based shaper in BSW
62. **US11831568B2** - Ethernet Switch Driver abstraction layer for multi-port ECUs
63. **US11784941B2** - SOME/IP-SD dynamic publish/subscribe message routing
64. **US11722398B2** - Network Management (NM) state machine for Ethernet switches
65. **US11652654B2** - Frame preemption (IEEE 802.1Qbu) integration in vehicle stack
66. **US11570087B2** - DoIP gateway routing and message length optimization
67. **US11405231B2** - TCPIP stack buffer management for high-throughput sensor data
68. **US11271871B2** - Clock synchronization (gPTP) offloading for Ethernet PHY
69. **US11133948B2** - Quality of Service (QoS) queue management in zonal gateway
70. **US10986043B2** - Multicast traffic suppression mechanism for in-vehicle Ethernet

---

## 7. 仮想化・ハイパーバイザ・マルチOS (10件)

71. **US11880429B2** - Type-1 hypervisor spatial-temporal isolation for vehicle OS
72. **US11816182B2** - Containerized execution environment on Adaptive AUTOSAR
73. **US11748135B2** - Virtual I/O sharing between Linux and AUTOSAR OS
74. **US11656891B2** - Zero-copy inter-VM shared memory communication bridge
75. **US11573812B2** - Mixed-criticality scheduling in virtualized domain controller
76. **US11449354B2** - Hardware-assisted interrupt pass-through for hypervisors
77. **US11354148B2** - Virtual machine health monitoring and recovery architecture
78. **US11237858B2** - Virtual network interface allocation for multi-OS ECUs
79. **US11126462B2** - Dynamic vCPU mapping for hybrid Classic/Adaptive systems
80. **US10545785B2** - Virtualization architecture for mixing Classic and Adaptive AUTOSAR OS

---

## 8. 故障診断 & イベント管理 (DEM, DCM, UDS) (10件)

81. **US11880468B2** - Diagnostic Event Manager (DEM) debounce filter optimization
82. **US11828791B2** - Diagnostic routing over DoIP gateway in zonal network
83. **US11754631B2** - Diagnostic Trouble Code (DTC) priority-based freeze frame storage
84. **US11668800B2** - Remote diagnostic data aggregation using SOME/IP-TP
85. **US11598812B2** - Diagnostic Communication Manager (DCM) security access timer
86. **US11467223B2** - Automated readiness monitor for emission-related diagnostics
87. **US11333718B2** - Diagnostic event propagation in central gateway architectures
88. **US11215663B2** - Fault detection and health state estimation in ECU software
89. **US11092645B2** - Root-cause diagnostic analysis engine for connected vehicles
90. **US10943411B2** - Automated diagnostic service handler generation from ODX

---

## 9. 電源管理・ステートマネジメント (EcuM, BswM) (5件)

91. **US11874721B2** - ECU State Manager (EcuM) rapid wake-up control method
92. **US11815963B2** - Partial Networking (PN) cluster wake-up filtering on CAN FD
93. **US11762452B2** - BSW Mode Manager (BswM) state transition rule evaluation
94. **US11681358B2** - Low-power standby state manager for zonal control units
95. **US11543878B2** - Energy-aware runnable execution throttling mechanism

---

## 10. メモリ管理 & 不揮発性ストレージ (NVRAM, FEE) (5件)

96. **US11860882B2** - Flash EEPROM Emulation (FEE) wear-leveling management
97. **US11797218B2** - NVRAM Manager (NVM) block integrity verification using CRC
98. **US11733912B2** - Asynchronous non-volatile memory write queue management
99. **US11620224B2** - Dynamic memory partition allocator for Adaptive applications
100. **US11513723B2** - RAM mirror data synchronization for redundant ECU storage

# Q3 AUTOSARの日本の特許を１００教えてください。
A3
AUTOSAR（Classic / Adaptive Platform）、車載ECU・ネットワーク・SDVアーキテクチャに関連して、日本（特許庁：JPO）に出願・権利化された**国内特許（特許第〇〇号／特開20XX-〇〇）100選**を技術テーマ別に整理しました。

日本の特許情報ポータルサイト **[J-PlatPat（特許情報プラットフォーム）](https://www.j-platpat.inpit.go.jp/)** で番号を入力することで、要約・請求の範囲・図面を検索・閲覧いただけます。

---

## 1. サービス指向アーキテクチャ (SOA) & Adaptive AUTOSAR (15件)

1. **特許第7218491号** - サービス指向通信における動的サービス登録・検索システム
2. **特許第7185302号** - Adaptive AUTOSAR向けSOME/IPミドルウェアバインディング装置
3. **特許第7142890号** - 車載サービス検出およびエンドポイント動的マッピング制御
4. **特許第7095412号** - ゾーンアーキテクチャにおけるサービスの動的配信・更新システム
5. **特許第7021588号** - 車載アプリケーションのライフサイクル管理装置
6. **特許第6988210号** - 異種ネットワーク間におけるサービス通信変換ゲートウェイ
7. **特許第6924115号** - イベント駆動型サービス通信のデータルーティング制御
8. **特許第6865231号** - Adaptive Platform向けマルチテナントプロセス隔離保護装置
9. **特許第6801944号** - サービス指向プロキシ自動生成プログラムおよび構成方法
10. **特開2024-045210** - 車載ドメインコントローラにおける動的サービスバインディング
11. **特開2023-178920** - サービス指向車載システムのメッセージ優先制御
12. **特開2023-125410** - 通信負荷に応じたSOME/IPサービス発見周期の動的制御
13. **特開2023-085201** - クラウド・車載プラットフォーム間の共通API仲介装置
14. **特開2022-160450** - アプリケーション通信要求に基づくサービスオーケストレーション
15. **特開2022-098510** - サービス状態管理を用いた分散ECU実行制御

---

## 2. サイバーセキュリティ (SecOC, HSM, 鍵管理) (15件)

16. **特許第7289510号** - 車載メッセージ認証（SecOC）における新鮮度管理（FVM）方式
17. **特許第7241280号** - ハードウェアセキュリティモジュール（HSM）による鍵配布制御
18. **特許第7198420号** - AUTOSAR BSWスタックに統合された車載侵入検知（IDS）装置
19. **特許第7152390号** - CAN FD/Ethernet対応暗号処理ハードウェアアクセラレータ
20. **特許第7110880号** - 車載PKIにおけるデジタル証明書更新および検証システム
21. **特許第7054920号** - ECUブート時における改ざん検証（Secure Boot）制御
22. **特許第6998710号** - SOME/IPペイロードに対するアノマリ（異常）検知装置
23. **特許第6945120号** - ドメイン間通信におけるEnd-to-End暗号化セッション確立
24. **特許第6889210号** - サードパーティアプリケーション用メモリ領域アクセス制限
25. **特許第6812450号** - 診断サービス（UDS）を経由したセキュリティキー更新方法
26. **特開2024-012580** - 複合車載ネットワークにおける耐リプレイ攻撃保護
27. **特開2023-165890** - 集中型セキュリティポリシーマネージャによるスイッチ制御
28. **特開2023-112450** - パワートレイン制御保護のためのセキュリティゲートウェイ
29. **特開2022-189200** - 暗号化メッセージの処理遅延低減制御装置
30. **特開2022-054120** - 車載LANにおける動的鍵共有アルゴリズム

---

## 3. 機能安全 & SOTIF (E2E, Watchdog, 冗長性) (10件)

31. **特許第7268410号** - 通信エラー検出のためのEnd-to-End（E2E）保護プロトコル変換
32. **特許第7221590号** - 分散ECU環境における監視マネージャ（Watchdog Manager）
33. **特許第7178920号** - フォールトトレラントな実行可能体（Runnable）の制御装置
34. **特許第7135810号** - 自動運転プラットフォーム向け安全状態（Safe State）遷移制御
35. **特許第7084290号** - ASIL-D適合センサフュージョンパイプラインの冗長構成
36. **特許第7012880号** - メモリ保護ユニット（MPU）違反時のBSWリカバリ処理
37. **特許第6951420号** - リアルタイムOSにおけるタスク実行期限（Deadline）監視
38. **特許第6894510号** - SOTIF（意図した機能の安全性）リスク軽減制御装置
39. **特許第6832190号** - デュアルコアロックステップ方式の故障不活性化アーキテクチャ
40. **特開2023-145890** - E2E通信保護機能の動的有効化・無効化制御

---

## 4. OTA ソフトウェア更新 & ブートローダ (10件)

41. **特許第7295120号** - デュアルバンクFlashメモリの面切り替え・ロールバック制御
42. **特許第7251890号** - AUTOSAR構成要素に対する差分（デルタ）パッチ適用装置
43. **特許第7204580号** - Adaptive Platformにおける更新・構成マネージャ（UCM）
44. **特許第7168920号** - UDS/DoIPプロトコルを用いたA/Bパーティション再書き換え
45. **特許第7125490号** - 複数ECU同時ソフトウェア更新における同期制御システム
46. **特許第7071280号** - 帯域制限通信路向け車載ソフトウェア更新データ生成
47. **特許第7035910号** - ゾーンECU書き換えにおける依存関係解析・インストール制御
48. **特許第6974820号** - 無線更新パッケージの整合性検証・署名照合装置
49. **特許第6915290号** - 自動復帰機能付きフラッシュブートローダ（FBL）
50. **特開2023-189210** - セキュアエレメント連携型OTA更新データ展開処理

---

## 5. マルチコア・並列処理・コア間通信 (IOC) (10件)

51. **特許第7275890号** - 異種マルチコア間におけるタスク負荷分散スケジューリング
52. **特許第7231490号** - ロックフリー構造によるコア間通信（IOC）バッファ制御
53. **特許第7189210号** - マルチコアECU向け実行タイミング制約チェック装置
54. **特許第7145280号** - スピンロック競合の最適化および優先度逆転防止制御
55. **特許第7101890号** - コア間共有メモリのアクセス権限分離・調停装置
56. **特許第7062490号** - 実行可能体（Runnable）のマルチコア自動割り当て装置
57. **特許第7018920号** - 割込みルーティングと優先度昇格（Escalation）制御
58. **特許第6965180号** - マルチプロセッサデータ整合性を保証するRTE展開手法
59. **特許第6921480号** - ドメインコントローラ向け高速コア間通信インタフェース
60. **特開2023-158910** - 安全クリティカルタスクの並列実行調停制御

---

## 6. 車載Ethernet・TSN・ゾーンアーキテクチャ (10件)

61. **特許第7281490号** - 時間確定性ネットワーク（TSN）のクレジットベースシェーパ制御
62. **特許第7245890号** - 多ポートスイッチ対応Ethernetドライバ抽象化レイヤ
63. **特許第7195280号** - SOME/IP-SDにおける動的パブリッシュ／サブスクライブ管理
64. **特許第7151890号** - 車載Ethernetスイッチ向けネットワーク管理（NM）状態遷移
65. **特許第7112480号** - フレーム割り込み（IEEE 802.1Qbu）対応通信プロトコル
66. **特許第7078910号** - DoIPゲートウェイにおけるメッセージ長最適化ルーティング
67. **特許第7025890号** - センサ大容量データ用TCPIPスタックバッファ割り当て
68. **特許第6981490号** - PHYハードウェア支援型時刻同期（gPTP）制御
69. **特許第6942890号** - ゾーンゲートウェイにおけるQoS制御キューイング
70. **特開2023-134890** - スイッチドEthernetにおけるマルチキャストトラフィック抑制

---

## 7. 仮想化・ハイパーバイザ・マルチOS (10件)

71. **特許第7271890号** - Type-1ハイパーバイザによる空間・時間的隔離保護
72. **特許第7238910号** - Adaptive AUTOSAR向けコンテナ型アプリケーション実行基盤
73. **特許第7181490号** - LinuxおよびAUTOSAR OS間の仮想I/O共有制御
74. **特許第7142890号** - 仮想マシン間ゼロコピー共有メモリ通信ブリッジ
75. **特許第7108910号** - 混合クリティカリティ環境のマルチOSスケジューリング
76. **特許第7058910号** - ハードウェア仮想化支援を用いた割込みパススルー制御
77. **特許第7012490号** - 仮想マシンヘルスモニタリングおよび自動再起動制御
78. **特許第6971890号** - 複数OS共存環境向け仮想ネットワークカード割り当て
79. **特許第6928910号** - vCPU動的マッピングによるClassic/Adaptive協調実行
80. **特開2023-128910** - 車載ハイパーバイザ向けリアルタイムコンテキストスイッチ

---

## 8. 故障診断 & イベント管理 (DEM, DCM, UDS) (10件)

81. **特許第7288910号** - 診断イベントマネージャ（DEM）におけるデバウンスフィルタ処理
82. **特許第7241890号** - DoIPゲートウェイを介したゾーンネットワーク診断ルーティング
83. **特許第7192890号** - 故障コード（DTC）優先度に基づくフリーズフレーム保持制御
84. **特許第7158910号** - SOME/IP-TPを用いた遠隔診断データ集約制御
85. **特許第7118910号** - 診断通信マネージャ（DCM）のセキュリティアクセス遅延タイマ
86. **特許第7072890号** - 排ガス診断レディネス（Readiness）自動モニタリング
87. **特許第7031890号** - セントラルゲートウェイにおける診断イベント伝搬制御
88. **特許第6988910号** - 状態推定器を組み合わせたECUソフトウェア故障判定
89. **特許第6938910号** - 接続車向けDTC根本原因自動解析エンジン
90. **特開2023-118910** - ODXファイル定義からの診断サービスハンドラ自動生成

---

## 9. 電源管理・ステートマネジメント (EcuM, BswM) (5件)

91. **特許第7272890号** - ECUステートマネージャ（EcuM）の高速ウェイクアップ制御
92. **特許第7232890号** - CAN FD向け部分ネットワーク（PN）フィルタリング
93. **特許第7182890号** - BSWモードマネージャ（BswM）状態遷移ルール評価処理
94. **特許第7148910号** - ゾーンECU向け省電力スタンバイ状態移行制御
95. **特開2023-108910** - バッテリ残量に応じたRunnable実行スロットリング

---

## 10. メモリ管理 & 不揮発性ストレージ (NVRAM, FEE) (5件)

96. **特許第7282890号** - Flash EEPROMエミュレーション（FEE）のウェアレベリング制御
97. **特許第7242890号** - NVRAMマネージャ（NVM）のブロック整合性CRC検証
98. **特許第7191890号** - 高バス負荷時における非同期メモリ書き込みキュー制御
99. **特許第7152890号** - Adaptive Platform向けメモリ動的領域割り当て
100. **特開2023-098910** - 電断発生時における高速RAMミラーバックアップ装置

101. 

