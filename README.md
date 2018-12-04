# Robotic-Arm-with-Unity-3D
This is a project Im doing for my undergraduate thesis and I am trying to simulate a fully functional robotic arm using the Unity 3D software.



PT-BR

Como tem muitos arquivos e o GitHub tem um limite de 100 arquivos, irei fazer upload no Google Drive e disponibilizar o link aqui: https://drive.google.com/open?id=1DLmOl0Mk68R6rK3tQSzEPl2WobyAJhCy

Atualmente a robótica é uma das áreas que mais crescem não apenas no setor industrial, mas também no setores de consumo e serviços. Diversas áreas se beneficiam com o avanço tecnológico da robótica, principalmente a área industrial que beneficia se com os ganhos em produtividade e qualidade. Porém, para atender a esta crescente demanda, é necessário formar profissionais que já saiam de seus respectivos cursos com um conhecimento mais aprofundado de como projetar e controlar um manipulador robótico.
É lógico que para obter esse conhecimento mais aprofundado em robótica, faz se necessário ter uma experiencia com um manipulador robótico real, pois a prática tem um poder de fixação muito mais poderoso do que a teoria. Porém, sabe se que uma braço robótico não é um investimento baixo, e sua manutenção também não é barata. Por isso, muitas instituições de ensino não tem condições de fornecer este tipo de experiencia a seus alunos. 
Pensando nisso, através do uso do Unity 3D, que é um software voltado para o desenvolvimento de jogos, foi desenvolvido um simulador de braço robótico para correlacionar a teoria da sala de aula com o que realmente acontece na prática.
O manipulador robótico deste simulador, pode ser controlado tanto pela cinemática inversa, (que é o padrão usado na indústria), quanto pela cinemática direta. Os resultados obtidos mostram que esta é uma abordagem viável.

O projeto consiste em desenvolver um software simulador, que terá um braço robótico totalmente controlado pelo usuário através de sua interface. Além disso, este software também possuirá um menu que deverá ser bem intuitivo e de fácil navegação.

O manipulador robótico poderá ser manipulado pelo usuário de duas formas:

-A primeira será utilizando a cinemática direta, onde o usuário poderá controlar a angulação de cada junta individualmente através de sliders que serão devidamente identificados e posicionados na interface do programa. Ao lado de cada um dos sliders, será posicionado um input field, que mostrará ao usuário quantos graus cada uma das juntas estará rotacionada.

-A segunda maneira de controlar o manipulador robótico será através da cinemática inversa. Na tela da cinemática inversa, o robô será controlado através de três input fields, que estarão presentes na interface. O usuário deverá digitar um vetor de posição (X, Y, Z). Através da programação de controle que contém as equações da cinemática inversa baseadas nas dimensões do manipulador desenvolvido no software, a ponta da ferramenta do braço robótico deverá ir para a posição digitada pelo usuário. Para auxiliar a visualização de qual ponto no espaço o usuário digitou, uma pequena esfera que estará presente na interface do programa se moverá para as coordenadas digitadas pelo usuário.

O braço robótico foi desenhado pelo próprio autor dentro do Unity e passou por várias modificações ao longo do desenvolvimento do projeto de forma a obter a melhor performance possível. Ele foi desenvolvido através da associação em série de objetos cilíndricos e retangulares e foi batizado de WyvernClaws4.

O manipulador possui cinco juntas de rotação e pode ser classificado como um braço articulado. Porém, uma de suas juntas controla apenas a ferramenta do manipulador. Na figura 30, pode se observar o design final do manipulador.

O longo do desenvolvimento do projeto, diversos problemas foram encontrados. A maioria dos problemas foram solucionados através de pesquisas online. Como já dito anteriormente, o Unity 3D possui uma comunidade muito grande e que sempre está disposta a ajudar. A maioria dos problemas encontrados por desenvolvedores iniciantes podem ser solucionados com uma rápida pesquisa.

Um dos principais problemas encontrados, foi fazer com que todos os componentes do manipulador se encaixassem sem que ocorresse nenhum tipo de conflito quando o simulador estivesse rodando. Isto ocorria, pois a caixa de colisão de cada um dos objetos que compõem o braço estava ativa, o que fazia com que o braço ficasse se tremendo sempre que o simulador começava a rodar. Para resolver este problema, a caixa de colisão de diversos objetos foram desabilitadas, e alguns dos objetos tiveram suas caixas de colisão reduzidas, para permitir que o manipulador ainda pudesse colidir com o chão ou consigo mesmo.

Outro problema de extrema importância que foi encontrado ao longo do projeto, foi no cálculo do \textit{theta1}. Para calcular o theta1, bastaria utilizar a função Mathf.Atan. Porém, em softwares utilizados para desenvolver jogos, esta função funciona de forma diferente. A função Mathf.Atan não é capaz de diferenciar o primeiro e o terceiro quadrante. Não importa se a divisão for positiva ou negativa, esta função sempre retornará o mesmo valor. Além disso, esta função também não retorna resultados caso a divisão seja por zero, ou seja, o eixo X do manipulador nunca poderia ser zero. E isto seria um grande problema para um braço robótico.

Para contornar este problema, foi utilizada a função Mathf.Atan2. Esta função retorna valores diferentes para cada um dos quatro quadrantes, além de retornar valores para caso a divisão seja por zero. Esta é a função utilizada nos jogos, e que deve ser utilizada neste software para calcular o arctg de qualquer valor.

Outra dica importante para realizar rotações neste tipo de software é utilizar a função Quaternion ao invés da função eulerAngles. Isto ocorre principalmente pois a função Quaternion não está sujeita ao efeito conhecido como Gimbal Lock. O gimbal lock, é um efeito que ocorre quando dois eixos acabam ficando em paralelo, o que faz com que o sistema "perca" um grau de liberdade. Outro motivo para utilizar o Quaternion, é que esta função sempre fará o menor percurso de rotação entre dois pontos, o que otimiza o sistema.

Com a conclusão deste projeto e com os resultados obtidos após a finalização do mesmo, foi possível observar que este software é uma abordagem totalmente viável e que pode ser implementada em qualquer curso de robótica como um método auxiliar para o ensino do assunto.

Utilizando o Unity 3D, foi possível não só desenvolver um manipulador robótico do zero, como também foi possível aplicar duas diferentes formas de controle ao mesmo. Além disso, o Unity possui uma curva de aprendizado bem acentuada, o que faz com que a correção de erros e otimizações passe a consumir cada vez menos tempo do desenvolvedor.

Ao longo do desenvolvimento do projeto, o Unity 3D mostrou ser uma ferramenta que tem muito potencial para ser utilizada não só no desenvolvimento de jogos, mas também no desenvolvimento de softwares voltados para o lado educacional. Por este ser um trabalho que é voltado para o âmbito educacional, todo o projeto será disponibilizado no GitHub para que outras pessoas possam contribuir no seu desenvolvimento. O intuito é transformar este simulador em uma ferramenta auxiliar que possa de fato contribuir para a formação de engenheiros e engenheiras que já saiam de seus cursos com uma boa bagagem na construção e controle de manipuladores robóticos.

Sugestões para trabalhos futuros incluem:

-Incluir uma maior variedade de modelos de manipuladores

-Melhorar a interface do software

-Portar o software para outras plataformas como Andoid, IOS, Linux, etc

-Incluir o detalhamento das equações de cada manipulador para permitir ao aluno e/ou professor uma melhor compreensão do que está ocorrendo por trás das movimentações do braço

-Incluir outros métodos de controle de manipuladores robóticos como a matriz jacobiana
