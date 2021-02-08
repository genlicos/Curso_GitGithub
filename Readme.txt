 Dicionário:
  a. branches: ramificação
  b. Hash: código de identificação da versão
  c. Commit: Enviar pra versão
  b. Markdown: São arquivos que usam extensão .md e que utilizam uma linguagem própria que serve para instanciar do txt para p html

---------------------------LOCAL---------------------------
1. Instalação do Git
  a. Direto: apt-get install git
  b. Com repositório: add-apt-repository ppa:git-core/ppa # apt update; apt install git

2.Configurações
  a.Usuário:
    i.  Criar: git config --global user.name "Elison Nogueira"
    ii. Visualizar: git config user.name  
  
  b.Email: 
    i.  Criar: git config --global user.email "elison3@gmail.com"
    ii. Visualiar: git config user.email   

  c.Editor Principal: 
    i.  Criar: git config --global core.editors subl (Para o Sublime)
    ii. Visualizar: git config core.editors
 
  d.Visualizar tudo do Git: git config --list

3. Inicializando Repositórios e trabalhando com os arquivos
  a.Inicializar: git init
  b.Status dos arquivos: git status
    i.  untracked: não monitorado: foi adicionado mas não está reconhecido pelo Git. Para ser monitorado: git add arquivo.arq
    ii. unmodified: não modificado: existe mas não existe modificação nele. 
    iii.modified: modificado: após o arquivo reconhecido ser editado. Para ser levado ao último estágio: git add arquivo.arq. Para comitar direto: git commit -am "Modificações feitas"
    iv. staged: estágio final do status, serve para criar a versão final do arquivo. Para inserir a versão final: git commit -m "Modificações feitas"

4.Visualizando Logs (Após os commits): 
  a. Visualização completa: git log ou git log --decorate (mais específico)
  b. Filtrar pelo autor: git log --author="Elison Nogueira"
  c. Log curto: git shortlog. Mostrar apenas a quantidade de commit: git shortlog -sn
  d. Forma gráfica: git log graph
  e. Especificar as mudanças em um commit a partir de uma hash: git show "hash"

5. Visualizando Diferenças (DIFF) em conteúdos e arquivos
  a. Visualiza conteúdo editado antes de ser comitado: git diff
  b. Visualiza apenas os nomes dos arquivos editados: git diff --name-only

6. Desfazendo modificações no arquivo
  a. Se estiver apenas editado: git checkout arquivo.arq
  b. Se o arquivo estiver no staged: git reset HEAD arquivo.arq
  c. Se já estiver sido comitado: 
    i.  Volta pro staged pronto pra comitar: git reset --soft hash
    ii. Volta pro modified podendo modificar o arquivo manualmente: git reset --mixed hash
    iii. Reset Bruto muito cuidado: Ignora a existência do commit: git reset --hard hash
    obs: sempre seleciona a hash anterior ao erro.

---------------------------REMOTO---------------------------
1. Crie um novo repositório no Github: https://github.com/new
2. Ajuste as chaves SSH publico e privado: https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
3. Conexão do repositório local com o remoto: 
  a.Conectar: git remote add origin https://github.com/genlicos/repositorio.git
  b. Preparar: git branch -M main
  a. Enviar: git push -u origin main
4. Enviar para repositório remoto
  a. após commitar: git remote origin main

