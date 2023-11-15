## Bridge <mdi-bridge />
Esse diagrama representa o modelo de threads na arquitetura Bridge.

<img src='/assets/rn-architecture/bridge/bridge_diagram.jpg' class='w-full' />

---
transition: fade-out
---

### Threads

<br/>
<div class='grid grid-cols-3 divide-x w-full h-100'>
    <div class='flex flex-col' v-click='1'>
        <h3 class='text-center'>JS Thread</h3>
        <br />
        <div class='p-x-2' v-click='2'>
            <li>Código React</li>
            <img src='/assets/rn-architecture/bridge/component_tree.jpg' />
        </div>
    </div>
    <div class='flex flex-col' v-click='3'>
        <h3 class='text-center'>Shadow Thread</h3>
        <br />
        <div class='p-x-2' v-click='4'>
            <li>Estilização e posição</li>
            <div class='flex justify-center'>
                <img src='/assets/rn-architecture/bridge/rendered_tree.jpg' class='w-60'/>
            </div>
        </div>
    </div>
    <div class='flex flex-col' v-click='5'>
        <h3 class='text-center'>Main Thread</h3>
        <br />
        <div class='p-x-2' v-click='6'>
            <li>Desenho da UI</li>
            <div class='flex justify-center'>
                <img src='/assets/rn-architecture/bridge/tree_in_mobile.jpg' class='w-45'/>
            </div>
        </div>
    </div>

</div>

---
transition: fade-out
---

### JS Thread
É responsável por executar todo o nosso código JS

<img src='/assets/rn-architecture/bridge/js_thread.jpg' />

---
transition: fade-out
---

### Shadow Thread
É responsável por calcular a estilização e o posicionamento dos componentes

<img src='/assets/rn-architecture/bridge/shadow_thread.jpg' />

---
transition: fade-out
---

### Main Thread
É responsável por "desenhar", metrificar e escutar eventos de forma nativa

<div class='flex justify-center'>
    <img src='/assets/rn-architecture/bridge/main_thread.jpg' class='w-140'/>
</div>

---
transition: fade-out
---

### E a comunicação entre o JS e o lado nativo?

<v-clicks>
    <div class='flex justify-center'>
        <img src='/assets/rn-architecture/bridge/bridge.jpg' class='w-140'/>
    </div>
    <li class='mt-6'>Operações em Batch</li>
    <li>Serialização</li>
    <li>Assíncrono</li>
</v-clicks>

---
transition: fade-out
---
### Fluxo de evento

<div class='flex justify-center'>
    <img src='/assets/rn-architecture/bridge/event_diagram.jpg' class='w-135' />
</div>

---
transition: fade-out
---
### Grande problema da Bridge

<div class='flex justify-between m-t-6'>
    <img src='/assets/rn-architecture/bridge/bridge_problem.gif' class='w-60'/>
    <img src='/assets/rn-architecture/bridge/bridge_problem.jpg' class='w-135' />
</div>
