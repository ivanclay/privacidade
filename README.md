# privacidade

Políticas de privacidade dos aplicativos publicados por Ivan Moura, num repositório só.

**No ar em:** https://ivanclay.github.io/privacidade/

| Página | Endereço |
|---|---|
| Índice | `https://ivanclay.github.io/privacidade/` |
| Caderno | `https://ivanclay.github.io/privacidade/caderno/` |

É este segundo endereço que vai no campo **"Política de Privacidade"** do Google Play Console.

---

## Por que um repositório só

Cada app precisa de uma URL pública de política de privacidade para ser publicado na loja. Um
repositório por app significa um GitHub Pages por app, um domínio por app e um lugar a mais para
esquecer de atualizar.

Aqui, **uma pasta por app** resolve. O índice na raiz aponta para todas.

## Como ligar o GitHub Pages (uma vez só)

1. No repositório, **Settings → Pages**.
2. Em *Build and deployment*, **Source: Deploy from a branch**.
3. Branch **`main`**, pasta **`/ (root)`**. Salvar.
4. Esperar um ou dois minutos e abrir `https://ivanclay.github.io/privacidade/`.

O arquivo `.nojekyll` na raiz desliga o processamento do Jekyll — não há nada para processar, e sem
ele qualquer pasta ou arquivo começando com `_` seria ignorado silenciosamente.

## Como acrescentar o próximo app

```
mkdir app2
cp caderno/index.html app2/index.html
# editar app2/index.html
# acrescentar o app na lista do index.html da raiz
```

O `estilo.css` é compartilhado e fica na raiz. As páginas das pastas o referenciam por
`../estilo.css`.

**Duas coisas que não podem faltar em cada página nova:**

1. **A data de atualização no topo**, e ela muda junto com o que a página diz. Política com data
   velha e conteúdo novo é pior que não ter data.
2. **Um endereço de contato.** A Google Play exige, e a recusa por causa disso acontece na revisão,
   depois de tudo pronto.

## O que estas páginas descrevem

O que o app **guarda**, **onde** isso fica e **o que sai do aparelho** — sempre nessa ordem. Quando a
resposta da terceira for "nada", a página diz **como isso é garantido**, e não só que é verdade.

## Pendências

- [ ] **Preencher o e-mail de contato** em `caderno/index.html` — está marcado como `[preencher...]`
      na seção "Quem é o responsável". **Sem ele a política fica incompleta para a loja.**
- [ ] Ligar o GitHub Pages (passos acima).
- [ ] Conferir a página no celular antes de colar o endereço no Play Console.

## Manutenção

**Se um app passar a guardar algo diferente, a página muda antes da versão que fizer isso chegar à
loja.** No caso do Caderno, a lista do que ele guarda cresce a cada fatia — horas, estudos,
participação, e depois nomes e endereços de terceiros. Cada uma dessas entradas é uma alteração aqui.
