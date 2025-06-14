# Arquitetura e Componentes Principais (Conteiner):

![C4Conteiner](https://github.com/user-attachments/assets/1c3e3193-d414-4df5-9c0e-d0fae651a9d3)



O sistema é composto pelos seguintes componentes principais, conforme visualizado no diagrama de contêineres C4:

- **Usuário (Person):** Interage com o sistema através do aplicativo móvel.
- **Aplicativo Móvel (Software System):** Interface frontend para que os usuários registrem denúncias, incluindo o upload de imagens, e consultem o status de ocorrências.
- **API (Software System):** O núcleo do backend, responsável por gerenciar toda a lógica de negócios, processar as requisições do aplicativo móvel e orquestrar a comunicação entre os demais serviços.
- **Banco de Dados (Container):** Utiliza um banco de dados relacional (ex: PostgreSQL) para o armazenamento persistente dos dados das denúncias.
- **Redis SGBD (Software System):** Empregado como um banco de dados em memória para caching e armazenamento rápido de dados frequentemente acessados, otimizando a performance.
- **MinIO com Bucket (Software System):** Simula um serviço de armazenamento de objetos (compatível com S3) para guardar as imagens enviadas nas denúncias.
- **ML Microservice (Software System):** Um microsserviço externo que encapsula um modelo de Machine Learning, responsável pela análise e processamento das imagens recebidas.

### Fluxo Principal:

1. O **Usuário** acessa o **Aplicativo Móvel**.
2. O **Aplicativo Móvel** envia as requisições (registro/consulta de denúncias, upload de imagens) para a **API** via JSON/HTTPS.
3. A **API** interage com:
    - O **Banco de Dados** para persistir e consultar informações das denúncias (via SQL).
    - O **Redis SGBD** para otimizar o acesso a dados com caching (via Redis Protocol/TCP).
    - O **MinIO** para armazenar as imagens das denúncias (via S3/HTTP).
4. As imagens armazenadas no **MinIO** são enviadas para o **ML Microservice** para análise (via REST/HTTP).
5. O **ML Microservice** retorna o resultado da análise da imagem para a **API** (via JSON/HTTP), que então pode ser disponibilizado ao usuário.

Este diagrama e descrição visam fornecer uma visão clara da arquitetura do sistema e das interações entre seus componentes.
