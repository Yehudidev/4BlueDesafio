# 4BlueDesafio
Teste Realizado para determinar quantidade de Bugs e Prioridade em sua ação.

Q.A: Yehudi Souza
Sistema Utilizado: Windows 11
Máquina Utilizada: Notebook


Criação de Conta

001-Título: Criação de Conta - Validação de layout das caixas de texto

Background:
Dado que o usuário acessa a tela de criação de conta

Cenário: Caixas de texto TELEFONE e CONFIRMAR SENHA estouradas à direita
Dado que a tela de "CriaçãoDeConta" foi incluída
Quando o sistema exibe as caixas de texto do formulário
E os campos "TELEFONE" e "CONFIRMAR SENHA" são apresentados ao usuário
Então as caixas de texto não devem ultrapassar o limite direito da tela
E ambos devem permanecer totalmente visíveis dentro do contêiner da página 

Link: https://drive.google.com/file/d/1aJ_8kkr9g_1ERo5VWu-_EM03cBfkb_ez/view?usp=drive_link
Severidade: Baixa 
—------------------------------------------------------
002-Título: Criação de Conta - Validação das caixas de texto

Background:
Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: Usuário inverte as informações de NOME COMPLETO e TELEFONE
Dado que o usuário está preenchendo o formulário de criação de conta
Quando o usuário insere um número de telefone no campo "NOME COMPLETO"
E insere um nome no campo "TELEFONE"
Então o sistema aceita o formulário
E a conta é criada com os dados informados 

Link:https://drive.google.com/file/d/1s34tIVYHPYKI9uBV7ViWLkLNacJ5PnFE/view?usp=drive_link
Severidade: Alta

—----------------------------------------------------

003-Título: Criação de Conta - Validação das informações inseridas anteriormente

Background:Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: O usuário utiliza o email já cadastrado anteriormente e o formulário é aceito
Dado que já existe uma conta cadastrada com determinado email
Quando o usuário preenche o formulário de criação de conta utilizando o mesmo email
E envia o formulário
Então o sistema aceita o formulário
E cria uma nova conta com o email já existente 

Link:https://drive.google.com/file/d/1s34tIVYHPYKI9uBV7ViWLkLNacJ5PnFE/view?usp=drive_link
Severidade: Alta
—----------------------------------------------------------------

004-Título: Criação de Conta - Validação das informações caixas de texto FONE

Background:
Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: Usuário digita telefone incompleto
Dado que o usuário está preenchendo o formulário de criação de conta
Quando o usuário digita telefone incompleto no campo "TELEFONE"
E envia o formulário
Então o sistema aceita o formulário
E a conta é criada com o telefone em formato inválido 


Link: https://drive.google.com/file/d/1Jwj7ZWoaz1ddF2Gpu-JC5MvSKGBlsjGf/view?usp=drive_link
Severidade: Média
—---------------------------------------------------------

005-Título: Criação de Conta - Validação das informações caixas de texto EMAIL

Background:
Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: Usuário digita email inexistente e em inconformidade de padrão
Dado que o usuário está preenchendo o formulário de criação de conta
Quando o usuário digita um email em formato inválido no campo "EMAIL"
E envia o formulário
Então o sistema aceita o formulário
E a conta é criada com o email em formato inválido 


Link: https://drive.google.com/file/d/1Jwj7ZWoaz1ddF2Gpu-JC5MvSKGBlsjGf/view?usp=drive_link
Severidade: Média
—---------------------------------------------------

006-Título: Criação de Conta - Validação das informações caixas de texto SENHA

Background: Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: Usuário digita senha com menos caracteres do que o permitido
Dado que o usuário está preenchendo o formulário de criação de conta
Quando o usuário digita uma senha com quantidade de caracteres menor que o mínimo exigido
E envia o formulário
Então o sistema aceita o formulário
E a conta é criada com a senha inválida


Link: https://drive.google.com/file/d/1Jwj7ZWoaz1ddF2Gpu-JC5MvSKGBlsjGf/view?usp=drive_link
Severidade para o usuário: Crítica
—---------------------------------------------------------

007-Título: Criação de Conta - Validação das informações caixas de texto NOME COMPLETO

Background:
Dado que o usuário acessa a tela de "CriaçãoDeConta"

Cenário: Usuário digita apenas o primeiro nome
Dado que o usuário está preenchendo o formulário de criação de conta
Quando o usuário digita apenas o primeiro nome no campo "NOME COMPLETO"
E envia o formulário
Então o sistema aceita o formulário
E a conta é criada apenas com o primeiro nome 

Link: https://drive.google.com/file/d/1Jwj7ZWoaz1ddF2Gpu-JC5MvSKGBlsjGf/view?usp=drive_link
Severidade para o usuário: Média
—--------------------------------------------------

Tela de Login 

008-TÍtulo:Login - Validação Login Cadastro Falho

Background:
Dado que o usuário acessa a tela de "Login" 

Cenário: Usuário digita email cadastrado de forma irregular e senha com menos caracteres e o acesso é permitido
Dado que existe um email cadastrado no sistema em formato irregular
Quando o usuário digita esse email no campo "EMAIL"
E digita uma senha com quantidade de menor que o mínimo permitido
E envia o formulário de login
Então o sistema aceita o algoritmo
E o usuário é direcionado para a próxima tela 

Link: https://drive.google.com/file/d/1fCOxRFw5K0jG3sVuMmR1Q05gVRLBizZp/view?usp=drive_link
Severidade para o usuário: Crítica
—--------------------------------------------------------
TELA DE SUCESSO

009-Título: Tela de Sucesso - Validação de comportamento após login

Background:
Dado que o usuário acessa a tela de "Login" 

Cenário: Usuário realiza login com credenciais válidas e erro é apresentado na tela de sucesso
Dado que existe um usuário cadastrado no sistema
Quando o usuário digita um email cadastrado no campo "EMAIL"
E digita a senha correta no campo "SENHA"
E envia o formulário de login
Então o sistema aceita o formulário
E o usuário é direcionado para a "TelaDeSucesso"
E é apresentado um erro no canto inferior direito da tela 

Link: https://drive.google.com/file/d/1HvGxjrrgtBMPGN05C20IDj2HAPNW9jqr/view?usp=drive_link
Severidade: Média

—---------------------------------------------------------

Principais Correções

006-Título: Criação de Conta - Validação das informações caixas de texto SENHA

Este bug deve ser tratado com prioridade, pois impacta diretamente a segurança do sistema. Além de não estar em conformidade com as normas previstas anteriormente pelo desenvolvedor, a falha pode comprometer a proteção e o acesso seguro às informações.

008-TÍtulo:Login - Validação Login Cadastro Falho

Este bug está relacionado ao problema identificado no processo de criação de conta. Mesmo quando as informações de e-mail e senha estão em desacordo com os critérios definidos, o sistema ainda permite a realização de login. Como consequência, essa falha pode comprometer a segurança da aplicação, tornando-a mais vulnerável.

Obs: Com relação ao que eu mudaria, acho que nada muito substâncial.
A cor e o design estão bem marcantes quanto a proposta, além de estarem de acordo com a conformidade da empresa.
No geral, seria apenas as correções relacionadas ao Banco de Dados e bugs relacionados a segurança.
