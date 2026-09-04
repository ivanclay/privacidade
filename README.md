# privacidade

Políticas de privacidade dos aplicativos publicados por Ivan Moura, num repositório só.

**No ar em:** https://ivanclay.github.io/privacidade/

| Página | Endereço |
|---|---|
| Índice | `https://ivanclay.github.io/privacidade/` |
| Caderno | `https://ivanclay.github.io/privacidade/caderno/` |
| SAuto | `https://ivanclay.github.io/privacidade/sauto/` |
| SMarket | `https://ivanclay.github.io/privacidade/smarket/` |

**No Google Play Console, cada app recebe o endereço da PASTA DELE** — nunca o do índice e nunca o
de outro app. O campo se chama *"Política de Privacidade"* e fica na configuração do app.

> ⚠ Apontar o Console de um app para a página de outro não dá erro em lugar nenhum: a página abre,
> o campo aceita, e a revisão pode passar. O que fica publicado é uma **declaração formal sobre
> práticas que não são as daquele app** — e quem lê uma política não tem como conferir.

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

- [x] ~~Preencher o e-mail de contato em `caderno/index.html`~~ · feito em 2026-09-02.
- [x] ~~Ligar o GitHub Pages~~ · feito em 2026-09-02.
- [ ] Conferir a página no celular antes de colar o endereço no Play Console.
- [ ] SMarket: conferir a data, a versão e o e-mail de contato do topo da página.
- [ ] **SAuto: apontar o Play Console para `.../privacidade/sauto/`.** O aplicativo ainda não foi
      submetido; a página existe porque a tela "Sobre" dentro do app precisa linkar para ela.
- [ ] **SAuto: o app ainda não tem cópia de segurança nem assinatura.** A página já diz que as duas
      chegam e que ela muda antes — **é essa promessa que precisa ser cumprida**, não esquecida.
- [ ] **SAuto: falta o EULA (termos de uso).** Este repositório só tem políticas de privacidade, e a
      tela "Sobre" do SAuto linka para os dois documentos. O segundo não existe em lugar nenhum.

## Manutenção

**Se um app passar a guardar algo diferente, a página muda antes da versão que fizer isso chegar à
loja.** No caso do Caderno, a lista do que ele guarda cresce a cada fatia — horas, estudos,
participação, e depois nomes e endereços de terceiros. Cada uma dessas entradas é uma alteração aqui.
