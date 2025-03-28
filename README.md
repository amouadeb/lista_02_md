(b)
p % q === 1 → 10 % 3 === 1 → verdadeiro
r * 2 > p → 6 * 2 > 10 → 12 > 10 → verdadeiro
q + r < p → 3 + 6 < 10 → 9 < 10 → verdadeiro


(c)
A diferença entre as funções está no uso de do...while e while. Enquanto analisarCredito1() soma os valores antes de verificar a condição e só para quando o próximo valor excede o limite (saldo final: -200), analisarCredito2() verifica a condição antes de somar e permite adicionar um valor extra antes de interromper (saldo final: -600).


(b)
Se idade >= 18 e idade < 60, imprime "Você é um adulto!". Se idade < 18, imprime "Você é menor de idade!". Mas se for idade >= 60, imprime "Você está na melhor idade!".


(b)
Dispositivo 1 (300W) → 1200 - 300 = 900
Dispositivo 2 (600W) → 900 - 600 = 300
Dispositivo 3 (500W) → Usa 300W da energia restante, precisa de mais 200W da bateria extra (resta 200W)
Dispositivo 4 (200W) → Usa os 200W restantes da bateria
Dispositivo 5 (400W) → Não liga



(b)
A função update() é executada a cada frame do jogo, atualizando os objetos para detectar colisões e movimentações.


(a)
O principal módulo em matter.js é o motor de física, que permite simular corpos, objetos e personagens para deixar as animações mais realistas.

var compras = [40.50, 20.50, 10.25, 30.85, 65.90];
var totalCompras = 0;
// vai somar o valor das compras
for (i = 0; i < compras.length; i++) {
    totalCompras += compras[i]; // totalCompras = 168
}
console.log(`O preço total de suas compras é R$ ${totalCompras.toFixed(2)}`); // O preço total das compras é R$ 168.00
// vai avaliar o frete em relação ao total da compra 
if (totalCompras < 50) {
    console.log("Frete não disponível!");
} else if (totalCompras >= 50 && totalCompras <= 199.99) {
    console.log("Frete com custo adicional!");
} else {
    console.log("Frete grátis!");
}
8.

javascript
Copiar
Editar
// Classe base Veiculo
class Veiculo {
    constructor(modelo, ano) {
        this.modelo = modelo;
        this.ano = ano;
    }

    calcularConsumo() {
        // Implementação genérica
        return 0;
    }
}

// Classe derivada Carro
class Carro extends Veiculo {
    constructor(modelo, ano, eficiencia) {
        super(modelo, ano);
        this.eficiencia = eficiencia; // km por litro
    }

    calcularConsumo(quilometragem) {
        return quilometragem / this.eficiencia;
    }
}

// Classe derivada Moto
class Moto extends Veiculo {
    constructor(modelo, ano, eficiencia) {
        super(modelo, ano);
        this.eficiencia = eficiencia; // km por litro
    }

    calcularConsumo(quilometragem) {
        return quilometragem / this.eficiencia;
    }
}

var carro = new Carro("Hyundai", 2022, 10);
console.log(` O Consumo do carro é: ${carro.calcularConsumo(100)} litros`);

var moto = new Moto("Kawasaki", 1990, 20);
console.log(` O Consumo da moto é : ${moto.calcularConsumo(100)} litros`);
9.

javascript
Copiar
Editar
// Variáveis de entrada
var velocidadeInicial = 5000; 
var velocidadeSegura = 5; 
var desaceleracao = 50; 
var tempoMaximo = 300; 

// Variável para armazenar o tempo necessário
var tempoNecessario = 0;

// Loop para calcular o tempo necessário
while (velocidadeInicial > velocidadeSegura && tempoNecessario < tempoMaximo) {
    velocidadeInicial -= desaceleracao;
    tempoNecessario++;
}

if (velocidadeInicial <= velocidadeSegura) {
    console.log(`Tempo necessário para atingir a velocidade segura de pouso: ${tempoNecessario} segundos`);
} else {
    console.log("Não foi possível atingir a velocidade segura de pouso dentro do tempo máximo permitido.");
}
10.

javascript
Copiar
Editar
// Função para multiplicar as matrizes
function MultiplicarMatrizesInvestimento(matrizA, matrizB) {
    // Verifica se o número de colunas da matrizA é igual ao número de linhas da matrizB
    if (matrizA[0].length !== matrizB.length) {
        return "As matrizes não podem ser multiplicadas. Elas têm dimensões incompatíveis.";
    }

    var linhasA = matrizA.length;
    var colunasA = matrizA[0].length;
    var colunasB = matrizB[0].length;
    var matrizResultado = [];

    // Inicializa a matrizResultado com zeros
    for (var i = 0; i < linhasA; i++) {
        matrizResultado[i] = [];
        for (var j = 0; j < colunasB; j++) {
            matrizResultado[i][j] = 0;
        }
    }

    // Loop para multiplicar as matrizes
    for (var i = 0; i < linhasA; i++) {
        for (var j = 0; j < colunasB; j++) {
            for (var k = 0; k < colunasA; k++) {
                matrizResultado[i][j] += matrizA[i][k] * matrizB[k][j];
            }
        }
    }

    return matrizResultado;
}

// Exemplo de uso da função
var investimentosAno1 = [[1000, 2000], [1500, 2500]];
var investimentosAno2 = [[1200, 1800], [1300, 2700]];

var totalInvestimentos = MultiplicarMatrizesInvestimento(investimentosAno1, investimentosAno2);
console.log("Total de investimentos acumulados:");
console.log(totalInvestimentos);


