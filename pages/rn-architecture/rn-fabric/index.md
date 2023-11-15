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