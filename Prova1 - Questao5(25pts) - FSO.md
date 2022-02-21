# Pergunta - Dado o diagrama abaixo, que mapeia os estados em que um processo pode se encontrar, descreva as condicoes em que as trocas de estado ocorrem.

R: Estados de um processo:
  -NEW: novo processo se iniciando
  -RUNNING: processo executando
  -WAITING: processo esperando algum evento
  -TERMINATED: processo terminou a execução
 
  Condições:
  -Pronto -> Execução = Quando um processo é criado, é colocado em uma lista de processos "PRONTO". Então é escolhido pelo sistema para ser executado.
  -Execução -> Espera = O processo passa para espera quando aguarda a conclusão de um evento solicitado.
  -Espera -> Pronto = O processo passa para pronto quando a operação solicitada é atendida ou o recurso esperado é concedido.
  -Execução -> Pronto = O processo passa de execução para pronto por eventos gerados pelo sistema.
