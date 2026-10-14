# Build sessions — Days 3 and 4

Four decks, one per build session on the schedule. No "hands-on" numbering anywhere; the
build session is the only label used. All 120 original hands-on slides were pooled and
re-split so each session matches the lecture it follows.

Body text is untouched — 370 paragraphs checked character for character. The only text
changed is 27 slide headings that all read "OBC Exercises", "EPS Exercises" or
"ADCS Exercise"; each now names what the slide actually asks for.

| Deck | Follows | Slides |
|---|---|---|
| Build Session 1 — Structure, avionics and C&DH bring-up | Lecture 1, From mission model to hardware | 60 |
| Build Session 2 — Power integration and telemetry | Lecture 2, Power and thermal | 19 |
| Build Session 3 — ADCS configuration and test | Lecture 3, Pointing and attitude control | 18 |
| Build Session 4 — Payload integration and downlink check | Lecture 4, Payload and the link to the ground | 24 |

## Build Session 1 — Structure, avionics and C&DH bring-up
*Day 3, 11:00–12:00 and 13:00–13:45*

| Section | Slides from | Code |
|---|---|---|
| Setting up the Arduino IDE | `Intro_arduinoIDE` 3–6, 10–16 | reference only |
| The kit, the tools and the boards | `Build_Setup` 2–4; `Intro_arduinoIDE` 9; `Build_Setup` 5, 6–11 | — |
| Building the structure | `Build_Setup` 17–37 | — |
| Boards check and on-board computer bring-up | `Build_Setup` 38–41, 13, 12, 14; `OBC_testing` 2–3; `Payload_telemetry` 2–3 | `Day4_Exercises` EX3, EX5, EX6 |

## Build Session 2 — Power integration and telemetry
*Day 3, 15:15–17:00. Power and thermal only; everything runs on the serial monitor.*

| Section | Slides from | Code |
|---|---|---|
| Side panels and solar panels | `Build_Setup` 45–48; `Power_temperature_telemetry` 9–10; `Build_Setup` 50–52 | — |
| EPS temperature and battery voltage | `Payload_telemetry` 4–5 | `Day4_Exercises` EX12, EX14, EX15, EX16 |
| Thermal and power warnings on the serial monitor | `Power_temperature_telemetry` 3–6 | `Day5_Exercises` EX3, EX4 |

## Build Session 3 — ADCS configuration and test
*Day 4, 10:15–11:15. The whole ADCS deck.*

| Section | Slides from | Code |
|---|---|---|
| Sun sensors and the reaction wheel | `ADCS_Day2` 1–8 | `Day6_Exercises` EX1, EX2, EX3 |
| The IMU | `ADCS_Day2` 9–10 | `Day6_Exercises` EX4, EX5 |
| Commanding the ADCS from the OBC | `ADCS_Day2` 11–14 | `Day6_Exercises` EX7 |

## Build Session 4 — Payload integration and downlink check
*Day 4, 12:00–12:45 and 13:45–14:45. Payload and TT&C.*

| Section | Slides from | Code |
|---|---|---|
| Fitting the antenna | `Build_Setup` 42–44, 53–54 | — |
| The ground station and the radio link | `Build_Setup` 15; `Ground_station` 1–5 | `Day2_Exercises`; `Day4_Exercises` EX8, EX9, EX11; `GROUND_RECEIVER_EXERCISE` |
| Telemetry over the link: sendAll and status | `Power_temperature_telemetry` 2, 7, 8 | `Day5_Exercises` EX5, EX6 |
| Taking a picture | `Payload_telemetry` 11, 13 | `Day6_Exercises/TAKE_A_PICTURE` |
| Final exercise | `AIT_Day2` 2–3 | `Day7_FInal_Exercise_Solution` |

## Headings changed

| Was | Now |
|---|---|
| OBC Exercises (`OBC_testing` 2) | Open a new sketch for the OBC |
| OBC Exercises (`OBC_testing` 3) | Reading the OBC temperature sensor |
| OBC Exercises (`Payload_telemetry` 2) | Reading sensors across PC104 |
| OBC Exercises (`Payload_telemetry` 4) | Reading the EPS temperature |
| OBC Exercises (`Payload_telemetry` 5) | Reading the battery voltage |
| OBC Exercises -Camera Challenge (`Payload_telemetry` 11) | Taking a picture |
| EPS Exercises (`Power_temperature_telemetry` 2) | Sending every reading by radio |
| Ground Station Exercises -LEDs (`Build_Setup` 15) | First code on the ground station |
| OBC/GS Exercises -LoRa (`Ground_station` 1–4) | Over to the ground station · Sending a first message over LoRa · Checking the range of the link · Sending a message on command |
| OBC Exercises (`Ground_station` 5) | Transmitting the OBC temperature |
| ADCS Exercise (`ADCS_Day2` 1–10) | Before you start · Reading one sun sensor · Comparing the three sun sensors · Driving the motor with an H-bridge · The H-bridge circuit · How to drive the motor correctly · Turning the wheel to the light · Testing on the stand · Reading the IMU · Detecting a shake |
| ADCS and OBC Exercise (`ADCS_Day2` 11–14) | Linking the ADCS to the OBC · Reading the ADCS temperature · Driving the wheel from the OBC · Detumbling |

## Slides left out

| Slide | Reason |
|---|---|
| `Intro_arduinoIDE` 2; `Build_Setup` 1, 16; `OBC_testing` 1; `Power_temperature_telemetry` 1; `Payload_telemetry` 6, 12; `AIT_Day2` 1 | Old dividers, replaced by the build-session title slides |
| `Intro_arduinoIDE` 7, 8 | Tinkercad circuit and the schematic drawn from it — needs a Google login and internet; `Intro_arduinoIDE` 9 gives the schematics they actually use |
| `Build_Setup` 49 | Solar cell counts, duplicated by `Power_temperature_telemetry` 10 |
| `Payload_telemetry` 1 | Duplicate of `Ground_station` 5 |
| `Payload_telemetry` 7 | sendAll, duplicated by `Power_temperature_telemetry` 2, which carries all five commands |
| `Payload_telemetry` 8, 9, 10 | Warnings, duplicated by `Power_temperature_telemetry` 3–5 |
| `Power_temperature_telemetry` 11, 12 | Empty |

## Code

31 sketches, from 48.

| Removed | Superseded by |
|---|---|
| `Day4_Exercises/EX1_TIME`, `EX2_TIME_MINUTES_SECONDS`, `EX4_TIME_RESET` | `EX3_TIME_REQUEST_T` |
| `Day4_Exercises/EX7_TIMEOBC_RTIMEOBC_TEMPOBC` | `EX16` |
| `Day4_Exercises/EX10_LORA_TEMPOBC` | `EX11_LORA_TEMPOBC_REQUEST` |
| `Day4_Exercises/EX13_TEMPCOMPARISON` | `EX14_TEMPCOMPARISON_WITH_ABSOLUTE_DIFFERENCE` |
| `Day5_Exercises/EX1_SENDALL`, `EX2_WARNINGS_SERIAL` | `EX3_TEMP_BATT_WARNINGS_SERIAL`, `EX5_SENDALL_WARNINGS_INCLUDED` |
| `Day6_Exercises/EX6_ADCS_OBC_TEMP` | `EX7_ADCS_OBC_TEMP_SERIAL_INPUT` |
| `Day2_Exercises` blink, for-loop, while and turn-on-LED drills (7 sketches) | The three kept sketches are the exercises printed on `Build_Setup` 15 |

## Two things to check

The antenna is fitted in Build Session 4 on Day 4, but in the original assembly sequence it
goes on **before** the side and solar panels, which are now in Build Session 2 on Day 3.
Either the teams leave the antenna off on Day 3 and fit it on Day 4, or they fit it during
Build Session 2 and the Build Session 4 slides serve as the reference.

`Build_Setup` 17–37 and the separate `1U CubeSat Build Instructions` deck cover the same
build; Build Session 1 is 60 slides for 1 h 45. Project one, print the other.
