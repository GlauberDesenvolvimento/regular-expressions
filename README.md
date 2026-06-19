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

*Flags*
<p>/g -> Global `new RegExp("abc", "g")`</p>
<p>/i -> ^ e $ para cada linha</p>
<p>/m -> Multiline /s ignora quebra de linha</p>
<p>/u -> Unicode</p>
<p>/b -> Trata apenas palavras e não as letras nas palavras</p>
<p>/y -> Stick pega a última posição</p>


*Grupos*
<p>(aeiou) -> aeiouaeiouaeiouaeiouaeiou</p>

## Classes Predefinidas de Caracteres

| Metacaractere | Significado | Equivale a | Exemplo | Resultado |
|---------------|-------------|------------|----------|-----------|
| `\d` | Um dígito | `[0-9]` | `\d+` | `123`, `4567` |
| `\D` | Não é um dígito | `[^0-9]` | `\D+` | `abc`, `@#$` |
| `\w` | Caractere de palavra | `[A-Za-z0-9_]` | `\w+` | `Glauber`, `abc123`, `teste_01` |
| `\W` | Não é caractere de palavra | `[^A-Za-z0-9_]` | `\W+` | `@#$`, `!?`, `-` |
| `\s` | Espaço em branco | `[ \t\n\r\f\v]` | `\d+\s\w+` | `123 ABC` |
| `\S` | Não é espaço em branco | `[^ \t\n\r\f\v]` | `\S+` | `Glauber`, `123ABC` |
| `\n` | Quebra de linha | — | `Olá\nMundo` | Nova linha |
| `\t` | Tabulação (TAB) | — | `Nome\tIdade` | Espaço de TAB |

## Sequências Especiais (Dependentes da Engine)

| Metacaractere | Significado | Observação |
|---------------|-------------|------------|
| `\a` | Caractere Bell (ASCII 7) | Emite um alerta sonoro em algumas linguagens. |
| `\A` | Início absoluto da string | Diferente de `^`, não é afetado pelo modo multilinha. |
| `\h` | Espaço em branco horizontal | Ex.: espaço e TAB horizontal. |
| `\H` | Não é espaço em branco horizontal | Inverso de `\h`. |
| `\l` | Converte o próximo caractere para minúsculo | Utilizado em substituições (Perl/PCRE). |
| `\L` | Converte todos os caracteres seguintes para minúsculo | Utilizado em substituições (Perl/PCRE). |
| `\u` | Converte o próximo caractere para maiúsculo | Em regex, normalmente usado apenas em substituições. Em JavaScript possui outro significado em strings (`\uXXXX`). |
| `\U` | Converte todos os caracteres seguintes para maiúsculo | Utilizado em substituições (Perl/PCRE). |