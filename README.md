# Como foi decidido a User Story
A User Story foi criada de acordo com o sistema disponibilizado no link https://creative-sherbet-a51eac.netlify.app/, levando em conta 
o ponto de vista de um usuário do sistema e os botões aos quais ele tem acesso, bem como os formulários que ele pode preencher, e o 
fluxo de telas pelas quais ele pode passar. Também foi considerado a implementação e estado atual do sistema.

# User Story
**Como**
	Usuário do módulo de curso do Beedoo

**Eu quero**
	Gerenciar os cursos do módulo

**Para**
	Poder visualizar, cadastrar e excluir cursos do sistema
	
	## Cenário 1: visualizar os cursos cadastrados no sistema
		**Dado**: que eu possua acesso ao módulo de curso do Beedoo;
		**Quando**: eu abrir a página inicial do sistema;
			**E**: houver pelo menos 1 curso cadastrado;
		**Então**: deverão ser exibidos os cursos em uma tabela na página inicial, cada item da tabela terá as seguintes informações:
		imagem de capa, tipo de curso, nome, instrutor, data de início, data de fim, quantidade de vagas e botão para excluir o curso.
		
	## Cenário 2: atualizar lista de cursos cadastrados no sistema
		**Dado**: que eu possua acesso ao módulo de curso do Beedoo;
			**E**: eu esteja em qualquer tela com acesso ao botão "Listar Cursos";
		**Quando**: eu clicar no botão "Listar Cursos";
		**Então**: eu serei redirecionado à página inicial do sistema;
			**E**: se houver pelo menos 1 curso cadastrado, ele será exibido conforme o Cenário 1.
			
	## Cenário 3: excluir curso do sistema com sucesso
		**Dado**: que eu esteja na página inicial do módulo de curso do Beedoo;
			**E**: exista pelo menos 1 curso cadastrado no sistema;
			**E**: eu tenho acesso ao botão "Excluir Curso";
		**Quando**: eu clicar no botão "Excluir Curso" de qualquer curso listado na página inicial;
		**Então**: o curso será excluído do sistema;
			**E**: um modal com o texto "Curso excluído com sucesso!" será exibido no topo da tela;
			**E**: a tabela de cursos será atualizada, removendo o curso excluído dela.
			
	## Cenário 4: acessar página de cadastro de cursos
		**Dado**: que eu possua acesso ao módulo de curso do Beedoo;
			**E**: eu esteja em qualquer tela com acesso ao botão "Cadastrar Curso";
		**Quando**: eu clicar no botão "Cadastrar Curso";
		**Então**: eu serei redirecionado à página "Cadastro de curso";
			**E**: serão exibidos os formulários de cadastro com preenchimento vazio e rótulos, tipo de formulário e regras conforme a
			seguinte ordem: Nome do curso (caixa de texto), Descrição do curso (caixa de texto), Instrutor (caixa de texto), Url da
			imagem de capa (caixa de texto), Data de início (seleção em calendário dd/mm/aaaa), Data de fim (seleção em calendário dd/mm/aaaa),
			Número de vagas (caixa de texto aceitando apenas números), Tipo de curso (lista: Presencial, Online), Endereço (caixa de texto,
			vísivel se o Tipo de curso for Presencial) e Link de inscrição (caixa de texto, vísivel se o Tipo de curso for Online)
			**E**: será exibido o botão "Cadastrar Curso" abaixo dos formulários.
	
	## Cenário 5: cadastrar curso com sucesso
		**Dado**: que eu possua acesso ao módulo de curso do Beedoo;
			**E**: eu esteja na página "Cadastro de curso";
			**E**: os formulários estejam preenchidos de acordo com suas regras;
		**Quando**: eu clicar no botão "Cadastrar Curso" abaixo dos formulários;
		**Então**: o sistema validará as regras dos campos;
			**E**: cadastrará o novo curso;
			**E**: eu serei redirecionado à página inicial do sistema;
			**E**: um modal com o texto "Curso cadastrado com sucesso!" será exibido no topo da tela;
			**E**: a tabela de cursos estará atualizada com o novo curso cadastrado.
			
	## Cenário 6: erro ao cadastrar curso
		**Dado**: que eu possua acesso ao módulo de curso do Beedoo;
			**E**: eu esteja na página "Cadastro de curso";
			**E**: os formulários não estejam preenchidos de acordo com suas regras;
		**Quando**: eu clicar no botão "Cadastrar Curso" abaixo dos formulários;
		**Então**: o sistema verificará que as regras dos campos não foram cumpridas;
			**E**: um modal com o texto "Erro ao cadastrar curso!" será exibido no topo da tela.