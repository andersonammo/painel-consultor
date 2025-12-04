👓 Painel de Alta Performance: Consultor de Ótica

Este projeto é uma Single Page Application (SPA) desenvolvida para auxiliar consultores de ótica a organizarem a sua rotina diária, acompanharem metas de vendas e gerirem o relacionamento com clientes (CRM) de forma eficiente.

O sistema funciona num único ficheiro HTML, integrado com Firebase para persistência de dados na nuvem, garantindo que as informações não se percam ao fechar o navegador.

🚀 Funcionalidades Principais

Autenticação de Utilizador: Sistema de Login e Cadastro (com encriptação básica de senha localmente antes do envio).

Cronograma Interativo: Uma linha do tempo diária com checklists de tarefas específicas para cada horário (08:00 às 18:00).

Missão Diária: Destaques automáticos baseados no dia da semana (ex: Foco em CRM na Segunda, Vendas no Sábado).

Rastreador de Performance: Gráfico interativo (Chart.js) que compara Vendas Realizadas vs. Meta Diária em tempo real.

Persistência de Dados: Integração com Google Firebase (Firestore) para salvar automaticamente:

Tarefas concluídas (Checklist).

Valores de vendas e metas.

Contagem de leads e agendamentos.

Scripts de Venda: Biblioteca de acesso rápido com roteiros para "Resgate de Clientes" e "Pós-Venda".

🛠️ Tecnologias Utilizadas

HTML5 & JavaScript (ES6+): Estrutura e lógica da aplicação.

Tailwind CSS (via CDN): Para estilização moderna e responsiva (funciona em telemóveis e desktop).

Chart.js (via CDN): Para a visualização de dados e gráficos de desempenho.

Firebase (Auth & Firestore): Backend-as-a-Service para autenticação anónima e banco de dados em tempo real.

📦 Como Usar

Não é necessária nenhuma instalação complexa (como Node.js ou Python). O projeto é "Serverless" e roda diretamente no navegador.

Opção 1: Rodar Localmente

Faça o download do arquivo index.html (ou OpticalConsultantDashboard.html).

Dê um duplo clique no arquivo para abri-lo no seu navegador (Chrome, Edge, Safari, etc.).

Crie uma conta ou faça login e comece a usar.

Opção 2: Hospedar Gratuitamente

Para aceder via link no telemóvel:

Netlify Drop: Arraste o arquivo index.html para app.netlify.com/drop.

GitHub Pages: Faça upload para um repositório GitHub e ative o GitHub Pages nas configurações.

📱 Instalação no Telemóvel (PWA Simulado)

Para ter uma experiência de aplicação nativa:

Abra o link do painel no navegador do telemóvel.

Toque no menu de opções do navegador.

Selecione "Adicionar ao Ecrã Principal".

⚙️ Configuração do Firebase

Este projeto utiliza uma configuração de demonstração. Para uso em produção, recomenda-se criar o seu próprio projeto no Firebase:

Crie um projeto em console.firebase.google.com.

Ative o Authentication (Anonymous e Email/Password).

Ative o Firestore Database e configure as regras de segurança.

Substitua a constante firebaseConfig no código pelo seu próprio objeto de configuração.

📄 Estrutura de Dados (Firestore)

Os dados são salvos na seguinte estrutura para garantir que cada consultor tenha o seu próprio histórico:

Coleção: artifacts/{appId}/public/data/daily_reports

ID do Documento: nome_do_consultor_YYYY-MM-DD

Campos:

sales (number)

goal (number)

leads (number)

appointments (number)

tasks (map/object com o estado dos checkboxes)

Desenvolvido para alta performance em vendas óticas.
