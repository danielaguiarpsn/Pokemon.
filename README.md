# Pokemon.
ATV Diego

# Pokemon.
ATV Diego:


Consultas


1)	Selecione o banco de dados (esquema) pokédex.
```sql
USE pokedex;
```

2)	Obtenha informações da estrutura da tabela Pokémon.

R: FROM 
        infotmation_schema.TABLES
        
   WHERE 
        TABLE_SCHEMA = 'pokedex'
         AND TABLE_NAME = 'Pokemon'


3)	Selecione todos os pokémons cadastrados no banco de dados.


R: USE pokedex;
   SELECT* FROM Pokemon


4)	Selecione o numero, nome, cor, altura_m e peso_kg de todos os pokémons cadastrados.

R: USE pokedex; 
   SELECT numero,
          nome,
          cor,
          altura_m,
          peso_kg
   FROM
        Pokemon;
        
        
5)	Qual é o numero e o nome de todos os pokémons da primeira geração?

R: USE pokedex;

   SELECT numero, nome 
   FROM Pokemon
   WHERE geração = 1;


6)	Quais são os pokémons Amarelo da primeira geração?

R:  USE pokedex;

   SELECT * FROM Pokemon
   WHERE geracao = 1
   AND cor = 'amarelo'


7)	Qual é o pokémon mais forte?

R:  USE pokedex;

   SELECT * FROM Pokemon
   ORDER BY total DESC
   LIMIT 1;
   
   
8)	Selecione o numero, nome e tipo1; de todos os pokémons cujo tipo primário é Fire.

R:  USE pokedex; 

   SELECT numero, nome, tipo1
   FROM Pokemon
   WHERE tipo1 = 'Fire';
   
   
10)	Selecione em ordem decrescente o numero, nome e defesa de todos os pokémons.

R:  USE pokedex;

   SELECT numero, nome, defesa
   FROM Pokemon 
   ORDER BY defesa DESC;
   

11)	Qual o pokémon possui menor taxa de captura? Selecione apenas numero e nome.

R:  USE pokedex; 

   SELECT numero, nome
   FROM Pokemon
   ORDER BY taxa_captura ASC
   LIMIT 1;
   

12) Selecione todos pokémons que não possuem tipo secundário, ou seja, tipo2. 

```sql
USE pokedex; 

SELECT numero, nome
FROM Pokemon
WHERE tipo2 IS NULL;
```

13) Selecione numero, nome, tipo1, tipo2 de todos os pokémons que possuem o peso entre 100kg e 500kg. 

R: USE pokedex; 
   SELECT numero,
       nome,
       tipo1
       yipo2
   FROM Pokemon
   WHERE peso_kg > 100 AND peso_kg < 50;

14) Crie um ranking dos top 10 pokémons mais velozes, contendo numero, nome e velocidade. 

R: USE pokedex; 
   SELECT numero, nome, velocidade
   FROM Pokemon
   ORDER BY velocidade DESC
   LIMIT 10;
   
15) Selecione numero, nome, tipo1, tipo2, taxa_captura dos pokémons que possuem os dois tipos e tenham uma taxa de captura acima de 100. Ordene os resultados decrescente pela taxa de captura. 

R: USE pokedex; 
   numero, nome, tipo1, tipo2, taxa_captura
   WHERE taxa_captura > 100
   AND tipo2 IS NOT NULL
   ORDER BY taxa_captura DESC;
   
16) Quais são os tipos primários dos pokémons? 

R: USE pokedex; 
   FROM Pokemon
   GROUP BY tipo1;
   
  
17) Selecione o numero, nome e cor; de todos os pokémons que o nome começa com a letra D. 

R: USE pokedex; 
   SELECT numero, nome, cor
   FROM Pokemon
   WHERE nome LIKE 'D%';
   
   
18) Qual é o pokémon mais poderoso de todas as gerações?

R: USE pokedex; 
SELECT  
      *
FROM Pokemon
ORDER BY total
19) Selecione o numero, nome, defesa, ataque dos pokémons com defesa > 60 e ataque <= 70; ordenados decrescente pelo total. 
20) Selecione todos os pokémons do tipo Planta e Venenoso que não sejam Green, ordenado crescente pelo nome. 
21) Selecione de maneira crescente os nomes dos pokémons que possuem a letra y na 4ª posição do nome. 
22) Qual é o maior valor de ataque_especial cadastrado? 
23) Selecione o numero, nome e altura_m dos pokémons que possuem altura acima de 2,10m. 
24) Quais são as diferentes tipos de cores dos pokémons? Apresente os resultados de maneira crescente pelo nome da cor. 
25) Selecione o nome e velocidade dos pokémons com velocidade entre 30 e 70. Ordene os resultados por nome (crescente) e velocidade (decrescente) 
26) Quem são os pokémons lendários? Apresente os resultados ordenados por total decrescente. 
27) Selecione os pokémons da primeira geração com taxa de captura igual a 255. 
28) Quem é o mais poderoso? selecione o Pikachu, Squirtle, Bulbasaur e Charmander; ordenados decrescente pelo total. 
29) Quem são os pokémons da primeira geração, que começam com a letra d e não possuem tipo secundário? Ordene os resultados crescente por taxa_captura e decrescente pelo total. 
30) Qual é o ranking dos top 5 pokémons lendários com maior taxa_captura e total? Apresente apenas numero, nome, total, taxa_captura nos resultados. 
31) Selecione o numero, nome, peso_kg dos pokémons com peso entre 2kg e 3kgs? 
32) Selecione o numero, nome, tipo1 e tipo2 dos pokémons com tipo primário Normal, que não possuem tipo secundário. Existe algum pokémon lendário nos resultados, se sim, os remova dos resultados? 
33) Quem são os pokémons do tipo Water que não são azuis? Apresente numero, nome, tipo1, tipo2 e cor, ordenados pelo nome de maneira crescente. 
34) Crie um ranking dos top 10 pokémons mais lentos. 
35) Selecione os pokémons cujo nome comece e termine com a letra a. 
36) Quem são os pokémons do tipo Fire que não são vermelhos? Apresente numero, nome, tipo1, tipo2 e cor, ordenados pelo nome de maneira crescente. 
37) Quais são os diferentes tipos de peso_kg dos pokémons? Apresente os resultados ordenados de maneira crescente. 
38) Selecione o numero, nome e hp dos pokémons com valores entre 0 e 100. Ordene os resultados de maneira crescente por hp e nome. 
39) Selecione o numero, nome, hp, ataque, defesa e total; dos pokémons com valores de hp, ataque, defesa maiores ou iguais a 100. 
40) Selecione todos os pokémons do tipos Water e Gelo, ordenados decrescente por total. 
