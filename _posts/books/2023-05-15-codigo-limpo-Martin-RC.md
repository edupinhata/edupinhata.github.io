---
layout: post
title: "Resumo: Código Limpo - R. C. Martin"
date: 2023-05-18 17:00 -0300
categories: livros computacao
---

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


### Cuidado com dependências entre métodos sincronizados

Dependências entre métodos sincronizados causam pequenos bugs no código concorrente. Evite usar mais 
de um método em um objeto compartilhado.
Três formas de deixar um código com um objeto compartilhado correto:
1. Bloqueio voltado para cliente
2. Bloqueio voltado para servidor
3. Servidor extra

### Mantenha pequenas as seções sincronizadas

Seções sincronizadas adicionam bloqueios que garantem que apenas uma thread rode por vez. Isto causa 
atrasos e trabalho extra, portanto deve-se proteger apenas seções críticas.

### É difícil criar códigos de desligamento corretos

Uma má implementação pode fazer com que threads fiquem travadas e o programa acabe não finalizando com sucesso.

Pense o quanto antes no desligamento do programa e faça com que ele funcione com êxito. Vai levar mais tempo do que
você espera. Revise os algoritmos existentes, pois isso é mais difícil do que você imagina.


### Teste de código com threads

Recomendações:

- Trate falhas falsas como questões relacionadas às threads.
- Primeiro, faça com que seu código sem thread funcione.
- Torne seu código com threads plugáveis;
- Torne seu código com threads ajustável;
- Execute com mais threads do que processadores;
- Execute em diferentes plataformas;
- Altere seu código para testar e forçar falhas.

Outras recomendações:

- Não ignore falhas de sistema como se fossem casos isolados;
- Não procure bugs não relacionados a threads com os relacionados a elas ao mesmo tempo. Certifique-se
de que seu código funciona sem threads.
- Faça de seu código com threads especialmente portátil de modo que possa executá-lo em várias configurações.
- Encontre maneiras de cronometrar o desempenho de seu sistema sob variadas configurações.
- Coisas acontecem quando o sistema alterna entre as tarefas. Execute mais threads do que os processadores ou núcleos presentes.
- Execute o quanto antes e frequentemente seu código com threads em todas as plataformas finais.

### Altere seu código para testar falhas

É comum que falhas se escondam em códigos concorrentes. Testes simples nem sempre conseguem expor esses erros.
Uma opção é forçar falhas de duas maneiras:

*Manualmente*

Inserir chamadas wait(), sleep(), yield() e priority() em lugares específicos para forçar falhas.

*Automátizada*

Você poderia utilizar uma classe com um único método:

'''vim
public class ThreadJigglePoint {
    public static void jiggle() {
    }
}
'''

É possível adicionar esta chamada em vários lugares no código:

'''vim
public synchronized String nextUrlOrNull() {
    if (hasNext()) {
        ThreadJigglePoint.jigle();
        String url = urlGenerator.next();
        ThreadJigglePoint.jigle();
        updateHasNext();
        ThreadJigglePoint.jigle();
        return url;
    }
    return null;
}
'''

A chamada agora pode selecionar aleatoriamente uma das ações: fazer nada, dormir ou ficar passivo.

## Abreviações

*SRP:* Princípio de Responsabilidade Única (método/classe/componente deve ter apenas um motivo para
ser alterado).
*DIP:*
*DRY:* Princípio do Não Se Repita



