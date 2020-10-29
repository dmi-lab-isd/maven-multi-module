# Maven multi-module tutorial

Vengono mostrati i passi necessari per creare un progetto maven multi-modulo con IntelliJ. Il progetto sarà composto da:

- modulo parent (definisce le dipendenze e le configurazioni in comune)
	- modulo core
	- modulo service (dipende dal core) 

#### Creare un nuovo progetto
![](docs/fig1.png)

#### Usare Maven (anche senza archetype)
![](docs/fig2.png)
![](docs/fig3.png)

#### Aggiungiamo al pom.xml qualche dipendenza (es. JUnit)
![](docs/fig4.png)

#### Nel modulo parent, creare un nuovo modulo (core)
![](docs/fig5.png)
![](docs/fig6.png)

#### In automatico verrà aggiunto al core un riferimento al parent e viceversa
![](docs/fig7.png)
![](docs/fig8.png)

#### Aggiungiamo al parent altre configurazioni in comune tra i sotto-moduli (es. properties)
![](docs/fig9.png)

#### Sempre dal parent, creiamo un secondo sotto-modulo (service)
![](docs/fig10.png)

#### Anche questo avrà un riferimento al parent (e viceversa); aggiungiamo una dipendenza esplicita dal modulo core
![](docs/fig11.png)

#### Usando mvn install sul parent verranno installati tutti e tre i moduli (in maniera analoga per altri comandi, es. mvn test)
![](docs/fig12.png)
![](docs/fig13.png)