
# Tech Stack Map
### **O que é um Tech Stack Map?**

O **Tech Stack Map** é uma representação visual das tecnologias, ferramentas e frameworks utilizados no desenvolvimento de um sistema ou aplicação. Ele organiza os componentes do projeto em camadas (frontend, backend, banco de dados, etc.) ou de acordo com suas funções dentro da solução, permitindo uma visão clara das interdependências e do fluxo de informações.

Ele serve como um guia para desenvolvedores, stakeholders e mantenedores do sistema, ajudando a comunicar de forma transparente como as tecnologias estão estruturadas e interligadas.

### **Tech Stack Map no Projeto "DeOlhoNoLixo"**

No projeto **DeOlhoNoLixo**, o Tech Stack Map foi criado para ilustrar as tecnologias utilizadas e como elas interagem para atender às funcionalidades propostas. A estrutura está organizada nas seguintes camadas:
                                      

## Camada Front-end
![Camada-front](https://github.com/user-attachments/assets/42d194ad-4161-4fa3-b52a-667f58c1422b)

## Camada Back-end
![Camada-back](https://github.com/user-attachments/assets/7c9d23ba-94fa-4a75-8c20-6bd82fcce6fc)

## Camada Armazenamento
![Camada-armazenamento](https://github.com/user-attachments/assets/36f8235e-123b-4878-9f6c-788afad27780)

## Camada Visão
![Camada-visao](https://github.com/user-attachments/assets/7df24dea-63f3-47a2-bbb9-897427d9385b)

## Tech Stack Map
![Tech-map](https://github.com/user-attachments/assets/3f694bb7-48af-4f53-8c99-ddc897582e17)

## Tabela Descritiva

| **Camada**              | **Tecnologias Utilizadas**                                                                 | **Justificativa**                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Frontend (App Mobile)** | - **Flutter/Dart**                                                                       | Permite desenvolvimento rápido e multiplataforma, com ótima performance em Android e iOS usando um único código-fonte.       |
|                         | - **SQLite**                                                                              | Banco de dados leve, ideal para armazenamento local no dispositivo e funcionamento offline.                                  |
|                         | - **Plugins (Image_picker, HTTP)**                                                        | Integrações facilitadas com a câmera e comunicação eficiente com o backend.                                                  |
| **Backend**             | - **Python**                                                                              | Linguagem robusta, com grande ecossistema para APIs e integração com machine learning.                                       |
|                         | - **FastAPI**                                                                             | Framework rápido, moderno e fácil de usar, facilita a criação de endpoints REST performáticos e com documentação automática.  |
|                         | - **Docker**                                                                              | Garante portabilidade e facilidade de deploy em diversos ambientes (dev, produção, servidores).                              |
|                         | - **Bibliotecas Adicionais (FastAPI[all], Uvicorn, Pydantic)**                             | Simplificam deploy, tipagem, validação e documentação da API.                                                                |
| **Banco de Dados**      | - **SQLite**                                                                              | Solução simples, sem necessidade de servidor dedicado, suficiente para volume moderado e prototipagem rápida.                |
| **Visão Computacional** | - **OpenCV**                                                                              | Biblioteca madura e consolidada para pré-processamento de imagens e operações básicas.                                       |
|                         | - **TensorFlow ou PyTorch**                                                               | Frameworks líderes de mercado, com excelente suporte a modelos de Machine Learning e integração direta com Python.           |
| **Deploy e Serviços**   | - **Docker**                                                                              | Facilita o empacotamento, escalabilidade e gerenciamento do backend e das dependências.
