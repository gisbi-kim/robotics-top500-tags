# robotics-top500-tags

12-tag taxonomy + tag-combination explorer for the top-500 cited robotics papers (2010–2026).

> 좋은 논문은 단일 태그가 아니라 **강한 태그 조합**으로 정의된다.
> 어떤 조합이 실제로 분야에서 통하는지 — top 500 cited 논문에 12개 태그를 매겨보고, 조합 분포로 검증하는 도구.

## 데모

- **Explorer**: [`index.html`](index.html) — 500편을 태그·venue·연도·검색·data-driven top combinations으로 필터
- **태그 가이드**: [`tags_guide.html`](tags_guide.html) — 12개 태그 정의 + A급 조합 vs 약한 조합

GitHub Pages가 켜져 있으면 `https://gisbi-kim.github.io/robotics-top500-tags/` 에서 바로 열림.

## 12개 태그

| 태그 | 정의 |
|------|------|
| 문제정의 | 새 문제·연구 질문을 세운다 |
| 평가축 | 성능을 재는 기준을 바꾼다 |
| 방법전환 | 같은 병목을 다른 formulation·구조로 푼다 |
| 인프라 | 데이터셋·벤치마크·툴·평가 파이프라인을 만든다 |
| 경고신호 | failure mode·negative result·deployment risk를 드러낸다 |
| 통합정리 | survey·taxonomy로 분야의 좌표를 잡는다 |
| 스케일업 | 모델·데이터·embodiment·실험 수를 키운다 |
| 실사용전환 | latency·real-time·on-device·hardware·closed-loop을 직접 겨냥한다 |
| 데이터전환 | 병목을 데이터 수집·정제·합성에서 푼다 |
| 해부분석 | 모델의 mechanism·내부 표현·ablation을 뜯어본다 |
| 표준후보 | 후속 논문이 계속 쓸 task·metric·protocol·benchmark를 제안한다 |
| 위험보류 | baseline·split·ablation·공개성 때문에 claim 확인이 필요하다 |

한 논문에 여러 개가 붙을 수 있고, 화면에서는 보통 핵심 2~3개만 보인다. 자세한 정의·Tier·조합론은 [tags_guide.html](tags_guide.html).

## 좋은 논문의 공식

```
[문제정의] + [평가축] + ( [경고신호]  or  [실사용전환] )
```

이 조합이 붙어 있으면 좋은 논문일 확률이 높다. 단일 태그만 강한 논문은 빠르게 잊힌다.

## 데이터

- **출처**: [RoboPaper Atlas](https://gisbi-kim.github.io/robotics-paper-phylogeny/) (DBLP + Crossref + OpenAlex), 인용수는 Semantic Scholar
- **인용 기준일**: 2026-05-08
- **범위**: ICRA · IROS · RA-L · T-RO · RSS · IJRR · Sci-Rob · SoRo · T-Mech · T-FR · RA-P · T-ASE · RAM · CoRL · iSpaRo (2010–2026)
- **선정**: 인용수 상위 500편

## 파일

- [`robotics_top500_tagged.json`](robotics_top500_tagged.json) — 500편 + 태그 (source of truth)
- [`index.html`](index.html) — explorer (필터·검색·top combinations)
- [`tags_guide.html`](tags_guide.html) — 12개 태그 정의 + 조합론

## 한계

- 태그는 제목·venue·년도·저자 기반 휴리스틱 판단. 실제 contribution 검증은 별도 필요.
- `위험보류` 태그는 baseline·split·공개성 같은 메타 정보가 필요해서 제목만으로는 거의 판단 불가 — 직접 검증이 필수.
- top combinations는 단순 빈도 기반. "좋은 조합"이 자동으로 상위에 오는 게 아니라 "흔한 조합"이 올라온다 (이게 분야의 실태를 보여주는 것).

## License

MIT
