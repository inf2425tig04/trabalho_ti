# Capítulo 3: Product

## Descrição do Produto
Site formado por 4 páginas estáticas (html, css e xml com respetivo xsd).
A primeira página fala da História do Ensino, a segunda fala com maior destaque da mesma só que em Portugal,
a terceira menciona Curiosidades e a última fornece uns dados estatísticos sobre algumas licenciaturas no país.

## 3.1 Instalação

### Organização no Github
1. Criamos um repositório no GitHub chamado `trabalho_ti`
2. Organizamos uma estrutura de pastas: 
\doc
\src com \img e 
                \img
                .html
                .css
                .js
README.md

3. Implantação no Netlify:
- Conectamos o repositório GitHub à conta Netlify
- Import GitHub -> Install Repository

## 3.2 Uso e Navegação

1. Acesse o site em: [[URL do site no Netlify](https://inf2425tig04.netlify.app/)]
2. Navegação principal:
- Cabeçalho com botões que permitem a navegação entre as páginas principais
- Caso tenha um "sub-cabeçalho", com botões também, tratam-se de navegações rápidas pela mesma página (como em "Curiosidades")
- Rodapé contém links secundários onde fornece link para o GitHub do projeto, entre outros

## 3.4 Formulários (em Curiosidades)

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

### Validação (HTML e CSS), exemplos

1. Validador HTML5 neste repositório:
🔗 **HTML Validator**:  
[https://validator.w3.org/nu/?showsource=yes&showoutline=yes&showimagereport=yes&doc=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti](https://validator.w3.org/nu/?showsource=yes&showoutline=yes&showimagereport=yes&doc=https%3A%2F%2Fgithub.com%2Finf2425tig04%2Ftrabalho_ti)
3. Validador CSS3 neste repositório: https://jigsaw.w3.org/css-validator

![Validador](img2/validador.png)


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
| Download do XML |       |
| Download do XSD |       |
| Tabela |       |
| Lista Ordenada |       |
| Lista Desordenada |       |
| Lista de Descrição |       |
| Lista Alinhada |       |
| Marcação de Texto | ``` <em>paragraph</em> ```       <table>
        <thead>
          <tr>
            <th rowspan="2">Método</th>
            <th colspan="2">Detalhes</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><strong>Sistema Montessori</strong></td>
            <td>Maria Montessori</td>
            <td>Autoeducação em espaços preparados com materiais sensoriais. Autonomia da criança, intervenção mínima do professor e ênfase no ritmo individual.</td>
          </tr>
          <tr>
            <td><strong>Pedagogia Waldorf</strong></td>
            <td>Rudolf Steiner</td>
            <td>Autoeducação em espaços preparados com materiais sensoriais. Autonomia da criança, intervenção mínima do professor e ênfase no ritmo individual.</td>
          </tr>
          <tr>
            <td><strong>Pedagogia Waldorf</strong></td>
            <td>Rudolf Steiner</td>
            <td>Enfatiza imaginação e criatividade. Sem computadores até aos 14 anos, aprendizagem através de atividades artísticas e manuais.</td>
          </tr>
          <tr>
            <td><strong>Escolas Democráticas</strong></td>
            <td>A.S. Neill (Summerhill)</td>
            <td>Escola autogovernada, frequência opcional. Liberdade exceto em questões de segurança, saúde ou direitos dos outros.</td>
          </tr>
          <tr>
            <td><strong>Método Kumon</strong></td>
            <td>Toru Kumon</td>
            <td>Sistema japonês de aprendizagem individualizada através da repetição e progressão gradual.</td>
        </tr>
        </tbody>
        <tfoot>
          <tr>
            <td colspan="3">Fonte: Wikipédia e Britannica</td>
          </tr>
        </tfoot>
      </table> |
| Imagem |      |
| Figure |   https://github.com/exemploTrabalho/report_inf-ti/blob/f676d24207f24920710211d87ed96dd4c602720e/src/index.html#L4-L6    |
| Figure Caption      |       |
| Internal Link |       |
| External Link |       |
| Form |       |

CSS Minimum requirements (usage of/change of)
| Requirement | Usage Example |
| :---: | :---: |
| Type selector |       |
| Id selector |       |
| Class Selector |       |
| Pseudo-class Selector |       |
| Attribute Selector |       |
| Pseudo-element Selector |       |
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
