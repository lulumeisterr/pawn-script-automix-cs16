# Sobre
  Desenvolvimento de scripts para servidores de Counter-Strike 1.6, permitindo a inicialização automática de partidas sem depender de plugins externos que possam interferir na mecânica do jogo.
  # Features
    - Iniciar partida ao contabilizar 10 players. (Done).
    - Troca de times automaticas ao atingir a 15 rounds (Doing).
    - Inicializar votação para misturar os times. (Backlog).
    - Permitir que os jogadores renasçam de forma ilimitada até que o início do mix ocorra (Backlog).
    - Disponibilizar menu utils: (Backlog).
        - All Spec
        - Kicks e Bans
        - Inicializar o modo CPL
        - Troca de mapas
      
# Configuração de ambiente
  - Instalar o amxmodx
    - Documentação amxmodx/Instalação
      - https://wiki.alliedmods.net/Installing_AMX_Mod_X_Manually    
  - Crie/Adicione o seu arquivo de plugin ".amxx" no diretorio ``\addons\amxmodx\plugins``
      # Configuração de build
      - Instalar VSCODE
      - Abrir o projeto na raiz
        - \SteamLibrary\steamapps\common\Half-Life\cstrike\addons\amxmodx
        - Criar um plano de execução de build a partir do vscode
          - CTRL + SHIFT + B (Adicionar o json abaixo)
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
                 [{"key": "f5","command": "workbench.action.tasks.build"}]
              ```
# Habilitar script amxx.
  - Adicionar o plugin (Exemplo) "teste.amxx" a ser criado na pasta ``cstrike\addons\amxmodx\plugins``    
    - Habilitar o plugin no arquivo  ``cstrike\addons\amxmodx\configs\plugins``
    - ![image](https://github.com/lulumeisterr/pawn-script-automix-cs16/assets/25963928/95f46a01-051b-4130-8924-288fa02ef479)
      
   
