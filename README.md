# TORRE-1

## Sobre o Projeto

Este projeto consiste em uma simulação física e jogo de arremesso bidimensional focado na destruição de estruturas estáveis e empilhadas. A aplicação foi desenvolvida utilizando HTML, CSS e a biblioteca **p5.js**, trazendo o motor de física **Matter.js** para calcular de forma realista o equilíbrio de corpos rígidos, gravidade, forças de impacto e colisões por fricção.

O objetivo do jogo é derrubar uma torre ou pirâmide constituída por múltiplos blocos dinâmicos utilizando um estilingue mecânico para disparar um projétil poligonal. Esta versão inicial foca no mapeamento do motor físico e no comportamento estático da torre até o impacto: os blocos atingidos sofrem com a transferência de força e caem de forma realista pelo cenário, permanecendo ativos e visíveis no mundo físico após a queda.

---

## Funcionalidades

* Mecânica de mira, tração e disparo de projétil baseada em uma restrição elástica ajustável (`slingshot.js`).
* Simulação física em tempo real controlando propriedades de peso, inércia, gravidade e colisão via `Matter.js`.
* Estrutura de torre estável gerada por blocos individuais empilhados sob superfícies de suporte elevado (`stand.js`).
* Persistência dos corpos rígidos no cenário pós-impacto, permitindo analisar o repouso e a física de empilhamento dos blocos caídos.
* Vinculação direta de imagem gráfica customizada ao sprite do projétil poligonal (`polygon.png`).

---

## Tecnologias Utilizadas

* **HTML5**
* **CSS3**
* **p5.js** (e extensões: p5.dom, p5.play)
* **Matter.js** (Engine de física 2D)

---

## Objetivo

O principal objetivo deste projeto é estabelecer as fundações de um motor de jogo de física 2D, aplicando conceitos de Programação Orientada a Objetos (POO) para construir e empilhar blocos de maneira modular. O foco está em calibrar as forças de atrito e as hitboxes dos blocos sobre o suporte para que fiquem perfeitamente equilibrados até sofrerem a ação de uma força externa (o projétil).

---

## Aprendizados

Durante o desenvolvimento deste projeto, foram aplicados conceitos como:

* Construção modular de estruturas através de classes customizadas em JavaScript (`block.js`, `stand.js`, `ground.js`).
* Implementação e configuração de restrições de distância elástica (`Matter.Constraint`) controladas pelos inputs do mouse.
* Sincronização do loop de renderização do p5.js com as atualizações de posição e rotação matemática calculadas pela engine física.
* Estudo prático de colisão elástica e distribuição de forças em cadeia (reação de blocos empilhados verticalmente).
* Organização estruturada do projeto isolando dependências de terceiros em `libraries/` e a lógica do jogo em `scripts/`.

---

## Como Executar

1. Clone este repositório:
```bash
git clone [https://github.com/seu-usuario/TORRE-1.git](https://github.com/seu-usuario/TORRE-1.git)
```

2. Acesse a pasta do projeto:

```bash
cd TORRE-1
```

3. Abra o arquivo index.html em seu navegador de preferência para tensionar o estilingue e disparar contra a torre de blocos.

---

## Estrutura do Projeto

```text
TORRE-1/
│
├── assets\img/
│   └── polygon.png
│
├── libraries/
│   ├── matter.js
│   ├── p5.dom.min.js
│   ├── p5.js
│   └── p5.play.js
│
├── scripts/
│   ├── block.js
│   ├── ground.js
│   ├── sketch.js
│   ├── slingshot.js
│   └── stand.js
│
├── style/
│   └── style.css
│
├── index.html
└── README.md
```

---

## Licença

Este projeto foi desenvolvido exclusivamente para fins educacionais e de aprendizado.

Desenvolvido como prática de desenvolvimento web e engenharia de simulações físicas, construindo as mecânicas fundamentais de um jogo de tiro ao alvo com blocos usando p5.js e Matter.js.
