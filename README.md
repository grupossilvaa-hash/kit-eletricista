# Pack Tesouro do Eletricista — página de vendas

Landing estática de venda do **Pack Tesouro do Eletricista Residencial**: plataforma de
consulta com +100 esquemas elétricos residenciais, cada um com diagrama, lista de material
quantificada e especificação de bitola e proteção.

- **Avatar:** eletricista residencial autônomo e "marido de aluguel", 24 a 45 anos.
- **Dor:** executa bem e vende mal — o que trava não é a mão, é o papel.
- **Mecanismo:** não é curso nem pasta de PDF. É plataforma de consulta que abre no
  celular, no meio da obra, com busca, filtro e zoom.

## Stack

HTML + CSS + JS puros, arquivo único (`index.html`). Sem build, sem dependência, sem
servidor — abre direto no navegador. Imagens em `img/`.

Gerada a partir de `padrao-paginas-de-vendas/base/index.html` (mesma estrutura, seletores
e scripts do padrão da linha; mudam só copy, imagens, fontes e paleta).

- **Fontes:** Barlow (display) + IBM Plex Sans (texto), via Google Fonts.
- **Paleta:** azul-marinho `#17395B` (primária) · âmbar `#C98A14` (CTA) ·
  verde `#4FAE82` (sucesso) · vermelho `#E2635C` (alerta).

## Planos e checkout

| Plano | Preço | Campanha (UTM) |
|---|---|---|
| Completo | R$ 27,90 (de R$ 47,00) | `ele-completo` |
| Básico | R$ 19,90 | `ele-basico` |
| Downsell (exit-intent) | R$ 19,90 | `ele-downsell` |

> **Nota:** a copy v2 do produto descreve **oferta única** de R$ 19,90. A estrutura de dois
> planos foi adotada para alinhar com o resto da linha (rural e PMOC) e com os mockups
> `mockup-plano-completo` / `mockup-plano-basico`, que já foram gerados nesse formato.
> Confirmar os preços antes de subir campanha.

> ⚠️ **Pendente:** as três URLs de checkout estão como `SKU-COMPLETO`, `SKU-BASICO` e
> `SKU-DOWNSELL`. O `window.pixelId` da UTMify também está como placeholder, e o bloco do
> Meta Pixel está vazio.
>
> Depoimentos, estatísticas e o especialista são **placeholder** — substituir por reais.

## Onde publica

Vercel, via Git. Todo push na `main` publica em produção.
