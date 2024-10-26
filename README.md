# Modelo Relacional de Universidade - Desafio DIO 🚀

Este projeto foi desenvolvido como parte de um desafio do bootcamp da [Digital Innovation One](https://www.dio.me/). O objetivo do desafio é recriar ou aprimorar um modelo relacional para um sistema acadêmico, utilizando **MySQL** para gerenciar os dados. O modelo apresentado aqui representa o sistema de uma Universidade, com foco nas relações entre alunos, professores, disciplinas e cursos.

## 📊 Estrutura do Modelo Relacional

![Modelo Relacional - Universidade](./desafioDIO-Modelo%20Relacional.png)

### Entidades Principais

1. **Aluno** (`aluno`)
   - Armazena dados dos alunos, como `idAluno`, `nome`, `idade`.
   - Relacionamento com a entidade `telefoneAluno`, para armazenar números de contato dos alunos.

2. **Professor** (`professor`)
   - Armazena dados dos professores, incluindo `idProfessor`, `nome`, `sexo`, `email`.
   - Relacionamento com `telefone_prof`, para registrar números de contato dos professores.

3. **Disciplina** (`disciplina`)
   - Contém informações das disciplinas oferecidas, como `idDisciplina`, `nomeDisci`, e a relação com `professor_idProfessor`, indicando o professor responsável.

4. **Curso** (`curso`)
   - Armazena os cursos da universidade, como `idcurso` e `nome`.
   - Relacionamento com a tabela `disciplina_curso`, que define as disciplinas oferecidas em cada curso.

5. **Departamento** (`departamento`)
   - Armazena informações dos departamentos, incluindo `idDepartamento`, `campus`, `nome`.

6. **Pré-Requisitos** (`preRequisitos`)
   - Define os pré-requisitos para uma disciplina, armazenando o `idpreRequisitos` e a relação com as disciplinas correspondentes.

### Tabelas de Relacionamento

- **Telefone do Aluno** (`telefoneAluno`)
  - Guarda os números de telefone dos alunos com base no `idtelefoneAluno`.

- **Telefone do Professor** (`telefone_prof`)
  - Guarda os números de telefone dos professores com base no `idtelefone_prof`.

- **Matriculado** (`matriculado`)
  - Tabela de relacionamento entre `aluno` e `disciplina`, indicando as disciplinas em que o aluno está matriculado, com as datas de início (`inicioMatricula`) e fim (`fimMatricula`).

- **Disciplina_Curso** (`disciplina_curso`)
  - Relaciona as disciplinas aos cursos que as incluem, especificando o número de alunos matriculados.

- **Pré-Requisitos de Disciplina** (`preRequisitos_disciplina`)
  - Define os pré-requisitos necessários para cursar determinadas disciplinas, com requisitos de `idade` e `renda`.

## 🛠️ Tecnologias Utilizadas

- **MySQL**: Banco de dados relacional utilizado para desenvolver e gerenciar o modelo.
- **MySQL Workbench**: Ferramenta para criação do modelo relacional e visualização das entidades.


