# 🥁 JS Drum Kit — Studio Edition

Uma aplicação web interativa e responsiva que transforma o teclado do computador em uma controladora de áudio profissional (estilo MPC / Launchpad de estúdio). Este projeto foi desenvolvido com o objetivo de consolidar conceitos fundamentais de JavaScript Vanilla (manipulação do DOM e eventos de áudio) combinados com técnicas avançadas de estilização e design UI moderno.

---

## 📸 Preview do Projeto

![Preview do Drum Kit](image.jpg)

---

## 🎛️ Mapeamento da Controladora

A interface possui 9 pads configurados com áudios de alta fidelidade, mapeados diretamente nas seguintes teclas do seu teclado:

| Tecla | Som Correspondente | Código do Evento (`keyCode`) |
| :---: | :--- | :---: |
| **A** | 👏 Clap (Palma) | `65` |
| **S** | 🪙 Hihat (Prato de Condução) | `83` |
| **D** | 🥁 Kick (Bumbo) | `68` |
| **F** | 🔓 Openhat (Prato Aberto) | `70` |
| **G** | 💥 Boom (Impacto Grave) | `71` |
| **H** | 🚴 Ride (Prato de Ritmo) | `72` |
| **J** | 🪘 Snare (Caixa) | `74` |
| **K** | 🪵 Tom (Tom-tom) | `75` |
| **L** | 🔔 Tink (Sino Metálico) | `76` |

---

## ✨ Funcionalidades e Destaques Visuais

* **Áudio de Baixa Latência:** Implementação de reset de tempo (`audio.currentTime = 0`) disparado no evento `keydown`. Isso garante que o som reinicie instantaneamente a cada clique, permitindo a execução de batidas e redobres rápidos sem atrasos.
* **Estética Launchpad Premium:** Visual escuro inspirado em hardwares de produção musical reais, utilizando efeitos de *Glassmorphism* (`backdrop-filter: blur`), gradientes sutis e iluminação neon dourada responsiva ao toque.
* **Feedback Físico 3D:** As teclas possuem profundidade simulada através de bordas assimétricas. Quando um pad é ativado, a classe `.playing` aplica um deslocamento no eixo Y (`translateY`) e reduz a borda inferior, criando a ilusão perfeita de que o botão foi fisicamente pressionado.
* **Arquitetura Flexível e Responsiva:** Layout projetado com Flexbox estruturado de forma rígida através de `flex-shrink: 0` para impedir que o navegador achate as teclas. Em dispositivos móveis, o chassi se adapta dinamicamente e ativa uma rolagem horizontal fluida e discreta.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi construído inteiramente com tecnologias web nativas, priorizando a performance e a fidelidade ao código puro:

* **HTML5:** Estruturação semântica e uso de atributos de dados customizados (`data-key`) para vincular os nós do DOM aos arquivos de áudio.
* **CSS3 Moderno:** Manipulação de Variáveis CSS (`:root`), transições suaves baseadas em curvas de animação (`cubic-bezier`), importação da tipografia *Plus Jakarta Sans* via Google Fonts e responsividade com Media Queries.
* **JavaScript (ES6):** Captura de eventos globais de escuta de teclado, interpolação de strings (*Template Literals*) para seletores dinâmicos e gerenciamento do ciclo de vida das animações utilizando o evento nativo `transitionend`.

---

## 🚀 Como Executar Localmente

1. Clone o repositório para o seu ambiente local:
   ```bash
   git clone [https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git](https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git)

2. Acesse o diretório do projeto e abra o arquivo index.html diretamente em qualquer navegador web moderno.

3. Ative o som do seu dispositivo, use as teclas correspondentes e crie seus próprios ritmos!

💡 Aprendizados Adquiridos

    Filtro de Transições Repetitivas: Durante a remoção de efeitos visuais via JavaScript, compreendeu-se que o evento transitionend é disparado individualmente para cada propriedade CSS que termina sua animação (borda, cor, sombra, etc.). Para mitigar execuções redundantes na pilha de processamento, foi aplicada uma condicional que filtra estritamente a propriedade principal (transform).

    Resiliência de Layout: Superação de comportamentos inesperados de esmagamento de elementos em layouts horizontais do Flexbox, garantindo o tamanho fixo ideal para os componentes de interface por meio de controle dimensional explícito.

👤 Autor

Desenvolvido com dedicação por Luiz Gustavo Garcia Da Silva.
📄 Licença e Créditos

Este projeto foi expandido, estilizado e aprimorado a partir do desafio prático do curso JavaScript 30 de Wes Bos. Sinta-se à vontade para utilizar, modificar e estudar o código!   
