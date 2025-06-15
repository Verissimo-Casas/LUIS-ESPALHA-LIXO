# Arquitetura e Componentes Principais (Contexto):

![Diagrama de Contexto](https://github.com/user-attachments/assets/ae9db415-5ef3-4d76-b901-c281da08167d)
Este documento descreve o contexto do **Sistema de Denúncia de Lixo** (DeOlho NOLixo). O diagrama de contexto acima ilustra o sistema principal, os tipos de usuários que interagem com ele e os sistemas externos com os quais ele se comunica.

### Sistema Principal:

- **Sistema de Denúncia de Lixo (`Software System`)**:
    - **Responsabilidade:** É o coração da solução, permitindo o cadastro e a visualização de denúncias relacionadas ao descarte inadequado de lixo.

### Atores (Usuários):

- **Usuário (`Person`)**:
    - Indivíduos que utilizam o sistema para visualizar denúncias existentes e registrar novas ocorrências de descarte irregular de lixo.
    - Acessa diretamente o "Sistema de Denúncia de Lixo".
- **Usuário Daltônico (`Person`)**:
    - Refere-se a usuários com daltonismo que também utilizam o sistema para visualizar e registrar denúncias. Embora suas necessidades de interface possam ser específicas (não detalhadas neste nível de diagrama), sua interação fundamental com o sistema é a mesma do "Usuário" genérico.
    - Acessa diretamente o "Sistema de Denúncia de Lixo".

### Sistemas Externos e Integrações:

O "Sistema de Denúncia de Lixo" interage com os seguintes sistemas externos para prover suas funcionalidades:

1. **Sistema de E-mail (`Software System`)**:
    
    - **Função:** Envia e-mails de confirmação de cadastro aos usuários.
    - **Interação:** O "Sistema de Denúncia de Lixo" _solicita o envio de e-mails de confirmação_ a este sistema.
2. **Sistema de Geolocalização (`Software System`)**:
    
    - **Função:** Fornece dados de localização do usuário e das denúncias, auxiliando na identificação e visualização de problemas ambientais em áreas próximas.
    - **Interação:** O "Sistema de Denúncia de Lixo" _consulta a localização do usuário e/ou da denúncia_ neste sistema.
3. **Sistema de Autenticação (`Software System`)**:
    
    - **Função:** Verifica as credenciais dos usuários (login e senha, por exemplo) para permitir ou negar o acesso ao "Sistema de Denúncia de Lixo".
    - **Interação:** O "Sistema de Denúncia de Lixo" utiliza este sistema para realizar a _autenticação de acesso_ dos usuários.
4. **Sistema de Armazenamento (`Software System`)**:
    
    - **Função:** Armazena de forma persistente os dados relacionados às denúncias, como fotos, descrições detalhadas e outras informações enviadas pelos usuários.
    - **Interação:** O "Sistema de Denúncia de Lixo" _envia os dados da denúncia_ para serem armazenados neste sistema.

O diagrama de contexto (Nível 1 do Modelo C4) visa fornecer uma compreensão de alto nível do escopo do "Sistema de Denúncia de Lixo" e suas principais dependências e interações externas.
