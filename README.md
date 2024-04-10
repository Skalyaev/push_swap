# Push_swap
> *Ce projet vous demande de trier des données dans une pile en utilisant un ensemble limité d'instructions, et avec le moins d'opérations possibles. Pour le réussir, vous devrez manipuler différents algorithmes de tri et choisir la solution la plus appropriée pour un classement optimal des données.*

Les algorithmes de tri et leur complexité sont des sujets classiques lors des entretiens d'embauche. Profitez de cette occasion pour approfondir sérieusement vos connaissances.

Les objectifs de ce projet incluent la rigueur, la pratique du langage C et l'utilisation d'algorithmes élémentaires, en particulier la compréhension de leur complexité.

Trier des valeurs est simple, mais les trier le plus rapidement possible est plus complexe, car un même algorithme de tri peut ne pas être le plus efficace d'une configuration d'entiers à une autre.

| Instruction | Description |
|-|-|
| sa (swap a) | Intervertit les 2 premiers éléments au sommet de la pile a |
| Ne fait rien s’il n’y en a qu’un ou aucun |
| sb (swap b ) | Intervertit les 2 premiers éléments au sommet de la pile b |
| Ne fait rien s’il n’y en a qu’un ou aucun |
| ss | sa et sb en même temps |
| pa (push a) | Prend le premier élément au sommet de b et le met sur a |
| Ne fait rien si b est vide |
| pb (push b) | Prend le premier élément au sommet de a et le met sur b |
| Ne fait rien si a est vide |
| ra (rotate a) | Décale d’une position vers le haut tous les élements de la pile a |
| Le premier élément devient le dernier |
| rb (rotate b) | Décale d’une position vers le haut tous les élements de la pile b |
| Le premier élément devient le dernier |
| rr | ra et rb en même temps |
| rra (reverse rotate a) | Décale d’une position vers le bas tous les élements de
| la pile a. Le dernier élément devient le premier |
| rrb (reverse rotate b) | Décale d’une position vers le bas tous les élements de
| la pile b. Le dernier élément devient le premier |
| rrr | rra et rrb en même temps |

## Preview
![](https://github.com/Skalyaeve/images/blob/main/screenshot/pushswap.gif)
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
link=Skalyaeve/push_swap
name=pushswap

git clone https://github.com/$link.git $name
cd .. && make && make clean

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

rm -r $name
rm $HOME/.local/bin/$name
rm $HOME/.local/src/$name
rm $HOME/.local/include/$name
```
