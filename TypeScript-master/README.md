# 🧠 TypeScript Algorithms & Data Structures

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Algorithms](https://img.shields.io/badge/Algorithms-FF6B6B?style=for-the-badge&logo=thealgorithms&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)

**A comprehensive collection of Algorithms & Data Structures implemented in TypeScript**

*80+ algorithms covering sorting, searching, graphs, dynamic programming, and more — all fully tested with Jest.*

</div>

---

## 📖 Table of Contents

- [🤔 What is this project?](#-what-is-this-project)
- [🆚 TypeScript vs JavaScript](#-typescript-vs-javascript)
- [🚀 Getting Started](#-getting-started)
- [📂 Project Structure](#-project-structure)
- [📦 Available Algorithms](#-available-algorithms)
- [🧪 Running Tests](#-running-tests)
- [📝 How to Add a New Algorithm](#-how-to-add-a-new-algorithm)
- [🎓 TypeScript for Beginners](#-typescript-for-beginners)
- [🤝 Contributing](#-contributing)

---

## 🤔 What is this project?

This project is an **educational library** containing **80+ algorithms** written in TypeScript. Its purpose is to:

- ✅ **Learn TypeScript** through hands-on practice
- ✅ **Understand Algorithms** commonly asked in coding interviews
- ✅ **Practice Data Structures** fundamentals
- ✅ **Compare TypeScript and JavaScript** and understand the differences

> 💡 **Note:** These implementations are for educational purposes. In production, use dedicated, optimized libraries for better performance and security.

---

## 🆚 TypeScript vs JavaScript

### Key Differences

| Feature | JavaScript 🟡 | TypeScript 🔵 |
|---|---|---|
| **Typing** | Dynamic — types are determined at runtime | Static — types are determined at compile time ✅ |
| **Error Detection** | Errors appear in the browser (Runtime) 😱 | Errors appear in the editor before running ✅ |
| **File Extension** | `.js` | `.ts` |
| **Execution** | Runs directly in browser or Node.js | Compiles to JavaScript first |
| **Learning Curve** | Easier to start with | Easier after learning JS |
| **Large Projects** | Harder to maintain | Much easier to manage ✅ |
| **Usage** | Frontend + Backend | Frontend + Backend (same!) |

### Practical Example from This Project

```typescript
// ✅ TypeScript — Clear and protected from errors
export function isSortedArray(arr: number[]): boolean {
    //                         ^^^^^^^^^^^  ^^^^^^^^
    //                         Type defined!  Return type defined!
    for (let i = 0; i < arr.length - 1; i++) {
        if (arr[i] >= arr[i + 1]) {
            return false;
        }
    }
    return true;
}

// If you try: isSortedArray("hello") ← Instant error! 🛑
```

```javascript
// ❌ JavaScript — No type safety
function isSortedArray(arr) {
    // You could pass a string and get no error!
    // isSortedArray("hello") ← Runs without any error 😱
    for (let i = 0; i < arr.length - 1; i++) {
        if (arr[i] >= arr[i + 1]) {
            return false;
        }
    }
    return true;
}
```

### 🏆 Which One Should You Choose?

| Situation | Recommendation |
|---|---|
| Complete beginner | Start with **JavaScript** first |
| Frontend development | **TypeScript + React** ✅ |
| Backend development | **TypeScript + Node.js** ✅ |
| Working at a company | **TypeScript** (most companies use it) ✅ |
| Small/personal project | **JavaScript** is sufficient |
| Large project / team | **TypeScript** is essential ✅ |

> 💡 **Tip:** Learn JavaScript first (1-2 weeks), then move to TypeScript. TypeScript is simply JavaScript + Types!

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or later
- [Git](https://git-scm.com/)
- A code editor — we recommend [VS Code](https://code.visualstudio.com/)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/tawfiq154/typescript-algorithms.git

# 2. Navigate to the project folder
cd typescript-algorithms

# 3. Install dependencies
npm install
```

### Quick Start

```bash
# Run all tests
npm test

# Run a specific test file
npx jest sorts/test/bubble_sort.test.ts

# Run a TypeScript file directly
npx ts-node sorts/bubble_sort.ts
```

---

## 📂 Project Structure

```
typescript-algorithms/
│
├── 📁 sorts/                  # Sorting algorithms (14 algorithms)
├── 📁 search/                 # Search algorithms (7 algorithms)
├── 📁 data_structures/        # Data structures (9 categories)
│   ├── 📁 stack/              #   Stack (LIFO)
│   ├── 📁 queue/              #   Queue (FIFO)
│   ├── 📁 list/               #   Linked List
│   ├── 📁 tree/               #   Binary Tree
│   ├── 📁 heap/               #   Heap / Priority Queue
│   ├── 📁 map/                #   Hash Map
│   ├── 📁 set/                #   Set
│   ├── 📁 tries/              #   Trie
│   └── 📁 disjoint_set/       #   Disjoint Set (Union-Find)
├── 📁 maths/                  # Math algorithms (41 algorithms)
├── 📁 graph/                  # Graph algorithms (10 algorithms)
├── 📁 dynamic_programming/    # Dynamic programming (3 algorithms)
├── 📁 backtracking/           # Backtracking (2 algorithms)
├── 📁 bit_manipulation/       # Bit manipulation (4 algorithms)
├── 📁 ciphers/                # Ciphers (1 algorithm)
├── 📁 other/                  # Miscellaneous (3 algorithms)
│
├── 📄 package.json            # Project configuration
├── 📄 tsconfig.json           # TypeScript configuration
├── 📄 jest.config.ts          # Test configuration
└── 📄 README.md               # You are here! 😄
```

---

## 📦 Available Algorithms

### 🔢 Sorting Algorithms

| Algorithm | Best Case | Worst Case | File |
|---|---|---|---|
| Bubble Sort | O(n) | O(n²) | `sorts/bubble_sort.ts` |
| Insertion Sort | O(n) | O(n²) | `sorts/insertion_sort.ts` |
| Selection Sort | O(n²) | O(n²) | `sorts/selection_sort.ts` |
| Merge Sort | O(n log n) | O(n log n) | `sorts/merge_sort.ts` |
| Quick Sort | O(n log n) | O(n²) | `sorts/quick_sort.ts` |
| Heap Sort | O(n log n) | O(n log n) | `sorts/heap_sort.ts` |
| Shell Sort | O(n log n) | O(n²) | `sorts/shell_sort.ts` |
| Counting Sort | O(n + k) | O(n + k) | `sorts/counting_sort.ts` |
| Cycle Sort | O(n²) | O(n²) | `sorts/cycle_sort.ts` |
| Gnome Sort | O(n) | O(n²) | `sorts/gnome_sort.ts` |
| Bogo Sort | O(n) | O(∞) 😅 | `sorts/bogo_sort.ts` |
| Swap Sort | O(n) | O(n²) | `sorts/swap_sort.ts` |
| Tree Sort | O(n log n) | O(n²) | `sorts/tree_sort.ts` |
| Quick Select | O(n) | O(n²) | `sorts/quick_select.ts` |

### 🔍 Search Algorithms

| Algorithm | Time Complexity | File |
|---|---|---|
| Linear Search | O(n) | `search/linear_search.ts` |
| Binary Search | O(log n) | `search/binary_search.ts` |
| Jump Search | O(√n) | `search/jump_search.ts` |
| Interpolation Search | O(log log n) | `search/interpolation_search.ts` |
| Exponential Search | O(log n) | `search/exponential_search.ts` |
| Fibonacci Search | O(log n) | `search/fibonacci_search.ts` |
| Sentinel Search | O(n) | `search/sentinel_search.ts` |

### 🌐 Graph Algorithms

| Algorithm | Use Case | File |
|---|---|---|
| Dijkstra | Shortest path (non-negative weights) | `graph/dijkstra.ts` |
| Bellman-Ford | Shortest path (handles negative weights) | `graph/bellman_ford.ts` |
| Floyd-Warshall | All-pairs shortest paths | `graph/floyd_warshall.ts` |
| Kruskal | Minimum Spanning Tree (MST) | `graph/kruskal.ts` |
| Prim | Minimum Spanning Tree (MST) | `graph/prim.ts` |
| Tarjan | Strongly Connected Components | `graph/tarjan.ts` |
| Kosaraju | Strongly Connected Components | `graph/kosajaru.ts` |
| Johnson | All-pairs shortest paths (sparse graphs) | `graph/johnson.ts` |
| Edmonds-Karp | Maximum Flow | `graph/edmonds_karp.ts` |
| Bipartite Graph | Bipartiteness check | `graph/bipartite_graph.ts` |

### 🏗️ Data Structures

| Structure | Description | Directory |
|---|---|---|
| Stack | LIFO — Last In, First Out | `data_structures/stack/` |
| Queue | FIFO — First In, First Out | `data_structures/queue/` |
| Linked List | Dynamic linear collection | `data_structures/list/` |
| Binary Tree | Hierarchical tree structure | `data_structures/tree/` |
| Heap | Priority Queue implementation | `data_structures/heap/` |
| Hash Map | Key-value storage | `data_structures/map/` |
| Set | Collection of unique elements | `data_structures/set/` |
| Trie | Prefix tree (for strings) | `data_structures/tries/` |
| Disjoint Set | Union-Find structure | `data_structures/disjoint_set/` |

### ➕ Math Algorithms (41 algorithms)

<details>
<summary>Click to expand the full list</summary>

| Algorithm | File |
|---|---|
| Factorial | `maths/factorial.ts` |
| Fibonacci | `maths/fibonacci.ts` |
| Prime Numbers | `maths/primes.ts` |
| Sieve of Eratosthenes | `maths/sieve_of_eratosthenes.ts` |
| GCD (Greatest Common Factor) | `maths/greatest_common_factor.ts` |
| LCM (Lowest Common Multiple) | `maths/lowest_common_multiple.ts` |
| Pascal's Triangle | `maths/pascals_triangle.ts` |
| Matrix Multiplication | `maths/matrix_multiplication.ts` |
| Binary Convert | `maths/binary_convert.ts` |
| Absolute Value | `maths/absolute_value.ts` |
| Armstrong Number | `maths/armstrong_number.ts` |
| Binomial Coefficient | `maths/binomial_coefficient.ts` |
| Calculate Mean | `maths/calculate_mean.ts` |
| Calculate Median | `maths/calculate_median.ts` |
| Degrees to Radians | `maths/degrees_to_radians.ts` |
| Radians to Degrees | `maths/radians_to_degrees.ts` |
| Digit Sum | `maths/digit_sum.ts` |
| Double Factorial | `maths/double_factorial_iterative.ts` |
| Euler Totient | `maths/euler_totient.ts` |
| Factors | `maths/factors.ts` |
| Find Min | `maths/find_min.ts` |
| Gaussian Elimination | `maths/gaussian_elimination.ts` |
| Hamming Distance | `maths/hamming_distance.ts` |
| Is Divisible | `maths/is_divisible.ts` |
| Is Even | `maths/is_even.ts` |
| Is Odd | `maths/is_odd.ts` |
| Is Leap Year | `maths/is_leap_year.ts` |
| Is Palindrome | `maths/is_palindrome.ts` |
| Is Square Free | `maths/is_square_free.ts` |
| Juggler Sequence | `maths/juggler_sequence.ts` |
| Number of Digits | `maths/number_of_digits.ts` |
| Perfect Cube | `maths/perfect_cube.ts` |
| Perfect Number | `maths/perfect_number.ts` |
| Perfect Square | `maths/perfect_square.ts` |
| Prime Factorization | `maths/prime_factorization.ts` |
| Pronic Number | `maths/pronic_number.ts` |
| Signum | `maths/signum.ts` |
| Square Root | `maths/square_root.ts` |
| Ugly Numbers | `maths/ugly_numbers.ts` |
| Zeller's Congruence | `maths/zellers_congruence.ts` |
| Aliquot Sum | `maths/aliquot_sum.ts` |

</details>

### 🧩 Other Categories

| Category | Algorithms |
|---|---|
| **Dynamic Programming** | Coin Change, Knapsack, Longest Common Subsequence (LCS) |
| **Backtracking** | All Combinations of Size K, Generate Parentheses |
| **Bit Manipulation** | Add Binary, Is Power of 2, Is Power of 4, Log Two |
| **Ciphers** | XOR Cipher |
| **Other** | Is Sorted Array, Parse Nested Brackets, Shuffle Array |

---

## 🧪 Running Tests

Every algorithm has its own test file inside a `test/` subdirectory:

```bash
# Run all tests
npm test

# Run tests for a specific category
npx jest sorts/
npx jest search/
npx jest maths/
npx jest graph/

# Run a test by name
npx jest --testNamePattern="bubble sort"

# Run with coverage report
npx jest --coverage
```

---

## 📝 How to Add a New Algorithm

### 1. Create the algorithm file

```typescript
// maths/my_algorithm.ts

/**
 * @function myAlgorithm
 * @description Describe what this algorithm does
 * @param {number} n - Description of the parameter
 * @returns {number} - Description of the return value
 * @example myAlgorithm(5) => 10
 */
export function myAlgorithm(n: number): number {
    // Your code here
    return n * 2;
}
```

### 2. Create the test file

```typescript
// maths/test/my_algorithm.test.ts
import { myAlgorithm } from "../my_algorithm";

describe("My Algorithm", () => {
    it("should return double the input", () => {
        expect(myAlgorithm(5)).toBe(10);
    });

    it("should handle zero", () => {
        expect(myAlgorithm(0)).toBe(0);
    });

    it("should handle negative numbers", () => {
        expect(myAlgorithm(-3)).toBe(-6);
    });
});
```

### 3. Run the test

```bash
npx jest maths/test/my_algorithm.test.ts
```

---

## 🎓 TypeScript for Beginners

### Essential Concepts

```typescript
// 1️⃣ Basic Types
let name: string = "Tawfiq";
let age: number = 25;
let isStudent: boolean = true;
let scores: number[] = [90, 85, 95];

// 2️⃣ Functions with Types
function add(a: number, b: number): number {
    return a + b;
}

// 3️⃣ Interfaces — Define the shape of an object
interface Student {
    name: string;
    age: number;
    grades: number[];
}

const student: Student = {
    name: "Tawfiq",
    age: 25,
    grades: [90, 85, 95]
};

// 4️⃣ Generics — Work with any type
function firstElement<T>(arr: T[]): T {
    return arr[0];
}

firstElement<number>([1, 2, 3]);     // returns 1
firstElement<string>(["a", "b"]);    // returns "a"

// 5️⃣ Enums — A set of named constants
enum Direction {
    Up = "UP",
    Down = "DOWN",
    Left = "LEFT",
    Right = "RIGHT"
}
```

### Frontend vs Backend

```
📱 Frontend (React + TypeScript)
   └── npx create-react-app my-app --template typescript
   └── Files: .tsx (TypeScript + JSX)
   └── Easier to start — see results instantly in the browser

🖥️ Backend (Node.js + TypeScript)
   └── npm init && npm install typescript ts-node
   └── Files: .ts
   └── More powerful for APIs and large-scale projects
```

---

## 🤝 Contributing

Contributions are welcome! 🎉

1. **Fork** the repository
2. Create a new **branch**: `git checkout -b feature/new-algorithm`
3. Add your code + tests
4. **Commit** your changes: `git commit -m "feat: add new algorithm"`
5. **Push** to your branch: `git push origin feature/new-algorithm`
6. Open a **Pull Request**

Please read the [Contributing Guidelines](CONTRIBUTING.md) for more details.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE) — feel free to use it however you like! 💪

---

<div align="center">

**⭐ If you found this project helpful, give it a star on GitHub!**

Made with ❤️ by [tawfiq154](https://github.com/tawfiq154)

</div>
