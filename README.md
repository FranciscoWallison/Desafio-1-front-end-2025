
# Dashboard de Cartas Pokémon com [Reactjs e Vite](https://pt.vitejs.dev/guide/)

![image](https://github.com/user-attachments/assets/4bf0189c-cc7e-4e45-94ce-9b0929edfc1b)


O commit inicial deve incluir as configurações básicas do Reactjs com Vite e a instalação das dependências (Bootstrap e pokemon-tcg-sdk):

```bash
git add .
git commit -m "ADS-init: <sua_matricula> Reactjs-vite"
```

### Objetivo do INIT  
Nesta etapa, o projeto deve ser iniciado do zero para garantir um histórico de evolução completo. Todos os arquivos criados devem conter data, nome e matrícula, além de uma breve descrição sobre o documento.

### Exemplo de Documentação em Arquivos  
```js
/**
 * Nome do arquivo: App.jsx
 * Data de criação: 22/05/2025
 * Autor: João Silva
 * Matrícula: 123456
 *
 * Descrição:
 * Este componente React implementa um dashboard de cartas do Pokémon TCG.
 * Funcionalidades:
 * - Campo de busca por código de card
 * - Exibição detalhada do card pesquisado
 * - Persistência e exibição de cartas salvas no localStorage
 * - Estilização com Bootstrap
 */
```

---

# Funcionalidades do Dashboard de Cartas Pokémon

1. **Exibição de Cartas Salvas**  
   - Exibe, no topo da página, miniaturas das cartas que o usuário salvou anteriormente (armazenadas em `localStorage`).  
   - Se não houver cartas salvas, mostra “Nenhuma carta salva.”  
   - **Exemplo de Commit**:  
     ```bash
     git commit -m "ADS-layout_cartas_salvas: <sua_matricula> Reactjs-vite"
     ```

2. **Campo de Busca de Cartas**  
   - Permite ao usuário digitar o código do card (ex.: `base1-4`) e clicar em **Buscar**.  
   - A busca é feita via `PokemonTCG.card.find(query, { apiKey })`.  
   - **Exemplo de Commit**:  
     ```bash
     git commit -m "ADS-filtro_busca: <sua_matricula> Reactjs-vite"
     ```

3. **Exibição Detalhada do Card**  
   - Ao pesquisar, renderiza:  
     - Imagem em alta resolução (`images.large`).  
     - Nome, supertype e subtypes.  
     - HP e tipos.  
     - Evoluções (`evolvesTo`).  
     - Regras especiais (`rules`).  
     - Lista de ataques com custo, dano e texto.  
     - Fraquezas e custo de recuo.  
     - Informações do conjunto (nome e data de lançamento).  
     - Número, raridade e artista.  
     - Preço médio de mercado (via `tcgplayer.prices.holofoil.market`).  
   - **Exemplo de Commit**:  
     ```bash
     git commit -m "ADS-detalhes_cartas: <sua_matricula> Reactjs-vite"
     ```

4. **Salvar Cartas**  
   - Botão “Salvar Carta” para persistir o card atual em `localStorage`.  
   - Evita duplicatas (desabilita o botão se o card já estiver salvo).  
   - **Exemplo de Commit**:  
     ```bash
     git commit -m "ADS-salvar_cartas: <sua_matricula> Reactjs-vite"
     ```

---

### Exemplo de Consulta à API Pokémon TCG

```js
import PokemonTCG from 'pokemon-tcg-sdk';

const apiKey = import.meta.env.VITE_POKEMON_API_KEY;
PokemonTCG.card.find('base1-4', { apiKey })
  .then(card => console.log(card))
  .catch(err => console.error('Erro ao buscar o card:', err));
```

---

### Histórico de Commits

Para manter um versionamento claro, siga sempre o padrão:

```bash
git add .
git commit -m "ADS-nome_da_funcionalidade: <sua_matricula> Reactjs-vite"
```

> Exemplos adicionais:  
> - `ADS-layout_cartas_salvas`  
> - `ADS-filtro_busca`  
> - `ADS-detalhes_cartas`  
> - `ADS-salvar_cartas`

---

## Estrutura do Projeto

```text
/public
  └─ index.html
/src
  ├─ App.jsx
  ├─ main.jsx
  └─ styles.css
.env
package.json
vite.config.js
```

Todos os arquivos devem conter cabeçalhos com data, nome e matrícula, e uma breve descrição da sua finalidade.

---

## Prazo de Entrega e Apresentações

A data de entrega e apresentações está definida para o período de 
**22/05** a **29/05**. 
Recomendo que concluam suas tarefas o mais cedo possível para evitar imprevistos de última hora.

