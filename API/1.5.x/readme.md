### Instalação

1. Acesse [GitHub Pagar.me - Opencart](https://github.com/pagarme/pagarme-opencart)
 e faça o download do ZIP do módulo. Faça isso como mostra a imagem a seguir:

[Download do Módulo](https://i.imgur.com/tOX6YcB.png)

2. Em seguida, extraia o conteúdo do arquivo;
3. Na pasta criada pelo arquivo extraído, siga o caminho `API > 1.5.x `. Lá, você deve encontrar uma pasta chamada `upload`;
4. Copie todo o conteúdo da pasta `upload` para a pasta raiz da instalação de seu OpenCart, que geralmente é algo como: `www/html`;
5. Por fim, volte ao Painel da sua loja e siga o caminho `Extensões > Formas de pagamento`, como é mostrado na imagem abaixo. Ao encontrar os módulos Pagar.Me, você está pronto para fazer as configurações e começar a transacionar.

[Página de Configuração do Módulo](https://i.imgur.com/Z5g3fYK.png)

### Configuração

O primeiro passo é procurar os métodos de pagamento do **Pagar.me** e clicar em *Install* em quais desejar habilitar, como na imagem abaixo.

[Meios de pagamento](https://i.imgur.com/vuxT7fB.png)

## Boleto

Após instalar o módulo, clique no botão *Edit*, referente a forma de pagamento de Boleto bancário, como é mostrado na imagem a seguir: 

[Boleto](https://i.imgur.com/lNipdAH.png)

Pronto, a tela de configurações foi aberta. Na explicação abaixo, veja o que cada campo significa e como você pode configurá-los para atender melhor a realidade do seu negócio.

[Configuração de boleto](https://i.imgur.com/h6X64kK.png)

## Cartão de crédito

Após instalar o módulo, clique no botão *Edit*, referente a forma de pagamento de cartão de crédito, como é mostrado na imagem a seguir: 

[Cartão de crédito](https://i.imgur.com/fXtrFwp.png)

Pronto, a tela de configurações foi aberta. Na explicação abaixo, veja o que cada campo significa e como você pode configurá-los para atender melhor a realidade do seu negócio.

[Configuração de cartão de crédito](https://i.imgur.com/fXtrFwp.png)


### Campos e significados

`Chave de API`:
Neste campo você coloca a sua API Key, que é uma chave utilizada para autenticar o seu negócio junto à API do Pagar.me.

`Chave de Criptografia`:
Neste campo você deve colocar a sua Encryption Key, que é uma chave essencial para realizar transações com Cartão de crédito usando a API Pagar.me.

`Texto informativo exibido na confirmação do pedido`:
Na página de finalização do pedido existe um espaço no qual você pode passar instruções para o comprador — por exemplo, um chamado para acompanhar o pedido.

`Nº máximo de parcelas`:
Este campo define em até quantas vezes será possível parcelar um pedido realizado no cartão de crédito.

`Taxa de juros do parcelamento (%)`:
O módulo Pagar.me oferece a conveniência de calcular (via juros simples) o valor das parcelas de acordo com um valor de juros passado neste campo. Configure este valor usando ponto, e não vírgula. Caso a sua aplicação não cobre juros, é preciso deixar o campo como 0.

`Nº de parcelas sem juros`:
Alinhado diretamente com o ponto de juros, esta opção define em até quantas parcelas aquele pedido não será cobrado juros. Exemplo: Digamos que o campo esteja configurado com 3, ou seja, caso o cliente opte por comprar em 1x, 2x ou 3x, seu pedido não será cobrado juros, mas caso escolha 4x, todas as parcelas terão juros aplicados.

`Valor mínimo da parcela`:
Caso queira, você pode definir um valor mínimo para as parcelas de compras feitas no seu site. O módulo mostra sempre o maior número até que o valor seja atingido. Por exemplo: Um produto A tem um valor de R$100,00, mas foi configurado no módulo que a parcela mínima seria R$70,00, então a única opção disponível é o pagamento à vista.

`Dias de vencimento do boleto`: 
Configure neste campo em até quantos dias o boleto gerado vai vencer. Isto é, quantos dias úteis o seu cliente tem para fazer o pagamento pela sua compra.

`Status Aguardando Pagamento`: 
Transações criadas com boleto tem um status inicial de `Waiting_Payment (Aguardando pagamento)` na API Pagar.me. Entretanto, no módulo você pode escolher qual será o status inicial do pedido dentro do OpenCart, enquanto o pagamento do boleto não é confirmado pelo banco. O status ideal a configurar nesse caso é `Pending`.

`Status Processando`: 
Para transações que ainda não estejam confirmadas junto ao banco emissor como `Pagas`, a API Pagar.me retorna um status intermediário chamado `Processing`. Logo, para que isso fique coerente é ideal que este campo esteja configurado também como `processing`. Entretanto, o módulo sempre espera um status concreto da API Pagar.me, ou seja, `Pago` ou `Recusado`. 

`Status Pago`: 
Para cartão de crédito, este status é referente a confirmação junto ao banco emissor de que a quantia será cobrada de fato na fatura do comprador. Para boleto bancário, este status significa que ele foi pago e conciliado. Logo, este campo deve estar configurado de acordo, em que os status possíveis são: **Processed**, **Processing** ou **Completed**. Entretanto, outros statuses podem ser usados, dependendo de seu modelo de negócio.

`Status Recusado`: 
Este status quer dizer que não foi possível realizar a cobrança no cartão inserido, já que ela foi recusada pelo banco emissor. Dos disponíveis, o status `Denied` é o mais coerente a ser usado.

`Status Reembolso`: 
Este status é referente a quando um pedido foi estornado. O valor mais coerente disponível é: `Refunded`.  


`Região geográfica`: 
Neste ponto é definido para quais possíveis compradores, dependendo do país em que a pessoa está acessando sua plataforma, a opção de Cartão de crédito do Pagar.me vai estar habilitada. O padrão é definido como `All Zones` e você precisa alterar isso apenas se quiser limitar essa abrangência.

`Situação`: 
Define se essa opção estará habilitada está habilitada ou não no seu site. O valor padrão é `Enabled`, ou seja, habilitado.

`Ordenação`: 
Define a ordem na qual a opção de Cartão de crédito aparece na lista de meios de pagamento em sua página de finalização de pedido. Valor padrão: 2.