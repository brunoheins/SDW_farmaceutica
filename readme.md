# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 27 de Dezembro de 2025

**Empresa:** Abstergo Industries

**Responsável:** Bruno Heins

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Bruno Heins. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos através da migração de uma infraestrutura física local para a nuvem.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos focados na redução de CAPEX (investimento em capital) e otimização de OPEX (despesas operacionais). A seguir, serão descritas as etapas do projeto:

### Etapa 1:
* **Ferramenta:** Amazon EC2 com instâncias Reserved (RI) ou Savings Plans.
* **Foco da ferramenta:** Computação escalável sob demanda.
* **Descrição de caso de uso:** Para um hub de distribuição, os servidores de inventário e logística não precisam ser dimensionados para o pico máximo de demanda 24/7. Ao migrar para o EC2, a empresa deixa de gastar com energia, resfriamento e hardware físico. Através do **Savings Plans**, a empresa se compromete com um uso estável por 1 ou 3 anos em troca de descontos de até 72%, eliminando o custo de manter servidores físicos ociosos durante a madrugada.
* **Principal Ganho:** Eliminação de gastos com manutenção de hardware e redução drástica no custo por hora de computação.

### Etapa 2:
* **Ferramenta:** Amazon S3 (Simple Storage Service) com S3 Intelligent-Tiering.
* **Foco da ferramenta:** Armazenamento de dados escalável e automático.
* **Descrição de caso de uso:** Empresas farmacêuticas precisam armazenar grandes volumes de dados por anos devido a regulamentações de saúde. Em vez de comprar storages físicos caros, o S3 armazena esses dados. O **Intelligent-Tiering** move automaticamente os arquivos que não são acessados para camadas de armazenamento mais baratas (como o Archive Instant Access), garantindo que a empresa nunca pague por "espaço premium" para dados antigos.
* **Principal Ganho:** Redução de custos de armazenamento em até 95% comparado a discos físicos locais para dados de longo prazo.

### Etapa 3:
* **Ferramenta:** AWS Lambda.
* **Foco da ferramenta:** Computação Serverless (sem servidor).
* **Descrição de caso de uso:** O hub de distribuição possui processos que rodam apenas em momentos específicos, como o processamento de pedidos no final do dia ou geração de relatórios de transporte. Em vez de manter um servidor ligado o mês inteiro para tarefas que duram 10 minutos, o Lambda executa o código apenas quando disparado.
* **Principal Ganho:** Cobrança por milissegundo de execução; se o código não rodar, o custo é **zero**.

## Conclusão
A implementação de ferramentas na empresa Abstergo Industries tem como esperado a redução dos custos fixos de manutenção de data center e a conversão de gastos variáveis em um modelo de pagamento pelo uso. Isso aumentará a eficiência e a produtividade da empresa, permitindo que o capital economizado seja reinvestido na logística de distribuição. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por tecnologias como o **AWS Cost Explorer** para monitorar a economia em tempo real.

## Anexos
1. Comparativo de custos: On-Premises vs. AWS (TCO Calculator).
2. Guia de boas práticas de segurança em nuvem para o setor farmacêutico.
3. Plano de migração de banco de dados para instâncias gerenciadas.

**Assinatura do Responsável pelo Projeto:**
Bruno Heins
