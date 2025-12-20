# ✈️ Flight On Time - Predição Inteligente de Atrasos
### Hackathon ONE II Brasil 2025

O **Flight On Time** é uma solução Full Stack que utiliza Inteligência Artificial para prever a probabilidade de atrasos em voos, integrando dados climáticos em tempo real e modelos de Machine Learning.

---

## 🚀 Tecnologias Utilizadas

O projeto foi construído utilizando uma arquitetura de microsserviços:

* **Frontend:** HTML5, CSS3 (Design Responsivo) e JavaScript (Fetch API).
* **Backend (Orquestrador):** Java 17 com **Spring Boot 3.2**.
* **Inteligência Artificial:** Python com **Flask** e Scikit-Learn.
* **APIs Externas:** StormGlass API (Clima) e Simulação de Tráfego Aéreo.

---

## 🏗️ Arquitetura do Sistema

O fluxo de dados funciona da seguinte forma:
1. O **Frontend** envia os dados do voo para o **Backend Spring Boot** (Porta 8085).
2. O **Spring Boot** consulta dados climáticos (Temperatura/Vento) e tráfego.
3. Caso uma API externa falhe, o sistema possui **Fallback (Resiliência)** para garantir a continuidade.
4. Os dados processados são enviados ao **Servidor ML em Python** (Porta 5000).
5. O modelo de IA retorna a probabilidade, que é exibida visualmente no painel do usuário.



---

## 🛠️ Como Rodar o Projeto

### 1. Servidor de Machine Learning (Python)
```bash
cd projeto-ML/Projetosmlapi
python app.py

Porta: 5000

2. Backend API (Java/Spring)
Abrir o projeto no IntelliJ IDEA.

Certificar-se de que a variável de ambiente CLIMA_API_KEY está configurada.

Executar a classe ApiApplication.

Porta: 8085

3. Frontend
Abrir o arquivo index.html no navegador (recomenda-se usar a extensão Live Server do VS Code).

💡 Diferenciais do Projeto
Resiliência: Tratamento de erros (403 Forbidden, Connection Timeout) com políticas de Fallback para não interromper a experiência do usuário.

Interoperabilidade: Comunicação eficiente entre tecnologias distintas (Java e Python) via JSON/HTTP.

UX/UI: Card de resultado dinâmico com alertas visuais e ícones baseados em níveis de risco (Verde, Amarelo, Vermelho).

🧪 Cenários de Teste Homologados
Para validar a inteligência do modelo em diferentes contextos, sugerimos os seguintes dados:

Contexto,Origem,Destino,Distância (km),Risco Esperado
Nacional (BR),GIG,GRU,440,Baixo / Moderado
Doméstico (AU),SYD,MEL,710,Moderado
Intercontinental,GRU,SYD,13500,Alto.