0. Dicionário:
  a. branches:
  b. Markdown: São arquivos que usam extensao .md e que utilizam uma linguagem propria que serve pra estanciar do txt para p html

1. Instalação do Git
  a. Direto: apt-get install git
  b. Com repositorio: add-apt-repository ppa:git-core/ppa # apt update; apt install git

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
  b.Status dos arquivos:
    i.  untracked: nao-marcado: foi adicionado mas não esta reconhecido pelo Git.
    ii. unmodified: nao-modificado: existe mas não existe modificação nele.
    iii.modified: modificado: apos o arquivo reconhecido ser editado.
    iv. staged: estágio final do status, serve para criar a versao final do arquivo.
  c...


