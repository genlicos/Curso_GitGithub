---------------------------DICIONARIO---------------------------
1. Branches: ramificação ou braço;
2. Hash: código de identificação da versão;
3. Commit: Enviar pra versão;
4. Markdown: São arquivos que usam extensão .md e que utilizam uma linguagem própria que serve para instanciar do txt para o html;

---------------------------RESUMO---------------------------
1. GIT
  a. Inicia: 		  git init (dentro da pasta)
  b. Status do arquivo:	  git status
  c. Modified->Staged:    git add . 
  d. Staged->Commit:	  git commit -m "Modificações feitas"
  e. Modified->Commit:    git commit -am "Modificações feitas"
  f. Visualizando Logs:   git log --oneline
  g. Desfazer checkout:   git checkout hash (apenas checa, nao mexe no branch) git checkout nome_branch (retorna pro ultimo ponto)
  h. Desf. revert:     	  git revert hash (remove tudo feito em um unico commit passado e cria um novo commit sem as modificacoes dele. Ele permanece apenas descrito na linha branch mas sem alteracoes)
  i. Desf. reset:      	  git reset hash (apaga todos os commits posteriores porem, mantem as modificacoes nos arquivos. Serve pra unir commits)
  j. Desf. reset --hard:  git reset hash --hard  (apaga todos os commits posteriores e todas as modificacoes nos arquivos, voltando ao estado originaal daquele commit)
  k. Ignorar arquivo: 	  touch .gitignore (Criaq um arquivo e tudo listado dentro é ignorado, nao rastreia, separa a lista por linhas nova)
  l. Exibir Branch's:     git branch (* exibe o atual selecionado)
  m. Criar Branch:	  git branch nome_novo_branch 
  n. Mudar de Branch:	  git checkout branch_desejado
  o. Deletar Branch's 	  git branch -D nome_branch (-D deleta mesmo se nao houver dado merge. -d apenas se os arquivos foram dados merge com o main)
  p. Unir Branch's	  git merge nome_branch (necessita estar no main, puxa os commits dos branchs mergidos)

2. GITHUB
  a. Alias origin:	  git remote add origin endere_remoto_github	  
  b. Envio remoto: 	  git push -F origin branch_interesse (-F forca o envio dos dados sob qualquer condicao)
  c. Up-load remoto: 	  git pull origin branch_interesse
  d. Clonar:		  git clone url_projeto_git novo_nome_projeto (usado caso o projeto nao esteja no PC, origin criada automaticamente)		
---------------------------LOCAL---------------------------
1. Instalação do Git
  a. Linux
    i. Direto: apt-get install git
    ii.Com repositório: add-apt-repository ppa:git-core/ppa # apt update; apt install git

  b. Windows
    i. https://desktop.github.com/download/
    ii.https://cmder.app/ (Terminal que ja vem com GIT)

2. Configurações
  a. Usuário:
    i.  Criar: git config --global user.name "Elison Nogueira"
    ii. Visualizar: git config user.name  
  
  b. Email: 
    i. Criar: git config --global user.email "elison3@gmail.com"
    ii.Visualiar: git config user.email   

  c. Editor Principal: 
    i. Criar: git config --global core.editors subl (Para o Sublime)
    ii.Visualizar: git config core.editors
 
  d. Visualizar tudo do Git: git config --list ou git config --global --list

3. Inicializando Repositórios e trabalhando com os arquivos
  a. Inicializar: git init
  b. Status dos arquivos: git status
    i.  untracked: não monitorado: foi adicionado mas não está reconhecido pelo Git. Para ser monitorado: git add arquivo.arq
    ii. unmodified: não modificado: existe mas não existe modificação nele. 
    iii.modified: modificado: após o arquivo reconhecido ser editado. Para ser levado ao último estágio: git add arquivo.arq. Para comitar direto: git commit -am "Modificações feitas"
    iv. staged: estágio final do status, serve para criar a versão final do arquivo. Para inserir a versão final: git commit -m "Modificações feitas"

4. Visualizando Logs (Após os commits): 
  a. Visualização completa: git log
  b. Vizualizacao de log curto: git shortlog: git shortlog -sn
  c. Hash especifico: git show "hash"
  d. Variacoes:
    i.  --decorate: mais específico 
    ii. --oneline: menos especifico e uma unica linha
    iii.--author="Elison Nogueira": Filtrar pelo autor 	
    iv. --graph: Forma grafica
    v.   -sn - Mostrar apenas a quantidade de commit

5. Visualizando Diferenças (DIFF) em conteúdos e arquivos
  a. Visualiza conteúdo editado antes de ser comitado: git diff
  b. Visualiza apenas os nomes dos arquivos editados: git diff --name-only

6. Desfazendo modificações no arquivo
  a. Se estiver apenas editado: git checkout arquivo.arq
  b. Se o arquivo estiver no staged: git reset HEAD arquivo.arq
  c. Se já estiver sido comitado: 
    i.  Volta pro staged pronto pra comitar: git reset --soft hash
    ii. Volta pro modified podendo modificar o arquivo manualmente: git reset --mixed hash
    iii.Reset Bruto muito cuidado: Ignora a existência do commit: git reset --hard hash
    obs:sempre seleciona a hash anterior ao erro.

---------------------------REMOTO---------------------------
1. Crie um novo repositório no Github: https://github.com/new
2. Ajuste as chaves SSH: https://youtu.be/5L4Mj5QTLyI?si=6BNnVdcdujdf1Baa
3. Conexão do repositório local com o remoto: 
  a. Conectar: git remote add origin https://github.com/genlicos/repositorio.git
  b. Preparar: git branch -M main
  a. Enviar:   git push -u origin main
4. Enviar para repositório remoto
  a. após commitar: git remote origin main

