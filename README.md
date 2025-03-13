# C1
Anagrams
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define char_count 256
int main() {
    char s1[100],s2[100];
    int count[ char_count]={0};
    int i;
    printf("Enter the first string:"); scanf("%s",s1);
   printf("Enter the second string:"); 
        scanf("%s",s2);
        if(strlen(s1)!=strlen(s2)){
            printf("The strings are not anagram with each other other. \n");
            return 0;
    for(i=0;s1[i]&&s2[i];i++){
    count[tolower((unsigned char)s1[i])]++;
    count[tolower((unsigned char)s2[i])]--;
    }
    for(i=0;i<char_count;i++){
        if(count[i]!=0){
            printf("The strings are not anagram with each other.\n");
            return 0;
        }
    }
        }
        printf("The strings are anagrams.\n");
    return 0;
}
