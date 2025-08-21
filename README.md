# Catalogue Code

This project demonstrates **Lagrange Interpolation** for reconstructing a hidden constant (the secret) from a set of points, where each point's `y`-value is given in a **different number system (base)**.  

It is essentially an implementation of the decoding step in **Shamir’s Secret Sharing**, where the constant term of the polynomial (`f(0)`) represents the hidden value.

---

## 📌 How It Works

1. **Input**
   - The program takes a JSON object with:
     - `keys.n`: total number of points available.
     - `keys.k`: minimum number of points required to reconstruct the secret.
     - Each entry (`"1"`, `"2"`, …) contains:
       - `base`: the base in which the value is encoded.
       - `value`: the number in that base.

   Example:
   ```json
   {
     "keys": { "n": 9, "k": 6 },
     "1": { "base": "10", "value": "28735619723837" },
     "2": { "base": "16", "value": "1A228867F0CA" },
     ...
   }
