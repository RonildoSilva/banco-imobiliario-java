# Banco Imobiliário em Java

> Modelagem do jogo Banco Imobiliário como exercício de padrões de projeto: Singleton, Factory, Strategy, Observer e enum com comportamento por casa do tabuleiro.

![status](https://img.shields.io/badge/status-incompleto-orange) ![java](https://img.shields.io/badge/Java-8-blue) ![patterns](https://img.shields.io/badge/padrões-GoF-lightgrey)

## Sobre
Trabalho da disciplina de Padrões de Projeto (2018). O foco foi a arquitetura do domínio a partir do manual do jogo; a interface gráfica com a biblioteca jPlay ficou apenas referenciada.

| Padrão | Onde |
|---|---|
| Singleton | `Cartas`: baralho único de Sorte/Revés |
| Factory | `CartaFactory` cria `CartaSorte` ou `CartaReves` por `TipoCarta` |
| Strategy | `IMonetiza` / `ControllerMonetiza` aplicam créditos e débitos |
| Observer | `ISubject` / `IObserver` / `JogadorObserver` acompanham o saldo do jogador |
| Enum com comportamento | `TipoAcaoCasa` executa a ação de cada tipo de casa (sorte/revés, imóvel, imposto...) |

## Estrutura de pastas
```text
src/Main.java                 demonstração
src/ufc/                      Casa, Casas, Dado, TipoAcaoCasa, interfaces
src/ufc/carta/                Carta, CartaSorte, CartaReves, CartaFactory, Cartas, TipoCarta
src/ufc/jogador/              Jogador, Propriedade, RepositorioPropriedades, JogadorObserver
src/ufc/util/CircularArrayList.java  tabuleiro circular
lib/                          jPlay
```

## Como executar
```bash
javac -cp lib/* -d out $(find src -name "*.java") && java -cp "out:lib/*" Main
```

## Status
Incompleto: o domínio e os padrões estão implementados, mas não há laço de jogo nem interface.

## Autor
Ronildo Silva · ronildo.comp@gmail.com
