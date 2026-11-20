# OKX robô de trading: quais estratégias existem, quanto custa usar e qual escolher primeiro? (as 7 opções comparadas)

A OKX lista sete robôs de trading na versão atual da sua central de ajuda, atualizada em outubro de 2026: Spot grid, Smart arbitrage, Spot DCA (Martingale), Recurring buy, Iceberg orders, TWAP e Smart portfolio. Nenhum deles tem mensalidade ou plano pago. O custo que sai do seu bolso é a taxa de negociação de cada ordem que o robô envia, e a OKX não publica esses números na documentação dos bots.

Se você quer só o resumo: mercado lateral pede Spot grid, acumulação de longo prazo pede Recurring buy, carteira com várias moedas pede Smart portfolio. O resto exige entender contrato perpétuo, slippage ou alavancagem.

> **Para quem já decidiu:** todos os bots ficam em Trade → Trading bots, dentro da conta. 👉 [Criar conta na OKX e abrir o painel de robôs](https://okx.com/join/CASH20)

## As 7 estratégias lado a lado

| Estratégia | Como funciona | Para quem | Limite que importa | Custo |
| --- | --- | --- | --- | --- |
| **Spot grid** | Compra e vende dentro de uma faixa de preço que você define | Iniciantes | Até 1.000 grids | Sem mensalidade; taxa por ordem |
| **Spot DCA (Martingale)** | Compra em intervalos e em faixas de preço menores até o alvo de saída | Quem aceita comprar na queda | Reserva mínima de Initial Order + First Safety Order | Sem mensalidade; taxa por ordem |
| **Recurring buy** | Compra no automático em intervalos fixos, com saldo em USDT | Longo prazo, sem acompanhamento | Até 20 criptomoedas | Sem mensalidade; taxa por ordem |
| **Smart portfolio** | Rebalanceia a carteira quando um ativo foge do percentual definido | Quem já tem posições | Até 10 criptomoedas | Sem mensalidade; taxa por ordem |
| **Smart arbitrage** | Delta neutro: compra à vista e vende o mesmo tanto no perpétuo | Quem entende taxa de financiamento | Modos Custom e Smart | Sem mensalidade; taxa por ordem |
| **Iceberg orders** | Quebra uma ordem grande em pedaços pequenos | Quem movimenta volume alto | Spot, perpétuo, futuro, margem e opções | Sem mensalidade; taxa por ordem |
| **TWAP** | Distribui a ordem grande ao longo do tempo | Quem monta ou desmonta posição grande | Slippage por Var. ou Ratio | Sem mensalidade; taxa por ordem |

Nenhuma linha dessa tabela tem preço de assinatura porque a OKX não vende os bots separadamente. Você paga a taxa da exchange, igual a qualquer ordem manual.

## O que a OKX chama de robô de trading

São ferramentas que executam ordens com base em regras definidas antes, sem você precisar acompanhar o gráfico. A própria OKX descreve o mecanismo como substituição do julgamento subjetivo por modelos matemáticos e algoritmos que analisam histórico de preços em busca de padrões com maior probabilidade de repetir. Na prática, isso significa duas coisas: o robô não decide por você o que é uma boa operação, e ele continua enviando ordens enquanto você está longe da tela.

A documentação da OKX classifica Spot grid, Smart portfolio e Recurring buy como os bots mais simples de operar. Iceberg e TWAP ficam para quem já lida com perfis de risco mais complexos, porque envolvem execução fatiada e controle de slippage.

## Spot grid: comece por aqui se você tem uma faixa de preço em mente

O Spot grid funciona assim: você define um teto e um piso de preço. Quando o ativo sobe até uma linha da grade, o robô vende; quando cai até uma linha, ele compra. As ordens ficam penduradas entre esses dois limites e se repetem enquanto o preço oscilar dentro da faixa.

O limite atual é de **1.000 grids**, contra 300 na versão anterior. A OKX chegou nesse número com um mecanismo dinâmico de ordens, avisos na interface e ordens de lógica desabilitadas com dica explicativa. Você pode montar a grade na mão ou usar a **estratégia de IA**, que parte de movimentos históricos e dados de backtest para sugerir os parâmetros.

Um detalhe que muda a conta no fim do mês: a integração com o **Simple Earn**. O dinheiro parado fora da faixa de negociação gera rendimento automaticamente e volta para a estratégia quando o mercado se move. Quando você encerra o robô, todos os fundos, incluindo os juros acumulados, retornam para a sua conta.

Vale testar com a faixa que o preço realmente percorreu nas últimas semanas. Faixa larga demais gera poucas execuções; faixa estreita demais faz o preço furar o teto ou o piso em pouco tempo. 👉 [Configurar um Spot grid na OKX](https://okx.com/join/CASH20)

## Spot DCA (Martingale): para quem aceita comprar enquanto cai

Esse robô compra o ativo em intervalos definidos e distribui as entradas em vários níveis de preço, vendendo quando o alvo de lucro é atingido ou quando o preço sobe. A diferença em relação a um DCA comum está na margem de manobra: você escolhe o momento de entrada com indicadores técnicos (as *Flexible start conditions*) e só precisa reservar o **Initial Order + First Safety Order** na criação.

Os fundos seguintes entram depois, conforme a estratégia for acionando as ordens de segurança. Existe também o recurso de **ciclos contínuos** (*Continuous trading cycles*), que mantém o robô rodando entre uma queda e uma recuperação e inicia um novo ciclo após bater o alvo de saída.

Quem não tem caixa para reforçar posição em queda prolongada deve passar longe. O desenho do Martingale pressupõe capital disponível nas quedas.

## Recurring buy: até 20 moedas, uma configuração

O Recurring buy compra cripto em intervalos que você escolhe, usando o saldo em **USDT** da conta. Dá para montar uma cesta com até **20 criptomoedas** de uma vez, o que resolve o caso de quem quer diversificar sem abrir ordem por ordem. Também é possível programar compras com cartão de crédito ou débito pela área **Buy Crypto**.

Para quem só quer acumular posição no longo prazo, esse é o bot que basta. Não tem parâmetro de faixa, não tem alvo de saída e não exige leitura de gráfico.

## Smart portfolio: 10 moedas e dois gatilhos de rebalanceamento

Você define o percentual de cada moeda na carteira, até **10 ativos**, e o robô compra e vende para voltar à proporção original quando ela sai do lugar. A OKX usa um exemplo simples: 25% ETH, 25% SOL e 50% BTC. Se o BTC subir muito e passar de 80% da carteira, o robô vende parte do BTC e compra ETH e SOL.

Existem dois modos de disparo. No **Scheduled**, o robô checa as proporções em intervalos fixos que você determina e corrige o desvio que encontrar. No **Proportional**, ele só age quando o desequilíbrio atinge o percentual que você definiu, como 5% de desvio.

Esse é o bot com menos execuções entre os sete, o que ajuda em custo. Em compensação, cada rebalanceamento é uma venda seguida de compras, e isso conta como ordem em cada ponta.

## Smart arbitrage: delta neutro, lucro na taxa de financiamento

O robô de arbitragem inteligente monta duas posições opostas do mesmo tamanho: compra o ativo no mercado à vista e vende a mesma quantidade no contrato perpétuo. Com isso, uma alta ou uma queda do preço afeta as duas pernas em direções contrárias, e o resultado líquido fica próximo de zero. O ganho vem da **taxa de financiamento** paga no mercado perpétuo, que se torna a fonte principal de retorno quando ela está positiva.

Há dois modos de operação. No **Custom mode**, você define a estratégia e o alvo de lucro. No **Smart mode**, o sistema escolhe a configuração e ajusta os parâmetros principais por conta própria. A OKX apresenta o produto como adequado a todos os níveis de experiência, mas a mecânica exige entender por que a taxa de financiamento existe e o que acontece quando ela vira negativa. Quem não sabe responder isso deve ficar nos grids e no DCA.

## Iceberg e TWAP: execução, não geração de sinal

Esses dois não tentam ganhar dinheiro com oscilação. Eles existem para reduzir o impacto da sua ordem no preço de mercado.

O **Iceberg** quebra uma compra ou venda grande em várias ordens menores para esconder o tamanho real e limitar o slippage. Funciona em **spot, perpétuo, futuro, margem e opções**. A tolerância de slippage pode ser definida por **Var.**, em unidades do ativo base do par, ou por **Ratio**, como percentual do preço da ordem.

O **TWAP** distribui a ordem ao longo de um período determinado, buscando um preço médio ponderado pelo tempo. Você escolhe comprar ou vender o primeiro ativo do par e define o slippage aceitável, seja em **Var.** com valor no segundo ativo, seja em **Ratio** como percentual do preço limite.

Se você nunca operou contrato perpétuo ou futuro, a própria OKX recomenda estudar o funcionamento desses produtos antes de usar ferramentas de execução nesses mercados.

## Signal trading e o marketplace

Além dos sete bots, a página de entrada da OKX cita **Signal trading**, onde é possível criar sinais próprios ou copiar estratégias de terceiros, e um **marketplace de robôs**. São caminhos diferentes dos bots nativos e não têm os mesmos parâmetros descritos acima. Trate como funcionalidade adicional a conferir dentro da plataforma, não como substituto do Spot grid.

## Como criar, parar e baixar o histórico

Criar: faça login, passe o mouse em **Trade** e selecione **Trading bots**. Na página, escolha a categoria (grid, DCA, arbitragem, fatiamento) e o par.

Parar: abra a aba **Bots** no painel de negociação, onde aparecem todos os robôs ativos e o resultado acumulado. Clique em **Stop** na operação correspondente, escolha entre manter o ativo ou converter a posição em **USDT**, confirme em **Confirm**. A operação sai da aba Bots e passa para o **History**.

Baixar histórico: no site, vá em **My Asset → Order center → Trading bots → Download**, selecione o tipo de operação e o período, clique em **Generate now**. O período personalizado pode recuar até **fevereiro de 2021**.

## O que mudou desde 2022 (e por que tutoriais antigos confundem)

A documentação de dezembro de 2022 listava **Futures grid, Price lock, Dip Sniper, Peak Sniper e Arbitrage**. A versão atualizada em outubro de 2026 não traz Futures grid, Price lock, Dip Sniper nem Peak Sniper, e o antigo "Arbitrage" aparece como **Smart arbitrage**, com mecânica de delta neutro e taxa de financiamento.

Se você seguir um tutorial que manda procurar "Dip Sniper" no menu, pode não encontrar nada. Antes de contar com qualquer uma dessas estratégias antigas, confirme dentro da plataforma se ela ainda está disponível na sua região. O Futures grid, quando existia, operava com contratos perpétuos e de vencimento, com modos Long, Short e Neutral e uso de alavancagem — a própria OKX já destacava o risco de liquidação nesse formato.

## Quanto custa de verdade

Não existe preço de assinatura para os robôs da OKX. A central de ajuda fala em "taxas de negociação baixas" e em uma reformulação da estrutura de tarifas que teria reduzido custos, sem publicar nenhum número na página dos bots. Também não há informação oficial, nessa documentação, sobre desconto específico para uso de robôs ou diferença por nível de conta.

Então o raciocínio que importa é este: cada ciclo completo de um grid envolve uma compra e uma venda, e as duas pagam taxa. Quanto mais apertada a grade, mais vezes o robô executa e mais taxa acumula. Uma grade desenhada com espaçamento menor do que o custo de ida e volta das ordens pode gerar dezenas de operações e terminar no zero ou no negativo. Antes de ligar um grid com muitos níveis, verifique a taxa aplicada à sua conta na tabela de tarifas da própria plataforma. 👉 [Ver os bots disponíveis na sua conta OKX](https://okx.com/join/CASH20)

## Quem não deveria usar robô na OKX

Quem espera retorno garantido: a OKX afirma explicitamente que os robôs são ferramentas de negociação, não recomendação de investimento, e que os retornos exibidos na tela são estimativas baseadas em backtest histórico, sem garantia de resultado real.

Quem não entende contrato perpétuo: Smart arbitrage e Iceberg em mercado de derivativos não são ponto de partida.

Quem só quer comprar e guardar por anos: o Recurring buy resolve, e nenhum grid vai superar isso em simplicidade.

Quem não tem caixa de reserva para o DCA Martingale: o robô foi desenhado para reforçar posição em quedas.

Quem opera valor alto em par com pouca liquidez: qualquer bot vai sofrer slippage ali, e Iceberg ou TWAP atenuam, mas não eliminam.

## Perguntas frequentes

**O robô de trading da OKX é gratuito?**
Não há mensalidade nem plano pago. O custo é a taxa de negociação de cada ordem executada.

**Preciso saber programar?**
Não. A OKX oferece parâmetros automáticos, guias escritos e vídeos. Você preenche faixa, valor e quantidade de grids.

**Qual o investimento mínimo?**
A documentação só é específica no Spot DCA, que exige reservar o Initial Order mais a First Safety Order na criação. Para grid e arbitragem, os valores mínimos não são divulgados na central de ajuda.

**Os robôs funcionam com o app?**
O acesso principal descrito pela OKX é pelo site, em Trade → Trading bots. Confira a disponibilidade das mesmas funções no aplicativo antes de montar uma estratégia pelo celular.

**Consigo encerrar e sacar quando quiser?**
Sim. O botão Stop fica na aba Bots, e você escolhe manter o ativo ou converter tudo em USDT.

**Posso usar mais de um robô ao mesmo tempo?**
A central de ajuda não impõe limite por conta. Cada robô fica identificado na aba Bots com o resultado acumulado.

## Como escolher o seu

Só quer acumular sem acompanhar preço: **Recurring buy**, com até 20 moedas.

Acredita que o preço vai oscilar dentro de uma faixa: **Spot grid**, começando com poucos níveis e usando a estratégia de IA para calibrar.

Já tem uma carteira montada e quer manter as proporções: **Smart portfolio**, no modo Proportional, que executa menos.

Quer comprar em quedas e tem capital para isso: **Spot DCA (Martingale)**, com o mínimo reservado e os ciclos contínuos ativados.

Entende taxa de financiamento e quer exposição delta neutra: **Smart arbitrage**, começando pelo Smart mode.

Precisa executar uma ordem grande sem mexer no preço: **Iceberg** ou **TWAP**, conforme o prazo que você tem.

Antes de ativar qualquer um, confirme três coisas na plataforma: a taxa que incide na sua conta, o valor mínimo aceito para o par escolhido e se a estratégia está disponível na sua região. A OKX não detalha esses três pontos na documentação dos bots, e eles mudam o resultado mais do que qualquer ajuste fino de parâmetro.

A conta nova já entra com acesso ao painel completo em Trade → Trading bots. 👉 [Começar com o bot que faz sentido para o seu caso](https://okx.com/join/CASH20)
