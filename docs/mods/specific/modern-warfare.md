---
description: Крашится игра после установки мода Modern Warfare
---
# Vic's Modern Warfare
:::danger[В чём проблема?]
Vic's Modern Warfare частично несовместим с последней версией Forge, однако эту проблему можно решить
:::

## Изменение настроек Forge
:::tip[Этот способ является рекомендуемым]
:::
1. Откройте папку игры. Это можно сделать кнопкой в лаунчере.
2. Перейдите в папку `config`
3. Найдите файл `forge.cfg` и откройте его любым текстовым редактором (например, [Notepad++](https://notepad-plus-plus.org/downloads/))
4. В открывшемся файле найдите строку `allowEmissiveItems=true` и замените значение `true` на `false`
```ini title="config/forge.cfg"
allowEmissiveItems=false
```
5. Сохраните файл и запустите игру

## Установка OptiFine
:::danger[Этот способ не является рекомендуемым]
:::
Установка OptiFine способна исправить данную проблему. Установите OptiFine по [инструкции](../optifine#forge)

## Установка более старой версии Forge
Если у вас нет модов, требующих новые версии Forge, вы можете установить Forge версии `14.23.4.2759` по [инструкции](../forge)