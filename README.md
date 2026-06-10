# Treino · Hipertrofia — Webapp

PWA de acompanhamento de treinos de hipertrofia. Mobile-first, sem servidor, sem cadastro.

## Funcionalidades

- 6 fichas de treino (Seg–Sex + Sábado Plus)
- Registro de carga (kg) e repetições por série
- Marcação de série concluída
- Cronômetro de descanso com vibração e presets (1min / 1:30 / 2min / 3min)
- Histórico de sessões salvo no localStorage (permanente no celular)
- Tela de evolução com gráfico de progressão de carga por exercício
- Instalável como PWA (ícone na tela inicial)

---

## Deploy no GitHub Pages (passo a passo)

### 1. Crie um repositório no GitHub

1. Acesse [github.com](https://github.com) → clique em **New repository**
2. Nome sugerido: `meu-treino` (ou qualquer nome)
3. Deixe como **Public**
4. Não inicialize com README (você vai subir os arquivos)
5. Clique em **Create repository**

### 2. Suba os arquivos

**Opção A — Pelo site (mais simples):**
1. Na página do repositório vazio, clique em **uploading an existing file**
2. Arraste os arquivos `index.html` e `manifest.json` para a área de upload
3. Clique em **Commit changes**

**Opção B — Via terminal:**
```bash
cd pasta-dos-arquivos
git init
git add .
git commit -m "primeira versão"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/meu-treino.git
git push -u origin main
```

### 3. Ative o GitHub Pages

1. No repositório → aba **Settings**
2. Menu lateral: **Pages**
3. Em "Branch": selecione `main` e pasta `/root`
4. Clique em **Save**
5. Aguarde ~2 minutos → seu app estará em:
   `https://SEU_USUARIO.github.io/meu-treino/`

---

## Instalar como app no celular

### iPhone (Safari):
1. Abra a URL no Safari
2. Toque no botão de compartilhar (quadrado com seta)
3. Role e toque em **Adicionar à Tela de Início**
4. Confirme o nome e toque em **Adicionar**

### Android (Chrome):
1. Abra a URL no Chrome
2. Toque nos três pontos (menu)
3. Toque em **Adicionar à tela inicial**
4. Confirme

---

## Adicionar ícone personalizado (opcional)

Para ter um ícone bonito na tela inicial:
1. Crie duas imagens PNG: `icon-192.png` (192×192px) e `icon-512.png` (512×512px)
2. Suba junto com os outros arquivos no repositório
3. Use um fundo escuro (#0a0a0a) com um símbolo simples (haltere, raio, etc.)

Gerador gratuito: [realfavicongenerator.net](https://realfavicongenerator.net)

---

## Estrutura de arquivos

```
meu-treino/
├── index.html      ← app completo (HTML + CSS + JS em um único arquivo)
├── manifest.json   ← configuração PWA
├── icon-192.png    ← ícone (opcional mas recomendado)
└── icon-512.png    ← ícone grande (opcional mas recomendado)
```

---

## Histórico e dados

- Todos os dados ficam no `localStorage` do navegador do celular
- Não são enviados a nenhum servidor
- Persistem entre sessões enquanto o browser não for limpo
- Para exportar: tela Evolução → funcionalidade de export será adicionada na V2

---

## Roadmap V2

- [ ] Export de histórico em CSV
- [ ] Semana atual vs semana anterior (comparação)
- [ ] Alerta de deload automático (semana 4)
- [ ] Modo escuro / claro alternável
- [ ] Backup via JSON para Google Drive
