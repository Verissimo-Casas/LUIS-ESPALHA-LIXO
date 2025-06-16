
```mermaid
  flowchart LR

  %% Color definitions - C4 Model blue and white theme
  classDef personStyle fill:#4B9BF1,stroke:#052E56,color:#ffffff
  classDef containerStyle fill:#4B9BF1,stroke:#0B4884,color:#ffffff
  classDef componentStyle fill:#4B9BF1,stroke:#346AC1,color:#ffffff
  classDef systemStyle fill:#999999,stroke:#777777,color:#ffffff
  classDef externalStyle fill:#B3B3B3,stroke:#8A8A8A,color:#ffffff
  classDef bind stroke-dasharray:5 5,stroke:#08427B
  
    %% ========== VIEWS ==========
    subgraph Views["Views • Flutter Widgets"]
      direction TB
      LoginPage["LoginPage\n(H1)"]
      RegisterPage["RegisterPage\n(H2)"]
      CameraPage["CameraPage\n(H4)"]
      DenunciaFormPage["DenunciaFormPage\n(H7)"]
      FeedPage["FeedPage\n(H16)"]
    end
  
    %% ========== VIEWMODELS ==========
    subgraph "ViewModels"
      direction TB
      LoginVM["LoginViewModel"]
      RegisterVM["RegisterViewModel"]
      CameraVM["CameraViewModel"]
      DenunciaFormVM["DenunciaFormViewModel"]
      FeedVM["FeedViewModel"]
    end
  
    %% ========== MODEL (Repositories) ==========
  subgraph Model["Model"]
      direction TB
      AuthRepo["AuthRepository"]
      DenunciaRepo["DenunciaRepository"]
      MediaRepo["MediaRepository"]
      GeoRepo["GeoRepository"]
    end
  
    %% ========== DATA SOURCES ==========
    subgraph DataSources["Data Sources"]
      direction TB
      %% Remote
      AuthRemote["AuthRemoteDS\n(Dio/Retrofit)"]
      DenRemote["DenunciaRemoteDS"]
      GeoRemote["GeoRemoteDS"]
      %% Local
      AuthLocal["AuthLocalDS\n(Hive)"]
      DenLocal["DenunciaLocalDS"]
      MediaLocal["MediaLocalDS"]
      %% Plugins
      CameraPlugin["camera / image_picker"]
      GPSPlugin["geolocator"]
      PermPlugin["permission_handler"]
    end
  
    %% ========== INFRA ==========
    subgraph Infra
      direction TB
      RemoteAPI["REST API (HTTPS)"]
      LocalDB["sqflite / Hive files"]
    end
  
    %% ------- BINDINGS View ↔ VM (reativo) -------
    classDef bind stroke-dasharray:4 4
    LoginPage --bind--> LoginVM:::bind
    RegisterPage --bind--> RegisterVM:::bind
    CameraPage --bind--> CameraVM:::bind
    DenunciaFormPage --bind--> DenunciaFormVM:::bind
    FeedPage --bind--> FeedVM:::bind
    LoginVM --> LoginPage:::bind
    RegisterVM --> RegisterPage:::bind
    CameraVM --> CameraPage:::bind
    DenunciaFormVM --> DenunciaFormPage:::bind
    FeedVM --> FeedPage:::bind
  
    %% ------- VM → Repositories -------
    LoginVM --> AuthRepo
    RegisterVM --> AuthRepo
    CameraVM --> MediaRepo
    CameraVM --> DenunciaRepo
    DenunciaFormVM --> MediaRepo
    DenunciaFormVM --> DenunciaRepo
    FeedVM --> GeoRepo
    FeedVM --> DenunciaRepo
  
    %% ------- Repositories → DataSources -------
    AuthRepo --> AuthRemote
    AuthRepo --> AuthLocal
  
    DenunciaRepo --> DenRemote
    DenunciaRepo --> DenLocal
  
    MediaRepo --> CameraPlugin
    MediaRepo --> MediaLocal
    MediaRepo --> PermPlugin
  
    GeoRepo --> GPSPlugin
    GeoRepo --> GeoRemote
    GeoRepo --> PermPlugin
  
    %% ------- DataSources → Infra -------
    AuthRemote --> RemoteAPI
    DenRemote --> RemoteAPI
    GeoRemote --> RemoteAPI
    AuthLocal --> LocalDB
    DenLocal --> LocalDB
    MediaLocal --> LocalDB
  
    %% ------- Offline sync / token refresh -------
    DenLocal -.sync.-> DenRemote
    AuthLocal -.token.-> AuthRemote


  %% Apply styles to subgraphs - using C4 Model color palette
  class Views personStyle
  class ViewModels containerStyle
  class Model componentStyle
  class DataSources componentStyle
  class Infra systemStyle
```

---

### Views

As **Views** representam a interface do usuário do sistema. No nosso caso, as Views são as **telas e componentes visuais do aplicativo mobile**, implementadas usando **Flutter Widgets**. Elas são responsáveis por exibir informações e capturar interações do usuário, funcionando como a "cara" do aplicativo. As Views observam e reagem a mudanças de estado fornecidas pelos seus respectivos ViewModels, garantindo uma UI dinâmica e responsiva.

---

### ViewModels

Os **ViewModels** são o elo entre a interface (Views) e a lógica de negócio (Model). Eles contêm o **estado da UI e a lógica de apresentação**, transformando os dados do Model em um formato que a View pode facilmente consumir. Utilizando gerenciadores de estado como **Provider** ou **Riverpod**, os ViewModels expõem dados reativos e métodos que as Views chamam em resposta a ações do usuário. Isso desacopla a View da complexidade do Model.

---

### Model

O **Model**, na nossa arquitetura, é materializado pelos **Repositories**. Cada Repository é uma camada de abstração que **define as operações de dados** para uma entidade específica (ex: usuários, denúncias, mídias). Eles atuam como coordenadores, ocultando a complexidade da origem dos dados (seja local ou remota) e oferecendo uma interface limpa e consistente aos ViewModels. Os Repositories são a única parte do Model com a qual os ViewModels interagem diretamente.

---

### Data Sources

As **Data Sources** são os **componentes que realmente executam as operações de acesso e persistência de dados**. Elas são especializadas: temos Data Sources **remotas** para comunicação com APIs externas (usando ferramentas como Dio/Retrofit), **locais** para interagir com o armazenamento interno do dispositivo (como Hive ou sqflite) e **baseadas em plugins** para funcionalidades específicas do dispositivo (como câmera ou GPS). As Data Sources são orquestradas pelos Repositories.

---

### Infra

A camada de **Infraestrutura** abrange os **recursos externos e tecnologias de baixo nível** com os quais o aplicativo se comunica. Isso inclui a **REST API**, que representa o servidor backend onde os dados das denúncias são armazenados e processados, e os **LocalDB**, que são os arquivos físicos no dispositivo onde os dados locais são persistidos (como um banco de dados SQLite ou arquivos Hive). Essa separação permite a troca de tecnologias de infraestrutura sem impactar as demais camadas da aplicação.
