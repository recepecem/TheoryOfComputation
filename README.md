# TheoryOfComputation
2013Q1)**Yanda verilen DFA modelinin içerikten bağımsız dil gramer kurallarını tanımlayınız.** (*Define the context-free language grammar rules of the DFA model given below*)
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/Visa/2013/2013VisaQ1.png)

2013Q4)**Düzenli ifadesi a U ba\* U ab\*a olan dilin DFA modelini çiziniz.** (*Draw the DFA model of regular expression a U ba\* U ab\*a*)
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/Visa/2013/2013VisaQ4.png)

2013Q5)**Düzenli bir dil olarak {a, b} alfabesi üzerinde tanımlanan L diline ait kelimelerin ne
başında ne de sonunda aa veya bb bulunur. Buna göre L dilinin NFA modelini çiziniz.** (*Language L defined on the {a, b} alphabet as a regular language. It does not have aa or bb at the beginning nor at the end. Draw the NFA model of language L*)
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/Visa/2013/2013VisaQ5.png)

2013Q6)**Aşağıdaki içerikten bağımsız dil gramer kurallarını kullanarak bir yığınlı otomata tasarlayınız.** (*Design a PDA using the following context-free language grammar rules*)
**S→aB | bA &nbsp;&nbsp;&nbsp;&nbsp; A→a | aS | bAA | c &nbsp;&nbsp;&nbsp;&nbsp; B→b | bS | aBB | c**
<pre>
First, convert it into CNF.<br>
S'-> S<br>
S -> CB | DA<br>
A -> C | CS | DF | E<br>
B -> D | DS | CG | E<br>
C -> a<br>
D -> b<br>
E -> c<br>
F -> AA<br>
G -> BB<br>

S: qa$ -> qNBC   A:  qa$ -> qNC   qa$ -> qNFD   B:  qa$ -> qND   qa$ -> qNGC   C:  qaC -> qR€   F: qa$ -> qNAA<br>
   qb$ -> qNBC       qb$ -> qNC   qb$ -> qNFD       qb$ -> qND   qb$ -> qNGC   D:  qaD -> qR€      qa$ -> qNAA<br>
   qc$ -> qNBC       qc$ -> qNC   qc$ -> qNFD       qc$ -> qND   qc$ -> qNGC   E:  qaE -> qR€      qa$ -> qNAA<br>

   qa$ -> qNAD       qa$ -> qNSC  qa$ -> qNE        qa$ -> qNSD  qa$ -> qNE    G:  qa$ -> qNBB <br>
   qb$ -> qNAD       qb$ -> qNSC  qb$ -> qNE        qb$ -> qNSD  qb$ -> qNE        qb$ -> qNBB<br>
   qc$ -> qNAD       qc$ -> qNSC  qc$ -> qNE        qc$ -> qNSD  qc$ -> qNE        qc$ -> qNBB<br>
</pre>

or you can just use jflap to convert CFG to PDA
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/Visa/2013/2013VisaQ6.png)

2019Q1)**A family members (2 parents and 2 children) wants to walk side by side on the road.
Each parent holds one children’s hand. Both children can be in the middle or on the sides at the
same time. Design a NFA that accepts all possible walking situations.**
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/Visa/2013/2019VisaQ1.png)

2019Q2)**Convert the DFA given below to Regular Expression.
<pre>
Lq1 = aLq1 U bLq3
Lq2 = aLq2 U bLq1
Lq3 = aLq1 U bLq2 U €

apply Arden's Theorem
Lq1 = a^*bLq3
Lq2 = a^*bLq1

Lq3 = aLq1 U b(a^*bLq1) U €
Lq3 = a(a^*bLq3) U b(a^*b(a^*bLq3)) U €
Lq3 = (aa^*b U ba^*ba^*b)Lq3 U €
Lq3 = (aa^*b U ba^*ba^*b)^*€
Lq3 = (aa^*b U ba^*ba^*b)^*

Lq1 = aLq1 U b((aa^*b U ba^*ba^*b)^*)
Lq1 = a^*b((aa^*b U ba^*ba^*b)^*)
</pre>
