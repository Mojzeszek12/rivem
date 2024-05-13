---
title: Wprowadzenie
layout: home
---
Wprowadzenie do programowamia. Jeżeli nie chcesz korzystać z mm-boilerplate, tutaj masz FAQ
----

1. W każdym naszym skrypcie zamieścić musimy podstawowy fxmanifest.lua
```lua
    fxversion 'bodacious'
    lua54 'yes'
    shared_scripts {
	    '@ox_lib/init.lua',
        'data/*.lua',
        '@mm-core/init.lua'
    }
    client_scripts {
        '@ox_core/imports/client.lua',
    }
    server_scripts {
        '@oxmysql/lib/MySQL.lua',
        '@ox_core/imports/server.lua'
    }
```
To jest podstawa jeśli chodzi o kodowanie skryptu. Dodatkowo zamieszczamy też swoje pliki w folderach:
- client
- server
- shared
- html
- json

Jeżeli z któregoś nie korzystacie, nie musicie go używać


2. Podstawowa deklaracja
```lua
    lib.onCache('ped', function(ped)
        playerPed = ped;
    end)
    playerPed = cache.ped
```

W każdym skrypcie na jego początku zapisujecie proste oświadczenie. Dzięki temu optymalizacja wzrasta. Nie musicie używać `PlayerPedId()`, tylko używacie `playerPed`