# Assignment 5 – CO5
## Reliable Software with Runtime Polymorphism and Exceptions

**Student:** S. Adithiyan  
**Register Number:** 1925260197  
**Course:** B.Tech – Artificial Intelligence and Machine Learning  
**GitHub Repository:** [https://github.com/Adithiyan-1005/DSA0112-1925260197-5](https://github.com/Adithiyan-1005/DSA0112-1925260197-5)

> The assignment PDF specifies the repository name `DSA01-1925260197-Assignment5`. The supplied repository URL currently uses `DSA0112-1925260197-5`. Confirm with the faculty whether the current name is acceptable or rename it to match the PDF.

## Compiler information
- **Compiler:** GNU g++
- **C++ standard:** C++17
- **Compiler version:** Record the version installed on the computer used for the final tests. Check with `g++ --version`.
- **Standard compile command:** `g++ -std=c++17 -Wall -Wextra source.cpp -o program`
- **Run:** `./program` (Linux/macOS) or `program.exe` (Windows)

For benchmark programs, compile with optimisation:
```bash
g++ -std=c++17 -O2 -Wall -Wextra benchmark.cpp -o benchmark
./benchmark
```

For memory-safety tests:
```bash
g++ -std=c++17 -Wall -Wextra -fsanitize=address -fno-omit-frame-pointer source.cpp -o program_asan
./program_asan
```

## Suggested repository structure
```text
DSA0112-1925260197-5/
├── README.md
├── Assignment_Report.pdf
├── Task01/
│   ├── design.md
│   └── evidence/
├── Task02/
│   ├── runtime_binding.cpp
│   └── evidence/
├── Task03/
│   ├── payer_design.md
│   └── evidence/
├── Task04/
│   ├── exception_design.md
│   └── evidence/
├── Task05/
│   ├── stack_unwinding.cpp
│   └── evidence/
├── Task06/
│   ├── polymorphic_billing.cpp
│   ├── input.txt
│   └── evidence/
├── Task07/
│   ├── error_tests.cpp
│   ├── input.txt
│   └── evidence/
├── Task08/
│   ├── benchmark.cpp
│   └── evidence/
└── Task09/
    ├── final_extension.cpp
    └── evidence/
```

The PDF groups its work under Tasks A1–A5 and B1–B4. The folders above are a suggested organisation; keep any additional subtask files inside the corresponding folder and use the exact task labels from the PDF in filenames.

## Task summaries
| PDF section | Work to include |
|---|---|
| A1 | Common Bill interface, abstract hierarchy, UML, daily-total pseudocode, switch alternative and complexity |
| A2 | Early/late binding, conceptual vtables, virtual destructor, predicted output and dynamic-cast alternative |
| A3 | Abstract Payer interface, SelfPay, Insurance, GovernmentScheme, extension and callable alternative |
| A4 | Error catalogue, exception hierarchy, throw/noexcept decisions, return-code alternative |
| A5 | Catch/log/rethrow plan, stack unwinding, RAII, predicted output and manual-cleanup comparison |
| B1 | Completed polymorphic bill program, hand-checked totals, tests, runtime-binding and destructor experiments |
| B2 | Invalid-input tests, allocation-failure test where safely feasible, predicted output, completed claim code and optional comparison |
| B3 | Same-data virtual/switch/variant benchmarks and exception-versus-return-code measurements |
| B4 | Add a bill type and payer, sanitizer evidence, production decision and plug-in/rule alternative |

## Build and run each program
From the relevant task folder:
```bash
g++ -std=c++17 -Wall -Wextra filename.cpp -o program
./program
```
For each program, record the exact command and actual output in a text file. Save genuine terminal screenshots in that task's `evidence/` folder.

## Testing and evidence
- Include normal, boundary and invalid-input test cases.
- For output-prediction questions, write the predicted output in the report **before** executing the program; then record the actual output and explain any difference.
- Use `-O2` for performance comparisons and report repeated measurements (preferably median), machine/OS details and compiler version.
- Use AddressSanitizer for resource-safety tests. Record the actual diagnostic or clean run; do not invent results.
- Do not force an enormous allocation on a shared or important machine. If testing `std::bad_alloc`, use a controlled test environment and document the limitation if the operating system overcommits memory.

## Progressive Git commits
Make a separate meaningful commit after completing each task, for example:
```bash
git add Task01
git commit -m "Complete Task A1 bill hierarchy design"
git add Task02
git commit -m "Complete Task A2 runtime binding analysis"
```
Continue similarly for each task. Do not upload all work in one final commit.

## Submission
1. Check that every task folder contains the required source/design files and actual evidence.
2. Push the commits to the GitHub repository.
3. Ensure the repository is public or add the course faculty as a collaborator if private.
4. Put the repository URL on the report cover page.
5. Submit the report and repository link through Google Classroom.

**Academic integrity:** This is an individual assignment. Understand each program and be prepared to explain and modify it during the viva. All code must be compiled, executed and verified by the student.
