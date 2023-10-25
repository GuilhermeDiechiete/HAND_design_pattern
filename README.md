# HAND Design Pattern
O objetivo desse Padrão de Design é separar as 'Pastas' ou 'Arquivos' cada vez que precisamos pegar algo ou devolver algo. Podemos usar o nome desse padrão para demostrar como ele foi pensado.

## HAND - ( MÃO )
Vamos criar um cenário de uma oficina mecanica. Nessa oficina nos temos os seguintes integrantes. Os atendentes(controllers), responsaveis por receber o veiculo(requisição) do cliente.
Temos o mecanicos(Handlings) que fazem a manipulação necessaria no veiculo, como alterar peças, apos isso, o mecanico vai devolver o veiculo com alguma resposta e então o atendente vai devolver o veiculo com a resposta. 

Esse exemplo resume esse Padrão de Design, agora vamos para a organização em si do projeto, vou falar sobre a arquitetura e dar um exemplo, OK!.

## Organização 

### Routes
A pasta <strong> routes </strong> é responsavel por conter todas as rotas para os controllers.

- Exemplo: Seria o caminho que o cliente pegou até chegar no balcão de atendentes da oficina.

A pasta <strong> controllers </strong> é responsavel por pegar a requisição, direcionar para um handling e enviar a resposta para o usuário depois de manipulada.

- Exemplo: Seria o atendente pegando o veiculo e mandando para o mecanico, apos a manipulação do veiculo, devolve a resposta ao cliente.

A pasta <strong> handlings </strong> é responsavel pela manipulação dos dados, como, alterar dados, validar, CRUD (no banco de dados).
- Exemplo: É o mecanico manipulando o veiculo do cliente.
  
A pasta <strong> fragments </strong> é responsavel por conter pedações de codigos necessarios para fazer a manipulação, como criptografar senhas, gerar tokens, formatar a mensagem.

- Exemplo: Sim, temos essa pasta que não foi mencionada la no inicio, essa pasta é tudo para o mecanico, sim, é a maleta de ferramentas, nessa pasta contem todas as cheves necessarias para o mecanico efetuar a manipulação no veiculo.

A pasta <strong> access </strong> responsavel por conter todo o CRUD do projeto, como buscar dados, salvar, alterar e excluir.

- Exemplo: Essa pasta seria o manual do mecanico, onde ele busca e guarda informações do veiculo.

## Agora cada a palavra mão que foi mencionada? Não foi dita até aqui.

Agora quando você for fazer um projeto, imagine o handling (mecanico) trabalhando, como assim? Imagina ele na oficina pegando varias coisas da caixa de ferramenta toda hora, indo no manual conferir dados e alterar, você percebeu que tudo que ele faz, ele está fazendo com as mãos, agora imagina os handlings com mãos pegando tudo o que é necessario para entregar a resposta para o cliente.

