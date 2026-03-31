*TADSS*


O que é MUTEX? é um mecanismo de sincronização usado em programação concorrente para garantir que apenas uma thread ou processo acesse um recurso compartilhado (seção crítica) por vez

O que é um processo? Um programa em execução

o que é Thread? Um fluxo de execução dentro do processo

O que é Stack? Área de memória da Thread (variaveis locais e pilha de chamada de funções)

o que é um processo ou thread daemon? é um programa de computador que executa como um processo em segundo plano (background), sem interação direta com o usuário

o que significa prioridade na thread? é um valor atribuído a uma thread que define sua importância para o sistema operacional, determinando qual thread recebe mais tempo de CPU

o que é starvation? é uma thread morrer de fome

o que é condição de corrida? é um erro em sistemas concorrentes onde o resultado final depende da ordem imprevisível de threads

qual a diferença entre escalonador cooperativo e preemptivo? No cooperativo, o processo manda e só para quando quer; se ele travar, o sistema todo para. No preemptivo, o sistema operacional manda e interrompe o processo à força para dar a vez a outros, garantindo que nada trave o computador inteiro.

Diferença entre paralelismo e concorrencia (concorrencia é usada no dia-a-dia)

O que é Sleep? O sleep é uma pausa programada onde o processo avisa ao sistema que não precisa da CPU por um tempo, saindo da fila de execução para economizar recursos. No modelo cooperativo, é o gesto de "educação" que libera o computador para outros; no preemptivo, o sistema apenas coloca o processo para "dormir" e o ignora até o tempo acabar.

Qualquer objeto no java pode ser usado pra fazer synchronized

Lock acontece quando duas threads executam ao mesmo tempo

Diferença entre mutex e semaforo A principal diferença entre Mutex e Semáforo é que o Mutex é um mecanismo de bloqueio para exclusão mútua, permitindo apenas uma thread por vez em um recurso, enquanto o Semáforo é um mecanismo de sinalização que permite acesso controlado a múltiplas instâncias de um recurso (contagem).

04/03/2026 thread main é iniciado quando o programa (main) é executado, é o ponto de partida. programa sequencial: executado passo a passo em sequencia start() não inicia uma thread, ela muda para o estado 'ready' scheduler coloca a thread no estado 'running' e não é possível ter controle sobre a ordem de execução após ser executada, a thread vira uma thread morta e não pode ser executada novamente thread são objetos processos terminados em 'd' são deamon, o que significa que são threads que não vão 'morrer' configurações (deamon, prioridade...) devem ser definidas antes do start() 11/03/2026 thread tem três partes:

núcleo do s.o., ou seja, o que executa; código que ela tem que executar (execução do método run()); stack, ou seja, a memória das variáveis locais (área onde somente a thread que está executando, diferente do heap que é uma área comppartilhada entre outras threads) thread de plataforma (so);

green thread: é menos usada pois foca em dispositivos com 1 núcleo;

virtual thread (coroutines): N > 1;

Speedup:
O Speedup é a métrica que nos diz o quanto o seu sistema ficou mais rápido depois que você adicionou mais recursos (como mais núcleos de processador ou mais máquinas). Ele é importante pois quantifica a qualidade e rapidez do processador.
É possível ter um Speedup Negativo?
Sim, é perfeitamente possível! Na verdade, em computação, chamamos isso de "Slowdown".

Acontece quando você adiciona mais threads ou processadores e, em vez de o programa rodar mais rápido, ele fica mais lento do que se estivesse rodando em um único núcleo, acontece um overhead.

Por qual motivo existe um limite no speedup?
Pois é a parte do programa que não pode ser paralelizada (parte sequencial).

Resumo: Concorrência é sobre lida (organizar a bagunça); Paralelismo é sobre fazer (trabalho braçal simultâneo).


Latência: É sobre o atraso (foco no indivíduo/tarefa única).
Throughput: É sobre a entrega (foco no grupo/sistema todo). quantidade de tarefas que realiza em um certo tempo
