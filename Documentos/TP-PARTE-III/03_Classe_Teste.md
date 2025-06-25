# H1 - - Como usuário, quero fazer login com meu e-mail e senha para acessar minha conta no aplicativo.

| Caso de teste | Classes de equivalência       | Entradas                                  | Resultado esperado                                          |
|---------------|-------------------------------|-------------------------------------------|------------------------------------------------------------|
| Caso 1        | 1,4,7,10,13,16,19            | Campos de e-mail e senha corretos, opção de ver funcional | Acesso e redirecionamento, senha oculta com opção de mostrar senha |
| Caso 2        | 2,4,7,10,13,16,19            | Campo de e-mail ausente na interface      | Falha ao realizar login, e-mail não identificado           |
| Caso 3        | 3,4,7,10,13,16,19            | Campo de senha ausente na interface       | Falha ao realizar login, senha não identificada            |
| Caso 4        | 1,5,7,10,13,16,19            | Campo de senha vazio                      | Falha ao realizar login, campo de senha vazio              |
| Caso 5        | 1,6,7,10,13,16,19            | Campo de senha preenchido com espaços     | Falha ao realizar login, senha inválida                    |
| Caso 6        | 1,4,8,10,13,16,19            | E-mail correto, senha incorreta           | Falha ao realizar login, e-mail ou senha inválida          |
| Caso 7        | 1,4,9,10,13,16,19            | E-mail incorreto, senha correta           | Falha ao realizar login, e-mail ou senha inválida          |
| Caso 8        | 1,4,7,11,13,16,19            | Senha visível mesmo sem a opção “ver/ocultar” selecionada | Interface com falha de privacidade                         |
| Caso 9        | 1,4,7,12,13,16,19            | Botão de “ver” senha inoperante           | Interface com falha de funcionalidade                      |
| Caso 10       | 1,4,7,10,14,16,19            | E-mail com domínio @yahoo                 | Falha ao realizar login, domínio não permitido             |
| Caso 11       | 1,4,7,10,15,16,19            | E-mail sem domínio                        | Falha ao realizar login, e-mail inválido                   |
| Caso 12       | 1,4,7,10,13,17,19            | Senha <= 5 caracteres                     | Falha ao realizar login, senha inválida                    |
| Caso 13       | 1,4,7,10,13,18,19            | Senha em branco                           | Falha ao realizar login, senha inválida                    |
| Caso 14       | 1,4,7,10,13,18,20            | O sistema não bloqueia o login temporariamente após 3 tentativas | Falha de segurança, sistema não aplica bloqueio             |
| Caso 15       | 1,4,7,10,13,18,21            | O sistema bloqueia antes das 3 tentativas | Falha de configuração, bloqueio antecipado                 |


---


# H2 - Como usuário, quero preencher as minhas informações básicas para poder me cadastrar e usar o aplicativo.


| Caso de teste | Classes de equivalência       | Entradas                                         | Resultado esperado                                     |
|---------------|-------------------------------|------------------------------------------------|-----------------------------------------------------|
| Caso 1        | 1,4,7,10,13                  | Campos preenchidos corretamente e confirmações recebidas | Cadastro realizado com sucesso                      |
| Caso 2        | 2,4,7,10,13                  | Campo obrigatório vazio                         | Falha ao cadastrar, campo obrigatório vazio          |
| Caso 3        | 3,4,7,10,13                  | Formato inválido no campo obrigatório           | Falha ao cadastrar, formato inválido                |
| Caso 4        | 1,5,7,10,13                  | Senha de confirmação diferente da senha informada | Falha ao cadastrar, as senhas informadas não conferem |
| Caso 5        | 1,6,7,10,13                  | Campo de confirmar senha vazio                  | Falha ao cadastrar, campo de confirmação de senha vazio |
| Caso 6        | 1,4,8,10,13                  | Ícone de visibilidade não responde              | Falha ao mostrar senha                               |
| Caso 7        | 1,4,9,10,13                  | Ícone não disponível                            | Falha ao mostrar senha                               |
| Caso 8        | 1,4,7,11,13                  | Erro no envio do e-mail de confirmação          | Falha ao cadastrar, erro ao enviar e-mail            |
| Caso 9        | 1,4,7,12,13                  | E-mail enviado com conteúdo corrompido          | Falha ao cadastrar, e-mail com erro de formatação   |
| Caso 10       | 1,4,7,10,14                  | “Salvar login” marcado, mas não funciona        | Falha ao salvar login                               |
| Caso 11       | 1,4,7,10,15                  | “Salvar login” não aparece na interface         | Falha ao apresentar a opção de salvar login         |

---
# H3 - Como usuário, quero recuperar minha senha por e-mail para voltar a acessar minha conta.

| Caso de teste | Classes de equivalência       | Entradas                                             | Resultado esperado                                      |
|---------------|-------------------------------|-----------------------------------------------------|--------------------------------------------------------|
| Caso 1        | 1,4,7,10,13                  | Nova senha válida inserida e captcha feito          | Senha alterada com sucesso                             |
| Caso 2        | 2,4,7,10,13                  | Captcha não aparece após a nova senha ser inserida  | Falha na validação de segurança                        |
| Caso 3        | 3,4,7,10,13                  | Captcha aparece antes de digitar a senha            | Falha de sequência                                     |
| Caso 4        | 1,5,7,10,13                  | Nova senha igual à anterior                         | Falha ao alterar senha, a nova senha não pode ser igual à anterior |
| Caso 5        | 1,6,7,10,13                  | Nova senha com padrão inválido                      | Falha ao alterar senha, senha inválida                 |
| Caso 6        | 1,4,8,10,13                  | E-mail de confirmação não enviado                   | Falha no envio de e-mail de confirmação                |
| Caso 7        | 1,4,9,10,13                  | E-mail enviado com erro (corrompido ou incompleto)  | Falha no processo de envio                             |
| Caso 8        | 1,4,7,11,13                  | Opção de “Esqueci minha senha” não aparece na interface | Usuário impossibilitado de alterar senha              |
| Caso 9        | 1,4,7,12,13                  | Opção de “Esqueci minha senha” visível, mas fora da posição | Problema de interface/UX                              |
| Caso 10       | 1,4,7,10,14                  | Acesso ao link depois de 30 minutos                 | Link expirado, acesso negado                           |
| Caso 11       | 1,4,7,10,15                  | Link utilizado ou inválido                          | Acesso negado                                          |

---
# H4 - Como usuário, quero acessar a câmera do meu celular para registrar uma denúncia sobre descarte irregular de lixo.

| Caso de teste | Classes de equivalência       | Entradas                                                                | Resultado esperado                                      |
|---------------|-------------------------------|------------------------------------------------------------------------|--------------------------------------------------------|
| Caso 1        | 1,4,7,10,13,16,19            | Usuário autoriza o acesso à câmera, permissão para realizar a denúncia ou usuário nega permissão | Fluxo de explicação de autorização ou fluxo de captura e envio de imagem |
| Caso 2        | 2,4,7,10,13,16,19            | O sistema não solicita permissão                                       | Falha de segurança, erro na captura                   |
| Caso 3        | 3,4,7,10,13,16,19            | Sistema acessa câmera sem permissão                                    | Erro na câmera, falha de privacidade                   |
| Caso 4        | 1,5,7,10,13,16,19            | Permissão negada sem mensagem                                          | Falta de feedback ao usuário                          |
| Caso 5        | 1,6,7,10,13,16,19            | Mensagem confusa após a negação de permissão                           | Falha de comunicação/UX                                |
| Caso 6        | 1,4,8,10,13,16,19            | Usuário não consegue tirar foto                                        | Processo interrompido                                  |
| Caso 7        | 1,4,9,10,13,16,19            | Foto retirada, mas sem visualização prévia                             | Falta de confirmação visual da imagem                 |
| Caso 8        | 1,4,7,11,13,16,19            | Imagem retirada não é anexada                                          | Falha ao realizar denúncia                            |
| Caso 9        | 1,4,7,12,13,16,19            | Imagem errada ou duplicada anexada                                     | Falha de integridade da evidência                     |
| Caso 10       | 1,4,7,10,14,16,19            | Permissão forçada sem consentimento                                    | Violação de consentimento                              |
| Caso 11       | 1,4,7,10,15,16,19            | Câmera usada silenciosamente em background                             | Bloqueio, risco de privacidade                        |
| Caso 12       | 1,4,7,10,13,17,19            | Foto em formato não suportado                                          | Rejeição da imagem                                    |
| Caso 13       | 1,4,7,10,13,18,19            | Foto muito grande, não redimensionada                                  | Falha de envio, imagem pode ficar distorcida          |
| Caso 14       | 1,4,7,10,13,18,20            | O sistema usa a imagem para outros fins                                | Violação de privacidade                               |
| Caso 15       | 1,4,7,10,13,18,21            | Informação sobre o uso da imagem não informada                         | Desrespeito com a conformidade da LGPD                |

---

# H6 - Como usuário, quero ter acesso rápido a um botão de denúncia, a fim de registrar, facilmente, um problema ambiental.

| Caso de teste | Classes de equivalência       | Entradas                                             | Resultado esperado                                     |
|---------------|-------------------------------|-----------------------------------------------------|-------------------------------------------------------|
| Caso 1        | 1,4,7,10,13,16                | Todos os comportamentos válidos                     | Fluxo completo e correto de denúncia após login       |
| Caso 2        | 2,4,7,10,13,16                | Botão visível antes do login                        | Botão não deveria estar visível antes do login        |
| Caso 3        | 3,4,7,10,13,16                | Botão não aparece mesmo após login                  | Falha ao exibir botão após autenticação               |
| Caso 4        | 1,5,7,10,13,16                | Botão sem ação ao ser clicado                       | Nenhum redirecionamento ocorre ao clicar no botão     |
| Caso 5        | 1,6,7,10,13,16                | Redirecionamento para tela errada                   | Redirecionamento leva à interface incorreta           |
| Caso 6        | 1,4,8,10,13,16                | Usuário anônimo consegue enviar denúncia            | Envio de denúncia não é permitido para usuários anônimos |
| Caso 7        | 1,4,9,10,13,16                | Usuário logado é impedido de enviar denúncia        | Usuário autenticado deveria conseguir enviar a denúncia |
| Caso 8        | 1,4,7,11,13,16                | Botão sobrepõe conteúdo importante                  | Botão está cobrindo elementos relevantes da interface |
| Caso 9        | 1,4,7,12,13,16                | Botão posicionado fora da tela                      | Botão não aparece na tela por estar fora do campo de visão |
| Caso 10       | 1,4,7,10,14,16                | Envio apenas de imagem                              | Não é feita a descrição textual                       |
| Caso 11       | 1,4,7,10,15,16                | Envio com apenas texto ou campos vazios             | Dados insuficientes para validar o envio da denúncia  |
| Caso 12       | 1,4,7,10,13,17                | O sistema não oferece rastreio                      | Usuário não consegue acompanhar o status de sua denúncia |
| Caso 13       | 1,4,7,10,13,18                | Sistema exibe dados incorretos ou denúncias inexistentes | Informações de rastreio incorretas ou denúncias inexistentes são exibidas |

---

# H7 - Como usuário, quero preencher um formulário com detalhes sobre a denúncia para fornecer informações úteis às autoridades.

| Caso de teste | Classes de equivalência       | Entradas                                             | Resultado esperado                                                           |
|---------------|-------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| Caso 1        | 1,3,6,9,12                   | Campos preenchidos corretamente                     | Formulário realizado com sucesso                                            |
| Caso 2        | 2,3,6,9,12                   | Campo de descrição vazia                            | Falha ao enviar o formulário, campo de descrição obrigatório não preenchido |
| Caso 3        | 1,4,6,9,12                   | Sistema não permite anexar fotos                    | Falha ao anexar fotos                                                       |
| Caso 4        | 1,5,6,9,12                   | Fotos anexadas mas não aparecem no envio final      | Falha ao anexar fotos, imagens salvas incorretamente                        |
| Caso 5        | 1,3,7,9,12                   | Envio não é permitido mesmo com campos preenchidos  | Falha no envio                                                              |
| Caso 6        | 1,3,8,9,12                   | Botão de envio inativo                              | Botão de envio desabilitado                                                 |
| Caso 7        | 1,3,6,10,12                  | Mais de 5 fotos anexadas                            | Limite de 5 fotos excedidas                                                 |
| Caso 8        | 1,3,6,11,12                  | Formato de imagem inválido                          | Falha ao anexar fotos, formato ou tamanho inválidos                         |
| Caso 9        | 1,3,6,9,13                   | O sistema não classifica imagem                     | Falha na classificação automática                                           |
| Caso 10       | 1,3,6,9,14                   | Classificação incorreta ou aleatória                | Classificação automática incorreta                                          |

---

# H8 - Como usuário, quero compartilhar minha localização em tempo real para indicar indicar o local exato do problema.

| Caso de teste | Classes de equivalência       | Entradas                                             | Resultado esperado                                                  |
|---------------|-------------------------------|-----------------------------------------------------|----------------------------------------------------------------------|
| Caso 1        | 1,4,7,10                     | Todos os comportamentos válidos                     | Localização ativada corretamente, com permissão e consentimento registrados |
| Caso 2        | 2,4,7,10                     | O botão está presente, mas não tem efeito funcional | A localização não pode ser ativada pois o botão está inoperante     |
| Caso 3        | 3,4,7,10                     | Botão de localização ausente ou não funcional       | Não é possível ativar ou desativar a localização                    |
| Caso 4        | 1,5,7,10                     | O sistema tenta acessar sem solicitar permissão     | Acesso à localização negado por ausência de solicitação formal      |
| Caso 5        | 1,6,7,10                     | Sistema exibe aviso genérico sem seguir padrões     | Solicitação de permissão inconsistente com os padrões da plataforma |
| Caso 6        | 1,4,8,10                     | Localização fixa ou desatualizada com botão ativo   | Coordenadas não são atualizadas em tempo real                       |
| Caso 7        | 1,4,9,10                     | Localização continua atualizando com botão desativado | Sistema continua rastreando mesmo com a funcionalidade desativada   |
| Caso 8        | 1,4,7,11                     | Localização usada sem consentimento                 | Uso da localização sem que o usuário tenha concedido permissão explícita |
| Caso 9        | 1,4,7,12                     | Consentimento foi pedido, mas não armazenado        | Sistema não registra o consentimento para uso posterior             |

---

# H13 - Como usuário, quero visualizar o histórico das denúncias que fiz, com status e respostas, para que eu saiba se estou gerando impacto e possa acompanhar o andamento das ações

| Caso de teste | Classes de equivalência       | Entradas                                                 | Resultado esperado                                                     |
|---------------|-------------------------------|---------------------------------------------------------|-------------------------------------------------------------------------|
| Caso 1        | 1,4,7,10                     | Visualização do feedback, status, lista de denúncia e histórico correto | Denúncias visíveis com status e feedback corretos                       |
| Caso 2        | 2,4,7,10                     | Feedback ausente                                        | Falha ao exibir o feedback                                              |
| Caso 3        | 3,4,7,10                     | Feedback sem contexto ou incompleto                    | Feedback incompleto                                                     |
| Caso 4        | 1,5,7,10                     | Status não exibido                                      | Falha ao exibir status                                                  |
| Caso 5        | 1,6,7,10                     | Status exibido incorretamente                          | Status incorreto                                                        |
| Caso 6        | 1,4,8,10                     | Lista de denúncias vazia, apesar de existirem           | Falha ao apresentar a lista de denúncias                               |
| Caso 7        | 1,4,9,10                     | Lista exibe denúncias de outros usuários                | Falha ao exibir lista de denúncia, acesso indevido a denúncias alheias  |
| Caso 8        | 1,4,7,11                     | Denúncias com menos de 1 ano desaparecem                | Perda de denúncias dentro do prazo permitido                            |
| Caso 9        | 1,4,7,12                     | Denúncias com mais de 1 ano ainda aparecem              | Denúncias não removidas após 1 ano                                      |

---

# H14 - Como usuário, quero compartilhar as denúncias diretamente pelo aplicativo, para que mais pessoas tomem conhecimento e também se envolvam na causa.


| Caso de teste | Classes de equivalência       | Entradas                                                  | Resultado esperado                                              |
|---------------|-------------------------------|----------------------------------------------------------|------------------------------------------------------------------|
| Caso 1        | 1,4                           | Botão de compartilhar disponível em cada item de denúncia, link de compartilhamento disponível | Denúncia compartilhada com sucesso                              |
| Caso 2        | 2,4                           | Botão de compartilhar ausente nas denúncias              | Usuário não consegue compartilhar                                |
| Caso 3        | 3,4                           | Botão aparece mas não executa nenhuma função             | Falha de interação                                               |
| Caso 4        | 1,5                           | Link exige login para visualizar                         | Restrição incorreta de acesso                                    |
| Caso 5        | 1,6                           | Link gera erro ou redireciona incorretamente             | Falha no link, o conteúdo não pode ser compartilhado             |

---

# H16 - Como usuário, quero visualizar um feed de denúncias próximas à minha localização atual para me manter informado sobre problemas ambientais na minha região.

| Caso de teste | Classes de equivalência       | Entradas                                                    | Resultado esperado                                             |
|---------------|-------------------------------|------------------------------------------------------------|-----------------------------------------------------------------|
| Caso 1        | 1,4,7,10,13,16,19            | Todas as funcionalidades válidas e elementos corretamente exibidos | Feed personalizado com base na localização atual e dados exibidos corretamente |
| Caso 2        | 2,4,7,10,13,16,19            | Permissão negada para localização                           | Feed não é exibido por falta de permissão                      |
| Caso 3        | 3,4,7,10,13,16,19            | Localização incorreta                                       | Feed exibido com base em local incorreto                       |
| Caso 4        | 1,5,7,10,13,16,19            | Botão de alternância ausente                                | Não é possível alternar entre ordenações de feed               |
| Caso 5        | 1,6,7,10,13,16,19            | Ordenação incorreta                                         | Itens não são exibidos conforme ordenação selecionada          |
| Caso 6        | 1,4,8,10,13,16,19            | Exibição de dados pessoais                                  | Informações sensíveis estão sendo mostradas indevidamente      |
| Caso 7        | 1,4,9,10,13,16,19            | Imagens ou textos com informações sensíveis                 | Elementos não filtrados estão aparecendo no feed               |
| Caso 8        | 1,4,7,11,13,16,19            | Mensagem genérica ao não encontrar denúncias                | O sistema falha pois não orienta adequadamente o usuário       |
| Caso 9        | 1,4,7,12,13,16,19            | App trava ou gera erros ao não encontrar denúncias          | O aplicativo não trata corretamente o estado de ausência de dados |
| Caso 10       | 1,4,7,10,14,16,19            | Miniatura ausente                                           | A imagem principal da denúncia não é exibida                  |
| Caso 11       | 1,4,7,10,15,16,19            | Imagem errada ou de outra denúncia                          | A imagem exibida não corresponde à denúncia correta            |
| Caso 12       | 1,4,7,10,13,17,19            | Ajuste permitido para raio maior que 20 km                  | O alcance de visualização ultrapassa o limite previsto         |
| Caso 13       | 1,4,7,10,13,18,19            | Raio de visualização sem possibilidade de ajuste            | Não é possível alterar a distância do filtro                  |
| Caso 14       | 1,4,7,10,13,16,20            | Um ou mais dados obrigatórios ausentes                      | Elementos como tipo, distância ou horário estão faltando       |
| Caso 15       | 1,4,7,10,13,16,21            | Dados trocados entre denúncias                              | Informações estão sendo exibidas de forma incorreta ou embaralhada |
<br>
<br>
