# PlayStation DNS blocklists

Собранные из источников сообщества списки доменов PlayStation для DNS-фильтрации.

| Файл | Содержание |
|---|---|
| `playstation-domains.txt` | 265 уникальных доменов PS3/PS4/PS5 и сервисов PlayStation |
| `playstation-hosts.txt` | Тот же список в формате `0.0.0.0 домен` |
| `ps5-update-domains.txt` | 41 домен из списка блокировки обновлений PS5 |
| `playstation-blocklist-research.md` | Дополнительные источники и замечания |

## Использование

Добавьте нужный список в Pi-hole или AdGuard Home и применяйте его только к консоли. Для Pi-hole удобно создать отдельную группу PlayStation и назначить ей консоль и список.

Полный список затрагивает PSN, загрузку игр, трофеи и другие функции. Список обновлений PS5 также содержит два общих домена загрузки: `sgst.prod.dl.playstation.net` и `gs2.ww.prod.dl.playstation.net`; их блокировка может затрагивать загрузку контента.

Записи здесь являются точными доменами. Блокировка корневого домена с поддоменами требует отдельного wildcard/regex-правила. IPv4 Firewall Funbox не принимает эти списки напрямую.

Списки не гарантируют блокировку всех обновлений: DNS-фильтрация не закрывает прямые подключения по IP, альтернативный DNS и установку уже скачанного обновления. На конкретной консоли списки не проверены.

## Источники

Проверены и собраны 7 октября 2026 года:

- https://github.com/illusionyy/hosts/blob/main/hosts — использован раздел PlayStation, без Windows/Nvidia/Tenda.
- https://gist.github.com/HatchiFr/c4430702d1c482db358ffa9b59b66d94
- https://gbatemp.net/threads/ps5-exploit-guide.613891/
- https://4pda.to/forum/index.php?showtopic=1055759&st=1000#entry125990307 — текст предоставлен пользователем, страницу прочитать не удалось.
- https://pastebin.com/j4bdVh6y
- https://github.com/MagicStuffCL/DnsblockListPS4PS5_Adguardhome

Сравнены также списки Al-Azif и b0bfranklin; подробности в `playstation-blocklist-research.md`.

Повторы удалены. Ошибочно склеенная строка `artcdnsecure.ribob01.netapi-p014.ribob01.net` исключена. Описание назначения серверов основано на источниках сообщества, а не на собственном анализе трафика.

Лицензия на объединённый набор не назначена: условия исходных источников могут различаться.
