# 회사·카테고리별 저장소 후보

확인일: 2026-10-23 (Asia/Seoul)

범위: 공식 저장소 URL과 소개·일부 기여/운영 문서 확인. 활동량·리뷰 비중·회사별 기여 비중은 아직 측정하지 않았다.

## 분류 규칙

- **P0**: 분야별 1차 조사 후보. 적합성 점검을 통과하면 본 분석에 채택한다.
- **P1**: 같은 분야 비교와 P0 대체를 위한 우선 후보.
- **P2**: 추가 확장 후보. 현재 활동량과 자료 확보 비용부터 점검한다.
- 회사 관계는 프로젝트의 출발·조직 경로에 대한 배경 정보다. 현재 기술 의사결정권이나 회사 전체 개발 방식의 대표성을 뜻하지 않는다.
- GitHub 조직명, 프로젝트 운영 주체, 재단의 후원·소유 관계는 별도 필드로 관리한다. 운영 이력은 분석 기간 당시의 자료로 재확인한다.

## 1. 프론트엔드·UI

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [react/react](https://github.com/react/react) | Meta에서 시작, 현재 React Foundation | API 설계 논의·호환성·릴리스가 어떻게 연결되는가? | UI, 라이브러리, API |
| P1 | [microsoft/fluentui](https://github.com/microsoft/fluentui) | Microsoft 조직 | 컴포넌트 소유권·접근성·버전 변경은 어떻게 검토되는가? | 디자인 시스템, 접근성, 모노레포 |
| P2 | [airbnb/visx](https://github.com/airbnb/visx) | Airbnb 조직 | 여러 시각화 패키지의 변경과 릴리스를 어떻게 묶는가? | 시각화, 패키지, 모노레포 |

React의 기존 `facebook/react` URL은 현재 `react/react`로 이동한다. [공식 재단 출범 발표](https://react.dev/blog/2026/02/24/the-react-foundation)는 2026-02-24 기준 소유 관계 변경을 설명한다. 분석 기간을 기준으로 Meta 조직의 현재 운영 사례와 분리한다.

## 2. 개발 도구·빌드

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [microsoft/vscode](https://github.com/microsoft/vscode) | Microsoft 조직 | 이슈 분류·마일스톤·수정 검증·릴리스는 어떻게 이어지는가? | 에디터, 제품, 확장성 |
| P1 | [bazelbuild/bazel](https://github.com/bazelbuild/bazel) | Google에서 시작, Bazel 프로젝트 | 빌드 시스템의 호환성과 외부 기여를 어떤 절차로 관리하는가? | 빌드, 대규모 코드베이스 |
| P2 | [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | Microsoft 조직 | 언어 도구 변경의 제안·회귀 테스트·릴리스는 어떻게 이어지는가? | 타입 검사, 컴파일러 |

TypeScript의 주 카테고리는 이번 비교 편의상 개발 도구로 정했다. 언어·컴파일러를 보조 태그로 사용한다. VS Code 저장소의 공개 소스·릴리스와 최종 제품 배포 사이의 차이도 보고서에 기록한다.

## 3. 언어·컴파일러·런타임

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [swiftlang/swift](https://github.com/swiftlang/swift) | Apple에서 시작, Swift 프로젝트 | 공개 언어 제안이 컴파일러 구현·리뷰·테스트에 어떻게 반영되는가? | 언어, 컴파일러, 호환성 |
| P1 | [dotnet/runtime](https://github.com/dotnet/runtime) | Microsoft 생태계, dotnet 조직 | 영역별 소유권·성능·API 변경 검토를 어떻게 연결하는가? | 런타임, GC, 표준 라이브러리 |
| P2 | [golang/go](https://github.com/golang/go) | Google과 오픈소스 커뮤니티, Go 프로젝트 | 제안·승인·구현·릴리스 동결은 어떻게 연결되는가? | 언어, 표준 라이브러리, Gerrit |

Swift는 [기여 안내](https://www.swift.org/contributing/)와 [프로젝트 운영 안내](https://www.swift.org/community/how-we-work/)를 함께 본다. Go는 [공식 기여 안내](https://go.dev/doc/contribute)에 따라 Gerrit의 CL을 조사해야 하므로 GitHub PR 수와 리뷰 시간만으로 비교하지 않는다. Go의 상세 수집기는 2차 이후 별도 범위로 둔다.

## 4. 클라우드·인프라

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [aws/aws-cdk](https://github.com/aws/aws-cdk) | Amazon/AWS 조직 | 인프라 API·모듈 변경과 호환성·통합 테스트를 어떻게 관리하는가? | IaC, SDK, 모노레포 |
| P1 | [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) | Google에서 시작, CNCF 생태계·커뮤니티 운영 | 영역별 리뷰·승인·릴리스 책임은 어떻게 나뉘는가? | 오케스트레이션, 다중 조직 |
| P2 | [envoyproxy/envoy](https://github.com/envoyproxy/envoy) | Lyft에서 시작, CNCF 프로젝트 | 네트워크 API·성능·릴리스 위험은 어떻게 검토되는가? | 프록시, 네트워크, 다중 조직 |

Kubernetes와 Envoy는 회사 단독 운영 사례로 분류하지 않는다. [Kubernetes 기여 안내](https://kubernetes.io/docs/contribute/)와 [CNCF Envoy 소개](https://www.cncf.io/projects/envoy/)를 출발점으로 프로젝트별 운영 문서를 추가 확인한다.

## 5. AI·머신러닝

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [tensorflow/tensorflow](https://github.com/tensorflow/tensorflow) | Google에서 시작, TensorFlow 프로젝트 | 여러 플랫폼의 검증과 공개 리뷰의 관찰 범위는 어떻게 다른가? | 학습, 프레임워크, 다중 플랫폼 |
| P1 | [pytorch/pytorch](https://github.com/pytorch/pytorch) | Meta에서 시작, PyTorch Foundation | 기능 변경의 설계·소유권·CI·릴리스를 어떻게 연결하는가? | 학습, 프레임워크, 가속기 |
| P2 | [NVIDIA/TensorRT](https://github.com/NVIDIA/TensorRT) | NVIDIA 조직, TensorRT의 공개 구성요소 | 공개 구성요소에서 추론 최적화·호환성 검증이 어디까지 보이는가? | 추론, GPU, SDK |

[PyTorch Foundation](https://pytorch.org/foundation/)은 현재 재단 운영 맥락을 설명한다. TensorRT 저장소는 제품의 공개 구성요소를 다루므로 제품 전체의 개발·릴리스를 대표한다고 가정하지 않는다. AI 분야도 코드 변경 워크플로우를 분석하며, 비공개 학습 데이터·모델 학습 운영·실험 관리까지 자동으로 범위를 확대하지 않는다.

## 6. 데이터·스토리지·관측

| 우선순위 | 저장소 | 회사 관계·현재 공개 맥락 | 분석 질문 | 태그 |
| --- | --- | --- | --- | --- |
| P0 | [Netflix/atlas](https://github.com/Netflix/atlas) | Netflix 조직 | 시계열 데이터 처리 변경의 테스트·성능 검증·릴리스는 어떻게 이어지는가? | 시계열, 관측, 데이터베이스 |
| P1 | [facebook/rocksdb](https://github.com/facebook/rocksdb) | Meta/Facebook 조직 | 저장 형식·성능·회귀 위험을 어떤 근거로 검토하는가? | 스토리지, 임베디드 DB, 성능 |
| P2 | [google/leveldb](https://github.com/google/leveldb) | Google 조직 | 성숙한 라이브러리의 유지보수·변경 수용·릴리스는 어떻게 운영되는가? | 스토리지, 유지보수 |

Atlas는 [기여 안내](https://github.com/Netflix/atlas/blob/main/CONTRIBUTING.md)와 실제 PR의 공개 리뷰량을 우선 대조한다. LevelDB는 최근 변경량부터 측정한다. 활동량이 적으면 활발한 프레임워크와 처리 속도를 직접 비교하기보다 성숙한 프로젝트의 유지보수 사례로 분리한다.

## 회사별 찾아보기

아래는 관계별 탐색용 목록이다. 재단 이관 프로젝트는 현재 회사 소유 목록에 합산하지 않는다.

| 회사 | 해당 회사 조직·생태계의 후보 | 해당 회사에서 시작한 별도 프로젝트 |
| --- | --- | --- |
| Microsoft | microsoft/vscode, microsoft/fluentui, microsoft/TypeScript, dotnet/runtime | — |
| Google | google/leveldb | bazelbuild/bazel, golang/go, tensorflow/tensorflow, kubernetes/kubernetes |
| Meta | facebook/rocksdb | react/react, pytorch/pytorch |
| Amazon/AWS | aws/aws-cdk | — |
| Apple | — | swiftlang/swift |
| Netflix | Netflix/atlas | — |
| NVIDIA | NVIDIA/TensorRT | — |
| Airbnb | airbnb/visx | — |
| Lyft | — | envoyproxy/envoy |

첫 연구는 Microsoft·Google·Meta·Amazon·Apple·Netflix와 관계된 프로젝트를 포함하는 방향이다. NVIDIA·Airbnb·Lyft는 분야를 확장하고 비교 대상을 보완하기 위한 후보로 둔다. 각 저장소의 현재 유지보수 조직과 의사결정 구조는 첫 주 점검에서 확정한다.

## 후보 등록 시 남길 정보

| 필드 | 기록 내용 |
| --- | --- |
| repository_id, canonical_url | GitHub의 고유 ID와 현재 공식 URL. 이름 변경·이동 이력 포함 |
| primary_category, tags | 주 카테고리 1개, 보조 태그 여러 개 |
| company_origin, company_relationship | 출발 회사와 현재 회사 관계, 근거 URL |
| github_owner, governance, governance_as_of | GitHub 조직, 공개 운영 구조, 해당 시점과 출처 |
| public_review_system | GitHub, Gerrit, 포럼 등 실제 공개 기록 위치 |
| evidence_visibility | PR·리뷰·CI·릴리스별 관찰 가능·부분 가능·불가 |
| pattern_candidates | 실행 단위 관행 후보 ID와 출처. 문서 규정·실제 관찰·AI 가설을 구분 |
| context, prerequisites | 기여 방식·역할·제품 제약·도구·필수 선행 조건 |
| counterevidence, portability_limits | 반례·공개되지 않은 과정·다른 팀에 옮길 때의 한계 |
| period, population_count, bot_share | 분석 기간과 측정한 전체 건수·자동화 비중 |
| priority, decision, reason | 후보 우선순위, 채택·보류·제외 및 이유 |

모든 후보의 저장소 URL은 위 각 행에 연결했다. 공식 소개에서 확인한 제품 설명과 연구자가 제안한 분석 질문을 구분하며, 수집 후 측정할 값은 미리 채우지 않는다.

## 관행 조합에 사용하는 방식

후보 저장소는 회사별 순위나 ‘장점 점수’를 매기기 위한 목록이 아니다. [AI 설계 기능](product/WORKFLOW_COMPOSER.md)은 이 목록에서 출처를 찾고, 실제 근거를 확인한 리뷰·설계·검증·릴리스 등의 모듈을 검색한다. 사용자에게 회사·분야 필터를 제공하되, 채택은 대상 팀의 문제·필수 조건·역할·부담에 따라 결정한다.

위 각 표의 분석 질문은 아직 검증한 모듈이 아니다. 프로젝트별 관행 카드에는 관찰 기간·문서 버전·반례·적용 전제를 연결하고, 다른 프로젝트 모듈과 결합한 새 연결은 별도 설계 가설로 표시한다. 오래된 근거는 현재 정책 여부를 재확인하며 기존 버전은 보존한다.
