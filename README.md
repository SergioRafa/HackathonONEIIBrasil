✈️ Flight On Time - Dashboard Preditivo com IA
🏆 Projeto Destaque | Hackathon ONE II Brasil 2025
O Flight On Time é uma plataforma Full Stack de alta performance que utiliza Inteligência Artificial para antecipar atrasos em voos. O sistema cruza dados geográficos, climáticos em tempo real e densidade de tráfego para fornecer uma análise de risco precisa.

🚀 
⚡ Inteligência Híbrida: Integração entre Java (Spring Boot) e Python (Flask/Machine Learning).

📡 Dados Reais: Consumo da API StormGlass para buscar temperatura e vento exatos no momento da consulta.

🛡️ Engenharia de Resiliência: Sistema de Fallback inteligente que garante uma resposta ao usuário mesmo em caso de falha nas APIs externas.

🎨 UI/UX Dinâmica: Painel com indicadores visuais que mudam de cor (Verde, Amarelo, Vermelho) conforme o grau de risco calculado pela IA.

🏗️ Arquitetura e Fluxo de Dados
O projeto utiliza uma estrutura de microsserviços orquestrada para máxima eficiência:

Frontend (UI): Captura os dados IATA e processa a entrada automática em maiúsculas para evitar erros de busca.

Backend (Orquestrador Java): Recebe a requisição, geolocaliza o aeroporto e consome dados meteorológicos em tempo real.

Core de IA (Python): Processa o JSON recebido através de um modelo de inteligência artificial treinado.

Entrega: O resultado retorna ao dashboard com feedback visual instantâneo e ícones dinâmicos.

🛠️ Tecnologias e Ferramentas
Camada,Tecnologia
Frontend,"HTML5, CSS3 (Modern Flexbox/Grid), JavaScript (ES6+)"
Backend,"Java 17, Spring Boot 3.2, Maven"
IA / ML,"Python 3.x, Flask, Scikit-Learn, Pandas"
Conectividade,"Ngrok (Túnel HTTP), Fetch API"
APIs,StormGlass (Weather Data)

⚙️ Configuração e Execução
1. Núcleo de Inteligência (Python)
 cd projeto-ML/Projetosmlapi
python app.py
# O servidor subirá na porta 5000

2. Orquestrador de Dados (Java)
Importe o projeto no IntelliJ IDEA.

Certifique-se de que a porta 8085 está liberada.

Execute a classe ApiApplication.

3. Interface do Usuário (Navegador)
Utilize o Live Server no VS Code para abrir o arquivo index.html.

O frontend está configurado para comunicar-se via túnel Ngrok.

🧪 Matriz de Testes Homologados
Cenário,Origem,Destino,Distância,Risco Esperado
Ponte Aérea,GIG,GRU,440 km,✅ Baixo / Moderado
Doméstico AU,SYD,MEL,710 km,⚠️ Moderado
Intercontinental,GRU,SYD,13.500 km,🚨 Alto

👥 Desenvolvedores
SergioRafa (Líder Técnico & Frontend/Backend)

Wesley (Colaborador / Repositório Original)

Gemini (Mentoria Técnica & IA Partner)
