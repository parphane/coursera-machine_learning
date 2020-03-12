# Notations
## Definitions
| Notation | Definition | Example
| :-: | - | -
| L | Total number of layers | -
| S<sub>l</sub> | Number of units in layer l | -
| S<sub>L</sub> | Number of units in output layer | -
| K | Number of units in output layer | 1&le;K&le;2&ensp;Binary
| | |

## Example
### Neural network
```plantuml
@startuml
digraph nn {
    rankdir=LR
    node [shape=circle, fixedsize=true, label="",color=orange]
    splines=line
    
    subgraph cluster_1 {
        node [color=green]
        label = "layer 1\nInput layer\n";
        color=transparent;
        u11 u12 u13
    }
    subgraph cluster_2 {
        label = "layer 2";
        color=transparent;
        u21 u22 u23 u24 u25
    }
    subgraph cluster_3 {
        label = "layer 3";
        color=transparent;
        u31 u32 u33 u34 u35
    }
    subgraph cluster_4 {
        node [color=red]
        label = "layer 4\n Output layer";
        color=transparent;
        u41 u42 u43 u44
    }
    u11, u12, u13 -> u21,u22,u23,u24,u25 -> u31,u32,u33,u34,u35 -> u41,u42,u43,u44
}
@enduml
```
### Notations values
| Notation | Value
| - | -
| L | 4
| S<sub>1</sub> | 3
| S<sub>2</sub> | 4
| S<sub>3</sub> | 5
| S<sub>4</sub> / S<sub>L</sub> | 4
