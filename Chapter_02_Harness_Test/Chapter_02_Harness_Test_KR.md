**Volume 19. Testing and Validation**

# Chapter 02. Harness Test

## 02.01. Dedicated Harness Tester

![](images/image1.png){width="7.268055555555556in" height="7.268055555555556in"}

전용 와이어링 하니스 시험기(Dedicated Harness Tester)는 완성된 와이어링 하니스(Wire Harness)가 로봇, 차량, 기계 또는 하위 시스템(Subsystem)에 장착되기 전에 의도된 전기 설계(Electrical Design)와 일치하는지를 확인하기 위한 전용 검증 시스템(Verification System)이다. 단순한 도통계(Continuity Meter)와 달리, 시험기는 사전에 정의된 커넥터 인터페이스(Connector Interface)와 저장된 시험 프로그램(Test Program)을 이용하여 다수의 회로를 평가한다. 이를 통해 하니스가 시스템 수준 조립(System-Level Assembly)에 투입되기 전에 제조 결함을 반복 가능하고 일관된 방법으로 검출할 수 있다.

시험기는 일반적으로 대상 장비의 전기 인터페이스(Electrical Interface)를 재현하는 전용 결합 치구(Mating Fixture) 또는 시험 어댑터(Test Adapter)를 통해 하니스에 연결된다. 각각의 하니스 커넥터(Harness Connector)는 대응하는 시험기 인터페이스에 연결되며, 이를 통해 개별 핀(Pin)을 자동으로 선택하여 검사할 수 있다. 이후 시험기는 승인된 하니스 도면(Harness Drawing), 배선표(Wiring Table) 또는 제조 정의(Manufacturing Definition)에서 생성된 기준 넷리스트(Reference Netlist)와 실제 측정된 연결 상태를 비교한다.

도통 검증(Continuity Verification)은 전용 하니스 시험기의 가장 기본적인 기능 중 하나이다. 예상되는 두 종단점(Endpoint) 사이에 제어된 시험 신호(Test Signal)를 인가하고, 측정된 저항을 허용 기준값(Acceptance Threshold)과 비교한다. 이 과정에서는 누락된 전선, 불완전한 압착(Crimp), 단선된 도체(Broken Conductor), 불완전하게 삽입된 단자(Terminal), 손상된 커넥터 접점(Contact) 등으로 발생하는 개방 회로(Open Circuit)를 검출한다. 저저항 측정(Low-Resistance Measurement)은 전기적으로 연결되어 있지만 성능이 저하된 연결 상태도 발견하는 데 활용될 수 있다.

완전한 하니스 시험(Harness Test)은 정상적으로 연결되어야 하는 회로만 확인해서는 안 된다. 서로 절연되어야 하는 회로 사이에 의도하지 않은 전기적 경로가 존재하는지도 확인해야 한다. 단락(Short Circuit)은 손상된 절연체(Insulation), 흩어진 도체 가닥(Stray Conductor Strand), 잘못된 스플라이스(Splice), 단자 삽입 오류, 오염 또는 제조 실수로 발생할 수 있다. 관련 핀 조합을 자동으로 순차 검사(Automated Scanning)하면 이러한 결함을 수동 포인트 투 포인트 측정(Point-to-Point Measurement)보다 훨씬 안정적으로 검출할 수 있다.

오배선 검출(Miswiring Detection)은 육안으로 구별하기 어려운 다수의 캐비티(Cavity)를 가진 커넥터가 사용되는 하니스에서 특히 중요하다. 두 전선이 각각 정상적인 도통 상태를 가지더라도 서로 바뀐 단자 위치에 삽입되어 있을 수 있다. 전용 시험기는 시험 대상의 모든 소스(Source)와 목적지(Destination)를 정의된 연결 매트릭스(Connectivity Matrix)와 비교함으로써 전선 교환(Swapped Wire), 교차 연결(Cross-Connection), 잘못된 분기(Branch), 잘못된 커넥터 캐비티 할당을 시스템 통합 전에 검출할 수 있다.

시험 치구(Test Fixture)는 전체 측정 시스템(Measurement System)의 핵심 구성 요소이다. 치구 커넥터(Fixture Connector)는 실링(Seal), 단자, 이차 잠금장치(Secondary Lock), 극성 구조(Polarization Feature)를 손상시키지 않으면서 생산 하니스 커넥터와 안정적으로 결합되어야 한다. 대량 생산 시험(High-Volume Testing)에서는 인터페이스 부품이 반복적인 체결 사이클(Mating Cycle)을 견딜 수 있어야 하며 마모 부품을 교체할 수 있어야 한다. 또한 시험 장비 내부의 결함이 하니스 결함으로 잘못 판정되지 않도록 치구 배선(Fixture Wiring)도 관리되어야 한다.

시험 프로그램(Test Program)은 하니스 설계가 변경될 때마다 예상되는 전기 네트워크(Electrical Network)도 변경되므로 형상 관리(Configuration Control)하에서 생성되고 유지되어야 한다. 하니스 부품 번호(Part Number), 리비전(Revision), 커넥터 구성, 핀 할당(Pin Assignment), 선택 사양 분기(Optional Branch), 적용되는 허용 기준(Acceptance Criteria)은 올바른 시험 레시피(Test Recipe)와 일치해야 한다. 변경된 하니스를 구형 기준 데이터로 시험하면 잘못된 불합격(False Failure)이 발생하거나, 더 심각하게는 잘못된 구성이 합격으로 판정될 수 있다.

따라서 실제 시험 시스템에서는 시험 대상품(Unit Under Test, UUT)을 명확하게 식별해야 한다. 작업자는 하니스를 연결하기 전에 하니스 부품 번호, 일련번호(Serial Number), 생산 지시 번호(Production Order) 또는 리비전 식별자(Revision Identifier)를 선택하거나 스캔할 수 있다. 시스템은 이에 대응하는 시험 설정(Test Configuration)을 자동으로 불러오고, 호환되지 않는 치구 또는 프로그램이 선택되었을 경우 시험 실행을 방지할 수 있다. 이러한 방식은 작업자의 기억에 대한 의존성을 줄이고 제조 추적성(Manufacturing Traceability)을 향상시킨다.

전용 하니스 시험(Dedicated Harness Testing)은 단순히 연결 여부를 이진 상태(Binary Condition)로 판단하는 대신 특정 회로에 대한 저항 허용 한계(Resistance Limit)를 포함할 수도 있다. 전력 도체(Power Conductor), 접지 귀환선(Ground Return), 안전 회로(Safety Circuit), 장거리 케이블은 과도한 저항이 전압 강하(Voltage Drop), 국부 발열(Localized Heating), 장비 동작 불안정을 유발할 수 있으므로 더욱 엄격한 저항 관리가 필요할 수 있다. 측정 기준에는 도체 길이, 전선 굵기(Wire Gauge), 단자, 스플라이스, 치구 저항 및 측정 불확도(Measurement Uncertainty)가 고려되어야 한다.

하니스에 실드(Shield), 드레인 와이어(Drain Wire) 또는 전용 섀시 접지 경로(Chassis-Ground Path)가 포함된 경우 이러한 연결 상태도 시험 정의(Test Definition)에 포함되어야 한다. 실드 종단(Shield Termination)에 오류가 있으면 신호 회로 자체는 정상적으로 연결되어 있어도 장착 후 전자기 적합성(Electromagnetic Compatibility, EMC) 성능이 저하될 수 있다. 시험기는 필요한 실드 종단점과 드레인 연결 상태를 검증할 수 있지만, 상세한 전자기 적합성 효과에 대한 평가는 별도의 전자기 적합성 검증(EMC Validation) 활동에서 수행한다.

다이오드(Diode), 저항기(Resistor), 서지 억제 소자(Suppression Device) 또는 기타 내장형 전기 부품(Embedded Electrical Component)을 포함하는 하니스에는 일반 배선과 해당 부품의 전기적 동작을 구별할 수 있는 시험 방법이 필요하다. 극성 의존형 소자(Polarity-Sensitive Element)는 양방향 측정이 필요할 수 있으며, 저항성 부품은 정의된 저항값 범위(Value Window)를 적용해야 한다. 따라서 시험 프로그램은 물리적인 연결 관계뿐만 아니라 하니스 어셈블리(Harness Assembly)에 포함된 부품의 예상 전기 특성까지 표현해야 한다.

안전 관련 하니스(Safety-Related Harness) 또는 고전압 하니스(High-Voltage Harness)의 경우 전용 시험기를 추가적인 절연 시험(Insulation Test) 또는 내전압 시험(Dielectric Test) 장비와 통합할 수 있지만, 이러한 기능은 일반적인 저전압 도통 시험(Low-Voltage Continuity Test)과 명확하게 구분되어야 한다. 스위칭 구조(Switching Architecture), 치구, 커넥터 및 작업자 보호 기능은 인가되는 시험 전압에 적합해야 한다. 자동 인터록(Automated Interlock)은 전압이 인가된 인터페이스에 작업자가 접근하는 것을 방지하고, 취급 전에 저장된 전기 에너지가 안전하게 방전되도록 할 수 있다.

시험 순서(Test Sequence)는 단순한 합격(PASS) 또는 불합격(FAIL) 결과만 제공하는 것이 아니라 고장 진단에 유용한 정보를 제공하도록 설계되어야 한다. 유용한 고장 기록(Failure Record)은 문제가 발생한 커넥터, 캐비티, 예상 목적지, 실제 측정 상태 및 적용된 허용 한계를 식별한다. 예를 들어 시험기는 정의된 두 핀 사이의 개방 회로, 서로 관련되지 않은 회로 사이의 비정상 연결, 또는 전력 도체에서 허용 기준을 초과한 저항을 구체적으로 보고할 수 있다.

이러한 진단 기능(Diagnostic Capability)은 제조 재작업(Manufacturing Rework)을 직접적으로 지원한다. 고장 발생 후 전체 하니스를 수동으로 추적하는 대신 기술자는 보고된 네트워크와 연관된 특정 커넥터, 스플라이스, 분기 또는 도체를 집중적으로 검사할 수 있다. 수리 후에는 일반적으로 수리된 회로만 다시 검사하는 것이 아니라 전체 시험을 반복해야 한다. 전체 재시험(Full Retest)은 취급이나 재작업 과정에서 하니스의 다른 부분에 새로운 결함이 발생하지 않았는지를 확인하는 데 도움이 된다.

생산 환경에서 운용하기 위해서는 시험기 자체에 대한 주기적인 검증(Periodic Verification)도 필요하다. 정상 상태가 확인된 기준 하니스(Known-Good Reference Harness), 루프백 치구(Loopback Fixture), 교정된 저항 표준(Calibrated Resistance Standard), 전용 자체 시험 어댑터(Self-Test Adapter)를 이용하여 시험 채널의 동작과 측정 정확도를 확인할 수 있다. 시험기 검증을 통해 손상된 치구 배선, 마모된 접점, 고장 난 스위칭 채널 또는 측정 드리프트(Measurement Drift)를 생산 결과에 영향을 주기 전에 발견해야 한다.

하니스의 복잡성이 증가할수록 측정 시스템 무결성(Measurement System Integrity)의 중요성도 증가한다. 현대 로봇 전기 아키텍처(Robotic Electrical Architecture)는 배터리 전력, 모터 인터페이스, 안전 회로, 센서, CAN 또는 CAN FD 네트워크, 이더넷(Ethernet), 직렬 통신(Serial Communication), 보조 입출력(Auxiliary I/O)을 서로 연관된 하니스 어셈블리에 함께 구성할 수 있다. 전용 시험기는 민감한 인터페이스에 부적절한 신호를 인가하거나 통신 토폴로지(Communication Topology)를 일반적인 포인트 투 포인트 배선으로 잘못 해석하지 않으면서 제조 연결 상태를 검증해야 한다.

추적성(Traceability)이 요구되는 경우 시험 결과는 제조 품질 기록(Manufacturing Quality Record)으로 저장되어야 한다. 일반적인 기록에는 하니스 식별 정보, 리비전, 시험기 식별 정보, 시험 프로그램 버전, 작업자 또는 시험 스테이션 정보, 시험 실행 시간, 측정값, 고장 상세 정보, 재작업 상태 및 최종 판정(Final Disposition)이 포함된다. 이러한 기록을 일련번호 또는 생산 로트(Production Lot) 정보와 연결하면 향후 현장에서 발생하는 고장을 제조 이력과 연계하여 분석할 수 있다.

수집된 시험기 데이터(Tester Data)는 통계적 공정 개선(Statistical Process Improvement)에도 활용할 수 있다. 특정 단자 위치에서 개방 회로가 반복적으로 발생한다면 압착, 삽입 또는 커넥터 취급 문제를 의미할 수 있으며, 특정 분기에서 단락이 반복된다면 조립 보드(Assembly Board) 또는 배선 경로(Routing)의 문제일 가능성이 있다. 따라서 고장 추세(Failure Trend)를 커넥터, 회로, 작업 스테이션, 하니스 리비전, 공급업체 로트(Supplier Lot), 생산 기간별로 분석하면 각각의 결함을 개별적으로 처리하는 수준을 넘어 체계적인 원인을 식별할 수 있다.

궁극적으로 전용 하니스 시험기(Dedicated Harness Tester)는 하니스 제조와 상위 수준 전기 시스템 통합(Electrical System Integration) 사이에서 제조 품질 게이트(Manufacturing Gate)의 역할을 수행한다. 그 목적은 완성된 로봇의 모든 기능적 동작을 검증하는 것이 아니라, 전기적 상호 연결 구조(Electrical Interconnection Structure)가 관리된 설계 정의에 따라 정확하게 제조되었음을 입증하는 것이다. 신뢰성 있는 도통, 절연(Isolation), 핀 매핑(Pin Mapping), 저항 검증, 형상 관리, 고장 진단 및 추적 가능한 기록은 시스템 통합 단계의 결함을 줄이고 이후의 시스템 검증(System Validation)을 위한 신뢰할 수 있는 기반을 제공한다.

## 02.02. Layout Board Inspection

![](images/image2.png){width="7.268055555555556in" height="7.268055555555556in"}

레이아웃 보드 검사(Layout Board Inspection)는 와이어링 하니스(Wire Harness)가 전기 시험(Electrical Testing)이나 시스템 장착 단계로 넘어가기 전에 승인된 물리적 설계 정의(Physical Definition)에 따라 조립되었는지를 확인하기 위한 체계적인 제조 검증 절차(Manufacturing Verification Process)이다. 하니스는 의도된 배선 경로(Routing), 분기 위치(Branch Location), 커넥터 위치(Connector Position), 분기점(Breakout Point), 치수 관계(Dimensional Relationship)를 재현한 전용 레이아웃 보드(Layout Board), 폼 보드(Form Board) 또는 조립 치구(Assembly Fixture)에 배치된다.

전용 하니스 시험기(Dedicated Harness Tester)가 주로 전기적 연결성(Electrical Connectivity)과 저항 관련 특성(Resistance-Related Characteristics)을 검증하는 것과 달리, 레이아웃 보드 검사는 제작된 하니스의 물리적 정확성(Physical Correctness)에 초점을 둔다. 하니스가 도통 시험(Continuity Testing)을 통과하더라도 잘못된 분기 길이, 부적절한 커넥터 위치, 불충분한 보호재, 과도한 꼬임 또는 잘못된 배선 형상을 포함할 수 있다. 따라서 물리적 검사는 전기적 검증을 보완하며 독립적인 제조 품질 게이트(Manufacturing Quality Gate)를 제공한다.

레이아웃 보드는 일반적으로 관리되는 하니스 도면(Harness Drawing), 치수 사양(Dimensional Specification), 커넥터 정의(Connector Definition), 제조 문서(Manufacturing Documentation)를 기반으로 개발된다. 치구(Fixture), 핀(Pin), 커넥터 홀더(Connector Holder), 배선 가이드(Routing Guide), 기준 표시(Reference Marking)는 핵심 형상을 재현하여 조립된 하니스를 기준 형상(Nominal Configuration)과 직접 비교할 수 있도록 한다. 보드는 설치성, 커넥터 접근성, 굽힘 거동, 장력(Strain), 대상 로봇이나 기계와의 호환성에 영향을 미치는 치수를 표현해야 한다.

검사 과정에서 하니스는 과도한 인장, 압축 또는 인위적인 변형 없이 정의된 배선 경로에 배치되어야 한다. 각각의 분기는 자연스럽게 지정된 치구 위치에 도달해야 하며, 커넥터는 와이어 번들(Wire Bundle)을 억지로 당기지 않고 해당 홀더에 결합되어야 한다. 하니스를 늘려야만 보드 형상에 맞출 수 있다면 분기 길이가 부족할 가능성이 있으며, 지나치게 많은 여유 길이는 구간이 너무 길거나 분기점 위치가 잘못되었음을 나타낼 수 있다.

전체 하니스 길이와 개별 분기 치수는 중요한 검사 항목이다. 치수 공차(Dimensional Tolerance)는 제조 편차를 허용하면서도 최종 시스템에 정상적으로 장착될 수 있도록 충분히 관리되어야 한다. 측정 항목에는 커넥터 간 거리, 분기점 위치, 분기 길이, 노출 도체 길이, 보호재 종단 위치 및 기타 설계별 치수가 포함될 수 있다. 합격 기준(Acceptance Criteria)은 작업자의 주관적인 판단이 아니라 해당 하니스 문서에 의해 정의되어야 한다.

커넥터 방향(Connector Orientation) 역시 검증해야 한다. 정확한 전기적 핀 매핑(Pin Mapping)이 올바른 기계적 방향까지 보장하는 것은 아니기 때문이다. 커넥터 클로킹(Connector Clocking), 극성(Polarization), 래치 방향(Latch Direction), 백셸 방향(Backshell Orientation), 스트레인 릴리프 방향(Strain-Relief Direction), 케이블 인출 각도(Cable Exit Angle)는 하니스가 비틀림이나 간섭 없이 설치될 수 있는지를 결정한다. 레이아웃 보드는 이러한 방향 특성을 일관되게 검사할 수 있는 기계적 기준(Mechanical Reference)을 제공한다.

분기점(Breakout Point)은 메인 번들(Main Bundle)이 서로 다른 장치로 연결되는 여러 분기로 나뉘는 위치를 결정하므로 특별한 주의가 필요하다. 잘못된 분기점 위치는 커넥터에 장력을 발생시키거나 주변 부품과 간섭하거나 설치 과정에서 하니스가 의도하지 않은 굽힘 반경(Bend Radius)을 갖도록 만들 수 있다. 검사자는 관리된 제조 정의에 따라 분기점 위치, 분기 방향, 번들 전환부(Bundle Transition), 관련 보호 구조를 확인해야 한다.

검사에서는 보호 재료(Protective Material)가 올바른 위치에 존재하며 적절한 범위로 적용되었는지도 확인해야 한다. 여기에는 주름관(Corrugated Tubing), 편조 슬리브(Braided Sleeving), 섬유 테이프(Textile Tape), 열수축 튜브(Heat-Shrink Tubing), 전선관(Conduit), 모서리 보호재(Edge Protection), 국부 보강재(Localized Reinforcement) 등이 포함될 수 있다. 이러한 재료는 기계적 보호, 환경 내구성, 번들 고정, 소음 저감, 변형 관리 등의 목적으로 사용되므로 잘못된 위치에 적용되면 초기 전기 성능이 정상이라도 장기적인 하니스 내구성이 저하될 수 있다.

클립(Clip), 클램프(Clamp), 그로밋(Grommet), 리테이너(Retainer) 및 기타 고정 부품도 올바른 종류, 수량, 위치 및 방향으로 설치되었는지 검사해야 한다. 이러한 부품은 하니스가 최종 제품과 기계적으로 결합되는 방식을 결정하며 진동, 움직임, 간극(Clearance), 하중 전달(Load Transfer)을 제어하는 경우가 많다. 잘못 배치된 클립은 실제 장착 시 배선 경로를 크게 변화시킬 수 있으며, 그로밋이 누락되면 하니스가 패널이나 구조물의 개구부를 통과하는 위치에서 마모될 수 있다.

하니스가 방향을 변경하는 모든 위치에서는 최소 굽힘 반경(Minimum Bend Radius)과 국부적인 번들 변형(Local Bundle Deformation)을 고려해야 한다. 지나치게 작은 굽힘 반경은 도체 가닥(Conductor Strand)을 손상시키고 실드(Shield)를 변형시키며 절연체(Insulation)에 응력을 발생시키거나 커넥터 및 분기 전환부 주변에서 장기적인 피로(Long-Term Fatigue)를 유발할 수 있다. 따라서 레이아웃 보드는 비현실적으로 급격한 굽힘을 유도해서는 안 되며, 제작된 하니스가 유해한 기계적 응력 없이 의도된 배선 경로를 따라갈 수 있음을 확인할 수 있도록 충분한 형상 기준을 제공해야 한다.

육안 작업 품질 검사(Visual Workmanship Inspection)도 동시에 수행된다. 레이아웃 보드에 하니스가 일정한 형태로 펼쳐지므로 대부분의 영역을 체계적으로 확인할 수 있기 때문이다. 검사자는 손상된 절연체, 절단 흔적, 눌림, 느슨한 테이핑, 노출된 도체, 불완전한 열수축, 이탈된 실(Seal), 손상된 커넥터 하우징(Connector Housing), 부적절하게 고정된 단자, 오염 또는 불균일한 번들 구성을 확인할 수 있다. 의심되는 결함은 기록하고 정의된 작업 품질 요구사항(Workmanship Requirement)에 따라 평가해야 한다.

전선 식별(Wire Identification)과 라벨링(Labeling)도 중요한 검사 항목이다. 하니스 라벨, 커넥터 식별자(Connector Identifier), 분기 마커(Branch Marker), 일련번호(Serial Number), 경고 라벨 및 기타 식별 요소는 해당 도면과 일치해야 하며 설치 이후에도 판독할 수 있어야 한다. 라벨의 방향과 위치는 조립 및 정비 작업을 지원할 수 있어야 한다. 잘못된 식별 정보는 즉각적인 전기적 동작에는 영향을 미치지 않을 수 있지만 이후 제품 수명주기(Product Life Cycle)에서 설치 오류, 정비 실수 또는 형상 혼란(Configuration Confusion)을 유발할 수 있다.

실드 케이블(Shielded Cable), 통신선(Communication Line), 대전류 도체(High-Current Conductor) 또는 안전 관련 회로(Safety-Related Circuit)가 포함된 하니스에서는 물리적 배선 구성이 더욱 중요한 의미를 가질 수 있다. 전력선과 신호선 분기 사이의 이격(Separation), 실드 처리(Shield Treatment), 접지 구성(Grounding Provision), 고에너지 회로 주변의 보호 구조는 설계 의도와 일치해야 한다. 레이아웃 검사는 전자기 적합성(EMC), 절연 또는 기능 시험을 대체하지 않지만 이러한 특성을 확보하기 위해 필요한 물리적 구조가 실제로 구현되었는지를 확인한다.

레이아웃 보드 자체도 생산 치공구(Production Tooling)로서 관리되어야 한다. 치구 위치, 커넥터 홀더, 기준 치수, 검사 표시(Inspection Marking)는 현재 하니스 리비전(Harness Revision)과 일치해야 한다. 마모, 기계적 손상, 치구 위치 변경 또는 승인되지 않은 수정은 정상적인 하니스를 불합격으로 판정하거나 결함이 있는 하니스를 합격시킬 수 있다. 따라서 특히 대량 생산 또는 장기간 생산 프로그램에서는 보드의 핵심 치수를 주기적으로 검증해야 한다.

여러 하니스 변형(Variant)이 유사한 형상을 공유하는 경우에는 형상 관리(Configuration Management)가 특히 중요하다. 선택 사양 분기(Optional Branch), 서로 다른 커넥터 종류, 지역별 구성, 센서 옵션 또는 제품 리비전으로 인해 외관상 거의 동일한 하니스가 만들어질 수 있다. 검사자는 검사 전에 부품 번호(Part Number)와 리비전을 명확하게 확인해야 하며, 잘못된 물리적 기준을 사용하여 합격 판정을 내리지 않도록 이에 대응하는 보드 구성 또는 검사 지침(Inspection Instruction)을 선택해야 한다.

검사 결과는 단순한 육안 합격 판정 이상의 정보를 제공해야 한다. 관련 치수 측정값, 부적합 위치(Nonconforming Location), 결함 분류(Defect Category), 하니스 식별 정보, 보드 또는 치구 식별 정보, 작업자 정보, 검사 날짜 및 최종 판정(Final Disposition)을 제조 품질 이력(Manufacturing Quality History)의 일부로 기록할 수 있다. 품질 절차에서 허용하는 경우 사진을 이용하여 비정상적인 결함, 재작업 상태 또는 특정 형상에 따른 특징을 기록할 수도 있다.

부적합(Nonconformance)이 발견되면 재작업(Rework)을 수행하기 전에 해당 특성을 평가해야 한다. 클립 위치 변경이나 보호 슬리브(Protective Sleeve) 교체는 비교적 간단할 수 있지만, 잘못된 분기 길이를 수정하려면 상당한 수준의 하니스 재제작이 필요할 수 있다. 재작업 이후에는 영향을 받은 물리적 특성을 다시 검사해야 하며, 수리로 인해 영향을 받을 가능성이 있는 전기 시험도 해당 제조 및 검증 절차에 따라 반복해야 한다.

레이아웃 보드 검사는 하니스 설계 및 제조 엔지니어링(Harness Design and Manufacturing Engineering)에 유용한 피드백을 제공할 수도 있다. 설계상 정상인 하니스를 보드에 맞추는 작업에서 반복적인 어려움이 발생한다면 비현실적인 치수 공차, 부적절한 분기점 정의, 잘못된 배선 경로 가정 또는 과도한 제조 편차를 의미할 수 있다. 따라서 반복되는 결함을 분석하면 도면, 치공구, 조립 지침, 부품 선정 및 하니스 자체의 물리적 아키텍처(Physical Architecture)를 개선할 기회를 발견할 수 있다.

로봇 시스템(Robotic System)에서는 배선이 좁은 구조물, 움직이는 어셈블리(Moving Assembly), 센서 장착부, 모터 주변, 배터리 구획 또는 정비 접근 영역(Service-Access Area)을 통과할 수 있기 때문에 하니스의 물리적 정확성이 특히 중요하다. 사소해 보이는 치수 오류도 움직이는 기구와 간섭하거나 정비 작업을 방해하고, 커넥터 하중을 증가시키거나 하니스를 마모에 노출시킬 수 있다. 레이아웃 검증(Layout Verification)은 이러한 제조 편차가 시스템 수준의 통합 문제로 확대되기 전에 발견하도록 한다.

궁극적으로 레이아웃 보드 검사(Layout Board Inspection)는 제작된 하니스가 관리된 설계 정의(Controlled Design Definition)에서 요구하는 물리적 형상과 작업 품질(Workmanship)을 갖추고 있음을 확인하는 과정이다. 전용 하니스 시험(Dedicated Harness Testing), 압착 검증(Crimp Verification), 필요한 경우의 고전압 시험(High-Voltage Testing), 자동화 검사(Automated Inspection)와 함께 사용될 때 전체 하니스 검증 프로세스(Harness Validation Process)의 일부를 구성한다. 전기적 정확성(Electrical Correctness)과 물리적 정확성(Physical Correctness)은 상호 보완적인 요구사항이며, 하니스가 신뢰성 있는 시스템 통합(System Integration)에 투입되기 전에 두 가지 모두 검증되어야 한다.

## 02.03. Crimp Pull Test

![](images/image3.png){width="7.268055555555556in" height="7.268055555555556in"}

압착 인장 시험(Crimp Pull Test)은 전기 도체(Electrical Conductor)와 압착 단자(Crimped Terminal) 사이 연결부의 강도와 일관성을 평가하기 위한 기계적 검증 방법(Mechanical Verification Method)이다. 와이어링 하니스(Wire Harness) 제조에서는 압착 공정(Crimping Process)이 충분한 기계적 유지력(Mechanical Retention)을 확보했는지를 직접적으로 검증한다. 이 시험은 전기적으로 도통되더라도 기계적 강도가 부족한 연결이 존재할 수 있기 때문에 전기적 도통 시험(Electrical Continuity Test)과 육안 검사(Visual Inspection)를 보완한다.

기본적인 시험 원리는 전선과 압착 단자 사이에 제어된 인장력(Tensile Force)을 가하여 규정된 허용 힘에 도달하거나 연결부가 분리될 때까지 하중을 증가시키는 것이다. 측정된 힘은 도체 압착부(Conductor Crimp)의 기계적 유지 능력을 나타낸다. 일반적으로 시험은 인장 하중을 지속적으로 측정하면서 제어된 속도로 힘을 가할 수 있는 전용 인장력 시험기(Pull-Force Tester)를 사용하여 수행한다.

일반적인 시험 시편(Test Specimen)은 평가 대상이 되는 실제 생산용 전선, 단자 및 압착 구성(Crimp Configuration)으로 이루어진다. 전선 크기, 도체 재질, 소선 구조(Strand Construction), 절연체 종류, 단자 부품 번호, 도금(Plating), 압착 형상(Crimp Geometry)은 모두 측정 결과에 영향을 미칠 수 있다. 따라서 모든 하니스 연결에 하나의 보편적인 인장력 요구사항을 적용하기보다는 특정 전선-단자 조합(Wire-Terminal Combination)에 대응하는 합격 기준(Acceptance Criteria)을 사용해야 한다.

시험 전에 시편이 의도된 생산 구성(Production Configuration)을 정확하게 대표하는지 검사해야 한다. 도체는 적절하게 탈피(Stripping)되어야 하고, 소선이 의도하지 않게 절단되거나 누락되어서는 안 되며, 단자는 요구되는 도체 압착부(Conductor Crimp)와 절연체 압착부(Insulation Crimp) 형상을 가져야 한다. 명백한 준비 과정의 손상이 있는 시편을 시험하면 정상적인 압착 공정 능력을 정확하게 나타내지 못하는 잘못된 결과가 발생할 수 있다.

시편은 단자가 적절한 치구(Fixture)에 견고하게 고정되고 전선이 인장 방향과 정렬되도록 장착해야 한다. 정렬 불량(Misalignment)은 굽힘, 비틀림 또는 측면 하중(Side Loading)을 발생시켜 측정되는 힘과 파손 거동(Failure Behavior)을 변화시킬 수 있다. 치구는 압착 영역을 손상시키거나 실제 조건과 다른 기계적 이점(Mechanical Advantage)을 발생시키지 않으면서 단자를 안정적으로 고정해야 한다.

인장 하중(Tensile Load)은 충격이나 갑작스러운 당김이 아니라 점진적이고 부드럽게 인가되어야 한다. 제어된 인장 속도(Pull Rate)는 시편 사이의 반복성(Repeatability)을 향상시키며 생산 로트(Production Lot), 공구 및 공정 설정 간의 결과를 의미 있게 비교할 수 있도록 한다. 시험기는 분리 또는 정의된 다른 파손 조건이 발생하기 전에 도달한 최대 힘(Maximum Force)을 기록하며, 이 값을 규정된 최소 인장력 요구사항(Minimum Pull-Force Requirement)과 비교한다.

파손 형태(Failure Mode)는 수치로 측정된 힘만큼 중요하다. 도체가 압착 배럴(Crimp Barrel)에서 빠져나오거나, 개별 소선이 미끄러지거나 파단될 수 있으며, 전선이 압착부 외부에서 끊어지거나 단자 자체가 변형될 수도 있다. 시편이 어떠한 방식으로 파손되었는지를 기록하면 압착 압력 부족과 도체 강도 문제, 잘못된 탈피, 단자 손상, 재료 편차 또는 부적절한 시험 설정을 구분하는 데 도움이 된다.

도체가 낮은 힘에서 단순히 압착 배럴에서 빠져나오는 현상은 일반적으로 단자와 도체 사이의 기계적 결합(Mechanical Engagement)이 부족함을 의미한다. 가능한 원인으로는 과도한 압착 높이(Crimp Height), 잘못된 공구(Tooling), 불충분한 압축, 부적절한 단자 선정 또는 잘못된 도체 위치가 있다. 따라서 측정된 힘을 독립적인 숫자로만 판단해서는 안 되며 파손된 시편의 물리적 상태와 함께 해석해야 한다.

압착 높이(Crimp Height)는 인장 시험 성능과 밀접하게 관련되며 일반적으로 별도의 공정 특성(Process Characteristic)으로 관리해야 한다. 압착 높이가 지나치게 크면 압축력이 부족하여 유지력이 떨어질 수 있으며, 지나치게 작으면 도체 소선을 손상시키거나 단자에 과도한 응력을 가할 수 있다. 인장 시험은 기계적 성능을 검증하고, 치수 검사(Dimensional Inspection)는 압착 공정이 의도된 성형 범위(Forming Window) 내에서 유지되고 있는지를 판단하는 데 도움을 준다.

전선 탈피 품질(Wire Stripping Quality) 역시 시험 결과에 큰 영향을 미친다. 탈피 길이(Strip Length)가 너무 짧으면 도체가 압착부에 충분히 삽입되지 않을 수 있으며, 지나치게 길면 의도된 배럴 영역 외부에 도체가 노출될 수 있다. 흠집이 생기거나 절단된 소선은 유효 도체 단면적(Effective Conductor Cross-Section)을 감소시키고 조기 파단(Premature Fracture)을 유발할 수 있다. 따라서 예상하지 못한 인장 시험 불합격이 발생하면 탈피 길이와 소선 상태를 함께 검사해야 한다.

절연체 압착부(Insulation Crimp)는 도체 압착부(Conductor Crimp)와 혼동해서는 안 된다. 절연체 압착부의 주요 목적은 일반적으로 전기적 연결을 형성하는 것이 아니라 스트레인 릴리프(Strain Relief)를 제공하고 절연된 전선을 기계적으로 지지하는 것이다. 적용되는 시험 방법에 따라 측정된 힘이 절연체의 추가적인 유지력이 아니라 도체 압착부 자체의 유지력을 나타내도록 절연체 지지 효과를 제거하거나 적절하게 처리해야 할 수 있다.

압착 인장 시험은 시편에 정의된 하중 한계까지 힘을 가하거나 파손될 때까지 시험하기 때문에 일반적으로 파괴 시험(Destructive Test)에 해당한다. 따라서 생산 관리(Production Control)에서는 모든 하니스의 모든 단자를 시험하는 대신 대표 시편(Representative Sample)을 이용하는 경우가 일반적이다. 샘플링 빈도(Sampling Frequency)는 생산량, 공정 능력(Process Capability), 공구 상태, 단자 및 전선 변경, 품질 요구사항, 해당 전기 연결의 중요도를 고려하여 결정해야 한다.

압착 공정이 최초로 구축되거나 변경되는 경우 인장 시험은 특히 중요한 검증 수단이 된다. 새로운 어플리케이터(Applicator), 다이(Die), 단자, 전선 공급업체, 도체 크기, 공구 조정, 유지보수 작업 또는 공정 파라미터(Process Parameter)의 변경은 압착 성능에 영향을 미칠 수 있다. 인장력 검증(Pull-Force Verification)은 정상 생산을 승인하기 전에 변경된 제조 조건에서도 기계적으로 적합한 연결이 계속 생산되는지를 정량적으로 입증한다.

자동 압착 장비(Automated Crimping Equipment)의 경우 인장 시험 결과를 압착 높이, 압착 폭(Crimp Width), 도체 위치, 공구 설정 및 장비 파라미터를 포함하는 보다 광범위한 공정 모니터링(Process Monitoring)의 일부로 활용할 수 있다. 하나의 측정 항목만으로는 압착 품질을 완전하게 평가할 수 없다. 기계적 인장 강도와 치수 검사 및 육안 검사를 결합하면 단자 접속 공정(Termination Process)이 안정적이고 충분한 공정 능력을 유지하고 있는지를 더욱 신뢰성 있게 판단할 수 있다.

시험 장비 자체도 유지관리 및 검증되어야 한다. 하중 측정 시스템(Load Measurement System)은 평가되는 힘에 적합한 측정 범위, 분해능(Resolution), 정확도(Accuracy)를 가져야 하며 교정 상태(Calibration Status)가 관리되어야 한다. 그립(Grip)과 단자 치구도 마모 또는 손상 여부를 검사해야 한다. 관리가 불량한 치구에서는 시편 미끄러짐이 발생하거나 의도하지 않은 하중이 추가되어 하중 센서가 정상적으로 작동하더라도 잘못된 측정 결과가 발생할 수 있다.

인장 시험을 제조 품질 관리(Manufacturing Quality Control)에 사용하는 경우 추적성(Traceability)이 중요하다. 기록에는 전선 종류와 크기, 단자 부품 번호, 압착기 또는 어플리케이터 식별 정보, 공구 설정, 시편 식별 정보, 측정된 인장력, 요구되는 최소값, 파손 형태, 작업자, 시험 장비 식별 정보, 시험 날짜 및 최종 판정(Final Disposition)이 포함될 수 있다. 이러한 기록을 통해 시험 결과를 특정 생산 조건과 연계할 수 있다.

반복적으로 측정된 결과를 통계적으로 분석하면 개별 시편이 합격 기준 이하로 떨어지기 전에 점진적인 공정 성능 저하(Process Deterioration)를 발견할 수 있다. 인장력이 지속적으로 감소하는 추세는 공구 마모, 압착 높이 변화, 도체 편차, 단자 편차 또는 장비 조정 문제를 의미할 수 있다. 따라서 통계적 모니터링(Statistical Monitoring)을 적용하면 인장 시험을 단순한 합격 또는 불합격 검사에서 제조 공정 안정성(Manufacturing Process Stability)을 나타내는 유용한 지표로 확장할 수 있다.

시편이 규정된 요구사항을 충족하지 못하면 개별 시편을 불합격 처리하는 것만으로 대응해서는 안 된다. 영향을 받을 가능성이 있는 생산 범위(Production Range)를 식별하고 압착 공정을 조사하며 관련 공구, 재료, 설정 파라미터 및 이전 품질 기록을 검토해야 한다. 시정 조치(Corrective Action)에는 공구 조정, 유지보수, 재료 교체, 추가 샘플링 또는 잠재적으로 영향을 받은 하니스의 격리(Containment)가 포함될 수 있다.

시정 조치 이후에는 대표 시편을 다시 시험하여 적절한 기계적 유지력이 회복되었음을 입증해야 한다. 문제의 특성에 따라 추가적인 압착 높이 측정, 육안 검사, 전기 저항 검증(Electrical Resistance Verification) 또는 하니스 수준 시험(Harness-Level Testing)이 필요할 수도 있다. 목적은 단순히 하나의 합격 결과를 얻는 것이 아니라 근본적인 제조 공정이 다시 관리된 상태(Controlled Condition)로 복귀했음을 확인하는 것이다.

로봇 시스템(Robotic System)에서는 하니스가 지속적인 진동, 반복적인 가속, 이동 플랫폼의 충격, 열 사이클링(Thermal Cycling), 케이블 움직임 및 정비 과정의 취급에 노출될 수 있기 때문에 신뢰성 있는 압착 연결이 특히 중요하다. 모터, 배터리, 안전 장치, 센서, 제어기 및 통신 장비에 연결되는 접속부는 이러한 조건에서도 전기적·기계적 무결성(Electrical and Mechanical Integrity)을 유지해야 한다. 약한 압착부는 하니스가 초기 도통 시험을 통과한 이후에도 장기간 사용 중 간헐적 고장(Intermittent Fault)을 발생시킬 수 있다.

따라서 압착 인장 시험(Crimp Pull Test)은 전체 하니스 시험 체계(Harness Test Structure)에서 단자 접속 작업 품질(Termination Workmanship)을 집중적으로 검증하는 방법으로 기능한다. 전용 하니스 시험(Dedicated Harness Testing), 레이아웃 보드 검사(Layout Board Inspection), 필요한 경우의 고전압 하니스 시험(High-Voltage Harness Testing), 하니스 시험 자동화(Harness Test Automation)와 함께 적용함으로써 제작된 전기적 상호 연결(Electrical Interconnection)이 전기적으로 정확할 뿐만 아니라 기계적으로도 견고하다는 것을 검증하는 데 기여한다.

## 02.04. HV Harness Test

![](images/image4.png){width="7.268055555555556in" height="7.268055555555556in"}

고전압 하니스 시험(HV Harness Test)은 고전압 와이어링 하니스(HV Wire Harness)가 신뢰성 있는 운용에 필요한 전기적 무결성(Electrical Integrity), 절연 성능(Insulation Performance), 기계적 구성(Mechanical Configuration), 안전 특성(Safety Characteristics)을 갖도록 제조되었는지를 검증한다. 전체 하니스 시험 체계에서 이 시험은 일반적인 도통 및 작업 품질 검사를 확장하여 절연 결함, 잘못된 연결 또는 불충분한 이격으로 인해 위험 전압 노출, 아크(Arcing), 장비 손상 또는 시스템 정지가 발생할 수 있는 회로를 검증한다.

고전압 하니스(HV Harness)는 일반적으로 배터리(Battery), 전력 분배 장치(Power Distribution Unit), 접촉기(Contactor), 인버터(Inverter), 모터 드라이브(Motor Drive), 직류-직류 변환기(DC-DC Converter), 충전기(Charger) 또는 기타 고에너지 장비를 연결한다. 이러한 회로는 일반적인 신호 배선보다 훨씬 높은 전압과 전류를 전달할 수 있으므로 제조 결함을 더욱 엄격하게 검출해야 한다. 따라서 시험 전략은 전기적 연결성 검증과 절연 관련 측정 및 통제된 안전 절차를 결합한다.

시험은 하니스 부품 번호(Part Number), 리비전(Revision), 전압 등급(Voltage Class), 커넥터 구성(Connector Configuration), 적용되는 시험 사양(Test Specification)을 명확하게 식별하는 것에서 시작해야 한다. 서로 다른 변형 하니스가 유사한 커넥터를 사용하면서도 핀 할당이나 절연 요구사항이 다를 수 있기 때문에 선택된 시험 프로그램(Test Program)은 정확한 생산 구성과 일치해야 한다. 형상 관리(Configuration Control)는 잘못된 하니스 정의로 인해 오해를 유발하는 합격(PASS) 결과가 발생하는 것을 방지한다.

높은 시험 전압을 인가하기 전에 육안 검사(Visual Inspection)를 수행해야 한다. 검사자는 커넥터 하우징(Connector Housing), 고전압 단자(HV Terminal), 실(Seal), 케이블 절연체(Cable Insulation), 보호 피복(Protective Covering), 실드(Shielding), 스트레인 릴리프(Strain Relief), 분기 전환부(Branch Transition), 라벨(Label), 그리고 적용되는 경우 인터록 관련 부품(Interlock-Related Component)을 확인해야 한다. 절단, 눌린 절연체, 노출된 도체, 불완전한 커넥터 조립, 오염 또는 손상된 실은 전압을 인가하는 시험 전에 수정되어야 한다.

도통 시험(Continuity Testing)은 각각의 고전압 도체가 올바른 소스(Source)와 목적지(Destination) 단자 사이에 연결되어 있는지를 확인한다. 측정 저항은 도체 길이, 단면적, 단자 시스템 및 연결 아키텍처에 대해 규정된 허용 범위 내에 있어야 한다. 과도한 저항은 불완전한 압착, 손상된 도체 소선, 제대로 안착되지 않은 단자, 불량 접합부 또는 실제 부하 조건에서 전압 강하와 국부 발열을 일으킬 수 있는 기타 상태를 나타낼 수 있다.

정확한 핀 매핑(Pin Mapping) 역시 중요하다. 전기적으로 도통되는 도체라도 잘못된 단자에 연결되어 있을 수 있기 때문이다. 시험 시스템은 실제 하니스 연결 상태를 관리된 배선 정의(Wiring Definition)와 비교하여 교차된 도체(Crossed Conductor), 반대로 연결된 회로, 잘못된 분기 할당 및 의도하지 않은 전기적 경로를 검출해야 한다. 직류 전력 회로(DC Power Circuit)에서는 하니스가 배터리나 전력 전자장치(Power Electronics)에 연결될 때 극성 오류(Polarity Error)가 특히 심각한 문제를 발생시킬 수 있다.

절연 저항 시험(Insulation Resistance Test)은 서로 전기적으로 절연되어야 하는 도체가 상호 간 그리고 실드, 섀시(Chassis) 또는 기타 정의된 기준점으로부터 충분한 절연 상태를 유지하는지를 평가한다. 제어된 직류 시험 전압(DC Test Voltage)을 인가하고 이에 따른 누설 특성(Leakage Behavior)을 측정한다. 낮은 절연 저항은 손상된 절연체, 오염, 수분, 도전성 이물질(Conductive Debris), 잘못된 조립 또는 도전성 요소 사이의 불충분한 이격을 의미할 수 있다.

적용되는 하니스 사양에서 정상 운전 조건보다 높은 전압에서의 검증을 요구하는 경우 내전압 시험(Dielectric Withstand Test)이 필요할 수 있다. 이 시험의 목적은 절연 시스템(Insulation System)이 절연 파괴(Breakdown), 섬락(Flashover) 또는 과도한 누설 없이 규정된 전기적 스트레스를 견딜 수 있음을 입증하는 것이다. 시험 전압, 시험 시간, 전압 상승 특성(Ramp Behavior), 전류 제한(Current Limit), 합격 기준은 임의로 결정해서는 안 되며 해당 엔지니어링 또는 검증 요구사항에 따라 정의되어야 한다.

내전압 시험(Dielectric Test)은 절연 저항 측정(Insulation Resistance Measurement)과 구분해야 한다. 절연 저항 시험은 정의된 직류 조건에서 절연 시스템의 저항을 특성화하는 반면, 내전압 시험은 규정된 높은 전압을 절연 시스템에 인가하여 절연 파괴가 발생하지 않는지를 검증한다. 두 시험 모두 고전압 하니스 검증에 적용될 수 있지만 서로 다른 정보를 제공하며 각각에 적합하게 구성된 시험 장비가 필요하다.

실드 및 접지 기능(Shielding and Grounding Feature)이 하니스 설계에 포함되어 있는 경우 이들 역시 검증해야 한다. 고전압 케이블에는 전자기 간섭(Electromagnetic Interference)을 제어하기 위한 편조 실드(Braided Shield), 포일 실드(Foil Shield), 드레인 경로(Drain Path), 실드 종단 하드웨어(Shield Termination Hardware) 또는 도전성 커넥터 구조가 포함될 수 있다. 시험에서는 실드 연결성을 고전압 도체의 절연 요구사항과 혼동하지 않으면서 이러한 구조에 요구되는 전기적 도통 상태를 확인해야 한다.

고전압 인터록 루프(High-Voltage Interlock Loop)가 커넥터 또는 하니스 아키텍처에 포함되어 있는 경우 전력 도체와 독립적으로 그 도통 상태와 배선 경로를 검증해야 한다. 인터록 회로(Interlock Circuit)는 시스템 수준에서 고전압 인터페이스가 분리되거나 제대로 결합되지 않은 상태를 감지하는 데 활용될 수 있다. 따라서 하니스 시험에서는 인터록 경로가 의도된 커넥터 구성과 일치하며 단선되거나 우회되거나 잘못 배선되지 않았는지를 확인해야 한다.

주요 시험 목적이 전기적 검증이라 하더라도 기계적 상태(Mechanical Condition)는 여전히 중요하다. 고전압 케이블은 일반적으로 더 큰 도체 단면적, 두꺼운 절연층, 실드층 및 제한된 굽힘 요구사항을 갖는다. 커넥터 인출부 주변에서 과도한 굽힘, 비틀림, 압축 또는 인장이 발생하면 내부 구조가 손상되거나 장기적인 내구성이 저하될 수 있다. 따라서 레이아웃 및 작업 품질 검사(Layout and Workmanship Inspection)는 전압이 인가되는 전기 시험을 보완해야 한다.

시험 치구(Test Fixture)와 어댑터(Adapter)는 최대 시험 조건에 적합한 정격 전압(Voltage Rating)을 가져야 한다. 치구 커넥터, 스위칭 장치(Switching Device), 케이블, 절연 장벽(Insulation Barrier), 측정 채널은 시험 시스템에서 가장 취약한 절연 지점이 되어서는 안 된다. 치구 자체의 누설이나 오염이 하니스 불량으로 잘못 판단될 수 있으며, 치구 절연이 불충분하면 내전압 시험 중 실제 전기적 위험을 발생시킬 수 있다.

작업자 보호(Operator Protection)는 고전압 시험의 기본적인 요구사항이다. 장비 특성에 따라 보호 치구(Guarded Fixture), 커버(Cover), 인클로저(Enclosure) 또는 인터록 시험 스테이션(Interlocked Test Station)을 사용하여 전압이 인가된 단자에 접근하지 못하도록 해야 한다. 보호 조건이 충족되지 않으면 시험 전압이 인가되지 않도록 시험 순서를 구성해야 하며, 인터록이 열리거나 비정상적인 상태가 검출되면 전압 인가 상태가 자동으로 종료되어야 한다.

시험 전압을 제거한 이후에도 저장된 전기 에너지(Stored Electrical Energy)를 고려해야 한다. 케이블 정전용량(Cable Capacitance), 시험기 회로, 필터 및 연결된 부품에는 시험 종료 이후 일정 시간 동안 전하가 남아 있을 수 있다. 제어된 방전 기능(Controlled Discharge Function)을 통해 치구를 열거나 하니스를 취급하기 전에 잔류 전압(Residual Voltage)을 안전한 수준으로 낮춰야 한다. 특히 높은 내전압 시험 전압을 사용하는 경우 방전 완료 확인이 중요하다.

자동화된 시험 순서(Automated Sequencing)는 안전성과 반복성을 모두 향상시킬 수 있다. 제어된 고전압 하니스 시험 스테이션(HV Harness Test Station)은 제품을 식별하고, 치구 상태를 확인하며, 저전압 도통 시험을 수행하고, 절연 관련 측정을 실행하고, 허용 한계를 평가한 후 시험 회로를 방전하고 최종 결과를 기록할 수 있다. 또한 높은 전압을 사용하는 시험보다 위험도가 낮은 검사를 먼저 수행하면 명백한 배선 결함을 사전에 발견하여 불필요한 고전압 스트레스가 가해지는 것을 방지할 수 있다.

고장 정보(Failure Information)는 단순한 불합격(FAIL) 표시만 제공하는 것이 아니라 문제가 발생한 전기적 경로와 부적합 유형(Nonconformance Type)을 식별해야 한다. 유용한 진단 정보에는 전력 도체 단선, 과도한 도체 저항, 예상하지 않은 교차 연결, 극성 오류, 낮은 절연 저항, 과도한 누설, 절연 파괴, 실드 단선(Shield Discontinuity), 인터록 고장 등이 포함될 수 있다. 상세한 진단 정보는 효율적인 격리(Containment)와 재작업(Rework)을 지원한다.

절연 또는 내전압 시험에서 불합격한 경우 이를 단순한 배선 수리 문제로 처리해서는 안 된다. 고장의 원인은 손상된 케이블 절연체, 오염된 커넥터 캐비티(Connector Cavity), 잘못 설치된 실, 도전성 이물질, 과도한 기계적 스트레스, 불량 시험 치구 또는 부적절한 시험 설정일 수 있다. 따라서 불합격한 하니스가 생산 공정으로 복귀하기 전에 해당 어셈블리와 시험 장비를 체계적으로 조사해야 한다.

재작업된 고전압 하니스는 수리로 인해 영향을 받을 가능성이 있는 특성에 따라 다시 시험해야 한다. 단자 교체는 도통, 저항, 실링(Sealing), 절연 검증을 요구할 수 있으며 케이블 절연체를 수리한 경우에는 보다 광범위한 평가가 필요할 수 있다. 재작업이 하나의 독립된 연결부만이 아니라 여러 전기적 또는 기계적 특성에 영향을 줄 수 있다면 전체 재시험(Complete Retest)이 적절할 수 있다.

시험 장비는 교정(Calibration) 및 주기적인 검증(Periodic Verification) 상태로 유지되어야 한다. 저항 측정 채널, 절연 저항 기능, 고전압 전원(High-Voltage Source), 누설 전류 측정(Leakage-Current Measurement), 전압 모니터링, 인터록 및 방전 회로는 적용되는 장비 관리 절차에 따라 점검해야 한다. 기준 장치(Reference Device) 또는 전용 검증 치구(Verification Fixture)를 사용하면 생산 하니스를 평가하기 전에 장비가 정상적으로 작동하는지를 확인할 수 있다.

추적성(Traceability)은 각각의 시험 결과를 특정 하니스 및 시험 구성과 연결해야 한다. 기록에는 하니스 일련번호(Serial Number), 부품 번호, 리비전, 시험기 식별 정보, 치구 식별 정보, 시험 프로그램 버전, 측정 저항, 절연 측정값, 내전압 시험 조건, 고장 정보, 작업자, 시험 날짜, 재작업 상태 및 최종 판정(Final Disposition)이 포함될 수 있다. 이러한 기록은 합격된 각각의 하니스가 관리된 제조 요구사항을 충족했다는 근거를 제공한다.

생산 데이터(Production Data)를 통계적으로 분석하면 개별적인 합격 또는 불합격 판단만으로는 명확하게 확인하기 어려운 문제의 발생 추세를 발견할 수 있다. 도체 저항이 증가하는 현상은 단자 또는 압착 상태의 악화를 의미할 수 있으며, 절연 저항이 감소하는 현상은 오염, 재료 손상 또는 치구 열화를 나타낼 수 있다. 따라서 추세 분석(Trend Analysis)은 결함이 광범위하게 확산되기 전에 예방 정비(Preventive Maintenance)와 공정 개선(Process Improvement)을 지원할 수 있다.

로봇 및 자율주행 플랫폼(Robotic and Autonomous Platform)에서 고전압 하니스 신뢰성은 추진(Propulsion), 구동(Actuation), 충전(Charging), 에너지 분배(Energy Distribution), 시스템 가용성(System Availability)에 직접적인 영향을 미친다. 이동 로봇 및 기타 전동 기계는 하니스를 진동, 충격, 반복 운동, 온도 변화, 오염 및 정비 과정의 취급에 노출시킬 수 있다. 따라서 제조 검증에서는 하니스가 이러한 운용 스트레스에 노출되기 전에 견고한 전기적·기계적 기준 상태를 확립해야 한다.

궁극적으로 고전압 하니스 시험(HV Harness Test)은 전체 하니스 검증 프로세스(Harness Validation Process)에서 안전에 중요한 제조 품질 게이트(Safety-Critical Manufacturing Gate)의 역할을 수행한다. 전용 하니스 시험(Dedicated Harness Testing), 레이아웃 보드 검사(Layout Board Inspection), 압착 인장 시험(Crimp Pull Testing), 후속 하니스 시험 자동화(Harness Test Automation)와 함께 적용함으로써 고에너지 전기 연결(High-Energy Electrical Interconnection)이 시스템 통합 전에 올바르게 배선되고, 충분히 절연되며, 기계적으로 적합하고, 추적 가능한 방식으로 검증되었음을 확인한다.

## 02.05. Harness Test Automation

![](images/image5.png){width="7.268055555555556in" height="7.268055555555556in"}

하니스 시험 자동화(Harness Test Automation)는 전기적 검증(Electrical Verification), 치구 제어(Fixture Control), 시험 순서(Test Sequencing), 데이터 수집(Data Acquisition), 결과 평가(Result Evaluation), 제조 추적성(Manufacturing Traceability)을 하나의 통합된 시험 프로세스로 결합한다. 작업자가 개별 측정을 수동으로 수행하는 대신 자동화 시험 스테이션(Automated Test Station)이 각 하니스 구성에 대해 사전에 정의된 절차를 실행한다. 이를 통해 반복성을 향상시키고 작업자 오류를 줄이며 다양한 생산 규모에서도 일관된 품질 관리를 수행할 수 있다.

자동화 프로세스는 시험 대상품(Unit Under Test)을 명확하게 식별하는 것에서 시작한다. 시험을 시작하기 전에 하니스 부품 번호(Part Number), 일련번호(Serial Number), 리비전(Revision), 생산 지시 번호(Production Order), 바코드(Barcode) 또는 기타 식별 정보를 입력하거나 스캔할 수 있다. 제어 소프트웨어(Control Software)는 이 정보를 이용하여 해당 시험 프로그램(Test Program), 기준 넷리스트(Reference Netlist), 허용 한계(Acceptance Limit), 치구 구성(Fixture Configuration)을 선택함으로써 잘못된 하니스 변형에 호환되지 않는 시험 레시피(Test Recipe)가 적용되는 것을 방지한다.

치구 검증(Fixture Verification)은 자동 시험을 수행하기 위한 중요한 사전 조건이다. 시스템은 측정을 시작하기 전에 필요한 어댑터(Adapter), 결합 커넥터(Mating Connector), 스위칭 인터페이스(Switching Interface), 안전 장치(Safety Device)가 올바르게 설치되었는지를 확인해야 한다. 치구 식별 기능(Fixture Identification)을 시험 스테이션에 통합하면 제어기가 하니스, 시험 프로그램 및 물리적 인터페이스 사이의 호환성을 확인할 수 있다. 이를 통해 설정 오류를 줄이고 하니스와 시험 장비를 모두 보호할 수 있다.

자동 도통 시험(Automated Continuity Testing)은 필요한 커넥터 핀을 순차적으로 선택하여 의도된 전기적 경로가 존재하는지를 확인한다. 스위칭 시스템(Switching System)은 수동으로 프로브(Probe)를 이동하지 않고도 지정된 종단점 사이에서 측정 채널을 전환한다. 측정된 저항은 회로별 허용 한계와 자동으로 비교할 수 있으며, 이를 통해 도체 또는 단자 접속 결함과 관련된 개방 회로(Open Circuit), 과도한 저항, 불완전한 연결 및 기타 이상 상태를 식별할 수 있다.

자동화는 의도하지 않은 전기적 연결을 체계적으로 검출할 수도 있다. 시험 매트릭스(Test Matrix)는 관련 핀 조합을 순차적으로 검사하여 단락(Short Circuit), 교차 배선(Crossed Wire), 잘못된 스플라이스(Incorrect Splice) 및 관리된 하니스 정의에 존재하지 않는 기타 전기적 경로를 식별할 수 있다. 이러한 기능은 많은 커넥터와 분기를 포함하는 복잡한 로봇 하니스에서 특히 중요하며, 전체를 수동으로 검사할 때 발생할 수 있는 긴 검사 시간과 작업자의 누락 가능성을 줄여준다.

핀 매핑(Pin Mapping)은 승인된 배선 정의(Wiring Definition)에서 생성된 기준 넷리스트와 실제 측정된 연결 상태를 비교하여 자동으로 평가할 수 있다. 각각의 소스 핀(Source Pin)은 의도된 목적지에 연결되어야 하며 관련 없는 회로와는 절연되어 있어야 한다. 소프트웨어는 교환된 도체(Swapped Conductor), 잘못된 커넥터 캐비티(Wrong Connector Cavity), 잘못된 분기 할당(Incorrect Branch Assignment), 극성 오류(Polarity Error)를 구체적인 커넥터 및 핀 정보와 함께 보고하여 시험 불합격 이후의 문제 해결 시간을 크게 줄일 수 있다.

단순한 도통 기준만으로 충분하지 않은 경우 회로별 저항 측정(Circuit-Specific Resistance Measurement)을 통합할 수 있다. 전력 도체(Power Conductor), 접지 경로(Ground Path), 안전 회로(Safety Circuit) 및 기타 중요 연결부는 과도한 저항으로 인해 전압 강하, 발열 또는 불안정한 동작이 발생할 수 있으므로 더욱 엄격한 저항 한계를 요구할 수 있다. 자동 평가를 사용하면 전체 하니스에 하나의 일반적인 도통 기준을 적용하는 대신 각각의 회로에 적합한 허용 한계를 적용할 수 있다.

필요한 경우 자동화 시험 스테이션은 일반적인 저전압 측정(Low-Voltage Measurement)과 절연 저항 시험(Insulation Resistance Test) 또는 고전압 하니스 시험(High-Voltage Harness Test)을 연계하여 제어할 수 있다. 이러한 기능에는 적절한 스위칭 아키텍처(Switching Architecture), 정격 전압을 만족하는 치구, 보호 인터페이스(Guarded Interface), 인터록(Interlock), 방전 제어(Discharge Control)가 필요하다. 자동화 시험 순서는 저전압 도통 시험과 높은 전압을 사용하는 시험을 명확하게 분리하고 모든 안전 조건이 충족되지 않으면 위험 전압이 인가되지 않도록 해야 한다.

잘 설계된 시험 순서에서는 일반적으로 더 높은 위험이나 스트레스를 수반하는 시험보다 위험도가 낮은 검사를 먼저 수행한다. 제품 식별(Product Identification), 치구 확인, 도통, 핀 매핑, 기본 저항 측정을 통해 절연 또는 내전압 시험(Dielectric Test)을 시작하기 전에 명백한 제조 문제를 검출할 수 있다. 이러한 순서는 결함이 있는 어셈블리에 불필요한 전기적 스트레스가 가해지는 것을 방지하고 자동화 프로세스의 가능한 초기 단계에서 고장을 진단할 수 있도록 한다.

위험 에너지(Hazardous Energy)를 취급하는 경우 안전 로직(Safety Logic)은 일반적인 시험 결과 처리와 독립적으로 동작해야 한다. 보호 커버(Protective Cover), 출입 도어(Access Door), 비상 제어 장치(Emergency Control), 치구 인터록(Fixture Interlock), 전압 모니터링(Voltage Monitoring), 방전 기능을 시험 스테이션 아키텍처에 통합할 수 있다. 안전 조건이 충족되지 않으면 고전압 발생을 차단해야 하며 작업자가 하니스를 제거하기 전에 시험 인터페이스가 정의된 안전 상태(Safe State)로 복귀해야 한다.

자동 방전 검증(Automatic Discharge Verification)은 높은 전압을 사용하는 시험 이후에 특히 중요하다. 하니스 정전용량(Harness Capacitance), 시험 케이블, 필터 및 내부 측정 회로에는 전원이 차단된 이후에도 전하가 남아 있을 수 있다. 제어기는 제어된 방전(Controlled Discharge)을 수행하고 잔류 전압(Residual Voltage)을 감시하며 측정 상태가 정의된 안전 임계값(Safe Threshold) 이하로 내려간 이후에만 치구 인터록을 해제할 수 있다. 이를 통해 안전 절차를 작업자에게 의존하는 행동이 아니라 시험 순서의 명시적인 일부로 구성할 수 있다.

자동 결과 평가(Automated Result Evaluation)는 원시 측정 데이터(Raw Measurement)를 관리된 제조 판정(Manufacturing Decision)으로 변환한다. 각각의 측정값은 적용되는 합격 기준(Acceptance Criteria)과 비교되며 소프트웨어는 해당 시험 단계의 합격 또는 불합격 여부를 결정한다. 모든 필수 검사가 성공적으로 완료된 이후에만 최종 하니스 판정(Final Harness Disposition)을 생성하도록 구성하면 완료되지 않은 시험 순서가 완전히 검증된 제품으로 잘못 판단되는 것을 방지할 수 있다.

고장 보고(Failure Reporting)는 재작업(Rework)을 직접적으로 지원할 수 있는 진단 정보를 제공해야 한다. 단순한 불합격(FAIL) 메시지만 표시하는 대신 시험 스테이션은 커넥터, 핀, 예상 목적지(Expected Destination), 측정 상태, 저항값, 절연 불량 또는 기타 관련 특성을 식별할 수 있다. 명확한 진단 정보를 제공하면 기술자가 전체 하니스를 수동으로 추적하는 대신 문제가 의심되는 전선, 단자, 스플라이스, 분기 또는 커넥터에 집중할 수 있다.

자동화 시스템은 관리된 재작업 및 재시험(Rework and Retest) 프로세스를 지원할 수 있다. 하니스가 불합격하면 결함이 수정될 때까지 제조 기록에서 해당 상태를 유지할 수 있다. 수리 후에는 적용되는 품질 규칙(Quality Rule)에 따라 영향을 받은 시험 단계 또는 전체 하니스 시험을 다시 수행하도록 시험 스테이션에서 요구할 수 있다. 이를 통해 수리된 어셈블리가 필요한 검증을 우회한 상태로 정상 생산 흐름에 복귀하는 것을 방지한다.

데이터 기록(Data Logging)은 자동화의 주요 장점 중 하나이다. 시스템은 하니스 식별 정보, 리비전, 시험 프로그램 버전, 치구 식별 정보, 시험 스테이션 식별 정보, 작업자, 날짜와 시간, 개별 측정값, 허용 한계, 고장 상세 정보, 재작업 이력 및 최종 판정을 기록할 수 있다. 이러한 기록은 실제 하니스와 시험 구성 그리고 해당 제품을 승인하는 데 사용된 검증 근거 사이에 추적 가능한 관계를 형성한다.

시험 프로그램 구성(Test-Program Configuration)은 공식적인 리비전 관리(Revision Control)하에 유지되어야 한다. 제품이 발전함에 따라 하니스 도면, 커넥터 정의, 넷리스트, 허용 한계 및 시험 순서가 변경될 수 있다. 따라서 자동화 시험 스테이션은 현재 제조 구성에 대응하는 승인된 프로그램을 사용해야 하며 시험 기록에 해당 프로그램 버전을 함께 저장해야 한다. 승인되지 않았거나 오래된 시험 레시피가 생산 합격 여부를 결정하도록 허용해서는 안 된다.

자동화가 시험 장비 자체에 대한 검증 필요성을 제거하는 것은 아니다. 스위칭 매트릭스(Switching Matrix), 저항 측정 채널, 절연 시험 기능, 고전압 전원, 치구 배선, 인터록 및 통신 인터페이스(Communication Interface)는 성능이 저하되거나 고장날 수 있다. 자체 시험 루틴(Self-Test Routine), 루프백 치구(Loopback Fixture), 기준 저항(Reference Resistance), 정상 상태가 확인된 기준 하니스(Known-Good Harness), 정기 교정(Scheduled Calibration)을 유지보수 전략에 포함하여 생산 판정이 신뢰할 수 있는 측정값을 기반으로 이루어지도록 해야 한다.

대량의 구조화된 시험 데이터(Structured Test Data)가 자동으로 수집되면 통계 분석(Statistical Analysis)을 실질적으로 활용할 수 있다. 저항값 분포, 고장 빈도, 커넥터별 결함, 반복적인 단선, 절연 성능 추세 및 재작업률(Rework Rate)을 시간에 따라 모니터링할 수 있다. 점진적인 변화는 불합격 하니스가 크게 증가하기 전에 공구 마모, 재료 편차, 치구 열화, 조립 문제 또는 공정 드리프트(Process Drift)를 나타낼 수 있다.

자동화 시험 데이터는 보다 광범위한 제조 품질 시스템(Manufacturing Quality System)을 지원할 수도 있다. 시험 결과를 생산 로트(Production Lot), 작업 스테이션, 압착 장비(Crimping Equipment), 재료 배치(Material Batch), 조립 작업자와 연계하면 반복적으로 발생하는 결함을 잠재적인 원인까지 추적할 수 있다. 제조 정보 시스템(Manufacturing Information System)과 통합하면 제품 계보(Product Genealogy)와 품질 이력(Quality History)을 구축할 수 있지만, 구체적인 인터페이스와 데이터베이스 아키텍처(Database Architecture)는 생산 환경에 따라 달라진다.

로봇 플랫폼(Robotic Platform)에서는 하니스 복잡성이 증가할수록 자동화의 가치가 더욱 커진다. 하나의 로봇에도 배터리 회로, 모터 전력, 안전 배선, CAN 또는 CAN FD, 이더넷(Ethernet), 센서, 액추에이터(Actuator), 충전 인터페이스 및 보조 입출력(Auxiliary I/O)이 여러 하니스 분기에 분산될 수 있다. 자동 시험을 적용하면 반복적인 수동 프로빙(Manual Probing)과 작업자의 해석에 의존하지 않고 이러한 연결을 관리된 회로별 규칙에 따라 검증할 수 있다.

그러나 하니스 시험 자동화는 물리적인 작업 품질 검사(Physical Workmanship Inspection)를 대체하기보다는 보완해야 한다. 전기적 자동 시험만으로는 배선 치수, 굽힘 반경(Bend Radius), 보호 슬리브(Protective Sleeve), 클립, 라벨, 실, 커넥터 방향 및 기계적 스트레인 릴리프가 올바른지를 입증할 수 없다. 따라서 레이아웃 보드 검사(Layout Board Inspection)와 압착 인장 시험(Crimp Pull Testing)은 여전히 중요한 보완 공정이며, 자동화는 반복 가능한 전기적 검증과 통합된 제조 기록을 제공한다.

궁극적으로 자동화 하니스 시험 스테이션(Automated Harness Test Station)은 하니스 조립과 시스템 통합(System Integration) 사이에서 관리된 제조 품질 게이트(Manufacturing Quality Gate)로 기능한다. 제품 식별, 치구 검증, 전기 시험, 안전 시험 순서, 자동 평가, 고장 진단, 추적성, 재시험 및 공정 데이터 분석을 결합함으로써 개별적인 하니스 측정을 점점 더 복잡해지는 로봇 전기 아키텍처(Robotic Electrical Architecture)에 적합한 반복 가능하고 체계적인 검증 워크플로(Validation Workflow)로 전환한다.
