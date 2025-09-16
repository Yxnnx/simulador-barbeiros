# Simulação Baseada em Agentes do Comportamento de Triatomíneos

<p align="center">
  <img src="https://github.com/Yxnnx/simulador-barbeiros/blob/main/controlado.gif" width="650">
</p>
> Animação demonstrando o comportamento de agregação dos agentes em ambiente controlado. Onde o “Abrigo” é representado pelos dados de Odor de Barbeiro, “Camundongo” pelo Odor de Camundongo e “Calor” pelo Estímulo Térmico.

<p align="center">
  <img src="https://github.com/Yxnnx/simulador-barbeiros/blob/main/natural.gif" width="650">
</p>
> Animação demonstrando o comportamento de agregação dos agentes em ambiente natural. Onde o “Abrigo” é representado pelos dados de Odor de Barbeiro, “Camundongo” pelo Odor de Camundongo e “Calor” pelo Estímulo Térmico.

<p align="center">
  <img src="https://github.com/Yxnnx/simulador-barbeiros/blob/main/simulaçãosimples.gif" width="650">
</p>
> Animação demonstrando o comportamento de agregação dos agentes em ambiente natural. Onde o “Abrigo” é representado pelos dados de Odor de Barbeiro e “Alimento” é a representação dos estímulos Calor + Odor de Camundongo.


## 📖 Sobre o Projeto

Este projeto apresenta uma **simulação baseada em agentes (ABM)**, desenvolvida em Python com a biblioteca `agentpy`, para modelar o comportamento de insetos triatomíneos ("barbeiros"), vetores da doença de Chagas. Esta simulação foi feita baseado em resultados conseguidos em Laboratório. 

A simulação explora como uma hierarquia de estímulos sensoriais (químicos e térmicos) e o estado do inseto de fuga influenciam suas decisões e resultam em comportamentos coletivos complexos, como a formação de colônias em abrigos.

## ⚙️ Como a Simulação Funciona

Cada "barbeiro" é um agente autônomo e o comportamento complexo do grupo emerge dessas regras individuais:

*   **Estados Comportamentais:** Os agentes alternam entre um estado inicial de **Fuga/Exploração** (movimento rápido pelas bordas) e um estado de **Busca Ativa**.
*   **Hierarquia de Estímulos:** No estado de busca, os agentes são atraídos por três tipos de estímulos com forças diferentes, refletindo a preferência biológica:
    1.  **Abrigo (Feromônio):** O estímulo mais forte, representando o local de agregação e segurança.
    2.  **Fonte Alimentar (Odor):** Um estímulo intermediário, representando um hospedeiro.
    3.  **Estímulo Térmico:** O estímulo mais fraco, associado ao calor do hospedeiro.
*   **Lógica de Saciação e Parada:** Após passar um tempo perto da fonte alimentar, um agente fica "saciado" e passa a ignorar este estímulo, focando exclusivamente em encontrar o abrigo. 

## 🚀 Tecnologias Utilizadas

*   **Linguagem:** Python
*   **Simulação de Agentes:** `agentpy`
*   **Manipulação de Dados:** `numpy`
*   **Visualização:** `matplotlib` para a geração da animação.


### Cores dos Estímulos (Áreas Circulares)

As áreas coloridas no ambiente representam as zonas de influência dos estímulos. Cada cor corresponde a um tipo de estímulo, alinhado com sua função biológica:

*   🟣 **Roxo (`purple`): Abrigo (Feromônio)**
    *   **Significado:** Refúgio principal. 

*   🟢 **Verde (`green`): Fonte Alimentar (Odor) ou Alimento** 
    *   **Significado:** Presença de uma fonte de alimento (um hospedeiro). 

*   🟠 **Laranja (`orangered`): Estímulo Térmico**
    *   **Significado:** Representa o calor emitido por um hospedeiro.
      
### Cores dos Agentes (Círculos em Movimento)


*   ⚫ **Preto (`black`): Busca Ativa**
    *   **Significado:**  Um agente preto está ativamente procurando por estímulos no ambiente, movendo-se em direção àquele que exerce a maior força de atração.

*   🔵 **Azul (`blue`): Saciado**
    *   **Significado:** Um agente se torna azul após passar um tempo na "Fonte Alimentar". Este estado indica que sua necessidade de se alimentar foi satisfeita.

*   ⚪ **Cinza (`gray`): Fuga**
    *   **Significado:** Representa o estado inicial do agente ao ser introduzido em um ambiente. O agente se move rapidamente pelas bordas da arena, um comportamento de estresse ou exploração antes de se "acalmar" e iniciar a busca ativa.


##  Resultados e Conclusões

A simulação validou as hipóteses baseadas nos dados experimentais feitos em laboratório:
*   **Dominância da Agregação:** O estímulo do abrigo é o principal direcionador do comportamento, confirmando que a segurança do grupo é prioritária.
*   **Dependência do Contexto:** O comportamento de busca por alimento se mostrou mais provável em cenários de fuga prolongada, onde a exploração aumenta a chance de encontros com fontes alimentares.
*   **Potencial Preditivo:** O modelo demonstrou ser uma ferramenta robusta para prever os locais de agregação dos vetores, confirmando seu potencial para o planejamento de estratégias de controle.

## 📄 Referências Científicas

A lógica do modelo foi fundamentada em pesquisas publicadas sobre o comportamento de triatomíneos. Alguns dos principais artigos de referência foram:

*   Lazzari, C. R., et al. (2013). Sensory Ecology of Chagas Disease Vectors: A Review. Journal of Medical Entomology.
*   Barrozo, R. B., & Lazzari, C. R. (2004). Interaction of olfactory and thermal cues in the orientation behaviour of the blood-sucking bug Triatoma infestans. Journal of Insect Physiology.
* Alavez-Rosas, D., et al. (2022). Chemical ecology of triatomines: current knowledge and implications for Chagas disease vector management. Chemoecology.



