# 📚 BookClub — Plataforma de Gestão Literária e Comunidade de Leitura

> **Atividade Prática – Desenvolvimento de Aplicação Web**  
> Aplicação dos conceitos de front-end e operações fundamentais de CRUD utilizando o `LocalStorage` do navegador para persistência de dados.

---

## 📖 1. Visão Geral do Projeto

O **BookClub** é uma aplicação web funcional e interativa concebida para incentivar hábitos de leitura, catalogação de obras e engajamento em comunidades literárias. 

O projeto conecta diretamente o modelo conceitual desenvolvido na disciplina de **Banco de Dados** com a disciplina de **Desenvolvimento Web**, demonstrando na prática o ciclo de vida completo da informação no ambiente de front-end.

---

## 🎯 2. Objetivos Acadêmicos

* **Operações CRUD Completas**: Implementar de forma 100% funcional as 4 operações fundamentais para cada entidade:
  * **C (Create)**: Cadastro de novos registros via formulários validados;
  * **R (Read)**: Consulta e listagem dinâmica dos registros em tabela;
  * **U (Update)**: Edição e atualização de registros existentes;
  * **D (Delete)**: Exclusão controlada de registros.
* **Persistência Client-Side com LocalStorage**:
  * Utilização de listas de objetos em JavaScript;
  * Serialização com `JSON.stringify()` e armazenamento via `localStorage.setItem()`;
  * Recuperação via `localStorage.getItem()` e conversão com `JSON.parse()`.
* **Organização e Domínio**: Cada integrante do grupo é responsável por um CRUD completo, demonstrando domínio total do código para a banca.
* **Interface Amigável e Responsiva**: Construída com **Bootstrap 5**, proporcionando clareza visual, facilidade de uso e elegância sem complexidade desnecessária.

---

## 👥 3. Divisão dos Módulos (1 Integrante = 1 CRUD)

| Módulo / CRUD | Entidade | Responsável | Nível | Descrição |
| :--- | :---: | :---: | :---: | :--- |
| **1. Gêneros Literários** | `GENERO` | *[Nome do Aluno 1]* | 🟢 Muito Fácil | Cadastro e categorização de gêneros (Fantasia, Ficção, Romance, etc.). |
| **2. Leitores (Usuários)** | `USUARIO` | *[Nome do Aluno 2]* | 🟡 Fácil | Gestão de perfis de leitores, e-mails e metas anuais de leitura. |
| **3. Catálogo de Livros** | `LIVRO` | *[Nome do Aluno 3]* | 🟠 Médio | Gerenciamento de acervo com título, autor, gênero, páginas e ano de publicação. |
| **4. Clubes de Leitura** | `CLUBE` | *[Nome do Aluno 4]* | 🔵 Médio+ | Administração de círculos literários, capacidade de membros e status de atividade. |
| **5. Avaliações & Resenhas**| `RESENHA` | *[Nome do Aluno 5]* | 🔴 Desafiador | Publicação de resenhas críticas, notas avaliativas (1 a 5) e recomendações. |

---

## 🏆 4. Tierlist de Complexidade dos CRUDs

```
[MUITO FÁCIL]      🟢 1. CRUD de Gêneros Literários
[FÁCIL]            🟡 2. CRUD de Leitores (Usuários)
[MÉDIO]            🟠 3. CRUD de Livros
[MÉDIO +]          🔵 4. CRUD de Clubes de Leitura
[DESAFIADOR]       🔴 5. CRUD de Avaliações / Resenhas
```

### Detalhamento por Módulo

#### 🟢 Módulo 1: Gêneros Literários (`GENERO`)
* **Campos**: `id`, `nome`, `descricao`
* **Características**: Entidade independente, foco em campos textuais básicos. Ideal para validação direta e código conciso.

#### 🟡 Módulo 2: Leitores / Usuários (`USUARIO`)
* **Campos**: `id`, `nome`, `email`, `meta_leitura`
* **Características**: Validação de formato de e-mail e campo numérico inteiro para a meta de leitura.

#### 🟠 Módulo 3: Catálogo de Livros (`LIVRO`)
* **Campos**: `id`, `titulo`, `autor`, `genero`, `paginas`, `ano`
* **Características**: Volume maior de atributos, conversão numérica (`parseInt`) para páginas e ano, e exibição em tabela estruturada.

#### 🔵 Módulo 4: Clubes de Leitura (`CLUBE`)
* **Campos**: `id`, `nome_clube`, `tema`, `capacidade_max`, `status` (Ativo/Em Pausa/Encerrado), `data_criacao`
* **Características**: Manipulação de campos de data (`input type="date"`), seleção com `<select>` e badges visuais de status.

#### 🔴 Módulo 5: Avaliações & Resenhas (`RESENHA`)
* **Campos**: `id`, `livro`, `leitor`, `nota` (1 a 5), `texto_resenha`, `recomenda` (Sim/Não)
* **Características**: Integração lógica com os livros cadastrados, validação de intervalo numérico de notas e controle booleano/checkbox.

---

## 💻 5. Tecnologias Utilizadas

* **HTML5**: Estruturação semântica das páginas e formulários;
* **CSS3**: Estilização complementar e refinamentos de layout;
* **Bootstrap 5**: Framework CSS para componentes (Navbar, Modais, Cards, Tabelas e Grid responsivo);
* **JavaScript (ES6+) Nativo**: Lógica de manipulação de DOM, eventos e persistência via LocalStorage, sem frameworks pesados.

---

## 📂 6. Estrutura Padrão de Funções (Didático)

Para manter a clareza e facilitar a explicação de cada aluno perante o professor, todos os módulos seguem uma convenção uniforme de funções:

```javascript
// Exemplo conceitual adotado em todos os CRUDs
function carregarDados() { ... }     // getItem() + JSON.parse()
function salvarDados(lista) { ... }  // JSON.stringify() + setItem()
function cadastrarRegistro() { ... } // Create
function listarRegistros() { ... }   // Read
function editarRegistro(id) { ... }  // Update
function excluirRegistro(id) { ... } // Delete
```

---

## 🚀 7. Como Executar a Aplicação

1. Clone ou baixe este repositório.
2. Abra a pasta do projeto.
3. Abra o arquivo `index.html` diretamente em qualquer navegador web moderno (Google Chrome, Firefox, Microsoft Edge).
4. **Dica de Teste**: Para verificar o funcionamento do `LocalStorage` do zero, teste em uma janela anônima ou limpe os dados do navegador através do DevTools (`F12` > *Application* > *Local Storage*).

---

## 📋 8. Checklist de Avaliação

- [ ] CRUD 1 (Gêneros Literários) funcional (Criar, Listar, Editar, Excluir)
- [ ] CRUD 2 (Leitores) funcional (Criar, Listar, Editar, Excluir)
- [ ] CRUD 3 (Livros) funcional (Criar, Listar, Editar, Excluir)
- [ ] CRUD 4 (Clubes de Leitura) funcional (Criar, Listar, Editar, Excluir)
- [ ] CRUD 5 (Resenhas & Avaliações) funcional (Criar, Listar, Editar, Excluir)
- [ ] Persistência via `LocalStorage` validada
- [ ] Utilização correta de `JSON.stringify()` e `JSON.parse()`
- [ ] Interface responsiva e limpa com Bootstrap 5
- [ ] Ausência de dependência de login ou tecnologias não ministradas em aula
