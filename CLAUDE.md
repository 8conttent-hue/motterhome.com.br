# CLAUDE.md — MOTTERHOME

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** MOTTERHOME
**Nicho:** Viagens e Turismo
**Keywords:** Por que a gente diz Pode entrar a casa e sua Sabemos
**Paleta de cores:** slate | **Fonte:** poppins

Por que a gente diz “Pode entrar, a casa é sua!”? Sabemos o quanto a escolha do hostel pode influenciar na experiência vivida pelo viajante. Não é mesmo? Por isso, aqui no Motter Home você curte a casa à vontade: a decoração tem um ‘quê’ de vintage, combinando com a arquitetura dos anos 1950. E ainda rolam grafites, painéis e pinturas de artistas locais pra você já ir se ambientando com o clima cultural da cidade. As amizades surgem fácil em um bate-papo na cozinha, num convite pra jogar uma sinuca, na escolha do canal pra assistir um programa de TV, tomando um sol no jardim ou logo na chegada, quando você encontra seus colegas de quarto. E digo mais, só rola gente boa por aqui! A galera do Motter Home Hostel está sempre afiada com as melhores dicas da semana e adoram te ajudar a tirar dúvidas e indicar como chegar aos pontos turísticos da cidade. Se o caso for dormir bem, nossas acomodações são super confortáveis, com camas king size, solteiro ou casal. A limpeza é um dos nossos pontos fortes. Se quiser uma dica para a noite, a gente manja das melhores festas e baladas da cidade! Para quem tem uma pegada mais aventureira, alugamos bikes, oferecemos pacotes para subir as montanhas próximas, passeios de trem para conhecer a Mata Atlântica, entre outras facilidades que você só encontra no Motter Home! Aqui também tem uma mercearia com quitutes, bebidas e produtos de higiene pessoal, além dos souvenirs mais lindos e originais da cidade. Nas redondezas você encontra restaurantes, mercados, farmácias, bancos e barzinhos. Em um raio de três quadras há várias linhas de ônibus que te levam aos mais variados lugares de Curitiba. Super fácil! O Centro Histórico, uma das regiões mais procuradas pela sua agitada vida boêmia e cultural, está apenas a 15 minutos a pé. Pode vir que a casa é sua!



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-E |
| Hero | Hero-H |
| Features | Features-G |
| About Section | About-E |
| Posts | Posts-G |
| Footer | Footer-D |
| Página Sobre | Sobre-J |
| Página Contato | Contato-F |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
