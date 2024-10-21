# LifeChain_Project
 Este projeto tem como objetivo criar uma blockchain simples em Python focada na gestão de dados médicos de um paciente diabético. A blockchain armazena de forma segura e imutável os resultados de exames de sangue do paciente, como níveis de glicose e colesterol, em blocos que formam uma cadeia. Cada bloco está conectado ao anterior por meio de uma estrutura de hash, garantindo a integridade dos dados. O projeto aborda os conceitos fundamentais da blockchain, como prova de trabalho (Proof of Work), validação da cadeia, contratos inteligentes (para verificação de condições), e armazenamento de blocos em um arquivo JSON.

Este projeto tem como objetivo criar uma blockchain simples em Python focada na gestão de dados médicos de um paciente diabético. A blockchain armazena de forma segura e imutável os resultados de exames de sangue do paciente, como níveis de glicose e colesterol, em blocos que formam uma cadeia. Cada bloco está conectado ao anterior por meio de uma estrutura de hash, garantindo a integridade dos dados. O projeto aborda os conceitos fundamentais da blockchain, como prova de trabalho (Proof of Work), validação da cadeia, contratos inteligentes (para verificação de condições), e armazenamento de blocos em um arquivo JSON.

Link do mapa mental do projeto: https://www.canva.com/design/DAGT3z3lTeU/cIvC3tICvALsGkTo2OVP-Q/view?utm_content=DAGT3z3lTeU&utm_campaign=designshare&utm_medium=link&utm_source=editor

Contexto
Em um ambiente de saúde, a necessidade de manter os dados do paciente seguros e imutáveis é fundamental, especialmente em condições crônicas como o diabetes, onde o monitoramento contínuo dos níveis de glicose é crucial. Utilizar a blockchain para esse fim proporciona uma solução de armazenamento seguro, transparente e rastreável. A imutabilidade dos dados garante que os resultados de exames não possam ser alterados ou manipulados, o que é essencial para garantir a confiabilidade do histórico médico.

Componentes do Projeto
Bloco: Cada bloco armazena os dados de um exame de sangue, como níveis de glicose e colesterol, juntamente com o índice do bloco, timestamp, hash anterior, nonce (usado na prova de trabalho) e hash atual.

Blockchain: A blockchain é uma cadeia de blocos conectados de forma criptograficamente segura. Ela garante que qualquer modificação em um bloco invalida toda a cadeia, tornando a manipulação de dados praticamente impossível.
Prova de Trabalho (Proof of Work):

A prova de trabalho é um mecanismo que introduz complexidade computacional para adicionar um novo bloco à cadeia. Um novo bloco só pode ser aceito quando o hash gerado por ele atende a um critério específico (iniciado com um certo número de zeros, por exemplo).
Esse processo garante a integridade e segurança da cadeia, dificultando a adição de blocos maliciosos.
Validação da Cadeia:

A função de validação da cadeia verifica se cada bloco está corretamente vinculado ao bloco anterior e se o hash de cada bloco é válido. Isso assegura que os dados não foram alterados após serem inseridos na blockchain.
Contratos Inteligentes:

O projeto utiliza um contrato inteligente simples para verificar automaticamente os dados dos exames de sangue. Por exemplo, ele pode alertar se os níveis de glicose e colesterol estão fora dos valores considerados normais, ajudando no monitoramento da saúde do paciente.
Armazenamento em JSON:

Cada bloco é armazenado em um arquivo JSON, permitindo que os dados sejam persistidos de forma estruturada e facilmente acessível. O arquivo JSON serve como o "livro razão" da blockchain, contendo todos os blocos e suas informações detalhadas.

Fluxo de Funcionamento do Projeto
Criação do Bloco Gênesis:

Todo blockchain começa com o bloco gênesis, que é o primeiro bloco da cadeia. Ele é criado automaticamente ao inicializar a blockchain e não contém dados de exames.
Adição de Blocos:

Novos blocos são adicionados à blockchain à medida que novos exames de sangue do paciente são registrados. Para cada novo exame, os dados são inseridos e um bloco é gerado.
O bloco contém o hash do bloco anterior, conectando-o à cadeia de forma segura.
Antes de ser adicionado, o bloco passa pelo processo de prova de trabalho para validar sua entrada na blockchain.
Validação da Blockchain:

A cada novo bloco inserido, a cadeia inteira é verificada para garantir que ela permaneça íntegra e válida.
A validação ocorre verificando tanto os hashes quanto a conexão com o bloco anterior.

Armazenamento e Persistência:
Após a validação, a blockchain é salva no arquivo blockchain.json, permitindo que todos os blocos sejam persistidos em disco.
Esse arquivo pode ser compartilhado, copiado e visualizado por outros sistemas.
Contratos Inteligentes Simples
Neste projeto, os contratos inteligentes são utilizados para fazer verificações automáticas nos dados inseridos. Um exemplo de contrato poderia ser:

Tecnologias Utilizadas:
Python 3.x: Para a implementação de toda a lógica da blockchain e dos blocos.
Hashlib: Para calcular os hashes criptográficos necessários para a prova de trabalho e a segurança da blockchain.
JSON: Para armazenar a blockchain em um formato persistente, estruturado e legível por humanos.
Bibliotecas padrão do Python: Como time para gerar timestamps e json para manipular arquivos JSON.

Execução do Código:

Ao executar o código, o sistema irá criar a blockchain com o bloco gênesis.
O aluno será solicitado a inserir os dados do exame de sangue, como glicose e colesterol.

Adição de Blocos:
Após a inserção dos dados, um novo bloco será gerado e adicionado à blockchain, passando pelo processo de prova de trabalho.

Validação da Cadeia:
A blockchain será validada, garantindo que todos os blocos estejam corretamente vinculados e seguros.

Armazenamento em JSON:
A blockchain será salva em um arquivo JSON (blockchain.json), que pode ser visualizado para conferir os dados do paciente e verificar a integridade da cadeia.