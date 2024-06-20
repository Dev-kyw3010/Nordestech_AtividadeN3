# Nordestech_AtividadeN3

## Membros do Time 

<div>
    <ul>
        <li class="link">
            <a href="https://github.com/Dev-kyw3010" style="font-size:18px;color:#fff;">Eduardo Kim</a>
            <span>;</span>
        </li>
        <li class="link">
            <a href="https://github.com/leebortnik" style="font-size:18px;color:#fff;">Letícia Bortnik</a>
            <span>;</span>
        </li>
        <li class="link">
            <a href="https://github.com/RealTastes" style="font-size:18px;color:#fff;">Walter Teles</a>
            <span>;</span>
        </li>
    </ul>
</div>

## Ciclo da Vida de uma Activity

### Introdução 

> A __Activity__ é um componente fundamental que representa uma única tela com uma interface do usuário. O seu ciclo de vida descreve as diversas fases pelas quais uma activity passa desde a sua criação até a sua destruição , e compreender e gerenciar adequadamente esse ciclo é essencial para construir aplicativos responsivos e eficientes .
> 
Além disso , o ciclo de vida é composto por vários métodos que são chamados pelo sistema Android em diferentes momentos. Estes métodos são classificados em três grupos principais :

1. [ __Métodos de Criação e Inicialização__](#métodos-de-criação-e-inicialização)
2. [__Métodos de Parada e Reinício__](#métodos-de-parada-e-reinício)
3. [__Métodos de Destruição__](#métodos-de-destruição)


## Métodos de Criação e Inicialização

__`onCreate()`__ = Esse método é o primeiro a ser chamado quando a _Activity_ é criada. Ele é usado para inicializar a _Activity_ , incluindo a configuração da interface do usuário e a inicialização de componentes essenciais.
* __Uso Comum__ = Configuração  da UI , inicialização de variáveis , vinculação de layouts usando <span style="color:#ff00aa">setContentView()</span>
``` Kotlin

    override fun onCreate(savedInstanceState: Bundle?){
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
    }
```
---
 __`onStart()`__ = Após o _onCreate()_ , o próximo método é o __onStart()__ , esse método indica que a _Activity_ está prestes a se tornar visível para o usuário.
* __Uso Comum__: Configurações que devem ser feitas quando a Activity está visível, mas ainda não está no foco interativo.

``` kotlin
    override fun onStart(){
        super.onStart()
        // Código para reiniciar atualizações ou animações , etc 
    }
```
---
__`onResume()`__ = Esse método é chamado quando a _Activity_ começa a interagir com o usuário. A partir desse momento a _Activity_ está em primeiro plano e pronta para receber entradas do usuário.
* __Uso Comum__: Retomar atividades pausadas, como animações, áudio ou vídeo.

``` kotlin

    override fun onResume(){
        super.onResume()
        // Reiniciar processos que estava pausados
    }
```
## Métodos de Parada e Reinício

__`onPause()`__ = Esse método é chamado quando a _Activity_ não está mais em primeiro plano , mas ainda está visível. É um momento apropriado para salvar o estado da _Activity_ e pausar as operações que não são mais necessárias .
* __Uso Comum__: Salvar dados temporários, liberar recursos que podem ser retomados quando a *Activity* voltar a interagir.
``` kotlin
    override fun onPause() {
        super.onPause()
        // Código para pausar operações.
    }
```
---
__`onStop()`__ = Esse método é chamado quando a _Activity_ não é mais visível para o usuário. Neste ponto, a _Activity_ pode estar prestes a ser destruída ou pode ser retomada posteriormente, como quando o aplicativo é colocado em segundo plano. A gerência desse método é de suma importância, já que é responsável por todas as atividades  que continuam rodando quando o aplicativo não está aberto e as que não continuarão rodando.


* __Uso Comum:__ Gerência de atividades quando o aplicativo não está aberto.
```kotlin
override fun onStop() {
    super.onStop()
    // Administração de atividades em segundo plano.
}
```

__`onRestart()`__ = 
## Métodos de Destruição

__`onDestroy()`__ = O onDestroy é basicamente a última chamada recebida antes que a __Activity__ seja finalizada. Pode acontecer de algumas formas, como por exemplo o sistema expurgar a Activity para economizar espaço ou quando alguém dá trigger no "finish()". Nunca deve ser utilizado para chamadas importantes que ficam ativadas após o fim do processo, já que pode causar a inutilização das mesmas, o correto seria utilizar o onStop ou onPause.

* __Uso Comum__: Realização de operação final antes da destruição da Activity.
```kotlin
    override fun onDestroy() {
        super.onDestroy()
        // Usado para liberar recursos finais.
    }
```


---
# Imagem de Demonstração

![Ciclo de Vida da Activity](/img/ciclo_de_vida_Activity.webp)


