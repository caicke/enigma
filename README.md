# enigma
Enigma SBC

######## C #############

#include <stdio.h>
#include <string.h>

int main(){
    char msg[30]; /*= "AAAAABABABABABABABABA";*/
    char crib[30]; /*= "ABA";*/
    
    scanf("%s", msg);
    scanf("%s", crib);
    
    int qtd = 0;
    int i;
    int j;
    
    for (i=0; i < (strlen(msg)-strlen(crib));i++){
        for (j =0; j < strlen(crib);j++){
            if (crib[j] == msg[i+j]){
                break;
            }
        }
        if (strlen(crib)==j){
            qtd+= 1;
        }
    }
    
    printf("%d\n",qtd);
    
    return 0;
}

#######################################################

########### Python #########################################

def main():
  msg = input()
  crib = input()
  i = 0
  qtd = 0

  while i < len(msg)-len(crib):
      j = 0
      while j < len(crib):
          if crib[j] == msg[i+j]:
              break
          j+= 1
      if len(crib)==j:
          qtd+= 1
      i += 1
  print(qtd,"\n")
  
  return 0;
