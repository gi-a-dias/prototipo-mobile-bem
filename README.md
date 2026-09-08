# HABIT — Protótipo Mobile (BEM CSS)

## Integrantes do Grupo
* **Giovanna Almeida Dias** - RA: 10436553
* **Lucas Masteguim** - RA: 10437300

## 📝 Descrição da Aplicação
O **HABIT** é uma plataforma moderna de publicação e consumo de conteúdo focada no cultivo de hábitos saudáveis e produtividade, organizada de forma semântica por categorias.

* **Área Pública:** Permite que leitores naveguem de forma responsiva por categorias populares, leiam postagens em destaque, visualizem as escolhas do editor, realizem buscas textuais e assinem a newsletter.
* **Área de Autenticação:** Permite que usuários se cadastrem, façam login e gerenciem seus perfis individuais com histórico de publicações e comentários.
* **Área Administrativa:** Permite o controle gerencial de categorias, criação e edição de novas postagens, moderação de comentários e fila de revisão de novos posts antes de serem publicados.

---

## 📱 Fluxo de Navegação e Telas
Nossa proposta mobile reorganizou os elementos das 14 telas originais para garantir uma excelente área de toque e leitura em dispositivos móveis.

| Tela | Nome da Tela | Fluxo | Arquivo na Pasta /wireframes |
| :---: | :--- | :--- | :--- |
| **01** | Início (Home) | Público | `tela_01_inicio.png` |
| **02** | Categoria | Público | `tela_02_categoria.png` |
| **03** | Destaques | Público | `tela_03_destaques.png` |
| **04** | Assinar Newsletter | Público | `tela_04_newsletter.png` |
| **05** | Admin · Categorias | Administrativo | `tela_05_admin_categorias.png` |
| **06** | Admin · Criar Post | Administrativo | `tela_06_admin_criar_post.png` |
| **07** | Admin · Escolhas do Editor | Administrativo | `tela_07_admin_escolhas_editor.png` |
| **08** | Admin · Usuários | Administrativo | `tela_08_admin_usuarios.png` |
| **09** | Admin · Fila de Revisão | Administrativo | `tela_09_admin_fila_revisao.png` |
| **10** | Admin · Fila de Comentários | Administrativo | `tela_10_admin_fila_comentarios.png` |
| **11** | Resultado da Busca | Público | `tela_11_resultados_busca.png` |
| **12** | Entrar (Login) | Autenticação | `tela_12_entrar.png` |
| **13** | Criar Conta | Autenticação | `tela_13_criar_conta.png` |
| **14** | Perfil do Usuário | Autenticação | `tela_14_perfil.png` |

### 🔄 Fluxos Principais
* **Fluxo Público:** `Tela 01` → `Tela 02` / `Tela 03` / `Tela 04` / `Tela 11`
* **Fluxo de Autenticação:** `Tela 12` → `Tela 13` → `Tela 14`
* **Fluxo Administrativo:** `Telas 05 a 10`
* **Fluxo de Publicação:** `Tela 06` → `Tela 09` → aprovação → publicação

---

## 🛠️ Identificação dos Componentes e Variações BEM
Todos os elementos de estilo foram estruturados utilizando a metodologia do **BEM** (Block__Element--Modifier):

| Componente (Block) | Onde Aparece | Elementos (`__`) | Variações / Modificadores (`--`) |
| :--- | :--- | :--- | :--- |
| **`button`** | Login, Cadastro, Newsletter, Criar Post, Fila de Revisão, Categorias | `button__text`, `button__icon` | `button--primary`, `button--secondary`, `button--disabled`, `button--danger` |
| **`card`** | Início, Categoria, Destaques, Resultados de Busca, Perfil | `card__image`, `card__title`, `card__category`, `card__date` | `card--large`, `card--medium`, `card--compact` |
| **`form`** | Início, Cadastro, Criar Post, Categorias (Busca), Perfil | `form__group`, `form__label`, `form__input`, `form__button` | `form__input--error`, `form__input--focused`, `form__input--disabled` |
| **`navigation`** | Header, Bottom Nav ou Sidebar do Admin | `navigation__list`, `navigation__item`, `navigation__link`, `navigation__icon` | `navigation__item--active`, `navigation--button`, `navigation--sidebar` |
| **`chip`** | Categoria (02), Destaques (03) | — | `chip--selected` |

---

## 📂 Organização dos Arquivos
Seguindo as orientações da disciplina, estruturamos os materiais do projeto de forma limpa e modularizada:

```text
projeto-mobile/
├── wireframes/              # Contém as 14 imagens PNG de baixa fidelidade
├── css/                     # Arquivos CSS separados por responsabilidade
│   ├── variables.css        # Centraliza os Design Tokens (cores, raios e bordas)
│   ├── button.css           # Estilos do bloco .button e suas variações BEM
│   ├── card.css             # Estilos do bloco .card (padrão, compact e featured)
│   ├── form.css             # Estilos dos campos de texto e agrupadores .form
│   ├── navigation.css       # Estilos das barras de navegação superior e inferior
│   └── device.css           # Simulador utilitário de dispositivo móvel para testes
├── html.html                # Arquivo HTML de teste unificado da aplicação
└── README.md                # Documentação técnica do projeto
```
```
