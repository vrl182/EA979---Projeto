# `<Estudo sobre Colorização Automática de Imagens Preto e Branco>`
# `<Automatic Colorization of Black and White Images>`

## Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de graduação *EA979A - Introdução a Computação Gráfica e Processamento de Imagens*, 
oferecida no primeiro semestre de 2022, na Unicamp, sob supervisão da Profa. Dra. Paula Dornhofer Paro Costa, do Departamento de Engenharia de Computação e Automação (DCA) da Faculdade de Engenharia Elétrica e de Computação (FEEC).

> Integrantes
> |Nome  | RA | Curso|
> |--|--|--|
> | Caio Eduardo Ferraz da Silva  | 195203  | Eng. Elétrica|
> | Victor Rodrigues Laterza  | 206601  | Eng. de Computação|


## Descrição do Projeto
> A ideia de transformar uma imagem em tons de cinza em uma imagem colorida é bastante desafiadora e interessante por si só. Pois, para que uma colorização ocorra de forma verossímil, ou seja, se aproximando de uma imagem com cores reais, há a necessidade de se ter um conhecimento prévio sobre o que está sendo representado pela imagem. Partindo deste pressuposto e movidos, à priori, pela curiosidade, decidimos estudar ferramentas no estado da arte, e, posteriormente, desenvolver uma técnica própria, o que se mostrou inviável no decorrer do desenvolvimento do projeto.
> 
> Desse modo, o foco do projeto como um todo se voltou em estudar e compreender passo a passo o funcionamento de uma dessas técnicas. Desse modo, escolhemos focar na leitura do artigo de 2017, "Learning Representations for Automatic Colorization" de Gustav Larsson, Michael Maire e Gregory Shakhnarovich, que se apresenta uma ferramenta bastante avançada quanto à sua acurácia, demonstração dos princiais tipos de erros gerados, e contribuições para a aplicação de modelos de aprendizagem visual auto-supervisionado.

## Abordagem Adotada
> Nosso estudo foi divido em algumas etapas:
 
### Exposição sobre o artido estudado:
> Neste artigo desenvolveu-se um sistema de colorização de imagem totalmente automático. Nele, exploraram-se representações de baixo nível e semânticas, aproveitando avanços em redes profundas. Assim, buscou-se treinar este modelo para que fosso possível prever histogramas de cores por pixel, a qual pode ser usada para gerar automaticamente uma imagem colorida ou manipulada adicionalmente antes da formação da imagem. Por fim, explorou-se a colorização como uma aplicação para o aprendizado de representação visual auto-supervisionada. E superando os métodos existentes.

### Metodologia utilizada:
> - Preparação dos dados:
>   - Luminosidade: para fazer o treinamento de dados, foi feito uma conversão da cor das imagens para escala de cinza, de acordo com a média aritmética dos valores RGB da imagem, isto é, foi definido L como a luminosidade, tal que L = (R+G+B)/3. Com esta simples técnica, foi possível fazer a dessaturação das imagens e utilizá-la na previsão de cores.
>   - Hue/chroma: ao invés de utilizar L como a matiz de cores de saída, foi utilizado espaços baseados em matiz, como por exemplo, o HSL que pode ser representado por um  cilindro com coordenada angular H (matiz), distância radial S (saturação) e altura L (luminosidade). Porém devido a instabilidades que ocorrem nas cores branco e preto, eventualmente foi pensado no espaço HSV, que só tem instabilidade no preto. Finalmente, para resolver as instabilidades e manter o canal L, foi feio um bicone tal que o canal S foi substituído pelo C (Chroma) na saturação. A conversão feita do HSV é dada por V = L+C/2 e S = C/V.
>   - Lab: Lab(L*a*b) foi projetado para ser linear. Um vetor (a,b) define um espaço Euclidiano onde a distância do vetor até a origem define o chroma.
>   - Loss: baseado no artigo [1], foi utilizado uma técnica para mensurar a perda, por meio de histogramas.
> - Arquitetura e treinamento da rede neural:
>   - VGG-16-G:
>   - Hipercolunas:
> %% (3.5)
> Descrever de maneira clara todas as etapas executadas no projeto, incluindo tópicos como:
> - bases de imagens utilizadas (e suas descrições);
> - modelagens adotadas;
> - descrição de simplificações realizadas;
> - testes realizados (incluindo descrição dos testes que não deram certo), etc.
> Nesta seção devem ser incluídos links para os notebooks que correspondem às diversas etapas do projeto ou devem ser realizadas referências à execução dos códigos.

## Resultados Finais
> Descrever e apresentar os resultados finais obtidos
> %%(4)

## Discussão
> Discutir os resultados finais obtidos considerando-se o objetivo inicialmente proposto.
> Descrever as principais dificuldades enfrentadas na execução do projeto.
> Descrever limitações da abordagem adotada.
> %% (5)


## Referências Bibliográficas
> https://arxiv.org/pdf/1603.06668.pdf
> 
> 1.Charpiat, G., Hofmann, M., Sch¨olkopf, B.: Automatic image colorization via multimodal predictions. In: ECCV (2008)

