Primeiro commit - Passagem de parâmetros obrigatórios na tela de Perfil:

Primeiramente em composable(route = "perfil/{nome}") é definido que para o perfil, precisará do parâmentro de "nome".

Em seguida, o navController.navigate("perfil/Fulano de Tal") preenche esse "vazio", fazendo o código levar essa informação
para a próxima etapa.

No it.arguments?.getString("nome") é onde o código pega o valor armazenado "Fulano de Tal" da variável nome.
Caso ele não encontre ele usa o "Usuário Genérico", pois Kotlin não pode ter nulo.

No final ele passa essa variável para o PerfilScreen em text = "PERFIL - $nome" exibindo o componente como texto na UI.

Segundo commit: Passagem de parâmetros opcionais na tela de Pedidos

Diferente do anterior, agora é passado para o Pedidos o campo opcional de cliente, diferente do nome que era obrigatório.
Mais um ponto diferene do anterior, é que está definido o valor default direto no navArgument de forma explicita.

Aqui em it.arguments?.getString("cliente") quando o código é executado, ele verifica se tem algo armazenado na variável, se tiver ele usa,
caso não tenha ele usa o default.

Terceiro commit: Inserindo valor ao parâmetro opcional na tela de Pedidos

Nesse commit, colocamos no onClick o envio do parâmetro opcional, mostrando o que estiver inserido no valor. Caso não houvesse nada, viria o valor
default, como tem, ele exibirá o "CLIENTE XPTO" no click.

Quarto commit: Passagem de múltiplos parâmetros

Aqui, atualizamos os parâmetros do Perfil, agora também sendo obrigatório além do nome, a idade, devendo ser inseridos na ordem correta nome -> idade.
No OnClick ele aparece agora com o parâmetro da idade também, obrigatóriamente depois do nome. E colocando o NavType, usando a lista, sinalizamos o tipo da variável
como inteiro. Por fim, no perfil screen passamos os parâmetros novamente. No final a tela irá exibir tudo que for inserido, com todos os parâmetros, pois são obrigatórios.

Em resumo, todos esses commits serviram para adicionar parâmetros, obrigatórios como "nome" e "idade", ou opcionais como "cliente", fazendo assim, a navegação ficar mais completa e exibir todos os dados que quisermos.
