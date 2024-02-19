# Sobre
  Criação de script para servidores de cs 1.6 para que o mesmo inicie partidas automaticas.
# Configuração de ambiente
  - Instalar o amxmodx
  - Crie/Adicione o seu arquivo de plugin ".amxx" no diretorio ``\addons\amxmodx\plugins``
      # Configuração de build
      - Abrir o projeto na raiz
        - \SteamLibrary\steamapps\common\Half-Life\cstrike\addons\amxmodx
        - Criar um plano de execução de build
          - CTRL + SHIFT + B
          - Adicionar o json abaixo.    
           ```json
              {
                "version": "2.0.0",
                "tasks": [
                  {
                    "taskName": "Compile AMXX Plugin",
                    "type": "process",
                    "command": "${workspaceFolder}/scripting/amxxpc.exe",
                    "args": [
                      "${file}",
                      "-i${workspaceFolder}/scripting/include",
                      "-o${workspaceFolder}/plugins/${fileBasenameNoExtension}.amxx"
                    ],
                    "group": {
                      "kind": "build",
                      "isDefault": true
                    }
                  }
              ]
            }
            ```
           - Configurar tecla de atalho para executar o build.
             - CTRL + K & CTRL + S
               ![image](https://github.com/lulumeisterr/pawn-script-automix-cs16/assets/25963928/efea407d-3dc7-4488-b7c7-4c7503287b43)
              ```json
                 [{
                      "key": "f5",
                      "command": "workbench.action.tasks.build"
                  }]
              ```
# Habilitar o script.
  - Adicionar o plugin (Exemplo) "teste.amxx" a ser criado na pasta ``cstrike\addons\amxmodx\plugins``    
    - Habilitar o plugin no arquivo  ``cstrike\addons\amxmodx\configs\plugins`` 
      - ![image](https://github.com/lulumeisterr/pawn-script-automix-cs16/assets/25963928/95f46a01-051b-4130-8924-288fa02ef479)
   
