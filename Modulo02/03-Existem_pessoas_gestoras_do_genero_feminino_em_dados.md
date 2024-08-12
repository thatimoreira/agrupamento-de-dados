# Existem pessoas do gênero feminino em dados?

Nessa aula revisamos a tabela dinâmica e vimos o quanto ela pode ser poderosa para tabalhar com nossos dados.
Na primeira análise que fizemos, usamos a tabela dinâmica só para agrupar informações básicas, como quantas
pessoas por gênero, raça ou etnia. Mas agora, vamos um pouco mais fundo, pois a tabela dinâmica é uma ferramenta
poderosa para agrupar, cruzar, filtrar e interagir com dados de forma dinâmica e flexível.

<br>

### Cruzamento de Dados

Imagina que queremos saber quantas mulheres responderam que são gestoras. Para isso, precisamos cruzar os dados
de duas colunas: a de **gênero** e a de **nível de cargo** (NOVO_NIVEL). Isso porque não dá para simplesmente agrupar por gênero ou
por cargo, precisamos combinar essas duas informações.

- Descobrimos que existem **132 mulheres** que se identificam como gestoras
-  Comparando com o número de homens gestores, que é bem maior: 578
-  Isso nos leva a pensar em questões como a diferença de gênero nos cargos de liderança

<br>

### Organização da tabela

Durante a aula, experimentamos diferentes maneiras de organizar a tabela, invertendo linhas e colunas para ver qual
visualização funcionava melhor para a gente.

> Às vezes, a primeira forma que a gente escolhe não é a ideal, então testamos outras até encontrar o que faz mais sentido.

<br>

### Considerações finais

Também falamos sobre a importância de olhar as proporções, não só os números absolutos. Por exemplo, mesmo que tenha
menos mulheres no total, se uma porcentagem maior de mulheres do que homens são gestoras, isso pode ser um dado importante.

<br>

### Exercícios

Responder e gerar gráficos sobre as perguntas abaixo:

1. Quantas mulheres responderam que são amarelas?<br>
  Resposta: 38<br><br>
  ![Tabela dinâmica genêro x raça/etnia](https://github.com/user-attachments/assets/45838afd-1b59-4ad1-9d39-3fed91771043)

  #### Solução:
  - **Criei uma tabela dinâmica, conforme os passos abaixo:**<br>
    I - Selecionei todas as informações da planilha que contém os dados<br>
    II - No menu do *Google Sheets* fui em **Inserir** > **Tabela Dinâmica**<br>
    III - Coloquei a tabela em uma nova aba<br>
    <br>
  - **Com a tabela dinâmica gerada, a configurei da seguinte forma:**<br>
    I   - Em *Linhas*, adicionei a coluna **Gênero**<br>
    II  - Em *Filtros*, adicionei a coluna **Raça/Cor/Etnia**<br>
    III - Em *Valores*, adicionei a **ID** (pois é uma coluna que tem valores únicos por pessoa), e escolhi a opção *COUNT* (contagem)

  <br>
  
2. Qual é o estado que mais tem gestores homens?<br>
  Resposta: São Paulo, com 286 gestores homens<br>
  ![Tabela dinâmica: estado x gênero x cargo](https://github.com/user-attachments/assets/cf059ca0-6b22-44e5-a5b4-0c5c6f19382b)

  #### Solução:
  - **Criei uma tabela dinâmica, conforme os passos da resposta 1:**<br>
    
  - **Com a tabela dinâmica gerada, a configurei da seguinte forma:**<br>
    I   - Em *Linhas*, adicionei a coluna **Estado**<br>
    II  - Em *Filtros*, adicionei a coluna **Gênero** e selecionei *Masculino*<br>
    III - Adicionei outro filtro para a coluna **NOVO_NIVEL** e selecione apenas *Pessoa Gestora*
    IV  - Em *Valores*, adicionei novamente a **ID** e escolhi a opção *COUNT*
    
  <br>
  
3. Qual é a média de idade?<br>
  Resposta: 31 <br><br>
  ![Tabela Média de Idade](https://github.com/user-attachments/assets/741eeb22-6855-4379-b3c5-26e4a9a64f3c)

  #### Solução:
  - **Em outra aba inseri a seguinte fórmula:**<br>
    ```
    =MÉDIA(Sheet1!B:B)
    ```
  
  <br>
  
4. Qual é a média de idade por gênero?<br>
  - Feminino.............: 31<br>
  - Masculino............: 31<br>
  - Prefiro não responder: 27<br>
  - Não respondido.......: 26<br><br>
  ![Tabela Média de Idade por Gênero](https://github.com/user-attachments/assets/d22f9fd0-faa2-4edb-ac80-d39f14c7faea)

  #### Solução:
  - **Na mesma aba do exercício 4 criei uma tabela com uma coluna para cada opção e inseri a seguinte fórmula:**<br>
    ```
    =MÉDIASE(Sheet1!$D:$D; "Feminino"; Sheet1!$B:$B)
    ```
  - Arrastei a fórmula para as demais colunas e adaptei o parâmetro do gênero apenas

  <br>
  
5. Qual é a média de idade por estado?<br><br>
  ![Tabela Média de Idade por Estado](https://github.com/user-attachments/assets/84bc11c2-0ffa-4922-81b6-3efaf3310ead)

  #### Solução:
  - **Criei uma tabela dinâmica, conforme os passos da resposta 1:**<br>
    
  - **Com a tabela dinâmica gerada, a configurei da seguinte forma:**<br>
    I  - Em *Linhas*, adicionei a coluna **Estado**<br>
    II - Em *Valores*, adicionei a coluna **Idade** e escolhi a opção *AVERAGE* (média)

  <br>

  6. Qual é a média de idade por gênero por estado?<br><br>
     ![Tabela dinâmica Média de Idade por Gênero por Estado](https://github.com/user-attachments/assets/7cc0be71-3a04-4adc-8ef4-5063d796917f)

  #### Solução:
  - **Criei uma tabela dinâmica, conforme os passos da resposta 1:**<br>
    
  - **Com a tabela dinâmica gerada, a configurei da seguinte forma:**<br>
    I   - Em *Linhas*, adicionei a coluna **Estado**<br>
    II  - Em *Colunas*, adicionei a coluna **Gênero**<br>
    III - Em *Valores*, adicionei a coluna **Idade** e escolhi a opção *AVERAGE* (média)
