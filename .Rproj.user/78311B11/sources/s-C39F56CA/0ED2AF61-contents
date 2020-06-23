# Przypisz zmienne
x <- 5
y <- 10

# Wykonaj dzialania
x+y
y-x
x*y
y/x
y^x

# Wykonaj wlasna funkcje 
liczby_1 <- function(d,e) {
  b <- d*e
  seq(b,100,by=10)
}
liczby_1 (2,4)

# Wykonaj sekwencje liczb od 1 do 30 co 2 
liczby_2 <-seq(1,30, by = 2)
liczby_2

# Stwórz wektor o nazwie liczby_2
liczby_3 <- c(x,y)
# Obejrzyj wektor oraz zbadaj ile liczb sie w nim znajduje (przy pomocy length)
liczby_3
length(liczby_3)

# Stworz nowa macierz liczby_4 zawierajaca liczby od 1 do 9 w 3 rzedach
liczby_4 <- matrix(1:9, byrow=TRUE, nrow = 3)
liczby_4

# Stworz data frame liczby_5 zawierajaca 3 oceny (dowolne) z "semestr 1", 
# oraz wskazanie czy jest to zaliczone (wartosc logiczna)
liczby_5 <- data.frame(semestr_1 =c(2,4,2),Zdane = c(F,T,F))
liczby_5

# Stworz liste liczby_6 zawierajaca każdy typ danych, zbadaj strukture 
#oraz uprosc ja do wektora
liczby_6 <- list(FALSE, c(3,4,5,6), "Warsztaty")
liczby_6
str(liczby_6)
unlist(liczby_6)

# Stworz liste faktorowa liczby_7 (dowolne dane jakosciowe ktore da sie uporzadkowac)
liczby_7 <- rep(c("d", "g", "a"), c(1,3,2))
liczby_7
factor(liczby_7,ordered=TRUE)

# Zainstaluj pakiet tidyverse
install.packages("tidyverse")
# Wgraj pakiet tidyverse do srodowiska programu
library(tidyverse)
# Zainstaluj pakiet danych gapminder
install.packages("gapminder")
# Wgraj dane gapminder do srodowiska programu
library(gapminder)
# Sprawdz zaladowane pakiety
library()

# Sprawdz poczatek i koniec gapminder
head(gapminder)
tail(gapminder)

#Sprawdz strukture gapminder
glimpse(gapminder)

#Wyciagnij dane z Azji o przewidywanej dlugosci zycia w roku 1952
gapminder %>%
  filter(continent == "Asia", year == 1952)

# Wyciagnij dane o przewidywanej dlugosci zycia w afryce od najdluzszej do 
# najkrotszej

gapminder %>%
  filter (continent =="Africa") %>%
  arrange (desc(lifeExp))

# Stwórz nowa kolumne w ktorej obliczysz calkowite pkb krajow azji w 1952 roku

gapminder %>%
  filter(continent=="Asia", year ==1952) %>%
  mutate(gdpTotal =(gdpPercap * pop))

# Stworz wykres kolumnowy pokazujcy srednie pkb na glowe na roznych kontynetach 
# w 1952 roku

wykres_1 <- gapminder %>%
  filter (year ==1952) %>%
  group_by (continent) %>%
  summarize (medianGdpPercap = median(gdpPercap))


ggplot (wykres_1,aes(x=continent,y =medianGdpPercap)) + geom_col()
