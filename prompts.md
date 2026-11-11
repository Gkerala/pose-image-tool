# 테스트에 쓴 프롬프트

- 공통 설정: FLUX.2-klein 4B (GGUF Q4_K_M), seed 42, 4 steps, cfg 1.0, euler/simple, 긴 변 1024px
- 포즈 지시 앞머리(뼈대 참조일 때 모든 프롬프트 앞에 붙음):

```
The reference image is a colored OpenPose stick-figure skeleton used only as a pose guide. Generate a new photograph in which the person matches that skeleton exactly: same head direction, same shoulder line, same arm and hand positions, same leg and foot positions, same framing. The final image shows only the real person and the scene; the skeleton lines stay invisible.
```

## 기본 프롬프트 (단계 7, 실험 B)

```
Subject: one factory worker in a navy work jacket and a white safety helmet. Action: holding exactly the pose of the reference. Camera: eye-level shot, 50mm lens, the whole pose in frame. Lighting: soft daylight from large windows. Environment: a clean, empty factory floor with machines in the background. Style: photorealistic, natural colors.
```

## 실험 기록

| 실험 | 포즈 | 이름 | 결과 파일 |
|---|---|---|---|
| A | pose_01 | chef | samples/expA_chef.png |
| A | pose_01 | astronaut | samples/expA_astronaut.png |
| A | pose_01 | watercolor | samples/expA_watercolor.png |
| B | pose_01 | base | samples/expB_pose_01.png |
| B | pose_02 | base | samples/expB_pose_02.png |
| C | pose_01 | chef / ref=skeleton | samples/expC_skeleton.png |
| C | pose_01 | chef / ref=photo | samples/expC_photo.png |

## 실험 A 프롬프트

### chef

```
Subject: one chef in a white uniform and apron. Action: holding exactly the pose of the reference. Camera: eye-level shot, 50mm lens, the whole pose in frame. Lighting: warm kitchen lights. Environment: a busy restaurant kitchen with steel counters. Style: photorealistic.
```

### astronaut

```
Subject: one astronaut in a white space suit with the helmet visor open. Action: holding exactly the pose of the reference. Camera: eye-level shot, 35mm lens, the whole pose in frame. Lighting: hard sunlight with deep shadows. Environment: a grey lunar surface with Earth in a black sky. Style: photorealistic.
```

### watercolor

```
Subject: one young woman in a yellow raincoat. Action: holding exactly the pose of the reference. Camera: eye-level shot, the whole pose in frame. Lighting: soft overcast light. Environment: a rainy city street with reflections. Style: loose watercolor illustration.
```
