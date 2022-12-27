#include <stdio.h> //biblioteca de comunicacao com o usuario
#include <stdlib.h> //espaco da memoria biblioteca de alocacao
#include <locale.h> //biblioteca de alocacoes de texto por regiao
#include <string.h> //biblioteca responsavel por cuidar das string

int registro ()

{
    char arquivo[40];
    char cpf[40];
    char nome[40];
    char sobrenome[40];
    char cargo[40];

    printf("Por favor, digite o CPF a ser cadastrado: ");
    scanf("%s", cpf);

    strcpy(arquivo, cpf); //responsavel por copiar os valores das strings

    FILE *file; //cria o arquivo
    file = fopen(arquivo, "w"); //cria o arquivo
    fprintf(file,cpf); //salva o valor da var
    fclose(file); //fecha o arquivo

    file = fopen(arquivo, "a");
    fprintf(file,",");
    fclose(file);

    printf("Digite um nome a ser cadastrado: ");
    scanf("%s",nome);

    file = fopen(arquivo, "a");
    fprintf(file,nome);
    fclose(file);
    
    file = fopen(arquivo, "a");
    fprintf(file,",");
    fclose(file);

    printf("Digite o sobrenome a ser cadastrado: ");
    scanf("%s", sobrenome);

    file = fopen(arquivo, "a");
    fprintf(file,sobrenome);
    fclose(file);

    file = fopen(arquivo, "a");
    fprintf(file,",");
    fclose(file);

    printf("Digite o cargo a ser cadastrado: ");
    scanf("%s", cargo);

    file = fopen(arquivo, "a");
    fprintf(file,cargo);
    fclose(file);

    system("pause");

}

int consulta ()

{
    setlocale (LC_ALL, "portuguese"); //definicao do idioma

    char cpf[40];
    char conteudo[200];

    printf("Digite o CPF a ser consultado: ");
    scanf("%s",cpf);

    FILE *file;
    file = fopen(cpf, "r");
    
    if(file == NULL)
    {
        printf("Não foi possível abrir o arquivo. Dados não localizados. \n");
    }

    while(fgets(conteudo, 200, file) != NULL)
    {
        printf("\n Essas são as informações do usuário: ");
        printf("%s", conteudo);
        printf("\n\n");
    }
    system("pause");
}


int deletar ()
    
{
    printf("Você escolheu a opção para deletar nomes\n");
    system("pause");        
}



int main ()
{
   int opcao=0; //definindo as variaveis
   int laco=1;

   for (laco=1;laco=1;)
   {

        system("clear");
    
        setlocale (LC_ALL, "portuguese"); //definicao do idioma
   
        printf("### Cartório da EBAC ### \n \n"); //inicio do menu
        printf("Escolha a opção desejada do menu: \n \n");
        printf("\t1 - Registrar nomes\n");
        printf("\t2 - Consultar nomes\n");
        printf("\t3 - Deletar nomes\n \n \n"); 

        printf("Digite a opção: "); //fim do menu
    
        scanf("%d", &opcao); //armazenamento da escolha do usuario

        system("clear"); //como o comando CLS deu erro, busquei uma alternativa e o CLEAR funcionou

        switch(opcao)
        {
                case 1:
                registro();
                break;

                case 2:
                consulta();
                break;

                case 3:
                deletar();
                break;

                default: 
                printf("Essa opção não está disponivel");
                system("pause");
                break;
        }
        
     }
}
