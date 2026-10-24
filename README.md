# EatWise · Protótipo navegável

Protótipo de front-end do **EatWise**, projeto do grupo **Seven** (TCC): um aplicativo que controla a
"segunda validade" dos alimentos, ou seja, até quando um produto pode ser consumido com segurança
depois que a embalagem é aberta.

> Tudo é simulado no navegador: não há backend, banco de dados, IA real nem envio de dados.
> Os produtos, alertas e números são fictícios.

## Como abrir

Abra o arquivo `index.html` em qualquer navegador (duplo clique). Não precisa instalar nada.

## App para celular

A pasta `app/` tem a versão para celular do EatWise: as mesmas telas, dados e visual do protótipo web, com cara de aplicativo.

- Tela de abertura e apresentação inicial em 3 telas (dá para deslizar com o dedo)
- Barra de navegação inferior com o botão **+** para registrar produtos
- Registro por foto com tela de câmera (visor, botão de disparo, galeria e flash simulados)
- Instalável na tela inicial (PWA): abre em tela cheia, com ícone próprio, e funciona sem internet depois do primeiro acesso

No computador, o app aparece dentro de uma moldura de celular, ideal para apresentar.

### Como instalar no celular

O app precisa estar publicado em um endereço `https`. O jeito mais simples é o GitHub Pages:

1. No GitHub, abra **Settings → Pages**.
2. Em **Branch**, escolha a branch deste projeto e a pasta `/ (root)`, e clique em **Save**.
3. Depois de alguns minutos, o app fica em `https://<usuário>.github.io/PrototipoTCC/app/`.
4. Abra esse endereço no celular:
   - **Android (Chrome):** menu ⋮ → **Instalar app** ou **Adicionar à tela inicial**.
   - **iPhone (Safari):** botão Compartilhar → **Adicionar à Tela de Início**.

Para gerar um arquivo **APK** (Android), cole o endereço do GitHub Pages em [pwabuilder.com](https://www.pwabuilder.com) e baixe o pacote Android.

### Manter as duas versões iguais

O `app/index.html` é gerado a partir do `index.html`. Depois de alterar o protótipo web, rode:

```
python3 tools/build_app.py
```

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
