A Jornada do Herói: O Enigma dos Portais 🚪✨


Bem-vindo ao reino de Algolia, onde a lógica e a criatividade são suas maiores armas!
Este projeto visa ajudar o herói Aldor a encontrar o caminho correto através de portais mágicos, resolvendo um desafio algorítmico com uma interface interativa e visualmente atraente.

📌 Sobre o Desafio
📖 Contexto
O herói Aldor precisa atravessar uma série de portais mágicos numerados. Cada portal só pode ser acessado se o próximo número na sequência for pelo menos o dobro do anterior mais um (next ≥ 2 * current + 1).

🎯 Objetivo
Implementar uma função que, dada uma lista de números, retorne a maior sequência válida de portais que Aldor pode percorrer.

📊 Exemplos
Entrada	Saída Válida	Explicação
[2, 3, 4, 7, 14, 30]	[2, 4, 7, 14, 30]	4 ≥ 2*2+1, 7 ≥ 2*4+1, 14 ≥ 2*7+1, 30 ≥ 2*14+1
[5, 1, 3, 6, 12, 24, 50, 100]	[1, 3, 6, 12, 24, 50, 100]	3 ≥ 2*1+1, 6 ≥ 2*3+1, 12 ≥ 2*6+1, 24 ≥ 2*12+1, 50 ≥ 2*24+1, 100 ≥ 2*50+1
[10, 1, 2, 5, 21, 42, 85]	[2, 5, 10, 21, 42, 85]	5 ≥ 2*2+1, 10 ≥ 2*5+1, 21 ≥ 2*10+1, 42 ≥ 2*21+1, 85 ≥ 2*42+1
🚀 Como Usar
1️⃣ Interface Web
Input: Insira números separados por vírgula (ex: 2, 3, 4, 7, 14, 30).

Botões:

DESVENDAR → Calcula a maior sequência válida.

RETORNAR → Limpa os campos.

Resultado: Exibe a sequência encontrada e o passo a passo do cálculo.

2️⃣ Algoritmo (JavaScript)
A função principal findPortalSequence() usa backtracking para testar combinações válidas:

javascript
function findPortalSequence(numbers) {
    const sorted = [...numbers].sort((a, b) => a - b);
    let maxSequence = [];

    function buildSequence(start, current) {
        if (current.length > maxSequence.length) maxSequence = [...current];
        for (let i = start; i < sorted.length; i++) {
            const num = sorted[i];
            if (current.length === 0 || num >= 2 * current[current.length - 1] + 1) {
                buildSequence(i + 1, [...current, num]);
            }
        }
    }

    buildSequence(0, []);
    return maxSequence;
}
🎨 Design & Tecnologias
✨ Estilo Visual
Tema: Fantasia medieval com efeitos de brilho (glow).

Cores: Gradiente mágico (roxo, ciano, dourado).

Responsivo: Adapta-se a dispositivos móveis.

🛠️ Tecnologias
Frontend: HTML5, CSS3 (Flexbox, Animations), JavaScript.

Efeitos Especiais: Botões com animação glowing.

📝 Licença
Este projeto é livre para uso e modificação.

Desafio proposto por: [OneBitCode]
Implementado por: [@luizfx.dev]



🌟 Que a sorte esteja com Aldor em sua jornada! 🌟
