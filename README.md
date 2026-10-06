# EatWise · Protótipo navegável

Protótipo de front-end do **EatWise**, projeto do grupo **Seven** (TCC): um aplicativo que controla a
"segunda validade" dos alimentos, ou seja, até quando um produto pode ser consumido com segurança
depois que a embalagem é aberta.

> Tudo é simulado no navegador: não há backend, banco de dados, IA real nem envio de dados.
> Os produtos, alertas e números são fictícios.

## Como abrir

Abra o arquivo `index.html` em qualquer navegador (duplo clique). Não precisa instalar nada.

## Telas

| Tela | O que mostra |
|---|---|
| Início (landing) | Proposta de valor, a "segunda validade", fluxo em 5 etapas, benefícios e planos (Gratuito / Premium R$ 19,90) |
| Login e Cadastro | Entrada simulada; o cadastro exibe "Cadastro realizado com sucesso" |
| Dashboard | Resumo da geladeira, itens para consumir primeiro, últimos registros, dica de conservação |
| Registrar produto | Funcionalidade principal: cadastro por **foto, texto ou áudio**, "IA" identificando o item, consulta à base de prazos e cálculo da data-limite |
| Minha geladeira | Listagem com abas (abertos/histórico), filtros por status e categoria, busca e ordenação |
| Detalhe do produto | Dias restantes, linha do tempo (aberto → alerta → data-limite), como o prazo foi calculado, ações consumir/descartar/editar/excluir |
| Alertas | Notificações agrupadas por período, lidas/não lidas |
| Base de prazos | Tabela de prazos pós-abertura por categoria (referência: ANVISA, Guia nº 16) |
| Meu impacto | Consumidos × descartados por mês, economia, meta do piloto (30% de redução com 20 usuários) |
| Perfil e configurações | Dados, preferências de notificação, casa compartilhada e plano |

## Fluxo sugerido para apresentação

Início → Entrar → Dashboard → Registrar produto (Foto) → Salvar → Detalhe do produto → Minha geladeira → Alertas → Meu impacto.
