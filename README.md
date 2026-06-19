**Traduções para as expressões regulares*

---

**Meta caracteres Padrão*
- . ? * + ^ $ | [ ] { } ( ) \

- [...] Lista
- [^...] Lista Negada
- ? Opcional
- () Grupo
- | Ou
- \+ E
- n,m de n até m
- \ Escapar algo (literalmente)
- \1 ... \9 Texto casado nos grupo 1...9

**Âncoras*

- ^ Início da Linha
- $ Fim da linha
- \b Início ou fim da palavra (borda)

**Nomes de arquivos*

- *.txt, nome-??.jpg  não são expressões relagulares
- São curingas de nomes de arquivos, e apesar de serem parecidos
- São usados apenas para nomeação de arquivos

- Lista exigênte: [aeiou] -> Somente vogais

- Exemplo:
- n[aã]o -> não e nao
- [0123456789] ou [0-9]

- Outros modelos agrupadores:
- [a-z] [A-Z] [A-Za-z] [A-Za-z0-9]

- Hexadecimais:
- [0-9A-Fa-f]

- Pontuações, espaço e tab e caracteres e branco:
- [.,!?:...] [ \t] [ \t\n\r\f\v]

- Caracteres imprimiveis
- [^ \t\n\r\f\v]

- Caracteres imprimiveis e o espaço
- [^\t\n\r\f\v]

- Quantificador	Significado	Exemplo
- 
- .	        qualquer    	        a.c -> aec ou abc
- +	        1 ou mais vezes	        a+c -> aaaacccc ou aacc
- ?	        opcional      	        https? (http ou https)
- *         tudo ou nada	        a* -> "" ou "a" ou "aaaaaaaaaaaaa"
- |         Ou uma coisa ou outra   gato|cachorro -> Ou gato ou cachorro
- {n}       Exatamente n vezes	    \d{4}
- {n,}	    Pelo menos n vezes	    a{3,}
- {n,m}	    Entre n e m vezes	    \d{2,4}

- somar expressões e o opcional
- [\d]+[^\d]2343423432sadadsds

- totalizadores
- 7{2} 77 ou \d{2,4} de 2 a 4 dígitos

- ^ fora do EA representa começa com
- $ fora do EA representa termina com