## Checkout Pagar.me ##

Siga as instruções abaixo, e após isso, selecione a versão de seu OpenCart para prosseguir com a instalação.

| Versão |
| ------ |
| [1.5.x](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/1.5.x) |
| [2.0 ~ 2.2](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/2.3) |
| [2.3](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/2.x) |


### Configure seu OpenCart para que o módulo funcione corretamente:

## 1.5.x

Habilite o CPF em seu OpenCart, para fazer isso, siga esse passo-a-passo:

1. Clique em `Sales` > `Customer Groups` e clique em editar no grupo de clientes

![Customer Groups](https://i.imgur.com/77SVtzo.png)

2. Habilite a opção `Display Tax ID` e torne-a obrigatória através do campo `Tax ID Required`

![Tax ID](https://i.imgur.com/r9dWemS.png)

## 2.x

## Campos Personalizados

Acesse seu painel administrador, selecione a opção `Customer > Custom Fields`, e clique para adicionar um novo campo customizável.

![Custom Fields](https://i.imgur.com/Enz7Vdf.png)

Os campos que podem ser criados para que a integração entenda são `CPF`, `CNPJ`, `Número` e `Complemento`.

Crie o campo de CPF caso venda para pessoas físicas e o de CNPJ caso venda para pessoas jurídicas.

# CPF

| *Campo do OpenCart* | *Valor Recomendado*                         | *Obrigatoriedade* |
|---------------------|---------------------------------------------|-------------------|
| Custom Field Name   | CPF                                         | Obrigatório       |
| Location            | Account                                     | Obrigatório       |
| Type                | Text                                        | Obrigatório       |
| Customer Group      | Habilite os grupos que possuirão esse campo | Obrigatório       |
| Required            | Habilitado                                  | Obrigatório       |
| Status              | Habilitado                                  | Obrigatório       |
| Sort Order          | 3                                           | Opcional          |


# CNPJ

| *Campo do OpenCart* | *Valor Recomendado*                         | *Obrigatoriedade* |
|---------------------|---------------------------------------------|-------------------|
| Custom Field Name   | CNPJ                                        | Obrigatório       |
| Location            | Account                                     | Obrigatório       |
| Type                | Text                                        | Obrigatório       |
| Customer Group      | Habilite os grupos que possuirão esse campo | Obrigatório       |
| Required            | Habilitado                                  | Obrigatório       |
| Status              | Habilitado                                  | Obrigatório       |
| Sort Order          | 3                                           | Opcional          |

# Número 

| *Campo do OpenCart* | *Valor Recomendado*                         | *Obrigatoriedade* |
|---------------------|---------------------------------------------|-------------------|
| Custom Field Name   | Número                                      | Obrigatório       |
| Location            | Address                                     | Obrigatório       |
| Type                | Text                                        | Obrigatório       |
| Customer Group      | Habilite os grupos que possuirão esse campo | Obrigatório       |
| Required            | Opcional                                    | Opcional          |
| Status              | Opcional                                    | Opcional          |
| Sort Order          | 2                                           | Opcional          |

# Complemento

| *Campo do OpenCart* | *Valor Recomendado*                         | *Obrigatoriedade* |
|---------------------|---------------------------------------------|-------------------|
| Custom Field Name   | Complemento                                 | Obrigatório       |
| Location            | Address                                     | Obrigatório       |
| Type                | Text                                        | Obrigatório       |
| Customer Group      | Habilite os grupos que possuirão esse campo | Obrigatório       |
| Required            | Opcional                                    | Opcional          |
| Status              | Opcional                                    | Opcional          |
| Sort Order          | 3                                           | Opcional          |


Escolha a versão de seu OpenCart para prosseguir com a instalação.

| Versão |
| ------ |
| [1.5.x](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/1.5.x) |
| [2.0 ~ 2.2](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/2.3) |
| [2.3](https://github.com/pagarme/pagarme-opencart/tree/update/readme/Checkout%20Pagar.Me/2.x) |
