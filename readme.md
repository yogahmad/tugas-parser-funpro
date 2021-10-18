# Tugas Functional Programming : Parser
Saya membuat parser yang bisa menentukan nilai operasi boolean.

## Logical operator Precedence
1. BRACKET "()"
2. NOT (!x)
3. IF AND ONLY IF (IFF) (<=>) 
4. IF (=>)
5. AND (&&)
6. XOR (^^)
7. OR (||)

## How To Run

- parse expr $ deleteSpace  "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5) ^^ T"
- parse expr $ deleteSpace "QUERY"

## Contoh Query

- "3 < 5 && 3 > 5" -> False
- "3 < 5 || 3 > 5" -> True
- "(3 < 5 || 3 > 5) => F" -> False
- "(3 < 5 || 3 > 5) => (3 == 3)" -> True
- "(3 < 5 || 3 > 5) => !(3 == 5)" -> True
- "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5)" -> False
- "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5) ^^ T" -> True