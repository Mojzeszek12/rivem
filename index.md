---
title: Wprowadzenie
layout: home
---
Wprowadzenie do programowamia. Jeżeli nie chcesz korzystać z mm-boilerplate, tutaj masz FAQ
----





## 1. W każdym naszym skrypcie zamieścić musimy podstawowy fxmanifest.lua {: .d-inline-block } Nowe (v0.1.0) {: .label .label-green }

```lua
fx_version   'cerulean'
lua54        'yes'
game         'gta5'


shared_scripts {
	'@ox_lib/init.lua',
    'data/*.lua',
    '@mm-core/init.lua'
}

dependecies {
    'ox_lib',
    'ox_core'
}

client_scripts {
    'client/*',
    '@ox_core/imports/client.lua',
}

server_scripts {
	'@oxmysql/lib/MySQL.lua',
    'server/*',
    '@ox_core/imports/server.lua',
}
```
To jest podstawa jeśli chodzi o kodowanie skryptu. Dodatkowo zamieszczamy też swoje pliki w folderach:
- client (pliki po stronie klienta)
- server (pliki po stronie serwera)
- shared (wszystkie pliki konfiguracyjne)
- html (pliki związane z ui)
- json (tylko i wyłącznie pliki .json)

Jeżeli z któregoś nie korzystacie, nie musicie go używać. Małe pliki oraz zasoby wrzucamy do mm-core. Tam jest ich miejsce.


## 2. Podstawowa deklaracja
{: .d-inline-block }

Nowe (v0.1.0)
{: .label .label-green }
```lua
    lib.onCache('ped', function(ped)
        playerPed = ped;
    end)
    playerPed = cache.ped
```

W każdym skrypcie na jego początku zapisujecie proste oświadczenie. Dzięki temu optymalizacja wzrasta. Nie musicie używać `PlayerPedId()`, tylko używacie `playerPed`