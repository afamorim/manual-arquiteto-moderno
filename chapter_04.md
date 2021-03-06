# Refatoração

Após alguns anos de estrada, todo desenvolvedor percebe que passa grande parte do seu tempo lendo código e, na maioria das vezes, código escrito por outros desenvolvedores. Sem muito esforço, ele percebe que esse tempo é superior ao tempo gasto escrevendo novas linhas de código, afinal de contas, ele precisa entender o funcionamento do código atual, onde deverá fazer suas mudanças e principalmente quais classes ou arquivos serão impactados por elas.

Não à toa, uma simples alteração no código, como adicionar um `if`, pode levar horas ou mesmo dias. Geralmente, esse alto custo para manter o software é consequência de uma péssima qualidade do código que foi escrito, afinal, quanto maior a dificuldade em ler e entender um trecho de código maior será o tempo gasto para alterá-lo. E não se engane, mesmo o desenvolvedor que implementou a funcionalidade no sistema pode ter dificuldades para ler o código após alguns meses.

Para evitar esse problema, é preciso investir na qualidade e na clareza do código atual e do código que venha a ser escrito pela equipe, dessa forma, diminuindo o custo para fazer alterações no sistema. O que eu estou querendo dizer, é que o desenvolvedor precisará melhorar o código já pronto e que funciona sem mudar o seu comportamento. E, essa técnica, conhecida por muitos profissionais, é chamada de **Refatoração** (ou do inglês Refactoring).

Uma das definições mais aceitas na indústria para "Refatoração" é a do **Martin Fowler** em seu livro **Refactoring: Improving the Design of Existing Code**, na qual diz:

> "Refatoração é uma técnica controlada para reestruturar um trecho de código existente, alterando sua estrutura interna sem modificar seu comportamento externo. Consiste em uma série de pequenas transformações que preservam o comportamento inicial. Cada transformação (chamada de refatoração) reflete em uma pequena mudança, mas uma sequência de transformações pode produzir uma significante reestruturação. Como cada refatoração é pequena, é menos provável que se introduza um erro. Além disso, o sistema  continua em pleno funcionamento depois de cada pequena refatoração, reduzindo as chances do sistema ser seriamente danificado durante a reestruturação."

Em outras palavras, refatoração é o processo de modificar um trecho de código já escrito, executando pequenos passos (**baby-steps**) sem modificar o comportamento atual do sistema. É uma técnica utilizada para melhorar algum aspecto do código, entre eles podemos citar melhorias na clareza do código para facilitar a leitura, ou também melhorias no design das classes a fim de trazer maior flexbilidade ao sistema.

## Medo de alterar código de outro programador

Todo desenvolvedor em algum momento da sua carreira entrou ou entrará no meio de um projeto de software. Isso quer dizer que ele chegou de paraquedas para desenvolver, corrigir e manter funcionalidades em cima de uma base de código existente, que pode ter desde 6 meses até 20 anos de vida. 

Essa base de código provavelmente já passou pela mão de diversos desenvolvedores, desde os mais experientes até os medianos e os estagiários, geralmente sob pressão e prazos surreais e apertados. Para piorar, dificilmente a equipe que iniciou o projeto e, tomou decisões importantes de arquitetura e de design, estará ainda na empresa. Ou seja, um sitema com 5 anos de idade pode ter trocado o time completo 2 ou 3 vezes no mínimo.

Essa alta rotatividade de profissionais traz inúmeros prejuízos à empresa, em especial ao código do sistema. Pois certos trechos de código críticos foram (e são) alterados, mantidos e evoluídos por diversos destes profissionais, uns que dominam o negócio de ponta a ponta, outros nem tanto; uns com completa maestria nas tecnologias e frameworks utilizados enquanto outros não tem a mínima idéia de como elas funcionam; já outros, utilizaram o projeto como laboratório no curto tempo que permanceram na empresa. Não é de se espantar que boa parte desse código seja repleto de gambiarras, duplicação de rotinas, abarrotados de comentários desatualizados, pouca clareza nas lógicas de negócio, alto acoplamento e baixa coesão. Não se assuste ao ter que manter uma classe ou um método com mais de 5 mil linhas de código macarrônico e totalmente ilegível.

Situações como essa são mais comuns do que a maioria dos profissionais imagina. Lidar com sistemas problemáticos dessa magnitude traz frustrução e, principalmente, **medo** para o novo desenvolvedor que acabara de entrar na empresa. Ele terá que trabalhar no código "dos outros", programando no escuro, sem ter a mínima noção se sua última alteração impacta noutras partes do sistema ou pior ainda, qual o tamanho desse impacto.

## A importância dos testes automatizados na hora refatorar

Quanto menos conhecimento no sistema o desenvolvedor tem, maior é sua insegurança na hora de alterar código e menores são as garantias de que suas alterações não causarão mais estragos ao sistema que já se encontra frágil pelo tempo. Mesmo pequenas refatorações com o intuito de melhorar a clareza ou a simplicidade do código podem gerar novos bugs, reintroduzir bugs antigos no sistema ou impactar o sistema de forma negativa.

Se refatorar código traz riscos, como o desenvolvedor pode garantir que erros não serão introduzidos nas suas refatorações?

A verdade, é que refatorar código sem uma garantia concreta de que o comportamento atual não vá mudar é um ato imprudente, pois não adianta nada melhorar o código se algo que já existe é quebrado. Essa garantia pode ser obtida de diversas maneiras, mas sem dúvida uma das melhores alternativas a um preço justo é através do uso de **testes automatizados**; uma bateria de testes de regressão mostraria rapidamente se uma determinada mudança (ou refatoração) no código mudou o comportamento da funcionalidade ou mesmo impactou outras partes do sistema. Perceba que os testes funcionam como uma rede de segurança para encorajar o desenvolvedor a refatorar código e, principalmente, a mantê-lo motivado a tornar essa prática uma constante no seu dia a dia.

Certamente é possível fazer refatorações sem uma linha de teste automatizado, muitas empresas e equipes fazem isso, contudo, não se pode ignorar que há grandes riscos envolvidos nessa prática que podem introduzir bugs ou gerar prejuízos à empresa ou cliente final. Refatorar código sem testes torna tudo mais difícil e arriscado, consome mais tempo do que o necessário, desencoraja melhorias no código e ainda exige muito mais do desenvolvedor. Um detalhe importante é que, a experiência do desenvolvedor conta bastante nesse momento, seja na hora de refatorar usando passos pequenos e seguros, analisar e mensurar o impacto de suas (possíveis) mudanças ou simplesmente decidir que não vale a pena refatorar determinado trecho de código.

Apesar da experiência do desenvolvedor fazer a diferença na hora de refatorar, as chances são de que seu gestor não o permita modificar código que funciona e já se encontra em produção.

## Refatoração contínua do código

## Sistemas legados e o ímpeto do jovem

## Qual sua motivação para refatorar o código?


### Refatorando para legibilidade
...

### Refatorando para flexibilidade
...

### Refatorando para performance
...

### Refatorando para remover duplicidade
...

### Refatorando para usar uma biblioteca
...

## Como medir a qualidade do seu código?

    - numero de linhas por metodo;
    - complexidade ciclomatica;
    - Número de métodos por classe;
    - Número de campos por classe;
    - acoplamento eferente
    - acoplamento aferente
    - Lack of Cohesion of Methods;

# Concluindo    

