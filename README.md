# Aula 1-Engenharia-de-Software

```mermaid
sequenceDiagram

 participant U as Usuários
 participant A as APP
participant B as Backend
participant BD as Bancos de Dados

U->>A: Click Endereço
note over A: GPS integrado
A->>B: Ender (look, useID)
B->>BD: Buscar ruas e números UserID
BD-->B: Endereços
note over B: Calcular Distância
B-->>A: Histórico, Distância
A-->>U: Pesquisa novo endereço ou existente
