---
title: Perguntas frequêntes

search: true
---

# Perguntas frequentes

## Dúvidas técnicas

### Aonde eu cadastro meus produtos?

A inclusão dos produtos é feita dentro do Backoffice, no menu de Produtos/Cadastrar Produto.

### Existe limite de produtos a serem cadastrados no CHECKOUT CIELO?

Não, você pode cadastrar quantos produtos desejar.

### É necessario cadastrar todos os meus produtos no CHECKOUT CIELO para que eu possa transacionar?

Não, o cadastro de produtos é opcional. Ele é realizado para a criação de um “botão”, que pode ser utilizado para a venda de um produto especifico.

### Quais informações eu preciso para montar o Post?

Os dados a serem preenchidos no post se referem basicamente a 4 grupos:

1. Dados do Pedido
2. Carrinho de Compras
3. Dados de Frete
4. Dados do Consumidor.

Todas as informações para auxiliar nesse processo, encontram-se no manual de desenvolvimento.

### Posso enviar um e-mail como forma de cobrança?

Sim, através da integração via botão você pode usar para enviar um e-mail marketing, ou uma cobrança por e-mail, adicionando ao HTML do e-mail, o botão referente ao produto/serviço sendo comprado/pago. Ou sempre que se desejar disponibilizar uma transação rápida sem desenvolvimento algum.

### O comprador precisa ser cliente do CHECKOUT CIELO para fechar a transação?

Não. A solução de checkout é simples e não exige que o cliente esteja logado ou se cadastre. No entanto todas as informações solicitadas para fechar a compra são salvas no pedido. E o lojista terá acesso a todas elas.

### Para que serve a URL de retorno?

Para que ao finalizar a compra, o consumidor final tenha a opção de voltar ao site do lojista. O Consumidor é redirecionado automaticamente a pagina definida nesta opção.

### Para que serve a URL de Notificação?

Ao finalizar a compra é enviando um post contendo informações sobre a transação. A utilização dessa URL é indicada para clientes que entregam através de uma Plataforma de E-commerce. Dessa maneira os dados do pedido ficam atualizados no Backoffice do CHECKOUT CIELO e no Backoffice junto a Plataforma.

### Para que serve a URL de Notificação?

Ao finalizar a compra é enviando um post contendo informações sobre a transação. A utilização dessa URL é indicada para clientes que entregam através de uma Plataforma de E-commerce. Dessa maneira os dados do pedido ficam atualizados no Backoffice do CHECKOUT CIELO e no Backoffice junto a Plataforma.

### Onde é feito o cadastro dessas URLs?

No seu backoffice, aba configurações -> configurações da loja.

### Posso dar desconto ao meu cliente?

Sim. É possível enviar um parâmetro com o valor ou a Porcentagem (%) do desconto a ser oferecido naquela transação. Esse parametro é valido para todos os meios de pagamento, não sendo aplicado a meios especificos e o desconto é sobre o valor total da transação.

Tambem é possivel definir um valor de desconto para pagamento com Debito online ou boleto, ambos podendo ser enviados via Post ou definidos no Backoffice. O desconto de boleto/débito pode ser acumulado ao desconto total.

### Como são os Posts para lojas que utilizam carrinhos?

O tipo de post a ser utilizado em sua loja dependerá do produto e de como esse é comercializado na sua loja.

Os Posts serão formados por parametros que devem ser enviados a URL, `https://cieloecommmerce.cielo.com.br/transactional/order/index`, onde serão processados. Veja a seção [Integração](#integraco) dessa documentação para mais informações.

<aside class="notice">É importante entender que apesar de alguns parametros descritos no manual de integração não serem obrigatorios para um determinado produto, isso não significa que eles não serão obrigatorios a outros tipos.</aside>

### Qual a relação entre os tipos de produtos e os tipos de fretes?

O tipo de produto a ser vendido no CHECKOUT CIELO influencia diretamente qual o tipo de frete e a informação a ser enviada para o processamento da transação. O tipo de frete a ser utilizado dependerá do tipo de produto que a sua loja comercializa. No CHECKOUT CIELO você pode comercializar 3 tipos de produtos:

* Bens Fisicos
* Bens digitais
* Serviços

Os tipos de frete que podem ser usados são:

* Correios
* Frete Fixo
* Frete Grátis
* Sem Frete (Retirada em mãos)
* Sem cobrança de frete (Usada para bens Digitais ou Serviços)

Se Produtos do tipo “Bens fisicos” necessitam de algum tipo de frete para serem enviados, obrigatoriamente será preciso a inclusão de informações como do peso do produto, Cep de origem e Cep de entrega, para o calculo do frete. Veja a seção [Integração](#integraco) dessa documentação para mais informações.

<aside class="notice">Diferentemente, “Bens digitais” ou “Serviços” não necessitam desse tipo de informação.</aside>

## Dúvidas comerciais

### Quais são os meios de pagamento disponíveis no CHECKOUT CIELO?

Cartões de Crédito (Bandeiras: Visa, Mastercard, Diners, Amex e Elo), Boleto Bancário
e Débito Online (Banco do Brasil e Bradesco).

### Quais são as diferenças entre o CHECKOUT CIELO e os Facilitadores de Pagamento, como Pagseguro e Paypal?

* Não intermediamos o dinheiro referente a suas transações. Isso significa que o lojista vende com suas afiliações. Seu dinheiro será depositado diretamente na sua conta corrente pela Cielo.
* Controle sobre os recebimentos. O lojista negocia diretamente com Cielo se deseja antecipar seus recebíveis
* Possibilidade de capturar transações imediatamente. O lojista decide se captura manualmente ou libera a captura automatica para transações de baixo risco.
* O lojista decide para quem quer vender com apoio de ferramenta antifraude. O Lojista decide se assume o risco informado (“Baixo, Moderado ou Alto”) em relação a um pedido, capturando ou cancelando a transação (conclui a transação ou não).

### É preciso ter contas nos bancos para adquirir as afiliações de boleto e Débito?

Sim. Para maiores informações sobre esse processo entre em contato com [cieloecommerce@cielo.com.br](mailto:cieloecommerce@cielo.com.br).

O CHECKOUT CIELO não gera boletos para cooperativas de crédito, mesmo que estas sejam vinculadas aos bancos utilizados.

### Quando o valor da transações é depositado em minha conta corrente?

O valor transacionado será depositado em sua conta corrente de acordo com os prazos estabelecidos em cada meio de pagamento. Para maiores informações sugerimos que entre em contato direto com cada meio que a sua loja utiliza.

### É possivel realizar parcelamentos no CHECKOUT CIELO?

Sim, o CHECKOUT CIELO pode parcelar compras com cartão de crédito em até 12x. As parcelas do CHECKOUT CIELO não incluem juros, sendo uma divisão do valor comprado pelo prazo do pagamento.

<aside class="notice">O numero maximo de parcelas é definido na afiliação da loja. Caso a sua afiliação tenha liberado 6x na afiliação e 12X no CHECKOUT CIELO, a transação não será autorizada. A alteração do numero maximo de parcelas da afiliação pode ser realizada diretamente com a Cielo.</aside>

### Saio do ambiente da minha loja durante a transação?

Sim, quando o comprador decidir realizar o checkout ele será redirecionado para a tela do CHECKOUT CIELO. Nessa tela segura, o comprador irá inserir os dados do meio de pagamento e o meio de entrega/frete (caso a loja permita) de sua preferencia.

### O CHECKOUT CIELO detém informações sobre prazo de entrega do produto?

Não , o CHECKOUT CIELO tem acesso somente a informações da transação de pagamento. Caso um cliente do lojista CHECKOUT CIELO entre em contato com duvidas a respeito do prazo de entrega ou solicitações a respeito do mesmo assunto, será sugerido a ele que entre em contato com a loja responsavel pela venda.

A equipe CHECKOUT CIELO não fornece os dados de contato do Lojista ao comprador em hipótese alguma.

## Dúvidas operacionais

### Quando esquecer a senha de acesso ao Backoffice, como proceder?

1. Acesse o site do backoffice, e clique em “Esqueci Minha Senha”
2. Preencha com o e-mail cadastrado. Um e-mail para redefinição de senha será enviado.

### Não consigo visualizar o pedido no backoffice, como resolver?

Primeiramente, verifique se na integração foi utilizado o MID correto. MID é o Merchant_Id de sua loja, e deve ser utilizado na integração com CHECKOUT CIELO, coforme o Manual de Desenvolvimento.

### O que devo fazer quando o pedido estiver com o status “Autorizado”?

Deverá conferir o status do antifraude e decidir por capturar (aceitar) ou cancelar a transação. Ressaltamos que o risco e a responsabilidade sempre serão do lojista caso venha a sofrer uma fraude e/ou um chargeback.

### Durante quanto tempo o pedido pode permanecer com o status “Autorizado”?

O pedido poderá ficar “Autorizado” por 5 dias corridos, após esse prazo não pode mais ser capturado junto a operadora de cartão de crédito/adquirente (Cielo). Recomendamos que Capture ou Cancele o pedido o quanto antes, agilizando a entrega da mercadoria ou liberando o limite de crédito do seu cliente.

### Qual é a diferença entre os status “Autorizado” e “Pago” em um pedido de cartão de
crédito?

* **Autorizado** – o valor da transação fica reservado no limite do cartão do cliente, aguardando a captura (efetivação do pagamento) ou o cancelamento ( o retorno do limite ao cliente). Significa que a transação ainda NÃO foi concluída.
* **Pago** – o valor foi efetivado e será cobrado na fatura do cliente. Significa que a transação foi concluída 

<aside class="warning">ATENÇÃO, para pedidos feitos com cartão de crédito o status “Pago” não significa que o dinheiro estará disponível na sua conta corrente imediatamente. A operadora de cartão de crédito (Cielo) efetiva o depósito dos valores referente à suas transações 30 dias após a captura. É possível receber antes dos 30 dias negociando diretamente com a Cielo ou com o seu banco a (Antecipação de recebíveis de cartão de crédito).</aside>

### O que devo fazer quando o pedido estiver com o status “Expirado”?

* Para pedidos com Cartão de Crédito, não será possível capturar a transação. O pedido foi automaticamente cancelado pela operadora de cartão de crédito/adquirente (Cielo).
* Para pedidos com Boleto Bancário, é necessário consultar no seu extrato bancário se valor foi creditado e alterar o status para PAGO.

### O que acontece se eu não alterar os status dos meus boletos que foram pagos?

Não haverá nenhum impacto em suas vendas, porém a visão da sua operação nos relatórios e gráficos do Dashboard ficará prejudicada por não refletir exatamente o status de sua operação.

### O que significa o status “Pendente” para cartões de crédito?

Significa que não foi repassada até o momento nenhuma resposta do Banco ou da Cielo.
Os pedidos serão sondados juntos as operadoras de cartão de crédito/Adquirentes, e seu status atualizado.

### Quais os possíveis status em cada meio de pagamento?

* **Cartão de Crédito**:
   * **Não Finalizado** - Falha de conexão no processamento da transação é possível recuperar a transação solicitando que o cliente refaça a transação.
   * **Pendente** - Status intermediário.
   * **Autorizado** - Quando um pedido foi aprovado e está pendente de captura. É necessário Capturar ou Cancelar a transação conforme a analise de risco.
   * **Não Autorizado** - pedido não foi aprovado pela Cielo/Banco Emissor Pago - status após a Captura manual ou automática da transação.
   * **Cancelado** - Quando é solicitado um cancelamento junto a operadora de cartão de crédito/adquirente.
   * **Chargeback** - Quando o comprador solicita o estorno junto ao banco emissor, o lojista pode utilizar esse status para seu controle.
   * **Expirado** - Não foi Capturado ou cancelado no prazo de 5 dias.
* **Boleto Bancário**:
   * **Pendente** - Aguardando pagamento
   * **Não Finalizado** - Falha de conexão no processamento da transação é possível recuperar a transação solicitando que o cliente refaça a transação.
   * **Expirado** - Não foi alterado o status no prazo de 5 dias após a data de vencimento, se o pagamento for confirmado no seu extrato bancário é possível alterar o status da transação para PAGO.
   * **Pago** - Confirmação de Pagamento após verificação no seu extrato bancário
* **Débito Online**:
   *  **Não Autorizado** - pedido não aprovado pelo banco.
   *  **Pago** - Pedido confirmado pelo banco, valor debitado da conta do comprador.
   *  **Não Finalizado** - Falha de conexão no processamento da transação. É necessário solicitar ao cliente que refaça a transação.
   *  **Pendente** - Status intermediário.

### Cliquei errado no botão “Cancelar”. Perdi a transação?

Sim, a transação foi cancelada junto a Cielo. Não sendo possível desfazer um cancelamento.

### Qual a diferença de Cancelamento e Estorno?

* **Cancelamento** - é feito no mesmo dia da captura, devolvendo o limite ao cartão do comprador em até 72h conforme regras do banco emissor do cartão.
* **Estorno** - a partir do dia seguinte da captura, o valor é “devolvido” na fatura do comprador em até 120 dias.

<aside class="warning">ATENÇÃO, o cancelamento e o estorno são realizamos através do “botão” cancelar. Seguindo as regras acima.</aside>

### Quanto tempo depois da transação eu posso efetuar um estorno?

Você tem até 120 dias após a data de captura do pedido.

### É possivel definir um valor minimo de parcelamento?

Sim, na aba configurações do CHECKOUT CIELO é possivel definir o valor minimo que uma parcela pode atingir. Dessa maneira, o valor da parcela não será inferior a um valor idal ao lojista.

### É possivel definir um valor minimo de boleto?

Sim, é possivel definir um valor minimo para que o boleto seja disponibilizado. Para maiores informações acesse BackOffice -> Manuais -> Tutorial do lojista.

### É possivel dar um desconto para o uso de boleto ou meio de pagamento?

Sim, é possivel definir um valor de desconto para que o boleto seja disponibilizado. Isso pode ser feito de duas maneiras: Backoffice ou via API de integração - descrita na seção [Integração](integraco).

### O que é antifraude? E para que serve?

“Anti-Fraudes” são ferramentas de Análise e Avaliação de Risco. Essas ferramentas verificam e apontam a possibilidade de uma transação incorrer em fraude, protegendo o empreendedor virtual de eventuais golpes.

Ao vender pela internet não existe a possibilidade de utilizar a segurança dos dispositivos físicos do cartão tais como o chip e a tarja magnética e por isso os lojistas virtuais são alvos constantes de tentativas de fraude.

Diante desse cenário, surgiram no mercado ferramentas específicas que buscam combater e inibir tais iniciativas, ou seja, os “anti-fraudes”.

Todas as transações de cartão de crédito autorizadas na Cielo no CHECKOUT CIELO são
processadas no antifraude Decision Manager da Cybersource.

### Para capturar minhas transações, necessito entrar no Backoffice

Depende. Caso deseje visualizar o status de cada transação e acompanhar pessoalmente o processo de venda, você pode mantar a captura manual.

Caso, prefira que o processo de captura seja automatizado, há na aba configurações opções de captura e rejeição de pedidos automaticamente.

### Qual a diferença de Captuta Automática e Captura Manual?

* **Captura Automática** – a decisão da venda é feita automaticamente após analise de fraude. Onde todos os pedidos autorizados e com “Baixo Risco” serão marcados como PAGO.
* **Captura Manual** – a decisão de venda é feita manualmente pelo lojista no backoffice. Analisando a resposta do antifraude.

### O que devo fazer quando o status do antifraude estiver como “Baixo Risco” e a minha captura é manual?

Recomendamos que capture o pedido e conclua a transação. Lembrando que não existe risco zero em transações online pois os mecanismos de segurança, tais como tarja magnética, chip e senhas não funcionam para transações online.

### O que devo fazer quando o status do antifraude estiver como “Alto Risco” e a minha captura é manual?

Neste caso recomendamos o cancelamento da autorização, porém você ainda pode optar por fazer uma análise manual do pedido e decidir por capturar a autorização e concluir a transação ignorando a orientação do antifraude e assumindo o risco.

### O que é um Chargeback?

Chargeback é o cancelamento feito pelo comprador de uma transação realizada com cartão de crédito. Que pode acontecer por dois motivos:

1. O não reconhecimento da compra por parte do titular do cartão
2. Ou a transação não obedecer às regras previstas entre o comprador e o lojista.

Caso um ChargeBack ocorra, o lojista não recebe o valor da compra ou seja, caso seja uma fraude, o fraudador, pode realizar uma compra com dados falsos.

### Quais a opções de frete eu posso utilizar?

* Correios
* Frete Fixo
* Frete Grátis
* Sem Frete (Retirada em mãos)
* Sem cobrança de frete (Usada para bens Digitais ou Serviços)

### Para utilizar o frete dos Correios o que eu devo fazer?

* Se você tem um contrato com o correio basta cadastrar seu usuário e senha no menu Configurações -> Configurações de loja do seu Backoffice.
* Se não tiver contrato, será necessario inserir CEP de origem, o CEP de destino e o peso do produto, calculando o frete do produto a ser enviado.

### Como o comprador final escolhe o frete?

O frete é escolhido na tela de finalização de compra, onde serão exibidas as opções cadastradas pelo vendedor.

<aside class="notice">OBS: O lojista tambem tem a opção de calcular o valor do frete dentro de sua loja.</aside>

### Como o valor do frete é repassado ao lojista?

O frete é incluso no valor da transação (valor do pedido + frete = Valor da transação).