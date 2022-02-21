# Pergunta: Escreva um trecho de codigo que utiliza a funcao fork() e gera a seguinte hierarquia de processos:Alem da hierarquia, faca com que o processo G envie um sinal SIGUSR1 para o processo A e assim que o processo A receber o sinal ele deve enviar um sinal SIGUSR2 para o processo C.




#include <stdio.h>
#include <signal.h>
#include <sys/types.h>
#include <unistd.h>

void trata_SIGALRM(int signum){
    printf("Ai que sono! Queria dormir mais...\n");
}
int main(){
    pid_t pid;
    
    if ((pid = fork()) != 0)
    {
        signal(SIGALRM, trata_SIGALRM);
        pause();
    }
    else
    kill (getppid(), SIGALRM);
    return 0;
}
