```mermaid
sequenceDiagram

    participant U as Usuáro
    participant A as App
    participant P as Pedir
    participant E as Empresa

U->>A: Usuário faz Login
A->>P: Usuário solicita Pacote
P->>E: Confirmar a solicitação
E-->>P: Pedido Válido
P-->>A: Exibir Validação
U->>A: Informa endereço
A->>P: Add Endereço a solicitação
P->>E: Solicitação Concluída
E-->>P: Criando Pacote
P-->>A: Exibir tempo status do Pedido (tempo estimado para entrega)
