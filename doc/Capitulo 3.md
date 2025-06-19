# Capítulo 3: Product

## Descrição do Produto

Website educativo estático composto por 4 páginas interligadas, desenvolvido com:
- HTML5
- CSS3
- JavaScript
- XML/XSD

Páginas disponíveis:
1. **História Geral do Ensino** - Visão geral da história do ensino
2. **A História do Ensino em Portugal** - Abordagem restringida ao ensino no país
3. **Curiosidades** - Seccção com curiosidades sobre outros países, entre outros; com formulário no final
4. **Estatísticas** - Dados sobre licenciaturas em Portugal

## 3.1 Instalação

### Organização no Github
1. Criação da organização `inf2425tig04` no GitHub
2. Repositório principal: `trabalho_ti`
3. Estrutura de pastas:
- \doc
- \src que, por sua vez, veio a ter
        - \img
        - .html
        - .css
        - .js
- README.md

3. Implantação no Netlify:
- Conectamos o repositório GitHub à conta Netlify
- Import GitHub -> Install Repository
- Configuramos para ir buscar a pasta correta ao GitHub, "/src"

## 3.2 Uso e Navegação

1. Acesso ao nosso site: [[Site Netlify](https://inf2425tig04.netlify.app/)]
2. Navegação principal:
- Cabeçalho com botões que permitem a navegação entre as páginas principais
- Na página curiosidades, também tem a possibilidade de, pelo botão "(...) Envie-nos", ir ao fim da página diretamente para a determinada secção
- Rodapé contém links onde fornece ligação para o GitHub do projeto, entre outros

## 3.3 Formulários (em "Curiosidades")
Para restringir uso de caracteres e etc na validação de texto inserido pelo utilizador. Usamos este método:

Primeiro, para inserir o nome:
usando required...
- pattern="^([A-Za-zÀ-ÿ]+(\s)?){2,4}$":
  - Aceita apenas: Letras (incluindo acentuadas)
  - 2 a 4 palavras separadas por espaços
- minlength="5" e maxlength="50" - como limite de caracteres

Segundo, a curiosidade:
com required...
- rows="5" - Altura inicial (5 linhas)
- minlength="20" e maxlength="500" - como limite de caracteres

```html
<section>
        <h2>Partilhe a sua Curiosidade!</h2>
        <form action="#" method="post" id="form-curiosidade">
          <label for="nome">Seu nome:</label>
          <input
            type="text"
            id="nome"
            name="nome"
            placeholder="Ex: Ana Silva"
            required
            pattern="^([A-Za-zÀ-ÿ]+(\s)?){2,4}$"
            title="Insira entre 2 e 4 palavras, apenas letras e espaços."
            minlength="5"
            maxlength="50"
          >

          <label for="curiosidade">Sua curiosidade:</label>
          <textarea
            id="curiosidade"
            name="curiosidade"
            rows="5"
            placeholder="Escreva aqui uma curiosidade sobre o ensino..."
            required
            minlength="20"
            maxlength="500"
          ></textarea>

          <button type="submit">Enviar Curiosidade</button>
        </form>
```

## 3.4 Validação (HTML e CSS) e Exemplos de Validação
Inserimos cada ficheiro html e css ao respetivo site, validando-os. Se desse erro, corrigiamos e validamos novamente.

1. Validador HTML5 neste repositório:
[Validador HTML5](https://validator.w3.org/nu/?showsource=yes&showoutline=yes&showimagereport=yes&doc=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti)
3. Validador CSS3 neste repositório:[Validador CSS W3C](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti)


![Validador HTML](img2/validador.png)
![Validador CSS](img2/validador3.png)



## 3.5 Requisitos Mandatórios
  Page Requirements
  | Requirement | Usage Example |
  | :---: | :---: |
  | At least 4 pages |  Add a link for at least 4 pages. |
  | 1 XML document | Add a link for the document |
  | 1 XSD document | Add a link for the document |
  | CSS file (if any) | Add a link for one of the documents |


  Describe how the XML validation was performed.

  Requisitos Mínimos HTML
  | Requisitos | Exemplo de Uso |
  | :---: | :---: |
  | Download do XML |   https://github.com/inf2425tig04/trabalho_ti/blob/48d10ca3666fffd2d203c4b2644a4e31d35867cb/src/estatisticas.html#L81-L84  |
  | Download do XSD |    https://github.com/inf2425tig04/trabalho_ti/blob/main/src/estatisticas.html#L87-L90   |
  | Tabela |     https://github.com/inf2425tig04/trabalho_ti/blob/main/src/curiosidades.html#L54-L89 |
  | Lista Ordenada |  https://github.com/inf2425tig04/trabalho_ti/blob/main/src/portugal.html#L168-L179|
  | Lista Desordenada |  https://github.com/inf2425tig04/trabalho_ti/blob/main/src/portugal.html#L118-L123   |
  | Lista de Descrição |     https://github.com/inf2425tig04/trabalho_ti/blob/main/src/curiosidades.html#L234-L272  |
  | Lista Alinhada |    https://github.com/inf2425tig04/trabalho_ti/blob/main/src/curiosidades.html#L99-L139 |
  | Marcação de Texto |  |
  | Imagem |  |
  | Figure |    |
  | Figure Caption      |      |
  | Internal Link |   https://github.com/inf2425tig04/trabalho_ti/blob/main/src/curiosidades.html#L24   |
  | External Link |   https://github.com/inf2425tig04/trabalho_ti/blob/main/src/curiosidades.html#L25   |
  | Form |     |

  CSS Minimum requirements (usage of/change of)
  | Requirement | Usage Example |
  | :---: | :---: |
  | Type selector |       |
  | Id selector |       |
  | Class Selector |       |
  | Pseudo-class Selector |       |
  | Attribute Selector |       |
  | Pseudo-element Selector |    |
  | Combinator Selector |       |
  | Change Highlight style |       |
  | Image insertion |       |
  | Hide an element |       |
  | Text style |       |
  | Font style |       |
  | Background style |       |
  | float/position style |       |
  | List style |       |
  | Box element style |       |
  | table style |       |
  | Responsibility style 2 screen sizes |       |
## Requisitos Extra
