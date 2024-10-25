This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/pages/api-reference/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/pages/building-your-application/routing/api-routes) instead of React pages.

This project uses [`next/font`](https://nextjs.org/docs/pages/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn-pages-router) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/pages/building-your-application/deploying) for more details.

## Explicação CSS

Estrutura Geral

1. Variáveis Globais: Usa variáveis CSS no :root para definir as cores padrão e estilos globais, como --background (cor de fundo) e --foreground (cor do texto). A presença do prefers-color-scheme permite a troca automática entre cores claras e escuras, respeitando a preferência do usuário.

2. Reset Básico: Elementos html, body, e * garantem que o conteúdo ocupe a largura da tela (max-width: 100vw) e evite problemas de overflow horizontal.

3. Definições Globais: Tipos de letra e suavização são aplicados ao body para garantir que todo o texto e aparência visual sejam consistentes.

Módulos Específicos

1. .page
Definição de cores adicionais: Define algumas cores para fundos e efeitos (--gray-alpha-100 e --gray-alpha-200), ajustando-as com transparência (rgba) e valores diferentes para o tema claro e escuro.
Grid Layout: Estabelece uma estrutura de página em três linhas (grid-template-rows), centrando conteúdo horizontal e verticalmente.
2. .main
Conteúdo Principal: Define uma lista ordenada ol e um estilo específico para códigos, melhorando a leitura e enfatizando os textos técnicos.
3. .ctas
Botões de Ação (CTAs): Configura botões para navegação e ação (a.primary, a.secondary) com transições suaves e cores que mudam no hover, usando variáveis para facilitar a manutenção.
4. .footer
Rodapé: Exibe links com espaçamento específico e um efeito de sublinhado ao passar o mouse, ajustado para dispositivos com hover habilitado.
5. Responsividade
Em Telas Pequenas: Ajusta o layout com padding reduzido na .page, alinhamento centralizado para a .main ol, e botões de chamada de ação em coluna, tornando o layout mais compacto.
Hover Condicional: Aplicado apenas em dispositivos não-touch, melhora a experiência em desktops sem comprometer a responsividade.
