# **Protótipo Mobile do BEM**
## Estrutura para o repositório de trabalho

### Integrantes:
* Giovanna Almeida Dias - 10436553
* Lucas Masteguim -

### Organização dos arquivos CSS (estruturados utilizando a metodologia do BEM)
* 'variables.css' : Centraliza os tojens de design (cores, arredondamentos e padrões visuais da tela inicial);
* 'button.css' : Estiização exclusiva do componente de botão e suas variações (BEM);
* 'form.css' : Estilização dos campos de entrada, rótilos e estaods d formulários;
* 'card.css' : Estrutura visual dos cartões de postagens;
* 'navegation.css' : Estilos das barras de navegação superior, inferior e menus;
* 'devices.css' : Arquivo utilitário que simula um celular físico no navegador do computador (para testes locais).

  
| Compontente | Onde Aparece | Elementos |Variações (Modificadores BEM) |
| :-----------| :----------: | :---: | -----------------------------: |
| *button*    | Login, Cadastro, Newsletter, Criar Post, Fila de Revisão, Categorias | (não aplicado | button--primary, button--secundary, button--disabled, button--danger|
| *card*    | Início, Categoria, Destaques, Resultados de Busca, Perfil | card__image, card__title, card__category, card__date| card--large, card--medium, card--compact |
| *form*    | Início, Cadastro, Criar Post, Categorias (Busca), Perfil | form__group, form__label, form__input, form__button| form__input--error, form__input--focused, form__input--disabled |
| *navegation*    | Header, Bottom Nav ou Sidebar do Admin | navegation__list, navegation__item, navegation__link, navegation__icon | navegation__item--active, navegation--button, navegation--sidebar |
