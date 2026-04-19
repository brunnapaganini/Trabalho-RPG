# The Night - Mini-RPG de Aventuras

The Night é um projeto de jogo de aventura interativo desenvolvido em Java, utilizando a biblioteca Swing. O jogo é inspirado no conceito de Livros-Jogos (gamebooks), onde o jogador assume o papel de um protagonista cujas escolhas determinam o rumo da história e o sucesso em combates estratégicos.

## Objetivos do Projeto

Este projeto foi desenvolvido para aplicar os pilares da Programação Orientada a Objetos (POO):
* **Abstração e Herança**: Uso de classes abstratas para definir a base dos aventureiros.
* **Polimorfismo**: Diferentes comportamentos para habilidades especiais de cada classe.
* **Interfaces**: Implementação de contratos de ações obrigatórias para personagens.
* **GUI (Graphic User Interface)**: Criação de uma interface visual rica para interação com o usuário.

## Estrutura de Telas e Fluxo

O jogo é composto por uma sequência de interfaces que gerenciam desde a criação do personagem até os confrontos finais:

1.  **TelaJogar**: Tela de configuração inicial (Nome, Classe e Rolagem de Atributos).
2.  **TelaInicio**: Introdução à narrativa e primeira decisão estratégica.
3.  **Fluxo de Exploração**: Telas `TelaPrimeira`, `TelaSegunda`, `TelaSegunda2` e `TelaTerceira` gerenciam o progresso da história e ramificações de escolhas.
4.  **Sistema de Combate**: 
    * `TelaBatalhaUm`: Primeiro encontro/combate.
    * `TelaBatalhaDois`: Confronto contra o Guardião da Cripta.
    * `TelaBatalhaTres`: Enfrentamento final contra o Lich (Guardião Final).

## Regras de Negócio Implementadas

### Personagens e Atributos
* **Classes Disponíveis**: Bárbaro, Mago, Arqueiro e Ladino.
* **Rolagem de Dados (RN02/RN03)**: Atributos iniciais como Vida e Mana são determinados por rolagens de dados antes do início da partida.
* **Especialização (RN11-RN18)**:
    * **Bárbaro**: +2 de Força; Habilidade *Fúria* (+50% de dano).
    * **Mago**: +3 de Mana; Habilidade *Magia* (Dano baseado em 2x Força).
    * **Arqueiro**: +3 de Agilidade; Habilidade *Tiro Preciso* (Aumenta acerto).
    * **Ladino**: +4 de Agilidade; Habilidade *Evasão* (Chance de fuga ou contra-ataque).

### Combate e Narrativa
* **Ações de Turno**: Durante as telas de batalha, o jogador pode Atacar, Usar Habilidade, Usar Item ou Fugir.
* **Decisões Narrativas**: Cada cenário apresenta no mínimo duas opções que impactam os atributos ou levam a inimigos mais fortes.
* **Persistência**: O jogo permite reiniciar a partida sem fechar a aplicação (reset de atributos).

## Requisitos Técnicos

* **Linguagem**: Java 8 ou superior.
* **Componentes Swing**: JFrame, JProgressBar (barras de vida/mana), JTextArea (narrativa), JButton e JOptionPane.
* **Arquivos Obrigatórios**:
    * `Personagem.java` (Interface)
    * `Aventureiro.java` (Classe Abstrata)
    * `Inimigo.java`
    * `Dados.java` (Gerador de números aleatórios)
    * `Jogo.java` (Classe Principal)

## Como Rodar o Projeto

1. Clone o repositório e importe as classes para sua IDE (NetBeans recomendado).
2. Verifique se as classes concretas (`Barbaro.java`, `Mago.java`, etc.) estão devidamente vinculadas à `Aventureiro.java`.
3. **Ajuste de Caminhos**: Como o projeto utiliza ícones e backgrounds, verifique os caminhos das imagens nos métodos `initComponents()` de cada tela para que correspondam ao seu diretório local.
4. Execute o arquivo `Jogo.java` ou `TelaJogar.java`.

---
**Desenvolvimento**: Brunna Paganini

**Contexto**: Trabalho Acadêmico de Programação Orientada a Objetos
