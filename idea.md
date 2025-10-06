# 🧩 **Blueprint Bahasa Pemrograman `indway` (v0.1)**

## 1. 🎯 **Visi & Filosofi**

**Nama:** `indway`
**Filosofi:**

> “Kita bebas melakukan apa pun yang kita mau, semau kita.”

**Misi:**
Menciptakan bahasa pemrograman yang *mengalir alami seperti pikiran*, fleksibel seperti bahasa manusia, namun tetap bisa dikompilasi ke berbagai perangkat — dari desktop, mobile, hingga web.

**Tagline:**

> *flow as you wish, code as you feel.*

---

## 2. 🧠 **Paradigma & Tujuan Desain**

| Aspek               | Deskripsi                                                                       |
| ------------------- | ------------------------------------------------------------------------------- |
| **Paradigma utama** | Multi-paradigm (imperatif, fungsional, ekspresif)                               |
| **Eksekusi**        | Bisa dijalankan secara interpretatif atau dikompilasi ke native / WASM          |
| **Target**          | Linux, Windows, macOS, Android, iOS, WebAssembly                                |
| **Filosofi desain** | Bebas gaya, bebas struktur, fokus ke *flow* dan hasil                           |
| **Inspirasi**       | Python (sederhana), Rust (safety), Lua (ringan), Bash (bebas), LISP (filosofis) |

---

## 3. 🔤 **Struktur Dasar Bahasa**

### Hello World

```indway
say "Hello, freedom!"
```

### Fungsi

```indway
fn greet(name) {
    say "Hai, " + name + "!"
}
greet "Irfan"
```

### Kontrol Alur

```indway
if time.now > 12: say "siang"
else say "pagi"
```

### Loop bebas

```indway
for i in range(1,5):
    say "Langkah ke", i
```

---

## 4. 🧩 **Tipe Data Dasar**

| Tipe   | Contoh                     | Deskripsi              |
| ------ | -------------------------- | ---------------------- |
| `text` | `"hello"`                  | String                 |
| `num`  | `42`, `3.14`               | Angka (auto float/int) |
| `bool` | `true`, `false`            | Boolean                |
| `list` | `[1, "bebas", true]`       | List campuran          |
| `map`  | `{name: "Irfan", age: 30}` | Dictionary / objek     |
| `none` | `none`                     | Nilai kosong           |

---

## 5. 🔧 **Fungsi & Modularitas**

### Definisi

```indway
fn add(a, b) -> a + b
```

### Anonim

```indway
let x = fn(a) => a * a
```

### Scope fleksibel

```indway
x = 10
fn test() {
    x = x + 1  # sah, lexical scope
}
```

---

## 6. ⚙️ **Struktur File & Eksekusi**

### File extension: `.ind`

```
program.ind
```

### Eksekusi

```
indway run program.ind
indway build program.ind --target native
indway build program.ind --target wasm
```

### Struktur project

```
myproject/
 ├─ src/
 │   └─ main.ind
 ├─ indfile.toml
 └─ build/
```

---

## 7. 🧱 **Compiler Arsitektur**

### 🛠 Pipeline

```
Source .ind
  ↓
Lexer → Parser
  ↓
AST (Abstract Syntax Tree)
  ↓
IR Generator (LLVM IR)
  ↓
Target Backend:
    - Native Binary (via LLVM)
    - WebAssembly
    - Embedded VM Bytecode
```

### 💡 Bootstrapping Plan

| Stage   | Tujuan                | Implementasi                         |
| ------- | --------------------- | ------------------------------------ |
| Stage 0 | Interpreter dasar     | Python (pakai Lark/PLY parser)       |
| Stage 1 | Compiler → LLVM IR    | Rust / C++                           |
| Stage 2 | Self-hosted compiler  | Compiler indway ditulis pakai indway |
| Stage 3 | Optimizer + VM custom | Cranelift / WASM                     |

---

## 8. 📦 **Core Library (v0.1)**

| Modul  | Fungsi                         | Deskripsi         |
| ------ | ------------------------------ | ----------------- |
| `say`  | `say("Hello")`                 | Output ke layar   |
| `sys`  | `sys.time()`, `sys.platform()` | Info sistem       |
| `file` | `file.read("a.txt")`           | File I/O          |
| `net`  | `net.get(url)`                 | HTTP simple       |
| `math` | `math.sum(list)`               | Operasi matematis |
| `flow` | `flow.sleep(1)`                | Delay, timer      |

---

## 9. 💬 **Manifesto Bahasa indway**

```
# indway Manifesto
1. Kamu bebas menulis seperti yang kamu mau.
2. Tidak ada gaya salah selama logika mengalir.
3. Kode adalah ekspresi, bukan instruksi.
4. Compiler hanyalah penerjemah, bukan penjaga.
5. Flow dengan cara kamu sendiri — the ind way.
```

---

## 10. 🚀 **Roadmap Pengembangan**

| Versi                | Fase                  | Target Utama                                 |
| -------------------- | --------------------- | -------------------------------------------- |
| **v0.1 (Prototype)** | Interpreter           | Bisa menjalankan `.ind` via Python           |
| **v0.2**             | Compiler LLVM backend | Output native & WASM                         |
| **v0.3**             | Standar Library       | File I/O, Network, Math                      |
| **v0.4**             | Package Manager       | `indway get <package>`                       |
| **v1.0**             | Self-hosted compiler  | Kompilasi indway dengan indway               |
| **v2.0+**            | AI-aware code flow    | Compiler bisa memahami konteks kreatif coder |

---

## 11. 🧬 **Contoh Program Lengkap**

```indway
# indway demo

fn inspire(name) {
    say "Jalanmu unik, " + name
    say "Lakukan semaumu, asal mengalir."
}

list = ["Irfan", "Neli", "Everyone"]

for n in list:
    inspire n
```

Output:

```
Jalanmu unik, Irfan
Lakukan semaumu, asal mengalir.
Jalanmu unik, Neli
Lakukan semaumu, asal mengalir.
Jalanmu unik, Everyone
Lakukan semaumu, asal mengalir.
```

---

## 12. 🌐 **Portabilitas & Distribusi**

| Platform                      | Output        | Catatan     |
| ----------------------------- | ------------- | ----------- |
| Desktop (Linux/Windows/macOS) | Native binary | via LLVM    |
| Web                           | WebAssembly   | ringan      |
| Mobile                        | ARM64 binary  | future plan |
| IoT                           | Bytecode      | via tinyVM  |

---

## 13. 🧰 **Ekosistem Awal**

| Komponen        | Nama     | Fungsi                          |
| --------------- | -------- | ------------------------------- |
| Compiler        | `indc`   | Compile `.ind` ke target        |
| Interpreter     | `indrun` | Jalankan langsung tanpa compile |
| CLI             | `indway` | Command utama                   |
| Package manager | `indget` | Ambil & pasang library          |
| Playground      | `indpad` | Web-based REPL (future)         |

---

## 14. 🪄 **Identitas & Branding**

* Nama resmi: **indway**
* Ekstensi file: `.ind`
* Logo: simbol “∞” yang dimodifikasi seperti aliran air
* Warna utama: **biru tua dan abu terang**
* Motto visual: *flow beyond syntax*
