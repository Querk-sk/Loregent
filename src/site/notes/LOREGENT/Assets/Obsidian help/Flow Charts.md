---
{"dg-publish":true,"permalink":"/loregent/assets/obsidian-help/flow-charts/","noteIcon":""}
---


### Flow Charts

V obsidiane funguje mermaid charts.
- [Flowcharts Syntax | Mermaid](https://mermaid.js.org/syntax/flowchart.html) Je tam aj syntax. Stačí ti flow
- [Advanced formatting syntax - Obsidian Help](https://help.obsidian.md/Editing+and+formatting/Advanced+formatting+syntax#Linking+files+in+a+diagram)

Possible FlowChart orientations are:

- TB - Top to bottom
- TD - Top-down/ same as top to bottom
- BT - Bottom to top
- RL - Right to left
- LR - Left to right

---

```mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

```

```mermaid
flowchart TD
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]

```

```mermaid
graph BT

A[krajina času]
B(Slide coagulase)
C(Tube coagulase)
D(S. aureus)
E(Micrococcus or CONS)

A --> B
B --(+)--> D
B --(-)--> C
C --(+)--> D
C --(-)--> E

class A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z internal-link;
```

[Flowcharts Syntax | Mermaid](https://mermaid.js.org/syntax/flowchart.html) 
- class A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z internal-link == všetko má linky
- class meno internal-link == iba jedna vec má link

---

```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid

```
[Mindmap | Mermaid](https://mermaid.js.org/syntax/mindmap.html)

---

```mermaid
timeline
    title Timeline of Industrial Revolution
    section 17th-20th century
        Industry 1.0 : Machinery, Water power, Steam <br>power
        Industry 2.0 : Electricity, Internal combustion engine, Mass production
        Industry 3.0 : Electronics, Computers, Automation
    section 21st century
        Industry 4.0 : Internet, Robotics, Internet of Things
        Industry 5.0 : Artificial intelligence, Big data, 3D printing

```
[Timeline Diagram | Mermaid](https://mermaid.js.org/syntax/timeline.html)

---

### LINK : 
[[LOREGENT/Assets/Structure/Map of content/MOC - Obsidian Help\|MOC - Obsidian Help]]