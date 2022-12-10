# palera1n-tutorial por iTalogc iOS   -     Sábado, 10 de Dezembro de 2022  -  14:17pm-brasilia

-----------------------------------------------------------------------------------------------------------------------------------------------------------

1.0 - INFORMAÇÕES ÚTEIS:

- Palera1n é um jailbreak do tipo "SEMI-TETHERED" para todos dispositivos de processadores A9 ao A11 com iOS15.0 ao 15.7.1; Ou Tethered para A9 ao A11 com iOS15.0 ao 15.3.1;

- O jailbreak do tipo "TETHERED" é somente para aparelhos com o ios15.0 até o ios15.3.1, mas esse jailbreak acaba bugando e se tornando em um semi-tethered do nada,
portanto, este tipo de jailbreak no momento pode ser considerado como sendo também um semi-tethered normal;

- Para este jailbreak funcionar perfeitamente e sem erros, você deverá executar todo processo com duas janelas de terminal abertas ao mesmo tempo, aonde o segundo terminal servirá para dois comandos extremamente importantes quase no final do processo, nos quais serão responsáveis de descrashar o processo de conexão da porta root 2222;

- O desenvolvedor recomenda instalar versões do linux ou Ubuntu superioras ao 20.04, sendo assim o mais recomendado de usar o novo "Linux Mint Cinnamon 21 - Vanessa", de preferência em dual-boot com o Windows10. No qual pode ser adquirido gratuitamente e no seu idioma preferido em: 
https://www.linuxmint.com/edition.php?id=299

- Para fazer a instalação do seu Linux Preferido é obrigatório o uso de um pendrive de no mínimo 4GB de armazenamento, e o pendrive bootável pode ser criado pelo
programa "RUFUS". O pendrive deverá ser formatado em padrão NTFS e em MBR nas configurações do rufus, selecione sua imagem iso do linux baixado e ao iniciar o processo
escolha a opção "criar imagem DD" na janela que abrir e espere o processo de criação do bootável terminar. Depois disso desligue seu pc e deixe o pendrive inserido para iniciar o processo de instalação do linux. O RUFUS poderá ser baixado no seu site oficial:
http://rufus.ie/pt_BR/

- Recomendável criar um novo disco de no mínimo 30GB a 50GB para poder instalar seu linux no seu hd. Deixe este novo disco num disco separado ao disco aonde está instalado seu sistema windows para evitar perder todo seu windows e instalar o linux por cima acidentalmente;

- Recomendado pelo desenvolvedor do Palera1n instalar no seu linux o pacote USBMUXD2, que os comandos de instalação estarão incluídos nos passos "2.0" abaixo;

- Recomendado também pelos fóruns do Jailbreak no site REDDIT a instalação das ferramentas de suporte "Apple File Conduit" e "FutureRestore", cujos comandos de
instalação de ambos estarão abaixo também.


#################################################################################################################

2.0 - COMANDOS DE PREPARAÇÃO PARA O FUTURO JAILBREAK:

IMPORTANTE:
- Cada comando deverá ser digitado na mesma ordem que estiverem listados abaixo, se der algum código de erro no terminal simplesmente ignore e pule para o próximo comando e aguarde o final da execução de cada um no terminal;
- Para evitar problemas recomendo apenas já copiar cada comando abaixo e colar no terminal, assim você eliminará todas as possibilidades de ter algum problema de comando 
digitado errado.

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.1 - INSTALAÇÃO DO USBMUXD2 E UTILIDADES FUNDAMENTAIS:
OBS: O comando do "LIBGENERAL" vai dar erro, não se preocupe que faz parte dos logs de comandos, e passe depois para os próximos comandos.


sudo apt install pip

sudo apt install git

sudo git clone --recursive https://github.com/tihmstar/usbmuxd2.git && cd usbmuxd2

sudo ./autogen.sh

sudo apt install libtoolize

sudo apt install aclocal

sudo apt install autoheader

sudo apt install automake

sudo apt install autoconf

sudo apt-get update

sudo apt-get upgrade

sudo ./autogen.sh

sudo git https://github.com/tihmstar/libgeneral.git 

sudo apt update

sudo apt upgrade

exit

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.2 - DOWNLOAD DO APLICATIVO DO PALERAIN QUE VAI SER INSTALADO NO SEU APARELHO APÓS O JAILBREAK:


sudo git clone --recursive https://github.com/pwnd2e/palera1n-3.0

sudo apt-get update

sudo apt-get upgrade

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.3 - INSTALAÇÃO DAS DEPENDÊNCIAS DO PALERA1N:
OBS: Se o último comando da lista abaixo não funcionar no seu linux teste também o comando:
sudo python3 -m pip install pyimg4


sudo add-apt-repository universe

sudo apt-get update

sudo apt install git -y

sudo apt install curl

sudo apt install libimobiledevice-utils

sudo apt install python3-pip

sudo apt install libusbmuxd-tools

sudo pip install pyimg4

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.4 - INSTALAÇÃO DO BREW E SUAS DEPENDÊNCIAS:


/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

sudo apt-get install build-essential procps curl file git

brew install libimobiledevice libirecovery

brew install wget

brew install gcc

sudo apt-get update

sudo apt-get upgrade

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.5 - INSTALAÇÃO DO OPENSSL, OPENSSH E DEPENDÊNCIAS DE SHELL:


sudo wget http://nz2.archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb

sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb

sudo apt-get install gvfs-backends

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.6 - RECOMENDAÇÕES DO REDDIT PARA FIX DE BUGS DE CONEXÃO ("APPLE FILE CONDUIT" e "FUTURERESTORE GUI"):


sudo git clone --recursive https://gitlab.gnome.org/GNOME/gvfs.git

sudo wget https://github.com/CoocooFroggy/FutureRestore-GUI/releases/download/v1.98.2/FutureRestore-GUI-Debian-1.98.2.deb

sudo dpkg -i FutureRestore-GUI-Debian-1.98.2.deb

-----------------------------------------------------------------------------------------------------------------------------------------------------------
2.7 - PASTA PRINCIPAL DO PROCESSO DO JAILBREAK:


sudo git clone --recursive https://github.com/palera1n/palera1n

#################################################################################################################
3.0 - PASSOS DO PROCESSO DO JAILBREAK:

I -   ABRIR 2 JANELAS DO TERMINAL DO SEU LINUX PARA FAZER TODO PROCEDIMENTO DO JAILBREAK;

II -  CONECTAR SEU APARELHO APPLE (IOS15) NO COMPUTADOR VIA CABO USB (DE PREFERẼNCIA ORIGINAL)

III - BOTAR MANUALMENTE O SEU APARELHO APPLE EM MODO DFU ANTES DE PROSSEGUIR COM O PROCESSO DE JAILBREAK

IV -  INICIAR O PROCEDIMENTO DE JAILBREAK EM APENAS UMA DAS DUAS JANELAS DE TERMINAL DO LINUX ABERTAS COM O COMANDO ABAIXO:
LEMBRETE: BOTE NO LUGAR DO "15.X.X" A VERSÃO DO IOS INSTALADA NO SEU DISPOSITIVO IOS
PARA FAZER JAILBREAK SEMI-TETHERED ESCREVA O COMANDO --semi-tethered DEPOIS DA SUA VERSÃO IOS NO COMANDO ABAIXO

cd palera1n

sudo ./palera1n.sh --tweaks 15.X.X


-----------------------------------------------------------------------------------------------------------------------------------------------------------
V -   QUANDO SOLICITADAS, ESCREVER AS MESMAS FRASES DE CONFIRMAÇÃO QUE VOCÊ QUER REALMENTE CORRER O RISCO DE FAZER O JAILBREAK QUANDO PEDIR NO TERMINAL.
SÃO ELAS:

Yes, pwn my idevice

Yes, do as I say


-----------------------------------------------------------------------------------------------------------------------------------------------------------
VI -   SEMPRE QUANDO APARECER A FRASE "Press any key when ready for DFU mode" NO TERMINAL, BOTE MANUALMENTE SEU APARELHO EM MODO DFU PARA PROSSEGUIR COM O PROCESSO AUTOMÁTICO NO TERMINAL. RECOMENDO QUE VOcÊ PESQUISE O MÉTODO DE DFU ESPECÍFICO PARA SEU MODELO DE APARELHO NA INTERNET E TREINE BASTANTE NO SEU APARELHO ANTES DE INICIAR O PROCESSO DE JAILBREAK, PARA EVITAR PROBLEMAS NO MEIO DO PROCEDIMENTO.


-----------------------------------------------------------------------------------------------------------------------------------------------------------
VII -  CASO ACONTEÇA DO JAILBREAK E O APARELHO CRASHAREM EM BOOTLOOP ETERNO COM A FRASE "waiting for connection no connection for 2222->22, fd = 5" NO TERMINAL, ABRA A SEGUNDA JANELA ABERTA DO TERMINAL E DIGITE CADA UM DOS COMANDOS ABAIXO PARA DESCRASHAR O APARELHO DO BOOTLOOP ETERNO. MAS JAMAIS FECHE A OUTRA JANELA DO TERMINAL, POIS O PROCESSO DE JAILBREAK VAI CONTINUAR EM DIANTE NAS DUAS JANELAS JUNTAS AO MESMO TEMPO:

sudo systemctl stop usbmuxd

sudo usbmuxd -f -p

-----------------------------------------------------------------------------------------------------------------------------------------------------------
VIII - O PROCESSO DO JAILBREAK VAI REBOOTAR SEU APARELHO NA TELA DA MAÇÃ DA APPLE PERTO DO ÚLTIMO PROCESSO DO JAILBREAK, DAÍ VAI SER PEDIDO QUE VOCÊ PONHA NOVAMENTE SEU APARELHO EM DFU PARA TERMINAR O PROCEDIMENTO E TECLE "ENTER". APÓS ISSO O JAILBREAK TERMINARÁ E SEU APARELHO LIGARÁ NORMALMENTE. NÃO TIRE O CABO USB E NEM FECHE AS JANELAS DO TERMINAL ENQUANTO VOCÊ NÃO CLICAR NO BOTÃO "INSTALL" E TAMBÉM NA OPÇÃO "DO ALL" NOS AJUSTES DO NOVO APLICATIVO DE JAILBREAK DO PALERA1N INSTALADO NO SEU APARELHO.


-----------------------------------------------------------------------------------------------------------------------------------------------------------
IX -  COMO JÁ MENCIONADO ANTES, PODE SER QUE SEU JAILBREAK TETHERED SE TRANSFORME SOZINHO NUM SEMI-TETHERED E SEU APARELHO AO DESLIGAR FIQUE CRASHADO NA TELA DE "RESTAURAÇÃO DE SOFTWARE". CASO ISSO ACONTEÇA, LEMBRE-SE QUE TODAS AS VEZES QUE SEU APARELHO DESLIGAR QUE VOCÊ PRECISARÁ DE CONECTAR VIA CABO USB DE NOVO NO LINUX E NO TERMINAL DIGITE NOVAMENTE O COMANDO ABAIXO. PARA ISSO NÃO ESQUEÇA DE BOTAR SEU APARELHO NA TELA PRETA DE DFU MANUALMENTE:

sudo ./palera1n.sh --tweaks 15.X.X

-----------------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------------------------------------------------------------------------------------------------------------------------------------

REMOVER O JAILBREAK DO PALERA1N - CASO O APARELHO BRICKE E VOCÊ NÃO CONSIGA MAIS DAR BOOT NELE:

I -  BOTE SEU APARELHO EM MODO DFU MANUALMENTE

II-  CONECTE SEU APARELHO VIA USB NO LINUX 

III- EXECUTE DOIS TERMINAIS NO LINUX

IV - NO PRIMEIRO TERMINAL DIGITE CADA COMANDO ABAIXO E DEPOIS TECLE "ENTER". NO "15.X.X" TROQUE PELA VERSãO ATUAL DO IOS INSTALADA NO SEU APARELHO:


cd palera1n

sudo ./palera1n.sh --restorerootfs 15.X.X



V -  CASO ACONTEÇA DO PROCESSO DE REMOÇÃO DO JAILBREAK NO APARELHO CRASHAREM BOOTLOOP ETERNO COM A FRASE "waiting for connection no connection for 2222->22, fd = 5" NO TERMINAL, ABRA A SEGUNDA JANELA ABERTA DO TERMINAL E DIGITE CADA UM DOS COMANDOS ABAIXO PARA DESCRASHAR O APARELHO DO BOOTLOOP ETERNO. MAS JAMAIS FECHE A OUTRA JANELA DO TERMINAL, POIS O PROCESSO DE REMOÇÃO DO JAILBREAK VAI CONTINUAR EM DIANTE NAS DUAS JANELAS JUNTAS AO MESMO TEMPO. NO FINAL DESTE PROCESSO O SEU APARELHO JÁ VAI LIGAR NORMALMENTE E SEMPRE QUE VOCÊ DESLIGAR E RELIGAR SEU APARELHO ELE NÃO CRASHARÁ MAIS NO LOOP DE RESTAURAÇÃO E TUDO DO JAILBREAK FICARÁ INATIVO DEFINITIVAMENTE NO SEU APARELHO ATÉ UM DIA QUE VOCÊ QUISER REFAZER O PROCESSO DE JAILBREAK NOVAMENTE:

sudo systemctl stop usbmuxd

sudo usbmuxd -f -p


xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
FIM DESTE SCRIPT DE TUTORIAL

