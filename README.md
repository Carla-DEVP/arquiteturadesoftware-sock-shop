

https://github.com/user-attachments/assets/7e5f6b4d-5449-412e-8bc7-d7b1cc6ed288

# Evolução DevOps - Sock Shop

## 📌 Objetivo do Projeto
Evolução da arquitetura do projeto open-source Sock Shop (Microservices Demo), com foco na implementação de práticas reais de DevOps: observabilidade, resiliência e automação de entrega.

## 🛠️ Tecnologias e Ferramentas Utilizadas
* *Infraestrutura e Orquestração:* Docker e Docker Compose.
* *Monitoramento Contínuo:* Prometheus (coleta de métricas) e Grafana (dashboards de CPU, memória, latência e throughput).
* *Logging Centralizado:* Elastic Stack. Utilização do Filebeat para coleta nos containers, Logstash para estruturação/grok, Elasticsearch para indexação e Kibana para visualização.
* *Automação (CI/CD):* GitHub Actions automatizando a validação e o deploy contínuo do microserviço carts.

## 🚀 Como Executar o Ambiente
1. Clone este repositório:
   git clone https://github.com/Carla-DEVP/arquiteturadesoftware-sock-shop.git
2. Acesse a pasta de deploy do Docker Compose:
   cd deploy/docker-compose
3. Suba a infraestrutura completa em background:
   docker-compose up -d
4. Acesse a aplicação no navegador via http://localhost.

## 📊 Acesso às Ferramentas de Observabilidade
* *Grafana (Métricas):* Acesse http://localhost:3000. O dashboard consolida a saúde dos microserviços em tempo real.
* *Kibana (Logs):* Acesse http://localhost:5601. Os logs estão padronizados contendo Timestamp, Serviço, Severidade, IP e Mensagem.

## ⚙️ Pipeline CI/CD (Atividade Extra)
O fluxo de Integração e Entrega Contínua está implementado no arquivo .github/workflows/ci-cd-local.yml. A cada novo push na branch master, o GitHub Actions valida a estrutura e atualiza automaticamente o container do microserviço de carrinhos (carts).
