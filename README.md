# **Protótipo Mobile do BEM**
## Estrutura para o repositório de trabalho

## Integrantes:
* Giovanna Almeida Dias - 10436553
* Lucas Masteguim - 10437300

## 📝 Descrição da Aplicação
O **HABIT** é uma plataforma moderna de publicação e consumo de conteúdo focada no cultivo de hábitos saudáveis e produtividade, organizada de forma semântica por categorias. 

*   **Área Pública:** Permite que leitores naveguem de forma responsiva por categorias populares, leiam postagens em destaque, visualizem as escolhas do editor, realizem buscas textuais e assinem a newsletter.
*   **Área de Autenticação:** Permite que usuários se cadastrem, façam login e gerenciem seus perfis individuais com histórico de publicações e comentários.
*   **Área Administrativa:** Permite o controle gerencial de categorias, criação e edição de novas postagens, moderação de comentários e fila de revisão de novos posts antes de serem publicados.

---

## 📱 Fluxo de Navegação e Telas
Nossa proposta mobile reorganizou os elementos das 14 telas originais para garantir uma excelente área de toque e leitura em dispositivos móveis.

| Tela | Nome | Fluxo | Arquivo na Pasta `/wireframes` |
| :---: | :--- | :---: | :--- |
| **01** | Início (Home) | Público | `tela_01_inicio.png` |
| **02** | Categoria | Público | `tela_02_categoria.png` |
| **03** | Destaques | Público | `tela_03_destaques.png` |
| **04** | Assinar Newsletter | Público | `-` |
| **05** | Admin · Categorias | Administrativo | `-` |
| **06** | Admin · Criar Post | Administrativo | `-` |
| **07** | Admin · Escolhas do Editor | Administrativo | `-` |
| **08** | Admin · Usuários | Administrativo | `-` |
| **09** | Admin · Fila de Revisão | Administrativo | `-` |
| **10** | Admin · Fila de Comentários | Administrativo | `-` |
| **11** | Resultado da Busca | Público | `tela_11_resultados_busca.png` |
| **12** | Entrar (Login) | Autenticação | `-` |
| **13** | Criar Conta | Autenticação | `-` |
| **14** | Perfil do Usuário | Autenticação | `-` |

---

### Organização dos arquivos CSS (estruturados utilizando a metodologia do BEM)
* 'variables.css' : Centraliza os tojens de design (cores, arredondamentos e padrões visuais da tela inicial);
* 'button.css' : Estiização exclusiva do componente de botão e suas variações (BEM);
* 'form.css' : Estilização dos campos de entrada, rótilos e estaods d formulários;
* 'card.css' : Estrutura visual dos cartões de postagens;
* 'navegation.css' : Estilos das barras de navegação superior, inferior e menus;
* 'devices.css' : Arquivo utilitário que simula um celular físico no navegador do computador (para testes locais).

## 📂 Organização dos Arquivos
Seguindo as orientações da disciplina, estruturamos os materiais do projeto em uma pasta limpa e modularizada:

projeto-mobile/
├── wireframes/              # Contém as 14 imagens PNG de baixa fidelidade
├── css/
│   ├── variables.css        # Centraliza os Design Tokens (cores, raios e bordas)
│   ├── button.css           # Estilos do bloco .button e suas variações BEM
│   ├── card.css             # Estilos do bloco .card (padrão, compact e featured)
│   ├── form.css             # Estilos dos campos de texto e agrupadores .form
│   ├── navigation.css       # Estilos das barras de navegação superior e inferior
│   └── device.css           # Simulador utilitário de dispositivo móvel para testes
├── html.html                # Arquivo HTML de teste unificado da aplicação
└── README.md                # Documentação técnica do projeto (esta página)

  
| Compontente | Onde Aparece | Elementos |Variações (Modificadores BEM) |
| :-----------| :----------: | :---: | -----------------------------: |
| *button*    | Login, Cadastro, Newsletter, Criar Post, Fila de Revisão, Categorias | (não aplicado | button--primary, button--secundary, button--disabled, button--danger|
| *card*    | Início, Categoria, Destaques, Resultados de Busca, Perfil | card__image, card__title, card__category, card__date| card--large, card--medium, card--compact |
| *form*    | Início, Cadastro, Criar Post, Categorias (Busca), Perfil | form__group, form__label, form__input, form__button| form__input--error, form__input--focused, form__input--disabled |
| *navegation*    | Header, Bottom Nav ou Sidebar do Admin | navegation__list, navegation__item, navegation__link, navegation__icon | navegation__item--active, navegation--button, navegation--sidebar |

Fluxos: 
* público 01 → 02 ou 03 ou 04 ou 11;
* Autenticação 12 → 13 → 14;
* Administrativo 05–10.
  
Fluxo de publicação:
* tela_06 → tela_09 → aprovação → publicação.
