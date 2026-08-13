# Azores by an Islander

Site de viagem sobre os Açores, com uma tab por ilha e um reel de vídeos na página inicial.

## Estrutura de ficheiros

```
index.html   → o site completo (código + conteúdo, tudo num único ficheiro)
fotos/       → onde colocas as fotos reais de cada ilha
videos/      → onde colocas os vídeos curtos de cada ilha (para o reel)
```

Cada ficheiro `coloca-fotos-XXX-aqui.txt` e `coloca-video-XXX-aqui.txt` dentro dessas pastas
é só um marcador para saberes onde por o conteúdo de cada ilha — podes apagá-los assim
que lá puseres as fotos/vídeos verdadeiros.

---

## Passo a passo para publicar no GitHub Pages

### 1. Cria uma conta no GitHub (se ainda não tiveres)
Vai a [github.com](https://github.com) e regista-te — é gratuito.

### 2. Cria um novo repositório
- Clica no `+` no canto superior direito → **New repository**
- Nome sugerido: `azores-by-an-islander` (ou o que preferires)
- Deixa como **Public**
- Não marques nenhuma opção extra (README, .gitignore, etc.) — vamos enviar os nossos ficheiros
- Clica **Create repository**

### 3. Envia os ficheiros
Na página do repositório recém-criado:
- Clica em **uploading an existing file** (ou **Add file → Upload files**)
- Arrasta para lá o `index.html`, o `README.md`, e as pastas `fotos` e `videos` completas
- Em baixo, escreve uma mensagem como "primeira versão do site" e clica **Commit changes**

> Nota: o GitHub só aceita pastas se arrastares ficheiros lá dentro — se a pasta aparecer vazia,
> arrasta a pasta toda de uma vez a partir do explorador de ficheiros do teu computador.

### 4. Ativa o GitHub Pages
- No repositório, vai a **Settings** (no menu de cima)
- No menu lateral esquerdo, clica em **Pages**
- Em **Branch**, escolhe `main` e a pasta `/ (root)`
- Clica **Save**
- Aguarda 1-2 minutos — o GitHub mostra-te o link do site (algo como
  `https://oteunome.github.io/azores-by-an-islander/`)

### 5. Vê o site online
Abre o link que apareceu no passo anterior — o site já está publicado e é gratuito para sempre.

---

## Como editar depois

**Editar texto (introduções, conclusões):**
No site publicado, os textos de "Introdução" e "Conclusão" de cada ilha estão marcados como
editáveis diretamente na página (clicas e escreves) — mas isso só funciona *enquanto tens a
página aberta*, não guarda de forma permanente. Para uma alteração que fique guardada:
1. No GitHub, abre o `index.html`
2. Clica no ícone do lápis (**Edit**)
3. Usa `Ctrl+F` (ou `Cmd+F`) para encontrar o texto que queres mudar dentro do código
4. Edita, e clica **Commit changes** no fundo da página
5. O site atualiza-se sozinho em menos de um minuto

**Adicionar fotos reais:**
No código, cada foto tem um comentário tipo:
```html
<!-- troca por: <img src="fotos/grw-1.jpg"> -->
```
1. Coloca o ficheiro da foto na pasta `fotos/` (ex: `fotos/grw-1.jpg`)
2. No `index.html`, troca a `<div class="ph">...</div>` correspondente por
   `<img src="fotos/grw-1.jpg" alt="Graciosa">`

**Adicionar vídeos reais ao reel:**
Mesma lógica — troca o `<div class="placeholder">` dentro do `.reel-card` por:
```html
<video src="videos/grw.mp4" muted loop playsinline></video>
```
ou por um `<iframe>` do YouTube/Vimeo, se preferires alojar os vídeos lá em vez de no repositório
(recomendado se os vídeos forem grandes, para não ocupar espaço no GitHub).

**Trocar os links de trilhos por ilha:**
No `index.html`, procura por `linksIlhas` — cada cartão tem um `url` a apontar para a rede
geral de trilhos. Troca por uma página específica da ilha assim que a encontrares.
