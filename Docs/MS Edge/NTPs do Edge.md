# Os NTPs do Microsoft Edge
Todo navegador deve ter pelo menos uma página inicial para começar a sua navegação.
Muitos navegadores tem NTPs e cada um é diferente.

Vamos por partes.

## O que é?
Um **NTP (New Tab Page)** é a página exibida quando você abre uma nova guia no navegador.  
Ela serve para o usuário facilmente pesquisar algo só abrindo uma nova aba.

## Tipos

No Microsoft Edge, existem pelo menos **dois tipos de NTP**: o **servidor** e o **local**.

## Explicação de cada um
 
### Servidor (ntp.msn.com)
O NTP ntp.msn.com é o padrão para servidor remoto de quando você abre a nova guia. Possivelmente, se o ntp.msn.com não estiver acessível, ele abre o local (veja lá em baixo).

A URL exata para a nova guia é https://ntp.msn.com/edge/ntp e ela aceita diversos **parâmetros opcionais** na URL. Veja a tabela:

| Parâmetro     | Valor        | Descrição                                                                 | Valor de exemplo                                                        |
|---------------|--------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| locale        | ab-CD        | Define idioma e região, seguindo a especificação IETF BCP 47              | `?localept-BR`                                                          |
| title         | texto        | Define o título da página exibido na aba                                  | `?title=Nova%20guias` → título será "Nova guias"                        |
| dsp           | 1            | Possivelmente "Display Search Provider"; significado não documentado      | `?dsp=1`                                                                |
| sp            | Bing         | Provavelmente define o provedor de busca                                  | `?sp=Bing`                                                              |
| feed_dis      | on / off     | Ativa ou desativa o feed de notícias                                      | `?feed_dis=off`                                                         |
| en_widget_reg | true / false | Relacionado a widgets                                                     | `?en_widget_reg=false`                                                  |
| PC            | XNNNN        | Identificador alfanumérico (X = letra, N = número)                        | `?PC=A1234`                                                             |
| adppc         | EDGEESS      | Possível identificador de campanha/publicidade                            | `?adppc=EDGEESS`                                                        |

Exemplo de URL: https://ntp.msn.com/edge/ntp?locale=pt-BR&title=Minha%20novinha%20guia&dsp=1&sp=Bing&feed_dis=off&en_widget_reg=false&PC=J1682&adppc=EDGEESS

Você também pode acessar sem parâmetros:  
- https://ntp.msn.com/edge/ntp | Se quiser, o link está aqui: [link](https://ntp.msn.com/edge/ntp)

### Local

Provavelmente todos navegadores baseados em Chromium possuem uma versão local do NTP, usada provavelmente como **fallback** quando o servidor não está disponível ou quando o usuário está offline:

- `chrome-search://local-ntp/local-ntp.html`

Não sei se há parâmetros que você possa usar.



Fim da documentação.


