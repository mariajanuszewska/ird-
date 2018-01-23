# ird-
ZAJĘCIA 1

1. instalowanie pakietów
install.packages("data.table")
library(data.table)

2. funkcje matematyczne
a/2

10 %% 3   # reszta z dzielenia
10 %/% 3  # liczba calkowita z dzielenia
938749324789203 %% 10 # ostatnia cyfra
a <- 2
b <- 3
a == b
a > b
a < b
a != b
3 <= 5
3 <=5 | 10 > 100 # lub
3 <=5 & 10 > 100 # oraz
sqrt(16) 
abs(-99)
sum(5, 6)
cos(pi)
sin(pi)
log(4)
log(10)
log10(10)
logb(56, base = 5)
logb(base = 5, x = 56)
logb(5, 56)
exp(0)
round(pi, 2)

ceiling(3.3)
floor(3.6)
trunc(5.99)
trunc(-1.5)
floor(-1.5)
ceiling(-1.5)

round(6.592, digits = 2)
factorial(4) # silnia

typeof(1)
class(1)

3. wektory
v1 <- 1:10
v1
v2 <- c(1,4,6,3,11,3)
v2
typeof(v2)
sort(v2)
length(v2)
unique(v2)

v3
v3[3] # 3ci element
v1[2:4] # element od 2giego do 4tego
v1[c(2,3,10)] # element 2, 3 i 10ty
v1[v1<4 | v1>6]
v1[v1>4 & v1<8]
v3[-1] # indeks z minusem oznacza "wszystko oprĂłcz tego"
vec_txt_u <- unique(vec_txt) # unikatowe wartoĹ›ci
vec_txt_u <- sort(vec_txt_u)
nchar('SGH') #cyfra - ilość liter
k <- sqrt(w)

4. inne operacje

x <- 1:100
x
3 %in% x # czy 3 jest w zbiorze x?
c(3, 100, 2000) %in% x # które elementy tego wektora sÄ… w zbiorze x?

seq(-1, 1, 0.1)
seq(from=-1,to=1,length=21)
seq(1, 1,length = 21)
seq(length=21, from=-1, by=0.1)
rep(1, 5) #potórzenie 1 piec razy
rep(1:2, times = 3)
rep(1:2,each = 3)


5. Macierze
m1 <- matrix (1:100, 10, 10, byrow = T) #kolejne liczby po kolei wierszami
m1
m2 <- matrix (1:100, 10, 10) #po kolei kolumnami 
m2
seq(from=-1,to=1,length=20)
m3 <- matrix(seq(from=-1,to=1,length=20), 4 ,5)
m3
m4 <- matrix(rep(1:3, times = 3), 3, 3)
m4
t(m1) #transpozycja
dim(m1) #wymiary
m1 %*% m2#mnozenie macierzy
nrow(m1)
ncol(m1) #ile wierszy/kolumn
cbind(m1, m2)
rbind(m1, m2) #przylaczenie do kolumn/wierszy
m1 == m2 # ktore elementy m1 = elementom m2 
any(m1 == m2)
all(m1 == m2) 
m1[2,3] # element z wiersz, kolumna
m1[1,] #wiersz
m1[,3] #kolumna
m1[m1>mean(m1)]

6. Listy
lista <- list (
lista[3] # 3 element listy
lista[[3]][1]      # pierwszy element trzeciego elementu listy
lista[["c"]]
lista$c # odwołanie
c(TRUE, TRUE) &  c(FALSE, TRUE) #porownanie pierwszych elementów

7. tabele czestości
table(plec)
t <- table(plec,wiek)
t

8. ramka danych
df1 <- data.frame(v1= c(10,20,30), v2= c("ala", "ma", "kota"), v3= c(NA, 13, NaN), v4 = c(TRUE, FALSE, TRUE))
df1
names(df1) <- c('wiek', 'haslo', 'wiek_brata', 'ma_siostre')
df1

ZADANIE 1
stwórz wektor o nazwie indeks, który będzie się składał z elementów będącymi poszczególnymi cyframi z numeru Twojego indeksu. 
Sprawdź, jakiego jest typu. 
Zamień trzeci element na liczbę 100.
Podnieś 1 i 2 element do kwadratu
Sprawdź które elementy są większe od 3 i mniejsze lub równe 8
Posortuj malejąco
Stwórz wektor indeks2, ktory bedzie dukrotnoscia wektora indeks
Dodaj elementy wektora indeks2, podziel przez 7.3 i zaokrąglij wynik do 2 miejsc po przecinku

indeks <- c(2, 5, 3, 4, 9, 2, 7)
typeof(indeks)
indeks[3] <- 100
indeks[1:2] <- indeks[1:2]^2
indeks[indeks > 3 & indeks <= 8]
indeks <- sort(indeks, decreasing = TRUE)
indeks2 <- 2 * indeks
round(sum(indeks2) / 7.3, 2)

ZADANIE 2
StwÓrz ramke danych "dane" z nastepujacymi rekordami:
imie, drugie imie, jeĹĽeli nie ma, to NA, wiek, płeć - jako czynnik (factor)
informacjÄ o tym, czy osoba ma status studenta (tak lub nie)
zawierającymi dane Twoje i trzech innych osób 
dane1 <- data.frame(imie = c('Jan', 'Adam', 'Ewa', 'Justyna'),
                   drugie_imie = c('Chryzostom', 'Jan', NA, 'Maria'),
                   wiek = c(24, 25, 23, 31),
                   plec = factor(c('m', 'm', 'f', 'f')),
                   status_studenta = c(TRUE, FALSE, TRUE, FALSE))

# Check:
class(dane$plec) == 'factor' # TRUE





