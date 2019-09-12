# Przykładowe rozwiązania zadań

### Rozdział I

Zadanie, podpunkt 3.

```c++
#include <iostream>

using namespace std;

int main(){
    
    if(chlebNieJestKrojony()){
        wezNoz();
        pokrojChleb();
    }
    
    posmarujKromkeMaslem();
    polozPlasterekSera();
    
    return 0;
}
```

### Rozdział III

Napisz program, który wypisze twoje imię i nazwisko, a linię poniżej “Technik Informatyk”.

```c++
#include <iostream>

using namespace std;

int main(){
    
    cout<<"Adam Przykladowy"<<endl;
    cout<<"Technik Informatyk";
  	
    return 0;
}
```

### Rozdział IV

1. Spróbuj

   Oblicz w podobny sposób objętość `V` kuli o promieniu `r=10`. Możesz skorzystać z programu liczącego pole koła.

   ```c++
   #include <iostream>
   
   using namespace std;
   
   int main(){
       const float PI = 3.1415; 
       
       float r = 10; 
       float V = 1.33*PI*r*r*r; 
       
       cout<<"Objetosc: "<<V;
       
       return 0;
   }
   ```

2. Spróbuj
   Na podstawie programu powyżej napisz pętlę `for`, która wypisze kolejne `12` potęg liczby `2`. Następnie spróbuj wykorzystać do tego pętle `while`. 

   ```c++
   #include <iostream>
   
   using namespace std;
   
   int main(){
      
       int x = 2;
       
       for(int i=0;i<12;i++){	
           cout<<x<<", ";
           x = x*2;
       }
       
       cout<<endl;
       
       return 0;
   }
   ```

3. Spróbuj
   Napisz program, który wypisze liczby od 1 do 30, ale liczby podzielne przez 3 zastąpi słowem Fizz, liczby podzielne przez 5 zastąpi słowem Buzz, a liczby podzielne przez 3 i 5 zastąpi słowem FizzBuzz.

   ```c++
   #include <iostream>
   
   using namespace std;
   
   int main(){
      
       for(int i=1;i<=30;i++){
           if(i%15 == 0)
               cout<<"FizzBuzz ";
           else if (i%5 == 0)
               cout<<"Buzz ";
           else if (i%3 == 0)
               cout<<"Fizz ";
           else
               cout<<i<<" ";
       }
       
       return 0;
   }
   ```

   

###### Zadanie

Za pomocą uzyskanej wiedzy o pętlach oraz instrukcjach warunkowych spróbuj napisać program, który wypisze na ekranie prostokąt o wymiarach `4` x `5` za pomocą znaku `#`.

*Przydatne okazać się mogą operatory ||, czyli \*lub* oraz `&&`, czyli *i*. Operator `||` zwraca prawdę w momencie kiedy przynajmniej jeden z warunków jest prawdziwy, np. `2 == 2 || 2 == 4` zwróci `true`, ponieważ `2 == 2` zwraca prawdę. Natomiast operator `&&` zwraca prawdę tylko wtedy kiedy wszystkie warunki są prawdziwe, np. `2 == 2 && 3 == 3` zwróci `true`, a `2 == 2 && 2 == 4` zwróci `false`.*

*Podpowiedź: Wykorzystaj pętle w pętli oraz zastanów się jakie wartości mają zmienne x oraz y na krawędziach takiego prostokąta.*

```c++
#include <iostream>

using namespace std;

int main(){
   
    for(int y = 0 ;y < 5 ;y++){
        for(int x = 0; x < 4 ; x++){
            if ( x == 0 || x == 3 || y == 0 || y == 4){
            	cout<<"#";
        	}
        }
        cout<<endl;
    }
    
    return 0;
}
```

