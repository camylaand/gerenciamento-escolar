# Banco de Dados Escolar – Desafio SQLiteOnline

## Contexto
Este desafio teve como objetivo criar e gerenciar um **banco de dados para uma escola**, utilizando SQL.  
O banco organiza informações sobre alunos, professores, disciplinas, turmas e notas, permitindo consultas e manipulação dos dados.

---

## Estrutura do Banco de Dados

### Tabela: Alunos
Armazena informações sobre os estudantes:
- `id_aluno` (INT, PK): identificador único do aluno.  
- `nome_aluno` (VARCHAR): nome completo do aluno.  
- `data_nascimento` (DATE): data de nascimento.  
- `genero` (VARCHAR): gênero do aluno.  
- `endereco` (VARCHAR): endereço residencial.  
- `telefone_contato` (VARCHAR): telefone de contato.  
- `email` (VARCHAR): e-mail do aluno.  

---

### Tabela: Professores
Armazena informações sobre os professores:
- `id_professor` (INT, PK): identificador único do professor.  
- `nome_professor` (VARCHAR): nome completo.  
- `data_nascimento` (DATE): data de nascimento.  
- `genero` (VARCHAR): gênero do professor.  
- `telefone_contato` (VARCHAR): telefone de contato.  
- `email` (VARCHAR): e-mail do professor.  

---

### Tabela: Disciplinas
Armazena informações das disciplinas:
- `id_disciplina` (INT, PK): identificador único da disciplina.  
- `nome_disciplina` (VARCHAR): nome da disciplina.  
- `descricao` (VARCHAR): descrição da disciplina.  
- `carga_horaria` (INT): carga horária da disciplina.  
- `id_professor` (INT, FK): referência ao professor que leciona a disciplina.  

---

### Tabela: Turmas
Registra turmas específicas:
- `id_turma` (INT, PK): identificador único da turma.  
- `nome_turma` (VARCHAR): nome ou código da turma.  
- `ano_letivo` (INT): ano letivo da turma.  
- `id_professor_orientador` (INT, FK): referência ao professor orientador da turma.  

---

### Tabela: Turma_Disciplinas
Relaciona turmas e disciplinas:
- `id_turma` (INT, FK)  
- `id_disciplina` (INT, FK)  
> Chave primária composta: `(id_turma, id_disciplina)`  

---

### Tabela: Turma_Alunos
Relaciona turmas e alunos:
- `id_turma` (INT, FK)  
- `id_aluno` (INT, FK)  
> Chave primária composta: `(id_turma, id_aluno)`  

---

### Tabela: Notas
Armazena notas dos alunos:
- `id_nota` (INT, PK): identificador único da nota.  
- `id_aluno` (INT, FK): referência ao aluno.  
- `id_disciplina` (INT, FK): referência à disciplina.  
- `valor_nota` (DECIMAL): nota atribuída.  
- `data_avaliacao` (DATE): data da avaliação.  

---

