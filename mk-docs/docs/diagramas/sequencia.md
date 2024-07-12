# Diagrama de Sequência

#### Cadastro de Usuário
```mermaid
---
title: Diagrama de Sequência - Cadastro de Usuário
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    
    Usuário->>App: Preenche Formulário de Cadastro
    App->>Servidor: Envia Dados de Cadastro
    Servidor->>Banco de Dados: Armazena Dados do Usuário
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>App: Resposta de Sucesso
    App-->>Usuário: Confirmação de Cadastro
```

#### Login
```mermaid
---
title: Diagrama de Sequência - Login
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    
    Usuário->>App: Insere Credenciais de Login
    App->>Servidor: Envia Credenciais
    Servidor->>Banco de Dados: Verifica Credenciais
    Banco de Dados-->>Servidor: Retorna Dados do Usuário
    Servidor-->>App: Resposta de Sucesso
    App-->>Usuário: Acesso Concedido
```

#### Explorar Serviços
```mermaid
---
title: Diagrama de Sequência - Explorar Serviços
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    
    Usuário->>App: Solicita Serviços
    App->>Servidor: Envia Requisição de Serviços
    Servidor->>Banco de Dados: Consulta Serviços Disponíveis
    Banco de Dados-->>Servidor: Retorna Lista de Serviços
    Servidor-->>App: Envia Lista de Serviços
    App-->>Usuário: Exibe Lista de Serviços
```

#### Solicitar Serviço
```mermaid
---
title: Diagrama de Sequência - Solicitar Serviço
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    participant Empresa
    
    Usuário->>App: Seleciona Serviço e Envia Solicitação
    App->>Servidor: Envia Solicitação de Serviço
    Servidor->>Banco de Dados: Armazena Solicitação
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>Empresa: Notifica Nova Solicitação
    Empresa-->>Servidor: Recebe Detalhes da Solicitação
    Servidor-->>App: Confirmação de Solicitação
    App-->>Usuário: Solicitação Enviada
```

#### Avaliar Serviço
```mermaid
---
title: Diagrama de Sequência - Avaliar Serviço
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    participant Empresa
    
    Usuário->>App: Deixa Avaliação e Nota
    App->>Servidor: Envia Dados da Avaliação
    Servidor->>Banco de Dados: Armazena Avaliação
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>Empresa: Notifica Nova Avaliação
    Empresa-->>Servidor: Recebe Detalhes da Avaliação
    Servidor-->>App: Confirmação de Avaliação
    App-->>Usuário: Avaliação Enviada
```

#### Cadastro de Empresa
```mermaid
---
title: Diagrama de Sequência - Cadastro de Empresa
---
sequenceDiagram
    participant Empresa
    participant App
    participant Servidor
    participant Banco de Dados
    
    Empresa->>App: Preenche Formulário de Cadastro
    App->>Servidor: Envia Dados de Cadastro
    Servidor->>Banco de Dados: Armazena Dados da Empresa
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>App: Resposta de Sucesso
    App-->>Empresa: Confirmação de Cadastro
```

#### Gerenciar Perfil
```mermaid
---
title: Diagrama de Sequência - Gerenciar Perfil
---
sequenceDiagram
    participant Empresa
    participant App
    participant Servidor
    participant Banco de Dados
    
    Empresa->>App: Atualiza Informações do Perfil
    App->>Servidor: Envia Dados Atualizados
    Servidor->>Banco de Dados: Atualiza Dados da Empresa
    Banco de Dados-->>Servidor: Confirmação de Atualização
    Servidor-->>App: Resposta de Sucesso
    App-->>Empresa: Perfil Atualizado
```

#### Receber Solicitações
```mermaid
---
title: Diagrama de Sequência - Receber Solicitações
---
sequenceDiagram
    participant Usuário
    participant App
    participant Servidor
    participant Banco de Dados
    participant Empresa
    
    Usuário->>App: Envia Solicitação de Serviço
    App->>Servidor: Envia Solicitação
    Servidor->>Banco de Dados: Armazena Solicitação
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>Empresa: Notifica Nova Solicitação
    Empresa-->>Servidor: Consulta Solicitação
    Servidor-->>App: Solicitação Recebida
    App-->>Usuário: Confirmação de Solicitação
```

#### Responder Avaliações
```mermaid
---
title: Diagrama de Sequência - Responder Avaliações
---
sequenceDiagram
    participant Empresa
    participant App
    participant Servidor
    participant Banco de Dados
    participant Usuário
    
    Empresa->>App: Responde Avaliação
    App->>Servidor: Envia Resposta
    Servidor->>Banco de Dados: Armazena Resposta
    Banco de Dados-->>Servidor: Confirmação de Armazenamento
    Servidor-->>Usuário: Notifica Nova Resposta
    Usuário-->>Servidor: Visualiza Resposta
    Servidor-->>App: Resposta Recebida
    App-->>Empresa: Resposta Enviada
```

Com estes diagramas de sequência, podemos visualizar claramente a interação entre os diferentes componentes do sistema durante as principais operações da plataforma WAI Conecta. Isso ajuda a garantir que todos os fluxos de trabalho sejam bem compreendidos e corretamente implementados.