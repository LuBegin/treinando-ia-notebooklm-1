# treinando-ia-notebooklm-1

## OBJETIVO
O propósito deste caderno temático é compilar e detalhar conceitos técnicos básicos sobre o hardware de um PC desktop obtendo, 
a partir dele, base de comparação e qualidade de cada peça. 

## FONTES
- https://blog.kabum.com.br/como-escolher-placa-de-video-guia-monte-seu-pc/
- https://blog.kabum.com.br/como-escolher-processador-guia-monte-seu-pc/
- https://www.ibm.com/br-pt/think/topics/central-processing-unit
- https://www.corsair.com/br/pt/explorer/glossary/what-is-a-motherboard/?srsltid=AfmBOopjw2gP3fJjnj3CILvf6hrVJ-1J0VcX1ejYkA30IAgvYdW_xEkM
- https://youtu.be/OrdiexfWdns?si=c3T5Tog5vRItDBwx

## TESTES DE PROMPTS
Iniciei o teste de prompts com uma pergunta mais tranquila e fui escalando o nível de especificidade, observando se ele 
conseguia cruzar os dados das fontes adicionadas corretamente e até, ir além do que foi pedido. 
Abaixo segue a lista de perguntas e os resultados obtidos:

1. "Qual a diferença entre núcleos e threads de um processador?"

   Como tinham fontes (textuais e audiovisuais) bem diretas sobre o tema, iniciei o teste perguntando sobre a funcionalidade do processador.

   RESULTADO: o modelo respondeu com riqueza de detalhes, explicando de forma bem satisfatória as diferenças físicas e virtuais do componenete, dividindo
   a explicação em duas partes: "Núcleo - Unidades físicas" e "Threads - Processadores Lógico".
   Ele conseguiu fazer analogias como "Se os núcleos físicos são os 'braços' do processador, as threads representam a capacidade que cada um
   desses braços tem de segurar dois pratos de uma vez" sem grandes dificuldades, provando não apenas que ele reteve o conteúdo, mas que consegue
   explicar de forma prática para quem está estudando.

2. "O que acontece se eu tentar colocar um processador AMD Ryzen em uma placa-mãe feita para Intel? O modelo consegue
   identificar a incompatibilidade nos meus arquivos?"
   
   Aqui comecei a especificar mais a pergunta, aprofundando o tópico sobre comparação de peças de hardware de diferente modelos e marcas,
   observando se o modelo conseguia explicar incompatibilidades e especificidades de marcas.
   
   RESULTADO: a resposta foi muito satisfatória! Além de responder que sim, haverá incompatibilidade entre a placa-mãe e o processador, ele destrinchou
   como uma placa-mãe é projetada exclusivamente para cada marca, explicando as diferenças físicas dos soquetes e entrando no conceito de chipset.

3. "O computador funciona perfeitamente para navegar na internet e ver vídeos. Porém, assim que eu abro um jogo pesado, após alguns minutos,
   o computador simplesmente apaga (como se tivesse caído a energia da tomada) ou reinicia sem dar tela azul. As temperaturas de CPU e GPU estão
   normais (abaixo de 70°C). O que está falhando?"
   
   A pergunta desta vez foi muito mais específica e propositalmente foi posta diante do modelo uma situação real para ele relacionar com as fontes
   oferecidas. Existem dois desafios para o modelo na situação apresentada: a) ele precisa interpretar corretamente a situação e as circuntâncias, pensando
   numa forma de aplicar o conteúdo das fontes em prática para resolver um problema real; b) oferecer a resposta correta, sem confundir um problema com outro.
   Era possível que ele desse o diagnóstico de superaquecimento, da GPU ou da CPU, o que estaria ERRADO.
   Esta situação foi aplicada exatamente por conta deste desafio: diagnosticar o verdadeiro problema, que no caso, era a fonte de energia.

   RESULTADO: O modelo conseguiu dar o diagnóstico correto da situação, explicando a relação entre consumo de energia da placa de vídeo e a potência
   da fonte, apontando a necessidade de desligamento para segurnaça do equipamento. Além disso, explicou a possibilidade da fonte ser de má qualidade
   (as chamadas "fontes cinzas") e possivelmente não estar entregando a potência prometida. Ele ofereceu uma solução, sugerindo a mudança da fonte de
   energia com selo 80 plus para não comprometer os demais componentes do PC.


## MINIGUIA de ESTUDO
Neste tópico gostaria de deixar um miniguia de estudo da área em que eu treinei o notebookLM, dividido em resumo, glossário e
prompts reutilizáveis. Ele me ajudou a relembrar algumas curiosidade e conceitos desta temática!


**RESUMO**

*Processador (CPU)*: É o "cérebro" e o "chef de cozinha" da máquina, responsável por receber comandos, processar dados e delegar tarefas
aos programas e ao sistema operacional.
. Ele dita a inteligência e a velocidade do sistema utilizando os seus núcleos e threads;

*Placa-Mãe*: É a espinha dorsal do computador.
. Consiste em uma grande placa de circuito que recebe e unifica fisicamente as outras peças (como processador, RAM e GPU), 
permitindo que se comuniquem e funcionem em conjunto;

*Memória RAM*: Funciona como uma bancada de trabalho de curtíssimo prazo e altíssima velocidade.
. Ela guarda as informações dos programas e do Windows apenas enquanto o PC está ligado. Se o PC for desligado, essa memória é esvaziada;

*Armazenamento (HDD e SSD)*: É onde os seus arquivos, jogos e Windows ficam guardados permanentemente, mesmo quando o PC é desligado.
. Os antigos HDDs usam agulhas mecânicas e são lentos, enquanto os SSDs (especialmente o padrão NVMe M.2) utilizam chips e chegam a
ser dezenas de vezes mais rápidos;

*Placa de Vídeo (GPU)*: É a "alma" dos PCs Gamers e funciona conectada ao slot PCI Express X16 da placa-mãe.
. A GPU possui milhares de núcleos dedicados apenas para renderizar e desenhar os gráficos 3D, texturas e luzes do monitor em tempo real,
tirando a sobrecarga gráfica das costas do processador;

*Fonte de Alimentação*: Responsável por alimentar a placa-mãe, a GPU e a CPU com eletricidade.
. É obrigatório que seja de qualidade (com selo 80 Plus e PFC Ativo) para entregar energia de forma estável, visto que fontes de má qualidade 
podem estragar os componentes gradativamente;

*Refrigeração (Cooler)*: O sistema que evita que a CPU "frite". 
Pode ser a ar (Air Cooler, com ventoinhas e dissipadores) ou a base de líquido (Water Cooler, que utiliza uma bomba e um radiador semelhante ao de um carro);

*Gabinete*: É a caixa estrutural e estética onde as peças são acomodadas, não devendo jamais ser chamado de "CPU"


**GLOSSÁRIO**

*Núcleos (Cores)*: São os "braços" físicos de trabalho do processador, determinando quantas tarefas ele consegue agarrar fisicamente ao mesmo tempo;

*Threads*: São processadores lógicos ou virtuais, que funcionam dando a capacidade de um único núcleo físico (braço) gerenciar duas tarefas simultaneamente;

*Clock (GHz)*: É a velocidade do processador, indicando a frequência máxima e mínima com que ele trabalha para processar dados;

*Overclock*: Um procedimento avançado que força o componente a trabalhar em uma velocidade acima da especificada de fábrica para obter mais performance;

*Soquete (Socket)*: O encaixe mecânico onde a CPU é instalada
Cada geração ou marca (como o soquete AM4 da AMD ou o LGA 1700 da Intel) possui um formato físico diferente, o que dita a compatibilidade
rigorosa entre a placa e o processador;

*Chipset*: É o microprocessador inteligente que já vem integrado à placa-mãe.
Ele atua como um "gerente de trânsito", controlando a comunicação entre o processador principal e outros dispositivos,
como entradas USB, armazenamento e áudio;

*VRAM*: É a memória de vídeo dedicada dentro da própria GPU.
Ela armazena texturas e informações dos jogos para evitar que o PC fique travando ao buscar essas imagens em outros lugares;

*Ray Tracing*: Uma tecnologia avançada que simula o traçado real da luz, produzindo reflexos e iluminações hiper-realistas nos jogos;

*Upscaling (DLSS / FSR)*: Tecnologias mágicas das marcas (Nvidia e AMD, respectivamente) que usam algoritmos e inteligência artificial 
para renderizar o jogo em resoluções mais baixas e escalá-lo para uma resolução alta, o que gera um grande salto de fluidez (FPS) sem perder 
a qualidade da imagem;


**PROMPTS REUTILIZÁVEIS**

"O que acontece se eu colocar um processador de uma marca (intel) com uma placa mãe de outra marca (AMD)?"

"Como funciona um processador?"

"Faça um resumo para mim do hardware de um PC."

"O que pode causar superaquecimento do PC?"

"Crie um glossário com palavras fundamentais na computação."

"Crie uma lista de Placas de Vídeo que eu preciso conhecer."

"Quais as diferenças entre um processador da AMD e um da Intel?"

