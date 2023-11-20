# Performance nos nossos Apps
Falando sobre aplicativos performáticos, precisamos entender alguns pontos:

<v-click>

## O que é performance nos aplicativos?

</v-click>
<br/>
<v-click>

## Quais métricas existem?

</v-click>
<br/>
<v-click>

## Como medimos a performance?

</v-click>
<br/>
<v-click>

## Como resolvemos?

</v-click>

---
transition: fade-out
layout: image-left
image: /assets/performance/performance_metric_gpt.png
---

## O que é performance nos aplicativos?

<v-clicks>
    <li class='m-t-10'>
        <span style='font-size: 22px'>Navegação e animações flúidas</span>
    </li>
    <li>
        <span style='font-size: 22px'>Inicialização rápida</span>
    </li>
    <li>
        <span style='font-size: 22px'>Pouco loading</span>
    </li>
</v-clicks>

---
transition: fade-out
---

## Quais métricas existem?

<v-click>
    <div class='flex justify-center'>
        <img src='/assets/performance/frame_rate.jpg' class='w-120 m-t-10 rounded-md'/>
    </div>
</v-click>

<v-clicks>
    <li class='m-t-10'>
        <span style='font-size: 22px'>Métricas nativas (cpu, ram, vídeo)</span>
    </li>
    <li>
        <span style='font-size: 22px'>Árvore de renderização do React</span>
    </li>
    <li>
        <span style='font-size: 22px'>Tempo de inicialização</span>
    </li>
    <li>
        <span style='font-size: 22px'>Tamanho de arquivos</span>
    </li>
</v-clicks>

---
transition: fade-out
---

## Como a gente mede tudo isso?

<v-click>
    <div class='flex justify-center'>
        <img src='/assets/performance/flipper.gif' class='w-200'/>
    </div>
    <span style='font-size:18px'>Alexandre at Bam</span>
</v-click>

---
transition: fade-out
---

### React dev tools

<div class='flex justify-center'>
    <img src='/assets/performance/devtools.gif' class='w-150 m-t-4 rounded-md'/>
</div>

---
transition: fade-out
---

### Android profiling
Implementação do React Native
<div class='flex justify-center'>
    <img src='/assets/performance/native_profile.png' class='w-150 m-t-4 rounded-md'/>
</div>

---
transition: fade-out
---

### IOS profiling
Ferramentas do Xcode
<div class='flex justify-between'>
    <img src='/assets/performance/ios_profiling_1.png' class='w-80 m-t-4 rounded-md'/>
    <img src='/assets/performance/ios_profiling_2.png' class='w-120 m-t-4 rounded-md'/>
</div>

---
transition: fade-out
layout: image-left
image: /assets/performance/performance_gpt.png
---

## Quais soluções nós temos?

<v-clicks>
    <li class='m-t-10'>
        <span style='font-size: 22px'>Memoização para evitar re-render</span>
    </li>
    <li>
        <span style='font-size: 22px'>Code splitting</span>
    </li>
    <li>
        <span style='font-size: 22px'>Compressão de arquivos estáticos</span>
    </li>
    <li>
        <span style='font-size: 22px'>Lazy loading</span>
    </li>
</v-clicks>