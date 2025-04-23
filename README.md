# Caso-de-Uso-Sistema-de-Gerenciamento-de-Biblioteca
Análise de Violações de SOLID e Refatoração

Violações Identificadas
Violação do Princípio da Responsabilidade Única (SRP)

A classe GerenciadorBiblioteca estava manipulando muitas responsabilidades, incluindo a gestão de livros, usuários e notificações, o que viola o SRP. Dividimos essas responsabilidades em classes separadas para cada tarefa.

Violação do Princípio de Inversão de Dependência (DIP)

GerenciadorBiblioteca dependia diretamente de implementações concretas para notificações (ex: NotificadorEmail). Refatoramos para que o GerenciadorBiblioteca dependa de uma abstração (interface INotificador), permitindo maior flexibilidade e testabilidade.

Violação do Princípio da Segregação de Interface (ISP)

Havia interfaces que continham métodos que não eram usados por todas as classes que as implementavam. Refatoramos essas interfaces para que cada classe implementasse apenas os métodos necessários.

Violação do Princípio da Abertura/Fechamento (OCP)

O código não estava bem preparado para extensões sem modificações. Ao criar interfaces e separando as responsabilidades, garantimos que novas funcionalidades possam ser adicionadas sem modificar o código existente.

Refatorações Realizadas
Divisão de responsabilidades: Criamos novas classes para responsabilidades específicas, como GerenciadorLivros, GerenciadorUsuarios e NotificadorEmail.

Aplicação do DIP: Implementação da interface INotificador para desacoplar a classe GerenciadorBiblioteca das implementações concretas de notificação.

Melhorias em Clean Code: Renomeação de variáveis e métodos para nomes mais claros e a redução de métodos longos.
