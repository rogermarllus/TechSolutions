# TechSolutions - Bootstrap (CSS-Only)

## Descrição

Interface front-end responsiva desenvolvida para a empresa fictícia TechSolutions. O projeto foca no uso avançado de **Bootstrap 5 (CSS)**, contornando a restrição de não utilizar JavaScript através de técnicas de CSS puro.

## Soluções Técnicas (Sem JS)

### 1. Navegação e Sidebar

Como o componente `collapse` do Bootstrap exige JS, a responsividade do menu foi resolvida via **CSS Display Utilities**:

- **Desktop:** Menu horizontal padrão ou Sidebar fixa (`d-md-block`).
- **Mobile:** Menu empilhado verticalmente ou Sidebar acionada via **Checkbox Hack** (input invisível que controla a visibilidade da div adjacente).

### 2. Modais Interativos

Para criar janelas modais sem script, utilizei a técnica do **Checkbox Hack**:

- Um `<input type="checkbox">` oculto armazena o estado (aberto/fechado).
- Os botões são tags `<label>` conectadas a esse input.
- O CSS utiliza o seletor irmão (`:checked ~ .modal`) para alterar o `display` do modal de `none` para `flex`.

### 3. Gráficos CSS

No Dashboard, os gráficos de barra foram construídos utilizando **Flexbox** e alturas percentuais inline, eliminando a necessidade de bibliotecas de gráficos JS.

## Design System

- **Cores:** Paleta padrão do Bootstrap (Primary, Success, Warning, Danger, Info, Dark).
- **Tipografia:** Padrão do sistema (Native Stack).
- **Ícones:** Bootstrap Icons.

## Estrutura

- `index.html`: Landing page com Hero, Cards e Tabela de Preços.
- `forms.html`: Formulários de Cadastro e Contato com validação visual.
- `dashboard.html`: Área administrativa com métricas e sidebar responsiva.

---

Desenvolvido por [Roger Marllus](https://github.com/rogermarllus).
