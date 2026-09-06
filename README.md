<p align="center">
  <img src="assets/banner.svg" alt="Arch Linux to NixOS — Migration Guide" width="100%" />
</p>

<div align="center">

[![License: GPL-2.0](https://img.shields.io/badge/License-GPL--2.0-yellow.svg)](LICENSE)
[![NixOS](https://img.shields.io/badge/NixOS-26.05%20%2F%20unstable-5277C3?logo=nixos&logoColor=white)](https://nixos.org)
[![Status](https://img.shields.io/badge/status-in%20progress-orange)](#-прогресс)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/vanyadima/arch-to-nixos-guide/pulls)
[![Stars](https://img.shields.io/github/stars/vanyadima/arch-to-nixos-guide?style=social)](https://github.com/vanyadima/arch-to-nixos-guide/stargazers)

</div>

<p align="center">
  Подробный практический гайд для тех, кто хочет перейти с <b>Arch Linux</b> на <b>NixOS</b> —<br/>
  от философии декларативных конфигураций до переноса dotfiles, WM и системных служб.
</p>



## 💡 О проекте

Этот гайд — не пересказ официальной документации, а взгляд человека, который уже прошёл путь Arch → NixOS и хочет
сэкономить время следующим. Упор сделан на практику: конкретные конфиги, типичные грабли и объяснение того,
*почему* NixOS устроен именно так, а не иначе — особенно там, где это контринтуитивно после Arch.

**Для кого этот гайд:**
- вы уверенно чувствуете себя в Arch и командной строке;
- вас не пугает мысль выучить ещё один язык (Nix-язык) ради воспроизводимой системы;
- вам важны атомарные обновления и откаты, а не только «последняя версия здесь и сейчас».

---

## 📖 Содержание

### [Часть I. Введение и подготовка](docs/01-vvedenie-i-podgotovka.md)
- [Глава 1. Зачем переходить на NixOS](docs/01-vvedenie-i-podgotovka.md#глава-1-зачем-переходить-на-nixos)
- [Глава 2. Ключевые концепции Nix и NixOS](docs/01-vvedenie-i-podgotovka.md#глава-2-ключевые-концепции-nix-и-nixos)
- [Глава 3. Подготовка к переходу](docs/01-vvedenie-i-podgotovka.md#глава-3-подготовка-к-переходу)

### [Часть II. Установка NixOS](docs/02-ustanovka.md)
- [Глава 4. Способы установки](docs/02-ustanovka.md#глава-4-способы-установки)
- [Глава 5. Разметка диска](docs/02-ustanovka.md#глава-5-разметка-диска)
- [Глава 6. Загрузчик и Secure Boot](docs/02-ustanovka.md#глава-6-загрузчик-и-secure-boot)
- [Глава 7. Первичная конфигурация системы](docs/02-ustanovka.md#глава-7-первичная-конфигурация-системы)

### [Часть III. Управление пакетами и конфигурацией](docs/03-upravlenie-paketami.md)
- [Глава 8. От императивного мышления к декларативному](docs/03-upravlenie-paketami.md#глава-8-от-императивного-мышления-к-декларативному)
- [Глава 9. Флейки подробно](docs/03-upravlenie-paketami.md#глава-9-флейки-подробно)
- [Глава 10. Home Manager и управление dotfiles](docs/03-upravlenie-paketami.md#глава-10-home-manager-и-управление-dotfiles)
- [Глава 11. Оверлеи, кастомные пакеты и аналог AUR](docs/03-upravlenie-paketami.md#глава-11-оверлеи-кастомные-пакеты-и-аналог-aur)

### [Часть IV. Миграция конкретных компонентов](docs/04-migraciya-komponentov.md)
- [Глава 12. Рабочий стол, оконные менеджеры и дисплей-менеджеры](docs/04-migraciya-komponentov.md#глава-12-рабочий-стол-оконные-менеджеры-и-дисплей-менеджеры)
- [Глава 13. Сеть и подключения](docs/04-migraciya-komponentov.md#глава-13-сеть-и-подключения)
- [Глава 14. Systemd-сервисы и автозагрузка](docs/04-migraciya-komponentov.md#глава-14-systemd-сервисы-и-автозагрузка)
- [Глава 15. Оборудование и драйверы](docs/04-migraciya-komponentov.md#глава-15-оборудование-и-драйверы)
- [Глава 16. Виртуализация и контейнеры](docs/04-migraciya-komponentov.md#глава-16-виртуализация-и-контейнеры)

### [Часть V. Продвинутые темы](docs/05-prodvinutye-temy.md)
- [Глава 17. Среды разработки](docs/05-prodvinutye-temy.md#глава-17-среды-разработки)
- [Глава 18. Управление секретами](docs/05-prodvinutye-temy.md#глава-18-управление-секретами)
- [Глава 19. Мультихостовые конфигурации](docs/05-prodvinutye-temy.md#глава-19-мультихостовые-конфигурации)
- [Глава 20. Rollback, generations и garbage collection](docs/05-prodvinutye-temy.md#глава-20-rollback-generations-и-garbage-collection)
- [Глава 21. Обновление системы и каналы](docs/05-prodvinutye-temy.md#глава-21-обновление-системы-и-каналы)

### [Часть VI. Проблемы и заключение](docs/06-problemy-i-zaklyuchenie.md)
- [Глава 22. Типичные проблемы и их решения](docs/06-problemy-i-zaklyuchenie.md#глава-22-типичные-проблемы-и-их-решения)
- [Глава 23. Чеклист миграции](docs/06-problemy-i-zaklyuchenie.md#глава-23-чеклист-миграции)
- [Глава 24. Полезные ресурсы и сообщество](docs/06-problemy-i-zaklyuchenie.md#глава-24-полезные-ресурсы-и-сообщество)
- [Глава 25. Заключение](docs/06-problemy-i-zaklyuchenie.md#глава-25-заключение)

### [Приложение. Глоссарий терминов](docs/glossary.md)

---

## 🆚 Arch vs NixOS: коротко о разнице

| | Arch Linux | NixOS |
|---|---|---|
| Философия | DIY, минимализм, KISS | Декларативность, воспроизводимость |
| Конфигурация | Императивная, правки в `/etc` руками | Декларативная, `configuration.nix` |
| Пакетный менеджер | `pacman` + AUR | `nix` + Nixpkgs |
| Откат системы | Снимки ФС (btrfs/timeshift), вручную | Generations «из коробки» |
| Воспроизводимость | Нужно документировать самому | Конфиг = система |
| Кривая обучения | Средняя | Высокая на старте (Nix-язык) |

## 🗂️ Структура репозитория

```text
arch-to-nixos-guide/
├── README.md
├── LICENSE
├── assets/
│   └── banner.svg
└── docs/
    ├── 01-vvedenie-i-podgotovka.md
    ├── 02-ustanovka.md
    ├── 03-upravlenie-paketami.md
    ├── 04-migraciya-komponentov.md
    ├── 05-prodvinutye-temy.md
    ├── 06-problemy-i-zaklyuchenie.md
    └── glossary.md
```

## 🚀 Быстрый старт

Просто откройте [оглавление](#-содержание) и переходите к нужной части — гайд удобно читать прямо на GitHub.
Если хотите локальную копию:

```bash
git clone https://github.com/vanyadima/arch-to-nixos-guide.git
cd arch-to-nixos-guide
```

## 🤝 Как помочь проекту

Гайд ещё пишется, и любая помощь пригодится:

- нашли неточность или устаревшую информацию — открывайте Issue;
- хотите написать или дополнить главу — открывайте Pull Request, ориентируясь на уже готовую структуру в `docs/`;
- есть свой болезненный опыт миграции — делитесь, лучшие практические советы обычно рождаются именно так.

## 📜 Лицензия

Материалы гайда распространяются под лицензией [GNU General Public License v2.0](LICENSE). Копируйте, форкайте, переводите :)

---

<p align="center">
  Если гайд оказался полезным — поставьте ⭐, это мотивирует дописать его до конца.<br/>
  Удачи в переходе на NixOS! ❄️
</p>
