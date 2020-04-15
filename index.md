---
layout: home
---

# Guia inicial
A maneira mais fácil de usar o RoVer é: Primeiramente [Adicionar o RoVer no seu servidor](https://discordapp.com/oauth2/authorize?client_id=607617445246664759&scope=bot&permissions=402656264). Temos um exemplo de como fazer a verificação no seu servidor, tudo isso é opcional:

1. Criar um cargo (Ele pode ser chamado de qualquer coisa, mas o termo mais popular é "Verificado") Esse é o qual todos os membros verificados iram receber.
2. Mova o cargo "RoVer" para acima de todos os cargos que você queira que o bot gerencie.
3. Execute o comando `!VerifiedRole NomeExatoDoCargoAqui`, repondo o "RoleNameHere" para o nome do cargo que queiras.
4. Modifique suas permissões de canal de texto, assim somente quem tem o cargo que você criou poderá ver/ler e falar nos canais de texto.
5. Execute o comando `!CreateVerifyChannel`, que irá criar um canal de texto com instruções de verificação para novos membros.

Se você tem um grupo, você pode executar o comando `!CreateGroupRanks <IdDoGrupo>` para criar os cargos vinculados ao seu grupo.

# Oque é isso?

Somos uma versão brasileira do bot [RoVer](https://rover.link/) Hospedada pelo Fptbb e traduzido pelo RafaRB.
O RoVer é um bot do discord, com código aberto que permitirá que seus membros autentiquem com segurança a conta Roblox no seu servidor do Discord. Isso capacita sua comunidade Roblox com as seguintes vantagens:

- Falar com confiança, pois todo mundo sabe quem é quem.
- Adicionando um passo extra entre os trolls & spammers reduzindo drasticamene atividades não desejadas.
- Integrando com o seu grupo no Roblox, mostrando ranks e dando cargos baseados no do seu grupo
- O banco de dados de verificação já preenchido com milhares de contas Discord-Roblox, ou seja alguns membros já podem entrar verificados no seu servidor. 
- Após fazer a verificação no site, você precisará digitar o comando `!verificar`

# Usando o RoVer

Quando um usuário entra no servidor o RoVer automaticamente checa se o usuário está no nosso banco de dados e ele possivelmente será verificado automaticamente. Se você não estiver verificado, o sistema pedirá normalmente pra verificar-se na pagina do Ro-Ver. Após fazer a verificação no website você deverá dar `!verify` no canal escolhido para verificação.

Você provavelmente irá fazer um canal de "Como Verificar", para ajudar os seus membros na verificação, não preisa desse trabalho todo! Você pode fazer tudo isso automaticamente! Basta executar o comando `!CreateVerifyChannel`. Depois de adicionar o RoVer no seu servidor você também pode custumizar o Rover seguindo alguns comandos listados abaixo. Ah, lembrando você precisa da permissão de `Manage Server` ou o cargo `RoVer Admin` no servidor do discord que deseja usar os comandos.

<span class="warn">**Porfavor, olhe!** Para que o RoVer funcione corretamente o cargo "RoVer" deve estar acima de todos os que o mesmo irá gerenciar. Se não, o bot não irá funcionar corretamente!</span>

## Comandos
<span class="info">**Nota**: &lt;Colchetes angulares&gt; Não são argumentos *requiridos*, e os [colchetes] são argumentos *opcionais*. Esses argumentos não seram necessários na execução de um comando </span>

## Configuração do Servidor

#### Configuração de apelidos
- `!Nickname <on|off>` - Defina se um novo usuário irá ser nomeado com seu apelido do Roblox ou não. Comum `on`
- `!NicknameFormat [formato]` - Defina se o Nome de usuário irá conter o Nome de usuário do roblox, id do usuário do roblox e etc. Por exemplo, argumentos válidos: `%USERNAME%`, `%USERID%`, `%SERVER%`, `%RANK%`, `%DISCORDNAME%`, and `%DISCORDID%`. Example: `%USERNAME% - (%USERID%)`. Comum `%USERNAME%`
- `!NicknameGroup [id_do_grupo]` - O ID do grupo a ser usado para a substituição do %RANK% em apelidos. Isso permite que você faça com que seus nomes de usuário sejam tipo [isso](https://i.imgur.com/4VA1vq9.png). Observe que, se o nome do seu grupo no Roblox.com começar com algo entre colchetes como “[PVT] Private”, apenas o “[PVT]” será usado para o apelido. Caso contrário, o nome completo da classificação será usado.

#### Configuração de Canal
- `!AnnounceChannel [channel]` - Defina um canal onde o RoVer postará uma mensagem todo vez que alguém se verificar. 
- `!VerifyChannel [channel]` - Defina um canal onde o RoVer irá apagar todas as mensagens exeto as de verificação. Default `null`.
- `!CreateVerifyChannel` - Crie um categoria com dois canais. Um para ensinar a fazer a verificação, e outro para executar a verificação aos membros.

#### Outros
- `!JoinDM <on|off>` Defina se novos usuários serão ou não automaticamente direcionados à mensagem automática com instruções de verificação ao ingressar neste servidor.
- `!WelcomeMessage [welcome message]` - Defina a mensagem de boas vindas quando um usuário executar o comando `!verify`. Os argumentos válidos são: `%USERNAME%`, `%USERID%`, `%SERVER%`, `%DISCORDNAME%`, and `%DISCORDID%`. Default `Welcome to %SERVER%, %USERNAME%!`.
- `@RoVer prefix [prefix]` - Mude o prefixo do RoVerificação. (Padrão: `!`) <span class="note">**Temporariamente indisponível**</span>

### Ranks
- `!VerifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros verificados iram ganhar. Pré-Definido `nulo`.
- `!UnverifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros não verificados iram ter. Pré-Definido `nulo`.
- `!Bind <"Nome Exato Do Cargo"> <IdDoGrupo>:<IdDoRank>...` Vincula um cargo do discord a um cargo no seu grupo do roblox. Bote o nome do cargo do discord em aspas quando executar o comando (ex: !Bind "staff" id do grupo:id do rank). Porfavor veja: [Integrando Com Os Grupos Do Roblox](#integrando-com-os-grupos-do-roblox).
- `!Unbind <Nome Exato Do Cargoo>` - desvincula um bind do cargo do discord.
- `!UnbindAll` - Remova Todos os bindings dos cargos do Discord.
- `!Bindings` - Mostra uma lista de todos os cargos vinculados.
- `!CreateGroupRanks <IdDoGrupo>` - Cria todos os cargos do grupo do roblox ao discord (Se já estiver um cargo com o mesmo nome o bot irá criar outro cargo)

### Ajuda e suporte
- `!RoVer` - Exibe uma descrição do RoVer.
- `!Help` - Exibe uma lista de comandos.
- `!Support` - Ajuda? link do [servidor oficial](https://discord.gg/wHXUztT) do rover (em inglês). Ajuda em português? Também tenho!  Comunidade em português [Aqui](https://robr.page/disc)
- `!Invite` - Postarei o invite do Rover.

### Administração de usuário
- `!Update <@user>` - Verificarei um usuário sem que o mesmo digite o comando `!verificar`. Para execução desse comando Requer: Permisssão de: `"Manage Server"` Ou um cargo chamado: `"RoVer Updater"`.

### Comandos De Usuário
- `!Whois <@user>` - Obtenha o link do perfil (Do Roblox) de um usuário verificado.
- `!Verify` - Se verifique com esse comando!

## Cargos Mágicos
Os Cargos mágicos são mágicos! Eles tem super poderes, precisam apenas de um nome específico para a mágica acontecer, eles fazem com que você não precisa dar nenhuma permissão especial ao cargo, o rover irá identificar que aquela pessoa tem aquele cargo específico e irá permitir o uso do comando! Legal né!

- `RoVer Bypass` -O RoVer irá ignorar as pessoas q tem o cargo "RoVer Bypass", Então, você pode dar apelidos custumizados a uma pessoa, ou você pode atribuir um cargo a uma pessoa mesmo que ela não tenha esse cargo no grupo ou nem esteja no grupo!
- `RoVer Nickname Bypass` - A mesma coisa que o RoVer Bypass, mas apenas para nomes de usuário. Cargos ainda seram dados.
- `RoVer Admin` - o RoVer deixará todo mundo que tenha o cargo "RoVer Admin" a executar qualquer comando do rover no servidor mesmo que ele não tenha a permissão de `"MANEGE SERVER"`
- `RoVer Updater` - Com o cargo "RoVer Updater", qualquer pessoa pode executar o comando `!update` e outros comandos, menos os de admins



## Integrando Com Os Grupos Do Roblox
É possível criar ligações de grupo para manter as funções do Discord atualizadas com as classificações do grupo do Roblox. O RoVer não oferece suporte ou planeja oferecer suporte a alterações de ranks ou shouts no seu grupo do Roblox.com, e você deve ter cuidado com os bots que oferecem essa funcionalidade, pois isso apresenta um grande risco à segurança.



Vinculações de grupo podem ser feitas com o comando `!Bind`.
- O primeiro argumento no comando bind é o nome exato do cargo do discord.
  - Ah, lembre-se que isso precisa estar entre aspas ("") caso tenha um espaço.
- Depois disso, você pode passar uma quantidade ilimitada de grupos com uma lista de classificações para cada grupo.
  - Os formatos de grupos são: `<id_do_grupo>:<NumeroDoRank>` (ex. `372372:135`).
    - Você pode encontrar as classificações do grupo Roblox para cada função em um grupo Roblox na página admin> funções do grupo Roblox; é um número entre 1 e 255..
    - Você pode fornecer uma lista de classificações, como `<groupid>:<rank>,<rank>,<rank>(por exemplo `372372:135,150,250`).
    - Você pode fornecer uma série de classificações em vez de listá-las, como `1-130`, por exemplo, ( 372372:1-130,255, que contará para qualquer pessoa que tenha uma classificação entre 1 e 130 [inclusive] ou a classificação 255).
     - Você também pode vincular a classificação `0` pessoas que não estão no grupo.
  - Se o usuário atender aos requisitos de qualquer um dos grupos, ele será considerado como tendo a função.


### Exemplos

<span class="warn">**Nota**: Você precisa colocar o nome da função Discord entre aspas, se houver espaços. Se você não fizer isso, obterá resultados inesperados..</span>

- Use o seguinte comando para configurar a atribuição de uma função a todos os membros de um grupo:

  `!Bind "Group Member" 372372`

- Use o seguinte comando para configurar a atribuição de uma função aos membros de uma determinada classificação em um grupo:

  `!Bind "Group Owner" 372372:255`

- Use o seguinte comando para configurar a atribuição de uma função aos membros de uma **determinada classificação** em um grupo:

  `!Bind "High Rank" 372372:200-254` 

- Use o seguinte comando para configurar a atribuição de uma função a um conjunto específico de classificações em um grupo:

  `!Bind "Group Leaders" 372372:50,100-150,200` - Isso vinculará uma classificação para usuários com uma classificação 50, de 100 a 150 (incluindo 111, 122, etc) e a classificação 200

- Use the following command to set up giving a role to a user who meets the requirements in any of a list of groups

  `!Bind "Faction Leader" 372372:250 372838:255 29393:250-255` - This will give the user the `Faction Leader` Discord role when they are rank 250 in the first group, *or* rank 255 in the second group, *or* ranks 250 through 255 in the last group.

- Use o seguinte comando para desvincular uma função de um grupo:

  `!Unbind Group Member` Onde `Group Member` é o nome de um *Cargo do Discord*

### Grupos Virtuais

Grupos virtuais são uma maneira de vincular classificações usando o sistema de ligação de classificação de grupo para serviços externos que não precisam ser grupos Roblox, como o fórum do desenvolvedor. Atualmente, eles estão disponíveis por padrão:

#### DevForum (devforum.roblox.com)
- `DevForumNewMember` - rank "Membro" no DevForum (as of Feb 2020)
- `DevForumRegular` - "Regular" rank no DevForum (as of Feb 2020)
- `DevForumAccess` -  Acesso ao DevForum (Regular ou membro)
- `DevForumTopContributor` - Top Contribuidor no DevForum 
- `CommunitySage` - Sábio da comunidade DevForum
- `PostApproval` Membro da equipe de aprovação do DevForum Post
- `RobloxStaff` - Um membro da equipe do Roblox (baseado na classificação do DevForum)

#### Comercial & Propriedade
- `GamePass:<gamepass_id>` -  Vincula a propriedade de uma gamepass, tem o id como argumento.
- `Badge:<badge_id>` - Vincula a propriedade de uma badge, tem o id como argumento.
- `Asset:<asset_id>` - Vincula a propriedade de um asset, tem o id como argumento.
#### Usuários
- `Friend:<user_id>` - Vincula ser amigo ao usuário especificado no Roblox
- `NBC` - Sem roblox premium
- `Premium` - Vincula ao Roblox Premium

#### Afiliações de grupo
- `Ally:<group_id>`* - Vincula estar em um grupo que é aliado pelo id do grupo
- `Enemy:<group_id>`* -  Vincula estar em um grupo inimigo pelo id do grupo



Para criar uma função para todos os membros do fórum de desenvolvimento em seu servidor, use o seguinte comando:

`!Bind DevForumMember DevForum`

Para criar uma função para todos os membros que possuem um ativo específico, use o seguinte comando:

`!Bind Winner Asset:424242`

Para criar uma função para todos os membros que possuem pelo menos um dos dois ativos, use o seguinte comando:

`!Bind Winner Asset:424242 Asset:525252`

Para criar uma função para todos os membros que estão no DevForum, têm OBC ou estão no grupo 372372 como proprietário:

`!Bind DevForumOrOBC DevForum OBC 372372:255`

### Classificações em apelidos

Se você deseja que as classificações do grupo de usuários apareçam no apelido, como "[PVT] evaera", siga estas etapas:

-Verifique-se se o RANK está presente em algum lugar no formato de apelido: `!NicknameFormat %RANK% %USERNAME%`
- Configure o ID do grupo a ser usado pelos ranks: `!NicknameGroup 372372`
- O RoVer selecionará automaticamente os rótulos de classificação, portanto, se a classificação do grupo for denominada “[PVT] Private”, a RoVer usará apenas o “[PVT]” para o apelido. Se não houver um rótulo no nome da classificação, o RoVer usará o nome inteiro da classificação.

