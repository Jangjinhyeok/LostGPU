# LOSTGPU (로스트아크 모작)

| 항목 | 내용 |
|---|---|
| 기간 | 2024.12.02 ~ 2024.12.30 (원티드 POTENUP 1기 1차 프로젝트) |
| 인원 | 3명 (팀원마다 레이드 보스 1종 담당) |
| 장르·플랫폼 | PC 탑뷰 핵앤슬래시, 레이드 매칭으로 솔로 레이드 보스를 공략하는 구조 |
| 기술 | UE5, Blueprint, UMG |
| 내 담당 | 보스 일리아칸(Akkan)과 기믹 시스템, 대기방·레벨 체인저 |
| 영상 | [LostGPU Beta (Akkan)](https://youtu.be/OFJ-Q6nRBBk) |

## 내가 구현한 것

### 보스 일리아칸

- 2관문 마지막 패턴은 보스에게 '파괴' 스택을 쌓아 쓰러뜨리는 기믹으로 만들었습니다. 보스 HP가 0이 되어도 쓰러지지 않고, 남은 스택은 플레이어에게 보이지 않습니다. 스택을 모두 소모하면 클리어, 제한 시간을 넘기거나 플레이어 HP가 0이 되면 게임 오버입니다.
- 공격 패턴은 카운터몹 스폰, 추적 장판, 십자 레이저이며, 보스 본체는 가운데에서 기를 모으는 동작을 이어 갑니다.
- 등장과 사망 연출은 Material Dissolve로 처리했습니다.
- 트러블슈팅: 십자 레이저와 카운터몹의 스폰 위치가 겹치는 문제가 있어, 겹치지 않도록 스폰 로직을 수정했습니다.

### 대기방과 레벨 체인저

- 대기방에서 트리거 박스로 이동한 뒤 체크박스를 클릭하면 해당 보스 맵으로 이동합니다. 각 보스 맵을 대기방과 연결했습니다.

## 팀 구성

| 담당 | 내용 |
|---|---|
| 장진혁 | 보스 일리아칸, 대기방·레벨 체인저 |
| 팀원 | 보스 쿠크세이튼, UI |
| 팀원 | 보스 발탄, 데이터 구조, 플레이어, UI 연동 |

# 👷‍♂️ Contributors
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="33.3%">
        <a href="https://github.com/chungchunglee">
          <img src="https://avatars.githubusercontent.com/u/55828069?v=4?s=100" width="100px;"/><br/>
          <sub><b>이충헌</b></sub>
        </a>
        <br/>
        <sub><a>발탄(Valtan)</a><br/></sub>
      </td>
      <td align="center" valign="top" width="33.3%">
        <a href="https://github.com/Jangjinhyeok">
          <img src="https://avatars.githubusercontent.com/u/37360607?v=4?s=100" width="100px;"/><br/>
          <sub><b>장진혁</b></sub>
        </a>
        <br/>
        <sub><a>일리아칸(Akkan)</a><br/></sub>
      </td>
      <td align="center" valign="top" width="33.3%">
        <a href="https://github.com/byungmeo">
          <img src="https://avatars.githubusercontent.com/u/37506142?v=4?s=100" width="100px;"/><br/>
          <sub><b>김병대</b></sub>
        </a>
        <br/>
        <sub><a>세이튼(Saydon)</a><br/></sub>
      </td>
    </tr>
  </tbody>
</table>
