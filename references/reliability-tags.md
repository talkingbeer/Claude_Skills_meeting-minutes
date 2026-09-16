# 신뢰도 표기 체계

## 4단 태그

| 태그 | 마크다운 표기 | HTML chip 클래스 | 의미 |
|---|---|---|---|
| 사실 | `[사실]` | `chip` | 제도, 데이터 등 검증 가능한 진술 |
| 본인 견해 | `[본인 견해]` | `chip view` | 인터뷰 대상 또는 발언자의 판단, 해석 |
| 전언 | `[전언]` | `chip hear` | 제3자에게 들은 내용 |
| 미확인 | `[미확인]` | `chip na` | 녹취 파손, 수치 불명 |

## 적용 규칙

- 문장 단위로 부여한다. 한 문단에 태그 하나로 묶지 않는다
- 본문 태그와 표 태그의 정합을 유지한다
- Q→A 확인 응답은 "~를 묻자 그렇다고 답했다"로 서술하고 태그는 본인 견해
- 인터뷰어의 부정 의문 전제에 대한 짧은 확인은 단정이 아니라 확인 응답으로 서술

## 범례 HTML

```html
<p class="legend" style="margin-top:12px"><b>신뢰도 표기</b></p>
<ul class="legend" style="list-style:none;margin:4px 0 0;font-size:12.5px">
  <li><span class="chip">사실</span> 제도, 데이터 등 검증 가능한 진술</li>
  <li><span class="chip view">본인 견해</span> 인터뷰 대상의 판단, 해석</li>
  <li><span class="chip hear">전언</span> 제3자에게 들은 내용</li>
  <li><span class="chip na">미확인</span> 녹취 파손 또는 수치 불명</li>
</ul>
<p style="margin-top:8px;color:#6f6f6f;font-size:12.5px">
  인물은 전원 역할 표기로 치환했다. 녹취가 파손된 구간은 추정하지 않고 미확인으로 남겼다.
</p>
```
