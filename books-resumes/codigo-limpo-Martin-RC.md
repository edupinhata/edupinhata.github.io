## Capítulo 12 - Emergência

Quatro regras do Projeto Simples

1. *Efetuar todos os testes*: se não há uma maneira fácil de verificar que o código funciona, ele é
dubitável.
2. *Sem duplicação de código*
3. *Expressar o propósito do programador*
4. *Minimizar o número de classes e métodos*

### Expressividade

Grande parte dos custos de um projeto de software está na manutenção em longo prazo. Qnto mais claro
o autor tornar seu código, enos tempo outras pessoas terão de gastar para compreendê-lo. Isso reduz
os defeitos e o custo de manutenção.

- Escolha de bons nomes;
- Mantendo pequenas as classes e funções;
- Usar uma nomenclatura padrão (padrões de projeto);
- Testes de unidade bem escritos;

  É necessário praticar!!!

### Poucas classes e métodos

Apesar de termos que tentar escrever funções e classes pequenas, devemos tentar, ao mesmo tempo,
reduzir sua quantidade, portanto minimizando tanto o tamanho quanto a quantidade de classes e
funções.

## Capítulo 13 - Concorrência

**Objetos são abstrações de procedimento. Threads são abstrações de agendamento** - James O. Coplien

### Por que concorrência?

Concorrência é uma estratégia de desacoplamento.
Desacoplar melhora consideravelmente tanto as estruturas quanto a taxa de transferência. Devemos
pensar que o aplicativo deveria como muitos minicomputadores trabalhando juntos. 
Este desacoplamento:

- Facilita a compreenção do sistema;
- Oferece recursos para separar preocupações.

### Mitos e conceitos equivocados

- *Mito -> frases mais corretas*
- A concorrência sempre melhora o desempenho -> A concorrência gera um certo aumento, tanto no
desempenho quanto na criação de código adicional.
- O projeto não muda ao criar programas concorrentes -> Uma concorrência correta é complexa, mesmo
  para problemas simples. A concorrência geralmente requer uma mudança essencial na estratégia do
  projeto.
- -> Os bugs de concorrência geralmente não se repetem, portanto são frequentemente ignorados como
  casos únicos em vez dos defeitos que realmente são.

### Princípios para proteção da concorrência

1. *Princípio da Responsabilidade Única:* O código voltado para concorrência possui seus próprios
desafios, portanto, **mantenha seu código voltado para a concorrência separado do resto do código.**
2. *Limite o escopo dos dados:* Leve a sério o encapsulamento de dados; limite severamente o acesso
a quaisquer dados que possam ser compartilhados.
3. *Use cópia de dados:* Se houver uma maneira fácil de evitar o compartilhamento de objetos, será
muito pouco provável que o código resultante cause problemas.
4. *As threads devem ser as mais independentes possíveis:* Escreva seu código de modo que cada
thread exista em seu próprio mundo, sem compatilhamento de dados.

### Métodos de Execução

1. *Producer-Consumer:* Uma ou mais threads **producer** criam alguma tarefa e colocam em um buffer
ou fila de espera. Uma ou mais threads consumer pegam a tarefa da fila de espera e a finalizam.
2. *Leitores e escritores:* Quanto existe um recurso compartilhado que serve principalmente como uma
fonte de informações para leitores, mas que de vez em quanto é atualizada por escritores. O problema
consistem em coordenar os leitores de modo que não leiam algo que um escritor esteja atualizando, e
vice-versa.
3. *Dining Philosophers (Problema dos Filósofos):* Uma mesa redonda com vários filósofos, cada um
com um garfo no seu lado esquerdo, e um prato de macarrão no meio. Os filósofos só comem o macarrão
quando estão com fome, e para isso, precisam de dois garfos. Substitua os filósofos por threads e os
garfos por recursos.


**Recomendação:** Aprenda esses algoritmos básicos e entenda suas soluções.




## Abreviações

*SRP:* Princípio de Responsabilidade Única (método/classe/componente deve ter apenas um motivo para
ser alterado).
*DIP:*
*DRY:* Princípio do Não Se Repita



