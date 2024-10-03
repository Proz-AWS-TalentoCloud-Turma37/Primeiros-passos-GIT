![](./assets/hd-header.png)

## Front-End | Git e GitHub

<details>
  <summary>1. Git - História</summary>
  
  - Linus Torvalds estava insatisfeito com o BitKeeper, ferramenta de controle de versão que ele utilizava para desenvolver o [kernel do Linux](https://pt.wikipedia.org/wiki/Linux_(n%C3%BAcleo)).

  - O BitKeeper foi substituído pelo Git, que é um sistema de controle de versão de código aberto.

  - O Git é um sistema de controle de versão de código aberto, que permite aos usuários acompanhar o histórico de alterações de um repositório.

  - [Linus Torvalds](https://pt.wikipedia.org/wiki/Linus_Torvalds), que é um dos fundadores do Git, criou o Git em seu laboratório de informática, em Linus Torvalds' home.


  
</details>

<details>
  <summary>2. Git - Mas por que eu usaria um controle de versão? </summary>
  
  ### Organizar o desenvolvimento de software
  - Gerenciar manualmente as versões do seu software não será mais necessário, o Git gerencia de uma forma mais organizada e eficiente para você. 
  ![](./assets/01.png)

  - O Git oferece controle total do projeto ao desenvolvedor para, entre outras coisas:
    - Visualizar as mudanças ocorridas em cada arquivo;
    - Visualizar o estado do projeto em etapas anteriores;
    - Desfazer mudanças;
    - Desenvolver funcionalidades em paralelo.

  ### Compartilhar projetos
  - Desenvolver projetos colaborativos nem sempre é fácil. Utilizar DropBox, pen drives ou afins para compartilhar código muitas vezes resulta em dor de cabeça.
  ![](./assets/02.png)

  - Estas ferramentas foram projetadas para fins genéricos, não oferecendo aspectos importantes para uma equipe de desenvolvimento, como histórico de ações de cada colaborador, consistência entre as versões dos integrantes e fácil identificação e correção de bugs.
  ![](./assets/03.png)

  - Independe da plataforma
  ![](./assets/04.png)

  - O mercado utiliza! E o Git está entre os mais populares.
  ![](./assets/05.png)

  - Quem usa Git?
  ![](./assets/06.png)

</details>

<details>
  <summary>3. Git - Como funciona?</summary>

  - Armazenamento baseado em Snapshots e não em lista de alterações
  ![](./assets/07.png)

  - SCV Distribuído. No Git, todos os clientes possuem uma cópia completa do repositório remoto.
  ![](./assets/08.png)

  - Fluxo de trabalho
  ![](./assets/09.png)

  - Working directory
  > O diretório de trabalho é o diretório onde o Git armazena os arquivos do projeto.

  - Staging Area
  > O staging area é um espaço temporário onde os arquivos são armazenados antes de serem enviados para o repositório remoto.

  - Local repo
  > O repositório local é onde os arquivos são armazenados.

  - Remote repo
  > O repositório remoto é onde os arquivos são armazenados.
  
</details>

<details>
<summary>4. Instalando o Git</summary>
...

 - Baixe o Instalador: Acesse o site oficial do Git em https://git-scm.com/ e clique no link de download para o Windows.

 - Execute o Instalador: Após o download ser concluído, execute o instalador clicando duas vezes no arquivo baixado.

 - Configuração da Instalação: Na tela de configuração, você pode optar por usar as configurações padrão ou personalizá-las de acordo com suas preferências. Clique em "Next" para prosseguir.

 - Seleção de Componentes: Na próxima tela, deixe todas as opções selecionadas por padrão, a menos que você saiba que não precisará de algum componente específico. Clique em "Next" novamente.

 - Seleção do Editor de Texto: Escolha o editor de texto que você deseja associar com o Git. O Notepad++ é uma escolha popular para muitos desenvolvedores, mas você pode selecionar qualquer editor de sua preferência. Clique em "Next".

 - Definindo as Variáveis de Ambiente: Na tela seguinte, mantenha a opção padrão selecionada para garantir que o Git seja acessível a partir da linha de comando. Clique em "Next".

 - Escolha de HTTPS ou SSH: Na próxima tela, escolha o método que você deseja usar para acessar repositórios remotos. Para a maioria dos usuários, a opção HTTPS é suficiente. Clique em "Next".

 - Configuração do Terminal: Selecione o terminal que você prefere usar com o Git. O Git Bash é uma escolha comum para usuários do Windows. Clique em "Next".

 - Instalação: Por fim, clique em "Install" para iniciar a instalação do Git no seu sistema.
 
 - Conclusão: Após a conclusão da instalação, você pode abrir o Git Bash ou qualquer outro terminal que você selecionou e começar a usar o Git. Use o comando git --version para verificar se o Git foi instalado corretamente e exibir a versão instalada.
 ...
</details>
<details>
  <summary>5. Git - Comandos básicos</summary>

  ```bash
  # Consultas rápidas. Caso não se lembre de algum comando no decorrer da prática ou queira uma explicação mais detalhada, use os comandos abaixo:

  # O comando git help é usado para obter ajuda sobre os comandos.
  git help
  ```

  - Configurando o ambiente
  >
  ```bash
  # Identificação
  git config --global user.name "Seu nome"
  git config --global user.email "Seu email"
  
  # Verificar configurações atuais
  git config --list
  ```
  - Iniciando um projeto
  >
  ```bash
  # Para iniciar um repositório Git.
  git init
  # Este comando cria toda a estrutura que o Git necessita para funcionar. Os arquivos são criador na pasta oculta .git/
  # A partir de agora você pode desenvolver seu projeto sob controle do Git
  ```
  
  - Verificando o estado do projeto
  >
  ```bash  
  # O git status exibe as alterações ocorridas no repositório desde o último commit.
  git status  
  ```

  - Adicionando arquivos

  ```bash
  # O git add adiciona ou atualiza um arquivo da staging area.
  # Ou seja, o comando informa ao Git para rastrear o referido arquivo. Caso o arquivo já esteja sob controle do Git, ele o atualiza.

  # Adicionar somente um arquivo
  git add arquivo.txt

  # Adicionar todos os arquivos
  git add .  
  ```

  - Confirmando mudanças

  ```bash
  # git commit transfere o estado do projeto salvo na staging area para o repositório do projeto.
  # Simplificando, ele confirma as suas modificações, criando um novo estado ou "ponto de referência" para o seu projeto. Todo commit é associado à um checksum para poder ser referenciado posteriormente.

  git commit -m "Mensagem de commit"
  ```

  - Desfazendo mudanças

  ```bash
  # O comando git restore restaura o estado do arquivo para o estado anterior ao commit.
  git restore arquivo.txt
  ```  

  - Vinculando repositório local com o remoto
  
  ```bash
  # O comando git remote add adiciona um repositório remoto ao projeto.
  git remote add origin https://github.com/<usuário>/<repositório>.git
  ```

  - Enviando mudanças para o repositório remoto
  
  ```bash
  # O comando git push envia as mudanças para o repositório remoto.
  git push -u origin master
  ```

  - Atualizando o repositório remoto
  
  ```bash
  # O comando git pull atualiza o repositório remoto com as mudanças do repositório local.
  git pull
  ```

  - Clonando repositório remoto
  
  ```bash
  # O comando git clone cria um repositório local a partir de um repositório remoto.
  git clone https://github.com/<usuário>/<repositório>.git
  ```
</details>

<details>
  <summary>6. GitHub</summary>

  > GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git. Ele permite que programadores, utilitários ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo. 

  > Criar uma conta [link](https://github.com/signup)  

  ![](./assets/10.png)
</details>

<details>
  <summary>7. SSH</summary>  

  > Secure Shell é um protocolo de rede criptográfico para operação de serviços de rede de forma segura sobre uma rede insegura. O melhor exemplo de aplicação conhecido é para login remoto de utilizadores a sistemas de computadores.
  
  - Gerar chave pública e privada [link](https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)

  ![](./assets/11.png)
  
</details>

-------------------------------
Referências
 - [Mini curso de Git](https://minicursogit.github.io/#/)
 - [GIT CHEAT SHEET](https://education.github.com/git-cheat-sheet-education.pdf)

###### tags: `Git` `GitHub` `SSH` `Repositórios`