# Raspberry Pi Pico Projects

Projekty dla **Raspberry Pi Pico**, **Pico W** i **Pico 2** w C (pico-sdk) oraz MicroPython.

## Struktura

```
Rpi_Pi_Pico/
├── C/
│   ├── common/            # współdzielone moduły C
│   ├── pico/              # RP2040 — Pico
│   ├── pico-w/            # RP2040 + WiFi — Pico W
│   └── pico-2/            # RP2350 — Pico 2
├── Micropython/
│   ├── common/            # współdzielone moduły .py
│   ├── pico/
│   ├── pico-w/
│   └── pico-2/
├── .gitignore
└── README.md
```

## C (pico-sdk)

- SDK instaluj **poza repozytorium** (submodule, `PICO_SDK_PATH` lub instalacja systemowa).
- Projekt budujesz z CMake, wybierając płytkę: `-DPICO_BOARD=pico`, `pico_w` lub `pico2`.
- Projekty specyficzne dla WiFi trzymaj w `C/pico-w/`, dla RP2350 w `C/pico-2/`.

## MicroPython

- Firmware MicroPython pobierz z [micropython.org/download](https://micropython.org/download/) — nie commituj `.uf2` firmware.
- Wgraj pliki projektu (`main.py`, moduły z `lib/`) przez **mpremote**, **Thonny** lub rshell.
- Projekty z WiFi → `Micropython/pico-w/`.

## Dodawanie projektu

| Język        | Lokalizacja                          | Przykład                    |
|--------------|--------------------------------------|-----------------------------|
| MicroPython  | `Micropython/<płytka>/<nazwa>/`      | `Micropython/pico/blink/`   |
| C            | `C/<płytka>/<nazwa>/`                | `C/pico/blink/`             |

Wspólny kod wielokrotnego użytku → odpowiedni folder `common/`.
