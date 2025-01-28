# WPS PROCOM

> ## PROCEDIMENTO PARA REFAZER O SISTEMA OPERACIONAL.

1. Desligue o equipamento e abra o mesmo.
2. Retire o cartão SD da placa de processamento.
3. Coloque no adptador de cartão SD para leitura no computador.

> ###### Ferramentas necessárias para refazer a imagem em sistema operacional WIMDOWS.

1. Programa para acesso via SSH do sistema operaciol via rede TCP/IP link para dowload [MOBAXTERM](https://mobaxterm.mobatek.net/download-home-edition.html).
2. Programa para criar o Pendrive ou SD Card com o sistema operacional [RUFUS](https://rufus.ie/pt_BR/#google_vignette).
3. Imagem do sistema operasional [WPS_OS](https://1drv.ms/u/s!ArXeMgbVkP2fjcxqR2bT8Sj3vNzylw?e=752ZSK)  ⚠️ **nova imagem** ⚠️

> ###### Login de acesso ao sistema operacional.

- Acesso via ssh pi@seu ip configurado, após isto ele vai solicitar uma senha que é: rsrdata
- Acesso via MOBAXTERM :

• MobaXterm permite que você inicie sessões remotas. Você só precisa clicar no botão "Sessão" para iniciar uma nova sessão.

![image](https://github.com/wimpeximport/procom/assets/171712821/2bdfe716-6a7e-4c33-a3e5-c75ad88904fb)

• Você pode editar, excluir, mover, importar ou exportar sessões clicando com o botão direito do mouse nelas na barra lateral esquerda do MobaXterm. Você também pode criar um atalho da área de trabalho para iniciar automaticamente uma sessão ou um grupo de sessões na inicialização do MobaXterm. 
Clicar com o botão direito do mouse em uma pasta de sessão permite que você inicie várias sessões de uma só vez. Pode ser muito útil quando você costuma trabalhar usando o mesmo ambiente e as mesmas sessões abertas.

![image](https://github.com/wimpeximport/procom/assets/171712821/c9b16c17-8381-46a8-b8dc-5e8d823ee241)

Remote host:		IP-address VoIP-Com device \
Specify username:	pi \
Senha:		rsrdata

• Entre em modo de super usuario atraves do terminal aberto com seguinte comando:

sudo su
Senha:		rsrdata

• Após estar em superusuário ir para a pasta bin através do terminal ocm o seguinte comando:
cd /home/procom/bin

• Agora devemos rodar o programa adequado a cada modelo de equipamento que queremos gerar a nova licença com o seguinte comando:

| Equipamento |      Comando              |
|-------------|---------------------------|
| CS46        | c_ptt --trace-level=999   |
| WPS         | c_ptt --trace-level=999   |
| PAGACon     | c_pa --trace-level=999    |
| InteX       | c_gw_cs --trace-level=999 |

• Após executar o comando adequado ao seu equipamento vai aparecer na tela as seguintes opções de configuração:

1º - Menu.\
Tipo de hardware (opção 1): digite 1.

2º - Menu.\
Número de interfaces de hardware suportadas (opção: 1):1 (para equipamentos sem amplificador embarcado) ou 2 (para equipamentos com amplificador embarcado).

3º - Menu.\
Opção bitfield (hex): deixe vazio e precione enter no teclado.

• Após este ultimo menu vai aparecer na tela a seguinte informação:

Hardware Serial No:\
ser:xxxxxxxxx\
enc-lic:UkUoe1hxDjRLS300I0lfQSVulumII3tGUD4=\
**** Estes numeros é só uma referencia para documentação ********

• Copie o numero da licença e acesse a interface web do dispositivo desta forma

Abra o google chrome ou seu navegador de preferencia e digite o seguinte comando na barra de endereço:
- Digite o IP do dispositivo na barra de endereço.
- Vá até o seguinte menu da interface Web que apareceu
    Configuration -> Main -> Licence Key
- E cole o numero de licença que foi copiado.
- Salve a informação e teste o equipamento.

Caso tenha alguma outra duvida entre em contato através de suporte técnico:

https://gvis.me/formulario/





