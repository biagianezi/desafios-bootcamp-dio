# Introdução do Git e Github

- Git - sistema de versionamento de código distribuído.
- Criado pelo mesmo criador do Linux, pois não gostava do outro sistema que existia na época o SVN OU CVS

### Comandos básicos para bom desempenho no terminal:

- Listar – se situar dentro do programa operacional: no Windows é (dir) no Linux/mac (ls) 
- Lista todos os diretórios dentro da pasta que estamos situados
- Navegar entre as pastas (Cd) = o comando é cd tanto pra w quanto pra Linux
- Para voltar = retroceder 1 nivel na navegação (cd ..)
- Para limpar o terminal = (cls) w / Linux (clear) ou ctrl +L
- Tab = autocompleta se eu digitar por exemplo cd W e apertar tab ele autocompleta Windows.
- Criar uma pasta = (mkdir) Windows e linux
- Comando echo printa no terminal o que vc digitar, se eu usar echo hello > hello.txt eu estou redirecionando o hello para um arquivo que criei o hello.txt
- Del + nome da pasta que vc quer deletar os arquivos = no w, deleta somente arquivos  que estao dentro do repositório (pasta)
- Setinha pra cima navega entre os comandos que usei
- Rmdir  workspace /s /q = remove o diretório (pasta workspace)
- No Linux = rm -rf workspace/ (deleta tudo dentro da pasta workspace, inclusive ela)
  - Se der tudo certo o terminal não fala nada (silêncio no sucesso)

### Como o Git funciona por baixo dos panos

SHA1 = algoritmo de encriptação, conjunto de funções hash criptográficas projetadas pela NSA

A encriptação gera conjunto de caracteres identificados de 40 digitos, é único. Se eu gerar um arquivo diferente ele gera uma hash totalmente diferente, agora se eu voltar cpmo ele era no inicio a hash do arquivo volta a ser a mesma.

#### Objetos internos do Git

###### Blobs 

Os arquivos ficam guardados dentro desse objeto que tem o tipo do objeto, o tamanho /0 e o texto do arquivo

Esse blob contem metadados do git que são o tamanho , o tipo do objeto, guarda o sha

###### Tree

Também tem metadados e aponta para um blob ou uma arvore, guarda o nome do arquivo 

![Diagrama  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image003.png)

###### Commit 

![Interface gráfica do usuário, Aplicativo  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)

 

Timestamp = data, hora, tempo que foi criado.

![Diagrama  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

Temos blobs (arquivos) , arvores que apontam pros blobs e podem apontar para outras arvores e temos o commit que da significância pra tudo isso e aponta pra avores e bloobs.

#### Chaves ssh e tokens

Chave ssh = forma de estabelecer conexão segura entre duas maquinas, chave publica e chave privada 

Token de acesso pessoal = Gera um token no git hub e guarda ele em algum lugar dai sempre que vc for fazer o login na hora da senha vc coloca o token pessoal.

#### Iniciando o git e criando um commit

Todo comando leva a palavra git na frente 

- (Git init)/ – inicio o repositório do git dentro da pasta quee estou, ela é oculta e para ver essa pasta repositório o comando é (ls -a)
- Git config

![Texto  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

~ Adicionando um arquivo chamado Markdown = forma mais humana de escrever um arquivo html ~

#### Criando um commit

- Git add *

- Git commit – m “commit inicial”

![Texto  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)



#### Passo a passo no ciclo do arquivo no git

![Tela de computador com página de internet informando algo  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

 Tínhamos um arquivo que tava untracked , o git ainda não sabia da existência dele. Fomos lá e usamos o git add ele moveu o arquivo direto pra staged (esperando pra entrar no palco).

O arquivo unmodified é o arquivo que não foi modificado, quando vc abre e altera ele ele muda na hora pra modified (o git sabe pq compara o sha1)

Se rodarmos o git add nesse modified ele entra em staged que esta esperando pra entrar em acação, mudar de grupo etc. 

Se tivermos um arquivo unmodified e removemos ele ele volta pra untracked.

Staged se prepara pra fazer parte de um commit. Quando commitamos ele deixa de ser staged e passa a ser commit e ai o commit volta a ser unmodified, ou seja, aguardando novas modificações. (ciclo)

#### O que os repositórios significam?

![Interface gráfica do usuário, Site  Descrição gerada automaticamente](file:///C:/Users/Beatriz/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

 Quando vc faz um commit ele passa a integrar o seu repositório local

Git status mostra o status do arquivo se ele ta untracked, etc

mv = comando para mover

git init – inicia o git na pasta em questão

 Para subir o repositório local para o Github = Primeiro git add . (ele pega tudo) git add nome do arquivo pega só o arquivo.

Depois : git commit -m “descrição”

Por fim: git push origin main 