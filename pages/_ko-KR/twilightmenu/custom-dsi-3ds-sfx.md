---
lang: ko-KR
layout: wiki
section: twilightmenu
category: customization
title: DSi / 3DS Skins - Custom SFX
description: TWiLight Menu++용 DSi와 3DS 스킨의 커스텀 배경음악과 사운드 효과를 사용하는 방법
---

TWiLightMenu는 테마에서 커스텀 사운드를 지원합니다. 사용할 사운드 파일을 테마 폴더 안의 `sound` 디렉토리에 넣습니다. 예를 들어, `white`라는 테마가 있다고 치면 파일을 각각 `themes/white/sound/sfx.bin` 그리고 `themes/sound/bgm.pcm.raw`으로 해서 넣어둡니다. 두 파일들은 굳이 넣어야 할 필요는 없고, 둘 중 하나가 사라지면 기본 사운드를 사용합니다. 파일을 잘 넣어놨다면, 설정의 음악 옵션을 "테마"로 설정합니다.

이 설명은 mmutil이 설치된 devkitPro를 갖고있다는 전제 하에 적용됩니다. [devkitPro 웹사이트](https://devkitpro.org/wiki/Getting_Started)에서 devkitPro를 받으실 수 있습니다.

## 사운드 효과 뱅크
사운드 효과 뱅크에서는 아이콘 선택 사운드와 같은 사운드 효과를 포함합니다.

| 파일          | 설명                                                              |
| ----------- | --------------------------------------------------------------- |
| startup.wav | 시스템을 시작할 때 재생합니다. 더 자세한 설명은 [부팅 음악](#startup-sound) 섹션을 참고해주세요. |
| back.wav    | 뒤로갈때 재생됩니다.                                                     |
| launch.wav  | 게임을 실행할 때 재생됩니다.                                                |
| select.wav  | 선택 커서를 움직일 때 재생됩니다.                                             |
| wrong.wav   | 페이지의 끝에 다다랐을 때 재생됩니다.                                           |
| switch.wav  | 페이지를 전환할 때 재생됩니다.                                               |
| stop.wav    | DSi 테마에서 선택커서가 움직임을 멈출 때 재생됩니다.                                 |
| bgm.pcm.raw | 사운드 목록의 일부분이 아닙니다. 더 자세한 설명은 [메뉴 배경음악](#menu-bgm) 섹션을 참고해주세요.   |

사운드 효과 뱅크를 만들기 위해 `make`를 실행할 수 있습니다. 위에 나열된 모든 파일들은 *bgm.pcm.raw*가 필요하지만 무음으로 만들 수도 있습니다.

최종적으로 *sfx.bin*은 **512000B = 512 KB를 넘어서는 안됩니다**. 이것보다 높을 경우, 충돌을 일으키거나 사운드가 끝까지 재생되지 않을 수 있습니다.

### 부팅 음악
다른 사운드 효과는 WAV 파일에서 작동하지만, 시작 사운드는 제대로 작동하려면 특정 형식이어야 하며, 그렇지 않으면 시작 사운드가 중지되는 시점과 배경 음악이 시작되는 시점 사이에 차이가 있을 수 있습니다.

startup.wav 파일은 반드시 **16-bit 16 kHz** 형식이어야 합니다. 이 형식으로 변환하기 위해 [Audacity](https://www.audacityteam.org/download/)를 사용해볼 수 있습니다. Audacity에 파일이 로딩되었으면, **Project Rate (Hz)**를 **16000**으로 변경하고, **Shift+M**을 누른 다음, **Format**을 **16-bit PCM**으로 변경합니다.

사용하려는 파일이 스테레오라면, **Tracks > Mix > Mix Stereo down to Mono**를 순서대로 진행하세요.

부팅 음악을 재생하고 싶으시면, 사용자의 `theme.ini`에서 `PlayStartupJingle=1`로 설정해주세요.


## 메뉴 배경음악

메뉴 배경음악은 **16-bit 16 kHz 모노** raw PCM 파일이여야 합니다. 이 형식으로 변환하기 위해 [Audacity](https://www.audacityteam.org/download/)를 사용해볼 수 있습니다. Audacity에 파일이 로딩되었으면, **Project Rate (Hz)**를 **16000**으로 변경하고, **Shift+M**을 누른 다음, **Format**을 **16-bit PCM**으로 변경합니다.

사용하려는 파일이 스테레오라면, **Tracks > Mix > Mix Stereo down to Mono**를 순서대로 진행하세요.

맞는 포맷으로 추출하기 위해 할 것:
1. `File` > `Export` > `Export Audio...`를 선택합니다.
1. `File Type`을 `Other uncompressed files`로 설정합니다.
1. `Header`를 `RAW (header-less)`로 설정합니다.
1. `Encoding`을 `Signed 16-bit PCM`로 설정합니다.
1. 이름을 `bgm.pcm.raw`로 설정하고 `Save`를 누릅니다.
1. 메타데이터 수정을 위해 `OK`를 누릅니다.

이제 만들어진 `bgm.pcm.raw` 파일을 복사하여 사용자의 테마 폴더 안에 *sound* 하위 폴더를 만든 후 붙여넣으세요.

sfx.bin 파일과는 다르게, *bgm.pcm.raw* 파일은 용량이 얼마든지 커도 좋습니다.
