# Capítulo 3: Product

## Descrição do Produto

Website educativo estático composto por 4 páginas interligadas, desenvolvido com:
- HTML5
- CSS3
- JavaScript
- XML/XSD

Páginas disponíveis:
1. **História Geral do Ensino** - Visão geral da história do ensino
2. **A História do Ensino em Portugal** - Abordagem restringida à história do ensino no país
3. **Curiosidades** - Seccção com curiosidades sobre outros países, entre outros; com formulário no final
4. **Estatísticas** - Dados sobre licenciaturas em Portugal

## 3.1 Instalação

### Organização no Github
1. Criação da organização `inf2425tig04` no GitHub
2. Repositório principal: `trabalho_ti`
3. Estrutura de pastas:
- \doc #documentação
- \src #source páginas e os seus requisitos (imagens):
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

1. Acesso ao nosso site: [Site Netlify](https://inf2425tig04.netlify.app/)
   - sem autenticação requerida;    
2. Navegação principal:
   - Cabeçalho com botões que permitem a navegação entre as páginas principais;
   - Na página curiosidades, também tem a possibilidade de, pelo botão "(...) Envie-nos", ir ao fim da página diretamente para a determinada secção;
   - Rodapé contém links onde fornece ligação para o GitHub do projeto, entre outros.

## 3.3 Formulários (em "Curiosidades")
Para restringir uso de caracteres e etc na validação de texto inserido pelo utilizador. Usamos este método:

Primeiro, para inserir o nome:
-  type="text"
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
Inserimos cada ficheiro, html e css, ao respetivo site, validando-os. Se houvesse erro, corrigiamos e validavamos novamente... até estar válido após as alterações.

1. Validador HTML5 neste repositório:
[Validador HTML5](https://validator.w3.org/nu/?showsource=yes&showoutline=yes&showimagereport=yes&doc=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti)
2. Validador CSS3 neste repositório:
[Validador CSS W3C](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti)

![Validador HTML](img2/validador.png)
*Resultado da validação de uma das páginas html*
![Validador CSS](img2/validador3.png)
*Resultado da validação da página do css*

## 3.5 Detalhes de Implementação

- Requisitos Mandatórios

  *Page Requirements*
  | Requirement | Usage Example |
  | :---: | :---: |
  | Index HTML |  src/index.html  |
  | Portugal HTML |src/portugal.html|
  | Curiosidades HTML |src/curiosidades.html|
  | Estatísticas HTML |src/estatisticas.html|
  | Cursos Schema XML | src/cursos.xml |
  | Cursos Schema XSD |src/cursos_schema.xsd |
  | Estilo CSS | src/estilo.css |


A validação do XML foi feita através do site: [W3Schools](https://www.w3schools.com/xml/xml_validator.asp).
  - Esta foi feita da mesma maneira que as páginas anteriores: verificar se válido colocando o ficheiro -> se não estiver válido, alteramos até ser válido vendo, novamente, a sua situação de validez após as alterações

   ![Validador XML](img2/validador4.png)

*Resultado da validação do documento xml -> canto superior direito: sem erros*


- Requisitos Mínimos HTML
  | Requisitos | Exemplo de Uso |
  | :---: | :---: |
  | Download do XML |    https://github.com/inf2425tig04/trabalho_ti/blob/48d10ca3666fffd2d203c4b2644a4e31d35867cb/src/estatisticas.html#L81-L84  |
  | Download do XSD |    https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/estatisticas.html#L87-L90  |
  | Tabela |     https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/curiosidades.html#L54-L89 |
  | Lista Ordenada | https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/portugal.html#L168-L179 |
  | Lista Desordenada | https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/portugal.html#L118-L123  |
  | Lista de Descrição |    https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/curiosidades.html#L234-L272  |
  | Lista Alinhada |    https://github.com/inf2425tig04/trabalho_ti/blob/7f4150c8e1002bb014fe3a18a1843c8e0c62ed2f/src/curiosidades.html#L99-L139 |
  | Marcação de Texto | https://github.com/inf2425tig04/trabalho_ti/blob/3009672b470f7980ca1f1f719cb8853c4b1cbda4/src/portugal.html#L53-L54 |
  | Imagem |   https://github.com/inf2425tig04/trabalho_ti/blob/3009672b470f7980ca1f1f719cb8853c4b1cbda4/src/portugal.html#L74   |
  | Figure |   https://github.com/inf2425tig04/trabalho_ti/blob/3009672b470f7980ca1f1f719cb8853c4b1cbda4/src/portugal.html#L73-L76 |
  | Figure Caption      |  https://github.com/inf2425tig04/trabalho_ti/blob/3009672b470f7980ca1f1f719cb8853c4b1cbda4/src/portugal.html#L75  |
  | Internal Link |   https://github.com/inf2425tig04/trabalho_ti/blob/9640d596084358c7141bce62f2b75f1577fb8bbb/src/curiosidades.html#L24   |
  | External Link |   https://github.com/inf2425tig04/trabalho_ti/blob/9640d596084358c7141bce62f2b75f1577fb8bbb/src/curiosidades.html#L25  |
  | Form |     https://github.com/inf2425tig04/trabalho_ti/blob/9640d596084358c7141bce62f2b75f1577fb8bbb/src/curiosidades.html#L388-L414  |

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
