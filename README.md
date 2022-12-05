var


   nome_aluno: vetor [1..3] de caracter
   notas: vetor [1..3,1..3] de real
   medias: vetor [1..3] de real
   contador_nome: inteiro
   contador_nota: inteiro


inicio
   para contador_nome de 1 ate 3 faca
      limpatela
      escreval("Qual o nome do aluno ", contador_nome, "?")
      leia (nome_aluno[contador_nome])
      limpatela
      para contador_nota de 1 ate 3 faca
         escreval("Na escala de 1 até 10, qual a nota", contador_nota, " do aluno(a) ", (nome_aluno[contador_nome]), ": ")
         leia(notas[contador_nome, contador_nota])
      fimpara
      medias[contador_nome] := (notas[contador_nome, 1] + notas[contador_nome, 2] + notas[contador_nome, 3])/3
   fimpara
   limpatela


   para contador_nome de 1 ate 3 faca
      se medias[contador_nome] >= 6 entao
         escreval
         mudacor("Verde","Frente")
         escreval("O aluno(a) ", nome_aluno[contador_nome], " possui as seguintes notas:")
         escreval("|Nota 1:",notas[contador_nome, 1], " | Nota 2:",notas[contador_nome, 2], " | Nota 3: ", notas[contador_nome, 3],"|")
         escreval("O aluno(a) ", nome_aluno[contador_nome], " foi aprovado. Parabéns!")
         escreval
      senao
         Mudacor("Vermelho","Frente")
         escreval
         escreval("O aluno(a) ", nome_aluno[contador_nome], " possui as seguintes notas:")
         escreval("|Nota 1:", notas[contador_nome, 1], " | Nota 2:",notas[contador_nome, 2], " | Nota 3: ", notas[contador_nome, 3],"|")
         escreval("O aluno(a) ", nome_aluno[contador_nome], " foi reprovado, infelizmente!")
         escreval
         fimse
         fimpara
fimalgoritmo
