# Tabela de Equivalência
A Tabela de Equivalência é uma ferramenta utilizada para garantir a descrição estruturada de funcionalidades em sistemas, mapeando as condições que representam comportamentos esperados (classe válida) e variáveis de falhas ou erros possíveis (classes inválidas). Ela é especialmente útil para análise e validação em projetos, garantindo que os requisitos técnicos e funcionais sejam atendidos.

Cada tabela auxilia desenvolvedores e analistas a identificar problemas potenciais em diferentes cenários de uso, desde registros, login, visualização de histórico até compartilhamentos e acessos à localização. Desta forma, facilita o desenvolvimento e a garantia de qualidade.


---
# H1 - Como usuário, quero fazer login com meu e-mail e senha para acessar minha conta no aplicativo.


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Campo de "descrição" obrigatório. | Campo preenchido com texto descritivo. (1) | Campo de descrição vazio. (2) | |
| Fotos adicionais no campo "referências" devem ser aceitas. | Fotos adicionadas no campo de referências. (3) | O sistema não permite anexar fotos. (4) | Fotos anexadas, mas não aparecem no envio final. (5) |
| O usuário pode preencher todos os campos e enviar. | Envio realizado com todos os campos preenchidos. (6) | O sistema não permite envio mesmo com campos preenchidos. (7) | Botão de envio inativo ou com erro. (8) |
| Até 5 fotos, cada uma ≤ 5MB, formato JPEG ou PNG. | 1 a 5 fotos JPEG/PNG, cada uma ≤ 5MB. (9) | Mais de 5 fotos enviadas. (10) | Formato inválido ou tamanho > 5MB. (11) |
| O sistema classifica automaticamente o tipo de imagem. | Classificação automática feita com sucesso. (12) | O sistema não classifica. (13) | Classificação incorreta ou aleatória. (14) |


---
# H2- Como usuário, quero preencher as minhas informações básicas para poder me cadastrar e usar o aplicativo.


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Todos os campos obrigatórios preenchidos (usuário, nome, e-mail, senha, confirmação de senha) | Todos os campos preenchidos corretamente. (1) | Campo obrigatório em branco. (2) | Campo obrigatório com formato inválido. (3) |
| Senha e confirmação de senha devem ser iguais. | Senha = Confirmar Senha. (4) | Senha ≠ Confirmar Senha. (5) | Confirmação de senha em branco. (6) |
| Campo "ver senha" funcional. | Ícone de visibilidade ativa, revela a senha. (7) | Ícone de visibilidade não funciona. (8) | Ícone indisponível ou não aparece na interface. (9) |
| O sistema deve enviar e-mail de confirmação. | E-mail de confirmação enviado ao fim do cadastro. (10) | Erro ao enviar E-mail. (11) | E-mail enviado com erro de formatação. (12) |
| O sistema deve permitir salvar o login. | Opção de salvar login marcada e funcionando. (13) | Opção marcada, mas não funciona. (14) | Opção indisponível. (15) |

---

# H3 - Como usuário, quero recuperar minha senha por e-mail para voltar a acessar minha conta

| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Captcha aparece após nova senha ser informada. | Captcha exibido após o campo de nova senha. (1) | Captcha ausente. (2) | Captcha exibido antes da senha. (3) |
| A nova senha não pode ser igual à antiga. | Nova senha diferente da anterior. (4) | Nova senha igual à anterior (mensagem de erro exibida). (5) | Nova senha fora dos padrões necessários. (6) |
| E-mail de confirmação da alteração de senha deve ser enviado. | E-mail enviado com sucesso. (7) | E-mail não enviado. (8) | E-mail enviado com erro. (9) |
| Link “Esqueci minha senha” deve estar visível na tela de login abaixo do campo senha. | Link visível e corretamente posicionado. (10) | Link não visível na tela. (11) | Link fora da posição esperada. (12) |
| O link de redefinição expira em 30 minutos após o envio. | Link usado antes de 30 minutos. (13) | Link usado após 30 minutos. (14) | Link já usado ou inválido. (15) |

---
# H4- Como usuário, quero acessar a câmera do meu celular para registrar uma denúncia sobre descarte irregular de lixo.

| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Solicitação de permissão à câmera. | O Sistema solicita permissão se ainda não concedida. (1) | O Sistema não solicita permissão. (2) | Sistema tenta acessar a câmera diretamente, causando erro. (3) |
| Mensagem explicativa ao negar permissão. | Usuário nega -> sistema exibe explicação clara sobre a necessidade. (4) | Permissão negada sem nenhuma mensagem. (5) | Mensagem exibida confusa ou genérica. (6) |
| Captura e visualização da prévia da imagem. | Usuário tira foto e visualiza uma prévia antes de confirmar. (7) | Usuário não consegue tirar foto. (8) | Foto tirada, mas sem visualização prévia. (9) |
| A imagem é vinculada corretamente à denúncia após confirmação. | Imagem confirmada → anexada corretamente à denúncia. (10) | A imagem capturada não é anexada. (11) | Imagem errada ou duplicada é anexada. (12) |
| Consentimento explícito do usuário (conforme Android/iOS). | Permissão concedida via prompt da plataforma. (13) | Permissão forçada sem consentimento. (14) | Câmera usada silenciosamente em background. (15) |
| Fotos no formato JPG ou PNG, redimensionadas. | Foto capturada e convertida/redimensionada com sucesso. (16) | Foto em outro formato. (17) | Foto muito grande, sem redimensionamento. (18) |
| Imagem usada somente na denúncia, e usuário informado. | Mensagem exibida informando uso exclusivo para denúncia. (19) | O sistema usa a imagem para outros fins. (20) | Nenhuma informação sobre o uso da imagem é apresentada ao usuário. (21) |

---

# H6- Como usuário, quero ter acesso rápido a um botão de denúncia, a fim de registrar, facilmente, um problema ambiental.


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Botão de denúncia visível apenas após login. | Botão visível apenas quando o usuário está autenticado. (1) | Botão visível antes do login. (2) | Botão não aparece mesmo após login. (3) |
| Ao tocar no botão, redireciona imediatamente para a interface de registro. | Redirecionamento instantâneo ao toque. (4) | Botão sem ação ao ser clicado. (5) | Redirecionamento para tela errada. (6) |
| Envio de denúncia permitido apenas para usuários autenticados. | Apenas usuários logados conseguem enviar a denúncia. (7) | Usuário anônimo consegue enviar denúncia. (8) | Usuário logado é impedido de enviar. (9) |
| Botão fixado em posição estratégica, sem obstruir elementos. | Botão fixado, visível, sem sobrepor menus ou campos. (10) | Botão sobrepõe conteúdo importante. (11) | Botão posicionado fora da tela. (12) |
| Registro exige imagem + descrição textual para validação. | Envio realizado com imagem + descrição. (13) | Envio apenas de imagem. (14) | Envio com apenas texto ou campos vazios. (15) |
| Sistema permite acompanhar status da denúncia após envio. | Após envio, usuário visualiza status. (16) | O sistema não oferece rastreio. (17) | Mostrar dados incorretos ou denúncias inexistentes. (18) |

---
# H7- Como usuário, quero preencher um formulário com detalhes sobre a denúncia para fornecer informações úteis às autoridades


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Campo de “descrição” obrigatório. | Campo preenchido com texto descritivo. (1) | Campo de descrição vazio. (2) | |
| Fotos adicionais no campo “referências” devem ser aceitas. | Fotos adicionadas no campo de referências. (3) | O sistema não permite anexar fotos. (4) | Fotos anexadas, mas não aparecem no envio final. (5) |
| O usuário pode preencher todos os campos e enviar. | Envio realizado com todos os campos preenchidos. (6) | O sistema não permite envio mesmo com campos preenchidos. (7) | Botão de envio inativo ou com erro. (8) |
| Até 5 fotos, cada uma ≤ 5MB, formato JPEG ou PNG. | 1 a 5 fotos JPEG/PNG, cada uma ≤ 5MB. (9) | Mais de 5 fotos enviadas. (10) | Formato inválido ou tamanho > 5MB. (11) |
| O sistema classifica automaticamente o tipo de imagem. | Classificação automática feita com sucesso. (12) | O sistema não classifica. (13) | Classificação incorreta ou aleatória. (14) |

---
# H8- Como usuário, quero compartilhar minha localização em tempo real para indicar indicar o local exato do problema.


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Botão de ativar/desativar localização. | Botão funcional e alterna corretamente entre “ativo” e “inativo”. (1) | Botão presente, mas sem efeito funcional. (2) | Botão ausente ou inoperante. (3) |
| Solicitação de permissão conforme o sistema operacional. | Permissão solicitada de forma adequada ao abrir o recurso de localização. (4) | O sistema tenta acessar sem solicitar permissão. (5) | Sistema exibe aviso genérico, sem seguir padrões da plataforma. (6) |
| Localização atualizada em tempo real quando ativada. | As coordenadas do usuário são atualizadas enquanto o botão está ativado. (7) | Localização fixa ou desatualizada mesmo com o botão ativo. (8) | Localização continua atualizando mesmo com botão desativado. (9) |
| Consentimento explícito e registrado para uso da localização (conforme LGPD). | Consentimento solicitado e logado/documentado internamente. (10) | Uso da localização sem solicitar consentimento. (11) | Consentimento pedido, mas não armazenado. (12) |

---
# H13- Como usuário, quero visualizar o histórico das denúncias que fiz, com status e respostas, para que eu saiba se estou gerando impacto e possa acompanhar o andamento das ações

| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Visualizar respostas (feedback) das denúncias realizadas. | Feedback visível para cada denúncia. (1) | Feedback ausente. (2) | Feedback exibido, mas sem contexto ou incompleto. (3) |
| Visualizar status atual das denúncias. | Status visível. (4) | Status não exibido. (5) | Status exibido incorretamente. (6) |
| Visualizar denúncias já realizadas pelo próprio usuário. | Lista de denúncias visível e filtrada por usuário. (7) | Lista vazia apesar de existirem denúncias. (8) | Lista exibe denúncias de outros usuários. (9) |
| Histórico deve ser mantido por no mínimo 1 ano após envio. | Denúncias com até 1 ano são visíveis. (10) | Denúncias com menos de 1 ano desaparecem. (11) | Denúncias com mais de 1 ano continuam aparecendo. (12) |

---

# H14- Como usuário, quero compartilhar as denúncias diretamente pelo aplicativo, para que mais pessoas tomem conhecimento e também se envolvam na causa.


| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Cada denúncia deve conter um botão de compartilhamento. | Botão de compartilhar visível e funcional em cada item de denúncia. (1) | Botão ausente em algumas denúncias. (2) | Botão aparece mas não executa nenhuma ação. (3) |
| A denúncia compartilhada deve ser acessível publicamente, mesmo sem login. | Link compartilhado abre visualização pública da denúncia. (4) | Link exige login para visualizar. (5) | Link gera erro ou redireciona incorretamente. (6) |

---
# H16 - Como usuário, quero visualizar um feed de denúncias próximas à minha localização atual para me manter informado sobre problemas ambientais na minha região.

| Condição de entrada | Classe válida | Classe inválida | Classe inválida |
|---|---|---|---|
| Solicitação e uso da localização atual para gerar o feed personalizado. | Permissão concedida -> feed baseado na localização atual. (1) | Permissão negada -> feed não aparece. (2) | Localização incorreta. (3) |
| Ordenação por mais recentes ou mais próximas com opção de alternância. | O botão de alternar funciona e ordena corretamente. (4) | O botão de alternância ausente ou inativo. (5) | Ordenação incorreta. (6) |
| Apenas dados essenciais exibidos (sem informação pessoal ou sensível). | Tipo, data, distância, status exibidos -> sem nome do denunciante. (7) | Dados pessoais. (8) | Imagens ou textos com informações sensíveis não filtradas. (9) |
| Sem denúncias próximas -> sistema informa e sugere aumentar o raio. | Mensagem clara: "Nenhuma denúncia próxima. Deseja ampliar o raio?". (10) | Mensagem genérica ou ausente. (11) | App travado ou erro ao não encontrar denúncias. (12) |
| Miniatura da imagem principal exibida com a denúncia. | Imagem visível em tamanho reduzido ao lado da denúncia. (13) | Miniatura ausente. (14) | Imagem errada ou de outra denúncia. (15) |
| Feed limitado ao raio padrão (5 km), ajustável até 20 km. | Raio inicial 5 km, com controle para aumentar até 20 km. (16) | Ajuste permitido para mais de 20 km. (17) | Raio fixo sem possibilidade de ajuste. (18) |
| Cada item do feed exibe tipo, distância, data/hora, status. | Todos os elementos obrigatórios visíveis. (19) | Um ou mais dados obrigatórios ausentes. (20) | Dados trocados. (21) |



