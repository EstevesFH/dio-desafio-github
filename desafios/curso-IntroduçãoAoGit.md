# Curso: Introdução ao GIT e ao GITHUB

### Sobre o GIT

- Pode se dizer que o **GIT** é um sistema de versonamento de código distribuído e o **GITHUB** é um servidor de repositório remoto;

- Armazena dados fazendo **SHA1** e armazena meta dados por meio do **Blob, Tree e Commit**;



### SHA1

- Secure Hash Algorithm (Algoritmo de Hash Seguro);

- Conjunto de funções hash criptográficas projetadas pela NSA (Agência de Segurança Nacional dos EUA);

- Encriptação gera conjunto de characteres identificador de **40 dígitos**;



### Objetos Internos do Git

- **Blob:** Armazena dados [blob (tamanho) \0(nome)];
  
  - EX.: blob 9\0conteudo - no código o tamanho é igual a 9 pela quantidade de caracteres contando com o zero;

- **Tree:** Árvores - Armazena Blobs [tree (tamanho)\0blob];

- **Commit:** Encapsula tudo [commit (tamanho tree parente autor mensagem timestamp)];
  
  - O SHA1 desse commit é o Hash de toda essa informação;



### Chave SSH e Token

- Estabelecer conxão segura entre duas máquinas (com duas chaves - uma pública e outra privada);

- as duas máquinas seriam o servidor e a máquina local;

- **Código:** 
  
  - 1° - ssh-keygen -t ed25519 -C (e-mail);
  
  - 2° - cd/c/users/marcelo\esteves/.ssh;
  
  - 3° - cat id_ed25519.pub;



### Iniciando o Git para o GitHub

- Git config --global user.email  "E-mail";

- Git config --global user.name (nome);



### Passo a passo no ciclo de vida

* **GIT Init:** Inicializa o GIT riando na pasta referência o arquivo ".GIT";

* **Untracke:** Quando arquivo está com esse status é necessário executar o "Git add (Nome do Arquivo)";

* **Unmodified:** Quando arquivo está com esse status é necessário executar o "Git add * ";

* **Modified:** Quando arquivo está com esse status é necessário executar o "Git add.";

* **Staged:** Arquivo aguardando para ser realizado o "Git commit -m "Mensagem explicando ação realizada";

* O aquivo que estiver no **Unmodified**que for removido ele volta automaticamente para o **Untracked**;



### Adicionar Repositório Remoto

- **Git remote add (nome de identificação do link) (link https do GitHub)** - Para adicionar o repositório ao GitHub;

- **Git push (Nome de identificação especificado na anterior) master** - Empurrar para o GitHub;

- **Git remote -v**  - Verificar o(s) repositório(s) ativo;



### Resolver Problemas

- Na hora de executar o "Push" para o GitHub, poderá apresentar erro caso algum outro usuário tenha modificado pelo GitHub. Caso ocorra, ele pedirá para usar o **Git pull (Nome de identificação especificado na anterior) master** e será feito manualmente as alterações para poder enviar novamente com o "Push" recomençando o envio desde o "Git add *";
  
  










