## Fabric <mdi-factory />
Uma nova arquitetura que substitui completamente a Bridge.
<v-click>
    <img src='/assets/rn-architecture/fabric/fabric_diagram.jpg' class='w-full' />
</v-click>

---
transition: fade-out
---

### JSI (JavaScript Interface)
É uma API para "embedar" um mecanismo JavaScript em um aplicativo C++. O Fabric o utiliza para se comunicar entre o lado nativo e  o React.

<v-click>
<p>
    Basicamente, é um objeto JavaScript que contém referências de C++, o que nos possibilita acessar o UI Manager diretamente, e vice-versa
</p>
</v-click>

<v-click>

```c++
getNativeModule('Camera').getPictures({video:true})
// C++
Camera:HostObject {
    Value get(propName) {
        switch (propName) {
            case 'getPictures':
                // Call Android/iOS API
                return JavaCameraManager.takePic();
        }
    }
}
```

</v-click>

---
transition: fade-out
---

### Caso de uso
Upload de imagem utilizando bridge
<img src='/assets/rn-architecture/fabric/jsi_old_diagram.jpg' class='w-full' />


---
transition: fade-out
---
### Caso de uso
Upload de imagem utilizando JSI
<img src='/assets/rn-architecture/fabric/jsi_diagram.jpg' class='w-full' />

---
transition: fade-out
---
### As três fases
O fabric é dividido em: Render, Commit e Mount
<div class='grid grid-cols-3 m-t-2 divide-x w-full h-10 border-b-1' v-click='1'>
    <div class='p-l-2'>
        <h3 class='text-center'>JavaScript</h3>
    </div>
    <div class='col-span-2 p-l-2'>
        <h3 class='text-center'>Plataforma Mobile</h3>
    </div>
</div>
<div class='grid grid-cols-3 divide-x w-full h-88 m-t-2'>
    <div class='flex flex-col' v-click='1'>
       <h4 class='text-center'>Render</h4>
       <span style='font-size:12px' class='text-center'>React JS</span>
       <img src='/assets/rn-architecture/fabric/fabric_render.jpg' class='w-45'/>
    </div>
   <div class='flex flex-col' v-click='2'>
       <h4 class='text-center'>Commit</h4>
       <span style='font-size:12px' class='text-center'>React Native</span>
       <img src='/assets/rn-architecture/fabric/fabric_commit.jpg' class='w-full m-t-2'/>
    </div>
   <div class='flex flex-col' v-click='3'>
       <h4 class='text-center'>Mount</h4>
       <span style='font-size:12px' class='text-center'>Native screen</span>
       <img src='/assets/rn-architecture/fabric/fabric_mount.jpg' class='w-full m-t-2'/>
    </div>
</div>

---
transition: fade-out
---
### Recap
<img src='/assets/rn-architecture/fabric/fabric_diagram.jpg' class='w-full' />