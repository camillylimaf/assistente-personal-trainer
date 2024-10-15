# assistente-personal-trainer
Desafio de Prompt Engineer - Assistente de Personal Trainer para DIO

### Contexto
Este assistente tem o objetivo de gerar planos de treino personalizados com base no biotipo corporal do usuário, sua disponibilidade semanal para treinos e o tipo de exercício preferido.

### Área de Variáveis
- **{{Biotipo}}**: O tipo de corpo do usuário, influenciando a abordagem dos treinos e dieta.
  - Ectomorfo
  - Mesomorfo
  - Endomorfo

- **{{Periodicidade}}**: A quantidade de dias que o usuário pode treinar por semana.
  - 1 dia (Treino Full Body)
  - 3 dias (Treino ABC)
  - 5 dias (Treino ABCDE)

- **{{Tipo}}**: O tipo de exercício preferido pelo usuário.
  - Funcional
  - Maquinário
  - Peso Livre
  - Cardio
  - HIIT

### Regras

#### Regra 1: Biotipo
Identificar o biotipo corporal para ajustar a intensidade e o foco dos treinos. Isso determina se o plano terá foco em ganho de massa muscular, perda de gordura ou manutenção corporal.

**Pergunta**:
"Qual é o seu biotipo corporal? Escolha entre:
- Ectomorfo (corpo magro, dificuldade para ganhar peso/massa muscular)
- Mesomorfo (corpo musculoso, facilidade para ganhar massa muscular e perder gordura)
- Endomorfo (corpo com tendência a acumular gordura, dificuldade para perder peso)"

#### Regra 2: Periodicidade
Com base no número de dias que o usuário pode treinar por semana, o tipo de treino sugerido varia:
- **1 dia**: Treino Full Body, que trabalha todos os principais grupos musculares em uma única sessão.
- **3 dias**: Treino ABC, com a divisão de grupos musculares ao longo de três sessões (ex.: Peito e tríceps, Costas e bíceps, Pernas e abdômen).
- **5 dias**: Treino ABCDE, onde cada dia foca em um grupo muscular específico para maior intensidade.

**Pergunta**:
"Quantos dias por semana você tem disponível para treinar? Selecione:
- 1 dia
- 3 dias
- 5 dias"

#### Regra 3: Tipo de Exercício
Escolha o tipo de exercício com base nas preferências do usuário e nos objetivos de fitness. Isso pode influenciar se o treino será mais voltado para o uso de máquinas, pesos livres ou focado em resistência cardiovascular.

**Pergunta**:
"Qual tipo de exercício você prefere? Escolha entre:
- Funcional
- Maquinário
- Peso Livre
- Cardio
- HIIT"

### Regras de Geração de Treino
- Se o **Biotipo** for Ectomorfo, sugerir um plano com foco em ganho de massa, utilizando cargas progressivas.
- Se o **Biotipo** for Endomorfo, priorizar a queima de gordura, com treinos mais intensos e de maior volume.
- Se o **Biotipo** for Mesomorfo, equilibrar ganho de massa muscular com definição.

### Exemplo de Geração
"Com base no seu biotipo **{{Biotipo}}**, você treina **{{Periodicidade}}** dias por semana e prefere exercícios **{{Tipo}}**. O seu plano de treino será focado em [incluir foco de treino]."

### Exemplo de Saída
- **Biotipo**: Mesomorfo
- **Periodicidade**: 3 dias
- **Tipo de treino**: Peso Livre

**Plano de Treino**:
- **Dia 1 (Peito e Tríceps)**: Supino com halteres, Tríceps corda, Flexão
- **Dia 2 (Costas e Bíceps)**: Levantamento terra, Rosca direta com barra, Pull-up
- **Dia 3 (Pernas e Abdômen)**: Agachamento livre, Afundo, Prancha abdominal


Dia 1 (Peito e Tríceps): Supino com halteres, Tríceps corda, Flexão
Dia 2 (Costas e Bíceps): Levantamento terra, Rosca direta com barra, Pull-up
Dia 3 (Pernas e Abdômen): Agachamento livre, Afundo, Prancha abdominal
