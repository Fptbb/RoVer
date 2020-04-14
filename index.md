---
layout: home
---
# Guia inicial
A maneira mais fácil de usar o RoVer é [Adicionar a versão hospedada](https://discordapp.com/oauth2/authorize?client_id=298796807323123712&scope=bot&permissions=402656264) no seu servidor. Tudo isso é opcional:

1. Criar um cargo —;(Ele pode ser chamado de qualquer coisa, mas o termo mais popular é "Verificado")—; Esse é o qual todos os membros verificados iram receber.
2. Mova o cargo "RoVer" para acima de todos os cargos que você queira que o bot gerencie.
3. Execute o comando `!VerifiedRole RoleNameHere`, repondo o "RoleNameHere" para o nome do cargo que queiras.
4. Modifique suas permissões de canal de texto, assim somente quem tem o cargo que você criou poderá ver/ler e falar nos canais de texto.
5. Execute o comando `!CreateVerifyChannel`, que irá criar um canal de texto con instruções de verificação para novos membros.

Se você tem um grupo, você pode executar o comando `!CreateGroupRanks <groupid>` para criar os cargos vinculados ao seu grupo.

# Oque é isso?

Somos uma versão brasileira do bot [RoVer](https://rover.link/) Hospedada pelo Fptbb.
O RoVer é um bot do discord, com código aberto que permitirá que seus membros autentiquem com segurança a conta Roblox no seu servidor do Discord. Isso capacita sua comunidade Roblox com as seguintes vantagens:

- Falar com confiança, pois todo mundo sabe quem é quem.
- Adicionando um passo extra entre os trolls & spammers reduzindo drasticamene atividades não desejadas.
- Integrando com o seu grupo no Roblox, mostrando ranks e dando cargos baseados no do seu grupo
- O banco de dados de verificação já preenchido com milhares de contas Discord-Roblox, ou seja alguns membros já podem entrar verificados no seu servidor. 
- A versão oficial do RoVer pode lidar com servidores maiores e será capaz de atualizar automaticamente as funções assim que um usuário verificar. (Se você hospedar o RoVer, o usuário precisará executar um comando para que a verificação ocorra.)

# Usando o RoVer

Quando um usuário entra no servidor o RoVer automaticamente checa se o usuário está no nosso banco de dados e ele possivelmente será verificado automaticamente. Se você não estiver verificado, o sistema pedirá normalmente pra verificar-se na pagina do Ro-Ver. Após fazer a verificação no website você deverá dar `!verify` no canal escolhido para verificação.

Você provavelmente irá fazer um canal de "Como Verificar", para ajudar os seus membros na verificação, não preisa desse trabalho todo! Você pode fazer tudo isso automaticamente! Basta executar o comando `!CreateVerifyChannel`. Depois de adicionar o RoVer no seu servidor você também pode custumizar o Rover seguindo alguns comandos listados abaixo. Ah, lembrando você precisa da permissão de `Manage Server` ou o cargo `RoVer Admin` no servidor do discord que deseja usar os comandos.

<span class="Atenção>**Porfavor, olhe!** that the "RoVer" role must be above any other roles that you want RoVer to act on. Anyone with a role that's above the RoVer role will not be able to be verified. This is just how the Discord permission system works, so please make sure to account for it!</span>

## Comandos
<span class="info">**Note**: &lt;angled brackets&gt; denote *required* arguments, and [square brackets] denote *optional* arguments. They should not be included when you run the command.</span>

You can run any of the commands that have all optional arguments by themselves to set them back to their default state.
### Configuração do Servidor
#### Configuração de apeliddos
- `!Nickname <on|off>` - Set whether or not new users will be nicknamed to their Roblox name. Default `on`.
- `!NicknameFormat [format]` - Set the nickname format, so you could have the nickname include their roblox id or discord name, for example. Available replacements are `%USERNAME%`, `%USERID%`, `%SERVER%`, `%RANK%`, `%DISCORDNAME%`, and `%DISCORDID%`. Example: `%USERNAME% - (%USERID%)`. Default `%USERNAME%`.
- `!NicknameGroup [group_id]` - The group ID to use for the %RANK% replacement in nicknames. This allows you to make your usernames look like [this](https://i.imgur.com/4VA1vq9.png). Note that if your group rank name on Roblox.com starts with something in brackets like "[PVT] Private", only the "[PVT]" will be used for the nickname. Otherwise, the entire rank name is used. Default `null`.

#### Configuração de Canal
- `!AnnounceChannel [channel]` - Defina um canal onde o RoVerificação postará uma mensagem todo vez que alguém se verificar. Default `null`.
- `!VerifyChannel [channel]` - Defina um canal onde o RoVerificação irá apagar todas as mensagens exeto as de verificação. Default `null`.
- `!CreateVerifyChannel` - Crie um categoria com dois canais. Um para ensinar a fazer a verificação, e outro para executar a verificação aos membros. Default `null`

#### Other
- `!JoinDM <on|off>` Set whether or not new users will be automatically direct messaged with verification instructions when joining this server. Default `on`.
- `!WelcomeMessage [welcome message]` - Set the message the user gets when they verify. Will be sent in DMs unless they use `!verify` command. Available replacements are `%USERNAME%`, `%USERID%`, `%SERVER%`, `%DISCORDNAME%`, and `%DISCORDID%`. Default `Welcome to %SERVER%, %USERNAME%!`.
- `@RoVer prefix [prefix]` - Mude o prefixo do RoVerificação. (Padrão: `!`)

### Ranks
- `!VerifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros verificados iram ganhar. Default `null`.
- `!UnverifiedRole [Nome Exato Do Cargo]` - Defina o cargo que os membros não verificados iram ter. Default `null`.
- `!Bind <"exact role name"> <group_id>:<rank_id> [<group_id>:<rank_id>]...` Binds Roblox group membership or group rank to a Discord role. Put the Discord role name in quotes. Please see [Integrating with Roblox Groups](#integrating-with-roblox-groups).
- `!Unbind <exact role name>` - Unbinds this role from any group ranks.
- `!UnbindAll` - Removes all group bindings configured for this server.
- `!Bindings` - Shows a list of all bound roles.
- `!CreateGroupRanks <group_id>` - Creates Discord roles from all of the roles in a given group, and then binds them to the group. (If a role already exists with a name matching a group rank, that role will be used instead of creating a new one.)

### Ajuda e suporte
- `!RoVer` - Exibe uma descrição do RoVer.
- `!Help` - Exibe uma lista de comandos.
- `!Support` - Pos
- `!Invite` - Posts an invite link for RoVer.

### Administração de usuário
- `!Update <@user>` - Forcibly update verification status of a user, same as them running `!verify`. Requires "Manage Server" or a role named "RoVer Updater".

### Comandos De Usuário
- `!Whois <@user>` - Get a link to a verified user's profile.
- `!Verify` - Verifies the user who runs this command.

## Cargos Mágicos
Magic roles are special role names that can give specific users in your server special power. There are no commands needed to use these, all you need to do is create a role in your server matching these exact names and assign them to users. These roles are checked for by name exactly, so if you create these roles on your server, ensure that they are spelled and capitalized exactly the same as they appear below.

- `RoVer Bypass` - RoVer will ignore users with a role called "RoVer Bypass", so you can give them custom names or give people a member role when they aren't actually verified or in a group.
- `RoVer Nickname Bypass` - The same as RoVer Bypass, except it only bypasses nicknames. Roles will still be given.
- `RoVer Admin` - RoVer will allow anyone with a role called "RoVer Admin" to run any of the server commands, even if they don't have Manage Server.
- `RoVer Updater` - You can also give users a role called "RoVer Updater", which will let the holder of that role run !update on others, but no other admin commands.

## Integrating with Roblox Groups
Group bindings can be created to keep Discord roles up to date with Roblox group ranks. RoVer does not support or plan to support changing group ranks or shouts on Roblox.com, and you should be wary of any bots that offer this functionality, as this introduces a major security risk.

Group bindings can be created with the `!Bind` command.
- The first argument in the Bind command is the Discord role name.
  - This needs to be in quotation marks if it has spaces
- After that, you can pass an unlimited amount of groups with a list of ranks for each group.
  - The groups are in the format `<group_id>:<rank_number>` (e.g. `372372:135`).
    - You can find the Roblox group ranks for each role in a Roblox group on the Roblox group admin > roles page; it is a number between 1 and 255.
    - You can provide a list of ranks, like `<groupid>:<rank>,<rank>,<rank>` (e.g. `372372:135,150,250`).
    - You can provide a range of ranks instead of listing them out, like `1-130`, e.g. (`372372:1-130,255`, which will count for anyone who has a rank between 1 and 130 [inclusive] or the rank 255).
     - You can also bind the rank `0` to bind rank for people who are *not* in the group.
  - If the user meets the requirements for *any* of the groups, they will be considered to have the role.

### Examples

<span class="warn">**Note**: You need to put the Discord role name in quotation marks if it has spaces. If you don't do this you will get unexpected results.</span>

- Use the following command to set up giving a role to all members of a group:

  `!Bind "Group Member" 372372`

- Use the following command to set up giving a role to members of a certain rank in a group:

  `!Bind "Group Owner" 372372:255`

- Use the following command to set up giving a role to members of a **certain range** of rank in a group:

  `!Bind "High Rank" 372372:200-254` 

- Use the following command to set up giving a role to a specific set of ranks in a group:

  `!Bind "Group Leaders" 372372:50,100-150,200` - This will bind a rank for users with a rank 50, anywhere from 100 to 150 (including 111, 122, etc), and the rank 200

- Use the following command to set up giving a role to a user who meets the requirements in any of a list of groups

  `!Bind "Faction Leader" 372372:250 372838:255 29393:250-255` - This will give the user the `Faction Leader` Discord role when they are rank 250 in the first group, *or* rank 255 in the second group, *or* ranks 250 through 255 in the last group.

- Use the following command to unbind a role from a group:

  `!Unbind Group Member` where `Group Member` is the *Discord role name*

### Virtual groups

Virtual groups are a way to bind ranks using the group rank binding system for external services that need not be Roblox groups, such as the developer forum. Currently, these are available by default:

#### DevForum (devforum.roblox.com)
- `DevForumNewMember` - "Member" rank on the DevForum (as of Feb 2020)
- `DevForumRegular` - "Regular" rank on the DevForum (as of Feb 2020)
- `DevForumAccess` - DevForum access (either regular or member)
- `DevForumTopContributor` - DevForum Top Contributor
- `CommunitySage` - DevForum Community Sage
- `PostApproval` DevForum Post Approval team member
- `RobloxStaff` - A Roblox staff member (based on DevForum rank)

#### Assets & Ownership
- `GamePass:<gamepass_id>` -  Binds ownership of a game pass, takes the id as an argument
- `Badge:<badge_id>` - Binds ownership of a badge, takes the id as an argument
- `Asset:<asset_id>` - Binds ownership of an asset, takes the id as an argument

#### Users
- `Friend:<user_id>` - Binds being a friend to the given user on Roblox
- `NBC` - No builders club or premium
- `Premium` - Roblox Premium

#### Group Affiliations
- `Ally:<group_id>`* - Binds being in a group that is allied to group_id
- `Enemy:<group_id>`* - Binds being in a group that is an enemy of to group_id

<small>* indicates a heavily-cached resource that cannot be manually cleared. The cache will expire every two hours on the official version.</small>

To create a role for all members of the dev forum in your server, use the following command:

`!Bind DevForumMember DevForum`

To create a role for all members who own a specific asset, use the following command:

`!Bind Winner Asset:424242`

To create a role for all members who own at least one of two assets, use the following command:

`!Bind Winner Asset:424242 Asset:525252`

To create a role for all members who are either in the DevForum, have OBC, or is in group 372372 as an owner:

`!Bind DevForumOrOBC DevForum OBC 372372:255`

### Ranks in nicknames

If you want users' group ranks to appear in their nickname, like "[PVT] evaera", follow these steps:

- Ensure the RANK is present somewhere in the nickname format: `!NicknameFormat %RANK% %USERNAME%`
- Configure the group id to be used for the ranks: `!NicknameGroup 372372`
- RoVer will automatically pick up on rank labels, so if the group rank is named "[PVT] Private", RoVer will only use the "[PVT]" for the nickname. If there is no label in the rank name, then RoVer will use the entire rank name instead.
