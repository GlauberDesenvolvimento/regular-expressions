## Traduções para as expressões regulares

**Meta caracteres Padrão**
- . ? * + ^ $ | [ ] { } ( ) \
---
- [...] Lista
- [^...] Lista Negada
- ? Opcional
- () Grupo
- | Ou
- \+ E
- n,m de n até m
- \ Escapar algo (literalmente)
- \1 ... \9 Texto casado nos grupo 1...9

*Âncoras*

<p>^ Início da Linha</p>
<p>$ Fim da linha</p>
<p>\b Início ou fim da palavra (borda)</p>

*Nomes de arquivos*

<p>*.txt, nome-??.jpg  não são expressões relagulares</p>
> São curingas de nomes de arquivos, e apesar de serem parecidos e São usados apenas para nomeação de arquivos

<p>Lista exigênte: [aeiou] -<p>Somente vogais</p>

*Exemplo:*
<p>n[aã]o -<p>não e nao</p>
<p>[0123456789] ou [0-9]</p>

**Outros modelos agrupadores:**
<p>[a-z] [A-Z] [A-Za-z] [A-Za-z0-9]</p>

*Hexadecimais:*
<p>[0-9A-Fa-f]</p>

*Pontuações, espaço e tab e caracteres e branco:*
<p>[.,!?:...] [ \t] [ \t\n\r\f\v]</p>

*Caracteres imprimiveis*
<p>[^ \t\n\r\f\v]</p>

*Caracteres imprimiveis e o espaço*
<p>[^\t\n\r\f\v]</p>

| Quantificador | Significado | Exemplo | Resultado |
|---------------|-------------|---------|-----------|
| `.` | Qualquer caractere | `a.c` | `abc`, `a1c`, `a@c`, `a-c` |
| `?` | Zero ou uma vez (opcional) | `https?` | `http`, `https` |
| `*` | Zero ou mais vezes | `a*` | `""`, `a`, `aa`, `aaa` |
| `+` | Uma ou mais vezes | `a+` | `a`, `aa`, `aaa`, `aaaa` |
| `\|` | Alternância (OU) | `gato\|cachorro` | `gato`, `cachorro` |
| `{n}` | Exatamente `n` vezes | `\d{4}` | `1234` |
| `{n,}` | Pelo menos `n` vezes | `a{3,}` | `aaa`, `aaaa`, `aaaaa` |
| `{n,m}` | Entre `n` e `m` vezes | `\d{2,4}` | `12`, `123`, `1234` |

**Somar expressões e o opcional**
<p>[\d]+[^\d]2343423432sadadsds</p>

*Totalizadores*
<p>7{2} 77 ou \d{2,4} de 2 a 4 dígitos</p>
> ^ fora do EA representa começa com... $ fora do EA representa termina com...