
# Assembler and Simulator Testing Framework

This project provides an automated testing framework to evaluate the correctness of student-written **Assembler** and **Simulator** implementations. The tests are categorized into **simple** and **hard** levels and are conducted independently for the assembler and simulator modules.

---

## 🧾 Directory Structure

```

Assembler\_Simulator/
├── SimpleAssembler/
│   └── Assembler.py              # Your assembler implementation
├── SimpleSimulator/
│   └── Simulator.py              # Your simulator implementation
├── tests/
│   ├── assembly/
│   │   ├── simpleBin/            # Input assembly codes (simple)
│   │   ├── hardBin/              # Input assembly codes (hard)
│   │   ├── errorGen/             # Malformed input codes
│   │   ├── bin\_s/                # Reference machine code (for simpleBin)
│   │   ├── bin\_h/                # Reference machine code (for hardBin)
│   │   ├── user\_bin\_s/           # Student-generated machine code (simple)
│   │   └── user\_bin\_h/           # Student-generated machine code (hard)
│   ├── bin/                      # Student-generated simulator trace output
│   └── traces/                   # Reference simulator traces
├── automatedTesting/
├── readme.txt
└── src/
└── main.py                   # Testing driver script

````

---

## 🧪 Test Cases Breakdown

### Assembler

| Type   | Count | Weight per Test |
|--------|-------|------------------|
| Simple | 10    | 0.1              |
| Hard   | 5     | 0.2              |

### Simulator

| Type   | Count | Weight per Test |
|--------|-------|------------------|
| Simple | 5     | 0.4              |
| Hard   | 5     | 0.8              |

---

## ⚙️ How to Use

### 🔧 Assembler

Your assembler should take an input assembly code file and produce the corresponding machine code file.

**Command Format:**
```bash
$ python3 Assembler.py <input_assembly_path> <output_machine_code_path>
````

**Steps:**

1. Rename your assembler file to `Assembler.py`.
2. Place it inside the `SimpleAssembler/` folder.

**Run Tests:**

* **Linux**:

  ```bash
  $ python3 src/main.py --no-sim --linux
  ```
* **Windows**:

  ```bash
  > python3 src\main.py --no-sim --windows
  ```

---

### 🧮 Simulator

Your simulator should take an input machine code file and produce an execution trace file.

**Command Format:**

```bash
$ python3 Simulator.py <input_machine_code_path> <output_trace_path>
```

**Steps:**

1. Rename your simulator file to `Simulator.py`.
2. Place it inside the `SimpleSimulator/` folder.

**Run Tests:**

* **Linux**:

  ```bash
  $ python3 src/main.py --no-asm --linux
  ```
* **Windows**:

  ```bash
  > python3 src\main.py --no-asm --windows
  ```

---

## 💡 Notes

* All input/output files **must use `.txt` extensions**.
* This framework is intended for **Python 3.x users only**.
* Ensure that your program strictly follows I/O formatting rules.

---

## 📌 Disclaimer

This framework is for educational testing purposes only. Test cases are structured to encourage modularity and robustness in assembler and simulator implementations.

---
