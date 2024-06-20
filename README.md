# Nordestech_AtividadeN3

## Membros do Time 

<div>
    <ul>
        <li class="link">
            <a href="https://github.com/Dev-kyw3010" style="font-size:17px;color:#fff">Eduardo Kim</a>
            <span>;</span>
        </li>
        <li class="link">
            <a href="https://github.com/leebortnik" style="font-size:17px;color:#fff">Letícia Bortnik</a>
            <span>;</span>
        </li>
        <li class="link">
            <a href="https://github.com/RealTastes" style="font-size:17px;color:#fff">Walter Teles</a>
            <span>;</span>
        </li>
    </ul>
</div>

## Ciclo da Vida de uma Activity

> __É um conjunto de métodos que são chamados em diferentes momentos durante a existência de uma Activity . Esses métodos permitem gerenciar o estado da Activity e responder a eventos importantes de seu ciclo de vida .__

### Métodos de Uma Activity:

#### `onCreate(Bundle savedInstanceState)`:

+ Chamada quando a Activity é criada pela primeira vez .
+ Neste método, você deve realizar a inicialização da Activity, como configurar a interface do usuário, inicializar variáveis, etc.

#### `onStart()`:

+ É chamado quando a Activity se torna visível para o usuário.
+ Aqui você pode iniciar processos que precisam ser executados quando a Activity está visível, como iniciar serviços , atualizar a interface do usuário , etc.

#### `onResume()`:

+ Chamado quando a Activity entra no estado ativo e começa a interagir com o usuário. 
+ Neste método , você pode retomar operações que foram pausadas , como reprodução de áudio ou vídeo.

#### `onPause()`:

+ É chamado quando a Activity é interrompida e perde o foco , mas ainda está visível.
+ Neste método, você deve salvar o estado da Activity, pausar operações que não devem ser executadas em segundo plano, etc.

#### `onStop()`:

+ É chamado quando a Activity não está mais visível para o usuário.
+ Neste método, você deve parar operações que não devem ser executadas quando a Activity não está visível, como animações, atualizações de interface do usuário, etc.

#### `onDestroy()`:

+ É chamado quando a Activity está prestes a ser destruída.
+ Neste método, você deve liberar todos os recursos alocados pela Activity, como fechar conexões de banco de dados, parar serviços, etc.

#### `onSaveInstanceState(Bundle outState)`:

+ É chamado antes de a Activity ser destruída, para que você possa salvar o estado da Activity.
+ Neste método , você deve salvar todas as informações necessárias para restaurar o estado da Activity quando ela for recriada.

#### `onRestoreInstanceState(Bundle savedInstanceState)`:

+ É chamado após a Activity ser recriada, para que você possa restaurar o estado da Activity.
+ Neste método, você deve restaurar o estado da Activity usando as informações salvas no método [**onSaveInstanceState()**](#onsaveinstancestatebundle-outstate).

---
## Imagem de Demonstração

![Ciclo de Vida da Activity](/img/ciclo_de_vida_Activity.webp)


