### Checkout Pagar.me

Esta opção, em relação as configurações, é bem parecida com o **Pagar.me - Cartão de crédito**. Entretanto, para capturar os dados de Cartão do cliente é usado o seguinte modal:

![Checkout Pagar.me](https://i.imgur.com/TpMs7mi.png)


### Instalação

1. Acesse [GitHub Pagar.me - Opencart](https://github.com/pagarme/pagarme-opencart)
 e faça o download do ZIP do módulo. Faça isso como mostra a imagem a seguir:


![Download do Módulo](https://i.imgur.com/tOX6YcB.png)

2. Em seguida, extraia o conteúdo do arquivo;

3. Acesse o seu painel administrativo OpenCart e clique em "Extensions Installer", como mostra a imagem abaixo: 


![Página de instalação do módulo](https://i.imgur.com/07x8EXn.png)


4. Ao fazer isso, a seguinte tela fica disponível. Nessa tela, clique em "Upload" encontre a pasta que você acabou de extrair, do módulo Pagar.me. 

Siga o caminho `Checkout Pagar.me > 2.3`

![Instalando um módulo no OpenCart](https://i.imgur.com/UETDVPy.png)

5. Dentro desta pasta você deve encontrar um arquivo chamado `pagar_me_checkout.ocmod.zip`, é ele que você precisa enviar para o OpenCart. Confirme o upload desse arquivo, e em seguida a seguinte tela é exibida:

![Módulo instalado com sucesso](https://i.imgur.com/d5WYIsj.png)

6. Para o próximo passo, é necessário ir até `Extensões > Modificações`, dentro do seu painel do OpenCart, como mostra a imagem a seguir:

![Painel de modificações](https://i.imgur.com/BXwYGLO.png)

7. Na tela ****Modificações****, clique em `Refresh`, o botão no canto superior direito, como é mostrado na imagem abaixo:

![Refresh](https://i.imgur.com/aBp8bxa.png)

Pronto! O seu módulo do OpenCart está instalado.

### Configuração

Para configurar o Checkout, siga o caminho pelo menu `Extensões > Métodos de pagamento`. Nessa lista, você deve encontrar a opção `Checkout - Pagar.me`.

[Instalando o checkout Pagar.me](https://i.imgur.com/y4c6WWS.png)

Ao encontrar essa opção, clique em `Install` e em seguida `Edit`, como é mostrado na imagem acima. Você poderá configurar o Checkout Pagar.me como bem entender.

![Configurando o Checkout Pagar.me](https://i.imgur.com/se0fWcl.png)

Confira tudo e, se estuver tudo certo, clique no botão `Save`, no canto superior direito. Ao finalizar uma compra com esse meio de pagamento, a seguinte tela irá aparecer:

![Finalização de compra com Checkout Pagar.me](https://i.imgur.com/JKnvvLH.png)

### Campos e significados

**Chave de API**:
Neste campo você coloca a sua API Key, que é uma chave utilizada para autenticar o seu negócio junto à API do Pagar.me.

**Chave de Criptografia**:
Neste campo você deve colocar a sua Encryption Key, que é uma chave essencial para realizar transações com Cartão de crédito usando a API Pagar.me.

**Texto informativo exibido na confirmação do pedido**:
Na página de finalização do pedido existe um espaço no qual você pode passar instruções para o comprador — por exemplo, um chamado para acompanhar o pedido.

**Nº máximo de parcelas**:
Este campo define em até quantas vezes será possível parcelar um pedido realizado no cartão de crédito.

**Taxa de juros do parcelamento (%)**:
O módulo Pagar.me oferece a conveniência de calcular (via juros simples) o valor das parcelas de acordo com um valor de juros passado neste campo. Configure este valor usando ponto, e não vírgula. Caso a sua aplicação não cobre juros, é preciso deixar o campo como 0.

**Nº de parcelas sem juros**:
Alinhado diretamente com o ponto de juros, esta opção define em até quantas parcelas aquele pedido não será cobrado juros. Exemplo: Digamos que o campo esteja configurado com 3, ou seja, caso o cliente opte por comprar em 1x, 2x ou 3x, seu pedido não será cobrado juros, mas caso escolha 4x, todas as parcelas terão juros aplicados.

**Valor mínimo da parcela**:
Caso queira, você pode definir um valor mínimo para as parcelas de compras feitas no seu site. O módulo mostra sempre o maior número até que o valor seja atingido. Por exemplo: Um produto A tem um valor de R$100,00, mas foi configurado no módulo que a parcela mínima seria R$70,00, então a única opção disponível é o pagamento à vista.

**Dias de vencimento do boleto**: 
Configure neste campo em até quantos dias o boleto gerado vai vencer. Isto é, quantos dias úteis o seu cliente tem para fazer o pagamento pela sua compra.

**Status Aguardando Pagamento**: 
Transações criadas com boleto tem um status inicial de `Waiting_Payment (Aguardando pagamento)` na API Pagar.me. Entretanto, no módulo você pode escolher qual será o status inicial do pedido dentro do OpenCart, enquanto o pagamento do boleto não é confirmado pelo banco. O status ideal a configurar nesse caso é `Pending`.

**Status Processando**: 
Para transações que ainda não estejam confirmadas junto ao banco emissor como `Pagas`, a API Pagar.me retorna um status intermediário chamado `Processing`. Logo, para que isso fique coerente é ideal que este campo esteja configurado também como `processing`. Entretanto, o módulo sempre espera um status concreto da API Pagar.me, ou seja, `Pago` ou `Recusado`. 

**Status Pago**: 
Para cartão de crédito, este status é referente a confirmação junto ao banco emissor de que a quantia será cobrada de fato na fatura do comprador. Para boleto bancário, este status significa que ele foi pago e conciliado. Logo, este campo deve estar configurado de acordo, em que os status possíveis são: ****Processed****, ****Processing**** ou ****Completed****. Entretanto, outros statuses podem ser usados, dependendo de seu modelo de negócio.

**Status Recusado**: 
Este status quer dizer que não foi possível realizar a cobrança no cartão inserido, já que ela foi recusada pelo banco emissor. Dos disponíveis, o status `Denied` é o mais coerente a ser usado.

**Status Reembolso**: 
Este status é referente a quando um pedido foi estornado. O valor mais coerente disponível é: `Refunded`.  


**Região geográfica**: 
Neste ponto é definido para quais possíveis compradores, dependendo do país em que a pessoa está acessando sua plataforma, a opção de Cartão de crédito do Pagar.me vai estar habilitada. O padrão é definido como `All Zones` e você precisa alterar isso apenas se quiser limitar essa abrangência.

**Situação**: 
Define se essa opção estará habilitada está habilitada ou não no seu site. O valor padrão é `Enabled`, ou seja, habilitado.

**Ordenação**: 
Define a ordem na qual a opção de Cartão de crédito aparece na lista de meios de pagamento em sua página de finalização de pedido. Valor padrão: 2.
