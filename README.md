programa {
  inclua biblioteca Util --> u
  inteiro esc, nusorteado
  real peso, altura, imc
  real prova1, prova2, prova3
  real trab1, trab2, trab3
  real media
  funcao inicio() {
    escreva ("(1) Para calcular o IMC \n")
    escreva ("(2) Para calcular a média trimestral \n")
    escreva ("(3) Para sortear um número \n")
    escreva ("Sua escolha:")
    leia(esc)

    escolha (esc){
      caso 1:
        escreva ("Vamos descobrir seu IMC \n")
        escreva ("Entre com seu peso:")
        leia (peso)
        escreva ("_kg\n")
        escreva ("Entre com sua altura:")
        leia (altura)
        escreva ("_m\n")
        imc = peso/(altura * altura)
        escreva ("\n O seu IMC é ")
        escreva (imc)
      caso 2:
        escreva ("vamos calcular sua média anual: \n")
        escreva ("coloque sua nota de prova do primeiro trimestre: \n")
        leia (prova1)
        escreva ("coloque sua nota de trabalho do primeiro trimestre: \n")
        leia (trab1)
        escreva ("coloque sua nota de prova do segundo trimestre: \n")
        leia (prova2)
        escreva ("coloque sua nota de trabalho do segundo trimestre: \n")
        leia (trab2)
        escreva ("coloque sua nota de prova do terceiro trimestre: \n")
        leia (prova3)
        escreva ("coloque sua nota de trabalho do terceiro trimestre: \n")
        leia (trab3)
          se (trab1 > 40 ou prova1 > 60 ou trab2 > 40 ou prova2 > 60 ou trab3 > 40 ou prova3 > 60){
          escreva ("você ultrapassou o limite de alguma nota: \n")}
        media = (prova1 + prova2 + prova3 + trab1 + trab2 + trab3) / 3
        escreva ("sua média anual é:")
        escreva (media)
      caso 3:
        nusorteado = u.sorteia(1,10)
        escreva ("o número sorteado é \n")
        escreva (nusorteado)
    
      pare
    }
  }
}
