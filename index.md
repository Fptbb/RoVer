---
layout: home
---

# Guia inicial
A maneira mais fácil de usar o RoVerificação é: Primeiramente [Adicionar o RoVer no seu servidor](https://discordapp.com/oauth2/authorize?client_id=607617445246664759&scope=bot&permissions=402656264). Temos um exemplo de como fazer a verificação no seu servidor. Lembrando, tudo isso é opcional:

1. Criar um cargo (Ele pode ser chamado de qualquer coisa, mas o termo mais popular é "Verificado") Esse é o cargo que todos os membros verificados iram receber.
2. Mova o cargo "RoVer" para acima de todos os cargos que você queira que o bot gerencie.
3. Execute o comando `!VerifiedRole NomeExatoDoCargoAqui`, repondo o "RoleNameHere" para o nome do cargo que quer ligar.
4. Modifique suas permissões de canal de texto, assim somente quem tem o cargo que você criou poderá ver/ler e falar nos canais de texto.
5. Execute o comando `!CreateVerifyChannel`, que irá criar um canal de texto com instruções de verificação para novos membros.

Se você tem um grupo, você pode executar o comando `!CreateGroupRanks <IdDoGrupo>` para criar os cargos do seu grupo no discord e configura-los automaticamente ao seu grupo.

# Oque é isso?

Somos uma versão brasileira do bot [RoVer](https://rover.link/) **Verificado pelo Discord** e hospedada pelo [Fptbb](https://fptbb.com/), e com a tradução da página feita pelo [Rafaaa](https://www.roblox.com/users/187416020/profile).
O RoVer é um bot do discord, com código aberto que permitirá que seus membros verifiquem com segurança a conta Roblox no seu servidor do Discord. Isso capacita sua comunidade Roblox com as seguintes vantagens:

- Falar com confiança, pois todo mundo sabe quem é quem.
- Adicionando um passo extra entre os trolls & spammers reduzindo drasticamene atividades não desejadas.
- Integrando com o seu grupo no Roblox, mostrando ranks e dando cargos baseados no do seu grupo.
- O banco de dados de verificação já preenchido com milhares de contas Discord-Roblox, ou seja alguns membros já podem entrar verificados no seu servidor. 
- Após fazer a verificação no site, você precisará digitar o comando `!verificar`

# Usando o RoVer

Quando um usuário entra no servidor o RoVer automaticamente checa se o usuário está no nosso banco de dados e ele possivelmente será verificado automaticamente. Se você não estiver verificado, o sistema pedirá normalmente pra verificar-se na pagina do Ro-Ver. Após fazer a verificação no site você deverá dar `!verify` no canal escolhido para verificação.

Você provavelmente irá querer fazer um canal de "Como Verificar", para ajudar os seus membros na verificação, não precisa desse trabalho todo! Você pode fazer tudo isso automaticamente! Basta executar o comando `!CreateVerifyChannel`. Depois de adicionar o RoVer no seu servidor você também pode custumizar o Rover seguindo alguns comandos listados abaixo. Ah, lembrando você precisa da permissão de `Manage Server` ou o cargo `RoVer Admin` no servidor do discord que deseja usar os comandos.

<span class="warn">**ATENÇÃO!** Para que o RoVer funcione corretamente o cargo "RoVer" deve estar acima de todos os que o mesmo irá gerenciar. Se não, o bot não irá funcionar corretamente!</span>

## Comandos
<span class="info">**Note que:**: &lt;Colchetes angulares&gt; Não são argumentos *requiridos*, e os [colchetes] são argumentos *opcionais*. Esses argumentos não seram necessários na execução de um comando </span>

## Configuração do Servidor

#### Configuração de apelidos
- `!Nickname <on|off>` - Defina se um novo usuário irá ser nomeado com seu apelido do Roblox ou não. Por padrão vem `on`
- `!NicknameFormat [formato]` - Defina se o Nome de usuário irá conter o Nome de usuário do roblox, id do usuário do roblox e etc. Por exemplo, argumentos válidos: `%USERNAME%`, `%USERID%`, `%SERVER%`, `%RANK%`, `%DISCORDNAME%`, and `%DISCORDID%`. Example: `%USERNAME% - (%USERID%)`. Comum `%USERNAME%`
- `!NicknameGroup [id_do_grupo]` - O ID do grupo a ser usado para a substituição do %RANK% em apelidos. Isso permite que você faça com que seus nomes de usuário sejam tipo [isso](https://i.imgur.com/4VA1vq9.png). Observe que, se o nome do seu grupo no Roblox.com começar com algo entre colchetes como “[PVT] Private”, apenas o “[PVT]” será usado para o apelido. Caso contrário, o nome completo da classificação será usado.

#### Configuração de Canal
- `!AnnounceChannel [channel]` - Defina um canal onde o RoVer postará uma mensagem todo vez que alguém se verificar. 
- `!VerifyChannel [channel]` - Defina um canal onde o RoVer irá apagar todas as mensagens exeto as de verificação. Default `null`.
- `!CreateVerifyChannel` - Crie um categoria com dois canais. Um para ensinar a fazer a verificação, e outro para executar a verificação aos membros.

#### Outros
- `!JoinDM <on|off>` Defina se novos usuários serão ou não automaticamente direcionados à mensagem automática com instruções de verificação ao ingressar neste servidor.
- `!WelcomeMessage [welcome message]` - Defina a mensagem de boas vindas quando um usuário executar o comando `!verify`. Os argumentos válidos são: `%USERNAME%`, `%USERID%`, `%SERVER%`, `%DISCORDNAME%`, and `%DISCORDID%`. Default `Welcome to %SERVER%, %USERNAME%!`.
- `@RoVer prefix [prefix]` - Mude o prefixo do RoVerificação. (Padrão: `!`) <span class="note">**Cuidado, esse comando pode cair as vezes (oscilar).**</span>

### Ranks
- `!VerifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros verificados iram ganhar. Pré-Definido `nulo`.
- `!UnverifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros não verificados iram ter. Pré-Definido `nulo`.
- `!Bind <"Nome Exato Do Cargo"> <IdDoGrupo>:<IdDoRank>...` Vincula um cargo do discord a um cargo no seu grupo do roblox. Bote o nome do cargo do discord em aspas quando executar o comando (ex: !Bind "staff" id do grupo:id do rank). Porfavor veja: [Integrando Com Os Grupos Do Roblox](#integrando-com-os-grupos-do-roblox).
- `!Unbind <Nome Exato Do Cargoo>` - desvincula um bind do cargo do discord.
- `!UnbindAll` - Remova Todos os bindings dos cargos do Discord.
- `!Bindings` - Mostra uma lista de todos os cargos vinculados.
- `!CreateGroupRanks <IdDoGrupo>` - Cria todos os cargos do grupo do roblox ao discord (Se já estiver um cargo com o mesmo nome o bot irá criar outro cargo)

### Ajuda e suporte
- `!ajuda` - Exibe uma lista de comandos.
- `!Invite` - Postarei o invite do Roverificação.

<span class="info">**Servidores de Suporte** - Suporte em inglês: Link do [servidor oficial](https://discord.gg/wHXUztT) do Rover (em inglês). </span>

<span class="info">**Servidores de Suporte** - Suporte em Português [Aqui!](robr.page/disc) Lembre-se de procurar o fptbb para ajuda. </span>

### Administração de usuário
- `!atualizar <@user>` - Verificarei um usuário sem que o mesmo digite o comando `!verificar`. Para execução desse comando Requer: Permisssão de: `"Manage Server"` Ou um cargo chamado: `"RoVer Updater"`.

### Comandos De Usuário
- `!queme <@user>` - Obtenha o link do perfil (Do Roblox) de um usuário verificado.
- `!verificar` - Se verifique com esse comando!

## Cargos Mágicos
Os Cargos mágicos são mágicos! Eles tem super poderes, precisam apenas de um nome específico para a mágica acontecer, eles fazem com que você não precise dar nenhuma permissão especial ao cargo, o roverificação irá identificar que aquela pessoa tem aquele cargo específico e irá permitir o uso do comando! Legal né!

- `RoVer Bypass` -O RoVerificação irá ignorar as pessoas q tem o cargo "RoVer Bypass", Então, você pode dar apelidos customizados a uma pessoa, ou você pode atribuir um cargo a uma pessoa mesmo que ela não tenha esse cargo no grupo ou nem esteja no grupo!
- `RoVer Nickname Bypass` - A mesma coisa que o RoVer Bypass, mas apenas para nomes de usuário. Cargos ainda seram dados.
- `RoVer Admin` - O RoVerificação deixará todo mundo que tenha o cargo "RoVer Admin" a executar qualquer comando do roverificação no servidor mesmo que ele não tenha a permissão de `"MANEGE SERVER"`
- `RoVer Updater` - Com o cargo "RoVer Updater", qualquer pessoa pode executar o comando `!update` e outros comandos, menos os de admins



## Integrando Com Os Grupos Do Roblox
É possível criar ligações de grupo para manter os cargos do Discord atualizadas com as do grupo do Roblox. O RoVerificação não oferece suporte ou planeja oferecer suporte a alterações de ranks ou shouts no seu grupo do Roblox.com, e você deve ter cuidado com os bots que oferecem essa funcionalidade, pois isso apresenta um grande risco à segurança. Caso queira um bot que faça esse tipo de modificação, aconselho criar seu proprio, um bom começo e criando uma copia identica do RoVer, como essa. Mas voltando ao assunto principal:



Vinculações de grupo podem ser feitas com o comando `!Bind`.
- O primeiro argumento no comando bind é o nome exato do cargo do discord.
  - Ah, lembre-se que ele precisa estar entre aspas ("") caso tenha um espaço.
- Depois disso, você pode passar uma quantidade ilimitada de grupos com uma lista de classificações para cada grupo.
  - Os formatos de grupos são: `<id_do_grupo>:<NumeroDoRank>` (ex. `372372:135`).
    - Você pode encontrar os ranks do grupo Roblox para cada role em um grupo Roblox na página Configurar grupo > Funções no Roblox; é um número entre 1 e 255..
    - Você pode fornecer uma lista de ranks, como `<groupid>:<rank>,<rank>,<rank>(por exemplo `372372:135,150,250`).
    - Você pode fornecer uma série de ranks em vez de listá-las, como `1-130`, por exemplo, ( 372372:1-130,255, que contará para qualquer pessoa que tenha uma classificação entre 1 e 130 [inclusive 130] ou a classificação 255).
     - Você também pode vincular o rank `0` a pessoas que não estão no grupo.
  - Se o usuário atender aos requisitos de qualquer um dos grupos, ele ira receber o cargo.


### Exemplos

<span class="warn">**Nota**: Você precisa colocar o nome do cargo do Discord entre aspas, se houver espaços. Se você não fizer isso, obterá resultados inesperados..</span>

- Use o seguinte comando para configurar a atribuição de uma função a todos os membros de um grupo:

  `!Bind "Membro" 3137245`

- Use o seguinte comando para configurar a atribuição de uma função aos membros de uma determinada classificação em um grupo:

  `!Bind "Dono do Grupo" 3137245:255`

- Use o seguinte comando para configurar a atribuição de uma função aos membros de uma **determinada classificação** em um grupo:

  `!Bind "Rank Alto" 3137245:200-254` 

- Use o seguinte comando para configurar a atribuição de uma função a um conjunto específico de classificações em um grupo:

  `!Bind "Lider de Grupo" 3137245:50,100-150,200` - Isso vinculará uma classificação para usuários com uma classificação 50, de 100 a 150 (incluindo 111, 122, etc) e a classificação 200

- Use o comando a seguir para dar um cargo a um membro que conclua qualquer um dos requerimentos nessesarios para tal.

  `!Bind "Lider de Facção" 3137245:250 5943549:255 5099039:250-255` - Isso vai dar ao usuario o cargo `Lider de Facção` no discord quando ele for rank 250 no primeiro grupo, *or* rank 255 no segundo grupo, *or* ranks 250 ate 255 no terceiro.

- Use o seguinte comando para desvincular uma role de um grupo:

  `!Unbind `Membro` Onde `Membro` é o nome de um *Cargo do Discord*

### Grupos Virtuais

Grupos virtuais são uma maneira de vincular classificações usando o sistema de "bind" de classificação de grupo para serviços externos que não precisam ser grupos Roblox, como o fórum do desenvolvedor. Atualmente, eles estão disponíveis por padrão:

#### DevForum (devforum.roblox.com)
- `DevForumNewMember` - rank "Membro" no DevForum
- `DevForumRegular` - "Regular" rank no DevForum
- `DevForumAccess` -  Acesso ao DevForum (Regular ou membro)
- `DevForumTopContributor` - Top Contributor no DevForum 
- `CommunitySage` - Community Sage no DevForum
- `PostApproval` Membro da equipe de aprovação de Topicos no DevForum
- `RobloxStaff` - Um membro da equipe do Roblox (baseado na classificação do DevForum)

#### Comercial & Propriedade
- `GamePass:<gamepass_id>` -  Use com o id de uma gamepass pra dar um cargo a quem tem ela.
- `Badge:<badge_id>` - Use com o id de uma badge pra dar um cargo a quem tem ela.
- `Asset:<asset_id>` - Use com o id de uma asset (roupa, imagem, model) pra dar um cargo a quem tem ela.
#### Usuários
- `Friend:<user_id>` - Use com o id de um player para dar um cargo aos amigos desse player.
- `NBC` - Use para dar um cargo a quem não tiver cargos pagos.
- `Premium` - Use para dar um cargo a quem tiver Premium.

#### Afiliações de grupo
- `Ally:<group_id>`* - Use com o id de um grupo para dar um cargo aos aliados desse grupo.
- `Enemy:<group_id>`* -  Use com o id de um grupo para dar um cargo aos inimigos desse grupo.



Para criar uma função para todos os membros do DevForum em seu servidor, use o seguinte comando:

`!Bind DevForumMember DevForum`

Para criar uma função para todos os membros que possuem um Asset específico, use o seguinte comando:

`!Bind "Vencedor do Concurso" Asset:424242`

Para criar uma função para todos os membros que possuem pelo menos um dos dois Assets, use o seguinte comando:

`!Bind "Vencedor do Concurso" Asset:424242 Asset:525252`

Para criar uma função para todos os membros que estão no DevForum, têm OBC ou estão no grupo 3137245 como proprietário:

`!Bind DevForumOrOBC DevForum OBC 3137245:255`

### Classificações em apelidos

Se você deseja que as classificações do grupo de usuários apareçam no apelido, como "[PVT] fptbb", siga estas etapas:

-Verifique-se se o RANK está presente em algum lugar no formato de apelido: `!NicknameFormat %RANK% %USERNAME%`
- Configure o ID do grupo a ser usado pelos ranks: `!NicknameGroup 372372`
- O RoVerificação selecionará automaticamente os rótulos de classificação, portanto, se a classificação do grupo for denominada “[PVT] Private”, a RoVer usará apenas o “[PVT]” para o apelido. Se não houver um rótulo no nome da classificação, o RoVer usará o nome inteiro da classificação.

<span class="info">**Informações Atualizadas Em**: 21/05/2020 às 16:15 horas pelo horário de Brasília por [Rafaaa](https://www.roblox.com/users/187416020/profile) </span>
