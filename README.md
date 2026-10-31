# BuzzTier v1.11

**Rank · Organize · Compare**

Crie tier lists, organize imagens e exporte seus rankings em PNG. O BuzzTier funciona no navegador, pode ser instalado como aplicativo (PWA) e guarda as listas localmente no dispositivo.

## Novidades da versão 1.11

- Reorganização imediata: ao soltar uma imagem, a miniatura muda de lugar na hora, sem esperar a gravação do banco.
- Movimentações salvam somente os IDs e a ordem das imagens em um registro pequeno do IndexedDB; as imagens não são regravadas a cada troca.
- O editor move o elemento visual existente, sem reconstruir todas as miniaturas a cada arrasto.
- Os indicadores de destino do arrasto atualizam somente os elementos ativos, evitando percorrer a grade inteira a cada movimento do dedo.
- Botão **Baixar app** na barra superior para instalar o BuzzTier pelo Chrome.
- Quando o Chrome oferece a instalação automática, o botão abre o aviso nativo de instalação.
- Quando o navegador não oferece o aviso, o botão mostra as instruções de instalação manual.
- Manifesto PWA reforçado com identificador estável do app e ícones de 192 px, 512 px e versão maskable.
- Sensibilidade de arrastar imagens ajustada ao gesto nativo de pressão longa: espera de 500 ms e tolerância de movimento de 18 px antes de ativar.
- Service worker atualizado para v1.11, renovando o cache do aplicativo sem mexer no banco de dados.
- Bandeja fixa de imagens não classificadas com rolagem horizontal por toque, com gesto lateral habilitado também sobre as miniaturas.
- Botão Voltar do Android retorna da edição da tier list à galeria, em vez de sair do aplicativo. Se houver uma janela aberta, o primeiro toque em Voltar fecha a janela.
- As tier lists continuam no mesmo banco IndexedDB da v1.7. A atualização não apaga seus dados.

## Recursos

- Várias tier lists, com renomeação, capa personalizada e exclusão.
- Tiers personalizáveis: nome, cor, posição e exclusão.
- Adição de imagens sem títulos.
- Grade de três colunas durante a edição.
- Arrastar imagens entre tiers e reordenar dentro da mesma tier.
- Bandeja fixa para imagens ainda não classificadas.
- Exportação de screenshot PNG com largura configurável de 3 a 15 imagens por linha.
- Importação em lote com barra de progresso.
- Backup e restauração em JSON.
- PWA e modo offline depois da primeira visita.

## Instalar no Android / Chrome

1. Abra o site publicado pelo Chrome.
2. Toque em **Baixar app** dentro do BuzzTier.
3. Aceite a instalação. Se o botão mostrar instruções, use o menu ⋮ do Chrome e escolha **Instalar app** ou **Adicionar à tela inicial**.
4. Procure o BuzzTier na lista de aplicativos do celular.

Se o Chrome informar que o app já está instalado, procure por BuzzTier na lista de aplicativos. Não limpe os dados do site nem desinstale o app antes de exportar um Backup JSON.

## Publicar no GitHub Pages usando somente BuzzTier.zip

O repositório pode manter somente estes itens na raiz:

- `BuzzTier.zip` — pacote completo do site.
- `README.md` — documentação do repositório.
- `.github/workflows/deploy.yml` — automação de publicação.

Não é necessário colocar `index.html`, ícones ou manifest na raiz do repositório. O GitHub Actions extrai `BuzzTier.zip`, verifica os arquivos obrigatórios e publica o site no GitHub Pages.

### Configuração

1. Em **Settings → Pages → Build and deployment → Source**, selecione **GitHub Actions**.
2. Envie ou substitua `BuzzTier.zip` na raiz da branch `main`.
3. A execução começa automaticamente. Também pode ser iniciada manualmente em **Actions → Gerar ZIP e publicar Buzz-Tier → Run workflow**.
4. Aguarde os dois trabalhos ficarem verdes: preparação e publicação.

O site deste repositório será publicado em `https://lobopidaokk.github.io/Buzz-Tier/`.

## Dados e atualização

As tier lists são guardadas no IndexedDB do navegador e dispositivo em que foram criadas. O GitHub Pages não sincroniza automaticamente os dados entre aparelhos.

O banco mantém o mesmo nome e a mesma versão estrutural desde a v1.7. Mesmo assim, faça um **Backup** antes de atualizar, limpar dados do Chrome ou trocar de aparelho.

---

Feito com 💜 por Mika · BuzzTier v1.11
