# Hotspot Patterns

Artigo: [https://apps.dtic.mil/sti/tr/pdf/ADA621415.pdf](https://apps.dtic.mil/sti/tr/pdf/ADA621415.pdf)

## Conceitos

Um _Design Rule Space_ é composto por um conjunto de arquivos e relacões, como herança, agregação e dependência. Tais arquivos agrupados formam uma _Design Rule Hierarchy_, com as seguintes caracteristícas: quanto mais no topo da camada mais eles influenciam suas camadas inferiores, camadas do topo não devem ser influenciadas por suas camadas inferiores e arquivos na mesma camada são agrupados em módulos mutuamente independentes.

A arquitetura de um software é o resultado do _overlapping_ de _DRSpaces_.

Portanto, os autores derivaram dessas definições uma matriz, chamada de _Design Structure Matrix_, que possibilitam avaliar a dependência de cada arquivo com cada outro do projeto.

## _Unstable Interface_

Se um arquivo com uma influência muito alta (alto _fan-out_) é alterado frequentemente junto a outros arquivos na hierarquia, tal arquivo é uma interface instável. O problema é que alterações nesse arquivo se propagarão para muitos outros arquivos que dependem dele.

## _Implicit Cross-module Dependency_

Ocorre quando dois arquivos em módulos diferentes mudam juntos, mas não há uma dependência explícita (como `include` ou `import`) entre eles. Isso sugere um acoplamento oculto que não é capturado pela arquitetura, podendo levar a efeitos cascata inesperados quando um dos arquivos é modificado.

## _Unhealthy Inheritance Hierarchy_

Ocorre quando uma superclasse e uma subclasse mudam juntas com frequência. Isso pode indicar que a abstração da superclasse é fraca ou que a subclasse está quebrando o Princípio de Substituição de Liskov. O problema é que alterações na superclasse exigem alterações na subclasse, o que anula o propósito da herança.

## _Cross-Module Cycle_

Acontece quando há um ciclo de dependências entre arquivos que pertencem a módulos diferentes. Por exemplo, o arquivo `A` no módulo `M1` depende do arquivo `B` no módulo `M2`, e `B` depende de `A`. Isso viola a hierarquia do _Design Rule Space_, pois cria um acoplamento forte entre os módulos, tornando-os difíceis de entender, testar e reutilizar de forma independente.

## _Cross-Package Cycle_

Similar ao _Cross-Module Cycle_, mas ocorre em um nível mais alto de abstração, entre pacotes ou subsistemas. Um ciclo de dependência entre pacotes indica um problema arquitetural grave, pois subsistemas inteiros se tornam interdependentes, dificultando a manutenção e evolução do sistema.

## Validação dos Resultados

O artigo cita que foram utilizados 9 projetos open-source e 1 projeto comercial, que não foi divulgado por razões de confidencialida. O análista responsável pelo projeto comercial concordou com os resultados tragos pelos autores e cita que planejam a refatoração dos problemas encontrados.
