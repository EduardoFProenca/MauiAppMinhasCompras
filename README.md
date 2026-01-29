# 🛒MauiAppMinhasCompras

Aplicativo de lista de compras desenvolvido em .NET MAUI para gerenciamento de produtos e cálculo de gastos.

## 📱 Sobre o Projeto

Este é um aplicativo mobile multiplataforma desenvolvido como atividade prática para a ETEC. O app permite criar, visualizar, editar e remover produtos de uma lista de compras, além de calcular automaticamente o valor total baseado na quantidade e preço unitário de cada item.

### 📚 Informações Acadêmicas

- **Disciplina**: Desenvolvimento de Sistemas III
- **Atividade**: AulaAgenda 06 - Avaliação DS_3
- **Professor**: Thiago Henrique Neto
- **Data da Avaliação**: 14/10/2025
- **Menção**: MB (Muito Bom)

**Feedback do Professor:**
> "Eduardo, Você implementou o desafio 1 de forma adequada, adicionando o atributo categoria à classe do produto e realizando as adequações necessárias nas Views. At.te"

## 📸 Screenshots

*(Adicione aqui capturas de tela do aplicativo quando disponíveis)*

## ✨ Funcionalidades

- **Gerenciamento Completo de Produtos**: Adicione, edite, visualize e remova produtos da lista
- **Busca Inteligente**: Sistema de pesquisa por descrição de produtos
- **Cálculo Automático**: Total calculado automaticamente (quantidade × preço)
- **Soma Total**: Visualize o valor total de todas as compras
- **Categorização**: Organize produtos por categorias personalizadas
- **Persistência de Dados**: Todos os dados salvos localmente com SQLite

## 🏗️ Estrutura do Projeto

```
MauiAppMinhasCompras/
├── Models/
│   └── Produto.cs              # Modelo de dados com categoria
├── Views/
│   ├── ListaProduto.xaml       # Tela principal com lista
│   ├── NovoProduto.xaml        # Tela para adicionar produto
│   └── EditarProduto.xaml      # Tela para editar produto
├── Helpers/
│   └── SQLiteDatabaseHelper.cs # Helper para operações no BD
├── Resources/
│   ├── Fonts/                  # Fontes customizadas
│   ├── Images/                 # Imagens e ícones
│   └── Styles/                 # Estilos e cores
├── App.xaml                    # Configurações globais
└── AppShell.xaml               # Navegação shell
```

## 🛠️ Tecnologias Utilizadas

- **.NET 9.0**
- **.NET MAUI** (Multi-platform App UI)
- **SQLite** (sqlite-net-pcl 1.9.172)
- **XAML** para interfaces
- **C#** para lógica de negócio
- **Visual Studio 2022**

## 📱 Plataformas Suportadas

- ✅ Android (API 21+)
- ✅ iOS (15.0+)
- ✅ Windows (10.0.17763.0+)
- ✅ MacCatalyst (15.0+)

## 💾 Banco de Dados

O aplicativo utiliza SQLite para armazenamento local dos dados. O banco é criado automaticamente no primeiro uso e armazena:

| Campo      | Tipo    | Descrição                          |
|------------|---------|-------------------------------------|
| Id         | Integer | Chave primária (autoincremento)    |
| Descricao  | String  | Nome/descrição do produto          |
| Quantidade | Double  | Quantidade do produto              |
| Preco      | Double  | Valor unitário                     |
| Total      | Double  | Valor total (calculado automaticamente) |

## 🚀 Como Executar

### Pré-requisitos

- Visual Studio 2022 (versão 17.14 ou superior)
- .NET 9.0 SDK
- Workload do .NET MAUI instalado

### Passos para Execução

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/MauiAppMinhasCompras.git
```

2. **Abra o projeto**
```bash
cd MauiAppMinhasCompras
```

3. **Abra a solução no Visual Studio**
```bash
start MauiAppMinhasCompras.sln
```

4. **Selecione a plataforma de destino** (Android, iOS, Windows, etc.)

5. **Execute o projeto** (F5)

## 🎯 Casos de Uso

### Adicionar Produto
1. Clique em **"Adicionar"** na barra superior
2. Preencha os campos:
   - Descrição do produto
   - Quantidade
   - Preço unitário
3. Clique em **"Salvar"**
4. O produto será adicionado à lista automaticamente

### Editar Produto
1. **Toque** em um produto da lista
2. Modifique os campos desejados
3. Clique em **"Salvar"**
4. As alterações serão salvas imediatamente

### Remover Produto
1. **Deslize** o produto para o lado (ou toque e segure)
2. Selecione **"Remover"**
3. O produto será excluído da lista

### Buscar Produto
1. Digite o termo na **barra de busca** no topo da tela
2. A lista será **filtrada automaticamente** conforme você digita
3. Limpe o campo para ver todos os produtos novamente

### Calcular Total Geral
1. Clique em **"Somar"** na barra superior
2. O sistema exibirá o **valor total** de todos os produtos cadastrados
3. O cálculo considera quantidade × preço de cada item

## 📐 Características Técnicas

### Validações Implementadas

- ✅ Descrição do produto é obrigatória
- ✅ Quantidade deve ser um número válido
- ✅ Preço deve ser um número válido
- ✅ Tratamento de erros com mensagens amigáveis
- ✅ Validação de campos vazios

### Operações do Banco de Dados

- **Insert**: Adiciona novo produto ao banco
- **Update**: Atualiza produto existente
- **Delete**: Remove produto do banco
- **GetAll**: Lista todos os produtos
- **Search**: Busca produtos por descrição

## 🏆 Desafios Implementados

### Desafio 1 - Categorização de Produtos ✅
Implementação do atributo **categoria** na classe Produto, com as devidas adequações nas Views para permitir a classificação dos produtos em diferentes categorias (ex: Alimentos, Limpeza, Higiene, etc.).

## 🎨 Design e Interface

O aplicativo utiliza temas adaptativos:
- **Modo Claro**: Interface limpa e moderna
- **Modo Escuro**: Adaptação automática às preferências do sistema
- **Layout Responsivo**: Funciona perfeitamente em diferentes tamanhos de tela
- **Grid System**: Organização em colunas para melhor visualização dos dados

### 🌟 Destaques da Interface

- Interface intuitiva e fácil de usar
- Lista organizada em formato de tabela
- Ações rápidas de contexto (remover)
- Feedback visual em todas as operações
- Barra de busca sempre acessível

## ✅ Qualidade e Testes

O projeto foi desenvolvido com foco em qualidade de código e funcionalidade:
- ✅ **Desafio 1 implementado adequadamente** (validado pelo professor)
- ✅ Tratamento de exceções em todas as operações
- ✅ Validações de dados de entrada
- ✅ Interface responsiva e adaptável
- ✅ Código limpo e bem estruturado
- ✅ Uso correto do padrão MVVM

---

<div align="center">

**Desenvolvido com 💙 por Eduardo Ferreira Proença**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eduardo-ferreira-39106b26a)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/EduardoFProenca)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:eduardo.ferreira.proenca.brasil@gmail.com)

⭐ **Se este repositório foi útil, considere dar uma estrela!** ⭐

**ETEC - Desenvolvimento de Sistemas III - 2025**

</div>
