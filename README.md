alert('Boas vinda ao jogo do número secreto');
let numeroMaximo = 5000;
// Para gerar um número entre 1 e 3, podemos usar o código: let numeroAleatorio1a3 = parseInt(Math.random() * 3) + 1;.
let numeroSecreto = parseInt(Math.random() * numeroMaximo + 1);
console.log(numeroSecreto);
let chute ;
let tentativas = 1;

// enquanto chute nao for igual ao numero secreto
while (chute != numeroSecreto){
    chute = prompt(`Escolha um número entre 1 e ${numeroMaximo} `);
    // seo chute for igual ao numero secreto
    if (chute == numeroSecreto){
        break;
    } else{
        if(chute > numeroSecreto){
            alert(`O número secreto é menor que ${chute}`);
        } else{
            alert(`O número secreto é maior que ${chute}`);
        }
        //tentativas = tentativas + 1;
        tentativas++;
    }
}

let palavraTentativa = tentativas > 1 ? 'tentativas' : 'tentativa'
alert(`Isso ai! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} ${palavraTentativa}.`);
//if(tentativas > 1){
//    alert(`Isso ai! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} tentativas.`);
//} else{
//    alert(`Isso ai! Você descobriu o número secreto ${numeroSecreto} com ${tentativas} tentativa.`);
//}
