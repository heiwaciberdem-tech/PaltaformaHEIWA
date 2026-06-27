<div align="center">
<img src="https://ik.imagekit.io/csktgzt59/Heiwa%20IMG/img/SiteHeiwa.jpg?updatedAt=1775416000671" alt="Banner da Plataforma DebateViz">
<br>
<h3>Heiwa Plataforma de Acompanhamento de Debates.</h3>
</div>


Heiwa (Harmonia) é uma plataforma inovadora para acompanhamento, visualização e curadoria de discussões em redes sociais. Desenvolvida como parte do projeto de pesquisa do CIBERDEM (Grupo de Pesquisa e Inovação em CiberDemocracia) da Universidade Presbiteriana Mackenzie, a plataforma utiliza técnicas avançadas de Mineração de Argumentos para promover o entendimento e estimular o pensamento crítico.

     Visão Geral do Projeto
O Projeto Heiwa nasce da necessidade de transformar o cenário de conflitos e polarizações observados nas redes sociais, especialmente no contexto brasileiro. Nossa missão é ampliar o entendimento do debate digital através de ferramentas de ciência de dados para o bem social, promovendo o diálogo e o equilíbrio na conexão entre indivíduos. A plataforma atua como um hub que unifica resultados de pesquisa em diferentes áreas, facilitando a curadoria, mineração e visualização de dados.

    Funcionalidades e Arquitetura
MVP Atual
O MVP da plataforma já oferece uma base sólida e funcional, com as seguintes características:

CMS Headless com Google Sheets: Todo o conteúdo do site (notícias, publicações, membros, textos, vídeos, dados de eixos de pesquisa) é gerenciado via planilhas Google, permitindo atualizações rápidas e seguras por meio de um formulário Google integrado.

Arquitetura de Cache Resiliente: Implementação de um sistema de cache de três camadas (Apps Script Cache, Local Storage do navegador e Configuração de Roteamento) que garante baixa latência e alta disponibilidade, mesmo em uma arquitetura de baixo custo.

    Estrutura de Páginas Dinâmicas:

Páginas Institucionais: Sobre, Notícias, Publicações, Membros e Financiadores.

Eixos do Projeto: Páginas dedicadas para cada um dos cinco eixos de pesquisa (Curadoria, Extração e Limpeza, Mineração de Argumentos, Visualização de Discussões, Aspectos Éticos e Legais), cada um exibindo cards com os resultados e artefatos gerados.

Carregamento Otimizado e UX: Carregamento assíncrono de conteúdo, botões de recarga que burlam o cache para exibir dados frescos e paginação eficiente.

Segurança: Implementação de um sistema de tokens no Google Apps Script que são renovados periodicamente, adicionando uma camada extra de proteção contra acessos não autorizados.

SEO e Análise: Configuração completa com react-helmet-async para SEO dinâmico, integração com Google Analytics (GA4) e Google Search Console (GSC).

    Próximos Passos (Roadmap)
Jornada do Usuário: Desenvolvimento de uma interface guiada para que os usuários possam inserir seus próprios dados e gerar modelos de visualização personalizados.

Data Flow Interativo: Criação de uma página que demonstra todas as etapas de um fluxo de dados, orientando o usuário sobre como utilizar as ferramentas do hub.

Ampliação da Computação: Decisão e implementação da infraestrutura para processamento de dados, seja em nuvem ou com modelos pré-disponibilizados.

🚀 Tecnologias Utilizadas
Frontend
React: Biblioteca principal para construção da interface.

TypeScript: Para tipagem estática e maior segurança no código.

Vite: Build tool moderna e rápida.

Yarn: Gerenciador de pacotes.

Tailwind CSS: Framework CSS para estilização ágil.

Framer Motion: Para animações suaves e interativas.

Backend e Infraestrutura
Google Sheets: Atua como banco de dados e CMS.

Google Apps Script: Criação da API JSON e gerenciamento do cache.

Google Cloud (Mackenzie): Hospedagem principal da plataforma.

Vercel: Deploy secundário para garantir alta disponibilidade (domínio próprio: heiwa.app.br).

Análise e SEO
Google Analytics (GA4): Monitoramento de navegação.

Google Search Console: Otimização para mecanismos de busca.

    Métricas e Performance
Testes de Carga: Foram realizados testes com Apache JMeter e k6, comprovando a estabilidade do sistema.

Latência: Embora estável, o sistema apresentou picos de latência de até 4.61 segundos devido à limitação do Google Apps Script. Este é um ponto crítico que será abordado nas próximas fases.

Otimizações Implementadas: Conversão de datas para timestamps, carregamento assíncrono e caching de três camadas para melhorar a percepção de velocidade.

     Instalação e Deploy
Pré-requisitos
Node.js (versão 16 ou superior)

Yarn

Acesso ao repositório GitHub.

Configuração do Ambiente
Clone o repositório:

bash
git clone (https://github.com/heiwaciberdem-tech/PaltaformaHEIWA/)
<br>
cd mvp-heiva-plataforma-01
Instale as dependências:

bash
yarn install
Crie um arquivo .env na raiz do projeto e defina a variável de ambiente:

text
VITE_BASE_PATH=/apps/Plataforma_Heiwa/
Build para Produção
Para gerar a build otimizada para produção, execute:

bash
yarn build
Os arquivos gerados estarão na pasta dist/.

Deploy
Servidor Mackenzie: Copie o conteúdo da pasta dist/ para o diretório https://ciberdem.mack.com.br/apps/plataformaheiwa/.

Vercel: Conecte o repositório GitHub à Vercel e configure a variável de ambiente VITE_BASE_PATH para / (ou o caminho desejado).

Arquivos Essenciais para SEO
Certifique-se de que os seguintes arquivos estejam na raiz do diretório de deploy:

index.html (com as tags GA4 e GSC)

sitemap.xml

robots.txt

Ações Pós-Deploy
Verifique a propriedade no Google Search Console.

Submeta o sitemap.xml.

🏛️ Estrutura do Projeto
```
├── public/
│   ├── index.html
│   ├── sitemap.xml
│   └── robots.txt
├── src/
│   ├── components/     # Componentes reutilizáveis (Cards, Navbar, etc.)
│   ├── pages/          # Páginas da aplicação (Home, Eixos, Sobre, etc.)
│   ├── services/       # Serviços para comunicação com a API do Google Apps Script
│   ├── utils/          # Funções utilitárias (datas, formatação, etc.)
│   ├── App.tsx
│   └── main.tsx
├── .env
├── vite.config.ts
├── tailwind.config.js
├── package.json
└── README.md
```
    Contribuição
Planejamento e desenvolvimento de arquitetura e softwere por Carlos Moroni Garcia como parte de suas atividades de pesquisa no Projeto Heiwa CIBERDEM.

Equipe de idealização do Projeto Heiwa 
https://ciberdem.mack.com.br/apps/plataformaheiwa/membros

CIBERDEM - Grupo de Pesquisa e Inovação em CiberDemocracia
Universidade Presbiteriana Mackenzie
Faculdade de Computação e Informática

🔗 Links
Plataforma Principal (Mackenzie): https://ciberdem.mack.com.br/apps/plataformaheiwa/

Deploy Alternativo (Vercel): https://mvp-heiva-plataforma-01.vercel.app/

Domínio Próprio: https://heiwa.app.br/

Repositório GitHub: https://github.com/ciberdem/ProjetoHEIWA

CIBERDEM: https://ciberdem.mack.com.br/
