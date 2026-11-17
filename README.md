# Saldo Positivo

Dashboard de saldos que lê uma Google Sheet e se atualiza a cada minuto, com o visual do iOS 27 (Liquid Glass).

## Funcionalidades
- **Total disponível** em cartão de vidro, com estado (Saudável / Atenção / Baixo) e barras de evolução diária dos últimos 14 dias (verde se subiu, vermelho se desceu).
- **Contas** numa lista agrupada: inicial colorida, estado, percentagem do total, valor e barras diárias.
- **Distribuição** do total por conta.
- **Saldos escondidos por omissão**: olho em cada conta e no total, e um olho no topo para mostrar ou esconder todos. Ao recarregar a página volta tudo a ficar escondido.
- **Tema** automático, claro ou escuro.
- **Barra de separadores** (Total, Contas, Distribuição) e pesquisa de contas pelo nome.
- **Instalável no ecrã principal** do iPhone/Android (ícone e manifest incluídos).

## Folha de cálculo
A primeira linha é o cabeçalho. Colunas reconhecidas pelo nome:

| Coluna | Obrigatória | Exemplo |
| --- | --- | --- |
| Conta | sim | Conta Principal |
| Saldo | sim | 2.430,15 € |
| Aviso | não | 1.000 € — estado "Atenção" abaixo deste valor (por omissão 500 €) |
| Perigo | não | 300 € — estado "Baixo" abaixo deste valor (por omissão 100 €) |

Linhas chamadas "Total" são ignoradas; o total é calculado pela página.

## Histórico
A evolução diária é guardada no próprio navegador (um registo por dia, até 90 dias). Cada dispositivo tem o seu histórico.

## Ficheiros
- `index.html` — a página completa (HTML, CSS e JavaScript)
- `favicon.svg`, `favicon-32.png`, `icons/` — ícones da app
- `manifest.webmanifest` — instalação como app

