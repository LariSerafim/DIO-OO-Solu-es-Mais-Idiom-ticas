# DIO-OO-Solu-es-Mais-Idiom-ticas
//Supondo que a população de um país A tenha N habitantes com uma taxa anual de crescimento de 3% e que a população de B M habitantes com uma taxa de crescimento de 1.5%. Faça um programa que calcule e escreva o número de anos necessários para que a população do país A ultrapasse ou iguale a população do país B, mantidas as taxas de crescimento.
//Obs: O valor inicial da população A deverá ser sempre menor que do país B



data class Pais(var habitantes: Double, var taxaCrescimento: Double) {

  fun crescerPopulacaoAnual() { 

   habitantes = habitantes + (habitantes * taxaCrescimento/100)

   // TODO("Criar a lógica de crescimento populacional, usando as propriedades do [Pais]")

  }

}



fun main() {

  val habitantesPaisA = readLine()!!.toDouble();

  val habitantesPaisB = readLine()!!.toDouble();

  val paisA = Pais(habitantesPaisA, taxaCrescimento = 3.0)

  val paisB = Pais(habitantesPaisB, taxaCrescimento = 1.5)

  

  var quantidadeAnos = 0

  while (paisA.habitantes < paisB.habitantes) {

  paisA.crescerPopulacaoAnual()

  paisB.crescerPopulacaoAnual()

  quantidadeAnos ++

  //  TODO("Invocar a função que consolida o crescimento anual de cada [Pais]")

  // TODO("Garantir de a variável mutável $quantidadeAnos seja atualizada")

  }

  

  println("$quantidadeAnos anos")

}
