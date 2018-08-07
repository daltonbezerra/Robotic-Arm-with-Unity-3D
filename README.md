# Robotic-Arm-with-Unity-3D
This is a project Im doing for my undergraduate thesis and I am trying to simulate a fully functional robotic arm using the Unity 3D software.



PT-BR

Como tem muitos arquivos e o GitHub tem um limite de 100 arquivos, irei fazer upload no Google Drive e disponibilizar o link aqui: https://drive.google.com/drive/folders/1jbXwvqnPtrMfiij1HHC3lclAo9ZLRKkw?usp=sharing


Até o momento tive muitas dificuldades com as juntas do software, especialmente ao tentar conectar mais de uma junta. Sempre que eu apertava o "play" o braço começava a tremer em todas as juntas e não estava retratando o que devia ser a realidade. Os videos tutoriais que encontrei pela internet e no proprio site do desenvolvedor do software eram mais voltados a explicar o funcionamento de cada junta separadamente e não faziam a conexão de duas ou mais juntas em sequencia.

Depois de muita pesquisa e principalmente tentativa e erro, consegui fazer com que o braço apresentasse um comportamento parecido com a "realidade". Consegui conectar três juntas e quando aperto o "play" e uso um cubo para colidir com o braço robótico, o mesmo cai como se estivesse sofrendo ação da gravidade. A junta de rotação ainda não está com um funcionamento ideal, mas já está muito satisfatório. Agora preciso aprender a movimentar o braço através de scrips.

Depois de pesquisar no google, no site do Unity e de assistir vários tutoriais no Youtube, consegui controlar cada junta do braço utilizandoum Slider para cada junta e utilizando o comando "transform.localrotation = quaternion" para fazer cada junta rodar dentro de seu próprio eixo sem que as juntas subsequentes perdessem o zero.



EN-US

Since there are too many files and GitHub only let me upload 100 files will upload on Google Drive and leave the link here: https://drive.google.com/drive/folders/1jbXwvqnPtrMfiij1HHC3lclAo9ZLRKkw?usp=sharing


So far I encountered many dificulties, especialy with the joints of the software. I was having a hard time connecting more than one joint together without the arm flickering  whenever I pressed the play buttom on the software. I've searched for many tutorials on the internet but all of them would only explain the functioning of each joint and I need to know how to connect more than one joint together without it going crazy.

After a lot of research and mainly trial and error I've manage to connect 3 joints without the arm flicker around when I pressed the play. I used a cube and collided it against the arm and it just felt down as if the gravity was acting on it. The rotation joint is not perfect but it is satisfatory. Now I need to figure how to move the arm around using scrips.

After some research on google, on Unity website and watching several tutorials on Youtube, I finally figured out how to control the joints using a Slider for each joint a using the command "transform.local rotation = quaternion" to make the joints rotate around its own axis without afcting the subsequent joint axis.
