---
title: Wprowadzenie
layout: home
---

[^1]: [W każdym naszym skrypcie zamieścić musimy podstawowy fxmanifest.lua]
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
1. client
2. server
3. shared
4. html
5. json

Jeżeli z któregoś nie korzystacie, nie musicie go używać


[^2]: [Drugi krok soon]
----

