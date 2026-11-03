# Hack & Slash 프로토타입 (1차) — 마법사 vs 몬스터

Unreal Engine 5.5 블루프린트로 만든 **3인칭 핵앤슬래시 프로토타입**입니다.
마법사 캐릭터가 스킬로 몬스터를 처치하는 전투의 핵심 루프를 빠르게 만들어 보는 것이 목표였습니다.

<!-- 플레이 영상이나 스크린샷을 여기에 넣어 주세요 -->

## 개요

| 항목 | 내용 |
| --- | --- |
| 엔진 | Unreal Engine 5.5 |
| 구현 방식 | 블루프린트 |
| 장르 | 3인칭 핵앤슬래시 |
| 기간 | 2025.04 (마지막 커밋 기준) |
| 인원 | 1인 |
| 이어지는 작업 | [20250430Test](https://github.com/leemingeun10/20250430Test) (2차 프로토타입) |

## 구현한 시스템

- **플레이어**: 마법사 캐릭터(`BP_Wizard`)와 전용 애니메이션 블루프린트(`ABP_main`)
- **스킬**: 스킬 기본 블루프린트(`BP_SkillBase`)와 보호막(`BP_shield`)
- **몬스터**: 공통 몬스터 블루프린트(`BP_BaseMonster`)와 비홀더, 선인장, 미믹(상자), 버섯 4종
- **컴포넌트**: 몬스터 스탯(`BP_MonStatComponent`)과 스폰(`BP_MonSpwanComponent`) 컴포넌트
- **보상**: 몬스터 처치 시 골드(`BP_GoldBall`) 드롭
- **UI**: 이름표 컴포넌트(`BP_NameTagComponet`)와 HUD(`BP_Hud`)

## 폴더 구조

```
Content/
├── HackandSlashGameForTest/   # 직접 만든 게임 로직 (몬스터, 스킬, UI)
├── BattleWizardPolyart/       # 마법사 캐릭터 (외부 에셋)
└── MonsterForSurvivalGame/    # 몬스터 모델·애니메이션 (외부 에셋)
```

## 실행 방법

Unreal Engine 5.5에서 `P20250425.uproject`를 열고 ThirdPerson 맵을 실행합니다.
