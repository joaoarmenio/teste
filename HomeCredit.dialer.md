# Home Credit Project

## Introduction

The Home Credit system has the main objetive to provide dialers to attend 5 locations:

- India
- Vietnam
- Philippines
- Indonesia
- Kazakhstan

## Basic Requirements

- CMS Dialer - supports 300 channels and 100000 calls per hour
- OSCC supports 1500 agents and 24000 calls per hour
- OSV  - for now an assumption of 100 cps raw calls and 6.7 cps ACD calls.


## Architecture

### India

- 6 million calls per day --> 600000 cph --> 166.7 cps
- 27000 OSCC cph (4.5% success rate)
- 3200 agents

```mermaid
graph TD
    A[Central Dialer] --> B[CMS Dialer 1]
    A --> C[CMS Dialer 2]
    A --> D[CMS Dialer 3]
    A --> E[CMS Dialer 4]
    A --> F[CMS Dialer 5]
    A --> G[CMS Dialer 6]
    B --> M[OSCC 1]
    C --> M
    D --> M
    E --> N[OSCC 2]
    F --> N
    G --> N
    B --> O1
    C --> O1
    D --> O1
    E --> O2
    F --> O2
    G --> O2
    M --> O1[OSV 1]
    N --> O2[OSV 2]
```

### Vietnam

- 4 million calls per day --> 400000 cph --> 111.1 cps
- 18000 cph (4.5% success rate)
- 900 agents

```mermaid
graph TD
    A[Central Dialer] --> B[CMS Dialer 1]
    A --> C[CMS Dialer 2]
    A --> E[CMS Dialer 3]
    A --> F[CMS Dialer 4]
    B --> M[OSCC 1]
    C --> M
    E --> N[OSCC 2]
    F --> N
    B --> O1
    C --> O1
    E --> O2
    F --> O2
    M --> O1[OSV 1]
    N --> O2[OSV 2]
```

### Philippines

- 11 million calls per day --> 1100000 cph --> 305.6 cps
- 49500 OSCC cph (4.5% success rate)
- 1300 agents

```mermaid
graph TD
    A[Central Dialer] --> B[CMS Dialer 1]
    A --> C[CMS Dialer 2]
    A --> D[CMS Dialer 3]
    A --> E[CMS Dialer 4]
    A --> F[CMS Dialer 5]
    A --> G[CMS Dialer 6]
    A --> H[CMS Dialer 7]
    A --> I[CMS Dialer 8]
    A --> J[CMS Dialer 9]
    A --> K[CMS Dialer 10]
    A --> L[CMS Dialer 11]
    B --> M[OSCC 1]
    C --> M
    D --> M
    E --> M
    F --> N[OSCC 2]
    G --> N
    H --> N
    I --> N
    J --> P[OSCC 3]
    K --> P
    L --> P
    B --> O1
    C --> O1
    D --> O1
    E --> O1
    F --> O2
    G --> O2
    H --> O2
    I --> O2
    J --> O3
    K --> O3
    L --> O3
    M --> O1[OSV 1]
    N --> O2[OSV 2]
    P --> O3[OSV 3]
```

### Indonesia

- 12 million calls per day --> 1200000 cph --> 333.3 cps
- 54000 OSCC cph (4.5% success rate)
- 900 agents

```mermaid
graph TD
    A[Central Dialer] --> B[CMS Dialer 1]
    A --> C[CMS Dialer 2]
    A --> D[CMS Dialer 3]
    A --> E[CMS Dialer 4]
    A --> F[CMS Dialer 5]
    A --> G[CMS Dialer 6]
    A --> H[CMS Dialer 7]
    A --> I[CMS Dialer 8]
    A --> J[CMS Dialer 9]
    A --> K[CMS Dialer 10]
    A --> L[CMS Dialer 11]
    A --> L2[CMS Dialer 12]
    B --> M[OSCC 1]
    C --> M
    D --> M
    E --> M
    F --> N[OSCC 2]
    G --> N
    H --> N
    I --> N
    J --> P[OSCC 3]
    K --> P
    L --> P
    L2 --> P
    B --> O1
    C --> O1
    D --> O1
    E --> O1
    F --> O2
    G --> O2
    H --> O2
    I --> O2
    J --> O3
    K --> O3
    L --> O3
    L2 --> O3
    M --> O1[OSV 1]
    N --> O2[OSV 2]
    P --> O3[OSV 3]
```

### Kazakhstan

- 1 million calls per day --> 100000 cph --> 27.8 cps
- 4500 OSCC cph (4.5% success rate)
- 600 agents

```mermaid
graph TD
    A[Central Dialer] --> B[CMS Dialer 1]
    A --> C[CMS Dialer 2]
    B --> M[OSCC 1]
    C --> M
    M --> O[OSV]
 ```
