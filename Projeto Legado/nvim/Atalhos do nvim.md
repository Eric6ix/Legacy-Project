# Principais atalhos Neovim (consulta rápida)

O significado de cada sequência depende do **modo** atual (normal, inserção, visual, linha de comando) e de **prefixos** (por exemplo, um número antes de um comando repete a ação).

## Modos

Keymap: " i "
  --Explicação: Entra no modo de inserção com o cursor **antes** do caractere sob o cursor; texto novo fica à esquerda dele. Só faz sentido a partir do modo normal.

Keymap: " a "
  --Explicação: Entra no modo de inserção **depois** do caractere sob o cursor (um caractere à frente em relação a `i`). Útil para acrescentar no fim da palavra sob o cursor.

Keymap: " A "
  --Explicação: Vai para o **fim da linha** atual e entra no modo de inserção (equivalente a `$` seguido de `a`).

Keymap: " I "
  --Explicação: Vai para o **início da linha** (primeiro caractere não em branco, como `^`) e entra no modo de inserção.

Keymap: " o "
  --Explicação: Abre uma **nova linha abaixo** da atual, move o cursor para ela e entra no modo de inserção.

Keymap: " O "
  --Explicação: Abre uma **nova linha acima** da atual, move o cursor para ela e entra no modo de inserção.

Keymap: " v "
  --Explicação: Entra no modo **visual por caractere**; movimentos expandem a seleção caractere a caractere.

Keymap: " V "
  --Explicação: Entra no modo **visual por linha**; linhas inteiras entram na seleção.

Keymap: " Ctrl+v "
  --Explicação: Entra no modo **visual em bloco** (coluna retangular); permite editar várias linhas alinhadas verticalmente.

Keymap: " : "
  --Explicação: Entra na **linha de comando** na parte inferior da tela para comandos ex (`:w`, `:q`, `:e`).

Keymap: " Esc "
  --Explicação: Sai do modo de inserção, visual ou substituição e volta ao **modo normal** (em muitos terminais, `Ctrl+[` é equivalente).

Keymap: " R "
  --Explicação: Entra no modo **substituição** (sobrescreve caractere a caractere até sair com `Esc`).

Keymap: " r "
  --Explicação: No modo normal, substitui **um único** caractere sob o cursor pelo próximo caractere digitado, sem entrar no modo de inserção completo.

## Movimento básico

Keymap: " h j k l "
  --Explicação: No modo normal (e em outros modos onde aplicável), move o cursor **esquerda, baixo, cima, direita**; são os movimentos básicos por um caractere ou linha.

Keymap: " w "
  --Explicação: Avança para o **início da próxima palavra** (delimitação “word” do Vim).

Keymap: " W "
  --Explicação: Como `w`, mas usa **WORDS** (delimitadas por espaço em branco), saltos maiores.

Keymap: " e "
  --Explicação: Vai para o **fim da palavra** atual ou, se já no fim, para o fim da próxima.

Keymap: " E "
  --Explicação: Como `e`, mas para **WORDS** em vez de palavras curtas.

Keymap: " b "
  --Explicação: Recua para o **início da palavra** anterior.

Keymap: " B "
  --Explicação: Como `b`, mas para **WORDS**.

Keymap: " 0 "
  --Explicação: Vai para a **coluna 0** (primeiro caractere da linha, inclusive espaço).

Keymap: " ^ "
  --Explicação: Vai para o **primeiro caractere não em branco** da linha.

Keymap: " $ "
  --Explicação: Vai para o **último caractere** da linha atual.

Keymap: " g g "
  --Explicação: Vai para a **primeira linha** do buffer.

Keymap: " G "
  --Explicação: Vai para a **última linha** do buffer; com número antes (`5G`), vai para essa linha.

Keymap: " { "
  --Explicação: Salta para o **parágrafo** anterior (bloco separado por linha em branco).

Keymap: " } "
  --Explicação: Salta para o **próximo** parágrafo.

Keymap: " % "
  --Explicação: Com o cursor sobre `(`, `[`, `{` ou equivalente de fechamento, salta para o **delimitador correspondente**.

Keymap: " f "
  --Explicação: No modo normal, `f` + caractere move para a **próxima ocorrência** desse caractere na linha (para trás usa `F`).

Keymap: " t "
  --Explicação: Como `f`, mas para **antes** do caractere procurado (`T` faz o mesmo para trás).

Keymap: " ; "
  --Explicação: Repete o último movimento **`f`**, **`F`**, **`t`** ou **`T`** na mesma direção.

Keymap: " , "
  --Explicação: Repete o último **`f`/`F`/`t`/`T`** na **direção oposta** à de `;`.

Keymap: " H M L "
  --Explicação: Move o cursor para a **parte alta**, **meio** ou **baixa** da **área visível** da janela (não do arquivo inteiro).

Keymap: " Ctrl+u "
  --Explicação: Rola a janela **meia tela para cima** (mantém contexto com o cursor).

Keymap: " Ctrl+d "
  --Explicação: Rola a janela **meia tela para baixo**.

Keymap: " Ctrl+b "
  --Explicação: Rola **uma tela para cima** (back).

Keymap: " Ctrl+f "
  --Explicação: Rola **uma tela para baixo** (forward).

## Edição, delete, yank e put

Keymap: " x "
  --Explicação: Apaga o caractere **sob o cursor** (como `dl`); no modo normal, sem entrar em inserção.

Keymap: " X "
  --Explicação: Apaga o caractere **antes** do cursor na linha (como `dh`).

Keymap: " dd "
  --Explicação: Apaga a **linha inteira** onde está o cursor e coloca em um registro (corta para colar com `p`).

Keymap: " D "
  --Explicação: Apaga do cursor até o **fim da linha** (`d$`).

Keymap: " cc "
  --Explicação: Apaga a **linha inteira** e entra no modo de inserção (mudança da linha).

Keymap: " C "
  --Explicação: Apaga do cursor até o **fim da linha** e entra no modo de inserção.

Keymap: " s "
  --Explicação: Substitui o caractere sob o cursor: apaga um caractere e entra em inserção (`cl`).

Keymap: " S "
  --Explicação: Apaga a **linha inteira** e entra em inserção (como `cc`).

Keymap: " yy "
  --Explicação: **Copia** (yank) a linha inteira para o registro padrão, sem apagar.

Keymap: " Y "
  --Explicação: Em muitas configurações equivale a **`yy`** (yank da linha).

Keymap: " p "
  --Explicação: **Cola** o registro depois do cursor (linha inteira cola na linha abaixo se o registro for linha).

Keymap: " P "
  --Explicação: Cola **antes** do cursor (linha inteira cola acima).

Keymap: " u "
  --Explicação: **Desfaz** a última alteração no modo normal (histórico de undo).

Keymap: " U "
  --Explicação: Desfaz todas as alterações na **linha atual** (comportamento mais raro que `u`).

Keymap: " Ctrl+r "
  --Explicação: **Refaz** o que foi desfeito com `u` (redo).

Keymap: " . "
  --Explicação: Repete a **última mudança** feita (muito útil após `cw`, `dd`, etc.).

Keymap: " J "
  --Explicação: **Junta** a linha de baixo ao fim da linha atual (remove a quebra de linha entre elas).

Keymap: " >> "
  --Explicação: **Indenta** a linha atual (ou seleção com operador).

Keymap: " << "
  --Explicação: **Remove indentação** da linha atual.

## Busca

Keymap: " / "
  --Explicação: Abre busca **para frente** na linha de comando; `Enter` confirma; `n` / `N` navegam ocorrências.

Keymap: " ? "
  --Explicação: Busca **para trás** no buffer (mesmo fluxo que `/` com direção invertida).

Keymap: " n "
  --Explicação: Vai para a **próxima** ocorrência da última busca (mesma direção da busca).

Keymap: " N "
  --Explicação: Vai para a ocorrência **anterior** em relação à direção de `n`.

Keymap: " * "
  --Explicação: Busca **para frente** a palavra sob o cursor (word) sem digitar o padrão.

Keymap: " # "
  --Explicação: Busca **para trás** a palavra sob o cursor.

Keymap: " :noh "
  --Explicação: Comando que **remove o realce** temporário das ocorrências de busca até a próxima busca.

## Visual e operadores

Keymap: " d "
  --Explicação: **Operador delete**: espera um movimento ou objeto de texto; por exemplo `dw` apaga até o fim da palavra, `d$` até o fim da linha.

Keymap: " c "
  --Explicação: **Operador change**: apaga o alcance do movimento e entra em **modo de inserção** (`cw`, `ciw`, etc.).

Keymap: " y "
  --Explicação: **Operador yank**: copia o alcance indicado pelo movimento (`yw`, `y$`, `yy` como atalho de linha).

Keymap: " diw "
  --Explicação: **Delete inner word**: apaga a palavra sob o cursor **sem** espaços ao redor (objeto de texto “inner word”).

Keymap: " daw "
  --Explicação: **Delete a word**: apaga a palavra **com** um espaço adjacente quando aplicável (word “a”).

Keymap: " ciw "
  --Explicação: **Change inner word**: apaga a palavra interna e fica em inserção (substituir a palavra inteira).

Keymap: " caw "
  --Explicação: **Change a word**: como `ciw`, mas inclui o tratamento de espaço de `daw`.

Keymap: " c i \" "
  --Explicação: **Change inside quotes** (no teclado: `c`, `i`, aspas duplas): com o cursor dentro de aspas duplas, apaga o conteúdo **entre** elas e entra em inserção; `ci'` e `ci)` usam o delimitador correspondente.

Keymap: " d i \" "
  --Explicação: **Delete inside quotes** (`d`, `i`, aspas duplas): remove só o que está **dentro** das aspas duplas, mantendo as aspas.

Keymap: " dip "
  --Explicação: **Delete inner paragraph**: apaga o parágrafo atual (bloco entre linhas em branco).

Keymap: " > "
  --Explicação: Operador de **indentação** com movimento (ex.: `>ip` indenta o parágrafo interno).

Keymap: " g~ "
  --Explicação: **Inverte maiúsculas/minúsculas** no alcance do movimento (ex.: `g~iw` na palavra).

Keymap: " gv "
  --Explicação: Reativa a **última seleção visual** com o mesmo alcance (modo normal).

## Janelas e splits

Keymap: " Ctrl+w s "
  --Explicação: Divide a janela **horizontalmente** (nova janela com o mesmo buffer ou fluxo de split padrão).

Keymap: " Ctrl+w v "
  --Explicação: Divide a janela **verticalmente** (dois painéis lado a lado).

Keymap: " Ctrl+w n "
  --Explicação: Abre uma nova janela com um **buffer vazio** (novo “arquivo” não salvo).

Keymap: " Ctrl+w q "
  --Explicação: Fecha a **janela atual** (como `:close`); se for a última janela do buffer, o comportamento segue as regras do Vim.

Keymap: " Ctrl+w o "
  --Explicação: Mantém só a **janela atual** e fecha as outras do layout (`only`).

Keymap: " Ctrl+w w "
  --Explicação: Alterna o foco para a **próxima** janela na ordem de ciclo.

Keymap: " Ctrl+w W "
  --Explicação: Alterna para a janela **anterior** no ciclo (direção oposta a `Ctrl+w w`).

Keymap: " Ctrl+w h "
  --Explicação: Move o foco para a janela à **esquerda**.

Keymap: " Ctrl+w j "
  --Explicação: Move o foco para a janela **abaixo**.

Keymap: " Ctrl+w k "
  --Explicação: Move o foco para a janela **acima**.

Keymap: " Ctrl+w l "
  --Explicação: Move o foco para a janela à **direita**.

Keymap: " Ctrl+w = "
  --Explicação: **Igual** as alturas e larguras das janelas no layout atual.

Keymap: " Ctrl+w _ "
  --Explicação: Maximiza a **altura** da janela atual (ou define altura com prefixo numérico).

Keymap: " Ctrl+w | "
  --Explicação: Maximiza a **largura** da janela atual (ou define com número).

## Extras Neovim

Keymap: " :terminal "
  --Explicação: Abre um **terminal embutido** em um split (Neovim); o shell interativo roda dentro do editor.

Keymap: " Ctrl+\\ Ctrl+n "
  --Explicação: Com o foco no buffer do terminal, volta ao **modo normal** do Neovim (sai do “modo terminal” para navegar/copy no histórico).

Keymap: " :e "
  --Explicação: Linha de comando **`edit`**: abre um caminho no buffer atual ou novo (`:e nome_do_arquivo`).

Keymap: " :enew "
  --Explicação: Abre um **buffer novo vazio** na janela atual.

Keymap: " :bn "
  --Explicação: **`bnext`**: vai para o **próximo** buffer da lista (sem fechar o anterior).

Keymap: " :bp "
  --Explicação: **`bprevious`**: vai para o **buffer anterior**.

Keymap: " :bd "
  --Explicação: **`bdelete`**: remove o buffer da lista (cuidado com alterações não salvas; o Vim pergunta se necessário).

Keymap: " :ls "
  --Explicação: Lista **buffers** carregados com número e estado (modificado, etc.).

Keymap: " :sp "
  --Explicação: Split **horizontal** e opcionalmente edita outro arquivo (`:sp arquivo`).

Keymap: " :vsp "
  --Explicação: Split **vertical** (`:vsplit`), mesma ideia com layout em colunas.
