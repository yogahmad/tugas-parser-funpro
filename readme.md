# Tugas Functional Programming : Parser
Saya membuat parser yang bisa menentukan nilai operasi boolean.

## Logical operator Precedence
- BRACKET "()"
- NOT (!x)
- IF AND ONLY IF (IFF) (<=>) 
- IF (=>)
- AND (&&)
- XOR (^^)
- OR (||)

## How To Run

parse expr $ deleteSpace  "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5) ^^ T"
parse expr $ deleteSpace "QUERY"

## Contoh Query

- "3 < 5 && 3 > 5" -> False
- "3 < 5 || 3 > 5" -> True
- "(3 < 5 || 3 > 5) => F" -> False
- "(3 < 5 || 3 > 5) => (3 == 3)" -> True
- "(3 < 5 || 3 > 5) => !(3 == 5)" -> True
- "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5)" -> False
- "(3 < 5 || 3 > 5) => !(3 == 5 <=> 3 == 5) ^^ T" -> True