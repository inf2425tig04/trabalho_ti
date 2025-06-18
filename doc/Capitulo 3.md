# Capítulo 3: Product

## Descrição do Produto
Site formado por 4 páginas estáticas (html, css e xml com respetivo xsd) através do import do GitHub para o Netlify.
A primeira página fala da História do Ensino, a segunda fala com maior destaque da mesma só que em Portugal,
a terceira menciona Curiosidades e a última fornece uns dados estatísticos sobre algumas licenciaturas no país.

## 3.1 Instalação

### Organização no Github
1. Criamos um repositório no GitHub chamado `trabalho_ti`
2. Organizamos uma estrutura de pastas: 
- \doc
- \src com 
    - \img
    - .html
    - .css
    - .js
- README.md

3. Implantação no Netlify:
- Conectamos o repositório GitHub à conta Netlify
- Import GitHub -> Install Repository

## 3.2 Uso e Navegação

1. Acesse o site em: [[Site Netlify](https://inf2425tig04.netlify.app/)]
2. Navegação principal:
- Cabeçalho com botões que permitem a navegação entre as páginas principais
- Na página curiosidades, também tem a possibilidade de, pelo botão "(...) Envie-nos", ir ao fim da página diretamente
- Rodapé contém links secundários onde fornece link para o GitHub do projeto, entre outros

## 3.3 Formulários (em "Curiosidades")
Para restringir uso de caracteres, etc. Usamos este método:

No primeiro, para inserir o nome:
usando required...
- pattern="^([A-Za-zÀ-ÿ]+(\s)?){2,4}$":
  - Aceita apenas: Letras (incluindo acentuadas)
  - 2 a 4 palavras separadas por espaços
- minlength="5" e maxlength="50" - como limite de caracteres

No segundo, a curiosidade:
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
| Download do XML |       |
| Download do XSD |       |
| Tabela |      
        <table>
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
| Lista Ordenada |  <ol>
            <li>Universidade de Coimbra (1290)</li>
            <li>Universidade de Évora (1559)</li>
            <li>Universidade de Lisboa (1911)</li>
            <li>Universidade do Porto (1911)</li>
            <li>Universidade Técnica de Lisboa (1930)</li>
            <li>Universidade Nova de Lisboa (1973)</li>
            <li>Universidade de Aveiro (1973)</li>
            <li>Universidade do Minho (1973)</li>
            <li>ISCTE (1972)</li>
            <li>Universidade dos Açores (1976)</li>
        </ol> |
| Lista Desordenada |  <ul>
        <li><a href="index.html">História Geral</a></li>
        <li><a href="portugal.html">História em Portugal</a></li>
        <li><a href="curiosidades.html">Curiosidades</a></li>
        <li><a href="estatisticas.html">Estatísticas</a></li>
      </ul>   |
| Lista de Descrição |         <dl>
        <dt><strong>Educação</strong></dt>
        <dd>
          <ul>
            <li>Processo de aquisição de conhecimento, habilidades e valores.</li>
            <li>Pode ser formal (escolas, universidades) ou informal (experiências diárias).</li>
          </ul>
        </dd>

        <dt><strong>Sistema Educativo</strong></dt>
        <dd>
          <ul>
            <li>Conjunto de instituições e políticas que regulam o ensino.</li>
            <li>
              Componentes principais:
              <ul>
                <li>Currículo escolar</li>
                <li>Professores e formadores</li>
                <li>Infraestruturas e recursos</li>
              </ul>
            </li>
          </ul>
        </dd>

        <dt><strong>Abordagens Pedagógicas</strong></dt>
        <dd>
          <ul>
            <li>Métodos utilizados para facilitar a aprendizagem.</li>
            <li>
              Exemplos:
              <ul>
                <li>Ensino tradicional</li>
                <li>Ensino baseado em projetos</li>
                <li>Aprendizagem colaborativa</li>
              </ul>
            </li>
          </ul>
        </dd>
      </dl>    |
| Lista Alinhada |     <ol class="roman-list">
        <li>
          <strong>Antiguidade Clássica</strong>
          <ul>
            <li>
              Na <strong>Grécia Antiga</strong>, os rapazes aprendiam <strong>música</strong>, <strong>ginástica</strong> e
              <strong>literatura</strong>, enquanto as raparigas aprendiam principalmente <strong>tarefas domésticas</strong>
              em casa.
            </li>
            <li>
              Devido ao alto custo do papel, usavam-se <strong>tábuas de cera reutilizáveis</strong> para escrever,
              apagando-se os conteúdos com a parte plana do <em>estilete</em>.
            </li>
          </ul>
        </li>  |
| Marcação de Texto | <strong>administradores coloniais</strong> exigiu o desenvolvimento de conhecimentos técnicos 
            específicos. A <mark>Escola de Sagres</mark> |
| Imagem |   <img src="img/ensino_monastico.jpeg" alt="Mosteiro">   |
| Figure |   <figure class="simbolo-figure">
          <img
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c1/DoorBell_001.jpg/330px-DoorBell_001.jpg"
            alt="Campainha elétrica"
            class="simbolo-img"
          >
          <figcaption><em>Campainha elétrica tradicional</em></figcaption>
        </figure>  |
| Figure Caption      |    <figcaption><em>Campainha elétrica tradicional</em></figcaption>   |
| Internal Link |    <a href="#formulario">Tem uma curiosidade? Envie-nos!</a>   |
| External Link |    <a href="index.html">História Geral</a></li>   |
| Form |             <form action="#" method="post" id="form-curiosidade">
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
        </form>  |

CSS Minimum requirements (usage of/change of)
| Requirement | Usage Example |
| :---: | :---: |
| Type selector |       |
| Id selector |       |
| Class Selector |       |
| Pseudo-class Selector |       |
| Attribute Selector |       |
| Pseudo-element Selector |    h2::before {
  content: "📘";
  color: var(--color-secondary);
  font-size: 1.2rem;
  margin-right: 6px;
}   |
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
