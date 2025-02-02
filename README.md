# <p align="center">push_swap</p>

> _Ce projet vous demande de trier des données dans une pile en utilisant un ensemble limité d'instructions, et avec le moins d'opérations possibles._
>
> _Pour le réussir, vous devrez manipuler différents algorithmes de tri et choisir la solution la plus appropriée pour un classement optimal des données._
>
> _Les algorithmes de tri et leur complexité sont des sujets classiques lors des entretiens d'embauche. Profitez de cette occasion pour approfondir sérieusement vos connaissances._
>
> _Les objectifs de ce projet incluent la rigueur, la pratique du langage C et l'utilisation d'algorithmes élémentaires, en particulier la compréhension de leur complexité._
>
> _Trier des valeurs est simple, mais les trier le plus rapidement possible est plus complexe, car un même algorithme de tri peut ne pas être le plus efficace d'une configuration d'entiers à une autre._

| Instruction                  |                        Description                         |
| ---------------------------- | :--------------------------------------------------------: |
| **`sa`** (swap a)            | Intervertit les 2 premiers éléments au sommet de la pile a |
| **`sb`** (swap b )           | Intervertit les 2 premiers éléments au sommet de la pile b |
| **`ss`**                     |             **`sa`** et **`sb`** en même temps             |
| **`pa`** (push a)            |  Prend le premier élément au sommet de b et le met sur a   |
| **`pb`** (push b)            |  Prend le premier élément au sommet de a et le met sur b   |
| **`ra`** (rotate a)          |     Le premier élément de la pile a devient le dernier     |
| **`rb`** (rotate b)          |     Le premier élément de la pile b devient le dernier     |
| **`rr`**                     |             **`ra`** et **`rb`** en même temps             |
| **`rra`** (reverse rotate a) |     Le dernier élément de la pile a devient le premier     |
| **`rrb`** (reverse rotate b) |     Le dernier élément de la pile b devient le premier     |
| **`rrr`**                    |            **`rra`** et **`rrb`** en même temps            |

## Preview

![](https://github.com/Skalyaev/push_swap/blob/main/preview.gif)

> Visualieur [ici](https://gitlab.com/hydrasho/visualizer-push-swap)

## Install

```bash
sudo apt update -y
sudo apt install -y gcc
sudo apt install -y make
```

```bash
mkdir -p $HOME/.local/bin
mkdir -p $HOME/.local/src
mkdir -p $HOME/.local/include
```

```bash
name=pushswap

git clone https://github.com/Skalyaeve/push_swap.git $name
cd $name && make && make clean

ln -s $PWD/$name $HOME/.local/bin/$name
ln -s $PWD/src $HOME/.local/src/$name
ln -s $PWD/include $HOME/.local/include/$name
```

## Usage

```bash
export PATH=$HOME/.local/bin:$PATH
pushswap <numbers>
```

## Uninstall

```bash
name=pushswap

rm -rf $name
rm $HOME/.local/bin/$name
rm $HOME/.local/src/$name
rm $HOME/.local/include/$name
```
