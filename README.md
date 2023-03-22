# mymermaid
try out mermaid

```mermaid
graph TD
    A{Does your flowchart have arrows?} --> B[No]
    A --> |TEXT WITHIN THE ARROW| C[yes]
    B <--> D(Add them already)
    C --> E(Yay, what a great flowchart!)
    D -.->|you can even add text to them| A
    
    subgraph warehouse
        H --> G
        H --> I
    end
```
```mermaid 
stateDiagram-v2
        s1 --> s2: A transition
```
# SECOND

```mermaid
flowchart TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
    one --> two
    three --> two
    two --> c2
```

# THIRD
```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

# FOUR

```mermaid
sequenceDiagram
    participant dotcom
    participant iframe
    participant viewscreen
    dotcom->>iframe: loads html w/ iframe url
    iframe->>viewscreen: request template
    viewscreen->>iframe: html & javascript
    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```

# NODES & LINKS
```mermaid
graph TD
%% Nodes
    0[Key Variable]
    1[Top Variable 1]
    2[Top Variable 2]
    3[Top Variable 3]
    31[Sub Variable 1]
    32[Sub Variable 2]
    321[Element 1]
    322[Element 2]

%% Links
    0 --- 1
    0 --- 2
    0 --- 3
    3 --- 31
    3 --- 32
    32 --- 321
    32 --- 322

%% Nodes
    0[Key Variable<br>Target: 100, Actual: 80]
    1[Top Variable 1<br>Tgt: 20, Act: 20]
    2[Top Variable 2<br>Tgt: 30, Act: 30]
    3[Top Variable 3<br>Tgt: 50, Act: 30]
    31[Sub Variable 1<br>Tgt: 25, Act: 25]
    32[Sub Variable 2<br>Tgt: 25, Act: 5]
    321[Element 1<br>Tgt: 20, Act: 1]
    322[Element 2<br>Tgt: 5, Act: 4]

%% Defining the styles
    classDef Red fill:#FF9999;
    classDef Amber fill:#FFDEAD;
    classDef Green fill:#BDFFA4;

%% Assigning styles to nodes
    class 3,32,321 Red;
    class 322 Amber;
    class 1,2,31 Green;
    
%% Changing color of links [NOTE: Link arrows will remain black]
    linkStyle default fill: none, stroke: grey;
    
```

# 6
```mermaid
graph TD
class diagram
  class User {
    +createProject()
    +assignTask()
    +trackProgress()
  }
  class Project {
    +setTitle(title: String)
    +setDescription(desc: String)
  }
  class Task {
    +setTitle(title: String)
    +setDescription(desc: String)
    +setAssignedTo(assignedTo: User)
  }
  class Progress {
    +setPercentage(percentage: Number)
    +setDate(date: Date)
  }
  User --> Project
  User --> Task
  Task --> Progress
```
```mermaid
gantt
axisFormat %e%b
todayMarker on
section Activity 1
    TaskA	: TA, 2021-06-14, 4d
    TaskB	: TB, after TA, 2d
section Activity 2
    TaskC	: TC, after TA, 3d
    TaskD	: TD, after TC, 2d
section Activity 3
    TaskE	: TE, after TD, 1d
    TaskF	: TF, after TE, 2d
