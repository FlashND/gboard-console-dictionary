# Gboard Console Dictionary

A personal dictionary for **Gboard** (Android) that stops autocorrect from mangling terminal commands and adds shortcuts for common long commands.
It covers Linux/Termux, ADB/fastboot, git, PowerShell, and Windows CMD.

Персональный словарь для **Gboard**. С ним клавиатура перестаёт «исправлять» команды в консоли и подсказывает частые команды Linux/Termux, ADB/fastboot, git, PowerShell и Windows CMD. Длинные команды можно вызывать по сокращениям.

## Install / Установка

1. Download [`console_dictionary.zip`](console_dictionary.zip) to your phone. / Скачай `console_dictionary.zip` на телефон.
2. In Gboard, go to **Settings → Dictionary → Personal dictionary**, then tap **⋮ → Import**. / В Gboard открой **Настройки → Словарь → Личный словарь** и нажми **⋮ → Импорт**.
3. Pick the ZIP. / Выбери ZIP.

The locale column is empty, so the words apply to every language. / Язык не указан, поэтому слова работают в любой раскладке.

Tip: for real terminal work, also turn off **Auto-correction** in Gboard → Text correction. / Совет: для консоли ещё отключи «Автоисправление» в разделе «Исправление текста».

## Shortcuts / Сокращения

Type the shortcut and the full command appears as a suggestion. / Набери сокращение, и полная команда появится в подсказках.

| Shortcut | Expands to |
|---|---|
| `alc` | `adb logcat` |
| `adv` | `adb devices` |
| `ash` | `adb shell` |
| `air` | `adb install -r` |
| `arb` | `adb reboot` |
| `aun` | `adb uninstall` |
| `apu` | `adb push` |
| `apl` | `adb pull` |
| `apm` | `adb shell pm list packages` |
| `alcc` | `adb logcat -c` |
| `fbd` | `fastboot devices` |
| `fbr` | `fastboot reboot` |
| `sau` | `sudo apt update && sudo apt upgrade -y` |
| `sai` | `sudo apt install` |
| `lla` | `ls -la` |
| `cdd` | `cd ..` |
| `chx` | `chmod +x` |
| `rmrf` | `rm -rf` |
| `grn` | `grep -rn` |
| `tlf` | `tail -f` |
| `psg` | `ps aux \| grep` |
| `gst` | `git status` |
| `gcm` | `git commit -m` |
| `gpl` | `git pull` |
| `gps` | `git push` |
| `gaa` | `git add .` |
| `glo` | `git log --oneline` |
| `sep` | `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser` |
| `gcr` | `Get-ChildItem -Recurse` |
| `gpw` | `Get-Process \| Where-Object` |
| `sof` | `Select-Object -First` |
| `iwr` | `Invoke-WebRequest -Uri` |
| `tnc` | `Test-NetConnection -Port` |
| `gsr` | `Get-Service \| Where-Object Status -eq Running` |
| `rir` | `Remove-Item -Recurse -Force` |
| `gct` | `Get-Content -Wait -Tail` |

## File format / Формат

`dictionary.txt` is a UTF-8 file. The first line is `# Gboard Dictionary version:1`. Each line after that is `word<TAB>shortcut<TAB>locale`, and the shortcut and locale can be left empty.

To rebuild the ZIP: `zip console_dictionary.zip dictionary.txt`

## Contributing / Как помочь

PRs are welcome. You can add commands, shortcuts, or new sections (Docker, kubectl, Python…). / Пулл-реквесты приветствуются: добавляй команды, сокращения или новые разделы.

## License

MIT
