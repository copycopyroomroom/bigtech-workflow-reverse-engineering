# 설계 참고 자료와 적용 범위

확인일: 2026-10-23. 아래 자료는 기획·평가 설계의 출발점이다. 후보 프로젝트별 출처는 [저장소 목록](REPOSITORIES.md)에 별도로 연결했다. 자료를 참고했다는 사실은 본 프로젝트가 인증·검증·효과 입증을 마쳤다는 뜻이 아니다.

| 자료 | 참고한 내용 | 이 프로젝트의 적용과 한계 |
| --- | --- | --- |
| [DORA 측정 안내](https://dora.dev/guides/dora-metrics/) | 서비스 맥락에서 배포 처리량·불안정성을 관찰하는 지표 | 실제 배포 자료가 있을 때만 사용. PR 처리 시간이나 GitHub 태그를 배포 지표로 대체하지 않음 |
| [SPACE 연구 소개](https://www.microsoft.com/en-us/research/publication/the-space-of-developer-productivity-theres-more-to-it-than-you-think/) | 생산성을 단일 활동량으로 설명할 수 없다는 측정 관점 | 흐름 지표와 품질·부담·정성 자료를 함께 검토. 개인 순위에 사용하지 않음 |
| [Google 코드 리뷰 기준](https://google.github.io/eng-practices/review/reviewer/standard.html) | 코드 건전성과 변경 진행 사이의 판단 기준 | 문서화된 정책 근거의 예. 모든 Google 팀의 실제 준수·개선 효과를 입증하지 않음 |
| [ACM SIGSOFT 경험 연구 기준](https://www2.sigsoft.org/EmpiricalStandards/docs/standards) | 방법별 연구 품질과 근거·한계·보고 요구 | 표본·분류·타당성 검토에 참고. 학술 심사 통과나 표준 적합성을 선언하지 않음 |
| [SIGSOFT 표본 선정 보충 자료](https://github.com/acmsigsoft/EmpiricalStandards/blob/master/docs/supplements/Sampling.md) | 모집단과 표본 프레임·선정 과정·편향의 구분 | 의도 선정 저장소와 상세 PR 표본의 대표성 범위를 명시 |
| [OpenSSF Best Practices 기준](https://www.bestpractices.dev/en/criteria/0) | 프로젝트 설명·기여 방법·인터페이스 문서·버전 관리 등의 공개 프로젝트 기준 | 공개 릴리스 준비 목록에 참고. 배지 획득을 목표 달성으로 표시하지 않음 |
| [W3C PROV 개요](https://www.w3.org/TR/prov-overview/) | 데이터·활동·주체의 출처 관계 | 원본→관찰→주장→모듈→제안의 계보 설계에 참고 |
| [JSON Schema 명세](https://json-schema.org/draft/2020-12) | 구조화 입출력 검증 | 구현 시 객체 구조 검사에 사용 예정. 의미·근거·자문 타당성은 별도 검사 |
| [OWASP Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) | 외부 콘텐츠가 모델 지시로 작동하는 위험 | 수집 콘텐츠를 데이터로 취급하고 권한·검증 경계를 분리. 프롬프트만으로 완전 방어한다고 주장하지 않음 |
| [GitHub 검색 API](https://docs.github.com/en/rest/search/search), [페이지네이션](https://docs.github.com/en/rest/using-the-rest-api/using-pagination-in-the-rest-api) | 검색 결과 제한과 목록 순회 | 기간 분할, 중첩 페이지·누락 검사에 사용 |
| [GitHub 속도 제한](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api), [Check runs](https://docs.github.com/en/rest/checks/runs) | 요청 제한과 체크 조회 구조 | 비용·재시도·관찰 가능한 검증 범위를 설계 |

표본 50개, 관찰 사례 3개, 목표 정확도와 통과율 등 이 기획에서 정한 숫자는 **프로젝트의 초기 운영 목표**다. 위 자료가 그 숫자를 공인했다고 해석하지 않는다. 구현·평가 이후 변경 이유와 버전을 남긴다.
