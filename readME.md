# UVM Testbench Generator Templates

# UVM Auto Generator 🚀

![UVM Logo](https://www.accellera.org/images/logo/uvm_logo.png)  
*Automated UVM Testbench Generation System*

## 📌 Overview

The **UVM Auto Generator** is a Python-based tool that automatically creates complete UVM (Universal Verification Methodology) testbenches from RTL module definitions. It significantly reduces verification setup time from days to minutes.

## ✨ Key Features

- 🔍 **Automatic RTL Analysis**  
  Parses Verilog/SystemVerilog modules to extract:
  - Input/output ports
  - Parameters
  - Clock/reset signals

- 🏗️ **Complete UVM Structure Generation**  
  Creates all UVM components:
  ```mermaid
  graph LR
    A[Interface] --> B[Transaction]
    B --> C[Driver]
    B --> D[Monitor]
    C & D --> E[Agent]
    E --> F[Environment]
    F --> G[Test Cases]

## 📂 Template Categories

### 1. 🏗️ Core UVM Components
| Template File | Description |
|--------------|-------------|
| `interface.sv.j2` | SystemVerilog interface with modports for DUT connection |
| `transaction.sv.j2` | Base UVM transaction class with all DUT signals |
| `driver.sv.j2` | UVM driver for stimulus generation |
| `monitor.sv.j2` | UVM monitor for response capture |
| `agent.sv.j2` | UVM agent container (driver + monitor + sequencer) |
| `env.sv.j2` | Top-level UVM environment |
| `test.sv.j2` | Base test class with configuration methods |
| `top_tb.sv.j2` | Testbench top module with clock/reset generation |

### 2. 🧪 Test Sequences
| Template File | Description |
|--------------|-------------|
| `basic_sequence.sv.j2` | Simple random sequence |
| `random_sequence.sv.j2` | Advanced constrained-random sequence |
| `corner_case_sequence.sv.j2` | Boundary condition tests |
| `reset_sequence.sv.j2` | Reset verification sequence |

### 3. 🔍 Verification Components
| Template File | Description |
|--------------|-------------|
| `scoreboard.sv.j2` | Result comparison checker |
| `coverage.sv.j2` | Functional coverage implementation |
| `config.sv.j2` | Environment configuration class |

### 4. 📊 Documentation
| Template File | Description |
|--------------|-------------|
| `README.md.j2` | Auto-generated technical documentation |

### 5. ⚙️ Automation Scripts
| Template File | Description |
|--------------|-------------|
| `compile.do.j2` | Modelsim/Questa compilation script |
| `run.do.j2` | Simulation run script with multi-seed support |
| `Makefile.j2` | Alternative build automation |

## 🛠️ Usage

1. Place templates in `templates/` directory
2. Run generator:
```bash
python uvm_auto_gen.py


## Dependency Graph

graph TD
    A[interface.sv] --> B[transaction.sv]
    B --> C[driver.sv]
    B --> D[monitor.sv]
    C & D --> E[agent.sv]
    E --> F[env.sv]
    F --> G[test.sv]
    G --> H[sequences]
    H --> I[top_tb.sv]
