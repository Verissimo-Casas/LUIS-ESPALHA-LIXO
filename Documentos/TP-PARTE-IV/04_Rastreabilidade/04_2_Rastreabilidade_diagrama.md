# Rastreabilidade com os diagramas

---

## Funcionalidade: Login

**Diagrama de Classe:**  
Utiliza as classes `LoginPage`, `LoginViewModel`, `AuthRepository`, `AuthRemoteDS`, `AuthLocalDS`.

**Diagrama C4 (Container):**  
A funcionalidade faz parte do container “Aplicativo Móvel”, que se comunica com o container “API”, responsável por autenticar o usuário via Sistema de Autenticação e armazenar dados no Banco de Dados SQL.

**Diagrama C4 (Componente):**  
Utiliza o Controlador de Login que aciona o Componente de Autenticação de Login. A autenticação é feita via API e armazenada no Banco de Dados SQL.

<div align="center">
  <img src="https://github.com/user-attachments/assets/eef4cdec-3537-4060-b33e-888e96b8aa39" width="300" alt="Captura de tela 2025-07-09 233106">
</div>

---

## Funcionalidade: Cadastro

**Diagrama de Classe:**  
Utiliza as classes `RegisterPage`, `RegisterViewModel`, `AuthRepository`, `AuthRemoteDS`, `AuthLocalDS`.

**Diagrama C4 (Container):**  
O cadastro acontece no “Aplicativo Móvel”, que envia os dados para a API, a qual salva os dados no Banco de Dados SQL e aciona o Sistema de E-mail para envio de confirmação.

**Diagrama C4 (Componente):**  
Usa o Controlador de Cadastro e o Componente de Cadastro para preencher e validar os dados antes do envio à API.

<div align="center">
  <img src="https://github.com/user-attachments/assets/6cf04dae-5e74-47d8-b0bf-527a43ef0829" width="300" alt="Captura de tela 2025-07-09 233106">
</div>

---

## Funcionalidade: Recuperação de senha

**Diagrama de Classe:**  
Utiliza as classes `LoginPage`, `LoginViewModel`, `AuthRepository`, `AuthRemoteDS`, `AuthLocalDS`.

**Diagrama C4 (Container):**  
O “Aplicativo Móvel” envia requisição para API, que valida o e-mail e aciona o Sistema de E-mail para envio de recuperação de senha.

**Diagrama C4 (Componente):**  
Utiliza o Controlador de Login, que aciona o Componente de Autenticação de Login para validar o e-mail informado e solicitar à API o envio do link de recuperação por meio do Sistema de E-mail.

<div align="center">
  <img src="https://github.com/user-attachments/assets/706c8c98-0ba7-43c5-a8b4-7dc20c4a9fef" width="300" alt="Captura de tela 2025-07-09 233106">
</div>

---

## Funcionalidade: Acesso à câmera

**Diagrama de Classe:**  
Utiliza as classes `CameraPage`, `CameraViewModel`, `MediaRepository`, `MediaLocalDS`.

**Diagrama C4 (Container):**  
O Aplicativo Móvel captura imagem e envia via API, que armazena no MinIO com Bucket. A imagem também é analisada por ML microservice.

**Diagrama C4 (Componente):**  
O Controlador de Câmera usa o Componente de Câmera, que envia a imagem via HTTP para a API.

<div align="center">
  <img src="https://github.com/user-attachments/assets/85885d18-269a-4d9e-b26a-757c55b7d69c" width="300" alt="Captura de tela 2025-07-09 233106">
</div>

---

## Funcionalidade: Acesso rápido ao botão de denúncia

**Diagrama de Classe:**  
Utiliza as classes `FeedPage`, `DenunciaFormPage`.

**Diagrama C4 (Container):**  
Localizado no Aplicativo Móvel, com acesso direto à funcionalidade de denúncia. Ao clicar, o app interage com o backend para enviar os dados ao Banco de Dados.

**Diagrama C4 (Componente):**  
O botão está presente em múltiplos controladores, principalmente no Controlador de Feed de Denúncia, que redireciona ao Controlador de Formulário.

---

## Funcionalidade: Formulário de denúncia

**Diagrama de Classe:**  
Utiliza as classes `DenunciaFormPage`, `DenunciaFormViewModel`, `DenunciaRepository`, `DenunciaRemoteDS`, `DenunciaLocalDS`.

**Diagrama C4 (Container):**  
O formulário enviado do Aplicativo Móvel é processado pela API, que armazena no Banco de Dados SQL e Redis para cache.

**Diagrama C4 (Componente):**  
O Controlador de Formulário usa o Componente de Formulário para coleta e envio de dados.

---

## Funcionalidade: Compartilhar localização

**Diagrama de Classe:**  
Utiliza as classes `DenunciaFormPage`, `DenunciaFormViewModel`, `GeoRepository`, `GeoRemoteDS`.

**Diagrama C4 (Container):**  
O Aplicativo Móvel acessa o Sistema de Geolocalização via API para obter coordenadas e popular o campo “Localização”.

**Diagrama C4 (Componente):**  
O Controlador de Formulário utiliza o Componente de Localização, que envia e consulta a geolocalização.

---

## Funcionalidade: Feed de denúncias

**Diagrama de Classe:**  
Utiliza as classes `FeedPage`, `FeedViewModel`, `DenunciaRepository`, `GeoRepository`, `DenunciaRemoteDS`, `GeoRemoteDS`.

**Diagrama C4 (Container):**  
A funcionalidade é exibida no Aplicativo Móvel, que consome dados da API que acessa o Banco de Dados SQL e Redis para listar denúncias com base na geolocalização.

**Diagrama C4 (Componente):**  
O Controlador de Feed de Denúncia usa o Componente de Localização para filtrar denúncias próximas.
