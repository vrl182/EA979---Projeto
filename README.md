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
> %%Hue e luminosidade (3.1) e Loss (3.2)
> - Inferência da cor final:
> %% (3.3)
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
> http://ijcsn.org/IJCSN-2019/8-2/Automatic-Colorization-of-Black-and-White-Images-using-Deep-Learning.pdf
> 
> https://www.ijrte.org/wp-content/uploads/papers/v8i6/F7719038620.pdf
