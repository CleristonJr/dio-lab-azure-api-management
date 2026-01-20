# 🛡️ API de Pagamentos Segura com Azure API Management

Desafio de projeto do Bootcamp da **DIO** focado em segurança e gerenciamento de APIs. O objetivo foi configurar uma instância do **Azure API Management (APIM)** para proteger endpoints de uma aplicação de pagamentos simulada.

## 📋 Cenário
Uma Fintech precisa expor suas APIs de processamento de pagamentos para parceiros, mas necessita garantir:
1.  **Segurança:** Proteção contra ataques DDoS e controle de acesso via chaves (Subscription Keys).
2.  **Monitoramento:** Logs de todas as transações.
3.  **Limitação de Taxa (Throttling):** Evitar que um único parceiro derrube o sistema.

## 🛠️ Solução Implementada

### Recurso: Azure API Management
Configurado na camada **Consumption** (Serverless) para otimização de custos e escalabilidade automática.

### Configurações de Segurança
* **Front-end:** API Gateway gerenciando as requisições de entrada.
* **Back-end:** Web App protegido, não exposto diretamente à internet pública.
* **Policies:** Implementação (teórica) de validação de JWT e Rate Limiting.

## 📸 Evidências

### Painel do API Management
![APIM Overview](https://github.com/CleristonJr/dio-lab-azure-api-management/blob/main/APIM-Overview.png?raw=true)
*Instância do APIM ativa e operante na região East US 2.*

### Estrutura da API
![API Design](https://github.com/CleristonJr/dio-lab-azure-api-management/blob/main/API-Design.png?raw=true)
*Endpoint `/processar` configurado para receber transações via método POST.*

## 🧠 Aprendizados
* **API Gateway:** A importância de ter um "porteiro" controlando o tráfego antes de chegar no servidor real.
* **Camadas (Tiers):** Diferença entre o tier *Developer* (para testes com custo fixo) e *Consumption* (Serverless, paga pelo que usa).
* **Mocking:** Capacidade de simular respostas da API antes mesmo do backend estar pronto.

---
## 👨‍💻 Autor
Cleriston Jr.
www.linkedin.com/in/cleriston-júnior-ba419218b
