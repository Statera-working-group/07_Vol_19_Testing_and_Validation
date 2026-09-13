**Volume 19. Testing and Validation**

# Chapter 03. EMC Test

## 03.01. CISPR 32/25 Radiated Emission

![](images/image1.png){width="7.268055555555556in" height="7.268055555555556in"}

방사 방출 시험(Radiated Emission Testing)은 전기·전자 장비에서 의도하지 않게 발생하여 자유 공간(Free Space)을 통해 전달되는 전자기 에너지(Electromagnetic Energy)를 평가한다. 제공된 검증 체계에서 이 활동은 전자파 적합성 시험(EMC Test) 영역에 속하며, CISPR 32/25 방사 방출 시험(CISPR 32/25 Radiated Emission Testing)으로 정의된다. 이를 통해 로봇, 제어기(Controller), 컴퓨팅 플랫폼(Computing Platform), 전기 서브시스템(Electrical Subsystem)이 대표적인 운전 조건에서 과도한 전자기 방해(Electromagnetic Disturbance)를 발생시키지 않는지를 확인한다.

CISPR 32와 CISPR 25는 서로 다른 적용 관점에서 방사 전자기 방해(Radiated Electromagnetic Disturbance)를 다룬다. CISPR 32는 일반적으로 멀티미디어 및 정보기술 장비(Multimedia and Information Technology Equipment)와 관련되며, CISPR 25는 차량 및 관련 설비에 사용되는 부품과 장비를 중심으로 한다. 로봇 시스템에는 컴퓨팅 하드웨어(Computing Hardware), 이더넷 인터페이스(Ethernet Interface), 스위칭 전력 변환기(Switching Power Converter), 디스플레이(Display), 카메라(Camera), 통신 모듈(Communication Module), 모터 제어 전자장치(Motor-Control Electronics)가 포함될 수 있으므로 제품의 사용 목적과 인증 범위에 따라 두 환경의 개념이 모두 중요할 수 있다.

기본적인 목적은 주파수(Frequency)에 따른 전자기장 세기(Electromagnetic Field Strength)를 측정하고, 측정값을 해당 방출 제한값(Emission Limit)과 비교하는 것이다. 전자회로에는 빠르게 변화하는 전류와 전압이 존재하며, 이로 인해 광대역(Broadband) 또는 협대역(Narrowband)의 전자기 에너지가 발생할 수 있다. 따라서 클록 발생기(Clock Generator), 프로세서(Processor), GPU, 스위칭 레귤레이터(Switching Regulator), 모터 인버터(Motor Inverter), 통신 송수신기(Communication Transceiver), 고속 디지털 버스(High-Speed Digital Bus)는 전기적 기능이 정상적으로 동작하더라도 중요한 방사 노이즈(Radiated Noise) 발생원이 될 수 있다.

방사 방출 문제(Radiated Emission Problem)는 일반적으로 노이즈 소스(Noise Source), 결합 경로(Coupling Path), 비의도성 안테나 구조(Unintended Antenna Structure)의 세 요소로 구성된다. 노이즈 소스는 스위칭 컨버터(Switching Converter)나 고속 프로세서(High-Speed Processor)가 될 수 있으며, 결합 경로는 PCB 배선(PCB Trace), 전원 도체(Power Conductor), 접지 구조(Grounding Structure), 공통 모드 전류(Common-Mode Current)를 포함할 수 있다. 이후 하네스(Harness), 케이블(Cable), 인클로저 이음부(Enclosure Seam), 커넥터 실드(Connector Shield), 대형 도전 구조물(Conductive Structure)이 안테나처럼 동작하여 전도성 방해(Conducted Disturbance)를 전자기 방사(Electromagnetic Radiation)로 변환할 수 있다.

시험은 시험 대상 장비(Equipment Under Test, EUT)에서 발생하는 방출을 외부 무선 신호와 주변 노이즈(Ambient Noise)로부터 구별할 수 있도록 제어된 전자기 환경(Controlled Electromagnetic Environment)에서 수행한다. 적용 절차에 따라 전파 무반사실(Anechoic Chamber) 또는 반무반사실(Semi-Anechoic Chamber)을 사용하며, 교정된 수신 안테나(Calibrated Receiving Antenna), EMI 수신기(EMI Receiver), 스펙트럼 분석기(Spectrum Analyzer), 케이블(Cable), 전치 증폭기(Preamplifier) 등의 측정 장비를 함께 사용한다. 물리적 배치는 측정되는 전자기장에 큰 영향을 주므로 엄격하게 관리되어야 한다.

정식 측정 전에 시험 대상 장비(EUT)는 정의되고 재현 가능한 운전 조건(Operating Condition)을 나타내도록 구성해야 한다. 로봇의 경우 활성화된 컴퓨팅 모듈(Computing Module), 통신 네트워크(Communication Network), 센서(Sensor), DC/DC 컨버터(DC/DC Converter), 모터 드라이버(Motor Driver), 대표적인 전기 부하(Electrical Load)가 포함될 수 있다. 높은 프로세서 부하, 네트워크 트래픽(Network Traffic), 스위칭 동작(Switching Activity), 액추에이터 동작(Actuator Operation)을 발생시키는 운전 모드는 특정 시스템 활동 조합에서 최대 방출이 발생할 수 있으므로 특히 주의해야 한다.

케이블 배선(Cable Routing)은 공통 모드 전류(Common-Mode Current)가 흐를 경우 케이블 자체가 효율적인 방사 구조(Radiating Structure)로 동작할 수 있기 때문에 특히 중요하다. 전원 케이블(Power Cable), 이더넷 라인(Ethernet Line), 카메라 인터페이스(Camera Interface), 모터 상 도체(Motor Phase Conductor), 센서 케이블(Sensor Cable), 외부 입출력 연결(External I/O Connection)은 임의로 배치하지 않고 규정된 시험 구성(Test Configuration)에 따라 배치해야 한다. 실드 종단(Shield Termination), 커넥터 본딩(Connector Bonding), 케이블 길이(Cable Length), 접지(Grounding), 도전성 표면과의 간격은 측정 방출값을 크게 변화시킬 수 있으므로 문서화해야 한다.

측정 과정에서 수신 시스템(Receiving System)은 요구되는 주파수 범위(Frequency Range)를 스캔하고, 안테나는 동작 중인 장비에서 발생하는 전자기장(Electromagnetic Field)을 검출한다. 안테나 편파(Antenna Polarization), 측정 거리(Measurement Distance), 안테나 위치(Antenna Position), 장비 방향(Equipment Orientation), 검파기 설정(Detector Setting)은 적용되는 시험 방법에 따라 결정한다. 목적은 단순히 하나의 스펙트럼 파형(Spectrum Trace)을 기록하는 것이 아니라, 제어되고 반복 가능한 조건에서 가장 높은 관련 방출을 발생시키는 구성과 운전 상태를 확인하는 것이다.

초기 스캔(Initial Scan)은 상세 측정을 수행하기 전에 의심되는 주파수를 식별하는 데 유용하다. 프로세서 클록(Processor Clock), 스위칭 주파수(Switching Frequency), 통신 인터페이스(Communication Interface) 또는 이들의 고조파(Harmonic)와 연관된 피크(Peak)는 중요한 진단 정보를 제공할 수 있다. 그러나 강한 스펙트럼 성분(Spectral Line)이 반드시 물리적인 발생원을 직접 나타내는 것은 아니다. 에너지가 방사되기 전에 여러 도전 경로(Conductive Path)를 통해 전달될 수 있으므로 주파수 상관관계(Frequency Correlation)를 제어된 공학적 실험과 함께 분석해야 한다.

방출값이 제한값(Limit)을 초과하거나 근접하는 경우 즉시 차폐재(Shielding Material)를 추가하는 것보다 체계적인 발생원 분리(Source Isolation)가 효과적이다. 엔지니어는 서브시스템(Subsystem)을 선택적으로 비활성화하고, 운전 모드(Operating Mode)를 변경하거나 불필요한 인터페이스를 분리하고, 부하 또는 케이블 배치를 변경하여 스펙트럼 변화를 관찰할 수 있다. 이후 PCB, 컨버터(Converter), 커넥터(Connector), 프로세서(Processor), 케이블 인출부(Cable Exit) 주변에 근접장 프로빙(Near-Field Probing)을 적용하여 전자기 에너지가 발생하거나 더 큰 방사 구조로 결합되는 영역을 찾을 수 있다.

공통 모드 전류(Common-Mode Current)는 실제 로봇 시스템에서 매우 중요한 방사 메커니즘(Radiation Mechanism)이 될 수 있다. 우수한 전자파 적합성(EMC)을 고려하여 설계된 차동 인터페이스(Differential Interface)도 비대칭성(Asymmetry)에 의해 차동 신호 일부가 공통 모드 에너지(Common-Mode Energy)로 변환되면 상당한 방사를 발생시킬 수 있다. 불완전한 실드 종단(Shield Termination), 불균등한 귀환 경로(Return Path), 커넥터 불연속성(Connector Discontinuity), PCB 불균형(PCB Imbalance), 불량한 섀시 본딩(Chassis Bonding)은 이러한 변환을 증가시킬 수 있다. 따라서 방사 문제 해결에는 단순한 신호 진폭 감소보다 전류 귀환 경로(Current Return Path)의 제어가 중요하다.

모터 구동 시스템(Motor-Drive System)은 대전류 스위칭(High-Current Switching)이 급격한 전압 및 전류 변화를 발생시키므로 추가적인 어려움을 만든다. PWM 에지(PWM Edge), 인버터 스위칭 노드(Inverter Switching Node), 모터 상 케이블(Motor Phase Cable), 제동 회로(Braking Circuit), DC 링크 구조(DC-Link Structure)는 광대역 방해(Broadband Disturbance)를 발생시켜 섀시와 인접 배선으로 결합될 수 있다. 필터링(Filtering), 제어된 스위칭 전이(Controlled Switching Transition), 짧은 전류 루프(Current Loop), 적절한 케이블 차폐(Cable Shielding), 섀시 본딩(Chassis Bonding), 노이즈가 큰 전력 회로와 민감한 통신 배선 사이의 분리는 중요한 EMC 설계 대책이다.

고성능 컴퓨팅 플랫폼(High-Performance Computing Platform)은 다른 형태의 방출 특성을 나타낸다. CPU, GPU, 메모리 인터페이스(Memory Interface), PCIe 링크(PCIe Link), 이더넷 인터페이스(Ethernet Interface), 카메라 연결(Camera Connection), 고주파 전압 레귤레이터(High-Frequency Voltage Regulator)는 넓은 주파수 범위에서 다수의 고조파 관련 성분을 발생시킬 수 있다. 금속 인클로저(Metal Enclosure)는 이음부, 통풍구(Ventilation Opening), 케이블 관통부(Cable Penetration), 커넥터 인터페이스(Connector Interface)에서 전자기적 연속성(Electromagnetic Continuity)을 유지할 때 효과적인 차폐를 제공할 수 있다.

측정 결과는 이후의 공학적 판단과 적합성 증거(Compliance Evidence)를 지원할 수 있도록 충분한 시험 조건과 함께 기록해야 한다. 유용한 기록에는 주파수(Frequency), 측정 레벨(Measured Level), 적용 제한값(Applicable Limit), 제한값 대비 마진(Margin), 안테나 편파(Antenna Polarization), 장비 방향(Equipment Orientation), 운전 모드(Operating Mode), 케이블 구성(Cable Configuration), 검파기 유형(Detector Type), 관련 시험 설정(Test Setup) 정보가 포함된다. 물리적 배치를 회귀 시험(Regression Test)이나 인증 시험(Certification Test)에서 재현할 수 있도록 별도의 구성 기록도 유지하는 것이 바람직하다.

마진(Margin)은 단 한 번의 합격 측정이 양산 제품의 충분한 강건성(Robustness)을 보장하지 않기 때문에 중요하다. 부품 공차(Component Tolerance), 하네스 편차(Harness Variation), 소프트웨어 워크로드(Software Workload), 프로세서 사용률(Processor Utilization), 컨버터 운전점(Converter Operating Point), 접지 차이(Grounding Difference), 제조 변경(Manufacturing Change)은 방출 특성을 변화시킬 수 있다. 따라서 공학적 검증에서는 충분한 적합성 마진(Compliance Margin)을 가진 결과와 제한값 바로 아래에 위치한 결과를 구분해야 하며, 한계에 가까운 주파수는 기술적으로 합격하더라도 설계 위험(Design Risk)으로 관리해야 한다.

시정 조치(Corrective Action)는 진단 과정에서 확인된 지배적인 결합 메커니즘(Dominant Coupling Mechanism)을 대상으로 해야 한다. 가능한 대책에는 섀시 본딩(Chassis Bonding) 개선, PCB 귀환 경로(Return Path) 최적화, 공통 모드 필터링(Common-Mode Filtering), 페라이트 부품(Ferrite Component), 피드스루 필터링(Feedthrough Filtering), 차폐 케이블(Shielded Cable), 커넥터 종단(Connector Termination) 개선, 루프 면적(Loop Area) 감소, 스위칭 동작 변경, 인클로저 수정(Enclosure Modification) 등이 있다. 하나의 주파수에서 개선된 대책이 다른 주파수에서는 효과가 없거나 오히려 악영향을 줄 수도 있으므로 각 대책은 반드시 측정을 통해 검증해야 한다.

방사 방출 시험(Radiated Emission Testing)은 일회성 인증 활동으로 취급하기보다 전체 검증 프로세스(Validation Process)에 통합해야 한다. 제공된 시험 구조에서는 전도 방출 시험(Conducted Emission Test), 정전기 방전 내성 시험(ESD Immunity Test), 서지 내성 시험(Surge Immunity Test), EMC 사전 적합성 시험(EMC Pre-Compliance Test)과 함께 배치되어 있으며, 이는 전자기 검증이 방출(Emission)과 내성(Immunity)을 모두 포함해야 함을 의미한다. 초기 사전 적합성 측정(Pre-Compliance Measurement)을 수행하면 PCB 레이아웃, 하네스 배선, 접지, 필터링, 인클로저 설계를 효율적으로 수정할 수 있는 단계에서 주요 문제를 발견할 수 있다.

복잡한 로봇에서 EMC 성능(EMC Performance)은 전력 분배(Power Distribution), 컴퓨팅(Computing), 통신(Communication), 센서(Sensor), 액추에이터(Actuator), 접지(Grounding), 차폐(Shielding), 기계 패키징(Mechanical Packaging)의 상호작용으로 형성되는 시스템 수준 특성(System-Level Property)이다. 개별적으로 우수한 성능을 보이는 서브시스템도 통합 이후 새로운 케이블 길이, 귀환 경로, 인클로저 연결, 스위칭 부하가 추가되면서 다른 특성을 나타낼 수 있다. 따라서 방사 방출 검증(Radiated Emission Validation)은 단순한 규격 적합성 측정을 넘어 전체 로봇 전기 아키텍처(Robotic Electrical Architecture)의 전자기적 건전성(Electromagnetic Integrity)을 평가하는 실질적인 방법이다.

## 03.02. IEC 61000 Conducted Emission

![](images/image2.png){width="7.268055555555556in" height="7.268055555555556in"}

전도 방출 시험(Conducted Emission Testing)은 전자 장비에서 발생한 원하지 않는 무선주파수 전기 에너지(Radio-Frequency Electrical Energy)가 주로 자유 공간을 통해 전파되는 것이 아니라 전원, 신호, 통신 또는 기타 도전성 인터페이스(Conductive Interface)를 통해 외부로 전달되는 현상을 평가한다. 제공된 검증 구조에서 이 활동은 CISPR 32/25 방사 방출 시험(Radiated Emission Testing)에 이어 IEC 61000 전도 방출 시험(Conducted Emission Testing)으로 정의되며, 로봇 전기 시스템의 전체 전자파 적합성 검증(EMC Verification)에서 중요한 부분을 구성한다.

IEC 61000 규격군(IEC 61000 Family)은 전자파 환경(Electromagnetic Environment), 방출 및 내성 현상(Emission and Immunity Phenomena), 측정 기법(Measurement Technique), 시험 방법(Test Method)을 포함하는 광범위한 전자파 적합성(Electromagnetic Compatibility) 체계를 제공한다. 전도 방출 평가는 장비에 연결된 전기 도체(Electrical Conductor)를 따라 전달되는 방해 신호를 대상으로 한다. 로봇에서는 AC 또는 DC 전원 입력, DC/DC 컨버터 연결, 외부 통신 인터페이스, 충전 회로, 센서 배선, 분산 전자 모듈을 연결하는 케이블 등이 주요 전달 경로가 될 수 있다.

전도성 전자기 노이즈(Conducted Electromagnetic Noise)는 빠르게 변화하는 전압이나 전류가 연결된 배선으로 결합되는 고주파 성분(High-Frequency Component)을 생성할 때 발생한다. 스위칭 전원 공급장치(Switching Power Supply), DC/DC 컨버터(DC/DC Converter), 모터 인버터(Motor Inverter), 프로세서(Processor), 통신 송수신기(Communication Transceiver), 배터리 충전기(Battery Charger), PWM 제어 부하(PWM-Controlled Load)가 대표적인 발생원이다. 회로의 기본 동작 주파수가 비교적 낮더라도 빠른 스위칭 에지(Switching Edge)는 기본 주파수를 훨씬 넘어서는 고조파 에너지(Harmonic Energy)를 포함하여 외부 케이블로 전달될 수 있다.

전도성 방해(Conducted Disturbance)를 분석하는 유용한 공학적 모델은 이를 차동 모드(Differential Mode)와 공통 모드(Common Mode) 성분으로 구분하는 것이다. 차동 모드 노이즈(Differential-Mode Noise)는 양극과 음극 전원선처럼 의도된 전기회로를 구성하는 두 도체 사이를 흐른다. 공통 모드 노이즈(Common-Mode Noise)는 여러 도체에서 동일한 방향으로 흐르며 섀시(Chassis), 보호 접지(Protective Earth), 기생 커패시턴스(Parasitic Capacitance), 실드(Shield) 또는 주변 구조물을 통해 귀환한다. 두 메커니즘은 필요한 필터링과 접지 대책이 크게 다를 수 있으므로 정확한 구분이 중요하다.

차동 모드 방해(Differential-Mode Disturbance)는 전원에서 인출되는 스위칭 전류(Switching Current)와 관련되는 경우가 많다. DC/DC 컨버터나 인버터(Inverter)는 주기적인 전류 펄스(Current Pulse)를 발생시켜 배터리 또는 상위 전력 분배 네트워크(Power Distribution Network) 방향으로 전달할 수 있다. 입력 커패시터(Input Capacitor), 차동 인덕터(Differential Inductor), 적절한 전원 플레인 설계(Power-Plane Design), 제어된 스위칭 루프(Switching Loop)를 통해 이러한 현상을 감소시킬 수 있다. 과도한 배선 인덕턴스(Wiring Inductance)나 부족한 로컬 에너지 저장(Local Energy Storage)은 외부 전원 인터페이스까지 전달되는 방해를 증가시킬 수 있다.

공통 모드 방해(Common-Mode Disturbance)는 빠르게 스위칭되는 노드와 섀시 또는 주변 도전성 구조물 사이의 용량성 결합(Capacitive Coupling)에서 발생하는 경우가 많다. 모터 인버터 스위칭 노드, 변압기 권선(Transformer Winding), 스위칭 레귤레이터(Switching Regulator), 프로세서 어셈블리(Processor Assembly), 방열판(Heat Sink)은 기생 커패시턴스를 통해 고주파 전류를 결합시킬 수 있다. 이 전류는 전원 케이블, 실드 또는 통신 배선을 따라 흐를 수 있으며, 공통 모드 초크(Common-Mode Choke), 섀시 본딩(Chassis Bonding), 필터 커패시터(Filter Capacitor), 차폐(Shielding), 귀환 경로 최적화(Return-Path Optimization) 등을 통해 저감할 수 있다.

전도 방출 시험에는 방해 전압(Disturbance Voltage)이나 방해 전류(Disturbance Current)를 반복 가능하게 측정할 수 있도록 제어된 전기적 측정 구성(Measurement Configuration)이 필요하다. 장비와 적용 시험 방법에 따라 안정화 네트워크(Stabilization Network), 결합 네트워크(Coupling Network), 전류 프로브(Current Probe), EMI 수신기(EMI Receiver), 스펙트럼 분석기(Spectrum Analyzer) 등을 사용할 수 있다. 측정 네트워크는 정의된 임피던스(Defined Impedance)를 제공하고 외부 전원 공급원의 불규칙한 특성으로부터 측정계를 분리하여 서로 다른 시험실과 제품 구성 사이의 비교 가능성을 향상시킨다.

시험 대상 장비(Equipment Under Test, EUT)는 측정 중 대표적인 운전 조건(Representative Operating Condition)에서 동작해야 한다. 로봇에서는 컴퓨팅 플랫폼(Computing Platform), 모터 제어기(Motor Controller), 센서(Sensor), 이더넷 통신(Ethernet Communication), DC/DC 컨버터, 냉각 시스템(Cooling System), 보조 전자장치(Auxiliary Electronics)를 동시에 활성화할 필요가 있다. 프로세서 집약적 연산, 네트워크 트래픽, 충전, 액추에이터 동작, 고전류 전력 변환처럼 스위칭 활동이나 전기 부하를 최대화하는 운전 상태를 고려해야 한다.

전력 아키텍처(Power Architecture)는 전도 EMC 성능(Conducted EMC Performance)에 큰 영향을 미친다. 로봇은 일반적으로 배터리(Battery), 전력 분배 장치(Power Distribution Unit), 보호 장치(Protection Device), 여러 DC/DC 컨버터, 모터 드라이버, 컴퓨팅 모듈, 센서, 통신 장비가 상호 연결된 전원 및 접지 네트워크를 공유한다. 하나의 서브시스템에서 발생한 노이즈가 이러한 네트워크를 통해 전파되어 다른 서브시스템에서 나타날 수 있으므로 전도 방출 시험은 개별 부품 시험에서는 확인하기 어려운 시스템 수준 결합(System-Level Coupling)을 발견하는 데에도 도움이 된다.

측정에서는 일반적으로 지정된 주파수 범위(Frequency Range)를 스캔하고 적용 절차에 적합한 검파 특성(Detector Characteristic)을 사용하여 방해 레벨(Disturbance Level)을 기록한다. 엔지니어는 측정값을 규정된 제한값(Limit)과 비교하고 마진(Margin)이 작아지는 주파수를 식별한다. 반복적으로 나타나는 피크는 컨버터 스위칭 주파수, PWM 동작, 프로세서 클록, 통신 활동 또는 고조파와 연관될 수 있다. 광대역 증가(Broadband Increase)는 빠른 스위칭 전이, 불안정한 접지 또는 여러 노이즈 발생원의 중첩을 나타낼 수 있다.

진단 시험(Diagnostic Testing)은 과도한 방해의 물리적 발생원과 전달 경로를 모두 확인해야 한다. 특정 모듈을 일시적으로 비활성화하거나 컨버터 부하를 변경하고, 모터 동작을 중지하거나 네트워크 활동을 줄이며, 불필요한 인터페이스를 분리하면 특정 스펙트럼 특성에 영향을 미치는 서브시스템을 확인할 수 있다. 전류 프로브(Current Probe)와 근접장 프로브(Near-Field Probe)는 케이블, PCB 영역, 커넥터, 실드, 섀시 연결부를 통해 흐르는 고주파 전류에 관한 추가 정보를 제공할 수 있다.

필터링(Filtering)은 실제 시스템에 존재하는 임피던스(Impedance)와 노이즈 모드(Noise Mode)에 따라 설계해야 한다. 단순히 더 큰 커패시터를 추가한다고 방출이 반드시 감소하는 것은 아니며, 고주파에서는 부품의 기생 성분(Component Parasitics)과 배선 인덕턴스가 더욱 중요해진다. 필터 커패시터, 인덕터(Inductor), 공통 모드 초크, 페라이트(Ferrite), 피드스루 부품(Feedthrough Component)은 유효 주파수 범위를 고려하여 선정해야 한다. 물리적 배치도 중요하며, 우수한 필터라도 노이즈의 유입 또는 유출 지점에서 멀리 배치하면 효과가 크게 감소할 수 있다.

PCB 레이아웃(PCB Layout)은 고주파 전류가 단순한 직류 저항(DC Resistance)이 아니라 임피던스에 의해 결정되는 경로를 따르기 때문에 전도 방출에 큰 영향을 미친다. 스위칭 루프는 작게 구성하고 귀환 경로는 연속성을 유지해야 하며, 노이즈가 큰 스위칭 노드는 민감한 인터페이스와 외부 커넥터에서 떨어뜨려야 한다. 디커플링 부품(Decoupling Component)은 지원 대상 회로 가까이에 배치해야 한다. 부적절한 PCB 형상은 기생 인덕턴스와 커패시턴스를 만들어 적절하게 선정된 필터 부품을 우회하여 노이즈가 전달되도록 할 수 있다.

하네스 및 커넥터 설계(Harness and Connector Design) 역시 전도 EMC 특성에 직접적으로 기여한다. 긴 전원 도체는 임피던스를 증가시키고 컨버터 입력 필터와 상호작용할 수 있으며, 실드 종단(Shield Termination)과 커넥터 본딩(Connector Bonding)은 공통 모드 전류 경로에 영향을 준다. 신호 케이블과 전원 케이블을 함께 배선하면 서브시스템 사이에 원하지 않는 결합이 발생할 수 있다. 따라서 가능한 경우 검증 과정에서 실제 양산 하네스 구성(Production Harness Configuration)을 재현해야 한다.

모터 드라이브(Motor Drive)는 이동 로봇(Mobile Robot)과 매니퓰레이터(Manipulator)에서 특별한 주의가 필요하다. 빠른 인버터 스위칭은 모터 권선(Motor Winding), 모터 프레임(Motor Frame), 상 케이블(Phase Cable), 기생 커패시턴스를 통해 결합될 수 있는 고주파 전압 전이를 발생시킨다. 이러한 전류는 섀시 구조나 저전압 전자장치를 통해 귀환하여 공유 전원 네트워크를 오염시킬 수 있다. 짧은 모터 연결, 차폐된 상 케이블, 적절한 접지, 제어된 스위칭 에지, 로컬 필터링, 전력 경로와 신호 경로의 분리를 통해 시스템 EMC 성능을 크게 향상시킬 수 있다.

전도 방출(Conducted Emission)과 방사 방출(Radiated Emission)은 서로 독립적인 현상으로 취급해서는 안 된다. 케이블을 따라 흐르는 고주파 전류는 처음에는 전도성 방해로 나타나지만 이후 케이블이 안테나처럼 동작하면서 방사 방출을 발생시킬 수 있다. 반대로 인클로저 내부에서 발생한 전자기장이 배선으로 결합되어 측정 가능한 전도성 노이즈가 될 수도 있다. 따라서 공통 모드 전류(Common-Mode Current)를 제어하면 전도 방출과 방사 방출 성능을 동시에 개선할 수 있는 경우가 많다.

시험 결과에는 측정 주파수, 방해 레벨, 적용 제한값, 적합성 마진(Compliance Margin), 운전 상태, 전기 부하, 케이블 구성, 측정 네트워크, 검파기 설정, 관련 하드웨어 및 소프트웨어 구성을 기록해야 한다. 로봇에서는 소프트웨어 워크로드(Software Workload)와 액추에이터 상태(Actuator State)에 따라 전기적 활동이 동적으로 변화할 수 있으므로 반복성(Repeatability)이 특히 중요하다. 구성 기록은 문제 해결, 설계 검증, 회귀 시험(Regression Testing), 최종 적합성 평가에서 동일한 운전 조건을 재현할 수 있도록 작성해야 한다.

적용 제한값보다 약간 낮은 측정 결과를 반드시 강건한 설계(Robust Design)로 판단해서는 안 된다. 양산 공차, 부품 대체, 케이블 길이 변화, 배터리 전압, 컨버터 부하, 온도, 소프트웨어 업데이트, 제조 차이는 전도성 노이즈 스펙트럼을 변화시킬 수 있다. 따라서 공학적 검증에서는 합리적인 적합성 마진을 확보하고 반복적으로 제한값에 접근하는 주파수를 추적해야 한다. 이러한 주파수는 현재 시제품이 공식적으로 합격하더라도 잠재적인 EMC 취약성(EMC Weakness)을 나타내는 중요한 지표가 된다.

시정 조치(Corrective Action)는 확인된 발생원-경로-수신부 관계(Source-Path-Receiver Relationship)를 기반으로 수행해야 한다. 지배적인 메커니즘에 따라 스위칭 루프 면적 감소, 컨버터 동작 변경, 차동 모드 또는 공통 모드 필터링 추가, 섀시 본딩 개선, 케이블 차폐 변경, 커넥터 종단 최적화, PCB 귀환 경로 재설계 등이 필요할 수 있다. 각각의 변경 사항은 동일한 운전 조건에서 다시 측정하여 효과를 추정하는 것이 아니라 실제로 입증해야 한다.

제공된 시험 계층 구조에서 전도 방출 시험(Conducted Emission Testing)은 EMC 시험(EMC Test) 장 내에서 방사 방출 시험(Radiated Emission), 정전기 방전 내성 시험(ESD Immunity Test), 서지 내성 시험(Surge Immunity Test), EMC 사전 적합성 시험(EMC Pre-Compliance Test)과 함께 구성된다. 이러한 구성은 로봇 시스템이 스스로 발생시키는 전자기 방해를 제어하는 동시에 외부 전자기 방해에 노출되어도 신뢰성 있게 동작해야 한다는 종합적인 검증 철학을 반영한다. 따라서 전도 방출 시험은 통합된 로봇 전기 아키텍처(Integrated Robotic Electrical Architecture)의 전자기적 건전성(Electromagnetic Integrity)을 입증하는 핵심 검증 활동이다.

## 03.03. ESD Immunity Test

![](images/image3.png){width="7.268055555555556in" height="7.268055555555556in"}

정전기 방전 내성 시험(ESD Immunity Testing)은 전기·전자 장비가 갑작스러운 정전기 방전(Electrostatic Discharge)에 노출되었을 때에도 안전하고 정상적으로 동작을 지속할 수 있는지를 평가한다. 제공된 시험 구조에서 ESD 내성 시험은 방사 방출 시험(Radiated Emission), 전도 방출 시험(Conducted Emission), 서지 내성 시험(Surge Immunity), EMC 사전 적합성 시험(EMC Pre-Compliance Testing)과 함께 EMC 검증(EMC Validation) 장에 포함된다. 목적은 정상적인 취급과 운용 과정에서 발생할 수 있는 과도 방해(Transient Disturbance)에 대한 시스템의 강건성(Robustness)을 검증하는 것이다.

정전기 전하(Electrostatic Charge)는 물질이 서로 접촉하거나 분리되거나 상대적으로 움직일 때 축적될 수 있다. 사람의 움직임, 합성섬유 의류, 플라스틱 표면, 바퀴, 바닥재, 포장재, 낮은 습도의 환경 등은 상당한 전위차(Potential Difference)를 발생시킬 수 있다. 대전된 사람이나 물체가 도전성 장비에 접근하면 저장된 에너지가 매우 짧은 시간에 방전되면서 급격한 전류 상승과 상당한 고주파 전자기 성분(High-Frequency Electromagnetic Content)을 가진 고전압 과도현상(High-Voltage Transient)을 발생시킬 수 있다.

로봇 시스템에서 ESD는 장비가 디스플레이(Display), 버튼(Button), 충전 인터페이스(Charging Interface), 커넥터(Connector), 비상 스위치(Emergency Switch), 커버(Cover), 손잡이(Handle), 노출된 기계 구조물 등에 사람이 직접 접촉하는 환경에서 자주 운용되기 때문에 특히 중요하다. 이동 로봇(Mobile Robot)은 절연성 바닥 위를 이동하면서 자체적으로 전하를 축적할 수도 있다. 접근 가능한 지점에서 발생한 방전은 섀시(Chassis), 케이블 실드(Cable Shield), 접지 네트워크(Grounding Network), 전력 분배(Power Distribution), 신호 인터페이스(Signal Interface)를 통해 전파되어 최초 방전 위치에서 멀리 떨어진 전자 모듈까지 교란할 수 있다.

따라서 ESD 현상은 단순한 국부적 전기 스파크(Local Electrical Spark)가 아니라 시스템 수준의 전자기 방해(System-Level Electromagnetic Disturbance)로 고려해야 한다. 방전 전류(Discharge Current)는 도전성 표면을 통해 유입되어 기계 구조물 전체로 확산되면서 국부적인 접지 전위(Local Ground Potential)를 급격하게 변화시킬 수 있다. 동시에 빠른 과도현상은 주변 회로에 용량성 또는 유도성으로 결합될 수 있는 전자기장을 발생시킨다. 그 결과 민감한 프로세서(Processor), 통신 인터페이스(Communication Interface), 센서(Sensor), 리셋 라인(Reset Line), 고임피던스 입력(High-Impedance Input)에서 일시적 또는 영구적인 교란이 발생할 수 있다.

일반적인 내성 평가(Immunity Evaluation)에서는 표준화된 방전 특성을 재현하는 교정된 ESD 발생기(Calibrated ESD Generator)를 사용한다. 발생기는 전기 에너지를 저장한 후 정의된 방전 네트워크(Discharge Network)를 통해 방출하여 일관된 시험을 수행할 수 있도록 한다. 시험 대상 장비(Equipment Under Test, EUT)는 제어된 구성으로 배치하고 대표적인 기능 모드(Functional Mode)로 동작시키면서 지정된 위치에 방전을 인가한다. 시험 전압(Test Voltage), 극성(Polarity), 방전 횟수(Number of Discharges), 인가 지점(Application Point), 환경 조건(Environmental Condition)은 제어되고 문서화되어야 한다.

접촉 방전(Contact Discharge)은 장비와 안정적인 전기적 접촉을 형성할 수 있는 도전성 표면에 일반적으로 적용한다. ESD 발생기 팁(Generator Tip)을 선택한 지점에 접촉시킨 후 방전을 시작하므로 비교적 반복성이 높은 전류 파형(Current Waveform)을 얻을 수 있다. 제품의 구조와 적용 시험 계획(Test Plan)에 따라 금속 인클로저(Metallic Enclosure), 도전성 제어부(Conductive Control), 커넥터 셸(Connector Shell), 노출된 체결부(Exposed Fastener), 충전 접점(Charging Contact), 기타 접근 가능한 도전성 구조물이 주요 시험 위치가 될 수 있다.

공기 방전(Air Discharge)은 직접적인 접촉 방전이 적합하지 않은 경우, 특히 절연 표면(Insulating Surface), 틈새(Gap), 이음부(Seam), 자연적인 스파크가 발생할 수 있는 기타 접근 가능한 위치에 사용된다. 대전된 발생기 전극(Generator Electrode)을 시험 지점에 접근시키면 중간 공기의 절연 파괴(Air Breakdown)가 발생하면서 방전된다. 공기 절연 파괴는 접근 속도, 형상(Geometry), 습도(Humidity), 표면 상태(Surface Condition) 등에 영향을 받기 때문에 공기 방전은 접촉 방전보다 변동성이 클 수 있으며 신중한 시험 수행이 필요하다.

간접 방전 시험(Indirect Discharge Testing)은 ESD가 장비에 직접 발생하는 것이 아니라 장비 근처에서 발생했을 때 생성되는 방해를 평가한다. 시험 대상 장비 주변에 배치된 정의된 결합 구조물(Coupling Structure)에 방전을 인가하여 발생한 전자기장과 과도 전류가 시스템과 상호작용하도록 한다. 실제 제품에서는 사람이 전자장치의 인클로저에 직접 방전하지 않더라도 인접한 도전성 물체에 방전하는 것만으로 오동작이 발생할 수 있으므로 이러한 시험 방법은 중요하다.

시험 대상 장비는 시험 전체 과정에서 대표적인 운전 상태(Representative Operational State)를 유지해야 한다. 로봇의 경우 활성화된 컴퓨팅 모듈(Computing Module), 통신 네트워크(Communication Network), 센서, 모터 제어 전자장치(Motor-Control Electronics), 안전 제어기(Safety Controller), 디스플레이, 전력 변환기(Power Converter)를 포함할 수 있다. 기능 모니터링(Functional Monitoring)은 완전한 시스템 정지뿐만 아니라 일시적인 리셋, 통신 오류, 손상된 센서 정보, 예상하지 못한 액추에이터 명령(Actuator Command), 인지 성능 저하, 안전 상태 전환(Safety-State Transition), 네트워크 동기화 손실까지 검출해야 한다.

시험 지점(Test Point)은 실제 사람과의 상호작용과 전기적 결합 경로(Electrical Coupling Path)를 고려하여 선정해야 한다. 디스플레이, 버튼, 비상 정지 제어부(Emergency-Stop Control), 충전 커넥터(Charging Connector), 통신 포트(Communication Port), 인클로저 이음부(Enclosure Seam), 노출 금속(Exposed Metal), 센서 하우징(Sensor Housing), 서비스 인터페이스(Service Interface) 주변은 특히 주의해야 한다. 무작위로 방전을 인가하기보다 전하가 유입될 가능성이 높은 위치와 방전 전류가 섀시, 하네스, 접지, 전자 아키텍처를 통해 이동할 수 있는 경로를 공학적으로 분석해야 한다.

접지 및 섀시 설계(Grounding and Chassis Design)는 ESD 내성에 큰 영향을 미친다. 잘 설계된 도전성 섀시는 방전 전류를 민감한 전자장치에서 우회시키는 제어된 저임피던스 경로(Low-Impedance Path)를 제공할 수 있다. 반대로 인클로저 부분 사이의 불량한 본딩(Bonding)은 국부적인 전위차를 발생시키고 과도 전류가 의도하지 않은 경로를 통해 흐르게 만들 수 있다. 따라서 기계적 접합부(Mechanical Joint), 도장 표면(Painted Surface), 양극 산화 처리 부품(Anodized Component), 체결 하드웨어(Mounting Hardware), 케이블 실드, 커넥터 셸을 고주파 전류 귀환 아키텍처(High-Frequency Current-Return Architecture)의 일부로 고려해야 한다.

PCB 설계(PCB Design) 역시 ESD가 매우 빠른 과도 성분을 포함하기 때문에 중요하다. 연속적인 기준면(Reference Plane), 짧은 귀환 경로(Return Path), 제어된 인터페이스 배선(Interface Routing), 적절한 이격(Separation), 신중한 커넥터 배치(Connector Placement)는 민감한 회로로의 결합을 감소시킬 수 있다. 외부 인터페이스에는 유입 지점 가까이에 배치된 과도현상 보호 부품(Transient Protection Component)이 필요할 수 있다. 보호 소자가 커넥터에서 멀리 떨어져 있으면 방전 전류가 보호 소자에 도달하기 전에 상당한 PCB 배선을 통과하여 보호 전략의 효과가 감소할 수 있다.

인터페이스 보호(Interface Protection)에는 과도 전압 억제 소자(Transient Voltage Suppression Device), 필터링 부품(Filtering Component), 직렬 임피던스(Series Impedance), 차폐(Shielding), 정밀하게 제어된 접지 구조(Grounding Structure) 등이 포함될 수 있다. 보호 소자를 선정할 때는 정상 신호 전압, 인터페이스 대역폭(Interface Bandwidth), 커패시턴스(Capacitance), 클램핑 특성(Clamping Behavior), 예상 과도 에너지(Transient Energy)를 고려해야 한다. 저속 제어 입력에 적합한 보호 방식이 고속 이더넷, 카메라 또는 센서 인터페이스에서는 과도한 커패시턴스로 신호 무결성(Signal Integrity)을 저하시킬 수 있다.

내성(Immunity)은 단순히 하드웨어가 손상되지 않는 것으로 결정되지 않으므로 소프트웨어 동작(Software Behavior)도 평가해야 한다. ESD는 하드웨어를 손상시키지 않으면서 짧은 통신 중단, 손상된 패킷(Corrupted Packet), 센서 타임아웃(Sensor Timeout), 프로세서 예외(Processor Exception), 일시적인 주변장치 리셋(Peripheral Reset)을 발생시킬 수 있다. 강건한 소프트웨어는 비정상 상태를 감지하고 잘못된 정보를 거부하며 필요한 경우 통신을 복구하고, 지속적인 동작의 안전성을 보장할 수 없는 경우 로봇을 제어된 상태(Controlled State)로 전환해야 한다. 따라서 복구 동작(Recovery Behavior)도 기능적 합격 기준(Functional Acceptance Criteria)에 포함해야 한다.

안전 관련 기능(Safety-Related Function)은 ESD 시험 과정에서 특별한 주의가 필요하다. 방해가 제어되지 않은 움직임(Uncontrolled Motion), 예상하지 못한 모터 활성화(Unexpected Motor Activation), 제동 제어 손실(Loss of Braking Control), 보호 기능의 위험한 우회(Unsafe Bypass)를 발생시켜서는 안 된다. 시스템이 일시적으로 인지 또는 통신 기능을 상실하더라도 그 대응은 의도된 안전 아키텍처(Safety Architecture)와 일치해야 한다. 따라서 ESD 내성 시험에서는 일반적인 사용자 인터페이스나 컴퓨팅 기능뿐만 아니라 액추에이터 명령과 안전 상태도 함께 모니터링해야 한다.

환경 조건(Environmental Condition)은 특히 공기 방전 시험에서 정전기 거동에 영향을 준다. 습도, 온도, 절연 재료(Insulating Material), 표면 오염(Surface Contamination)은 전하 축적과 절연 파괴 특성(Breakdown Characteristic)에 영향을 미칠 수 있다. 따라서 시험 보고서에는 장비 구성과 함께 관련 환경 조건을 기록해야 한다. 일관된 환경 제어(Environmental Control)는 반복성을 향상시키고 실제 설계 변경으로 발생한 차이와 시험 환경 변화에 의한 차이를 구분하는 데 도움이 된다.

고장 진단(Failure Diagnosis)은 전체 방해 전달 경로(Disturbance Path)에 초점을 맞춰야 한다. 로봇이 인클로저 이음부에 방전을 인가한 후 리셋되었다고 해서 프로세서 자체의 내성이 부족하다고 즉시 판단해서는 안 된다. 방전이 불량한 섀시 본딩을 통해 유입되거나 케이블 실드에 결합되고, 전원 기준 전위(Power Reference)를 변화시키거나 리셋 신호를 교란하거나 통신 인터페이스를 통해 전파되었을 수 있다. 전류 경로 분석(Current-Path Analysis)과 의심되는 결합 지점의 제어된 변경을 통해 실제 메커니즘을 확인할 수 있다.

시정 조치(Corrective Measure)에는 섀시 본딩 개선, 실드 종단(Shield Termination) 수정, 커넥터 접지 개선, PCB 귀환 경로 최적화, 과도현상 보호 소자 적용, 인터페이스 필터링, 물리적 이격 증가, 인클로저 수정(Enclosure Modification) 등이 포함될 수 있다. 방전 전류가 통신 또는 센서 배선에 강하게 결합되는 경우에는 케이블 배선(Cable Routing)을 수정해야 할 수도 있다. 효과적인 대책은 과도 에너지에 우선적인 전달 경로(Preferred Path)를 제공하면서 해당 에너지가 민감한 전자장치나 중요 기준 회로를 통과하지 않도록 해야 한다.

각각의 시정 조치 이후에는 동일한 방전 지점, 극성, 운전 조건, 기능 상태에서 반복 시험(Repeat Testing)을 수행해야 한다. 제품에 여러 운전 모드나 케이블 구성이 존재하는 경우 단 하나의 구성에서 합격하는 것만으로는 충분하지 않다. 인클로저, 하네스, 커넥터, PCB 레이아웃, 소프트웨어, 접지에 변경이 이루어진 후에는 회귀 시험(Regression Testing)이 중요하다. 기계 설계, 비용 절감, 제조성을 목적으로 한 변경도 의도하지 않게 ESD 전류 경로를 변화시킬 수 있기 때문이다.

시험 문서(Test Documentation)에는 장비 구성, 운전 모드, 방전 방법, 시험 지점, 극성, 인가 레벨(Applied Level), 관찰된 동작, 복구 특성(Recovery Characteristic), 최종 합격 상태(Acceptance Status)를 기록해야 한다. 시스템이 자동으로 복구되는 경우에도 기능적 이상 현상(Functional Anomaly)은 기록해야 한다. 이러한 정보는 엔지니어링 팀이 하드웨어 손상, 일시적 성능 저하, 자체 복구 가능한 방해(Self-Recovering Disturbance), 안전 관련 고장(Safety-Relevant Failure)을 구분할 수 있게 하며 이후 설계 변경과 적합성 평가를 위한 추적성(Traceability)을 제공한다.

제공된 검증 계층 구조에서 ESD 내성 시험(ESD Immunity Testing)은 앞선 방사 및 전도 방출 평가를 보완하면서 로봇이 발생시키는 방해에서 로봇에 가해지는 방해로 평가 관점을 전환한다. 서지 내성 시험(Surge Immunity Testing) 및 EMC 사전 적합성 시험과 함께 방출 제어(Emission Control)와 외부 방해 내성(Disturbance Tolerance)을 모두 포괄하는 보다 광범위한 EMC 검증 프로세스를 구성한다. 통합 로봇 플랫폼에서는 이를 통해 전기 아키텍처, 기계 구조, 접지, 인터페이스, 소프트웨어 복구 기능이 함께 전자기적 강건성(Electromagnetic Robustness)에 기여하는지를 검증한다.

## 03.04. Surge Immunity Test

![](images/image4.png){width="7.268055555555556in" height="7.268055555555556in"}

서지 내성 시험(Surge Immunity Testing)은 전기·전자 장비가 고에너지 과도 과전압 및 과도 전류(High-Energy Transient Overvoltage and Current)에 노출되었을 때 허용할 수 없는 성능 저하, 오동작 또는 손상 없이 이를 견딜 수 있는지를 평가한다. 제공된 검증 구조에서 서지 내성 시험은 방사 방출 시험(Radiated Emission), 전도 방출 시험(Conducted Emission), 정전기 방전 내성 시험(ESD Immunity), EMC 사전 적합성 시험(EMC Pre-Compliance Testing)과 함께 EMC 시험(EMC Test) 장에 포함된다. 이는 일반적인 정전기 방전보다 훨씬 큰 에너지를 포함하는 과도 방해(Transient Disturbance)를 대상으로 한다.

전기적 서지(Electrical Surge)는 스위칭 동작(Switching Operation), 유도성 부하 차단(Inductive Load Interruption), 전력망 교란(Power-Network Disturbance), 릴레이 또는 접촉기 동작(Relay or Contactor Operation), 충전 장비(Charging Equipment), 인접한 낙뢰에 의한 결합(Lightning-Related Coupling) 등에서 발생할 수 있다. 이러한 현상은 연결된 도체에 짧은 시간 동안 지속되지만 높은 에너지를 가진 전압 및 전류 과도현상을 발생시킬 수 있다. 로봇 시스템에서는 외부 전원 입력, 충전 포트, 긴 케이블, 통신 인터페이스, 접지 연결 또는 분산 장비에 연결된 배선을 통해 방해가 유입될 수 있다.

서지(Surge)는 특성 에너지와 시간적 거동 측면에서 정전기 방전(ESD)과 차이가 있다. ESD는 일반적으로 매우 빠른 상승 시간(Rise Time)과 상대적으로 제한된 저장 에너지(Stored Energy)를 가지지만, 서지 현상은 일반적으로 더 오랫동안 지속되며 장비에 훨씬 많은 에너지를 전달할 수 있다. 이러한 차이는 보호 설계(Protection Design)에 직접적인 영향을 준다. ESD 과도현상을 성공적으로 클램핑(Clamping)하는 부품이라도 반복적인 서지에 노출될 경우 열화나 치명적인 고장 없이 견딜 수 있는 충분한 에너지 처리 능력(Energy-Handling Capability)을 갖지 못할 수 있다.

기본적인 서지 내성 모델(Surge Immunity Model)은 방해 발생원(Disturbance Source), 결합 경로(Coupling Path), 시험 대상 장비(Equipment Under Test), 그리고 이들 사이에 위치하는 보호 네트워크(Protection Network)로 구성된다. 과도현상은 외부 인터페이스를 통해 유입되어 도체를 따라 전파되며, 이후 우회되거나 흡수되거나 제한되거나 소산된다. 보호 아키텍처(Protection Architecture)가 충분하지 않으면 과도한 전압이 전력 변환기, 통신 송수신기, 프로세서, 센서, 모터 제어기 또는 절연 구조에 도달하여 기능 장애나 영구적인 손상을 발생시킬 수 있다.

제어된 서지 시험(Controlled Surge Test)은 정의된 전압 및 전류 파형을 발생시킬 수 있는 표준화된 발생기(Standardized Generator)를 사용한다. 발생기는 적절한 결합 및 감결합 구성(Coupling and Decoupling Arrangement)을 통해 시험 대상 장비와 연결되며, 이를 통해 과도현상을 반복 가능하게 인가하는 동시에 보조 장비로의 의도하지 않은 전파를 제한한다. 시험 파라미터에는 인가 전압 레벨(Applied Voltage Level), 극성(Polarity), 펄스 횟수(Number of Pulses), 반복 간격(Repetition Interval), 결합 모드(Coupling Mode), 방해가 인가되는 전기적 인터페이스가 포함된다.

시험 계획(Test Plan)에서 요구하는 경우 시험 대상 장비(EUT)는 서지가 인가되는 동안 대표적인 기능 상태(Representative Functional State)에서 동작해야 한다. 로봇에서는 메인 컴퓨터(Main Computer), 안전 제어기(Safety Controller), DC/DC 컨버터, 통신 네트워크, 센서, 모터 드라이버, 충전 전자장치(Charging Electronics), 보조 부하(Auxiliary Load) 등이 활성화될 수 있다. 서지는 눈에 보이는 하드웨어 손상이 없더라도 짧은 리셋, 통신 중단, 센서 고장, 안전 상태 전환 또는 액추에이터 정지를 발생시킬 수 있으므로 지속적인 모니터링이 중요하다.

전원 인터페이스(Power Interface)는 외부 에너지원과 내부 전자장치를 직접 연결하기 때문에 가장 중요한 서지 유입 지점 중 하나이다. AC 전원 장비는 전력 공급망에서 방해를 받을 수 있으며, DC 전원 로봇은 충전기, 도킹 스테이션(Docking Station), 외부 전원 공급장치, 긴 DC 케이블 또는 스위칭 장비를 통해 과도현상에 노출될 수 있다. 배터리로 동작한다고 해서 서지 위험이 자동으로 제거되는 것은 아니며, 외부 충전 및 인프라 연결이 로봇 내부로 이어지는 도전성 경로(Conductive Path)를 형성할 수 있다.

차동 모드 서지(Differential-Mode Surge)는 선간(Line-to-Line) 또는 전원의 양극과 음극(Positive-to-Negative) 연결처럼 동일한 전기회로에 속하는 도체 사이에서 발생한다. 이때 발생하는 전압은 연결된 장비의 입력단에 직접 인가되어 커패시터, 반도체 스위치(Semiconductor Switch), 컨버터 및 보호 소자에 스트레스를 가할 수 있다. 효과적인 저감을 위해서는 과도현상 억제 소자(Transient Suppressor), 적절한 입력 필터링(Input Filtering), 제어된 임피던스(Controlled Impedance), 에너지 흡수 부품(Energy-Absorbing Component), 영향을 받는 전체 전력 경로의 충분한 정격 전압이 필요할 수 있다.

공통 모드 서지(Common-Mode Surge)는 하나 이상의 활성 도체(Active Conductor)와 섀시, 보호 접지(Protective Earth) 또는 다른 기준 구조(Reference Structure) 사이에서 발생한다. 이러한 방해는 접지와 기계 구조를 통해 큰 과도 전류를 흐르게 하며 여러 서브시스템에 동시에 영향을 줄 수 있다. 따라서 보호 성능은 개별 억제 소자뿐만 아니라 섀시 본딩(Chassis Bonding), 접지 토폴로지(Grounding Topology), 실드 종단(Shield Termination), 절연 협조(Insulation Coordination), 과도 전류가 흐를 수 있는 짧고 낮은 임피던스의 경로에 의해 결정된다.

결합 및 감결합 네트워크(Coupling and Decoupling Network)는 제어된 서지 시험에서 중요한 요소이다. 이 네트워크는 과도현상을 의도한 도체에 인가하면서 외부 지원 장비 또는 시험실 전원 공급원으로 전파되는 것을 감소시킨다. 선택되는 네트워크는 해당 인터페이스와 시험 목적에 적합해야 한다. 잘못된 결합 방식은 비현실적인 스트레스를 발생시키거나 실제 방해 전달 경로를 제대로 재현하지 못할 수 있으므로 구성 관리(Configuration Control)가 의미 있는 내성 평가에서 매우 중요하다.

서지 보호(Surge Protection)는 하나의 보호 부품이 아니라 에너지 관리 아키텍처(Energy-Management Architecture)로 설계해야 한다. 첫 번째 보호 단계(Protection Stage)는 유입되는 과도 에너지의 상당 부분을 우회시키거나 흡수할 수 있으며, 이후 단계에서는 잔류 전압(Residual Voltage)을 민감한 전자장치가 견딜 수 있는 수준으로 감소시킨다. 보호 단계 사이의 적절한 협조(Coordination)는 하위 부품에 과도한 스트레스가 집중되는 것을 방지하고 적절한 전압, 전류 및 에너지 처리 능력을 가진 여러 소자에 과도 에너지를 분산시킨다.

과도 전압 억제 소자(Transient Voltage Suppression Device)는 취약한 인터페이스 근처에서 일반적으로 사용되지만 그 효과는 단순한 공칭 클램핑 전압(Nominal Clamping Voltage)만으로 결정되지 않는다. 엔지니어는 최대 펄스 전류(Peak Pulse Current), 에너지 처리 능력, 동적 저항(Dynamic Resistance), 응답 특성(Response Behavior), 누설 전류(Leakage), 커패시턴스, 반복 스트레스(Repetitive Stress), 고장 모드(Failure Mode)를 고려해야 한다. 보호 대상 회로 역시 보호 소자가 도통하는 동안 남아 있는 잔류 전압을 견딜 수 있어야 한다.

고전류 과도현상이 발생할 때는 물리적 레이아웃(Physical Layout)이 매우 중요해진다. 긴 PCB 패턴, 배선 및 접지 연결에는 기생 인덕턴스(Parasitic Inductance)가 존재하며, 급격한 전류 변화에 따라 추가적인 전압을 발생시킨다. 따라서 전기적으로는 보호 소자가 가까워 보이더라도 물리적으로 커넥터에서 멀리 떨어져 있으면 전류가 억제 소자에 도달하기 전에 상당한 과도 전압이 발생할 수 있다. 짧고 넓은 전류 경로와 적절한 기준 구조에 대한 직접적인 연결은 보호 효과를 향상시킨다.

접지 및 섀시 아키텍처(Grounding and Chassis Architecture)는 서지 전류가 시스템에 유입된 이후 어느 경로로 흐르는지를 결정한다. 강건한 설계(Robust Design)는 과도 에너지가 민감한 로직 접지(Logic Ground)나 통신 기준 전위(Communication Reference)를 통과하지 않도록 예측 가능한 전류 경로를 제공한다. 불량한 본딩은 인클로저 부분이나 전자 모듈 사이에 큰 전위차를 발생시킬 수 있다. 따라서 분산형 로봇에서는 기계 프레임, 배터리 인클로저, 컴퓨팅 캐비닛, 모터 하우징, 커넥터 실드를 과도 전류 아키텍처(Transient-Current Architecture)의 일부로 고려해야 한다.

모터 드라이브(Motor Drive)와 전기기계 장비(Electromechanical Equipment)는 과도 방해를 받을 수도 있고 자체적으로 발생시킬 수도 있다. 접촉기, 릴레이, 브레이크, 솔레노이드(Solenoid), 모터, 유도성 부하는 자기 에너지(Magnetic Energy)를 저장하며 전류가 차단될 때 이 에너지가 방출되어야 한다. 적절한 억제 장치가 없으면 로봇 내부에서도 상당한 전압 스파이크(Voltage Spike)가 발생할 수 있다. 플라이백 경로(Flyback Path), 스너버(Snubber), 억제 소자, 제어된 스위칭, 로컬 에너지 관리(Local Energy Management)를 통해 내부에서 발생한 과도현상이 공유 전원 네트워크로 전파되기 전에 감소시킬 수 있다.

충전 및 도킹 시스템(Charging and Docking System)은 이동 로봇을 외부 인프라에 연결하기 때문에 특별한 주의가 필요하다. 접점 바운스(Contact Bounce), 커넥터 체결, 충전기 스위칭, 접지 전위차(Grounding Difference), 전력 변환 장비는 연결 및 분리 과정에서 과도 스트레스를 발생시킬 수 있다. 따라서 인터페이스는 적절한 전기 정격, 시퀀싱(Sequencing), 필요한 경우 프리차지(Pre-Charge), 과도현상 억제, 접지 전략, 모니터링을 함께 적용하여 반복적인 도킹이 전력 전자장치를 점진적으로 손상시키지 않도록 해야 한다.

통신 및 센서 인터페이스(Communication and Sensor Interface)도 케이블이 보호 인클로저 외부로 연장되거나 물리적으로 상당히 떨어진 장비를 연결하는 경우 서지 영향을 고려해야 한다. 서로 다른 접지 구조 사이의 전위차는 실드 또는 신호 기준선을 통해 과도 전류를 흐르게 할 수 있다. 통신 시스템의 대역폭과 신호 무결성 요구사항을 유지하면서 절연(Isolation), 실드 본딩(Shield Bonding), 서지 대응 인터페이스 부품(Surge-Rated Interface Component), 제어된 접지, 전용 보호 네트워크를 적용할 필요가 있다.

기능적 합격 기준(Functional Acceptance Criteria)은 영구적인 손상, 일시적인 기능 상실, 자동 복구(Automatic Recovery), 운전자 개입이 필요한 동작을 구분해야 한다. 자율 로봇(Autonomous Robot)에서는 일시적인 방해라도 제어되지 않은 움직임이나 제동, 위치추정(Localization), 인지(Perception), 안전 통신(Safety Communication)의 상실을 발생시키면 안전에 치명적일 수 있다. 따라서 서지 내성 평가는 각 펄스 이후 전자 하드웨어에 전원이 유지되는지만 확인하는 것이 아니라 시스템 수준의 동작(System-Level Behavior)을 관찰해야 한다.

안전 기능(Safety Function)은 과도현상이 발생하는 동안과 이후에도 의도된 안전 아키텍처(Safety Architecture)와 일치하는 상태를 유지해야 한다. 정상 운전을 지속할 수 없는 경우 로봇은 의도하지 않은 액추에이터 명령을 발생시키는 대신 적절하게 제어된 상태 또는 안전 상태(Safe State)로 전환되어야 한다. 시험 구성과 관련되는 경우 모니터링에는 모터 활성화 신호(Motor Enable Signal), 제동 상태(Braking Status), 안전 제어기 상태, 비상 정지 기능(Emergency-Stop Function), 통신 상태(Communication Health), 복구 시퀀스(Recovery Sequence)가 포함되어야 한다.

고장 진단(Failure Diagnosis)은 눈에 보이는 고장 부품만이 아니라 전체 과도현상 전달 경로(Transient Path)를 식별해야 한다. 손상된 컨버터가 최종적으로 과전압의 피해를 받은 부품일 수 있지만 실제 근본 원인(Root Cause)은 불충분한 입력 보호, 부적절한 접지, 과도한 배선 인덕턴스 또는 보호 단계 사이의 잘못된 협조일 수 있다. 전압 및 전류 측정, 보호 소자의 제어된 교체, 전류 귀환 경로(Current-Return Path) 검토를 통해 실제 근본 원인을 파악할 수 있다.

시정 조치(Corrective Action)에는 더 높은 성능의 과도현상 억제 소자, 협조된 다단 보호(Coordinated Protection Stages), 필터링 개선, 전류 경로 단축, 접지 구조 수정, 섀시 본딩 개선, 추가적인 절연, 커넥터 보호 개선, 전력 아키텍처 변경 등이 포함될 수 있다. 부품의 정격 전압(Component Voltage Rating)과 절연 마진(Insulation Margin)도 재검토해야 할 수 있다. 전류 경로를 변경하면 스트레스가 제거되는 대신 다른 서브시스템으로 이동할 수도 있으므로 모든 변경 사항은 동일한 서지 조건에서 다시 검증해야 한다.

시험 문서(Test Documentation)에는 장비 구성, 운전 상태, 인가 서지 레벨(Applied Surge Level), 극성, 결합 방법, 인가 인터페이스, 펄스 횟수, 환경 조건, 관찰된 동작, 복구 특성(Recovery Characteristic), 합격 판정(Acceptance Result)을 기록해야 한다. 하드웨어 및 소프트웨어 변경 이력도 추적할 수 있어야 한다. 상세한 기록을 통해 이후 회귀 시험(Regression Test)에서 전력 분배, 커넥터, 하네스, 인클로저, 접지 또는 전자장치의 변경이 시스템 내성에 영향을 주었는지를 확인할 수 있다.

일부 보호 소자는 개별 서지에는 견딜 수 있지만 누적 스트레스(Cumulative Stress)에 의해 점진적으로 열화될 수 있으므로 반복 시험(Repeated Testing)이 중요하다. 하나의 펄스 이후 정상적으로 동작하는 제품이라도 실제 운용에서 반복적인 방해에 노출될 경우 충분한 수명 강건성(Lifetime Robustness)을 제공하지 못할 수 있다. 따라서 공학적 검증에서는 즉각적인 합격 또는 불합격뿐만 아니라 보호 마진(Protection Margin), 부품 디레이팅(Component Derating), 반복 내구 능력(Repetitive Capability), 잠재 손상(Latent Damage)의 가능성도 고려해야 한다.

제공된 검증 계층 구조에서 서지 내성 시험(Surge Immunity Testing)은 정전기 방전 내성 시험(ESD Immunity Testing) 이후, EMC 사전 적합성 시험(EMC Pre-Compliance Testing) 이전에 배치되어 있다. 방사 및 전도 방출 평가와 함께 이러한 활동은 로봇이 발생시키는 방해와 외부에서 로봇에 가해지는 방해를 모두 포괄하는 시스템 수준의 EMC 프로세스를 구성한다. 서지 내성 시험은 특히 전력 아키텍처, 접지, 보호 회로, 인터페이스, 하드웨어, 소프트웨어, 안전 동작이 함께 고에너지 과도현상을 허용할 수 없는 결과 없이 견딜 수 있는지를 검증한다.

## 03.05. EMC Pre-Compliance Test

![](images/image5.png){width="7.268055555555556in" height="7.268055555555556in"}

EMC 사전 적합성 시험(EMC Pre-Compliance Testing)은 공식적인 전자파 적합성 인증(Formal Electromagnetic Compatibility Certification)을 수행하기 전에 실시하는 공학적 검증 활동(Engineering Verification Activity)이다. 제공된 시험 구조에서는 방사 방출 시험(Radiated Emission), 전도 방출 시험(Conducted Emission), 정전기 방전 내성 시험(ESD Immunity), 서지 내성 시험(Surge Immunity)에 이어 EMC 시험 장의 마지막 활동으로 구성된다. 목적은 전자기적 취약점을 조기에 발견하고 설계 마진(Design Margin)을 평가하여 공인 적합성 시험소(Accredited Compliance Laboratory)에 진입할 때 발생할 수 있는 기술 및 일정 위험을 줄이는 것이다.

공식 EMC 시험(Formal EMC Testing)은 전문 시험 챔버(Specialized Chamber), 교정된 장비(Calibrated Equipment), 자격을 갖춘 시험 인력(Qualified Personnel), 상당한 시험실 시간을 필요로 할 수 있다. 따라서 인증 단계에서 주요 방출 또는 내성 문제가 처음 발견되면 비용이 큰 재설계와 반복적인 시험실 예약이 발생할 수 있다. 사전 적합성 시험은 이러한 조사의 상당 부분을 개발 과정으로 앞당겨 PCB 레이아웃, 필터, 케이블, 접지, 차폐, 인클로저, 소프트웨어 운전 모드, 서브시스템 구성을 효율적으로 수정할 수 있도록 한다.

사전 적합성 시험(Pre-Compliance Testing)은 반드시 공인 인증 환경의 모든 세부 조건을 완전히 재현할 필요는 없다. 대신 잠재적인 적합성 문제를 발견하고 마진을 추정할 수 있을 정도로 제어되고 대표성 있는 측정 환경을 구축한다. 제품 및 목표 요구사항에 따라 스펙트럼 분석기(Spectrum Analyzer), EMI 수신기(EMI Receiver), 근접장 프로브(Near-Field Probe), 전류 프로브(Current Probe), 안테나(Antenna), 안정화 네트워크(Stabilization Network), 과도현상 발생기(Transient Generator), 결합 네트워크(Coupling Network), 접지면(Ground Plane), 간소화된 차폐 또는 반무반사 측정 공간(Semi-Anechoic Measurement Area) 등을 사용할 수 있다.

효과적인 사전 적합성 전략(Pre-Compliance Strategy)은 목표 제품 구성과 적용되는 EMC 요구사항을 정의하는 것에서 시작한다. 시험 대상 장비(Equipment Under Test, EUT)는 컴퓨팅 모듈, 전력 변환기, 모터 드라이버, 통신 인터페이스, 센서, 하네스, 커넥터, 접지, 차폐, 인클로저 구조 등을 포함하여 예상되는 양산 아키텍처(Production Architecture)를 가능한 한 가깝게 반영해야 한다. 지나치게 단순화된 시제품을 시험하면 최종 통합 이후에만 나타나는 시스템 수준 결합 경로(System-Level Coupling Path)를 발견하지 못할 수 있다.

운전 모드(Operating Mode) 역시 현실적인 최악 조건의 전자기 환경(Worst-Case Electromagnetic Condition)을 대표해야 한다. 로봇은 대기, 충전, 이동, 인지 데이터 처리, 플릿 서버(Fleet Server)와의 통신 또는 여러 액추에이터의 동시 동작에 따라 매우 다른 방출 특성을 나타낼 수 있다. 따라서 높은 GPU 및 CPU 사용률, 많은 이더넷 트래픽(Ethernet Traffic), PWM 모터 제어, 스위칭 컨버터, 카메라 스트림(Camera Stream), LiDAR 동작, 냉각 팬, 충전 전자장치를 조합하여 최대 전자기 활동을 유발하는 상태를 구성할 수 있다.

방출 사전 적합성 시험(Emission Pre-Compliance Testing)은 일반적으로 방사 및 전도 측정을 모두 포함한다. 방사 측정(Radiated Measurement)은 인클로저, 케이블, 이음부 및 기타 비의도성 안테나(Unintended Antenna)를 통해 제품 외부로 방출되는 전자기 에너지를 탐색하며, 전도 측정(Conducted Measurement)은 전원 및 외부 도전성 인터페이스를 통해 전파되는 노이즈를 평가한다. 목적은 시제품이 제한값 이하에 있는지만 판단하는 것이 아니라 적합성 마진(Compliance Margin)이 충분하지 않은 주파수를 식별하는 데 있다.

예상 제한값(Expected Limit)에 근접한 측정 결과는 사전 적합성 측정에서 기술적으로 합격하는 것으로 보이더라도 공학적 경고(Engineering Warning)로 취급해야 한다. 개발 시험실과 공인 시험실 사이의 차이, 측정 불확도(Measurement Uncertainty), 케이블 배치, 안테나 형상, 양산 공차, 부품 편차, 소프트웨어 워크로드에 따라 최종 결과가 달라질 수 있다. 따라서 사전 적합성 시험에서는 개별 피크가 기준선 바로 아래에 있는지를 확인하는 것보다 합리적인 수준의 마진을 확보하는 것이 중요하다.

내성 사전 적합성 시험(Immunity Pre-Compliance Testing)은 대표적인 전자기 방해를 의도적으로 인가했을 때 시스템이 허용 가능한 성능을 계속 유지하는지를 평가한다. 검증 범위에 따라 EMC 장에서 이미 다루어진 정전기 방전(ESD) 및 서지(Surge) 현상을 포함할 수 있다. 목적은 공식 내성 시험을 시작하기 전에 취약한 인터페이스, 접지 경로, 리셋 메커니즘(Reset Mechanism), 통신 링크, 보호 소자, 소프트웨어 복구 동작(Software Recovery Behavior)을 발견하는 것이다.

로봇에서는 외관만으로 확인할 수 없는 고장이 발생할 수 있으므로 내성 평가 과정에서 기능 모니터링(Functional Monitoring)이 필수적이다. 엔지니어는 프로세서 리셋, 통신 오류, 센서 데이터 손상, 위치추정 성능 저하(Localization Degradation), 안전 제어기 상태 전환, 모터 활성화 상태, 제동 동작, 예상하지 못한 액추에이터 명령, 복구 시퀀스를 관찰해야 한다. 시스템의 전원이 유지되더라도 중요한 안전 또는 인지 기능을 상실한다면 자동으로 전자기적으로 강건한 시스템으로 판단할 수 없다.

사전 적합성 시험은 노이즈 발생원 식별(Source Identification)에 특히 유용하다. 방출 피크가 발견되면 엔지니어는 서브시스템을 선택적으로 비활성화하고 프로세서 워크로드를 변경하거나 통신 인터페이스를 중지하고, 컨버터 부하를 변경하거나 센서를 분리하고 모터 동작을 변화시킬 수 있다. 이러한 변경에 따라 스펙트럼 응답(Spectral Response)이 달라지면 원인이 되는 서브시스템이나 결합 메커니즘을 좁혀갈 수 있다. 이후 근접장 프로브와 전류 프로브를 사용하여 고주파 에너지가 흐르는 PCB 영역, 케이블, 커넥터 또는 섀시 경로를 찾을 수 있다.

동일한 발생원-경로-수신부 개념(Source-Path-Receiver Concept)을 내성 문제에도 적용할 수 있다. 충전 커넥터를 통해 유입된 방해가 전력 분배를 따라 전파되어 프로세서 리셋 라인을 교란할 수 있으며, 인클로저 이음부에 인가된 ESD가 섀시를 통해 통신 인터페이스에 결합될 수도 있다. 단순히 고장이 발생한 전자 부품만 식별하는 것으로는 충분하지 않다. 효과적인 시정 조치(Corrective Action)를 위해서는 방해가 어디에서 유입되고, 어떤 경로로 전파되며, 최종적으로 어떤 회로나 기능이 영향을 받았는지를 이해해야 한다.

임시적인 공학적 대책(Temporary Engineering Countermeasure)은 사전 적합성 작업 과정에서 진단 속도를 높일 수 있다. 페라이트(Ferrite), 추가 필터링, 임시 차폐, 개선된 본딩 스트랩(Bonding Strap), 대체 케이블 배선, 추가 접지 연결, 국부적인 억제 부품(Suppression Component) 등을 실험적으로 적용할 수 있다. 이러한 변경이 반드시 최종 양산 솔루션을 의미하는 것은 아니다. 목적은 어떤 전자기 메커니즘이 문제를 지배하는지를 확인하고 더욱 강건한 설계 변경을 위한 근거를 확보하는 것이다.

지배적인 메커니즘(Dominant Mechanism)을 이해한 이후에는 시정 조치를 실제 설계 아키텍처에 반영해야 한다. PCB 귀환 경로(Return Path)를 수정하고, 스위칭 루프를 축소하며, 공통 모드 필터링(Common-Mode Filtering)을 추가하거나 실드 종단(Shield Termination)을 개선하고, 커넥터 본딩을 강화하며, 과도현상 보호 소자(Transient Protection Device)의 위치를 변경하거나 인클로저 이음부를 수정할 수 있다. 하네스 배선 및 이격도 조정해야 할 수 있으며, 불필요한 차폐나 필터를 추가하기보다 실제 물리적 결합 메커니즘을 해결하도록 설계해야 한다.

로봇 시스템에서는 전력 전자장치(Power Electronics)와 디지털 전자장치(Digital Electronics)의 상호작용에 특별한 주의가 필요하다. 모터 드라이브, DC/DC 컨버터, 충전기, 프로세서, GPU, 이더넷 인터페이스, 카메라, 센서는 전원, 접지, 섀시, 하네스 구조를 공유할 수 있다. 따라서 하나의 서브시스템에서 발생한 노이즈가 여러 경로를 통해 다른 서브시스템에 영향을 미칠 수 있다. 대표적인 시스템 통합 이후 수행하는 사전 적합성 시험은 개별 부품 수준의 EMC 시험만으로는 완전히 확인하기 어려운 정보를 제공한다.

인클로저 패널, 장착 구조, 케이블 길이, 커넥터 위치, 본딩 지점이 EMC 특성에 영향을 주므로 기계적 구성(Mechanical Configuration)도 제어된 상태를 유지해야 한다. 디버깅 편의를 위해 커버를 제거하는 것만으로도 방사 방출이나 내성 특성이 크게 달라질 수 있다. 마찬가지로 양산 케이블을 짧은 시험용 케이블로 교체하면 공통 모드 전류 경로가 달라질 수 있다. 따라서 구성 기록(Configuration Record)은 이후 중요한 측정을 재현할 수 있을 정도로 물리적 배치를 정확하게 식별해야 한다.

소프트웨어 구성(Software Configuration)도 제어해야 한다. 현대의 로봇은 프로세서 주파수, GPU 워크로드, 통신 트래픽, 센서 활성화, 전력 관리 상태(Power-Management State), 제어 알고리즘에 따라 전기적 활동이 변화하는 소프트웨어 정의 시스템(Software-Defined System)이다. 따라서 하드웨어가 변경되지 않더라도 소프트웨어 업데이트만으로 전자기적 특성(Electromagnetic Signature)이 달라질 수 있다. 컴퓨팅, 통신 또는 액추에이터 워크로드가 크게 변경되는 소프트웨어 수정 이후에는 사전 적합성 회귀 시험(Pre-Compliance Regression Testing)을 고려해야 한다.

초기 공학적 시험에서는 시험실 수준의 완벽한 정확도보다 측정 반복성(Measurement Repeatability)이 더욱 중요하다. 안정적인 시험 구성을 확보하면 설계 변경이 EMC 성능을 개선했는지 또는 악화시켰는지를 판단할 수 있다. 따라서 설계 반복(Design Iteration)을 비교할 때 안테나 위치, 케이블 배치, 접지, 장비 방향, 운전 상태, 측정 대역폭(Measurement Bandwidth), 검파기 설정(Detector Setting), 계측기 구성을 일정하게 유지해야 한다. 공식 인증 수준의 정확도를 확보하기 전에도 상대적인 개선 정도는 매우 중요한 공학적 정보를 제공한다.

사전 적합성 결과는 단순한 합격 또는 불합격(Pass or Fail)보다 마진과 위험(Margin and Risk)을 중심으로 정리해야 한다. 큰 마진을 가진 주파수나 시험 조건은 상대적으로 낮은 위험을 의미하며, 예상 제한값에 가까운 측정 결과는 추가적인 검토가 필요하다. 일시적 성능 저하, 자동 복구, 운전자 개입 또는 안전하지 않은 동작을 발생시키는 내성 시험 결과 역시 서로 구분해야 한다. 이러한 접근을 통해 공식 인증 전에 가장 중요한 전자기적 취약점에 엔지니어링 자원을 집중할 수 있다.

실용적인 EMC 이슈 로그(EMC Issue Log)는 각각의 관찰된 이상 현상을 해당 주파수 또는 방해 조건, 운전 모드, 의심되는 발생원, 결합 경로, 영향을 받은 기능, 임시 대책, 영구 시정 조치, 재시험 결과와 연결할 수 있다. 이를 통해 설계 반복 과정 전체에 걸쳐 추적성(Traceability)을 확보하고 이미 해결된 문제가 다시 발생하는 것을 방지할 수 있다. 또한 전기, 기계, 하네스, 소프트웨어, 안전, 시스템 엔지니어링 팀 사이의 효과적인 정보 공유를 지원한다.

전자기적 동작을 변화시킬 가능성이 있는 변경 이후에는 회귀 시험(Regression Testing)을 수행해야 한다. PCB 개정, 대체 부품, 새로운 케이블 공급업체, 하네스 배선 변경, 커넥터 교체, 인클로저 수정, 접지 변경, 소프트웨어 업데이트, 모터 드라이브 튜닝(Motor-Drive Tuning), 충전기 수정은 모두 방출 또는 내성에 영향을 줄 수 있다. 이러한 변경 이후 위험도가 높은 사전 적합성 시험을 선택적으로 반복하면 제품이 공식 검증 단계에 진입하기 전에 성능 회귀를 효율적으로 발견할 수 있다.

공식 적합성 시험(Formal Compliance Testing)으로 진행할지에 대한 결정은 주요 방출 및 내성 위험이 충분히 감소했고 대표적인 구성에서 적절한 마진이 확보되었다는 증거를 기반으로 해야 한다. 시스템은 관련 운전 모드에서 반복 가능한 동작을 보여야 하며 알려진 이상 현상에 대한 처리 결과도 문서화되어야 한다. 인증이 요구되는 경우 사전 적합성 시험이 공인 인증을 대체할 수는 없지만, 공식 시험에서 큰 재설계 없이 성공할 가능성을 크게 향상시킬 수 있다.

사전 적합성 시험은 향후 제품 개발을 위한 피드백(Feedback)도 제공한다. 특정 컨버터 토폴로지(Converter Topology), 커넥터 실드 종단, 케이블 배치, 인클로저 이음부 또는 접지 구조에서 반복적으로 발생하는 문제는 내부 설계 규칙(Internal Design Rule)으로 전환할 수 있다. 시간이 지남에 따라 EMC 지식은 사후적인 문제 해결(Reactive Troubleshooting)에서 아키텍처 수준의 예방(Architecture-Level Prevention)으로 발전하며, 후속 로봇 플랫폼은 더 우수한 접지, 차폐, 필터링, 인터페이스 보호, 패키징 설계를 기반으로 개발을 시작할 수 있다.

제공된 검증 계층 구조에서 EMC 사전 적합성 시험(EMC Pre-Compliance Testing)은 방사 방출 시험, 전도 방출 시험, ESD 내성 시험, 서지 내성 시험 이후 EMC 시험 시퀀스(EMC Test Sequence)를 완성한다. 따라서 공식 검증 전에 방출 성능, 외부 방해 내성, 기능 동작, 설계 마진, 회귀 시험 증거를 통합하는 통합 게이트(Integration Gate)의 역할을 한다. 복잡한 로봇 플랫폼에서 이 공학적 단계는 EMC를 개발 후반의 인증 문제로 남겨두는 대신 전기 아키텍처 개발(Electrical Architecture Development)과 시스템 검증(System Validation)의 통제된 일부로 전환하는 데 중요한 역할을 한다.
