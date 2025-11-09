
# Yu-Gi-Oh | Jo-ken-po Edition

Jogo de jokenpo que criei para explicar conceitos de lógica de programação aplicados a jogos

conceitos abordados:

- Armazenamento e gerenciamento de estado manual
- Funções limpas
- Organização de código

-----------------------------------------------------------------------

# Learned in  the Video-Aula

- Dicas de tutores sempre são:Antes de Iniciar, reflita, veja, raciocíne tudo que 
 você está planejando fazer, quais coisas você irá precisar ter, como: aqui vamos precisar de 3 divs, vamos necessitar de uma função..; quebre sempre o problema/ questão em peuqenos detalhes e vai solucionando um por um.
 

- [FACILITAR A CRIAÇÃO DE *DIVS* NO *HTML*]

* div.Jogos+div.container>(div.container-one+div.container-two)

- [COLOCAÇÃO DE *VIDEO* EM PROJETO]

*  == utilizando *source* *autoPlay* *loop* *muted*==> Ao inicializar
 
*  <video class="video" autoplay loop muted>
        <source src="./src/assets/video/yugi.mp4" type="video/mp4"/>
    </video>

* Gerenciamento de Estado Global e Imutabilidade

* **Objeto de Estado Centralizado (`state`):** Todas as referências essenciais do DOM (como `scoreBox`, `card-image`, `next-duel`) e as variáveis de placar (`playerScore`, `computerScore`) são encapsuladas no objeto `state`. Isso permite um **gerenciamento de estado (state management) manual** limpo, facilitando as atualizações da UI a partir de um único ponto.

* **Funções de Propósito Único: ***

    * `getRandomCardId()`: Apenas retorna um ID de carta aleatório.
    * `drawCardsInField()`: Apenas atualiza o `src` das imagens das cartas no campo.
    * `checkDuelResults()`: Apenas compara os IDs das cartas e retorna o resultado.

### 3. Manipulação Dinâmica do DOM

* **Criação Programática de Elementos:** A função **`createCardImage()`** ilustra a criação de elementos `<img>` do zero (`document.createElement`), e a atribuição de múltiplos atributos (`setAttribute`, `classList.add`) e *data attributes* (`data-id`).

* **Gerenciamento de Eventos e Feedback Visual:**
    * Event Listeners de **`mouseover`** e **`click`** são adicionados dinamicamente às cartas criadas, ligando a interação do usuário diretamente às funções de lógica (`drawSelectCard` para feedback e `setCardsField` para ação de jogo).

* **Limpeza de Elementos:** 
`removeAllCardsImages()`** demonstra uma maneira eficiente de "limpar" a tela antes do duelo, usando `querySelectorAll("img")` dentro de um contêiner específico e o método `remove()` em cada elemento

---------------------------------------------------------------------------------------------

![Yu-gi-oh-](https://github.com/user-attachments/assets/c1de59dd-ec16-4a6f-970c-e5ea38c3285f)

