
# Tech Stack Map
### **O que é um Tech Stack Map?**

O **Tech Stack Map** é uma representação visual das tecnologias, ferramentas e frameworks utilizados no desenvolvimento de um sistema ou aplicação. Ele organiza os componentes do projeto em camadas (frontend, backend, banco de dados, etc.) ou de acordo com suas funções dentro da solução, permitindo uma visão clara das interdependências e do fluxo de informações.

Ele serve como um guia para desenvolvedores, stakeholders e mantenedores do sistema, ajudando a comunicar de forma transparente como as tecnologias estão estruturadas e interligadas.

### **Tech Stack Map no Projeto "DeOlhoNoLixo"**

No projeto **DeOlhoNoLixo**, o Tech Stack Map foi criado para ilustrar as tecnologias utilizadas e como elas interagem para atender às funcionalidades propostas. A estrutura está organizada nas seguintes camadas:
                                      

## Camada Front-end
![1](https://github.com/user-attachments/assets/8e324401-8df5-48a1-aa0a-668b02fee7ce)

## Camada Back-end
![2](https://github.com/user-attachments/assets/af77be85-ecab-4c6d-88bc-d8f09b224da4)

## Camada Armazenamento
![3](https://github.com/user-attachments/assets/45ad2883-f295-4a0a-b7d7-4c71d3e1911a)

## Camada Visão
![4](https://github.com/user-attachments/assets/37c4e660-91b2-4ab0-9e11-1f0df87aa138)


## Tech Stack Map
![5](https://github.com/user-attachments/assets/9e3eea2e-480a-41b9-90a3-34860e12377d)


## Tabela Descritiva

| **Camada**                | **Tecnologias Utilizadas**                                                 | **Justificativa**                                                                                                        |
|---------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Frontend (App Mobile)** | - **Flutter/Dart**<br>- **Plugins (Image_picker, HTTP)**                  | Permite desenvolvimento rápido e multiplataforma, com ótima performance em Android e iOS usando um único código-fonte.<br>Integrações facilitadas com a câmera e comunicação eficiente com o backend. |
| **Backend**               | - **Python**<br>- **FastAPI**<br>- **Docker**<br>- **Bibliotecas Adicionais (FastAPI[all], Uvicorn, Pydantic)** | Linguagem robusta, com grande ecossistema para APIs e integração com machine learning.<br>Framework rápido, moderno e fácil de usar, facilita a criação de endpoints REST performáticos e com documentação automática.<br>Garante portabilidade e facilidade de deploy em diversos ambientes (dev, produção, servidores).<br>Simplificam deploy, tipagem, validação e documentação da API. |
| **Banco de Dados**        | - **SQLite**<br>- **Redis**                                                | Solução simples, sem necessidade de servidor dedicado, suficiente para volume moderado e prototipagem rápida.<br>Armazenamento em memória para cache, aumentando a performance de consultas rápidas. |
| **Visão Computacional**   | - **OpenCV**<br>- **TensorFlow ou PyTorch**                                | Biblioteca madura e consolidada para pré-processamento de imagens e operações básicas.<br>Frameworks líderes de mercado, com excelente suporte a modelos de Machine Learning e integração direta com Python. |
| **Deploy e Serviços**     | - **Docker**                                                               | Facilita o empacotamento, escalabilidade e gerenciamento do backend e das dependências. |


## Conclusão
O Tech Stack Map apresentado proporciona uma visão clara e organizada de todas as tecnologias e ferramentas escolhidas para o desenvolvimento do projeto "DeOlhoNoLixo". Cada camada, desde o frontend até o backend, banco de dados, deploy e visão computacional, foi pensada estrategicamente para atender aos requisitos do sistema, priorizando eficiência, escalabilidade e facilidade de manutenção.


