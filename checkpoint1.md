Primeiro commit - Passagem de parâmetros obrigatórios na tela de Perfil:

Primeiramente em composable(route = "perfil/{nome}") é definido que para o perfil, precisará do parâmentro de "nome".

Em seguida, o navController.navigate("perfil/Fulano de Tal") preenche esse "vazio", fazendo o código levar essa informação
para a próxima etapa.

No it.arguments?.getString("nome") é onde o código pega o valor armazenado "Fulano de Tal" da variável nome.
Caso ele não encontre ele usa o "Usuário Genérico", pois Kotlin não pode ter nulo.

No final ele passa essa variável para o PerfilScreen em text = "PERFIL - $nome" exibindo o componente como texto na UI.

