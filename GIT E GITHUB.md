**GIT E GITHUB**

1- Comandos

1.1 \- git — version  
Mostra qual é a versão do git instalada no computador.

1.2 \-  git init  
Inicializar repositório git vazio.

1.3 \- git add  
Ao fazer alterações em arquivos (adicionar, modificar, excluir, etc) no repositório, essas alterações não são registradas automaticamente no histórico do Git. Elas permanecem no seu diretório de trabalho.  
Para o registro dessas alterações, usa o comando git add.  
Isso move as alterações da pasta de trabalho para a área de staging. As alterações em staging são aquelas que serão adicionadas no próximo commit.

	1.3.1 \- git add . ou git add \-A  
	Adiciona todos os arquivos alterados.

	1.3.2 \- git add arquivo1.txt arquivo1.txt   
	Adiciona os arquivos citados.

	1.3.3 \- git add \-u  
	Adiciona apenas arquivos não estão sendo rastreados.

1.4 \- git commit  
versões que criamos do código

	1.4.1 \-  git commit \-m “Mensagem descritiva”:   
	Registra as alterações na área de staging no repositório e inclui uma mensagem descritiva. Tem que usar as aspas para adicionar a mensagem.

1.5 \-  git status:   
Verifica o estado atual do seu repositório Git. Ele fornece informações sobre o que está acontecendo no seu diretório de trabalho e na área de staging.  
Ele mostra:  
Em qual branch você está (ex: main ou feature-branch).  
Quais mudanças estão prontas para serem commitadas.  
Quais mudanças foram feitas, mas não estão preparadas para o commit.  
Quais arquivos ainda não estão sendo rastreados pelo Git

1.6 \- git branch \-M “novo nome”:  
Renomear a branch que eu me encontro.

1.7 \- git remote add origin \-link do repositório no GitHub- :  
Conecta seu repositório local ao repositório remoto no GitHub (ou em outro serviço), permitindo que você compartilhe suas alterações e colabore com outros.  
Mas só esse comando não é o suficiente. Usa o próximo comando também.  
Adicionado uma única vez, pois a conexão já foi criada.

	1.7.1 \- git remote \- v:  
Lista todas as URLs de repositórios remotos associados ao seu repositório Git local, exibindo os detalhes de forma mais "verbal" ou detalhada

1.8 \- git push \-u origin main:  
Enviar suas alterações locais para o repositório remoto que você configurou anteriormente (no caso, o repositório origin).   
 O “-u” siginica “upstream”. Ao usar \-u, você está dizendo ao Git para lembrar da relação entre sua branch local (main, neste caso) e a branch remota correspondente. Isso facilita futuros git push e git pull, pois você não precisará especificar o repositório e a branch toda vez.   
Ao executar esse comando, vai abrir uma tela pop up pedindo para fazer login no GitHub.

1.9 \- git checkout \-b “nome-nova-branch”:  
Cria uma nova branch, sai da branch que estava antes, no meu caso, eu estava na main, e aí vou para a branch nome-nova-branch. 

 	1.9.1 \- git checkout “nome-branch-existente”:  
Saio da branch atual e vou para a uma outra branch já existente.

Por ser uma nova branch, não precisa criar um novo arquivo, pode usar um arquivo já existente, assim como qualquer outro commit. 

1.10 \- git merge “nome-branch”:  
Para dar esse comando, lembre-se de usar o git checkout para ir para a branch que você deseja merge com a branch “nome-branch”.

Pegar o repositório meu ou de outra pessoa no GitHub e puxar para a minha máquina:  
1.11 \- git clone link-do-repositório  
Primeiro, deve-se criar uma pasta, na área de trabalho mesmo ou em qualquer lugar de preferência, abrir o git bash nela, e aí dar esse comando. Para visualizar tudo, só abrir a pasta no VS Code.  
O repositório clonado só vai aparecer na máquina, não vai aparecer no GitHub\!  
Para aparecer no GitHub, entra no repositório que você deseja, em cima tem uma opção chamada Fork. Aí é só clicar na opção que aparece o seu perfil.  
	1.11.1 \- git clone link-do-repositorio novo-nome  
	Ao invés de criar um repositório com o mesmo nome do clonado, estou criando um que contém as mesmas informações só que com outro nome.

Suponhamos que o arquivo que eu clonei está desatualizado, para atualizar ele com as novas informações:  
Primeiro, deve-se entrar com cd nomepasta que está localizado dentro da pasta principal, que contém o que eu quero ver.   
1.12 \- git pull:  
Contrário do Push.  
Pega o que está no repositório do GitHub para a sua máquina.

1.13 \- git pull request  
Eu mando solicitação para o dono do repositório que eu dei um fork. Normalmente faz isso quando eu mudei algo no código dele e gostaria que ele visse. Ela tem a opção de adicionar ou não essa minha mudança no projeto dela.  
Primeiro, faço alteração, crio um commit. Vou no repositório e seleciono a opção “Contribute”. Em seguida, clico em “Open pull-request” e pronto, o pull-request está feito\!  
Para eu aceitar um pull-request de alguém, vou no meu repositório, abro a aba pull-request e vejo qual que eu quero aceitar. Após selecionar a opção desejada, clico em merge pull-request " e está feito\!

1.14 \- mkdir nome-diretorio-novo  
Cria uma nova pasta.

1.15 \-  ls  
Lista conteúdo de um diretório.

1.16 \- cat nomearquivo  
Exibe conteúdo de um arquivo.

Pastas que começam com “.” são pastas ocultas. 

1.17 \- rm \-rf nomePasta  
Exclui a pasta permanentemente.  
	1.17.1 \- rm nomeArquivo  
	Exclui arquivos permanentemente.

1.18 \- touch nomearq  
Cria um arquivo novo.

1.19 \- git log  
Mostra o histórico de commits.

1.20 \- Para desfazer alterações:

1.20.1 \-  Não completadas (ou seja, não deu o comando git add .):  
git checkout \-- nome\_do\_arquivo

1.20.2 \- Completadas mas sem ter dado commit (ou seja, na staging area):   
	git reset nome\_do\_arquivo

1.20.3 \- Desfazer o commit mantendo as alterações:   
	git reset HEAD\~1  
	Isso desfaz o último commit e mantém as alterações no seu diretório de trabalho.

1.20.4 \- Desfazer o commit sem manter as alterações:  
	git reset \--hard HEAD\~1  
	Isso desfaz o último commit e remove todas as alterações do diretório de trabalho.

1.20.5 \- Desfazer um commit específico:   
	git revert \<commit\_hash\>  
	Isso cria um novo commit que desfaz as alterações do commit especificado.

	

**DICIONÁRIO**

1 \- Staging:  
A área de staging é um espaço intermediário entre o seu diretório de trabalho (onde você faz alterações nos arquivos) e o repositório Git (onde os commits são armazenados). 

2- Arquivos que não estão sendo rastreados:  
Arquivos não rastreados são aqueles que foram criados ou adicionados ao diretório do seu repositório, mas que ainda não foram adicionados à área de staging usando o comando git add. O Git não sabe nada sobre esses arquivos e não registra quaisquer alterações feitas neles.

3- Branches:  
Branches são cópias separadas do código em um projeto que permite trabalhar em alterações sem afetar a versão principal do projeto.

Por que criar branches?  
Você pode experimentar e trabalhar em diferentes partes do projeto sem tocar na versão principal ou "estável" do código.

Isso é bom porque, se acontecer um bug em uma funcionalidade específica do seu projeto,  – por exemplo, um bug na funcionalidade de criar um botão – o seu código, que antes funcionava perfeitamente e não apresentava erros, fica comprometido.

Então, ao invés de trazer esse bug para o código todo (na branch main), o mais recomendado é a criação de branches para cada funcionalidade do código, e resolver cada problema na sua branch respectiva. Assim, quando o problema for resolvido, você pode mesclar ele na branch principal. 

Além disso, usar o conceito de branch é interessante pois, em projetos maiores, cada membro da equipe pode trabalhar em uma branch diferente, sem afetar a branch principal, gerando um projeto mais “limpo” e bem organizado.   
Por fim, o uso de branches possibilita um maior controle nas mudanças feitas no projeto, o que facilita a identificação de quando e por que uma alteração foi realizada.

4- Merge  
Junção da branch alternativa com a branch principal.

6- Arquivo MarkDown (linguagem de marcação) ReadMe.md:  
Arquivo presente em muitos projetos pois ele é meio que toda a instrução, tudo que você precisa de informação que não vai estar dentro do código do projeto em si. É literalmente um "Me leia antes de começar a fazer qualquer coisa".

//alterações  
1° \- git remote add origin \<link repositório\>  
2° \- git add .  
3° \- git commit   
4° \- git push \- u origin \<nomebranch\> 

//clonar  
1° e único passo:git clone link-do-repositório