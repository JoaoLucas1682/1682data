## Microsoft Edge

### A função edgeCopilotPrivate.launchVision

**Esta função foi testada no Microsoft Edge 143.0.3650.96 e funciona corretamente**

Inicia o modo do Copilot Vision no navegador Microsoft Edge.

Sintaxe:
```
window.chrome.edgeCopilotPrivate.launchVision(string: form_code, optional: function callback)
```

**Nota:** Eu não testei optional function callback

Se você não passa form_code, dá um erro semelhante a este:
```
Uncaught TypeError: Error in invocation of edgeCopilotPrivate.launchVision(string form_code, optional function callback): No matching signature.
```

No caso, como não sei o form_code, passei qualquer número (no caso, 123) e iniciou o modo do Copilot Vision. Aqui está a função que usei:
```sj
window.chrome.edgeCopilotPrivate.launchVision('123')
```
E quando executei, deu um Promise:
```
Promise {<pending>}
- [[Prototype]]: Promise
- [[PromiseState]]: "fulfilled"
- [[PromiseResult]]: true
```
