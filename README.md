## CRUD Ionic 3 + Angular 4 + Firebase 4 + AngularFire2 4.0

Instalar o NodeJs  
Instalar o Atom  

$ npm install -g ionic@latest  
$ ionic start meuProjeto sidemenu  
$ cd ./meuProjeto  
$ npm install angularfire2 firebase --save  
$ npm install promise-polyfill --save-exact  
$ ionic serve  

$ ionic g page alunosPage  
$ ionic g page alunoCriarPage  
$ ionic g page alunoEditarPage  
$ ionic g page alunoDetalhePage  

### No arquivo app.module.ts:  

```typescript
import { AngularFireModule } from 'angularfire2';  

export const environment = {  
  production: false,  
  firebase: {  
    apiKey: '<your-key>',  
    authDomain: '<your-project-authdomain>',  
    databaseURL: '<your-database-URL>',  
    projectId: '<your-project-id>',  
    storageBucket: '<your-storage-bucket>',  
    messagingSenderId: '<your-messaging-sender-id>'  
  }  
};  

@NgModule({  
  imports: [  
    ...,  
    AngularFireModule.initializeApp(environment.firebase)  
  ],  
  ...  
})  
export class AppModule {}
```

## Para a exportação
$ ionic cordova platform add `<platform>`  
$ ionic cordova build `<platform>`  
