# 🛠️ DNI & NIE Validation Exercise

## 📌 Objective
Implement a Java program to **validate Spanish DNI and NIE numbers** based on their structure and verification algorithm.

## 🔍 Validation Rules

### **DNI (Documento Nacional de Identidad)**
- Consists of **8 digits + 1 letter** (e.g., `12345678Z`).
- The letter is calculated using the remainder of the number divided by 23.
- The remainder corresponds to the following sequence of letters:
```
T, R, W, A, G, M, Y, F, P, D, X, B, N, J, Z, S, Q, V, H, L, C, K, E
```

- If the calculated letter matches the last character of the DNI, it is **valid**.

### **NIE (Número de Identidad de Extranjero)**
- Follows the format **X, Y, or Z** + **7 digits** + **1 letter** (e.g., `Y1234567L`).
- The initial letter is converted to a number:
- `X` → `0`
- `Y` → `1`
- `Z` → `2`
- After conversion, the rest of the process is the same as for DNI validation.

## 🚀 Tasks

1. Implement a function `boolean isValidDni(String dni)` to validate **DNI numbers**.
2. Implement a function `boolean isValidNie(String nie)` to validate **NIE numbers**.
3. Ensure that both functions handle **invalid formats** properly.
4. Write **unit tests** to validate different cases.

## 📝 Examples

```java
isValidDni("12345678Z"); // → true
isValidDni("87654321X"); // → false
isValidDni("A2345678Z"); // → false

isValidNie("Y1234567D"); // → true
isValidNie("Z7654321X"); // → false
isValidNie("X0000000T"); // → true