# Como configurar/instalar/usar teclado `US` (Estados Unidos) no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar teclado `US` (Estados Unidos) no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to configure/install/use `US` (United States) keyboard in `Linux Ubuntu`._

## Descrição [2]

### Teclado `US` (Estados Unidos)

Um teclado US (Estados Unidos) é um tipo de teclado de computador que segue o layout de teclado padrão usado nos Estados Unidos. Ele é amplamente reconhecido por seu design de teclado QWERTY, que se refere à disposição das primeiras seis letras do teclado alfabético. O teclado US inclui letras, números e símbolos comuns usados na língua inglesa, bem como teclas de função e teclas de controle, como Enter, Shift, Ctrl e Alt. O layout do teclado US é amplamente utilizado em sistemas de computador e é considerado o padrão nos Estados Unidos e em muitos outros países de língua inglesa. No entanto, em algumas regiões, podem existir variações regionais, como o teclado britânico, que difere em alguns aspectos, como a posição da tecla Shift direita e a presença da tecla £. O teclado US é usado em grande parte do mundo e é compatível com a maioria dos sistemas operacionais e aplicativos de software.

## 1. Como configurar/instalar/usar teclado `US` (Estados Unidos) no Linux Ubuntu [1]

Para configurar/instalar/usar teclado `US` (Estados Unidos) no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`



```python
2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

```

Para configurar o teclado `US` no `Linux Ubuntu` para digitar acentos e caracteres especiais em português brasileiro, você pode seguir os seguintes passos:

3. Digite o seguinte comando para editar o arquivo de configuração do teclado: `sudo nano /etc/default/keyboard`

4. Localize a linha que começa com `XKBLAYOUT` e mude o valor para `us` para configurar o layout do teclado para US. Deve ficar assim: `XKBLAYOUT="us"`

5. Agora, você precisará adicionar as configurações do layout de teclado para que ele funcione corretamente com acentos em português brasileiro. Para fazer isso, adicione as seguintes linhas ao arquivo:

    ```
    XKBVARIANT="intl"
    XKBOPTIONS="lv3:ralt_switch,compose:menu"
    ```
    - A linha `XKBVARIANT` configura a variante do layout para `"intl"`, que é a variante que permite a digitação de caracteres acentuados em português brasileiro.

    - A linha `XKBOPTIONS` define algumas opções adicionais para o layout do teclado, como o uso da tecla `Alt Gr` para alternar entre símbolos especiais e a configuração de uma tecla de composição para acentos.

6. Salve as alterações e saia do editor de texto. No Nano, você pode fazer isso pressionando `Ctrl + O`, pressionando Enter para confirmar o nome do arquivo e, em seguida, pressionando `Ctrl + X` para sair do editor.

7. Reinicie o seu sistema para aplicar as alterações: `sudo systemctl reboot`

    Depois de reiniciar, seu teclado US deve estar configurado para digitar acentos e caracteres especiais em português brasileiro. Você pode usar a tecla `Alt Gr` (Right Alt) para acessar os acentos e caracteres especiais. Por exemplo, para digitar "á", você pode pressionar `Alt Gr + '` e, em seguida, a tecla "a".

Espero que isso ajude a configurar o teclado da maneira desejada!

### 1.2 Código completo para configurar/instalar

Para configurar/instalar/usar teclado `US` (Estados Unidos) no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NAO ha.
    ```


## Referências

[1] OPENAI. ***Configurar teclado US no ubuntu.*** Disponível em: <https://chat.openai.com/c/4c82ae10-a13a-4fa5-9579-30627664d830> (texto adaptado). ChatGPT. Acessado em: 07/12/2023 19:22.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 07/12/2023 19:22.

