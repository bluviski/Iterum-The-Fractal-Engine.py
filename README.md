[README-BR.md](https://github.com/user-attachments/files/23664744/README-BR.md)
ITFE Version 1.1

Bem vindo! Esse projeto é open source de puro domínio público (não precisa de crédito ao original programador, não precisa de autorização, pode fazer uso pessoal, comercial, extender, distorcer,
tudo da maneira que quiser: esse agora é seu projeto, para trabalhar sobre ou reformular totalmente. É sua escolha).

Documentação atual do projeto:

"ITFE.py -

Esse projeto, como base, não possui dono.

Ele é um laboratório de ideias (muitas delas não agradaram muito bem a performance) sobre o conjunto de mandelbrot do matemático Benoît Mandelbrot; caminhável. Onde, se funciona via um sistema de 
tiles que muda conforme o nível de iteração naquele pixel de região do mandelbrot. É inspirado em jogos como Rimworld e exploradores fractais. Posso destacar dentre os elementos de gameplay e tecnologia:

GERAÇÃO FRACTAL  &  A*

A geração do terreno em tiles consiste em pegar uma pequena parcela do mandelbrot (1.0430190101693154e-05) sob o mouse ao apertar o botão esquerdo. Para ter uma ideia, esse sample-size (10,43µm) é em escala 
microcóspicas: glóbulos vermelhos (hemácias) possuem cerca de 8µm de diâmetro.

O mandelbrot possui regiões (biomas), que possuem diferentes cores (para embelezar a exploração do conjunto no terreno!) como magma, verde, ciano, sem cor (padrão), etc.

A geração de diferentes tipos de tiles funciona em base da iteração da parcela: em cada pixel dentro dela, ditada pelo map size. Se o pixel (para motivos mais simplistas, tiles) de iteração for 
baixo, ou seja, o número escapa rápido, cria terrenos passáveis (se for muito baixo, buraco). Se a iteração for muito alta, há montanhas e artefatos mandelbrotnianos! O A* (pathfinding) evita 
terrenos não passáveis e aqueles que custam mais para se movimentar (como "galhos" caindo, chão com buraco, etc)

IA  &  ENTIDADES: 

Temos entidades que funcionam em um sistema relativamente complexo de combate (mas nada fora da curva). Eles possuem pathfinding (A*), simples finite state machines para comportamento 
modificável, equipes (vermelho e azul) e batalham assim que são gerados com a equipe opositora.

As armas deles, como uma forma de IA independente, possuem sistemas de carregamento/munição próprias, possuem chances de emperrar a arma ao atirar conforme a dor e a habilidade do 
portador (habilidade sempre baixa, talvez mude no futuro). Ao atirar, há uma chance de acertar (também ditada pela habilidade e dor) e, se acertar, se ativa todo um sistema de dano. O sistema 
calcula se a penetração da bala é < que a proteção balística do certo membro do corpo. Se for menor, divide o dano total por 2 ao tecido e faz com que a bala atravesse a camada para o osso, e 
assim adiante (órgãos, etc). Então, quanto mais penetração o efeito pode ser mais crítico, mesmo que o dano aparentemente seja diminuído. Há também sangramento, que, se o L de sangue for <= 0 a 
entidade morre, tal como se a vida de partes vitais (coração, torso, cabeça, cérebro, etc) for <= 0, morre também. Atualmente, não há regeneração ou curativos, se uma entidade levar um tiro, chance de morte 
é alta ao decorrer do tempo. Eles também podem cair no chão se a dor passar de > 99, e normalmente neste estágio vai errar todos os tiros ou nunca vai disparar sequer (devido ao emperramento contínuo), mas 
algumas armas possuem algumas dessas funções desativadas (como algumas de laser) com precisão também altíssima.

ENGINE  &  PARADIGMA:

O paradigma é OOP, desenvolvido em Python puro na livraria ARCADE."

