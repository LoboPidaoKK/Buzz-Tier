<div align="center">
  <img src="icon.png" alt="Ícone do BuzzTier" width="112" height="112" />
  <h1>BuzzTier</h1>
  <p><strong>Rank · Organize · Compare</strong></p>
  <p>Crie tier lists, organize imagens e exporte seus rankings em PNG.</p>
  <p>
    <img src="https://img.shields.io/badge/version-1.7-9B42D5?style=for-the-badge" alt="Versão 1.7" />
    <img src="https://img.shields.io/badge/platform-web-6B4BC3?style=for-the-badge" alt="Plataforma web" />
    <img src="https://img.shields.io/badge/storage-IndexedDB-247A70?style=for-the-badge" alt="Armazenamento IndexedDB" />
  </p>
</div>

---

## ✨ Sobre o projeto

O **BuzzTier** é um criador de tier lists feito para organizar imagens em categorias personalizadas. Ele funciona no navegador, pode ser instalado como aplicativo (PWA) e mantém os dados localmente no dispositivo.

## 🚀 Recursos

- **Várias tier lists:** crie, renomeie, personalize a capa e organize diferentes rankings.
- **Categorias personalizadas:** crie tiers, altere nomes, escolha cores, reorganize ou exclua categorias.
- **Imagens sem títulos:** adicione imagens do dispositivo sem precisar preencher nomes ou descrições.
- **Grade de três colunas:** organize as imagens em uma grade clara durante a edição.
- **Reordenação:** mova imagens entre tiers, para a bandeja de não classificadas e para qualquer posição dentro da mesma tier.
- **Bandeja fixa:** imagens ainda não classificadas ficam acessíveis no rodapé do editor.
- **Screenshot em PNG:** exporte o ranking e escolha de 3 a 15 imagens por linha. Essa configuração vale somente para a exportação.
- **Importação em lote:** acompanhe o progresso, a porcentagem, a quantidade processada e eventuais falhas.
- **Backup e restauração:** exporte e importe suas listas em JSON.
- **PWA e modo offline:** instale o BuzzTier no dispositivo e use o cache offline depois da primeira visita.

## 📱 Arrastar imagens no celular

Para evitar movimentos acidentais durante a rolagem da página, o arraste no celular exige uma ação deliberada:

1. Toque e mantenha o dedo parado sobre a imagem por aproximadamente **650 ms**.
2. Quando aparecer o contorno roxo, a imagem estará pronta para ser arrastada.
3. Sem levantar o dedo, mova a imagem até a tier ou posição desejada e solte.

**Atenção:** se o dedo começar a se mover antes de completar a espera, o arraste é cancelado e a rolagem normal continua. Um toque simples ainda abre o menu da imagem.

No computador, use o arraste normal do mouse.

## 💾 Seus dados e backups

As tier lists são guardadas no **IndexedDB do navegador**. Isso significa que os dados ficam no navegador e dispositivo em que foram criados; publicar o site no GitHub Pages não sincroniza automaticamente as listas entre aparelhos.

Recomendação: use **Backup** na página inicial antes de atualizar o aplicativo, limpar os dados do navegador ou trocar de dispositivo. Para recuperar suas listas, use **Restaurar** e selecione o arquivo JSON exportado anteriormente.

## 🌐 Publicar no GitHub Pages

O repositório já inclui o workflow `/.github/workflows/deploy.yml`. Ele faz duas coisas quando há um push para a branch `main`:

1. Prepara os arquivos estáticos e publica o BuzzTier no **GitHub Pages**.
2. Gera `BuzzTier-v1.7.zip` e disponibiliza o arquivo como artefato para download na execução do GitHub Actions.

### Configuração inicial

1. Crie um repositório no GitHub, por exemplo, `BuzzTier`.
2. Envie **o conteúdo desta pasta** para a raiz do repositório. O `index.html` deve ficar diretamente na raiz, e a pasta `.github/workflows/` também precisa ser enviada.
3. Abra **Settings → Pages**.
4. Em **Build and deployment → Source**, selecione **GitHub Actions**.
5. Faça um commit na branch `main`.
6. Abra a aba **Actions** e acompanhe a execução **Gerar ZIP e publicar BuzzTier**.
7. Quando terminar com sucesso, abra a execução e baixe o artefato **BuzzTier-v1.7-ZIP** na seção *Artifacts*.
8. O endereço do site aparecerá no resumo do trabalho de publicação. Para um repositório chamado `BuzzTier`, o formato será `https://SEU-USUARIO.github.io/BuzzTier/`.

O workflow também pode ser iniciado manualmente em **Actions → Gerar ZIP e publicar BuzzTier → Run workflow**.

## 🗂️ Estrutura do repositório

```text
BuzzTier/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── .nojekyll
├── README.md
├── LEIA-ME.txt
├── index.html
├── icon.png
├── icon-original.png
├── manifest.webmanifest
└── sw.js
```

## 🧰 Tecnologias

- HTML, CSS e JavaScript puro
- IndexedDB para armazenamento local
- Canvas API para exportação PNG
- Progressive Web App (PWA) e Service Worker
- GitHub Actions e GitHub Pages para automação e publicação

## 📌 Histórico

| Versão | Alterações |
|---|---|
| 1.0–1.5 | Estrutura inicial, listas, tiers, imagens, capas e exportação configurável |
| 1.6 | Reordenação de imagens e barra de progresso da importação |
| **1.7** | Arraste no celular com espera maior e cancelamento quando o gesto indica rolagem |

---

<div align="center">
  <sub>Feito com 💜 por Mika · BuzzTier v1.7</sub>
</div>
