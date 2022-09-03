# find-the-alphabet
# A word S consisting of only lowercase letters of the alphabet is given. For each alphabet, write a program that prints the position of the first occurrence if it is included in the word, and -1 if it is not included in the word. is the 1st position.) 알파벳 소문자로만 이루어진 단어 S가 주어진다. 각각의 알파벳에 대해서, 단어에 포함되어 있는 경우에는 처음 등장하는 위치를, 포함되어 있지 않은 경우에는 -1을 출력하는 프로그램을 작성하시오.(단어의 첫 번째 글자는 0번째 위치이고, 두 번째 글자는 1번째 위치이다.)
# c program
# case 1
#include <stdio.h>
#include <string.h>
int main(void){
	char s[100];
	int len;
	printf("입력:");
	scanf("%s",&s);
	len=strlen(s);
	char ch='a';
	int cnt=0;
	char *p; //포인터를 이용
	p=s;
	for(ch='a';ch<='z';ch++){
		cnt=0;
	for(p=s;p<s+len;p++){
		if(*p==ch){
		printf("%d",p-s);
		cnt++;
		break;}}
    if(cnt==0){
    	printf("-1");
	}}

	return 0;
}
#include <stdio.h> int main(void){    char word[100] = { 0 };    scanf("%s", word);    for (int i = 97; i <= 122; i++) {        int j = 0;        while (word[j] != 0) {  if (word[j] == (char)i) break;   j++; }        
if (word[j] == (char)i) printf("%d ", j);        else printf("-1 ");    }}
#input--> baekjoon
#result--> 1 0 -1 -1 2 -1 -1 -1 -1 4 3 -1 -1 7 5 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1 -1
