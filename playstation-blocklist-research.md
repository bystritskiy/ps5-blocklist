# Дополнительные списки сообщества — 7 октября 2026

## Точные домены
Общий список обновлён до 265 доменов. Добавлены из MagicStuffCL:
- ecode.np.cs.playstation.net
- ps4updptl.us.np.community.playstation.net (PS4, сохранён в общем списке)
Назначение ecode отдельно не подтверждено; включение основано на списке автора, а не проверке трафика консоли.

## Источники
- https://github.com/MagicStuffCL/DnsblockListPS4PS5_Adguardhome
- https://github.com/b0bfranklin/Playstation_Blocklists
- https://gist.github.com/Al-Azif/296c7a4319c2fe3b597d96206213cdb6
- https://gist.github.com/Al-Azif/6982e30a9653f48c88d0f5a6a8778d05
- https://github.com/idlesauce/PS5-Exploit-Host

Список b0bfranklin не добавил новых точных доменов. Региональные PS5-адреса из конфигурации Al-Azif уже присутствуют.
MagicStuffCL также блокирует сторонние игровые сервисы; эти правила не перенесены в список PlayStation.

## Блокировка зон с поддоменами
Al-Azif использует playstation.com, playstation.net, playstation.org, scea.com, sonyentertainmentnetwork.com, sie-rd.com с охватом поддоменов.
Это отдельная широкая политика блокировки PSN/Sony, не список только обновлений. Добавление корневого домена как точной записи не эквивалентно блокировке поддоменов.
idlesauce по умолчанию блокирует имена, содержащие playstation, sonyentertainmentnetwork, scea. Это ещё более широкое сопоставление.
В Pi-hole такие зоны следует оформлять правилами wildcard/regex только для группы консоли.

manuals.playstation.net и www.playstation.com в конфигурации Al-Azif используются также для перенаправления на локальный exploit host. Не добавлены как новые обязательные запреты.

DNS-фильтрация не гарантирует запрет прямых IP-подключений, обходного DNS или установки уже скачанного обновления. Проверка на конкретной консоли не проводилась.
