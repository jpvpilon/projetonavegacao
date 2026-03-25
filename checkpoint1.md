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

