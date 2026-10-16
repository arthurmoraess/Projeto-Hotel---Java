# Projeto-Hotel-Java
Projeto da disciplina: Programação orientada a objetos. Ministrada pelo professor Isaac Elgrably. Projeto feito por Arthur Moraes de Souza. Outubro de 2026.
# Sistema de Gerenciamento e Análise Hoteleira

## Descrição do Problema e Usuários
Este projeto resolve o desafio de gestão de um hotel de médio porte. O sistema centraliza o controle de hospedagens, desde a realização de reservas prévias até o check-in no balcão, lançamento de serviços adicionais, controle de disponibilidade de quartos e check-out com faturamento.
**Usuários-alvo:** Recepcionistas, gerentes hoteleiros e administradores do estabelecimento.

## Principais Classes de Domínio
* `Hotel`: Centraliza os cadastros e calcula os relatórios e indicadores estatísticos.
* `Hospede`: Armazena dados cadastrais e realiza validação e formatação automática de CPF/Telefone.
* `Quarto`: Representa as acomodações com validação de faixas de preço e tipo (Essencial, Confort, Deluxe).
* `Reserva`: Registra intenções de hospedagem com cálculo de desconto automático por antecedência.
* `Hospedagem`: Controla o ciclo ativo da estadia (check-in, lista de serviços consumidos e check-out).
* `ServicoAdicional`: Registra serviços extras oferecidos pelo hotel (lavanderia, café da manhã, etc.).

## Regras de Negócio Implementadas
1. **Desconto por Antecedência:** Reservas feitas com 60+ dias têm 30% de desconto, 30+ dias têm 15%, 15+ dias têm 5%.
2. **Preço e Tipo de Quarto Rígido:** Aceita apenas diárias de R\$ 125.00 (Essencial), R\$ 250.00 (Confort) ou R\$ 500.00 (Deluxe).
3. **Bloqueio de Quarto Ocupado:** Impede novas hospedagens em quartos que já estão ocupados.
4. **Validação de Estadia:** A data de saída deve ser estritamente posterior à data de entrada.
5. **Autopreenchimento de Endereço:** Integração com ViaCEP para buscar logradouro e bairro via CEP.

## Tecnologias Utilizadas
* **Java 17 / POO**
* **Maven** (Gerenciamento de dependências)
* **Google Gson** (Persistência em arquivo `hotel.json`)
* **Java HTTP Client** (Consumo da API REST ViaCEP)

## Instruções de Configuração e Execução
1. Clone o repositório do GitHub.
2. Abra o projeto na sua IDE (VS Code, IntelliJ ou Eclipse).
3. Certifique-se de carregar as dependências do Maven.
4. Execute a classe `Main.java` situada no pacote `com.hotel`.

## Uso de Inteligência Artificial

| Ferramenta | Objetivo | Resumo do uso | Revisão pelo Dev |
| :--- | :--- | :--- | :--- |
| Gemini raciocínio 3.6 | Regras de Negócio, Documentação e README | Apoiou a definição da arquitetura inicial do código base, a modelagem da lógica das regras de negócio e a resolução de problemas de validação. | Validação manual de todas as regras, adaptação para evitar conceitos não estudados (uso de loops `for` em vez de Streams/Maps) e testes das exceções. | Auxiliou na estruturação, formatação e redação do ficheiro README.md. | conferência do fluxo e alinhamento com os requisitos da entrega. |
