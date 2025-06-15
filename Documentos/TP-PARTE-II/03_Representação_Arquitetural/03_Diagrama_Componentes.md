# Modelo C4: Componente
Nesse nível, um **componente** representa uma unidade funcional encapsulada dentro de um contêiner. Ele pode ser uma classe, um módulo, uma API, um microserviço ou qualquer outro artefato abstrato que desempenhe um papel específico no sistema. O diagrama de componentes visa descrever as interações entre esses elementos, destacando como eles colaboram para atender aos requisitos do sistema.

Essa visão é útil para desenvolvedores e equipes técnicas, pois fornece detalhes operacionais e facilita o entendimento do design, da comunicação e das responsabilidades dos elementos internos de uma aplicação.

A seguir, apresentamos o diagrama de componentes do sistema **DeOlho NoLixo**, que ilustra suas principais partes funcionais e as interações entre elas de forma integrada e visual.
![Diagrama de Componente1](https://github.com/user-attachments/assets/9ac1bf0e-4c4e-4192-90bf-83e889b3cc9d)
### **Primeira Parte: Aplicativo Móvel**

Este diagrama apresenta a arquitetura dos componentes básicos do aplicativo móvel relacionados ao front-end do sistema. O **Aplicativo Móvel** atua como um container que fornece funcionalidades de denúncia aos usuários. Seus componentes principais são:

1. **Controlador de Login**: Responsável por gerenciar a autenticação do usuário utilizando e-mail e senha.
    
2. **Controlador de Cadastro**: Permite que novos usuários realizem o cadastro no sistema.
    
3. **Controlador de Câmera**: Possibilita ao usuário capturar imagens para as denúncias.
    
4. **Controlador de Formulário**: Oferece campos para preenchimento de detalhes sobre as denúncias.
    
5. **Controlador de Feed de Denúncia**: Exibe as denúncias registradas por outros usuários.

![Diagrama de Componente2](https://github.com/user-attachments/assets/288c81f6-7fdd-467e-add4-66e684dfee4d)

### **Segunda Parte: Backend e Integrações**

Este parte do diagrama foca nos componentes do back-end e como estes se conectam ao front-end do projeto. Ele apresenta o fluxo de informações e integração entre os serviços técnicos:

1. **Componentes de Front-End**:
    
    - Autenticação de Login
    - Cadastro
    - Câmera
    - Formulário
    - Localização
2. **Back-End**:
    
    - **Banco de Dados SQL**: Centraliza as informações de login, senha e detalhes do formulário de denúncia.
    - **Banco de Dados Memória**: Gerencia informações de imagens de forma temporária.
    - **Bucket de Imagens**: Simulação de um bucket S3 para armazenar as imagens enviadas pelos usuários.
    - **IA de Categorização**: Responsável pela classificação das imagens de acordo com o nível de poluição detectado.
    - **API**: Coordenadora central, responsável por conectar o front-end, IA, bancos de dados e bucket de imagens.
    - **Sistema de Localização**: Permite o mapeamento das denúncias baseando-se em coordenadas geográficas.

![Diagrama de Componente](https://github.com/user-attachments/assets/a859581e-ba46-4045-b208-7541c13087b8)

### **Diagrama Completo: Integração Geral**

- Este é o panorama que une as partes do sistema *DeOlho NoLixo*, mostrando uma visão holística. Abrange:
    - A interação do **Aplicativo Móvel** com o backend.
    - Conexão de componentes internos como banco de dados, APIs e IA de categorização.
    - Comunicação entre os controladores do aplicativo e os serviços associados.
    - Representação de interação com sistemas como o Bucket de Imagens e a funcionalidade de localização.

Todo o fluxo do sistema organiza-se de forma coesa para captar, categorizar e mapear denúncias de maneira eficiente e estruturada.

